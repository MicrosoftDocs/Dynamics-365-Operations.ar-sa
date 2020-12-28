---
title: رموز خطوة الموجة
description: يقدم هذا الموضوع نظرة عامة حول أكواد خطوة الموجة وكيفية استخدامها.
author: josaw1
manager: tfehr
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveStepCode, WHSReplenishmentTemplates, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9332e45f7213ed815e4417969b617256778598db
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4421777"
---
# <a name="wave-step-codes"></a><span data-ttu-id="be827-103">رموز خطوة الموجة</span><span class="sxs-lookup"><span data-stu-id="be827-103">Wave step codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be827-104">أكواد خطوة الموجة هي أكواد يمكن للمستخدمين إعدادها واستخدامها لربط مثيلات معينة من أساليب الموجة بقالب مقابل.</span><span class="sxs-lookup"><span data-stu-id="be827-104">Wave step codes are codes that users can set up and use to link specific instances of wave methods to a corresponding template.</span></span> <span data-ttu-id="be827-105">وتتضمن القوالب قوالب للتزويد والتعبئة في حاويات وطباعة التسمية وإنشاء الحمل والفرز.</span><span class="sxs-lookup"><span data-stu-id="be827-105">The templates include templates for replenishment, containerization, label printing, load building, and sorting.</span></span>

<span data-ttu-id="be827-106">عندما لا يتم استخدام أكواد خطوة الموجة، يجب أن يقوم المستخدمون بإدخال نص حر للإشارة إلى قالب محدد من مثيل أسلوب الموجة.</span><span class="sxs-lookup"><span data-stu-id="be827-106">When wave step codes aren't used, users must enter free text to reference a specific template from the wave method instance.</span></span> <span data-ttu-id="be827-107">يكون النص الحر عرضة للخطأ، لأن المستخدمين يجب أن يتأكدوا من أن نص خطوة الموجة الذي أضافوه لأسلوب خطوة موجة معين في قالب موجة يطابق تمامًا نص خطوة الموجة في القالب المستهدف.</span><span class="sxs-lookup"><span data-stu-id="be827-107">Free text is prone to errors because users must make sure that the wave step text that they add for a specific wave step method in a wave template exactly matches the wave step text in the target template.</span></span>

<span data-ttu-id="be827-108">يتم إعداد أكواد خطوة الموجة لنوع خطوة موجة معينة في صفحة منفصلة.</span><span class="sxs-lookup"><span data-stu-id="be827-108">Wave step codes for a specific wave step type are set up on a separate page.</span></span> <span data-ttu-id="be827-109">لكل مثيل من مثيلات أسلوب خطوة الموجة في قالب موجة يتطلب كود خطوة موجة، يجب تحديد كود خطوة الموجة في قائمة منسدلة.</span><span class="sxs-lookup"><span data-stu-id="be827-109">For every wave step method instance in a wave template that requires a wave step code, the wave step code must be selected in a drop-down list.</span></span> <span data-ttu-id="be827-110">يؤدي التحديد في القائمة المنسدلة إلى استبدال الإدخال النصي الحر ويساعد على تقليل خطر وتأثير الخطأ البشري.</span><span class="sxs-lookup"><span data-stu-id="be827-110">Selection in a drop-down list replaces free text entry and helps reduce the risk and impact of human error.</span></span> <span data-ttu-id="be827-111">تُستخدم أكواد الإعداد لربط أسلوب خطوة الموجة في قالب موجة بقالب هدف للأسلوب.</span><span class="sxs-lookup"><span data-stu-id="be827-111">Setup codes are used to link a wave step method in a wave template to a target template for the method.</span></span>

> [!NOTE]
> <span data-ttu-id="be827-112">يُعد استخدام ميزة أكواد خطوة الموجة اختياريًا.</span><span class="sxs-lookup"><span data-stu-id="be827-112">Use of the wave step codes feature is optional.</span></span> <span data-ttu-id="be827-113">وهي ممكنة على نطاق المنظمة لجميع الكيانات القانونية.</span><span class="sxs-lookup"><span data-stu-id="be827-113">It is enabled organization-wide for all legal entities.</span></span>

## <a name="setup-demo"></a><span data-ttu-id="be827-114">إعداد العرض التوضيحي</span><span class="sxs-lookup"><span data-stu-id="be827-114">Setup demo</span></span> 

<span data-ttu-id="be827-115">بالنسبة إلى هذا العرض التوضيحي، يجب تثبيت بيانات العرض التوضيحي، ويجب استخدام شركة بيانات العرض التوضيحي **USMF‎**.</span><span class="sxs-lookup"><span data-stu-id="be827-115">For this demo, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="enable-wave-step-codes"></a><span data-ttu-id="be827-116">تمكين رموز خطوة الموجة</span><span class="sxs-lookup"><span data-stu-id="be827-116">Enable wave step codes</span></span>

<span data-ttu-id="be827-117">اتبع الخطوات التالية لتشغيل ميزة أكواد خطوة الموجة.</span><span class="sxs-lookup"><span data-stu-id="be827-117">Follow these steps to turn on the wave step codes feature.</span></span>

1. <span data-ttu-id="be827-118">انتقل إلى **إدارة الميزات**.</span><span class="sxs-lookup"><span data-stu-id="be827-118">Go to **Feature Management**.</span></span>
2. <span data-ttu-id="be827-119">حدد لتمكين الميزة المسماة **كود خطوة الموجة على مستوى المؤسسة**.</span><span class="sxs-lookup"><span data-stu-id="be827-119">Select to enable the feature called **Organization-wide Wave Step Code**.</span></span>

<span data-ttu-id="be827-120">تتم ترقية جميع النصوص الحرة لخطوة الموجة الحالية في كافة الكيانات القانونية إلى البنية الجديدة.</span><span class="sxs-lookup"><span data-stu-id="be827-120">All existing wave step free texts in all legal entities are upgraded to the new structure.</span></span> <span data-ttu-id="be827-121">بعد إكمال هذه الترقية لكافة الكيانات القانونية، يتم تمكين الميزة.</span><span class="sxs-lookup"><span data-stu-id="be827-121">After this upgrade is completed for all legal entities, then the feature is enabled.</span></span> <span data-ttu-id="be827-122">إذا تعذر تمكين الميزة لكيان قانوني واحد أو أكثر، فلن يتم تمكين الميزة لأية كيانات قانونية.</span><span class="sxs-lookup"><span data-stu-id="be827-122">If the feature cannot be enabled for one or more legal entities, then the feature is not enabled for any legal entities.</span></span>

<span data-ttu-id="be827-123">أثناء التمكين، يتم التحقق من صحة الأمر أثناء ترقية البيانات.</span><span class="sxs-lookup"><span data-stu-id="be827-123">During the enablement, validations are done during the data upgrade.</span></span> <span data-ttu-id="be827-124">في حالة فشل الترقية، فإنك ستتلقي رسالة خطأ.</span><span class="sxs-lookup"><span data-stu-id="be827-124">If the upgrade fails, you receive an error message.</span></span> <span data-ttu-id="be827-125">قد تفشل عملية الترقية بسبب التعارضات التالية:</span><span class="sxs-lookup"><span data-stu-id="be827-125">An upgrade might fail because of the following conflicts:</span></span>

- <span data-ttu-id="be827-126">وجود نصوص حرة مكررة لخطوة الموجة.</span><span class="sxs-lookup"><span data-stu-id="be827-126">Duplicate wave step free texts exist.</span></span>
- <span data-ttu-id="be827-127">وجود تخصيصات.</span><span class="sxs-lookup"><span data-stu-id="be827-127">Customizations exist.</span></span>
- <span data-ttu-id="be827-128">لا يُطابق النص الحر لخطوة الموجة المقترن بمثيل أسلوب خطوة الموجة نوع القالب المتوقع.</span><span class="sxs-lookup"><span data-stu-id="be827-128">A wave step free text that is associated with a wave step method instance doesn't match the expected template type.</span></span>

<span data-ttu-id="be827-129">بعد حل أية تعارضات تم التعرف علهيا أثناء التحقق من الصحة، يمكنك إعادة محاولة تمكين الميزة.</span><span class="sxs-lookup"><span data-stu-id="be827-129">After you've resolved any conflicts that are identified during the validations, you can retry to enable the feature.</span></span>

<span data-ttu-id="be827-130">عند نجاح تميكن الميزة، تصبح صفحة **أكواد خطوة الموجة** (**إدارة المستودعات \> إعداد \> أمواج \> أكواد خطوة الموجة**) متوفرة.</span><span class="sxs-lookup"><span data-stu-id="be827-130">When the feature has been enabled, the **Wave step codes** page (**Warehouse management \> Setup \> Waves \> Wave step codes**) becomes available.</span></span> <span data-ttu-id="be827-131">تسرد هذه الصفحة أكواد خطوة الموجة التي تمت ترقيتها عند تميكن ميزة كود خطوة الموجة.</span><span class="sxs-lookup"><span data-stu-id="be827-131">This page lists the wave step codes that were upgraded when the Organization-wide Wave Step Code feature was enabled.</span></span>

### <a name="create-new-wave-step-codes"></a><span data-ttu-id="be827-132">إنشاء أكواد جديدة لخطوة الموجة</span><span class="sxs-lookup"><span data-stu-id="be827-132">Create new wave step codes</span></span>

<span data-ttu-id="be827-133">يمكنك استخدام صفحة **أكواد خطوة الموجة** لإنشاء أكواد خطوة الموجة وحذفها.</span><span class="sxs-lookup"><span data-stu-id="be827-133">You can use the **Wave step codes** page to create and delete wave step codes.</span></span>

<span data-ttu-id="be827-134">يجب أن يكون كل كود جديد من أكواد خطوة الموجة ومعرّفه المقترن به فريدًا عبر كافة أنواع خطوات الموجة، ويجب تحديدهما لنوع خطوة موجة معين.</span><span class="sxs-lookup"><span data-stu-id="be827-134">Every new wave step code and its associated ID must be unique across all wave step types, and they must be defined for a specific wave step type.</span></span>

### <a name="apply-wave-step-codes"></a><span data-ttu-id="be827-135">تطبيق أكواد خطوة الموجة</span><span class="sxs-lookup"><span data-stu-id="be827-135">Apply wave step codes</span></span>

<span data-ttu-id="be827-136">بعد أن قمت بتحديد أكواد خطوة الموجة المناسبة، يمكن تطبيقها على أساليب عملية الموجة.</span><span class="sxs-lookup"><span data-stu-id="be827-136">After you've defined the appropriate wave step codes, they can be applied to the wave process methods.</span></span>

<span data-ttu-id="be827-137">لتطبيق أكواد خطوة الموجة، انتقل إلى القالب الهدف المناسب.</span><span class="sxs-lookup"><span data-stu-id="be827-137">To apply wave step codes, go to the appropriate target template.</span></span> <span data-ttu-id="be827-138">فيما يلي القوالب الهدف التي تم تعيين لها أكواد خطوه موجة للإشارة إلى:</span><span class="sxs-lookup"><span data-stu-id="be827-138">Here are the target templates that the wave step codes are designated to point to:</span></span>

- <span data-ttu-id="be827-139">**قوالب التزويد:** إدارة المستودعات \> الإعداد \> التزويد \> قوالب التزويد.</span><span class="sxs-lookup"><span data-stu-id="be827-139">**Replenishment templates:** Warehouse management \> Setup \> Replenishment \> Replenishment templates</span></span>
- <span data-ttu-id="be827-140">**تحميل قوالب الإنشاء**: إدارة المستودعات \> الإعداد \> تحميل \>‎تحميل قوالب الإنشاء</span><span class="sxs-lookup"><span data-stu-id="be827-140">**Load build templates:** Warehouse management \> Setup \> Load \> Load build templates</span></span>
- <span data-ttu-id="be827-141">**فرز القوالب:** إدارة المستودعات \> الإعداد \> ‏‫التعبئة‬ \> قوالب الفرز الصادرة</span><span class="sxs-lookup"><span data-stu-id="be827-141">**Sort templates:** Warehouse management \> Setup \> Packing \> Outbound sorting templates</span></span>
- <span data-ttu-id="be827-142">**قوالب ‏‫التعبئة في حاويات:** إدارة المستودعات \> الإعداد \> الحاويات \> ‏‫قوالب إنشاء الحاوية‬</span><span class="sxs-lookup"><span data-stu-id="be827-142">**Containerization templates:** Warehouse management \> Setup \> Containers \> Container build templates</span></span>
- <span data-ttu-id="be827-143">**قوالب طباعة التسمية:** إدارة المستودعات \> الإعداد \> ‏‫توجيه المستند‬ \> قوالب تسمية الموجة</span><span class="sxs-lookup"><span data-stu-id="be827-143">**Label printing templates:** Warehouse management \> Setup \> Document routing \> Wave label templates</span></span>

<span data-ttu-id="be827-144">يتم تطبيق القوالب الموجودة في هذه القائمة عند الإشاره إليها من طريقة معالجة الموجة التي تم تحديدها في قالب موجة.</span><span class="sxs-lookup"><span data-stu-id="be827-144">The templates in this list are applied when they are referenced from a wave process method that is selected in a wave template.</span></span> <span data-ttu-id="be827-145">عندما يُطابق كود خطوة الموجة بطريقة معالجة موجة في قالب موجة كود خطوة الموجة في أحد أنواع القوالب، يتم تطبيق القالب.</span><span class="sxs-lookup"><span data-stu-id="be827-145">When the wave step code on a wave process method in a wave template matches the wave step code in one of the templates types, the template is applied.</span></span>

### <a name="sample-scenario"></a><span data-ttu-id="be827-146">سيناريو كمثال</span><span class="sxs-lookup"><span data-stu-id="be827-146">Sample scenario</span></span>

<span data-ttu-id="be827-147">يساعد الإجراء التالي على ضمان أن قالب التزويد الذي قمت بإنشائه سيتم تطبيقه على قالب الموجة.</span><span class="sxs-lookup"><span data-stu-id="be827-147">The following procedure helps guarantee that the replenishment template that you created will be applied for the wave template.</span></span>

1. <span data-ttu-id="be827-148">انتقل إلى **إدارة المستودعات \> الإعداد \> الموجة \> أكواد خطوة الموجة**، وقم بإنشاء كود خطوة موجة للنوع **تزويد**.</span><span class="sxs-lookup"><span data-stu-id="be827-148">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**, and create a wave step code for the **Replenishment** type.</span></span>
2. <span data-ttu-id="be827-149">انتقل إلى **إدارة المستودعات \> الإعداد \> التزويد \> قوالب التزويد**، وقم بإنشاء قالب تزويد.</span><span class="sxs-lookup"><span data-stu-id="be827-149">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**, and create a replenishment template.</span></span>
3. <span data-ttu-id="be827-150">في قالب التزويد، حدد كود خطوة الموجة التي قمت بإنشائه لنوع **التزويد**.</span><span class="sxs-lookup"><span data-stu-id="be827-150">In the replenishment template, select the wave step code that you created for the **Replenishment** type.</span></span>
4. <span data-ttu-id="be827-151">انتقل إلى **إدارة المستودعات \> الإعداد \> الموجات \> قوالب الموجات**، وحدد قالب الموجة الذي ترغب في استخدامه.</span><span class="sxs-lookup"><span data-stu-id="be827-151">Go to **Warehouse management \> Setup \> Waves \> Wave templates**, and select the wave template that you intend to use.</span></span>
5. <span data-ttu-id="be827-152">في القالب، على علامة التبويب السريعة **الطرق**، حدد طريقة **التزويد**.</span><span class="sxs-lookup"><span data-stu-id="be827-152">In the template, on the **Methods** FastTab, select the **Replenishment** method.</span></span>
6. <span data-ttu-id="be827-153">في حقل **كود خطوة الموجة**، حدد كود خطوة الموجة التي حددتها في قالب التزويد.</span><span class="sxs-lookup"><span data-stu-id="be827-153">In the **Wave step code** field, select the wave step code that you selected in the replenishment template.</span></span>

<span data-ttu-id="be827-154">قم بتنفيذ هذه الخطوات لكل كيان قانوني.</span><span class="sxs-lookup"><span data-stu-id="be827-154">You perform these steps for each legal entity.</span></span>
