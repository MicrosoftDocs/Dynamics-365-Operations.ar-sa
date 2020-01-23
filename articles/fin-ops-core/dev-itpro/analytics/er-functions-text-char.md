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
ms.openlocfilehash: d42afcf97690351763138fd9e16265aa104a6bc4
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915730"
---
# <span data-ttu-id="212be-103"><a name="CHAR">CHAR ER وظيفة</a></span><span class="sxs-lookup"><span data-stu-id="212be-103"><a name="CHAR">CHAR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="212be-104">تُرجع الوظيفة `CHAR` قيمة *السلسلة* التي توضح حرف واحد مُشار إليه بواسطة رقم Unicode الموحد.</span><span class="sxs-lookup"><span data-stu-id="212be-104">The `CHAR` function returns a *String* value that presents a single character that is referenced by the specified Unicode number.</span></span>

## <a name="syntax"></a><span data-ttu-id="212be-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="212be-105">Syntax</span></span>

```
CHAR (number)
```

## <a name="arguments"></a><span data-ttu-id="212be-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="212be-106">Arguments</span></span>

<span data-ttu-id="212be-107">`number`: *عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="212be-107">`number`: *Integer*</span></span>

<span data-ttu-id="212be-108">رقم يتوافق مع حرف مفرد متوقع.</span><span class="sxs-lookup"><span data-stu-id="212be-108">A number that corresponds to an expected single character.</span></span>

## <a name="return-values"></a><span data-ttu-id="212be-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="212be-109">Return values</span></span>

<span data-ttu-id="212be-110">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="212be-110">*String*</span></span>

<span data-ttu-id="212be-111">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="212be-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="212be-112">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="212be-112">Usage notes</span></span>

<span data-ttu-id="212be-113">تتوقف السلسلة التي تُرجعها هذه وظيفة على الترميز المحدد في عنصر تنسيق **FILE** الأصلي.</span><span class="sxs-lookup"><span data-stu-id="212be-113">The string that this function returns depends on the encoding that is selected in the parent **FILE** format element.</span></span> <span data-ttu-id="212be-114">للحصول على قائمة بالرموز المدعومة، راجع [فئة الترميز](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="212be-114">For a list of the supported encodings, see [Encoding class](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span></span>

## <a name="example"></a><span data-ttu-id="212be-115">مثال</span><span class="sxs-lookup"><span data-stu-id="212be-115">Example</span></span>

<span data-ttu-id="212be-116">تُرجع `CHAR (255)` **"ÿ"**.</span><span class="sxs-lookup"><span data-stu-id="212be-116">`CHAR (255)` returns **"ÿ"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="212be-117">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="212be-117">Additional resources</span></span>

[<span data-ttu-id="212be-118">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="212be-118">Text functions</span></span>](er-functions-category-text.md)
