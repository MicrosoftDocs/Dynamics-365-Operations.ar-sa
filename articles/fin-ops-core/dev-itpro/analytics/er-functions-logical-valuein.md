---
title: VALUEIN ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية VALUEIN (ER).
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d0df97234df41d11897473dea4e85354e82d36ec
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041689"
---
# <span data-ttu-id="eec85-103"><a name="VALUEIN">VALUEIN ER وظيفة</a></span><span class="sxs-lookup"><span data-stu-id="eec85-103"><a name="VALUEIN">VALUEIN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eec85-104">تُحدد الوظيفة `VALUEIN` ما إذا كان الإدخال المُحدد يطابق أي قيمة عنصر مُحدد في القائمة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="eec85-104">The `VALUEIN` function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="eec85-105">يقوم بإرجاع قيمة *منطقية* **TRUE** إذا كان الإدخال المُحدد يُطابق نتيجة تشغيل التعبير المُحدد لسجل واحد على الأقل من القائمة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="eec85-105">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="eec85-106">وبخلاف ذلك، تُرجع قيمة *منطقية* لـ **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="eec85-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="eec85-107">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="eec85-107">Syntax</span></span>

```vb
VALUEIN (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="eec85-108">الوسائط</span><span class="sxs-lookup"><span data-stu-id="eec85-108">Arguments</span></span>

<span data-ttu-id="eec85-109">`input`: *الحقل*</span><span class="sxs-lookup"><span data-stu-id="eec85-109">`input`: *Field*</span></span>

<span data-ttu-id="eec85-110">مسار صالح لعنصر مصدر بيانات من نوع *قائمة السجلات*.</span><span class="sxs-lookup"><span data-stu-id="eec85-110">The valid path of an item of a data source of the *Record list* type.</span></span> <span data-ttu-id="eec85-111">وستتم مطابقة قيمة هذا الصنف.</span><span class="sxs-lookup"><span data-stu-id="eec85-111">The value of this item will be matched.</span></span>

<span data-ttu-id="eec85-112">`list`: *قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="eec85-112">`list`: *Record list*</span></span>

<span data-ttu-id="eec85-113">مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.</span><span class="sxs-lookup"><span data-stu-id="eec85-113">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="eec85-114">`list item expression`: *منطقي*</span><span class="sxs-lookup"><span data-stu-id="eec85-114">`list item expression`: *Boolean*</span></span>

<span data-ttu-id="eec85-115">تعبير شرطي صالح يشير إما إلى أو يحتوي على حقل واحد من القائمة المحددة يجب استخدامه للمطابقة.</span><span class="sxs-lookup"><span data-stu-id="eec85-115">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="eec85-116">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="eec85-116">Return values</span></span>

<span data-ttu-id="eec85-117">*منطقي*</span><span class="sxs-lookup"><span data-stu-id="eec85-117">*Boolean*</span></span>

<span data-ttu-id="eec85-118">القيمة *المنطقية* الناتجة.</span><span class="sxs-lookup"><span data-stu-id="eec85-118">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="eec85-119">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="eec85-119">Usage notes</span></span>

<span data-ttu-id="eec85-120">بشكل عام، يتم تحويل الوظيفة `VALUEIN` إلى مجموعة من شروط **OR**.</span><span class="sxs-lookup"><span data-stu-id="eec85-120">In general, the `VALUEIN` function is translated to a set of **OR** conditions.</span></span>

```vb
(input = list.item1.value) OR (input = list.item2.value) OR …
```

<span data-ttu-id="eec85-121">في بعض الحالات، يُمكن تحويله إلى عبارة SQL لقاعدة بيانات باستخدام عامل التشغيل `EXISTS JOIN`.</span><span class="sxs-lookup"><span data-stu-id="eec85-121">In some cases, it can be translated to a database SQL statement by using the `EXISTS JOIN` operator.</span></span>

## <a name="example-1"></a><span data-ttu-id="eec85-122">مثال1</span><span class="sxs-lookup"><span data-stu-id="eec85-122">Example 1</span></span>

<span data-ttu-id="eec85-123">في تعيين النموذج الخاص بك، يجب عليك تحديد مصدر البيانات **القائمة** من النوع *الحقل المحسوب*.</span><span class="sxs-lookup"><span data-stu-id="eec85-123">In your model mapping, you define the **List** data source of the *Calculated field* type.</span></span> <span data-ttu-id="eec85-124">يحتوي مصدر البيانات هذا على التعبير `SPLIT ("a,b,c", ",")`.</span><span class="sxs-lookup"><span data-stu-id="eec85-124">This data source contains the expression `SPLIT ("a,b,c", ",")`.</span></span>

<span data-ttu-id="eec85-125">عندما يتم استدعاء مصدر بيانات، إذا تم تكوينه كتعبير `VALUEIN ("B", List, List.Value)`، يُرجع **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="eec85-125">When a data source is called, if it has been configured as the `VALUEIN ("B", List, List.Value)` expression, it returns **TRUE**.</span></span> <span data-ttu-id="eec85-126">في هذه الحالة، يتم تحويل الوظيفة `VALUEIN` إلى مجموعة الشروط التالية: `(("B" = "a") or ("B" = "b") or ("B" = "c"))` ، حيث تساوي `("B" = "b")` **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="eec85-126">In this case, the `VALUEIN` function is translated to the following set of conditions: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, where `("B" = "b")` equals **TRUE**.</span></span>

<span data-ttu-id="eec85-127">عندما يتم استدعاء مصدر بيانات، إذا تم تكوينه كتعبير `VALUEIN ("B", List, LEFT(List.Value, 0))`، يُرجع **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="eec85-127">When a data source is called, if it has been configured as the `VALUEIN ("B", List, LEFT(List.Value, 0))` expression, it returns **FALSE**.</span></span> <span data-ttu-id="eec85-128">في هذه الحالة، تتم ترجمة الوظيفة `VALUEIN` إلى الشرط التالي: `("B" = "")`، والذي لا يساوي **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="eec85-128">In this case, the `VALUEIN` function is translated to the following condition: `("B" = "")`, which doesn't equal **TRUE**.</span></span>

<span data-ttu-id="eec85-129">الحد الأقصى لعدد الأحرف في نص شرط هو 32768 حرفًا.</span><span class="sxs-lookup"><span data-stu-id="eec85-129">The upper limit for the number of characters in the text of such a condition is 32,768 characters.</span></span> <span data-ttu-id="eec85-130">لذلك، يجب عدم إنشاء مصادر بيانات قد تتجاوز هذا الحد في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="eec85-130">Therefore, you should not create data sources that might exceed this limit at runtime.</span></span> <span data-ttu-id="eec85-131">إذا تم تجاوز الحد المسموح به، يتوقف تشغيل التطبيق، ويتم طرح استثناء.</span><span class="sxs-lookup"><span data-stu-id="eec85-131">If the limit is exceeded, the application stops running, and an exception is thrown.</span></span> <span data-ttu-id="eec85-132">على سبيل المثال، قد تحدث هذه الحالة إذا تم تكوين مصدر البيانات على الشكل `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)` ، وتحتوي القائمتين **List1**و **List2** على عدد ضخم من السجلات.</span><span class="sxs-lookup"><span data-stu-id="eec85-132">For example, this situation can occur if the data source is configured as `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)`, and the **List1** and **List2** lists contain a large volume of records.</span></span>

<span data-ttu-id="eec85-133">في بعض الحالات، تُترجم الوظيفة `VALUEIN` إلى بيان قاعدة بيانات باستخدام عامل التشغيل `EXISTS JOIN`.</span><span class="sxs-lookup"><span data-stu-id="eec85-133">In some cases, the `VALUEIN` function is translated to a database statement by using the `EXISTS JOIN` operator.</span></span> <span data-ttu-id="eec85-134">يحدث هذا السلوك عند استخدام الدالة [FILTER](er-functions-list-filter.md) وتلبية الشروط التالية:</span><span class="sxs-lookup"><span data-stu-id="eec85-134">This behavior occurs when the [FILTER](er-functions-list-filter.md) function is used and the following conditions are met:</span></span>

- <span data-ttu-id="eec85-135">يكون الخيار **طلب استعلام**‬ متوقفًا عن التشغيل لمصدر بيانات الوظيفة `VALUEIN` التي تشير إلى قائمة السجلات.</span><span class="sxs-lookup"><span data-stu-id="eec85-135">The **ASK FOR QUERY** option is turned off for the data source of the `VALUEIN` function that refers to the list of records.</span></span> <span data-ttu-id="eec85-136">لم يتم تطبيق أية شروط إضافية لمصدر البيانات هذا في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="eec85-136">No additional conditions will be applied to this data source at runtime.</span></span>
- <span data-ttu-id="eec85-137">لا يتم تكوين تعبيرات متداخلة لمصدر بيانات وظيفة `VALUEIN` التي تشير إلى قائمة السجلات.</span><span class="sxs-lookup"><span data-stu-id="eec85-137">No nested expressions are configured for the data source of the `VALUEIN` function that refers to the list of records.</span></span>
- <span data-ttu-id="eec85-138">يُشير عنصر قائمة الوظيفة `VALUEIN` إلى حقل مصدر بيانات مُحدد، وليس إلى تعبير أو أسلوب لمصدر البيانات هذا.</span><span class="sxs-lookup"><span data-stu-id="eec85-138">A list item of the `VALUEIN` function refers to a field of the specified data source, not to an expression or method of that data source.</span></span>

<span data-ttu-id="eec85-139">يمكنك استخدام هذا الخيار بدلاً من الوظيفة [WHERE](er-functions-list-where.md) الموضحة سابقًا في هذا المثال.</span><span class="sxs-lookup"><span data-stu-id="eec85-139">Consider using this option instead of the [WHERE](er-functions-list-where.md) function that is described earlier in this example.</span></span>

## <a name="example-2"></a><span data-ttu-id="eec85-140">مثال2</span><span class="sxs-lookup"><span data-stu-id="eec85-140">Example 2</span></span>

<span data-ttu-id="eec85-141">أنت تحدد مصادر البيانات التالية في تعيين نموذج:</span><span class="sxs-lookup"><span data-stu-id="eec85-141">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="eec85-142">مصدر البيانات **In** من النوع *سجلات الجدول*.</span><span class="sxs-lookup"><span data-stu-id="eec85-142">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="eec85-143">يشير مصدر البيانات هذا إلى جدول نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي. </span><span class="sxs-lookup"><span data-stu-id="eec85-143">This data source refers to the Intrastat table.</span></span>
- <span data-ttu-id="eec85-144">مصدر البيانات **المنفذ** من النوع *سجلات الجدول*.</span><span class="sxs-lookup"><span data-stu-id="eec85-144">The **Port** data source of the *Table records* type.</span></span> <span data-ttu-id="eec85-145">يشير مصدر البيانات هذا إلى جدول IntrastatPort. </span><span class="sxs-lookup"><span data-stu-id="eec85-145">This data source refers to the IntrastatPort table.</span></span>

<span data-ttu-id="eec85-146">عند استدعاء مصدر بيانات تم تكوينه على أنه التعبير `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` ، يتم إنشاء عبارة SQL التالية لإرجاع السجلات التي تمت تصفيتها في جدول نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="eec85-146">When a data source is called that has been configured as the `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` expression, the following SQL statement is generated to return filtered records of the Intrastat table.</span></span>

```vb
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

<span data-ttu-id="eec85-147">بالنسبة إلى حقول **dataAreaId**، يتم إنشاء عبارة SQL النهائية باستخدام عامل التشغيل `IN`.</span><span class="sxs-lookup"><span data-stu-id="eec85-147">For **dataAreaId** fields, the final SQL statement is generated by the using `IN` operator.</span></span>

## <a name="example-3"></a><span data-ttu-id="eec85-148">المثال الثالث</span><span class="sxs-lookup"><span data-stu-id="eec85-148">Example 3</span></span>

<span data-ttu-id="eec85-149">أنت تحدد مصادر البيانات التالية في تعيين نموذج:</span><span class="sxs-lookup"><span data-stu-id="eec85-149">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="eec85-150">مصدر البيانات **Le** من النوع *الحقل المحسوب*.</span><span class="sxs-lookup"><span data-stu-id="eec85-150">The **Le** data source of the *Calculated field* type.</span></span> <span data-ttu-id="eec85-151">يحتوي مصدر البيانات هذا على التعبير `SPLIT ("DEMF,GBSI,USMF", ",")`.</span><span class="sxs-lookup"><span data-stu-id="eec85-151">This data source contains the expression `SPLIT ("DEMF,GBSI,USMF", ",")`.</span></span>
- <span data-ttu-id="eec85-152">مصدر البيانات **In** من النوع *سجلات الجدول*.</span><span class="sxs-lookup"><span data-stu-id="eec85-152">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="eec85-153">يشير مصدر البيانات هذا إلى جدول نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي ، ويتم تشغيل الخيار **عبر الشركة** لذلك.</span><span class="sxs-lookup"><span data-stu-id="eec85-153">This data source refers to the Intrastat table, and the **Cross-company** option is turned on for it.</span></span>

<span data-ttu-id="eec85-154">عند استدعاء مصدر بيانات تم تكوينه على أنه التعبير `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` ، تحتوي عبارة SQL النهائية على الشرط التالي:</span><span class="sxs-lookup"><span data-stu-id="eec85-154">When a data source is called that has been configured as the `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` expression, the final SQL statement contains the following condition.</span></span>

```vb
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a><span data-ttu-id="eec85-155">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="eec85-155">Additional resources</span></span>

[<span data-ttu-id="eec85-156">الوظائف المنطقية</span><span class="sxs-lookup"><span data-stu-id="eec85-156">Logical functions</span></span>](er-functions-category-logical.md)
