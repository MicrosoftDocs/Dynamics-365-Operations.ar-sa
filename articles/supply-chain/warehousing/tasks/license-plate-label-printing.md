---
title: تمكين طباعة بطاقة لوحة الترخيص
description: يبين هذا الموضوع كيفية تمكين الطباعة التلقائية لبطاقة كود مسلسل لحاوية الشحن (SSCC)‬ بعد انتقاء الصنف الأخير من المخزون في عملية انتقاء المبيعات.
author: perlynne
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 545f1c15888bcd0b46e1028f58cbe3a274846c92
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146013"
---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="aa80e-103">تمكين طباعة بطاقة لوحة الترخيص</span><span class="sxs-lookup"><span data-stu-id="aa80e-103">Enable license plate label printing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aa80e-104">يبين هذا الموضوع كيفية تمكين الطباعة التلقائية لبطاقة كود مسلسل لحاوية الشحن (SSCC)‬ بعد انتقاء الصنف الأخير من المخزون في عملية انتقاء المبيعات.</span><span class="sxs-lookup"><span data-stu-id="aa80e-104">This topic shows how to enable the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="aa80e-105">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="aa80e-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="aa80e-106">إذا كنت تقوم بتشغيله باستخدام بياناتك الخاصة، فيجب إعداد تسلسل رقم للوحات الترخيص.</span><span class="sxs-lookup"><span data-stu-id="aa80e-106">If you're run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="aa80e-107">تحتاج إلى إعداد طابعة بطاقات قبل البدء في هذه المهمة.</span><span class="sxs-lookup"><span data-stu-id="aa80e-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="aa80e-108">انتقل إلى إدارة المؤسسة > إعداد > طابعات الشبكة‬.</span><span class="sxs-lookup"><span data-stu-id="aa80e-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="aa80e-109">في جزء الإجراءات، انقر فوق "خيارات"، ثم فوق الزر "تنزيل مثبّت عامل توجيه المستند‬".</span><span class="sxs-lookup"><span data-stu-id="aa80e-109">On the Action pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="aa80e-110">شغّل المثبت، وتأكد من أن لديك طابعة شبكة صالحة معينة إلى "نشطة" قبل متابعة الإجراء.</span><span class="sxs-lookup"><span data-stu-id="aa80e-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="aa80e-111">إعداد بادئة الشركة GS1</span><span class="sxs-lookup"><span data-stu-id="aa80e-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="aa80e-112">انتقل إلى **جزء التنقل > الوحدات النمطية > إدارة المخزون > الإعداد > محددات إدارة المستودعات‬**.</span><span class="sxs-lookup"><span data-stu-id="aa80e-112">Go to **Navigation pane > Modules > Warehouse management > Setup > Warehouse management parameters**.</span></span>
2. <span data-ttu-id="aa80e-113">في الحقل **بادئة الشركة GS1**، أدخل الأرقام السبعة لرقم شركتك GS1.</span><span class="sxs-lookup"><span data-stu-id="aa80e-113">In the **GS1 company prefix** field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="aa80e-114">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="aa80e-114">Select **Save**.</span></span>
4. <span data-ttu-id="aa80e-115">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="aa80e-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="aa80e-116">إعداد تسلسل لوحة ترخيص المستخدم</span><span class="sxs-lookup"><span data-stu-id="aa80e-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="aa80e-117">انتقل إلى **جزء التنقل > الوحدات النمطية > إدارة المؤسسة > التسلسلات الرقمية > التسلسلات الرقمية**.</span><span class="sxs-lookup"><span data-stu-id="aa80e-117">Go to **Navigation pane > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="aa80e-118">في الحقل **المنطقة**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="aa80e-118">In the **Area** field, select an option.</span></span>
3. <span data-ttu-id="aa80e-119">في الحقل **المرجع**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="aa80e-119">In the **Reference** field, select an option.</span></span>
4. <span data-ttu-id="aa80e-120">في الحقل **الشركة**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="aa80e-120">In the **Company** field, type a value.</span></span>
5. <span data-ttu-id="aa80e-121">وسّع قسم **الشرائح**.</span><span class="sxs-lookup"><span data-stu-id="aa80e-121">Expand the **Segments** section.</span></span>
6. <span data-ttu-id="aa80e-122">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="aa80e-122">Select **Edit**.</span></span>
7. <span data-ttu-id="aa80e-123">في جدول **الشرائح**، حدد الصف الأول</span><span class="sxs-lookup"><span data-stu-id="aa80e-123">In the **Segments** table, select the first row</span></span>
8. <span data-ttu-id="aa80e-124">حدد **إزالة**.</span><span class="sxs-lookup"><span data-stu-id="aa80e-124">Select **Remove**.</span></span>
9. <span data-ttu-id="aa80e-125">حدد **إزالة**.</span><span class="sxs-lookup"><span data-stu-id="aa80e-125">Select **Remove**.</span></span>
10. <span data-ttu-id="aa80e-126">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="aa80e-126">Select **Save**.</span></span>
11. <span data-ttu-id="aa80e-127">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="aa80e-127">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="aa80e-128">إنشاء تخطيط مسار المستند</span><span class="sxs-lookup"><span data-stu-id="aa80e-128">Create the document route layout</span></span>
1. <span data-ttu-id="aa80e-129">انتقل إلى **جزء التنقل > الوحدات النمطية إدارة المستودعات > الإعداد > توجيه المستند > تخطيطات توجيه المستند**.</span><span class="sxs-lookup"><span data-stu-id="aa80e-129">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing layouts**.</span></span> <span data-ttu-id="aa80e-130">مكّن تخطيط SSCC.</span><span class="sxs-lookup"><span data-stu-id="aa80e-130">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="aa80e-131">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="aa80e-131">Select **New**.</span></span>
3. <span data-ttu-id="aa80e-132">في الحقل **معرف التخطيط**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="aa80e-132">In the **Layout ID** field, type a value.</span></span>
4. <span data-ttu-id="aa80e-133">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="aa80e-133">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="aa80e-134">حدد **إدراج في نهاية النص**.</span><span class="sxs-lookup"><span data-stu-id="aa80e-134">Select **Insert at end of text**.</span></span>
6. <span data-ttu-id="aa80e-135">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="aa80e-135">Select **Save**.</span></span>
7. <span data-ttu-id="aa80e-136">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="aa80e-136">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="aa80e-137">إعداد توجيه المستندات</span><span class="sxs-lookup"><span data-stu-id="aa80e-137">Set up the document routing</span></span>
1. <span data-ttu-id="aa80e-138">انتقل إلى **جزء التنقل > الوحدات النمطية إدارة المستودعات > الإعداد > توجيه المستند > توجيه المستند**.</span><span class="sxs-lookup"><span data-stu-id="aa80e-138">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing**.</span></span>
2. <span data-ttu-id="aa80e-139">في الحقل **نوع أمر العمل**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="aa80e-139">In the **Work order type** field, select an option.</span></span>
3. <span data-ttu-id="aa80e-140">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="aa80e-140">Select **New**.</span></span>
4. <span data-ttu-id="aa80e-141">في الحقل **المستودع**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="aa80e-141">In the **Warehouse** field, type a value.</span></span>
5. <span data-ttu-id="aa80e-142">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="aa80e-142">In the **Name** field, type a value.</span></span>
6. <span data-ttu-id="aa80e-143">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="aa80e-143">Select **New**.</span></span>
7. <span data-ttu-id="aa80e-144">في الحقل **معرف التخطيط**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="aa80e-144">In the **Layout ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="aa80e-145">في حقل **الاسم**، أدخل اسم الطابعة المراد استخدامها.</span><span class="sxs-lookup"><span data-stu-id="aa80e-145">In the **Name** field, enter the printer name that you want to use.</span></span>
9. <span data-ttu-id="aa80e-146">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="aa80e-146">Select **Save**.</span></span>
10. <span data-ttu-id="aa80e-147">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="aa80e-147">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="aa80e-148">إنشاء قائمة الجهاز المحمول</span><span class="sxs-lookup"><span data-stu-id="aa80e-148">Create mobile device menu</span></span>
1. <span data-ttu-id="aa80e-149">انتقل إلى **جزء التنقل > الوحدات النمطية > إدارة المستودعات > الإعداد > الجهاز المحمول > عناصر قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="aa80e-149">Go to **Navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu items**.</span></span>
2. <span data-ttu-id="aa80e-150">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="aa80e-150">Select **New**.</span></span>
3. <span data-ttu-id="aa80e-151">في الحقل **اسم عنصر القائمة‬**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="aa80e-151">In the **Menu item name** field, type a value.</span></span>
4. <span data-ttu-id="aa80e-152">في الحقل **العنوان**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="aa80e-152">In the **Title** field, type a value.</span></span>
5. <span data-ttu-id="aa80e-153">في الحقل **الوضع**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="aa80e-153">In the **Mode** field, select an option.</span></span>
6. <span data-ttu-id="aa80e-154">حدد **نعم** في الحقل **استخدام العمل الموجود**.</span><span class="sxs-lookup"><span data-stu-id="aa80e-154">Select **Yes** in the **Use existing work** field.</span></span>
7. <span data-ttu-id="aa80e-155">حدد **نعم** في الحقل **إنشاء لوحة ترخيص**.</span><span class="sxs-lookup"><span data-stu-id="aa80e-155">Select **Yes** in the **Generate license plate** field.</span></span>
8. <span data-ttu-id="aa80e-156">وسّع مقطع **فئات العمل**.</span><span class="sxs-lookup"><span data-stu-id="aa80e-156">Expand the **Work classes** section.</span></span>
9. <span data-ttu-id="aa80e-157">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="aa80e-157">Select **New**.</span></span>
10. <span data-ttu-id="aa80e-158">في الحقل **معرف فئة العمل**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="aa80e-158">In the **Work class ID** field, type a value.</span></span>
11. <span data-ttu-id="aa80e-159">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="aa80e-159">Select **Save**.</span></span>
12. <span data-ttu-id="aa80e-160">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="aa80e-160">Close the page.</span></span>
13. <span data-ttu-id="aa80e-161">انتقل إلى **جزء التنقل > الوحدات النمطية > إدارة المستودعات > الإعداد > الجهاز المحمول > عناصر قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="aa80e-161">Go to **navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu**.</span></span>
14. <span data-ttu-id="aa80e-162">في الشجرة، حدد عنصر القائمة الذي قمت بإنشائه من قبل.</span><span class="sxs-lookup"><span data-stu-id="aa80e-162">In the tree, select the menu item that you created before.</span></span>
15. <span data-ttu-id="aa80e-163">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="aa80e-163">Select **Edit**.</span></span>
16. <span data-ttu-id="aa80e-164">حدد السهم لإضافة عنصر القائمة إلى القائمة.</span><span class="sxs-lookup"><span data-stu-id="aa80e-164">Select the arrow to add the menu item to the menu.</span></span>
17. <span data-ttu-id="aa80e-165">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="aa80e-165">Select **Save**.</span></span>
18. <span data-ttu-id="aa80e-166">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="aa80e-166">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="aa80e-167">تحديث قالب عمل</span><span class="sxs-lookup"><span data-stu-id="aa80e-167">Update a work template</span></span>
1. <span data-ttu-id="aa80e-168">انتقل إلى **جزء التنقل > الوحدات النمطية > إدارة المستودعات > الإعداد > العمل > قوالب العمل**.</span><span class="sxs-lookup"><span data-stu-id="aa80e-168">Go to **Navigation pane > Modules > Warehouse management > Setup > Work > Work templates**.</span></span>
2. <span data-ttu-id="aa80e-169">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="aa80e-169">Select **Edit**.</span></span>
3. <span data-ttu-id="aa80e-170">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="aa80e-170">Select **New**.</span></span>
4. <span data-ttu-id="aa80e-171">في الحقل **نوع العمل**، حدد **طباعة**.</span><span class="sxs-lookup"><span data-stu-id="aa80e-171">In the **Work type** field, select **Print**.</span></span>
5. <span data-ttu-id="aa80e-172">في الحقل **معرف فئة العمل**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="aa80e-172">In the **Work class ID** field, enter or select a value.</span></span>
6. <span data-ttu-id="aa80e-173">حدد **تحريك لأعلى**.</span><span class="sxs-lookup"><span data-stu-id="aa80e-173">Select **Move up**.</span></span>
7. <span data-ttu-id="aa80e-174">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="aa80e-174">Select **Save**.</span></span>
8. <span data-ttu-id="aa80e-175">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="aa80e-175">Close the page.</span></span>

