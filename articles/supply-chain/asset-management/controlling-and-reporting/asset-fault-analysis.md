---
title: تحليل أخطأ الأصول
description: يشرح هذا الموضوع تحليل أخطاء الأصول في إدارة الأصول.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 43772903f6845409cb33c7f2a13a049a3e9aa208
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652392"
---
# <a name="asset-fault-analysis"></a><span data-ttu-id="cf87e-103">تحليل أخطأ الأصول</span><span class="sxs-lookup"><span data-stu-id="cf87e-103">Asset fault analysis</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="cf87e-104">في إدارة الأصول، يمكنك تحليل تسجيلات أخطاء الأصول للحصول على نظرة عامة حول العدد الإجمالي للأخطاء المسجلة خلال فترة محددة.</span><span class="sxs-lookup"><span data-stu-id="cf87e-104">In Asset Management, you can analyze asset fault registrations to get an overview of the total number of faults registered during a specific period.</span></span> <span data-ttu-id="cf87e-105">يمكن تحليل تسجيلات الأخطاء من مناظير مختلفة، على سبيل المثال مع التركيز على الأصول أو أنواع الأصول أو مواقع العمل أو أعراض الأخطاء أو أنواع الأخطاء.</span><span class="sxs-lookup"><span data-stu-id="cf87e-105">Fault registrations can be analyzed from different perspectives, for example with focus on assets, asset types, functional locations, fault symptoms, or fault types.</span></span>

1. <span data-ttu-id="cf87e-106">انقر فوق **إدارة الأصول** > **استعلامات‬** > **أخطاء الأصول** > **تحليل أخطاء الأصول‬‏‎**.</span><span class="sxs-lookup"><span data-stu-id="cf87e-106">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault analysis**.</span></span>

2. <span data-ttu-id="cf87e-107">في مربع الحوار **حساب تحليل أخطاء الأصول**، يمكنك استخدام‏‎ حقل **المستوى** للإشارة إلى مستوى التفصيل الذي ترغب فيه في بنود أخطاء الأصول فيما يتعلق بمواقع العمل.</span><span class="sxs-lookup"><span data-stu-id="cf87e-107">In the **Asset fault analysis calculation** dialog, you can use the **Level** field to indicate how detailed you want the asset fault lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="cf87e-108">على سبيل المثال، إذا قمت بإدراج الرقم "1" في الحقل، وكان لديك بنية موقع عمل متعدد المستويات، فستظهر جميع بنود أخطاء الأصول لموقع عمل في المستوى العلوي، وبالتالي فإن الساعات على البند قد تُضاف من مواقع عمل موجودة في مستوى أدنى.‬</span><span class="sxs-lookup"><span data-stu-id="cf87e-108">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
        
    <span data-ttu-id="cf87e-109">إذا قمت بإدراج الرقم "0" في حقل **المستوى**، فسترى نتيجة مفصلة تعرض جميع بنود أخطاء الأصول على جميع مستويات مواقع العمل التي ترتبط بها.</span><span class="sxs-lookup"><span data-stu-id="cf87e-109">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault lines on all the functional location level to which they are related.</span></span>

3. <span data-ttu-id="cf87e-110">إذا كنت ترغب في تقييد البحث، فيمكنك تحديد أصول معينة وتواريخ وأسباب أخطاء معينة وعلاجاتها على علامة التبويب السريعة **السجلات المطلوب تضمينها‬**.</span><span class="sxs-lookup"><span data-stu-id="cf87e-110">If you want to limit the search, you can select specific assets, fault dates, fault causes, and fault remedies on the **Records to include** FastTab.</span></span>

4. <span data-ttu-id="cf87e-111">انقر فوق **موافق** لبدء الحساب.</span><span class="sxs-lookup"><span data-stu-id="cf87e-111">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="cf87e-112">على علامة التبويب **تحليل أخطاء الأصل‬** ، انقر فوق زر أو أكثر من أزرار **تجميع حسب‬** لعرض مستوى التفاصيل الذي تريد رؤيته.</span><span class="sxs-lookup"><span data-stu-id="cf87e-112">On the **Asset fault analysis** tab, click one or more **Group by** buttons to display the detail level you want to see.</span></span> <span data-ttu-id="cf87e-113">يتم تمييز الأزرار التي تم تنشيطها.</span><span class="sxs-lookup"><span data-stu-id="cf87e-113">Activated buttons are highlighted.</span></span> <span data-ttu-id="cf87e-114">يمكنك تنشيط الأزرار أو إلغاء تنشيطها بالنقر فوقها.</span><span class="sxs-lookup"><span data-stu-id="cf87e-114">Activate or deactivate buttons by clicking on them.</span></span>

6. <span data-ttu-id="cf87e-115">انقر فوق **تحديث الحسابات** لإظهار التحديدات على الشاشة.</span><span class="sxs-lookup"><span data-stu-id="cf87e-115">Click **Update calculations** to show your selections on the screen.</span></span> 

>[!NOTE]
><span data-ttu-id="cf87e-116">في كل مرة تقوم فيها بتنشيط أو إلغاء تنشيط زر **تجميع حسب** ، تذكر النقر فوق الزر **تحديث العمليات الحسابية** .</span><span class="sxs-lookup"><span data-stu-id="cf87e-116">Every time you activate or deactivate a **Group by** button, remember to click the **Update calculations** button.</span></span> <span data-ttu-id="cf87e-117">هذا الإجراء مطلوب بسبب معالجة كمية كبيرة من البيانات عندما تعيد حساب حساب احتمالية الخطأ.</span><span class="sxs-lookup"><span data-stu-id="cf87e-117">This is required because a large amount of data is processed as you are recalculating fault probability.</span></span>

## <a name="examples"></a><span data-ttu-id="cf87e-118">أمثلة</span><span class="sxs-lookup"><span data-stu-id="cf87e-118">Examples</span></span>

<span data-ttu-id="cf87e-119">هناك العديد من الطرق لتحليل تسجيلات الأخطاء.</span><span class="sxs-lookup"><span data-stu-id="cf87e-119">There are many ways to analyze fault registrations.</span></span> <span data-ttu-id="cf87e-120">يحتوي هذا القسم على خمسة أمثلة حول كيفية توفير تحديدات البيانات المختلفة لمزيد من المعلومات والتفاصيل عند تحليل تسجيلات أخطاء الأصل.</span><span class="sxs-lookup"><span data-stu-id="cf87e-120">This section has five examples of how different data selections can provide more insight and detail when analyzing asset fault registrations.</span></span>

### <a name="group-by-symptoms"></a><span data-ttu-id="cf87e-121">تجميع حسب الأعراض</span><span class="sxs-lookup"><span data-stu-id="cf87e-121">Group by symptoms</span></span>

<span data-ttu-id="cf87e-122">في لقطة الشاشة أدناه، تم تحديد زر **العَرَضْ‬** فقط.</span><span class="sxs-lookup"><span data-stu-id="cf87e-122">In the screenshot below, only the **Symptom** button is selected.</span></span>

- <span data-ttu-id="cf87e-123">تم إجراء تسجيلات الأخطاء على ثلاثة أعراض للخطأ: "تسرب الهواء" و"مصهر محترق" و"تعطل المعدات".</span><span class="sxs-lookup"><span data-stu-id="cf87e-123">Fault registrations have been made on three fault symptoms: "Air leak", "Blown fuse", and "Equipment jammed".</span></span>  
- <span data-ttu-id="cf87e-124">في عمود **الاحتمالية %**، تصل كافة النسب المئوية إلى 100%.</span><span class="sxs-lookup"><span data-stu-id="cf87e-124">In the **Probability %** column, all percentages add up to 100%.</span></span> <span data-ttu-id="cf87e-125">تستند الاحتمالية إلى كافة تسجيلات **الأعراض** في تحليل الخطأ هذا.</span><span class="sxs-lookup"><span data-stu-id="cf87e-125">Probability is based on all **Symptom** registrations in this fault analysis.</span></span>

![الشكل 1](media/06-controlling-and-reporting.png)

### <a name="group-by-symptoms-and-time-period"></a><span data-ttu-id="cf87e-127">تجميع حسب الأعراض والفترة الزمنية</span><span class="sxs-lookup"><span data-stu-id="cf87e-127">Group by symptoms and time period</span></span>

<span data-ttu-id="cf87e-128">في لقطة الشاشة أدناه، تمت إضافة **السنة** و**الشهر** لإظهار كيفية عرض تسجيلات الأخطاء أثناء فترة محددة.</span><span class="sxs-lookup"><span data-stu-id="cf87e-128">In the screenshot below, **Year** and **Month** are added to show how you can view fault registrations during a selected period.</span></span>

- <span data-ttu-id="cf87e-129">تظهر الآن أعراض الأخطاء كتسجيلات في السنة/الشهر.</span><span class="sxs-lookup"><span data-stu-id="cf87e-129">The fault symptoms are now shown as registrations per year/month.</span></span>  
- <span data-ttu-id="cf87e-130">في عمود **الاحتمالية %**، إذا قمت بإضافة كافة النسب المئوية لكل شهر، فإنها تصل إلى 100%.</span><span class="sxs-lookup"><span data-stu-id="cf87e-130">In the **Probability %** column, if you add all percentages for each month, they add up to 100%.</span></span> <span data-ttu-id="cf87e-131">تستند الاحتمالية إلى تسجيلات **الأعراض** في تحليل الخطأ هذا.</span><span class="sxs-lookup"><span data-stu-id="cf87e-131">Probability is based on the **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="cf87e-132">إذا كان لديك عدد كبير من البنود في أحد الأصول، ولكن نسبة مئوية كبيرة تبرز على أحد البنود، فقد يكون ذلك إشارة إلى عَرَض خطأ يجب فحصه عن كثب للعثور على طريقة لتحديد عدد التسجيلات لعَرَض الخطأ هذا.</span><span class="sxs-lookup"><span data-stu-id="cf87e-132">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![الشكل 2](media/07-controlling-and-reporting.png)

### <a name="group-by-multiple-symptoms-and-assets"></a><span data-ttu-id="cf87e-134">تجميع حسب الأعراض والأصول المتعددة</span><span class="sxs-lookup"><span data-stu-id="cf87e-134">Group by multiple symptoms and assets</span></span>

<span data-ttu-id="cf87e-135">يتم استخدام مجموعة الأصول ونوع الأصل كأساس للعمليات الحسابية التي تظهر في لقطات الشاشة الثلاث أدناه، والتي ستزداد في مستوى التفاصيل.</span><span class="sxs-lookup"><span data-stu-id="cf87e-135">The combination of assets and an asset type is used as a basis for the calculations shown in the three screenshots below, which will increase in detail level.</span></span>  

<span data-ttu-id="cf87e-136">بشكل عام، تحتوي الأزرار الموجودة في مجموعات جزء الإجراءات **تجميع حسب التاريخ** و**تجميع حسب الأصل** و**تجميع حسب موقع العمل**، بالإضافة إلى زر **الخطأ** (معرف الخطأ)، على فترات أو علاقات الأصول.</span><span class="sxs-lookup"><span data-stu-id="cf87e-136">Generally, the buttons in the **Group by date**, **Group by asset**, **Group by functional location** action pane groups, as well as the **Fault** button (Fault ID), contain periods or asset relations.</span></span> <span data-ttu-id="cf87e-137">تعتبر أزرار **العَرَض** و**المجال** و**النوع** و**السبب** و**العلاج** بمثابة تصنيفات تُستخدم في إدارة الأخطاء لتحليل تسجيلات أخطاء الأصول وتحديد المجالات التي تنطوي على مشاكل.</span><span class="sxs-lookup"><span data-stu-id="cf87e-137">The **Symptom**, **Area**, **Type**, **Cause**, and **Remedy** buttons are categorizations used in fault management to analyze asset fault registrations and pinpoint problem areas.</span></span>  

<span data-ttu-id="cf87e-138">**تجميع حسب العرض والأصل ونوع الأصل**</span><span class="sxs-lookup"><span data-stu-id="cf87e-138">**Group by symptom, asset, and asset type**</span></span>

<span data-ttu-id="cf87e-139">في لقطة الشاشة أدناه، تمت إضافة **الأصل** و**نوع الأصل** لتوفير المزيد من التفاصيل فيما يتعلق بتسجيلات الأخطاء.</span><span class="sxs-lookup"><span data-stu-id="cf87e-139">In the screenshot below, **Asset** and **Asset type** were added to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="cf87e-140">أعراض الأخطاء مقسمة الآن في مجموعة مكونة من **الأصل** / **نوع الأصل** / **العَرَض**.</span><span class="sxs-lookup"><span data-stu-id="cf87e-140">The fault symptoms are now split up in **Asset** / **Asset type** / **Symptom** combinations.</span></span>  
- <span data-ttu-id="cf87e-141">في عمود **الاحتمالية %**، إذا أضفت جميع النسب المئوية للمجموعة المكونة من **الأصل** / **نوع الأصل** / **العَرَض** على التوالي، فإن كل واحدة منها تصل إلى 100%.</span><span class="sxs-lookup"><span data-stu-id="cf87e-141">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** respectively, they each add up to 100%.</span></span> <span data-ttu-id="cf87e-142">تستند الاحتمالية إلى تسجيلات **الأعراض** في تحليل الخطأ هذا.</span><span class="sxs-lookup"><span data-stu-id="cf87e-142">Probability is based on **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="cf87e-143">إذا كان لديك عدد كبير من البنود في أحد الأصول، ولكن نسبة مئوية كبيرة تبرز على أحد البنود، فقد يكون ذلك إشارة إلى عَرَض خطأ يجب فحصه عن كثب للعثور على طريقة لتحديد عدد التسجيلات لعَرَض الخطأ هذا.</span><span class="sxs-lookup"><span data-stu-id="cf87e-143">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![الشكل 3](media/08-controlling-and-reporting.png)

<span data-ttu-id="cf87e-145">**تجميع حسب عرضين، والأصل، ونوع الأصل**</span><span class="sxs-lookup"><span data-stu-id="cf87e-145">**Group by two symptoms, asset, and asset type**</span></span>

<span data-ttu-id="cf87e-146">في لقطة الشاشة أدناه، تم إضافة **المجال** إلى **العَرَض** و**الأصل‏‎** و**نوع الأصل‏‎** لتوفير المزيد من التفاصيل فيما يتعلق بتسجيلات الأخطاء.</span><span class="sxs-lookup"><span data-stu-id="cf87e-146">In the screenshot below, **Area** was added to **Symptom**, **Asset**, and **Asset type** to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="cf87e-147">في عمود **الاحتمالية %**، إذا أضفت جميع النسب المئوية لمجموعة **الأصل** / **نوع الأصل** / **العَرَض** على أصل ما، فإن كل واحدة منها تصل إلى 100%.</span><span class="sxs-lookup"><span data-stu-id="cf87e-147">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="cf87e-148">تستند الاحتمالية إلى مجموعة **العَرَض** و**المجال** في تحليل الخطأ هذا.</span><span class="sxs-lookup"><span data-stu-id="cf87e-148">Probability is based on the combination of **Symptom** and **Area** in this fault analysis.</span></span> <span data-ttu-id="cf87e-149">إذا كان لديك عدد كبير من البنود في أحد الأصول، ولكن نسبة مئوية كبيرة تبرز على أحد البنود، فقد يكون ذلك إشارة إلى مجال خطأ يجب فحصه عن كثب للعثور على طريقة لتحديد عدد التسجيلات لمجال الخطأ هذا.</span><span class="sxs-lookup"><span data-stu-id="cf87e-149">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault area to examine more closely to find a way to limit the number of registrations for that fault area.</span></span>  

![الشكل 4](media/09-controlling-and-reporting.png)

<span data-ttu-id="cf87e-151">**تجميع حسب ثلاثة أعراض والأصل ونوع الأصل**</span><span class="sxs-lookup"><span data-stu-id="cf87e-151">**Group by three symptom, asset, and asset type**</span></span>

<span data-ttu-id="cf87e-152">في لقطة الشاشة أدناه، تمت إضافة **النوع**، ويُظهر هذا المثال الحساب الأكثر تفصيلاً.</span><span class="sxs-lookup"><span data-stu-id="cf87e-152">In the screenshot below, **Type** was added, and the most detailed calculation in this example is shown.</span></span>
 
- <span data-ttu-id="cf87e-153">في عمود **الاحتمالية %**، إذا أضفت جميع النسب المئوية لمجموعة **الأصل** / **نوع الأصل** / **العَرَض** على أصل ما، فإن كل واحدة منها تصل إلى 100%.</span><span class="sxs-lookup"><span data-stu-id="cf87e-153">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="cf87e-154">تستند الاحتمالية إلى مجموعة **العَرَض** و**المجال** و**النوع** في تحليل الخطأ هذا.</span><span class="sxs-lookup"><span data-stu-id="cf87e-154">Probability is based on the combination of **Symptom**, **Area**, and **Type** in this fault analysis.</span></span> <span data-ttu-id="cf87e-155">إذا كان لديك عدد كبير من البنود في أحد الأصول، ولكن نسبة مئوية كبيرة تبرز على أحد البنود، فقد يكون ذلك إشارة إلى نوع خطأ يجب فحصه عن كثب للعثور على طريقة لتحديد عدد التسجيلات على نوع الخطأ هذا.</span><span class="sxs-lookup"><span data-stu-id="cf87e-155">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault type to examine more closely to find a way to limit the number of registrations on that fault type.</span></span>

![الشكل 5](media/10-controlling-and-reporting.png)


>[!NOTE]
><span data-ttu-id="cf87e-157">للحصول على نظرة عامة على كافة تسجيلات الأخطاء التي تم إنشاؤها على أوامر العمل وطلبات الصيانة، انقر فوق **إدارة الأصول** > **استعلامات** > **خطأ الأصل** > **أخطاء الأصول**.</span><span class="sxs-lookup"><span data-stu-id="cf87e-157">For an overview of all fault registrations created on work orders and maintenance requests, click **Asset management** > **Inquiries** > **Asset fault** > **Asset faults**.</span></span> <span data-ttu-id="cf87e-158">في صفحة **أخطاء‏‎ الأصول**، حدد تسجيل خطأ الأصل، وقم بتوسيع الجزء **معلومات ذات صلة** لعرض المعلومات المتعلقة بأمر العمل أو طلب الصيانة ذي الصلة.</span><span class="sxs-lookup"><span data-stu-id="cf87e-158">On the **Asset faults** page, select an asset fault registration and expand the **Related information** pane to see information regarding the related work order or maintenance request.</span></span>

