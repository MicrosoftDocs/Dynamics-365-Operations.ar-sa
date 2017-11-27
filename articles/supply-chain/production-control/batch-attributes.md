---
title: "مواصفات التشغيلة"
description: "يوفر هذا الموضوع معلومات حول مواصفات التشغيلة. مواصفات التشغيلة هي الصفات المميزة للمواد الخام والمنتجات التامة الصنع والتي تشكل مجموعات المخزون. يوضح الموضوع أيضًا كيفية تعيين مواصفات التشغيلة، وكيف يمكنك البحث فيها عند حجز الدُفعات."
author: YuyuScheller
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PdsBatchAttrib, PdsBatchAttribAssociate, PdsBatchAttribByAttribGroup, PdsBatchAttribByItem, PdsBatchAttribByitemCustomer, PdsBatchAttribGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19271
ms.assetid: 41de0250-4a96-412e-a412-aa06615b6b1d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6c18b007a72686b1ede69b750e930d72e86f0aba
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="batch-attributes"></a><span data-ttu-id="c4d38-105">مواصفات التشغيلة</span><span class="sxs-lookup"><span data-stu-id="c4d38-105">Batch attributes</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c4d38-106">يوفر هذا الموضوع معلومات حول مواصفات التشغيلة.</span><span class="sxs-lookup"><span data-stu-id="c4d38-106">This topic provides information about batch attributes.</span></span> <span data-ttu-id="c4d38-107">مواصفات التشغيلة هي الصفات المميزة للمواد الخام والمنتجات التامة الصنع والتي تشكل مجموعات المخزون.</span><span class="sxs-lookup"><span data-stu-id="c4d38-107">Batch attributes are characteristics of raw materials and finished products that make up inventory batches.</span></span> <span data-ttu-id="c4d38-108">يوضح الموضوع أيضًا كيفية تعيين مواصفات التشغيلة، وكيف يمكنك البحث فيها عند حجز الدُفعات.</span><span class="sxs-lookup"><span data-stu-id="c4d38-108">The topic also explains how to assign batch attributes, and how you can search on them when you reserve batches.</span></span>

<span data-ttu-id="c4d38-109">مواصفات التشغيلة هي الصفات المميزة للمواد الخام والمنتجات التامة الصنع والتي تشكل مجموعات المخزون.</span><span class="sxs-lookup"><span data-stu-id="c4d38-109">Batch attributes are characteristics of raw materials and finished products that make up inventory batches.</span></span> <span data-ttu-id="c4d38-110">ويمكن أن تختلف مواصفات التشغيلة، تبعاً لعوامل مثل الظروف البيئية، أو جودة المواد الخام التي تُستخدم لإنتاج الدُفعة، أو نتيجة المنتج النهائي.</span><span class="sxs-lookup"><span data-stu-id="c4d38-110">Batch attributes can vary, depending on factors such as environmental conditions, the quality of the raw materials that are used to produce the batch, or the outcome of the finished product.</span></span> <span data-ttu-id="c4d38-111">عدد وأنواع مواصفات التشغيلة المستخدمة يمكن أن تتفاوت تفاوتاً كبيرًا من صناعة إلى أخرى.</span><span class="sxs-lookup"><span data-stu-id="c4d38-111">The number and types of batch attributes that are used can vary widely from one industry to another.</span></span> <span data-ttu-id="c4d38-112">فيما يلي مثالين يوضحان كيفية استخدام مواصفات التشغيلة:</span><span class="sxs-lookup"><span data-stu-id="c4d38-112">Here are two examples that show how to use batch attributes:</span></span>

-   <span data-ttu-id="c4d38-113">في صناعة الجبن، يمكن أن يشتمل اللبن، وهو من المواد الخام التي تُستخدم لإنتاج الجبن، على سمات مثل وزن محتوى الدهون والوزن بالنسبة المئوية.</span><span class="sxs-lookup"><span data-stu-id="c4d38-113">In the cheese industry, milk, which is one of the raw materials that are used to produce the cheese, can have attributes such as fat content and percentage weight.</span></span> <span data-ttu-id="c4d38-114">ويمكن أن يشتمل الجبن الذي تم إنتاجه من الحليب سمات أخرى، مثل الرطوبة والعمر.</span><span class="sxs-lookup"><span data-stu-id="c4d38-114">The cheese that is produced from the milk can have other attributes, such as moisture and age.</span></span>
-   <span data-ttu-id="c4d38-115">وفي صناعة الصلب، قد يشمل الحديد سمات مثل النسب المئوية لمحتوى الماغنسيوم، ومحتوى الفضة، ومحتوى الزنك.</span><span class="sxs-lookup"><span data-stu-id="c4d38-115">In the steel industry, the iron that is produced might have attributes such as the percentages of magnesium content, silver content, and zinc content.</span></span>

<span data-ttu-id="c4d38-116">ولإدارة عدد وأنواع السمات بشكل أفضل، يمكنك استخدام مجموعات مواصفات التشغيلة.</span><span class="sxs-lookup"><span data-stu-id="c4d38-116">To better manage the number and types of attributes, you can use batch attribute groups.</span></span> <span data-ttu-id="c4d38-117">وبهذه الطريقة، لا يلزمك إضافة كل سمة على حدة.</span><span class="sxs-lookup"><span data-stu-id="c4d38-117">In this way, you don't have to add each attribute individually.</span></span>

## <a name="assign-batch-attributes"></a><span data-ttu-id="c4d38-118">تعيين المواصفات التشغيلة</span><span class="sxs-lookup"><span data-stu-id="c4d38-118">Assign batch attributes</span></span>
<span data-ttu-id="c4d38-119">يمكنك تعيين مواصفات التشغيلة للمنتجات الفردية التي يُحتفظ يها في دُفعات المخزون، أو يمكنك تعيينها للمنتجات المرتبطة بعملاء معينين.</span><span class="sxs-lookup"><span data-stu-id="c4d38-119">You can assign batch attributes to individual products that are held in inventory batches, or you can assign them to products that are associated with specific customers.</span></span> <span data-ttu-id="c4d38-120">وقبل تعيين مواصفة تشغيلة على مستوى العميل، يجب تعيينها على مستوى المنتج.</span><span class="sxs-lookup"><span data-stu-id="c4d38-120">Before you can assign a batch attribute at the customer level, you must assign it at the product level.</span></span> <span data-ttu-id="c4d38-121">يجب تعيين المنتج على مجموعة أبعاد الدُفعة إلى **نشطة** في مجموعة أبعاد التعقب.</span><span class="sxs-lookup"><span data-stu-id="c4d38-121">The product must have the batch dimension set to **Active** in the tracking dimension group.</span></span> <span data-ttu-id="c4d38-122">ولتعيين مواصفة تشغيلة لمنتج واحد، استخدم الصفحة الخاصة بالمنتج.</span><span class="sxs-lookup"><span data-stu-id="c4d38-122">To assign a batch attribute to an individual product, use the product-specific page.</span></span> <span data-ttu-id="c4d38-123">وإذا كانت السمة خاصة بمنتج عميل، استخدم الصفحة الخاصة بالعميل.</span><span class="sxs-lookup"><span data-stu-id="c4d38-123">If the attribute is specific to a product for a customer, use the customer-specific page.</span></span> <span data-ttu-id="c4d38-124">وعند إضافة سمة إلى منتج، يمكنك أيضًا تحديد معلمات أخرى.</span><span class="sxs-lookup"><span data-stu-id="c4d38-124">When you add an attribute to a product, you also define other parameters.</span></span> <span data-ttu-id="c4d38-125">فيما يلي بعض الأمثلة:</span><span class="sxs-lookup"><span data-stu-id="c4d38-125">Here are some examples:</span></span>

-   <span data-ttu-id="c4d38-126">الحد الأدنى والحد الأقصى للسمة من نوع **العدد الصحيح** أو **الكسر**.</span><span class="sxs-lookup"><span data-stu-id="c4d38-126">The minimum and maximum ranges for an attribute of the **Integer** or **Fraction** type.</span></span>
-   <span data-ttu-id="c4d38-127">‏‫إجراءات التفاوت للسمة من نوع **العدد الصحيح** أو **الكسر‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="c4d38-127">The tolerance actions for an attribute of the **Integer** or **Fraction** type.</span></span> <span data-ttu-id="c4d38-128">إذا كانت قيمة السمة تقع خارج نطاق الحد الأدنى والحد الأقصى، يمكن أن يكون الإجراء إما رسالة تحذير أو رسالة خطأ.‬</span><span class="sxs-lookup"><span data-stu-id="c4d38-128">If the value of the attribute falls outside the minimum and maximum range, the action can be either a warning message or an error message.</span></span>
-   <span data-ttu-id="c4d38-129">القيمة الهدف للسمة.</span><span class="sxs-lookup"><span data-stu-id="c4d38-129">The target value for the attribute.</span></span> <span data-ttu-id="c4d38-130">هذه القيمة هي القيمة المثلى للسمة، ويتم تطبيقها على كافة أنواع السمات.</span><span class="sxs-lookup"><span data-stu-id="c4d38-130">This value is the optimal value of the attribute, and it applies to all attribute types.</span></span>

<span data-ttu-id="c4d38-131">يمكنك الوصول إلى صفحات المنتجات التي تحددها في صفحة **المنتجات التي تم إصدارها** في إدارة معلومات المنتج.</span><span class="sxs-lookup"><span data-stu-id="c4d38-131">You can access the pages for products that you select on the **Released products** page in Product information management.</span></span> <span data-ttu-id="c4d38-132">وبعد تعيين مواصفات التشغيلة لمنتج، يمكنك إضافة قيم معينة إلى السمات في صفحة **مواصفات التشغيلة للمخزون**.</span><span class="sxs-lookup"><span data-stu-id="c4d38-132">After you assign batch attributes to a product, you can add specific values to the attributes on the **Inventory batch attributes** page.</span></span>

## <a name="reserve-batches"></a><span data-ttu-id="c4d38-133">حجز الدُفعات</span><span class="sxs-lookup"><span data-stu-id="c4d38-133">Reserve batches</span></span>
<span data-ttu-id="c4d38-134">يمكنك البحث في مواصفات التشغيلة عند قيامك بإجراء عمليات حجر الدُفعات لأمر مبيعات لتنفيذ أمر عميل أو عند انتقاء وحجز الدُفعات لأمر إنتاج.</span><span class="sxs-lookup"><span data-stu-id="c4d38-134">You can search on batch attributes when you do batch reservations for a sales order to fulfill a customer's order, or when you pick and reserve batches for a production order.</span></span> <span data-ttu-id="c4d38-135">ويساعد البحث في تحديد موقع دُفعة المخزون التي تحتوي على المنتج الذي يحتوي على مواصفة التشغيلة التي تريدها.</span><span class="sxs-lookup"><span data-stu-id="c4d38-135">The search helps locate an inventory batch that contains the product that has the batch attribute that you want.</span></span> <span data-ttu-id="c4d38-136">وبعد تحديد موقع الدُفعة أو الدُفعات، يمكنك حجز المنتج لبند حركة المخزون الأصلي.</span><span class="sxs-lookup"><span data-stu-id="c4d38-136">After you locate the batch or batches, you can reserve the product to the originating inventory transaction line.</span></span>




