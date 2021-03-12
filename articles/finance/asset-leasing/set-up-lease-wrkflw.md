---
title: إعداد سير عمل الموافقة على الإيجار
description: يوضح الموضوع كيفية إعداد سير عمل معتمدة سيتم تشغيله عند إنشاء عقد إيجار جديد.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d2135458873963dc7c930b4bcef0c508c7d9635f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992829"
---
# <a name="set-up-lease-approval-workflows"></a>إعداد سير عمل الموافقة على الإيجار

[!include [banner](../includes/banner.md)]

يوضح الموضوع كيفية إعداد سير عمل معتمدة سيتم تشغيله عند إنشاء عقد إيجار جديد. للحصول على معلومات حول كيفية استخدام سير العمل، راجع [استخدام عمليات سير عمل معتمدة لعقد الإيجار](use-create-lease-wrkflw.md). 

1. انتقل إلى **تأجير الأصول \> الضبط \> سير عمل عقود الإيجار**.
2. في صفحة **سير عمل عقد الإيجار‬**، حدد **جديد**.
3. في مربع الحوار الذي يظهر، ضمن **نوع سير العمل**، حدد الارتباط **سير عمل الإيجار**.

    يتم فتح استمارة التقديم. بعد تشغيله، قم بتسجيل الدخول إلى Azure Active Directory (Azure AD) ليتم إعادة التوجيه إلى استمارة تقديم سير العمل.

4. اسحب العنصر **اعتماد سير عمل عقد الإيجار** إلى سير العمل.
5. قم بتوصيل عقدة واحدة من **البدء** إلى **اعتماد سير عمل عقد الإيجار**. قم بتوصيل **اعتماد سير عمل عقد الإيجار** إلى **النهاية**.
6. انقر نقرًا مزدوجًا فوق **اعتماد سير عمل عقد الإيجار**.
7. حدد **الخصائص**، ثم، ضمن **إعدادات الأساسية**، أدخل اسمًا لسير العمل.

    في هذه الصفحة، يمكنك أيضًا تعيين المزيد من المعلمات لسير العمل. إذا قمت بتشغيل **الإجراءات التلقائية**، سيقوم النظام تلقائيًا بتنفيذ إجراء معين. يمكن إرسال الإخطارات إذا تم تحديدها في علامة التبويب **الإخطارات**. في علامة التبويب **إعدادات متقدمة**، ويمكنك تحديد معتمد نهائي وتعيين حد زمني وتعيين إجراءات معينة يجب إكمالها.

8. عند الانتهاء من إعداد معلمات سير العمل، حدد **إغلاق**.
9. حدد **الخطوة 1**، ثم حدد **الخصائص**.
10. ضمن **الإعدادات الأساسية**، أدخل اسمًا للخطوة، وقم بإنشاء بند موضوع للاعتماد، وحدد الإرشادات الخاصة بالاعتماد.
11. في الصفحة **مهمة**، حدد نوع المهمة.
12. لتعيين مستخدمين محددين للاعتماد، حدد **مستخدم**، ثم حدد المستخدمين الذين يوافقوا على عقود الإيجار، ثم حدد **إغلاق**.
13. حدد **حفظ وإغلاق** لإنشاء سير العمل. ثم، عند المطالبة، حدد **موافق**.
14. في صفحة **إنشاء سير عمل‬**، حدد **إغلاق**.
14. حدد سير العمل الجديد، ثم حدد **إصدارات**. ثم حدد **تنشيط** لضمان أن سير العمل نشطًا.
15. حدد **إغلاق**. يظهر الإصدار النشط الجديد.