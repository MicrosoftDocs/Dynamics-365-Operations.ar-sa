---
title: الأسئلة المتداولة حول سير العمل
description: يجيب هذا الموضوع عن الأسئلة المتداولة حول نظام سير العمل في Microsoft Dynamics 365 for Finance and Operations.
author: ChrisGarty
manager: AnnBe
ms.date: 05/07/2019
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
ms.openlocfilehash: f6240b1b5136937aa47f455547fed6f0c7c08e2c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/07/2019
ms.locfileid: "1509281"
---
# <a name="workflow-system"></a>نظام سير العمل

[!include [banner](../includes/banner.md)]

يجيب هذا الموضوع عن الأسئلة المتداولة حول نظام سير العمل في Microsoft Dynamics 365 for Finance and Operations.

## <a name="notifications"></a>الإخطارات

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>لماذا أتلقى إخطارات متعددة عند رفض عنصر عمل؟
عند رفض عنصر عمل، يتم إكمال هذا العنصر كعنصر مرفوض. ويتم إنشاء عنصر عمل آخر وتعيينه إلى المنشئ. وهذا يعني إرسال إخطار إلى المنشئ يتعلق بعنصر العمل المرفوض وإخطار منفصل إلى المستخدم المعيّن إلى عنصر العمل الجديد "التغيير المطلوب‬". 

يتعلق كل إخطار بعنصر عمل مختلف، ولكن التشابه قد يسبب الإرباك. نحن بصدد البحث عن طرق لتحسين هذا الأمر في إصدار مستقبلي.

### <a name="why-are-my-workflow-exports-failing"></a>لماذا يفشل تصدير عمليات سير العمل؟
يوجد حاليًا قيد في ميزة تصدير عمليات سير العمل يمنع تجاوز أسماء عمليات سير العمل 48 حرفًا. قد يؤدي استخدام اسم أطول من 48 حرفًا إلى ظهور الخطأ "فشل الخادم في مصادقة الطلب" و/أو منع تصدير ملف بدون نوع ملف. يوفر منشور المدونة التالي المزيد من التفاصيل [استكشاف أخطاء تصدير سير العمل وإصلاحها](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).
