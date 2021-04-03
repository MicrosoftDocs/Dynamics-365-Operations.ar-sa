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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d653b072eca134c765a5db5659b228648fc13c4a
ms.sourcegitcommit: 3fe4d9a33447aa8a62d704fbbf18aeb9cb667baa
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/12/2021
ms.locfileid: "5582709"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="a9e47-103">إضافة الدعم إلى شبكة تسليم المحتوى (CDN)</span><span class="sxs-lookup"><span data-stu-id="a9e47-103">Add support for a content delivery network (CDN)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a9e47-104">يوضح هذا الموضوع كيفية إضافة شبكة توصيل المحتوى (CDN) إلى بيئة Microsoft Dynamics 365 Commerce الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="a9e47-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="a9e47-105">عندما تقوم بإعداد بيئة تجارة إلكترونية في Dynamics 365 Commerce، يُمكنك تكوينها للعمل مع خدمة CDN الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="a9e47-105">When you set up an e-commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="a9e47-106">يُمكن تمكين مجالك المُخصص أثناء عملية التوفير لبيئة التجارة الإلكترونية الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="a9e47-106">Your custom domain can be enabled during the provisioning process for your e-commerce environment.</span></span> <span data-ttu-id="a9e47-107">وبدلًا من ذلك، يُمكن استخدام طلب خدمة لإعداده بعد اكتمال عملية التوفير.</span><span class="sxs-lookup"><span data-stu-id="a9e47-107">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="a9e47-108">تقوم عملية توفير بيئة التجارة الإلكترونية بإنشاء اسم مضيف مرتبط بالبيئة.</span><span class="sxs-lookup"><span data-stu-id="a9e47-108">The provisioning process for the e-commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="a9e47-109">يكون لاسم هذا المضيف التنسيق التالي، حيث \<*e-commerce-tenant-name*\> هو اسم بيئتك:</span><span class="sxs-lookup"><span data-stu-id="a9e47-109">This host name has the following format, where \<*e-commerce-tenant-name*\> is the name of your environment:</span></span>

<span data-ttu-id="a9e47-110">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="a9e47-110">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="a9e47-111">يدعم اسم المضيف أو النقطة النهائية التي يتم إنشاؤها خلال عملية التوفير شهادة طبقة مآخذ التوصيل الآمنة (SSL) فقط لـ \*.commerce.dynamics.com. </span><span class="sxs-lookup"><span data-stu-id="a9e47-111">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="a9e47-112">ولا يدعم SSL للمجالات المُخصصة.</span><span class="sxs-lookup"><span data-stu-id="a9e47-112">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="a9e47-113">وبالتالي، يجب عليك إنهاء SSL للمجالات المخصصة في CDN الخاصة بك وإعادة توجيه حركة النقل من CDN إلى اسم المضيف أو النقطة النهائية التي قام Commerce بإنشائها.</span><span class="sxs-lookup"><span data-stu-id="a9e47-113">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="a9e47-114">بالإضافة إلى ذلك، يتم عرض *الإحصاءات* (إما JavaScript أو ملفات أوراق الأنماط المتتالية \[CSS\]) من Commerce من النقطة النهائية الذي قام Commerce بإنشاءها (\*.commerce.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="a9e47-114">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="a9e47-115">يُمكن تخزين هذه الإحصائيات مؤقتًا فقط في حالة إذا تم وضع اسم المضيف أو نقطة النهاية التي قام Commerce بإنشائها بعد CDN.</span><span class="sxs-lookup"><span data-stu-id="a9e47-115">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="a9e47-116">إعداد نظام إدارة الأوامر الموزعة (SSL)</span><span class="sxs-lookup"><span data-stu-id="a9e47-116">Set up SSL</span></span>

<span data-ttu-id="a9e47-117">وللمساعدة في ضمان إعداد SSL، وأنه قد تم تخزين الإحصائيات مؤقتًا، يجب عليك تكوين CDN الخاص بك بحيث يكون مقترنًا باسم المضيف الذي قام Commerce بإنشاءه للبيئة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="a9e47-117">To help guarantee that SSL is set up, and that statics are cached, you must configure your CDN so that it is associated with the host name that Commerce generated for your environment.</span></span> <span data-ttu-id="a9e47-118">كما يجب عليك أيضًا تخزين الأنماط التالية للإحصائيات مؤقتًا فقط:</span><span class="sxs-lookup"><span data-stu-id="a9e47-118">You must also cache the following pattern for statics only:</span></span> 

<span data-ttu-id="a9e47-119">/\_msdyn365/\_scnr/\*</span><span class="sxs-lookup"><span data-stu-id="a9e47-119">/\_msdyn365/\_scnr/\*</span></span>

<span data-ttu-id="a9e47-120">بعد توفير بيئة Commerce الخاصة بك مع المجال المخصص الذي تم توفيره، أو بعد أن تقوم بتوفير مجال مخصص للبيئة الخاصة بك باستخدام طلب خدمة، قم بالإشارة إلى مجالك المخصص لاسم المضيف أو النقطة النهائية التي قام Commerce بإنشائها.</span><span class="sxs-lookup"><span data-stu-id="a9e47-120">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, point your custom domain to the host name or endpoint that Commerce generated.</span></span>

<span data-ttu-id="a9e47-121">وكما سبق ذكره، يدعم اسم المضيف أو نقطة النهاية التي تم إنشائها شهادة SSL فقط لـ \*.commerce.dynamics.com. </span><span class="sxs-lookup"><span data-stu-id="a9e47-121">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="a9e47-122">ولا يدعم SSL للمجالات المُخصصة.</span><span class="sxs-lookup"><span data-stu-id="a9e47-122">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="a9e47-123">خدمات CDN</span><span class="sxs-lookup"><span data-stu-id="a9e47-123">CDN services</span></span>

<span data-ttu-id="a9e47-124">يُمكن استخدام أي خدمة من خدمات CDN مع بيئة Commerce.</span><span class="sxs-lookup"><span data-stu-id="a9e47-124">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="a9e47-125">وفيما يلي مثالين:</span><span class="sxs-lookup"><span data-stu-id="a9e47-125">Here are two examples:</span></span>

- <span data-ttu-id="a9e47-126">**Microsoft Azure Front Door Service** – حل Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="a9e47-126">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="a9e47-127">للمزيد من المعلومات حول Azure Front Door Service، راجع [وثائق Azure Front Door Service](https://docs.microsoft.com/azure/frontdoor/).</span><span class="sxs-lookup"><span data-stu-id="a9e47-127">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/).</span></span>
- <span data-ttu-id="a9e47-128">**Akamai Dynamic Site Accelerator** – للمزيد من المعلومات، راجع [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span><span class="sxs-lookup"><span data-stu-id="a9e47-128">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="a9e47-129">إعداد CDN</span><span class="sxs-lookup"><span data-stu-id="a9e47-129">CDN setup</span></span>

<span data-ttu-id="a9e47-130">تتكون عملية إعداد CDN من الخطوات العامة التالية:</span><span class="sxs-lookup"><span data-stu-id="a9e47-130">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="a9e47-131">إضافة مضيف واجهة أمامية.</span><span class="sxs-lookup"><span data-stu-id="a9e47-131">Add a front-end host.</span></span>
1. <span data-ttu-id="a9e47-132">تكوين وعاء خلفي.</span><span class="sxs-lookup"><span data-stu-id="a9e47-132">Configure a backend pool.</span></span>
1. <span data-ttu-id="a9e47-133">إعداد القواعد للتوجيه والتخزين المؤقت.</span><span class="sxs-lookup"><span data-stu-id="a9e47-133">Set up rules for routing and caching.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="a9e47-134">إضافة مضيف واجهة أمامية</span><span class="sxs-lookup"><span data-stu-id="a9e47-134">Add a front-end host</span></span>

<span data-ttu-id="a9e47-135">يُمكن استخدام أي خدمة من خدمات CDN، ولكن بالنسبة للمثال الموجود في هذا الموضوع، يتم استخدام Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="a9e47-135">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="a9e47-136">للحصول على معلومات حول كيفية إعداد Azure Front Door Service، راجع [Quickstart: إنشاء Front Door لتطبيق الويب العمومي المتوفرة بشكل كبير](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span><span class="sxs-lookup"><span data-stu-id="a9e47-136">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a><span data-ttu-id="a9e47-137">تكوين وعاء خلفي في Azure Front Door Service</span><span class="sxs-lookup"><span data-stu-id="a9e47-137">Configure a backend pool in Azure Front Door Service</span></span>

<span data-ttu-id="a9e47-138">لتكوين وعاء خلفي في Azure Front Door Service، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="a9e47-138">To configure a backend pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="a9e47-139">أضف **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** إلى الوعاء الخلفي كمضيف مخصص له عنوان مضيف خلفي فارغ.</span><span class="sxs-lookup"><span data-stu-id="a9e47-139">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a backend pool as a custom host that has an empty backend host header.</span></span>
1. <span data-ttu-id="a9e47-140">تحت **موازنة التحميل**، اترك القيم الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="a9e47-140">Under **Load balancing**, leave the default values.</span></span>

<span data-ttu-id="a9e47-141">يُبين الرسم التوضيحي التالي مربع الحوار **إضافة وعاء خلفي** في Azure Front Door Service مع إدخال اسم مضيف وعاء خلفي.</span><span class="sxs-lookup"><span data-stu-id="a9e47-141">The following illustration shows the **Add a backend** dialog box in Azure Front Door Service with the backend host name entered.</span></span>

![إضافة مربع حوار وعاء خلفي](./media/CDN_BackendPool.png)

<span data-ttu-id="a9e47-143">يُبين الرسم التوضيحي التالي مربع الحوار **إضافة وعاء خلفي** في Azure Front Door Service مع قيم موازنة الحمل الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="a9e47-143">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service with the default load balancing values.</span></span>

![إضافة مربع حوار وعاء خلفي يتبع](./media/CDN_BackendPool_2.png)

### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="a9e47-145">إعداد القواعد في Azure Front Door Service</span><span class="sxs-lookup"><span data-stu-id="a9e47-145">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="a9e47-146">لإعداد قاعدة التوجيه في Azure Front Door Service، اتبع الخطوات التالية. </span><span class="sxs-lookup"><span data-stu-id="a9e47-146">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="a9e47-147">إضافة قاعدة التوجيه.</span><span class="sxs-lookup"><span data-stu-id="a9e47-147">Add a routing rule.</span></span>
1. <span data-ttu-id="a9e47-148">في الحقل **الاسم** ، أدخل **‏افتراضي**.</span><span class="sxs-lookup"><span data-stu-id="a9e47-148">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="a9e47-149">في حقل **البروتوكول المقبول** ، حدد **HTTP وHTTPS**.</span><span class="sxs-lookup"><span data-stu-id="a9e47-149">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="a9e47-150">في حقل **مضيفو الواجهة الأمامية** ، ادخل **dynamics-ecom-tenant-name.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="a9e47-150">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="a9e47-151">تحت **النماذج المطلوب مطابقتها**، في الحقل العلوي، ادخل **/\***.</span><span class="sxs-lookup"><span data-stu-id="a9e47-151">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="a9e47-152">تحت **تفاصيل التوجيه**، قم بتعيين خيار **نوع التوجيه** إلى **للأمام**.</span><span class="sxs-lookup"><span data-stu-id="a9e47-152">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="a9e47-153">في حقل **الوعاء الخلفي** ،حدد **ecom-backend**. </span><span class="sxs-lookup"><span data-stu-id="a9e47-153">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="a9e47-154">في مجموعة حقل **بروتوكول إعادة التوجيه** ،حدد خيار **مطابقة الطلب**.</span><span class="sxs-lookup"><span data-stu-id="a9e47-154">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="a9e47-155">قم بتعيين خيار **إعادة كتابة عنوان URL** إلى **مُعطل**.</span><span class="sxs-lookup"><span data-stu-id="a9e47-155">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="a9e47-156">قم بتعيين خيار **التخزين المؤقت** إلى **مُعطل**.</span><span class="sxs-lookup"><span data-stu-id="a9e47-156">Set the **Caching** option to **Disabled**.</span></span>

<span data-ttu-id="a9e47-157">لإعداد قاعدة التخزين المؤقت في Azure Front Door Service، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="a9e47-157">To set up a caching rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="a9e47-158">إضافة قاعدة التخزين المؤقت.</span><span class="sxs-lookup"><span data-stu-id="a9e47-158">Add a caching rule.</span></span>
1. <span data-ttu-id="a9e47-159">في الحقل **الاسم** ، أدخل **‏الإحصائيات**.</span><span class="sxs-lookup"><span data-stu-id="a9e47-159">In the **Name** field, enter **statics**.</span></span>
1. <span data-ttu-id="a9e47-160">في حقل **البروتوكول المقبول** ، حدد **HTTP وHTTPS**.</span><span class="sxs-lookup"><span data-stu-id="a9e47-160">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="a9e47-161">في حقل **مضيفو الواجهة الأمامية** ، ادخل **dynamics-ecom-tenant-name.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="a9e47-161">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="a9e47-162">تحت **النماذج المطلوب مطابقتها** ، في الحقل العلوي، **/\_msdyn365/\_scnr/\***.</span><span class="sxs-lookup"><span data-stu-id="a9e47-162">Under **Patterns to match**, in the upper field, **/\_msdyn365/\_scnr/\***.</span></span>
1. <span data-ttu-id="a9e47-163">تحت **تفاصيل التوجيه**، قم بتعيين خيار **نوع التوجيه** إلى **للأمام**.</span><span class="sxs-lookup"><span data-stu-id="a9e47-163">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="a9e47-164">في حقل **الوعاء الخلفي** ،حدد **ecom-backend**. </span><span class="sxs-lookup"><span data-stu-id="a9e47-164">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="a9e47-165">في مجموعة حقل **بروتوكول إعادة التوجيه** ،حدد خيار **مطابقة الطلب**.</span><span class="sxs-lookup"><span data-stu-id="a9e47-165">In the **Forwarding protocol** field group, select the **Match request** option.</span></span>
1. <span data-ttu-id="a9e47-166">قم بتعيين خيار **إعادة كتابة عنوان URL** إلى **مُعطل**.</span><span class="sxs-lookup"><span data-stu-id="a9e47-166">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="a9e47-167">قم بتعيين خيار **التخزين المؤقت** إلى **مُعطل**.</span><span class="sxs-lookup"><span data-stu-id="a9e47-167">Set the **Caching** option to **Disabled**.</span></span>
1. <span data-ttu-id="a9e47-168">في حقل **سلوك التخزين المؤقت لسلسلة الاستعلام** ،حدد **تخزين مؤقت لكل عنوان URL فريد**.</span><span class="sxs-lookup"><span data-stu-id="a9e47-168">In the **Query string caching behavior** field, select **Cache every unique URL**.</span></span>
1. <span data-ttu-id="a9e47-169">في مجموعة حقل **الضغط الديناميكي** ،حدد خيار **مُمكّن**.</span><span class="sxs-lookup"><span data-stu-id="a9e47-169">In the **Dynamic compression** field group, select the **Enabled** option.</span></span>

<span data-ttu-id="a9e47-170">يُبين الرسم التوضيحي التالي مربع الحوار **إضافة قاعدة** في Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="a9e47-170">The following illustration shows the **Add a rule** dialog box in Azure Front Door Service.</span></span>

![إضافة مربع حوار قاعدة](./media/CDN_CachingRule.png)

> [!WARNING]
> <span data-ttu-id="a9e47-172">إذا كان المجال الذي ستستخدمه نشطًا ومباشرًا، فأنشئ تذكرة دعم من الإطار المتجانب **الدعم** في [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) للحصول على المساعدة لخطواتك التالية.</span><span class="sxs-lookup"><span data-stu-id="a9e47-172">If the domain that you will use is already active and live, create a support ticket from the **Support** tile in [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) to get assistance for your next steps.</span></span> <span data-ttu-id="a9e47-173">لمزيد من المعلومات، راجع [الحصول على الدعم لتطبيقات Finance and Operations أو Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="a9e47-173">For more information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

<span data-ttu-id="a9e47-174">إذا كان مجالك جديدًا وليس مجالاً مباشرًا موجودًا بشكل مسبق، فيمكنك إضافة مجال مخصص إلى تكوين Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="a9e47-174">If your domain is new and is not a pre-existing live domain, you can add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="a9e47-175">سيؤدي ذلك إلى تمكين حركة مرور الويب لتوجيه موقعك عبر مثيل Azure Front Door.</span><span class="sxs-lookup"><span data-stu-id="a9e47-175">This will enable web traffic to direct to your site via the Azure Front Door instance.</span></span> <span data-ttu-id="a9e47-176">لإضافة مجال مخصص (على سبيل المثال، `www.fabrikam.com`)، يجب عليك تكوين اسم متعارف عليه (CNAME) للمجال.</span><span class="sxs-lookup"><span data-stu-id="a9e47-176">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="a9e47-177">يُبين الرسم التوضيحي التالي مربع الحوار **تكوين CNAME** في Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="a9e47-177">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![مربع حوار تكوين CNAME](./media/CNAME_Configuration.png)

<span data-ttu-id="a9e47-179">يُمكنك استخدام Azure Front Door Service لإدارة الشهادة، أو يُمكنك استخدام شهادتك الخاصة للمجال المخصص. </span><span class="sxs-lookup"><span data-stu-id="a9e47-179">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="a9e47-180">يُبين الرسم التوضيحي التالي مربع الحوار **HTTP للمجال المخصص** في Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="a9e47-180">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![مربع حوار HTTP للمجال المخصص](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="a9e47-182">للحصول على إرشادات مفصلة حول إضافة مجال مخصص إلى Azure Front Door، راجع [إضافة مجال مخصص إلى Front Door](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span><span class="sxs-lookup"><span data-stu-id="a9e47-182">For detailed instructions on adding a custom domain to your Azure Front Door, see [Add a custom domain to your Front Door](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span></span>

<span data-ttu-id="a9e47-183">يجب الآن تكوين CDN بشكل صحيح بحيث يُمكن استخدامه مع موقع Commerce الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="a9e47-183">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a9e47-184">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="a9e47-184">Additional resources</span></span>

[<span data-ttu-id="a9e47-185">خيارات تنفيذ شبكة تسليم المحتويات</span><span class="sxs-lookup"><span data-stu-id="a9e47-185">Content delivery network implementation options</span></span>](cdn-options.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
