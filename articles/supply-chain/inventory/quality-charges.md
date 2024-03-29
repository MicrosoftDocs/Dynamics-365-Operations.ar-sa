---
title: رسوم عمليات عدم المطابقة
description: يوضح هذا المقال كيفيه إنشاء مصاريف الجودة التي يمكن استخدامها مع العمليات الخاصة بعدم التوافق.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestMiscCharges
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 29520afca07adee49846d1be987685a1ece8283c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850717"
---
# <a name="charges-for-nonconformance-operations"></a>رسوم عمليات عدم المطابقة

[!include [banner](../includes/banner.md)]

يوضح هذا المقال كيفيه إنشاء مصاريف الجودة التي يمكن استخدامها مع العمليات الخاصة بعدم التوافق.

يمكنك استخدام صفحة **رسوم الجودة** لتحديد أنواع الرسوم التي يمكن إضافتها إلى عمليات عدم المطابقة. تمكنك المصاريف من تتبع التفاصيل المتعلقة بالرسوم أو الرسوم التي تدين بها إلى أحد العملاء للمنتجات غير المتوافقة، أو التي يمتلكها المورد بالنسبة للمنتجات غير المتوافقة التي تلقيتها. ويمكن أيضا استخدام المصاريف لتتبع التكاليف المطلوبة للموردين أو الخدمات الخارجية لاجراء أحدي العمليات.

## <a name="examples-of-quality-charges"></a>أمثله لتكاليف الجودة

أنت تعمل لشركه تصنيع. لدي شركتك عقود مع العديد من الموردين. مقاييس العقود التفصيلية هذه للشحن والاضرار وجوده المنتج للأصناف. المثل، يكون لدي العديد من العملاء اتفاقيات مع شركتك حول المرتجعات، والاضرار، وجوده المنتج.

يتم تحديد بنيه الرسوم لكل حاله من الحالات والمحددة في العقد. يمكنك تكوين تكاليف الجودة لتخطيط أنواع مختلفه من المصاريف، مثل *الأضرار* و *الشحنة المتأحرة* و *الجودة*. وبعد ذلك، عند إنشاء عدم التوافق، قم باضافه عمليه واحده أو أكثر. بالنسبة لكل عمليه، حدد **الرسوم** لتحديد التفاصيل المتعلقة بالرسوم.

## <a name="create-a-quality-charge"></a>إنشاء تكلفة جودة

1. انتقل إلى **إدارة المخزون \> الإعداد \> إدارة الجودة \> رسوم الجودة**.
1. في جزء الإجراءات، حدد **جديد** لإضافة صف إلى الشبكة. ثم قم بتعيين الحقول التالية للصف الجديد:

    - **كود المصاريف** – ادخل معرفا فريدا أو اسما فريدا لتكلفه الجودة.
    - **الوصف** - أدخل وصفًا مفصلاً لتكلفة الجودة.

1. قم بإغلاق الصفحة.

## <a name="add-a-quality-charge-to-an-operation-for-a-nonconformance"></a>أضافه تكلفه جوده إلى عمليه عدم توافق

للحصول علي تفاصيل حول كيفيه أضافه عمليات إلى عدم التوافق وتطبيق المصاريف عليها، راجع [عمليات عدم التوافق](quality-operations.md).

## <a name="additional-resources"></a>الموارد الإضافية

- [نظرة عامة على إدارة الجودة](quality-management-processes.md)
- [تمكين إدارة عدم المطابقة والجودة](enable-quality-management.md)
- [العاملون المسؤولون عن الموافقة على حالات عدم المطابقة](quality-responsible-workers.md)
- [مناطق العزل لحالات عدم المطابقة](quality-quarantine-zones.md)
- [أنواع التشخيص لحالات عدم المطابقة](quality-diagnostic-types.md)
- [مصاريف الجودة لحالات عدم المطابقة](quality-charges.md)
- [عمليات حالات عدم المطابقة](quality-operations.md)
- [إدارة الجودة لعمليات المستودعات](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
