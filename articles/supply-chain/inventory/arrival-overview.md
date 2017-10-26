---
title: "نظرة عامة على الوصول"
description: "يوفر هذا الموضوع معلومات حول ميزة النظرة العامة على الوصول. تعتبر الصفحة \"نظرة عامة على الوصول\" جزءًا من هذه الميزة وتوفر نظرة عامة على كافة العناصر التي من المتوقع أن تصل كأصناف واردة."
author: perlynne
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSArrivalOverview, WMSArrivalOverviewProfile, WMSJournalTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: d9ebc0ea12de0c97718b565b77d99c3a1fcd6f21
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="arrival-overview"></a><span data-ttu-id="85a37-104">نظرة عامة على الوصول</span><span class="sxs-lookup"><span data-stu-id="85a37-104">Arrival overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="85a37-105">يوفر هذا الموضوع معلومات حول ميزة النظرة العامة على الوصول.</span><span class="sxs-lookup"><span data-stu-id="85a37-105">This topic provides information about the Arrival overview feature.</span></span> <span data-ttu-id="85a37-106">تعتبر الصفحة "نظرة عامة على الوصول" جزءًا من هذه الميزة وتوفر نظرة عامة على كافة العناصر التي من المتوقع أن تصل كأصناف واردة.</span><span class="sxs-lookup"><span data-stu-id="85a37-106">The Arrival overview page is part of this feature and provides an overview of all items that are expected to arrive as incoming items.</span></span>

<span data-ttu-id="85a37-107">توفر الصفحة **نظرة عامة على الوصول** نظرة عامة على جميع الأصناف الواردة المتوقعة.</span><span class="sxs-lookup"><span data-stu-id="85a37-107">The **Arrival overview** page provides an overview of all expected incoming items.</span></span> <span data-ttu-id="85a37-108">وتُظهر أيضًا عمليات الوصول التي يمكن تهيئتها استنادًا إلى النظرة العامة.</span><span class="sxs-lookup"><span data-stu-id="85a37-108">It also shows arrivals that can be initialized based on the overview.</span></span> <span data-ttu-id="85a37-109">يركز هذا الموضوع على عملية الاستلام.</span><span class="sxs-lookup"><span data-stu-id="85a37-109">This topic focuses on the receiving process.</span></span>

## <a name="business-scenario"></a><span data-ttu-id="85a37-110">سيناريو العمل</span><span class="sxs-lookup"><span data-stu-id="85a37-110">Business scenario</span></span>
<span data-ttu-id="85a37-111">خذ في الاعتبار السيناريو التالي في العمليات الواردة.</span><span class="sxs-lookup"><span data-stu-id="85a37-111">Consider the following scenario in the inbound processes.</span></span>

<span data-ttu-id="85a37-112">[![سيناريو العمل](./media/arrival-overview-scenario.png)](./media/arrival-overview-scenario.png)</span><span class="sxs-lookup"><span data-stu-id="85a37-112">[![Business scenario](./media/arrival-overview-scenario.png)](./media/arrival-overview-scenario.png)</span></span>

<span data-ttu-id="85a37-113">سامي، موظف الاستقبال، يريد معرفة الأصناف التي من المتوقع استلامها في اليوم الحالي.</span><span class="sxs-lookup"><span data-stu-id="85a37-113">Sammy, a receiving clerk, wants to know what is expected to be received on the current day.</span></span> <span data-ttu-id="85a37-114">في الصفحة **نظرة عامة على الوصول**، يستطيع سامي الحصول على نظرة عامة على المهام الحالية، وتقديرًا أوليًا للكميات، والحجم والوزن، ومختلف أنواع الأوامر وغير ذلك.</span><span class="sxs-lookup"><span data-stu-id="85a37-114">On the **Arrival overview** page, Sammy can get an overview of the current tasks, and a rough estimate of quantities, volume, weight, different order types, and so on.</span></span> <span data-ttu-id="85a37-115">في وقت لاحق، تصل عملية تسليم تصل إلى أحد الأرصفة الداخلية، ويتلقى سامي قائمة بالتسليم.</span><span class="sxs-lookup"><span data-stu-id="85a37-115">Later, a delivery arrives at one of the inbound docks, and Sammy receives a list of the delivery.</span></span> <span data-ttu-id="85a37-116">في الصفحة **نظرة عامة على الوصول**، يستطيع سامي تنفيذ المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="85a37-116">On the **Arrival overview** page, Sammy can perform the following tasks:</span></span>

-   <span data-ttu-id="85a37-117">تحديد أمر الاستلام المطابق، وتسجيل عملية الاستلام على أنها **قيد التقدم**.</span><span class="sxs-lookup"><span data-stu-id="85a37-117">Identify the matching receipt order, and register the receipt as **In progress**.</span></span> <span data-ttu-id="85a37-118">يتم تلقائيًا إنشاء البنود المطلوبة للتسجيل، ويمكن مراقبة الإيصال، على الرغم من عدم ترحيل الحركات بعد على أنها **مسجلة**.</span><span class="sxs-lookup"><span data-stu-id="85a37-118">The lines that are required for a registration are automatically generated, and the receipt can be monitored, even though the transactions haven't yet been posted as **Registered**.</span></span>
-   <span data-ttu-id="85a37-119">الوصول إلى مرجع دفتر يومية الوصول المناسب (أي، دفتر يومية **وصول الصنف** أو دفتر يومية **مدخلات الإنتاج**)، وتحديد دفاتر اليومية الجاهزة لتحديث استلام المنتج.</span><span class="sxs-lookup"><span data-stu-id="85a37-119">Access the appropriate arrival journal reference (that is, the **Item arrival** journal or the **Production input** journal), and identify journals that are ready for a product receipt update.</span></span>

## <a name="arrival-overview-page"></a><span data-ttu-id="85a37-120">صفحة النظرة العامة على الوصول</span><span class="sxs-lookup"><span data-stu-id="85a37-120">Arrival overview page</span></span>
<span data-ttu-id="85a37-121">لفتح الصفحة **نظرة عامة على الوصول**، انقر فوق **إدارة المخزون** &gt; **الأوامر الواردة** &gt; **نظرة عامة على الوصول**.</span><span class="sxs-lookup"><span data-stu-id="85a37-121">To open the **Arrival overview** page, click **Inventory management** &gt; **Inbound orders** &gt; **Arrival overview**.</span></span> <span data-ttu-id="85a37-122">يمكنك عرض قائمة بالأوامر التي من المتوقع أن يتم استلامها.</span><span class="sxs-lookup"><span data-stu-id="85a37-122">You can view a list of orders that are expected to be received.</span></span> <span data-ttu-id="85a37-123">تم تقسيم النظرة العامة إلى رأس وبنود.</span><span class="sxs-lookup"><span data-stu-id="85a37-123">The overview is divided into a header and lines.</span></span> <span data-ttu-id="85a37-124">وتم تجميع معلومات الرأس حسب نوع الأمر وتاريخ الاستلام المتوقع ووجهة التسليم.</span><span class="sxs-lookup"><span data-stu-id="85a37-124">The header information is grouped by the order type, expected receipt date, and delivery destination.</span></span> <span data-ttu-id="85a37-125">عندما يتم تحديد بند رأس للوصول، يتم تحديد كافة بنود التفاصيل المتعلقة بمرجع الإيصال للوصول في جزء تفاصيل البند من الصفحة.</span><span class="sxs-lookup"><span data-stu-id="85a37-125">When a header line is selected for arrival, all the detail lines that are related to the receipt reference are selected for arrival in the line details part of the page.</span></span> <span data-ttu-id="85a37-126">عند ترحيل كافة بنود دفتر اليومية المرتبطة، لا تظهر هذه المعلومات.</span><span class="sxs-lookup"><span data-stu-id="85a37-126">When all related journal lines have been posted, this information isn't shown.</span></span>

### <a name="arrival-overview-profiles"></a><span data-ttu-id="85a37-127">ملفات تعريف النظرة العامة على الوصول</span><span class="sxs-lookup"><span data-stu-id="85a37-127">Arrival overview profiles</span></span>

<span data-ttu-id="85a37-128">توفر الصفحة **نظرة عامة على الوصول** نظرة عامة على الأصناف المتوقع وصولها وتاريخ وصولها المتوقع.</span><span class="sxs-lookup"><span data-stu-id="85a37-128">The **Arrival overview** page provides an overview of items that are expected to arrive and the date when they are expected to arrive.</span></span> <span data-ttu-id="85a37-129">كجزء من عملية الوصول، يمكن استخدام عدة مجموعات من الإعدادات الشخصية.</span><span class="sxs-lookup"><span data-stu-id="85a37-129">As part of the arrival process, multiple sets of personal settings can be used.</span></span> <span data-ttu-id="85a37-130">يمكن للمستخدمين الفرديين تعريف إعداداتهم الشخصية في صفحة **ملفات تعريف النظرة العامة على الوصول**.</span><span class="sxs-lookup"><span data-stu-id="85a37-130">Individual users can define their personal settings on the **Arrival overview profiles** page.</span></span>

### <a name="set-up-item-arrival"></a><span data-ttu-id="85a37-131">إعداد وصول الصنف</span><span class="sxs-lookup"><span data-stu-id="85a37-131">Set up item arrival</span></span>

<span data-ttu-id="85a37-132">يرغب سامي، في هذا المثال، في إعداد كمبيوتر جديد في موقع سيتم استخدامه لاستلام البضائع المنتهية التي تأتي من الإنتاج في الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="85a37-132">In our example, Sammy wants to set up a new computer at a location that will be used to receive finished goods that come from production at Site 1.</span></span> <span data-ttu-id="85a37-133">في الصفحة **ملفات تعريف النظرة العامة على الوصول**، يقوم سامي بإنشاء إعداد جديد يسمى **إنتاج الموقع 1** ويحدد الإعدادات التالية.</span><span class="sxs-lookup"><span data-stu-id="85a37-133">On the **Arrival overview profiles** page, Sammy creates a new setup that is named **Site 1 production** and specifies the following settings.</span></span>

1.  <span data-ttu-id="85a37-134">على علامة التبويب السريعة **خيارات الوصول**، في مجموعة الحقول **النطاق**، أدخل معلومات حول فترة الأيام والمستودعات لتضمينها في النظرة العامة.</span><span class="sxs-lookup"><span data-stu-id="85a37-134">On the **Arrival options** FastTab, in the **Range** field group, enter information about a day interval and the warehouses to include in the overview.</span></span>
2.  <span data-ttu-id="85a37-135">على علامة التبويب السريعة **خيارات الوصول**، في مجموعة حقول **دفتر اليومية**، أدخل المستودع المستلم والموقع واسم دفتر اليومية (وصول الصنف/مدخلات الإنتاج).</span><span class="sxs-lookup"><span data-stu-id="85a37-135">On the **Arrival options** FastTab, in the **Journal** field group, enter a receiving warehouse, a location, and a journal name (item arrival/production input).</span></span>
3.  <span data-ttu-id="85a37-136">على علامة التبويب السريعة **تفاصيل استعلام الوصول**، في مجموعة الحقول **الموقع**، في الحقل **قيد الموقع** ، أدخل موقعًا لتقييد العرض في منطقة النظرة العامة.</span><span class="sxs-lookup"><span data-stu-id="85a37-136">On the **Arrival query details** FastTab, in the **Site** field group, in the **Restrict to site** field, enter a site to limit the view in the overview area.</span></span>
4.  <span data-ttu-id="85a37-137">على علامة التبويب السريعة **تفاصيل استعلام الوصول**، في مجموعة الحقول **أنواع الحركات المعروضة**، قم بتعيين الخيار **أوامر الإنتاج** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="85a37-137">On the **Arrival query details** FastTab, in the **Transaction types shown** field group, set the **Production orders** option to **Yes**.</span></span>
5.  <span data-ttu-id="85a37-138">على علامة التبويب السريعة **تفاصيل استعلام الوصول**، في مجموعة الحقول **متنوعة**، قم بتعيين الخيار **تحديث عند بدء التشغيل** إلى **نعم** إذا كان يجب تحديث العرض تلقائيًا عند بدء التشغيل.</span><span class="sxs-lookup"><span data-stu-id="85a37-138">On the **Arrival query details** FastTab, in the **Miscellaneous** group, set the **Update on startup** option to **Yes** if the view should be automatically updated at startup.</span></span> <span data-ttu-id="85a37-139">قم بتعيين الخيار **التحديث عند تغيير النطاق** إلى **نعم** إذا كان يجب أن يتم تلقائيًا تحديث العرض عند حدوث تغيير في قيم النطاق‏‎.</span><span class="sxs-lookup"><span data-stu-id="85a37-139">Set the **Update on range change** option to **Yes** if the view should be automatically updated when range values are changed.</span></span>

<span data-ttu-id="85a37-140">بالنسبة إلى هذا المثال، تم تعيين الحقل **اسم ملف تعريف النظرة العامة على الوصول** على علامة التبويب السريعة **خيارات الوصول** في الصفحة **نظرة عامة على الوصول** إلى **إنتاج الموقع 1**.</span><span class="sxs-lookup"><span data-stu-id="85a37-140">For this example, the **Arrival overview profile name** field on the **Arrival options** FastTab of the **Arrival overview** page is set to **Site 1 production**.</span></span>

### <a name="prerequisites-for-arrival-journals"></a><span data-ttu-id="85a37-141">المتطلبات الأساسية لدفاتر يومية الوصول</span><span class="sxs-lookup"><span data-stu-id="85a37-141">Prerequisites for arrival journals</span></span>

<span data-ttu-id="85a37-142">لإنشاء دفاتر يومية الوصول بشكل تلقائي من الصفحة **نظرة عامة على الوصول**، يجب عليك تحديد المعلومات المناسبة في مجموعة الحقول **دفتر اليومية** على علامة التبويب السريعة **خيارات الوصول**.</span><span class="sxs-lookup"><span data-stu-id="85a37-142">To automatically create arrival journals from the **Arrival overview** page, you must define appropriate information in the **Journal** field group on the **Arrival options** FastTab.</span></span>

-   <span data-ttu-id="85a37-143">يجب تحديد اسم دفتر يومية لإنشاء دفتر يومية.</span><span class="sxs-lookup"><span data-stu-id="85a37-143">You must specify a journal name to create a journal.</span></span>

<span data-ttu-id="85a37-144">[![تحديد اسم دفتر اليومية](./media/arrival-overview-journal.png)](./media/arrival-overview-journal.png)</span><span class="sxs-lookup"><span data-stu-id="85a37-144">[![Specifying a journal name](./media/arrival-overview-journal.png)](./media/arrival-overview-journal.png)</span></span>

-   <span data-ttu-id="85a37-145">إذا حددت القيم الموجودة في حقلي **المستودع** و**الموقع**، فسيتم تطبيق هذه القيم على بنود دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="85a37-145">If you specify values in the **Warehouse** and **Location** fields, those values are applied on the journal lines.</span></span> <span data-ttu-id="85a37-146">إذا لم تحدد القيم، فإن النظام يستخدم القيم من البُعد الذي تم تحديده في حركات المخزون.</span><span class="sxs-lookup"><span data-stu-id="85a37-146">If you don't specify values, the system uses the values from the dimension that is specified on the inventory transactions.</span></span>

#### <a name="items-that-are-received-from-one-expected-receipt-order"></a><span data-ttu-id="85a37-147">الأصناف التي تم استلامها من أمر استلام متوقع</span><span class="sxs-lookup"><span data-stu-id="85a37-147">Items that are received from one expected receipt order</span></span>

<span data-ttu-id="85a37-148">على علامة التبويب السريعة **عمليات الاستلام**، يحدد سامي بندًا ثم ينقر فوق **بدء الوصول**.</span><span class="sxs-lookup"><span data-stu-id="85a37-148">On the **Receipts** FastTab, Sammy selects a line and then clicks **Start arrival**.</span></span> <span data-ttu-id="85a37-149">يتم بشكل تلقائي تحديد كافة البنود ذات الصلة الموجودة في النطاق المحدد والتي لديها كمية يجب تسجيلها.</span><span class="sxs-lookup"><span data-stu-id="85a37-149">All related lines that are in the specified range and that have a quantity to register are automatically selected.</span></span> <span data-ttu-id="85a37-150">يتم إنشاء دفتر يومية وصول الصنف الذي يوجد فيه تطابق بين أمر الاستلام المتوقع ودفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="85a37-150">An item arrival journal is generated that has a match between the expected receipt order and the journal.</span></span> <span data-ttu-id="85a37-151">تتم تهيئة الكمية تلقائيًا على كافة البنود التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="85a37-151">The quantity is automatically initialized on all lines that are created.</span></span>

#### <a name="items-that-are-received-from-more-than-one-expected-receipt-order"></a><span data-ttu-id="85a37-152">الأصناف التي تم استلامها من أكثر من أمر استلام متوقع</span><span class="sxs-lookup"><span data-stu-id="85a37-152">Items that are received from more than one expected receipt order</span></span>

<span data-ttu-id="85a37-153">على علامة التبويب السريعة **عمليات الاستلام**، يحدد سامي عدة بنود ثم ينقر فوق **بدء الوصول**.</span><span class="sxs-lookup"><span data-stu-id="85a37-153">On the **Receipts** FastTab, Sammy selects multiple lines and then clicks **Start arrival**.</span></span> <span data-ttu-id="85a37-154">يتم إنشاء دفتر يومية وصول الصنف الذي يوجد فيه تطابق بين جميع أوامر الاستلام المتوقعة ودفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="85a37-154">An item arrival journal is generated that has a match between all the expected receipt orders and the journal.</span></span> <span data-ttu-id="85a37-155">يتم إنشاء كافة البنود في رأس دفتر يومية وصول صنف واحد، وتتم تهيئة الكمية تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="85a37-155">All lines are created on one item arrival journal header, and the quantity is automatically initialized.</span></span>

### <a name="receive-items-from-one-or-more-expected-receipt-orders"></a><span data-ttu-id="85a37-156">استلام أصناف من أمر استلام متوقع واحد أو أكثر</span><span class="sxs-lookup"><span data-stu-id="85a37-156">Receive items from one or more expected receipt orders</span></span>

#### <a name="view-information"></a><span data-ttu-id="85a37-157">عرض المعلومات</span><span class="sxs-lookup"><span data-stu-id="85a37-157">View information</span></span>

<span data-ttu-id="85a37-158">للحصول على نظرة عامة حول عمليات الاستلام المتوقعة في فترة تاريخ، يدخل سامي المعلومات التالية في الحقول الموجودة على علامة التبويب السريعة **خيارات الوصول**  في الصفحة **نظرة عامة على الوصول**، ثم ينقر فوق **تحديث** لتحديث طريقة العرض:</span><span class="sxs-lookup"><span data-stu-id="85a37-158">To get an overview of expected receipts in a date interval, Sammy enters the following information in the fields on the **Arrival options** FastTab on the **Arrival overview** page and then clicks **Update** to update the view:</span></span>

-   <span data-ttu-id="85a37-159">اسم ملف تعريف النظرة العامة على الوصول: **استعلام**</span><span class="sxs-lookup"><span data-stu-id="85a37-159">Arrival overview profile name: **Inquiry**</span></span>
-   <span data-ttu-id="85a37-160">إظهار البنود: **الكل**</span><span class="sxs-lookup"><span data-stu-id="85a37-160">Show lines: **All**</span></span>
-   <span data-ttu-id="85a37-161">الأيام السابقة: (فارغ)</span><span class="sxs-lookup"><span data-stu-id="85a37-161">Days back: (Blank)</span></span>
-   <span data-ttu-id="85a37-162">الأيام التالية: **0**</span><span class="sxs-lookup"><span data-stu-id="85a37-162">Days forward: **0**</span></span>
-   <span data-ttu-id="85a37-163">المستودعات: **GW وMW**</span><span class="sxs-lookup"><span data-stu-id="85a37-163">Warehouses: **GW, MW**</span></span>

<span data-ttu-id="85a37-164">باستطاعة سامي عرض المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="85a37-164">Sammy can view the following information:</span></span>

-   <span data-ttu-id="85a37-165">كافة أوامر الاستلام ذات الصلة لتاريخ النظام وعدد غير محدود من أيام العمل في الماضي منها (**InventTrans.StatusDate** الفاصل الزمني)، وإيصالات الاستلام لمستودعات GW وMW، بغض النظر عن الحالة.</span><span class="sxs-lookup"><span data-stu-id="85a37-165">All related receipt orders for the system date and an infinite number of days back from it (the **InventTrans.StatusDate** interval), and receipts to warehouses GW and MW, regardless of status.</span></span>
-   <span data-ttu-id="85a37-166">معلومات مفصلة حول البنود لأكثر من أمر واحد.</span><span class="sxs-lookup"><span data-stu-id="85a37-166">Detailed line information for more than one order.</span></span> <span data-ttu-id="85a37-167">باستطاعة سامي GW and MW عدة بنود رأس متعددة في النظرة العامة ثم النقر فوق **إظهار كل المحدد** لعرض كافة المعلومات المناظرة حول تفاصيل البنود لكافة الأوامر المحددة.</span><span class="sxs-lookup"><span data-stu-id="85a37-167">Sammy can select multiple header lines in the overview and then click **Show all selected** to view all the corresponding line detail information for all selected orders.</span></span>
-   <span data-ttu-id="85a37-168">معلومات حول أمر شراء معين.</span><span class="sxs-lookup"><span data-stu-id="85a37-168">Information about a specific purchase order.</span></span> <span data-ttu-id="85a37-169">لإظهار فقط المعلومات المرتبطة برقم مرجعي محدد في النظرة العامة، يستطيع سامي إدخال رقم حساب في الحقل **رقم الحساب** ورقم أمر في حقل **الرقم المرجعي**.</span><span class="sxs-lookup"><span data-stu-id="85a37-169">To show only information that is related to a specific reference number in the overview, Sammy can enter an account number in the **Account number** field and an order number in the **Reference number** field.</span></span>
-   <span data-ttu-id="85a37-170">نظرة عامة على تسجيل المهام المستحقة لكافة بنود الأمر التي تم إنشاء دفتر يومية وصول أصناف لها ولكن لم يتم ترحيلها بعد.</span><span class="sxs-lookup"><span data-stu-id="85a37-170">An overview of the registration tasks that are due for all the order lines that an item arrival journal has been created for but hasn't yet been posted.</span></span> <span data-ttu-id="85a37-171">لعرض هذه المعلومات، يستطيع سامي تحديد **قيد التقدم** في الحقل **إظهار البنود‬**.</span><span class="sxs-lookup"><span data-stu-id="85a37-171">To view this information, Sammy can select **In progress** in the **Show lines** field.</span></span>

### <a name="update-journals"></a><span data-ttu-id="85a37-172">تحديث دفاتر اليومية</span><span class="sxs-lookup"><span data-stu-id="85a37-172">Update journals</span></span>

<span data-ttu-id="85a37-173">لتسجيل بند أمر أو أكثر لمعالجته، يستطيع سامي تحديد البنود في شبكة النظرة العامة أو في شبكة البنود، ثم النقر فوق **دفاتر اليومية** &gt; **إظهار عمليات الوصول من عمليات الاستلام**.</span><span class="sxs-lookup"><span data-stu-id="85a37-173">To register one or more order lines that are due to be processed, Sammy can select the lines in the overview grid or in the line grid, and then click **Journals** &gt; **Show arrivals from receipts**.</span></span> <span data-ttu-id="85a37-174">يتم عرض عناوين وصول الأصناف التي تتطابق مع البنود.</span><span class="sxs-lookup"><span data-stu-id="85a37-174">The item arrival headers that match the lines are shown.</span></span> <span data-ttu-id="85a37-175">لتحديث إيصال استلام منتجات أمر لأصناف مسجلة، يستطيع سامي الوصول إلى رؤوس دفتر يومية وصول الصنف الجاهزة للتحديث.</span><span class="sxs-lookup"><span data-stu-id="85a37-175">To purchase order product receipt update the registered items, Sammy can access the item arrival journal headers that are ready for update.</span></span> <span data-ttu-id="85a37-176">للوصول إلى رؤوس دفتر يومية وصول الصنف هذه، ينقر سامي فوق **دفاتر اليومية** &gt; **دفاتر اليومية الجاهزة لإيصال استلام المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="85a37-176">To access these item arrival journal headers, he clicks **Journals** &gt; **Product receipt ready journals**.</span></span> <span data-ttu-id="85a37-177">يتم عرض كافة بنود الرأس الجاهزة لتحديث إيصال استلام المنتجات في نطاق المستودع المحدد.</span><span class="sxs-lookup"><span data-stu-id="85a37-177">All the header lines that are ready for product receipt update in the specified warehouse range are shown.</span></span> <span data-ttu-id="85a37-178">(لا تتعلق بنود الرأس التي تظهر بفترة الأيام).</span><span class="sxs-lookup"><span data-stu-id="85a37-178">(The header lines that are shown aren't related to the day interval).</span></span>

### <a name="start-an-arrival-registration"></a><span data-ttu-id="85a37-179">بدء تشغيل تسجيل الوصول</span><span class="sxs-lookup"><span data-stu-id="85a37-179">Start an arrival registration</span></span>

<span data-ttu-id="85a37-180">عن طريق تحديد بنود متعددة في الصفحة **نظرة عامة على الوصول**، يستطيع سامي بدء الوصول لأكثر من مرجع إيصال واحد.</span><span class="sxs-lookup"><span data-stu-id="85a37-180">By selecting multiple lines on the **Arrival overview** page, Sammy can start an arrival of more than one receipt reference.</span></span> <span data-ttu-id="85a37-181">عندما يقوم بتحديد بند من النظرة العامة على عمليات الاستلام، يتم تحديد تفاصيل البند المقابل.</span><span class="sxs-lookup"><span data-stu-id="85a37-181">When he selects a line from the receipts overview, the corresponding line details are selected.</span></span> <span data-ttu-id="85a37-182">في حالة وجود كمية للتسجيل، سيكون الزر **بدء الوصول** متاحًا.</span><span class="sxs-lookup"><span data-stu-id="85a37-182">If a quantity for registration exists, the **Start arrival** button is available.</span></span> <span data-ttu-id="85a37-183">يستطيع سامي استخدام أسلوبين لبدء تسجيل الوصول:</span><span class="sxs-lookup"><span data-stu-id="85a37-183">Sammy can use two methods to start the arrival registration:</span></span>

-   <span data-ttu-id="85a37-184">لتصفية الصفحة بحيث تعرض فقط السجلات التي تستوفي معايير محددة، في الحقل **مرجع المورد**، امسح رقمًا مرجعيًا من أحد الموردين، مثل الرمز الشريطي الخاص بمذكرة تسليم.</span><span class="sxs-lookup"><span data-stu-id="85a37-184">To filter the page so that it shows only records that meet specific criteria, in the **Vendor reference** field, scan a reference number from a vendor, such as the bar code for a delivery note.</span></span>
-   <span data-ttu-id="85a37-185">في جزء النظرة العامة أو في جزء التفاصيل في الصفحة **نظرة عامة على الوصول**، حدد يدويًا مجموعة من السجلات لتسجيل الوصول.</span><span class="sxs-lookup"><span data-stu-id="85a37-185">In the overview part or the details part of the **Arrival overview** page, manually select or cancel the selection of records for arrival registration.</span></span> <span data-ttu-id="85a37-186">عندئذٍ، عندما ينقر سامي فوق **بدء الوصول**، يتم بشكل تلقائي إنشاء السجلات المحددة في دفتر يومية دفتر وصول الصنف.</span><span class="sxs-lookup"><span data-stu-id="85a37-186">Then, when Sammy clicks **Start arrival**, the selected records are automatically created in an item arrival journal.</span></span> <span data-ttu-id="85a37-187">تتضمن السجلات معلومات حول البنود، ويتم تعيين كافة معلومات الحقل الفريدة.</span><span class="sxs-lookup"><span data-stu-id="85a37-187">The records include line information, and all unique field information is assigned.</span></span>

## <a name="update-arrival-information-and-process-a-product-receipt"></a><span data-ttu-id="85a37-188">تحديث معلومات الوصول ومعالجة إيصال استلام المنتجات</span><span class="sxs-lookup"><span data-stu-id="85a37-188">Update arrival information and process a product receipt</span></span>
<span data-ttu-id="85a37-189">بعد تسجيل كافة السلع، يستطيع مدير المستودع أو مدير الشراء تحديث الأصناف المستلمة بواسطة إيصال استلام المنتجات لإضافة التكلفة الفعلية.</span><span class="sxs-lookup"><span data-stu-id="85a37-189">When all goods have been registered, the warehouse manager or purchasing manager can update the received items with a product receipt to add the physical cost.</span></span> <span data-ttu-id="85a37-190">لتحديث معلومات الوصول وترحيل إيصال استلام المنتجات، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="85a37-190">To update arrival information and post a product receipt, follow these steps.</span></span>

1.  <span data-ttu-id="85a37-191">انقر فوق **إدارة المخزون** &gt; **الأوامر الواردة** &gt; **نظرة عامة على الوصول**.</span><span class="sxs-lookup"><span data-stu-id="85a37-191">Click **Inventory management** &gt; **Inbound orders** &gt; **Arrival overview**.</span></span>
2.  <span data-ttu-id="85a37-192">في الصفحة **نظرة عامة على الوصول**، انقر فوق **دفاتر اليومية** &gt; **دفاتر اليومية الجاهزة لإيصال استلام المنتجات‬** لعرض قائمة بدفاتر اليومية الجاهزة لتحديث إيصال استلام المنتجات.</span><span class="sxs-lookup"><span data-stu-id="85a37-192">On the **Arrival overview** page, click **Journals** &gt; **Product receipt ready journals** to show a list of the journals that are ready for product receipt update.</span></span>
3.  <span data-ttu-id="85a37-193">حدد دفاتر اليومية التي يجب تحديثها، ثم انقر فوق **الوظائف** &gt; **إيصال استلام المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="85a37-193">Select the journals that must be updated, and then click **Functions** &gt; **Product receipt**.</span></span>
4.  <span data-ttu-id="85a37-194">في الصفحة **ترحيل**، أدخل رقم إيصال استلام المنتجات، إذا لم يكن متوفرًا في دفتر اليومية، ومن ثم انقر فوق **موافق** لمعالجة إيصال استلام المنتجات.</span><span class="sxs-lookup"><span data-stu-id="85a37-194">On the **Posting** page, enter the product receipt number, if it isn't already available on the journal, and then click **OK** to process the product receipt.</span></span>

## <a name="summary"></a><span data-ttu-id="85a37-195">ملخص</span><span class="sxs-lookup"><span data-stu-id="85a37-195">Summary</span></span>
<span data-ttu-id="85a37-196">باستطاعة الصفحة **نظرة عامة على الوصول** مساعدة مدير المستودع والعاملين فيه على تحقيق نظرة عامة على العمل المتوقع الذي يجب تنفيذه كجزء من عملية واردة.</span><span class="sxs-lookup"><span data-stu-id="85a37-196">The **Arrival overview** page can help the warehouse manager and warehouse workers achieve an overview of expected work that must be done as part of an inbound process.</span></span> <span data-ttu-id="85a37-197">ويمكن استخدام الصفحة أيضًا لبدء عملية وصول الصنف، للمساعدة في ضمان تعقب هذه العناصر عند الدخول الأول إلى المستودع.</span><span class="sxs-lookup"><span data-stu-id="85a37-197">The page can also be used to start the item arrival process, to help guarantee that items are tracked at the first entry into the warehouse.</span></span>
