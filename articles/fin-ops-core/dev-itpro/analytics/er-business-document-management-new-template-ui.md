---
title: واجهة مستخدم مستند جديد في إدارة مستندات الأعمال
description: يوفر هذا الموضوع معلومات حول كيفية استخدام واجهة مستخدم (UI) مستند جديد في ميزة إدارة مستندات الأعمال في إطار عمل إعداد التقارير الإلكترونية (ER).
author: v-anamir
manager: AnnBe
ms.date: 05/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7f8099f2f6872c34c30de918a6fc5fd27bcde958
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565700"
---
# <a name="new-document-user-interface-in-business-document-management"></a><span data-ttu-id="8c1fd-103">واجهة مستخدم مستندات جديدة في إدارة مستندات الأعمال</span><span class="sxs-lookup"><span data-stu-id="8c1fd-103">New document user interface in Business document management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8c1fd-104">تتيح إدارة مستندات الأعمال لمستخدمي الأعمال تحرير قوالب مستندات الأعمال باستخدام خدمة Microsoft 365 أو تطبيق سطح مكتب Microsoft Office الملائم.</span><span class="sxs-lookup"><span data-stu-id="8c1fd-104">Business document management lets business users edit business document templates by using a Microsoft 365 service or the appropriate Microsoft Office desktop application.</span></span> <span data-ttu-id="8c1fd-105">وقد تتضمن عمليات التحرير تغييرات في التصميم أو عمليات نشر جديدة، أو قد يضيف المستخدمون عناصر نائبة لتضمين بيانات إضافية دون الحاجة إلى تغيير الكود المصدر.</span><span class="sxs-lookup"><span data-stu-id="8c1fd-105">Edits might include design changes or new deployments, or users might add placeholders to include additional data without having to change the source code.</span></span> <span data-ttu-id="8c1fd-106">لمزيد من المعلومات حول كيفية العمل مع إدارة مستندات الأعمال، راجع [نظرة عامة على إدارة مستندات الأعمال‬](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="8c1fd-106">For more information about how to work with Business document management, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="8c1fd-107">تعد واجهة مستخدم (UI) مستند جديد أوضح ومريحة أكثر للاستخدام.</span><span class="sxs-lookup"><span data-stu-id="8c1fd-107">The new document user interface (UI) is clearer and more comfortable to use.</span></span> <span data-ttu-id="8c1fd-108">لا تظهر منطقة **مستندات الأعمال** إلا القوالب المتوفرة للموفر الحالي.</span><span class="sxs-lookup"><span data-stu-id="8c1fd-108">The **Business document** area shows only the templates that are available for the current provider.</span></span>

<span data-ttu-id="8c1fd-109">يتيح زر **مستند جديد** للمستخدمين إنشاء قالب وتحريره في تكوين تنسيق إعداد التقارير الإلكترونية (ER) الذي يوفره موفر آخر.</span><span class="sxs-lookup"><span data-stu-id="8c1fd-109">The **New document** button lets users create and edit a template in an Electronic reporting (ER) format configuration that is provided by another provider.</span></span> <span data-ttu-id="8c1fd-110">في المثال الموجود في هذا الموضوع، الموفر هو Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8c1fd-110">In the example in this topic, the provider is Microsoft.</span></span>

## <a name="make-the-new-document-ui-in-business-document-management-available"></a><span data-ttu-id="8c1fd-111">توفير واجهة مستخدم مستند جديد في إدارة مستندات الأعمال</span><span class="sxs-lookup"><span data-stu-id="8c1fd-111">Make the new document UI in Business document management available</span></span>

<span data-ttu-id="8c1fd-112">لبدء استخدام واجهة مستخدم مستند جديد في إدارة مستندات الأعمال، يجب تشغيل ميزة **تجربة واجهة المستخدم التي تشبه Office لإدارة مستندات الأعمال** في مساحة العمل **إدارة الميزات**.</span><span class="sxs-lookup"><span data-stu-id="8c1fd-112">To start to use the new document UI in Business document management, you must turn on the **Office-like UI experience for Business document management** feature in the **Feature management** workspace.</span></span>

<span data-ttu-id="8c1fd-113">اتبع هذه الخطوات لتشغيل هذه الميزة لكل الكيانات القانونية.</span><span class="sxs-lookup"><span data-stu-id="8c1fd-113">Follow these steps to turn on this feature for all legal entities.</span></span>

1. <span data-ttu-id="8c1fd-114">في مساحة العمل **إدارة الميزات**، في علامة التبويب **جديد**، حدد ميزة **تجربة واجهة المستخدم التي تشبه Office لإدارة مستندات العمل** الموجودة في القائمة.</span><span class="sxs-lookup"><span data-stu-id="8c1fd-114">In the **Feature management** workspace, on the **New** tab, select the **Office-like UI experience for Business document management** feature in the list.</span></span>
2. <span data-ttu-id="8c1fd-115">حدد **تمكين الآن** لتشغيل الميزة المحددة.</span><span class="sxs-lookup"><span data-stu-id="8c1fd-115">Select **Enable now** to turn on the selected feature.</span></span>
3. <span data-ttu-id="8c1fd-116">قم بتحديث الصفحة للوصول إلى الميزة الجديدة.</span><span class="sxs-lookup"><span data-stu-id="8c1fd-116">Refresh the page to access the new feature.</span></span>

### <a name="edit-templates-that-are-owned-by-other-providers"></a><span data-ttu-id="8c1fd-117">تحرير القوالب التي يملكها موفرون آخرون</span><span class="sxs-lookup"><span data-stu-id="8c1fd-117">Edit templates that are owned by other providers</span></span>

1. <span data-ttu-id="8c1fd-118">في مساحة عمل **إدارة مستندات الأعمال**، حدد **مستند جديد**.</span><span class="sxs-lookup"><span data-stu-id="8c1fd-118">In the **Business document management** workspace, select **New document**.</span></span>

    ![مساحة عمل إدارة مستندات الأعمال](./media/BDM_overview_new_template1.png)

2. <span data-ttu-id="8c1fd-120">في مربع الحوار، حدد المستند المراد استخدامه كقالب، ثم حدد **إنشاء مستند**.</span><span class="sxs-lookup"><span data-stu-id="8c1fd-120">In the dialog box, select the document to use as a template, and then select **Create document**.</span></span>

    ![مربع الحوار مستندات الأعمال](./media/BDM_overview_new_template2.png)

3. <span data-ttu-id="8c1fd-122">في مربع الحوار الجديد، في حقل **العنوان**، غيِّر العنوان على النحو الذي تريده.</span><span class="sxs-lookup"><span data-stu-id="8c1fd-122">In the new dialog box, in the **Title** field, change the title as you require.</span></span> <span data-ttu-id="8c1fd-123">يتم استخدام نص العنوان لتسمية تكوين تنسيق إعداد التقارير الإلكترونية الجديد الذي يتم إنشاؤه تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="8c1fd-123">The title text is used to name the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="8c1fd-124">سيحتوي إصدار المسودة لهذا التكوين **(نسخة تقرير FTI للعميل (GER)**) على القالب الذي تم تحريره وسيتم استخدامه لتشغيل تنسيق إعداد التقارير الإلكترونية هذا للمستخدم الحالي.</span><span class="sxs-lookup"><span data-stu-id="8c1fd-124">The draft version of this configuration (**Customer FTI report (GER) Copy**) will contain the edited template and will be used to run this ER format for the current user.</span></span> <span data-ttu-id="8c1fd-125">وسيتم استخدام القالب الأصلي من تكوين تنسيق إعداد التقارير الإلكترونية الأساسي لتشغيل تنسيق إعداد التقارير الإلكترونية هذا لكل المستخدمين الآخرين.</span><span class="sxs-lookup"><span data-stu-id="8c1fd-125">The original template from the base ER format configuration will be used to run this ER format for every other user.</span></span>
4. <span data-ttu-id="8c1fd-126">في الحقل‏‎ **الاسم**، غيِّر اسم المراجعة الأولى للقالب القابل للتحرير التي سيتم إنشاؤها تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="8c1fd-126">In the **Name** field, change the name of the first revision of the editable template that will be automatically created.</span></span>
5. <span data-ttu-id="8c1fd-127">في حقل‏‎ **التعليق**، غيِّر الملاحظات للمراجعة التي سيتم إنشاؤها تلقائيًا للقالب القابل للتحرير.</span><span class="sxs-lookup"><span data-stu-id="8c1fd-127">In the **Comment** field, update the remarks for the revision of the editable template that will be automatically created.</span></span>
6. <span data-ttu-id="8c1fd-128">حدد **موافق** لتأكيد بدء عملية التحرير.</span><span class="sxs-lookup"><span data-stu-id="8c1fd-128">Select **OK** to confirm the start of the editing process.</span></span>

    ![مربع حوار إنشاء مستند](./media/BDM_overview_new_template3.png)

<span data-ttu-id="8c1fd-130">يُستخدم زر **مستند جديد** لإنشاء قالب في تكوين تنسيق إعداد التقارير الإلكترونية الذي يوفره موفر آخر وتحريره.</span><span class="sxs-lookup"><span data-stu-id="8c1fd-130">The **New document** button is used to create and edit a template in an ER format configuration that is provided by another provider.</span></span> <span data-ttu-id="8c1fd-131">في هذا المثال، الموفر هو Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8c1fd-131">In this example, the provider is Microsoft.</span></span> <span data-ttu-id="8c1fd-132">عند تحديد **مستند جديد**، يمكنك عرض جميع القوالب المملوكة للموفرين الحاليين والآخرين.</span><span class="sxs-lookup"><span data-stu-id="8c1fd-132">When you select **New document**, you can view all the templates that are owned by current and other providers.</span></span> <span data-ttu-id="8c1fd-133">بعد تحديد القالب، يتم فتحه للتحرير.</span><span class="sxs-lookup"><span data-stu-id="8c1fd-133">After you select the template, it's opened for editing.</span></span> <span data-ttu-id="8c1fd-134">يتم بعد ذلك تخزين القالب الذي تم تحريره في تكوين تنسيق تقارير إلكترونية جديد يتم إنشاؤه بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="8c1fd-134">The edited template will then be stored in a new ER format configuration that is automatically generated.</span></span>

<span data-ttu-id="8c1fd-135">لمزيد من المعلومات، راجع [‏‫نظرة عامة على إدارة مستندات الأعمال](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="8c1fd-135">For more information, see [Business document management overview](er-business-document-management.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]