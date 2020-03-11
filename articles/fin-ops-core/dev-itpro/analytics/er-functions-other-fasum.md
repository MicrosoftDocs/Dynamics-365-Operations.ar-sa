---
title: FA_SUM ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية FA_SUM (ER).
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
ms.openlocfilehash: 03bed091350b39601edb22b5af6bda5a83af47eb
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041344"
---
# <span data-ttu-id="fd12c-103"><a name="FA_SUM">FA_SUM ER وظيفة</a></span><span class="sxs-lookup"><span data-stu-id="fd12c-103"><a name="FA_SUM">FA_SUM ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fd12c-104">تُرجع الوظيفة `FA_SUM` قيمة *حاوية (سجل)* تتكون من بيانات لمبالغ الأصول الثابتة لعنصر الأصل الثابت المُحدد وكود نموذج القيمة والفترات المرتبطة بالتواريخ.</span><span class="sxs-lookup"><span data-stu-id="fd12c-104">The `FA_SUM` function returns a *Container (record)* value that consists of data for the fixed asset amounts for the specified fixed asset item, value model code, and period of dates.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd12c-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="fd12c-105">Syntax</span></span>

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a><span data-ttu-id="fd12c-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="fd12c-106">Arguments</span></span>

<span data-ttu-id="fd12c-107">`fixed asset code`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="fd12c-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="fd12c-108">قيمة *السلسلة* التي تمثل كود الأصل الثابت الذي يتم حساب الرصيد له.</span><span class="sxs-lookup"><span data-stu-id="fd12c-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="fd12c-109">`value model code`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="fd12c-109">`value model code`: *String*</span></span>

<span data-ttu-id="fd12c-110">قيمة *السلسلة* التي تمثل كود نموذج القيمة الذي يتم حساب الرصيد له.</span><span class="sxs-lookup"><span data-stu-id="fd12c-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="fd12c-111">`start date`: *التاريخ*</span><span class="sxs-lookup"><span data-stu-id="fd12c-111">`start date`: *Date*</span></span>

<span data-ttu-id="fd12c-112">قيمة *التاريخ* التي تمثل تاريخ بدء الفترة التي تم حساب مبالغ الأصول الثابتة لها.</span><span class="sxs-lookup"><span data-stu-id="fd12c-112">A *Date* value that represents the start date of a period that the fixed asset amounts are calculated for.</span></span>

<span data-ttu-id="fd12c-113">`end date`: *التاريخ*</span><span class="sxs-lookup"><span data-stu-id="fd12c-113">`end date`: *Date*</span></span>

<span data-ttu-id="fd12c-114">قيمة *التاريخ* التي تمثل تاريخ نهاية الفترة التي تم حساب مبالغ الأصول الثابتة لها.</span><span class="sxs-lookup"><span data-stu-id="fd12c-114">A *Date* value that represents the end date of a period that the fixed asset amounts are calculated for.</span></span>

## <a name="return-values"></a><span data-ttu-id="fd12c-115">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="fd12c-115">Return values</span></span>

<span data-ttu-id="fd12c-116">*حاوية (سجل)*</span><span class="sxs-lookup"><span data-stu-id="fd12c-116">*Container (record)*</span></span>

<span data-ttu-id="fd12c-117">قيمة السجل الناتجة.</span><span class="sxs-lookup"><span data-stu-id="fd12c-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="fd12c-118">مثال</span><span class="sxs-lookup"><span data-stu-id="fd12c-118">Example</span></span>

<span data-ttu-id="fd12c-119">يُرجع التعبير `FA_SUM ("COMP-000001", "Current", Date1, Date2)` حاوية بيانات الأصل الثابت **COMP-000001** التي تم إعدادها لنموذج القيمة **الحالية** ولمدة من **Date1** إلى **Date2**.</span><span class="sxs-lookup"><span data-stu-id="fd12c-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` returns the data container for fixed asset **COMP-000001** that has been prepared for the **Current** value model and for a period from **Date1** to **Date2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fd12c-120">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="fd12c-120">Additional resources</span></span>

[<span data-ttu-id="fd12c-121">دالات أخرى (خاصة بمجال الأعمال)</span><span class="sxs-lookup"><span data-stu-id="fd12c-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
