---
title: EMPTYLIST ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني EMPTYLIST (ER).
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
ms.openlocfilehash: 747b661d0dee4e9c27741e167c89f9ef7eefa470
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745311"
---
# <a name="emptylist-er-function"></a><span data-ttu-id="0f7d6-103">EMPTYLIST ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="0f7d6-103">EMPTYLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f7d6-104">تُرجع الوظيفة `EMPTYLIST` قيمة *قائمة سجلات* فارغة باستخدام القائمة المُحددة كمصدر لبنية القائمة.</span><span class="sxs-lookup"><span data-stu-id="0f7d6-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f7d6-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="0f7d6-105">Syntax</span></span>

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="0f7d6-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="0f7d6-106">Arguments</span></span>

<span data-ttu-id="0f7d6-107">`list`: *قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="0f7d6-107">`list`: *Record list*</span></span>

<span data-ttu-id="0f7d6-108">مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.</span><span class="sxs-lookup"><span data-stu-id="0f7d6-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="0f7d6-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="0f7d6-109">Return values</span></span>

<span data-ttu-id="0f7d6-110">*قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="0f7d6-110">*Record list*</span></span>

<span data-ttu-id="0f7d6-111">قائمة السجلات الناتجة.</span><span class="sxs-lookup"><span data-stu-id="0f7d6-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="0f7d6-112">مثال</span><span class="sxs-lookup"><span data-stu-id="0f7d6-112">Example</span></span>

<span data-ttu-id="0f7d6-113">يُرجع التعبير `EMPTYLIST (SPLIT ("abc", 1))` قائمة فارغة جديدة لها نفس بنية القائمة المُرتجعة بواسطة وظيفة `SPLIT` المستخدمة.</span><span class="sxs-lookup"><span data-stu-id="0f7d6-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0f7d6-114">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="0f7d6-114">Additional resources</span></span>

[<span data-ttu-id="0f7d6-115">دالات القائمة</span><span class="sxs-lookup"><span data-stu-id="0f7d6-115">List functions</span></span>](er-functions-category-list.md)
