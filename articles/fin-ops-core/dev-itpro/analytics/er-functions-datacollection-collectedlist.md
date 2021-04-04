---
title: 'وظيفة COLLECTEDLIST ER '
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني COLLECTEDLIST (ER).
author: NickSelin
manager: kfend
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
ms.openlocfilehash: ff48170247130a03b10dc8fe2973f8d774046944
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561388"
---
# <a name="collectedlist-er-function"></a><span data-ttu-id="45ba7-103">وظيفة COLLECTEDLIST ER </span><span class="sxs-lookup"><span data-stu-id="45ba7-103">COLLECTEDLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="45ba7-104">تُرجع وظيفة `COLLECTEDLIST` قيمة *قائمة السجل* التي تحتوي على قائمة القيم التي تم ارجاعها بواسطة خاصية **قيمة مفتاح البيانات التي تم جمعها** من عناصر التنسيق والتي تم جمعها عند استخدام عناصر التنسيق لإنشاء تشغيل مستند صادر أثناء التنسيق، والذي يفي بالشروط المحددة.</span><span class="sxs-lookup"><span data-stu-id="45ba7-104">The `COLLECTEDLIST` function a *Record list* value that contains the list of values that were returned by the **Collected data key value** property of format elements and collected when the format elements were used to generate outbound documents during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="45ba7-105">يتكون كل شرط من نطاق المفتاح وقيمة المفتاح.</span><span class="sxs-lookup"><span data-stu-id="45ba7-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="45ba7-106">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="45ba7-106">Syntax</span></span>

```vb
COLLECTEDLIST (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="45ba7-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="45ba7-107">Arguments</span></span>

<span data-ttu-id="45ba7-108">`condition 1 range`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="45ba7-108">`condition 1 range`: *String*</span></span>

<span data-ttu-id="45ba7-109">القيمة التي يتم إرجاعها بواسطة لتعبير الذي تم تكوينه في خاصية **اسم مفتاح البيانات المُجمعة** لمكون تنسيق التقارير الإلكترونية (ER).</span><span class="sxs-lookup"><span data-stu-id="45ba7-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span> <span data-ttu-id="45ba7-110">هذه الوسيطة إلزامية.</span><span class="sxs-lookup"><span data-stu-id="45ba7-110">This argument is mandatory.</span></span>

<span data-ttu-id="45ba7-111">`condition 1 value`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="45ba7-111">`condition 1 value`: *String*</span></span>

<span data-ttu-id="45ba7-112">القيمة التي يتم إرجاعها بواسطة التعبير الذي تم تكوينه في خاصية **قيمة مفتاح البيانات المُجمعة** لمكون تنسيق ER.</span><span class="sxs-lookup"><span data-stu-id="45ba7-112">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="45ba7-113">هذه الوسيطة إلزامية.</span><span class="sxs-lookup"><span data-stu-id="45ba7-113">This argument is mandatory.</span></span>

<span data-ttu-id="45ba7-114">`condition N range`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="45ba7-114">`condition N range`: *String*</span></span>

<span data-ttu-id="45ba7-115">القيمة التي يتم إرجاعها بواسطة التعبير الذي تم تكوينه في خاصية **اسم مفتاح البيانات المُجمعة** لمكون تنسيق ER.</span><span class="sxs-lookup"><span data-stu-id="45ba7-115">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="45ba7-116">هذه الوسائط الإضافية اختيارية.</span><span class="sxs-lookup"><span data-stu-id="45ba7-116">These additional arguments are optional.</span></span>

<span data-ttu-id="45ba7-117">`condition N value`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="45ba7-117">`condition N value`: *String*</span></span>

<span data-ttu-id="45ba7-118">القيمة التي يتم إرجاعها بواسطة التعبير الذي تم تكوينه في خاصية **قيمة مفتاح البيانات المُجمعة** لمكون تنسيق ER.</span><span class="sxs-lookup"><span data-stu-id="45ba7-118">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="45ba7-119">هذه الوسائط الإضافية اختيارية.</span><span class="sxs-lookup"><span data-stu-id="45ba7-119">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="45ba7-120">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="45ba7-120">Return values</span></span>

<span data-ttu-id="45ba7-121">*قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="45ba7-121">*Record list*</span></span>

<span data-ttu-id="45ba7-122">قائمة السجلات الناتجة.</span><span class="sxs-lookup"><span data-stu-id="45ba7-122">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="45ba7-123">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="45ba7-123">Usage notes</span></span>

<span data-ttu-id="45ba7-124">يُمكن تكوين خصائص **اسم مفتاح البيانات المُجمّعة** و **قيمة مفتاح البيانات المُجمعة** لكل من مكون **التسلسل** أو مكون **عنصر XML** لتنسيق ER الذي يوجد ضمن مكون **ملف\\شائع** حيث يتم تشغيل خيار **تجميع تفاصيل المُخرجات**.</span><span class="sxs-lookup"><span data-stu-id="45ba7-124">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="45ba7-125">تُرجع هذه الوظيفة قائمة فارغة عندما يكون خيار **تجميع تفاصيل المُخرجات** لمكون **ملف\\شائع** متوقف عن التشغيل.</span><span class="sxs-lookup"><span data-stu-id="45ba7-125">This function returns an empty list when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="45ba7-126">في الوسيطة `condition range` ، يُمكن استخدام حرف البدل **"\*"** لتمثيل أي أحرف متعددة.</span><span class="sxs-lookup"><span data-stu-id="45ba7-126">In `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="45ba7-127">في الوسيطة `condition value` ، يُمكن استخدام حرف البدل **"\*"** لتمثيل أي أحرف متعددة.</span><span class="sxs-lookup"><span data-stu-id="45ba7-127">In `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="45ba7-128">مثال</span><span class="sxs-lookup"><span data-stu-id="45ba7-128">Example</span></span>

<span data-ttu-id="45ba7-129">لمزيد من المعلومات حول كيفية استخدام هذه الوظيفة، راجع دليل المهام [التقارير الإلكترونية - استخدام بيانات مخرجات التنسيق لعمليات الجرد والتجميع](tasks/er-format-counting-summing-1.md) جزء من عملية الأعمال **اكتساب/تطوير خدمة تكنولوجيا المعلومات/مكونات الحلول**.</span><span class="sxs-lookup"><span data-stu-id="45ba7-129">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="45ba7-130">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="45ba7-130">Additional resources</span></span>

[<span data-ttu-id="45ba7-131">وظائف تجميع البيانات</span><span class="sxs-lookup"><span data-stu-id="45ba7-131">Data collection functions</span></span>](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]