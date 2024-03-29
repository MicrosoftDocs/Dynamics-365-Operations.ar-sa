---
title: وحدة القياس وسياسات المخزون
description: توضح هذه المقالة كيفية استخدام الوحدات الافتراضية وتسلسلات الوحدات وتحويلات الوحدات في عمليات المستودع.
author: perlynne
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetails, EcoResProductDetailsExtended, EcoResStorageDimensionGroup, InventItemOrderSetup, UnitOfMeasureConversion, WHSRFMenuItem, WHSUOMSeqGroupTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 29611
ms.assetid: 4b5ca875-9a06-416d-9ac0-cc3ab8f7338e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca1c18a293d66ab78f41cac857461249826ce4c9
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069111"
---
# <a name="unit-of-measure-and-stocking-policies"></a>وحدة القياس وسياسات المخزون

[!include [banner](../includes/banner.md)]

توضح هذه المقالة كيفية استخدام الوحدات الافتراضية وتسلسلات الوحدات وتحويلات الوحدات في عمليات المستودع.

تحدد مجموعات تسلسلات الوحدة تسلسل الوحدات التي يمكن استخدامها في عمليات المستودع. ‏‫ويتم إنشاؤها في صفحة **مجموعات تسلسلات الوحدات**. ويوضح التسلسل العلاقة بين الوحدات المختلفة.‬ على سبيل المثال، يمكنك تخزين البالتات التي تحتوي على مربعات تحتوي على أجزاء فردية من الأصناف. وفي هذه الحالة، يجب توفير الوحدات الثلاث المختلفة والترتيب المنطقي للطبقات. وتتيح لك مجموعات تسلسلات الوحدات إمكانية تحديد سياسات تجميع لوحات الترخيص، والوحدات الافتراضية التي يجب استخدامها لعمليات المستودع المختلفة. تنطبق هذه المقالة على كل من عمليات إدارة المستودعات (WMS) المتوفرة في وحدة إدارة المستودعات وحل التخزين الأساسي المتاح في وحدة إدارة المخزون.

## <a name="unit-sequence-groups-for-released-products"></a>مجموعات تسلسلات الوحدات للمنتجات الصادرة
إذا كنت تريد استخدام المنتجات الصادرة في عمليات العمل في المستودع، يجب تعيين مجموعة تسلسلات الوحدة لها. وفي حالة التحقق من صحة منتج مقترن بمجموعة أبعاد تخزين، وتم تعيين خيار **استخدام عمليات إدارة المستودع** لمجموعة أبعاد التخزين إلى **نعم**، تتلقى رسالة خطأ، إذا لم يتم تحديد معرف مجموعة تسلسل وحدة للمنتج. وإذا احتوت مجموعة تسلسلات الوحدة التي تستخدمها على بنود متعددة (وبالتالي وحدات متعددة)، يجب عليك إعداد تحويل وحدة بين الوحدات. ويمكنك إكمال هذا الإعداد في صفحة **تحويلات الوحدات**. ويجب أن تطابق أصغر وحدة في مجموعة التسلسلات التي تقوم بإقرانها بمنتج صادر وحدة المخزون التي تم تحديدها للمنتج المطابق. ووحدة المخزون هي الوحدة المستخدمة لعمليات الحساب الأساسية للمخزون الفعلي. ويمكنك أيضًا إعداد تحويلات وحدة القياس لمتغيرات المنتج لأصول المنتجات من خلال استخدام خيار **تمكين تحويلات وحدة القياس**.

## <a name="license-plate-grouping"></a>مجموعة لوحة الترخيص
يمكنك تحديد ما إذا كان يجب تجميع إيصالات الكميات الأقل من أو الأكثر من وحدة محددة في لوحة ترخيص واحدة أو تقسيمها إلى لوحة ترخيص منفصلة لكل وحدة. ولإعداد هذا السلوك، استخدم خيار **تجميع لوحات الترخيص** في علامة التبويب **تفاصيل البند** في صفحة **مجموعات تسلسلات الوحدات**. إذا كنت تريد استخدام مجموعة لوحات الترخيص عند قيامك معالجة العمل باستخدام جهاز محمول، فإنه يجب عليك خيار **مجموعة لوحات الترخيص** في صنف قائمة **الجهاز المحمول**. على سبيل المثال، إنك تستخدم جهازًا محمولاً لتسجيل صنف مقترن بمجموعة تسلسلات وحدة تشمل بندين. البند الأول للقطع، ويتم تعيين خيار **مجموعات لوحات الترخيص** إلى **نعم**. والبند الثاني مخصص لوحدة البالتة، ويتم تعيين خيار **مجموعات لوحات الترخيص** إلى **لا**. وفي هذه الحالة، يمكن أن يوجه النظام تلقائياً تقسيم وإنشاء لوحات الترخيص لكل 100 قطعة.

## <a name="units-for-cycle-counting"></a>وحدات الجرد الدوري
لتحديد الوحدات التي يجب استخدامها كجزء من عمليات الجرد الدوري، حدد خيار **استخدام وحدة الجرد الدوري‬** في صفحة **مجموعات تسلسلات الوحدات**. يمكنك تحديد أربع وحدات كحد أقصى في مجموعة التسلسلات. إذا قمت بتحديد أكثر من أربع وحدات، فلن تظهر الوحدات الإضافية على الجهاز المحمول.

## <a name="default-units-for-mobile-device-receiving-processes"></a>عمليات استلام الوحدات الافتراضية للأجهزة المحمولة
لتعيين الوحدات الافتراضية التي يجب استخدامها لعمليات الاستلام على الأجهزة المحمولة، قم بتمكين خياري **الوحدة الافتراضية للشراء والتحويل** و **الوحدة الافتراضية للإنتاج** في صفحة **مجموعات تسلسلات الوحدات**. على سبيل المثال، يمكنك بشكل افتراضي تحديد أن النظام يجب أن يستخدم كميات بالتات عند استلام المخزون الفعلي لأمر الشراء باستخدام جهاز محمول، ولكن يجب أن تكون وحدة الاحتفاظ بالمخزون قطعًا. للحصول على التحويل لعدد القطع التي تحتوي عليها كل بالته، يجب عليك تحديد تحويل وحدة، مثل أجهزة 100 قطعة = بالتة واحدة.

## <a name="default-order-settings"></a>إعدادات الأوامر الافتراضية
وكجزء من إنشاء المنتجات الصادرة، يجب تحديد الوحدات الافتراضية للمشتريات والمبيعات والمخزون لمعالجة العديد من الأوامر. ويمكنك تعيين الوحدات الافتراضية والكميات لمستندات المصدر المختلفة باستخدام صفحتي **إعدادات الأوامر الافتراضية** و **إعدادات الأوامر الخاصة بالموقع**. ويمكنك الوصول إلى هذه الصفحات من صفحة **المنتجات التي تم إصدارها**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]