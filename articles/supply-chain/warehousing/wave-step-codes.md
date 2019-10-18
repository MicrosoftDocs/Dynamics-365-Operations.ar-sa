---
title: رموز خطوة الموجة
description: يقدم هذا الموضوع نظرة عامة حول أكواد خطوة الموجة وكيفية استخدامها.
author: josaw1
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0f89c6098db9e2e3a9aa4ee3666e4b9ae608f054
ms.sourcegitcommit: d8f1135cdbc2deca70bc4b2805a0519253c9a31f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/06/2019
ms.locfileid: "1992347"
---
# <a name="wave-step-codes"></a><span data-ttu-id="b9476-103">رموز خطوة الموجة</span><span class="sxs-lookup"><span data-stu-id="b9476-103">Wave step codes</span></span>

[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]

## <a name="about-wave-step-codes"></a><span data-ttu-id="b9476-104">حول أكواد خطوة الموجة</span><span class="sxs-lookup"><span data-stu-id="b9476-104">About wave step codes</span></span>

<span data-ttu-id="b9476-105">أكواد خطوة الموجة هي أكواد يمكن للمستخدمين إعدادها واستخدامها لربط مثيلات معينة من أساليب الموجة بقالب مقابل.</span><span class="sxs-lookup"><span data-stu-id="b9476-105">Wave step codes are codes that users can set up and use to link specific instances of wave methods to a corresponding template.</span></span> <span data-ttu-id="b9476-106">وتتضمن القوالب قوالب للتزويد والتعبئة في حاويات وطباعة التسمية وإنشاء الحمل والفرز.</span><span class="sxs-lookup"><span data-stu-id="b9476-106">The templates include templates for replenishment, containerization, label printing, load building, and sorting.</span></span>

<span data-ttu-id="b9476-107">عندما لا يتم استخدام أكواد خطوة الموجة، يجب أن يقوم المستخدمون بإدخال نص حر للإشارة إلى قالب محدد من مثيل أسلوب الموجة.</span><span class="sxs-lookup"><span data-stu-id="b9476-107">When wave step codes aren't used, users must enter free text to reference a specific template from the wave method instance.</span></span> <span data-ttu-id="b9476-108">يكون النص الحر عرضة للخطأ، لأن المستخدمين يجب أن يتأكدوا من أن نص خطوة الموجة الذي أضافوه لأسلوب خطوة موجة معين في قالب موجة يطابق تمامًا نص خطوة الموجة في القالب المستهدف.</span><span class="sxs-lookup"><span data-stu-id="b9476-108">Free text is prone to error, because users must make sure that the wave step text that they add for a specific wave step method in a wave template exactly matches the wave step text in the target template.</span></span>

<span data-ttu-id="b9476-109">يتم إعداد أكواد خطوة الموجة لنوع خطوة موجة معينة في صفحة منفصلة.</span><span class="sxs-lookup"><span data-stu-id="b9476-109">Wave step codes for a specific wave step type are set up on a separate page.</span></span> <span data-ttu-id="b9476-110">لكل مثيل من مثيلات أسلوب خطوة الموجة في قالب موجة يتطلب كود خطوة موجة، يجب تحديد كود خطوة الموجة في قائمة منسدلة.</span><span class="sxs-lookup"><span data-stu-id="b9476-110">For every wave step method instance in a wave template that requires a wave step code, the wave step code must be selected in a drop-down list.</span></span> <span data-ttu-id="b9476-111">يؤدي التحديد في القائمة المنسدلة إلى استبدال الإدخال النصي الحر ويساعد على تقليل خطر وتأثير الخطأ البشري.</span><span class="sxs-lookup"><span data-stu-id="b9476-111">Selection in a drop-down list replaces free text entry and helps reduce the risk and impact of human error.</span></span> <span data-ttu-id="b9476-112">تُستخدم أكواد الإعداد لربط أسلوب خطوة الموجة في قالب موجة بقالب هدف للأسلوب.</span><span class="sxs-lookup"><span data-stu-id="b9476-112">Setup codes are used to link a wave step method in a wave template to a target template for the method.</span></span>

> [!NOTE]
> <span data-ttu-id="b9476-113">استخدام ميزة أكواد خطوة الموجة اختياري، ويكون التنفيذ لكل كيان قانوني.</span><span class="sxs-lookup"><span data-stu-id="b9476-113">Use of the wave step codes feature is optional, and uptake is per legal entity.</span></span> <span data-ttu-id="b9476-114">وبالتالي، في حالة استخدم كيان قانوني محدد هذه الميزة، تتم ترقية كافة أكواد خطوة الموجة الحالية في الكيان القانوني إلى البنية الجديدة.</span><span class="sxs-lookup"><span data-stu-id="b9476-114">Therefore, if a specific legal entity uses the feature, all existing wave step codes in that legal entity are upgraded to the new structure.</span></span>

## <a name="setup-demo"></a><span data-ttu-id="b9476-115">إعداد العرض التوضيحي</span><span class="sxs-lookup"><span data-stu-id="b9476-115">Setup demo</span></span> 

<span data-ttu-id="b9476-116">بالنسبة إلى هذا العرض التوضيحي، يجب تثبيت بيانات العرض التوضيحي، ويجب استخدام شركة بيانات العرض التوضيحي **USMF‎**.</span><span class="sxs-lookup"><span data-stu-id="b9476-116">For this demo, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="enable-wave-step-codes"></a><span data-ttu-id="b9476-117">تمكين رموز خطوة الموجة</span><span class="sxs-lookup"><span data-stu-id="b9476-117">Enable wave step codes</span></span>

<span data-ttu-id="b9476-118">اتبع الخطوات التالية لتشغيل ميزة أكواد خطوة الموجة.</span><span class="sxs-lookup"><span data-stu-id="b9476-118">Follow these steps to turn on the wave step codes feature.</span></span>

1. <span data-ttu-id="b9476-119">انتقل إلى **إدارة المستودعات‬\> إعداد‬ \> محددات إدارة المستودعات**.</span><span class="sxs-lookup"><span data-stu-id="b9476-119">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
2. <span data-ttu-id="b9476-120">على علامة التبويب **عام**، على علامة التبويب السريعة **معالجة الموجة‬**، عيّن الخيار **تمكين أكواد خطوة الموجة‬** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="b9476-120">On the **General** tab, on the **Wave processing** FastTab, set the **Enable wave step codes** option to **Yes**.</span></span>

<span data-ttu-id="b9476-121">تتم ترقية جميع النصوص الحرة لخطوة الموجة الحالية إلى البنية الجديدة.</span><span class="sxs-lookup"><span data-stu-id="b9476-121">All existing wave step free texts are upgraded to the new structure.</span></span> <span data-ttu-id="b9476-122">بعد اكتمال الترقية لكيان قانوني، لم يعد الخيار **تمكين أكواد خطوة الموجة** متوفرًا على صفحة **‏‫محددات إدارة المستودعات**.</span><span class="sxs-lookup"><span data-stu-id="b9476-122">After this upgrade is completed for a legal entity, the **Enable wave step codes** option is no longer available on the **Warehouse management parameters** page.</span></span>

<span data-ttu-id="b9476-123">يتم إجراء التحقق من الصحة أثناء الترقية، وفي حالة فشل الترقية، تظهر رسالة خطأ.</span><span class="sxs-lookup"><span data-stu-id="b9476-123">Validations are done during the upgrade, and if the upgrade fails, you receive an error message.</span></span> <span data-ttu-id="b9476-124">قد تفشل عملية الترقية بسبب التعارضات التالية:</span><span class="sxs-lookup"><span data-stu-id="b9476-124">An upgrade might fail because of the following conflicts:</span></span>

- <span data-ttu-id="b9476-125">وجود نصوص حرة مكررة لخطوة الموجة.</span><span class="sxs-lookup"><span data-stu-id="b9476-125">Duplicate wave step free texts exist.</span></span>
- <span data-ttu-id="b9476-126">وجود تخصيصات.</span><span class="sxs-lookup"><span data-stu-id="b9476-126">Customizations exist.</span></span>
- <span data-ttu-id="b9476-127">لا يُطابق النص الحر لخطوة الموجة المقترن بمثيل أسلوب خطوة الموجة نوع القالب المتوقع.</span><span class="sxs-lookup"><span data-stu-id="b9476-127">A wave step free text that is associated with a wave step method instance doesn't match the expected template type.</span></span>

<span data-ttu-id="b9476-128">بعد حل إيه تعارضات تم التعرف علهيا أثناء التحقق من الصحة، يمكنك إعادة تشغيل عملية الترقية.</span><span class="sxs-lookup"><span data-stu-id="b9476-128">After you've resolved any conflicts that are identified during the validations, you can rerun the upgrade process.</span></span>

<span data-ttu-id="b9476-129">عند نجاح الترقية، تصبح صفحة **أكواد خطوة الموجة** (**إدارة المستودعات \> إعداد \> أمواج \>أكواد خطوة الموجة**) متوفرة.</span><span class="sxs-lookup"><span data-stu-id="b9476-129">When the upgrade succeeds, the **Wave step codes** page (**Warehouse management \> Setup \> Waves \> Wave step codes**) becomes available.</span></span> <span data-ttu-id="b9476-130">تسرد هذه الصفحة أكواد خطوة الموجة التي تمت ترقيتها عند تشغيل ميزة أكواد خطوة الموجة.</span><span class="sxs-lookup"><span data-stu-id="b9476-130">This page lists the wave step codes that were upgraded when the wave step codes feature was turned on.</span></span>

### <a name="create-new-wave-step-codes"></a><span data-ttu-id="b9476-131">إنشاء أكواد جديدة لخطوة الموجة</span><span class="sxs-lookup"><span data-stu-id="b9476-131">Create new wave step codes</span></span>

<span data-ttu-id="b9476-132">يمكنك استخدام صفحة **أكواد خطوة الموجة** لإنشاء أكواد خطوة الموجة وحذفها.</span><span class="sxs-lookup"><span data-stu-id="b9476-132">You can use the **Wave step codes** page to create and delete wave step codes.</span></span>

<span data-ttu-id="b9476-133">يجب أن يكون كل كود جديد من أكواد خطوة الموجة ومعرّفه المقترن به فريدًا عبر كافة أنواع خطوات الموجة، ويجب تحديدهما لنوع خطوة موجة معين.</span><span class="sxs-lookup"><span data-stu-id="b9476-133">Every new wave step code and its associated ID must be unique across all wave step types, and they must be defined for a specific wave step type.</span></span>

### <a name="apply-wave-step-codes"></a><span data-ttu-id="b9476-134">تطبيق أكواد خطوة الموجة</span><span class="sxs-lookup"><span data-stu-id="b9476-134">Apply wave step codes</span></span>

<span data-ttu-id="b9476-135">بعد أن قمت بتحديد أكواد خطوة الموجة المناسبة، يمكن تطبيقها على أساليب عملية الموجة.</span><span class="sxs-lookup"><span data-stu-id="b9476-135">After you've defined the appropriate wave step codes, they can be applied to the wave process methods.</span></span>

<span data-ttu-id="b9476-136">لتطبيق أكواد خطوة الموجة، انتقل إلى القالب الهدف المناسب.</span><span class="sxs-lookup"><span data-stu-id="b9476-136">To apply wave step codes, go to the appropriate target template.</span></span> <span data-ttu-id="b9476-137">فيما يلي القوالب الهدف التي تم تعيين لها أكواد خطوه موجة للإشارة إلى:</span><span class="sxs-lookup"><span data-stu-id="b9476-137">Here are the target templates that the wave step codes are designated to point to:</span></span>

- <span data-ttu-id="b9476-138">**قوالب التزويد:** إدارة المستودعات \> الإعداد \> التزويد \> قوالب التزويد.</span><span class="sxs-lookup"><span data-stu-id="b9476-138">**Replenishment templates:** Warehouse management \> Setup \> Replenishment \> Replenishment templates</span></span>
- <span data-ttu-id="b9476-139">**تحميل قوالب الإنشاء**: إدارة المستودعات \> الإعداد \> تحميل \>‎تحميل قوالب الإنشاء</span><span class="sxs-lookup"><span data-stu-id="b9476-139">**Load build templates:** Warehouse management \> Setup \> Load \> Load build templates</span></span>
- <span data-ttu-id="b9476-140">**فرز القوالب:** إدارة المستودعات \> الإعداد \> ‏‫التعبئة‬ \> قوالب الفرز الصادرة</span><span class="sxs-lookup"><span data-stu-id="b9476-140">**Sort templates:** Warehouse management \> Setup \> Packing \> Outbound sorting templates</span></span>
- <span data-ttu-id="b9476-141">**قوالب ‏‫التعبئة في حاويات:** إدارة المستودعات \> الإعداد \> الحاويات \> ‏‫قوالب إنشاء الحاوية‬</span><span class="sxs-lookup"><span data-stu-id="b9476-141">**Containerization templates:** Warehouse management \> Setup \> Containers \> Container build templates</span></span>
- <span data-ttu-id="b9476-142">**قوالب طباعة التسمية:** إدارة المستودعات \> الإعداد \> ‏‫توجيه المستند‬ \> قوالب تسمية الموجة</span><span class="sxs-lookup"><span data-stu-id="b9476-142">**Label printing templates:** Warehouse management \> Setup \> Document routing \> Wave label templates</span></span>

<span data-ttu-id="b9476-143">يتم تطبيق القوالب الموجودة في هذه القائمة عند الإشاره إليها من طريقة معالجة الموجة التي تم تحديدها في قالب موجة.</span><span class="sxs-lookup"><span data-stu-id="b9476-143">The templates in this list are applied when they are referenced from a wave process method that is selected in a wave template.</span></span> <span data-ttu-id="b9476-144">عندما يُطابق كود خطوة الموجة بطريقة معالجة موجة في قالب موجة كود خطوة الموجة في أحد أنواع القوالب، يتم تطبيق القالب.</span><span class="sxs-lookup"><span data-stu-id="b9476-144">When the wave step code on a wave process method in a wave template matches the wave step code in one of the templates types, the template is applied.</span></span>

### <a name="sample-scenario"></a><span data-ttu-id="b9476-145">سيناريو كمثال</span><span class="sxs-lookup"><span data-stu-id="b9476-145">Sample scenario</span></span>

<span data-ttu-id="b9476-146">يساعد الإجراء التالي على ضمان أن قالب التزويد الذي قمت بإنشائه سيتم تطبيقه على قالب الموجة.</span><span class="sxs-lookup"><span data-stu-id="b9476-146">The following procedure helps guarantee that the replenishment template that you created will be applied for the wave template.</span></span>

1. <span data-ttu-id="b9476-147">انتقل إلى **إدارة المستودعات \> الإعداد \> الموجة \> أكواد خطوة الموجة**، وقم بإنشاء كود خطوة موجة للنوع **تزويد**.</span><span class="sxs-lookup"><span data-stu-id="b9476-147">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**, and create a wave step code for the **Replenishment** type.</span></span>
2. <span data-ttu-id="b9476-148">انتقل إلى **إدارة المستودعات \> الإعداد \> التزويد \> قوالب التزويد**، وقم بإنشاء قالب تزويد.</span><span class="sxs-lookup"><span data-stu-id="b9476-148">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**, and create a replenishment template.</span></span>
3. <span data-ttu-id="b9476-149">في قالب التزويد، حدد كود خطوة الموجة التي قمت بإنشائه لنوع **التزويد**.</span><span class="sxs-lookup"><span data-stu-id="b9476-149">In the replenishment template, select the wave step code that you created for the **Replenishment** type.</span></span>
4. <span data-ttu-id="b9476-150">انتقل إلى **إدارة المستودعات \> الإعداد \> الموجات \> قوالب الموجات**، وحدد قالب الموجة الذي ترغب في استخدامه.</span><span class="sxs-lookup"><span data-stu-id="b9476-150">Go to **Warehouse management \> Setup \> Waves \> Wave templates**, and select the wave template that you intend to use.</span></span>
5. <span data-ttu-id="b9476-151">في القالب، على علامة التبويب السريعة **الطرق**، حدد طريقة **التزويد**.</span><span class="sxs-lookup"><span data-stu-id="b9476-151">In the template, on the **Methods** FastTab, select the **Replenishment** method.</span></span>
6. <span data-ttu-id="b9476-152">في حقل **كود خطوة الموجة**، حدد كود خطوة الموجة التي حددتها في قالب التزويد.</span><span class="sxs-lookup"><span data-stu-id="b9476-152">In the **Wave step code** field, select the wave step code that you selected in the replenishment template.</span></span>
