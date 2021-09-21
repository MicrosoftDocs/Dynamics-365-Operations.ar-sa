---
title: الحد الأقصى لعدد الأرقام العشرية لوحدة حفظ المخزون هي 0
description: عند محاولة ترحيل حركة مخزون أو حجز مخزون، ستتلقى الخطأ "الحد الأقصى لعدد الأرقام العشرية لوحدة حفظ المخزون هي 0".
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 9dec198e2d77efd2253c80e14d15791cc37f88e1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475511"
---
# <a name="maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a>الحد الأقصى لعدد الأرقام العشرية لوحدة حفظ المخزون هي 0


## <a name="symptoms"></a>العلامات

عند محاولة ترحيل أحدي حركات المخزون أو حجز المخزون، تظهر رسالة الخطأ التالية:

> الحد الأقصى لعدد الأرقام العشرية لوحدة حفظ المخزون هي 0.

تحدث هذه المشكلة عند تحديد كميه العملية المخزنية كقيمه عشريه اقل من مستوي الدقة التي يدعمها الحقل. علي سبيل المثال، تم تحديد كميه قيمتها *0.5* لحركه المخزون، ولكن يتم دعم كميات الاعداد الصحيحة فقط. التالي، يجب ان تكون القيمة *1* بدلا من *0.5*.

## <a name="resolution"></a>الحل

1. قم بتشغيل البرنامج النصي التالي علي مثيل SQL Server لتقريب الكميات في العمليات المخزنية. سيقوم هذا البرنامج النصي بتصحيح القيم الموجودة في الجدول **inventTrans**.

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. تشغيل التحقق من التناسق الفعلي حيث يتم تشغيل خيار **إصلاح الخطأ**. سيقوم هذا الفحص بتصحيح القيم الموجودة في الجدول **inventSum**.

> [!IMPORTANT]
> نوصي بشده بتحرير البرنامج النصي كما هو مطلوب للبيئة الخاصة بك، واختباره في بيئة اختبار، ثم التحقق من البيانات الناتجة قبل تشغيل البرنامج النصي في بيئة التشغيل.
