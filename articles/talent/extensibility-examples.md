---
title: توسيع Talent باستخدام Power Apps وPower Automate
description: يوضح هذا المقال بعض الأمثلة عن سيناريوهات قابلية توسعة Microsoft Dynamics 365 Talent - Attract التي تستخدم Microsoft Power Apps وPower Automate.
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: cfdf36e9486aa4853d3bf674afa73ec3a4d1c161
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529624"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a>توسيع Talent باستخدام Power Apps وPower Automate

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يوضح هذا المقال بعض الأمثلة عن سيناريوهات قابلية توسعة Microsoft Dynamics 365 Talent: Attract التي تستخدم Microsoft Power Apps وMicrosoft Power Automate. يمكنك استيراد حزمة الحل المقترنة بكل مثال إلى بيئتك في Power Apps. بعد ذلك، يمكنك استخدام الحزم كنقاط إرشادية أو كنقاط بداية لتنفيذ السيناريوهات التي تنطبق على مؤسستك.

> [!IMPORTANT]
> إذا أردت استخدام القوالب والتطبيقات التي تم وصفها في هذا المقال "كما هي"، فتأكد من اختبارها للتأكد من أنها تغطي كافة السيناريوهات المتعلقة بعملية التنفيذ التي تقوم بها.


## <a name="prerequisites"></a>المتطلبات الأساسية

- لاستيراد الحزم، يجب أن يتوفر إذن **أداة إنشاء البيئة** لدى المستخدمين.
- لتصدير التطبيقات أو استيرادها، يجب أن يتوفر لدى المستخدمين ترخيص Power Apps Plan 2 أو ترخيص إصدار تجريبي Power Apps Plan 2.

## <a name="power-automate--form-connect"></a>Power Automate – توصيل النماذج

يمكن استخدام القالب **Power Automate – توصيل النماذج** لقراءة البيانات من Microsoft Forms وتخزينها في كيان Common Data Service.

ويمكن توسيع هذا القالب لتمكين سيناريوهات أخرى من استخدامه. فيما يلي بعض الأمثلة:

- التقاط تقييمات المرشح.
- التقاط النتائج من استبيانات الدورة التدريبية.
- تجميع مكتبة تتضمن أسئلة المقابلات لمسؤولي الموارد البشرية (HR).
- التقاط تقييم المرشح أثناء عملية المقابلة

في Microsoft Dynamics 365: Attract، بإمكانك استخدام النماذج في مدخل المرشحين، التي يملأ المرشحون التفاصيل فيها. ويمكنك أيضًا تضمين النماذج كأنشطة في قالب وظيفة.

عندما يرسل المرشح نموذجًا، يلتقط Microsoft Power Automate عملية إرسال النموذج ويقرأ البيانات ويخزنها في كيان Common Data Service.

لتنزيل القالب **Power Automate – توصيل النماذج** وبنية الكيان المخصص، انتقل إلى [Power Automate – توصيل النماذج](https://go.microsoft.com/fwlink/?linkid=2081988) على مركز التنزيل لـ Microsoft.

## <a name="power-automate--sharepoint-integration"></a>تكامل Power Automate – SharePoint

يمكن استخدام القالب **تكامل Power Automate – SharePoint** لقراءة البيانات من قائمة Microsoft SharePoint ومقارنة القائمة مع قيم الحقول لأي من كيانات Common Data Service وإرسال نتائج المقارنة كبريد إلكتروني للإخطار. 

قد تتوفر لدى مؤسسة مجموعة من المهارات تحتاج إليها بطريقة ملحة. يمكن تخزين هذه المهارات في SharePoint كقائمة SharePoint. عندما يقدم أحد المرشحين طلب الحصول على أي وظيفة تم إدراج مجموعة المهارات المطلوبة لها، يتم إرسال بريد إلكتروني للإعلام عند وجود تطابق ملحوظ بين مهارات المرشح والمهارات المخزنة في SharePoint. ويساعد هذا في ملء المناصب المطلوبة بشكل مُلح بسرعة أكبر، لأن الإخطارات تساعد مسؤولي التعيين على توظيف المرشحين عبر المؤسسة.

يمكن توسيع هذا القالب لتمكين استخدامه لأي سيناريو يشتمل على تكامل SharePoint.

لتنزيل القالب **تكامل Power Automate – SharePoint**، انتقل إلى [تكامل Power Automate – SharePoint](https://go.microsoft.com/fwlink/?linkid=2082109) على مركز التنزيل لـ Microsoft.

## <a name="referral-app"></a>تطبيق Referral

يمكنك استخدام التطبيق Referral لإضافة مرشحين إلى مجموعة مواهب مشتركة. بإمكان المحيل إدخال **الاسم الأول** و **اسم العائلة** و **البريد الإلكتروني** و **Linkedln URL** عند إرسال مرشح. يتم بعد ذلك ملء بيانات تعريف مصدر المرشح بواسطة معلومات المحيل.

يمكنك تضمين هذا التطبيق في الخدمة الذاتية للموظف لإرسال الإحالات، أو يمكنك استخدامه كارتباط تشعبي في مدخل الشركة وتشغيله كتطبيق مستقل.

لتنزيل **تطبيق Referral**، انتقل إلى [حل قابلية التوسعة في Dynamics 365 Talent: تطبيق Referral](https://www.microsoft.com/download/details.aspx?id=58497) في مركز التنزيل لـ Microsoft. يمكنك استيراد هذا التطبيق وتخصيصه لإضافة المزيد من الوظائف.

## <a name="additional-resources"></a>الموارد الإضافية

[Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>
[ترحيل التطبيق بين المستأجرين والبيئات](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
