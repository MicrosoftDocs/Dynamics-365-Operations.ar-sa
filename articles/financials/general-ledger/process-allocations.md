---
title: "توزيعات العمليات"
description: "توفر هذه المقالة معلومات حول عمليات التخصيص والخيارات الخاصة بمعالجتها في Microsoft Dynamics 365 for Finance and Operations, Enterprise edition وكيف يمكن استخدامها في تخطيط الموازنة. تستخدم عمليات التخصيص لتوزيع مبالغ عبر مجموعات متعددة من حسابات دفتر الأستاذ. وهي تساعد على ضمان تحميل النفقات أو الإيرادات للكائن الصحيح في المحاسبة."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 298ac47e2253f8add1aa3938dda15afe186afbeb
ms.openlocfilehash: e6d88503972850f6163aba6b45547a111f44abab
ms.contentlocale: ar-sa
ms.lasthandoff: 06/20/2017


---

# <a name="process-allocations"></a>توزيعات العمليات

[!include[banner](../includes/banner.md)]


توفر هذه المقالة معلومات حول عمليات التخصيص والخيارات الخاصة بمعالجتها في Microsoft Dynamics 365 for Finance and Operations, Enterprise edition وكيف يمكن استخدامها في تخطيط الموازنة. تستخدم عمليات التخصيص لتوزيع مبالغ عبر مجموعات متعددة من حسابات دفتر الأستاذ. وهي تساعد على ضمان تحميل النفقات أو الإيرادات للكائن الصحيح في المحاسبة.

يوفر Microsoft Dynamics 365 for Finance and Operations القدرات التالية لدعم هذه العملية:

-   قم يدويًا بتوزيع مبالغ الحركات باستخدام إجراء التقسيم في التوزيعات المحاسبية، أو عن طريق تطبيق القوالب الافتراضية للأبعاد المالية على مستند. ولمزيد من المعلومات، راجع [التوزيعات المحاسبية.](../accounts-payable/accounting-distributions.md)
-   قم تلقائيًا بتوزيع مبالغ الحركات استناداً إلى مدة التوزيع المحددة في حساب رئيسي فردي. وسيتم إنشاء إدخالات حساب التوزيع لكل دفتر يومية استناداً إلى حساب دفتر أستاذ الوجهة والنسبة المئوية حيث يفي إدخال المحاسبة بالمعايير المحددة باعتبارها حساب دفتر الأستاذ المصدر.
-   قم تلقائيًا بتوزيع أرصدة دفتر الأستاذ أو المبالغ الثابتة استناداً إلى قواعد توزيع دفتر الأستاذ. تتم معالجة قواعد توزيع دفتر الأستاذ على أساس دوري باستخدام دفاتر يومية التوزيع. 

###  <a name="allocations-in-budget-planning"></a>التوزيعات في تخطيط الموازنة

يمكن استخدام قواعد توزيع دفتر الأستاذ لخطط الموازنة. عند استخدام قواعد توزيع دفتر الأستاذ في تخطيط الموازنة، تعمل قواعد التوزيع بنفس الطريقة المتبعة في دفتر الأستاذ، ولكن تأتي البيانات المصدر والبيانات الوجهة من خطة الموازنة. يمكنك تحديد قواعد توزيع دفتر الأستاذ لاستخدامها بخطط الموازنة يدويًا. بدلاً من ذلك، يمكنك استخدام جدول توزيع يتم تشغيله كجزء من عملية سير العمل.

> [!NOTE]
> يمكنك استخدام قواعد توزيع دفتر الأستاذ بين الشركات الشقيقة لتخطيط الموازنة.






