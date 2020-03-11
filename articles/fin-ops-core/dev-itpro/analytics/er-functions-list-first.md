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
ms.openlocfilehash: 4d10abcf15b93961bd2ba4aec22914825d9ac38c
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042080"
---
# <span data-ttu-id="73be2-103"><a name="FIRST">FIRST ER وظيفة</a></span><span class="sxs-lookup"><span data-stu-id="73be2-103"><a name="FIRST">FIRST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="73be2-104">تُعيد الوظيفة `FIRST` السجل الأول من القائمة المُحددة كقيمة *حاوية (سجل)*، إذا لم تكن هذه القائمة فارغة.</span><span class="sxs-lookup"><span data-stu-id="73be2-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="73be2-105">إذا كانت القائمة فارغة، تطرح هذه الوظيفة استثناء.</span><span class="sxs-lookup"><span data-stu-id="73be2-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="73be2-106">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="73be2-106">Syntax</span></span>

```vb
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="73be2-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="73be2-107">Arguments</span></span>

<span data-ttu-id="73be2-108">`list`: *قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="73be2-108">`list`: *Record list*</span></span>

<span data-ttu-id="73be2-109">مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.</span><span class="sxs-lookup"><span data-stu-id="73be2-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="73be2-110">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="73be2-110">Return values</span></span>

<span data-ttu-id="73be2-111">*حاوية (سجل)*</span><span class="sxs-lookup"><span data-stu-id="73be2-111">*Container (record)*</span></span>

<span data-ttu-id="73be2-112">قيمة السجل الناتجة.</span><span class="sxs-lookup"><span data-stu-id="73be2-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="73be2-113">مثال1</span><span class="sxs-lookup"><span data-stu-id="73be2-113">Example 1</span></span>

<span data-ttu-id="73be2-114">يُرجع التعبير `FIRST(SPLIT("ABC",1)).Value` القيمة النصية **"A"**.</span><span class="sxs-lookup"><span data-stu-id="73be2-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="73be2-115">مثال2</span><span class="sxs-lookup"><span data-stu-id="73be2-115">Example 2</span></span>

<span data-ttu-id="73be2-116">يطرح التعبير `FIRST(SPLIT("",1)).Value` استثناءًا في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="73be2-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="73be2-117">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="73be2-117">Additional resources</span></span>

[<span data-ttu-id="73be2-118">دالات القائمة</span><span class="sxs-lookup"><span data-stu-id="73be2-118">List functions</span></span>](er-functions-category-list.md)
