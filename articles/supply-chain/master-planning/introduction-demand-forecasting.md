---
title: "نظرة عامة على التنبؤ بالطلب‬"
description: "يتم استخدام التنبؤ بالطلب للتنبؤ بطلب غير معال من أوامر المبيعات وطلب معال عند أي نقطة اتصال لأوامر العملاء. توفر قواعد خفض التنبؤ بالطلب المحسن حلاً مثاليًا للتخصيص الشامل."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 72004
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 20eb67a341f462328bc73907fb3052b3405190d4
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---

# <a name="demand-forecasting-overview"></a>نظرة عامة على التنبؤ بالطلب‬

[!include [banner](../includes/banner.md)]

يتم استخدام التنبؤ بالطلب للتنبؤ بطلب غير معال من أوامر المبيعات وطلب معال عند أي نقطة اتصال لأوامر العملاء. توفر قواعد خفض التنبؤ بالطلب المحسن حلاً مثاليًا للتخصيص الشامل.

لإنشاء تنبؤ خط أساسي، يتم تمرير ملخص الحركات المسجلة إلى خدمة Microsoft Azure Machine Learning التي يتم استضافتها على Azure. لأنه لا تتم مشاركة هذه الخدمة بين المستخدمين، فإنه يمكن تخصيصها بسهولة لتلبي المتطلبات الخاصة بالصناعة. يمكنك استخدام Finance and Operations لإظهار التنبؤ وتعديل التنبؤ وعرض مؤشرات الأداء الرئيسية (KPI) حول دقة التنبؤ.

## <a name="key-features-of-demand-forecasting"></a>الميزات الرئيسية للتنبؤ بالطلب
فيما يلي بعض الميزات الرئيسية للتنبؤ بالطلب:

-   قم بإنشاء تنبؤ أساسي إحصائي يعتمد على بيانات مسجلة.
-   استخدم مجموعة ديناميكية من أبعاد التنبؤ.
-   قم بإظهار اتجاهات الطلب وفواصل الثقة وتعديلات للتنبؤ.
-   قم بتخويل التنبؤ المعدل ليتم استخدامه في عمليات التخطيط.
-   إزالة القيم المتطرفة.
-   إنشاء قياس دقة التنبؤ.

## <a name="major-themes-in-demand-forecasting"></a>المواضيع الرئيسية في التنبؤ بالطلب
يتم تنفيذ المواضيع الرئيسية الثلاثة في التنبؤ بالطلب:

-   **النمطية** - إن التنبؤ بالطلب أمر نمطي وسهل التكوين. يمكنك تشغيل الوظيفة وإيقاف تشغيلها عن طريق تغيير مفتاح التكوين في **التجارة‏‎** &gt; **التنبؤ بالمخزون** &gt; **التنبؤ بالطلب**.
-   **‬‏‫إعادة استخدام مكدس Microsoft** – أطلقت Microsoft نظام "Machine Learning" الأساسي في شباط/فبراير عام 2015. يتيح لك Machine Learning، الذي يُعد الآن جزءًا من مجموعة التحليلات Microsoft Cortana، إنشاء تجارب التحليل التنبؤية، مثل التجارب تقدير الطلب، بسرعة وسهولة باستخدام خوارزميات R أو لغات البرمجة بيثون وواجهة سحب وإفلات بسيطة.‬
    -   يمكنك تنزيل تجارب التنبؤ بالطلب في Finance and Operations وتغييرها لتلبية متطلبات العمل ونشرها كخدمة ويب على Azure واستخدامها لإنشاء التنبؤات بالطلب. تتوفر التجارب للتنزيل إذا قمت بشراء اشتراك Finance and Operations لمخطط إنتاج كمستخدم على مستوى المؤسسة.
    -   يمكنك تنزيل أي من التجارب توقع الطلب المتوفرة حاليًا من [معرض التحليلات Cortana](https://gallery.cortanaanalytics.com/). في حين يتم تكامل تجارب التنبؤ بالطلب في Finance and Operations تلقائيًا مع Finance and Operations، يجب على العملاء والشركاء معالجة تكامل التجارب التي قاموا بتنزيلها من [معرض تحليلات Cortana](https://gallery.cortanaanalytics.com/). ومن ثمَّ، لا تكون التجارب من [معرض تحليلات Cortana](https://gallery.cortanaanalytics.com/) واضحة ومباشرة لاستخدامها كتجارب التنبؤ بالطلب في Finance and Operations. يجب عليك تعديل كود التجارب لتستخدم واجهة برمجة تطبيقات Finance and Operations.
    -   يمكنك إنشاء التجارب الخاصة بك في Microsoft Azure Machine Learning Studio ونشرها كخدمات على Azure واستخدامها لإنشاء التنبؤ بالطلب.
    -   إذا كنت لا تحتاج إلى أداء عالي أو إذا كنت لا تحتاج إلى معالجة كمية كبيرة من البيانات، يمكنك استخدام Machine Learning free tier. نوصي بأن تبدأ من هذا المستوى، خاصة أثناء مرحلتي الاختبار والتنفيذ. إذا كنت تحتاج إلى مستوى أعلى من الأداء ومساحة تخزين إضافية، فإنه يمكنك استخدام Machine Learning standard tier. يتطلب هذا المستوى اشتراك Azure وينطوي على تكاليف إضافية. لمزيد من التفاصيل حول أسعار Machine Learning، راجع <http://aka.ms/machine-learning-price-info>.
-   **خفض التنبؤ في أي نقطة اتصال** – يعتمد التنبؤ بالطلب في Forecast reduction at any decoupling point على هذه الوظيفة، التي تتيح لك التنبؤ بالطلب التابع والمستقل في أي نقطة اتصال.

## <a name="basic-flow-in-demand-forecasting"></a>تدفق الأساسي في التنبؤ بالطلب
ويوضح الرسم التخطيطي التالي التدفق الأساسي للتنبؤ بالطلب. 

[![مخطط مقدمة التنبؤ بالطلب‬‏‫](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

يبدأ إنشاء التنبؤ بالطلب في Finance and Operations. يتم تجميع بيانات الحركات المسجلة من قاعدة بيانات الحركات في Finance and Operations وتملأ جدولاً مرحليًا. تتم تغذية هذا الجدول المرحلي فيما بعد إلى خدمة Machine Learning. عن طريق إجراء تخصيص الحد الأدنى، يمكنك توصيل مصادر البيانات المختلفة بالجدول المرحلي.‬ ‏‫يمكن أن تتضمن مصادر البيانات ملفات Microsoft Excel وملفات قيمة مفصولة بفاصلة (CSV) والبيانات من Microsoft Dynamics AX 2009 وMicrosoft Dynamics AX 2012. لذلك، يمكنك إنشاء التنبؤات بالطلب التي تأخذ بعين الاعتبار البيانات المسجلة التي تنتشر بين الأنظمة المتعددة.‬ ومع ذلك، يجب أن تكون البيانات الرئيسية، مثل أسماء العناصر ووحدات القياس، هي نفسها عبر مصادر البيانات المختلفة.

إذا كنت تستخدم تجارب التعلم الآلي في التنبؤ بالطلب Finance and Operations، فإنها تبحث عن أفضل ملاءمة بين أساليب التنبؤ لسلاسل الوقت الخمس لحساب تنبؤ الخط الأساسي. تتم إدارة معلمات أساليب التنبؤ هذه في Finance and Operations. 

وتتوفر عندئذٍ التنبؤات والبيانات القديمة وأي تغييرات أجريت على التنبؤات بالطلب في التكرارات السابقة في Finance and Operations. 

يمكنك استخدام Finance and Operations. لتصور تنبؤات الخط الأساسي وتعديلها. يجب أن يتم تخويل التعديلات اليدوية قبل أن يتم استخدام التنبؤات للتخطيط.

## <a name="limitations"></a>قيود
التنبؤ بالطلب في Finance and Operations هو أداة تساعد العملاء في قطاع الصناعة على إنشاء عمليات التنبؤ. ‏‫ويوفر الوظائف الأساسية لحل التنبؤ بالطلب ويتم تصميمه حتى يمكن توسيعه بسهولة. قد لا يكون التنبؤ بالطلب الأفضل مناسبةً للعملاء في صناعات مثل البيع بالتجزئة أو الجملة أو التخزين أو النقل أو الخدمات المهنية الأخرى.‬

<a name="additional-resources"></a>الموارد الإضافية
--------

[إعداد التنبؤ بالطلب](demand-forecasting-setup.md)

[إنشاء التنبؤ الأساسي الإحصائي](generate-statistical-baseline-forecast.md)

[القيام بتسويات يدوية في تنبؤ الخط الأساسي](manual-adjustments-baseline-forecast.md)

[تخويل ‏‫التنبؤ الذي تمت تسويته](authorize-adjusted-forecast.md)

[مراقبة دقة التنبؤ](monitor-forecast-accuracy.md)

[إزالة القيم المتطرفة من بيانات الحركة القديمة عند حساب التنبؤ بالطلب](remove-historical-outliers-calculating-demand-forecast.md)

[توسيع وظيفة التنبؤ بالطلب](https://www.youtube.com/watch?v=4OIKIXLiNjI&feature=youtu.be)




