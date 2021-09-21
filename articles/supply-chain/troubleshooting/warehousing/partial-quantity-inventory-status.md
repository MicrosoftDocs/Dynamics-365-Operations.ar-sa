---
title: تغيير حالة المخزون للعمل الجزئي للكمية
description: توضح هذه الصفحة كيفية إنشاء عنصر قائمة بالإعدادات المناسبة لتمكين العاملين من تغيير حالة المخزون للكمية الجزئية للدفعة.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 056ce412955808ddf126025ad917b874c54a5e62
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475422"
---
# <a name="enable-inventory-status-change-for-partial-quantity-work"></a>تمكين تغيير حالة المخزون للعمل الجزئي للكمية

## <a name="symptoms"></a>العلامات

يلزمك إجراء تغيير حالة المخزون لكمية جزئية في دفعة.

## <a name="resolution"></a>الحل

لتمكين العاملين من اجراء هذا التغيير، يمكنك إنشاء عنصر قائمه لتطبيق إدارة المستودع للأجهزة المحمولة. في صفحة **عناصر قائمة الجهاز المحمول**، أنشئ عناصر قائمة لأحد الطرق التالية:

- **الوضع:** *العمل*
- **استخدام العمل الموجود:** *لا*
- **عملية إنشاء العمل:** *الحركة*
- **عرض حالة المخزون:** *نعم*

يمكنك تعيين حقول أخرى في الصفحة كما هو مطلوب.
