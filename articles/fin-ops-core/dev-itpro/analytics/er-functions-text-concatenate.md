---
title: 'وظيفة CONCATENATE ER '
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني CONCATENATE (ER)
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 903429994ae5618b597aa0ab0991e9f6783a96ed
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687928"
---
# <a name="concatenate-er-function"></a><span data-ttu-id="e59de-103">وظيفة CONCATENATE ER </span><span class="sxs-lookup"><span data-stu-id="e59de-103">CONCATENATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e59de-104">تُرجع الوظيفة `CONCATENATE` جميع السلاسل النصية المُحددة كقيمة *سلسلة* بعد انضمامها في سلسلة واحدة.</span><span class="sxs-lookup"><span data-stu-id="e59de-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="e59de-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="e59de-105">Syntax</span></span>

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="e59de-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="e59de-106">Arguments</span></span>

<span data-ttu-id="e59de-107">`text 1`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="e59de-107">`text 1`: *String*</span></span>

<span data-ttu-id="e59de-108">مرجع إلى مصدر البيانات من نوع بيانات *السلسلة*.</span><span class="sxs-lookup"><span data-stu-id="e59de-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="e59de-109">هذه الوسيطة مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="e59de-109">This argument is required.</span></span>

<span data-ttu-id="e59de-110">`text N`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="e59de-110">`text N`: *String*</span></span>

<span data-ttu-id="e59de-111">مرجع إلى مصدر البيانات من نوع بيانات *السلسلة*.</span><span class="sxs-lookup"><span data-stu-id="e59de-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="e59de-112">هذه الوسائط الإضافية اختيارية.</span><span class="sxs-lookup"><span data-stu-id="e59de-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="e59de-113">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="e59de-113">Return values</span></span>

<span data-ttu-id="e59de-114">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="e59de-114">*String*</span></span>

<span data-ttu-id="e59de-115">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="e59de-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="e59de-116">مثال</span><span class="sxs-lookup"><span data-stu-id="e59de-116">Example</span></span>

<span data-ttu-id="e59de-117">يُرجع التعبير `CONCATENATE ("abc", "def")` **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="e59de-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e59de-118">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="e59de-118">Usage notes</span></span>

<span data-ttu-id="e59de-119">كما يُرجع التعبير `"abc" & "def"` **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="e59de-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e59de-120">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="e59de-120">Additional resources</span></span>

[<span data-ttu-id="e59de-121">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="e59de-121">Text functions</span></span>](er-functions-category-text.md)
