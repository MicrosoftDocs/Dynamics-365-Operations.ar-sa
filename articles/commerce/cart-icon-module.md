---
title: وحدة أيقونة عربة التسوق
description: يتناول هذا الموضوع وحدة أيقونة عربة التسوق ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 138c256b56593c4fafb20050a97e614fa584597c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997815"
---
# <a name="cart-icon-module"></a><span data-ttu-id="a7bbd-103">وحدة أيقونة عربة التسوق</span><span class="sxs-lookup"><span data-stu-id="a7bbd-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a7bbd-104">يتناول هذا الموضوع وحدة أيقونة عربة التسوق ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a7bbd-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a7bbd-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="a7bbd-105">Overview</span></span>

<span data-ttu-id="a7bbd-106">تمثل وحدة أيقونة عربة التسوق في وحدة الرأس على الصفحة، وتُظهر عدد الأصناف في سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="a7bbd-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="a7bbd-107">تعرض أيضًا وحدة أيقونة سلة التسوق ملخص السلة (تعرف أيضًا بسلة تسوق صغيرة) عند تمرير الماوس فوق أيقونة السلة.</span><span class="sxs-lookup"><span data-stu-id="a7bbd-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="a7bbd-108">توفر سلة التسوق الصغيرة للمستخدم ملخص الأصناف الموجودة في سلة التسوق دون الحاجة إلى الانتقال إلى صفحة سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="a7bbd-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="a7bbd-109">بالإضافة إلى ذلك، تسمح أيضًا للمستخدم بالانتقال مباشرةً إلى صفحة السداد مع الخروج إذا أعجبه الملخص.</span><span class="sxs-lookup"><span data-stu-id="a7bbd-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="a7bbd-110">يؤدي ذلك إلى تقليل عدد عمليات التنقل في الصفحات ويسهل عملية السداد والخروج.</span><span class="sxs-lookup"><span data-stu-id="a7bbd-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

> [!NOTE]
> <span data-ttu-id="a7bbd-111">يتوفر دعم الوحدة النمطية لأيقونة عربة التسوق في الوحدات النمطية للرأس في Dynamics 365 Commerce الإصدار 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="a7bbd-111">Support for the cart icon module is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>

<span data-ttu-id="a7bbd-112">تظهر الصورة التالية مثالاً عن وحدة أيقونة سلة تسوق تعرض سلة تسوق صغيرة في رأس Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="a7bbd-112">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![مثال عن وحدة أيقونة سلة التسوق](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="a7bbd-114">خصائص الوحدة النمطية</span><span class="sxs-lookup"><span data-stu-id="a7bbd-114">Module properties</span></span>

- <span data-ttu-id="a7bbd-115">**إظهار سلة التسوق الصغيرة** – تمكّن هذه الخاصية، عندما تكون قيمتها صواب، عرض ملخص سلة التسوق (سلة التسوق الصغيرة) عند تمرير الماوس فوق أيقونة سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="a7bbd-115">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="a7bbd-116">هذه الوظيفة مدعومة فقط لمنافذ عرض سطح المكتب.</span><span class="sxs-lookup"><span data-stu-id="a7bbd-116">This functionality is only supported for desktop view ports.</span></span>

## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="a7bbd-117">إضافة وحدة سلة التسوق إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="a7bbd-117">Add a cart icon module to a page</span></span>

<span data-ttu-id="a7bbd-118">لإضافة وحدة ايقونة سلة التسوق، راجع [وحدة الرأس](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="a7bbd-118">To add a cart icon module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a7bbd-119">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="a7bbd-119">Additional resources</span></span>

[<span data-ttu-id="a7bbd-120">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="a7bbd-120">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="a7bbd-121">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="a7bbd-121">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="a7bbd-122">الوحدة النمطية للدفع</span><span class="sxs-lookup"><span data-stu-id="a7bbd-122">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="a7bbd-123">الوحدة النمطية لعنوان الشحن</span><span class="sxs-lookup"><span data-stu-id="a7bbd-123">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="a7bbd-124">الوحدة النمطية لخيارات التسليم</span><span class="sxs-lookup"><span data-stu-id="a7bbd-124">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="a7bbd-125">الوحدة النمطية لمعلومات الانتقاء</span><span class="sxs-lookup"><span data-stu-id="a7bbd-125">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="a7bbd-126">الوحدة النمطية لتفاصيل الأوامر</span><span class="sxs-lookup"><span data-stu-id="a7bbd-126">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="a7bbd-127">الوحدة النمطية لبطاقة الهدايا</span><span class="sxs-lookup"><span data-stu-id="a7bbd-127">Gift card module</span></span>](add-giftcard.md)
