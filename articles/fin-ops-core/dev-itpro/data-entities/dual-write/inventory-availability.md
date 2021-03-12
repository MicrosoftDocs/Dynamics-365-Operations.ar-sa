---
title: توفر المخزون في الكتابة المزدوجة
description: يوفر هذا الموضوع معلومات حول فحص توفر المخزون في الكتابة المزدوجة.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: a7bfe998d2d787203a507a831c171fc43b03fedc
ms.sourcegitcommit: cc9921295f26804259cc9ec5137788ec9f2a4c6f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/08/2021
ms.locfileid: "4839539"
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

تطبيقات Finance and Operations | تطبيق Customer Engagement | الوصف 
---|---|---
[إدخالات المخزون الفعلي في CDS](#145) | msdyn_inventoryonhandentries |
[طلبات المخزون الفعلي في CDS](#147) | msdyn_inventoryonhandrequests |

[!include [banner](../../includes/dual-write-symbols.md)]

###  <a name="cds-inventory-on-hand-entries-msdyn_inventoryonhandentries"></a><a name="145"></a>الإدخالات الفعلية لمخزون الاقراص المضغوطة (msdyn_inventoryonhandentries)

يقوم هذا القالب بمزامنة البيانات بين تطبيقات Finance and Operations وDataverse.

حقل Finance and Operations | نوع التعيين | حقل Customer Engagement | قيمة افتراضية
---|---|---|---
`REQUESTID` | = | `msdyn_request.msdyn_requestid` |
`INVENTORYSITEID` | = | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | = | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`AVAILABLEONHANDQUANTITY` | > | `msdyn_availableonhandquantity` |
`AVAILABLEORDEREDQUANTITY` | > | `msdyn_availableorderedquantity` |
`ONHANDQUANTITY` | > | `msdyn_onhandquantity` |
`ONORDERQUANTITY` | > | `msdyn_onorderquantity` |
`ORDEREDQUANTITY` | > | `msdyn_orderedquantity` |
`RESERVEDONHANDQUANTITY` | > | `msdyn_reservedonhandquantity` |
`RESERVEDORDEREDQUANTITY` | > | `msdyn_reservedorderedquantity` |
`TOTALAVAILABLEQUANTITY` | > | `msdyn_totalavailablequantity` |
`ATPDATE` | = | `msdyn_atpdate` |
`ATPQUANTITY` | > | `msdyn_atpquantity` |
`PROJECTEDISSUEQUANTITY` | > | `msdyn_projectedissuequantity` |
`PROJECTEDONHANDQUANTITY` | > | `msdyn_projectedonhandquantity` |
`PROJECTEDRECEIPTQUANTITY` | > | `msdyn_projectedreceiptquantity` |
`ORDERQUANTITY` | > | `msdyn_orderquantity` |
`UNAVAILABLEONHANDQUANTITY` | > | `msdyn_unavailableonhandquantity` |

###  <a name="cds-inventory-on-hand-requests-msdyn_inventoryonhandrequests"></a><a name="147"></a>الطلبات المخزون الفعلي CDS (msdyn_inventoryonhandrequests)

يقوم هذا القالب بمزامنة البيانات بين تطبيقات Finance and Operations وDataverse.

حقل Finance and Operations | نوع التعيين | حقل Customer Engagement | قيمة افتراضية
---|---|---|---
`REQUESTID` | = | `msdyn_requestid` |
`PRODUCTNUMBER` | < | `msdyn_product.msdyn_productnumber` |
`ISATPCALCULATION` | << | `msdyn_isatpcalculation` |
`ORDERQUANTITY` | < | `msdyn_orderquantity` |
`INVENTORYSITEID` | < | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | < | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`REFERENCENUMBER` | < | `msdyn_referencenumber` |
`LINECREATIONSEQUENCENUMBER` | < | `msdyn_linecreationsequencenumber` |




