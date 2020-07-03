---
title: توسيع Talent باستخدام Power Apps وPower Automate
description: يصف هذا المقال بعض الأمثلة عن سيناريوهات قابلية التوسعة في Microsoft Dynamics 365 Human Resources التي تستخدم Microsoft Power Apps وMicrosoft Power Automate.
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: Dynamics 365 Human Resources;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core;Experience Apps;Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 36b8145764338b91bfedf96c43a7137a89831742
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410094"
---
# <a name="extend-with-power-apps-and-power-automate"></a>توسيع باستخدام Power Apps وPower Automate

يصف هذا المقال بعض الأمثلة عن سيناريوهات قابلية التوسعة في Microsoft Dynamics 365 Human Resources التي تستخدم Microsoft Power Apps وMicrosoft Power Automate. يمكنك استيراد حزمة الحل المقترنة بكل مثال إلى بيئتك في Power Apps. بعد ذلك، يمكنك استخدام الحزم كنقاط إرشادية أو كنقاط بداية لتنفيذ السيناريوهات التي تنطبق على مؤسستك.

> [!IMPORTANT]
> إذا أردت استخدام القوالب والتطبيقات التي تم وصفها في الموضوع "كما هي"، فتأكد من اختبارها للتأكد من أنها تغطي كافة السيناريوهات المتعلقة بعملية التنفيذ التي تقوم بها.

## <a name="prerequisites"></a>المتطلبات الأساسية

- لاستيراد الحزم، يجب أن يتوفر إذن **أداة إنشاء البيئة** لدى المستخدمين.
- لتصدير التطبيقات أو استيرادها، يجب أن يتوفر لدى المستخدمين ترخيص Power Apps Plan 2 أو ترخيص إصدار تجريبي Power Apps Plan 2.

## <a name="integration-with-office-365-power-automate"></a>التكامل مع Office 365 وPower Automate

يمكن استخدام تطبيق **التكامل مع Office 365** لاستخراج معلومات الفريق للمستخدمين الذين سجلوا دخولهم من Microsoft Office 365. ويشير إلى العاملين في الموارد البشرية لاستخراج أنواع ‏‫معرفات الموظفين. يمكن للمديرين فحص تواريخ انتهاء صلاحية أنواع معرفات الموظفين. كما يمكنهم إرسال تذكير بالبريد الكتروني إذا انتهت صلاحية نوع معرف الموظف. يتكامل Power Automate مع Power Apps لإرسال هذا التذكير. سيتم إعادة إرسال التأكيد إلى Power Apps من Power Automate وقت إرسال التذكير. تتضمن أنواع التعريف رخصة القيادة وجواز السفر والنماذج الأخرى المقبولة للمعرف.

يمكنك توسيع هذا التطبيق لسيناريوهات أخرى. على سبيل المثال، يمكن استخدامه لإظهار معلومات العطلة الخاصة بالفريق بالإضافة إلى أحداث التقويم وأي أحداث خاصة بالفريق.

لتنزيل تطبيق **تكامل مع Office 365 و Power Automate**، انتقل إلى [تكامل مع Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) على مركز التنزيل لـ Microsoft.

## <a name="power-automate--sql-connect-and-execute"></a>Power Automate – توصيل وتنفيذ SQL

يقوم القالب **Power Automate – توصيل وتنفيذ SQL‬** بالتوصيل بخادم Microsoft SQL Server ويتيح تشغيل استعلامات SQL.

على الرغم من أن هذا القالب يقرأ جداول SQL ويقوم بتحديثه، إلا أنه يمكنك توسيعه واستخدامه في السيناريوهات الأخرى. على سبيل المثال، يمكن استخدامه لتعبئة جدول مرحلي في Common Data Service بواسطة سجلات من SQL Server، ولمزامنة الجدول المرحلي بشكل دوري باستخدام توزيع تزايدي من SQL Server.

الاستعلام المتقدم متكامل مع التدفق لتمكين تحويل البيانات والدفع المتزايد.

لتنزيل القالب **Power Automate – توصيل وتنفيذ SQL**، انتقل إلى [Power Automate – توصيل وتنفيذ SQL](https://go.microsoft.com/fwlink/?linkid=2081789) على مركز تنزيل Microsoft.

## <a name="additional-resources"></a>الموارد الإضافية

[Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>