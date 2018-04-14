---
title: "بيع وإرجاع المنتجات خارج عملية فرز"
description: "باستخدام Dynamics 365 for Retail، يمكنك بيع المنتجات وإرجاعها خارج عمليات الفرز."
author: pdp1207
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.search.region: Global
ms.search.industry: retail
ms.author: prabhup
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 8d2188ddac937ab373315759b89ecf85c0b7e007
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---

# <a name="sell-and-return-products-outside-of-an-assortment"></a><span data-ttu-id="4c47f-103">بيع وإرجاع المنتجات خارج عملية فرز</span><span class="sxs-lookup"><span data-stu-id="4c47f-103">Sell and return products outside of an assortment</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="4c47f-104">هناك سيناريو شائع لأي بائع التجزئة وهو بيع المنتجات إلى العملاء أو قبول المرتجعات من العملاء حتى لو لم تكن بعض المنتجات المحددة موجودة في المتجر (بمعنى آخر، لا يتم فرز المنتجات في المتجر).</span><span class="sxs-lookup"><span data-stu-id="4c47f-104">A common scenario for any retailer is to sell products to their customers or accept returns from their customers even if they don’t carry the specific products in their store (in other words, the products are not assorted to the store).</span></span>
<span data-ttu-id="4c47f-105">وفيما يلي بعض السيناريوهات النموذجية:</span><span class="sxs-lookup"><span data-stu-id="4c47f-105">Here are some typical scenarios:</span></span>

+ <span data-ttu-id="4c47f-106">كافة المنتجات لدى بائع التجزئة غير متوفرة في متجر معين.</span><span class="sxs-lookup"><span data-stu-id="4c47f-106">A retailer doesn’t carry all its products in a specific store.</span></span> <span data-ttu-id="4c47f-107">يتم تخزين المنتجات المتبقية في المستودع.</span><span class="sxs-lookup"><span data-stu-id="4c47f-107">The remaining products are stored in the warehouse.</span></span> <span data-ttu-id="4c47f-108">باستطاعة موظف المتجر مساعدة العميل عن طريق البحث عن منتجات معينة في المتجر أو استعراضها، وإضافتها إلى عربة التسوق، وإكمال عملية السداد والخروج عن طريق تحديد أسلوب تسليم، مثل الشحن إلى عنوان ما من المستودع أو السماح للعميل باستلام المنتج من المتجر الحالي أو متجر آخر.</span><span class="sxs-lookup"><span data-stu-id="4c47f-108">The store associate can assist the customer by searching or browsing for the products in the warehouse, add them to the cart, and complete the checkout by selecting a delivery method, such as shipping to an address from the warehouse or letting the customer pick up the product from the current store or from another store.</span></span>
+ <span data-ttu-id="4c47f-109">لا توجد لدى بائع التجزئة منتجات محددة في المتجر أو هي غير متوفرة في المخزون في المتجر الذي زاره العميل، ولكن هذه المنتجات متوفرة في متاجر أخرى.</span><span class="sxs-lookup"><span data-stu-id="4c47f-109">A retailer doesn’t carry specific products in the store or doesn’t have them in stock at the store the customer visited, but the products are available in other stores.</span></span> <span data-ttu-id="4c47f-110">باستطاعة موظف المتجر مساعدة العميل عن طريق البحث عن منتجات معينة في المتجر أو استعراضها، وإضافتها إلى عربة التسوق، وإكمال عملية السداد والخروج عن طريق تحديد أسلوب تسليم.</span><span class="sxs-lookup"><span data-stu-id="4c47f-110">The store associate can assist the customer by searching or browsing the products in the other store, add them to the cart, and complete the checkout by selecting a delivery method.</span></span>
+ <span data-ttu-id="4c47f-111">لدى بائع التجزئة الكثير من المتاجر في منطقة محددة أو رمز بريدي محدد أو حولهما، وهو لا يريد إجبار العملاء على إعادة المنتجات إلى المتجر نفسه حيث تمت عملية الشراء.</span><span class="sxs-lookup"><span data-stu-id="4c47f-111">A retailer has many stores in and around a specific city or zip code and doesn’t want to force the customers to return products to the same store they were purchased in.</span></span> <span data-ttu-id="4c47f-112">بدلاً من ذلك، باستطاعة العملاء إرجاع المنتجات إلى أي متجر.</span><span class="sxs-lookup"><span data-stu-id="4c47f-112">Instead, customers can return products to any store.</span></span>


<span data-ttu-id="4c47f-113">تتوفر هذه السيناريوهات الشائعة لبائعي التجزئة الذين يستخدمون Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="4c47f-113">Those common scenarios are available for retailers using Dynamics 365 for Retail.</span></span> <span data-ttu-id="4c47f-114">باستخدام Retail، يمكنك:</span><span class="sxs-lookup"><span data-stu-id="4c47f-114">With Retail, you can:</span></span>
+ <span data-ttu-id="4c47f-115">البحث عن منتجات في متاجر أخرى أو استعراضها.</span><span class="sxs-lookup"><span data-stu-id="4c47f-115">Search or browse products at other stores.</span></span>
+ <span data-ttu-id="4c47f-116">البحث عن جميع المنتجات الصادرة أو استعراضها.</span><span class="sxs-lookup"><span data-stu-id="4c47f-116">Search or browse all released products.</span></span>
+ <span data-ttu-id="4c47f-117">إنشاء حركات تعتمد على الدفع نقدًا والنقل أو أوامر العملاء.</span><span class="sxs-lookup"><span data-stu-id="4c47f-117">Create cash-and-carry transactions or customer orders.</span></span>
+ <span data-ttu-id="4c47f-118">تحديد خيارات التسليم الخاصة بأوامر العملاء.</span><span class="sxs-lookup"><span data-stu-id="4c47f-118">Select delivery options for customer orders.</span></span>
+ <span data-ttu-id="4c47f-119">استلام المنتجات في المتجر الحالي أو متجر آخر.</span><span class="sxs-lookup"><span data-stu-id="4c47f-119">Pick up products at the current store or another store.</span></span>
+ <span data-ttu-id="4c47f-120">إلغاء أمر في المتجر الحالي أو متجر آخر.</span><span class="sxs-lookup"><span data-stu-id="4c47f-120">Cancel an order at the current store or another store.</span></span>
+ <span data-ttu-id="4c47f-121">إرجاع أمر مع أو بدون إيصال الاستلام في المتجر الحالي أو متجر آخر.</span><span class="sxs-lookup"><span data-stu-id="4c47f-121">Return an order with or without the receipt at the current store or another store.</span></span>

