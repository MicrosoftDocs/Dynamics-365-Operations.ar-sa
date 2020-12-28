---
title: مناطق المواقع الإضافية
description: يوفر هذا الموضوع نظرة عامة على مناطق المواقع الجديدة التي تمت اضافتها إلى Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationBuild, WHSZone
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 6cf81939989b8faffcda51bbbd5bc6b27aec7eea
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4421734"
---
# <a name="additional-location-zones"></a>مناطق المواقع الإضافية

[!include [banner](../includes/banner.md)]

تتوفر ثلاثة حقول مناطق جديدة في Microsoft Dynamics 365 Supply Chain Management. ويمكن لمديري المستودع استخدامهما لتحديد المؤسسات أو التخطيطات الإضافية للمستودع. يمكن تعيين حقول المنطقة الجديدة إما يدويًا أو باستخدام معالج **إعداد الموقع**. ويمكن استخدامها في أي استعلام أو تصفية تستخدم جدول المواقع.

لا يتطلب الأمر أي إعداد إضافي لاستخدام حقول المنطقة.

## <a name="turn-on-the-additional-location-zone-feature"></a>تشغيل ميزة منطقة الموقع الإضافية

قبل أن تتمكن من استخدام ميزة *منطقة الموقع الإضافية*، يجب تشغيلها في النظام الخاص بك. يمكن للمسؤولين استخدام إعدادات [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها إذا كانت مطلوبة. في مساحة عمل **إدارة الميزات**، تكون هذه الميزة مدرجة بالطريقة التالية:

- **الوحدة:** *إدارة المستودعات*
- **اسم الميزة:** *منطقة الموقع الإضافية*

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
