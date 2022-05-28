---
title: استخدام أكواد السبب
description: يمكنك استخدام كود سبب لتوضيح سبب إلغاء اتفاقية مستوى الخدمة (SLA)، أو سبب تجاوز أمر خدمة لحدود الوقت التي قمت بتحديدها في SLA.
author: sorenva
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
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 06c2b6a2b338dbfdbecdeb75e12fa1c20af8e56d
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/03/2022
ms.locfileid: "8669505"
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