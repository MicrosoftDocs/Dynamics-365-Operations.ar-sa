---
title: وظيفة التقرير الإلكترونية CONTAINS
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية CONTAINS (ER).
author: NickSelin
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: c1d2d761a38d0edfb9abd439e0f710b336f54927
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745415"
---
# <a name="contains-er-function"></a><span data-ttu-id="c8483-103">وظيفة التقرير الإلكترونية CONTAINS</span><span class="sxs-lookup"><span data-stu-id="c8483-103">CONTAINS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c8483-104">تحدد وظيفة `CONTAINS` ما إذا كان الإدخال المحدد يحتوي على النص المحدد أم لا.</span><span class="sxs-lookup"><span data-stu-id="c8483-104">The `CONTAINS` function determines whether the specified input contains the specified text.</span></span> <span data-ttu-id="c8483-105">تقوم بإرجاع *القيمة المنطقية* **TRUE** إذا كان الإدخال المحدد يحتوي على النص المحدد.</span><span class="sxs-lookup"><span data-stu-id="c8483-105">It returns a *Boolean* value of **TRUE** if the specified input contains the specified text.</span></span> <span data-ttu-id="c8483-106">وبخلاف ذلك، تُرجع قيمة *منطقية* لـ **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="c8483-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8483-107">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="c8483-107">Syntax</span></span>

```vb
CONTAINS (input, search text)
```

## <a name="arguments"></a><span data-ttu-id="c8483-108">الوسائط</span><span class="sxs-lookup"><span data-stu-id="c8483-108">Arguments</span></span>

<span data-ttu-id="c8483-109">`input`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="c8483-109">`input`: *String*</span></span>

<span data-ttu-id="c8483-110">المسار الصالح لعنصر مصدر بيانات من *نوع السلسلة* أو ثابت السلسلة، والذي قد تحتوي قيمته على الوسيطة الثانية.</span><span class="sxs-lookup"><span data-stu-id="c8483-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might contain the second argument.</span></span>

<span data-ttu-id="c8483-111">`search text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="c8483-111">`search text`: *String*</span></span>

<span data-ttu-id="c8483-112">المسار الصالح لمصدر بيانات من *نوع السلسلة* أو ثابت السلسلة، والذي قد تكون قيمته متضمنة في الوسيطة الأولى.</span><span class="sxs-lookup"><span data-stu-id="c8483-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be contained in the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="c8483-113">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="c8483-113">Return values</span></span>

<span data-ttu-id="c8483-114">*منطقي*</span><span class="sxs-lookup"><span data-stu-id="c8483-114">*Boolean*</span></span>

<span data-ttu-id="c8483-115">القيمة *المنطقية* الناتجة.</span><span class="sxs-lookup"><span data-stu-id="c8483-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c8483-116">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="c8483-116">Usage notes</span></span>

<span data-ttu-id="c8483-117">يمكن استخدام هذه الوظيفة لتحديد تعبير شرط لوظيفة [FILTER](er-functions-list-filter.md) فقط عند تكوين التعيين المرتبط في [ Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md)للوصول إلى [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span><span class="sxs-lookup"><span data-stu-id="c8483-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span></span> <span data-ttu-id="c8483-118">خلاف ذلك، يتم إلقاء استثناء في وقت التصميم.</span><span class="sxs-lookup"><span data-stu-id="c8483-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="c8483-119">توصي الرسالة التي تستلمها باستخدام وظيفة التصفية [WHERE](er-functions-list-where.md) بدلا من وظيفة `FILTER`.</span><span class="sxs-lookup"><span data-stu-id="c8483-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="c8483-120">مثال1</span><span class="sxs-lookup"><span data-stu-id="c8483-120">Example 1</span></span>

<span data-ttu-id="c8483-121">يقوم التعبير `CONTAINS ("abc", "d")` بإرجاع **FALSE**، بينما يقوم التعبير `CONTAINS ("abc", "C")` بإرجاع **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="c8483-121">The expression `CONTAINS ("abc", "d")` returns **FALSE**, whereas the expression `CONTAINS ("abc", "C")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="c8483-122">مثال2</span><span class="sxs-lookup"><span data-stu-id="c8483-122">Example 2</span></span>

<span data-ttu-id="c8483-123">يقوم التعبير `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` بإرجاع **TRUE** إذا كانت قيمة حقل **العنوان** في مصدر بيانات **النموذج** يحتوي على السلسلة **DEU**.</span><span class="sxs-lookup"><span data-stu-id="c8483-123">The expression `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` returns **TRUE** if the value of the **Address** field of the **model** data source contains the string **DEU**.</span></span> <span data-ttu-id="c8483-124">وإلا، يتم إرجاع **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="c8483-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c8483-125">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="c8483-125">Additional resources</span></span>

[<span data-ttu-id="c8483-126">الوظائف المنطقية</span><span class="sxs-lookup"><span data-stu-id="c8483-126">Logical functions</span></span>](er-functions-category-logical.md)
