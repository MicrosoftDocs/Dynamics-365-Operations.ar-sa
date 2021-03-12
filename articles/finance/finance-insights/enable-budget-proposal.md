---
title: تمكين مقترحات الموازنة (معاينة)
description: يوضح هذا الموضوع كيفية تشغيل ميزة مقترح الموازنة في Finance Insights.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 59cf40e8bf69734c5f3645997ff0b07c29d4f40e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995130"
---
# <a name="enable-budget-proposals-preview"></a>تمكين مقترحات الموازنة (معاينة)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

يوضح هذا الموضوع كيفية تشغيل ميزة مقترح الموازنة في Finance Insights.

1. استخدم المعلومات من صفحة البيئة في Microsoft Dynamics Lifecycle Services (LCS) للاتصال بالمثيل الأساسي لـ Azure SQL لتلك البيئة. قم بتشغيل الأمر Transact-SQL (T-SQL) لتشغيل إصدارات التقييم لبيئة وضع الحماية. (قد تضطر إلى تشغيل الوصول إلى عنوان IP الخاص بك في LCS قبل أن تتمكن من الاتصال بخادم كائن التطبيق عن بُعد \[AOS\].)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > إذا كان نشر Microsoft Dynamics 365 Finance عبارة عن نشر Service Fabric، فإنه يمكنك تخطي هذه الخطوة. يجب أن يكون فريق Finance Insights قد قام بالفعل بتشغيل إصدار التقييم. في حالة عدم رؤية الميزة في مساحة العمل **إدارة الميزات** أو في حالة مواجهة مشكلات عند محاولة تشغيلها، قم بإرسال بريد إلكتروني إلى [فريق معاينه تطبيق Finance Insights](mailto:fiap@microsoft.com).

2. افتح مساحة العمل **إدارة الميزات**، واتبع الخطوات التالية:

    1. حدد **التحقق من وجود تحديثات**.
    2. ابحث عن **مقترح الموازنة** وقم بتشغيل تلك الميزة.

3. انتقل إلى **إعداد الموازنة \> الإعداد \> إعداد الموازنة الأساسية \> مقترح الموازنة (معاينة)**، وحدد **تمكين الميزة**.

#### <a name="privacy-notice"></a>إشعار الخصوصية
إن المعاينات (1) قد تستخدم تدابير أقل تتعلق بالخصوصية وإجراءات الأمان مقارنةً بخدمة Dynamics 365 Finance and Operations‏، و(2) لا يتم تضمينها في اتفاقية مستوى الخدمة (SLA) لهذه الخدمة، و(3) يجب ألا يتم استخدامها لمعالجة البيانات الشخصية أو البيانات الأخرى التي تخضع لمتطلبات التوافق القانونية أو التنظيمية، و(4) هي ذات دعم محدود.
