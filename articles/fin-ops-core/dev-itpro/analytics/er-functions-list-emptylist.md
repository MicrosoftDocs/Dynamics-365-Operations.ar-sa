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
ms.openlocfilehash: a60bc948ff6223b6e3acccd0ba40bf64f238aac2
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917386"
---
# <span data-ttu-id="d37cb-103"><a name="EMPTYLIST">EMPTYLIST ER وظيفة</a></span><span class="sxs-lookup"><span data-stu-id="d37cb-103"><a name="EMPTYLIST">EMPTYLIST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d37cb-104">تُرجع الوظيفة `EMPTYLIST` قيمة *قائمة سجلات* فارغة باستخدام القائمة المُحددة كمصدر لبنية القائمة.</span><span class="sxs-lookup"><span data-stu-id="d37cb-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="d37cb-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="d37cb-105">Syntax</span></span>

```
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="d37cb-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="d37cb-106">Arguments</span></span>

<span data-ttu-id="d37cb-107">`list`: *قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="d37cb-107">`list`: *Record list*</span></span>

<span data-ttu-id="d37cb-108">مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.</span><span class="sxs-lookup"><span data-stu-id="d37cb-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="d37cb-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="d37cb-109">Return values</span></span>

<span data-ttu-id="d37cb-110">*قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="d37cb-110">*Record list*</span></span>

<span data-ttu-id="d37cb-111">قائمة السجلات الناتجة.</span><span class="sxs-lookup"><span data-stu-id="d37cb-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="d37cb-112">مثال</span><span class="sxs-lookup"><span data-stu-id="d37cb-112">Example</span></span>

<span data-ttu-id="d37cb-113">يُرجع التعبير `EMPTYLIST (SPLIT ("abc", 1))` قائمة فارغة جديدة لها نفس بنية القائمة المُرتجعة بواسطة وظيفة `SPLIT` المستخدمة.</span><span class="sxs-lookup"><span data-stu-id="d37cb-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d37cb-114">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="d37cb-114">Additional resources</span></span>

[<span data-ttu-id="d37cb-115">دالات القائمة</span><span class="sxs-lookup"><span data-stu-id="d37cb-115">List functions</span></span>](er-functions-category-list.md)