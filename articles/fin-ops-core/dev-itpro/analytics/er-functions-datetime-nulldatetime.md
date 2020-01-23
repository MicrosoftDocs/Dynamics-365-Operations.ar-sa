---
title: NULLDATETIME ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني NULLDATETIME (ER).
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
ms.openlocfilehash: 4165f6e064d12200907ac76b6779d35bc578daba
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917478"
---
# <span data-ttu-id="cc201-103"><a name="NULLDATETIME">NULLDATETIME ER وظيفة</a></span><span class="sxs-lookup"><span data-stu-id="cc201-103"><a name="NULLDATETIME">NULLDATETIME ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cc201-104">تقوم وظيفة `NULLDATETIME` بإرجاع قيمة *DateTime* التي تظهر قيمة التاريخ/الوقت **الفارغة** (1 يناير 1900) بالتوقيت العالمي المتفق عليه (توقيت جرينتش المتوسط \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="cc201-104">The `NULLDATETIME` function returns a *DateTime* value that represents the **null** date/time value (January 1, 1900) in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span>

## <a name="syntax"></a><span data-ttu-id="cc201-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="cc201-105">Syntax</span></span>

```
NULLDATETIME ()
```

## <a name="return-values"></a><span data-ttu-id="cc201-106">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="cc201-106">Return values</span></span>

<span data-ttu-id="cc201-107">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="cc201-107">*DateTime*</span></span>

<span data-ttu-id="cc201-108">قيمة التاريخ/الوقت الناتجة.</span><span class="sxs-lookup"><span data-stu-id="cc201-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="cc201-109">مثال</span><span class="sxs-lookup"><span data-stu-id="cc201-109">Example</span></span>

<span data-ttu-id="cc201-110">تُرجع وظيفة `DATETIMEFORMAT( NULLDATETIME(), "O")` قيمة السلسلة **1900-01-01T00:00:00.0000000+00:00** عندما يتم استدعاءها أثناء عملية تم البدء فيها بواسطة مستخدم تطبيق لديه قيمة منطقة زمنية **‏‫التوقيت العالمي المتفق عليه (GMT)‬** في قسم **‏‫تفضيلات البلد/المنطقة واللغة‬**.</span><span class="sxs-lookup"><span data-stu-id="cc201-110">`DATETIMEFORMAT( NULLDATETIME(), "O")` returns the string value **1900-01-01T00:00:00.0000000+00:00** when it's called during a process that was initiated by an application user who has the time zone value **(GMT) Coordinated Universal Time** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cc201-111">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="cc201-111">Additional resources</span></span>

[<span data-ttu-id="cc201-112">دلات التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="cc201-112">Date and time functions</span></span>](er-functions-category-datetime.md)
