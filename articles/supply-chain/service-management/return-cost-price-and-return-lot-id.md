---
title: سعر تكلفة الإرجاع وكود شحنة الإرجاع
description: قد تحتاج إلى أن تكون التكلفة للمنتجات المرتجعة تساوي التكلفة للمنتجات في وقت بيع المنتجات للعميل. يمكنك القيام بذلك باستخدام **كود شحنة الإرجاع**.
author: sorenva
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnInventTransIdLookup, ReturnItemNumLookup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4c1d236918eddf3203a544a6b047f8ccac777971
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/15/2022
ms.locfileid: "9017229"
---
# <a name="return-cost-price-and-return-lot-id"></a>سعر تكلفة الإرجاع وكود شحنة الإرجاع        

[!include [banner](../includes/banner.md)]



يتم حساب التكلفة للمنتجات التي يتم إرجاعها إلى المخزون باستخدام التكلفة الحالية للمنتجات. مع ذلك، قد تحتاج إلى أن تكون التكلفة للمنتجات المرتجعة تساوي التكلفة للمنتجات في وقت بيع المنتجات للعميل. يمكنك القيام بذلك باستخدام حقل **كود شحنة الإرجاع** في علامة التبويب السريعة **تفاصيل بند** في النموذج **أمر المبيعات**.

فكر في السيناريو التالي على سبيل المثال. أن تقوم بعمل فاتورة لعميل. وبعد ذلك، قام العميل بإرجاع المنتجات التي تم تسليمها لك. وأنت أرجعت المنتجات إلى المخزون. في هذه الحالة، عندما تقوم برد ثمن المنتجات المرتجعة إلى العميل، يتم حساب التكلفة لتلك المنتجات باستخدام التكلفة الحالية للمنتجات. ومع ذلك، إذا قمت باستخدام حقل **كود شحنة الإرجاع**، يتم حساب التكلفة للمنتجات المرتجعة باستخدام التكلفة في فاتورة البيع الأصلي إلى العميل.

لاستخدام تكلفة أخرى غير التكلفة الحالية للمرتجعات من عميل، استخدم إحدى الطرق التالية.

## <a name="method-1-manually-enter-the-return-cost-price"></a>الطريقة الأولى: إدخال سعر تكلفة الإرجاع يدوياً

بشكل افتراضي، عندما تقوم بإضافة أصناف إلى أمر إرجاع، يتم إرجاع الأصناف إلى المخزون بسعر التكلفة الحالي. لتحديد سعر تكلفة إرجاع مختلف، اتبع هذه الخطوات.

1.  انقر فوق **المبيعات والتسويق** \> **مرتجعات المبيعات‬** \> **جميع أوامر الإرجاع**.

2.  في **جزء الإجراءات**، في المجموعة **جديد**، انقر فوق **أمر إرجاع**.

3.  في نموذج **إنشاء أمر إرجاع**، حدد حساب عميل ومن ثم انقر فوق **موافق**.

4.  في النموذج **أمر الإرجاع - رقم ترخيص المواد المسترجعة: %1, %2**، حدد أحد الأصناف ومن ثم أدخل كمية سالبة في حقل **الكمية‏‎**.

5.  انقر فوق علامة التبويب السريعة **تفاصيل البند**.

6.  من علامة التبويب **عام**، حدد قيمة في الحقل **سعر تكلفة الإرجاع**. يتم استخدام هذه القيمة عند إرجاع البضائع إلى المخزون. إذا لم تقم بإدخال قيمة، يتم استخدام سعر التكلفة الحالي عند إرجاع البضائع إلى المخزون.

## <a name="method-2-automatically-generate-the-cost-price-based-on-the-customer-invoice-line"></a>الطريقة الثانية: إنشاء سعر التكلفة تلقائيًا وفقا لبند فاتورة العميل

هذه هي الطريقة المفضل استخدامها لإنشاء بنود الإرجاع. لاستخدام تكلفة المنتجات في قت بيع المنتجات للعميل، قم بإنشاء أمر إرجاع وحدد بند مبيعات للإرجاع.

1.  انقر فوق **المبيعات والتسويق** \> **مرتجعات المبيعات‬** \> **جميع أوامر الإرجاع**.

2.  في **جزء الإجراءات**، في المجموعة **جديد**، انقر فوق **أمر إرجاع**.

3.  في نموذج **إنشاء أمر إرجاع**، حدد حساب عميل ومن ثم انقر فوق **موافق**.

4.  في النموذج **أمر الإرجاع - رقم ترخيص المواد المسترجعة: %1, %2**، في **جزء الإجراءات**، انقر فوق **العثور على أمر المبيعات‬**.

5.  في النموذج **العثور على أمر المبيعات‬**، حدد بند الفاتورة للإرجاع، ثم انقر فوق **موافق**.
    
    في علامة التبويب السريعة **تفاصيل البند**، في علامة التبويب **عام**، يتم عرض حقل **كود شحنة الإرجاع** من بند المبيعات الأصلي. بالإضافة إلى ذلك، يعرض **سعر تكلفة الإرجاع** قيمة التكلفة من بند المبيعات الأصلي.

## <a name="cost-calculation-example"></a>مثال حساب التكلفة

عندما تستخدم حقل **كود شحنة الإرجاع** في بند أمر إرجاع لتحديد سعر تكلفة الإرجاع، يتم استخدام التكلفة في بند أمر الإرجاع. إذا قمت بتشغيل وظيفة إقفال أو إعادة حساب المخزون، يتم تعديل التكلفة في بند المبيعات الأصلي. يتم تعطيل التكلفة في بند أمر الإرجاع تلقائياً لتعكس نفس التكلفة لكل قطعة.

1.  قم بإنشاء وإصدار منتج الذي يسمى Test. في نموذج **‏‫تفاصيل المنتج الذي تم إصداره‬**، حدد المعلومات التالية:
    
    1.  في علامة التبويب السريعة **إدارة التكاليف**، في حقل **مجموعة الأصناف**، حدد مجموعة **أجزاء**.
    
    2.  في علامة التبويب السريعة **عام**، في الحقل **مجموعة نماذج الصنف‬**، حدد **DEF**.
    
    3.  في علامة التبويب السريعة **شراء**، في حقل **السعر** اكتب 10.00 كسعر تكلفة للبند.
    
    4.  في **جزء الإجراءات**، انقر فوق **مجموعات الأبعاد**. في حقل **مجموعة أبعاد التخزين**، حدد **الموقع والمستودع فقط**. في حقل **مجموعة أبعاد التعقب**، حدد **بدون أبعاد التعقب النشطة**.

2.  قم بإنشاء أمر شراء لـ 10 قطع من الصنف Test بسعر 6.00 لكل قطعة، وقم بترحيل فاتورة لأمر الشراء.
    
    قم بإنشاء أمر شراء ثان لـ 10 قطع من الصنف Test بسعر 8.00 لكل قطعة، وقم بترحيل فاتورة لأمر الشراء.

3.  قم بترحيل فاتورة لأمر المبيعات لبيع خمسة أجزاء من العنصر Test.
    
    في هذه الحالة، يتم تحديد تكلفة بند أمر المبيعات بسعر 35.00 (خمس قطع \* 7.00 متوسط التكلفة لكل قطعة).

4.  قم بإنشاء أمر إرجاع للعميل. في النموذج **العثور على أمر المبيعات‬**، حدد بند الفاتورة، ثم انقر فوق **موافق**.

5.  في النموذج **أمر الإرجاع - رقم ترخيص المواد المسترجعة: %1, %2**، تحقق من إنشاء أمر إرجاع لإرجاع الصنف Test. تم تعيين كمية أمر الإرجاع على 5.00.
    
    يعرض حقل **كود شحنة الإرجاع** معرف الشحنة. يتم استخدام رقم الشحنة هذا من أمر المبيعات الأصلي الخاص بالصنف الذي تم بيعه للعميل. يعرض **سعر تكلفة الإرجاع** سعر التكلفة من بند المبيعات الأصلي.

6.  سجل استلام الأصناف المرجعة.

7.  قم بترحيل كشف تعبئة للأصناف المرتجعة.

8.  قم بترحيل فاتورة لأمر الإرجاع. في صفحة قائمة **كافة أوامر المبيعات**، حدد أمر توريد الذي يكون نوع الأمر له **‏‫الأمر المرجع‬**.

9.  افتح نموذج **حركات المخزون**. تحقق من تحديد تكلفة الإرجاع بسعر 7.00 لكل جزء باستخدام القيمة الموجودة في حل **سعر تكلفة الإرجاع**، بمجموع 35.00 في حقل **مبلغ التكلفة**. يمكنك فتح نموذج **حركات المخزون** من النموذج **أمر الإرجاع - رقم ترخيص المواد المسترجعة: %1, %2**. في الشبكة **بنود**، انقر فوق **مخزون** \> **حركات**.

10. في إدارة المخزون والمستودعات، استخدم نموذج **الإقفال والتعديل** لتشغيل الإجراء **3. الإغلاق**.
    
    يعدل هذا الإجراء التكلفة في بند المبيعات الأصلي الذي تم تحديد تكلفة بسعر 35.00 (5 قطع \*7.00) إلى-30.00 (5 قطع \*6.00). نظرًا لأن مجموعة نموذج المخزون تستخدم قاعدة "ما يدخل أولاً يخرج أولاً" (FIFO)، وسعر 6.00 لكل قطعة هو تكلفة FIFO من أمر الشراء الأول. بالإضافة إلى ذلك، يعدل الإجراء التكلفة في بند مبيعات الإرجاع لتطابق التكلفة لكل قطعة في بند المبيعات الأصلي. لذلك، يتم تعديل تكلفة بند الإرجاع من 35.00 إلى 30.00.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]