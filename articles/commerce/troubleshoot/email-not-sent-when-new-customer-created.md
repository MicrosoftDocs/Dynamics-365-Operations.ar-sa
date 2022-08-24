---
title: لا يتم إرسال البريد الإلكتروني الترحيبي عند إنشاء عملاء جدد
description: يوفر هذا المقال إرشادات استكشاف الأخطاء وإصلاحها التي يمكن أن تساعد في حالة عدم إرسال إشعار بريد إلكتروني ترحيبي عند إنشاء عميل جديد في Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 08/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 5aa7d864555f96194500989e2d7ad200d8892121
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219394"
---
# <a name="welcome-email-isnt-sent-when-new-customers-are-created"></a>لا يتم إرسال البريد الإلكتروني الترحيبي عندما يتم إنشاء عملاء جدد

[!include [banner](../../includes/banner.md)]

يوفر هذا المقال إرشادات استكشاف الأخطاء وإصلاحها التي يمكن أن تساعد في حالة عدم إرسال إشعار بريد إلكتروني ترحيبي عند إنشاء عميل جديد في Microsoft Dynamics 365 Commerce.

## <a name="description"></a>‏‏الوصف‬

عندما يتم إنشاء عميل جديد في Commerce headquarters، لا يتم إرسال بريد إلكتروني ترحيبي إلى العميل، على الرغم من تكوين إشعار بريد إلكتروني لنوع إشعار البريد الإلكتروني **العميل الذي تم إنشاؤه**.

## <a name="resolution"></a>القرار

### <a name="associate-an-email-notification-profile-under-commerce-parameters"></a>اقران ملف تعريف اخطار بالبريد الكتروني ضمن محددات التجارة

1. في المقر، انتقل إلى **البيع بالتجزئة والتجارة \> إعداد المقر \> المعلمات \> معلمات التجارة \> عام**.
2. في القائمة المنسدلة لملف تعريف **اعلامات البريد** الكتروني ، حدد ملف تعريف اعلام البريد الكتروني الذي يحتوي علي تعيين بين نوع اخطار تم إنشاؤه من قبل العميل وقالب بريد الكتروني انشاه العميل.  

> [!NOTE] 
> عند تمكين إخطارات انشاتها العميل ، سيتلقى العملاء الذين تم إنشاؤهم في كافة القنوات داخل الكيان القانوني البريد الكتروني الذي انشاه العميل. في الوقت الحالي ، لا يمكن ان تكون الاعلامات التي انشاها العميل محدودة بقناة واحده.

لمزيد من المعلومات، راجع [إنشاء قوالب بريد إلكتروني لأحداث المعاملات](../email-templates-transactions.md). 

## <a name="additional-resources"></a>الموارد الإضافية

[إنشاء ملف تعريف الإخطار بالبريد الإلكتروني](../email-notification-profiles.md)
