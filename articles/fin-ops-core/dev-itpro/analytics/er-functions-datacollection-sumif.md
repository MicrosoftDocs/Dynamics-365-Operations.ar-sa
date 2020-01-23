---
title: وظيفة SUMIF ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني SUMIF (ER).
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 579b14c713bc5f9831c5e012d16bb3b6f97b1035
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916420"
---
# <span data-ttu-id="e66ed-103"><a name="SUMIF">وظيفة SUMIF ER</a></span><span class="sxs-lookup"><span data-stu-id="e66ed-103"><a name="SUMIF">SUMIF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e66ed-104">تُرجع الوظيفة `SUMIF` قيمة *حقيقية* الذي يمثل مجموع القيم التي تم إرجاعها بواسطة روابط عناصر التنسيق والتي تم جمعها عند استخدام عناصر التنسيق لإنشاء مستند صادر أثناء تشغيل التنسيق، والتي تفي بالشرط المحدد.</span><span class="sxs-lookup"><span data-stu-id="e66ed-104">The `SUMIF` function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="e66ed-105">يتكون الشرط من نطاق المفتاح وقيمة المفتاح.</span><span class="sxs-lookup"><span data-stu-id="e66ed-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e66ed-106">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="e66ed-106">Syntax</span></span>

```
SUMIF (key name for summing, condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="e66ed-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="e66ed-107">Arguments</span></span>

<span data-ttu-id="e66ed-108">`key name for summing`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="e66ed-108">`key name for summing`: *String*</span></span>

<span data-ttu-id="e66ed-109">القيمة التي يتم إرجاعها بواسطة التعبير الذي تم تكوينه في خاصية **اسم مفتاح البيانات المُجمعة** لمكون تنسيق التقارير الإلكترونية (ER) الذي يجب استخدام قيمة الربط لأغراض التجميع.</span><span class="sxs-lookup"><span data-stu-id="e66ed-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of the Electronic reporting (ER) format component for which the value of the binding must be used for summing purposes.</span></span>

<span data-ttu-id="e66ed-110">يُمكن تكوين خاصية **اسم مفتاح البيانات المُجمّعة** لكل من مكون **التسلسل** أو مكون **عنصر XML** لتنسيق ER الذي يوجد ضمن مكون **ملف\\شائع** حيث يتم تشغيل خيار **تجميع تفاصيل المُخرجات**.</span><span class="sxs-lookup"><span data-stu-id="e66ed-110">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="return-values"></a><span data-ttu-id="e66ed-111">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="e66ed-111">Return values</span></span>

<span data-ttu-id="e66ed-112">*حقيقي*</span><span class="sxs-lookup"><span data-stu-id="e66ed-112">*Real*</span></span>

<span data-ttu-id="e66ed-113">القيمة العددية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="e66ed-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e66ed-114">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="e66ed-114">Usage notes</span></span>

<span data-ttu-id="e66ed-115">تُرجع هذه الوظيفة قيمة **0** (صفر) عندما يتوقف تشغيل خيار **تجميع تفاصيل المُخرجات** لمكون **ملف\\شائع**.</span><span class="sxs-lookup"><span data-stu-id="e66ed-115">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="e66ed-116">في الوسيطة `condition range` ، يُمكن استخدام حرف البدل **"\*"** لتمثيل أي أحرف متعددة.</span><span class="sxs-lookup"><span data-stu-id="e66ed-116">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="e66ed-117">في الوسيطة `condition value` ، يُمكن استخدام حرف البدل **"\*"** لتمثيل أي أحرف متعددة.</span><span class="sxs-lookup"><span data-stu-id="e66ed-117">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="e66ed-118">مثال</span><span class="sxs-lookup"><span data-stu-id="e66ed-118">Example</span></span>

<span data-ttu-id="e66ed-119">لمزيد من المعلومات حول كيفية استخدام هذه الوظيفة، راجع دليل المهام [التقارير الإلكترونية - استخدام بيانات مخرجات التنسيق لعمليات الجرد والتجميع](tasks/er-format-counting-summing-1.md) جزء من عملية الأعمال **اكتساب/تطوير خدمة تكنولوجيا المعلومات/مكونات الحلول**.</span><span class="sxs-lookup"><span data-stu-id="e66ed-119">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e66ed-120">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="e66ed-120">Additional resources</span></span>

[<span data-ttu-id="e66ed-121">وظائف تجميع البيانات</span><span class="sxs-lookup"><span data-stu-id="e66ed-121">Data collection functions</span></span>](er-functions-category-data-collection.md)
