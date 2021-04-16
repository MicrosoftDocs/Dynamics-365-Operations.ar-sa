---
title: 'وظيفة VALUEINLARGE ER '
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية VALUEINLARGE (ER).
author: NickSelin
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 74d6856a0598293d87f79baabed4773d617164d0
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743741"
---
# <a name="valueinlarge-er-function"></a><span data-ttu-id="19d6c-103">وظيفة VALUEINLARGE ER </span><span class="sxs-lookup"><span data-stu-id="19d6c-103">VALUEINLARGE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="19d6c-104">تُحدد وظيفة `VALUEINLARGE` ما إذا كان الإدخال المُحدد من النوع *Int64* أو *عدد صحيح* يطابق أي قيمة عنصر مُحدد في القائمة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="19d6c-104">The `VALUEINLARGE` function determines whether the specified input of the *Int64* or *Integer* type matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="19d6c-105">تقوم الوظيفة بإرجاع قيمة *منطقية* **TRUE** إذا كان الإدخال المُحدد يُطابق نتيجة تشغيل التعبير المُحدد لسجل واحد على الأقل من القائمة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="19d6c-105">The function returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="19d6c-106">وبخلاف ذلك، تُرجع قيمة *منطقية* لـ **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="19d6c-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> <span data-ttu-id="19d6c-107">لفهم المختلف في الوظيفة `VALUEIN` ، راجع قسم [ملاحظة الاستخدام](#usage_note) لاحقًا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="19d6c-107">To understand the difference with the `VALUEIN` function, see the [Usage note](#usage_note) section later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="19d6c-108">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="19d6c-108">Syntax</span></span>

```vb
VALUEINLARGE (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="19d6c-109">الوسائط</span><span class="sxs-lookup"><span data-stu-id="19d6c-109">Arguments</span></span>

<span data-ttu-id="19d6c-110">`input`: *الحقل*</span><span class="sxs-lookup"><span data-stu-id="19d6c-110">`input`: *Field*</span></span>

<span data-ttu-id="19d6c-111">مسار صالح لصنف مصدر بيانات من نوع *قائمة السجلات*.</span><span class="sxs-lookup"><span data-stu-id="19d6c-111">The valid path of a data source item of the *Record list* type.</span></span> <span data-ttu-id="19d6c-112">وستتم مطابقة قيمة هذا الصنف.</span><span class="sxs-lookup"><span data-stu-id="19d6c-112">The value of this item will be matched.</span></span>

<span data-ttu-id="19d6c-113">`list`: *قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="19d6c-113">`list`: *Record list*</span></span>

<span data-ttu-id="19d6c-114">مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.</span><span class="sxs-lookup"><span data-stu-id="19d6c-114">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="19d6c-115">`list item expression`: *التعبير*</span><span class="sxs-lookup"><span data-stu-id="19d6c-115">`list item expression`: *Expression*</span></span>

<span data-ttu-id="19d6c-116">تعبير شرطي صالح يشير إما إلى أو يحتوي على حقل واحد من القائمة المحددة يجب استخدامه للمطابقة.</span><span class="sxs-lookup"><span data-stu-id="19d6c-116">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="19d6c-117">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="19d6c-117">Return values</span></span>

<span data-ttu-id="19d6c-118">*منطقي*</span><span class="sxs-lookup"><span data-stu-id="19d6c-118">*Boolean*</span></span>

<span data-ttu-id="19d6c-119">القيمة *المنطقية* الناتجة.</span><span class="sxs-lookup"><span data-stu-id="19d6c-119">The resulting *Boolean* value.</span></span>

## <a name=""></a><span data-ttu-id="19d6c-120"><a name="usage_note">ملاحظات الاستخدام</a></span><span class="sxs-lookup"><span data-stu-id="19d6c-120"><a name="usage_note">Usage notes</a></span></span>

<span data-ttu-id="19d6c-121">عندما يمثل الإدخال المُحدد نوع *Int64* أو *عدد صحيح* لصنف مصدر البيانات، فمن ثم يكون الاستدعاء لها قابلًا للترجمة إلى عبارة SQL مباشرة، يتم تحويل القائمة المُحددة إلى جدول SQL مؤقت ويتم إجراء مطابقة في قاعدة البيانات من خلال تنفيذ استعلام `EXISTS JOIN` واحد.</span><span class="sxs-lookup"><span data-stu-id="19d6c-121">When the specified input represents an *Int64* or *Integer* type of a data source item, the call to which is translatable to a direct SQL statement, the specified list is converted to a temporary SQL table and matching is performed in the database by executing a single `EXISTS JOIN` query.</span></span> <span data-ttu-id="19d6c-122">وبخلاف ذلك، تعمل هذه الوظيفة كوظيفة [`VALUEIN`](er-functions-logical-valuein.md).</span><span class="sxs-lookup"><span data-stu-id="19d6c-122">Otherwise, this function works as the [`VALUEIN`](er-functions-logical-valuein.md) function.</span></span>

<span data-ttu-id="19d6c-123">عندما يمثل الإدخال المُحدد صنف مصدر بيانات تم تصمميه كأحد الأصناف بخلاف النوع *Int64* و *عدد صحيح*، يحدث خطأ في وقت التصميم يُخبرك بأن وظيفة `VALUEINLARGE` غير منطبقة لتعبير ER الذي تم تكوينه.</span><span class="sxs-lookup"><span data-stu-id="19d6c-123">When the specified input represents a data source item that is designed as an item other than *Int64* and *Integer* type, an error occurs at design time informing you that the `VALUEINLARGE` function is not applicable for the configured ER expression.</span></span>

<span data-ttu-id="19d6c-124">عندما يتم تنفيذ تعبير الوظيفة `VALUEINLARGE` واستخدام أكثر من جدول مؤقت في نطاق هذا التنفيذ، يحدث خطأ في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="19d6c-124">When the `VALUEINLARGE` function expression is executed and more than one temporary table is used in scope of this execution, a runtime error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="19d6c-125">مثال</span><span class="sxs-lookup"><span data-stu-id="19d6c-125">Example</span></span>

<span data-ttu-id="19d6c-126">أنت تحدد مصادر البيانات التالية في تعيين نموذج:</span><span class="sxs-lookup"><span data-stu-id="19d6c-126">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="19d6c-127">مصدر البيانات **In** من النوع *سجلات الجدول*.</span><span class="sxs-lookup"><span data-stu-id="19d6c-127">The **In** data source of the *Table records* type.</span></span>
    - <span data-ttu-id="19d6c-128">يشير مصدر البيانات هذا إلى جدول **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي**. </span><span class="sxs-lookup"><span data-stu-id="19d6c-128">This data source refers to the **Intrastat** table.</span></span>
    - <span data-ttu-id="19d6c-129">يتم تعيين الخيار **عبر الشركة** إلى **لا**.</span><span class="sxs-lookup"><span data-stu-id="19d6c-129">The **Cross-company** option is set to **No**.</span></span>
- <span data-ttu-id="19d6c-130">مصدر البيانات **InMemory** من النوع *الحقل المحسوب*.</span><span class="sxs-lookup"><span data-stu-id="19d6c-130">The **InMemory** data source of the *Calculated field* type.</span></span>
    - <span data-ttu-id="19d6c-131">يحتوي مصدر البيانات هذا على التعبير `WHERE (In, In.Port <> "")`.</span><span class="sxs-lookup"><span data-stu-id="19d6c-131">This data source contains the expression `WHERE (In, In.Port <> "")`.</span></span>
- <span data-ttu-id="19d6c-132">مصدر البيانات **InFiltered** من النوع *الحقل المحسوب*.</span><span class="sxs-lookup"><span data-stu-id="19d6c-132">The **InFiltered** data source of the *Calculated field* type.</span></span>
    - <span data-ttu-id="19d6c-133">يحتوي مصدر البيانات هذا على التعبير `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.</span><span class="sxs-lookup"><span data-stu-id="19d6c-133">This data source contains the expression `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.</span></span>

<span data-ttu-id="19d6c-134">عندما يتم استدعاء مصدر البيانات **InFiltered** ضمن سياق الشركة **DEMF**، يتم إنشاء جدول مؤقت جديد في قاعدة بيانات التطبيق، ويتم إدراج ما تم تجميعه في قائمة ذاكرة رموز تعريف السجل في هذا الجدول، ويتم إنشاء عبارة SQL التالية لإرجاع السجلات التي تمت تصفيتها من جدول **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي**. </span><span class="sxs-lookup"><span data-stu-id="19d6c-134">When the data source **InFiltered** is called under the context of the company **DEMF**, a new temporary table is created in the application database, the collected in memory list of record identification codes are inserted to this table, and the following SQL statement is generated to return filtered records of the **Intrastat** table.</span></span>

```xpp
SELECT … from Intrastat T1
WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF'))) AND
EXISTS (SELECT 'x' FROM tempdb."DBO".? T2 WHERE ((T2.PARTITION=?) AND (T1.RecId=T2.RecId)))
```

## <a name="additional-resources"></a><span data-ttu-id="19d6c-135">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="19d6c-135">Additional resources</span></span>

[<span data-ttu-id="19d6c-136">الوظائف المنطقية</span><span class="sxs-lookup"><span data-stu-id="19d6c-136">Logical functions</span></span>](er-functions-category-logical.md)

[<span data-ttu-id="19d6c-137">وظائف VALUEIN</span><span class="sxs-lookup"><span data-stu-id="19d6c-137">VALUEIN functions</span></span>](er-functions-logical-valuein.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]