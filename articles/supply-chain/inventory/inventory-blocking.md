---
title: حظر المخزون
description: توفر هذه المقالة نظرة عامة حول حظر المخزون، الذي يشكل جزءًا من عملية فحص الجودة في Supply Chain Management. يمكنك استخدام حظر المخزون لمنع معالجة الأصناف أو استهلاكها.
author: yufeihuang
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventQualityOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2094
ms.assetid: 1968e32f-eff9-4c17-8f7f-a870f0c38fbc
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 83b5417dc24af85f09e6713f2b12fdc358f61d54
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334674"
---
# <a name="inventory-blocking"></a>حظر المخزون

[!include [banner](../includes/banner.md)]

توفر هذه المقالة نظرة عامة حول حظر المخزون، الذي يشكل جزءًا من عملية فحص الجودة في Supply Chain Management. يمكنك استخدام حظر المخزون لمنع معالجة الأصناف أو استهلاكها.

يمكنك حظر أصناف المخزون بالطرق التالية:

- يدويًا
- بإنشاء أمر جودة.
- باستخدام عملية إنشاء أمر الجودة
- من خلال استخدام حظر حالة المخزون

## <a name="blocking-items-manually"></a>حظر الأصناف يدويًا

يمكنك حظر كمية صنف ما بإنشاء حركة في صفحة **حظر المخزون**. يمكن حظر فقط الأصناف المتاحة كمخزون فعلي يدويًا. وبالنسبة للكميات المحظورة يدوياً، يجب عليك تحديد ما إذا كانت أنشطة التخطيط تتضمن إيصالات الاستلام المتوقعة ككمية فعلية متوقعة. عمليات الاستلام المتوقعة هي الأصناف المحظورة المتوقع أن تكون متوفرة كمخزون فعلى بعد الفحص. يمكنك الاحتفاظ بالتاريخ المتوقع. وبشكل افتراضي، يتم تحديد خيار **إيصالات الاستلام المتوقعة** للأصناف التي يتم حظرها من خلال أمر جودة. يمكنك إلغاء حظر يدوي في كمية عن طريق حذف الحركة الموجودة في صفحة **حظر المخزون**.

## <a name="blocking-items-by-creating-a-quality-order"></a>حظر الأصناف بإنشاء أمر جودة

يمكنك تحديد العناصر التي يجب فحصها قبل إنشاء أمر جودة في صفحة **أوامر الجودة**. عند إنشاء أمر جودة، يتم حظر الكمية التي تحددها لصنف. وتتحكم خطة أخذ العينات المرتبطة بأمر جودة فقط في كمية الأصناف التي يجب فحصها، وليس الكمية التي يتم حظرها. والكمية التي يتم إدخالها في أمر الجودة هي الكمية التي يتم حظرها، بغض النظر عن الكمية التي تحدد خطة أخذ العينات وجوب إرسالها للفحص.

> [!NOTE]
> لا يتم دعم استخدام كل من تاريخ انتهاء صلاحيه المجموعة وميزات حالة مخزون الحظر بواسطة التخطيط الرئيسي. وقد ينتج عن ذلك استبعاد مزدوج للمخزون الفعلي ، والذي يمكن أن يحدث اثناء التخطيط الرئيسي. ونوصي بالاعتماد علي رموز إرجاع الدفعة ، بدلا من حالة المخزون ، لحظر المجموعات منتهية الصلاحية.

## <a name="blocking-items-by-using-a-process-that-generates-a-quality-order"></a>حظر الأصناف باستخدام عملية إنشاء أمر الجودة

إذا كانت عملية جودة تحدد صنفًا يجب فحصه، فإنه يتم حظر كمية الصنف تلقائيًا. ولذلك، عندما يتم إنشاء أمر جودة تلقائيًا، تتحكم خطة أخذ عينات الصنف المقترنة بأمر الجودة في كلٍّ من كمية الأصناف المحظورة والكمية التي يجب فحصها. إذا تم تحديد خيار **الحظر الكامل** في صفحة **أخذ عينات الأصناف**، فإنه يتم حظر الكمية الكاملة لبند أمر شراء مثلاً أثناء الفحص، بغض النظر عن كمية أخذ عينات الصنف.

### <a name="example"></a>مثال

في المثال التالي، يتم إنشاء أمر جودة عند ترحيل إيصال تعبئة خاص بأمر الشراء. في صفحة **عمليات اقتران الجودة‬**، حددت أنت ترحيل إيصال التعبئة الخاص بأمر الشراء بأنها العملية التي تقوم بتنشيط أمر الجودة.

|إعداد |إجراء المستخدم |النتيجة |
|----|---|---|
| تحدد اقتران الجودة أن أمر الجودة يجب إنشاؤه عند ترحيل إيصال تعبئة أمر الشراء. ويحدد إعداد أخذ عينات الصنف لأمر الجودة أنه يمكن فحص 10 بالمائة من الكمية الموجودة في بند أمر الشراء الذي يجب فحصه. علاوةً على ذلك، ونظرًا لتحديد **الحظر الكامل** في إعداد أخذ عينات الصنف، يجب حظر الكمية الكاملة لسطر أمر الشراء أثناء الفحص، بغض النظر عن الكمية التي يتم إرسالها للفحص. | تم ترحيل إيصال التعبئة. | تم إنشاء أمر جودة. تم إرسال عشرة بالمائة من كمية أمر الشراء للصنف للفحص. تم حظر الكمية الكاملة من سطر أمر الشراء. |

## <a name="blocking-items-by-using-inventory-status-blocking"></a>حظر الأصناف من خلال استخدام حظر حالة المخزون

يمكنك تحديد حالات المخزون التي هي حالات حظر باستخدام معلمة **حظر المخزون** في صفحة **حالات المخزون**. لا يمكنك استخدام حالات المخزون كحالات حظر لأوامر الإنتاج، أو أوامر المبيعات، أو أوامر التحويل، أو الحركات الصادرة، أو عمليات دمج المشاريع. وبالنسبة للعمل الصادر، استخدم أصنافًا بحالة مخزون متوفر. إذا كانت الأصناف حالة **معطلة** والتخطيط الرئيسي يعمل على هذه الأصناف، تعتبر الأصناف مفقودة، ويتم تزويد المخزون تلقائياً.

## <a name="take-care-when-blocking-items-that-use-both-inventory-status-blocking-and-quality-order-blocking"></a>الاهتمام عند حظر الأصناف التي تستخدم كلٍ من حظر حالة المخزون وحظر أمر الجودة

يمكنك إنشاء أمر جودة مرتبط بالمخزون يحتوي على حالة المخزون التي تم تمكين معلمة **حظر المخزون** الخاصة به. في هذه الحالة، سيقوم أمر الجودة بإنشاء سجل حظر مخزون إضافي بالإضافة إلى تلك التي تم إنشاؤها بواسطة حالة المخزون. ونظرًا لأن حظر مخزون أمر الجودة، فإنه سيتم تمكين المعلمة **عمليات الاستلام المتوقعة**، وهذا يعمل على إنشاء الحركة *المخزون المطلوب* الإضافية التي يتم حظرها أيضًا بواسطة حالة المخزون الخاصة بها. يمكن أن تؤدي هذه المجموعة إلى حدوث صعوبات في فهم معني حركات المخزن التي تم إنشاؤها، نظرًا لأنها ستظهر بالرغم من أن إجمالي الكمية المحظورة يكون زائدًا عن إجمالي الكمية الفعلية. لنقم بفحص الحركات الموجودة في أحد أمثلة الاستلام المكون من 10 قطع من الصنف A0001 بأمر الجودة الذي تم إنشاؤه لعينة القطعة 1. ويعتمد السلوك أيضًا على ما إذا كان يتم تمكين الخيار **حجز الأصناف المطلوبة** في الصفحة **معلمات إدارة المخزون والمستودع**.

>[!NOTE]
>إذا كنت تستخدم حظر حالة المخزون وأوامر الجودة معًا، نُوصي بشدة بتمكين الخيار **الأصناف المطلوبة للحجز**.

### <a name="example-with-reserve-ordered-items-enabled"></a>مثال على تمكين "حجز الأصناف المطلوبة"

عند تمكين **حجز الأصناف المطلوبة**، ستكون كافة حركات حظر المخزون بالحالة إما *الفعلية المحجوزة* أو *المطلوبة المحجوزة*.

| مرجع حركة المخزون | استلام | إصدار | الكمية | الموقع | المستودع | حالة المخزون |  الموق | لوحة الترخيص | الملاحظات |
|---|---|---|---|---|---|---|---|---|---|
| أمر شراء | المشترى | | 10 قطع | 2 | 24 | وقف التعامل | RECV | receiptLp1 | | 
| حظر المخزون | | الفعلي المحجوز | -9 قطع | 2 | 24 | وقف التعامل | | | الحركة التي تم إنشاؤها بواسطة حظر حالة المخزون |
| حظر المخزون | | الفعلي المحجوز | -قطعة واحدة | 2 | 24 | وقف التعامل | RECV | receiptLp1 | الحركة التي تم إنشاؤها بواسطة حظر نماذج أمر الجودة |
| حظر المخزون | مطلوبة | | قطعة واحدة | 2 | 24 | وقف التعامل | RECV | receiptLp1 | الإيصالات المتوقعة من حظر عينات أمر الجودة |
| حظر المخزون | | المطلوب المحجوز | قطعة واحدة | 2 | 24 | وقف التعامل | | | الحركة التي تم إنشاؤها بواسطة حظر حالة المخزون

### <a name="example-with-reserve-ordered-items-disabled"></a>مثال على تعطيل "حجز الأصناف المطلوبة"

عند تعطيل **حجز الأصناف المطلوبة**، يتعذر حجز إيصالات الاستلام المتوقعة لأنها بالحالة *مطلوبة*، وبالتالي سيتم ترك بعض الحظر في الحالة *تحت الطلب*.

| مرجع حركة المخزون | استلام | إصدار | الكمية | الموقع | المستودع | حالة المخزون |  الموق | لوحة الترخيص | الملاحظات |
|---|---|---|---|---|---|---|---|---|---|
| أمر شراء | المشترى | | 10 قطع | 2 | 24 | وقف التعامل | RECV | receiptLp1 | |
| حظر المخزون | | الفعلي المحجوز | -9 قطع | 2 | 24 | وقف التعامل | | | الحركة التي تم إنشاؤها بواسطة حظر حالة المخزون |
| حظر المخزون | | الفعلي المحجوز | -قطعة واحدة | 2 | 24 | وقف التعامل | RECV | receiptLp1 | الحركة التي تم إنشاؤها بواسطة حظر نماذج أمر الجودة |
| حظر المخزون | مطلوبة | | قطعة واحدة | 2 | 24 | وقف التعامل | RECV | receiptLp1 | الإيصالات المتوقعة من حظر عينات أمر الجودة |
| حظر المخزون | | تحت الطلب | قطعة واحدة | 2 | 24 | وقف التعامل | RECV | receiptLp1 | الحركة التي تم إنشاؤها بواسطة حظر حالة المخزون

لاحظ الفرق في حالة الحركة والأبعاد بين الحالتين. لهذا السبب، نُوصي بتمكين الخيار **حجز الأصناف المطلوبة**.

## <a name="disable-expected-receipts-from-quality-orders-that-sample-blocked-inventory"></a>تعطيل عمليات الاستلام المتوقعة من أوامر الجودة التي تقوم بأخذ عينة من المخزون المحظور

لتبسيط حركات المخزون في حالة أوامر الجودة التي قامت عينة المخزون بحظرها نتيجة لحالة المخزون، يوفر النظام ميزة تعطل عمليات الاستلام المتوقعة من أوامر الجودة هذه. نظرًا لأنه تم حظر الاستلام المتوقع فورًا عن طريق حظر حالة المخزون، فلا يوجد تخفيض في المخزون الفعلي بسبب هذا التغيير.

لاستخدام هذه الميزة ، يجب تشغيلها لنظامك. اعتبارًا من الإصدار 10.0.29 من Supply Chain Management، يتم تشغيل هذه الميزة افتراضيًا. بإمكان المسؤولين تشغيل هذه الوظيفة أو إيقاف تشغيلها عن طريق البحث عن الميزة *تعطيل عمليات الاستلام المتوقعة من أوامر الجودة التي تقوم بأخذ عينة من المخزون المحظور‬* في مساحة عمل [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="additional-resources"></a>الموارد الإضافية

[إنشاء وصيانة حظر المخزون](tasks/create-maintain-inventory-blocking.md)

[عمليات إدارة الجودة](quality-management-processes.md)

[فحص جودة البضائع](tasks/inspect-quality-goods.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]