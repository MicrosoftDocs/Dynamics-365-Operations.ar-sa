---
title: "موازنة الدفعات"
description: "يصف هذا الموضوع عملية موازنة الدفعات."
author: johanhoffmann
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 63b986f9f3a1505dba4c2f64f872b9472e1aca87
ms.contentlocale: ar-sa
ms.lasthandoff: 08/07/2018

---

# <a name="batch-balancing"></a><span data-ttu-id="01e47-103">موازنة الدفعات</span><span class="sxs-lookup"><span data-stu-id="01e47-103">Batch balancing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="01e47-104">يصف هذا الموضوع كيفية دعم عملية موازنة الدفعات.</span><span class="sxs-lookup"><span data-stu-id="01e47-104">This topic describes how the batch balancing process is supported.</span></span> 

<span data-ttu-id="01e47-105">شاهد [فيديو حول موازنة الدُفعات في Microsoft Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=4SNLWsU9KyI&feature=youtu.be).</span><span class="sxs-lookup"><span data-stu-id="01e47-105">Watch a [video on batch balancing in Microsoft Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=4SNLWsU9KyI&feature=youtu.be).</span></span>

<span data-ttu-id="01e47-106">في عملية موازنة الدفعات، يتم حساب قيمة المكونات المطلوب استخدامها في إحدى دفعات الإنتاج من تركيز المكونات النشطة في دُفعات المنتجات المُحددة.</span><span class="sxs-lookup"><span data-stu-id="01e47-106">In the batch balancing process, the amount of ingredients to use in a production batch is calculated from the concentration of active ingredients in selected product batches.</span></span>

<a name="products-that-have-an-active-ingredient"></a><span data-ttu-id="01e47-107">المنتجات التي يكون لها مكونًا نشطًا</span><span class="sxs-lookup"><span data-stu-id="01e47-107">Products that have an active ingredient</span></span>
---------------------------------------

<span data-ttu-id="01e47-108">يُمكن تعريف المنتج من خلال تركيزه لمكون نشط.</span><span class="sxs-lookup"><span data-stu-id="01e47-108">A product can be defined by its concentration of an active ingredient.</span></span> <span data-ttu-id="01e47-109">تمت نمذجة المكون النشط لمنتج باستخدام مواصفات تشغيلية خاصة بالمنتج لها قيمة حد أدني وحد أقصى ومستوى مستهدف.</span><span class="sxs-lookup"><span data-stu-id="01e47-109">The active ingredient of a product is modeled by using a product-specific batch attribute that has a minimum value, a maximum value, and a target level.</span></span>

<span data-ttu-id="01e47-110">يمثل المستوى المستخدف للمواصفات التشغيلية النسبة التقديرية لمكون نشط في أحد المنتجات.</span><span class="sxs-lookup"><span data-stu-id="01e47-110">The target level of a batch attribute represents the estimated percentage of an active ingredient in a product.</span></span> <span data-ttu-id="01e47-111">تمثل قيم الحد الأدنى والحد الأقصى الانحراف المقبول عن المستوى المستهدف.</span><span class="sxs-lookup"><span data-stu-id="01e47-111">The minimum and maximum values represent the accepted deviation from the target level.</span></span> <span data-ttu-id="01e47-112">ويمكن استخدامها، على سبيل المثال، كتفاوت مقبول للدفعات في ايصال استلام المنتجات.</span><span class="sxs-lookup"><span data-stu-id="01e47-112">They can be used, for example, as an accepted tolerance for batches at product receipt.</span></span>

<span data-ttu-id="01e47-113">يمكن أن يحتوي المنتج مكون نشط واحد.</span><span class="sxs-lookup"><span data-stu-id="01e47-113">A product can have only one active ingredient.</span></span> <span data-ttu-id="01e47-114">لتحديد المكون النشط لأحد المنتجات، يجب عليك أولًا تحديد المواصفات التشغيلية الخاصة بالمنتج.</span><span class="sxs-lookup"><span data-stu-id="01e47-114">To specify the active ingredient of a product, you must first define a product-specific batch attribute.</span></span> <span data-ttu-id="01e47-115">يمكنك بعد ذلك إقران السمة كسمة أساسية للمنتج.</span><span class="sxs-lookup"><span data-stu-id="01e47-115">You then associate the attribute as a base attribute of the product.</span></span>

<span data-ttu-id="01e47-116">على مستوى المنتج، يجب علي أيضًا تحديد كيف يتم تسجيل مستوى المكون النشط لدفعة المنتج: كجزء من عملية استلام المشتريات أو كجزء من عملية أمر الجودة.</span><span class="sxs-lookup"><span data-stu-id="01e47-116">On the product level, you must also specify how the level of the active ingredient for a batch of the product should be recorded: as part of the purchase receipt process or as part of a quality order process.</span></span>

<span data-ttu-id="01e47-117">لإقران سمة أساسية بأحد المنتجات، يلزم الإعداد التالي:</span><span class="sxs-lookup"><span data-stu-id="01e47-117">To associate a base attribute with a product, the following setup is required:</span></span>

-   <span data-ttu-id="01e47-118">يجب أن يكون المنتج يتم التحكم فيه بواسطة الدفعة.</span><span class="sxs-lookup"><span data-stu-id="01e47-118">The product must be batch-controlled.</span></span> <span data-ttu-id="01e47-119">لجعل أحد المنتجات تتحكم فيه الدفعة، يجب عليك تعيين مجموعة أبعاد تعقب لمنتج له بعد دفعة نشط.</span><span class="sxs-lookup"><span data-stu-id="01e47-119">To make a product batch-controlled, you must assign a tracking dimension group to the product that has an active Batch dimension.</span></span>

-   <span data-ttu-id="01e47-120">يجب تعريف السمة التي تشير إلى مستويات المكونات كمواصفات تشغيلية خاصة بالمنتج للمنتج.</span><span class="sxs-lookup"><span data-stu-id="01e47-120">The attribute that indicates the ingredient levels must be defined as a product-specific batch attribute for the product.</span></span>

<span data-ttu-id="01e47-121">يمكنك البحث عن وتحرير القيمة الفعلية للمكون النشط لدفعة في صفحة **المواصفات التشغيلة للمخزون**.</span><span class="sxs-lookup"><span data-stu-id="01e47-121">You can look up and edit the actual value of the active ingredient for a batch on the **Inventory batch attributes** page.</span></span> 

-  <span data-ttu-id="01e47-122">حدد **إدارة المخزون** \> **الاستعلامات والتقارير** \> **أبعاد التعقب** \> **الدفعات** \> **المواصفات التشغيلية للمخزون**.</span><span class="sxs-lookup"><span data-stu-id="01e47-122">Select **Inventory management** \> **Inquiries and reports** \> **Tracking dimensions** \> **Batches** \> **Inventory batch attributes**.</span></span>

<a name="ingredient-types-and-how-they-interact-in-the-batch-balancing-process"></a><span data-ttu-id="01e47-123">أنوع المكون وكيف تتفاعل في عملية موازنة الدفعة</span><span class="sxs-lookup"><span data-stu-id="01e47-123">Ingredient types and how they interact in the batch balancing process</span></span>
---------------------------------------------------------------------

<span data-ttu-id="01e47-124">يمكن أن يكون سطر المعادلة التي يتم إنشاؤها أحد أنواع هذه المكونات:</span><span class="sxs-lookup"><span data-stu-id="01e47-124">A formula line that is created can have one of these ingredient types:</span></span>

-   <span data-ttu-id="01e47-125">بلا</span><span class="sxs-lookup"><span data-stu-id="01e47-125">None</span></span>

-   <span data-ttu-id="01e47-126">نشط</span><span class="sxs-lookup"><span data-stu-id="01e47-126">Active</span></span>

-   <span data-ttu-id="01e47-127">التعويض</span><span class="sxs-lookup"><span data-stu-id="01e47-127">Compensating</span></span>

-   <span data-ttu-id="01e47-128">تزويدي</span><span class="sxs-lookup"><span data-stu-id="01e47-128">Filler</span></span>

<span data-ttu-id="01e47-129">يقدم بقية القسم أمثلة توضح كيفية عمل نوع كل مكون.</span><span class="sxs-lookup"><span data-stu-id="01e47-129">The rest of this section provides examples that show how each ingredient type works.</span></span> <span data-ttu-id="01e47-130">تستند الأمثلة إلى المعادلة التالية التي لها حجم دفعة إجمالي 100 لتر.</span><span class="sxs-lookup"><span data-stu-id="01e47-130">The examples are based on the following formula that has a total batch size of 100 liters.</span></span>

| <span data-ttu-id="01e47-131">**نوع المكوّن**</span><span class="sxs-lookup"><span data-stu-id="01e47-131">**Ingredient type**</span></span> | <span data-ttu-id="01e47-132">**رقم العنصر**</span><span class="sxs-lookup"><span data-stu-id="01e47-132">**Item number**</span></span> | <span data-ttu-id="01e47-133">**كمية سطر المُعادلة**</span><span class="sxs-lookup"><span data-stu-id="01e47-133">**Formula line quantity**</span></span> | <span data-ttu-id="01e47-134">**الوحدة**</span><span class="sxs-lookup"><span data-stu-id="01e47-134">**Unit**</span></span> |
|---------------------|-----------------|---------------------------|----------|
| <span data-ttu-id="01e47-135">بلا</span><span class="sxs-lookup"><span data-stu-id="01e47-135">None</span></span>                | <span data-ttu-id="01e47-136">و</span><span class="sxs-lookup"><span data-stu-id="01e47-136">A</span></span>               | <span data-ttu-id="01e47-137">20</span><span class="sxs-lookup"><span data-stu-id="01e47-137">20</span></span>                        | <span data-ttu-id="01e47-138">لتر</span><span class="sxs-lookup"><span data-stu-id="01e47-138">Liter</span></span>    |
| <span data-ttu-id="01e47-139">نشط</span><span class="sxs-lookup"><span data-stu-id="01e47-139">Active</span></span>              | <span data-ttu-id="01e47-140">ع</span><span class="sxs-lookup"><span data-stu-id="01e47-140">B</span></span>               | <span data-ttu-id="01e47-141">30</span><span class="sxs-lookup"><span data-stu-id="01e47-141">30</span></span>                        | <span data-ttu-id="01e47-142">لتر</span><span class="sxs-lookup"><span data-stu-id="01e47-142">Liter</span></span>    |
| <span data-ttu-id="01e47-143">التعويض</span><span class="sxs-lookup"><span data-stu-id="01e47-143">Compensating</span></span>        | <span data-ttu-id="01e47-144">ش</span><span class="sxs-lookup"><span data-stu-id="01e47-144">C</span></span>               | <span data-ttu-id="01e47-145">10</span><span class="sxs-lookup"><span data-stu-id="01e47-145">10</span></span>                        | <span data-ttu-id="01e47-146">لتر</span><span class="sxs-lookup"><span data-stu-id="01e47-146">Liter</span></span>    |
| <span data-ttu-id="01e47-147">تزويدي</span><span class="sxs-lookup"><span data-stu-id="01e47-147">Filler</span></span>              | <span data-ttu-id="01e47-148">ق</span><span class="sxs-lookup"><span data-stu-id="01e47-148">D</span></span>               | <span data-ttu-id="01e47-149">40</span><span class="sxs-lookup"><span data-stu-id="01e47-149">40</span></span>                        | <span data-ttu-id="01e47-150">لتر</span><span class="sxs-lookup"><span data-stu-id="01e47-150">Liter</span></span>    |

### <a name="active"></a><span data-ttu-id="01e47-151">نشط</span><span class="sxs-lookup"><span data-stu-id="01e47-151">Active</span></span>

<span data-ttu-id="01e47-152">عندما تتم إضافة منتج له سمة أساسية إلى بند المعادلة،فمن ثم يُشار إليها بـ *المكون النشط* للمُعادلة.</span><span class="sxs-lookup"><span data-stu-id="01e47-152">When a product that has a base attribute is added to a formula line, it's referred to as an *active ingredient* of the formula.</span></span> <span data-ttu-id="01e47-153">يمكن استخدام أوامر الدفعات التي تحتوي على مكونات نشطة لعملية موازنة الدفعات.</span><span class="sxs-lookup"><span data-stu-id="01e47-153">Batch orders that have formulas that include active ingredients can be used for the batch balancing process.</span></span> <span data-ttu-id="01e47-154">لكل مكون في المعادلة، تُقدر عملية موازنة الدفعات المبلغ المطلوب لإصدار المنتج.</span><span class="sxs-lookup"><span data-stu-id="01e47-154">For each ingredient in the formula, the batch balancing process estimates the amount that is required to produce the product.</span></span> <span data-ttu-id="01e47-155">يستند تقدير المبالغ على تركيز المكونات النشطة في الدفعات المحددة.</span><span class="sxs-lookup"><span data-stu-id="01e47-155">The estimate of amounts is based on the concentration of active ingredients in the selected batches.</span></span>

<span data-ttu-id="01e47-156">**مثال**</span><span class="sxs-lookup"><span data-stu-id="01e47-156">**Example**</span></span>

<span data-ttu-id="01e47-157">يمتلك مكون ب السمة الأساسية X ومستوى مستهدف 30، وتم تضمينها في مُعادلة تتطلب 30 لتر من المكون ب لكل 100 لتر من المنتج.</span><span class="sxs-lookup"><span data-stu-id="01e47-157">Ingredient B has base attribute X and a target level of 30, and it's included in a formula that requires 30 liters of ingredient B for every 100 liters of the product.</span></span> <span data-ttu-id="01e47-158">يتم إنشاء أمر دفعة أ يحتوي على حجم دفعة 100 لتر.</span><span class="sxs-lookup"><span data-stu-id="01e47-158">A batch order is created that has a batch size of 100 liters.</span></span> <span data-ttu-id="01e47-159">تم بدء تشغيل أمر الدفعة، وخلال عملية موازنة الدفعة، حدد المستخدم دفعة للمكون ب يوجد به مستوى قوة 35.</span><span class="sxs-lookup"><span data-stu-id="01e47-159">The batch order is started, and during the batch balancing process, the user selects a batch of ingredient B that has a potency level of 35.</span></span> <span data-ttu-id="01e47-160">نظرًا لأن مستوى القوة 35 أعلى من المستوى المستهدف 30، يتم تخفيض الكمية الموزونة من المكون ب باستخدام نسبة قيمة القوة إلى المستوى المستهدف للدفعة، والتي يتم ضربها في الكمية المُقدرة.</span><span class="sxs-lookup"><span data-stu-id="01e47-160">Because the potency level of 35 is higher than the target level of 30, the balanced quantity of ingredient B is reduced by using the ratio of the potency value to the target level of the batch, which is multiplied by the estimated quantity.</span></span> <span data-ttu-id="01e47-161">يبدو حساب الكمية الموزونة على النحو التالي:</span><span class="sxs-lookup"><span data-stu-id="01e47-161">The calculation of the balanced quantity looks like this:</span></span>

<span data-ttu-id="01e47-162">(30 ÷ 35) × 30 لتر = 25.71 لتر</span><span class="sxs-lookup"><span data-stu-id="01e47-162">(30 ÷ 35) × 30 liters = 25.71 liters</span></span>

| <span data-ttu-id="01e47-163">**رقم العنصر**</span><span class="sxs-lookup"><span data-stu-id="01e47-163">**Item number**</span></span> | <span data-ttu-id="01e47-164">**نوع المكوّن**</span><span class="sxs-lookup"><span data-stu-id="01e47-164">**Ingredient type**</span></span> | <span data-ttu-id="01e47-165">**الكمية المقدّرة**</span><span class="sxs-lookup"><span data-stu-id="01e47-165">**Estimated quantity**</span></span> | <span data-ttu-id="01e47-166">**الكمية الموزونة**</span><span class="sxs-lookup"><span data-stu-id="01e47-166">**Balanced quantity**</span></span> | <span data-ttu-id="01e47-167">**الكمية النشطة**</span><span class="sxs-lookup"><span data-stu-id="01e47-167">**Active quantity**</span></span> | <span data-ttu-id="01e47-168">**الوحدة**</span><span class="sxs-lookup"><span data-stu-id="01e47-168">**Unit**</span></span> | <span data-ttu-id="01e47-169">**القيمة الأساسية**</span><span class="sxs-lookup"><span data-stu-id="01e47-169">**Base value**</span></span> |
|-----------------|---------------------|------------------------|-----------------------|---------------------|----------|----------------|
| <span data-ttu-id="01e47-170">و</span><span class="sxs-lookup"><span data-stu-id="01e47-170">A</span></span>               | <span data-ttu-id="01e47-171">بلا</span><span class="sxs-lookup"><span data-stu-id="01e47-171">None</span></span>                | <span data-ttu-id="01e47-172">20</span><span class="sxs-lookup"><span data-stu-id="01e47-172">20</span></span>                     | <span data-ttu-id="01e47-173">20</span><span class="sxs-lookup"><span data-stu-id="01e47-173">20</span></span>                    |                     | <span data-ttu-id="01e47-174">لتر</span><span class="sxs-lookup"><span data-stu-id="01e47-174">Liter</span></span>    |                |
| <span data-ttu-id="01e47-175">ع</span><span class="sxs-lookup"><span data-stu-id="01e47-175">B</span></span>               | <span data-ttu-id="01e47-176">نشط</span><span class="sxs-lookup"><span data-stu-id="01e47-176">Active</span></span>              | <span data-ttu-id="01e47-177">30</span><span class="sxs-lookup"><span data-stu-id="01e47-177">30</span></span>                     | <span data-ttu-id="01e47-178">25.71</span><span class="sxs-lookup"><span data-stu-id="01e47-178">25.71</span></span>                 | <span data-ttu-id="01e47-179">9.00</span><span class="sxs-lookup"><span data-stu-id="01e47-179">9.00</span></span>                | <span data-ttu-id="01e47-180">لتر</span><span class="sxs-lookup"><span data-stu-id="01e47-180">Liter</span></span>    | <span data-ttu-id="01e47-181">30.00</span><span class="sxs-lookup"><span data-stu-id="01e47-181">30.00</span></span>          |
| <span data-ttu-id="01e47-182">ش</span><span class="sxs-lookup"><span data-stu-id="01e47-182">C</span></span>               | <span data-ttu-id="01e47-183">التعويض</span><span class="sxs-lookup"><span data-stu-id="01e47-183">Compensating</span></span>        | <span data-ttu-id="01e47-184">10</span><span class="sxs-lookup"><span data-stu-id="01e47-184">10</span></span>                     | <span data-ttu-id="01e47-185">14.72</span><span class="sxs-lookup"><span data-stu-id="01e47-185">14.72</span></span>                 |                     | <span data-ttu-id="01e47-186">لتر</span><span class="sxs-lookup"><span data-stu-id="01e47-186">Liter</span></span>    |                |
| <span data-ttu-id="01e47-187">ق</span><span class="sxs-lookup"><span data-stu-id="01e47-187">D</span></span>               | <span data-ttu-id="01e47-188">تزويدي</span><span class="sxs-lookup"><span data-stu-id="01e47-188">Filler</span></span>              | <span data-ttu-id="01e47-189">40</span><span class="sxs-lookup"><span data-stu-id="01e47-189">40</span></span>                     | <span data-ttu-id="01e47-190">39.57</span><span class="sxs-lookup"><span data-stu-id="01e47-190">39.57</span></span>                 |                     | <span data-ttu-id="01e47-191">لتر</span><span class="sxs-lookup"><span data-stu-id="01e47-191">Liter</span></span>    |                |

### <a name="none"></a><span data-ttu-id="01e47-192">بلا</span><span class="sxs-lookup"><span data-stu-id="01e47-192">None</span></span>

<span data-ttu-id="01e47-193">عندما تقوم بتطبيق عملية موازنة الدفعة عندما يكون نوع المكون هو **بلا**، تكون الكمية المقدرة والكمية الموزونة لبند المُعادلة في أمر الدفعة مماثلة.</span><span class="sxs-lookup"><span data-stu-id="01e47-193">When you apply the batch balancing process when the ingredient type is **None**, the estimated quantity and the balanced quantity of the formula line in the batch order are the same.</span></span>

<span data-ttu-id="01e47-194">**مثال**</span><span class="sxs-lookup"><span data-stu-id="01e47-194">**Example**</span></span>

<span data-ttu-id="01e47-195">يتم تعيين المكون أ إلى مكون من النوع **بلا** ويُضاف إلى المُعادلة لمنتج نهائي.</span><span class="sxs-lookup"><span data-stu-id="01e47-195">Ingredient A is assigned to an ingredient of the **None** type and added to a formula for a finished product.</span></span> <span data-ttu-id="01e47-196">تتطلب المعادلة 10 لترات من المكون أ لكل 100 لتر من المنتج النهائي.</span><span class="sxs-lookup"><span data-stu-id="01e47-196">The formula requires 10 liters of ingredient A for every 100 liters of the finished product.</span></span> <span data-ttu-id="01e47-197">عندما يتطلب أمر دفعي 200 لتر، يتم حساب كل من الكمية المقدرة والكمية الموزونة للمكون أ على أنها 20 لترًا.</span><span class="sxs-lookup"><span data-stu-id="01e47-197">When a batch order requires 200 liters, both the estimated quantity and the balanced quantity of ingredient A are calculated as 20 liters.</span></span>

### <a name="compensating"></a><span data-ttu-id="01e47-198">التعويض</span><span class="sxs-lookup"><span data-stu-id="01e47-198">Compensating</span></span>

<span data-ttu-id="01e47-199">يمكن إما مقاصة مكون تعويضي أو يكون مكملًا لأثر المكون النشط في أحد المنتجات.</span><span class="sxs-lookup"><span data-stu-id="01e47-199">A compensating ingredient can either offset or complement the effect of the active ingredient in a product.</span></span> <span data-ttu-id="01e47-200">لذلك، تعتمد كمية المكون التعويضي المُستهلك على قوة المنتج:</span><span class="sxs-lookup"><span data-stu-id="01e47-200">Therefore, the quantity of a compensating ingredient that is consumed depends on the potency of the product:</span></span>

-   <span data-ttu-id="01e47-201">**التأثير المتعاكس** -إذا كانت قيمة المكون النشط أكثر من المتوقع، يجب عليك إضافة أقل من المكون التعويضي.</span><span class="sxs-lookup"><span data-stu-id="01e47-201">**Opposing effect** – If the amount of the active ingredient is more than anticipated, you must add less of the compensating ingredient.</span></span>

-   <span data-ttu-id="01e47-202">**التأثير المتمم** -إذا كانت قيمة المكون النشط أقل من المتوقع، يجب عليك إضافة المزيد من المكون التعويضي.</span><span class="sxs-lookup"><span data-stu-id="01e47-202">**Complementary effect** – If the amount of the active ingredient is less than anticipated, you must add more of the compensating ingredient.</span></span>

<span data-ttu-id="01e47-203">تم إعداد العلاقة بين المكون النشط والمكون المتكامل على صفحة **قاعدة التعويض**.</span><span class="sxs-lookup"><span data-stu-id="01e47-203">The relation between an active ingredient and a complementary ingredient is set up on the **Compensating principle** page.</span></span>

<span data-ttu-id="01e47-204">اتبع الخطوات التالية لإعداد العلاقات بين المكونات:</span><span class="sxs-lookup"><span data-stu-id="01e47-204">Follow these steps to set up relations between ingredients.</span></span>

1.  <span data-ttu-id="01e47-205">حدد **إدارة معلومات المنتج** \> **الفواتير والمواد والمعادلات** \> **المعادلات**، ثم قم بفتح سطر المعادلة، ثم حدد **المكونات** لفتح صفحة **قاعدة التعويض**.</span><span class="sxs-lookup"><span data-stu-id="01e47-205">Select **Product information management** \> **Bills and materials and formulas** \> **Formulas**, open a formula line, and then select **Ingredients** to open the **Compensating principle** page.</span></span>

2.  <span data-ttu-id="01e47-206">حدد السطر الذي يمثل قاعدة التعويض، ثم حدد المكون النشط للتعويض.</span><span class="sxs-lookup"><span data-stu-id="01e47-206">Select the line that represents a compensating principle, and then select the active ingredient to compensate.</span></span>

>   <span data-ttu-id="01e47-207">في قاعدة التعويض، تقوم أيضًا بإدخال معامل تعويض سالب أو موجب لتحديد كمية التعويض، وما إذا كان يجب عكس القاعدة أو جعلها متممة.</span><span class="sxs-lookup"><span data-stu-id="01e47-207">In the compensating principle, you also enter a positive or negative compensating factor to specify how much to compensate for, and whether the principle should be opposing or complementary.</span></span> <span data-ttu-id="01e47-208">يشير العامل الموجب إلى التأثير المتمم، ويُشير العامل السالب إلى التأثير المتعاكس.</span><span class="sxs-lookup"><span data-stu-id="01e47-208">A positive factor indicates a complementary effect, and a negative factor indicates an opposing effect.</span></span>

<span data-ttu-id="01e47-209">**مثال**</span><span class="sxs-lookup"><span data-stu-id="01e47-209">**Example**</span></span>

<span data-ttu-id="01e47-210">حالة المكون ب هي مكون نشط يحتوي على سمة أساسية X ومستوى مستهدف 30.</span><span class="sxs-lookup"><span data-stu-id="01e47-210">Ingredient B is an active ingredient that has base attribute X and a target level of 30.</span></span> <span data-ttu-id="01e47-211">تم تضمينها في المعادلة التي تتطلب 30 لتر من المكون ب لكل 100 لتر من المنتج.</span><span class="sxs-lookup"><span data-stu-id="01e47-211">It's included in a formula that requires 30 liters of ingredient B for every 100 liters of the product.</span></span> <span data-ttu-id="01e47-212">يمثل المكون ج مكونًا تعويضيًا، ويتم تضمين كمية 10 لتر في نفس المعادلة.</span><span class="sxs-lookup"><span data-stu-id="01e47-212">Ingredient C is a compensating ingredient, and a quantity of 10 is included in the same formula.</span></span> <span data-ttu-id="01e47-213">تم إعداد معامل تعويض قيمته 1.10 لقاعدة التعويض.</span><span class="sxs-lookup"><span data-stu-id="01e47-213">A compensating factor of 1.10 is set up for the compensating principle.</span></span> <span data-ttu-id="01e47-214">لذلك، سوف يتم تقليل كمية المكون التعويضي بالفرق بين الكمية الموزونة للمكون النشط والكمية المقدرة المطلوبة مضروبة في 1.10.</span><span class="sxs-lookup"><span data-stu-id="01e47-214">Therefore, the balanced quantity of the compensating ingredient will be reduced by the difference between the active ingredient's balanced quantity and the estimated required quantity multiplied by 1.10.</span></span>

<span data-ttu-id="01e47-215">في المثال لنوع المكون **النشط**، تم حساب الكمية الموزونة للمكون النشط المطلوب على أنها 25.71، وتم حساب الكمية المقدرة المطلوبة بـ 30.</span><span class="sxs-lookup"><span data-stu-id="01e47-215">In the example for the **Active** ingredient type, the balanced quantity of the required active ingredient was calculated as 25.71, and the estimated required quantity was calculated as 30.</span></span> <span data-ttu-id="01e47-216">في هذه الحالة، سوف يتم حساب كمية المكون التعويضي المتوازنة على النحو التالي:</span><span class="sxs-lookup"><span data-stu-id="01e47-216">In this case, the balanced quantity of the compensating ingredient will be calculated like this:</span></span>

1.  <span data-ttu-id="01e47-217">يتم تحديد الفرق بين الكمية المُقدرة والموزونة:</span><span class="sxs-lookup"><span data-stu-id="01e47-217">The difference between the estimated and the balanced quantity is determined:</span></span>

>   <span data-ttu-id="01e47-218">25.71 – 30 = –4.29</span><span class="sxs-lookup"><span data-stu-id="01e47-218">25.71 – 30 = –4.29</span></span>

2.  <span data-ttu-id="01e47-219">ثم يتم ضرب النتيجة بعد ذلك في المعامل التعويضي:</span><span class="sxs-lookup"><span data-stu-id="01e47-219">The result is multiplied by the compensating factor:</span></span>

>   <span data-ttu-id="01e47-220">4.29 × 1.10 = –4.72</span><span class="sxs-lookup"><span data-stu-id="01e47-220">4.29 × 1.10 = –4.72</span></span>

3.  <span data-ttu-id="01e47-221">يتم تقليل الكمية التعويضية المُقدرة بنسبة - 4.72 لتحديد الكمية التعويضية الموزونة:</span><span class="sxs-lookup"><span data-stu-id="01e47-221">The estimated compensating quantity is reduced by –4.72 to determine the balanced compensating quantity:</span></span>

>   <span data-ttu-id="01e47-222">10 – (–4.72) = 14.72</span><span class="sxs-lookup"><span data-stu-id="01e47-222">10 – (–4.72) = 14.72</span></span>

<span data-ttu-id="01e47-223">نظرًا لأن 1.10 هو معامل تعويضي موجبه، فسوف يكون لهذه القاعدة التعويضية تأثير متمم.</span><span class="sxs-lookup"><span data-stu-id="01e47-223">Because 1.10 is a positive compensating factor, this compensating principle has a complementary effect.</span></span> <span data-ttu-id="01e47-224">في هذه الحالة، يكون المكون النشط أكثر قوة من المتوقع.</span><span class="sxs-lookup"><span data-stu-id="01e47-224">In this case, the active ingredient is more potent than anticipated.</span></span> <span data-ttu-id="01e47-225">ولذلك، يلزم وجود أكثر من مكون تعويضي.</span><span class="sxs-lookup"><span data-stu-id="01e47-225">Therefore, more of the compensating ingredient is required.</span></span>

### <a name="filler"></a><span data-ttu-id="01e47-226">تزويدي</span><span class="sxs-lookup"><span data-stu-id="01e47-226">Filler</span></span>

<span data-ttu-id="01e47-227">يمثل *المكون التزويدي* مكونًا حياديًا يستخدم للوصول إلى كمية الإخراج المطلوبة للمنتج النهائي.</span><span class="sxs-lookup"><span data-stu-id="01e47-227">A *filler ingredient* is a neutral ingredient that is used to reach the desired output quantity of the finished product.</span></span> <span data-ttu-id="01e47-228">تُحسب التعديلات للكميات التزويدية بناءً على التغييرات في المكون النشط والمكون التعويضي مقارنة بالكمية القياسية.</span><span class="sxs-lookup"><span data-stu-id="01e47-228">Adjustments to filler quantities are calculated based on variations in the active ingredient and the compensating ingredient compared to the standard quantity.</span></span>

<span data-ttu-id="01e47-229">**مثال**</span><span class="sxs-lookup"><span data-stu-id="01e47-229">**Example**</span></span>

<span data-ttu-id="01e47-230">لقد قمت بصياغة منتج يتضمن المكونات أ وب وج لحجم معادلة 100 لتر.</span><span class="sxs-lookup"><span data-stu-id="01e47-230">You've formulated a product that includes ingredients A, B, C, and D for a formula size of 100 liters.</span></span> <span data-ttu-id="01e47-231">ولقد قمت بحساب الكمية الموزونة لجميع أنواع المكونات باسثتناء نوع المكون **التزويدي**المستخدم في بند واحد.</span><span class="sxs-lookup"><span data-stu-id="01e47-231">You've calculated the balanced quantity of all the ingredient types except the **Filler** ingredient type that is used on one line.</span></span>
<span data-ttu-id="01e47-232">يتم حساب الكمية الموزونة للمكون التزويدي بوصفها الفرق بين حجم دفعة 100 لتر ومجموع المكونات أ وب وج:</span><span class="sxs-lookup"><span data-stu-id="01e47-232">The balanced quantity of the filler ingredient is calculated as the difference between the batch size of 100 liters and the sum of ingredients A, B, and C:</span></span>

<span data-ttu-id="01e47-233">100 – (20 + 25.71 + 14.72) = 39.57</span><span class="sxs-lookup"><span data-stu-id="01e47-233">100 – (20 + 25.71 + 14.72) = 39.57</span></span>

<a name="the-batch-balancing-process"></a><span data-ttu-id="01e47-234">عملية موازنة الدفعة</span><span class="sxs-lookup"><span data-stu-id="01e47-234">The batch balancing process</span></span>
---------------------------

<span data-ttu-id="01e47-235">يتم تنفيذ عملية موازنة الدفعات من صفحة **موازنة الدفعات** .</span><span class="sxs-lookup"><span data-stu-id="01e47-235">The batch balancing process is performed from the **Batch balancing** page.</span></span>
<span data-ttu-id="01e47-236">حدد **إدارة التكلفة** \> **أوامر الدفعات**، ثم على علامة تبويب **عملية** ، حدد **موازنة الدفعات**.</span><span class="sxs-lookup"><span data-stu-id="01e47-236">Select **Cost management** \> **Batch orders**, and then, on the **Process** tab, select **Batch balancing**.</span></span> <span data-ttu-id="01e47-237">يتوفر موازنة الدفعات لأوامر الدفعات التي تكون حالتها **تم البدء**.</span><span class="sxs-lookup"><span data-stu-id="01e47-237">Batch balancing is available for batch orders that have a status of **Started**.</span></span>

<span data-ttu-id="01e47-238">بشكل عام، يمكن تطبيق موازنة الدفعات على أوامر الدفعات إذا كان للمُعادلة سطر مُعادلة واحد على الأقل عندما يكون نوع المكون **نشط**.</span><span class="sxs-lookup"><span data-stu-id="01e47-238">In general, batch balancing can be applied to batch orders if the formula has at least one formula line where the ingredient type is **Active**.</span></span> <span data-ttu-id="01e47-239">(ولمعرفة الاستثناءات لهذه القاعدة، راجع "أوامر الدفعات غير المنطبقة على موازنة الدفعات" القسم اللاحق في هذا الموضوع.)</span><span class="sxs-lookup"><span data-stu-id="01e47-239">(For the exception to this rule, see the "Batch orders that aren't applicable for batch balancing" section later in this topic.)</span></span>

<span data-ttu-id="01e47-240">يمكن تقسيم عملية موازنة الدفعات إلى عمليتين فرعيتين:</span><span class="sxs-lookup"><span data-stu-id="01e47-240">The batch balancing process can be divided into two subprocesses:</span></span>

1.  <span data-ttu-id="01e47-241">مكونات دفعات الموازنة</span><span class="sxs-lookup"><span data-stu-id="01e47-241">Balance batch ingredients</span></span>

2.  <span data-ttu-id="01e47-242">تأكيد المُعادلة وتحريرها</span><span class="sxs-lookup"><span data-stu-id="01e47-242">Confirm and release the formula</span></span>

### <a name="balance-batch-ingredients"></a><span data-ttu-id="01e47-243">مكونات دفعات الموازنة</span><span class="sxs-lookup"><span data-stu-id="01e47-243">Balance batch ingredients</span></span>

<span data-ttu-id="01e47-244">في العملية الفرعية لموازنة مكونات الدفعات، يتم حساب مقدار المكونات المطلوب استخدامها لدفعة الإنتاج بناءً على الدُفعات المُحددة التي لها مكونات نشطة.</span><span class="sxs-lookup"><span data-stu-id="01e47-244">In the Balance batch ingredients subprocess, the amount of ingredients to use for the production batch is calculated based on the selected batches that have active ingredients.</span></span> <span data-ttu-id="01e47-245">كقاعدة، يمكن إكمال الحساب فقط إذا كانت هناك تغطية كاملة لكافة المكونات.</span><span class="sxs-lookup"><span data-stu-id="01e47-245">As a rule, the calculation can be completed only if there is full coverage of all ingredients.</span></span> <span data-ttu-id="01e47-246">لا يمكنك موازنة جزء واحد فقط من الدفعة التي يتم تعيين الأمر الدفعي لإنتاجها.</span><span class="sxs-lookup"><span data-stu-id="01e47-246">You can't balance only part of the batch that the batch order is set up to produce.</span></span>

[!NOTE]
<span data-ttu-id="01e47-247">لا يمكنك حفظ عملية حسابية، ثم قم بإتمام عملية موازنة الدفعات لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="01e47-247">You can't save a calculation and then complete the batch balancing process later.</span></span> <span data-ttu-id="01e47-248">إذا قمت بإغلاق صفحة **موازنة الدفعة**، يجب عليك تكرار العملية الحسابية لإتمام العملية.</span><span class="sxs-lookup"><span data-stu-id="01e47-248">If you close the **Batch balancing** page, you must repeat the calculation to complete the process.</span></span>

### <a name="confirm-and-release-the-formula"></a><span data-ttu-id="01e47-249">تأكيد المُعادلة وتحريرها</span><span class="sxs-lookup"><span data-stu-id="01e47-249">Confirm and release the formula</span></span>

<span data-ttu-id="01e47-250">بعد حساب كميات المكون، يمكنك تأكيد المعادلة وإصدارها.</span><span class="sxs-lookup"><span data-stu-id="01e47-250">After the ingredient quantities have been calculated, you can confirm and release the formula.</span></span> <span data-ttu-id="01e47-251">تختلف عملية الإصدار بناءً على ما إذا كانت المنتجات تم تمكينها لعمليات إدارة المستودع.</span><span class="sxs-lookup"><span data-stu-id="01e47-251">The release process differs, depending on whether the products are enabled for the warehouse management processes:</span></span>

-   <span data-ttu-id="01e47-252">إذا تم تمكين منتج لعمليات إدارة المستودعات، فمن ثم يتم إصدار بند المعادلة إلى المستودع طبقًا لقواعد عمليات إدارة المستودعات.</span><span class="sxs-lookup"><span data-stu-id="01e47-252">If a product is enabled for the warehouse management processes, the formula line is released to the warehouse according to the principles for the warehouse management processes.</span></span> <span data-ttu-id="01e47-253">يتم إصدار بند المعادلة في الكميات التي تطابق الكميات الموزونة، وتم إصدارها لدُفعات معينة تم تحديدها للمكونات النشطة.</span><span class="sxs-lookup"><span data-stu-id="01e47-253">The formula line is released in quantities that match the balanced quantities, and it's released for the specific batches that are selected for the active ingredients.</span></span>

> [!NOTE]
>   <span data-ttu-id="01e47-254">يمكن تحرير بنود المعادلة للمستودعات فقط كجزء من عملية موازنة الدفعات.</span><span class="sxs-lookup"><span data-stu-id="01e47-254">Formula lines can be released to warehouse only as part of the batch balancing process.</span></span> <span data-ttu-id="01e47-255">وعلى الرغم من وجود خيارات أخرى لإصدار المواد للإنتاج إلى المستودع، فلا يمكن استخدام هذه الخيارات لبنود المعادلة.</span><span class="sxs-lookup"><span data-stu-id="01e47-255">Although there are other options for releasing materials for production to warehouse, those options can't be used for formula lines.</span></span>

-   <span data-ttu-id="01e47-256">إذا لم يتم تمكين منتج لعمليات إدارة المستوعات، يتم إنشاء قائمة انتقاء الإنتاج للمنتج عندما تقوم بالتأكيد وإصدار المعادلة.</span><span class="sxs-lookup"><span data-stu-id="01e47-256">If a product isn't enabled for the warehouse management processes, a production picking list is created for the product when you confirm and release the formula.</span></span>

<span data-ttu-id="01e47-257">في المعادلة الواحدة، يمكنك تجميع المنتجات التي تم تمكينها لعمليات إدارة المستوعات والمنتجات التي لم يتم تمكينها لعمليات إدارة المستودعات.</span><span class="sxs-lookup"><span data-stu-id="01e47-257">In a single formula, you can combine products that are enabled for the warehouse management processes and products that aren't enabled for the warehouse management processes.</span></span> <span data-ttu-id="01e47-258">عندما يتم تضمين نوعين من المنتجات في معادلة واحدة، يتم إصدار المنتجات التي تم تمكينها لعمليات إدارة المستودعات إلى المستودع.</span><span class="sxs-lookup"><span data-stu-id="01e47-258">When the two types of products are included in one formula, the products that are enabled for the warehouse management processes are released to warehouse.</span></span> <span data-ttu-id="01e47-259">وبالنسبة للمنتجات التي لم يتم تمكينها لعمليات إدارة المستودعات، يتم إنشاء قائمة انتقاء عندما يتم تأكيد المُعادلة وإصدارها.</span><span class="sxs-lookup"><span data-stu-id="01e47-259">For the products that aren't enabled for the warehouse management processes, a picking list is created when the formula is confirmed and released.</span></span>

### <a name="batch-orders-that-arent-applicable-for-batch-balancing"></a><span data-ttu-id="01e47-260">الأوامر الدفعية غير القابلة للتطبيق لموازنة الدفعات</span><span class="sxs-lookup"><span data-stu-id="01e47-260">Batch orders that aren't applicable for batch balancing</span></span>

<span data-ttu-id="01e47-261">يوجد استثناء واحد للقاعدة يمكن فيه تطبيق الأوامر الدفعية لموازنة الدفعات إذا كان المعادلة تحتوي على سطر معادلة واحد على الاقل عندما يون نوع المكون **نشط**</span><span class="sxs-lookup"><span data-stu-id="01e47-261">There is one exception to the rule that batch orders are applicable for batch balancing if the formula has at least one formula line where the ingredient type is **Active**.</span></span>

<span data-ttu-id="01e47-262">إذا كانت هناك معادلة تحتوي على مكون نشط لمنتج تم تمكينه لعمليات إدارة المستودعات، ولكن رقم الدفعة أقل من الموقع في التدرج الهرمي للحجز، فلا ينطبق أمر الدفعة على موازنة الدفعات.</span><span class="sxs-lookup"><span data-stu-id="01e47-262">If a formula contains an active ingredient for a product that is enabled for the warehouse management processes, but Batch number is below Location in the reservation hierarchy, the batch order isn't applicable for batch balancing.</span></span>

<span data-ttu-id="01e47-263">يمر أمر الدفعة غير القابل للتطبيق لموازنة الدفعات في دورة عملية عادية للأوامر الدفعية.</span><span class="sxs-lookup"><span data-stu-id="01e47-263">A batch order that isn't applicable for batch balancing goes through the regular process cycle for batch orders.</span></span>

