---
title: FIRSTORNULL ER وظيفة
description: 'يشرح هذا الموضوع كيفية استخدام وظيفة التقارير الإلكترونية FIRSTORNULL (ER) '
author: NickSelin
manager: kfend
ms.date: 11/29/2019
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
ms.openlocfilehash: e360812c5b0dbfb8df4ab279bf3e0050acebbb25
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745180"
---
# <a name="firstornull-er-function"></a><span data-ttu-id="1f873-103">FIRSTORNULL ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="1f873-103">FIRSTORNULL ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1f873-104">تُعيد الوظيفة `FIRSTORNULL` السجل الأول من القائمة المُحددة كقيمة *حاوية (سجل)*، إذا لم يكن هذا السجل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="1f873-104">The `FIRSTORNULL` function returns the first record of the specified list as a *Container (record)* value, if that record isn't empty.</span></span> <span data-ttu-id="1f873-105">إذا كان السجل فارغًا، تُرجع هذه الوظيفة قيمة *حاوية (سجل)* فارغة.</span><span class="sxs-lookup"><span data-stu-id="1f873-105">If the record is empty, this function returns a null *Container (record)* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f873-106">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="1f873-106">Syntax</span></span>

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a><span data-ttu-id="1f873-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="1f873-107">Arguments</span></span>

<span data-ttu-id="1f873-108">`list`: *قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="1f873-108">`list`: *Record list*</span></span>

<span data-ttu-id="1f873-109">مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.</span><span class="sxs-lookup"><span data-stu-id="1f873-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="1f873-110">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="1f873-110">Return values</span></span>

<span data-ttu-id="1f873-111">*حاوية (سجل)*</span><span class="sxs-lookup"><span data-stu-id="1f873-111">*Container (record)*</span></span>

<span data-ttu-id="1f873-112">قيمة السجل الناتجة.</span><span class="sxs-lookup"><span data-stu-id="1f873-112">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="1f873-113">مثال</span><span class="sxs-lookup"><span data-stu-id="1f873-113">Example</span></span>

<span data-ttu-id="1f873-114">يُرجع التعبير `FIRSTORNULL(SPLIT("",1)).Value` سلسلة فارغة (**""**).</span><span class="sxs-lookup"><span data-stu-id="1f873-114">The expression `FIRSTORNULL(SPLIT("",1)).Value` returns an empty string (**""**).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1f873-115">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="1f873-115">Additional resources</span></span>

[<span data-ttu-id="1f873-116">دالات القائمة</span><span class="sxs-lookup"><span data-stu-id="1f873-116">List functions</span></span>](er-functions-category-list.md)
