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
ms.openlocfilehash: ed4fa28039c9320998f6524c9c9edb0a0301b7b0
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/08/2019
ms.locfileid: "1866816"
---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="9c7e8-103">تمكين طباعة بطاقة لوحة الترخيص</span><span class="sxs-lookup"><span data-stu-id="9c7e8-103">Enable license plate label printing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9c7e8-104">يبين هذا الموضوع كيفية تمكين الطباعة التلقائية لبطاقة كود مسلسل لحاوية الشحن (SSCC)‬ بعد انتقاء الصنف الأخير من المخزون في عملية انتقاء المبيعات.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-104">This topic shows how to enable the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="9c7e8-105">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="9c7e8-106">إذا كنت تقوم بتشغيله باستخدام بياناتك الخاصة، فيجب إعداد تسلسل رقم للوحات الترخيص.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-106">If you’re run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="9c7e8-107">تحتاج إلى إعداد طابعة بطاقات قبل البدء في هذه المهمة.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="9c7e8-108">انتقل إلى إدارة المؤسسة > إعداد > طابعات الشبكة‬.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="9c7e8-109">في جزء الإجراءات، انقر فوق "خيارات"، ثم فوق الزر "تنزيل مثبّت عامل توجيه المستند‬".</span><span class="sxs-lookup"><span data-stu-id="9c7e8-109">On the Action pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="9c7e8-110">شغّل المثبت، وتأكد من أن لديك طابعة شبكة صالحة معينة إلى "نشطة" قبل متابعة الإجراء.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="9c7e8-111">إعداد بادئة الشركة GS1</span><span class="sxs-lookup"><span data-stu-id="9c7e8-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="9c7e8-112">انتقل إلى **جزء التنقل > الوحدات النمطية > إدارة المخزون > الإعداد > محددات إدارة المستودعات‬**.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-112">Go to **Navigation pane > Modules > Warehouse management > Setup > Warehouse management parameters**.</span></span>
2. <span data-ttu-id="9c7e8-113">في الحقل **بادئة الشركة GS1**، أدخل الأرقام السبعة لرقم شركتك GS1.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-113">In the **GS1 company prefix** field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="9c7e8-114">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-114">Select **Save**.</span></span>
4. <span data-ttu-id="9c7e8-115">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="9c7e8-116">إعداد تسلسل لوحة ترخيص المستخدم</span><span class="sxs-lookup"><span data-stu-id="9c7e8-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="9c7e8-117">انتقل إلى **جزء التنقل > الوحدات النمطية > إدارة المؤسسة > التسلسلات الرقمية > التسلسلات الرقمية**.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-117">Go to **Navigation pane > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="9c7e8-118">في الحقل **المنطقة**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-118">In the **Area** field, select an option.</span></span>
3. <span data-ttu-id="9c7e8-119">في الحقل **المرجع**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-119">In the **Reference** field, select an option.</span></span>
4. <span data-ttu-id="9c7e8-120">في الحقل **الشركة**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-120">In the **Company** field, type a value.</span></span>
5. <span data-ttu-id="9c7e8-121">وسّع قسم **الشرائح**.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-121">Expand the **Segments** section.</span></span>
6. <span data-ttu-id="9c7e8-122">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-122">Select **Edit**.</span></span>
7. <span data-ttu-id="9c7e8-123">في جدول **الشرائح**، حدد الصف الأول</span><span class="sxs-lookup"><span data-stu-id="9c7e8-123">In the **Segments** table, select the first row</span></span>
8. <span data-ttu-id="9c7e8-124">حدد **إزالة**.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-124">Select **Remove**.</span></span>
9. <span data-ttu-id="9c7e8-125">حدد **إزالة**.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-125">Select **Remove**.</span></span>
10. <span data-ttu-id="9c7e8-126">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-126">Select **Save**.</span></span>
11. <span data-ttu-id="9c7e8-127">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-127">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="9c7e8-128">إنشاء تخطيط مسار المستند</span><span class="sxs-lookup"><span data-stu-id="9c7e8-128">Create the document route layout</span></span>
1. <span data-ttu-id="9c7e8-129">انتقل إلى **جزء التنقل > الوحدات النمطية إدارة المستودعات > الإعداد > توجيه المستند > تخطيطات توجيه المستند**.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-129">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing layouts**.</span></span> <span data-ttu-id="9c7e8-130">مكّن تخطيط SSCC.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-130">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="9c7e8-131">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-131">Select **New**.</span></span>
3. <span data-ttu-id="9c7e8-132">في الحقل **معرف التخطيط**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-132">In the **Layout ID** field, type a value.</span></span>
4. <span data-ttu-id="9c7e8-133">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-133">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="9c7e8-134">حدد **إدراج في نهاية النص**.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-134">Select **Insert at end of text**.</span></span>
6. <span data-ttu-id="9c7e8-135">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-135">Select **Save**.</span></span>
7. <span data-ttu-id="9c7e8-136">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-136">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="9c7e8-137">إعداد توجيه المستندات</span><span class="sxs-lookup"><span data-stu-id="9c7e8-137">Set up the document routing</span></span>
1. <span data-ttu-id="9c7e8-138">انتقل إلى **جزء التنقل > الوحدات النمطية إدارة المستودعات > الإعداد > توجيه المستند > توجيه المستند**.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-138">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing**.</span></span>
2. <span data-ttu-id="9c7e8-139">في الحقل **نوع أمر العمل**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-139">In the **Work order type** field, select an option.</span></span>
3. <span data-ttu-id="9c7e8-140">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-140">Select **New**.</span></span>
4. <span data-ttu-id="9c7e8-141">في الحقل **المستودع**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-141">In the **Warehouse** field, type a value.</span></span>
5. <span data-ttu-id="9c7e8-142">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-142">In the **Name** field, type a value.</span></span>
6. <span data-ttu-id="9c7e8-143">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-143">Select **New**.</span></span>
7. <span data-ttu-id="9c7e8-144">في الحقل **معرف التخطيط**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-144">In the **Layout ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="9c7e8-145">في حقل **الاسم**، أدخل اسم الطابعة المراد استخدامها.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-145">In the **Name** field, enter the printer name that you want to use.</span></span>
9. <span data-ttu-id="9c7e8-146">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-146">Select **Save**.</span></span>
10. <span data-ttu-id="9c7e8-147">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-147">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="9c7e8-148">إنشاء قائمة الجهاز المحمول</span><span class="sxs-lookup"><span data-stu-id="9c7e8-148">Create mobile device menu</span></span>
1. <span data-ttu-id="9c7e8-149">انتقل إلى **جزء التنقل > الوحدات النمطية > إدارة المستودعات > الإعداد > الجهاز المحمول > عناصر قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-149">Go to **Navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu items**.</span></span>
2. <span data-ttu-id="9c7e8-150">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-150">Select **New**.</span></span>
3. <span data-ttu-id="9c7e8-151">في الحقل **اسم عنصر القائمة‬**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-151">In the **Menu item name** field, type a value.</span></span>
4. <span data-ttu-id="9c7e8-152">في الحقل **العنوان**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-152">In the **Title** field, type a value.</span></span>
5. <span data-ttu-id="9c7e8-153">في الحقل **الوضع**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-153">In the **Mode** field, select an option.</span></span>
6. <span data-ttu-id="9c7e8-154">حدد **نعم** في الحقل **استخدام العمل الموجود**.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-154">Select **Yes** in the **Use existing work** field.</span></span>
7. <span data-ttu-id="9c7e8-155">حدد **نعم** في الحقل **إنشاء لوحة ترخيص**.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-155">Select **Yes** in the **Generate license plate** field.</span></span>
8. <span data-ttu-id="9c7e8-156">وسّع مقطع **فئات العمل**.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-156">Expand the **Work classes** section.</span></span>
9. <span data-ttu-id="9c7e8-157">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-157">Select **New**.</span></span>
10. <span data-ttu-id="9c7e8-158">في الحقل **معرف فئة العمل**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-158">In the **Work class ID** field, type a value.</span></span>
11. <span data-ttu-id="9c7e8-159">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-159">Select **Save**.</span></span>
12. <span data-ttu-id="9c7e8-160">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-160">Close the page.</span></span>
13. <span data-ttu-id="9c7e8-161">انتقل إلى **جزء التنقل > الوحدات النمطية > إدارة المستودعات > الإعداد > الجهاز المحمول > عناصر قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-161">Go to **navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu**.</span></span>
14. <span data-ttu-id="9c7e8-162">في الشجرة، حدد عنصر القائمة الذي قمت بإنشائه من قبل.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-162">In the tree, select the menu item that you created before.</span></span>
15. <span data-ttu-id="9c7e8-163">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-163">Select **Edit**.</span></span>
16. <span data-ttu-id="9c7e8-164">حدد السهم لإضافة عنصر القائمة إلى القائمة.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-164">Select the arrow to add the menu item to the menu.</span></span>
17. <span data-ttu-id="9c7e8-165">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-165">Select **Save**.</span></span>
18. <span data-ttu-id="9c7e8-166">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-166">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="9c7e8-167">تحديث قالب عمل</span><span class="sxs-lookup"><span data-stu-id="9c7e8-167">Update a work template</span></span>
1. <span data-ttu-id="9c7e8-168">انتقل إلى **جزء التنقل > الوحدات النمطية > إدارة المستودعات > الإعداد > العمل > قوالب العمل**.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-168">Go to **Navigation pane > Modules > Warehouse management > Setup > Work > Work templates**.</span></span>
2. <span data-ttu-id="9c7e8-169">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-169">Select **Edit**.</span></span>
3. <span data-ttu-id="9c7e8-170">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-170">Select **New**.</span></span>
4. <span data-ttu-id="9c7e8-171">في الحقل **نوع العمل**، حدد **طباعة**.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-171">In the **Work type** field, select **Print**.</span></span>
5. <span data-ttu-id="9c7e8-172">في الحقل **معرف فئة العمل**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-172">In the **Work class ID** field, enter or select a value.</span></span>
6. <span data-ttu-id="9c7e8-173">حدد **تحريك لأعلى**.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-173">Select **Move up**.</span></span>
7. <span data-ttu-id="9c7e8-174">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-174">Select **Save**.</span></span>
8. <span data-ttu-id="9c7e8-175">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-175">Close the page.</span></span>

