---
title: إعداد مستأجر B2C في Commerce
description: يصف هذا الموضوع كيفية إعداد مستأجري متاجرة بين عمل ومستهلك (B2C) في Azure Active Directory (Azure AD) لمصادقة موقع المستخدم في Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4ee667bb49e70e0c881a2db1248b3f0c7fc017ce
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478130"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a><span data-ttu-id="92bd2-103">إعداد مستأجر B2C في Commerce</span><span class="sxs-lookup"><span data-stu-id="92bd2-103">Set up a B2C tenant in Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="92bd2-104">يصف هذا الموضوع كيفية إعداد مستأجري متاجرة بين عمل ومستهلك (B2C) في Azure Active Directory (Azure AD) لمصادقة موقع المستخدم في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="92bd2-104">This topic describes how to set up your Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants for user site authentication in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="92bd2-105">يقوم Dynamics 365 Commerce باستخدام Azure AD B2C لدعم بيانات اعتماد المستخدم وتدفقات المصادقة.</span><span class="sxs-lookup"><span data-stu-id="92bd2-105">Dynamics 365 Commerce uses Azure AD B2C to support user credential and authentication flows.</span></span> <span data-ttu-id="92bd2-106">بإمكان المستخدم التسجيل وتسجيل الدخول وإعادة تعيين كلمة المرور من خلال هذه التدفقات.</span><span class="sxs-lookup"><span data-stu-id="92bd2-106">A user can sign up, sign in, and reset their password through these flows.</span></span> <span data-ttu-id="92bd2-107">يقوم Azure AD B2C بتخزين معلومات المصادقة الحساسة، مثل اسم المستخدم وكلمه المرور.</span><span class="sxs-lookup"><span data-stu-id="92bd2-107">Azure AD B2C stores sensitive user authentication information, such as username and password.</span></span> <span data-ttu-id="92bd2-108">سيقوم سجل المستخدم في مستأجر B2C بتخزين سجل حساب محلي B2C أو سجل موفر هوية اجتماعية B2C.</span><span class="sxs-lookup"><span data-stu-id="92bd2-108">The user record in the B2C tenant will store either a B2C local account record or a B2C social identity provider record.</span></span> <span data-ttu-id="92bd2-109">سترتبط سجلات B2C هذه من جديد بسجل العميل في بيئة Commerce.</span><span class="sxs-lookup"><span data-stu-id="92bd2-109">These B2C records will link back to the customer record in the Commerce environment.</span></span>

## <a name="create-or-link-to-an-existing-aad-b2c-tenant-in-the-azure-portal"></a><span data-ttu-id="92bd2-110">إنشاء مستأجر AAD B2C موجود في مدخل Azure أو الارتباط به</span><span class="sxs-lookup"><span data-stu-id="92bd2-110">Create or link to an existing AAD B2C tenant in the Azure portal</span></span>

1. <span data-ttu-id="92bd2-111">سجل الدخول إلى [مدخل Azure ](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="92bd2-111">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="92bd2-112">من قائمة مدخل Azure، حدد **إنشاء مورد**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-112">From the Azure portal menu, select **Create a resource**.</span></span> <span data-ttu-id="92bd2-113">احرص على استخدام الاشتراك والدليل الذي سيتم توصيله ببيئة Commerce.</span><span class="sxs-lookup"><span data-stu-id="92bd2-113">Be sure to use the subscription and directory that will be connected with your Commerce environment.</span></span>

    ![إنشاء مورد في مدخل Azure](./media/B2CImage_1.png)

1. <span data-ttu-id="92bd2-115">انتقل إلى **الهوية \> Azure Active Directory B2C**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-115">Go to **Identity \> Azure Active Directory B2C**.</span></span>
1. <span data-ttu-id="92bd2-116">عند وصولك إلى صفحة **إنشاء مستأجر B2C جديد أو الارتباط بمستأجر موجود**، استخدم أحد الخيارات أدناه الأكثر ملاءمة لاحتياجات شركتك:</span><span class="sxs-lookup"><span data-stu-id="92bd2-116">Once on the **Create New B2C Tenant or Link to existing Tenant** page, use one of the options below that best suits your company's needs:</span></span>

    - <span data-ttu-id="92bd2-117">**إنشاء مستأجر Azure AD B2C جديد**: استخدم هذا الخيار لإنشاء مستأجر AAD B2C جديد.</span><span class="sxs-lookup"><span data-stu-id="92bd2-117">**Create a new Azure AD B2C Tenant**: Use this option to create a new AAD B2C tenant.</span></span>
        1. <span data-ttu-id="92bd2-118">حدد **إنشاء مستأجر Azure AD B2C جديد**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-118">Select **Create a new Azure AD B2C Tenant**.</span></span>
        1. <span data-ttu-id="92bd2-119">ضمن **اسم المؤسسة**، أدخل اسم المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="92bd2-119">Under **Organization name**, enter the organization name.</span></span>
        1. <span data-ttu-id="92bd2-120">ضمن **اسم المجال الأولي**، أدخل اسم المجال الأولي‏‎.</span><span class="sxs-lookup"><span data-stu-id="92bd2-120">Under **Initial domain name**, enter the initial domain name.</span></span>
        1. <span data-ttu-id="92bd2-121">في **البلد أو المنطقة**، حدد البلد أو المنطقة.</span><span class="sxs-lookup"><span data-stu-id="92bd2-121">For **Country or region**, select the country or region.</span></span>
        1. <span data-ttu-id="92bd2-122">حدد **إنشاء** لإنشاء المستأجر.</span><span class="sxs-lookup"><span data-stu-id="92bd2-122">Select **Create** to create the tenant.</span></span>

     ![إنشاء مستأجر Azure AD جديد](./media/B2CImage_2.png)

     - <span data-ttu-id="92bd2-124">**ربط مستأجر Azure AD B2C موجود باشتراكي في Azure**: استخدم هذا الخيار إذا كان لديك مستأجر Azure AD B2C تريد الارتباط به.</span><span class="sxs-lookup"><span data-stu-id="92bd2-124">**Link an existing Azure AD B2C Tenant to my Azure subscription**: Use this option if you already have an Azure AD B2C tenant you want to link to.</span></span>
        1. <span data-ttu-id="92bd2-125">حدد **ربط مستأجر Azure AD B2C موجود باشتراكي في Azure**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-125">Select **Link an existing Azure AD B2C Tenant to my Azure subscription**.</span></span>
        1. <span data-ttu-id="92bd2-126">في **مستأجر Azure AD B2C**، حدد مستأجر B2C المناسب.</span><span class="sxs-lookup"><span data-stu-id="92bd2-126">For **Azure AD B2C Tenant**, select the appropriate B2C tenant.</span></span> <span data-ttu-id="92bd2-127">إذا ظهرت الرسالة "لم يتم العثور على مستأجري B2C مؤهلين" في مربع التحديد، فهذا يعني عدم وجود مستأجر B2C مؤهل ويجب إنشاء واحد جديد.</span><span class="sxs-lookup"><span data-stu-id="92bd2-127">If the message "No eligible B2C Tenants found" appears in the selection box, you do not have an existing eligible B2C tenant and will need to create a new one.</span></span>
        1. <span data-ttu-id="92bd2-128">في **مجموعة الموارد**، حدد **إنشاء جديد**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-128">For **Resource group**, select **Create new**.</span></span> <span data-ttu-id="92bd2-129">أدخل **اسم** مجموعة الموارد التي ستحتوي على المستأجر، وحدد، **موقع مجموعة الموارد**، ثم حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-129">Enter a **Name** for the resource group that will contain the tenant, select the **Resource group location**, and then select **Create**.</span></span>

    ![ربط مستأجر Azure AD B2C موجود باشتراك Azure](./media/B2CImage_3.png)

1. <span data-ttu-id="92bd2-131">بعد إنشاء دليل Azure AD B2C الجديد (قد يستغرق هذا الأمر لحظات قليلة)، سيظهر ارتباط إلى الدليل الجديد على لوحة المعلومات.</span><span class="sxs-lookup"><span data-stu-id="92bd2-131">Once the new Azure AD B2C directory is created (this may take a few moments), a link to the new directory will appear on the dashboard.</span></span> <span data-ttu-id="92bd2-132">سيوجهك هذا الارتباط إلى صفحة "مرحباً بك في Azure Active Directory B2C".</span><span class="sxs-lookup"><span data-stu-id="92bd2-132">This link will direct you to the "Welcome to Azure Active Directory B2C" page.</span></span>

    ![ارتباط إلى دليل AAD جديد](./media/B2CImage_4.png)

> [!NOTE]
> <span data-ttu-id="92bd2-134">إذا كانت لديك اشتراكات متعددة داخل حساب Azure أو قمت بإعداد مستأجر B2C بدون إنشاء ارتباط إلى اشتراك نشط، سيقوم شعار **استكشاف الأخطاء وإصلاحها** بتوجيهك لربط المستأجر باشتراك.</span><span class="sxs-lookup"><span data-stu-id="92bd2-134">If you have multiple subscriptions within your Azure account or have set up the B2C tenant without linking to an active subscription, a **Troubleshoot** banner will direct you to link the tenant to a subscription.</span></span> <span data-ttu-id="92bd2-135">حدد رسالة استكشاف الأخطاء وإصلاحها واتبع الإرشادات لحل مشكلة الاشتراك.</span><span class="sxs-lookup"><span data-stu-id="92bd2-135">Select the troubleshooting message and follow the instructions to resolve the subscription issue.</span></span>

<span data-ttu-id="92bd2-136">تبين الصورة التالية مثالاً عن شعار **استكشاف الأخطاء وإصلاحها في Azure AD B2C**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-136">The following image shows an example of an Azure AD B2C **Troubleshoot** banner.</span></span>

![تحذير يشير إلى عدم وجود اشتراك نشط لدى الدليل](./media/B2CImage_5.png)

## <a name="create-the-b2c-application"></a><span data-ttu-id="92bd2-138">إنشاء تطبيق B2C</span><span class="sxs-lookup"><span data-stu-id="92bd2-138">Create the B2C application</span></span>

<span data-ttu-id="92bd2-139">بعد إنشاء مستأجر B2C، ستقوم بإنشاء تطبيق B2C داخل المستأجر للتفاعل مع إجراءات Commerce.</span><span class="sxs-lookup"><span data-stu-id="92bd2-139">Once the B2C tenant has been created, you will create a B2C application within the tenant to interact with the Commerce actions.</span></span>

<span data-ttu-id="92bd2-140">لإنشاء تطبيق B2C، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="92bd2-140">To create the B2C application, follow these steps.</span></span>

1. <span data-ttu-id="92bd2-141">في مدخل Azure، حدد **التطبيقات (قديمة)** ثم حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-141">In the Azure portal, select **Applications(Legacy)** and then select **Add**.</span></span>
1. <span data-ttu-id="92bd2-142">ضمن **الاسم**، أدخل اسم تطبيق AAD B2C المطلوب.</span><span class="sxs-lookup"><span data-stu-id="92bd2-142">Under **Name**, enter the name of the desired AAD B2C application.</span></span>
1. <span data-ttu-id="92bd2-143">ضمن **تطبيق الويب/واجهة API‏‎ للويب**، في **تضمين تطبيق الويب/واجهة API‏‎ للويب**، حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-143">Under **Web App/Web API**, for **Include web app / web API**, select **Yes**.</span></span>
1. <span data-ttu-id="92bd2-144">في **السماح بالتدفق الضمني**، حدد **نعم** (القيمة الافتراضية).</span><span class="sxs-lookup"><span data-stu-id="92bd2-144">For **Allow implicit flow**, select **Yes** (the default value).</span></span>
1. <span data-ttu-id="92bd2-145">ضمن **عنوان URL‏‎ الخاص بالرد**، أدخل عناوين URL‏‎ الخاصة بالرد المخصصة.</span><span class="sxs-lookup"><span data-stu-id="92bd2-145">Under **Reply URL**, enter your dedicated reply URLs.</span></span> <span data-ttu-id="92bd2-146">راجع [عناوين URL‏‎ الخاصة بالرد](#reply-urls) أدناه للحصول على معلومات حول عناوين URL‏‎ الخاصة بالرد وكيفية تنسيقها هنا.</span><span class="sxs-lookup"><span data-stu-id="92bd2-146">See [Reply URLs](#reply-urls) below for information on reply URLs and how to format them here.</span></span>
1. <span data-ttu-id="92bd2-147">في **تضمين العميل الأصلي**، حدد **لا** (القيمة الافتراضية).</span><span class="sxs-lookup"><span data-stu-id="92bd2-147">For **Include native client**, select **No** (the default value).</span></span>
1. <span data-ttu-id="92bd2-148">حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-148">Select **Create**.</span></span>

### <a name="reply-urls"></a><span data-ttu-id="92bd2-149">عناوين URL الخاصة بالرد</span><span class="sxs-lookup"><span data-stu-id="92bd2-149">Reply URLs</span></span>

<span data-ttu-id="92bd2-150">تعتبر عناوين URL الخاصة بالرد مهمة لأنها توفر قائمة بيضاء للمجالات المرتجعة عندما يقوم موقعك باستدعاء Azure AD B2C لمصادقة مستخدم.</span><span class="sxs-lookup"><span data-stu-id="92bd2-150">Reply URLs are important as they provide an allow list of the return domains when your site calls Azure AD B2C to authenticate a user.</span></span> <span data-ttu-id="92bd2-151">يسمح ذلك بإرجاع المستخدم الذي تمت مصادقته إلى المجال الذي يتم تسجيل الدخول منه (مجال موقعك).</span><span class="sxs-lookup"><span data-stu-id="92bd2-151">This permits the return of the authenticated user back to the domain from which they are signing into (your site domain).</span></span> 

<span data-ttu-id="92bd2-152">في المربع **عنوان URL الخاص بالرد** على شاشة **Azure AD B2c - تطبيقات \> تطبيق جديد**، تحتاج إلى إضافة خطوط منفصلة لكل من مجال الموقع و(بعد تزويد بيئتك) عنوان URL المنشأ في Commerce.</span><span class="sxs-lookup"><span data-stu-id="92bd2-152">In the **Reply URL** box on the **Azure AD B2c - Applications \> New application** screen, you need to add separate lines for both your site domain and (once your environment is provisioned) the Commerce-generated URL.</span></span> <span data-ttu-id="92bd2-153">يجب أن تستخدم عناوين URL هذه دائمًا تنسيق URL صالحًا ويجب أن تكون عناوين URL أساسية فقط (لا توجد أي خطوط مائلة أمامية أو مسارات).</span><span class="sxs-lookup"><span data-stu-id="92bd2-153">These URLs must always use a valid URL format and must be base URLs only (no trailing forward slashes or paths).</span></span> <span data-ttu-id="92bd2-154">يجب إلحاق السلسلة ``/_msdyn365/authresp`` بعناوين URL الأساسية، كما في الأمثلة التالية:</span><span class="sxs-lookup"><span data-stu-id="92bd2-154">The string ``/_msdyn365/authresp`` then needs to be appended to the base URLs, as in the following examples.</span></span>

- <span data-ttu-id="92bd2-155">``https://www.fabrikam.com/_msdyn365/authresp``(يجب أن يطابق المجال مجال التجارة الإلكترونية بالكامل.</span><span class="sxs-lookup"><span data-stu-id="92bd2-155">``https://www.fabrikam.com/_msdyn365/authresp`` (The domain should match the e-commerce domain completely.</span></span> <span data-ttu-id="92bd2-156">إذا كان لديك مجالات متعددة، فأنت بحاجة إلى إضافةعنوان URL هذا لكل مجال.)</span><span class="sxs-lookup"><span data-stu-id="92bd2-156">If you have multiple domains, you need to add this URL for each domain.)</span></span>
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="create-user-flow-policies"></a><span data-ttu-id="92bd2-157">إنشاء سياسات تدفق المستخدم</span><span class="sxs-lookup"><span data-stu-id="92bd2-157">Create user flow policies</span></span>

<span data-ttu-id="92bd2-158">سياسات تدفق المستخدم هي السياسات التي يستخدمها Azure AD B2C لتوفير تجارب مستخدم آمنة للتسجيل وتسجيل الدخول وتحرير ملف التعريف ونسيان كلمه المرور.</span><span class="sxs-lookup"><span data-stu-id="92bd2-158">User flows are the policies Azure AD B2C uses to provide secure sign in, sign up, edit profile, and forget password user experiences.</span></span> <span data-ttu-id="92bd2-159">يستخدم Dynamics 365 Commerce  هذه التدفقات لتنفيذ إجراءات السياسة للتفاعل مع مستأجر Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="92bd2-159">Dynamics 365 Commerce uses these flows to perform the policy actions to interact with the Azure AD B2C tenant.</span></span> <span data-ttu-id="92bd2-160">عندما يتفاعل المستخدم مع هذه السياسات، يعاد توجيههم إلى مستأجر Azure AD B2C لتنفيذ الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="92bd2-160">When a user interacts with these policies, they are redirected to the Azure AD B2C tenant to perform the actions.</span></span>

<span data-ttu-id="92bd2-161">يوفر Azure AD B2C ثلاثة أنواع من تدفقات المستخدم الأساسية:</span><span class="sxs-lookup"><span data-stu-id="92bd2-161">Azure AD B2C provides three basic user flow types:</span></span>
- <span data-ttu-id="92bd2-162">التسجيل وتسجيل الدخول</span><span class="sxs-lookup"><span data-stu-id="92bd2-162">Sign up and sign in</span></span>
- <span data-ttu-id="92bd2-163">تحرير ملف التعريف</span><span class="sxs-lookup"><span data-stu-id="92bd2-163">Profile editing</span></span>
- <span data-ttu-id="92bd2-164">إعادة تعيين كلمة المرور</span><span class="sxs-lookup"><span data-stu-id="92bd2-164">Password reset</span></span>

<span data-ttu-id="92bd2-165">يمكنك اختيار استخدام تدفقات المستخدم الافتراضية التي يوفرها Azure AD، والتي ستقوم بعرض صفحة يستضيفها AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="92bd2-165">You can choose to use the default user flows provided by Azure AD, which will display a page hosted by AAD B2C.</span></span> <span data-ttu-id="92bd2-166">أو يمكنك إنشاء صفحة HTML للتحكم في شكل وأسلوب تجارب تدفق المستخدم هذه.</span><span class="sxs-lookup"><span data-stu-id="92bd2-166">Alternately, you can create an HTML page to control the look and feel of these user flow experiences.</span></span> 

<span data-ttu-id="92bd2-167">لتخصيص صفحات سياسة المستخدم لـ Dynamics 365 Commerce، راجع [إعداد صفحات مخصصة لعمليات تسجيل دخول المستخدمين‬](custom-pages-user-logins.md).</span><span class="sxs-lookup"><span data-stu-id="92bd2-167">To customize the user policy pages for Dynamics 365 Commerce, see [Set up custom pages for user logins](custom-pages-user-logins.md).</span></span> <span data-ttu-id="92bd2-168">للحصول على معلومات إضافية، راجع [تخصيص واجهة تجارب المستخدم في Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).</span><span class="sxs-lookup"><span data-stu-id="92bd2-168">For additional information, see [Customize the interface of user experiences in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).</span></span>

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a><span data-ttu-id="92bd2-169">إنشاء عملية تسجيل وتسجيل دخول في سياسة تدفق المستخدم</span><span class="sxs-lookup"><span data-stu-id="92bd2-169">Create a sign up and sign in user flow policy</span></span>

<span data-ttu-id="92bd2-170">لإنشاء عملية تسجيل وتسجيل دخول في سياسة تدفق المستخدم، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="92bd2-170">To create a sign up and sign in user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="92bd2-171">في مدخل Azure، حدد **تدفقات المستخدم (السياسات)** في جزء التنقل الأيمن.</span><span class="sxs-lookup"><span data-stu-id="92bd2-171">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="92bd2-172">في صفحة **Azure AD B2C – تدفقات المستخدم (السياسات)‬‏‫**، حدد **تدفق مستخدم جديد‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-172">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="92bd2-173">في علامة التبويب **موصي به**، حدد **التسجيل وتسجيل الدخول**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-173">On the **Recommended** tab, select **Sign up and sign in**.</span></span>
1. <span data-ttu-id="92bd2-174">ضمن **الاسم**، أدخل اسمًا للسياسة.</span><span class="sxs-lookup"><span data-stu-id="92bd2-174">Under **Name**, enter a policy name.</span></span> <span data-ttu-id="92bd2-175">سيظهر هذا الاسم بعد ذلك مع بادئة يعينها المدخل (على سبيل المثال، "B2C_1_").</span><span class="sxs-lookup"><span data-stu-id="92bd2-175">This name will display afterwards with a prefix the portal assigns (for example, "B2C_1_").</span></span>
1. <span data-ttu-id="92bd2-176">ضمن **موفرو الهوية**، حدد خانة الاختيار المناسبة.</span><span class="sxs-lookup"><span data-stu-id="92bd2-176">Under **Identity providers**, select the appropriate check box.</span></span>
1. <span data-ttu-id="92bd2-177">ضمن **مصادقة متعددة العوامل**، حدد الاختيار المناسب لشركتك.</span><span class="sxs-lookup"><span data-stu-id="92bd2-177">Under **Multifactor Authentication**, select the appropriate choice for your company.</span></span> 
1. <span data-ttu-id="92bd2-178">ضمن **سمات ومطالبات المستخدم**، حدد الخيارات لجمع السمات أو إرجاع المطالبات حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="92bd2-178">Under **User attributes and claims**, select options to collect attributes or return claims as appropriate.</span></span> <span data-ttu-id="92bd2-179">يحتاج Commerce إلى الخيارات الافتراضية التالية:</span><span class="sxs-lookup"><span data-stu-id="92bd2-179">Commerce requires the following default options:</span></span>

    | <span data-ttu-id="92bd2-180">**جمع سمة**</span><span class="sxs-lookup"><span data-stu-id="92bd2-180">**Collect  attribute**</span></span> | <span data-ttu-id="92bd2-181">**إرجاع مطالبة**</span><span class="sxs-lookup"><span data-stu-id="92bd2-181">**Return  claim**</span></span> |
    | ---------------------- | ----------------- |
    | <span data-ttu-id="92bd2-182">عنوان البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="92bd2-182">Email Address</span></span>          | <span data-ttu-id="92bd2-183">عناوين البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="92bd2-183">Email Addresses</span></span>   |
    | <span data-ttu-id="92bd2-184">الاسم المحدد</span><span class="sxs-lookup"><span data-stu-id="92bd2-184">Given Name</span></span>             | <span data-ttu-id="92bd2-185">الاسم المحدد</span><span class="sxs-lookup"><span data-stu-id="92bd2-185">Given Name</span></span>        |
    |                        | <span data-ttu-id="92bd2-186">موفر الهوية‬</span><span class="sxs-lookup"><span data-stu-id="92bd2-186">Identity Provider</span></span> |
    | <span data-ttu-id="92bd2-187">اللقب</span><span class="sxs-lookup"><span data-stu-id="92bd2-187">Surname</span></span>                | <span data-ttu-id="92bd2-188">اللقب</span><span class="sxs-lookup"><span data-stu-id="92bd2-188">Surname</span></span>           |
    |                        | <span data-ttu-id="92bd2-189">معرف الكائن الخاص بالمستخدم</span><span class="sxs-lookup"><span data-stu-id="92bd2-189">User’s Object ID</span></span>  |

1. <span data-ttu-id="92bd2-190">حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-190">Select **Create**.</span></span>

<span data-ttu-id="92bd2-191">الصورة التالية هي مثال تدفق المستخدم للتسجيل وتسجيل الدخول إلى Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="92bd2-191">The following image is an example of the Azure AD B2C sign up and sign in user flow.</span></span>

![إعدادات سياسة التسجيل وتسجيل الدخول](./media/B2CImage_11.png)

<span data-ttu-id="92bd2-193">تظهر الصورة التالية الخيار **تشغيل تدفق المستخدم** في Azure AD B2C تدفق المستخدم للتسجيل وتسجيل الدخول إلى B2C.</span><span class="sxs-lookup"><span data-stu-id="92bd2-193">The following image shows the **Run user flow** option in the Azure AD B2C sign up and sign in user flow.</span></span>

![الخيار "تشغيل تدفق المستخدم‬‏‫" في تدفق السياسة](./media/B2CImage_23.png)
   
### <a name="create-a-profile-editing-user-flow-policy"></a><span data-ttu-id="92bd2-195">إنشاء سياسة تدفق المستخدم لتحرير ملف التعريف</span><span class="sxs-lookup"><span data-stu-id="92bd2-195">Create a profile editing user flow policy</span></span>

<span data-ttu-id="92bd2-196">لإنشاء سياسة تدفق المستخدم لتحرير ملف التعريف، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="92bd2-196">To create a profile editing user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="92bd2-197">في مدخل Azure، حدد **تدفقات المستخدم (السياسات)** في جزء التنقل الأيمن.</span><span class="sxs-lookup"><span data-stu-id="92bd2-197">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="92bd2-198">في صفحة **Azure AD B2C – تدفقات المستخدم (السياسات)‬‏‫**، حدد **تدفق مستخدم جديد‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-198">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="92bd2-199">على علامة التبويب **موصى به**، حدد **تحرير ملف التعريف**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-199">On the **Recommended** tab, select **Profile editing**.</span></span>
1. <span data-ttu-id="92bd2-200">ضمن **الاسم**، أدخل تدفق المستخدم لتحرير ملف التعريف.</span><span class="sxs-lookup"><span data-stu-id="92bd2-200">Under **Name**, enter the profile editing user flow.</span></span> <span data-ttu-id="92bd2-201">سيظهر هذا الاسم بعد ذلك مع بادئة يعينها المدخل (على سبيل المثال، "B2C_1_").</span><span class="sxs-lookup"><span data-stu-id="92bd2-201">This name will display afterwards with a prefix the portal assigns (for example, "B2C_1_").</span></span>
1. <span data-ttu-id="92bd2-202">ضمن **موفرو الهوية**، حدد **، تسجيل الدخول إلى الحساب المحلي**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-202">Under **Identity providers**, select **Local Account SignIn**.</span></span>
1. <span data-ttu-id="92bd2-203">ضمن **سمات المستخدم**، حدد خانات الاختيار التالية:</span><span class="sxs-lookup"><span data-stu-id="92bd2-203">Under **User attributes**, select the following check boxes:</span></span>
    - <span data-ttu-id="92bd2-204">**عناوين البريد الإلكتروني** (**إرجاع مطالبة** فقط)</span><span class="sxs-lookup"><span data-stu-id="92bd2-204">**Email Addresses** (**Return claim** only)</span></span>
    - <span data-ttu-id="92bd2-205">**الاسم المحدد** (**جمع السمة** و **إرجاع مطالبة‬‏‫**)</span><span class="sxs-lookup"><span data-stu-id="92bd2-205">**Given Name** (**Collect attribute** and **Return claim**)</span></span>
    - <span data-ttu-id="92bd2-206">**موفر‏‎ الهوية** (**إرجاع مطالبة‬‏‫** فقط)</span><span class="sxs-lookup"><span data-stu-id="92bd2-206">**Identity Provider** (**Return claim** only)</span></span>
    - <span data-ttu-id="92bd2-207">**اللقب‬‏‫** (**جمع السمة** و **إرجاع مطالبة‬‏‫**)</span><span class="sxs-lookup"><span data-stu-id="92bd2-207">**Surname** (**Collect attribute** and **Return claim**)</span></span>
    - <span data-ttu-id="92bd2-208">**معرف الكائن الخاص بالمستخدم‬** (**إرجاع مطالبة** فقط)</span><span class="sxs-lookup"><span data-stu-id="92bd2-208">**User's Object ID** (**Return claim** only)</span></span>
1. <span data-ttu-id="92bd2-209">حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-209">Select **Create**.</span></span>

<span data-ttu-id="92bd2-210">تعرض الصورة التالية مثالاً عن تدفق المستخدم لتحرير مرف تعريف Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="92bd2-210">The following image shows an example of the Azure AD B2C profile editing user flow.</span></span>

![إنشاء تدفق المستخدم لتحرير ملف التعريف](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a><span data-ttu-id="92bd2-212">إنشاء سياسة تدفق المستخدم لإعادة تعيين كلمة المرور</span><span class="sxs-lookup"><span data-stu-id="92bd2-212">Create a password reset user flow policy</span></span>

<span data-ttu-id="92bd2-213">لإنشاء سياسة تدفق المستخدم لإعادة تعيين كلمة المرور، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="92bd2-213">To create a password reset user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="92bd2-214">في مدخل Azure، حدد **تدفقات المستخدم (السياسات)** في جزء التنقل الأيمن.</span><span class="sxs-lookup"><span data-stu-id="92bd2-214">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="92bd2-215">في صفحة **Azure AD B2C – تدفقات المستخدم (السياسات)‬‏‫**، حدد **تدفق مستخدم جديد‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-215">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="92bd2-216">على علامة التبويب **موصى به**، حدد **إعادة تعيين كلمة المرور**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-216">On the **Recommended** tab, select **Password Reset**.</span></span>
1. <span data-ttu-id="92bd2-217">ضمن **الاسم**، أدخل اسمًا لتدفق المستخدم لإعادة تعيين كلمة المرور.</span><span class="sxs-lookup"><span data-stu-id="92bd2-217">Under **Name**, enter a name for the password reset user flow.</span></span>
1. <span data-ttu-id="92bd2-218">ضمن **موفرو الهوية**، حدد **إعادة تعيين كلمة المرور باستخدام عنوان البريد الكتروني**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-218">Under **Identity providers**, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="92bd2-219">حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-219">Select **Create**.</span></span>
1. <span data-ttu-id="92bd2-220">ضمن **مطالبات التطبيق**، حدد خانات الاختيار التالية:</span><span class="sxs-lookup"><span data-stu-id="92bd2-220">Under **Application claims**, select the following check boxes:</span></span>
    - <span data-ttu-id="92bd2-221">**عناوين البريد الإلكتروني**</span><span class="sxs-lookup"><span data-stu-id="92bd2-221">**Email addresses**</span></span>
    - <span data-ttu-id="92bd2-222">**الاسم المحدد**</span><span class="sxs-lookup"><span data-stu-id="92bd2-222">**Given Name**</span></span>
    - <span data-ttu-id="92bd2-223">**اللقب**</span><span class="sxs-lookup"><span data-stu-id="92bd2-223">**Surname**</span></span>
    - <span data-ttu-id="92bd2-224">**معرف الكائن الخاص بالمستخدم**</span><span class="sxs-lookup"><span data-stu-id="92bd2-224">**User's Object ID**</span></span>
1. <span data-ttu-id="92bd2-225">حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-225">Select **Create**.</span></span>

<span data-ttu-id="92bd2-226">توضح الصورة التالية المكان حيث يجب تعيين الخيار **إعادة تعيين كلمة المرور باستخدام عنوان بريد إلكتروني** في تدفق المستخدم لإعادة تعيين كلمة المرور في Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="92bd2-226">The following image shows where to set **Reset Password using mail address** in the Azure AD B2C password reset user flow.</span></span>

![تعيين "إعادة تعيين كلمة المرور باستخدام عنوان بريد إلكتروني" في سياسة إعادة تعيين كلمة المرور](./media/B2CImage_13.png)

## <a name="add-social-identity-providers-optional"></a><span data-ttu-id="92bd2-228">إضافة موفري الهوية الاجتماعية (اختياري)</span><span class="sxs-lookup"><span data-stu-id="92bd2-228">Add social identity providers (Optional)</span></span>

<span data-ttu-id="92bd2-229">يسمح موفرو الهوية الاجتماعية للمستخدمين باستخدام حساباتهم الاجتماعية للمصادقة.</span><span class="sxs-lookup"><span data-stu-id="92bd2-229">Social identity providers allow users to use their social accounts for authentication.</span></span> <span data-ttu-id="92bd2-230">تعتبر إضافة مصادقة موفر الهوية الاجتماعية اختيارية في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="92bd2-230">Adding social identity provider authentication is optional in Dynamics 365 Commerce.</span></span> 

<span data-ttu-id="92bd2-231">إذا لم تتم إضافة مصادقة موفر الهوية الاجتماعية، ستكون ملفات تعريف Azure AD B2C الافتراضية ملفات التعريف الأساسية لقاعدة المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="92bd2-231">If social identity provider authentication is not added, the default Azure AD B2C profiles will be the main profiles for your user base.</span></span> <span data-ttu-id="92bd2-232">سيقوم المستخدمون بتحديد اسم المستخدم (عنوان بريدهم الإلكتروني المفضل) وتعيين كلمة مرور.</span><span class="sxs-lookup"><span data-stu-id="92bd2-232">Users will select their own username (their preferred email address) and set a password.</span></span> <span data-ttu-id="92bd2-233">سيقوم Azure AD B2C بمصادقة المستخدمين بشكل مباشر.</span><span class="sxs-lookup"><span data-stu-id="92bd2-233">Azure AD B2C will authenticate users directly.</span></span> 

<span data-ttu-id="92bd2-234">إذا تمت إضافة مصادقة موفر الهوية الاجتماعية واختار أحد المستخدمين أحد موفري الهوية الاجتماعية المعروضين، فسيتم مع ذلك إنشاء كيان في مستأجر Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="92bd2-234">If social identity provider authentication is added and a user chooses one of the social identity providers offered, an entity is still created in the Azure AD B2C tenant.</span></span> <span data-ttu-id="92bd2-235">سيقوم Azure AD B2C عندئذٍ بمصادقة بيانات اعتماد المستخدم مع موفر الهوية الاجتماعية.</span><span class="sxs-lookup"><span data-stu-id="92bd2-235">Azure AD B2C will then authenticate the user's credentials with the social identity provider.</span></span>

> [!NOTE]
> <span data-ttu-id="92bd2-236">يؤدي تسجيل دخول الموفر إلى إنشاء سجل في مستأجر B2C، ولكن بتنسيق مختلف عن الحسابات المحلية لأنه سيقوم باستدعاء مرجع موفر الهوية الاجتماعية الخارجي للمصادقة.</span><span class="sxs-lookup"><span data-stu-id="92bd2-236">The identity provider sign in creates a record in the B2C tenant, but in a different format than local accounts since it will call the external social identity provider reference for authentication.</span></span> <span data-ttu-id="92bd2-237">يمكن للمستخدم استخدام عنوان البريد الإلكتروني نفسه عبر موفري الهويات الاجتماعية، مما يعني أن اسم المستخدم للبريد الإلكتروني الذي تم استخدامه للمصادقة قد لا يكون فريدًا للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="92bd2-237">The user can use the same email address across social identity providers, meaning that the email username used for authentication may not be unique to the tenant.</span></span> <span data-ttu-id="92bd2-238">سيفرض Azure AD B2C فقط وجود عنوان بريد إلكتروني فريد للمستخدمين على حسابات B2C المحلية.</span><span class="sxs-lookup"><span data-stu-id="92bd2-238">Azure AD B2C will only enforce that users have a unique email address on local B2C accounts.</span></span>

<span data-ttu-id="92bd2-239">قبل أن تتمكن من إضافة موفر هوية اجتماعية للمصادقة، يجب الانتقال إلى مدخل موفر الهوية وإعداد تطبيق موفر هوية كما هو موضح في وثائق Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="92bd2-239">Before you can add a social identity provider for authentication, you must go to the identity provider's portal and set up an identity provider application as instructed in the Azure AD B2C documentation.</span></span> <span data-ttu-id="92bd2-240">توجد أدناه قائمة بالارتباطات إلى الوثائق.</span><span class="sxs-lookup"><span data-stu-id="92bd2-240">A list of links to the documentation is provided below.</span></span>

- [<span data-ttu-id="92bd2-241">Amazon</span><span class="sxs-lookup"><span data-stu-id="92bd2-241">Amazon</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [<span data-ttu-id="92bd2-242">Azure AD (مستأجر واحد)</span><span class="sxs-lookup"><span data-stu-id="92bd2-242">Azure AD (Single Tenant)</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [<span data-ttu-id="92bd2-243">حساب Microsoft</span><span class="sxs-lookup"><span data-stu-id="92bd2-243">Microsoft Account</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [<span data-ttu-id="92bd2-244">Facebook</span><span class="sxs-lookup"><span data-stu-id="92bd2-244">Facebook</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [<span data-ttu-id="92bd2-245">GitHub</span><span class="sxs-lookup"><span data-stu-id="92bd2-245">GitHub</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [<span data-ttu-id="92bd2-246">Google</span><span class="sxs-lookup"><span data-stu-id="92bd2-246">Google</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [<span data-ttu-id="92bd2-247">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="92bd2-247">LinkedIn</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [<span data-ttu-id="92bd2-248">OpenID Connect</span><span class="sxs-lookup"><span data-stu-id="92bd2-248">OpenID Connect</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [<span data-ttu-id="92bd2-249">Twitter</span><span class="sxs-lookup"><span data-stu-id="92bd2-249">Twitter</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a><span data-ttu-id="92bd2-250">إضافة موفر هوية اجتماعية وإعداده</span><span class="sxs-lookup"><span data-stu-id="92bd2-250">Add and set up a social identity provider</span></span>

<span data-ttu-id="92bd2-251">لإضافة موفر هوية اجتماعية وإعداده، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="92bd2-251">To add and set up a social identity provider, follow these steps.</span></span>  

1. <span data-ttu-id="92bd2-252">في مدخل Azure، انتقل إلى **موفرو الهوية**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-252">In the Azure portal, navigate to **Identity Providers**.</span></span>
1. <span data-ttu-id="92bd2-253">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-253">Select **Add**.</span></span> <span data-ttu-id="92bd2-254">تظهر الشاشة **إضافة موفر هوية**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-254">The **Add identity provider** screen appears.</span></span>
1. <span data-ttu-id="92bd2-255">ضمن **الاسم**، أدخل الاسم المطلوب عرضه للمستخدمين على شاشة تسجيل الدخول.</span><span class="sxs-lookup"><span data-stu-id="92bd2-255">Under **Name**, enter the name to be displayed to users on your sign in screen.</span></span>
1. <span data-ttu-id="92bd2-256">ضمن **نوع موفر الهوية**، حدد موفر هوية من القائمة.</span><span class="sxs-lookup"><span data-stu-id="92bd2-256">Under **Identity provider type**, select an identity provider from the list.</span></span>
1. <span data-ttu-id="92bd2-257">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-257">Select **OK**.</span></span>
1. <span data-ttu-id="92bd2-258">حدد **إعداد موفر الهوية هذا** للوصول إلى شاشة **إعداد موفر الهوية الاجتماعية**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-258">Select **Set up this identity provider** to access the **Set up the social identity provider** screen.</span></span>
1. <span data-ttu-id="92bd2-259">ضمن **معرف العميل**، أدخل معرف العميل كما تم الحصول عليه من إعداد تطبيق موفر الهوية.</span><span class="sxs-lookup"><span data-stu-id="92bd2-259">Under **Client ID**, enter the client ID as obtained from the identity provider application setup.</span></span>
1. <span data-ttu-id="92bd2-260">ضمن **سر العميل**، أدخل سر العميل كما تم الحصول عليه من إعداد تطبيق موفر الهوية.</span><span class="sxs-lookup"><span data-stu-id="92bd2-260">Under **Client secret**, enter the client secret as obtained from the identity provider application setup.</span></span>
1. <span data-ttu-id="92bd2-261">إرفاق تدفق المستخدم لسياسات التسجيل:</span><span class="sxs-lookup"><span data-stu-id="92bd2-261">Attach user flow for sign in sign up policies:</span></span>
1. <span data-ttu-id="92bd2-262">انتقل إلى **Azure AD B2C – تدفقات المستخدم (السياسات) \> {سياسة التسجيل وتسجيل الدخول} \> موفرو الهوية**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-262">Go to **Azure AD B2C – User flows (policies) \> {your sign-in sign-up policy} \> Identity providers**.</span></span>
1. <span data-ttu-id="92bd2-263">لإرفاق سياسة تدفق المستخدم للتسجيل/تسجيل الدخول، حدد كل موفر هوية قمت بإعداده لحسابك.</span><span class="sxs-lookup"><span data-stu-id="92bd2-263">To attach the sign in/sign up user flow policy, select each identity provider you have set up for your account.</span></span> <span data-ttu-id="92bd2-264">لاختبار هؤلاء، حدد **تشغيل تدفق المستخدم** لكل موفر هوية.</span><span class="sxs-lookup"><span data-stu-id="92bd2-264">To test these, select **Run user flow** for each identity provider.</span></span> <span data-ttu-id="92bd2-265">ستعرض علامة تبويب جديدة صفحة تسجيل الدخول التي تعرض مربع تحديد موفر الهوية الجديد.</span><span class="sxs-lookup"><span data-stu-id="92bd2-265">A new tab will display the sign-in page displaying the new identity provider selection box.</span></span>

<span data-ttu-id="92bd2-266">تظهر الصورة التالية أمثلة عن شاشات **إضافة موفر هوية** و **إعداد موفر الهوية الاجتماعية** في Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="92bd2-266">The following image shows examples of the **Add identity provider** and **Set up the social identity provider** screens in Azure AD B2C.</span></span>

![إضافة موفر هوية اجتماعية إلى تطبيقك](./media/B2CImage_14.png)

<span data-ttu-id="92bd2-268">تعرض الصورة التالية مثالاً عن كيفية تحديد موفري الهوية في صفحة **موفرو هوية** Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="92bd2-268">The following image shows an example of how to select identity providers on the Azure AD B2C **Identity Providers** page.</span></span>

![حدد كل موفر هوية اجتماعية لتمكينه لسياستك](./media/B2CImage_16.png)

<span data-ttu-id="92bd2-270">تعرض الصورة التالية مثالاً عن شاشة تسجيل دخول افتراضية مع عرض زر تسجيل الدخول إلى موفر هوية اجتماعية.</span><span class="sxs-lookup"><span data-stu-id="92bd2-270">The following image shows an example of a default sign-in screen with a social identity provider sign-in button displayed.</span></span>

![مثال عن شاشة تسجيل دخول افتراضية مع عرض زر تسجيل الدخول إلى موفر هوية اجتماعية](./media/B2CImage_17.png)

## <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a><span data-ttu-id="92bd2-272">تحديث Commerce headquarters بواسطة معلومات Azure AD B2C جديدة</span><span class="sxs-lookup"><span data-stu-id="92bd2-272">Update Commerce headquarters with the new Azure AD B2C information</span></span>

<span data-ttu-id="92bd2-273">بعد إكمال خطوات تزويد Azure AD B2C أعلاه، يجب تسجيل تطبيق Azure AD B2C في بيئتك في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="92bd2-273">Once the Azure AD B2C provisioning steps above are completed, the Azure AD B2C application must be registered in your Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="92bd2-274">لتحديث المقر الرئيسي بمعلومات Azure AD B2C الجديدة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="92bd2-274">To update headquarters with the new Azure AD B2C information, follow these steps.</span></span>

1. <span data-ttu-id="92bd2-275">في Commerce، انتقل إلى **معلمات Commerce المشتركة**، وحدد **موفرو الهوية** في القائمة اليسرى</span><span class="sxs-lookup"><span data-stu-id="92bd2-275">In Commerce, go to **Commerce Shared Parameters** and select **Identity Providers** in the left menu.</span></span>
1. <span data-ttu-id="92bd2-276">ضمن **موفرو الهوية**، قم بما يلي:</span><span class="sxs-lookup"><span data-stu-id="92bd2-276">Under **Identity Providers**, do the following:</span></span>
    1. <span data-ttu-id="92bd2-277">في **المصدر**، أدخل عنوان URL لمصدر موفر الهوية.</span><span class="sxs-lookup"><span data-stu-id="92bd2-277">In the **Issuer** box, enter the identity provider issuer URL.</span></span> <span data-ttu-id="92bd2-278">للعثور على عنوان URL الخاص بالمصدر‏‎، راجع  [الحصول على عنوان المصدر](#obtain-issuer-url) أدناه.</span><span class="sxs-lookup"><span data-stu-id="92bd2-278">To find your issuer URL, see [Obtain issuer URL](#obtain-issuer-url) below.</span></span>
    1. <span data-ttu-id="92bd2-279">في مربع **الاسم**، أدخل اسمًا لسجل المصدر.</span><span class="sxs-lookup"><span data-stu-id="92bd2-279">In the **Name** box, enter a name for your issuer record.</span></span>
    1. <span data-ttu-id="92bd2-280">في مربع **النوع**، أدخل **Azure AD B2C (id_token)**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-280">In the **Type** box, enter **Azure AD B2C (id_token)**.</span></span>
1. <span data-ttu-id="92bd2-281">ضمن **الأطراف المعتمِدة**، مع تحديد عنصر موفر هوية B2C أعلاه، قم بما يلي:</span><span class="sxs-lookup"><span data-stu-id="92bd2-281">Under **Relying Parties**, with the above B2C identity provider item selected, do the following:</span></span>
    1. <span data-ttu-id="92bd2-282">في المربع‏‎ **معرف العميل**، أدخل معرف تطبيق B2C.</span><span class="sxs-lookup"><span data-stu-id="92bd2-282">In the **ClientID** box, enter your B2C application ID.</span></span> <span data-ttu-id="92bd2-283">يمكنك العثور على هذا المعرف في مربع **معرف التطبيق** في صفحة خصائص تطبيق B2C.</span><span class="sxs-lookup"><span data-stu-id="92bd2-283">You can find this in the **Application ID** box of your B2C application's properties page.</span></span>
    1. <span data-ttu-id="92bd2-284">في مربع **النوع**، أدخل **عام**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-284">In the **Type** box, enter **Public**.</span></span>
    1. <span data-ttu-id="92bd2-285">في مربع **نوع المستخدم**، أدخل **عميل**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-285">In the **User Type** box, enter **Customer**.</span></span>
1. <span data-ttu-id="92bd2-286">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-286">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="92bd2-287">في مربع البحث في Commerce، ابحث عن **جدول التوزيع**</span><span class="sxs-lookup"><span data-stu-id="92bd2-287">In the Commerce search box, search for **Distribution schedule**</span></span>
1. <span data-ttu-id="92bd2-288">في قائمة التنقل اليسرة من صفحة **جداول التوزيع**، حدد الوظيفة **1110 تكوين عمومي**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-288">In the left navigation menu of the **Distribution schedules** page, select job **1110 Global configuration**.</span></span>
1. <span data-ttu-id="92bd2-289">في جزء الإجراءات، حدد **تشغيل الآن**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-289">On the action pane, select **Run Now**.</span></span>

### <a name="obtain-issuer-url"></a><span data-ttu-id="92bd2-290">الحصول على عنوان URL للمصدر</span><span class="sxs-lookup"><span data-stu-id="92bd2-290">Obtain issuer URL</span></span>

<span data-ttu-id="92bd2-291">للحصول على عنوان URL لمصدر موفر الهوية، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="92bd2-291">To obtain your identity provider issuer URL, follow these steps.</span></span>

1. <span data-ttu-id="92bd2-292">قم بإنشاء عنوان URL لعنوان بيانات التعريف بالتنسيق التالي باستخدام سياسة ومستأجر B2C: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``</span><span class="sxs-lookup"><span data-stu-id="92bd2-292">Create a metadata address URL in the following format using your B2C tenant and policy: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``</span></span>
    - <span data-ttu-id="92bd2-293">مثال: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.</span><span class="sxs-lookup"><span data-stu-id="92bd2-293">Example: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.</span></span>
1. <span data-ttu-id="92bd2-294">أدخل عنوان URL لعنوان بيانات التعريف في شريط العناوين في المستعرض.</span><span class="sxs-lookup"><span data-stu-id="92bd2-294">Enter the metadata address URL into a browser address bar.</span></span>
1. <span data-ttu-id="92bd2-295">في بيانات التعريف، انسخ عنوان URL لمصدر موفر الهوية (قيمة **"المصدر"**).</span><span class="sxs-lookup"><span data-stu-id="92bd2-295">In the metadata, copy the identity provider issuer URL (the value for **"issuer"**).</span></span>
    - <span data-ttu-id="92bd2-296">مثال: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.</span><span class="sxs-lookup"><span data-stu-id="92bd2-296">Example: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.</span></span>

## <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a><span data-ttu-id="92bd2-297">تكوين مستأجر B2C في منشئ موقع Commerce</span><span class="sxs-lookup"><span data-stu-id="92bd2-297">Configure your B2C tenant in Commerce site builder</span></span>

<span data-ttu-id="92bd2-298">وبمجرد اكتمال إعداد مستأجر Azure AD B2C، يجب تكوين مستأجر B2C في منشئ موقع Commerce.</span><span class="sxs-lookup"><span data-stu-id="92bd2-298">Once setup of your Azure AD B2C tenant is completed, you must configure the B2C tenant in Commerce site builder.</span></span> <span data-ttu-id="92bd2-299">تتضمن خطوات التكوين تجميع معلومات تطبيق B2C من مدخل Azure، وإدخال معلومات تطبيق B2C في منشئ الموقع، ثم ربط تطبيق B2C بموقعك وقناتك.</span><span class="sxs-lookup"><span data-stu-id="92bd2-299">Configuration steps include collecting B2C application information from the Azure portal, entering that B2C application information into site builder, and then associating the B2C application with your site and channel.</span></span>

### <a name="collect-the-required-application-information"></a><span data-ttu-id="92bd2-300">تجميع معلومات التطبيق المطلوبة</span><span class="sxs-lookup"><span data-stu-id="92bd2-300">Collect the required application information</span></span>

<span data-ttu-id="92bd2-301">لتجميع معلومات التطبيق المطلوبة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="92bd2-301">To collect the required application information, follow these steps.</span></span>

1. <span data-ttu-id="92bd2-302">في مدخل Azure، انتقل إلى **الصفحة الرئيسية \> Azure AD B2C - تطبيقات**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-302">In the Azure portal, go to **Home \> Azure AD B2C - Applications**.</span></span>
1. <span data-ttu-id="92bd2-303">حدد تطبيقك، ثم حدد **خصائص** في جزء التنقل الأيسر للحصول على تفاصيل التطبيق.</span><span class="sxs-lookup"><span data-stu-id="92bd2-303">Select your application, and then in the left navigation pane select **Properties** to obtain the application details.</span></span>
1. <span data-ttu-id="92bd2-304">من المربع **معرف التطبيق**، قم بتجميع معرف التطبيق الخاص بتطبيق B2C الذي تم إنشاؤه في مستأجر B2C.</span><span class="sxs-lookup"><span data-stu-id="92bd2-304">From the **Application ID** box, collect the application ID of the B2C application created in your B2C tenant.</span></span> <span data-ttu-id="92bd2-305">سيتم إدخاله في وقت لاحق على أنه **GUID‎ العميل** في منشئ الموقع.</span><span class="sxs-lookup"><span data-stu-id="92bd2-305">This will later be entered as the **Client GUID** in site builder.</span></span>
1. <span data-ttu-id="92bd2-306">تحت **عنوان URL الخاص بالرج**، قم تجميع عنوان URL الخاص بالرد.</span><span class="sxs-lookup"><span data-stu-id="92bd2-306">Under **Reply URL**, collect the reply URL.</span></span>
1. <span data-ttu-id="92bd2-307">انتقل إلى **الصفحة الرئيسية \> Azure AD B2C – تدفقات المستخدم (السياسات)**، ثم اجمع أسماء كل تدفق سياسة مستخدم.</span><span class="sxs-lookup"><span data-stu-id="92bd2-307">Go to **Home \> Azure AD B2C – User flows (policies)**, and then collect the names of each user flow policy.</span></span>

<span data-ttu-id="92bd2-308">تعرض الصورة التالية مثالاً عن صفحة **Azure AD B2C - التطبيقات**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-308">The following image shows an example of the **Azure AD B2C - Applications** page.</span></span>

![الانتقال إلى تطبيق B2C داخل المستأجر](./media/B2CImage_19.png)

<span data-ttu-id="92bd2-310">تعرض الصورة التالية مثالاً عن صفحة **خصائص** التطبيق في Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="92bd2-310">The following image shows an example of an application **Properties** page in Azure AD B2C.</span></span> 

![نسخ معرف التطبيق من خصائص تطبيق B2C](./media/B2CImage_21.png)

<span data-ttu-id="92bd2-312">تعرض الصورة التالية مثالاً عن سياسات تدفق المستخدم في صفحة **Azure AD B2C – تدفقات المستخدم (السياسات)**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-312">The following image shows an example of user flow policies on the **Azure AD B2C – User flows (policies)** page.</span></span>

![جمع أسماء كل تدفق سياسة B2C](./media/B2CImage_22.png)

### <a name="enter-your-aad-b2c-tenant-application-information-into-commerce"></a><span data-ttu-id="92bd2-314">إدخال معلومات تطبيق مستأجر AAD B2C في Commerce</span><span class="sxs-lookup"><span data-stu-id="92bd2-314">Enter your AAD B2C tenant application information into Commerce</span></span>

<span data-ttu-id="92bd2-315">يجب إدخال التفاصيل الخاصة بمستأجر Azure AD B2C في منشئ موقع Commerce قبل ربط مستأجر B2C بموقعك (مواقعك).</span><span class="sxs-lookup"><span data-stu-id="92bd2-315">You must enter details of the Azure AD B2C tenant into Commerce site builder before associating the B2C tenant with your site(s).</span></span>

<span data-ttu-id="92bd2-316">لإضافة معلومات تطبيق مستأجر AAD B2C إلى Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="92bd2-316">To add your AAD B2C tenant application information to Commerce, follow these steps.</span></span>

1. <span data-ttu-id="92bd2-317">سجل دخولك كمسؤول إلى منشئ موقع Commerce لبيئتك.</span><span class="sxs-lookup"><span data-stu-id="92bd2-317">Sign in as an administrator to Commerce site builder for your environment.</span></span>
1. <span data-ttu-id="92bd2-318">في جزء التنقل الأيسر، حدد **إعدادات المستأجر** لتوسيعه.</span><span class="sxs-lookup"><span data-stu-id="92bd2-318">In the left navigation pane, select **Tenant Settings**  to expand it.</span></span>
1. <span data-ttu-id="92bd2-319">ضمن **إعدادات المستأجر**، حدد **إعدادات B2C**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-319">Under **Tenant Settings**, select **B2C Settings**.</span></span> 
1. <span data-ttu-id="92bd2-320">في النافذة الرئيسية، إلى جانب **تطبيقات B2C**، حدد **إدارة**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-320">In the main window next **B2C Applications**, select **Manage**.</span></span> <span data-ttu-id="92bd2-321">(إذا ظهر المستأجر في قائمة تطبيقات B2C، فهذا يعني أنه أضيف بواسطة المسؤول.</span><span class="sxs-lookup"><span data-stu-id="92bd2-321">(If your tenant appears in the B2C Applications list, then it was already added by an administrator.</span></span> <span data-ttu-id="92bd2-322">تحقق من تطابق البنود الموجودة في الخطوة 6 أدناه مع تطبيق B2C.)</span><span class="sxs-lookup"><span data-stu-id="92bd2-322">Verify that the items in step 6 below match your B2C Application.)</span></span>
1. <span data-ttu-id="92bd2-323">حدد **إضافة تطبيق B2C**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-323">Select **Add B2C Application**.</span></span>
1. <span data-ttu-id="92bd2-324">أدخل البنود المطلوبة التالية في النموذج المعروض، باستخدام قيم من مستأجر B2C وتطبيقك.</span><span class="sxs-lookup"><span data-stu-id="92bd2-324">Enter the following required items in the form displayed, using values from your B2C tenant and application.</span></span> <span data-ttu-id="92bd2-325">يمكن ترك الحقول غير المطلوبة (تلك التي لا توجد علامة نجمية إلى جانبها) فارغة.</span><span class="sxs-lookup"><span data-stu-id="92bd2-325">Fields that are not required (those without an asterisk) may be left blank.</span></span>

    - <span data-ttu-id="92bd2-326">**اسم التطبيق**: اسم تطبيق B2C، على سبيل المثال "Fabrikam B2C".</span><span class="sxs-lookup"><span data-stu-id="92bd2-326">**Application Name**: The name for your B2C Application, for example "Fabrikam B2C".</span></span>
    - <span data-ttu-id="92bd2-327">**اسم المستأجر**: اسم مستأجر B2C الخاص بك (على سبيل المثال، استخدم "‏‫شركة الاتحاد للتصنيع‬" إذا ظهر المجال على أنه "fabrikam.onmicrosoft.com" للمستاجر B2C).</span><span class="sxs-lookup"><span data-stu-id="92bd2-327">**Tenant Name**: The name of your B2C tenant (for example, use "fabrikam" if the domain appears as "fabrikam.onmicrosoft.com" for the B2C tenant).</span></span> 
    - <span data-ttu-id="92bd2-328">**معرف سياسة نسيان كلمة المرور**: معرف سياسة تدفق المستخدم لنسيان كلمة المرور، على سبيل المثال "B2C_1_PasswordReset".</span><span class="sxs-lookup"><span data-stu-id="92bd2-328">**Forget Password Policy ID**: The forget password user flow policy ID, for example "B2C_1_PasswordReset".</span></span>
    - <span data-ttu-id="92bd2-329">**معرف سياسة التسجيل وتسجيل الدخول**: معرف سياسة تدفق المستخدم للتسجيل وتسجيل الدخول، على سبيل المثال "B2C_1_signup_signin".</span><span class="sxs-lookup"><span data-stu-id="92bd2-329">**Signup Signin Policy ID**: The sign up and sign in user flow policy ID, for example "B2C_1_signup_signin".</span></span>
    - <span data-ttu-id="92bd2-330">**GUID‏‎ العميل**: معرف تطبيق B2C، على سبيل المثال "22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6".</span><span class="sxs-lookup"><span data-stu-id="92bd2-330">**Client GUID**: The B2C application ID, for example "22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6".</span></span>
    - <span data-ttu-id="92bd2-331">**معرف سياسة تحرير ملف التعريف**: معرف سياسة تدفق المستخدم لتحرير ملف التعريف، على سبيل المثال، "B2C_1A_ProfileEdit".</span><span class="sxs-lookup"><span data-stu-id="92bd2-331">**Edit Profile Policy ID**: The profile editing user flow policy ID, for example "B2C_1A_ProfileEdit".</span></span>

1. <span data-ttu-id="92bd2-332">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-332">Select **OK**.</span></span> <span data-ttu-id="92bd2-333">من المفترض أن يظهر الآن اسم تطبيق B2C في القائمة.</span><span class="sxs-lookup"><span data-stu-id="92bd2-333">You should now see the name of your B2C application appear in the list.</span></span>
1. <span data-ttu-id="92bd2-334">حدد **حفظ** لحفظ تغييراتك.</span><span class="sxs-lookup"><span data-stu-id="92bd2-334">Select **Save** to save your changes.</span></span>

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a><span data-ttu-id="92bd2-335">ربط تطبيق B2C بموقعك وقناتك</span><span class="sxs-lookup"><span data-stu-id="92bd2-335">Associate the B2C application to your site and channel</span></span>

> [!WARNING]
> <span data-ttu-id="92bd2-336">إذا كان موقعك مرتبطًا بتطبيق B2C، فسيؤدي التغيير إلى تطبيق B2C مختلف إلى إزالة المراجع الحالية التي تم تأسيسها للمستخدمين الذين قاموا بالتسجيل في هذه البيئة.</span><span class="sxs-lookup"><span data-stu-id="92bd2-336">If your site is already associated with a B2C application, changing to a different B2C application will remove the current references established for users already signed up in this environment.</span></span> <span data-ttu-id="92bd2-337">إذا حصل التغيير، فإن أي بيانات اعتماد مرتبطة بتطبيق B2C المعين حاليًا لن تكون متوفرة للمستخدمين.</span><span class="sxs-lookup"><span data-stu-id="92bd2-337">If changed, any credentials associated with the currently-assigned B2C application will not be available to users.</span></span> 
> 
> <span data-ttu-id="92bd2-338">قم بتحديث تطبيق B2C فقط إذا كنت تعمل على اعداد تطبيق B2C الخاص بالقناة للمرة الأولى أو إذا كنت تريد من المستخدمين إعادة التسجيل باستخدام بيانات اعتماد جديدة لهذه القناة مع تطبيق B2C الجديد.</span><span class="sxs-lookup"><span data-stu-id="92bd2-338">Only update the B2C application if you are setting up the channel's B2C application for the first time or if you intend to have users re-sign up with new credentials to this channel with the new B2C application.</span></span> <span data-ttu-id="92bd2-339">يجب توخي الحذر عند ربط القنوات بتطبيقات B2C، واحرص على تسمية التطبيقات بطريقة واضحة.</span><span class="sxs-lookup"><span data-stu-id="92bd2-339">Take caution when associating channels to B2C applications, and name applications clearly.</span></span> <span data-ttu-id="92bd2-340">إذا لم تكن قناة مرتبطة بتطبيق B2C في الخطوات أدناه، فإن المستخدمين الذين يسجلون دخولهم إلى هذه القناة لموقعك سيدخلون إلى تطبيق B2C الذي يظهر على أنه **افتراضي** في قائمة **إعدادات المستأجر \> إعدادات B2C** لتطبيقات B2C.</span><span class="sxs-lookup"><span data-stu-id="92bd2-340">If a channel is not associated to a B2C application in the steps below, users signing into that channel for your site will be entered into the B2C application showing as **default** in the **Tenant Settings \> B2C Settings** list of B2C applications.</span></span>

<span data-ttu-id="92bd2-341">لربط تطبيق B2C بموقعك وقناتك، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="92bd2-341">To associate the B2C application to your site and channel, follow these steps.</span></span>

1. <span data-ttu-id="92bd2-342">انتقل إلى موقعك في منشئ موقع Commerce.</span><span class="sxs-lookup"><span data-stu-id="92bd2-342">Navigate to your site in Commerce site builder.</span></span>
1. <span data-ttu-id="92bd2-343">في جزء التنقل الأيسر، حدد **إعدادات الموقع** لتوسيعه.</span><span class="sxs-lookup"><span data-stu-id="92bd2-343">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="92bd2-344">ضمن **إعدادات الموقع**، حدد **القنوات**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-344">Below **Site Settings**, select **Channels**.</span></span>
1. <span data-ttu-id="92bd2-345">في النافذة الرئيسية، ضمن **القنوات‏‎**، حدد قناتك.</span><span class="sxs-lookup"><span data-stu-id="92bd2-345">In the main window under **Channels**, select your channel.</span></span>
1. <span data-ttu-id="92bd2-346">في جزء خصائص القناة إلى اليسار، حدد اسم تطبيق B2C من القائمة المنسدلة **تحديد تطبيق B2C**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-346">In the channel properties pane on the right, select your B2C application name from the **Select B2C Application** drop down menu.</span></span>
1. <span data-ttu-id="92bd2-347">حدد **إغلاق**، ثم حدد **حفظ ونشر**.</span><span class="sxs-lookup"><span data-stu-id="92bd2-347">Select **Close**, and then select **Save and Publish**.</span></span>

## <a name="additional-b2c-information"></a><span data-ttu-id="92bd2-348">معلومات B2C إضافية</span><span class="sxs-lookup"><span data-stu-id="92bd2-348">Additional B2C information</span></span>

### <a name="customer-migration"></a><span data-ttu-id="92bd2-349">ترحيل العملاء</span><span class="sxs-lookup"><span data-stu-id="92bd2-349">Customer migration</span></span>

<span data-ttu-id="92bd2-350">إذا كنت ترغب في ترحيل سجلات العملاء من نظام موفر الهوية السابق، فيرجى العمل مع فريق Dynamics 365 Commerce لمراجعة احتياجات ترحيل العملاء.</span><span class="sxs-lookup"><span data-stu-id="92bd2-350">If you are considering migrating customer records from a previous identity provider platform, please work with the Dynamics 365 Commerce team to review your customer migration needs.</span></span>

<span data-ttu-id="92bd2-351">للحصول على وثائق Azure AD B2C إضافة حول ترحيل العملاء، راجع [ترحيل العملاء إلى Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).</span><span class="sxs-lookup"><span data-stu-id="92bd2-351">For additional Azure AD B2C documentation on customer migration, see [Migrate users to Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).</span></span>

### <a name="custom-policies"></a><span data-ttu-id="92bd2-352">سياسات مخصصة</span><span class="sxs-lookup"><span data-stu-id="92bd2-352">Custom policies</span></span>

<span data-ttu-id="92bd2-353">للحصول على معلومات إضافية حول تخصيص تفاعلات وتدفقات سياسة Azure AD B2C بما يتجاوز ما تقدمه سياسات B2C القياسية، راجع [السياسات المخصصة في Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom).</span><span class="sxs-lookup"><span data-stu-id="92bd2-353">For additional information regarding customizing Azure AD B2C interactions and policy flows beyond what is offered by B2C standard policies, see [Custom policies in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom).</span></span> 

### <a name="secondary-admin"></a><span data-ttu-id="92bd2-354">المسؤول الثانوي</span><span class="sxs-lookup"><span data-stu-id="92bd2-354">Secondary admin</span></span>

<span data-ttu-id="92bd2-355">يمكن إضافة حساب مسؤول ثانوي اختياري في قسم **المستخدمون** في مستأجر B2C.</span><span class="sxs-lookup"><span data-stu-id="92bd2-355">An optional, secondary administrator account can be added in the **Users** section of your B2C tenant.</span></span> <span data-ttu-id="92bd2-356">قد يكون هذا الحساب مباشرًا أو عامًا.</span><span class="sxs-lookup"><span data-stu-id="92bd2-356">This can be a direct account or a general account.</span></span> <span data-ttu-id="92bd2-357">إذا أردت مشاركة حساب عبر موارد الفريق، يمكن أيضًا إنشاء حساب عام.</span><span class="sxs-lookup"><span data-stu-id="92bd2-357">If you need to share an account across team resources, a common account can also be created.</span></span> <span data-ttu-id="92bd2-358">بسبب حساسية البيانات المخزنة في Azure AD B2C، يجب مراقبة حساب عام عن كثب وفق ممارسات الأمان الخاصة بشركتك.</span><span class="sxs-lookup"><span data-stu-id="92bd2-358">Due to the sensitivity of the data stored in Azure AD B2C, a common account should be monitored closely per your company's security practices.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="92bd2-359">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="92bd2-359">Additional resources</span></span>

[<span data-ttu-id="92bd2-360">تكوين اسم مجالك</span><span class="sxs-lookup"><span data-stu-id="92bd2-360">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="92bd2-361">نشر مستأجر التجارة الإلكترونية الجديد</span><span class="sxs-lookup"><span data-stu-id="92bd2-361">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="92bd2-362">إنشاء موقع تجارة إلكترونية</span><span class="sxs-lookup"><span data-stu-id="92bd2-362">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="92bd2-363">إقران موقع Dynamics 365 Commerce بقناة عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="92bd2-363">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="92bd2-364">إدارة ملفات robots.txt</span><span class="sxs-lookup"><span data-stu-id="92bd2-364">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

<span data-ttu-id="92bd2-365">[يُعيد تحميل عنوان URL التوجيه بالإجمال](upload-bulk-redirects.md)إقران موقع Dynamics 365 Commerce بقناة عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="92bd2-365">[Upload URL redirects in bulk](upload-bulk-redirects.md)Associate a Dynamics 365 Commerce site with an online channel</span></span>

[<span data-ttu-id="92bd2-366">إعداد صفحات مخصصة لعمليات تسجيل دخول المستخدمين</span><span class="sxs-lookup"><span data-stu-id="92bd2-366">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="92bd2-367">تكوين العديد من مستأجرين شركة إلى عميل في بيئة Commerce</span><span class="sxs-lookup"><span data-stu-id="92bd2-367">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="92bd2-368">إضافة الدعم إلى شبكة تسليم المحتوى (CDN)</span><span class="sxs-lookup"><span data-stu-id="92bd2-368">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="92bd2-369">تمكين اكتشاف المتجر استنادًا إلى الموقع</span><span class="sxs-lookup"><span data-stu-id="92bd2-369">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
