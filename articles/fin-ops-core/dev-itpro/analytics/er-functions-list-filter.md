---
title: FILTER ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية FILTER (ER).
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
ms.openlocfilehash: adeefd08531f59e478efbb45ab294b3bc8216f4c
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042126"
---
# <a name="FILTER">FILTER ER وظيفة</a>

[!include [banner](../includes/banner.md)]

تٌرجع وظيفة `FILTER` القائمة المُحددة كقيمة *قائمة سجلات* بعد تغيير الاستعلام بحيث تتم تصفيتها للشرط المُحدد.

## <a name="syntax"></a>بناء الجملة

```vb
FILTER (list, condition)
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

تختلف هذه وظيفة عن وظيفة [WHERE](er-functions-list-where.md) لأنه يتم تطبيق الشرط المحدد على أي من مصادر بيانات التقارير الإلكترونية (ER) لنوع *سجلات الجداول* على مستوى قاعدة البيانات. يمكن تحديد القائمة والشرط باستخدام الجداول والعلاقات.

إذا لم تسمح أحد الوسيطتين أو كليهما المكونة لهذه الوظيفة (`list` و`condition`) بترجمة هذا الطلب للاستدعاء المباشر لـ SQL، يتم طرح استثناء في وقت التصميم. يُعلم هذا الاستثناء المستخدم أنه إما `list` أو `condition` لا يُمكن استخدامهم للاستعلام عن قاعدة البيانات.

## <a name="example-1"></a>مثال1

إذا تم تكوين **Vendor** كمصدر بيانات تقارير إلكترونية يشير إلى جدول VendTable، يُرجع التعبير `FILTER (Vendors, Vendors.VendGroup = "40")` قائمة المورّدين التي تنتمي إلى مجموعة الموردين 40.

## <a name="example-2"></a>مثال2

إذا تم تكوين **المورّد** كمصدر بيانات التقارير الإلكترونية (ER) يُشير إلى جدول VendTable، وإذا تم تكوين **parmVendorBankGroup** كمصدر بيانات التقارير الإلكترونية (ER) يُرجع قيمة نوع بيانات *السلسلة*، يُرجع التعبير `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` قائمة حسابات المورّدين الذين ينتمون إلى مجموعة بنكية مُحددة.

## <a name="example-3"></a>المثال الثالث

يُمكنك إدخال مصدر بيانات **DS** من النوع *الحقل المحسوب* ، الذي يحتوي على التعبير `SPLIT ("A,B,C", ",")`. ثم قم بإدخال تعبير آخر، `FILTER( DS, DS.Value = "B")`. عندما تحاول حفظ هذا التعبير في مصم تركيبة التقارير الإلكترونية ER، يتم طرح الاستثناء التالي: "خطأ التحقق من الصحة: تعبير القائمة للوظيفة FILTER غير قابل للاستعلام."

## <a name="additional-resources"></a>الموارد الإضافية

[دالات القائمة](er-functions-category-list.md)
