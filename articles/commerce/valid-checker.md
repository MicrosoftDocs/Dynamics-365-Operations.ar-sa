---
title: مدقق تناسق حركة البيع بالتجزئة
description: يصف هذا الموضوع وظيفة مدقق تناسق الحركة في Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 10/07/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 869230c0003735c1e9f48170a16ca9409a9edc19
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976530"
---
# <a name="retail-transaction-consistency-checker"></a>مدقق تناسق حركة البيع بالتجزئة

[!include [banner](includes/banner.md)]

يصف هذا الموضوع وظيفة مدقق تناسق الحركة في Microsoft Dynamics 365 Commerce. يحدد مدقق التناسق الحركات غير المتناسقة ويعزلها قبل انتقائها من قبل عملية ترحيل كشف الحساب.

عند ترحيل كشف حساب، قد يفشل الترحيل بسبب وجود بيانات غير متناسقة في جداول حركات التجارة. قد يعود سبب المشكلة في البيانات إلى ظهور مشاكل غير متوقعة في تطبيق نقطة البيع (POS)، أو إذا تم استيراد الحركات بشكل غير صحيح من أنظمة نقطة البيع الخارجية. تشتمل الأمثلة حول كيفية ظهور حالات عدم التناسق هذه على ما يلي: 

- إجمالي الحركة في جدول الرأس غير متطابق مع إجمالي الحركة في البنود.
- عدد البنود في جدول الرأس غير متطابق مع عدد البنود في جدول الحركة.
- الضرائب في جدول الرأس غير متطابقة مع قيمة الضريبة في البنود. 

عندما تنتقي عمليات ترحيل كشوف الحسابات حركات غير متناسقة، يتم إنشاء دفاتر يومية دفعات وفواتير مبيعات غير متناسقة، وتفشل عملية ترحيل كشف الحساب بكاملها نتيجة لذلك. تشتمل عملية استرداد كشوف الحسابات من حالة من هذا النوع على عمليات إصلاح معقدة للبيانات عبر جداول حركات متعددة. يمنع مدقق تناسق الحركة حدوث مثل هذه المشاكل.

يوضح المخطط التالي عملية الترحيل باستخدام مدقق تناسق الحركة.

![عمليه ترحيل كشف الحساب مع مدقق تناسق الحركة](./media/validchecker.png "عمليه ترحيل كشف الحساب مع مدقق تناسق حركة البيع بالتجزئة")

تدقق العملية الدُفعية **التحقق من صحة الحركات** في تناسق جداول حركات التجارة للسيناريوهات التالية.

- **حساب العميل** – التأكد من أن حساب العميل في جداول الحركات موجود في المقر الرئيسي للعميل.
- **عدد البنود** – التأكد من أن عدد البنود، كما تم تسجيله في جدول رأس الحركة، يتطابق مع أرقام البنود في جداول حركة مبيعات.
- **يتضمن السعر الضريبة** – التحقق من أن **السعر يشتمل علي معلمة ضريبة** متسقة مع بنود الحركة والسعر في بند المبيعات ومتوافق مع سعر يتضمن الضريبة وتكوين الإعفاء الضريبي.
- **مبلغ الدفع** - يتحقق من أن سجلات الدفع تطابق مبلغ الدفع في الرأس، وفي الوقت نفسه بيع الديون في التكوين مقابل التقريب النقدي في دفتر الأستاذ العام.
- **المبلغ الإجمالي** – يتحقق من أن المبلغ الإجمالي في الرأس هو مجموع صافي المبالغ الموجودة في البنود بالإضافة إلى مبلغ الضريبة، وفي الوقت نفسه بيع الديون في التكوين مقابل التقريب النقدي في دفتر الأستاذ العام.
- **صافي المبلغ** – يتحقق من أن المبلغ الإجمالي في الرأس هو مجموع صافي المبالغ الموجودة في البنود بالإضافة إلى مبلغ الضريبة، وفي الوقت نفسه بيع الديون في التكوين مقابل التقريب النقدي في دفتر الأستاذ العام.
- **دفع بالزيادة/بالنقصان‬** – التأكد من أن الفرق بين إجمالي المبلغ على الرأس ومبلغ الدفع لا يتجاوز تكوين دفع بالزيادة/بالنقصان، وفي الوقت نفسه بيع الديون في التكوين مقابل التقريب النقدي في دفتر الأستاذ العام.
- **مبلغ الخصم** – التأكد من تناسق مبلغ الخصم في جداول الخصم ومبلغ الخصم في جداول بنود حركة البيع بالتجزئة، وأن مبلغ الخصم في الرأس هو مجموع مبالغ الخصم في البنود، وفي الوقت نفسه بيع الديون في التكوين مقابل التقريب النقدي في دفتر الأستاذ العام.
- **خصم البند** – التأكد من أن خصم البند على بند الحركة هو مجموع كافة البنود في جدول الخصم الذي يتوافق مع بند الحركة.
- **صنف بطاقة الهدايا‬** – لا يدعم Commerce إرجاع أصناف بطاقة الهدايا. ومع ذلك، يمكن صرف الرصيد في بطاقة الهدايا. عند معالجة صنف بطاقة هدايا كبند مرتجع بدلاً من بند مصروف، فهو يفشل في عملية ترحيل كشوف الحسابات. تضمن عملية التحقق من الصحة التي تتم على أصناف بطاقة الهدايا أن تكون فقط عناصر بنود بطاقة الهدايا المرتجعة على جداول الحركات هي البنود المصروفة في بطاقة الهدايا.
- **السعر السالب** – يتحقق من عدم وجود بنود حركة ذات سعر سالب.
- **الصنف والمتغير** – التأكد من أن الأصناف والمتغيرات في بنود الحركة موجودة في الملف الرئيسي للصنف والمتغير.
- **مبلغ الضريبة** - التحقق من مطابقة سجلات الضريبة‏‎ مع مبالغ الضريبة على البنود.
- **الرقم التسلسلي** - التحقق من وجود الرقم التسلسلي في بنود الحركة للأصناف التي يتم التحكم فيها بواسطة الرقم التسلسلي.
- **علامة‬** - التحقق من أن العلامة على الكمية وصافي المبلغ هي نفسها في جميع بنود الحركة.
- **تاريخ العمل** - التحقق من أن الفترات المالية لجميع تواريخ العمل الخاصة بالحركات مفتوحة.
- **المصاريف** - التحقق من توافق مبلغ الرأس وتكلفة البند، بما في ذلك تكوين الضريبة، بما في ذلك الضريبة وتكون الإعفاء الضريبي.

## <a name="set-up-the-consistency-checker"></a>إعداد مدقق التناسق

قم بتكوين العملية الدُفعية "التحقق من صحة حركات المتجر‬" في **Retail وCommerce \> تكنولوجيا معلومات Retail وCommerce \> ترحيل نقطة البيع**، لعمليات التشغيل الدورية. يمكن جدولة الوظيفة الدُفعية استنادًا إلى التدرج الهرمي للمؤسسات في المتجر، بطريقة مماثلة لكيفية إعداد العمليتين "حساب الكشوف على دُفعات‬" و"ترحيل الكشوف على دُفعات‬". من المستحسن تكوين هذه العملية الدُفعية لتشغيلها عدة مرات في اليوم وجدولتها بحيث يتم تشغيلها في نهاية كل تنفيذ لوظيفة P.

## <a name="results-of-validation-process"></a>نتائج التحقق من الصحة

توضع علامة نتائج التحقق من الصحة التي تقوم بها العملية الدُفعية على الحركة المناسبة. يكون الحقل **حالة التحقق من الصحة** على سجل الحركة معينًا إلى **ناجح‬** أو **خطأ**، ويظهر تاريخ تشغيل عملية التحقق من الصحة الأخيرة في الحقل **وقت آخر عملية تحقق من الصحة**.

لعرض نص وصفي للخطأ المتعلق بفشل التحقق من الصحة، حدد سجل حركة المتجر الملائم، ثم انقر فوق الزر **أخطاء التحقق من الصحة**.

لن تتضمن كشوف الحسابات الحركات التي لم تنجح في عملية التحقق من الصحة والحركات التي لم يتم بعد التحقق من صحتها. أثناء عملية "حساب كشف الحساب"، سيتم يتم إبلاغ المستخدمين عن وجود حركات كان يجب تضمينها في كشف الحساب ولكن لم يتم تضمينها فيه.

إذا تم العثور على خطأ يتعلق بالتحقق من الصحة، فإن الطريقة الوحيدة لإصلاحه هو الاتصال بدعم Microsoft. في إصدار مستقبلي، سنضيف ميزة تسمح للمستخدمين بإصلاح السجلات التي فشلت عبر واجهة المستخدم. وسنوفر أيضًا قدرات التسجيل والتدقيق لتتبع محفوظات التعديلات.

> [!NOTE]
> سنضيف المزيد من قواعد التحقق من الصحة لدعم سيناريوهات إضافية في إصدار مستقبلي.


[!INCLUDE[footer-include](../includes/footer-banner.md)]