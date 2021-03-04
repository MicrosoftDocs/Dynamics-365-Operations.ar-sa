---
title: توفر المخزون في الكتابة المزدوجة
description: يوفر هذا الموضوع معلومات حول فحص توفر المخزون في الكتابة المزدوجة.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 4d1022eec633bf0a9edb4d5b26982853cec836d7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4449363"
---
# <a name="inventory-availability-in-dual-write"></a>توفر المخزون في الكتابة المزدوجة

[!include [banner](../../includes/banner.md)]

باستخدام توفر المخزون، يمكنك فحص المخزون قبل إضافة منتج إلى صفحة **عروض الأسعار** أو **الأوامر** أو **الفواتير** في Microsoft Dynamics 365 Sales. على سبيل المثال، يمكنك فحص المخزون وتحديد تاريخ التنفيذ كمهمة أساسية في عملية [العميل المتوقع إلى النقدية](dual-write-prospect-to-cash.md).

إذا لم يكن لديك مخزون كافٍ، فيمكنك تقدير تاريخ التسليم استنادًا إلى عمليات استلام المخزون المتوقعة ومشاكلها. يمكنك أيضًا التحقق من معلومات "متوفر حسب التعهد‬" للمنتج، حيث يمكنك العثور على كمية ATP في الحد الزمني المحدد مسبقًا.

## <a name="on-hand-inventory"></a>المخزون الفعلي

في رأس صفحات **عروض الأسعار** أو **الأوامر** أو **الفواتير** في Dynamics 365 Sales، تمت إضافة زر جديد **المخزون الفعلي**. عند النقر فوق الزر، يظهر مربع حوار ويمكنك تحديد الشركة والمنتج الذي تريد فحص مخزونه الفعلي. يظهر مربع الحوار هذا نفس المعلومات كـ [مخزون فعلي](../../../../supply-chain/inventory/tasks/check-availability-stock.md).

يقوم مربع الحوار بإرجاع معلومات المخزون من Dynamics 365 Supply Chain Management. تشمل هذه المعلومات الكميات التالية:

- الكمية المتاحة
- الكمية المحجوزة
- الكمية الفعلية المتوفرة
- الكمية المطلوبة
- الكمية تحت الطلب
- الكمية المطلوبة المحجوزة
- إجمالي الكمية المتوفرة

## <a name="atp-information"></a>معلومات ATP

في Sales، تمت إضافة زر **معلومات ATP** جديد إلى أصناف البند في صفحة **عروض الأسعار** و **الأوامر** و **الفواتير**. عند تحديد هذا الزر، يظهر مربع حوار ويمكنك تحديد الشركة والمنتج وموقع المخزون ومستودع المخزون وكمية الأمر. لمربع الحوار هذا نفس الإعدادات الموضحة في [‏‫التعهد بالأمر‬](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).

يقوم مربع الحوار بإرجاع معلومات ATP من Supply Chain Management. تشمل هذه المعلومات الكميات التالية:

- كمية ATP
- كمية الإيصال
- كمية الإصدار
- الكمية المتاحة


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]