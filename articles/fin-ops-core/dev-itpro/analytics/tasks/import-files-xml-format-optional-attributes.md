---
title: استيراد ملفات (RCS) بتنسيق XML مع سمات اختيارية
description: يوفر هذا الموضوع معلومات حول كيف يمكن لمستخدم تصميم تكوين تنسيق ER لاستيراد الملفات بتنسيق XML والذي يحتوي على سمات اختيارية.
author: NickSelin
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d1d4c8c1d81faa60193d2339fd6541e752c2e2f9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684125"
---
# <a name="rcs-import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="bc199-103">استيراد ملفات (RCS) بتنسيق XML مع سمات اختيارية</span><span class="sxs-lookup"><span data-stu-id="bc199-103">(RCS) Import files in XML format with optional attributes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bc199-104">تشرح الخطوات التالية كيف يمكن لمستخدم بدور مسؤول النظام أو مطور التقارير الإلكترونية تصميم تكوين تنسيق التقارير الإلكترونية (ER) لاستيراد الملفات التي تحتوي على سمات اختيارية بتنسيق XML.</span><span class="sxs-lookup"><span data-stu-id="bc199-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="bc199-105">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "إنشاء موفر تكوين ووضع علامة عليه على أنه نشط".</span><span class="sxs-lookup"><span data-stu-id="bc199-105">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span> <span data-ttu-id="bc199-106">قبل البدء، قم بتنزيل وحفظ الملف IncomingDocumentToLearnHowToHandleOptionalAttributes.xml محليًا من [مركز تنزيل Microsoft](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="bc199-106">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

1.    <span data-ttu-id="bc199-107">انتقل إلى **كل مساحات العمل‬** > **إعداد التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="bc199-107">Go to **All workspaces** > **Electronic reporting**.</span></span>
2.    <span data-ttu-id="bc199-108">تأكد من وجود موفر التكوين للشركة النموذجية "Litware, Inc." ومن وضع علامة عليه كـ **نشط**.</span><span class="sxs-lookup"><span data-stu-id="bc199-108">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="bc199-109">في حالة عدم رؤية موفر التكوين هذا، أكمل الخطوات المذكورة في الإجراء [إنشاء موفرات تكوين وتحديدها بالحالة نشط‬](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="bc199-109">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3.    <span data-ttu-id="bc199-110">انقر فوق **تكوينات إعداد التقارير‬**.</span><span class="sxs-lookup"><span data-stu-id="bc199-110">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="bc199-111">إنشاء تكوين نموذج بيانات جديد</span><span class="sxs-lookup"><span data-stu-id="bc199-111">Create a new data model configuration</span></span>
1.    <span data-ttu-id="bc199-112">انقر فوق **إنشاء تكوين** لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="bc199-112">Click **Create configuration** to open the drop dialog.</span></span>
2.    <span data-ttu-id="bc199-113">في حقل **الاسم**، اكتب "نموذج لاستيراد ملف xml".</span><span class="sxs-lookup"><span data-stu-id="bc199-113">In the **Name** field, type 'Model to import xml file'.</span></span>
3.    <span data-ttu-id="bc199-114">وانقر فوق **إنشاء تكوين**.</span><span class="sxs-lookup"><span data-stu-id="bc199-114">Click **Create configuration**.</span></span>
4.    <span data-ttu-id="bc199-115">انقر فوق **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="bc199-115">Click **Designer**.</span></span>
5.    <span data-ttu-id="bc199-116">انقر فوق **جديد**  لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="bc199-116">Click **New** to open the drop dialog.</span></span>
6.    <span data-ttu-id="bc199-117">في حقل **الاسم**، اكتب "الجذر"‬.</span><span class="sxs-lookup"><span data-stu-id="bc199-117">In the **Name** field, type 'Root'.</span></span>
7.    <span data-ttu-id="bc199-118">انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="bc199-118">Click **Add**.</span></span>
8.    <span data-ttu-id="bc199-119">انقر فوق **جديد**  لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="bc199-119">Click **New** to open the drop dialog.</span></span>
9.    <span data-ttu-id="bc199-120">في حقل **الاسم**، اكتب "القائمة"‬.</span><span class="sxs-lookup"><span data-stu-id="bc199-120">In the **Name** field, type 'List'.</span></span>
10.    <span data-ttu-id="bc199-121">في حقل **نوع الصنف**، حدد **قائمة سجلات**.</span><span class="sxs-lookup"><span data-stu-id="bc199-121">In the **Item type** field, select **Record list**.</span></span>
11.    <span data-ttu-id="bc199-122">انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="bc199-122">Click **Add**.</span></span>
12.    <span data-ttu-id="bc199-123">انقر فوق **جديد**  لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="bc199-123">Click **New** to open the drop dialog.</span></span>
13.    <span data-ttu-id="bc199-124">في حقل **الاسم**، اكتب "الرمز".</span><span class="sxs-lookup"><span data-stu-id="bc199-124">In the **Name** field, type 'Code'.</span></span>
14.    <span data-ttu-id="bc199-125">في الحقل **نوع الصنف**، حدد **سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="bc199-125">In the **Item type** field, select **String**.</span></span>
15.    <span data-ttu-id="bc199-126">انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="bc199-126">Click **Add**.</span></span>
16.    <span data-ttu-id="bc199-127">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="bc199-127">Click **Save**.</span></span>
17.    <span data-ttu-id="bc199-128">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="bc199-128">Close the page.</span></span>
18.    <span data-ttu-id="bc199-129">انقر فوق **تغيير الحالة**.</span><span class="sxs-lookup"><span data-stu-id="bc199-129">Click **Change status**.</span></span>
19.    <span data-ttu-id="bc199-130">انقر فوق **إكمال**.</span><span class="sxs-lookup"><span data-stu-id="bc199-130">Click **Complete**.</span></span>
20.    <span data-ttu-id="bc199-131">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="bc199-131">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="bc199-132">إنشاء تنسيق لاستيراد البيانات</span><span class="sxs-lookup"><span data-stu-id="bc199-132">Create a format for data import</span></span>
1.    <span data-ttu-id="bc199-133">انقر فوق **إنشاء تكوين** لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="bc199-133">Click **Create configuration** to open the drop dialog.</span></span>
2.    <span data-ttu-id="bc199-134">في الحقل **جديد**، أدخل "التنسيق المستند إلى نموذج البيانات نموذج لاستيراد ملف xml".</span><span class="sxs-lookup"><span data-stu-id="bc199-134">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3.    <span data-ttu-id="bc199-135">في حقل **الاسم** ، اكتب "تنسيق لاستيراد ملف xml".</span><span class="sxs-lookup"><span data-stu-id="bc199-135">In the **Name** field, type 'Format to import xml file'.</span></span>
4.    <span data-ttu-id="bc199-136">حدد **نعم** في الحقل **دعم استيراد البيانات**.</span><span class="sxs-lookup"><span data-stu-id="bc199-136">Select **Yes** in the **Supports data import** field.</span></span>
5.    <span data-ttu-id="bc199-137">وانقر فوق **إنشاء تكوين**.</span><span class="sxs-lookup"><span data-stu-id="bc199-137">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="bc199-138">تصميم تنسيق لتحليل الملف الوارد بتنسيق xml</span><span class="sxs-lookup"><span data-stu-id="bc199-138">Design a format to parse incoming file in xml format</span></span>
1.    <span data-ttu-id="bc199-139">انقر فوق **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="bc199-139">Click **Designer**.</span></span>
2.    <span data-ttu-id="bc199-140">انقر فوق **إضافة جذر** لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="bc199-140">Click **Add root** to open the drop dialog.</span></span>
3.    <span data-ttu-id="bc199-141">في الشجرة، **XML\العنصر**.</span><span class="sxs-lookup"><span data-stu-id="bc199-141">In the tree, select **XML\Element**.</span></span>
4.    <span data-ttu-id="bc199-142">في حقل **الاسم**، اكتب "الجذر"‬.</span><span class="sxs-lookup"><span data-stu-id="bc199-142">In the **Name** field, type 'root'.</span></span>
5.    <span data-ttu-id="bc199-143">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="bc199-143">Click **OK**.</span></span>
6.    <span data-ttu-id="bc199-144">انقر فوق **إضافة** لفتح مربع حوار الإسقاط.</span><span class="sxs-lookup"><span data-stu-id="bc199-144">Click **Add** to open the drop dialog.</span></span>
7.    <span data-ttu-id="bc199-145">في الشجرة، **XML\العنصر**.</span><span class="sxs-lookup"><span data-stu-id="bc199-145">In the tree, select **XML\Element**.</span></span>
8.    <span data-ttu-id="bc199-146">في حقل **الاسم**، اكتب "المستند".</span><span class="sxs-lookup"><span data-stu-id="bc199-146">In the **Name** field, type 'document'.</span></span>
9.    <span data-ttu-id="bc199-147">في حقل **التعدد**، حدد **واحد كثير‬**.</span><span class="sxs-lookup"><span data-stu-id="bc199-147">In the **Multiplicity** field, select **One many**.</span></span>
10.    <span data-ttu-id="bc199-148">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="bc199-148">Click **OK**.</span></span>
11.    <span data-ttu-id="bc199-149">في الشجرة، حدد **root\document**.</span><span class="sxs-lookup"><span data-stu-id="bc199-149">In the tree, select **root\document**.</span></span>
12.    <span data-ttu-id="bc199-150">انقر فوق **إضافة** لفتح مربع حوار الإسقاط.</span><span class="sxs-lookup"><span data-stu-id="bc199-150">Click **Add** to open the drop dialog.</span></span>
13.    <span data-ttu-id="bc199-151">في الشجرة، حدد **XML\سمة**.</span><span class="sxs-lookup"><span data-stu-id="bc199-151">In the tree, select **XML\Attribute**.</span></span>
14.    <span data-ttu-id="bc199-152">في حقل **الاسم**، اكتب "المعرف".</span><span class="sxs-lookup"><span data-stu-id="bc199-152">In the **Name** field, type 'ID'.</span></span>
15.    <span data-ttu-id="bc199-153">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="bc199-153">Click **OK**.</span></span>
16.    <span data-ttu-id="bc199-154">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="bc199-154">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="bc199-155">تصميم تعيين تنسيق لحفظ المعلومات التي تم تحليلها لنموذج البيانات</span><span class="sxs-lookup"><span data-stu-id="bc199-155">Design a format mapping to save parsed information to data model</span></span>
1. <span data-ttu-id="bc199-156">انقر فوق **تعيين تنسيق لنموذج‬**.</span><span class="sxs-lookup"><span data-stu-id="bc199-156">Click **Map format to model**.</span></span>
2. <span data-ttu-id="bc199-157">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="bc199-157">Click **New**.</span></span>
3. <span data-ttu-id="bc199-158">في حقل **التعريف**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="bc199-158">In the **Definition** field, enter or select a value.</span></span>
4. <span data-ttu-id="bc199-159">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="bc199-159">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="bc199-160">في حقل **الاسم**، اكتب "تعيين".</span><span class="sxs-lookup"><span data-stu-id="bc199-160">In the **Name** field, type 'Mapping'.</span></span>
6. <span data-ttu-id="bc199-161">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="bc199-161">Click **Save**.</span></span>
7. <span data-ttu-id="bc199-162">انقر فوق **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="bc199-162">Click **Designer**.</span></span>
8. <span data-ttu-id="bc199-163">في الشجرة، وسَّع **التنسيق**.</span><span class="sxs-lookup"><span data-stu-id="bc199-163">In the tree, expand **format**.</span></span>
9. <span data-ttu-id="bc199-164">في الشجرة، وسَّع **format\root: XML Element(root)**.</span><span class="sxs-lookup"><span data-stu-id="bc199-164">In the tree, expand **format\root: XML Element(root)**.</span></span>
10.    <span data-ttu-id="bc199-165">في الشجرة، حدد \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="bc199-165">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="bc199-166">(المستند)\*\*.</span><span class="sxs-lookup"><span data-stu-id="bc199-166">(document)\*\*.</span></span>
11.    <span data-ttu-id="bc199-167">انقر فوق **ربط**.</span><span class="sxs-lookup"><span data-stu-id="bc199-167">Click **Bind**.</span></span>
12.    <span data-ttu-id="bc199-168">في الشجرة، وسَّع \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="bc199-168">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="bc199-169">(المستند)\*\*.</span><span class="sxs-lookup"><span data-stu-id="bc199-169">(document)\*\*.</span></span>
13.    <span data-ttu-id="bc199-170">في الشجرة، حدد \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="bc199-170">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="bc199-171">(المستند)\معرف\*\*.</span><span class="sxs-lookup"><span data-stu-id="bc199-171">(document)\id\*\*.</span></span>
14.    <span data-ttu-id="bc199-172">في الشجرة، وسّع **القائمة = format.root.document**.</span><span class="sxs-lookup"><span data-stu-id="bc199-172">In the tree, expand **List = format.root.document**.</span></span>
15.    <span data-ttu-id="bc199-173">في الشجرة، حدد **القائمة = format.root.document\Code**.</span><span class="sxs-lookup"><span data-stu-id="bc199-173">In the tree, select **List = format.root.document\Code**.</span></span>
16.    <span data-ttu-id="bc199-174">انقر فوق **ربط**.</span><span class="sxs-lookup"><span data-stu-id="bc199-174">Click **Bind**.</span></span>
17.    <span data-ttu-id="bc199-175">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="bc199-175">Click **Save**.</span></span>
18.    <span data-ttu-id="bc199-176">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="bc199-176">Close the page.</span></span>
 
## <a name="run-format-mapping"></a><span data-ttu-id="bc199-177">تشغيل تعيين التنسيق</span><span class="sxs-lookup"><span data-stu-id="bc199-177">Run format mapping</span></span>
1. <span data-ttu-id="bc199-178">انقر فوق **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="bc199-178">Click **Run**.</span></span>
2. <span data-ttu-id="bc199-179">انقر فوق **استعراض** وحدد **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="bc199-179">Click **Browse** and select **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="bc199-180">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="bc199-180">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="bc199-181">لم يتم استيراد الملف المحدد لأن تصميم التنسيق يفترض وجود سمة "المعرف" للعنصر "المستند"، ولكن الملف المستورد لا يحتوي على مثل هذه السمة.</span><span class="sxs-lookup"><span data-stu-id="bc199-181">The selected file has not been imported as the format design assumes the existence of 'id' attribute for the 'document' element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="bc199-182">عدِّل بنية التنسيق لمعالجة سمة xml كملف اختياري</span><span class="sxs-lookup"><span data-stu-id="bc199-182">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="bc199-183">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="bc199-183">Close the page.</span></span>
2. <span data-ttu-id="bc199-184">في الشجرة، وسَّع **root\document**.</span><span class="sxs-lookup"><span data-stu-id="bc199-184">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="bc199-185">في الشجرة، حدد **root\document\id**.</span><span class="sxs-lookup"><span data-stu-id="bc199-185">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="bc199-186">حدد **نعم** في حقل **سلسلة فارغة للسمة المفقودة**.</span><span class="sxs-lookup"><span data-stu-id="bc199-186">Select **Yes** in the **Empty string for missing attribute** field.</span></span>
5. <span data-ttu-id="bc199-187">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="bc199-187">Click **Save**.</span></span>
 
## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="bc199-188">تشغيل تعيين التنسيق لاختبار التغييرات</span><span class="sxs-lookup"><span data-stu-id="bc199-188">Run format mapping to test changes</span></span>
1. <span data-ttu-id="bc199-189">انقر فوق **تعيين تنسيق لنموذج‬**.</span><span class="sxs-lookup"><span data-stu-id="bc199-189">Click **Map format to model**.</span></span>
2. <span data-ttu-id="bc199-190">انقر فوق **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="bc199-190">Click **Run**.</span></span>
3. <span data-ttu-id="bc199-191">انقر فوق **استعراض** وحدد ملف **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="bc199-191">Click **Browse** and select the **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** file.</span></span>
4. <span data-ttu-id="bc199-192">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="bc199-192">Click **OK**.</span></span>
5. <span data-ttu-id="bc199-193">راجع الملف المنشأ.</span><span class="sxs-lookup"><span data-stu-id="bc199-193">Review the generated file.</span></span> 

> [!NOTE]
> <span data-ttu-id="bc199-194">تم استيراد نفس الملف لأن تصميم التنسيق يأخذ بعين الاعتبار سمة "المعرف" لعنصر "المستند" باعتبارها اختيارية.</span><span class="sxs-lookup"><span data-stu-id="bc199-194">The same file has been imported as the format design now consider the 'id' attribute for the 'document' element as optional.</span></span>
