---
title: INDEX ER الوظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية INDEX (ER).
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
ms.openlocfilehash: 45e95751e3adfe6aa208daaba774a349216e1f1f
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042057"
---
# <span data-ttu-id="6c7fc-103"><a name="INDEX">INDEX ER الوظيفة</a></span><span class="sxs-lookup"><span data-stu-id="6c7fc-103"><a name="INDEX">INDEX ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6c7fc-104">تقوم الوظيفة `INDEX` بإرجاع قيمة *الحاوية (سجل)* المُحددة باستخدام الفهرس الرقمي المُحدد في القائمة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="6c7fc-104">The `INDEX` function returns a *Container (record)* value that is selected by using the specified numeric index in the specified list.</span></span> <span data-ttu-id="6c7fc-105">إذا كان هذا الفهرس خارج النطاق للسجلات في القائمة المُحددة، يتم طرح استثناء.</span><span class="sxs-lookup"><span data-stu-id="6c7fc-105">If the index is out of range for the records in the specified list, an exception is thrown.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c7fc-106">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="6c7fc-106">Syntax</span></span>

```vb
INDEX (list, index)
```

## <a name="arguments"></a><span data-ttu-id="6c7fc-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="6c7fc-107">Arguments</span></span>

<span data-ttu-id="6c7fc-108">`list`: *قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="6c7fc-108">`list`: *Record list*</span></span>

<span data-ttu-id="6c7fc-109">مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.</span><span class="sxs-lookup"><span data-stu-id="6c7fc-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="6c7fc-110">`index`: *عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="6c7fc-110">`index`: *Integer*</span></span>

<span data-ttu-id="6c7fc-111">فهرس رقمي يشير إلى موضع السجل المطلوب في القائمة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="6c7fc-111">A numeric index that indicates the position of the desired record in the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="6c7fc-112">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="6c7fc-112">Return values</span></span>

<span data-ttu-id="6c7fc-113">*حاوية (سجل)*</span><span class="sxs-lookup"><span data-stu-id="6c7fc-113">*Container (record)*</span></span>

<span data-ttu-id="6c7fc-114">قيمة السجل الناتجة.</span><span class="sxs-lookup"><span data-stu-id="6c7fc-114">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="6c7fc-115">مثال1</span><span class="sxs-lookup"><span data-stu-id="6c7fc-115">Example 1</span></span>

<span data-ttu-id="6c7fc-116">إذا أدخلت مصدر البيانات **DS** من النوع *حقل محتسب* ، يحتوي على التعبير `SPLIT ("A|B|C", "|")` ، يُرجع التعبير `DS.Value` القيمة النصية **"B"** للسجل الثاني من قائمة النص هذه.</span><span class="sxs-lookup"><span data-stu-id="6c7fc-116">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `DS.Value` returns the text value **"B"** for the second record of this record list.</span></span> <span data-ttu-id="6c7fc-117">يُرجع التعبير `INDEX (SPLIT ("A|B|C", "|"), 2).Value` القيمة النصية **"B"** أيضًا.</span><span class="sxs-lookup"><span data-stu-id="6c7fc-117">The expression `INDEX (SPLIT ("A|B|C", "|"), 2).Value` also returns the text value **"B"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="6c7fc-118">مثال2</span><span class="sxs-lookup"><span data-stu-id="6c7fc-118">Example 2</span></span>

<span data-ttu-id="6c7fc-119">إذا قمت بإدخال مصدر البيانات **DS** من النوع *الحقل المحسوب* ، ويحتوي على التعبير `SPLIT ("A|B|C", "|")` ، يطرح التعبير `INDEX (SPLIT ("A|B|C", "|"), 4).Value` استثناءً في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="6c7fc-119">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `INDEX (SPLIT ("A|B|C", "|"), 4).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6c7fc-120">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="6c7fc-120">Additional resources</span></span>

[<span data-ttu-id="6c7fc-121">دالات القائمة</span><span class="sxs-lookup"><span data-stu-id="6c7fc-121">List functions</span></span>](er-functions-category-list.md)
