---
title: وظيفة NUMSEQVALUE ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية NUMSEQVALUE (ER).
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
ms.openlocfilehash: 70e07fe429472b703f739baa09f700fb8970d34e
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744013"
---
# <a name="numseqvalue-er-function"></a><span data-ttu-id="b89d7-103">وظيفة NUMSEQVALUE ER</span><span class="sxs-lookup"><span data-stu-id="b89d7-103">NUMSEQVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b89d7-104">تُرجع الوظيفة `NUMSEQVALUE` قيمة *سلسلة* تمثل القيمة الجديدة التي تم إنشاؤها للتسلسل الرقمي، استنادًا إلى التسلسل الرقمي المُحدد والنطاق ومُعرف النطاق.</span><span class="sxs-lookup"><span data-stu-id="b89d7-104">The `NUMSEQVALUE` function returns a *String* value that represents the new generated value of a number sequence, based on the specified number sequence, scope, and scope ID.</span></span> <span data-ttu-id="b89d7-105">يساوي مُعرف النطاق كود الشركة الذي يتم توفيره بواسطة السياق الذي يتم تشغيل تنسيق إعداد التقارير الإلكترونية (ER) ضمنه.</span><span class="sxs-lookup"><span data-stu-id="b89d7-105">The scope ID equals the company code that is supplied by the context that the Electronic reporting (ER) format is run under.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="b89d7-106">بناء الجملة 1</span><span class="sxs-lookup"><span data-stu-id="b89d7-106">Syntax 1</span></span>

```vb
NUMSEQVALUE (number sequence code)
```

## <a name="syntax-2"></a><span data-ttu-id="b89d7-107">بناء الجملة 2</span><span class="sxs-lookup"><span data-stu-id="b89d7-107">Syntax 2</span></span>

```vb
NUMSEQVALUE (number sequence record ID)
```

## <a name="syntax-3"></a><span data-ttu-id="b89d7-108">بناء الجملة 3</span><span class="sxs-lookup"><span data-stu-id="b89d7-108">Syntax 3</span></span>

```vb
NUMSEQVALUE (number sequence code, scope type, scope ID)
```

## <a name="arguments"></a><span data-ttu-id="b89d7-109">الوسائط</span><span class="sxs-lookup"><span data-stu-id="b89d7-109">Arguments</span></span>

<span data-ttu-id="b89d7-110">`number sequence code`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="b89d7-110">`number sequence code`: *String*</span></span>

<span data-ttu-id="b89d7-111">قيمة نصية تمثل كود التسلسل الرقمي المطلوب فيه قيمة جديدة.</span><span class="sxs-lookup"><span data-stu-id="b89d7-111">A text value that represents the code of the number sequence that a new value is required in.</span></span>

<span data-ttu-id="b89d7-112">`number sequence record ID`: *Int64*</span><span class="sxs-lookup"><span data-stu-id="b89d7-112">`number sequence record ID`: *Int64*</span></span>

<span data-ttu-id="b89d7-113">قيمة *Int64* تُمثل مُعرف السجل لسجل في جدول NumberSequenceTable يحتوي على تعريف التسلسل الرقمي المطلوب فيه قيمة جديدة. </span><span class="sxs-lookup"><span data-stu-id="b89d7-113">An *Int64* value that represents the record ID of a record in the NumberSequenceTable table that contains the definition of the number sequence that a new value is required in.</span></span>

<span data-ttu-id="b89d7-114">`scope type`: *قيمة التعداد*</span><span class="sxs-lookup"><span data-stu-id="b89d7-114">`scope type`: *Enum value*</span></span>

<span data-ttu-id="b89d7-115">قيمة تعداد لتعداد **ERExpressionNumberSequenceScopeType** التي تعرف نطاق التسلسل الرقمي المطلوب فيه قيمة جديدة. </span><span class="sxs-lookup"><span data-stu-id="b89d7-115">An enumeration value of the **ERExpressionNumberSequenceScopeType** enumeration that defines the scope of the number sequence that a new value is required in.</span></span> <span data-ttu-id="b89d7-116">أنواع النطاقات المتاحة هي **مشتركة** و **كيان قانوني** و **شركة**.</span><span class="sxs-lookup"><span data-stu-id="b89d7-116">The available scope types are **Shared**, **Legal entity**, and **Company**.</span></span>

<span data-ttu-id="b89d7-117">`scope ID`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="b89d7-117">`scope ID`: *String*</span></span>

<span data-ttu-id="b89d7-118">قيمة *السلسلة* التي تُعرف النطاق، استنادًا إلى نوع النطاق المُحدد.</span><span class="sxs-lookup"><span data-stu-id="b89d7-118">A *String* value that identifies the scope, based on the specified scope type.</span></span>

## <a name="return-values"></a><span data-ttu-id="b89d7-119">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="b89d7-119">Return values</span></span>

<span data-ttu-id="b89d7-120">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="b89d7-120">*String*</span></span>

<span data-ttu-id="b89d7-121">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="b89d7-121">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b89d7-122">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="b89d7-122">Usage notes</span></span>

<span data-ttu-id="b89d7-123">بالنسبة إلى نوع النطاق **المشترك**، حدد سلسلة فارغة كمعرف النطاق.</span><span class="sxs-lookup"><span data-stu-id="b89d7-123">For the **Shared** scope type, specify an empty string as the scope ID.</span></span>

<span data-ttu-id="b89d7-124">بالنسبة إلى نوعي النطاق **الشركة** و **الكيان القانوني** ، حدد كود الشركة كمعرف النطاق.</span><span class="sxs-lookup"><span data-stu-id="b89d7-124">For the **Company** and **Legal entity** scope types, specify the company code as the scope ID.</span></span> <span data-ttu-id="b89d7-125">إذا قمت بتحديد سلسلة فارغة كمُعرف نطاق لأنواع النطاقات هذه، يتم استخدام كود الشركة الحالي.</span><span class="sxs-lookup"><span data-stu-id="b89d7-125">If you specify an empty string as the scope ID for these scope types, the current company code is used.</span></span>

<span data-ttu-id="b89d7-126">عند استخدام بناء الجملة 1، يتم طلب التسلسل الرقمي لنوع نطاق **الشركة** ، ويتم توفير رمز الشركة بواسطة السياق الذي يتم تشغيل تنسيق ER ضمنه.</span><span class="sxs-lookup"><span data-stu-id="b89d7-126">When syntax 1 is used, the number sequence is requested for the **Company** scope type, and the company code is supplied by the context that the ER format is run under.</span></span>

## <a name="example-1"></a><span data-ttu-id="b89d7-127">مثال1</span><span class="sxs-lookup"><span data-stu-id="b89d7-127">Example 1</span></span>

<span data-ttu-id="b89d7-128">في تنسيق ER الخاص بك، يجب عليك تحديد مصدر بيانات **AskNumSeq** من النوع *مُعلمات إدخال المستخدم*.</span><span class="sxs-lookup"><span data-stu-id="b89d7-128">In your ER format, you define the **AskNumSeq** data source of the *User input parameter* type.</span></span> <span data-ttu-id="b89d7-129">يشير مصدر البيانات هذا إلى نوع البيانات الموسعة (EDT) **الوصف**.</span><span class="sxs-lookup"><span data-stu-id="b89d7-129">This data source refers to the **Description** extended data type (EDT).</span></span> <span data-ttu-id="b89d7-130">بعد ذلك، يُمكن تعريف مصدر البيانات **NumSeq** من النوع *الحقل المحسوب*.</span><span class="sxs-lookup"><span data-stu-id="b89d7-130">Next, you define the **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="b89d7-131">يحتوي مصدر البيانات هذا على التعبير `NUMSEQVALUE (AskNumSeq)`.</span><span class="sxs-lookup"><span data-stu-id="b89d7-131">This data source contains the expression `NUMSEQVALUE (AskNumSeq)`.</span></span> <span data-ttu-id="b89d7-132">عندما يتم استدعاء مصدر البيانات **NumSeq** ، يُرجع القيمة الجديدة التي تم إنشاؤها من التسلسل الرقمي الذي تم تحديده في وقت التشغيل عن طريق إدخال الكود الخاص به في مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="b89d7-132">When the **NumSeq** data source is called, it returns the new generated value of the number sequence that was specified at runtime by entering its code in the dialog box.</span></span> <span data-ttu-id="b89d7-133">يتم طلب التسلسل الرقمي لنوع نطاق **الشركة**.</span><span class="sxs-lookup"><span data-stu-id="b89d7-133">The number sequence is requested for the **Company** scope type.</span></span> <span data-ttu-id="b89d7-134">يتم توفير كود الشركة بواسطة السياق الذي تم تشغيل تنسيق ER ضمنه.</span><span class="sxs-lookup"><span data-stu-id="b89d7-134">The company code is supplied by the context that the ER format is run under.</span></span>

## <a name="example-2"></a><span data-ttu-id="b89d7-135">مثال2</span><span class="sxs-lookup"><span data-stu-id="b89d7-135">Example 2</span></span>

<span data-ttu-id="b89d7-136">يتم تعريف مصادر البيانات التالية في تعيين النموذج الخاص بك:</span><span class="sxs-lookup"><span data-stu-id="b89d7-136">The following data sources are defined in your model mapping:</span></span>

- <span data-ttu-id="b89d7-137">مصدر البيانات **LedgerParms** من النوع *الجدول*.</span><span class="sxs-lookup"><span data-stu-id="b89d7-137">The **LedgerParms** data source of the *Table* type.</span></span> <span data-ttu-id="b89d7-138">يشير مصدر البيانات هذا إلى جدول LedgerParameters. </span><span class="sxs-lookup"><span data-stu-id="b89d7-138">This data source refers to the LedgerParameters table.</span></span>
- <span data-ttu-id="b89d7-139">مصدر البيانات **NumSeq** من النوع *الحقل المحسوب*.</span><span class="sxs-lookup"><span data-stu-id="b89d7-139">The **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="b89d7-140">يحتوي مصدر البيانات هذا على التعبير `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.</span><span class="sxs-lookup"><span data-stu-id="b89d7-140">This data source contains the expression `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.</span></span>

<span data-ttu-id="b89d7-141">يُرجع نوع مصدر البيانات **NumSeq**، عند استدعائه، القيمة الجديدة المُنشأة للتسلسل الرقمي الذي تم تكوينه في معلمات دفتر الأستاذ العام للشركة التي توفر السياق الذي يعمل ضمنه تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="b89d7-141">When the **NumSeq** data source is called, it returns the new generated value of the number sequence that has been configured in the General ledger parameters for the company that supplies the context that the ER format is run under.</span></span> <span data-ttu-id="b89d7-142">يحدد هذا التسلسل الرقمي دفاتر اليومية بشكل فريد ويعمل كرقم دُفعة يربط الحركات ببعضها.</span><span class="sxs-lookup"><span data-stu-id="b89d7-142">This number sequence uniquely identifies journals and acts as a batch number that links the transactions together.</span></span>

## <a name="example-3"></a><span data-ttu-id="b89d7-143">المثال الثالث</span><span class="sxs-lookup"><span data-stu-id="b89d7-143">Example 3</span></span>

<span data-ttu-id="b89d7-144">يتم تعريف مصادر البيانات التالية في تعيين النموذج الخاص بك:</span><span class="sxs-lookup"><span data-stu-id="b89d7-144">The following data sources are defined in your model mapping:</span></span>

- <span data-ttu-id="b89d7-145">مصدر بيانات **enumScope** من النوع Dynamics 365 Finance Microsoft *تعداد*.</span><span class="sxs-lookup"><span data-stu-id="b89d7-145">The **enumScope** data source of the Microsoft Dynamics 365 Finance *enumeration* type.</span></span> <span data-ttu-id="b89d7-146">يُشير مصدر البيانات هذا إلى تعداد **‎ERExpressionNumberSequenceScopeType**. </span><span class="sxs-lookup"><span data-stu-id="b89d7-146">This data source refers to the **ERExpressionNumberSequenceScopeType** enumeration.</span></span>
- <span data-ttu-id="b89d7-147">مصدر البيانات **NumSeq** من النوع *الحقل المحسوب*.</span><span class="sxs-lookup"><span data-stu-id="b89d7-147">The **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="b89d7-148">يحتوي مصدر البيانات هذا على التعبير `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.</span><span class="sxs-lookup"><span data-stu-id="b89d7-148">This data source contains the expression `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.</span></span>

<span data-ttu-id="b89d7-149">يُرجع نوع مصدر البيانات **NumSeq**، عند استدعائه، القيمة الجديدة المُنشأة للتسلسل الرقمي **Gene\_1** الذي تم تكوينه للشركة التي توفر السياق الذي يعمل ضمنه تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="b89d7-149">When the **NumSeq** data source is called, it returns the new generated value of the **Gene\_1** number sequence that has been configured for the company that supplies the context that the ER format is run under.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b89d7-150">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="b89d7-150">Additional resources</span></span>

[<span data-ttu-id="b89d7-151">دالات أخرى (خاصة بمجال الأعمال)</span><span class="sxs-lookup"><span data-stu-id="b89d7-151">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
