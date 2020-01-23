---
title: CURCREDREF ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني CURCREDREF (ER).
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
ms.openlocfilehash: 5633541b1c7e25a0cfb837c4679691506806421b
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916995"
---
# <span data-ttu-id="ab60a-103"><a name="CURCREDREF">CURCREDREF ER وظيفة</a></span><span class="sxs-lookup"><span data-stu-id="ab60a-103"><a name="CURCREDREF">CURCREDREF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ab60a-104">تُرجع الوظيفة `CURCREDREF` قيمة *سلسلة* تُمثل مرجع دائن، بناءً على أرقام رقم الفاتورة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="ab60a-104">The `CURCREDREF` function returns a *String* value that represents a creditor reference, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab60a-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="ab60a-105">Syntax</span></span>

```
CURCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="ab60a-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="ab60a-106">Arguments</span></span>

<span data-ttu-id="ab60a-107">`invoice number digits`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="ab60a-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="ab60a-108">قيمة نصية تمثل الأرقام الخاصة برقم الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="ab60a-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="ab60a-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="ab60a-109">Return values</span></span>

<span data-ttu-id="ab60a-110">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="ab60a-110">*String*</span></span>

<span data-ttu-id="ab60a-111">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="ab60a-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="ab60a-112">مثال</span><span class="sxs-lookup"><span data-stu-id="ab60a-112">Example</span></span>

<span data-ttu-id="ab60a-113">يُرجع التعبير `CURCredRef ("VEND-200002")` **"2200002"**.</span><span class="sxs-lookup"><span data-stu-id="ab60a-113">`CURCredRef ("VEND-200002")` returns **"2200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ab60a-114">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="ab60a-114">Additional resources</span></span>

[<span data-ttu-id="ab60a-115">دالات أخرى (خاصة بمجال الأعمال)</span><span class="sxs-lookup"><span data-stu-id="ab60a-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
