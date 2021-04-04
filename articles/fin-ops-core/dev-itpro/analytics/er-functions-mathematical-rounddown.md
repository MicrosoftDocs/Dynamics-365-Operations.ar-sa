---
title: ROUNDDOWN ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية ROUNDDOWN (ER).
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
ms.openlocfilehash: f199d662eb31f184b6f978b3d251e64907254584
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567130"
---
# <a name="rounddown-er-function"></a><span data-ttu-id="aaa75-103">ROUNDDOWN ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="aaa75-103">ROUNDDOWN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aaa75-104">تُرجع الوظيفة `ROUNDDOWN` الرقم المُحدد كقيمة *حقيقية* بعد أن تم تقريبه لأسفل إلى عدد المنازل العشرة المُحدد.</span><span class="sxs-lookup"><span data-stu-id="aaa75-104">The `ROUNDDOWN` function returns the specified number as a *Real* value after it has been rounded down to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaa75-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="aaa75-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="aaa75-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="aaa75-106">Arguments</span></span>

<span data-ttu-id="aaa75-107">`number`: *حقيقي*</span><span class="sxs-lookup"><span data-stu-id="aaa75-107">`number`: *Real*</span></span>

<span data-ttu-id="aaa75-108">قيمة رقمية يجب تقريبها لأسفل.</span><span class="sxs-lookup"><span data-stu-id="aaa75-108">A numeric value that must be rounded down.</span></span>

<span data-ttu-id="aaa75-109">`decimals`: *عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="aaa75-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="aaa75-110">قيمة رقمية تمثل عدد المنازل العشرية.</span><span class="sxs-lookup"><span data-stu-id="aaa75-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="aaa75-111">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="aaa75-111">Return values</span></span>

<span data-ttu-id="aaa75-112">*حقيقي*</span><span class="sxs-lookup"><span data-stu-id="aaa75-112">*Real*</span></span>

<span data-ttu-id="aaa75-113">القيمة العددية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="aaa75-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="aaa75-114">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="aaa75-114">Usage notes</span></span>

<span data-ttu-id="aaa75-115">تعمل هذه الدالة مثل الدالة [ROUND](er-functions-mathematical-round.md)، إلا أنها تقرّب دائمًا الرقم المحدد لأسفل (في اتجاه الصفر).</span><span class="sxs-lookup"><span data-stu-id="aaa75-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number down (toward zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="aaa75-116">مثال1</span><span class="sxs-lookup"><span data-stu-id="aaa75-116">Example 1</span></span>

<span data-ttu-id="aaa75-117">تقرّب `ROUNDDOWN (1200.767, 2)` لأسفل إلى منزلتين عشريتين وترجع **1200.76**.</span><span class="sxs-lookup"><span data-stu-id="aaa75-117">`ROUNDDOWN (1200.767, 2)` rounds down to two decimal places and returns **1200.76**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="aaa75-118">مثال2</span><span class="sxs-lookup"><span data-stu-id="aaa75-118">Example 2</span></span>

<span data-ttu-id="aaa75-119">تُقربّ `ROUNDDOWN (1700.767, -3)` لأسفل إلى أقرب مضاعف من 1,000 وترجع **1000**.</span><span class="sxs-lookup"><span data-stu-id="aaa75-119">`ROUNDDOWN (1700.767, -3)` rounds down to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aaa75-120">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="aaa75-120">Additional resources</span></span>

[<span data-ttu-id="aaa75-121">الدالات الحسابية</span><span class="sxs-lookup"><span data-stu-id="aaa75-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]