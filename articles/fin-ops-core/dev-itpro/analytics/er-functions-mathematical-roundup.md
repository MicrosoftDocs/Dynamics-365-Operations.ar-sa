---
title: ROUNDUP ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية ROUNDUP (ER).
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ed86e2a848248dd8f2fc99401d12e0a162bf20a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686824"
---
# <a name="roundup-er-function"></a><span data-ttu-id="78aea-103">ROUNDUP ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="78aea-103">ROUNDUP ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="78aea-104">تُرجع الوظيفة `ROUNDUP` الرقم المُحدد كقيمة *حقيقية* بعد أن تم تقريبه لأعلى إلى عدد المنازل العشرة المُحدد.</span><span class="sxs-lookup"><span data-stu-id="78aea-104">The `ROUNDUP` function returns the specified number as a *Real* value after it has been rounded up to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="78aea-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="78aea-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="78aea-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="78aea-106">Arguments</span></span>

<span data-ttu-id="78aea-107">`number`: *حقيقي*</span><span class="sxs-lookup"><span data-stu-id="78aea-107">`number`: *Real*</span></span>

<span data-ttu-id="78aea-108">قيمة رقمية يجب تقريبها لأعلى.</span><span class="sxs-lookup"><span data-stu-id="78aea-108">A numeric value that must be rounded up.</span></span>

<span data-ttu-id="78aea-109">`decimals`: *عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="78aea-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="78aea-110">قيمة رقمية تمثل عدد المنازل العشرية.</span><span class="sxs-lookup"><span data-stu-id="78aea-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="78aea-111">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="78aea-111">Return values</span></span>

<span data-ttu-id="78aea-112">*حقيقي*</span><span class="sxs-lookup"><span data-stu-id="78aea-112">*Real*</span></span>

<span data-ttu-id="78aea-113">القيمة العددية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="78aea-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="78aea-114">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="78aea-114">Usage notes</span></span>

<span data-ttu-id="78aea-115">تعمل هذه الدالة مثل الدالة [ROUND](er-functions-mathematical-round.md)، إلا أنها تقرّب دائمًا الرقم المحدد لأعلى (بعيدًا عن الصفر).</span><span class="sxs-lookup"><span data-stu-id="78aea-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number up (away from zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="78aea-116">مثال1</span><span class="sxs-lookup"><span data-stu-id="78aea-116">Example 1</span></span>

<span data-ttu-id="78aea-117">تقرّب `ROUNDUP (1200.763, 2)` لأعلى إلى منزلتين عشريتين وترجع **1200.77**.</span><span class="sxs-lookup"><span data-stu-id="78aea-117">`ROUNDUP (1200.763, 2)` rounds up to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="78aea-118">مثال2</span><span class="sxs-lookup"><span data-stu-id="78aea-118">Example 2</span></span>

<span data-ttu-id="78aea-119">تُقربّ `ROUNDUP (1200.767, -3)` لأعلى إلى أقرب مضاعف من 1,000 وترجع **2000**.</span><span class="sxs-lookup"><span data-stu-id="78aea-119">`ROUNDUP (1200.767, -3)` rounds up to the nearest multiple of 1,000 and returns **2000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="78aea-120">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="78aea-120">Additional resources</span></span>

[<span data-ttu-id="78aea-121">الدالات الحسابية</span><span class="sxs-lookup"><span data-stu-id="78aea-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)
