---
title: 'تكوين التكامل مع Finance '
description: توضح هذه المقاولة الوظيفة المتاحة للتكامل من Dynamics 365 Human Resources و Dynamics 365 Finance.
author: andreabichsel
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3b4d6369ab567879e23e1f132265aaff45c8ce47
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527899"
---
# <a name="configure-integration-with-finance"></a>تكوين التكامل مع Finance

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

لاجراء تكامل Dynamics 365 Human Resources مع Dynamics 365 Finance، يمكنك استخدام Human Resources في قالب Finance في [مكامل بيانات ](https://docs.microsoft.com/powerapps/administrator/data-integrator). تتيح Human Resources لقالب Finance تدفق البيانات للوظائف والمناصب والعاملين. يسمح القالب بتدفق البيانات من Human Resources إلى Finance، لكنه لا يسمح بتدفق البيانات من Finance إلى Human Resources.

![تدفق تكامل Human Resources إلى Finance](./media/hr-admin-integration-finance-flow.png)

يوفر حل Human Resources إلى Finance الأنواع التالية من مزامنة البيانات:

- الاحتفاظ بالوظائف في Human Resources ومزامنتها من Human Resources إلى Finance
- الاحتفاظ بالمناصب ومهام المناصب في Human Resources ومزامنتها من Human Resources إلى Finance
- الاحتفاظ بعمليات التوظيف في Human Resources ومزامنتها من Human Resources إلى Finance
- الاحتفاظ بالعمال وعناوين العمال في Human Resources ومزامنتها من Human Resources إلى Finance

## <a name="system-requirements-for-human-resources"></a>متطلبات النظام لـ Human Resourcesـ

يتطلب حل التكامل الإصدارات التالية من Human Resources و Finance: 

- Dynamics 365 Human Resources في Common Data Service
- الإصدار 7.2 من Dynamics 365 Finance والإصدار اللاحق

## <a name="template-and-tasks"></a>القوالب والمهام

للوصول إلى قالب Human Resources إلى Finance.

1. فتح [مركز مسؤول Power Apps](https://admin.powerapps.com/). 

2. حدد **المشاريع**، ثم حدد **مشروع جديد** في الركن الأيمن العلوي. أنشئ مشروع جديد لكل كيان قانوني ترغب في تكامله في Finance.

3. حدد **Human Resources (Human Resources Common Data Service إلى Finance)** لمزامنة السجلات من Human Resources إلى Finance.

يستخدم القالب المهام الأساسية التالية لمزامنة السجلات من Human Resources إلى Finance:

- **مهام الوظائف إلى مهمة وظيفة التعويض**
- **الأقسام إلى وحدة التشغيل**
- **أنواع الوظائف لنوع وظيفة التعويض**
- **وظائف للوظائف**
- **وظائف لتفاصيل الوظيفة**
- **أنواع المناصب لنوع المنصب**
- **المناصب الوظيفية إلى المنصب الأساسي**
- **مناصب الوظيفة إلى تفاصيل المناصب**
- **المناصب الوظيفية إلى مُدد المنصب**
- **المناصب الوظيفية إلى التدرجات الهرمية للمناصب**
- **العاملون إلى العامل**
- **عمليات التوظيف إلى التوظيف**
- **عمليات التوظيف إلى تفاصيل التوظيف**
- **تعيين العامل بالمنصب إلى تعيينات العاملين بالمناصب**
- **عناوين العاملين إلى العنوان البريدي للعامل V2**

## <a name="template-mappings"></a>تعيينات القالب

في جداول تعيين القوالب التالية، يحتوي اسم المهمة على الكيانات المستخدمة في كل تطبيق. يقع مصدر (Human Resources) على اليسار والوجهة (Finance) على اليمين.

### <a name="job-functions-to-compensation-job-function"></a>مهام الوظائف إلى مهمة وظيفة التعويض

| كيان Common Data Service (المصدر) | كيان Finance (الوجهة) |
|-------------------------------------|---------------------------------------------|
| cdm_name (cdm_Job   اسم الوظيفة)  | JOBFUNCTIONID   (JOBFUNCTIONID)            |
| cdm_description   (cdm_description) | الوصف   (الوصف)                 |

### <a name="departments-to-operating-unit"></a>الأقسام إلى وحدة التشغيل

| كيان Common Data Service (المصدر)           | كيان Finance (الوجهة) |
|-----------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                           | الاسم (الاسم)                                 |
| cdm_departmentnumber   (cdm_departmentnumber) | OPERATINGUNITNUMBER   (OPERATINGUNITNUMBER) |
|                                               | OPERATINGUNITTYPE   (OPERATINGUNITTYPE)     |
| cdm_description   (cdm_description)           | NAMEALIAS   (NAMEALIAS)                     |

### <a name="job-types-to-compensation-job-type"></a>أنواع الوظائف لنوع وظيفة التعويض

| كيان Common Data Service (المصدر)   | كيان Finance (الوجهة) |
|---------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                   | JOBTYPEID   (JOBTYPEID)                     |
| cdm_description   (cdm_description)   | الوصف   (الوصف)                 |
| cdm_exemptstatus   (cdm_exemptstatus) | EXEMPTSTATUS   (EXEMPTSTATUS)               |

### <a name="jobs-to-jobs"></a>وظائف للوظائف

| كيان Common Data Service (المصدر)                           | كيان Finance (الوجهة)           |
|---------------------------------------------------------------|-------------------------------------------------------|
| cdm_name (cdm_name)                                           | JOBID (JOBID)                                         |
| cdm_maximumnumberofpositions   (cdm_maximumnumberofpositions) | MAXIMUMNUMBEROFPOSITIONS   (MAXIMUMNUMBEROFPOSITIONS) |
| cdm_allowedunlimitedpositions   (cdm_allowunlimitedpositions) | ALLOWUNLIMITEDPOSITIONS   (ALLOWUNLIMITEDPOSITIONS)   |
| cdm_description   (cdm_description)                           | الوصف   (الوصف)                           |
| cdm_jobdescription   (cdm_jobdescription)                     | JOBDESCRIPTION   (JOBDESCRIPTIONS)                    |

### <a name="jobs-to-job-detail"></a>وظائف لتفاصيل الوظيفة

| كيان Common Data Service (المصدر)                             | كيان Finance (الوجهة) |
|-----------------------------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                                             | JOBID (JOBID)                               |
| cdm_jobtypeid.cdm_name   (Job Type (Job Type Name))             | JOBTYPEID   (JOBTYPEID)                     |
| cdm_jobfunctionid.cdm_name   (Job Function (Job Function Name)) | FUNCTIONID   (FUCNTIONID)                   |
| cdm_validfrom (صالح من)                                    | VALIDFROM   (VALIDFROM)                     |
| cdm_validto (صالح إلى)                                        | VALIDTO (VALIDTO)                           |
| cdm_defaultfulltimeequivalent (مُكافئ الدوام الكامل الافتراضي)   | FULLTIMEEQUIVALENT   (FULLTIMEEQUIVALENT)   |

### <a name="position-types-to-position-type"></a>أنواع المناصب لنوع المنصب

| كيان Common Data Service (المصدر)       | كيان Finance (الوجهة) |
|-------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                       | POSITIONTYPEID   (POSITIONTYPEID)           |
| cdm_description   (cdm_description)       | الوصف   (الوصف)                 |
| cdm_classification   (cdm_classification) | التصنيف   (التصنيف)           |

### <a name="job-positions-to-base-position"></a>المناصب الوظيفية إلى المنصب الأساسي

| كيان Common Data Service (المصدر)           | كيان Finance (الوجهة) |
|-----------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber   (رقم منصب الوظيفة) | POSITIONID (POSITIONID)                      |

### <a name="job-positions-to-position-details"></a>مناصب الوظيفة إلى تفاصيل المناصب

| كيان Common Data Service (المصدر)              | كيان Finance (الوجهة)       |
|--------------------------------------------------------------------------|---------------------------------------------------|
| cdm_jobpositionnumber (رقم منصب الوظيفة)                            | POSITIONID (POSITIONID)                             |
| cdm_jobid.cdm_name   (الوظيفة (الاسم))                                        | JOBID (JOBID)                                    |
| cdm_description   (cdm_description)                                        | الوصف   (الوصف)                       |
| cdm_departmentid.cdm_departmentnumber   (القسم (رقم القسم)) | DEPARTMENTNUMBER   (DEPARTMENTNUMBER)             |
| cdm_positiontypeid.cdm_name   (نوع المنصب (الاسم))                     | POSITIONTYPEID   (POSITIONTYPEID)                 |
| cdm_avaialableforassignment (متوفر للتعيين)                 | AVAILABLEFORASSIGNMENT   (AVAILABLEFORASSIGNMENT) |
| cdm_validfrom (صالح من)                                            | VALIDFROM   (VALIDFROM)                           |
| cdm_validto (صالح إلى)                                                 | VALIDTO (VALIDTO)                               |
| cdm_fulltimeequivalent   (مُكافئ الدوام الكامل)                           | FULLTIMEEQUIVALENT   (FULLTIMEEQUIVALENT)         |

### <a name="job-positions-to-position-durations"></a>المناصب الوظيفية إلى مُدد المنصب

| كيان Common Data Service (المصدر)             | كيان Finance (الوجهة) |
|-------------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber   (رقم منصب الوظيفة)   | POSITIONID (POSITIONID)                      |
| التنشيط المحسوب (التنشيط المحسوب) | VALIDFROM (VALIDFROM)                        |
| التقاعد المحسوب (التقاعد المحسوب) | VALIDTO (VALIDTO)                         |

### <a name="job-positions-to-position-hierarchies"></a>المناصب الوظيفية إلى التدرجات الهرمية للمناصب

| كيان Common Data Service (المصدر)        | كيان Finance (الوجهة) |
|-----------------------------------------------------------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber   (رقم منصب الوظيفة)                                                 | POSITIONID(POSITIONID)                      |
| cdm_parentjobpositionid.cdmjobpositionnumber   (cdm_parentjobpositionid.cdmjobpositionnumber) | PARENTPOSITIONID (PARENTPOSITIONID)         |
| cdm_validfrom (صالح من)                                                                  | VALIDFROM   (VALIDFROM)                     |
| cdm_validto (صالح إلى)                                                                      | VALIDTO (VALIDTO)                           |
| HIERARCHYTYPENAME   (HIERARCHYTYPENAME)                                                       | HIERARCHYTYPENAME   (HIERARCHYTYPENAME)     |


### <a name="workers-to-worker"></a>العاملون إلى العامل
| كيان Common Data Service (المصدر)           | كيان Finance (الوجهة)       |
|-----------------------------------------------|---------------------------------------------------|
| cdm_birthdate   (cdm_birthdate)               | BIRTHDATE   (BIRTHDATE)                           |
| cdm_gender   (cdm_gender)                     | GENDER (GENDER)                                   |
| cdm_primaryaddress   (cdm_primaryaddress)     | PRIMARYCONTACTEMAIL   (PRIMARYCONTACTEMAIL )      |
| cdm_primarytelephone   (cdm_primarytelephone) | PRIMARYCONTACTPHONE   (PRIMARYCONTACTPHONE)       |
| cdm_facebookidentity   (cdm_facebookidentity) | PRIMARYCONTACTFACEBOOK   (PRIMARYCONTACTFACEBOOK) |
| cdm_twitteridentity   (cdm_twitteridentity)   | PRIMARYCONTACTTWITTER   (PRIMARYCONTACTTWITTER)   |
| cdm_linkedinIdentity   (cdm_linkedinIdentity) | PRIMARYCONTACTLINKEDIN   (PRIMARYCONTACTLINKEDIN) |
| cdm_websiteurl   (cdm_websiteurl)             | PRIMARYCONTACTURL   (PRIMARYCONTACTURL)           |
| cdm_firstname   (cdm_firstname)               | FIRSTNAME   (FIRSTNAME)                           |
| cdm_middlename   (cdm_middlename)             | MIDDLENAME   (MIDDLENAME)                         |
| cdm_lastname   (cdm_lastname)                 | LASTNAME (LASTNAME)                               |
| cdm_workernumber   (cdm_workernumber)         | PERSONNELNUMBER   (PERSONNELNUMBER)               |
| cdm_type (cdm_type)                           | WORKERTYPE   (WORKERTYPE)                         |
| cdm_state   (cdm_state)                       | WORKSTATUS   (WORKERSTATUS)                       |

### <a name="employments-to-employment"></a>عمليات التوظيف إلى التوظيف

| كيان Common Data Service (المصدر)                             | كيان Finance (الوجهة) |
|-----------------------------------------------------------------|---------------------------------------------|
| cdm_employmentstartdate   (cdm_employmentstartdate)             | EMPLOYMENTSTARTDATE   (EMPLOYMENTSTARTDATE) |
| cdm_employmentenddate   (cdm_employmentenddate)                 | EMPLOYMENTENDDATE   (EMPLOYMENTENDDATE)     |
| cdm_workertype   (cdm_workertype)                               | WORKERTYPE   (WORKERTYPE)                   |
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)         |
| cdm_companyid.cdm_companycode   (cdm_companyid.cdm_companycode) | LEGALENTITYID   (LEGALENTITYID)             |

### <a name="employments-to-employment-detail"></a>عمليات التوظيف إلى تفاصيل التوظيف

| كيان Common Data Service (المصدر)                             | كيان Finance (الوجهة)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_employmentstartdate   (cdm_employmentstartdate)             | EMPLOYMENTSTARTDATE   (EMPLOYMENTSTARTDATE)   |
| cdm_employmentenddate   (cdm_employmentenddate)                 | EMPLOYMENTENDDATE   (EMPLOYMENTENDDATE)       |
| cdm_validfrom (صالح من)                                    | VALIDFROM   (VALIDFROM)                       |
| cdm_validto (صالح إلى)                                        | VALIDTO (VALIDTO)                             |
| cdm_workerstartdate   (cdm_workerstartdate)                     | WORKERSTARTDATE   (WORKERSTARTDATE)           |
| cdm_lastdateworked   (cdm_lastdateworked)                       | LASTDATEWORKED   (LASTDATEWORKED)             |
| cdm_transitiondate   (cdm_transitiondate)                       | TRANSITIONDATE   (TRANSITIONDATE)             |
| cdm_employerunitofnotice   (cdm_employerunitofnotice)           | EMPLOYERUNITOFNOTICE   (EMPLOYERUNITOFNOTICE) |
| cdm_workerunitofnotice   (cdm_workerunitofnotice)               | WORKERUNITOFNOTICE   (WORKERUNITOFNOTICE)     |
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_companyid.cdm_companycode   (cdm_companyid.cdm_companycode) | LEGALENTITYID   (LEGALENTITYID)               |
| cdm_employernoticeamount   (cdm_employernoticeamount)           | EMPLOYERNOTICEAMOUNT   (EMPLOYERNOTICEAMOUNT) |
| cdm_workernoticeamount   (cdm_workernoticeamount )              | WORKERNOTICEAMOUNT   (WORKERNOTICEAMOUNT)     |

### <a name="position-worker-assignment-to-position-worker-assignments"></a>تعيين العامل بالمنصب إلى تعيينات العاملين بالمناصب

| كيان Common Data Service (المصدر)                             | كيان Finance (الوجهة)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_jobpositionnumber   (رقم منصب الوظيفة)                   | POSITIONID(POSITIONID)                        |
| cdm_validfrom (صالح من)                                    | VALIDFROM   (VALIDFROM)                       |
| cdm_validto (صالح إلى)                                        | VALIDTO (VALIDTO)                             |

### <a name="worker-addresses-to-worker-postal-address-v2"></a>عناوين العاملين إلى العنوان البريدي للعامل V2

| كيان Common Data Service (المصدر)                             | كيان Finance (الوجهة)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_addresstype   (cdm_addresstype)                             | ADDRESSLOCATIONROLES   (ADDRESSLOCATIONROLES) |
| cdm_line1   (cdm_line1)                                         | ADDRESSSTREET   (ADDRESSSTREET)               |
| cdm_city (cdm_city)                                             | ADDRESSCITY   (ADDRESSCITY)                   |
| cdm_stateorprovince   (cdm_stateorprovince)                     | ADDRESSSTATE   (ADDRESSSTATE)                 |
| cdm_postalcode   (cdm_postalcode)                               | ADDRESSZIPCODE(ADDRESSZIPCODE)                |
| cdm_countryregion   (cdm_countryregion)                         | ADDRESSCOUNTRYREGION(ADDRESSCOUNTRYREGION)    |
| cdm_addressnumber   (cdm_addressnumber)                         | ADDRESSLOCATIONID(ADDRESSLOCATIONID)          |
| cdm_ispreferred   (cdm_ispreferred)                             | ISPRIMARY   (ISPRIMARY)                       |
| cdm_county   (cdm_county)                                       | ADDRESSCOUNTYID(ADDRESSCOUNTYID)              |
| cdm_addresstype   (cdm_addresstype)                             | ADDRESSDESCRIPTION(ADDRESSDESCRIPTION)        |

## <a name="integration-considerations"></a>اعتبارات التكامل

يحاول التكامل من Human Resources إلى Finance مطابقة السجلات بناءً على المُعرف. في حالة تطابق السجلات، يستبدل مكامل البيانات البيانات الموجودة في Finance بالقيم الموجودة في Human Resources. ومع ذلك، قد تحدث مشكلة إذا كانت هذه سجلات مختلفة منطقيًا وتم إنشاء نفس المعرّف في أي من Human Resources أو Finance استنادًا إلى تسلسل الأرقام المعني.

قد تحدث هذه المشكلة لدى **العامل**، الذي يستخدم **رقم الموظف** لإجراء المطابقة، و **المناصب**. لا تستخدم الوظائف التسلسلات الرقمية. ونتيجة لذلك، إذا كان نفس مُعرف الوظيفة موجودًا في كل من Human Resources و Finance، تقوم معلومات Human Resources باستبدال معلومات Dynamics 365 Finance. 

لمنع حدوث مشكلات مع مُعرفات مُكررة، يُمكنك إما إضافة بادئة على [تسلسل الرقم](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/number-sequence-overview?toc=/dynamics365/unified-operations/talent/toc.json)، أو تعيين رقم بداية على التسلسل الرقمي الموجود خارج نطاق النظام الآخر. 

لا يُمثل مُعرف الموقع المستخدم لعنوان العامل جزءًا من تسلسل رقمي. عند تكامل عنوان عامل من Human Resources إلى Finance، إذا كان عنوان العامل موجودًا بالفعل في Finance، فمن ثم يجوز إنشاء سجل عنوان مكرر. 

يبين الشكل التوضيحي التالي مثالاً لتعيين قالب في موحد البيانات. 

![تعيين القالب](./media/IntegrationMapping.png)