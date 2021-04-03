---
title: مراقبة وإدارة ذكاء IoT
description: يوضح هذا الموضوع كيفية مراقبة وإدارة ذكاء IoT.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8a037cb31e297926b1bcb66bff91bdd7eb5c40b7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264838"
---
# <a name="monitor-and-manage-iot-intelligence"></a>مراقبة وإدارة ذكاء IoT

[!include [banner](../../includes/banner.md)]

يوضح هذا الموضوع كيفية مراقبة وإدارة ذكاء IoT.

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

يمكنك محاكاة إشارات جهاز المصنع. لمزيد من المعلومات، راجع هذه الموضوعات:

+ [توصيل IoT DevKit AZ3166 بمركز Azure IoT](https://docs.microsoft.com/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [توصيل وحدة محاكاة Raspberry Pi على الإنترنت بمركز Azure IoT (Node.js)](https://docs.microsoft.com/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)
+ [نظرة عامة حول مسرع حل محاكاة الأجهزة](https://docs.microsoft.com/azure/iot-accelerators/iot-accelerators-device-simulation-overview)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]