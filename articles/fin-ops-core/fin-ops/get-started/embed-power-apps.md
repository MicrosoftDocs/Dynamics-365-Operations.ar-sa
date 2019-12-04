---
title: تضمين Power Apps
description: يصف هذا الموضوع كيفية تضمين Power Apps في العميل لزيادة الأداء الوظيفي للمنتج.
author: jasongre
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: 755a30f89725ca0a7e1c14252984c617d6ba280e
ms.sourcegitcommit: 4162d9ef4239c9d4e5297b8aaa903dd54f9cafc3
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/21/2019
ms.locfileid: "2824483"
---
# <a name="embed-microsoft-power-apps"></a>تضمين Microsoft Power Apps

[!include [banner](../includes/banner.md)]

يدعم Platform update 14 التكامل مع Microsoft Power Apps، وهي عبارة عن خدمة للمطورين والمستخدمين غير التقنيين لإنشاء تطبيقات أعمال مخصصة للأجهزة المحمولة وأجهزة الكمبيوتر اللوحية والويب من دون كتابة تعليمة برمجية. ويمكن بعد ذلك تضمين Power Apps الذي طورته أنت أو مؤسستك أو النظام البيئي الأوسع في تطبيقات Finance and Operations لزيادة الأداء الوظيفي للمنتج. على سبيل المثال، قد تقوم بإنشاء Power App لتكملة تطبيقات Finance and Operations بالمعلومات التي تم استردادها من نظام آخر.

لمزيد من المعلومات حول تضمين Power Apps، شاهد مقطع الفيديو القصير [كيفية تضمين Power Apps](https://www.youtube.com/watch?v=x3qyA1bH-NY) video.

## <a name="adding-an-embedded-power-app-to-a-page"></a>إضافة Power App مضمن إلى صفحة

### <a name="overview"></a>نظرة عامة

قبل تضمين Power App في العميل، تحتاج أولاً إلى البحث عن Power App أو بنائه بواسطة المرئيات و/أو الوظيفة المطلوبة. لن نصف العملية التفصيلية لإنشاء Power App هنا. يعتبر الموضوع [مقدمة إلى Power Apps](https://docs.microsoft.com/powerapps/getting-started) نقطة بداية جيدة إذا كان استخدام Power Apps أمرًا جديدًا بالنسبة لك.

عندما تكون مستعدًا لدمج Power App محدد، يمكنك الاختيار من بين إحدى الطريقتين التاليتين للوصول إلى Power App في صفحة، أي الطريقتين أنسب للسيناريو الخاص بك. الطريقة الأولى هي استخدام الزر Power Apps الذي تمت إضافته إلى جزء الإجراءات القياسية. سوف تظهر Power Apps الذي التي تمت إضافتها باستخدام هذه الآلية كعناصر قائمة داخل زر القائمة Power Apps. عند تحديد كل عنصر من عناصر القائمة هذه، ستقوم بفتح جزءًا جانبيًا يحتوي على Power App المضمن. بدلاً من ذلك، يمكنك اختيار إظهار Power App مباشرةً على صفحة كعلامة تبويب جديدة، أو كعلامة تبويب سريعة، أو ريشة، أو كقسم جديد في مساحة عمل.

عند تكوين Power App المضمن، يمكنك تحديد حقل واحد تريد إرساله كإدخال إلى Power App. يتيح هذا لـ Power App أن يستجيب استنادًا إلى البيانات التي تقوم بعرضها حاليًا.

### <a name="details"></a>التفاصيل

تبين الإرشادات التالية كيفية تضمين Power App في عميل الويب.

1. انتقل إلى الصفحة التي تريد فيها تضمين Power App. ستكون هذه الصفحة نفس الصفحة التي تحتوي على أي بيانات يجب أن يتم تمريرها إلى Power App كإدخال.
2. افتح جزء **إدخال Power App**:

    - انقر فوق **خيارات**، ثم حدد **تخصيص هذا النموذج**. ضمن القائمة **إدراج**، اختر **Power App**. وأخيرًا، حدد المنطقة التي تريد فيها إضافة Power App. إذا كنت ترغب في تضمين Power App ضمن زر القائمة Power Apps، فاختر "جزء الإجراءات". إذا كنت ترغب في تضمين Power App مباشرةً في الصفحة، فاختر علامة التبويب المناسبة، أو علامة التبويب السريعة، أو الريشة، أو القسم (إذا كنت متصلاً بمساحة عمل).
    - إذا كان سيتم الوصول إلى Power App باستخدام زر القائمة Power Apps، يمكنك بدلاً من ذلك النقر فوق زر القائمة **Power Apps** في جزء الإجراءات القياسية، ثم تحديد **إدراج Power App**

3. تكوين Power App المضمن:

    - يشير الحقل **اسم** إلى النص الذي سيظهر للزر أو علامة التبويب التي سوف تحتوي على Power App المضمن. قد تحتاج أحيانًا إلى تكرار اسم Power App في هذا الحقل.
    - **معرف التطبيق** هو GUID (المعرف الفريد العمومي) لـ Power App الذي تريد تضمينه. لاسترداد هذه القيمة، ابحث عن Power App في [web.powerapps.com](https://web.powerapps.com)، ثم حدد موقع الحقل **معرف التطبيق** ضمن **التفاصيل**.
    - بالنسبة إلى **بيانات إدخال Power App**، يمكنك بشكل اختياري تحديد الحقل الذي يحتوي على البيانات التي تريد تمريرها إلى Power App كإدخال. راجع القسم لاحقًا في هذا الموضوع المسمى [تصميم Power App يستفيد من البيانات من تطبيقات Finance and Operations](#building-a-powerapp-that-leverages-data-sent-from-finance-and-operations-apps) للحصول على تفاصيل حول كيفية وصول Power App إلى البيانات المرسلة من تطبيقات Finance and Operations.
    - اختر **حجم التطبيق** الذي يتطابق مع نوع Power App الذي تقوم بتضمينه. حدد **رفيع** لتطبيقات Power Apps المبنية للأجهزة المحمولة، و**عريض** لتطبيقات Power Apps المبنية لأجهزة الكمبيوتر اللوحية. ويضمن هذا أن يتم تخصيص مساحة كافية لـ Power App المضمن.
    - توفر علامة التبويب السريعة **الكيانات القانونية** القدرة على اختيار الكيانات القانونية التي يتوفر Power App لها. الإعداد الافتراضي هو عرض Power App في جميع الكيانات القانونية.

4. بعد التأكد من أن إعدادات التكوين صحيحة، انقر فوق **إدراج** لتضمين Power App في الصفحة. ستتم مطالبتك بتحديث المستعرض لرؤية Power App المضمن.

## <a name="sharing-an-embedded-power-app"></a>مشاركة Power App مضمن

بعد قيامك بتضمين Power App على صفحة والتأكد من أنه يعمل بشكل صحيح بأي سياق بيانات تم تمريره من الصفحة، فقد تحتاج إلى مشاركة Power App المضمن هذا مع مستخدمين آخرين في النظام. يمكن أن يتم ذلك بطريقتين مختلفتين باستخدام إمكانات تخصيص المنتج:

- يتم السيناريو الموصى به من خلال مسؤول النظام، الذي يمكنه تقديم تخصيص لجميع المستخدمين أو مجموعة فرعية من المستخدمين.
- وبدلاً من ذلك، يمكنك تصدير تخصيصات الصفحة الخاصة بك وإرسالها إلى مستخدم واحد أو أكثر وجعل كل واحد من هؤلاء المستخدمين يستورد تلك التغييرات. يتيح لك الخيار إدارة في شريط أدوات التخصيص إمكانية تصدير واستيراد التخصيصات.

راجع [تخصيص تجربة المستخدم](personalize-user-experience.md) لمزيد من التفاصيل حول إمكانات التخصيص في المنتج وكيفية استخدامها.

## <a name="building-a-power-app-that-leverages-data-sent-from-finance-and-operations-apps"></a>تصميم Power App يستفيد من البيانات المرسلة من تطبيقات Finance and Operations

يستخدم جزء مهم في تصميم Power App الذي سيتم تضمينه في تطبيقات Finance and Operations بيانات الإدخال من تطبيقات Finance and Operations. داخل Power App، يمكن الوصول إلى بيانات الإدخال باستخدام متغير المعلمة ("EntityId").

على سبيل المثال، في وظيفة OnStart الخاصة بتطبيق Power App، يمكنك تعيين بيانات الإدخال من تطبيقات Finance and Operations إلى متغير مثل هذا:

```
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-an-embedded-power-app"></a>عرض Power App مضمن

لعرض Power App مضمن في إحدى الصفحات في تطبيقات Finance and Operations، انتقل ببساطة إلى صفحة باستخدام Power App مضمن. تذكر أنه يمكن الوصول إلى Power Apps من خلال الزر Power Apps في جزء الإجراءات القياسية، أو يمكنه أن يظهر مباشرةً على الصفحة كعلامة تبويب جديدة أو علامة تبويب سريعة أو كقسم جديد في مساحة عمل. عندما يحاول مستخدم أولاً تحميل Power App على صفحة، ستتم مطالبته بتسجيل الدخول إلى Power Apps للتأكد من المستخدم لديه أذونات مناسبة لاستخدام Power App.

## <a name="editing-an-embedded-power-app"></a>تحرير Power App مضمن

بعد أن تم تضمين Power App في صفحة، قد تحتاج إلى إجراء بعض التغييرات لتكوين Power App. على سبيل المثال، ربما تحتاج إلى تعديل التسمية المقترنة Power App مضمن أو إنشاء إصدار جديد من Power App وتحتاج إلى تحديث "معرف التطبيق" للإشارة إلى أحدث Power App.

اتبع هذه الخطوات لتحرير تكوين Power App مضمن:

1. انتقل إلى جزء **تحرير Power App**.

    - إذا تم الوصول إلى Power App مضمن من خلال زر القائمة Power Apps، فانقر بزر الماوس الأيمن فوق زر القائمة Power Apps، ثم حدد **تخصيص**. حدد Power App الذي تريد تكوينه من القائمة المنسدلة **تحديد Power App**.
    - إذا ظهر Power App المضمن مباشرةً في الصفحة، حدد **خيارات**، ثم حدد **تخصيص هذا النموذج**. استخدام أداة **التحديد**، انقر فوق Power App المضمن.

2. قم بإجراء التعديلات المطلوبة على تكوين Power Apps، ثم انقر فوق **حفظ‏‎**.

## <a name="removing-an-embedded-power-app"></a>إزالة Power App مضمن

بعد أن تم تضمين Power App في صفحة، هناك طريقتان لإزالته إذا لزم الأمر:

- انتقل إلى جزء **تحرير Power App** باستخدام الإرشادات من القسم السابق [تحرير Power App مضمن](#editing-an-embedded-powerapp) في هذا الموضوع. تأكد من أن الجزء يعرض معلومات Power App المضمن الذي تريد إزالته، ثم انقر فوق الزر **حذف**.
- بسبب حفظ Power App مضمن كبيانات تخصيص، سيؤدي أيضًا مسح تخصيص الصفحة إلى إزالة أي Power Apps مضمن في هذه الصفحة. لاحظ أن مسح تخصيص الصفحة دائم ولا يمكن التراجع عنه. لإزالة التخصيصات الخاصة بك في صفحة، حدد **خيارات**، ثم انقر فوق **تخصيص هذا النموذج**. ضمن القائمة **إدارة**، حدد الزر **مسح**. بعد تحديث المستعرض الخاص بك، ستتم إزالة جميع التخصيصات السابقة لهذه الصفحة. راجع [تخصيص تجربة المستخدم](personalize-user-experience.md) لمزيد من المعلومات حول كيفية تحسين الصفحات باستخدام التخصيص.

## <a name="appendix"></a>الملحق

### <a name="developer-control-over-where-a-power-app-can-be-embedded"></a>يمكن تضمين تحكم المطور في المكان الذي يتم فيه تضمين Power App

بشكل افتراضي، بإمكان المستخدمين تضمين Power Apps في أية صفحة، إما ضمن زر القائمة Power Apps أو مباشرةً على الصفحة كعلامة تبويب أو علامة تبويب سريعة أو نافذة أو كقسم جديد في مساحة عمل. ومع ذلك، إذا لزم الأمر، بإمكان المطورين أيضًا تكوين هذه الميزة للسماح فقط بتضمين Power Apps على صفحات معينة عن طريق تطبيق الأساليب التالية:

- **isPowerAppPersonalizationEnabled** – إذا أرجع هذا الأسلوب خطأ لصفحة معينة، فلن يظهر زر القائمة Power Apps، ولن يتمكن المستخدمون من تضمين Power Apps في أي مكان في هذه الصفحة، بما في ذلك كعلامة تبويب.
- **isPowerAppTabPersonalizationEnabled** – إذا أرجع هذا الأسلوب خطأً لصفحة معينة، فلن يتمكن المستخدمون من تضمين Power Apps مباشرةً في الصفحة كعلامة تبويب أو علامة تبويب سريعة أو قسم بانوراما. سيبقى باستطاعة المستخدمين تضمين Power Apps من خلال زر القائمة Power Apps في حالة السماح بالتضمين في الصفحة.

يوضح المثال التالي فئة جديدة مع الطريقتين المطلوبتين لتكوين المكان الذي يمكن فيه تضمين Power Apps.

```
[ExtensionOf(classStr(FormRunConfigurationPowerAppsConfiguration))]

public final class ClassTest_Extension
{
    public static boolean isPowerAppPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppPersonalizationEnabled(pageName);
        return result;
    }
    
    public static boolean isPowerAppTabPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppTabPersonalizationEnabled(pageName);
        return result;
    }
}
```
