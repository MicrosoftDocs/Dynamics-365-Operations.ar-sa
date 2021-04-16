---
title: إعداد تجربة
description: يصف هذا الموضوع كيفيه إعداد تجربه في خدمه جهة خارجيه.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 9976ca461f7e988c32b81565fa2d084709e5ad6e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792488"
---
# <a name="set-up-an-experiment"></a>إعداد تجربة

بعد [تعريف الفرضية وتحديد معايير النجاح التي ترغب في استخدامها](experimentation-identify.md)، سيتعين عليك اعداد التجربة الخاصة بك في الخدمة التابعة لجهة خارجية. يوضح الرسم التخطيطي التالي كافة الخطوات المتضمنة في اعداد وتشغيل تجربه علي أحد مواقع التجارة الالكترونيه في Dynamics 365 Commerce. وتتم تغطيه الخطوات الاضافيه في موضوعات منفصلة.

[![رحلة مستخدم التجربة - الإعداد](./media/experimentation_setup.svg)](./media/experimentation_setup.svg#lightbox)


## <a name="set-up-your-experiment-in-the-third-party-service"></a>اعداد التجربة الخاصة بك في خدمه الجهة الخارجية
يمكنك الآن اختيار خدمه الجهات الخارجية الخاصة بك لتشغيل التجربة ومراقبتها، واعداد موصل التجربة. ويتم سرد هذه المتطلبات الاساسيه في [التجربة في Dynamics 365 Commerce](experimentation-overview.md).

اتبع الخطوات المطلوبة لإنشاء تجربه في الخدمة التابعة لجهة خارجية. إذا تم تكوين الموصل بشكل صحيح، فإن قائمة التجارب الكاملة التي يتم إعدادها في الخدمة التابعة لجهة خارجية ستظهر في منشئ موقع Commerce خلال حوالي 5 دقائق.

## <a name="set-up-your-success-metrics"></a>قم باعداد معايير النجاح الخاصة بك
ويحتاج كل تجربه إلى معايير لقياس تاثير التباينات وللتحقق من صحة الفرضية. اتبع الخطوات التالية لتمكين حساب المقاييس في خدمه الجهة الأخرى باستخدام احداث بيانات تتبع الاستخدام النشطة من Dynamics 365 Commerce.

لإعداد معايير النجاح الخاصة بك، اتبع الخطوات التالية.

1. في منشئ موقع Commerce، حدد علامة التبويب **صفحات** في جزء التنقل الأيسر، ثم حدد الصفحة التي ترغب في تجميع المعايير عليها. 
1. انتقل إلى القسم **معرفات الاحداث للتعقب** الموجود في جزء الخصائص الأيمن للصفحة أو الوحدة النمطية التي تريد تعقبها.
1. حدد **عرض**. يتم عرض قائمه بكافة معرفات الاحداث. انسخ الحدث الذي تريد تعقبه، ثم ألصق مفتاح الحدث في الموقع المعين في خدمه الجهة الأخرى. إذا كنت تريد أكثر من حدث واحد، فقم بنسخ المفاتيح الواحدة كل مره. 
    - لمعرفه كيفيه عرض كافة الاحداث والسمات المتاحة، بما في ذلك طرق عرض الصفحة وتعقب الإيرادات، راجع [احداث مكونات التجارة لعمليات التشخيص واستكشاف الأخطاء وإصلاحها ](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).
1. قم باجراء إيه خطوات أخرى لتعقب المقاييس وفقا لما هو مطلوب في الخدمات التابعة لجهة خارجية.

## <a name="previous-step"></a>الخطوة السابقة
[تحديد الفرضية وتحديد المقاييس الخاصة بتجربة](experimentation-identify.md) 


## <a name="next-step"></a>الخطوة التالية
[الاتصال بتجربة وتحريرها](experimentation-connect-edit.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]