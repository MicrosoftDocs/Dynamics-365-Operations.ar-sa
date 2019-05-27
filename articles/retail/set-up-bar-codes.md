---
title: إعداد الأكواد الشريطية
description: توضح هذه المقالة كيفية استخدام الأكواد الشريطية في Microsoft Dynamics 365 for Retail.
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
ms.openlocfilehash: 15d12abe32d3f5a47348016c67a4fb02d0a5d8e3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555457"
---
# <a name="set-up-bar-codes"></a><span data-ttu-id="7124b-103">إعداد الأكواد الشريطية</span><span class="sxs-lookup"><span data-stu-id="7124b-103">Set up bar codes</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7124b-104">توضح هذه المقالة كيفية استخدام الأكواد الشريطية في Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="7124b-104">This article describes how to use bar codes in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="7124b-105">يمكنك استخدام الاطكواد الشريطية لشراء وبيع المنتجات وتعقب متغيرات المنتج وإعداد العملاء والموظفين.</span><span class="sxs-lookup"><span data-stu-id="7124b-105">You can use bar codes to purchase and sell products, track product variants, and set up customers and employees.</span></span> <span data-ttu-id="7124b-106">ويمكنك أيضًا استخدام الرموز الشريطية لإصدار والموافقة على القسائم، وبطاقات الهدايا، ومذكرات الائتمان.</span><span class="sxs-lookup"><span data-stu-id="7124b-106">You can also use bar codes to issue and endorse coupons, gift cards, and credit memos.</span></span> <span data-ttu-id="7124b-107">كما يمكنك إعداد منتجات البيع بالتجزئة بحيث تشتمل على رموز الأكواد الشريطية القياسية أو المخصصة أو الداخلية.</span><span class="sxs-lookup"><span data-stu-id="7124b-107">You can set up retail products so that they have standard bar codes or custom, in-house bar codes.</span></span> <span data-ttu-id="7124b-108">ويمكن أن تحتوي المنتجات على أكثر من كود شريطي واحد.</span><span class="sxs-lookup"><span data-stu-id="7124b-108">Products can have more than one bar code.</span></span> <span data-ttu-id="7124b-109">على سبيل المثال، قد يشتمل منتج على رموز شريطية متعددة إذا جاء من العديد من الشركات المصنعة أو إذا اشتمل على متغيرات تعتمد على الحجم أو النمط أو اللون.</span><span class="sxs-lookup"><span data-stu-id="7124b-109">For example, a product might have multiple bar codes if it comes from various manufacturers, or if it has variants that are based on size, style, or color.</span></span> <span data-ttu-id="7124b-110">ويمكن لرموز الأكواد الشريطية أن تتضمن وزن المنتج أو سعره.</span><span class="sxs-lookup"><span data-stu-id="7124b-110">Bar codes can include the weight or price of the product.</span></span> <span data-ttu-id="7124b-111">وأقنعة الأكواد الشريطية هي قوالب يتم استخدامها لإنشاء الرموز الشريطية.</span><span class="sxs-lookup"><span data-stu-id="7124b-111">Bar code masks are templates that are used to create bar codes.</span></span>

> [!NOTE]
> <span data-ttu-id="7124b-112">إذا قمت بتعيين كود شريطي فريد لكل مجموعة متغير، فيمكنك مسح الكود الشريطي في السجل والسماح للبرنامج بتحديد متغير المنتج الذي يتم بيعه.</span><span class="sxs-lookup"><span data-stu-id="7124b-112">If you assign a unique bar code to each variant combination, you can scan the bar code at the register and let the program determine which variant of the product is being sold.</span></span> <span data-ttu-id="7124b-113">كما يمكنك تجميع وعرض الإحصاءات المتعلقة بالمبيعات حسب المتغير.</span><span class="sxs-lookup"><span data-stu-id="7124b-113">You can also collect and view statistics about sales by variant.</span></span> <span data-ttu-id="7124b-114">ويمكن تعيين رقم فريد لكل مجموعة نمط ولون وحجم يحدد هذه المجموعة في الكود الشريطي.</span><span class="sxs-lookup"><span data-stu-id="7124b-114">Each size, color, and style group can be assigned a unique number that identifies that group in the bar code.</span></span> <span data-ttu-id="7124b-115">يستخدم Dynamics 365 for Retail قناع الكود الشريطي لإنشاء رموز الأكواد الشريطية تلقائيًا لكل مجموعة متغيرات.</span><span class="sxs-lookup"><span data-stu-id="7124b-115">Dynamics 365 for Retail uses the bar code mask to automatically generate bar codes for each variant combination.</span></span> <span data-ttu-id="7124b-116">ويمكن أن تكون هذه الوظيفة مفيدة في حالة وجود العديد من الأحجام أو الألوان أو الأنماط نظرًا لزيادة عدد المجموعات بشكل كبير مع كل كود متغير تتم إضافته.</span><span class="sxs-lookup"><span data-stu-id="7124b-116">This functionality can be useful if there are many sizes, colors, and styles, because the number of combinations increases significantly as each variant code is added.</span></span> <span data-ttu-id="7124b-117">‏‫وفي حالة عدم استخدام هذه الوظيفة، فيجب أن يتم تعيين الأكواد الشريطية يدويًا لكل مجموعة تمثل متغير منتج.</span><span class="sxs-lookup"><span data-stu-id="7124b-117">If this functionality isn't used, bar codes must be manually assigned to each combination that represents a product variant.</span></span>

<span data-ttu-id="7124b-118">ويمكنك إنشاء رموز الأكواد الشريطية يدويًا أو تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="7124b-118">You can create bar codes manually or automatically.</span></span> <span data-ttu-id="7124b-119">لإنشاء الرموز الشريطية، أكمل المهام التالية بالترتيب الذي تم سردها به.</span><span class="sxs-lookup"><span data-stu-id="7124b-119">To create bar codes, complete the following tasks in the order in which they are listed.</span></span>

1. <span data-ttu-id="7124b-120">[إعداد أحرف قناع الكود الشريطي ](set-up-bar-code-masks.md).</span><span class="sxs-lookup"><span data-stu-id="7124b-120">[Set up bar code mask characters](set-up-bar-code-masks.md).</span></span>
2. <span data-ttu-id="7124b-121">[إعداد أقنعة الكود الشريطي ](set-up-bar-code-masks.md).</span><span class="sxs-lookup"><span data-stu-id="7124b-121">[Set up bar code masks](set-up-bar-code-masks.md).</span></span>
3. <span data-ttu-id="7124b-122">تكوين إعدادات الكود الشريطي.</span><span class="sxs-lookup"><span data-stu-id="7124b-122">Configure bar code setups.</span></span>
4. <span data-ttu-id="7124b-123">إنشاء رموز شريطية لمنتجات.</span><span class="sxs-lookup"><span data-stu-id="7124b-123">Create bar codes for products.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7124b-124">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="7124b-124">Additional resources</span></span>

[<span data-ttu-id="7124b-125">إعداد أقنعة الأكواد الشريطية</span><span class="sxs-lookup"><span data-stu-id="7124b-125">Set up bar code masks</span></span>](set-up-bar-code-masks.md)
