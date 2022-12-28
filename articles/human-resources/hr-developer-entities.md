---
title: جداول Dataverse
description: تستخدم Microsoft Dynamics 365 Human Resources خدمة Dataverse لتمكين سيناريوهات ‏‫قابلية التوسعة والتكامل.
author: twheeloc
ms.date: 12/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 51be30f10c8e5f5e962f54f720f66c712a785835
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838572"
---
# <a name="dataverse-tables"></a>جداول Dataverse


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

تستخدم Microsoft Dynamics 365 Human Resources خدمة Dataverse لتمكين سيناريوهات ‏‫قابلية التوسعة والتكامل.

> [!NOTE]
> تتوافق كيانات Human Resources مع جداول Dataverse. لمزيد من المعلومات حول Dataverse (المعروف في السابق باسم Common Data Service) وتحديثات المصطلحات، راجع [الجديد في Microsoft Dataverse؟](/powerapps/maker/data-platform/data-platform-intro)

جداول Dataverse التالي متوفرة استنادًا إلى كيانات Human Resources.

لمزيد من المعلومات حول المشكلات المعروفة، راجع [‬‏‫البحث عن المشاكل في Lifecycle Services (LCS)](/dev-itpro/lifecycle-services/issue-search-lcs).

## <a name="benefit-tables"></a>جداول الميزات

| Name | الجدول | مشكلات معروفة  | Status |
| --- | --- |    --------|----------  |
| تكرار حساب الميزة | cdm_benefitcalculationfrequency |     |     |
| حساب تكرار فترة دفع الميزة | cdm_benefitcalculationfrequencypayperiod |     |     |
| معدل حساب الميزة | cdm_benefitcalculationrate |    |     |
| تفاصيل معدل حساب الميزة | cdm_benefitcalculationratedetail |753225 | تم الحل  |
| خيار الميزة | cdm_benefitoption |    |     |
| خطة الميزة | cdm_benefitplan (غير ممكّن‬ لدعم الحقل المخصص) |    |     |
| نوع الميزة | cdm_benefittype |    |     |

## <a name="business-process-tasks-tables"></a>جداول مهام العملية التجارية

| Name | الجدول |مشكلات معروفة  | Status |
| --- | --- |   --------|----------   |
| تقويم عملية الأعمال | cdm_businessprocesscalendar | 751867 | تم الحل |
| تعيين مجموعة عمليات الأعمال | cdm_businessprocessgroupassignment | 751869  751863 | نشط(ة)|
| مجموعة مهام مكتبة عمليات الأعمال | cdm_businessprocesslibrarytaskgroup |751866 | مقفل |
| مرحلة عملية الأعمال‬ | cdm_businessprocessstage |      |     |
| رأس قالب قائمة الاختيار | cdm_businessprocesstemplateheader |     |     |
| مهمة قالب قائمة الاختيار | cdm_businessprocesstemplatetask |      |     |

## <a name="compensation-tables"></a>جداول التعويض

| Name | الجدول |مشكلات معروفة  | Status |
| --- | --- | ----------      | -------    |
| خطة التعويض الثابت | cdm_compensationfixedplan |754453 | مقفل |
| شبكة التعويض | cdm_compensationgrid |             |     |
| مستوى التعويض | cdm_compensationlevel |           |     |
| تكرار دفع التعويض | cdm_compensationpayfrequency |                  |     |
| إعداد النقاط المرجعية للتعويض | cdm_compensationreferencepointsetup |               |     |
| إعداد بند النقاط المرجعية للتعويض | cdm_compensationreferencepointsetupline |             |     |
| منطقة التعويض | cdm_compensationregion |                   |     |
| بنية التعويض | cdm_compensationstructure |    754456        | مقفل    |
| خطة التعويض المتغير | cdm_compensationvariableplan |               |     |
| مستوى خطة التعويض المتغير | cdm_compensationvariableplanlevel |                |     |
| نوع خطة التعويض المتغير | cdm_compensationvariableplantype |               |     |
| حدث التعويض الثابت | cdm_fixedcompensationevent |               |     |
| قاعدة الاستحقاق | cdm_vestingrule |              |     |
| التعويض الثابت للعاملين | cdm_workerfixedcompensation |              |     |

## <a name="organization-tables"></a>جداول المؤسسة

| Name | الجدول |مشكلات معروفة  | Status |
| --- | --- | ----------      | -------    |
| قسم | cdm_department |  752194    | مقفل    |
| التوظيف | cdm_employment | 762414  |  مقفل  |
| الشركة | cdm_company |  |     |
| وظيفة | cdm_job |  |     |
| مهمة الوظيفة | cdm_jobfunction |        |     |
| منصب الوظيفة | cdm_jobposition | 752214      | مقفل    |
| نوع المنصب | cdm_positiontype |            |     |
| تعيين العامل بالمنصب | cdm_positionworkerassignmentmap | 752224    |  مقفل   |
| بُعد منصب الوظيفة | cdm_jobpositiondimension|       |     |
| نوع الوظيفة | cdm_jobtype |      |     |
| اللغة | cdm_language |        |     |
| المسمى الوظيفي | cdm_title |       |     |

> [!NOTE]
> توفر الأبعاد المالية لـ **نوع المنصب**، و **تعيين عامل المنصب**، و **التوظيف** تكاملاً من اتجاه واحد لـ Dataverse. في الوقت الحالي، لا يمكن مزامنة تحديثات الأبعاد المالية من Dataverse إلى Human Resources. 

## <a name="leave-and-absence-tables"></a>جداول الإجازة والغياب

| Name | الجدول | مشكلات معروفة  | Status |
| --- | --- |   ----------      | -------    |
| حركة بنك الإجازة | cdm_leavebanktransaction |  752252    |    تم الحل |
| تسجيل الإجازات | cdm_leaveenrollment |  752934    |مقفل     |
| خطة الإجازة | cdm_leaveplan |   752232   |   مقفل  |
| طلب الإجازة | cdm_leaverequest | 753207     | مقفل    |
| تفاصيل طلب المستخدم | cdm_leaverequestdetail | 753207     |   مقفل  |
| نوع الإجازة | cdm_leavetype |      |     |
| كود سبب نوع الإجازة‬ | cdm_leavetypereasoncode |         |     |

>[!NOTE]
>يتوفر التكامل ثنائي الكتابة باستخدام جداول Dataverse للإجازة والغياب فقط عندما يتم تمكين الميزة **تكوين أنواع إجازات متعددة في خطة إجازة واحدة‬** في المالية Microsoft Dynamics 365 Finance باستخدام **إدارة الميزات**. 

## <a name="payroll-tables"></a>جداول الرواتب

| Name | الجدول |مشكلات معروفة  | Status |
| --- | --- |  ----------      | -------    |
| دورة الدفع | cdm_paycycle |    |     |
| فترة الدفع | cdm_payperiod |          |     |
| كود أرباح كشف الرواتب | cdm_payrollearningcode |   754458        |   مقفل  |
| مصروف الحساب البنكي | cdm_bankaccountdisbursement |    751904     |   مقفل  |
| منطقة الضريبة | cdm_taxregion |          |     |

## <a name="worker-tables"></a>جداول العامل

| Name | الجدول |مشكلات معروفة  | Status |
| --- | --- |----------      | -------    |
| العامل | cdm_worker |    751906    |    مقفل |
| عنوان العامل | cdm_workeraddress |   754465     |مقفل     |
| التفاصيل الشخصية للعامل | cdm_workerpersonaldetail |   751906     |   مقفل  |
| رقم الهوية الشخصية للعامل | cdm_workerpersonidentificationnumber |  766704      |   مقفل  |
| نوع الهوية الشخصية للعامل | cdm_workerpersonidentificationtype |        |     |
| تقويم العمل | cdm_workcalendar |        |     |
| يوم تقويم العمل | cdm_workcalendarday |        |     |
| إجازة تقويم العمل |cdm_workcalendarholiday |        |     |
| بند أجازة تقويم العمل | cdm_workcalendarholidayline |        |     |
| الفاصل الزمني لتقويم العمل | cdm_workcalendartimeinterval (غير ممكّن‬ لدعم الحقل المخصص) |        |     |
| الحساب البنكي للعامل | cdm_workerbankaccount |        |     |

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

![العامل.](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>الوظيفة ومنصب الوظيفة

![الوظيفة ومنصب الوظيفة.](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>المزايا‬

![المزايا‬.](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>التعويض

![التعويض.](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>الإجازة

![الإجازة.](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>تقويم العمل

![تقويم العمل.](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a>راجع أيضًا

[اختيار تقنية تكامل بيانات](hr-admin-integration-choose-technology.md)<br>
[تكوين تكامل Dataverse ](hr-admin-integration-common-data-service.md)<br>
[تكوين جداول Dataverse الظاهرية](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[الأسئلة المتداولة حول الجداول الظاهرية في Human Resources](hr-admin-virtual-entity-faq.md)<br>
[ما هو Microsoft Dataverse؟](/powerapps/maker/data-platform/data-platform-intro)<br>
[تحديثات المصطلحات](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
