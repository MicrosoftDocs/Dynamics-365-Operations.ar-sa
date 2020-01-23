---
title: 'وظيفة NULLCONTAINER ER '
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني NULLCONTAINER (ER).
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
ms.openlocfilehash: 1dde102acf18e451cb895b51b28d22102f38936c
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915776"
---
# <span data-ttu-id="da560-103"><a name="NULLCONTAINER">وظيفة NULLCONTAINER ER </a></span><span class="sxs-lookup"><span data-stu-id="da560-103"><a name="NULLCONTAINER">NULLCONTAINER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="da560-104">تُرجع الوظيفة `NULLCONTAINER` قيمة *حاوية (سجل)* فارغة لها نفس البنية كقائمة سجلات مُحددة أو سجل.</span><span class="sxs-lookup"><span data-stu-id="da560-104">The `NULLCONTAINER` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="da560-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="da560-105">Syntax</span></span>

```
NULLCONTAINER (list)
```

## <a name="arguments"></a><span data-ttu-id="da560-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="da560-106">Arguments</span></span>

<span data-ttu-id="da560-107">`list`: *قائمة سجلات* أو *حاوية (سجل)*</span><span class="sxs-lookup"><span data-stu-id="da560-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="da560-108">مسار صالح لمصدر بيانات إما من النوع *قائمة السجلات* أو *حاوية (سجل)*.</span><span class="sxs-lookup"><span data-stu-id="da560-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="da560-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="da560-109">Return values</span></span>

<span data-ttu-id="da560-110">*حاوية (سجل)*</span><span class="sxs-lookup"><span data-stu-id="da560-110">*Container (record)*</span></span>

<span data-ttu-id="da560-111">قيمة السجل الناتجة.</span><span class="sxs-lookup"><span data-stu-id="da560-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="da560-112">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="da560-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="da560-113">هذه الدالة قديمة.</span><span class="sxs-lookup"><span data-stu-id="da560-113">This function is obsolete.</span></span> <span data-ttu-id="da560-114">استخدم الوظيفة `EMPTYRECORD` بدلًا من ذلك.</span><span class="sxs-lookup"><span data-stu-id="da560-114">Use the `EMPTYRECORD` function instead.</span></span> <span data-ttu-id="da560-115">لمزيد من المعلومات، راجع [EMPTYRECORD](er-functions-record-emptyrecord.md).</span><span class="sxs-lookup"><span data-stu-id="da560-115">For more information, see [EMPTYRECORD](er-functions-record-emptyrecord.md).</span></span>

## <a name="example"></a><span data-ttu-id="da560-116">مثال</span><span class="sxs-lookup"><span data-stu-id="da560-116">Example</span></span>

<span data-ttu-id="da560-117">يُرجع التعبير `NULLCONTAINER (SPLIT ("abc", 1))` سجل فارغ جديد له نفس بنية القائمة المُرتجعة بواسطة الوظيفة `SPLIT` .</span><span class="sxs-lookup"><span data-stu-id="da560-117">`NULLCONTAINER (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="da560-118">لمزيد من المعلومات، راجع [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="da560-118">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="da560-119">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="da560-119">Additional resources</span></span>

[<span data-ttu-id="da560-120">وظائف السجلات</span><span class="sxs-lookup"><span data-stu-id="da560-120">Record functions</span></span>](er-functions-category-record.md)
