---
title: توسيع Talent باستخدام Power Apps وPower Automate
description: يصف هذا المقال بعض الأمثلة عن سيناريوهات قابلية التوسعة في Microsoft Dynamics 365 Human Resources التي تستخدم Microsoft Power Apps و Microsoft Power Automate.
author: negudava
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5b1ebe17063d954b52a0607d39e3ea08518adb89
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/18/2021
ms.locfileid: "6057588"
---
# <a name="extend-with-power-apps-and-power-automate"></a>توسيع باستخدام Power Apps وPower Automate

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يصف هذا المقال بعض الأمثلة عن سيناريوهات قابلية التوسعة في Microsoft Dynamics 365 Human Resources التي تستخدم Microsoft Power Apps و Microsoft Power Automate. يمكنك استيراد حزمة الحل المقترنة بكل مثال إلى بيئتك في Power Apps. بعد ذلك، يمكنك استخدام الحزم كنقاط إرشادية أو كنقاط بداية لتنفيذ السيناريوهات التي تنطبق على مؤسستك.

> [!IMPORTANT]
> إذا أردت استخدام القوالب والتطبيقات التي تم وصفها في الموضوع "كما هي"، فتأكد من اختبارها للتأكد من أنها تغطي كافة السيناريوهات المتعلقة بعملية التنفيذ التي تقوم بها.

## <a name="prerequisites"></a>المتطلبات الأساسية

- لاستيراد الحزم، يجب أن يتوفر إذن **أداة إنشاء البيئة** لدى المستخدمين.
- لتصدير التطبيقات أو استيرادها، يجب أن يتوفر لدى المستخدمين ترخيص Power Apps Plan 2 أو ترخيص إصدار تجريبي Power Apps Plan 2.

## <a name="integration-with-microsoft-365-power-automate"></a>التكامل مع Microsoft 365، Power Automate

يمكن استخدام تطبيق **التكامل مع Microsoft 365** لاستخراج معلومات الفريق للمستخدمين الذين سجلوا دخولهم من Microsoft 365. ويشير إلى العاملين في الموارد البشرية لاستخراج أنواع ‏‫معرفات الموظفين. يمكن للمديرين فحص تواريخ انتهاء صلاحية أنواع معرفات الموظفين. كما يمكنهم إرسال تذكير بالبريد الكتروني إذا انتهت صلاحية نوع معرف الموظف. يتكامل Power Automate مع Power Apps لإرسال هذا التذكير. سيتم إعادة إرسال التأكيد إلى Power Apps من Power Automate وقت إرسال التذكير. تتضمن أنواع التعريف رخصة القيادة وجواز السفر والنماذج الأخرى المقبولة للمعرف.

يمكنك توسيع هذا التطبيق لسيناريوهات أخرى. على سبيل المثال، يمكن استخدامه لإظهار معلومات العطلة الخاصة بالفريق بالإضافة إلى أحداث التقويم وأي أحداث خاصة بالفريق.

لتنزيل تطبيق **التكامل مع Microsoft 365، Power Automate**، انتقل إلى [التكامل مع Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2081787) على مركز التنزيل لـ Microsoft.

## <a name="power-automate--sql-connect-and-execute"></a>Power Automate – توصيل وتنفيذ SQL

يقوم القالب **Power Automate – توصيل وتنفيذ SQL‬** بالتوصيل بخادم Microsoft SQL Server ويتيح تشغيل استعلامات SQL.

على الرغم من أن هذا القالب يقرأ جداول SQL ويقوم بتحديثه، إلا أنه يمكنك توسيعه واستخدامه في السيناريوهات الأخرى. على سبيل المثال، يمكن استخدامه لتعبئة جدول مرحلي في Dataverse بواسطة سجلات من SQL Server، ولمزامنة الجدول المرحلي بشكل دوري باستخدام توزيع تزايدي من SQL Server.

الاستعلام المتقدم متكامل مع التدفق لتمكين تحويل البيانات والدفع المتزايد.

لتنزيل القالب **Power Automate – توصيل وتنفيذ SQL**، انتقل إلى [Power Automate – توصيل وتنفيذ SQL](https://go.microsoft.com/fwlink/?linkid=2081789) على مركز تنزيل Microsoft.

## <a name="additional-resources"></a>الموارد الإضافية

[Microsoft Power Platform](/power-platform/admin/admin-documentation)</br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]