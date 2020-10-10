---
title: التدرجات الهرمية لـ Commerce
description: تشرح هذه المقالة التدرجات الهرمية في Dynamics 365 Commerce.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: OMHierarchyManager, EcoResCategoryHierarchyFactbox
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 8f7e4d01970f459f66934fe434ec7307104b39b2
ms.sourcegitcommit: 97d4a9bd442fe20f90605d8154c3a947c7645b37
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/28/2020
ms.locfileid: "3895271"
---
# <a name="commerce-hierarchies"></a><span data-ttu-id="78452-103">التدرجات الهرمية لـ Commerce</span><span class="sxs-lookup"><span data-stu-id="78452-103">Commerce hierarchies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="78452-104">تشرح هذه المقالة التدرجات الهرمية في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="78452-104">This article describes hierarchies in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="78452-105">يمكنك إنشاء تدرج هرمي للفئات لتنظيم المنتجات التي تبيعها عبر القنوات.</span><span class="sxs-lookup"><span data-stu-id="78452-105">You can create a category hierarchy to organize the products that you sell through your channels.</span></span> <span data-ttu-id="78452-106">ويمكنك استخدام التدرجات الهرمية للمنتجات لتصنيف أو تجميع المنتجات.</span><span class="sxs-lookup"><span data-stu-id="78452-106">You can use product hierarchies to categorize or group products.</span></span> <span data-ttu-id="78452-107">ويمكنك بعد ذلك استخدام هذه المنتجات لإنشاء عمليات فرز المنتجات وبرامج ولاء العملاء.</span><span class="sxs-lookup"><span data-stu-id="78452-107">You can then use these products to create product assortments and customer loyalty programs.</span></span> <span data-ttu-id="78452-108">كما يمكنك تعيين خصائص وسمات المنتجات، وتعيين هيكل تسعير، وتضمين المنتجات في عروض المنتجات، واستخدام المنتجات للإبلاغ.</span><span class="sxs-lookup"><span data-stu-id="78452-108">You can also assign product attributes and properties, assign a pricing structure, include the products in product promotions, and use the products for reporting.</span></span> <span data-ttu-id="78452-109">يمكنك إنشاء تدرج هرمي واحد للفئات لتمثيل كافة المنتجات والفئات في مؤسستك، ثم استخدام ذلك التدرج الهرمي للفئات لأغراض متعددة.</span><span class="sxs-lookup"><span data-stu-id="78452-109">You can create one category hierarchy to represent all the products and categories in your organization, and then use that category hierarchy for multiple purposes.</span></span> <span data-ttu-id="78452-110">وبدلاً من ذلك، يمكنك إنشاء تدرجات هرمية متعددة للفئات لأغراضٍ خاصة، مثل عروض المنتجات.</span><span class="sxs-lookup"><span data-stu-id="78452-110">Alternatively, you can create multiple category hierarchies for special purposes, such as product promotions.</span></span> <span data-ttu-id="78452-111">عند إنشاء تدرج هرمي للمنتجات، يجب تعيين نوع تدرج هرمي للفئات لتحديد غرض التدرج الهرمي للفئات.</span><span class="sxs-lookup"><span data-stu-id="78452-111">When you create a product hierarchy, you must assign a category hierarchy type to identify the purpose of the category hierarchy.</span></span> <span data-ttu-id="78452-112">على سبيل المثال، يتم الرجوع إلى التدرجات الهرمية للمنتجات فقط التي تم تعيين نوع **التدرج الهرمي للتنقل في Commerce** لها، عند استعراض المنتجات حسب الفئة عبر الإنترنت أو في نقطة البيع (POS).</span><span class="sxs-lookup"><span data-stu-id="78452-112">For example, only product hierarchies that are assigned the **Commerce navigation hierarchy** type are referenced when you browse products by category online or in point of sale (POS).</span></span>

## <a name="hierarchy-types"></a><span data-ttu-id="78452-113">أنواع التدرج الهرمي</span><span class="sxs-lookup"><span data-stu-id="78452-113">Hierarchy types</span></span>

<span data-ttu-id="78452-114">يسرد الجدول التالي أنواع التدرجات الهرمية للفئات المتوفرة والغرض العام لكل نوع.</span><span class="sxs-lookup"><span data-stu-id="78452-114">The following table lists the types of category hierarchies that are available and the general purpose of each type.</span></span>

| <span data-ttu-id="78452-115">نوع التدرج الهرمي للفئات</span><span class="sxs-lookup"><span data-stu-id="78452-115">Category hierarchy type</span></span>       | <span data-ttu-id="78452-116">الغرض</span><span class="sxs-lookup"><span data-stu-id="78452-116">Purpose</span></span> |
|-------------------------------|---------|
| <span data-ttu-id="78452-117">التدرج الهرمي للمنتجات</span><span class="sxs-lookup"><span data-stu-id="78452-117">Product hierarchy</span></span>      | <span data-ttu-id="78452-118">استخدم نوع التدرج الهرمي هذا لتحديد التدرج الهرمي الشامل للمنتجات لمؤسستك.</span><span class="sxs-lookup"><span data-stu-id="78452-118">Use this hierarchy type to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="78452-119">ويمكنك استخدام هذا النوع من التدرج الهرمي للترويج للسلع والتسعير والعروض، والتقارير، وتخطيط الفرز.</span><span class="sxs-lookup"><span data-stu-id="78452-119">You can use this hierarchy type for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="78452-120">ويمكن تعيين نوع التدرج الهرمي هذا لتدرج هرمي واحد للمنتجات.</span><span class="sxs-lookup"><span data-stu-id="78452-120">Only one product hierarchy can be assigned this hierarchy type.</span></span> |
| <span data-ttu-id="78452-121">التدرج الهرمي التكميلي</span><span class="sxs-lookup"><span data-stu-id="78452-121">Supplemental hierarchy</span></span> | <span data-ttu-id="78452-122">استخدم نوع التدرج الهرمي هذا لأي تدرجات هرمية للفئات الإضافية التي تريد إنشائها.</span><span class="sxs-lookup"><span data-stu-id="78452-122">Use this hierarchy type for any additional category hierarchies that you want to create.</span></span> <span data-ttu-id="78452-123">على سبيل المثال، في فصل الربيع، يكون لديك ترويج لملابس السباحة.</span><span class="sxs-lookup"><span data-stu-id="78452-123">For example, in the spring, you have a promotion for swimwear.</span></span> <span data-ttu-id="78452-124">ولذلك، تقوم بتضمين المنتجات ملابس السباحة في تدرج هرمي منفصل للفئات وتطبيق الأسعار الترويجية على مختلف فئات المنتجات.</span><span class="sxs-lookup"><span data-stu-id="78452-124">Therefore, you include your swimwear products in a separate category hierarchy and apply the promotional pricing to the various product categories.</span></span> |
| <span data-ttu-id="78452-125">التدرج الهرمي للتنقل‬</span><span class="sxs-lookup"><span data-stu-id="78452-125">Navigation hierarchy</span></span>   | <span data-ttu-id="78452-126">استخدم هذا النوع من التدرج الهرمي لتجميع وتنظيم المنتجات في فئات بحيث يمكنك استعراض المنتجات على الإنترنت أو في نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="78452-126">Use this hierarchy type to group and organize products into categories so that the products can be browsed online or in POS.</span></span> |

<span data-ttu-id="78452-127">باستخدام تدرج هرمي للفئات لتنظيم منتجاتك، يمكن إعداد وصيانة سمات وخصائص المنتجات على مستوى الفئة.</span><span class="sxs-lookup"><span data-stu-id="78452-127">By using a category hierarchy to structure your products, you can set up and maintain product attributes and properties at the category level.</span></span> <span data-ttu-id="78452-128">وتتضمن هذه السمات والخصائص إعدادات أبعاد المنتج وإعدادات نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="78452-128">These attributes and properties include settings for product dimensions and POS settings.</span></span> <span data-ttu-id="78452-129">وترث منتجات تقوم بتعيينها إلى الفئات تلقائياً السمات والخصائص التي تحددها.</span><span class="sxs-lookup"><span data-stu-id="78452-129">Any products that you assign to the categories automatically inherit the attributes and properties that you define.</span></span> <span data-ttu-id="78452-130">كما يمكنك نسخ إعدادات الخصائص لأي منتج لعدة منتجات في فئة محددة في نفس الوقت.</span><span class="sxs-lookup"><span data-stu-id="78452-130">You can also copy the property settings for any product to multiple products in a selected category at the same time.</span></span>
