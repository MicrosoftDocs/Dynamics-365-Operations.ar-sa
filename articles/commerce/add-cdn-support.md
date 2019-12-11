---
title: إضافة الدعم إلى شبكة تسليم المحتوى (CDN)
description: يوضح هذا الموضوع كيفية إضافة شبكة توصيل المحتوى (CDN) إلى بيئة Microsoft Dynamics 365 Commerce الخاصة بك.
author: brianshook
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fb757672fffb56892837c066d552773908dd1ec1
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696958"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="f2e84-103">إضافة الدعم إلى شبكة تسليم المحتوى (CDN)</span><span class="sxs-lookup"><span data-stu-id="f2e84-103">Add support for a content delivery network (CDN)</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="f2e84-104">يوضح هذا الموضوع كيفية إضافة شبكة توصيل المحتوى (CDN) إلى بيئة Microsoft Dynamics 365 Commerce الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="f2e84-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

## <a name="overview"></a><span data-ttu-id="f2e84-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="f2e84-105">Overview</span></span>

<span data-ttu-id="f2e84-106">عندما تقوم بإعادة بيئة تجارة إلكترونية في Dynamics 365 Commerce، يُمكنك تكوينه للعمل مع خدمة CDN الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="f2e84-106">When you set up an e-Commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="f2e84-107">يُمكن تمكين مجالك المُخصص أثناء عملية التوفير لبيئة التجارة الإلكترونية الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="f2e84-107">Your custom domain can be enabled during the provisioning process for your e-Commerce environment.</span></span> <span data-ttu-id="f2e84-108">وبدلًا من ذلك، يُمكن استخدام طلب خدمة لإعداده بعد اكتمال عملية التوفير.</span><span class="sxs-lookup"><span data-stu-id="f2e84-108">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="f2e84-109">تقوم عملية توفير بيئة التجارة الإلكترونية بإنشاء اسم مضيف مرتبط بالبيئة.</span><span class="sxs-lookup"><span data-stu-id="f2e84-109">The provisioning process for the e-Commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="f2e84-110">يكون لاسم هذا المضيف التنسيق التالي، حيث يكون *e-commerce-tenant-name* هو اسم البيئة الخاصة بك: </span><span class="sxs-lookup"><span data-stu-id="f2e84-110">This host name has the following format, where *e-commerce-tenant-name* is the name of your environment:</span></span>

<span data-ttu-id="f2e84-111">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="f2e84-111">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="f2e84-112">يدعم اسم المضيف أو النقطة النهائية التي يتم إنشاؤها خلال عملية التوفير شهادة طبقة مآخذ التوصيل الآمنة (SSL) فقط لـ \*.commerce.dynamics.com. </span><span class="sxs-lookup"><span data-stu-id="f2e84-112">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="f2e84-113">ولا يدعم SSL للمجالات المُخصصة.</span><span class="sxs-lookup"><span data-stu-id="f2e84-113">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="f2e84-114">وبالتالي، يجب عليك إنهاء SSL للمجالات المخصصة في CDN الخاصة بك وإعادة توجيه حركة النقل من CDN إلى اسم المضيف أو النقطة النهائية التي قام Commerce بإنشائها.</span><span class="sxs-lookup"><span data-stu-id="f2e84-114">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="f2e84-115">بالإضافة إلى ذلك، يتم عرض *الإحصاءات* (إما JavaScript أو ملفات أوراق الأنماط المتتالية \[CSS\]) من Commerce من النقطة النهائية الذي قام Commerce بإنشاءها (\*.commerce.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="f2e84-115">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="f2e84-116">يُمكن تخزين هذه الإحصائيات مؤقتًا فقط في حالة إذا تم وضع اسم المضيف أو نقطة النهاية التي قام Commerce بإنشائها بعد CDN.</span><span class="sxs-lookup"><span data-stu-id="f2e84-116">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="f2e84-117">إعداد نظام إدارة الأوامر الموزعة (SSL)</span><span class="sxs-lookup"><span data-stu-id="f2e84-117">Set up SSL</span></span>

<span data-ttu-id="f2e84-118">وللمساعدة في ضمان إعداد SSL، وأنه قد تم تخزين الإحصائيات مؤقتًا، يجب عليك تكوين CDN الخاص بك بحيث يكون مقترنًا باسم المضيف الذي قام Commerce بإنشاءه للبيئة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="f2e84-118">To help guarantee that SSL is set up, and that statics are cached, you must configure your CDN so that it is associated with the host name that Commerce generated for your environment.</span></span> <span data-ttu-id="f2e84-119">كما يجب عليك أيضًا تخزين الأنماط التالية للإحصائيات مؤقتًا فقط:</span><span class="sxs-lookup"><span data-stu-id="f2e84-119">You must also cache the following pattern for statics only:</span></span> 

<span data-ttu-id="f2e84-120">/\_msdyn365/\_scnr/\*</span><span class="sxs-lookup"><span data-stu-id="f2e84-120">/\_msdyn365/\_scnr/\*</span></span>

<span data-ttu-id="f2e84-121">بعد توفير بيئة Commerce الخاصة بك مع المجال المخصص الذي تم توفيره، أو بعد أن تقوم بتوفير مجال مخصص للبيئة الخاصة بك باستخدام طلب خدمة، قم بالإشارة إلى مجالك المخصص لاسم المضيف أو النقطة النهائية التي قام Commerce بإنشائها.</span><span class="sxs-lookup"><span data-stu-id="f2e84-121">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, point your custom domain to the host name or endpoint that Commerce generated.</span></span>

<span data-ttu-id="f2e84-122">وكما سبق ذكره، يدعم اسم المضيف أو نقطة النهاية التي تم إنشائها شهادة SSL فقط لـ \*.commerce.dynamics.com. </span><span class="sxs-lookup"><span data-stu-id="f2e84-122">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="f2e84-123">ولا يدعم SSL للمجالات المُخصصة.</span><span class="sxs-lookup"><span data-stu-id="f2e84-123">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="f2e84-124">خدمات CDN</span><span class="sxs-lookup"><span data-stu-id="f2e84-124">CDN services</span></span>

<span data-ttu-id="f2e84-125">يُمكن استخدام أي خدمة من خدمات CDN مع بيئة Commerce.</span><span class="sxs-lookup"><span data-stu-id="f2e84-125">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="f2e84-126">وفيما يلي مثالين:</span><span class="sxs-lookup"><span data-stu-id="f2e84-126">Here are two examples:</span></span>

- <span data-ttu-id="f2e84-127">**Microsoft Azure Front Door Service** – حل Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="f2e84-127">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="f2e84-128">للمزيد من المعلومات حول Azure Front Door Service، راجع [وثائق Azure Front Door Service](https://docs.microsoft.com/azure/frontdoor/).</span><span class="sxs-lookup"><span data-stu-id="f2e84-128">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/).</span></span>
- <span data-ttu-id="f2e84-129">**Akamai Dynamic Site Accelerator** – للمزيد من المعلومات، راجع [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span><span class="sxs-lookup"><span data-stu-id="f2e84-129">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="f2e84-130">إعداد CDN</span><span class="sxs-lookup"><span data-stu-id="f2e84-130">CDN setup</span></span>

<span data-ttu-id="f2e84-131">تتكون عملية إعداد CDN من الخطوات العامة التالية:</span><span class="sxs-lookup"><span data-stu-id="f2e84-131">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="f2e84-132">إضافة مضيف واجهة أمامية.</span><span class="sxs-lookup"><span data-stu-id="f2e84-132">Add a front-end host.</span></span>
1. <span data-ttu-id="f2e84-133">قم بتكوين مجموعة النهاية الخلفية.</span><span class="sxs-lookup"><span data-stu-id="f2e84-133">Configure a back-end pool.</span></span>
1. <span data-ttu-id="f2e84-134">إعداد القواعد للتوجيه والتخزين المؤقت.</span><span class="sxs-lookup"><span data-stu-id="f2e84-134">Set up rules for routing and caching.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="f2e84-135">إضافة مضيف واجهة أمامية</span><span class="sxs-lookup"><span data-stu-id="f2e84-135">Add a front-end host</span></span>

<span data-ttu-id="f2e84-136">يُمكن استخدام أي خدمة من خدمات CDN، ولكن بالنسبة للمثال الموجود في هذا الموضوع، يتم استخدام Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="f2e84-136">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="f2e84-137">للحصول على معلومات حول كيفية إعداد Azure Front Door Service، راجع [Quickstart: إنشاء Front Door لتطبيق الويب العمومي المتوفرة بشكل كبير](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span><span class="sxs-lookup"><span data-stu-id="f2e84-137">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-back-end-pool-in-azure-front-door-service"></a><span data-ttu-id="f2e84-138">تكوين وعاء خلفي في Azure Front Door Service </span><span class="sxs-lookup"><span data-stu-id="f2e84-138">Configure a back-end pool in Azure Front Door Service</span></span>

<span data-ttu-id="f2e84-139">لتكوين وعاء خلفي في Azure Front Door Service، اتبع الخطوات التالية. </span><span class="sxs-lookup"><span data-stu-id="f2e84-139">To configure a back-end pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="f2e84-140">إضافة **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** للوعاء الخلفي كمضيف مخصص له عنوان مضيف خلفي فارغ.</span><span class="sxs-lookup"><span data-stu-id="f2e84-140">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a back-end pool as a custom host that has an empty back-end host header.</span></span>
1. <span data-ttu-id="f2e84-141">ضمن **فحوصات الصحة**، في حقل **المسار** ، ادخل **/keepalive**. </span><span class="sxs-lookup"><span data-stu-id="f2e84-141">Under **Health probes**, in the **Path** field, enter **/keepalive**.</span></span>
1. <span data-ttu-id="f2e84-142">في حقل **الفواصل الزمنية (ثوان)** ، ادخل **255**.</span><span class="sxs-lookup"><span data-stu-id="f2e84-142">In the **Intervals (seconds)** field, enter **255**.</span></span>
1. <span data-ttu-id="f2e84-143">تحت **موازنة التحميل**، اترك القيم الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="f2e84-143">Under **Load balancing**, leave the default values.</span></span>

<span data-ttu-id="f2e84-144">يُبين الرسم التوضيحي التالي مربع الحوار **إضافة وعاء خلفي** في Azure Front Door Service. </span><span class="sxs-lookup"><span data-stu-id="f2e84-144">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service.</span></span>

![إضافة مربع حوار وعاء خلفي](./media/CDN_BackendPool.png)

### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="f2e84-146">إعداد القواعد في Azure Front Door Service</span><span class="sxs-lookup"><span data-stu-id="f2e84-146">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="f2e84-147">لإعداد قاعدة التوجيه في Azure Front Door Service، اتبع الخطوات التالية. </span><span class="sxs-lookup"><span data-stu-id="f2e84-147">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="f2e84-148">إضافة قاعدة التوجيه.</span><span class="sxs-lookup"><span data-stu-id="f2e84-148">Add a routing rule.</span></span>
1. <span data-ttu-id="f2e84-149">في الحقل **الاسم** ، أدخل **‏افتراضي**.</span><span class="sxs-lookup"><span data-stu-id="f2e84-149">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="f2e84-150">في حقل **البروتوكول المقبول** ، حدد **HTTP وHTTPS**.</span><span class="sxs-lookup"><span data-stu-id="f2e84-150">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="f2e84-151">في حقل **مضيفو الواجهة الأمامية** ، ادخل **dynamics-ecom-tenant-name.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="f2e84-151">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="f2e84-152">تحت **النماذج المطلوب مطابقتها**، في الحقل العلوي، ادخل **/\***.</span><span class="sxs-lookup"><span data-stu-id="f2e84-152">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="f2e84-153">تحت **تفاصيل التوجيه**، قم بتعيين خيار **نوع التوجيه** إلى **للأمام**.</span><span class="sxs-lookup"><span data-stu-id="f2e84-153">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="f2e84-154">في حقل **الوعاء الخلفي** ،حدد **ecom-backend**. </span><span class="sxs-lookup"><span data-stu-id="f2e84-154">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="f2e84-155">في مجموعة حقل **بروتوكول إعادة التوجيه** ،حدد خيار **مطابقة الطلب**.</span><span class="sxs-lookup"><span data-stu-id="f2e84-155">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="f2e84-156">قم بتعيين خيار **إعادة كتابة عنوان URL** إلى **مُعطل**.</span><span class="sxs-lookup"><span data-stu-id="f2e84-156">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="f2e84-157">قم بتعيين خيار **التخزين المؤقت** إلى **مُعطل**.</span><span class="sxs-lookup"><span data-stu-id="f2e84-157">Set the **Caching** option to **Disabled**.</span></span>

<span data-ttu-id="f2e84-158">لإعداد قاعدة التخزين المؤقت في Azure Front Door Service، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="f2e84-158">To set up a caching rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="f2e84-159">إضافة قاعدة التخزين المؤقت.</span><span class="sxs-lookup"><span data-stu-id="f2e84-159">Add a caching rule.</span></span>
1. <span data-ttu-id="f2e84-160">في الحقل **الاسم** ، أدخل **‏الإحصائيات**.</span><span class="sxs-lookup"><span data-stu-id="f2e84-160">In the **Name** field, enter **statics**.</span></span>
1. <span data-ttu-id="f2e84-161">في حقل **البروتوكول المقبول** ، حدد **HTTP وHTTPS**.</span><span class="sxs-lookup"><span data-stu-id="f2e84-161">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="f2e84-162">في حقل **مضيفو الواجهة الأمامية** ، ادخل **dynamics-ecom-tenant-name.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="f2e84-162">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="f2e84-163">تحت **النماذج المطلوب مطابقتها** ، في الحقل العلوي، **/\_msdyn365/\_scnr/\***.</span><span class="sxs-lookup"><span data-stu-id="f2e84-163">Under **Patterns to match**, in the upper field, **/\_msdyn365/\_scnr/\***.</span></span>
1. <span data-ttu-id="f2e84-164">تحت **تفاصيل التوجيه**، قم بتعيين خيار **نوع التوجيه** إلى **للأمام**.</span><span class="sxs-lookup"><span data-stu-id="f2e84-164">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="f2e84-165">في حقل **الوعاء الخلفي** ،حدد **ecom-backend**. </span><span class="sxs-lookup"><span data-stu-id="f2e84-165">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="f2e84-166">في مجموعة حقل **بروتوكول إعادة التوجيه** ،حدد خيار **مطابقة الطلب**.</span><span class="sxs-lookup"><span data-stu-id="f2e84-166">In the **Forwarding protocol** field group, select the **Match request** option.</span></span>
1. <span data-ttu-id="f2e84-167">قم بتعيين خيار **إعادة كتابة عنوان URL** إلى **مُعطل**.</span><span class="sxs-lookup"><span data-stu-id="f2e84-167">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="f2e84-168">قم بتعيين خيار **التخزين المؤقت** إلى **مُعطل**.</span><span class="sxs-lookup"><span data-stu-id="f2e84-168">Set the **Caching** option to **Disabled**.</span></span>
1. <span data-ttu-id="f2e84-169">في حقل **سلوك التخزين المؤقت لسلسلة الاستعلام** ،حدد **تخزين مؤقت لكل عنوان URL فريد**.</span><span class="sxs-lookup"><span data-stu-id="f2e84-169">In the **Query string caching behavior** field, select **Cache every unique URL**.</span></span>
1. <span data-ttu-id="f2e84-170">في مجموعة حقل **الضغط الديناميكي** ،حدد خيار **مُمكّن**.</span><span class="sxs-lookup"><span data-stu-id="f2e84-170">In the **Dynamic compression** field group, select the **Enabled** option.</span></span>

<span data-ttu-id="f2e84-171">يُبين الرسم التوضيحي التالي مربع الحوار **إضافة قاعدة** في Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="f2e84-171">The following illustration shows the **Add a rule** dialog box in Azure Front Door Service.</span></span>

![إضافة مربع حوار قاعدة](./media/CDN_CachingRule.png)

<span data-ttu-id="f2e84-173">بعد أن يتم نشر هذا التكوين الأولي، يجب عليك إضافة مجالك المخصص إلى التكوين الخاص بـ Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="f2e84-173">After this initial configuration is deployed, you must add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="f2e84-174">لإضافة مجال مخصص (على سبيل المثال، `www.fabrikam.com`)، يجب عليك تكوين اسم متعارف عليه (CNAME) للمجال.</span><span class="sxs-lookup"><span data-stu-id="f2e84-174">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="f2e84-175">يُبين الرسم التوضيحي التالي مربع الحوار **تكوين CNAME** في Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="f2e84-175">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![مربع حوار تكوين CNAME](./media/CNAME_Configuration.png)

> [!NOTE]
> <span data-ttu-id="f2e84-177">إذا كان المجال الذي سوف تستخدمه نشطًا ومباشرًا بالفعل، اتصل بالدعم لتمكين هذا المجال مع Azure Front Door Service لإعداد اختبار.</span><span class="sxs-lookup"><span data-stu-id="f2e84-177">If the domain that you will use is already active and live, contact support to enable this domain with Azure Front Door Service to set up a test.</span></span>

<span data-ttu-id="f2e84-178">يُمكنك استخدام Azure Front Door Service لإدارة الشهادة، أو يُمكنك استخدام شهادتك الخاصة للمجال المخصص. </span><span class="sxs-lookup"><span data-stu-id="f2e84-178">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="f2e84-179">يُبين الرسم التوضيحي التالي مربع الحوار **HTTP للمجال المخصص** في Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="f2e84-179">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![مربع حوار HTTP للمجال المخصص](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="f2e84-181">يجب الآن تكوين CDN بشكل صحيح بحيث يُمكن استخدامه مع موقع Commerce الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="f2e84-181">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f2e84-182">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="f2e84-182">Additional resources</span></span>

[<span data-ttu-id="f2e84-183">نظرة عامة على المتجر على الإنترنت</span><span class="sxs-lookup"><span data-stu-id="f2e84-183">Online store overview</span></span>](online-store-overview.md)

[<span data-ttu-id="f2e84-184">إنشاء موقع تجارة إلكترونية</span><span class="sxs-lookup"><span data-stu-id="f2e84-184">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="f2e84-185">نشر موقع تجارة إلكترونية جديد</span><span class="sxs-lookup"><span data-stu-id="f2e84-185">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="f2e84-186">إقران موقع عبر الإنترنت بقناة</span><span class="sxs-lookup"><span data-stu-id="f2e84-186">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="f2e84-187">تكوين اسم مجالك</span><span class="sxs-lookup"><span data-stu-id="f2e84-187">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="f2e84-188">تمكين اكتشاف المتجر استنادًا إلى الموقع</span><span class="sxs-lookup"><span data-stu-id="f2e84-188">Enable location-based store detection</span></span>](enable-store-detection.md)

[<span data-ttu-id="f2e84-189">إعداد صفحات مخصصة لعمليات تسجيل دخول المستخدمين</span><span class="sxs-lookup"><span data-stu-id="f2e84-189">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)
