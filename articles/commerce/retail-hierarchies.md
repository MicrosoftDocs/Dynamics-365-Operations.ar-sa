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
ms.search.form: OMHierarchyManager
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
ms.openlocfilehash: e1b9fc647ccaa3caeec0d0e3a8594fd6a2a8be0f
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070726"
---
# <a name="commerce-hierarchies"></a><span data-ttu-id="75004-103">التدرجات الهرمية لـ Commerce</span><span class="sxs-lookup"><span data-stu-id="75004-103">Commerce hierarchies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="75004-104">تشرح هذه المقالة التدرجات الهرمية في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="75004-104">This article describes hierarchies in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="75004-105">يمكنك إنشاء تدرج هرمي للفئات لتنظيم المنتجات التي تبيعها عبر القنوات.</span><span class="sxs-lookup"><span data-stu-id="75004-105">You can create a category hierarchy to organize the products that you sell through your channels.</span></span> <span data-ttu-id="75004-106">ويمكنك استخدام التدرجات الهرمية للمنتجات لتصنيف أو تجميع المنتجات.</span><span class="sxs-lookup"><span data-stu-id="75004-106">You can use product hierarchies to categorize or group products.</span></span> <span data-ttu-id="75004-107">ويمكنك بعد ذلك استخدام هذه المنتجات لإنشاء عمليات فرز المنتجات وبرامج ولاء العملاء.</span><span class="sxs-lookup"><span data-stu-id="75004-107">You can then use these products to create product assortments and customer loyalty programs.</span></span> <span data-ttu-id="75004-108">كما يمكنك تعيين خصائص وسمات المنتجات، وتعيين هيكل تسعير، وتضمين المنتجات في عروض المنتجات، واستخدام المنتجات للإبلاغ.</span><span class="sxs-lookup"><span data-stu-id="75004-108">You can also assign product attributes and properties, assign a pricing structure, include the products in product promotions, and use the products for reporting.</span></span> <span data-ttu-id="75004-109">يمكنك إنشاء تدرج هرمي واحد للفئات لتمثيل كافة المنتجات والفئات في مؤسستك، ثم استخدام ذلك التدرج الهرمي للفئات لأغراض متعددة.</span><span class="sxs-lookup"><span data-stu-id="75004-109">You can create one category hierarchy to represent all the products and categories in your organization, and then use that category hierarchy for multiple purposes.</span></span> <span data-ttu-id="75004-110">وبدلاً من ذلك، يمكنك إنشاء تدرجات هرمية متعددة للفئات لأغراضٍ خاصة، مثل عروض المنتجات.</span><span class="sxs-lookup"><span data-stu-id="75004-110">Alternatively, you can create multiple category hierarchies for special purposes, such as product promotions.</span></span> <span data-ttu-id="75004-111">عند إنشاء تدرج هرمي للمنتجات، يجب تعيين نوع تدرج هرمي للفئات لتحديد غرض التدرج الهرمي للفئات.</span><span class="sxs-lookup"><span data-stu-id="75004-111">When you create a product hierarchy, you must assign a category hierarchy type to identify the purpose of the category hierarchy.</span></span> <span data-ttu-id="75004-112">على سبيل المثال، يتم الرجوع إلى التدرجات الهرمية للمنتجات فقط التي تم تعيين نوع **التدرج الهرمي للتنقل في Commerce** لها، عند استعراض المنتجات حسب الفئة عبر الإنترنت أو في نقطة البيع (POS).</span><span class="sxs-lookup"><span data-stu-id="75004-112">For example, only product hierarchies that are assigned the **Commerce navigation hierarchy** type are referenced when you browse products by category online or in point of sale (POS).</span></span>

## <a name="hierarchy-types"></a><span data-ttu-id="75004-113">أنواع التدرج الهرمي</span><span class="sxs-lookup"><span data-stu-id="75004-113">Hierarchy types</span></span>

<span data-ttu-id="75004-114">يسرد الجدول التالي أنواع التدرجات الهرمية للفئات المتوفرة والغرض العام لكل نوع.</span><span class="sxs-lookup"><span data-stu-id="75004-114">The following table lists the types of category hierarchies that are available and the general purpose of each type.</span></span>

| <span data-ttu-id="75004-115">نوع التدرج الهرمي للفئات</span><span class="sxs-lookup"><span data-stu-id="75004-115">Category hierarchy type</span></span>       | <span data-ttu-id="75004-116">الغرض</span><span class="sxs-lookup"><span data-stu-id="75004-116">Purpose</span></span> |
|-------------------------------|---------|
| <span data-ttu-id="75004-117">التدرج الهرمي للمنتجات</span><span class="sxs-lookup"><span data-stu-id="75004-117">Product hierarchy</span></span>      | <span data-ttu-id="75004-118">استخدم نوع التدرج الهرمي هذا لتحديد التدرج الهرمي الشامل للمنتجات لمؤسستك.</span><span class="sxs-lookup"><span data-stu-id="75004-118">Use this hierarchy type to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="75004-119">ويمكنك استخدام هذا النوع من التدرج الهرمي للترويج للسلع والتسعير والعروض، والتقارير، وتخطيط الفرز.</span><span class="sxs-lookup"><span data-stu-id="75004-119">You can use this hierarchy type for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="75004-120">ويمكن تعيين نوع التدرج الهرمي هذا لتدرج هرمي واحد للمنتجات.</span><span class="sxs-lookup"><span data-stu-id="75004-120">Only one product hierarchy can be assigned this hierarchy type.</span></span> |
| <span data-ttu-id="75004-121">التدرج الهرمي التكميلي</span><span class="sxs-lookup"><span data-stu-id="75004-121">Supplemental hierarchy</span></span> | <span data-ttu-id="75004-122">استخدم نوع التدرج الهرمي هذا لأي تدرجات هرمية للفئات الإضافية التي تريد إنشائها.</span><span class="sxs-lookup"><span data-stu-id="75004-122">Use this hierarchy type for any additional category hierarchies that you want to create.</span></span> <span data-ttu-id="75004-123">على سبيل المثال، في فصل الربيع، يكون لديك ترويج لملابس السباحة.</span><span class="sxs-lookup"><span data-stu-id="75004-123">For example, in the spring, you have a promotion for swimwear.</span></span> <span data-ttu-id="75004-124">ولذلك، تقوم بتضمين المنتجات ملابس السباحة في تدرج هرمي منفصل للفئات وتطبيق الأسعار الترويجية على مختلف فئات المنتجات.</span><span class="sxs-lookup"><span data-stu-id="75004-124">Therefore, you include your swimwear products in a separate category hierarchy and apply the promotional pricing to the various product categories.</span></span> |
| <span data-ttu-id="75004-125">التدرج الهرمي للتنقل‬</span><span class="sxs-lookup"><span data-stu-id="75004-125">Navigation hierarchy</span></span>   | <span data-ttu-id="75004-126">استخدم هذا النوع من التدرج الهرمي لتجميع وتنظيم المنتجات في فئات بحيث يمكنك استعراض المنتجات على الإنترنت أو في نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="75004-126">Use this hierarchy type to group and organize products into categories so that the products can be browsed online or in POS.</span></span> |

<span data-ttu-id="75004-127">باستخدام تدرج هرمي للفئات لتنظيم منتجاتك، يمكن إعداد وصيانة سمات وخصائص المنتجات على مستوى الفئة.</span><span class="sxs-lookup"><span data-stu-id="75004-127">By using a category hierarchy to structure your products, you can set up and maintain product attributes and properties at the category level.</span></span> <span data-ttu-id="75004-128">وتتضمن هذه السمات والخصائص إعدادات أبعاد المنتج وإعدادات نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="75004-128">These attributes and properties include settings for product dimensions and POS settings.</span></span> <span data-ttu-id="75004-129">وترث منتجات تقوم بتعيينها إلى الفئات تلقائياً السمات والخصائص التي تحددها.</span><span class="sxs-lookup"><span data-stu-id="75004-129">Any products that you assign to the categories automatically inherit the attributes and properties that you define.</span></span> <span data-ttu-id="75004-130">كما يمكنك نسخ إعدادات الخصائص لأي منتج لعدة منتجات في فئة محددة في نفس الوقت.</span><span class="sxs-lookup"><span data-stu-id="75004-130">You can also copy the property settings for any product to multiple products in a selected category at the same time.</span></span>
