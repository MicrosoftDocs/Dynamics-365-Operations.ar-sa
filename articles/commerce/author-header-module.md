---
title: وحدة الرأس
description: يتناول هذا المقال وحدات الرأس ويصف كيفية إنشاء رؤوس الصفحات في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 63c298f36f64f2e107d3df3c0c5f3b6445546aa1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275775"
---
# <a name="header-module"></a>وحدة الرأس

[!include [banner](includes/banner.md)]

يتناول هذا المقال وحدات الرأس ويصف كيفية إنشاء رؤوس الصفحات في Microsoft Dynamics 365 Commerce.

في Dynamics 365 Commerce، يتم تكوين رأس الصفحة كجزء صفحة يتضمن الوحدات النمطية للرأس والشعار الترويجي والموافقة على ملفات تعريف الارتباط‬. 

تتضمن وحدة الرأس شعار الموقع وارتباطات إلى التدرج الهرمي للتنقل وارتباطات إلى صفحات أخرى في الموقع ووحدة نمطية لأيقونة سلة التسوق ورمز قائمة الأمنيات وخيارات تسجيل الدخول وشريط البحث. يتم تحسين وحدة الرأس بشكل تلقائي للجهاز الذي يتم عرض الموقع عليه (بمعنىً آخر لجهاز سطح المكتب أو جهاز محمول). على سبيل المثال، على جهاز المحمول، يتم طي شريط التنقل إلى زر **القائمة** (والذي يُشار إليه أحيانًا بـ *قائمة هامبورجير*).

تعرض الصورة التالية مثالاً عن وحدة الرأس في صفحة رئيسية.

![مثال عن وحدة رأس.](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a>خصائص وحدة الرأس

تدعم وحدة الرأس خصائص **صورة الشعار** و **ارتباط الشعار** و **ارتباطات حسابي**. 

تُستخدم خصائص **صورة الشعار** و **ارتباط الشعار** لتعريف شعار على الصفحة. لمزيد من المعلومات، راجع [إضافة شعار](add-logo.md). 

يمكن استخدام الخاصية **ارتباطات حسابي** لتحديد صفحات الحساب التي يريد مالك الموقع عرض ارتباطات سريعة لها في الرأس.

## <a name="modules-that-are-available-within-a-header-module"></a>الوحدات النمطية المتوفرة في الوحدة النمطية للرأس

يُمكن استخدام الوحدات النمطية في الوحدة النمطية للعنوان:

- **قائمة التنقل** – تمثل قائمة التنقل التدرج الهرمي للتنقل في القناة وغيرها من ارتباطات التنقل الثابتة. لمزيد من المعلومات، راجع [الوحدة النمطية لقائمة التنقل](nav-menu-module.md).

- **بحث** – تسمح وحدة البحث للمستخدمين بإدخال مصطلحات البحث للبحث عن المنتجات. يجب توفير عنوان URL لصفحة البحث الافتراضية ومحددات استعلام البحث في **إعدادات الموقع \> الملحقات**. تتضمن وحدة البحث خصائص تتيح لك منع زر البحث أو التسمية كما هو مطلوب. وتدعم أيضًا وحدة البحث خيارات الاقتراح التلقائي، مثل نتائج البحث عن منتج وكلمة أساسية وفئة.

- **أيقونة سلة التسوق** - تمثل وحدة أيقونة سلة التسوق أيقونة سلة التسوق، التي تعرض عدد الأصناف في سلة التسوق في أي وقت محدد. لمزيد من المعلومات، راجع‏‎ [وحدة أيقونة سلة التسوق](cart-icon-module.md).

- **محدد الموقع** - تتيح الوحدة النمطية لمحدد الموقع للمستخدمين استعراض المواقع المختلفة المعرفة مسبقًا، استنادًا إلى السوق والمناطق والإعدادات المحلية. لمزيد من المعلومات، راجع‏‎ [الوحدة النمطية لمحدد الموقع](site-selector.md).

- **محدد المتجر** - يمكن تضمين الوحدة النمطية لمحدد المتجر في فتحة محدد المتجر الخاصة بالوحدة النمطية لرأس. تتيح للمستخدمين استعراض المتاجر القريبة والبحث عنها. كما يمكن للمستخدمين تحديد المتجر المفضل. سيتم بعد ذلك إظهار ذلك المتجر في الرأس. عند تضمين الوحدة النمطية لمحدد المتجر في الوحدة النمطية للرأس، فإنه يجب تعيين الخاصية **وضع** على **البحث عن المتاجر**. لمزيد من المعلومات، راجع‏‎ [الوحدة النمطية لمحدد المتجر](store-selector.md).

> [!NOTE]
> - يتوفر دعم استخدام الوحدة النمطية لأيقونة سلة التسوق في الوحدات النمطية للرأس اعتبارًا من الإصدار 10.0.11 من Dynamics 365 Commerce.
> - يتوفر دعم استخدام الوحدة النمطية لمحدد الموقع في الوحدات النمطية للرأس اعتبارًا من الإصدار 10.0.14 من Dynamics 365 Commerce.
> - يتوفر دعم استخدام الوحدة النمطية لمحدد المتجر في الوحدات النمطية للرأس اعتبارًا من الإصدار 10.0.15 من Dynamics 365 Commerce.

## <a name="header-module-in-the-adventure-works-theme"></a>الوحدة النمطية للرأس في نسق Adventure Works

في نسق Adventure Works، دعم الوحدة النمطية للرأس خاصة **شعار الجهاز المحمول**. تمكن هذه الخاصية من تحديد شعار لمنافذ العرض الخاصة بالأجهزة المحمولة. تتوفر خاصية **شعار الأجهزة المحمولة** كملحق تعريف للوحدة النمطية.

> [!IMPORTANT]
> ويتوفر نسق Adventure Works اعتباراً من الإصدار 10.0.20 من Dynamics 365 Commerce.

## <a name="create-a-header-fragment-for-a-page"></a>إنشاء جزء رأس لصفحة

لإنشاء جزء رأس، اتبع هذه الخطوات.

1. انتقل إلى **الأجزاء**، ثم حدد **جديد** لإنشاء جزء جديد.
1. في مربع الحوار **تحديد جزء**، حدد وحدة **الحاوية**، وأدخل اسمًا للجزء، ثم حدد **موافق**.
1. حدد فتحة **الحاوية الافتراضية**، ثم في جزء الخصائص الموجود إلى اليمين، قم بتعيين خاصية **العرض** إلى **ملء الشاشة‬‏‫**.
1. في فتحة **الحاوية الافتراضية‬‬‏‫**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.
1. في مربع الحوار **تحديد وحدات**، حدد الوحدات النمطية **الموافقة على ملفات تعريف الارتباط** و **الرأس** و **الشعار الترويجي**، ثم حدد **موافق**.
1. في جزء الخصائص في الوحدة النمطية **الشعار الترويجي**، حدد **إضافة رسالة**، ثم حدد **الرسالة**.
1. في مربع الحوار **الرسالة**، أضف النص والارتباطات للمحتوى الترويجي، ثم حدد **موافق**.
1. في جزء الخصائص في الوحدة النمطية **الموافقة على ملفات تعريف الارتباط**، أضف وكوّن نصًا وارتباطًا إلى صفحة خصوصية الموقع.
1. في فتحة **قائمة التنقل** لوحدة الرأس، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.
1. في مربع الحوار **تحديد وحدات**، حدد وحدة **قائمة التنقل**، ثم حدد **موافق**.
1. في جزء الخصائص في الوحدة النمطية لقائمة التنقل، ضمن **المصدر لقائمة التنقل**، حدد **Retail Server**.
1. في جزء الخصائص في الوحدة النمطية لقائمة التنقل، ضمن **عناصر القائمة الثابتة**، حدد **إضافة عنصر قائمة**، ثم حدد **عنصر قائمة**. 
1. في مربع الحوار **عنصر القائمة**، ضمن **نص عنصر القائمة**، أدخل "جهة اتصال".
1. في مربع الحوار **عنصر القائمة**، ضمن **هدف ارتباط عنصر القائمة**، حدد **إضافة ارتباط**.
1. في مربع الحوار **إضافة ارتباط** ،حدد عنوان URL لصفحة "جهة الاتصال" في الموقع، ثم حدد **موافق**.  
1. في مربع الحوار **عنصر القائمة‬‏‫** حدد **موافق**.
1. في فتحة **البحث** لوحدة الرأس، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.
1. في مربع الحوار **تحديد وحدات**، حدد وحدة **البحث‬‏‎**، ثم حدد **موافق**.
1. في جزء الخصائص لوحدة البحث، قم بتكوين الخصائص وفق الحاجة.
1. في فتحة **أيقونة سلة التسوق** لوحدة الرأس، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.
1. في مربع الحوار **تحديد وحدات**، حدد وحدة **أيقونة سلة التسوق‬‏‎**، ثم حدد **موافق**.
1. في جزء الخصائص لوحدة أيقونة سلة التسوق، قم بتكوين الخصائص وفق الحاجة. إذا أردت أن تعرض أيقونة سلة التسوق ملخصًا لسلة التسوق (تُعرف أيضًا بسلة التسوق الصغيرة) عند قيام المستخدم بتمرير الماوس فوقها، فحدد **إظهار سلة التسوق الصغيرة**.
1. حدد **حفظ**، وحدد **إنهاء التحرير** لإيداع الجزء، ثم حدد **نشر** لنشره.

للمساعدة في ضمان ظهور الرأس في كل صفحة، اتبع هذه الخطوات في كل قالب صفحة تم إنشاؤه للموقع.

1. في فتحة **الرأس** في وحدة **الصفحة الافتراضية**، أضف جزء التذييل الذي قمت بإنشائه.
1. حدد **حفظ**، وحدد **إنهاء التحرير** لإيداع القالب، ثم حدد **نشر** لنشره.

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة حول مكتبة الوحدات النمطية](starter-kit-overview.md)

[وحدة الحاوية](add-container-module.md)

[الوحدة النمطية لرمز عربة التسوق](cart-icon-module.md)

[وحدة الشعار الترويجي](add-alert.md)

[الوحدة النمطية لقائمة التنقل](nav-menu-module.md) 

[الموافقة على ملف تعريف الارتباط](cookie-consent-module.md)

[وحدة التذييلات‬](author-footer-module.md)

[الوحدة النمطية لمحدد الموقع](site-selector.md)

[الوحدة النمطية لمحدد المتجر](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
