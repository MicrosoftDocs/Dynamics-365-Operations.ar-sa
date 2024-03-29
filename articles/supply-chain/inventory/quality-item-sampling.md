---
title: أخذ عينات من صنف أداره الجودة
description: يصف هذا المقال كيفية إعداد عينات العنصر.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 644eae4fbd9f82027c1cb69efba00dc893f8fc66
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865139"
---
# <a name="quality-management-item-sampling"></a>أخذ عينات من صنف أداره الجودة

[!include [banner](../includes/banner.md)]

يتم استخدام نماذج الأصناف كجزء من عمليه اقتران الجودة. وهو يحدد مقدار المخزون الفعلي الحالي الذي يجب فحصه. يمكن أن يستند أخذ العينات إلى كميات ثابتة أو نسبة مئوية أو لوحة الترخيص الكاملة.

## <a name="set-up-item-sampling"></a>إعداد أخذ عينات الصنف‬

اتبع هذه الخطوات لإعداد عينات العنصر.

1. انتقل إلى **إدارة المخزون \> إعداد \> مراقبة الجودة‬ \> أخذ عينات للصنف‬**.
1. حدد **جديد**.
1. في الحقل **أخذ عينات للصنف**، أدخل قيمة.
1. في حقل **الوصف**، أدخل قيمة.
1. في الحقل **القيمة**، أدخل رقمًا. ترتبط هذه القيمة بقيمة مواصفات الكمية المحددة في الحقل المجاور.
1. في قسم **العملية**، حدد خانة الاختيار **الحظر الكامل** إذا كان يجب حظر الكمية الكاملة أو كمية بند الأمر في حالة فشل الاختبار. في حاله إلغاء تحديد خانه الاختيار هذه، سيتم حظر الأصناف الموجودة في أمر الجودة فقط في حاله فشل الاختبار.
1. حدد **حفظ**.
1. قم بإغلاق الصفحة.

> [!NOTE]
> توفر ميزة *‏‫إدارة الجودة لعمليات المستودعات‬* إمكانات أخذ عينات إضافية للأصناف. ويقوم بإضافة لـ *نطاق أخذ العينات للصنف* ويتيح لك تحديد لوحة ترخيص كاملة كمواصفة للكمية. إذا قمت بتشغيل هذه الميزة، فراجع [إدارة الجودة لعمليات المستودعات](quality-management-for-warehouses-processes.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
