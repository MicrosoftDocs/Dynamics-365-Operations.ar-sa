---
title: التحقق من إمكانية الوصول إلى محتوى الصفحة
description: يصف هذا المقال كيفية التحقق من إمكانية الوصول إلى محتوى الصفحة في Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: retail
ms.search.form: ''
ms.openlocfilehash: 686ec37f24cf68902c4dd918c0ca8aea7612e1a9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291963"
---
# <a name="verify-page-content-accessibility"></a>التحقق من إمكانية الوصول إلى محتوى الصفحة

[!include [banner](includes/banner.md)]

يصف هذا المقال كيفية التحقق من إمكانية الوصول إلى محتوى الصفحة في Microsoft Dynamics 365 Commerce.

عند الانتهاء من تغيير صفحة، فإنه يجب عليك التأكد من إمكانية الوصول إلى المحتوى لكل شخص على الويب. في أدوات التأليف الخاصة بـ Commerce، يمكنك بسهولة التحقق من إمكانية الوصول إلى محتوى الصفحة باستخدام خدمة [Microsoft Accessibility Insights](https://accessibilityinsights.io/) المتكاملة. تتحقق هذه الخدمة من محتوى الصفحة الخاص بك بالمقارنة مع أحدث إرشادات [إمكانية الوصول التي وضعتها جمعية شبكة الإنترنت العالمية (W3C)](https://www.w3.org/standards/webdesign/accessibility).

يجب تشغيل دمج [Microsoft Accessibility Insights](https://accessibilityinsights.io/) على مستوى المستأجر أو الموقع قبل أن تتمكن من استخدامه.

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a>تشغيل Microsoft Accessibility Insights لكافة المواقع في المستأجر الخاص بك

لتشغيل تكامل [Microsoft Accessibility Insights](https://accessibilityinsights.io/) لكافة مواقع Commerce في المستأجر الخاص بك، اتبع هذه الخطوات.

> [!NOTE]
> للوصول إلى إعدادات المستأجر، فإنه يجب أن تقوم بتسجيل الدخول إلى Commerce بصفتك مسؤول نظام.

1. قم بتسجيل الدخول إلى Commerce بصفتك مسؤول نظام.
1. في جزء التنقل الأيمن، حدد **إعدادات المستأجر** (بجانب رمز الترس) لتوسيعه.
1. ضمن **إعدادات المستأجر**، حدد **الميزات**.
1. قم بتعيين خيار **التحقق من إمكانية الوصول** إلى **تشغيل**.

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a>تشغيل Microsoft Accessibility Insights لموقع واحد

لتشغيل تكامل [Microsoft Accessibility Insights](https://accessibilityinsights.io/) لموقع Commerce واحد، اتبع هذه الخطوات.

1. تحت **المواقع**، حدد **شركه الاتحاد للتصنيع** (أو اسم موقعك).
1. في جزء التنقل الأيسر، حدد **إعدادات الموقع** لتوسيعه.
1. ضمن **إعدادات الموقع**، حدد **الميزات**.
1. قم بتعيين خيار **التحقق من إمكانية الوصول** إلى **تشغيل**.

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a>التحقق من إمكانية الوصول إلى المحتوى على الصفحة الرئيسية

لاستخدام خدمة [Microsoft Accessibility Insights](https://accessibilityinsights.io/) المتكاملة لفحص محتوى الصفحة الرئيسية في Commerce والتحقق من صحته، اتبع الخطوات التالية.

1. تحت **المواقع**، حدد **شركه الاتحاد للتصنيع** (أو اسم موقعك).
1. في جزء التنقل الأيسر، حدد **الصفحات**.
1. ابحث عن الصفحة الرئيسية وحددها لفتحها في محرر الصفحة.
1. في شريط الأوامر، حدد **التحقق من إمكانية الوصول**. تظهر صفحة **التحقق من إمكانية الوصول**.
1. بعد اكتمال الفحص، راجع محتويات التقرير.
1. إذا فشلت أية عمليات فحص، حدد كل عنصر تحقق تم فشله لتوسيعه بحيث يمكنك عرض مزيد من التفاصيل.
1. لإغلاق التقرير بعد الانتهاء من مراجعته، قم بالتمرير إلى أسفل الصفحة **التحقق من إمكانية الوصول**، ثم حدد **موافق**.

## <a name="additional-resources"></a>الموارد الإضافية

[تعديل صفحة موقع موجودة](modify-existing-page.md)

[إضافة صفحة موقع جديدة](add-new-page.md)

[تحديد تخطيطات الصفحة](select-page-layouts.md)

[إدارة بيانات تعريف SEO](manage-seo-metadata.md)

[حفظ صفحة ومعاينتها ونشرها](save-preview-publish-page.md)

[إثراء صفحة منتج](enrich-product-page.md)

[إثراء الصفحة المنتقل إليها‬ لفئة](enrich-category-page.md)

[إنشاء صفحات التجارة الإلكترونية الديناميكية استنادا إلى معلمات URL](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
