---
title: COUNT ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني COUNT (ER).
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b3a5bb33964c70c85c7d8571057060c1c2b9d433
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687710"
---
# <a name="count-er-function"></a><span data-ttu-id="469d5-103">COUNT ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="469d5-103">COUNT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="469d5-104">تُرجع الوظيفة `COUNT` قيمة *عدد صحيح* تمثل عدد السجلات في القائمة المحددة، إذا لم تكن القائمة فارغة.</span><span class="sxs-lookup"><span data-stu-id="469d5-104">The `COUNT` function returns an *Integer* value that represents the number of records in the specified list, if the list isn't empty.</span></span> <span data-ttu-id="469d5-105">إذا كانت القائمة فارغة، تُرجع هذه وظيفة القيمة **0** (صفر).</span><span class="sxs-lookup"><span data-stu-id="469d5-105">If the list is empty, this function returns **0** (zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="469d5-106">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="469d5-106">Syntax</span></span>

```vb
COUNT (list)
```

## <a name="arguments"></a><span data-ttu-id="469d5-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="469d5-107">Arguments</span></span>

<span data-ttu-id="469d5-108">`list`: *قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="469d5-108">`list`: *Record list*</span></span>

<span data-ttu-id="469d5-109">مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.</span><span class="sxs-lookup"><span data-stu-id="469d5-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="469d5-110">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="469d5-110">Return values</span></span>

<span data-ttu-id="469d5-111">*عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="469d5-111">*Integer*</span></span>

<span data-ttu-id="469d5-112">القيمة العددية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="469d5-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="469d5-113">مثال</span><span class="sxs-lookup"><span data-stu-id="469d5-113">Example</span></span>

<span data-ttu-id="469d5-114">يُرجع التعبير `COUNT (SPLIT("abcd" , 3))` **2** ، لأن وظيفة `SPLIT` المستخدمة في هذا المثال تقوم بإنشاء قائمة تتكون من سجلين.</span><span class="sxs-lookup"><span data-stu-id="469d5-114">`COUNT (SPLIT("abcd" , 3))` returns **2**, because the `SPLIT` function that is used in this example creates a list that consists of two records.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="469d5-115">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="469d5-115">Additional resources</span></span>

[<span data-ttu-id="469d5-116">دالات القائمة</span><span class="sxs-lookup"><span data-stu-id="469d5-116">List functions</span></span>](er-functions-category-list.md)
