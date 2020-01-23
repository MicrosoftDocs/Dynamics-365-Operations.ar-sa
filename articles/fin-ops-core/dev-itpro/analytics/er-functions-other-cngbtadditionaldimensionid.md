---
title: CN_GBT_ADDITIONALDIMENSIONID ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية CN_GBT_ADDITIONALDIMENSIONID (ER).
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
ms.openlocfilehash: df693d745d1fe74b4500dd3fda0cc0c4be21142d
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917018"
---
# <span data-ttu-id="479ed-103"><a name="CN_GBT_ADDITIONALDIMENSIONID">CN_GBT_ADDITIONALDIMENSIONID ER وظيفة</a></span><span class="sxs-lookup"><span data-stu-id="479ed-103"><a name="CN_GBT_ADDITIONALDIMENSIONID">CN_GBT_ADDITIONALDIMENSIONID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="479ed-104">تقوم الوظيفة `CN_GBT_ADDITIONALDIMENSIONID` بإرجاع قيمة *سلسلة* تمثل مُعرف بعد مالي واحد مأخوذ من السلسلة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="479ed-104">The `CN_GBT_ADDITIONALDIMENSIONID` function returns a *String* value that represents a single financial dimension ID that is taken from the specified string.</span></span> <span data-ttu-id="479ed-105">تعرض السلسلة المُحددة كافة الأبعاد كقائمة مُعرفات مفصولة بفاصلة.</span><span class="sxs-lookup"><span data-stu-id="479ed-105">The specified string presents all dimensions as a comma-separated list of IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="479ed-106">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="479ed-106">Syntax</span></span>

```
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a><span data-ttu-id="479ed-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="479ed-107">Arguments</span></span>

<span data-ttu-id="479ed-108">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="479ed-108">`text`: *String*</span></span>

<span data-ttu-id="479ed-109">قيمة *سلسلة*تمثل كافة الأبعاد كقائمة مُعرفات مفصولة بفاصلة.</span><span class="sxs-lookup"><span data-stu-id="479ed-109">A *String* value that presents all dimensions as a comma-separated list of IDs.</span></span>

<span data-ttu-id="479ed-110">`number`: عدد صحيح</span><span class="sxs-lookup"><span data-stu-id="479ed-110">`number`: Integer</span></span>

<span data-ttu-id="479ed-111">قيمة *عدد صحيح* تُحدد كود التسلسل للبعد المُطلوب في السلسلة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="479ed-111">An *Integer* value that defines the sequence code of the requested dimension in the specified string.</span></span>

## <a name="return-values"></a><span data-ttu-id="479ed-112">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="479ed-112">Return values</span></span>

<span data-ttu-id="479ed-113">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="479ed-113">*String*</span></span>

<span data-ttu-id="479ed-114">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="479ed-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="479ed-115">مثال</span><span class="sxs-lookup"><span data-stu-id="479ed-115">Example</span></span>

<span data-ttu-id="479ed-116">تُرجع `CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` **"CC"**.</span><span class="sxs-lookup"><span data-stu-id="479ed-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returns **"CC"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="479ed-117">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="479ed-117">Additional resources</span></span>

[<span data-ttu-id="479ed-118">دالات أخرى (خاصة بمجال الأعمال)</span><span class="sxs-lookup"><span data-stu-id="479ed-118">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
