---
title: SESSIONTODAY ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني SESSIONTODAY (ER).
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 6d0fcbbf1a1fb0809e3f76161314f38bcd8a74aa
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746761"
---
# <a name="sessiontoday-er-function"></a><span data-ttu-id="4971b-103">SESSIONTODAY ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="4971b-103">SESSIONTODAY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4971b-104">تُرجع وظيفة `SESSIONTODAY` قيمة *التاريخ* التي تمثل تاريخ جلسة التطبيق الحالي.</span><span class="sxs-lookup"><span data-stu-id="4971b-104">The `SESSIONTODAY` function returns a *Date* value that represents the current application session date.</span></span>

## <a name="syntax"></a><span data-ttu-id="4971b-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="4971b-105">Syntax</span></span>

```vb
SESSIONTODAY ()
```

## <a name="return-values"></a><span data-ttu-id="4971b-106">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="4971b-106">Return values</span></span>

<span data-ttu-id="4971b-107">*التاريخ*</span><span class="sxs-lookup"><span data-stu-id="4971b-107">*Date*</span></span>

<span data-ttu-id="4971b-108">قيمة التاريخ الناتجة.</span><span class="sxs-lookup"><span data-stu-id="4971b-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="4971b-109">مثال</span><span class="sxs-lookup"><span data-stu-id="4971b-109">Example</span></span>

<span data-ttu-id="4971b-110">تُرجع وظيفة `DATEFORMAT (SESSIONTODAY (), "d", "DE")` قيمة تاريخ جلسة التطبيق الحالية، 24 ديسمبر 2015، كسلسلة **"24-12-2015"**، بناءً على الثقافة الألمانية المُحددة والتنسيق المُحدد. </span><span class="sxs-lookup"><span data-stu-id="4971b-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4971b-111">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="4971b-111">Additional resources</span></span>

[<span data-ttu-id="4971b-112">دلات التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="4971b-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]