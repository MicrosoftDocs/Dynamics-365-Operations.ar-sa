---
title: قائمة وظائف التقارير الإلكترونية في فئة الحاوية
description: يوفر هذا الموضوع معلومات حول وظائف الحاوية المعتمدة في التقارير الإلكترونية (ER).
author: NickSelin
manager: kfend
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 46d1af85773f6c3d07865658c554dee74fae625f
ms.sourcegitcommit: e8a46e127d70986539c138b27a641bff6f6874d0
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/15/2020
ms.locfileid: "4739052"
---
# <a name="list-of-er-functions-in-the-container-category"></a><span data-ttu-id="b4311-103">قائمة وظائف التقارير الإلكترونية في فئة الحاوية</span><span class="sxs-lookup"><span data-stu-id="b4311-103">List of ER functions in the container category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b4311-104">يُمكن استخدام [وظائف](er-formula-language.md#functions) حاوية [التقارير الإلكترونية (ER)](general-electronic-reporting.md) لإجراء العمليات التي تتضمن مصادر البيانات من نوع البيانات *الحاوية*.</span><span class="sxs-lookup"><span data-stu-id="b4311-104">[Electronic reporting (ER)](general-electronic-reporting.md) container [functions](er-formula-language.md#functions) can be used to perform operations that involve data sources of the *Container* data type.</span></span> <span data-ttu-id="b4311-105">تحدث هذه العمليات عندما تمثل معالجه البيانات مجموعه من البيانات الثنائية بتنسيق الكائن الثنائي الكبير (BLOB).</span><span class="sxs-lookup"><span data-stu-id="b4311-105">These operations occur when the processing data represents a collection of binary data in binary large object (BLOB) format.</span></span> <span data-ttu-id="b4311-106">يعرض هذا الموضوع ملخصًا لهذه الوظائف.</span><span class="sxs-lookup"><span data-stu-id="b4311-106">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="b4311-107">قائمة الوظائف المدعومة</span><span class="sxs-lookup"><span data-stu-id="b4311-107">List of supported functions</span></span>

| <span data-ttu-id="b4311-108">الوظيفة</span><span class="sxs-lookup"><span data-stu-id="b4311-108">Function</span></span> | <span data-ttu-id="b4311-109">الوصف</span><span class="sxs-lookup"><span data-stu-id="b4311-109">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="b4311-110">Base64StringToContainer</span><span class="sxs-lookup"><span data-stu-id="b4311-110">Base64StringToContainer</span></span>](er-functions-container-base64stringtocontainer.md) | <span data-ttu-id="b4311-111">تقوم هذه الوظيفة بإرجاع القيمة *الحاوية* التي تتكون من المحتوي الثنائي الذي يتم فك ترميزه من سلسله ASCII المحددة التي تمثل مجموعه Base64 الخاصة بانظمه ترميز ثنائيه النص.</span><span class="sxs-lookup"><span data-stu-id="b4311-111">This function returns a *Container* value that consists of binary content that is decoded from the specified ASCII string that represents a Base64 group of binary-to-text encoding schemes.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="b4311-112">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="b4311-112">Additional resources</span></span>

[<span data-ttu-id="b4311-113">نظرة عامة حول التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="b4311-113">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="b4311-114">مصمم المعادلات في التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="b4311-114">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="b4311-115">لغة تركيبة التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="b4311-115">Electronic reporting formula language</span></span>](er-formula-language.md)
