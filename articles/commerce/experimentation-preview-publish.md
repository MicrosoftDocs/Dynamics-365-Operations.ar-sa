---
title: معاينه التجربة ونشرها
description: يوضح هذا الموضوع كيفيه معاينه التجربة ونشرها من Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 32115378be00df771c6ff658da0c090446edf8b0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009921"
---
# <a name="preview-and-publish-an-experiment"></a>معاينه التجربة ونشرها

يصف هذا الموضوع كيفيه معاينه التجربة الخاصة بك ونشرها في Dynamics 365 Commerce بعد قيامك [بتوصيل التجربة وتحرير التباينات الخاصة بك](experimentation-connect-edit.md). يوضح الرسم التخطيطي التالي كافة الخطوات المتضمنة في اعداد وتشغيل تجربه علي أحد مواقع التجارة الالكترونيه في Dynamics 365 Commerce. وتتم تغطيه الخطوات الاضافيه في موضوعات منفصلة.

[![رحلة مستخدم التجربة - المعاينه والنشر](./media/experimentation_preview_publish.svg)](./media/experimentation_preview_publish.svg#lightbox)

## <a name="preview-your-experiment-variations"></a>معاينه تباينات التجربة الخاصة بك
يمكنك معاينه التباينات الخاصة بك ومتابعه تحريرها حتى تبدو بالطريقة التي تريدها.

لمعاينة تباينات التجربة الخاصة بك في منشئ مواقع Commerce، اتبع الخطوات التالية.

1. من القائمة المنسدلة تباينات أسفل شريط الأوامر، حدد المحتوى الذي تريد معاينته. 
1. في شريط الأوامر، حدد **معاينة**. يتم عرض معاينه لما سيبدو عليه المحتوي عند نشره.
1. لمعاينة تباين مختلف، قم بتحديده من القائمة المنسدلة الخاصة بالتباين وحدد **معاينة** مرة أخرى.

## <a name="publish-your-experiment"></a>انشر تجربتك
إذا كنت لا تستخدم مجموعه نشر لجدوله وقت وصول التجربة الخاصة بك وترغب في النشر علي الفور، حدد **نشر** في شريط الأوامر. سيتم نشر كافة الاختلافات التي تنتمي إلى التجربة.
    
> [!IMPORTANT]
> إذا كانت الصفحة تحتوي علي URL غير منشور، يجب أولا نشر محدد موقع المعلومات (URL) أو لن يكون مرئيا لمستخدمي موقع الويب الخاص بك. للحصول على مزيد من التفاصيل، راجع [حفظ صفحة ومعاينتها ونشرها](save-preview-publish-page.md).
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a>استخدام مجموعات النشر للجدولة عندما يتم نشر التجربة الخاصة بك بشكل مباشر
يمكن جدوله الاختلافات التي تم إنشاؤها في منشئ المواقع للنشر باستخدام مجموعه النشر. داخل مجموعة نشر، يمكنك توصيل صفحة أو جزء بتجربتك الخاصة عن طريق تحديد **تجارب** في جزء التنقل الأيسر. يمكنك أيضًا القيام بذلك عن طريق تحديد **الصفحات** أو **الأجزاء** واتباع التعليمات في [توصيل تجربة وتحرير التباينات](experimentation-connect-edit.md). للحصول على معلومات حول نشر المجموعات، راجع [العمل مع مجموعات النشر](publish-groups.md).

عند استخدامك نشر مجموعات مع التجارب، هناك بعض الاعتبارات الهامه التي يجب ان تكون علي علم بها.
- عندما تقوم باضافه صفحه أو جزء تم تشغيل تجربة عليه في مجموعه نشر، ستتم أزاله التجربة من الصفحة أو الجزء في مجموعه النشر.
- لا تتوفر التجارب المتصلة بالصفحات الموجودة في موقع مباشر للصفحات الموجودة في نشر المجموعات والعكس بالعكس. بالمثل، لا تتوفر الصفحات التي يتم تشغيل التجارب عليها في موقع مباشر لتجارب أخرى في مجموعات النشر والعكس.
- عند نشر مجموعه نشر أو جدولتها، يتم نشر كافة المحتويات الموجودة في مجموعه النشر، بغض النظر عما إذا كان هناك تجربه مقترنة بمجموعه النشر.
- ونظرا لاستمرار استمرار مجموعه النشر بعد نشرها إلى موقع مباشر ، ستستمر الاكسبيريمينتس في مجموعه النشر أيضا. لذلك، لن تتمكن من اقران التجارب الأخرى بنفس الصفحة أو الجزء. لتجنب هذا القيد، قم بحذف إيه مجموعات نشر تحتوي على تجارب مستمرة. بالمثل، إذا كنت ترغب في حذف تجربه في موقع مباشر موجود أيضا في مجموعه نشر، فقم بحذفه من مجموعة النشر أولا.

## <a name="previous-step"></a>الخطوة السابقة
[الاتصال بتجربة وتحريرها](experimentation-connect-edit.md)

## <a name="next-step"></a>الخطوة التالية
[تشغيل تجربة ومراقبتها](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]