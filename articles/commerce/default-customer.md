---
title: إنشاء عميل افتراضي
description: يوضح هذا المقال كيفية إنشاء عميل افتراضي لاستخدامه عند إنشاء قناة في Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 79e145c21be9178622b7c105afefecb78062e3b5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273575"
---
# <a name="create-a-default-customer"></a>إنشاء عميل افتراضي

[!include [banner](includes/banner.md)]

يوضح هذا المقال كيفية إنشاء عميل افتراضي لاستخدامه عند إنشاء قناة في Microsoft Dynamics 365 Commerce.

عند إنشاء قناة، ستحتاج إلى توفير عميل افتراضي. يمكن إنشاء عميلاً افتراضيًا بسهولة بعد إنشاء مجموعة العميل ودفتر عناوين العميل أولاً.

## <a name="create-a-customer-group"></a>إنشاء مجموعة عميل

في حالة عدم وجود أي مجموعات للعملاء بعد، يمكنك إنشاء واحدة. قد تكون الأمثلة مجموعات لتمثيل مجموعات عملاء مختلفة، مثل البيع بالجملة والبيع بالتجزئة والإنترنت والموظفين وما إلى ذلك.

لإنشاء مجموعة عميل، اتبع الخطوات التالية.

1. في جزء التنقل، انتقل إلى **الوحدات النمطية \> البيع بالتجزئة والتجارة \> العملاء \> مجموعات العملاء**.
1. في جزء الإجراءات، حدد **جديد**.
1. في المربع **مجموعة العميل**، أدخل معرف مجموعة العميل.
1. في مربع **الوصف**، أدخل وصفًا مناسبًا.
1. في مربع **شروط الدفع**، أدخل قيمة مناسبة.
1. في مربع **‏‫الوقت بين تاريخ استحقاق الفاتورة وتاريخ الدفع‬**، أدخل قيمة مناسبة.
1. في مربع **مجموعة الضريبة الافتراضية**، أدخل مجموعة ضريبة إن وجدت.
1. حدد خانة الاختيار **الأسعار شاملة ضريبة المبيعات** إن وجدت.
1. في المربع **‏‫سبب الإلغاء الافتراضي‬**، أدخل قيمة مناسبة إن وجد.

تعرض الصورة التالية العديد من مجموعات العملاء التي تم تكوينها.

![مجموعات العملاء.](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a>إنشاء دفتر عناوين للعميل.

يجب إقران العميل بدفتر عناوين. إذا لم يتم إنشاء دفتر عناوين بعد، ستحتاج إلى إنشاء واحدًا.

لإنشاء دفتر عناوين عميل، اتبع الخطوات التالية.

1. في جزء التنقل، انتقل إلى **الوحدات النمطية \> البيع بالتجزئة والتجارة \> إعداد القناة \> دفاتر العناوين**.
1. في جزء الإجراءات، حدد **جديد**.
1. في حقل **الاسم**، أدخل اسمًا.
1. في مربع **الوصف**، أدخل وصفًا.
1. في جزء الإجراءات، حدد **حفظ**.

تعرض الصورة التالية مثالاً لدفتر عناوين.

![دفتر العناوين.](media/address-book.png)

## <a name="create-a-default-customer"></a>إنشاء عميل افتراضي

لإنشاء عميل افتراضي، اتبع الخطوات التالية.

1. في جزء التنقل، انتقل إلى **الوحدات النمطية \> البيع بالتجزئة والتجارة \> العملاء \> كل العملاء**.
1. في جزء الإجراءات، حدد **جديد**.
1. من القائمة المنسدلة **النوع** حدد "شخص".
1. في القائمة المنسدلة **حساب العميل**، حدد رقم حساب أو أدخله (على سبيل المثال، "100001").
1. في القائمة المنسدلة **الاسم الأول**، حدد اسمًا أو أدخله (على سبيل المثال، "الافتراضي").
1. في القائمة المنسدلة **الاسم الأوسط**، حدد اسمًا أو أدخله (على سبيل المثال، "البيع بالتجزئة").
1. في القائمة المنسدلة **الاسم الأخير**، حدد اسمًا أو أدخله (على سبيل المثال، "العميل").
1. في القائمة المنسدلة **العملة**، حدد عملة أو أدخلها (على سبيل المثال، "دولار أمريكي").
1. في القائمة المنسدلة **العملة**، حدد مجموعة العملاء التي تم إنشاؤها مسبقًا.
1. في القائمة المنسدلة **دفاتر العناوين**، حدد دفتر عناوين عميل موجود.
1. حدد **حفظ** للحفظ والرجوع إلى شاشة تفاصيل العميل للعميل الجديد.

> [!NOTE]
> ليس من الضروري إضافة عنوان لعميل افتراضي.

تعرض الصورة التالية مثالاً لإنشاء عميل.

![إنشاء عميل افتراضي.](media/default-customer-creation.png)

تظهر الصورة التالية تكوين عميل افتراضي.

![عينة تكوين عميل.](media/default-customer-configuration1.png)

يمكن أن تبقى معظم القيم الافتراضية على شاشة تفاصيل العميل، ولكن يجب تغيير قيمتين.

1. من شاشة تفاصيل العميل، وسَّع **إعدادات أوامر المبيعات الافتراضية**.
1. من القائمة المنسدلة **الموقع**، حدد موقعًا تم تكوينه مسبقًا أو أدخله.
1. في القائمة المنسدلة **المستودع**، حدد مستودعًا تم تكوينه مسبقًا أو أدخله.

تعرض الصورة التالية مثالاً لتكوين عميل.

![مثال تكوين عميل.](media/default-customer-configuration2.png)

## <a name="additional-resources"></a>الموارد الإضافية

[نظره عامة حول القنوات](channels-overview.md)

[المتطلبات الأساسية لإعداد القناة](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
