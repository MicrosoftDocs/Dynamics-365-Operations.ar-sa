---
title: "الصفحة الرئيسية للتخطيط الرئيسي"
description: "يتيح التخطيط الرئيسي للشركات إمكانية تحديد وموازنة الاحتياجات المستقبلية للمواد الخام والقدرة اللازمة لتلبية أهداف الشركة."
author: YuyuScheller
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 18ed011fa1c1aa35b4a401d51bffc6af19395577
ms.openlocfilehash: 030579ac73d6333ac4ed55433b9679a58247c088
ms.contentlocale: ar-sa
ms.lasthandoff: 02/13/2018

---

# <a name="master-planning-home-page"></a>الصفحة الرئيسية للتخطيط الرئيسي

[!include [banner](../includes/banner.md)]

في أساسه، يتيح التخطيط الرئيسي للشركات إمكانية تحديد وموازنة الاحتياجات المستقبلية للمواد الخام والقدرة اللازمة لتلبية أهداف الشركة. يقيّم التخطيط الرئيسي ما يلي: 

-  ما المواد الخام والقدرات المتوفرة حاليًا؟ 
-  ما المواد الخام والقدرات المطلوبة لإكمال الإنتاج؟ على سبيل المثال، ما الذي يجب أن يتم تصنيع أو شراؤه أو نقله أو طرحه جانبًا كمخزون احتياطي قبل أن يمكنك إكمال الإنتاج.

يستخدم التخطيط الرئيسي المعلومات لحساب المتطلبات وإنشاء الأوامر المخططة.

فيما يلي عمليات التخطيط الرئيسي الثلاث:

-  **التخطيط الرئيسي** - تحسب الخطة الرئيسية صافي المتطلبات. يعتمد على الأوامر الحالية الفعلية ويتيح للشركات إمكانية التحكم في تزويد المخزون على أساس فترة قصيرة أو بصفة يومية. هناك مصطلح آخر لوصفه ألا وهو *خطة صافي المتطلبات*. لمزيد من المعلومات، راجع [التخطيط الرئيسي](master-plans.md). 

-  **تخطيط التنبؤ** - يحسب جدول التنبؤ إجمالي المتطلبات. يعتمد على التوقعات المستقبلية (أو التنبؤات)، ويتيح للشركات إمكانية إجراء التخطيط طويل الأمد للمواد والقدرة. لمزيد من المعلومات، راجع [تخطيط التنبؤ](introduction-demand-forecasting.md). 

-  **التخطيط الرئيسي بين الشركات الشقيقة** - تحسب الخطة الرئيسية بين الشركات الشقيقة صافي المتطلبات عبر الكيانات القانونية. يقوم بتوصيل الطلب والتوريد بين الشركات ليس فقط لتأكيد طلب وتوريد الشركات لفترة قصيرة، ولكن أيضًا للطلب والتوريد المخطط (غير المؤكد بعد) لفترة طويلة. لمزيد من المعلومات، راجع [التخطيط الرئيسي بين الشركات الشقيقة](https://mbspartner.microsoft.com/AX/CourseOverview/1276) (التعليم الإلكتروني) (يتطلب حساب CustomerSource). 

تستطيع الشركات تغيير نتيجة الخطة. يمكنهم تشغيل الخطط التجديدية أو خطط صافي التغيير أو كلاهما. تقوم الخطط التجديدية بتحديث جميع المتطلبات، بينما لا تقوم خطط صافي التغيير إلا بتحديث الخطة المتعلقة بالعناصر المشتملة على متطلبات جديدة التي ظهرت منذ تشغيل الجدولة الأخيرة.

عادةً ما تشتمل خطط الجدولة الرئيسية على الفترة القصيرة، التي يمكنها أن تتراوح ما بين أسبوع واحد وستة أشهر في أي مكان. تحدد وحدة التخطيط الرئيسي احتياجات التوريد (المواد) والقدرة (الموارد) التي ستلبي الطلب الحالي (صافي المتطلبات). في معظم الشركات، يتم توسيعها لتشمل زمن وصول البضاعة التراكمي الأطول بين المنتجات المطلوب استلامها.

## <a name="learning-map"></a>خريطة التعلم

تُظهر خريطة التعلم‬ التالية المفاهيم والمهام الرئيسية التي تشكل إطار عمل وحدة التخطيط الرئيسي. انقر فوق الارتباطات الموجودة في القسم [الارتباطات السريعة](#quick-links) للتعرف على كيفية استخدام الوحدة النمطية.

[![خريطة التعلم للتخطيط الرئيسي](./media/master-planning-learning-map.png)](./media/master-planning-learning-map.png)

## <a name="quick-links"></a>ارتباطات سريعة

|      |   |
|------|---|
|        [الخطط الرئيسية](master-plans.md)       |     [إنشاء خطة مقيدة](./tasks/constrained-plan.md)  |
| [إنشاء خطة مادية للمنتجات المساعدة](./tasks/create-material-plan-co-products.md)   |  [التخطيط الرئيسي ووظائف المواقع المتعددة](master-plan-multisite-functionality.md)  |
| [إنشاء خطة بين الشركات الشقيقة](./tasks/create-intercompany-plan.md) | [نظرة عامة على التنبؤ بالطلب‬](introduction-demand-forecasting.md)  | 
|[مفاتيح الخفض](reduction-keys.md)| [أساسيات التخطيط الرئيسي](https://mbspartner.microsoft.com/AX/CourseOverview/1275) (التعليم الإلكتروني) (تتطلب حساب CustomerSource)     |
|  [التخطيط الرئيسي للتصنيع التحويلي](https://mbspartner.microsoft.com/D365E/CourseOverview/1514) (التعليم الإلكتروني) (تتطلب حساب CustomerSource) | [التخطيط الرئيسي بين الشركات الشقيقة](https://mbspartner.microsoft.com/AX/CourseOverview/1276) (التعليم الإلكتروني) (يتطلب حساب CustomerSource)|
                                  
## <a name="additional-resources"></a>الموارد الإضافية

### <a name="roadmaps"></a>خرائط الطريق
انتقل إلى [خارطة طريق Microsoft Dynamics 365](https://roadmap.dynamics.com/) لمعرفة الميزات الجديدة التي تم إصدارها والميزات الجديدة قيد التطوير.

### <a name="blogs"></a>المدونات
يمكنك العثور على الآراء والأخبار وغيرها من المعلومات حول التخطيط الرئيسي وغيرها من الحلول ضمن [مدونة فريق بحث وتطوير Dynamics AX Manufacturing](https://blogs.msdn.microsoft.com/axmfg) و[إدارة سلسلة التوريد في مدونة فريق بحث وتطوير Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm).

### <a name="task-guides"></a>دلائل المهام
تتوفر التعليمات الإضافية كدلائل مهام داخل Finance and Operations. وللوصول إلى دلائل المهام، انقر فوق الزر **تعليمات** في أي صفحة.

### <a name="webinars"></a>الندوات عبر الإنترنت
[استخدام التعلم الآلي من Azure للتنبؤ بالطلب](https://www.youtube.com/watch?v=4nQsccdFFDA&feature=youtu.be)

### <a name="tech-conference-recordings"></a>تسجيلات المؤتمر التقني
-  [توسيع وظيفة التنبؤ بالطلب](https://www.youtube.com/watch?v=4OIKIXLiNjI&feature=youtu.be)
-  [التخطيط الرئيسي - تلميحات ونصائح حول استكشاف أخطاء الأداء وإصلاحها](https://youtu.be/7v8BPmEs9Dg)
-  [التعليمات! تخطيط متطلبات المواد بطيء!](https://youtu.be/RLXybx20B5o)




