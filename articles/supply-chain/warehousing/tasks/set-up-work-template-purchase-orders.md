---
title: إعداد قالب عمل لأوامر الشراء
description: يصف هذا الموضوع كيفية إعداد قالب عمل بسيط لاستخدامه عند تخزين الأصناف المستلمة.
author: ShylaThompson
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e9acf6db9138a009527c6662f1cbb7e5fedc8778
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976853"
---
# <a name="set-up-a-work-template-for-purchase-orders"></a>إعداد قالب عمل لأوامر الشراء

[!include [banner](../../includes/banner.md)]

يصف هذا الموضوع كيفية إعداد قالب عمل بسيط لاستخدامه عند تخزين الأصناف المستلمة. تحدد قوالب العمل مجموعة الإرشادات المقدمة إلى عامل المستودع على جهاز محمول عند نقل الأصناف من منطقة الاستلام. يمكنك استخدام هذا الإجراء مع البيانات المذكورة في شركة بيانات العرض التوضيحي USMF. قبل تشغيل هذا الدليل، قم بإنشاء معرف وعاء عمل. في هذا المثال، يُستخدم معرف وعاء عمل يتم استدعاؤه في "الوارد". هذا الإجراء مخصص لمدير المستودعات.

1. في جزء التنقل، انتقل إلى **الوحدات النمطية > إدارة المستودعات > الإعداد > العمل > قوالب العمل**.
2. في الحقل **نوع أمر العمل**، حدد **أوامر الشراء**.

## <a name="create-a-work-template-header"></a>إنشاء رأس قالب عمل
1. حدد **جديد**.
2. الرقم التسلسلي **الرقم التسلسلي**، أدخل رقمًا. هذا هو التسلسل الذي يتم من خلاله تقييم قوالب العمل. يمكنك أيضا تعديل التسلسل، إذا لزم الأمر.  
3. في الحقل **قالب العمل**، اكتب قيمة. هذا هو المعرف الفريد لهذا القالب.  
4. في الحقل **وصف قالب العمل**، اكتب قيمة.
    - لن يتم تحديد الخيار **صالح** حتى تُكمل جميع المعلومات التي يحتاجها القالب ثم تنقر فوق **حفظ**.  
    - لا يمكن معالجة أمر عمل من النوع **أمر شراء** تلقائيًا، وبالتالي اترك الخيار **المعالجة تلقائيًا** معينًا على **لا**.  
5. في الحقل **معرف وعاء العمل**، اكتب قيمة. تتيح لك معرفات أوعية العمل تنظيم العمل في مجموعات. ستكون القيمة التي تعينُها هنا هي القيمة الافتراضية لأي عمل يتم إنشاؤه باستخدام هذا القالب.  
6. في الحقل **أولوية العمل**، أدخل `1`. ويشير هذا إلى أهمية العمل، وستكون القيمة التي تقوم تعينُها هنا هي القيمة الافتراضية لأي عمل يتم إنشاؤه باستخدام هذا القالب.  
7. حدد **حفظ**. يجب حفظ رأس القالب قبل يصبح الزر **تحرير الاستعلام** متوفرًا.  

## <a name="set-up-the-query-for-the-work-template"></a>إعداد الاستعلام الخاص بقالب العمل
1. حدد **تحرير الاستعلام**. سنقوم بتعيين قيد بحيث لا يمكن استخدام القالب إلا في مستودع معين.  
2. حدد **إضافة**.
3. في حقل **الحقل** على الصف الجديد، اكتب `warehouse`‬.
4. في الحقل **المعايير**، اكتب قيمة.
5. حدد **موافق**.
6. حدد **نعم**.

## <a name="set-work-template-details"></a>تعيين تفاصيل قالب العمل
1. حدد **جديد**.
2. في الحقل **نوع العمل**، حدد **انتقاء**.
3. في الحقل **معرف فئة العمل**، اكتب `purchase`. ستكون فئة العمل التي تعينها هنا هي الفئة الافتراضية بجميع بنود العمل من النوع "الانتقاء" التي يتم إنشاؤها باستخدام هذا القالب. لا يمكن إلغاء فئة العمل من بنود أمر العمل. تُستخدم فئات العمل لتوجيه و/أو الحد من نوع بنود أوامر العمل التي يستطيع عامل مستودع معالجتها باستخدام جهاز محمول.  
4. حدد **جديد**.
5. في الحقل **نوع العمل**، حدد **تم وضعه**.
6. في الحقل **معرف فئة العمل**، اكتب قيمة. تكون إرشادات الانتقاء والوضع مجموعة. يجب أن تتضمن كل مجموعة انتقاء/وضع نفس فئة العمل. استخدم نفس فئة العمل التي قمت بتوفيرها لإرشادات الانتقاء.  
7. حدد **حفظ**. لاحظ أن خانة الاختيار **صالح** أصبحت محددة الآن.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]