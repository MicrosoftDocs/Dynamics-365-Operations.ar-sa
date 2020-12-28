---
title: نشر مستأجر التجارة الإلكترونية الجديد
description: يصف هذا الموضوع كيفية نشر موقع تجارة إلكترونية جديد لـ Dynamics 365 Commerce باستخدام Microsoft Dynamics Lifecycle Services (LCS).
author: psimolin
manager: annbe
ms.date: 07/02/2020
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
ms.openlocfilehash: 157dc8225e5bbf9338a1b5a79a2880e8a8c4bf10
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517272"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="6b3d8-103">نشر مستأجر التجارة الإلكترونية الجديد</span><span class="sxs-lookup"><span data-stu-id="6b3d8-103">Deploy a new e-commerce tenant</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="6b3d8-104">يصف هذا الموضوع كيفية نشر موقع تجارة إلكترونية جديد لـ Dynamics 365 Commerce باستخدام Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="6b3d8-104">This topic describes how to deploy a new Dynamics 365 Commerce e-commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="overview"></a><span data-ttu-id="6b3d8-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="6b3d8-105">Overview</span></span>

<span data-ttu-id="6b3d8-106">تعتبر Microsoft Dynamics Lifecycle Services مساحة عمل تعاونيه قائمة على السحابة ويمكن للشركاء والعملاء استخدامها لإدارة المشاريع والبيئات الخاصة بهم، وعرض أحدث المعلومات حول منتجات Microsoft Dynamics والميزات، وإنشاء حوادث الدعم وتعقبها واستعراضها.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-106">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="6b3d8-107">تتكامل ميزات إدارة التجارة الإلكترونية في LCS.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-107">E-commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="6b3d8-108">لمعرفه المزيد عن LCS، راجع [دليل مستخدم Lifecycle Services](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span><span class="sxs-lookup"><span data-stu-id="6b3d8-108">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="6b3d8-109">بدء الاستخدام</span><span class="sxs-lookup"><span data-stu-id="6b3d8-109">Get started</span></span>

<span data-ttu-id="6b3d8-110">قبل أن تتمكن من تهيئة التجارة الإلكترونية، يجب تهيئة مشروع، وبيئة، و Retail Cloud Scale Unit (RCSU).</span><span class="sxs-lookup"><span data-stu-id="6b3d8-110">Before you can initialize e-commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="6b3d8-111">للقيام بعملية التهيئة في LCS ، يجب أن يكون لديك أذونات إما لمالك المشروع أو دور مُدير البيئة.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-111">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="6b3d8-112">يتم دعم مخططات بيئة الإنتاج وبيئة الاختبار المعزولة.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-112">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="6b3d8-113">لمزيد من المعلومات حول البيئات، راجع [تخطيط البيئة](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span><span class="sxs-lookup"><span data-stu-id="6b3d8-113">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="6b3d8-114">لمزيد من المعلومات حول RCSU، راجع [تهيئة Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="6b3d8-114">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="6b3d8-115">تهيئة التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="6b3d8-115">Initialize e-commerce</span></span>

<span data-ttu-id="6b3d8-116">استخدم هذا الإجراء لتهيئة ميزة التجارة الإلكترونية في بيئة موجودة.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-116">Use this procedure to initialize the e-commerce feature in an existing environment.</span></span>

<span data-ttu-id="6b3d8-117">قبل البدء، تأكد من أن لديك المعلومات المطلوبة التالية:</span><span class="sxs-lookup"><span data-stu-id="6b3d8-117">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="6b3d8-118">RCSU المستخدمة.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-118">The RCSU that will be used.</span></span>
- <span data-ttu-id="6b3d8-119">مجموعة أمان Microsoft Azure Active Directory التي سيتم استخدامها لمسؤولي النظام بالتجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-119">The Microsoft Azure Active Directory security group that will be used for e-commerce system admins.</span></span>
- <span data-ttu-id="6b3d8-120">مجموعه أمان Microsoft Azure Active Directory التي سيتم استخدامها للتصنيفات ومراجعات الوسطاء.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-120">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="6b3d8-121">المجالات التي سوف يتم إقرانها بالبيئة.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-121">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="6b3d8-122">بالإضافة إلى ذلك، يمكنك جمع المعلومات الاختيارية التالية:</span><span class="sxs-lookup"><span data-stu-id="6b3d8-122">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="6b3d8-123">معلومات Azure AD العمل-المستهلك (B2C) :</span><span class="sxs-lookup"><span data-stu-id="6b3d8-123">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="6b3d8-124">اسم المستأجر.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-124">Tenant Name.</span></span>
    - <span data-ttu-id="6b3d8-125">معرّف العميل.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-125">Client ID.</span></span>
    - <span data-ttu-id="6b3d8-126">تسجيل الدخول إلى المجال المخصص.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-126">Login Custom Domain.</span></span>
    - <span data-ttu-id="6b3d8-127">عنوان URL الخاص بالرد.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-127">Reply URL.</span></span>
    - <span data-ttu-id="6b3d8-128">معرف سياسة تسجيل الاشتراك وتسجيل الدخول.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-128">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="6b3d8-129">إعادة تعيين مُعرف سياسة كلمة المرور.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-129">Reset password Policy ID.</span></span>
    - <span data-ttu-id="6b3d8-130">تحرير معرف سياسة ملف التعريف.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-130">Edit Profile Policy ID.</span></span>

> [!NOTE]
> <span data-ttu-id="6b3d8-131">يمكن إضافة هذه المعلومات في وقت لاحق، من خلال طلب خدمة.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-131">This information can be added later, through a service request.</span></span>

<span data-ttu-id="6b3d8-132">بعد تجميع المعلومات المطلوبة، اتبع الخطوات التالية لتهيئة التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-132">After you've collected the required information, follow these steps to initialize e-commerce.</span></span>

1. <span data-ttu-id="6b3d8-133">سجل الدخول إلى [LCS](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="6b3d8-133">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="6b3d8-134">افتح المشروع الذي يحتوي على البيئة التي ترغب في تهيئة التجارة الإلكترونية فيها.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-134">Open the project that contains the environment where you want to initialize e-commerce.</span></span>
1. <span data-ttu-id="6b3d8-135">في قسم **البيئات** ، حدد البيئة.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-135">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="6b3d8-136">تحت **ميزات البيئة**، حدد ارتباط **إدارة Retail** .</span><span class="sxs-lookup"><span data-stu-id="6b3d8-136">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="6b3d8-137">في علامة التبويب **التجارة الإلكترونية** ، حدد **إعداد**.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-137">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="6b3d8-138">سوف يظهر مربع حوار، حيث يجب عليك إدخال المعلومات المطلوب توفيرها.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-138">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="6b3d8-139">قم بملء المعلومات المطلوبة، ثم انتقل إلى الصفحة التالية.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-139">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="6b3d8-140">‏‫يمكنك في الصفحة التالية ملء المعلومات المطلوبة، ثم ارسل النموذج.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-140">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="6b3d8-141">يتم إرجاعك إلى علامة تبويب **التجارة الإلكترونية** ، حيث ستشاهد انه قد تم بدء التهيئة.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-141">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="6b3d8-142">لعرض حالة التهيئة ، قم **بالتحديث** أو الرجوع إلى علامة تبويب **التجارة الإلكترونية** لاحقا.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-142">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="6b3d8-143">عند تهيئة التجارة الإلكترونية من LCS، يقوم النظام بتوفير العديد من المكونات المطلوبة للتجارة الإلكترونية وربطها بالبيئة.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-143">When e-commerce is initialized from LCS, the system provisions several components that are required for e-commerce and associates them with the environment.</span></span> <span data-ttu-id="6b3d8-144">بعد الانتهاء من عملية التوفير، يتم تحديث علامة التبويب **التجارة الإلكترونية** في صفحة **إدارة البيع بالتجزئة** لعرض التوفير.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-144">After provisioning is complete, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="6b3d8-145">وتعرض الصفحة أحدث عمليات نشر التخصيص وحالة أي عمليات نشر أخرى جارية.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-145">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="6b3d8-146">وتتضمن أيضًا ارتباطات إلى موقع التجارة الإلكترونية ومنشئ موقع التجارة الإلكترونية حيث يتم تأليف المواقع.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-146">It also includes links to the e-commerce site and the Commerce site builder where sites are authored.</span></span>

## <a name="access-commerce-site-builder"></a><span data-ttu-id="6b3d8-147">الوصول إلى منشئ موقع التجارة</span><span class="sxs-lookup"><span data-stu-id="6b3d8-147">Access Commerce site builder</span></span>

<span data-ttu-id="6b3d8-148">للوصول إلى منشئ موقع التجارة، انتقل إلى علامة التبويب **التجارة الإلكترونية** الموجودة في صفحة **إدارة البيع بالتجزئة** في LCS وحدد ارتباط **أداة إدارة موقع التجارة الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-148">To access Commerce site builder, go to the **e-Commerce** tab on the **Retail management** page in LCS and select the **e-Commerce site management tool** link.</span></span> <span data-ttu-id="6b3d8-149">تعرض صفحة منشئ الموقع المنتقل إليها طريقة عرض على مستوى المستأجر.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-149">The site builder landing page displays a tenant-level view.</span></span> <span data-ttu-id="6b3d8-150">ويمكنك من خلال هذه الصفحة:</span><span class="sxs-lookup"><span data-stu-id="6b3d8-150">From this page, you can:</span></span>

- <span data-ttu-id="6b3d8-151">تعديل الإعدادات على مستوى المستأجر.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-151">Modify tenant-level settings.</span></span>
- <span data-ttu-id="6b3d8-152">الانتقال إلى أي موقع أنشأته ولديك إذن لعرضه.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-152">Navigate to any site you have created, and have permission to view.</span></span> 
- <span data-ttu-id="6b3d8-153">الوصول إلى ميزات المراجعة كالإشراف وإعداد التقارير.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-153">Access Reviews features such as moderation and reporting.</span></span>
- <span data-ttu-id="6b3d8-154">إنشاء موقع جديد.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-154">Create a new site.</span></span> <span data-ttu-id="6b3d8-155">لمزيد من المعلومات حول كيفية إنشاء موقع جديد، راجع [إنشاء موقع تجارة إلكترونية](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="6b3d8-155">For more information about how to create a new site, see [Create an e-commerce site](create-ecommerce-site.md) .</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="6b3d8-156">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="6b3d8-156">Additional resources</span></span>

[<span data-ttu-id="6b3d8-157">تكوين اسم مجالك</span><span class="sxs-lookup"><span data-stu-id="6b3d8-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="6b3d8-158">إنشاء موقع تجارة إلكترونية</span><span class="sxs-lookup"><span data-stu-id="6b3d8-158">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="6b3d8-159">إقران موقع Dynamics 365 Commerce بقناة عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="6b3d8-159">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="6b3d8-160">إدارة ملفات robots.txt</span><span class="sxs-lookup"><span data-stu-id="6b3d8-160">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="6b3d8-161">تحميل عناوين URL لإعادة التوجيه‬ بشكل مجمع</span><span class="sxs-lookup"><span data-stu-id="6b3d8-161">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="6b3d8-162">إعداد مستأجر B2C في Commerce</span><span class="sxs-lookup"><span data-stu-id="6b3d8-162">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="6b3d8-163">إعداد صفحات مخصصة لعمليات تسجيل دخول المستخدمين</span><span class="sxs-lookup"><span data-stu-id="6b3d8-163">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="6b3d8-164">تكوين مستأجرين متعددين لمتاجرة عمل-مستهلك في بيئة Commerce</span><span class="sxs-lookup"><span data-stu-id="6b3d8-164">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="6b3d8-165">إضافة الدعم إلى شبكة تسليم المحتوى (CDN)</span><span class="sxs-lookup"><span data-stu-id="6b3d8-165">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="6b3d8-166">تمكين اكتشاف المتجر استنادًا إلى الموقع</span><span class="sxs-lookup"><span data-stu-id="6b3d8-166">Enable location-based store detection</span></span>](enable-store-detection.md)
