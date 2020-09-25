---
title: ENUMERATE ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني ENUMERATE (ER).
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
ms.openlocfilehash: e1871ee41267c2c0e8b35007a47c9601079f05d7
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745239"
---
# <a name="enumerate-er-function"></a><span data-ttu-id="442cb-103">ENUMERATE ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="442cb-103">ENUMERATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="442cb-104">تُرجع الوظيفة `ENUMERATE` قيمة *قائمة سجلات* جديدة تتكون من السجلات التي تم تعدادها للقائمة المحددة.</span><span class="sxs-lookup"><span data-stu-id="442cb-104">The `ENUMERATE` function returns a new *Record list* value that consists of enumerated records of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="442cb-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="442cb-105">Syntax</span></span>

```vb
ENUMERATE (list)
```

## <a name="arguments"></a><span data-ttu-id="442cb-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="442cb-106">Arguments</span></span>

<span data-ttu-id="442cb-107">`list`: *قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="442cb-107">`list`: *Record list*</span></span>

<span data-ttu-id="442cb-108">مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.</span><span class="sxs-lookup"><span data-stu-id="442cb-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="442cb-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="442cb-109">Return values</span></span>

<span data-ttu-id="442cb-110">*قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="442cb-110">*Record list*</span></span>

<span data-ttu-id="442cb-111">قائمة السجلات الناتجة.</span><span class="sxs-lookup"><span data-stu-id="442cb-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="442cb-112">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="442cb-112">Usage notes</span></span>

<span data-ttu-id="442cb-113">تكشف قائمة السجلات التي تم تعدادها المُعادة العناصر الإضافية التالية:</span><span class="sxs-lookup"><span data-stu-id="442cb-113">The list of enumerated records that is returned exposes the following additional elements:</span></span>

- <span data-ttu-id="442cb-114">سجل الحقول (مكون**القيمة** )</span><span class="sxs-lookup"><span data-stu-id="442cb-114">The record of fields (**Value** component)</span></span>
- <span data-ttu-id="442cb-115">فهرس السجلات الحالية (المكون **Number**)</span><span class="sxs-lookup"><span data-stu-id="442cb-115">The current record index (**Number** component)</span></span>

## <a name="example"></a><span data-ttu-id="442cb-116">مثال</span><span class="sxs-lookup"><span data-stu-id="442cb-116">Example</span></span>

<span data-ttu-id="442cb-117">في الرسم التوضيحي التالي، يتم إنشاء مصدر البيانات **Enumerated** كقائمة تم تعدادها لسجلات المورّدين من مصدر البيانات **Vendors** الذي يشير إلى الجدول VendTable.</span><span class="sxs-lookup"><span data-stu-id="442cb-117">In the following illustration, an **Enumerated** data source is created as an enumerated list of vendor records from the **Vendors** data source that refers to the VendTable table.</span></span>

<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>

<span data-ttu-id="442cb-118">يوضح الرسم التوضيحي التالي تنسيق التقارير الإلكترونية (ER).</span><span class="sxs-lookup"><span data-stu-id="442cb-118">The following illustration shows the Electronic reporting (ER) format.</span></span> <span data-ttu-id="442cb-119">في هذا التنسيق، يتم إنشاء عمليات ربط البيانات لإنشاء إخراج بتنسيق XML.</span><span class="sxs-lookup"><span data-stu-id="442cb-119">In this format, data bindings are created to generate output in XML format.</span></span> <span data-ttu-id="442cb-120">يقدم هذا الإخراج موردين فرديين كعقد تم تعدادها.</span><span class="sxs-lookup"><span data-stu-id="442cb-120">This output presents individual vendors as enumerated nodes.</span></span>

<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>

<span data-ttu-id="442cb-121">يعرض الرسم التوضيحي التالي النتيجة عند تشغيل التنسيق المصمم.</span><span class="sxs-lookup"><span data-stu-id="442cb-121">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>

## <a name="additional-resources"></a><span data-ttu-id="442cb-122">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="442cb-122">Additional resources</span></span>

[<span data-ttu-id="442cb-123">دالات القائمة</span><span class="sxs-lookup"><span data-stu-id="442cb-123">List functions</span></span>](er-functions-category-list.md)
