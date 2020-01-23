---
title: ما الجديد أو المتغير في Dynamics 365 Talent‏ (10 ديسمبر 2019)
description: يصف هذا المقال الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b4bb599be27e7d97fed1c060f97627c7c6a868e6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915500"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-december-10-2019"></a>ما الجديد أو المتغير في Dynamics 365 Talent‏ (10 ديسمبر 2019)

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Dynamics 365 Talent.

## <a name="changes-in-attract"></a>التغييرات في Attract

يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>التغييرات في Onboard

يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>التغييرات في Core HR

تنطبق التغييرات التي ورد وصفها في هذا القسم على الإصدار رقم 8.1.2660. تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام الدعم في Microsoft Dynamics Lifecycle Services (LCS).

### <a name="feature-management-workspace"></a>مساحة عمل إدارة الميزات

توفر مساحة عمل **إدارة الميزات** قائمة بالميزات التي يتم تسليمها في كل إصدار. بشكل افتراضي، تكون الميزات الجديدة متوقفة عن التشغيل. ويمكنك استخدام مساحة العمل لتشغيلها وعرض الوثائق الخاصة بها. لمزيد من المعلومات حول إدارة الميزات، راجع [نظرة عامة على إدارة الميزات](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

تبقي كافة الميزات الجديدة في معاينه لمده 30 يوما علي الأقل ، وبشكل نموذجي 30-60 يوما. تتوفر الميزات الرئيسية بشكل عام في أكتوبر و ابريل من كل عام يتبع فتره المعاينة. بمجرد ان تشاهد إمكانيات جديده في مساحة عمل **إدارة الميزات**، يمكنك تشغيلها. قد تكون بعض الميزات قيد التشغيل بشكل افتراضي.
 
في بعض الأوقات، سيتم تشغيل ميزه متكاملة بشكل افتراضي ولا يمكن إيقاف تشغيلها (على سبيل المثال مساحة عمل **إدارة الميزات**).
 
وبمجرد توفر إحدى الميزات بصفه عامه ، قد يتم تشغيلها أو إيقاف تشغيلها في بيئات الإنتاج. وتشير مساحة عمل **إدارة الميزات** إلى ان ميزه المعاينة ستصبح إلزاميه. وعاده ما يكون هذا التاريخ في يوم 1 أكتوبر أو 1 إبريل لكي تتم محاذاته مع خطط الإصدار نصف السنوية. لا يمكنك إيقاف تشغيل الميزات الإلزامية. وحتى تصبح إلزاميا، يمكنك تشغيل أحدي الميزات وإيقاف تشغيلها في كافة البيئات.

### <a name="streamlined-worker-form-has-moved-to-the-feature-management-workspace-390583"></a>تم نقل نموذج العامل المبسط إلى مساحة عمل إدارة الميزات (390583)

باستخدام هذا التغيير، يمكن الآن تمكين نموذج العامل المبسط في مساحة عمل **إدارة الميزات**. تم نقل هذه الميزة من نموذج **معلمات النظام** في **إدارة النظام**.

### <a name="prevent-hcmworkerpayrollinfo-records-from-being-written-without-a-worker-value-394526"></a>منع السجلات HcmWorkerPayrollInfo من الكتابة بدون قيمة عامل (394526)

مع هذا الإصدار، لم تعد سجلات **hcmworkerpayrollinfo** منشأة ضمن مرجع العامل في هذا السيناريو. 

### <a name="message-log-associated-to-the-action-isnt-populated-when-the-action-fails-to-complete-374007"></a>لا تتم تعبئة سجل الرسائل المقترن بالإجراء عند فشل الإجراء لإكماله (374007)

يتضمن هذا الإصدار تغييرًا لتعبئة سجل رسائل الإجراء عند فشل إجراء في سيناريوهات معينة. 

### <a name="common-data-service-integration-batch-job-creation-388030"></a>إنشاء وظيفة وظيفة دفعية لتكامل Common data service (388030)

مع هذا التغيير، يتم إنشاء الوظيفة الدفعية لتكامل Common Data Service عند تمكين الخدمة.

### <a name="additional-pick-list-values-to-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a>لا تنعكس قيم قائمة الانتقاء الإضافية في الحقول المخصصة في Common Data Service بعد النقر فوق تطبيق في نموذج الحقول المخصصة (379599)

مع هذا التغيير، تتم الآن مزامنة قيم قائمة الانتقاء الجديدة التي تم إدخالها في Talent لـ Common Data Service عند تطبيق التغييرات الخاصة بك.

### <a name="update-to-common-data-service-for-then-leave-bank-transaction-entity-turns-into-an-insert-on-talent-side-352938"></a>يتحول التحديث إلى Common Data Service بكيان حركة أجازة البنك إلى إدراج في جانب Talent (352938)

يعمل هذا التغيير على تصحيح مشكلة حيث يعمل تحديث حركة أجازة البنك على إنشاء سجل جديد في Talent.

## <a name="in-preview"></a>قيد المعاينة

ستتوافر ميزات المعاينة في بيئات **الاختبار المعزولة** فقط.

### <a name="print-performance-reviews"></a>طباعة مراجعات الأداء

راجع [‏‫طباعة مراجعات الأداء‬](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) في خطة الموجة 2 من إصدار Dynamics 365: 2019.

