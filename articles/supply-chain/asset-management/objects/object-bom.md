---
title: BOM الأصل
description: يصف هذا الموضوع قوائم مكونات الصنف (BOM) للأصل في إدارة الأصول.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 761364c8c58258baf2268f917cb174ac300c4528
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783052"
---
# <a name="asset-boms"></a>BOM الأصل

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

يصف هذا الموضوع قوائم مكونات الصنف (BOM) للأصل في إدارة الأصول. تعرض صفحة **BOM الأصل** قائمة بجميع الأصناف (قطع الغيار والأصناف الأخرى) التي يتم استخدامها على أحد الأصول خلال عمره الكامل. عند إنشاء أصل جديد، يجب عليك إعداد BOM الأصل كجزء من إجراء الإعداد. وبهذه الطريقة، يمكنك تعقب محفوظات الأصناف التابعة للأصل من تاريخ الإنشاء.

بعد الانتهاء من مهمة صيانة، وتسجيل استهلاك الصنف في أمر عمل، يمكنك تعقب استهلاك قطع الغيار والأصناف الأخرى المستخدمة في الأصل. تتيح لك هذه الوظيفة الاحتفاظ بسجل استهلاك كامل للأصناف لجميع الأصول. على سبيل المثال، يمكنك استخدام السجل لمراقبة ما إذا كان يتم استبدال قطعة غيار معينة بشكل متكرر، أو لتعقب قطع الغيار أو الأصناف الأخرى المستخدمة حاليًا على الأصل.

> [!NOTE]
> في أمر العمل، قد يشمل استهلاك الصنف قطع الغيار وغيرها من الأصناف الإضافية، مثل مواد التشحيم والبراغي والحشايا.

يمكن تحديث BOM الأصل تلقائيًا استنادًا إلى الإعداد في إدارة الأصول. إذا تم إنشاء حالة دورة حياة أمر عمل لمعالجة أوامر عمل منجزة أو مكتملة، وإذا تم تعيين الخيار **تحديث BOM‏‎ الأصل** لحالة دورة حياة أمر العمل هذا إلى **نعم** في صفحة **حالات دورة حياة أمر العمل**، فسيتم تحديث جميع الأصناف المستخدمة على أمر العمل بشكل تلقائي في صفحة **BOM‏‎ الأصل** عند تحديث أمر العمل إلى حالة دورة الحياة هذه. 


يمكنك أيضًا تحديث BOM‎ الأصل يدويًا عن طريق إنشاء بنود أصناف جديدة في صفحة **BOM‎ الأصل**.

في صفحة **BOM‎ الأصل**، يمكنك تعقب محفوظات قطع الغيار للأصول بعد تسجيل استهلاك الأصناف في أمر عمل. لاستخدام هذه الوظيفة، يجب تحديد مجموعات الأصناف التي يجب استخدامها لتسجيل قطع الغيار في صفحة **مجموعات أصناف قطع الغيار**.

لاستخدام وظيفة BOM الأصل، يجب أولاً إعداد مجموعات أصناف قطع الغيار المطلوبة. ثم، إذا كنت تريد تحديث BOM الأصل تلقائيًا عند اكتمال أمر عمل، يمكنك إعداد حالة دورة حياة أمر العمل لمعالجة هذا التحديث. 


## <a name="set-up-spare-parts-item-groups"></a>إعداد مجموعات أصناف قطع الغيار

يستند إعداد محفوظات قطع الغيار إلى مجموعات الأصناف التي يتم إنشاؤها في الوحدة النمطية **إدارة المخزون والمستودعات‬**. في إدارة الأصول، يمكنك إعداد مجموعات الأصناف بحيث يمكنك تعقب محفوظات قطع الغيار للأصناف في مجموعات الأصناف المحددة.

1. حدد **إدارة الأصول** \> **الإعداد** \> **الأصل** \> **مجموعات أصناف قطع الغيار‬**.
2. حدد **جديد** لإعداد مجموعة أصناف.
3. في حقل **مجموعة الأصناف**، حدد المجموعة. يتم إدخال اسم المجموعة تلقائيًا في حقل **الاسم**.

## <a name="view-and-update-asset-boms"></a>عرض وتحديث BOM الأصل

بعد ترحيل استهلاك الصنف في أمر عمل، يمكنك عرض استهلاك الأصناف المسجلة في صفحة **BOM الأصل**.

1. حدد **إدارة الأصول** \> **عام** \> **الأصول** \> **الأصول‏‎ النشطة**. حدد الأصل في القائمة، ثم حدد‏‎ **BOM الأصل**.

    > [!NOTE]
    > لعرض جميع تسجيلات استهلاك الأصناف على جميع الأصول، حدد **إدارة الأصول** \> **الاستفسارات** \> **الأصول** \> **BOM‏‎ الأصل**.

2. حدد **تحديث BOM الأصل**. يمكنك إضافة الأصول وأنواع الأصول والموارد إلى التحديث كما هو مطلوب من خلال تحديد **تحديد**. حدد **موافق** لبدء التحديث. يمكنك أيضًا اعداد وظيفة التحديث كوظيفة دفعية.
3. إذا كنت ترغب في عرض مزيد من المعلومات المرتبطة بالأصناف، فيمكنك إضافة أبعاد المخزون. حدد **المخزون** \> **عرض الأبعاد‬**، ثم حدد خانات الاختيار للمتغيرات التي تريد استخدامها. للاحتفاظ بهذا الاعداد لجميع الأصول في صفحة **BOM الأصل**، عيّن الخيار **حفظ الإعداد** إلى **نعم**.
4. للحصول علي نظرة عامة حول المكان في إدارة الأصول حيث يتم استخدام الصنف على البند المحدد، بالنسبة إلى الأصول والإعدادات الافتراضية لنوع الوظيفة وقطع الغيار وأوامر العمل، حدد **مكان استخدام الصنف**. 
5. إذا أردت رؤية بنود الصنف النشطة فقط، فحدد **عرض** \> **الحالي**. لعرض كافة بنود الأصناف، بما في ذلك البنود التي لديها تاريخ انتهاء صلاحية أبكر من التاريخ الحالي، حدد **عرض** \> **الكل**.

> [!NOTE]
> عندما تكمل أمر عمل، إذا انتهت صلاحيه بعض الأصناف أو قطع الغيار المرتبطة بالأصل ذي الصلة أو تم استبدالها بأصناف أو قطع غيار أخرى، فنحن ننصحك بتحديث BOM الأصل وفقًا لذلك.

## <a name="create-a-new-item-line-in-an-asset-bom"></a>إنشاء بند صنف جديد في BOM الأصل

يمكنك إنشاء بنود الأصناف الخاصة بالأصول يدويًا.

1. في صفحة **BOM‎ الأصل‬**، حدد **جديد**.
2. في حقل **الأصل**، حدد الأصل المراد إضافة بند صنف له.
3. في الحقل **رقم البند**، أدخل رقم بند تسلسلي.
4. في الحقل **سارٍ‏‎** حدد تاريخ بدء الصنف.
5. إذا كان لدى الصنف تاريخ انتهاء صلاحية، فأدخل تاريخ الانتهاء في حقل **انتهاء الصلاحية**.
6. في الحقل **رقم الصنف**، حدد الصنف. يتم إدخال الاسم تلقائيًا في حقل **اسم المنتج**.
7. في حقل **الكمية**، أدخل الكمية المستخدمة. يتم تحديث حقل **الوحدة** تلقائيًا.