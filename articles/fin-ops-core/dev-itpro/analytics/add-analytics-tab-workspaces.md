---
title: إضافة تحليلات إلى مساحات العمل باستخدام Power BI Embedded
description: يوضح هذا الموضوع كيفية تضمين تقرير Power BI في علامة تبويب "التحليلات" في مساحة عمل.
author: tjvass
manager: AnnBe
ms.date: 06/21/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 1a357c4623f4f9dc441fe328ec0d5481c14ae4af
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771623"
---
# <a name="add-analytics-to-workspaces-by-using-power-bi-embedded"></a><span data-ttu-id="a7bdd-103">إضافة تحليلات إلى مساحات العمل باستخدام Power BI Embedded</span><span class="sxs-lookup"><span data-stu-id="a7bdd-103">Add analytics to workspaces by using Power BI Embedded</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="a7bdd-104">هذه الميزة مدعومة في Finance and Operations (الإصدار 7.2 والإصدارات اللاحقة).</span><span class="sxs-lookup"><span data-stu-id="a7bdd-104">This feature is supported in Finance and Operations (version 7.2 and later).</span></span>

## <a name="introduction"></a><span data-ttu-id="a7bdd-105">مقدمة</span><span class="sxs-lookup"><span data-stu-id="a7bdd-105">Introduction</span></span>
<span data-ttu-id="a7bdd-106">يوضح هذا الموضوع كيفية تضمين تقرير Microsoft Power BI في علامة تبويب **التحليلات** في مساحة عمل.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-106">This topic shows how to embed a Microsoft Power BI report on the **Analytics** tab of a workspace.</span></span> <span data-ttu-id="a7bdd-107">بالنسبة إلى المثال الذي تم تقديمه هنا، سنقوم بتوسيع مساحة عمل **إدارة الحجز** في تطبيق إدارة الأسطول لتضمين مساحة عمل تحليلية على علامة تبويب **التحليلات**.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-107">For the example that is given here, we will extend the **Reservation management** workspace in the Fleet Management application to embed an analytical workspace on an **Analytics** tab.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a7bdd-108">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="a7bdd-108">Prerequisites</span></span>
+ <span data-ttu-id="a7bdd-109">الوصول إلى بيئة مطور تقوم بتشغيل تحديث النظام الأساسي 8 أو الإصدارات الأحدث.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-109">Access to a developer environment that runs Platform update 8 or later.</span></span>
+ <span data-ttu-id="a7bdd-110">تقرير تحليلي (ملف pbix.) تم إنشاؤه باستخدام Microsoft Power BI Desktop، وله نموذج بيانات مصدره قاعدة بيانات مخزن الكيانات.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-110">An analytical report (.pbix file) that was created by using Microsoft Power BI Desktop, and that has a data model that is sourced from the Entity store database.</span></span>

## <a name="overview"></a><span data-ttu-id="a7bdd-111">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="a7bdd-111">Overview</span></span>
<span data-ttu-id="a7bdd-112">سواء قمت بتوسيع مساحة عمل تطبيق موجودة أو بتقديم مساحة عمل جديدة خاصة بك، يمكنك استخدام طرق العرض التحليلية المضمنة لتقديم عروض ثاقبة وتفاعلية لبيانات عملك.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-112">Whether you extend an existing application workspace or introduce a new workspace of your own, you can use embedded analytical views to deliver insightful and interactive views of your business data.</span></span> <span data-ttu-id="a7bdd-113">تتكون عملية إضافة علامة تبويب مساحة عمل تحليلية من أربع خطوات.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-113">The process for adding an analytical workspace tab has four steps.</span></span>

1. <span data-ttu-id="a7bdd-114">إضافة ملف pbix. كمورد Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-114">Add a .pbix file as a Dynamics 365 resource.</span></span>
2. <span data-ttu-id="a7bdd-115">تحديد علامة تبويب مساحة عمل تحليلية.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-115">Define an analytical workspace tab.</span></span>
3. <span data-ttu-id="a7bdd-116">تضمين مورد pbix. في علامة تبويب مساحة العمل.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-116">Embed the .pbix resource on the workspace tab.</span></span>
4. <span data-ttu-id="a7bdd-117">اختياري: إضافة ملحقات لتخصيص طريقة العرض.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-117">Optional: Add extensions to customize the view.</span></span>

> [!NOTE]
> <span data-ttu-id="a7bdd-118">للحصول على مزيد من المعلومات حول كيفية إنشاء تقارير تحليلية، راجع [بدء استخدام Power BI Desktop](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).</span><span class="sxs-lookup"><span data-stu-id="a7bdd-118">For more information about how to create analytical reports, see [Getting started with Power BI Desktop](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).</span></span> <span data-ttu-id="a7bdd-119">تعتبر هذه الصفحة مصدرًا رائعًا للحصول على معلومات دقيقة من شأنها مساعدتك في إنشاء حلول تتعلق بإعداد تقارير تحليلية مقنعة.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-119">This page is a great source for insights that can help you create compelling analytical reporting solutions.</span></span>

## <a name="add-a-pbix-file-as-a-resource"></a><span data-ttu-id="a7bdd-120">إضافة ملف pbix. كمورد</span><span class="sxs-lookup"><span data-stu-id="a7bdd-120">Add a .pbix file as a resource</span></span>
<span data-ttu-id="a7bdd-121">قبل أن تبدأ، يجب إنشاء تقرير Power BI الذي ستقوم بتضمينه في مساحة العمل أو الحصول عليه.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-121">Before you begin, you must create or obtain the Power BI report that you will embed in the workspace.</span></span> <span data-ttu-id="a7bdd-122">للحصول على مزيد من المعلومات حول كيفية إنشاء تقارير تحليلية، راجع [بدء استخدام Power BI Desktop](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).</span><span class="sxs-lookup"><span data-stu-id="a7bdd-122">For more information about how to create analytical reports, see [Getting started with Power BI Desktop](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).</span></span>

<span data-ttu-id="a7bdd-123">اتبع هذه الخطوات لإضافة ملف pbix. كمنتج لمشروع Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-123">Follow these steps to add a .pbix file as a Visual Studio project artifact.</span></span>

1. <span data-ttu-id="a7bdd-124">أنشئ مشروعًا جديدً في النموذج المناسب.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-124">Create a new project in the appropriate model.</span></span>
2. <span data-ttu-id="a7bdd-125">في "مستكشف الحلول"، حدد المشروع وانقر بزر الماوس الأيمن فوقه، ثم حدد **إضافة** \> **صنف جديد**.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-125">In Solution Explorer, select the project, right-click, and then select **Add** \> **New Item**.</span></span>
3. <span data-ttu-id="a7bdd-126">في **إضافة صنف جديد**، تحت **منتجات Operations**، حدد قالب **المورد**.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-126">In the **Add New Item** dialog box, under **Operations Artifacts**, select the **Resource** template.</span></span>
4. <span data-ttu-id="a7bdd-127">أدخل اسمًا سيتم استخدامه للإشارة إلى التقرير في بيانات تعريف X++، ومن ثم انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-127">Enter a name that will be used to reference the report in X++ metadata, and then click **Add**.</span></span>

    ![مربع الحوار "إضافة صنف جديد"](media/analytical-workspace-add.png)

5. <span data-ttu-id="a7bdd-129">ابحث عن ملف pbix. الذي يحتوي على تعريف التقرير التحليلي، ثم انقر فوق **فتح**.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-129">Find the .pbix file that contains the definition of the analytical report, and then click **Open**.</span></span>

    ![حدد مربع حوار "ملف المورد"](media/analytical-workspace-select-resource.png)

<span data-ttu-id="a7bdd-131">والآن بعد أن قمت بإضافة ملف pbix. كمورد Dynamics 365، يمكنك تضمين التقارير في مساحات العمل وإضافة الارتباطات المباشرة باستخدام عناصر القائمة.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-131">Now that you've added the .pbix file as a Dynamics 365 resource, you can embed the reports in workspaces and add direct links by using menu items.</span></span>

## <a name="add-a-tab-control-to-an-application-workspace"></a><span data-ttu-id="a7bdd-132">إضافة عنصر تحكم علامة تبويب إلى مساحة عمل التطبيق</span><span class="sxs-lookup"><span data-stu-id="a7bdd-132">Add a tab control to an application workspace</span></span>
<span data-ttu-id="a7bdd-133">في هذا المثال، سنقوم بتوسيع مساحة عمل **إدارة الحجز** في نموذج إدارة الأسطول عن طريق إضافة علامة تبويب **التحليلات** إلى تعريف النموذج **FMClerkWorkspace**.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-133">In this example, we will extend the **Reservation management** workspace in the Fleet Management model by adding the **Analytics** tab to the definition of the **FMClerkWorkspace** form.</span></span>

<span data-ttu-id="a7bdd-134">يبين الرسم التوضيحي التالي الشكل الذي يتخذه النموذج **FMClerkWorkspace** في المصمم في Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-134">The following illustration shows what the **FMClerkWorkspace** form looks like in the designer in Microsoft Visual Studio.</span></span>

![نموذج FMClerkWorkspace قبل التغييرات](media/analytical-workspace-definition-before.png)

<span data-ttu-id="a7bdd-136">اتبع هذه الخطوات لتوسيع تعريف النموذج لمساحة عمل **إدارة الحجز**.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-136">Follow these steps to extend the form definition for the **Reservation management** workspace.</span></span>

1. <span data-ttu-id="a7bdd-137">افتح مصمم النماذج لتوسيع تعريف التصميم.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-137">Open the form designer to extend the design definition.</span></span>
2. <span data-ttu-id="a7bdd-138">في تعريف التصميم، حدد العنصر العلوي المسمى **تصميم | نمط: تشغيلي في مساحة العمل**.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-138">In the design definition, select the top element that is labeled **Design | Pattern: Workspace Operational**.</span></span>
3. <span data-ttu-id="a7bdd-139">انقر بزر الماوس الأيمن، ثم حدد **جديد** \> **علامة التبويب** لإضافة عنصر تحكم جديد مسمى **FormTabControl1**.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-139">Right-click, and then select **New** \> **Tab** to add a new control that is named **FormTabControl1**.</span></span>
4. <span data-ttu-id="a7bdd-140">في مصمم النماذج، حدد **FormTabControl1**.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-140">In the form designer, select **FormTabControl1**.</span></span>
5. <span data-ttu-id="a7bdd-141">انقر بزر الماوس الأيمن، ثم حدد **صفحة علامة تبويب جديدة** لإضافة صفحة علامة تبويب جديدة.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-141">Right-click, and then select **New Tab Page** to add a new tab page.</span></span>
6. <span data-ttu-id="a7bdd-142">أعد تسمية صفحة علامة التبويب باسم ذي مغزى، مثل **مساحة عمل**.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-142">Rename the tab page to something meaningful, such as **Workspace**.</span></span>
7. <span data-ttu-id="a7bdd-143">في مصمم النماذج، حدد **FormTabControl1**.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-143">In the form designer, select **FormTabControl1**.</span></span>
8. <span data-ttu-id="a7bdd-144">انقر بزر الماوس الأيمن، ثم حدد **صفحة علامة تبويب جديدة**.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-144">Right-click, and then select **New Tab Page**.</span></span>
9. <span data-ttu-id="a7bdd-145">أعد تسمية صفحة علامة التبويب باسم ذي مغزى، مثل **تحليلات**.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-145">Rename the tab page to something meaningful, such as **Analytics**.</span></span>
10. <span data-ttu-id="a7bdd-146">في مصمم النماذج، حدد **التحليلات (صفحة علامة التبويب)**.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-146">In the form designer, select **Analytics (Tab Page)**.</span></span>
11. <span data-ttu-id="a7bdd-147">عيّن خاصية **التسمية التوضيحية** إلى **التحليلات**.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-147">Set the **Caption** property to **Analytics**.</span></span>
12. <span data-ttu-id="a7bdd-148">انقر بزر الماوس الأيمن فوق عنصر التحكم، ثم حدد **جديد‏‎** \> **مجموعة** لإضافة عنصر تحكم مجموعة نماذج جديدة.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-148">Right-click the control, and then select **New** \> **Group** to add a new form group control.</span></span>
13. <span data-ttu-id="a7bdd-149">أعد تسمية مجموعة النماذج باسم ذي مغزى، مثل **powerBIReportGroup**.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-149">Rename the form group to something meaningful, such as **powerBIReportGroup**.</span></span>
14. <span data-ttu-id="a7bdd-150">في مصمم النماذج، حدد **PanoramaBody (علامة التبويب)**، ثم قم بسحب عنصر التحكم إلى علامة تبويب **مساحة العمل**.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-150">In the form designer, select **PanoramaBody (Tab)**, and then drag the control onto the **Workspace** tab.</span></span>
15. <span data-ttu-id="a7bdd-151">في تعريف التصميم، حدد العنصر العلوي المسمى **تصميم | نمط: تشغيلي في مساحة العمل**.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-151">In the design definition, select the top element that is labeled **Design | Pattern: Workspace Operational**.</span></span>
16. <span data-ttu-id="a7bdd-152">انقر بزر الماوس الأيمن، ثم حدد **إزالة النقش**.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-152">Right-click, and then select **Remove pattern**.</span></span>
17. <span data-ttu-id="a7bdd-153">انقر بزر الماوس الأيمن مرة أخرى، ثم حدد **إضافة نمط** \> **مساحة عمل مبوبة**.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-153">Right-click again, and then select **Add pattern** \> **Workspace Tabbed**.</span></span>
18. <span data-ttu-id="a7bdd-154">نفّذ عملية إنشاء للتحقق من التغييرات التي أجريتها.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-154">Perform a build to verify your changes.</span></span>

<span data-ttu-id="a7bdd-155">يبين الرسم التوضيحي التالي الشكل الذي يتخذه التصميم بعد تطبيق هذه التغييرات.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-155">The following illustration shows what the design looks like after these changes are applied.</span></span>

![FMClerkWorkspace بعد التغييرات](media/analytical-workspace-definition-after.png)

<span data-ttu-id="a7bdd-157">والآن بعد أن قمت بإضافة عناصر تحكم النموذج التي سيتم استخدامها لتضمين تقرير مساحة العمل، يجب تحديد حجم عنصر التحكم الأصل بحيث يستوعب التخطيط.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-157">Now that you've added the form controls that will be used to embed the workspace report, you must define the size of the parent control so that it accommodates the layout.</span></span> <span data-ttu-id="a7bdd-158">بشكل افتراضي، سوف تظهر في التقرير الصفحة **"جزء عوامل تصفية"** والصحفة **علامة التبويب**.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-158">By default, both the **Filters Pane** page and the **Tab** page will be visible on the report.</span></span> <span data-ttu-id="a7bdd-159">ومع ذلك، يمكنك تغيير كيفية ظهور عناصر التحكم هذه بما يتناسب مع المستخدم المستهدف للتقرير.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-159">However, you can change the visibility of these controls as appropriate for the target consumer of the report.</span></span>

> [!NOTE]
> <span data-ttu-id="a7bdd-160">بالنسبة إلى مساحات العمل المضمنة، نوصي باستخدام الملحقات لإخفاء الصفحتين **"جزء عوامل تصفية"** و**علامة التبويب**، لتوفير التناسق.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-160">For embedded workspaces, we recommend that you use extensions to hide both the **Filters Pane** and **Tab** pages, for consistency.</span></span>

<span data-ttu-id="a7bdd-161">لقد أتممت الآن مهمة توسيع تعريف نموذج التطبيق.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-161">You've now completed the task of extending the application form definition.</span></span> <span data-ttu-id="a7bdd-162">للحصول على مزيد من المعلومات حول كيفية استخدام الملحقات لإجراء التخصيصات، راجع [التخصيص من خلال تراكب الطبقات والملحقات](../extensibility/customization-overlayering-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="a7bdd-162">For more information about how to use extensions to do customizations, see [Customize through extension and overlayering](../extensibility/customization-overlayering-extensions.md).</span></span>

## <a name="add-x-business-logic-to-embed-a-viewer-control"></a><span data-ttu-id="a7bdd-163">إضافة منطق تسلسل العمل X++ لتضمين عنصر تحكم العارض</span><span class="sxs-lookup"><span data-stu-id="a7bdd-163">Add X++ business logic to embed a viewer control</span></span>
<span data-ttu-id="a7bdd-164">اتبع هذه الخطوات لإضافة منطق تسلسل العمل الذي يقوم بتهيئة عنصر تحكم العارض المضمن في مساحة عمل **إدارة الحجز**.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-164">Follow these steps to add business logic that initializes the report viewer control that is embedded in the **Reservation management** workspace.</span></span>

1. <span data-ttu-id="a7bdd-165">افتح مصمم النماذج **FMClerkWorkspace** لتوسيع تعريف التصميم.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-165">Open the **FMClerkWorkspace** form designer to extend the design definition.</span></span>
2. <span data-ttu-id="a7bdd-166">اضغط F7 للوصول إلى التعليمات البرمجية خلف تعريف التعليمات البرمجية.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-166">Press F7 to access the code behind the code definition.</span></span>
3. <span data-ttu-id="a7bdd-167">أضف التعليمات البرمجية X++ التالية.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-167">Add the following X++ code.</span></span>

    ```
    [Form] 
    public class FMClerkWorkspace extends FormRun
    {
        private boolean initReportControl = true;
        protected void initAnalyticalReport()
        {
            if (!initReportControl)
            {
                return;
            }
            // Note: secure entry point into the Workspace's Analytics report
            if (Global::hasMenuItemAccess(menuItemDisplayStr(FMClerkWorkspace), MenuItemType::Display))
            {
                // initialize the PBI report control using shared helper
                PBIReportHelper::initializeReportControl('FMPBIWorkspaces', powerBIReportGroup);
            }
            initReportControl = false;
        }
        /// <summary>
        /// Initializes the form.
        /// </summary>
        public void init()
        {
            super();
            this.initAnalyticalReport();
        }
    }
    ```

4. <span data-ttu-id="a7bdd-168">نفّذ عملية إنشاء للتحقق من التغييرات التي أجريتها.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-168">Perform a build to verify your changes.</span></span>

<span data-ttu-id="a7bdd-169">لقد أتممت الآن مهمة إضافة منطق تسلسل العمل لتهيئة عنصر تحكم عارض التقرير المضمن.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-169">You've now completed the task of adding business logic to initialize the embedded report viewer control.</span></span> <span data-ttu-id="a7bdd-170">يبين الرسم التوضيحي التالي الشكل الذي تتخذه مساحة العمل بعد تطبيق هذه التغييرات.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-170">The following illustration shows what the workspace looks like after these changes are applied.</span></span>

![تقرير مضمن في مساحة العمل](media/analytical-workspace-final.png)

> [!NOTE]
> <span data-ttu-id="a7bdd-172">يمكنك الوصول إلى طريقة العرض التشغيلية الموجودة باستخدام علامات تبويب مساحة العمل تحت عنوان الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-172">You can access the existing operational view by using the workspace tabs below the page title.</span></span>

## <a name="reference"></a><span data-ttu-id="a7bdd-173">المرجع</span><span class="sxs-lookup"><span data-stu-id="a7bdd-173">Reference</span></span>

### <a name="pbireporthelperinitializereportcontrol-method"></a><span data-ttu-id="a7bdd-174">أسلوب PBIReportHelper.initializeReportControl</span><span class="sxs-lookup"><span data-stu-id="a7bdd-174">PBIReportHelper.initializeReportControl method</span></span>
<span data-ttu-id="a7bdd-175">يوفر هذا المقطع معلومات حول فئة المساعد التي تُستخدم لتضمين تقرير Power BI (مورد pbix.) في عنصر تحكم مجموعة النماذج.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-175">This section provides information about the helper class that is used to embed a Power BI report (.pbix resource) in a form group control.</span></span>

#### <a name="syntax"></a><span data-ttu-id="a7bdd-176">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="a7bdd-176">Syntax</span></span>
```
public static void initializeReportControl(
    str                 _resourceName,
    FormGroupControl    _formGroupControl,
    str                 _defaultPageName = '',
    boolean             _showFilterPane = false,
    boolean             _showNavPane = false,
    List                _defaultFilters = new List(Types::Class))
```

#### <a name="parameters"></a><span data-ttu-id="a7bdd-177">المحددات</span><span class="sxs-lookup"><span data-stu-id="a7bdd-177">Parameters</span></span>

| <span data-ttu-id="a7bdd-178">الاسم</span><span class="sxs-lookup"><span data-stu-id="a7bdd-178">Name</span></span>             | <span data-ttu-id="a7bdd-179">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="a7bdd-179">Description</span></span>                                                                                                  |
|------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7bdd-180">resourceName</span><span class="sxs-lookup"><span data-stu-id="a7bdd-180">resourceName</span></span>     | <span data-ttu-id="a7bdd-181">اسم مورد pbix.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-181">The name of the .pbix resource.</span></span>                                                                              |
| <span data-ttu-id="a7bdd-182">formGroupControl</span><span class="sxs-lookup"><span data-stu-id="a7bdd-182">formGroupControl</span></span> | <span data-ttu-id="a7bdd-183">عنصر تحكم مجموعة النماذج لتطبيق عنصر تحكم تقرير Power BI عليه.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-183">The form group control to apply the Power BI report control to.</span></span>                                              |
| <span data-ttu-id="a7bdd-184">defaultPageName</span><span class="sxs-lookup"><span data-stu-id="a7bdd-184">defaultPageName</span></span>  | <span data-ttu-id="a7bdd-185">اسم الصفحة الافتراضية</span><span class="sxs-lookup"><span data-stu-id="a7bdd-185">The default page name.</span></span>                                                                                       |
| <span data-ttu-id="a7bdd-186">showFilterPane</span><span class="sxs-lookup"><span data-stu-id="a7bdd-186">showFilterPane</span></span>   | <span data-ttu-id="a7bdd-187">قيمة منطقية تشير إلى ما إذا كان يجب عرض جزء عامل التصفية (**true**) أو إخفاؤه (**false**).</span><span class="sxs-lookup"><span data-stu-id="a7bdd-187">A Boolean value that indicates whether the filter pane should be shown (**true**) or hidden (**false**).</span></span>     |
| <span data-ttu-id="a7bdd-188">showNavPane</span><span class="sxs-lookup"><span data-stu-id="a7bdd-188">showNavPane</span></span>      | <span data-ttu-id="a7bdd-189">قيمة منطقية تشير إلى ما إذا كان يجب عرض جزء التنقل (**true**) أو إخفاؤه (**false**).</span><span class="sxs-lookup"><span data-stu-id="a7bdd-189">A Boolean value that indicates whether the navigation pane should be shown (**true**) or hidden (**false**).</span></span> |
| <span data-ttu-id="a7bdd-190">defaultFilters</span><span class="sxs-lookup"><span data-stu-id="a7bdd-190">defaultFilters</span></span>   | <span data-ttu-id="a7bdd-191">عوامل التصفية الافتراضية لتقرير Power BI.</span><span class="sxs-lookup"><span data-stu-id="a7bdd-191">The default filters for the Power BI report.</span></span>                                                                 |
