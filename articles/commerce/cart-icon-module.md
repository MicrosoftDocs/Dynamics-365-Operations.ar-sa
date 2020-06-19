---
title: وحدة أيقونة عربة التسوق
description: يتناول هذا الموضوع وحدة أيقونة عربة التسوق ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: 6771a84118504cd5c8e44302380eb970e4658902
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411079"
---
# <a name="cart-icon-module"></a><span data-ttu-id="05017-103">وحدة أيقونة عربة التسوق</span><span class="sxs-lookup"><span data-stu-id="05017-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="05017-104">يتناول هذا الموضوع وحدة أيقونة عربة التسوق ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="05017-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="05017-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="05017-105">Overview</span></span>

<span data-ttu-id="05017-106">تمثل وحدة أيقونة عربة التسوق في وحدة الرأس على الصفحة، وتُظهر عدد الأصناف في سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="05017-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="05017-107">تعرض أيضًا وحدة أيقونة سلة التسوق ملخص السلة (تعرف أيضًا بسلة تسوق صغيرة) عند تمرير الماوس فوق أيقونة السلة.</span><span class="sxs-lookup"><span data-stu-id="05017-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="05017-108">توفر سلة التسوق الصغيرة للمستخدم ملخص الأصناف الموجودة في سلة التسوق دون الحاجة إلى الانتقال إلى صفحة سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="05017-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="05017-109">بالإضافة إلى ذلك، تسمح أيضًا للمستخدم بالانتقال مباشرةً إلى صفحة السداد مع الخروج إذا أعجبه الملخص.</span><span class="sxs-lookup"><span data-stu-id="05017-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="05017-110">يؤدي ذلك إلى تقليل عدد عمليات التنقل في الصفحات ويسهل عملية السداد والخروج.</span><span class="sxs-lookup"><span data-stu-id="05017-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

<span data-ttu-id="05017-111">تظهر الصورة التالية مثالاً عن وحدة أيقونة سلة تسوق تعرض سلة تسوق صغيرة في رأس Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="05017-111">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![مثال عن وحدة أيقونة سلة التسوق](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="05017-113">خصائص الوحدة النمطية</span><span class="sxs-lookup"><span data-stu-id="05017-113">Module properties</span></span>

- <span data-ttu-id="05017-114">**إظهار سلة التسوق الصغيرة** – تمكّن هذه الخاصية، عندما تكون قيمتها صواب، عرض ملخص سلة التسوق (سلة التسوق الصغيرة) عند تمرير الماوس فوق أيقونة سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="05017-114">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="05017-115">هذه الوظيفة مدعومة فقط لمنافذ عرض سطح المكتب.</span><span class="sxs-lookup"><span data-stu-id="05017-115">This functionality is only supported for desktop view ports.</span></span>


## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="05017-116">إضافة وحدة سلة التسوق إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="05017-116">Add a cart icon module to a page</span></span>

<span data-ttu-id="05017-117">لإضافة وحدة ايقونة سلة التسوق، راجع [وحدة الرأس](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="05017-117">To add a cart icon module, see [Header module](author-header-module.md).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="05017-118">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="05017-118">Additional resources</span></span>

[<span data-ttu-id="05017-119">الوحدة النمطية لصندوق الشراء</span><span class="sxs-lookup"><span data-stu-id="05017-119">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="05017-120">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="05017-120">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="05017-121">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="05017-121">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="05017-122">الوحدة النمطية لتأكيد الأمر</span><span class="sxs-lookup"><span data-stu-id="05017-122">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="05017-123">وحدة الرأس</span><span class="sxs-lookup"><span data-stu-id="05017-123">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="05017-124">وحدة التذييل</span><span class="sxs-lookup"><span data-stu-id="05017-124">Footer module</span></span>](author-footer-module.md)
