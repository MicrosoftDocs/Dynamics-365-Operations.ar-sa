---
title: ROUND ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية ROUND (ER).
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 6751c1321fc71419fa8b153145a057371e0f7af5
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041597"
---
# <span data-ttu-id="963af-103"><a name="ROUND">ROUND ER وظيفة</a></span><span class="sxs-lookup"><span data-stu-id="963af-103"><a name="ROUND">ROUND ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="963af-104">تُرجع الوظيفة `ROUND` الرقم المُحدد كقيمة *حقيقية* بعد أن تم تقريبه إلى عدد المنازل العشرة المُحدد.</span><span class="sxs-lookup"><span data-stu-id="963af-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="963af-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="963af-105">Syntax</span></span>

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="963af-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="963af-106">Arguments</span></span>

<span data-ttu-id="963af-107">`number`: *حقيقي*</span><span class="sxs-lookup"><span data-stu-id="963af-107">`number`: *Real*</span></span>

<span data-ttu-id="963af-108">قيمة رقمية يجب تقريبها.</span><span class="sxs-lookup"><span data-stu-id="963af-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="963af-109">`decimals`: *عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="963af-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="963af-110">قيمة رقمية تمثل عدد المنازل العشرية.</span><span class="sxs-lookup"><span data-stu-id="963af-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="963af-111">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="963af-111">Return values</span></span>

<span data-ttu-id="963af-112">*حقيقي*</span><span class="sxs-lookup"><span data-stu-id="963af-112">*Real*</span></span>

<span data-ttu-id="963af-113">القيمة العددية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="963af-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="963af-114">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="963af-114">Usage notes</span></span>

<span data-ttu-id="963af-115">إذا كانت قيمة وسيطة `decimals` أكبر من 0 (صفر)، فيتم تقريب الرقم المحدد إلى عدد المنازل العشرية العديدة.</span><span class="sxs-lookup"><span data-stu-id="963af-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="963af-116">إذا كانت قيمة الوسيطة `decimals` المحددة تساوي **0** (صفر) فيتم تقريب الرقم المحدد إلى أقرب عدد صحيح.</span><span class="sxs-lookup"><span data-stu-id="963af-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest integer.</span></span>

<span data-ttu-id="963af-117">إذا كانت قيمة وسيطة `decimals` المحددة أقل من 0 (صفر)، فيتم تقريب الرقم المحدد إلى يسار الفاصلة العشرية.</span><span class="sxs-lookup"><span data-stu-id="963af-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="963af-118">مثال1</span><span class="sxs-lookup"><span data-stu-id="963af-118">Example 1</span></span>

<span data-ttu-id="963af-119">تقرّب `ROUND (1200.767, 2)` إلى منزلتين عشريتين وترجع **1200.77**.</span><span class="sxs-lookup"><span data-stu-id="963af-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="963af-120">مثال2</span><span class="sxs-lookup"><span data-stu-id="963af-120">Example 2</span></span>

<span data-ttu-id="963af-121">تُقربّ `ROUND (1200.767, -3)` إلى أقرب مضاعف من 1,000 وترجع **1000**.</span><span class="sxs-lookup"><span data-stu-id="963af-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="963af-122">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="963af-122">Additional resources</span></span>

[<span data-ttu-id="963af-123">الدالات الحسابية</span><span class="sxs-lookup"><span data-stu-id="963af-123">Mathematical functions</span></span>](er-functions-category-mathematical.md)
