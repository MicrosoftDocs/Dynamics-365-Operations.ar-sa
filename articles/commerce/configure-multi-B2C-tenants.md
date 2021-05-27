---
title: تكوين عدة مستأجرين B2C في بيئة Commerce
description: يوضح هذا الموضوع متى وكيفية إعداد عدة مستأجري متاجرة بين عمل ومستهلك (B2C) لكل قناة Microsoft Azure Active Directory (Azure AD) لمصادقة المستخدم في بيئة Dynamics 365 Commerce مخصصة.
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
ms.search.validFrom: 2020-02-12
ms.dyn365.ops.version: ''
ms.openlocfilehash: c813adb79ae1b78a052332e077393f125830633f
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6027712"
---
# <a name="configure-multiple-b2c-tenants-in-a-commerce-environment"></a><span data-ttu-id="1dca3-103">تكوين عدة مستأجرين B2C في بيئة Commerce</span><span class="sxs-lookup"><span data-stu-id="1dca3-103">Configure multiple B2C tenants in a Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1dca3-104">يوضح هذا الموضوع متى وكيفية إعداد عدة مستأجري متاجرة بين عمل ومستهلك (B2C) لكل قناة Microsoft Azure Active Directory (Azure AD) لمصادقة المستخدم في بيئة Dynamics 365 Commerce مخصصة.</span><span class="sxs-lookup"><span data-stu-id="1dca3-104">This topic describes when and how to set up multiple Microsoft Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants per channel for user authentication in a dedicated Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="1dca3-105">يستخدم Dynamics 365 Commerce خدمة الهوية عبر السحابة Azure AD B2C لدعم بيانات اعتماد المستخدم وتدفقات المصادقة.</span><span class="sxs-lookup"><span data-stu-id="1dca3-105">Dynamics 365 Commerce uses the Azure AD B2C cloud identity service to support user credentials and authentication flows.</span></span> <span data-ttu-id="1dca3-106">بإمكان المستخدمين استخدام تدفقات المصادقة للتسجيل، وتسجيل الدخول، وإعادة تعيين كلمه المرور.</span><span class="sxs-lookup"><span data-stu-id="1dca3-106">Users can use the authentication flows to sign up, sign in, and reset their password.</span></span> <span data-ttu-id="1dca3-107">يقوم Azure AD B2C بتخزين معلومات المصادقة الحساسة للمستخدم، مثل اسم المستخدم وكلمة المرور.</span><span class="sxs-lookup"><span data-stu-id="1dca3-107">Azure AD B2C stores a user's sensitive authentication information, such as the user name and password.</span></span> <span data-ttu-id="1dca3-108">ويكون سجل المستخدمين فريدًا لكل مستأجر B2C، ويستخدم إما بيانات اعتماد اسم المستخدم (عنوان البريد إلكتروني) أو بيانات اعتماد موفر الهوية الاجتماعية.</span><span class="sxs-lookup"><span data-stu-id="1dca3-108">The user record is unique to each B2C tenant, and it uses either user name (email address) credentials or social identity provider credentials.</span></span>

<span data-ttu-id="1dca3-109">في معظم الحالات، يتم استخدام مستأجر Azure AD B2C في بيئة Commerce.</span><span class="sxs-lookup"><span data-stu-id="1dca3-109">In most cases, a single Azure AD B2C tenant is used in a Commerce environment.</span></span> <span data-ttu-id="1dca3-110">بعد ذلك، يستطيع عملاء Commerce إنشاء مواقع متعددة ونشرها في بيئة Commerce نفسها، كما سيتم استخدام بيانات اعتماد العميل نفسها عبر هذه المواقع.</span><span class="sxs-lookup"><span data-stu-id="1dca3-110">Commerce customers can then create and publish multiple sites in the same Commerce environment, and the same customer credentials will be used across these sites.</span></span> <span data-ttu-id="1dca3-111">لكن، إذا كان يجب معاملة المواقع في البيئة كعلامات تجارية مختلفة، وإذا كانت تظهر للمستخدمين كأعمال منفصلة، يمكن تكوين مستأجر B2C للقناة المستخدمة لفصل الموقع/العلامة التجارية.</span><span class="sxs-lookup"><span data-stu-id="1dca3-111">However, if the sites in the environment should be treated as different brands and appear to users as separate businesses, a B2C tenant can be configured for the channel that is used for the site/brand separation.</span></span>

## <a name="considerations-when-multiple-b2c-tenants-are-set-up-per-channel"></a><span data-ttu-id="1dca3-112">أمور يجب مراعاتها عند إعداد عدة مستأجرين B2C لكل قناة</span><span class="sxs-lookup"><span data-stu-id="1dca3-112">Considerations when multiple B2C tenants are set up per channel</span></span>

<span data-ttu-id="1dca3-113">في أغلب الأحيان، عندما يتم التعامل مع كل قناة أو موقع على أنه عمل منفصل، فان أفضل خيار بالنسبة لتدفقات مصادقه المستخدم في Commerce هو استخدام كيانات قانونيه منفصلة.</span><span class="sxs-lookup"><span data-stu-id="1dca3-113">Often, when each channel or site is being treated as a separate business, the best option with respect to user authentication flows in Commerce is to use separate legal entities.</span></span> <span data-ttu-id="1dca3-114">ومع ذلك، إذا كنت ترغب في الاحتفاظ بكل قناة/موقع في نفس البيئة والكيان القانوني، ولكنك تريد أن يكون لديك مصادقه مستخدم منفصلة لكل موقع، فمن المهم مراعاة النقاط التالية قبل المتابعة:</span><span class="sxs-lookup"><span data-stu-id="1dca3-114">However, if you want to keep each channel/site in the same environment and legal entity, but want to have separate user authentication for each site, it's important that you consider the following points before you proceed:</span></span>

- <span data-ttu-id="1dca3-115">سيحصل المستخدمون على بيانات الاعتماد المميزة الخاصة بهم لكل قناة/موقع.</span><span class="sxs-lookup"><span data-stu-id="1dca3-115">Users will have their own distinct credentials for each channel/site.</span></span>

    <span data-ttu-id="1dca3-116">بإمكان الشخص نفسه امتلاك حسابين منفصلين لكل قناة/موقع، لأن كل حساب سيكون إدخالاً فريدًا في مستأجر B2C منفصل.</span><span class="sxs-lookup"><span data-stu-id="1dca3-116">The same person can have two separate accounts per channel/site, because each account will be a unique entry into a separate B2C tenant.</span></span>

- <span data-ttu-id="1dca3-117">في بيئة Microsoft Dynamics، سيتم إرجاع سجلات عميل منفصلة لعمليات البحث العمومية عن السجلات.</span><span class="sxs-lookup"><span data-stu-id="1dca3-117">In the Microsoft Dynamics environment, separate customer records will be returned for global record searches.</span></span>

    <span data-ttu-id="1dca3-118">إذا استخدم المستخدم نفس عنوان البريد الإلكتروني عبر القنوات/المواقع، فإن عمليات البحث العمومية ستؤدي إلى إرجاع نتائج لكل قناة/موقع.</span><span class="sxs-lookup"><span data-stu-id="1dca3-118">If a user uses the same email address across channels/sites, global customer searches will return results for each channel/site.</span></span> <span data-ttu-id="1dca3-119">(سيتم إظهار مؤشر القناة.)</span><span class="sxs-lookup"><span data-stu-id="1dca3-119">(A channel indicator will be shown.)</span></span>

- <span data-ttu-id="1dca3-120">يمكن استخدام دفتر العناوين للمساعدة في تجميع المستخدمين، بحيث يمكن تعقبهم لكل قناة.</span><span class="sxs-lookup"><span data-stu-id="1dca3-120">The address book can be used to help group users, so that they can be tracked per channel.</span></span>
- <span data-ttu-id="1dca3-121">قد يزداد عدد سجلات العملاء لكل قناة، وقد تؤثر هذه الزيادة على أداء عمليات البحث العمومية عن العملاء.</span><span class="sxs-lookup"><span data-stu-id="1dca3-121">The number of customer records per channel might increase, and this increase might affect the performance of global customer searches.</span></span>
- <span data-ttu-id="1dca3-122">يجب أن يتم تعيين مستأجري B2C إلى قناة بعناية، للمساعدة في منع الحالات التي يقوم فيها العملاء بالتسجيل للحصول على مستأجر غير صحيح.</span><span class="sxs-lookup"><span data-stu-id="1dca3-122">B2C tenants must be carefully mapped to a channel, to help prevent situations where customers sign up for an incorrect tenant.</span></span> <span data-ttu-id="1dca3-123">وإلا، يمكن حدوث التباس أو مشاكل في التعقب.</span><span class="sxs-lookup"><span data-stu-id="1dca3-123">Otherwise, confusion or tracking issues can occur.</span></span>

<span data-ttu-id="1dca3-124">يبين الرسم التوضيحي التالي مستأجري B2C متعددين في بيئة Commerce.</span><span class="sxs-lookup"><span data-stu-id="1dca3-124">The following illustration shows multiple B2C tenants in a Commerce environment.</span></span>

![مستأجرو B2C متعددون في بيئة Commerce](media/MultiB2C_In_Environment.png)

<span data-ttu-id="1dca3-126">إذا قررت أن أعمالك تتطلب مستأجري B2C متميزين لكل قناة في بيئة Commerce نفسها، فأكمل الإجراءات الموجودة في الأقسام التالية لطلب هذه الميزة.</span><span class="sxs-lookup"><span data-stu-id="1dca3-126">If you decide that your business requires distinct B2C tenants per channel in the same Commerce environment, complete the procedures in the following sections to request this feature.</span></span>

## <a name="configure-b2c-tenants-in-your-environment"></a><span data-ttu-id="1dca3-127">تكوين مستأجري B2C في بيئتك</span><span class="sxs-lookup"><span data-stu-id="1dca3-127">Configure B2C tenants in your environment</span></span>

<span data-ttu-id="1dca3-128">لتكوين مستأجري B2C في بيئتك، أكمل الإجراءات ذات الصلة في هذا القسم.</span><span class="sxs-lookup"><span data-stu-id="1dca3-128">To configure B2C tenants in your environment, complete the relevant procedures in this section.</span></span>

### <a name="add-an-azure-ad-b2c-tenant"></a><span data-ttu-id="1dca3-129">إضافة مستأجر Azure AD B2C</span><span class="sxs-lookup"><span data-stu-id="1dca3-129">Add an Azure AD B2C tenant</span></span>

<span data-ttu-id="1dca3-130">لإضافة مستأجر Azure AD B2C إلى بيئتك، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="1dca3-130">To add an Azure AD B2C tenant to your environment, follow these steps.</span></span>

1. <span data-ttu-id="1dca3-131">قم بتسجيل الدخول إلى منشئ موقع Commerce لبيئتك كمسؤول نظام. لتكوين مستأجري Azure AD B2C، يجب أن تكون مسؤول نظام لبيئة Commerce.</span><span class="sxs-lookup"><span data-stu-id="1dca3-131">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="1dca3-132">في جزء التنقل الأيسر، حدد **إعدادات المستأجر** لتوسيعه.</span><span class="sxs-lookup"><span data-stu-id="1dca3-132">In the left navigation pane, select **Tenant Settings** to expand it.</span></span>
1. <span data-ttu-id="1dca3-133">حدد **إعدادات B2C**، ثم حدد **إدارة**.</span><span class="sxs-lookup"><span data-stu-id="1dca3-133">Select **B2C Settings**, and then select **Manage**.</span></span>
1. <span data-ttu-id="1dca3-134">حدد **إضافة تطبيق B2C**، ثم أدخل المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="1dca3-134">Select **Add B2C Application**, and then enter the following information:</span></span>

    - <span data-ttu-id="1dca3-135">**اسم التطبيق**: أدخل الاسم الذي ينبغي استخدامه للتطبيق في سياق إدارته في Commerce.</span><span class="sxs-lookup"><span data-stu-id="1dca3-135">**Application Name**: Enter the name that should be used for the application in the context of managing it in Commerce.</span></span> <span data-ttu-id="1dca3-136">نوصي باستخدام اسم التطبيق الذي اخترته عند إعداد تطبيق Azure AD B2C في مدخل Azure.</span><span class="sxs-lookup"><span data-stu-id="1dca3-136">We recommend that you use the application name that you chose when you set up the Azure AD B2C application in the Azure portal.</span></span> <span data-ttu-id="1dca3-137">وبهذه الطريقة، يمكنك المساعدة على تقليل الالتباس عند إدارة مستأجري B2C في Commerce.</span><span class="sxs-lookup"><span data-stu-id="1dca3-137">In this way, you can help reduce confusion when you manage B2C tenants in Commerce.</span></span>
    - <span data-ttu-id="1dca3-138">**اسم المستأجر**: أدخل اسم مستأجر B2C كما يظهر في مدخل Azure.</span><span class="sxs-lookup"><span data-stu-id="1dca3-138">**Tenant Name**: Enter the B2C tenant name as it appears in the Azure portal.</span></span>
    - <span data-ttu-id="1dca3-139">**معرف سياسة نسيان كلمة المرور**: أدخل معرف السياسة (اسم السياسة في مدخل Azure).</span><span class="sxs-lookup"><span data-stu-id="1dca3-139">**Forget Password Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>
    - <span data-ttu-id="1dca3-140">**معرف سياسة التسجيل وتسجيل الدخول**: أدخل معرف السياسة (اسم السياسة في مدخل Azure).</span><span class="sxs-lookup"><span data-stu-id="1dca3-140">**Signup Signin Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>
    - <span data-ttu-id="1dca3-141">**GUID‎ العميل**: أدخل معرف مستأجر Azure AD B2C كما يظهر في مدخل Azure (وليس معرف التطبيق لمستأجر B2C).</span><span class="sxs-lookup"><span data-stu-id="1dca3-141">**Client GUID**: Enter the Azure AD B2C tenant ID as it appears in the Azure portal (not the application ID for the B2C tenant).</span></span>
    - <span data-ttu-id="1dca3-142">**تحرير معرف سياسة ملف التعريف**: أدخل معرف السياسة (اسم السياسة في مدخل Azure).</span><span class="sxs-lookup"><span data-stu-id="1dca3-142">**Edit Profile Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>

1. <span data-ttu-id="1dca3-143">عند الانتهاء من إدخال هذه المعلومات، حدد **موافق** لحفظ التغييرات.</span><span class="sxs-lookup"><span data-stu-id="1dca3-143">When you've finished entering this information, select **OK** to save your changes.</span></span> <span data-ttu-id="1dca3-144">يجب أن يظهر مستأجر Azure AD B2C الجديد في القائمة ضمن **إدارة تطبيقات B2C**.</span><span class="sxs-lookup"><span data-stu-id="1dca3-144">Your new Azure AD B2C tenant should now appear in the list under **Manage B2C Applications**.</span></span>

> [!NOTE]
> <span data-ttu-id="1dca3-145">يجب ترك حقول مثل **النطاق**، و **معرف السياسة غير التفاعلية**، و **معرف العميل غير التفاعلي**، و **المجال المخصص لتسجيل الدخول**، و **معرف سياسة التسجيل** فارغة إلا إذا طلب منك فريق Dynamics 365 Commerce تعيينها.</span><span class="sxs-lookup"><span data-stu-id="1dca3-145">You should leave fields such as **Scope**, **Non Interactive Policy ID**, **Non Interactive Client ID**, **Login Custom Domain**, and **Sign Up Policy ID** blank unless the Dynamics 365 Commerce team instructs you to set them.</span></span>


### <a name="manage-or-delete-an-azure-ad-b2c-tenant"></a><span data-ttu-id="1dca3-146">إدارة مستأجر Azure AD B2C أو حذفه</span><span class="sxs-lookup"><span data-stu-id="1dca3-146">Manage or delete an Azure AD B2C tenant</span></span>

1. <span data-ttu-id="1dca3-147">قم بتسجيل الدخول إلى منشئ موقع Commerce لبيئتك كمسؤول نظام. لتكوين مستأجري Azure AD B2C، يجب أن تكون مسؤول نظام لبيئة Commerce.</span><span class="sxs-lookup"><span data-stu-id="1dca3-147">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="1dca3-148">في جزء التنقل الأيسر، حدد **إعدادات المستأجر** لتوسيعه.</span><span class="sxs-lookup"><span data-stu-id="1dca3-148">In the left navigation pane, select **Tenant Settings** to expand it.</span></span>
1. <span data-ttu-id="1dca3-149">حدد **إعدادات B2C**، ثم حدد **إدارة**.</span><span class="sxs-lookup"><span data-stu-id="1dca3-149">Select **B2C Settings**, and then select **Manage**.</span></span>
1. <span data-ttu-id="1dca3-150">لتحرير مستأجر B2C، حدد رمز قلم الرصاص المجاور له.</span><span class="sxs-lookup"><span data-stu-id="1dca3-150">To edit a B2C tenant, select the pencil symbol next to it.</span></span> <span data-ttu-id="1dca3-151">لحذف مستأجر B2C، حدد رمز سلة المهملات المجاور له.</span><span class="sxs-lookup"><span data-stu-id="1dca3-151">To delete a B2C tenant, select the trash can symbol next to it.</span></span>
1. <span data-ttu-id="1dca3-152">حدد **حفظ**، ثم حدد **نشر** لتنشيط التغييرات.</span><span class="sxs-lookup"><span data-stu-id="1dca3-152">Select **Save**, and then select **Publish** to activate your changes.</span></span>

> [!WARNING]
> <span data-ttu-id="1dca3-153">عند تكوين مستأجر B2C لموقع مباشر/منشور، ربما قام المستخدمون بالتسجيل باستخدام الحسابات الموجودة على المستأجر.</span><span class="sxs-lookup"><span data-stu-id="1dca3-153">When a B2C tenant is configured for a live/published site, users might have signed up by using accounts that are present on the tenant.</span></span> <span data-ttu-id="1dca3-154">إذا حذفت مستأجر تم تكوينه في قائمة **إعدادات مستأجر \> B2C**، فأنت تقوم بإزالة اقتران مستأجر B2C هذا من المواقع المقترنة بأي قنوات للمستأجر.</span><span class="sxs-lookup"><span data-stu-id="1dca3-154">If you delete a configured tenant on the **Tenant Settings \> B2C Tenant** menu, you remove the association of that B2C tenant from sites that are associated with any channels of the tenant.</span></span> <span data-ttu-id="1dca3-155">في هذه الحالة، قد يتعذر على المستخدمين لديك تسجيل الدخول إلى حساباتهم.</span><span class="sxs-lookup"><span data-stu-id="1dca3-155">In this case, your users might no longer be able to sign in to their accounts.</span></span> <span data-ttu-id="1dca3-156">لذلك، توخى الانتباه الشديد عند حذف مستأجر تم تكوينه.</span><span class="sxs-lookup"><span data-stu-id="1dca3-156">Therefore, use extreme caution when you delete a configured tenant.</span></span>
>
> <span data-ttu-id="1dca3-157">عند حذف مستأجر تم تكوينه، سيستمر الاحتفاظ بمستأجر B2C والسجلات، ولكن سيتم تغيير تكوين نظام Commerce لذلك المستأجر أو إزالته.</span><span class="sxs-lookup"><span data-stu-id="1dca3-157">When a configured tenant is deleted, the B2C tenant and records will continue to be maintained, but the Commerce system configuration of that tenant will be changed or removed.</span></span> <span data-ttu-id="1dca3-158">سيقوم المستخدمون الذين يحاولون التسجيل في الموقع أو تسجيل الدخول إليه بإنشاء سجل حساب جديد في مستأجر B2C الافتراضي أو المقترن حديثًا والذي تم تكوينه لقناة الموقع.</span><span class="sxs-lookup"><span data-stu-id="1dca3-158">Users who try to sign up or sign in to the site will create a new account record in the default or newly associated B2C tenant that is configured for the channel of the site.</span></span>

## <a name="configure-your-channel-with-a-b2c-tenant"></a><span data-ttu-id="1dca3-159">تكوين قناتك مع مستأجر B2C</span><span class="sxs-lookup"><span data-stu-id="1dca3-159">Configure your channel with a B2C tenant</span></span>

1. <span data-ttu-id="1dca3-160">قم بتسجيل الدخول إلى منشئ موقع Commerce لبيئتك كمسؤول نظام. لتكوين مستأجري Azure AD B2C، يجب أن تكون مسؤول نظام لبيئة Commerce.</span><span class="sxs-lookup"><span data-stu-id="1dca3-160">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="1dca3-161">في جزء التنقل الأيسر، حدد **إعدادات الموقع** لتوسيعه.</span><span class="sxs-lookup"><span data-stu-id="1dca3-161">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="1dca3-162">حدد **القنوات**، ثم حدد القناة المطلوب تكوينها.</span><span class="sxs-lookup"><span data-stu-id="1dca3-162">Select **Channels**, and then select the channel to configure.</span></span>
1. <span data-ttu-id="1dca3-163">في جزء الخصائص الموجود على اليمين، في الحقل **تحديد تطبيق B2C**، حدد مستأجر Azure AD B2C الذي تم تكوينه لاستخدامه في هذه القناة.</span><span class="sxs-lookup"><span data-stu-id="1dca3-163">In the properties pane on the right, in the **Select B2C Application** field, select the configured Azure AD B2C tenant to use for this channel.</span></span>
1. <span data-ttu-id="1dca3-164">في شريط الأوامر ، حدد **حفظ ونشر** للالتزام بالتكوين الجديد أو المحدث.</span><span class="sxs-lookup"><span data-stu-id="1dca3-164">On the command bar, select **Save and Publish** to commit the new or updated configuration.</span></span>

> [!WARNING]
> <span data-ttu-id="1dca3-165">إذا قمت بتغيير تطبيق B2C الذي تم تعيينه للقناة، فإنك تقوم بإزالة المراجع الحالية التي تم تأسيسها لأي مستخدمين قاموا بالتسجيل في البيئة.</span><span class="sxs-lookup"><span data-stu-id="1dca3-165">If you change the B2C application that is assigned to the channel, you remove the current references that have been established for any users who have already signed up in the environment.</span></span> <span data-ttu-id="1dca3-166">في هذه الحالة، لن تتوفر أي بيانات اعتماد مقترنة بتطبيق B2C المعين حاليًا للمستخدمين.</span><span class="sxs-lookup"><span data-stu-id="1dca3-166">In this case, any credentials that are associated with the currently assigned B2C application won't be available to users.</span></span> <span data-ttu-id="1dca3-167">لذلك، قم بتغيير تكوين قناة Azure AD B2C فقط إذا كنت تقوم بإعداد القناة لأول مرة، ولم يتمكن أي مستخدم من التسجيل.</span><span class="sxs-lookup"><span data-stu-id="1dca3-167">Therefore, change a channel Azure AD B2C configuration only if you're setting up the channel for the first time, and no users have been able to sign up.</span></span> <span data-ttu-id="1dca3-168">وإلا، فقد يضطر المستخدمون إلى التسجيل مرة أخرى لتأسيس سجل في مستأجر Azure AD B2C الجديد.</span><span class="sxs-lookup"><span data-stu-id="1dca3-168">Otherwise, users might have to sign up again to establish a record in the new Azure AD B2C tenant.</span></span>
## <a name="additional-resources"></a><span data-ttu-id="1dca3-169">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="1dca3-169">Additional resources</span></span>

[<span data-ttu-id="1dca3-170">تكوين اسم مجالك</span><span class="sxs-lookup"><span data-stu-id="1dca3-170">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="1dca3-171">نشر مستأجر التجارة الإلكترونية الجديد</span><span class="sxs-lookup"><span data-stu-id="1dca3-171">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="1dca3-172">إنشاء موقع تجارة إلكترونية</span><span class="sxs-lookup"><span data-stu-id="1dca3-172">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="1dca3-173">إقران موقع Dynamics 365 Commerce بقناة عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="1dca3-173">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="1dca3-174">إدارة ملفات robots.txt</span><span class="sxs-lookup"><span data-stu-id="1dca3-174">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="1dca3-175">تحميل عناوين URL لإعادة التوجيه‬ بشكل مجمع</span><span class="sxs-lookup"><span data-stu-id="1dca3-175">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="1dca3-176">إعداد مستأجر B2C في Commerce</span><span class="sxs-lookup"><span data-stu-id="1dca3-176">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="1dca3-177">إعداد صفحات مخصصة لعمليات تسجيل دخول المستخدمين</span><span class="sxs-lookup"><span data-stu-id="1dca3-177">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="1dca3-178">إضافة الدعم إلى شبكة تسليم المحتوى (CDN)</span><span class="sxs-lookup"><span data-stu-id="1dca3-178">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="1dca3-179">تمكين اكتشاف المتجر استنادًا إلى الموقع</span><span class="sxs-lookup"><span data-stu-id="1dca3-179">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
