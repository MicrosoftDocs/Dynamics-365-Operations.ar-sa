---
title: تسويات دفتر الأستاذ
description: توضح هذه المقالة كيفية استخدام صفحة "تسويات دفتر الأستاذ‬" لتسوية حركات دفتر الأستاذ وعكس التسويات.
author: kweekley
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTransSettlement
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-11-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 6357629f83873437eb62a4839fafd8efd98fffc1
ms.sourcegitcommit: 9041fa6e00ecbdf1a1880659d9bdfff4d888f20e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/22/2022
ms.locfileid: "9800621"
---
# <a name="ledger-settlements"></a>تسويات دفتر الأستاذ

[!include [banner](../includes/banner.md)]

تسوية دفتر الأستاذ هي عملية مطابقة الحركات المدينة والدائنة في دفتر الأستاذ العام. يتم استخدام تسوية المبالغ المدينة والدائنة لتسوية رصيد حساب دفتر الأستاذ بواسطة الحركات المفصلة التي تكوّن هذا الرصيد.

يمكن استبعاد الحركات التي تمت تسويتها من الاستعلامات والتقارير. وبهذه الطريقة، من الأسهل تحليل حركات دفتر الأستاذ المفتوحة التي تكوّن رصيد حساب دفتر الأستاذ.

> [!IMPORTANT] 
> توجد أيضًا لدى وحدات الحسابات الدائنة والحسابات المدينة تسوية فواتير ودفعات. عند حدوث التسوية في دفاتر الأستاذ الفرعية للحسابات الدائنة والحسابات المدينة، لا تتم تسوية إدخالات دفتر الأستاذ المناظرة بشكل تلقائي.

## <a name="ledger-settlement-features"></a>ميزات تسوية دفتر الأستاذ
في الإصدار 10.0.21 من Microsoft Dynamics 365‎ Finance تمت إزالة الخيار **تمكين تسوية دفتر الأستاذ المتقدم** من صفحة **معلمات دفتر الأستاذ العام**. تم الآن أيضًا تمكين تسوية دفتر الأستاذ المتقدم.
في الإصدار 10.0.25 من Finance، تم تقديم ميزة **الوعي بين تسوية دفتر الأستاذ وإغلاق نهاية العام**. تغيّر هذه الميزة تغيير الوظائف الأساسية في كل من تسوية دفتر الأستاذ وإغلاق نهاية العام لدفتر الأستاذ العام. قبل تمكين هذه الميزة، في مساحة عمل **إدارة الميزات**، راجع [الوعي بين تسوية دفتر الأستاذ وإغلاق نهاية العام‬‏‫](awareness-between-ledger-settlement-year-end-close.md).

## <a name="set-up-ledger-settlement"></a>إعداد تسوية دفتر الأستاذ
يجب تحديد الحسابات الرئيسية التي تريد اجراء تسوية دفتر الأستاذ لها. هناك طريقتان لتحديد هذه الحسابات الرئيسية.

1. انتقل إلى **دفتر الأستاذ العام** > **إعداد دفتر الأستاذ** > **معلمات دفتر الأستاذ العام**.
2. في علامة التبويب **تسويات دفتر الأستاذ**، حدد أدلة الحسابات التي تريد تحديد الحسابات الرئيسية منها.
3. حد الحسابات الرئيسية لإجراء تسوية دفتر الأستاذ لها. وبسبب كون أدلة الحسابات عمومية، سيكون لدى جميع الشركات التي تم تعيين أدلة الحسابات لها الحسابات الرئيسية نفسها المحددة لتسوية دفتر الأستاذ.

  -أو -

1. انتقل إلى **دفتر الأستاذ العام** > **المهام الدورية** > **تسويات دفتر الأستاذ**.
2. حدد **حسابات تسوية دفتر الأستاذ**.
3. في مربع الحوار، حدد أدلة الحسابات والحسابات الرئيسية لإجراء تسوية دفتر الأستاذ لها. مربع الحوار هذا عبارة عن اختصار. ستنعكس أيضًا أي حسابات رئيسية تقوم بإضافتها هنا على صفحة **معلمات دفتر الأستاذ العام**.

يمكنك استخدام نفس الإجراءات الأساسية لإزالة الحسابات الرئيسية من تسوية دفتر الأستاذ في أي وقت. لن تؤثر إزالة حساب رئيسي على تسويات دفتر الأستاذ السابقة. ومع ذلك، سيتوقف ظهور الحساب الرئيسي والحركات في صفحة **تسوية دفتر الأستاذ**.

## <a name="settle-transactions"></a><a name="settle-transactions"></a>تسوية الحركات
لتسوية حركات دفتر الأستاذ، اتبع هذه الخطوات:

1. انتقل إلى **دفتر الأستاذ العام** > **المهام الدورية** > **تسويات دفتر الأستاذ**.
2. قم بتعيين عوامل التصفية في أعلى الصفحة:

    - حدد نطاق تاريخ. أو حدد كود الفاصل الزمني‬ لتعبئة نطاق التاريخ بشكل تلقائي. لا نوصي بإجراء تسوية دفتر الأستاذ للحركات التي تعبر السنوات المالية.
    - قم بتغيير طبقة الترحيل كما تقتضي الحاجة. لا يمكنك تسوية الحركات الموجودة في طبقات ترحيل مختلفة.
    - لعرض الحساب الرئيسي والأبعاد بشكل منفصل، حدد مجموعة أبعاد مالية.

3. حدد **عرض الحركات** لعرض كافة الحركات التي تطابق عوامل التصفية التي قمت بتعيين وقائمة بالحسابات التي قمت بتحديدها عند إعداد دليل الحسابات في القسم السابق.

    - إذا قمت بتغيير أي من عوامل التصفية أو مجموعات الأبعاد، فيجب تحديد **عرض الحركات** مرة أخرى.
    - لتصفيه الحركات إلى حساب رئيسي فردي، استخدم عامل التصفية في الحقل **حساب دفتر الأستاذ**. لا نوصي بإجراء تسوية دفتر الأستاذ للحركات التي تم ترحيلها إلى حسابات رئيسية مختلفة.

4. حدد بنودًا للتسوية. تتزايد أو تتناقص قيمة حقل **المبلغ المحدد** في أعلى الصفحة لعكس المبلغ الإجمالي في البنود المحددة.
5. بعد الانتهاء من تحديد الحركات، حدد **تمييز المحددة**. لكل حركة محددة، تظهر علامة اختيار في العمود **معلّم**. علاوةً على ذلك، تتزايد أو تتناقص قيمة حقل **المبلغ المحدد** في أعلى الشبكة لعكس المبلغ الإجمالي في البنود التي حددتها.
6. عندما تكون قيمة **المبلغ المحدد** عبارة عن **0** (صفر)، حدد **تسوية الحركات المميزة‬**. يتم تحديث حالة الحركات المميزة إلى **تمت التسوية**.

    > [!IMPORTANT]
    > ستتم تسوية جميع الحركات التي حددتها للتسوية للكيان القانوني النشط، حتى لو لم تظهر حاليًا في صفحة تسوية دفتر الأستاذ لأنك قمت بتطبيق عامل تصفية.

## <a name="make-transactions-easier-to-find"></a>تسهيل العثور على الحركات
تتضمن صفحة **تسويات دفتر الأستاذ** قدرات تسهّل عرض الحركات التي تحتاج إليها للتسوية.

- استخدم عامل التصفية **معلّم** لتصفية الحركات استنادًا إلى ما إذا كانت خانة الاختيار **معلّم** التابعة لها محددة.
- استخدم عامل تصفية **الحالة** لتصفية الحركات بالاستناد إلى حالتها.
- حدد **فرز حسب المبلغ المطلق** لفرز المبالغ حسب القيمة المطلقة. وبهذه الطريقة، يمكنك تجميع الديون والائتمان التي لها نفس المبلغ.

## <a name="reverse-a-settlement"></a>عكس تسوية
يمكنك عكس تسوية تمت عن طريق الخطأ.

1. اتبع الخطوات من 1 إلى 3 في القسم [تسوية الحركات](#settle-transactions) لإظهار الحركات التي تهمك.
2. في عامل التصفية **حالة**، حدد **تمت التسوية**.
3. حدد بنودًا لعكسها.
4. حدد **عكس الحركات المميزة‬‬‏‫**. يتم تحديث حالة كافة الحركات التي لها معرف التسوية نفسه إلى **لم تتم تسويتها**.

    > [!IMPORTANT]
    > سيتم عكس كافة الحركات التي لها نفس معرف التسوية، حتى لو لم يتم تمييزها. على سبيل المثال، تم تمييز أربعة بنود وتسويتها. جميع البنود الأربعة لديها معرف التسوية نفسه. إذا قمت بتمييز أحد هذه البنود الأربعة، ثم حدد **عكس الحركات المميزة**، فسيتم عكس جميع البنود.

## <a name="unmark-for-selected-users"></a>إلغاء تعليم للمستخدمين المحددين
حدد **إلغاء تعليم للمستخدمين المحددين** لإلغاء علامة المعاملات المستقرة في دفتر الأستاذ لجميع الكيانات القانونية بواسطة معرف المستخدم. على سبيل المثال، سيسمح هذا لمدير المحاسبة بإلغاء تحديد المعاملات للمستخدم الذي غادر في إجازة قبل الانتهاء من التسوية أو لمستخدم غادر المؤسسة. سيسمح هذا الإجراء بوضع علامة على هذه المعاملات للتسوية من قبل مستخدم آخر.


## <a name="unmark-all-transactions"></a>إلغاء علامة كافة الحركات
حدد **إلغاء تحديد كافة المعاملات** لإلغاء تحديد كافة المعاملات التي تمت تسويتها في دفتر الأستاذ لجميع المستخدمين وجميع الكيانات القانونية. هذا الإجراء متاح لدور المسؤول.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
