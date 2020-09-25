---
title: ROUNDDOWN ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية ROUNDDOWN (ER).
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
ms.openlocfilehash: 7ac559983609d4fdb80c9ac70d84031e4a231889
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744517"
---
# <a name="rounddown-er-function"></a><span data-ttu-id="68fc6-103">ROUNDDOWN ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="68fc6-103">ROUNDDOWN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="68fc6-104">تُرجع الوظيفة `ROUNDDOWN` الرقم المُحدد كقيمة *حقيقية* بعد أن تم تقريبه لأسفل إلى عدد المنازل العشرة المُحدد.</span><span class="sxs-lookup"><span data-stu-id="68fc6-104">The `ROUNDDOWN` function returns the specified number as a *Real* value after it has been rounded down to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="68fc6-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="68fc6-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="68fc6-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="68fc6-106">Arguments</span></span>

<span data-ttu-id="68fc6-107">`number`: *حقيقي*</span><span class="sxs-lookup"><span data-stu-id="68fc6-107">`number`: *Real*</span></span>

<span data-ttu-id="68fc6-108">قيمة رقمية يجب تقريبها لأسفل.</span><span class="sxs-lookup"><span data-stu-id="68fc6-108">A numeric value that must be rounded down.</span></span>

<span data-ttu-id="68fc6-109">`decimals`: *عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="68fc6-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="68fc6-110">قيمة رقمية تمثل عدد المنازل العشرية.</span><span class="sxs-lookup"><span data-stu-id="68fc6-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="68fc6-111">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="68fc6-111">Return values</span></span>

<span data-ttu-id="68fc6-112">*حقيقي*</span><span class="sxs-lookup"><span data-stu-id="68fc6-112">*Real*</span></span>

<span data-ttu-id="68fc6-113">القيمة العددية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="68fc6-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="68fc6-114">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="68fc6-114">Usage notes</span></span>

<span data-ttu-id="68fc6-115">تعمل هذه الدالة مثل الدالة [ROUND](er-functions-mathematical-round.md)، إلا أنها تقرّب دائمًا الرقم المحدد لأسفل (في اتجاه الصفر).</span><span class="sxs-lookup"><span data-stu-id="68fc6-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number down (toward zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="68fc6-116">مثال1</span><span class="sxs-lookup"><span data-stu-id="68fc6-116">Example 1</span></span>

<span data-ttu-id="68fc6-117">تقرّب `ROUNDDOWN (1200.767, 2)` لأسفل إلى منزلتين عشريتين وترجع **1200.76**.</span><span class="sxs-lookup"><span data-stu-id="68fc6-117">`ROUNDDOWN (1200.767, 2)` rounds down to two decimal places and returns **1200.76**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="68fc6-118">مثال2</span><span class="sxs-lookup"><span data-stu-id="68fc6-118">Example 2</span></span>

<span data-ttu-id="68fc6-119">تُقربّ `ROUNDDOWN (1700.767, -3)` لأسفل إلى أقرب مضاعف من 1,000 وترجع **1000**.</span><span class="sxs-lookup"><span data-stu-id="68fc6-119">`ROUNDDOWN (1700.767, -3)` rounds down to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="68fc6-120">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="68fc6-120">Additional resources</span></span>

[<span data-ttu-id="68fc6-121">الدالات الحسابية</span><span class="sxs-lookup"><span data-stu-id="68fc6-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)
