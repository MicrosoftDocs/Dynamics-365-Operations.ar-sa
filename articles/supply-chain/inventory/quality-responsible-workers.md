---
title: العاملون المسؤولون عن الموافقة على حالات عدم المطابقة
description: يوضح هذا الموضوع كيفيه تكوين العمال المسؤولين عن اعتماد حالات عدم التوافق.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d3f647de2c188661c2c9c5f31e2642c3f8ca0b5
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021770"
---
# <a name="workers-responsible-for-approving-nonconformances"></a>العاملون المسؤولون عن الموافقة على حالات عدم المطابقة

[!include [banner](../includes/banner.md)]

يوضح هذا الموضوع كيفيه تكوين العمال المسؤولين عن اعتماد حالات عدم التوافق.

يجب اعتماد عدم التوافق قبل ان يتمكن المستخدمون من البدء في إدخال التفاصيل مثل التصحيحات أو العمليات. قبل ان يتمكن المستخدمون من اعتماد حالات عدم التوافق أو رفضها، يجب ربط معرف المستخدم (سجل المستخدم) الخاص بهم بسجل العامل. يمكنك اختياريا تكوين العمال المسؤولين عن الجودة، ثم السماح لعامل واحد باعتماد العمل بالنيابة عن عامل آخر.

## <a name="enable-a-user-for-nonconformance-processing"></a>تمكين المستخدم لمعالجة عدم المطابقة.

قبل أن يتمكن المستخدم من قبول حالات عدم المطابقة أو رفضها، يجب عليك ربط سجل المستخدم الخاص به بسجل عامل. ويمكن بعد ذلك تعيين حقول الاعتماد تلقائيا، ويمكن ملء المستخدم الحالي تلقائيا بالجدول الزمني. قبل أن يتمكن المستخدم من استخدام ملاحظات المستند، يجب عليك تنشيط معالجة المستندات في خيارات المستخدم الخاصة به.

1. انتقل إلى **إدارة النظام \> المستخدمون‏‎ \> المستخدمون**.
1. البحث عن وفتح المستخدم الذي يجب ان يكون قادرا علي اعتماد حالات عدم التوافق أو رفضها.
1. قم بتعيين حقل **الشخص** إلى اسم العامل المرتبط بسجل المستخدم الحالي.
1. في جزء الإجراءات، حدد **خيارات المستخدم**.
1. في صفحة **الخيارات** لسجل المستخدم الحالي، في علامة التبويب **التفضيلات**، قم بتعيين خيار **تمكين معالجة المستند** إلى *نعم*.
1. قم بإغلاق الصفحات.

## <a name="define-workers-that-are-responsible-for-quality"></a>تحديد العاملين المسؤولين عن الجودة

1. انتقل إلى **إدارة المخزون \> الإعداد \> مراقبة الجودة \> العمال المسؤولين عن الجودة**.
2. في جزء الإجراء، حدد **جديد**.
3. في حقل **العامل**، حدد العامل الذي يدخل بيانات الجودة.
4. في حقل **العامل المسؤول**، حدد العامل الذي يقوم العامل المحدد بإدخال العمل نيابة عنه. وعند إنشاء حالات عدم التوافق وتحديثها، سيتم إدخال هذا العامل بشكل افتراضي في حقول **العاملين**.

## <a name="additional-resources"></a>الموارد الإضافية

- [نظرة عامة على إدارة الجودة](quality-management-processes.md)
- [تمكين إدارة عدم المطابقة والجودة](enable-quality-management.md)
- [مصاريف الجودة](quality-charges.md)
- [مناطق العزل لحالات عدم المطابقة](quality-quarantine-zones.md)
- [أنواع التشخيص لحالات عدم المطابقة](quality-diagnostic-types.md)
- [مصاريف الجودة لحالات عدم المطابقة](quality-charges.md)
- [عمليات حالات عدم المطابقة](quality-operations.md)
- [إدارة الجودة لعمليات المستودعات](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]