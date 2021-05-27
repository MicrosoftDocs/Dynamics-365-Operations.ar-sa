---
title: متغيرات اختبار إدارة الجودة
description: يوضح هذا الموضوع كيفيه إنشاء متغيرات الاختبار التي يمكن استخدامها للاختبارات النوعية علي أوامر الجودة في Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: b5102d09f5762a390d6fd3aadafcb2ed23820982
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021698"
---
# <a name="quality-management-test-variables"></a><span data-ttu-id="8015c-103">متغيرات اختبار إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="8015c-103">Quality management test variables</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8015c-104">يوضح هذا الموضوع كيفيه إنشاء متغيرات الاختبار التي يمكن استخدامها للاختبارات النوعية علي أوامر الجودة في Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="8015c-104">This topic describes how to create test variables that can be used for qualitative tests on quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="8015c-105">بالنسبة لكل اختبار نوعي يتم تحديده في صفحة **الاختبارات**، يجب عليك تحديد متغير الاختبار ونتائجها المحتملة (النتائج).</span><span class="sxs-lookup"><span data-stu-id="8015c-105">For every qualitative test that is defined on the **Tests** page, you must define a test variable and its possible outcomes (results).</span></span> <span data-ttu-id="8015c-106">(بالنسبة لاختبارات الجودة، يتم تعيين حقل **النوع** في صفحة **الاختبارات** إلى *الخيار*.)</span><span class="sxs-lookup"><span data-stu-id="8015c-106">(For qualitative tests, the **Type** field on the **Tests** page is set to *Option*.)</span></span>

<span data-ttu-id="8015c-107">يمكنك استخدام صفحة **متغيرات الاختبارات** لإعداد وتحرير وعرض النتائج المحتملة لمتغير اختبار مرتبط باختبار نوعي.</span><span class="sxs-lookup"><span data-stu-id="8015c-107">You use the **Test variables** page to set up, edit, and view the possible outcomes for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="8015c-108">لكل نتيجة، تقوم بتعيين حالة نتيجة لأي منهما *نجاح* أو *فشل* للإشارة إلى ما إذا كان الاختبار قد تم اجتيازه أو فشله عند تحديد هذه النتيجة كنتيجة اختبار.</span><span class="sxs-lookup"><span data-stu-id="8015c-108">For each outcome, you assign an outcome status of either *Pass* or *Fail* to indicate whether the test is passed or failed when that outcome is selected as a test result.</span></span> <span data-ttu-id="8015c-109">يمكنك استخدام صفحة **مجموعات الاختبارات** لتعيين متغير اختبار والنتيجة الافتراضية لاختبار جودة فردي.</span><span class="sxs-lookup"><span data-stu-id="8015c-109">You use the **Test groups** page to assign a test variable and a default outcome for it to an individual qualitative test.</span></span>

<span data-ttu-id="8015c-110">لكل متغير اختبار، نوصي بتحديد اثنين علي الأقل من النتيجتين التاليتين: الأول الذي له حاله نتيجة *النجاح* والاخر له حاله نتيجة *فاشله*.</span><span class="sxs-lookup"><span data-stu-id="8015c-110">For every test variable, we recommend that you define at least two outcomes: one that has an outcome status of *Pass* and one that has an outcome status of *Fail*.</span></span> <span data-ttu-id="8015c-111">لا يوجد حد لإجمالي عدد المتغيرات أو النتائج التي يمكن تعريفها.</span><span class="sxs-lookup"><span data-stu-id="8015c-111">There is no limit on the total number of variables or outcomes that can be defined.</span></span> <span data-ttu-id="8015c-112">بالاضافه إلى ذلك، يمكن لاختبارات متعددة استخدام نفس متغيرات الاختبار لتسجيل النتائج.</span><span class="sxs-lookup"><span data-stu-id="8015c-112">Additionally, multiple tests can use the same test variables to record results.</span></span>

## <a name="examples-of-test-variables"></a><span data-ttu-id="8015c-113">أمثله علي متغيرات الاختبار</span><span class="sxs-lookup"><span data-stu-id="8015c-113">Examples of test variables</span></span>

### <a name="example-1"></a><span data-ttu-id="8015c-114">مثال1</span><span class="sxs-lookup"><span data-stu-id="8015c-114">Example 1</span></span>

<span data-ttu-id="8015c-115">تقوم أحدي الشركات المصنعة باجراء اختبارين علي المواد المصنعة.</span><span class="sxs-lookup"><span data-stu-id="8015c-115">A manufacturing company performs two tests on manufactured materials.</span></span> <span data-ttu-id="8015c-116">في أحد الاختبارات، يرتبط مستوى الأس الهيدروجيني بشريط ألوان.</span><span class="sxs-lookup"><span data-stu-id="8015c-116">In one test, the pH level is associated with a color strip.</span></span> <span data-ttu-id="8015c-117">تكون مستويات الأس الهيدروجيني المقبولة بألوان أفتح، ومستويات الأس الهيدروجيني غير المقبولة بألوان أغمق.</span><span class="sxs-lookup"><span data-stu-id="8015c-117">Acceptable pH levels are in lighter colors, and unacceptable pH levels are in darker colors.</span></span> <span data-ttu-id="8015c-118">في اختبار آخر، يتم إجراء عمليات فحص بصرية متعددة، ويستخدم عمال الجودة حكمهم لتحديد ما إذا كان العنصر يمر أو يفشل في الفحص البصري.</span><span class="sxs-lookup"><span data-stu-id="8015c-118">In another test, multiple visual inspections are performed, and quality workers use their judgement to determine whether the item passes or fails the visual inspection.</span></span>

### <a name="example-2"></a><span data-ttu-id="8015c-119">مثال2</span><span class="sxs-lookup"><span data-stu-id="8015c-119">Example 2</span></span>

<span data-ttu-id="8015c-120">شركة تصنيع تنتج حلوى، تقوم بإجراء اختبار فحص للمنتج المنتهي.</span><span class="sxs-lookup"><span data-stu-id="8015c-120">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="8015c-121">ويشتمل اختبار الفحص هذا على متغيرات متعددة.</span><span class="sxs-lookup"><span data-stu-id="8015c-121">This inspection test has several variables.</span></span> <span data-ttu-id="8015c-122">ومن بين هذه المتغيرات الطعم، وتكون النتائج المحتملة لهذا المتغير جيدة وسيئة.</span><span class="sxs-lookup"><span data-stu-id="8015c-122">One variable is taste, and the possible outcomes for it are good and bad.</span></span> <span data-ttu-id="8015c-123">أما المتغير الثاني فهو اللون، وتكون النتائج المحتملة له داكن جدًا أو فاتح جدًا أو صحيح.</span><span class="sxs-lookup"><span data-stu-id="8015c-123">A second variable is color, and the possible outcomes for it are too dark, too light, and correct.</span></span>

## <a name="create-a-test-variable"></a><span data-ttu-id="8015c-124">إنشاء متغير اختبار</span><span class="sxs-lookup"><span data-stu-id="8015c-124">Create a test variable</span></span>

<span data-ttu-id="8015c-125">اتبع هذه الخطوات لإنشاء متغير اختبار.</span><span class="sxs-lookup"><span data-stu-id="8015c-125">Follow these steps to create a test variable.</span></span>

1. <span data-ttu-id="8015c-126">انتقل إلى **إدارة المخزون \> الإعداد \> مراقبة الجودة \> متغيرات الاختبار**.</span><span class="sxs-lookup"><span data-stu-id="8015c-126">Go to **Inventory management \> Setup \> Quality control \> Test variables**.</span></span>
1. <span data-ttu-id="8015c-127">في جزء الإجراءات، حدد **جديد** لإضافة صف إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="8015c-127">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="8015c-128">ثم قم بتعيين الحقول التالية للصف الجديد:</span><span class="sxs-lookup"><span data-stu-id="8015c-128">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="8015c-129">**المتغير** – ادخل معرفا فريدا أو اسما للمتغير.</span><span class="sxs-lookup"><span data-stu-id="8015c-129">**Variable** – Enter a unique ID or name for the variable.</span></span>
    - <span data-ttu-id="8015c-130">**الوصف** - أدخل وصفًا مفصلاً للمتغير.</span><span class="sxs-lookup"><span data-stu-id="8015c-130">**Description** – Enter a detailed description of the variable.</span></span>

1. <span data-ttu-id="8015c-131">في حين ان الصف الجديد لا يزال محددا، حدد **النتائج** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="8015c-131">While the new row is still selected, select **Outcomes** on the Action Pane.</span></span>
1. <span data-ttu-id="8015c-132">في صفحة **نتائج متغيرات الاختبارات**، في جزء الإجراءات، حدد **جديد** لإضافة صف إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="8015c-132">On the **Test variable outcomes** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="8015c-133">ثم قم بتعيين الحقول التالية للصف الجديد:</span><span class="sxs-lookup"><span data-stu-id="8015c-133">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="8015c-134">**النتيجة** – ادخل معرفا فريدا أو اسما للنتيجة.</span><span class="sxs-lookup"><span data-stu-id="8015c-134">**Outcome** – Enter a unique ID or name for the outcome.</span></span>
    - <span data-ttu-id="8015c-135">**الوصف** - أدخل وصفًا مفصلاً للنتيجة.</span><span class="sxs-lookup"><span data-stu-id="8015c-135">**Description** – Enter a detailed description of the outcome.</span></span>
    - <span data-ttu-id="8015c-136">**حالة النتيجة** – حدد إما *نجاح* أو *فشل* للإشارة إلى ما إذا كان الاختبار قد تم اجتيازه أو فشله عند تحديد هذه النتيجة كنتيجة اختبار.</span><span class="sxs-lookup"><span data-stu-id="8015c-136">**Outcome status** – Select either *Pass* or *Fail* to indicate whether the test is passed or failed when the outcome is selected as a test result.</span></span>

1. <span data-ttu-id="8015c-137">كرر الخطوة السابقة لكل نتيجة اضافيه.</span><span class="sxs-lookup"><span data-stu-id="8015c-137">Repeat the previous step for each additional outcome.</span></span> <span data-ttu-id="8015c-138">تأكد من أن نتيجة واحدة على الأقل لها حالة نتيجة *نجاح* وواحدة على الأقل له حالة نتيجة *فشل*.</span><span class="sxs-lookup"><span data-stu-id="8015c-138">Make sure that at least one outcome has an outcome status of *Pass* and at least one has an outcome status of *Fail*.</span></span>
1. <span data-ttu-id="8015c-139">قم بإغلاق الصفحات.</span><span class="sxs-lookup"><span data-stu-id="8015c-139">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8015c-140">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="8015c-140">Additional resources</span></span>

- [<span data-ttu-id="8015c-141">أدوات اختبار إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="8015c-141">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="8015c-142">اختبارات إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="8015c-142">Quality management tests</span></span>](quality-tests.md)
- [<span data-ttu-id="8015c-143">مجموعات اختبارات إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="8015c-143">Quality management test groups</span></span>](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
