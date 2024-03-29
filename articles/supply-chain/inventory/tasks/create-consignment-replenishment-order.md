---
title: إنشاء أمر تزويد شحن
description: يوضح هذا المقال كيفية إنشاء أمر تزويد الشحن حيث يمكنك تعقب التسليم المتوقع من مورّد إلى مخزون الشحن.
author: yufeihuang
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple, ConsignmentProductReceiptJournal, ConsignmentReplenishmentOrderLineQuantity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 31a1d0a7d322b17d3d80dd9fade2b037dd148d9f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859362"
---
# <a name="create-a-consignment-replenishment-order"></a>إنشاء أمر تزويد شحن

[!include [banner](../../includes/banner.md)]

يوضح هذا المقال كيفية إنشاء أمر تزويد الشحن حيث يمكنك تعقب التسليم المتوقع من مورّد إلى مخزون الشحن. ويوضح أيضًا كيفية تسجيل إيصال استلام المنتجات بحيث يتم تسجيل مخزون الشحن كمخزون فعلي يملكه المورّد. يقوم عادةً أخصائي التدبير بتنفيذ هذا الإجراء. ويمكنك استخدام هذا الدليل في شركة بيانات العرض التوضيحي USMF. يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.

## <a name="create-a-consignment-replenishment-order"></a>إنشاء أمر تزويد شحن
1. في جزء التنقل، انتقل إلى **الوحدات النمطية > التدبير والتوريد > الشحن > أوامر تزويد الشحن‬**.
2. حدد **جديد**.
3. في الحقل **حساب المورّد**، حدد المورّد **US-104** (يجب تحديد مورّد غير مسجل كمالك في صفحة **ملاك المخزون**). 
4. حدد **موافق**.
5. حدد **إضافة بند**.
6. في الحقل **رقم الصنف**، اكتب `M9211CI` (يجب تحديد صنف تم إعداده لمخزون الشحن).
7. في الحقل **الكمية**، أدخل رقمًا.
8. في حقل **‏‫تاريخ التسليم المطلوب‬‬**، أدخل تاريخًا. يتم استخدام التواريخ المطلوبة والمؤكدة بواسطة محرك MRP لوصول البضائع المنتظر.  
9. في حقل **‏‫تاريخ التسليم المؤكد‬**، أدخل تاريخًا.
10. قم بتوسيع قسم **تفاصيل البند**.
11. حدد علامة التبويب **أبعاد المخزون**.
12. لإظهار المالك في الحقل **مالك أبعاد المخزون**، قم بتحديث الصفحة. تم الآن إدراج المورّد US-104 كالمالك.  

## <a name="check-the-inventory-transaction-status"></a>التحقق من حالة حركة المخزون
1. حدد **المخزون**.
2. حدد **الحركات**.
3. في الصف المطلوب، لاحظ أنه تم تعيين حقل **الاستلام** إلى **مطلوب‬**.  
4. قم بإغلاق الصفحة.

## <a name="receive-items"></a>استلام الأصناف
1. حدد **إيصال استلام المنتجات**.
2. في الحقل **إيصال استلام المنتجات الخارجي‬**، اكتب قيمة.
3. في حقل **الكمية**، أدخل رقمًا أقل من الرقم الذي يظهر هناك. 
4. حدد **موافق**.

## <a name="check-the-on-hand-inventory"></a>التحقق من المخزون الفعلي
1. حدد **المخزون**.
2. حدد **المخزون الفعلي**.
3. حدد **نظرة عامة**. تتوفر الأصناف التي تم استلامها كمخزون شحن مملوك من قِبل المورّد بشكل فعلي. وتظهر الكمية المتبقية في أمر تزويد الشحن في حقل **الكمية المطلوبة إجمالاً‬**.  
4. قم بإغلاق الصفحة.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]