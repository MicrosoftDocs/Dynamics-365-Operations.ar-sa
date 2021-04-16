---
title: FA_BALANCE ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية FA_BALANCE (ER).
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
ms.openlocfilehash: ec78b9c5bf800503023315eb893076486b0a1fb0
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744309"
---
# <a name="fa_balance-er-function"></a><span data-ttu-id="ebe2a-103">FA_BALANCE ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="ebe2a-103">FA_BALANCE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ebe2a-104">تُرجع الوظيفة `FA_BALANCE` قيمة *حاوية (سجل)* تتكون من بيانات لرصيد الأصل الثابت لعنصر الأصل الثابت المُحدد وكود نموذج القيمة وسنة إعداد التقرير وتاريخ إعداد التقرير.</span><span class="sxs-lookup"><span data-stu-id="ebe2a-104">The `FA_BALANCE` function returns a *Container (record)* value that consists of data for the fixed asset balance for the specified fixed asset item, value model code, reporting year, and reporting date.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebe2a-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="ebe2a-105">Syntax</span></span>

```vb
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a><span data-ttu-id="ebe2a-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="ebe2a-106">Arguments</span></span>

<span data-ttu-id="ebe2a-107">`fixed asset code`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="ebe2a-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="ebe2a-108">قيمة *السلسلة* التي تمثل كود الأصل الثابت الذي يتم حساب الرصيد له.</span><span class="sxs-lookup"><span data-stu-id="ebe2a-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="ebe2a-109">`value model code`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="ebe2a-109">`value model code`: *String*</span></span>

<span data-ttu-id="ebe2a-110">قيمة *السلسلة* التي تمثل كود نموذج القيمة الذي يتم حساب الرصيد له.</span><span class="sxs-lookup"><span data-stu-id="ebe2a-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="ebe2a-111">`reporting year`: *قيمة التعداد*</span><span class="sxs-lookup"><span data-stu-id="ebe2a-111">`reporting year`: *Enumeration value*</span></span>

<span data-ttu-id="ebe2a-112">قيمة التعداد لتعداد تطبيق **AssetYear** التي تُعرف فترة لحساب الرصيد.</span><span class="sxs-lookup"><span data-stu-id="ebe2a-112">An enumeration value of the **AssetYear** application enumeration that defines a period for the balance calculation.</span></span>

<span data-ttu-id="ebe2a-113">`reporting date`: *التاريخ*</span><span class="sxs-lookup"><span data-stu-id="ebe2a-113">`reporting date`: *Date*</span></span>

<span data-ttu-id="ebe2a-114">قيمة *التاريخ* التي تعرف تاريخ لحساب الرصيد.</span><span class="sxs-lookup"><span data-stu-id="ebe2a-114">A *Date* value that defines a date for the balance calculation.</span></span>

## <a name="return-values"></a><span data-ttu-id="ebe2a-115">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="ebe2a-115">Return values</span></span>

<span data-ttu-id="ebe2a-116">*حاوية (سجل)*</span><span class="sxs-lookup"><span data-stu-id="ebe2a-116">*Container (record)*</span></span>

<span data-ttu-id="ebe2a-117">قيمة السجل الناتجة.</span><span class="sxs-lookup"><span data-stu-id="ebe2a-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="ebe2a-118">مثال</span><span class="sxs-lookup"><span data-stu-id="ebe2a-118">Example</span></span>

<span data-ttu-id="ebe2a-119">يُرجع التعبير `FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` حاوية بيانات الأرصدة المعدة للأصل الثابت **COMP-000001** الذي لديه نموذج القيمة **الحالية** في تاريخ جلسة عمل التطبيق الحالية.</span><span class="sxs-lookup"><span data-stu-id="ebe2a-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` returns the data container of balances for fixed asset **COMP-000001** that has been prepared for the **Current** value model on the current application session date.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ebe2a-120">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="ebe2a-120">Additional resources</span></span>

[<span data-ttu-id="ebe2a-121">دالات أخرى (خاصة بمجال الأعمال)</span><span class="sxs-lookup"><span data-stu-id="ebe2a-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]