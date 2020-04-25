---
title: الميزات التي تمت إزالتها أو إهمالها في Dynamics 365 Finance
description: يصف هذا الموضوع الميزات التي تمت إزالتها أو تلك المخطط لإزالتها من Dynamics 365 Finance.
author: roschlom
manager: AnnBe
ms.date: 03/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: aebce032d7d780b296ba74fea4467425a3cbe1a7
ms.sourcegitcommit: 4e9b3746790355f9f72bbfddc099c4065a49ad63
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/30/2020
ms.locfileid: "3175098"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>الميزات التي تمت إزالتها أو إهمالها في Dynamics 365 Finance

[!include [banner](../includes/banner.md)]

يصف هذا الموضوع الميزات التي تمت إزالتها أو تلك المخطط لإزالتها من Dynamics 365 Finance.

- لم تعد ميزة *تمت الإزالة* متوفرة في المنتج.
- لا توجد ميزة *المهملة* في التطوير النشط وقد يتم إزالتها في تحديثات مستقبلية.

تهدف هذه القائمة إلى مساعدتك في مراعاة ميزات الإزالة وعمليات الإهلاك للتخطيط الخاص بك. 

> [!NOTE]
> يمكن العثور على معلومات مفصلة حول الكائنات في تطبيقات Finance and Operations [التقارير المرجعية التقنية](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). يمكنك مقارنة إصدارات مختلفة من هذه التقارير لمعرفة المزيد حول الكائنات التي تم تغييرها أو التي تمت إزالتها من كل إصدار من تطبيقات Finance and Operations.

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a>ميزات تمت إزالتها أو إهمالها في الإصدار 10.0.12 من Finance

### <a name="polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a>تقارير SSRS البولندية: سجل ضريبة القيمة المضافة للإخراج، سجل ضريبة القيمة المضافة للإدخال، سجل تقرير ملخص ضريبة القيمة المضافة للاتحاد الأوروبي‬، مرجع الميزة PL-00014

|   |  |
|------------|--------------------|
| **سبب الإهلاك/الإزالة** | غير مطلوبة من الناحية القانونية.  |
| **هل تم الاستبدال بميزة أخرى؟**   | نعم (تنسيق Excel لملف المراجعة القياسي مع إقرار ضريبة القيمة المضافة - JPK_VDEK) |
| **مناطق المنتجات المتأثرة**         | التطبيق |
| **خيارات النشر**              | ‏‏الكل |
| **الحالة**                         | ميزات مهملة: بحلول 1 يوليو 2021، سنتوقف عن توفير الدعم لتقارير SSRS: **سجل ضريبة القيمة المضافة للإخراج، سجل ضريبة القيمة المضافة للإدخال، سجل تقرير ملخص ضريبة القيمة المضافة للاتحاد الأوروبي‬، مرجع الميزة PL-00014‬**. بدلاً من ذلك، سيتم تقديم مثال عن تنسيق Excel لملف المراجعة القياسي مع إقرار ضريبة القيمة المضافة (JPK_VDEK). |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a>ميزات تمت إزالتها أو إهمالها في الإصدار 10.0.11 من Finance

### <a name="norwegian-standard-main-accounts"></a>الحسابات النرويجية الرئيسية القياسية

|   |  |
|------------|--------------------|
| **سبب الإهلاك/الإزالة** | إعادة التصميم  |
| **هل تم الاستبدال بميزة أخرى؟**   | نعم (تم استبداله بالمعلمات الخاصة بتطبيق تنسيق التقارير الإلكترونية) |
| **مناطق المنتجات المتأثرة**         | التطبيق |
| **خيارات النشر**              | ‏‏الكل |
| **الحالة**                         | ميزة مهملة: بحلول 1 ابريل 2021، نخطط لإيقاف دعم الوظيفة ذات الصلة بالحسابات الرئيسية القياسية: حقل المرجع، الجدول ذو الصلة، كيان البيانات. |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a>ميزات تمت إزالتها أو إهمالها في الإصدار 10.0.7 من Finance

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>لم يعد مربع حوار تغيير طلب سير العمل يتضمن القائمة المنسدلة لتحديد المستخدم
|   |  |
|------------|--------------------|
| **سبب الإهلاك/الإزالة** | يتم تغييرها إلى الميزة مع تحديد مجموعات الحساب.  |
| **هل تم الاستبدال بميزة أخرى؟**   | ‏‏نعم |
| **مناطق المنتجات المتأثرة**         | سير العمل |
| **خيارات النشر**              | ‏‏الكل |
| **الحالة**                         | مهمل: بحلول 1 ديسمبر 2020، لا نقدم خطط لدعم إعداد أنواع الإيصالات الصينية دون تحديد مجموعات الحساب. يمكنك العثور على مزيد من التفاصيل حول التصميم الجديد في [ما الجديد في الإصدار 10.0.7](whats-new-changed-10-0-7.md). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>الإعلانات السابقة حول الميزات التي تمت إزالتها أو إهمالها
لمعرفه المزيد حول الميزات التي تمت إزالتها أو إهمالها في الإصدارات السابقة، راجع [‏‫الميزات التي تمت إزالتها أو إهمالها في الإصدارات السابقة‬](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).
