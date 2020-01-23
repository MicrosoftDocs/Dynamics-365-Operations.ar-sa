---
title: ما الجديد أو المتغير في Dynamics 365 for Talent‏ (10 سبتمبر 2019)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 9/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-09-10
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 14e3482f366319851bed84b6cdd6135f0bcd1e80
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897318"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-september-10-2019"></a>ما الجديد أو المتغير في Dynamics 365 for Talent‏ (10 سبتمبر 2019)

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>التغييرات في Attract

### <a name="candidate-e-mail-login"></a>تسجيل الدخول باستخدام البريد الكتروني للمرشح

الآن يمكن للترشيحين استخدام أي عنوان بريد إلكتروني لإنشاء حساب وتسجيل الدخول إلى موقع وظائف Talent للتقدم للوظائف والبحث عن حالة استمارة التقديم الخاصة بهم. هذا بالإضافة إلى إمكانية تسجيل الدخول بالفعل إلى موقع وظائف Talent باستخدام الحسابات الاجتماعية أو بيانات اعتماد المؤسسة الخاصة بهم.

### <a name="job-activation-and-posting"></a>تنشيط الوظيفة وترحيلها

قمنا بإجراء تغييرات قليلة على تنشيط الوظيفة وترحيلها. يجب تنشيط الوظائف قبل ترحيلها إلى موقع وظائف Talent أو إلى أي من لوحات الوظائف الخارجية، بما في ذلك LinkedIn أو Broadbean.

## <a name="changes-in-onboard"></a>التغييرات في Onboard

يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>التغييرات في Core HR

تنطبق التغييرات التي ورد وصفها في هذا القسم على الإصدار رقم 8.1.2482. تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام الدعم في Microsoft Dynamics Lifecycle Services (LCS).

### <a name="you-can-enable-preview-features-in-sandbox-and-trial-environments"></a>يمكنك تمكين ميزات المعاينة في ‏‫بيئة الاختبار المعزولة‬ والبيئات التجريبية

عند توفير مثيل جديد من Talent‬، يمكنك تحديد ما إذا كان نوع المثيل هو إنتاج أو بيئة اختبار معزولة. تسمح أنواع مثيلات بيئة اختبار معزولة بالاختبار المبكر للميزات الجديدة. إذا كنت ترغب في تحديث أحد المثيلات الموجودة لديك إلى نوع مثيل بيئة الاختبار المعزولة، اتصل بـ الدعم لبدء طلب التغيير.

لمزيد من المعلومات حول كيفية نشر التغييرات، راجع [توفير Talent‬](./provisioning-talent.md).

### <a name="platform-update-29"></a>update 29 للنظام الأساسي

للحصول على مزيد من التفاصيل حول Platform update 29، راجع [ميزات المعاينة في Dynamics 365 for Finance and Operations platform update 29 (أكتوبر 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-29).

### <a name="new-job-base-entity-available-in-data-management-framework-347202"></a>يتوفر كيان أساسي جديد للوظائف في إطار عمل إدارة البيانات (347202)

ومع هذا الإصدار، يتوفر كيان وظائف أساسية جديد لاستيراد/تصدير البيانات. 

### <a name="worker-advanced-security-policy-incorrectly-displays-positions-in-position-hierarchy-354868"></a>تعرض سياسة الأمان المتقدمة للعاملين المناصب بشكل غير صحيح في التدرج الهرمي للمنصب (354868)

وبهذا الإصدار، لن تُعرض المناصب عامل "مفتوح مع "فارغ" عندما يكون للمستخدم صلاحية وصول مقيدة.

### <a name="job-form-close-box-wont-close-form-in-certain-situations-342467"></a>لن يغلق صندوق غلق المهمة نموذج الغلق في مواقف معينة (342467)

يتضمن هذا الإصدار تغييرًا يتيح إغلاق نموذج الوظيفة في جميع السيناريوهات.

### <a name="new-case-on-employee-record-is-locked-for-human-resources-manager-role-337111"></a>تم تأمين حالة جديدة في سجل الموظف لدور إدارة الموارد البشرية (337111)

ومن خلال هذا التغيير، لا يصبح نموذج إدارة الحالات مؤمنًا عند الوصول إليه من نموذج الموظف.

### <a name="employment-end-date-always-defaults-to-235959-351492"></a>دائمًا ما يكون تاريخ انتهاء التوظيف معيًنا على الإعدادات الافتراضية إلى 23:59:59 (351492)

ومع هذا التغيير، يمكنك تغيير تاريخ التوظيف إلى وقت آخر بخلاف 23:59:59 عند إنهاء توظيف يدويًا.

### <a name="unable-to-set-up-expiration-date-on-an-earning-code-through-data-management-336604"></a>غير قادر على إعداد تاريخ انتهاء الصلاحية على كود أرباح من خلال إدارة البيانات (336604)

في هذا الإصدار، يمكنك إعداد أكواد الإرباح التي تنتهي صلاحيتها من خلال الكيان **PayrollWorkerPositionEarningCodeEntity**.

### <a name="employee-development-analytic-report-doesnt-display-data-348737"></a>لا يعرض التقرير التحليلي لتطوير الموظفين البيانات (348737)

في إصدار هذا الأسبوع، تم تحديث التحليلات الخاصة بمهارات الموظف لتوفير تقارير دقيقة.

### <a name="terms-of-employment-datetime-dont-default-to-beginning-of-day-349101"></a>لا يمكن إعداد شروط تاريخ/وقت التوظيف إلى الإعداد الافتراضي في بداية اليوم (349101)

بهذا التغيير، يتم الآن تعيين تاريخ/وقت البدء افتراضيًا لبداية اليوم وإعداد تاريخ/وقت الانتهاء افتراضيًا لنهاية اليوم.

### <a name="changing-the-employment-end-date-on-worker-action-form-displays-an-error-354092"></a>يؤدي تغيير تاريخ نهاية التوظيف في نموذج إجراء العامل إلى عرض خطأ (354092) 

يعمل هذا التغيير على تصحيح مشكلة عند تعديل تاريخ انتهاء التوظيف كجزء من إجراء العامل.

### <a name="applying-onboarding-checklists-across-companies-338433"></a>تطبيق قوائم الاختيار الخاصة بالإلحاق عبر الشركات (338433)

يوفر هذا الإصدار الآن القدرة على تطبيق قوائم الاختيار للموظفين الذين تم توظيفهم في كيانات قانونية غير الكيان القانوني الذي تم تسجيل الدخول إليه.

## <a name="in-preview"></a>قيد المعاينة

### <a name="streamlined-employee-entry-and-navigation"></a>إدخال الموظفين والتنقل المبسط

تتوفر هذه الوظيفة الآن في بيئات الاختبار المعزولة. لتشغيل هذه الميزة، انتقل إلى **إدارة النظام > الارتباطات > الإعداد > محددات النظام‬ > ميزات المعاينة‬**. حدد **نموذج العامل المحسن والتنقل‬**. سيؤدي ذلك إلى تمكين هذه التغييرات لكافة المستخدمين. يمكنك إيقاف تشغيل هذا الخيار في اي وقت.

لمزيد من المعلومات، راجع [إدخال الموظفين والتنقل المبسط‬](./streamlined-employee-entry.md).
