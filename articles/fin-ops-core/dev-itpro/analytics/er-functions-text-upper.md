---
title: UPPER ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية Upper (ER).
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: ed862ab823cfc3539c420d3066c9397e1e6d870e
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916673"
---
# <span data-ttu-id="65b24-103"><a name="UPPER">UPPER ER وظيفة</a></span><span class="sxs-lookup"><span data-stu-id="65b24-103"><a name="UPPER">UPPER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="65b24-104">تقوم وظيفة `UPPER` بإرجاع سلسلة النص المُحددة كقيمة *سلسلة* بعد أن تم تحويلها إلى أحرف كبيرة.</span><span class="sxs-lookup"><span data-stu-id="65b24-104">The `UPPER` function returns the specified text string as a *String* value after it has been converted to uppercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="65b24-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="65b24-105">Syntax</span></span>

```
UPPER (text )
```

## <a name="arguments"></a><span data-ttu-id="65b24-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="65b24-106">Arguments</span></span>

<span data-ttu-id="65b24-107">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="65b24-107">`text`: *String*</span></span>

<span data-ttu-id="65b24-108">المسار الصالح لمصدر البيانات من نوع *السلسلة*.</span><span class="sxs-lookup"><span data-stu-id="65b24-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="65b24-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="65b24-109">Return values</span></span>

<span data-ttu-id="65b24-110">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="65b24-110">*String*</span></span>

<span data-ttu-id="65b24-111">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="65b24-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="65b24-112">مثال</span><span class="sxs-lookup"><span data-stu-id="65b24-112">Example</span></span>

<span data-ttu-id="65b24-113">تُرجع `UPPER ("Sample")` **"SAMPLE"**.</span><span class="sxs-lookup"><span data-stu-id="65b24-113">`UPPER ("Sample")` returns **"SAMPLE"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="65b24-114">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="65b24-114">Additional resources</span></span>

[<span data-ttu-id="65b24-115">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="65b24-115">Text functions</span></span>](er-functions-category-text.md)
