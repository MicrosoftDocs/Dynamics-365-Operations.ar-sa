---
title: يمكن عمل سداد مع الخروج للأصناف التي ليس لها مخزون
description: يوفر هذا المقال إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد عندما يقوم أحد العملاء بإضافة أصناف خارج المخزون إلى سلة التسوق الخاصة بهم ومتابعة السداد مع الخروج.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 24400953d2a17384be8ab3000aa829bf2bcb7192
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877175"
---
# <a name="items-without-inventory-can-be-checked-out"></a>يمكن عمل سداد مع الخروج للأصناف التي ليس لها مخزون

[!include [banner](../../includes/banner.md)]

يوفر هذا المقال إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد عندما يقوم أحد العملاء بإضافة أصناف خارج المخزون إلى سلة التسوق الخاصة بهم ومتابعة السداد مع الخروج.

## <a name="description"></a>الوصف

يمكن للمستخدمين إضافة أحد الأصناف إلى سلة التسوق الخاصة بهم، على الرغم من عدم وجود مخزون فعلي في المتجر، ثم الانتقال إلى صفحة السداد مع الخروج.

## <a name="resolution"></a>الدقة

### <a name="enable-the-show-out-of-stock-errors-property-in-commerce-site-builder"></a>تمكين خاصية إظهار أخطاء نفاد المخزون في منشئ موقع Commerce

لتمكين خاصية **إظهار أخطاء نفاد المخزون** في منشئ موقع Commerce، اتبع هذه الخطوات.

1. حدد الموقع الذي تعمل عليه.
1. في جزء التنقل الأيسر، حدد **الصفحات**.
1. حدد **CartPage** لفتحه.
1. حدد فتحة **سلة التسوق 1**، وحدد **تحرير**، ثم في جزء الخصائص، حدد خانة الاختيار **إظهار أخطاء نفاد المخزون**.
1. احفظ الصفحة وقم بنشرها.

## <a name="additional-resources"></a>الموارد الإضافية

[تطبيق إعدادات المخزون](../inventory-settings.md)

[حساب توفر المخزون لقنوات البيع بالتجزئة](../calculated-inventory-retail-channels.md)

[تكوين المخازن المؤقتة للمخزون ومستويات المخزون](../inventory-buffers-levels.md)
