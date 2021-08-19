---
title: معالجة تغييرات المعدل
description: قم بمعالجة تغييرات معدل الميزة في Microsoft Dynamics 365 Human Resources عندما تحتوي خطة ميزة جديدة أو حالية في إعدادات قاعدة الأهلية.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitRate, BenefitEligibilityProcessResultViewer
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: eb9206df990fa8980c4c641b565203828715ada9f1d2f2107a7bb707f545e225
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718121"
---
# <a name="process-rate-changes"></a>معالجة تغييرات المعدل

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

قم بمعالجة تغييرات معدل الميزة في Microsoft Dynamics 365 Human Resources عندما تحتوي خطة ميزة جديدة أو حالية في إعدادات قاعدة الأهلية. إذا تم إنشاء قاعدة أهلية جديدة وتعيينها إلى الخطة، فإن هذا سيطالب النظام بإعادة تشغيل أهلية العامل للتحقق مما إذا كان من الممكن تأهيل العاملين الآن للخطة بناءً على خيارات الأهلية الجديدة. 

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