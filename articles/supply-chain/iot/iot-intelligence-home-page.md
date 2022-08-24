---
title: الصفحة الرئيسية لذكاء IoT
description: يوفر هذا المقال ارتباطات إلى معلومات حول ذكاء IoT.
author: johanhoffmann
ms.date: 08/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0d8b2be25abaeff7404d7f4ef3cd825a50147fef
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228346"
---
# <a name="iot-intelligence-home-page"></a>الصفحة الرئيسية لذكاء IoT

[!include [banner](../../includes/banner.md)]
[!INCLUDE [iot-sdi-announcement](../../includes/iot-sdi-announcement.md)]

> [!IMPORTANT]
> تتوفر هذه الميزة في الوقت الحالي فقط في البلدان/المناطق التالية:
>
> - الولايات المتحدة (الولايات المتحدة الامريكيه)
> - اتحاد أوروبي (EU)
> - أستراليا (AU)
> - كندا (CA)
> - المملكة المتحدة (UK)

ذكاء IoT هو وظيفة اضافيه ل Microsoft Dynamics 365 Supply Chain Management. وهو يقوم بدمج إشارات إنترنت الأشياء (IoT) مع البيانات الموجودة في Supply Chain Management لإنتاج رؤى قابله للتنفيذ.

يدعم ذكاء IoT السيناريوهات التالية:

- **عمليات تاخير الإنتاج** - يقارن هذا السيناريو زمن الدورة الفعلي مع وقت الدورة المخطط. تقوم Supply Chain Management باعلامك عندما لا يكون الإنتاج في الجدول الزمني ، بحيث يمكنك التدخل لزيادة كفاءه التشغيل وتجنب تاخير الأمر.
- **وقت التوقف للمعدات** – يقارن هذا السيناريو بين وقت الجهاز والمحددات المحددة بواسطة المستخدم. تقوم Supply Chain Management باعلامك عند تجاوز حد قطع العمل ، بحيث يمكنك القيام بإجراءات مثل أعاده جدوله أمر الإنتاج أو إنشاء أمر عمل الصيانة.
- **جوده المنتج** – يقارن هذا السيناريو قراءات الاستشعار ، مثل الرطوبة ودرجات الحرارة ، لمقاييس الجودة المحددة من قبل المستخدم. تقوم Supply Chain Management باعلامك عند حدوث انحراف ، بحيث يمكنك التدخل للحفاظ علي معايير الجودة وتقليل المهدورات.

يبين الرسم التوضيحي التالي تفاعل مركز Azure IoT وذكاء IoT وSupply Chain Management.

![مركز IoT وذكاء IoT وSupply Chain Management.](media/iot_intelligence.png)

<!-- KFM: hide setup info for now

## Setup

You can set up and configure IoT Intelligence without writing any code. Here are the basic steps.

1. [Set up Azure resources](iot-azure-setup.md) – Create an IoT hub, a Redis cache, and a key vault that can be accessed from Supply Chain Management.
2. [Message schema formats for IoT Hub](iot-schema-format.md) – Configure your devices to send messages to IoT Hub, and define the JavaScript Object Notation (JSON) message format.
3. In Feature Management, enable the IoT Intelligence feature flag. 
4. [Install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md) – Install the add-in in LCS, and configure the Azure secrets.
5. [Set up metrics](iot-metrics-setup.md) – Set up metrics in Supply Chain Management.
6. [Scenario setup](iot-scenario-setup.md) – Set up the scenarios in Supply Chain Management.

-->

## <a name="tracking-and-maintenance"></a>التتبع والصيانة

- [مراقبة السيناريوهات في Dynamics 365 Supply Chain Management](iot-management.md#monitor-scenarios)
- [تعطيل سيناريو](iot-scenario-setup.md#disable-a-scenario)
- [تعديل سيناريو ذكاء IoT قيد التشغيل](iot-management.md#modify-a-running-iot-intelligence-scenario)
- [خيارات المحاكاة](iot-management.md#simulation-options)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]