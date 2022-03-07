---
title: مناطق العزل لحالات عدم المطابقة
description: يوضح هذا الموضوع كيفيه إنشاء مناطق العزل لحالات عدم التوافق واستخدامها.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c770da899f07597896d0d392b5192ddc4162bec6271d0e11c34797d7a15f857e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6754025"
---
# <a name="quarantine-zones-for-nonconformances"></a>مناطق العزل لحالات عدم المطابقة

[!include [banner](../includes/banner.md)]

يوضح هذا الموضوع كيفيه إنشاء مناطق العزل لحالات عدم التوافق واستخدامها.

يمكنك استخدام **مناطق العزل** لتحديد المناطق التي يمكن تعيينها لحالات عدم المطابقة. عند إنشاء حالة عدم توافق، يمكنك تعيين حقلي **منطقة العزل** و **نوع العزل** في علامة التبويب **عام** في صفحة **حالات عدم المطابقة**. يشير حقل **منطقة العزل** يشير عادةً إلى المنطقة أو الموقع حيث يوجد العنصر. يحدد حقل **نوع العزل** العنصر كإما *استخدام مقيد* أو *لا يمكن استخدامه*.

عند طباعه تقرير عدم التوافق أو التصحيحات لعدم التوافق، يمكنك عرض منطقه الفحص التي يوجد بها الصنف.

يمكنك أيضا طباعه علامة عدم توافق لعدم التوافق. يعرض هذا التقرير منطقة العزل المعينة ومعلومات حول الاستخدام لتقديم إرشادات حول كيفية معالجة المواد المعيبة. وقد تتطابق مناطق العزل مع مواقع المخزون أو موارد العمليات.

## <a name="examples-of-quarantine-zones"></a>أمثلة لمناطق العزل

### <a name="example-1"></a>مثال1

أنت تعمل في شركه تصنيع الكترونيات التي تقوم بإنتاج أجهزه التلفزيون ومكبرات الصوت ومشغلات الوسائط وتوزيعها. في هذه الحالة، يمكنك تكوين منطقه فحص لتمثل كل نوع من أنواع المنتجات.

### <a name="example-2"></a>مثال2

يتم استخدام ثلاثه حاويات والحاملين لتخزين الأصناف غير المتوافقة. في هذه الحالة، يمكنك تكوين خمسه مناطق فحص، واحده لكل حاويه وكل حامل.

## <a name="create-a-quarantine-zone"></a>إنشاء منطقة عزل

1. انتقل إلى **إدارة المخزون \> الإعداد \> إدارة الجودة \> مناطق العزل**.
1. في جزء الإجراءات، حدد **جديد** لإضافة صف إلى الشبكة. ثم قم بتعيين الحقول التالية للصف الجديد:

    - **منطقة العزل** – أدخل معرفا فريدا أو اسما فريدا لمنطقة العزل.
    - **الوصف** - أدخل وصفًا مفصلاً لمنطقة العزل.

1. قم بإغلاق الصفحة.

## <a name="additional-resources"></a>الموارد الإضافية

- [نظرة عامة على إدارة الجودة](quality-management-processes.md)
- [تمكين إدارة عدم المطابقة والجودة](enable-quality-management.md)
- [العاملون المسؤولون عن الموافقة على حالات عدم المطابقة](quality-responsible-workers.md)
- [أنواع المشكلات لحالات عدم المطابقة](quality-quarantine-zones.md)
- [أنواع التشخيص لحالات عدم المطابقة](quality-diagnostic-types.md)
- [مصاريف الجودة لحالات عدم المطابقة](quality-charges.md)
- [عمليات حالات عدم المطابقة](quality-operations.md)
- [إدارة الجودة لعمليات المستودعات](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
