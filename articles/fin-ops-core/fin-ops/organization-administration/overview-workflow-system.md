---
title: نظرة عامة على نظام سير العمل
description: توضح المقالة نظام سير العمل.
author: ChrisGarty
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom:
- "56381"
- intro-internal
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 13dd4335a8b939a44ea7176a90f660999c32a83a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863177"
---
# <a name="workflow-system-overview"></a>نظرة عامة على نظام سير العمل

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

توضح المقالة نظام سير العمل.

## <a name="what-is-workflow"></a>ما المقصود بسير العمل؟

المصطلح *سير* يمكن تعريفه بطريقتين: كنظام وكعملية تجارية.

### <a name="workflow-is-a-system"></a>سير العمل كنظام

يُمثل سير العمل نظامًا يتم تشغيله على Application Object Server (AOS).  يوفر نظام سير العمل الوظائف التي يمكن استخدامها في إنشاء سير عمل فردي، أو عمليات تجارية.

### <a name="workflow-is-a-business-process"></a>سير العمل كعملية تجارية

يعد سير العمل بمثابة عملية تجارية. فهو يحدد كيفية تدفق المستند، أو انتقاله عبر النظام عن طريق عرض الفرد المنوط بإكمال المهمة، أو اتخاذ القرار أو الموافقة على المستند. على سبيل المثال، يُظهر الرسم التالي سير عمل لتقارير المصروفات.

![سير عمل مع عناصر تم تعيينها للمستخدمين.](./media/workflow_user.gif)

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]