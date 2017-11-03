---
title: "التسلسلات الهرمية للبيع بالتجزئة"
description: "توضح هذه المقالة التدرجات الهرمية للبيع بالتجزئة في Microsoft Dynamics 365 for Retail."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e94b59540c9ef188a07e2e24ef4a04829b9d37f8
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="retail-hierarchies"></a><span data-ttu-id="3473b-103">التسلسلات الهرمية للبيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="3473b-103">Retail hierarchies</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="3473b-104">توضح هذه المقالة التدرجات الهرمية للبيع بالتجزئة في Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="3473b-104">This article describes retail hierarchies in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="3473b-105">يمكنك إنشاء تدرج هرمي لفئات البيع بالتجزئة لتنظيم المنتجات التي تبيعها عبر قنوات البيع بالتجزئة لديك.</span><span class="sxs-lookup"><span data-stu-id="3473b-105">You can create a retail category hierarchy to organize the products that you sell through your retail channels.</span></span> <span data-ttu-id="3473b-106">ويمكنك استخدام التدرجات الهرمية لمنتجات البيع بالتجزئة لتصنيف أو تجميع المنتجات.</span><span class="sxs-lookup"><span data-stu-id="3473b-106">You can use retail product hierarchies to categorize or group products.</span></span> <span data-ttu-id="3473b-107">ويمكنك بعد ذلك استخدام هذه المنتجات لإنشاء عمليات فرز المنتجات وبرامج ولاء العملاء.</span><span class="sxs-lookup"><span data-stu-id="3473b-107">You can then use these products to create product assortments and customer loyalty programs.</span></span> <span data-ttu-id="3473b-108">كما يمكنك تعيين خصائص وسمات المنتجات، وتعيين هيكل تسعير، وتضمين المنتجات في عروض المنتجات، واستخدام المنتجات للإبلاغ.</span><span class="sxs-lookup"><span data-stu-id="3473b-108">You can also assign product attributes and properties, assign a pricing structure, include the products in product promotions, and use the products for reporting.</span></span> <span data-ttu-id="3473b-109">يمكنك إنشاء تدرج هرمي واحد لفئات البيع بالتجزئة لتمثيل كافة المنتجات والفئات في مؤسستك، ثم استخدام ذلك التدرج الهرمي للفئات لأغراض متعددة.</span><span class="sxs-lookup"><span data-stu-id="3473b-109">You can create one retail category hierarchy to represent all the products and categories in your organization, and then use that category hierarchy for multiple purposes.</span></span> <span data-ttu-id="3473b-110">وبدلاً من ذلك، يمكنك إنشاء تدرجات هرمية متعددة لفئات البيع بالتجزئة لأغراضٍ خاصة، مثل عروض المنتجات.</span><span class="sxs-lookup"><span data-stu-id="3473b-110">Alternatively, you can create multiple retail category hierarchies for special purposes, such as product promotions.</span></span> <span data-ttu-id="3473b-111">عند إنشاء تدرج هرمي لمنتجات بيع بالتجزئة، يجب تعيين نوع تدرج هرمي للفئات لتحديد غرض التدرج الهرمي للفئات.</span><span class="sxs-lookup"><span data-stu-id="3473b-111">When you create a retail product hierarchy, you must assign a category hierarchy type to identify the purpose of the category hierarchy.</span></span> <span data-ttu-id="3473b-112">على سبيل المثال، يتم الرجوع إلى التدرجات الهرمية للمنتجات فقط التي تم تعيين نوع **التدرج الهرمي للتنقل للبيع بالتجزئة** لها، عند استعراض المنتجات حسب الفئة عبر الإنترنت أو في نقطة البيع (POS).</span><span class="sxs-lookup"><span data-stu-id="3473b-112">For example, only product hierarchies that are assigned the **Retail navigation hierarchy** type are referenced when you browse products by category online or in point of sale (POS).</span></span>

## <a name="retail-hierarchy-types"></a><span data-ttu-id="3473b-113">أنواع التدرج الهرمي للبيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="3473b-113">Retail hierarchy types</span></span>
<span data-ttu-id="3473b-114">يسرد الجدول التالي أنواع التدرجات الهرمية لفئات اليع بالتجزئة المتوفرة والغرض العام لكل نوع.</span><span class="sxs-lookup"><span data-stu-id="3473b-114">The following table lists the types of retail category hierarchies that are available and the general purpose of each type.</span></span>

| <span data-ttu-id="3473b-115">نوع التدرج الهرمي للفئات</span><span class="sxs-lookup"><span data-stu-id="3473b-115">Category hierarchy type</span></span>       | <span data-ttu-id="3473b-116">الغرض</span><span class="sxs-lookup"><span data-stu-id="3473b-116">Purpose</span></span>                                                                                                                                                                                                                                                                                                            |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3473b-117">التسلسل الهرمي لمنتج البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="3473b-117">Retail product hierarchy</span></span>      | <span data-ttu-id="3473b-118">استخدم نوع التدرج الهرمي هذا لتحديد التدرج الهرمي الشامل للمنتجات لمؤسستك.</span><span class="sxs-lookup"><span data-stu-id="3473b-118">Use this hierarchy type to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="3473b-119">ويمكنك استخدام هذا النوع من التدرج الهرمي للترويج للسلع والتسعير والعروض، والتقارير، وتخطيط الفرز.</span><span class="sxs-lookup"><span data-stu-id="3473b-119">You can use this hierarchy type for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="3473b-120">ويمكن تعيين نوع التدرج الهرمي هذا لتدرج هرمي واحد لمنتجات البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="3473b-120">Only one retail product hierarchy can be assigned this hierarchy type.</span></span>                                       |
| <span data-ttu-id="3473b-121">التدرج الهرمي التكميلي للبيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="3473b-121">Supplemental retail hierarchy</span></span> | <span data-ttu-id="3473b-122">استخدم نوع التدرج الهرمي هذا لأي تدرجات هرمية للفئات الإضافية للبيع بالتجزئة التي تريد إنشائها.</span><span class="sxs-lookup"><span data-stu-id="3473b-122">Use this hierarchy type for any additional retail category hierarchies that you want to create.</span></span> <span data-ttu-id="3473b-123">على سبيل المثال، في فصل الربيع، يكون لديك ترويج لملابس السباحة.</span><span class="sxs-lookup"><span data-stu-id="3473b-123">For example, in the spring, you have a promotion for swimwear.</span></span> <span data-ttu-id="3473b-124">ولذلك، تقوم بتضمين المنتجات ملابس السباحة في تدرج هرمي منفصل للفئات وتطبيق الأسعار الترويجية على مختلف فئات المنتجات.</span><span class="sxs-lookup"><span data-stu-id="3473b-124">Therefore, you include your swimwear products in a separate category hierarchy and apply the promotional pricing to the various product categories.</span></span> |
| <span data-ttu-id="3473b-125">التدرج الهرمي للتنقل في البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="3473b-125">Retail navigation hierarchy</span></span>   | <span data-ttu-id="3473b-126">استخدم هذا النوع من التدرج الهرمي لتجميع وتنظيم المنتجات في فئات بحيث يمكنك استعراض المنتجات على الإنترنت أو في نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="3473b-126">Use this hierarchy type to group and organize products into categories so that the products can be browsed online or in POS.</span></span>                                                                                                                                                                                       |

<span data-ttu-id="3473b-127">باستخدام تدرج هرمي لفئات البيع بالتجزئة لتنظيم منتجاتك، يمكن إعداد وصيانة سمات وخصائص المنتجات على مستوى الفئة.</span><span class="sxs-lookup"><span data-stu-id="3473b-127">By using a retail category hierarchy to structure your products, you can set up and maintain product attributes and properties at the category level.</span></span> <span data-ttu-id="3473b-128">وتتضمن هذه السمات والخصائص إعدادات أبعاد المنتج وإعدادات نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="3473b-128">These attributes and properties include settings for product dimensions and POS settings.</span></span> <span data-ttu-id="3473b-129">وترث منتجات تقوم بتعيينها إلى الفئات تلقائياً السمات والخصائص التي تحددها.</span><span class="sxs-lookup"><span data-stu-id="3473b-129">Any products that you assign to the categories automatically inherit the attributes and properties that you define.</span></span> <span data-ttu-id="3473b-130">كما يمكنك نسخ إعدادات الخصائص لأي منتج لعدة منتجات في فئة محددة في نفس الوقت.</span><span class="sxs-lookup"><span data-stu-id="3473b-130">You can also copy the property settings for any product to multiple products in a selected category at the same time.</span></span>




