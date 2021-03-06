---
title: إضافة صفحة موقع جديدة
description: يصف هذا الموضوع كيفية إضافة صفحة موقع جديدة في Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 54e690b0dde048b17ce074fcc30cf20a9ff7a4ca
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097119"
---
# <a name="add-a-new-site-page"></a>إضافة صفحة موقع جديدة


[!include [banner](includes/banner.md)]

يصف هذا الموضوع كيفية إضافة صفحة موقع جديدة في Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>نظرة عامة

بعد إنشاء القوالب والأجزاء الخاصة بموقعك، فإن الخطوة التالية هي البدء في إنشاء صفحات تستخدمها. للبدء، يجب عليك تحديد قالب أو تخطيط واسم صفحة وعنوان URL للصفحة.

## <a name="template-or-layout"></a>قالب أو تخطيط

يمكنك استخدام قالب أو تخطيط لصفحتك الجديدة. لمزيد من المعلومات ، راجع [نظرة عامة على القوالب والتخطيطات](templates-layouts-overview.md).

## <a name="page-name"></a>اسم الصفحة

يجب أن يكون اسم الصفحة فريدًا لصفحتك. يجب أن يكون وصفيًا، حتى تتمكن من العثور عليه بسهولة ويعرف الآخرون المقصود من الصفحة. اختر اسم الصفحة بعناية، لأنه لا يمكن تغييره لاحقًا.

## <a name="page-url"></a>عنوان URL للصفحة

يمكنك الحصول على خيار إدخال عنوان URL لصفحتك الجديدة. عند إنشاء صفحة ، يمكنك إدخال سلسلة يتم استخدامها لتشكيل عنوان URL كامل. تُعرف هذه السلسلة بعنوان URL المرتبط أو عنوان URL الوصفي. ثم يتم إنشاء عنوان URL كامل استنادًا إلى عنوان URL الوصفي، ويتم تعيين الصفحة الجديدة إليها. يمكنك تغيير عنوان URL في وقت لاحق، قبل نشر الصفحة. لمزيد من المعلومات، راجع [إنشاء عنوان URL للصفحة](create-page-URL.md)

> [!NOTE]
> يفصل Dynamics 365 Commerce عناوين URL والمحتوى. بمعنى آخر، يمكن إنشاء صفحة غير مرتبطة بعنوان URL، ويمكن إنشاء عنوان URL غير مرتبط بصفحة. لذلك، يمكن إجراء تبديل المحتوى لعنوان URL ولا يتطلب تعطيلاً، كما أن عمليات إعادة التوجيه أسهل في إدارتها.

## <a name="add-a-new-page"></a>إضافة صفحة جديدة

لإضافة صفحة موقع جديدة إلى موقعك، اتبع هذه الخطوات.

1. تحت **المواقع**، حدد **شركه الاتحاد للتصنيع** (أو اسم موقعك).
1. حدد **صفحة جديدة**.
1. في مربع الحوار **صفحة جديدة** ، حدد قالب، ثم حدد **موافق**.
1. في الحقل **اسم الصفحة** ، ادخل اسم الصفحة (علي سبيل المثال، **صفحتي الجديدة**).
1. في الحقل **URL** ، أدخل سلسلة (URL slug) لإكمال عنوان URL (على سبيل المثال، **صفحتي_الجديدة**).
1. حدد **موافق**. يظهر محرر الصفحة. لاحظ أنه يتم إضافة عنوان وتذييل تلقائيًا إلى الصفحة، استنادًا إلى القالب الذي حددته.
1. في مخطط الصفحة، حدد فتحة **الرئيسية** ، وحدد زر علامة القطع (**...**) ، ثم حدد **إضافة وحدة نمطية**.
1. حدد **الحاوية**، ثم قم بتحديد **موافق**.
1. حدد **حاوية السائل**، حدد زر علامة الحذف، ثم حدد **‏‫إضافة وحدة نمطية**‬.
1. حدد **كتلة تنسيق المحتوى**، ثم حدد **موافق**.
1. حدد **كتلة تنسيق المحتوى**، حدد زر علامة الحذف، ثم حدد **‏‫إضافة وحدة نمطية**‬.
1. حدد **عنصر كتلة تنسيق المحتوى**، ثم حدد **موافق**.
1. في جزء الخصائص الموجود علي اليمين، حدد **فقرة**، ثم في الحقل، أدخل **نص الاختبار الخاص بي**.
1. حدد **حفظ**، ثم قم بتحديد **إنهاء التحرير**.
1. في حقل **التعليقات** ، أدخل **إضافة صفحة جديدة**، ثم حدد **موافق**.
1. حدد **معاينة** لمعاينه الصفحة الخاصة بك. عند الانتهاء، قم بإغلاق علامة تبويب المعاينة للرجوع إلى أداة التأليف.
1. حدد **نشر**.
1. في مسار التنقل (عناوين) ، حدد **شركه الاتحاد للتصنيع** (أو اسم موقعك).
1. في جزء التنقل علي اليسار، حدد **عناوين URL**.
1. ابحث عن وحدد عنوان URL لـ (**mynewpage**) الخاص بك في القائمة.
1. حدد **نشر**.

## <a name="additional-resources"></a>الموارد الإضافية

[تعديل صفحة موقع موجودة](modify-existing-page.md)

[تحديد تخطيطات الصفحة](select-page-layouts.md)

[إدارة بيانات تعريف SEO](manage-seo-metadata.md)

[حفظ صفحة ومعاينتها ونشرها](save-preview-publish-page.md)

[إثراء صفحة منتج](enrich-product-page.md)

[إثراء الصفحة المنتقل إليها‬ لفئة](enrich-category-page.md)

[التحقق من إمكانية الوصول إلى محتوى الصفحة](verify-accessibility.md)

[إنشاء صفحات التجارة الإلكترونية الديناميكية استنادا إلى معلمات URL](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]