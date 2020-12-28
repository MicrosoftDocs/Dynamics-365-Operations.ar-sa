---
title: تحسين الأداء من خلال جدولة وظائف دفعية بعد ساعات العمل
description: يوضح هذا الموضوع كيفية حل بعض مشكلات الأداء باستخدام Microsoft Dynamics 365 Human Resources عن طريق جدولة الوظائف الدفعية التي يستغرق تشغيلها فترة طويلة بعد ساعات العمل.
author: andreabichsel
manager: AnnBe
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 452a87cf5ba6c1ac73636584d75b2ec2ac555e02
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527755"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a>تحسين الأداء من خلال جدولة وظائف دفعية بعد ساعات العمل

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a>المشكلة

يمكن أن يواجه Microsoft Dynamics 365 Human Resources مشكلات في الأداء إذا كانت الوظائف الدفعية التي يستغرق تشغيلها فترة طويلة تعمل أثناء ساعات العمل العادية.

## <a name="resolution"></a>الحل‬

قم بجدولة الوظائف الدفعية التالية أثناء الساعات توقف العمل. نوصي أيضًا بمراجعة تكرار الوظائف الدفعية التي تعمل بشكل متكرر. قم بتخفيض تكرار الوظيفة الدفعية إذا كان ذلك ممكنا. في العديد من الحالات، يكون التكرار الافتراضي كافيًا.

يجب تشغيل الوظائف الدفعية التالية ليلا أو بعد ساعات العمل. تأكد من التحقق من المنطقة الزمنية لهذه الوظائف الدفعية المتكررة. قد تستخدم بعض الوظائف الدفعية التوقيت الرسمي الباسيفيكي (PST).

| وظيفة دفعية | التكرار الافتراضي |
| --- | --- |
| تنظيف محفوظات الوظائف الدفعية | مرة واحدة كل شهر |
| تصدير تنظيف التشغيل المرحلي | مرة واحدة كل يوم |
| مزامنة الطلب المفقود لتكامل Common Data Service | مرة واحدة كل يوم |
| وظيفة نظام ضغط قاعدة البيانات التي يلزم تشغيلها بشكل منتظم خلال ساعات توقف العمل | مرة واحدة كل يوم |
| وظيفة نظام إعادة بناء فهرس قاعدة البيانات التي يلزم تشغيلها بشكل منتظم خلال ساعات توقف العمل | مرة واحدة كل يوم |

1. في Human Resources، حدد **إدارة النظام**.

2. في شريط **البحث**، ابحث عن إحدى الوظائف الدفعية المذكورة أعلاه.

3. حدد **تشغيل في الخلفية**، ثم حدد **التكرار**.

   ![تعيين التكرار](media/talent-batch-history-cleanup-recurrence.png)

4. تحت **تعريف التكرار**، قم بتعيين **تاريخ البدء** و **وقت البدء** بحيث يقعان خلال ساعات التوقف عن العمل أو عطلة نهاية الأسبوع. حدد **بلا تاريخ انتهاء**. 

   ![تعيين تاريخ بدء التكرار ووقته](media/talent-batch-history-cleanup-define-recurrence.png)

5. حدد **موافق**.

6. إذا لزم الأمر، قم بتغيير أي معلمات أخرى تحت **تشغيل في الخلفية**، ثم حدد **موافق**.

## <a name="additional-resources"></a>الموارد الإضافية

[تحسين الأداء باستخدام مهام التنظيف التلقائية](hr-admin-troubleshooting-batch-history.md)
