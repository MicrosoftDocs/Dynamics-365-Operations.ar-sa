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
ms.openlocfilehash: 1080a1c2e30cd7ca64ea43120c11eb90d3c99416
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916328"
---
# <span data-ttu-id="45c1f-103"><a name="DAYOFYEAR">وظيفة DAYOFYEAR ER</a></span><span class="sxs-lookup"><span data-stu-id="45c1f-103"><a name="DAYOFYEAR">DAYOFYEAR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="45c1f-104">ترجع الوظيفة `DAYOFYEAR` قيمة *عدد صحيح* تمثل عدد الأيام بين 1 يناير والتاريخ المُحدد.</span><span class="sxs-lookup"><span data-stu-id="45c1f-104">The `DAYOFYEAR` function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="45c1f-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="45c1f-105">Syntax</span></span>

```
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a><span data-ttu-id="45c1f-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="45c1f-106">Arguments</span></span>

<span data-ttu-id="45c1f-107">`date`: *التاريخ*</span><span class="sxs-lookup"><span data-stu-id="45c1f-107">`date`: *Date*</span></span>

<span data-ttu-id="45c1f-108">قيمة التاريخ التي تمثل التاريخ المراد الذي سيتم استخدامه لحساب عدد الأيام.</span><span class="sxs-lookup"><span data-stu-id="45c1f-108">A date value that represents the date to use for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="45c1f-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="45c1f-109">Return values</span></span>

<span data-ttu-id="45c1f-110">*عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="45c1f-110">*Integer*</span></span>

<span data-ttu-id="45c1f-111">القيمة العددية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="45c1f-111">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="45c1f-112">مثال1</span><span class="sxs-lookup"><span data-stu-id="45c1f-112">Example 1</span></span>

<span data-ttu-id="45c1f-113">يُرجع التعبير `DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` **61**.</span><span class="sxs-lookup"><span data-stu-id="45c1f-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` returns **61**.</span></span>

## <a name="example-2"></a><span data-ttu-id="45c1f-114">مثال2</span><span class="sxs-lookup"><span data-stu-id="45c1f-114">Example 2</span></span>

<span data-ttu-id="45c1f-115">يُرجع التعبير `DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` **1**.</span><span class="sxs-lookup"><span data-stu-id="45c1f-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="45c1f-116">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="45c1f-116">Additional resources</span></span>

[<span data-ttu-id="45c1f-117">دلات التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="45c1f-117">Date and time functions</span></span>](er-functions-category-datetime.md)
