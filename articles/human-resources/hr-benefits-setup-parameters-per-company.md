---
title: تكوين محددات إدارة المزايا لكل شركة
description: توضح هذه المقالة كيفية تكوين المعلمات لإدارة الميزات لكل شركة في Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 8/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e9516977002280e17ee82bf7581d8d7c5060de2a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904206"
---
# <a name="configure-benefits-management-parameters-per-company"></a>تكوين معلمات إدارة المزايا لكل شركة


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

بالنسبة لكل مؤسسة تقدم مزايا، يجب عليك تكوين الإعدادات لرسائل البريد الإلكتروني لتأكيد المزايا.

## <a name="configure-confirmation-email-settings"></a>تكوين إعدادات البريد الإلكتروني للتأكيد

1. في مساحة عمل **إدارة الميزات**، ضمن **الإعداد**، حدد **معلمات الموارد البشرية**.

2. في علامة التبويب **إدارة المزايا**، حدد قيمًا للحقول التالية: 

   | الحقل | الوصف |
   | --- | --- |
   | **إرسال بريد إلكتروني للتأكيد** | عند تشغيل هذه الميزة، سيتم إرسال بريد إلكتروني للتأكيد إلى الموظفين عند تسجيل الخروج من تجربة تسجيل المزايا في **الخدمة الذاتية للموظف**. |
   | **قالب البريد الإلكتروني للتأكيد** | حدد قالب البريد الإلكتروني للمؤسسة لاستخدامه عند إرسال تأكيد التسجيل. إذا لم تحدد نموذجًا، فسيتم إرسال البريد الإلكتروني العام التالي:<br><br>%EmployeeFirstName%،<br><br>تهانينا! لقد أكملت بنجاح التسجيل في المزايا.<br><br>شكرًا لك،<br>مزايا <Company/Org name>. |
   | **عنوان مرسل البريد الإلكتروني الافتراضي** | عنوان البريد الإلكتروني المراد استخدامه عند إرسال رسالة التأكيد عبر البريد الإلكتروني. |

3. حدد **حفظ**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
