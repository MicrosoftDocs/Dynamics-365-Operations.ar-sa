---
title: إنشاء مشروع موحد البيانات (معاينة)
description: يشرح هذا الموضوع كيفية إنشاء مشروع موحد البيانات.
author: ShivamPandey-msft
ms.date: 06/03/2021
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
ms.openlocfilehash: 59f85c64ea7b1f539a245e08b76bd6a34797b0ca
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186458"
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

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
