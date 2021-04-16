---
title: CONVERTCURRENCY ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني CONVERTCURRENCY (ER).
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
ms.openlocfilehash: fb8f7f28f5a9bb27402544efcffa6393238e38d8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744357"
---
# <a name="convertcurrency-er-function"></a><span data-ttu-id="0aa2c-103">CONVERTCURRENCY ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="0aa2c-103">CONVERTCURRENCY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0aa2c-104">تُرجع الوظيفة `CONVERTCURRENCY` قيمة *حقيقية* تمثيل نتيجة تحويل المبلغ المالي المحدد من العملة المصدر المحددة إلى العملة الهدف المحددة باستخدام إعدادات الشركة المُحددة في التاريخ المُحدد.</span><span class="sxs-lookup"><span data-stu-id="0aa2c-104">The `CONVERTCURRENCY` function returns a *Real* value that represents the result of converting the specified monetary amount from the specified source currency to the specified target currency by using the settings of the specified company on the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="0aa2c-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="0aa2c-105">Syntax</span></span>

```vb
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a><span data-ttu-id="0aa2c-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="0aa2c-106">Arguments</span></span>

<span data-ttu-id="0aa2c-107">`amount`: *عدد صحيح* أو *حقيقي*</span><span class="sxs-lookup"><span data-stu-id="0aa2c-107">`amount`: *Integer* or *Real*</span></span>

<span data-ttu-id="0aa2c-108">قيمة رقمية تمثل المبلغ النقدي الذي يجب تحويله.</span><span class="sxs-lookup"><span data-stu-id="0aa2c-108">A numeric value that represents the monetary amount that must be converted.</span></span>

<span data-ttu-id="0aa2c-109">`source currency`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="0aa2c-109">`source currency`: *String*</span></span>

<span data-ttu-id="0aa2c-110">كود عملة المصدر.</span><span class="sxs-lookup"><span data-stu-id="0aa2c-110">The code of the source currency.</span></span>

<span data-ttu-id="0aa2c-111">`target currency`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="0aa2c-111">`target currency`: *String*</span></span>

<span data-ttu-id="0aa2c-112">كود العملة الهدف.</span><span class="sxs-lookup"><span data-stu-id="0aa2c-112">The code of the target currency.</span></span>

<span data-ttu-id="0aa2c-113">`date`: *التاريخ*</span><span class="sxs-lookup"><span data-stu-id="0aa2c-113">`date`: *Date*</span></span>

<span data-ttu-id="0aa2c-114">قيمة *التاريخ* التي تمثل التاريخ المستخدم لتحديد سعر الصرف للتحويل.</span><span class="sxs-lookup"><span data-stu-id="0aa2c-114">A *Date* value that represents the date that is used to determine the exchange rate for the conversion.</span></span>

<span data-ttu-id="0aa2c-115">`company`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="0aa2c-115">`company`: *String*</span></span>

<span data-ttu-id="0aa2c-116">قيمة *السلسلة* التي تمثل كود الشركة التي توفر الإعدادات المستخدمة للتحويل.</span><span class="sxs-lookup"><span data-stu-id="0aa2c-116">A *String* value that represents the code of a company that supplies the settings that are used for the conversion.</span></span>

## <a name="return-values"></a><span data-ttu-id="0aa2c-117">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="0aa2c-117">Return values</span></span>

<span data-ttu-id="0aa2c-118">*حقيقي*</span><span class="sxs-lookup"><span data-stu-id="0aa2c-118">*Real*</span></span>

<span data-ttu-id="0aa2c-119">القيمة العددية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="0aa2c-119">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="0aa2c-120">مثال</span><span class="sxs-lookup"><span data-stu-id="0aa2c-120">Example</span></span>

<span data-ttu-id="0aa2c-121">تُرجع `CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` مكافئ اليورو الواحد بالدولار الأمريكي بتاريخ الجلسة الحالية، استنادًا إلى إعدادات شركة **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="0aa2c-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` returns the equivalent of one euro in US dollars on the current session date, based on settings for the **DEMF** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0aa2c-122">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="0aa2c-122">Additional resources</span></span>

[<span data-ttu-id="0aa2c-123">دالات أخرى (خاصة بمجال الأعمال)</span><span class="sxs-lookup"><span data-stu-id="0aa2c-123">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]