---
title: استراتيجية الحلول لتكوين المنتج
description: يوضح هذا الموضوع كيفية استخدام استراتيجية الحلول لتحسين أداء تكوين المنتج.
author: cvocph
manager: AnnBe
ms.date: 02/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCCreateProductConfigurationModel, PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4a548d3536bbc0056ee22c07c464af062029da81
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250566"
---
# <a name="solver-strategy-for-product-configuration"></a><span data-ttu-id="e5fd2-103">استراتيجية الحلول لتكوين المنتج</span><span class="sxs-lookup"><span data-stu-id="e5fd2-103">Solver strategy for product configuration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e5fd2-104">يوضح هذا الموضوع كيفية استخدام استراتيجية الحلول لتحسين أداء تكوين المنتج.</span><span class="sxs-lookup"><span data-stu-id="e5fd2-104">This topic describes how you can use the solver strategy to improve the performance of product configuration.</span></span>

<span data-ttu-id="e5fd2-105">تم تقديم مفهوم استراتيجيات الحلول أولاً في التحديث التراكمي 7 (CU7) لـ Microsoft Dynamics AX 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="e5fd2-105">The concept of solver strategies was first introduced in Cumulative update 7 (CU7) for Microsoft Dynamics AX 2012 R2.</span></span> <span data-ttu-id="e5fd2-106">وتم توسيعه في التحديث التراكمي 8 (CU8) لكل من Microsoft Dynamics AX 2012 R3 وMicrosoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.</span><span class="sxs-lookup"><span data-stu-id="e5fd2-106">It was extended in Cumulative update 8 (CU8) for Microsoft Dynamics AX 2012 R3 and Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.</span></span>

<span data-ttu-id="e5fd2-107">يتكون مفهوم استراتيجية الحلول الآن من الاستراتيجيات التالية:</span><span class="sxs-lookup"><span data-stu-id="e5fd2-107">The solver strategy concept now consists of the following strategies:</span></span>

- <span data-ttu-id="e5fd2-108">الإعداد الافتراضي</span><span class="sxs-lookup"><span data-stu-id="e5fd2-108">Default</span></span>
- <span data-ttu-id="e5fd2-109">أقل المجالات أولاً</span><span class="sxs-lookup"><span data-stu-id="e5fd2-109">Minimal domains first</span></span>
- <span data-ttu-id="e5fd2-110">تنازلي</span><span class="sxs-lookup"><span data-stu-id="e5fd2-110">Top-down</span></span>
- <span data-ttu-id="e5fd2-111">Z3</span><span class="sxs-lookup"><span data-stu-id="e5fd2-111">Z3</span></span>

## <a name="solver-strategy"></a><span data-ttu-id="e5fd2-112">إستراتيجية الحلول</span><span class="sxs-lookup"><span data-stu-id="e5fd2-112">Solver strategy</span></span> 

<span data-ttu-id="e5fd2-113">يمكن صياغة نموذج تكوين منتج كـ [مشكلة تقييد الرضا (CSP)](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf).</span><span class="sxs-lookup"><span data-stu-id="e5fd2-113">A product configuration model can be formulated as a [constraint satisfaction problem (CSP)](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf).</span></span> <span data-ttu-id="e5fd2-114">يوفر Microsoft Solver Foundation ‏(MSF) نوعين من أنواع استراتيجيات الحلول لحل مشكلات CSP التي يمكن استخدامها من نماذج تكوين المنتجات.</span><span class="sxs-lookup"><span data-stu-id="e5fd2-114">Microsoft Solver Foundation (MSF) provides two types of solver strategies to solve the CSPs that can be used from product configuration models.</span></span> <span data-ttu-id="e5fd2-115">تعتمد استراتيجيات الحلول هذه على [الأساليب البحثية](https://techterms.com/definition/heuristic)، التي يتم استخدامها لتحديد الترتيب الذي تتم فيه مراعاة متغيرات مشكلات CSP عندما يتم حل المشكلة.</span><span class="sxs-lookup"><span data-stu-id="e5fd2-115">These solver strategies rely on [heuristics](https://techterms.com/definition/heuristic), which are used to determine the order that the variables of the CSPs are considered in when the problem is being solved.</span></span> <span data-ttu-id="e5fd2-116">يمكن للأساليب البحثية التأثير إلى حد كبير على الأداء عندما يتم حل مشكلة أو فئة من المشكلات.</span><span class="sxs-lookup"><span data-stu-id="e5fd2-116">Heuristics can significantly affect performance when a problem or class of problems is being solved.</span></span>

<span data-ttu-id="e5fd2-117">تحدد استراتيجية الحلول لنماذج تكوين المنتجات أي حل يتم استخدامه باستخدام الأساليب البحثية.</span><span class="sxs-lookup"><span data-stu-id="e5fd2-117">The solver strategy for product configuration models determines which solver is used with heuristics.</span></span> <span data-ttu-id="e5fd2-118">تستخدم استراتيجيات **الافتراضي**، و**أقل المجالات أولاً‬**، و**تنازلي‬** الحلين من MSF، بينما تستخدم استراتيجية **Z3** حل Z3.</span><span class="sxs-lookup"><span data-stu-id="e5fd2-118">The **Default**, **Minimal domains first**, and **Top-down** strategies use the two solvers from MSF, whereas the **Z3** strategy uses the Z3 solver.</span></span> 

<span data-ttu-id="e5fd2-119">أظهرت دراسات تطبيق العميل الحقيقية أن أي تغيير في استراتيجية الحل لنموذج تكوين منتج يمكنه تقليل وقت الاستجابة من دقائق إلى ميلي ثانية.</span><span class="sxs-lookup"><span data-stu-id="e5fd2-119">Real customer implementation studies have shown that a change in the solver strategy for a product configuration model can reduce the response time from minutes to milliseconds.</span></span> <span data-ttu-id="e5fd2-120">لذلك، إنه من المفيد تجربة استراتيجيات حلول مختلفة للبحث عن الاستراتيجية الأكثر كفاءة لنموذج تكوين المنتج.</span><span class="sxs-lookup"><span data-stu-id="e5fd2-120">Therefore, it's worth the effort to try different solver strategies to find the most efficient strategy for your product configuration model.</span></span>

## <a name="change-the-settings-for-the-solver-strategy"></a><span data-ttu-id="e5fd2-121">تغيير الإعدادات لاستراتيجية الحل</span><span class="sxs-lookup"><span data-stu-id="e5fd2-121">Change the settings for the solver strategy</span></span>

<span data-ttu-id="e5fd2-122">لتغيير استراتيجية الحل، في صفحة**نماذج تكوين المنتج**، في "جزء الإجراءات"، حدد **خصائص النموذج**.</span><span class="sxs-lookup"><span data-stu-id="e5fd2-122">To change the solver strategy, on the **Product configuration models** page, on the Action Pane, select **Model properties**.</span></span> <span data-ttu-id="e5fd2-123">بعد ذلك، في مربع الحوار **تحرير تفاصيل النموذج**، حدد استراتيجية حل.</span><span class="sxs-lookup"><span data-stu-id="e5fd2-123">Then, in the **Edit the model details** dialog box, select a solver strategy.</span></span>

<span data-ttu-id="e5fd2-124">[![تغيير استراتيجية الحل](./media/solver-strategy.png)](./media/solver-strategy.png)</span><span class="sxs-lookup"><span data-stu-id="e5fd2-124">[![Changing the solver strategy](./media/solver-strategy.png)](./media/solver-strategy.png)</span></span>

<span data-ttu-id="e5fd2-125">لا يوجد حاليًا منطق يكتشف تلقائيًا استراتيجية الحل التي ستكون الاستراتيجية الأكثر كفاءة لتكوين المنتج المستند إلى قيد.</span><span class="sxs-lookup"><span data-stu-id="e5fd2-125">Currently, there is no logic that automatically detects which solver strategy will be the most efficient strategy for constraint-based product configuration.</span></span> <span data-ttu-id="e5fd2-126">لذلك، يجب عليك تجربة استراتيجيات الحلول واحدة تلو الأخرى.</span><span class="sxs-lookup"><span data-stu-id="e5fd2-126">Therefore, you must try the solver strategies one by one.</span></span>

<span data-ttu-id="e5fd2-127">يوفر الجدول التالي نصائح حول استراتيجية الحل المُراد استخدامها في السيناريوهات المختلفة.</span><span class="sxs-lookup"><span data-stu-id="e5fd2-127">The following table provides recommendations about the solver strategy to use in various scenarios.</span></span>

| <span data-ttu-id="e5fd2-128">إستراتيجية الحلول</span><span class="sxs-lookup"><span data-stu-id="e5fd2-128">Solver strategy</span></span>      | <span data-ttu-id="e5fd2-129">استخدام الاستراتيجية في هذا السيناريو</span><span class="sxs-lookup"><span data-stu-id="e5fd2-129">Use the strategy in this scenario</span></span> |
|----------------------|-----------------------------------|
| <span data-ttu-id="e5fd2-130">الإعداد الافتراضي</span><span class="sxs-lookup"><span data-stu-id="e5fd2-130">Default</span></span>              | <span data-ttu-id="e5fd2-131">تم تحسين الاستراتيجية **الافتراضية** لحل النماذج التي تعتمد على قيود الجداول.</span><span class="sxs-lookup"><span data-stu-id="e5fd2-131">The **Default** strategy has been optimized to solve models that rely on table constraints.</span></span> <span data-ttu-id="e5fd2-132">أظهرت دراسات تطبيق العميل أن هذه الاستراتيجية هي الاستراتيجية الأكثر كفاءة في السيناريوهات حيث يتم استخدام قيود الجداول بصورة مكثفة.</span><span class="sxs-lookup"><span data-stu-id="e5fd2-132">Customer implementation studies have shown that this strategy is the most efficient strategy in scenarios where table constraints are used extensively.</span></span> |
| <span data-ttu-id="e5fd2-133">أقل المجالات أولاً</span><span class="sxs-lookup"><span data-stu-id="e5fd2-133">Minimal domains first</span></span> | <span data-ttu-id="e5fd2-134">الاستراتيجيتان **أقل المجالات أولاً** و**تنازلي** مرتبطتان بشكل كبير.</span><span class="sxs-lookup"><span data-stu-id="e5fd2-134">The **Minimal domains first** and **Top-down** strategies are closely related.</span></span> <span data-ttu-id="e5fd2-135">أظهرت دراسات تطبيق العميل أن استراتيجية **تنازلي** تتفوق على استراتيجية **أقل المجالات أولاً**.</span><span class="sxs-lookup"><span data-stu-id="e5fd2-135">Customer implementation studies have shown that the **Top-down** strategy, outperforms the **Minimal domains first** strategy.</span></span> <span data-ttu-id="e5fd2-136">ومع ذلك، يتم الاحتفاظ باستراتيجية **أقل المجالات أولاً** في المنتج للتوافق مع الإصدارات السابقة.</span><span class="sxs-lookup"><span data-stu-id="e5fd2-136">However, the **Minimal domains first** strategy is kept in the product for backward compatibility.</span></span> <span data-ttu-id="e5fd2-137">ثبت أن كلاًّ من استراتيجيتي الحلول أكثر فعالية عند حل النماذج التي تحتوي على العديد من التعبيرات الرياضية التي لا يتم فيها استخدام أي قيود جداول.</span><span class="sxs-lookup"><span data-stu-id="e5fd2-137">Both these solver strategies have been shown to be more efficient at solving models that contain several arithmetic expressions where no table constraints are used.</span></span> <span data-ttu-id="e5fd2-138">ومع ذلك، في بعض الحالات، تتفوق الاستراتيجية **الافتراضية** على هاتين الاستراتيجيتين.</span><span class="sxs-lookup"><span data-stu-id="e5fd2-138">However, in some cases, the **Default** strategy outperforms these two strategies.</span></span> <span data-ttu-id="e5fd2-139">لذلك، تذكر أن تجرب كل استراتيجية.</span><span class="sxs-lookup"><span data-stu-id="e5fd2-139">Therefore, remember to try each strategy.</span></span> |
| <span data-ttu-id="e5fd2-140">تنازلي</span><span class="sxs-lookup"><span data-stu-id="e5fd2-140">Top-down</span></span>             | <span data-ttu-id="e5fd2-141">الاستراتيجيتان **أقل المجالات أولاً** و**تنازلي** مرتبطتان بشكل كبير.</span><span class="sxs-lookup"><span data-stu-id="e5fd2-141">The **Minimal domains first** and **Top-down** strategies are closely related.</span></span> <span data-ttu-id="e5fd2-142">أظهرت دراسات تطبيق العميل أن استراتيجية **تنازلي** تتفوق على استراتيجية **أقل المجالات أولاً**.</span><span class="sxs-lookup"><span data-stu-id="e5fd2-142">Customer implementation studies have shown that the **Top-down** strategy, outperforms the **Minimal domains first** strategy.</span></span> <span data-ttu-id="e5fd2-143">ومع ذلك، يتم الاحتفاظ باستراتيجية **أقل المجالات أولاً** في المنتج للتوافق مع الإصدارات السابقة.</span><span class="sxs-lookup"><span data-stu-id="e5fd2-143">However, the **Minimal domains first** strategy is kept in the product for backward compatibility.</span></span> <span data-ttu-id="e5fd2-144">ثبت أن كلاًّ من استراتيجيتي الحلول أكثر فعالية عند حل النماذج التي تحتوي على العديد من التعبيرات الرياضية التي لا يتم فيها استخدام أي قيود جداول.</span><span class="sxs-lookup"><span data-stu-id="e5fd2-144">Both these solver strategies have been shown to be more efficient at solving models that contain several arithmetic expressions where no table constraints are used.</span></span> <span data-ttu-id="e5fd2-145">ومع ذلك، في بعض الحالات، تتفوق الاستراتيجية **الافتراضية** على هاتين الاستراتيجيتين.</span><span class="sxs-lookup"><span data-stu-id="e5fd2-145">However, in some cases, the **Default** strategy outperforms these two strategies.</span></span> <span data-ttu-id="e5fd2-146">لذلك، تذكر أن تجرب كل استراتيجية.</span><span class="sxs-lookup"><span data-stu-id="e5fd2-146">Therefore, remember to try each strategy.</span></span> |
| <span data-ttu-id="e5fd2-147">Z3</span><span class="sxs-lookup"><span data-stu-id="e5fd2-147">Z3</span></span>                   | <span data-ttu-id="e5fd2-148">نوصيك باستخدام استراتيجية **Z3** باعتبارها استراتيجية الحل الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="e5fd2-148">We recommend that you use the **Z3** strategy as the default solver strategy.</span></span> <span data-ttu-id="e5fd2-149">إذا كنت مهتمًا بالأداء وإمكانية التوسع، فيمكنك تقييم استراتيجيات أخرى.</span><span class="sxs-lookup"><span data-stu-id="e5fd2-149">If you're concerned about performance and scalability, you can evaluate the other strategies.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="e5fd2-150">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="e5fd2-150">Additional resources</span></span>

[<span data-ttu-id="e5fd2-151">تصميم نموذج تكوين المنتج</span><span class="sxs-lookup"><span data-stu-id="e5fd2-151">Build product configuration model</span></span>](build-product-configuration-model.md)

[<span data-ttu-id="e5fd2-152">الأساليب البحثية</span><span class="sxs-lookup"><span data-stu-id="e5fd2-152">Heuristics</span></span>](https://techterms.com/definition/heuristic)

[<span data-ttu-id="e5fd2-153">مشكلة الرضا عن القيود</span><span class="sxs-lookup"><span data-stu-id="e5fd2-153">Constraint Satisfaction Problem</span></span>](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf)
