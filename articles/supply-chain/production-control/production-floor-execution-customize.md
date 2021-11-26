---
title: تخصيص واجهة تنفيذ صالة الإنتاج‬ واستخدامها
description: يشرح هذا الموضوع كيفية توسيع النماذج الحالية أو إنشاء نماذج وأزرار جديدة لواجهة تنفيذ أرضية الإنتاج.
author: johanhoffmann
ms.date: 11/08/2021
ms.topic: article
ms.search.form: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-11-08
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 414fe5d6e16ad125bc2b9bb7ed427e5db5180ec9
ms.sourcegitcommit: bc9e75c38e192664cde226ed3a94df5a0b304369
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/10/2021
ms.locfileid: "7790954"
---
# <a name="customize-the-production-floor-execution-interface"></a>تخصيص واجهة تنفيذ صالة الإنتاج‬ واستخدامها

[!include [banner](../includes/banner.md)]

يمكن للمطورين توسيع النماذج الحالية أو إنشاء نماذجهم وأزرارهم لواجهة تنفيذ أرضية الإنتاج. بعد إضافة رمز هذه العناصر الجديدة، يمكن للمسؤولين أو مديري المتجر إضافتها بسهولة إلى الواجهة باستخدام عناصر التحكم في التكوين القياسية.

على سبيل المثال، فيما يلي بعض الحلول الممكنة إذا كانت هناك حاجة إلى أعمدة جديدة في نموذج رئيسي:

- قم بتوسيع نموذج `JmgProductionFloorExecutionMainGrid`، وأضف الحقول المطلوبة.
- قم بإنشاء نموذج جديد وإضافته كعرض رئيسي جديد (علامة تبويب).

## <a name="add-a-new-button-action"></a>إضافة زر جديد (إجراء)

لإضافة زر جديد (إجراء)، اتبع هذه الخطوات لإنشاء فصل دراسي يقوم بتنفيذ الإجراء المخصص الخاص بك.

1. قم بإنشاء فئة جديدة باسم `<ExtensionPrefix>_JmgProductionFloorExecution<ActionName>Action`، حيث:

    - `<ExtensionPrefix>` يعرّف الحل بشكل فريد، عادةً باستخدام اسم شركتك.
    - `<ActionName>` هو اسم فريد للفئة. عادة ما يحدد نوع العمل.

1. يجب أن توسع الفئة الجديدة فئة `JmgProductionFloorExecutionAction`.
1. تجاوز كل الطرق الضرورية.

للحصول على أمثلة، انظر إلى رمز الفئات التالية:

- `JmgProductionFloorExecutionBreakAction` – فئة لإجراء بسيط لا يحتاج إلى أي سجلات.
- `JmgProductionFloorExecutionReportFeedbackAction` – فئة توفر وظائف أكثر تعقيدًا.

عند الانتهاء، سيتم إدراج الزر الجديد (الإجراء) تلقائيًا في صفحة **علامات تبويب التصميم** في Microsoft Dynamics 365 Supply Chain Management. هناك، يمكنك (أو المسؤول أو مدير الأرضية) إضافته بسهولة إلى شريط الأدوات الأساسي أو الثانوي، تمامًا كما يمكنك إضافة الأزرار القياسية. للاطلاع على التعليمات، راجع [تصميم واجهة تنفيذ أرضية الإنتاج](production-floor-execution-tabs.md).

## <a name="add-a-new-main-view"></a>إضافة عرض رئيسي جديد

1. قم بإنشاء نموذج جديد يحتوي على العناصر والوظائف المطلوبة. لاحظ أن هذا النموذج هو نموذج جديد، وليس امتدادًا. قم بتسمية النموذج `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>`، حيث:

    - `<ExtensionPrefix>` يعرّف الحل بشكل فريد، عادةً باستخدام اسم شركتك.
    - `<FormName>` هو اسم فريد للنموذج.

1. قم بإنشاء عنصر قائمة يسمى `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>`.
1. قم بإنشاء ملحق يسمى `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension`، حيث يتم توسيع أسلوب `getMainMenuItemsList` عن طريق إضافة عنصر القائمة الجديد إلى القائمة. يبين الرمز التالي مثالاً.

    ```xpp
    [ExtensionOf(classStr(JmgProductionFloorExecutionForm))]
    public final class <ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>_Extension{
        static public List getMainMenuItemsList()
        {
            List menuItemList = next getMainMenuItemsList();
            menuItemList.addEnd(menuItemDisplayStr(<ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>));
            return menuItemList;
        }
    ```

عند الانتهاء، سيتم إدراج العرض الرئيسي الجديد تلقائيًا في المربع المنسدل **طريقة العرض الرئيسية** في صفحة **تصميم علامات التبويب** في Supply Chain Management. هناك، يمكنك (أو مسؤول أو مدير الطابق) إضافته بسهولة إلى علامات تبويب جديدة أو موجودة، تمامًا كما يمكنك إضافة طرق العرض الرئيسية القياسية. للاطلاع على التعليمات، راجع [تصميم واجهة تنفيذ أرضية الإنتاج](production-floor-execution-tabs.md).

## <a name="add-a-details-view"></a>إضافة طريقة عرض التفاصيل

1. قم بإنشاء نموذج جديد يحتوي على العناصر والوظائف المطلوبة. لاحظ أن هذا النموذج جديد وليس ملحقًا. قم بتسمية النموذج `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail`، حيث: 

    - `<ExtensionPrefix>` يعرّف الحل بشكل فريد، عادةً باستخدام اسم شركتك.
    - `<FormName>` هو اسم فريد للنموذج.

1. قم بإنشاء عنصر قائمة يسمى `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail`.
1. قم بإنشاء ملحق يسمى `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension`، حيث يتم توسيع أسلوب `getDetailsMenuItemList` عن طريق إضافة عنصر القائمة الجديد إلى القائمة.

عند الانتهاء، سيتم إدراج طريقة عرض التفاصيل الجديدة تلقائيًا في المربع المنسدل **طريقة عرض التفاصيل** في صفحة **تصميم علامات التبويب** في Supply Chain Management. هناك، يمكنك (أو مسؤول أو مدير الطابق) إضافته بسهولة إلى علامات تبويب جديدة أو موجودة، تمامًا كما يمكنك إضافة طرق عرض التفاصيل القياسية. للاطلاع على التعليمات، راجع [تصميم واجهة تنفيذ أرضية الإنتاج](production-floor-execution-tabs.md).

## <a name="add-a-numeric-keypad-to-a-form-or-dialog"></a>إضافة لوحة مفاتيح رقمية إلى نموذج أو مربع حوار

يوضح المثال التالي كيفية إضافة لوحات المفاتيح الرقمية إلى نموذج.

1. يجب أن يساوي عدد وحدات التحكم في لوحة المفاتيح الرقمية التي يحتوي عليها كل نموذج عدد لوحات المفاتيح الرقمية في هذا النموذج.

    ```xpp
    private JmgProductionFloorExecutionNumpadController   numpadController1;
    private JmgProductionFloorExecutionNumpadController   numpadController2;
    private JmgProductionFloorExecutionNumpadController   numpadController3;
    ```

1. قم بإعداد سلوك كل وحدة تحكم في لوحة المفاتيح الرقمية، وقم بتوصيل كل وحدة تحكم في لوحة المفاتيح الرقمية بجزء من نموذج لوحة المفاتيح الرقمية.

    ```xpp
    /// <summary>
    /// Initializes all numpad controllers, defines their behavior and connects them with numpad form parts.
    /// </summary>
    public void initializeNumpadController()
    {
        numpadController1 = new JmgProductionFloorExecutionNumpadController();
        numpadController1.getValueFromNumpadDelegate += eventhandler(this.setQuanityValueFromNumpad_1);
        QuantityNumpad1.getPartFormRun().setNumpadController(numpadController1);
    
        numpadController2 = new JmgProductionFloorExecutionNumpadController();
        numpadController2.parmNumpadEnabled(false);
        numpadController2.parmNumpadValue(333.56);
        numpadController2.getValueFromNumpadDelegate += eventhandler(this.setQuanityValueFromNumpad_2);
        QuantityNumpad2.getPartFormRun().setNumpadController(numpadController2);
    }
    ```

## <a name="use-a-numeric-keypad-as-a-pop-up-dialog"></a>استخدم لوحة المفاتيح الرقمية كمربع حوار منبثق

يوضح المثال التالي طريقة واحدة لإعداد وحدة تحكم رقمية في لوحة المفاتيح لمربع حوار منبثق.

```xpp
private void setupNumpadController()
{
    numpadController = new JmgProductionFloorExecutionNumpadController();
    numpadController.parmShouldNumpadShowOkCancelButtons(true);
    numpadController.setNumpadValueToParentFormDelegate += eventhandler(this.setQtyValueFromNumpad);
}
```

يوضح المثال التالي طريقة واحدة للاتصال بمربع الحوار المنبثق بلوحة المفاتيح الرقمية.

```xpp
Args args = new Args();
args.name(formstr(JmgProductionFloorExecutionNumpad));
args.menuItemName(menuItemDisplayStr(JmgProductionFloorExecutionNumpad));
args.caller(element);
Object formRun = classfactory.formRunClass(args);
formRun.init();
formRun.setNumpadController(numpadController);
numpadController.setValueToNumpad(333.56);
formRun.run();
```

## <a name="additional-resources"></a>الموارد الإضافية

- [واجهة تنفيذ صالة الإنتاج](production-floor-execution-styles.md)
- [تصميم واجهة تنفيذ صالة الإنتاج](production-floor-execution-tabs.md)
