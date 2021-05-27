---
title: أخذ عينات من صنف أداره الجودة
description: يصف هذا الموضوع كيفية إعداد عينات العنصر.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae8bfd329ca0d7c30adcd93a759ee6bea7b76278
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022218"
---
# <a name="quality-management-item-sampling"></a>أخذ عينات من صنف أداره الجودة

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
