---
title: إنشاء مشروع تكامل البيانات
description: توضح هذه المقالة كيفية إنشاء مشروع تكامل البيانات.
author: ShivamPandey-msft
ms.date: 05/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 4ff4f88c6c5d55d853aebd7d437bfb107292fb2f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876229"
---
# <a name="create-a-data-integration-project"></a>إنشاء مشروع تكامل البيانات

[!include [banner](../includes/banner.md)]

توضح هذه المقالة كيفية إنشاء مشروع تكامل البيانات.

1. سجل دخولك إلى Microsoft Dynamics 365 Finance.
2. انتقل إلى **مساحات العمل \> إدارة البيانات**، وحدد **كيانات البيانات**. انتظر حتى يتم تحديث كافة كيانات البيانات قبل الانتقال إلى الخطوة التالية.
3. افتح مدخل [Power Apps ](https://make.powerapps.com/)، واتبع الخطوات التالية:

    1. حدد البيئة المناسبة.
    2. في جزء التنقل الأيسر، حدد **Dataverse \> الاتصالات**.
    3. الاتصال بالمثيلات المناسبة للعناصر التالية:

        - Dynamics 365
        - Dynamics 365 for Fin & Ops

4. افتح البيئات [Power Apps ](https://admin.powerapps.com/environments)، واتبع الخطوات التالية:

    1. حدد **تكامل البيانات**.
    2. حدد **مجموعات الاتصال**.
    3. حدد **مجموعة اتصال جديدة**.
    4. أدخل اسمًا للاتصال.
    5. حدد الاتصالات المناسبة للأصناف التالية:

        - Dynamics 365
        - Dynamics 365 for Fin & Ops

    6. حدد تعيين المؤسسة المناسب.
    7. حدد **إنشاء**.

5. افتح البيئات [Power Apps ](https://admin.powerapps.com/environments)، واتبع الخطوات التالية:  

    1. إنشاء مشروع واحد لتكامل البيانات لكل قالب من القوالب التالية باستخدام مجموعة الاتصال التي قمت بإنشائها:

        - نتيجة رؤى الدفع للعملاء (CDS إلى Fin and Ops ‏10.0.17+)
        - نتائج السلسلة الزمنية للتدفق النقدي (CDS لـ Fin وOps)
        - نتائج السلسلة الزمنية للموازنة (CDS لـ Fin وOps)

      > [!NOTE]
      > قد يؤدي إنشاء مشاريع تكامل بيانات متعددة لكل قالب إلى حدوث أخطاء تؤدي إلى حظر التحديثات.

    2. قم بتعيين الجدولة المناسبة لكل مشروع.

> [!NOTE]
> في حالة عدم رؤية الكيانات المطلوبة في Dataverse، انتقل إلى **عمليات التحصيل والائتمان‬** > **إعداد** > **Finance Insights** > **معلمات Finance insights**، وقم بتمكين الميزة **توقعات دفع العميل**، ثم حدد **إنشاء نموذج توقع**. عند اكتمال نشر نموذج الذكاء الاصطناعي، سيتم نشر كيانات Dataverse المطلوبة لإنشاء التكامل.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
