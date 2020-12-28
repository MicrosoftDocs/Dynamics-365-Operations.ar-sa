---
title: المجالات في Dynamics 365 Commerce
description: يصف هذا الموضوع كيفية معالجة المجالات في Microsoft Dynamics 365 Commerce.
author: BrShoo
manager: AnnBe
ms.date: 09/03/2020
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
ms.author: BrShoo
ms.search.validFrom: ''
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: cb2b003168d32d05387bd45796d313736b11a41f
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517345"
---
# <a name="domains-in-dynamics-365-commerce"></a><span data-ttu-id="e3d68-103">المجالات في Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="e3d68-103">Domains in Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e3d68-104">يصف هذا الموضوع كيفية معالجة المجالات في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e3d68-104">This topic describes how domains are handled in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e3d68-105">المجالات هي عناوين ويب تُستخدم للانتقال إلى مواقع Dynamics 365 Commerce في مستعرض الويب.</span><span class="sxs-lookup"><span data-stu-id="e3d68-105">Domains are web addresses used to navigate to Dynamics 365 Commerce sites in a web browser.</span></span> <span data-ttu-id="e3d68-106">يمكنك التحكم في إدارة مجالك مع موفر خادم اسم مجال (DNS) تختاره.</span><span class="sxs-lookup"><span data-stu-id="e3d68-106">You control management of your domain with a chosen Domain Name Server (DNS) provider.</span></span> <span data-ttu-id="e3d68-107">يُشار إلى المجالات عبر منشئ المواقع في Dynamics 365 Commerce لتنسيق كيفية الوصول إلى الموقع عند نشره.</span><span class="sxs-lookup"><span data-stu-id="e3d68-107">Domains are referenced throughout Dynamics 365 Commerce site builder to coordinate how a site will be accessed when published.</span></span> <span data-ttu-id="e3d68-108">يراجع هذا الموضوع كيفية التعامل مع المجالات والإشارة اليها عبر دورة حياة تطوير موقع Commerce وتشغيله.</span><span class="sxs-lookup"><span data-stu-id="e3d68-108">This topic reviews how domains are handled and referenced throughout the lifecycle of the Commerce site development and launch.</span></span>

## <a name="provisioning-and-supported-host-names"></a><span data-ttu-id="e3d68-109">التزويد وأسماء الأجهزة المضيفة المدعومة‬‏‫</span><span class="sxs-lookup"><span data-stu-id="e3d68-109">Provisioning and supported host names</span></span>

<span data-ttu-id="e3d68-110">عند توفير بيئة تجارة إلكترونية في [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/)، يتم استخدام المربع **أسماء الأجهزة المضيفة المدعومة** على شاشة توفير التجارة الإلكترونية لإدخال مجالات سيتم ربطها ببيئة Commerce المنشورة.</span><span class="sxs-lookup"><span data-stu-id="e3d68-110">When provisioning an e-commerce environment in [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/), the **Supported host names** box on the e-commerce provisioning screen is used to enter domains that will be associated with the deployed Commerce environment.</span></span> <span data-ttu-id="e3d68-111">ستكون هذه المجالات أسماء خوادم أسماء المجالات (DNS) المخصصة للعملاء وستكون حيث ستتم استضافة مواقع الويب للتجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="e3d68-111">These domains will be the customer-facing Domain Name Server (DNS) names where e-commerce websites will be hosted.</span></span> <span data-ttu-id="e3d68-112">لا يؤدي إدخال مجال في هذه المرحلة إلى بدء تحويل حركة المرور للمجال إلى Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e3d68-112">Entering a domain at this stage does not start diverting traffic for the domain to Dynamics 365 Commerce.</span></span> <span data-ttu-id="e3d68-113">سيتم توجيه حركة المرور لمجال ما إلى نقطة نهاية Commerce فقط عند تحديث سجل DNS CNAME لاستخدام نقطة نهاية Commerce مع المجال.</span><span class="sxs-lookup"><span data-stu-id="e3d68-113">Traffic for a domain will only be routed to the Commerce endpoint when the DNS CNAME record is updated to use the Commerce endpoint with the domain.</span></span>

> [!NOTE]
> <span data-ttu-id="e3d68-114">يمكن إدخال مجالات متعددة في مربع **أسماء الأجهزة المضيفة المدعومة‬‏‫** وذلك بفصلها بفواصل منقوطة.</span><span class="sxs-lookup"><span data-stu-id="e3d68-114">Multiple domains can be entered into the **Supported host names** box by separating them with semi-colons.</span></span>

<span data-ttu-id="e3d68-115">يبين الرسم التوضيحي التالي شاشة توفير التجارة الإلكترونية في LCS مع تمييز المربع **أسماء الأجهزة المضيفة المدعومة**.</span><span class="sxs-lookup"><span data-stu-id="e3d68-115">The following illustration shows the LCS e-commerce provisioning screen with the **Supported host names** box highlighted.</span></span> 

![شاشة توفير التجارة الإلكترونية في LCS مع تمييز المربع **أسماء الأجهزة المضيفة المدعومة**](./media/Domains_ProvisioningeCommerceScreen.png)

<span data-ttu-id="e3d68-117">يمكنك إنشاء طلب خدمة لإضافة المزيد من المجالات إلى بيئة في حال كان التزويد قد حدث بالفعل.</span><span class="sxs-lookup"><span data-stu-id="e3d68-117">You can create a service request to add additional domains to an environment if provisioning has already occurred.</span></span> <span data-ttu-id="e3d68-118">لإنشاء طلب خدمة في LCS، انتقل في بيئتك إلى **الدعم \> مشاكل الدعم** وحدد **إرسال حادث**.</span><span class="sxs-lookup"><span data-stu-id="e3d68-118">To create a service request in LCS, within your environment go to **Support \> Support issues** and select **Submit an incident**.</span></span>

## <a name="commerce-generated-urls"></a><span data-ttu-id="e3d68-119">عناوين URL المنشأة من Commerce</span><span class="sxs-lookup"><span data-stu-id="e3d68-119">Commerce-generated URLs</span></span>

<span data-ttu-id="e3d68-120">عند توفير بيئة تجارة إلكترونية لـ Dynamics 365 Commerce ، سينشئ Commerce عنوان URL سوف يكون عنوان العمل الخاص بالبيئة.</span><span class="sxs-lookup"><span data-stu-id="e3d68-120">When provisioning a Dynamics 365 Commerce e-commerce environment, Commerce will generate a URL that will be the working address for the environment.</span></span> <span data-ttu-id="e3d68-121">يُشار إلى عنوان URL هذا في ارتباط موقع التجارة الإلكترونية الذي يظهر في LCS بعد توفير البيئة.</span><span class="sxs-lookup"><span data-stu-id="e3d68-121">This URL is referenced in the e-commerce site link shown in LCS after the environment is provisioned.</span></span> <span data-ttu-id="e3d68-122">يكون عنوان URL الذي يتم إنشائه في Commerce في تنسيق `https://<e-commerce tenant name>.commerce.dynamics.com`، حيث يكون اسم مستأجر التجارة الإلكترونية هو الاسم الذي تم إدخاله في LCS لبيئة Commerce.</span><span class="sxs-lookup"><span data-stu-id="e3d68-122">A Commerce-generated URL is in the format `https://<e-commerce tenant name>.commerce.dynamics.com`, where the e-commerce tenant name is the name entered in LCS for the Commerce environment.</span></span>

<span data-ttu-id="e3d68-123">يمكنك استخدام أسماء الأجهزة المضيفة لموقع الإنتاج في بيئة اختبار معزولة أيضًا.</span><span class="sxs-lookup"><span data-stu-id="e3d68-123">You can use production site host names in a sandbox environment as well.</span></span> <span data-ttu-id="e3d68-124">يعد هذا الخيار مثاليًا عندما تقوم بنسخ موقع من بيئة اختبار معزولة إلى بيئة إنتاج.</span><span class="sxs-lookup"><span data-stu-id="e3d68-124">This option is ideal when you will be copying a site from a sandbox environment to production.</span></span>

## <a name="site-setup"></a><span data-ttu-id="e3d68-125">إعداد الموقع</span><span class="sxs-lookup"><span data-stu-id="e3d68-125">Site setup</span></span>

<span data-ttu-id="e3d68-126">بعد توفير بيئة التجارة الإلكترونية الخاصة بك، يجب عليك إعداد موقعك في منشئ المواقع في Commerce لربط موقعك بعنوان URL صالح للعمل.</span><span class="sxs-lookup"><span data-stu-id="e3d68-126">After your e-commerce environment is provisioned, you must set up your site in Commerce site builder to associate your site to the working URL.</span></span>

<span data-ttu-id="e3d68-127">عند إعداد موقع للمرة الأولى في منشئ المواقع، سيظهر مربع الحوار **إعداد موقعك**.</span><span class="sxs-lookup"><span data-stu-id="e3d68-127">When you first set up a site in site builder, the **Setup your Site** dialog box will appear.</span></span>

<span data-ttu-id="e3d68-128">يبين الرسم التوضيحي التالي مربع الحوار **إعداد موقعك** لموقع مسمى "افتراضي" عندما تنتقل إلى الموقع للمرة الأولى في منشئ المواقع.</span><span class="sxs-lookup"><span data-stu-id="e3d68-128">The following illustration shows the **Setup your Site** dialog box for a site named "default" when you access the site for the first time in site builder.</span></span>

![مربع الحوار **إعداد موقعك**](./media/Domains_SetupyoursiteScreen.png)

<span data-ttu-id="e3d68-130">يسمح لك المربع **تحديد مجال** بربط أحد أسماء الأجهزة المضيفة المدعومة لموقعك في LCS في منشئ المواقع.</span><span class="sxs-lookup"><span data-stu-id="e3d68-130">The **Select a domain** box allows you to associate one of the supported host names provided for your site in LCS to your site in site builder.</span></span>

<span data-ttu-id="e3d68-131">يمكن ترك مربع **المسار** فارغًا، أو يمكن إضافة سلسلة مسار إضافية سوف تنعكس في عنوان URL صالح للعمل.</span><span class="sxs-lookup"><span data-stu-id="e3d68-131">The **Path** box can be left blank, or an additional path string can be added that will be reflected in your working URL.</span></span> <span data-ttu-id="e3d68-132">يؤدي ترك مربع **المسار** فارغًا إلى ربط عنوان URL الأساسي الذي تم إنشاؤه في Commerce بالموقع الذي يجري إعداده في منشئ المواقع.</span><span class="sxs-lookup"><span data-stu-id="e3d68-132">Leaving the **Path** box blank associates the base Commerce-generated URL with the site being set up in site builder.</span></span> <span data-ttu-id="e3d68-133">يجب أن تكون المسارات فريدة لكل زوج موقع/مجال.</span><span class="sxs-lookup"><span data-stu-id="e3d68-133">Paths must be unique for each site/domain pair.</span></span> <span data-ttu-id="e3d68-134">ضمن الموقع والمجال المحددين، بإمكان موقع واحد فقط في البيئة استخدام المسار الفارغ أو المرتبط بسلسلة مسار فريدة.</span><span class="sxs-lookup"><span data-stu-id="e3d68-134">Within the site and domain selected, only one site in the environment can use the blank path or be associated with a unique path string.</span></span> <span data-ttu-id="e3d68-135">ستصبح أي سلسلة تُضاف إلى حقل **المسار** أثناء إعداد الموقع مسارًا فرعيًا اعداد الموقع مسارا فرعًا لعنوان URL الأساسي الذي تم إنشاؤه في Commerce والمستخدم للوصول إلى الموقع في مستعرض الويب.</span><span class="sxs-lookup"><span data-stu-id="e3d68-135">Any string added to the **Path** field during site setup will become a subpath of the base Commerce-generated URL used to access the site in a web browser.</span></span>

> [!NOTE]
> <span data-ttu-id="e3d68-136">يعرف المسار أيضًا باسم **مسار المطابقة** عند إضافة قناة في قسم مسار تكوين **إعدادات الموقع \> القنوات** في منشئ المواقع.</span><span class="sxs-lookup"><span data-stu-id="e3d68-136">The path is also known as the **Match path** when adding a channel in the **Site Settings \> Channels** configuration section of site builder.</span></span>

<span data-ttu-id="e3d68-137">على سبيل المثال، إذا كان لديك موقع في منشئ الموقع يسمى "fabrikam" في مستأجر تجارة إلكترونية يسمى "xyz"، وإذا قمت بإعداد الموقع بمسار فارغ، فيمكنك في هذه الحالة الوصول إلى محتوى الموقع المنشور في مستعرض الويب بالانتقال مباشرةً إلى عنوان URL الأساسي الذي تم إنشاؤه في Commerce.‬</span><span class="sxs-lookup"><span data-stu-id="e3d68-137">For example, if you have a site in site builder called "fabrikam" in an e-commerce tenant named "xyz," and if you set up the site with a blank path, then you would access the published site content in a web browser by going directly to the base Commerce-generated URL:</span></span>

`https://xyz.commerce.dynamics.com`

<span data-ttu-id="e3d68-138">بدلاً من ذلك، إذا أضفت مسار "fabrikam" أثناء إعداد هذا الموقع نفسه، فيمكنك الوصول إلى محتوى الموقع المنشور في مستعرض الويب باستخدام عنوان URL التالي:</span><span class="sxs-lookup"><span data-stu-id="e3d68-138">Alternately, if you had added a path of "fabrikam" during this same site's setup, you would access the published site content in a web browser using the following URL:</span></span>

`https://xyz.commerce.dynamics.com/fabrikam`

## <a name="pages-and-urls"></a><span data-ttu-id="e3d68-139">الصفحات وعناوين URL</span><span class="sxs-lookup"><span data-stu-id="e3d68-139">Pages and URLs</span></span>

<span data-ttu-id="e3d68-140">بعد إعداد موقعك بواسطة مسار، سيتم بناء جميع عناوين URL المقترنة بصفحات في منشئ المواقع على عنوان URL صالح للعمل (عنوان URL الذي تم إنشاؤه في Commerce أو عنوان URL الذي تم إنشاؤه في Commerce بالإضافة إلى المسار) للموقع.</span><span class="sxs-lookup"><span data-stu-id="e3d68-140">After your site is set up with a path, all URLs associated with pages in site builder will build on the working URL (the Commerce-generated URL, or the Commerce-generated URL plus the path) for the site.</span></span> <span data-ttu-id="e3d68-141">سيؤدي إنشاء عنوان URL جديد في منشئ المواقع (**URLS /> +جديد**) من خلال تحديد صفحة من القائمة في مربع الحوار **عنوان URL جديد** وإدخال مسار عنوان URL لتلك الصفحة إلى ربط عنوان URL هذا بالصفحة المحددة.</span><span class="sxs-lookup"><span data-stu-id="e3d68-141">Creating a new URL in site builder (**URLS /> +New**) by selecting a page from the list in the **New URL** dialog box and entering the URL path for that page will associate that URL with the selected page.</span></span> <span data-ttu-id="e3d68-142">تُلحق عندئذٍ قيمة مسار عنوان URL بعنوان URL صالح للعمل خاص بالموقع للوصول إلى الصفحة، وتحمل التسمية `./<URL path>` في قائمة URL لصفحة **عناوين URL** في منشئ المواقع.</span><span class="sxs-lookup"><span data-stu-id="e3d68-142">The URL path value then appends to the site's working URL to access the page, and is labeled as `./<URL path>` in the URL list of the **URLs** page in site builder.</span></span>

<span data-ttu-id="e3d68-143">يبين الرسم التوضيحي التالي مربع الحوار **عنوان URL جديد** في منشئ المواقع مع تمييز مسار URL كمثال.</span><span class="sxs-lookup"><span data-stu-id="e3d68-143">The following illustration shows the **New URL** dialog box in site builder with an example URL path highlighted.</span></span> 

![مربع الحوار **عنوان URL جديد** في منشئ المواقع](./media/Domains_PageSetup2a.png)

<span data-ttu-id="e3d68-145">يبين الرسم التوضيحي التالي صفحة **عناوين URL** في منشئ المواقع مع تمييز عنوان URL كمثال في القائمة.</span><span class="sxs-lookup"><span data-stu-id="e3d68-145">The following illustration shows the **URLs** page in site builder with an example URL highlighted in the list.</span></span>

![الخيار "تشغيل تدفق المستخدم‬‏‫" في تدفق السياسة](./media/Domains_URLsInSiteBuilder2a.png)

## <a name="domains-in-site-builder"></a><span data-ttu-id="e3d68-147">المجالات في منشئ المواقع</span><span class="sxs-lookup"><span data-stu-id="e3d68-147">Domains in site builder</span></span>

<span data-ttu-id="e3d68-148">تتوفر قيم أسماء الأجهزة المضيفة المدعومة ليتم إقرانها كمجال عند إعداد موقع.</span><span class="sxs-lookup"><span data-stu-id="e3d68-148">The supported host names values are available to be associated as a domain when setting up a site.</span></span> <span data-ttu-id="e3d68-149">عند تحديد قيمة اسم مضيف مدعوم كمجال، ستشاهد المجال الذي تم اختياره وقد تمت الإشارة إليه عبر منشئ المواقع.</span><span class="sxs-lookup"><span data-stu-id="e3d68-149">When selecting a supported host name value as the domain, you will see the chosen domain referenced throughout site builder.</span></span> <span data-ttu-id="e3d68-150">يعد هذا المجال مرجعًا فقط داخل بيئة Commerce، ولن تتم بعد إعادة توجيه حركة المرور المباشرة لهذا المجال إلى Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e3d68-150">This domain is only a reference within the Commerce environment, live traffic for that domain will not yet be forwarded to Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e3d68-151">عند العمل مع المواقع في منشئ المواقع، عند وجود موقعين تم إعدادهما بواسطة مجالين مختلفة، يمكنك إلحاق السمة **?domain=** بعنوان URL الصالح للعمل للوصول إلى محتوى الموقع المنشور في المستعرض.</span><span class="sxs-lookup"><span data-stu-id="e3d68-151">When working with sites in site builder, if you have two sites set up with two different domains, you can append the **?domain=** attribute to your working URL to access the published site content in a browser.</span></span>

<span data-ttu-id="e3d68-152">على سبيل المثال، تم تزويد البيئة "xyz"، وتم إنشاء موقعين وربطهما في منشئ المواقع: أحدهما مع المجال `www.fabrikam.com` والآخر مع المجال `www.constoso.com`.</span><span class="sxs-lookup"><span data-stu-id="e3d68-152">For example, environment "xyz" has been provisioned, and two sites have been created and associated in site builder: one with the domain `www.fabrikam.com` and the other with the domain `www.constoso.com`.</span></span> <span data-ttu-id="e3d68-153">تم إعداد كل موقع باستخدام مسار فارغ.</span><span class="sxs-lookup"><span data-stu-id="e3d68-153">Each site was set up using a blank path.</span></span> <span data-ttu-id="e3d68-154">ويمكن بعد ذلك الوصول إلى هذين الموقعين في مستعرض ويب كالتالي باستخدام السمة **?domain=**:</span><span class="sxs-lookup"><span data-stu-id="e3d68-154">These two sites could then be accessed in a web browser as follows using the **?domain=** attribute:</span></span>
- `https://xyz.commerce.dynamics.com?domain=www.fabrikam.com`
- `https://xyz.commerce.dynamics.com?domain=www.contoso.com`

<span data-ttu-id="e3d68-155">عندما لا يتم إعطاء سلسلة استعلام مجال في بيئة تم فيها توفير مجالات متعددة، يستخدم Commerce المجال الأول الذي قمت بتوفيره.</span><span class="sxs-lookup"><span data-stu-id="e3d68-155">When a domain query string is not given in an environment with multiple domains provided, Commerce uses the first domain you provided.</span></span> <span data-ttu-id="e3d68-156">على سبيل المثال، إذا تم تقديم المسار "fabrikam" أولاً أثناء إعداد الموقع، فيمكن استخدام عنوان URL `https://xyz.commerce.dynamics.com` للوصول إلى موقع محتوى الموقع المنشور في `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="e3d68-156">For example, if the path "fabrikam" was provided first during site setup, the URL `https://xyz.commerce.dynamics.com` could be used to access the published site content site for `www.fabrikam.com`.</span></span>

## <a name="traffic-forwarding-in-production"></a><span data-ttu-id="e3d68-157">إعادة توجيه حركة المرور في الإنتاج</span><span class="sxs-lookup"><span data-stu-id="e3d68-157">Traffic forwarding in production</span></span>

<span data-ttu-id="e3d68-158">يمكنك محاكاة مجالات متعددة باستخدام معلمات سلسلة استعلام المجال في نقطة نهاية commerce.dynamics.com نفسها.</span><span class="sxs-lookup"><span data-stu-id="e3d68-158">You can simulate multiple domains using domain query string parameters on the commerce.dynamics.com endpoint itself.</span></span> <span data-ttu-id="e3d68-159">ولكن عندما تحتاج إلى الانتقال إلى العرض المباشر في الإنتاج، يجب عليك توجيه حركة المرور لمجالك المخصص إلى نقطة النهاية `<e-commerce tenant name>.commerce.dynamics.com`.</span><span class="sxs-lookup"><span data-stu-id="e3d68-159">But when you need to go live in production, you must forward the traffic for your custom domain to the `<e-commerce tenant name>.commerce.dynamics.com` endpoint.</span></span>

<span data-ttu-id="e3d68-160">لا تدعم نقطة النهاية `<e-commerce tenant name>.commerce.dynamics.com` مآخذ توصيل آمنة (SSL) للمجالات المخصصة، وبالتالي بجب إعداد مجالات مخصصة باستخدام خدمة الواجهة الأمامية أو شبكة تسليم المحتوى (CDN).</span><span class="sxs-lookup"><span data-stu-id="e3d68-160">The `<e-commerce tenant name>.commerce.dynamics.com` endpoint does not support custom domain Secure Sockets Layers (SSLs), so you must set up custom domains using a front door service or content delivery network (CDN).</span></span> 

<span data-ttu-id="e3d68-161">لإعداد مجالات مخصصة باستخدام خدمة الواجهة الأمامية أو CDN، هناك خياران:</span><span class="sxs-lookup"><span data-stu-id="e3d68-161">To set up custom domains using a front door service or CDN, you have two options:</span></span>

- <span data-ttu-id="e3d68-162">إعداد خدمة واجهة أمامية مثل Azure Front Door للتعامل مع حركة مرور الواجهة الأمامية والاتصال Commerce.</span><span class="sxs-lookup"><span data-stu-id="e3d68-162">Set up a front door service like Azure Front Door to handle front-end traffic and connect to your Commerce environment.</span></span> <span data-ttu-id="e3d68-163">ويوفر ذلك مستوى أكبر من التحكم في إدارة المجالات والشهادات وسياسات أمان أكثر دقة.</span><span class="sxs-lookup"><span data-stu-id="e3d68-163">This provides greater control over domain and certificate management and more granular security policies.</span></span>
- <span data-ttu-id="e3d68-164">استخدام مثيل Azure Front Door الذي يوفره Commerce.</span><span class="sxs-lookup"><span data-stu-id="e3d68-164">Use the Commerce-supplied Azure Front Door instance.</span></span> <span data-ttu-id="e3d68-165">يتطلب ذلك تنسيق الإجراء مع فريق Dynamics 365 Commerce للتحقق من المجال والحصول على شهادات SSL لمجال الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="e3d68-165">This requires coordinating action with the Dynamics 365 Commerce team for domain verification and obtaining SSL certificates for your production domain.</span></span>

<span data-ttu-id="e3d68-166">للحصول على معلومات حول كيفية إعداد خدمة CDN مباشرة، راجع [إضافة الدعم لشبكة تسليم المحتوى (CDN)](add-cdn-support.md).</span><span class="sxs-lookup"><span data-stu-id="e3d68-166">For information about how to set up a CDN service directly, see [Add support for a content delivery network (CDN)](add-cdn-support.md).</span></span>

<span data-ttu-id="e3d68-167">لاستخدام مثيل Azure Front Door الذي توفره التجارة الإلكترونية، يجب إنشاء طلب خدمة للمساعدة في إعداد من فريق إعداد Commerce.</span><span class="sxs-lookup"><span data-stu-id="e3d68-167">To use the Commerce-supplied Azure Front Door instance, you must create a service request for CDN setup assistance from the Commerce onboarding team.</span></span> 

- <span data-ttu-id="e3d68-168">ستحتاج إلى إدخال اسم شركتك ومجال الإنتاج ومعرف البيئة واسم مستأجر التجارة الإلكترونية للإنتاج.</span><span class="sxs-lookup"><span data-stu-id="e3d68-168">You will need to provide your company name, the production domain, environment ID, and production e-commerce tenant name.</span></span> 
- <span data-ttu-id="e3d68-169">ستحتاج إلى تأكيد ما إذا كان هذا المجال عبارة عن مجال موجود (يستخدم لموقع نشط حاليًا) أو مجال جديد.</span><span class="sxs-lookup"><span data-stu-id="e3d68-169">You will need to confirm if this is an existing domain (used for a currently active site) or a new domain.</span></span> 
- <span data-ttu-id="e3d68-170">بالنسبة لمجال جديد، يمكن تحقيق التحقق من المجال وشهادة SSL في خطوة واحدة.</span><span class="sxs-lookup"><span data-stu-id="e3d68-170">For a new domain, the domain verification and SSL certificate can be achieved in a single step.</span></span> 
- <span data-ttu-id="e3d68-171">بالنسبة لمجال يقوم بخدمة موقع ويب موجود، توجد عملية متعددة الخطوات مطلوبة لتأسيس التحقق من المجال وشهادة SSL.</span><span class="sxs-lookup"><span data-stu-id="e3d68-171">For a domain serving an existing website, there is a multistep process required to establish the domain verification and SSL certificate.</span></span> <span data-ttu-id="e3d68-172">تتكون هذه العملية من اتفاقية مستوى خدمة لمدة 7 أيام عمل كي ينتقل المجال إلى وضع العرض المباشر، لأنها تشتمل على خطوات متسلسلة متعددة.</span><span class="sxs-lookup"><span data-stu-id="e3d68-172">This process has a 7-working-day service level agreement (SLA) for a domain to go live, because it includes multiple sequential steps.</span></span>

<span data-ttu-id="e3d68-173">لإنشاء طلب خدمة في LCS، انتقل في بيئتك إلى **الدعم \> مشاكل الدعم** وحدد **إرسال حادث**.</span><span class="sxs-lookup"><span data-stu-id="e3d68-173">To create a service request in LCS, within your environment go to **Support \> Support issues** and select **Submit an incident**.</span></span>

> [!NOTE]
> <span data-ttu-id="e3d68-174">يتم اعتماد المجالات المخصصة مع SSL فقط في بيئات التشغيل.</span><span class="sxs-lookup"><span data-stu-id="e3d68-174">Custom domains with SSL are only supported on production environments.</span></span> <span data-ttu-id="e3d68-175">بالنسبة للبيئات غير الإنتاجية مثل بيئة الاختبار المعزولة واختبار قبول المستخدم (UAT)، استخدام عنوان URL الذي أنشأه Commerce للوصول إلى المحتوى المنشور في مستعرض الويب.</span><span class="sxs-lookup"><span data-stu-id="e3d68-175">For non-production environments such as sandbox and user acceptance testing (UAT), use the Commerce-generated URL to access published content in a web browser.</span></span>

## <a name="ssl-certificate-process"></a><span data-ttu-id="e3d68-176">عملية شهادة SSL</span><span class="sxs-lookup"><span data-stu-id="e3d68-176">SSL certificate process</span></span>

<span data-ttu-id="e3d68-177">عند القيام بتصنيف طلب خدمة، يقوم فريق Commerce بتنسيق الخطوات التالية معك.</span><span class="sxs-lookup"><span data-stu-id="e3d68-177">When a service request is filed, the Commerce team will coordinate the following steps with you.</span></span>

<span data-ttu-id="e3d68-178">للمجالات الجديدة:</span><span class="sxs-lookup"><span data-stu-id="e3d68-178">For new domains:</span></span>
- <span data-ttu-id="e3d68-179">سيقوم فريق Commerce بإعداد مثيل Azure Front Door (مستضاف في Commerce).</span><span class="sxs-lookup"><span data-stu-id="e3d68-179">The Commerce team will set up the Azure Front Door instance (Commerce-hosted).</span></span>
- <span data-ttu-id="e3d68-180">سيقوم فريق Commerce بعد ذلك بتوفير سجل CNAME للإشارة إل مجالك المخصص.</span><span class="sxs-lookup"><span data-stu-id="e3d68-180">The Commerce team will then provide the CNAME record to point your custom domain.</span></span>
- <span data-ttu-id="e3d68-181">بعد تحديث السجل CNAME، سيكون مثيل Azure Front Door المستضاف في Commerce قادرًا على التحقق من ملكية المجال والحصول على شهادة SSL.</span><span class="sxs-lookup"><span data-stu-id="e3d68-181">After the CNAME record is updated, the Commerce-hosted Azure Front Door instance will be able to verify the domain ownership and get the SSL certificate.</span></span>

<span data-ttu-id="e3d68-182">للمجالات الموجودة/النشطة:</span><span class="sxs-lookup"><span data-stu-id="e3d68-182">For existing/active domains:</span></span>
- <span data-ttu-id="e3d68-183">سيرشدك فريق Commerce لإضافة سجل `afdverify.<custom-domain>` CNAME لتقديمه إلى موفر DNS لمجالك.</span><span class="sxs-lookup"><span data-stu-id="e3d68-183">The Commerce team will instruct you to add an `afdverify.<custom-domain>` CNAME record to provide to your domain DNS provider.</span></span>
- <span data-ttu-id="e3d68-184">وعند الانتهاء، سيقوم فريق Commerce بإضافة المجال إلى مثيل Azure Front Door وتوفير سجلات DNS TXT إضافية لإضافتها إلى DNS الخاص بالمجال.</span><span class="sxs-lookup"><span data-stu-id="e3d68-184">When complete, the Commerce team will add the domain to the Azure Front Door instance and provide additional DNS TXT records to be added to the DNS for the domain.</span></span>
- <span data-ttu-id="e3d68-185">بعد إكمال سجلات TXT، سيقوم فريق Commerce بإكمال تحديثات Azure Front Door للمجال الذي سيقوم بإعداد شهادة SSL.</span><span class="sxs-lookup"><span data-stu-id="e3d68-185">After the TXT records are completed, the Commerce team will complete the Azure Front Door updates for the domain that will set up the SSL certificate.</span></span>

## <a name="apex-domains"></a><span data-ttu-id="e3d68-186">مجالات Apex</span><span class="sxs-lookup"><span data-stu-id="e3d68-186">Apex domains</span></span>

<span data-ttu-id="e3d68-187">لا يدعم مثيل Azure Front Door الذي يوفره Commerce مجالات apex (المجالات الجذر التي لا تتضمن مجالات ثانوية).</span><span class="sxs-lookup"><span data-stu-id="e3d68-187">The Commerce-supplied Azure Front Door instance does not support apex domains (root domains that do not contain subdomains).</span></span> <span data-ttu-id="e3d68-188">تتطلب مجالات Apex عنوان IP لحل المشكلة، ويوجد Commerce Azure Front Door مع نقاط النهاية الظاهرية فقط.</span><span class="sxs-lookup"><span data-stu-id="e3d68-188">Apex domains require an IP address to resolve, and the Commerce Azure Front Door instance exists with virtual endpoints only.</span></span> <span data-ttu-id="e3d68-189">لاستخدام مجال apex، لديك خياران:</span><span class="sxs-lookup"><span data-stu-id="e3d68-189">To use an apex domain, you have two options:</span></span>

- <span data-ttu-id="e3d68-190">**الخيار 1** - استخدم موفر DNS لإعادة توجيه مجال apex إلى مجال "www".</span><span class="sxs-lookup"><span data-stu-id="e3d68-190">**Option 1** - Use your DNS provider to redirect the apex domain to a "www" domain.</span></span> <span data-ttu-id="e3d68-191">على سبيل المثال، يعيد fabrikam.com التوجيه إلى `www.fabrikam.com` حيث `www.fabrikam.com` يمثل سجل CNAME الذي يشير إلى مثيل Azure Front Door المستضاف في Commerce.</span><span class="sxs-lookup"><span data-stu-id="e3d68-191">For example, fabrikam.com redirects to `www.fabrikam.com` where `www.fabrikam.com` is the CNAME record that points to the Commerce-hosted Azure Front Door instance.</span></span>

- <span data-ttu-id="e3d68-192">**الخيار 2** - إعداد CDN/مثيل واجهة أمامية لاستضافة مجال apex.</span><span class="sxs-lookup"><span data-stu-id="e3d68-192">**Option 2** - Set up a CDN/front door instance on your own to host the apex domain.</span></span>

> [!NOTE]
> <span data-ttu-id="e3d68-193">إذا كنت تستخدم Azure Front Door، فيجب عليك أيضًا اعداد Azure DNS في نفس الاشتراك.</span><span class="sxs-lookup"><span data-stu-id="e3d68-193">If you are using Azure Front Door, you must also set up an Azure DNS in the same subscription.</span></span> <span data-ttu-id="e3d68-194">يمكن لمجال apex المستضاف على Azure DNS الإشارة إلى Azure Front Door كسجل باسم مستعار.</span><span class="sxs-lookup"><span data-stu-id="e3d68-194">The apex domain hosted on Azure DNS can point to your Azure Front Door as an alias record.</span></span> <span data-ttu-id="e3d68-195">هذا هو الحل الوحيد، إذ يجب أن تشير مجالات apex دائمًا إلى عنوان IP.</span><span class="sxs-lookup"><span data-stu-id="e3d68-195">This is the only work around, as apex domains must always point to an IP address.</span></span>

  ## <a name="additional-resources"></a><span data-ttu-id="e3d68-196">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="e3d68-196">Additional resources</span></span>

  [<span data-ttu-id="e3d68-197">نشر مستأجر التجارة الإلكترونية الجديد</span><span class="sxs-lookup"><span data-stu-id="e3d68-197">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

  [<span data-ttu-id="e3d68-198">إعداد قناة متجر عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="e3d68-198">Set up an online store channel</span></span>](online-stores.md)

  [<span data-ttu-id="e3d68-199">إنشاء موقع تجارة إلكترونية</span><span class="sxs-lookup"><span data-stu-id="e3d68-199">Create an e-commerce site</span></span>](create-ecommerce-site.md)

  [<span data-ttu-id="e3d68-200">إقران موقع Dynamics 365 Commerce بقناة عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="e3d68-200">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

  [<span data-ttu-id="e3d68-201">إدارة ملفات robots.txt</span><span class="sxs-lookup"><span data-stu-id="e3d68-201">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

  [<span data-ttu-id="e3d68-202">تحميل عناوين URL لإعادة التوجيه‬ بشكل مجمع</span><span class="sxs-lookup"><span data-stu-id="e3d68-202">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

  [<span data-ttu-id="e3d68-203">إعداد مستأجر B2C في Commerce</span><span class="sxs-lookup"><span data-stu-id="e3d68-203">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

  [<span data-ttu-id="e3d68-204">إعداد صفحات مخصصة لعمليات تسجيل دخول المستخدمين</span><span class="sxs-lookup"><span data-stu-id="e3d68-204">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

  [<span data-ttu-id="e3d68-205">تكوين مستأجرين متعددين لمتاجرة عمل-مستهلك في بيئة Commerce</span><span class="sxs-lookup"><span data-stu-id="e3d68-205">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

  [<span data-ttu-id="e3d68-206">إضافة الدعم إلى شبكة تسليم المحتوى (CDN)</span><span class="sxs-lookup"><span data-stu-id="e3d68-206">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

  [<span data-ttu-id="e3d68-207">تمكين اكتشاف المتجر استنادًا إلى الموقع</span><span class="sxs-lookup"><span data-stu-id="e3d68-207">Enable location-based store detection</span></span>](enable-store-detection.md)
