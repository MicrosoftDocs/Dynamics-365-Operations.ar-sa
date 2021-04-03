---
title: وظيفة DATETODATETIME ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية DATETODATETIME (ER).
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: d30fdc9c7b6f277b8712b733cabdb0552db2a748
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563572"
---
# <a name="datetodatetime-er-function"></a><span data-ttu-id="aaddb-103">وظيفة DATETODATETIME ER</span><span class="sxs-lookup"><span data-stu-id="aaddb-103">DATETODATETIME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aaddb-104">تُرجع الوظيفة `DATETODATETIME` قيمة *DateTime* يتم تحويلها من قيمة تاريخ مُعين إلى قيمة تاريخ/وقت بالتوقيت العالمي المنسق (توقيت جرينتش المتوسط \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="aaddb-104">The `DATETODATETIME` function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span>

## <a name="syntax"></a><span data-ttu-id="aaddb-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="aaddb-105">Syntax</span></span>

```vb
DATETODATETIME (date)
```

## <a name="arguments"></a><span data-ttu-id="aaddb-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="aaddb-106">Arguments</span></span>

<span data-ttu-id="aaddb-107">`date`: *التاريخ*</span><span class="sxs-lookup"><span data-stu-id="aaddb-107">`date`: *Date*</span></span>

<span data-ttu-id="aaddb-108">قيمة التاريخ التي تمثل التاريخ المُراد تحويله.</span><span class="sxs-lookup"><span data-stu-id="aaddb-108">A date value that represents the date to convert.</span></span>

## <a name="return-values"></a><span data-ttu-id="aaddb-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="aaddb-109">Return values</span></span>

<span data-ttu-id="aaddb-110">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="aaddb-110">*DateTime*</span></span>

<span data-ttu-id="aaddb-111">قيمة التاريخ/الوقت الناتجة.</span><span class="sxs-lookup"><span data-stu-id="aaddb-111">The resulting date/time value.</span></span>

## <a name="example-1"></a><span data-ttu-id="aaddb-112">مثال1</span><span class="sxs-lookup"><span data-stu-id="aaddb-112">Example 1</span></span>

<span data-ttu-id="aaddb-113">يُرجع `DATETODATETIME (CompInfo. 'getCurrentDate()')` تاريخ جلسة Microsoft Dynamics 365 Finance الحالية، 24 ديسمبر 2015، على الشكل التالي **12/24/2015 12:00:00 AM**. </span><span class="sxs-lookup"><span data-stu-id="aaddb-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` returns the date of the current Microsoft Dynamics 365 Finance session, December 24, 2015, as **12/24/2015 12:00:00 AM**.</span></span> <span data-ttu-id="aaddb-114">في هذا المثال، **CompInfo** عبارة عن مصدر بيانات تقارير إلكترونية (ER) من النوع **Finance and Operations/جدول**، ويشير إلى جدول CompanyInfo table.</span><span class="sxs-lookup"><span data-stu-id="aaddb-114">In this example, **CompInfo** is an Electronic reporting (ER) data source of the **Finance and Operations/Table** type, and it refers to the CompanyInfo table.</span></span>

## <a name="example-2"></a><span data-ttu-id="aaddb-115">مثال2</span><span class="sxs-lookup"><span data-stu-id="aaddb-115">Example 2</span></span>

<span data-ttu-id="aaddb-116">يُرجع `DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` قيمة التاريخ/الوقت **11/12/2019 12:00:00 AM**. </span><span class="sxs-lookup"><span data-stu-id="aaddb-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` returns the date/time value **11/12/2019 12:00:00 AM**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aaddb-117">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="aaddb-117">Additional resources</span></span>

[<span data-ttu-id="aaddb-118">دلات التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="aaddb-118">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]