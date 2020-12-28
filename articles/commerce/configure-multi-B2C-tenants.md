---
title: تكوين عدة مستأجرين B2C في بيئة Commerce
description: يوضح هذا الموضوع متى وكيفية إعداد عدة مستأجري متاجرة بين عمل ومستهلك (B2C) لكل قناة Microsoft Azure Active Directory (Azure AD) لمصادقة المستخدم في بيئة Dynamics 365 Commerce مخصصة.
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
ms.author: brshoo
ms.search.validFrom: 2020-02-12
ms.dyn365.ops.version: ''
ms.openlocfilehash: da27e3ed0a0e50126590609d09575befe17a7aa2
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517103"
---
# <a name="configure-multiple-b2c-tenants-in-a-commerce-environment"></a><span data-ttu-id="49422-103">تكوين عدة مستأجرين B2C في بيئة Commerce</span><span class="sxs-lookup"><span data-stu-id="49422-103">Configure multiple B2C tenants in a Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="49422-104">يوضح هذا الموضوع متى وكيفية إعداد عدة مستأجري متاجرة بين عمل ومستهلك (B2C) لكل قناة Microsoft Azure Active Directory (Azure AD) لمصادقة المستخدم في بيئة Dynamics 365 Commerce مخصصة.</span><span class="sxs-lookup"><span data-stu-id="49422-104">This topic describes when and how to set up multiple Microsoft Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants per channel for user authentication in a dedicated Dynamics 365 Commerce environment.</span></span>

## <a name="overview"></a><span data-ttu-id="49422-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="49422-105">Overview</span></span>

<span data-ttu-id="49422-106">يستخدم Dynamics 365 Commerce خدمة الهوية عبر السحابة Azure AD B2C لدعم بيانات اعتماد المستخدم وتدفقات المصادقة.</span><span class="sxs-lookup"><span data-stu-id="49422-106">Dynamics 365 Commerce uses the Azure AD B2C cloud identity service to support user credentials and authentication flows.</span></span> <span data-ttu-id="49422-107">بإمكان المستخدمين استخدام تدفقات المصادقة للتسجيل، وتسجيل الدخول، وإعادة تعيين كلمه المرور.</span><span class="sxs-lookup"><span data-stu-id="49422-107">Users can use the authentication flows to sign up, sign in, and reset their password.</span></span> <span data-ttu-id="49422-108">يقوم Azure AD B2C بتخزين معلومات المصادقة الحساسة للمستخدم، مثل اسم المستخدم وكلمه المرور الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="49422-108">Azure AD B2C stores a user's sensitive authentication information, such as his or her user name and password.</span></span> <span data-ttu-id="49422-109">ويكون سجل المستخدمين فريدًا لكل مستأجر B2C، ويستخدم إما بيانات اعتماد اسم المستخدم (عنوان البريد إلكتروني) أو بيانات اعتماد موفر الهوية الاجتماعية.</span><span class="sxs-lookup"><span data-stu-id="49422-109">The user record is unique to each B2C tenant, and it uses either user name (email address) credentials or social identity provider credentials.</span></span>

<span data-ttu-id="49422-110">في معظم الحالات، يتم استخدام مستأجر Azure AD B2C في بيئة Commerce.</span><span class="sxs-lookup"><span data-stu-id="49422-110">In most cases, a single Azure AD B2C tenant is used in a Commerce environment.</span></span> <span data-ttu-id="49422-111">بعد ذلك، يستطيع عملاء Commerce إنشاء مواقع متعددة ونشرها في بيئة Commerce نفسها، كما سيتم استخدام بيانات اعتماد العميل نفسها عبر هذه المواقع.</span><span class="sxs-lookup"><span data-stu-id="49422-111">Commerce customers can then create and publish multiple sites in the same Commerce environment, and the same customer credentials will be used across these sites.</span></span> <span data-ttu-id="49422-112">لكن، إذا كان يجب معاملة المواقع في البيئة كعلامات تجارية مختلفة، وإذا كانت تظهر للمستخدمين كأعمال منفصلة، يمكن تكوين مستأجر B2C للقناة المستخدمة لفصل الموقع/العلامة التجارية.</span><span class="sxs-lookup"><span data-stu-id="49422-112">However, if the sites in the environment should be treated as different brands and appear to users as separate businesses, a B2C tenant can be configured for the channel that is used for the site/brand separation.</span></span>

## <a name="considerations-when-multiple-b2c-tenants-are-set-up-per-channel"></a><span data-ttu-id="49422-113">أمور يجب مراعاتها عند إعداد عدة مستأجرين B2C لكل قناة</span><span class="sxs-lookup"><span data-stu-id="49422-113">Considerations when multiple B2C tenants are set up per channel</span></span>

<span data-ttu-id="49422-114">في أغلب الأحيان، عندما يتم التعامل مع كل قناة أو موقع على أنه عمل منفصل، فان أفضل خيار بالنسبة لتدفقات مصادقه المستخدم في Commerce هو استخدام كيانات قانونيه منفصلة.</span><span class="sxs-lookup"><span data-stu-id="49422-114">Often, when each channel or site is being treated as a separate business, the best option with respect to user authentication flows in Commerce is to use separate legal entities.</span></span> <span data-ttu-id="49422-115">ومع ذلك، إذا كنت ترغب في الاحتفاظ بكل قناة/موقع في نفس البيئة والكيان القانوني، ولكنك تريد أن يكون لديك مصادقه مستخدم منفصلة لكل موقع، فمن المهم مراعاة النقاط التالية قبل المتابعة:</span><span class="sxs-lookup"><span data-stu-id="49422-115">However, if you want to keep each channel/site in the same environment and legal entity, but want to have separate user authentication for each site, it's important that you consider the following points before you proceed:</span></span>

- <span data-ttu-id="49422-116">سيحصل المستخدمون على بيانات الاعتماد المميزة الخاصة بهم لكل قناة/موقع.</span><span class="sxs-lookup"><span data-stu-id="49422-116">Users will have their own distinct credentials for each channel/site.</span></span>

    <span data-ttu-id="49422-117">بإمكان الشخص نفسه امتلاك حسابين منفصلين لكل قناة/موقع، لأن كل حساب سيكون إدخالاً فريدًا في مستأجر B2C منفصل.</span><span class="sxs-lookup"><span data-stu-id="49422-117">The same person can have two separate accounts per channel/site, because each account will be a unique entry into a separate B2C tenant.</span></span>

- <span data-ttu-id="49422-118">في بيئة Microsoft Dynamics، سيتم إرجاع سجلات عميل منفصلة لعمليات البحث العمومية عن السجلات.</span><span class="sxs-lookup"><span data-stu-id="49422-118">In the Microsoft Dynamics environment, separate customer records will be returned for global record searches.</span></span>

    <span data-ttu-id="49422-119">إذا استخدم المستخدم نفس عنوان البريد الإلكتروني عبر القنوات/المواقع، فإن عمليات البحث العمومية ستؤدي إلى إرجاع نتائج لكل قناة/موقع.</span><span class="sxs-lookup"><span data-stu-id="49422-119">If a user uses the same email address across channels/sites, global customer searches will return results for each channel/site.</span></span> <span data-ttu-id="49422-120">(سيتم إظهار مؤشر القناة.)</span><span class="sxs-lookup"><span data-stu-id="49422-120">(A channel indicator will be shown.)</span></span>

- <span data-ttu-id="49422-121">يمكن استخدام دفتر العناوين للمساعدة في تجميع المستخدمين، بحيث يمكن تعقبهم لكل قناة.</span><span class="sxs-lookup"><span data-stu-id="49422-121">The address book can be used to help group users, so that they can be tracked per channel.</span></span>
- <span data-ttu-id="49422-122">قد يزداد عدد سجلات العملاء لكل قناة، وقد تؤثر هذه الزيادة على أداء عمليات البحث العمومية عن العملاء.</span><span class="sxs-lookup"><span data-stu-id="49422-122">The number of customer records per channel might increase, and this increase might affect the performance of global customer searches.</span></span>
- <span data-ttu-id="49422-123">يجب أن يتم تعيين مستأجري B2C إلى قناة بعناية، للمساعدة في منع الحالات التي يقوم فيها العملاء بالتسجيل للحصول على مستأجر غير صحيح.</span><span class="sxs-lookup"><span data-stu-id="49422-123">B2C tenants must be carefully mapped to a channel, to help prevent situations where customers sign up for an incorrect tenant.</span></span> <span data-ttu-id="49422-124">وإلا، يمكن حدوث التباس أو مشاكل في التعقب.</span><span class="sxs-lookup"><span data-stu-id="49422-124">Otherwise, confusion or tracking issues can occur.</span></span>

<span data-ttu-id="49422-125">يبين الرسم التوضيحي التالي مستأجري B2C متعددين في بيئة Commerce.</span><span class="sxs-lookup"><span data-stu-id="49422-125">The following illustration shows multiple B2C tenants in a Commerce environment.</span></span>

![مستأجرو B2C متعددون في بيئة Commerce](media/MultiB2C_In_Environment.png)

<span data-ttu-id="49422-127">إذا قررت أن أعمالك تتطلب مستأجري B2C متميزين لكل قناة في بيئة Commerce نفسها، فأكمل الإجراءات الموجودة في الأقسام التالية لطلب هذه الميزة.</span><span class="sxs-lookup"><span data-stu-id="49422-127">If you decide that your business requires distinct B2C tenants per channel in the same Commerce environment, complete the procedures in the following sections to request this feature.</span></span>

## <a name="request-that-b2c-per-channel-be-enabled-in-your-environment"></a><span data-ttu-id="49422-128">طلب تمكين B2C لكل قناة في بيئتك</span><span class="sxs-lookup"><span data-stu-id="49422-128">Request that B2C per channel be enabled in your environment</span></span>

<span data-ttu-id="49422-129">في الوقت الحالي، إذا كنت ترغب في توفير مستأجري B2C مميزين لكل قناة في بيئة Commerce نفسها، فيجب تقديم طلب إلى Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="49422-129">Currently, if you want distinct B2C tenants per channel to be available in the same Commerce environment, you must submit a request to Dynamics 365 Commerce.</span></span> <span data-ttu-id="49422-130">لمزيد من المعلومات، راجع [الحصول على دعم Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md)، أو ناقش هذه المشكلة مع جهة الاتصال الخاصة بحلول Commerce.</span><span class="sxs-lookup"><span data-stu-id="49422-130">For more information, see [Get support for Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md), or discuss this issue with your Commerce solutions contact.</span></span>

## <a name="configure-b2c-tenants-in-your-environment"></a><span data-ttu-id="49422-131">تكوين مستأجري B2C في بيئتك</span><span class="sxs-lookup"><span data-stu-id="49422-131">Configure B2C tenants in your environment</span></span>

<span data-ttu-id="49422-132">لتكوين مستأجري B2C في بيئتك، أكمل الإجراءات ذات الصلة في هذا القسم.</span><span class="sxs-lookup"><span data-stu-id="49422-132">To configure B2C tenants in your environment, complete the relevant procedures in this section.</span></span>

### <a name="add-an-azure-ad-b2c-tenant"></a><span data-ttu-id="49422-133">إضافة مستأجر Azure AD B2C</span><span class="sxs-lookup"><span data-stu-id="49422-133">Add an Azure AD B2C tenant</span></span>

<span data-ttu-id="49422-134">لإضافة مستأجر Azure AD B2C إلى بيئتك، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="49422-134">To add an Azure AD B2C tenant to your environment, follow these steps.</span></span>

1. <span data-ttu-id="49422-135">قم بتسجيل الدخول إلى منشئ موقع Commerce لبيئتك كمسؤول نظام. لتكوين مستأجري Azure AD B2C، يجب أن تكون مسؤول نظام لبيئة Commerce.</span><span class="sxs-lookup"><span data-stu-id="49422-135">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="49422-136">في جزء التنقل الأيسر، حدد **إعدادات المستأجر** لتوسيعه.</span><span class="sxs-lookup"><span data-stu-id="49422-136">In the left navigation pane, select **Tenant Settings** to expand it.</span></span>
1. <span data-ttu-id="49422-137">حدد **إعدادات B2C**، ثم حدد **إدارة**.</span><span class="sxs-lookup"><span data-stu-id="49422-137">Select **B2C Settings**, and then select **Manage**.</span></span>
1. <span data-ttu-id="49422-138">حدد **إضافة تطبيق B2C**، ثم أدخل المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="49422-138">Select **Add B2C Application**, and then enter the following information:</span></span>

    - <span data-ttu-id="49422-139">**اسم التطبيق**: أدخل الاسم الذي ينبغي استخدامه للتطبيق في سياق إدارته في Commerce.</span><span class="sxs-lookup"><span data-stu-id="49422-139">**Application Name**: Enter the name that should be used for the application in the context of managing it in Commerce.</span></span> <span data-ttu-id="49422-140">نوصي باستخدام اسم التطبيق الذي اخترته عند إعداد تطبيق Azure AD B2C في مدخل Azure.</span><span class="sxs-lookup"><span data-stu-id="49422-140">We recommend that you use the application name that you chose when you set up the Azure AD B2C application in the Azure portal.</span></span> <span data-ttu-id="49422-141">وبهذه الطريقة، يمكنك المساعدة على تقليل الالتباس عند إدارة مستأجري B2C في Commerce.</span><span class="sxs-lookup"><span data-stu-id="49422-141">In this way, you can help reduce confusion when you manage B2C tenants in Commerce.</span></span>
    - <span data-ttu-id="49422-142">**اسم المستأجر**: أدخل اسم مستأجر B2C كما يظهر في مدخل Azure.</span><span class="sxs-lookup"><span data-stu-id="49422-142">**Tenant Name**: Enter the B2C tenant name as it appears in the Azure portal.</span></span>
    - <span data-ttu-id="49422-143">**معرف سياسة نسيان كلمة المرور**: أدخل معرف السياسة (اسم السياسة في مدخل Azure).</span><span class="sxs-lookup"><span data-stu-id="49422-143">**Forget Password Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>
    - <span data-ttu-id="49422-144">**معرف سياسة التسجيل وتسجيل الدخول**: أدخل معرف السياسة (اسم السياسة في مدخل Azure).</span><span class="sxs-lookup"><span data-stu-id="49422-144">**Signup Signin Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>
    - <span data-ttu-id="49422-145">**GUID‎ العميل**: أدخل معرف مستأجر Azure AD B2C كما يظهر في مدخل Azure (وليس معرف التطبيق لمستأجر B2C).</span><span class="sxs-lookup"><span data-stu-id="49422-145">**Client GUID**: Enter the Azure AD B2C tenant ID as it appears in the Azure portal (not the application ID for the B2C tenant).</span></span>
    - <span data-ttu-id="49422-146">**تحرير معرف سياسة ملف التعريف**: أدخل معرف السياسة (اسم السياسة في مدخل Azure).</span><span class="sxs-lookup"><span data-stu-id="49422-146">**Edit Profile Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>

1. <span data-ttu-id="49422-147">عند الانتهاء من إدخال هذه المعلومات، حدد **موافق** لحفظ التغييرات.</span><span class="sxs-lookup"><span data-stu-id="49422-147">When you've finished entering this information, select **OK** to save your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="49422-148">يجب ترك حقول مثل **النطاق**، و **معرف السياسة غير التفاعلية**، و **معرف العميل غير التفاعلي**، و **المجال المخصص لتسجيل الدخول**، و **معرف سياسة التسجيل** فارغة إلا إذا طلب منك فريق Dynamics 365 Commerce تعيينها.</span><span class="sxs-lookup"><span data-stu-id="49422-148">You should leave fields such as **Scope**, **Non Interactive Policy ID**, **Non Interactive Client ID**, **Login Custom Domain**, and **Sign Up Policy ID** blank unless the Dynamics 365 Commerce team instructs you to set them.</span></span>
<span data-ttu-id="49422-149">يجب أن يظهر مستأجر Azure AD B2C الجديد في القائمة ضمن **إدارة تطبيقات B2C**.</span><span class="sxs-lookup"><span data-stu-id="49422-149">Your new Azure AD B2C tenant should now appear in the list under **Manage B2C Applications**.</span></span>

### <a name="manage-or-delete-an-azure-ad-b2c-tenant"></a><span data-ttu-id="49422-150">إدارة مستأجر Azure AD B2C أو حذفه</span><span class="sxs-lookup"><span data-stu-id="49422-150">Manage or delete an Azure AD B2C tenant</span></span>

1. <span data-ttu-id="49422-151">قم بتسجيل الدخول إلى منشئ موقع Commerce لبيئتك كمسؤول نظام. لتكوين مستأجري Azure AD B2C، يجب أن تكون مسؤول نظام لبيئة Commerce.</span><span class="sxs-lookup"><span data-stu-id="49422-151">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="49422-152">في جزء التنقل الأيسر، حدد **إعدادات المستأجر** لتوسيعه.</span><span class="sxs-lookup"><span data-stu-id="49422-152">In the left navigation pane, select **Tenant Settings** to expand it.</span></span>
1. <span data-ttu-id="49422-153">حدد **إعدادات B2C**، ثم حدد **إدارة**.</span><span class="sxs-lookup"><span data-stu-id="49422-153">Select **B2C Settings**, and then select **Manage**.</span></span>
1. <span data-ttu-id="49422-154">لتحرير مستأجر B2C، حدد رمز قلم الرصاص المجاور له.</span><span class="sxs-lookup"><span data-stu-id="49422-154">To edit a B2C tenant, select the pencil symbol next to it.</span></span> <span data-ttu-id="49422-155">لحذف مستأجر B2C، حدد رمز سلة المهملات المجاور له.</span><span class="sxs-lookup"><span data-stu-id="49422-155">To delete a B2C tenant, select the trash can symbol next to it.</span></span>
1. <span data-ttu-id="49422-156">حدد **حفظ**، ثم حدد **نشر** لتنشيط التغييرات.</span><span class="sxs-lookup"><span data-stu-id="49422-156">Select **Save**, and then select **Publish** to activate your changes.</span></span>

> [!WARNING]
> <span data-ttu-id="49422-157">عند تكوين مستأجر B2C لموقع مباشر/منشور، ربما قام المستخدمون بالتسجيل باستخدام الحسابات الموجودة على المستأجر.</span><span class="sxs-lookup"><span data-stu-id="49422-157">When a B2C tenant is configured for a live/published site, users might have signed up by using accounts that are present on the tenant.</span></span> <span data-ttu-id="49422-158">إذا حذفت مستأجر تم تكوينه في قائمة **إعدادات مستأجر \> B2C**، فأنت تقوم بإزالة اقتران مستأجر B2C هذا من المواقع المقترنة بأي قنوات للمستأجر.</span><span class="sxs-lookup"><span data-stu-id="49422-158">If you delete a configured tenant on the **Tenant Settings \> B2C Tenant** menu, you remove the association of that B2C tenant from sites that are associated with any channels of the tenant.</span></span> <span data-ttu-id="49422-159">في هذه الحالة، قد يتعذر على المستخدمين لديك تسجيل الدخول إلى حساباتهم.</span><span class="sxs-lookup"><span data-stu-id="49422-159">In this case, your users might no longer be able to sign in to their accounts.</span></span> <span data-ttu-id="49422-160">لذلك، توخى الانتباه الشديد عند حذف مستأجر تم تكوينه.</span><span class="sxs-lookup"><span data-stu-id="49422-160">Therefore, use extreme caution when you delete a configured tenant.</span></span>
>
> <span data-ttu-id="49422-161">عند حذف مستأجر تم تكوينه، سيستمر الاحتفاظ بمستأجر B2C والسجلات، ولكن سيتم تغيير تكوين نظام Commerce لذلك المستأجر أو إزالته.</span><span class="sxs-lookup"><span data-stu-id="49422-161">When a configured tenant is deleted, the B2C tenant and records will continue to be maintained, but the Commerce system configuration of that tenant will be changed or removed.</span></span> <span data-ttu-id="49422-162">سيقوم المستخدمون الذين يحاولون التسجيل في الموقع أو تسجيل الدخول إليه بإنشاء سجل حساب جديد في مستأجر B2C الافتراضي أو المقترن حديثًا والذي تم تكوينه لقناة الموقع.</span><span class="sxs-lookup"><span data-stu-id="49422-162">Users who try to sign up or sign in to the site will create a new account record in the default or newly associated B2C tenant that is configured for the channel of the site.</span></span>
## <a name="configure-your-channel-with-a-b2c-tenant"></a><span data-ttu-id="49422-163">تكوين قناتك مع مستأجر B2C</span><span class="sxs-lookup"><span data-stu-id="49422-163">Configure your channel with a B2C tenant</span></span>

1. <span data-ttu-id="49422-164">قم بتسجيل الدخول إلى منشئ موقع Commerce لبيئتك كمسؤول نظام. لتكوين مستأجري Azure AD B2C، يجب أن تكون مسؤول نظام لبيئة Commerce.</span><span class="sxs-lookup"><span data-stu-id="49422-164">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="49422-165">في جزء التنقل الأيسر، حدد **إعدادات الموقع** لتوسيعه.</span><span class="sxs-lookup"><span data-stu-id="49422-165">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="49422-166">حدد **القنوات**، ثم حدد القناة المطلوب تكوينها.</span><span class="sxs-lookup"><span data-stu-id="49422-166">Select **Channels**, and then select the channel to configure.</span></span>
1. <span data-ttu-id="49422-167">في جزء الخصائص الموجود على اليمين، في الحقل **تحديد تطبيق B2C**، حدد مستأجر Azure AD B2C الذي تم تكوينه لاستخدامه في هذه القناة.</span><span class="sxs-lookup"><span data-stu-id="49422-167">In the properties pane on the right, in the **Select B2C Application** field, select the configured Azure AD B2C tenant to use for this channel.</span></span>
1. <span data-ttu-id="49422-168">في شريط الأوامر ، حدد **حفظ ونشر** للالتزام بالتكوين الجديد أو المحدث.</span><span class="sxs-lookup"><span data-stu-id="49422-168">On the command bar, select **Save and Publish** to commit the new or updated configuration.</span></span>

> [!WARNING]
> <span data-ttu-id="49422-169">إذا قمت بتغيير تطبيق B2C الذي تم تعيينه للقناة، فإنك تقوم بإزالة المراجع الحالية التي تم تأسيسها لأي مستخدمين قاموا بالتسجيل في البيئة.</span><span class="sxs-lookup"><span data-stu-id="49422-169">If you change the B2C application that is assigned to the channel, you remove the current references that have been established for any users who have already signed up in the environment.</span></span> <span data-ttu-id="49422-170">في هذه الحالة، لن تتوفر أي بيانات اعتماد مقترنة بتطبيق B2C المعين حاليًا للمستخدمين.</span><span class="sxs-lookup"><span data-stu-id="49422-170">In this case, any credentials that are associated with the currently assigned B2C application won't be available to users.</span></span> <span data-ttu-id="49422-171">لذلك، قم بتغيير تكوين قناة Azure AD B2C فقط إذا كنت تقوم بإعداد القناة لأول مرة، ولم يتمكن أي مستخدم من التسجيل.</span><span class="sxs-lookup"><span data-stu-id="49422-171">Therefore, change a channel Azure AD B2C configuration only if you're setting up the channel for the first time, and no users have been able to sign up.</span></span> <span data-ttu-id="49422-172">وإلا، فقد يضطر المستخدمون إلى التسجيل مرة أخرى لتأسيس سجل في مستأجر Azure AD B2C الجديد.</span><span class="sxs-lookup"><span data-stu-id="49422-172">Otherwise, users might have to sign up again to establish a record in the new Azure AD B2C tenant.</span></span>
## <a name="additional-resources"></a><span data-ttu-id="49422-173">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="49422-173">Additional resources</span></span>

[<span data-ttu-id="49422-174">تكوين اسم مجالك</span><span class="sxs-lookup"><span data-stu-id="49422-174">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="49422-175">نشر مستأجر التجارة الإلكترونية الجديد</span><span class="sxs-lookup"><span data-stu-id="49422-175">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="49422-176">إنشاء موقع تجارة إلكترونية</span><span class="sxs-lookup"><span data-stu-id="49422-176">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="49422-177">إقران موقع Dynamics 365 Commerce بقناة عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="49422-177">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="49422-178">إدارة ملفات robots.txt</span><span class="sxs-lookup"><span data-stu-id="49422-178">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="49422-179">تحميل عناوين URL لإعادة التوجيه‬ بشكل مجمع</span><span class="sxs-lookup"><span data-stu-id="49422-179">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="49422-180">إعداد مستأجر B2C في Commerce</span><span class="sxs-lookup"><span data-stu-id="49422-180">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="49422-181">إعداد صفحات مخصصة لعمليات تسجيل دخول المستخدمين</span><span class="sxs-lookup"><span data-stu-id="49422-181">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="49422-182">إضافة الدعم إلى شبكة تسليم المحتوى (CDN)</span><span class="sxs-lookup"><span data-stu-id="49422-182">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="49422-183">تمكين اكتشاف المتجر استنادًا إلى الموقع</span><span class="sxs-lookup"><span data-stu-id="49422-183">Enable location-based store detection</span></span>](enable-store-detection.md)
