---
title: استخدام أكواد السبب
description: يمكنك استخدام كود سبب لتوضيح سبب إلغاء اتفاقية مستوى الخدمة (SLA)، أو سبب تجاوز أمر خدمة لحدود الوقت التي قمت بتحديدها في SLA.
author: ShylaThompson
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c2e823a2e015c4bf22da8eff94e2bc85c813c03b5bb744aa4ce52c95dcaff898
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6753831"
---
# <a name="use-stage-reason-codes"></a>استخدام أكواد السبب 

[!include [banner](../includes/banner.md)]


يمكنك استخدام كود سبب لتوضيح سبب إلغاء اتفاقية مستوى الخدمة (SLA)، أو سبب تجاوز أمر خدمة لحدود الوقت التي قمت بتحديدها في SLA.

ويمكنك أيضًا تحديد أن أحد أكواد السبب مطلوب عند إلغاء SLA، أو عندما يتجاوز حد الوقت المدة المحددة في SLA لأمر الخدمة.

إذا قمت بتحديد أن أحد أكواد السبب مطلوب، فيجب عليك إدخال كود سبب في المواقف التالية:

  - عندما يتم نقل أمر خدمة إلى مرحلة تقوم بإيقاف تسجيل الوقت في مقابل SLA لأمر الخدمة.

  - وقت اعتماد أمر الخدمة.

  - عندما يتم إيقاف تسجيل الوقت يدويًا.

## <a name="set-up-reason-codes"></a>إعداد أكواد السبب

1.  انقر فوق **إدارة الخدمة** \> **الإعداد** \> **أوامر الخدمة** \> **أكواد سبب المرحلة**.

2.  في النموذج **‏‫رموز السبب للمرحلة**، انقر فوق **جديد** لإنشاء رمز سبب جديد.

3.  في الحقل **‏‫رموز السبب للمرحلة**، أدخل رمز سبب فريد خاص بالمرحلة.

4.  في الحقل **الوصف**، أخل وصفًا لرمز السبب الخاص بالمرحلة.

5.  أغلق النموذج لحفظ التغييرات.

## <a name="require-reason-codes-when-a-service-level-agreement-is-canceled"></a>طلب أكواد سبب عند إلغاء اتفاقية مستوى الخدمة

1.  انقر فوق **إدارة الخدمة‬** \> **الإعداد** \> **محددات إدارة الخدمة**.

2.  في نموذج **محددات إدارة الخدمة** ، انقر فوق الارتباط **عام** ثم قم بتحديد خانة الاختيار **‏‫رمز سبب الإلغاء‬** .

## <a name="require-reason-codes-when-the-a-service-order-exceeds-the-time-limit-that-is-set-by-the-service-level-agreement"></a>تقديم أكواد السبب عندما يتجاوز أمر الخدمة حد الوقت المعين بواسطة اتفاقية مستوى الخدمة

1.  انقر فوق **إدارة الخدمة‬** \> **الإعداد** \> **محددات إدارة الخدمة**.

2.  في نموذج **محددات إدارة الخدمة** ، انقر فوق الارتباط **عام** ثم قم بتحديد خانة الاختيار **‏‫رمز سبب ‏‫تجاوز الوقت‬** .

## <a name="see-also"></a>راجع أيضًا

[تسجيل وقت البدء والتوقف على أمر خدمة](start-and-stop-time-recording-on-a-service-order.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]