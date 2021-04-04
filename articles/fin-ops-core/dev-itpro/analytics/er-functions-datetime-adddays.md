---
title: وظيفة ADDDAYS ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية ADDDAYS (ER).
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 85ad6508c0d16796efbf1ad81e25d74365de8f30
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570762"
---
# <a name="adddays-er-function"></a><span data-ttu-id="79359-103">وظيفة ADDDAYS ER</span><span class="sxs-lookup"><span data-stu-id="79359-103">ADDDAYS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="79359-104">تحسب وظيفة `ADDDAYS` قيمة *DateTime* والتي هي عدد الأيام المُحددة قبل أو بعد تاريخ البدء المُحدد.</span><span class="sxs-lookup"><span data-stu-id="79359-104">The `ADDDAYS` function calculates a *DateTime* value that is the specified number of days before or after a specified start date.</span></span>

## <a name="syntax"></a><span data-ttu-id="79359-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="79359-105">Syntax</span></span>

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a><span data-ttu-id="79359-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="79359-106">Arguments</span></span>

<span data-ttu-id="79359-107">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="79359-107">`datetime`: *DateTime*</span></span>

<span data-ttu-id="79359-108">قيمة الوقت/التاريخ التي تمثل تاريخ البدء.</span><span class="sxs-lookup"><span data-stu-id="79359-108">A date/time value that represents the start date.</span></span>

<span data-ttu-id="79359-109">`days`: *عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="79359-109">`days`: *Integer*</span></span>

<span data-ttu-id="79359-110">عدد الأيام قبل أو بعد `datetime`.</span><span class="sxs-lookup"><span data-stu-id="79359-110">The number of days before or after `datetime`.</span></span>

## <a name="return-values"></a><span data-ttu-id="79359-111">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="79359-111">Return values</span></span>

<span data-ttu-id="79359-112">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="79359-112">*DateTime*</span></span>

<span data-ttu-id="79359-113">قيمة التاريخ/الوقت الناتجة.</span><span class="sxs-lookup"><span data-stu-id="79359-113">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="79359-114">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="79359-114">Usage notes</span></span>

<span data-ttu-id="79359-115">قيمة موجبة لـ `days` تُعطي تاريخ مستقبلي.</span><span class="sxs-lookup"><span data-stu-id="79359-115">A positive value for `days` yields a future date.</span></span> <span data-ttu-id="79359-116">قيمة سالبة تعطي تاريخًا سابقًا.</span><span class="sxs-lookup"><span data-stu-id="79359-116">A negative value yields a past date.</span></span>

## <a name="example-1"></a><span data-ttu-id="79359-117">مثال1</span><span class="sxs-lookup"><span data-stu-id="79359-117">Example 1</span></span>

<span data-ttu-id="79359-118">يُرجع التعبير `ADDDAYS (NOW(), 7)` التاريخ والوقت سبعة أيام في المستقبل.</span><span class="sxs-lookup"><span data-stu-id="79359-118">`ADDDAYS (NOW(), 7)` returns the date and time seven days in the future.</span></span>

## <a name="example-2"></a><span data-ttu-id="79359-119">مثال2</span><span class="sxs-lookup"><span data-stu-id="79359-119">Example 2</span></span>

<span data-ttu-id="79359-120">يُرجع التعبير `ADDDAYS (NOW(), -3)` التاريخ والوقت ثلاثة أيام في الماضي.</span><span class="sxs-lookup"><span data-stu-id="79359-120">`ADDDAYS (NOW(), -3)` returns the date and time three days in the past.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="79359-121">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="79359-121">Additional resources</span></span>

[<span data-ttu-id="79359-122">دلات التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="79359-122">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]