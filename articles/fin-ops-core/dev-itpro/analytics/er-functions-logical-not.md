---
title: NOT ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني NOT (ER).
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
ms.openlocfilehash: 9b55b3d8930ece7e2f2925579821ca88749801f7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565870"
---
# <a name="not-er-function"></a><span data-ttu-id="7bb3a-103">NOT ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="7bb3a-103">NOT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7bb3a-104">ترجع الوظيفة `NOT` القيمة المنطقية المعكوسة للشرط المُحدد كقيمة *منطقية*.</span><span class="sxs-lookup"><span data-stu-id="7bb3a-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bb3a-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="7bb3a-105">Syntax</span></span>

```vb
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="7bb3a-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="7bb3a-106">Arguments</span></span>

<span data-ttu-id="7bb3a-107">`condition`: *منطقي*</span><span class="sxs-lookup"><span data-stu-id="7bb3a-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="7bb3a-108">تعبير شرطي صالح يجب عكسه.</span><span class="sxs-lookup"><span data-stu-id="7bb3a-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="7bb3a-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="7bb3a-109">Return values</span></span>

<span data-ttu-id="7bb3a-110">*منطقي*</span><span class="sxs-lookup"><span data-stu-id="7bb3a-110">*Boolean*</span></span>

<span data-ttu-id="7bb3a-111">القيمة *المنطقية* الناتجة.</span><span class="sxs-lookup"><span data-stu-id="7bb3a-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="7bb3a-112">مثال</span><span class="sxs-lookup"><span data-stu-id="7bb3a-112">Example</span></span>

<span data-ttu-id="7bb3a-113">يُرجع التعبير `NOT (TRUE)` **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="7bb3a-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7bb3a-114">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="7bb3a-114">Additional resources</span></span>

[<span data-ttu-id="7bb3a-115">الوظائف المنطقية</span><span class="sxs-lookup"><span data-stu-id="7bb3a-115">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]