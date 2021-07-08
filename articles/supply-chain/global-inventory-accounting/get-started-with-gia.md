---
title: الشروع في العمل في ‏‫محاسبة المخزون العالمي
description: يصف هذا الموضوع كيفية الشروع في العمل مع محاسبة المخزون العالمي.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 59f9db309312bbbc88b4fa47c12c4c02f09e7c6d
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301688"
---
# <a name="get-started-with-global-inventory-accounting"></a><span data-ttu-id="085fb-103">الشروع في العمل في ‏‫محاسبة المخزون العالمي</span><span class="sxs-lookup"><span data-stu-id="085fb-103">Get started with Global Inventory Accounting</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="085fb-104">تتيح لك محاسبة المخزون العالمي إجراء محاسبات متعددة للمخزون في دفاتر الأستاذ العام لمحاسبة المخزون العالمي التي قمت بإعدادها.</span><span class="sxs-lookup"><span data-stu-id="085fb-104">Global Inventory Accounting lets you do multiple inventory accountings in the Global Inventory Accounting ledgers that you've set up.</span></span> <span data-ttu-id="085fb-105">يمكنك إقران كل دفتر أستاذ لمحاسبة المخزون العالمي بـ *اصطلاح*.</span><span class="sxs-lookup"><span data-stu-id="085fb-105">You must associate each Global Inventory Accounting ledger with a *convention*.</span></span> <span data-ttu-id="085fb-106">والاصطلاح هو مجموعة من الأنواع التالية من سياسات المحاسبة:</span><span class="sxs-lookup"><span data-stu-id="085fb-106">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="085fb-107">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="085fb-107">Cost object</span></span>
- <span data-ttu-id="085fb-108">أساس قياس الإدخال</span><span class="sxs-lookup"><span data-stu-id="085fb-108">Input measurement basis</span></span>
- <span data-ttu-id="085fb-109">افتراض تدفق التكلفة</span><span class="sxs-lookup"><span data-stu-id="085fb-109">Cost flow assumption</span></span>
- <span data-ttu-id="085fb-110">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="085fb-110">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="085fb-111">حتى بعد تشغيل خدمة محاسبة المخزون العالمي، ما يزال بإمكانك إجراء محاسبة المخزون في Microsoft Dynamics 365 Supply Chain Management كما هو معتاد.</span><span class="sxs-lookup"><span data-stu-id="085fb-111">Even after you turn on Global Inventory Accounting, you can still do inventory accounting in Microsoft Dynamics 365 Supply Chain Management in the usual way.</span></span>

<span data-ttu-id="085fb-112">تُعد محاسبة المخزون العالمي وظيفة إضافية.</span><span class="sxs-lookup"><span data-stu-id="085fb-112">Global Inventory Accounting is an add-in.</span></span> <span data-ttu-id="085fb-113">ولجعل ميزاتها متوفرة، يجب أن تثبتها من Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="085fb-113">To make its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="085fb-114">يمكنك اختيار تقييمها في بيئة اختبار قبل تشغيلها في بيئات التشغيل.</span><span class="sxs-lookup"><span data-stu-id="085fb-114">You can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="085fb-115">لا تدعم محاسبة المخزون العالمي حاليًا كافة ميزات إدارة التكلفة المضمنة في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="085fb-115">Global Inventory Accounting doesn't currently support all the cost management features that are built into Supply Chain Management.</span></span> <span data-ttu-id="085fb-116">بالتالي، من المهم أن تجري تقييمًا بشأن ما إذا كانت مجموعة الميزات المتوفرة حاليًا ستلبي متطلباتك أم لا.</span><span class="sxs-lookup"><span data-stu-id="085fb-116">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="how-to-get-the-global-inventory-accounting-public-preview"></a><a name="sign-up"></a><span data-ttu-id="085fb-117">كيفية الحصول على إصدار أولي للاستخدام العام لمحاسبة المخزون العالمي</span><span class="sxs-lookup"><span data-stu-id="085fb-117">How to get the Global Inventory Accounting public preview</span></span>

> [!IMPORTANT]
> <span data-ttu-id="085fb-118">لاستخدام محاسبة المخزون العام، يجب أن يكون لديك بيئة عالية التوفر ممكن بها LCS (ليس بيئة OneBox).</span><span class="sxs-lookup"><span data-stu-id="085fb-118">To use Global Inventory Accounting, you must have an LCS-enabled high-availability environment (not a OneBox environment).</span></span> <span data-ttu-id="085fb-119">بالإضافة إلى ذلك، يجب تشغيل Supply Chain Management الإصدار 10.0.19 أو إصدار لاحق.</span><span class="sxs-lookup"><span data-stu-id="085fb-119">Additionally, you must be running Supply Chain Management version 10.0.19 or later.</span></span>

<span data-ttu-id="085fb-120">للتسجيل في الإصدار الأولي للاستخدام العام لمحاسبة المخزون العالمي، قم بإرسال معرف بيئة LCS الخاص بك بالبريد الإلكتروني إلى [فريق محاسبة المخزون العالمي](mailto:GlobalInventoryAccounting@service.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="085fb-120">To sign up for the Global Inventory Accounting public preview, send your LCS environment ID by email to the [Global Inventory Accounting team](mailto:GlobalInventoryAccounting@service.microsoft.com).</span></span> <span data-ttu-id="085fb-121">وبعد الموافقة على البرنامج، سيقوم الفريق بإرسال بريد إلكتروني للمتابعة يحتوي على مفتاح بيتا لمحاسبة المخزون العالمي ونقاط نهاية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="085fb-121">After you're approved for the program, the team will send you a follow-up email that contains a Global Inventory Accounting beta key and your service endpoints.</span></span> <span data-ttu-id="085fb-122">بعد استلام مفتاح بيتا، يمكنك [تثبيت الوظيفة الإضافية](#install).</span><span class="sxs-lookup"><span data-stu-id="085fb-122">After you receive the beta key, you can [install the add-in](#install).</span></span>

## <a name="licensing"></a><span data-ttu-id="085fb-123">الترخيص</span><span class="sxs-lookup"><span data-stu-id="085fb-123">Licensing</span></span>

<span data-ttu-id="085fb-124">يجري ترخيص محاسبة المخزون العالمي معًا مع الميزات القياسية لمحاسبة المخزون المتوفرة لـ Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="085fb-124">Global Inventory Accounting is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="085fb-125">لا يتعين عليك شراء ترخيص إضافي لاستخدام محاسبة المخزون العالمي.</span><span class="sxs-lookup"><span data-stu-id="085fb-125">You don't have to purchase an additional license to use Global Inventory Accounting.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="085fb-126">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="085fb-126">Prerequisites</span></span>

### <a name="set-up-microsoft-power-platform-integration"></a><span data-ttu-id="085fb-127">إعداد تكامل Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="085fb-127">Set up Microsoft Power Platform integration</span></span>

<span data-ttu-id="085fb-128">قبل تمكين وظيفة الوظيفة الإضافية، فإنه يجب التكامل مع Microsoft Power Platform باتباع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="085fb-128">Before you can enable add-in functionality, you must integrate with Microsoft Power Platform by following these steps.</span></span>

1. <span data-ttu-id="085fb-129">افتح بيئة LCS حيث تريد إضافة الخدمة بها.</span><span class="sxs-lookup"><span data-stu-id="085fb-129">Open the LCS environment where you want to add the service.</span></span>
1. <span data-ttu-id="085fb-130">انتقل إلى **التفاصيل الكاملة**.</span><span class="sxs-lookup"><span data-stu-id="085fb-130">Go to **Full details**.</span></span>
1. <span data-ttu-id="085fb-131">في القسم **تكامل Power Platform**، حدد **إعداد**.</span><span class="sxs-lookup"><span data-stu-id="085fb-131">In the **Power Platform Integration** section, select **Setup**.</span></span>
1. <span data-ttu-id="085fb-132">في مربع الحوار **إعداد بيئة Power platform**، حدد خانة الاختيار، ثم حدد **إعداد**</span><span class="sxs-lookup"><span data-stu-id="085fb-132">In the **Power platform environment setup** dialog box, select the checkbox, and then select **Setup**.</span></span> <span data-ttu-id="085fb-133">وعادةً، يستغرق الإعداد بين 60 و90 دقيقة.</span><span class="sxs-lookup"><span data-stu-id="085fb-133">Typically, setup takes between 60 and 90 minutes.</span></span>
1. <span data-ttu-id="085fb-134">بعد اكتمال الإعداد الخاص بالبيئة Microsoft Power Platform، تعرض الصفحة اسم البيئة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="085fb-134">After setup of the Microsoft Power Platform environment is completed, the page shows the name of your environment.</span></span> <span data-ttu-id="085fb-135">بالإضافة إلى ذلك، يعرض القسم تكامل **Power Platform** الكشف و"تم إكمال إعداد البيئة Power Platform".</span><span class="sxs-lookup"><span data-stu-id="085fb-135">Additionally, the **Power Platform Integration** section shows the statement, "Power Platform environment setup is complete."</span></span> <span data-ttu-id="085fb-136">لا تتطلب محاسبة المخزون العالمي تطبيقًا ثنائي الكتابة.</span><span class="sxs-lookup"><span data-stu-id="085fb-136">Global Inventory Accounting doesn't require a dual-write application.</span></span>

<span data-ttu-id="085fb-137">لمزيد من المعلومات، راجع [الإعداد بعد نشر البيئة](../../fin-ops-core/dev-itpro/power-platform/overview.md#set-up-after-environment-deployment).</span><span class="sxs-lookup"><span data-stu-id="085fb-137">For more information, see [Set up after environment deployment](../../fin-ops-core/dev-itpro/power-platform/overview.md#set-up-after-environment-deployment).</span></span>

### <a name="set-up-dataverse"></a><span data-ttu-id="085fb-138">إعداد Dataverse</span><span class="sxs-lookup"><span data-stu-id="085fb-138">Set up Dataverse</span></span>

<span data-ttu-id="085fb-139">قبل إعداد Dataverse، قم بإضافة مبادئ خدمة محاسبة المخزون العالمي إلى المستأجر باتباع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="085fb-139">Before you set up Dataverse, add the Global Inventory Accounting service principles to your tenant by following these steps.</span></span>

1. <span data-ttu-id="085fb-140">قم بتثبيت وحدة Azure AD النمطية لـ Windows PowerShell الإصدار 2 كما هو موضح في [تثبيت Azure Active Directory PowerShell للرسم البياني](/powershell/azure/active-directory/install-adv2).</span><span class="sxs-lookup"><span data-stu-id="085fb-140">Install Azure AD Module for Windows PowerShell v2 as described in [Install Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span></span>
1. <span data-ttu-id="085fb-141">قم بتشغيل الأمر PowerShell التالي.</span><span class="sxs-lookup"><span data-stu-id="085fb-141">Run the following PowerShell command.</span></span>

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)

    New-AzureADServicePrincipal -AppId "7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9" -DisplayName "d365-scm-costaccountingservice"

    New-AzureADServicePrincipal -AppId "5f58fc56-0202-49a8-ac9e-0946b049718b" -DisplayName "d365-scm-operationdataservice"
    ```

<span data-ttu-id="085fb-142">بعد ذلك، قم بإنشاء مستخدمي التطبيق لمحاسبة المخزون العالمي في Dataverse باتباع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="085fb-142">Next, create application users for Global Inventory Accounting in Dataverse by following these steps.</span></span>

1. <span data-ttu-id="085fb-143">افتح عنوان URL الخاص ببيئة Dataverse الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="085fb-143">Open the URL of your Dataverse environment.</span></span>
1. <span data-ttu-id="085fb-144">انتقل إلى **إعدادات متقدمة \> النظام \> الأمان \> المستخدمين**، وقم بإنشاء مستخدم تطبيق.</span><span class="sxs-lookup"><span data-stu-id="085fb-144">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="085fb-145">استخدم الحقل **عرض** لتغيير طريقة عرض الصفحة إلى *مستخدمي التطبيق*.</span><span class="sxs-lookup"><span data-stu-id="085fb-145">Use the **View** field to change the page view to *Application users*.</span></span>
1. <span data-ttu-id="085fb-146">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="085fb-146">Select **New**.</span></span>
1. <span data-ttu-id="085fb-147">عيّن الحقل **معرف التطبيق** إلى *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*.</span><span class="sxs-lookup"><span data-stu-id="085fb-147">Set the **Application ID** field to *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*.</span></span>
1. <span data-ttu-id="085fb-148">حدد **تعيين دور**، ثم حدد *مسؤول النظام*.</span><span class="sxs-lookup"><span data-stu-id="085fb-148">Select **Assign Role**, and then select *System Administrator*.</span></span> <span data-ttu-id="085fb-149">إذا كان هناك دور يسمي *مستخدم Common Data Service*، فحدده أيضًا.</span><span class="sxs-lookup"><span data-stu-id="085fb-149">If there is a role that is named *Common Data Service User*, select it too.</span></span>
1. <span data-ttu-id="085fb-150">كرر الخطوات السابقة، ولكن قم بتعيين الحقل **معرف التطبيق** إلى *5f58fc56-0202-49a8-ac9e-0946b049718b*.</span><span class="sxs-lookup"><span data-stu-id="085fb-150">Repeat the preceding steps, but set the **Application ID** field to *5f58fc56-0202-49a8-ac9e-0946b049718b*.</span></span>

<span data-ttu-id="085fb-151">لمزيد من المعلومات، راجع [إنشاء مستخدم تطبيق](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="085fb-151">For more information, see [Create an application user](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

<span data-ttu-id="085fb-152">إذا لم تكن اللغة الإنجليزية لتثبيت Dataverse هي اللغة الافتراضية، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="085fb-152">If the default language of your Dataverse installation isn't English, follow these steps.</span></span>

1. <span data-ttu-id="085fb-153">انتقل إلى **إعداد متقدم \> الإدارة \> اللغات**.</span><span class="sxs-lookup"><span data-stu-id="085fb-153">Go to **Advanced Setting \> Administration \> Languages**.</span></span>
1. <span data-ttu-id="085fb-154">حدد *الإنجليزية* (*LanguageCode=1033*)، ثم حدد **تطبيق**.</span><span class="sxs-lookup"><span data-stu-id="085fb-154">Select *English* (*LanguageCode=1033*), and then select **Apply**.</span></span>

## <a name="install-the-add-in"></a><a name="install"></a><span data-ttu-id="085fb-155">تثبيت الوظيفة الإضافية</span><span class="sxs-lookup"><span data-stu-id="085fb-155">Install the add-in</span></span>

<span data-ttu-id="085fb-156">اتبع هذه الخطوات لتثبيت الوظيفة الإضافية بحيث يمكنك استخدام محاسبة المخزون العالمي.</span><span class="sxs-lookup"><span data-stu-id="085fb-156">Follow these steps to install the add-in so that you can use Global Inventory Accounting.</span></span>

1. <span data-ttu-id="085fb-157">[التسجيل](#sign-up) إصدار أولي للاستخدام العام لمحاسبة المخزون العالمي.</span><span class="sxs-lookup"><span data-stu-id="085fb-157">[Sign up](#sign-up) for the Global Inventory Accounting public preview.</span></span>
1. <span data-ttu-id="085fb-158">سجل الدخول إلى [LCS](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="085fb-158">Sign in to [LCS](https://lcs.dynamics.com/Logon/Index).</span></span>
1. <span data-ttu-id="085fb-159">انتقل إلى **إدارة ميزة المعاينة**.</span><span class="sxs-lookup"><span data-stu-id="085fb-159">Go to **Preview feature management**.</span></span>
1. <span data-ttu-id="085fb-160">حدد علامة الزائد (**+**).</span><span class="sxs-lookup"><span data-stu-id="085fb-160">Select the plus sign (**+**).</span></span>
1. <span data-ttu-id="085fb-161">في حقل **الرمز**، أدخل مفتاح بيتا للوظيفة الإضافية لمحاسبة المخزون العالمي.</span><span class="sxs-lookup"><span data-stu-id="085fb-161">In the **Code** field, enter your add-in beta key for Global Inventory Accounting.</span></span> <span data-ttu-id="085fb-162">(يجب أن تكون قد حصلت على مفتاح بيتا الخاص بك عبر البريد الإلكتروني عند التسجيل الاشتراك.)</span><span class="sxs-lookup"><span data-stu-id="085fb-162">(You should have received your beta key by email when you signed up.)</span></span>
1. <span data-ttu-id="085fb-163">حدد **إلغاء الحظر**.</span><span class="sxs-lookup"><span data-stu-id="085fb-163">Select **Unblock**.</span></span>
1. <span data-ttu-id="085fb-164">افتح بيئة LCS حيث تريد إضافة الخدمة بها.</span><span class="sxs-lookup"><span data-stu-id="085fb-164">Open the LCS environment where you want to add the service.</span></span>
1. <span data-ttu-id="085fb-165">انتقل إلى **التفاصيل الكاملة**.</span><span class="sxs-lookup"><span data-stu-id="085fb-165">Go to **Full details**.</span></span>
1. <span data-ttu-id="085fb-166">انتقل إلى **تكامل Power Platform**، وحدد **إعداد**.</span><span class="sxs-lookup"><span data-stu-id="085fb-166">Go to **Power Platform Integration**, and select **Setup**.</span></span>
1. <span data-ttu-id="085fb-167">في مربع الحوار **إعداد بيئة Power platform**، حدد خانة الاختيار، ثم حدد **إعداد**</span><span class="sxs-lookup"><span data-stu-id="085fb-167">In the **Power platform environment setup** dialog box, select the checkbox, and then select **Setup**.</span></span> <span data-ttu-id="085fb-168">وعادةً، يستغرق الإعداد بين 60 و90 دقيقة.</span><span class="sxs-lookup"><span data-stu-id="085fb-168">Typically, setup takes between 60 and 90 minutes.</span></span>
1. <span data-ttu-id="085fb-169">بعد إكمال إعداد بيئة Microsoft Power Platform، في علامة التبويب السريعة **الوظائف الإضافية للبيئة**، حدد **تثبيت وظيفة إضافية جديدة**.</span><span class="sxs-lookup"><span data-stu-id="085fb-169">After setup of the Microsoft Power Platform environment is completed, on the **Environment add-ins** FastTab, select **Install a new add-in**.</span></span>
1. <span data-ttu-id="085fb-170">حدد **محاسبة المخزون العالمي**.</span><span class="sxs-lookup"><span data-stu-id="085fb-170">Select **Global inventory accounting**.</span></span>
1. <span data-ttu-id="085fb-171">اتبع دليل التثبيت، ووافق على البنود والشروط.</span><span class="sxs-lookup"><span data-stu-id="085fb-171">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="085fb-172">حدد **تثبيت**.</span><span class="sxs-lookup"><span data-stu-id="085fb-172">Select **Install**.</span></span>
1. <span data-ttu-id="085fb-173">في علامة التبويب السريعة **الوظائف الإضافية للبيئة**، يجب أن تشاهد محاسبة المخزون العالمي قد تم تثبيتها.</span><span class="sxs-lookup"><span data-stu-id="085fb-173">On the **Environment add-ins** FastTab, you should see that Global Inventory Accounting is being installed.</span></span> <span data-ttu-id="085fb-174">بعد بضع دقائق، يجب أن تغير الحالة من *قيد التثبيت* إلى *مثبت*.</span><span class="sxs-lookup"><span data-stu-id="085fb-174">After a few minutes, the status should change from *Installing* to *Installed*.</span></span> <span data-ttu-id="085fb-175">(قد تحتاج إلى تحديث الصفحة لعرض هذا التغيير.) في تلك النقطة، تكون محاسبة المخزون العالمي جاهزة للاستخدام.</span><span class="sxs-lookup"><span data-stu-id="085fb-175">(You might have to refresh the page to see this change.) At that point, Global Inventory Accounting is ready to use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="085fb-176">إعداد التكامل</span><span class="sxs-lookup"><span data-stu-id="085fb-176">Set up the integration</span></span>

<span data-ttu-id="085fb-177">اتبع هذه الخطوات لإعداد التكامل بين محاسبة المخزون العالمي وSupply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="085fb-177">Follow these steps to set up the integration between Global Inventory Accounting and Supply Chain Management.</span></span>

1. <span data-ttu-id="085fb-178">سجل دخولك إلى Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="085fb-178">Sign in to Supply Chain Management.</span></span>
1. <span data-ttu-id="085fb-179">انتقل إلى **إدارة النظام \> إدارة الميزات**.</span><span class="sxs-lookup"><span data-stu-id="085fb-179">Go to **System administration \> Feature Management**.</span></span>
1. <span data-ttu-id="085fb-180">حدد **التحقق من وجود تحديثات**.</span><span class="sxs-lookup"><span data-stu-id="085fb-180">Select **Check for updates**.</span></span>
1. <span data-ttu-id="085fb-181">في علامة التبويب **الكل**، ابحث عن الميزة التي تسمي *محاسبة المخزون العالمي*.</span><span class="sxs-lookup"><span data-stu-id="085fb-181">On the **All** tab, search for the feature that is named *Global inventory accounting*.</span></span>
1. <span data-ttu-id="085fb-182">حدد **تمكين الآن**.</span><span class="sxs-lookup"><span data-stu-id="085fb-182">Select **Enable now**.</span></span>
1. <span data-ttu-id="085fb-183">انتقل إلى **محاسبة المخزون العالمي \> الإعداد \> معلمات محاسبة المخزون العالمي \> معلمات التكامل**.</span><span class="sxs-lookup"><span data-stu-id="085fb-183">Go to **Global inventory accounting \> Setup \> Global inventory accounting parameters \> Integrations parameters**.</span></span>
1. <span data-ttu-id="085fb-184">في الحقلين **نقطة نهاية خدمة البيانات** و **نقطة نهاية محاسبة المخزون العالمي**، أدخل عناوين URL من البريد الإلكتروني الذي أرسله فريق محاسبة المخزون العالمي عند التسجيل في الإصدار الأولي.</span><span class="sxs-lookup"><span data-stu-id="085fb-184">In the **Data service endpoint** and **Global inventory accounting endpoint** fields, enter the URLs from the email that the Global Inventory Accounting team sent when you signed up for the preview.</span></span>

<span data-ttu-id="085fb-185">محاسبة المخزون العالمي جاهزة الآن للاستخدام.</span><span class="sxs-lookup"><span data-stu-id="085fb-185">Global Inventory Accounting is now ready to use.</span></span>
