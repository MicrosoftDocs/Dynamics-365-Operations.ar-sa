---
title: استلام لوحة الترخيص‬ عبر تطبيق المستودع
description: يوضح هذا الموضوع كيفية إعداد تطبيق المستودع لدعم استخدام عملية استلام لوحة الترخيص لاستلام المخزون الفعلي.
author: perlynne
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 7d5ac6598ab80ece0164d7c92f5d84e91d21b385
ms.sourcegitcommit: ffd845d4230646499b6f074cb43e69ab95787671
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/07/2020
ms.locfileid: "3346366"
---
# <a name="license-plate-receiving-via-the-warehousing-app"></a>استلام لوحة الترخيص‬ عبر تطبيق المستودع

يوضح هذا الموضوع كيفية إعداد تطبيق المستودع بحيث يدعم استخدام عملية استلام لوحة الترخيص لاستلام المخزون الفعلي.

يمكنك استخدام هذه الوظيفة لتسجيل استلام المخزون الوارد المرتبط بإشعار شحن مسبق (ASN) بسرعة. ينشئ النظام بشكل تلقائي إشعار ASN عند استخدام عمليات إدارة المستودعات لشحن أمر تحويل. بالنسبة إلى عملية أمر الشراء، يمكن تسجيل ASN يدويًا أو يمكن استيراده تلقائيًا باستخدام عمليات كيان بيانات ASN الواردة.

ترتبط بيانات ASN بالأحمال والشحنات عبر *بنى التعبئة*، حيث يمكن ان تحتوي البالتات (لوحات الترخيص الرئيسية) على حالات (لوحات الترخيص المتداخلة).

> [!NOTE]
> لتخفيض عدد حركات المخزون عند استخدام بنيات التعبئة التي تحتوي على لوحات ترخيص متداخلة، يقوم النظام بتسجيل المخزون الفعلي الموجود علي لوحة الترخيص الرئيسية. لتشغيل حركة المخزون الفعلي من لوحة الترخيص الأصلية إلى لوحات الترخيص المتداخلة، استنادًا إلى بيانات بنيه التعبئة، يجب أن يوفر الجهاز المحمول عنصر قائمة يستند إلى عملية إنشاء العمل *تعبئة لألواح الترخيص المتداخلة*.

<!-- To be used later (will require further editing):
## Warehousing mobile device app processing

When a worker scans an incoming license plate ID, the system initializes a license plate receiving process. Based on this information, the content of the license plate (data coming from the ASN) gets physically registered at the inbound dock location. The flows that follow will depend your business process needs.

## Work policies

As with (for example) the *Report as finished* mobile device menu item process, the license plate receiving process supports several workflows based on the defined setup.

### Work policies with work creation

Registration of physical on-hand where either the same warehouse worker immediately process a put-away work process following the inbound receiving (License plate receiving and put away) or where the registration and put away process gets handled as two different warehouse operations (License plate receiving) following the processing of the put-away work by using the existing work process via another mobile device menu item.

## Work policies without work creation

You can use the license plate receiving process without creating work by using the *License plate receiving without creating work* feature.

By defining **Work policies** with a **Work order type** of *Transfer receipt* and/or *Purchase orders*, and using the **Process** for **License plate receiving (and put away)**, the two Warehousing app process:

- License plate receiving
- License plate receiving and put away

will not create work, but only register the inbound physical inventory on the license plate at the inbound receiving dock.

For more information about the *Report as finished* production scenario, see the [Warehouse work policies overview](warehouse-work-policies.md).

-->

## <a name="show-or-skip-the-receiving-summary-page"></a>إظهار صفحة ملخص الاستلام أو تخطيها

يمكنك استخدام الميزة *التحكم في عرض صفحة ملخص الاستلام على الأجهزة المحمولة* للاستفادة من سير مهام إضافي مفصل في تطبيق مستودع إضافي كجزء من عملية استلام لوحة الترخيص.

قبل أن تتمكن من استخدام هذه الميزة، يجب تشغيلها في النظام. بإمكان المسؤولين استخدام إعدادات [دارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها. في مساحة عمل **إدارة الميزات**، تكون هذه الميزة مدرجة بالطريقة التالية:

- **الوحدة:** *إدارة المستودعات*
- **اسم الميزة:** *التحكم في عرض صفحة ملخص الاستلام على الأجهزة المحمولة*

عند تشغيل هذه الميزة، ستوفر عناصر قائمة الجهاز المحمول لاستلام لوحة الترخيص‬ أو استلام ‏‫لوحة الترخيص‬ وتخزينها‬ الإعداد **عرض صفحة ملخص الاستلام**. يتضمن هذا الإعداد الخيارات التالية:

- **عرض ملخص مفصل** – أثناء استلام لوحة الترخيص، سيرى العاملون صفحة إضافية تعرض معلومات ASN الكاملة.
- **تخطي الملخص** – لن يتمكن العاملون من رؤية معلومات ASN الكاملة. ولن يتمكن عمال المستودعات أيضًا من تعيين رمز الإرجاع أو إضافة استثناءات أثناء عملية الاستلام.

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a>منع استخدام لوحات الترخيص المشحونة في أمر التحويل في المستودعات غير المستودع الوجهة.

لا يمكن استخدام عملية استلام لوحة الترخيص إذا احتوى إشعار ASN على معرف لوحة ترخيص موجود ولديه بيانات فعلية في موقع مستودع آخر غير موقع المستودع حيث يحدث تسجيل لوحة الترخيص.

بالنسبة إلى سيناريوهات أمر التحويل التي لا يتعقب فيها مستودع البضاعة بالطريق ألواح الترخيص (وبالتالي لا يتعقب أيضًا المخزون الفعلي لكل لوحة ترخيص)، يمكنك استخدام الميزة *منع استخدام لوحات الترخيص المشحونة في أمر التحويل في مستودعات أخرى غير المستودع الوجهة.‬* لمنع التحديثات الفعلية لألواح الترخيص بالطريق.

قبل أن تتمكن من استخدام هذه الميزة، يجب تشغيلها في النظام. بإمكان المسؤولين استخدام إعدادات [دارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها. في مساحة عمل **إدارة الميزات**، تكون هذه الميزة مدرجة بالطريقة التالية:

- **الوحدة:** *إدارة المستودعات*
- **اسم الميزة:** *منع استخدام لوحات الترخيص المشحونة في أمر التحويل في مستودعات أخرى غير المستودع الوجهة*

لإدارة الوظائف عندما تكون هذه الميزة متوفرة، اتبع الخطوات التالية.

1. انتقل إلى **إدارة المستودعات‬\> إعداد‬ \> محددات إدارة المستودعات**.
1. على علامة التبويب **عام**، على علامة التبويب السريعة **ألواح الترخيص**، قم بتعيين الحقل **سياسة لوحة ترخيص مستودع البضاعة بالطريق** إلى إحدى القيم التالية:

    - **السماح بإعادة استخدام لوحة ترخيص غير متعقبة** – يعمل النظام بنفس الطريقة التي يعمل بها عندما لا تكون الميزة *منع استخدام لوحات الترخيص المشحونة في أمر التحويل في مستودعات أخرى غير المستودع الوجهة* متوفرة. هذه القيمة هي الإعداد الافتراضي عندما تقوم بتنشيط الميزة للمرة الأولى.
    - **منع إعادة استخدام لوحة الترخيص غير المتعقبة** – سوف يسمح فقط التحديثات المتاحة ذات الصلة بلوحة ترخيص مشحونة في المستودع الوجهة حتى يتم استلام أمر التحويل.

## <a name="more-information"></a>مزيد من المعلومات

<!-- To read more about inbound loads, see [Link for Inbound load (Olga's doc.)] -->

لمزيد من المعلومات حول عناصر قائمة الجهاز المحمول، راجع [إعداد الأجهزة المحمولة لعمل المستودع](configure-mobile-devices-warehouse.md).
