---
title: إعداد الأكواد الشريطية
description: توضح هذه المقالة كيفية استخدام الأكواد الشريطية في Dynamics 365 Commerce.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailBarcodeMaskCharacter, RetailBarcodeMaskSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 74a08fc168dd3c41fa501ca8110af899a181e333
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021499"
---
# <a name="set-up-bar-codes"></a><span data-ttu-id="14bb4-103">إعداد الأكواد الشريطية</span><span class="sxs-lookup"><span data-stu-id="14bb4-103">Set up bar codes</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="14bb4-104">توضح هذه المقالة كيفية استخدام الأكواد الشريطية في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="14bb4-104">This article describes how to use bar codes in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="14bb4-105">يمكنك استخدام الاطكواد الشريطية لشراء وبيع المنتجات وتعقب متغيرات المنتج وإعداد العملاء والموظفين.</span><span class="sxs-lookup"><span data-stu-id="14bb4-105">You can use bar codes to purchase and sell products, track product variants, and set up customers and employees.</span></span> <span data-ttu-id="14bb4-106">ويمكنك أيضًا استخدام الرموز الشريطية لإصدار والموافقة على القسائم، وبطاقات الهدايا، ومذكرات الائتمان.</span><span class="sxs-lookup"><span data-stu-id="14bb4-106">You can also use bar codes to issue and endorse coupons, gift cards, and credit memos.</span></span> <span data-ttu-id="14bb4-107">كما يمكنك إعداد منتجات البيع بالتجزئة بحيث تشتمل على رموز الأكواد الشريطية القياسية أو المخصصة أو الداخلية.</span><span class="sxs-lookup"><span data-stu-id="14bb4-107">You can set up retail products so that they have standard bar codes or custom, in-house bar codes.</span></span> <span data-ttu-id="14bb4-108">ويمكن أن تحتوي المنتجات على أكثر من كود شريطي واحد.</span><span class="sxs-lookup"><span data-stu-id="14bb4-108">Products can have more than one bar code.</span></span> <span data-ttu-id="14bb4-109">على سبيل المثال، قد يشتمل منتج على رموز شريطية متعددة إذا جاء من العديد من الشركات المصنعة أو إذا اشتمل على متغيرات تعتمد على الحجم أو النمط أو اللون.</span><span class="sxs-lookup"><span data-stu-id="14bb4-109">For example, a product might have multiple bar codes if it comes from various manufacturers, or if it has variants that are based on size, style, or color.</span></span> <span data-ttu-id="14bb4-110">ويمكن لرموز الأكواد الشريطية أن تتضمن وزن المنتج أو سعره.</span><span class="sxs-lookup"><span data-stu-id="14bb4-110">Bar codes can include the weight or price of the product.</span></span> <span data-ttu-id="14bb4-111">وأقنعة الأكواد الشريطية هي قوالب يتم استخدامها لإنشاء الرموز الشريطية.</span><span class="sxs-lookup"><span data-stu-id="14bb4-111">Bar code masks are templates that are used to create bar codes.</span></span>

> [!NOTE]
> <span data-ttu-id="14bb4-112">إذا قمت بتعيين كود شريطي فريد لكل مجموعة متغير، فيمكنك مسح الكود الشريطي في السجل والسماح للبرنامج بتحديد متغير المنتج الذي يتم بيعه.</span><span class="sxs-lookup"><span data-stu-id="14bb4-112">If you assign a unique bar code to each variant combination, you can scan the bar code at the register and let the program determine which variant of the product is being sold.</span></span> <span data-ttu-id="14bb4-113">كما يمكنك تجميع وعرض الإحصاءات المتعلقة بالمبيعات حسب المتغير.</span><span class="sxs-lookup"><span data-stu-id="14bb4-113">You can also collect and view statistics about sales by variant.</span></span> <span data-ttu-id="14bb4-114">ويمكن تعيين رقم فريد لكل مجموعة نمط ولون وحجم يحدد هذه المجموعة في الكود الشريطي.</span><span class="sxs-lookup"><span data-stu-id="14bb4-114">Each size, color, and style group can be assigned a unique number that identifies that group in the bar code.</span></span> <span data-ttu-id="14bb4-115">يستخدم Retail قناع الكود الشريطي لإنشاء رموز الأكواد الشريطية تلقائيًا لكل مجموعة متغيرات.</span><span class="sxs-lookup"><span data-stu-id="14bb4-115">Retail uses the bar code mask to automatically generate bar codes for each variant combination.</span></span> <span data-ttu-id="14bb4-116">ويمكن أن تكون هذه الوظيفة مفيدة في حالة وجود العديد من الأحجام أو الألوان أو الأنماط نظرًا لزيادة عدد المجموعات بشكل كبير مع كل كود متغير تتم إضافته.</span><span class="sxs-lookup"><span data-stu-id="14bb4-116">This functionality can be useful if there are many sizes, colors, and styles, because the number of combinations increases significantly as each variant code is added.</span></span> <span data-ttu-id="14bb4-117">‏‫وفي حالة عدم استخدام هذه الوظيفة، فيجب أن يتم تعيين الأكواد الشريطية يدويًا لكل مجموعة تمثل متغير منتج.</span><span class="sxs-lookup"><span data-stu-id="14bb4-117">If this functionality isn't used, bar codes must be manually assigned to each combination that represents a product variant.</span></span>

<span data-ttu-id="14bb4-118">ويمكنك إنشاء رموز الأكواد الشريطية يدويًا أو تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="14bb4-118">You can create bar codes manually or automatically.</span></span> <span data-ttu-id="14bb4-119">لإنشاء الرموز الشريطية، أكمل المهام التالية بالترتيب الذي تم سردها به.</span><span class="sxs-lookup"><span data-stu-id="14bb4-119">To create bar codes, complete the following tasks in the order in which they are listed.</span></span>

1. <span data-ttu-id="14bb4-120">[إعداد أحرف قناع الكود الشريطي ](set-up-bar-code-masks.md).</span><span class="sxs-lookup"><span data-stu-id="14bb4-120">[Set up bar code mask characters](set-up-bar-code-masks.md).</span></span>
2. <span data-ttu-id="14bb4-121">[إعداد أقنعة الكود الشريطي ](set-up-bar-code-masks.md).</span><span class="sxs-lookup"><span data-stu-id="14bb4-121">[Set up bar code masks](set-up-bar-code-masks.md).</span></span>
3. <span data-ttu-id="14bb4-122">تكوين إعدادات الكود الشريطي.</span><span class="sxs-lookup"><span data-stu-id="14bb4-122">Configure bar code setups.</span></span>
4. <span data-ttu-id="14bb4-123">إنشاء رموز شريطية لمنتجات.</span><span class="sxs-lookup"><span data-stu-id="14bb4-123">Create bar codes for products.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="14bb4-124">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="14bb4-124">Additional resources</span></span>

[<span data-ttu-id="14bb4-125">إعداد أقنعة الأكواد الشريطية</span><span class="sxs-lookup"><span data-stu-id="14bb4-125">Set up bar code masks</span></span>](set-up-bar-code-masks.md)
