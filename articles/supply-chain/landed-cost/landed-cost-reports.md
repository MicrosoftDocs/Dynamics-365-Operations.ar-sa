---
title: تقارير التكلفة المستلمة
description: يوضح هذا المقال كيفية البحث عن الأنواع المختلفة من التقارير المتوفرة واستخدامها للوحدة النمطية للتكلفة المستلمة.
author: Weijiesa
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-02-21
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 836d6b538b32d818ed3b825000d004b005ce95d8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905939"
---
# <a name="landed-cost-reports"></a>تقارير التكلفة المستلمة

[!include [banner](../../includes/banner.md)]

## <a name="outstanding-invoices"></a>الفواتير المعلّقة

يحتوي تقرير الفواتير المعلقة على قائمة بجميع الفواتير المعلقة لمستويات التكلفة المختلفة المرتبطة بكل رحلة. ويستخدم لتسويه تكاليف الرحلات والرحلات معا مع قائمه حركات دفتر الأستاذ بصفه دوريه. بعد فوتره تكلفه الحمولة ، تتم ازالتها من التقرير.

لإنشاء تقرير الفواتير المعلقة ، اتبع هذه الخطوات.

1. انتقل إلى **التكلفة المستلمة \> التقارير \> التعقب \> الفواتير المعلقة**.
1. في مربع الحوار **الفواتير المعلقة**، في الحقل **اعتبارًا من التاريخ**، حدد تاريخًا. إيه فاتورة كانت مستحقه في هذا التاريخ أو قبله سيتم تضمينها في المخرجات.
1. ضمن **إظهار**، حدد أحد الخيارات التالية:

    - **التكلفة غير المفوتره** – قم بتضمين التكاليف للشحنات المفوتره التي لها قيمه تكلفه تقديريه ولكن لا توجد تكلفه فعليه.
    - **المخزون غير المفوتر** – قم بتضمين التكاليف التي تمت فوترتها ، ولكن لم يتم بعد استلام أمر الشراء له.
    - **لم تتم فوترة الكل** – قم بتضمين نتائج كلٍّ من خيار **التكلفة غير المفوترة** وخيار **المخزون غير المفوتر**.

1. قم بتعيين خيار **تضمين التكاليف الجديدة** إلى *نعم* لتضمين التكاليف التي لا تحتوي علي تكلفه فعليه، ولم يتم استلام هذا المخزون لها. في حاله تعيينه إلى *لا*، سيتضمن التقرير التكاليف التي تمت فوترتها فقط.
1. في قسم **العرض**، قم بتمكين كل نوع من التفاصيل التي تريد تضمينها في التقرير.
1. كما يمكنك القيام بالأنواع الأخرى من التقارير في Microsoft Dynamics 365 Supply Chain Management، استخدم علامة التبويب السريع **الوجهة** لتحديد تنسيق الإخراج الخاص بالتقرير.
1. كما تفعل مع الأنواع الأخرى من التقارير في Supply Chain Management، استخدم علامة التبويب السريع **السجلات المراد تضمينها** لتحديد السجلات التي سيتم تضمينها في التقرير.
1. حدد **موافق** لإنشاء التقرير.

## <a name="activityprovider-analysis-reports"></a>تقارير تحليل النشاط/المزود

تتيح لك تقارير تحليل النشاط/الموفر مراجعه دقه تقديرات الوقت الخاصة بك لكل موفر.

لإنشاء تقرير تحليل النشاط/المزود، اتبع هذه الخطوات.

1. استنادا إلى نوع التقرير الذي ترغب في إنشائه ، اتبع إحدي الخطوتين التاليتين:

    - انتقل إلى **التكلفة المستلمة \> التقارير \> تحليل النشاط/الموفر حسب النشاط**. في هذه الحالة ، سيتم تجميع التقديرات الزمنيه حسب النشاط.
    - انتقل إلى **التكلفة المستلمة \> التقارير \> تحليل النشاط/الموفر حسب الموفر**. في هذه الحالة ، سيتم تجميع التقديرات الزمنيه حسب الموفر.

    يظهر مربع الحوار **تحليل النشاط/الموفر حسب النشاط** أو مربع الحوار **تحليل النشاط/الموفر حسب الموفر**. ويوفر كل من مربعي الحوار نفس الخيارات.

1. كما يمكنك القيام بالأنواع الأخرى من التقارير في Supply Chain Management، استخدم علامة التبويب السريع **الوجهة** لتحديد تنسيق الإخراج الخاص بالتقرير.
1. كما تفعل مع الأنواع الأخرى من التقارير في Supply Chain Management، استخدم علامة التبويب السريع **السجلات المراد تضمينها** لتحديد السجلات التي سيتم تضمينها في التقرير.
1. حدد **موافق** لإنشاء التقرير.

## <a name="voyage-costing-reports"></a>تقارير تكاليف الرحلات.

تعرض تقارير "تكلفه الرحلة" تكلفه الأصناف وتكاليف الاستيراد لكل فليو أو حاويه شحن أو رحله، اعتمادا علي الخيارات التي تحددها عند إنشاء التقرير. ويتيح لك كل تقرير لتكاليف الرحلة عرض التكلفة المقدرة لرحله في مقابل التكلفة الفعلية ، كما يمكن تقسيمها بواسطة العديد من العوامل المعرفة.

لإنشاء تقرير تكلفة الرحلة، اتبع هذه الخطوات.

1. استنادا إلى نوع التقرير الذي ترغب في إنشائه ، اتبع إحدي الخطوتين التاليتين:

    - انتقل إلى **التكلفة المستلمة \> التقارير \> التكاليف \> تكاليف الرحلة حسب التكلفة الفردية**. في هذه الحالة ، سيعرض خيار التكلفة الفردية تكاليف الاستيراد لكل منطقه تكلفه حسب كود نوع التكلفة.
    - انتقل إلى **التكلفة المستلمة \> التقارير \> التكاليف \> تكاليف الرحلة حسب فئة التقارير**. وفي هذه الحالة ، سيتم تقسيم تكلفه الاستيراد إلى فئات التقارير المختلفة. يتم تجميع أنواع التكلفة حسب فئات إعداد التقارير.

    يظهر مربع الحوار **تكاليف الرحلة حسب التكلفة الفردية** أو مربع الحوار **تكاليف الرحلة حسب فئة التقارير‬‏‫**. مربعات الحوار هذه متشابهة. تتم الإشارة إلى أي اختلافات في باقي هذا الإجراء.

1. إذا قمت بفتح مربع الحوار **تكاليف الرحلة حسب فئة التقارير**، في حقل **التكلفة**، حدد إحدى القيم التالية:

    - **قيمة التكلفة** – يتم حساب القيمة باستخدام التكاليف التلقائية أو التي تم إنشاؤها يدويا في منطقه التكلفة.
    - **المقدرة** - بعد استلام البضائع ، يتم تعيين التكلفة المقدرة.
    - **الفعلية** -بعد فوتره الأمر ، يتم تعيين التكلفة الفعلية إلى التكلفة على الفاتورة.
    - **الأفضل** – سيقوم النظام باستخدام أي خيار من الخيارات الثلاثة السابقة يكون الأكثر دقه. (نوصي بتحديد هذا الخيار.)

1. قم بتعيين الخيار **حسب الصنف** إلى *نعم* لعرض تكلفة كل صنف. قم بتعيينه إلى *لا* لعرض التكاليف لكل رحلة.
1. في قسم **العرض**، حدد الفئات التي سيتم تقسيم التكلفة إليها.
1. في قسم **الأبعاد**، حدد الأبعاد لتضمينها في التقرير.
1. كما يمكنك القيام بالأنواع الأخرى من التقارير في Supply Chain Management، استخدم علامة التبويب السريع **الوجهة** لتحديد تنسيق الإخراج الخاص بالتقرير.
1. كما تفعل مع الأنواع الأخرى من التقارير في Supply Chain Management، استخدم علامة التبويب السريع **السجلات المراد تضمينها** لتحديد السجلات التي سيتم تضمينها في التقرير.
1. حدد **موافق** لإنشاء التقرير.

## <a name="shipping-container-receipts-list"></a>قائمة إيصالات حاوية الشحن

تحتوي قائمة إيصالات حاوية الشحن على جميع الكميات غير المستلمة المستحقة في تاريخ متوقع أو قبله. يمكن لفريق المستودع استخدام هذا التقرير لتحديد البضائع المتوقعة في أحدي حاويات الشحن. كما يمكن استخدامها أيضا للتحقق من صحة السلع يدويا عند استلامها علي أحدي حاويات الشحن.

لإنشاء قائمه عمليات استلام حاويه الشحن، اتبع الخطوات التالية.

1. انتقل إلى **التكلفة المستلمة \> التقارير \> التعقب \> قائمة عمليات استلام حاويات الشحن**.
1. في مربع الحوار **قائمة عمليات استلام حاويات الشحن**، في حقل **التاريخ المتوقع**، حدد تاريخًا. سيتم تضمين أي كميات لم يتم استلامها في هذا التاريخ أو قبله في الإخراج.
1. في قسم **الأبعاد**، حدد الأبعاد لتضمينها في التقرير.
1. كما يمكنك القيام بالأنواع الأخرى من التقارير في Supply Chain Management، استخدم علامة التبويب السريع **الوجهة** لتحديد تنسيق الإخراج الخاص بالتقرير.
1. كما تفعل مع الأنواع الأخرى من التقارير في Supply Chain Management، استخدم علامة التبويب السريع **السجلات المراد تضمينها** لتحديد السجلات التي سيتم تضمينها في التقرير.
1. حدد **موافق** لإنشاء التقرير.

## <a name="expected-delivery-report"></a>تقرير التسليم المتوقع

يحتوي تقرير التسليم المتوقع علي معلومات أساسيه حول الرحلة وحاويه الشحن والفليو والأصناف وتاريخ التسليم المتوقع.

لإنشاء تقرير تسليم متوقع ، اتبع هذه الخطوات.

1. انتقل إلى **التكلفة المستلمة \> التقارير \> التعقب \> التسليم المتوقع**.
1. في مربع حوار **التسليم المتوقع**، في حقل **التاريخ المتوقع**، حدد التاريخ عند توقع تسليم البضائع إلى مستودع الوجهة النهائي. سيتم تضمين أي خط رحلة له تاريخ متوقع في ذلك التاريخ أو قبله ، ولم يتم استلامه بعد ، في الإخراج.
1. اختياري: في حقل **حساب المورد**، حدد حساب مورد لتضمين عمليات التسليم من مورد معين فقط.
1. في قسم **الأبعاد**، حدد الأبعاد لتضمينها في التقرير.
1. كما يمكنك القيام بالأنواع الأخرى من التقارير في Supply Chain Management، استخدم علامة التبويب السريع **الوجهة** لتحديد تنسيق الإخراج الخاص بالتقرير.
1. كما تفعل مع الأنواع الأخرى من التقارير في Supply Chain Management، استخدم علامة التبويب السريع **السجلات المراد تضمينها** لتحديد السجلات التي سيتم تضمينها في التقرير.
1. حدد **موافق** لإنشاء التقرير.
