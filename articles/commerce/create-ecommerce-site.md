---
title: إنشاء موقع تجارة إلكترونية
description: يوضح هذا الموضوع الخطوات والمعلومات المطلوبة لإنشاء موقع جديد للتجارة الإلكترونية في منشئ مواقع Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 61fe44df7165780be2dd00be3f210ab2da05ddfe
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795777"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="b2980-103">إنشاء موقع تجارة إلكترونية</span><span class="sxs-lookup"><span data-stu-id="b2980-103">Create an e-commerce site</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b2980-104">يوضح هذا الموضوع الخطوات والمعلومات المطلوبة لإنشاء موقع جديد للتجارة الإلكترونية في منشئ مواقع Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b2980-104">This topic describes the steps and information required to create a new e-commerce site in Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="b2980-105">عندما تقوم بترخيص إمكانات Dynamics 365 Commerce ، سيتم تزويد منشئ المواقع بموقع بدء يمكنك استخدامه كأساس لموقعك الخاص.</span><span class="sxs-lookup"><span data-stu-id="b2980-105">When you license the Dynamics 365 Commerce capabilities, site builder will be provisioned with a starter site that you can use as a basis for your own site.</span></span> <span data-ttu-id="b2980-106">مع ذلك، إذا أردت البدء من البداية أو إذا كنت تريد إنشاء موقع ثان، ستحتاج إلى إنشاء موقع جديد في بيئة تأليف الموقع.</span><span class="sxs-lookup"><span data-stu-id="b2980-106">However, if you want to start from scratch or if you want to establish a second site, you will need to establish a new site in the site authoring environment.</span></span> 

## <a name="set-up-your-site"></a><span data-ttu-id="b2980-107">إعداد موقعك</span><span class="sxs-lookup"><span data-stu-id="b2980-107">Set up your site</span></span>

<span data-ttu-id="b2980-108">لإعداد موقعك ، قم بما يلي.</span><span class="sxs-lookup"><span data-stu-id="b2980-108">To set up your site, do the following.</span></span>

1. <span data-ttu-id="b2980-109">افتح بيئة منشئ المواقع.</span><span class="sxs-lookup"><span data-stu-id="b2980-109">Open the site builder environment.</span></span> <span data-ttu-id="b2980-110">يمكنك العثور على ارتباط لمنشئ المواقع في Microsoft Lifecycle Services (LCS) في صفحة ميزات البيئة الخاصة بالتجارة.</span><span class="sxs-lookup"><span data-stu-id="b2980-110">You can find a link to site builder in Microsoft Lifecycle Services (LCS) in the environment features page for Commerce.</span></span>
1. <span data-ttu-id="b2980-111">في الصفحة الرئيسية لبيئة تأليف الموقع، حدد **موقع جديد**.</span><span class="sxs-lookup"><span data-stu-id="b2980-111">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="b2980-112">في مربع الحوار **موقع جديد** ، أدخل المعلومات التالية.</span><span class="sxs-lookup"><span data-stu-id="b2980-112">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="b2980-113">الحقل</span><span class="sxs-lookup"><span data-stu-id="b2980-113">Field</span></span>                               | <span data-ttu-id="b2980-114">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="b2980-114">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="b2980-115">اسم الموقع</span><span class="sxs-lookup"><span data-stu-id="b2980-115">Site name</span></span>                           | <span data-ttu-id="b2980-116">أدخل اسم العرض الذي يجب استخدامه لموقعك في بيئة تأليف الموقع.</span><span class="sxs-lookup"><span data-stu-id="b2980-116">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="b2980-117">هذا الاسم مرئي فقط في بيئة التأليف ولن يتم عرضه للعملاء.</span><span class="sxs-lookup"><span data-stu-id="b2980-117">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="b2980-118">مجموعة أمان مسؤول الموقع</span><span class="sxs-lookup"><span data-stu-id="b2980-118">Site administrator's security group</span></span> | <span data-ttu-id="b2980-119">حدد مجموعه أمان Microsoft Azure Active Directory (Azure AD) التي تدير المستخدمين الذين لديهم دور مسؤول الموقع في هذا الموقع.</span><span class="sxs-lookup"><span data-stu-id="b2980-119">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="b2980-120">القناة الافتراضية (رقم وحدة التشغيل)</span><span class="sxs-lookup"><span data-stu-id="b2980-120">Default channel (operating unit number)</span></span> | <span data-ttu-id="b2980-121">حدد المتجر على الإنترنت الذي سيكون هذا الموقع بمثابة واجهة الويب له.</span><span class="sxs-lookup"><span data-stu-id="b2980-121">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="b2980-122">إذا كنت تريد أن يدعم موقع التجارة الإلكترونية الخاص بك العديد من المتاجر عبر الإنترنت، يجب عليك ربط المتاجر بموقعك في **إعدادات الموقع** بعد إعداد الموقع.</span><span class="sxs-lookup"><span data-stu-id="b2980-122">If you want your e-commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="b2980-123">اللغة الافتراضية</span><span class="sxs-lookup"><span data-stu-id="b2980-123">Default language</span></span>                            | <span data-ttu-id="b2980-124">حدد اللغة الافتراضية لهذا المتجر والسوق عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="b2980-124">Specify the default language for this online store and market.</span></span> <span data-ttu-id="b2980-125">يمكن لمتجر على الإنترنت دعم لغات متعددة.</span><span class="sxs-lookup"><span data-stu-id="b2980-125">An online store can support multiple languages.</span></span> <span data-ttu-id="b2980-126">إذا كنت ترغب في دعم لغات متعددة لهذا المتجر عبر الإنترنت أو متجر آخر على الإنترنت، يمكنك تكوين هذا الدعم في **إعدادات الموقع** بعد إعداد الموقع.</span><span class="sxs-lookup"><span data-stu-id="b2980-126">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="b2980-127">مجال</span><span class="sxs-lookup"><span data-stu-id="b2980-127">Domain</span></span>                              | <span data-ttu-id="b2980-128">حدد اسم المجال الذي سيكون بمثابة مجال لهذا المتجر عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="b2980-128">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="b2980-129">إذا لم تقم بتكوين أي نطاقات في LCS، يمكنك ترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="b2980-129">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="b2980-130">بعد تكوين المجال الخاص بك في LCS، يجب عليك إضافته إلى متجرك عبر الإنترنت في **إعدادات الموقع**.</span><span class="sxs-lookup"><span data-stu-id="b2980-130">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="b2980-131">المسار</span><span class="sxs-lookup"><span data-stu-id="b2980-131">Path</span></span>                              | <span data-ttu-id="b2980-132">عندما يدعم موقعك أكثر من لغة واحدة لاسم مجال معين، استخدم حقل المسار لإنشاء عنوان URL فريد للموقع لهذا المجال ومجموعة اللغة.</span><span class="sxs-lookup"><span data-stu-id="b2980-132">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="b2980-133">إذا كانت اللغة التي حددتها في حقل **اللغة الافتراضية** هي اللغة الوحيدة التي ستدعمها لهذا المجال، أو ستظل هي اللغة الافتراضية بعد ترجمة موقعك إلى لغات إضافية، نوصي أن تترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="b2980-133">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="b2980-134">بعد إنشاء موقعك، يمكنك التحقق من ارتباطه بمتجرك عبر الإنترنت من خلال تحديد علامة التبويب **المنتجات** . ينبغي عليك الاطلاع على مجموعة متنوعة من المنتجات التي تم تخصيصها لمتجر على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="b2980-134">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="b2980-135">يمكنك أيضًا استخدام القائمة المنسدلة في أعلى يمين الصفحة للوصول إلى المنتجات المخصصة حسب الفئة.</span><span class="sxs-lookup"><span data-stu-id="b2980-135">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b2980-136">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="b2980-136">Additional resources</span></span>

[<span data-ttu-id="b2980-137">تكوين اسم مجالك</span><span class="sxs-lookup"><span data-stu-id="b2980-137">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="b2980-138">نشر مستأجر التجارة الإلكترونية الجديد</span><span class="sxs-lookup"><span data-stu-id="b2980-138">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="b2980-139">إقران موقع Dynamics 365 Commerce بقناة عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="b2980-139">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="b2980-140">إدارة ملفات robots.txt</span><span class="sxs-lookup"><span data-stu-id="b2980-140">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="b2980-141">تحميل عناوين URL لإعادة التوجيه‬ بشكل مجمع</span><span class="sxs-lookup"><span data-stu-id="b2980-141">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="b2980-142">إعداد مستأجر B2C في Commerce</span><span class="sxs-lookup"><span data-stu-id="b2980-142">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="b2980-143">إعداد صفحات مخصصة لعمليات تسجيل دخول المستخدمين</span><span class="sxs-lookup"><span data-stu-id="b2980-143">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="b2980-144">تكوين مستأجرين متعددين لمتاجرة عمل-مستهلك في بيئة Commerce</span><span class="sxs-lookup"><span data-stu-id="b2980-144">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="b2980-145">إضافة الدعم إلى شبكة تسليم المحتوى (CDN)</span><span class="sxs-lookup"><span data-stu-id="b2980-145">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="b2980-146">تمكين اكتشاف المتجر استنادًا إلى الموقع</span><span class="sxs-lookup"><span data-stu-id="b2980-146">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]