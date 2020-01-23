---
title: 'وظيفة SESSIONNOW ER '
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية SESSIONNOW (ER).
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 4dff6daa8fbd60ef1fc84d783e428d69477aac6d
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916259"
---
# <span data-ttu-id="2f18d-103"><a name="">SESSIONNOW ER وظيفة</a></span><span class="sxs-lookup"><span data-stu-id="2f18d-103"><a name="">SESSIONNOW ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2f18d-104">ُتُرجع وظيفة `SESSIONNOW` قيمة *DateTime* التي تمثل تاريخ جلسة التطبيق الحالي والتوقيت.</span><span class="sxs-lookup"><span data-stu-id="2f18d-104">The `SESSIONNOW` function returns a *DateTime* value that represents the current application session date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f18d-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="2f18d-105">Syntax</span></span>

```
SESSIONNOW ()
```

## <a name="return-values"></a><span data-ttu-id="2f18d-106">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="2f18d-106">Return values</span></span>

<span data-ttu-id="2f18d-107">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="2f18d-107">*DateTime*</span></span>

<span data-ttu-id="2f18d-108">قيمة التاريخ/الوقت الناتجة.</span><span class="sxs-lookup"><span data-stu-id="2f18d-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="2f18d-109">مثال</span><span class="sxs-lookup"><span data-stu-id="2f18d-109">Example</span></span>

<span data-ttu-id="2f18d-110">تُرجع وظيفة `DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` قيمة تاريخ/وقت جلسة التطبيق الحالية، 24 ديسمبر 2015، كـ **"24.12.2015"**، بناءً على الثقافة الألمانية المُحددة والتنسيق المُحدد. </span><span class="sxs-lookup"><span data-stu-id="2f18d-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2f18d-111">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="2f18d-111">Additional resources</span></span>

[<span data-ttu-id="2f18d-112">دلات التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="2f18d-112">Date and time functions</span></span>](er-functions-category-datetime.md)
