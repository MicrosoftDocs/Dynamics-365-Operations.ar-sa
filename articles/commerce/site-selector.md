---
title: الوحدة النمطية لمحدد الموقع
description: يتناول هذا الموضوع وحدة محدّد الموقع ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/20/2020
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
ms.openlocfilehash: 6e8eefe7afe385ca77eca6027638ff938e1356e3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791765"
---
# <a name="site-selector-module"></a><span data-ttu-id="fea02-103">الوحدة النمطية لمحدد الموقع</span><span class="sxs-lookup"><span data-stu-id="fea02-103">Site selector module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fea02-104">يتناول هذا الموضوع وحدة محدّد الموقع ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fea02-104">This topic covers the site selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="fea02-105">عندما يكون للشركة مواقع مختلفه عبر الأسواق والمناطق والإعدادات المحلية، فان مستخدمي الموقع يحتاجون إلى طريقة سهلة للتبديل بين المواقع وتحديد موقع التسوق المفضل لديهم.</span><span class="sxs-lookup"><span data-stu-id="fea02-105">When a business has different sites across markets, regions, and locales, site users need an easy way to switch between sites and select their preferred shopping site.</span></span> <span data-ttu-id="fea02-106">لاحتواء هذا السيناريو ، تسمح الوحدة النمطية لمحدد الموقع للمستخدمين بالاستعراض عبر مواقع متعددة.</span><span class="sxs-lookup"><span data-stu-id="fea02-106">To accommodate this scenario, the site selector module lets users browse across multiple sites.</span></span>

<span data-ttu-id="fea02-107">يجب تكوين الوحدة النمطية لمحدد الموقع بقائمة المواقع (الأسواق أو المناطق أو الإعدادات المحلية) التي يمكن لمستخدمي الموقع استعراضها.</span><span class="sxs-lookup"><span data-stu-id="fea02-107">The site selector module must be configured with the list of sites (markets, regions, or locales) that site users can browse.</span></span>

> [!NOTE]
> <span data-ttu-id="fea02-108">تتوفر الوحدة النمطية لمحدد الموقع في Dynamics 365 Commerce الإصدار 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="fea02-108">The site selector module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="fea02-109">يبين الرسم التوضيحي التالي مثالاً للوحدة النمطية لمحدد الموقع والتي تكون مميزه في رأس صفحة الموقع.</span><span class="sxs-lookup"><span data-stu-id="fea02-109">The following illustration shows an example of a site selector module that is featured in the header of a site page.</span></span>

![مثال لوحدة نمطية لمحدد موقع في رأس صفحة موقع](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a><span data-ttu-id="fea02-111">خصائص وحدة محدِّد الموقع</span><span class="sxs-lookup"><span data-stu-id="fea02-111">Site selector module properties</span></span>

| <span data-ttu-id="fea02-112">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="fea02-112">Property name</span></span> | <span data-ttu-id="fea02-113">قيمة</span><span class="sxs-lookup"><span data-stu-id="fea02-113">Value</span></span>                 | <span data-ttu-id="fea02-114">الوصف</span><span class="sxs-lookup"><span data-stu-id="fea02-114">Description</span></span> |
|---------------|-----------------------|-------------|
| <span data-ttu-id="fea02-115">العنوان</span><span class="sxs-lookup"><span data-stu-id="fea02-115">Heading</span></span>       | <span data-ttu-id="fea02-116">النص</span><span class="sxs-lookup"><span data-stu-id="fea02-116">Text</span></span>                  | <span data-ttu-id="fea02-117">عنوان الوحدة النمطية.</span><span class="sxs-lookup"><span data-stu-id="fea02-117">The heading for the module.</span></span> |
| <span data-ttu-id="fea02-118">خيارات المواقع</span><span class="sxs-lookup"><span data-stu-id="fea02-118">Site options</span></span>  | <span data-ttu-id="fea02-119">الاسم، الصورة ، عنوان URL</span><span class="sxs-lookup"><span data-stu-id="fea02-119">Name, Image, URL</span></span>      | <span data-ttu-id="fea02-120">تحدد هذه الخاصية اسمًا وارتباطا بالصفحة الرئيسية للموقع وصورة اختياريه لعرضها لكل موقع يتم تضمينه في الوحدة النمطية.</span><span class="sxs-lookup"><span data-stu-id="fea02-120">This property specifies a name, a link to the site's home page, and an optional image to show for each site that is included in the module.</span></span> <span data-ttu-id="fea02-121">ويمكن أن تكون الصورة علامة أو تمثيلا لأحد الأسواق أو المنطقة أو الإعدادات المحلية.</span><span class="sxs-lookup"><span data-stu-id="fea02-121">The image can be a flag, or some representation of a market, region, or locale.</span></span> |

## <a name="add-a-site-selector-module-to-a-page"></a><span data-ttu-id="fea02-122">إضافة وحدة محدِّد موقع إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="fea02-122">Add a site selector module to a page</span></span>

<span data-ttu-id="fea02-123">يمكن إضافة الوحدة النمطية لمحدد الموقع إلى [الوحدة النمطية للرؤوس](author-header-module.md) ضمن فتحة "محدد الموقع".</span><span class="sxs-lookup"><span data-stu-id="fea02-123">The site selector module can be added to the [Header module](author-header-module.md) under the site selector slot.</span></span> <span data-ttu-id="fea02-124">بعد إضافتها، يمكنك تحديد عنوان الوحدة النمطية وخيارات الموقع.</span><span class="sxs-lookup"><span data-stu-id="fea02-124">After it's added, you can define the module heading and site options.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fea02-125">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="fea02-125">Additional resources</span></span>

[<span data-ttu-id="fea02-126">نظرة عامة على مكتبة الوحدات</span><span class="sxs-lookup"><span data-stu-id="fea02-126">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="fea02-127">الوحدة النمطية للرؤوس</span><span class="sxs-lookup"><span data-stu-id="fea02-127">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="fea02-128">الوحدة النمطية لمسار التنقل</span><span class="sxs-lookup"><span data-stu-id="fea02-128">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="fea02-129">الوحدة النمطية لقائمة التنقل</span><span class="sxs-lookup"><span data-stu-id="fea02-129">Navigation menu module</span></span>](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]