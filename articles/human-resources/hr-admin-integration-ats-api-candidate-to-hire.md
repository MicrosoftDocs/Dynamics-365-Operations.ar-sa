---
title: المرشح المُراد توظيفه
description: يصف هذا الموضوع المرشح المطلوب لكيان التوظيف لـ Dynamics 365 Human Resources.
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
ms.openlocfilehash: eb16f9f46e3f5c58854ec06c3b89ec72dd7bae00
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125727"
---
# <a name="candidate-to-hire"></a>المرشح المُراد توظيفه

يصف هذا الموضوع المرشح المطلوب لكيان التوظيف لـ Dynamics 365 Human Resources.

الاسم الفعلي: mshr_hcmcandidatetohireentity

## <a name="description"></a>الوصف

يوفر هذا الكيان تفاصيل الترشيح المستخدمة لإنشاء عامل في Dynamics 365 Human Resources. وهو يستخدم لقراءة كافة سجلات المرشحين وإنشاء سجلات مرشح داخلية وخارجية، مما يسمح لك بإنشاء تفاصيل شخصية لهذا المرشح الجديد.

عند إنشاء سجل مرشح خارجي والذي سيكون سجل شخص جديد في النظام، يجب عدم تحديد رقم الطرف (الشخص) الذي تقوم بترحيل سجل مرشح جديد له. يتم إنشاء سجل كيان الشخص الجديد باستخدام سجل المرشح الجديد.

عند إنشاء سجل مرشح داخلي (مرشح لمنصب يوجد له بالفعل سجل موظف مع الشركة)، حدد رقم الطرف (الشخص) للسجل الموجود بالفعل للخاصية mshr_partynumber في سجل المرشح بدلا من تعريف معلومات شخصية (مثل الاسم أو النوع أو تاريخ الميلاد) التي سيتم استخدامها لإنشاء سجل شخص جديد.

## <a name="json-representation"></a>تمثيل JSON

```json
        {
            "mshr_candidateid": "String",
            "mshr_partynumber": "String",
            "mshr_partytype": "String",
            "mshr_recruitingrequestid": "String",
            "mshr_positionid": "String",
            "mshr_firstname": "String",
            "mshr_middlename": "String",
            "mshr_lastnameprefix": "String",
            "mshr_lastname": "String",
            "mshr_gender": Int,
            "mshr_birthdate": "Date",
            "mshr_citizenshipcountrycode": "String",
            "mshr_veteranstatusid": "String",
            "mshr_isdisabledveteran": Int,
            "mshr_availabilitydate": "Date",
            "mshr_iswillingtorelocate": Int,
            "mshr_comments": "String",
            "mshr_applicantintegrationresult": Int,
            "mshr_donothirereasoncodeid": "String",
            "mshr_dataareaid": "String",
            "_mshr_dataareaid_id_value": "Guid",
            "_mshr_fk_person_id_value": "Guid",
            "_mshr_fk_recruitingrequest_id_value": "Guid",
            "_mshr_fk_position_id_value": "Guid",
            "mshr_hcmcandidatetohireentityid": "Guid",
            "_mshr_fk_veteranstatus_id_value": "Guid",
            "_mshr_fk_reasoncode_id_value": "Guid",
            "mshr_militaryserviceenddate": "Guid",
            "mshr_militaryservicestartdate": "Guid"
        }
```

## <a name="properties"></a>الخصائص

| الخاصية<br>**الاسم الفعلي**<br>**_النوع_** | استخدام | الوصف |
| --- | --- | --- |
| **معرف كيان المرشح للتوظيف**<br>mshr_hcmcandidatetohireentityid<br>Guid | للقراءة فقط<br>مطلوب<br>منشأ بواسطة النظام | معرف فريد منشأ بواسطة النظام لسجل الكيان. |
| **معرف المرشح**<br>mshr_candidateid<br>سلسلة | للقراءة فقط<br>مطلوب<br>منشأ بواسطة النظام | المعرف الفريد للكيان. |
| **رقم الطرف**<br>mshr_partynumber<br>سلسلة | للقراءة فقط<br>مطلوب | رقم الطرف (الشخص) لسجل الشخص المرشح. |
| **قيمة معرف الشخص**<br>_mshr_fk_person_id_value<br>Guid | للقراءة فقط<br>مطلوب<br>المفتاح الخارجي: mshr_dirpersonentityid من mshr_direpersonentity | المعرف الفريد المنشأ بواسطة النظام لسجل الطرف (الشخص) الخاص بالمرشح. |
| **نوع الطرف**<br>mshr_partytype<br>مجموعة خيارات mshr_dirpartytype | للقراءة فقط<br>مطلوب | نوع الطرف للسجل، كما هو محدد في مجموعة الخيارات mshr_dirpartytype. بالنسبة لهذا الكيان، سيكون النوع دائمًا "شخص". |
| **معرف طلب التعيين**<br>mshr_recruitingrequestid<br>سلسلة | الكتابة مرة واحدة<br>اختياري | يشير إلى طلب التعيين الذي يستوفيه المرشح. |
| **قيمة معرف طلب التعيين**<br>_mshr_fk_recruitingrequest_id_value<br>Guid | قراءة/كتابة<br>اختياري<br>المفتاح الخارجي: mshr_hcmrecruitingrequestentityid لـ mshr_hcmrecruitingrequestentity | المعرف الفريد المنشأ بواسطة النظام لطلب التوظيف هلذي يستوفيه المرشح. |
| **معرف المنصب**<br>mshr_positionid<br>سلسلة | قراءة/كتابة<br>اختياري | المعرف الخاص بالمنصب الذي يتم اعتبار المرشح لشغله. |
| **قيمة معرف المنصب**<br>_mshr_fk_position_if_value<br>Guid | للقراءة فقط<br>اختياري<br>المفتاح الخارجي: mshr_hcmpositionv2entityid لـ mshr_hcmpositionv2entity | المعرف المنشأة بواسطة النظام للمنصب الذي يتم اعتبار المرشح لشغله. |
| **الاسم الأول**<br>mshr_firstname<br>سلسلة | قراءة/كتابة<br>مطلوب | الاسم الأول للمرشح. |
| **الاسم الأوسط**<br>mshr_middlename<br>سلسلة | قراءة/كتابة<br>اختياري | الاسم الأوسط للمرشح. |
| **بادئة اسم العائلة**<br>mshr_lastnameprefix<br>سلسلة | قراءة/كتابة<br>اختياري | بادئة اسم العائلة للمرشح. |
| **اسم العائلة**<br>mshr_lastname<br>سلسلة | قراءة/كتابة<br>اختياري | اسم العائلة للمرشح. |
| **الجنس**<br>mshr_gender<br>مجموعة خيارات mshr_hcmpersongender | قراءة/كتابة<br>اختياري | نوع المرشح. |
| **تاريخ الميلاد**<br>mshr_birthdate<br>التاريخ والوقت | قراءة/كتابة<br>اختياري | تاريخ ميلاد المرشح. |
| **رمز بلد المواطنة**<br>mshr_citizenshipcountrycode<br>سلسلة | قراءة/كتابة<br>اختياري | يحدد البلد الذي هو موطن المرشح. رموز البلاد الصالحة في mshr_logisticaddresscountryregionentity. |
| **معرف حالة الخبرة**<br>mshr_veteranstatusid<br>سلسلة | قراءة/كتابة<br>اختياري | يشير إلى حالة الخبرة للمرشح. |
| **قيمة معرف حالة الخبرة**<br>_mshr_fk_veteranstatus_id_value<br>Guid | للقراءة فقط<br>اختياري<br>المفتاح الخارجي: mshr_hcmveteranstatusentityid لـ mshr_hcmveteranstatusentity | معرف فريد منشأ بواسطة النظام لسجل كيان حالة الخبرة. |
| **تاريخ بدء الخدمة العسكرية**<br>mshr_militaryservicestartdate<br>التاريخ والوقت | قراءة/كتابة<br>اختياري | تاريخ بدء الخدمة العسكرية للمرشح. |
| **تاريخ انتهاء الخدمة العسكرية**<br>mshr_militaryserviceenddate<br>التاريخ والوقت | قراءة/كتابة<br>اختياري | تاريخ انتهاء الخدمة العسكرية للمرشح. |
| **هو خبير معاق**<br>mshr_isdisabledveteran<br>مجموعة خيارات mshr_noyes | قراءة/كتابة<br>اختياري | يشير إلى ما إذا قام المرشح بتعطيل حالة الخبرة. |
| **تاريخ التوفر**<br>mshr_availabilitydate<br>التاريخ والوقت | قراءة/كتابة<br>اختياري | التاريخ الأسبق الذي سيكون فيه المرشح متاحًا للعمل. |
| **مستعد لتغيير موقعه**<br>mshr_iswillingtorelocate<br>مجموعة خيارات mshr_noyes | قراءة/كتابة<br>اختياري | يشير إلى ما إذا كان المرشح على استعداد لتغيير محل إقامته لأجل المنصب. |
| **التعليقات**<br>mshr_comments<br>سلسلة | قراءة/كتابة<br>اختياري | التعليقات التي يتم استخدامها بواسطة مدير التوظيف أو مدير التعيين. |
| **نتيجة تكامل الطلب**<br>mshr_applcantintegrationresult<br>مجموعة خيارات mshr_applicantintegrationresult | قراءة/كتابة<br>مطلوب | حالة المرشح في عملية التوظيف المرتبطة بالتكامل. |
| **معرف رمز سبب عدم التوظيف**<br>mshr_donothirereasoncodeid<br>سلسلة | قراءة/كتابة<br>اختياري | يتم توفير رمز السبب اختياريًا عند تعيين الحالة (نتيجة تكامل الطلب) إلى "عدم التوظيف". |
| **قيمة معرف رمز السبب**<br>_mshr_fk_reasoncode_id_value<br>Guid | للقراءة فقط<br>اختياري<br>المفتاح الخارجي: mshr_hcmreasoncodeentityid لـ mshr_hcmreasoncodeentity entity | معرف فريد منشأ بواسطة النظام لرمز سبب **عدد التوظيف**. |
| **معرف منطقة البيانات**<br>mshr_dataareaid<br>سلسلة | قراءة/كتابة<br>اختياري |  يحدد الكيان القانوني (الشركة). |
| **قيمة معرف منطقة البيانات**<br>_mshr_dataareaid_id_value<br>Guid | للقراءة فقط<br>اختياري<br>المفتاح الخارجي: cdm_companyid للكيان cdm_company | قيمة GUID تم إنشاؤها بواسطة النظام لتعرف الكيان القانوني (الشركة). |

## <a name="see-also"></a>راجع أيضًا

[مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب](hr-admin-integration-ats-api-introduction.md)<br>
[مثال الاستعلام عن مرشح مراد توظيفه](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]