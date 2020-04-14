---
title: كيانات Common Data Service .
description: تستخدم Microsoft Dynamics 365 Human Resources خدمة Common Data Service لتمكين سيناريوهات ‏‫قابلية التوسعة والتكامل.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: c8e0288da16829c04a9b97c0a52caa8bd27cddf8
ms.sourcegitcommit: fde8045ea49d0cf26d5e7ac5a0da5c0d3d69d5bc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/26/2020
ms.locfileid: "3166488"
---
# <a name="common-data-service-entities"></a>كيانات Common Data Service .

تستخدم Microsoft Dynamics 365 Human Resources خدمة Common Data Service لتمكين سيناريوهات ‏‫قابلية التوسعة والتكامل.

لمزيدٍ من المعلومات حول Common Data Service، راجع [ما المقصود بـ Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).

كيانات الموارد البشرية التالية متوفرة في Common Data Service.

## <a name="benefit-entities"></a>كيانات الميزة

| الاسم | الكيان |
| --- | --- |
| تكرار حساب الميزة | cdm_benefitcalculationfrequency |
| حساب تكرار فترة دفع الميزة | cdm_benefitcalculationfrequencypayperiod |
| معدل حساب الميزة | cdm_benefitcalculationrate |
| تفاصيل معدل حساب الميزة | cdm_benefitcalculationratedetail |
| خيار الميزة | cdm_benefitoption |
| خطة الميزة | cdm_benefitplan (غير ممكّن‬ لدعم الحقل المخصص) |
| نوع الميزة | cdm_benefittype |

## <a name="business-process-tasks-entities"></a>كيانات مهام العملية التجارية

| الاسم | الكيان |
| --- | --- |
| تقويم عملية الأعمال | cdm_businessprocesscalendar |
| تعيين مجموعة عمليات الأعمال | cdm_businessprocessgroupassignment |
| مجموعة مهام مكتبة عمليات الأعمال | cdm_businessprocesslibrarytaskgroup |
| مرحلة عملية الأعمال‬ | cdm_businessprocessstage |
| رأس قالب قائمة الاختيار | cdm_businessprocesstemplateheader |
| مهمة قالب قائمة الاختيار | cdm_businessprocesstemplatetask |

## <a name="compensation-entities"></a>كيانات التعويض

| الاسم | الكيان |
| --- | --- |
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
| حدث التعويض الثابت | cdm_fixedcompensationevent |
| قاعدة الاستحقاق | cdm_vestingrule |
| التعويض الثابت للعامل | cdm_workerfixedcompensation |

## <a name="organization-entities"></a>كيانات المؤسسة

| الاسم | الكيان |
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
> توفر الأبعاد المالية لـ **نوع المنصب **، و**تعيين عامل المنصب**، و**التوظيف** تكاملاً من اتجاه واحد لـ Common Data Service. في الوقت الحالي، لا يمكن مزامنة تحديثات الأبعاد المالية من Common Data Service إلى Human Resources. 

## <a name="leave-and-absence-entities"></a>كيانات الإجازة والغياب

| الاسم | الكيان |
| --- | --- |
| حركة بنك الإجازة | cdm_leavebanktransaction |
| تسجيل الأجازة | cdm_leaveenrollment |
| خطة الإجازة | cdm_leaveplan |
| طلب الإجازة | cdm_leaverequest |
| تفاصيل طلب المستخدم | cdm_leaverequestdetail |
| نوع الإجازة | cdm_leavetype |
| كود سبب نوع الإجازة‬ | cdm_leavetypereasoncode |

## <a name="payroll-entities"></a>كيانات الرواتب

| الاسم | الكيان |
| --- | --- |
| دورة الدفع | cdm_paycycle |
| فترة الدفع | cdm_payperiod |
| كود أرباح كشف الرواتب | cdm_payrollearningcode |
| مصروف الحساب البنكي | cdm_bankaccountdisbursement |
| منطقة الضريبة | cdm_taxregion |

## <a name="worker-entities"></a>كيانات العامل

| الاسم | الكيان |
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

## <a name="worker-setup-entities"></a>كيانات إعداد العامل

| الاسم | الكيان |
| --- | --- |
| حالة الخبير | cdm_veteranstatus |
| الأصل العرقي | cdm_ethnicorigin |
| كود السبب | cdm_reasoncode |
| وكاله إصدار الهوية الشخصية | cdm_personidentificationissuingagency |

## <a name="competency-entities"></a>كيانات الاختصاص

| الاسم | الكيان |
| --- | --- |
| نوع المهارة | cdm_skilltype |

## <a name="entity-relationship-models"></a>نماذج علاقة الكيان

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

[اختيار تقنية تكامل بيانات](hr-admin-integration-choose-technology.md)</br>
[تكوين تكامل Common Data Service ](hr-admin-integration-common-data-service.md)
