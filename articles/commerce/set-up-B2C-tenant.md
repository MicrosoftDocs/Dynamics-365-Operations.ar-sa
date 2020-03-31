---
title: إعداد مستأجر B2C في Commerce
description: يصف هذا الموضوع كيفية إعداد مستأجري متاجرة بين عمل ومستهلك (B2C) في Azure Active Directory (Azure AD) لمصادقة موقع المستخدم في Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 03/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: BriShoo
ms.search.validFrom: 2020-02-13
ms.dyn365.ops.version: ''
ms.openlocfilehash: a5fca37fb89c723273ef753b102092e2cfb26563
ms.sourcegitcommit: 236672932ffd0a758012ebb7b2df9bc51249c126
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096487"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a><span data-ttu-id="aeb29-103">إعداد مستأجر B2C في Commerce</span><span class="sxs-lookup"><span data-stu-id="aeb29-103">Set up a B2C tenant in Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="aeb29-104">يصف هذا الموضوع كيفية إعداد مستأجري متاجرة بين عمل ومستهلك (B2C) في Azure Active Directory (Azure AD) لمصادقة موقع المستخدم في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="aeb29-104">This topic describes how to set up your Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants for user site authentication in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="aeb29-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="aeb29-105">Overview</span></span>

<span data-ttu-id="aeb29-106">يقوم Dynamics 365 Commerce باستخدام Azure AD B2C لدعم بيانات اعتماد المستخدم وتدفقات المصادقة.</span><span class="sxs-lookup"><span data-stu-id="aeb29-106">Dynamics 365 Commerce uses Azure AD B2C to support user credential and authentication flows.</span></span> <span data-ttu-id="aeb29-107">بإمكان المستخدم التسجيل وتسجيل الدخول وإعادة تعيين كلمة المرور من خلال هذه التدفقات.</span><span class="sxs-lookup"><span data-stu-id="aeb29-107">A user can sign up, sign in, and reset their password through these flows.</span></span> <span data-ttu-id="aeb29-108">يقوم Azure AD B2C بتخزين معلومات المصادقة الحساسة، مثل اسم المستخدم وكلمه المرور.</span><span class="sxs-lookup"><span data-stu-id="aeb29-108">Azure AD B2C stores sensitive user authentication information, such as username and password.</span></span> <span data-ttu-id="aeb29-109">سيقوم سجل المستخدم في مستأجر B2C بتخزين سجل حساب محلي B2C أو سجل موفر هوية اجتماعية B2C.</span><span class="sxs-lookup"><span data-stu-id="aeb29-109">The user record in the B2C tenant will store either a B2C local account record or a B2C social identity provider record.</span></span> <span data-ttu-id="aeb29-110">سترتبط سجلات B2C هذه من جديد بسجل العميل في بيئة Commerce.</span><span class="sxs-lookup"><span data-stu-id="aeb29-110">These B2C records will link back to the customer record in the Commerce environment.</span></span>

## <a name="create-or-link-to-an-existing-aad-b2c-tenant-in-the-azure-portal"></a><span data-ttu-id="aeb29-111">إنشاء مستأجر AAD B2C موجود في مدخل Azure أو الارتباط به</span><span class="sxs-lookup"><span data-stu-id="aeb29-111">Create or link to an existing AAD B2C tenant in the Azure portal</span></span>

1. <span data-ttu-id="aeb29-112">سجل الدخول إلى [مدخل Azure ](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="aeb29-112">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="aeb29-113">من قائمة مدخل Azure، حدد **إنشاء مورد**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-113">From the Azure portal menu, select **Create a resource**.</span></span> <span data-ttu-id="aeb29-114">احرص على استخدام الاشتراك والدليل الذي سيتم توصيله ببيئة Commerce.</span><span class="sxs-lookup"><span data-stu-id="aeb29-114">Be sure to use the subscription and directory that will be connected with your Commerce environment.</span></span>

    ![إنشاء مورد في مدخل Azure](./media/B2CImage_1.png)

1. <span data-ttu-id="aeb29-116">انتقل إلى **الهوية \> Azure Active Directory B2C**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-116">Go to **Identity \> Azure Active Directory B2C**.</span></span>
1. <span data-ttu-id="aeb29-117">عند وصولك إلى صفحة **إنشاء مستأجر B2C جديد أو الارتباط بمستأجر موجود**، استخدم أحد الخيارات أدناه الأكثر ملاءمة لاحتياجات شركتك:</span><span class="sxs-lookup"><span data-stu-id="aeb29-117">Once on the **Create New B2C Tenant or Link to existing Tenant** page, use one of the options below that best suits your company's needs:</span></span>

    - <span data-ttu-id="aeb29-118">**إنشاء مستأجر Azure AD B2C جديد**: استخدم هذا الخيار لإنشاء مستأجر AAD B2C جديد.</span><span class="sxs-lookup"><span data-stu-id="aeb29-118">**Create a new Azure AD B2C Tenant**: Use this option to create a new AAD B2C tenant.</span></span>
        1. <span data-ttu-id="aeb29-119">حدد **إنشاء مستأجر Azure AD B2C جديد**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-119">Select **Create a new Azure AD B2C Tenant**.</span></span>
        1. <span data-ttu-id="aeb29-120">ضمن **اسم المؤسسة**، أدخل اسم المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="aeb29-120">Under **Organization name**, enter the organization name.</span></span>
        1. <span data-ttu-id="aeb29-121">ضمن **اسم المجال الأولي**، أدخل اسم المجال الأولي‏‎.</span><span class="sxs-lookup"><span data-stu-id="aeb29-121">Under **Initial domain name**, enter the initial domain name.</span></span>
        1. <span data-ttu-id="aeb29-122">في **البلد أو المنطقة**، حدد البلد أو المنطقة.</span><span class="sxs-lookup"><span data-stu-id="aeb29-122">For **Country or region**, select the country or region.</span></span>
        1. <span data-ttu-id="aeb29-123">حدد **إنشاء** لإنشاء المستأجر.</span><span class="sxs-lookup"><span data-stu-id="aeb29-123">Select **Create** to create the tenant.</span></span>

     ![إنشاء مستأجر Azure AD جديد](./media/B2CImage_2.png)

     - <span data-ttu-id="aeb29-125">**ربط مستأجر Azure AD B2C موجود باشتراكي في Azure**: استخدم هذا الخيار إذا كان لديك مستأجر Azure AD B2C تريد الارتباط به.</span><span class="sxs-lookup"><span data-stu-id="aeb29-125">**Link an existing Azure AD B2C Tenant to my Azure subscription**: Use this option if you already have an Azure AD B2C tenant you want to link to.</span></span>
        1. <span data-ttu-id="aeb29-126">حدد **ربط مستأجر Azure AD B2C موجود باشتراكي في Azure**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-126">Select **Link an existing Azure AD B2C Tenant to my Azure subscription**.</span></span>
        1. <span data-ttu-id="aeb29-127">في **مستأجر Azure AD B2C**، حدد مستأجر B2C المناسب.</span><span class="sxs-lookup"><span data-stu-id="aeb29-127">For **Azure AD B2C Tenant**, select the appropriate B2C tenant.</span></span> <span data-ttu-id="aeb29-128">إذا ظهرت الرسالة "لم يتم العثور على مستأجري B2C مؤهلين" في مربع التحديد، فهذا يعني عدم وجود مستأجر B2C مؤهل ويجب إنشاء واحد جديد.</span><span class="sxs-lookup"><span data-stu-id="aeb29-128">If the message "No eligible B2C Tenants found" appears in the selection box, you do not have an existing eligible B2C tenant and will need to create a new one.</span></span>
        1. <span data-ttu-id="aeb29-129">في **مجموعة الموارد**، حدد **إنشاء جديد**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-129">For **Resource group**, select **Create new**.</span></span> <span data-ttu-id="aeb29-130">أدخل **اسم** مجموعة الموارد التي ستحتوي على المستأجر، وحدد، **موقع مجموعة الموارد**، ثم حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-130">Enter a **Name** for the resource group that will contain the tenant, select the **Resource group location**, and then select **Create**.</span></span>

    ![ربط مستأجر Azure AD B2C موجود باشتراك Azure](./media/B2CImage_3.png)

1. <span data-ttu-id="aeb29-132">بعد إنشاء دليل Azure AD B2C الجديد (قد يستغرق هذا الأمر لحظات قليلة)، سيظهر ارتباط إلى الدليل الجديد على لوحة المعلومات.</span><span class="sxs-lookup"><span data-stu-id="aeb29-132">Once the new Azure AD B2C directory is created (this may take a few moments), a link to the new directory will appear on the dashboard.</span></span> <span data-ttu-id="aeb29-133">سيوجهك هذا الارتباط إلى صفحة "مرحباً بك في Azure Active Directory B2C".</span><span class="sxs-lookup"><span data-stu-id="aeb29-133">This link will direct you to the "Welcome to Azure Active Directory B2C" page.</span></span>

    ![ارتباط إلى دليل AAD جديد](./media/B2CImage_4.png)

> [!NOTE]
> <span data-ttu-id="aeb29-135">إذا كانت لديك اشتراكات متعددة داخل حساب Azure أو قمت بإعداد مستأجر B2C بدون إنشاء ارتباط إلى اشتراك نشط، سيقوم شعار **استكشاف الأخطاء وإصلاحها** بتوجيهك لربط المستأجر باشتراك.</span><span class="sxs-lookup"><span data-stu-id="aeb29-135">If you have multiple subscriptions within your Azure account or have set up the B2C tenant without linking to an active subscription, a **Troubleshoot** banner will direct you to link the tenant to a subscription.</span></span> <span data-ttu-id="aeb29-136">حدد رسالة استكشاف الأخطاء وإصلاحها واتبع الإرشادات لحل مشكلة الاشتراك.</span><span class="sxs-lookup"><span data-stu-id="aeb29-136">Select the troubleshooting message and follow the instructions to resolve the subscription issue.</span></span>

<span data-ttu-id="aeb29-137">تبين الصورة التالية مثالاً عن شعار **استكشاف الأخطاء وإصلاحها في Azure AD B2C**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-137">The following image shows an example of an Azure AD B2C **Troubleshoot** banner.</span></span>

![تحذير يشير إلى عدم وجود اشتراك نشط لدى الدليل](./media/B2CImage_5.png)

## <a name="create-the-b2c-application"></a><span data-ttu-id="aeb29-139">إنشاء تطبيق B2C</span><span class="sxs-lookup"><span data-stu-id="aeb29-139">Create the B2C application</span></span>

<span data-ttu-id="aeb29-140">بعد إنشاء مستأجر B2C، ستقوم بإنشاء تطبيق B2C داخل المستأجر للتفاعل مع إجراءات Commerce.</span><span class="sxs-lookup"><span data-stu-id="aeb29-140">Once the B2C tenant has been created, you will create a B2C application within the tenant to interact with the Commerce actions.</span></span>

<span data-ttu-id="aeb29-141">لإنشاء تطبيق B2C، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="aeb29-141">To create the B2C application, follow these steps.</span></span>

1. <span data-ttu-id="aeb29-142">في مدخل Azure، حدد **التطبيقات** ثم حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-142">In the Azure portal, select **Applications** and then select **Add**.</span></span>
1. <span data-ttu-id="aeb29-143">ضمن **الاسم**، أدخل اسم تطبيق AAD B2C المطلوب.</span><span class="sxs-lookup"><span data-stu-id="aeb29-143">Under **Name**, enter the name of the desired AAD B2C application.</span></span>
1. <span data-ttu-id="aeb29-144">ضمن **تطبيق الويب/واجهة API‏‎ للويب**، في **تضمين تطبيق الويب/واجهة API‏‎ للويب**، حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-144">Under **Web App/Web API**, for **Include web app / web API**, select **Yes**.</span></span>
1. <span data-ttu-id="aeb29-145">في **السماح بالتدفق الضمني**، حدد **نعم** (القيمة الافتراضية).</span><span class="sxs-lookup"><span data-stu-id="aeb29-145">For **Allow implicit flow**, select **Yes** (the default value).</span></span>
1. <span data-ttu-id="aeb29-146">ضمن **عنوان URL‏‎ الخاص بالرد**، أدخل عناوين URL‏‎ الخاصة بالرد المخصصة.</span><span class="sxs-lookup"><span data-stu-id="aeb29-146">Under **Reply URL**, enter your dedicated reply URLs.</span></span> <span data-ttu-id="aeb29-147">راجع [عناوين URL‏‎ الخاصة بالرد](#reply-urls) أدناه للحصول على معلومات حول عناوين URL‏‎ الخاصة بالرد وكيفية تنسيقها هنا.</span><span class="sxs-lookup"><span data-stu-id="aeb29-147">See [Reply URLs](#reply-urls) below for information on reply URLs and how to format them here.</span></span>
1. <span data-ttu-id="aeb29-148">في **تضمين العميل الأصلي**، حدد **لا** (القيمة الافتراضية).</span><span class="sxs-lookup"><span data-stu-id="aeb29-148">For **Include native client**, select **No** (the default value).</span></span>
1. <span data-ttu-id="aeb29-149">حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-149">Select **Create**.</span></span>

### <a name="reply-urls"></a><span data-ttu-id="aeb29-150">عناوين URL الخاصة بالرد</span><span class="sxs-lookup"><span data-stu-id="aeb29-150">Reply URLs</span></span>

<span data-ttu-id="aeb29-151">تعتبر عناوين URL الخاصة بالرد مهمة لأنها تسمح بقائمة بيضاء للمجالات المرتجعة عندما يقوم موقعك باستدعاء Azure AD B2C لمصادقة مستخدم.</span><span class="sxs-lookup"><span data-stu-id="aeb29-151">Reply URLs are important as they allow a whitelist of the return domains when your site calls Azure AD B2C to authenticate a user.</span></span> <span data-ttu-id="aeb29-152">يسمح ذلك بإرجاع المستخدم الذي تمت مصادقته إلى المجال الذي يتم تسجيل الدخول منه (مجال موقعك).</span><span class="sxs-lookup"><span data-stu-id="aeb29-152">This allows the return of the authenticated user back to the domain from which they are signing into (your site domain).</span></span> 

<span data-ttu-id="aeb29-153">في المربع **عنوان URL الخاص بالرد** على شاشة **Azure AD B2c - تطبيقات \> تطبيق جديد**، تحتاج إلى إضافة خطوط منفصلة لكل من مجال الموقع و(بعد تزويد بيئتك) عنوان URL المنشأ في Commerce.</span><span class="sxs-lookup"><span data-stu-id="aeb29-153">In the **Reply URL** box on the **Azure AD B2c - Applications \> New application** screen, you need to add separate lines for both your site domain and (once your environment is provisioned) the Commerce-generated URL.</span></span> <span data-ttu-id="aeb29-154">يجب أن تستخدم عناوين URL هذه دائمًا تنسيق URL صالحًا ويجب أن تكون عناوين URL أساسية فقط (لا توجد أي خطوط مائلة أمامية أو مسارات).</span><span class="sxs-lookup"><span data-stu-id="aeb29-154">These URLs must always use a valid URL format and must be base URLs only (no trailing forward slashes or paths).</span></span> <span data-ttu-id="aeb29-155">يجب إلحاق السلسلة ``/_msdyn365/authresp`` بعناوين URL الأساسية، كما في الأمثلة التالية:</span><span class="sxs-lookup"><span data-stu-id="aeb29-155">The string ``/_msdyn365/authresp`` then needs to be appended to the base URLs, as in the following examples.</span></span>

- ``https://fabrikam.com/_msdyn365/authresp``
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="create-user-flow-policies"></a><span data-ttu-id="aeb29-156">إنشاء سياسات تدفق المستخدم</span><span class="sxs-lookup"><span data-stu-id="aeb29-156">Create user flow policies</span></span>

<span data-ttu-id="aeb29-157">سياسات تدفق المستخدم هي السياسات التي يستخدمها Azure AD B2C لتوفير تجارب مستخدم آمنة للتسجيل وتسجيل الدخول وتحرير ملف التعريف ونسيان كلمه المرور.</span><span class="sxs-lookup"><span data-stu-id="aeb29-157">User flows are the policies Azure AD B2C uses to provide secure sign in, sign up, edit profile, and forget password user experiences.</span></span> <span data-ttu-id="aeb29-158">يستخدم Dynamics 365 Commerce  هذه التدفقات لتنفيذ إجراءات السياسة للتفاعل مع مستأجر Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="aeb29-158">Dynamics 365 Commerce uses these flows to perform the policy actions to interact with the Azure AD B2C tenant.</span></span> <span data-ttu-id="aeb29-159">عندما يتفاعل المستخدم مع هذه السياسات، يعاد توجيههم إلى مستأجر Azure AD B2C لتنفيذ الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="aeb29-159">When a user interacts with these policies, they are redirected to the Azure AD B2C tenant to perform the actions.</span></span>

<span data-ttu-id="aeb29-160">يوفر Azure AD B2C ثلاثة أنواع من تدفقات المستخدم الأساسية:</span><span class="sxs-lookup"><span data-stu-id="aeb29-160">Azure AD B2C provides three basic user flow types:</span></span>
- <span data-ttu-id="aeb29-161">التسجيل وتسجيل الدخول</span><span class="sxs-lookup"><span data-stu-id="aeb29-161">Sign up and sign in</span></span>
- <span data-ttu-id="aeb29-162">تحرير ملف التعريف</span><span class="sxs-lookup"><span data-stu-id="aeb29-162">Profile editing</span></span>
- <span data-ttu-id="aeb29-163">إعادة تعيين كلمة المرور</span><span class="sxs-lookup"><span data-stu-id="aeb29-163">Password reset</span></span>

<span data-ttu-id="aeb29-164">يمكنك اختيار استخدام تدفقات المستخدم الافتراضية التي يوفرها Azure AD، والتي ستقوم بعرض صفحة يستضيفها AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="aeb29-164">You can choose to use the default user flows provided by Azure AD, which will display a page hosted by AAD B2C.</span></span> <span data-ttu-id="aeb29-165">أو يمكنك إنشاء صفحة HTML للتحكم في شكل وأسلوب تجارب تدفق المستخدم هذه.</span><span class="sxs-lookup"><span data-stu-id="aeb29-165">Alternately, you can create an HTML page to control the look and feel of these user flow experiences.</span></span> 

<span data-ttu-id="aeb29-166">لتخصيص صفحات سياسة المستخدم لـ Dynamics 365 Commerce، راجع [إعداد صفحات مخصصة لعمليات تسجيل دخول المستخدمين‬](custom-pages-user-logins.md).</span><span class="sxs-lookup"><span data-stu-id="aeb29-166">To customize the user policy pages for Dynamics 365 Commerce, see [Set up custom pages for user logins](custom-pages-user-logins.md).</span></span> <span data-ttu-id="aeb29-167">للحصول على معلومات إضافية، راجع [تخصيص واجهة تجارب المستخدم في Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).</span><span class="sxs-lookup"><span data-stu-id="aeb29-167">For additional information, see [Customize the interface of user experiences in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).</span></span>

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a><span data-ttu-id="aeb29-168">إنشاء عملية تسجيل وتسجيل دخول في سياسة تدفق المستخدم</span><span class="sxs-lookup"><span data-stu-id="aeb29-168">Create a sign up and sign in user flow policy</span></span>

<span data-ttu-id="aeb29-169">لإنشاء عملية تسجيل وتسجيل دخول في سياسة تدفق المستخدم، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="aeb29-169">To create a sign up and sign in user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="aeb29-170">في مدخل Azure، حدد **تدفقات المستخدم (السياسات)** في جزء التنقل الأيمن.</span><span class="sxs-lookup"><span data-stu-id="aeb29-170">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="aeb29-171">في صفحة **Azure AD B2C – تدفقات المستخدم (السياسات)‬‏‫**، حدد **تدفق مستخدم جديد‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-171">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="aeb29-172">في علامة التبويب **موصي به**، حدد **التسجيل وتسجيل الدخول**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-172">On the **Recommended** tab, select **Sign up and sign in**.</span></span>
1. <span data-ttu-id="aeb29-173">ضمن **الاسم**، أدخل اسمًا للسياسة.</span><span class="sxs-lookup"><span data-stu-id="aeb29-173">Under **Name**, enter a policy name.</span></span> <span data-ttu-id="aeb29-174">سيظهر هذا الاسم بعد ذلك مع بادئة يعينها المدخل (على سبيل المثال، "B2C_1_").</span><span class="sxs-lookup"><span data-stu-id="aeb29-174">This name will display afterwards with a prefix the portal assigns (for example, "B2C_1_").</span></span>
1. <span data-ttu-id="aeb29-175">ضمن **موفرو الهوية**، حدد خانة الاختيار المناسبة.</span><span class="sxs-lookup"><span data-stu-id="aeb29-175">Under **Identity providers**, select the appropriate check box.</span></span>
1. <span data-ttu-id="aeb29-176">ضمن **مصادقة متعددة العوامل**، حدد الاختيار المناسب لشركتك.</span><span class="sxs-lookup"><span data-stu-id="aeb29-176">Under **Multifactor Authentication**, select the appropriate choice for your company.</span></span> 
1. <span data-ttu-id="aeb29-177">ضمن **سمات ومطالبات المستخدم**، حدد الخيارات لجمع السمات أو إرجاع المطالبات حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="aeb29-177">Under **User attributes and claims**, select options to collect attributes or return claims as appropriate.</span></span> <span data-ttu-id="aeb29-178">يحتاج Commerce إلى الخيارات الافتراضية التالية:</span><span class="sxs-lookup"><span data-stu-id="aeb29-178">Commerce requires the following default options:</span></span>

    | <span data-ttu-id="aeb29-179">**جمع سمة**</span><span class="sxs-lookup"><span data-stu-id="aeb29-179">**Collect  attribute**</span></span> | <span data-ttu-id="aeb29-180">**إرجاع مطالبة**</span><span class="sxs-lookup"><span data-stu-id="aeb29-180">**Return  claim**</span></span> |
    | ---------------------- | ----------------- |
    |                        | <span data-ttu-id="aeb29-181">عناوين البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="aeb29-181">Email Addresses</span></span>   |
    | <span data-ttu-id="aeb29-182">الاسم المحدد</span><span class="sxs-lookup"><span data-stu-id="aeb29-182">Given Name</span></span>             | <span data-ttu-id="aeb29-183">الاسم المحدد</span><span class="sxs-lookup"><span data-stu-id="aeb29-183">Given Name</span></span>        |
    |                        | <span data-ttu-id="aeb29-184">موفر الهوية‬</span><span class="sxs-lookup"><span data-stu-id="aeb29-184">Identity Provider</span></span> |
    | <span data-ttu-id="aeb29-185">اللقب</span><span class="sxs-lookup"><span data-stu-id="aeb29-185">Surname</span></span>                | <span data-ttu-id="aeb29-186">اللقب</span><span class="sxs-lookup"><span data-stu-id="aeb29-186">Surname</span></span>           |
    |                        | <span data-ttu-id="aeb29-187">معرف الكائن الخاص بالمستخدم</span><span class="sxs-lookup"><span data-stu-id="aeb29-187">User’s Object ID</span></span>  |

1. <span data-ttu-id="aeb29-188">حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-188">Select **Create**.</span></span>

<span data-ttu-id="aeb29-189">الصورة التالية هي مثال تدفق المستخدم للتسجيل وتسجيل الدخول إلى Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="aeb29-189">The following image is an example of the Azure AD B2C sign up and sign in user flow.</span></span>

![إعدادات سياسة التسجيل وتسجيل الدخول](./media/B2CImage_11.png)

<span data-ttu-id="aeb29-191">تظهر الصورة التالية الخيار **تشغيل تدفق المستخدم** في Azure AD B2C تدفق المستخدم للتسجيل وتسجيل الدخول إلى B2C.</span><span class="sxs-lookup"><span data-stu-id="aeb29-191">The following image shows the **Run user flow** option in the Azure AD B2C sign up and sign in user flow.</span></span>

![الخيار "تشغيل تدفق المستخدم‬‏‫" في تدفق السياسة](./media/B2CImage_23.png)
   
### <a name="create-a-profile-editing-user-flow-policy"></a><span data-ttu-id="aeb29-193">إنشاء سياسة تدفق المستخدم لتحرير ملف التعريف</span><span class="sxs-lookup"><span data-stu-id="aeb29-193">Create a profile editing user flow policy</span></span>

<span data-ttu-id="aeb29-194">لإنشاء سياسة تدفق المستخدم لتحرير ملف التعريف، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="aeb29-194">To create a profile editing user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="aeb29-195">في مدخل Azure، حدد **تدفقات المستخدم (السياسات)** في جزء التنقل الأيمن.</span><span class="sxs-lookup"><span data-stu-id="aeb29-195">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="aeb29-196">في صفحة **Azure AD B2C – تدفقات المستخدم (السياسات)‬‏‫**، حدد **تدفق مستخدم جديد‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-196">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="aeb29-197">على علامة التبويب **موصى به**، حدد **تحرير ملف التعريف**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-197">On the **Recommended** tab, select **Profile editing**.</span></span>
1. <span data-ttu-id="aeb29-198">ضمن **الاسم**، أدخل تدفق المستخدم لتحرير ملف التعريف.</span><span class="sxs-lookup"><span data-stu-id="aeb29-198">Under **Name**, enter the profile editing user flow.</span></span> <span data-ttu-id="aeb29-199">سيظهر هذا الاسم بعد ذلك مع بادئة يعينها المدخل (على سبيل المثال، "B2C_1_").</span><span class="sxs-lookup"><span data-stu-id="aeb29-199">This name will display afterwards with a prefix the portal assigns (for example, "B2C_1_").</span></span>
1. <span data-ttu-id="aeb29-200">ضمن **موفرو الهوية**، حدد **، تسجيل الدخول إلى الحساب المحلي**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-200">Under **Identity providers**, select **Local Account SignIn**.</span></span>
1. <span data-ttu-id="aeb29-201">ضمن **سمات المستخدم**، حدد خانات الاختيار التالية:</span><span class="sxs-lookup"><span data-stu-id="aeb29-201">Under **User attributes**, select the following check boxes:</span></span>
    - <span data-ttu-id="aeb29-202">**عناوين البريد الإلكتروني** (**إرجاع مطالبة** فقط)</span><span class="sxs-lookup"><span data-stu-id="aeb29-202">**Email Addresses** (**Return claim** only)</span></span>
    - <span data-ttu-id="aeb29-203">**الاسم المحدد** (**جمع السمة** و**إرجاع مطالبة‬‏‫**)</span><span class="sxs-lookup"><span data-stu-id="aeb29-203">**Given Name** (**Collect attribute** and **Return claim**)</span></span>
    - <span data-ttu-id="aeb29-204">**موفر‏‎ الهوية** (**إرجاع مطالبة‬‏‫** فقط)</span><span class="sxs-lookup"><span data-stu-id="aeb29-204">**Identity Provider** (**Return claim** only)</span></span>
    - <span data-ttu-id="aeb29-205">**اللقب‬‏‫** (**جمع السمة** و**إرجاع مطالبة‬‏‫**)</span><span class="sxs-lookup"><span data-stu-id="aeb29-205">**Surname** (**Collect attribute** and **Return claim**)</span></span>
    - <span data-ttu-id="aeb29-206">**معرف الكائن الخاص بالمستخدم‬** (**إرجاع مطالبة** فقط)</span><span class="sxs-lookup"><span data-stu-id="aeb29-206">**User's Object ID** (**Return claim** only)</span></span>
1. <span data-ttu-id="aeb29-207">حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-207">Select **Create**.</span></span>

<span data-ttu-id="aeb29-208">تعرض الصورة التالية مثالاً عن تدفق المستخدم لتحرير مرف تعريف Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="aeb29-208">The following image shows an example of the Azure AD B2C profile editing user flow.</span></span>

![إنشاء تدفق المستخدم لتحرير ملف التعريف](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a><span data-ttu-id="aeb29-210">إنشاء سياسة تدفق المستخدم لإعادة تعيين كلمة المرور</span><span class="sxs-lookup"><span data-stu-id="aeb29-210">Create a password reset user flow policy</span></span>

<span data-ttu-id="aeb29-211">لإنشاء سياسة تدفق المستخدم لإعادة تعيين كلمة المرور، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="aeb29-211">To create a password reset user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="aeb29-212">في مدخل Azure، حدد **تدفقات المستخدم (السياسات)** في جزء التنقل الأيمن.</span><span class="sxs-lookup"><span data-stu-id="aeb29-212">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="aeb29-213">في صفحة **Azure AD B2C – تدفقات المستخدم (السياسات)‬‏‫**، حدد **تدفق مستخدم جديد‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-213">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="aeb29-214">على علامة التبويب **موصى به**، حدد **إعادة تعيين كلمة المرور**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-214">On the **Recommended** tab, select **Password Reset**.</span></span>
1. <span data-ttu-id="aeb29-215">ضمن **الاسم**، أدخل اسمًا لتدفق المستخدم لإعادة تعيين كلمة المرور.</span><span class="sxs-lookup"><span data-stu-id="aeb29-215">Under **Name**, enter a name for the password reset user flow.</span></span>
1. <span data-ttu-id="aeb29-216">ضمن **موفرو الهوية**، حدد **إعادة تعيين كلمة المرور باستخدام عنوان البريد الكتروني**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-216">Under **Identity providers**, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="aeb29-217">حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-217">Select **Create**.</span></span>
1. <span data-ttu-id="aeb29-218">ضمن **مطالبات التطبيق**، حدد خانات الاختيار التالية:</span><span class="sxs-lookup"><span data-stu-id="aeb29-218">Under **Application claims**, select the following check boxes:</span></span>
    - <span data-ttu-id="aeb29-219">**البريد الإلكتروني**</span><span class="sxs-lookup"><span data-stu-id="aeb29-219">**Email**</span></span>
    - <span data-ttu-id="aeb29-220">**العناوين**</span><span class="sxs-lookup"><span data-stu-id="aeb29-220">**Addresses**</span></span>
    - <span data-ttu-id="aeb29-221">**الاسم المحدد**</span><span class="sxs-lookup"><span data-stu-id="aeb29-221">**Given Name**</span></span>
    - <span data-ttu-id="aeb29-222">**اللقب**</span><span class="sxs-lookup"><span data-stu-id="aeb29-222">**Surname**</span></span>
    - <span data-ttu-id="aeb29-223">**معرف الكائن الخاص بالمستخدم**</span><span class="sxs-lookup"><span data-stu-id="aeb29-223">**User's Object ID**</span></span>
1. <span data-ttu-id="aeb29-224">حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-224">Select **Create**.</span></span>

<span data-ttu-id="aeb29-225">توضح الصورة التالية المكان حيث يجب تعيين الخيار **إعادة تعيين كلمة المرور باستخدام عنوان بريد إلكتروني** في تدفق المستخدم لإعادة تعيين كلمة المرور في Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="aeb29-225">The following image shows where to set **Reset Password using mail address** in the Azure AD B2C password reset user flow.</span></span>

![تعيين "إعادة تعيين كلمة المرور باستخدام عنوان بريد إلكتروني" في سياسة إعادة تعيين كلمة المرور](./media/B2CImage_13.png)

## <a name="add-social-identity-providers-optional"></a><span data-ttu-id="aeb29-227">إضافة موفري الهوية الاجتماعية (اختياري)</span><span class="sxs-lookup"><span data-stu-id="aeb29-227">Add social identity providers (Optional)</span></span>

<span data-ttu-id="aeb29-228">يسمح موفرو الهوية الاجتماعية للمستخدمين باستخدام حساباتهم الاجتماعية للمصادقة.</span><span class="sxs-lookup"><span data-stu-id="aeb29-228">Social identity providers allow users to use their social accounts for authentication.</span></span> <span data-ttu-id="aeb29-229">تعتبر إضافة مصادقة موفر الهوية الاجتماعية اختيارية في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="aeb29-229">Adding social identity provider authentication is optional in Dynamics 365 Commerce.</span></span> 

<span data-ttu-id="aeb29-230">إذا لم تتم إضافة مصادقة موفر الهوية الاجتماعية، ستكون ملفات تعريف Azure AD B2C الافتراضية ملفات التعريف الأساسية لقاعدة المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="aeb29-230">If social identity provider authentication is not added, the default Azure AD B2C profiles will be the main profiles for your user base.</span></span> <span data-ttu-id="aeb29-231">سيقوم المستخدمون بتحديد اسم المستخدم (عنوان بريدهم الإلكتروني المفضل) وتعيين كلمة مرور.</span><span class="sxs-lookup"><span data-stu-id="aeb29-231">Users will select their own username (their preferred email address) and set a password.</span></span> <span data-ttu-id="aeb29-232">سيقوم Azure AD B2C بمصادقة المستخدمين بشكل مباشر.</span><span class="sxs-lookup"><span data-stu-id="aeb29-232">Azure AD B2C will authenticate users directly.</span></span> 

<span data-ttu-id="aeb29-233">إذا تمت إضافة مصادقة موفر الهوية الاجتماعية واختار أحد المستخدمين أحد موفري الهوية الاجتماعية المعروضين، فسيتم مع ذلك إنشاء كيان في مستأجر Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="aeb29-233">If social identity provider authentication is added and a user chooses one of the social identity providers offered, an entity is still created in the Azure AD B2C tenant.</span></span> <span data-ttu-id="aeb29-234">سيقوم Azure AD B2C عندئذٍ بمصادقة بيانات اعتماد المستخدم مع موفر الهوية الاجتماعية.</span><span class="sxs-lookup"><span data-stu-id="aeb29-234">Azure AD B2C will then authenticate the user's credentials with the social identity provider.</span></span>

> [!NOTE]
> <span data-ttu-id="aeb29-235">يؤدي تسجيل دخول الموفر إلى إنشاء سجل في مستأجر B2C، ولكن بتنسيق مختلف عن الحسابات المحلية لأنه سيقوم باستدعاء مرجع موفر الهوية الاجتماعية الخارجي للمصادقة.</span><span class="sxs-lookup"><span data-stu-id="aeb29-235">The identity provider sign in creates a record in the B2C tenant, but in a different format than local accounts since it will call the external social identity provider reference for authentication.</span></span> <span data-ttu-id="aeb29-236">يمكن للمستخدم استخدام عنوان البريد الإلكتروني نفسه عبر موفري الهويات الاجتماعية، مما يعني أن اسم المستخدم للبريد الإلكتروني الذي تم استخدامه للمصادقة قد لا يكون فريدًا للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="aeb29-236">The user can use the same email address across social identity providers, meaning that the email username used for authentication may not be unique to the tenant.</span></span> <span data-ttu-id="aeb29-237">سيفرض Azure AD B2C فقط وجود عنوان بريد إلكتروني فريد للمستخدمين على حسابات B2C المحلية.</span><span class="sxs-lookup"><span data-stu-id="aeb29-237">Azure AD B2C will only enforce that users have a unique email address on local B2C accounts.</span></span>

<span data-ttu-id="aeb29-238">قبل أن تتمكن من إضافة موفر هوية اجتماعية للمصادقة، يجب الانتقال إلى مدخل موفر الهوية وإعداد تطبيق موفر هوية كما هو موضح في وثائق Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="aeb29-238">Before you can add a social identity provider for authentication, you must go to the identity provider's portal and set up an identity provider application as instructed in the Azure AD B2C documentation.</span></span> <span data-ttu-id="aeb29-239">توجد أدناه قائمة بالارتباطات إلى الوثائق.</span><span class="sxs-lookup"><span data-stu-id="aeb29-239">A list of links to the documentation is provided below.</span></span>

- [<span data-ttu-id="aeb29-240">Amazon</span><span class="sxs-lookup"><span data-stu-id="aeb29-240">Amazon</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [<span data-ttu-id="aeb29-241">Azure AD (مستأجر واحد)</span><span class="sxs-lookup"><span data-stu-id="aeb29-241">Azure AD (Single Tenant)</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [<span data-ttu-id="aeb29-242">حساب Microsoft</span><span class="sxs-lookup"><span data-stu-id="aeb29-242">Microsoft Account</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [<span data-ttu-id="aeb29-243">Facebook</span><span class="sxs-lookup"><span data-stu-id="aeb29-243">Facebook</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [<span data-ttu-id="aeb29-244">GitHub</span><span class="sxs-lookup"><span data-stu-id="aeb29-244">GitHub</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [<span data-ttu-id="aeb29-245">Google</span><span class="sxs-lookup"><span data-stu-id="aeb29-245">Google</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [<span data-ttu-id="aeb29-246">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="aeb29-246">LinkedIn</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [<span data-ttu-id="aeb29-247">OpenID Connect</span><span class="sxs-lookup"><span data-stu-id="aeb29-247">OpenID Connect</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [<span data-ttu-id="aeb29-248">Twitter</span><span class="sxs-lookup"><span data-stu-id="aeb29-248">Twitter</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a><span data-ttu-id="aeb29-249">إضافة موفر هوية اجتماعية وإعداده</span><span class="sxs-lookup"><span data-stu-id="aeb29-249">Add and set up a social identity provider</span></span>

<span data-ttu-id="aeb29-250">لإضافة موفر هوية اجتماعية وإعداده، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="aeb29-250">To add and set up a social identity provider, follow these steps.</span></span>  

1. <span data-ttu-id="aeb29-251">في مدخل Azure، انتقل إلى **موفرو الهوية**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-251">In the Azure portal, navigate to **Identity Providers**.</span></span>
1. <span data-ttu-id="aeb29-252">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-252">Select **Add**.</span></span> <span data-ttu-id="aeb29-253">تظهر الشاشة **إضافة موفر هوية**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-253">The **Add identity provider** screen appears.</span></span>
1. <span data-ttu-id="aeb29-254">ضمن **الاسم**، أدخل الاسم المطلوب عرضه للمستخدمين على شاشة تسجيل الدخول.</span><span class="sxs-lookup"><span data-stu-id="aeb29-254">Under **Name**, enter the name to be displayed to users on your sign in screen.</span></span>
1. <span data-ttu-id="aeb29-255">ضمن **نوع موفر الهوية**، حدد موفر هوية من القائمة.</span><span class="sxs-lookup"><span data-stu-id="aeb29-255">Under **Identity provider type**, select an identity provider from the list.</span></span>
1. <span data-ttu-id="aeb29-256">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-256">Select **OK**.</span></span>
1. <span data-ttu-id="aeb29-257">حدد **إعداد موفر الهوية هذا** للوصول إلى شاشة **إعداد موفر الهوية الاجتماعية**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-257">Select **Set up this identity provider** to access the **Set up the social identity provider** screen.</span></span>
1. <span data-ttu-id="aeb29-258">ضمن **معرف العميل**، أدخل معرف العميل كما تم الحصول عليه من إعداد تطبيق موفر الهوية.</span><span class="sxs-lookup"><span data-stu-id="aeb29-258">Under **Client ID**, enter the client ID as obtained from the identity provider application setup.</span></span>
1. <span data-ttu-id="aeb29-259">ضمن **سر العميل**، أدخل سر العميل كما تم الحصول عليه من إعداد تطبيق موفر الهوية.</span><span class="sxs-lookup"><span data-stu-id="aeb29-259">Under **Client secret**, enter the client secret as obtained from the identity provider application setup.</span></span>
1. <span data-ttu-id="aeb29-260">إرفاق تدفق المستخدم لسياسات التسجيل:</span><span class="sxs-lookup"><span data-stu-id="aeb29-260">Attach user flow for sign in sign up policies:</span></span>
1. <span data-ttu-id="aeb29-261">انتقل إلى **Azure AD B2C – تدفقات المستخدم (السياسات) \> {سياسة التسجيل وتسجيل الدخول} \> موفرو الهوية**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-261">Go to **Azure AD B2C – User flows (policies) \> {your sign-in sign-up policy} \> Identity providers**.</span></span>
1. <span data-ttu-id="aeb29-262">لإرفاق سياسة تدفق المستخدم للتسجيل/تسجيل الدخول، حدد كل موفر هوية قمت بإعداده لحسابك.</span><span class="sxs-lookup"><span data-stu-id="aeb29-262">To attach the sign in/sign up user flow policy, select each identity provider you have set up for your account.</span></span> <span data-ttu-id="aeb29-263">لاختبار هؤلاء، حدد **تشغيل تدفق المستخدم** لكل موفر هوية.</span><span class="sxs-lookup"><span data-stu-id="aeb29-263">To test these, select **Run user flow** for each identity provider.</span></span> <span data-ttu-id="aeb29-264">ستعرض علامة تبويب جديده صفحة تسجيل الدخول التي تعرض مربع تحديد موفر الهوية الجديد.</span><span class="sxs-lookup"><span data-stu-id="aeb29-264">A new tab will display the sign-in page displaying the new identity provider selection box.</span></span>

<span data-ttu-id="aeb29-265">تظهر الصورة التالية أمثلة عن شاشات **إضافة موفر هوية** و**إعداد موفر الهوية الاجتماعية** في Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="aeb29-265">The following image shows examples of the **Add identity provider** and **Set up the social identity provider** screens in Azure AD B2C.</span></span>

![إضافة موفر هوية اجتماعية إلى تطبيقك](./media/B2CImage_14.png)

<span data-ttu-id="aeb29-267">تعرض الصورة التالية مثالاً عن كيفية تحديد موفري الهوية في صفحة **موفرو هوية** Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="aeb29-267">The following image shows an example of how to select identity providers on the Azure AD B2C **Identity Providers** page.</span></span>

![حدد كل موفر هوية اجتماعية لتمكينه لسياستك](./media/B2CImage_16.png)

<span data-ttu-id="aeb29-269">تعرض الصورة التالية مثالاً عن شاشة تسجيل دخول افتراضية مع عرض زر تسجيل الدخول إلى موفر هوية اجتماعية.</span><span class="sxs-lookup"><span data-stu-id="aeb29-269">The following image shows an example of a default sign-in screen with a social identity provider sign-in button displayed.</span></span>

![مثال عن شاشة تسجيل دخول افتراضية مع عرض زر تسجيل الدخول إلى موفر هوية اجتماعية](./media/B2CImage_17.png)

## <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a><span data-ttu-id="aeb29-271">تحديث Commerce headquarters بواسطة معلومات Azure AD B2C جديدة</span><span class="sxs-lookup"><span data-stu-id="aeb29-271">Update Commerce headquarters with the new Azure AD B2C information</span></span>

<span data-ttu-id="aeb29-272">بعد إكمال خطوات تزويد Azure AD B2C أعلاه، يجب تسجيل تطبيق Azure AD B2C في بيئتك في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="aeb29-272">Once the Azure AD B2C provisioning steps above are completed, the Azure AD B2C application must be registered in your Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="aeb29-273">لتحديث المقر الرئيسي بمعلومات Azure AD B2C الجديدة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="aeb29-273">To update headquarters with the new Azure AD B2C information, follow these steps.</span></span>

1. <span data-ttu-id="aeb29-274">في Commerce، انتقل إلى **معلمات Commerce المشتركة**، وحدد **موفرو الهوية** في القائمة اليسرى</span><span class="sxs-lookup"><span data-stu-id="aeb29-274">In Commerce, go to **Commerce Shared Parameters** and select **Identity Providers** in the left menu.</span></span>
1. <span data-ttu-id="aeb29-275">ضمن **موفرو الهوية**، قم بما يلي:</span><span class="sxs-lookup"><span data-stu-id="aeb29-275">Under **Identity Providers**, do the following:</span></span>
    1. <span data-ttu-id="aeb29-276">في **المصدر**، أدخل عنوان URL لمصدر موفر الهوية.</span><span class="sxs-lookup"><span data-stu-id="aeb29-276">In the **Issuer** box, enter the identity provider issuer URL.</span></span> <span data-ttu-id="aeb29-277">للعثور على عنوان URL الخاص بالمصدر‏‎، راجع  [الحصول على عنوان المصدر](#obtain-issuer-url) أدناه.</span><span class="sxs-lookup"><span data-stu-id="aeb29-277">To find your issuer URL, see [Obtain issuer URL](#obtain-issuer-url) below.</span></span>
    1. <span data-ttu-id="aeb29-278">في مربع **الاسم**، أدخل اسمًا لسجل المصدر.</span><span class="sxs-lookup"><span data-stu-id="aeb29-278">In the **Name** box, enter a name for your issuer record.</span></span>
    1. <span data-ttu-id="aeb29-279">في مربع **النوع**، أدخل **Azure AD B2C (id_token)**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-279">In the **Type** box, enter **Azure AD B2C (id_token)**.</span></span>
1. <span data-ttu-id="aeb29-280">ضمن **الأطراف المعتمِدة**، مع تحديد عنصر موفر هوية B2C أعلاه، قم بما يلي:</span><span class="sxs-lookup"><span data-stu-id="aeb29-280">Under **Relying Parties**, with the above B2C identity provider item selected, do the following:</span></span>
    1. <span data-ttu-id="aeb29-281">في المربع‏‎ **معرف العميل**، أدخل معرف تطبيق B2C.</span><span class="sxs-lookup"><span data-stu-id="aeb29-281">In the **ClientID** box, enter your B2C application ID.</span></span> <span data-ttu-id="aeb29-282">يمكنك العثور على هذا المعرف في مربع **معرف التطبيق** في صفحة خصائص تطبيق B2C.</span><span class="sxs-lookup"><span data-stu-id="aeb29-282">You can find this in the **Application ID** box of your B2C application's properties page.</span></span>
    1. <span data-ttu-id="aeb29-283">في مربع **النوع**، أدخل **عام**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-283">In the **Type** box, enter **Public**.</span></span>
    1. <span data-ttu-id="aeb29-284">في مربع **نوع المستخدم**، أدخل **عميل**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-284">In the **User Type** box, enter **Customer**.</span></span>
1. <span data-ttu-id="aeb29-285">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-285">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="aeb29-286">في مربع البحث في Commerce، ابحث عن **التسلسلات الرقمية‬** (إدارة المؤسسة > التسلسلات الرقمية‬).</span><span class="sxs-lookup"><span data-stu-id="aeb29-286">In the Commerce search box, search for **Number sequences** (Organization administration > Number sequences).</span></span>
1. <span data-ttu-id="aeb29-287">ضمن جزء الإجراءات، حدد **تحرير** ضمن **المحافظة**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-287">Under the action pane, select **Edit** under **Maintain**.</span></span>
1. <span data-ttu-id="aeb29-288">على علامة التبويب السريعة **عام**، حدد **لا‏‎** للخيار **يدوي**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-288">On the **General** fast tab, select **No** for **Manual**.</span></span>
1. <span data-ttu-id="aeb29-289">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-289">On the action pane, select **Save**.</span></span> 
1. <span data-ttu-id="aeb29-290">في مربع البحث في Commerce، ابحث عن **جدول التوزيع**</span><span class="sxs-lookup"><span data-stu-id="aeb29-290">In the Commerce search box, search for **Distribution schedule**</span></span>
1. <span data-ttu-id="aeb29-291">في قائمة التنقل اليسرة من صفحة **جداول التوزيع**، حدد الوظيفة **1110 تكوين عمومي**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-291">In the left navigation menu of the **Distribution schedules** page, select job **1110 Global configuration**.</span></span>
1. <span data-ttu-id="aeb29-292">في جزء الإجراءات، حدد **تشغيل الآن**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-292">On the action pane, select **Run Now**.</span></span>

### <a name="obtain-issuer-url"></a><span data-ttu-id="aeb29-293">الحصول على عنوان URL للمصدر</span><span class="sxs-lookup"><span data-stu-id="aeb29-293">Obtain issuer URL</span></span>

<span data-ttu-id="aeb29-294">للحصول على عنوان URL لمصدر موفر الهوية، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="aeb29-294">To obtain your identity provider issuer URL, follow these steps.</span></span>

1. <span data-ttu-id="aeb29-295">قم بإنشاء عنوان URL لعنوان بيانات التعريف بالتنسيق التالي باستخدام سياسة ومستأجر B2C: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``</span><span class="sxs-lookup"><span data-stu-id="aeb29-295">Create a metadata address URL in the following format using your B2C tenant and policy: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``</span></span>
    - <span data-ttu-id="aeb29-296">مثال: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.</span><span class="sxs-lookup"><span data-stu-id="aeb29-296">Example: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.</span></span>
1. <span data-ttu-id="aeb29-297">أدخل عنوان URL لعنوان بيانات التعريف في شريط العناوين في المستعرض.</span><span class="sxs-lookup"><span data-stu-id="aeb29-297">Enter the metadata address URL into a browser address bar.</span></span>
1. <span data-ttu-id="aeb29-298">في بيانات التعريف، انسخ عنوان URL لمصدر موفر الهوية (قيمة **"المصدر"**).</span><span class="sxs-lookup"><span data-stu-id="aeb29-298">In the metadata, copy the identity provider issuer URL (the value for **"issuer"**).</span></span>
    - <span data-ttu-id="aeb29-299">مثال: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.</span><span class="sxs-lookup"><span data-stu-id="aeb29-299">Example: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.</span></span>

## <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a><span data-ttu-id="aeb29-300">تكوين مستأجر B2C في منشئ موقع Commerce</span><span class="sxs-lookup"><span data-stu-id="aeb29-300">Configure your B2C tenant in Commerce site builder</span></span>

<span data-ttu-id="aeb29-301">وبمجرد اكتمال إعداد مستأجر Azure AD B2C، يجب تكوين مستأجر B2C في منشئ موقع Commerce.</span><span class="sxs-lookup"><span data-stu-id="aeb29-301">Once setup of your Azure AD B2C tenant is completed, you must configure the B2C tenant in Commerce site builder.</span></span> <span data-ttu-id="aeb29-302">تتضمن خطوات التكوين تجميع معلومات تطبيق B2C من مدخل Azure، وإدخال معلومات تطبيق B2C في منشئ الموقع، ثم ربط تطبيق B2C بموقعك وقناتك.</span><span class="sxs-lookup"><span data-stu-id="aeb29-302">Configuration steps include collecting B2C application information from the Azure portal, entering that B2C application information into site builder, and then associating the B2C application with your site and channel.</span></span>

### <a name="collect-the-required-application-information"></a><span data-ttu-id="aeb29-303">تجميع معلومات التطبيق المطلوبة</span><span class="sxs-lookup"><span data-stu-id="aeb29-303">Collect the required application information</span></span>

<span data-ttu-id="aeb29-304">لتجميع معلومات التطبيق المطلوبة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="aeb29-304">To collect the required application information, follow these steps.</span></span>

1. <span data-ttu-id="aeb29-305">في مدخل Azure، انتقل إلى **الصفحة الرئيسية \> Azure AD B2C - تطبيقات**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-305">In the Azure portal, go to **Home \> Azure AD B2C - Applications**.</span></span>
1. <span data-ttu-id="aeb29-306">حدد تطبيقك، ثم حدد **خصائص** في جزء التنقل الأيسر للحصول على تفاصيل التطبيق.</span><span class="sxs-lookup"><span data-stu-id="aeb29-306">Select your application, and then in the left navigation pane select **Properties** to obtain the application details.</span></span>
1. <span data-ttu-id="aeb29-307">من المربع **معرف التطبيق**، قم بتجميع معرف التطبيق الخاص بتطبيق B2C الذي تم إنشاؤه في مستأجر B2C.</span><span class="sxs-lookup"><span data-stu-id="aeb29-307">From the **Application ID** box, collect the application ID of the B2C application created in your B2C tenant.</span></span> <span data-ttu-id="aeb29-308">سيتم إدخاله في وقت لاحق على أنه **GUID‎ العميل** في منشئ الموقع.</span><span class="sxs-lookup"><span data-stu-id="aeb29-308">This will later be entered as the **Client GUID** in site builder.</span></span>
1. <span data-ttu-id="aeb29-309">تحت **عنوان URL الخاص بالرج**، قم تجميع عنوان URL الخاص بالرد.</span><span class="sxs-lookup"><span data-stu-id="aeb29-309">Under **Reply URL**, collect the reply URL.</span></span>
1. <span data-ttu-id="aeb29-310">انتقل إلى **الصفحة الرئيسية \> Azure AD B2C – تدفقات المستخدم (السياسات)**، ثم اجمع أسماء كل تدفق سياسة مستخدم.</span><span class="sxs-lookup"><span data-stu-id="aeb29-310">Go to **Home \> Azure AD B2C – User flows (policies)**, and then collect the names of each user flow policy.</span></span>

<span data-ttu-id="aeb29-311">تعرض الصورة التالية مثالاً عن صفحة **Azure AD B2C - التطبيقات**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-311">The following image shows an example of the **Azure AD B2C - Applications** page.</span></span>

![الانتقال إلى تطبيق B2C داخل المستأجر](./media/B2CImage_19.png)

<span data-ttu-id="aeb29-313">تعرض الصورة التالية مثالاً عن صفحة **خصائص** التطبيق في Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="aeb29-313">The following image shows an example of an application **Properties** page in Azure AD B2C.</span></span> 

![نسخ معرف التطبيق من خصائص تطبيق B2C](./media/B2CImage_21.png)

<span data-ttu-id="aeb29-315">تعرض الصورة التالية مثالاً عن سياسات تدفق المستخدم في صفحة **Azure AD B2C – تدفقات المستخدم (السياسات)**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-315">The following image shows an example of user flow policies on the **Azure AD B2C – User flows (policies)** page.</span></span>

![جمع أسماء كل تدفق سياسة B2C](./media/B2CImage_22.png)

### <a name="enter-your-aad-b2c-tenant-application-information-into-commerce"></a><span data-ttu-id="aeb29-317">إدخال معلومات تطبيق مستأجر AAD B2C في Commerce</span><span class="sxs-lookup"><span data-stu-id="aeb29-317">Enter your AAD B2C tenant application information into Commerce</span></span>

<span data-ttu-id="aeb29-318">يجب إدخال التفاصيل الخاصة بمستأجر Azure AD B2C في منشئ موقع Commerce قبل ربط مستأجر B2C بموقعك (مواقعك).</span><span class="sxs-lookup"><span data-stu-id="aeb29-318">You must enter details of the Azure AD B2C tenant into Commerce site builder before associating the B2C tenant with your site(s).</span></span>

<span data-ttu-id="aeb29-319">لإضافة معلومات تطبيق مستأجر AAD B2C إلى Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="aeb29-319">To add your AAD B2C tenant application information to Commerce, follow these steps.</span></span>

1. <span data-ttu-id="aeb29-320">سجل دخولك كمسؤول إلى منشئ موقع Commerce لبيئتك.</span><span class="sxs-lookup"><span data-stu-id="aeb29-320">Sign in as an administrator to Commerce site builder for your environment.</span></span>
1. <span data-ttu-id="aeb29-321">في جزء التنقل الأيسر، حدد **إعدادات المستأجر** لتوسيعه.</span><span class="sxs-lookup"><span data-stu-id="aeb29-321">In the left navigation pane, select **Tenant Settings**  to expand it.</span></span>
1. <span data-ttu-id="aeb29-322">ضمن **إعدادات المستأجر**، حدد **إعدادات B2C**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-322">Under **Tenant Settings**, select **B2C Settings**.</span></span> 
1. <span data-ttu-id="aeb29-323">في النافذة الرئيسية، إلى جانب **تطبيقات B2C**، حدد **إدارة**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-323">In the main window next **B2C Applications**, select **Manage**.</span></span> <span data-ttu-id="aeb29-324">(إذا ظهر المستأجر في قائمة تطبيقات B2C، فهذا يعني أنه أضيف بواسطة المسؤول.</span><span class="sxs-lookup"><span data-stu-id="aeb29-324">(If your tenant appears in the B2C Applications list, then it was already added by an administrator.</span></span> <span data-ttu-id="aeb29-325">تحقق من تطابق البنود الموجودة في الخطوة 6 أدناه مع تطبيق B2C.)</span><span class="sxs-lookup"><span data-stu-id="aeb29-325">Verify that the items in step 6 below match your B2C Application.)</span></span>
1. <span data-ttu-id="aeb29-326">حدد **إضافة تطبيق B2C**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-326">Select **Add B2C Application**.</span></span>
1. <span data-ttu-id="aeb29-327">أدخل البنود المطلوبة التالية في النموذج المعروض، باستخدام قيم من مستأجر B2C وتطبيقك.</span><span class="sxs-lookup"><span data-stu-id="aeb29-327">Enter the following required items in the form displayed, using values from your B2C tenant and application.</span></span> <span data-ttu-id="aeb29-328">يمكن ترك الحقول غير المطلوبة (تلك التي لا توجد علامة نجمية إلى جانبها) فارغة.</span><span class="sxs-lookup"><span data-stu-id="aeb29-328">Fields that are not required (those without an asterisk) may be left blank.</span></span>

    - <span data-ttu-id="aeb29-329">**اسم التطبيق**: اسم تطبيق B2C، على سبيل المثال "Fabrikam B2C".</span><span class="sxs-lookup"><span data-stu-id="aeb29-329">**Application Name**: The name for your B2C Application, for example "Fabrikam B2C".</span></span>
    - <span data-ttu-id="aeb29-330">**اسم المستأجر**: اسم مستأجر B2C، على سبيل المثال، "Fabrikam".</span><span class="sxs-lookup"><span data-stu-id="aeb29-330">**Tenant Name**: The name of your B2C Tenant, for example "Fabrikam".</span></span>
    - <span data-ttu-id="aeb29-331">**معرف سياسة نسيان كلمة المرور**: معرف سياسة تدفق المستخدم لنسيان كلمة المرور، على سبيل المثال "B2C_1_PasswordReset".</span><span class="sxs-lookup"><span data-stu-id="aeb29-331">**Forget Password Policy ID**: The forget password user flow policy ID, for example "B2C_1_PasswordReset".</span></span>
    - <span data-ttu-id="aeb29-332">**معرف سياسة التسجيل وتسجيل الدخول**: معرف سياسة تدفق المستخدم للتسجيل وتسجيل الدخول، على سبيل المثال "B2C_1_signup_signin".</span><span class="sxs-lookup"><span data-stu-id="aeb29-332">**Signup Signin Policy ID**: The sign up and sign in user flow policy ID, for example "B2C_1_signup_signin".</span></span>
    - <span data-ttu-id="aeb29-333">**GUID‏‎ العميل**: معرف تطبيق B2C، على سبيل المثال "22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6".</span><span class="sxs-lookup"><span data-stu-id="aeb29-333">**Client GUID**: The B2C application ID, for example "22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6".</span></span>
    - <span data-ttu-id="aeb29-334">**معرف سياسة تحرير ملف التعريف**: معرف سياسة تدفق المستخدم لتحرير ملف التعريف، على سبيل المثال، "B2C_1A_ProfileEdit".</span><span class="sxs-lookup"><span data-stu-id="aeb29-334">**Edit Profile Policy ID**: The profile editing user flow policy ID, for example "B2C_1A_ProfileEdit".</span></span>

1. <span data-ttu-id="aeb29-335">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-335">Select **OK**.</span></span> <span data-ttu-id="aeb29-336">من المفترض أن يظهر الآن اسم تطبيق B2C في القائمة.</span><span class="sxs-lookup"><span data-stu-id="aeb29-336">You should now see the name of your B2C application appear in the list.</span></span>

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a><span data-ttu-id="aeb29-337">ربط تطبيق B2C بموقعك وقناتك</span><span class="sxs-lookup"><span data-stu-id="aeb29-337">Associate the B2C application to your site and channel</span></span>

> [!WARNING]
> <span data-ttu-id="aeb29-338">إذا كان موقعك مرتبطًا بتطبيق B2C، فسيؤدي التغيير إلى تطبيق B2C مختلف إلى إزالة المراجع الحالية التي تم تأسيسها للمستخدمين الذين قاموا بالتسجيل في هذه البيئة.</span><span class="sxs-lookup"><span data-stu-id="aeb29-338">If your site is already associated with a B2C application, changing to a different B2C application will remove the current references established for users already signed up in this environment.</span></span> <span data-ttu-id="aeb29-339">إذا حصل التغيير، فإن أي بيانات اعتماد مرتبطة بتطبيق B2C المعين حاليًا لن تكون متوفرة للمستخدمين.</span><span class="sxs-lookup"><span data-stu-id="aeb29-339">If changed, any credentials associated with the currently-assigned B2C application will not be available to users.</span></span> 
> 
> <span data-ttu-id="aeb29-340">قم بتحديث تطبيق B2C فقط إذا كنت تعمل على اعداد تطبيق B2C الخاص بالقناة للمرة الأولى أو إذا كنت تريد من المستخدمين إعادة التسجيل باستخدام بيانات اعتماد جديدة لهذه القناة مع تطبيق B2C الجديد.</span><span class="sxs-lookup"><span data-stu-id="aeb29-340">Only update the B2C application if you are setting up the channel's B2C application for the first time or if you intend to have users re-sign up with new credentials to this channel with the new B2C application.</span></span> <span data-ttu-id="aeb29-341">يجب توخي الحذر عند ربط القنوات بتطبيقات B2C، واحرص على تسمية التطبيقات بطريقة واضحة.</span><span class="sxs-lookup"><span data-stu-id="aeb29-341">Take caution when associating channels to B2C applications, and name applications clearly.</span></span> <span data-ttu-id="aeb29-342">إذا لم تكن قناة مرتبطة بتطبيق B2C في الخطوات أدناه، فإن المستخدمين الذين يسجلون دخولهم إلى هذه القناة لموقعك سيدخلون إلى تطبيق B2C الذي يظهر على أنه **افتراضي** في قائمة **إعدادات المستأجر \> إعدادات B2C** لتطبيقات B2C.</span><span class="sxs-lookup"><span data-stu-id="aeb29-342">If a channel is not associated to a B2C application in the steps below, users signing into that channel for your site will be entered into the B2C application showing as **default** in the **Tenant Settings \> B2C Settings** list of B2C applications.</span></span>

<span data-ttu-id="aeb29-343">لربط تطبيق B2C بموقعك وقناتك، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="aeb29-343">To associate the B2C application to your site and channel, follow these steps.</span></span>

1. <span data-ttu-id="aeb29-344">انتقل إلى موقعك في منشئ موقع Commerce.</span><span class="sxs-lookup"><span data-stu-id="aeb29-344">Navigate to your site in Commerce site builder.</span></span>
1. <span data-ttu-id="aeb29-345">في جزء التنقل الأيسر، حدد **إعدادات الموقع** لتوسيعه.</span><span class="sxs-lookup"><span data-stu-id="aeb29-345">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="aeb29-346">ضمن **إعدادات الموقع**، حدد **القنوات**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-346">Below **Site Settings**, select **Channels**.</span></span>
1. <span data-ttu-id="aeb29-347">في النافذة الرئيسية، ضمن **القنوات‏‎**، حدد قناتك.</span><span class="sxs-lookup"><span data-stu-id="aeb29-347">In the main window under **Channels**, select your channel.</span></span>
1. <span data-ttu-id="aeb29-348">في جزء خصائص القناة إلى اليسار، حدد اسم تطبيق B2C من القائمة المنسدلة **تحديد تطبيق B2C**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-348">In the channel properties pane on the right, select your B2C application name from the **Select B2C Application** drop down menu.</span></span>
1. <span data-ttu-id="aeb29-349">حدد **إغلاق**، ثم حدد **حفظ ونشر**.</span><span class="sxs-lookup"><span data-stu-id="aeb29-349">Select **Close**, and then select **Save and Publish**.</span></span>

## <a name="additional-b2c-information"></a><span data-ttu-id="aeb29-350">معلومات B2C إضافية</span><span class="sxs-lookup"><span data-stu-id="aeb29-350">Additional B2C information</span></span>

### <a name="customer-migration"></a><span data-ttu-id="aeb29-351">ترحيل العملاء</span><span class="sxs-lookup"><span data-stu-id="aeb29-351">Customer migration</span></span>

<span data-ttu-id="aeb29-352">إذا كنت ترغب في ترحيل سجلات العملاء من نظام موفر الهوية السابق، فيرجى العمل مع فريق Dynamics 365 Commerce لمراجعة احتياجات ترحيل العملاء.</span><span class="sxs-lookup"><span data-stu-id="aeb29-352">If you are considering migrating customer records from a previous identity provider platform, please work with the Dynamics 365 Commerce team to review your customer migration needs.</span></span>

<span data-ttu-id="aeb29-353">للحصول على وثائق Azure AD B2C إضافة حول ترحيل العملاء، راجع [ترحيل العملاء إلى Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).</span><span class="sxs-lookup"><span data-stu-id="aeb29-353">For additional Azure AD B2C documentation on customer migration, see [Migrate users to Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).</span></span>

### <a name="custom-policies"></a><span data-ttu-id="aeb29-354">سياسات مخصصة</span><span class="sxs-lookup"><span data-stu-id="aeb29-354">Custom policies</span></span>

<span data-ttu-id="aeb29-355">للحصول على معلومات إضافية حول تخصيص تفاعلات وتدفقات سياسة Azure AD B2C بما يتجاوز ما تقدمه سياسات B2C القياسية، راجع [السياسات المخصصة في Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom).</span><span class="sxs-lookup"><span data-stu-id="aeb29-355">For additional information regarding customizing Azure AD B2C interactions and policy flows beyond what is offered by B2C standard policies, see [Custom policies in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom).</span></span> 

### <a name="secondary-admin"></a><span data-ttu-id="aeb29-356">المسؤول الثانوي</span><span class="sxs-lookup"><span data-stu-id="aeb29-356">Secondary admin</span></span>

<span data-ttu-id="aeb29-357">يمكن إضافة حساب مسؤول ثانوي اختياري في قسم **المستخدمون** في مستأجر B2C.</span><span class="sxs-lookup"><span data-stu-id="aeb29-357">An optional, secondary administrator account can be added in the **Users** section of your B2C tenant.</span></span> <span data-ttu-id="aeb29-358">قد يكون هذا الحساب مباشرًا أو عامًا.</span><span class="sxs-lookup"><span data-stu-id="aeb29-358">This can be a direct account or a general account.</span></span> <span data-ttu-id="aeb29-359">إذا أردت مشاركة حساب عبر موارد الفريق، يمكن أيضًا إنشاء حساب عام.</span><span class="sxs-lookup"><span data-stu-id="aeb29-359">If you need to share an account across team resources, a common account can also be created.</span></span> <span data-ttu-id="aeb29-360">بسبب حساسية البيانات المخزنة في Azure AD B2C، يجب مراقبة حساب عام عن كثب وفق ممارسات الأمان الخاصة بشركتك.</span><span class="sxs-lookup"><span data-stu-id="aeb29-360">Due to the sensitivity of the data stored in Azure AD B2C, a common account should be monitored closely per your company's security practices.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aeb29-361">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="aeb29-361">Additional resources</span></span>

[<span data-ttu-id="aeb29-362">تكوين اسم مجالك</span><span class="sxs-lookup"><span data-stu-id="aeb29-362">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="aeb29-363">نشر موقع تجارة إلكترونية جديد</span><span class="sxs-lookup"><span data-stu-id="aeb29-363">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="aeb29-364">إنشاء موقع تجارة إلكترونية</span><span class="sxs-lookup"><span data-stu-id="aeb29-364">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="aeb29-365">إقران موقع عبر الإنترنت بقناة</span><span class="sxs-lookup"><span data-stu-id="aeb29-365">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="aeb29-366">إدارة ملفات robots.txt</span><span class="sxs-lookup"><span data-stu-id="aeb29-366">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="aeb29-367">تحميل عناوين URL لإعادة التوجيه‬ بشكل مجمع</span><span class="sxs-lookup"><span data-stu-id="aeb29-367">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="aeb29-368">إعداد صفحات مخصصة لعمليات تسجيل دخول المستخدمين</span><span class="sxs-lookup"><span data-stu-id="aeb29-368">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="aeb29-369">تكوين مستأجرين متعددين لمتاجرة عمل-مستهلك في بيئة Commerce</span><span class="sxs-lookup"><span data-stu-id="aeb29-369">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="aeb29-370">إضافة الدعم إلى شبكة تسليم المحتوى (CDN)</span><span class="sxs-lookup"><span data-stu-id="aeb29-370">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="aeb29-371">تمكين اكتشاف المتجر استنادًا إلى الموقع</span><span class="sxs-lookup"><span data-stu-id="aeb29-371">Enable location-based store detection</span></span>](enable-store-detection.md)