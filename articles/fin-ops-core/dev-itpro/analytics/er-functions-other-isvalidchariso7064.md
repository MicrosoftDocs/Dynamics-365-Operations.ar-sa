---
title: ISVALIDCHARACTERISO7064 ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية ISVALIDCHARACTERISO7064 (ER).
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
ms.openlocfilehash: 6f6f3326c9ca5cdcb3cef52f243d6d3da34251ce
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915914"
---
# <span data-ttu-id="0bf41-103"><a name="ISVALIDCHARACTERISO7064">ISVALIDCHARACTERISO7064 ER وظيفة</a></span><span class="sxs-lookup"><span data-stu-id="0bf41-103"><a name="ISVALIDCHARACTERISO7064">ISVALIDCHARACTERISO7064 ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0bf41-104">تُرجع الوظيفة `ISVALIDCHARACTERISO7064` قيمة *منطقية* **TRUE** إذا كانت السلسلة المُحددة تمثل رقم حساب مصرفي دولي (IBAN) صالحًا.</span><span class="sxs-lookup"><span data-stu-id="0bf41-104">The `ISVALIDCHARACTERISO7064` function returns a *Boolean* value of **TRUE** if the specified string represents a valid international bank account number (IBAN).</span></span> <span data-ttu-id="0bf41-105">وبخلاف ذلك، تُرجع قيمة *منطقية* لـ **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="0bf41-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bf41-106">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="0bf41-106">Syntax</span></span>

```
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a><span data-ttu-id="0bf41-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="0bf41-107">Arguments</span></span>

<span data-ttu-id="0bf41-108">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="0bf41-108">`text`: *String*</span></span>

<span data-ttu-id="0bf41-109">قيمة نصية تمثل رقم الـ IBAN.</span><span class="sxs-lookup"><span data-stu-id="0bf41-109">A text value that represents an IBAN.</span></span>

## <a name="return-values"></a><span data-ttu-id="0bf41-110">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="0bf41-110">Return values</span></span>

<span data-ttu-id="0bf41-111">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="0bf41-111">*String*</span></span>

<span data-ttu-id="0bf41-112">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="0bf41-112">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="0bf41-113">مثال</span><span class="sxs-lookup"><span data-stu-id="0bf41-113">Example</span></span>

<span data-ttu-id="0bf41-114">يُرجع التعبير `ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="0bf41-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returns **TRUE**.</span></span> 

<span data-ttu-id="0bf41-115">يُرجع التعبير `ISVALIDCHARACTERISO7064 ("AT61")` **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="0bf41-115">`ISVALIDCHARACTERISO7064 ("AT61")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0bf41-116">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="0bf41-116">Additional resources</span></span>

[<span data-ttu-id="0bf41-117">دالات أخرى (خاصة بمجال الأعمال)</span><span class="sxs-lookup"><span data-stu-id="0bf41-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
