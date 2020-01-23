---
title: FA_BALANCE ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية FA_BALANCE (ER).
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
ms.openlocfilehash: 0907cb8cb4bc1e90b9fb59eccedb699a894b5cc9
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916006"
---
# <span data-ttu-id="1dd8b-103"><a name="FA_BALANCE">FA_BALANCE ER وظيفة</a></span><span class="sxs-lookup"><span data-stu-id="1dd8b-103"><a name="FA_BALANCE">FA_BALANCE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1dd8b-104">تُرجع الوظيفة `FA_BALANCE` قيمة *حاوية (سجل)* تتكون من بيانات لرصيد الأصل الثابت لعنصر الأصل الثابت المُحدد وكود نموذج القيمة وسنة إعداد التقرير وتاريخ إعداد التقرير.</span><span class="sxs-lookup"><span data-stu-id="1dd8b-104">The `FA_BALANCE` function returns a *Container (record)* value that consists of data for the fixed asset balance for the specified fixed asset item, value model code, reporting year, and reporting date.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dd8b-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="1dd8b-105">Syntax</span></span>

```
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a><span data-ttu-id="1dd8b-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="1dd8b-106">Arguments</span></span>

<span data-ttu-id="1dd8b-107">`fixed asset code`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="1dd8b-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="1dd8b-108">قيمة *السلسلة* التي تمثل كود الأصل الثابت الذي يتم حساب الرصيد له.</span><span class="sxs-lookup"><span data-stu-id="1dd8b-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="1dd8b-109">`value model code`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="1dd8b-109">`value model code`: *String*</span></span>

<span data-ttu-id="1dd8b-110">قيمة *السلسلة* التي تمثل كود نموذج القيمة الذي يتم حساب الرصيد له.</span><span class="sxs-lookup"><span data-stu-id="1dd8b-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="1dd8b-111">`reporting year`: *قيمة التعداد*</span><span class="sxs-lookup"><span data-stu-id="1dd8b-111">`reporting year`: *Enumeration value*</span></span>

<span data-ttu-id="1dd8b-112">قيمة التعداد لتعداد تطبيق **AssetYear** التي تُعرف فترة لحساب الرصيد.</span><span class="sxs-lookup"><span data-stu-id="1dd8b-112">An enumeration value of the **AssetYear** application enumeration that defines a period for the balance calculation.</span></span>

<span data-ttu-id="1dd8b-113">`reporting date`: *التاريخ*</span><span class="sxs-lookup"><span data-stu-id="1dd8b-113">`reporting date`: *Date*</span></span>

<span data-ttu-id="1dd8b-114">قيمة *التاريخ* التي تعرف تاريخ لحساب الرصيد.</span><span class="sxs-lookup"><span data-stu-id="1dd8b-114">A *Date* value that defines a date for the balance calculation.</span></span>

## <a name="return-values"></a><span data-ttu-id="1dd8b-115">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="1dd8b-115">Return values</span></span>

<span data-ttu-id="1dd8b-116">*حاوية (سجل)*</span><span class="sxs-lookup"><span data-stu-id="1dd8b-116">*Container (record)*</span></span>

<span data-ttu-id="1dd8b-117">قيمة السجل الناتجة.</span><span class="sxs-lookup"><span data-stu-id="1dd8b-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="1dd8b-118">مثال</span><span class="sxs-lookup"><span data-stu-id="1dd8b-118">Example</span></span>

<span data-ttu-id="1dd8b-119">يُرجع التعبير `FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` حاوية بيانات الأرصدة المعدة للأصل الثابت **COMP-000001** الذي لديه نموذج القيمة **الحالية** في تاريخ جلسة عمل التطبيق الحالية.</span><span class="sxs-lookup"><span data-stu-id="1dd8b-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` returns the data container of balances for fixed asset **COMP-000001** that has been prepared for the **Current** value model on the current application session date.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1dd8b-120">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="1dd8b-120">Additional resources</span></span>

[<span data-ttu-id="1dd8b-121">دالات أخرى (خاصة بمجال الأعمال)</span><span class="sxs-lookup"><span data-stu-id="1dd8b-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)