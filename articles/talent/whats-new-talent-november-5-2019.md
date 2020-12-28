---
title: ما الجديد أو المتغير في Dynamics 365 Talent‏ (5 نوفمبر 2019)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 11/05/2019
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
ms.search.validFrom: 2019-11-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c4068cf81782d2f9559179b91da31e049c006059
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527110"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-november-5-2019"></a>ما الجديد أو المتغير في Dynamics 365 Talent‏ (5 نوفمبر 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Dynamics 365 Talent.

## <a name="changes-in-attract"></a>التغييرات في Attract

يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>التغييرات في Onboard

يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>التغييرات في Core HR

تنطبق التغييرات التي ورد وصفها في هذا القسم على الإصدار رقم 8.1.2598. تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام الدعم في Microsoft Dynamics Lifecycle Services (LCS).

### <a name="copy-a-core-hr-instance"></a>نسخ مثيل Core HR

في إصدار الأسبوع هذا، يمكنك استخدام Microsoft Dynamics Lifecycle Services (LCS) لنسخ قاعدة بيانات Microsoft Dynamics 365 Talent: Core HR إلى بيئة وضع الحماية. إذا كان لديك بيئة وضع حماية أخرى ، يمكنك أيضًا نسخ قاعدة البيانات من تلك البيئة إلى بيئة وضع حماية مستهدفة. لمزيد من المعلومات، راجع:

- [إدارة البيئة الأوسع](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/broader-environment-management) في Dynamics 365: الخطة 2 لموجة إصدارات لعام 2019

- [نسخ مثيل Core HR](hr-copy-instance.md) وثائق Talent

### <a name="common-data-service-integration-batch-jobs-arent-created-when-common-data-service-integration-is-enabled-388030"></a>لا يتم إنشاء وظائف دفعة تكامل Common Data Service عند تمكين تكامل Common Data Service (388030)

سيقوم هذا التغيير بإنشاء وظائف دفعية لتكامل Common Data Service عند تمكينه.

### <a name="the-hcmpersonimageentity-doesnt-resize-the-person-image-when-uploaded-369469"></a>لا يقوم HcmPersonImageEntity بتغيير حجم صوره الشخص عند تحميلها (369469)

ويغير إصدار هذا الأسبوع كيفيه تغيير حجم الصور للحصول علي أداء أفضل عند استيرادها من خلال أداره البيانات.

### <a name="a-positions-available-for-assignment-date-can-be-earlier-than-the-activation-date-340103"></a>يمكن ان يكون المنصب المتوفر لتاريخ التعيين قبل تاريخ التنشيط (340103)

وبهذا التغيير، سيظهر تحذير إذا قمت بتحديد **متاح لتاريخ التعيين** السابق **لتاريخ تنشيط** المنصب.

### <a name="cant-create-a-compensation-change-request-in-employee-self-service-for-step-based-plans-376872"></a>لا يمكن إنشاء طلب تغيير تعويض في الخدمة الذاتية للموظف للخطط المستندة إلى خطوه (376872)

يعمل هذا الإصدار على تصحيح مشكله عند طلب تغييرات التعويض من خلال الخدمة الذاتية للموظف للخطط المستندة إلى الخطوة. 

### <a name="reason-code-doesnt-sync-to-common-data-service-if-the-description-is-longer-than-30-characters-core-hr-allows-60-352682"></a>لا تتم مزامنة رمز السبب مع Common Data Service الا إذا كان الوصف أطول من 30 حرفا، ويسمح Core HR بـ 60 (352682)

وبهذا التغيير، سيتم تحديث أكواد السبب التي تحتوي على أكثر من 30 حرفًا في Common Data Service. سيتم أيضًا عكس التغييرات التي تم إجراؤها في Common Data Service في Talent.

### <a name="address-integration-from-talent-to-finance-and-operations-351961"></a>تكامل العنوان من Talent إلى Finance and Operations ‏(351961)

يعمل هذا الإصدار على إصلاح مشكلة عدم تحديث العناوين التي تم تحديثها في Talent في Finance and Operations. سيتم تحديث التغييرات التي تتم على كتل العناوين.

## <a name="coming-soon"></a>قريبًا

### <a name="print-performance-reviews"></a>طباعة مراجعات الأداء

راجع [‏‫طباعة مراجعات الأداء‬](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) في خطة الموجة 2 من إصدار Dynamics 365: 2019.

### <a name="feature-management-workspace"></a>مساحة عمل إدارة الميزات

تتم إضافة ميزات وتحديثها في كل إصدار. وتوفر تجربة إدارة الميزات مساحة عمل حيث يمكنك عرض قائمه بالميزات التي تم تقديمها في كل إصدار. بشكل افتراضي، تكون الميزات الجديدة متوقفة عن التشغيل. ويمكنك استخدام مساحة العمل لتشغيلها وعرض الوثائق الخاصة بها.

لمعرفة المزيد حول التغييرات المصاحبة لإدارة الميزات، راجع [نظرة على إدارة الميزات‬](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).
