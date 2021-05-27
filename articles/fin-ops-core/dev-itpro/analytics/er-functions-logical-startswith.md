---
title: وظيفة التقارير الإلكترونية STARTSWITH
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية STARTSWITH.
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
ms.openlocfilehash: 50883bb604d2d1f2947545ce27fa02099e70b0e6
ms.sourcegitcommit: 17cee26b03f7b5afe8a089a0a9b2380e8d377d70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2021
ms.locfileid: "6048832"
---
# <a name="startswith-er-function"></a><span data-ttu-id="706c2-103">وظيفة التقارير الإلكترونية STARTSWITH</span><span class="sxs-lookup"><span data-stu-id="706c2-103">STARTSWITH ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="706c2-104">تحدد وظيفة `STARTSWITH` ما إذا كانت الإدخال المحدد يبدأ بالنص المحدد أم لا.</span><span class="sxs-lookup"><span data-stu-id="706c2-104">The `STARTSWITH` function determines whether the specified input starts with the specified text.</span></span> <span data-ttu-id="706c2-105">تقوم بإرجاع *القيمة المنطقية* **TRUE** إذا كانت المدخلات المحددة تبدأ بالنص المحدد.</span><span class="sxs-lookup"><span data-stu-id="706c2-105">It returns a *Boolean* value of **TRUE** if the specified input starts with the specified text.</span></span> <span data-ttu-id="706c2-106">وبخلاف ذلك، تُرجع قيمة *منطقية* لـ **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="706c2-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="706c2-107">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="706c2-107">Syntax</span></span>

```vb
STARTSWITH (input, start text)
```

## <a name="arguments"></a><span data-ttu-id="706c2-108">الوسائط</span><span class="sxs-lookup"><span data-stu-id="706c2-108">Arguments</span></span>

<span data-ttu-id="706c2-109">`input`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="706c2-109">`input`: *String*</span></span>

<span data-ttu-id="706c2-110">المسار الصالح لعنصر مصدر بيانات من *نوع السلسلة* أو ثابت السلسلة، والذي قد تبدأ قيمته بالوسيطة الثانية.</span><span class="sxs-lookup"><span data-stu-id="706c2-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might start with the second argument.</span></span>

<span data-ttu-id="706c2-111">`start text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="706c2-111">`start text`: *String*</span></span>

<span data-ttu-id="706c2-112">المسار الصالح لمصدر بيانات من *نوع السلسلة* أو ثابت السلسلة، والذي قد تكون قيمته في بداية الوسيطة الأولى.</span><span class="sxs-lookup"><span data-stu-id="706c2-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be at the beginning of the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="706c2-113">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="706c2-113">Return values</span></span>

<span data-ttu-id="706c2-114">*منطقي*</span><span class="sxs-lookup"><span data-stu-id="706c2-114">*Boolean*</span></span>

<span data-ttu-id="706c2-115">القيمة *المنطقية* الناتجة.</span><span class="sxs-lookup"><span data-stu-id="706c2-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="706c2-116">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="706c2-116">Usage notes</span></span>

<span data-ttu-id="706c2-117">يمكن استخدام هذه الوظيفة لتحديد تعبير شرط لوظيفة [FILTER](er-functions-list-filter.md) فقط عند تكوين التعيين المرتبط في [ Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md)للوصول إلى [Microsoft Dataverse](/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="706c2-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](/power-platform/admin/data-integrator).</span></span> <span data-ttu-id="706c2-118">خلاف ذلك، يتم إلقاء استثناء في وقت التصميم.</span><span class="sxs-lookup"><span data-stu-id="706c2-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="706c2-119">توصي الرسالة التي تستلمها باستخدام وظيفة التصفية [WHERE](er-functions-list-where.md) بدلا من وظيفة `FILTER`.</span><span class="sxs-lookup"><span data-stu-id="706c2-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="706c2-120">مثال1</span><span class="sxs-lookup"><span data-stu-id="706c2-120">Example 1</span></span>

<span data-ttu-id="706c2-121">يقوم التعبير `STARTSWITH ("abc", "d")` بإرجاع **FALSE**، بينما يقوم التعبير `STARTSWITH ("abc", "A")` بإرجاع **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="706c2-121">The expression `STARTSWITH ("abc", "d")` returns **FALSE**, whereas the expression `STARTSWITH ("abc", "A")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="706c2-122">مثال2</span><span class="sxs-lookup"><span data-stu-id="706c2-122">Example 2</span></span>

<span data-ttu-id="706c2-123">يقوم التعبير `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` بإرجاع **TRUE** إذا كانت قيمة حقل **العنوان** في مصدر بيانات **النموذج** تبدأ بالسلسلة **123 شارع القهوة**.</span><span class="sxs-lookup"><span data-stu-id="706c2-123">The expression `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` returns **TRUE** if the value of the **Address** field of the **model** data source starts with the string **123 Coffee Street**.</span></span> <span data-ttu-id="706c2-124">وإلا، يتم إرجاع **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="706c2-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="706c2-125">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="706c2-125">Additional resources</span></span>

[<span data-ttu-id="706c2-126">الوظائف المنطقية</span><span class="sxs-lookup"><span data-stu-id="706c2-126">Logical functions</span></span>](er-functions-category-logical.md)
