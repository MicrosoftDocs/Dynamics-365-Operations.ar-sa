---
title: اختبارات إدارة الجودة
description: يوضح هذا الموضوع كيفيه إنشاء اختبارات يمكن استخدامها لأوامر الجودة في Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b88011f486b6582db4727b85d021868899c6abe1
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956533"
---
# <a name="quality-management-tests"></a><span data-ttu-id="1c7f2-103">اختبارات إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="1c7f2-103">Quality management tests</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1c7f2-104">يوضح هذا الموضوع كيفيه إنشاء اختبارات يمكن استخدامها لأوامر الجودة في Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1c7f2-104">This topic describes how to create tests that can be used for quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="1c7f2-105">يمكنك استخدام صفحة **الاختبارات** لتحديد الاختبارات الفردية وعرضها والتي تحدد ما إذا كانت منتجاتك تفي بمواصفات الجودة أم لا.</span><span class="sxs-lookup"><span data-stu-id="1c7f2-105">You use the **Tests** page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="1c7f2-106">ويمكنك تعيين واحد أو أكثر من الاختبارات الفردية لمجموعة اختبار.</span><span class="sxs-lookup"><span data-stu-id="1c7f2-106">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="1c7f2-107">وفي هذه الحالة، يمكنك أيضًا تحديد المعلومات الخاصة بالاختبار، مثل قيم القياس المقبولة.</span><span class="sxs-lookup"><span data-stu-id="1c7f2-107">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="1c7f2-108">يتم استخدام قيم القياس للاختبارات الكمية.</span><span class="sxs-lookup"><span data-stu-id="1c7f2-108">Measurement values are used for quantitative tests.</span></span> <span data-ttu-id="1c7f2-109">بالنسبة لاختبارات الجودة، يتم استخدام متغيرات الاختبار.</span><span class="sxs-lookup"><span data-stu-id="1c7f2-109">For qualitative tests, test variables are used.</span></span>

- <span data-ttu-id="1c7f2-110">بالنسبة للاختبارات الكمية، يتم تعيين حقل **النوع** إلى *عدد صحيح* أو *كسر*.</span><span class="sxs-lookup"><span data-stu-id="1c7f2-110">For quantitative tests, the **Type** field is set to *Integer* or *Fraction*.</span></span> <span data-ttu-id="1c7f2-111">يتم أيضًا تحديد وحدة قياس.</span><span class="sxs-lookup"><span data-stu-id="1c7f2-111">A unit of measure is also specified.</span></span> <span data-ttu-id="1c7f2-112">يتم التعبير عن مواصفات الجودة ونتائج الاختبارات كأرقام.</span><span class="sxs-lookup"><span data-stu-id="1c7f2-112">Quality specifications and test results are expressed as numbers.</span></span>
- <span data-ttu-id="1c7f2-113">بالنسبة لاختبارات الجودة، يتم تعيين حقل **النوع** إلى *خيار*.</span><span class="sxs-lookup"><span data-stu-id="1c7f2-113">For qualitative tests, the **Type** field is set to *Option*.</span></span> <span data-ttu-id="1c7f2-114">وتتطلب الاختبارات النوعية معلومات إضافية حول متغير الاختبار الذي يتم قياسه وخياراته العديدة.</span><span class="sxs-lookup"><span data-stu-id="1c7f2-114">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="1c7f2-115">يتم التعبير عن مواصفات الجودة ونتائج الاختبارات حسب النتيجة.</span><span class="sxs-lookup"><span data-stu-id="1c7f2-115">Quality specifications and test results are expressed according to an outcome.</span></span>

<span data-ttu-id="1c7f2-116">يمكنك اختياريا تعيين أداة اختبار للاختبار.</span><span class="sxs-lookup"><span data-stu-id="1c7f2-116">You can optionally assign a test instrument to a test.</span></span> <span data-ttu-id="1c7f2-117">ومع ذلك، لا تكون مستندات الاختبار مطلوبه لإنشاء واستخدام الاختبارات مع أوامر الجودة.</span><span class="sxs-lookup"><span data-stu-id="1c7f2-117">However, test instruments aren't required to create and use tests with quality orders.</span></span> <span data-ttu-id="1c7f2-118">لمزيد من المعلومات، راجع [مستندات اختبار إدارة الجودة](quality-test-instruments.md).</span><span class="sxs-lookup"><span data-stu-id="1c7f2-118">For more information, see [Quality management test instruments](quality-test-instruments.md).</span></span>

<span data-ttu-id="1c7f2-119">يمكنك أيضا تحديد وحده لاختبار بشكل اختياري، للاشاره إلى وحده القياس التي يتم تسجيل نتائج الاختبار بها.</span><span class="sxs-lookup"><span data-stu-id="1c7f2-119">You can also optionally specify a unit for a test, to indicate the unit of measure that test results are recorded in.</span></span> <span data-ttu-id="1c7f2-120">علي سبيل المثال، قد يتضمن اختبار درجه الحرارة وحده اما درجات فهرنهيت أو درجات مئوية.</span><span class="sxs-lookup"><span data-stu-id="1c7f2-120">For example, a test for temperature might include a unit of either degrees Fahrenheit or degrees Celsius.</span></span>

## <a name="example-of-a-test"></a><span data-ttu-id="1c7f2-121">مثال لاختبار</span><span class="sxs-lookup"><span data-stu-id="1c7f2-121">Example of a test</span></span>

<span data-ttu-id="1c7f2-122">تقوم إحدى شركات التصنيع بإجراء اختبارين على المادة التي تم شراؤها وهما اختبار كمي حول جودة المادة واختبار نوعي حول حدوث تلف في التعبئة.</span><span class="sxs-lookup"><span data-stu-id="1c7f2-122">A manufacturing company performs two tests on purchased material: a quantitative test for material quality and a qualitative test for packaging damage.</span></span> <span data-ttu-id="1c7f2-123">وتحدد الشركة معلومات إضافية حول الاختبار النوعي لتحديد متغير الاختبار (مثل التعبئة التالفة) ونتائجه.</span><span class="sxs-lookup"><span data-stu-id="1c7f2-123">The company specifies additional information about the qualitative test to define the test variable (for example, damaged packaging) and its outcomes.</span></span> <span data-ttu-id="1c7f2-124">تستخدم الشركة صفحة **مجموعات الاختبار** لتعيين الاختبارين لمجموعة اختبارات وتحديد المعلومات الخاصة بالاختبار.</span><span class="sxs-lookup"><span data-stu-id="1c7f2-124">The company uses the **Test groups** page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="1c7f2-125">يتم تعيين مجموعة الاختبار إلى أمر الجودة بحيث يمكن للشركة تقديم تقرير بنتائج الاختبار لكلا الاختبارين.</span><span class="sxs-lookup"><span data-stu-id="1c7f2-125">The test group is assigned to a quality order so that the company can report test results for the two tests.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="1c7f2-126">إنشاء اختبار</span><span class="sxs-lookup"><span data-stu-id="1c7f2-126">Create a test</span></span>

<span data-ttu-id="1c7f2-127">اتبع هذه الخطوات لإنشاء اختبار.</span><span class="sxs-lookup"><span data-stu-id="1c7f2-127">Follow these steps to create a test.</span></span>

1. <span data-ttu-id="1c7f2-128">انتقل إلى **إدارة المخزون \> الإعداد \> مراقبة الجودة \> الاختبارات**.</span><span class="sxs-lookup"><span data-stu-id="1c7f2-128">Go to **Inventory management \> Setup \> Quality control \> Tests**.</span></span>
1. <span data-ttu-id="1c7f2-129">في جزء الإجراءات، حدد **جديد** لإضافة صف إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="1c7f2-129">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="1c7f2-130">ثم قم بتعيين الحقول التالية للصف الجديد:</span><span class="sxs-lookup"><span data-stu-id="1c7f2-130">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="1c7f2-131">**الاختبار** – أدخل معرفا فريدا أو اسما للاختبار.</span><span class="sxs-lookup"><span data-stu-id="1c7f2-131">**Test** – Enter a unique ID or name for the test.</span></span>
    - <span data-ttu-id="1c7f2-132">**الوصف** - أدخل وصفًا مفصلاً للاختبار.</span><span class="sxs-lookup"><span data-stu-id="1c7f2-132">**Description** – Enter a detailed description of the test.</span></span>
    - <span data-ttu-id="1c7f2-133">**النوع** - حدد نوع النتائج التي ينتج عنها الاختبار.</span><span class="sxs-lookup"><span data-stu-id="1c7f2-133">**Type** – Select the type of results that the test produces.</span></span> <span data-ttu-id="1c7f2-134">للحصول علي اختبارات الكمية، حدد *الكسر* أو *العدد الصحيح*.</span><span class="sxs-lookup"><span data-stu-id="1c7f2-134">For quantitative tests, select *Fraction* or *Integer*.</span></span> <span data-ttu-id="1c7f2-135">بالنسبة لاختبارات الجودة، حدد *خيار*.</span><span class="sxs-lookup"><span data-stu-id="1c7f2-135">For qualitative tests, select *Option*.</span></span>
    - <span data-ttu-id="1c7f2-136">**مستند الاختبار** – حدد [مستند الاختبار](quality-test-instruments.md) الذي يجب استخدامه للاختبار.</span><span class="sxs-lookup"><span data-stu-id="1c7f2-136">**Test instrument** – Select a [test instrument](quality-test-instruments.md) that should be used for the test.</span></span>
    - <span data-ttu-id="1c7f2-137">**الوحدة** – في حالة تحديد *الكسر* أو *العدد الصحيح* في حقل **النوع** (أي، إذا كان الاختبار اختبارًا كميًا)، فحدد وحدة القياس التي يجب تسجيل نتائج الاختبار بها.</span><span class="sxs-lookup"><span data-stu-id="1c7f2-137">**Unit** – If you selected *Fraction* or *Integer* in the **Type** field (that is, if the test is a quantitative test), select the unit of measure that test results should be recorded in.</span></span>

1. <span data-ttu-id="1c7f2-138">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1c7f2-138">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="1c7f2-139">بعد ان تقوم بحفظ اختبار، لا يمكنك تحرير حقل **النوع** في الشبكة.</span><span class="sxs-lookup"><span data-stu-id="1c7f2-139">After you save a test, you can no longer edit the **Type** field in the grid.</span></span> <span data-ttu-id="1c7f2-140">إذا كان يجب عليك تغيير نوع نتائج الاختبار التي سيتم تسجيلها للاختبار، فحدد **تغيير نوع اختبار الجودة** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="1c7f2-140">If you must change the type of test results that will be recorded for a test, select **Change quality test type** on the Action Pane.</span></span> <span data-ttu-id="1c7f2-141">في مربع الحوار **تغيير نوع اختبار الجودة**، قم بتعيين حقل **النوع الجديد** إلى النو المطلوب، ثم حدد **موافق** لإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="1c7f2-141">In the **Change quality test type** dialog box, set the **New type** field to the desired type, and then select **OK** to close the dialog box.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1c7f2-142">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="1c7f2-142">Additional resources</span></span>

- [<span data-ttu-id="1c7f2-143">أدوات اختبار إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="1c7f2-143">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="1c7f2-144">مجموعات اختبارات إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="1c7f2-144">Quality management test groups</span></span>](quality-test-groups.md)
- [<span data-ttu-id="1c7f2-145">متغيرات اختبار إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="1c7f2-145">Quality management test variables</span></span>](quality-test-variables.md)
- [<span data-ttu-id="1c7f2-146">عمليات اقتران الجودة</span><span class="sxs-lookup"><span data-stu-id="1c7f2-146">Quality associations</span></span>](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
