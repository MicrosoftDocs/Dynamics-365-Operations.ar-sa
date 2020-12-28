---
title: تعقب التغييرات في بيانات التعيين
description: تسمح لك ميزة معالجة التدقيق بتعقب الوقت الذي يحدث فيه تغيير في المرشحين أو فرص التوظيف أو استمارات التقديم للوظائف لأسباب تتعلق بإعداد التقارير أو الامتثال.
author: tracykeya
manager: AnnBe
ms.date: 04/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.1.0, Talent April 2019 update
ms.openlocfilehash: c009f82e69bff0e4ea540514de8f9e60eca1e466
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460252"
---
# <a name="track-changes-in-recruiting-data"></a>تعقب التغييرات في بيانات التعيين

[!include [banner](includes/banner.md)]

يمكنك تعقب التغييرات التي تتم على المرشحين أو الوظائف الشاغرة أو استمارات التقديم للوظائف باستخدام معالجة التدقيق. وهذا مفيد لأسباب تتعلق بإعداد التقارير أو الامتثال.

يمكنك عرض البيانات المتعقبة في Power BI باستخدام موصل OData. لمزيد من المعلومات، راجع [الاتصال بموجزات OData في Power BI Desktop](https://docs.microsoft.com/power-bi/desktop-connect-odata).

## <a name="track-changes"></a>تعقب التغييرات
لإعداد تعقب التغييرات في بيانات التعيين، اتبع الخطوات التالية:

1. في [Power Apps](https://web.powerapps.com)، حدد البيئة المناسبة.

2. حدد **الإعدادات** (أيقونة الترس)، واخت **التخصيصات المتقدمة**، ثم حدد **الموارد** ضمن **موارد المطور**. 

3. في صفحة **موارد‏‎ المطور**، انسخ القيمة في الحقل **قيمة Web API للمثيل**. على سبيل المثال، قد تبدو القيمة كما يلي: https://yourorgname.api.crm.dynamics.com/api/data/v9.1/.

4. يمكنك بعد ذلك الاستعلام عن البيانات من أحد الكيانات التالية:
  - محفوظات فرص التوظيف (msdyn_jobopeninghistories)
  - محفوظات استمارات التقديم للوظائف (msdyn_jobapplicationhistories) 
  - محفوظات المرشحين (msdyn_candidatehistories)

## <a name="data-reported"></a>البيانات التي تم الإبلاغ عنها

تتوفر البيانات التالية مع معالجة التدقيق.

| البيانات التي تم الإبلاغ عنها | الوصف |
| --- | --- |
| تم التغيير بواسطة (msdyn_ChangedbyId) | مرجع إلى المستخدم |
| تاريخ الإنشاء (createdon) |  التاريخ والوقت بتنسيق UTC عند حدوث التغيير |
| نوع التغيير (msdyn_changetype) | التغيير الذي حدث |
| القيم العامة للمرشحين وفرص التوظيف <br></br>واستمارات التقديم للوظائف | تاريخ الإنشاء<br></br>محدث |
| محفوظات استمارات التقديم للوظائف | البيانات الاصطناعية المضافة <br></br>البيانات الاصطناعية المزالة |
| محفوظات فرص التوظيف | TODO: منشور مضاف <br></br>TODO: منشور مزال <br></br>TODO: منشور محدّث <br></br>TODO: مشارك مضاف <br></br>TODO: مشارك مزال |
| محفوظات المرشحين | البيانات الاصطناعية المضافة <br></br>البيانات الاصطناعية المزالة <br></br>خبرات العمل المضافة <br></br>خبرات العمل المزالة <br></br>التعليم المضاف <br></br>التعليم المزال <br></br>المهارة المضافة <br></br>المهارة المزالة <br></br>العلامة المضافة <br></br>العلامة المزالة <br></br>الشبكة الاجتماعية المضافة <br></br>الشبكة الاجتماعية المزالة <br></br>البيانات الشخصية المضافة <br></br>البيانات الشخصية المحدّثة<br></br> |
| الحقول المتغيرة (msdyn_changedfields) | قد لا تقوم الحقول المتغيرة في قائمة كائنات JSON بتخزين قيم لجميع الحقول.<br></br><br></br>بالنسبة إلى التغييرات "المُنشأة" و"المحدّثة"، سوف تسرد الحقول في السجل المُنشأ أو المحدّث.<br></br><br></br>بالنسبة إلى أنواع التغييرات "المضافة"، سوف تسرد الحقول في السجل التابع.<br></br><br></br>**مثال:**<br></br><br></br>{<br></br>  "msdyn_applyurl": { "newValue": "" },<br></br>  "msdyn_description": { "valueOmitted": true } <br></br>} |
|محفوظات استمارات التقديم للوظائف | استمارة التقديم للوظيفة‬ (msdyn_JobapplicatonId)<br></br>الحالة (msdyn_status) <br></br>سبب الحالة (msdyn_statusreason) <br></br>سبب الرفض (msdyn_rejectionreason) |
| محفوظات فرص التوظيف | فرص التوظيف (msdyn_JobopeningId) <br></br>الحالة (msdyn_jobopeningstatus) <br></br>سبب الحالة (msdyn_jobopeningstatusreason) |
| محفوظات المرشحين | المرشح (msdyn_CandidateId) |
