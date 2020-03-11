---
title: GETCURRENTCOMPANY ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني GETCURRENTCOMPANY (ER).
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
ms.openlocfilehash: d91caff1a1b89e060a16833e53f3647208ed3826
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041413"
---
# <span data-ttu-id="327ff-103"><a name="GETCURRENTCOMPANY">GETCURRENTCOMPANY ER وظيفة</a></span><span class="sxs-lookup"><span data-stu-id="327ff-103"><a name="GETCURRENTCOMPANY">GETCURRENTCOMPANY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="327ff-104">تُرجع وظيفة `GETCURRENTCOMPANY` قيمة *السلسلة* التي تمثل كود الكيان القانوني (الشركة) الذي يقوم مستخدم بتسجيل الدخول فيه حاليًا.</span><span class="sxs-lookup"><span data-stu-id="327ff-104">The `GETCURRENTCOMPANY` function returns a *String* value that represents the code for the legal entity (company) that a user is currently signed in to.</span></span>

## <a name="syntax"></a><span data-ttu-id="327ff-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="327ff-105">Syntax</span></span>

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a><span data-ttu-id="327ff-106">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="327ff-106">Return values</span></span>

<span data-ttu-id="327ff-107">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="327ff-107">*String*</span></span>

<span data-ttu-id="327ff-108">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="327ff-108">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="327ff-109">مثال</span><span class="sxs-lookup"><span data-stu-id="327ff-109">Example</span></span>

<span data-ttu-id="327ff-110">يُرجع التعبير `GETCURRENTCOMPANY ()` **USMF** لمستخدم سجل دخوله إلى شركة **Contoso Entertainment System USA**.</span><span class="sxs-lookup"><span data-stu-id="327ff-110">`GETCURRENTCOMPANY ()` returns **USMF** for a user who is signed in to the **Contoso Entertainment System USA** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="327ff-111">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="327ff-111">Additional resources</span></span>

[<span data-ttu-id="327ff-112">دالات أخرى (خاصة بمجال الأعمال)</span><span class="sxs-lookup"><span data-stu-id="327ff-112">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
