---
title: وظيفة JSONVALUE ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة JSONVALUE ER.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: d8209f8ce9d244ab7c82f897e4f59283e94e0522
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915661"
---
# <span data-ttu-id="c860d-103"><a name="JSONVALUE">وظيفة JSONVALUE ER</a></span><span class="sxs-lookup"><span data-stu-id="c860d-103"><a name="JSONVALUE">JSONVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c860d-104">تُحلل وظيفة `JSONVALUE` البيانات في تنسيق JavaScript Object Notation (JSON) الذي يتم الوصول إليه في المسار المُحدد، ويستخرج قيمة عددية تعتمد على المعرف المحدد.‬</span><span class="sxs-lookup"><span data-stu-id="c860d-104">The `JSONVALUE` function parses data in JavaScript Object Notation (JSON) format that is accessed at the specified path, and it extracts a scalar value that has the specified ID.</span></span> <span data-ttu-id="c860d-105">ثم يقوم بإرجاع القيمة العددية المستخرجة كقيمة *سلسلة* .</span><span class="sxs-lookup"><span data-stu-id="c860d-105">It then returns the extracted scalar value as a *String* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="c860d-106">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="c860d-106">Syntax</span></span>

```
JSONVALUE (input, path)
```

## <a name="arguments"></a><span data-ttu-id="c860d-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="c860d-107">Arguments</span></span>

<span data-ttu-id="c860d-108">`input`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="c860d-108">`input`: *String*</span></span>

<span data-ttu-id="c860d-109">المسار الصالح لمصدر البيانات من نوع *السلسلة* الذي يحتوي على بيانات JSON.</span><span class="sxs-lookup"><span data-stu-id="c860d-109">The valid path of a data source of the *String* type that contains JSON data.</span></span>

<span data-ttu-id="c860d-110">`path`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="c860d-110">`path`: *String*</span></span>

<span data-ttu-id="c860d-111">معرف نوع القيمة العددية لبيانات JSON.</span><span class="sxs-lookup"><span data-stu-id="c860d-111">The identifier of a scalar value of JSON data.</span></span>

## <a name="return-values"></a><span data-ttu-id="c860d-112">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="c860d-112">Return values</span></span>

<span data-ttu-id="c860d-113">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="c860d-113">*String*</span></span>

<span data-ttu-id="c860d-114">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="c860d-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="c860d-115">مثال</span><span class="sxs-lookup"><span data-stu-id="c860d-115">Example</span></span>

<span data-ttu-id="c860d-116">يحتوي مصدر البيانات **JsonField** على البيانات التالية بتنسيق: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span><span class="sxs-lookup"><span data-stu-id="c860d-116">The **JsonField** data source contains the following data in JSON format: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span></span> <span data-ttu-id="c860d-117">في هذه الحالة، يقوم التعبير `JSONVALUE (JsonField, "BuildNumber")` بإرجاع القيمة التالية من نوع البيانات *سلسلة* : **"7.3.1234.1"**.</span><span class="sxs-lookup"><span data-stu-id="c860d-117">In this case, the expression `JSONVALUE (JsonField, "BuildNumber")` returns the following value of the *String* data type: **"7.3.1234.1"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c860d-118">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="c860d-118">Additional resources</span></span>

[<span data-ttu-id="c860d-119">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="c860d-119">Text functions</span></span>](er-functions-category-text.md)
