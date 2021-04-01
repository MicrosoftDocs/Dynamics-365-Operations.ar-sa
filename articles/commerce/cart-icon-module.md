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
ms.openlocfilehash: 43bc274548de016f24569001bac94aff324bea12
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213224"
---
# <a name="cart-icon-module"></a><span data-ttu-id="802d2-103">الوحدة النمطية لرمز عربة التسوق</span><span class="sxs-lookup"><span data-stu-id="802d2-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="802d2-104">يتناول هذا الموضوع وحدة أيقونة عربة التسوق ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="802d2-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="802d2-105">تمثل وحدة أيقونة عربة التسوق في وحدة الرأس على الصفحة، وتُظهر عدد الأصناف في سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="802d2-105">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="802d2-106">تعرض أيضًا وحدة أيقونة سلة التسوق ملخص السلة (تعرف أيضًا بسلة تسوق صغيرة) عند تمرير الماوس فوق أيقونة السلة.</span><span class="sxs-lookup"><span data-stu-id="802d2-106">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="802d2-107">توفر سلة التسوق الصغيرة للمستخدم ملخص الأصناف الموجودة في سلة التسوق دون الحاجة إلى الانتقال إلى صفحة سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="802d2-107">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="802d2-108">بالإضافة إلى ذلك، تسمح أيضًا للمستخدم بالانتقال مباشرةً إلى صفحة السداد مع الخروج إذا أعجبه الملخص.</span><span class="sxs-lookup"><span data-stu-id="802d2-108">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="802d2-109">يؤدي ذلك إلى تقليل عدد عمليات التنقل في الصفحات ويسهل عملية السداد والخروج.</span><span class="sxs-lookup"><span data-stu-id="802d2-109">This reduces the number of page navigations and makes checkout faster.</span></span> 

> [!NOTE]
> <span data-ttu-id="802d2-110">يتوفر دعم الوحدة النمطية لأيقونة عربة التسوق في الوحدات النمطية للرأس في Dynamics 365 Commerce الإصدار 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="802d2-110">Support for the cart icon module is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>

<span data-ttu-id="802d2-111">تظهر الصورة التالية مثالاً عن وحدة أيقونة سلة تسوق تعرض سلة تسوق صغيرة في رأس Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="802d2-111">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![مثال عن وحدة أيقونة سلة التسوق](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="802d2-113">خصائص الوحدة النمطية</span><span class="sxs-lookup"><span data-stu-id="802d2-113">Module properties</span></span>

- <span data-ttu-id="802d2-114">**إظهار سلة التسوق الصغيرة** – تمكّن هذه الخاصية، عندما تكون قيمتها صواب، عرض ملخص سلة التسوق (سلة التسوق الصغيرة) عند تمرير الماوس فوق أيقونة سلة التسوق.</span><span class="sxs-lookup"><span data-stu-id="802d2-114">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="802d2-115">هذه الوظيفة مدعومة فقط لمنافذ عرض سطح المكتب.</span><span class="sxs-lookup"><span data-stu-id="802d2-115">This functionality is only supported for desktop view ports.</span></span>

## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="802d2-116">إضافة وحدة سلة التسوق إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="802d2-116">Add a cart icon module to a page</span></span>

<span data-ttu-id="802d2-117">لإضافة وحدة ايقونة سلة التسوق، راجع [وحدة الرأس](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="802d2-117">To add a cart icon module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="802d2-118">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="802d2-118">Additional resources</span></span>

[<span data-ttu-id="802d2-119">الوحدة النمطية لعربة التسوق</span><span class="sxs-lookup"><span data-stu-id="802d2-119">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="802d2-120">الوحدة النمطية للسداد مع الخروج</span><span class="sxs-lookup"><span data-stu-id="802d2-120">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="802d2-121">الوحدة النمطية للدفع</span><span class="sxs-lookup"><span data-stu-id="802d2-121">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="802d2-122">الوحدة النمطية لعنوان الشحن</span><span class="sxs-lookup"><span data-stu-id="802d2-122">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="802d2-123">الوحدة النمطية لخيارات التسليم</span><span class="sxs-lookup"><span data-stu-id="802d2-123">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="802d2-124">الوحدة النمطية لمعلومات الانتقاء</span><span class="sxs-lookup"><span data-stu-id="802d2-124">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="802d2-125">الوحدة النمطية لتفاصيل الأوامر</span><span class="sxs-lookup"><span data-stu-id="802d2-125">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="802d2-126">الوحدة النمطية لبطاقة الهدايا</span><span class="sxs-lookup"><span data-stu-id="802d2-126">Gift card module</span></span>](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]