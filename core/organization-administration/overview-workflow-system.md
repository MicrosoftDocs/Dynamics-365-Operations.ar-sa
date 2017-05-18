---
title: "نظرة عامة على نظام سير العمل"
description: "يوضح هذا الموضوع نظام سير العمل في Microsoft Dynamics 365 for Operations."
author: sericks007
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 5432e67ffa41e6a38b19c9fe5bb12c5acb2c345c
ms.contentlocale: ar-sa
ms.lasthandoff: 04/25/2017


---

# <a name="workflow-system-overview"></a>نظرة عامة على نظام سير العمل

[!include[banner](../includes/banner.md)]


يوضح هذا الموضوع نظام سير العمل في Microsoft Dynamics 365 for Operations.

<a name="what-is-workflow"></a>ما المقصود بسير العمل؟
-----------------

المصطلح *سير* يمكن تعريفه بطريقتين: كنظام وكعملية تجارية.
### <a name="workflow-is-a-system"></a>سير العمل كنظام

سير العمل عبارة عن نظام مثبت مع Dynamics 365 for Operations ويتم تشغيله على خادم كائنات التطبيق‬ (AOS). يوفر نظام سير العمل الوظائف التي يمكن استخدامها في إنشاء سير عمل فردي، أو عمليات تجارية.

### <a name="workflow-is-a-business-process"></a>سير العمل كعملية تجارية

يعد سير العمل بمثابة عملية تجارية. فهو يحدد كيفية تدفق المستند، أو انتقاله عبر النظام عن طريق عرض الفرد المنوط بإكمال المهمة، أو اتخاذ القرار أو الموافقة على المستند. على سبيل المثال، يُظهر الرسم التالي سير عمل لتقارير المصروفات. 

![سير عمل مع عناصر تم تعيينها للمستخدمين](./media/workflow_user.gif) 

لاستيعاب سير العمل هذا على نحو أفضل، لنفترض أن سامي يقدم تقرير مصروفات بمبلغ 7000 دولار أمريكي. في هذا السيناريو، يجب أن يقوم فريد بمراجعة عمليات الاستلام التي يقوم سامي بتوجيهها له. بعد ذلك يجب أن يقوم تميم وسلمان باعتماد تقرير المصروفات. لنفترض الآن أن سامي يقدم تقرير مصروفات بمبلغ 11.000 دولار أمريكي. ففي هذا السيناريو، يجب أن يقوم فريد بمراجعة عمليات الاستلام ولا بد من اعتماد التقرير من قبل تميم وسلمان وسليم.

## <a name="benefits-of-using-the-workflow-system"></a> فوائد استخدام نظام سير العمل

ويترتب على استخدام نظام سير العمل في المؤسسة العديد من الفوائد:
-   **عمليات متسقة** — يمكنك تحديدمستندات بعينها تمت معالجتها، مثل طلبات الشراء وتقارير المصروفات. ومن خلال استخدام نظام سير العمل، فأنت تؤكد على أنه تتم معالجة المستندات واعتمادها بأسلوب متسق وفعال.
-   **وضوح العمليات** - يمكنك تتبع حالة وتاريخ ومعايير أداء مثيلات سير العمل. ويساعدك هذا الأمر على تحديد ما إذا كانت هناك ضرورة لإجراء تغييرات على سير العمل لتحسين كفاءته أم لا.
-   **قائمة العمل المركزية** — يمكن للمستخدمين عرض قائمة عمل مركزية تعرض مهام سير العمل والموافقات المعينة لهم.


## <a name="workflow-content"></a>محتوى سير العمل

+ [بنية سير العمل](workflow-system-architecture.md)
+ [عناصر سير العمل](workflow-elements.md)
+ [إجراءات سير العمل](workflow-actions.md)
+ [إنشاء سير عمل](create-workflow.md)
+ [تكوين خصائص سير العمل](configure-workflow-properties.md)
+ [تكوين مهمة يدوية في سير عمل‬](configure-manual-task-workflow.md)
+ [تكوين مهمة مؤتمتة في سير عمل‬](configure-automated-task-workflow.md)
+ [تكوين عملية اعتماد في سير عمل](configure-approval-process-workflow.md)
+ [تكوين خطوة اعتماد في سير عمل](configure-approval-step-workflow.md)
+ [تكوين قرار يدوي في سير عمل](configure-manual-decision-workflow.md)
+ [تكوين قرار شرطي في سير عمل‬](configure-conditional-decision-workflow.md)
+ [تكوين نشاط موازٍ في سير عمل](configure-parallel-activity-workflow.md)
+ [تكوين فرع موازٍ في سير عمل](configure-parallel-branch-workflow.md)
+ [تكوين سير عمل لعنصر بند](configure-line-item-workflow.md)

