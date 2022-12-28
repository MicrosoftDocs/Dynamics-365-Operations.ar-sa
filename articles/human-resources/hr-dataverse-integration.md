---
title: تكوين التكامل مع جداول dataverse
description: يوضح هذا المقال التكامل بين Microsoft Dynamics 365 Human Resources و Dataverse.
author: anschmidt
ms.date: 12/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2022-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 63c25020b7026a76ecc6e2c3563f8299627ec8a8
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838617"
---
# <a name="configure-integration-with-dataverse-tables"></a>تكوين التكامل مع جداول Dataverse

>[!Important]
>تتوفر الوظيفة المذكورة في هذا المقال حاليًا لعملاء Dynamics 365 Human Resources في بنية Finance and Operations الأساسية. 


لتكامل Microsoft Dynamics 365 Human Resources مع Dataverse، يمكنك استخدام [موحد البيانات](/powerapps/administrator/data-integrator). تتيح Human Resources–إلى–قالب Dataverse البيانات الخاصة بالوظائف والمناصب والعمال وآخرين للتدفق من Human Resources إلى Dataverse ومن Dataverse إلى Human Resources مما يؤدي إلى إنشاء كتابة في كلا النظامين.

## <a name="system-requirements-for-human-resources"></a>متطلبات النظام لـ Human Resourcesـ

يتطلب حل التكامل الإصدارات التالية من Human Resources و Dynamics 365 Finance: 

- الإصدار 7.2 وإصدار لاحق من Dynamics 365 Finance
- بيئة Dynamics CRM التي تم فيها إنشاء قاعدة بيانات والسماح بتطبيقات Dynamics 365

## <a name="template-and-tasks"></a>القوالب والمهام

اتبع هذه الخطوات للوصول إلى قالب Human Resources–إلى–Finance.

1. افتح [مركز مسؤول Power Apps](https://admin.powerapps.com/). 
2. ضمن البيئة الخاصة بك ، حدد **تطبيقات Dynamics 365**، ثم حدد **مصدر التطبيق** على شريط الأدوات.
3. لتثبيت القالب، ابحث عن "Human Resources للكتابة المزدوجة"، أو انتقل مباشرة إلى العنوان التالي: <https://appsource.microsoft.com/product/dynamics-365/mscrm.hcm_dualwrite>.
3. بعد اكتمال التثبيت، افتح Dynamics 365 Finance.
4. افتح مساحة العمل **إدارة البيانات**. 
5. حدد **الكتابة المزدوجة**. 
6. اتبع العملية لربط البيئة الخاصة بك بشركة واحدة على الأقل في مؤسستك. 
7. عند الانتهاء من إعداد ارتباط لبيئة Dataverse الخاصة بك، حدد **تطبيق الحل**. يتم تطبيق الحل، ويتم تثبيت التعيينات في تطبيق الموحد.

## <a name="template-mappings"></a>تعيينات القالب

في جداول تعيين القوالب التالية، يشير اسم المهمة إلى الكيانات المستخدمة في كل تطبيق. Finance على اليسار، وتكون Dataverse على اليمين.

### <a name="bank-account-disbursements-dual-write-to-bank-account-disbursement"></a>مصروفات الحساب البنكي (الكتابة المزدوجة) إلى مصروف الحساب البنكي

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ACCOUNTIDENTIFICATIONID        | cdm\_bankaccountid.cdm\_accountidentification        |
| المبلغ                         | cdm\_amount                                         |
| PRIORITY                       | cdm\_disbursementpriority                           |
| PERSONNELNUMBER                | cdm\_bankaccountid.cdm\_workerid.cdm\_workernumber    |
| REMAINDER                      | cdm\_isremainder                                    |

### <a name="benefit-calculation-rate-detail-dual-write-to-benefit-calculation-rate-detail"></a>تفاصيل معدل حساب الميزة لتفاصيل معدل حساب الميزة

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| CONTRIBUTIONMETHOD             | cdm\_contributionmethod                             |
| EFFECTIVE                      | cdm\_السريان                                      |
| EMPLOYERCONTRIBUTION           | cdm\_employercontribution                           |
| EXPIRATION                     | cdm\_expiration                                     |
| WORKERDEDUCTION                | cdm\_workerdeduction                                |
| NAME                           | cdm\_calculationrateid.cdm\_name                     |

### <a name="benefit-calculation-rate-header-to-benefit-calculation-rate"></a>عنوان سعر حساب الميزة لمعدل حساب الميزة

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| الوصف                    | cdm\_description                                    |
| NAME                           | cdm\_name                                           |
| TIERTYPE                       | cdm\_tiertype                                       |

### <a name="benefit-option-to-benefit-option"></a>خيار الميزة لخيار الميزة

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ALLOWBENEFICIARYDESIGNATIONS   | cdm\_allowbeneficiarydesignations                   |
| ALLOWDEPENDENTCOVERAGE         | cdm\_allowdependentcoverage                         |
| BENEFITOPTIONID                | cdm\_name                                           |
| الوصف                    | cdm\_description                                    |
| ISWAIVE                        | cdm\_iswaived                                       |

### <a name="benefit-type-to-benefit-type"></a>نوع الميزة لنوع الميزة

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| BENEFITTYPEID                  | cdm\_name                                           |
| CONCURRENTENROLLMENT           | cdm\_concurrentenrollment                           |
| الوصف                    | cdm\_description                                    |
| PAYROLLCATEGORY                | cdm\_payrollcategory                                |

### <a name="business-calendar-to-business-process-calendar"></a>تقويم الأعمال ‏‫لتقويم عملية الأعمال

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| CALENDARID                     | cdm\_name                                           |
| NAME                           | cdm\_calendarname                                   |
| STARTDATE                      | cdm\_startdate                                      |
| ENDDATE                        | cdm\_enddate                                        |
| ISOPENMONDAY                   | cdm\_ismondayopen                                   |
| ISOPENTUESDAY                  | cdm\_istuesdayopen                                  |
| ISOPENWEDNESDAY                | cdm\_iswednesdayopen                                |
| ISOPENTHURSDAY                 | cdm\_isthursdayopen                                 |
| ISOPENFRIDAY                   | cdm\_isfridayopen                                   |
| ISOPENSATURDAY                 | cdm\_issaturdayopen                                 |
| ISOPENSUNDAY                   | cdm\_issundayopen                                   |

### <a name="business-process-to-business-process-header"></a>عملية الأعمال لعنوان عملية الأعمال

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSID                      | cdm\_processid                                      |
| PROCESSTYPE                    | cdm\_processtype                                    |
| GENERICSUBTYPE                 | cdm\_genericsubtype                                 |
| NAME                           | cdm\_name                                           |
| الوصف                    | cdm\_description                                    |
| الحالة                         | cdm\_الحالة                                         |
| TARGETDATE                     | cdm\_targetdate                                     |
| STARTDATETIME                  | cdm\_startdatetime                                  |
| ENDDATETIME                    | cdm\_enddatetime                                    |
| RESOLVEDBYPERSONNELNUMBER      | cdm\_resolvedbyid.cdm\_workernumber                  |
| PROCESSOWNERPERSONNELNUMBER    | cdm\_processownerid.cdm\_workernumber                |
| SOURCETEMPLATENAME             | cdm\_sourcetemplateid.cdm\_name                      |
| SOURCETEMPLATEPROCESSTYPE      | cdm\_sourcetemplateid.cdm\_businessprocesstype       |
| SOURCETEMPLATEGENERICSUBTYPE   | cdm\_sourcetemplateid.cdm\_genericsubtype            |

### <a name="business-process-library-task-group-to-business-process-library-task-group"></a>‏‫مجموعات مهام مكتبة عمليات الأعمال‬ إلى ‏‫مجموعات مهام مكتبة عمليات الأعمال‬

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSTYPE                    | cdm\_processtype                                    |
| NAME                           | cdm\_name                                           |
| الوصف                    | cdm\_description                                    |

### <a name="business-process-stage-to-business-process-stage"></a>مرحلة عملية الأعمال لمرحلة عملية الأعمال

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSTYPE                    | cdm\_businessprocesstype                            |
| NAME                           | cdm\_name                                           |
| الوصف                    | cdm\_description                                    |
| SEQUENCENUMBER                 | cdm\_sequencenumber                                 |

### <a name="business-process-task-to-business-process-task"></a>مهمة عملية الأعمال لمهمة عملية الأعمال

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| الوصف                    | cdm\_description                                    |
| DUEDATE                        | cdm\_duedate                                        |
| TASKID                         | cdm\_taskid                                         |
| INSTRUCTIONS                   | cdm\_instructions                                   |
| COMPLETIONDATETIME             | cdm\_completiondatetime                             |
| ASSIGNMENTTYPE                 | cdm\_assignmenttype                                 |
| ISOPTIONAL                     | cdm\_isoptional                                     |
| NAME                           | cdm\_name                                           |
| الحالة                         | cdm\_status                                         |
| RESOLVEDBY\_PERSONNELNUMBER     | cdm\_resolvedbyid.cdm\_workernumber                  |
| TEMPLATETASKID                 | cdm\_templatetaskid.cdm\_taskid                      |
| ASSIGNEDWORKER\_PERSONNELNUMBER | cdm\_assignedworkerid.cdm\_workernumber              |
| PROCESSID                      | cdm\_processheaderid.cdm\_processid                  |
| ASSIGNEDGROUP\_NAME             | cdm\_assignedgroupid.cdm\_name                       |
| ASSIGNEDPOSITION\_POSITIONID    | cdm\_assignedposition.cdm\_jobpositionnumber         |

### <a name="business-process-template-to-checklist-template-header"></a>قالب عملية الأعمال لعنوان قالب قائمة الاختيار

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSTYPE                    | cdm\_businessprocesstype                            |
| GENERICSUBTYPE                 | cdm\_genericsubtype                                 |
| NAME                           | cdm\_name                                           |
| الوصف                    | cdm\_description                                    |
| CALENDARID                     | cdm\_businessprocesscalendarid.cdm\_name             |
| PERSONNELNUMBER                | cdm\_processownerid.cdm\_workernumber                |
| ISACTIVE                       | cdm\_isactive                                       |

### <a name="business-process-template-task-to-checklist-template-task"></a>مهمة قالب عملية الأعمال لمهمة قالب قائمة الاختيار

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| TASKID                         | cdm\_taskid                                         |
| NAME                           | cdm\_name                                           |
| TEMPLATEHEADER\_PROCESSTYPE     | cdm\_businessprocesstemplateheaderid.cdm\_businessprocesstype |
| TEMPLATEHEADER\_GENERICSUBTYPE  | cdm\_businessprocesstemplateheaderid.cdm\_genericsubtype |
| TEMPLATEHEADER\_NAME            | cdm\_businessprocesstemplateheaderid.cdm\_name       |
| الوصف                    | cdm\_description                                    |
| DUEDATEOFFSETDAYS              | cdm\_duedateoffsetdays                              |
| MENUITEMTYPE                   | cdm\_tasklinktype                                   |
| MENUITEM                       | cdm\_tasklink                                       |
| CONTACTPERSON\_PERSONNELNUMBER  | cdm\_contactpersonid.cdm\_workernumber               |
| ASSIGNMENTTYPE                 | cdm\_assignmenttype                                 |
| ASSIGNEDWORKER\_PERSONNELNUMBER | cdm\_assignedworkerid.cdm\_workernumber              |
| ASSIGNEDPOSITION\_POSITIONID    | cdm\_assignedpositionid.cdm\_jobpositionnumber       |
| ASSIGNEDGROUP\_NAME             | cdm\_assignedgroupid.cdm\_name                       |
| ISOPTIONAL                     | cdm\_isoptional                                     |
| INSTRUCTIONS                   | cdm\_الإرشادات                                   |

### <a name="calculation-frequency-to-benefit-calculation-frequency"></a>تكرار الحساب لتكرار حساب الميزة

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| الوصف                    | cdm\_description                                    |
| FREQUENCY                      | cdm\_name                                           |
| FREQUENCYCONTROL               | cdm\_frequencycontrol                               |
| ISIMMUTABLE                    | cdm\_isimmutable                                    |

### <a name="calculation-frequency-pay-period-to-benefit-calculation-frequency-pay-period"></a>فترة دفع تكرار الحساب لفترة دفع تكرار حساب الميزة

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| CALCULATIONFREQUENCYID         | cdm\_benefitcalculationfrequencyid.cdm\_name         |
| PERIODSTARTDATE                | cdm\_payperiodid.cdm\_periodstartdate                |
| PAYCYCLEID                     | cdm\_payperiodid.cdm\_paycycleid.cdm\_name            |

### <a name="calendar-to-work-calendar"></a>تقويم لتقويم العمل

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| CALENDARID                     | cdm\_name                                           |
| CALENDARNAME                   | cdm\_description                                    |
| WORKCALENDARHOLIDAYID          | cdm\_workcalendarholidayid.cdm\_name                 |

### <a name="compensation-fixed-action-table-to-fixed-compensation-event"></a>جدول إجراءات التعويض الثابتة لحدث التعويض الثابت

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ACTION                         | cdm\_name                                           |
| ACTIVE                         | cdm\_isactive                                       |
| الوصف                    | cdm\_description                                    |
| النوع                           | cdm\_eventtype                                      |

### <a name="compensation-fixed-plan-to-compensation-fixed-plan"></a>الخطة الثابتة للتعويض لخطة التعويض الثابت

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| PLAN                           | cdm\_name                                           |
| الوصف                    | cdm\_description                                    |
| النوع                           | cdm\_type                                           |
| EFFECTIVEDATE                  | cdm\_effectivedate                                  |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| العملة                       | cdm\_transactioncurrencyid.isocurrencycode          |
| PAYFREQUENCY                   | cdm\_payfrequency.cdm\_name                          |
| HIRERULE                       | cdm\_hirerule                                       |
| OUTOFRANGETOLERANCE            | cdm\_outofrangetolerance                            |
| RECOMMENDATIONALLOWED          | cdm\_recommendationallowed                          |
| COMPENSATIONSTRUCTURE          | cdm\_compensationgrid.cdm\_name                      |
| REFPOINTSETUPID                | cdm\_referencepointsetupline.cdm\_referencepointsetupid.cdm\_الاسم |
| CONTROLPOINT                   | cdm\_referencepointsetupline.cdm\_name               |

### <a name="compensation-grids-to-compensation-grid"></a>شبكات التعويض لشبكة التعويض

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| GRIDID                         | cdm\_name                                           |
| الوصف                    | cdm\_description                                    |
| EFFECTIVEDATE                  | cdm\_effectivedate                                  |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| REFERENCESETUP                 | cdm\_referencepointsetupid.cdm\_name                 |
| النوع                           | cdm\_type                                           |
| العملة                       | cdm\_transactioncurrencyid.isocurrencycode          |

### <a name="compensation-job-function-to-job-function"></a>مهمة وظيفة التعويض إلى مهمة الوظيفة

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| JOBFUNCTIONID                  | cdm\_name                                           |
| الوصف                    | cdm\_description                                    |

### <a name="compensation-job-type-to-job-type"></a>نوع وظيفة التعويض لنوع الوظيفة

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| JOBTYPEID                      | cdm\_name                                           |
| الوصف                    | cdm\_description                                    |
| EXEMPTSTATUS                   | cdm\_exemptstatus                                   |

### <a name="compensation-pay-frequency-to-compensation-pay-frequency"></a>تكرار دفع التعويض لتكرار دفع التعويض

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| PAYRATECONVERSION              | cdm\_name                                           |
| PERIOD                         | cdm\_الفترة                                         |
| الوصف                    | cdm\_description                                    |
| ANNUALCONVERSIONFACTOR         | cdm\_annualconversionfactor                         |
| HOURLYCONVERSIONFACTOR         | cdm\_hourlyconversionfactor                         |
| MONTHLYCONVERSIONFACTOR        | cdm\_monthlyconversionfactor                        |
| WEEKLYCONVERSIONFACTOR         | cdm\_weeklyconversionfactor                         |

### <a name="compensation-regions-to-compensation-region"></a>مناطق التعويض لمنطقة التعويض

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| الوصف                    | cdm\_description                                    |
| الموقع                       | cdm\_name                                           |

### <a name="compensation-variable-plan-v2-to-compensation-variable-plan"></a>خطة التعويض المتغيرة V2 لخطة التعويض المتغيرة

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| VARIABLEAWARDBASIS             | cdm\_awardbasis                                     |
| AWARDBASISCALCULATION          | cdm\_awardbasiscalculation                          |
| CALCULATIONTYPE                | cdm\_calculationtype                                |
| الوصف                    | cdm\_description                                    |
| ENABLEENROLLMENT               | cdm\_enableenrollment                               |
| ENABLELEVELS                   | cdm\_enablelevels                                   |
| ENABLERECOMMENDATION           | cdm\_enablerecommendation                           |
| HIRERULE                       | cdm\_hirerule                                       |
| LEVERAGE100PERCENT             | cdm\_leverage100percent                             |
| LEVERAGEMAXIMUM                | cdm\_leveragemaximum                                |
| LEVERAGEMINIMUM                | cdm\_leverageminimum                                |
| LEVERAGEOVEROBJECTIVE          | cdm\_leverageoverobjective                          |
| LEVERAGEUNDEROBJECTIVE         | cdm\_leverageunderobjective                         |
| PERCENTOFBASIS                 | cdm\_percentofbasis                                 |
| PLANID                         | cdm\_name                                           |
| VARIABLECOMPENSATIONTYPE       | cdm\_variablecompensationtypeid.cdm\_name            |
| UNITCURRENCYCODE               | transactioncurrencyid.isocurrencycode              |
| UNITRELATIONSHIP               | cdm\_unitrelationship                               |
| UNITVALUE                      | cdm\_unitvalue                                      |
| NUMBEROFUNITSREAL              | cdm\_numberofunits                                  |
| EFFECTIVEDATE                  | cdm\_effectivedate                                  |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| VESTINGRULE                    | cdm\_vestingruleid.cdm\_name                         |
| LEVERAGETOLERANCEMAX           | cdm\_leveragetolerancemax                           |
| LEVERAGETOLERANCEMIN           | cdm\_leveragetolerancemin                           |

### <a name="compensation-variable-type-to-compensation-variable-plan-type"></a>نوع خطة التعويض المتغيرة لنوع خطة التعويض المتغيرة

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| الوصف                    | cdm\_description                                    |
| النوع                           | cdm\_awardtype                                      |
| VARIABLECOMPENSATIONTYPE       | cdm\_name                                           |

### <a name="compensation-vesting-rules-to-vesting-rule"></a>قواعد استحقاقات التعويض لقاعدة الاستحقاق

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| الوصف                    | cdm\_description                                    |
| ملاحظة                           | cdm\_notes                                          |
| VESTINGRULE                    | cdm\_name                                           |

### <a name="department-v2-to-department"></a>القسم V2 إلى القسم

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| OPERATINGUNITNUMBER            | cdm\_departmentnumber                               |
| NAME                           | cdm\_name                                           |
| SEARCHNAME                     | cdm\_description                                    |
| PARTYTYPE                      | cdm\_partytype                                      |

### <a name="dual-write-tax-region-to-tax-region"></a>منطقة ضريبة الكتابة المزدوجة لمنطقة الضريبة

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| CITY                           | cdm\_city                                           |
| COUNTRYORREGION                | cdm\_countryorregion                                |
| COUNTY                         | cdm\_county                                         |
| STATE                          | cdm\_stateorprovince                                |
| TAXREGIONNAME                  | cdm\_name                                           |

### <a name="dual-write-worker-identification-to-worker-person-identification-number"></a>‏‫تعريف عامل الكتابة المزدوجة‬ لرقم الهوية الشخصية للعامل‬

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| الوصف                    | cdm\_description                                    |
| ENTRYTYPE                      | cdm\_entrytype                                      |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| IDENTIFICATIONNUMBER           | cdm\_identificationnumber                           |
| IDENTIFICATIONTYPEID           | cdm\_identificationtypeid.cdm\_name                  |
| ISPRIMARY                      | cdm\_isprimary                                      |
| ISSUEDATE                      | cdm\_issuedate                                      |
| ISSUINGAGENCYID                | cdm\_issuingagencyid.cdm\_name                       |
| WORKERNUMBER                   | cdm\_workerid.cdm\_workernumber                      |

### <a name="compensation-structure-to-compensation-structure"></a>بنية التعويض لبنية التعويض

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| المبلغ                         | cdm\_amount                                         |
| GRID                           | cdm\_compensationgridid.cdm\_name                    |
| LEVELID                        | cdm\_compensationlevelid.cdm\_name                   |
| REFERENCEPOINTLINENUMBER       | cdm\_referencepointid.cdm\_linenumber                |
| REFERENCESETUP                 | cdm\_referencepointid.cdm\_referencepointsetupid.cdm\_الاسم |
| REFERENCEPOINT                 | cdm\_referencepointid.cdm\_name                      |

### <a name="earning-code-to-payroll-earning-code"></a>كود الأرباح لكود أرباح كشف الرواتب

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| EARNINGCODE                    | cdm\_name                                           |
| الوصف                    | cdm\_description                                    |
| INCLUDEINPAYMENTTYPE           | cdm\_includeinpaymenttype                           |
| QUANTITYUNIT                   | cdm\_quantityunit                                   |
| TRACKFMLAHOURS                 | cdm\_trackfmlahours                                 |
| ISPRODUCTIVE                   | cdm\_isproductive                                   |

### <a name="employee-fixed-compensation-to-worker-fixed-compensation"></a>التعويض الثابت للموظفين للتعويض الثابت للعاملين

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| COMPENSATIONLEVELID            | cdm\_compensationlevelid.cdm\_name                   |
| النوع                           | cdm\_compensationtype                               |
| EFFECTIVEDATE                  | cdm\_effectivedate                                  |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| LINENUMBER                     | cdm\_linenumber                                     |
| PAYFREQUENCY                   | cdm\_payfrequencyid.cdm\_name                        |
| PAYRATE                        | cdm\_payrate                                        |
| PLAN                           | cdm\_planid.cdm\_name                                |
| POSITIONID                     | cdm\_positionid.cdm\_jobpositionnumber               |
| PROCESSTYPE                    | cdm\_processtype                                    |
| PERSONNELNUMBER                | cdm\_workerid.cdm\_workernumber                      |
| ACTION                         | cdm\_eventid.cdm\_الاسم                               |
| STEP                           | cdm\_referencepointsetuplineid.cdm\_name             |
| REFPOINTSETUPID                | cdm\_referencepointsetuplineid.cdm\_referencepointsetupid.cdm\_name |

### <a name="employment-per-company-to-employment"></a>التوظيف لكل شركة للتوظيف

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| EMPLOYMENTENDDATE              | cdm\_employmentenddate                              |
| PERSONNELNUMBER                | cdm\_workerid.cdm\_workernumber                      |
| EMPLOYMENTSTARTDATE            | cdm\_employmentstartdate                            |
| WORKERTYPE                     | cdm\_workertype                                     |
| DIMENSIONDISPLAYVALUE          | cdm\_dimensiondisplayvalue                          |
| ADJUSTEDWORKERSTARTDATE        | cdm\_adjustedworkerstartdate                        |
| EMPLOYERNOTICEAMOUNT           | cdm\_employernoticeamount                           |
| EMPLOYERUNITOFNOTICE           | cdm\_employerunitofnotice                           |
| WORKERUNITOFNOTICE             | cdm\_workerunitofnotice                             |
| WORKERNOTICEAMOUNT             | cdm\_workernoticeamount                             |
| LASTDATEWORKED                 | cdm\_lastdateworked                                 |
| PROBATIONENDDATE               | cdm\_probationenddate                               |
| TRANSITIONDATE                 | cdm\_transitiondate                                 |
| TRANSITIONREASONCODENAME       | cdm\_transitionreasoncode.cdm\_name                  |
| WORKERSTARTDATE                | cdm\_workerstartdate                                |
| VALIDTO                        | cdm\_validto                                        |
| VALIDFROM                      | cdm\_validfrom                                      |

### <a name="ethnic-origins-to-ethnic-origin"></a>الأصل العرقي للأصل العرقي

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ETHNICORIGINID                 | cdm\_name                                           |
| الوصف                    | cdm\_description                                    |

### <a name="group-assignment-to-business-process-group-assignment"></a>تعيين مجموعة لتعيين مجموعة عمليات الأعمال

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| NAME                           | cdm\_name                                           |
| الوصف                    | cdm\_الوصف                                    |
| ISACTIVE                       | cdm\_isactive                                       |

### <a name="identification-type-to-worker-person-identification-type"></a>نوع الهوية لنوع هوية الشخص العامل

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| الوصف                    | cdm\_description                                    |
| IDENTIFICATIONTYPEID           | cdm\_name                                           |
| ALLOWEDVALUES                  | cdm\_allowedvalues                                  |
| FIXEDLENGTH                    | cdm\_fixedlength                                    |
| IDENTIFICATIONNUMBERFORMAT     | cdm\_identificationnumberformat                     |

### <a name="issuing-agency-to-person-identification-issuing-agency"></a>وكالة إصدار لوكالة إصدار هوية العامل

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| البريد الإلكتروني                          | cdm\_email                                          |
| الرقم الداخلي                      | cdm\_extension                                      |
| FAX                            | cdm\_fax                                            |
| ISSUINGAGENCY                  | cdm\_name                                           |
| MOBILEPHONE                    | cdm\_mobilephone                                    |
| INTERNETADDRESS                | cdm\_websiteurl                                     |
| NAME                           | cdm\_description                                    |
| PAGER                          | cdm\_pager                                          |
| الرسائل النصية القصيرة                            | cdm\_sms                                            |
| TELEPHONE                      | cdm\_telephone                                      |
| TELEXNUMBER                    | cdm\_telex                                          |
| ADDRESSCITY                    | cdm\_city                                           |
| ADDRESSCOUNTY                  | cdm\_county                                         |
| ADDRESSDESCRIPTION             | cdm\_addressdescription                             |
| ADDRESSSTATE                   | cdm\_stateorprovince                                |
| ADDRESSSTREET                  | cdm\_street                                         |
| ADDRESSZIPCODE                 | cdm\_postalcode                                     |
| ADDRESSCOUNTRYREGIONISOCODE    | cdm\_countryregion                                  |

### <a name="job-positions-dual-write-to-job-position"></a>مناصب الوظائف للكتابة الثنائية لوضع الوظيفة

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| POSITIONID                     | cdm\_jobpositionnumber                              |
| ACTIVATION                     | cdm\_activation                                     |
| AVAILABLEFORASSIGNMENT         | cdm\_availableforassignment                         |
| COMPENSATIONREGIONID           | cdm\_compensationregionid.cdm\_name                  |
| DEPARTMENTID                   | cdm\_departmentid.cdm\_departmentnumber              |
| الوصف                    | cdm\_description                                    |
| FULLTIMEEQUIVALENT             | cdm\_fulltimeequivalent                             |
| JOBID                          | cdm\_jobid.cdm\_name                                 |
| PARENTPOSITIONID               | cdm\_parentjobpositionid.cdm\_jobpositionnumber      |
| POSITIONTYPEID                 | cdm\_positiontypeid.cdm\_name                        |
| التقاعد                     | cdm\_retirement                                     |
| TITLEID                        | cdm\_titleid.cdm\_name                               |
| VALIDFROM                      | cdm\_validfrom                                      |
| VALIDTO                        | cdm\_validto                                        |

### <a name="jobs-dual-write-to-job"></a>الوظائف للكتابة المزدوجة للوظيفة

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| JOBID                          | cdm\_name                                           |
| الوصف                    | cdm\_description                                    |
| JOBDESCRIPTION                 | cdm\_jobdescription                                 |
| ALLOWUNLIMITEDPOSITIONS        | cdm\_allowunlimitedpositions                        |
| MAXIMUMNUMBEROFPOSITIONS       | cdm\_maximumnumberofpositions                       |
| JOBFUNCTIONID                  | cdm\_jobfunctionid.cdm\_name                         |
| JOBTYPEID                      | cdm\_jobtypeid.cdm\_name                             |
| TITLEID                        | cdm\_titleid.cdm\_name                               |
| VALIDFROM                      | cdm\_validfrom                                      |
| VALIDTO                        | cdm\_validto                                        |
| DEFAULTFULLTIMEEQUIVALENCY     | cdm\_defaultfulltimeequivalent                      |

### <a name="language-codes-to-language"></a>أكواد اللغة للغة

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| LANGUAGECODEID                 | cdm\_name                                           |
| الوصف                    | cdm\_description                                    |

### <a name="leave-and-absence-bank-transaction-v2-to-leave-bank-transaction"></a>‏‫الحركة البنكية للإجازة والغياب V2‬ للحركة البنكية للإجازة

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| المبلغ                         | cdm\_amount                                         |
| LEAVETYPEID                    | cdm\_leavetypeid.cdm\_type                           |
| LEAVEPLANID                    | cdm\_leaveplanid.cdm\_name                           |
| TRANSACTIONDATE                | cdm\_transactiondate                                |
| TRANSACTIONNUMBER              | cdm\_transactionnumber                              |
| PERSONNELNUMBER                | cdm\_workerid.cdm\_workernumber                      |
| TRANSACTIONTYPE                | cdm\_transactiontype                                |

### <a name="leave-and-absence-enrollment-v2-to-leave-enrollment"></a>‏‫تسجيل الإجازة والغياب V2‬ لتسجيل الإجازة

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| STARTDATE                      | cdm\_startdate                                      |
| ENDDATE                        | cdm\_enddate                                        |
| CUSTOMDATE                     | cdm\_customdate                                     |
| ACCRUALSTARTDATE               | cdm\_accrualstartdate                               |
| ACCRUALDATEBASIS               | cdm\_accrualdatebasis                               |
| ISACCRUALSUSPENDED             | cdm\_isaccrualsuspended                             |
| LEAVEPLANID                    | cdm\_leaveplanid.cdm\_name                           |
| TIERBASIS                      | cdm\_tierbasis                                      |
| PERSONNELNUMBER                | cdm\_workerid.cdm\_workernumber                      |

### <a name="leave-and-absence-plan-v2-to-leave-plan"></a>خطة الإجازة والغياب V2‬ لخطة الإجازة

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ACCRUALFREQUENCY               | cdm\_accrualfrequency                               |
| NAME                           | cdm\_name                                           |
| الوصف                    | cdm\_description                                    |
| STARTDATE                      | cdm\_startdate                                      |
| LEAVETYPEID                    | cdm\_leavetypeid.cdm\_type                           |

### <a name="leave-and-absence-type-to-leave-type"></a>نوع الإجازة والغياب لنوع الإجازة

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| الوصف                    | cdm\_description                                    |
| النوع                           | cdm\_type                                           |
| EARNINGCODEID                  | cdm\_earningcodeid.cdm\_name                         |

### <a name="leave-and-absence-type-reason-code-to-leave-type-reason-code"></a>‏‫رمز سبب نوع الإجازة والغياب ‏‫لرمز سبب نوع الإجازة

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| LEAVETYPE                      | cdm\_typeid.cdm\_type                                |
| REASONCODEID                   | cdm\_reasoncodeid.cdm\_name                          |

### <a name="leave-time-off-request-detail-to-leave-request-detail"></a>‏‫تفاصيل طلب الإجازة لتفاصيل طلب الإجازة

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| المبلغ                         | cdm\_amount                                         |
| LEAVEDATE                      | cdm\_leavedate                                      |
| REQUESTID                      | cdm\_leaverequestid.cdm\_leaverequestnumber          |
| النوع                           | cdm\_leavetypeid.cdm\_type                           |

### <a name="leave-time-off-request-header-to-leave-request"></a>عنوان طلب الإجازة لطلب الإجازة

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| REQUESTID                      | cdm\_leaverequestnumber                             |
| REQUESTDATE                    | cdm\_requestdate                                    |
| الحالة                         | cdm\_status                                         |
| COMMENT                        | cdm\_comment                                        |
| PERSONNELNUMBER                | cdm\_workerid.cdm\_workernumber                      |

### <a name="levels-to-compensation-level"></a>المستويات لمستوى التعويض

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| النوع                           | cdm\_type                                           |
| الوصف                    | cdm\_description                                    |
| LEVEL                          | cdm\_name                                           |

### <a name="onboarding-process-header-to-onboard-process-header"></a>عنوان عملية الإلحاق لعنوان عملية الإلحاق

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSID                      | cdm\_processheaderid.cdm\_processid                  |
| ONBOARDEDEMPLOYEEPERSONNELNUMBER | cdm\_onboardedemployeeid.cdm\_workernumber           |
| EMPLOYMENTPERSONNELNUMBER      | cdm\_employmentid.cdm\_workerid.cdm\_workernumber     |
| LEGALENTITYID                  | cdm\_employmentid.cdm\_companyid.cdm\_companycode     |
| EMPLOYMENTSTARTDATE            | cdm\_employmentid.cdm\_employmentstartdate           |

### <a name="pay-cycle-to-pay-cycle"></a>دورة الدفع لدورة الدفع

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| PAYCYCLEID                     | cdm\_name                                           |
| الوصف                    | cdm\_description                                    |
| PAYCYCLEFREQUENCY              | cdm\_frequency                                      |

### <a name="pay-period-to-pay-period"></a>فترة الدفع لفترة الدفع

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| التعليقات                       | cdm\_description                                    |
| DEFAULTPAYMENTDATE             | cdm\_defaultpaymentdate                             |
| PAYCYCLEID                     | cdm\_paycycleid.cdm\_name                            |
| PERIODENDDATE                  | cdm\_periodenddate                                  |
| PERIODSTARTDATE                | cdm\_periodstartdate                                |
| الحالة                         | cdm\_status                                         |

### <a name="payroll-details-for-positions-to-payroll-position-detail"></a>تفاصيل كشف الرواتب للمناصب لتفاصيل المنصب في كشف الرواتب

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| PAYCYCLEID                     | cdm\_paycycle.cdm\_name                              |
| POSITIONID                     | cdm\_position.cdm\_jobpositionnumber                 |
| VALIDFROM                      | cdm\_validfrom                                      |
| VALIDTO                        | cdm\_validto                                        |
| ANNUALREGULARHOURS             | cdm\_annualregularhours                             |
| PAIDBYLEGALENTITY              | cdm\_paidby.cdm\_companycode                         |

### <a name="position-default-dimensions-dual-write-to-job-position-dimension"></a>‏‫أبعاد الوضع الافتراضي للكتابة المزدوجة‬ ل‏‫بُعد منصب الوظيفة‬

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| DIMENSIONDISPLAYVALUE          | cdm\_dimensiondisplayvalue                          |
| POSITIONID                     | cdm\_jobpositionid.cdm\_jobpositionnumber            |

### <a name="position-type-to-position-type"></a>نوع المنصب لنوع المنصب

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| POSITIONTYPEID                 | cdm\_name                                           |
| الوصف                    | cdm\_description                                    |
| CLASSIFICATION                 | cdm\_classification                                 |

### <a name="position-worker-assignments-v2-to-position-worker-assignment"></a>‏‫تعيينات العاملين بالمناصب الإصدار 2‬ لتعيين العامل بالمنصب

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| PERSONNELNUMBER                | cdm\_workerid.cdm\_workernumber                      |
| POSITIONID                     | cdm\_jobpositionid.cdm\_jobpositionnumber            |
| VALIDFROM                      | cdm\_validfrom                                      |
| VALIDTO                        | cdm\_validto                                        |
| IsPrimaryPosition              | cdm\_isprimaryposition                              |

### <a name="reason-codes-to-reason-code"></a>رموز السبب لرمز السبب

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| REASONCODEID                   | cdm\_name                                           |
| الوصف                    | cdm\_description                                    |
| ISABSENCEAPPLICABLE            | cdm\_isabsenceapplicable                            |
| ISAPPLICATIONAPPLICABLE        | cdm\_isapplicationapplicable                        |
| ISCOMPENSATIONAPPLICABLE       | cdm\_iscompensationapplicable                       |
| ISCREATENEWPOSITIONAPPLICABLE  | cdm\_iscreatenewpositionapplicable                  |
| ISEDITPOSITIONAPPLICABLE       | cdm\_iseditpositionapplicable                       |
| ISHIREAPPLICABLE               | cdm\_ishireapplicable                               |
| ISSKILLMAPPINGAPPLICABLE       | cdm\_isskillmappingapplicable                       |
| ISTERMINATIONAPPLICABLE        | cdm\_isterminationapplicable                        |
| ISTRANSFERAPPLICABLE           | cdm\_istransferapplicable                           |

### <a name="reference-point-setup-line-dual-write-to-compensation-reference-point-setup-line"></a>‏‫بند إعداد النقطة المرجعية‬ (الكتابة المزدوجة) ل‏‫بند إعداد النقطة المرجعية للتعويض

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| الوصف                    | cdm\_description                                    |
| LINENUM                        | cdm\_linenumber                                     |
| REFPOINTID                     | cdm\_name                                           |
| REFPOINTSETUPID                | cdm\_referencepointsetupid.cdm\_name                 |

### <a name="reference-point-setups-to-compensation-reference-point-setup"></a>‏‫إعدادات النقاط المرجعية‬ ل‏‫إعداد النقاط المرجعية للتعويض‬

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| REFERENCESETUP                 | cdm\_name                                           |
| الوصف                    | cdm\_description                                    |
| النوع                           | cdm\_compensationtype                               |

### <a name="skill-types-to-skill-type"></a>أنواع المهارات لنوع المهارة

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| SKILLTYPE                      | cdm\_name                                           |
| الوصف                    | cdm\_description                                    |

### <a name="titles-to-title"></a>العناوين إلى العنوان

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| TITLEID                        | cdm\_name                                           |

### <a name="variable-compensation-level-v2-to-compensation-variable-plan-level"></a>مستوى التعويض المتغير الإصدار 2 لمستوى خطة التعويض المتغير

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| AWARDAMOUNT                    | cdm\_awardamount                                    |
| AWARDPERCENT                   | cdm\_awardpercent                                   |
| AWARDUNITSREAL                 | cdm\_awardunits                                     |
| COMPENSATIONLEVELID            | cdm\_compensationlevelid.cdm\_name                   |
| PLANID                         | cdm\_compensationvariableplanid.cdm\_name            |

### <a name="veteran-status-to-veteran-status"></a>حالة الخبرة لحالة الخبرة

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| VETERANSTATUSID                | cdm\_name                                           |
| الوصف                    | cdm\_description                                    |
| ISPROTECTEDVETERAN             | cdm\_isprotectedveteran                             |

### <a name="work-calendar-enrollments-to-work-calendar-enrollment"></a>‏‫تسجيلات تقويم العمل لتسجيل تقويم العمل

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| STARTDATE                      | cdm\_employmentid.cdm\_employmentstartdate           |
| PERSONNELNUMBER                | cdm\_employmentid.cdm\_workerid.cdm\_workernumber     |
| CALENDARID                     | cdm\_workcalendarid.cdm\_name                        |
| COMPANYID                      | cdm\_employmentid.cdm\_companyid.cdm\_companycode     |

### <a name="work-calendar-holiday-to-work-calendar-holiday"></a>‏‫إجازة تقويم العمل لإجازة تقويم العمل

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ID                             | cdm\_name                                           |
| الوصف                    | cdm\_description                                    |

### <a name="work-calendar-holiday-line-to-work-calendar-holiday-line"></a>بند ‏‫إجازة تقويم العمل لبند إجازة تقويم العمل

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| HOLIDAYID                      | cdm\_workcalendarholidayid.cdm\_name                 |
| NAME                           | cdm\_name                                           |
| HOLIDAYDATE                    | cdm\_holidaydate                                    |

### <a name="worker-to-worker"></a>العامل إلى العامل

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| PERSONNELNUMBER                | cdm\_workernumber                                   |
| FIRSTNAME                      | cdm\_firstname                                      |
| MIDDLENAME                     | cdm\_middlename                                     |
| LASTNAME                       | cdm\_lastname                                       |
| WORKERTYPE                     | cdm\_type                                           |
| WORKERSTATUS                   | cdm\_status                                         |
| PRIMARYCONTACTEMAIL            | cdm\_primaryemailaddress                            |
| PRIMARYCONTACTPHONE            | cdm\_primarytelephone                               |
| PRIMARYCONTACTFACEBOOK         | cdm\_facebookidentity                               |
| PRIMARYCONTACTTWITTER          | cdm\_twitteridentity                                |
| PRIMARYCONTACTLINKEDIN         | cdm\_linkedinidentity                               |
| PRIMARYCONTACTURL              | cdm\_websiteurl                                     |
| GENDER                         | cdm\_gender                                         |
| BIRTHDATE                      | cdm\_birthdate                                      |
| NAME                           | cdm\_fullname                                       |

### <a name="worker-bank-accounts-to-worker-bank-account"></a>الحسابات البنكية للعامل للحساب البنكي للعامل

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ACCOUNTIDENTIFICATION          | cdm\_accountidentification                          |
| ADDRESSCITY                    | cdm\_city                                           |
| ADDRESSCOUNTRYREGIONID         | cdm\_countryorregion                                |
| ADDRESSCOUNTY                  | cdm\_county                                         |
| ADDRESSDESCRIPTION             | cdm\_addressdescription                             |
| ADDRESSDISTRICTNAME            | cdm\_districtname                                   |
| ADDRESSPOSTBOX                 | cdm\_postofficebox                                  |
| ADDRESSSTATE                   | cdm\_stateorprovince                                |
| ADDRESSZIPCODE                 | cdm\_postalcode                                     |
| PERSONNELNUMBER                | cdm\_workerid.cdm\_workernumber                      |
| BANKACCOUNTNUMBER              | cdm\_bankaccountnumber                              |
| BANKACCOUNTTYPE                | cdm\_bankaccounttype                                |
| البريد الإلكتروني                          | cdm\_email                                          |
| EXTENSION                      | cdm\_extension                                      |
| FAX                            | cdm\_fax                                            |
| INTERNETADDRESS                | cdm\_websiteurl                                     |
| MOBILEPHONE                    | cdm\_mobilephone                                    |
| ROUTINGNUMBER                  | cdm\_routingnumber                                  |
| TELEPHONE                      | cdm\_telephone                                      |
| TELEXNUMBER                    | cdm\_telexnumber                                    |
| BANKIBAN                       | cdm\_iban                                           |
| SWIFTNO                        | cdm\_swiftcode                                      |
| BANKLOCATIONCODE               | cdm\_banklocationcode                               |
| BRANCHNAME                     | cdm\_branchname                                     |
| BRANCHNUMBER                   | cdm\_branchnumber                                   |
| ROUTINGNUMBERTYPE              | cdm\_routingnumbertype                              |
| ACCOUNTHOLDER                  | cdm\_accountholder                                  |
| NAMEOFPERSON                   | cdm\_nameofperson                                   |
| NAME                           | cdm\_description                                    |
| ADDRESSSTREET                  | cdm\_line1                                          |
| ADDRESSSTREETNUMBER            | cdm\_line2                                          |

### <a name="worker-personal-details-to-worker-personal-detail"></a>التفاصيل الشخصية للعامل للتفاصيل الشخصية للعامل

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| PERSONNELNUMBER                | cdm\_workerid.cdm\_workernumber                      |
| BIRTHDATE                      | cdm\_birthdate                                      |
| PERSONBIRTHCITY                | cdm\_birthcity                                      |
| GENDER                         | cdm\_gender                                         |
| EXPATRIATEENDDATE              | cdm\_expatriateenddate                              |
| EXPATRIATESTARTDATE            | cdm\_expatriatestartdate                            |
| DISABLEDVETERAN                | cdm\_isdisabledveteran                              |
| DECEASEDDATE                   | cdm\_deceaseddate                                   |
| DISABLEDVERIFICATIONDATE       | cdm\_disabledveteranverificationdate                |
| EDUCATION                      | cdm\_education                                      |
| ETHNICORIGINID                 | cdm\_ethnicoriginid.cdm\_name                        |
| ISDISABLED                     | cdm\_isdisabled                                     |
| ISFULLTIMESTUDENT              | cdm\_isfulltimestudent                              |
| ISEXPATRIATERULINGAPPLICABLE   | cdm\_isexpatriaterulingapplicable                   |
| MARITALSTATUS                  | cdm\_maritalstatus                                  |
| MILITARYSERVICESTARTDATE       | cdm\_militaryservicestartdate                       |
| MILITARYSERVICEENDDATE         | cdm\_militaryserviceenddate                         |
| NUMBEROFDEPENDENTS             | cdm\_numberofdependents                             |
| NATIVELANGUAGEID               | cdm\_nativelanguageidid.cdm\_name                    |
| NATIONALITYCOUNTRYREGION       | cdm\_nationalitycountryregion                       |
| PERSONBIRTHCOUNTRYREGION       | cdm\_birthcountryregion                             |
| FATHERBIRTHCOUNTRYREGION       | cdm\_fatherbirthcountryregion                       |
| MOTHERBIRTHCOUNTRYREGION       | cdm\_motherbirthcountryregion                       |
| CITIZENSHIPCOUNTRYREGION       | cdm\_citizenshipcountryregion                       |
| VETERANSTATUSID                | cdm\_veteranstatusid.cdm\_name                       |

### <a name="worker-postal-addresses-dual-write-to-worker-address"></a>‏‫العناوين البريدية للعامل‬ للكتابة المزدوجة لعنوان العامل

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| PERSONNELNUMBER                | cdm\_workerid.cdm\_workernumber                      |
| ADDRESSLOCATIONID              | cdm\_addressnumber                                  |
| ADDRESSLOCATIONROLES           | cdm\_addresstype                                    |
| EFFECTIVE                      | cdm\_effectivedate                                  |
| انتهاء الصلاحية                     | cdm\_expirationdate                                 |
| ADDRESSSTREET                  | cdm\_street                                         |
| ADDRESSSTREETNUMBER            | cdm\_streetnumber                                   |
| ADDRESSCITY                    | cdm\_city                                           |
| ADDRESSCOUNTRYREGIONISOCODE    | cdm\_countryregion                                  |
| ADDRESSSTATE                   | cdm\_stateorprovince                                |
| ADDRESSCOUNTYID                | cdm\_county                                         |
| ADDRESSDESCRIPTION             | cdm\_description                                    |
| ADDRESSLATITUDE                | cdm\_latitude                                       |
| ADDRESSLONGITUDE               | cdm\_longitude                                      |
| ADDRESSZIPCODE                 | cdm\_postalcode                                     |
| ADDRESSPOSTBOX                 | cdm\_postofficebox                                  |
| ISPRIMARY                      | cdm\_ispreferred                                    |

### <a name="working-time-to-work-calendar-time-interval"></a>أوقات العمل للفاصل الزمني لتقويم العمل

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| ENDTIME                        | cdm\_endtime                                        |
| STARTTIME                      | cdm\_starttime                                      |
| WORKCALENDARDATE               | cdm\_workcalendardayid.cdm\_calendardate             |
| WORKCALENDARID                 | cdm\_workcalendarid.cdm\_name                        |
| WORKCALENDARID                 | cdm\_workcalendardayid.cdm\_workcalendarid.cdm\_الاسم  |

### <a name="working-times-to-work-calendar-day"></a>أوقات العمل ليوم تقويم العمل

| كيان Finance                 | جدول Dataverse                                    | 
|--------------------------------|----------------------------------------------------|
| CALENDARDATE                   | cdm\_calendardate                                   |
| WORKCALENDARID                 | cdm\_workcalendarid.cdm\_name                        |
| WORKINGDAYDEFINITION           | cdm\_status                                         |

## <a name="integration-considerations"></a>اعتبارات التكامل

- ستخضع كافة التغييرات التي يتم إجراؤها على البيانات في أي نظام للتحقق من النظام الآخر. وفي حالة حدوث فشل، لن تتم كتابة البيانات في أي من النظامين. 
- كافة الكتابات تخضع للبيانات الافتراضية (في حالة حدوث منطق مخصص في Finance).
- يستخدم التطبيق الموحد للكتابة المزدوجة مفاتيح التكامل للتعيين بين النظامين. في بعض الأحيان، من الصعب اختيار مفتاح التكامل الصحيح، خصوصًا إذا كانت مفاتيح تكامل متعددة تستوفي المتطلبات. للمساعدة في هذا الاختيار، يسرد الجدول التالي مفاتيح التكامل المقترحة للتعيينات الخاصة بك.

| جدول Dataverse                          | مفاتيح تكامل |
|------------------------------------------|------------------|
| مصروف الحساب البنكي                | cdm\_bankaccountid.cdm\_accountidentification, cdm\_bankaccountid.cdm\_workerid.cdm\_workernumber, cdm\_companyid.cdm\_companycode |
| تكرار حساب الميزة            | cdm\_name |
| حساب تكرار فترة دفع الميزة | cdm\_payperiodid.cdm\_periodstartdate, cdm\_payperiodid.cdm\_paycycleid.cdm\_name, cdm\_benefitcalculationfrequencyid.cdm\_الاسم |
| معدل حساب الميزة                 | cdm\_name |
| تفاصيل معدل حساب الميزة          | cdm\_workerdeduction, cdm\_effective, cdm\_calculationrateid.cdm\_الاسم |
| خيار الميزة                           | cdm\_name |
| نوع الميزة                             | cdm\_name |
| تقويم عملية الأعمال                | cdm\_name |
| تعيين مجموعة عمليات الأعمال        | cdm\_name |
| رأس عملية الأعمال                  | cdm\_processid |
| مجموعة مهام مكتبة عمليات الأعمال      | cdm\_processtype, cdm\_name |
| مرحلة عملية الأعمال‬                   | cdm\_name, cdm\_businessprocesstype, cdm\_companyid.cdm\_companycode |
| مهمة دورة العمل                    | cdm\_taskid |
| وحدة الأعمال                            | |
| رأس قالب قائمة الاختيار                | cdm\_businessprocesstype, cdm\_name, cdm\_genericsubtype |
| مهمة قالب قائمة الاختيار                  | cdm\_taskid |
| الشركة                                  | cdm\_companycode |
| خطة التعويض الثابت                  | cdm\_name, cdm\_company.cdm\_companycode |
| شبكة التعويض                        | cdm\_name, cdm\_companyid.cdm\_companycode |
| مستوى التعويض                       | cdm\_name |
| تكرار دفع التعويض               | cdm\_name, cdm\_companyid.cdm\_companycode |
| إعداد النقاط المرجعية للتعويض       | cdm\_name, cdm\_companyid.cdm\_companycode |
| إعداد بند النقاط المرجعية للتعويض  | cdm\_name, cdm\_referencepointsetupid.cdm\_name, cdm\_referencepointsetupid.cdm\_companyid.cdm\_companycode |
| منطقة التعويض                      | cdm\_name |
| بنية التعويض                   | cdm\_compensationlevelid.cdm\_name, cdm\_referencepointid.cdm\_name, cdm\_referencepointid.cdm\_referencepointsetupid.cdm\_name, cdm\_referencepointid.cdm\_referencepointsetupid.cdm\_companyid.cdm\_companycode, cdm\_companyid.cdm\_companycode, cdm\_compensationgridid.cdm\_name, cdm\_compensationgridid.cdm\_companyid.cdm\_companycode |
| خطة التعويض المتغير               | cdm\_name, cdm\_companyid.cdm\_companycode |
| مستوى خطة التعويض المتغير         | cdm\_companyid.cdm\_companycode, cdm\_compensationvariableplanid.cdm\_name, cdm\_compensationvariableplanid.cdm\_companyid.cdm\_companycode, cdm\_compensationlevelid.cdm\_name |
| نوع خطة التعويض المتغير          | cdm\_name, cdm\_companyid.cdm\_companycode |
| عملة                                 | isocurrencycode |
| قسم                               | cdm\_departmentnumber |
| التوظيف                               | cdm\_employmentstartdate, cdm\_workerid.cdm\_workernumber, cdm\_companyid.cdm\_companycode |
| الأصل العرقي                            | cdm\_name |
| حدث التعويض الثابت                 | cdm\_name, cdm\_companyid.cdm\_companycode |
| وظيفة                                      | cdm\_name |
| مهمة الوظيفة                             | cdm\_name |
| منصب الوظيفة                             | cdm\_jobpositionnumber |
| بُعد منصب الوظيفة                   | cdm\_jobpositionid.cdm\_jobpositionnumber, cdm\_companyid.cdm\_companycode |
| نوع الوظيفة                                 | cdm\_name |
| اللغة                                 | cdm\_name |
| حركة بنك الإجازة                   | cdm\_transactiondate, cdm\_transactiontype, cdm\_transactionnumber, cdm\_leavetypeid.cdm\_type, cdm\_leavetypeid.cdm\_companyid.cdm\_companycode, cdm\_companyid.cdm\_companycode, cdm\_workerid.cdm\_workernumber |
| تسجيل الإجازات                         | cdm\_startdate, cdm\_leaveplanid.cdm\_name, cdm\_leaveplanid.cdm\_companyid.cdm\_companycode, cdm\_companyid.cdm\_companycode, cdm\_workerid.cdm\_workernumber |
| خطة الإجازة                               | cdm\_name, cdm\_companyid.cdm\_companycode |
| طلب الإجازة                            | cdm\_leaverequestnumber, cdm\_companyid.cdm\_companycode |
| تفاصيل طلب المستخدم                     | cdm\_leavedate, cdm\_leavetypeid.cdm\_type, cdm\_leavetypeid.cdm\_companyid.cdm\_companycode, cdm\_leaverequestid.cdm\_leaverequestnumber, cdm\_leaverequestid.cdm\_companyid.cdm\_companycode |
| نوع الإجازة                               | cdm\_type, cdm\_companyid.cdm\_companycode |
| كود سبب نوع الإجازة‬                   | cdm\_reasoncodeid.cdm\_name, cdm\_typeid.cdm\_type, cdm\_typeid.cdm\_companyid.cdm\_companycode |
| رأس عملية الإعداد                   | cdm\_processheaderid.cdm\_processid |
| المؤسسة                             | |
| دورة الدفع                                | cdm\_name |
| فترة الدفع                               | cdm\_periodstartdate, cdm\_paycycleid.cdm\_name, cdm\_periodenddate |
| كود أرباح كشف الرواتب                     | cdm\_name |
| تفصيل المنصب في كشف الرواتب                  | cdm\_validfrom, cdm\_validto, cdm\_position.cdm\_jobpositionnumber |
| وكالة إصدار هوية العامل     | cdm\_name |
| نوع المنصب                            | cdm\_name |
| تعيين العامل بالمنصب               | cdm\_validfrom, cdm\_jobpositionid.cdm\_jobpositionnumber |
| كود السبب                              | cdm\_name |
| نوع المهارة                               | cdm\_name |
| منطقة الضريبة                               | cdm\_stateorprovince, cdm\_name, cdm\_countryorregion, cdm\_county, cdm\_city |
| الفريق                                     | azureactivedirectoryobjectid, membershiptype |
| العنوان‬                                    | cdm\_name |
| المستخدم                                     | azureactivedirectoryobjectid |
| قاعدة الاستحقاق                             | cdm\_name, cdm\_companyid.cdm\_companycode |
| حالة الخبير                           | cdm\_name |
| تقويم العمل                            | cdm\_name, cdm\_companyid.cdm\_companycode |
| يوم تقويم العمل                        | cdm\_calendardate, cdm\_companyid.cdm\_companycode, cdm\_workcalendarid.cdm\_name, cdm\_workcalendarid.cdm\_companyid.cdm\_companycode |
| تسجيل تقويم العمل                 | cdm\_employmentid.cdm\_employmentstartdate, cdm\_employmentid.cdm\_workerid.cdm\_workernumber, cdm\_employmentid.cdm\_companyid.cdm\_companycode |
| إجازة تقويم العمل                    | cdm\_name |
| بند أجازة تقويم العمل               | cdm\_holidaydate, cdm\_workcalendarholidayid.cdm\_name |
| الفاصل الزمني لتقويم العمل              | cdm\_starttime, cdm\_workcalendardayid.cdm\_calendardate, cdm\_workcalendardayid.cdm\_companyid.cdm\_companycode, cdm\_workcalendardayid.cdm\_workcalendarid.cdm\_name, cdm\_workcalendardayid.cdm\_workcalendarid.cdm\_companyid.cdm\_companycode, cdm\_companyid.cdm\_companycode, cdm\_workcalendarid.cdm\_name, cdm\_workcalendarid.cdm\_companyid.cdm\_companycode |
| العامل                                   | cdm\_workernumber |
| عنوان العامل                           | cdm\_addressnumber, cdm\_addresstype, cdm\_workerid.cdm\_workernumber |
| الحساب البنكي للعامل                      | cdm\_accountidentification, cdm\_workerid.cdm\_workernumber |
| التعويض الثابت للعاملين                | cdm\_linenumber, cdm\_effectivedate, cdm\_companyid.cdm\_companycode, cdm\_positionid.cdm\_jobpositionnumber, cdm\_workerid.cdm\_workernumber, cdm\_eventid.cdm\_name, cdm\_eventid.cdm\_companyid.cdm\_companycode, cdm\_planid.cdm\_name, cdm\_planid.cdm\_company.cdm\_companycode |
| رقم الهوية الشخصية للعامل      | cdm\_identificationnumber, cdm\_workerid.cdm\_workernumber, cdm\_identificationtypeid.cdm\_name |
| نوع الهوية الشخصية للعامل        | cdm\_name |
| التفاصيل الشخصية للعامل                   | cdm\_workerid.cdm\_workernumber |
