---
title: إضافه حقول جديده إلى قالب مستند عمل في Microsoft Excel
description: يوفر هذا الموضوع معلومات حول كيفيه أضافه حقول جديده إلى قالب مستند عمل في Microsoft Excel باستخدام ميزه أداره مستندات العمل.
author: NickSelin
manager: AnnBe
ms.date: 11/15/2019
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
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 6368d763f44c015a6e85652b1880cfd86ff5ba09
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569011"
---
# <a name="add-new-fields-to-a-business-document-template-in-microsoft-excel"></a><span data-ttu-id="a12e2-103">إضافه حقول جديده إلى قالب مستند عمل في Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="a12e2-103">Add new fields to a business document template in Microsoft Excel</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a12e2-104">يمكنك أضافه حقول جديده إلى قالب يستخدم لإنشاء مستندات الاعمال بتنسيق Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="a12e2-104">You can add new fields to a template that is used to generate business documents in Microsoft Excel format.</span></span> <span data-ttu-id="a12e2-105">يمكن أضافه هذه الحقول كعناصر نائبه يتم استخدامها لملء المستندات التي تم إنشاؤها بالمعلومات المطلوبة من التطبيق.</span><span class="sxs-lookup"><span data-stu-id="a12e2-105">These fields can be added as placeholders that are used to fill generated documents with required information from the application.</span></span> <span data-ttu-id="a12e2-106">بالنسبة لكل حقل تقوم بإضافته ، يمكنك أيضا تحديد ربط لمصادر البيانات ، لتحديد بيانات التطبيق التي سيتم إدخالها في الحقل عند استخدام القالب لإنشاء مستندات الاعمال.</span><span class="sxs-lookup"><span data-stu-id="a12e2-106">For every field that you add, you can also specify a binding to the data sources, to specify what application data will be entered in the field when the template is used to generate business documents.</span></span>

<span data-ttu-id="a12e2-107">لمعرفة المزيد حول هذه الميزة، أكمل المثال في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="a12e2-107">To learn more about this feature, complete the example in this topic.</span></span> <span data-ttu-id="a12e2-108">يوضح هذا المثال كيفيه تحديث قالب لملء الحقول في نماذج فواتير النص الحر التي يتم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="a12e2-108">This example shows how to update a template to fill in the fields in free text invoice forms that are generated.</span></span>

## <a name="configure-business-document-management-to-edit-templates"></a><span data-ttu-id="a12e2-109">تكوين إدارة مستندات الأعمال لتحرير القوالب</span><span class="sxs-lookup"><span data-stu-id="a12e2-109">Configure Business document management to edit templates</span></span>

<span data-ttu-id="a12e2-110">نظرا لان أداره مستندات العمل (BDM) مبنيه على اطار عمل [النظرة العامة على التقارير الكترونيه (ER)](general-electronic-reporting.md) ، يجب ان تقوم بتكوين معلمات التقاريرالإللكترونية ومعلمات BDM المطلوبة قبل ان تتمكن من البدء في العمل باستخدام BDM.</span><span class="sxs-lookup"><span data-stu-id="a12e2-110">Because Business document management (BDM) is built on top of the [Electronic reporting (ER) overview](general-electronic-reporting.md) framework, you must configure the required ER and BDM parameters before you can start to work with BDM.</span></span>

1.  <span data-ttu-id="a12e2-111">سجل الدخول إلى مثيل Microsoft Dynamics 365 Finance كمسؤول النظام.</span><span class="sxs-lookup"><span data-stu-id="a12e2-111">Sign in to the instance of Microsoft Dynamics 365 Finance as the system administrator.</span></span>
2.  <span data-ttu-id="a12e2-112">أكمل الخطوات التالية للمثال الموجود في الموضوع [نظره عامه على أداره مستندات الاعمال](er-business-document-management.md):</span><span class="sxs-lookup"><span data-stu-id="a12e2-112">Complete the following steps of the example in the [Business document management overview](er-business-document-management.md) topic:</span></span>

    1.  <span data-ttu-id="a12e2-113">قم بتكوين معلمات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a12e2-113">Configure ER parameters.</span></span>
    2.  <span data-ttu-id="a12e2-114">قم بتشغيل BDM.</span><span class="sxs-lookup"><span data-stu-id="a12e2-114">Turn on BDM.</span></span>

<span data-ttu-id="a12e2-115">يمكنك الآن بدء استخدام BDM لتحرير قوالب مستندات العمل.</span><span class="sxs-lookup"><span data-stu-id="a12e2-115">You can now start to use BDM to edit business document templates.</span></span>

## <a name="import-er-solutions-that-contain-a-template"></a><span data-ttu-id="a12e2-116">استيراد حلول التقارير الإلكترونية التي تحتوي على قالب</span><span class="sxs-lookup"><span data-stu-id="a12e2-116">Import ER solutions that contain a template</span></span>

<span data-ttu-id="a12e2-117">يستخدم المثال في هذا الإجراء حل التقارير الإلكترونية الذي تم نشره رسميا.</span><span class="sxs-lookup"><span data-stu-id="a12e2-117">The example in this procedure uses the officially published ER solution.</span></span> <span data-ttu-id="a12e2-118">يجب استيراد تكوينات التقارير الإلكترونية الخاصة بهذا الحل إلى المثيل الحالي لـ Finance.</span><span class="sxs-lookup"><span data-stu-id="a12e2-118">You must import the ER configurations of this solution into your current instance of Finance.</span></span>

<span data-ttu-id="a12e2-119">يحتوي تكوين تنسيق التقارير الإلكترونية **فاتورة النص الحر (Excel)** لهذا الحل على قالب مستند العمل الموجود في تنسيق Excel الذي يمكن تحريره باستخدام BDM.</span><span class="sxs-lookup"><span data-stu-id="a12e2-119">The **Free text invoice (Excel)** ER format configuration of this solution contains the business document template in Excel format that can be edited by using BDM.</span></span> <span data-ttu-id="a12e2-120">قم باستيراد أحدث إصدار من تكوين تنسيق التقارير الإلكترونية هذا من Microsoft Dynamics Lifecycle Service (LCS).</span><span class="sxs-lookup"><span data-stu-id="a12e2-120">Import the latest version of this ER format configuration from Microsoft Dynamics Lifecycle Service (LCS).</span></span> <span data-ttu-id="a12e2-121">سيتم استيراد نموذج بيانات التقارير الإلكترونية المقابل وتكوينات تعيينات نماذج التقارير الإلكترونية تلقائيا.</span><span class="sxs-lookup"><span data-stu-id="a12e2-121">The corresponding ER data model and ER model mapping configurations will be imported automatically.</span></span>

<span data-ttu-id="a12e2-122">لمزيد من المعلومات حول كيفية استيراد تكوينات التقارير الإلكترونية، راجع [إدارة دورة حياة تكوينات التقارير الإلكترونية](general-electronic-reporting-manage-configuration-lifecycle.md).</span><span class="sxs-lookup"><span data-stu-id="a12e2-122">For more information about how to import ER configurations, see [Manage the ER configuration lifecycle](general-electronic-reporting-manage-configuration-lifecycle.md).</span></span>

![صفحة مكتبة الأصول المشتركة لـ LCS](./media/BDM-AddFldExcel-LCS.png)

### <a name="edit-the-er-solution-template"></a><span data-ttu-id="a12e2-124">تحرير قالب حل التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="a12e2-124">Edit the ER solution template</span></span>

1.  <span data-ttu-id="a12e2-125">سجل دخولك كمستخدم لديه حق الوصول إلى مساحة عمل **إدارة مستندات الأعمال**.</span><span class="sxs-lookup"><span data-stu-id="a12e2-125">Sign in as a user who has access to the **Business document management** workspace.</span></span>
2.  <span data-ttu-id="a12e2-126">افتح مساحة عمل **إدارة مستندات الأعمال**.</span><span class="sxs-lookup"><span data-stu-id="a12e2-126">Open the **Business document management** workspace.</span></span>

    ![مساحة عمل إدارة مستندات الأعمال](./media/BDM-AddFldExcel-Workspace.png)

3.  <span data-ttu-id="a12e2-128">في الشبكة، حدد قالب **فاتورة النص الحر (Excel)**.</span><span class="sxs-lookup"><span data-stu-id="a12e2-128">In the grid, select the **Free text invoice (Excel)** template.</span></span>
4.  <span data-ttu-id="a12e2-129">في الجزء الأيسر، حدد **قالب جديد** لإنشاء قالب جديد يستند إلى القالب المحدد.</span><span class="sxs-lookup"><span data-stu-id="a12e2-129">In the right pane, select **New template** to create a new template that is based on the selected template.</span></span>
5.  <span data-ttu-id="a12e2-130">في حقل **العنوان**، أدخل **فاتورة النص الحر (Excel) لـ Contoso** كعنوان للقالب الجديد.</span><span class="sxs-lookup"><span data-stu-id="a12e2-130">In the **Title** field, enter **Free text invoice (Excel) Contoso** as the title of the new template.</span></span>
6.  <span data-ttu-id="a12e2-131">حدد **موافق** لتأكيد بدء عملية التحرير.</span><span class="sxs-lookup"><span data-stu-id="a12e2-131">Select **OK** to confirm the start of the editing process.</span></span>

<span data-ttu-id="a12e2-132">تظهر صفحة محرر قالب BDM.</span><span class="sxs-lookup"><span data-stu-id="a12e2-132">The BDM template editor page appears.</span></span> <span data-ttu-id="a12e2-133">يمكنك استخدام Microsoft 365 لتحرير القالب المحدد عبر الإنترنت في عنصر التحكم المضمن.</span><span class="sxs-lookup"><span data-stu-id="a12e2-133">You can use Microsoft 365 to edit the selected template online in the embedded control.</span></span>

![صفحة محرر قالب BDM](./media/BDM-AddFldExcel-EditableTemplate.png)

### <a name="add-the-label-for-a-new-field-to-the-template"></a><span data-ttu-id="a12e2-135">إضافه التسمية لحقل جديد إلى القالب</span><span class="sxs-lookup"><span data-stu-id="a12e2-135">Add the label for a new field to the template</span></span>

1.  <span data-ttu-id="a12e2-136">في صفحة "محرر قالب BDM"، ضمن شريط Excel، في علامة التبويب **طريقة العرض**، حدد خانات الاختيار **العناوين وخطوط الشبكات** لقالب Excel القابل للتحرير.</span><span class="sxs-lookup"><span data-stu-id="a12e2-136">On the BDM template editor page, on the Excel ribbon, on the **View** tab, select the **Headings and Gridlines** check boxes for the editable Excel template.</span></span>

    ![خانات اختيار العناوين وخطوط الشبكة المحددة](./media/BDM-AddFldExcel-EditableTemplate2.png)

2.  <span data-ttu-id="a12e2-138">حدد الخلايا **E8:F8**.</span><span class="sxs-lookup"><span data-stu-id="a12e2-138">Select cells **E8:F8**.</span></span>
3.  <span data-ttu-id="a12e2-139">على شريط Excel، في علامة التبويب **الصفحة الرئيسية**، حدد **الدمج والمركز** لدمج الخلايا المحددة في خلية **E8:F8** مدمجة جديدة.</span><span class="sxs-lookup"><span data-stu-id="a12e2-139">On the Excel ribbon, on the **Home** tab, select **Merge & Center** to merge the selected cells into a new merged **E8:F8** cell.</span></span>
4.  <span data-ttu-id="a12e2-140">في الخلية المدمجة **E8:F8**، أدخل **URL**.</span><span class="sxs-lookup"><span data-stu-id="a12e2-140">In the merged cell **E8:F8**, enter **URL**.</span></span>
5.  <span data-ttu-id="a12e2-141">حدد الخلية المدمجة **E7:F7**، حدد **رسام التنسيق**، ثم حدد الخلية المدمجة **E8:F8** لتنسيقها بنفس الطريقة مثل الخلية المدمجة **E7:F7**.</span><span class="sxs-lookup"><span data-stu-id="a12e2-141">Select merged cell **E7:F7**, select **Format painter**, and then select merged cell **E8:F8** to format it in the same way as merged cell **E7:F7**.</span></span>

    ![إضافه تسمية الحقل الجديد إلى القالب](./media/BDM-AddFldExcel-EditableTemplate3.png)

### <a name="format-the-template-to-reserve-space-for-a-new-field"></a><span data-ttu-id="a12e2-143">تنسيق القالب لحجز مساحة لحقل جديد</span><span class="sxs-lookup"><span data-stu-id="a12e2-143">Format the template to reserve space for a new field</span></span>

1.  <span data-ttu-id="a12e2-144">في صفحة محرر قالب BDM، حدد الخلية المدمجة **G8:H8**.</span><span class="sxs-lookup"><span data-stu-id="a12e2-144">On the BDM template editor page, select merged cell **G8:H8**.</span></span>
2.  <span data-ttu-id="a12e2-145">على شريط Excel، في علامة التبويب **الصفحة الرئيسية**، حدد **الدمج والمركز** لدمج الخلايا المحددة في خلية **G8:H8** مدمجة جديدة.</span><span class="sxs-lookup"><span data-stu-id="a12e2-145">On the Excel ribbon, on the **Home** tab, select **Merge & Center** to merge the selected cells into a new merged **G8:H8** cell.</span></span>
3.  <span data-ttu-id="a12e2-146">حدد الخلية المدمجة **G7:H7**، حدد **رسام التنسيق**، ثم حدد الخلية المدمجة **G8:H8** لتنسيقها بنفس الطريقة مثل الخلية المدمجة **G7:H7**.</span><span class="sxs-lookup"><span data-stu-id="a12e2-146">Select merged cell **G7:H7**, select **Format painter**, and then select merged cell **G8:H8** to format it in the same way as merged cell **G7:H7**.</span></span>

    ![المساحة المحجوزة للحقل الجديد](./media/BDM-AddFldExcel-EditableTemplate4.png)

4.  <span data-ttu-id="a12e2-148">في حقل مربع **الاسم**، حدد **CompanyInfo**.</span><span class="sxs-lookup"><span data-stu-id="a12e2-148">In the **Name** box field, select **CompanyInfo**.</span></span>

    <span data-ttu-id="a12e2-149">يحتفظ نطاق **CompanyInfo** الخاص بقالب Excel الحالي بكافة الحقول المستخدمة لملء راس التقرير الذي تم إنشاؤه بتفاصيل الشركة الحالية كطرف البائع.</span><span class="sxs-lookup"><span data-stu-id="a12e2-149">The **CompanyInfo** range of the current Excel template holds all the fields that are used to fill the header of a generated report with the details of the current company as a seller party.</span></span>

    ![نطاق CompanyInfo المحدد](./media/BDM-AddFldExcel-SelectCompanyInfoRange.png)

### <a name="add-a-new-field-to-the-template"></a><span data-ttu-id="a12e2-151">إضافة حقل جديد إلى القالب</span><span class="sxs-lookup"><span data-stu-id="a12e2-151">Add a new field to the template</span></span>

1.  <span data-ttu-id="a12e2-152">في صفحة **محرر قالب BDM**، ضمن جزء الإجراء، حدد **إظهار التنسيق**.</span><span class="sxs-lookup"><span data-stu-id="a12e2-152">On the **BDM template editor** page, on the Action Pane, select **Show format**.</span></span>
2.  <span data-ttu-id="a12e2-153">في جزء **بنية القالب**، حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="a12e2-153">In the **Template structure** pane, select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a12e2-154">يجب عليك تعديل القسم من القالب الذي تريد استخدامه كحقل جديد.</span><span class="sxs-lookup"><span data-stu-id="a12e2-154">You must adjust the section of the template that you want to use as a new field.</span></span> <span data-ttu-id="a12e2-155">لقد قمت بالفعل بهذا التعديل عن طريق تنسيق الخلية المدمجة **G8:H8**.</span><span class="sxs-lookup"><span data-stu-id="a12e2-155">You already made this adjustment by formatting merged cell **G8:H8**.</span></span>

    ![إضافة حقل جديد إلى القالب](./media/BDM-AddFldExcel-AddCell.png)

3.  <span data-ttu-id="a12e2-157">حدد **Excel/خلية** لأضافه حقل جديد كخليه في القالب.</span><span class="sxs-lookup"><span data-stu-id="a12e2-157">Select **Excel\Cell** to add a new field as a cell in the template.</span></span>

    <span data-ttu-id="a12e2-158">يمكنك تحديد **Excel/نطاق** إذا كنت ترغب في أضافه نطاق جديد إلى القالب.</span><span class="sxs-lookup"><span data-stu-id="a12e2-158">You can select **Excel\Range** if you want to add a new range to the template.</span></span> <span data-ttu-id="a12e2-159">يمكن ان يحتوي النطاق الذي يتم إدخاله على خلايا متعددة.</span><span class="sxs-lookup"><span data-stu-id="a12e2-159">The range that is entered can contain multiple cells.</span></span> <span data-ttu-id="a12e2-160">يمكنك أضافة هذه الخلايا لاحقا.</span><span class="sxs-lookup"><span data-stu-id="a12e2-160">You can add these cells later.</span></span>
    
    <span data-ttu-id="a12e2-161">ولاحظ أن مكون قالب **CompanyInfo** يتم تحديده تلقائيا في جزء **بنية القالب**، نظرا لأنه المكون الأصلي الأكثر ملائمة في بنيه القالب الحالي للحقل الذي تقوم بإضافته.</span><span class="sxs-lookup"><span data-stu-id="a12e2-161">Notice that the **CompanyInfo** template component, is automatically selected in the **Template structure** pane, because it's the most suitable parent component in the current template structure for the field that you're adding.</span></span>
    
4.  <span data-ttu-id="a12e2-162">في حقل **نطاق Excel**، أدخل **CompanyURL_Value**.</span><span class="sxs-lookup"><span data-stu-id="a12e2-162">In the **Excel range** field, enter **CompanyURL_Value**.</span></span>
5.  <span data-ttu-id="a12e2-163">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="a12e2-163">Select **OK**.</span></span>

    ![إضافة حقل CompanyURL_Value إلى بنية القالب](./media/BDM-AddFldExcel-EditableTemplate5.png)

6.  <span data-ttu-id="a12e2-165">في جزء **بنية القالب**، حدد زر علامة الحذف (...)، ثم حدد **إظهار الروابط**.</span><span class="sxs-lookup"><span data-stu-id="a12e2-165">In the **Template structure** pane, select the ellipsis button (...), and then select **Show bindings**.</span></span>

    ![إظهار الروابط المحددة](./media/BDM-AddFldExcel-ShowBindings.png)

    <span data-ttu-id="a12e2-167">يعرض جزء **بنيه القالب** الآن مصادر البيانات المتوفرة في التنسيق الأساسي للتقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a12e2-167">The **Template structure** pane now shows the data sources that are available in the underlying ER format.</span></span>

7.  <span data-ttu-id="a12e2-168">حدد **CompanyInfo_Value** كالحقل الذي تخطط لربطه بمصدر بيانات بتنسيق التقارير الإلكترونية الأساسي.</span><span class="sxs-lookup"><span data-stu-id="a12e2-168">Select **CompanyInfo_Value** as the field that you plan to bind to a data source of the underlying ER format.</span></span>
8.  <span data-ttu-id="a12e2-169">في قسم **مصادر البيانات** في جزء **بنية القالب**، قم بتوسيع **النموذج \> InvoiceBase \> CompanyInfo**.</span><span class="sxs-lookup"><span data-stu-id="a12e2-169">In the **Data sources** section of the **Template structure** pane, expand **Model \> InvoiceBase \> CompanyInfo**.</span></span>
9.  <span data-ttu-id="a12e2-170">ضمن **CompanyInfo**، حدد عنصر **WebsiteURI**.</span><span class="sxs-lookup"><span data-stu-id="a12e2-170">Under **CompanyInfo**, select the **WebsiteURI** item.</span></span>

    ![عنصر WebsiteURI المحدد](./media/BDM-AddFldExcel-BindURL.png)

10. <span data-ttu-id="a12e2-172">حدد **ربط**.</span><span class="sxs-lookup"><span data-stu-id="a12e2-172">Select **Bind**.</span></span>
11. <span data-ttu-id="a12e2-173">في جزء **بنيه القالب**، حدد **حفظ**، ثم اغلق صفحة محرر قالب BDM.</span><span class="sxs-lookup"><span data-stu-id="a12e2-173">In the **Template structure** pane, select **Save**, and then close the BDM template editor page.</span></span>

<span data-ttu-id="a12e2-174">في مساحة عمل **إدارة مستندات الأعمال**، تعرض علامة التبويب **القالب** في الجزء الأيسر القالب المحدث.</span><span class="sxs-lookup"><span data-stu-id="a12e2-174">In the **Business document management** workspace, the **Template** tab in the right pane shows the updated template.</span></span> <span data-ttu-id="a12e2-175">في الشبكة، لاحظ أن حقل **الحالة** للقالب المحرر تم تغييره إلى إلى **مسودة**، ولم يُعد حقل **المراجعة** فارغًا.</span><span class="sxs-lookup"><span data-stu-id="a12e2-175">In the grid, notice that the **Status** field for the edited template has been changed to **Draft**, and the **Revision** field is no longer blank.</span></span> <span data-ttu-id="a12e2-176">تشير هذه التغييرات إلى أن عملية تحرير هذا القالب قد بدأت.</span><span class="sxs-lookup"><span data-stu-id="a12e2-176">These changes indicate that the process of editing this template has been started.</span></span>

![القالب المحرر في مساحة عمل إدارة مستندات العمل](./media/BDM-AddFldExcel-Workspace2.png)

## <a name="review-company-settings"></a><span data-ttu-id="a12e2-178">مراجعة إعدادات الشركة</span><span class="sxs-lookup"><span data-stu-id="a12e2-178">Review company settings</span></span>

1.  <span data-ttu-id="a12e2-179">انتقل إلى **إدارة المؤسسة \> المؤسسات \> الكيانات القانونية**.</span><span class="sxs-lookup"><span data-stu-id="a12e2-179">Go to **Organization administration \> Organizations \> Legal entities**.</span></span>
2.  <span data-ttu-id="a12e2-180">في علامة التبويب السريع **معلومات جهة الاتصال**، تحقق من إدخال عنوان URL الخاص بالشركة.</span><span class="sxs-lookup"><span data-stu-id="a12e2-180">On the **Contact information** FastTab, verify that the company URL is entered.</span></span>

![عنوان URL للشركة الذي تم إدخاله في صفحة الكيانات القانونية](./media/BDM-AddFldExcel-CompanyInfo.png)

## <a name="generate-business-documents-to-test-the-updated-template"></a><span data-ttu-id="a12e2-182">إنشاء مستندات الأعمال لاختبار القالب المحدث</span><span class="sxs-lookup"><span data-stu-id="a12e2-182">Generate business documents to test the updated template</span></span>

1.  <span data-ttu-id="a12e2-183">في التطبيق، قم بتغيير الشركة إلى **USMF**، وانتقل إلى **الحسابات المدينة \> الفواتير\> كل فواتير النص الحر**.</span><span class="sxs-lookup"><span data-stu-id="a12e2-183">In the application, change the company to **USMF**, and go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>
2.  <span data-ttu-id="a12e2-184">حدد الفاتورة **FTI-00000002**، ثم حدد **إدارة الطباعة**.</span><span class="sxs-lookup"><span data-stu-id="a12e2-184">Select invoice **FTI-00000002**, and then select **Print management**.</span></span>
3.  <span data-ttu-id="a12e2-185">في الجزء الأيمن، قم بتوسيع **الوحدة - الحسابات المدينة\> المستندات\> فاتورة النص الحر**.</span><span class="sxs-lookup"><span data-stu-id="a12e2-185">In the left pane, expand **Module - accounts receivable \> Documents \> Free text invoice**.</span></span>
4.  <span data-ttu-id="a12e2-186">ضمن **فاتورة النص الحر**، حدد مستوى **النص الأصلي** لتحديد نطاق الفواتير للمعالجة.</span><span class="sxs-lookup"><span data-stu-id="a12e2-186">Under **Free text invoice**, select the **Original document** level to specify the scope of invoices for processing.</span></span>
5.  <span data-ttu-id="a12e2-187">في الجزء الأيسر، في حقل **تنسيق التقرير**، حدد **فاتورة النص الحر (Excel) لـ Contoso** لمستوى المستند المحدد.</span><span class="sxs-lookup"><span data-stu-id="a12e2-187">In the right pane, in the **Report format** field, select the **Free text invoice (Excel) Contoso** template for the specified document level.</span></span>

    ![قالب فاتورة النص الحر (Excel) لشركة Contoso المحدد](./media/BDM-AddFldExcel-PrintMngtSetting.png)

6.  <span data-ttu-id="a12e2-189">اضغط **Esc** لإغلاق الصفحة الحالية.</span><span class="sxs-lookup"><span data-stu-id="a12e2-189">Press **Esc** to close the current page.</span></span>
7.  <span data-ttu-id="a12e2-190">حدد **طباعة \> تم التحديد**.</span><span class="sxs-lookup"><span data-stu-id="a12e2-190">Select **Print \> Selected**.</span></span>
8.  <span data-ttu-id="a12e2-191">قم بتنزيل المستند الذي تم إنشاؤه، ثم قم بفتحه في Excel.</span><span class="sxs-lookup"><span data-stu-id="a12e2-191">Download the generated document, and open it in Excel.</span></span>

    ![فاتورة النص الحر بتنسيق Excel](./media/BDM-AddFldExcel-PreviewReport.png)

<span data-ttu-id="a12e2-193">يتم استخدام القالب المعدل لإنشاء تقرير فاتورة النص الحر للصنف المحدد.</span><span class="sxs-lookup"><span data-stu-id="a12e2-193">The modified template is used to generate the free text invoice report for the selected item.</span></span> <span data-ttu-id="a12e2-194">لتحليل كيفية تأثر هذا التقرير بالتغييرات التي قمت بإدخالها على القالب، يمكنك تشغيل هذا التقرير في جلسة عمل تطبيق واحدة مباشرة بعد تغيير القالب في جلسة عمل تطبيق أخرى.</span><span class="sxs-lookup"><span data-stu-id="a12e2-194">To analyze how this report is affected by changes that you make to the template, run the report in one application session immediately after you change the template in another application session.</span></span>

## <a name="related-links"></a><span data-ttu-id="a12e2-195">الارتباطات‬ ذات الصلة</span><span class="sxs-lookup"><span data-stu-id="a12e2-195">Related links</span></span>

[<span data-ttu-id="a12e2-196">نظرة عامة حول التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="a12e2-196">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="a12e2-197">نظرة عامة على إدارة مستندات الأعمال</span><span class="sxs-lookup"><span data-stu-id="a12e2-197">Business document management overview</span></span>](er-business-document-management.md)

[<span data-ttu-id="a12e2-198">تصميم تكوين لإنشاء التقارير بتنسيق OPENXML</span><span class="sxs-lookup"><span data-stu-id="a12e2-198">Design a configuration for generating reports in OPENXML format</span></span>](tasks/er-design-reports-openxml-2016-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]