---
title: NOT ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني NOT (ER).
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
ms.openlocfilehash: af588c3714069040fa339d3121e6eb404b9be979
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744637"
---
# <a name="not-er-function"></a><span data-ttu-id="5762b-103">NOT ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="5762b-103">NOT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5762b-104">ترجع الوظيفة `NOT` القيمة المنطقية المعكوسة للشرط المُحدد كقيمة *منطقية*.</span><span class="sxs-lookup"><span data-stu-id="5762b-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="5762b-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="5762b-105">Syntax</span></span>

```vb
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="5762b-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="5762b-106">Arguments</span></span>

<span data-ttu-id="5762b-107">`condition`: *منطقي*</span><span class="sxs-lookup"><span data-stu-id="5762b-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="5762b-108">تعبير شرطي صالح يجب عكسه.</span><span class="sxs-lookup"><span data-stu-id="5762b-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="5762b-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="5762b-109">Return values</span></span>

<span data-ttu-id="5762b-110">*منطقي*</span><span class="sxs-lookup"><span data-stu-id="5762b-110">*Boolean*</span></span>

<span data-ttu-id="5762b-111">القيمة *المنطقية* الناتجة.</span><span class="sxs-lookup"><span data-stu-id="5762b-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="5762b-112">مثال</span><span class="sxs-lookup"><span data-stu-id="5762b-112">Example</span></span>

<span data-ttu-id="5762b-113">يُرجع التعبير `NOT (TRUE)` **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="5762b-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5762b-114">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="5762b-114">Additional resources</span></span>

[<span data-ttu-id="5762b-115">الوظائف المنطقية</span><span class="sxs-lookup"><span data-stu-id="5762b-115">Logical functions</span></span>](er-functions-category-logical.md)