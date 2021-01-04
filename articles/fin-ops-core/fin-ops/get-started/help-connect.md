---
title: تكوين تجربة التعليمات لتطبيقات Finance and Operations
description: يوفر هذا الموضوع معلومات حول مكونات نظام التعليمات لبعض تطبيقات Microsoft Dynamics 365. كما يوضح كيفية توصيل هذه التطبيقات وتوفير ملخص لعملية إنشاء تعليمات مخصصة.
author: margoc
manager: AnnBe
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0495bbc008ed1760b98c2c1ace63fc4a8b1ab5cc
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694411"
---
# <a name="configure-the-help-experience-for-finance-and-operations-apps"></a>تكوين تجربة التعليمات لتطبيقات Finance and Operations

[!include [banner](../includes/banner.md)]

في هذا الموضوع، ستجد نظرة عامة على مكونات نظام التعليمات لتطبيقات Finance and Operations، مثل Microsoft Dynamics 365 Finance وDynamics 365 Supply Chain Management وDynamics 365 Commerce وDynamics 365 Human Resources. يوضح الموضوع أيضًا كيفية توصيل هذه التطبيقات ويوفر ملخصًا لعملية إنشاء تعليمات مخصصة.

## <a name="help-architecture"></a>بنية التعليمات

تشمل تطبيقات Finance and Operations نظرات تصورية ومواضيع أخرى يتم نشرها على موقع [https://docs.microsoft.com/dynamics365](/dynamics365/). يمكن بعد ذلك الوصول إلى هذا المحتوى من خلال جزء **التعليمات** داخل المنتج. يبين الرسم التوضيحي التالي أجزاء نظام التعليمات.

[![بنية التعليمات](./media/help-architecture.png)](./media/help-architecture.png)

يقوم نظام التعليمات داخل المنتج بسحب المقالات من docs.microsoft.com ومواقع ويب الأخرى المتصلة. كما يسحب أيضًا أدلة المهام التي يتم تخزينها في ‏‫أداة تكوين عمليات الأعمال (BPM)‬ في Microsoft Dynamics Lifecycle Services (LCS).

## <a name="adding-task-guides"></a>إضافة دلائل المهام

> [!NOTE]
> في الوقت الحالي لا تتوفر علامة التبويب **دلائل المهام** في Human Resources أو Commerce. <!--We are currently working to enable this functionality in a future release.--> مع ذلك، تظل دلائل المهام في تجربة "بدء الاستخدام" في Human Resources متاحة لتغطية الوظائف الأساسية. فيما يتعلق بكل من Human Resources وCommerce، تتوفر تعليمات إجرائية على موقع [https://docs.microsoft.com/dynamics365](/dynamics365/).

في صفحة **معلمات النظام**، يمكن لمسؤولي النظام تكوين الوصول إلى مكتبات دلائل المهام ذات الصلة لأي عملية تنفيذ.

> [!NOTE]
> - لتكوين التعليمات، يجب أن تسجل الدخول باستخدام حساب في المستأجر نفسه الذي تم فيه نشر التطبيق.
> - لا يمكن الاتصال بمكتبة LCS من مثيل تطبيق قيد التشغيل على محرك أقراص ثابت محلي ظاهري (VHD).

[![نموذج محددات النظام مع إعدادات نظام التعليمات](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)

لتكوين دلائل مهام لأحد الحلول، اتبع الخطوات التالية في صفحة **معلمات النظام**.

> [!IMPORTANT]
> في المرة الأولى التي تفتح فيها علامة التبويب **تعليمات** يجب الاتصال بميزة Lifecycle Services. احرص على تحديد الارتباط الموجود في وسط النموذج، وانتظر الاتصال، ثم قم بإغلاق مربع الحوار، ثم حدد **موافق** للوصول إلى صفحة **معلمات النظام**.
>
> [![الاتصال بـ LCS](./media/connect-to-lcs-crop-1024x365.png "الاتصال بـ LCS")](./media/connect-to-lcs-crop.png)

1. تحديد مشروع Lifecycle Services المراد الاتصال به.
2. تحديد مكتبات BPM (في المشروع المحدد) لاسترداد تسجيلات المهام منها.
3. تعيين أمر العرض لمكتبات BPM. ويحدد ترتيب العرض الترتيب الذي ستظهر به تسجيلات المهام من المكتبات في جزء **المساعدة**.

بعد أن تكمل هذه الخطوات، يمكنك فتح جزء **التعليمات** وتحديد علامة تبويب **دلائل المهام**. سترى الآن دلائل المهام التي تنطبق على الصفحة التي تعمل عليها حاليًا في تطبيقات Finance and Operations. إذا لم تعثر على دلائك المهام، فيمكنك إدخال كلمات أساسية لتنقية البحث.

### <a name="showing-translated-task-guides"></a>إظهار دلائل المهام المترجمة

تم إصدار دلائل المهام المترجمة لأول مرة في شهر مايو 2016 لمكتبة بدء الاستخدام والمكتبة الموحدة APQC. لرؤية تعليمات دلائل المهام المترجمة، تأكد من اتصال حل Dynamics 365 بمكتبة مايو 2016. يمكن للمستخدمين تغيير اللغة التي يظهر بها دليل المهام بواسطة تغيير إعدادات اللغة ضمن **الخيارات** &gt; **التفضيلات**.

> [!NOTE]
> على الرغم من ترجمة العديد من دلائل المهام، إلا أن العميل لا يعرض الآن أسماء دلائل المهام المترجمة. علاوةً على ذلك، في مكتبة شهر مايو، تتوفر الترجمات فقط لدلائل المهام المترجمة التي تم إصدارها في شهر فبراير 2016. سوف تصدر Microsoft مكتبة محدثة تشمل الترجمات الإضافية.
>
> - إذا كان دليل المهمة مترجمًا، فسيظهر نصه بلغتك المحددة عندما تفتحه.
> - إذا لم يكن دليل المهمة مترجمًا بعد، فسيظهر بعض النص فقط (نصر عناصر التحكم) بلغتك المحددة عندما تفتحه.

## <a name="adding-custom-help"></a>إضافة تعليمات مخصصة

يمكنك استخدام أدلة المهام لإنشاء تعليمات مخصصة أو يمكنك ربط موقع الويب لتعليمات مخصصة بجزء **التعليمات**.

### <a name="create-custom-help-by-using-task-guides"></a>إنشاء تعليمات مخصصة باستخدام دلائل المهام

يمكنك إنشاء تعليمات مخصصة للتطبيقات المدعومة عن طريق إنشاء تسجيلات المهام التي تعكس التنفيذ ثم حفظها إلى مكتبة عملية أعمال في LCS. لا يمكنك إنشاء دلائل مهام مخصصة لـ Human Resources.

إذا كنت شريكًا، وقمت بترقية مكتبة إلى مكتبة شركة وقمت بتضمينها في أحد حلول، فستتوفر للعملاء الخاصين بك. يمكنك أيضًا إنشاء نسخة من المكتبة العمومية الموحدة APQC، ثم فتح تسجيلات المهام في النسخة وتحريرها وحفظ التغييرات الخاصة بك. لمزيد من المعلومات، راجع [موارد مسجل المهام](../../dev-itpro/user-interface/task-recorder.md).

### <a name="connect-a-custom-help-site"></a>الاتصال بموقع تعليمات مخصص

نادرًا ما يتم استخدام تطبيقات Finance and Operations في نموذج جاهز لها. بدلا من ذلك، يتم تخصيص الحل وتوسيعه لملائمة احتياجات المؤسسة. يمكنك أيضا تخصيص تجربة التعليمات وتوسيعها. على سبيل المثال، يمكنك إضافة تعليمات مخصصة إلى جزء **تعليمات** داخل المنتج.

قامت Microsoft بتوفير مجموعة أدوات تساعدك في نشر التعليمات المخصصة وتوصيلها بجزء **التعليمات**. للحصول على معلومات حول كيفية إعداد حل تعليمات مخصص متصل جزء **التعليمات**، راجع [نظرة عامة حول التعليمات المخصصة](../../dev-itpro/help/custom-help-overview.md).

إذا كنت ترغب في التعاون مع Microsoft بشأن الأدوات والعمليات الخاصة بتخصيص التعليمات، فقم بملء النموذج في [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback)

## <a name="see-also"></a>راجع أيضًا

[نظام التعليمات](help-overview.md)  
[نظرة عامة حول التعليمات المخصصة](../../dev-itpro/help/custom-help-overview.md)  
[موارد مسجل المهام](../../dev-itpro/user-interface/task-recorder.md)  
[إنشاء الوثائق أو التدريب بمسجل المهام](../../dev-itpro/user-interface/task-recorder-training-docs.md)  
[مستودع GitHub للتعليمات المخصصة](https://github.com/microsoft/dynamics356f-o-custom-help)  
