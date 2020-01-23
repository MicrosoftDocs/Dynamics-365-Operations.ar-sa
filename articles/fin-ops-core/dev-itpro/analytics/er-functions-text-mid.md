---
title: MID ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني MID (ER).
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
ms.openlocfilehash: e178b01740954b46e2afbd2a2be6200a652a18c0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915592"
---
# <span data-ttu-id="660d1-103"><a name="MID">MID ER وظيفة</a></span><span class="sxs-lookup"><span data-stu-id="660d1-103"><a name="MID">MID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="660d1-104">تُرجع وظيفة `MID` قيمة *السلسلة* التي توضح العدد المُحدد من الأحرف من السلسلة المُحددة، بداية من الموضع المُحدد.</span><span class="sxs-lookup"><span data-stu-id="660d1-104">The `MID` function returns a *String* value that presents the specified number of characters from the specified string, starting at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="660d1-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="660d1-105">Syntax</span></span>

```
MID (text, starting position, number of characters)
```

## <a name="arguments"></a><span data-ttu-id="660d1-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="660d1-106">Arguments</span></span>

<span data-ttu-id="660d1-107">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="660d1-107">`text`: *String*</span></span>

<span data-ttu-id="660d1-108">قيمه *السلسلة* التي تحدد النص الذي سيتم إرجاع الأحرف منه.</span><span class="sxs-lookup"><span data-stu-id="660d1-108">A *String* value that specifies the text to return characters from.</span></span>

<span data-ttu-id="660d1-109">`starting position`: *عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="660d1-109">`starting position`: *Integer*</span></span>

<span data-ttu-id="660d1-110">قيمه *عدد صحيح* التي تحدد موضع الحرف الأول الذي يجب إرجاعه من النص المحدد.</span><span class="sxs-lookup"><span data-stu-id="660d1-110">An *Integer* value that specifies the position of the first character that must be returned from the specified text.</span></span>

<span data-ttu-id="660d1-111">`number of characters`: *عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="660d1-111">`number of characters`: *Integer*</span></span>

<span data-ttu-id="660d1-112">قيمه *عدد صحيح* التي تحدد عدد الأحرف التي يجب إرجاعها، بدءًا من موضع البداية المحدد.</span><span class="sxs-lookup"><span data-stu-id="660d1-112">An *Integer* value that specifies the number of characters that must be returned, starting at the specified starting position.</span></span>

## <a name="return-values"></a><span data-ttu-id="660d1-113">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="660d1-113">Return values</span></span>

<span data-ttu-id="660d1-114">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="660d1-114">*String*</span></span>

<span data-ttu-id="660d1-115">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="660d1-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="660d1-116">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="660d1-116">Usage notes</span></span>

<span data-ttu-id="660d1-117">إذا كانت قيمة الوسيطة `starting position` أقل من 0 (صفر)، يتم حساب الأحرف التي يتم إرجاعها من الموضع الأول في السلسلة المحددة.</span><span class="sxs-lookup"><span data-stu-id="660d1-117">If the value of the `starting position` argument is less than 0 (zero), the characters that are returned are counted from the first position in the specified string.</span></span>

<span data-ttu-id="660d1-118">إذا تجاوزت قيمة `starting position` الوسيطة طول السلسلة المحددة، يتم إرجاع سلسله فارغه.</span><span class="sxs-lookup"><span data-stu-id="660d1-118">If the value of the `starting position` argument exceeds length of the specified string, an empty string is returned.</span></span>

## <a name="example"></a><span data-ttu-id="660d1-119">مثال</span><span class="sxs-lookup"><span data-stu-id="660d1-119">Example</span></span>

<span data-ttu-id="660d1-120">تُرجع`MID ("Sample", 2, 3)` القيمة **"amp"**.</span><span class="sxs-lookup"><span data-stu-id="660d1-120">`MID ("Sample", 2, 3)` returns **"amp"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="660d1-121">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="660d1-121">Additional resources</span></span>

[<span data-ttu-id="660d1-122">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="660d1-122">Text functions</span></span>](er-functions-category-text.md)
