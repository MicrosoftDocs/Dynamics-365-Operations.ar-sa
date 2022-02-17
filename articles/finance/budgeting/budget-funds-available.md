---
title: أموال الموازنة المتاحة
description: يقدم هذا الموضوع ميزة أموال الموازنة المتوفرة ويوفر معلومات يمكن أن تساعدك في تكوين التحكم في الموازنة لتحسين إدارة الموارد المالية لمؤسستك.
author: rcarlson
ms.date: 11/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetControlConfiguration
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "60493"
- intro-internal
ms.assetid: be964167-43bc-431d-9adb-48bff32d68d5
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2021-11-28
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: a8279ae9b08c7537548c1c8b71e6e978fee2b8a1
ms.sourcegitcommit: c85eac17fbfbd311288b50664f9e2bae101c1fe6
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/03/2021
ms.locfileid: "7891298"
---
# <a name="budget-funds-available"></a>أموال الموازنة المتاحة

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

يقدم هذا الموضوع ميزة أموال الموازنة المتوفرة ويوفر معلومات يمكن أن تساعدك في تكوين التحكم في الموازنة لتحسين إدارة الموارد المالية لمؤسستك.

## <a name="enhanced-calculation-feature-for-budget-funds-available"></a>ميزة حساب معززة لأموال الموازنة المتاحة

تتيح لك الميزة **ميزة الحساب المسار الوحيد في أموال الموازنة** تتبع جداول رقابة الموازنة الأساسية لأنواع المستندات والحالات، استنادًا إلى الإعدادات في الصفحة **تحديد معلمات رقابة الموازنة**.

يجب أن يكون لدى بعض خيارات تكوين رقابة الموازنة إعدادات محددة لكي تعمل الميزة بشكل صحيح. يتم تحديد هذه الخيارات أو إلغاء تحديدها في علامة التبويب **أموال الموازنة المتوفرة** للصفحة **تحديد معلمات رقابة الموازنة**. يعرض الجدول التالي الإعدادات المطلوبة لميزة أموال الموازنة المتوفرة.

| إذا تم تحديد هذا الخيار | يجب تحديد هذا الخيار أيضًا |
| ------------------------- | -------------------------------- |
| حجوزات الموازنة للالتزامات المسبقة | حجوزات الموازنة للالتزامات *و* النفقات الفعلية |
| حجوزات الموازنة للالتزامات | النفقات الفعلية |
| حجوزات الموازنة للالتزامات باستخدام مستندات نوع طلب الشراء | حجوزات الموازنة للالتزامات المسبقة |

تؤثر هذه الميزة على المستندات الجديدة فقط. سيستمر تتبع مبالغ المستندات الموجودة ويتم عرضها في استعلام إحصائيات التحكم في الموازنة حتى يتم تغيير إعداد أموال الموازنة المتوفرة وتنشيط تكوين رقابة الموازنة الجديدة. وعند هذه النقطة، ستتم إزالة بيانات تتبع الموازنة للمستندات التي تمت إزالتها من حساب أموال الموازنة المتوفرة.

نُوصي بإلغاء تحديد الخيار **النفقات الفعلية غير المرحلة**. في حالة تحديد هذا الحقل، يتم إجراء حساب رقابة الموازنة الأمر الذي يتسغرق بعض الوقت على المستندات غير المرحلة، مثل فواتير المورد المعلقة.