---
title: 'وظيفة EMPTYRECORD ER '
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية EMPTYRECORD (ER).
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
ms.openlocfilehash: 2e46fcef3d53483b782ac39a0661fc0edc8d861c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743940"
---
# <a name="emptyrecord-er-function"></a><span data-ttu-id="f5a94-103">وظيفة EMPTYRECORD ER </span><span class="sxs-lookup"><span data-stu-id="f5a94-103">EMPTYRECORD ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f5a94-104">تُرجع الوظيفة `EMPTYRECORD` قيمة *حاوية (سجل)* فارغة لها نفس البنية كقائمة سجلات مُحددة أو سجل.</span><span class="sxs-lookup"><span data-stu-id="f5a94-104">The `EMPTYRECORD` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5a94-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="f5a94-105">Syntax</span></span>

```vb
EMPTYRECORD (list)
```

## <a name="arguments"></a><span data-ttu-id="f5a94-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="f5a94-106">Arguments</span></span>

<span data-ttu-id="f5a94-107">`list`: *قائمة سجلات* أو *حاوية (سجل)*</span><span class="sxs-lookup"><span data-stu-id="f5a94-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="f5a94-108">مسار صالح لمصدر بيانات إما من النوع *قائمة السجلات* أو *حاوية (سجل)*.</span><span class="sxs-lookup"><span data-stu-id="f5a94-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="f5a94-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="f5a94-109">Return values</span></span>

<span data-ttu-id="f5a94-110">*حاوية (سجل)*</span><span class="sxs-lookup"><span data-stu-id="f5a94-110">*Container (record)*</span></span>

<span data-ttu-id="f5a94-111">قيمة السجل الناتجة.</span><span class="sxs-lookup"><span data-stu-id="f5a94-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f5a94-112">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="f5a94-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="f5a94-113">سجل فارغ عبارة عن سجل تحتوي فيه جميع الحقول على قيمة فارغة.</span><span class="sxs-lookup"><span data-stu-id="f5a94-113">A null record is a record where all fields have an empty value.</span></span> <span data-ttu-id="f5a94-114">قيمة فارغة هي **0** (صفر) للأرقام، سلسلة فارغة للسلاسل، وهكذا.</span><span class="sxs-lookup"><span data-stu-id="f5a94-114">An empty value is **0** (zero) for numbers, an empty string for strings, and so on.</span></span>

## <a name="example"></a><span data-ttu-id="f5a94-115">مثال</span><span class="sxs-lookup"><span data-stu-id="f5a94-115">Example</span></span>

<span data-ttu-id="f5a94-116">يُرجع التعبير `EMPTYRECORD (SPLIT ("abc", 1))` سجل فارغ جديد له نفس بنية القائمة المُرتجعة بواسطة الوظيفة `SPLIT` .</span><span class="sxs-lookup"><span data-stu-id="f5a94-116">`EMPTYRECORD (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="f5a94-117">لمزيد من المعلومات، راجع [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="f5a94-117">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f5a94-118">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="f5a94-118">Additional resources</span></span>

[<span data-ttu-id="f5a94-119">وظائف السجلات</span><span class="sxs-lookup"><span data-stu-id="f5a94-119">Record functions</span></span>](er-functions-category-record.md)
