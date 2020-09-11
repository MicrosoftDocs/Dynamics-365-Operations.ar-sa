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
ms.openlocfilehash: c7f78b687865e63e658c1c1c4f148b50595bf063
ms.sourcegitcommit: 54bdcf8e9b6d1b1aae2a244f7a82754879d12053
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/31/2020
ms.locfileid: "3740653"
---
# <a name=""></a><span data-ttu-id="d50b5-103"><a name="LISTJOIN">الدالة LISTJOIN ER</a></span><span class="sxs-lookup"><span data-stu-id="d50b5-103"><a name="LISTJOIN">LISTJOIN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d50b5-104">تُرجع الدالة `LISTJOIN` قيمة *قائمة السجلات* التي تمثل قائمة منضمة جديدة تم إنشاءها من الوسيطات المُحددة.</span><span class="sxs-lookup"><span data-stu-id="d50b5-104">The `LISTJOIN` function returns a *Record list* value that represents a new joined list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="d50b5-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="d50b5-105">Syntax</span></span>

```vb
LIST (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a><span data-ttu-id="d50b5-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="d50b5-106">Arguments</span></span>

<span data-ttu-id="d50b5-107">`list 1`: *قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="d50b5-107">`list 1`: *Record list*</span></span>

<span data-ttu-id="d50b5-108">مرجع إلى مصدر البيانات من نوع بيانات *قائمة سجلات*.</span><span class="sxs-lookup"><span data-stu-id="d50b5-108">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="d50b5-109">هذه الوسيطة إلزامية.</span><span class="sxs-lookup"><span data-stu-id="d50b5-109">This argument is mandatory.</span></span>

<span data-ttu-id="d50b5-110">`list N`: *قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="d50b5-110">`list N`: *Record list*</span></span>

<span data-ttu-id="d50b5-111">مرجع إلى مصدر البيانات من نوع بيانات *قائمة سجلات*.</span><span class="sxs-lookup"><span data-stu-id="d50b5-111">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="d50b5-112">هذه الوسائط الإضافية اختيارية.</span><span class="sxs-lookup"><span data-stu-id="d50b5-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="d50b5-113">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="d50b5-113">Return values</span></span>

<span data-ttu-id="d50b5-114">*قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="d50b5-114">*Record list*</span></span>

<span data-ttu-id="d50b5-115">قائمة السجلات الناتجة.</span><span class="sxs-lookup"><span data-stu-id="d50b5-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d50b5-116">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="d50b5-116">Usage notes</span></span>

<span data-ttu-id="d50b5-117">تحتوي بنية القائمة التي تم إنشائها فقط على الحقول الموجودة في بنية كل قائمة سجلات مشار إليها في الوسيطات.</span><span class="sxs-lookup"><span data-stu-id="d50b5-117">The structure of the list that is created contains only the fields that are present in the structure of every record list that is referenced in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="d50b5-118">مثال</span><span class="sxs-lookup"><span data-stu-id="d50b5-118">Example</span></span>

<span data-ttu-id="d50b5-119">أدخل مصدر البيانات **السجل 1** من النوع `Container`.</span><span class="sxs-lookup"><span data-stu-id="d50b5-119">You enter data source **Record 1** of the `Container` type.</span></span> <span data-ttu-id="d50b5-120">يحتوي مصدر البيانات هذا على الحقول المتداخلة التالية من النوع `Calculated field`:</span><span class="sxs-lookup"><span data-stu-id="d50b5-120">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="d50b5-121">**الرمز**: يحتوي هذا الحقل على تعبير يُرجع قيمة من النوع `String`.</span><span class="sxs-lookup"><span data-stu-id="d50b5-121">**Code**: This field contains an expression that returns a value of the `String` type.</span></span>
- <span data-ttu-id="d50b5-122">**المبلغ**: يحتوي هذا الحقل على تعبير يُرجع قيمة من النوع `Real`.</span><span class="sxs-lookup"><span data-stu-id="d50b5-122">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>

<span data-ttu-id="d50b5-123">بعد ذلك، أدخل مصدر البيانات **السجل 2** من النوع `Container`.</span><span class="sxs-lookup"><span data-stu-id="d50b5-123">You then enter data source **Record 2** of the `Container` type.</span></span> <span data-ttu-id="d50b5-124">يحتوي مصدر البيانات هذا على الحقول المتداخلة التالية من النوع `Calculated field`:</span><span class="sxs-lookup"><span data-stu-id="d50b5-124">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="d50b5-125">**المبلغ**: يحتوي هذا الحقل على تعبير يُرجع قيمة من النوع `Real`.</span><span class="sxs-lookup"><span data-stu-id="d50b5-125">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>
- <span data-ttu-id="d50b5-126">**‎IsValid**: يحتوي هذا الحقل على تعبير يُرجع قيمة من النوع `Boolean`.</span><span class="sxs-lookup"><span data-stu-id="d50b5-126">**IsValid**: This field contains an expression that returns a value of the `Boolean` type.</span></span>

![صفحة مصمم تعيين نموذج إعداد التقارير الإلكترونية](./media/er-functions-list-listjoin-image1.gif)

<span data-ttu-id="d50b5-128">في هذه الحالة، يُرجع التعبير `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` قائمة جديدة تحتوي على سجلين.</span><span class="sxs-lookup"><span data-stu-id="d50b5-128">In this case, the expression `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` returns a new list that contains two records.</span></span>

![صفحة مصمم تعيين نموذج إعداد التقارير الإلكترونية](./media/er-functions-list-listjoin-image2.gif)

<span data-ttu-id="d50b5-130">تتكون بنية هذه القائمة من حقل **مبلغ** واحد من النوع `Real`، لأن هذا الحقل هو الحقل الوحيد الذي يتم تقديمه في كل وسطية من الوظيفة المستدعاة.</span><span class="sxs-lookup"><span data-stu-id="d50b5-130">The structure of this list consists of a single **Amount** field of the `Real` type, because this field is the only field that is presented in every argument of the called function.</span></span>

![صفحة مصمم تعيين نموذج إعداد التقارير الإلكترونية](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a><span data-ttu-id="d50b5-132">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="d50b5-132">Additional resources</span></span>

[<span data-ttu-id="d50b5-133">دالات القائمة</span><span class="sxs-lookup"><span data-stu-id="d50b5-133">List functions</span></span>](er-functions-category-list.md)

[<span data-ttu-id="d50b5-134">تصحيح مصادر البيانات لتنسيق ER الذي تم تنفيذه لتحليل تدفق البيانات وتحويلها</span><span class="sxs-lookup"><span data-stu-id="d50b5-134">Debug data sources of an executed ER format to analyze data flow and transformation</span></span>](er-debug-data-sources.md)
