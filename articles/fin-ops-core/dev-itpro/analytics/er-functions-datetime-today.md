---
title: TODAY ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني TODAY (ER).
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
ms.openlocfilehash: 45ee4282acf4d6a5febe4b74b6955410e73e86a3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746737"
---
# <a name="today-er-function"></a><span data-ttu-id="2cc95-103">TODAY ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="2cc95-103">TODAY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2cc95-104">تُرجع الوظيفة `TODAY` قيمة *التاريخ* التي تمثل تاريخ جلسة الخادم الحالي.</span><span class="sxs-lookup"><span data-stu-id="2cc95-104">The `TODAY` function returns a *Date* value that represents the current application server date.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cc95-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="2cc95-105">Syntax</span></span>

```xpp
TODAY ()
```

## <a name="return-values"></a><span data-ttu-id="2cc95-106">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="2cc95-106">Return values</span></span>

<span data-ttu-id="2cc95-107">*التاريخ*</span><span class="sxs-lookup"><span data-stu-id="2cc95-107">*Date*</span></span>

<span data-ttu-id="2cc95-108">قيمة التاريخ الناتجة.</span><span class="sxs-lookup"><span data-stu-id="2cc95-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="2cc95-109">مثال</span><span class="sxs-lookup"><span data-stu-id="2cc95-109">Example</span></span>

<span data-ttu-id="2cc95-110">تُرجع وظيفة `DATEFORMAT (TODAY (), "dd-MM-yyyy")` تاريخ خادم التطبيق الحالي، 24 ديسمبر 2015، كسلسلة **"24-12-2015"**، بناءً على التنسيق المخصص المُحدد. </span><span class="sxs-lookup"><span data-stu-id="2cc95-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2cc95-111">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="2cc95-111">Additional resources</span></span>

[<span data-ttu-id="2cc95-112">دلات التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="2cc95-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]