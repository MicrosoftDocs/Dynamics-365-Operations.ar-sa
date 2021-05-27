---
title: وظيفة التقارير الإلكترونية ENDSWITH
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية ENDSWITH.
author: NickSelin
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 1155bb5446f0370d9a5c4b035a767aaeb1d46ee1
ms.sourcegitcommit: 17cee26b03f7b5afe8a089a0a9b2380e8d377d70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2021
ms.locfileid: "6048884"
---
# <a name="endswith-er-function"></a><span data-ttu-id="39bef-103">وظيفة التقارير الإلكترونية ENDSWITH</span><span class="sxs-lookup"><span data-stu-id="39bef-103">ENDSWITH ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="39bef-104">تحدد وظيفة `ENDSWITH` ما إذا كانت نهايات الإدخال المحددة تنتهي بالنص المحدد أم لا.</span><span class="sxs-lookup"><span data-stu-id="39bef-104">The `ENDSWITH` function determines whether the specified input ends with the specified text.</span></span> <span data-ttu-id="39bef-105">تقوم بإرجاع *القيمة المنطقية* **TRUE** إذا كانت المدخلات المحددة تنتهي بالنص المحدد.</span><span class="sxs-lookup"><span data-stu-id="39bef-105">It returns a *Boolean* value of **TRUE** if the specified input ends with the specified text.</span></span> <span data-ttu-id="39bef-106">وبخلاف ذلك، تُرجع قيمة *منطقية* لـ **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="39bef-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="39bef-107">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="39bef-107">Syntax</span></span>

```vb
ENDSWITH (input, end text)
```

## <a name="arguments"></a><span data-ttu-id="39bef-108">الوسائط</span><span class="sxs-lookup"><span data-stu-id="39bef-108">Arguments</span></span>

<span data-ttu-id="39bef-109">`input`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="39bef-109">`input`: *String*</span></span>

<span data-ttu-id="39bef-110">المسار الصالح لعنصر مصدر بيانات من *نوع السلسلة* أو ثابت السلسلة، والذي قد تنتهي قيمته بالوسيطة الثانية.</span><span class="sxs-lookup"><span data-stu-id="39bef-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might end with the second argument.</span></span>

<span data-ttu-id="39bef-111">`start text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="39bef-111">`start text`: *String*</span></span>

<span data-ttu-id="39bef-112">المسار الصالح لمصدر بيانات من *نوع السلسلة* أو ثابت السلسلة، والذي قد تكون قيمته في نهاية الوسيطة الأولى.</span><span class="sxs-lookup"><span data-stu-id="39bef-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be at the end of the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="39bef-113">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="39bef-113">Return values</span></span>

<span data-ttu-id="39bef-114">*منطقي*</span><span class="sxs-lookup"><span data-stu-id="39bef-114">*Boolean*</span></span>

<span data-ttu-id="39bef-115">القيمة *المنطقية* الناتجة.</span><span class="sxs-lookup"><span data-stu-id="39bef-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="39bef-116">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="39bef-116">Usage notes</span></span>

<span data-ttu-id="39bef-117">يمكن استخدام هذه الوظيفة لتحديد تعبير شرط لوظيفة [FILTER](er-functions-list-filter.md) فقط عند تكوين التعيين المرتبط في [ Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md)للوصول إلى [Microsoft Dataverse](/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="39bef-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](/power-platform/admin/data-integrator).</span></span> <span data-ttu-id="39bef-118">خلاف ذلك، يتم إلقاء استثناء في وقت التصميم.</span><span class="sxs-lookup"><span data-stu-id="39bef-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="39bef-119">توصي الرسالة التي تستلمها باستخدام وظيفة التصفية [WHERE](er-functions-list-where.md) بدلا من وظيفة `FILTER`.</span><span class="sxs-lookup"><span data-stu-id="39bef-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="39bef-120">مثال1</span><span class="sxs-lookup"><span data-stu-id="39bef-120">Example 1</span></span>

<span data-ttu-id="39bef-121">يقوم التعبير `ENDSWITH ("abc", "d")` بإرجاع **FALSE**، بينما يقوم التعبير `ENDSWITH ("abc", "C")` بإرجاع **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="39bef-121">The expression `ENDSWITH ("abc", "d")` returns **FALSE**, whereas the expression `ENDSWITH ("abc", "C")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="39bef-122">مثال2</span><span class="sxs-lookup"><span data-stu-id="39bef-122">Example 2</span></span>

<span data-ttu-id="39bef-123">يقوم التعبير `ENDSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "USA")` بإرجاع **TRUE** إذا كانت قيمة حقل **العنوان** في مصدر بيانات **النموذج** تنتهي بالسلسلة **الولايات المتحدة**.</span><span class="sxs-lookup"><span data-stu-id="39bef-123">The expression `ENDSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "USA")` returns **TRUE** if the value of the **Address** field of the **model** data source ends with the string **USA**.</span></span> <span data-ttu-id="39bef-124">وإلا، يتم إرجاع **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="39bef-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="39bef-125">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="39bef-125">Additional resources</span></span>

[<span data-ttu-id="39bef-126">الوظائف المنطقية</span><span class="sxs-lookup"><span data-stu-id="39bef-126">Logical functions</span></span>](er-functions-category-logical.md)
