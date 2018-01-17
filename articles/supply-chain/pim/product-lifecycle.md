---
title: "حالة دورة حياة المنتج"
description: "توثق حالة دورة حياة منتج، حالة دورة حياة المنتج الذي تم إصداره أو متغير المنتج."
author: cvocph
manager: AnnBe
ms.date: 12/08/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductLifecycleState, EcoResReleasedProductLifecycleStateChanges
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core (Operations, Core)
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: cvocph
ms.dyn365.ops.intro: 7.3
ms.search.validFrom: 2017-12-31
ms.translationtype: HT
ms.sourcegitcommit: 33130a4061f22335aeeffa69c478b693604393a9
ms.openlocfilehash: a57f306ba02c5758c39c4bd29d9a4fa0d7efbcd3
ms.contentlocale: ar-sa
ms.lasthandoff: 12/20/2017

---

# <a name="product-lifecycle-state"></a><span data-ttu-id="fe1ef-103">حالة دورة حياة المنتج</span><span class="sxs-lookup"><span data-stu-id="fe1ef-103">Product lifecycle state</span></span> 

[!include[banner](../includes/banner.md)]


<span data-ttu-id="fe1ef-104">توثق حالة دورة حياة منتج، حالة دورة حياة المنتج الذي تم إصداره أو متغير المنتج.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-104">A product lifecycle state documents the lifecycle state of a released product or product variant.</span></span> <span data-ttu-id="fe1ef-105">تُحدد حالات دورة حياة المنتج بواسطة المستخدم، وعادةً ما تُحدد من خلال مدير المنتج أو مدير مدير البيانات الرئيسية للمنتج.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-105">Product lifecycle states are defined by the user, typically a product manager or a product master data manager.</span></span> <span data-ttu-id="fe1ef-106">قد تتأثر عمليات أعمال مُحددة، مثل التخطيط الرئيسي، بحالة دورة حياة محددة.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-106">Specific business processes, such as master planning, can be affected by a specific lifecycle state.</span></span>   
 
<span data-ttu-id="fe1ef-107">يمكن إقران منتج مُصدر أو متغير المنتج بحالة دورة حياة منتج والتي يتم فيها توثيق حالة دورة حياة منتج محدد أو المتغير الخاص بحالة المنتج حاليًا.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-107">A released product or product variant can be associated with a product lifecycle state that documents in which lifecycle state a specific product or variant is currently in.</span></span> <span data-ttu-id="fe1ef-108">يمكنك تحديد أي عدد من حالات دورة حياة المنتج عن طريق تعيين اسم حالة ووصف.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-108">You can define any number of product lifecycle states by assigning a state name and description.</span></span> <span data-ttu-id="fe1ef-109">يمكنك تحديد حالة دورة حياة واحدة كحالة افتراضية للمنتجات المُصدرة حديثًا.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-109">You can select one lifecycle state as the default state for new released products.</span></span> <span data-ttu-id="fe1ef-110">تكتسب متغيرات المنتجات المُصدرة حالة دورة حياة المنتج من أصل المنتج المُصدر عند إنشائها.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-110">Released product variants inherit their product lifecycle state from their released product master on creation.</span></span> <span data-ttu-id="fe1ef-111">عند تغيير حالة دورة حياة منتج على أصل المنتج المٌصدر، يمكن اختيار تحديث جميع المتغيرات الحالية التي لها نفس الحالة الأصلية.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-111">When changing the lifecycle state on a released product master, you can choose to update all existing variants that have the same original state.</span></span>  

## <a name="create-a-new-product-lifecycle-state"></a><span data-ttu-id="fe1ef-112">إنشاء حلة دورة حياة منتج جديد</span><span class="sxs-lookup"><span data-stu-id="fe1ef-112">Create a new product lifecycle state</span></span> 
 
- <span data-ttu-id="fe1ef-113">لإنشاء حالة دورة حياة منتج جديد، قم بتشغيل أو قراءة دليل المهام **إنشاء حالة دورة حياة منتج جديد**.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-113">To create a new product lifecycle state, play or read the task guide **Create a new product lifecycle state**.</span></span> 

-  <span data-ttu-id="fe1ef-114">لإنشاء حالة دورة حياة منتج افتراضية، قم بتشغيل أو قراءة دليل المهام **إنشاء حالة دورة حياة منتج افتراضية**.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-114">To create a default product lifecycle state, play or read the task guide **Create a default product lifecycle state**.</span></span>   

## <a name="associate-product-lifecycle-states-to-released-products"></a><span data-ttu-id="fe1ef-115">إقران حالات دورة حياة المنتج للمنتجات المُصدرة</span><span class="sxs-lookup"><span data-stu-id="fe1ef-115">Associate product lifecycle states to released products</span></span>  

<span data-ttu-id="fe1ef-116">توجد عدة طرق لإقران حالة دورة حياة منتج للمنتجات المُصدرة أو متغيرت المُنتج.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-116">There are multiple ways to associate a product lifecycle state to released products or product variants.</span></span>

-  <span data-ttu-id="fe1ef-117">عند إنشاء منتج مُصدر جديد، يتم تعيين **حالة دورة حياة المنتج** الافتراضية تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-117">On creation of a new released product, the default **Product lifecycle state** is automatically assigned.</span></span> 
-  <span data-ttu-id="fe1ef-118">عند إصدار منتج لكيان قانوني، يتم تعيين **حالة دورة حياة المنتج** الافتراضية تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-118">On release of a product to a legal entity, the default **Product lifecycle state** is automatically assigned.</span></span> 
-  <span data-ttu-id="fe1ef-119">عند إصدار متغير المنتج لكيان قانوني، يتم تعيين **حالة دورة حياة المنتج** المقترنة بأصل المنتج المُصدر في هذا الكيان القانوني تلقائيًا إلى المتغير الجديد.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-119">On release of a product variant to a legal entity, the **Product lifecycle state** associated to the released product master in this legal entity is automatically assigned to the new variant.</span></span> 

<span data-ttu-id="fe1ef-120">يمكنك تحديث حالة دورة حياة المنتج يدوياً باستخدام:</span><span class="sxs-lookup"><span data-stu-id="fe1ef-120">You can manually update the product lifecycle state by using:</span></span> 

-    <span data-ttu-id="fe1ef-121">صفحة قائمة **المنتجات التي تم إصدارها**، أو **طريقة عرض التفاصيل**.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-121">The **Released products** list page or **Details view**.</span></span> 
-  <span data-ttu-id="fe1ef-122">صفحة قائمة **متغيرات المنتجات التي تم إصدارها**، أو **طريقة عرض التفاصيل**.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-122">The **Released product variants** list page or **Details view**.</span></span> 
-  <span data-ttu-id="fe1ef-123">ابحث عن المنتجات القديمة أو متغيرات المنتج بناءً على الطلب وإقرانها بحالة دورة حياة المنتج.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-123">Find the obsolete products or product variants based on demand and associate a lifecycle state.</span></span>  

<span data-ttu-id="fe1ef-124">للحصول على معلومات تفصيلية حول كيفية إقران حالات دورة حياة المنتج، قم بتشغيل أو قراءة دليلي المهام التاليين.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-124">For detailed information about how to associate product lifecycle states, play or read the following two task guides.</span></span>

-  <span data-ttu-id="fe1ef-125">لإقران حالة دورة حياة إلى أصل منتج تم إصداره، قم بتشغيل أو قراءة دليل المهام **تعيين حالة دورة حياة منتج لأصل منتج تم إصداره**.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-125">To associate a product lifecycle state to a released product master, play or read the task guide **Assign a product lifecycle state to a released product master**.</span></span> 

-  <span data-ttu-id="fe1ef-126">لإقران حالة دورة حياة إلى منتج مُصدر، قم بتشغيل أو قراءة دليل المهام **تعيين حالة دورة حياة منتج لمنتج تم إصداره**.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-126">To associate a product lifecycle state to a release product, play or read the task guide **Assign a product lifecycle state to a released product**.</span></span> 

## <a name="impact-on-master-planning"></a><span data-ttu-id="fe1ef-127">الأثر على التخطيط الرئيسي</span><span class="sxs-lookup"><span data-stu-id="fe1ef-127">Impact on master planning</span></span> 

<span data-ttu-id="fe1ef-128">يكون لحالة دورة حياة المنتج علامة تحكم واحدة فقط وهي:**نشط للتخطيط**.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-128">The product lifecycle state has only one control flag: **Is active for planning**.</span></span> <span data-ttu-id="fe1ef-129">بشكل افتراضي، يتم تعيينها إلى **نعم**لجميع حالات دورة حياة المنتج التي تم إنشاؤها، ولكن يمكن تغييرها إلى **لا**.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-129">By default, this is set to **Yes** for all created product lifecycle states, but it can be changed to **No**.</span></span> <span data-ttu-id="fe1ef-130">عند التعيين إلى **لا**، تكون المنتجات المقترنة التي تم إصدارها أو متغيرات المنتجات التي تم إصدارها هي:</span><span class="sxs-lookup"><span data-stu-id="fe1ef-130">When set to **No**, the associated released products or released product variants are:</span></span> 

-  <span data-ttu-id="fe1ef-131">مستبعدة من التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-131">Excluded from master planning.</span></span> 
-  <span data-ttu-id="fe1ef-132">مستبعدة من حساب مستوى قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-132">Excluded from BOM-level calculation.</span></span> 

<span data-ttu-id="fe1ef-133">للحصول على معلومات تفصيلية حول كيفية استخدام حالة دورة حياة المنتج لاستبعاد منتجات من التخطيط الرئيسي وحساب مستوى قائمة مكونات الصنف، قم بتشغيل أو قراءة دليل المهام **إنشاء حالة دورة حياة منتج لاستبعاد المنتجات من التخطيط الرئيسي**.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-133">For detailed information about how to use product lifecycle state to exclude products from master planning and BOM-level calculation, play or read the task guide **Create a product lifecycle state to exclude products from Master planning**.</span></span>

> [!NOTE]
> <span data-ttu-id="fe1ef-134">لأسباب تتعلق بالتنفيذ، فإنه يوصي وبشدة إقران جميع المنتجات القديمة المُصدرة أو متغيرات المنتج، وبخاصة عند التعامل مع متغيرات تكوين منتج غير قابلة لإعادة الاستخدام، بحالة دورة حياة المنتج الذي تم إلغاء تنشيط التخطيط الرئيسي لها.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-134">For performance reasons, it is highly recommended to associate all obsolete released products or product variants, especially when working with non-reusable product configuration variants, with a product lifecycle state that is deactivated for master planning.</span></span>  
 
## <a name="default-migration-import-and-export"></a><span data-ttu-id="fe1ef-135">ترحيل البيانات الافتراضي واستيرادها وتصديرها</span><span class="sxs-lookup"><span data-stu-id="fe1ef-135">Default migration, import, and export</span></span> 

<span data-ttu-id="fe1ef-136">حالات دورة حياة المنتج غير مدعومة من قبل كيانات البيانات، ولا يمكن تعيين حالة دورة حياة إلى حالة متغيرة من خلال كيانات بيانات المنتجات المُصدرة.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-136">The product lifecycle states are not supported by data entities, and the lifecycle state cannot be set to a variable state through the released product data entities.</span></span>

-  <span data-ttu-id="fe1ef-137">عند الترحيل من إصدارات سابقة، سوف تكون جميع حالة دورة حياة جميع المنتجات ومتغيرات المنتج فارغة.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-137">On migration from previous releases, the lifecycle state of all products and product variants will be blank.</span></span>  
-  <span data-ttu-id="fe1ef-138">عند استيراد منتجات مُصدرة من خلال كيان بيانات، فسوف تطبق حالة دورة الحياة الافتراضية عند إنشائها.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-138">When importing released products through a data entity, the default lifecycle state will be applied on creation.</span></span>  
-  <span data-ttu-id="fe1ef-139">عند استيراد متغيرات منتجات تم إصدارها من خلال كيان البيانات، فسوف يتم استيراد حالة دورة حياة المنتج لأصل المنتجات الذي تم إصدارها.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-139">When importing released product variants through a data entity, the product lifecycle state of the released product master will be imported.</span></span>   
 
## <a name="find-obsolete-products-and-products-variants"></a><span data-ttu-id="fe1ef-140">البحث عن المنتجات القديمة ومتغيرات المنتجات</span><span class="sxs-lookup"><span data-stu-id="fe1ef-140">Find obsolete products and products variants</span></span> 
 
<span data-ttu-id="fe1ef-141">يمكنك تشغيل تحليل محاكاة للبحث عن المنتجات القديمة المُصدرة أو متغيرات المنتجات، ثم قم بتحديث حالة دورة حياة المنتج الخاصة بهذه المنتجات.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-141">You can run a simulation analysis to find the obsolete released products or product variants and then update their product lifecycle status.</span></span> <span data-ttu-id="fe1ef-142">للبحث عن المنتجات القديمة، قم بتشغيل وقراءة دليل المهام **البحث عن متغيرات المنتجات القديمة وتعيين حالة دورة حياة منتج**.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-142">To find obsolete products, play and read the task guide **Find obsolete product variants and assign a product lifecycle state**.</span></span> <span data-ttu-id="fe1ef-143">يوضح دليل المهام هذا كيفية البحث عن المنتجات القديمة المُصدرة أو متغيرات المنتج، وكيفية إقرانها بحالة دورة حياة منتج بالمنتجات القديمة.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-143">This task guide shows how to find obsolete released products or product variants and how to associate a product lifecycle state to the obsolete products.</span></span> <span data-ttu-id="fe1ef-144">ويوضح أيضًا كيفية عرض نتائج المحاكاة، وتقييم كيف إقران العديد من المنتجات ومتغيرات المنتجات بحالة دورة حياة منتج جديد عند تشغيل التحديث بدون محاكاة.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-144">It also shows hot to view the simulation results and assess how many products and product variants will be associated with a new product lifecycle state when running the update without simulation.</span></span>  
 
<span data-ttu-id="fe1ef-145">من خلال تشغيل التحليل في وضع محاكاة، سوف يتم عرض المنتجات وتغيرات المنتجات المُحددة كمنتجات قديمة في نموذج محدد، بحيث تسهل مراجعتها.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-145">By running the analysis in a simulation mode, the products and product variants identified as obsolete are displayed in a specific form, where they can easily be reviewed.</span></span> <span data-ttu-id="fe1ef-146">تبحث التحليلات عن الحركات وأصل المنتج المحدد لتحديد المنتجات التي ليس عليها طلب خلال فترة زمنية متغيرة وليس لها أصل منتج قد يؤدي إلى الطلب.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-146">The analysis searches for transactions and specific master data to identify products that have no demand within a variable period and no master data that can result in demand.</span></span> <span data-ttu-id="fe1ef-147">يمكن استبعاد المنتجات الجديدة الصادرة في غضون فترة زمنية متغيرة من التحليل.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-147">New released products within a variable period can be excluded from the analysis.</span></span> <span data-ttu-id="fe1ef-148">عندما تعرض محاكاة التحليل نتيجة متوقعة، يمكن للمستخدم تشغيل التحليل وتعيين حالة دورة حياة منتج جديد لجميع المنتجات التي حددها التحليل على أنها قديمة.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-148">When the analysis simulation returns the expected result, the user can run the analysis and set a new product lifecycle state to all products identified as obsolete by the analysis.</span></span>  
 
> [!NOTE]
> <span data-ttu-id="fe1ef-149">لاحظ أن كافة التحليلات والتحديثات يجب أن تتم في نفس الكيان القانوني.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-149">Note that all analysis and updates must be done within the same legal entity.</span></span>  
 
## <a name="criteria-to-select-and-update-released-products-or-product-variants"></a><span data-ttu-id="fe1ef-150">المعايير اللازم تحديدها وتحديث المنتجات الصادرة أو متغيرات المنتجات.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-150">Criteria to select and update released products or product variants</span></span> 
 
<span data-ttu-id="fe1ef-151">استخدم المعيار التالي لتحديد وتحديث المنتجات الصادرة ومتغيرات المنتجات:</span><span class="sxs-lookup"><span data-stu-id="fe1ef-151">Use the following criteria to select and update the released products and product variants:</span></span> 

-    <span data-ttu-id="fe1ef-152">يجب أن تختلف حالة دورة حياة المنتج للمنت أو متغير المنتج عن الحالة الجديدة المرغوبة.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-152">The product lifecycle state of the product or product variant must be different from the new desired state.</span></span> 
-  <span data-ttu-id="fe1ef-153">تم إنشاء منتج أو متغير منتج منذ عدة أيام بناءً على عدد الأيام التي يتم إدخالها في مربع حوار التحديد.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-153">The product or product variant was created some days ago based on the number of days that you enter in the selection dialog box.</span></span> 
-  <span data-ttu-id="fe1ef-154">لا توجد أوامر إنتاج مفتوحة (الحالة = < إنهاء) لمنتج أو متغير المنتج.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-154">There are no open production orders (= status < ended) for the product or product variant.</span></span> 
-  <span data-ttu-id="fe1ef-155">لا توجد حركات مخزون مفتوحة (= إصدار حالة ReservPhysical إلى QuotationIssue أو أو حالة إيصال استلام مسجل إلى QuotationReceipt) للمنتج أو متغير المنتج.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-155">There are no open inventory transactions (= status issue ReservPhysical to QuotationIssue or status receipt Registrered to QuotationReceipt) for the product or product variant.</span></span> 
-  <span data-ttu-id="fe1ef-156">لا توجد أي حركات مخزون خلال آخر عدة أيام للمنتج أو متغير المنتج.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-156">There are no inventory transactions within the last number of days for the product or product variant.</span></span> 
-  <span data-ttu-id="fe1ef-157">لا يوجد طلب مستقبلي أو تنبؤ بالتوريد للمنتج أو متغير المنتج.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-157">There is no future demand or supply forecast for the product or product variant.</span></span>  
-  <span data-ttu-id="fe1ef-158">لم يتم تعيين مستوى الحد الأدنى للمخزون في تغطية الصنف للمنتج أو متغير المنتج.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-158">No minimum stock level has been set in item coverage for the product or product variant.</span></span> 
-  <span data-ttu-id="fe1ef-159">لا توجد قاعدة كانبان لكمية ثابتة نشطة للمنتج أو متغير المنتج.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-159">No active fixed quantity kanban rule for the product or product variant.</span></span>  
-  <span data-ttu-id="fe1ef-160">لا يوجد بند أمر خدمة للمنتج أو متغير المنتج.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-160">No service order line for the product or product variant.</span></span> 
-  <span data-ttu-id="fe1ef-161">لا توجد مبيعات نشطة أو مستقبلية أو بنود اتفاقية شراء للمنتج أو متغير المنتج.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-161">No active or future sales or purchase agreement lines for the product or product variant.</span></span> 
-  <span data-ttu-id="fe1ef-162">لا يستخدم المنتج أو مُتغير المنتج في قائمة مكونات الصنف المقترنة بإصدار قائمة مكونات صنف معتمدة وغير منتهية الصلاحية لمنتج أو متغر نشط للتخطيط.</span><span class="sxs-lookup"><span data-stu-id="fe1ef-162">The product or product variant is not used in a BOM that is associated with a non-expired approved BOM version for a product or variant that is active for planning.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe1ef-163">مواضيع مرتبطة</span><span class="sxs-lookup"><span data-stu-id="fe1ef-163">Related topics</span></span>

-  <span data-ttu-id="fe1ef-164">إنشاء حلة دورة حياة منتج جديد</span><span class="sxs-lookup"><span data-stu-id="fe1ef-164">Create a new product lifecycle state</span></span>
-  <span data-ttu-id="fe1ef-165">إنشاء حالة دورة حياة منتج جديد افتراضية</span><span class="sxs-lookup"><span data-stu-id="fe1ef-165">Create a default new product lifecycle state</span></span>
-  <span data-ttu-id="fe1ef-166">تعيين حالة دورة حياة منتج لأصل منتج صادر</span><span class="sxs-lookup"><span data-stu-id="fe1ef-166">Assign a product lifecycle state to a released product master</span></span>
-  <span data-ttu-id="fe1ef-167">تعيين حالة دورة حياة منتج لمنتج صادر</span><span class="sxs-lookup"><span data-stu-id="fe1ef-167">Assign a product lifecycle state to a released product</span></span>
-  <span data-ttu-id="fe1ef-168">البحث عن متغيرات منتجات قديمة، وتعيين حالة دورة حياة منتج</span><span class="sxs-lookup"><span data-stu-id="fe1ef-168">Find obsolete product variants and assign a product lifecycle state</span></span>
-  <span data-ttu-id="fe1ef-169">إنشاء حالة دورة حياة منتج لاستبعاد المنتجات من التخطيط الرئيسي</span><span class="sxs-lookup"><span data-stu-id="fe1ef-169">Create a product lifecycle state to exclude products from Master planning</span></span>

