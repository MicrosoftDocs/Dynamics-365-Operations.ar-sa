---
title: IF ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية IF (ER).
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: a69675e3c743154e8119ba6c04da5897f23a8422
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565894"
---
# <a name="if-er-function"></a><span data-ttu-id="89ae0-103">IF ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="89ae0-103">IF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="89ae0-104">تُرجع الوظيفة `IF` القيمة المُحددة الأولى عند تحقق الشرط المُحدد.</span><span class="sxs-lookup"><span data-stu-id="89ae0-104">The `IF` function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="89ae0-105">وإلا، تُرجع القيمة المحددة الثانية.</span><span class="sxs-lookup"><span data-stu-id="89ae0-105">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="89ae0-106">يُمكن أن تكون القيمة التي يتم إرجاعها قيمة من أي أنواع بيانات مدعومة.</span><span class="sxs-lookup"><span data-stu-id="89ae0-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="89ae0-107">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="89ae0-107">Syntax</span></span>

```vb
IF (condition, first value, second value) as any of the supported data types
```

## <a name="arguments"></a><span data-ttu-id="89ae0-108">الوسائط</span><span class="sxs-lookup"><span data-stu-id="89ae0-108">Arguments</span></span>

<span data-ttu-id="89ae0-109">`condition`: *منطقي*</span><span class="sxs-lookup"><span data-stu-id="89ae0-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="89ae0-110">تعبير شرطي صالح يجب اختباره.</span><span class="sxs-lookup"><span data-stu-id="89ae0-110">A valid conditional expression that must be tested.</span></span>

<span data-ttu-id="89ae0-111">`first value`: *أي من أنواع البيانات المعتمدة*</span><span class="sxs-lookup"><span data-stu-id="89ae0-111">`first value`: *Any of the supported data types*</span></span>

<span data-ttu-id="89ae0-112">النتيجة التي يتم إرجاعها إذا تحقق الشرط.</span><span class="sxs-lookup"><span data-stu-id="89ae0-112">The result that is returned if the condition is met.</span></span>

<span data-ttu-id="89ae0-113">`second value`: *أي من أنواع البيانات المعتمدة*</span><span class="sxs-lookup"><span data-stu-id="89ae0-113">`second value`: *Any of the supported data types*</span></span>

<span data-ttu-id="89ae0-114">النتيجة التي يتم إرجاعها إذا لم يتحقق الشرط.</span><span class="sxs-lookup"><span data-stu-id="89ae0-114">The result that is returned if the condition isn't met.</span></span>

## <a name="return-values"></a><span data-ttu-id="89ae0-115">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="89ae0-115">Return values</span></span>

<span data-ttu-id="89ae0-116">*أي من أنواع البيانات المدعومة*</span><span class="sxs-lookup"><span data-stu-id="89ae0-116">*Any of the supported data types*</span></span>

<span data-ttu-id="89ae0-117">القيمة الناتجة لأي من أنواع البيانات المدعومة.</span><span class="sxs-lookup"><span data-stu-id="89ae0-117">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="89ae0-118">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="89ae0-118">Usage notes</span></span>

<span data-ttu-id="89ae0-119">يجب تحديد الوسيطات `first value` و `second value` باستخدام نفس نوع البيانات.</span><span class="sxs-lookup"><span data-stu-id="89ae0-119">The `first value` and `second value` arguments must be specified by using the same data type.</span></span> <span data-ttu-id="89ae0-120">يتم طرح استثناء في وقت التصميم إذا لم تتطابق أنواع بيانات القيم المكونة.</span><span class="sxs-lookup"><span data-stu-id="89ae0-120">An exception is thrown at design time if the data types of the configured values don't match.</span></span>

<span data-ttu-id="89ae0-121">إذا كانت قيمة النتيجة الأولى وقيمة النتيجة الثانية هي قيم أنواع البيانات *الحاوية (السجل)* أو *قوائم السجلات* ، فإن النتيجة تحتوي فقط على الحقول الموجودة في كلا القيمتين.</span><span class="sxs-lookup"><span data-stu-id="89ae0-121">If the first value and the second value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="89ae0-122">مثال</span><span class="sxs-lookup"><span data-stu-id="89ae0-122">Example</span></span>

<span data-ttu-id="89ae0-123">يُرجع التعبير `IF (1=2, "condition is met", "condition is not met")` السلسلة **عدم تحقق الشرط**.</span><span class="sxs-lookup"><span data-stu-id="89ae0-123">`IF (1=2, "condition is met", "condition is not met")` returns the string **"condition is not met"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="89ae0-124">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="89ae0-124">Additional resources</span></span>

[<span data-ttu-id="89ae0-125">الوظائف المنطقية</span><span class="sxs-lookup"><span data-stu-id="89ae0-125">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]