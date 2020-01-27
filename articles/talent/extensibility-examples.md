---
title: توسيع Talent باستخدام Power Apps وPower Automate
description: يصف هذا الموضوع بعض الأمثلة عن سيناريوهات قابلية التوسعة في Microsoft Dynamics 365 Talent التي تستخدم Microsoft Power Apps وMicrosoft Power Automate.
author: negudava
manager: Annbe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2019-03-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 6c8a583a93c2ceb70d8c3b0e0047e2bf2047b56d
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898307"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a>توسيع Talent باستخدام Power Apps وPower Automate

يصف هذا الموضوع بعض الأمثلة عن سيناريوهات قابلية التوسعة في Microsoft Dynamics 365 Talent التي تستخدم Microsoft Power Apps وMicrosoft Power Automate. يمكنك استيراد حزمة الحل المقترنة بكل مثال إلى بيئتك في Power Apps. بعد ذلك، يمكنك استخدام الحزم كنقاط إرشادية أو كنقاط بداية لتنفيذ السيناريوهات التي تنطبق على مؤسستك.

> [!IMPORTANT]
> إذا أردت استخدام القوالب والتطبيقات التي تم وصفها في الموضوع "كما هي"، فتأكد من اختبارها للتأكد من أنها تغطي كافة السيناريوهات المتعلقة بعملية التنفيذ التي تقوم بها.


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

في Microsoft Dynamics 365: Attract، بإمكان النماذج أن تظهر في مدخل المرشحين، وبإمكان المرشحين ملء التفاصيل فيها. ويمكن أيضًا تضمين النماذج كأنشطة في قالب وظيفة.

عندما يرسل المرشح نموذجًا، يلتقط Microsoft Power Automate عملية إرسال النموذج ويقرأ البيانات ويخزنها في كيان Common Data Service.

لتنزيل القالب **Power Automate – توصيل النماذج** وبنية الكيان المخصص، انتقل إلى [Power Automate – توصيل النماذج](https://go.microsoft.com/fwlink/?linkid=2081988) على مركز التنزيل لـ Microsoft.

## <a name="initiate-and-extract-parameters-passed-to-power-apps"></a>تهيئة واستخراج المعلمات التي تم تمريرها إلى Power Apps

يمكن استخدام القالب **تهيئة واستخراج المعلمات التي تم تمريرها إلى Power Apps** كنقطة بداية لأي سيناريو Power Apps يتعلق بتطبيق Attract. ويتضمن هذا القالب جميع المعلمات الافتراضية التي تم تمريرها بواسطة Attract، مثل **استمارة التقديم للوظيفة** و**معرف المرشح** و**معرف الوظيفة**.

يمكن استخدام هذا القالب للعثور على نموذج تقييم المرشح لتمكين مدير التوظيف من عرض التقييم الذي قام المرشح بتعبئته.

يمكن تضمين التطبيقات التي يتم إنشاؤها باستخدام Power Apps في قالب الوظيفة في Attract.

لتنزيل القالب **تهيئة واستخراج المعلمات التي تم تمريرها إلى Power Apps** وبنية الكيان المخصص، انتقل إلى [تهيئة واستخراج المعلمات التي تم تمريرها إلى Power Apps](https://go.microsoft.com/fwlink/?linkid=2081991) في مركز التنزيل لـ Microsoft.

## <a name="integration-with-office-365"></a>التكامل مع Office 365

يمكن استخدام تطبيق **التكامل مع Office 365** لاستخراج معلومات الفريق للمستخدمين الذين سجلوا دخولهم من Microsoft Office 365. وهو يشير إلى العاملين في Talent لاستخراج تسجيلات تفاصيل بدء العمل وانتهاء العمل والاستثناءات. يتم تخزين تفاصيل بدء العمل وانتهاء العمل في كيانات مخصصة في Common Data Service. ويتم الافتراض أن تعبئة هذه التفاصيل يتم من أنظمة خارجية عن طريق التكامل.

يمكن توسيع هذا التطبيق لتمكين سيناريوهات أخرى من استخدامه. على سبيل المثال، يمكن استخدامه لإظهار معلومات العطلة الخاصة بالفريق بالإضافة إلى أحداث التقويم وأي أحداث خاصة بالفريق.

لتنزيل تطبيق **التكامل مع Office 365** وبنية الكيان المخصص، انتقل إلى [التكامل مع Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) في مركز التنزيل لـ Microsoft.

## <a name="power-automate--email-notification"></a>Power Automate – الإخطار بالبريد الإلكتروني

يمكن استخدام القالب **Power Automate – الإخطار بالبريد الإلكتروني** لسيناريوهات الإخطار بالبريد الإلكتروني. ويمكن استخدامه لتشغيل الإعلامات بواسطة البريد الإلكتروني الموجهة للمرشحين الذين رفضهم فريق التوظيف أثناء أي مرحلة من مراحل التعيين.

يمكن توسيع هذا القالب لتعقب التغييرات في مرحلة المرشح عبر عملية التعيين، ولإرسال إعلامات إلى فريق التوظيف والمرشح.

بشكل عام، بالنسبة إلى الكيانات المخزنة في Common Data Service، يمكن إعداد مهام سير العمل لإرسال إعلامات تتعلق بالأحداث التي تقع في Core HR أو Attract أو Onboard.

لتنزيل القالب **Power Automate – الإخطار بالبريد الإلكتروني**، انتقل إلى [Power Automate – الإخطار بالبريد الإلكتروني](https://go.microsoft.com/fwlink/?linkid=2082103) على مركز التنزيل لـ Microsoft.

## <a name="power-automate--sql-connect-and-execute"></a>Power Automate – توصيل وتنفيذ SQL

يقوم القالب **Power Automate – توصيل وتنفيذ SQL‬** بالتوصيل بخادم Microsoft SQL Server ويتيح تشغيل استعلامات SQL.

على الرغم من تصميم هذا القالب لقراءة وتحديث جداول SQL، إلا أنه من الممكن توسيعه لتمكين استخدامه لسيناريوهات أخرى. على سبيل المثال، يمكن استخدامه لتعبئة جدول مرحلي في Common Data Service بواسطة سجلات من SQL Server، ولمزامنة الجدول المرحلي بشكل دوري باستخدام توزيع تزايدي من SQL Server.

لتنزيل القالب **Power Automate – توصيل وتنفيذ SQL**، انتقل إلى [Power Automate – توصيل وتنفيذ SQL](https://go.microsoft.com/fwlink/?linkid=2081789) على مركز تنزيل Microsoft.

## <a name="power-automate--sharepoint-integration"></a>تكامل Power Automate – SharePoint

يمكن استخدام القالب **تكامل Power Automate – SharePoint** لقراءة البيانات من قائمة Microsoft SharePoint ومقارنة القائمة مع قيم الحقول لأي من كيانات Common Data Service وإرسال نتائج المقارنة كبريد إلكتروني للإخطار. 

قد تتوفر لدى مؤسسة مجموعة من المهارات تحتاج إليها بطريقة ملحة. يمكن تخزين هذه المهارات في SharePoint كقائمة SharePoint. عندما يقدم أحد المرشحين طلب الحصول على أي وظيفة تم إدراج مجموعة المهارات المطلوبة لها، يتم إرسال بريد إلكتروني للإعلام عند وجود تطابق ملحوظ بين مهارات المرشح والمهارات المخزنة في SharePoint. وبهذه الطريقة، يتم ملء المناصب المطلوبة بشكل ملح بسرعة أكبر، لأن الإعلامات تساعد مسؤولي التعيين على الوصول إلى المرشحين عبر المؤسسة وتوظيفهم.

يمكن توسيع هذا القالب لتمكين استخدامه لأي سيناريو يشتمل على تكامل SharePoint.

لتنزيل القالب **تكامل Power Automate – SharePoint**، انتقل إلى [تكامل Power Automate – SharePoint](https://go.microsoft.com/fwlink/?linkid=2082109) على مركز التنزيل لـ Microsoft.

## <a name="referral-app"></a>تطبيق Referral
يمكنك استخدام التطبيق Referral لإضافة مرشحين إلى مجموعة مواهب مشتركة. بإمكان المحيل إدخال **الاسم الأول** و**اسم العائلة** و**البريد الإلكتروني** و**Linkedln URL** عند إرسال مرشح. يتم بعد ذلك ملء بيانات تعريف مصدر المرشح بواسطة معلومات المحيل.

يمكنك تضمين هذا التطبيق في الخدمة الذاتية للموظف (ESS) لإرسال الإحالات، أو يمكنك استخدامه كارتباط تشعبي في مدخل الشركة وتشغيله كتطبيق مستقل.

لتنزيل **تطبيق Referral**، انتقل إلى [حل قابلية التوسعة في Dynamics 365 Talent: تطبيق Referral](https://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d) في مركز التنزيل لـ Microsoft. يمكنك استيراد هذا التطبيق وتخصيصه لإضافة المزيد من الوظائف.

## <a name="additional-resources"></a>الموارد الإضافية

[Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[ترحيل التطبيق بين المستأجرين والبيئات](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
