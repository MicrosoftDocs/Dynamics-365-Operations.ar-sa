---
title: ROUNDUP ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية ROUNDUP (ER).
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: d23a984bd59c4d2d37c407e3fcfed9c7017dcc7f
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569325"
---
# <a name="roundup-er-function"></a><span data-ttu-id="77a13-103">ROUNDUP ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="77a13-103">ROUNDUP ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="77a13-104">تُرجع الوظيفة `ROUNDUP` الرقم المُحدد كقيمة *حقيقية* بعد أن تم تقريبه لأعلى إلى عدد المنازل العشرة المُحدد.</span><span class="sxs-lookup"><span data-stu-id="77a13-104">The `ROUNDUP` function returns the specified number as a *Real* value after it has been rounded up to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="77a13-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="77a13-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="77a13-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="77a13-106">Arguments</span></span>

<span data-ttu-id="77a13-107">`number`: *حقيقي*</span><span class="sxs-lookup"><span data-stu-id="77a13-107">`number`: *Real*</span></span>

<span data-ttu-id="77a13-108">قيمة رقمية يجب تقريبها لأعلى.</span><span class="sxs-lookup"><span data-stu-id="77a13-108">A numeric value that must be rounded up.</span></span>

<span data-ttu-id="77a13-109">`decimals`: *عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="77a13-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="77a13-110">قيمة رقمية تمثل عدد المنازل العشرية.</span><span class="sxs-lookup"><span data-stu-id="77a13-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="77a13-111">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="77a13-111">Return values</span></span>

<span data-ttu-id="77a13-112">*حقيقي*</span><span class="sxs-lookup"><span data-stu-id="77a13-112">*Real*</span></span>

<span data-ttu-id="77a13-113">القيمة العددية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="77a13-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="77a13-114">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="77a13-114">Usage notes</span></span>

<span data-ttu-id="77a13-115">تعمل هذه الدالة مثل الدالة [ROUND](er-functions-mathematical-round.md)، إلا أنها تقرّب دائمًا الرقم المحدد لأعلى (بعيدًا عن الصفر).</span><span class="sxs-lookup"><span data-stu-id="77a13-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number up (away from zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="77a13-116">مثال1</span><span class="sxs-lookup"><span data-stu-id="77a13-116">Example 1</span></span>

<span data-ttu-id="77a13-117">تقرّب `ROUNDUP (1200.763, 2)` لأعلى إلى منزلتين عشريتين وترجع **1200.77**.</span><span class="sxs-lookup"><span data-stu-id="77a13-117">`ROUNDUP (1200.763, 2)` rounds up to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="77a13-118">مثال2</span><span class="sxs-lookup"><span data-stu-id="77a13-118">Example 2</span></span>

<span data-ttu-id="77a13-119">تُقربّ `ROUNDUP (1200.767, -3)` لأعلى إلى أقرب مضاعف من 1,000 وترجع **2000**.</span><span class="sxs-lookup"><span data-stu-id="77a13-119">`ROUNDUP (1200.767, -3)` rounds up to the nearest multiple of 1,000 and returns **2000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="77a13-120">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="77a13-120">Additional resources</span></span>

[<span data-ttu-id="77a13-121">الدالات الحسابية</span><span class="sxs-lookup"><span data-stu-id="77a13-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]