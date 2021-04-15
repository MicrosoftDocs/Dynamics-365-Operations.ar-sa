---
title: وظيفة SUMIFS ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية SUMIFS (ER).
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: a3adfe62d9fd7bdc23784cf7311f65a4d2e88960
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747073"
---
# <a name="sumifs-er-function"></a><span data-ttu-id="e1472-103">وظيفة SUMIFS ER</span><span class="sxs-lookup"><span data-stu-id="e1472-103">SUMIFS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1472-104">تُرجع الوظيفة `SUMIFS` قيمة *حقيقية* الذي يمثل مجموع القيم التي تم إرجاعها بواسطة روابط عناصر التنسيق والتي تم جمعها عند استخدام عناصر التنسيق لإنشاء مستند صادر أثناء تشغيل التنسيق، والتي تفي بالشروط المحددة.</span><span class="sxs-lookup"><span data-stu-id="e1472-104">The `SUMIFS` function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="e1472-105">يتكون كل شرط من نطاق المفتاح وقيمة المفتاح.</span><span class="sxs-lookup"><span data-stu-id="e1472-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1472-106">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="e1472-106">Syntax</span></span>

```vb
SUMIFS (key name for summing, condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="e1472-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="e1472-107">Arguments</span></span>

<span data-ttu-id="e1472-108">`key name for summing`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="e1472-108">`key name for summing`: *String*</span></span>

<span data-ttu-id="e1472-109">القيمة التي يتم إرجاعها بواسطة التعبير الذي تم تكوينه في خاصية **اسم مفتاح البيانات المُجمعة** لمكون تنسيق التقارير الإلكترونية (ER) الذي يجب استخدام قيمة الربط لأغراض التجميع.</span><span class="sxs-lookup"><span data-stu-id="e1472-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of the Electronic reporting (ER) format component for which the value of the binding must be used for summing purposes.</span></span>

<span data-ttu-id="e1472-110">يُمكن تكوين خاصية **اسم مفتاح البيانات المُجمّعة** لكل من مكون **رقمي** أو مكون **السلسلة** لتنسيق ER الذي يوجد ضمن مكون **ملف\\شائع** حيث يتم تشغيل خيار **تجميع تفاصيل المُخرجات**.</span><span class="sxs-lookup"><span data-stu-id="e1472-110">The **Collected data key name** property can be configured for either a **Numeric** component or a **String** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="e1472-111">`condition 1 range`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="e1472-111">`condition 1 range`: *String*</span></span>

<span data-ttu-id="e1472-112">القيمة التي يتم إرجاعها بواسطة التعبير الذي تم تكوينه في خاصية **اسم مفتاح البيانات المُجمعة** لمكون تنسيق ER.</span><span class="sxs-lookup"><span data-stu-id="e1472-112">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="e1472-113">هذه الوسيطة إلزامية.</span><span class="sxs-lookup"><span data-stu-id="e1472-113">This argument is mandatory.</span></span>

<span data-ttu-id="e1472-114">يُمكن تكوين خاصية **اسم مفتاح البيانات المُجمّعة** لكل من مكون **التسلسل** أو مكون **عنصر XML** لتنسيق ER الذي يوجد ضمن مكون **ملف\\شائع** حيث يتم تشغيل خيار **تجميع تفاصيل المُخرجات**.</span><span class="sxs-lookup"><span data-stu-id="e1472-114">The **Collected data key name** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="e1472-115">`condition 1 value`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="e1472-115">`condition 1 value`: *String*</span></span>

<span data-ttu-id="e1472-116">القيمة التي يتم إرجاعها بواسطة التعبير الذي تم تكوينه في خاصية **قيمة مفتاح البيانات المُجمعة** لمكون تنسيق ER.</span><span class="sxs-lookup"><span data-stu-id="e1472-116">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="e1472-117">هذه الوسيطة إلزامية.</span><span class="sxs-lookup"><span data-stu-id="e1472-117">This argument is mandatory.</span></span>

<span data-ttu-id="e1472-118">يُمكن تكوين خاصية **اسم مفتاح البيانات المُجمّعة** لكل من مكون **التسلسل** أو مكون **عنصر XML** لتنسيق ER الذي يوجد ضمن مكون **ملف\\شائع** حيث يتم تشغيل خيار **تجميع تفاصيل المُخرجات**.</span><span class="sxs-lookup"><span data-stu-id="e1472-118">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="e1472-119">`condition N range`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="e1472-119">`condition N range`: *String*</span></span>

<span data-ttu-id="e1472-120">القيمة التي يتم إرجاعها بواسطة التعبير الذي تم تكوينه في خاصية **اسم مفتاح البيانات المُجمعة** لمكون تنسيق ER.</span><span class="sxs-lookup"><span data-stu-id="e1472-120">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="e1472-121">هذه الوسائط الإضافية اختيارية.</span><span class="sxs-lookup"><span data-stu-id="e1472-121">These additional arguments are optional.</span></span>

<span data-ttu-id="e1472-122">يُمكن تكوين خاصية **اسم مفتاح البيانات المُجمّعة** لكل من مكون **التسلسل** أو مكون **عنصر XML** لتنسيق ER الذي يوجد ضمن مكون **ملف\\شائع** حيث يتم تشغيل خيار **تجميع تفاصيل المُخرجات**.</span><span class="sxs-lookup"><span data-stu-id="e1472-122">The **Collected data key name** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="e1472-123">`condition N value`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="e1472-123">`condition N value`: *String*</span></span>

<span data-ttu-id="e1472-124">القيمة التي يتم إرجاعها بواسطة التعبير الذي تم تكوينه في خاصية **قيمة مفتاح البيانات المُجمعة** لمكون تنسيق ER.</span><span class="sxs-lookup"><span data-stu-id="e1472-124">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="e1472-125">هذه الوسائط الإضافية اختيارية.</span><span class="sxs-lookup"><span data-stu-id="e1472-125">These additional arguments are optional.</span></span>

<span data-ttu-id="e1472-126">يُمكن تكوين خاصية **اسم مفتاح البيانات المُجمّعة** لكل من مكون **التسلسل** أو مكون **عنصر XML** لتنسيق ER الذي يوجد ضمن مكون **ملف\\شائع** حيث يتم تشغيل خيار **تجميع تفاصيل المُخرجات**.</span><span class="sxs-lookup"><span data-stu-id="e1472-126">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="return-values"></a><span data-ttu-id="e1472-127">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="e1472-127">Return values</span></span>

<span data-ttu-id="e1472-128">*حقيقي*</span><span class="sxs-lookup"><span data-stu-id="e1472-128">*Real*</span></span>

<span data-ttu-id="e1472-129">القيمة العددية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="e1472-129">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e1472-130">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="e1472-130">Usage notes</span></span>

<span data-ttu-id="e1472-131">تُرجع هذه الوظيفة قيمة **0** (صفر) عندما يتوقف تشغيل خيار **تجميع تفاصيل المُخرجات** لمكون **ملف\\شائع**.</span><span class="sxs-lookup"><span data-stu-id="e1472-131">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="e1472-132">في الوسيطات `condition range` ، يُمكن استخدام حرف البدل **"\*"** لتمثيل أي أحرف متعددة.</span><span class="sxs-lookup"><span data-stu-id="e1472-132">In the `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="e1472-133">في الوسيطات `condition value` ، يُمكن استخدام حرف البدل **"\*"** لتمثيل أي أحرف متعددة.</span><span class="sxs-lookup"><span data-stu-id="e1472-133">In the `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="e1472-134">مثال</span><span class="sxs-lookup"><span data-stu-id="e1472-134">Example</span></span>

<span data-ttu-id="e1472-135">لمزيد من المعلومات حول كيفية استخدام هذه الوظيفة، راجع دليل المهام [التقارير الإلكترونية - استخدام بيانات مخرجات التنسيق لعمليات الجرد والتجميع](tasks/er-format-counting-summing-1.md) جزء من عملية الأعمال **اكتساب/تطوير خدمة تكنولوجيا المعلومات/مكونات الحلول**.</span><span class="sxs-lookup"><span data-stu-id="e1472-135">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e1472-136">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="e1472-136">Additional resources</span></span>

[<span data-ttu-id="e1472-137">وظائف تجميع البيانات</span><span class="sxs-lookup"><span data-stu-id="e1472-137">Data collection functions</span></span>](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]