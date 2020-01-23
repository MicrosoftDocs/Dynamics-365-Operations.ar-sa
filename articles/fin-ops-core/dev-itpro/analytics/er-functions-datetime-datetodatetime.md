---
title: وظيفة DATETODATETIME ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية DATETODATETIME (ER).
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
ms.openlocfilehash: f9ce977b36cd96a27a228dba1bc8c8445bafd879
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916374"
---
# <span data-ttu-id="66a48-103"><a name="DATETODATETIME">وظيفة DATETODATETIME ER</a></span><span class="sxs-lookup"><span data-stu-id="66a48-103"><a name="DATETODATETIME">DATETODATETIME ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="66a48-104">تُرجع الوظيفة `DATETODATETIME` قيمة *DateTime* يتم تحويلها من قيمة تاريخ مُعين إلى قيمة تاريخ/وقت بالتوقيت العالمي المنسق (توقيت جرينتش المتوسط \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="66a48-104">The `DATETODATETIME` function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span>

## <a name="syntax"></a><span data-ttu-id="66a48-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="66a48-105">Syntax</span></span>

```
DATETODATETIME (date)
```

## <a name="arguments"></a><span data-ttu-id="66a48-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="66a48-106">Arguments</span></span>

<span data-ttu-id="66a48-107">`date`: *التاريخ*</span><span class="sxs-lookup"><span data-stu-id="66a48-107">`date`: *Date*</span></span>

<span data-ttu-id="66a48-108">قيمة التاريخ التي تمثل التاريخ المُراد تحويله.</span><span class="sxs-lookup"><span data-stu-id="66a48-108">A date value that represents the date to convert.</span></span>

## <a name="return-values"></a><span data-ttu-id="66a48-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="66a48-109">Return values</span></span>

<span data-ttu-id="66a48-110">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="66a48-110">*DateTime*</span></span>

<span data-ttu-id="66a48-111">قيمة التاريخ/الوقت الناتجة.</span><span class="sxs-lookup"><span data-stu-id="66a48-111">The resulting date/time value.</span></span>

## <a name="example-1"></a><span data-ttu-id="66a48-112">مثال1</span><span class="sxs-lookup"><span data-stu-id="66a48-112">Example 1</span></span>

<span data-ttu-id="66a48-113">يُرجع `DATETODATETIME (CompInfo. 'getCurrentDate()')` تاريخ جلسة Microsoft Dynamics 365 Finance الحالية، 24 ديسمبر 2015، على الشكل التالي **12/24/2015 12:00:00 AM**. </span><span class="sxs-lookup"><span data-stu-id="66a48-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` returns the date of the current Microsoft Dynamics 365 Finance session, December 24, 2015, as **12/24/2015 12:00:00 AM**.</span></span> <span data-ttu-id="66a48-114">في هذا المثال، **CompInfo** عبارة عن مصدر بيانات تقارير إلكترونية (ER) من النوع **Finance and Operations/جدول** ، ويشير إلى جدول CompanyInfo.</span><span class="sxs-lookup"><span data-stu-id="66a48-114">In this example, **CompInfo** is an Electronic reporting (ER) data source of the **Finance and Operations/Table** type, and it refers to the CompanyInfo table.</span></span>

## <a name="example-2"></a><span data-ttu-id="66a48-115">مثال2</span><span class="sxs-lookup"><span data-stu-id="66a48-115">Example 2</span></span>

<span data-ttu-id="66a48-116">يُرجع `DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` قيمة التاريخ/الوقت **11/12/2019 12:00:00 AM**. </span><span class="sxs-lookup"><span data-stu-id="66a48-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` returns the date/time value **11/12/2019 12:00:00 AM**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="66a48-117">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="66a48-117">Additional resources</span></span>

[<span data-ttu-id="66a48-118">دلات التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="66a48-118">Date and time functions</span></span>](er-functions-category-datetime.md)
