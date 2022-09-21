---
title: معلمات Sensor Data Intelligence
description: يقدم هذا المقال معلومات حول إعدادات التكوين المتوفرة في صفحه معلمات Sensor Data Intelligence.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreServiceParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 4a6665cc078e54da4ebb7920ec8826352ab7a816
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428275"
---
# <a name="sensor-data-intelligence-parameters"></a>معلمات Sensor Data Intelligence

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

توفر صفحه **معلمات Sensor Data Intelligence** إعدادات قليله يمكنك استخدامها لتكوين الميزة. تتضمن هذه الإعدادات معلمات اتصال Azure ومعلمة لمده بقاء رسائل التنبيه التي يتم إرسالها إلى المستخدمين استجابة لقياسات أداة الاستشعار.

## <a name="read-and-change-connection-details-for-your-azure-iot-solution"></a>قراءه تفاصيل الاتصال الخاصة بحل Azure IoT الخاص بك وتغييرها

بشكل عام، ستقوم باعداد حل Azure IoT الخاص بك وتوصيله بشركة Microsoft Dynamics 365 Supply Chain Management من صفحة **‎‏‫نشر موارد Azure والاتصال بها** التي سترشدك خلال كلا الإجراءين. (لمزيد من المعلومات ، راجع [‎نشر حل IoT علي Azure](sdi-deploy-iot-solution-on-azure.md).) يمكنك أيضا عرض تفاصيل الاتصال وتحريرها في اي وقت في Supply Chain Management بإتباع الخطوات التالية.

1. الانتقال إلى **إعداد \> إدارة النظام \> Sensor Data Intelligence \> Sensor Data Intelligenceمعلمات**.
1. من علامة **التبويب التسلسل الزمني** ، في حقل **‏‫سلسلة اتصال مخزن Redis القياسي‬** ، أدخل قيمه **سلسله الاتصال الاساسية (StackExchange.Redis)** لحل Azure IoT الذي تريد الاتصال به. لمزيد من المعلومات حول كيفيه العثور علي هذه القيمة [‎نشر حل IoT علي Azure](sdi-deploy-iot-solution-on-azure.md).
1. في علامة التبويب **تكامل** في حقل **Azure AD معرف تطبيق العميل** أدخل قيمة **معرف العميل** لحل Azure IoT الذي ترغب في الاتصال به. لمزيد من المعلومات حول كيفيه العثور علي هذه القيمة [‎نشر حل IoT علي Azure](sdi-deploy-iot-solution-on-azure.md).

## <a name="set-the-lifetime-of-alert-messages"></a>تعيين عمر رسائل التنبيه

وفي كل مره تقوم فيها أداه الاستشعار بكشف المعلومات عن حاله تتطلب إخطار المستخدم، فإنها ترسل إخطارًا إلى المستخدم ذي الصلة. لمنع هذه الإخطارات من الظهور في النظام، يجب تعيينها علي ان تنتهي صلاحيتها بعد عده أيام.

1. الانتقال إلى **إعداد \> إدارة النظام \> Sensor Data Intelligence \> Sensor Data Intelligenceمعلمات**.
1. في علامة التبويب **الإخطارات** ، في حقل **‏‫أيام الإخطار للعرض المباشر** ، ادخل عدد الأيام للاحتفاظ بالإخطار. وبعد مرور الفترة المحددة، سيتم حذف الإخطار.
