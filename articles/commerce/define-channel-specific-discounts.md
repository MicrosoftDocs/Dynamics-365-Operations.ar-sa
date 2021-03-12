---
title: تحديد الخصومات الخاصة بالقناة
description: يعيّن تجار البيع بالتجزئة في أغلب الأحيان خصومات مختلفة في قنوات مختلفة. يستعرض هذا الموضوع المفاهيم التي تحتاج إلى معرفتها لإنشاء خصم لقناة محددة.
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 990c0d0b4b89420094dc86552b3e07717e5c7056
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991380"
---
# <a name="define-channel-specific-discounts"></a><span data-ttu-id="80f8b-104">تحديد الخصومات الخاصة بالقناة</span><span class="sxs-lookup"><span data-stu-id="80f8b-104">Define channel-specific discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="80f8b-105">يستعرض هذا الموضوع المفاهيم التي تحتاج إلى معرفتها لإنشاء خصم لقناة محددة.</span><span class="sxs-lookup"><span data-stu-id="80f8b-105">This topic reviews the concepts you need to know to create a discount for a specific channel.</span></span>

## <a name="channel-specific-discounts"></a><span data-ttu-id="80f8b-106">الخصومات الخاصة بالقناة</span><span class="sxs-lookup"><span data-stu-id="80f8b-106">Channel-specific discounts</span></span>

<span data-ttu-id="80f8b-107">‏‫يقدم تجار التجزئة غالباً خصومات مختلفة في قنوات مختلفة.</span><span class="sxs-lookup"><span data-stu-id="80f8b-107">Retailers often offer different discounts in different channels.</span></span> <span data-ttu-id="80f8b-108">قد يتم إجراء ذلك للتعامل مع ظروف السوق المحلية أو التعامل مع تجار التجزئة المنافسين.‬</span><span class="sxs-lookup"><span data-stu-id="80f8b-108">This may be done to address local market conditions or to deal with competing retailers.</span></span>

<span data-ttu-id="80f8b-109">يستخدم Commerce مجموعات الأسعار لتحديد الخصومات المحددة للقناة.</span><span class="sxs-lookup"><span data-stu-id="80f8b-109">Commerce uses price groups to define channel-specific discounts.</span></span> <span data-ttu-id="80f8b-110">ويمكن تعيين مجموعات الأسعار لواحدة أو أكثر من الوحدات التالية: القنوات والكتالوجات والتبعيات وبرامج الولاء.</span><span class="sxs-lookup"><span data-stu-id="80f8b-110">Price groups can be assigned to one or more of the following entities: channels, catalogs, affiliations, and loyalty programs.</span></span> <span data-ttu-id="80f8b-111">وتتناول هذه المقالة القنوات، لكن نفس المفاهيم تنطبق على خصومات الكتالوج وخصومات التبعيات وخصومات الولاء.</span><span class="sxs-lookup"><span data-stu-id="80f8b-111">This article discusses channels, but the same concepts apply to catalog discounts, affiliations discounts, and loyalty discounts.</span></span>

## <a name="price-groups"></a><span data-ttu-id="80f8b-112">مجموعات الأسعار</span><span class="sxs-lookup"><span data-stu-id="80f8b-112">Price groups</span></span>

<span data-ttu-id="80f8b-113">[![مجموعات الأسعار](./media/price-groups-1024x608.png)](./media/price-groups.png)</span><span class="sxs-lookup"><span data-stu-id="80f8b-113">[![Price groups](./media/price-groups-1024x608.png)](./media/price-groups.png)</span></span>

<span data-ttu-id="80f8b-114">‏‫يوضح الرسم البياني أعلاه العلاقة بين الكيانات التي قد تكون موجودة في حركة (القناة، الكتالوج، التبعيات، العميل، بطاقة الولاء) ومختلف أنواع الخصم التي يمكن تكوينها.</span><span class="sxs-lookup"><span data-stu-id="80f8b-114">The diagram above illustrates the relationship between entities that may be on a transaction (channel, catalog, affiliation, customer, loyalty card) and the various discount types that can be configured.</span></span> <span data-ttu-id="80f8b-115">وتتم كافة الحركات في قناة، حيث يتم ضمان القناة لتقديمها في حركة.‬</span><span class="sxs-lookup"><span data-stu-id="80f8b-115">All transactions occur in a channel, so the channel is guaranteed to be present on a transaction.</span></span> <span data-ttu-id="80f8b-116">الكيانات المتبقية اختيارية.</span><span class="sxs-lookup"><span data-stu-id="80f8b-116">The remaining entities are optional.</span></span> <span data-ttu-id="80f8b-117">وفي كل صفحة من صفحات البيانات الرئيسية، هناك رابط إلى صفحة مجموعات الأسعار ذات الصلة، حيث يمكنك عرض وإضافة مجموعات الأسعار عند اللزوم.</span><span class="sxs-lookup"><span data-stu-id="80f8b-117">On each master data pages there is a link to a related price groups page where you can view and add price groups as needed.</span></span> <span data-ttu-id="80f8b-118">يتم استخدام مجموعة أسعار لربط أربعة أنواع مختلفة من الكيانات بتسويات الأسعار والخصومات والاتفاقيات التجارية.</span><span class="sxs-lookup"><span data-stu-id="80f8b-118">A price group is used to relate four different types of entities to discounts, price adjustments, and trade agreements.</span></span> <span data-ttu-id="80f8b-119">ونُوصي بأن تخطط إستراتيجية للطريقة التي ستسمي بها مجموعات الأسعار الخاصة بك للحفاظ على تنظيمها.‬</span><span class="sxs-lookup"><span data-stu-id="80f8b-119">We recommend that you plan a strategy for how you will name your price groups to keep them organized.</span></span> <span data-ttu-id="80f8b-120">هناك خيار واحد يتمثل في استخدام حرف أو بادئة رقم أو لاحقة رقم للتمييز بين الأنواع المختلفة.</span><span class="sxs-lookup"><span data-stu-id="80f8b-120">One option would be to use a letter or number prefix or suffix to distinguish between the different types.</span></span> <span data-ttu-id="80f8b-121">على سبيل المثال، 1-xxxxx لمجموعات أسعار القنوات و2-xxxxx لمجموعات أسعار الكتالوج.‬</span><span class="sxs-lookup"><span data-stu-id="80f8b-121">For example, 1-xxxxx for channel price groups and 2-xxxxx for catalog price groups.</span></span> <span data-ttu-id="80f8b-122">توجد أربع صفحات استعلام تركز على كل كيان من الكيانات التجارية التي يمكن ارتباط الخصومات بها.</span><span class="sxs-lookup"><span data-stu-id="80f8b-122">There are four inquiry pages that focus on each of the commerce entities that can have discounts associated to them.</span></span>

- <span data-ttu-id="80f8b-123">**مجموعات أسعار القنوات** - تعرض هذه الصفحة قائمة بالقنوات والخصومات المرتبطة ببعضها بعضًا لكل مجموعة أسعار.</span><span class="sxs-lookup"><span data-stu-id="80f8b-123">**Channel channel price groups** – This page shows a list of channels and discounts linked together for each price group.</span></span>
- <span data-ttu-id="80f8b-124">**مجموعات أسعار الكتالوج** – تعرض هذه الصفحة قائمة بالكتالوجات والخصومات المرتبطة ببعضها البعض لكل مجموعة أسعار.</span><span class="sxs-lookup"><span data-stu-id="80f8b-124">**Catalog price groups** – This page shows a list of catalogs and discounts linked together for each price group.</span></span>
- <span data-ttu-id="80f8b-125">**مجموعات أسعار الولاء** - تعرض هذه الصفحة قائمة ببرامج الولاء والخصومات المرتبطة ببعضها البعض لكل مجموعة أسعار.</span><span class="sxs-lookup"><span data-stu-id="80f8b-125">**Loyalty price groups** – This page shows a list of loyalty programs and discounts linked together for each price group.</span></span>
- <span data-ttu-id="80f8b-126">**مجموعات أسعار التبعيات** - تعرض هذه الصفحة قائمة بالتبعيات والخصومات المرتبطة ببعضها البعض لكل مجموعة أسعار.</span><span class="sxs-lookup"><span data-stu-id="80f8b-126">**Affiliation price groups** – This page shows a list of affiliations and discounts linked together for each price group.</span></span>

## <a name="example-channel-discount-set-up"></a><span data-ttu-id="80f8b-127">مثال على إعداد خصومات القناة</span><span class="sxs-lookup"><span data-stu-id="80f8b-127">Example channel discount set up</span></span>

<span data-ttu-id="80f8b-128">يوضح المثال التالي المهام المتضمنة في إعداد خصم قناة.</span><span class="sxs-lookup"><span data-stu-id="80f8b-128">The following example illustrates the tasks involved in setting up a channel discount.</span></span>

1. <span data-ttu-id="80f8b-129">على سبيل المثال، لديك قناة تسمى **هيوستن**، وستقوم بإنشاء خصم جديد يسمى **العودة إلى المدرسة.**</span><span class="sxs-lookup"><span data-stu-id="80f8b-129">For this example, you have a channel called **Houston**, and you're going to create a new discount called **Back-to-School**.</span></span>
2. <span data-ttu-id="80f8b-130">لأن استراتيجية التسعير والخصم تتضمن إمكانية خصومات القنوات، يمكنك دائمًا إنشاء مجموعة أسعار خاصة بالقناة عند إنشاء قناة.</span><span class="sxs-lookup"><span data-stu-id="80f8b-130">Because the pricing and discount strategy includes the possibility of channel discounts, you always create a channel-specific price group when you create a channel.</span></span>
3. <span data-ttu-id="80f8b-131">لديك مجموعة أسعار **هيوستن-بي جي** وتم تعيينها إلى قناة **هيوستن**.</span><span class="sxs-lookup"><span data-stu-id="80f8b-131">You have the price group **Houston-PG** and it is assigned to the **Houston** channel.</span></span>
4. <span data-ttu-id="80f8b-132">بعد إنشاء خصم **العودة إلى المدرسة** الجديد، يجب عليك النقر فوق **مجموعات الأسعار** في الجزء العلوي من صفحة **الخصم**.</span><span class="sxs-lookup"><span data-stu-id="80f8b-132">After you create the new **Back-to-School** discount, you need to click **Price groups** on the top of the **Discount** page.</span></span> <span data-ttu-id="80f8b-133">سيتم فتح صفحة **مجموعات أسعار الخصومات**.</span><span class="sxs-lookup"><span data-stu-id="80f8b-133">The **Discount price groups** page will open.</span></span> <span data-ttu-id="80f8b-134">وبعد ذلك، انقر فوق **جديد**، وحدد مجموعة الأسعار **هيوستن-بي جي**.</span><span class="sxs-lookup"><span data-stu-id="80f8b-134">Next, click **New** and select the **Houston-PG** price group.</span></span>
5. <span data-ttu-id="80f8b-135">يمكنك الآن تمكين الخصم ودفعه للقناة.</span><span class="sxs-lookup"><span data-stu-id="80f8b-135">Now you can enable the discount and push it to the channel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="80f8b-136">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="80f8b-136">Additional resources</span></span>

[<span data-ttu-id="80f8b-137">تعديلات الأسعار والخصومات</span><span class="sxs-lookup"><span data-stu-id="80f8b-137">Price adjustments and discounts</span></span>](price-adjustments-discounts.md)
