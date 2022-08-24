---
title: يمكن عمل سداد مع الخروج للأصناف التي ليس لها مخزون
description: يوفر هذا المقال إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد عندما يقوم أحد العملاء بإضافة أصناف خارج المخزون إلى سلة التسوق الخاصة بهم ومتابعة السداد مع الخروج.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 3bc924e44077886b942e19b25a84f0f1d4298c13
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282724"
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
