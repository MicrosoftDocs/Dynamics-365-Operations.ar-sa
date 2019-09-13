---
title: إنشاء وصيانة حظر المخزون
description: يوضح هذا الإجراء كيفية منع حجز مخزون فعلي موجود بواسطة مستندات مصدر صادرة أخرى باستخدام حظر المخزون.
author: perlynne
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b2485eaf31226b11106895074ae0ad95e561777b
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916589"
---
# <a name="create-and-maintain-an-inventory-blocking"></a>إنشاء وصيانة حظر المخزون

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

