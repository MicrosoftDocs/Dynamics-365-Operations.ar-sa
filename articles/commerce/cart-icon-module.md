---
title: وحدة أيقونة عربة التسوق
description: يتناول هذا الموضوع وحدة أيقونة عربة التسوق ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8cc96e0476a9d8a46aed7011359dc65fbc678fbf
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261550"
---
# <a name="cart-icon-module"></a><span data-ttu-id="cfefd-103">وحدة أيقونة عربة التسوق</span><span class="sxs-lookup"><span data-stu-id="cfefd-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cfefd-104">يتناول هذا الموضوع وحدة أيقونة عربة التسوق ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="cfefd-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="cfefd-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="cfefd-105">Overview</span></span>

<span data-ttu-id="cfefd-106">تمثل وحدة أيقونة عربة التسوق في وحدة الرأس على الصفحة، وتُظهر عدد الأصناف في سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="cfefd-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="cfefd-107">تعرض أيضًا وحدة أيقونة سلة التسوق ملخص السلة (تعرف أيضًا بسلة تسوق صغيرة) عند تمرير الماوس فوق أيقونة السلة.</span><span class="sxs-lookup"><span data-stu-id="cfefd-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="cfefd-108">توفر سلة التسوق الصغيرة للمستخدم ملخص الأصناف الموجودة في سلة التسوق دون الحاجة إلى الانتقال إلى صفحة سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="cfefd-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="cfefd-109">بالإضافة إلى ذلك، تسمح أيضًا للمستخدم بالانتقال مباشرةً إلى صفحة السداد مع الخروج إذا أعجبه الملخص.</span><span class="sxs-lookup"><span data-stu-id="cfefd-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="cfefd-110">يؤدي ذلك إلى تقليل عدد عمليات التنقل في الصفحات ويسهل عملية السداد والخروج.</span><span class="sxs-lookup"><span data-stu-id="cfefd-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="cfefd-111">خصائص الوحدة النمطية</span><span class="sxs-lookup"><span data-stu-id="cfefd-111">Module properties</span></span>

- <span data-ttu-id="cfefd-112">**إظهار سلة التسوق الصغيرة** – تمكّن هذه الخاصية، عندما تكون قيمتها صواب، عرض ملخص سلة التسوق (سلة التسوق الصغيرة) عند تمرير الماوس فوق أيقونة سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="cfefd-112">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="cfefd-113">هذه الوظيفة مدعومة فقط لمنافذ عرض سطح المكتب.</span><span class="sxs-lookup"><span data-stu-id="cfefd-113">This functionality is only supported for desktop view ports.</span></span>


## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="cfefd-114">إضافة وحدة سلة التسوق إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="cfefd-114">Add a cart icon module to a page</span></span>

<span data-ttu-id="cfefd-115">لإضافة وحدة ايقونة سلة التسوق، راجع [وحدة الرأس](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="cfefd-115">To add a cart icon module, see [Header module](author-header-module.md).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="cfefd-116">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="cfefd-116">Additional resources</span></span>

[<span data-ttu-id="cfefd-117">الوحدة النمطية لصندوق الشراء</span><span class="sxs-lookup"><span data-stu-id="cfefd-117">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="cfefd-118">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="cfefd-118">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="cfefd-119">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="cfefd-119">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="cfefd-120">الوحدة النمطية لتأكيد الأمر</span><span class="sxs-lookup"><span data-stu-id="cfefd-120">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="cfefd-121">وحدة الرأس</span><span class="sxs-lookup"><span data-stu-id="cfefd-121">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="cfefd-122">وحدة التذييل</span><span class="sxs-lookup"><span data-stu-id="cfefd-122">Footer module</span></span>](author-footer-module.md)
