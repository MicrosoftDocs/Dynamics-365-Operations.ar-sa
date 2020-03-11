---
title: LISTOFFIRSTITEM ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية LISTOFFIRSTITEM (ER).
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
ms.openlocfilehash: 8cd48732280c9af0b89129a32b42285207f97fb7
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041965"
---
# <span data-ttu-id="75297-103"><a name="LISTOFFIRSTITEM">LISTOFFIRSTITEM ER وظيفة</a></span><span class="sxs-lookup"><span data-stu-id="75297-103"><a name="LISTOFFIRSTITEM">LISTOFFIRSTITEM ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="75297-104">تُرجع الوظيفة `LISTOFFIRSTITEM` قيمة *قائمة السجلات* التي تتكون فقط من السجل الأول للقائمة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="75297-104">The `LISTOFFIRSTITEM` function returns a *Record list* value that consists of only the first record of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="75297-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="75297-105">Syntax</span></span>

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a><span data-ttu-id="75297-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="75297-106">Arguments</span></span>

<span data-ttu-id="75297-107">`list`: *قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="75297-107">`list`: *Record list*</span></span>

<span data-ttu-id="75297-108">مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.</span><span class="sxs-lookup"><span data-stu-id="75297-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="75297-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="75297-109">Return values</span></span>

<span data-ttu-id="75297-110">*قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="75297-110">*Record list*</span></span>

<span data-ttu-id="75297-111">قائمة السجلات الناتجة.</span><span class="sxs-lookup"><span data-stu-id="75297-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="75297-112">مثال</span><span class="sxs-lookup"><span data-stu-id="75297-112">Example</span></span>

<span data-ttu-id="75297-113">يُرجع التعبير `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` القيمة النصية **"A"**.</span><span class="sxs-lookup"><span data-stu-id="75297-113">The expression `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returns the text value **"A"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="75297-114">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="75297-114">Additional resources</span></span>

[<span data-ttu-id="75297-115">دالات القائمة</span><span class="sxs-lookup"><span data-stu-id="75297-115">List functions</span></span>](er-functions-category-list.md)
