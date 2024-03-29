---
title: إعداد ملف تعريف الإعلام بالبريد الإلكتروني
description: يوضح هذا المقال كيفية إنشاء ملف تعريف إخطار البريد الإلكتروني في Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: db6c46d471e3b54982132df3e4819236833cf4a8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292125"
---
# <a name="set-up-an-email-notification-profile"></a>إعداد ملف تعريف الإعلام بالبريد الإلكتروني

[!include [banner](includes/banner.md)]

يوضح هذا المقال كيفية إنشاء ملف تعريف إخطار البريد الإلكتروني في Microsoft Dynamics 365 Commerce.

عند إنشاء القنوات، يمكنك إعداد ملف تعريف الإخطار بالبريد الكتروني. يقوم ملف تعريف الإعلام بالبريد الإلكتروني بتعريف أحداث حركة المبيعات (مثل أحداث الأمر الذي تم إنشاؤه وتعبئته وفوترته) والتي ستُرسل إخطارات تتعلق بها إلى عملائك. 

للحصول على مزيد من المعلومات حول تكوين البريد الإلكتروني، راجع [تكوين البريد الإلكتروني وإرساله](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).



## <a name="create-an-email-template"></a>إنشاء قالب بريد إلكتروني

قبل تمكين نوع الإخطار بالبريد الإلكتروني، يجب إنشاء قالب بريد الكتروني للمؤسسة في المركز الرئيسي لـ Commerce لكل نوع إخطار تريد دعمه. يحدد هذا القالب موضوع البريد الإلكتروني والمرسل واللغة الافتراضية ونص البريد الإلكتروني لكل لغة مدعومة.

لإنشاء قالب بريد إلكتروني، اتبع هذه الخطوات.

1. في جزء التنقل، انتقل إلى **الوحدات النمطية \> Retail وCommerce \> إعداد المراكز الرئيسية \> المعلمات \> قوالب البريد الإلكتروني للمؤسسة**.
1. في جزء الإجراءات، حدد **جديد**.
1. في الحقل **معرف البريد الإلكتروني**، أدخل معرفًا للمساعدة في تعريف هذا القالب.
1. في حقل **اسم المرسل**، أدخل اسم المرسل‏‎.
1. في **وصف البريد الإلكتروني**، أدخل وصفًا هادفًا.
1. في **‏‫البريد الإلكتروني للمرسل‬** ، أدخل عنوان البريد الإلكتروني للمرسل.
1. في القسم **عام**، حدد اللغة الافتراضية لقالب البريد الإلكتروني. سيتم استخدام اللغة الافتراضية في حالة عدم وجود أي قالب مترجم خاص باللغة المحددة.
1. وسَّع قسم **محتوى رسالة البريد الإلكتروني** وحدد **جديد** لإنشاء محتوى القالب. بالنسبة لكل عنصر محتوى، حدد اللغة وأدخل سطر موضوع البريد الإلكتروني. إذا كان البريد الإلكتروني يحتوي على نص، تأكد من تحديد خانة **‏‫يتضمن نص‬**.
1. في جزء الإجراءات، حدد **رسالة بريد إلكتروني** لتوفير قالب نص البريد الإلكتروني.

توضح الصورة التالية بعض أمثلة لإعدادات قالب البريد الإلكتروني.

![إعدادات قالب البريد الإلكتروني.](media/email-template.png)

للحصول على المزيد من المعلومات حول كيفية إنشاء قوالب البريد الكتروني وتحميلها، راجع [إنشاء قوالب بريد إلكتروني لأحداث الحركات](email-templates-transactions.md). 

## <a name="create-an-email-notification-profile"></a>إنشاء ملف تعريف إخطار البريد الإلكتروني

لإنشاء ملف تعريف إعلام بالبريد الإلكتروني في المقر الرئيسي ، اتبع هذه الخطوات.

1. في جزء التنقل، انتقل إلى **الوحدات النمطية \> Retail وcommerce \> إعداد Headquarters \> ملف تعريف إخطار البريد الإلكتروني لـ Commerce**‬.
1. في جزء الإجراءات، حدد **جديد**.
1. في الحقل **ملف تعريف إخطار البريد الإلكتروني**، أدخل اسمًا لتحديد ملف التعريف.
1. في حقل **الوصف**، أدخل وصفًا ذا صلة.
1. عيِّن المفتاح **نشط** على القيمة **نعم**.

## <a name="add-a-notification-type"></a>أضف نوع الإخطار

لإنشاء حدث بالبريد الإلكتروني، اتبع هذه الخطوات.

1. في جزء التنقل، انتقل إلى **الوحدات النمطية \> Retail وcommerce \> إعداد Headquarters \> ملف تعريف إخطار البريد الإلكتروني لـ Commerce**‬.
1. تحت **إعدادات** اعلام البريد الكتروني للبيع بالتجزئة ، حدد **جديد**.
1. حدد **نوع إخطار البريد الإلكتروني** المناسب من القائمة المنسدلة.
1. حدد قالب البريد الكتروني الذي قمت بإنشاءه أعلاه من القائمة المنسدلة لمعرف **البريد الكتروني**.
1. حدد خانة الاختيار **نشط**.
1. في جزء الإجراءات، حدد **حفظ**.

توضح الصورة التالية بعض أمثلة لإعدادات إخطار حدث.

![إعدادات الإخطار بالحدث.](media/email-notification-profile.png)


## <a name="schedule-a-recurring-email-notification-process-job"></a>جدولة وظيفة عملية إخطار بالبريد الإلكتروني مكررة

لإرسال إعلامات بالبريد الكتروني، يجب أن تكون الوظيفة **معالجة إخطار البريد الإلكتروني للبيع بالتجزئة‬** قيد التشغيل.

لإعداد مهمة مجموعه في المركز لإرسال رسائل بريد الكتروني للمعاملات ، اتبع الخطوات التالية.

1. انتقل إلى **Retail وCommerce \> تكنولوجيا المعلومات لـ Retail وCommerce \> البريد الإلكتروني والإخطارات \> إرسال إخطار بالبريد الإلكتروني**.
1. في مربع الحوار **معالجة إخطار البريد الإلكتروني للبيع بالتجزئة**، حدد **تكرار**.
1. حدد **بلا تاريخ انتهاء** في مربع الحوار **تحديد التكرار**.
1. ضمن **نمط التكرار**، حدد **دقائق**، ثم قم بتعيين الحقل **تعداد** إلى **1**. ستضمن هذه الإعدادات معالجة الإخطارات بالبريد الإلكتروني في أسرع وقت ممكن.
1. حدد **موافق** للعودة إلى مربع الحوار **معالجة إخطار البريد الإلكتروني للبيع بالتجزئة**.
1. حدد **موافق** لإكمال إعداد الوظيفة.

## <a name="next-steps"></a>الخطوات التالية

قبل أن تتمكن من إرسال رسائل البريد الإلكتروني، يجب عليك تكوين خدمة البريد الصادر. لمزيد من المعلومات، راجع [تكوين البريد الإلكتروني وإرساله](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).

## <a name="additional-resources"></a>الموارد الإضافية

[تكوين وإرسال البريد الإلكتروني](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[نظره عامة حول القنوات](channels-overview.md)

[المتطلبات الأساسية‬ لإعداد قناة](channels-prerequisites.md)

[نظرة عامة المؤسسات والتدرجات الهرمية للمؤسسات](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
