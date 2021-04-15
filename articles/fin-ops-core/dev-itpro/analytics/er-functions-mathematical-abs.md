---
title: ABS ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية ABS (ER).
author: NickSelin
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
ms.openlocfilehash: 2a3613483d53fb265741b5d6a34a91da443dcef7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753134"
---
# <a name="abs-er-function"></a><span data-ttu-id="70ace-103">ABS ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="70ace-103">ABS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="70ace-104">تُرجع الوظيفة `ABS` القيمة المُطلقة (للمعاملات) للرقم المُحدد كقيمة *حقيقة*.</span><span class="sxs-lookup"><span data-stu-id="70ace-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="70ace-105">وبمعني آخر، يقوم بإرجاع الرقم دون إشارته.</span><span class="sxs-lookup"><span data-stu-id="70ace-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="70ace-106">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="70ace-106">Syntax</span></span>

```vb
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="70ace-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="70ace-107">Arguments</span></span>

<span data-ttu-id="70ace-108">`number`: *حقيقي*</span><span class="sxs-lookup"><span data-stu-id="70ace-108">`number`: *Real*</span></span>

<span data-ttu-id="70ace-109">القيمة الرقمية التي تُريدها من المعاملات.</span><span class="sxs-lookup"><span data-stu-id="70ace-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="70ace-110">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="70ace-110">Return values</span></span>

<span data-ttu-id="70ace-111">*حقيقي*</span><span class="sxs-lookup"><span data-stu-id="70ace-111">*Real*</span></span>

<span data-ttu-id="70ace-112">القيمة العددية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="70ace-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="70ace-113">مثال</span><span class="sxs-lookup"><span data-stu-id="70ace-113">Example</span></span>

<span data-ttu-id="70ace-114">يُرجع التعبير `ABS (-1)` **1**.</span><span class="sxs-lookup"><span data-stu-id="70ace-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="70ace-115">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="70ace-115">Additional resources</span></span>

[<span data-ttu-id="70ace-116">الدالات الحسابية</span><span class="sxs-lookup"><span data-stu-id="70ace-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]