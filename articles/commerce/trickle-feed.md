---
title: إنشاء أوامر تستند إلى التغذية المستمرة لحركات متجر البيع بالتجزئة
description: يصف هذا الموضوع إنشاء أوامر تستند إلى التغذية المستمرة لحركات المتجر في Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7d5812893edff24a60a0e2eb3607701ac47a8a78
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057130"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions-public-preview"></a><span data-ttu-id="fcb49-103">إنشاء أوامر تستند إلى التغذية المستمرة لحركات متاجر البيع بالتجزئة (معاينة عامة)</span><span class="sxs-lookup"><span data-stu-id="fcb49-103">Trickle feed-based order creation for retail store transactions (Public preview)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fcb49-104">في الإصدار 10.0.4 من Dynamics 365 Retail والإصدارات السابقة، يعتبر ترحيل كشوف الحسابات إحدى عمليات نهاية اليوم ويتم ترحيل جميع الحركات في الدفاتر في نهاية اليوم.</span><span class="sxs-lookup"><span data-stu-id="fcb49-104">In Dynamics 365 Retail versions 10.0.4 and earlier, statement posting is an end-of-day operation and all transactions are posted in the books at the end of the day.</span></span> <span data-ttu-id="fcb49-105">عندئذٍ، يجب معالجة الحركات الكبيرة في غضون فاصل زمني محدد، مما يؤدي في بعض الأحيان إلى نشوء حالات فشل في ترحيل حمل العمل والتأمين وكشوف الحسابات.</span><span class="sxs-lookup"><span data-stu-id="fcb49-105">Large transactions must then be processed in a limited time window, sometimes resulting in load and locks and statement posting failures.</span></span> <span data-ttu-id="fcb49-106">ويتعذر أيضًا على بائعي التجزئة التعرف على الإيرادات والمدفوعات في دفاترهم خلال اليوم.</span><span class="sxs-lookup"><span data-stu-id="fcb49-106">Retailers also can't recognize revenue and payments in their books throughout the day.</span></span>

<span data-ttu-id="fcb49-107">مع المعاينة العامة لوظيفة إنشاء أوامر تستند إلى التغذية المستمرة التي تم تقديمها في الإصدار 10.0.5 من Retail، تتم معالجة الحركات خلال اليوم، في حين تتم معالجة التسوية المالية لطرق الدفع والحركات الأخرى لإدارة النقدية في نهاية اليوم.</span><span class="sxs-lookup"><span data-stu-id="fcb49-107">With the public preview of trickle feed-based order creation introduced in Retail version 10.0.5, transactions are processed throughout the day, and only the financial reconciliation of tenders and other cash management transactions are processed at the end of the day.</span></span> <span data-ttu-id="fcb49-108">تقوم هذه الوظيفة بتقسيم حمل عمل إنشاء أوامر المبيعات والفواتير والمدفوعات خلال اليوم، مما يوفر أداء أفضل والقدرة على التعرف على الإيرادات والمدفوعات في الدفاتر في وقت قريب من الحقيقي‬.</span><span class="sxs-lookup"><span data-stu-id="fcb49-108">This functionality splits the load of creating sales orders, invoices, and payments throughout the day, providing better perceived performance and the ability to recognize revenue and payments in the books in near real-time.</span></span> 


## <a name="how-to-use-trickle-feed-based-posting"></a><span data-ttu-id="fcb49-109">كيفية استخدام الترحيل الذي يستند إلى التغذية المستمرة</span><span class="sxs-lookup"><span data-stu-id="fcb49-109">How to use trickle feed-based posting</span></span>
  
1. <span data-ttu-id="fcb49-110">لتمكين الترحيل الذي يستند إلى التغذية المستمرة‬ للحركات، انتقل إلى **إدارة النظام > الإعداد > تكوين الترخيص** وعطّل المفتاح **كشوف الحساب**.</span><span class="sxs-lookup"><span data-stu-id="fcb49-110">To enable trickle feed-based posting of transactions, go to **System administration > Set up > License configuration** and disable the the **Statements** key.</span></span>

2. <span data-ttu-id="fcb49-111">على الصفحة نفسها، قم بتمكين مفتاح ترخيص **كشوف الحساب (تغذية مستمرة) – معاينة**.</span><span class="sxs-lookup"><span data-stu-id="fcb49-111">On the same page, enable the **Statements (trickle feed) – Preview** license key.</span></span> <span data-ttu-id="fcb49-112">عند تمكين هذا المفتاح، تأكد من عدم وجود كشوف حسابات معلّقة تنتظر ترحيلها.</span><span class="sxs-lookup"><span data-stu-id="fcb49-112">When you enable this key, make sure there are no pending statements waiting to be posted.</span></span> 

    > [!Important]
    > <span data-ttu-id="fcb49-113">قبل تمكين **كشوف الحساب (تغذية مستمرة) – معاينة**، تأكد من عدم وجود كشوف حسابات معلّقة تنتظر ترحيلها.</span><span class="sxs-lookup"><span data-stu-id="fcb49-113">Before you enable the **Statements (trickle feed) – Preview** license key, make sure that no pending statements are waiting to be posted.</span></span>

3. <span data-ttu-id="fcb49-114">سيتم تقسيم مستند كشف الحساب الحالي إلى نوعين مختلفين: كشف الحركات والقائمة المالية.</span><span class="sxs-lookup"><span data-stu-id="fcb49-114">The current statement document will be split into two different types; transactional statement and financial statement.</span></span>

      - <span data-ttu-id="fcb49-115">سيقوم كشف الحركات بانتقاء جميع الحركات غير المرحّلة والتي تم التحقق من صحتها، وينشئ دفاتر يومية لأوامر المبيعات وفواتير المبيعات والمدفوعات والخصومات، وحركات الإيرادات والمصروفات وفق الوتيرة التي تريد تكوينها.</span><span class="sxs-lookup"><span data-stu-id="fcb49-115">The transactional statement will pick up all unposted and validated transactions and create sales orders, sales invoices, payment and discount journals, and income-expense transactions at the cadence that you configure.</span></span> <span data-ttu-id="fcb49-116">يجب تكوين هذه العملية كي تعمل وفق تكرار عالٍ بحيث يتم إنشاء المستندات عند تحميل الحركات إلى Headquarters عبر وظيفة P.</span><span class="sxs-lookup"><span data-stu-id="fcb49-116">You should configure this process to run at a high frequency so that documents are created when the transactions are uploaded into Headquarters through the P-job.</span></span> <span data-ttu-id="fcb49-117">مع كشف الحركات الذي ينشئ أوامر المبيعات وفواتير المبيعات، لا حاجة حقيقية لتكوين الوظيفة الدُفعية **ترحيل المخزون**.</span><span class="sxs-lookup"><span data-stu-id="fcb49-117">With the transactional statement that already creates sales orders and sales invoices, there is no real need to configure the **Post inventory** batch job.</span></span> <span data-ttu-id="fcb49-118">ومع ذلك، يمكنك مع ذلك استخدامه لتلبية احتياجات عمل معينة قد تكون لديك.</span><span class="sxs-lookup"><span data-stu-id="fcb49-118">However, you can still use it to meet specific business requirements that you may have.</span></span>  
      
     - <span data-ttu-id="fcb49-119">تم تصميم القائمة المالية بحيث يتم إنشاؤها في نهاية اليوم وهي تدعم فقط أسلوب الإقفال **وردية**.</span><span class="sxs-lookup"><span data-stu-id="fcb49-119">The financial statement is designed to be created at the end of the day and only supports the closing method of **Shift**.</span></span> <span data-ttu-id="fcb49-120">سوف يقتصر كشف الحساب هذا على التسوية المالية وسينشئ فقط دفاتر اليومية لمبالغ الفروقات بين المبلغ المحسوب ومبلغ الحركة لمختلف طريق الدفع، بالإضافة إلى دفاتر اليومية لحركات إدارة النقدية الأخرى.</span><span class="sxs-lookup"><span data-stu-id="fcb49-120">This statement will be limited to financial reconciliation and will only create the journals for the difference amounts between counted amount and transaction amount for the different tenders, along with journals for other cash management transactions.</span></span>   

4. <span data-ttu-id="fcb49-121">لحساب كشف الحركات، انقر فوق **Retail and Commerce > تكنولوجيا معلومات Retail and Commerce > ترحيل نقطة البيع > حساب كشوف الحركات على دُفعات**.</span><span class="sxs-lookup"><span data-stu-id="fcb49-121">To calculate the transactional statement, click **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate transactional statements in batch**.</span></span> <span data-ttu-id="fcb49-122">لترحيل كشف الحركات على دُفعات، انقر فوق **Retail and Commerce > تكنولوجيا معلومات Retail and Commerce > ترحيل نقطة البيع > ترحيل كشوف الحركات على دُفعات**.</span><span class="sxs-lookup"><span data-stu-id="fcb49-122">To post the transactional statement statements in batch, click **Retail and Commerce > Retail and Commerce IT > POS Posting > Post transactional statements in batch**.</span></span>

5. <span data-ttu-id="fcb49-123">لحساب القائمة المالية، انقر فوق **Retail and Commerce > تكنولوجيا معلومات Retail and Commerce > ترحيل نقطة البيع > حساب القوائم المالية على دُفعات**.</span><span class="sxs-lookup"><span data-stu-id="fcb49-123">To calculate the financial statement, click **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate financial statements in batch**.</span></span> <span data-ttu-id="fcb49-124">لترحيل القوائم المالية، انقر فوق **Retail and Commerce > تكنولوجيا معلومات Retail and Commerce > ترحيل نقطة البيع > ترحيل القوائم المالية على دُفعات**.</span><span class="sxs-lookup"><span data-stu-id="fcb49-124">To post the financial statements in batch, click **Retail and Commerce > Retail and Commerce IT > POS Posting > Post financial statements in batch**.</span></span>

> [!NOTE]
> <span data-ttu-id="fcb49-125">تمت إزالة عناصر القائمة **Retail and Commerce > تكنولوجيا معلومات Retail and Commerce > ترحيل نقطة البيع > حساب الكشوف على دُفعات‬** و**Retail and Commerce > تكنولوجيا معلومات Retail and Commerce > ترحيل نقطة البيع > ترحيل الكشوف على دُفعات‬** مع هذه الميزة.</span><span class="sxs-lookup"><span data-stu-id="fcb49-125">The menu items **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate statements in batch** and **Retail and Commerce > Retail and Commerce IT > POS Posting > Post statements in batch** are removed with this new feature.</span></span>

<span data-ttu-id="fcb49-126">كطريقة بديلة، يمكن إنشاء أنواع كشوف الحسابات والقوائم المالية يدويًا.</span><span class="sxs-lookup"><span data-stu-id="fcb49-126">Alternately, transactional and financial statement types can be created manually.</span></span> <span data-ttu-id="fcb49-127">انتقل إلى **Retail and Commerce > القنوات > المتاجر‏‎** وانقر فوق **كشوف الحساب**.</span><span class="sxs-lookup"><span data-stu-id="fcb49-127">Go to **Retail and Commerce > Channels > Stores** and click **Statements**.</span></span> <span data-ttu-id="fcb49-128">انقر فوق **جديد**، ثم اختر نوع الكشف الذي ترغب في إنشائه.</span><span class="sxs-lookup"><span data-stu-id="fcb49-128">Click **New** and then choose the type of statement that you want to create.</span></span> <span data-ttu-id="fcb49-129">ستعرض الحقول في صفحة **كشوف الحساب** والإجراءات تحت **مجموعة كشوف الحسابات** في الصفحة البيانات والإجراءات ذات الصلة استنادًا إلى نوع الكشف المحدد.</span><span class="sxs-lookup"><span data-stu-id="fcb49-129">Fields on the **Statements** page and actions under the **Statement group** of the page will show relevant data and actions based on the selected statement type.</span></span>