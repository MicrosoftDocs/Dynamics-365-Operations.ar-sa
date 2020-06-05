---
title: تثبيت الوظيفة الإضافية لذكاء IoT في LCS
description: يشرح هذه الموضوع تثبيت الوظيفة الإضافية لذكاء IoT في Microsoft Dynamics Lifecycle Services (LCS).
author: robinarh
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 04333b3659f090b15cc0d0ee216f14dabc588883
ms.sourcegitcommit: 261b70ea358b2c231e20f320ed8bd6adc1e7d715
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386481"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a>تثبيت الوظيفة الإضافية لذكاء IoT في LCS

[!include [banner](../../includes/banner.md)]

يشرح هذه الموضوع تثبيت الوظيفة الإضافية لذكاء IoT في Microsoft Dynamics Lifecycle Services (LCS). قبل أن تتمكن من تثبيت الوظيفة الإضافية، يجب [إنشاء موارد Azure](iot-azure-setup.md).

## <a name="set-up-the-lcs-environment"></a>إعداد بيئة LCS

1. افتح LCS، وانتقل إلى بيئة Microsoft Dynamics 365 Supply Chain Management الخاصة بك.
2. قم بالتمرير إلى قسم **الوظائف الإضافية للبيئة**.
3. حدد **تثبيت وظيفة إضافية جديدة** لإظهار قائمة بالوظائف الإضافية التي تم تمكينها للبيئة.
4. في مربع الحوار **تحديد وظيفة إضافية للتثبيت**، حدد **ذكاء IoT**.
5. في مربع الحوار **إعداد وظيفة إضافية**، قم بتوفير تفاصيل مركز IoT وذاكرة تخزين Redis المؤقتة الخاصة بك. يمكنك العثور على القيم المطلوبة في المخزن الرئيسي الذي قمت بإنشائه في [إنشاء موارد Azure](iot-azure-setup.md).

    + **معرف المستأجر** – في مدخل Azure، انتقل إلى المخزن الرئيسي، ثم في جزء التنقل الأيسر، حدد **نظرة عامة**، ثم انسخ قيمة **معرف الدليل**. قم بلصق هذه القيمة في مربع الحوار **إعداد الوظيفة الإضافية**.
    + **عنوان URI للمخزن الرئيسي لنقطة النهاية المتوافقة مع مركز أحداث IoT** – انتقل إلى المفتاح الرئيسي، ثم في جزء التنقل الأيسر، حدد **نظرة عامة**، وانسخ قيمة **اسم DNS**. قم بلصق هذه القيمة في مربع الحوار **إعداد الوظيفة الإضافية**.
    + **اسم سر نقطة النهاية المتوافقة مع مركز أحداث IoT** – انتقل إلى المخزن الرئيسي، ثم حدد جزء التنقل الأيسر، وحدد **الأسرار**، وانسخ اسم السر الذي سيتم فيه تخزين سلسلة اتصال مركز الأحداث لـ مركز IoT. قم بلصق هذه القيمة في مربع الحوار **إعداد الوظيفة الإضافية**.
    + **عنوان URI للمخزن الرئيسي لذاكرة تخزين Redis المؤقتة** – انتقل إلى المفتاح الرئيسي، ثم في جزء التنقل الأيسر، حدد **نظرة عامة**، وانسخ قيمة **اسم DNS**. قم بلصق هذه القيمة في مربع الحوار **إعداد الوظيفة الإضافية**.
    + **اسم سر نقطة النهاية ذاكرة تخزين Redis المؤقتة** – انتقل إلى المخزن الرئيسي، ثم حدد جزء التنقل الأيسر، وحدد **الأسرار**، وانسخ اسم السر الذي سيتم فيه تخزين سلسلة الاتصال لذاكرة تخزين Redis المؤقتة. قم بلصق هذه القيمة في مربع الحوار **إعداد الوظيفة الإضافية**.

6. حدد خانة الاختيار لقبول البنود والشروط.
7. حدد **تثبيت**.
8. يظهر مربع رسالة ينص على أنه "تم بنجاح تشغيل الوظيفة الإضافية للتثبيت." حدد **موافق**.

اكتمل الآن إعداد LCS. الخطوة التالية هي [إعداد السيناريوهات](iot-scenario-setup.md).

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a>إلغاء تثبيت الوظيفة الإضافية

1. في Supply Chain Management، [قم بتعطيل السيناريوهات](iot-scenario-setup.md#how-to-disable-a-scenario).
2. في LCS، انتقل إلى تفاصيل بيئة Supply Chain Management.
3. قم بالتمرير إلى قسم **الوظائف الإضافية للبيئة**.
4. حدد **إلغاء التثبيت** للوظيفة الإضافية لذكاء IoT.