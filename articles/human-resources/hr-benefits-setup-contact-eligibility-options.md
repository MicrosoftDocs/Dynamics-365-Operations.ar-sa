---
title: تكوين خيارات أهلية جهة الاتصال الشخصية
description: قم بتكوين خيارات الأهلية لجهات الاتصال الشخصية في Microsoft Dynamics 365 Human Resources. يمكن أن تكون جهات الاتصال الشخصية من المستفيدين أو التابعين.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 49a519aafc56c303765619a66d815d79b668d0f9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790874"
---
# <a name="configure-personal-contact-eligibility-options"></a>تكوين خيارات أهلية جهة الاتصال الشخصية

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

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