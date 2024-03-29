---
title: إضافة تعليمات برمجية لبرنامج نصي إلى صفحات الموقع لدعم تتبع الاستخدام
description: يصف هذا المقال كيفيه إضافة التعليمات البرمجية لبرنامج نصي من جانب العميل إلى صفحات موقعك لدعم مجموعة تتبع الاستخدام من جانب العميل.
author: bicyclingfool
ms.date: 09/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: a0a5103d239c7f93ad6888a2eaf56d1cac32bd58
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282262"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a>إضافة تعليمات برمجية لبرنامج نصي إلى صفحات الموقع لدعم تتبع الاستخدام

[!include [banner](includes/banner.md)]

يصف هذا المقال كيفيه إضافة التعليمات البرمجية لبرنامج نصي من جانب العميل إلى صفحات موقعك لدعم مجموعة تتبع الاستخدام من جانب العميل.

تُعد تحليلات الويب أداة أساسية عندما ترغب في فهم كيفية تفاعل عملائك مع موقعك واتخاذ قرارات من شأنها أن تساعد في تحسين التجربة لتحقيق أقصى قدر من التحويل. تتوفر العديد من حزم تحليلات الويب لمساعدتك في تحقيق هذه الأهداف، مثل Google Analytics وClicky وMoz Analytics وKISSMetrics. تتطلب معظم حزم تحليلات الويب أن تضيف التعليمات البرمجية لبرنامج نصي في عنصر **\<head\>** من HTML لجميع صفحات موقعك.

> [!NOTE]
> تنطبق الإرشادات الواردة في هذا المقال أيضًا على الوظائف المخصصة الأخرى من جانب العميل التي لا يوفرها Microsoft Dynamics 365 Commerce.

## <a name="create-a-reusable-fragment-for-your-script-code"></a>إنشاء جزء قابل لإعادة الاستخدام للتعليمات البرمجية لبرنامج نصي

يتيح لك الجزء إعادة استخدام التعليمات البرمجية المضمنة أو الخارجية في كافة صفحات موقعك، بغض النظر عن القالب الذي تستخدمه.

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a>إنشاء جزء قابل لإعادة الاستخدام للتعليمات البرمجية لبرنامج نصي مضمن

لإنشاء جزء قابل لإعادة الاستخدام للتعليمات البرمجية للنص المضمن في منشئ المواقع، اتبع الخطوات التالية.

1. انتقل إلى **الأجزاء**، ثم حدد **جديد**.
1. في مربع الحوار **جزء جديد**، حدد **البرنامج النصي المضمن**.
1. ضمن **اسم الجزء**، أدخل اسمًا لهذا الجزء، ثم حدد **موافق**.
1. ضمن الجزء الذي قمت بإنشائه، حدد الوحدة **البرنامج النصي الافتراضي المضمن**.
1. في جزء الخصائص الموجود على الجانب الأيمن، ضمن **البرنامج النصي المضمن**، أدخل البرنامج النصي من جانب العميل. قم بعد ذلك بتكوين الخيارات الأخرى كما تتطلب.
1. حدد **حفظ**، ثم قم بتحديد **إنهاء التحرير**.
1. حدد **نشر**.

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a>إنشاء جزء قابل لإعادة الاستخدام للتعليمات البرمجية لبرنامج نصي خارجي

لإنشاء جزء قابل لإعادة الاستخدام للتعليمات البرمجية للبرنامج النصي الخارجي في منشئ المواقع، اتبع الخطوات التالية.

1. انتقل إلى **الأجزاء**، ثم حدد **جديد**.
1. في مربع الحوار **جزء جديد**، حدد **البرنامج النصي الخارجي**.
1. ضمن **اسم الجزء**، أدخل اسمًا لهذا الجزء، ثم حدد **موافق**.
1. ضمن الجزء الذي قمت بإنشائه، حدد الوحدة **البرنامج النصي الافتراضي الخارجي**.
1. في جزء الخصائص الموجود على الجانب الأيمن، ضمن **مصدر البرنامج النصي**، أضف عنوان URL خارجيًا أو ذي صلة لمصدر البرنامج النصي الخارجي. قم بعد ذلك بتكوين الخيارات الأخرى كما تتطلب.
1. حدد **حفظ**، ثم قم بتحديد **إنهاء التحرير**.
1. حدد **نشر**.

> [!NOTE]
> إذا تم تمكين نهج أمان المحتوي (CSP) للموقع الخاص بك، فتاكد من أضافه كافة عناوين URL الخارجية إلى توجيه CSP **مصدر النص البرمجي** في أداة إنشاء موقع Commerce. لمزيد من المعلومات، راجع [إدارة سياسة أمان المحتوى (CSP)](manage-csp.md).

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a>أضف جزء يحتوي على التعليمات البرمجية للبرنامج النصي إلى قالب

لإضافة جزء يتضمن التعليمات البرمجية للبرنامج النصي إلى قالب في منشئ المواقع، اتبع الخطوات التالية.

1. انتقل إلى **القوالب**، وافتح القالب الخاص بالصفحات التي تريد إضافة التعليمات البرمجية لبرنامج نصي اليها.
1. في الجزء الأيسر، قم بتوسيع التدرج الهرمي للقالب لإظهار فتحة **عنوان HTML** .
1. في فتحة **رأس HTML‬‏‫**، حدد زر علامة القطع (**...**)، ثم حدد **إضافة جزء**.
1. حدد الجزء الذي قمت بإنشاءه للتعليمات البرمجية لبرنامجك النصي.
1. حدد **حفظ**، ثم قم بتحديد **إنهاء التحرير**.
1. حدد **نشر**.

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a>إضافة برنامج نصي خارجي أو برنامج نصي مضمن مباشرةً إلى قالب

إذا كنت ترغب في إدراج برنامج نصي مضمن أو خارجي مباشرةً في مجموعة من الصفحات التي يتم التحكم فيها بواسطة قالب واحد، فلن تحتاج إلى إنشاء جزء أولاً.

### <a name="add-an-inline-script-directly-to-a-template"></a>إضافة برنامج نصي مضمن مباشرةً إلى قالب

لإضافة برنامج نصي مضمن مباشرةً إلى قالب في منشئ الموقع، اتبع الخطوات التالية.

1. انتقل إلى **القوالب**، وافتح القالب الخاص بالصفحات التي تريد إضافة التعليمات البرمجية لبرنامج نصي اليها.
1. في الجزء الأيسر، قم بتوسيع التدرج الهرمي للقالب لإظهار فتحة **عنوان HTML** .
1. في فتحة **عنوان HTML‬‏‫**، وحدد علامة الحذف (**...**)، ثم حدد **إضافة وحدة**.
1. في مربع الحوار **إضافة وحدة**، حدد **البرنامج النصي المضمن**.
1. في جزء الخصائص الموجود على الجانب الأيمن، ضمن **البرنامج النصي المضمن**، أدخل البرنامج النصي من جانب العميل. قم بعد ذلك بتكوين الخيارات الأخرى كما تتطلب.
1. حدد **حفظ**، ثم قم بتحديد **إنهاء التحرير**.
1. حدد **نشر**.

### <a name="add-an-external-script-directly-to-a-template"></a>إضافة برنامج نصي خارجي مباشرةً إلى قالب

لإضافة برنامج نصي خارجي مباشرةً إلى قالب في منشئ الموقع، اتبع الخطوات التالية.

1. انتقل إلى **القوالب**، وافتح القالب الخاص بالصفحات التي تريد إضافة التعليمات البرمجية لبرنامج نصي اليها.
1. في الجزء الأيسر، قم بتوسيع التدرج الهرمي للقالب لإظهار فتحة **عنوان HTML** .
1. في فتحة **عنوان HTML‬‏‫**، وحدد علامة الحذف (**...**)، ثم حدد **إضافة وحدة**.
1. في مربع الحوار **إضافة وحدة**، حدد **البرنامج النصي الخارجي**.
1. في جزء الخصائص الموجود على الجانب الأيمن، ضمن **مصدر البرنامج النصي**، أضف عنوان URL خارجيًا أو ذي صلة لمصدر البرنامج النصي الخارجي. قم بعد ذلك بتكوين الخيارات الأخرى كما تتطلب.
1. حدد **حفظ**، ثم قم بتحديد **إنهاء التحرير**.
1. حدد **نشر**.

## <a name="additional-resources"></a>الموارد الإضافية

[إضافة شعار](add-logo.md)

[تحديد سمة الموقع](select-site-theme.md)

[العمل CSS مع ملفات التجاوز](css-override-files.md)

[إضافة أيقونة المفضلة](add-favicon.md)

[إضافة إشعار لحقوق النشر](add-copyright-notice.md)

[إضافة لغات إلى الموقع الخاص بك](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
