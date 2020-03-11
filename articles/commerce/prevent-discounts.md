---
title: خيارات منع الخصومات لمنتجات البيع بالتجزئة
description: هناك أسباب مختلفة تكمن خلف رغبة تجار التجزئة في منع تطبيق الخصومات على بعض المنتجات، سواء من عرض ترويجي أو أثناء عملية البيع في نقطة البيع.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
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
ms.openlocfilehash: 6a683ffce487dc4388711ad160c2e8dc55a690dd
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057454"
---
# <a name="options-for-preventing-discounts-for-retail-products"></a><span data-ttu-id="53ed5-103">خيارات منع الخصومات لمنتجات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="53ed5-103">Options for preventing discounts for retail products</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="53ed5-104">هناك أسباب مختلفة تكمن خلف رغبة تجار التجزئة في منع تطبيق الخصومات على بعض المنتجات، سواء من عرض ترويجي أو أثناء عملية البيع في نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="53ed5-104">There are various reasons why retailers may want to prevent some products from being discounted, either from a promotion or during the sale at the POS.</span></span>

<span data-ttu-id="53ed5-105">سوف تسمح الخيارات التالية الموجودة على علامة تبويب **Commerce** للمنتجات الصادرة بتكوين المنتج لمنع جميع الخصومات أو الخصومات اليدوية.</span><span class="sxs-lookup"><span data-stu-id="53ed5-105">The following options, which can be found on the **Commerce** tab of released products, will allow the product to be configured to prevent all or manual discounts.</span></span> <span data-ttu-id="53ed5-106">يمكن أيضًا تحديد الإعدادات على مستوى الفئة من التدرج الهرمي للفئات.</span><span class="sxs-lookup"><span data-stu-id="53ed5-106">The settings can also be specified at the category level from the category hierarchy.</span></span>

- <span data-ttu-id="53ed5-107">**منع كافة الخصومات** – حدد هذا الخيار لمنع تطبيق كافة أنواع الخصومات على هذا المنتج.</span><span class="sxs-lookup"><span data-stu-id="53ed5-107">**Prevent all discounts** – Select this option to prevent all types of discounts from being applied to this product.</span></span> <span data-ttu-id="53ed5-108">وهذا يشمل العروض الترويجية مثل خصومات أصناف الخلط والمطابقة والكمية وخصومات الحد، بالإضافة إلى خصومات البنود والحركات اليدوية التي يتم تطبيقها أثناء عملية البيع من قبل مستخدم نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="53ed5-108">This includes promotions such as mix and match, quantity and threshold discounts, as well as manual line and transaction discounts that are applied during a sale by a POS user.</span></span>
- <span data-ttu-id="53ed5-109">**منع الخصومات اليدوية** – حدد هذا الخيار لمنع فقط خصومات البنود أو الحركات اليدوية التي يتم تطبيقها أثناء عملية بيع من قبل مستخدم نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="53ed5-109">**Prevent manual discounts** – Select this option to only prevent the manual line or transaction discounts that are applied during a sale by a POS user.</span></span> <span data-ttu-id="53ed5-110">تبقى المنتجات التي تم تحديد هذا الخيار لها مؤهلة للعروض الترويجية، مثل خصومات أصناف الخلط والمطابقة والكمية وخصومات الحد.</span><span class="sxs-lookup"><span data-stu-id="53ed5-110">Products with this option selected are still eligible for promotions, such as mix and match and quantity and threshold discounts.</span></span>

> [!NOTE]
> <span data-ttu-id="53ed5-111">لا تقيد هذه الإعدادات عملية تجاوز السعر، حيث تقوم بتعيين السعر الأساسي ولا تتم معاملتها على أنها خصم.</span><span class="sxs-lookup"><span data-stu-id="53ed5-111">These settings do not restrict the price override operation, because that sets the base price and is not treated as a discount.</span></span>

<span data-ttu-id="53ed5-112">[![حقل منع الخصومات](./media/prevent-discounts.png)](./media/prevent-discounts.png)</span><span class="sxs-lookup"><span data-stu-id="53ed5-112">[![Prevent discounts field](./media/prevent-discounts.png)](./media/prevent-discounts.png)</span></span>