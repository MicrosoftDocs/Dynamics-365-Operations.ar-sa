---
title: تعليم الشخص
description: يصف هذا الموضوع كيان تعليم الشخص لـ Dynamics 365 Human Resources.
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
ms.openlocfilehash: cfa05fe6816c6b24034f8f015bf6e42d665ef1dc
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466486"
---
# <a name="person-education"></a>تعليم الشخص

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا الموضوع كيان تعليم الشخص لـ Dynamics 365 Human Resources.

الاسم الفعلي: mshr_hcmpersoneducationentity

## <a name="description"></a>الوصف

يحتوي هذا الكيان على المحفوظات التعليمية للشخص الذي يترشح. يرتبط التعليم بسجل الشخص ما يسمح باقتران التعليم بأية أدوار أخرى يتم إنشاؤها للشخص بالإضافة إلى سجل المرشح (العامل والمقاول وهكذا).

## <a name="json-representation"></a>تمثيل JSON

```json
{
    "mshr_creditbasis": Int,
    "mshr_creditscompleted": Decimal,
    "mshr_creditsearned": Decimal,
    "mshr_creditsneeded": Decimal,
    "mshr_description": "String",
    "mshr_duration": Decimal,
    "mshr_durationunit": Int,
    "mshr_educationdisciplineid": "String",
    "mshr_educationinstitutionid": "String",
    "mshr_educationlevelid": "String",
    "mshr_enddate": "Date",
    "mshr_gradepointaverage": Decimal,
    "mshr_gradescale": "String",
    "mshr_notes": "String",
    "mshr_secondaryemphasis": "String",
    "mshr_startdate": "Date",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_educationdiscipline_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_educationinstitution_id_value": "Guid",
    "_mshr_fk_educationlevel_id_value": "Guid",
    "mshr_hcmpersoneducationentityid": "Guid"
}
```

## <a name="properties"></a>الخصائص

| الخاصية<br>**الاسم الفعلي**<br>**_النوع_** | استخدام | الوصف |
| --- | --- | --- |
| **معرف كيان تعليم الشخص**<br>mshr_hcmpersoneducationentityid<br>*GUID* | للقراءة فقط<br>مطلوب | معرف فريد منشأ بواسطة النظام لسجل كيان تعليم الشخص. |
| **رقم الطرف**<br>mshr_partynumber<br>*سلسلة* | قراءة/كتابة<br>مطلوب | المعرف الفريد لسجل الطرف (الشخص) الخاص بالمرشح. |
| **قيمة معرف الشخص**<br>_mshr_fk_person_id_value<br>*GUID* | للقراءة فقط<br>مطلوب<br>المفتاح الخارجي: mshr_dirpersonentityid لـ mshr_dirpersonentity | المعرف الفريد المنشأ بواسطة النظام لسجل الشخص المرشح. |
| **أساس الساعة المعتمدة**<br>mshr_creditbasis<br>*مجموعة خيارات mshr_hcmeducationcreditbasis* | قراءة/كتابة<br>اختياري | أساس الساعات المعتمدة لدرجة التعليم. |
| **الساعات المعتمدة المكتملة**<br>mshr_creditscompleted<br>*عشري* | قراءة/كتابة<br>اختياري | عدد الساعات المعتمدة المكتملة لعملية التعليم. |
| **الساعات المعتمدة المكتسبة**<br>mshr_creditsearned<br>*عشري* | قراءة/كتابة<br>اختياري | عدد الساعات المعتمدة المكتسبة التي تم الحصول عليها للسجل التعليمي للدرجة قيد التقدم. |
| **الساعات المعتمدة المطلوبة**<br>mshr_creditsneeded<br>*عشري* | قراءة/كتابة<br>اختياري | عدد الساعات المعتمدة المطلوبة لكل درجه قيد التقدم. |
| **‏‏الوصف**<br>mshr_description<br>*سلسلة* | قراءة/كتابة<br>اختياري | وصف لدرجة المرشح. |
| **معرف مستوى التعليم**<br>mshr_educationlevelid<br>*سلسلة* | قراءة/كتابة<br>اختياري | المعرف لمستوى التعليم. | 
| **قيمة معرف مستوى التعليم**<br>_mshr_fk_educationlevel_id_value<br>*GUID* | للقراءة فقط<br>اختياري<br>المفتاح الخارجي: mshr_hcmeducationdegreeentityid للكيان mshr_hcmeducationdegreeentity entity | المعرف الذي تم إنشاؤه بواسطة النظام لسجل الدرجة التعليمية. يوفر هذا المعرف الدرجات ومستويات التعليم المحددة للمؤسسة. |
| **معرف النظام التعليمي**<br>mshr_educationdisciplineid<br>*سلسلة* | قراءة/كتابة<br>مطلوب<br>المفتاح الخارجي: EducationDiscipline | المعرف للنظام التعليمي. |
| **قيمة معرف النظام التعليمي**<br>_mshr_fk_educationdiscipline_id_value<br>*GUID* | للقراءة فقط<br>مطلوب<br>المفتاح الخارجي: mshr_hcmeducationdisciplineentityid of mshr_hcmeducationdisciplineentity | المعرف الفريد المنشأ بواسطة النظام للنظام التعليمي للسجل التعليمي. |
| **التخصص الثانوي**<br>mshr_secondaryemphasis<br>*سلسلة* | قراءة/كتابة<br>اختياري | التخصص الثانوي للدرجة المكتسبة. |
| **معرف المؤسسة التعليمية**<br>mshr_educationinstitutionid<br>*سلسلة* | قراءة/كتابة<br>اختياري | معرف المؤسسة التعليمية التي تم الحضور فيها. |
| **قيمة معرف المؤسسة التعليمية**<br>_mshr_fk_educationinstitution_id_value<br>*GUID* | للقراءة فقط<br>اختياري<br>المفتاح الخارجي: mshr_hcmeducationinstitutionentityid of mshr_hcmeducationinstitutionentity | المعرف الذي تم إنشاؤه بواسطة النظام للمؤسسة التعليمية. |
| **تاريخ البدء**<br>mshr_startdate<br>*Datetime* | قراءة/كتابة<br>اختياري | تاريخ بدء التعليم الخاص بالدرجة المكتسبة. |
| **تاريخ النهاية**<br>mshr_enddate<br>*Datetime* | قراءة/كتابة<br>مطلوب | تاريخ إصدار بيانات الاعتماد. |
| **المدة**<br>mshr_duration<br>*عشري* | قراءة/كتابة<br>اختياري | الفترة الزمنية للسجل التعليمي. |
| **وحدة المدة**<br>mshr_durationunit<br>*مجموعة خيارات mshr_periodunit* | قراءة/كتابة<br>اختياري | وحدة الوقت المقترنة بمدة السجل التعليمي. |
| **متوسط نقاط الدرجات**<br>mshr_gradepointaverage<br>*عشري* | قراءة/كتابة<br>اختياري | متوسط النقاط للدرجة التي تم اكتسابها. |
| **مقياس الدرجة**<br>mshr_gradescale<br>*سلسلة* | قراءة/كتابة<br>اختياري | المقياس المستخدم لحساب متوسط النقاط للدرجة. |
| **الملاحظات**<br>mshr_notes<br>*سلسلة* | قراءة/كتابة<br>اختياري | ملاحظات للاستخدام من جانب مسؤولي التعيين أو مدراء التوظيف. |
| **الحقل الأساسي**<br>mshr_primaryfield<br>*سلسلة* | للقراءة فقط<br>مطلوب | حقل يستخدم كمعرف أساسي آخر لسجل الكيان. مجموعة من رقم الطرف ومعرف النظام التعليمي ومعرف المؤسسة التعليمية ومعرف المستوى التعليمي. |

## <a name="see-also"></a>راجع أيضًا

[مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب](hr-admin-integration-ats-api-introduction.md)<br>
[مثال الاستعلام عن مرشح مراد توظيفه](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]