---
title: تضمين تطبيقات الجهات الخارجية
description: يشرح هذا الموضوع كيفية تضمين تطبيقات الجهات الخارجية لزيادة وظائف المنتج.
author: jasongre
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, UserWorkspaceAdd, UserWorkspaceConfigureWebsite
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2021-04-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d348683e0a2ed35f26830a6ce05c0bf9ca5970bd
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944818"
---
# <a name="embed-third-party-apps"></a><span data-ttu-id="73ce5-103">تضمين تطبيقات الجهات الخارجية</span><span class="sxs-lookup"><span data-stu-id="73ce5-103">Embed third-party apps</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="73ce5-104">يستخدم العديد من العملاء مجموعة من التطبيقات لإدارة أعمالهم.</span><span class="sxs-lookup"><span data-stu-id="73ce5-104">Many customers use a range of applications to run their business.</span></span> <span data-ttu-id="73ce5-105">بعض هذه التطبيقات هي تطبيقات ويب تابعة لجهات خارجية تعمل جنبًا إلى جنب مع تطبيقات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="73ce5-105">Some of those applications are third-party web apps that work in conjunction with Finance and Operations apps.</span></span> <span data-ttu-id="73ce5-106">لتوفير تجربة مستخدم أكثر سلاسة، يمكنك استخدام ميزة **(إصدار أولي) تطبيقات الصفحة الكاملة** لتضمين تطبيقات الجهات الخارجية مباشرةً في تطبيقات Finance and Operations (شريطة أن تسمح تطبيقات الجهات الخارجية بأن تكون مضمنة).</span><span class="sxs-lookup"><span data-stu-id="73ce5-106">To provide a more seamless user experience, you can use the **(Preview) Full page apps** feature to embed those third-party apps directly into your Finance and Operations apps (provided that the third-party apps allow themselves to be embedded).</span></span> <span data-ttu-id="73ce5-107">بهذه الطريقة، يمكن للمستخدمين الوصول إلى مواقع الويب والتطبيقات التي يحتاجون إليها دون الحاجة إلى تبديل علامات التبويب أو النوافذ.</span><span class="sxs-lookup"><span data-stu-id="73ce5-107">In this way, users can access the websites and apps that they require without having to switch tabs or windows.</span></span>

<span data-ttu-id="73ce5-108">قبل أن تتمكن من تضمين تطبيقات الجهات الخارجية في المنتج، يجب عليك تشغيل ميزة **(إصدار أولي) تطبيقات الصفحة الكاملة** في إدارة الميزات.</span><span class="sxs-lookup"><span data-stu-id="73ce5-108">Before you can embed third-party apps into the product, you must turn on the **(Preview) Full page apps** feature in Feature management.</span></span> <span data-ttu-id="73ce5-109">يمكنك بعد ذلك استخدام إحدى الطرق التالية لتضمين تطبيق أو موقع ويب تابع لجهة خارجية.</span><span class="sxs-lookup"><span data-stu-id="73ce5-109">You can then use one of the following methods to embed a third-party app or website.</span></span> <span data-ttu-id="73ce5-110">تشبه هذه الطرق الطرق المستخدمة لتضمين تطبيقات اللوحة من Microsoft Power Apps في تطبيقات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="73ce5-110">These methods are analogous to the methods that are used to embed canvas apps from Microsoft Power Apps into Finance and Operations apps.</span></span>

- <span data-ttu-id="73ce5-111">قم بتضمين التطبيق أو موقع الويب في صفحة موجودة كصفحة علامة تبويب جديدة (علامة التبويب المحورية أو علامة التبويب السريعة أو الشفرة أو قسم مساحة العمل).</span><span class="sxs-lookup"><span data-stu-id="73ce5-111">Embed the app or website on an existing page as a new tab page (pivot tab, FastTab, blade, or workspace section).</span></span>
- <span data-ttu-id="73ce5-112">أنشئ تجربة صفحة كاملة جديدة للتطبيق أو موقع الويب من لوحة المعلومات.</span><span class="sxs-lookup"><span data-stu-id="73ce5-112">Create a new full-page experience for the app or website from the dashboard.</span></span>

## <a name="embed-a-website-on-an-existing-page"></a><span data-ttu-id="73ce5-113">تضمين موقع ويب علي صفحه موجودة</span><span class="sxs-lookup"><span data-stu-id="73ce5-113">Embed a website on an existing page</span></span>

<span data-ttu-id="73ce5-114">استخدم هذا الاجراء إذا كنت ترغب في أضافه صفحه موجودة في النظام مع تطبيق مضمن.</span><span class="sxs-lookup"><span data-stu-id="73ce5-114">Use this procedure if you want to supplement an existing page in the system with an embedded app.</span></span>

1. <span data-ttu-id="73ce5-115">افتح الصفحة حيث تريد تضمين التطبيق.</span><span class="sxs-lookup"><span data-stu-id="73ce5-115">Open the page where you want to embed the app.</span></span>
2. <span data-ttu-id="73ce5-116">افتح جزء **إضافة تطبيق**:</span><span class="sxs-lookup"><span data-stu-id="73ce5-116">Open the **Add an app** pane:</span></span>

    1. <span data-ttu-id="73ce5-117">حدد **الإعدادات** ثم **تخصيص** لفتح شريط أدوات **التخصيص**.</span><span class="sxs-lookup"><span data-stu-id="73ce5-117">Select **Settings** and then **Personalize** to open the **Personalization** toolbar.</span></span>
    2. <span data-ttu-id="73ce5-118">حدد **المزيد \> إضافة تطبيق**.</span><span class="sxs-lookup"><span data-stu-id="73ce5-118">Select **More \> Add an app**.</span></span>

3. <span data-ttu-id="73ce5-119">حدد منطقة الصفحة حيث تريد إضافة التطبيق.</span><span class="sxs-lookup"><span data-stu-id="73ce5-119">Select the region of the page where you want to add the app.</span></span> <span data-ttu-id="73ce5-120">يجب أن تكون هذه المنطقة *حاوية علامة التبويب* لعلامة تبويب محورية أو علامة تبويب سريعة أو شفرة أو قسم مساحة عمل.</span><span class="sxs-lookup"><span data-stu-id="73ce5-120">This region must be a *tab container* for a pivot tab, FastTab, blade, or workspace section.</span></span>
4. <span data-ttu-id="73ce5-121">حدد **موقع ويب**.</span><span class="sxs-lookup"><span data-stu-id="73ce5-121">Select **Website**.</span></span>
5. <span data-ttu-id="73ce5-122">تكوين التطبيق المضمن:</span><span class="sxs-lookup"><span data-stu-id="73ce5-122">Configure the embedded app:</span></span>

    - <span data-ttu-id="73ce5-123">**الاسم** – أدخل النص الذي يجب أن يظهر لعلامة التبويب التي تحتوي على التطبيق المضمن.</span><span class="sxs-lookup"><span data-stu-id="73ce5-123">**Name** – Enter the text that should be shown for the tab that contains the embedded app.</span></span> <span data-ttu-id="73ce5-124">في كثير من الأحيان، سترغب في أن يكون هذا النص هو اسم التطبيق.</span><span class="sxs-lookup"><span data-stu-id="73ce5-124">Often, you will want this text to be the name of the app.</span></span>
    - <span data-ttu-id="73ce5-125">**URL** – حدد موقع التطبيق.</span><span class="sxs-lookup"><span data-stu-id="73ce5-125">**URL** – Specify the location of the app.</span></span>

    > [!IMPORTANT]
    > - <span data-ttu-id="73ce5-126">لأسباب تتعلق بالأمان، يجب أن يستخدم عنوان URL بروتوكول نقل النص التشعبي الآمن (HTTPS).</span><span class="sxs-lookup"><span data-stu-id="73ce5-126">For security reasons, the URL must use Hypertext Transfer Protocol Secure (HTTPS).</span></span>
    > - <span data-ttu-id="73ce5-127">يجب تكوين التطبيق أو موقع الويب بحيث يسمح بتضمين نفسه.</span><span class="sxs-lookup"><span data-stu-id="73ce5-127">The app or website must be configured to allow itself to be embedded.</span></span>

6. <span data-ttu-id="73ce5-128">حدد **حفظ** لتضمين التطبيق علي الصفحة.</span><span class="sxs-lookup"><span data-stu-id="73ce5-128">Select **Save** to embed the app on the page.</span></span> <span data-ttu-id="73ce5-129">تتم أضافه التطبيق كعلامة التبويب أو المقطع الأخير في المجموعة.</span><span class="sxs-lookup"><span data-stu-id="73ce5-129">The app is added as the last tab or section in the group.</span></span>
7. <span data-ttu-id="73ce5-130">تأكد من ظهور التطبيق كما هو متوقع.</span><span class="sxs-lookup"><span data-stu-id="73ce5-130">Confirm that the app appears as expected.</span></span> <span data-ttu-id="73ce5-131">إذا لم يتم عرض التطبيق، فراجع قسم [استكشاف الأخطاء وإصلاحها](#troubleshooting) لاحقًا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="73ce5-131">If the app isn't rendered, see the [Troubleshooting](#troubleshooting) section later in this topic.</span></span>
8. <span data-ttu-id="73ce5-132">افتح محدد العرض، وحدد إما **حفظ** (إذا كان يجب إقران التطبيق بالملف الشخصي الحالي) أو **حفظ باسم** (لحفظ التطبيق في طريقة عرض مختلفة).</span><span class="sxs-lookup"><span data-stu-id="73ce5-132">Open the view selector, and select either **Save** (if the app should be associated with the current view) or **Save as** (to save the app to a different view).</span></span>

    <span data-ttu-id="73ce5-133">إذا لم يكن للصفحة محدد عرض (على سبيل المثال، إذا كانت الصفحة عبارة عن مربع حوار أو مساحة عمل)، فيمكنك تخطي هذه الخطوة.</span><span class="sxs-lookup"><span data-stu-id="73ce5-133">If the page doesn't have a view selector (for example, if the page is a dialog box or a workspace), you can skip this step.</span></span>

## <a name="embed-a-website-as-a-full-page-experience-from-the-dashboard"></a><span data-ttu-id="73ce5-134">تضمين موقع ويب كتجربة صفحة كاملة من لوحة المعلومات</span><span class="sxs-lookup"><span data-stu-id="73ce5-134">Embed a website as a full-page experience from the dashboard</span></span>

<span data-ttu-id="73ce5-135">استخدم هذا الإجراء إذا لم يكن التطبيق الذي تريد تضمينه مرتبطًا بصفحة موجودة، أو إذا كنت تريد فقط تجربة صفحة كاملة للتطبيق داخل تطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="73ce5-135">Use this procedure if the app that you want to embed isn't related to an existing page, or if you just want a full-page experience for the app inside the Finance and Operations app.</span></span>

1. <span data-ttu-id="73ce5-136">افتح لوحة المعلومات.</span><span class="sxs-lookup"><span data-stu-id="73ce5-136">Open the dashboard.</span></span>
2. <span data-ttu-id="73ce5-137">حدد مع الاستمرار (أو انقر بزر الماوس الأيمن) على الصفحة، وحدد **تشخيص**، ثم حدد **إضافة صفحة**.</span><span class="sxs-lookup"><span data-stu-id="73ce5-137">Select and hold (or right-click) the page, select **Personalize**, and then select **Add a page**.</span></span>
3. <span data-ttu-id="73ce5-138">في جزء **إضافة صفحة**، حدد **موقع الويب**.</span><span class="sxs-lookup"><span data-stu-id="73ce5-138">In the **Add a page** pane, select **Website**.</span></span>
4. <span data-ttu-id="73ce5-139">تكوين التطبيق المضمن:</span><span class="sxs-lookup"><span data-stu-id="73ce5-139">Configure the embedded app:</span></span>

    - <span data-ttu-id="73ce5-140">**الاسم** – أدخل النص الذي يجب أن يظهر على اللوحة التي تمت إضافتها للتطبيق المضمن في لوحة المعلومات.</span><span class="sxs-lookup"><span data-stu-id="73ce5-140">**Name** – Enter the text that should be shown on the tile that is added for the embedded app on the dashboard.</span></span> <span data-ttu-id="73ce5-141">في كثير من الأحيان، سترغب في أن يكون هذا النص هو اسم التطبيق.</span><span class="sxs-lookup"><span data-stu-id="73ce5-141">Often, you will want this text to be the name of the app.</span></span>
    - <span data-ttu-id="73ce5-142">**URL** – حدد موقع التطبيق.</span><span class="sxs-lookup"><span data-stu-id="73ce5-142">**URL** – Specify the location of the app.</span></span>

    > [!IMPORTANT]
    > - <span data-ttu-id="73ce5-143">لأسباب تتعلق بالأمان، يجب أن يستخدم عنوان URL بروتوكول HTTPS.</span><span class="sxs-lookup"><span data-stu-id="73ce5-143">For security reasons, the URL must use HTTPS.</span></span>
    > - <span data-ttu-id="73ce5-144">يجب تكوين التطبيق أو موقع الويب بحيث يسمح بتضمين نفسه.</span><span class="sxs-lookup"><span data-stu-id="73ce5-144">The app or website must be configured to allow itself to be embedded.</span></span>

5. <span data-ttu-id="73ce5-145">حدد **حفظ** لإضافة التطبيق إلى لوحة القيادة كتجانب جديد.</span><span class="sxs-lookup"><span data-stu-id="73ce5-145">Select **Save** to add the app to the dashboard as a new tile.</span></span>
6. <span data-ttu-id="73ce5-146">حدد التجانب الجديد في لوحة المعلومات، وتأكد من ظهور التطبيق بالشكل المتوقع.</span><span class="sxs-lookup"><span data-stu-id="73ce5-146">Select the new tile on the dashboard, and confirm that the app appears as expected.</span></span> <span data-ttu-id="73ce5-147">إذا لم يتم عرض التطبيق، فراجع قسم [استكشاف الأخطاء وإصلاحها](#troubleshooting) لاحقًا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="73ce5-147">If the app isn't rendered, see the [Troubleshooting](#troubleshooting) section later in this topic.</span></span>

## <a name="sharing-embedded-apps"></a><span data-ttu-id="73ce5-148">مشاركة التطبيقات المضمنة</span><span class="sxs-lookup"><span data-stu-id="73ce5-148">Sharing embedded apps</span></span>

<span data-ttu-id="73ce5-149">بعد قيامك بتضمين تطبيق باستخدام إحدى الطرق الموضحة في الأقسام السابقة، قد ترغب في مشاركة طريقة العرض مع مستخدمين آخرين في النظام.</span><span class="sxs-lookup"><span data-stu-id="73ce5-149">After you've embedded an app by using one of the methods that are described in the previous sections, you might want to share the view with other users in the system.</span></span> <span data-ttu-id="73ce5-150">لمشاركة تطبيق مضمن، استخدم إحدى الطرق التالية:</span><span class="sxs-lookup"><span data-stu-id="73ce5-150">To share an embedded app, use one of the following methods:</span></span>

- <span data-ttu-id="73ce5-151">**نشر طريقة العرض (مستحسن):** إذا تم حفظ التطبيق المضمن في طريقة عرض، فإن الطريقة الموصى بها والمفضلة لمشاركته هي نشر العرض للمستخدمين الذين لديهم أدوار الأمان المناسبة.</span><span class="sxs-lookup"><span data-stu-id="73ce5-151">**Publish the view (Recommended):** If the embedded app has been saved to a view, the recommended and preferred way to share it is to publish the view to users who have the appropriate security roles.</span></span> <span data-ttu-id="73ce5-152">بعد ذلك، سيرى جميع المستخدمين الذين لديهم أدوار الأمان التي تستهدفها طريقة العرض المنشورة التطبيق في تطبيقات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="73ce5-152">Then, all users who have the security roles that are targeted by the published view will see the app in Finance and Operations apps.</span></span> <span data-ttu-id="73ce5-153">لمزيد من المعلومات حول كيفية نشر طريقة عرض، راجع [نشر طرق العرض](saved-views.md#publishing-views).</span><span class="sxs-lookup"><span data-stu-id="73ce5-153">For more information about how to publish a view, see [Publishing views](saved-views.md#publishing-views).</span></span>

    <span data-ttu-id="73ce5-154">يمكنك أيضًا نشر تطبيق تم تضمينه كتجربة صفحة كاملة من لوحة المعلومات.</span><span class="sxs-lookup"><span data-stu-id="73ce5-154">You can also publish an app that has been embedded as a full-page experience from the dashboard.</span></span> <span data-ttu-id="73ce5-155">في لوحة المعلومات، حدد باستمرار (أو انقر بزر الماوس الأيمن) فوق التجانب المرتبط بالتطبيق، وحدد **تخصيص**، ثم حدد **نشر صفحة**.</span><span class="sxs-lookup"><span data-stu-id="73ce5-155">On the dashboard, select and hold (or right-click) the tile that is associated with the app, select **Personalize**, and then select **Publish page**.</span></span> <span data-ttu-id="73ce5-156">حاليًا، يمكنك النشر لأدوار الأمان فقط.</span><span class="sxs-lookup"><span data-stu-id="73ce5-156">Currently, you can publish only to security roles.</span></span> <span data-ttu-id="73ce5-157">ومع ذلك، ستتم إضافة القدرة على النشر إلى الكيانات القانونية قبل أن تصبح الميزة متاحة بشكل عام.</span><span class="sxs-lookup"><span data-stu-id="73ce5-157">However, the capability to publish to legal entities will be added before the feature becomes generally available.</span></span>

- <span data-ttu-id="73ce5-158">**نسخ التخصيص:** بالنسبة للصفحات التي لا تدعم طرق العرض (على سبيل المثال، مربعات الحوار أو مساحات العمل)، أو لتجربة تطبيق الصفحة الكاملة، يمكنك نسخ التخصيص إلى المستخدمين المناسبين.</span><span class="sxs-lookup"><span data-stu-id="73ce5-158">**Copy the personalization:** For pages that don't support views (for example, dialog boxes or workspaces), or for the full-page app experience, you can copy the personalization to the appropriate users.</span></span> <span data-ttu-id="73ce5-159">لمزيد من المعلومات، راجع [مشاركة التخصيصات](personalize-user-experience.md#sharing-personalizations).</span><span class="sxs-lookup"><span data-stu-id="73ce5-159">For more information, see [Sharing personalizations](personalize-user-experience.md#sharing-personalizations).</span></span>

## <a name="viewing-embedded-apps"></a><span data-ttu-id="73ce5-160">عرض التطبيقات المضمنة</span><span class="sxs-lookup"><span data-stu-id="73ce5-160">Viewing embedded apps</span></span>

<span data-ttu-id="73ce5-161">لعرض تطبيق مضمن على صفحة في تطبيقات Finance and Operations، افتح الصفحة التي تحتوي على التطبيق المضمن.</span><span class="sxs-lookup"><span data-stu-id="73ce5-161">To view an embedded app on a page in Finance and Operations apps, open the page that has the embedded app.</span></span> <span data-ttu-id="73ce5-162">تذكر أنه في بعض الصفحات، يمكن الوصول إلى التطبيقات المضمنة باستخدام زر **Power Apps** في جزء الإجراءات القياسي.</span><span class="sxs-lookup"><span data-stu-id="73ce5-162">Remember that, on some pages, embedded apps can be accessed by using the **Power Apps** button on the standard Action Pane.</span></span> <span data-ttu-id="73ce5-163">بدلاً من ذلك، قد تظهر مباشرةً على الصفحة كعلامة تبويب جديدة أو علامة تبويب سريعة أو شفرة نصية أو كقسم جديد في مساحة العمل.</span><span class="sxs-lookup"><span data-stu-id="73ce5-163">Alternatively, they might appear directly on the page as a new tab, FastTab, or blade, or as a new section in a workspace.</span></span>

## <a name="editing-or-removing-embedded-apps"></a><span data-ttu-id="73ce5-164">تحرير أو إزالة التطبيقات المضمنة</span><span class="sxs-lookup"><span data-stu-id="73ce5-164">Editing or removing embedded apps</span></span>

<span data-ttu-id="73ce5-165">بعد أن يتم تضمين التطبيق في الصفحة، قد تضطر إلى تعديل التكوين الخاص به (على سبيل المثال، عن طريق تغيير تسمية القسم أو عنوان URL).</span><span class="sxs-lookup"><span data-stu-id="73ce5-165">After an app has been embedded on a page, you might have to edit its configuration (for example, by changing the section label or the URL).</span></span> <span data-ttu-id="73ce5-166">بدلاً من ذلك، قد تضطر إلى إزالته من الصفحة.</span><span class="sxs-lookup"><span data-stu-id="73ce5-166">Alternatively, you might have to remove it from the page.</span></span> <span data-ttu-id="73ce5-167">استخدم أحد الإجراءات التالية لتحرير تكوين تطبيق مضمن أو إزالته بالكامل.</span><span class="sxs-lookup"><span data-stu-id="73ce5-167">Use one of the following procedures to edit the configuration of an embedded app or remove it completely.</span></span>

### <a name="apps-that-are-embedded-on-existing-pages"></a><span data-ttu-id="73ce5-168">التطبيقات المضمنة في صفحات موجودة</span><span class="sxs-lookup"><span data-stu-id="73ce5-168">Apps that are embedded on existing pages</span></span>

1. <span data-ttu-id="73ce5-169">افتح الصفحة حيث تم تضمين التطبيق.</span><span class="sxs-lookup"><span data-stu-id="73ce5-169">Open the page where the app is embedded.</span></span>
2. <span data-ttu-id="73ce5-170">حدد **الإعدادات** ثم **تخصيص** لفتح شريط أدوات **التخصيص**.</span><span class="sxs-lookup"><span data-stu-id="73ce5-170">Select **Settings** and then **Personalize** to open the **Personalization** toolbar.</span></span>
3. <span data-ttu-id="73ce5-171">حدد أداة **التحديد**، ثم حدد التطبيق المضمن.</span><span class="sxs-lookup"><span data-stu-id="73ce5-171">Select the **Select** tool, and then select the embedded app.</span></span>
4. <span data-ttu-id="73ce5-172">لتحرير التطبيق، قم بإجراء التغييرات المطلوبة على تكوينه، ثم حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="73ce5-172">To edit the app, make the required changes to its configuration, and then select **Save**.</span></span>

    <span data-ttu-id="73ce5-173">أو بدلاً من ذلك، لإزالة التطبيق، حدد **حذف**.</span><span class="sxs-lookup"><span data-stu-id="73ce5-173">Alternatively, to remove the app, select **Delete**.</span></span>

5. <span data-ttu-id="73ce5-174">أعد حفظ أو أعد نشر طريقة العرض.</span><span class="sxs-lookup"><span data-stu-id="73ce5-174">Re-save or republish the view.</span></span> <span data-ttu-id="73ce5-175">لاحظ أنه إذا غادرت الصفحة بدون حفظ العرض بشكل صريح، فلن يتم حفظ أي من الإجراءات التي قمت بتنفيذها في جزء **تحرير موقع الويب**.</span><span class="sxs-lookup"><span data-stu-id="73ce5-175">Note that if you leave the page without explicitly saving the view, none of the actions that you performed in the **Edit website** pane will be maintained.</span></span>

### <a name="apps-that-are-embedded-from-the-dashboard"></a><span data-ttu-id="73ce5-176">التطبيقات المضمنة من لوحة المعلومات</span><span class="sxs-lookup"><span data-stu-id="73ce5-176">Apps that are embedded from the dashboard</span></span>

1. <span data-ttu-id="73ce5-177">افتح لوحة المعلومات.</span><span class="sxs-lookup"><span data-stu-id="73ce5-177">Open the dashboard.</span></span>
2. <span data-ttu-id="73ce5-178">حدد مع الاستمرار (أو انقر بزر الماوس الأيمن) على المربع المرتبط بالتطبيق المضمن، ثم حدد **تخصيص**.</span><span class="sxs-lookup"><span data-stu-id="73ce5-178">Select and hold (or right-click) the tile that is associated with the embedded app, and then select **Personalize**.</span></span>
3. <span data-ttu-id="73ce5-179">لتحرير التطبيق، حدد **تحرير الصفحة**.</span><span class="sxs-lookup"><span data-stu-id="73ce5-179">To edit the app, select **Edit page**.</span></span> <span data-ttu-id="73ce5-180">في جزء **تحرير موقع الويب**، قم بإجراء التغييرات المطلوبة على تكوين التطبيق، ثم حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="73ce5-180">In the **Edit website** pane, make the required changes to the app configuration, and then select **Save**.</span></span>

    <span data-ttu-id="73ce5-181">بدلاً من ذلك، لإزالة التطبيق، حدد **إزالة صفحة**.</span><span class="sxs-lookup"><span data-stu-id="73ce5-181">Alternatively, to remove the app, select **Remove page**.</span></span>

## <a name="appendix"></a><span data-ttu-id="73ce5-182">الملحق</span><span class="sxs-lookup"><span data-stu-id="73ce5-182">Appendix</span></span>

### <a name="troubleshooting"></a><span data-ttu-id="73ce5-183">استكشاف الأخطاء وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="73ce5-183">Troubleshooting</span></span>

<span data-ttu-id="73ce5-184">إذا لم يتم عرض موقع الويب بشكل صحيح بعد تضمينه في تطبيق Finance and Operation، أو إذا تلقيت رسالة خطأ تنص على أن عنوان URL قد تم رفض الاتصال به، فمن المحتمل أن يكون موقع الويب قد تم تكوينه لمنع نفسه من التضمين في iframe.</span><span class="sxs-lookup"><span data-stu-id="73ce5-184">If a website isn't rendered correctly after it's embedded in a Finance and Operation app, or if you receive an error message that states that the URL was denied a connection, the website is probably configured to prevent itself from being embedded in an iframe.</span></span> <span data-ttu-id="73ce5-185">اتبع هذه الخطوات لتحديد ما إذا كان يمكن تضمين موقع الويب.</span><span class="sxs-lookup"><span data-stu-id="73ce5-185">Follow these steps to determine whether the website can be embedded.</span></span>

1. <span data-ttu-id="73ce5-186">افتح أدوات المطور للمتصفح الذي تستخدمه.</span><span class="sxs-lookup"><span data-stu-id="73ce5-186">Open the developer tools for the browser that you're using.</span></span>
2. <span data-ttu-id="73ce5-187">في علامة تبويب **الشبكة**، ابحث عن الاستجابة وحددها من الموقع المضمن.</span><span class="sxs-lookup"><span data-stu-id="73ce5-187">On the **Network** tab, find and select the response from the embedded site.</span></span>
3. <span data-ttu-id="73ce5-188">في علامة التبويب **الرؤوس**، ضمن **رؤوس الاستجابة**، ابحث عن **x-frame-options**.</span><span class="sxs-lookup"><span data-stu-id="73ce5-188">On the **Headers** tab, under **Response Headers**, look for **x-frame-options**.</span></span> <span data-ttu-id="73ce5-189">إذا كان **x-frame-options** موجودًا في رؤوس الاستجابة، ويشتمل على قيمة **DENY** أو **SAMEORIGIN**، لا يمكن تضمين موقع الويب حاليًا.</span><span class="sxs-lookup"><span data-stu-id="73ce5-189">If **x-frame-options** exists in the response headers, and has a value of **DENY** or **SAMEORIGIN**, the website can't currently be embedded.</span></span> <span data-ttu-id="73ce5-190">سيتعين عليك العمل مع مالك التطبيق لتمكينه من التضمين بأمان.</span><span class="sxs-lookup"><span data-stu-id="73ce5-190">You will have to work with the owner of the app to enable it to be safely embedded.</span></span>

### <a name="developer-modeling-a-website-on-a-form"></a><span data-ttu-id="73ce5-191">[المطور] نمذجة موقع ويب في نموذج</span><span class="sxs-lookup"><span data-stu-id="73ce5-191">[Developer] Modeling a website on a form</span></span>

<span data-ttu-id="73ce5-192">على الرغم من أن هذا الموضوع يركز على تضمين تطبيقات الجهات الخارجية أو مواقع الويب من خلال التخصيص، يمكن للمطورين أيضًا تضمينها في نموذج باستخدام تجربة تطوير Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="73ce5-192">Although this topic is focused on embedding third-party apps or websites through personalization, developers can also embed them in a form by using the Visual Studio development experience.</span></span> <span data-ttu-id="73ce5-193">أضف فقط عنصر تحكم **WebsiteHostControl** إلى النموذج.</span><span class="sxs-lookup"><span data-stu-id="73ce5-193">Just add a **WebsiteHostControl** control to the form.</span></span> <span data-ttu-id="73ce5-194">توفر خصائص بيانات التعريف المتوفرة لعنصر التحكم نفس الإمكانيات مثل تجربة التخصيص.</span><span class="sxs-lookup"><span data-stu-id="73ce5-194">The metadata properties that are available for the control provide the same capabilities as the personalization experience.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
