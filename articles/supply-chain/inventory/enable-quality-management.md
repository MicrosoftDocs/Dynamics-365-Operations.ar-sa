---
title: تمكين إدارة عدم المطابقة والجودة
description: يقدم هذا الموضوع نظرة عامة حول عملية إعداد وتكوين ميزات إدارة الجودة وعدم المطابقة في Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome, InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 67d5da648e31d07d054246f5d308a6c6cdeb506c
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956244"
---
# <a name="enable-quality-and-nonconformance-management"></a>تمكين إدارة عدم المطابقة والجودة

[!include [banner](../includes/banner.md)]

يقدم هذا الموضوع نظرة عامة حول عملية إعداد وتكوين ميزات إدارة الجودة وعدم المطابقة في Microsoft Dynamics 365 Supply Chain Management.

## <a name="enable-quality-and-nonconformance-management"></a><a name="enable-qm"></a>تمكين إدارة عدم المطابقة والجودة

اتبع هذه الخطوات لتمكين إدارة الجودة على نظامك.

1. انتقل إلى **إدارة المخزون \> إعداد \> معلمات إدارة المخزون والمستودع**.
1. في علامة التبويب **إدارة الجودة**، قم بتعيين خيار **استخدام إدارة الجودة** إلى *نعم*.
1. وفي حقل **الأجر بالساعة**، أدخل أجر عامل بالساعة بالعملة المحلية. ويتم استخدام الأجر بالساعة لحساب تكاليف العمليات المرتبطة بعدم المطابقة. ويوفر حقلا الأجر بالساعة والتكاليف المحسوبة معلومات مرجعية لعدم المطابقة. ولا يتفاعلا مع الوظائف الأخرى.
1. تحديد **إعداد التقرير**.
1. أضف سطورًا جديدة لأنواع التقارير المختلفة، وحدد نوع المستند المراد استخدامه لكل تقرير.
1. قم بإغلاق الصفحة.
1. قم بإغلاق الصفحة.

## <a name="quality-management-configuration-process"></a>عملية تكوين إدارة الجودة

قبل أن تتمكن من البدء في استخدام ميزات إدارة الجودة وإنشاء أوامر الجودة، يجب عليك تكوين النظام والمتطلبات الأساسية. فيما يلي قائمة بالخطوات المطلوبة لتكوين إدارة الجودة.

1. [تمكين إدارة عدم المطابقة والجودة](#enable-qm).
1. اختياري: [تكوين مستندات الاختبار](quality-test-instruments.md).
1. [تكوين الاختبارات](quality-tests.md).
1. [تكوين متغيرات الاختبار ونتائجه](quality-test-variables.md).
1. [تكوين مجموعات الاختبار](quality-test-groups.md).
1. اختياري: [تكوين مجموعات الجودة والارتباط بالمنتجات](quality-groups.md).
1. اختياري: [تكوين عمليات إقران الجودة](quality-associations.md).

بعد اكتمال التكوين، يمكنك البدء في إنشاء أوامر الجودة ومعالجتها. لمزيد من المعلومات حول كيفية إنشاء أوامر الجودة والعمل معها، راجع [أوامر الجودة](quality-orders.md).

## <a name="nonconformance-management-configuration-process"></a>عملية تكوين إدارة عدم المطابقة

قبل أن تتمكن من البدء في استخدام ميزات إدارة عدم المطابقة وإنشاء حالات عدم المطابقة، يجب عليك تكوين النظام والمتطلبات الأساسية. فيما يلي قائمة بالخطوات المطلوبة لتكوين إدارة عدم المطابقة.

1. [تمكين إدارة عدم المطابقة والجودة](#enable-qm).
1. [تكوين العاملين المسؤولين عن الموافقة على حالات عدم المطابقة](quality-responsible-workers.md).
1. [تكوين أنواع المشكلات](quality-problem-types.md).
1. [تكوين مناطق العزل](quality-quarantine-zones.md).
1. [تكوين أنواع التشخيص](quality-diagnostic-types.md).
1. [تكوين العمليات](quality-operations.md).
1. اختياري: [تكوين تكاليف الجودة](quality-charges.md).

بعد اكتمال التكوين، يمكنك البدء في إنشاء حالات عدم المطابقة ومعالجتها. لمزيد من المعلومات حول كيفية إنشاء والعمل مع عدم المطابقة، راجع [إنشاء حالات عدم المطابقة ومعالجتها](tasks/create-process-non-conformance.md).

## <a name="additional-resources"></a>الموارد الإضافية

- [نظرة عامة على إدارة الجودة](quality-management-processes.md)
- [تمكين إدارة عدم المطابقة والجودة](enable-quality-management.md)
- [إدارة الجودة لعمليات المستودعات](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
