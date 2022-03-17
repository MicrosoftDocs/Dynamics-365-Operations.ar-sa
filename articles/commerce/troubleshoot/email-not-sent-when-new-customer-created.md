---
title: لا يتم إرسال البريد الإلكتروني الترحيبي عند إنشاء عملاء جدد
description: يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها التي يمكن أن تساعد في حالة عدم إرسال إشعار بريد إلكتروني ترحيبي عند إنشاء عميل جديد في Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 1a4faf6cd189f69232e7f9ab8d0e79b320cfe2d9
ms.sourcegitcommit: d2e5d38ed1550287b12c90331fc4136ed546b14c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/25/2022
ms.locfileid: "8349936"
---
# <a name="welcome-email-is-not-sent-when-new-customers-are-created"></a>لا يتم إرسال البريد الإلكتروني الترحيبي عند إنشاء عملاء جدد

[!include [banner](../../includes/banner.md)]

يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها التي يمكن أن تساعد في حالة عدم إرسال إشعار بريد إلكتروني ترحيبي عند إنشاء عميل جديد في Microsoft Dynamics 365 Commerce.

## <a name="description"></a>‏‏الوصف‬

عندما يتم إنشاء عميل جديد في Commerce headquarters، لا يتم إرسال بريد إلكتروني ترحيبي إلى العميل، على الرغم من تكوين إشعار بريد إلكتروني لنوع إشعار البريد الإلكتروني **العميل الذي تم إنشاؤه**.

## <a name="resolution"></a>القرار

### <a name="set-the-correct-email-id-value-for-the-customer-created-email-notification-type"></a>تعيين قيمة معرف البريد الإلكتروني الصحيحة لنوع إشعار البريد الإلكتروني الذي أنشأه العميل

لتعيين قيمة **معرّف البريد الإلكتروني** لنوع إشعار البريد الإلكتروني **الذي تم إنشاؤه بواسطة العميل** في المقر، اتبع هذه الخطوات.

1. انتقل إلى **Retail وCommerce \> إعداد Headquarters \> ملف تعريف إشعار البريد الإلكتروني لـ Commerce**.
1. في جزء التنقل الأيسر، حدد ملف تعريف إعلام البريد الإلكتروني.
1. ضمن **إعدادات إعلامات أحداث Retail**، بالنسبة لنوع إعلام البريد الإلكتروني **الذي تم إنشاؤه بواسطة العميل**، قم بتعيين حقل **معرف البريد الإلكتروني** إلى **NewCust**.

## <a name="additional-resources"></a>الموارد الإضافية

[إنشاء ملف تعريف الإخطار بالبريد الإلكتروني](../email-notification-profiles.md)
