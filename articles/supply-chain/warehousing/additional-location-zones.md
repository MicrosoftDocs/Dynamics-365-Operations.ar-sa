---
title: مناطق المواقع الإضافية
description: يوفر هذا المقال نظرة عامة على مناطق المواقع الجديدة التي تمت اضافتها إلى Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationBuild, WHSZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 819330e0f6e6cd419da441f919d68ff996b6475c
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336474"
---
# <a name="additional-location-zones"></a>مناطق المواقع الإضافية

[!include [banner](../includes/banner.md)]

تتوفر ثلاثة حقول مناطق جديدة في Microsoft Dynamics 365 Supply Chain Management. ويمكن لمديري المستودع استخدامهما لتحديد المؤسسات أو التخطيطات الإضافية للمستودع. يمكن تعيين حقول المنطقة الجديدة إما يدويًا أو باستخدام معالج **إعداد الموقع**. ويمكن استخدامها في أي استعلام أو تصفية تستخدم جدول المواقع.

لا يتطلب الأمر أي إعداد إضافي لاستخدام حقول المنطقة.

## <a name="turn-the-additional-location-zone-feature-on-or-off"></a>تشغيل ميزة منطقة الموقع الإضافية أو إيقاف تشغيلها

لاستخدام هذه الميزة ، يجب تشغيلها لنظامك. اعتبارًا من الإصدار 10.0.25 من Supply Chain Management، يتم تشغيل هذه الميزة افتراضيًا. اعتبارًا من الإصدار 10.0.29 من Supply Chain Management، هذه الميزة إلزامية ولا يمكن إيقاف تشغيلها. إذا كنت تقوم بتشغيل إصدار أقدم من 10.0.29، فبإمكان المسؤولين تشغيل هذه الوظيفة أو إيقاف تشغيلها عن طريق البحث عن ميزة *منطقة موقع إضافية‬‬‬* في مساحة عمل [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="use-location-zones"></a>استخدام مناطق الموقع

1. انتقل إلى **إدارة المستودع \> الإعداد \> المستودع \> معالج إعداد الموقع**.
2. قم بتعيين القيم التالية:

    - في حقل **المستودع**، حدد _62_.
    - في الحقل **معرف المنطقة**، حدد _FLOOR_.
    - في الحقل **المنطقة الإضافية 1**، حدد _PICKZONE1_.
    - في الحقل **المنطقة الإضافية 2**، حدد _WEBSHOP1_.
    - في الحقل **معرف ملف تعريف الموقع**، حدد _FLOOR_.

3. حدد سطر **الأرضية**.
4. في الحقل **‏من رقم**، أدخل _1_. في الحقل **‏إلى رقم**، أدخل _3_.
5. حدد سطر **الممر**.
6. في الحقل **‏من رقم**، أدخل _1_. في الحقل **‏إلى رقم**، أدخل _5_.
7. حدد **إنشاء**.
8. سوف تتلقى رسائل تشير إلى إضافة مواقع جديدة. حدد زر **إظهار الرسائل** لعرض الرسائل.
9. انتقل إلى **إدارة المستودعات \> الإعداد \> المستودع \> المواقع**. تظهر المواقع الجديدة في القائمة، وتتوفر كافة حقول المنطقة (وهي حقل المنطقة الموجود وحقول المنطقة الإضافية الجديدة).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]