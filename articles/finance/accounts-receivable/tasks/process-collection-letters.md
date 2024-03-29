---
title: معالجة خطابات التحصيل
description: توضح هذه المقالة كيفية إنشاء وطباعة وترحيل خطابات التحصيل.
author: ShivamPandey-msft
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: fbca4acf30e2c58d8bb615d659b883b574a12aa7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909116"
---
# <a name="process-collection-letters"></a>معالجة خطابات التحصيل

[!include [banner](../../includes/banner.md)]

توضح هذه المقالة كيفية إنشاء وطباعة وترحيل خطابات التحصيل. تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a>إعداد تسلسل خطاب تحصيل بملف تعريف الترحيل
1. انتقل إلى **جزء التنقل > الوحدات النمطية‬ > عمليات التحصيل والائتمان‬ > الإعداد > ملفات تعريف ترحيل العملاء**.
2. انقر فوق **تحرير**.
3. حدد تسلسل خطاب التحصيل من القائمة المنسدلة. إذا كنت لا تريد إنشاء خطابات تحصيل للحركات باستخدام ملف تعريف الترحيل هذا، فاترك الحقل فارغًا.  
4. قم بتوسيع علامة التبويب **تقييدات الجداول**‬ لتغيير الطريقة التي تتم بها معالجة خطابات التحصيل. إذا تم تعيين هذا الحقل إلى **نعم**، فسيتم إنشاء خطابات التحصيل لملف تعريف الترحيل هذا.  

## <a name="create-collection-letters"></a>إنشاء خطابات تحصيل
1. انتقل إلى **جزء التنقل > الوحدات النمطية > الائتمان والتحصيلات‬ > خطاب التحصيل > إنشاء خطابات التحصيل**.
2. حدد أنواع الحركات التي سيتم تحصيل الخطابات لها. سيتم تضمين كافة الحركات المفتوحة لهذه الأنواع في الحساب.  
3. حدد خيارًا في حقل **خطاب التحصيل**.
4. في حقل **تاريخ خطاب التحصيل**، أدخل تاريخ خطاب التحصيل.
5. حدد ملف تعريف ترحيل إذا قمت بتغيير **استخدام ملف تعريف الترحيل من** إلى **تحديد**. هناك خياران لملفات تعريف الترحيل:   

   - **الحساب** – تستخدم ملف تعريف الترحيل الذي تم تعيينه لحساب العميل لكل إشعار فائدة.   
   - **تحديد** – استخدم ملف تعريف الترحيل الذي حددته في الحقل **ملف تعريف الترحيل**.  

6. وسّع القسم **السجلات المطلوب تضمينها**.
7. حدد **عامل تصفية**.
8. في حقل **المعايير**، أدخل معرّف العميل. على سبيل المثال، أدخل "US-001".
9. حدد **موافق**.
10. حدد **موافق**.

## <a name="print-collection-letters"></a>طباعة خطابات التحصيل
1. انتقل إلى **جزء التنقل > الوحدات النمطية > الائتمان والتحصيلات‬ > خطاب التحصيل > مراجعة خطابات التحصيل ومعالجتها‬**.
2. في حقل **الحالة**، حدد **تم إنشاؤه**.
3. في الحقل **مطبوع**، حدد **غير مطبوع**.
4. حدد **طباعة**.
5. حدد **إشعار خطاب التحصيل‬**.
6. في قسم **المعلمات**، أدخل تاريخ إيقاف الترحيلات.
7. قم بتوسيع القسم **السجلات المطلوب تضمينها‬** ثم أدخل تفاصيل إشعار خطاب التحصيل.
8. حدد **موافق** لطباعة خطاب التحصيل.
9. قم بترحيل خطاب التحصيل.

    1. حدد **ترحيل**.
    1. أدخل تاريخ الترحيل لخطاب التحصيل.
    1. وسّع القسم **السجلات المطلوب تضمينها**.
    1. حدد **موافق**.
    1. في حقل **الحالة**، حدد **مرحّل**.
    1. في الحقل **مطبوع**، حدد خيارًا.

## <a name="control-collection-letters-at-the-customer-level"></a>مراقبة خطابات التحصيل ومستوى العميل
إذا تم إعداد خطابات التحصيل على مستوى الحركة، فقد يتم إنشاء خطابات متعددة للعميل، استنادًا إلى تقادم الحركة. إذا ظهرت الحركات في تسلسلات خطابات مختلفة، فسيتم إنشاء خطابات تحصيل منفصلة لكل مجموعة من الحركات المستحقة للعميل. وبالتالي، قد يتلقى عميل فردي، على سبيل المثال، خطاب تحصيل للحركات التي استحقت منذ 60 يومًا وخطاب تحصيل للحركات التي استحقت منذ 90 يومًا. 

يقترن كل خطاب تحصيل بكود خطاب تحصيل. كما يقترن كود خطاب التحصيل بحركات فرديه ويُستخدم لتحديد الوقت الذي يجب أن يتم فيها إنشاء خطاب التحصيل التالي لكل حركة. على سبيل المثال، إذا كانت الحركة مستحقة منذ أكثر من 30 يومًا، فإن كود خطاب التحصيل يحدد أنه سيتم إرسال خطاب التحصيل التالي عندما تصبح الحركة مستحقة منذ 60 يومًا وذلك إذا لم يتم تسديدها قبل هذا الوقت. 

يمكن أيضًا إعداد خطابات التحصيل على مستوي العميل. وفي هذه الحال، يتم تعقب كود خطاب التحصيل لكل حركة، غير أن معالجة خطابات التحصيل سوف تستند إلى مستوى خطاب تحصيل فردي تم تخزينه للعميل. سيحتوى خطاب التحصيل الفردي على جميع الحركات المستحقة للعميل. نظرًا لتعقب أيام السماح الآن على مستوى العميل، لن يتم إرسال خطاب التحصيل التالي إلا بعد انقضاء أيام السماح لخطاب التحصيل التالي في التسلسل، حتى لو أصبحت الحركات مستحقة بعد إرسال خطاب التحصيل الأخير. يساعد هذا الخيار على خفض عدد خطابات التحصيل التي يجب إرسالها إلى كل عميل,

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a>إعداد العميل لمراقبة التحصيل ومستوى العميل
1.  انتقل إلى **جزء التنقل > الوحدات النمطية > عمليات التحصيل والائتمان‬ > الإعداد > محددات الحسابات المدينة‬** وحدد علامة تبويب **التحصيلات**. 
2.  غيّر قيمة **إنشاء خطاب تحصيل لكل‬** إلى **عميل**. 
3.  انتقل إلى **جزء التنقل > الوحدات النمطية > الائتمان والتحصيلات‬ > خطاب التحصيل > مراجعة خطابات التحصيل ومعالجتها‬**. سيتم إنشاء خطاب تحصيل واحد فقط لعميل مع جميع الحركات المستحقة.

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a>تجاهل المدفوعات والإشعارات الدائنة عند حساب كود خطاب التحصيل
إذا قمت بتضمين المدفوعات والإشعارات الدائنة في الحركات التي سيتم تضمينها في خطابات التحصيل، قد يكون لديك مدفوعات وإشعارات دائنة ستؤدي إلى تشغيل حساب تحصيل. يمكنك التحكم في كيفية قيام المدفوعات والإشعارات الدائنة بالتحكم في كود خطاب التحصيل عن طريقة تغيير القيمة في المعلمة **تجاهل المدفوعات والإشعارات الدائنة عند حساب كود خطاب التحصيل‬**. 

لتجاهل المدفوعات والإشعارات الدائنة عند حساب كود خطاب التحصيل، قم بما يلي:

1. انتقل إلى **جزء التنقل > الوحدات النمطية > عمليات التحصيل والائتمان‬ > الإعداد > محددات الحسابات المدينة‬** وانقر فوق علامة تبويب **التحصيلات**. 
2. قم بتغيير قيمة **تجاهل المدفوعات والإشعارات الدائنة عند حساب كود خطاب التحصيل** إلى **نعم**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
