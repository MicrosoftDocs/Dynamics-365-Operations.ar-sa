---
title: تضمين تطبيقات PowerApps
description: يصف هذا الموضوع كيفية تضمين PowerApps في العميل لزيادة الأداء الوظيفي للمنتج.
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
ms.openlocfilehash: 37faf2a7a880c384f6f01d06ef5c9f28055d5006
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191168"
---
# <a name="embed-powerapps-apps"></a>تضمين تطبيقات PowerApps

[!include [banner](../includes/banner.md)]

يدعم Platform update 14 التكامل مع Microsoft PowerApps، وهي عبارة عن خدمة للمطورين والمستخدمين غير التقنيين لإنشاء تطبيقات أعمال مخصصة للأجهزة المحمولة وأجهزة الكمبيوتر اللوحية والويب من دون كتابة تعليمة برمجية. ويمكن بعد ذلك تضمين PowerApps الذي طورته أنت أو مؤسستك أو النظام البيئي الأوسع في تطبيقات Finance and Operations لزيادة الأداء الوظيفي للمنتج. على سبيل المثال، قد تقوم بإنشاء PowerApp لتكملة تطبيقات Finance and Operations بالمعلومات التي تم استردادها من نظام آخر.

لمزيد من المعلومات حول تضمين PowerApps، شاهد مقطع الفيديو القصير [كيفية تضمين PowerApps](https://www.youtube.com/watch?v=x3qyA1bH-NY) video.

## <a name="adding-an-embedded-powerapp-to-a-page"></a>إضافة PowerApp مضمن إلى صفحة

### <a name="overview"></a>نظرة عامة

قبل تضمين PowerApp في العميل، تحتاج أولاً إلى البحث عنPowerApp أو بنائه بواسطة المرئيات و/أو الوظيفة المطلوبة. لن نصف العملية التفصيلية لإنشاء PowerApp هنا. يعتبر الموضوع [مقدمة إلى PowerApps](https://docs.microsoft.com/powerapps/getting-started) نقطة بداية جيدة إذا كان استخدام PowerApps أمرًا جديدًا بالنسبة لك.

عندما تكون مستعدًا لدمج PowerApp محدد، يمكنك الاختيار من بين إحدى الطريقتين التاليتين للوصول إلى PowerApp في صفحة، أي الطريقتين أنسب للسيناريو الخاص بك. الطريقة الأولى هي استخدام الزر PowerApps الذي تمت إضافته إلى جزء الإجراءات القياسية. سوف تظهر PowerApps الذي التي تمت إضافتها باستخدام هذه الآلية كعناصر قائمة داخل زر القائمة PowerApps. عند تحديد كل عنصر من عناصر القائمة هذه، ستقوم بفتح جزءًا جانبيًا يحتوي على PowerApp المضمن. بدلاً من ذلك، يمكنك اختيار إظهار PowerApp مباشرةً على صفحة كعلامة تبويب جديدة، أو كعلامة تبويب سريعة، أو ريشة، أو كقسم جديد في مساحة عمل.

عند تكوين PowerApp المضمن، يمكنك تحديد حقل واحد تريد إرساله كإدخال إلى PowerApp. يتيح هذا لـ PowerApp أن يستجيب استنادًا إلى البيانات التي تقوم بعرضها حاليًا.

### <a name="details"></a>التفاصيل

تبين الإرشادات التالية كيفية تضمين PowerApp في عميل الويب.

1. انتقل إلى الصفحة التي تريد فيها تضمين PowerApp. ستكون هذه الصفحة نفس الصفحة التي تحتوي على أي بيانات يجب أن يتم تمريرها إلى PowerApp كإدخال.
2. افتح جزء **إدخال PowerApp**:

    - انقر فوق **خيارات**، ثم حدد **تخصيص هذا النموذج**. ضمن القائمة **إدراج**، اختر **PowerApp**. وأخيرًا، حدد المنطقة التي تريد فيها إضافة PowerApp. إذا كنت ترغب في تضمين PowerApp ضمن زر القائمة PowerApps، فاختر "جزء الإجراءات". إذا كنت ترغب في تضمين PowerApp مباشرةً في الصفحة، فاختر علامة التبويب المناسبة، أو علامة التبويب السريعة، أو الريشة، أو القسم (إذا كنت متصلاً بمساحة عمل).
    - إذا كان سيتم الوصول إلى PowerApp باستخدام زر القائمة PowerApps، يمكنك بدلاً من ذلك النقر فوق زر القائمة **PowerApps** في جزء الإجراءات القياسية، ثم تحديد **إدراج PowerApp**

3. تكوين PowerApp المضمن:

    - يشير الحقل **اسم** إلى النص الذي سيظهر للزر أو علامة التبويب التي سوف تحتوي على PowerApp المضمن. قد تحتاج أحيانًا إلى تكرار اسم PowerApp في هذا الحقل.
    - **معرف التطبيق** هو GUID (المعرف الفريد العمومي) لـ PowerApp الذي تريد تضمينه. لاسترداد هذه القيمة، ابحث عن PowerApp في [web.powerapps.com](https://web.powerapps.com)، ثم حدد موقع الحقل **معرف التطبيق** ضمن **التفاصيل**.
    - بالنسبة إلى **بيانات إدخال PowerApp**، يمكنك بشكل اختياري تحديد الحقل الذي يحتوي على البيانات التي تريد تمريرها إلى PowerApp كإدخال. راجع القسم لاحقًا في هذا الموضوع المسمى [تصميم PowerApp يستفيد من البيانات من تطبيقات Finance and Operations](#building-a-powerapp-that-leverages-data-sent-from-finance-and-operations-apps) للحصول على تفاصيل حول كيفية وصول PowerApp إلى البيانات المرسلة من تطبيقات Finance and Operations.
    - اختر **حجم التطبيق** الذي يتطابق مع نوع PowerApp الذي تقوم بتضمينه. حدد **رفيع** لتطبيقات PowerApps المبنية للأجهزة المحمولة، و**عريض** لتطبيقات PowerApps المبنية لأجهزة الكمبيوتر اللوحية. ويضمن هذا أن يتم تخصيص مساحة كافية لـ PowerApp المضمن.
    - توفر علامة التبويب السريعة **الكيانات القانونية** القدرة على اختيار الكيانات القانونية التي يتوفر PowerApp لها. الإعداد الافتراضي هو عرض PowerApp في جميع الكيانات القانونية.

4. بعد التأكد من أن إعدادات التكوين صحيحة، انقر فوق **إدراج** لتضمين PowerApp في الصفحة. ستتم مطالبتك بتحديث المستعرض لرؤية PowerApp المضمن.

## <a name="sharing-an-embedded-powerapp"></a>مشاركة PowerApp مضمن

بعد قيامك بتضمين PowerApp على صفحة والتأكد من أنه يعمل بشكل صحيح بأي سياق بيانات تم تمريره من الصفحة، فقد تحتاج إلى مشاركة PowerApp المضمن هذا مع مستخدمين آخرين في النظام. يمكن أن يتم ذلك بطريقتين مختلفتين باستخدام إمكانات تخصيص المنتج:

- يتم السيناريو الموصى به من خلال مسؤول النظام، الذي يمكنه تقديم تخصيص لجميع المستخدمين أو مجموعة فرعية من المستخدمين.
- وبدلاً من ذلك، يمكنك تصدير تخصيصات الصفحة الخاصة بك وإرسالها إلى مستخدم واحد أو أكثر وجعل كل واحد من هؤلاء المستخدمين يستورد تلك التغييرات. يتيح لك الخيار إدارة في شريط أدوات التخصيص إمكانية تصدير واستيراد التخصيصات.

راجع [تخصيص تجربة المستخدم](personalize-user-experience.md) لمزيد من التفاصيل حول إمكانات التخصيص في المنتج وكيفية استخدامها.

## <a name="building-a-powerapp-that-leverages-data-sent-from-finance-and-operations-apps"></a>تصميم PowerApp يستفيد من البيانات المرسلة من تطبيقات Finance and Operations

يستخدم جزء مهم في تصميم PowerApp الذي سيتم تضمينه في تطبيقات Finance and Operations بيانات الإدخال من تطبيقات Finance and Operations. داخل PowerApp، يمكن الوصول إلى بيانات الإدخال باستخدام متغير المعلمة ("EntityId").

على سبيل المثال، في وظيفة OnStart الخاصة بتطبيق PowerApp، يمكنك تعيين بيانات الإدخال من تطبيقات Finance and Operations إلى متغير مثل هذا:

```
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-an-embedded-powerapp"></a>عرض PowerApp مضمن

لعرض PowerApp مضمن في إحدى الصفحات في تطبيقات Finance and Operations، انتقل ببساطة إلى صفحة باستخدام PowerApp مضمن. تذكر أنه يمكن الوصول إلى PowerApps من خلال الزر PowerApps في جزء الإجراءات القياسية، أو يمكنه أن يظهر مباشرةً على الصفحة كعلامة تبويب جديدة أو علامة تبويب سريعة أو كقسم جديد في مساحة عمل. عندما يحاول مستخدم أولاً تحميل PowerApp على صفحة، ستتم مطالبته بتسجيل الدخول إلى PowerApps للتأكد من المستخدم لديه أذونات مناسبة لاستخدام PowerApp.

## <a name="editing-an-embedded-powerapp"></a>تحرير PowerApp مضمن

بعد أن تم تضمين PowerApp في صفحة، قد تحتاج إلى إجراء بعض التغييرات لتكوين PowerApp. على سبيل المثال، ربما تحتاج إلى تعديل التسمية المقترنة PowerApp مضمن أو إنشاء إصدار جديد من PowerApp وتحتاج إلى تحديث "معرف التطبيق" للإشارة إلى أحدث PowerApp.

اتبع هذه الخطوات لتحرير تكوين PowerApp مضمن:

1. انتقل إلى جزء **تحرير PowerApp**.

    - إذا تم الوصول إلى PowerApp مضمن من خلال زر القائمة PowerApps، فانقر بزر الماوس الأيمن فوق زر القائمة PowerApps، ثم حدد **تخصيص**. حدد PowerApp الذي تريد تكوينه من القائمة المنسدلة **تحديد PowerApp**.
    - إذا ظهر PowerApp المضمن مباشرةً في الصفحة، حدد **خيارات**، ثم حدد **تخصيص هذا النموذج**. استخدام أداة **التحديد**، انقر فوق PowerApp المضمن.

2. قم بإجراء التعديلات المطلوبة على تكوين PowerApps، ثم انقر فوق **حفظ‏‎**.

## <a name="removing-an-embedded-powerapp"></a>إزالة PowerApp مضمن

بعد أن تم تضمين PowerApp في صفحة، هناك طريقتان لإزالته إذا لزم الأمر:

- انتقل إلى جزء **تحرير PowerApp** باستخدام الإرشادات من القسم السابق [تحرير PowerApp مضمن](#editing-an-embedded-powerapp) في هذا الموضوع. تأكد من أن الجزء يعرض معلومات PowerApp المضمن الذي تريد إزالته، ثم انقر فوق الزر **حذف**.
- بسبب حفظ PowerApp مضمن كبيانات تخصيص، سيؤدي أيضًا مسح تخصيص الصفحة إلى إزالة أي PowerApps مضمن في هذه الصفحة. لاحظ أن مسح تخصيص الصفحة دائم ولا يمكن التراجع عنه. لإزالة التخصيصات الخاصة بك في صفحة، حدد **خيارات**، ثم انقر فوق **تخصيص هذا النموذج**. ضمن القائمة **إدارة**، حدد الزر **مسح**. بعد تحديث المستعرض الخاص بك، ستتم إزالة جميع التخصيصات السابقة لهذه الصفحة. راجع [تخصيص تجربة المستخدم](personalize-user-experience.md) لمزيد من المعلومات حول كيفية تحسين الصفحات باستخدام التخصيص.

## <a name="appendix"></a>الملحق

### <a name="developer-control-over-where-a-powerapp-can-be-embedded"></a>يمكن تضمين تحكم المطور في المكان الذي يتم فيه تضمين PowerApp

بشكل افتراضي، بإمكان المستخدمين تضمين PowerApps في أية صفحة، إما ضمن زر القائمة PowerApps أو مباشرةً على الصفحة كعلامة تبويب أو علامة تبويب سريعة أو نافذة أو كقسم جديد في مساحة عمل. ومع ذلك، إذا لزم الأمر، بإمكان المطورين أيضًا تكوين هذه الميزة للسماح فقط بتضمين PowerApps على صفحات معينة عن طريق تطبيق الأساليب التالية:

- **isPowerAppPersonalizationEnabled** – إذا أرجع هذا الأسلوب خطأ لصفحة معينة، فلن يظهر زر القائمة PowerApps، ولن يتمكن المستخدمون من تضمين PowerApps في أي مكان في هذه الصفحة، بما في ذلك كعلامة تبويب.
- **isPowerAppTabPersonalizationEnabled** – إذا أرجع هذا الأسلوب خطأً لصفحة معينة، فلن يتمكن المستخدمون من تضمين PowerApps مباشرةً في الصفحة كعلامة تبويب أو علامة تبويب سريعة أو قسم بانوراما. سيبقى باستطاعة المستخدمين تضمين PowerApps من خلال زر القائمة PowerApps في حالة السماح بالتضمين في الصفحة.

يوضح المثال التالي فئة جديدة مع الطريقتين المطلوبتين لتكوين المكان الذي يمكن فيه تضمين PowerApps.

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