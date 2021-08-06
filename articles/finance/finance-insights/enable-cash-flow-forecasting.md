---
title: تمكين تقدير التدفق النقدي (معاينة)
description: يوضح هذا الموضوع كيفية تشغيل ميزة توقعات التدفق النقدي في Finance Insights.
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
ms.openlocfilehash: 29118557a1de4d3521f8125395b26471f7f48f3e
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638598"
---
# <a name="enable-cash-flow-forecasting-preview"></a>تمكين تقدير التدفق النقدي (معاينة)

[!include [banner](../includes/banner.md)]

يوضح هذا الموضوع كيفية تشغيل ميزة توقعات التدفق النقدي في Finance Insights.

> [!NOTE]
> لاستخدام تنبؤات الدفع في التدفق النقدي، فإنه يجب إعداد ميزة تنبؤات الدفع الخاصة بالعميل كما هو موضح في [تمكين تنبؤات مدفوعات العميل](enable-cust-paymnt-prediction.md).

1. استخدم المعلومات من صفحة البيئة في Microsoft Dynamics Lifecycle Services (LCS) للاتصال بالمثيل الأساسي لـ Azure SQL لتلك البيئة. قم بتشغيل الأمر Transact-SQL (T-SQL) لتشغيل إصدارات التقييم لبيئة وضع الحماية. (قد تضطر إلى تشغيل الوصول إلى عنوان IP الخاص بك في LCS قبل أن تتمكن من الاتصال بخادم كائن التطبيق عن بُعد \[AOS\].)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > تجاوز هذه الخطوة إذا كنت تستخدم الإصدار 10.0.20 أو أحدث، أو إذا كنت تستخدم عملية نشر Service Fabric. يجب أن يكون فريق Finance insights قد قام بالفعل بتشغيل إصدار التقييم. إذا لم تر الميزة في مساحة عمل **إدارة الميزات**، أو إذا واجهتك مشكلات عند محاولة تشغيلها، تواصل على <fiap@microsoft.com>
  
2. افتح مساحة العمل **إدارة الميزات**، واتبع الخطوات التالية:

    1. حدد **التحقق من وجود تحديثات**.
    2. تشغيل الميزات التالية:

        - عنصر تحكم شبكة جديد
        - تجميع في الشبكات (معاينة) 
        - تنبؤات دفع العميل (معاينة)
        - تنبؤات التدفقات النقدية (معاينة)

3. انتقل إلى **إدارة النقد والبنوك \> إعداد التنبؤ بالتدفقات النقدية**، وأضف حسابات السيولة التي يجب تضمينها في التوقعات.

    > [!NOTE]
    > في حالة عدم إعداد حسابات السيولة، لا يمكن إنشاء التدفق النقدي.

4. انتقل إلى **إدارة النقد والبنوك \> الإعداد \> Finance Insights (معاينة) \> تقديرات التدفقات المالية (معاينة)**، واتبع هذه الخطوات:

    1. في علامة التبويب **تقدير التدفقات النقدية**، حدد **تمكين الميزة**.
    2. حدد **إنشاء نموذج توقع**.

لمزيد من المعلومات حول قدرة تقدير التدفقات النقدية، راجع [تقدير التدفقات النقدية](cash-flow-forecast-intro.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
