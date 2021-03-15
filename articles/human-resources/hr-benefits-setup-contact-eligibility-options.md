---
title: تكوين خيارات أهلية جهة الاتصال الشخصية
description: قم بتكوين خيارات الأهلية لجهات الاتصال الشخصية في Microsoft Dynamics 365 Human Resources. يمكن أن تكون جهات الاتصال الشخصية من المستفيدين أو التابعين.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 137416477928fd4d6b4438f25df5afea93972027
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111348"
---
# <a name="configure-personal-contact-eligibility-options"></a>تكوين خيارات أهلية جهة الاتصال الشخصية

يوضح هذا المقال كيفية تكوين أنواع جهات الاتصال الشخصية لاستخدامها في الميزات الموجودة في Microsoft Dynamics 365 Human Resources. يمكن أن تكون جهات الاتصال الشخصية من المستفيدين أو التابعين. 

1. في مساحة العمل **إدارة الميزات**، ضمن **إعداد**، حدد **خيارات أهلية جهات الاتصال الشخصية**.

2. حدد **جديد**.

3. حدد قيمًا للحقول التالية:

   | الحقل | ‏‏الوصف |
   | --- | --- |
   | **خيار الاستحقاق** | اسم أو كود خيار أهلية فريد لتحديد خيار الأهلية. |
   | **‏‏الوصف** | وصف مختصر لخيار الأهلية. |
   | **كود استحقاق جهات الاتصال** | كود النظام الذي يصف خيار الاستحقاق الشخصي بشكل أفضل. يمكنك الاختيار من بين: <ul><li>العلاقة</li><li>الطالب</li><li>معال مسن</li><li>المعال المعاق المسن</li></ul> |
   | **الحالة** | حالة خيار الأهلية. إذا تم تعيين حالة أحد خيارات الأهلية على غير نشط، فلا يمكنك تحديد خيار أهلية الاتصال الشخصي لجهات الاتصال الشخصية. |
   | **العلاقة** | يحدد العلاقة بين جهة الاتصال الشخصية والموظف. يكون هذا الحقل نشطًا فقط في حالة تعيين كود أهلية جهة الاتصال على العلاقة. |
   | **العمر** | السن الأقصى لجهة اتصال شخصية مؤهلة لخطة الميزة. يكون هذا الحقل نشطًا فقط في حالة تحديد علاقة. تتم مقارنة هذا العمر بالسن المحسوب لجهة الاتصال الشخصية. السن المحسوب هو: (تاريخ التغطية – تاريخ ميلاد جهة اتصال شخصية / 365). ودائمًا ما يكون هذا الرقم عددًا صحيحًا. |

4. حدد **حفظ**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]