---
title: تحديد قواعد تغطية للأصناف
description: شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.
author: ShylaThompson
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c156ae4a8a19a428378581a0d5c7dc01d86b5ec7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999871"
---
# <a name="define-coverage-rules-for-items"></a>تحديد قواعد تغطية للأصناف

[!include [banner](../../includes/banner.md)]

شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF. يوضح هذا الإجراء كيفية إنشاء قواعد التغطية وتجاوز إعدادات التغطية لصنف معين. كما يوضح كيفية تعيين إعدادات المخزون الافتراضية.


## <a name="create-a-coverage-group"></a>إنشاء مجموعة تغطية
1. انتقل إلى **إلى جزء التنقل > الوحدات النمطية > التخطيط‏‎ الرئيسي > الإعداد > مجموعات التغطية**.
2. انقر فوق **جديد**.
3. في الحقل **مجموعة التغطية**، اكتب قيمة.
4. في الحقل **الاسم**، اكتب قيمة.
5. في الحقل **التقويم**، اكتب قيمة. اختر التقويم الذي يستخدمه التخطيط الرئيسي لإنشاء اقتراحات التزويد للعناصر في هذه المجموعة.  
6. في الحقل **كود التغطية**، حدد خيارًا. حدد "متطلب" لهذا الإجراء.  
7. في الحقل **الحد الزمني للتغطية (بالأيام)**، أدخل "90". للعناصر الموجودة في هذه المجموعة، سوف ينشئ التخطيط الرئيسي اقتراحات التزويد لغاية 90 يومًا في المستقبل.  
8. في الحقل **الأيام السالبة‬**، أدخل "1".
9. في الحقل **الأيام الموجبة‬**، أدخل "1".
10. قم بتوسيع أو طي القسم **غير ذلك**.
11. ضمن القسم **هوامش الضمان بالأيام‬**، في الحقل **استلام الهامش المضاف إلى تاريخ المتطلبات**، ادخل '1'. على سبيل المثال، إذا تم تعيين هامش الاستلام على يوم واحد وتمت جدولة بند أمر شراء لاستلامه في 15 مايو، فسيحسب التخطيط الرئيسي تاريخ الاستلام المعدل باعتباره 16 مايو.  
12. في الحقل **إصدار الهامش المقتطع من تاريخ المتطلبات**، أدخل "1". على سبيل المثال، إذا تم تعيين حد الأمان‬ على يوم واحد وتمت جدولة بند أمر مبيعات للتسليم في 15 مايو، فستحسب الجدولة الرئيسية تاريخ التسليم المعدل باعتباره 14 مايو.  
13. في الحقل **تمت إضافة ‏‫هامش حد الطلب‬ إلى وقت إنتاج الصنف**‬، أدخل "1".
14. انقر فوق **حفظ**.

## <a name="create-a-new-product"></a>إنشاء منتج جديد
1. ‏‫انتقل إلى ‬**جزء التنقل > الوحدات > إدارة معلومات المنتج > المنتجات > المنتجات الصادرة‬** .
2. انقر فوق **جديد**.
3. في الحقل **رقم المنتج**، اكتب قيمة.
4. في الحقل **اسم المنتج**، اكتب قيمة.
5. في الحقل **مجموعة نماذج الصنف**، انقر فوق زر القائمة المنسدلة لفتح البحث.
6. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
7. في القائمة، انقر فوق الارتباط في الصف المحدد.
8. في الحقل **مجموعة الأصناف‬‬‬**، انقر فوق زر القائمة المنسدلة لفتح البحث.
9. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
10. في القائمة، انقر فوق الارتباط في الصف المحدد.
11. في الحقل **مجموعة أبعاد التخزين**، انقر فوق زر القائمة المنسدلة لفتح البحث.
12. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
13. في القائمة، انقر فوق الارتباط في الصف المحدد.
14. في الحقل **مجموعة أبعاد التعقب**‬، انقر فوق زر القائمة المنسدلة لفتح البحث.
15. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
16. في القائمة، انقر فوق الارتباط في الصف المحدد.
17. انقر فوق **موافق**.

## <a name="setup-default-order-settings"></a>إعداد إعدادات الأوامر الافتراضية
1. في **جزء الإجراءات**، انقر فوق **الخطة**.
2. ضمن **إعدادات الأوامر‬**، انقر فوق **إعدادات الأوامر الافتراضية‬**.
3. ضمن **أمر الشراء**، في حقل **الموقع الافتراضي**، اكتب الموقع المستخدم كافتراضي عند إنشاء أوامر الشراء.
4. في الحقل **المستودع الافتراضي‬**‬، اكتب الموقع الذي سيتم تخزين الصنف فيه.
5. قم بتوسيع أو طي قسم **المخزون**.
6. في الحقل **متعدد‬**، اكتب "10".
7. في الحقل **الحد الأدنى لكمية الطلب**، اكتب "10".
8. في الحقل **الحد الأقصى لكمية الطلب‏‎**، اكتب "100".
9. في الحقل **كمية الطلب القياسية‬**، اكتب "10".
10. في الحقل **الحد الأدنى لوقت إنتاج المشتريات**‬، أدخل رقمًا.
11. حدد خانة الاختيار **أيام العمل** أو قم بإلغاء تحديدها.
12. انقر فوق **حفظ**.
13. في الحقل **نوع الأمر الافتراضي**، حدد "أمر شراء".
14. انقر فوق **حفظ**.
15. قم بإغلاق الصفحة. قم بإغلاق صفحة ‏‫"إعدادات الأوامر الافتراضية".  

## <a name="add-an-item-to-a-coverage-group"></a>إضافة صنف إلى مجموعة تغطية
1. قم بتوسيع أو طي قسم **الخطة**.
2. في الحقل **مجموعة التغطية**، انقر فوق زر القائمة المنسدلة لفتح البحث.
3. في القائمة، ابحث عن **مجموعة التغطية** التي أنشأتها.
4. في القائمة، انقر فوق الارتباط في الصف المحدد.

## <a name="create-item-coverage-rules"></a>إنشاء قواعد تغطية الصنف
1. في **جزء الإجراءات**، انقر فوق **الخطة**.
2. ضمن **التغطية**، انقر فوق **تغطية الصنف‬**.
3. انقر فوق **جديد**.
4. انقر فوق علامة التبويب **عام**.
5. حدد المربع على الرأس **تجاوز إعدادات مجموعة التغطية‬**.
6. في الحقل **الحد الزمني للتغطية (بالأيام)**، أدخل "60". على الرغم من أن التخطيط لمتطلبات الأصناف الموجودة في مجموعة التغطية يتم قبل 90 يومًا، سيتم التخطيط لهذا البند قبل 60 يومًا.  
7. في الحقل **الأيام السالبة‬**، أدخل "2".
8. في الحقل **الأيام الموجبة‬**، أدخل "2".
9. انقر فوق علامة التبويب **الحد الأدنى لوقت الإنتاج**.
10. حدد المربع على الرأس **الشراء**.
11. في الحقل **وقت الشراء**‬، أدخل "5".
12. انقر فوق **حفظ**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]