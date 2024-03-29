---
title: الإجراءات في عمليات الموافقة على سير العمل
description: توضح هذه المقالة الإجراءات التي يمكن أن يتخذها كل مشارك في عملية موافقة على سير عمل.
author: ChrisGarty
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 56411
ms.assetid: 65fb711c-6474-42d1-81ed-ca657c29bf1f
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2e546dc57692e31d4501984dafa21fbae23a48fe
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070923"
---
# <a name="actions-in-workflow-approval-processes"></a>الإجراءات في عمليات الموافقة على سير العمل

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

توضح هذه المقالة الإجراءات التي يمكن أن يتخذها كل مشارك في عملية موافقة على سير عمل.

يمكن أن ينطوي سير العمل على عدة مجموعات من الأشخاص: المنشئ، والمعينين للمهام، وصانعي القرار، والمعتمدين. على سبيل المثال، في سير عمل تقرير المصروفات التالي، يعد سامي هو المنشئ، وأعضاء قائمة الانتظار هم المعينين للمهام، وسعيد هو صانع القرار، وسمر، وفيصل هم المعتمدون.

[![Workflow\_WithManualDecision.](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif)

تشرح الأقسام التالية إجراءات سير العمل التي تستطيع كل مجموعة تنفيذها.

## <a name="actions-that-an-originator-can-perform"></a>الإجراءات التي يمكن أن يتخذها المنشئ

يبدأ المنشئ في إجراء مثيل سير عمل عن طريق إرسال مستند للمعالجة. على سبيل المثال، يجب على سامي النقر فوق الزر **إرسال** في صفحة **تقرير المصروفات** لإرسال تقرير المصروفات الخاص به.

## <a name="actions-that-a-task-assignee-can-perform"></a>الإجراءات التي يمكن أن يتخذها معين لهمة

يمكن تعيين مهمة إلى عدة أشخاص أو إلى قائمة انتظار عنصر عمل تتم مراقبته من قِبل عدة أشخاص. ومع ذلك، يمكن لشخص واحد فقط إكمال مهمة. على سبيل المثال، قام سامي بإرسال تقرير مصروفات وتوجيه ايصالاته إلى إدارة تقارير المصروفات في المؤسسة الخاصة به لمراجعتها.

ويراقب أعضاء إدارة تقارير مصروفات شركة المنتجات التجارية قائمة الانتظار. وقبلت منال، وهي عضو في تلك الإدارة، مهمة مراجعة إيصالات وتقرير المصروفات الخاصة بسامي. ويمكنها الآن إجراء واحد من الإجراءات التالية: الإكمال أو الرفض أو التفويض أو طلب التغيير أو إعادة التعيين أو الإصدار.

> [!NOTE]
> تختلف الإجراءات المتاحة بحسب الطريقة التي قام بها مطور البرنامج بتصميم المهمة.

### <a name="complete"></a>الإكمال

عندما يقوم مستخدم بإكمال مهمة، يتم تعيين المستند الذي تم إرساله للمعالجة إلى المستخدم التالي في سير العمل، عندما يكون هناك مستخدم تالي. عند عدم الحاجة إلى إجراء مزيد من المعالجة، تنتهي عملية سير العمل.

على سبيل المثال، قبلت منال، وهي عضو في إدارة تقارير مصروفات شركة المنتجات التجارية، مهمة مراجعة إيصالات وتقرير المصروفات الخاصة بسامي. وبعد أن تُكمل منال مراجعتها، يتم تعيين المستند إلى يحيى.

### <a name="reject"></a>رفض

وعندما يقوم مستخدم برفض مستند، تنتهي عملية سير العمل.

على سبيل المثال، قبلت منال، وهي عضو في إدارة تقارير مصروفات شركة المنتجات التجارية، مهمة مراجعة إيصالات وتقرير المصروفات الخاصة بسامي. وإذا رفضت منال تقرير المصروفات، تنتهي عملية سير العمل.

ويمكن لسامي فيما بعد إعادة إرسال تقرير المصروفات. ويمكنه إجراء التغييرات أولاً، أو أنه يمكن إعادة إرسال النسخة الأصلية. فإذا أعاد سامي إرسال تقرير المصروفات، تبدأ عملية سير العمل في مهمة المراجعة اليدوية.

### <a name="delegate"></a>التفويض

عندما يقوم مستخدم بتفويض مهمة، يتم تعيين المهمة إلى مستخدم آخر.

على سبيل المثال، قبلت منال، وهي عضو في إدارة تقارير مصروفات شركة المنتجات التجارية، مهمة مراجعة إيصالات وتقرير المصروفات الخاصة بسامي. وتفوض منال هذه المهمة إلى تامر، وهو مساعد لها.

ويتصرف تامر بالنيابة عن منال فيما بعد. ولذلك، عندما يُكمل تامر مراجعته، فإنه يتم تعيين تقرير المصروفات إلى يحيى، كما لو أن منال أكملت المهمة.

### <a name="request-change"></a>تغيير الطلب

عندما يطالب مستخدم بإجراء تغيير في مستند تم إرساله، يتم إرسال المستند إلى المنشئ.

على سبيل المثال، قبلت منال، وهي عضو في إدارة تقارير مصروفات شركة المنتجات التجارية، مهمة مراجعة إيصالات وتقرير المصروفات الخاصة بسامي. وتلاحظ منال بعض الأخطاء في تقرير المصروفات وتطلب إجراء تغيير. ويتم إرسال تقرير المصروفات إلى سامي مرة أخرى.

ويمكن لسامي إعادة إرسال تقرير المصروفات. ويمكنه إجراء التغييرات المطلوبة أولاً، أو أنه يمكن إعادة إرسال النسخة الأصلية. وإذا أعاد سامي إرسال تقرير المصروفات، فيجب على عضو في قائمة انتظار عناصر العمل مراجعة تقرير المصروفات والإيصالات مرة أخرى.

### <a name="reassign"></a>إعادة تعيين

يمكن لأعضاء قائمة انتظار عناصر العمل إعادة تعيين المستندات الموجودة في قائمة الانتظار تلك إلى قائمة انتظار أخرى.

على سبيل المثال، تراقب منال، وهي عضو في إدارة تقارير مصروفات شركة المنتجات التجارية، قائمة الانتظار. وللمساعدة في موازنة حمل العمل، تقوم بإعادة تعيين تقرير المصروفات والإيصالات المشمولة فيه، إلى قائمة انتظار أخرى.

### <a name="release"></a>الإصدار

وفي بعض الأحيان، قد يقبل عضو قائمة انتظار عناصر العمل مهمة، ولكنه يقرر أو تقرر أنه لا يمكنه إكمال المهمة. وفي هذه الحالة، الشخص الذي قام بقبول المهمة يمكنه إصدار المستند مرة أخرى إلى قائمة انتظار عناصر العمل.

على سبيل المثال، قبلت منال، وهي عضو في إدارة تقارير مصروفات شركة المنتجات التجارية، مهمة مراجعة إيصالات وتقرير المصروفات الخاصة بسامي. إذا قررت منال أنه لا يمكنها إكمال المهمة، فيمكنها تحرير المستند. ويتم إرجاع تقرير المصروفات إلى قائمة الانتظار، بحيث يستطيع أعضاء آخرون في إدارة تقارير المصروفات شركة المنتجات التجارية إنجاز المهمة.

## <a name="actions-that-a-decision-maker-can-perform"></a>الإجراءات التي يمكن أن يتخذها صانع قرار

بشكل عام، يتم تعيين مستند إلى صانع قرار، لأن هناك سؤال يجب على متخذ القرار الإجابة عنه. والإجابة على السؤال عادةً ما تكون **نعم** أو **لا**، أو **صحيح** أو **خطأ**. إذا لم يحدد متخذ القرار واحد من هذه الخيارات، فيمكنه أو يمكنها تفويض القرار.

### <a name="choice-1-or-choice-2"></a>\[الخيار 1\] أو \[الخيار 2\]

يجب على صانع قرار الإجابة عن سؤال مرتبط بالمستند. والإجابة على السؤال عادةً ما تكون **نعم** أو **لا**، أو **صحيح** أو **خطأ**. وتحدد الإجابة التي يحددها متخذ القرار فرع سير العمل الذي يتم استخدامه لمعالجة المستند.

على سبيل المثال، يتم تعيين تقرير مصروفات سامي إلى يحيى. ويجب أن يقرر يحيى ما إذا كانت المعلومات الموجودة في المستند تتطلب الاتصال بمدير سامي. وإذا قرر يحيى ضرورة الاتصال، فإنه يتم تعيين تقرير المصروفات إلى إسراء، التي يجب عليها الاتصال بمدير سامي لاحقًا. وإذا قرر يحيى أن الاتصال غير ضروري، فإنه يتم تعيين تقرير المصروفات إلى سعيد للاعتماد.

### <a name="delegate"></a>التفويض

عندما يفوض متخذ قرار قرارًا، يتم تعيين المستند إلى مستخدم آخر يجب عليه اتخاذ القرار.

على سبيل المثال، يتم تعيين تقرير مصروفات سامي إلى يحيى. ويفوض يحيى قرارًا لمريم، وهي مساعدة له.

وتتصرف مريم بالنيابة عن يحيى فيما بعد. وإذا قررت مريم أنه من غير الضروري الاتصال بمدير سامي، فإنه يتم تعيين تقرير المصروفات إلى إسراء، التي يجب عليها الاتصال بمدير سامي لاحقًا. وإذا قررت مريم أن الاتصال غير ضروري، فإنه يتم تعيين تقرير المصروفات إلى سعيد للاعتماد.

## <a name="actions-that-an-approver-can-perform"></a>الإجراءات التي يمكن أن يتخذها معتمد

عند تعيين مستند إلى معتمد، يمكن للمعتمد اتخاذ أحد الإجراءات التالية: اععتماد أو رفض أو تفويض أو طلب تغيير.

### <a name="approve"></a>اعتماد

وعندما يقوم معتمد باعتماد مستند، يتم تعيين المستند إلى المستخدم التالي في سير العمل، إذا كان مستخدم تالي. عند عدم الحاجة إلى إجراء مزيد من المعالجة، تنتهي عملية سير العمل.

على سبيل المال، قام سامي بتقديم ‏‏تقرير مصروفات بمبلغ 6,000 دولار أمريكي، وتم تعيين هذا المستند إلى سعيد. وعندما يعتمد سعيد المستند، يتم تعيينه إلى سمر للاعتماد. وعندما تقوم سمر باعتماد تقرير المصروفات، تنتهي عملية سير العمل.

### <a name="reject"></a>رفض

عندما يقوم معتمد برفض مستند، تنتهي معالجة سير العمل.

على سبيل المال، قام سامي بتقديم ‏‏تقرير مصروفات بمبلغ 12,000 دولار أمريكي، وتم تعيين هذا المستند إلى سمر. إذا رفضت سمر تقرير المصروفات، تنتهي عملية سير العمل.

ويمكن لسامي إعادة إرسال تقرير المصروفات. ويمكنه إجراء التغييرات أولاً، أو أنه يمكن إعادة إرسال النسخة الأصلية لتقرير المصروفات. فإذا أعاد سامي إرسال تقرير المصروفات، تبدأ عملية سير العمل من عملية الاعتماد.

### <a name="delegate"></a>التفويض

عندما يقوم معتمد بتفويض مستند، يتم تعيين المستند إلى مستخدم آخر للاعتماد.

على سبيل المال، قام سامي بتقديم ‏‏تقرير مصروفات بمبلغ 12,000 دولار أمريكي، وتم تعيين هذا المستند إلى سعيد. يقوم سعيد بتفويض تقرير المصروفات إلى فيصل.

عندئذٍ يتصرف فيصل نيابةً عن سعيد. ولذلك، عندما يقوم فيصل باعتماد المستند، فإنه يتم تعيين المستند إلى سمر للاعتماد، تمامًا كما لو أن سعيد قد اعتمده. وبعد أن تعتمد سمر المستند، يتم إرساله إلى فيصل للاعتماد.

### <a name="request-change"></a>تغيير الطلب

عندما يطلب معتمد إجراء تغيير في مستند، تتم إعادة إرسال المستند إلى المنشئ.

على سبيل المال، قام سامي بتقديم ‏‏تقرير مصروفات بمبلغ 12,000 دولار أمريكي، وتم تعيين هذا المستند إلى سمر. وإذا طلبت سمر إجراء تغيير، فإنه تتم إعادة إرسال تقرير المصروفات إلى سامي.

ويمكن لسامي إعادة إرسال تقرير المصروفات. ويمكنه إجراء التغييرات المطلوبة أولاً، أو أنه يمكن إعادة إرسال النسخة الأصلية لتقرير المصروفات. وإذا أعاد سامي إرسال تقرير المصروفات، فسيتم إرساله إلى سعيد للاعتماد نظرًا لأن سعيد هو المعتمد الأول في عملية الاعتماد.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]