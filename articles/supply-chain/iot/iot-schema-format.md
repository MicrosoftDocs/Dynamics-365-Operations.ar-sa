---
title: تنسيقات مخطط الرسائل لمركز IoT
description: يشرح هذا الموضوع كيفيه تصميم مخطط رسائل يمكنك استخدامه في ذكاء IoT.
author: tonyafehr
ms.date: 04/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.custom: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b24a6e14182baa91299abad0da2987b2dca92601
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781582"
---
# <a name="schema-formats-for-iot-hub-messages"></a>تنسيقات مخطط الرسائل لمركز IoT

[!include [banner](../../includes/banner.md)]

يشرح هذا الموضوع كيفيه تصميم مخطط رسائل يمكنك استخدامه في ذكاء IoT.

## <a name="message-requirements"></a>متطلبات الرسالة

تنطبق القواعد التالية علي مراقبه الرسائل في ذكاء IoT:

+ يجب ان تكون مخططات الرسائل بتنسيق منهج كائن JavaScript (JSON).
+ يجب أن تكون خاصية **الطابع الزمني** UNIX، حيث يتم التعبير عن القيمة بالمللي ثانية، موجودة في رسالة مركز Microsoft Azure IoT.
+ يتم تعقب الرسالة فقط إذا كانت تحتوي علي كافة الخصائص التي تم تعريفها في اعداد السيناريو. علي سبيل المثال ، إذا قمت بتعريف خصائص **المعرف** و **الطابع الزمني** و **القيمة** ، يتم مراقبه الرسالة التالية.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True
    }
    ```

    هذه الرسالة غير مراقبه ، لان الخاصية **القيمة** مفقوده.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
    }
    ```

+ ويتجاهل ذكاء IoT الخصائص في الرسالة التي لم يتم تعريفها في تكوين السيناريو. علي سبيل المثال ، إذا قمت بتعريف خصائص **المعرف** و **الطابع الزمني** و **القيمة** ، يراقب ذكاء IoT الرسائل التالية.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True
    },
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True,
        "machine" : "Machine1225",
    },
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True,
         "activity": "PartOut"
    },
    ```

+ يقوم ذكاء IoT بهدوء بتجاهل الرسائل التي لا تتطابق مع معايير تكوين السيناريو.
+ يمكنك تعريف أنواع متعددة من مخططات الرسائل واستخدامها.
+ لا يجب تحديد كل نوع من مخططات الرسائل. يجب تحديد المخططات التي سيتم استخدامها لسيناريوهات ذكاء IoT فقط.

## <a name="id-value-pair-schema"></a>مخطط ازدواج قيمه المعرف

ويعتبر زوج قيمه المعرف نمطا عاما لمخططات رسائل ذكاء IoT. وباستخدام زوج من قيمه المعرف ، فانك بذلك تضمن ان يكون مخطط الرسالة هو نفسه عبر كافة وحدات السيناريو. علي سبيل المثال ، فيما يلي رسالة لسيناريو **تعطل المعدات** أو **تاخير الإنتاج**.

```json
{
    "id": "IoTInt.Machine1225.PartOut",
    "timestamp": 1576016821614,
    "value": True
}
```

فيما يلي رسالة لسيناريو **جوده المنتج**.

```json
{
    "id": "IoTInt.Machine1225.Temperature",
    "timestamp": 1576016821614,
    "value": 105
}
```

تحتوي كلتا الرسائل السابقة علي خصائص **المعرف** و **القيمة**. يمكن تعيين قيم **المعرف** في جدول **قيم بيانات الإشارات** اثناء اعداد السيناريو. بالنسبة لسيناريو **تعطل المعدات** ، ستقوم بتعيين القيمة **IoTInt.Machine1225.PartOut**. بالنسبة لسيناريو **جودة المنتج** ، ستقوم بتعيين القيمة **IoTInt.Machine1225.Temperature**.

لمزيد من المعلومات، راجع [وثائق مركز Azure IoT](/azure/iot-hub/).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]