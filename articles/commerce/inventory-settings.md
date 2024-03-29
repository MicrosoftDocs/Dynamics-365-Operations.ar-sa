---
title: تطبيق إعدادات المخزون
description: يتناول هذا المقال إعدادات المخزون ويصف كيفية تطبيقها في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 08/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 49310a44f8b9c636734e04d4eed9445384b55791
ms.sourcegitcommit: 1d5cebea3e05b6d758cd01225ae7f566e05698d2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/02/2022
ms.locfileid: "9405310"
---
# <a name="apply-inventory-settings"></a>تطبيق إعدادات المخزون

[!include [banner](includes/banner.md)]

يتناول هذا المقال إعدادات المخزون ويصف كيفية تطبيقها في Microsoft Dynamics 365 Commerce.

تحدد إعدادات المخزون ما إذا كان ينبغي فحص المخزون قبل إضافة المنتجات إلى سلة التسوق. وهي تحدد أيضًا رسائل ترويج البضائع المرتبطة بالمخزون، مثل "في المخزون" و "بقي عدد قليل فقط." وتضمن هذه الإعدادات عدم إمكانية شراء منتج عندما ينفد من المخزون.

يوفر Dynamics 365 Commerce تقديرات عن التوفر الفعلي للمنتجات. للحصول على معلومات حول كيفية حساب التوفر الفعلي، راجع [حساب توفر المخزون لقنوات البيع بالتجزئة](calculated-inventory-retail-channels.md).

في منشئ الموقع في Commerce، يمكن تعريف حدود ونطاقات المخزون لمنتج أو فئة. وهي تحدد ما إذا كان من الممكن تصنيف المخزون في حالة "في المخزون" أو "نفد من المخزون" أو "مخزون قليل". للاطلاع على التفاصيل، راجع [تكوين المخازن المؤقتة للمخزون ومستويات المخزون](inventory-buffers-levels.md).

> [!NOTE]
> يتوفر دعم حدود ونطاقات في Dynamics 365 Commerce الإصدار 10.0.12.

## <a name="inventory-settings"></a>إعدادات المخزون

في Commerce، يتم تعريف إعدادات المخزون في **إعدادات الموقع \> الملحقات \> إدارة المخزون** في منشئ الموقع. هناك ستة إعدادات للمخزون، أحدها أصبح قديمًا ومهملاً:

- **تمكين فحص المخزون على التطبيق** – يقوم هذا الإعداد بتشغيل فحص مخزون المنتج. ستقوم عندئذٍ الوحدات‬ النمطية لصندوق الشراء‬ وسلة التسوق والانتقاء في المتجر‬ الصندوق بفحص مخزون المنتجات، وستسمح بإضافة منتج إلى سلة التسوق فقط إذا توفر المخزون.
- **مستوى المخزون استنادًا إلى** – يحدد هذا الإعداد كيفية حساب مستويات المخزون. القيم المتوفرة هي **الإجمالي المتوفر** و **الفعلي المتوفر** و **حد النفاد من المخزون**. في Commerce، يمكن تعريف حدود ونطاقات المخزون لكل منتج أو فئة. تقوم واجهات API للمخزون بإرجاع معلومات عن مخزون المنتج للخاصيتين **الإجمالي المتوفر** و **الفعلي المتوفر**. يقرر بائع التجزئة ما إذا كان يجب استخدام قيمة **الإجمالي المتوفر** و **الفعلي المتوفر** لتحديد جرد المخزون والنطاقات المناظر للحالتين "في المخزون" و"نفد من المخزون".

    قيمة **حد النفاد من المخزون** لإعداد **مستوى المخزون استنادًا إلى** هي قيمة قديمة ومهمة. عند تحديد هذه القيمة، يتم تحديد جرد المخزون من نتائج قيمة **الإجمالي المتوفر**، ولكن يتم تعريف الحد بواسطة الإعداد الرقمي **حد النفاد من المخزون** الذي سيرد وصفه لاحقًا. ينطبق إعداد الحد هذا على كافة المنتجات في موقع تجارة إلكترونية. إذا كان المخزون أقل من رقم الحد، فسيُعتبر المنتج على أنه نفد من المخزون. بخلاف ذلك، سيُعتبر على أنه في المخزون. تعتبر قدرات قيمة **حد النفاد من المخزون** محدودة، ولا ننصح باستخدامها في الإصدار 10.0.12 والإصدارات اللاحقة.

- **مستوى المخزون لمستودعات متعددة** – يتيح هذا الإعداد حساب مستوى المخزون مقابل المستودع الافتراضي أو المستودعات المتعددة. سيحسب خيار **على أساس المستودع الفردي** مستويات المخزون على أساس المستودع الافتراضي. بدلاً من ذلك، يمكن أن يشير موقع التجارة الإلكترونية إلى مستودعات متعددة لتسهيل التنفيذ. في هذه الحالة، يتم استخدام خيار **على أساس التجميع لمخازن الشحن والاستلام** للإشارة إلى توافر المخزون. على سبيل المثال، عندما يشتري أحد العملاء صنفًا ويحدد "الشحن" كوضع التسليم، يمكن شحن الصنف من أي مستودع في مجموعة التنفيذ التي تحتوي على مخزون متاح. ستعرض صفحة تفاصيل المنتج (PDP) رسالة "متوفر" للشحن إذا كان هناك مخزون في أي مستودع شحن متوفر في مجموعة التنفيذ. 

    > [!IMPORTANT] 
    > يتوفر إعداد **مستوى المخزون لمستودعات متعددة** اعتبارًا من إصدار Commerce رقم 10.0.19. إذا كنت تقوم بالتحديث من إصدار قديم من Commerce، فيجب عليك تحديث ملف appsettings.json يدويًا. للاطلاع على التعليمات، راجع [تحديثات مكتبة الوحدات وSDK](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

- **إعدادات المخزون لصفحات قوائم المنتجات** -يحدد هذا الاعداد كيفيه عرض المنتجات خارج المخزون في قوائم المنتجات التي يتم تقديمها بواسطة مجموعه المنتجات والوحدات النمطية لنتائج البحث. يتم **عرض القيم المتوفرة بالترتيب مع المنتجات الأخرى**، و **إخفاء منتجات المخزون من القائمة** ، و **عرض منتجات خارج المخزون في نهاية القائمة**. لاستخدام هذا الاعداد ، يجب تكوين بعض الإعدادات الاساسيه أولا في الاداره التجارية. لمزيد من المعلومات، راجع [قائمة المنتجات المدركة للمخزون](inventory-aware-product-listing.md).

    > [!IMPORTANT] 
    > يتوفر إعداد **إعدادات المخزون لصفحات قائمة المنتجات** اعتبارًا من إصدار Commerce رقم 10.0.20. إذا كنت تقوم بالتحديث من إصدار قديم من Commerce، فيجب عليك تحديث ملف appsettings.json يدويًا. للاطلاع على التعليمات، راجع [تحديثات مكتبة الوحدات وSDK](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

- **نطاقات المخزون** – يحدد هذا الإعداد رسائل نطاق المخزون التي يتم عرضها في وحدات الموقع. ينطبق هذا الإعداد فقط عندما تكون قيمة **الإجمالي المتوفر** أو قيمة **الفعلي المتوفر** محددة للإعداد **مستوى المخزون استنادًا إلى‬‏‫**. القيم المتوفرة هي **الكل** و **مخزون قليل ونفد من المخزون** و **نفد من المخزون**.

    - عند تحديد **الكل**، ستظهر رسائل لجميع نطاقات المخزون، من الحالة "في المخزون" (الرسالة "متوفر") إلى "نفد من المخزون" (الرسالة "نفد من المخزون").
    - عند تحديد **مخزون قليل ونفد من المخزون‬‏‫**، ستظهر رسائل لجميع نطاقات المخزون باستثناء الحالة "في المخزون" (الرسالة "متوفر").
    - عند تحديد **نفد من المخزون**، ستظهر الرسالة "نفد من المخزون" فقط.

- **حد النفاد من المخزون** – سيصبح الإعداد الرقمي القديم ساري المفعول فقط عند تحديد قيمة **حد النفاد من المخزون** للإعداد **مستوى المخزون استنادًا إلى**.

> [!IMPORTANT] 
> تتوفر هذه الإعدادات في Dynamics 365 Commerce الإصدار 10.0.12. إذا كنت تقوم بالتحديث من إصدار قديم من Dynamics 365 Commerce، فيجب عليك تحديث ملف appsettings.json يدويًا. للحصول على تعليمات حول تحديث ملف appsettings.json، راجع [تحديثات SDK ومكتبة الوحدات النمطية](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="modules-that-use-inventory-settings"></a>الوحدات النمطية التي تستخدم إعدادات المخزون

تستخدم الوحدات النمطية صندوق الشراء وقائمة الأمنيات وسلة التسوق وأيقونة سلة التسوق إعدادات المخزون لإظهار نطاقات المخزون ورسائله.

في المثال الموضح في الرسم التوضيحي التالي، تعرض PDP رسالة في المخزن ("متوفرة").

![مثال عن وحدة PDP تتضمن رسالة التوفر "في المخزون".](./media/pdp-InStock.png)

في المثال الموضح في الرسم التوضيحي التالي، تعرض PDP رسالة "نفاد المخزون".

![مثال عن وحدة PDP تتضمن رسالة "نفد من المخزون".](./media/pdp-outofstock.png)

في المثال الموضح في الرسم التوضيحي التالي، تعرض عربة التسوق رسالة في المخزن ("متوفرة").

![مثال عن وحدة سلة تسوق تتضمن رسالة التوفر "في المخزون".](./media/cart-instock.png)

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على مكتبة الوحدات](starter-kit-overview.md)

[تكوين المخازن المؤقتة للمخزون ومستويات المخزون](inventory-buffers-levels.md)

[الوحدة النمطية لعربة التسوق](add-cart-module.md)

[الوحدة النمطية لصندوق الشراء](add-buy-box.md)

[صفحات ووحدات إدارة الحسابات](account-management.md)

[الوحدة النمطية لمحدد المتجر](store-selector.md)

[تحديثات SDK ومكتبة الوحدات النمطية](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
