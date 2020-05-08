---
title: تزويد Human Resources
description: يستعرض هذا المقال عملية توفير بيئة إنتاج جديدة لتطبيق Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 88a0be50a9b861190e7ce9b3f56bb4e583b791d1
ms.sourcegitcommit: 33685a5cc37081a189279e917def7f122d3beaef
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/24/2020
ms.locfileid: "3285479"
---
# <a name="provision-human-resources"></a>تزويد Human Resources

يستعرض هذا المقال عملية توفير بيئة إنتاج جديدة لتطبيق Microsoft Dynamics 365 Human Resources. يفترض هذا المقال أنك قمت بشراء Human Resources من خلال اتفاقية هندسة مؤسسة (EA) أو موفر حلول مجموعة (CSP). إذا كان لديك ترخيص Microsoft Dynamics 365 يتضمن خطة خدمة Human Resources، ولا يمكنك إتمام الخطوات المذكورة في هذا المقال، فاتصل بالدعم.

للبدء، يجب على المسؤول العمومي تسجيل الدخول إلى [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) وإنشاء مشروع Human Resources جديد. ما لم يكن إصدار ترخيص يمنعك من توفير Human Resources، فلا يلزم طلب مساعدة من الدعم أو ممثلي هندسة خدمة Dynamics (DSE).

## <a name="create-an-lcs-project"></a>إنشاء مشروع LCS

لاستخدام LCS لإدارة بيئات Human Resources، يجب أولاً إنشاء مشروع LCS.

1. قم بتسجيل الدخول إلى [LCS](https://lcs.dynamics.com/Logon/Index) باستخدام الحساب الذي استخدمته للاشتراك في Human Resources.

2. حدد علامة زائد (**+**) لإنشاء مشروع.

3. حدد **Microsoft Dynamics 365 Human Resources** كاسم المنتج وإصدار المنتج.

4. حدد منهجية **Dynamics 365 Human Resources**.

5. حدد **إنشاء**.

لمزيد من المعلومات حول كيفية الشروع في العمل مع Human Resources، راجع منهجية **Human Resources** التي قمت بإنشائها في المشروع الجديد الخاص بك. بعد الانتهاء من إنشاء المشروع، أكمل الإجراء التالي لتوفير بيئة Human Resources الخاصة بك.

## <a name="provision-a-human-resources-project"></a>توفير مشروع Human Resources

بعد إنشاء مشروع LCS، يمكنك توفير Human Resources في بيئة.

1. في مشروع LCS، حدد تجانب **"إدارة تطبيق Human Resources**.

2. حدد ما إذا كانت هذه البيئة مثيلا لوضع حماية أو مثيل إنتاج لـ Human Resources. قد تتوفر ميزات المعاينة المبكرة في مثيلات وضع الحماية للسماح بالردود والاختبار في وقت مبكر.
   
    > [!NOTE]
    > لا يمكن تغيير نوع مثيل Human Resources بمجرد تعيينه. تحقق من تحديد نوع المثيل الصحيح قبل المتابعة.</br></br>
    > يعد نوع مثيل Human Resources منفصلاً عن نوع مثيل بيئة Microsoft Power Apps ، الذي قمت بتعيينه في مركز إدارة Power Apps .
    
3. حدد الخيار **تضمين بيانات العرض التوضيحي** إذا كنت تريد أن تتضمن بيئتك مجموعة بيانات العرض التوضيحي نفسها المستخدمة في تجربة اختبار إصدار Human Resources. تكون بيانات العرض التوضيحي مفيدة في العرض التوضيحي طويل الأمد أو بيئات التدريب، ويجب إلا يتم أبدًا استخدامها في بيئات الإنتاج. يجب أن تحدد هذا الخيار عند النشر الأولى. لا يمكنك تحديث نشر موجود في وقت لاحق.

4. يتم توفير Human Resources دومًا في بيئة Microsoft Power Apps ، لتمكين تكامل Power Apps وقابليته للتوسع. راجع قسم "تحديد بيئة Power Apps " في هذا المقال قبل المتابعة. إذا لم تكن لديك بيئة Power Apps ، فحدد "إدارة البيئات" في LCS أو انتقل إلى مركز إدارة Power Apps . ثم اتبع الخطوات التي تؤدي إلى [إنشاء بيئة Power Apps .](https://docs.microsoft.com/powerapps/administrator/create-environment).

5. حدد البيئة المراد توفير Human Resources فيها.

6. حدد **نعم** للموافقة على الشروط وبدء النشر.

   تظهر بيئتك الجديدة في قائمة البيئات في جزء التنقل على الجانب الأيسر. ومع ذلك، لا يمكنك البدء في استخدام البيئة حتى يتم تحديث حالة النشر إلى **تم النشر**. تستغرق هذه العملية عادةً دقائق معدودة. إذا لم تنجح عملية التوفير، فيجب الاتصال بالدعم.

7. حدد **تسجيل الدخول إلى Human Resources** لاستخدام بيئتك الجديدة.

    > [!NOTE]
    > إذا لم تكن قد وافقت على المتطلبات النهائية بعد، فيمكنك نشر مثيل اختبار Human Resources في المشروع. يمكنك بعد ذلك استخدام هذا المثيل لاختبار الحل الخاص بك قبل إبداء الموافقة. إذا كنت تستخدم بيئتك الجديدة للاختبار، فيجب تكرار هذا الإجراء لإنشاء بيئة إنتاج.

    > قد تفكر في الاستفادة من [بيئة الإصدار التجريبي لـ Human Resources](https://go.microsoft.com/fwlink/p/?LinkId=2115962) المجانية لمدة 60 يومًا. على الرغم من أن البيئة التجريبية مملوكة من قبل المستخدم الذي طلبها، إلا أنه يمكن دعوة مستخدمين آخرين من خلال تجربة إدارة النظام لـ Human Resources. تحتوي البيئات التجريبية على بيانات خيالية يمكن استخدامها لاستكشاف البرنامج بطريقة آمنة. وهي غير مخصصة لاستخدام كبيئات إنتاج. لاحظ أنه عند انتهاء صلاحية البيئة التجريبية بعد 60 يومًا، ستُحذف كل البيانات الموجودة بداخلها ولا يمكن استردادها. يمكنك التسجيل للحصول على بيئة تجريبية جديدة بعد انتهاء مدة صلاحية البيئة الحالية.

## <a name="select-a-power-apps-environment"></a>تحديد بيئة Power Apps 

يمكنك دمج وتوسيع استخدام بيانات Human Resources باستخدام أدوات Power Apps. لمزيد من المعلومات حول بيئات Power Apps ، بما في ذلك نطاق البيئة، والوصول إلى البيئة، وإنشاء واختيار بيئة، راجع [الإعلان عن بيئات Power Apps .](https://powerapps.microsoft.com/blog/powerapps-environments/). 

استخدم الإرشادات التالية عند تحديد بيئة Power Apps لنشر Human Resources في: 

1. في LCS، حدد **إدارة البيئات**. يمكنك أيضًا الانتقال مباشرة إلى مركز مسؤول Power Apps ، حيث يمكنك عرض البيئات الموجودة وإنشاء بيئات جديدة.

2. تم تعيين بيئة Human Resources واحدة لبيئة Power Apps واحدة.

3. تحتوي بيئة Power Apps على Human Resources، إلى جانب تطبيقات Power Apps ، وPower Automate، وCommon Data Service. إذا تم حذف بيئة Power Apps، لذا توجد التطبيقات داخله. عند تزويد بيئة Human Resources، يمكن تزويد إما بيئة **الإصدار التجريبي** أو **الإنتاج** . اختر نوع البيئة استنادًا إلى كيفية استخدام البيئة. 

4. يجب مراعاة استراتيجيات الاختبار وتكامل البيانات، مثل بيئة الاختبار المعزولة أو اختبار قبول المستخدم (UAT)‬ أو الإنتاج. فكر بعناية في مختلف الدلالات التي ستترتب على عملية النشر، لأنه من الصعب تغيير بيئة Human Resources المعينة إلى بيئة Power Apps.

5. لا يمكنك استخدام بيئات Power Apps التالية لـ Human Resources. وتتم تصفيتها من قائمة التحديد في LCS:
 
    - **بيئات Power Apps الافتراضية** - بينما يتم تزويد كل مستأجر تلقائيًا ببيئة Power Apps افتراضية، لكن لا نوصي باستخدامها مع Human Resources. يمكن لجميع المستخدمين المستأجرين الوصول إلى بيئة Power Apps ويمكنهم إتلاف بيانات الإنتاج بدون قصد عند الاختبار والاكتشاف مع تكاملات Power Apps أو Power Automate.
   
    - **البيئات التجريبية** - يتم إنشاء هذه البيئات بتاريخ انتهاء الصلاحية. وعند انتهاء الصلاحية، تتم إزالة البيئة الخاصة بك وأي مثيلات لـ Human Resources المضمنة فيه تلقائيًا.
   
    - **المناطق غير المدعومة** - يتم حاليًا دعم Human Resources فقط في المناطق التالية: الولايات المتحدة وأوروبا والمملكة المتحدة وأستراليا وكندا وآسيا.

    > [!NOTE]
    > يتم توفير بيئة Human Resources في نفس المنطقة التي يتم توفير بيئة Power Appsفيها. ترحيل بيئة Human Resources إلى منطقة أخرى غير معتمدة.

6. بعد تحديد البيئة الصحيحة التي تريد استخدامها، يمكنك متابعة عملية التوفير. 
 
## <a name="grant-access-to-the-environment"></a>منح الوصول إلى البيئة

بشكل افتراضي، يتمتع المسؤول العمومي الذي أنشأ البيئة بحق الوصول إليها. يجب عليك منح حق الوصول بشكل واضح إلى مستخدمي التطبيق الإضافيين. ويجب أن تضيف المستخدمين وتعين الأدوار المناسبة لهم في بيئة Human Resources. يجب أيضًا على المسؤول العمومي الذي نشر Human Resources تشغيل تطبيقات Attract وOnboard لإكمال التهيئة وتمكين الوصول لمستخدمي شبكة الاتصال المستأجرة الأخرىن. وحتى حدوث ذلك، لن يتمكن المستخدمون الآخرون من الوصول إلى تطبيقات Attract وOnboard وسوف يحصلون على خطأ مخالفة الوصول. للحصول على مزيد من المعلومات، راجع [إنشاء مستخدمين جدد](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) و[تعيين مستخدمين إلى أدوار أمان](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 
