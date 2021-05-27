---
title: نظرة عامة حول موقع التجارة الالكترونية
description: يقدم هذا الموضوع نظرة عامة حول دعم مواقع التجارة الإلكترونية في Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 55c40029082e49c1fbc9d9d5e9361218e5ddc5a0
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022462"
---
# <a name="e-commerce-site-overview"></a><span data-ttu-id="87b8c-103">نظره عامه حول موقع التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="87b8c-103">E-commerce site overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="87b8c-104">يقدم هذا الموضوع نظرة عامة حول دعم مواقع التجارة الإلكترونية في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="87b8c-104">This topic provides an overview of the support for e-commerce sites in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="87b8c-105">وهو يتضمن معلومات حول كيفية تهيئة وإدارة متاجر التجارة الإلكترونية عبر الإنترنت في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="87b8c-105">It includes information about how e-commerce online stores are initialized and managed in Dynamics 365 Commerce.</span></span> <span data-ttu-id="87b8c-106">كما يوفر روابط لمزيد من المعلومات حول المتاجر عبر الإنترنت، وحول كيفية إعداد موقع التجارة الإلكترونية وتكوينه.</span><span class="sxs-lookup"><span data-stu-id="87b8c-106">It also provides links to more information about online stores, and about how to set up and configure an e-commerce site.</span></span> <span data-ttu-id="87b8c-107">على الرغم من أن هذا الموضوع يغطي العديد من الأساسيات، إلا أنه لا يغطي كل ما هو مطلوب لإنشاء موقع تجارة إلكترونية للإنتاج.</span><span class="sxs-lookup"><span data-stu-id="87b8c-107">Although this topic covers many of the basics, it doesn't cover everything that is required to set up a production e-commerce site.</span></span> <span data-ttu-id="87b8c-108">يمكن الاطلاع علي مواضيع أكثر تقدمًا في وثائق Dynamics 365 Commerce .</span><span class="sxs-lookup"><span data-stu-id="87b8c-108">More advanced topics can be found in the Dynamics 365 Commerce documentation.</span></span>

## <a name="online-store-channel"></a><span data-ttu-id="87b8c-109">قناة متجر عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="87b8c-109">Online store channel</span></span>

<span data-ttu-id="87b8c-110">قبل أن تتمكن من إنشاء موقعك في Dynamics 365 Commerce، فإنه يجب إنشاء قناة متجر واحدة عبر الإنترنت على الأقل.</span><span class="sxs-lookup"><span data-stu-id="87b8c-110">Before you can build your site in Dynamics 365 Commerce, at least one online store channel must be set up.</span></span> <span data-ttu-id="87b8c-111">لمزيد من المعلومات، راجع [إعداد قناة عبر الإنترنت](channel-setup-online.md).</span><span class="sxs-lookup"><span data-stu-id="87b8c-111">For more information, see [Set up an online channel](channel-setup-online.md).</span></span> 

<span data-ttu-id="87b8c-112">في Dynamics 365 Commerce، يمكنك استخدام قناة متجر عبر الإنترنت لإنشاء المنتجات والتسعير واللغات وطرق الدفع وأوضاع التسليم ومراكز الاستيفاء وغيرها من الجوانب الخاصة بتجربة الإنترنت التي ينبغي أن تكون متاحة لعملائك.</span><span class="sxs-lookup"><span data-stu-id="87b8c-112">In Dynamics 365 Commerce, you use an online store channel to establish the products, pricing, languages, payment methods, delivery modes, fulfillment centers, and other aspects of the online experience that should be available to your customers.</span></span>

<span data-ttu-id="87b8c-113">يجب إعداد قناة متجر واحد فقط عبر الإنترنت قبل أن تبدأ استخدام Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="87b8c-113">Only one online store channel has to be set up before you can get started with Dynamics 365 Commerce.</span></span> <span data-ttu-id="87b8c-114">ومع ذلك، يمكن أن يقدم موقع تجارة إلكترونية واحد تجربة عبر الإنترنت للعديد من المتاجر عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="87b8c-114">However, a single e-commerce site can provide the online experience for multiple online stores.</span></span> <span data-ttu-id="87b8c-115">على سبيل المثال، إذا تم إعداد العديد من المتاجر عبر الإنترنت لدعم مناطق جغرافية مختلفة، فإنه يمكن استخدام مجموعة واحدة من صفحات التجارة الإلكترونية لتوفير التجارب الفريدة التي يتم تعريفها بواسطة كل متجر.</span><span class="sxs-lookup"><span data-stu-id="87b8c-115">For example, if multiple online stores are set up to support different geographical regions, a single set of e-commerce pages can be used to provide the unique experiences that are defined by each store.</span></span> <span data-ttu-id="87b8c-116">لمزيد من المعلومات حول كيفية تكوين موقع لدعم العديد من المتاجر عبر الإنترنت، راجع [إقران موقع عبر الإنترنت بقناة](associate-site-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="87b8c-116">For more information about how to configure a site to support multiple online stores, see [Associate an online site with a channel](associate-site-online-store.md).</span></span>

<span data-ttu-id="87b8c-117">بعد إعداد متجر عبر الإنترنت، فإنه يمكن أن يقترن بالموقع Dynamics 365 Commerce الذي سيكون بمثابة واجهة المتجر عبر الإنترنت الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="87b8c-117">After an online store is set up, it can be associated with the Dynamics 365 Commerce site that will serve as your online storefront.</span></span> <span data-ttu-id="87b8c-118">لمزيد من المعلومات حول المتاجر عبر الإنترنت وكيفية إعدادها، راجع [إعداد متاجر عبر الإنترنت](/dynamics365/unified-operations/retail/online-stores).</span><span class="sxs-lookup"><span data-stu-id="87b8c-118">For more information about online stores and how to set them up, see [Set up online stores](/dynamics365/unified-operations/retail/online-stores).</span></span>

## <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="87b8c-119">نشر مستأجر التجارة الإلكترونية الجديد</span><span class="sxs-lookup"><span data-stu-id="87b8c-119">Deploy a new e-commerce tenant</span></span>

<span data-ttu-id="87b8c-120">تتم مطالبتك باسم المجال في أثناء تهيئة موقع التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="87b8c-120">During initialization of an e-commerce site, you're prompted for a domain name.</span></span> <span data-ttu-id="87b8c-121">لمزيد من المعلومات حول المجالات في Commerce، راجع [تكوين اسم المجال الخاص بك](configure-your-domain-name.md) و [المجالات ف Dynamics 365 Commerce](domains-commerce.md)</span><span class="sxs-lookup"><span data-stu-id="87b8c-121">For more information about domains in Commerce, see [Configure your domain name](configure-your-domain-name.md) and [Domains in Dynamics 365 Commerce](domains-commerce.md).</span></span> <span data-ttu-id="87b8c-122">لنشر مستاجر التجارة الإلكترونية الجديدة باستخدام [Microsoft Dynamics Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)،اتبع الخطوات الواردة في [نشر مستأجر تجارة إلكترونية جديد](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="87b8c-122">To deploy a new e-commerce tenant by using [Microsoft Dynamics Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide), follow the steps in [Deploy a new e-commerce tenant](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="87b8c-123">بعد إعداد مستأجر التجارة الإلكترونية في LCS، سيتم توفير ارتباط لمنشئ موقع Commerce.</span><span class="sxs-lookup"><span data-stu-id="87b8c-123">After your e-commerce tenant is set up in LCS, a link to Commerce site builder will be provided.</span></span> <span data-ttu-id="87b8c-124">يمكنك بعد ذلك استخدام منشئ موقع Commerce لتهيئة مواقع التجارة الإلكترونية وتكوينها.</span><span class="sxs-lookup"><span data-stu-id="87b8c-124">You can then use Commerce site builder to initialize and configure your e-commerce sites.</span></span>

## <a name="initialize-your-e-commerce-site"></a><span data-ttu-id="87b8c-125">تهيئة موقع التجارة الإلكترونية الخاص بك</span><span class="sxs-lookup"><span data-stu-id="87b8c-125">Initialize your e-commerce site</span></span>

<span data-ttu-id="87b8c-126">عند بدء تشغيل منشئ موقع Commerce من LCS، تظهر صفحة **المواقع** .</span><span class="sxs-lookup"><span data-stu-id="87b8c-126">When you start Commerce site builder from LCS, the **Sites** page appears.</span></span> <span data-ttu-id="87b8c-127">تتضمن هذه الصفحة موقعين مكونين مسبقًا، **افتراضي** و **fabrikam**، كما هو موضح في المثال الموضح في التوضيح التالي.</span><span class="sxs-lookup"><span data-stu-id="87b8c-127">This page includes two preconfigured sites, **default** and **fabrikam**, as shown in the example in the following illustration.</span></span>

![صفحه المواقع في منشئ موقع Commerce](media/e-commerce-site-01.png)

<span data-ttu-id="87b8c-129">عند تحديد أحد هذه المواقع، تتم مطالبتك بتحديد اسم المجال وقناه المتجر الافتراضية عبر الإنترنت واللغة المعتمدة للقناة المحددة والمسار.</span><span class="sxs-lookup"><span data-stu-id="87b8c-129">When you select one of these sites, you're prompted to select a domain name, a default online store channel, a supported language for the selected channel, and a path.</span></span> <span data-ttu-id="87b8c-130">في حالة استخدام قناة واحدة فقط، يمكنك ترك المسار فارغًا.</span><span class="sxs-lookup"><span data-stu-id="87b8c-130">If only one channel is used, you can leave the path blank.</span></span> <span data-ttu-id="87b8c-131">يمكن تكوين المزيد من قنوات المتاجر عبر الإنترنت أو اللغات فيما بعد في منشئ موقع Commerce.</span><span class="sxs-lookup"><span data-stu-id="87b8c-131">More online store channels or languages can be configured later in Commerce site builder.</span></span> <span data-ttu-id="87b8c-132">ستتطلب كل قناه أو لغة إضافية مسارًا فريدًا.</span><span class="sxs-lookup"><span data-stu-id="87b8c-132">Each additional channel or language will require a unique path.</span></span> <span data-ttu-id="87b8c-133">علي سبيل المثال، يوجد لديك قناتان عبر الإنترنت مقترنتان بموقع واحد، واسم المجال للموقع هو `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="87b8c-133">For example, you have two online channels that are associated with a single site, and the domain name for the site is `www.fabrikam.com`.</span></span> <span data-ttu-id="87b8c-134">في هذه الحالة، يمكن أن يكون مسار أحدي القنوات هو القيمة الافتراضية التي ليس لها مسار (`https://www.fabrikam.com`)، ويمكن تعيين القناة الثانية إلى مسار جديد، مثل **site2** ، والذي سيكون له عنوان URL `https://www.fabrikam.com/site2`.</span><span class="sxs-lookup"><span data-stu-id="87b8c-134">In this case, the path for one channel can be the default value that has no path (`https://www.fabrikam.com`), and the second channel can be set to a new path, such as **site2**, that will have the URL `https://www.fabrikam.com/site2`.</span></span> <span data-ttu-id="87b8c-135">يبين الرسم التوضيحي التالي مثالاً لمربع حوار تهيئة الموقع في منشئ موقع Commerce.</span><span class="sxs-lookup"><span data-stu-id="87b8c-135">The following illustration shows an example of a site initialization dialog box in Commerce site builder.</span></span>

![مربع حوار تهيئة الموقع في منشئ موقع Commerce](media/e-commerce-site-02.png)

<span data-ttu-id="87b8c-137">تتضمن صفحة **المواقع** أيضًا زر **موقع جديد** .</span><span class="sxs-lookup"><span data-stu-id="87b8c-137">The **Sites** page also includes a **New site** button.</span></span> <span data-ttu-id="87b8c-138">إن مربع الحوار الذي يظهر عند تحديد هذا الزر يشابه مربع حوار تهيئة الموقع، ولكنه يُستخدم لإنشاء موقع جديد.</span><span class="sxs-lookup"><span data-stu-id="87b8c-138">The dialog box that appears when you select this button resembles the site initialization dialog box, but it's used to create a new site.</span></span> <span data-ttu-id="87b8c-139">المواقع الجديدة فارغة.</span><span class="sxs-lookup"><span data-stu-id="87b8c-139">New sites are blank.</span></span> <span data-ttu-id="87b8c-140">ولا تتضمن نفس القوالب والأجزاء والصفحات والصور الافتراضية التي يتم توفيرها مع الموقعين **الافتراضي** والخاص بـ **fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="87b8c-140">They don't include the same default templates, fragments, pages, and images that are provided with the **default** and **fabrikam** sites.</span></span> <span data-ttu-id="87b8c-141">ومع ذلك، وكما هو مطلوب، يمكنك فتح بطاقة دعم لطلب إضافة نسخة من المحتوي الافتراضي إلى موقع جديد فارغ.</span><span class="sxs-lookup"><span data-stu-id="87b8c-141">However, as you require, you can open a support ticket to request that a copy of the default content be added to a new blank site.</span></span> <span data-ttu-id="87b8c-142">لمزيد من المعلومات، راجع [إنشاء موقع التجارة الإلكترونية](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="87b8c-142">For more information, see [Create an e-commerce site](create-ecommerce-site.md).</span></span>

<span data-ttu-id="87b8c-143">بعد تهيئة موقع جديد، تظهر صفحة **الصفحة الرئيسية** لمنشئ موقع Commerce .</span><span class="sxs-lookup"><span data-stu-id="87b8c-143">After a new site is initialized, the Commerce site builder **Home** page appears.</span></span> <span data-ttu-id="87b8c-144">تتضمن هذه الصفحة ارتباطات لمحتوي الإجراءات العامة ومحتوي الدليل، كما هو موضح في المثال الموجود في التوضيح التالي.</span><span class="sxs-lookup"><span data-stu-id="87b8c-144">This page includes links to common actions and guidance content, as shown in the example in the following illustration.</span></span>

![الارتباطات علي الصفحة الرئيسية في منشئ موقع Commerce](media/e-commerce-site-03.png)

## <a name="modify-online-store-channels-or-add-online-store-channels-to-an-e-commerce-site"></a><span data-ttu-id="87b8c-146">تعديل قنوات المتجر علي الإنترنت أو إضافة قنوات متجر عبر الإنترنت إلى موقع التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="87b8c-146">Modify online store channels or add online store channels to an e-commerce site</span></span>

<span data-ttu-id="87b8c-147">بعد إنشاء موقع التجارة الإلكترونية، يمكنك تغيير القناة المقترنة بها باتباع الخطوات الموجودة في [اقتران موقع التجارة الإلكترونية بقناة عبر الإنترنت](associate-site-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="87b8c-147">After an e-commerce site is created, you can change the channel that it's associated with by following the steps in [Associate an e-commerce site with an online channel](associate-site-online-store.md).</span></span> <span data-ttu-id="87b8c-148">يبين المثال في الرسم التوضيحي التالي كيف يمكن تغيير رقم وحدة تشغيل القناة (OUN) في صفحة **القنوات** (**إعدادات القناة \> القنوات**).</span><span class="sxs-lookup"><span data-stu-id="87b8c-148">The example in the following illustration shows how a channel operating unit number (OUN) can be changed on the **Channels** page (**Site settings \> Channels**).</span></span> <span data-ttu-id="87b8c-149">بعد الانتهاء من إجراء تغيير، تأكد من تحديد **حفظ ونشر**.</span><span class="sxs-lookup"><span data-stu-id="87b8c-149">After you've finished making a change, be sure to select **Save and publish**.</span></span> <span data-ttu-id="87b8c-150">وبهذه الطريقة، سوف تتأكد من أنه تم نشر التغيير.</span><span class="sxs-lookup"><span data-stu-id="87b8c-150">In this way, you ensure that the change is published.</span></span>

![صفحة القنوات في منشئ موقع Commerce](media/e-commerce-site-04.png)

<span data-ttu-id="87b8c-152">يمكنك إضافة قنوات جديدة عن طريق تحديد **إضافة قناة**.</span><span class="sxs-lookup"><span data-stu-id="87b8c-152">You can add new channels by selecting **Add a channel**.</span></span> <span data-ttu-id="87b8c-153">لإضافة لغات جديدة إلى قناة، حدد القناة، ثم حدد **إضافة لغة محلية** في مربع حوار القناة الذي يظهر.</span><span class="sxs-lookup"><span data-stu-id="87b8c-153">To add new languages to a channel, select the channel, and then select **Add a locale** in the channel dialog box that appears.</span></span> <span data-ttu-id="87b8c-154">قبل أن تظهر اللغات المحلية في مربع الحوار، يتعين تكوينها مسبقًا لقناة المتجر عبر الإنترنت في المراكز الرئيسية لـ Commerce.</span><span class="sxs-lookup"><span data-stu-id="87b8c-154">Before locales can appear in the dialog box, they must be preconfigured for the online store channel in Commerce headquarters.</span></span>

![مربع حوار قناة في منشئ موقع Commerce](media/e-commerce-site-05.png)

## <a name="set-up-an-azure-b2c-tenant"></a><span data-ttu-id="87b8c-156">إعداد مستأجر Azure B2C</span><span class="sxs-lookup"><span data-stu-id="87b8c-156">Set up an Azure B2C tenant</span></span>

<span data-ttu-id="87b8c-157">يقوم Dynamics 365 Commerce باستخدام Azure Active Directory (Azure AD) العمل-إلى-المستهلك (B2C) لدعم بيانات اعتماد المستخدم وتدفقات المصادقة.</span><span class="sxs-lookup"><span data-stu-id="87b8c-157">Dynamics 365 Commerce uses Azure Active Directory (Azure AD) business-to-consumer (B2C) to support user credential and authentication flows.</span></span> <span data-ttu-id="87b8c-158">للحصول علي معلومات حول كيفية إعداد مستأجر Azure B2C، راجع [إعداد مستاجر B2C في Commerce](set-up-b2c-tenant.md)، [وإعداد صفحات مخصصة لوظائف تسجيل الدخول الخاصة بالمستخدمين](custom-pages-user-logins.md)، و [تكوين العديد من مستأجري B2C في بيئة Commerce](configure-multi-b2c-tenants.md).</span><span class="sxs-lookup"><span data-stu-id="87b8c-158">For information about how to set up your Azure B2C tenant, see [Set up a B2C tenant in Commerce](set-up-b2c-tenant.md), [Set up custom pages for user sign-ins](custom-pages-user-logins.md), and [Configure multiple B2C tenants in a Commerce environment](configure-multi-b2c-tenants.md).</span></span>

## <a name="overview-of-the-default-site-pages"></a><span data-ttu-id="87b8c-159">نظرة عامة علي صفحات الموقع الافتراضية</span><span class="sxs-lookup"><span data-stu-id="87b8c-159">Overview of the default site pages</span></span>

<span data-ttu-id="87b8c-160">تتضمن المواقع **الافتراضية** و **abrikam** قوالب وأجزاء وصفحات مكونة مسبقًا لمساعدتك علي البدء.</span><span class="sxs-lookup"><span data-stu-id="87b8c-160">The **default** and **fabrikam** sites include preconfigured templates, fragments, and pages to help you get started.</span></span> <span data-ttu-id="87b8c-161">لمزيد من المعلومات، راجع الموضوعات التالية:</span><span class="sxs-lookup"><span data-stu-id="87b8c-161">For more information, see the following topics:</span></span>

- [<span data-ttu-id="87b8c-162">نظرة عامة على الصفحة الرئيسية</span><span class="sxs-lookup"><span data-stu-id="87b8c-162">Home page overview</span></span>](quick-tour-home-page.md)
- [<span data-ttu-id="87b8c-163">نظرة عامة على صفحة تفاصيل المنتج</span><span class="sxs-lookup"><span data-stu-id="87b8c-163">Product details page overview</span></span>](quick-tour-pdp.md)
- [<span data-ttu-id="87b8c-164">نظرة عامة على صفحات سلة التسوق والسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="87b8c-164">Cart and checkout pages overview</span></span>](quick-tour-cart-checkout.md)
- [<span data-ttu-id="87b8c-165">نظرة عامة على صفحات إدارة الحسابات</span><span class="sxs-lookup"><span data-stu-id="87b8c-165">Account management pages overview</span></span>](quick-tour-account-management.md)

## <a name="manage-site-settings"></a><span data-ttu-id="87b8c-166">إدارة إعدادات الموقع</span><span class="sxs-lookup"><span data-stu-id="87b8c-166">Manage site settings</span></span>

<span data-ttu-id="87b8c-167">لمزيد من المعلومات حول كيفية إدارة إعداد موقعك، راجع المواضيع التالية:</span><span class="sxs-lookup"><span data-stu-id="87b8c-167">For information about how to manage your site settings, see the following topics:</span></span>

- [<span data-ttu-id="87b8c-168">إدارة المستخدمين والأدوار في التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="87b8c-168">Manage e-commerce users and roles</span></span>](manage-ecommerce-users-roles.md)
- [<span data-ttu-id="87b8c-169">اعتبارات تحسين محرك البحث (SEO) لموقعك</span><span class="sxs-lookup"><span data-stu-id="87b8c-169">Search engine optimization (SEO) considerations for your site</span></span>](/search-engine-optimization-considerations.md)
- [<span data-ttu-id="87b8c-170">إدارة سياسة أمان المحتوى (CSP)</span><span class="sxs-lookup"><span data-stu-id="87b8c-170">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)
- [<span data-ttu-id="87b8c-171">تحديد سمة الموقع</span><span class="sxs-lookup"><span data-stu-id="87b8c-171">Select a site theme</span></span>](select-site-theme.md)

## <a name="manage-site-content"></a><span data-ttu-id="87b8c-172">إدارة محتوى الموقع</span><span class="sxs-lookup"><span data-stu-id="87b8c-172">Manage site content</span></span>

<span data-ttu-id="87b8c-173">لمزيد من المعلومات حول كيفية إدارة محتوى الموقع، راجع المواضيع التالية:</span><span class="sxs-lookup"><span data-stu-id="87b8c-173">For information about how to manage site content, see the following topics:</span></span>

- [<span data-ttu-id="87b8c-174">مصطلحات نموذج الصفحة</span><span class="sxs-lookup"><span data-stu-id="87b8c-174">Page model glossary</span></span>](page-elements-overview.md)
- [<span data-ttu-id="87b8c-175">حالات المستند ودورة الحياة</span><span class="sxs-lookup"><span data-stu-id="87b8c-175">Document states and lifecycle</span></span>](document-states-overview.md)
- [<span data-ttu-id="87b8c-176">القوالب والتخطيطات</span><span class="sxs-lookup"><span data-stu-id="87b8c-176">Templates and layout</span></span>](templates-layouts-overview.md)
- [<span data-ttu-id="87b8c-177">العمل باستخدام الأجزاء</span><span class="sxs-lookup"><span data-stu-id="87b8c-177">Work with fragments</span></span>](work-with-fragments.md)
- [<span data-ttu-id="87b8c-178">العمل باستخدام الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="87b8c-178">Work with modules</span></span>](work-with-modules.md)
- [<span data-ttu-id="87b8c-179">نظرة عامة على إدارة الأصول الرقمية</span><span class="sxs-lookup"><span data-stu-id="87b8c-179">Digital asset management overview</span></span>](dam-overview.md)
- [<span data-ttu-id="87b8c-180">نظرة عامة على مكتبة الوحدات</span><span class="sxs-lookup"><span data-stu-id="87b8c-180">Module library overview</span></span>](starter-kit-overview.md)

## <a name="additional-resources"></a><span data-ttu-id="87b8c-181">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="87b8c-181">Additional resources</span></span>

[<span data-ttu-id="87b8c-182">إنشاء موقع تجارة إلكترونية</span><span class="sxs-lookup"><span data-stu-id="87b8c-182">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="87b8c-183">نشر موقع تجارة إلكترونية جديد</span><span class="sxs-lookup"><span data-stu-id="87b8c-183">Deploy a new e-commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="87b8c-184">إقران موقع عبر الإنترنت بقناة</span><span class="sxs-lookup"><span data-stu-id="87b8c-184">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="87b8c-185">تكوين اسم مجالك</span><span class="sxs-lookup"><span data-stu-id="87b8c-185">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="87b8c-186">إضافة الدعم إلى شبكة تسليم المحتوى (CDN)</span><span class="sxs-lookup"><span data-stu-id="87b8c-186">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="87b8c-187">تمكين اكتشاف المتجر استنادًا إلى الموقع</span><span class="sxs-lookup"><span data-stu-id="87b8c-187">Enable location-based store detection</span></span>](enable-store-detection.md)

[<span data-ttu-id="87b8c-188">إعداد صفحات مخصصة لعمليات تسجيل دخول المستخدمين</span><span class="sxs-lookup"><span data-stu-id="87b8c-188">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]