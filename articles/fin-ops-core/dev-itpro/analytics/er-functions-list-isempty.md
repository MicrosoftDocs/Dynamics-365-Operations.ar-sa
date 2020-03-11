---
title: ISEMPTY ER الوظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية ISEMPTY (ER).
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
ms.openlocfilehash: 6adca3c95c10e7d4b3287561925a9d9fe8a74121
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042034"
---
# <span data-ttu-id="62612-103"><a name="ISEMPTY">ISEMPTY ER الوظيفة</a></span><span class="sxs-lookup"><span data-stu-id="62612-103"><a name="ISEMPTY">ISEMPTY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="62612-104">تُرجع الوظيفة `ISEMPTY` قيمة *منطقية* **TRUE** إذا كانت القائمة المُحددة لا تحتوي على سجلات.</span><span class="sxs-lookup"><span data-stu-id="62612-104">The `ISEMPTY` function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="62612-105">وبخلاف ذلك، تُرجع قيمة *منطقية* لـ **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="62612-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="62612-106">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="62612-106">Syntax</span></span>

```vb
ISEMPTY (list)
```

## <a name="arguments"></a><span data-ttu-id="62612-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="62612-107">Arguments</span></span>

<span data-ttu-id="62612-108">`list`: *قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="62612-108">`list`: *Record list*</span></span>

<span data-ttu-id="62612-109">مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.</span><span class="sxs-lookup"><span data-stu-id="62612-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="62612-110">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="62612-110">Return values</span></span>

<span data-ttu-id="62612-111">*منطقي*</span><span class="sxs-lookup"><span data-stu-id="62612-111">*Boolean*</span></span>

<span data-ttu-id="62612-112">القيمة *المنطقية* الناتجة.</span><span class="sxs-lookup"><span data-stu-id="62612-112">The resulting *Boolean* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="62612-113">مثال1</span><span class="sxs-lookup"><span data-stu-id="62612-113">Example 1</span></span>

<span data-ttu-id="62612-114">إذا قمت بإدخال مصدر البيانات **DS** من النوع *الحقل المحسوب* ، ويحتوي على التعبير `SPLIT ("A|B|C", "|")` ، يُرجع التعبير `ISEMPTY(DS)` **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="62612-114">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `ISEMPTY(DS)` returns **FALSE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="62612-115">مثال2</span><span class="sxs-lookup"><span data-stu-id="62612-115">Example 2</span></span>

<span data-ttu-id="62612-116">يُرجع التعبير `ISEMPTY (SPLIT ("",1))` **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="62612-116">The expression `ISEMPTY (SPLIT ("",1))` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="62612-117">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="62612-117">Additional resources</span></span>

[<span data-ttu-id="62612-118">دالات القائمة</span><span class="sxs-lookup"><span data-stu-id="62612-118">List functions</span></span>](er-functions-category-list.md)
