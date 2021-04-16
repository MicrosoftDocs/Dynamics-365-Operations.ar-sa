---
title: إعدادات التغطية
description: يوفر هذا الموضوع معلومات حول إعدادات التغطية التي تستخدمها الجدولة الرئيسية لحساب متطلبات الصنف.
author: roxanadiaconu
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard, ReqItemTableSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 987d487622740eb5e8bcdda9056c43627006555a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816546"
---
# <a name="coverage-settings"></a><span data-ttu-id="f5347-103">إعدادات التغطية</span><span class="sxs-lookup"><span data-stu-id="f5347-103">Coverage settings</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f5347-104">تستخدم الجدولة الرئيسية إعدادات التغطية لحساب متطلبات الصنف.</span><span class="sxs-lookup"><span data-stu-id="f5347-104">Master scheduling uses coverage settings to calculate item requirements.</span></span>

<span data-ttu-id="f5347-105">يمكنك تحديد إعدادات التغطية بعدة طرق:</span><span class="sxs-lookup"><span data-stu-id="f5347-105">You can specify coverage settings in several ways:</span></span>

- <span data-ttu-id="f5347-106">حدد إعدادات التغطية لمجموعة تغطية.</span><span class="sxs-lookup"><span data-stu-id="f5347-106">Specify coverage settings for a coverage group.</span></span>

    <span data-ttu-id="f5347-107">يمكنك إنشاء مجموعة تغطية تحتوي على إعدادات لكل المنتجات المرتبطة بمجموعة التغطية.</span><span class="sxs-lookup"><span data-stu-id="f5347-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="f5347-108">لإنشاء مجموعة تغطية، انتقل إلى **التخطيط الرئيسي &gt; الإعداد &gt; التغطية &gt; مجموعات التغطية**.</span><span class="sxs-lookup"><span data-stu-id="f5347-108">To create a coverage group, go to **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups**.</span></span> <span data-ttu-id="f5347-109">يمكن ربط مجموعة تغطية لأحد المنتجات.</span><span class="sxs-lookup"><span data-stu-id="f5347-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="f5347-110">إذا كان الارتباط خاصًا بموقع أو مستودع أو بُعد منتج، فاستخدم حقل **مجموعة التغطية** في صفحة **تغطية الصنف**.</span><span class="sxs-lookup"><span data-stu-id="f5347-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="f5347-111">إذا كان الارتباط عامًا، وبغض النظر عن أبعاد المنتج، فاستخدم حقل **مجموعة التغطية** في علامة التبويب السريعة **خطة** في صفحة **تفاصيل المنتج**.</span><span class="sxs-lookup"><span data-stu-id="f5347-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** field on the **Plan** FastTab of the **Product details** page.</span></span> <span data-ttu-id="f5347-112">بشكل افتراضي، إذا لم تربط مجموعة تغطية بمنتج، يستخدم التخطيط الرئيسي مجموعة التغطية العامة المحددة في صفحة **معلمات التخطيط الرئيسي**.</span><span class="sxs-lookup"><span data-stu-id="f5347-112">By default, if you don't link a coverage group to a product, master planning uses the general coverage group that is specified on the **Master planning parameters** page.</span></span>

- <span data-ttu-id="f5347-113">تحديد إعدادات التغطية لمنتج.</span><span class="sxs-lookup"><span data-stu-id="f5347-113">Specify coverage settings for a product.</span></span>

    <span data-ttu-id="f5347-114">يمكنك إنشاء إعدادات التغطية لمنتج محدد.</span><span class="sxs-lookup"><span data-stu-id="f5347-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="f5347-115">انتقل إلى **إدارة معلومات المنتج‬ &gt; المنتجات &gt; المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="f5347-115">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="f5347-116">حدد المنتج، ثم في جزء الإجراءات، علامة التبويب **خطة**، في مجموعة **التغطية‏‎**، حدد **تغطية الصنف** لفتح صفحة **تغطية الصنف**.</span><span class="sxs-lookup"><span data-stu-id="f5347-116">Select the product, and then, on the Action Pane, on the **Plan** tab, in the **Coverage** group, select **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="f5347-117">إذا تم ربط المنتج بمجموعة تغطية بالفعل، فيمكنك تجاوز إعدادات مجموعة التغطية باستخدام حقل **التجاوز**.</span><span class="sxs-lookup"><span data-stu-id="f5347-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="f5347-118">تأخذ إعدادات التغطية في صفحة **تغطية الصنف** الأسبقية على الإعدادات في صفحة **مجموعة التغطية**.</span><span class="sxs-lookup"><span data-stu-id="f5347-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

- <span data-ttu-id="f5347-119">تحديد إعدادات التغطية لمنتج باستخدام معالج.</span><span class="sxs-lookup"><span data-stu-id="f5347-119">Specify coverage settings for a product by using a wizard.</span></span>

    <span data-ttu-id="f5347-120">يقوم المعالج بإرشادك خطوة بخطوة خلال عملية إعداد معلمات تغطية الصنف الرئيسية.‬</span><span class="sxs-lookup"><span data-stu-id="f5347-120">The wizard guides you step by step through the process of setting up the primary item coverage parameters.</span></span> <span data-ttu-id="f5347-121">في صفحة **تغطية الصنف**، على جزء الإجراءات، حدد **معالج** لفتح **معالج تغطية الصنف**.</span><span class="sxs-lookup"><span data-stu-id="f5347-121">On the **Item coverage** page, on the Action Pane, select **Wizard** to open the **Item Coverage Wizard**.</span></span>

- <span data-ttu-id="f5347-122">تحديد إعدادات تغطية لمجموعة أبعاد.</span><span class="sxs-lookup"><span data-stu-id="f5347-122">Specify coverage settings for a dimension group.</span></span>

    <span data-ttu-id="f5347-123">انتقل إلى **إدارة معلومات المنتج‬ &gt; المنتجات &gt; المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="f5347-123">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="f5347-124">في صفحة **تفاصيل المنتجات الصادرة‬**، في علامة التبويب السريعة **عام**، في القسم **الإدارة**، حدد الارتباط في الحقل **مجموعة أبعاد التخزين**.</span><span class="sxs-lookup"><span data-stu-id="f5347-124">On the **Released product details** page, on the **General** FastTab, in the **Administration** section, select the link in the **Storage dimension group** field.</span></span> <span data-ttu-id="f5347-125">في صفحة **مجموعات أبعاد التخزين**، حدد خانة الاختيار **خطة التغطية حسب البعد** لإنشاء إعدادات التغطية لبُعد في مجموعة أبعاد التخزين.</span><span class="sxs-lookup"><span data-stu-id="f5347-125">On the **Storage dimension groups** page, select the **Coverage plan by dimension** check box to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="f5347-126">يجب تحديد الحقل **خطة التغطية حسب البُعد** لجميع أبعاد المنتج، مثل التكوين واللون والحجم والنمط.</span><span class="sxs-lookup"><span data-stu-id="f5347-126">The **Coverage plan by dimension** field must be selected for all product dimensions, such as configuration, color, size, and style.</span></span>


## <a name="coverage-codes"></a><span data-ttu-id="f5347-127">أكواد التغطية</span><span class="sxs-lookup"><span data-stu-id="f5347-127">Coverage codes</span></span>

<span data-ttu-id="f5347-128">يمكن تكوين التخطيط الرئيسي لاستخدام أساليب تزويد مختلفة.</span><span class="sxs-lookup"><span data-stu-id="f5347-128">Master planning can be configured to use different replenishment methods.</span></span> <span data-ttu-id="f5347-129">تعتبر أساليب التزويد أو أساليب تغيير حجم الدفعة التقنيات التي يستخدمها النظام لتحديد حجم الدفعة للأصناف التي تم شراؤها أو إنتاجها.</span><span class="sxs-lookup"><span data-stu-id="f5347-129">The replenishment methods or lot-sizing methods are the techniques used by the system to determine the batch size for purchased or produced items.</span></span> 

<span data-ttu-id="f5347-130">يتم تعيين أحد أكواد التغطية التالية لكل أسلوب تزويد:</span><span class="sxs-lookup"><span data-stu-id="f5347-130">Each replenishment method is assigned one of the following coverage codes:</span></span>

- <span data-ttu-id="f5347-131">**يدوي** -أسلوب تغيير حجم الدفعة حيث لا يقترح النظام أوامر الشراء أو التحويل أو الإنتاج الخاصة بالصنف.</span><span class="sxs-lookup"><span data-stu-id="f5347-131">**Manual** - The lot-sizing method where the system does not suggest purchased, transfer, or production orders for the item.</span></span> <span data-ttu-id="f5347-132">سيكون مخطط الصنف مسؤولاً عن إنشاء الأوامر المطلوبة لتزويد الصنف.</span><span class="sxs-lookup"><span data-stu-id="f5347-132">The planner for the item will be in charge of creating the required orders for the replenishment of the item.</span></span>
- <span data-ttu-id="f5347-133">**لكل متطلب** - أسلوب تغيير حجم الدفعة حيث يقوم النظام بإنشاء أمر شراء أو تحويل أو أمر إنتاج مخطط لكل واحد من المتطلبات الخاصة بالصنف.</span><span class="sxs-lookup"><span data-stu-id="f5347-133">**Per requirement** - The lot-sizing method in which the system creates a planned purchase, transfer, or production order per requirement for the item.</span></span> <span data-ttu-id="f5347-134">ويستخدم هذا بشكل عام في الأصناف المكلفة ذات طلب متقطع عليها.</span><span class="sxs-lookup"><span data-stu-id="f5347-134">This is generally used for expensive items with intermittent demand.</span></span>  
- <span data-ttu-id="f5347-135">**لكل فتره** -أسلوب تغيير حجم الدفعة الذي يضم كافة الطلبات لفترة ما في أمر واحد للصنف.</span><span class="sxs-lookup"><span data-stu-id="f5347-135">**Per period** - The lot-sizing method that combines all the demand for a period into one order for the item.</span></span> <span data-ttu-id="f5347-136">سيتم التخطيط للأمر لأول يوم من الفترة، وستستوفي كميته صافي المتطلبات خلال الفترة التي تم تعيينها.</span><span class="sxs-lookup"><span data-stu-id="f5347-136">The order will be planned for the first day of the period and its quantity will fulfill the net requirements during the established period.</span></span> <span data-ttu-id="f5347-137">تبدأ الفترة مع الطلب الأول للصنف وتغطي المدة المحددة.</span><span class="sxs-lookup"><span data-stu-id="f5347-137">The period starts with the first demand of the item and covers the defined length in time.</span></span> <span data-ttu-id="f5347-138">ستبدأ الفترة التالية مع المتطلبات التالية للصنف.</span><span class="sxs-lookup"><span data-stu-id="f5347-138">The next period will start with the next requirements of the item.</span></span>
- <span data-ttu-id="f5347-139">**الحد الأدنى/الحد الأقصى** -أسلوب تغيير حجم الدفعة الذي يحتوي على تزويد المخزون حتى مستوى معين عندما يكون التوقع الفعلي اقل من الحد المعين.</span><span class="sxs-lookup"><span data-stu-id="f5347-139">**Min/Max** - The lot-sizing method that contains the replenishment of inventory up to a certain level when the predicted on-hand is below a threshold.</span></span> <span data-ttu-id="f5347-140">ستكون كمية التزويد الفرق بين الحد الأقصى لمستوى المخزون والمستوى الفعلي المتوقع.</span><span class="sxs-lookup"><span data-stu-id="f5347-140">The replenishment quantity will be the difference between the maximum level and the predicted on-hand level.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="f5347-141">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="f5347-141">Additional resources</span></span>

[<span data-ttu-id="f5347-142">نظرة عامة على الخطط الرئيسية</span><span class="sxs-lookup"><span data-stu-id="f5347-142">Master plans overview</span></span>](master-plans.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]