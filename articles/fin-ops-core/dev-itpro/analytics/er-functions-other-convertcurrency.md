---
title: CONVERTCURRENCY ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني CONVERTCURRENCY (ER).
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
ms.openlocfilehash: bf972c6c2cc798811a9fb3bd3a355ac6ffca5a60
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915937"
---
# <span data-ttu-id="dd2ad-103"><a name="CONVERTCURRENCY">CONVERTCURRENCY ER وظيفة</a></span><span class="sxs-lookup"><span data-stu-id="dd2ad-103"><a name="CONVERTCURRENCY">CONVERTCURRENCY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dd2ad-104">تُرجع الوظيفة `CONVERTCURRENCY` قيمة *حقيقية* تمثيل نتيجة تحويل المبلغ المالي المحدد من العملة المصدر المحددة إلى العملة الهدف المحددة باستخدام إعدادات الشركة المُحددة في التاريخ المُحدد.</span><span class="sxs-lookup"><span data-stu-id="dd2ad-104">The `CONVERTCURRENCY` function returns a *Real* value that represents the result of converting the specified monetary amount from the specified source currency to the specified target currency by using the settings of the specified company on the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd2ad-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="dd2ad-105">Syntax</span></span>

```
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a><span data-ttu-id="dd2ad-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="dd2ad-106">Arguments</span></span>

<span data-ttu-id="dd2ad-107">`amount`: *عدد صحيح* أو *حقيقي*</span><span class="sxs-lookup"><span data-stu-id="dd2ad-107">`amount`: *Integer* or *Real*</span></span>

<span data-ttu-id="dd2ad-108">قيمة رقمية تمثل المبلغ النقدي الذي يجب تحويله.</span><span class="sxs-lookup"><span data-stu-id="dd2ad-108">A numeric value that represents the monetary amount that must be converted.</span></span>

<span data-ttu-id="dd2ad-109">`source currency`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="dd2ad-109">`source currency`: *String*</span></span>

<span data-ttu-id="dd2ad-110">كود عملة المصدر.</span><span class="sxs-lookup"><span data-stu-id="dd2ad-110">The code of the source currency.</span></span>

<span data-ttu-id="dd2ad-111">`target currency`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="dd2ad-111">`target currency`: *String*</span></span>

<span data-ttu-id="dd2ad-112">كود العملة الهدف.</span><span class="sxs-lookup"><span data-stu-id="dd2ad-112">The code of the target currency.</span></span>

<span data-ttu-id="dd2ad-113">`date`: *التاريخ*</span><span class="sxs-lookup"><span data-stu-id="dd2ad-113">`date`: *Date*</span></span>

<span data-ttu-id="dd2ad-114">قيمة *التاريخ* التي تمثل التاريخ المستخدم لتحديد سعر الصرف للتحويل.</span><span class="sxs-lookup"><span data-stu-id="dd2ad-114">A *Date* value that represents the date that is used to determine the exchange rate for the conversion.</span></span>

<span data-ttu-id="dd2ad-115">`company`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="dd2ad-115">`company`: *String*</span></span>

<span data-ttu-id="dd2ad-116">قيمة *السلسلة* التي تمثل كود الشركة التي توفر الإعدادات المستخدمة للتحويل.</span><span class="sxs-lookup"><span data-stu-id="dd2ad-116">A *String* value that represents the code of a company that supplies the settings that are used for the conversion.</span></span>

## <a name="return-values"></a><span data-ttu-id="dd2ad-117">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="dd2ad-117">Return values</span></span>

<span data-ttu-id="dd2ad-118">*حقيقي*</span><span class="sxs-lookup"><span data-stu-id="dd2ad-118">*Real*</span></span>

<span data-ttu-id="dd2ad-119">القيمة العددية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="dd2ad-119">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="dd2ad-120">مثال</span><span class="sxs-lookup"><span data-stu-id="dd2ad-120">Example</span></span>

<span data-ttu-id="dd2ad-121">تُرجع `CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` مكافئ اليورو الواحد بالدولار الأمريكي بتاريخ الجلسة الحالية، استنادًا إلى إعدادات شركة **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="dd2ad-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` returns the equivalent of one euro in US dollars on the current session date, based on settings for the **DEMF** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dd2ad-122">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="dd2ad-122">Additional resources</span></span>

[<span data-ttu-id="dd2ad-123">دالات أخرى (خاصة بمجال الأعمال)</span><span class="sxs-lookup"><span data-stu-id="dd2ad-123">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
