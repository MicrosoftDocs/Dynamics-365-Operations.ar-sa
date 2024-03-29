---
title: إعادة توزيع إقرار الإيرادات - السيناريو 4
description: يستعرض هذا المقال سيناريو إعادة التوزيع حيث يتم إزالة بند من أمر مبيعات موجود تمت فوترته جزئيًا. يؤدي هذا السيناريو إلى النتيجة نفسها، بغض النظر عما إذا كانت قد تمت إزالة البند من أمر المبيعات أو تم تعيينه إلى حالة تم الإلغاء.
author: bking
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: bking
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 8ec28460319e7bfabe82261ee4ed7861c4b6eb11
ms.sourcegitcommit: 1909d18a74cef85aad020a6a7473281e451f58c7
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348256"
---
# <a name="revenue-recognition-reallocation--scenario-4"></a>إعادة توزيع إقرار الإيرادات - السيناريو 4

[!include [banner](../includes/banner.md)]

يستعرض هذا المقال سيناريو إعادة التوزيع حيث يتم إزالة بند من أمر مبيعات موجود تمت فوترته جزئيًا. يؤدي هذا السيناريو إلى النتيجة نفسها، بغض النظر عما إذا كانت قد تمت إزالة البند من أمر المبيعات أو تم تعيينه إلى حالة تم الإلغاء.

بالنسبة لهذا السيناريو، يتم تعيين خيار **ترحيل تصحيحات الفواتير إلى الحسابات المدينة** إلى **لا** في علامة التبويب **إقرار الإيرادات** لصفحة **معلمات دفتر الأستاذ العام** (**إقرار الإيرادات \> إعداد \> معلمات دفتر الأستاذ العام**).

[![تعيين خيار ترحيل تصحيحات الفواتير إلى الحسابات المدينة إلى لا.](./media/37_rev-rec-scenarios.png)](./media/37_rev-rec-scenarios.png)

يتم إنشاء أمر المبيعات للعميل US\_SI\_0003. يشتري العميل كمبيوتر محمول (رقم الصنف S0012) وخدمات التثبيت (رقم الصنف S0001) وخطة الدعم للكمبيوتر المحمول (رقم الصنف S0008، "خدمة الهندسة المستدامة"). يتم الاعتراف فورًا بعائدات الكمبيوتر المحمول وخدمات التثبيت. وستؤجل إيرادات خطة الدعم وتُقر على مدى 12 شهرًا، على النحو المحدد في النطاق الزمني المحدد في العقد.

[![بنود أمر المبيعات للكمبيوتر المحمول وخدمات التثبيت وخطة الدعم.](./media/38_rev-rec-scenarios.png)](./media/38_rev-rec-scenarios.png)

تم تأكيد أمر المبيعات. نظرًا لإعداد الأصناف الثلاثة لتوزيع سعر الإيرادات، يتم حساب سعر الإيرادات عند تأكيد أمر المبيعات. يمكنك عرض الإيراد الذي سيتم اقراره في صفحة **توزيع سعر الإيرادات** (في صفحة **أمر المبيعات** ، في جزء الإجراءات، في علامة التبويب **إدارة** ، في مجموعة **إقرار الإيرادات** ، حدد **توزيع سعر الإيرادات**). سيتم ترحيل إيرادات الكمبيوتر المحمول إلى حساب الإيرادات بمبلغ 995.84 دولارًا أمريكيًا. وتُرحل إيرادات خدمات التثبيت أيضًا إلى حساب الإيرادات بمبلغ 314,47 دولارًا أمريكيًا. سيتم ترحيل إيرادات خطة الدعم إلى حساب الإيرادات المؤجلة بمبلغ 188,69 دولارًا أمريكيًا. يجب أن يساوي مجموع أسعار الإيرادات مجموع البنود التي تم إعدادها لالتقاط توزيع سعر الإيرادات (1,499.00 دولارًا أمريكيًا).

[![صفحة توزيع سعر الإيرادات.](./media/39_rev-rec-scenarios.png)](./media/39_rev-rec-scenarios.png)

تتم فوترة العميل لأجهزة الكمبيوتر المحمول وخطة الدعم، ولكن لا يُحاسب على خدمات التثبيت. يوضح الرسم التوضيحي التالي إدخال المحاسبة الذي تم ترحيله للفاتورة.

[![إدخال محاسبي لأمر المبيعات المفوتر.](./media/40_rev-rec-scenarios.png)](./media/40_rev-rec-scenarios.png)

يتم ترحيل الإدخال المحاسبي 1.276.94 دولارًا أمريكيًا إلى الحسابات المدينة. ولكن، نظرًا لأن هذه الفاتورة فاتورة جزئية، فإن الإيراد أو الإيراد المؤجل بالإضافة إلى الضريبة لا يساوي مبلغ الحسابات المدينة. ويُرحل الفرق البالغ - 14.47 دولارًا أمريكيًا إلى حساب المقاصة الجزئي لإيرادات الفاتورة.

يتم أيضًا إنشاء جدول إقرار الإيرادات.

[![صفحة جدول إقرار الإيراد للفاتورة الجزئية.](./media/41_rev-rec-scenarios.png)](./media/41_rev-rec-scenarios.png)

بعد ذلك، يقرر العميل عدم شراء خدمات التثبيت. لذلك، تتم إزالة هذا البند من أمر المبيعات. لاحظ أنه لا يمكن تأكيد أمر المبيعات مرة أخرى، لأنه لا يتبقى سوى البنود المفوترة فقط في أمر المبيعات.

[![أمر المبيعات بعد إزالة بند خدمات التثبيت.](./media/42_rev-rec-scenarios.png)](./media/42_rev-rec-scenarios.png)

وعلى الرغم من أنه لا يمكن تأكيد أمر المبيعات، إلا أنه يمكن إعادة توزيعه. في أوامر المبيعات، حدد **إعادة توزيع السعر ببنود أمر جديد** لفتح صفحة **إعادة توزيع السعر ببنود أمر جديد** . حدد البندين المتبقيين من أمر المبيعات، ثم حدد **تحديث إعادة التوزيع**. يعرض العمود **المبلغ المعاد توزيعه** سعر الإيرادات الجديد لكل بند متبقي في أمر مبيعات.

[![صفحة أسعار الإيرادات الجديدة على سعر إعادة التوزيع مع بنود أوامر جديدة.](./media/43_rev-rec-scenarios.png)](./media/43_rev-rec-scenarios.png)

بعد ذلك، حدد **الإيصال المتوقع** لعرض الإدخالات المحاسبية.

[![الإدخالات المحاسبية في صفحة الإيصال المتوقع.](./media/44_rev-rec-scenarios.png)](./media/44_rev-rec-scenarios.png)

في صفحة **الإيصال المتوقع**، تعكس البنود الخمسة الأخيرة الإدخال المحاسبي الأصلي من الفاتورة التي تم ترحيلها. وتمثل البنود الأربعة الأولي الإدخالات المحاسبية الجديدة التي تم ترحيلها للفاتورة. من المهم أن تدرك أنه لا يتم تقديم فاتورة جديدة للعميل. بعد إعادة التوزيع، لا يزال العميل مدينًا بمبلغ 1,276.94 دولارًا أمريكيًا، وهو المبلغ الذي يتعين ترحيله إلى الحسابات المدينة في الإدخال المحاسبي الجديد. الإيرادات الجديدة أو الإيرادات المؤجلة بالإضافة إلى الضريبة تساوي 1.276.94 دولارًا أمريكيًا. لذلك، لا تحتاج إلى ترحيل إلى حساب مقاصة إيرادات الفاتورة الجزئية.

لإكمال إعادة التوزيع، حدد **معالجة**. يتم إدخال تاريخ الترحيل. بعد اكتمال إعادة التوزيع، تعرض صفحة **توزيع سعر الإيرادات** إعادة توزيع السعر للصنفين المتبقيين.

[![إعادة توزيع السعر للأصناف المتبقية في صفحة توزيع سعر الإيرادات.](./media/45_rev-rec-scenarios.png)](./media/45_rev-rec-scenarios.png)

تم تحديث جدول إقرار الإيرادات أيضًا، استنادًا إلى سعر إعادة توزيع الإيرادات الجديد. من أمر المبيعات، افتح صفحة **جدولة إقرار الإيرادات**. سابقًا، كان يوجد 13 بند للصنف S0008 (تم تعيين جدول لمدة 12 شهرًا لهذا الصنف). يوجد الآن 39 بندًا: 13 بند جدول أصلي و13 بند جدول إلغاء و13 بند يستند على سعر الإيرادات الجديد.

[![صفحة جدول إقرار الإيرادات المحدثة بـ 39 بندًا للصنف S0008.](./media/46_rev-rec-scenarios.png)](./media/46_rev-rec-scenarios.png)

عند تحديد **الإيصال**، يعرض دفتر يومية الفواتير الإدخال المحاسبي الأصلي. لعرض الإدخال العكسي والإدخال المحاسبي الجديد من أمر المبيعات ، حدد **تعديلات الإيرادات** في جزء الإجراءات ، ثم قم بتحديد **الإيصال**.

بعد ذلك، افتح صفحة **كل العملاء** (**الحسابات المدينة \> العملاء \> كل العملاء**)، حدد العميل **US\_SI\_0003**، ثم حدد **الحركات**. تظهر صفحة **حركات العميل** الفاتورة الأصلية (000008) مع الإدخال المحاسبي الأصلي فقط. نظرًا لأنه يتم تعيين خيار **ترحيل تصحيحات الفاتورة إلى الحسابات المدينة** إلى **لا** في صفحة **محددات دفتر الأستاذ العام** ، يتم تحديث دفتر الأستاذ العام فقط. بالتالي، لا يتم عرض الإدخالات المحاسبية المعكوسة أو التي تم إلغائها. لاحظ أنه يتم عرض حركات تعديل الإيرادات التي تم إنشاؤها في [السيناريو 3](rev-rec-reallocation-scenario-3.md).

[![الإدخال المحاسبي الأصلي في صفحة حركات العميل.](./media/47_rev-rec-scenarios.png)](./media/47_rev-rec-scenarios.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
