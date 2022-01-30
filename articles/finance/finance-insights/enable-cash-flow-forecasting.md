---
title: تمكين تقدير التدفق النقدي
description: يوضح هذا الموضوع كيفية تشغيل ميزة توقعات التدفق النقدي في Finance Insights.
author: ShivamPandey-msft
ms.date: 11/03/2021
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
ms.openlocfilehash: cfcdbe76d640d1786b4622febf9157f5fb1c42f9
ms.sourcegitcommit: 133aa728b8a795eaeaef22544f76478da2bd1df9
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/13/2022
ms.locfileid: "7969127"
---
# <a name="enable-cash-flow-forecasting"></a>تمكين تقدير التدفق النقدي

[!include [banner](../includes/banner.md)]

يوضح هذا الموضوع كيفية تشغيل ميزة توقعات التدفق النقدي في Finance Insights.

> [!NOTE]
> لاستخدام تنبؤات الدفع في التدفق النقدي، فإنه يجب إعداد ميزة تنبؤات الدفع الخاصة بالعميل كما هو موضح في [تمكين تنبؤات مدفوعات العميل](enable-cust-paymnt-prediction.md).
  
1. افتح مساحة العمل **إدارة الميزات**، واتبع الخطوات التالية:

    1. حدد **التحقق من وجود تحديثات**.
    2. في علامة التبويب **الكل**، ابحث عن **التنبؤات بالتدفقات النقدية**. إذا لم تجد الميزة، فابحث عن **(الإصدار الأولي) التنبؤات بالتدفقات النقدية**. 
    3. قم بتشغيل الميزة.

2. انتقل إلى **إدارة النقد والبنوك \> إعداد التنبؤ بالتدفقات النقدية**، وأضف حسابات السيولة التي يجب تضمينها في التوقعات. قم أيضًا بإعداد حساب السيولة للدفعات في علامتي التبويب **الحسابات المدينة** و **الحسابات الدائنة**. تأكد من إعادة حساب التنبؤ بالتدفقات النقدية.

    > [!NOTE]
    > في حالة عدم إعداد حسابات السيولة، لا يمكن إنشاء التدفق النقدي.
    >
    > لمزيد من المعلومات حول كيفية إعداد تنبؤات التدفق النقدي، راجع [التنبؤ بالتدفق النقدي](../cash-bank-management/cash-flow-forecasting.md).

3. انتقل إلى **إدارة النقد والبنوك \> الإعداد \> Finance Insights (معاينة) \> تقديرات التدفقات المالية (معاينة)**، واتبع هذه الخطوات:

    1. في علامة التبويب **تقدير التدفقات النقدية**، حدد **تمكين الميزة**.
    2. حدد **إنشاء نموذج توقع**.

لمزيد من المعلومات حول قدرة تقدير التدفقات النقدية، راجع [تقدير التدفقات النقدية](cash-flow-forecast-intro.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
