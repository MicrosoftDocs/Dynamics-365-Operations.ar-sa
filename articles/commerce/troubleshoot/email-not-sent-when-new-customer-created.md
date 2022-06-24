---
title: لا يتم إرسال البريد الإلكتروني الترحيبي عند إنشاء عملاء جدد
description: يوفر هذا المقال إرشادات استكشاف الأخطاء وإصلاحها التي يمكن أن تساعد في حالة عدم إرسال إشعار بريد إلكتروني ترحيبي عند إنشاء عميل جديد في Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 8e95b33d4b8a9af13c613ab89dd33de6b4934694
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853673"
---
# <a name="welcome-email-is-not-sent-when-new-customers-are-created"></a>لا يتم إرسال البريد الإلكتروني الترحيبي عند إنشاء عملاء جدد

[!include [banner](../../includes/banner.md)]

يوفر هذا المقال إرشادات استكشاف الأخطاء وإصلاحها التي يمكن أن تساعد في حالة عدم إرسال إشعار بريد إلكتروني ترحيبي عند إنشاء عميل جديد في Microsoft Dynamics 365 Commerce.

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
