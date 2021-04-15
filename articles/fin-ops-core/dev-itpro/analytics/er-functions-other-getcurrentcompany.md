---
title: GETCURRENTCOMPANY ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني GETCURRENTCOMPANY (ER).
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 87bef4aa11c01b42af19f7dc20ca8731b9fb4111
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752810"
---
# <a name="getcurrentcompany-er-function"></a><span data-ttu-id="2ec66-103">GETCURRENTCOMPANY ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="2ec66-103">GETCURRENTCOMPANY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ec66-104">تُرجع وظيفة `GETCURRENTCOMPANY` قيمة *السلسلة* التي تمثل كود الكيان القانوني (الشركة) الذي يقوم مستخدم بتسجيل الدخول فيه حاليًا.</span><span class="sxs-lookup"><span data-stu-id="2ec66-104">The `GETCURRENTCOMPANY` function returns a *String* value that represents the code for the legal entity (company) that a user is currently signed in to.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ec66-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="2ec66-105">Syntax</span></span>

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a><span data-ttu-id="2ec66-106">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="2ec66-106">Return values</span></span>

<span data-ttu-id="2ec66-107">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="2ec66-107">*String*</span></span>

<span data-ttu-id="2ec66-108">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="2ec66-108">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="2ec66-109">مثال</span><span class="sxs-lookup"><span data-stu-id="2ec66-109">Example</span></span>

<span data-ttu-id="2ec66-110">يُرجع التعبير `GETCURRENTCOMPANY ()` **USMF** لمستخدم سجل دخوله إلى شركة **Contoso Entertainment System USA**.</span><span class="sxs-lookup"><span data-stu-id="2ec66-110">`GETCURRENTCOMPANY ()` returns **USMF** for a user who is signed in to the **Contoso Entertainment System USA** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2ec66-111">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="2ec66-111">Additional resources</span></span>

[<span data-ttu-id="2ec66-112">دالات أخرى (خاصة بمجال الأعمال)</span><span class="sxs-lookup"><span data-stu-id="2ec66-112">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]