---
title: ABS ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية ABS (ER).
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
ms.openlocfilehash: 214fb2808f024487795f27de45de1d4de8cead2d
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041643"
---
# <span data-ttu-id="33a4b-103"><a name="ABS">ABS ER وظيفة</a></span><span class="sxs-lookup"><span data-stu-id="33a4b-103"><a name="ABS">ABS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="33a4b-104">تُرجع الوظيفة `ABS` القيمة المُطلقة (للمعاملات) للرقم المُحدد كقيمة *حقيقة*.</span><span class="sxs-lookup"><span data-stu-id="33a4b-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="33a4b-105">وبمعني آخر، يقوم بإرجاع الرقم دون إشارته.</span><span class="sxs-lookup"><span data-stu-id="33a4b-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="33a4b-106">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="33a4b-106">Syntax</span></span>

```vb
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="33a4b-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="33a4b-107">Arguments</span></span>

<span data-ttu-id="33a4b-108">`number`: *حقيقي*</span><span class="sxs-lookup"><span data-stu-id="33a4b-108">`number`: *Real*</span></span>

<span data-ttu-id="33a4b-109">القيمة الرقمية التي تُريدها من المعاملات.</span><span class="sxs-lookup"><span data-stu-id="33a4b-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="33a4b-110">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="33a4b-110">Return values</span></span>

<span data-ttu-id="33a4b-111">*حقيقي*</span><span class="sxs-lookup"><span data-stu-id="33a4b-111">*Real*</span></span>

<span data-ttu-id="33a4b-112">القيمة العددية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="33a4b-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="33a4b-113">مثال</span><span class="sxs-lookup"><span data-stu-id="33a4b-113">Example</span></span>

<span data-ttu-id="33a4b-114">يُرجع التعبير `ABS (-1)` **1**.</span><span class="sxs-lookup"><span data-stu-id="33a4b-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="33a4b-115">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="33a4b-115">Additional resources</span></span>

[<span data-ttu-id="33a4b-116">الدالات الحسابية</span><span class="sxs-lookup"><span data-stu-id="33a4b-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)
