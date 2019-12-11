---
title: نشر مستأجر التجارة الإلكترونية الجديد
description: يصف هذا الموضوع كيفية نشر مستأجر التجارة الإلكترونية الجديد باستخدام Microsoft Dynamics Lifecycle Services (LCS).
author: psimolin
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c2632632b9b21dd3a88e9a4df0e65cfd28e579d2
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697441"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="a5cbb-103">نشر مستأجر التجارة الإلكترونية الجديد</span><span class="sxs-lookup"><span data-stu-id="a5cbb-103">Deploy a new e-Commerce tenant</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="a5cbb-104">يصف هذا الموضوع كيفية نشر موقع تجارة إلكترونية جديد باستخدام Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="a5cbb-104">This topic describes how to deploy a new e-Commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="overview"></a><span data-ttu-id="a5cbb-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="a5cbb-105">Overview</span></span>
    
<span data-ttu-id="a5cbb-106">تعتبر Microsoft Dynamics Lifecycle Services مساحة عمل تعاونيه قائمة على السحابة ويمكن للشركاء والعملاء استخدامها لإدارة المشاريع والبيئات الخاصة بهم، وعرض أحدث المعلومات حول منتجات Microsoft Dynamics والميزات، وإنشاء حوادث الدعم وتعقبها واستعراضها.</span><span class="sxs-lookup"><span data-stu-id="a5cbb-106">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="a5cbb-107">تتكامل ميزات إدارة التجارة الإلكترونية في LCS.</span><span class="sxs-lookup"><span data-stu-id="a5cbb-107">E-Commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="a5cbb-108">لمعرفه المزيد عن LCS، راجع [دليل مستخدم Lifecycle Services](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span><span class="sxs-lookup"><span data-stu-id="a5cbb-108">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="a5cbb-109">البدء</span><span class="sxs-lookup"><span data-stu-id="a5cbb-109">Get started</span></span>

<span data-ttu-id="a5cbb-110">قبل أن تتمكن من تهيئة التجارة الإلكترونية، يجب تهيئة مشروع، وبيئة، و Retail Cloud Scale Unit (RCSU).</span><span class="sxs-lookup"><span data-stu-id="a5cbb-110">Before you can initialize e-Commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="a5cbb-111">للقيام بعملية التهيئة في LCS ، يجب أن يكون لديك أذونات إما لمالك المشروع أو دور مُدير البيئة.</span><span class="sxs-lookup"><span data-stu-id="a5cbb-111">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="a5cbb-112">يتم دعم مخططات بيئة الإنتاج وبيئة الاختبار المعزولة.</span><span class="sxs-lookup"><span data-stu-id="a5cbb-112">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="a5cbb-113">لمزيد من المعلومات حول البيئات، راجع [تخطيط البيئة](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span><span class="sxs-lookup"><span data-stu-id="a5cbb-113">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="a5cbb-114">لمزيد من المعلومات حول RCSU، راجع [تهيئة Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="a5cbb-114">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="a5cbb-115">تهيئة التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="a5cbb-115">Initialize e-Commerce</span></span>

<span data-ttu-id="a5cbb-116">استخدم هذا الاجراء لتهيئة ميزة التجارة الإلكترونية في بيئة موجودة.</span><span class="sxs-lookup"><span data-stu-id="a5cbb-116">Use this procedure to initialize the e-Commerce feature in an existing environment.</span></span>

<span data-ttu-id="a5cbb-117">قبل البدء، تأكد من أن لديك المعلومات المطلوبة التالية:</span><span class="sxs-lookup"><span data-stu-id="a5cbb-117">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="a5cbb-118">RCSU المستخدمة.</span><span class="sxs-lookup"><span data-stu-id="a5cbb-118">The RCSU that will be used.</span></span>
- <span data-ttu-id="a5cbb-119">مجموعه أمان Microsoft Azure Active Directory التي سيتم استخدامها لمسؤولي النظام بالتجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a5cbb-119">The Microsoft Azure Active Directory security group that will be used for e-Commerce system admins.</span></span>
- <span data-ttu-id="a5cbb-120">مجموعه أمان Microsoft Azure Active Directory التي سيتم استخدامها للتصنيفات ومراجعات الوسطاء.</span><span class="sxs-lookup"><span data-stu-id="a5cbb-120">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="a5cbb-121">المجالات التي سوف يتم إقرانها بالبيئة.</span><span class="sxs-lookup"><span data-stu-id="a5cbb-121">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="a5cbb-122">بالإضافة إلى ذلك، يمكنك جمع المعلومات الاختيارية التالية:</span><span class="sxs-lookup"><span data-stu-id="a5cbb-122">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="a5cbb-123">معلومات Azure AD العمل-المستهلك (B2C) :</span><span class="sxs-lookup"><span data-stu-id="a5cbb-123">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="a5cbb-124">اسم المستأجر.</span><span class="sxs-lookup"><span data-stu-id="a5cbb-124">Tenant Name.</span></span>
    - <span data-ttu-id="a5cbb-125">معرّف العميل.</span><span class="sxs-lookup"><span data-stu-id="a5cbb-125">Client ID.</span></span>
    - <span data-ttu-id="a5cbb-126">تسجيل الدخول إلى المجال المخصص.</span><span class="sxs-lookup"><span data-stu-id="a5cbb-126">Login Custom Domain.</span></span>
    - <span data-ttu-id="a5cbb-127">عنوان URL الخاص بالرد.</span><span class="sxs-lookup"><span data-stu-id="a5cbb-127">Reply URL.</span></span>
    - <span data-ttu-id="a5cbb-128">معرف سياسة تسجيل الاشتراك وتسجيل الدخول.</span><span class="sxs-lookup"><span data-stu-id="a5cbb-128">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="a5cbb-129">إعادة تعيين مُعرف سياسة كلمة المرور.</span><span class="sxs-lookup"><span data-stu-id="a5cbb-129">Reset password Policy ID.</span></span>
    - <span data-ttu-id="a5cbb-130">تحرير معرف سياسة ملف التعريف.</span><span class="sxs-lookup"><span data-stu-id="a5cbb-130">Edit Profile Policy ID.</span></span>

[!NOTE]
<span data-ttu-id="a5cbb-131">يمكن إضافة هذه المعلومات في وقت لاحق، من خلال طلب خدمة.</span><span class="sxs-lookup"><span data-stu-id="a5cbb-131">This information can be added later, through a service request.</span></span>

<span data-ttu-id="a5cbb-132">بعد تجميع المعلومات المطلوبة، اتبع الخطوات التالية لتهيئه التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a5cbb-132">After you've collected the required information, follow these steps to initialize e-Commerce.</span></span>

1. <span data-ttu-id="a5cbb-133">سجل الدخول إلى [LCS](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="a5cbb-133">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="a5cbb-134">افتح المشروع الذي يحتوي علي البيئة التي ترغب في تهيئة التجارة الإلكترونية فيها.</span><span class="sxs-lookup"><span data-stu-id="a5cbb-134">Open the project that contains the environment where you want to initialize e-Commerce.</span></span>
1. <span data-ttu-id="a5cbb-135">في قسم **البيئات** ، حدد البيئة.</span><span class="sxs-lookup"><span data-stu-id="a5cbb-135">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="a5cbb-136">تحت **ميزات البيئة**، حدد ارتباط **إدارة Retail** .</span><span class="sxs-lookup"><span data-stu-id="a5cbb-136">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="a5cbb-137">في علامة التبويب **التجارة الإلكترونية** ، حدد **إعداد**.</span><span class="sxs-lookup"><span data-stu-id="a5cbb-137">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="a5cbb-138">سوف يظهر مربع حوار، حيث يجب عليك إدخال المعلومات المطلوب توفيرها.</span><span class="sxs-lookup"><span data-stu-id="a5cbb-138">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="a5cbb-139">قم بملء المعلومات المطلوبة، ثم انتقل إلى الصفحة التالية.</span><span class="sxs-lookup"><span data-stu-id="a5cbb-139">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="a5cbb-140">‏‫يمكنك في الصفحة التالية ملء المعلومات المطلوبة، ثم ارسل النموذج.</span><span class="sxs-lookup"><span data-stu-id="a5cbb-140">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="a5cbb-141">يتم إرجاعك إلى علامة تبويب **التجارة الإلكترونية** ، حيث ستشاهد انه قد تم بدء التهيئة.</span><span class="sxs-lookup"><span data-stu-id="a5cbb-141">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="a5cbb-142">لعرض حالة التهيئة ، قم **بالتحديث** أو الرجوع إلى علامة تبويب **التجارة الإلكترونية** لاحقا.</span><span class="sxs-lookup"><span data-stu-id="a5cbb-142">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="a5cbb-143">عند تهيئة التجارة الإلكترونية من LCS، يقوم النظام بتوفير العديد من المكونات المطلوبة للتجارة الإلكترونية وربطها بالبيئة.</span><span class="sxs-lookup"><span data-stu-id="a5cbb-143">When e-Commerce is initialized from LCS, the system provisions several components that are required for e-Commerce and associates them with the environment.</span></span> <span data-ttu-id="a5cbb-144">بعد الانتهاء من التوفير، يتم تحديث علامة التبويب **التجارة الإلكترونية** في صفحة **إدارة Retail** لتعكس التوفير.</span><span class="sxs-lookup"><span data-stu-id="a5cbb-144">After provisioning is completed, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="a5cbb-145">وتعرض الصفحة أحدث عمليات نشر التخصيص وحالة أي عمليات نشر أخرى جارية.</span><span class="sxs-lookup"><span data-stu-id="a5cbb-145">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="a5cbb-146">ويتضمن أيضا ارتباطات إلى موقع التجارة الإلكترونية وأداة إدارة موقع التجارة الإلكترونية (أداة التأليف).</span><span class="sxs-lookup"><span data-stu-id="a5cbb-146">It also includes links to the e-Commerce site and the e-Commerce site management tool (the authoring tool).</span></span>

## <a name="access-the-authoring-environment"></a><span data-ttu-id="a5cbb-147">الوصول إلى بيئة التأليف</span><span class="sxs-lookup"><span data-stu-id="a5cbb-147">Access the authoring environment</span></span>

<span data-ttu-id="a5cbb-148">للوصول إلى بيئة التأليف، انتقل إلى علامة التبويب **التجارة الإلكترونية** في صفحة **إدارة Retail** .</span><span class="sxs-lookup"><span data-stu-id="a5cbb-148">To access the authoring environment, go to the **e-Commerce** tab on the **Retail management** page.</span></span> <span data-ttu-id="a5cbb-149">هناك، سوف تجد ارتباطات لموقع التجارة الإلكترونية الخاصة بك وأداة إدارة المواقع.</span><span class="sxs-lookup"><span data-stu-id="a5cbb-149">There, you will find links to your e-Commerce site and the site management tool.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a5cbb-150">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="a5cbb-150">Additional resources</span></span>

[<span data-ttu-id="a5cbb-151">نظرة عامة على المتجر على الإنترنت</span><span class="sxs-lookup"><span data-stu-id="a5cbb-151">Online store overview</span></span>](online-store-overview.md)

[<span data-ttu-id="a5cbb-152">إنشاء موقع تجارة إلكترونية</span><span class="sxs-lookup"><span data-stu-id="a5cbb-152">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="a5cbb-153">إقران موقع عبر الإنترنت بقناة</span><span class="sxs-lookup"><span data-stu-id="a5cbb-153">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="a5cbb-154">تكوين اسم مجالك</span><span class="sxs-lookup"><span data-stu-id="a5cbb-154">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="a5cbb-155">إضافة الدعم إلى شبكة تسليم المحتوى (CDN)</span><span class="sxs-lookup"><span data-stu-id="a5cbb-155">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="a5cbb-156">تمكين اكتشاف المتجر استنادًا إلى الموقع</span><span class="sxs-lookup"><span data-stu-id="a5cbb-156">Enable location-based store detection</span></span>](enable-store-detection.md)

[<span data-ttu-id="a5cbb-157">إعداد صفحات مخصصة لعمليات تسجيل دخول المستخدمين</span><span class="sxs-lookup"><span data-stu-id="a5cbb-157">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)
