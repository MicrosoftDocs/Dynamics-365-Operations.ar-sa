---
title: EMPTYLIST ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني EMPTYLIST (ER).
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 1e2a92d9951c3ad27503cf82f1b45026f16c3835
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746665"
---
# <a name="emptylist-er-function"></a><span data-ttu-id="2ea05-103">EMPTYLIST ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="2ea05-103">EMPTYLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ea05-104">تُرجع الوظيفة `EMPTYLIST` قيمة *قائمة سجلات* فارغة باستخدام القائمة المُحددة كمصدر لبنية القائمة.</span><span class="sxs-lookup"><span data-stu-id="2ea05-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ea05-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="2ea05-105">Syntax</span></span>

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="2ea05-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="2ea05-106">Arguments</span></span>

<span data-ttu-id="2ea05-107">`list`: *قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="2ea05-107">`list`: *Record list*</span></span>

<span data-ttu-id="2ea05-108">مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.</span><span class="sxs-lookup"><span data-stu-id="2ea05-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="2ea05-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="2ea05-109">Return values</span></span>

<span data-ttu-id="2ea05-110">*قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="2ea05-110">*Record list*</span></span>

<span data-ttu-id="2ea05-111">قائمة السجلات الناتجة.</span><span class="sxs-lookup"><span data-stu-id="2ea05-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="2ea05-112">مثال</span><span class="sxs-lookup"><span data-stu-id="2ea05-112">Example</span></span>

<span data-ttu-id="2ea05-113">يُرجع التعبير `EMPTYLIST (SPLIT ("abc", 1))` قائمة فارغة جديدة لها نفس بنية القائمة المُرتجعة بواسطة وظيفة `SPLIT` المستخدمة.</span><span class="sxs-lookup"><span data-stu-id="2ea05-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2ea05-114">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="2ea05-114">Additional resources</span></span>

[<span data-ttu-id="2ea05-115">دالات القائمة</span><span class="sxs-lookup"><span data-stu-id="2ea05-115">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]