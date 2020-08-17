---
title: إضافة الدعم إلى شبكة تسليم المحتوى (CDN)
description: يوضح هذا الموضوع كيفية إضافة شبكة توصيل المحتوى (CDN) إلى بيئة Microsoft Dynamics 365 Commerce الخاصة بك.
author: brianshook
manager: annbe
ms.date: 07/31/2020
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
ms.openlocfilehash: 662d26c0157377977bd1031cd7bb13a8e692f37e
ms.sourcegitcommit: 078befcd7f3531073ab2c08b365bcf132d6477b0
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/31/2020
ms.locfileid: "3646029"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="053f0-103">إضافة الدعم إلى شبكة تسليم المحتوى (CDN)</span><span class="sxs-lookup"><span data-stu-id="053f0-103">Add support for a content delivery network (CDN)</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="053f0-104">يوضح هذا الموضوع كيفية إضافة شبكة توصيل المحتوى (CDN) إلى بيئة Microsoft Dynamics 365 Commerce الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="053f0-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

## <a name="overview"></a><span data-ttu-id="053f0-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="053f0-105">Overview</span></span>

<span data-ttu-id="053f0-106">عندما تقوم بإعادة بيئة تجارة إلكترونية في Dynamics 365 Commerce، يُمكنك تكوينه للعمل مع خدمة CDN الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="053f0-106">When you set up an e-Commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="053f0-107">يُمكن تمكين مجالك المُخصص أثناء عملية التوفير لبيئة التجارة الإلكترونية الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="053f0-107">Your custom domain can be enabled during the provisioning process for your e-Commerce environment.</span></span> <span data-ttu-id="053f0-108">وبدلًا من ذلك، يُمكن استخدام طلب خدمة لإعداده بعد اكتمال عملية التوفير.</span><span class="sxs-lookup"><span data-stu-id="053f0-108">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="053f0-109">تقوم عملية توفير بيئة التجارة الإلكترونية بإنشاء اسم مضيف مرتبط بالبيئة.</span><span class="sxs-lookup"><span data-stu-id="053f0-109">The provisioning process for the e-Commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="053f0-110">يكون لاسم هذا المضيف التنسيق التالي، حيث \<*e-commerce-tenant-name*\> هو اسم بيئتك:</span><span class="sxs-lookup"><span data-stu-id="053f0-110">This host name has the following format, where \<*e-commerce-tenant-name*\> is the name of your environment:</span></span>

<span data-ttu-id="053f0-111">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="053f0-111">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="053f0-112">يدعم اسم المضيف أو النقطة النهائية التي يتم إنشاؤها خلال عملية التوفير شهادة طبقة مآخذ التوصيل الآمنة (SSL) فقط لـ \*.commerce.dynamics.com. </span><span class="sxs-lookup"><span data-stu-id="053f0-112">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="053f0-113">ولا يدعم SSL للمجالات المُخصصة.</span><span class="sxs-lookup"><span data-stu-id="053f0-113">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="053f0-114">وبالتالي، يجب عليك إنهاء SSL للمجالات المخصصة في CDN الخاصة بك وإعادة توجيه حركة النقل من CDN إلى اسم المضيف أو النقطة النهائية التي قام Commerce بإنشائها.</span><span class="sxs-lookup"><span data-stu-id="053f0-114">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="053f0-115">بالإضافة إلى ذلك، يتم عرض *الإحصاءات* (إما JavaScript أو ملفات أوراق الأنماط المتتالية \[CSS\]) من Commerce من النقطة النهائية الذي قام Commerce بإنشاءها (\*.commerce.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="053f0-115">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="053f0-116">يُمكن تخزين هذه الإحصائيات مؤقتًا فقط في حالة إذا تم وضع اسم المضيف أو نقطة النهاية التي قام Commerce بإنشائها بعد CDN.</span><span class="sxs-lookup"><span data-stu-id="053f0-116">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="053f0-117">إعداد نظام إدارة الأوامر الموزعة (SSL)</span><span class="sxs-lookup"><span data-stu-id="053f0-117">Set up SSL</span></span>

<span data-ttu-id="053f0-118">وللمساعدة في ضمان إعداد SSL، وأنه قد تم تخزين الإحصائيات مؤقتًا، يجب عليك تكوين CDN الخاص بك بحيث يكون مقترنًا باسم المضيف الذي قام Commerce بإنشاءه للبيئة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="053f0-118">To help guarantee that SSL is set up, and that statics are cached, you must configure your CDN so that it is associated with the host name that Commerce generated for your environment.</span></span> <span data-ttu-id="053f0-119">كما يجب عليك أيضًا تخزين الأنماط التالية للإحصائيات مؤقتًا فقط:</span><span class="sxs-lookup"><span data-stu-id="053f0-119">You must also cache the following pattern for statics only:</span></span> 

<span data-ttu-id="053f0-120">/\_msdyn365/\_scnr/\*</span><span class="sxs-lookup"><span data-stu-id="053f0-120">/\_msdyn365/\_scnr/\*</span></span>

<span data-ttu-id="053f0-121">بعد توفير بيئة Commerce الخاصة بك مع المجال المخصص الذي تم توفيره، أو بعد أن تقوم بتوفير مجال مخصص للبيئة الخاصة بك باستخدام طلب خدمة، قم بالإشارة إلى مجالك المخصص لاسم المضيف أو النقطة النهائية التي قام Commerce بإنشائها.</span><span class="sxs-lookup"><span data-stu-id="053f0-121">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, point your custom domain to the host name or endpoint that Commerce generated.</span></span>

<span data-ttu-id="053f0-122">وكما سبق ذكره، يدعم اسم المضيف أو نقطة النهاية التي تم إنشائها شهادة SSL فقط لـ \*.commerce.dynamics.com. </span><span class="sxs-lookup"><span data-stu-id="053f0-122">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="053f0-123">ولا يدعم SSL للمجالات المُخصصة.</span><span class="sxs-lookup"><span data-stu-id="053f0-123">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="053f0-124">خدمات CDN</span><span class="sxs-lookup"><span data-stu-id="053f0-124">CDN services</span></span>

<span data-ttu-id="053f0-125">يُمكن استخدام أي خدمة من خدمات CDN مع بيئة Commerce.</span><span class="sxs-lookup"><span data-stu-id="053f0-125">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="053f0-126">وفيما يلي مثالين:</span><span class="sxs-lookup"><span data-stu-id="053f0-126">Here are two examples:</span></span>

- <span data-ttu-id="053f0-127">**Microsoft Azure Front Door Service** – حل Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="053f0-127">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="053f0-128">للمزيد من المعلومات حول Azure Front Door Service، راجع [وثائق Azure Front Door Service](https://docs.microsoft.com/azure/frontdoor/).</span><span class="sxs-lookup"><span data-stu-id="053f0-128">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/).</span></span>
- <span data-ttu-id="053f0-129">**Akamai Dynamic Site Accelerator** – للمزيد من المعلومات، راجع [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span><span class="sxs-lookup"><span data-stu-id="053f0-129">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="053f0-130">إعداد CDN</span><span class="sxs-lookup"><span data-stu-id="053f0-130">CDN setup</span></span>

<span data-ttu-id="053f0-131">تتكون عملية إعداد CDN من الخطوات العامة التالية:</span><span class="sxs-lookup"><span data-stu-id="053f0-131">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="053f0-132">إضافة مضيف واجهة أمامية.</span><span class="sxs-lookup"><span data-stu-id="053f0-132">Add a front-end host.</span></span>
1. <span data-ttu-id="053f0-133">تكوين وعاء خلفي.</span><span class="sxs-lookup"><span data-stu-id="053f0-133">Configure a backend pool.</span></span>
1. <span data-ttu-id="053f0-134">إعداد القواعد للتوجيه والتخزين المؤقت.</span><span class="sxs-lookup"><span data-stu-id="053f0-134">Set up rules for routing and caching.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="053f0-135">إضافة مضيف واجهة أمامية</span><span class="sxs-lookup"><span data-stu-id="053f0-135">Add a front-end host</span></span>

<span data-ttu-id="053f0-136">يُمكن استخدام أي خدمة من خدمات CDN، ولكن بالنسبة للمثال الموجود في هذا الموضوع، يتم استخدام Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="053f0-136">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="053f0-137">للحصول على معلومات حول كيفية إعداد Azure Front Door Service، راجع [Quickstart: إنشاء Front Door لتطبيق الويب العمومي المتوفرة بشكل كبير](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span><span class="sxs-lookup"><span data-stu-id="053f0-137">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a><span data-ttu-id="053f0-138">تكوين وعاء خلفي في Azure Front Door Service</span><span class="sxs-lookup"><span data-stu-id="053f0-138">Configure a backend pool in Azure Front Door Service</span></span>

<span data-ttu-id="053f0-139">لتكوين وعاء خلفي في Azure Front Door Service، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="053f0-139">To configure a backend pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="053f0-140">أضف **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** إلى الوعاء الخلفي كمضيف مخصص له عنوان مضيف خلفي فارغ.</span><span class="sxs-lookup"><span data-stu-id="053f0-140">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a backend pool as a custom host that has an empty backend host header.</span></span>
1. <span data-ttu-id="053f0-141">تحت **موازنة التحميل**، اترك القيم الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="053f0-141">Under **Load balancing**, leave the default values.</span></span>

<span data-ttu-id="053f0-142">يُبين الرسم التوضيحي التالي مربع الحوار **إضافة وعاء خلفي** في Azure Front Door Service مع إدخال اسم مضيف وعاء خلفي.</span><span class="sxs-lookup"><span data-stu-id="053f0-142">The following illustration shows the **Add a backend** dialog box in Azure Front Door Service with the backend host name entered.</span></span>

![إضافة مربع حوار وعاء خلفي](./media/CDN_BackendPool.png)

<span data-ttu-id="053f0-144">يُبين الرسم التوضيحي التالي مربع الحوار **إضافة وعاء خلفي** في Azure Front Door Service مع قيم موازنة الحمل الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="053f0-144">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service with the default load balancing values.</span></span>

![إضافة مربع حوار وعاء خلفي يتبع](./media/CDN_BackendPool_2.png)

### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="053f0-146">إعداد القواعد في Azure Front Door Service</span><span class="sxs-lookup"><span data-stu-id="053f0-146">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="053f0-147">لإعداد قاعدة التوجيه في Azure Front Door Service، اتبع الخطوات التالية. </span><span class="sxs-lookup"><span data-stu-id="053f0-147">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="053f0-148">إضافة قاعدة التوجيه.</span><span class="sxs-lookup"><span data-stu-id="053f0-148">Add a routing rule.</span></span>
1. <span data-ttu-id="053f0-149">في الحقل **الاسم** ، أدخل **‏افتراضي**.</span><span class="sxs-lookup"><span data-stu-id="053f0-149">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="053f0-150">في حقل **البروتوكول المقبول** ، حدد **HTTP وHTTPS**.</span><span class="sxs-lookup"><span data-stu-id="053f0-150">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="053f0-151">في حقل **مضيفو الواجهة الأمامية** ، ادخل **dynamics-ecom-tenant-name.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="053f0-151">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="053f0-152">تحت **النماذج المطلوب مطابقتها**، في الحقل العلوي، ادخل **/\***.</span><span class="sxs-lookup"><span data-stu-id="053f0-152">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="053f0-153">تحت **تفاصيل التوجيه**، قم بتعيين خيار **نوع التوجيه** إلى **للأمام**.</span><span class="sxs-lookup"><span data-stu-id="053f0-153">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="053f0-154">في حقل **الوعاء الخلفي** ،حدد **ecom-backend**. </span><span class="sxs-lookup"><span data-stu-id="053f0-154">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="053f0-155">في مجموعة حقل **بروتوكول إعادة التوجيه** ،حدد خيار **مطابقة الطلب**.</span><span class="sxs-lookup"><span data-stu-id="053f0-155">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="053f0-156">قم بتعيين خيار **إعادة كتابة عنوان URL** إلى **مُعطل**.</span><span class="sxs-lookup"><span data-stu-id="053f0-156">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="053f0-157">قم بتعيين خيار **التخزين المؤقت** إلى **مُعطل**.</span><span class="sxs-lookup"><span data-stu-id="053f0-157">Set the **Caching** option to **Disabled**.</span></span>

<span data-ttu-id="053f0-158">لإعداد قاعدة التخزين المؤقت في Azure Front Door Service، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="053f0-158">To set up a caching rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="053f0-159">إضافة قاعدة التخزين المؤقت.</span><span class="sxs-lookup"><span data-stu-id="053f0-159">Add a caching rule.</span></span>
1. <span data-ttu-id="053f0-160">في الحقل **الاسم** ، أدخل **‏الإحصائيات**.</span><span class="sxs-lookup"><span data-stu-id="053f0-160">In the **Name** field, enter **statics**.</span></span>
1. <span data-ttu-id="053f0-161">في حقل **البروتوكول المقبول** ، حدد **HTTP وHTTPS**.</span><span class="sxs-lookup"><span data-stu-id="053f0-161">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="053f0-162">في حقل **مضيفو الواجهة الأمامية** ، ادخل **dynamics-ecom-tenant-name.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="053f0-162">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="053f0-163">تحت **النماذج المطلوب مطابقتها** ، في الحقل العلوي، **/\_msdyn365/\_scnr/\***.</span><span class="sxs-lookup"><span data-stu-id="053f0-163">Under **Patterns to match**, in the upper field, **/\_msdyn365/\_scnr/\***.</span></span>
1. <span data-ttu-id="053f0-164">تحت **تفاصيل التوجيه**، قم بتعيين خيار **نوع التوجيه** إلى **للأمام**.</span><span class="sxs-lookup"><span data-stu-id="053f0-164">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="053f0-165">في حقل **الوعاء الخلفي** ،حدد **ecom-backend**. </span><span class="sxs-lookup"><span data-stu-id="053f0-165">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="053f0-166">في مجموعة حقل **بروتوكول إعادة التوجيه** ،حدد خيار **مطابقة الطلب**.</span><span class="sxs-lookup"><span data-stu-id="053f0-166">In the **Forwarding protocol** field group, select the **Match request** option.</span></span>
1. <span data-ttu-id="053f0-167">قم بتعيين خيار **إعادة كتابة عنوان URL** إلى **مُعطل**.</span><span class="sxs-lookup"><span data-stu-id="053f0-167">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="053f0-168">قم بتعيين خيار **التخزين المؤقت** إلى **مُعطل**.</span><span class="sxs-lookup"><span data-stu-id="053f0-168">Set the **Caching** option to **Disabled**.</span></span>
1. <span data-ttu-id="053f0-169">في حقل **سلوك التخزين المؤقت لسلسلة الاستعلام** ،حدد **تخزين مؤقت لكل عنوان URL فريد**.</span><span class="sxs-lookup"><span data-stu-id="053f0-169">In the **Query string caching behavior** field, select **Cache every unique URL**.</span></span>
1. <span data-ttu-id="053f0-170">في مجموعة حقل **الضغط الديناميكي** ،حدد خيار **مُمكّن**.</span><span class="sxs-lookup"><span data-stu-id="053f0-170">In the **Dynamic compression** field group, select the **Enabled** option.</span></span>

<span data-ttu-id="053f0-171">يُبين الرسم التوضيحي التالي مربع الحوار **إضافة قاعدة** في Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="053f0-171">The following illustration shows the **Add a rule** dialog box in Azure Front Door Service.</span></span>

![إضافة مربع حوار قاعدة](./media/CDN_CachingRule.png)

> [!WARNING]
> <span data-ttu-id="053f0-173">إذا كان المجال الذي ستستخدمه نشطًا ومباشرًا، فأنشئ تذكرة دعم من الإطار المتجانب **الدعم** في [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) للحصول على المساعدة لخطواتك التالية.</span><span class="sxs-lookup"><span data-stu-id="053f0-173">If the domain that you will use is already active and live, create a support ticket from the **Support** tile in [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) to get assistance for your next steps.</span></span> <span data-ttu-id="053f0-174">لمزيد من المعلومات، راجع [الحصول على الدعم لتطبيقات Finance and Operations أو Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="053f0-174">For more information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

<span data-ttu-id="053f0-175">إذا كان مجالك جديدًا وليس مجالاً مباشرًا موجودًا بشكل مسبق، فيمكنك إضافة مجال مخصص إلى تكوين Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="053f0-175">If your domain is new and is not a pre-existing live domain, you can add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="053f0-176">سيؤدي ذلك إلى تمكين حركة مرور الويب لتوجيه موقعك عبر مثيل Azure Front Door.</span><span class="sxs-lookup"><span data-stu-id="053f0-176">This will enable web traffic to direct to your site via the Azure Front Door instance.</span></span> <span data-ttu-id="053f0-177">لإضافة مجال مخصص (على سبيل المثال، `www.fabrikam.com`)، يجب عليك تكوين اسم متعارف عليه (CNAME) للمجال.</span><span class="sxs-lookup"><span data-stu-id="053f0-177">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="053f0-178">يُبين الرسم التوضيحي التالي مربع الحوار **تكوين CNAME** في Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="053f0-178">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![مربع حوار تكوين CNAME](./media/CNAME_Configuration.png)

<span data-ttu-id="053f0-180">يُمكنك استخدام Azure Front Door Service لإدارة الشهادة، أو يُمكنك استخدام شهادتك الخاصة للمجال المخصص. </span><span class="sxs-lookup"><span data-stu-id="053f0-180">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="053f0-181">يُبين الرسم التوضيحي التالي مربع الحوار **HTTP للمجال المخصص** في Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="053f0-181">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![مربع حوار HTTP للمجال المخصص](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="053f0-183">للحصول على إرشادات مفصلة حول إضافة مجال مخصص إلى Azure Front Door، راجع [إضافة مجال مخصص إلى Front Door](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span><span class="sxs-lookup"><span data-stu-id="053f0-183">For detailed instructions on adding a custom domain to your Azure Front Door, see [Add a custom domain to your Front Door](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span></span>

<span data-ttu-id="053f0-184">يجب الآن تكوين CDN بشكل صحيح بحيث يُمكن استخدامه مع موقع Commerce الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="053f0-184">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="053f0-185">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="053f0-185">Additional resources</span></span>

[<span data-ttu-id="053f0-186">تكوين اسم مجالك</span><span class="sxs-lookup"><span data-stu-id="053f0-186">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="053f0-187">نشر موقع تجارة إلكترونية جديد</span><span class="sxs-lookup"><span data-stu-id="053f0-187">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="053f0-188">إنشاء موقع تجارة إلكترونية</span><span class="sxs-lookup"><span data-stu-id="053f0-188">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="053f0-189">إقران موقع عبر الإنترنت بقناة</span><span class="sxs-lookup"><span data-stu-id="053f0-189">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="053f0-190">إدارة ملفات robots.txt</span><span class="sxs-lookup"><span data-stu-id="053f0-190">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="053f0-191">تحميل عناوين URL لإعادة التوجيه‬ بشكل مجمع</span><span class="sxs-lookup"><span data-stu-id="053f0-191">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="053f0-192">إعداد مستأجر B2C في Commerce</span><span class="sxs-lookup"><span data-stu-id="053f0-192">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="053f0-193">إعداد صفحات مخصصة لعمليات تسجيل دخول المستخدمين</span><span class="sxs-lookup"><span data-stu-id="053f0-193">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="053f0-194">تكوين مستأجرين متعددين لمتاجرة عمل-مستهلك في بيئة Commerce</span><span class="sxs-lookup"><span data-stu-id="053f0-194">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="053f0-195">تمكين اكتشاف المتجر استنادًا إلى الموقع</span><span class="sxs-lookup"><span data-stu-id="053f0-195">Enable location-based store detection</span></span>](enable-store-detection.md)
