---
title: DAYS ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية DAYS (ER).
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
ms.openlocfilehash: 4f8c12a22f7654285d5598064473bf86689ed207
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916282"
---
# <span data-ttu-id="7d3d4-103"><a name="DAYS">DAYS ER وظيفة</a></span><span class="sxs-lookup"><span data-stu-id="7d3d4-103"><a name="DAYS">DAYS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7d3d4-104">تُرجع الوظيفة `DAYS` قيمة *عدد صحيح* تمثل عدد الأيام بين التاريخ المُحدد الأول والتاريخ المُحدد الثاني.</span><span class="sxs-lookup"><span data-stu-id="7d3d4-104">The `DAYS` function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d3d4-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="7d3d4-105">Syntax</span></span>

```
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a><span data-ttu-id="7d3d4-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="7d3d4-106">Arguments</span></span>

<span data-ttu-id="7d3d4-107">`date 1`: *التاريخ*</span><span class="sxs-lookup"><span data-stu-id="7d3d4-107">`date 1`: *Date*</span></span>

<span data-ttu-id="7d3d4-108">قيمة التاريخ التي تمثل تاريخ البدء لحساب عدد الأيام.</span><span class="sxs-lookup"><span data-stu-id="7d3d4-108">A date value that represents the start date for the calculation of the number of days.</span></span>

<span data-ttu-id="7d3d4-109">`date 2`: *التاريخ*</span><span class="sxs-lookup"><span data-stu-id="7d3d4-109">`date 2`: *Date*</span></span>

<span data-ttu-id="7d3d4-110">قيمة التاريخ التي تمثل تاريخ النهاية لحساب عدد الأيام.</span><span class="sxs-lookup"><span data-stu-id="7d3d4-110">A date value that represents the end date for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="7d3d4-111">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="7d3d4-111">Return values</span></span>

<span data-ttu-id="7d3d4-112">*عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="7d3d4-112">*Integer*</span></span>

<span data-ttu-id="7d3d4-113">القيمة العددية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="7d3d4-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="7d3d4-114">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="7d3d4-114">Usage notes</span></span>

<span data-ttu-id="7d3d4-115">تُرجع الوظيفة `DAYS` قيمة موجبه عندما يكون التاريخ الأول لاحقًا للتاريخ الثاني ، وتُرجع **0** (صفر) عندما يساوي التاريخ الأول التاريخ الثاني، ويُرجع قيمة سالبة عندما يكون التاريخ الأول سابقًا للتاريخ الثاني.</span><span class="sxs-lookup"><span data-stu-id="7d3d4-115">The `DAYS` function returns a positive value when the first date is later than the second date, it returns **0** (zero) when the first date equals the second date, and it returns a negative value when the first date is earlier than the second date.</span></span>

## <a name="example"></a><span data-ttu-id="7d3d4-116">مثال</span><span class="sxs-lookup"><span data-stu-id="7d3d4-116">Example</span></span>

<span data-ttu-id="7d3d4-117">يُرجع التعبير `DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` **-1**.</span><span class="sxs-lookup"><span data-stu-id="7d3d4-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` returns **-1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7d3d4-118">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="7d3d4-118">Additional resources</span></span>

[<span data-ttu-id="7d3d4-119">دلات التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="7d3d4-119">Date and time functions</span></span>](er-functions-category-datetime.md)
