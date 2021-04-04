---
title: تحديث بنية قالب مستند الأعمال
description: يشرح هذا الموضوع كيفيه تحديث بنيه قالب مستند العمل باستخدام ميزه أداره مستندات العمل.
author: NickSelin
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-12-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 09813115544701ea3fffb6be06114bcdd63c0ba0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570438"
---
# <a name="update-the-structure-of-a-business-document-template"></a><span data-ttu-id="7619e-103">تحديث بنية قالب مستند الأعمال</span><span class="sxs-lookup"><span data-stu-id="7619e-103">Update the structure of a business document template</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7619e-104">في جزء **بنية القالب** الخاص بمحرر قالب [إدارة مستندات الأعمال](er-business-document-management.md)، يمكنك تعديل قالب مستند أعمال عن طريق [إضافة حقول جديدة](er-bdm-add-field-to-excel-template.md) إلى قالب في Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="7619e-104">In the **Template structure** pane of the [Business document management](er-business-document-management.md) template editor, you can modify a business document template by [adding new fields](er-bdm-add-field-to-excel-template.md) to a template in Microsoft Excel.</span></span> <span data-ttu-id="7619e-105">ويتم بعد ذلك تحديث بنية القالب تلقائيًا في Dynamics 365 Finance، بحيث يعكس التغييرات التي أجريتها في جزء **بنية القالب**.</span><span class="sxs-lookup"><span data-stu-id="7619e-105">The structure of the template is then automatically updated in Dynamics 365 Finance, so that it reflects the changes that you made in the **Template structure** pane.</span></span>

<span data-ttu-id="7619e-106">يمكنك أيضًا تعديل قالب باستخدام وظيفة Office 365 عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="7619e-106">You can also modify a template by using Office 365 online functionality.</span></span> <span data-ttu-id="7619e-107">علي سبيل المثال، يمكنك أضافه عنصر مسمي جديد، مثل صوره أو شكل، إلى ورقه العمل القابلة للتحرير.</span><span class="sxs-lookup"><span data-stu-id="7619e-107">For example, you can add a new named item, such as a picture or shape, to the editable worksheet.</span></span> <span data-ttu-id="7619e-108">في هذه الحالة، لا يتم تحديث بنيه القالب تلقائيا في التمويل، ولا يظهر العنصر الذي قمت بإضافته في جزء **بنية القالب**.</span><span class="sxs-lookup"><span data-stu-id="7619e-108">In this case, the structure of the template isn't automatically updated in Finance, and the item that you added doesn't appear in the **Template structure** pane.</span></span> <span data-ttu-id="7619e-109">قم بتحديث بنيه القالب يدويا في المالية من خلال تحديد **تحديث البنية** في صفحة محرر القالب.</span><span class="sxs-lookup"><span data-stu-id="7619e-109">Manually update the template structure in Finance by selecting **Update structure** on the template editor page.</span></span>

<span data-ttu-id="7619e-110">للاطلاع على مزيد من المعلومات حول الميزة، أكمل المثال التالي.</span><span class="sxs-lookup"><span data-stu-id="7619e-110">For more information about this feature, complete the following example.</span></span>

## <a name="example-update-the-structure-of-a-business-document-template"></a><span data-ttu-id="7619e-111">مثال: تحديث بنيه قالب مستند الأعمال</span><span class="sxs-lookup"><span data-stu-id="7619e-111">Example: Update the structure of a business document template</span></span>

<span data-ttu-id="7619e-112">يوضح هذا المثال كيفيه قيام مسؤول النظام بتحديث بنيه قالب مستند العمل في التمويل بعد تعديل القالب في Office Online.</span><span class="sxs-lookup"><span data-stu-id="7619e-112">This example shows how a system administrator can update the structure of a business document template in Finance after the template is modified in Office Online.</span></span> <span data-ttu-id="7619e-113">توضح الأقسام التالية الخطوات المتضمنة.</span><span class="sxs-lookup"><span data-stu-id="7619e-113">The following sections explain the steps that are involved.</span></span>

### <a name="prepare-a-business-document-template-for-editing"></a><span data-ttu-id="7619e-114">إعداد قالب مستند عمل للتحرير</span><span class="sxs-lookup"><span data-stu-id="7619e-114">Prepare a business document template for editing</span></span>

<span data-ttu-id="7619e-115">أكمل الإجراءات التالية في [نظرة عامة على إدارة مستندات الأعمال](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="7619e-115">Complete the following procedures in [Business document management overview](er-business-document-management.md).</span></span>

1. [<span data-ttu-id="7619e-116">تكوين معلمات التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="7619e-116">Configure ER parameters</span></span>](er-business-document-management.md#configure-er-parameters)
2. [<span data-ttu-id="7619e-117">استيراد حلول التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="7619e-117">Import ER solutions</span></span>](er-business-document-management.md#import-er-solutions)
3. [<span data-ttu-id="7619e-118">تمكين إدارة مستندات الأعمال</span><span class="sxs-lookup"><span data-stu-id="7619e-118">Enable Business document management</span></span>](er-business-document-management.md#enable-business-document-management)
4. [<span data-ttu-id="7619e-119">تكوين محددات</span><span class="sxs-lookup"><span data-stu-id="7619e-119">Configure parameters</span></span>](er-business-document-management.md#configure-parameters)

### <a name="edit-a-business-document-template"></a><span data-ttu-id="7619e-120">تحرير قالب مستند أعمال</span><span class="sxs-lookup"><span data-stu-id="7619e-120">Edit a business document template</span></span>

1. <span data-ttu-id="7619e-121">في مساحة عمل **إدارة مستندات الأعمال**، حدد **مستند جديد**.</span><span class="sxs-lookup"><span data-stu-id="7619e-121">In the **Business document management** workspace, select **New document**.</span></span>
2. <span data-ttu-id="7619e-122">في صفحة **إنشاء قالب جديد**، حدد قالب **فاتورة النص الحر (نموذج التقارير الإلكترونية) (Excel)**.</span><span class="sxs-lookup"><span data-stu-id="7619e-122">On the **Create a new template** page, select the **Free text invoice (ER sample)(Excel)** template.</span></span>
3. <span data-ttu-id="7619e-123">حدد **إنشاء مستند**.</span><span class="sxs-lookup"><span data-stu-id="7619e-123">Select **Create document**.</span></span>
4. <span data-ttu-id="7619e-124">في حقل **العنوان**، أدخل **FTI sample Litware**.</span><span class="sxs-lookup"><span data-stu-id="7619e-124">In the **Title** field, enter **FTI sample Litware**.</span></span>
5. <span data-ttu-id="7619e-125">حدد **موافق** لإنشاء القالب الجديد.</span><span class="sxs-lookup"><span data-stu-id="7619e-125">Select **OK** to create the new template.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7619e-126">إذا لم تقم بتسجيل الدخول بعد إلى Office Online، فسيتم [توجيهك إلى صفحة تسجيل الدخول إلى Office 365](er-business-document-management.md#frequently-asked-questions).</span><span class="sxs-lookup"><span data-stu-id="7619e-126">If you haven't yet signed in to Office Online, you're [directed to the Office 365 sign-in page](er-business-document-management.md#frequently-asked-questions).</span></span> <span data-ttu-id="7619e-127">للرجوع إلى بيئة Finance، حدد الزر **رجوع** في المستعرض.</span><span class="sxs-lookup"><span data-stu-id="7619e-127">To return to your Finance environment, select the **Back** button in your browser.</span></span>

    <span data-ttu-id="7619e-128">يتم فتح القالب الجديد للتحرير في عنصر تحكم Excel Online المضمن في صفحة محرر القوالب.</span><span class="sxs-lookup"><span data-stu-id="7619e-128">The new template is opened for editing in the Excel Online embedded control on the template editor page.</span></span>

<span data-ttu-id="7619e-129">[![استخدام مساحة عمل إدارة مستندات الأعمال للبدء في تحرير قالب مستند الأعمال](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)</span><span class="sxs-lookup"><span data-stu-id="7619e-129">[![Using the Business document management workspace to start to edit a business document template](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)</span></span>

### <a name="review-the-current-structure-of-the-editable-template"></a><span data-ttu-id="7619e-130">مراجعة البنية الحالية للقالب القابل للتحرير</span><span class="sxs-lookup"><span data-stu-id="7619e-130">Review the current structure of the editable template</span></span>

1. <span data-ttu-id="7619e-131">في Excel Online، ضمن الشريط، ضمن علامة التبويب **طريقة العرض**، في مجموعة **الإظهار**، حدد **خطوط الشبكة**.</span><span class="sxs-lookup"><span data-stu-id="7619e-131">In Excel Online, on the ribbon, on the **View** tab, in the **Show** group, select **Gridlines**.</span></span>
2. <span data-ttu-id="7619e-132">في القالب القابل للتحرير، حدد المستطيل أعلى عنوان القالب.</span><span class="sxs-lookup"><span data-stu-id="7619e-132">In the editable template, select the rectangle above the template title.</span></span> <span data-ttu-id="7619e-133">هذا المستطيل هو صورة تسمي **rptHeaderCompLogo**.</span><span class="sxs-lookup"><span data-stu-id="7619e-133">This rectangle is a picture that is named **rptHeaderCompLogo**.</span></span>
3. <span data-ttu-id="7619e-134">إذا كان جزء **بنية القالب** مخفيًا، فحدد **إظهار البنية**.</span><span class="sxs-lookup"><span data-stu-id="7619e-134">If the **Template structure** pane is hidden, select **Show structure**.</span></span>
4. <span data-ttu-id="7619e-135">في جزء **بنية القالب**، قم بتوسيع **التقرير \> الفاتورة \> rptHeader \> rptHeaderPart1**.</span><span class="sxs-lookup"><span data-stu-id="7619e-135">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
5. <span data-ttu-id="7619e-136">لاحظ أنه في بنية القالب في Finance، يتم عرض عنصر **rptHeaderCompLogo** كعنصر تابع لـ **التقرير \> الفاتورة \> rptHeader \> rptHeaderPart1**.</span><span class="sxs-lookup"><span data-stu-id="7619e-136">Notice that, in the template structure in Finance, the **rptHeaderCompLogo** item is presented as a child item of **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>

<span data-ttu-id="7619e-137">[![استخدام مساحة عمل إدارة مستندات الأعمال لمراجعة الهيكل الحالي لقالب قابل للتحرير](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)</span><span class="sxs-lookup"><span data-stu-id="7619e-137">[![Using the Business document management workspace to review the current structure of an editable template](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)</span></span>

### <a name="update-the-structure-of-a-business-document-template-by-deleting-a-picture"></a><span data-ttu-id="7619e-138">تحديث بنية قالب مستند الأعمال عن طريق حذف صورة</span><span class="sxs-lookup"><span data-stu-id="7619e-138">Update the structure of a business document template by deleting a picture</span></span>

1. <span data-ttu-id="7619e-139">في Excel Online، في القالب القابل للتحرير، حدد صورة **rptHeaderCompLogo**.</span><span class="sxs-lookup"><span data-stu-id="7619e-139">In Excel Online, in the editable template, select the **rptHeaderCompLogo** picture.</span></span>
2. <span data-ttu-id="7619e-140">اتبع إحدى الخطوات التالية لحذف الصورة المحددة من القالب القابل للتحرير:</span><span class="sxs-lookup"><span data-stu-id="7619e-140">Follow one of these steps to delete the selected picture from the editable template:</span></span>

    - <span data-ttu-id="7619e-141">حدد المفتاح **Delete** في لوحة المفاتيح.</span><span class="sxs-lookup"><span data-stu-id="7619e-141">Select the **Delete** key on your keyboard.</span></span>
    - <span data-ttu-id="7619e-142">حدد ثم اضغط (أو انقر بزر الماوس الأيمن) فوق الصورة، ثم حدد **قص**.</span><span class="sxs-lookup"><span data-stu-id="7619e-142">Select and hold (or right-click) the picture, and then select **Cut**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7619e-143">لا يزال عنصر **rptHeaderCompLogo** موجودًا حاليًا في بنية القالب في Finance، على الرغم من أن الصورة لم تعد مضمنة في قالب Excel.</span><span class="sxs-lookup"><span data-stu-id="7619e-143">The **rptHeaderCompLogo** item is currently still present in the template structure in Finance, even though the picture is no longer included in the Excel template.</span></span>

3. <span data-ttu-id="7619e-144">حدد **تحديث البنية** لمزامنة بنيه القالب القابل للتحرير في Excel وFinance.</span><span class="sxs-lookup"><span data-stu-id="7619e-144">Select **Update structure** to sync the structure of the editable template in Excel and Finance.</span></span>
4. <span data-ttu-id="7619e-145">في جزء **بنية القالب**، قم بتوسيع **التقرير \> الفاتورة \> rptHeader \> rptHeaderPart1**.</span><span class="sxs-lookup"><span data-stu-id="7619e-145">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
5. <span data-ttu-id="7619e-146">لاحظ أن عنصر **rptHeaderCompLogo** لم يعد مضمنًا في بنية القالب في Finance.</span><span class="sxs-lookup"><span data-stu-id="7619e-146">Notice that the **rptHeaderCompLogo** item is no longer included in the template structure in Finance.</span></span>

<span data-ttu-id="7619e-147">[![استخدام مساحة عمل إدارة مستندات الأعمال لحذف صورة من قالب مستند الأعمال](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)</span><span class="sxs-lookup"><span data-stu-id="7619e-147">[![Using the Business document management workspace to delete a picture from a business document template](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)</span></span>

### <a name="update-the-structure-of-a-business-document-template-by-adding-a-picture"></a><span data-ttu-id="7619e-148">تحديث بنية قالب مستند الأعمال عن طريق إضافة صورة</span><span class="sxs-lookup"><span data-stu-id="7619e-148">Update the structure of a business document template by adding a picture</span></span>

1. <span data-ttu-id="7619e-149">في Excel Online، ضمن الشريط، في علامة التبويب **إدراج** في مجموعة **الرسوم التوضيحية**، حدد **صورة**.</span><span class="sxs-lookup"><span data-stu-id="7619e-149">In Excel Online, on the ribbon, on the **Insert** tab, in the **Illustrations** group, select **Picture**.</span></span>
2. <span data-ttu-id="7619e-150">حدد **اختيار ملف**، واستعرض إلى الصورة التي تريد إضافتها، وحددها، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7619e-150">Select **Choose file**, browse to the image that you want to add, select it, and then select **OK**.</span></span>
3. <span data-ttu-id="7619e-151">حدد **إدراج**.</span><span class="sxs-lookup"><span data-stu-id="7619e-151">Select **Insert**.</span></span>
4. <span data-ttu-id="7619e-152">انقل الصورة الجديدة حتى تصبح في المكان الصحيح.</span><span class="sxs-lookup"><span data-stu-id="7619e-152">Move the new picture until it's in the correct place.</span></span> <span data-ttu-id="7619e-153">يقوم Excel بتسمية الصورة افتراضيًا.</span><span class="sxs-lookup"><span data-stu-id="7619e-153">By default, Excel names the picture.</span></span> <span data-ttu-id="7619e-154">على سبيل المثال، قد يقوم بتسمية الصورة **صورة 2**.</span><span class="sxs-lookup"><span data-stu-id="7619e-154">For example, it might name the picture **Picture 2**.</span></span>
5. <span data-ttu-id="7619e-155">حدد **تحديث البنية** لمزامنة بنيه القالب القابل للتحرير في Excel وFinance.</span><span class="sxs-lookup"><span data-stu-id="7619e-155">Select **Update structure** to sync the structure of the editable template in Excel and Finance.</span></span>
6. <span data-ttu-id="7619e-156">في جزء **بنية القالب**، قم بتوسيع **التقرير \> الفاتورة \> rptHeader \> rptHeaderPart1**.</span><span class="sxs-lookup"><span data-stu-id="7619e-156">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
7. <span data-ttu-id="7619e-157">لاحظ أن الصورة الجديدة مضمنة الآن كعنصر في بنية القالب في Finance.</span><span class="sxs-lookup"><span data-stu-id="7619e-157">Notice that the new picture is now included as an item in the template structure in Finance.</span></span>

<span data-ttu-id="7619e-158">[![استخدام مساحة عمل إدارة مستندات الأعمال لإضافة صورة إلى قالب مستند الأعمال](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)</span><span class="sxs-lookup"><span data-stu-id="7619e-158">[![Using the Business document management workspace to add a picture to a business document template](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)</span></span>

## <a name="related-links"></a><span data-ttu-id="7619e-159">الارتباطات‬ ذات الصلة</span><span class="sxs-lookup"><span data-stu-id="7619e-159">Related links</span></span>

[<span data-ttu-id="7619e-160">نظرة عامة على إعداد التقارير الإلكترونية (ER)</span><span class="sxs-lookup"><span data-stu-id="7619e-160">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="7619e-161">نظرة عامة على إدارة مستندات الأعمال</span><span class="sxs-lookup"><span data-stu-id="7619e-161">Business document management overview</span></span>](er-business-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]