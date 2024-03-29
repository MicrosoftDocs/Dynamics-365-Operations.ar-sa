---
title: تثبيت الأصول في مواقع العمل
description: يوضح هذا المقال كيفية تثبيت الأصول في مواقع العمل في "إدارة الأصول".
author: johanhoffmann
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationObjectChange, EntAssetFunctionalLocationObjectInstall, EntAssetFunctionalLocationObject
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3ae571f4ad7210b31d212b0472610b36dc5c488b
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016061"
---
# <a name="install-assets-on-functional-locations"></a>تثبيت الأصول في مواقع العمل

[!include [banner](../../includes/banner.md)]

 

بعد إنشاء بنى مواقع العمل، تقضي الخطوة التالية بتثبيت الأصول في مواقع العمل ذات الصلة. يُوضح هذا المقال كيفية تثبيت الأصول في مواقع العمل هذه في "إدارة الأصول". لمزيد من المعلومات حول كيفية إنشاء الأصول، راجع [مقدمة إلى الأصول](../objects/introduction-to-objects.md).

إذا قمت بإنشاء بنية أصول، فيجب تثبيت بنية الأصول الكاملة في موقع العمل. وبالتالي، يمكن تحديد الأصول الأساسية فقط (الأصول ذات المستوى الأعلى التي ليس لديها أصل أساسي) في موقع العمل. كما سيتم تثبيت جميع الأصول التابعة ذات الصلة (الأصول الفرعية) في موقع العمل. عند تثبيت الأصول في موقع عمل، قد يتم نقل الأبعاد المالية لموقع العمل تلقائيًا إليها، استنادًا إلى الإعداد على نوع موقع العمل المحدد لموقع العمل. لمزيد من المعلومات حول كيفية إعداد أنواع مواقع العمل، راجع [أنواع مواقع العمل](../setup-for-functional-locations/functional-location-types.md).

> [!NOTE]
> يمكنك إعداد أنواع الأصول في نوع موقع العمل المستخدم لموقع العمل. في هذه الحالة، عند تثبيت الأصول في موقع العمل، يتم إظهار الأصول الأساسية التي لها نفس نوع الأصل في قائمة الأصول التي يمكن تثبيتها في موقع العمل.

بعد تثبيت الأصول في موقع عمل، يمكنك استبدال أصل أساسي أو بنية أصل عندما تحتاج إلى ذلك. كما هو الحال عند تثبيت الأصول، يمكنك تحديد أصل أساسي للاستبدال. كما سيتم استبدال جميع الأصول التابعة ذات الصلة. 


## <a name="install-an-asset-structure-on-a-functional-location"></a>تثبيت بنية أصل في موقع عمل

1. حدد **إدارة الأصول** \> **مواقع العمل** \> **جميع مواقع العمل** أو **مواقع العمل النشطة**.
2. حدد موقع العمل لتثبيت أصل فيه.
3. حدد **تثبيت الأصل**.

    يُظهر قسم **السمات** قائمة بمتطلبات سمة الأصل التي تم إعدادها في نوع موقع العمل المحدد لموقع العمل. السمات هي لأغراض معلوماتية فقط. لا يتحقق النظام من صحة السمات مقابل سمات الأصل التي تم إعدادها على الأصل الذي تقوم بتثبيته. يجب إجراء التحقق من الصحة هذا بعد تحديد أصل في حقل **الأصل**.

4. في حقل **الأصل**، حدد الأصل الأساسي المراد تثبيته. يتم تضمين كافة الأصول التابعة ذات الصلة تلقائيًا في التثبيت.

    يُظهر قسم **سمات الأصل** الموجود إلى يسار قائمة الأصول سمات الأصل المرتبطة بالأصل المحدد.

5. في الحقل **ساري**، حدد التاريخ والوقت الذي بدءًا منه يكون تثبيت الأصل صالحًا. بعد ذلك التاريخ والوقت، سترتبط تكاليف الأصول والأصول الفرعية ذات الصلة بموقع العمل.

    > [!NOTE]
    > تتم إضافة سمات الأصل التي تم إعدادها على الأصل إلى قسم **السمات**. على سبيل المثال تمت إضافة سمة **الوزن** كمتطلب على كل من الأصل وموقع العمل. إذا تضمن الأصل متطلبات سمة من نفس نوع موقع العمل، يتم إدخال قيم متطلبات سمة الأصل في حقول **القيمة**. لذلك، يمكنك التحقق من صحة قيم الأصول مقابل متطلبات السمات التي تم إعدادها في موقع العمل. يتم وضع علامة اختيار على متطلبات السمات التي تم إعدادها في موقع العمل.

6. حدد **موافق**.

    > [!NOTE]
    > لتغيير تثبيت أصل عن طريق تثبيته في موقع عمل جديد، اتبع الخطوات من 1 إلى 6 من هذا الإجراء. عند تثبيت أصل في موقع عمل جديد، يتم إلغاء تثبيت الأصل تلقائيًا من موقع العمل السابق. **لا** يتم نقل أي طلبات الصيانة أو أوامر العمل النشطة تم إنشاؤها على الأصل قبل تثبيته في موقع عمل جديد تلقائيًا إلى موقع العمل الجديد. إذا كانت طلبات الصيانة وأوامر العمل هذه لا تزال مطلوبة للأصل، يترتب عليك إعادة إنشائها يدويًا بعد تثبيت الأصل في الموقع الجديد.

7. لعرض قائمة بكافة الأصول، بما في ذلك الأصول الفرعية، المثبتة في موقع العمل، حدد موقع العمل في صفحة **جميع مواقع العمل**، ثم حدد **الأصول**.
8. لعرض قائمة بطلبات الصيانة النشطة أو أوامر العمل النشطة أو تسجيلات الخطأ المرتبطة بالأصول التي تم تثبيتها في موقع عمل، حدد موقع العمل في صفحة **جميع مواقع العمل**، ثم حدد **الطلبات**، أو **أوامر العمل**، أو **الأخطاء**.

> [!NOTE]
> عند تغيير البيانات المرتبطة بالأصول، يتم تحديثها تلقائيًا في موقع العمل الذي تم تثبيت الأصل فيه. يتعلق هذا التحديث التلقائي بالتغييرات في طلبات الصيانة، وأوامر العمل، وتسجيلات أخطاء الأصول، وتسجيلات وقت تعطل الصيانة، وتسجيلات قياس الأصول.

## <a name="automatically-create-one-asset-on-a-functional-location"></a>إنشاء أصل واحد تلقائيًا في موقع العمل

يمكنك إعداد مراحل مواقع العمل وأنواع مواقع العمل لمعالجة الإنشاء التلقائي لأصل *واحد* في موقع العمل. يحصل الأصل على نفس معرف واسم موقع العمل. قد تكون هذه الوظيفة مفيدة عندما تقوم بمعالجة الصيانة على أصل كبير وثابت، مثل المبنى.

قبل أن تتمكن من إنشاء أصل تلقائيًا في موقع عمل، يجب أن تكون بيانات الإعداد التالية متوفرة:

- قم بإنشاء نوع موقع العمل لمعالجة الإنشاء التلقائي لأصل. في حقل **نوع الأصل**، حدد معرف نوع أصل. لمزيد من المعلومات، راجع [أنواع مواقع العمل](../setup-for-functional-locations/functional-location-types.md).
- قم بإنشاء حالة دورة حياة موقع العمل لمعالجة الإنشاء التلقائي لأصل. عيّن الخيار **إنشاء أصل** إلى **نعم**. لمزيد من المعلومات، راجع [حالات دورة حياة مواقع العمل](../setup-for-functional-locations/functional-location-stages.md).

بعد توفر بيانات الإعداد، تكون جاهزًا لإنشاء أصل.

1. في الصفحة **جميع مواقع العمل**، تأكد من أن موقع العمل حيث تريد إنشاء الأصل تلقائيًا يستخدم نوع موقع العمل الذي قمت بإنشائه لهذا الغرض.
2. حدد موقع العمل في القائمة.
3. حدد **تحديث حالة موقع العمل**، ثم حدد حالة دورة الحياة التي قمت بإنشائها لهذا الغرض. يتم الآن التثبيت التلقائي لأصل واحد في موقع العمل. يحصل هذا الأصل على نفس اسم موقع العمل.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]