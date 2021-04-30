---
title: إنشاء مشروع موحد البيانات (معاينة)
description: يشرح هذا الموضوع كيفية إنشاء مشروع موحد البيانات.
author: ShivamPandey-msft
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 9ecf6ef7b7f052ebbb1201dcd04a7431f5b72ce5
ms.sourcegitcommit: b64c52d85aa6f110f3b1959a5521637dd8631b5b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867437"
---
# <a name="create-a-data-integrator-project-preview"></a>إنشاء مشروع موحد البيانات (معاينة)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

يشرح هذا الموضوع كيفية إنشاء مشروع موحد البيانات.

1. تسجيل الدخول إلى Microsoft Dynamics 365 Finance.
2. انتقل إلى **مساحات العمل \> إدارة البيانات**، وحدد **كيانات البيانات**. انتظر حتى يتم تحديث كافة كيانات البيانات قبل الانتقال إلى الخطوة التالية.
3. افتح مدخل [Power Apps ](https://make.powerapps.com/)، واتبع الخطوات التالية:

    1. حدد البيئة المناسبة.
    2. في جزء التنقل الأيسر، حدد **البيانات \> الاتصالات**.
    3. الاتصال بالمثيلات المناسبة للعناصر التالية:

        - Dynamics 365
        - Dynamics 365 for Fin & Ops

4. افتح البيئات [Power Apps ](https://admin.powerapps.com/environments)، واتبع الخطوات التالية:

    1. حدد **موحد البيانات**.
    2. حدد **مجموعات الاتصال**.
    3. حدد **مجموعة اتصال جديدة**.
    4. أدخل اسمًا للاتصال.
    5. حدد الاتصالات المناسبة للأصناف التالية:

        - Dynamics 365
        - Dynamics 365 for Fin & Ops

    6. حدد تعيين المؤسسة المناسب.
    7. حدد **إنشاء**.

5. افتح البيئات [Power Apps ](https://admin.powerapps.com/environments)، واتبع الخطوات التالية:  

    1. إنشاء مشاريع تكامل البيانات للقوالب التالية باستخدام مجموعة الاتصال التي قمت بإنشائها:

        - نتائج معلومات الدفع الخاصة بالعميل (CDS لـ Fin وOps)
            - إذا كنت تستخدم الإصدار 10.0.17 أو إصدار أحدث، ستحتاج إلى استخدام القالب المسمى، نتيجة الرؤى لمدفوعات العميل (CDS إلى Fin and Ops 10.0.17+).
        - نتائج السلسلة الزمنية للتدفق النقدي (CDS لـ Fin وOps)
        - نتائج السلسلة الزمنية للموازنة (CDS لـ Fin وOps)

    2. قم بتعيين الجدولة المناسبة لكل مشروع.

> [!NOTE]
> في حالة عدم رؤية الكيانات المطلوبة في CDS، الرجاء الانتقال إلى **عمليات التحصيل والائتمان > الضبط > Finance Insights > معلمات Finance insights**، قم بتمكين ميزة توقعات دفع العميل وانقر فوق الزر **إنشاء نموذج توقع**. عند اكتمال نشر نموذج AI (ناجح أو فاشل)، فإنه سيتم نشر كيانات CDS المطلوبة لإنشاء تكامل في CDS.

## <a name="privacy-notice"></a>إشعار الخصوصية

إن المعاينات (1) قد تستخدم تدابير أقل تتعلق بالخصوصية وإجراءات الأمان مقارنةً بخدمة Dynamics 365 Finance and Operations‏، و(2) لا يتم تضمينها في اتفاقية مستوى الخدمة (SLA) لهذه الخدمة، و(3) يجب ألا يتم استخدامها لمعالجة البيانات الشخصية أو البيانات الأخرى التي تخضع لمتطلبات التوافق القانونية أو التنظيمية، و(4) هي ذات دعم محدود.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
