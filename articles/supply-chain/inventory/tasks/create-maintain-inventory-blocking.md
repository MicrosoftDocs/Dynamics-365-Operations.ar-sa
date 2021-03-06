---
title: إنشاء وصيانة حظر المخزون
description: يوضح هذا الإجراء كيفية منع حجز مخزون فعلي موجود بواسطة مستندات مصدر صادرة أخرى باستخدام حظر المخزون.
author: perlynne
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eab6730daa2eb7df0f91d99d1026d4736285fef9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000049"
---
# <a name="create-and-maintain-an-inventory-blocking"></a>إنشاء وصيانة حظر المخزون

[!include [banner](../../includes/banner.md)]

يوضح هذا الإجراء كيفية منع حجز مخزون فعلي موجود بواسطة مستندات مصدر صادرة أخرى باستخدام حظر المخزون. يمكنك تشغيل هذا الإجراء في شركة بيانات العرض التوضيحي USMF باستخدام قيم الأمثلة الموضحة. يجب أن يتوفر لديك صنف مع مخزون فعلي موجود قبل بدء هذا الإجراء.


## <a name="create-an-inventory-blocking"></a>إنشاء حظر المخزون
1. في **جزء التنقل**، انتقل إلى **الوحدات النمطية > إدارة المخزون > المهام الدورية > حظر المخزون**.
2. انقر فوق **جديد**.
3. في الحقل **رقم الصنف**، انقر فوق زر القائمة المنسدلة لفتح البحث.
4. في القائمة، حدد الصنف الذي تريد اختياره. حدد رقم صنف مع المخزون الفعلي الموجود الذي تريد حظره. إذا كنت تستخدم USMF، فيمكنك تحديد الصنف M9201.  
5. في الحقل **الكمية**، أدخل رقمًا. إذا كنت تستخدم الصنف M9201، فتحتاج إلى تحديد أقل من 200.
6. قم بتوسيع القسم **أبعاد المخزون**.
7. في الحقل **المستودع**، انقر فوق زر القائمة المنسدلة لفتح البحث.
8. في القائمة، قم بالبحث عن السجل المطلوب وحدده. إذا كنت تستخدم الصنف M9201، فيمكنك تحديد المستودع 51.  
9. انقر فوق **حفظ**.

## <a name="update-the-conditions-of-the-inventory-blocking"></a>تحديث شروط حظر المخزون
1. على علامة التبويب السريعة **عام**، أدخل رقمًا في حقل **الكمية**. حدّث الحقل "كمية المخزون" لعكس الكمية التي تريد حظرها.  
2. أدخل تاريخًا في حقل **التاريخ المتوقع‬**. قد تحتاج إلى الإشارة إلى الوقت الذي من المتوقع أن يصبح فيه المخزون المحظور متوفرًا للحجز عن طريق تعيين تاريخ متوقع. إذا تم تحديد الخيار "الإيصالات المستلمة‬" لحظر المخزون، كما يتم بشكل افتراضي عندما تنشئ الحظر يدويًا، فسيظهر هذا التاريخ على الحركة المتوقعة.  
3. انقر فوق **حفظ**.

## <a name="remove-the-inventory-blocking"></a>إزالة حظر المخزون
1. في **جزء الإجراءات**، انقر فوق **حذف**.
2. انقر فوق **نعم**.
3. قم بإغلاق الصفحة.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]