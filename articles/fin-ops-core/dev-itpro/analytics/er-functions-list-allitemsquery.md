---
title: ALLITEMSQUERY ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني ALLITEMSQUERY (ER).
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
ms.openlocfilehash: 56ac956cdfe28d282b8a80d7caec34a50eca5dbe
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559593"
---
# <a name="allitemsquery-er-function"></a>ALLITEMSQUERY ER وظيفة

[!include [banner](../includes/banner.md)]

تعمل الوظيفة `ALLITEMSQUERY` كاستعلام SQL مُنضم. يقوم بإرجاع قيمة قيمة *قائمة السجلات* المٌسطحة التي تتكون من قائمة السجلات التي تمثل كافة العناصر التي تتطابق مع المسار المُحدد.

## <a name="syntax"></a>بناء الجملة

```vb
ALLITEMSQUERY (path)
```

## <a name="arguments"></a>الوسائط

`path`: *قائمة السجلات*

مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*. يجب أن يحتوي على علاقة واحدة على الأقل.

## <a name="return-values"></a>إرجاع القيم

*قائمة السجلات*

قائمة السجلات الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

يجب تعريف المسار المُحدد كمسار مصدر بيانات صالح لعنصر مصدر بيانات لنوع بيانات *قائمة السجلات*. يجب أن يحتوي أيضًا على علاقة واحدة على الأقل. يجب أن تُظهر عناصر البيانات مثل *سلسلة* المسار و *التاريخ* خطأ في وقت التصميم في منشئ تعبير التقارير الإلكترونية (ER).

عند تطبيق هذه وظيفة على مصادر البيانات من نوع بيانات *قائمة السجلات* التي تشير إلى كائن تطبيق يُمكن استدعائه مباشرة باستخدام SQL (على سبيل المثال، جدول أو كيان أو استعلام)، يتم تشغيله كاستعلام SQL مُنضم. وإلا، يتم تشغيله في الذاكرة كوظيفة [ALLITEMS](er-functions-list-allitems.md).

## <a name="example"></a>مثال

أنت تحدد مصادر البيانات التالية في تعيين نموذج:

- مصدر بيانات **CustInv** من النوع *سجلات الجدول* الذي يُشير إلى جدول CustInvoiceTable. 
- مصدر بيانات **FilteredInv** من النوع *الحقل المحسوب* الذي يحتوي على التعبير `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`
- مصدر بيانات **JourLines** من النوع *الحقل المحسوب* الذي يحتوي على التعبير `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`

عندما تقوم بتشغيل تعيين نموذج لطلب مصدر البيانات **JourLines**، فإنه يتم تشغيل عبارة SQL التالية:

```sql
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN
CUSTINVOICETRANS T3 WHERE...
```

## <a name="additional-resources"></a>الموارد الإضافية

[دالات القائمة](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]