---
title: CN_GBT_ADDITIONALDIMENSIONID ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية CN_GBT_ADDITIONALDIMENSIONID (ER).
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 5774bb6928ae321af923819d6b2cc609dbf35b99
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564132"
---
# <a name="cn_gbt_additionaldimensionid-er-function"></a><span data-ttu-id="f71cb-103">CN_GBT_ADDITIONALDIMENSIONID ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="f71cb-103">CN_GBT_ADDITIONALDIMENSIONID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f71cb-104">تقوم الوظيفة `CN_GBT_ADDITIONALDIMENSIONID` بإرجاع قيمة *سلسلة* تمثل مُعرف بعد مالي واحد مأخوذ من السلسلة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="f71cb-104">The `CN_GBT_ADDITIONALDIMENSIONID` function returns a *String* value that represents a single financial dimension ID that is taken from the specified string.</span></span> <span data-ttu-id="f71cb-105">تعرض السلسلة المُحددة كافة الأبعاد كقائمة مُعرفات مفصولة بفاصلة.</span><span class="sxs-lookup"><span data-stu-id="f71cb-105">The specified string presents all dimensions as a comma-separated list of IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="f71cb-106">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="f71cb-106">Syntax</span></span>

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a><span data-ttu-id="f71cb-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="f71cb-107">Arguments</span></span>

<span data-ttu-id="f71cb-108">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="f71cb-108">`text`: *String*</span></span>

<span data-ttu-id="f71cb-109">قيمة *سلسلة* تمثل كافة الأبعاد كقائمة مُعرفات مفصولة بفاصلة.</span><span class="sxs-lookup"><span data-stu-id="f71cb-109">A *String* value that presents all dimensions as a comma-separated list of IDs.</span></span>

<span data-ttu-id="f71cb-110">`number`: عدد صحيح</span><span class="sxs-lookup"><span data-stu-id="f71cb-110">`number`: Integer</span></span>

<span data-ttu-id="f71cb-111">قيمة *عدد صحيح* تُحدد كود التسلسل للبعد المُطلوب في السلسلة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="f71cb-111">An *Integer* value that defines the sequence code of the requested dimension in the specified string.</span></span>

## <a name="return-values"></a><span data-ttu-id="f71cb-112">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="f71cb-112">Return values</span></span>

<span data-ttu-id="f71cb-113">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="f71cb-113">*String*</span></span>

<span data-ttu-id="f71cb-114">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="f71cb-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="f71cb-115">مثال</span><span class="sxs-lookup"><span data-stu-id="f71cb-115">Example</span></span>

<span data-ttu-id="f71cb-116">تُرجع `CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` **"CC"**.</span><span class="sxs-lookup"><span data-stu-id="f71cb-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returns **"CC"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f71cb-117">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="f71cb-117">Additional resources</span></span>

[<span data-ttu-id="f71cb-118">دالات أخرى (خاصة بمجال الأعمال)</span><span class="sxs-lookup"><span data-stu-id="f71cb-118">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]