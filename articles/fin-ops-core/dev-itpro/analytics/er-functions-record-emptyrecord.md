---
title: 'وظيفة EMPTYRECORD ER '
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية EMPTYRECORD (ER).
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 2d3c34cbff8551b84121201b9489250c07c7799e
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563236"
---
# <a name="emptyrecord-er-function"></a><span data-ttu-id="17fbc-103">وظيفة EMPTYRECORD ER </span><span class="sxs-lookup"><span data-stu-id="17fbc-103">EMPTYRECORD ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17fbc-104">تُرجع الوظيفة `EMPTYRECORD` قيمة *حاوية (سجل)* فارغة لها نفس البنية كقائمة سجلات مُحددة أو سجل.</span><span class="sxs-lookup"><span data-stu-id="17fbc-104">The `EMPTYRECORD` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="17fbc-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="17fbc-105">Syntax</span></span>

```vb
EMPTYRECORD (list)
```

## <a name="arguments"></a><span data-ttu-id="17fbc-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="17fbc-106">Arguments</span></span>

<span data-ttu-id="17fbc-107">`list`: *قائمة سجلات* أو *حاوية (سجل)*</span><span class="sxs-lookup"><span data-stu-id="17fbc-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="17fbc-108">مسار صالح لمصدر بيانات إما من النوع *قائمة السجلات* أو *حاوية (سجل)*.</span><span class="sxs-lookup"><span data-stu-id="17fbc-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="17fbc-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="17fbc-109">Return values</span></span>

<span data-ttu-id="17fbc-110">*حاوية (سجل)*</span><span class="sxs-lookup"><span data-stu-id="17fbc-110">*Container (record)*</span></span>

<span data-ttu-id="17fbc-111">قيمة السجل الناتجة.</span><span class="sxs-lookup"><span data-stu-id="17fbc-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="17fbc-112">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="17fbc-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="17fbc-113">سجل فارغ عبارة عن سجل تحتوي فيه جميع الحقول على قيمة فارغة.</span><span class="sxs-lookup"><span data-stu-id="17fbc-113">A null record is a record where all fields have an empty value.</span></span> <span data-ttu-id="17fbc-114">قيمة فارغة هي **0** (صفر) للأرقام، سلسلة فارغة للسلاسل، وهكذا.</span><span class="sxs-lookup"><span data-stu-id="17fbc-114">An empty value is **0** (zero) for numbers, an empty string for strings, and so on.</span></span>

## <a name="example"></a><span data-ttu-id="17fbc-115">مثال</span><span class="sxs-lookup"><span data-stu-id="17fbc-115">Example</span></span>

<span data-ttu-id="17fbc-116">يُرجع التعبير `EMPTYRECORD (SPLIT ("abc", 1))` سجل فارغ جديد له نفس بنية القائمة المُرتجعة بواسطة الوظيفة `SPLIT` .</span><span class="sxs-lookup"><span data-stu-id="17fbc-116">`EMPTYRECORD (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="17fbc-117">لمزيد من المعلومات، راجع [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="17fbc-117">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="17fbc-118">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="17fbc-118">Additional resources</span></span>

[<span data-ttu-id="17fbc-119">وظائف السجلات</span><span class="sxs-lookup"><span data-stu-id="17fbc-119">Record functions</span></span>](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]