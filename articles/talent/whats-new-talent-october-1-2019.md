---
title: ما الجديد أو المتغير في Dynamics 365 Talent‏ (1 أكتوبر 2019)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 10/01/2019
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
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 69c0a805027f215b2a2a42d826ee7a346cfdd511
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529650"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-1-2019"></a>ما الجديد أو المتغير في Dynamics 365 Talent‏ (1 أكتوبر 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Dynamics 365 Talent.

## <a name="changes-in-attract"></a>التغييرات في Attract

يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>التغييرات في Onboard

يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>التغييرات في Core HR

تنطبق التغييرات التي ورد وصفها في هذا القسم على الإصدار رقم 8.1.2509. تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام الدعم في Microsoft Dynamics Lifecycle Services (LCS).

### <a name="streamlined-employee-entry-and-navigation"></a>إدخال الموظفين والتنقل المبسط

تتوفر هذه الوظيفة الآن في جميع البيئات. لتشغيل هذه الميزة، انتقل إلى **إدارة النظام > الارتباطات > الإعداد > محددات النظام‬ > ميزات المعاينة‬**. حدد **نموذج العامل المحسن والتنقل‬**. سيؤدي ذلك إلى تمكين هذه التغييرات لكافة المستخدمين. يمكنك إيقاف تشغيل هذا الخيار في اي وقت.

لمزيد من المعلومات، راجع [إدخال الموظفين والتنقل المبسط‬](./streamlined-employee-entry.md). لمشاهدة فيديو حول هذه التغييرات، راجع نظرة عامة حول الموجة 2 من إصدار [Dynamics 365 for Talent 2019](https://aka.ms/ROGT19RW2ROV)

### <a name="you-can-enable-preview-features-in-sandbox-and-trial-environments"></a>يمكنك تمكين ميزات المعاينة في ‏‫بيئة الاختبار المعزولة‬ والبيئات التجريبية

عند توفير مثيل جديد من Talent‬، يمكنك تحديد ما إذا كان نوع المثيل هو إنتاج أو بيئة اختبار معزولة. تسمح أنواع مثيلات بيئة اختبار معزولة بالاختبار المبكر للميزات الجديدة. إذا كنت ترغب في تحديث أحد المثيلات الموجودة لديك إلى نوع مثيل بيئة الاختبار المعزولة، اتصل بـ الدعم لبدء طلب التغيير.

لمزيد من المعلومات حول كيفية نشر التغييرات، راجع [توفير Talent‬](./provisioning-talent.md).

### <a name="compensation-date-defaults-to-a-different-date-than-the-position-assignment-337694"></a>القيم الافتراضية لتاريخ التعويض هو تاريخ مختلف عن تعيين المنصب (337694)

يؤدي هذا التغيير إلى تعيين القيم الافتراضية لتاريخ بدء التعويض إلى تاريخ بدء تعيين المنصب.

### <a name="not-able-to-end-compensation-along-with-its-position-assignment-328993"></a>غير قادر على إنهاء التعويض إلى جانب تعيين المنصب (328993)

ومن خلال هذا التغيير ، يمكن إنهاء التعويض عند إنهاء تعيين المنصب باستخدام **إنهاء تعيين** في صفحة **‏‫تعيينات منصب العامل‬** مع وضع إجراءات العاملين‬ في وضع التشغيل.

### <a name="bank-account-validation-requires-routing-and-account-numbers-in-all-locations-340403"></a>تتطلب عملية التحقق من صحة الحساب البنكي أرقام الحساب والتوجيه في كافة المواقع (340403)

باستخدام تغييرات هذا الأسبوع، تمت إضافة خيار تكوين جديد لتعطيل التحقق من صحة **رقم التوجيه** و **رقم الحساب** المطلوب. 

### <a name="attachments-are-not-enabled-in-mss-performance-journals-for-performance-feedback-341794"></a>لم يتم تمكين المرفقات في دفاتر يومية أداء MSS لملاحظات الأداء (341794)

وباستخدام إصدار الأسبوع هذا، يتم تمكين المرفقات لعناصر الملاحظات في صفحة دفتر يومية الأداء.

### <a name="leave-request-details-dont-sync-from-common-data-service-to-talent-369608"></a>تفاصيل طلب الإجازة لا تتزامن من  Common Data Service إلى Talent (369608)

بهذه التغييرات، ستتم مزامنة تفاصيل طلب الإجازة في Common Data Service مرة أخرى إلى Talent.

### <a name="job-description-doesnt-display-for-the-job-in-the-skill-gap-analysis-page-369398"></a>لا يعرض وصف الوظيفة للمهمة في صفحة تحليل المهارات المفقودة (369398)

في إصدار هذا الأسبوع، سيتم عرض الوصف عند تحديد الوظيفة في صفحة **تحليل المهارات المفقودة**.

## <a name="coming-soon"></a>قريبًا

### <a name="print-performance-reviews"></a>طباعة مراجعات الأداء

سيتمكن الموظفون والمديرون وموظفي الموارد البشرية من طباعة مراجعة أداء الموظف.
