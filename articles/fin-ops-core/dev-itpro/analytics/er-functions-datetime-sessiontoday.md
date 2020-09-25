---
title: SESSIONTODAY ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني SESSIONTODAY (ER).
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 2aa3d5e34e6dcd9b5d4a3fe3f21d7e3285adbcad
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745407"
---
# <a name="sessiontoday-er-function"></a><span data-ttu-id="ce47f-103">SESSIONTODAY ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="ce47f-103">SESSIONTODAY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce47f-104">تُرجع وظيفة `SESSIONTODAY` قيمة *التاريخ* التي تمثل تاريخ جلسة التطبيق الحالي.</span><span class="sxs-lookup"><span data-stu-id="ce47f-104">The `SESSIONTODAY` function returns a *Date* value that represents the current application session date.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce47f-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="ce47f-105">Syntax</span></span>

```vb
SESSIONTODAY ()
```

## <a name="return-values"></a><span data-ttu-id="ce47f-106">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="ce47f-106">Return values</span></span>

<span data-ttu-id="ce47f-107">*التاريخ*</span><span class="sxs-lookup"><span data-stu-id="ce47f-107">*Date*</span></span>

<span data-ttu-id="ce47f-108">قيمة التاريخ الناتجة.</span><span class="sxs-lookup"><span data-stu-id="ce47f-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="ce47f-109">مثال</span><span class="sxs-lookup"><span data-stu-id="ce47f-109">Example</span></span>

<span data-ttu-id="ce47f-110">تُرجع وظيفة `DATEFORMAT (SESSIONTODAY (), "d", "DE")` قيمة تاريخ جلسة التطبيق الحالية، 24 ديسمبر 2015، كسلسلة **"24-12-2015"**، بناءً على الثقافة الألمانية المُحددة والتنسيق المُحدد. </span><span class="sxs-lookup"><span data-stu-id="ce47f-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ce47f-111">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="ce47f-111">Additional resources</span></span>

[<span data-ttu-id="ce47f-112">دلات التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="ce47f-112">Date and time functions</span></span>](er-functions-category-datetime.md)
