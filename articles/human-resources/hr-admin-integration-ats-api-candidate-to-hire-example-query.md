---
title: مثال الاستعلام عن مرشح مراد توظيفه
description: يقدم هذا الموضوع مثالا للاستعلام عن المرشح مطلوب لكيان التوظيف في Dynamics 365 Human Resources.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 963e12e9114664a995b92ffe22063c14f904da35
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125751"
---
# <a name="example-query-for-candidate-to-hire"></a>مثال الاستعلام عن مرشح مراد توظيفه

يقدم هذا الموضوع مثالا للاستعلام عن المرشح مطلوب لكيان التوظيف في Dynamics 365 Human Resources.

يوفر هذا الموضوع مثالا يوضح كيفية استخدام *الإدراجات العميقة* لإنشاء كافة التفاصيل لسجل مرشح جديد في عملية API واحدة. لمزيد من المعلومات حول الإدراجات العميقة، راجع [إنشاء سجلات الكيان المرتبط في عملية واحدة](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-entity-web-api#create-related-entity-records-in-one-operation).

يعد الكيان **mshr_hcmcandidatetohireentity** فريدًا نظرًا علاقته بالكيان **mshr_dirpersonentity**. يتم اشتقاق العديد من الخصائص في **mshr_hcmcandidatetohireentity** (على سبيل المثال، **mshr_firstname** و **mshr_lastname** و **mshr_birthdate**) من سجل **mshr_dirpersonentity**. إذا قمت بترحيل سجل مرشح جديد إلى **mshr_hcmcandidatetohireentity** بدون استخدام الإدراج العميق، فيمكنك تعريف قيم لهذه الخصائص مباشرة على السجل **mshr_hcmcandidatetohireentity**. يتم إنشاء سجل **mshr_dirpersonentity** المرتبط ضمنيًا بالقيم المعرفة للخصائص. ويمكنك بعد ذلك إنشاء أية سجلات كيانات أخرى ذات صلة (مثل المهارات أو التعليم) على أنها استدعاءات API منفصلة.

ومع ذلك، إذا أردت استخدام الإدراجات العميقة لإنشاء كافة الكيانات ذات الصلة في عملية واحدة، بيجب تحديد الخصائص الخاصة بالكيان **mshr_dirpersonentity** على هذا المستوى المتداخل للعملية.

يوضح هذا المثال كيف يمكنك إنشاء سجل مرشح وسجل الشخص المقترن ومهارات الشخص والتعليم في ثلاثة مستويات متداخلة باستخدام عمليات الإدراج العميقة في عملية API واحدة.

> [!NOTE]
> لا يتضمن المثال كافة خصائص كل من كيانات واجهة برمجة التطبيقات (API). وهي مبسطة لأغراض التوضيح.

**الطلب**

```http

POST [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities
Content-Type: application/json; charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0
Accept: application/json

{
    "mshr_dataareaid": "usmf",
    "mshr_recruitingrequestid": "USMF-000141",
    "mshr_positionid": "000601",
    "mshr_iswillingtorelocate": 200000000,
    "mshr_availabilitydate": "2021-03-18",
    "mshr_comments": "Evelyn's experience is exactly what we need for this position.",
    "mshr_FK_Person_id":
        {
            "mshr_firstname": "Evelyn",
            "mshr_lastname": "Chambers",
            "mshr_namesequencedisplayas": "FirstMiddleLast",
            "mshr_FK_HcmPersonSkillEntity_Person":
            [
                {
                    "mshr_skillid": "CustFocus",
                    "mshr_ratingid": "Skills",
                    "mshr_levelid": "4",
                    "mshr_ratinglevelexaminer": "",
                    "mshr_leveltype": 200000000,
                    "mshr_yearsofexperience": 0,
                    "mshr_verified": 200000000,
                    "mshr_leveldate": "2013-01-01T00:00:00Z"
                },
                {
                    "mshr_skillid": "CashFlow",
                    "mshr_ratingid": "Skills",
                    "mshr_levelid": "4",
                    "mshr_ratinglevelexaminer": "",
                    "mshr_leveltype": 200000000,
                    "mshr_yearsofexperience": 0,
                    "mshr_verified": 200000000,
                    "mshr_leveldate": "2013-01-01T00:00:00Z"
                }
            ],
            "mshr_FK_HcmPersonEducationEntity_Person": [
                {
                    "mshr_creditbasis": 200000000,
                    "mshr_enddate": "2021-02-22T00:00:00Z",
                    "mshr_educationlevelid": "Bachelor",
                    "mshr_creditsearned": 0,
                    "mshr_startdate": "2017-02-21T00:00:00Z",
                    "mshr_creditscompleted": 0,
                    "mshr_educationinstitutionid": "Cottonwood Univ",
                    "mshr_educationdisciplineid": "Business Mgmt",
                    "mshr_durationunit": 200000000
                }              
            ]
        }
}
```

**استجابة**

```http

HTTP/1/1 204 No Content
OData-Version: 4.0
OData-EntityId: [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities(00000d2d-0000-0000-7317-005001000000)

```

## <a name="see-also"></a>راجع أيضًا

[مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب](hr-admin-integration-ats-api-introduction.md)<br>


[!INCLUDE[footer-include](../includes/footer-banner.md)]