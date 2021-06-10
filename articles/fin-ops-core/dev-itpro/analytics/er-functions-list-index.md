---
title: INDEX ER الوظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية INDEX (ER).
author: NickSelin
ms.date: 05/20/2021
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
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a0fdb8958670efe8e2a37cee183bf836fa6c7e8
ms.sourcegitcommit: 047b0503868cc7d7b21868e24405d76af35db747
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/21/2021
ms.locfileid: "6087741"
---
# <a name="index-er-function"></a><span data-ttu-id="38ae0-103">INDEX ER الوظيفة</span><span class="sxs-lookup"><span data-stu-id="38ae0-103">INDEX ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="38ae0-104">تقوم الوظيفة `INDEX` بإرجاع قيمة *الحاوية (سجل)* المُحددة باستخدام الفهرس الرقمي المُحدد في القائمة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="38ae0-104">The `INDEX` function returns a *Container (record)* value that is selected by using the specified numeric index in the specified list.</span></span> <span data-ttu-id="38ae0-105">إذا كان هذا الفهرس خارج النطاق للسجلات في القائمة المُحددة، يتم طرح استثناء.</span><span class="sxs-lookup"><span data-stu-id="38ae0-105">If the index is out of range for the records in the specified list, an exception is thrown.</span></span>

## <a name="syntax"></a><span data-ttu-id="38ae0-106">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="38ae0-106">Syntax</span></span>

```vb
INDEX (list, index)
```

## <a name="arguments"></a><span data-ttu-id="38ae0-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="38ae0-107">Arguments</span></span>

<span data-ttu-id="38ae0-108">`list`: *قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="38ae0-108">`list`: *Record list*</span></span>

<span data-ttu-id="38ae0-109">مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.</span><span class="sxs-lookup"><span data-stu-id="38ae0-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="38ae0-110">`index`: *عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="38ae0-110">`index`: *Integer*</span></span>

<span data-ttu-id="38ae0-111">فهرس رقمي يشير إلى موضع السجل المطلوب في القائمة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="38ae0-111">A numeric index that indicates the position of the desired record in the specified list.</span></span>

> [!NOTE]
> <span data-ttu-id="38ae0-112">وبسبب استخدام ترقيم يستند إلى واحد لهذه الوظيفة، حدد القيمة **1** لإرجاع السجل الأول من القائمة المحددة.</span><span class="sxs-lookup"><span data-stu-id="38ae0-112">Because one-based numbering is used for this function, specify the value **1** to return the first record of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="38ae0-113">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="38ae0-113">Return values</span></span>

<span data-ttu-id="38ae0-114">*حاوية (سجل)*</span><span class="sxs-lookup"><span data-stu-id="38ae0-114">*Container (record)*</span></span>

<span data-ttu-id="38ae0-115">قيمة السجل الناتجة.</span><span class="sxs-lookup"><span data-stu-id="38ae0-115">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="38ae0-116">مثال1</span><span class="sxs-lookup"><span data-stu-id="38ae0-116">Example 1</span></span>

<span data-ttu-id="38ae0-117">إذا أدخلت مصدر البيانات **DS** من النوع *حقل محتسب* ، يحتوي على التعبير `SPLIT ("A|B|C", "|")` ، يُرجع التعبير `DS.Value` القيمة النصية **"B"** للسجل الثاني من قائمة النص هذه.</span><span class="sxs-lookup"><span data-stu-id="38ae0-117">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `DS.Value` returns the text value **"B"** for the second record of this record list.</span></span> <span data-ttu-id="38ae0-118">يُرجع التعبير `INDEX (SPLIT ("A|B|C", "|"), 2).Value` القيمة النصية **"B"** أيضًا.</span><span class="sxs-lookup"><span data-stu-id="38ae0-118">The expression `INDEX (SPLIT ("A|B|C", "|"), 2).Value` also returns the text value **"B"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="38ae0-119">مثال2</span><span class="sxs-lookup"><span data-stu-id="38ae0-119">Example 2</span></span>

<span data-ttu-id="38ae0-120">إذا قمت بإدخال مصدر البيانات **DS** من النوع *الحقل المحسوب* ، ويحتوي على التعبير `SPLIT ("A|B|C", "|")` ، يطرح التعبير `INDEX (SPLIT ("A|B|C", "|"), 4).Value` استثناءً في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="38ae0-120">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `INDEX (SPLIT ("A|B|C", "|"), 4).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="38ae0-121">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="38ae0-121">Additional resources</span></span>

[<span data-ttu-id="38ae0-122">دالات القائمة</span><span class="sxs-lookup"><span data-stu-id="38ae0-122">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
