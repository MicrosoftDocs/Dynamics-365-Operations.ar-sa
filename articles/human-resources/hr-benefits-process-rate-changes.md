---
title: معالجة تغييرات المعدلات
description: يشرح هذا الموضوع كيفية معالجة تغييرات معدل المزايا في Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitRate, BenefitEligibilityProcessResultViewer
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5e0dfbdde8ee950a0341fffb1e268fff05434953
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070365"
---
# <a name="process-rate-changes"></a>معالجة تغييرات المعدلات


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يشرح هذا الموضوع كيفية معالجة تغييرات معدل المزايا في Microsoft Dynamics 365 Human Resources عندما تحتوي خطة ميزة جديدة أو حالية في إعدادات قاعدة الأهلية. إذا تم إنشاء قاعدة أهلية جديدة وتعيينها إلى الخطة، فإن هذا سيطالب النظام بإعادة تشغيل أهلية العامل للتحقق مما إذا كان من الممكن تأهيل العاملين الآن للخطة بناءً على خيارات الأهلية الجديدة. 

1. في مساحة العمل **إدارة الميزات**، ضمن **معالجة**، حدد **معالجة تحديث تغيير المعدل**.

2. في مربع الحوار **تشغيل معالجة معدل الميزة**، حدد قيم الحقول التالية:

   | الحقل | ‏‏الوصف |
   | --- | --- |
   | **فترة التسجيل** | تغييرات المعدل المراد معالجة الأحداث الحياتية خلالها. |

3. إذا كنت ترغب في تشغيل العملية في الخلفية، حدد **تشغيل في الخلفية** وقم بالمهام التالية:

   1. إدخال المعلومات للمعالجة.

   2. لإعداد مهمة متكررة، حدد **التكرار**، وادخل معلومات التكرار، وحدد **موافق**.

   3. لإعداد تنبيه بالمهمة، حدد **التنبيهات**، وحدد التنبيهات المراد استلامها، ثم حدد **موافق**.

   4. حدد **موافق**. سيتم تشغيل العملية باستخدام المعلمات التي قمت بتعيينها.

4. حدد **موافق**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
