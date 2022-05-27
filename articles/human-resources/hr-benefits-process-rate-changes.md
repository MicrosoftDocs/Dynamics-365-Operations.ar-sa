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
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c1eea61df6dd5fbe0b52a21944deba69928b5125
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/04/2022
ms.locfileid: "8696115"
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
