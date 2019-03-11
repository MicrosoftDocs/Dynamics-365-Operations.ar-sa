---
title: قابلية التوسعة‬ في Attract
description: يصف هذا الموضوع كيف يمكنك توسيع تطبيق Microsoft Dynamics 365 for Talent - Attract باستخدام النظام الأساسي Microsoft Power.
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: d9e1dd3a67c5f64b5d05f0f171226085138e0b44
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "303081"
---
# <a name="extensibility-in-attract"></a>قابلية التوسعة‬ في Attract

[!include[banner](../includes/banner.md)]

تم بناء Microsoft Dynamics 365 for Talent استنادًا إلى النظام الأساسي Common Data Service (CDS) للتطبيقات، ويمكن توسيعه بطرق مختلفة باستخدام النظام الأساسي Microsoft Power والقدرات التي تقدمها Common Data Service للتطبيقات. لذلك، يمكنك تكوين وتخصيص النظام باستخدام Microsoft PowerApps وMicrosoft Flow. ويمكنك أيضًا الحصول على تحليلات إضافية حول الأشخاص باستخدام Microsoft Power BI. علاوة على ذلك، ثمة أنشطة مخصصة جديدة، مثل أنشطة PowerApps ومحتوى الويب (iframe)، تجعل عملية التوظيف قابلة للتكيف أكثر من أي وقت مضى. باستخدام هذه الأنشطة، يمكن تخصيص عملية التوظيف بحيث تتلاءم مع احتياجات وعمليات الأعمال لديك، ويمكنك أن تتأكد من حصول كل من فريق التوظيف والمرشحين على تجربة سلسة ومخصصة.

## <a name="take-advantage-of-the-microsoft-power-platform"></a>استفد من Microsoft Power Platform 

نظرًا لوجود كافة البيانات من Attract في Common Data Service للتطبيقات، يمكنك استخدام الأدوات من النظام الأساسي Microsoft Power لدمج احتياجات العمل الفريدة لديك في Attract.

### <a name="powerapps"></a>PowerApps

يمكنك استخدام PowerApps لإنشاء تطبيقات تتصل ببياناتك في Attract بسهولة، وتستخدم تعبيرات مثل التعبيرات في Microsoft Excel لإضافة المنطق. يمكنك تشغيل التطبيقات التي تقوم بإنشائها باستخدام PowerApps على الويب وعلى أجهزة Apple iOS وGoogle Android.

على سبيل المثال، يمكنك أن تجعل معارض الوظائف التي تقام في الجامعات أكثر سهولة بالنسبة إلى مسؤولي التعيين عن طريق إنشاء تطبيق منخفض المرتبة يسمح لهم بفحص السير الذاتية وإعداد المرشحين لمنصب ما في Attract. أو يمكنك إنشاء تطبيق يساعد في تلبية متطلبات التوافق الخاصة بمؤسستك. للحصول على مزيد من المعلومات حول PowerApps وكيفية استخدامه لإنشاء التطبيقات، راجع [دمج البيانات في Common Data Service للتطبيقات](https://docs.microsoft.com/en-us/powerapps).

### <a name="microsoft-flow"></a>Microsoft Flow 

يمكنك استخدام Microsoft Flow لإنشاء مهام سير عمل تلقائية تستخدم بيانات Attract. يمكنك الاتصال بسهولة بمئات من الخدمات والتطبيقات الشائعة من دون الحاجة إلى كتابة تعليمات برمجية. من خلال إنشاء مهام سير عمل تتفاعل مع كيانات وظائف Attract والمرشحين واستمارات التقديم في Common Data Service للتطبيقات، يمكنك أتمتة إجراءات مختلفة. على سبيل المثال، عندما يقبل أحد المرشحين العرض المقدم له، يمكن إرسال إعلام إلى فريق الإعداد أو يمكن الإعلان عن الخبر على Twitter. لمزيد من المعلومات حول مهام سير العمل، راجع [وثائق Microsoft Flow](https://docs.microsoft.com/en-us/flow/).

### <a name="power-bi"></a>Power BI

يسمح لك Power BI بإنشاء وعرض التقارير المخصصة ولوحات المعلومات التي توفر لك معلومات أكثر عمقًا حول بيانات Attract. للحصول على مزيد من المعلومات حول Power BI وكيفية إنشاء تقارير ولوحات المعلومات تفاعلية، راجع [وثائق Power BI](https://docs.microsoft.com/en-us/power-bi/).

### <a name="custom-activities"></a>الأنشطة المخصصة 

يمكنك إضافة أنشطة مخصصة، مثل أنشطة تطبيقات PowerApps ومحتوى الويب (iframe)، على مستوى قالب عملية الوظيفة أو أثناء إنشاء وظيفة جديدة. تسمح لك هذه الأنشطة بتخصيص عملية التوظيف وإحضار منطق العمل الفريد لمؤسستك إلى Attract.

#### <a name="powerapps-activity"></a>نشاط PowerApps 

يسمح نشاط PowerApps لمنشئ الوظيفة أو قالب عملية الوظيفة بتضمين تطبيقات PowerApps في سير عمل التوظيف. بعد إنشاء ونشر التطبيق، يمكنك إدخال معرّف التطبيق ف تكوينات النشاط. باستخدام تطبيقا PowerApps، يمكنك قراءة وكتابة البيانات إلى Common Data Service للتطبيقات. حتى أنه يمكنك ربط التطبيق بسير عمل. على سبيل المثال، لديك تطبيق يستخدمه مسؤولو التعيين لملء نموذج أثناء إجرائهم مقابلات عبر الهاتف. في هذه الحالة، يمكنك ربط التطبيق بسير عمل يقيّم ما إذا كان من الممكن نقل مقدم الطلب إلى مرحلة متقدمة في عملية تقديم طلب الحصول على الوظيفة‬. يمكن عرض هذا النوع من النشاط فقط بواسطة أعضاء فريق التوظيف. للحصول على مزيد من المعلومات حول كيفية تكوين نشاط PowerApps، راجع [الأنشطة في Attract‎](./activities-attract.md).

> [!NOTE]
> يتوفر نشاط PowerApps فقط مع المكون الإضافي Comprehensive hiring.

#### <a name="web-content-iframe-activity"></a>نشاط محتوى الويب (iframe)

يسمح لك نشاط محتوى الويب (iframe) بتضمين حل ويب مخصص أنشأته في عملية التوظيف أو مدخل المرشح. يمكنك قراءة وكتابة البيانات مباشرة من Common Data Service للتطبيقات. ويمكنك أيضًا تخصيص الحل بحيث يقوم بتشغيل مهام سير العمل أو الاستفادة من وظائف Microsoft Azure. للحصول على مزيد من المعلومات حول كيفية تكوين نشاط محتوى الويب، راجع [الأنشطة في Attract‎](./activities-attract.md).

> [!NOTE]
> يتوفر نشاط محتوى الويب فقط مع المكون الإضافي Comprehensive hiring.
