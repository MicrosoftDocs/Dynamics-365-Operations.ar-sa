---
title: تكوين معلمات إدارة المزايا لكل شركة
description: قم بتكوين المعلمات لإدارة الميزات لكل شركة في Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 12/07/2020
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
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2943d0095e4c9421725b90e579b7cbb841038ab7
ms.sourcegitcommit: d02fae79d5c02a4bc4f4b16a410c2f5ce026c204
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/05/2021
ms.locfileid: "4984590"
---
# <a name="configure-benefits-management-parameters-per-company"></a>تكوين معلمات إدارة المزايا لكل شركة

بالنسبة لكل مؤسسة تقدم مزايا، يجب عليك تكوين الإعدادات لرسائل البريد الإلكتروني لتأكيد المزايا.

## <a name="configure-confirmation-email-settings"></a>تكوين إعدادات البريد الإلكتروني للتأكيد

1. في مساحة عمل **إدارة الميزات**، ضمن **الإعداد**، حدد **معلمات الموارد البشرية**.

2. في علامة التبويب **إدارة المزايا**، حدد قيمًا للحقول التالية: 

   | الحقل | الوصف |
   | --- | --- |
   | **إرسال بريد إلكتروني للتأكيد** | عند تشغيل هذه الميزة، سيتم إرسال بريد إلكتروني للتأكيد إلى الموظفين عند تسجيل الخروج من تجربة تسجيل المزايا في الخدمة الذاتية للموظف. |
   | **قالب البريد الإلكتروني للتأكيد** | حدد قالب البريد الإلكتروني للمؤسسة لاستخدامه عند إرسال تأكيد التسجيل. إذا لم تحدد نموذجًا، فسيتم إرسال البريد الإلكتروني العام التالي:<br><br>%EmployeeFirstName%،<br><br>تهانينا! لقد أكملت بنجاح التسجيل في المزايا.<br><br>شكرًا لك،<br>مزايا <Company/Org name>. |
   | **عنوان مرسل البريد الإلكتروني الافتراضي** | عنوان البريد الإلكتروني المراد استخدامه عند إرسال رسالة التأكيد عبر البريد الإلكتروني. |

3. حدد **حفظ**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]