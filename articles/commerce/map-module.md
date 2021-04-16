---
title: وحدة الخريطة
description: يتناول هذا الموضوع الوحدات النمطية للخريطة ويصف كيفية تكوينها في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: b8c3ab0653fd5e3561d0bfbe85624d912756e2be
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794177"
---
# <a name="map-module"></a><span data-ttu-id="75960-103">وحدة الخريطة</span><span class="sxs-lookup"><span data-stu-id="75960-103">Map module</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="75960-104">يتناول هذا الموضوع الوحدات النمطية للخريطة ويصف كيفية تكوينها في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="75960-104">This topic covers map modules and describes how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="75960-105">تظهر الوحدة النمطية للخريطة مواقع المتاجر في خريطة تفاعلية يتم عرضها باستخدام [عنصر تحكم ويب V8 لخرائط Bing](https://docs.microsoft.com/bingmaps/v8-web-control/).</span><span class="sxs-lookup"><span data-stu-id="75960-105">A map module shows the locations of stores on an interactive map that is rendered by using the [Bing Maps V8 Web Control](https://docs.microsoft.com/bingmaps/v8-web-control/).</span></span> <span data-ttu-id="75960-106">يلزم إدخال مفتاح API لخرائط Bing ويجب إضافته إلى صفحة المعلمات المشتركة في مركز Commerce الرئيسي.‬</span><span class="sxs-lookup"><span data-stu-id="75960-106">A Bing Maps API key is required and must be added to the shared parameters page in Commerce headquarters.</span></span> <span data-ttu-id="75960-107">توفر الوحدات النمطية للخريطة طرق عرض مختلفة، مثل الطريق والجو والشارع، يمكن للمستخدمين تحديدها لعرض مواقع الخريطة.</span><span class="sxs-lookup"><span data-stu-id="75960-107">Map modules provide different views, such as Road, Aerial, and Streetside, that users can select to view map locations.</span></span> <span data-ttu-id="75960-108">كما تسمح أيضًا بالتفاعلات مثل التكبير/التصغير واستخدام موقع المستخدم.</span><span class="sxs-lookup"><span data-stu-id="75960-108">They also allow for interactions such as zooming and using the user's location.</span></span>

<span data-ttu-id="75960-109">تعمل الوحدة النمطية للخريطة بالتزامن مع الوحدة النمطية لمحدد المتجر لتحديد المواقع الجغرافية للمتاجر التي يجب عرضها على الخريطة.</span><span class="sxs-lookup"><span data-stu-id="75960-109">A map module works in conjunction with the store selector module to determine the geographic locations of stores that must be rendered on a map.</span></span> <span data-ttu-id="75960-110">ويتفاعل محدد المتجر والوحدات النمطية للخريطة عندما يقوم المستخدم بتحديد أحد المتاجر في إحدى هذه الوحدات في صفحة موقع.</span><span class="sxs-lookup"><span data-stu-id="75960-110">Store selector and map modules interact when a user selects a store in one of those modules on a site page.</span></span> <span data-ttu-id="75960-111">يمكن توسيع الوحدات النمطية للخريطة لسيناريوهات أخرى، تتجاوز التفاعل مع وحدات محدد المتجر.</span><span class="sxs-lookup"><span data-stu-id="75960-111">Map modules can be extended for other scenarios, beyond interaction with store selector modules.</span></span> <span data-ttu-id="75960-112">ومع ذلك، يلزم تخصيص الوحدة النمطية.</span><span class="sxs-lookup"><span data-stu-id="75960-112">However, module customization is required.</span></span>

> [!NOTE]
> <span data-ttu-id="75960-113">تتوفر الوحدة النمطية للخريطة في Dynamics 365 Commerce الإصدار 10.0.13.</span><span class="sxs-lookup"><span data-stu-id="75960-113">The map module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="75960-114">تعرض الصورة التالية مثالاً عن وحدة الخريطة المستخدمة في صفحة مواقع المتجر.</span><span class="sxs-lookup"><span data-stu-id="75960-114">The following image shows an example of a map module that is used on a store locations page.</span></span>

![مثال لوحدة محدِّد المتجر](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a><span data-ttu-id="75960-116">خصائص الوحدة النمطية</span><span class="sxs-lookup"><span data-stu-id="75960-116">Module properties</span></span>

| <span data-ttu-id="75960-117">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="75960-117">Property name</span></span>             | <span data-ttu-id="75960-118">قيمة</span><span class="sxs-lookup"><span data-stu-id="75960-118">Value</span></span>                 | <span data-ttu-id="75960-119">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="75960-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="75960-120">العنوان</span><span class="sxs-lookup"><span data-stu-id="75960-120">Heading</span></span> | <span data-ttu-id="75960-121">النص</span><span class="sxs-lookup"><span data-stu-id="75960-121">Text</span></span> | <span data-ttu-id="75960-122">عنوان الوحدة النمطية.</span><span class="sxs-lookup"><span data-stu-id="75960-122">The heading for the module.</span></span> |
| <span data-ttu-id="75960-123">خيارات دبوس التثبيت: أيقونة افتراضية</span><span class="sxs-lookup"><span data-stu-id="75960-123">Pushpin options: Default icon</span></span> | <span data-ttu-id="75960-124">صورة</span><span class="sxs-lookup"><span data-stu-id="75960-124">Image</span></span> | <span data-ttu-id="75960-125">صورة رمز دبوس التثبيت المطلوب استخدامها للمتاجر المعروضة على الخريطة.</span><span class="sxs-lookup"><span data-stu-id="75960-125">The pushpin symbol image to use for stores that are shown on a map.</span></span> |
| <span data-ttu-id="75960-126">خيارات دبوس التثبيت: أيقونة نشطة</span><span class="sxs-lookup"><span data-stu-id="75960-126">Pushpin options: Active icon</span></span> | <span data-ttu-id="75960-127">صورة</span><span class="sxs-lookup"><span data-stu-id="75960-127">Image</span></span> | <span data-ttu-id="75960-128">صورة رمز دبوس التثبيت المطلوب استخدامها لمتجر محدد على الخريطة.</span><span class="sxs-lookup"><span data-stu-id="75960-128">The pushpin symbol image to use for a store that is selected on a map.</span></span> |
| <span data-ttu-id="75960-129">خيارات دبوس التثبيت: لون الأيقونة الافتراضية</span><span class="sxs-lookup"><span data-stu-id="75960-129">Pushpin options: Default icon color</span></span> | <span data-ttu-id="75960-130">سلسلة أحرف</span><span class="sxs-lookup"><span data-stu-id="75960-130">Character string</span></span> | <span data-ttu-id="75960-131">النص أو القيمة الست العشرية للون رموز دبابيس التثبيت على الخريطة.</span><span class="sxs-lookup"><span data-stu-id="75960-131">The text or hexadecimal value for the color of pushpin symbols on a map.</span></span> |
| <span data-ttu-id="75960-132">خيارات دبوس التثبيت: لون الأيقونة النشطة</span><span class="sxs-lookup"><span data-stu-id="75960-132">Pushpin options: Active icon color</span></span> | <span data-ttu-id="75960-133">سلسلة أحرف</span><span class="sxs-lookup"><span data-stu-id="75960-133">Character string</span></span> | <span data-ttu-id="75960-134">النص أو القيمة الست العشرية للون رموز دبابيس التثبيت المحددة على الخريطة.</span><span class="sxs-lookup"><span data-stu-id="75960-134">The text or hexadecimal value for the color of selected pushpin symbols on a map.</span></span> |
| <span data-ttu-id="75960-135">إظهار الفهرس</span><span class="sxs-lookup"><span data-stu-id="75960-135">Show index</span></span> | <span data-ttu-id="75960-136">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="75960-136">**True** or **False**</span></span> | <span data-ttu-id="75960-137">إذا تم تعيين هذه الخاصية إلى **صواب**، فسيظهر في الفهرس كل رمز دبوس تثبيت يشير إلى متجر.</span><span class="sxs-lookup"><span data-stu-id="75960-137">If this property is set to **True**, every pushpin symbol that indicates a store will show an index.</span></span> <span data-ttu-id="75960-138">سيتطابق هذا الفهرس مع الفهرس الموجود في طريقة عرض القائمة التي تعرضها الوحدة النمطية لمحدد المتجر.</span><span class="sxs-lookup"><span data-stu-id="75960-138">This index will match the index in the list view that the store selector module shows.</span></span> |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a><span data-ttu-id="75960-139">إضافة عناوين URL مواقع للتعيين المسموح بها إلى توجيهات سياسة أمان محتوى الموقع</span><span class="sxs-lookup"><span data-stu-id="75960-139">Add allowed mapping URLs to a site's content security policy directives</span></span>

<span data-ttu-id="75960-140">لكي تتفاعل الوحدة النمطية للخريطة مع خرائط Bing، يجب عليك التأكد من أن عناوين URL للتعيين التالية مسموح بها وفقًا لسياسة أمان محتوى الموقع (CSP) الخاص بك.‬</span><span class="sxs-lookup"><span data-stu-id="75960-140">For the maps module to interact with Bing Maps, you must ensure that the following mapping URLs are allowed per your site's content security policy (CSP).</span></span> <span data-ttu-id="75960-141">يتم إجراء هذا الإعداد في منشئ مواقع Commerce، عن طريق إضافة عناوين URL مسموح بها إلى توجيهات CSP متعددة للموقع (على سبيل المثال، **img-src**).</span><span class="sxs-lookup"><span data-stu-id="75960-141">This setup is done in Commerce site builder, by adding allowed URLs to various site CSP directives (for example, **img-src**).</span></span> <span data-ttu-id="75960-142">لمزيد من المعلومات، راجع [سياسة أمان المحتوى](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="75960-142">For more information, see [Content security policy](manage-csp.md).</span></span> 

- <span data-ttu-id="75960-143">إلى التوجيه **connect-src**، أضف **&#42;.bing.com**.</span><span class="sxs-lookup"><span data-stu-id="75960-143">To the **connect-src** directive, add **&#42;.bing.com**.</span></span>
- <span data-ttu-id="75960-144">إلى التوجيه **img-src**، أضف **&#42;.virtualearth.net**.</span><span class="sxs-lookup"><span data-stu-id="75960-144">To the **img-src** directive, add **&#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="75960-145">إلى التوجيه **script-src**، أضف **&#42;.bing.com, &#42;.virtualearth.net**.</span><span class="sxs-lookup"><span data-stu-id="75960-145">To the **script-src** directive, add **&#42;.bing.com, &#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="75960-146">إلى التوجيه **script style-src**، أضف **&#42;.bing.com**.</span><span class="sxs-lookup"><span data-stu-id="75960-146">To the **script style-src** directive, add **&#42;.bing.com**.</span></span>

## <a name="add-a-map-module-to-a-page"></a><span data-ttu-id="75960-147">إضافة وحدة خريطة إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="75960-147">Add a map module to a page</span></span>

<span data-ttu-id="75960-148">للحصول على معلومات مفصلة حول كيفيه تكوين وحدة نمطية للخريطة على صفحة، راجع [الوحدة النمطية لمحدد المتجر](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="75960-148">For detailed information about how to configure a map module on a page, see [Store selector module](store-selector.md).</span></span> 
 
## <a name="additional-resources"></a><span data-ttu-id="75960-149">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="75960-149">Additional resources</span></span>

[<span data-ttu-id="75960-150">نظرة عامة حول مكتبة الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="75960-150">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="75960-151">الوحدة النمطية لصندوق الشراء</span><span class="sxs-lookup"><span data-stu-id="75960-151">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="75960-152">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="75960-152">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="75960-153">الوحدة النمطية لمحدد المتجر</span><span class="sxs-lookup"><span data-stu-id="75960-153">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="75960-154">إدارة خرائط Bing لمؤسستك</span><span class="sxs-lookup"><span data-stu-id="75960-154">Manage Bing Maps for your organization</span></span>](./dev-itpro/manage-bing-maps.md)

[<span data-ttu-id="75960-155">عنصر تحكم ويب V8 لخرائط Bing</span><span class="sxs-lookup"><span data-stu-id="75960-155">Bing Maps V8 Web Control</span></span>](https://docs.microsoft.com/bingmaps/v8-web-control/)


[!INCLUDE[footer-include](../includes/footer-banner.md)]