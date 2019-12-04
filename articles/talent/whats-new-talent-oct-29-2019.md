---
title: ما الجديد أو المتغير في Dynamics 365 Talent‏ (29 أكتوبر 2019)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 10/29/2019
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
ms.search.validFrom: 2019-10-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 83b4734190163ebd2dc29096632642bd45c61e8f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773867"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-29-2019"></a>ما الجديد أو المتغير في Dynamics 365 Talent‏ (29 أكتوبر 2019)

[!include [banner](includes/banner.md)]

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Dynamics 365 Talent.

## <a name="changes-in-attract"></a>التغييرات في Attract

يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>التغييرات في Onboard

يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>التغييرات في Core HR

تنطبق التغييرات التي ورد وصفها في هذا القسم على الإصدار رقم 8.1.2586. تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام الدعم في Microsoft Dynamics Lifecycle Services (LCS).

### <a name="delete-parties-with-no-roles-should-be-on-by-default-371233"></a>يجب أن يتم حذف الأطراف التي ليس لها أدوار افتراضيًا (371233)

عند توفير بيئة جديده في Talent، **احذف الأطراف في حاله عدم وجود أي أدوار** قيد التشغيل افتراضيا. عندما تقوم بحذف عامل ، لا تتم أزاله الطرف المقترن بالعامل ما لم يكن هذا الاعداد قيد التشغيل. يحد هذا التغيير من السجلات المكررة في دفتر العناوين العام عندما تحتاج إلى استيراد العمال أو تغييرهم أو إعادة استيرادهم.

### <a name="draft-and-cancelled-leave-requests-should-be-allowed-to-be-deleted-in-common-data-service-376999"></a>يجب السماح بحذف طلبات المسودة وطلبات المغادرة الملغية في Common Data Service (376999)

بهذا التغيير، يمكنك الآن حذف طلبات الاجازه التي بحالة **مسودة** أو **تم الإلغاء** في Common Data Service.

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a>لا تنعكس قيم القائمة الاضافيه في الحقول المخصصة في Common Data Service بعد النقر فوق تطبيق على نموذج الحقول المخصصة (379599)

عند أضافه قيم قائمه جديده إلى حقل مخصص موجود تمت مزامنته بالفعل مع Common Data Service، تكون الآن متاحه في Common Data Serivce بعد تطبيق تغييراتك في نموذج **الحقول المخصصة**.

### <a name="apply-onboarding-checklists-across-legal-entities-when-more-than-one-employment-exists-371270"></a>تطبيق قوائم الاختيار الخاصة بإلحاق عبر الكيانات القانونية عندما يوجد أكثر من توظيف واحد (371270)

في الإصدار الخاص بهذا الأسبوع، يمكنك تطبيق قوائم الاختيار للموظفين الذين لديهم أكثر من توظيف واحد في **نموذج العامل > قوائم الاختيار**.

### <a name="benefits-open-enrollment-preview-feature-has-been-removed"></a>تمت إزالة الميزات التي تفتح ميزة معاينة التسجيل

بالتزامن مع إعلاننا الخاص [بالاستثمارات الاستراتيجية المنشور في مدونة التفوق العملي لتحسين core HR](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence)، عملت Microsoft على إزالة الميزات التي تفتح ميزة التسجيل المعاينة العامة. سيتم إصدار وظيفة جديدة في المستقبل. استخدام الإنتاج للميزات التي تفتح ميزة التسجيل غير مدعوم

## <a name="coming-soon"></a>قريبًا

### <a name="print-performance-reviews"></a>طباعة مراجعات الأداء

راجع [‏‫طباعة مراجعات الأداء‬](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) في خطة الموجة 2 من إصدار Dynamics 365: 2019.

### <a name="feature-management-workspace"></a>مساحة عمل إدارة الميزات

تتم إضافة ميزات وتحديثها في كل إصدار. وتوفر تجربة إدارة الميزات مساحة عمل حيث يمكنك عرض قائمه بالميزات التي تم تقديمها في كل إصدار. بشكل افتراضي، تكون الميزات الجديدة متوقفة عن التشغيل. ويمكنك استخدام مساحة العمل لتشغيلها وعرض الوثائق الخاصة بها.

لمعرفة المزيد حول التغييرات المصاحبة لإدارة الميزات، راجع [نظرة على إدارة الميزات‬](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).
