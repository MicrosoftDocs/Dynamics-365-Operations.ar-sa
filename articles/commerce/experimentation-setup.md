---
title: إعداد تجربة
description: يصف هذا المقال كيفيه إعداد تجربه في خدمه جهة خارجيه.
author: sushma-rao
ms.date: 06/08/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 1073cdc509622279ce7388b8b406079a4e6e9e09
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946156"
---
# <a name="set-up-an-experiment"></a>إعداد تجربة

بعد [تعريف الفرضية وتحديد معايير النجاح التي ترغب في استخدامها](experimentation-identify.md)، سيتعين عليك اعداد التجربة الخاصة بك في الخدمة التابعة لجهة خارجية. يوضح الرسم التخطيطي التالي كافة الخطوات المتضمنة في اعداد وتشغيل تجربه علي أحد مواقع التجارة الالكترونيه في Dynamics 365 Commerce. وتتم تغطيه الخطوات الاضافيه في مقالات منفصلة.

[ ![رحلة مستخدم التجربة - الإعداد.](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)


## <a name="set-up-your-experiment-in-the-third-party-service"></a>اعداد التجربة الخاصة بك في خدمه الجهة الخارجية
يمكنك الآن اختيار خدمه الجهات الخارجية الخاصة بك لتشغيل التجربة ومراقبتها، واعداد موصل التجربة. ويتم سرد هذه المتطلبات الاساسيه في [التجربة في Dynamics 365 Commerce](experimentation-overview.md).

اتبع الخطوات المطلوبة لإنشاء تجربه في الخدمة التابعة لجهة خارجية. إذا تم تكوين الموصل بشكل صحيح، فإن قائمة التجارب الكاملة التي يتم إعدادها في الخدمة التابعة لجهة خارجية ستظهر في منشئ موقع Commerce خلال حوالي 5 دقائق.

## <a name="set-up-your-success-metrics"></a>قم باعداد معايير النجاح الخاصة بك
ويحتاج كل تجربه إلى معايير لقياس تاثير التباينات وللتحقق من صحة الفرضية. اتبع الخطوات التالية لتمكين حساب المقاييس في خدمه الجهة الأخرى باستخدام احداث بيانات تتبع الاستخدام النشطة من Dynamics 365 Commerce.

لإعداد مقاييس النجاح للوحدات الجاهزة، اتبع هذه الخطوات.

1. في منشئ موقع Commerce، حدد علامة التبويب **صفحات** في جزء التنقل الأيسر، ثم حدد الصفحة التي ترغب في تجميع المعايير عليها. 
1. انتقل إلى القسم **معرفات الاحداث للتعقب** الموجود في جزء الخصائص الأيمن للصفحة أو الوحدة النمطية التي تريد تعقبها.
1. حدد **عرض**. يتم عرض قائمة بجميع معرفات حدث النقر. انسخ الحدث الذي تريد تتبعه، ثم الصق مفتاح الحدث في الموقع المحدد في خدمة الجهة الخارجية. إذا كنت تريد أكثر من حدث واحد، فقم بنسخ المفاتيح الواحدة كل مره. 
1. بالنسبة لطرق عرض الصفحة ، استخدم قيمه التجزئة الSHA-256ه لاسم الصفحة في منشئ الموقع الملحقة ب `.PageView`. علي سبيل المثال ، معرف الحدث ل `Homepage.PageView``e217eb66c7808ecc43b0f5c517c6a83b39d72b91412fbd54a485da9d8e186a9`
1. قم باجراء إيه خطوات أخرى لتعقب المقاييس وفقا لما هو مطلوب في الخدمات التابعة لجهة خارجية.

بالنسبة لنقرات الوحدة النمطية المخصصة ، اتبع الخطوات التالية لتحرير احداث النقر:

1. قم **بتحضير كائن تيليميتريكونتينت** للوحدة النمطية باستخدام الوظيفة أدناه. تاخذ هذه الوظيفة اسم الصفحة واسم الوحدة النمطية وكائن بيانات تتبع الاستخدام الافتراضي الذي تم توفيره كادخالات.

    ```TypeScript
    getTelemetryObject(pageName: string, moduleName: string, telemetry: ITelemetry): ITelemetryContent
    ```
    
    التالي هو مثال لطلب: 
    
    ```TypeScript
    private readonly telemetryContent: ITelemetryContent = getTelemetryObject(this.props.context.request.telemetryPageName!, this.props.friendlyName, this.props.telemetry);
    ```
    
1. تتيح إنشاء بيانات الحمولة التي تحتوي علي معلومات حول ما يجب التقاطه. بالنسبة للأزرار وعناصر التحكم الأخرى الثابتة ، يمكنك تضمين **اتيكست** مثل "التسوق الآن" أو "البحث". النسبة للمكونات التي تتضمن نقرات مثل النقر فوق بطاقة المنتج ، يمكن إرسال **recid** وهو معرف السجل الخاص بالمنتج أو معرف المنتج.

    ```TypeScript
    getPayloadObject(eventType: string, telemetryContent: ITelemetryContent, etext: string, recid?: string): IPayLoad
    ```
    كمثال لعناصر التحكم الثابتة ، قم بتمرير الزر سلسله نصيه كما هو موضح أدناه:

    ```TypeScript
    const payLoad = getPayloadObject('click', this.props.telemetryContent, 'Shop Now', '');
    ```
    كمثال لنقرات المنتج، قم بتمرير ريكورديد المنتج كما هو موضح أدناه:

    ```TypeScript
    const payLoad = getPayloadObject('click', telemetryContent!, '', product.RecordId.toString());
    ```
    
1. قم باستدعاء الدالة **OnClick** لتسجيل الحدث.

    ```TypeScript
    onTelemetryClick = (telemetryContent: ITelemetryContent, payLoad: IPayLoad, linkText: string) => () =>
    ```

    التالي هو مثال لطلب:

    ```TypeScript
    onClick: onTelemetryClick(this.props.telemetryContent, payLoad, linkText)
    ```

## <a name="previous-step"></a>الخطوة السابقة
[تحديد الفرضية وتحديد المقاييس الخاصة بتجربة](experimentation-identify.md) 


## <a name="next-step"></a>الخطوة التالية
[الاتصال بتجربة وتحريرها](experimentation-connect-edit.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
