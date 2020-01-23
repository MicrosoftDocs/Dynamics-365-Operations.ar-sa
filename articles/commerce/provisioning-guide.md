---
title: توفير بيئة معاينة Commerce
description: يشرح هذا الموضوع كيفية توفير بيئة معاينة Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b77d2cbbc100aeae5dcd53ddbe69ff2e4435da13
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934738"
---
# <a name="provision-a-commerce-preview-environment"></a><span data-ttu-id="5a7cf-103">توفير بيئة معاينة Commerce</span><span class="sxs-lookup"><span data-stu-id="5a7cf-103">Provision a Commerce preview environment</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="5a7cf-104">يشرح هذا الموضوع كيفية توفير بيئة معاينة Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce preview environment.</span></span>

<span data-ttu-id="5a7cf-105">قبل البدء ، نوصي بأن تتصفح هذا الموضوع بالكامل على الأقل للحصول على فكرة عما تستلزمه العملية وما يتضمنه هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-105">Before you begin, we recommend that you at least skim through this whole topic to get an idea of what the process entails and what this topic contains.</span></span>

> [!NOTE]
> <span data-ttu-id="5a7cf-106">إذا لم يتم منحك إلى الآن حق الوصول إلى معاينة Dynamics 365 Commerce فيمكنك طلب الوصول إلى المعاينة من [موقع Commerce](https://aka.ms/Dynamics365CommerceWebsite).</span><span class="sxs-lookup"><span data-stu-id="5a7cf-106">If you haven't yet been granted access to the Dynamics 365 Commerce preview, you can request preview access from the [Commerce website](https://aka.ms/Dynamics365CommerceWebsite).</span></span>

## <a name="overview"></a><span data-ttu-id="5a7cf-107">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="5a7cf-107">Overview</span></span>

<span data-ttu-id="5a7cf-108">لتوفير بيئة معاينة Commerce بنجاح، يجب عليك إنشاء مشروع له اسم منتج محدد ونوع معين.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-108">To successfully provision your Commerce preview environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="5a7cf-109">لدي البيئة و Retail Cloud Scale Unit (RCSU) بعض المعلمات المحددة التي يتعين عليك استخدامها لتوفير التجارة الإلكترونية في وقت لاحق.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-109">The environment and Retail Cloud Scale Unit (RCSU) also have some specific parameters that you must use when you provision e-Commerce later.</span></span> <span data-ttu-id="5a7cf-110">تصف الإرشادات الواردة في هذا الموضوع كافة الخطوات المطلوبة التي يجب عليك إكمالها والمعلمات التي يجب استخدامها.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-110">The instructions in this topic describe all the required steps that you must complete and the parameters that you must use.</span></span>

<span data-ttu-id="5a7cf-111">بعد نجاحك في توفير بيئة معاينة Commerce، يجب عليك إكمال بعض الخطوات التالية للتوفير التي يجب اتخاذها لإعداد البيئة.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-111">After you successfully provision your Commerce preview environment, you must complete a few post-provisioning steps to prepare it.</span></span> <span data-ttu-id="5a7cf-112">بعض الخطوات تكون اختيارية، بناءً على أوجه النظام التي ترغب في تقييمها.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="5a7cf-113">يمكنك دائمًا إكمال الخطوات الاختيارية لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="5a7cf-114">للحصول علي معلومات حول كيفية تكوين بيئة معاينة Commerce بعد توفيرها، راجع [ تكوين بيئة معاينة Commerce](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="5a7cf-114">For information about how to configure your Commerce preview environment after you provision it, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="5a7cf-115">للحصول علي معلومات حول كيفية تكوين الميزات الاختيارية لبيئة معاينة Commerce، راجع [تكوين الميزات الاختيارية لبيئة معاينة Commerce](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="5a7cf-115">For information about how to configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

<span data-ttu-id="5a7cf-116">إذا كان لديك أية أسئلة تتعلق بخطوات التوفير أو كنت تواجه أية مشكلات، يرجى إعلام Microsoft على [مجموعة Microsoft Dynamics 365 Commerce Preview Yammer](https://aka.ms/Dynamics365CommercePreviewYammer).</span><span class="sxs-lookup"><span data-stu-id="5a7cf-116">If you have any questions about the provisioning steps, or if you encounter any issues, let Microsoft know in the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5a7cf-117">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="5a7cf-117">Prerequisites</span></span>

<span data-ttu-id="5a7cf-118">يجب تتوفر المتطلبات الأساسية التالية قبل توفير بيئة معاينة Commerce الخاصة بك:</span><span class="sxs-lookup"><span data-stu-id="5a7cf-118">The following prerequisites must be in place before you can provision your Commerce preview environment:</span></span>

- <span data-ttu-id="5a7cf-119">يمكنك الوصول إلى مدخل Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="5a7cf-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="5a7cf-120">لقد تم قبولك في برنامج Dynamics 365 Commerce Preview.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-120">You've been accepted into the Dynamics 365 Commerce Preview program.</span></span>
- <span data-ttu-id="5a7cf-121">لديك الأذونات المطلوبة لإنشاء مشروع لـ **‏‫عمليات ما قبل البيع المتوقعة‬** أو **‏‫الترحيل وإنشاء الحلول وتعلم ‬**</span><span class="sxs-lookup"><span data-stu-id="5a7cf-121">You have the required permissions to create a project for **Prospective presales** or **Migrate, create solutions, and learn**.</span></span>
- <span data-ttu-id="5a7cf-122">أنت عضو في **‏‫مدير البيئة‬** أو دور **مالك المشروع** في المشروع الذي ستوفر فيه البيئة.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-122">You're a member of the **Environment manager** or **Project owner** role in the project where you will provision the environment.</span></span>
- <span data-ttu-id="5a7cf-123">لديك حق وصول المسؤول إلى اشتراك Microsoft Azure الخاص بك، أو اتصل بمسؤول الاشتراك والذي يمكنه إكمال الخطوتين اللتين تتطلبان أذونات المسؤول نيابة عنك.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-123">You have admin access to your Microsoft Azure subscription, or you're in contact with a subscription admin who can complete the two steps that require admin permissions on your behalf.</span></span>
- <span data-ttu-id="5a7cf-124">يتوفر لديك معرف مستأجر Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="5a7cf-124">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="5a7cf-125">لقد قمت بإنشاء مجموعة أمان Azure AD لاستخدامها كـ مجموعة مسؤولي نظام التجارة الإلكترونية ويتوفر لديك معرف لها.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-125">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="5a7cf-126">لقد قمت بإنشاء مجموعة أمان Azure AD لاستخدامها كمجموعة المشرفين على التقييمات والمراجعات ويتوفر لديك معرف لها.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-126">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="5a7cf-127">(يمكن أن تكون مجموعة الأمان هذه هي نفس مجموعة مسؤولي نظام التجارة الإلكترونية.)</span><span class="sxs-lookup"><span data-stu-id="5a7cf-127">(This security group can be the same as the e-Commerce system admin group.)</span></span>

### <a name="find-your-azure-ad-tenant-id"></a><span data-ttu-id="5a7cf-128">كيفية العثور علي معرف مستأجر Azure AD الخاص بك</span><span class="sxs-lookup"><span data-stu-id="5a7cf-128">Find your Azure AD tenant ID</span></span>

<span data-ttu-id="5a7cf-129">معرف مستأجر Azure AD الخاص بك هو معرف فريد عمومي (GUID) يشبه هذا المثال: **72f988bf-86f1-41af-91ab-2d7cd011db47**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-129">Your Azure AD tenant ID is a globally unique identifier (GUID) that resembles this example: **72f988bf-86f1-41af-91ab-2d7cd011db47**.</span></span>

#### <a name="find-your-azure-ad-tenant-id-by-using-the-azure-portal"></a><span data-ttu-id="5a7cf-130">كيفية العثور على معرف مستأجر Azure AD الخاص بك باستخدام مدخل Azure</span><span class="sxs-lookup"><span data-stu-id="5a7cf-130">Find your Azure AD tenant ID by using the Azure portal</span></span>

1. <span data-ttu-id="5a7cf-131">سجل الدخول إلى [مدخل Azure ](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="5a7cf-131">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="5a7cf-132">تأكد من أنك قمت بتحديد الدليل الصحيح.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-132">Make sure that the correct directory is selected.</span></span>
1. <span data-ttu-id="5a7cf-133">في القائمة اليمنى، حدد **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-133">On the menu on the left, select **Azure Active Directory**.</span></span>
1. <span data-ttu-id="5a7cf-134">اختر **الخصائص** ضمن **إدارة**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-134">Under **Manage**, select **Properties**.</span></span> <span data-ttu-id="5a7cf-135">يظهر معرف مستأجر Azure AD الخاص بك ضمن **معرف الدليل**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-135">Your Azure AD tenant ID appears under **Directory ID**.</span></span>

#### <a name="find-your-azure-ad-tenant-id-by-using-openid-connect-metadata"></a><span data-ttu-id="5a7cf-136">كيفية العثور على معرف مستأجر Azure AD الخاص بك باستخدام بيانات تعريف OpenID Connect</span><span class="sxs-lookup"><span data-stu-id="5a7cf-136">Find your Azure AD tenant ID by using OpenID Connect metadata</span></span>

<span data-ttu-id="5a7cf-137">قم بإنشاء عنوان URL لـ OpenID عن طريق استبدال **\{YOUR\_DOMAIN\}** بالمجال الخاص بك، مثل `microsoft.com`.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-137">Create an OpenID URL by replacing **\{YOUR\_DOMAIN\}** with your domain, such as `microsoft.com`.</span></span> <span data-ttu-id="5a7cf-138">على سبيل المثال، `https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration` سيصبح `https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration`.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-138">For example, `https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration` will become `https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration`.</span></span>

1. <span data-ttu-id="5a7cf-139">انتقل إلى عنوان URL لـ OpenID الذي يحتوي على المجال الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-139">Go to the OpenID URL that contains your domain.</span></span>

    <span data-ttu-id="5a7cf-140">يمكن العثور على معرف مستأجر Azure AD في قيم خصائص متعددة.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-140">You can find you Azure AD tenant ID in multiple property values.</span></span>

1. <span data-ttu-id="5a7cf-141">ابحث عن **authorization\_endpoint** ثم استخرج GUID الذي يظهر مباشرة بعد `login.microsoftonline.com/`.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-141">Find **authorization\_endpoint**, and extract the GUID that appears immediately after `login.microsoftonline.com/`.</span></span>

### <a name="find-your-azure-ad-security-group-id"></a><span data-ttu-id="5a7cf-142">كيفية العثور على معرف مجموعة أمان Azure AD الخاصة بك</span><span class="sxs-lookup"><span data-stu-id="5a7cf-142">Find your Azure AD security group ID</span></span>

<span data-ttu-id="5a7cf-143">معرف مجموعة أمان Azure AD الخاصة بك هو GUID يشبه المثال التالي: **436ea7f5-ee6c-40c1-9f08-825c5811066a**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-143">The ID of your Azure AD security group is a GUID that resembles this example: **436ea7f5-ee6c-40c1-9f08-825c5811066a**.</span></span>

<span data-ttu-id="5a7cf-144">يفترض هذا الإجراء أن تكون عضوًا في المجموعة التي تحاول العثور على المعرف لها.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-144">This procedure assumes that you're a member of the group that you're trying to find the ID for.</span></span>

1. <span data-ttu-id="5a7cf-145">افتح [مستكشف الرسومات البيانية](https://developer.microsoft.com/graph/graph-explorer#).</span><span class="sxs-lookup"><span data-stu-id="5a7cf-145">Open the [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer#).</span></span>
1. <span data-ttu-id="5a7cf-146">حدد **تسجيل الدخول باستخدام Microsoft** وسجل الدخول باستخدام بيانات اعتمادك.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-146">Select **Sign In with Microsoft**, and sign in by using your credentials.</span></span>
1. <span data-ttu-id="5a7cf-147">على اليمين ، حدد **إظهار مزيد من العينات**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-147">On the left, select **show more samples**.</span></span>
1. <span data-ttu-id="5a7cf-148">قم بتمكين **المجموعات** من الجزء الأيسر.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-148">In the right pane, enable **Groups**.</span></span>
1. <span data-ttu-id="5a7cf-149">أغلق الجزء الأيسر.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-149">Close the right pane.</span></span>
1. <span data-ttu-id="5a7cf-150">حدد **جميع المجموعات التي أننتمي إليها**</span><span class="sxs-lookup"><span data-stu-id="5a7cf-150">Select **all groups I belong to**.</span></span>
1. <span data-ttu-id="5a7cf-151">في حقل **معاينة الاستجابة‬‏‫**، ابحث عن مجموعتك.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-151">In the **Response Preview** field, find your group.</span></span> <span data-ttu-id="5a7cf-152">يظهر معرف مجموعة الأمان ضمن خاصية **المعرف**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-152">The security group ID appears under the **id** property.</span></span>

## <a name="provision-your-commerce-preview-environment"></a><span data-ttu-id="5a7cf-153">توفير بيئة معاينة Commerce الخاصة بك</span><span class="sxs-lookup"><span data-stu-id="5a7cf-153">Provision your Commerce preview environment</span></span>

<span data-ttu-id="5a7cf-154">توضح هذه الإجراءات كيفية توفير بيئة معاينة Commerce.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-154">These procedures explain how to provision a Commerce preview environment.</span></span> <span data-ttu-id="5a7cf-155">بعد إكمالها بنجاح، ستكون بيئة معاينة Commerce جاهزة للتكوين.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-155">After you successfully complete them, the Commerce preview environment will be ready for configuration.</span></span> <span data-ttu-id="5a7cf-156">ويتم إجراء كافة الأنشطة الموضحة هنا في مدخل LCS.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-156">All the activities that are described here occur in the LCS portal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5a7cf-157">يتم ربط الوصول إلى المعاينة إلى حساب LCS والمؤسسة التي قمت بتحديدها في تطبيق المعاينة الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-157">Preview access is tied to the LCS account and organization that you specified in your preview application.</span></span> <span data-ttu-id="5a7cf-158">يجب استخدام نفس الحساب لتوفير بيئة معاينة Commerce.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-158">You must use the same account to provision the Commerce preview environment.</span></span> <span data-ttu-id="5a7cf-159">إذا كان يتعين عليك استخدام حساب LCS مختلف أو مستاجر لبيئة معاينة Commerce، يجب تقديم هذه التفاصيل إلى Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-159">If you must use a different LCS account or tenant for the Commerce preview environment, you must provide those details to Microsoft.</span></span> <span data-ttu-id="5a7cf-160">للحصول على معلومات جهة الاتصال، راجع قسم [دعم بيئة معاينة Commerce](#commerce-preview-environment-support) لاحقًا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-160">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section later in this topic.</span></span>

### <a name="grant-access-to-e-commerce-applications"></a><span data-ttu-id="5a7cf-161">منح الوصول إلى تطبيقات التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="5a7cf-161">Grant access to e-Commerce applications</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5a7cf-162">يجب أن يكون الشخص الذي سجل دخوله مسؤول مستأجر Azure AD لديه معرف مستاجر Azure AD.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-162">The person who signs in must be an Azure AD tenant admin who has the Azure AD tenant ID.</span></span> <span data-ttu-id="5a7cf-163">إذا لم تكتمل هذه الخطوة بنجاح، فستفشل خطوات التوفير المتبقية.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-163">If this step isn't successfully completed, the remaining provisioning steps will fail.</span></span>

<span data-ttu-id="5a7cf-164">لتخويل تطبيقات التجارة الإلكترونية للوصول إلى اشتراك Azure اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-164">To authorize e-Commerce applications to access your Azure subscription, follow these steps.</span></span>

1. <span data-ttu-id="5a7cf-165">تجميع عنوان URL بالتنسيق التالي:</span><span class="sxs-lookup"><span data-stu-id="5a7cf-165">Assemble a URL in the following format:</span></span>

    `https://login.windows.net/{AAD_TENANT_ID}/oauth2/authorize?client_id=fbcbf727-cd18-4422-a723-f8274075331a&response_type=code&redirect_uri=https://sb.manage.commerce.dynamics.com/_commerce/Consent&response_mode=query&prompt=admin_consent&state=12345`

1. <span data-ttu-id="5a7cf-166">انسخ والصق عنوان URL في المتصفح أو محرر النصوص، واستبدل **\{AAD\_TENANT\_ID\}** بمعرف مستأجر Azure AD لديك.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-166">Copy and paste the URL into your browser or text editor, and replace **\{AAD\_TENANT\_ID\}** with your Azure AD tenant ID.</span></span> <span data-ttu-id="5a7cf-167">ثم افتح عنوان URL.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-167">Then open the URL.</span></span>
1. <span data-ttu-id="5a7cf-168">في مربع حوار تسجيل الدخول إلى Azure AD، قم بتسجيل الدخول، وتأكد من أنك تريد منح **Dynamics 365 Commerce (معاينة)** حق الوصول إلى اشتراكك.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-168">In the Azure AD sign-in dialog box, sign in, and confirm that you want to grant **Dynamics 365 Commerce (Preview)** access to your subscription.</span></span> <span data-ttu-id="5a7cf-169">سيُعاد توجيهك إلى صفحة تؤكد ما إذا كانت العملية قد اكتملت بنجاح أم لا.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-169">You're redirected to a page that indicates whether the operation was successful.</span></span>

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a><span data-ttu-id="5a7cf-170">التأكد من توفير ميزات المعاينة وتمكينها في LCS</span><span class="sxs-lookup"><span data-stu-id="5a7cf-170">Confirm that preview features are available and turned on in LCS</span></span>

<span data-ttu-id="5a7cf-171">للتأكد من توفير ميزات المعاينة وتمكينها في LCS، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-171">To confirm that preview features are available and turned on in LCS, follow these steps.</span></span>

1. <span data-ttu-id="5a7cf-172">قم بتسجيل الدخول إلى [بوابة LCS](https://lcs.dynamics.com) باستخدام نفس حساب LCS الذي استخدمته لطلب الوصول إلى المعاينة.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-172">Sign in to the [LCS portal](https://lcs.dynamics.com) by using the same LCS account that you used to request access to the preview.</span></span>
1. <span data-ttu-id="5a7cf-173">في صفحة LCS الرئيسية، قم بالتمرير أقصى اليمين ثم انقر فوق اللوحة **‏‫إدارة ميزات المعاينة‬**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-173">On the LCS home page, scroll all the way to the right, and select the **Preview feature management** tile.</span></span>

    ![لوحة إدارة المعاينة](./media/preview1.png)

1. <span data-ttu-id="5a7cf-175">قم بالتمرير لأسفل إلى **ميزات المعاينة الخاصة** وتأكد من توفر الميزات التالية وتمكينها:</span><span class="sxs-lookup"><span data-stu-id="5a7cf-175">Scroll down to **Private preview features**, and confirm that the following features are available and turned on:</span></span>

    - <span data-ttu-id="5a7cf-176">تقييم التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="5a7cf-176">e-Commerce Evaluation</span></span>
    - <span data-ttu-id="5a7cf-177">بيئات برنامج Commerce Preview</span><span class="sxs-lookup"><span data-stu-id="5a7cf-177">Commerce Preview Program Environments</span></span>

    ![ميزات المعاينة الخاصة](./media/preview2.png)

1. <span data-ttu-id="5a7cf-179">إذا لم تظهر هذه الميزات في القائمة، فاتصل بـ Microsoft ، وقم بتوفير عنوان البريد الكتروني للعمل وحساب LCS وتفاصيل المستأجر.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-179">If those features don't appear in the list, contact Microsoft, and provide your work email address, LCS account, and tenant details.</span></span> <span data-ttu-id="5a7cf-180">للحصول على معلومات جهة الاتصال، راجع قسم [دعم بيئة معاينة Commerce](#commerce-preview-environment-support).</span><span class="sxs-lookup"><span data-stu-id="5a7cf-180">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="5a7cf-181">إنشاء مشروع جديد</span><span class="sxs-lookup"><span data-stu-id="5a7cf-181">Create a new project</span></span>

<span data-ttu-id="5a7cf-182">لإنشاء مشروع جديد في LCS، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="5a7cf-182">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="5a7cf-183">في صفحة LCS الرئيسية، حدد علامة الجمع (**+**) لإنشاء مشروع.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-183">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="5a7cf-184">في الجزء الأيسر، اتبع أحدي الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="5a7cf-184">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="5a7cf-185">إذا كنت شريكا، فحدد **‏‫الترحيل وإنشاء الحلول وتعلم ‬**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-185">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="5a7cf-186">إذا كنت عميلاً، فحدد **‏‫عمليات ما قبل البيع المتوقعة‬**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-186">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="5a7cf-187">أدخل الاسم والوصف والصناعة.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-187">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="5a7cf-188">في حقل **اسم المنتج**، حدد **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-188">In the **Product name** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="5a7cf-189">في حقل **إصدار المنتج**، حدد **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-189">In the **Product version** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="5a7cf-190">في حقل **المنهجية**، حدد **منهجية تنفيذ Dynamics Retail**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-190">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="5a7cf-191">اختياري: يمكنك استيراد الأدوار والمستخدمين من مشروع موجود.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-191">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="5a7cf-192">حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-192">Select **Create**.</span></span> <span data-ttu-id="5a7cf-193">تظهر طريقة عرض المشروع.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-193">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="5a7cf-194">إضافة موصل Azure</span><span class="sxs-lookup"><span data-stu-id="5a7cf-194">Add the Azure Connector</span></span>

<span data-ttu-id="5a7cf-195">لإضافة موصل Azure إلى مشروع LCS، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-195">To add the Azure Connector to your LCS project, follow these steps.</span></span>

1. <span data-ttu-id="5a7cf-196">اتبع إحدى الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="5a7cf-196">Follow one of these steps:</span></span>

    - <span data-ttu-id="5a7cf-197">إذا كنت شريكًا، فحدد اللوحة **إعدادات المشروع** في أقصي اليمين.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-197">If you're a partner, select the **Project settings** tile on the far right.</span></span>
    - <span data-ttu-id="5a7cf-198">إذا كنت عميلاً، فاختر **إعدادات المشروع** من القائمة العليا.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-198">If you're a customer, select **Project settings** on the top menu.</span></span>

1. <span data-ttu-id="5a7cf-199">حدد **موصل‬ات Azure**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-199">Select **Azure connectors**.</span></span>
1. <span data-ttu-id="5a7cf-200">حدد **+ إضافة** لإضافة موصل Azure.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-200">Select **Add** to add the Azure Connector.</span></span>
1. <span data-ttu-id="5a7cf-201">أدخل اسمًا.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-201">Enter a name.</span></span>
1. <span data-ttu-id="5a7cf-202">أدخل معرف اشتراك Azure الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-202">Enter your Azure subscription ID.</span></span>
1. <span data-ttu-id="5a7cf-203">قم بتشغيل خيار **التكوين لاستخدام مدير موارد Azure ‏(ARM)**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-203">Turn on the **Configure to use Azure Resource Manager (ARM)** option.</span></span>
1. <span data-ttu-id="5a7cf-204">تحقق من أن قيمة **‏‫مجال مستأجر AAD لاشتراك Azure (أو المعرف)‬** صحيحة.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-204">Verify that the **Azure subscription AAD Tenant Domain (or ID)** value is correct.</span></span> <span data-ttu-id="5a7cf-205">راجع مسؤول الاشتراك في Azure، عند الضرورة.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-205">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="5a7cf-206">حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-206">Select **Next**.</span></span>
1. <span data-ttu-id="5a7cf-207">اتبع الإرشادات على الصفحة لمنح التطبيقات المطلوب حق الوصول إلى الاشتراك الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-207">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="5a7cf-208">راجع مسؤول الاشتراك في Azure، عند الضرورة.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-208">Consult your Azure subscription admin as required.</span></span>

    1. <span data-ttu-id="5a7cf-209">سجل الدخول إلى [مدخل Azure ](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="5a7cf-209">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
    1. <span data-ttu-id="5a7cf-210">تأكد من تحديد الدليل الصحيح، ثم من القائمة على اليسار ، حدد **الاشتراكات**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-210">Make sure that the correct directory is selected, and then, on the menu on the left, select **Subscriptions**.</span></span>
    1. <span data-ttu-id="5a7cf-211">اعثر على موقع الاشتراك الصحيح من القائمة وحدده.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-211">Find the correct subscription in the list, and select it.</span></span> <span data-ttu-id="5a7cf-212">استخدم وظيفة البحث كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-212">Use the search functionality as required.</span></span>
    1. <span data-ttu-id="5a7cf-213">في القائمة، حدد **التحكم في الوصول (IAM)**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-213">On the menu, select **Access control (IAM)**.</span></span>
    1. <span data-ttu-id="5a7cf-214">حدد**إضافة** أسفل **إضافة تعيين دور** على الجانب الأيسر.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-214">On the right, under **Add a role assignment**, select **Add**.</span></span> <span data-ttu-id="5a7cf-215">يظهر جزء **إضافة تعيين دور**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-215">The **Add role assignment** pane appears.</span></span>
    1. <span data-ttu-id="5a7cf-216">في حقل **الدور**، حدد **المساهم**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-216">In the **Role** field, select **Contributor**.</span></span>
    1. <span data-ttu-id="5a7cf-217">في حقل **تعيين حق الوصول إلى**، اترك القيمة الافتراضية، أو مستخدم **Azure AD أو المجموعة أو كيان الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-217">In the **Assign access to** field, leave the default value, **Azure AD user, group, or service principal**.</span></span>
    1. <span data-ttu-id="5a7cf-218">ضمن **تحديد**، أدخل **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-218">Under **Select**, enter **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span></span>
    1. <span data-ttu-id="5a7cf-219">حدد **خدمات نشر Dynamics \[تمكين wsfed\]** من القائمة.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-219">Select **Dynamics Deployment Services \[wsfed-enabled\]** in the list.</span></span>
    1. <span data-ttu-id="5a7cf-220">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-220">Select **Save**.</span></span>

1. <span data-ttu-id="5a7cf-221">حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-221">Select **Next**.</span></span>
1. <span data-ttu-id="5a7cf-222">اتبع الإرشادات على الصفحة لمنح التطبيقات المطلوب حق الوصول إلى الاشتراك الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-222">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="5a7cf-223">راجع مسؤول الاشتراك في Azure، عند الضرورة.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-223">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="5a7cf-224">حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-224">Select **Next**.</span></span>
1. <span data-ttu-id="5a7cf-225">في حقل **منطقة Azure**، اختر إما **‏‫شرق الولايات المتحدة‬**، أو **‏‫شرق الولايات المتحدة‬ 2**، أو **‏‫غرب الولايات المتحدة‬** أو **‏‫غرب الولايات المتحدة‬ 2**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-225">In the **Azure region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="5a7cf-226">حدد **اتصال**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-226">Select **Connect**.</span></span> <span data-ttu-id="5a7cf-227">يجب أن يظهر موصل Azure الخاص بك في القائمة.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-227">Your Azure Connector should appear in the list.</span></span>

### <a name="import-the-commerce-preview-demo-base-extension"></a><span data-ttu-id="5a7cf-228">استيراد ملحق قاعدة العرض التوضيحي لمعاينة Commerce‬‏‫‬‏‫</span><span class="sxs-lookup"><span data-stu-id="5a7cf-228">Import the Commerce Preview Demo Base Extension</span></span>

<span data-ttu-id="5a7cf-229">لاستيراد "ملحق قاعدة العرض التوضيحي لمعاينة Commerce‬‏‫‬‏‫" في المشروع اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-229">To import the Commerce Preview Demo Base Extension into your project, follow these steps.</span></span>

1. <span data-ttu-id="5a7cf-230">افتح الصفحة الرئيسية للمشروع الخاص بك عن طريق تحديد اسم المشروع في الأعلى.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-230">Open the home page for your project by selecting the project name at the top.</span></span>
1. <span data-ttu-id="5a7cf-231">اتبع إحدى الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="5a7cf-231">Follow one of these steps:</span></span>

    - <span data-ttu-id="5a7cf-232">إذا كنت شريكًا، فحدد اللوحة **مكتبة الأصول** في أقصي اليمين.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-232">If you're a partner, select the **Asset library** tile on the far right.</span></span>
    - <span data-ttu-id="5a7cf-233">إذا كنت عميلاً، فاختر **مكتبة الأصول** من القائمة العليا.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-233">If you're a customer, select **Asset library** on the top menu.</span></span>

1. <span data-ttu-id="5a7cf-234">حدد **‏‫حزمة قابلة للنشر للبرنامج‬** من القائمة الموجودة على اليسار.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-234">In the list on the left, select **Software deployable package**.</span></span>
1. <span data-ttu-id="5a7cf-235">حدد **استيراد**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-235">Select **Import**.</span></span>
1. <span data-ttu-id="5a7cf-236">حدد **ملحق قاعدة العرض التوضيحي لمعاينة Commerce** من قائمة الأصول أسفل **‏‫مكتبة الأصول المشتركة‬**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-236">Under **Shared asset library**, select **Commerce Preview Demo Base Extension** in the list of assets.</span></span>
1. <span data-ttu-id="5a7cf-237">حدد **انتقاء**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-237">Select **Pick**.</span></span> <span data-ttu-id="5a7cf-238">سيتم إرجاعك إلى مكتبه الأصول وستشاهد الملحق في القائمة.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-238">You're returned to the Asset library, and you should see the extension in the list.</span></span>

<span data-ttu-id="5a7cf-239">يبين الرسم التوضيحي التالي الإجراءات التي يجب اتخاذها في صفحة **مكتبة الأصول** لـ LCS.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-239">The following illustration shows the actions that must be taken on the LCS **Asset library** page.</span></span>

![استيراد ملحق قاعدة العرض التوضيحي لمعاينة Commerce‬‏‫‬‏‫](./media/import.png)

### <a name="deploy-the-environment"></a><span data-ttu-id="5a7cf-241">نشر البيئة</span><span class="sxs-lookup"><span data-stu-id="5a7cf-241">Deploy the environment</span></span>

<span data-ttu-id="5a7cf-242">لاستيراد البيئة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-242">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="5a7cf-243">قد لا تضطر إلى إكمال الخطوات 6 و 7 و/أو 8 ، لأنه يتم تخطي الصفحات التي تحتوي على خيار واحد.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-243">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="5a7cf-244">في عرض **معلمات البيئة**، تأكد من أن النص **Dynamics 365 Commerce (معاينة) - العرض التوضيحي (10.0.6 مع تحديث النظام الأساسي 30)** يظهر مباشرة فوق حقل **اسم البيئة**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-244">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce (Preview) - Demo (10.0.6 with Platform update 30)** appears directly above the **Environment name** field.</span></span> <span data-ttu-id="5a7cf-245">راجع الرسم التوضيحي الذي يظهر بعد الخطوة 8.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-245">See the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="5a7cf-246">في القائمة العلوية، حدد **البيئات المستضافة على السحابة**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-246">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="5a7cf-247">حدد **إضافة** لإضافة بيئة.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-247">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="5a7cf-248">في حقل **إصدار التطبيق**، حدد **10.0.6**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-248">In the **Application version** field, select **10.0.6**.</span></span>
1. <span data-ttu-id="5a7cf-249">في **إصدار النظام الأساسي**، حدد **تحديث النظام الأساسي 30**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-249">In the **Platform version** field, select **Platform Update 30**.</span></span>

    ![تحديد إصدارات التطبيق والنظام الأساسي](./media/project1.png)

1. <span data-ttu-id="5a7cf-251">حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-251">Select **Next**.</span></span>
1. <span data-ttu-id="5a7cf-252">حدد **العرض التوضيحي** كمخطط البيئة.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-252">Select **Demo** as the environment topology.</span></span>

    ![تحديد مخطط البيئة 1](./media/project2.png)

1. <span data-ttu-id="5a7cf-254">حدد **Dynamics 365 Commerce (معاينة) - العرض التوضيحي** كمخطط البيئة.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-254">Select **Dynamics 365 Commerce (Preview) - Demo** as the environment topology.</span></span> <span data-ttu-id="5a7cf-255">إذا قمت بتكوين موصل Azure سابقًا، فسيتم استخدامه لهذه البيئة.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-255">If you configured a single Azure Connector earlier, it will be used for this environment.</span></span> <span data-ttu-id="5a7cf-256">إذا قمت بتكوين موصلات Azure متعددة، يمكنك تحديد الموصل المراد استخدامه: **‏‫شرق الولايات المتحدة‬** أو **‏‫شرق الولايات المتحدة‬ 2** أو **‏‫غرب الولايات المتحدة‬** أو **غرب الولايات المتحدة‬ 2**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-256">If you configured multiple Azure Connectors, you can select which connector to use: **East US**, **East US 2**, **West US**, or **West US 2**.</span></span> <span data-ttu-id="5a7cf-257">(للحصول علي أفضل أداء، ننصحك باختيار **غرب الولايات المتحدة‬ 2**.)</span><span class="sxs-lookup"><span data-stu-id="5a7cf-257">(For the best end-to-end performance, we recommend that you select **West US 2**.)</span></span>

    ![تحديد مخطط البيئة 2](./media/project3.png)

1. <span data-ttu-id="5a7cf-259">في صفحة **بيئة النشر**، أدخل اسم بيئة.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-259">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="5a7cf-260">اترك الإعدادات المتقدمة كما هي.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-260">Leave the advanced settings as they are.</span></span>

    ![نشر صفحة البيئة](./media/project4.png)

1. <span data-ttu-id="5a7cf-262">اضبط حجم الجهاز الظاهري (VM) كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-262">Adjust the VM size as required.</span></span> <span data-ttu-id="5a7cf-263">(نوصي بوحدة حفظ المخزون للجهاز الظاهري (VM) \[SKU\] **D13 v2**.)</span><span class="sxs-lookup"><span data-stu-id="5a7cf-263">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="5a7cf-264">راجع شروط التسعير والترخيص، ثم حدد خانة الاختيار للإشارة إلى موافقتك عليها.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-264">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="5a7cf-265">حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-265">Select **Next**.</span></span>
1. <span data-ttu-id="5a7cf-266">في صفحة تأكيد النشر، تحقق من صحة التفاصيل، ثم حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-266">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="5a7cf-267">ستعود إلى طريقة العرض **بيئات مستضافة على الشبكة السحابية** بعدها ستظهر البيئة في القائمة.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-267">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="5a7cf-268">سيتم عرض البيئة المطلوبة في قائمة الانتظار ثم نشرها.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-268">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="5a7cf-269">ستستغرق عمليات سير العمل في البيئة بعض الوقت لإكمالها.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-269">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="5a7cf-270">ولذلك، تحقق مره أخرى بعد ما يقرب من ست إلى تسع ساعات.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-270">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="5a7cf-271">قبل المتابعة، تأكد أن حالة البيئة هي **تم النشر**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-271">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-rcsu"></a><span data-ttu-id="5a7cf-272">تهيئة RCSU</span><span class="sxs-lookup"><span data-stu-id="5a7cf-272">Initialize RCSU</span></span>

<span data-ttu-id="5a7cf-273">لتهيئة RCSU اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="5a7cf-273">To initialize RCSU, follow these steps.</span></span>

1. <span data-ttu-id="5a7cf-274">في طريقة العرض **بيئات مستضافة على الشبكة السحابية**، حدد البيئة من القائمة.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-274">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="5a7cf-275">حدد **كل التفاصيل** من طريقة عرض البيئة الموجودة على الجانب الأيسر.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-275">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="5a7cf-276">ستظهر طريقة عرض تفاصيل البيئة.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-276">The environment details view appears.</span></span>
1. <span data-ttu-id="5a7cf-277">ضمن **ميزات البيئة**، حدد **إدارة**</span><span class="sxs-lookup"><span data-stu-id="5a7cf-277">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="5a7cf-278">في علامة التبويب **البيع بالتجزئة**، حدد **تهيئه**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-278">On the **Retail** tab, select **Initialize**.</span></span> <span data-ttu-id="5a7cf-279">ستظهر طريقة عرض معلمات تهيئة RCSU.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-279">The RCSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="5a7cf-280">في حقل **المنطقة**، اختر إما **‏‫شرق الولايات المتحدة‬**، أو **‏‫شرق الولايات المتحدة‬ 2**، أو **‏‫غرب الولايات المتحدة‬** أو **‏‫غرب الولايات المتحدة‬ 2**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-280">In the **Region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="5a7cf-281">في حقل **الإصدار** ، حدد **تحديد إصدار** في القائمة، ثم حدد **9.16.19262.5** في الحقل الذي يظهر.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-281">In the **Version** field, select **Specify a version** in the list, and then specify **9.16.19262.5** in the field that appears.</span></span> <span data-ttu-id="5a7cf-282">تأكد من تحديد نفس الإصدار المشار اليه هنا.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-282">Be sure to specify the exact version that is indicated here.</span></span> <span data-ttu-id="5a7cf-283">وإلا، سيلزمك تحديث RCSU إلى الإصدار الصحيح لاحقا.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-283">Otherwise, you will have to update RCSU to the correct version later.</span></span>
1. <span data-ttu-id="5a7cf-284">قم بتشغيل خيار **تطبيق الملحق**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-284">Turn on the **Apply extension** option.</span></span>
1. <span data-ttu-id="5a7cf-285">من قائمة الملحقات، حدد **ملحق قاعدة العرض التوضيحي لمعاينة Commerce‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-285">In the list of extensions, select **Commerce Preview Demo Base Extension**.</span></span>
1. <span data-ttu-id="5a7cf-286">حدد **تهيئة**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-286">Select **Initialize**.</span></span>
1. <span data-ttu-id="5a7cf-287">في صفحة تأكيد النشر، تحقق من صحة التفاصيل، ثم حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-287">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="5a7cf-288">يتم إرجاعك إلى طريقة العرض **إدارة البيئع بالتجزئة**، مع تحديد علامة التبويب **البيئع بالتجزئة**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-288">You're returned to the **Retail management** view, where the **Retail** tab is selected.</span></span> <span data-ttu-id="5a7cf-289">تم وضع RCSU في قائمة الانتظار لعمية التوفير.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-289">Your RCSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="5a7cf-290">قبل المتابعة، تأكد أن حالة RCSU هي **نجاح**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-290">Before you continue, make sure that the status of your RCSU is **Success**.</span></span> <span data-ttu-id="5a7cf-291">تستغرق التهيئة حوالي ساعتين إلى خمس ساعات.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-291">Initialization takes approximately two to five hours.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="5a7cf-292">تهيئة التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="5a7cf-292">Initialize e-Commerce</span></span>

<span data-ttu-id="5a7cf-293">لتهيئة التجارة الإلكترونية، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="5a7cf-293">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="5a7cf-294">في علامة **التبويب التجارة الكترونيه (معاينه)** ، راجع موافقه المعاينة ، **ثم**حدد الاعداد.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-294">On the **e-Commerce (Preview)** tab, review the preview consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="5a7cf-295">أدخل اسما لـ **اسم مستأجر التجارة الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-295">In the **e-Commerce tenant name** field, enter a name.</span></span> <span data-ttu-id="5a7cf-296">ومع ذلك، لاحظ أن ذلك الاسم سيكون مرئيًا في بعض عناوين URL التي تشير إلى مثيل التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-296">However, be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="5a7cf-297">في الحقل **اسم Retail cloud scale unit‬‏‫**، حدد RCSU الخاص بك في القائمة.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-297">In the **Retail cloud scale unit name** field, select your RCSU in the list.</span></span> <span data-ttu-id="5a7cf-298">(يجب أن تحتوي القائمة على خيار واحد فقط).</span><span class="sxs-lookup"><span data-stu-id="5a7cf-298">(The list should have only one option.)</span></span>

    <span data-ttu-id="5a7cf-299">يتم تعيين حقل **جغرافيا التجارية الإلكترونية** تلقائيًا، ولا يمكن تغيير القيمة.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-299">The **e-Commerce geography** field is set automatically, and the value can't be changed.</span></span>

1. <span data-ttu-id="5a7cf-300">للمتابعة، حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-300">Select **Next** to continue.</span></span>
1. <span data-ttu-id="5a7cf-301">في الحقل **أسماء الأجهزة المضيفة المدعومة**، أدخل أي مجال صالح، مثل `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-301">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1.  <span data-ttu-id="5a7cf-302">في الحقل **مجموعة أمان AAD لمسؤول النظام‬‏‫**، أدخل الأحرف القليلة الأولى من اسم مجموعة الأمان التي تريد استخدامها.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-302">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="5a7cf-303">حدد رمز العدسة المكبرة لعرض نتائج البحث.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-303">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="5a7cf-304">حدد مجموعة أمان من القائمة.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-304">Select a security group from the list.</span></span>
2.  <span data-ttu-id="5a7cf-305">في الحقل **مجموعه أمان AAD الخاصة بالمشرف على التقييمات والمراجعات**، أدخل الأحرف القليلة الأولى من اسم مجموعة الأمان التي تريد استخدامها.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-305">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="5a7cf-306">حدد رمز العدسة المكبرة لعرض نتائج البحث.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-306">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="5a7cf-307">حدد مجموعة أمان من القائمة.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-307">Select a security group from the list.</span></span>
1. <span data-ttu-id="5a7cf-308">اترك خيار **تمكين خدمة التقييمات والمراجعات** ممكنًا.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-308">Leave the **Enable ratings and review service** option turned on.</span></span>
1. <span data-ttu-id="5a7cf-309">إذا قمت بالفعل بإكمال خطوة الموافقة على Microsoft Azure Active Directory (Azure AD) كما هو موضح في قسم "‏‫منح الوصول إلى تطبيقات التجارة الإلكترونية‬" ، فحدد خانة الاختيار لتأكيد موافقتك.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-309">If you have already completed the Microsoft Azure Active Directory (Azure AD) consent step as described in the "Grant access to e-Commerce applications" section, select the check box to confirm your consent.</span></span> <span data-ttu-id="5a7cf-310">إذا لم تكن قد أكملت هذه الخطوة بعد، تحتاج إلى القيام بذلك قبل متابعة التهيئة.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-310">If you have not yet completed this step, you need to do that before proceeding with the initialization.</span></span> <span data-ttu-id="5a7cf-311">حدد الارتباط ضمن النص الموجود بجوار خانة الاختيار لفتح مربع حوار الموافقة وإكمال الخطوة.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-311">Select the link within the text next to the check box to open the consent dialog box and complete the step.</span></span>
1. <span data-ttu-id="5a7cf-312">حدد **تهيئة**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-312">Select **Initialize**.</span></span> <span data-ttu-id="5a7cf-313">يتم إرجاعك إلى طريقة العرض **إدارة البيئع بالتجزئة**، مع تحديد علامة التبويب **التجارةالإلكترونية (معيانة)**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-313">You're returned to the **Retail management** view, where the **e-Commerce (Preview)** tab is selected.</span></span> <span data-ttu-id="5a7cf-314">تم بدء تشغيل تهيئة التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-314">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="5a7cf-315">قبل المتابعة، انتظر حتى تصبح حالة تهيئة التجارة الإلكترونية هي **نجاح التهيئة**.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-315">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="5a7cf-316">ضمن **الارتباطات** الواردة في الجانب السفلي الأيمن، قم بتدوين عناوين URL للارتباطات التالية:</span><span class="sxs-lookup"><span data-stu-id="5a7cf-316">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="5a7cf-317">**موقع التجارة الإلكترونية**  – رابط جذر موقع التجارة الإلكترونية الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-317">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="5a7cf-318">**أداة إدارة موقع التجارة الإلكترونية‬‏‫** – رابط أداة إدارة الموقع.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-318">**e-Commerce site management tool** – The link to the site management tool.</span></span>

## <a name="commerce-preview-environment-support"></a><span data-ttu-id="5a7cf-319">دعم بيئة معاينة Commerce</span><span class="sxs-lookup"><span data-stu-id="5a7cf-319">Commerce preview environment support</span></span>

<span data-ttu-id="5a7cf-320">في حالة مواجهة مشكلات أثناء إكمال خطوات التوفير، يُرجى زيارة، [مجموعة Microsoft Dynamics 365 Commerce Preview Yammer ](https://aka.ms/Dynamics365CommercePreviewYammer) للحصول على المساعدة.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-320">If you experience issues while you're completing the provisioning steps, visit the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer) for help.</span></span>

<span data-ttu-id="5a7cf-321">إذا واجهت مشكلات عند محاولة الوصول إلى مجموعة Yammer ، يمكنك التواصل مع Microsoft عبر البريد الكتروني <Dynamics365Commerce@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-321">If you experience issues when you try to access the Yammer group, you can contact Microsoft by email at <Dynamics365Commerce@microsoft.com>.</span></span> <span data-ttu-id="5a7cf-322">لا يتم مراقبة هذا البريد الإلكتروني بنشاط.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-322">This email address isn't actively monitored.</span></span> <span data-ttu-id="5a7cf-323">لذا، توقع تأخير في الاستجابة.</span><span class="sxs-lookup"><span data-stu-id="5a7cf-323">Therefore, expect a delay in the response.</span></span>

## <a name="next-steps"></a><span data-ttu-id="5a7cf-324">الخطوات التالية</span><span class="sxs-lookup"><span data-stu-id="5a7cf-324">Next steps</span></span>

<span data-ttu-id="5a7cf-325">لمتابعة عملية توفير وتكوين بيئة معاينة Commerce، راجع [ تكوين بيئة معاينة Commerce](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="5a7cf-325">To continue the process of provisioning and configuring your Commerce preview environment, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5a7cf-326">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="5a7cf-326">Additional resources</span></span>

[<span data-ttu-id="5a7cf-327">نظرة عامة على بيئة معاينة التجارة</span><span class="sxs-lookup"><span data-stu-id="5a7cf-327">Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="5a7cf-328">تكوين بيئة معاينة التجارة</span><span class="sxs-lookup"><span data-stu-id="5a7cf-328">Configure a Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="5a7cf-329">تكوين الميزات الاختيارية لبيئة معاينة التجارة</span><span class="sxs-lookup"><span data-stu-id="5a7cf-329">Configure optional features for a Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="5a7cf-330">الأسئلة المتداولة حول بيئة معاينة التجارة</span><span class="sxs-lookup"><span data-stu-id="5a7cf-330">Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="5a7cf-331">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="5a7cf-331">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="5a7cf-332">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="5a7cf-332">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="5a7cf-333">مدخل Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="5a7cf-333">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="5a7cf-334">موقع ويب Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="5a7cf-334">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="5a7cf-335">موارد تعليمات لـ Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="5a7cf-335">Help resources for Dynamics 365 Retail</span></span>](../retail/index.md)
