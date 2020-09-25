---
title: POWER ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية POWER (ER).
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
ms.openlocfilehash: 080b2f9b1ada55209c9470386aceab2d3ef456af
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744565"
---
# <a name="power-er-function"></a><span data-ttu-id="2664c-103">POWER ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="2664c-103">POWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2664c-104">تُرجع الوظيفة `POWER` قيمة *حقيقية* تمثل نتيجة رفع الرقم الموجب المحدد إلى الأس المحدد.‬ </span><span class="sxs-lookup"><span data-stu-id="2664c-104">The `POWER` function returns a *Real* value that represents the result of raising the specified positive number to the specified power.</span></span>

## <a name="syntax"></a><span data-ttu-id="2664c-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="2664c-105">Syntax</span></span>

```vb
POWER (number, power)
```

## <a name="arguments"></a><span data-ttu-id="2664c-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="2664c-106">Arguments</span></span>

<span data-ttu-id="2664c-107">`number`: *عدد حقيقي* أو *صحيح*</span><span class="sxs-lookup"><span data-stu-id="2664c-107">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="2664c-108">قيمة رقمية يجب رفعها إلى الأس المُحدد.</span><span class="sxs-lookup"><span data-stu-id="2664c-108">A numeric value that must be raised to the specified power.</span></span>

<span data-ttu-id="2664c-109">`power`: *عدد حقيقي* أو *صحيح*</span><span class="sxs-lookup"><span data-stu-id="2664c-109">`power`: *Real* or *Integer*</span></span>

<span data-ttu-id="2664c-110">قيمة رقمية تمثل الأس المُحدد.</span><span class="sxs-lookup"><span data-stu-id="2664c-110">A numeric value that represents the specific power.</span></span>

## <a name="return-values"></a><span data-ttu-id="2664c-111">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="2664c-111">Return values</span></span>

<span data-ttu-id="2664c-112">*حقيقي*</span><span class="sxs-lookup"><span data-stu-id="2664c-112">*Real*</span></span>

<span data-ttu-id="2664c-113">القيمة العددية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="2664c-113">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="2664c-114">مثال1</span><span class="sxs-lookup"><span data-stu-id="2664c-114">Example 1</span></span>

<span data-ttu-id="2664c-115">يُرجع التعبير `POWER (10, 2)` **100**.</span><span class="sxs-lookup"><span data-stu-id="2664c-115">`POWER (10, 2)` returns **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="2664c-116">مثال2</span><span class="sxs-lookup"><span data-stu-id="2664c-116">Example 2</span></span>

<span data-ttu-id="2664c-117">يُرجع التعبير `POWER (4, 0.5)` **2**.</span><span class="sxs-lookup"><span data-stu-id="2664c-117">`POWER (4, 0.5)` returns **2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2664c-118">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="2664c-118">Additional resources</span></span>

[<span data-ttu-id="2664c-119">الدالات الحسابية</span><span class="sxs-lookup"><span data-stu-id="2664c-119">Mathematical functions</span></span>](er-functions-category-mathematical.md)
