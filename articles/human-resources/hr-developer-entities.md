---
title: جداول Dataverse
description: تستخدم Microsoft Dynamics 365 Human Resources خدمة Dataverse لتمكين سيناريوهات ‏‫قابلية التوسعة والتكامل.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: caf8b0a5d0b24ef3619f45a6d236acae6d29c8ab
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465212"
---
# <a name="dataverse-tables"></a>جداول Dataverse

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

تستخدم Microsoft Dynamics 365 Human Resources خدمة Dataverse لتمكين سيناريوهات ‏‫قابلية التوسعة والتكامل.

> [!NOTE]
> تتوافق كيانات Human Resources مع جداول Dataverse. لمزيد من المعلومات حول Dataverse (المعروف في السابق باسم Common Data Service) وتحديثات المصطلحات، راجع [الجديد في Microsoft Dataverse؟](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)

جداول Dataverse التالي متوفرة استنادًا إلى كيانات Human Resources.

## <a name="benefit-tables"></a>جداول الميزات

| الاسم | الجدول |
| --- | --- |
| تكرار حساب الميزة | cdm_benefitcalculationfrequency |
| حساب تكرار فترة دفع الميزة | cdm_benefitcalculationfrequencypayperiod |
| معدل حساب الميزة | cdm_benefitcalculationrate |
| تفاصيل معدل حساب الميزة | cdm_benefitcalculationratedetail |
| خيار الميزة | cdm_benefitoption |
| خطة الميزة | cdm_benefitplan (غير ممكّن‬ لدعم الحقل المخصص) |
| نوع الميزة | cdm_benefittype |

## <a name="business-process-tasks-tables"></a>جداول مهام العملية التجارية

| الاسم | الجدول |
| --- | --- |
| تقويم عملية الأعمال | cdm_businessprocesscalendar |
| تعيين مجموعة عمليات الأعمال | cdm_businessprocessgroupassignment |
| مجموعة مهام مكتبة عمليات الأعمال | cdm_businessprocesslibrarytaskgroup |
| مرحلة عملية الأعمال‬ | cdm_businessprocessstage |
| رأس قالب قائمة الاختيار | cdm_businessprocesstemplateheader |
| مهمة قالب قائمة الاختيار | cdm_businessprocesstemplatetask |

## <a name="compensation-tables"></a>جداول التعويض

| الاسم | الجدول |
| --- | --- |
| خطة التعويض الثابت | cdm_compensationfixedplan |
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
| حدث التعويض الثابت | cdm_fixedcompensationevent |
| قاعدة الاستحقاق | cdm_vestingrule |
| التعويض الثابت للعاملين | cdm_workerfixedcompensation |

## <a name="organization-tables"></a>جداول المؤسسة

| الاسم | الجدول |
| --- | --- |
| قسم | cdm_department |
| التوظيف | cdm_employment |
| الشركة | cdm_company |
| وظيفة | cdm_job |
| مهمة الوظيفة | cdm_jobfunction |
| منصب الوظيفة | cdm_jobposition |
| نوع المنصب | cdm_positiontype |
| تعيين العامل بالمنصب | cdm_positionworkerassignmentmap |
| بُعد منصب الوظيفة | cdm_jobpositiondimension|
| نوع الوظيفة | cdm_jobtype |
| اللغة | cdm_language |
| المسمى الوظيفي | cdm_title |

> [!NOTE]
> توفر الأبعاد المالية لـ **نوع المنصب**، و **تعيين عامل المنصب**، و **التوظيف** تكاملاً من اتجاه واحد لـ Dataverse. في الوقت الحالي، لا يمكن مزامنة تحديثات الأبعاد المالية من Dataverse إلى Human Resources. 

## <a name="leave-and-absence-tables"></a>جداول الإجازة والغياب

| الاسم | الجدول |
| --- | --- |
| حركة بنك الإجازة | cdm_leavebanktransaction |
| تسجيل الإجازات | cdm_leaveenrollment |
| خطة الإجازة | cdm_leaveplan |
| طلب الإجازة | cdm_leaverequest |
| تفاصيل طلب المستخدم | cdm_leaverequestdetail |
| نوع الإجازة | cdm_leavetype |
| كود سبب نوع الإجازة‬ | cdm_leavetypereasoncode |

## <a name="payroll-tables"></a>جداول الرواتب

| الاسم | الجدول |
| --- | --- |
| دورة الدفع | cdm_paycycle |
| فترة الدفع | cdm_payperiod |
| كود أرباح كشف الرواتب | cdm_payrollearningcode |
| مصروف الحساب البنكي | cdm_bankaccountdisbursement |
| منطقة الضريبة | cdm_taxregion |

## <a name="worker-tables"></a>جداول العامل

| الاسم | الجدول |
| --- | --- |
| العامل | cdm_worker |
| عنوان العامل | cdm_workeraddress |
| التفاصيل الشخصية للعامل | cdm_workerpersonaldetail |
| رقم الهوية الشخصية للعامل | cdm_workerpersonidentificationnumber |
| نوع الهوية الشخصية للعامل | cdm_workerpersonidentificationtype |
| تقويم العمل | cdm_workcalendar |
| يوم تقويم العمل | cdm_workcalendarday |
| إجازة تقويم العمل |cdm_workcalendarholiday |
| بند أجازة تقويم العمل | cdm_workcalendarholidayline |
| الفاصل الزمني لتقويم العمل | cdm_workcalendartimeinterval (غير ممكّن‬ لدعم الحقل المخصص) |
| الحساب البنكي للعامل | cdm_workerbankaccount |

## <a name="worker-setup-tables"></a>جداول إعداد العامل

| الاسم | الجدول |
| --- | --- |
| حالة الخبير | cdm_veteranstatus |
| الأصل العرقي | cdm_ethnicorigin |
| كود السبب | cdm_reasoncode |
| وكالة إصدار هوية العامل | cdm_personidentificationissuingagency |

## <a name="competency-tables"></a>جداول الاختصاص

| الاسم | الجدول |
| --- | --- |
| نوع المهارة | cdm_skilltype |

## <a name="table-relationship-models"></a>نماذج علاقة الجدول

### <a name="worker"></a>العامل

![العامل](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>الوظيفة ومنصب الوظيفة

![الوظيفة ومنصب الوظيفة](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>المزايا

![المزايا](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>التعويض

![التعويض](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>الإجازة

![الإجازة](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>تقويم العمل

![تقويم العمل](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a>راجع أيضًا

[اختيار تقنية تكامل بيانات](hr-admin-integration-choose-technology.md)<br>
[تكوين تكامل Dataverse ](hr-admin-integration-common-data-service.md)<br>
[تكوين جداول Dataverse الظاهرية](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[الأسئلة المتداولة حول الجداول الظاهرية في Human Resources](hr-admin-virtual-entity-faq.md)<br>
[ما هو Microsoft Dataverse؟](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[تحديثات المصطلحات](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]