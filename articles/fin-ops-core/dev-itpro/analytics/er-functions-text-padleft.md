---
title: وظيفة PADLEFT ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية PADLEFT (ER).
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
ms.openlocfilehash: 28306b2e5fb1febce49ab55240c6d84ff240282a
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916765"
---
# <span data-ttu-id="b0653-103"><a name="PADLEFT">وظيفة PADLEFT ER</a></span><span class="sxs-lookup"><span data-stu-id="b0653-103"><a name="PADLEFT">PADLEFT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b0653-104">تُرجع وظيفة `PADLEFT` قيمة *سلسلة* بطول مُحدد، تمت فيه تعبئة بداية السلسلة المُحددة بالأحرف المُحددة.</span><span class="sxs-lookup"><span data-stu-id="b0653-104">The `PADLEFT` function returns a *String* value of the specified length, where the start of the specified string is padded with the specified characters.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0653-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="b0653-105">Syntax</span></span>

```
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a><span data-ttu-id="b0653-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="b0653-106">Arguments</span></span>

<span data-ttu-id="b0653-107">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="b0653-107">`text`: *String*</span></span>

<span data-ttu-id="b0653-108">قيمة *سلسلة* التي تمثل النص الأصلي.</span><span class="sxs-lookup"><span data-stu-id="b0653-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="b0653-109">`length`: *عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="b0653-109">`length`: *Integer*</span></span>

<span data-ttu-id="b0653-110">قيمة *عدد صحيح* تمثل الرقم النهائي للأحرف في السلسلة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="b0653-110">An *Integer* value that represents the final number of characters in the padded string.</span></span>

<span data-ttu-id="b0653-111">`padding chars`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="b0653-111">`padding chars`: *String*</span></span>

<span data-ttu-id="b0653-112">الأحرف التي سوف يتم استخدامها للتحديد.</span><span class="sxs-lookup"><span data-stu-id="b0653-112">The characters to use for padding.</span></span>

## <a name="return-values"></a><span data-ttu-id="b0653-113">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="b0653-113">Return values</span></span>

<span data-ttu-id="b0653-114">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="b0653-114">*String*</span></span>

<span data-ttu-id="b0653-115">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="b0653-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="b0653-116">مثال</span><span class="sxs-lookup"><span data-stu-id="b0653-116">Example</span></span>

<span data-ttu-id="b0653-117">تُرجع `PADLEFT ("1234", 10, "`&nbsp;`")` السلسلة النصية **&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234**</span><span class="sxs-lookup"><span data-stu-id="b0653-117">`PADLEFT ("1234", 10, "`&nbsp;`")` returns the text string **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b0653-118">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="b0653-118">Additional resources</span></span>

[<span data-ttu-id="b0653-119">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="b0653-119">Text functions</span></span>](er-functions-category-text.md)
