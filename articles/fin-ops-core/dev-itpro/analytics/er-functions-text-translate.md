---
title: وظيفة TRANSLATE ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني TRANSLATE (ER).
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 11954f3e48d8dc2257b3a0bc8768df47af3c5c0c
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916696"
---
# <span data-ttu-id="2dcbc-103"><a name="TRANSLATE">وظيفة TRANSLATE ER</a></span><span class="sxs-lookup"><span data-stu-id="2dcbc-103"><a name="TRANSLATE">TRANSLATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2dcbc-104">تقوم وظيفة `TRANSLATE` بإرجاع السلسلة النصية المُحددة كقيمة *سلسلة* بعد استبدالها كليًا أو جزئيًا بسلسلة أخرى.</span><span class="sxs-lookup"><span data-stu-id="2dcbc-104">The `TRANSLATE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dcbc-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="2dcbc-105">Syntax</span></span>

```
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="2dcbc-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="2dcbc-106">Arguments</span></span>

<span data-ttu-id="2dcbc-107">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="2dcbc-107">`text`: *String*</span></span>

<span data-ttu-id="2dcbc-108">المسار الصالح لمصدر البيانات من نوع *السلسلة*.</span><span class="sxs-lookup"><span data-stu-id="2dcbc-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="2dcbc-109">`pattern`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="2dcbc-109">`pattern`: *String*</span></span>

<span data-ttu-id="2dcbc-110">النص الذي يجب استبداله.</span><span class="sxs-lookup"><span data-stu-id="2dcbc-110">The text that must be replaced.</span></span>

<span data-ttu-id="2dcbc-111">`replacement`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="2dcbc-111">`replacement`: *String*</span></span>

<span data-ttu-id="2dcbc-112">النص الذي سيتم استخدامه كبديل.</span><span class="sxs-lookup"><span data-stu-id="2dcbc-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="2dcbc-113">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="2dcbc-113">Return values</span></span>

<span data-ttu-id="2dcbc-114">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="2dcbc-114">*String*</span></span>

<span data-ttu-id="2dcbc-115">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="2dcbc-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="2dcbc-116">مثال</span><span class="sxs-lookup"><span data-stu-id="2dcbc-116">Example</span></span>

<span data-ttu-id="2dcbc-117">يستبدل `TRANSLATE ("abcdef", "cd", "GH")` النمط **"cd"** بالسلسلة **"GH"** وترجع **"abGHef"**.</span><span class="sxs-lookup"><span data-stu-id="2dcbc-117">`TRANSLATE ("abcdef", "cd", "GH")` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2dcbc-118">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="2dcbc-118">Additional resources</span></span>

[<span data-ttu-id="2dcbc-119">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="2dcbc-119">Text functions</span></span>](er-functions-category-text.md)
