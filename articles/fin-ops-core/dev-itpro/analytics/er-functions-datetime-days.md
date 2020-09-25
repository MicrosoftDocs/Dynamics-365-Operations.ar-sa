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
ms.openlocfilehash: 47d992d061f8664a55332024ee5c6cd41e4bc495
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743557"
---
# <a name="days-er-function"></a><span data-ttu-id="c19ce-103">DAYS ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="c19ce-103">DAYS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c19ce-104">تُرجع الوظيفة `DAYS` قيمة *عدد صحيح* تمثل عدد الأيام بين التاريخ المُحدد الأول والتاريخ المُحدد الثاني.</span><span class="sxs-lookup"><span data-stu-id="c19ce-104">The `DAYS` function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="c19ce-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="c19ce-105">Syntax</span></span>

```vb
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a><span data-ttu-id="c19ce-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="c19ce-106">Arguments</span></span>

<span data-ttu-id="c19ce-107">`date 1`: *التاريخ*</span><span class="sxs-lookup"><span data-stu-id="c19ce-107">`date 1`: *Date*</span></span>

<span data-ttu-id="c19ce-108">قيمة التاريخ التي تمثل تاريخ البدء لحساب عدد الأيام.</span><span class="sxs-lookup"><span data-stu-id="c19ce-108">A date value that represents the start date for the calculation of the number of days.</span></span>

<span data-ttu-id="c19ce-109">`date 2`: *التاريخ*</span><span class="sxs-lookup"><span data-stu-id="c19ce-109">`date 2`: *Date*</span></span>

<span data-ttu-id="c19ce-110">قيمة التاريخ التي تمثل تاريخ النهاية لحساب عدد الأيام.</span><span class="sxs-lookup"><span data-stu-id="c19ce-110">A date value that represents the end date for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="c19ce-111">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="c19ce-111">Return values</span></span>

<span data-ttu-id="c19ce-112">*عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="c19ce-112">*Integer*</span></span>

<span data-ttu-id="c19ce-113">القيمة العددية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="c19ce-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c19ce-114">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="c19ce-114">Usage notes</span></span>

<span data-ttu-id="c19ce-115">تُرجع الوظيفة `DAYS` قيمة موجبه عندما يكون التاريخ الأول لاحقًا للتاريخ الثاني ، وتُرجع **0** (صفر) عندما يساوي التاريخ الأول التاريخ الثاني، ويُرجع قيمة سالبة عندما يكون التاريخ الأول سابقًا للتاريخ الثاني.</span><span class="sxs-lookup"><span data-stu-id="c19ce-115">The `DAYS` function returns a positive value when the first date is later than the second date, it returns **0** (zero) when the first date equals the second date, and it returns a negative value when the first date is earlier than the second date.</span></span>

## <a name="example"></a><span data-ttu-id="c19ce-116">مثال</span><span class="sxs-lookup"><span data-stu-id="c19ce-116">Example</span></span>

<span data-ttu-id="c19ce-117">يُرجع التعبير `DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` **-1**.</span><span class="sxs-lookup"><span data-stu-id="c19ce-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` returns **-1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c19ce-118">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="c19ce-118">Additional resources</span></span>

[<span data-ttu-id="c19ce-119">دلات التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="c19ce-119">Date and time functions</span></span>](er-functions-category-datetime.md)
