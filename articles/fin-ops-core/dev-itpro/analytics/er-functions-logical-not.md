---
title: NOT ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني NOT (ER).
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
ms.openlocfilehash: 7c10ed61b97dcd4d4a66a530bb3d08c539659233
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751694"
---
# <a name="not-er-function"></a><span data-ttu-id="941d1-103">NOT ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="941d1-103">NOT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="941d1-104">ترجع الوظيفة `NOT` القيمة المنطقية المعكوسة للشرط المُحدد كقيمة *منطقية*.</span><span class="sxs-lookup"><span data-stu-id="941d1-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="941d1-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="941d1-105">Syntax</span></span>

```vb
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="941d1-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="941d1-106">Arguments</span></span>

<span data-ttu-id="941d1-107">`condition`: *منطقي*</span><span class="sxs-lookup"><span data-stu-id="941d1-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="941d1-108">تعبير شرطي صالح يجب عكسه.</span><span class="sxs-lookup"><span data-stu-id="941d1-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="941d1-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="941d1-109">Return values</span></span>

<span data-ttu-id="941d1-110">*منطقي*</span><span class="sxs-lookup"><span data-stu-id="941d1-110">*Boolean*</span></span>

<span data-ttu-id="941d1-111">القيمة *المنطقية* الناتجة.</span><span class="sxs-lookup"><span data-stu-id="941d1-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="941d1-112">مثال</span><span class="sxs-lookup"><span data-stu-id="941d1-112">Example</span></span>

<span data-ttu-id="941d1-113">يُرجع التعبير `NOT (TRUE)` **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="941d1-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="941d1-114">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="941d1-114">Additional resources</span></span>

[<span data-ttu-id="941d1-115">الوظائف المنطقية</span><span class="sxs-lookup"><span data-stu-id="941d1-115">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]