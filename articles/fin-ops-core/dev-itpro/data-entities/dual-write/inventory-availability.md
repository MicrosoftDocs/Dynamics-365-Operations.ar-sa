---
title: توفر المخزون في الكتابة المزدوجة
description: توفر هذه المقالة معلومات عن فحص توفر المخزون في الكتابة المزدوجة.
author: RamaKrishnamoorthy
ms.date: 05/26/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: efd175dfbe49549561bdb7d697c8bc47016f1d5d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908251"
---
# <a name="inventory-availability-in-dual-write"></a>توفر المخزون في الكتابة المزدوجة

[!include [banner](../../includes/banner.md)]

باستخدام توفر المخزون، يمكنك فحص المخزون قبل إضافة منتج إلى صفحة **عروض الأسعار** أو **الأوامر** أو **الفواتير** في Microsoft Dynamics 365 Sales. على سبيل المثال، يمكنك فحص المخزون وتحديد تاريخ التنفيذ كمهمة أساسية في عملية [العميل المتوقع إلى النقدية](dual-write-prospect-to-cash.md).

إذا لم يكن لديك مخزون كافٍ، فيمكنك تقدير تاريخ التسليم استنادًا إلى عمليات استلام المخزون المتوقعة ومشاكلها. يمكنك أيضًا التحقق من معلومات "متوفر حسب التعهد‬" للمنتج، حيث يمكنك العثور على كمية ATP في الحد الزمني المحدد مسبقًا.

## <a name="on-hand-inventory"></a>المخزون الفعلي

في رأس صفحات **عروض الأسعار** أو **الأوامر** أو **الفواتير** في Dynamics 365 Sales، تمت إضافة زر جديد **المخزون الفعلي**. عند النقر فوق الزر، يظهر مربع حوار ويمكنك تحديد الشركة والمنتج الذي تريد فحص مخزونه الفعلي. يظهر مربع الحوار هذا نفس المعلومات كـ [مخزون فعلي](../../../../supply-chain/inventory/tasks/check-availability-stock.md).

يقوم مربع الحوار بإرجاع معلومات المخزون من Dynamics 365 Supply Chain Management. تشمل هذه المعلومات الكميات التالية:

- الكمية المتاحة
- الكمية المحجوزة
- الكمية الفعلية المتوفرة
- الكمية المطلوبة
- الكمية تحت الطلب
- الكمية المطلوبة المحجوزة
- إجمالي الكمية المتوفرة

## <a name="atp-information"></a>معلومات ATP

في Sales، تمت إضافة زر **معلومات ATP** جديد إلى أصناف البند في صفحة **عروض الأسعار** و **الأوامر** و **الفواتير**. عند تحديد هذا الزر، يظهر مربع حوار ويمكنك تحديد الشركة والمنتج وموقع المخزون ومستودع المخزون وكمية الأمر. لمربع الحوار هذا نفس الإعدادات الموضحة في [‏‫التعهد بالأمر‬](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).

يقوم مربع الحوار بإرجاع معلومات ATP من Supply Chain Management. تشمل هذه المعلومات الكميات التالية:

- كمية ATP
- كمية الإيصال
- كمية الإصدار
- كمية المخزون الفعلي

## <a name="how-it-works"></a>كيف يعمل

عند تحديد الزر **المخزون الفعلي** في الصفحة **عروض الأسعار** أو **الأوامر** أو **الفواتير**، يتم اجراء استدعاء ثنائي الكتابة واجهة API **المخزون الفعلي**. تقوم واجهه برمجه التطبيقات بحساب المخزون الفعلي للمنتج المحدد. يتم تخزين النتيجة في الجدولين **InventCDSInventoryOnHandRequestEntity** و **InventCDSInventoryOnHandEntryEntity**، ثم تتم كتابتها علي Dataverse حسب الكتابة الثنائية. لاستخدام هذه الوظيفة، يجب تشغيل التعيينات ثنائيه الكتابة التالية. يستخدم هذا الحقل لتخطي المزامنة الاوليه عند تشغيل الخرائط.

- الإدخالات الفعلية لمخزون الاقراص المضغوطة (msdyn_inventoryonhandentries)
- الطلبات المخزون الفعلي CDS (msdyn_inventoryonhandrequests)

## <a name="templates"></a>القوالب

تتوفر القوالب التالية لعرض بيانات المخزون الفعلي.

تطبيقات Finance and Operations | تطبيقات Customer Engagement     | الوصف
---|---|---
[إدخالات المخزون الفعلي في CDS](mapping-reference.md#145) | msdyn_inventoryonhandentries |
[طلبات المخزون الفعلي في CDS](mapping-reference.md#147) | msdyn_inventoryonhandrequests |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
