---
title: إقفال نهاية السنة يفتقد الأرصدة الافتتاحية
description: يشرح هذا المقال سبب فقد الأرصدة الافتتاحية عند إقفال سنة، وكيفية إعادة تكوين هذه الأرصدة إذا كانت مفقودة.
author: kweekley
ms.date: 05/12/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9b64118fc3ff368e21ea8935c1e706f2161c620f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894837"
---
# <a name="year-end-close-missing-opening-balances"></a>إقفال نهاية السنة يفتقد الأرصدة الافتتاحية

[!include [banner](../includes/banner.md)]

يشرح هذا المقال سبب فقد الأرصدة الافتتاحية عند إقفال سنة، وكيفية إعادة تكوين هذه الأرصدة إذا كانت مفقودة.

### <a name="symptom"></a>العَرَضْ

لماذا لا توجد أي أرصدة افتتاحية بعد تشغيل إقفال نهاية السنة لدفتر الأستاذ العام؟ 

### <a name="resolution"></a>الحل

فيما يلي بعض الأشياء التي يجب التحقق منها إذا كنت قد أقفلت سنة في دفتر الأستاذ العام، ثم قمت بإنشاء ميزان مراجعة لا يعرض الأرصدة الافتتاحية للسنة المالية التالية.

في حالة تعيين حقل **تراجع عن الإقفال السابق‬‏‫** إلى **نعم**، يتم إلغاء إقفال نهاية السنة السابقة لنفس السنة المالية. عند تشغيل عملية لإلغاء إقفال نهاية السنة، سيتم حذف جميع إدخالات كل من الأرصدة الختامية والأرصدة الافتتاحية، كما لو لم يتم إقفال السنة مطلقًا. يتم حذف الإيصالات أيضًا. لن يتم تشغيل عملية إقفال نهاية السنة تلقائيًا مرة أخرى. يجب عليك بدء العملية مرة أخرى، ولكن هذه المرة بتحديث **تراجع عن الإقفال السابق‬‏‫** إلى **لا**.

تمت تغطية هذا السيناريو في مقال الأسئلة الشائعة حول إقفال نهاية السنة. لمزيد من المعلومات، راجع [الأسئلة الشائعة حول أنشطة نهاية السنة](faq-year-end-activities.md).

### <a name="symptom"></a>العَرَضْ

قمتُ بتشغيل إقفال نهاية السنة عن طريق تعيين خيار **تراجع عن الإقفال السابق** إلى **لا**، ومازلت لا أمتلك أرصدة افتتاحية للسنة المالية.

### <a name="resolution"></a>الحل

تحقق أولاً من حالة وظيفة الدُفعة. يتضمن إقفال السنة عددًا من المهام المنفصلة، ولكن الخطوة الأكثر أهميةً هي مهمة الدُفعة مع وصف المهمة **الخطوة 5.0.0**. يتم ترحيل الحركات الافتتاحية، واختياريًا الحركات الختامية، إلى دفتر الأستاذ العام أثناء هذه الخطوة. 

[![قائمة محفوظات الدُفعات.](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)

إذا انتهت هذه الخطوة بنجاح ولكنك لا ترى الأرصدة الافتتاحية في صفحة **الاستعلام عن ميزان المراجعة** (**دفتر الأستاذ العام > الاستعلامات والتقارير > ميزات المراجعة**)، فراجع نتائج وظيفة دُفعة إقفال نهاية السنة لمعرفة ما إذا كانت خطوة إعادة إنشاء الأرصدة قد اكتملت بنجاح.

[![نتائج وظيفة دُفعة إقفال نهاية السنة.](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)

إذا فشلت هذه الخطوة لأي سبب من الأسباب، من المحتمل أن يكون قد تم ترحيل الحركات الافتتاحية (والختامية اختياريًا) بنجاح. يمكنك التحقق من ترحيل حركات دفتر الأستاذ العام بنجاح باستخدام صفحة **الاستعلام عن حركات الإيصالات** عن طريق تحديد رقم الإيصال والتاريخ الموفرين في مربع حوار إقفال نهاية السنة للسنة التي أقفلتها، (**دفتر الأستاذ العام > الاستعلامات والتقارير > حركات الإيصالات**).

[![الاستعلام عن حركات الإيصالات.](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)

إذا كانت الإيصالات الافتتاحية (والختامية اختياريًا) موجودة، فلن تحتاج إلى إجراء إقفال نهاية السنة مرة أخرى. بدلاً من ذلك، راجع القسم التالي للحصول على معلومات حول كيفية المُضي قدمًا.

### <a name="symptom"></a>العَرَضْ

فشلت خطوة "إعادة إنشاء الأرصدة" في إقفال نهاية السنة، هل أحتاج إلى إعادة إجراء عملية إقفال نهاية السنة بالكامل؟

### <a name="resolution"></a>الحل

تعمل خطوة إعادة إنشاء الأرصدة على تحديث أرصدة دفتر الأستاذ العام التي يتم استخدامها عند إنشاء استعلام عن ميزان المراجعة.  إنها الخطوة الأخيرة في عملية إقفال نهاية السنة.  إذا كانت هذه الخطوة هي الخطوة الوحيدة التي فشلت، فقد تم ترحيل حركات دفتر الأستاذ العام بنجاح.  لا تحتاج إلى إجراء إقفال نهاية السنة مرة أخرى. يمكنك إجراء العملية لإعادة تكوين الأرصدة يدويًا باستخدام صفحة **مجموعات الأبعاد المالية** (**دفتر الأستاذ العام > مخطط الحسابات > الأبعاد > مجموعات الأبعاد المالية**).

[![زر إعادة إنشاء الأرصدة في صفحة مجموعات الأبعاد المالية.](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)

إذا كانت هذه الخطوة تستغرق وقتًا طويلاً للمعالجة، فإننا نوصي بمراجعة أفضل الممارسات لمجموعات الأبعاد المالية على النحو الموضح في [أفضل الممارسات لتحديث مجموعات الأبعاد المالية](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets). 

