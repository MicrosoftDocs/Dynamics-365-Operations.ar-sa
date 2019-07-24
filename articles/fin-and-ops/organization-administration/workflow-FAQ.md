---
title: الأسئلة المتداولة حول سير العمل
description: يجيب هذا الموضوع عن الأسئلة المتداولة حول نظام سير العمل في Microsoft Dynamics 365 for Finance and Operations.
author: ChrisGarty
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: adcc9bbc422a3fddfd51d248daf95c0da6d4c9bb
ms.sourcegitcommit: 8cf77e9171d6cad8ae6c8bfad9e4f9a46fef6d23
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/19/2019
ms.locfileid: "1688990"
---
# <a name="workflow-faq"></a>الأسئلة المتداولة حول سير العمل

[!include [banner](../includes/banner.md)]

يجيب هذا الموضوع عن الأسئلة المتداولة حول نظام سير العمل في Microsoft Dynamics 365 for Finance and Operations.

## <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>لماذا أتلقى إخطارات متعددة عند رفض عنصر عمل؟
عند رفض عنصر عمل، يتم إكمال هذا العنصر كعنصر مرفوض. ويتم إنشاء عنصر عمل آخر وتعيينه إلى المنشئ. وهذا يعني إرسال إخطار إلى المنشئ يتعلق بعنصر العمل المرفوض وإخطار منفصل إلى المستخدم المعيّن إلى عنصر العمل الجديد "التغيير المطلوب‬". 

يتعلق كل إخطار بعنصر عمل مختلف، ولكن التشابه قد يسبب الإرباك. نحن بصدد البحث عن طرق لتحسين هذا الأمر في إصدار مستقبلي.

## <a name="why-are-my-workflow-exports-failing"></a>لماذا يفشل تصدير عمليات سير العمل؟
يوجد حاليًا قيد في ميزة تصدير عمليات سير العمل يمنع تجاوز أسماء عمليات سير العمل 48 حرفًا. قد يؤدي استخدام اسم أطول من 48 حرفًا إلى ظهور الخطأ "فشل الخادم في مصادقة الطلب" و/أو منع تصدير ملف بدون نوع ملف. يوفر منشور المدونة التالي المزيد من التفاصيل [استكشاف أخطاء تصدير سير العمل وإصلاحها](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).

## <a name="can-the-submitter-of-a-workflow-also-approve-the-workflow"></a>هل يمكن لمرسل سير عمل القيام أيضًا الموافقة على سير العمل؟
نعم، يمكن أيضًا لمرسل سير عمل الموافقة على سير العمل إذا تم تكوينه بهذه الطريقة. لمنع حدوث مثل هذا السلوك، عيِّن **معلمات سير العمل > عام > المعتمد > عدم السماح للمرسِل بالموافقة‬**على **نعم**.

## <a name="can-i-add-alerts-to-workflows-to-provide-notifications-to-users"></a>هل يمكنني إضافة تنبيهات إلى مهام سير العمل لتوفير إخطارات للمستخدمين؟
فيما يلي بعض المناطق الأساسية لملاحظة إضافة تنبيهات إلى مهام سير العمل لتوفير إخطارات:
- التنبيهات مقابل آليات إخطار سير العمل
    - يمكن إعداد التنبيهات لتغييرات السجلات. تغير مهام سير العمل السجلات، لذا من الممكن إعداد تنبيه مرتبط بتغيير سجل يحدث بسبب سير عمل. ولكن نظرًا لوجود خيارات إخطار مضمنة مختلفة لمهام سير العمل، لا يعد استخدام التنبيهات مثاليًا.
- إخطارات قياسية من مهام سير العمل 
    - توجد إخطارات بريد إلكتروني مضمنة ف مهام سير العمل. يمكن للعميل تكوين الإخطارات بحيث يتم إرسال رسائل بريد إلكتروني إلى المستخدمين. لا تؤدي هذه الإخطارات إلى إرسال رسائل مركز الإجراءات للمستخدمين.
    - في أحد التحديثات المستقبلية ستتم إضافة رسالة مركز الإجراءات حتى يتم تعيين عنصر عمل سير العمل إلى المستخدم. 
- إضافة إخطارات لمهام سير العمل
    - يمكن إنشاء رسائل مركز الإجراءات لمستخدمين محددين، مثل رسالة تم إنشاؤها من سير عمل في X++.
    - [تحتوي مهام سير العمل علي أحداث أعمال](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) يمكن للعميل استخدامها لتشغيل المهام ذات الإشعارات التي يبحث عنها.   

وفي الملخص، في حالة عدم حصول المستخدم على الإخطار المناسب من مركز الإجراءات عند تعيين عنصر عمل لسير العمل، قم بزيادة [أحداث أعمال سير العمل](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) مع Microsoft Flow لتوفير إخطارات إضافية أو مختلفة.
