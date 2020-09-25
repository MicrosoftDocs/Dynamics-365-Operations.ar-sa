---
title: الدالة LISTJOIN ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام دالة إعداد التقارير الإلكترونية LISTJOIN.
author: NickSelin
manager: kfend
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 035bf720a892e987ff9fc073ab8ed6f6cc6ea18e
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745095"
---
# <a name="listjoin-er-function"></a><span data-ttu-id="4f31e-103">الدالة LISTJOIN ER</span><span class="sxs-lookup"><span data-stu-id="4f31e-103">LISTJOIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4f31e-104">تُرجع الدالة `LISTJOIN` قيمة *قائمة السجلات* التي تمثل قائمة منضمة جديدة تم إنشاءها من الوسيطات المُحددة.</span><span class="sxs-lookup"><span data-stu-id="4f31e-104">The `LISTJOIN` function returns a *Record list* value that represents a new joined list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f31e-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="4f31e-105">Syntax</span></span>

```vb
LIST (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a><span data-ttu-id="4f31e-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="4f31e-106">Arguments</span></span>

<span data-ttu-id="4f31e-107">`list 1`: *قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="4f31e-107">`list 1`: *Record list*</span></span>

<span data-ttu-id="4f31e-108">مرجع إلى مصدر البيانات من نوع بيانات *قائمة سجلات*.</span><span class="sxs-lookup"><span data-stu-id="4f31e-108">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="4f31e-109">هذه الوسيطة إلزامية.</span><span class="sxs-lookup"><span data-stu-id="4f31e-109">This argument is mandatory.</span></span>

<span data-ttu-id="4f31e-110">`list N`: *قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="4f31e-110">`list N`: *Record list*</span></span>

<span data-ttu-id="4f31e-111">مرجع إلى مصدر البيانات من نوع بيانات *قائمة سجلات*.</span><span class="sxs-lookup"><span data-stu-id="4f31e-111">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="4f31e-112">هذه الوسائط الإضافية اختيارية.</span><span class="sxs-lookup"><span data-stu-id="4f31e-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="4f31e-113">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="4f31e-113">Return values</span></span>

<span data-ttu-id="4f31e-114">*قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="4f31e-114">*Record list*</span></span>

<span data-ttu-id="4f31e-115">قائمة السجلات الناتجة.</span><span class="sxs-lookup"><span data-stu-id="4f31e-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="4f31e-116">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="4f31e-116">Usage notes</span></span>

<span data-ttu-id="4f31e-117">تحتوي بنية القائمة التي تم إنشائها فقط على الحقول الموجودة في بنية كل قائمة سجلات مشار إليها في الوسيطات.</span><span class="sxs-lookup"><span data-stu-id="4f31e-117">The structure of the list that is created contains only the fields that are present in the structure of every record list that is referenced in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="4f31e-118">مثال</span><span class="sxs-lookup"><span data-stu-id="4f31e-118">Example</span></span>

<span data-ttu-id="4f31e-119">أدخل مصدر البيانات **السجل 1** من النوع `Container`.</span><span class="sxs-lookup"><span data-stu-id="4f31e-119">You enter data source **Record 1** of the `Container` type.</span></span> <span data-ttu-id="4f31e-120">يحتوي مصدر البيانات هذا على الحقول المتداخلة التالية من النوع `Calculated field`:</span><span class="sxs-lookup"><span data-stu-id="4f31e-120">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="4f31e-121">**الرمز**: يحتوي هذا الحقل على تعبير يُرجع قيمة من النوع `String`.</span><span class="sxs-lookup"><span data-stu-id="4f31e-121">**Code**: This field contains an expression that returns a value of the `String` type.</span></span>
- <span data-ttu-id="4f31e-122">**المبلغ**: يحتوي هذا الحقل على تعبير يُرجع قيمة من النوع `Real`.</span><span class="sxs-lookup"><span data-stu-id="4f31e-122">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>

<span data-ttu-id="4f31e-123">بعد ذلك، أدخل مصدر البيانات **السجل 2** من النوع `Container`.</span><span class="sxs-lookup"><span data-stu-id="4f31e-123">You then enter data source **Record 2** of the `Container` type.</span></span> <span data-ttu-id="4f31e-124">يحتوي مصدر البيانات هذا على الحقول المتداخلة التالية من النوع `Calculated field`:</span><span class="sxs-lookup"><span data-stu-id="4f31e-124">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="4f31e-125">**المبلغ**: يحتوي هذا الحقل على تعبير يُرجع قيمة من النوع `Real`.</span><span class="sxs-lookup"><span data-stu-id="4f31e-125">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>
- <span data-ttu-id="4f31e-126">**‎IsValid**: يحتوي هذا الحقل على تعبير يُرجع قيمة من النوع `Boolean`.</span><span class="sxs-lookup"><span data-stu-id="4f31e-126">**IsValid**: This field contains an expression that returns a value of the `Boolean` type.</span></span>

![صفحة مصمم تعيين نموذج إعداد التقارير الإلكترونية](./media/er-functions-list-listjoin-image1.gif)

<span data-ttu-id="4f31e-128">في هذه الحالة، يُرجع التعبير `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` قائمة جديدة تحتوي على سجلين.</span><span class="sxs-lookup"><span data-stu-id="4f31e-128">In this case, the expression `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` returns a new list that contains two records.</span></span>

![صفحة مصمم تعيين نموذج التقارير الإلكترونية مع سجلين](./media/er-functions-list-listjoin-image2.gif)

<span data-ttu-id="4f31e-130">تتكون بنية هذه القائمة من حقل **مبلغ** واحد من النوع `Real`، لأن هذا الحقل هو الحقل الوحيد الذي يتم تقديمه في كل وسطية من الوظيفة المستدعاة.</span><span class="sxs-lookup"><span data-stu-id="4f31e-130">The structure of this list consists of a single **Amount** field of the `Real` type, because this field is the only field that is presented in every argument of the called function.</span></span>

![حقل المبلغ في صفحة مصمم تعيين نموذج إعداد التقارير الإلكترونية](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a><span data-ttu-id="4f31e-132">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="4f31e-132">Additional resources</span></span>

[<span data-ttu-id="4f31e-133">دالات القائمة</span><span class="sxs-lookup"><span data-stu-id="4f31e-133">List functions</span></span>](er-functions-category-list.md)

[<span data-ttu-id="4f31e-134">تصحيح مصادر البيانات لتنسيق ER الذي تم تنفيذه لتحليل تدفق البيانات وتحويلها</span><span class="sxs-lookup"><span data-stu-id="4f31e-134">Debug data sources of an executed ER format to analyze data flow and transformation</span></span>](er-debug-data-sources.md)
