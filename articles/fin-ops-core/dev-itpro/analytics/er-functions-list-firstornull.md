---
title: FIRSTORNULL ER وظيفة
description: 'يشرح هذا الموضوع كيفية استخدام وظيفة التقارير الإلكترونية FIRSTORNULL (ER) '
author: NickSelin
ms.date: 11/29/2019
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
ms.openlocfilehash: 1ccc094fc468470ffc857c729b6d8402796785d7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753206"
---
# <a name="firstornull-er-function"></a><span data-ttu-id="96d6d-103">FIRSTORNULL ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="96d6d-103">FIRSTORNULL ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="96d6d-104">تُعيد الوظيفة `FIRSTORNULL` السجل الأول من القائمة المُحددة كقيمة *حاوية (سجل)*، إذا لم يكن هذا السجل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="96d6d-104">The `FIRSTORNULL` function returns the first record of the specified list as a *Container (record)* value, if that record isn't empty.</span></span> <span data-ttu-id="96d6d-105">إذا كان السجل فارغًا، تُرجع هذه الوظيفة قيمة *حاوية (سجل)* فارغة.</span><span class="sxs-lookup"><span data-stu-id="96d6d-105">If the record is empty, this function returns a null *Container (record)* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="96d6d-106">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="96d6d-106">Syntax</span></span>

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a><span data-ttu-id="96d6d-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="96d6d-107">Arguments</span></span>

<span data-ttu-id="96d6d-108">`list`: *قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="96d6d-108">`list`: *Record list*</span></span>

<span data-ttu-id="96d6d-109">مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.</span><span class="sxs-lookup"><span data-stu-id="96d6d-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="96d6d-110">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="96d6d-110">Return values</span></span>

<span data-ttu-id="96d6d-111">*حاوية (سجل)*</span><span class="sxs-lookup"><span data-stu-id="96d6d-111">*Container (record)*</span></span>

<span data-ttu-id="96d6d-112">قيمة السجل الناتجة.</span><span class="sxs-lookup"><span data-stu-id="96d6d-112">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="96d6d-113">مثال</span><span class="sxs-lookup"><span data-stu-id="96d6d-113">Example</span></span>

<span data-ttu-id="96d6d-114">يُرجع التعبير `FIRSTORNULL(SPLIT("",1)).Value` سلسلة فارغة (**""**).</span><span class="sxs-lookup"><span data-stu-id="96d6d-114">The expression `FIRSTORNULL(SPLIT("",1)).Value` returns an empty string (**""**).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="96d6d-115">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="96d6d-115">Additional resources</span></span>

[<span data-ttu-id="96d6d-116">دالات القائمة</span><span class="sxs-lookup"><span data-stu-id="96d6d-116">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]