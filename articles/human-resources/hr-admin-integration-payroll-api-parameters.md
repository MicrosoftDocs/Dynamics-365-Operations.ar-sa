---
title: معلمات تكامل كشف الرواتب
description: يصف هذا الموضوع معلمات تكامل كشف الرواتب في Dynamics 365 Human Resources.
author: marcelbf
ms.date: 06/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-17
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 37d4dc52e7fe5ddd95f43d98267db819a275bd92
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069847"
---
# <a name="payroll-integration-parameters"></a>معلمات تكامل كشف الرواتب


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

قبل استخدام تكامل كشف الرواتب في Dynamics 365 Human Resources، يجب إعداد المعلمات الموضحة في هذا الموضوع.

## <a name="enable-payroll-address"></a>تمكين عنوان كشف الرواتب

لكي تتمكن من استخدام عنوان كشف الرواتب، يجب تمكينه من [نموذج المعلمات المشتركة](hr-setup-shared-parameters.md) في علامة تبويب تكامل كشف الرواتب.

## <a name="define-the-identification-type"></a>تحديد نوع التعريف

لكشف معرف نوع التعريف في [كيان موظف كشفالرواتب](hr-admin-integration-payroll-api-payroll-employee.md)، يجب تكوين [معلمات الموارد البشرية](hr-setup-shared-parameters.md) لكل شركة.

1. في مساحة عمل **إدارة التعويض**، ضمن الارتباطات، حدد **معلمات الموارد البشرية**. 
2. في علامة التبويب **تكامل كشف الرواتب**، حدد قيمة الحقول التالية.

| الحقل | الوصف |
| --- | --- |
| استخدام أنواع التعريف في معالجة كشف الرواتب | عند تحديد هذا الخيار، سيتم الكشف عن معرف النوع المحدد في كيان موظف الرواتب. |
| نوع التعريف | نوع التعريف الذي سيتم كشفه في الحقل **mshr_payrollemployeeentityid** لـ [كيان موظف الرواتب](hr-admin-integration-payroll-api-payroll-employee.md). |

## <a name="see-also"></a>راجع أيضًا

[‏‫مقدمة إلى واجهة API لتكامل كشف الرواتب](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
