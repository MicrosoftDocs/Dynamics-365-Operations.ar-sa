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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c48483a6677aaeb36eac57a57cec71bf54c7991d
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745335"
---
# <a name="count-er-function"></a><span data-ttu-id="d3d44-103">COUNT ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="d3d44-103">COUNT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d3d44-104">تُرجع الوظيفة `COUNT` قيمة *عدد صحيح* تمثل عدد السجلات في القائمة المحددة، إذا لم تكن القائمة فارغة.</span><span class="sxs-lookup"><span data-stu-id="d3d44-104">The `COUNT` function returns an *Integer* value that represents the number of records in the specified list, if the list isn't empty.</span></span> <span data-ttu-id="d3d44-105">إذا كانت القائمة فارغة، تُرجع هذه وظيفة القيمة **0** (صفر).</span><span class="sxs-lookup"><span data-stu-id="d3d44-105">If the list is empty, this function returns **0** (zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="d3d44-106">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="d3d44-106">Syntax</span></span>

```vb
COUNT (list)
```

## <a name="arguments"></a><span data-ttu-id="d3d44-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="d3d44-107">Arguments</span></span>

<span data-ttu-id="d3d44-108">`list`: *قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="d3d44-108">`list`: *Record list*</span></span>

<span data-ttu-id="d3d44-109">مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.</span><span class="sxs-lookup"><span data-stu-id="d3d44-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="d3d44-110">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="d3d44-110">Return values</span></span>

<span data-ttu-id="d3d44-111">*عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="d3d44-111">*Integer*</span></span>

<span data-ttu-id="d3d44-112">القيمة العددية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="d3d44-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="d3d44-113">مثال</span><span class="sxs-lookup"><span data-stu-id="d3d44-113">Example</span></span>

<span data-ttu-id="d3d44-114">يُرجع التعبير `COUNT (SPLIT("abcd" , 3))` **2** ، لأن وظيفة `SPLIT` المستخدمة في هذا المثال تقوم بإنشاء قائمة تتكون من سجلين.</span><span class="sxs-lookup"><span data-stu-id="d3d44-114">`COUNT (SPLIT("abcd" , 3))` returns **2**, because the `SPLIT` function that is used in this example creates a list that consists of two records.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d3d44-115">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="d3d44-115">Additional resources</span></span>

[<span data-ttu-id="d3d44-116">دالات القائمة</span><span class="sxs-lookup"><span data-stu-id="d3d44-116">List functions</span></span>](er-functions-category-list.md)
