---
title: مراقبة وإدارة ذكاء IoT
description: يوضح هذا المقال كيفية مراقبة وإدارة ذكاء IoT.
author: johanhoffmann
ms.date: 08/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f1804e8b9cfa407f6549dc146df17338c4d51572
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228848"
---
# <a name="monitor-and-manage-iot-intelligence"></a>مراقبة وإدارة ذكاء IoT

[!include [banner](../../includes/banner.md)]
[!INCLUDE [iot-sdi-announcement](../../includes/iot-sdi-announcement.md)]

يوضح هذا المقال كيفية مراقبة وإدارة ذكاء IoT.

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a>مراقبة السيناريوهات في Microsoft Dynamics 365 Supply Chain Management

يمكنك مراقبة معالجة ذكاء IoT من عدة أماكن:

+ **الوحدات \> التحكم في الإنتاج \> الاستفسارات والتقارير \> ذكاء IoT \> الإخطارات** – عرض قائمة بالإخطارات التي لم يتم حلها.
+ **الوحدات \> التحكم في الإنتاج \> الاستفسارات والتقارير \> ذكاء IoT \> الإخطارات المغلقة** – عرض قائمة بالإخطارات التي يتم حلها أو تجاهلها.
+ **الوحدات \> التحكم في الإنتاج \> الاستعلامات والتقارير \> ذكاء IoT \> المفاتيح القياسية** – عرض المفاتيح القياسية لجداول السلاسل الزمنية لـ **حالة المورد**.
+ **الوحدات \> التحكم في الإنتاج \> تنفيذ التصنيع \> حالة المورد** – تتبع مقاييس خاصة باستخدام مربع حوار **التكوين**. في حالة اكتشاف أحد السيناريوهات لاستثناء، يتم عرض إخطار يوضع تفاصيل الاستثناء.
+ **مساحات العمل \> إدارة طابق الإنتاج \> الإخطارات** – عرض قائمة بالإخطارات التي لم يتم حلها.

## <a name="modify-a-running-iot-intelligence-scenario"></a>تعديل سيناريو ذكاء IoT قيد التشغيل

عندما يكون السيناريو قيد التشغيل، يمكنك إجراء هذه التغييرات:

+ إضافة تعريفات جديدة لمخطط المستشعرات.
+ تحديد حدد قيم بيانات إشارة جديدة.
+ إلغاء تحديد قيم بيانات الإشارة الموجودة.
+ إضافة قيم بيانات إشارة جديدة وتعيينها.
+ تحديث قيم الحد.

عندما يكون السيناريو قيد التشغيل، يحظر إجراء هذه التغييرات:

+ حذف أو تعديل أي تعريفات للمخططات التي يتم استهلاكها حاليًا بواسطة سيناريو ممكن.
+ تغيير مسارات المخططات المحددة الخاصة بالسيناريو الممكن.

## <a name="simulation-options"></a>خيارات المحاكاة

يمكنك محاكاة إشارات جهاز المصنع. لمزيد من المعلومات، راجع هذه المقالات:

+ [توصيل IoT DevKit AZ3166 بمركز Azure IoT](/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [توصيل وحدة محاكاة Raspberry Pi على الإنترنت بمركز Azure IoT (Node.js)](/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
