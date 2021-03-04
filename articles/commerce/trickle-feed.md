---
title: إنشاء أوامر تستند إلى التغذية المستمرة لحركات متجر البيع بالتجزئة
description: يصف هذا الموضوع إنشاء أوامر تستند إلى التغذية المستمرة لحركات المتجر في Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 09/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1f864fd6e3aa62cabd039922ed55ad5f7714f0ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991310"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a><span data-ttu-id="2c4f3-103">إنشاء أوامر تستند إلى التغذية المستمرة لحركات متجر البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="2c4f3-103">Trickle feed-based order creation for retail store transactions</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2c4f3-104">في الإصدار 10.0.4 من Dynamics 365 Retail والإصدارات السابقة، يعتبر ترحيل كشوف الحسابات إحدى عمليات نهاية اليوم ويتم ترحيل جميع الحركات في الدفاتر في نهاية اليوم.</span><span class="sxs-lookup"><span data-stu-id="2c4f3-104">In Dynamics 365 Retail versions 10.0.4 and earlier, statement posting is an end-of-day operation and all transactions are posted in the books at the end of the day.</span></span> <span data-ttu-id="2c4f3-105">عندئذٍ، يجب معالجة الحركات الكبيرة في غضون فاصل زمني محدد، مما يؤدي في بعض الأحيان إلى نشوء حالات فشل في ترحيل حمل العمل والتأمين وكشوف الحسابات.</span><span class="sxs-lookup"><span data-stu-id="2c4f3-105">Large transactions must then be processed in a limited time window, sometimes resulting in load and locks and statement posting failures.</span></span> <span data-ttu-id="2c4f3-106">ويتعذر أيضًا على بائعي التجزئة التعرف على الإيرادات والمدفوعات في دفاترهم خلال اليوم.</span><span class="sxs-lookup"><span data-stu-id="2c4f3-106">Retailers also can't recognize revenue and payments in their books throughout the day.</span></span>

<span data-ttu-id="2c4f3-107">مع وظيفة إنشاء أوامر تستند إلى التغذية المستمرة التي تم تقديمها في الإصدار 10.0.5 من Retail، تتم معالجة الحركات خلال اليوم، في حين تتم معالجة التسوية المالية لطرق الدفع والحركات الأخرى لإدارة النقدية في نهاية اليوم.</span><span class="sxs-lookup"><span data-stu-id="2c4f3-107">With trickle feed-based order creation introduced in Retail version 10.0.5, transactions are processed throughout the day, and only the financial reconciliation of tenders and other cash management transactions are processed at the end of the day.</span></span> <span data-ttu-id="2c4f3-108">تقوم هذه الوظيفة بتقسيم حمل عمل إنشاء أوامر المبيعات والفواتير والمدفوعات خلال اليوم، مما يوفر أداء أفضل والقدرة على التعرف على الإيرادات والمدفوعات في الدفاتر في وقت قريب من الحقيقي‬.</span><span class="sxs-lookup"><span data-stu-id="2c4f3-108">This functionality splits the load of creating sales orders, invoices, and payments throughout the day, providing better perceived performance and the ability to recognize revenue and payments in the books in near real-time.</span></span> 


## <a name="how-to-use-trickle-feed-based-posting"></a><span data-ttu-id="2c4f3-109">كيفية استخدام الترحيل الذي يستند إلى التغذية المستمرة</span><span class="sxs-lookup"><span data-stu-id="2c4f3-109">How to use trickle feed-based posting</span></span>
  
1. <span data-ttu-id="2c4f3-110">لتمكين ترحيل حركات البيع بالتجزئة التي تستند إلى التغذية المستمرة‬، قم بتمكين الميزة الموجودة باسم **كشوف حساب البيع بالتجزئة - التغذية المستمرة** باستخدام إدارة الميزات.</span><span class="sxs-lookup"><span data-stu-id="2c4f3-110">To enable trickle feed-based posting of retail transactions, enable the feature named **Retail statements - Trickle feed** using Feature management.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="2c4f3-111">وقبل تمكين الميزة، تأكد من عدم وجود كشوف حسابات معلّقة في انتظار الترحيل.</span><span class="sxs-lookup"><span data-stu-id="2c4f3-111">Before you enable the feature, make sure that no pending statements are waiting to be posted.</span></span>

2. <span data-ttu-id="2c4f3-112">سيتم تقسيم مستند كشف الحساب الحالي إلى نوعين: كشف حساب الحركات والقائمة المالية.</span><span class="sxs-lookup"><span data-stu-id="2c4f3-112">The current statement document will be split into two types: transactional statement and financial statement.</span></span>

      - <span data-ttu-id="2c4f3-113">سيقوم كشف حساب الحركات بانتقاء جميع الحركات غير المرحّلة والحركات التي تم التحقق من صحتها، وينشئ دفاتر يومية لأوامر المبيعات وفواتير المبيعات والمدفوعات والخصومات، وحركات الإيرادات والمصروفات وفق الوتيرة التي تريد تكوينها.</span><span class="sxs-lookup"><span data-stu-id="2c4f3-113">The transactional statement will pick up all unposted and validated transactions and create sales orders, sales invoices, payment and discount journals, and income-expense transactions at the cadence that you configure.</span></span> <span data-ttu-id="2c4f3-114">يجب تكوين هذه العملية كي تعمل وفق تكرار عالٍ بحيث يتم إنشاء المستندات عند تحميل الحركات إلى Headquarters عبر وظيفة P.</span><span class="sxs-lookup"><span data-stu-id="2c4f3-114">You should configure this process to run at a high frequency so that documents are created when the transactions are uploaded into Headquarters through the P-job.</span></span> <span data-ttu-id="2c4f3-115">مع كشف الحركات الذي ينشئ أوامر المبيعات وفواتير المبيعات، لا حاجة حقيقية لتكوين الوظيفة الدُفعية **ترحيل المخزون**.</span><span class="sxs-lookup"><span data-stu-id="2c4f3-115">With the transactional statement that already creates sales orders and sales invoices, there is no real need to configure the **Post inventory** batch job.</span></span> <span data-ttu-id="2c4f3-116">ومع ذلك، يمكنك مع ذلك استخدامه لتلبية احتياجات عمل معينة قد تكون لديك.</span><span class="sxs-lookup"><span data-stu-id="2c4f3-116">However, you can still use it to meet specific business requirements that you may have.</span></span>  
      
     - <span data-ttu-id="2c4f3-117">تم تصميم القائمة المالية بحيث يتم إنشاؤها في نهاية اليوم وهي تدعم فقط أسلوب الإقفال **وردية**.</span><span class="sxs-lookup"><span data-stu-id="2c4f3-117">The financial statement is designed to be created at the end of the day and only supports the closing method of **Shift**.</span></span> <span data-ttu-id="2c4f3-118">وسيقتصر كشف الحساب هذا على التسوية المالية ولن ينشئ إلا دفاتر اليومية لمبالغ الفروقات بين المبلغ المحسوب ومبلغ الحركة لطريق الدفع المختلفة، بالإضافة إلى دفاتر اليومية لحركات إدارة النقدية الأخرى.</span><span class="sxs-lookup"><span data-stu-id="2c4f3-118">This statement will be limited to financial reconciliation and will only create the journals for the difference amounts between counted amount and transaction amount for the different tenders, along with journals for other cash management transactions.</span></span>   

3. <span data-ttu-id="2c4f3-119">لحساب كشف حساب الحركات، انتقل إلى **Retail وCommerce > تكنولوجيا معلومات Retail وCommerce > ترحيل نقطة البيع > حساب كشوف حسابات الحركات على دُفعات**.</span><span class="sxs-lookup"><span data-stu-id="2c4f3-119">To calculate the transactional statement, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate transactional statements in batch**.</span></span> <span data-ttu-id="2c4f3-120">لترحيل كشوف حسابات الحركات على دُفعات، انتقل إلى **Retail وCommerce > تكنولوجيا معلومات Retail وCommerce > ترحيل نقطة البيع > ترحيل كشوف حسابات الحركات على دُفعات**.</span><span class="sxs-lookup"><span data-stu-id="2c4f3-120">To post the transactional statements in batch, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Post transactional statements in batch**.</span></span>

4. <span data-ttu-id="2c4f3-121">لحساب القائمة المالية، انتقل إلى **Retail وCommerce > تكنولوجيا معلومات Retail وCommerce > ترحيل نقطة البيع > حساب القوائم المالية على دُفعات**.</span><span class="sxs-lookup"><span data-stu-id="2c4f3-121">To calculate the financial statement, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate financial statements in batch**.</span></span> <span data-ttu-id="2c4f3-122">لترحيل القوائم المالية، انتقل إلى **Retail وCommerce > تكنولوجيا معلومات Retail وCommerce > ترحيل نقطة البيع > ترحيل القوائم المالية على دُفعات**.</span><span class="sxs-lookup"><span data-stu-id="2c4f3-122">To post the financial statements in batch, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Post financial statements in batch**.</span></span>

> [!NOTE]
> <span data-ttu-id="2c4f3-123">تمت إزالة عناصر القائمة **Retail وCommerce > تكنولوجيا معلومات Retail وCommerce > ترحيل نقطة البيع > حساب الكشوف على دُفعات‬** و **Retail وCommerce > تكنولوجيا معلومات Retail وCommerce > ترحيل نقطة البيع > ترحيل الكشوف على دُفعات‬** مع هذه الميزة.</span><span class="sxs-lookup"><span data-stu-id="2c4f3-123">The menu items **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate statements in batch** and **Retail and Commerce > Retail and Commerce IT > POS Posting > Post statements in batch** are removed with this new feature.</span></span>

<span data-ttu-id="2c4f3-124">كطريقة بديلة، يمكن إنشاء أنواع كشوف الحسابات والقوائم المالية يدويًا.</span><span class="sxs-lookup"><span data-stu-id="2c4f3-124">Alternately, transactional and financial statement types can be created manually.</span></span> <span data-ttu-id="2c4f3-125">انتقل إلى **Retail وCommerce > القنوات > المتاجر‏‎** وانقر فوق **كشوف الحساب**.</span><span class="sxs-lookup"><span data-stu-id="2c4f3-125">Go to **Retail and Commerce > Channels > Stores** and click **Statements**.</span></span> <span data-ttu-id="2c4f3-126">انقر فوق **جديد**، ثم اختر نوع الكشف الذي ترغب في إنشائه.</span><span class="sxs-lookup"><span data-stu-id="2c4f3-126">Click **New** and then choose the type of statement that you want to create.</span></span> <span data-ttu-id="2c4f3-127">ستعرض الحقول في صفحة **كشوف الحساب** والإجراءات تحت **مجموعة كشوف الحسابات** في الصفحة البيانات والإجراءات ذات الصلة استنادًا إلى نوع الكشف المحدد.</span><span class="sxs-lookup"><span data-stu-id="2c4f3-127">Fields on the **Statements** page and actions under the **Statement group** of the page will show relevant data and actions based on the selected statement type.</span></span>
