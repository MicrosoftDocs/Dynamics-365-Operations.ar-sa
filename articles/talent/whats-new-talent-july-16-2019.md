---
title: ما الجديد والمتغير في Dynamics 365 Talent (16 يوليو 2019)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 07/16/2019
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
ms.search.validFrom: 2019-07-16
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6dce39bc529bf6dd6079ed900af12510c0773f9a
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/06/2019
ms.locfileid: "2899072"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-july-16-2019"></a>ما الجديد والمتغير في Dynamics 365 Talent (16 يوليو 2019)

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent.

## <a name="changes-in-attract"></a>التغييرات في Attract
يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Attract.

### <a name="coming-soon-in-attract"></a>قريبًا في Attract
#### <a name="job-approvals-appear-on-the-home-page"></a>تظهر الموافقات على الوظائف في الصفحة الرئيسية

تظهر الموافقات في قسم **الموافقات** على لوحة المعلومات. يستطيع المعتمدون مراجعة موافقاتهم ضمن **المعينة لك**، التي تعرض معرف الوظيفة والمسمى الوظيفي والمعتمدين الآخرين وتاريخ تعيين الوظيفة. يستطيع المستخدمين الذين يقومون بإرسال وظيفة للاعتماد مراجعة الوظائف الخاصة بهم ضمن **طلبتها**، التي تعرض المعتمدين الذين لا يزالوا يحتاجون إلى اعتماد الوظيفة التي تم إرسالها.

## <a name="changes-in-onboard"></a>التغييرات في Onboard
يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>التغييرات في Core HR
تنطبق التغييرات التي ورد وصفها في هذا القسم على الإصدار رقم 8.1.2390.

### <a name="common-data-service-entities-that-now-support-custom-fields"></a>كيانات Common Data Service التي تدعم الآن الحقول المخصصة

- BusinessProcessCalendar                     
- BusinessProcessGroupAssignment         
- BusinessProcessStage                          
- BusinessProcessTemplateHeader          
- BusinessProcessTemplateTask            
- HcmBenefitOption                              
- HcmBenefitType                                  
- HcmCompensationGrid                            
- HcmCompensationLevel                          
- HcmCompensationPayFrequency                 
- HcmCompensationReferencePointSetup        
- HcmCompensationReferencePointSetupLine 
- HcmCompensationRegion                     
- HcmCompFixedPlanTable                     
- HcmEmployment                                
- HcmEthnicOrigin                                
- HcmFixedCompensationEvent                 
- HcmJob                                           
- HcmJobFunction
- HcmJobType
- HcmLanguageCode
- HcmPayrollCalculationFrequency
- HcmPosition
- HcmPositionType
- HcmSkillType
- HcmVeteranStatus
- HcmWorkCalendarHoliday
- HcmWorkCalendarHolidayLine
- HcmWorker
- HcmWorkerPersonalDetail
- LeaveType
- OMDepartment
- OMLegalEntity
- PayCycle
- PayPeriod
- PayrollBenefitCalculationRate
- PayrollBenefitCalculationRateDetail
- PayrollEarningCode

### <a name="unable-to-see-goals-and-reviews-in-manager-self-service"></a>غير قادر على رؤية الأهداف والمراجعات في الخدمة الذاتية للمدراء

تسمح الآن التغييرات التي تمت هذا الأسبوع بعرض وتحرير الأهداف والمراجعات لمدراء تخطي المستويات في الخدمة الذاتية للمدراء.

### <a name="goal-form-cannot-be-closed-after-a-user-edits-any-goal-field"></a>لا يمكن إغلاق نموذج الهدف بعد قيام أحد المستخدمين بتحرير أي حقل هدف

يعمل هذا الإصدار على تصحيح مشكلة عدم إغلاق نموذج الهدف عند تحديد **إغلاق**.

### <a name="creating-new-goals-and-saving-displays-error"></a>ظهور رسالة خطأ عند إنشاء أهداف جديدة وحفظها

يعمل هذا الإصدار على تصحيح مشكلة تحدث عند حفظ الأهداف في الخدمة الذاتية للموظفين والمدراء.

### <a name="unable-to-add-a-field-to-position-details"></a>غير قادر على إضافة حقل إلى تفاصيل المنصب 

يدعم هذا الإصدار الآن الحقول المخصصة في تفاصيل المنصب.
 
### <a name="unable-to-set-up-expiring-date-on-the-earning-code-through-data-management"></a>غير قادر على إعداد تاريخ انتهاء الصلاحية على كود الأرباح من خلال إدارة البيانات

تسمح لك التغييرات الآن بتعيين تواريخ انتهاء الصلاحية على أكواد الأرباح في إدارة البيانات.

### <a name="new-custom-fields-dont-sync-quickly-enough"></a>عدم مزامنة الحقول المخصصة الجديدة بسرعة كافية

تم تحسين أداء مزامنة الحقول المخصصة إلى Common Data Service في إصدار هذا الأسبوع.

### <a name="entity-export-to-database-jobs-fail-with-error-message-format-of-the-initialization-string-does-not-conform-to-specification-starting-at-index-0"></a>فشل تصدير الكيان إلى وظائف قاعدة البيانات وظهور رسالة الخطأ: "لا يتوافق تنسيق سلسلة التهيئة مع المواصفات التي تبدأ عند الفهرس 0."

يعمل هذا الإصدار على تصحيح المشكلة التي تفشل فيها الوظائف الدفعية لقاعدة البيانات. لإجراء التحديث يدويًا:

1. انتقل إلى **إدارة البيانات**.
2. حدد **تكوين تصدر الكيان إلى قاعدة البيانات**.
3. أعد إدخال سلسلة الاتصال في قاعدة البيانات الهدف وحدد **حفظ**.

### <a name="smtp-email-configuration-suddenly-fails-with-error-message-the-smtp-server-requires-a-secure-connection-or-the-client-was-not-authenticated"></a>فشل تكوين البريد الإلكتروني SMTP بشكل مفاجئ مع ظهور رسالة الخطأ: "يحتاج خادم SMTP إلى اتصال آمن أو لم تتم مصادقة العميل."

يعمل هذا الإصدار على تصحيح تكوين البريد الإلكتروني SMTP الذي يفشل بشكل مفاجئ. لإجراء التحديث يدويًا:

1. انتقل إلى **إدارة النظام**.
2. حدد **محددات البريد الإلكتروني**.
3. حدد **إعدادات SMTP**. 
4. أعد إدخال اسم المستخدم وكلمة المرور المستخدمين لخادم SMTP وحدد **حفظ**.

## <a name="in-preview"></a>قيد المعاينة

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>لا يتم تمكين ميزات المعاينة إلا في مثيلات بيئة الاختبار المعزول

عند توفير مثيل جديد من Talent‬، يمكنك تحديد ما إذا كان نوع المثيل هو **إنتاج** أو **بيئة اختبار معزولة**. تسمح أنواع مثيلات **بيئة اختبار معزولة** بالاختبار المبكر للميزات الجديدة. سيتم تحديث كافة مثيلات Talent الموجودة إلى نوع مثيل **الإنتاج**. إذا كنت ترغب في تحديث أحد المثيلات الموجودة لديك إلى نوع مثيل **بيئة الاختبار المعزولة**، اتصل بـ [الدعم](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) لبدء طلب التغيير.

لمزيد من المعلومات حول كيفية نشر التغييرات، راجع [توفير Talent‬](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="restrict-leave-types-in-time-off-requests"></a>تقييد أنواع الإجازات في طلب أيام الإجازات

يمكن للمؤسسات تقديم العديد من الأنواع المختلفة من الإجازات إلى الموظفين. ولكن، قد لا يكون مناسبًا للموظفين تقديم طلبات الإجازات لبعض أنواع الإجازات. قد تتم إدارة أنواع الإجازات هذه بواسطة الموارد البشرية بدلاً من ذلك. يمكنك في هذا الإصدار تكوين أنواع الإجازات التي يمكن للموظفين تقديم طلبات أيام الإجازة لها. 

### <a name="view-performance-information-for-direct-and-extended-reports-in-manager-self-service"></a>عرض معلومات الأداء للتقارير المباشرة والموسعة في الخدمة الذاتية للمدير

سيسمح خيار جديد للمديرين بعرض أداء التقارير المباشرة والتقارير الملحقة. في الوقت الحالي، يمكن لمديري البنود تعيين أهداف الأداء وتحديثها وإصدار مراجعات جديدة. بالإضافة إلى ذلك، يمكن للمديرين المباشرين وموظفيهم الاحتفاظ بدفاتر يومية الأداء وتحديثها للمساعدة في ضمان كفاءة عملية مراجعه الأداء. عند تطبيق هذا التغيير، سيتمكن المديرون من عرض المعلومات المتعلقة بالأداء وصيانتها للتقارير الموسعة بالإضافة إلى التقارير المباشرة.
