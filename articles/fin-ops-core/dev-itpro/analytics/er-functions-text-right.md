---
title: RIGHT ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني RIGHT (ER).
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: f59b12f0b3f7b100b953b2072677c83c836746ff
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746113"
---
# <a name="right-er-function"></a><span data-ttu-id="2e230-103">RIGHT ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="2e230-103">RIGHT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2e230-104">تقوم الوظيفة `RIGHT` بإرجاع قيمة *سلسلة* توضح العدد المُحدد من الأحرف من نهاية السلسلة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="2e230-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e230-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="2e230-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="2e230-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="2e230-106">Arguments</span></span>

<span data-ttu-id="2e230-107">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="2e230-107">`text`: *String*</span></span>

<span data-ttu-id="2e230-108">قيمة *سلسلة* التي تمثل النص الأصلي.</span><span class="sxs-lookup"><span data-stu-id="2e230-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="2e230-109">`number`: *عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="2e230-109">`number`: *Integer*</span></span>

<span data-ttu-id="2e230-110">عدد الأحرف التي يجب إرجاعها من نهاية النص الأصلي.</span><span class="sxs-lookup"><span data-stu-id="2e230-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="2e230-111">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="2e230-111">Return values</span></span>

<span data-ttu-id="2e230-112">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="2e230-112">*String*</span></span>

<span data-ttu-id="2e230-113">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="2e230-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="2e230-114">مثال</span><span class="sxs-lookup"><span data-stu-id="2e230-114">Example</span></span>

<span data-ttu-id="2e230-115">تُرجع وظيفة `RIGHT ("Sample", 3)` **"ple"**.</span><span class="sxs-lookup"><span data-stu-id="2e230-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2e230-116">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="2e230-116">Additional resources</span></span>

[<span data-ttu-id="2e230-117">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="2e230-117">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]