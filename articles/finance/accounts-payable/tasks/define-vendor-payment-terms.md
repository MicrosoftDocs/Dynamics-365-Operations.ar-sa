---
title: ‏‫تحديد شروط دفع المورد
description: توضح هذه المقالة كيفية إعداد شروط الدفع لفواتير المورّدين.
author: abruer
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a676856ed43bf1b78684eac0682e0fdef9c84083
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906460"
---
# <a name="define-vendor-payment-terms"></a>‏‫تحديد شروط دفع المورد

[!include [banner](../../includes/banner.md)]

توضح هذه المقالة كيفية إعداد شروط الدفع لفواتير المورّدين. تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.

1. انتقل إلى **جزء التنقل > الوحدات النمطية > الحسابات المدينة > إعداد الدفع‬ > شروط الدفع**.
2. حدد **جديد**. تُستخدم صفحة **شروط الدفع** لتعريف الطريقة التي سيتم بها حساب تاريخ الاستحقاق. ولا تستخدم هذه الصفحة لتعريف كيف سيتم حساب تاريخ الخصم النقدي.  
3. في حقل **شروط الدفع**، اكتب قيمة.
4. في حقل **الوصف**، اكتب قيمة.
5. في الحقل **الأيام**، أدخل رقمًا. سيستخدم الرقم الذي تم إدخاله هنا لإضافته إلى تاريخ الاستحقاق، أو إلى نهاية الفترة المحددة في **طريقة الدفع**. على سبيل المثال، إذا قمت بتحديد **الصافي**، فسيضاف الرقم إلى تاريخ الاستحقاق. أما إذا حددت **الشهر الحالي**، فسيُضاف الرقم إلى اليوم الأخير من الشهر الحالي لحساب تاريخ الاستحقاق.  
6. حدد **حفظ**.
7. قم بإغلاق الصفحة.
8. انتقل إلى **الحسابات المدينة > إعداد الدفع > الخصومات النقدية**‬‬.
9. حدد **جديد**.
10. في الحقل **الخصم النقدي**، أدخل معرفًا.
11. في حقل **الوصف**، اكتب قيمة.
12. إذا قدم المورّد خصمًا متدرجًا، فحدد الخصم النقدي التالي بعد انتهاء مدة صلاحية الحالي.
13. قم بإغلاق الصفحة.
14. في الحقل **الأيام**، أدخل رقمًا. سيتم استخدام الكمية المدخلة في حقل **الأيام** لحساب **تاريخ الخصم النقدي**، استنادًا إلى الخيار الذي تم تحديده في الحقل **الصافي/الحالي**‬. إذا تم تحديد **الصافي**، فستضاف الكمية إلى تاريخ الفاتورة لتحديد تاريخ الخصم النقدي. إذا تم تحديد **الشهر الحالي**، فستضاف الكمية إلى نهاية الشهر الحالي لتحديد تاريخ الخصم النقدي.  
15. أدخل النسبة المئوية للخصم النقدي في حقل **الخصم**. 
16. أدخل الحساب الرئيسي الذي سيتم ترحيل الخصم النقدي إليه لفواتير العميل، ثم أدخل الحساب الرئيسي الذي سيتم ترحيل الخصم النقدي إليه لفواتير المورّد. إذا تم تعيين **الحسابات المقابلة للخصومات** إلى **استخدام الحساب الرئيسي لخصم المورد**، فسيتم عندئذٍ استخدام الحساب الرئيسي. إذا تم تعيين الخيار إلى **الحسابات الموجودة في بنود الفاتورة**، فسيتم ترحيل الخصم النقدي إلى حسابات الأصول/المصروفات على بنود الفاتورة.  
17. حدد **حفظ**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
