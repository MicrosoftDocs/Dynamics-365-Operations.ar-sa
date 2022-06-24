---
title: معالجة تغييرات المعدلات
description: توضح هذه المقالة كيفية معالجة تغييرات معدل المزايا في Microsoft Dynamics 365 Human Resources.
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
ms.openlocfilehash: 09714c70cb00b1a1b5dbd4613bbd70ff11d35cb2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882942"
---
# <a name="process-rate-changes"></a>معالجة تغييرات المعدلات


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

توضح هذه المقالة كيفية معالجة تغييرات معدل المزايا في Microsoft Dynamics 365 Human Resources عندما تحتوي خطة ميزة جديدة أو حالية في إعدادات قاعدة الأهلية. إذا تم إنشاء قاعدة أهلية جديدة وتعيينها إلى الخطة، فإن هذا سيطالب النظام بإعادة تشغيل أهلية العامل للتحقق مما إذا كان من الممكن تأهيل العاملين الآن للخطة بناءً على خيارات الأهلية الجديدة. 

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
