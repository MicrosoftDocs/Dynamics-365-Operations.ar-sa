---
title: مدقق تناسق حركة البيع بالتجزئة
description: يصف هذا الموضوع وظيفة مدقق تناسق حركة البيع بالتجزئة في Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 01/08/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: db01a12b92574b41f1f4fe7281c23992e0d36027
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "301867"
---
# <a name="retail-transaction-consistency-checker"></a><span data-ttu-id="ee0f6-103">مدقق تناسق حركة البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="ee0f6-103">Retail transaction consistency checker</span></span>


[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

<span data-ttu-id="ee0f6-104">يصف هذا الموضوع وظيفة مدقق تناسق حركة البيع بالتجزئة في Microsoft Dynamics 365 for Finance and Operations ، الإصدار 8.1.3.</span><span class="sxs-lookup"><span data-stu-id="ee0f6-104">This topic describes the retail transaction consistency checker functionality introduced in Microsoft Dynamics 365 for Finance and Operations version 8.1.3.</span></span> <span data-ttu-id="ee0f6-105">يحدد مدقق التناسق الحركات غير المتناسقة ويعزلها قبل انتقائها من قبل عملية ترحيل كشف الحساب.</span><span class="sxs-lookup"><span data-stu-id="ee0f6-105">The consistency checker identifies and isolates inconsistent transactions before they are picked up by the statement posting process.</span></span>

<span data-ttu-id="ee0f6-106">عند ترحيل كشف حساب في Retail، قد يفشل الترحيل بسبب وجود بيانات غير متناسقة في جداول حركات البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="ee0f6-106">When a statement is posted in Retail, posting can fail due to inconsistent data in the retail transaction tables.</span></span> <span data-ttu-id="ee0f6-107">قد يعود سبب المشكلة في البيانات إلى ظهور مشاكل غير متوقعة في تطبيق نقطة البيع (POS)، أو إذا تم استيراد الحركات بشكل غير صحيح من أنظمة نقطة البيع الخارجية.</span><span class="sxs-lookup"><span data-stu-id="ee0f6-107">The data issue may be caused by by unforeseen issues in the point of sale (POS) application, or if transactions were incorrectly imported from third-party POS systems.</span></span> <span data-ttu-id="ee0f6-108">تشتمل الأمثلة حول كيفية ظهور حالات عدم التناسق هذه على ما يلي:</span><span class="sxs-lookup"><span data-stu-id="ee0f6-108">Examples of how these inconsistencies may appear include:</span></span> 

  - <span data-ttu-id="ee0f6-109">إجمالي الحركة في جدول الرأس غير متطابق مع إجمالي الحركة في البنود.</span><span class="sxs-lookup"><span data-stu-id="ee0f6-109">The transaction total on the header table does not match the transaction total on the lines.</span></span>
  - <span data-ttu-id="ee0f6-110">عدد البنود في جدول الرأس غير متطابق مع عدد البنود في جدول الحركة.</span><span class="sxs-lookup"><span data-stu-id="ee0f6-110">The line count on the header table does not match with the number of lines in the transaction table.</span></span>
  - <span data-ttu-id="ee0f6-111">الضرائب في جدول الرأس غير متطابقة مع قيمة الضريبة في البنود.</span><span class="sxs-lookup"><span data-stu-id="ee0f6-111">Taxes on the header table do not match the tax amount on the lines.</span></span> 
  
<span data-ttu-id="ee0f6-112">عندما تنتقي عمليات ترحيل كشوف الحسابات حركات غير متناسقة، يتم إنشاء دفاتر يومية دفعات وفواتير مبيعات غير متناسقة، وتفشل عملية ترحيل كشف الحساب بكاملها نتيجة لذلك.</span><span class="sxs-lookup"><span data-stu-id="ee0f6-112">When inconsistent transactions are picked up by the statement posting process, inconsistent sales invoices and payment journals are created, and the entire statement posting process fails as a result.</span></span> <span data-ttu-id="ee0f6-113">تشتمل عملية استرداد كشوف الحسابات من حالة من هذا النوع على عمليات إصلاح معقدة للبيانات عبر جداول حركات متعددة.</span><span class="sxs-lookup"><span data-stu-id="ee0f6-113">Recovering the statements from such a state involves complex data fixes across multiple transaction tables.</span></span> <span data-ttu-id="ee0f6-114">يمنع مدقق تناسق حركة البيع بالتجزئة حدوث مثل هذه المشاكل.</span><span class="sxs-lookup"><span data-stu-id="ee0f6-114">The retail transaction consistency checker prevents such issues.</span></span>

<span data-ttu-id="ee0f6-115">يوضح المخطط التالي عملية الترحيل باستخدام مدقق تناسق الحركة.</span><span class="sxs-lookup"><span data-stu-id="ee0f6-115">The following chart illustrates the posting process with the transaction consistency checker.</span></span>

<span data-ttu-id="ee0f6-116">![عملية ترحيل كشف الحساب باستخدام مدقق تناسق حركة البيع بالتجزئة](./media/validchecker.png "عملية ترحيل كشف الحساب باستخدام مدقق تناسق حركة البيع بالتجزئة")</span><span class="sxs-lookup"><span data-stu-id="ee0f6-116">![Statement posting process with retail transaction consistency checker](./media/validchecker.png "Statement posting process with retail transsaction consistency checker")</span></span>

<span data-ttu-id="ee0f6-117">تدقق العملية الدُفعية **التحقق من صحة حركات المتجر‬** في تناسق جداول حركات البيع بالتجزئة للسيناريوهات التالية.</span><span class="sxs-lookup"><span data-stu-id="ee0f6-117">The **Validate store transactions** batch process checks the consistency of the retail transaction tables for the following scenarios.</span></span>

- <span data-ttu-id="ee0f6-118">حساب العميل - التأكد من أن حساب العميل في جداول حركات البيع بالتجزئة موجود في المقر الرئيسي للعميل.</span><span class="sxs-lookup"><span data-stu-id="ee0f6-118">Customer account - Validates that the customer account in the retail transaction tables exists in the HQ customer master.</span></span>
- <span data-ttu-id="ee0f6-119">عدد البنود - التأكد من أن عدد البنود، كما تم تسجيله في جدول رأس الحركة، يتطابق مع أرقام البنود في جداول حركة مبيعات.</span><span class="sxs-lookup"><span data-stu-id="ee0f6-119">Line count - Validates that the number of lines, as captured on the transaction header table, matches the number of lines in the sales transaction tables.</span></span>

## <a name="set-up-the-consistency-checker"></a><span data-ttu-id="ee0f6-120">إعداد مدقق التناسق</span><span class="sxs-lookup"><span data-stu-id="ee0f6-120">Set up the consistency checker</span></span>
<span data-ttu-id="ee0f6-121">قم بتكوين العملية الدُفعية "التحقق من صحة حركات المتجر‬" في **البيع بالتجزئة \> تكنولوجيا معلومات البيع بالتجزئة‬ \> ترحيل نقطة البيع**، لعمليات التشغيل الدورية.</span><span class="sxs-lookup"><span data-stu-id="ee0f6-121">Configure the "Validate store transactions" batch process, at **Retail \> Retail IT \> POS posting**, for periodic runs.</span></span> <span data-ttu-id="ee0f6-122">يمكن جدولة الوظيفة الدُفعية استنادًا إلى التدرج الهرمي للمؤسسات في المتجر، بطريقة مماثلة لكيفية إعداد العمليتين "حساب الكشوف على دُفعات‬" و"ترحيل الكشوف على دُفعات‬".</span><span class="sxs-lookup"><span data-stu-id="ee0f6-122">The batch job can be scheduled based on store organization hierarchy, similar to how the "Calculate statement in batch" and "Post statement in batch" processes are set up.</span></span> <span data-ttu-id="ee0f6-123">من المستحسن تكوين هذه العملية الدُفعية لتشغيلها عدة مرات في اليوم وجدولتها بحيث يتم تشغيلها في نهاية كل تنفيذ لوظيفة P.</span><span class="sxs-lookup"><span data-stu-id="ee0f6-123">We recommend that you configure this batch process to run multiple times in a day and schedule it so that it runs at the end of every P-job execution.</span></span>

## <a name="results-of-validation-process"></a><span data-ttu-id="ee0f6-124">نتائج التحقق من الصحة</span><span class="sxs-lookup"><span data-stu-id="ee0f6-124">Results of validation process</span></span>
<span data-ttu-id="ee0f6-125">توضع علامة نتائج التحقق من الصحة التي تقوم بها العملية الدُفعية على حركة البيع بالتجزئة المناسبة.</span><span class="sxs-lookup"><span data-stu-id="ee0f6-125">The results of the validation check by the batch process are tagged on the appropriate retail transaction.</span></span> <span data-ttu-id="ee0f6-126">يكون الحقل **حالة التحقق من الصحة** على سجل حركة البيع بالتجزئة معينًا إلى **ناجح‬** أو **خطأ**، ويظهر تاريخ تشغيل عملية التحقق من الصحة الأخيرة في الحقل **وقت آخر عملية تحقق من الصحة**.</span><span class="sxs-lookup"><span data-stu-id="ee0f6-126">The **Validation status** field on the retail transaction record is either set to **Successful** or **Error**, and the date of the last validation run appears on the **Last validation time** field.</span></span>

<span data-ttu-id="ee0f6-127">لعرض نص وصفي للخطأ المتعلق بفشل التحقق من الصحة، حدد سجل حركة متجر البيع بالتجزئة الملائم، ثم انقر فوق الزر **أخطاء التحقق من الصحة**.</span><span class="sxs-lookup"><span data-stu-id="ee0f6-127">To view more descriptive error text relating to a validation failure, select the relevant retail store transaction record and click the **Validation errors** button.</span></span>

<span data-ttu-id="ee0f6-128">لن تتضمن كشوف الحسابات الحركات التي لم تنجح في عملية التحقق من الصحة والحركات التي لم يتم بعد التحقق من صحتها.</span><span class="sxs-lookup"><span data-stu-id="ee0f6-128">Transactions that fail the validation check and transactions that have not yet been validated will not be pulled into statements.</span></span> <span data-ttu-id="ee0f6-129">أثناء عملية "حساب كشف الحساب"، سيتم يتم إبلاغ المستخدمين عن وجود حركات كان يجب تضمينها في كشف الحساب ولكن لم يتم تضمينها فيه.</span><span class="sxs-lookup"><span data-stu-id="ee0f6-129">During the "Calculate statement" process, users will be notified if there are transactions that could have been included in the statement but weren't.</span></span>

<span data-ttu-id="ee0f6-130">إذا تم العثور على خطأ يتعلق بالتحقق من الصحة، فإن الطريقة الوحيدة لإصلاحه هو الاتصال بدعم Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ee0f6-130">If a validation error is found, the only way to fix the error is to contact Microsoft Support.</span></span> <span data-ttu-id="ee0f6-131">في إصدار مستقبلي، سنضيف ميزة تسمح للمستخدمين بإصلاح السجلات التي فشلت عبر واجهة المستخدم.</span><span class="sxs-lookup"><span data-stu-id="ee0f6-131">In a future release, capability will be added so that users can fix the records that failed through the user interface.</span></span> <span data-ttu-id="ee0f6-132">وسنوفر أيضًا قدرات التسجيل والتدقيق لتتبع محفوظات التعديلات.</span><span class="sxs-lookup"><span data-stu-id="ee0f6-132">Logging and auditing capabilities will also be made available to trace the history of the modifications.</span></span>

> [!NOTE]
> <span data-ttu-id="ee0f6-133">سنضيف المزيد من قواعد التحقق من الصحة لدعم سيناريوهات إضافية في إصدار مستقبلي.</span><span class="sxs-lookup"><span data-stu-id="ee0f6-133">Additional validation rules to support more scenarios will be added in a future release.</span></span>