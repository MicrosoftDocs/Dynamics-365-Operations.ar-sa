---
title: "منع الخصومات لمنتجات البيع بالتجزئة"
description: "هناك أسباب مختلفة تكمن خلف رغبة تجار التجزئة في منع تطبيق الخصومات على بعض المنتجات، سواء من عرض ترويجي أو أثناء عملية البيع في نقطة البيع."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: e8c5a24f-7edd-4fd6-af80-5e0ac9f03127
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 2c9045b6383e66dfe1df61eda483525ca4741854
ms.contentlocale: ar-sa
ms.lasthandoff: 02/07/2018

---

# <a name="prevent-discounts-for-retail-products"></a><span data-ttu-id="76bfb-103">منع الخصومات لمنتجات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="76bfb-103">Prevent discounts for retail products</span></span>

[!include[banner](includes/banner.md)]

<span data-ttu-id="76bfb-104">هناك أسباب مختلفة تكمن خلف رغبة تجار التجزئة في منع تطبيق الخصومات على بعض المنتجات، سواء من عرض ترويجي أو أثناء عملية البيع في نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="76bfb-104">There are various reasons why retailers may want to prevent some products from being discounted, either from a promotion or during the sale at the POS.</span></span>

<span data-ttu-id="76bfb-105">سوف تسمح الخيارات التالية الموجودة على علامة تبويب **Retail** للمنتجات الصادرة بتكوين المنتج لمنع جميع الخصومات أو الخصومات اليدوية.</span><span class="sxs-lookup"><span data-stu-id="76bfb-105">The following options, which can be found on the **Retail** tab of released products, will allow the product to be configured to prevent all or manual discounts.</span></span> <span data-ttu-id="76bfb-106">يمكن أيضًا تحديد الإعدادات على مستوى الفئة من التدرج الهرمي لفئات البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="76bfb-106">The settings can also be specified at the category level from the retail category hierarchy.</span></span>

<span data-ttu-id="76bfb-107">**منع كافة الخصومات**: حدد هذا الخيار لمنع تطبيق كافة أنواع الخصومات على هذا المنتج.</span><span class="sxs-lookup"><span data-stu-id="76bfb-107">**Prevent all discounts**: Select this option to prevent all types of discounts from being applied to this product.</span></span> <span data-ttu-id="76bfb-108">وهذا يشمل العروض الترويجية مثل خصومات أصناف الخلط والمطابقة والكمية وخصومات الحد، بالإضافة إلى خصومات البنود والحركات اليدوية التي يتم تطبيقها أثناء عملية البيع من قبل مستخدم نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="76bfb-108">This includes promotions such as mix and match, quantity and threshold discounts, as well as manual line and transaction discounts that are applied during a sale by a POS user.</span></span>

<span data-ttu-id="76bfb-109">**منع الخصومات اليدوية**: حدد هذا الخيار لمنع فقط خصومات البنود أو الحركات أو اليدوية التي يتم تطبيقها أثناء عملية بيع من قبل مستخدم نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="76bfb-109">**Prevent manual discounts**: Select this option to only prevent the manual line or transaction discounts that are applied during a sale by a POS user.</span></span> <span data-ttu-id="76bfb-110">تبقى المنتجات التي تم تحديد هذا الخيار لها مؤهلة للعروض الترويجية، مثل خصومات أصناف الخلط والمطابقة والكمية وخصومات الحد.</span><span class="sxs-lookup"><span data-stu-id="76bfb-110">Products with this option selected are still eligible for promotions, such as mix and match and quantity and threshold discounts.</span></span>

<span data-ttu-id="76bfb-111">**ملاحظة**: لا تقيد هذه الإعدادات عملية تجاوز السعر، حيث تقوم بتعيين السعر الأساسي ولا تتم معاملتها على أنها خصم.</span><span class="sxs-lookup"><span data-stu-id="76bfb-111">**Note**: These settings do not restrict the price override operation, because that sets the base price and is not treated as a discount.</span></span>  

<span data-ttu-id="76bfb-112">[![حقل منع الخصومات](./media/prevent discounts.png)](./media/prevent discounts.png)</span><span class="sxs-lookup"><span data-stu-id="76bfb-112">[![prevent discounts field](./media/prevent discounts.png)](./media/prevent discounts.png)</span></span>

