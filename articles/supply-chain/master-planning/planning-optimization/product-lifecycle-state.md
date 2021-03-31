---
title: استبعاد المنتجات التي لها حالات دورة حياة منتج معينه
description: يشرح هذا الموضوع كيفيه استبعاد المنتجات التي تعتمد علي حاله دوره الحياة عند استخدام وظيفة تحسين التخطيط.
author: ChristianRytt
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-13
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a1e0c734db763ffa69e2d6540a07d5fa04c22ea1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227791"
---
# <a name="exclude-products-that-have-specific-product-lifecycle-states"></a><span data-ttu-id="e2603-103">استبعاد المنتجات التي لها حالات دورة حياة منتج معينه</span><span class="sxs-lookup"><span data-stu-id="e2603-103">Exclude products that have specific product lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e2603-104">تتضمن المنتجات الصادرة وإصدارات المنتجات الصادرة حقل **حاله دوره حياه المنتج**.</span><span class="sxs-lookup"><span data-stu-id="e2603-104">Released products and released product versions include a **Product lifecycle state** field.</span></span> <span data-ttu-id="e2603-105">يتيح لك هذا الحقل التحكم في المنتجات ، من ضمن أشياء أخرى ، والتي يتم تضمينها اثناء التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="e2603-105">This field lets you control, among other things, which products are included during master planning.</span></span> <span data-ttu-id="e2603-106">يمكنك أضافه وأزاله وتحرير حالات الدورات الحياة كما هو مطلوب من خلال الانتقال إلى **أداره معلومات المنتج \> إعداد \>حاله دوره حياه المنتج**.</span><span class="sxs-lookup"><span data-stu-id="e2603-106">You can add, remove, and edit lifecycle states as required by going to **Product information management \> Setup \> Product lifecycle state**.</span></span> <span data-ttu-id="e2603-107">بالنسبة لكل حاله من دوره حياه المنتج ، تكون قيمه تعيين **نشطه لخيار التخطيط** إلى *نعم* إذا كان يجب تضمين المنتجات التي لها هذه الحالة اثناء التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="e2603-107">For each product lifecycle state, set the **Is active for planning** option to *Yes* if products that have that state should be included during master planning.</span></span> <span data-ttu-id="e2603-108">عند تعيين الخيار علي *لا*، سيتم استبعاد المنتجات والمتغيرات المرتبطة من كافة التخطيطات الرئيسية وكافة الحسابات علي مستوي قائمة مكونات الصنف (BOM).</span><span class="sxs-lookup"><span data-stu-id="e2603-108">When the option is set to *No*, the associated products and variants will be excluded from all master planning and all calculations at the bill of materials (BOM) level.</span></span>

<span data-ttu-id="e2603-109">تعامل المنتجات والمتغيرات الصادرة التي يتم تركها في الحقل حاله **دوره حياه المنتج** فارغا كما لو انه تم تعيين حاله دوره حياه المنتج عندما **يكون نشطا لخيار التخطيط** معينا إلى *نعم*.</span><span class="sxs-lookup"><span data-stu-id="e2603-109">Released products and variants where the **Product lifecycle state** field is left blank are treated as though they have a product lifecycle state where the **Is active for planning** option is set to *Yes*.</span></span> <span data-ttu-id="e2603-110">بمعني آخر ، سيتم تضمينها اثناء التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="e2603-110">In other words, they will be included during master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="e2603-111">للمساعدة علي تجنب اقتراحات التوريد غير الضرورية ، نوصي بشده باقران كافة المنتجات والمنتجات القديمة التي تم إصدارها بحاله دوره حياه المنتج حيث **يكون نشطا لخيار التخطيط في وضع التنشيط** علي *لا*.</span><span class="sxs-lookup"><span data-stu-id="e2603-111">To help avoid unnecessary supply suggestions, we strongly recommend that you associate all obsolete released products and variants with a product lifecycle state where the **Is active for planning** option is set to *No*.</span></span> <span data-ttu-id="e2603-112">وتعتبر هذه الطريقة هامه بشكل خاص عند العمل مع متغيرات تكوين المنتج التي لا يمكن أعاده استخدامها ، لأنها ستساعد في منع المهدورات.</span><span class="sxs-lookup"><span data-stu-id="e2603-112">This approach is especially important when you work with product configuration variants that aren't reusable, because it will help prevent waste.</span></span>

## <a name="related-resources"></a><span data-ttu-id="e2603-113">الموارد ذات الصلة</span><span class="sxs-lookup"><span data-stu-id="e2603-113">Related resources</span></span>

<span data-ttu-id="e2603-114">لمزيد من المعلومات حول حالات دورة حياة المنتجات، راجع [‏‫نظرة عامة على حالة دورة حياة المنتجات‬](../../pim/product-lifecycle.md).</span><span class="sxs-lookup"><span data-stu-id="e2603-114">For more information about product lifecycle states, see [Product lifecycle state overview](../../pim/product-lifecycle.md).</span></span>

<span data-ttu-id="e2603-115">للحصول على معلومات تفصيلية تتضمن خطوات استخدام حالات دورة حياة المنتج لاستبعاد منتجات من التخطيط الرئيسي وحساب مستوى قائمة مكونات الصنف، راجع [إنشاء حالة دورة حياة منتج لاستبعاد المنتجات من التخطيط الرئيسي](../../pim/tasks/exclude-products-master-planning.md).</span><span class="sxs-lookup"><span data-stu-id="e2603-115">For detailed information that includes steps for using product lifecycle states to exclude products from master planning and BOM-level calculations, see [Create a product lifecycle state to exclude products from Master planning](../../pim/tasks/exclude-products-master-planning.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]