---
title: FIRST ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية FIRST (ER).
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
ms.openlocfilehash: 3ed0e0aaf29e2a67a4842d71121f1adc24f524f7
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745215"
---
# <a name="first-er-function"></a><span data-ttu-id="d245a-103">FIRST ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="d245a-103">FIRST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d245a-104">تُعيد الوظيفة `FIRST` السجل الأول من القائمة المُحددة كقيمة *حاوية (سجل)*، إذا لم تكن هذه القائمة فارغة.</span><span class="sxs-lookup"><span data-stu-id="d245a-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="d245a-105">إذا كانت القائمة فارغة، تطرح هذه الوظيفة استثناء.</span><span class="sxs-lookup"><span data-stu-id="d245a-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="d245a-106">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="d245a-106">Syntax</span></span>

```vb
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="d245a-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="d245a-107">Arguments</span></span>

<span data-ttu-id="d245a-108">`list`: *قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="d245a-108">`list`: *Record list*</span></span>

<span data-ttu-id="d245a-109">مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.</span><span class="sxs-lookup"><span data-stu-id="d245a-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="d245a-110">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="d245a-110">Return values</span></span>

<span data-ttu-id="d245a-111">*حاوية (سجل)*</span><span class="sxs-lookup"><span data-stu-id="d245a-111">*Container (record)*</span></span>

<span data-ttu-id="d245a-112">قيمة السجل الناتجة.</span><span class="sxs-lookup"><span data-stu-id="d245a-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="d245a-113">مثال1</span><span class="sxs-lookup"><span data-stu-id="d245a-113">Example 1</span></span>

<span data-ttu-id="d245a-114">يُرجع التعبير `FIRST(SPLIT("ABC",1)).Value` القيمة النصية **"A"**.</span><span class="sxs-lookup"><span data-stu-id="d245a-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="d245a-115">مثال2</span><span class="sxs-lookup"><span data-stu-id="d245a-115">Example 2</span></span>

<span data-ttu-id="d245a-116">يطرح التعبير `FIRST(SPLIT("",1)).Value` استثناءًا في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="d245a-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d245a-117">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="d245a-117">Additional resources</span></span>

[<span data-ttu-id="d245a-118">دالات القائمة</span><span class="sxs-lookup"><span data-stu-id="d245a-118">List functions</span></span>](er-functions-category-list.md)
