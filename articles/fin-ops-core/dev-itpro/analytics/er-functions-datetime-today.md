---
title: TODAY ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني TODAY (ER).
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a93a9171456fb69e16c8104b0afb9ad485311b1a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683785"
---
# <a name="today-er-function"></a><span data-ttu-id="128bc-103">TODAY ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="128bc-103">TODAY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="128bc-104">تُرجع الوظيفة `TODAY` قيمة *التاريخ* التي تمثل تاريخ جلسة الخادم الحالي.</span><span class="sxs-lookup"><span data-stu-id="128bc-104">The `TODAY` function returns a *Date* value that represents the current application server date.</span></span>

## <a name="syntax"></a><span data-ttu-id="128bc-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="128bc-105">Syntax</span></span>

```xpp
TODAY ()
```

## <a name="return-values"></a><span data-ttu-id="128bc-106">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="128bc-106">Return values</span></span>

<span data-ttu-id="128bc-107">*التاريخ*</span><span class="sxs-lookup"><span data-stu-id="128bc-107">*Date*</span></span>

<span data-ttu-id="128bc-108">قيمة التاريخ الناتجة.</span><span class="sxs-lookup"><span data-stu-id="128bc-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="128bc-109">مثال</span><span class="sxs-lookup"><span data-stu-id="128bc-109">Example</span></span>

<span data-ttu-id="128bc-110">تُرجع وظيفة `DATEFORMAT (TODAY (), "dd-MM-yyyy")` تاريخ خادم التطبيق الحالي، 24 ديسمبر 2015، كسلسلة **"24-12-2015"**، بناءً على التنسيق المخصص المُحدد. </span><span class="sxs-lookup"><span data-stu-id="128bc-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="128bc-111">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="128bc-111">Additional resources</span></span>

[<span data-ttu-id="128bc-112">دلات التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="128bc-112">Date and time functions</span></span>](er-functions-category-datetime.md)
