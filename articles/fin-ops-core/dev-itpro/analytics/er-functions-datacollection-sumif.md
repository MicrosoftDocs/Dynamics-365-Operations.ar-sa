---
title: وظيفة SUMIF ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني SUMIF (ER).
author: NickSelin
ms.date: 04/27/2020
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
ms.openlocfilehash: 60cf85ac0ffcdb163c12670efa3dcc7e9f05cb16
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747097"
---
# <a name="sumif-er-function"></a><span data-ttu-id="fd44c-103">وظيفة SUMIF ER</span><span class="sxs-lookup"><span data-stu-id="fd44c-103">SUMIF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fd44c-104">تُرجع الوظيفة `SUMIF` قيمة *حقيقية* الذي يمثل مجموع القيم التي تم إرجاعها بواسطة روابط عناصر التنسيق والتي تم جمعها عند استخدام عناصر التنسيق لإنشاء مستند صادر أثناء تشغيل التنسيق، والتي تفي بالشرط المحدد.</span><span class="sxs-lookup"><span data-stu-id="fd44c-104">The `SUMIF` function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="fd44c-105">يتكون الشرط من نطاق المفتاح وقيمة المفتاح.</span><span class="sxs-lookup"><span data-stu-id="fd44c-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd44c-106">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="fd44c-106">Syntax</span></span>

```vb
SUMIF (key name for summing, condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="fd44c-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="fd44c-107">Arguments</span></span>

<span data-ttu-id="fd44c-108">`key name for summing`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="fd44c-108">`key name for summing`: *String*</span></span>

<span data-ttu-id="fd44c-109">القيمة التي يتم إرجاعها بواسطة التعبير الذي تم تكوينه في خاصية **اسم مفتاح البيانات المُجمعة** لمكون تنسيق التقارير الإلكترونية (ER) الذي يجب استخدام قيمة الربط لأغراض التجميع.</span><span class="sxs-lookup"><span data-stu-id="fd44c-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of the Electronic reporting (ER) format component for which the value of the binding must be used for summing purposes.</span></span>

<span data-ttu-id="fd44c-110">يُمكن تكوين خاصية **اسم مفتاح البيانات المُجمّعة** لكل من مكون **التسلسل** أو مكون **عنصر XML** لتنسيق ER الذي يوجد ضمن مكون **ملف\\شائع** حيث يتم تشغيل خيار **تجميع تفاصيل المُخرجات**.</span><span class="sxs-lookup"><span data-stu-id="fd44c-110">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="return-values"></a><span data-ttu-id="fd44c-111">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="fd44c-111">Return values</span></span>

<span data-ttu-id="fd44c-112">*حقيقي*</span><span class="sxs-lookup"><span data-stu-id="fd44c-112">*Real*</span></span>

<span data-ttu-id="fd44c-113">القيمة العددية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="fd44c-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="fd44c-114">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="fd44c-114">Usage notes</span></span>

<span data-ttu-id="fd44c-115">تُرجع هذه الوظيفة قيمة **0** (صفر) عندما يتوقف تشغيل خيار **تجميع تفاصيل المُخرجات** لمكون **ملف\\شائع**.</span><span class="sxs-lookup"><span data-stu-id="fd44c-115">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="fd44c-116">في الوسيطة `condition range` ، يُمكن استخدام حرف البدل **"\*"** لتمثيل أي أحرف متعددة.</span><span class="sxs-lookup"><span data-stu-id="fd44c-116">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="fd44c-117">في الوسيطة `condition value` ، يُمكن استخدام حرف البدل **"\*"** لتمثيل أي أحرف متعددة.</span><span class="sxs-lookup"><span data-stu-id="fd44c-117">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="fd44c-118">مثال</span><span class="sxs-lookup"><span data-stu-id="fd44c-118">Example</span></span>

<span data-ttu-id="fd44c-119">لمزيد من المعلومات حول كيفية استخدام هذه الوظيفة، راجع دليل المهام [التقارير الإلكترونية - استخدام بيانات مخرجات التنسيق لعمليات الجرد والتجميع](tasks/er-format-counting-summing-1.md) جزء من عملية الأعمال **اكتساب/تطوير خدمة تكنولوجيا المعلومات/مكونات الحلول**.</span><span class="sxs-lookup"><span data-stu-id="fd44c-119">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

<span data-ttu-id="fd44c-120">لمزيد من المعلومات والأمثلة حول استخدام هذه الوظيفة، راجع [تأجيل تنفيذ عناصر التسلسل في تنسيقات إعداد التقارير الإلكترونية](er-defer-sequence-element.md#Example) و [‏‫تأجيل تنفيذ عناصر XML في تنسيقات إعداد التقارير الإلكترونية‬](er-defer-xml-element.md#Example).</span><span class="sxs-lookup"><span data-stu-id="fd44c-120">For more information and examples about using this function, see [Defer the execution of sequence elements in ER formats](er-defer-sequence-element.md#Example) and [Defer the execution of XML elements in ER formats](er-defer-xml-element.md#Example).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fd44c-121">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="fd44c-121">Additional resources</span></span>

[<span data-ttu-id="fd44c-122">وظائف تجميع البيانات</span><span class="sxs-lookup"><span data-stu-id="fd44c-122">Data collection functions</span></span>](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]