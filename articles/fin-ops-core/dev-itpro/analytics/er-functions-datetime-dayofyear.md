---
title: وظيفة DAYOFYEAR ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية DAYOFYEAR (ER).
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
ms.openlocfilehash: 755f5f1de28f95ed682648caf47155ad71c8f4b0
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745479"
---
# <a name="dayofyear-er-function"></a><span data-ttu-id="909ae-103">وظيفة DAYOFYEAR ER</span><span class="sxs-lookup"><span data-stu-id="909ae-103">DAYOFYEAR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="909ae-104">ترجع الوظيفة `DAYOFYEAR` قيمة *عدد صحيح* تمثل عدد الأيام بين 1 يناير والتاريخ المُحدد.</span><span class="sxs-lookup"><span data-stu-id="909ae-104">The `DAYOFYEAR` function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="909ae-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="909ae-105">Syntax</span></span>

```vb
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a><span data-ttu-id="909ae-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="909ae-106">Arguments</span></span>

<span data-ttu-id="909ae-107">`date`: *التاريخ*</span><span class="sxs-lookup"><span data-stu-id="909ae-107">`date`: *Date*</span></span>

<span data-ttu-id="909ae-108">قيمة التاريخ التي تمثل التاريخ المراد الذي سيتم استخدامه لحساب عدد الأيام.</span><span class="sxs-lookup"><span data-stu-id="909ae-108">A date value that represents the date to use for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="909ae-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="909ae-109">Return values</span></span>

<span data-ttu-id="909ae-110">*عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="909ae-110">*Integer*</span></span>

<span data-ttu-id="909ae-111">القيمة العددية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="909ae-111">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="909ae-112">مثال1</span><span class="sxs-lookup"><span data-stu-id="909ae-112">Example 1</span></span>

<span data-ttu-id="909ae-113">يُرجع التعبير `DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` **61**.</span><span class="sxs-lookup"><span data-stu-id="909ae-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` returns **61**.</span></span>

## <a name="example-2"></a><span data-ttu-id="909ae-114">مثال2</span><span class="sxs-lookup"><span data-stu-id="909ae-114">Example 2</span></span>

<span data-ttu-id="909ae-115">يُرجع التعبير `DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` **1**.</span><span class="sxs-lookup"><span data-stu-id="909ae-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="909ae-116">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="909ae-116">Additional resources</span></span>

[<span data-ttu-id="909ae-117">دلات التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="909ae-117">Date and time functions</span></span>](er-functions-category-datetime.md)
