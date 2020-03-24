---
title: إنشاء موقع تجارة إلكترونية
description: يوضح هذا الموضوع الخطوات والمعلومات المطلوبة لإنشاء موقع جديد للتجارة الإلكترونية في منشئ مواقع Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 03/02/2020
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
ms.openlocfilehash: 7177bae911dfa91a645b40581bf23b3ed76562a3
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096764"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="fb0ac-103">إنشاء موقع تجارة إلكترونية</span><span class="sxs-lookup"><span data-stu-id="fb0ac-103">Create an e-Commerce site</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="fb0ac-104">يوضح هذا الموضوع الخطوات والمعلومات المطلوبة لإنشاء موقع جديد للتجارة الإلكترونية في منشئ مواقع Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fb0ac-104">This topic describes the steps and information required to create a new e-Commerce site in Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="fb0ac-105">قبل البدء في إمكانية تطوير موقع التجارة الإلكترونية لديك، يجب أولاً إنشاء موقع جديد في منشئ مواقع.</span><span class="sxs-lookup"><span data-stu-id="fb0ac-105">Before you can start developing your e-Commerce site, you must first establish a new site in site builder.</span></span> 


<span data-ttu-id="fb0ac-106">لبدء تطوير موقع التجارة الإلكترونية الخاص بك، يجب عليك أولاً إنشاء موقع جديد في بيئة تأليف الموقع.</span><span class="sxs-lookup"><span data-stu-id="fb0ac-106">To start to develop your e-Commerce site, you must first establish a new site in the site authoring environment.</span></span> <span data-ttu-id="fb0ac-107">قبل أن تتمكن من إنشاء موقع جديد، يجب إنشاء متجر واحد على الأقل على الإنترنت في التجارة.</span><span class="sxs-lookup"><span data-stu-id="fb0ac-107">Before you can create a new site, at least one online store must be created in Commerce.</span></span> 


## <a name="set-up-your-site"></a><span data-ttu-id="fb0ac-108">إعداد موقعك</span><span class="sxs-lookup"><span data-stu-id="fb0ac-108">Set up your site</span></span>

<span data-ttu-id="fb0ac-109">لإعداد موقعك ، قم بما يلي.</span><span class="sxs-lookup"><span data-stu-id="fb0ac-109">To set up your site, do the following.</span></span>

1. <span data-ttu-id="fb0ac-110">افتح بيئة منشئ المواقع.</span><span class="sxs-lookup"><span data-stu-id="fb0ac-110">Open the site builder environment.</span></span> <span data-ttu-id="fb0ac-111">يمكنك العثور على ارتباط لمنشئ المواقع في Microsoft Lifecycle Services (LCS) في صفحة ميزات البيئة الخاصة بالتجارة.</span><span class="sxs-lookup"><span data-stu-id="fb0ac-111">You can find a link to site builder in Microsoft Lifecycle Services (LCS) in the environment features page for Commerce.</span></span>
1. <span data-ttu-id="fb0ac-112">في الصفحة الرئيسية لبيئة تأليف الموقع، حدد **موقع جديد**.</span><span class="sxs-lookup"><span data-stu-id="fb0ac-112">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="fb0ac-113">في مربع الحوار **موقع جديد** ، أدخل المعلومات التالية.</span><span class="sxs-lookup"><span data-stu-id="fb0ac-113">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="fb0ac-114">الحقل</span><span class="sxs-lookup"><span data-stu-id="fb0ac-114">Field</span></span>                               | <span data-ttu-id="fb0ac-115">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="fb0ac-115">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="fb0ac-116">اسم الموقع</span><span class="sxs-lookup"><span data-stu-id="fb0ac-116">Site name</span></span>                           | <span data-ttu-id="fb0ac-117">أدخل اسم العرض الذي يجب استخدامه لموقعك في بيئة تأليف الموقع.</span><span class="sxs-lookup"><span data-stu-id="fb0ac-117">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="fb0ac-118">هذا الاسم مرئي فقط في بيئة التأليف ولن يتم عرضه للعملاء.</span><span class="sxs-lookup"><span data-stu-id="fb0ac-118">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="fb0ac-119">مجموعة أمان مسؤول الموقع</span><span class="sxs-lookup"><span data-stu-id="fb0ac-119">Site administrator's security group</span></span> | <span data-ttu-id="fb0ac-120">حدد مجموعه أمان Microsoft Azure Active Directory (Azure AD) التي تدير المستخدمين الذين لديهم دور مسؤول الموقع في هذا الموقع.</span><span class="sxs-lookup"><span data-stu-id="fb0ac-120">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="fb0ac-121">القناة الافتراضية (رقم وحدة التشغيل)</span><span class="sxs-lookup"><span data-stu-id="fb0ac-121">Default channel (operating unit number)</span></span> | <span data-ttu-id="fb0ac-122">حدد المتجر على الإنترنت الذي سيكون هذا الموقع بمثابة واجهة الويب له.</span><span class="sxs-lookup"><span data-stu-id="fb0ac-122">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="fb0ac-123">إذا كنت تريد أن يدعم موقع التجارة الإلكترونية الخاص بك العديد من المتاجر عبر الإنترنت، يجب عليك ربط المخازن بموقعك في **إعدادات الموقع** بعد إعداد الموقع.</span><span class="sxs-lookup"><span data-stu-id="fb0ac-123">If you want your e-Commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="fb0ac-124">اللغة الافتراضية</span><span class="sxs-lookup"><span data-stu-id="fb0ac-124">Default language</span></span>                            | <span data-ttu-id="fb0ac-125">حدد اللغة الافتراضية لهذا المتجر والسوق عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="fb0ac-125">Specify the default language for this online store and market.</span></span> <span data-ttu-id="fb0ac-126">يمكن لمتجر على الإنترنت دعم لغات متعددة.</span><span class="sxs-lookup"><span data-stu-id="fb0ac-126">An online store can support multiple languages.</span></span> <span data-ttu-id="fb0ac-127">إذا كنت ترغب في دعم لغات متعددة لهذا المتجر عبر الإنترنت أو متجر آخر على الإنترنت، يمكنك تكوين هذا الدعم في **إعدادات الموقع** بعد إعداد الموقع.</span><span class="sxs-lookup"><span data-stu-id="fb0ac-127">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="fb0ac-128">مجال</span><span class="sxs-lookup"><span data-stu-id="fb0ac-128">Domain</span></span>                              | <span data-ttu-id="fb0ac-129">حدد اسم المجال الذي سيكون بمثابة مجال لهذا المتجر عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="fb0ac-129">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="fb0ac-130">إذا لم تقم بتكوين أي نطاقات في LCS، يمكنك ترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="fb0ac-130">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="fb0ac-131">بعد تكوين المجال الخاص بك في LCS، يجب عليك إضافته إلى متجرك عبر الإنترنت في **إعدادات الموقع**.</span><span class="sxs-lookup"><span data-stu-id="fb0ac-131">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="fb0ac-132">المسار</span><span class="sxs-lookup"><span data-stu-id="fb0ac-132">Path</span></span>                              | <span data-ttu-id="fb0ac-133">عندما يدعم موقعك أكثر من لغة واحدة لاسم مجال معين، استخدم حقل المسار لإنشاء عنوان URL فريد للموقع لهذا المجال ومجموعة اللغة.</span><span class="sxs-lookup"><span data-stu-id="fb0ac-133">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="fb0ac-134">إذا كانت اللغة التي حددتها في حقل **اللغة الافتراضية** هي اللغة الوحيدة التي ستدعمها لهذا المجال، أو ستظل هي اللغة الافتراضية بعد ترجمة موقعك إلى لغات إضافية، نوصي أن تترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="fb0ac-134">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="fb0ac-135">بعد إنشاء موقعك، يمكنك التحقق من ارتباطه بمتجرك عبر الإنترنت من خلال تحديد علامة التبويب **المنتجات** . ينبغي عليك الاطلاع على مجموعة متنوعة من المنتجات التي تم تخصيصها لمتجر على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="fb0ac-135">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="fb0ac-136">يمكنك أيضًا استخدام القائمة المنسدلة في أعلى يمين الصفحة للوصول إلى المنتجات المخصصة حسب الفئة.</span><span class="sxs-lookup"><span data-stu-id="fb0ac-136">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fb0ac-137">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="fb0ac-137">Additional resources</span></span>

[<span data-ttu-id="fb0ac-138">تكوين اسم مجالك</span><span class="sxs-lookup"><span data-stu-id="fb0ac-138">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="fb0ac-139">نشر موقع تجارة إلكترونية جديد</span><span class="sxs-lookup"><span data-stu-id="fb0ac-139">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="fb0ac-140">إعداد قناة متجر عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="fb0ac-140">Set up an online store channel</span></span>](online-stores.md)

[<span data-ttu-id="fb0ac-141">إقران موقع عبر الإنترنت بقناة</span><span class="sxs-lookup"><span data-stu-id="fb0ac-141">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="fb0ac-142">إدارة ملفات robots.txt</span><span class="sxs-lookup"><span data-stu-id="fb0ac-142">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="fb0ac-143">تحميل عناوين URL لإعادة التوجيه‬ بشكل مجمع</span><span class="sxs-lookup"><span data-stu-id="fb0ac-143">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="fb0ac-144">إعداد مستأجر B2C في Commerce</span><span class="sxs-lookup"><span data-stu-id="fb0ac-144">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="fb0ac-145">إعداد صفحات مخصصة لعمليات تسجيل دخول المستخدمين</span><span class="sxs-lookup"><span data-stu-id="fb0ac-145">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="fb0ac-146">تكوين مستأجرين متعددين لمتاجرة عمل-مستهلك في بيئة Commerce</span><span class="sxs-lookup"><span data-stu-id="fb0ac-146">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="fb0ac-147">إضافة الدعم إلى شبكة تسليم المحتوى (CDN)</span><span class="sxs-lookup"><span data-stu-id="fb0ac-147">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="fb0ac-148">تمكين اكتشاف المتجر استنادًا إلى الموقع</span><span class="sxs-lookup"><span data-stu-id="fb0ac-148">Enable location-based store detection</span></span>](enable-store-detection.md)
