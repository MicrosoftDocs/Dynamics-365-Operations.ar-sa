---
title: إعداد مستأجر B2C في Commerce
description: يصف هذا الموضوع كيفية إعداد مستأجري متاجرة بين عمل ومستهلك (B2C) في Azure Active Directory (Azure AD) لمصادقة موقع المستخدم في Dynamics 365 Commerce.
author: BrianShook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.dyn365.ops.version: ''
ms.openlocfilehash: f062f40c9eb883d02c4a0ee06c797ed1b0b22665
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793985"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a><span data-ttu-id="4d250-103">إعداد مستأجر B2C في Commerce</span><span class="sxs-lookup"><span data-stu-id="4d250-103">Set up a B2C tenant in Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4d250-104">يصف هذا الموضوع كيفية إعداد مستأجري متاجرة بين عمل ومستهلك (B2C) في Azure Active Directory (Azure AD) لمصادقة موقع المستخدم في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4d250-104">This topic describes how to set up your Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants for user site authentication in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="4d250-105">يقوم Dynamics 365 Commerce باستخدام Azure AD B2C لدعم بيانات اعتماد المستخدم وتدفقات المصادقة.</span><span class="sxs-lookup"><span data-stu-id="4d250-105">Dynamics 365 Commerce uses Azure AD B2C to support user credential and authentication flows.</span></span> <span data-ttu-id="4d250-106">بإمكان المستخدم التسجيل وتسجيل الدخول وإعادة تعيين كلمة المرور من خلال هذه التدفقات.</span><span class="sxs-lookup"><span data-stu-id="4d250-106">A user can sign up, sign in, and reset their password through these flows.</span></span> <span data-ttu-id="4d250-107">يقوم Azure AD B2C بتخزين معلومات المصادقة الحساسة، مثل اسم المستخدم وكلمه المرور.</span><span class="sxs-lookup"><span data-stu-id="4d250-107">Azure AD B2C stores sensitive user authentication information, such as username and password.</span></span> <span data-ttu-id="4d250-108">سيقوم سجل المستخدم في مستأجر B2C بتخزين سجل حساب محلي B2C أو سجل موفر هوية اجتماعية B2C.</span><span class="sxs-lookup"><span data-stu-id="4d250-108">The user record in the B2C tenant will store either a B2C local account record or a B2C social identity provider record.</span></span> <span data-ttu-id="4d250-109">سترتبط سجلات B2C هذه من جديد بسجل العميل في بيئة Commerce.</span><span class="sxs-lookup"><span data-stu-id="4d250-109">These B2C records will link back to the customer record in the Commerce environment.</span></span>

> [!WARNING] 
> <span data-ttu-id="4d250-110">سيُوقف Azure AD B2C عمليات سير عمل المستخدمين القدامى بحلول 1 أغسطس2021.</span><span class="sxs-lookup"><span data-stu-id="4d250-110">Azure AD B2C will retire old (legacy) user flows by August 1, 2021.</span></span> <span data-ttu-id="4d250-111">لذلك، يجب أن تخطط لترحيل تدفقات المستخدم إلى الإصدار الجديد الموصى به.</span><span class="sxs-lookup"><span data-stu-id="4d250-111">Therefore, you should plan to migrate your user flows to the new recommended version.</span></span> <span data-ttu-id="4d250-112">يوفر الإصدار الجديد تماثل ميزات وميزات جديده.</span><span class="sxs-lookup"><span data-stu-id="4d250-112">The new version provides feature parity and new features.</span></span> <span data-ttu-id="4d250-113">يجب استخدام مكتبة الوحدات لإصدار Commerce رقم 10.0.15 أو إصدار أحدث مع عمليات سير عمل مستخدم B2C الموصى بها.</span><span class="sxs-lookup"><span data-stu-id="4d250-113">The module library for Commerce version 10.0.15 or higher should be used with the recommended B2C user flows.</span></span> <span data-ttu-id="4d250-114">لمزيد من المعلومات، راجع [عمليات سير عمل المستخدمين في Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/user-flow-overview).</span><span class="sxs-lookup"><span data-stu-id="4d250-114">For more information, see [User flows in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/user-flow-overview).</span></span>
 
 > [!NOTE]
 > <span data-ttu-id="4d250-115">تأتي بيئات تقييم Commerce مع مستأجر Azure AD B2C المحمل مسبقًا لأغراض التوضيح.</span><span class="sxs-lookup"><span data-stu-id="4d250-115">Commerce evaluation environments come with a pre-loaded Azure AD B2C tenant for demonstration purposes.</span></span> <span data-ttu-id="4d250-116">لا يلزم تحميل مستأجر Azure AD  B2Cالخاص بك باستخدام الخطوات التالية لبيئات التقييم.</span><span class="sxs-lookup"><span data-stu-id="4d250-116">Loading your own Azure AD B2C tenant using the steps below is not required for evaluation environments.</span></span>

## <a name="create-or-link-to-an-existing-aad-b2c-tenant-in-the-azure-portal"></a><span data-ttu-id="4d250-117">إنشاء مستأجر AAD B2C موجود في مدخل Azure أو الارتباط به</span><span class="sxs-lookup"><span data-stu-id="4d250-117">Create or link to an existing AAD B2C tenant in the Azure portal</span></span>

1. <span data-ttu-id="4d250-118">سجل الدخول إلى [مدخل Azure ](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="4d250-118">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="4d250-119">من قائمة مدخل Azure، حدد **إنشاء مورد**.</span><span class="sxs-lookup"><span data-stu-id="4d250-119">From the Azure portal menu, select **Create a resource**.</span></span> <span data-ttu-id="4d250-120">احرص على استخدام الاشتراك والدليل الذي سيتم توصيله ببيئة Commerce.</span><span class="sxs-lookup"><span data-stu-id="4d250-120">Be sure to use the subscription and directory that will be connected with your Commerce environment.</span></span>

    ![إنشاء مورد في مدخل Azure](./media/B2CImage_1.png)

1. <span data-ttu-id="4d250-122">انتقل إلى **الهوية \> Azure Active Directory B2C**.</span><span class="sxs-lookup"><span data-stu-id="4d250-122">Go to **Identity \> Azure Active Directory B2C**.</span></span>
1. <span data-ttu-id="4d250-123">عند وصولك إلى صفحة **إنشاء مستأجر B2C جديد أو الارتباط بمستأجر موجود**، استخدم أحد الخيارات أدناه الأكثر ملاءمة لاحتياجات شركتك:</span><span class="sxs-lookup"><span data-stu-id="4d250-123">Once on the **Create New B2C Tenant or Link to existing Tenant** page, use one of the options below that best suits your company's needs:</span></span>

    - <span data-ttu-id="4d250-124">**إنشاء مستأجر Azure AD B2C جديد**: استخدم هذا الخيار لإنشاء مستأجر AAD B2C جديد.</span><span class="sxs-lookup"><span data-stu-id="4d250-124">**Create a new Azure AD B2C Tenant**: Use this option to create a new AAD B2C tenant.</span></span>
        1. <span data-ttu-id="4d250-125">حدد **إنشاء مستأجر Azure AD B2C جديد**.</span><span class="sxs-lookup"><span data-stu-id="4d250-125">Select **Create a new Azure AD B2C Tenant**.</span></span>
        1. <span data-ttu-id="4d250-126">ضمن **اسم المؤسسة**، أدخل اسم المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="4d250-126">Under **Organization name**, enter the organization name.</span></span>
        1. <span data-ttu-id="4d250-127">ضمن **اسم المجال الأولي**، أدخل اسم المجال الأولي‏‎.</span><span class="sxs-lookup"><span data-stu-id="4d250-127">Under **Initial domain name**, enter the initial domain name.</span></span>
        1. <span data-ttu-id="4d250-128">في **البلد أو المنطقة**، حدد البلد أو المنطقة.</span><span class="sxs-lookup"><span data-stu-id="4d250-128">For **Country or region**, select the country or region.</span></span>
        1. <span data-ttu-id="4d250-129">حدد **إنشاء** لإنشاء المستأجر.</span><span class="sxs-lookup"><span data-stu-id="4d250-129">Select **Create** to create the tenant.</span></span>

     ![إنشاء مستأجر Azure AD جديد](./media/B2CImage_2.png)

     - <span data-ttu-id="4d250-131">**ربط مستأجر Azure AD B2C موجود باشتراكي في Azure**: استخدم هذا الخيار إذا كان لديك مستأجر Azure AD B2C تريد الارتباط به.</span><span class="sxs-lookup"><span data-stu-id="4d250-131">**Link an existing Azure AD B2C Tenant to my Azure subscription**: Use this option if you already have an Azure AD B2C tenant you want to link to.</span></span>
        1. <span data-ttu-id="4d250-132">حدد **ربط مستأجر Azure AD B2C موجود باشتراكي في Azure**.</span><span class="sxs-lookup"><span data-stu-id="4d250-132">Select **Link an existing Azure AD B2C Tenant to my Azure subscription**.</span></span>
        1. <span data-ttu-id="4d250-133">في **مستأجر Azure AD B2C**، حدد مستأجر B2C المناسب.</span><span class="sxs-lookup"><span data-stu-id="4d250-133">For **Azure AD B2C Tenant**, select the appropriate B2C tenant.</span></span> <span data-ttu-id="4d250-134">إذا ظهرت الرسالة "لم يتم العثور على مستأجري B2C مؤهلين" في مربع التحديد، فهذا يعني عدم وجود مستأجر B2C مؤهل ويجب إنشاء واحد جديد.</span><span class="sxs-lookup"><span data-stu-id="4d250-134">If the message "No eligible B2C Tenants found" appears in the selection box, you do not have an existing eligible B2C tenant and will need to create a new one.</span></span>
        1. <span data-ttu-id="4d250-135">في **مجموعة الموارد**، حدد **إنشاء جديد**.</span><span class="sxs-lookup"><span data-stu-id="4d250-135">For **Resource group**, select **Create new**.</span></span> <span data-ttu-id="4d250-136">أدخل **اسم** مجموعة الموارد التي ستحتوي على المستأجر، وحدد، **موقع مجموعة الموارد**، ثم حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="4d250-136">Enter a **Name** for the resource group that will contain the tenant, select the **Resource group location**, and then select **Create**.</span></span>

    ![ربط مستأجر Azure AD B2C موجود باشتراك Azure](./media/B2CImage_3.png)

1. <span data-ttu-id="4d250-138">بعد إنشاء دليل Azure AD B2C الجديد (قد يستغرق هذا الأمر لحظات قليلة)، سيظهر ارتباط إلى الدليل الجديد على لوحة المعلومات.</span><span class="sxs-lookup"><span data-stu-id="4d250-138">Once the new Azure AD B2C directory is created (this may take a few moments), a link to the new directory will appear on the dashboard.</span></span> <span data-ttu-id="4d250-139">سيوجهك هذا الارتباط إلى صفحة "مرحباً بك في Azure Active Directory B2C".</span><span class="sxs-lookup"><span data-stu-id="4d250-139">This link will direct you to the "Welcome to Azure Active Directory B2C" page.</span></span>

    ![ارتباط إلى دليل AAD جديد](./media/B2CImage_4.png)

> [!NOTE]
> <span data-ttu-id="4d250-141">إذا كانت لديك اشتراكات متعددة داخل حساب Azure أو قمت بإعداد مستأجر B2C بدون إنشاء ارتباط إلى اشتراك نشط، سيقوم شعار **استكشاف الأخطاء وإصلاحها** بتوجيهك لربط المستأجر باشتراك.</span><span class="sxs-lookup"><span data-stu-id="4d250-141">If you have multiple subscriptions within your Azure account or have set up the B2C tenant without linking to an active subscription, a **Troubleshoot** banner will direct you to link the tenant to a subscription.</span></span> <span data-ttu-id="4d250-142">حدد رسالة استكشاف الأخطاء وإصلاحها واتبع الإرشادات لحل مشكلة الاشتراك.</span><span class="sxs-lookup"><span data-stu-id="4d250-142">Select the troubleshooting message and follow the instructions to resolve the subscription issue.</span></span>

<span data-ttu-id="4d250-143">تبين الصورة التالية مثالاً عن شعار **استكشاف الأخطاء وإصلاحها في Azure AD B2C**.</span><span class="sxs-lookup"><span data-stu-id="4d250-143">The following image shows an example of an Azure AD B2C **Troubleshoot** banner.</span></span>

![تحذير يشير إلى عدم وجود اشتراك نشط لدى الدليل](./media/B2CImage_5.png)

## <a name="create-the-b2c-application"></a><span data-ttu-id="4d250-145">إنشاء تطبيق B2C</span><span class="sxs-lookup"><span data-stu-id="4d250-145">Create the B2C application</span></span>

<span data-ttu-id="4d250-146">بعد إنشاء مستأجر B2C، ستقوم بإنشاء تطبيق B2C داخل مستأجر Azure AD B2C للتفاعل مع Commerce.</span><span class="sxs-lookup"><span data-stu-id="4d250-146">Once the B2C tenant has been created, you will create a B2C application within your new Azure AD B2C tenant to interact with Commerce.</span></span>

<span data-ttu-id="4d250-147">لإنشاء تطبيق B2C، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="4d250-147">To create the B2C application, follow these steps.</span></span>

1. <span data-ttu-id="4d250-148">في مدخل Azure، حدد **تسجيلات التطبيق**، ثم حدد **تسجيل جديد**.</span><span class="sxs-lookup"><span data-stu-id="4d250-148">In the Azure portal, select **App registrations**, and then select **New registration**.</span></span>
1. <span data-ttu-id="4d250-149">ضمن **الاسم**، أدخل الاسم لتسمية تطبيق Azure AD B2C هذا به.</span><span class="sxs-lookup"><span data-stu-id="4d250-149">Under **Name**, enter the name to give this Azure AD B2C application.</span></span>
1. <span data-ttu-id="4d250-150">ضمن **أنواع الحسابات المدعومة**، حدد **الحسابات في أي موفر هوية أو دليل تنظيمي (لمصادقة المستخدمين بعمليات سير عمل المستخدمين)**.</span><span class="sxs-lookup"><span data-stu-id="4d250-150">Under **Supported account types**, select **Accounts in any identity provider or organizational directory (for authenticating users with user flows)**.</span></span>
1. <span data-ttu-id="4d250-151">بالنسبة إلى **عنوان URI لإعادة التوجيه**، أدخل عناوين URL للردود المخصصة كنوع **الويب**.</span><span class="sxs-lookup"><span data-stu-id="4d250-151">For **Redirect URI**, enter your dedicated reply URLs as type **Web**.</span></span> <span data-ttu-id="4d250-152">للحصول على معلومات حول عناوين URL للرد وكيفية تنسيقها، راجع [عناوين URL للردود](#reply-urls) أدناه.</span><span class="sxs-lookup"><span data-stu-id="4d250-152">For information on reply URLs and how to format them, see [Reply URLs](#reply-urls) below.</span></span>
1. <span data-ttu-id="4d250-153">للحصول على **الأذونات**، حدد **منح موافقة المسؤول على أذونات openid و offline_access**.</span><span class="sxs-lookup"><span data-stu-id="4d250-153">For **Permissions**, select **Grant admin consent to openid and offline_access permissions**.</span></span>
1. <span data-ttu-id="4d250-154">حدد **السجل**.</span><span class="sxs-lookup"><span data-stu-id="4d250-154">Select **Register**.</span></span>
1. <span data-ttu-id="4d250-155">حدد التطبيق الذي تم إنشاؤه حديثا وانتقل إلى قائمه **المصادقة**.</span><span class="sxs-lookup"><span data-stu-id="4d250-155">Select the newly-created application and navigate to the **Authentication** menu.</span></span> <span data-ttu-id="4d250-156">يمكنك هنا إضافة **عناوين URI لإعادة التوجيه** الإضافية عند اللزوم (الآن أو لاحقًا).</span><span class="sxs-lookup"><span data-stu-id="4d250-156">Here you can add additional **Redirect URIs** if needed (now or later).</span></span> <span data-ttu-id="4d250-157">تابع إلى الخطوة التالية إذا لم تكن هناك حاجة إليها حاليًا.</span><span class="sxs-lookup"><span data-stu-id="4d250-157">Continue to the next step if not currently needed.</span></span>
1. <span data-ttu-id="4d250-158">ضمن **المنح الضمني**، حدد كلا من **رموز الوصول المميزة** و **رموز المعرفات المميزة** لتمكينها للتطبيق.</span><span class="sxs-lookup"><span data-stu-id="4d250-158">Under **Implicit grant**, select both **Access tokens** and **ID tokens** to enable them for the application.</span></span> <span data-ttu-id="4d250-159">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="4d250-159">Select **Save**.</span></span>
1. <span data-ttu-id="4d250-160">انتقل إلى قائمة **النظرة العامة** في مدخل Azue وانسخ **معرف التطبيق (العميل)**.</span><span class="sxs-lookup"><span data-stu-id="4d250-160">Go to the **Overview** menu of the Azure portal and copy the **Application (client) ID**.</span></span> <span data-ttu-id="4d250-161">لاحظ هذا المعرف لخطوات الاعداد التالية (المشار اليها فيما بعد باعتباره **المعرف الفريد العمومي للعميل**).</span><span class="sxs-lookup"><span data-stu-id="4d250-161">Note this ID for later setup steps (referenced later as the **Client GUID**).</span></span>

<span data-ttu-id="4d250-162">للحصول علي مرجع إضافي حول تسجيلات التطبيق في Azure ADB2C، يُرجى مراجعة [تجربه تسجيلات التطبيق الجديدة لـ Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/app-registrations-training-guide)</span><span class="sxs-lookup"><span data-stu-id="4d250-162">For additional reference on App Registrations in Azure AD B2C, please see [The new App registrations experience for Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/app-registrations-training-guide)</span></span>

### <a name="reply-urls"></a><span data-ttu-id="4d250-163">عناوين URL الخاصة بالرد</span><span class="sxs-lookup"><span data-stu-id="4d250-163">Reply URLs</span></span>

<span data-ttu-id="4d250-164">تعتبر عناوين URL الخاصة بالرد مهمة لأنها توفر قائمة بيضاء للمجالات المرتجعة عندما يقوم موقعك باستدعاء Azure AD B2C لمصادقة مستخدم.</span><span class="sxs-lookup"><span data-stu-id="4d250-164">Reply URLs are important as they provide an allow list of the return domains when your site calls Azure AD B2C to authenticate a user.</span></span> <span data-ttu-id="4d250-165">يسمح ذلك بإرجاع المستخدم الذي تمت مصادقته إلى المجال الذي يتم تسجيل الدخول منه (مجال موقعك).</span><span class="sxs-lookup"><span data-stu-id="4d250-165">This permits the return of the authenticated user back to the domain from which they are signing into (your site domain).</span></span> 

<span data-ttu-id="4d250-166">في المربع **عنوان URL الخاص بالرد** على شاشة **Azure AD B2c - تطبيقات \> تطبيق جديد**، تحتاج إلى إضافة خطوط منفصلة لكل من مجال الموقع و(بعد تزويد بيئتك) عنوان URL المنشأ في Commerce.</span><span class="sxs-lookup"><span data-stu-id="4d250-166">In the **Reply URL** box on the **Azure AD B2c - Applications \> New application** screen, you need to add separate lines for both your site domain and (once your environment is provisioned) the Commerce-generated URL.</span></span> <span data-ttu-id="4d250-167">يجب أن تستخدم عناوين URL هذه دائمًا تنسيق URL صالحًا ويجب أن تكون عناوين URL أساسية فقط (لا توجد أي خطوط مائلة أمامية أو مسارات).</span><span class="sxs-lookup"><span data-stu-id="4d250-167">These URLs must always use a valid URL format and must be base URLs only (no trailing forward slashes or paths).</span></span> <span data-ttu-id="4d250-168">يجب إلحاق السلسلة ``/_msdyn365/authresp`` بعناوين URL الأساسية، كما في الأمثلة التالية:</span><span class="sxs-lookup"><span data-stu-id="4d250-168">The string ``/_msdyn365/authresp`` then needs to be appended to the base URLs, as in the following examples.</span></span>

- <span data-ttu-id="4d250-169">``https://www.fabrikam.com/_msdyn365/authresp``(يجب أن يطابق المجال مجال التجارة الإلكترونية بالكامل.</span><span class="sxs-lookup"><span data-stu-id="4d250-169">``https://www.fabrikam.com/_msdyn365/authresp`` (The domain should match the e-commerce domain completely.</span></span> <span data-ttu-id="4d250-170">إذا كان لديك مجالات متعددة، فأنت بحاجة إلى إضافةعنوان URL هذا لكل مجال.)</span><span class="sxs-lookup"><span data-stu-id="4d250-170">If you have multiple domains, you need to add this URL for each domain.)</span></span>
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="create-user-flow-policies"></a><span data-ttu-id="4d250-171">إنشاء سياسات تدفق المستخدم</span><span class="sxs-lookup"><span data-stu-id="4d250-171">Create user flow policies</span></span>

<span data-ttu-id="4d250-172">سياسات تدفق المستخدم هي السياسات التي يستخدمها Azure AD B2C لتوفير تجارب مستخدم آمنة للتسجيل وتسجيل الدخول وتحرير ملف التعريف ونسيان كلمه المرور.</span><span class="sxs-lookup"><span data-stu-id="4d250-172">User flows are the policies Azure AD B2C uses to provide secure sign in, sign up, edit profile, and forget password user experiences.</span></span> <span data-ttu-id="4d250-173">يستخدم Dynamics 365 Commerce  هذه التدفقات لتنفيذ إجراءات السياسة للتفاعل مع مستأجر Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="4d250-173">Dynamics 365 Commerce uses these flows to perform the policy actions to interact with the Azure AD B2C tenant.</span></span> <span data-ttu-id="4d250-174">عندما يتفاعل المستخدم مع هذه السياسات، يعاد توجيههم إلى مستأجر Azure AD B2C لتنفيذ الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="4d250-174">When a user interacts with these policies, they are redirected to the Azure AD B2C tenant to perform the actions.</span></span>

<span data-ttu-id="4d250-175">يوفر Azure AD B2C ثلاثة أنواع من تدفقات المستخدم الأساسية:</span><span class="sxs-lookup"><span data-stu-id="4d250-175">Azure AD B2C provides three basic user flow types:</span></span>
- <span data-ttu-id="4d250-176">التسجيل وتسجيل الدخول</span><span class="sxs-lookup"><span data-stu-id="4d250-176">Sign up and sign in</span></span>
- <span data-ttu-id="4d250-177">تحرير ملف التعريف</span><span class="sxs-lookup"><span data-stu-id="4d250-177">Profile editing</span></span>
- <span data-ttu-id="4d250-178">إعادة تعيين كلمة المرور</span><span class="sxs-lookup"><span data-stu-id="4d250-178">Password reset</span></span>

<span data-ttu-id="4d250-179">يمكنك اختيار استخدام تدفقات المستخدم الافتراضية التي يوفرها Azure AD، والتي ستقوم بعرض صفحة يستضيفها AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="4d250-179">You can choose to use the default user flows provided by Azure AD, which will display a page hosted by AAD B2C.</span></span> <span data-ttu-id="4d250-180">أو يمكنك إنشاء صفحة HTML للتحكم في شكل وأسلوب تجارب تدفق المستخدم هذه.</span><span class="sxs-lookup"><span data-stu-id="4d250-180">Alternately, you can create an HTML page to control the look and feel of these user flow experiences.</span></span> 

<span data-ttu-id="4d250-181">لتخصيص صفحات سياسة المستخدم مع الضفحات المضمنة في Dynamics 365 Commerce، راجع [إعداد صفحات مخصصة لعمليات تسجيل دخول المستخدمين‬](custom-pages-user-logins.md).</span><span class="sxs-lookup"><span data-stu-id="4d250-181">To customize the user policy pages with pages built in Dynamics 365 Commerce, see [Set up custom pages for user logins](custom-pages-user-logins.md).</span></span> <span data-ttu-id="4d250-182">للحصول على معلومات إضافية، راجع [تخصيص واجهة تجارب المستخدم في Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).</span><span class="sxs-lookup"><span data-stu-id="4d250-182">For additional information, see [Customize the interface of user experiences in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).</span></span>

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a><span data-ttu-id="4d250-183">إنشاء عملية تسجيل وتسجيل دخول في سياسة تدفق المستخدم</span><span class="sxs-lookup"><span data-stu-id="4d250-183">Create a sign up and sign in user flow policy</span></span>

<span data-ttu-id="4d250-184">لإنشاء عملية تسجيل وتسجيل دخول في سياسة تدفق المستخدم، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="4d250-184">To create a sign up and sign in user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="4d250-185">في مدخل Azure، حدد **تدفقات المستخدم (السياسات)** في جزء التنقل الأيمن.</span><span class="sxs-lookup"><span data-stu-id="4d250-185">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="4d250-186">في صفحة **Azure AD B2C – تدفقات المستخدم (السياسات)‬‏‫**، حدد **تدفق مستخدم جديد‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="4d250-186">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="4d250-187">حدد سياسة **تسجيل الاشتراك وتسجيل الدخول**، ثم حدد الإصدار **الموصى به**.</span><span class="sxs-lookup"><span data-stu-id="4d250-187">Select the **Sign up and sign in** policy, and then select the **Recommended** version.</span></span>
1. <span data-ttu-id="4d250-188">ضمن **الاسم**، أدخل اسمًا للسياسة.</span><span class="sxs-lookup"><span data-stu-id="4d250-188">Under **Name**, enter a policy name.</span></span> <span data-ttu-id="4d250-189">سيظهر هذا الاسم بعد ذلك مع بادئة يعينها المدخل (على سبيل المثال، "B2C_1_").</span><span class="sxs-lookup"><span data-stu-id="4d250-189">This name will display afterwards with a prefix the portal assigns (for example, "B2C_1_").</span></span>
1. <span data-ttu-id="4d250-190">ضمن **موفرو الهوية**، حدد خانة الاختيار المناسبة.</span><span class="sxs-lookup"><span data-stu-id="4d250-190">Under **Identity providers**, select the appropriate check box.</span></span>
1. <span data-ttu-id="4d250-191">ضمن **مصادقة متعددة العوامل**، حدد الاختيار المناسب لشركتك.</span><span class="sxs-lookup"><span data-stu-id="4d250-191">Under **Multifactor Authentication**, select the appropriate choice for your company.</span></span> 
1. <span data-ttu-id="4d250-192">ضمن **سمات ومطالبات المستخدم**، حدد الخيارات لجمع السمات أو إرجاع المطالبات حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="4d250-192">Under **User attributes and claims**, select options to collect attributes or return claims as appropriate.</span></span> <span data-ttu-id="4d250-193">يحتاج Commerce إلى الخيارات الافتراضية التالية:</span><span class="sxs-lookup"><span data-stu-id="4d250-193">Commerce requires the following default options:</span></span>

    | <span data-ttu-id="4d250-194">**جمع سمة**</span><span class="sxs-lookup"><span data-stu-id="4d250-194">**Collect  attribute**</span></span> | <span data-ttu-id="4d250-195">**إرجاع مطالبة**</span><span class="sxs-lookup"><span data-stu-id="4d250-195">**Return  claim**</span></span> |
    | ---------------------- | ----------------- |
    | <span data-ttu-id="4d250-196">عنوان البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="4d250-196">Email Address</span></span>          | <span data-ttu-id="4d250-197">عناوين البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="4d250-197">Email Addresses</span></span>   |
    | <span data-ttu-id="4d250-198">الاسم المحدد</span><span class="sxs-lookup"><span data-stu-id="4d250-198">Given Name</span></span>             | <span data-ttu-id="4d250-199">الاسم المحدد</span><span class="sxs-lookup"><span data-stu-id="4d250-199">Given Name</span></span>        |
    |                        | <span data-ttu-id="4d250-200">موفر الهوية‬</span><span class="sxs-lookup"><span data-stu-id="4d250-200">Identity Provider</span></span> |
    | <span data-ttu-id="4d250-201">اللقب</span><span class="sxs-lookup"><span data-stu-id="4d250-201">Surname</span></span>                | <span data-ttu-id="4d250-202">اللقب</span><span class="sxs-lookup"><span data-stu-id="4d250-202">Surname</span></span>           |
    |                        | <span data-ttu-id="4d250-203">معرف الكائن الخاص بالمستخدم</span><span class="sxs-lookup"><span data-stu-id="4d250-203">User’s Object ID</span></span>  |

1. <span data-ttu-id="4d250-204">حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="4d250-204">Select **Create**.</span></span>

<span data-ttu-id="4d250-205">الصورة التالية هي مثال تدفق المستخدم للتسجيل وتسجيل الدخول إلى Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="4d250-205">The following image is an example of the Azure AD B2C sign up and sign in user flow.</span></span>

![إعدادات سياسة التسجيل وتسجيل الدخول](./media/B2CImage_11.png)

<span data-ttu-id="4d250-207">تظهر الصورة التالية الخيار **تشغيل تدفق المستخدم** في Azure AD B2C تدفق المستخدم للتسجيل وتسجيل الدخول إلى B2C.</span><span class="sxs-lookup"><span data-stu-id="4d250-207">The following image shows the **Run user flow** option in the Azure AD B2C sign up and sign in user flow.</span></span>

![الخيار "تشغيل تدفق المستخدم‬‏‫" في تدفق السياسة](./media/B2CImage_23.png)
   
### <a name="create-a-profile-editing-user-flow-policy"></a><span data-ttu-id="4d250-209">إنشاء سياسة تدفق المستخدم لتحرير ملف التعريف</span><span class="sxs-lookup"><span data-stu-id="4d250-209">Create a profile editing user flow policy</span></span>

<span data-ttu-id="4d250-210">لإنشاء سياسة تدفق المستخدم لتحرير ملف التعريف، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="4d250-210">To create a profile editing user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="4d250-211">في مدخل Azure، حدد **تدفقات المستخدم (السياسات)** في جزء التنقل الأيمن.</span><span class="sxs-lookup"><span data-stu-id="4d250-211">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="4d250-212">في صفحة **Azure AD B2C – تدفقات المستخدم (السياسات)‬‏‫**، حدد **تدفق مستخدم جديد‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="4d250-212">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="4d250-213">حدد **تحرير ملف التعريف**، ثم حدد الإصدار **الموصى به**.</span><span class="sxs-lookup"><span data-stu-id="4d250-213">Select **Profile editing**, and then select the **Recommended** version.</span></span>
1. <span data-ttu-id="4d250-214">ضمن **الاسم**، أدخل تدفق المستخدم لتحرير ملف التعريف.</span><span class="sxs-lookup"><span data-stu-id="4d250-214">Under **Name**, enter the profile editing user flow.</span></span> <span data-ttu-id="4d250-215">سيظهر هذا الاسم بعد ذلك مع بادئة يعينها المدخل (على سبيل المثال، "B2C_1_").</span><span class="sxs-lookup"><span data-stu-id="4d250-215">This name will display afterwards with a prefix the portal assigns (for example, "B2C_1_").</span></span>
1. <span data-ttu-id="4d250-216">ضمن **موفرو الهوية**، حدد **تسجيل الدخول إلى البريد الإلكتروني**.</span><span class="sxs-lookup"><span data-stu-id="4d250-216">Under **Identity providers**, select **Email SignIn**.</span></span>
1. <span data-ttu-id="4d250-217">ضمن **سمات المستخدم**، حدد خانات الاختيار التالية:</span><span class="sxs-lookup"><span data-stu-id="4d250-217">Under **User attributes**, select the following check boxes:</span></span>
    - <span data-ttu-id="4d250-218">**عناوين البريد الإلكتروني** (**إرجاع مطالبة** فقط)</span><span class="sxs-lookup"><span data-stu-id="4d250-218">**Email Addresses** (**Return claim** only)</span></span>
    - <span data-ttu-id="4d250-219">**الاسم المحدد** (**جمع السمة** و **إرجاع مطالبة‬‏‫**)</span><span class="sxs-lookup"><span data-stu-id="4d250-219">**Given Name** (**Collect attribute** and **Return claim**)</span></span>
    - <span data-ttu-id="4d250-220">**موفر‏‎ الهوية** (**إرجاع مطالبة‬‏‫** فقط)</span><span class="sxs-lookup"><span data-stu-id="4d250-220">**Identity Provider** (**Return claim** only)</span></span>
    - <span data-ttu-id="4d250-221">**اللقب‬‏‫** (**جمع السمة** و **إرجاع مطالبة‬‏‫**)</span><span class="sxs-lookup"><span data-stu-id="4d250-221">**Surname** (**Collect attribute** and **Return claim**)</span></span>
    - <span data-ttu-id="4d250-222">**معرف الكائن الخاص بالمستخدم‬** (**إرجاع مطالبة** فقط)</span><span class="sxs-lookup"><span data-stu-id="4d250-222">**User's Object ID** (**Return claim** only)</span></span>
1. <span data-ttu-id="4d250-223">حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="4d250-223">Select **Create**.</span></span>

<span data-ttu-id="4d250-224">تعرض الصورة التالية مثالاً عن تدفق المستخدم لتحرير مرف تعريف Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="4d250-224">The following image shows an example of the Azure AD B2C profile editing user flow.</span></span>

![إنشاء تدفق المستخدم لتحرير ملف التعريف](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a><span data-ttu-id="4d250-226">إنشاء سياسة تدفق المستخدم لإعادة تعيين كلمة المرور</span><span class="sxs-lookup"><span data-stu-id="4d250-226">Create a password reset user flow policy</span></span>

<span data-ttu-id="4d250-227">لإنشاء سياسة تدفق المستخدم لإعادة تعيين كلمة المرور، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="4d250-227">To create a password reset user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="4d250-228">في مدخل Azure، حدد **تدفقات المستخدم (السياسات)** في جزء التنقل الأيمن.</span><span class="sxs-lookup"><span data-stu-id="4d250-228">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="4d250-229">في صفحة **Azure AD B2C – تدفقات المستخدم (السياسات)‬‏‫**، حدد **تدفق مستخدم جديد‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="4d250-229">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="4d250-230">حدد **إعادة تعيين كلمة المرور**، ثم حدد الإصدار **الموصى به**.</span><span class="sxs-lookup"><span data-stu-id="4d250-230">Select **Password Reset**, and then select the **Recommended** version.</span></span>
1. <span data-ttu-id="4d250-231">ضمن **الاسم**، أدخل اسمًا لتدفق المستخدم لإعادة تعيين كلمة المرور.</span><span class="sxs-lookup"><span data-stu-id="4d250-231">Under **Name**, enter a name for the password reset user flow.</span></span>
1. <span data-ttu-id="4d250-232">ضمن **موفرو الهوية**، حدد **إعادة تعيين كلمة المرور باستخدام عنوان البريد الكتروني**.</span><span class="sxs-lookup"><span data-stu-id="4d250-232">Under **Identity providers**, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="4d250-233">حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="4d250-233">Select **Create**.</span></span>
1. <span data-ttu-id="4d250-234">ضمن **مطالبات التطبيق**، حدد خانات الاختيار التالية:</span><span class="sxs-lookup"><span data-stu-id="4d250-234">Under **Application claims**, select the following check boxes:</span></span>
    - <span data-ttu-id="4d250-235">**عناوين البريد الإلكتروني**</span><span class="sxs-lookup"><span data-stu-id="4d250-235">**Email addresses**</span></span>
    - <span data-ttu-id="4d250-236">**الاسم المحدد**</span><span class="sxs-lookup"><span data-stu-id="4d250-236">**Given Name**</span></span>
    - <span data-ttu-id="4d250-237">**اللقب**</span><span class="sxs-lookup"><span data-stu-id="4d250-237">**Surname**</span></span>
    - <span data-ttu-id="4d250-238">**معرف الكائن الخاص بالمستخدم**</span><span class="sxs-lookup"><span data-stu-id="4d250-238">**User's Object ID**</span></span>
1. <span data-ttu-id="4d250-239">حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="4d250-239">Select **Create**.</span></span>

<span data-ttu-id="4d250-240">توضح الصورة التالية المكان حيث يجب تعيين الخيار **إعادة تعيين كلمة المرور باستخدام عنوان بريد إلكتروني** في تدفق المستخدم لإعادة تعيين كلمة المرور في Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="4d250-240">The following image shows where to set **Reset Password using mail address** in the Azure AD B2C password reset user flow.</span></span>

![تعيين "إعادة تعيين كلمة المرور باستخدام عنوان بريد إلكتروني" في سياسة إعادة تعيين كلمة المرور](./media/B2CImage_13.png)

## <a name="add-social-identity-providers-optional"></a><span data-ttu-id="4d250-242">إضافة موفري الهوية الاجتماعية (اختياري)</span><span class="sxs-lookup"><span data-stu-id="4d250-242">Add social identity providers (Optional)</span></span>

<span data-ttu-id="4d250-243">يسمح موفرو الهوية الاجتماعية للمستخدمين باستخدام حساباتهم الاجتماعية للمصادقة.</span><span class="sxs-lookup"><span data-stu-id="4d250-243">Social identity providers allow users to use their social accounts for authentication.</span></span> <span data-ttu-id="4d250-244">تعتبر إضافة مصادقة موفر الهوية الاجتماعية اختيارية في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4d250-244">Adding social identity provider authentication is optional in Dynamics 365 Commerce.</span></span> 

<span data-ttu-id="4d250-245">إذا لم تتم إضافة مصادقة موفر الهوية الاجتماعية، ستكون ملفات تعريف Azure AD B2C الافتراضية ملفات التعريف الأساسية لقاعدة المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="4d250-245">If social identity provider authentication is not added, the default Azure AD B2C profiles will be the main profiles for your user base.</span></span> <span data-ttu-id="4d250-246">سيقوم المستخدمون بتحديد اسم المستخدم (عنوان بريدهم الإلكتروني المفضل) وتعيين كلمة مرور.</span><span class="sxs-lookup"><span data-stu-id="4d250-246">Users will select their own username (their preferred email address) and set a password.</span></span> <span data-ttu-id="4d250-247">سيقوم Azure AD B2C بمصادقة المستخدمين بشكل مباشر.</span><span class="sxs-lookup"><span data-stu-id="4d250-247">Azure AD B2C will authenticate users directly.</span></span> 

<span data-ttu-id="4d250-248">إذا تمت إضافة مصادقة موفر الهوية الاجتماعية واختار أحد المستخدمين أحد موفري الهوية الاجتماعية المعروضين، فسيتم مع ذلك إنشاء كيان في مستأجر Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="4d250-248">If social identity provider authentication is added and a user chooses one of the social identity providers offered, an entity is still created in the Azure AD B2C tenant.</span></span> <span data-ttu-id="4d250-249">سيقوم Azure AD B2C عندئذٍ بمصادقة بيانات اعتماد المستخدم مع موفر الهوية الاجتماعية.</span><span class="sxs-lookup"><span data-stu-id="4d250-249">Azure AD B2C will then authenticate the user's credentials with the social identity provider.</span></span>

> [!NOTE]
> <span data-ttu-id="4d250-250">يؤدي تسجيل دخول الموفر إلى إنشاء سجل في مستأجر B2C، ولكن بتنسيق مختلف عن الحسابات المحلية لأنه سيقوم باستدعاء مرجع موفر الهوية الاجتماعية الخارجي للمصادقة.</span><span class="sxs-lookup"><span data-stu-id="4d250-250">The identity provider sign in creates a record in the B2C tenant, but in a different format than local accounts since it will call the external social identity provider reference for authentication.</span></span> <span data-ttu-id="4d250-251">يمكن للمستخدم استخدام عنوان البريد الإلكتروني نفسه عبر موفري الهويات الاجتماعية، مما يعني أن اسم المستخدم للبريد الإلكتروني الذي تم استخدامه للمصادقة قد لا يكون فريدًا للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="4d250-251">The user can use the same email address across social identity providers, meaning that the email username used for authentication may not be unique to the tenant.</span></span> <span data-ttu-id="4d250-252">سيفرض Azure AD B2C فقط وجود عنوان بريد إلكتروني فريد للمستخدمين على حسابات B2C المحلية.</span><span class="sxs-lookup"><span data-stu-id="4d250-252">Azure AD B2C will only enforce that users have a unique email address on local B2C accounts.</span></span>

<span data-ttu-id="4d250-253">قبل أن تتمكن من إضافة موفر هوية اجتماعية للمصادقة، يجب الانتقال إلى مدخل موفر الهوية وإعداد تطبيق موفر هوية كما هو موضح في وثائق Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="4d250-253">Before you can add a social identity provider for authentication, you must go to the identity provider's portal and set up an identity provider application as instructed in the Azure AD B2C documentation.</span></span> <span data-ttu-id="4d250-254">توجد أدناه قائمة بالارتباطات إلى الوثائق.</span><span class="sxs-lookup"><span data-stu-id="4d250-254">A list of links to the documentation is provided below.</span></span>

- [<span data-ttu-id="4d250-255">Amazon</span><span class="sxs-lookup"><span data-stu-id="4d250-255">Amazon</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [<span data-ttu-id="4d250-256">Azure AD (مستأجر واحد)</span><span class="sxs-lookup"><span data-stu-id="4d250-256">Azure AD (Single Tenant)</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [<span data-ttu-id="4d250-257">حساب Microsoft</span><span class="sxs-lookup"><span data-stu-id="4d250-257">Microsoft Account</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [<span data-ttu-id="4d250-258">Facebook</span><span class="sxs-lookup"><span data-stu-id="4d250-258">Facebook</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [<span data-ttu-id="4d250-259">GitHub</span><span class="sxs-lookup"><span data-stu-id="4d250-259">GitHub</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [<span data-ttu-id="4d250-260">Google</span><span class="sxs-lookup"><span data-stu-id="4d250-260">Google</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [<span data-ttu-id="4d250-261">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="4d250-261">LinkedIn</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [<span data-ttu-id="4d250-262">OpenID Connect</span><span class="sxs-lookup"><span data-stu-id="4d250-262">OpenID Connect</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [<span data-ttu-id="4d250-263">Twitter</span><span class="sxs-lookup"><span data-stu-id="4d250-263">Twitter</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a><span data-ttu-id="4d250-264">إضافة موفر هوية اجتماعية وإعداده</span><span class="sxs-lookup"><span data-stu-id="4d250-264">Add and set up a social identity provider</span></span>

<span data-ttu-id="4d250-265">لإضافة موفر هوية اجتماعية وإعداده، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="4d250-265">To add and set up a social identity provider, follow these steps.</span></span>  

1. <span data-ttu-id="4d250-266">في مدخل Azure، انتقل إلى **موفرو الهوية**.</span><span class="sxs-lookup"><span data-stu-id="4d250-266">In the Azure portal, navigate to **Identity Providers**.</span></span>
1. <span data-ttu-id="4d250-267">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="4d250-267">Select **Add**.</span></span> <span data-ttu-id="4d250-268">تظهر الشاشة **إضافة موفر هوية**.</span><span class="sxs-lookup"><span data-stu-id="4d250-268">The **Add identity provider** screen appears.</span></span>
1. <span data-ttu-id="4d250-269">ضمن **الاسم**، أدخل الاسم المطلوب عرضه للمستخدمين على شاشة تسجيل الدخول.</span><span class="sxs-lookup"><span data-stu-id="4d250-269">Under **Name**, enter the name to be displayed to users on your sign in screen.</span></span>
1. <span data-ttu-id="4d250-270">ضمن **نوع موفر الهوية**، حدد موفر هوية من القائمة.</span><span class="sxs-lookup"><span data-stu-id="4d250-270">Under **Identity provider type**, select an identity provider from the list.</span></span>
1. <span data-ttu-id="4d250-271">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="4d250-271">Select **OK**.</span></span>
1. <span data-ttu-id="4d250-272">حدد **إعداد موفر الهوية هذا** للوصول إلى شاشة **إعداد موفر الهوية الاجتماعية**.</span><span class="sxs-lookup"><span data-stu-id="4d250-272">Select **Set up this identity provider** to access the **Set up the social identity provider** screen.</span></span>
1. <span data-ttu-id="4d250-273">ضمن **معرف العميل**، أدخل معرف العميل كما تم الحصول عليه من إعداد تطبيق موفر الهوية.</span><span class="sxs-lookup"><span data-stu-id="4d250-273">Under **Client ID**, enter the client ID as obtained from the identity provider application setup.</span></span>
1. <span data-ttu-id="4d250-274">ضمن **سر العميل**، أدخل سر العميل كما تم الحصول عليه من إعداد تطبيق موفر الهوية.</span><span class="sxs-lookup"><span data-stu-id="4d250-274">Under **Client secret**, enter the client secret as obtained from the identity provider application setup.</span></span>
1. <span data-ttu-id="4d250-275">إرفاق تدفق المستخدم لسياسات التسجيل:</span><span class="sxs-lookup"><span data-stu-id="4d250-275">Attach user flow for sign in sign up policies:</span></span>
1. <span data-ttu-id="4d250-276">انتقل إلى **Azure AD B2C – تدفقات المستخدم (السياسات) \> {سياسة التسجيل وتسجيل الدخول} \> موفرو الهوية**.</span><span class="sxs-lookup"><span data-stu-id="4d250-276">Go to **Azure AD B2C – User flows (policies) \> {your sign-in sign-up policy} \> Identity providers**.</span></span>
1. <span data-ttu-id="4d250-277">لإرفاق سياسة تدفق المستخدم للتسجيل/تسجيل الدخول، حدد كل موفر هوية قمت بإعداده لحسابك.</span><span class="sxs-lookup"><span data-stu-id="4d250-277">To attach the sign in/sign up user flow policy, select each identity provider you have set up for your account.</span></span> <span data-ttu-id="4d250-278">لاختبار هؤلاء، حدد **تشغيل تدفق المستخدم** لكل موفر هوية.</span><span class="sxs-lookup"><span data-stu-id="4d250-278">To test these, select **Run user flow** for each identity provider.</span></span> <span data-ttu-id="4d250-279">ستعرض علامة تبويب جديدة صفحة تسجيل الدخول التي تعرض مربع تحديد موفر الهوية الجديد.</span><span class="sxs-lookup"><span data-stu-id="4d250-279">A new tab will display the sign-in page displaying the new identity provider selection box.</span></span>

<span data-ttu-id="4d250-280">تظهر الصورة التالية أمثلة عن شاشات **إضافة موفر هوية** و **إعداد موفر الهوية الاجتماعية** في Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="4d250-280">The following image shows examples of the **Add identity provider** and **Set up the social identity provider** screens in Azure AD B2C.</span></span>

![إضافة موفر هوية اجتماعية إلى تطبيقك](./media/B2CImage_14.png)

<span data-ttu-id="4d250-282">تعرض الصورة التالية مثالاً عن كيفية تحديد موفري الهوية في صفحة **موفرو هوية** Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="4d250-282">The following image shows an example of how to select identity providers on the Azure AD B2C **Identity Providers** page.</span></span>

![حدد كل موفر هوية اجتماعية لتمكينه لسياستك](./media/B2CImage_16.png)

<span data-ttu-id="4d250-284">تعرض الصورة التالية مثالاً عن شاشة تسجيل دخول افتراضية مع عرض زر تسجيل الدخول إلى موفر هوية اجتماعية.</span><span class="sxs-lookup"><span data-stu-id="4d250-284">The following image shows an example of a default sign-in screen with a social identity provider sign-in button displayed.</span></span>

> [!NOTE]
> <span data-ttu-id="4d250-285">إذا كنت تستخدم الصفحات المخصصة المضمنة في Commerce لتدفقات المستخدم الخاصة بك، فستحتاج الأزرار الخاصة بموفري الهوية الاجتماعية إلى إضافتها باستخدام ميزات القابلية للتوسعة في مكتبة وحدة Commerce.</span><span class="sxs-lookup"><span data-stu-id="4d250-285">If using the custom pages built in Commerce for your user flows, the buttons for social identity providers will need to be added using the extensibility features of the Commerce module library.</span></span> <span data-ttu-id="4d250-286">بالإضافة إلى ذلك، عند إعداد تطبيقاتك باستخدام موفر هوية اجتماعية محدد، قد يكون عنوان URL أو سلاسل التكوين في بعض الحالات حساسة لحالة الأحرف.</span><span class="sxs-lookup"><span data-stu-id="4d250-286">Additionally, when setting up your applications with a specific social identity provider, in some cases URL or configuration strings may be case sensitive.</span></span> <span data-ttu-id="4d250-287">راجع إرشادات الاتصال الخاصة بموفر الهوية الاجتماعية لمزيد من المعلومات.</span><span class="sxs-lookup"><span data-stu-id="4d250-287">Refer to your social identity provider's connection instructions for more information.</span></span>
 
![مثال عن شاشة تسجيل دخول افتراضية مع عرض زر تسجيل الدخول إلى موفر هوية اجتماعية](./media/B2CImage_17.png)

## <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a><span data-ttu-id="4d250-289">تحديث Commerce headquarters بواسطة معلومات Azure AD B2C جديدة</span><span class="sxs-lookup"><span data-stu-id="4d250-289">Update Commerce headquarters with the new Azure AD B2C information</span></span>

<span data-ttu-id="4d250-290">بعد إكمال خطوات تزويد Azure AD B2C أعلاه، يجب تسجيل تطبيق Azure AD B2C في بيئتك في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4d250-290">Once the Azure AD B2C provisioning steps above are completed, the Azure AD B2C application must be registered in your Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="4d250-291">لتحديث المقر الرئيسي بمعلومات Azure AD B2C الجديدة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="4d250-291">To update headquarters with the new Azure AD B2C information, follow these steps.</span></span>

1. <span data-ttu-id="4d250-292">في Commerce، انتقل إلى **معلمات Commerce المشتركة**، وحدد **موفرو الهوية** في القائمة اليسرى</span><span class="sxs-lookup"><span data-stu-id="4d250-292">In Commerce, go to **Commerce Shared Parameters** and select **Identity Providers** in the left menu.</span></span>
1. <span data-ttu-id="4d250-293">ضمن **موفرو الهوية**، قم بما يلي:</span><span class="sxs-lookup"><span data-stu-id="4d250-293">Under **Identity Providers**, do the following:</span></span>
    1. <span data-ttu-id="4d250-294">في **المصدر**، أدخل عنوان URL لمصدر موفر الهوية.</span><span class="sxs-lookup"><span data-stu-id="4d250-294">In the **Issuer** box, enter the identity provider issuer URL.</span></span> <span data-ttu-id="4d250-295">للعثور على عنوان URL الخاص بالمصدر‏‎، راجع  [الحصول على عنوان المصدر](#obtain-issuer-url) أدناه.</span><span class="sxs-lookup"><span data-stu-id="4d250-295">To find your issuer URL, see [Obtain issuer URL](#obtain-issuer-url) below.</span></span>
    1. <span data-ttu-id="4d250-296">في مربع **الاسم**، أدخل اسمًا لسجل المصدر.</span><span class="sxs-lookup"><span data-stu-id="4d250-296">In the **Name** box, enter a name for your issuer record.</span></span>
    1. <span data-ttu-id="4d250-297">في مربع **النوع**، أدخل **Azure AD B2C (id_token)**.</span><span class="sxs-lookup"><span data-stu-id="4d250-297">In the **Type** box, enter **Azure AD B2C (id_token)**.</span></span>
1. <span data-ttu-id="4d250-298">ضمن **الأطراف المعتمِدة**، مع تحديد عنصر موفر هوية B2C أعلاه، قم بما يلي:</span><span class="sxs-lookup"><span data-stu-id="4d250-298">Under **Relying Parties**, with the above B2C identity provider item selected, do the following:</span></span>
    1. <span data-ttu-id="4d250-299">في المربع‏‎ **معرف العميل**، أدخل معرف تطبيق B2C.</span><span class="sxs-lookup"><span data-stu-id="4d250-299">In the **ClientID** box, enter your B2C application ID.</span></span> <span data-ttu-id="4d250-300">يمكنك العثور على هذا المعرف في مربع **معرف التطبيق** في صفحة خصائص تطبيق B2C.</span><span class="sxs-lookup"><span data-stu-id="4d250-300">You can find this in the **Application ID** box of your B2C application's properties page.</span></span>
    1. <span data-ttu-id="4d250-301">في مربع **النوع**، أدخل **عام**.</span><span class="sxs-lookup"><span data-stu-id="4d250-301">In the **Type** box, enter **Public**.</span></span>
    1. <span data-ttu-id="4d250-302">في مربع **نوع المستخدم**، أدخل **عميل**.</span><span class="sxs-lookup"><span data-stu-id="4d250-302">In the **User Type** box, enter **Customer**.</span></span>
1. <span data-ttu-id="4d250-303">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="4d250-303">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="4d250-304">في مربع البحث في Commerce، ابحث عن **جدول التوزيع**</span><span class="sxs-lookup"><span data-stu-id="4d250-304">In the Commerce search box, search for **Distribution schedule**</span></span>
1. <span data-ttu-id="4d250-305">في قائمة التنقل اليسرة من صفحة **جداول التوزيع**، حدد الوظيفة **1110 تكوين عمومي**.</span><span class="sxs-lookup"><span data-stu-id="4d250-305">In the left navigation menu of the **Distribution schedules** page, select job **1110 Global configuration**.</span></span>
1. <span data-ttu-id="4d250-306">في جزء الإجراءات، حدد **تشغيل الآن**.</span><span class="sxs-lookup"><span data-stu-id="4d250-306">On the action pane, select **Run Now**.</span></span>

### <a name="obtain-issuer-url"></a><span data-ttu-id="4d250-307">الحصول على عنوان URL للمصدر</span><span class="sxs-lookup"><span data-stu-id="4d250-307">Obtain issuer URL</span></span>

<span data-ttu-id="4d250-308">للحصول على عنوان URL لمصدر موفر الهوية، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="4d250-308">To obtain your identity provider issuer URL, follow these steps.</span></span>
1. <span data-ttu-id="4d250-309">في صفحة Azure AD B2C الخاصة بمدخل Azure، انتقل إلى سير عمل مستخدم **تسجيل الاشتراك وتسجيل الدخول**.</span><span class="sxs-lookup"><span data-stu-id="4d250-309">On the Azure AD B2C page of the Azure portal, navigate to your **Sign up and sign in** user flow.</span></span>
1. <span data-ttu-id="4d250-310">حدد **تخطيطات الصفحات** في قائمه التنقل إلى اليسار، ضمن **اسم التخطيط**، حدد **صفحة تسجيل الاشتراك أو تسجيل الدخول الموحد**، ثم حدد **تشغيل سير عمل المستخدم**.</span><span class="sxs-lookup"><span data-stu-id="4d250-310">Select **Page layouts** in the left navigation menu, under **Layout name** select **Unified sign up or sign in page**, and then select **Run user flow**.</span></span>
1. <span data-ttu-id="4d250-311">تأكد من تعيين التطبيق الخاص بك إلى تطبيق Azure AD B2C المقصود الذي تم إنشاؤه أعلاه، ثم حدد الارتباط ضمن رأس **تشغيل سير عمل المستخدم** الذي يتضمن ``.../.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``.</span><span class="sxs-lookup"><span data-stu-id="4d250-311">Make sure your application is set to your intended Azure AD B2C application created above, and then select the link under the **Run user flow** header that includes ``.../.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``.</span></span>
1. <span data-ttu-id="4d250-312">يتم عرض صفحه بيانات التعريف في علامة تبويب المستعرض الخاصة بك. انسخ عنوان URL الخاص بمصدر موفر الهوية (قيمة **المُصدر**).</span><span class="sxs-lookup"><span data-stu-id="4d250-312">A metadata page is displayed in your browser tab. Copy the identity provider issuer URL (the value for **"issuer"**).</span></span>
   - <span data-ttu-id="4d250-313">مثال: ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.</span><span class="sxs-lookup"><span data-stu-id="4d250-313">Example: ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.</span></span>
 
<span data-ttu-id="4d250-314">**أو**: لإنشاء نفس عنوان URL لبيانات التعريف يدويا، قم باجراء الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="4d250-314">**OR**: To construct the same metadata URL manually, do the following steps.</span></span>

1. <span data-ttu-id="4d250-315">قم بإنشاء عنوان URL لعنوان بيانات التعريف بالتنسيق التالي باستخدام سياسة ومستأجر B2C: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``</span><span class="sxs-lookup"><span data-stu-id="4d250-315">Create a metadata address URL in the following format using your B2C tenant and policy: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``</span></span>
    - <span data-ttu-id="4d250-316">مثال: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.</span><span class="sxs-lookup"><span data-stu-id="4d250-316">Example: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.</span></span>
1. <span data-ttu-id="4d250-317">أدخل عنوان URL لعنوان بيانات التعريف في شريط العناوين في المستعرض.</span><span class="sxs-lookup"><span data-stu-id="4d250-317">Enter the metadata address URL into a browser address bar.</span></span>
1. <span data-ttu-id="4d250-318">في بيانات التعريف، انسخ عنوان URL لمصدر موفر الهوية (قيمة **"المصدر"**).</span><span class="sxs-lookup"><span data-stu-id="4d250-318">In the metadata, copy the identity provider issuer URL (the value for **"issuer"**).</span></span>
    - <span data-ttu-id="4d250-319">مثال: ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.</span><span class="sxs-lookup"><span data-stu-id="4d250-319">Example: ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.</span></span>

## <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a><span data-ttu-id="4d250-320">تكوين مستأجر B2C في منشئ موقع Commerce</span><span class="sxs-lookup"><span data-stu-id="4d250-320">Configure your B2C tenant in Commerce site builder</span></span>

<span data-ttu-id="4d250-321">وبمجرد اكتمال إعداد مستأجر Azure AD B2C، يجب تكوين مستأجر B2C في منشئ موقع Commerce.</span><span class="sxs-lookup"><span data-stu-id="4d250-321">Once setup of your Azure AD B2C tenant is completed, you must configure the B2C tenant in Commerce site builder.</span></span> <span data-ttu-id="4d250-322">تتضمن خطوات التكوين تجميع معلومات تطبيق B2C من مدخل Azure، وإدخال معلومات تطبيق B2C في منشئ الموقع، ثم ربط تطبيق B2C بموقعك وقناتك.</span><span class="sxs-lookup"><span data-stu-id="4d250-322">Configuration steps include collecting B2C application information from the Azure portal, entering that B2C application information into site builder, and then associating the B2C application with your site and channel.</span></span>

### <a name="collect-the-required-application-information"></a><span data-ttu-id="4d250-323">تجميع معلومات التطبيق المطلوبة</span><span class="sxs-lookup"><span data-stu-id="4d250-323">Collect the required application information</span></span>

<span data-ttu-id="4d250-324">لتجميع معلومات التطبيق المطلوبة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="4d250-324">To collect the required application information, follow these steps.</span></span>

1. <span data-ttu-id="4d250-325">في مدخل Azure، انتقل إلى **الصفحة الرئيسية \> Azure AD B2C - تطبيقات**.</span><span class="sxs-lookup"><span data-stu-id="4d250-325">In the Azure portal, go to **Home \> Azure AD B2C - Applications**.</span></span>
1. <span data-ttu-id="4d250-326">حدد تطبيقك، ثم حدد **خصائص** في جزء التنقل الأيسر للحصول على تفاصيل التطبيق.</span><span class="sxs-lookup"><span data-stu-id="4d250-326">Select your application, and then in the left navigation pane select **Properties** to obtain the application details.</span></span>
1. <span data-ttu-id="4d250-327">من المربع **معرف التطبيق**، قم بتجميع معرف التطبيق الخاص بتطبيق B2C الذي تم إنشاؤه في مستأجر B2C.</span><span class="sxs-lookup"><span data-stu-id="4d250-327">From the **Application ID** box, collect the application ID of the B2C application created in your B2C tenant.</span></span> <span data-ttu-id="4d250-328">سيتم إدخاله في وقت لاحق على أنه **GUID‎ العميل** في منشئ الموقع.</span><span class="sxs-lookup"><span data-stu-id="4d250-328">This will later be entered as the **Client GUID** in site builder.</span></span>
1. <span data-ttu-id="4d250-329">تحت **عنوان URL الخاص بالرج**، قم تجميع عنوان URL الخاص بالرد.</span><span class="sxs-lookup"><span data-stu-id="4d250-329">Under **Reply URL**, collect the reply URL.</span></span>
1. <span data-ttu-id="4d250-330">انتقل إلى **الصفحة الرئيسية \> Azure AD B2C – تدفقات المستخدم (السياسات)**، ثم اجمع أسماء كل تدفق سياسة مستخدم.</span><span class="sxs-lookup"><span data-stu-id="4d250-330">Go to **Home \> Azure AD B2C – User flows (policies)**, and then collect the names of each user flow policy.</span></span>

<span data-ttu-id="4d250-331">تعرض الصورة التالية مثالاً عن صفحة **Azure AD B2C - التطبيقات**.</span><span class="sxs-lookup"><span data-stu-id="4d250-331">The following image shows an example of the **Azure AD B2C - Applications** page.</span></span>

![الانتقال إلى تطبيق B2C داخل المستأجر](./media/B2CImage_19.png)

<span data-ttu-id="4d250-333">تعرض الصورة التالية مثالاً عن صفحة **خصائص** التطبيق في Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="4d250-333">The following image shows an example of an application **Properties** page in Azure AD B2C.</span></span> 

![نسخ معرف التطبيق من خصائص تطبيق B2C](./media/B2CImage_21.png)

<span data-ttu-id="4d250-335">تعرض الصورة التالية مثالاً عن سياسات تدفق المستخدم في صفحة **Azure AD B2C – تدفقات المستخدم (السياسات)**.</span><span class="sxs-lookup"><span data-stu-id="4d250-335">The following image shows an example of user flow policies on the **Azure AD B2C – User flows (policies)** page.</span></span>

![جمع أسماء كل تدفق سياسة B2C](./media/B2CImage_22.png)

### <a name="enter-your-aad-b2c-tenant-application-information-into-commerce"></a><span data-ttu-id="4d250-337">إدخال معلومات تطبيق مستأجر AAD B2C في Commerce</span><span class="sxs-lookup"><span data-stu-id="4d250-337">Enter your AAD B2C tenant application information into Commerce</span></span>

<span data-ttu-id="4d250-338">يجب إدخال التفاصيل الخاصة بمستأجر Azure AD B2C في منشئ موقع Commerce قبل ربط مستأجر B2C بموقعك (مواقعك).</span><span class="sxs-lookup"><span data-stu-id="4d250-338">You must enter details of the Azure AD B2C tenant into Commerce site builder before associating the B2C tenant with your site(s).</span></span>

<span data-ttu-id="4d250-339">لإضافة معلومات تطبيق مستأجر AAD B2C إلى Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="4d250-339">To add your AAD B2C tenant application information to Commerce, follow these steps.</span></span>

1. <span data-ttu-id="4d250-340">سجل دخولك كمسؤول إلى منشئ موقع Commerce لبيئتك.</span><span class="sxs-lookup"><span data-stu-id="4d250-340">Sign in as an administrator to Commerce site builder for your environment.</span></span>
1. <span data-ttu-id="4d250-341">في جزء التنقل الأيسر، حدد **إعدادات المستأجر** لتوسيعه.</span><span class="sxs-lookup"><span data-stu-id="4d250-341">In the left navigation pane, select **Tenant Settings**  to expand it.</span></span>
1. <span data-ttu-id="4d250-342">ضمن **إعدادات المستأجر**، حدد **إعدادات B2C**.</span><span class="sxs-lookup"><span data-stu-id="4d250-342">Under **Tenant Settings**, select **B2C Settings**.</span></span> 
1. <span data-ttu-id="4d250-343">في النافذة الرئيسية، إلى جانب **تطبيقات B2C**، حدد **إدارة**.</span><span class="sxs-lookup"><span data-stu-id="4d250-343">In the main window next **B2C Applications**, select **Manage**.</span></span> <span data-ttu-id="4d250-344">(إذا ظهر المستأجر في قائمة تطبيقات B2C، فهذا يعني أنه أضيف بواسطة المسؤول.</span><span class="sxs-lookup"><span data-stu-id="4d250-344">(If your tenant appears in the B2C Applications list, then it was already added by an administrator.</span></span> <span data-ttu-id="4d250-345">تحقق من تطابق البنود الموجودة في الخطوة 6 أدناه مع تطبيق B2C.)</span><span class="sxs-lookup"><span data-stu-id="4d250-345">Verify that the items in step 6 below match your B2C Application.)</span></span>
1. <span data-ttu-id="4d250-346">حدد **إضافة تطبيق B2C**.</span><span class="sxs-lookup"><span data-stu-id="4d250-346">Select **Add B2C Application**.</span></span>
1. <span data-ttu-id="4d250-347">أدخل البنود المطلوبة التالية في النموذج المعروض، باستخدام قيم من مستأجر B2C وتطبيقك.</span><span class="sxs-lookup"><span data-stu-id="4d250-347">Enter the following required items in the form displayed, using values from your B2C tenant and application.</span></span> <span data-ttu-id="4d250-348">يمكن ترك الحقول غير المطلوبة (تلك التي لا توجد علامة نجمية إلى جانبها) فارغة.</span><span class="sxs-lookup"><span data-stu-id="4d250-348">Fields that are not required (those without an asterisk) may be left blank.</span></span>

    - <span data-ttu-id="4d250-349">**اسم التطبيق**: اسم تطبيق B2C، على سبيل المثال "Fabrikam B2C".</span><span class="sxs-lookup"><span data-stu-id="4d250-349">**Application Name**: The name for your B2C Application, for example "Fabrikam B2C".</span></span>
    - <span data-ttu-id="4d250-350">**اسم المستأجر**: اسم مستأجر B2C الخاص بك (على سبيل المثال، استخدم "‏‫شركة الاتحاد للتصنيع‬" إذا ظهر المجال على أنه "fabrikam.onmicrosoft.com" للمستاجر B2C).</span><span class="sxs-lookup"><span data-stu-id="4d250-350">**Tenant Name**: The name of your B2C tenant (for example, use "fabrikam" if the domain appears as "fabrikam.onmicrosoft.com" for the B2C tenant).</span></span> 
    - <span data-ttu-id="4d250-351">**معرف سياسة نسيان كلمة المرور**: معرف سياسة تدفق المستخدم لنسيان كلمة المرور، على سبيل المثال "B2C_1_PasswordReset".</span><span class="sxs-lookup"><span data-stu-id="4d250-351">**Forget Password Policy ID**: The forget password user flow policy ID, for example "B2C_1_PasswordReset".</span></span>
    - <span data-ttu-id="4d250-352">**معرف سياسة التسجيل وتسجيل الدخول**: معرف سياسة تدفق المستخدم للتسجيل وتسجيل الدخول، على سبيل المثال "B2C_1_signup_signin".</span><span class="sxs-lookup"><span data-stu-id="4d250-352">**Signup Signin Policy ID**: The sign up and sign in user flow policy ID, for example "B2C_1_signup_signin".</span></span>
    - <span data-ttu-id="4d250-353">**GUID‏‎ العميل**: معرف تطبيق B2C، على سبيل المثال "22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6".</span><span class="sxs-lookup"><span data-stu-id="4d250-353">**Client GUID**: The B2C application ID, for example "22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6".</span></span>
    - <span data-ttu-id="4d250-354">**معرف سياسة تحرير ملف التعريف**: معرف سياسة تدفق المستخدم لتحرير ملف التعريف، على سبيل المثال، "B2C_1A_ProfileEdit".</span><span class="sxs-lookup"><span data-stu-id="4d250-354">**Edit Profile Policy ID**: The profile editing user flow policy ID, for example "B2C_1A_ProfileEdit".</span></span>

1. <span data-ttu-id="4d250-355">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="4d250-355">Select **OK**.</span></span> <span data-ttu-id="4d250-356">من المفترض أن يظهر الآن اسم تطبيق B2C في القائمة.</span><span class="sxs-lookup"><span data-stu-id="4d250-356">You should now see the name of your B2C application appear in the list.</span></span>
1. <span data-ttu-id="4d250-357">حدد **حفظ** لحفظ تغييراتك.</span><span class="sxs-lookup"><span data-stu-id="4d250-357">Select **Save** to save your changes.</span></span>

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a><span data-ttu-id="4d250-358">ربط تطبيق B2C بموقعك وقناتك</span><span class="sxs-lookup"><span data-stu-id="4d250-358">Associate the B2C application to your site and channel</span></span>

> [!WARNING]
> <span data-ttu-id="4d250-359">إذا كان موقعك مرتبطًا بتطبيق B2C، فسيؤدي التغيير إلى تطبيق B2C مختلف إلى إزالة المراجع الحالية التي تم تأسيسها للمستخدمين الذين قاموا بالتسجيل في هذه البيئة.</span><span class="sxs-lookup"><span data-stu-id="4d250-359">If your site is already associated with a B2C application, changing to a different B2C application will remove the current references established for users already signed up in this environment.</span></span> <span data-ttu-id="4d250-360">إذا حصل التغيير، فإن أي بيانات اعتماد مرتبطة بتطبيق B2C المعين حاليًا لن تكون متوفرة للمستخدمين.</span><span class="sxs-lookup"><span data-stu-id="4d250-360">If changed, any credentials associated with the currently-assigned B2C application will not be available to users.</span></span> 
> 
> <span data-ttu-id="4d250-361">قم بتحديث تطبيق B2C فقط إذا كنت تعمل على اعداد تطبيق B2C الخاص بالقناة للمرة الأولى أو إذا كنت تريد من المستخدمين إعادة التسجيل باستخدام بيانات اعتماد جديدة لهذه القناة مع تطبيق B2C الجديد.</span><span class="sxs-lookup"><span data-stu-id="4d250-361">Only update the B2C application if you are setting up the channel's B2C application for the first time or if you intend to have users re-sign up with new credentials to this channel with the new B2C application.</span></span> <span data-ttu-id="4d250-362">يجب توخي الحذر عند ربط القنوات بتطبيقات B2C، واحرص على تسمية التطبيقات بطريقة واضحة.</span><span class="sxs-lookup"><span data-stu-id="4d250-362">Take caution when associating channels to B2C applications, and name applications clearly.</span></span> <span data-ttu-id="4d250-363">إذا لم تكن قناة مرتبطة بتطبيق B2C في الخطوات أدناه، فإن المستخدمين الذين يسجلون دخولهم إلى هذه القناة لموقعك سيدخلون إلى تطبيق B2C الذي يظهر على أنه **افتراضي** في قائمة **إعدادات المستأجر \> إعدادات B2C** لتطبيقات B2C.</span><span class="sxs-lookup"><span data-stu-id="4d250-363">If a channel is not associated to a B2C application in the steps below, users signing into that channel for your site will be entered into the B2C application showing as **default** in the **Tenant Settings \> B2C Settings** list of B2C applications.</span></span>

<span data-ttu-id="4d250-364">لربط تطبيق B2C بموقعك وقناتك، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="4d250-364">To associate the B2C application to your site and channel, follow these steps.</span></span>

1. <span data-ttu-id="4d250-365">انتقل إلى موقعك في منشئ موقع Commerce.</span><span class="sxs-lookup"><span data-stu-id="4d250-365">Navigate to your site in Commerce site builder.</span></span>
1. <span data-ttu-id="4d250-366">في جزء التنقل الأيسر، حدد **إعدادات الموقع** لتوسيعه.</span><span class="sxs-lookup"><span data-stu-id="4d250-366">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="4d250-367">ضمن **إعدادات الموقع**، حدد **القنوات**.</span><span class="sxs-lookup"><span data-stu-id="4d250-367">Below **Site Settings**, select **Channels**.</span></span>
1. <span data-ttu-id="4d250-368">في النافذة الرئيسية، ضمن **القنوات‏‎**، حدد قناتك.</span><span class="sxs-lookup"><span data-stu-id="4d250-368">In the main window under **Channels**, select your channel.</span></span>
1. <span data-ttu-id="4d250-369">في جزء خصائص القناة إلى اليسار، حدد اسم تطبيق B2C من القائمة المنسدلة **تحديد تطبيق B2C**.</span><span class="sxs-lookup"><span data-stu-id="4d250-369">In the channel properties pane on the right, select your B2C application name from the **Select B2C Application** drop down menu.</span></span>
1. <span data-ttu-id="4d250-370">حدد **إغلاق**، ثم حدد **حفظ ونشر**.</span><span class="sxs-lookup"><span data-stu-id="4d250-370">Select **Close**, and then select **Save and Publish**.</span></span>

## <a name="additional-b2c-information"></a><span data-ttu-id="4d250-371">معلومات B2C إضافية</span><span class="sxs-lookup"><span data-stu-id="4d250-371">Additional B2C information</span></span>

### <a name="customer-migration"></a><span data-ttu-id="4d250-372">ترحيل العملاء</span><span class="sxs-lookup"><span data-stu-id="4d250-372">Customer migration</span></span>

<span data-ttu-id="4d250-373">إذا كنت ترغب في ترحيل سجلات العملاء من نظام موفر الهوية السابق، فيرجى العمل مع فريق Dynamics 365 Commerce لمراجعة احتياجات ترحيل العملاء.</span><span class="sxs-lookup"><span data-stu-id="4d250-373">If you are considering migrating customer records from a previous identity provider platform, please work with the Dynamics 365 Commerce team to review your customer migration needs.</span></span>

<span data-ttu-id="4d250-374">للحصول على وثائق Azure AD B2C إضافة حول ترحيل العملاء، راجع [ترحيل العملاء إلى Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).</span><span class="sxs-lookup"><span data-stu-id="4d250-374">For additional Azure AD B2C documentation on customer migration, see [Migrate users to Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).</span></span>

### <a name="custom-policies"></a><span data-ttu-id="4d250-375">سياسات مخصصة</span><span class="sxs-lookup"><span data-stu-id="4d250-375">Custom policies</span></span>

<span data-ttu-id="4d250-376">للحصول على معلومات إضافية حول تخصيص تفاعلات وتدفقات سياسة Azure AD B2C بما يتجاوز ما تقدمه سياسات B2C القياسية، راجع [السياسات المخصصة في Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom).</span><span class="sxs-lookup"><span data-stu-id="4d250-376">For additional information regarding customizing Azure AD B2C interactions and policy flows beyond what is offered by B2C standard policies, see [Custom policies in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom).</span></span> 

### <a name="secondary-admin"></a><span data-ttu-id="4d250-377">المسؤول الثانوي</span><span class="sxs-lookup"><span data-stu-id="4d250-377">Secondary admin</span></span>

<span data-ttu-id="4d250-378">يمكن إضافة حساب مسؤول ثانوي اختياري في قسم **المستخدمون** في مستأجر B2C.</span><span class="sxs-lookup"><span data-stu-id="4d250-378">An optional, secondary administrator account can be added in the **Users** section of your B2C tenant.</span></span> <span data-ttu-id="4d250-379">قد يكون هذا الحساب مباشرًا أو عامًا.</span><span class="sxs-lookup"><span data-stu-id="4d250-379">This can be a direct account or a general account.</span></span> <span data-ttu-id="4d250-380">إذا أردت مشاركة حساب عبر موارد الفريق، يمكن أيضًا إنشاء حساب عام.</span><span class="sxs-lookup"><span data-stu-id="4d250-380">If you need to share an account across team resources, a common account can also be created.</span></span> <span data-ttu-id="4d250-381">بسبب حساسية البيانات المخزنة في Azure AD B2C، يجب مراقبة حساب عام عن كثب وفق ممارسات الأمان الخاصة بشركتك.</span><span class="sxs-lookup"><span data-stu-id="4d250-381">Due to the sensitivity of the data stored in Azure AD B2C, a common account should be monitored closely per your company's security practices.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4d250-382">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="4d250-382">Additional resources</span></span>

[<span data-ttu-id="4d250-383">تكوين اسم مجالك</span><span class="sxs-lookup"><span data-stu-id="4d250-383">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="4d250-384">نشر مستأجر التجارة الإلكترونية الجديد</span><span class="sxs-lookup"><span data-stu-id="4d250-384">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="4d250-385">إنشاء موقع تجارة إلكترونية</span><span class="sxs-lookup"><span data-stu-id="4d250-385">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="4d250-386">إقران موقع Dynamics 365 Commerce بقناة عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="4d250-386">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="4d250-387">إدارة ملفات robots.txt</span><span class="sxs-lookup"><span data-stu-id="4d250-387">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="4d250-388">تحميل عناوين URL لإعادة التوجيه‬ بشكل مجمع</span><span class="sxs-lookup"><span data-stu-id="4d250-388">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="4d250-389">إعداد صفحات مخصصة لعمليات تسجيل دخول المستخدمين</span><span class="sxs-lookup"><span data-stu-id="4d250-389">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="4d250-390">تكوين مستأجرين متعددين لمتاجرة عمل-مستهلك في بيئة Commerce</span><span class="sxs-lookup"><span data-stu-id="4d250-390">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="4d250-391">إضافة الدعم إلى شبكة تسليم المحتوى (CDN)</span><span class="sxs-lookup"><span data-stu-id="4d250-391">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="4d250-392">تمكين اكتشاف المتجر استنادًا إلى الموقع</span><span class="sxs-lookup"><span data-stu-id="4d250-392">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
