---
title: LIST ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية LIST (ER).
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 6848fe535a6a588eaf06f96e93f28db9ef304940
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917271"
---
# <span data-ttu-id="6f6ff-103"><a name="LIST">LIST ER وظيفة</a></span><span class="sxs-lookup"><span data-stu-id="6f6ff-103"><a name="LIST">LIST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f6ff-104">تُرجع الوظيفة `LIST` قيمة *قائمة سجلات* جديدة تتكون من قائمة سجلات جديدة تم إنشاءها من الوسيطات المُحددة.</span><span class="sxs-lookup"><span data-stu-id="6f6ff-104">The `LIST` function returns a *Record list* value that consists of a new list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f6ff-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="6f6ff-105">Syntax</span></span>

```
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a><span data-ttu-id="6f6ff-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="6f6ff-106">Arguments</span></span>

<span data-ttu-id="6f6ff-107">`record 1`: *حاوية (سجل)*</span><span class="sxs-lookup"><span data-stu-id="6f6ff-107">`record 1`: *Container (record)*</span></span>

<span data-ttu-id="6f6ff-108">مرجع إلى مصدر البيانات من نوع بيانات *السجل*.</span><span class="sxs-lookup"><span data-stu-id="6f6ff-108">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="6f6ff-109">هذه الوسيطة مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="6f6ff-109">This argument is required.</span></span>

<span data-ttu-id="6f6ff-110">`record N`: *حاوية (سجل)*</span><span class="sxs-lookup"><span data-stu-id="6f6ff-110">`record N`: *Container (record)*</span></span>

<span data-ttu-id="6f6ff-111">مرجع إلى مصدر البيانات من نوع بيانات *السجل*.</span><span class="sxs-lookup"><span data-stu-id="6f6ff-111">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="6f6ff-112">هذه الوسائط الإضافية اختيارية.</span><span class="sxs-lookup"><span data-stu-id="6f6ff-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="6f6ff-113">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="6f6ff-113">Return values</span></span>

<span data-ttu-id="6f6ff-114">*قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="6f6ff-114">*Record list*</span></span>

<span data-ttu-id="6f6ff-115">قائمة السجلات الناتجة.</span><span class="sxs-lookup"><span data-stu-id="6f6ff-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="6f6ff-116">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="6f6ff-116">Usage notes</span></span>

<span data-ttu-id="6f6ff-117">تحتوي بنية القائمة التي تم إنشائها فقط على الحقول التي يتم عرضها في البنية لكل سجل مذكور في الوسيطات.</span><span class="sxs-lookup"><span data-stu-id="6f6ff-117">The structure of the list that is created contains only the fields that are presented in the structure of every record that is mentioned in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="6f6ff-118">مثال</span><span class="sxs-lookup"><span data-stu-id="6f6ff-118">Example</span></span>

<span data-ttu-id="6f6ff-119">قم بإدخال مصدر البيانات **السجل 1** من النوع *الحاوية*.</span><span class="sxs-lookup"><span data-stu-id="6f6ff-119">You enter data source **Record 1** of the *Container* type.</span></span> <span data-ttu-id="6f6ff-120">يحتوي مصدر البيانات هذا على الحقول المتداخلة من النوع *الحقل المحسوب*:</span><span class="sxs-lookup"><span data-stu-id="6f6ff-120">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="6f6ff-121">**الرمز:** يحتوي هذا الحقل على تعبيرًا يُرجع قيمة من النوع *السلسلة*.</span><span class="sxs-lookup"><span data-stu-id="6f6ff-121">**Code:** This field contains an expression that returns a value of the *String* type.</span></span>
- <span data-ttu-id="6f6ff-122">**المقدار:** يحتوي هذا الحقل على تعبيرًا يُرجع قيمة من النوع *الحقيقي*.</span><span class="sxs-lookup"><span data-stu-id="6f6ff-122">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>

<span data-ttu-id="6f6ff-123">يُمكنك بعدها إدخال مصدر البيانات **السجل 2** من نوع *الحاوية*.</span><span class="sxs-lookup"><span data-stu-id="6f6ff-123">You then enter data source **Record 2** of the *Container* type.</span></span> <span data-ttu-id="6f6ff-124">يحتوي مصدر البيانات هذا على الحقول المتداخلة من النوع *الحقل المحسوب*:</span><span class="sxs-lookup"><span data-stu-id="6f6ff-124">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="6f6ff-125">**المقدار:** يحتوي هذا الحقل على تعبيرًا يُرجع قيمة من النوع *الحقيقي*.</span><span class="sxs-lookup"><span data-stu-id="6f6ff-125">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>
- <span data-ttu-id="6f6ff-126">**IsValid:** يحتوي هذا الحقل على تعبيرًا يُرجع قيمة من النوع *المنطقي*.</span><span class="sxs-lookup"><span data-stu-id="6f6ff-126">**IsValid:** This field contains an expression that returns a value of the *Boolean* type.</span></span>

<span data-ttu-id="6f6ff-127">في هذه الحالة، يُرجع التعبير `LIST('Record 1', 'Record 2')` قائمة جديدة تحتوي على سجلين.</span><span class="sxs-lookup"><span data-stu-id="6f6ff-127">In this case, the expression `LIST('Record 1', 'Record 2')` returns a new list that contains two records.</span></span> <span data-ttu-id="6f6ff-128">تتكون بنية هذه القائمة من حقل **مبلغ** واحد من النوع *الحقيقي* ، لأن هذا الحقل هو الحقل الوحيد الذي يتم عرضه في كل وسطية من الوظيفة التي تم استدعاءها.</span><span class="sxs-lookup"><span data-stu-id="6f6ff-128">The structure of this list consists of a single **Amount** field of the *Real* type, because this field is the only field that is presented in every argument of the called function.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6f6ff-129">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="6f6ff-129">Additional resources</span></span>

[<span data-ttu-id="6f6ff-130">دالات القائمة</span><span class="sxs-lookup"><span data-stu-id="6f6ff-130">List functions</span></span>](er-functions-category-list.md)
