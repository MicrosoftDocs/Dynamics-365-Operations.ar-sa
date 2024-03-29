---
title: إدارة عمليات تعليق الأمر
description: يوضح هذا الإجراء كيفية وضع أوامر مبيعات العميل قيد الانتظار، وكيفية العمل مع عمليات سحب تعليقات الأمر، وكيفية إزالة تعليقات الأمر.
author: Henrikan
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MCRHoldCodeTable, SalesTableListPage, SalesCreateOrder, SalesTable, MCRHoldCodeTrans, MCRHoldCheckOutOverride, MCRHoldCodeTable, MCRItemListCopying, MCRItemListTable, MCROMHoldList
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 938b21b66b7b61452be104936877278a3bc120f2
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566277"
---
# <a name="manage-order-holds"></a>إدارة عمليات تعليق الأمر

[!include [banner](../../includes/banner.md)]

يوضح هذا الإجراء كيفية وضع أوامر مبيعات العميل قيد الانتظار، وكيفية العمل مع عمليات سحب تعليقات الأمر، وكيفية إزالة تعليقات الأمر. قد يتم وضع أمر قيد الانتظار لأسباب عدة. على سبيل المثال، قد تضع أمر قيد الانتظار حتى يمكن التحقق من أسلوب الدفع أو عنوان عميل أو حتى يقوم مدير بمراجعة حد الائتمان الخاص بالعميل. بينما يكون الأمر قيد الانتظار، لا يمكن معالجته بواسطة المستودع لشحنه. 

يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF أو باستخدام بياناتك الخاصة.


## <a name="set-up-order-holds"></a>إعداد تعليقات الأمر
1. انتقل إلى **جزء التنقل > الوحدات > المبيعات والتسويق > إعداد > أوامر المبيعات > أكواد تعليق الأمر**.
2. انقر فوق **جديد**.
3. في حقل **كود التعليق**، اكتب قيمة. على سبيل المثال، اكتب "استدعاء".  
4. في حقل **الوصف**، اكتب قيمة.
    - على سبيل المثال، تعليق أمر قيد انتظار استدعاء العميل.  
    - بشكل اختياري، حدد خانة الاختيار **إزالة الحجوزات‬** لإزالة أي حجوزات‬ فعلية من الأمر عند إضافة كود التعليق هذا.  
5. انقر فوق **حفظ**.

## <a name="place-order-on-hold"></a>وضع أمر قيد الانتظار
1. انتقل إلى **جزء التنقل > الوحدات > المبيعات والتسويق > أوامر المبيعات > جميع أوامر المبيعات**.
2. انقر فوق **جديد**.
3. أدخل قيمة أو حددها في حقل **حساب العميل**.
4. انقر فوق **موافق**.
5. في الحقل **رقم الصنف**، أدخل قيمة أو حددها.
6. في الحقل **الكمية**، أدخل رقمًا.
7. في **جزء الإجراءات**، انقر فوق **أمر المبيعات**.
8. انقر فوق **تعليقات الأمر**.
9. انقر فوق **جديد**.
10. في حقل **كود التعليق**، حدد الكود الذي أنشأته في المهمة الفرعية السابقة.
11. انقر فوق **حفظ**.
12. قم بإغلاق الصفحة.
13. انتقل إلى **المبيعات والتسويق > أوامر المبيعات > كافة أوامر المبيعات**. 
14. في القائمة، قم بوضع علامة للصف المحدد. تتضمن الأوامر الموضوعة قيد الانتظار حاليًا الحقلين "‏‫لا تقم بالمعالجة‬ "و"تعليق‬" وقد تم تعليمهما.
15. في جزء الإجراءات، انقر فوق **انتقاء وتعبئة**.

## <a name="manage-order-holds"></a>إدارة عمليات تعليق الأمر
1. انتقل إلى **المبيعات والتسويق > أوامر المبيعات > الأوامر المفتوحة > تعليقات الأمر**.  تعمل الصفحة **تعليقات الأمر‬** كمنضدة عمل حيث يمكنك الحصول على نظرة عامة على كافة التعليقات الحالية وتلك التي تمت معالجتها، وحيث يمكنك معالجتها كأوامر مبيعات مقترنة.     
2. في القائمة، قم بوضع علامة للصف المحدد.
3. في **جزء الإجراءات**، انقر فوق **السحب المعلق**.
4. انقر فوق **سحب**.
5. في القائمة، قم بإلغاء علامة الصف المحدد. يعرض الآن حقل **السحب إلى** معرف المستخدم الخاص بك.   
6. انقر فوق **مسح السحب**.
7. في **جزء الإجراءات**، انقر فوق **مسح التعليق**.
    - عندما تصبح جاهزًا لإزالة تعليق الأمر والسماح للأمر بالمتابعة إلى خطوة التنفيذ التالية، يجب مسح التعليق. إذا لم يتطلب الأمر إجراء أي تغيير، فيمكنك تشغيل الإجراء "مسح التعليقات‬". ومع ذلك، يمكنك استخدام الإجراء "مسح وتعديل‬"، إذا كان الأمر بحاجة إلى تحديث عند مسح التعليق.      
    - ينطبق الإجراء **مسح وإرسال** فقط عندما تستخدم وظيفة مركز الاتصال‬.  
8. انقر فوق **مسح التعليقات‬**. تم الآن مسح التعليق من الأمر وتمت إزالته من قائمة التعليقات النشطة. لعرض كافة التعليقات أو مجموعتها الفرعية وفقًا لحالة معينة، قم بتغيير القيمة الموجودة في الحقل "إظهار".     



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]