---
title: MID ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني MID (ER).
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
ms.openlocfilehash: 9a9ff3f1055f6757d6d4073dbb816773d8bfc8ba
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746257"
---
# <a name="mid-er-function"></a><span data-ttu-id="bef78-103">MID ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="bef78-103">MID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bef78-104">تُرجع وظيفة `MID` قيمة *السلسلة* التي توضح العدد المُحدد من الأحرف من السلسلة المُحددة، بداية من الموضع المُحدد.</span><span class="sxs-lookup"><span data-stu-id="bef78-104">The `MID` function returns a *String* value that presents the specified number of characters from the specified string, starting at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="bef78-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="bef78-105">Syntax</span></span>

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a><span data-ttu-id="bef78-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="bef78-106">Arguments</span></span>

<span data-ttu-id="bef78-107">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="bef78-107">`text`: *String*</span></span>

<span data-ttu-id="bef78-108">قيمه *السلسلة* التي تحدد النص الذي سيتم إرجاع الأحرف منه.</span><span class="sxs-lookup"><span data-stu-id="bef78-108">A *String* value that specifies the text to return characters from.</span></span>

<span data-ttu-id="bef78-109">`starting position`: *عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="bef78-109">`starting position`: *Integer*</span></span>

<span data-ttu-id="bef78-110">قيمه *عدد صحيح* التي تحدد موضع الحرف الأول الذي يجب إرجاعه من النص المحدد.</span><span class="sxs-lookup"><span data-stu-id="bef78-110">An *Integer* value that specifies the position of the first character that must be returned from the specified text.</span></span>

<span data-ttu-id="bef78-111">`number of characters`: *عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="bef78-111">`number of characters`: *Integer*</span></span>

<span data-ttu-id="bef78-112">قيمه *عدد صحيح* التي تحدد عدد الأحرف التي يجب إرجاعها، بدءًا من موضع البداية المحدد.</span><span class="sxs-lookup"><span data-stu-id="bef78-112">An *Integer* value that specifies the number of characters that must be returned, starting at the specified starting position.</span></span>

## <a name="return-values"></a><span data-ttu-id="bef78-113">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="bef78-113">Return values</span></span>

<span data-ttu-id="bef78-114">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="bef78-114">*String*</span></span>

<span data-ttu-id="bef78-115">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="bef78-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="bef78-116">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="bef78-116">Usage notes</span></span>

<span data-ttu-id="bef78-117">إذا كانت قيمة الوسيطة `starting position` أقل من 0 (صفر)، يتم حساب الأحرف التي يتم إرجاعها من الموضع الأول في السلسلة المحددة.</span><span class="sxs-lookup"><span data-stu-id="bef78-117">If the value of the `starting position` argument is less than 0 (zero), the characters that are returned are counted from the first position in the specified string.</span></span>

<span data-ttu-id="bef78-118">إذا تجاوزت قيمة `starting position` الوسيطة طول السلسلة المحددة، يتم إرجاع سلسله فارغه.</span><span class="sxs-lookup"><span data-stu-id="bef78-118">If the value of the `starting position` argument exceeds length of the specified string, an empty string is returned.</span></span>

## <a name="example"></a><span data-ttu-id="bef78-119">مثال</span><span class="sxs-lookup"><span data-stu-id="bef78-119">Example</span></span>

<span data-ttu-id="bef78-120">تُرجع`MID ("Sample", 2, 3)` القيمة **"amp"**.</span><span class="sxs-lookup"><span data-stu-id="bef78-120">`MID ("Sample", 2, 3)` returns **"amp"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bef78-121">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="bef78-121">Additional resources</span></span>

[<span data-ttu-id="bef78-122">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="bef78-122">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]