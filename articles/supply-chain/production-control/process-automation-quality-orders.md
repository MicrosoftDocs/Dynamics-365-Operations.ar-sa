---
title: استدعاء تدفقات التشغيل التلقائي للعمليات لإنشاء أوامر الجودة
description: يقدم هذا المقال موارد لاستخدام Power Automate لتنفيذ العمليات التجارية تلقائيًا، باستخدام مثال أوامر الجودة.
author: johanhoffmann
ms.date: 05/28/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-05-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a9c1cb7664963e60dcf6e50c7367f33382373832
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890701"
---
# <a name="invoke-process-automation-flows-to-create-quality-orders"></a>استدعاء تدفقات التشغيل التلقائي للعمليات لإنشاء أوامر الجودة

[!include [banner](../includes/banner.md)]

ويكون للمؤسسات طلب متزايد لتنفيذ العمليات التجارية القياسية تلقائيًا، وتوفير تعاملات أكثر ملائمة للفريق، واستخدام العديد من إشارات البيانات والأنظمة لمعالجة العمليات التجارية تلقائيًا. باستخدام التشغيل التلقائي للعمليات (RPA) و Microsoft Power Automate، يمكن للأعمال استخدام تجربة بدون كود لتنفيذ العمليات المتكررة تلقائيًا، ومن ثم الحصول على الكفاءة والدقة.

يعرض قالب حل التشغيل التلقائي القابل للتنزيل لـ Supply Chain Management الكيفية التي يمكن بها استخدام Power Automate لتنفيذ العمليات التجارية تلقائيًا باستخدام أوامر الجودة كمثال.

يمكنك تنزيل قالب حل التشغيل التلقائي [هنا](https://aka.ms/D365SCMQualityOrderRPASolution).

للحصول على نظرة عامة حول هذه الميزة والقدرات الخاصة بها، راجع الفيديو التالي: [استخدام RPA لإنشاء أوامر جودة في Dynamics 365 Supply Chain Management](https://www.youtube.com/watch?v=LFbzJ6-H89w)

![خيارات التشغيل التلقائي مع RPA.](media/rpa-automation-options.png "خيارات التشغيل التلقائي مع RPA")

يتضمن قالب حل Power Automate تدفق تنفيذ تلقائي لمجموعة وتدفق التشغيل التلقائي لسطح المكتب والذي يقوم بالتشغيل التلقائي بإنشاء أوامر الجودة في Supply Chain Management.

يمكن بدء التشغيل التلقائي كاستجابة للعديد من الأحداث والإشارات، بما في ذلك الإشارات الخاصة بإدخال المستخدم أو الجهاز (بما في ذلك إنترنت الأشياء (IoT)). يتم تضمين تطبيق Power *Q-Order* في قالب الحل. يسمح للمستخدم بمسح كود QR للصنف، وإدخال الكمية وإرفاق الصور باستخدام كاميرا.

يتم تضمين معلمات الحل لتكوين التشغيل التلقائي لحالة استخدام معينة في تسهيل الإنتاج.

![إنشاء أمر الجودة.](media/rpa-create-quality-roder.png "إنشاء أمر الجودة")

للحصول على دليل كامل خطوة بخطوة حول كيفية تنزيل حل نموذج وتثبيته واستخدامه للتشغيل التلقائي لإنشاء أمر الجودة، راجع [‬‏‫التشغيل التلقائي لإنشاء أمر الجودة على Dynamics 365 Supply Chain Management بواسطة التشغيل التلقائي للعمليات Power Automate Desktop](/power-automate/desktop-flows/dynamics365-scm-rpa).

