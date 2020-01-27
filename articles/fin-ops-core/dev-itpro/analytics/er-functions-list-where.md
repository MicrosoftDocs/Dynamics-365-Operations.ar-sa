---
title: WHERE ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية WHERE (ER).
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
ms.openlocfilehash: 50d90697f522f3c4d7b62190928008b6d923ffc6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916075"
---
# <a name="WHERE">WHERE ER وظيفة</a>

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `WHERE` القائمة المُحددة كقيمة *قائمة السجلات* بعد أن تمت تصفيتها وفقًا للشرط المُحدد.

## <a name="syntax"></a>بناء الجملة

```
WHERE (list, condition)
```

## <a name="arguments"></a>الوسائط

`list`: *قائمة السجلات*

مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.

`condition`: *منطقي*

تعبير شرطي صالح يُستخدم لتصفية سجلات القائمة المُحددة.

## <a name="return-values"></a>إرجاع القيم

*قائمة السجلات*

قائمة السجلات الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

تختلف هذه الوظيفة عن وظيفة [FILTER](er-functions-list-filter.md) ، لأن يتم تطبيق الشرط المُحدد على أي من مصادر بيانات التقارير الإلكترونية (ER) لنوع *قائمة السجلات* الموجودة في الذاكرة.

إذا كانت هذه الوسيطات المكونة لهذه الوظيفة (`list` و`condition`) تسمح بترجمة هذا الطلب للاستدعاء المباشر لـ SQL، يتم طرح رسالة تحذيرية في وقت التصميم. تُعلم هذه الرسالة المستخدم أنه يُمكنه تحسين الأداء إذا تم استخدام الوظيفة [FILTER](er-functions-list-filter.md) بدلًا من `WHERE`.

## <a name="example-1"></a>مثال1

إذا تم تكوين **Vendor** كمصدر بيانات تقارير إلكترونية يشير إلى جدول VendTable، يُرجع التعبير `WHERE (Vendors, Vendors.VendGroup = "40")` قائمة المورّدين التي تنتمي إلى مجموعة الموردين 40.

## <a name="example-2"></a>مثال2

إذا أدخلت مصدر البيانات **DS** من النوع *الحقل المحسوب* ، ويحتوي على التعبير `SPLIT ("A|B|C", "|")` ، يُرجع التعبير `WHERE( DS, DS.Value = "B")` قائمة بسجل واحد فقط يحتوي على النص **"B"** في حقل **القيمة**.

## <a name="additional-resources"></a>الموارد الإضافية

[دالات القائمة](er-functions-category-list.md)
