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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e3d3ff87a59632d58a7c34ef96f856b38f005651
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915753"
---
# <span data-ttu-id="9d6fd-103"><a name="CONCATENATE">وظيفة CONCATENATE ER </a></span><span class="sxs-lookup"><span data-stu-id="9d6fd-103"><a name="CONCATENATE">CONCATENATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9d6fd-104">تُرجع الوظيفة `CONCATENATE` جميع السلاسل النصية المُحددة كقيمة *سلسلة* بعد انضمامها في سلسلة واحدة.</span><span class="sxs-lookup"><span data-stu-id="9d6fd-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d6fd-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="9d6fd-105">Syntax</span></span>

```
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="9d6fd-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="9d6fd-106">Arguments</span></span>

<span data-ttu-id="9d6fd-107">`text 1`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="9d6fd-107">`text 1`: *String*</span></span>

<span data-ttu-id="9d6fd-108">مرجع إلى مصدر البيانات من نوع بيانات *السلسلة*.</span><span class="sxs-lookup"><span data-stu-id="9d6fd-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="9d6fd-109">هذه الوسيطة مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="9d6fd-109">This argument is required.</span></span>

<span data-ttu-id="9d6fd-110">`text N`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="9d6fd-110">`text N`: *String*</span></span>

<span data-ttu-id="9d6fd-111">مرجع إلى مصدر البيانات من نوع بيانات *السلسلة*.</span><span class="sxs-lookup"><span data-stu-id="9d6fd-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="9d6fd-112">هذه الوسائط الإضافية اختيارية.</span><span class="sxs-lookup"><span data-stu-id="9d6fd-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="9d6fd-113">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="9d6fd-113">Return values</span></span>

<span data-ttu-id="9d6fd-114">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="9d6fd-114">*String*</span></span>

<span data-ttu-id="9d6fd-115">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="9d6fd-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="9d6fd-116">مثال</span><span class="sxs-lookup"><span data-stu-id="9d6fd-116">Example</span></span>

<span data-ttu-id="9d6fd-117">يُرجع التعبير `CONCATENATE ("abc", "def")` **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="9d6fd-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="9d6fd-118">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="9d6fd-118">Usage notes</span></span>

<span data-ttu-id="9d6fd-119">كما يُرجع التعبير `"abc" & "def"` **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="9d6fd-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9d6fd-120">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="9d6fd-120">Additional resources</span></span>

[<span data-ttu-id="9d6fd-121">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="9d6fd-121">Text functions</span></span>](er-functions-category-text.md)
