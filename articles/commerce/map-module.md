---
title: وحدة الخريطة
description: يتناول هذا الموضوع الوحدات النمطية للخريطة ويصف كيفية تكوينها في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: ca531e6cbf0a1044b0a13e5cdf42c7b4f0498fe5
ms.sourcegitcommit: 629988f1a704d62648d98649056931b8c33b9e08
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/14/2020
ms.locfileid: "3811174"
---
# <a name="map-module"></a><span data-ttu-id="884e7-103">وحدة الخريطة</span><span class="sxs-lookup"><span data-stu-id="884e7-103">Map module</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="884e7-104">يتناول هذا الموضوع الوحدات النمطية للخريطة ويصف كيفية تكوينها في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="884e7-104">This topic covers map modules and describes how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="884e7-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="884e7-105">Overview</span></span>

<span data-ttu-id="884e7-106">تظهر الوحدة النمطية للخريطة مواقع المتاجر في خريطة تفاعلية يتم عرضها باستخدام [عنصر تحكم ويب V8 لخرائط Bing](https://docs.microsoft.com/bingmaps/v8-web-control/).</span><span class="sxs-lookup"><span data-stu-id="884e7-106">A map module shows the locations of stores on an interactive map that is rendered by using the [Bing Maps V8 Web Control](https://docs.microsoft.com/bingmaps/v8-web-control/).</span></span> <span data-ttu-id="884e7-107">يلزم إدخال مفتاح API لخرائط Bing ويجب إضافته إلى صفحة المعلمات المشتركة في مركز Commerce الرئيسي.‬</span><span class="sxs-lookup"><span data-stu-id="884e7-107">A Bing Maps API key is required and must be added to the shared parameters page in Commerce headquarters.</span></span> <span data-ttu-id="884e7-108">توفر الوحدات النمطية للخريطة طرق عرض مختلفة، مثل الطريق والجو والشارع، يمكن للمستخدمين تحديدها لعرض مواقع الخريطة.</span><span class="sxs-lookup"><span data-stu-id="884e7-108">Map modules provide different views, such as Road, Aerial, and Streetside, that users can select to view map locations.</span></span> <span data-ttu-id="884e7-109">كما تسمح أيضًا بالتفاعلات مثل التكبير/التصغير واستخدام موقع المستخدم.</span><span class="sxs-lookup"><span data-stu-id="884e7-109">They also allow for interactions such as zooming and using the user's location.</span></span>

<span data-ttu-id="884e7-110">تعمل الوحدة النمطية للخريطة بالتزامن مع الوحدة النمطية لمحدد المتجر لتحديد المواقع الجغرافية للمتاجر التي يجب عرضها على الخريطة.</span><span class="sxs-lookup"><span data-stu-id="884e7-110">A map module works in conjunction with the store selector module to determine the geographic locations of stores that must be rendered on a map.</span></span> <span data-ttu-id="884e7-111">ويتفاعل محدد المتجر والوحدات النمطية للخريطة عندما يقوم المستخدم بتحديد أحد المتاجر في إحدى هذه الوحدات في صفحة موقع.</span><span class="sxs-lookup"><span data-stu-id="884e7-111">Store selector and map modules interact when a user selects a store in one of those modules on a site page.</span></span> <span data-ttu-id="884e7-112">يمكن توسيع الوحدات النمطية للخريطة لسيناريوهات أخرى، تتجاوز التفاعل مع وحدات محدد المتجر.</span><span class="sxs-lookup"><span data-stu-id="884e7-112">Map modules can be extended for other scenarios, beyond interaction with store selector modules.</span></span> <span data-ttu-id="884e7-113">ومع ذلك، يلزم تخصيص الوحدة النمطية.</span><span class="sxs-lookup"><span data-stu-id="884e7-113">However, module customization is required.</span></span>

<span data-ttu-id="884e7-114">تم تقديم الوحدة النمطية للخريط في الإصدار 10.0.13 من Commerce.</span><span class="sxs-lookup"><span data-stu-id="884e7-114">The map module was introduced in Commerce version 10.0.13.</span></span>

<span data-ttu-id="884e7-115">تعرض الصورة التالية مثالاً عن وحدة الخريطة المستخدمة في صفحة مواقع المتجر.</span><span class="sxs-lookup"><span data-stu-id="884e7-115">The following image shows an example of a map module that is used on a store locations page.</span></span>

![مثال لوحدة محدِّد المتجر](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a><span data-ttu-id="884e7-117">خصائص الوحدة النمطية</span><span class="sxs-lookup"><span data-stu-id="884e7-117">Module properties</span></span>

| <span data-ttu-id="884e7-118">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="884e7-118">Property name</span></span>             | <span data-ttu-id="884e7-119">قيمة</span><span class="sxs-lookup"><span data-stu-id="884e7-119">Value</span></span>                 | <span data-ttu-id="884e7-120">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="884e7-120">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="884e7-121">العنوان</span><span class="sxs-lookup"><span data-stu-id="884e7-121">Heading</span></span> | <span data-ttu-id="884e7-122">النص</span><span class="sxs-lookup"><span data-stu-id="884e7-122">Text</span></span> | <span data-ttu-id="884e7-123">عنوان الوحدة النمطية.</span><span class="sxs-lookup"><span data-stu-id="884e7-123">The heading for the module.</span></span> |
| <span data-ttu-id="884e7-124">خيارات دبوس التثبيت: أيقونة افتراضية</span><span class="sxs-lookup"><span data-stu-id="884e7-124">Pushpin options: Default icon</span></span> | <span data-ttu-id="884e7-125">صورة</span><span class="sxs-lookup"><span data-stu-id="884e7-125">Image</span></span> | <span data-ttu-id="884e7-126">صورة رمز دبوس التثبيت المطلوب استخدامها للمتاجر المعروضة على الخريطة.</span><span class="sxs-lookup"><span data-stu-id="884e7-126">The pushpin symbol image to use for stores that are shown on a map.</span></span> |
| <span data-ttu-id="884e7-127">خيارات دبوس التثبيت: أيقونة نشطة</span><span class="sxs-lookup"><span data-stu-id="884e7-127">Pushpin options: Active icon</span></span> | <span data-ttu-id="884e7-128">صورة</span><span class="sxs-lookup"><span data-stu-id="884e7-128">Image</span></span> | <span data-ttu-id="884e7-129">صورة رمز دبوس التثبيت المطلوب استخدامها لمتجر محدد على الخريطة.</span><span class="sxs-lookup"><span data-stu-id="884e7-129">The pushpin symbol image to use for a store that is selected on a map.</span></span> |
| <span data-ttu-id="884e7-130">خيارات دبوس التثبيت: لون الأيقونة الافتراضية</span><span class="sxs-lookup"><span data-stu-id="884e7-130">Pushpin options: Default icon color</span></span> | <span data-ttu-id="884e7-131">سلسلة أحرف</span><span class="sxs-lookup"><span data-stu-id="884e7-131">Character string</span></span> | <span data-ttu-id="884e7-132">النص أو القيمة الست العشرية للون رموز دبابيس التثبيت على الخريطة.</span><span class="sxs-lookup"><span data-stu-id="884e7-132">The text or hexadecimal value for the color of pushpin symbols on a map.</span></span> |
| <span data-ttu-id="884e7-133">خيارات دبوس التثبيت: لون الأيقونة النشطة</span><span class="sxs-lookup"><span data-stu-id="884e7-133">Pushpin options: Active icon color</span></span> | <span data-ttu-id="884e7-134">سلسلة أحرف</span><span class="sxs-lookup"><span data-stu-id="884e7-134">Character string</span></span> | <span data-ttu-id="884e7-135">النص أو القيمة الست العشرية للون رموز دبابيس التثبيت المحددة على الخريطة.</span><span class="sxs-lookup"><span data-stu-id="884e7-135">The text or hexadecimal value for the color of selected pushpin symbols on a map.</span></span> |
| <span data-ttu-id="884e7-136">إظهار الفهرس</span><span class="sxs-lookup"><span data-stu-id="884e7-136">Show index</span></span> | <span data-ttu-id="884e7-137">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="884e7-137">**True** or **False**</span></span> | <span data-ttu-id="884e7-138">إذا تم تعيين هذه الخاصية إلى **صواب**، فسيظهر في الفهرس كل رمز دبوس تثبيت يشير إلى متجر.</span><span class="sxs-lookup"><span data-stu-id="884e7-138">If this property is set to **True**, every pushpin symbol that indicates a store will show an index.</span></span> <span data-ttu-id="884e7-139">سيتطابق هذا الفهرس مع الفهرس الموجود في طريقة عرض القائمة التي تعرضها الوحدة النمطية لمحدد المتجر.</span><span class="sxs-lookup"><span data-stu-id="884e7-139">This index will match the index in the list view that the store selector module shows.</span></span> |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a><span data-ttu-id="884e7-140">إضافة عناوين URL مواقع للتعيين المسموح بها إلى توجيهات سياسة أمان محتوى الموقع</span><span class="sxs-lookup"><span data-stu-id="884e7-140">Add allowed mapping URLs to a site's content security policy directives</span></span>

<span data-ttu-id="884e7-141">لكي تتفاعل الوحدة النمطية للخريطة مع خرائط Bing، يجب عليك التأكد من أن عناوين URL للتعيين التالية مسموحة (ما يعرف أيضًا بأنها "مدرجة في قائمة بيضاء") وفق سياسة أمان محتوى الموقع (CSP).‬</span><span class="sxs-lookup"><span data-stu-id="884e7-141">For the maps module to interact with Bing Maps, you must ensure that the following mapping URLs are allowed (also known as "whitelisted") per your site's content security policy (CSP).</span></span> <span data-ttu-id="884e7-142">يتم إجراء هذا الإعداد في منشئ مواقع Commerce، عن طريق إضافة عناوين URL مسموح بها إلى توجيهات CSP متعددة للموقع (على سبيل المثال، **img-src**).</span><span class="sxs-lookup"><span data-stu-id="884e7-142">This setup is done in Commerce site builder, by adding allowed URLs to various site CSP directives (for example, **img-src**).</span></span> <span data-ttu-id="884e7-143">لمزيد من المعلومات، راجع [سياسة أمان المحتوى](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="884e7-143">For more information, see [Content security policy](manage-csp.md).</span></span> 

- <span data-ttu-id="884e7-144">إلى التوجيه **connect-src**، أضف **&#42;.bing.com**.</span><span class="sxs-lookup"><span data-stu-id="884e7-144">To the **connect-src** directive, add **&#42;.bing.com**.</span></span>
- <span data-ttu-id="884e7-145">إلى التوجيه **img-src**، أضف **&#42;.virtualearth.net**.</span><span class="sxs-lookup"><span data-stu-id="884e7-145">To the **img-src** directive, add **&#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="884e7-146">إلى التوجيه **script-src**، أضف **&#42;.bing.com, &#42;.virtualearth.net**.</span><span class="sxs-lookup"><span data-stu-id="884e7-146">To the **script-src** directive, add **&#42;.bing.com, &#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="884e7-147">إلى التوجيه **script style-src**، أضف **&#42;.bing.com**.</span><span class="sxs-lookup"><span data-stu-id="884e7-147">To the **script style-src** directive, add **&#42;.bing.com**.</span></span>

## <a name="add-a-map-module-to-a-page"></a><span data-ttu-id="884e7-148">إضافة وحدة خريطة إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="884e7-148">Add a map module to a page</span></span>

<span data-ttu-id="884e7-149">للحصول علي معلومات مفصلة حول كيفيه تكوين وحدة نمطية للخريطة على صفحة، راجع [الوحدة النمطية لمحدد المتجر](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="884e7-149">For detailed information about how to configure a map module on a page, see [Store selector module](store-selector.md).</span></span> 
 
## <a name="additional-resources"></a><span data-ttu-id="884e7-150">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="884e7-150">Additional resources</span></span>

[<span data-ttu-id="884e7-151">نظرة عامة حول أدوات البداية</span><span class="sxs-lookup"><span data-stu-id="884e7-151">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="884e7-152">الوحدة النمطية لصندوق الشراء</span><span class="sxs-lookup"><span data-stu-id="884e7-152">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="884e7-153">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="884e7-153">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="884e7-154">الوحدة النمطية لمحدد المتجر</span><span class="sxs-lookup"><span data-stu-id="884e7-154">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="884e7-155">إدارة خرائط Bing لمؤسستك</span><span class="sxs-lookup"><span data-stu-id="884e7-155">Manage Bing Maps for your organization</span></span>](./dev-itpro/manage-bing-maps.md)

[<span data-ttu-id="884e7-156">عنصر تحكم ويب V8 لخرائط Bing</span><span class="sxs-lookup"><span data-stu-id="884e7-156">Bing Maps V8 Web Control</span></span>](https://docs.microsoft.com/bingmaps/v8-web-control/)
