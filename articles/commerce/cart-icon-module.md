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
ms.openlocfilehash: 137debe3f4cad3948d20b2902ea80e66fa74ffd4
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661137"
---
# <a name="cart-icon-module"></a><span data-ttu-id="1d4cb-103">وحدة أيقونة عربة التسوق</span><span class="sxs-lookup"><span data-stu-id="1d4cb-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1d4cb-104">يتناول هذا الموضوع وحدة أيقونة عربة التسوق ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1d4cb-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1d4cb-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="1d4cb-105">Overview</span></span>

<span data-ttu-id="1d4cb-106">تمثل وحدة أيقونة عربة التسوق في وحدة الرأس على الصفحة، وتُظهر عدد الأصناف في سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="1d4cb-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="1d4cb-107">تعرض أيضًا وحدة أيقونة سلة التسوق ملخص السلة (تعرف أيضًا بسلة تسوق صغيرة) عند تمرير الماوس فوق أيقونة السلة.</span><span class="sxs-lookup"><span data-stu-id="1d4cb-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="1d4cb-108">توفر سلة التسوق الصغيرة للمستخدم ملخص الأصناف الموجودة في سلة التسوق دون الحاجة إلى الانتقال إلى صفحة سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="1d4cb-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="1d4cb-109">بالإضافة إلى ذلك، تسمح أيضًا للمستخدم بالانتقال مباشرةً إلى صفحة السداد مع الخروج إذا أعجبه الملخص.</span><span class="sxs-lookup"><span data-stu-id="1d4cb-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="1d4cb-110">يؤدي ذلك إلى تقليل عدد عمليات التنقل في الصفحات ويسهل عملية السداد والخروج.</span><span class="sxs-lookup"><span data-stu-id="1d4cb-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

<span data-ttu-id="1d4cb-111">تظهر الصورة التالية مثالاً عن وحدة أيقونة سلة تسوق تعرض سلة تسوق صغيرة في رأس Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="1d4cb-111">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![مثال عن وحدة أيقونة سلة التسوق](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="1d4cb-113">خصائص الوحدة النمطية</span><span class="sxs-lookup"><span data-stu-id="1d4cb-113">Module properties</span></span>

- <span data-ttu-id="1d4cb-114">**إظهار سلة التسوق الصغيرة** – تمكّن هذه الخاصية، عندما تكون قيمتها صواب، عرض ملخص سلة التسوق (سلة التسوق الصغيرة) عند تمرير الماوس فوق أيقونة سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="1d4cb-114">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="1d4cb-115">هذه الوظيفة مدعومة فقط لمنافذ عرض سطح المكتب.</span><span class="sxs-lookup"><span data-stu-id="1d4cb-115">This functionality is only supported for desktop view ports.</span></span>

## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="1d4cb-116">إضافة وحدة سلة التسوق إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="1d4cb-116">Add a cart icon module to a page</span></span>

<span data-ttu-id="1d4cb-117">لإضافة وحدة ايقونة سلة التسوق، راجع [وحدة الرأس](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="1d4cb-117">To add a cart icon module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1d4cb-118">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="1d4cb-118">Additional resources</span></span>

[<span data-ttu-id="1d4cb-119">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="1d4cb-119">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="1d4cb-120">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="1d4cb-120">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="1d4cb-121">الوحدة النمطية للدفع</span><span class="sxs-lookup"><span data-stu-id="1d4cb-121">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="1d4cb-122">الوحدة النمطية لعنوان الشحن</span><span class="sxs-lookup"><span data-stu-id="1d4cb-122">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="1d4cb-123">الوحدة النمطية لخيارات التسليم</span><span class="sxs-lookup"><span data-stu-id="1d4cb-123">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="1d4cb-124">وحدة تفاصيل الأوامر</span><span class="sxs-lookup"><span data-stu-id="1d4cb-124">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="1d4cb-125">وحدة بطاقة الهدايا</span><span class="sxs-lookup"><span data-stu-id="1d4cb-125">Gift card module</span></span>](add-giftcard.md)
