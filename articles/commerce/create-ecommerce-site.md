---
title: إنشاء موقع تجارة إلكترونية
description: يصف هذا الموضوع المهام المرتبطة بإنشاء موقع جديد للتجارة الإلكترونية في Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fd87a51b73deae64867b0420c00db9fce7c79336
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697119"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="e2871-103">إنشاء موقع تجارة إلكترونية</span><span class="sxs-lookup"><span data-stu-id="e2871-103">Create an e-Commerce site</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="e2871-104">يصف هذا الموضوع المهام المرتبطة بإنشاء موقع جديد للتجارة الإلكترونية في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e2871-104">This topic describes the tasks that are associated with the creation of a new e-Commerce site in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e2871-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="e2871-105">Overview</span></span>

<span data-ttu-id="e2871-106">لبدء تطوير موقع التجارة الإلكترونية الخاص بك، يجب عليك أولاً إنشاء موقع جديد في بيئة تأليف الموقع.</span><span class="sxs-lookup"><span data-stu-id="e2871-106">To start to develop your e-Commerce site, you must first establish a new site in the site authoring environment.</span></span> <span data-ttu-id="e2871-107">قبل أن تتمكن من إنشاء موقع جديد، يجب إنشاء متجر واحد على الأقل على الإنترنت في Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="e2871-107">Before you can create a new site, at least one online store must be created in Dynamics 365 Retail.</span></span> 

## <a name="set-up-your-site"></a><span data-ttu-id="e2871-108">إعداد موقعك</span><span class="sxs-lookup"><span data-stu-id="e2871-108">Set up your site</span></span>

<span data-ttu-id="e2871-109">لإعداد موقعك ، قم بما يلي.</span><span class="sxs-lookup"><span data-stu-id="e2871-109">To set up your site, do the following.</span></span>

1. <span data-ttu-id="e2871-110">في Microsoft Lifecycle Services (LCS)، حدد الارتباط الخاص ببيئة تأليف الموقع.</span><span class="sxs-lookup"><span data-stu-id="e2871-110">In Microsoft Lifecycle Services (LCS), select the link for the site authoring environment.</span></span> 
1. <span data-ttu-id="e2871-111">في الصفحة الرئيسية لبيئة تأليف الموقع، حدد **موقع جديد**.</span><span class="sxs-lookup"><span data-stu-id="e2871-111">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="e2871-112">في مربع الحوار **موقع جديد** ، أدخل المعلومات التالية.</span><span class="sxs-lookup"><span data-stu-id="e2871-112">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="e2871-113">الحقل</span><span class="sxs-lookup"><span data-stu-id="e2871-113">Field</span></span>                               | <span data-ttu-id="e2871-114">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="e2871-114">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="e2871-115">اسم الموقع</span><span class="sxs-lookup"><span data-stu-id="e2871-115">Site name</span></span>                           | <span data-ttu-id="e2871-116">أدخل اسم العرض الذي يجب استخدامه لموقعك في بيئة تأليف الموقع.</span><span class="sxs-lookup"><span data-stu-id="e2871-116">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="e2871-117">هذا الاسم مرئي فقط في بيئة التأليف ولن يتم عرضه للعملاء.</span><span class="sxs-lookup"><span data-stu-id="e2871-117">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="e2871-118">مجموعة أمان مسؤول الموقع</span><span class="sxs-lookup"><span data-stu-id="e2871-118">Site administrator's security group</span></span> | <span data-ttu-id="e2871-119">حدد مجموعه أمان Microsoft Azure Active Directory (Azure AD) التي تدير المستخدمين الذين لديهم دور مسؤول الموقع في هذا الموقع.</span><span class="sxs-lookup"><span data-stu-id="e2871-119">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="e2871-120">القناة الافتراضية (رقم وحدة التشغيل)</span><span class="sxs-lookup"><span data-stu-id="e2871-120">Default channel (operating unit number)</span></span> | <span data-ttu-id="e2871-121">حدد المتجر على الإنترنت الذي سيكون هذا الموقع بمثابة واجهة الويب له.</span><span class="sxs-lookup"><span data-stu-id="e2871-121">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="e2871-122">إذا كنت تريد أن يدعم موقع التجارة الإلكترونية الخاص بك العديد من المتاجر عبر الإنترنت، يجب عليك ربط المخازن بموقعك في **إعدادات الموقع** بعد إعداد الموقع.</span><span class="sxs-lookup"><span data-stu-id="e2871-122">If you want your e-Commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="e2871-123">اللغة الافتراضية</span><span class="sxs-lookup"><span data-stu-id="e2871-123">Default language</span></span>                            | <span data-ttu-id="e2871-124">حدد اللغة الافتراضية لهذا المتجر والسوق عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="e2871-124">Specify the default language for this online store and market.</span></span> <span data-ttu-id="e2871-125">يمكن لمتجر على الإنترنت دعم لغات متعددة.</span><span class="sxs-lookup"><span data-stu-id="e2871-125">An online store can support multiple languages.</span></span> <span data-ttu-id="e2871-126">إذا كنت ترغب في دعم لغات متعددة لهذا المتجر عبر الإنترنت أو متجر آخر على الإنترنت، يمكنك تكوين هذا الدعم في **إعدادات الموقع** بعد إعداد الموقع.</span><span class="sxs-lookup"><span data-stu-id="e2871-126">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="e2871-127">مجال</span><span class="sxs-lookup"><span data-stu-id="e2871-127">Domain</span></span>                              | <span data-ttu-id="e2871-128">حدد اسم المجال الذي سيكون بمثابة مجال لهذا المتجر عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="e2871-128">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="e2871-129">إذا لم تقم بتكوين أي نطاقات في LCS، يمكنك ترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="e2871-129">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="e2871-130">بعد تكوين المجال الخاص بك في LCS، يجب عليك إضافته إلى متجرك عبر الإنترنت في **إعدادات الموقع**.</span><span class="sxs-lookup"><span data-stu-id="e2871-130">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="e2871-131">المسار</span><span class="sxs-lookup"><span data-stu-id="e2871-131">Path</span></span>                              | <span data-ttu-id="e2871-132">عندما يدعم موقعك أكثر من لغة واحدة لاسم مجال معين، استخدم حقل المسار لإنشاء عنوان URL فريد للموقع لهذا المجال ومجموعة اللغة.</span><span class="sxs-lookup"><span data-stu-id="e2871-132">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="e2871-133">إذا كانت اللغة التي حددتها في حقل **اللغة الافتراضية** هي اللغة الوحيدة التي ستدعمها لهذا المجال، أو ستظل هي اللغة الافتراضية بعد ترجمة موقعك إلى لغات إضافية، نوصي أن تترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="e2871-133">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="e2871-134">بعد إنشاء موقعك، يمكنك التحقق من ارتباطه بمتجرك عبر الإنترنت من خلال تحديد علامة التبويب **المنتجات** . ينبغي عليك الاطلاع على مجموعة متنوعة من المنتجات التي تم تخصيصها لمتجر على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="e2871-134">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="e2871-135">يمكنك أيضًا استخدام القائمة المنسدلة في أعلى يمين الصفحة للوصول إلى المنتجات المخصصة حسب الفئة.</span><span class="sxs-lookup"><span data-stu-id="e2871-135">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e2871-136">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="e2871-136">Additional resources</span></span>

[<span data-ttu-id="e2871-137">نظرة عامة على المتجر على الإنترنت</span><span class="sxs-lookup"><span data-stu-id="e2871-137">Online store overview</span></span>](online-store-overview.md)

[<span data-ttu-id="e2871-138">نشر موقع تجارة إلكترونية جديد</span><span class="sxs-lookup"><span data-stu-id="e2871-138">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="e2871-139">إقران موقع عبر الإنترنت بقناة</span><span class="sxs-lookup"><span data-stu-id="e2871-139">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="e2871-140">تكوين اسم مجالك</span><span class="sxs-lookup"><span data-stu-id="e2871-140">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="e2871-141">إضافة الدعم إلى شبكة تسليم المحتوى (CDN)</span><span class="sxs-lookup"><span data-stu-id="e2871-141">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="e2871-142">تمكين اكتشاف المتجر استنادًا إلى الموقع</span><span class="sxs-lookup"><span data-stu-id="e2871-142">Enable location-based store detection</span></span>](enable-store-detection.md)

[<span data-ttu-id="e2871-143">إعداد صفحات مخصصة لعمليات تسجيل دخول المستخدمين</span><span class="sxs-lookup"><span data-stu-id="e2871-143">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="e2871-144">نظرة عامة على صفحة التأليف الرئيسية</span><span class="sxs-lookup"><span data-stu-id="e2871-144">Authoring home page overview</span></span>](authoring-home-overview.md)

[<span data-ttu-id="e2871-145">إضافة صفحة موقع جديدة</span><span class="sxs-lookup"><span data-stu-id="e2871-145">Add a new site page</span></span>](add-new-page.md)
