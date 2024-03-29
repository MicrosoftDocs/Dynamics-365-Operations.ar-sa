---
title: إعداد عنصر قائمة جهاز محمول لإكمال عمل من النوع "أمر الشراء"
description: يوضح هذا المقال كيفية إعداد عنصر قائمة جهاز محمول.
author: Mirzaab
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFAutoConfirm, WHSRFMenu
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 09286e8e482780523b61006081205868be487755
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882275"
---
# <a name="set-up-a-mobile-device-menu-item-for-completing-work-of-type-purchase-order"></a>إعداد عنصر قائمة جهاز محمول لإكمال عمل من النوع "أمر الشراء"

[!include [banner](../../includes/banner.md)]

يوضح هذا المقال كيفية إعداد عنصر قائمة جهاز محمول. في هذا المثال، يتم استخدام عنصر القائمة لتنفيذ عمل من النوع "أمر الشراء". تحدد فئة العمل المرتبطة بعنصر القائمة العمل الصالح. ويمكنك استخدام هذا الدليل في شركة بيانات العرض التوضيحي USMF. يقوم مدير المستودع عادةً بتنفيذ هذا الإجراء.


## <a name="create-a-mobile-device-menu-item"></a>إنشاء عنصر قائمة جهاز محمول
1. انتقل إلى **عناصر قائمة الجهاز المحمول** وذلك بإدخالها في شريط البحث.
2. حدد **جديد**.
3. في الحقل **اسم عنصر القائمة‬**، اكتب قيمة. أدخل قيمة فريدة. على سبيل المثال، يمكنك كتابة `POMove`. تذكر القيمة، إذ ستحتاجها في وقت لاحق.  
4. في الحقل **العنوان**، اكتب قيمة. هذا هو المسمى الوظيفي الذي سيُعرض على الجهاز المحمول. على سبيل المثال، يمكنك كتابة `PO Move`.  
5. في الحقل **الوضع**، حدد **العمل**.
6. حدد **نعم** في الحقل **استخدام العمل الموجود**.
    - يتم استخدام عنصر قائمة الجهاز المحمول هذا لتنفيذ العمل الموجود. لذلك يجب تعيين هذه القيمة إلى **نعم**.  
    - يحدد حقل **عرض حالة المخزون** ما إذا كانت حالة المخزون للمخزون الفعلي ستظهر للعامل في المستودع على الجهاز المحمول.  
7. في الحقل **موجه بواسطة**، حدد **تجميع النظام**. عند تحديد شيء ما في الحقل **موجه بواسطة**‬، تظهر حقول إضافية في القسم **عام** في هذه الصفحة. تتوقف الحقول التي تظهر على ما قمت بتحديده. عندما تحدد **تجميع النظام**، يُضاف حقلان جديدان. سيرد شرح هذان الحقلان أدناه.  
8. في حقل **تجميع النظام**، حدد **WorkPoolId**. عند قيام العاملين في المستودع بفتح عنصر القائمة هذا، ستتم مطالبتهم بفحص معرف وعاء العمل‬. سيتم دفع كافة أوامر العمل التي لديها معرف وعاء العمل هذا وبنود أوامر العمل المفتوحة مع إحدى فئات العمل المضافة إلى عنصر القائمة هذا إلى المستخدم.  
9. في الحقل **تسمية تجميع النظام**، اكتب قيمة. هذا هو النص الذي سيتم عرضه للمستخدم على الجهاز المحمول. على سبيل المثال، يمكنك كتابة **وعاء العمل**.  
10. حدد **نعم** في الحقل **تجاوز لوحة الترخيص‬ أثناء التخزين**. يسمح هذا الخيار للعاملين في المستودع تجاوز لوحة الترخيص الهدف عندما يتم وضع الأصناف على موقع تتحكم به لوحة ترخيص.  
11. حدد **نعم** في الحقل **تخزين المجموعة**.
    - إذا كانت كافة بنود الوضع في أمر العمل تشارك الموقع نفسه، فسيتلقى المستخدم إرشادات وضع مدمجة لكافة البنود. 
    - معرف قالب التدقيق: يسمح لك معرف قالب التدقيق بتحديد وجوب مقاطعة عملية العمل لعنصر قائمة بحيث يمكن تنفيذ عملية أخرى. على سبيل المثال، إذا كان عنصر القائمة هذا للعمل الوارد، فقد يتطلب قالب التدقيق أن يتحقق العامل من درجة الحرارة. تم تحديد النقطة التي تمت عندها مقاطعة العملية على قالب التدقيق ويمكن أن تكون، على سبيل المثال، عند بدء العمل أو إكماله أو عند تغيير حالته.  
12. وسّع مقطع **فئات العمل**.
13. حدد **جديد**.
14. في الحقل **معرف فئة العمل**، اكتب `Purchase`. يقوم وعاء العمل بتقييد العمل الذي يمكن استخدام عنصر القائمة له. في هذه الحالة سيتم استخدامه لبنود أمر العمل المفتوح التي لديها معرف فئة العمل "شراء".  
15. حدد **حفظ**.

## <a name="set-up-work-confirmation"></a>إعداد تأكيد العمل
1. حدد **إعداد تأكيد العمل**.
2. في الحقل **نوع العمل**، حدد **انتقاء**.
3. حدد خانة الاختيار **تأكيد تلقائي**. سيتم تأكيد إرشادات العمل ذات نوع العمل "انتقاء" بشكل تلقائي. لن يتم تقديم هذه الإرشادات للمستخدم.  
4. حدد **جديد**.
5. في الحقل **نوع العمل، حدد تم وضعه**.
6. حدد خانة الاختيار **تأكيد الموقع**. ستتم مطالبة العامل في المستودع بإجراء فحص تأكيد للموقع، عندما يتم وضع الصنف.  
7. حدد **حفظ**.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>إضافة عنصر القائمة إلى قائمة جهاز محمول
1. انتقل إلى قائمة **الجهاز المحمول** وذلك بإدخالها في شريط البحث.
2. حدد **تحرير**.
3. استخدم عامل التصفية السريع للبحث عن السجلات. على سبيل المثال، قم بإجراء التصفية على حقل **الاسم** باستخدام قيمة **الوارد**. إنك تريد العثور على القائمة التي تستخدمها لعناصر القائمة الواردة. في USMF، يسمى ذلك **الوارد‬**.  
4. في الشجرة، حدد **قيمة**.
5. حدد السهم المتجه لليمين.
6. حدد **حفظ**.
7. قم بإغلاق الصفحة.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]