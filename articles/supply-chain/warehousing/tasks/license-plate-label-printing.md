---
title: تمكين طباعة بطاقة لوحة الترخيص
description: يتيح هذا الإجراء الطباعة التلقائية لبطاقة كود مسلسل لحاوية الشحن (SSCC)‬ بعد انتقاء الصنف الأخير من المخزون في عملية انتقاء المبيعات.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8d906ca9f5a6536870fa0c322a0792ed5672c25e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "324021"
---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="566d3-103">تمكين طباعة بطاقة لوحة الترخيص</span><span class="sxs-lookup"><span data-stu-id="566d3-103">Enable license plate label printing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="566d3-104">يتيح هذا الإجراء الطباعة التلقائية لبطاقة كود مسلسل لحاوية الشحن (SSCC)‬ بعد انتقاء الصنف الأخير من المخزون في عملية انتقاء المبيعات.</span><span class="sxs-lookup"><span data-stu-id="566d3-104">This procedure enables the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="566d3-105">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="566d3-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="566d3-106">إذا كنت تقوم بتشغيله باستخدام بياناتك الخاصة، فيجب إعداد تسلسل رقم للوحات الترخيص.</span><span class="sxs-lookup"><span data-stu-id="566d3-106">If you’re run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="566d3-107">تحتاج إلى إعداد طابعة بطاقات قبل البدء في هذه المهمة.</span><span class="sxs-lookup"><span data-stu-id="566d3-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="566d3-108">انتقل إلى إدارة المؤسسة > إعداد > طابعات الشبكة‬.</span><span class="sxs-lookup"><span data-stu-id="566d3-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="566d3-109">في جزء الإجراءات، انقر فوق "خيارات"، ثم فوق الزر "تنزيل مثبّت عامل توجيه المستند‬".</span><span class="sxs-lookup"><span data-stu-id="566d3-109">On the Action pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="566d3-110">شغّل المثبت، وتأكد من أن لديك طابعة شبكة صالحة معينة إلى "نشطة" قبل متابعة الإجراء.</span><span class="sxs-lookup"><span data-stu-id="566d3-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="566d3-111">إعداد بادئة الشركة GS1</span><span class="sxs-lookup"><span data-stu-id="566d3-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="566d3-112">انتقل إلى إدارة المستودعات > إعداد‬ > محددات إدارة المستودعات.</span><span class="sxs-lookup"><span data-stu-id="566d3-112">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="566d3-113">في الحقل "بادئة الشركة GS1"، أدخل الأرقام السبعة لرقم شركتك GS1.</span><span class="sxs-lookup"><span data-stu-id="566d3-113">In the GS1 company prefix field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="566d3-114">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="566d3-114">Click Save.</span></span>
4. <span data-ttu-id="566d3-115">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="566d3-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="566d3-116">إعداد تسلسل لوحة ترخيص المستخدم</span><span class="sxs-lookup"><span data-stu-id="566d3-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="566d3-117">انتقل إلى إدارة المؤسسة > التسلسلات الرقمية > التسلسلات الرقمية.</span><span class="sxs-lookup"><span data-stu-id="566d3-117">Go to Organization administration > Number sequences > Number sequences.</span></span>
2. <span data-ttu-id="566d3-118">في الحقل "المنطقة"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="566d3-118">In the Area field, select an option.</span></span>
3. <span data-ttu-id="566d3-119">في الحقل "المرجع"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="566d3-119">In the Reference field, select an option.</span></span>
4. <span data-ttu-id="566d3-120">في الحقل "الشركة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="566d3-120">In the Company field, type a value.</span></span>
5. <span data-ttu-id="566d3-121">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="566d3-121">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="566d3-122">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="566d3-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="566d3-123">وسّع مقطع "المقاطع‬".</span><span class="sxs-lookup"><span data-stu-id="566d3-123">Expand the Segments section.</span></span>
8. <span data-ttu-id="566d3-124">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="566d3-124">Click Edit.</span></span>
9. <span data-ttu-id="566d3-125">في جدول المقاطع، حدد الصف الأول</span><span class="sxs-lookup"><span data-stu-id="566d3-125">In the Segments table, select the first row</span></span>
10. <span data-ttu-id="566d3-126">انقر فوق "إزالة".</span><span class="sxs-lookup"><span data-stu-id="566d3-126">Click Remove.</span></span>
11. <span data-ttu-id="566d3-127">انقر فوق "إزالة".</span><span class="sxs-lookup"><span data-stu-id="566d3-127">Click Remove.</span></span>
12. <span data-ttu-id="566d3-128">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="566d3-128">Click Save.</span></span>
13. <span data-ttu-id="566d3-129">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="566d3-129">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="566d3-130">إنشاء تخطيط مسار المستند</span><span class="sxs-lookup"><span data-stu-id="566d3-130">Create the document route layout</span></span>
1. <span data-ttu-id="566d3-131">انتقل إلى إدارة المستودعات > إعداد > توجيه المستند > تخطيطات توجيه المستند.</span><span class="sxs-lookup"><span data-stu-id="566d3-131">Go to Warehouse management > Setup > Document routing > Document routing layouts.</span></span>
    * <span data-ttu-id="566d3-132">مكّن تخطيط SSCC.</span><span class="sxs-lookup"><span data-stu-id="566d3-132">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="566d3-133">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="566d3-133">Click New.</span></span>
3. <span data-ttu-id="566d3-134">في الحقل "معرف التخطيط"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="566d3-134">In the Layout ID field, type a value.</span></span>
4. <span data-ttu-id="566d3-135">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="566d3-135">In the Description field, type a value.</span></span>
5. <span data-ttu-id="566d3-136">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="566d3-136">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="566d3-137">انقر فوق "إدراج في نهاية النص".</span><span class="sxs-lookup"><span data-stu-id="566d3-137">Click Insert at end of text.</span></span>
7. <span data-ttu-id="566d3-138">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="566d3-138">Click Save.</span></span>
8. <span data-ttu-id="566d3-139">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="566d3-139">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="566d3-140">إعداد توجيه المستندات</span><span class="sxs-lookup"><span data-stu-id="566d3-140">Set up the document routing</span></span>
1. <span data-ttu-id="566d3-141">انتقل إلى إدارة المستودعات > إعداد > توجيه المستند > توجيه المستند.</span><span class="sxs-lookup"><span data-stu-id="566d3-141">Go to Warehouse management > Setup > Document routing > Document routing.</span></span>
2. <span data-ttu-id="566d3-142">في الحقل "نوع أمر العمل‬"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="566d3-142">In the Work order type field, select an option.</span></span>
3. <span data-ttu-id="566d3-143">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="566d3-143">Click New.</span></span>
4. <span data-ttu-id="566d3-144">في الحقل "المستودع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="566d3-144">In the Warehouse field, type a value.</span></span>
5. <span data-ttu-id="566d3-145">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="566d3-145">In the Name field, type a value.</span></span>
6. <span data-ttu-id="566d3-146">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="566d3-146">Click New.</span></span>
7. <span data-ttu-id="566d3-147">في الحقل "معرف التخطيط‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="566d3-147">In the Layout ID field, enter or select a value.</span></span>
8. <span data-ttu-id="566d3-148">في حقل "الاسم"، أدخل اسم الطابعة المراد استخدامها.</span><span class="sxs-lookup"><span data-stu-id="566d3-148">In the Name field, enter the printer name that you want to use..</span></span>
9. <span data-ttu-id="566d3-149">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="566d3-149">Click Save.</span></span>
10. <span data-ttu-id="566d3-150">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="566d3-150">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="566d3-151">إنشاء قائمة الجهاز المحمول</span><span class="sxs-lookup"><span data-stu-id="566d3-151">Create mobile device menu</span></span>
1. <span data-ttu-id="566d3-152">انتقل إلى إدارة المستودعات > إعداد > الجهاز المحمول > عناصر قائمة الجهاز المحمول.</span><span class="sxs-lookup"><span data-stu-id="566d3-152">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="566d3-153">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="566d3-153">Click New.</span></span>
3. <span data-ttu-id="566d3-154">في الحقل "اسم عنصر القائمة‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="566d3-154">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="566d3-155">في الحقل "المسمى الوظيفي"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="566d3-155">In the Title field, type a value.</span></span>
5. <span data-ttu-id="566d3-156">في الحقل "الوضع"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="566d3-156">In the Mode field, select an option.</span></span>
6. <span data-ttu-id="566d3-157">حدد "نعم" في الحقل "استخدام العمل الموجود‬".</span><span class="sxs-lookup"><span data-stu-id="566d3-157">Select Yes in the Use existing work field.</span></span>
7. <span data-ttu-id="566d3-158">حدد "نعم" في حقل "إنشاء لوحة ترخيص‬".</span><span class="sxs-lookup"><span data-stu-id="566d3-158">Select Yes in the Generate license plate field.</span></span>
8. <span data-ttu-id="566d3-159">وسّع مقطع "فئات العمل".</span><span class="sxs-lookup"><span data-stu-id="566d3-159">Expand the Work classes section.</span></span>
9. <span data-ttu-id="566d3-160">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="566d3-160">Click New.</span></span>
10. <span data-ttu-id="566d3-161">في الحقل "معرف فئة العمل"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="566d3-161">In the Work class ID field, type a value.</span></span>
11. <span data-ttu-id="566d3-162">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="566d3-162">Click Save.</span></span>
12. <span data-ttu-id="566d3-163">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="566d3-163">Close the page.</span></span>
13. <span data-ttu-id="566d3-164">انتقل إلى إدارة المستودعات > إعداد > جهاز محمول > قائمة الجهاز المحمول.</span><span class="sxs-lookup"><span data-stu-id="566d3-164">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
14. <span data-ttu-id="566d3-165">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="566d3-165">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="566d3-166">في الشجرة، حدد "في الشجرة، حدد عنصر القائمة الذي قمت بإنشائه من قبل".</span><span class="sxs-lookup"><span data-stu-id="566d3-166">In the tree, select 'In the tree, select the menu item that you created before.'.</span></span>
16. <span data-ttu-id="566d3-167">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="566d3-167">Click Edit.</span></span>
17. <span data-ttu-id="566d3-168">انقر فوق السهم لإضافة عنصر القائمة إلى القائمة.</span><span class="sxs-lookup"><span data-stu-id="566d3-168">Click on the arrow to add the menu item to the menu.</span></span>
18. <span data-ttu-id="566d3-169">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="566d3-169">Click Save.</span></span>
19. <span data-ttu-id="566d3-170">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="566d3-170">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="566d3-171">تحديث قالب عمل</span><span class="sxs-lookup"><span data-stu-id="566d3-171">Update a work template</span></span>
1. <span data-ttu-id="566d3-172">انتقل إلى إدارة المستودعات > إعداد > العمل > قوالب العمل.</span><span class="sxs-lookup"><span data-stu-id="566d3-172">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="566d3-173">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="566d3-173">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="566d3-174">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="566d3-174">Click Edit.</span></span>
4. <span data-ttu-id="566d3-175">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="566d3-175">Click New.</span></span>
5. <span data-ttu-id="566d3-176">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="566d3-176">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="566d3-177">في الحقل "نوع العمل"، حدد "طباعة".</span><span class="sxs-lookup"><span data-stu-id="566d3-177">In the Work type field, select 'Print'.</span></span>
7. <span data-ttu-id="566d3-178">في الحقل "معرف فئة العمل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="566d3-178">In the Work class ID field, enter or select a value.</span></span>
8. <span data-ttu-id="566d3-179">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="566d3-179">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="566d3-180">انقر فوق "تحريك لأعلى".</span><span class="sxs-lookup"><span data-stu-id="566d3-180">Click Move up.</span></span>
10. <span data-ttu-id="566d3-181">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="566d3-181">Click Save.</span></span>
11. <span data-ttu-id="566d3-182">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="566d3-182">Close the page.</span></span>

