---
title: تمكين مقترحات الموازنة (معاينة)
description: يوضح هذا الموضوع كيفية تشغيل ميزة مقترح الموازنة في Finance Insights.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: d3fac4cbb80493c7cf94e3d9f4a4f544a749fb64
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638599"
---
# <a name="enable-budget-proposals-preview"></a>تمكين مقترحات الموازنة (معاينة)

[!include [banner](../includes/banner.md)]

يوضح هذا الموضوع كيفية تشغيل ميزة مقترح الموازنة في Finance Insights.

1. استخدم المعلومات من صفحة البيئة في Microsoft Dynamics Lifecycle Services (LCS) للاتصال بالمثيل الأساسي لـ Azure SQL لتلك البيئة. قم بتشغيل الأمر Transact-SQL (T-SQL) لتشغيل إصدارات التقييم لبيئة وضع الحماية. (قد تضطر إلى تشغيل الوصول إلى عنوان IP الخاص بك في LCS قبل أن تتمكن من الاتصال بخادم كائن التطبيق عن بُعد \[AOS\].)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > تجاوز هذه الخطوة إذا كنت تستخدم الإصدار 10.0.20 أو أحدث، أو إذا كنت تستخدم عملية نشر Service Fabric. يجب أن يكون فريق Finance insights قد قام بالفعل بتشغيل إصدار التقييم. إذا لم تر الميزة في مساحة عمل **إدارة الميزات**، أو إذا واجهتك مشكلات عند محاولة تشغيلها، تواصل على <fiap@microsoft.com>

2. افتح مساحة العمل **إدارة الميزات**، واتبع الخطوات التالية:

    1. حدد **التحقق من وجود تحديثات**.
    2. ابحث عن **مقترح الموازنة** وقم بتشغيل تلك الميزة.

3. انتقل إلى **إعداد الموازنة \> الإعداد \> إعداد الموازنة الأساسية \> مقترح الموازنة (معاينة)**، وحدد **تمكين الميزة**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
