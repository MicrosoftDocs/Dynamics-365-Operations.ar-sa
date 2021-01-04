---
title: وظيفة ADDDAYS ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية ADDDAYS (ER).
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: e3d90c19ddc64286843347976c000267e416bf05
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688433"
---
# <a name="adddays-er-function"></a><span data-ttu-id="f93fe-103">وظيفة ADDDAYS ER</span><span class="sxs-lookup"><span data-stu-id="f93fe-103">ADDDAYS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f93fe-104">تحسب وظيفة `ADDDAYS` قيمة *DateTime* والتي هي عدد الأيام المُحددة قبل أو بعد تاريخ البدء المُحدد.</span><span class="sxs-lookup"><span data-stu-id="f93fe-104">The `ADDDAYS` function calculates a *DateTime* value that is the specified number of days before or after a specified start date.</span></span>

## <a name="syntax"></a><span data-ttu-id="f93fe-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="f93fe-105">Syntax</span></span>

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a><span data-ttu-id="f93fe-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="f93fe-106">Arguments</span></span>

<span data-ttu-id="f93fe-107">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="f93fe-107">`datetime`: *DateTime*</span></span>

<span data-ttu-id="f93fe-108">قيمة الوقت/التاريخ التي تمثل تاريخ البدء.</span><span class="sxs-lookup"><span data-stu-id="f93fe-108">A date/time value that represents the start date.</span></span>

<span data-ttu-id="f93fe-109">`days`: *عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="f93fe-109">`days`: *Integer*</span></span>

<span data-ttu-id="f93fe-110">عدد الأيام قبل أو بعد `datetime`.</span><span class="sxs-lookup"><span data-stu-id="f93fe-110">The number of days before or after `datetime`.</span></span>

## <a name="return-values"></a><span data-ttu-id="f93fe-111">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="f93fe-111">Return values</span></span>

<span data-ttu-id="f93fe-112">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="f93fe-112">*DateTime*</span></span>

<span data-ttu-id="f93fe-113">قيمة التاريخ/الوقت الناتجة.</span><span class="sxs-lookup"><span data-stu-id="f93fe-113">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f93fe-114">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="f93fe-114">Usage notes</span></span>

<span data-ttu-id="f93fe-115">قيمة موجبة لـ `days` تُعطي تاريخ مستقبلي.</span><span class="sxs-lookup"><span data-stu-id="f93fe-115">A positive value for `days` yields a future date.</span></span> <span data-ttu-id="f93fe-116">قيمة سالبة تعطي تاريخًا سابقًا.</span><span class="sxs-lookup"><span data-stu-id="f93fe-116">A negative value yields a past date.</span></span>

## <a name="example-1"></a><span data-ttu-id="f93fe-117">مثال1</span><span class="sxs-lookup"><span data-stu-id="f93fe-117">Example 1</span></span>

<span data-ttu-id="f93fe-118">يُرجع التعبير `ADDDAYS (NOW(), 7)` التاريخ والوقت سبعة أيام في المستقبل.</span><span class="sxs-lookup"><span data-stu-id="f93fe-118">`ADDDAYS (NOW(), 7)` returns the date and time seven days in the future.</span></span>

## <a name="example-2"></a><span data-ttu-id="f93fe-119">مثال2</span><span class="sxs-lookup"><span data-stu-id="f93fe-119">Example 2</span></span>

<span data-ttu-id="f93fe-120">يُرجع التعبير `ADDDAYS (NOW(), -3)` التاريخ والوقت ثلاثة أيام في الماضي.</span><span class="sxs-lookup"><span data-stu-id="f93fe-120">`ADDDAYS (NOW(), -3)` returns the date and time three days in the past.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f93fe-121">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="f93fe-121">Additional resources</span></span>

[<span data-ttu-id="f93fe-122">دلات التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="f93fe-122">Date and time functions</span></span>](er-functions-category-datetime.md)
