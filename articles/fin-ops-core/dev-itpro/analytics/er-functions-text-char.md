---
title: CHAR ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية CHAR (ER).
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
ms.openlocfilehash: 63df7b1ac847e12cf429467dd444450552a59162
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744951"
---
# <a name="char-er-function"></a><span data-ttu-id="d7bf4-103">CHAR ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="d7bf4-103">CHAR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d7bf4-104">تُرجع الوظيفة `CHAR` قيمة *السلسلة* التي توضح حرف واحد مُشار إليه بواسطة رقم Unicode الموحد.</span><span class="sxs-lookup"><span data-stu-id="d7bf4-104">The `CHAR` function returns a *String* value that presents a single character that is referenced by the specified Unicode number.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7bf4-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="d7bf4-105">Syntax</span></span>

```vb
CHAR (number)
```

## <a name="arguments"></a><span data-ttu-id="d7bf4-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="d7bf4-106">Arguments</span></span>

<span data-ttu-id="d7bf4-107">`number`: *عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="d7bf4-107">`number`: *Integer*</span></span>

<span data-ttu-id="d7bf4-108">رقم يتوافق مع حرف مفرد متوقع.</span><span class="sxs-lookup"><span data-stu-id="d7bf4-108">A number that corresponds to an expected single character.</span></span>

## <a name="return-values"></a><span data-ttu-id="d7bf4-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="d7bf4-109">Return values</span></span>

<span data-ttu-id="d7bf4-110">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="d7bf4-110">*String*</span></span>

<span data-ttu-id="d7bf4-111">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="d7bf4-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d7bf4-112">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="d7bf4-112">Usage notes</span></span>

<span data-ttu-id="d7bf4-113">تتوقف السلسلة التي تُرجعها هذه وظيفة على الترميز المحدد في عنصر تنسيق **FILE** الأصلي.</span><span class="sxs-lookup"><span data-stu-id="d7bf4-113">The string that this function returns depends on the encoding that is selected in the parent **FILE** format element.</span></span> <span data-ttu-id="d7bf4-114">للحصول على قائمة بالرموز المدعومة، راجع [فئة الترميز](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="d7bf4-114">For a list of the supported encodings, see [Encoding class](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span></span>

## <a name="example"></a><span data-ttu-id="d7bf4-115">مثال</span><span class="sxs-lookup"><span data-stu-id="d7bf4-115">Example</span></span>

<span data-ttu-id="d7bf4-116">تُرجع `CHAR (255)` **"ÿ"**.</span><span class="sxs-lookup"><span data-stu-id="d7bf4-116">`CHAR (255)` returns **"ÿ"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d7bf4-117">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="d7bf4-117">Additional resources</span></span>

[<span data-ttu-id="d7bf4-118">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="d7bf4-118">Text functions</span></span>](er-functions-category-text.md)
