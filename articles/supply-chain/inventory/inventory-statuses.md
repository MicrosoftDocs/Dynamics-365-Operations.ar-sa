---
title: حالات المخزون
description: توضح هذه المقالة كيفية استخدام حالات المخزون لتصنيف المخزون وتعقبه.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, WHSInventStatus, WHSWarehouseStatusChange
audience: Application User
ms.reviewer: kamaybac
ms.custom: 21331
ms.assetid: b35f495f-de4f-48a0-9d09-4d06781d7650
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0c4cad56389c7a8fd6d37591c1ff335fff715707
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001814"
---
# <a name="inventory-statuses"></a>حالات المخزون

[!include [banner](../includes/banner.md)]

توضح هذه المقالة كيفية استخدام حالات المخزون لتصنيف المخزون وتعقبه.

## <a name="set-up-and-use-inventory-statuses"></a>اعداد حالات المخزون واستخدامها

يمكنك استخدام حالات المخزون لتصنيف المخزون. ويمكنك فيما بعد بدء الإجراءات المناسبة، مثل عمل الإبعاد أو التزويد.

وفيما يلي بعض الأمثلة على طرق استخدام حالات المخزون:

- إنشاء حالات المخزون المتوافر والحركات الصادرة والحركات الواردة.
- تحديد حالة مخزون افتراضي لحركات المستودع.
- قم بتغيير حالة مخزون للأصناف قبل وصولها، أو أثناء الوصول، أو عندما يتم تخزين الأصناف خلال حركة المخزون.
- استخدام حالة مخزون لأصناف الأسعار عند إرجاعها ولتخطيط تغطية الصنف أثناء التخطيط الرئيسي.

حالة مخزون هي أحد الأبعاد في مجموعة أبعاد التخزين. يمكن تصنيف حالات المخزون على أنها متوفرة أو غير متوفرة، ويمكنك استخدام معلمة **حظر المخزون** لحظر الأصناف التي تكون بحالة مخزون غير متوفر. وتعتبر الأصناف ذات حالة محظورة هي المخزون الفعلي ولا يمكن استخدامها في أمر الإنتاج أو أمر التوريد، أمر التحويل أو الحركة الصادرة.

يمكنك استخدام أصناف المستودع بحالات المخزون متوفرة أو غير متوفرة للعمل الوارد. على سبيل المثال، يمكنك إنشاء حالة متاحة باسم *جاهزة*، وتتم تسمية الحالة غير المتاحة باسم *تالفة*، وتُسمى حالة محظورة باسم *محظورة*. وعند إنشاء أمر شراء للأصناف المستلمة أو المرتجعة، إذا كانت أي أصناف تالفة أو مقطوعة، فيمكنك تغيير حالة المخزون لتلك الأصناف إلى *تالفة* في بند أمر الشراء. وبعد تلقي هذه الأصناف، يتم تعيين الحالة تلقائياً إلى *محظورة*. وفي حالة مسح الأصناف التالفة باستخدام جهاز محمول، بإمكان Supply Chain Management استخدام توجيهات الموقع وقوالب العمل لإظهار معلومات حول الموقع المناسب أو مجموعة من المواقع حيث يمكنك إبعاد تلك الأصناف. وبالنسبة للاصناف المرتجعة، يتم إنشاء نوع الإصدار *حجز* في صفحة **حركات المخزون**.

وبالنسبة للعمل الصادر، استخدم أصنافًا بحالة مخزون متوفر. إذا كان لديك أصناف ذات حالة *معطلة*, ويعمل التخطيط الرئيسي على هذه الأصناف، تعتبر الأصناف مفقودة ويتم تزويد المخزون تلقائياً.

وبعد إعداد حالات المخزون، يمكنك تعيين حالة المخزون الافتراضية للموقع والصنف والمستودع. كما يمكنك تعيين حالة افتراضية لأوامر المبيعات والتحويل والشراء. ولا يمكن أن تكون الحالة الافتراضية لأوامر المبيعات وأمر التحويل الصادر في خيار **حظر المخزون** قم تعيينها إلى *نعم*. وحالة المخزون تكون موروثة من الإعدادات الافتراضية في موقع أو مستودع أو صنف أو أمر شراء أو أمر تحويل أو أمر مبيعات ويمكن تغييرها باستخدام الجهاز المحمول أو في بند أمر التحويل أو أمر الشراء أو أمر المبيعات.

ولتخطيط تغطية الأصناف التي تكون بحالة مخزون متوفر، حدد خيار **خطة التغطية حسب البعد** لبُعد تخزين في صفحة **مجموعات أبعاد التخزين**. وعند فتح معالج **تغطية الصنف**، تظهر الأصناف التي تكون بحالة متاحة في صفحة **الحالة**. لإنشاء إعدادات تغطية لهذه الأصناف، حدد معرف حالة المخزون لحالات المخزون المتاحة. استناداً إلى إعدادات التغطية، يمكنك حساب متطلبات الصنف والتنبؤ بالعرض والطلب والأصناف المتوفرة أثناء التخطيط الرئيسي. لا يمكنك إنشاء إعداد تغطية صنف بحالة مخزون محظور. وبدلاً من ذلك، استخدم صفحة **تغطية الصنف** لإنشاء أو تعديل معلمات تغطية الصنف.

## <a name="change-inventory-statuses"></a>تغييرات حالة المخزون

يمكنك تغيير حالات المخزون اما باستخدام صفحه **الموقع الفعلية بواسطة** أو باستخدام المهمة الدورية *تغيير حاله المخزون*.

- عند استخدام المهمة الدورية *تغيير حاله المخزون*، يمكنك تحديد السجلات التي تريد تضمينها وتعيين المهمة لتعمل في المجموعة في الفاصل المطلوب.
- لتغيير حاله المخزون كعمليه عند الطلب، انتقل إلى الصفحة **الكمية الفعلية حسب الموقع**، وحدد السجلات المناسبة، ثم حدد الزر **تغيير حاله المخزون**.

> [!NOTE]
> تسمح ميزة *تغيير حاله المخزون للأصناف التي يتم التحكم فيها بواسطة ميزه الابعاد الخاصة بالتعقب* بتغيير حاله المخزون للأصناف التي يتم التحكم فيها من خلال تعقب الابعاد ، بما في ذلك القدرة علي تحديث السجلات المحددة فقط. استخدم [أداره الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) لتمكين الميزة حسب الحاجة. عند تمكين الميزة ، ستتمكن من القيام بما يلي:
>
> - في الصفحة **الكمية الفعلية حسب الموقع** ، يمكنك تجميع البنود استنادا إلى الابعاد المعروضة باستخدام الزر **عرض الابعاد** وتغيير حاله البنود المحددة.
> - في الصفحة **الكمية الفعلية حسب الموقع**، يمكنك تحديد سجلات متعددة ثم استخدام الزر **تغيير حاله المخزون** لتغيير كافة السجلات في نفس الوقت.
> - في المهمة الدورية **تغيير حاله المخزون** ستتمكن من التصفية حسب ابعاد التعقب.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]