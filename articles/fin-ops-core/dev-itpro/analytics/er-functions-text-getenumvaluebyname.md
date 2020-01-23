---
title: 'وظيفة GETENUMVALUEBYNAME ER '
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني GETENUMVALUEBYNAME (ER).
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 4ded0c62b4556b21e731cd9b98db2863ec6ec442
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916834"
---
# <span data-ttu-id="84703-103"><a name="GETENUMVALUEBYNAME">وظيفة GETENUMVALUEBYNAME ER</a></span><span class="sxs-lookup"><span data-stu-id="84703-103"><a name="GETENUMVALUEBYNAME">GETENUMVALUEBYNAME ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="84703-104">تبحث وظيفة `GETENUMVALUEBYNAME` عن قيمة *Enum* مُحددة في مصدر بيانات التعداد المُحدد باستخدام اسم التعداد المُحدد كقيمة *السلسلة* .</span><span class="sxs-lookup"><span data-stu-id="84703-104">The `GETENUMVALUEBYNAME` function searches for a specific *Enum* value in the specified enumeration data source by using the enumeration name that is specified as a *String* value.</span></span> <span data-ttu-id="84703-105">إذا تم العثور على قيمة *تعداد* ، تقوم الوظيفة بإرجاعها.</span><span class="sxs-lookup"><span data-stu-id="84703-105">If the *Enum* value is found, the function returns it.</span></span> <span data-ttu-id="84703-106">وإلا، تقوم الوظيفة بإرجاع قيمه التعداد **null**.</span><span class="sxs-lookup"><span data-stu-id="84703-106">Otherwise, the function returns the **null** enumeration value.</span></span>

## <a name="syntax"></a><span data-ttu-id="84703-107">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="84703-107">Syntax</span></span>

```
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a><span data-ttu-id="84703-108">الوسائط</span><span class="sxs-lookup"><span data-stu-id="84703-108">Arguments</span></span>

<span data-ttu-id="84703-109">`enumeration data source path`: *تعداد*</span><span class="sxs-lookup"><span data-stu-id="84703-109">`enumeration data source path`: *Enumeration*</span></span>

<span data-ttu-id="84703-110">مسار مرجع صالح لمصدر بيانات أحد أنواع التعداد التالية:</span><span class="sxs-lookup"><span data-stu-id="84703-110">The valid path of a data source of one of the following enumeration types:</span></span>

- <span data-ttu-id="84703-111">تعداد نموذج إعداد التقارير الإلكترونية (ER)</span><span class="sxs-lookup"><span data-stu-id="84703-111">Electronic reporting (ER) model enumeration</span></span>
- <span data-ttu-id="84703-112">تعداد تنسيق إعداد التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="84703-112">ER format enumeration</span></span>
- <span data-ttu-id="84703-113">تعداد Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="84703-113">Microsoft Dynamics 365 Finance enumeration</span></span>

<span data-ttu-id="84703-114">`enumeration value text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="84703-114">`enumeration value text`: *String*</span></span>

<span data-ttu-id="84703-115">قيمة سلسلة تمثل اسم قيمة تعداد مُفرد.</span><span class="sxs-lookup"><span data-stu-id="84703-115">A string value that represents the name of a single enumeration value.</span></span>

## <a name="return-values"></a><span data-ttu-id="84703-116">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="84703-116">Return values</span></span>

<span data-ttu-id="84703-117">‏‫قابل للإبطال *Enum*</span><span class="sxs-lookup"><span data-stu-id="84703-117">Nullable *Enum*</span></span>

<span data-ttu-id="84703-118">قيمة التعداد الناتجة.</span><span class="sxs-lookup"><span data-stu-id="84703-118">The resulting enumeration value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="84703-119">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="84703-119">Usage notes</span></span>

<span data-ttu-id="84703-120">لا يتم طرح أي استثناء إذا لم يتم العثور على قيمة *Enum* باستخدام اسم قيمة التعداد المحدد كقيمة *سلسلة* .</span><span class="sxs-lookup"><span data-stu-id="84703-120">No exception is thrown if an *Enum* value isn't found by using the name of the enumeration value that is specified as a *String* value.</span></span>

## <a name="example"></a><span data-ttu-id="84703-121">مثال</span><span class="sxs-lookup"><span data-stu-id="84703-121">Example</span></span>

<span data-ttu-id="84703-122">في الرسم التوضيحي التالي، يتم تقديم تعداد **ReportDirection** في نموذج بيانات.</span><span class="sxs-lookup"><span data-stu-id="84703-122">In the following illustration, the **ReportDirection** enumeration is introduced in a data model.</span></span> <span data-ttu-id="84703-123">لاحظ أنه يتم تحديد التسميات لقيم التعداد.</span><span class="sxs-lookup"><span data-stu-id="84703-123">Notice that labels are defined for the enumeration values.</span></span>

<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for a data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="84703-124">يبين الرسم التوضيحي التالي هذه التفاصيل:</span><span class="sxs-lookup"><span data-stu-id="84703-124">The following illustration shows these details:</span></span>

- <span data-ttu-id="84703-125">يتم تكوين مصدر البيانات **$Direction** في تقرير التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="84703-125">The **$Direction** data source is configured in an ER report.</span></span> <span data-ttu-id="84703-126">يتم تكوين مصدر البيانات هذا استنادًا إلى تعداد نموذج **ReportDirection**.</span><span class="sxs-lookup"><span data-stu-id="84703-126">This data source is configured based on the **ReportDirection** model enumeration.</span></span>
- <span data-ttu-id="84703-127">تم تصميم التعبير `$IsArrivals` ليستخدم مصدر بيانات **$Direction** المستند إلى تعداد النموذج تعداد النموذج كمعلمة لهذه الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="84703-127">The `$IsArrivals` expression is designed to use the model enumeration–based **$Direction** data source as a parameter of this function.</span></span>
- <span data-ttu-id="84703-128">قيمة تعبير المقارنة هذا هي **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="84703-128">The value of this comparison expression is **TRUE**.</span></span>

<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

## <a name="additional-resources"></a><span data-ttu-id="84703-129">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="84703-129">Additional resources</span></span>

[<span data-ttu-id="84703-130">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="84703-130">Text functions</span></span>](er-functions-category-text.md)
