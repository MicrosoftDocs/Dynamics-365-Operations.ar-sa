---
title: الصفحة الرئيسية لذكاء IoT
description: يوفر هذا الموضوع ارتباطات إلى معلومات حول ذكاء IoT.
author: tonyafehr
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.custom: intro-internal
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6b6c179052cdb9d1ca808d9cba089163bde0d5d5
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782671"
---
# <a name="iot-intelligence-home-page"></a>الصفحة الرئيسية لذكاء IoT

[!include [banner](../../includes/banner.md)]

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

+ **عمليات تاخير الإنتاج** - يقارن هذا السيناريو زمن الدورة الفعلي مع وقت الدورة المخطط. تقوم Supply Chain Management باعلامك عندما لا يكون الإنتاج في الجدول الزمني ، بحيث يمكنك التدخل لزيادة كفاءه التشغيل وتجنب تاخير الأمر.
+ **وقت التوقف للمعدات** – يقارن هذا السيناريو بين وقت الجهاز والمحددات المحددة بواسطة المستخدم. تقوم Supply Chain Management باعلامك عند تجاوز حد قطع العمل ، بحيث يمكنك القيام بإجراءات مثل أعاده جدوله أمر الإنتاج أو إنشاء أمر عمل الصيانة.
+ **جوده المنتج** – يقارن هذا السيناريو قراءات الاستشعار ، مثل الرطوبة ودرجات الحرارة ، لمقاييس الجودة المحددة من قبل المستخدم. تقوم Supply Chain Management باعلامك عند حدوث انحراف ، بحيث يمكنك التدخل للحفاظ علي معايير الجودة وتقليل المهدورات.

يبين الرسم التوضيحي التالي تفاعل مركز Azure IoT وذكاء IoT وSupply Chain Management.

![مركز IoT وذكاء IoT وSupply Chain Management.](media/iot_intelligence.png)

## <a name="setup"></a>الإعداد

يمكنك اعداد ذكاء IoT وتكوينه دون كتابه إيه تعليمه برمجيه. وهذه هي الخطوات الاساسيه.

1. [اعداد موارد Azure](iot-azure-setup.md) – إنشاء مركز IoT وذاكره تخزين مؤقت Redis ومخزن مفتاح يمكن الوصول اليه من Supply Chain Management.
2. [تنسيقات مخطط الرسائل لمركز IoT](iot-schema-format.md) – قم بتكوين أجهزتك لإرسال رسائل إلى مركز IoT، وتعريف تنسيق الرسالة منهج كائن JavaScript (JSON).
3. في أداره الميزات ، قم بتمكين علامة الخاصية ذكاء IoT. 
4. [قم بتثبيت الوظيفة الاضافيه لمركز IoT في Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md) – ثبت الوظيفة الاضافيه في LCS ، وقم بتكوين اسرار Azure.
5. [اعداد المقاييس](iot-metrics-setup.md) – اعداد المقاييس في Supply Chain Management.
6. [اعداد السيناريو](iot-scenario-setup.md) – قم باعداد السيناريوهات في Supply Chain Management.

## <a name="tracking-and-maintenance"></a>التتبع والصيانة

+ [مراقبة السيناريوهات في Dynamics 365 Supply Chain Management](iot-management.md#monitor-scenarios)
+ [تعطيل سيناريو](iot-scenario-setup.md#disable-a-scenario)
+ [إلغاء تثبيت الوظيفة الإضافية](iot-lcs-setup.md#uninstall-addin)
+ [تعديل سيناريو ذكاء IoT قيد التشغيل](iot-management.md#modify-a-running-iot-intelligence-scenario)
+ [خيارات المحاكاة](iot-management.md#simulation-options)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]