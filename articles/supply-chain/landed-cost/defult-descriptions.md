---
title: الأوصاف الافتراضية لدفتر الأستاذ العام
description: يمكن استخدام الأوصاف الافتراضية لتحديث حقل الوصف في ترحيلات الإيصالات إلى دفتر الأستاذ العام.
author: sherry-zheng
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TransactionTexts
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 47c5c9e71dba7a0cb7c798c167208faebeb5af6c
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500370"
---
# <a name="default-descriptions-for-the-general-ledger"></a>الأوصاف الافتراضية لدفتر الأستاذ العام

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

يمكن استخدام الأوصاف الافتراضية لتحديث حقل **الوصف** في ترحيلات الإيصالات إلى دفتر الأستاذ العام. تم تحسين هذه الوظيفة للعمل مع التكلفة شاملة التفريغ.

لإعداد الأوصاف الافتراضية لترحيلات دفتر الأستاذ، انتقل إلى **الإدارة التنظيمية \> الإعداد \> الأوصاف الافتراضية**.

يسرد الجدول التالي القيم الجديدة التي تمت إضافتها للحقل **الوصف** في صفحة **الأوصاف الافتراضية** لدعم التكلفة شاملة التفريغ.

| نوع الوصف | الملاحظات |
|---|---|
| تكاليف الاستيراد - استحقاق التكلفة | عند ترحيل فاتورة أمر شراء، تتم معالجة استحقاق التكلفة لتقدير تكاليف الرحلة. يمكن تحديد الأوصاف الافتراضية لإضافة رقم الرحلة إلى الوصف. استخدم *%4* لرقم الشحنة. |
| تكاليف الاستيراد - أمر بضاعة بالطريق | إذا كنت تستخدم معالجة الإرسال النقل، سيتم ترحيل فاتورة أمر الشراء، وترحيل البضائع إلى بضائع في حساب البضاعة بالطريق. يمكن تحديد الأوصاف الافتراضية لإضافة رقم أمر النقل إلى الوصف. تستخدم *%4* لرقم أمر النقل. |
| المخزون - إقفال - تسوية | عند معالجة فاتورة الحسابات الدائنة (AP) لتكلفه الرحلة، تتم معالجة تسوية المخزون لتقدير تكاليف الرحلة. يمكن تحديد الأوصاف الافتراضية لإضافة رقم الرحلة إلى الوصف. استخدم *%4* لرقم الشحنة. |

لمزيد من المعلومات حول كيفيه العمل مع صفحة **‏‫الأوصاف الافتراضية** ، راجع [اعداد الأوصاف الافتراضية للترحيل التلقائي](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).
