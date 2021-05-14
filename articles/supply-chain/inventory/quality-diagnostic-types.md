---
title: أنواع التشخيص لحالات عدم المطابقة
description: يوضح هذا الموضوع كيفيه استخدام وإنشاء أنواع التشخيصات التي يمكن استخدامها مع حالات عدم التوافق.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestDiagnosticType, InventTestCorrection
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 19fcd57e28efabd6ca32c444ab961b876bde424d
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956528"
---
# <a name="diagnostic-types-for-nonconformances"></a>أنواع التشخيص لحالات عدم المطابقة

[!include [banner](../includes/banner.md)]

يوضح هذا الموضوع كيفيه استخدام وإنشاء أنواع التشخيصات التي يمكن استخدامها مع حالات عدم التوافق.

يمكنك استخدام صفحة **أنواع التشخيص** لتحديد تصنيف إجراءات التشخيص. وبعد ذلك، عندما تقوم بإنشاء تصحيح لعدم توافق، فانك تقوم بتحديد تشخيص. يحدد التصحيح نوع إجراء التشخيص الذي ينبغي القيام به لحالة عدم مطابقة معتمدة، وكذلك الشخص الذي ينبغي عليه القيام بالإجراء. ويحدد أيضًا تاريخ الاكتمال المطلوب وتاريخ الاكتمال المخطط له.

## <a name="examples-of-diagnostic-types"></a>أمثلة على أنواع التشخيص

لقد قمت بالعمل لشركه تصنيع، وإذا فشلت العديد من الأصناف في اختبارات جوده فاشله. يتم نقل هذه الأصناف إلى منطقه الفحص وتمييزها كمنتجات غير متوافقة. يتم إنشاء سجل عدم توافق في Microsoft Dynamics 365 Supply Chain Management لتتبع التفاصيل من خلال حل المشكلة.

في هذه الحالة، تحدث مشكلات الجودة بسبب بيرينجس في الجهاز والتي اختفت في حزم الأصناف وأوفيرهياتينجها. والتصحيح الخاص بهذه المشكلة هو استبدال الأجزاء الموجودة في الجهاز.

عند تكوين أنواع التشخيص، يمكنك إنشاء سجلات متعددة، يمثل كل منها نوعا مختلفا من المشكلات التي قد يمتلكها الجهاز. بدلا من ذلك، يمكنك إنشاء نوع تشخيص عام واحد يمثل إصلاح الجهاز.

## <a name="create-a-diagnostic-type"></a>إنشاء نوع تشخيص

1. انتقل إلى **إدارة المخزون \> الإعداد \> إدارة الجودة \> أنواع التشخيص**.
1. في جزء الإجراءات، حدد **جديد** لإضافة صف إلى الشبكة. ثم قم بتعيين الحقول التالية للصف الجديد:

    - **التشخيص** – أدخل معرفًا فريدًا أو اسمًا لنوع التشخيص.
    - **الوصف** - أدخل وصفًا مفصلاً لنوع التشخيص.

1. قم بإغلاق الصفحة.

## <a name="additional-resources"></a>الموارد الإضافية

- [نظرة عامة على إدارة الجودة](quality-management-processes.md)
- [تمكين إدارة عدم المطابقة والجودة](enable-quality-management.md)
- [العاملون المسؤولون عن الموافقة على حالات عدم المطابقة](quality-responsible-workers.md)
- [مناطق العزل لحالات عدم المطابقة](quality-quarantine-zones.md)
- [أنواع المشكلات لحالات عدم المطابقة](quality-problem-types.md)
- [مصاريف الجودة لحالات عدم المطابقة](quality-charges.md)
- [عمليات حالات عدم المطابقة](quality-operations.md)
- [إدارة الجودة لعمليات المستودعات](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
