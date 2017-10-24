---
title: "مواصفات التشغيلة"
description: "توفر هذه المقالة معلومات حول مواصفات التشغيلة. مواصفات التشغيلة هي الصفات المميزة للمواد الخام والمنتجات التامة الصنع والتي تشكل مجموعات المخزون. كما توضح هذه المقالة كيفية تعيين مواصفات التشغيلة، وكيف يمكنك البحث فيها عند حجز الدُفعات."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PdsBatchAttrib, PdsBatchAttribAssociate, PdsBatchAttribByAttribGroup, PdsBatchAttribByItem, PdsBatchAttribByitemCustomer, PdsBatchAttribGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19271
ms.assetid: 41de0250-4a96-412e-a412-aa06615b6b1d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0c3f5115377178941984e53749c18cc1c9179812
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="batch-attributes"></a><span data-ttu-id="4e3ee-105">مواصفات التشغيلة</span><span class="sxs-lookup"><span data-stu-id="4e3ee-105">Batch attributes</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="4e3ee-106">توفر هذه المقالة معلومات حول مواصفات التشغيلة.</span><span class="sxs-lookup"><span data-stu-id="4e3ee-106">This article provides information about batch attributes.</span></span> <span data-ttu-id="4e3ee-107">مواصفات التشغيلة هي الصفات المميزة للمواد الخام والمنتجات التامة الصنع والتي تشكل مجموعات المخزون.</span><span class="sxs-lookup"><span data-stu-id="4e3ee-107">Batch attributes are characteristics of raw materials and finished products that make up inventory batches.</span></span> <span data-ttu-id="4e3ee-108">كما توضح هذه المقالة كيفية تعيين مواصفات التشغيلة، وكيف يمكنك البحث فيها عند حجز الدُفعات.</span><span class="sxs-lookup"><span data-stu-id="4e3ee-108">The article also explains how to assign batch attributes, and how you can search on them when you reserve batches.</span></span>

<span data-ttu-id="4e3ee-109">مواصفات التشغيلة هي الصفات المميزة للمواد الخام والمنتجات التامة الصنع والتي تشكل مجموعات المخزون.</span><span class="sxs-lookup"><span data-stu-id="4e3ee-109">Batch attributes are characteristics of raw materials and finished products that make up inventory batches.</span></span> <span data-ttu-id="4e3ee-110">ويمكن أن تختلف المواصفات التشغيلية، تبعاً لعوامل مثل الظروف البيئية، أو جودة المواد الخام التي تُستخدم لإنتاج الدُفعة، أو نتيجة المنتج النهائي.</span><span class="sxs-lookup"><span data-stu-id="4e3ee-110">Batch attributes can vary, depending on factors such as environmental conditions, the quality of the raw materials that are used to produce the batch, or the outcome of the finished product.</span></span> <span data-ttu-id="4e3ee-111">عدد وأنواع المواصفات التشغيلية المستخدمة يمكن أن تتفاوت تفاوتاً كبيرًا من صناعة إلى أخرى.</span><span class="sxs-lookup"><span data-stu-id="4e3ee-111">The number and types of batch attributes that are used can vary widely from one industry to another.</span></span> <span data-ttu-id="4e3ee-112">فيما يلي مثالين يوضحان كيفية استخدام المواصفات التشغيلية:</span><span class="sxs-lookup"><span data-stu-id="4e3ee-112">Here are two examples that show how to use batch attributes:</span></span>

-   <span data-ttu-id="4e3ee-113">في صناعة الجبن، يمكن أن يشتمل اللبن، وهو من المواد الخام التي تُستخدم لإنتاج الجبن، على سمات مثل وزن محتوى الدهون والوزن بالنسبة المئوية.</span><span class="sxs-lookup"><span data-stu-id="4e3ee-113">In the cheese industry, milk, which is one of the raw materials that are used to produce the cheese, can have attributes such as fat content and percentage weight.</span></span> <span data-ttu-id="4e3ee-114">ويمكن أن يشتمل الجبن الذي تم إنتاجه من الحليب سمات أخرى، مثل الرطوبة والعمر.</span><span class="sxs-lookup"><span data-stu-id="4e3ee-114">The cheese that is produced from the milk can have other attributes, such as moisture and age.</span></span>
-   <span data-ttu-id="4e3ee-115">وفي صناعة الصلب، قد يشمل الحديد سمات مثل النسب المئوية لمحتوى الماغنسيوم، ومحتوى الفضة، ومحتوى الزنك.</span><span class="sxs-lookup"><span data-stu-id="4e3ee-115">In the steel industry, the iron that is produced might have attributes such as the percentages of magnesium content, silver content, and zinc content.</span></span>

<span data-ttu-id="4e3ee-116">ولإدارة عدد وأنواع السمات بشكل أفضل، يمكنك استخدام مجموعات المواصفات التشغيلية.</span><span class="sxs-lookup"><span data-stu-id="4e3ee-116">To better manage the number and types of attributes, you can use batch attribute groups.</span></span> <span data-ttu-id="4e3ee-117">وبهذه الطريقة، لا يلزمك إضافة كل سمة على حدة.</span><span class="sxs-lookup"><span data-stu-id="4e3ee-117">In this way, you don't have to add each attribute individually.</span></span>

## <a name="assign-batch-attributes"></a><span data-ttu-id="4e3ee-118">تعيين المواصفات التشغيلة</span><span class="sxs-lookup"><span data-stu-id="4e3ee-118">Assign batch attributes</span></span>
<span data-ttu-id="4e3ee-119">يمكنك تعيين المواصفات التشغيلية للمنتجات الفردية التي يُحتفظ يها في دُفعات المخزون، أو يمكنك تعيينها للمنتجات المرتبطة بعملاء معينين.</span><span class="sxs-lookup"><span data-stu-id="4e3ee-119">You can assign batch attributes to individual products that are held in inventory batches, or you can assign them to products that are associated with specific customers.</span></span> <span data-ttu-id="4e3ee-120">وقبل تعيين مواصفة تشغيلية على مستوى العميل، يجب تعيينها على مستوى المنتج.</span><span class="sxs-lookup"><span data-stu-id="4e3ee-120">Before you can assign a batch attribute at the customer level, you must assign it at the product level.</span></span> <span data-ttu-id="4e3ee-121">يجب تعيين المنتج على مجموعة أبعاد الدُفعة إلى **نشطة** في مجموعة أبعاد التعقب.</span><span class="sxs-lookup"><span data-stu-id="4e3ee-121">The product must have the batch dimension set to **Active** in the tracking dimension group.</span></span> <span data-ttu-id="4e3ee-122">ولتعيين مواصفة تشغيلية لمنتج واحد، استخدم الصفحة الخاصة بالمنتج.</span><span class="sxs-lookup"><span data-stu-id="4e3ee-122">To assign a batch attribute to an individual product, use the product-specific page.</span></span> <span data-ttu-id="4e3ee-123">وإذا كانت السمة خاصة بمنتج عميل، استخدم الصفحة الخاصة بالعميل.</span><span class="sxs-lookup"><span data-stu-id="4e3ee-123">If the attribute is specific to a product for a customer, use the customer-specific page.</span></span> <span data-ttu-id="4e3ee-124">وعند إضافة سمة إلى منتج، يمكنك أيضًا تحديد معلمات أخرى.</span><span class="sxs-lookup"><span data-stu-id="4e3ee-124">When you add an attribute to a product, you also define other parameters.</span></span> <span data-ttu-id="4e3ee-125">فيما يلي بعض الأمثلة:</span><span class="sxs-lookup"><span data-stu-id="4e3ee-125">Here are some examples:</span></span>

-   <span data-ttu-id="4e3ee-126">الحد الأدنى والحد الأقصى للسمة من نوع **العدد الصحيح** أو **الكسر**.</span><span class="sxs-lookup"><span data-stu-id="4e3ee-126">The minimum and maximum ranges for an attribute of the **Integer** or **Fraction** type.</span></span>
-   <span data-ttu-id="4e3ee-127">‏‫إجراءات التفاوت للسمة من نوع **العدد الصحيح** أو **الكسر‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="4e3ee-127">The tolerance actions for an attribute of the **Integer** or **Fraction** type.</span></span> <span data-ttu-id="4e3ee-128">إذا كانت قيمة السمة تقع خارج نطاق الحد الأدنى والحد الأقصى، يمكن أن يكون الإجراء إما رسالة تحذير أو رسالة خطأ.‬</span><span class="sxs-lookup"><span data-stu-id="4e3ee-128">If the value of the attribute falls outside the minimum and maximum range, the action can be either a warning message or an error message.</span></span>
-   <span data-ttu-id="4e3ee-129">القيمة الهدف للسمة.</span><span class="sxs-lookup"><span data-stu-id="4e3ee-129">The target value for the attribute.</span></span> <span data-ttu-id="4e3ee-130">هذه القيمة هي القيمة المثلى للسمة، ويتم تطبيقها على كافة أنواع السمات.</span><span class="sxs-lookup"><span data-stu-id="4e3ee-130">This value is the optimal value of the attribute, and it applies to all attribute types.</span></span>

<span data-ttu-id="4e3ee-131">يمكنك الوصول إلى صفحات المنتجات التي تحددها في صفحة **المنتجات التي تم إصدارها** في إدارة معلومات المنتج.</span><span class="sxs-lookup"><span data-stu-id="4e3ee-131">You can access the pages for products that you select on the **Released products** page in Product information management.</span></span> <span data-ttu-id="4e3ee-132">وبعد تعيين المواصفات التشغيلية لمنتج، يمكنك إضافة قيم معينة إلى السمات في صفحة **المواصفات التشغيلية للمخزون**.</span><span class="sxs-lookup"><span data-stu-id="4e3ee-132">After you assign batch attributes to a product, you can add specific values to the attributes on the **Inventory batch attributes** page.</span></span>

## <a name="reserve-batches"></a><span data-ttu-id="4e3ee-133">حجز الدُفعات</span><span class="sxs-lookup"><span data-stu-id="4e3ee-133">Reserve batches</span></span>
<span data-ttu-id="4e3ee-134">يمكنك البحث في المواصفات التشغيلية عند قيامك بإجراء عمليات حجر الدُفعات لأمر مبيعات لتنفيذ أمر عميل أو عند انتقاء وحجز الدُعات لأمر إنتاج.</span><span class="sxs-lookup"><span data-stu-id="4e3ee-134">You can search on batch attributes when you do batch reservations for a sales order to fullfill a customer's order, or when you pick and reserve batches for a production order.</span></span> <span data-ttu-id="4e3ee-135">ويساعد البحث في تحديد موقع دُفعة مخزون الذي يحتوي على المنتج الذي يحتوي على المواصفة التشغيلية التي تريدها.</span><span class="sxs-lookup"><span data-stu-id="4e3ee-135">The search helps locate an inventory batch that contains the product that has the batch attribute that you want.</span></span> <span data-ttu-id="4e3ee-136">وبعد تحديد موقع الدُفعة أو الدُفعات، يمكنك حجز المنتج لبند حركة المخزون الأصلي.</span><span class="sxs-lookup"><span data-stu-id="4e3ee-136">After you locate the batch or batches, you can reserve the product to the originating inventory transaction line.</span></span>




