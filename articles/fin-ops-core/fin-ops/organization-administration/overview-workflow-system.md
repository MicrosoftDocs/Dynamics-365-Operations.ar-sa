---
title: نظرة عامة على نظام سير العمل
description: يصف هذا الموضوع نظام سير العمل.
author: ChrisGarty
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 660e01618eea66bc611dd51818694d36993ba9ea
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/19/2020
ms.locfileid: "4796986"
---
# <a name="workflow-system-overview"></a>نظرة عامة على نظام سير العمل

[!include [banner](../includes/banner.md)]

يصف هذا الموضوع نظام سير العمل.

## <a name="what-is-workflow"></a>ما المقصود بسير العمل؟

المصطلح *سير* يمكن تعريفه بطريقتين: كنظام وكعملية تجارية.

### <a name="workflow-is-a-system"></a>سير العمل كنظام

يُمثل سير العمل نظامًا يتم تشغيله على Application Object Server (AOS).  يوفر نظام سير العمل الوظائف التي يمكن استخدامها في إنشاء سير عمل فردي، أو عمليات تجارية.

### <a name="workflow-is-a-business-process"></a>سير العمل كعملية تجارية

يعد سير العمل بمثابة عملية تجارية. فهو يحدد كيفية تدفق المستند، أو انتقاله عبر النظام عن طريق عرض الفرد المنوط بإكمال المهمة، أو اتخاذ القرار أو الموافقة على المستند. على سبيل المثال، يُظهر الرسم التالي سير عمل لتقارير المصروفات.

![سير عمل مع عناصر تم تعيينها للمستخدمين](./media/workflow_user.gif)

لاستيعاب سير العمل هذا على نحو أفضل، لنفترض أن سامي يقدم تقرير مصروفات بمبلغ 7000 دولار أمريكي. في هذا السيناريو، يجب أن يقوم فريد بمراجعة عمليات الاستلام التي يقوم سامي بتوجيهها له. بعد ذلك يجب أن يقوم تميم وسلمان باعتماد تقرير المصروفات. لنفترض الآن أن سامي يقدم تقرير مصروفات بمبلغ 11.000 دولار أمريكي. ففي هذا السيناريو، يجب أن يقوم فريد بمراجعة عمليات الاستلام ولا بد من اعتماد التقرير من قبل تميم وسلمان وسليم.

## <a name="benefits-of-using-the-workflow-system"></a> فوائد استخدام نظام سير العمل

ويترتب على استخدام نظام سير العمل في المؤسسة العديد من الفوائد:

- **عمليات متسقة** — يمكنك تحديدمستندات بعينها تمت معالجتها، مثل طلبات الشراء وتقارير المصروفات. ومن خلال استخدام نظام سير العمل، فأنت تؤكد على أنه تتم معالجة المستندات واعتمادها بأسلوب متسق وفعال.
- **وضوح العمليات** - يمكنك تتبع حالة وتاريخ ومعايير أداء مثيلات سير العمل. ويساعدك هذا الأمر على تحديد ما إذا كانت هناك ضرورة لإجراء تغييرات على سير العمل لتحسين كفاءته أم لا.
- **قائمة العمل المركزية** — يمكن للمستخدمين عرض قائمة عمل مركزية تعرض مهام سير العمل والموافقات المعينة لهم.


## <a name="workflow-content"></a>محتوى سير العمل

+ [بنية نظام سير العمل](workflow-system-architecture.md)
+ [عناصر سير العمل](workflow-elements.md)
+ [الإجراءات في عمليات الموافقة على سير العمل](workflow-actions.md)
+ [نظرة عامة حول إنشاء عمليات سير العمل](create-workflow.md)
+ [تكوين خصائص سير العمل](configure-workflow-properties.md)
+ [تكوين المهام اليدوية في سير عمل](configure-manual-task-workflow.md)
+ [تكوين المهام المؤتمتة في سير عمل](configure-automated-task-workflow.md)
+ [تكوين عمليات الاعتماد في سير عمل](configure-approval-process-workflow.md)
+ [تكوين خطوات الاعتماد في سير عمل](configure-approval-step-workflow.md)
+ [تكوين القرارات اليدوية في سير عمل](configure-manual-decision-workflow.md)
+ [تكوين القرارات الشرطية في سير عمل‬](configure-conditional-decision-workflow.md)
+ [تكوين أنشطة موازية في سير عمل](configure-parallel-activity-workflow.md)
+ [تكوين فروع موازٍية في سير عمل](configure-parallel-branch-workflow.md)
+ [تكوين عمليات سير عمل لعنصر بند](configure-line-item-workflow.md)
+ [الأسئلة المتداولة حول سير العمل](workflow-FAQ.md)
