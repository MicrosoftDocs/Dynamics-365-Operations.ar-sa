---
title: ما الجديد أو المتغير في Dynamics 365 Talent‏ (3 ديسمبر 2019)
description: يصف هذا المقال الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 12/03/2019
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
ms.search.validFrom: 2019-12-03
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b1ed998302762203bad736161a27a48152de65f7
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897708"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-december-3-2019"></a>ما الجديد أو المتغير في Dynamics 365 Talent‏ (3 ديسمبر 2019)

تصف هذه المقالة الميزات الجديدة أو المتغيرة في Dynamics 365 Talent.

## <a name="changes-in-attract"></a>التغييرات في Attract

يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>التغييرات في Onboard

يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>التغييرات في Core HR

تنطبق التغييرات التي ورد وصفها في هذا القسم على الإصدار رقم 8.1.2646. تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام الدعم في Microsoft Dynamics Lifecycle Services (LCS).

### <a name="feature-management-workspace"></a>مساحة عمل إدارة الميزات

توفر مساحة عمل **إدارة الميزات** قائمة بالميزات التي يتم تسليمها في كل إصدار. بشكل افتراضي، تكون الميزات الجديدة متوقفة عن التشغيل. ويمكنك استخدام مساحة العمل لتشغيلها وعرض الوثائق الخاصة بها. لمزيد من المعلومات حول إدارة الميزات، راجع [نظرة عامة على إدارة الميزات](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

تبقي كافة الميزات الجديدة في معاينه لمده 30 يوما علي الأقل ، وبشكل نموذجي 30-60 يوما. تتوفر الميزات الرئيسية بشكل عام في أكتوبر و ابريل من كل عام يتبع فتره المعاينة. بمجرد ان تشاهد إمكانيات جديده في مساحة عمل **إدارة الميزات**، يمكنك تشغيلها. قد تكون بعض الميزات قيد التشغيل بشكل افتراضي.
 
في بعض الأوقات، سيتم تشغيل ميزه متكاملة بشكل افتراضي ولا يمكن إيقاف تشغيلها (على سبيل المثال مساحة عمل **إدارة الميزات**).
 
وبمجرد توفر إحدى الميزات بصفه عامه ، قد يتم تشغيلها أو إيقاف تشغيلها في بيئات الإنتاج. وتشير مساحة عمل **إدارة الميزات** إلى ان ميزه المعاينة ستصبح إلزاميه. وعاده ما يكون هذا التاريخ في يوم 1 أكتوبر أو 1 إبريل لكي تتم محاذاته مع خطط الإصدار نصف السنوية. لا يمكنك إيقاف تشغيل الميزات الإلزامية. وحتى تصبح إلزاميا، يمكنك تشغيل أحدي الميزات وإيقاف تشغيلها في كافة البيئات.

### <a name="add-automatic-scheduling-of-batch-job-history-cleanup-332528"></a>إضافة جدولة تلقائية لمسح محفوظات الوظيفة الدفعية (332528)

مع هذا التغيير، تعمل **محفوظات الوظيفة الدفعية** كل ليلة وتزيل أصناف محفوظات الوظيفة الدفعية الأقدم من 30 يومًا.

### <a name="talent-doesnt-respond-in-worker-actions-when-identification-number-length-doesnt-match-the-identification-type-390971"></a>لا يستجيب Talent لإجراءات العاملين عندما لا يتطابق طول رقم الهوية مع نوع التعريف (390971)

يقوم هذا الإصدار بتصحيح المشكلة التي ظهرت عندما لا يتطابق طول رقم الهوية مع التعريف ضمن نوع الهوية. 

### <a name="fixed-compensation-doesnt-update-level-with-changes-to-position-details--348085"></a>لا يقوم التعويض الثابت بتحديث المستوى مع التغييرات لتفاصيل المناصب (348085)

في إصدار هذا الأسبوع، يحدد **تاريخ بدء التعويض** الوظيفة المقترنة بالمنصب عند تلك النقطة في وقت إنشاء سجل تعويض ثابت جديد لموظف ما.

### <a name="workers-employees-and-contractors-lists-show-worker-type-as-both-when-they-should-only-be-worker-or-contractor-384473"></a>تظهر قوائم العمال والموظفين والمقاولين نوع العامل ككلاهما عندما يجب أن تكون فقط العامل أو المقاول (384473)

يعكس هذا التغيير بدقه نوع العامل الذي تم إدخاله (المقاول أو الموظف).

### <a name="email-notifications-for-new-hire-actions-dont-contain-name-information-due-to-security-policies-383402"></a>لا تحتوي إخطارات البريد الإلكتروني لإجراءات التوظيف الجديدة على معلومات الاسم بسبب سياسات الأمان (383402)

يعمل هذا التغيير على تصحيح المعلومات المعروضة في الحقلين الأول أو الكنية ضمن العناصر النائبة لسير العمل عند تمكين الأمان المتقدم.

### <a name="system-allows-two-full-day-leave-requests-for-the-same-day-379284"></a>يسمح النظام بطلبين أجازة لمدة يوم كامل في اليوم نفسه (379284)

ومع هذا التغيير، يتعذر عليك إصدار طلبي أجازة لليوم نفسه. 

### <a name="address-changes-list-should-be-sorted-by-effective-date-352798"></a>يجب أن يتم فرز قائمة تغييرات العنوان حسب تاريخ السريان (352798)

مع هذا التغيير، يتم الآن فرز قائمة تغيير العنوان حسب **تاريخ السريان**.

### <a name="leave-requests-should-allow-deletes-from-common-data-service-to-talent-376999"></a>يجب أن تسمح طلبات الأجازة بعمليات الحذف من Common Data Service إلى Talent (376999)

مع هذا التغيير، يمكن حذف طلبات المسود وطلبات الإجازات الملغية من Common Data Service ثم ازالتها من Talent.

### <a name="delete-earning-codes-is-allowed-when-the-same-earning-code-is-assigned-to-an-employee-371792"></a>يتم السماح بحذف أكواد الأرباح عندما يتم تعيين كود الربح نفسه لموظف (371792)

في هذا الإصدار، يجب أولاً إزالة كود الربح من الموظف قبل حذف كود الربح من النظام.

### <a name="leave-and-absence-workflow-with-two-approval-stages-fails-to-complete--391116"></a>فشل إكمال سير العمل في الأجازة والغياب في مرحلتي اعتماد (391116)

مع هذا التغيير، يستمر سير العمل الخاص بالأجازة والغياب من خلال كافة الخطوات عندما يتم تكوين أكثر من مرحلة اعتماد واحدة للطلب.

### <a name="issue-date-doesnt-sync-to-common-data-service-when-updated-or-entered-in-talent-397361"></a>لا يتم مزامنة تاريخ الإصدار لـ Common Data Service عند تحديثه أو إدخاله في Talent (397361)

يعمل هذا التغيير على تصحيح مشكلة حيث لم يتم مزامنة تاريخ الإصدار لسجلات **هوية الشخص** لـ Common Data Service من Talent.

### <a name="hierarchy-circular-reference-error-issued-when-assigning-a-manager-to-a-position-386659"></a>تم إصدار خطأ مرجع دائري للتدرج الهرمي عند تعيين مدير في منصب (386659)

يعمل هذا التغيير على تصحيح سيناريو فريد حيث يظهر خطأ مرجع دائري عند تعيين مدير جديد في منصب.

### <a name="common-data-service-entities-that-now-support-custom-fields"></a>كيانات Common Data Service التي تدعم الآن الحقول المخصصة

تدعم كيانات Common Data Service التالية الحقول المخصصة الآن:

| الاسم | الكيان |
| --- | --- |
| مصروف الحساب البنكي | cdm_bankaccountdisbursement |
| تكرار حساب الميزة | cdm_benefitcalculationfrequency |
| حساب تكرار فترة دفع الميزة | cdm_benefitcalculationfrequencypayperiod |
| معدل حساب الميزة | cdm_benefitcalculationrate |
| تفاصيل معدل حساب الميزة | cdm_benefitcalculationratedetail |
| خيار الميزة | cdm_benefitoption |
| خطة الميزة | cdm_benefitplan (غير ممكّن‬ لدعم الحقل المخصص) |
| نوع الميزة | cdm_benefittype |
| تقويم عملية الأعمال | cdm_businessprocesscalendar |
| تعيين مجموعة عمليات الأعمال | cdm_businessprocessgroupassignment |
| مجموعة مهام مكتبة عمليات الأعمال | cdm_businessprocesslibrarytaskgroup |
| مرحلة عملية الأعمال‬ | cdm_businessprocessstage |
| رأس قالب قائمة الاختيار | cdm_businessprocesstemplateheader |
| مهمة قالب قائمة الاختيار | cdm_businessprocesstemplatetask |
| الشركة | cdm_company |
| الخطة الثابتة للتعويض | cdm_compensationfixedplan |
| شبكة التعويض | cdm_compensationgrid |
| مستوى التعويض | cdm_compensationlevel |
| تكرار دفع التعويض | cdm_compensationpayfrequency |
| إعداد النقاط المرجعية للتعويض | cdm_compensationreferencepointsetup |
| إعداد بند النقاط المرجعية للتعويض | cdm_compensationreferencepointsetupline |
| منطقة التعويض | cdm_compensationregion |
| بنية التعويض | cdm_compensationstructure |
| خطة التعويض المتغير | cdm_compensationvariableplan |
| مستوى خطة التعويض المتغير | cdm_compensationvariableplanlevel |
| نوع خطة التعويض المتغير | cdm_compensationvariableplantype |
| قسم | cdm_department |
| التوظيف | cdm_employment |
| الأصل العرقي | cdm_ethnicorigin |
| حدث التعويض الثابت | cdm_fixedcompensationevent |
| وظيفة | cdm_job |
| مهمة الوظيفة | cdm_jobfunction |
| منصب الوظيفة | cdm_jobposition |
| نوع الوظيفة | cdm_jobtype |
| اللغة | cdm_language |
| حركة أجازة البنك | cdm_leavebanktransaction |
| تسجيل الأجازة | cdm_leaveenrollment |
| خطة الإجازة | cdm_leaveplan |
| طلب الإجازة | cdm_leaverequest |
| تفاصيل طلب المستخدم | cdm_leaverequestdetail |
| نوع الإجازة | cdm_leavetype |
| كود سبب نوع الإجازة‬ | cdm_leavetypereasoncode |
| دورة الدفع | cdm_paycycle |
| فترة الدفع | cdm_payperiod |
| كود أرباح كشف الرواتب | cdm_payrollearningcode |
| وكاله إصدار الهوية الشخصية | cdm_personidentificationissuingagency |
| نوع المنصب | cdm_positiontype |
| تعيين العامل بالمنصب | cdm_positionworkerassignmentmap |
| كود السبب | cdm_reasoncode |
| نوع المهارة | cdm_skilltype |
| منطقة الضريبة | cdm_taxregion |
| قاعدة الاستحقاق | cdm_vestingrule |
| حالة الخبير | cdm_veteranstatus |
| تقويم العمل | cdm_workcalendar |
| يوم تقويم العمل | cdm_workcalendarday |
| إجازة تقويم العمل |cdm_workcalendarholiday |
| بند أجازة تقويم العمل | cdm_workcalendarholidayline |
| الفاصل الزمني لتقويم العمل | cdm_workcalendartimeinterval (غير ممكّن‬ لدعم الحقل المخصص) |
| العامل | cdm_worker |
| عنوان العامل | cdm_workeraddress |
| الحساب البنكي للعامل | cdm_workerbankaccount |
| التعويض الثابت للعامل | cdm_workerfixedcompensation |
| التفاصيل الشخصية للعامل | cdm_workerpersonaldetail |
| رقم الهوية الشخصية للعامل | cdm_workerpersonidentificationnumber |
| نوع الهوية الشخصية للعامل | cdm_workerpersonidentificationtype |

## <a name="in-preview"></a>قيد المعاينة

ستتوافر ميزات المعاينة في بيئات **الاختبار المعزولة** فقط.

### <a name="print-performance-reviews"></a>طباعة مراجعات الأداء

راجع [‏‫طباعة مراجعات الأداء‬](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) في خطة الموجة 2 من إصدار Dynamics 365: 2019.
