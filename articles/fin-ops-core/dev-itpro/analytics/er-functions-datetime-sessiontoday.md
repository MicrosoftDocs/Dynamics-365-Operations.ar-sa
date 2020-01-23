---
title: SESSIONTODAY ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني SESSIONTODAY (ER).
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
ms.openlocfilehash: bcfb36d6e3fb8475546f7cfb420c4aca848ac896
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917455"
---
# <span data-ttu-id="b3bb7-103"><a name="SESSIONTODAY">SESSIONTODAY ER وظيفة</a></span><span class="sxs-lookup"><span data-stu-id="b3bb7-103"><a name="SESSIONTODAY">SESSIONTODAY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b3bb7-104">تُرجع وظيفة `SESSIONTODAY` قيمة *التاريخ* التي تمثل تاريخ جلسة التطبيق الحالي.</span><span class="sxs-lookup"><span data-stu-id="b3bb7-104">The `SESSIONTODAY` function returns a *Date* value that represents the current application session date.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3bb7-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="b3bb7-105">Syntax</span></span>

```
SESSIONTODAY ()
```

## <a name="return-values"></a><span data-ttu-id="b3bb7-106">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="b3bb7-106">Return values</span></span>

<span data-ttu-id="b3bb7-107">*التاريخ*</span><span class="sxs-lookup"><span data-stu-id="b3bb7-107">*Date*</span></span>

<span data-ttu-id="b3bb7-108">قيمة التاريخ الناتجة.</span><span class="sxs-lookup"><span data-stu-id="b3bb7-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="b3bb7-109">مثال</span><span class="sxs-lookup"><span data-stu-id="b3bb7-109">Example</span></span>

<span data-ttu-id="b3bb7-110">تُرجع وظيفة `DATEFORMAT (SESSIONTODAY (), "d", "DE")` قيمة تاريخ جلسة التطبيق الحالية، 24 ديسمبر 2015، كسلسلة **"24-12-2015"**، بناءً على الثقافة الألمانية المُحددة والتنسيق المُحدد. </span><span class="sxs-lookup"><span data-stu-id="b3bb7-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b3bb7-111">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="b3bb7-111">Additional resources</span></span>

[<span data-ttu-id="b3bb7-112">دلات التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="b3bb7-112">Date and time functions</span></span>](er-functions-category-datetime.md)
