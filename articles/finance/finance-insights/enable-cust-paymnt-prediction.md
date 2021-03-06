---
title: تمكين توقعات دفع العميل (معاينة)
description: يوضح هذا الموضوع كيفية تشغيل وتكوين ميزة توقعات دفع العميل في Finance Insights.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 584c1af5f9252a4b8c88a8866a64184bd0595b2e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009408"
---
# <a name="enable-customer-payment-predictions-preview"></a>تمكين توقعات دفع العميل (معاينة)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

يوضح هذا الموضوع كيفية تشغيل وتكوين ميزة توقعات دفع العميل في Finance Insights. يمكنك تشغيل الميزة في مساحة عمل **إدارة الميزات** وأدخل إعدادات التكوين في الصفحة **معلمات Financial insights**. يتضمن هذا الموضوع أيضًا معلومات يمكن أن تساعدك في استخدام الميزة بفاعلية.

> [!NOTE]
> قبل إكمال الخطوات التالية، تأكد من إكمال الخطوات الأساسية في الموضوع [تكوين Financial insights](configure-for-fin-insites.md).

1. استخدم المعلومات من صفحة البيئة في Microsoft Dynamics Lifecycle Services (LCS) للاتصال بالمثيل الأساسي لـ Azure SQL لتلك البيئة. قم بتشغيل الأمر Transact-SQL (T-SQL) لتشغيل إصدارات التقييم لبيئة وضع الحماية. (قد تضطر إلى تشغيل الوصول إلى عنوان IP الخاص بك في LCS قبل أن تتمكن من الاتصال بخادم كائن التطبيق عن بُعد \[AOS\].)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED, PARTITION) VALUES ('PayPredEnableFeature', 1, 5637144576)`

    > [!NOTE]
    > إذا كان نشر Microsoft Dynamics 365 Finance عبارة عن نشر Service Fabric، فإنه يمكنك تخطي هذه الخطوة. يجب أن يكون فريق Finance insights قد قام بالفعل بتشغيل إصدار التقييم. إذا لم تر الميزة في مساحة عمل **إدارة الميزات**، أو إذا واجهتك مشكلات عند محاولة تشغيلها، تواصل على <fiap@microsoft.com>

2. تشغيل ميزة معلومات دفع العميل:

    1. انتقل إلى **إدارة النظام \> مساحات العمل \> إدارة الميزات**.
    2. ابحث عن الميزة التي تسمى **معلومات دفع العميل (معاينة)‬**.
    3. حدد **تمكين الآن**.

    تم تشغيل ميزة معلومات دفع العميل الآن وأصبحت جاهزة ليتم تكوينها.

3. تكوين ميزة معلومات دفع العميل:

    1. انتقل إلى **عمليات التحصيل والائتمان \> الإعداد \> Finance insights \> معلمات Finance insights**.

        [![صفحة معلمات Financial insights قبل تكوين الميزة](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)

    2. في الصفحة **معلمات Financial insights**، في علامة التبويب **معلومات دفع العميل**، حدد الارتباط **عرض حقول البيانات المستخدمة في نموذج التنبؤ** لفتح الصفحة **حقول البيانات لنموذج التنبؤ**. هناك، يمكنك عرض القائمة الافتراضية للحقول المستخدمة لإنشاء نموذج التنبؤ الخاص بالذكاء الاصطناعي (AI) لتوقعات دفع العميل.

        لاستخدام قائمة الحقول الافتراضية لإنشاء نموذج التنبؤ، قم بإغلاق الصفحة **حقول البيانات لصفحة نموذج التنبؤ**، ثم، في الصفحة **معلمات Financial insights**، قم بتعيين الخيار **تمكين الميزة** إلى **نعم**.

    3. حدد فترة الحركة "متأخر جدًا" لتحديد ما إذا كان دلو التنبؤ **متأخر جدًا** تعني لشركتك أم لا.

        بالنسبة لكل فاتورة مفتوحة، يقوم النظام بالتوقع إلى احتمالية الدفع في ثلاثة دلو **في الوقت المحدد** و **متأخر** و **متأخر جدًا**.

        - **في الوقت المحدد** يتضمن هذا الدلو المدفوعات المتوقعة التي يتم دفعها في أو قبل تاريخ استحقاق الحركة.
        - **متأخر** – يتضمن هذا الدلو المدفوعات المتوقعة التي يتم دفعها بعد تاريخ استحقاق الحركة ولكن قبل بدء فترة الحركة "متأخر جدًا".
        - **متأخر جدًا** – يتضمن هذا الدلو المدفوعات المتوقعة التي يتم دفعها بعد بدء الحركة "متأخر جدًا".

        > [!NOTE]
        > إذا قمت بتغيير فترة الحركة "متأخر جدا" وحدد **تغيير الحد** بعد أن تم إنشاء نموذج التنبؤ AI الخاص بمدفوعات العميل، فإنه سيتم حذف نموذج التنبؤ الموجود وإنشاء نموذج جديد. سيقوم نموذج التنبؤ الجديد بنقل الحركات إلى فترة "متأخر جدا"، وذلك استنادًا إلى الإعدادات التي تم إدخالها لتعريفها.

    4. بعد الانتهاء من تحديد فترة الحركة "متأخر جدًا"، حدد **إنشاء نموذج توقع** لإنشاء نموذج التنبؤ. يعرض القسم **نموذج التنبؤ** على الصفحة **معلمات Financial insights** حالة نموذج التنبؤ.

        > [!NOTE]
        > في أي وقت يتم فيه إنشاء نموذج التنبؤ، فإنه يمكن تحديد **إعادة تعيين إنشاء نموذج** لإعادة تشغيل العملية.

    لقد تم تكوين الميزة الآن وهي جاهزة للاستخدام.

بعد أن تم تشغيل الميزة وتكوينها، وإنشاء نموذج التنبؤ والعمل، يعرض القسم **نموذج التنبؤ** في الصفحة **معلمات Financial insights** دقة النموذج، كما هو موضح في الرسم التوضيحي التالي.

[![دقة نموذج التنبؤ في صفحة معلمات Financial insights](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)

## <a name="release-details"></a>تفاصيل الإصدار

تتوفر معاينة عامة لـ Finance insights لعمليات النشر التجريبية في الولايات المتحدة الأميركية وأوروبا والمملكة المتحدة. تُعد Microsoft دعمًا إضافيًا بشكل متزايد للعديد من المناطق.

يمكن أن يتم تشغيل ميزات المعاينة العامة ويجب تشغيلها فقط في بيئات الحماية لتحديد صلاحيات المستوى 2. لا يمكن ترحيل نماذج الإعداد وAI التي يتم إنشاؤها في بيئة الحماية إلى بيئة التشغيل. لمزيد من المعلومات، راجع [شروط الاستخدام الإضافية لمعاينات Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).

## <a name="privacy-notice"></a>إشعار الخصوصية

إن المعاينات (1) قد تستخدم تدابير أقل تتعلق بالخصوصية وإجراءات الأمان مقارنةً بخدمة Dynamics 365 Finance and Operations‏، و(2) لا يتم تضمينها في اتفاقية مستوى الخدمة (SLA) لهذه الخدمة، و(3) يجب ألا يتم استخدامها لمعالجة البيانات الشخصية أو البيانات الأخرى التي تخضع لمتطلبات التوافق القانونية أو التنظيمية، و(4) هي ذات دعم محدود.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]