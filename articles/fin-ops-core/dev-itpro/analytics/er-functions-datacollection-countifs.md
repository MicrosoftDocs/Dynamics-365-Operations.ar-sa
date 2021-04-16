---
title: 'وظيفة COUNTIFS ER '
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية COUNTIFS (ER).
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 667002aa01537f846c616d38bba436da18f6e05f
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755266"
---
# <a name="countifs-er-function"></a><span data-ttu-id="e0f0a-103">وظيفة COUNTIFS ER </span><span class="sxs-lookup"><span data-stu-id="e0f0a-103">COUNTIFS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e0f0a-104">تُرجع وظيفة `COUNTIFS` قيمة *عدد صحيح* الذي يمثل رقم عناصر التنسيق التي تم تجميعها عند استخدام عناصر التنسيق لإنشاء مستند صادر أثناء تشغيل التنسيق، والذي يفي بالشروط المحددة.</span><span class="sxs-lookup"><span data-stu-id="e0f0a-104">The `COUNTIFS` function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="e0f0a-105">يتكون كل شرط من نطاق المفتاح وقيمة المفتاح.</span><span class="sxs-lookup"><span data-stu-id="e0f0a-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0f0a-106">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="e0f0a-106">Syntax</span></span>

```vb
COUNTIFS (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="e0f0a-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="e0f0a-107">Arguments</span></span>

<span data-ttu-id="e0f0a-108">`condition 1 range`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="e0f0a-108">`condition 1 range`: *String*</span></span>

<span data-ttu-id="e0f0a-109">القيمة التي يتم إرجاعها بواسطة لتعبير الذي تم تكوينه في خاصية **اسم مفتاح البيانات المُجمعة** لمكون تنسيق التقارير الإلكترونية (ER).</span><span class="sxs-lookup"><span data-stu-id="e0f0a-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span> <span data-ttu-id="e0f0a-110">هذه الوسيطة إلزامية.</span><span class="sxs-lookup"><span data-stu-id="e0f0a-110">This argument is mandatory.</span></span>

<span data-ttu-id="e0f0a-111">`condition 1 value`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="e0f0a-111">`condition 1 value`: *String*</span></span>

<span data-ttu-id="e0f0a-112">القيمة التي يتم إرجاعها بواسطة التعبير الذي تم تكوينه في خاصية **قيمة مفتاح البيانات المُجمعة** لمكون تنسيق ER.</span><span class="sxs-lookup"><span data-stu-id="e0f0a-112">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="e0f0a-113">هذه الوسيطة إلزامية.</span><span class="sxs-lookup"><span data-stu-id="e0f0a-113">This argument is mandatory.</span></span>

<span data-ttu-id="e0f0a-114">`condition N range`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="e0f0a-114">`condition N range`: *String*</span></span>

<span data-ttu-id="e0f0a-115">القيمة التي يتم إرجاعها بواسطة التعبير الذي تم تكوينه في خاصية **اسم مفتاح البيانات المُجمعة** لمكون تنسيق ER.</span><span class="sxs-lookup"><span data-stu-id="e0f0a-115">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="e0f0a-116">هذه الوسائط الإضافية اختيارية.</span><span class="sxs-lookup"><span data-stu-id="e0f0a-116">These additional arguments are optional.</span></span>

<span data-ttu-id="e0f0a-117">`condition N value`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="e0f0a-117">`condition N value`: *String*</span></span>

<span data-ttu-id="e0f0a-118">القيمة التي يتم إرجاعها بواسطة التعبير الذي تم تكوينه في خاصية **قيمة مفتاح البيانات المُجمعة** لمكون تنسيق ER.</span><span class="sxs-lookup"><span data-stu-id="e0f0a-118">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="e0f0a-119">هذه الوسائط الإضافية اختيارية.</span><span class="sxs-lookup"><span data-stu-id="e0f0a-119">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="e0f0a-120">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="e0f0a-120">Return values</span></span>

<span data-ttu-id="e0f0a-121">*عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="e0f0a-121">*Integer*</span></span>

<span data-ttu-id="e0f0a-122">القيمة العددية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="e0f0a-122">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e0f0a-123">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="e0f0a-123">Usage notes</span></span>

<span data-ttu-id="e0f0a-124">يُمكن تكوين خصائص **اسم مفتاح البيانات المُجمّعة** و **قيمة مفتاح البيانات المُجمعة** لكل من مكون **التسلسل** أو مكون **عنصر XML** لتنسيق ER الذي يوجد ضمن مكون **ملف\\شائع** حيث يتم تشغيل خيار **تجميع تفاصيل المُخرجات**.</span><span class="sxs-lookup"><span data-stu-id="e0f0a-124">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="e0f0a-125">تُرجع هذه الوظيفة قيمة **0** (صفر) عندما يتوقف تشغيل خيار **تجميع تفاصيل المُخرجات** لمكون **ملف\\شائع**.</span><span class="sxs-lookup"><span data-stu-id="e0f0a-125">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="e0f0a-126">في الوسيطة `condition range` ، يُمكن استخدام حرف البدل **"\*"** لتمثيل أي أحرف متعددة.</span><span class="sxs-lookup"><span data-stu-id="e0f0a-126">In `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="e0f0a-127">في الوسيطة `condition value` ، يُمكن استخدام حرف البدل **"\*"** لتمثيل أي أحرف متعددة.</span><span class="sxs-lookup"><span data-stu-id="e0f0a-127">In `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="e0f0a-128">مثال</span><span class="sxs-lookup"><span data-stu-id="e0f0a-128">Example</span></span>

<span data-ttu-id="e0f0a-129">لمزيد من المعلومات حول كيفية استخدام هذه الوظيفة، راجع دليل المهام [التقارير الإلكترونية - استخدام بيانات مخرجات التنسيق لعمليات الجرد والتجميع](tasks/er-format-counting-summing-1.md) جزء من عملية الأعمال **اكتساب/تطوير خدمة تكنولوجيا المعلومات/مكونات الحلول**.</span><span class="sxs-lookup"><span data-stu-id="e0f0a-129">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e0f0a-130">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="e0f0a-130">Additional resources</span></span>

[<span data-ttu-id="e0f0a-131">وظائف تجميع البيانات</span><span class="sxs-lookup"><span data-stu-id="e0f0a-131">Data collection functions</span></span>](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]