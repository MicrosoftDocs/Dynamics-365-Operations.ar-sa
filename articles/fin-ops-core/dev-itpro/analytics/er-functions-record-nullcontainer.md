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
ms.openlocfilehash: ea71bfc4b30164fd32e804bf83a46c49cd18d155
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041459"
---
# <span data-ttu-id="d0d1f-103"><a name="NULLCONTAINER">وظيفة NULLCONTAINER ER </a></span><span class="sxs-lookup"><span data-stu-id="d0d1f-103"><a name="NULLCONTAINER">NULLCONTAINER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d0d1f-104">تُرجع الوظيفة `NULLCONTAINER` قيمة *حاوية (سجل)* فارغة لها نفس البنية كقائمة سجلات مُحددة أو سجل.</span><span class="sxs-lookup"><span data-stu-id="d0d1f-104">The `NULLCONTAINER` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0d1f-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="d0d1f-105">Syntax</span></span>

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a><span data-ttu-id="d0d1f-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="d0d1f-106">Arguments</span></span>

<span data-ttu-id="d0d1f-107">`list`: *قائمة سجلات* أو *حاوية (سجل)*</span><span class="sxs-lookup"><span data-stu-id="d0d1f-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="d0d1f-108">مسار صالح لمصدر بيانات إما من النوع *قائمة السجلات* أو *حاوية (سجل)*.</span><span class="sxs-lookup"><span data-stu-id="d0d1f-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="d0d1f-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="d0d1f-109">Return values</span></span>

<span data-ttu-id="d0d1f-110">*حاوية (سجل)*</span><span class="sxs-lookup"><span data-stu-id="d0d1f-110">*Container (record)*</span></span>

<span data-ttu-id="d0d1f-111">قيمة السجل الناتجة.</span><span class="sxs-lookup"><span data-stu-id="d0d1f-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d0d1f-112">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="d0d1f-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="d0d1f-113">هذه الدالة قديمة.</span><span class="sxs-lookup"><span data-stu-id="d0d1f-113">This function is obsolete.</span></span> <span data-ttu-id="d0d1f-114">استخدم الوظيفة `EMPTYRECORD` بدلًا من ذلك.</span><span class="sxs-lookup"><span data-stu-id="d0d1f-114">Use the `EMPTYRECORD` function instead.</span></span> <span data-ttu-id="d0d1f-115">لمزيد من المعلومات، راجع [EMPTYRECORD](er-functions-record-emptyrecord.md).</span><span class="sxs-lookup"><span data-stu-id="d0d1f-115">For more information, see [EMPTYRECORD](er-functions-record-emptyrecord.md).</span></span>

## <a name="example"></a><span data-ttu-id="d0d1f-116">مثال</span><span class="sxs-lookup"><span data-stu-id="d0d1f-116">Example</span></span>

<span data-ttu-id="d0d1f-117">يُرجع التعبير `NULLCONTAINER (SPLIT ("abc", 1))` سجل فارغ جديد له نفس بنية القائمة المُرتجعة بواسطة الوظيفة `SPLIT` .</span><span class="sxs-lookup"><span data-stu-id="d0d1f-117">`NULLCONTAINER (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="d0d1f-118">لمزيد من المعلومات، راجع [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="d0d1f-118">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d0d1f-119">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="d0d1f-119">Additional resources</span></span>

[<span data-ttu-id="d0d1f-120">وظائف السجلات</span><span class="sxs-lookup"><span data-stu-id="d0d1f-120">Record functions</span></span>](er-functions-category-record.md)
