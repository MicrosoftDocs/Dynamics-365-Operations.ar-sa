---
title: "نقل المخزون مع العمل المقترن في إدارة المستودعات"
description: "يصف هذا الموضوع كيفية إعداد وتطبيق تأكيد انتقاء الأجزاء من جهاز محمول."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: d2db0431a3f749cbdaf35cc5108851f1e116bc96
ms.contentlocale: ar-sa
ms.lasthandoff: 06/20/2017

---

# <a name="movement-of-inventory-with-associated-work-in-warehouse-management"></a>نقل المخزون مع العمل المقترن في إدارة المستودعات

[!include[banner](../includes/banner.md)]

باستخدام نقل المخزون، يمكنك أن تحدد العاملين في المستودع الذين يتم السماح لهم بنقل المخزون المحجوز. من شأن ذلك أن يوفر مرونة في المستودعات المنظمة حيث يمكنك تحديد عدم السماح لعامل باختيار موقع انتقاء جديد لعمل الانتقاء الذي أنشأه. ويسمح أيضًا لمدير المستودع بمراقبة القدرات التي ينبغي أن تكون لدى بعض العاملين ذوي خبرات أقل.

قد تكون المرونة في إدارة العمليات اليومية للعاملين في المستودعات مفيدة في سيناريوهات كتلك التي تلي:

## <a name="scenario-1"></a>السيناريو 1
شركة لديها مساحة استلام صغيرة نسبيًا، وهي مزدحمة بالبالتات والصناديق المخزنة فيها. من المتوقع وصول شحنة كبيرة في اليوم الحالي، لذلك يقرر موظف الاستلام‬ تحرير منطقة الاستلام عن طريق نقل بعض البالتات‬ إلى منطقة إعداد داخلية ثانوية.

## <a name="scenario-2"></a>السيناريو 2
يلاحظ عامل مستودع من ذوي الخبرة فرصة في مستودع ما لتجميع العناصر في مكان واحد بدلاً من تقسيمها عبر 3 مواقع مجاورة يحتوي كل واحد منها على كمية صغيرة. يريد العامل تجميع الكمية عن طريق نقل العناصر من كل واحد من هذه المواقع إلى الموقع نفسه وإلى لوحة الترخيص نفسها.

## <a name="scenario-3"></a>السيناريو 3
هناك بالتة تنتظر الشحن في موقع إعداد، مثل STAGE01، القريب من BAYDOOR01. ومع ذلك، ونظرًا لتغيير الخطط تم جدولة وصول الشاحنة إلى BAYDOOR04. موظف الشحن يدرك ذلك ويريد التأكد من أن الشاحنة لن تنتظر تحميلها من STAGE01. يقرر موظف الشحن نقل الأصناف في هذه الشحنة من STAGE01 إلى STAGE04، الأقرب إلى الوجهة الجديدة.

### <a name="current-limitations"></a>القيود الحالية

تقتصر عمليات حجز العمل التي يمكنك نقلها على أمر المبيعات وإصدار أمر التحويل واستلام أمر التحويل وأمر الشراء وعمل التزويد.

يتم تقييد نقل الأصناف لمنع تقسيم بنود العمل. وهذا يعني أنه إذا كان لديك بند عمل من 100 قطعة للصنف A من الموقع Loc1، فلن تتمكن من نقل 30 قطعة فقط للصنف A من هناك إلى موقع آخر. قد يؤدي هذا إلى تقسيم بند العمل موجود إلى 30 و70، لأن المواقع باتت الآن مختلفة.

بالنسبة إلى سيناريوهات الإعداد، حيث تم تعيين لوحة الترخيص التي تنقل الأصناف منها أو لوحة الترخيص التي تنقل الأصناف إليها كلوحة الترخيص الهدف‬ لأمر عمل، يسمح فقط بنقل لوحة الترخيص بكاملها لكي لا يتم تقسيم لوحة الترخيص الهدف.
في الوقت الحالي، يتم دعم الحركة المخصصة فقط. وهذا يعني أنك لن تتمكن من نقل المخزون المحجوز من خلال عملية النقل بواسطة عناصر قائمة الجهاز المحمول للقالب.

### <a name="set-up-the-permission-to-move-reserved-inventory-for-individual-workers"></a>إعداد الإذن لنقل المخزون المحجوز لعاملين فرديين

بالنسبة إلى العامل الذي من المفترض أن يسمح له بنقل المخزون المحجوز، حدد خانة الاختيار **السماح بنقل المخزون مع العمل المقترن‬** ضمن **إدارة المستودعات** > **الإعداد** > **العامل**.  

### <a name="backported"></a>الحمل العكسي

تم أيضًا إجراء تحميل عكسي لهذه الميزة إلى Microsoft Dynamics AX 2012 R3 وسيتكون متوفرة كجزء من CU12.
يمكن أيضًا تنزيلها بشكل فردي من خلال رقم قاعدة المعارف 3192548. 

