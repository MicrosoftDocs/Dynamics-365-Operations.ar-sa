---
title: DAYS ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية DAYS (ER).
author: NickSelin
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
ms.openlocfilehash: 310359a29a506d69d1f34aaa710a82b0f2ea528e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746881"
---
# <a name="days-er-function"></a><span data-ttu-id="8ef88-103">DAYS ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="8ef88-103">DAYS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ef88-104">تُرجع الوظيفة `DAYS` قيمة *عدد صحيح* تمثل عدد الأيام بين التاريخ المُحدد الأول والتاريخ المُحدد الثاني.</span><span class="sxs-lookup"><span data-stu-id="8ef88-104">The `DAYS` function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ef88-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="8ef88-105">Syntax</span></span>

```vb
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a><span data-ttu-id="8ef88-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="8ef88-106">Arguments</span></span>

<span data-ttu-id="8ef88-107">`date 1`: *التاريخ*</span><span class="sxs-lookup"><span data-stu-id="8ef88-107">`date 1`: *Date*</span></span>

<span data-ttu-id="8ef88-108">قيمة التاريخ التي تمثل تاريخ البدء لحساب عدد الأيام.</span><span class="sxs-lookup"><span data-stu-id="8ef88-108">A date value that represents the start date for the calculation of the number of days.</span></span>

<span data-ttu-id="8ef88-109">`date 2`: *التاريخ*</span><span class="sxs-lookup"><span data-stu-id="8ef88-109">`date 2`: *Date*</span></span>

<span data-ttu-id="8ef88-110">قيمة التاريخ التي تمثل تاريخ النهاية لحساب عدد الأيام.</span><span class="sxs-lookup"><span data-stu-id="8ef88-110">A date value that represents the end date for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="8ef88-111">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="8ef88-111">Return values</span></span>

<span data-ttu-id="8ef88-112">*عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="8ef88-112">*Integer*</span></span>

<span data-ttu-id="8ef88-113">القيمة العددية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="8ef88-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8ef88-114">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="8ef88-114">Usage notes</span></span>

<span data-ttu-id="8ef88-115">تُرجع الوظيفة `DAYS` قيمة موجبه عندما يكون التاريخ الأول لاحقًا للتاريخ الثاني ، وتُرجع **0** (صفر) عندما يساوي التاريخ الأول التاريخ الثاني، ويُرجع قيمة سالبة عندما يكون التاريخ الأول سابقًا للتاريخ الثاني.</span><span class="sxs-lookup"><span data-stu-id="8ef88-115">The `DAYS` function returns a positive value when the first date is later than the second date, it returns **0** (zero) when the first date equals the second date, and it returns a negative value when the first date is earlier than the second date.</span></span>

## <a name="example"></a><span data-ttu-id="8ef88-116">مثال</span><span class="sxs-lookup"><span data-stu-id="8ef88-116">Example</span></span>

<span data-ttu-id="8ef88-117">يُرجع التعبير `DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` **-1**.</span><span class="sxs-lookup"><span data-stu-id="8ef88-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` returns **-1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8ef88-118">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="8ef88-118">Additional resources</span></span>

[<span data-ttu-id="8ef88-119">دلات التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="8ef88-119">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]