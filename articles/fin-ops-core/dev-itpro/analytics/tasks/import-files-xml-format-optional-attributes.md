---
title: استيراد ملفات (RCS) بتنسيق XML مع سمات اختيارية
description: يوفر هذا الموضوع معلومات حول كيف يمكن لمستخدم تصميم تكوين تنسيق ER لاستيراد الملفات بتنسيق XML والذي يحتوي على سمات اختيارية.
author: NickSelin
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 25ced72bc1bb1b18996c8bab986270fde0557ed3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744857"
---
# <a name="rcs-import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="c16bd-103">استيراد ملفات (RCS) بتنسيق XML مع سمات اختيارية</span><span class="sxs-lookup"><span data-stu-id="c16bd-103">(RCS) Import files in XML format with optional attributes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c16bd-104">تشرح الخطوات التالية كيف يمكن لمستخدم بدور مسؤول النظام أو مطور التقارير الإلكترونية تصميم تكوين تنسيق التقارير الإلكترونية (ER) لاستيراد الملفات التي تحتوي على سمات اختيارية بتنسيق XML.</span><span class="sxs-lookup"><span data-stu-id="c16bd-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="c16bd-105">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "إنشاء موفر تكوين ووضع علامة عليه على أنه نشط".</span><span class="sxs-lookup"><span data-stu-id="c16bd-105">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span> <span data-ttu-id="c16bd-106">قبل البدء، قم بتنزيل وحفظ الملف IncomingDocumentToLearnHowToHandleOptionalAttributes.xml محليًا من [مركز تنزيل Microsoft](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="c16bd-106">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

1.    <span data-ttu-id="c16bd-107">انتقل إلى **كل مساحات العمل‬** > **إعداد التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-107">Go to **All workspaces** > **Electronic reporting**.</span></span>
2.    <span data-ttu-id="c16bd-108">تأكد من وجود موفر التكوين للشركة النموذجية "Litware, Inc." ومن وضع علامة عليه كـ **نشط**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-108">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="c16bd-109">في حالة عدم رؤية موفر التكوين هذا، أكمل الخطوات المذكورة في الإجراء [إنشاء موفرات تكوين وتحديدها بالحالة نشط‬](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="c16bd-109">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3.    <span data-ttu-id="c16bd-110">انقر فوق **تكوينات إعداد التقارير‬**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-110">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="c16bd-111">إنشاء تكوين نموذج بيانات جديد</span><span class="sxs-lookup"><span data-stu-id="c16bd-111">Create a new data model configuration</span></span>
1.    <span data-ttu-id="c16bd-112">انقر فوق **إنشاء تكوين** لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="c16bd-112">Click **Create configuration** to open the drop dialog.</span></span>
2.    <span data-ttu-id="c16bd-113">في حقل **الاسم**، اكتب "نموذج لاستيراد ملف xml".</span><span class="sxs-lookup"><span data-stu-id="c16bd-113">In the **Name** field, type 'Model to import xml file'.</span></span>
3.    <span data-ttu-id="c16bd-114">وانقر فوق **إنشاء تكوين**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-114">Click **Create configuration**.</span></span>
4.    <span data-ttu-id="c16bd-115">انقر فوق **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-115">Click **Designer**.</span></span>
5.    <span data-ttu-id="c16bd-116">انقر فوق **جديد**  لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="c16bd-116">Click **New** to open the drop dialog.</span></span>
6.    <span data-ttu-id="c16bd-117">في حقل **الاسم**، اكتب "الجذر"‬.</span><span class="sxs-lookup"><span data-stu-id="c16bd-117">In the **Name** field, type 'Root'.</span></span>
7.    <span data-ttu-id="c16bd-118">انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-118">Click **Add**.</span></span>
8.    <span data-ttu-id="c16bd-119">انقر فوق **جديد**  لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="c16bd-119">Click **New** to open the drop dialog.</span></span>
9.    <span data-ttu-id="c16bd-120">في حقل **الاسم**، اكتب "القائمة"‬.</span><span class="sxs-lookup"><span data-stu-id="c16bd-120">In the **Name** field, type 'List'.</span></span>
10.    <span data-ttu-id="c16bd-121">في حقل **نوع الصنف**، حدد **قائمة سجلات**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-121">In the **Item type** field, select **Record list**.</span></span>
11.    <span data-ttu-id="c16bd-122">انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-122">Click **Add**.</span></span>
12.    <span data-ttu-id="c16bd-123">انقر فوق **جديد**  لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="c16bd-123">Click **New** to open the drop dialog.</span></span>
13.    <span data-ttu-id="c16bd-124">في حقل **الاسم**، اكتب "الرمز".</span><span class="sxs-lookup"><span data-stu-id="c16bd-124">In the **Name** field, type 'Code'.</span></span>
14.    <span data-ttu-id="c16bd-125">في الحقل **نوع الصنف**، حدد **سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-125">In the **Item type** field, select **String**.</span></span>
15.    <span data-ttu-id="c16bd-126">انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-126">Click **Add**.</span></span>
16.    <span data-ttu-id="c16bd-127">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-127">Click **Save**.</span></span>
17.    <span data-ttu-id="c16bd-128">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c16bd-128">Close the page.</span></span>
18.    <span data-ttu-id="c16bd-129">انقر فوق **تغيير الحالة**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-129">Click **Change status**.</span></span>
19.    <span data-ttu-id="c16bd-130">انقر فوق **إكمال**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-130">Click **Complete**.</span></span>
20.    <span data-ttu-id="c16bd-131">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-131">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="c16bd-132">إنشاء تنسيق لاستيراد البيانات</span><span class="sxs-lookup"><span data-stu-id="c16bd-132">Create a format for data import</span></span>
1.    <span data-ttu-id="c16bd-133">انقر فوق **إنشاء تكوين** لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="c16bd-133">Click **Create configuration** to open the drop dialog.</span></span>
2.    <span data-ttu-id="c16bd-134">في الحقل **جديد**، أدخل "التنسيق المستند إلى نموذج البيانات نموذج لاستيراد ملف xml".</span><span class="sxs-lookup"><span data-stu-id="c16bd-134">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3.    <span data-ttu-id="c16bd-135">في حقل **الاسم** ، اكتب "تنسيق لاستيراد ملف xml".</span><span class="sxs-lookup"><span data-stu-id="c16bd-135">In the **Name** field, type 'Format to import xml file'.</span></span>
4.    <span data-ttu-id="c16bd-136">حدد **نعم** في الحقل **دعم استيراد البيانات**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-136">Select **Yes** in the **Supports data import** field.</span></span>
5.    <span data-ttu-id="c16bd-137">وانقر فوق **إنشاء تكوين**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-137">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="c16bd-138">تصميم تنسيق لتحليل الملف الوارد بتنسيق xml</span><span class="sxs-lookup"><span data-stu-id="c16bd-138">Design a format to parse incoming file in xml format</span></span>
1.    <span data-ttu-id="c16bd-139">انقر فوق **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-139">Click **Designer**.</span></span>
2.    <span data-ttu-id="c16bd-140">انقر فوق **إضافة جذر** لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="c16bd-140">Click **Add root** to open the drop dialog.</span></span>
3.    <span data-ttu-id="c16bd-141">في الشجرة، **XML\العنصر**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-141">In the tree, select **XML\Element**.</span></span>
4.    <span data-ttu-id="c16bd-142">في حقل **الاسم**، اكتب "الجذر"‬.</span><span class="sxs-lookup"><span data-stu-id="c16bd-142">In the **Name** field, type 'root'.</span></span>
5.    <span data-ttu-id="c16bd-143">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-143">Click **OK**.</span></span>
6.    <span data-ttu-id="c16bd-144">انقر فوق **إضافة** لفتح مربع حوار الإسقاط.</span><span class="sxs-lookup"><span data-stu-id="c16bd-144">Click **Add** to open the drop dialog.</span></span>
7.    <span data-ttu-id="c16bd-145">في الشجرة، **XML\العنصر**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-145">In the tree, select **XML\Element**.</span></span>
8.    <span data-ttu-id="c16bd-146">في حقل **الاسم**، اكتب "المستند".</span><span class="sxs-lookup"><span data-stu-id="c16bd-146">In the **Name** field, type 'document'.</span></span>
9.    <span data-ttu-id="c16bd-147">في حقل **التعدد**، حدد **واحد كثير‬**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-147">In the **Multiplicity** field, select **One many**.</span></span>
10.    <span data-ttu-id="c16bd-148">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-148">Click **OK**.</span></span>
11.    <span data-ttu-id="c16bd-149">في الشجرة، حدد **root\document**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-149">In the tree, select **root\document**.</span></span>
12.    <span data-ttu-id="c16bd-150">انقر فوق **إضافة** لفتح مربع حوار الإسقاط.</span><span class="sxs-lookup"><span data-stu-id="c16bd-150">Click **Add** to open the drop dialog.</span></span>
13.    <span data-ttu-id="c16bd-151">في الشجرة، حدد **XML\سمة**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-151">In the tree, select **XML\Attribute**.</span></span>
14.    <span data-ttu-id="c16bd-152">في حقل **الاسم**، اكتب "المعرف".</span><span class="sxs-lookup"><span data-stu-id="c16bd-152">In the **Name** field, type 'ID'.</span></span>
15.    <span data-ttu-id="c16bd-153">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-153">Click **OK**.</span></span>
16.    <span data-ttu-id="c16bd-154">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-154">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="c16bd-155">تصميم تعيين تنسيق لحفظ المعلومات التي تم تحليلها لنموذج البيانات</span><span class="sxs-lookup"><span data-stu-id="c16bd-155">Design a format mapping to save parsed information to data model</span></span>
1. <span data-ttu-id="c16bd-156">انقر فوق **تعيين تنسيق لنموذج‬**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-156">Click **Map format to model**.</span></span>
2. <span data-ttu-id="c16bd-157">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-157">Click **New**.</span></span>
3. <span data-ttu-id="c16bd-158">في حقل **التعريف**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c16bd-158">In the **Definition** field, enter or select a value.</span></span>
4. <span data-ttu-id="c16bd-159">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c16bd-159">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="c16bd-160">في حقل **الاسم**، اكتب "تعيين".</span><span class="sxs-lookup"><span data-stu-id="c16bd-160">In the **Name** field, type 'Mapping'.</span></span>
6. <span data-ttu-id="c16bd-161">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-161">Click **Save**.</span></span>
7. <span data-ttu-id="c16bd-162">انقر فوق **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-162">Click **Designer**.</span></span>
8. <span data-ttu-id="c16bd-163">في الشجرة، وسَّع **التنسيق**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-163">In the tree, expand **format**.</span></span>
9. <span data-ttu-id="c16bd-164">في الشجرة، وسَّع **format\root: XML Element(root)**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-164">In the tree, expand **format\root: XML Element(root)**.</span></span>
10.    <span data-ttu-id="c16bd-165">في الشجرة، حدد \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="c16bd-165">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="c16bd-166">(المستند)\*\*.</span><span class="sxs-lookup"><span data-stu-id="c16bd-166">(document)\*\*.</span></span>
11.    <span data-ttu-id="c16bd-167">انقر فوق **ربط**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-167">Click **Bind**.</span></span>
12.    <span data-ttu-id="c16bd-168">في الشجرة، وسَّع \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="c16bd-168">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="c16bd-169">(المستند)\*\*.</span><span class="sxs-lookup"><span data-stu-id="c16bd-169">(document)\*\*.</span></span>
13.    <span data-ttu-id="c16bd-170">في الشجرة، حدد \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="c16bd-170">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="c16bd-171">(المستند)\معرف\*\*.</span><span class="sxs-lookup"><span data-stu-id="c16bd-171">(document)\id\*\*.</span></span>
14.    <span data-ttu-id="c16bd-172">في الشجرة، وسّع **القائمة = format.root.document**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-172">In the tree, expand **List = format.root.document**.</span></span>
15.    <span data-ttu-id="c16bd-173">في الشجرة، حدد **القائمة = format.root.document\Code**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-173">In the tree, select **List = format.root.document\Code**.</span></span>
16.    <span data-ttu-id="c16bd-174">انقر فوق **ربط**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-174">Click **Bind**.</span></span>
17.    <span data-ttu-id="c16bd-175">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-175">Click **Save**.</span></span>
18.    <span data-ttu-id="c16bd-176">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c16bd-176">Close the page.</span></span>
 
## <a name="run-format-mapping"></a><span data-ttu-id="c16bd-177">تشغيل تعيين التنسيق</span><span class="sxs-lookup"><span data-stu-id="c16bd-177">Run format mapping</span></span>
1. <span data-ttu-id="c16bd-178">انقر فوق **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-178">Click **Run**.</span></span>
2. <span data-ttu-id="c16bd-179">انقر فوق **استعراض** وحدد **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-179">Click **Browse** and select **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="c16bd-180">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-180">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="c16bd-181">لم يتم استيراد الملف المحدد لأن تصميم التنسيق يفترض وجود سمة "المعرف" للعنصر "المستند"، ولكن الملف المستورد لا يحتوي على مثل هذه السمة.</span><span class="sxs-lookup"><span data-stu-id="c16bd-181">The selected file has not been imported as the format design assumes the existence of 'id' attribute for the 'document' element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="c16bd-182">عدِّل بنية التنسيق لمعالجة سمة xml كملف اختياري</span><span class="sxs-lookup"><span data-stu-id="c16bd-182">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="c16bd-183">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c16bd-183">Close the page.</span></span>
2. <span data-ttu-id="c16bd-184">في الشجرة، وسَّع **root\document**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-184">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="c16bd-185">في الشجرة، حدد **root\document\id**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-185">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="c16bd-186">حدد **نعم** في حقل **سلسلة فارغة للسمة المفقودة**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-186">Select **Yes** in the **Empty string for missing attribute** field.</span></span>
5. <span data-ttu-id="c16bd-187">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-187">Click **Save**.</span></span>
 
## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="c16bd-188">تشغيل تعيين التنسيق لاختبار التغييرات</span><span class="sxs-lookup"><span data-stu-id="c16bd-188">Run format mapping to test changes</span></span>
1. <span data-ttu-id="c16bd-189">انقر فوق **تعيين تنسيق لنموذج‬**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-189">Click **Map format to model**.</span></span>
2. <span data-ttu-id="c16bd-190">انقر فوق **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-190">Click **Run**.</span></span>
3. <span data-ttu-id="c16bd-191">انقر فوق **استعراض** وحدد ملف **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-191">Click **Browse** and select the **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** file.</span></span>
4. <span data-ttu-id="c16bd-192">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c16bd-192">Click **OK**.</span></span>
5. <span data-ttu-id="c16bd-193">راجع الملف المنشأ.</span><span class="sxs-lookup"><span data-stu-id="c16bd-193">Review the generated file.</span></span> 

> [!NOTE]
> <span data-ttu-id="c16bd-194">تم استيراد نفس الملف لأن تصميم التنسيق يأخذ بعين الاعتبار سمة "المعرف" لعنصر "المستند" باعتبارها اختيارية.</span><span class="sxs-lookup"><span data-stu-id="c16bd-194">The same file has been imported as the format design now consider the 'id' attribute for the 'document' element as optional.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]