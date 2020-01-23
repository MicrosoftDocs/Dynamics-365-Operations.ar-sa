---
title: NULLDATE ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني NULLDATE (ER).
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
ms.openlocfilehash: 7761342c6759c11591e06fc7c32f0ddd8bef407a
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916305"
---
# <span data-ttu-id="938b8-103"><a name="NULLDATE">NULLDATE ER وظيفة</a></span><span class="sxs-lookup"><span data-stu-id="938b8-103"><a name="NULLDATE">NULLDATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="938b8-104">تُرجع وظيفة `NULLDATE` قيمة *تاريخ* يمثل التاريخ **الفارغ** (1 يناير 1900).</span><span class="sxs-lookup"><span data-stu-id="938b8-104">The `NULLDATE` function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span>

## <a name="syntax"></a><span data-ttu-id="938b8-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="938b8-105">Syntax</span></span>

```
NULLDATE () as 
```

## <a name="return-values"></a><span data-ttu-id="938b8-106">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="938b8-106">Return values</span></span>

<span data-ttu-id="938b8-107">*التاريخ*</span><span class="sxs-lookup"><span data-stu-id="938b8-107">*Date*</span></span>

<span data-ttu-id="938b8-108">قيمة التاريخ الناتجة.</span><span class="sxs-lookup"><span data-stu-id="938b8-108">The resulting date value.</span></span>

## <a name="example-1"></a><span data-ttu-id="938b8-109">مثال1</span><span class="sxs-lookup"><span data-stu-id="938b8-109">Example 1</span></span>

<span data-ttu-id="938b8-110">تُرجع وظيفة `DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` التاريخ **الفارغ**،1 يناير 1900 كـ **"1900-01-01"**، بناءً على التنسيق المخصص المُحدد.</span><span class="sxs-lookup"><span data-stu-id="938b8-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` returns the **null** date, January 1, 1900, as **"1900-01-01"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="938b8-111">مثال2</span><span class="sxs-lookup"><span data-stu-id="938b8-111">Example 2</span></span>

<span data-ttu-id="938b8-112">يُرجع التعبير `IF( Invoice.DocumentDate = NULLDATE(), true, false)` **True** عندما تكون قيمة الحقل **DocumentDate** تساوي التاريخ **الفارغ**.</span><span class="sxs-lookup"><span data-stu-id="938b8-112">The expression `IF( Invoice.DocumentDate = NULLDATE(), true, false)` returns **True** when the value of the **DocumentDate** field equals the **null** date.</span></span> <span data-ttu-id="938b8-113">في هذا المثال، **Invoice** عبارة عن مصدر بيانات تقارير إلكترونية (ER) من النوع **سجلات المالية/الجدول** ، ويشير إلى جدول CustInvoiceJour.</span><span class="sxs-lookup"><span data-stu-id="938b8-113">In this example, **Invoice** is an Electronic reporting (ER) data source of the **Finance/Table records** type, and it refers to the CustInvoiceJour table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="938b8-114">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="938b8-114">Additional resources</span></span>

[<span data-ttu-id="938b8-115">دلات التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="938b8-115">Date and time functions</span></span>](er-functions-category-datetime.md)
