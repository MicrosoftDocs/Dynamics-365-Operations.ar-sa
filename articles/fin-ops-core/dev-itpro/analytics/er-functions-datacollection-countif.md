---
title: 'وظيفة COUNTIF ER '
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية COUNTIF (ER).
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: ca7c0f449aff75527e5052ba01e6fc0e29bb0fd7
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917685"
---
# <span data-ttu-id="92771-103"><a name="COUNTIF">وظيفة COUNTIF ER </a></span><span class="sxs-lookup"><span data-stu-id="92771-103"><a name="COUNTIF">COUNTIF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="92771-104">تُرجع وظيفة `COUNTIF` قيمة *عدد صحيح* الذي يمثل رقم عناصر التنسيق التي تم تجميعها عند استخدام عناصر التنسيق لإنشاء مستند صادر أثناء تشغيل التنسيق، والذي يفي بالشرط المحدد.</span><span class="sxs-lookup"><span data-stu-id="92771-104">The `COUNTIF` function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="92771-105">يتكون الشرط من نطاق المفتاح وقيمة المفتاح.</span><span class="sxs-lookup"><span data-stu-id="92771-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="92771-106">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="92771-106">Syntax</span></span>

```
COUNTIF (condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="92771-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="92771-107">Arguments</span></span>

<span data-ttu-id="92771-108">`condition range`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="92771-108">`condition range`: *String*</span></span>

<span data-ttu-id="92771-109">القيمة التي يتم إرجاعها بواسطة لتعبير الذي تم تكوينه في خاصية **اسم مفتاح البيانات المُجمعة** لمكون تنسيق التقارير الإلكترونية (ER).</span><span class="sxs-lookup"><span data-stu-id="92771-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span>

<span data-ttu-id="92771-110">`condition value`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="92771-110">`condition value`: *String*</span></span>

<span data-ttu-id="92771-111">القيمة التي يتم إرجاعها بواسطة التعبير الذي تم تكوينه في خاصية **قيمة مفتاح البيانات المُجمعة** لمكون تنسيق ER.</span><span class="sxs-lookup"><span data-stu-id="92771-111">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span>

## <a name="return-values"></a><span data-ttu-id="92771-112">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="92771-112">Return values</span></span>

<span data-ttu-id="92771-113">*عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="92771-113">*Integer*</span></span>

<span data-ttu-id="92771-114">القيمة العددية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="92771-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="92771-115">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="92771-115">Usage notes</span></span>

<span data-ttu-id="92771-116">يُمكن تكوين خصائص **اسم مفتاح البيانات المُجمّعة** و **قيمة مفتاح البيانات المُجمعة** لكل من مكون **التسلسل** أو مكون **عنصر XML** لتنسيق ER الذي يوجد ضمن مكون **ملف\\شائع** حيث يتم تشغيل خيار **تجميع تفاصيل المُخرجات**.</span><span class="sxs-lookup"><span data-stu-id="92771-116">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="92771-117">تُرجع هذه الوظيفة قيمة **0** (صفر) عندما يتوقف تشغيل خيار **تجميع تفاصيل المُخرجات** لمكون **ملف\\شائع**.</span><span class="sxs-lookup"><span data-stu-id="92771-117">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="92771-118">في الوسيطة `condition range` ، يُمكن استخدام حرف البدل **"\*"** لتمثيل أي أحرف متعددة.</span><span class="sxs-lookup"><span data-stu-id="92771-118">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="92771-119">في الوسيطة `condition value` ، يُمكن استخدام حرف البدل **"\*"** لتمثيل أي أحرف متعددة.</span><span class="sxs-lookup"><span data-stu-id="92771-119">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="92771-120">مثال</span><span class="sxs-lookup"><span data-stu-id="92771-120">Example</span></span>

<span data-ttu-id="92771-121">لمزيد من المعلومات حول كيفية استخدام هذه الوظيفة، راجع دليل المهام [التقارير الإلكترونية - استخدام بيانات مخرجات التنسيق لعمليات الجرد والتجميع](tasks/er-format-counting-summing-1.md) جزء من عملية الأعمال **اكتساب/تطوير خدمة تكنولوجيا المعلومات/مكونات الحلول**.</span><span class="sxs-lookup"><span data-stu-id="92771-121">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="92771-122">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="92771-122">Additional resources</span></span>

[<span data-ttu-id="92771-123">وظائف تجميع البيانات</span><span class="sxs-lookup"><span data-stu-id="92771-123">Data collection functions</span></span>](er-functions-category-data-collection.md)
