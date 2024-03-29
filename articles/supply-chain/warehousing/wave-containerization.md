---
title: التعبئة في حاويات
description: يصف هذا المقال كيفية جعل تعبئة الأحمال في الحاويات عملية تلقائية. تنشئ التعبئة في الحاويات المؤتمتة حاويات وعمل الانتقاء للشحنات عند معالجة موجة.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable, WHSContainerizatonHistory, WHSContainerPackingPolicyChange, WHSManifestShipmentContainers, WHSAllowedContainerTypeGroup, WHSPostMethod, WHSContainerCreateDialog, WHSContainerCloseDiag, WHSContainer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 4bdd13d794f01c9971ee1bcbdf206bff6b526afa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880411"
---
# <a name="containerization"></a>التعبئة في حاويات

[!include [banner](../includes/banner.md)]

يصف هذا المقال كيفية جعل تعبئة الأحمال في الحاويات عملية تلقائية. تنشئ التعبئة في الحاويات المؤتمتة حاويات وعمل الانتقاء للشحنات عند معالجة موجة.

لإعداد التعبئة في الحاويات، يجب عليك إنشاء التالي:

- **نوع الحاوية** ─ تعريف الخصائص المادية للحاويات. استخدام أنواع الحاويات لحزم أصناف المخزون في نوع وحجم معين من العبوات، مثل صناديق أم بالتات.
- **مجموعات الحاويات** ─ إنشاء مجموعات أنواع الحاويات المتشابهة. على سبيل المثال، يمكن أن تتضمن مجموعة الحاويات أنواع الحاويات ذات أبعاد الحجم المتشابهة. تحدد مجموعة الحاويات التسلسل الذي سيتم حزم الحاويات فيه، ونسبة تعبئة كل حاوية.
- **قالب بنية الحاوية** ─ قم بإنشاء قوالب تحدد قواعد التعبئة في الحاويات. على سبيل المثال، قواعد لخلط المخزون وغيرها من استراتيجيات التعبئة.
- **قوالب الموجات** – إعداد واحد أو أكثر من قوالب الموجة لإنشاء عمل الانتقاء للتعبئة في الحاويات.

## <a name="create-wave-templates-for-containerization"></a>إنشاء قوالب الموجات للتعبئة في الحاويات

يجب عليك إعداد واحد أو أكثر من قوالب موجة الشحن للتعبئة في الحاويات. تتضمن قوالب الموجة المعايير التي تحدد ما يلي:

- كيفية معالجة الموجات. يمكن القيام بذلك يدويًا أو تلقائيًا.
- كيفية إنشاء عمل الانتقاء. يتم تحديد هذا بأساليب الموجة. يجب أن يتضمن قالب الموجة أسلوب **التعبئة في الحاويات**.
- كيفية تطابق سطور التوزيع أو الأصناف بالموجة.

لمزيد من المعلومات، راجع [قوالب الموجات](wave-templates.md).

## <a name="create-container-types"></a>إنشاء أنواع الحاويات

استخدم أنواع الحاويات لإنشاء أوصاف الحاويات، بما في ذلك الحد الأقصى لقيم أبعاد الحجم الفعلي وقدرة الوزن. عند معالجة موجة معبئة في حاويات، يتم إنشاء الحاويات استنادًا إلى معلومات نوع الحاوية.

لإعداد نوع حاوية، اتبع هذه الخطوات:

1. انتقل إلى **إدارة المستودعات** \> **إعداد** \> **الحاويات** \> **نوع الحاوية**.
1. حدد **جديد** لإنشاء نوع حاوية جديدة.
1. أدخل معرفًا فريدًا ووصفًا لنوع الحاوية.
1. في حقل **وزن الفارغ‬**، أدخل الوزن الفعلي أو المقدر للحاوية.
1. في **الحد الأقصى للوزن**، أدخل الحد الأقصى للوزن الذي يمكن أن تتحمله الحاوية.
1. في حقول **الحد الأقصى لحجم التعبئة في الحاويات**، و **الحد الأقصى لطول التعبئة في الحاويات**، و **الحد الأقصى لعرض التعبئة في الحاويات**، و **الحد الأقصى لارتفاع التعبئة في الحاويات**، حدد الأبعاد المادية للحاوية.

    > [!NOTE]
    > قيم الطول والعرض قابلة للتبادل. وهذا يعني أنه يمكنك تدوير الأصناف أفقيًا أو على المحور س، إذا لزم الأمر. على سبيل المثال، إذا كان الطول 2 قدم، والعرض قدم واحد، يمكنك تغيير الطول إلى قدم واحد والعرض إلى قدمين. لاحظ أنه لا يتم تطبيق هذا لبعد الارتفاع. لا يمكنك تغيير قيمة الارتفاع لتدوير صنف عموديًا.

1. حدد قيم السمة المخصصة للحاوية في حقول السمات. السمات هي القيم المخصصة التي يتم استخدامها لتصفية أو فرز الأصناف استنادًا إلى قيمة غير متوفرة. على سبيل المثال، إذا كنت ترغب في حزم الأصناف لعميل معين، يمكنك إنشاء سمة لاسم العميل. يمكنك إنشاء السمات في صفحة **سمات الحاوية**.

## <a name="create-container-groups"></a>إنشاء مجموعات الحاويات

يمكنك إعداد مجموعات منطقية من أنواع الحاويات. لكل مجموعة، يمكنك تحديد التسلسل الذي يتم حزم الحاويات فيه، والنسبة المئوية للحاويات المراد تعبئتها. تُستخدم أبعاد حجم الصنف لتحديد ما إذا كان سيتم احتواؤه في حاوية أم لا. يتم استخدام الحاوية الأقرب إلى أبعاد حجم الصنف المستخدم. إذا كان لديك أنواع متعددة من الحاويات في مجموعة، نوصي بترتيب التسلسل حسب الحجم، حيث تكون الحاوية الأكبر أولاً، أي رقم 1 في التسلسل والحاوية الأصغر تكون الأخيرة.

لإعداد مجموعة حاويات، اتبع هذه الخطوات:

1. انتقل إلى **إدارة المستودعات** \> **إعداد** \> **الحاويات** \> **مجموعات الحاويات**.
1. حدد **جديد** لإنشاء مجموعة حاويات.
1. أدخل معرفًا فريدًا ووصفًا لمجموعة الحاويات.
1. في علامة التبويب السريع **التفاصيل**، حدد **جديد** لإضافة نوع حاوية للمجموعة.
1. في حقل **نوع الحاوية**، حدد نوع حاوية.
1. حدد **تحريك لأعلى** أو **تحريك لأسفل** لتحديد التسلسل الذي يتم تعبئة أنواع الحاويات فيه.

## <a name="create-container-build-templates"></a>إنشاء قوالب بنية الحاوية

يمكنك إعداد قواعد لعملية التعبئة في الحاويات، مثل قواعد خلط المخزون وغيرها من استراتيجيات التعبئة. على سبيل المثال، يمكنك إعداد قاعدة حيث إن العمال لا يمكنهم حزم سطور التوزيع التي تمثل أوامر المبيعات من عملاء مختلفين في نفس الحاوية.

لإعداد قالب إنشاء حاوية، اتبع هذه الخطوات:

1. انتقل إلى **إدارة المستودعات** \> **إعداد** \> **الحاويات** \> **قالب بنية الحاوية**.
1. إنشاء قالب بنية حاوية جديد.
1. في حقلي **اسم التعبئة في الحاوية** و **الرقم المسلسل**، أدخل اسم قالب التعبئة في الحاويات والترتيب المطابق لبنود التوزيع.

    > [!NOTE]
    > سيطبق النظام القالب الأول الذي يطابق سطر التوزيع معايير الاستعلام الخاصة به. لذلك، ضع القالب مع المعايير الأكثر تحديدًا في أعلى القائمة. كلما كانت المعايير أشمل، على الأرجح أن سطر التوزيع سوف يطابق المعايير. قد يؤدي هذا إلى تعيين السطور إلى الحاوية غير الصحيحة. عند الحاجة، يمكنك تحديد **تحريك لأعلى** أو **تحريك لأسفل** لتغيير ترتيب تسلسل القوالب.

1. في **معرف مجموعة الحاوية**، حدد مجموعة الحاويات التي يتم إنشاء الحاويات منها.
1. في حقل **أنواع استعلامات الأساس**، حدد نوع الاستعلام الذي يحدد ما سيتم حزمه وما الذي سيسند إليه عامل تصفية الاستعلام. وتتوفر الخيارات التالية:

      - **بند توزيع المبيعات** ─ بنود توزيع الحزم التي تم إنشاؤها لأوامر المبيعات.
      - **بند توزيع النقل** ─ بنود توزيع الحزم التي تم إنشاؤها لأوامر النقل.
      - **الحاوية** ─ تعبئة حاوية تم إنشاؤها مسبقًا بعملية التعبئة في الحاويات. على سبيل المثال، يتم استخدام هذا لتداخل الحاويات.

        > [!NOTE]
        > لاستخدام حاويات التداخل، يجب إجراء أسلوب التعبئة في الحاويات بشكل متكرر. لمزيد من المعلومات، راجع [قوالب الموجات](wave-templates.md).

1. في علامة التبويب السريع **عام**، في حقل **رمز خطوة الموجة**، أدخل المعرف الفريد لأسلوب عملية الموجة الذي يربط قالب إنشاء الحاوية بخطوات في قالب موجة.ف
1. حدد خانة الاختيار **السماح بتقسيم الانتقاءات** للسماح للعمال بحزم الأصناف من أمر عمل في حاويات منفصلة. وهذا يتطلب أن تكون الكمية كلها ملائمة للحاوية. يتم دائمًا استخدام أكبر وحدة قياس في سطر التوزيع.
1. في حقل **التعبئة حسب الوحدة**، حدد وحدة القياس التي ستمثل الحاوية. على سبيل المثال، يمكنك الإشارة إلى أن الوعاء حاوية. إذا قمت بحزم بوحدة القياس، فلا يمكنك تحديد مجموعة حاويات لأن وحدة القياس هي الحاوية.
1. في حقل **إستراتيجية تعبئة الحاويات**، حدد إستراتيجية الحزم التي سيتم استخدامها. وتتوفر الخيارات التالية:

    > [!NOTE]
    > تطبيق الإستراتيجية فقط على سطور توزيع المبيعات وسطور توزيع النقل.

      - **التعبئة في جميع الحاويات المفتوحة** – يقوم النظام بتقييم ما إذا كان سطر التوزيع يلاءم أي حاوية تم إنشاؤها أثناء دورة التعبئة في الحاويات.
      - **التعبئة في الحاوية الحالية فقط** – يقوم النظام بتقييم فقط ما إذا كان سطر التوزيع يلاءم الحاوية الأحدث إنشاءً.

    لمزيد من المعلومات والأمثلة التي تظهر كيفية العمل مع استراتيجيات تعبئة الحاوية، راجع [استراتيجيات تعبئة الحاوية](container-packing-strategy-overview.md).

1. لإعداد قواعد لتعبئة بنود التوزيع في حاويات، حدد **فواصل منطق الخلط**. على سبيل المثال، يمكنك إنشاء قاعدة التي سوف تسمح للعمال بحزم سطور التوزيع لصنفين مختلفين في نفس الحاوية. لتعريف قاعدة خلط، اتبع الخطوات التالية:

    1. في صفحة **فواصل منطق الخلط**، حدد **جديد**.
    1. في حقل **الجدول**، حدد الجدول الذي يحتوي على الحقل لاستخدامه كمعيار لفصل منطق الخلط.
    1. في حقل **تحديد الحقل**، حدد الحقل الذي سيتم استخدامه كمعيار لفصل منطق الخلط.
    1. كرر هذه الخطوات حتى يتم إضافة جميع المعايير لفصل منطق مزج.

    > [!NOTE]
    > إذا كنت تستخدم منطق خلط، نوصي بالفرز حسب نفس الحقول الموجودة في استعلام معايير عامل التصفية. وهذا سيقلل عدد الحاويات التي تم إنشاؤها.
