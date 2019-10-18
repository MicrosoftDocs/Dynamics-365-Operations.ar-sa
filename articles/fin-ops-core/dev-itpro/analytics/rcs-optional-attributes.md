---
title: استيراد ملفات بتنسيق XML مع سمات اختيارية
description: يوفر هذا الموضوع معلومات حول تصميم تنسيقات ER التي تحدد سمات XML لتحليل المستندات الإلكترونية الواردة بتنسيق XML.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: eb5d721784f45097ab466f75d43256495aac36ca
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182820"
---
# <a name="import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="8b107-103">استيراد ملفات بتنسيق XML مع سمات اختيارية</span><span class="sxs-lookup"><span data-stu-id="8b107-103">Import files in XML format with optional attributes</span></span>

<span data-ttu-id="8b107-104">يمكنك تصميم تنسيقات إعداد التقارير الإلكترونية (ER) لتحليل المستندات الإلكترونية الواردة بتنسيق XML.</span><span class="sxs-lookup"><span data-stu-id="8b107-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents in XML format.</span></span> <span data-ttu-id="8b107-105">يمكن تحديد سمات معينة لعناصر XML بتنسيق ER مصمم كخيار اختياري.</span><span class="sxs-lookup"><span data-stu-id="8b107-105">Certain attributes of XML elements can be specified in designed ER format as optional.</span></span> <span data-ttu-id="8b107-106">سيسمح لك ذلك بمعالجة الملفات الواردة باستخدام سمات XML هذه ومن دونها بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="8b107-106">It will allow you to handle incoming files with and without such XML attributes properly.</span></span> <span data-ttu-id="8b107-107">يمكنك بعد ذلك استخدام المحتوى من هذه الملفات لتحديث بيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="8b107-107">You can then use the content from these files to update application data.</span></span>

<span data-ttu-id="8b107-108">لمعرفة المزيد حول هذه الميزة، أكمل الخطوات الموجودة في الموضوع، [استيراد ملفات RCS بتنسيق XML مع سمات اختيارية](tasks/import-files-xml-format-optional-attributes.md)، وهي جزء من العملية التجارية 7.5.4.3 اكتساب/تطوير خدمة تكنولوجيا المعلومات/مكونات الحل (10677).</span><span class="sxs-lookup"><span data-stu-id="8b107-108">To learn more about this feature, complete the steps in the topic, [RCS Import files in XML format with optional attributes](tasks/import-files-xml-format-optional-attributes.md), which is part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process.</span></span> <span data-ttu-id="8b107-109">يمكنك تنزيل دليل المهام هذا وملفات العينة المرتبطة من [مركز تنزيل Microsoft](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="8b107-109">You can download this task guide and associated sample files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>


| <span data-ttu-id="8b107-110">وصف المحتوى</span><span class="sxs-lookup"><span data-stu-id="8b107-110">Content description</span></span>       | <span data-ttu-id="8b107-111">الملف</span><span class="sxs-lookup"><span data-stu-id="8b107-111">File</span></span>                                                         |
|---------------------------|--------------------------------------------------------------|
| <span data-ttu-id="8b107-112">ملف العينة بتنسيق XML</span><span class="sxs-lookup"><span data-stu-id="8b107-112">Sample file in XML format</span></span> | <span data-ttu-id="8b107-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span><span class="sxs-lookup"><span data-stu-id="8b107-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span></span>     |
| <span data-ttu-id="8b107-114">دليل المهام</span><span class="sxs-lookup"><span data-stu-id="8b107-114">Task guide</span></span>                | <span data-ttu-id="8b107-115">استيراد ملفات RCS بتنسيق XML مع سمات اختيارية.axtr</span><span class="sxs-lookup"><span data-stu-id="8b107-115">RCS Import files in XML format with optional attributes.axtr</span></span> |


<span data-ttu-id="8b107-116">تشرح الخطوات التالية كيف يمكن لمستخدم بدور مسؤول النظام أو مطور التقارير الإلكترونية تصميم تكوين تنسيق التقارير الإلكترونية (ER) لاستيراد الملفات التي تحتوي على سمات اختيارية بتنسيق XML.</span><span class="sxs-lookup"><span data-stu-id="8b107-116">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="8b107-117">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء [إنشاء موفر تكوين وتحديده بالحالة نشط](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="8b107-117">To complete these steps, you must first complete the steps in the procedure, [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="8b107-118">قبل البدء، نزِّل الملف IncomingDocumentToLearnHowToHandleOptionalAttributes.xml من مركز تنزيل Microsoft واحفظه محليًا (https://go.microsoft.com/fwlink/?linkid=874684 ).</span><span class="sxs-lookup"><span data-stu-id="8b107-118">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from Microsoft Download Center (https://go.microsoft.com/fwlink/?linkid=874684 ).</span></span>

1. <span data-ttu-id="8b107-119">انتقل إلى **إدارة المؤسسة** > **مساحات العمل‬** > **إعداد التقارير الإلكترونية**‬.</span><span class="sxs-lookup"><span data-stu-id="8b107-119">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span>
2. <span data-ttu-id="8b107-120">تأكد من وجود موفر التكوين للشركة النموذجية "Litware, Inc." ومن وضع علامة عليه كـ **نشط**.</span><span class="sxs-lookup"><span data-stu-id="8b107-120">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="8b107-121">في حالة عدم رؤية موفر التكوين هذا، يجب إكمال الخطوات المذكورة في الموضوع، [إنشاء موفر تكوين وتحديدها بالحالة نشط‬](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="8b107-121">If you don’t see this configuration provider, complete the steps in the topic, [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="8b107-122">انقر فوق **تكوينات إعداد التقارير‬**.</span><span class="sxs-lookup"><span data-stu-id="8b107-122">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="8b107-123">إنشاء تكوين نموذج بيانات جديد</span><span class="sxs-lookup"><span data-stu-id="8b107-123">Create a new data model configuration</span></span>
1. <span data-ttu-id="8b107-124">انقر فوق **إنشاء تكوين** لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="8b107-124">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="8b107-125">في حقل **الاسم**، اكتب "نموذج لاستيراد ملف xml".</span><span class="sxs-lookup"><span data-stu-id="8b107-125">In the **Name** field, type 'Model to import xml file'.</span></span>
3. <span data-ttu-id="8b107-126">وانقر فوق **إنشاء تكوين**.</span><span class="sxs-lookup"><span data-stu-id="8b107-126">Click **Create configuration**.</span></span>
4. <span data-ttu-id="8b107-127">انقر فوق **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="8b107-127">Click **Designer**.</span></span>
5. <span data-ttu-id="8b107-128">انقر فوق **جديد**  لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="8b107-128">Click **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="8b107-129">في حقل **الاسم**، اكتب "الجذر"‬.</span><span class="sxs-lookup"><span data-stu-id="8b107-129">In the **Name** field, type 'Root'.</span></span>
7. <span data-ttu-id="8b107-130">انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="8b107-130">Click **Add**.</span></span>
8. <span data-ttu-id="8b107-131">انقر فوق **جديد**  لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="8b107-131">Click **New** to open the drop dialog.</span></span>
9. <span data-ttu-id="8b107-132">في حقل **الاسم**، اكتب "القائمة"‬.</span><span class="sxs-lookup"><span data-stu-id="8b107-132">In the **Name** field, type 'List'.</span></span>
10. <span data-ttu-id="8b107-133">في حقل **نوع الصنف**، حدد **قائمة سجلات**.</span><span class="sxs-lookup"><span data-stu-id="8b107-133">In the **Item type** field, select **Record list**.</span></span>
11. <span data-ttu-id="8b107-134">انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="8b107-134">Click **Add**.</span></span>
12. <span data-ttu-id="8b107-135">انقر فوق **جديد**  لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="8b107-135">Click **New** to open the drop dialog.</span></span>
13. <span data-ttu-id="8b107-136">في حقل **الاسم**، اكتب "الرمز".</span><span class="sxs-lookup"><span data-stu-id="8b107-136">In the **Name** field, type 'Code'.</span></span>
14. <span data-ttu-id="8b107-137">في الحقل **نوع الصنف**، حدد **سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="8b107-137">In the **Item type** field, select **String**.</span></span>
15. <span data-ttu-id="8b107-138">انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="8b107-138">Click **Add**.</span></span>
16. <span data-ttu-id="8b107-139">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8b107-139">Click **Save**.</span></span>
17. <span data-ttu-id="8b107-140">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8b107-140">Close the page.</span></span>
18. <span data-ttu-id="8b107-141">انقر فوق **تغيير الحالة**.</span><span class="sxs-lookup"><span data-stu-id="8b107-141">Click **Change status**.</span></span>
19. <span data-ttu-id="8b107-142">انقر فوق **إكمال**.</span><span class="sxs-lookup"><span data-stu-id="8b107-142">Click **Complete**.</span></span>
20. <span data-ttu-id="8b107-143">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="8b107-143">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="8b107-144">إنشاء تنسيق لاستيراد البيانات</span><span class="sxs-lookup"><span data-stu-id="8b107-144">Create a format for data import</span></span>
1. <span data-ttu-id="8b107-145">انقر فوق **إنشاء تكوين** لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="8b107-145">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="8b107-146">في الحقل **جديد**، أدخل "التنسيق المستند إلى نموذج البيانات نموذج لاستيراد ملف xml".</span><span class="sxs-lookup"><span data-stu-id="8b107-146">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3. <span data-ttu-id="8b107-147">في حقل **الاسم**، اكتب "تنسيق لاستيراد ملف xml".</span><span class="sxs-lookup"><span data-stu-id="8b107-147">In the **Nam**e field, type 'Format to import xml file'.</span></span> 
4. <span data-ttu-id="8b107-148">حدد **نعم** في الحقل **دعم استيراد البيانات**.</span><span class="sxs-lookup"><span data-stu-id="8b107-148">Select **Yes** in the **Supports data import** field.</span></span>
5. <span data-ttu-id="8b107-149">وانقر فوق **إنشاء تكوين**.</span><span class="sxs-lookup"><span data-stu-id="8b107-149">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="8b107-150">تصميم تنسيق لتحليل الملف الوارد بتنسيق xml</span><span class="sxs-lookup"><span data-stu-id="8b107-150">Design a format to parse incoming file in xml format</span></span>
1. <span data-ttu-id="8b107-151">انقر فوق **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="8b107-151">Click **Designer**.</span></span>
2. <span data-ttu-id="8b107-152">انقر فوق **إضافة جذر** لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="8b107-152">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="8b107-153">في الشجرة، **XML\العنصر**.</span><span class="sxs-lookup"><span data-stu-id="8b107-153">In the tree, select **XML\Element**.</span></span>
4. <span data-ttu-id="8b107-154">في حقل **الاسم**، اكتب "الجذر"‬.</span><span class="sxs-lookup"><span data-stu-id="8b107-154">In the **Name** field, type 'root'.</span></span>
5. <span data-ttu-id="8b107-155">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="8b107-155">Click **OK**.</span></span>
6. <span data-ttu-id="8b107-156">انقر فوق **إضافة** لفتح مربع حوار الإسقاط.</span><span class="sxs-lookup"><span data-stu-id="8b107-156">Click **Add** to open the drop dialog.</span></span>
7. <span data-ttu-id="8b107-157">في الشجرة، **XML\العنصر**.</span><span class="sxs-lookup"><span data-stu-id="8b107-157">In the tree, select **XML\Element**.</span></span>
8. <span data-ttu-id="8b107-158">في حقل **الاسم**، اكتب "المستند".</span><span class="sxs-lookup"><span data-stu-id="8b107-158">In the **Name** field, type 'document'.</span></span>
9. <span data-ttu-id="8b107-159">في حقل **التعدد**، حدد **واحد كثير‬**.</span><span class="sxs-lookup"><span data-stu-id="8b107-159">In the **Multiplicity** field, select **One many**.</span></span>
10. <span data-ttu-id="8b107-160">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="8b107-160">Click **OK**.</span></span>
11. <span data-ttu-id="8b107-161">في الشجرة، حدد **root\document**.</span><span class="sxs-lookup"><span data-stu-id="8b107-161">In the tree, select **root\document**.</span></span>
12. <span data-ttu-id="8b107-162">انقر فوق **إضافة** لفتح مربع حوار الإسقاط.</span><span class="sxs-lookup"><span data-stu-id="8b107-162">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="8b107-163">في الشجرة، حدد **XML\سمة**.</span><span class="sxs-lookup"><span data-stu-id="8b107-163">In the tree, select **XML\Attribute**.</span></span>
14. <span data-ttu-id="8b107-164">في حقل **الاسم**، اكتب "المعرف".</span><span class="sxs-lookup"><span data-stu-id="8b107-164">In the **Name** field, type 'id'.</span></span>
15. <span data-ttu-id="8b107-165">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="8b107-165">Click **OK**.</span></span>
16. <span data-ttu-id="8b107-166">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8b107-166">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="8b107-167">تصميم تعيين تنسيق لحفظ المعلومات التي تم تحليلها لنموذج البيانات</span><span class="sxs-lookup"><span data-stu-id="8b107-167">Design a format mapping to save parsed information to data model</span></span>
1.  <span data-ttu-id="8b107-168">انقر فوق **تعيين تنسيق لنموذج‬**.</span><span class="sxs-lookup"><span data-stu-id="8b107-168">Click **Map format to model**.</span></span>
2.  <span data-ttu-id="8b107-169">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="8b107-169">Click **New**.</span></span>
3.  <span data-ttu-id="8b107-170">في حقل **التعريف**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="8b107-170">In the **Definition** field, enter or select a value.</span></span>
4.  <span data-ttu-id="8b107-171">في حقل **الاسم**، اكتب "تعيين".</span><span class="sxs-lookup"><span data-stu-id="8b107-171">In the **Name** field, type 'Mapping'.</span></span>
5.  <span data-ttu-id="8b107-172">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8b107-172">Click **Save**.</span></span>
6.  <span data-ttu-id="8b107-173">انقر فوق **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="8b107-173">Click **Designer**.</span></span>
7.  <span data-ttu-id="8b107-174">في الشجرة، وسَّع **التنسيق**.</span><span class="sxs-lookup"><span data-stu-id="8b107-174">In the tree, expand **format**.</span></span>
8.  <span data-ttu-id="8b107-175">في الشجرة، وسَّع **format\root: XML Element(root)**.</span><span class="sxs-lookup"><span data-stu-id="8b107-175">In the tree, expand **format\root: XML Element(root)**.</span></span>
9.  <span data-ttu-id="8b107-176">في الشجرة، حدد \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="8b107-176">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="8b107-177">(المستند)\*\*.</span><span class="sxs-lookup"><span data-stu-id="8b107-177">(document)\*\*.</span></span>
10. <span data-ttu-id="8b107-178">انقر فوق **ربط**.</span><span class="sxs-lookup"><span data-stu-id="8b107-178">Click **Bind**.</span></span>
11. <span data-ttu-id="8b107-179">في الشجرة، وسَّع \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="8b107-179">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="8b107-180">(المستند)\*\*.</span><span class="sxs-lookup"><span data-stu-id="8b107-180">(document)\*\*.</span></span>
12. <span data-ttu-id="8b107-181">في الشجرة، حدد \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="8b107-181">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="8b107-182">(المستند)\معرف\*\*.</span><span class="sxs-lookup"><span data-stu-id="8b107-182">(document)\id\*\*.</span></span>
13. <span data-ttu-id="8b107-183">في الشجرة، وسّع **القائمة = format.root.document**.</span><span class="sxs-lookup"><span data-stu-id="8b107-183">In the tree, expand **List = format.root.document**.</span></span>
14. <span data-ttu-id="8b107-184">في الشجرة، حدد **القائمة = format.root.document\Code**.</span><span class="sxs-lookup"><span data-stu-id="8b107-184">In the tree, select **List = format.root.document\Code**.</span></span>
15. <span data-ttu-id="8b107-185">انقر فوق **ربط**.</span><span class="sxs-lookup"><span data-stu-id="8b107-185">Click **Bind**.</span></span>
16. <span data-ttu-id="8b107-186">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8b107-186">Click **Save**.</span></span>
17. <span data-ttu-id="8b107-187">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8b107-187">Close the page.</span></span>

## <a name="run-format-mapping"></a><span data-ttu-id="8b107-188">تشغيل تعيين التنسيق</span><span class="sxs-lookup"><span data-stu-id="8b107-188">Run format mapping</span></span>
1. <span data-ttu-id="8b107-189">انقر فوق **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="8b107-189">Click **Run**.</span></span>
2. <span data-ttu-id="8b107-190">انقر فوق **استعراض** وحدد الملف، **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="8b107-190">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="8b107-191">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="8b107-191">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="8b107-192">لم يتم استيراد الملف المحدد نظرًا لأن تصميم التنسيق يفترض وجود سمة "المعرف" للعنصر "المستند"، ولكن الملف المستورد لا يحتوي علي مثل هذه السمة.</span><span class="sxs-lookup"><span data-stu-id="8b107-192">The selected file has not been imported as the format design assumes the existence of ‘id’ attribute for the ‘document’ element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="8b107-193">عدِّل بنية التنسيق لمعالجة سمة xml كملف اختياري</span><span class="sxs-lookup"><span data-stu-id="8b107-193">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="8b107-194">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8b107-194">Close the page.</span></span>
2. <span data-ttu-id="8b107-195">في الشجرة، وسَّع **root\document**.</span><span class="sxs-lookup"><span data-stu-id="8b107-195">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="8b107-196">في الشجرة، حدد **root\document\id**.</span><span class="sxs-lookup"><span data-stu-id="8b107-196">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="8b107-197">في حقل **‎سلسلة فارغة للسمة المفقودة**، حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="8b107-197">In the **Empty string for missing attribute** field, select **Yes**.</span></span>
5. <span data-ttu-id="8b107-198">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8b107-198">Click **Save**.</span></span>

## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="8b107-199">تشغيل تعيين التنسيق لاختبار التغييرات</span><span class="sxs-lookup"><span data-stu-id="8b107-199">Run format mapping to test changes</span></span>
1. <span data-ttu-id="8b107-200">انقر فوق **تعيين تنسيق لنموذج‬**.</span><span class="sxs-lookup"><span data-stu-id="8b107-200">Click **Map format to model**.</span></span>
2. <span data-ttu-id="8b107-201">انقر فوق **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="8b107-201">Click **Run**.</span></span>
3. <span data-ttu-id="8b107-202">انقر فوق **استعراض** وحدد الملف، **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="8b107-202">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
4. <span data-ttu-id="8b107-203">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="8b107-203">Click **OK**.</span></span>
5. <span data-ttu-id="8b107-204">راجع الملف المنشأ.</span><span class="sxs-lookup"><span data-stu-id="8b107-204">Review the generated file.</span></span> <span data-ttu-id="8b107-205">لاحظ أنه تم استيراد نفس الملف نظرًا لمراعاة تصميم التنسيق لسمة "المعرف" لعنصر "المستند" باعتبارها اختيارية.</span><span class="sxs-lookup"><span data-stu-id="8b107-205">Note that same file has been imported as the format design now consider the ‘id’ attribute for the ‘document’ element as optional.</span></span>
