---
title: "الاتصال بنظام التعليمات"
description: "يصف هذا الموضوع مكونات نظام تعليمات تطبيق Microsoft Dynamics 365 for Finance and Operations، ويقدم لمحة عامة عن كيفية توصيلها بالإضافة إلى ملخص حول كيفية إنشاء تعليمات مخصصة."
author: margoc
manager: AnnBe
ms.date: 09/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c0942b66859da3659be49b19986bfd146ac43130
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="connect-the-help-system"></a>الاتصال بنظام التعليمات

[!INCLUDE [banner](../includes/banner.md)]

يصف هذا الموضوع المكونات التي تشكّل نظام تعليمات Microsoft Dynamics 365 for Finance and Operations. ويقدم نظرة عامة حول كيفية توصيل هذه المكونات وملخصًا لكيفية إنشاء تعليمات مخصصة. 

## <a name="help-architecture"></a>بنية التعليمات
يبين الرسم التوضيحي التالي أجزاء نظام تعليمات Finance and Operations. يعمل نظام التعليمات في المنتج على سحب المقالات من موقع Finance and Operations الموجود على https://docs.microsoft.com، وكذلك من دلائل المهام المخزنة في "أداة تكوين عمليات الأعمال" في Lifecycle Services (LCS)‎. 
> [!NOTE]
> الميزات المدرجة في الرسم التخطيطي مع العلامة النجمية (\*) عبارة عن ميزات تم التخطيط لإصدارها، ولكنها غير متوفرة حتى الآن. [![بنية التعليمات](./media/help-architecture.png)](./media/help-architecture.png)


## <a name="connecting-the-help-system"></a>الاتصال بنظام التعليمات
> [!NOTE]
> علامة التبويب **دلائل المهام** غير متوفرة بعد في كل من Microsoft Dynamics 365 for Talent وMicrosoft Dynamics 365 for Retail. نحن نعمل حاليًا على تمكين هذه الوظيفة في إصدار مستقبلي. تبقى دلائل المهام في تجربة "بدء الاستخدام" في Talent متوفرة لتغطية الوظائف الأساسية. تتوفر أيضًا تعليمات إجرائية في الموقع docs.microsoft.com site ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) لكل من Retail وTalent.


من خلال استخدام صفحة **معلمات النظام**، يتصل مسؤولو النظام بأجزاء نظام التعليمات لتطبيقها. [![نموذج معلمات النظام مع إعدادات التعليمات](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) في صفحة **معلمات النظام**‎، اتبع الخطوات التالية:

> [!IMPORTANT]
> في المرة الأولى التي تفتح فيها علامة التبويب **تعليمات** يجب الاتصال بميزة Lifecycle Services. احرص على النقر فوق الارتباط الموجود في وسط النموذج، وانتظر الاتصال، وقم بإغلاق مربع الحوار، ثم انقر فوق **موافق** للانتقال إلى صفحة **معلمات النظام**.[![الاتصال بـ LCS](./media/connect-to-lcs-crop-1024x365.png "الاتصال بـ LCS")](./media/connect-to-lcs-crop.png)

1.  تحديد مشروع Lifecycle Services المراد الاتصال به.
2.  تحديد مكتبات BPM (في المشروع المحدد) لاسترداد تسجيلات المهام منها.
    - بالنسبة إلى Finance and Operations، ولمحتوى Microsoft، حدد المكتبة الموحدة APQC (فبراير 2017) الأحدث لتطبيق Finance and Operations. 
    - بالنسبة إلى Retail، سنقوم بإصدار مكتبة في المستقبل القريب. 
    - لا تحتاج إلى تحديد مكتبة لتطبيق Talent — يتم تأسيس الاتصال بالمكتبة الصحيحة بالنيابة عنك. 

3.  تعيين أمر العرض لمكتبات BPM. ويحدد هذا الترتيب الذي ستظهر به تسجيلات المهام من المكتبات في جزء **المساعدة**.

بعد أن تكمل هذه الخطوات، يمكنك فتح جزء **التعليمات** والنقر فوق علامة تبويب **دلائل المهام**. سترى الآن دلائل المهام التي تنطبق على الصفحة التي تعمل عليها حاليًا في Finance and Operations. إذا لم تعثر على دلائك المهام، فيمكنك إدخال كلمات أساسية لتنقية البحث.

### <a name="showing-translated-task-guides"></a>إظهار دلائل المهام المترجمة

تم شحن دلائل المهام المترجمة لأول مرة في شهر مايو 2016 لمكتبة بدء الاستخدام والمكتبة الموحدة APQC. في Finance and Operations، لرؤية تعليمات دلائل المهام المترجمة، تأكد من اتصالك بمكتبة مايو. يمكن للمستخدم التحكم في اللغة التي يظهر بها دليل المهام بواسطة إعدادات اللغة ضمن**الخيارات** &gt; **التفضيلات**. 

> [!NOTE]
> على الرغم من العدد الكبير من دلائل المهام التي تمت ترجمتها، إلا أن عميل Finance and Operations لا يعرض أسماء دلائل المهام المترجمة. علاوةً على ذلك، لا تتضمن مكتبة شهر مايو سوى دلائل المهام المترجمة التي تم إصدارها في شهر فبراير 2016. سوف نقوم بإصدار مكتبة محدثة تضم ترجمات إضافية.
> -   إذا كان دليل المهمة مترجمًا، فسيظهر نصه بلغتك المحددة عندما تفتحه.
> -   إذا لم يكن دليل المهمة مترجمًا بعد، فسيظهر بعض النص فقط (نصر عناصر التحكم) بلغتك المحددة عندما تفتحه.

## <a name="creating-custom-help"></a>إنشاء التعليمات المخصصة
يمكنك إنشاء تعليمات مخصصة لتطبيق Finance and Operations وRetail بإنشاء تسجيلات المهام التي تعكس التنفيذ، وحفظها إلى مكتبة عمليات أعمال LCS. لا يمكنك إنشاء دلائل مهام مخصصة لتطبيق Talent. 

وبالنسبة للشركاء، إذا قمت بترقية مكتبة إلى مكتبة شركة وقمت بتضمينها في أحد حلول، فستتوفر للعملاء. يمكنك أيضًا إنشاء نسخة من المكتبة العمومية الموحدة APQC، ثم فتح نسختك وفتح تسجيلات المهام منها وتعديلها وحفظ التسجيلات مع تغييراتك. لمزيد من المعلومات، راجع [كيفية إنشاء تسجيل مهام لاستخدامه كوثيقة أو تدريب](../../dev-itpro/user-interface/task-recorder.md).

<a name="see-also"></a>راجع أيضًا
--------

[نظرة عامة حول التعليمات](help-overview.md)

[نظرة عامة حول مسجل المهام](../../dev-itpro/user-interface/task-recorder.md)

[كيفية إنشاء تسجيل مهمة لاستخدامه كوثائق أو تدريب](../../dev-itpro/user-interface/task-recorder-training-docs.md)





