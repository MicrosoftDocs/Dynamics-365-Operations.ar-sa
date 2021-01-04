---
title: STRINGJOIN ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية STRINGJOIN (ER).
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 586dbcb98d237325188f4b0384580613ab7a9347
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683714"
---
# <a name="stringjoin-er-function"></a><span data-ttu-id="d13fb-103">STRINGJOIN ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="d13fb-103">STRINGJOIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d13fb-104">تُرجع الوظيفة `STRINGJOIN` قيمة *السلسلة* التي تتكون من القيم المتصلة للحقل المُحدد من القائمة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="d13fb-104">The `STRINGJOIN` function returns a *String* value that consists of concatenated values of the specified field from the specified list.</span></span> <span data-ttu-id="d13fb-105">يُمكن فصل القيم بالمحدد المعين.</span><span class="sxs-lookup"><span data-stu-id="d13fb-105">The values can be separated by the specified delimiter.</span></span>

## <a name="syntax"></a><span data-ttu-id="d13fb-106">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="d13fb-106">Syntax</span></span>

```vb
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a><span data-ttu-id="d13fb-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="d13fb-107">Arguments</span></span>

<span data-ttu-id="d13fb-108">`list`: *قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="d13fb-108">`list`: *Record list*</span></span>

<span data-ttu-id="d13fb-109">مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.</span><span class="sxs-lookup"><span data-stu-id="d13fb-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="d13fb-110">`field`: *الحقل*</span><span class="sxs-lookup"><span data-stu-id="d13fb-110">`field`: *Field*</span></span>

<span data-ttu-id="d13fb-111">المسار الصالح لحقل من نوع بيانات *السلسلة* في القائمة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="d13fb-111">The valid path of a field of the *String* data type in the specified list.</span></span>

<span data-ttu-id="d13fb-112">`delimiter`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="d13fb-112">`delimiter`: *String*</span></span>

<span data-ttu-id="d13fb-113">مُحدد يستخدم لفصل السلاسل الفرعية.</span><span class="sxs-lookup"><span data-stu-id="d13fb-113">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="d13fb-114">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="d13fb-114">Return values</span></span>

<span data-ttu-id="d13fb-115">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="d13fb-115">*String*</span></span>

<span data-ttu-id="d13fb-116">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="d13fb-116">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="d13fb-117">مثال</span><span class="sxs-lookup"><span data-stu-id="d13fb-117">Example</span></span>

<span data-ttu-id="d13fb-118">إذا قمت بإدخال `SPLIT("abc" , 1)` كمصدر بيانات **DS**، يُرجع التعبير `STRINGJOIN (DS, DS.Value, "-")` **"a-b-c"**.</span><span class="sxs-lookup"><span data-stu-id="d13fb-118">If you enter `SPLIT("abc" , 1)` as data source **DS**, the expression `STRINGJOIN (DS, DS.Value, "-")` returns **"a-b-c"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d13fb-119">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="d13fb-119">Additional resources</span></span>

[<span data-ttu-id="d13fb-120">دالات القائمة</span><span class="sxs-lookup"><span data-stu-id="d13fb-120">List functions</span></span>](er-functions-category-list.md)
