---
title: إدارة المجموعات المنوعة
description: يشرح هذا الموضوع المفاهيم الأساسية لإدارة المجموعات المنوعة في Dynamics 365 Commerce، ويوفر اعتبارات التنفيذ لمشروعك.
author: jblucher
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.search.region: Global
ms.author: jeffbl
ms.search.validFrom: 2017-11-21
ms.dyn365.ops.version: Application update 5
ms.openlocfilehash: e1b177989065740eef0bd917a7ce1e0a2c79088b
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021430"
---
# <a name="assortment-management"></a><span data-ttu-id="111b2-103">إدارة الفرز</span><span class="sxs-lookup"><span data-stu-id="111b2-103">Assortment management</span></span>

[!include [banner](../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="111b2-104">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="111b2-104">Overview</span></span>

<span data-ttu-id="111b2-105">يوفر Dynamics 365 Commerce *مجموعات منوعة* تتيح لك إدارة توفر المنتجات عبر القنوات.</span><span class="sxs-lookup"><span data-stu-id="111b2-105">Dynamics 365 Commerce provides *assortments* that let you manage product availability across channels.</span></span> <span data-ttu-id="111b2-106">تحدد عمليات الفرز المنتجات التي تتوفر في متاجر مُعينة وخلال فترة زمنية معينة.</span><span class="sxs-lookup"><span data-stu-id="111b2-106">Assortments determine which products are available at specific stores and during a specific period.</span></span>

<span data-ttu-id="111b2-107">في Commerce، تمثل عملية الفرز تعيين لقناة واحدة أو أكثر (أو مجموعة من القنوات، عند استخدام التدرجات الهرمية للمؤسسات) لمنتج واحد أو أكثر (أو مجموعة منتجات عند استخدام التدرجات الهرمية للفئات).</span><span class="sxs-lookup"><span data-stu-id="111b2-107">In Commerce, an assortment is a mapping of one or more channels (or groups of channels, when organization hierarchies are used) to one or more products (or groups of products, when category hierarchies are used).</span></span>

<span data-ttu-id="111b2-108">يُحدد مزيج قنوات المنتج الشامل بواسطة عمليات الفرز المنشورة المُعيّنة للقناة.</span><span class="sxs-lookup"><span data-stu-id="111b2-108">The overall product mix of a channel is determined by the published assortments that are assigned to the channel.</span></span> <span data-ttu-id="111b2-109">لذلك، يمكنك تكوين العديد من عمليات الفرز النشطة لكل قناة.</span><span class="sxs-lookup"><span data-stu-id="111b2-109">Therefore, you can configure multiple active assortments per channel.</span></span>

### <a name="basic-assortment-setup"></a><span data-ttu-id="111b2-110">إعداد الفرز الأساسي</span><span class="sxs-lookup"><span data-stu-id="111b2-110">Basic assortment setup</span></span>

<span data-ttu-id="111b2-111">في المثال التالي، يتم تكوين فرز فريد لكل متجر.</span><span class="sxs-lookup"><span data-stu-id="111b2-111">In the following example, a unique assortment is configured for each store.</span></span> <span data-ttu-id="111b2-112">في هذه الحالة، يتوفر فقط المنتج 1 في المتجر 1، ويتوافر فقط المنتج 2 في المتجر 2.</span><span class="sxs-lookup"><span data-stu-id="111b2-112">In this case, only product 1 is available at store 1, and only product 2 is available at store 2.</span></span>

![يتوفر كل منتج في أحد المتاجر](./media/Managing-assortments-figure1.png)

<span data-ttu-id="111b2-114">لإتاحة المنتج 2 في المخزن 1، يمكنك إضافة المنتج إلى الفرز 1.</span><span class="sxs-lookup"><span data-stu-id="111b2-114">To make product 2 available at store 1, you can add the product to assortment 1.</span></span>

![تمت إضافة المنتج 2 إلى الفرز 1](./media/Managing-assortments-figure2.png)

<span data-ttu-id="111b2-116">بدلاً من ذلك، يمكنك إضافة المتجر 1 إلى الفرز 2.</span><span class="sxs-lookup"><span data-stu-id="111b2-116">Alternatively, you can add store 1 to assortment 2.</span></span>

![تمت إضافة المتجر 1 إلى الفرز 2](./media/Managing-assortments-figure3.png)

### <a name="organization-hierarchies"></a><span data-ttu-id="111b2-118">التدرجات الهرمية للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="111b2-118">Organization hierarchies</span></span>

<span data-ttu-id="111b2-119">في الحالات التي تشترك فيها عدة قنوات في نفس عمليات فرز المنتجات، يمكنك تكوين عمليات الفرز باستخدام التدرج الهرمي للمؤسسات لعمليات فرز Commerce.</span><span class="sxs-lookup"><span data-stu-id="111b2-119">In situations where multiple channels share the same product assortments, you can configure the assortments by using the Commerce assortment organization hierarchy.</span></span> <span data-ttu-id="111b2-120">عند إضافة العقد من هذا التدرج الهرمي، فسوف يتم تضمين جميع القنوات في تلك العقدة والعقد التابعة لها.</span><span class="sxs-lookup"><span data-stu-id="111b2-120">When nodes from this hierarchy are added, all channels in that node and its child nodes will be included.</span></span>

![التدرج الهرمي للمؤسسات](./media/Managing-assortments-figure4.png)

### <a name="product-categories"></a><span data-ttu-id="111b2-122">فئات المنتج</span><span class="sxs-lookup"><span data-stu-id="111b2-122">Product categories</span></span>

<span data-ttu-id="111b2-123">وبشكل مماثل، على جانب المنتج، يمكنك تضمين مجموعات المنتجات باستخدام التدرجات الهرمية لفئات المنتج.</span><span class="sxs-lookup"><span data-stu-id="111b2-123">Similarly, on the product side, you can include groups of products by using product category hierarchies.</span></span> <span data-ttu-id="111b2-124">يمكنك تكوين عمليات الفرز من خلال تضمين عقد تدرج هرمي للفئات واحدة أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="111b2-124">You can configure assortments by including one or more category hierarchy nodes.</span></span> <span data-ttu-id="111b2-125">في هذه الحالة، سوف تتضمن عملية الفرز جميع المنتجات في عقد الفئة تلك والعقد التابعة لها.</span><span class="sxs-lookup"><span data-stu-id="111b2-125">In this case, the assortment will include all products in that category node and its child nodes.</span></span>

![فئات المنتج](./media/Managing-assortments-figure5.png)

### <a name="excluded-products-or-categories"></a><span data-ttu-id="111b2-127">المنتجات أو الفئات المستثناة</span><span class="sxs-lookup"><span data-stu-id="111b2-127">Excluded products or categories</span></span>

<span data-ttu-id="111b2-128">بالإضافة إلى تضمين المنتجات والفئات في عمليات الفرز، يمكنك استخدام خيار استثناء لتحديد منتجات معينة أو فئات يجب استثنائها من عمليات الفرز.</span><span class="sxs-lookup"><span data-stu-id="111b2-128">In addition to including products and categories in assortments, you can use the Exclude option to define specific products or categories that should be excluded from assortments.</span></span> <span data-ttu-id="111b2-129">في المثال التالي، تحتاج إلى تضمين جميع المنتجات في فئة معينة، فيما عدا المنتج 2.</span><span class="sxs-lookup"><span data-stu-id="111b2-129">In the following example, you want to include all the products in a specific category, except product 2.</span></span> <span data-ttu-id="111b2-130">في هذه الحالة، لا يلزم تحديد فرز المنتجات حسب المنتج أو إنشاء عقد فئات إضافية.</span><span class="sxs-lookup"><span data-stu-id="111b2-130">In this case, you don't have to define the assortment product by product or create additional category nodes.</span></span> <span data-ttu-id="111b2-131">بدلاً من ذلك، يمكنك فقط تضمين الفئة مع استبعاد المنتج.</span><span class="sxs-lookup"><span data-stu-id="111b2-131">Instead, you can just include the category but exclude the product.</span></span>

> [!NOTE]
> <span data-ttu-id="111b2-132">إذا كان أحد المنتجات مُدرج ومستبعد في واحدة أو أكثر من عمليات الفرز حسب التعريف، فسوف يعتبر المنتج مستبعد دائمًا.</span><span class="sxs-lookup"><span data-stu-id="111b2-132">If a product is both included and excluded in one or more assortments by definition, the product will always be considered excluded.</span></span>

![المنتج المستثنى](./media/Managing-assortments-figure6.png)

### <a name="global-and-released-products"></a><span data-ttu-id="111b2-134">المنتجات العمومية والمُصدرة</span><span class="sxs-lookup"><span data-stu-id="111b2-134">Global and released products</span></span>

<span data-ttu-id="111b2-135">يتم تحديد عمليات الفرز على مستوى عمومي، ويمكن أن تحتوي على قنوات من كيانات قانونية متعددة.</span><span class="sxs-lookup"><span data-stu-id="111b2-135">Assortments are defined at a global level and can contain channels from multiple legal entities.</span></span> <span data-ttu-id="111b2-136">تتم أيضًا مشاركة المنتجات والفئات المُضمنة في عمليات الفرز عبر الكيانات القانونية.</span><span class="sxs-lookup"><span data-stu-id="111b2-136">The products and categories that are included in assortments are also shared across legal entities.</span></span> <span data-ttu-id="111b2-137">ومع ذلك، يجب إصدار منتج قبل بيعه فعليًا أو طلبه أو حسابه أو استلامه في القناة (على سبيل المثال، في نقطة البيع \[نقطة البيع\]).</span><span class="sxs-lookup"><span data-stu-id="111b2-137">However, a product must be released before it can actually be sold, ordered, counted, or received in the channel (for example, in the point of sale \[POS\]).</span></span> <span data-ttu-id="111b2-138">ولذلك، على الرغم من أنه يمكن لمتجرين في كيانات قانونية مختلففة مشاركة عملية فرز تحتوي على نفس المنتجات، فسوف تتوافر المنتجات فقط إذا تم إصدارها لهذه الكيانات القانونية.</span><span class="sxs-lookup"><span data-stu-id="111b2-138">Therefore, although two stores in different legal entities can share an assortment that contains the same products, the products are available only if they have been released to those legal entities.</span></span>

### <a name="dynamic-and-static-assortments"></a><span data-ttu-id="111b2-139">عمليات الفرز الديناميكية والثابتة</span><span class="sxs-lookup"><span data-stu-id="111b2-139">Dynamic and static assortments</span></span>

<span data-ttu-id="111b2-140">يمكن تحديد عمليات الفرز باستخدام قنوات معينة ومنتجات، أو من خلال تضمين وحدات المؤسسات والفئات.</span><span class="sxs-lookup"><span data-stu-id="111b2-140">Assortments can be defined with specific channels and products or by including organization units and categories.</span></span> <span data-ttu-id="111b2-141">وتعتبر عمليات الفرز بما في ذلك المراجع لهذه المجموعات، عمليات فرز ديناميكية.</span><span class="sxs-lookup"><span data-stu-id="111b2-141">Assortments including references to these groups are considered dynamic assortments.</span></span> <span data-ttu-id="111b2-142">إذا تغير تعريف أو محتويات هذه المجموعات عندما يكون الفرز نشطًا، فسوف يتغير أيضًا تعريف الفرز.</span><span class="sxs-lookup"><span data-stu-id="111b2-142">If the definition or contents of those groups change while the assortment is active, the definition of the assortment will also change.</span></span>

<span data-ttu-id="111b2-143">على سبيل المثال، تم تحديد عملية فرز في الأصل ونشرت حتى تشير إلى فئة المنتجات.</span><span class="sxs-lookup"><span data-stu-id="111b2-143">For example, an assortment is originally defined and published so that it references a category of products.</span></span> <span data-ttu-id="111b2-144">إذا تمت إضافة منتجات إضافية إلى الفئة في وقت لاحق، فمن ثم تُضمن تلك المنتجات تلقائيًا في تعريف عملية الفرز الحالية.</span><span class="sxs-lookup"><span data-stu-id="111b2-144">If additional products are later added to the category, those products are automatically included in the definition of the existing assortment.</span></span> <span data-ttu-id="111b2-145">ولا يلزمك إضافة المنتجات إلى عملية الفرز يدويًا.</span><span class="sxs-lookup"><span data-stu-id="111b2-145">You don't have to manually add the products to the assortment.</span></span> <span data-ttu-id="111b2-146">وبالمثل، إذا تمت إضافة وحدة تنظيمية إلى عقد مختلفة، فمن ثم يتم ضبط فرز الوحدة التنظيمية بناءً على هذا التعريف.</span><span class="sxs-lookup"><span data-stu-id="111b2-146">Similarly, if an organization unit is added to a different node, the organization unit's assortment is automatically adjusted based on that definition.</span></span>

### <a name="stopped-products"></a><span data-ttu-id="111b2-147">المنتجات التي تم وقفها</span><span class="sxs-lookup"><span data-stu-id="111b2-147">Stopped products</span></span>

<span data-ttu-id="111b2-148">يمكنك "وقف" المنتجات المُصرة لعملية المبيعات من خلال تشغيل إعداد في إعدادات **الأوامر الافتراضية**.</span><span class="sxs-lookup"><span data-stu-id="111b2-148">You can "stop" released products for the sales process by turning on a setting in the **Default order** settings.</span></span> <span data-ttu-id="111b2-149">يُستخدم هذا الإعداد غالبًا عندما يكون أحد المنتجات في نهاية دورة الحياة الخاصة به، ولا يجب بيعه إلى في أي قناة.</span><span class="sxs-lookup"><span data-stu-id="111b2-149">This setting is most often used when a product is at the end of its life and should not be sold at any channel.</span></span> <span data-ttu-id="111b2-150">تُراعي عمليات الفرز هذا الإعداد، وتقوم المنتجات ولا تُدخلها ضمن الفرز، بغض النظر عن تكوين الفرز.</span><span class="sxs-lookup"><span data-stu-id="111b2-150">Assortments respect this setting, and stopped products won't be assorted, regardless of the assortment configuration.</span></span>

### <a name="blocked-products"></a><span data-ttu-id="111b2-151">المنتجات المحظورة</span><span class="sxs-lookup"><span data-stu-id="111b2-151">Blocked products</span></span>

<span data-ttu-id="111b2-152">بالإضافة إلى إيقاف مبيعات أحد المنتجات، يمكن حظر مبيعات أحد المنتجات مؤقتًا.</span><span class="sxs-lookup"><span data-stu-id="111b2-152">In addition to stopping sales of a product, you can temporarily block sales of a product.</span></span> <span data-ttu-id="111b2-153">يمكنك تكوين هذا الإعداد على علامة تبويب **التجارة** لمنتج تم إصداره.</span><span class="sxs-lookup"><span data-stu-id="111b2-153">You can configure this setting on the **Commerce** tab of a released product.</span></span> <span data-ttu-id="111b2-154">لا تزال المنتجات المحظورة مُصنفة، ولكن سوف تتسلم رسالة في نقطة البيع تنص على أن المنتج لا يمكن بيعه.</span><span class="sxs-lookup"><span data-stu-id="111b2-154">Blocked products are still assorted, but you will receive a message in the POS that states that the product can't be sold.</span></span>

### <a name="date-effectivity"></a><span data-ttu-id="111b2-155">سريان التاريخ</span><span class="sxs-lookup"><span data-stu-id="111b2-155">Date effectivity</span></span>

<span data-ttu-id="111b2-156">عمليات الفرز لها تاريخ سريان.</span><span class="sxs-lookup"><span data-stu-id="111b2-156">Assortments are date-effective.</span></span> <span data-ttu-id="111b2-157">ولذلك، يمكن لتجار التجزئة تكوين متى يجب توافر المنتجات أو لا يجب توافرها لكل قناة.</span><span class="sxs-lookup"><span data-stu-id="111b2-157">Therefore, retailers can configure when products should or should not be available per channel.</span></span> <span data-ttu-id="111b2-158">يمكنك تحديد ونشر عمليات فرز الأحداث مسبقاً، وتحديد تواريخ البدء والانتهاء.</span><span class="sxs-lookup"><span data-stu-id="111b2-158">You can define and publish assortments ahead of time, and specify the start and end dates.</span></span> <span data-ttu-id="111b2-159">سوف تصبح المنتجات متاحة أو غير متاحة تلقائيًا في التواريخ المُحددة.</span><span class="sxs-lookup"><span data-stu-id="111b2-159">The products will automatically become available or unavailable on the specified dates.</span></span>

### <a name="process-assortments-batch-job"></a><span data-ttu-id="111b2-160">قم بمعالجة الوظيفة الدفعية للمجموعة</span><span class="sxs-lookup"><span data-stu-id="111b2-160">Process assortments batch job</span></span>

<span data-ttu-id="111b2-161">يجب معالجة عمليات الفرز التي تم تعريفها في Commerce قبل تفعيلها.</span><span class="sxs-lookup"><span data-stu-id="111b2-161">Assortments that are defined in Commerce must be processed before they take effect.</span></span> <span data-ttu-id="111b2-162">تنفذ هذه المُعالجة للأسباب التالية:</span><span class="sxs-lookup"><span data-stu-id="111b2-162">This processing is done for the following reasons:</span></span>

- <span data-ttu-id="111b2-163">يجب ألا يتم توحيد تعريفات عمليات الفرز بحيث تستهلكها القنوات بسهولة.</span><span class="sxs-lookup"><span data-stu-id="111b2-163">Assortment definitions must be de-normalized so that channels can more easily consume them.</span></span> <span data-ttu-id="111b2-164">يمكن تحديد خلط المنتج لقناة من خلال عمليات فرز متعددة تمتد على نطاقات تواريخ مختلفة.</span><span class="sxs-lookup"><span data-stu-id="111b2-164">A product mix for a channel can be defined through multiple assortments that span various date ranges.</span></span> <span data-ttu-id="111b2-165">عندما يتم حساب بعض من هذه المعلومات مسبقًا على الخادم، يتحسن الأداء في القناة.</span><span class="sxs-lookup"><span data-stu-id="111b2-165">When some of this information is calculated ahead of time on the server, performance at the channel is improved.</span></span>
- <span data-ttu-id="111b2-166">يمكن تغيير المنتجات والقنوات في الفرز خارج عملية الفرز نفسها.</span><span class="sxs-lookup"><span data-stu-id="111b2-166">The products and channels in the assortment can change outside the assortment itself.</span></span> <span data-ttu-id="111b2-167">يجب مُعالجة عمليات الفرز الديناميكية التي تحتوي على مراجع للفئات أو الوحدات التنظيمية بشكل دوري بحيث تقوم بتضمين أو استبعاد السجلات على أساس التعيينات الحالية الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="111b2-167">Dynamic assortments that contain references to categories or organization units must be processed periodically so that they include or exclude records, based on their current assignment.</span></span>

## <a name="implementation-considerations"></a><span data-ttu-id="111b2-168">اعتبارات التنفيذ</span><span class="sxs-lookup"><span data-stu-id="111b2-168">Implementation considerations</span></span>

<span data-ttu-id="111b2-169">ضع في الاعتبار متطلبات التنفيذ التالية عندما تكون بصدد التخطيط وإدارة عمليات فرز لتنفيذ Commerce:</span><span class="sxs-lookup"><span data-stu-id="111b2-169">Consider the following implementation requirements as you plan and manage assortments for your Commerce implementation:</span></span>

- <span data-ttu-id="111b2-170">**حجم قاعدة بيانات والنسخ المتماثل للبيانات** -على الرغم من أن عمليات الفرز تساعد في خدمة احتياجات العمل في إدارة توافر المنتجات، فإنها أيضًا تُعد أداة مهمة لإدارة حجم القناة وقواعد البيانات دون اتصال.</span><span class="sxs-lookup"><span data-stu-id="111b2-170">**Data replication and database size** – Although assortments help serve the business need to manage product availability, they are also an important tool for managing the size of channel and offline databases.</span></span> <span data-ttu-id="111b2-171">تُساعد عمليات الفرز المُدارة بشكل جيد على تقليل كمية البيانات التي يجب معالجتها ونسخها نسخًا متماثلًا إلى القناة وقواعد البيانات دون اتصال.</span><span class="sxs-lookup"><span data-stu-id="111b2-171">Well-managed assortments help reduce the amount of data that must be processed and replicated to channel and offline databases.</span></span> <span data-ttu-id="111b2-172">وتساعد أيضًا على تقليل عدد السجلات التي يجب أن تستمر.</span><span class="sxs-lookup"><span data-stu-id="111b2-172">They also help reduce the number of records that must be persisted.</span></span> <span data-ttu-id="111b2-173">وسوف يُزيد وجود عدد أقل من السجلات في قواعد البيانات هذه، من الأداء عند إضافة الأصناف إلى الحركة أو البحث أو الاستعراض بحثًا عن المنتجات.</span><span class="sxs-lookup"><span data-stu-id="111b2-173">Fewer records in these databases will increase performance when you add items to a transaction, search, and browse for products.</span></span>
- <span data-ttu-id="111b2-174">**تاريخ سريان/انتهاء عمليات الفرز** -من الأدوات الأكثر فعالية لإدارة عدد المنتجات في القناة وقواعد البيانات دون اتصال هي فاعلية تاريخ عمليات الفرز.</span><span class="sxs-lookup"><span data-stu-id="111b2-174">**Date-effective/expiring assortments** – One of the most effective tools for managing the number of products in channel and offline databases is the date effectivity of assortments.</span></span> <span data-ttu-id="111b2-175">إذا تركت عمليات الفرز بنهاية مفتوحة (غير منتهية) لمنتجات موسمية أو لمنتجات في نهاية دورة حياتها، فسوف يزد حجم قواعد البيانات هذه بشكل غير محدود.</span><span class="sxs-lookup"><span data-stu-id="111b2-175">If you leave open-ended (non-expiring) assortments for seasonal products or products that are at the end of their life, these databases will grow indefinitely.</span></span> <span data-ttu-id="111b2-176">يمكنك استخدام أساليب مختلفة للمساعدة في إدارة هذا الموقف.</span><span class="sxs-lookup"><span data-stu-id="111b2-176">You can use various approaches to help manage this situation.</span></span> <span data-ttu-id="111b2-177">على سبيل المثال، يمكنك الاحتفاظ بعمليات فرز منفصلة للمنتجات الموسمية والمنتجات المتوفرة بشكل دائم.</span><span class="sxs-lookup"><span data-stu-id="111b2-177">For example, you can maintain separate assortments for seasonal products and products that are always available.</span></span>
- <span data-ttu-id="111b2-178">**المبيعات والعائدات خارج عمليات الفرز** – تساعد هذه الإمكانية تجار التجزئة في الإدارة الفعّالة لعمليات الفرز الخاصة بهم عن طريق السماح لهم بتحديد عدد المنتجات المتوفرة بالنسبة للمنتجات التي تنتمي إلى خليط المنتج الأساسي الخاص بالمتجر.</span><span class="sxs-lookup"><span data-stu-id="111b2-178">**Sales and returns outside assortments** – This capability helps retailers effectively manage their assortments by letting them limit the number of available products to products that belong to the core product mix for the store.</span></span> <span data-ttu-id="111b2-179">كما تساعد هذه الإمكانية تجار التجزئة على التعامل مع المواقف التي يتم فيها حذف منتج عن طريق الخطأ من عملية الفرز، أو عندما يتم إرجاع منتج خارج نطاق التواريخ الفعّالة لعملية الفرز.</span><span class="sxs-lookup"><span data-stu-id="111b2-179">This capability also helps retailers handle situations where a product was mistakenly omitted from an assortment, or where a product was returned outside the effective dates for the assortment.</span></span>

<span data-ttu-id="111b2-180">في حالة عدم وجود بيانات المنتج في قواعد بيانات القناة، فمن ثم تقوم نقطة البيع باستدعاءات في الوقت الفعلي للمركز الرئيسي لاسترداد المعلومات المطلوبة، وبذلك يُمكن بيع المنتج أو إعادته أو وضعه في طلب عميل.</span><span class="sxs-lookup"><span data-stu-id="111b2-180">If product data doesn't exist in the channel database, the POS makes real-time calls to headquarters to retrieve the required information, so that the product can be sold, returned, or put on a customer order.</span></span> <span data-ttu-id="111b2-181">تتوافر معلومات المنتج التي يتم استردادها بهذه الطريقة فقط في أثناء نطاق هذه الحركة.</span><span class="sxs-lookup"><span data-stu-id="111b2-181">Product information that is retrieved in this manner is available only during the scope of that transaction.</span></span> <span data-ttu-id="111b2-182">لا تتم إضافة المنتج إلى تعريف الفرز.</span><span class="sxs-lookup"><span data-stu-id="111b2-182">The product isn't added to the assortment definition.</span></span> <span data-ttu-id="111b2-183">لذلك، سوف يتم إجراء الاستدعاءات اللاحقة في الوقت الفعلي على النحو المطلوب.</span><span class="sxs-lookup"><span data-stu-id="111b2-183">Therefore, subsequent real-time calls will be made as required.</span></span>