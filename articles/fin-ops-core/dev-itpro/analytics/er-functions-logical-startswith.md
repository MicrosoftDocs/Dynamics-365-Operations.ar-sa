---
title: وظيفة التقارير الإلكترونية STARTSWITH
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية STARTSWITH.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 22e99d9e131410820abd12536b8d4f3e868c6863
ms.sourcegitcommit: 08ac570bece3e4ee4a0f632f51623e328536dfcf
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/08/2021
ms.locfileid: "5557495"
---
# <a name="startswith-er-function"></a><span data-ttu-id="eeb2c-103">وظيفة التقارير الإلكترونية STARTSWITH</span><span class="sxs-lookup"><span data-stu-id="eeb2c-103">STARTSWITH ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eeb2c-104">تحدد وظيفة `STARTSWITH` ما إذا كانت الإدخال المحدد يبدأ بالنص المحدد أم لا.</span><span class="sxs-lookup"><span data-stu-id="eeb2c-104">The `STARTSWITH` function determines whether the specified input starts with the specified text.</span></span> <span data-ttu-id="eeb2c-105">تقوم بإرجاع *القيمة المنطقية* **TRUE** إذا كانت المدخلات المحددة تبدأ بالنص المحدد.</span><span class="sxs-lookup"><span data-stu-id="eeb2c-105">It returns a *Boolean* value of **TRUE** if the specified input starts with the specified text.</span></span> <span data-ttu-id="eeb2c-106">وبخلاف ذلك، تُرجع قيمة *منطقية* لـ **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="eeb2c-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="eeb2c-107">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="eeb2c-107">Syntax</span></span>

```vb
STARTSWITH (input, start text)
```

## <a name="arguments"></a><span data-ttu-id="eeb2c-108">الوسائط</span><span class="sxs-lookup"><span data-stu-id="eeb2c-108">Arguments</span></span>

<span data-ttu-id="eeb2c-109">`input`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="eeb2c-109">`input`: *String*</span></span>

<span data-ttu-id="eeb2c-110">المسار الصالح لعنصر مصدر بيانات من *نوع السلسلة* أو ثابت السلسلة، والذي قد تبدأ قيمته بالوسيطة الثانية.</span><span class="sxs-lookup"><span data-stu-id="eeb2c-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might start with the second argument.</span></span>

<span data-ttu-id="eeb2c-111">`start text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="eeb2c-111">`start text`: *String*</span></span>

<span data-ttu-id="eeb2c-112">المسار الصالح لمصدر بيانات من *نوع السلسلة* أو ثابت السلسلة، والذي قد تكون قيمته في بداية الوسيطة الأولى.</span><span class="sxs-lookup"><span data-stu-id="eeb2c-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be at the beginning of the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="eeb2c-113">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="eeb2c-113">Return values</span></span>

<span data-ttu-id="eeb2c-114">*منطقي*</span><span class="sxs-lookup"><span data-stu-id="eeb2c-114">*Boolean*</span></span>

<span data-ttu-id="eeb2c-115">القيمة *المنطقية* الناتجة.</span><span class="sxs-lookup"><span data-stu-id="eeb2c-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="eeb2c-116">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="eeb2c-116">Usage notes</span></span>

<span data-ttu-id="eeb2c-117">يمكن استخدام هذه الوظيفة لتحديد تعبير شرط لوظيفة [FILTER](er-functions-list-filter.md) فقط عند تكوين التعيين المرتبط في [ Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md)للوصول إلى [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span><span class="sxs-lookup"><span data-stu-id="eeb2c-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span></span> <span data-ttu-id="eeb2c-118">خلاف ذلك، يتم إلقاء استثناء في وقت التصميم.</span><span class="sxs-lookup"><span data-stu-id="eeb2c-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="eeb2c-119">توصي الرسالة التي تستلمها باستخدام وظيفة التصفية [WHERE](er-functions-list-where.md) بدلا من وظيفة `FILTER`.</span><span class="sxs-lookup"><span data-stu-id="eeb2c-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="eeb2c-120">مثال1</span><span class="sxs-lookup"><span data-stu-id="eeb2c-120">Example 1</span></span>

<span data-ttu-id="eeb2c-121">يقوم التعبير `STARTSWITH ("abc", "d")` بإرجاع **FALSE**، بينما يقوم التعبير `STARTSWITH ("abc", "A")` بإرجاع **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="eeb2c-121">The expression `STARTSWITH ("abc", "d")` returns **FALSE**, whereas the expression `STARTSWITH ("abc", "A")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="eeb2c-122">مثال2</span><span class="sxs-lookup"><span data-stu-id="eeb2c-122">Example 2</span></span>

<span data-ttu-id="eeb2c-123">يقوم التعبير `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` بإرجاع **TRUE** إذا كانت قيمة حقل **العنوان** في مصدر بيانات **النموذج** تبدأ بالسلسلة **123 شارع القهوة**.</span><span class="sxs-lookup"><span data-stu-id="eeb2c-123">The expression `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` returns **TRUE** if the value of the **Address** field of the **model** data source starts with the string **123 Coffee Street**.</span></span> <span data-ttu-id="eeb2c-124">وإلا، يتم إرجاع **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="eeb2c-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eeb2c-125">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="eeb2c-125">Additional resources</span></span>

[<span data-ttu-id="eeb2c-126">الوظائف المنطقية</span><span class="sxs-lookup"><span data-stu-id="eeb2c-126">Logical functions</span></span>](er-functions-category-logical.md)
