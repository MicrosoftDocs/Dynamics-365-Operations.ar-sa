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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: dd0995eb8c70ed06cdc3c0f6a28b13b117297533
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426972"
---
# <a name="inventory-availability"></a>توفر المخزون

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

باستخدام توفر المخزون، يمكنك فحص المخزون قبل إضافة منتج إلى نماذج **عروض الأسعار** أو **الأوامر** أو **الفواتير** في التطبيقات المستندة إلى نموذج في Dynamics 365. على سبيل المثال، يعتبر فحص المخزون وتحديد تاريخ التنفيذ مهمة أساسية في عملية [العميل المتوقع إلى النقدية](dual-write-prospect-to-cash.md). إذا لم يكن لديك مخزون كافٍ، فيمكنك تقدير تاريخ التسليم استنادًا إلى عمليات استلام المخزون المتوقعة ومشاكلها. يمكنك أيضًا التحقق من معلومات "متوفر حسب التعهد‬" للمنتج، حيث يمكنك العثور على كمية ATP في الحد الزمني المحدد مسبقًا.

## <a name="on-hand-inventory"></a>المخزون الفعلي 

في رأس نماذج **عروض الأسعار** أو **الأوامر** أو **الفواتير** في Dynamics 365 Sales، تمت إضافة زر جديد **المخزون الفعلي**. عند النقر فوق الزر، يظهر مربع حوار ويمكنك تحديد الشركة والمنتج الذي تريد فحص مخزونه الفعلي. إنه يُرجع معلومات المخزون من Dynamics 365 Supply Chain Management، ويعرض المعلومات نفسها كما في [المخزون الفعلي](../../../../supply-chain/inventory/tasks/check-availability-stock.md). وتتضمن المعلومات الكميات التالية:

- **الكمية الفعلية**
- **الكمية المحجوزة**
- **الكمية الفعلية المتوفرة**
- **الكمية المطلوبة**
- **الكمية تحت الطلب**
- **الكمية المطلوبة المحجوزة**
- **إجمالي الكمية المتوفرة**

## <a name="atp-information"></a>معلومات ATP

في عناصر بنود **عروض الأسعار** أو **الأوامر** أو **الفواتير** في Dynamics 365 Sales، تمت إضافة زر جديد **معلومات ATP**. عند النقر فوق الزر، يظهر مربع حوار ويمكنك تحديد الشركة والمنتج وموقع المخزون ومستودع المخزون وكمية الأمر. وهو يُرجع **معلومات ATP** من Supply Chain Management ويعرض الإعدادات التي ورد وصفها في [التعهد بالأمر‬](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations). تتضمن المعلومات **كمية ATP** و**كمية الإيصال** و**كمية الإصدار** و**الكمية الفعلية**.
