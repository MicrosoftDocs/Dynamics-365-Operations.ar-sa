---
title: NUMBERFORMAT ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية NUMBERFORMAT (ER).
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: 8de57d8b0a45b8b58849a24f2d8f0cde41e0ea3a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746189"
---
# <a name="numberformat-er-function"></a><span data-ttu-id="0e554-103">NUMBERFORMAT ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="0e554-103">NUMBERFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0e554-104">تقوم وظيفة `NUMBERFORMAT` بإرجاع قيمة *سلسلة* تمثل الرقم المحدد في التنسيق المُحدد وفي [الثقافة](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) المُحددة بشكل اختياري.</span><span class="sxs-lookup"><span data-stu-id="0e554-104">The `NUMBERFORMAT` function returns a *String* value that presents the specified number in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="0e554-105">لمزيد من المعلومات حول التنسيقات المعتمدة، راجع [قياسي](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) و [مخصص](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="0e554-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="0e554-106">بناء الجملة 1</span><span class="sxs-lookup"><span data-stu-id="0e554-106">Syntax 1</span></span>

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a><span data-ttu-id="0e554-107">بناء الجملة 2</span><span class="sxs-lookup"><span data-stu-id="0e554-107">Syntax 2</span></span>

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="0e554-108">الوسائط</span><span class="sxs-lookup"><span data-stu-id="0e554-108">Arguments</span></span>

<span data-ttu-id="0e554-109">`number`: *عدد صحيح* أو *حقيقي*</span><span class="sxs-lookup"><span data-stu-id="0e554-109">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="0e554-110">قيمة رقمية تُحدد الرقم الذي يجب تنسيقه.</span><span class="sxs-lookup"><span data-stu-id="0e554-110">A numeric value that specifies the number that must be formatted.</span></span>

<span data-ttu-id="0e554-111">`format`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="0e554-111">`format` : *String*</span></span>

<span data-ttu-id="0e554-112">قيمة *سلسلة* تمثل التنسيق.</span><span class="sxs-lookup"><span data-stu-id="0e554-112">A *String* value that represents the format.</span></span>

<span data-ttu-id="0e554-113">`culture`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="0e554-113">`culture`: *String*</span></span>

<span data-ttu-id="0e554-114">قيمة *السلسلة* التي تمثل الثقافة لاستخدامها للتنسيق.</span><span class="sxs-lookup"><span data-stu-id="0e554-114">A *String* value that represents the culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="0e554-115">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="0e554-115">Return values</span></span>

<span data-ttu-id="0e554-116">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="0e554-116">*String*</span></span>

<span data-ttu-id="0e554-117">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="0e554-117">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0e554-118">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="0e554-118">Usage notes</span></span>

<span data-ttu-id="0e554-119">إذا لم يتم تعريف الثقافة كوسيطه للوظيفة المسماة، فإن السياق الذي يتم فيه تشغيل هذه الوظيفة يحدد الثقافة التي يتم استخدامها لتنسيق الأرقام.</span><span class="sxs-lookup"><span data-stu-id="0e554-119">If the culture isn't defined as an argument of the called function, the context that this function is run in determines the culture that is used to format numbers.</span></span>

## <a name="example-1"></a><span data-ttu-id="0e554-120">مثال1</span><span class="sxs-lookup"><span data-stu-id="0e554-120">Example 1</span></span>

<span data-ttu-id="0e554-121">للثقافة **EN-US**, ترجع `NUMBERFORMAT (0.45, "p")` القيمة **"45.00 %"**، وترجع `NUMBERFORMAT (10.45, "#")` القيمة **"10"**.</span><span class="sxs-lookup"><span data-stu-id="0e554-121">For the **EN-US** culture, `NUMBERFORMAT (0.45, "p")` returns **"45.00 %"**, and `NUMBERFORMAT (10.45, "#")` returns **"10"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="0e554-122">مثال2</span><span class="sxs-lookup"><span data-stu-id="0e554-122">Example 2</span></span>

<span data-ttu-id="0e554-123">تُرجع`NUMBERFORMAT (10/3, "F2", "de")` القيمة **3،33**، بينما تُرجع `NUMBERFORMAT (10/3, "F2", "en-us")` القيمة **3.33**.</span><span class="sxs-lookup"><span data-stu-id="0e554-123">`NUMBERFORMAT (10/3, "F2", "de")` returns **3,33**, whereas `NUMBERFORMAT (10/3, "F2", "en-us")` returns **3.33**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0e554-124">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="0e554-124">Additional resources</span></span>

[<span data-ttu-id="0e554-125">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="0e554-125">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]