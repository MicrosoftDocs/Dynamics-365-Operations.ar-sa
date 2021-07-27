---
title: نظرة عامة على نسق Adventure Works
description: يقدم هذا الموضوع نظرة عامة على نسق Adventure Works ويوضح كيفية تطبيقه على صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: c7557a36a948de5ae877d74bbbdea78821099b82
ms.sourcegitcommit: 7e976059118938b0089e40bef948029a8c088b38
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/09/2021
ms.locfileid: "6479397"
---
# <a name="adventure-works-theme-overview"></a>نظرة عامة على نسق Adventure Works

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

يقدم هذا الموضوع نظرة عامة على نسق Adventure Works ويوضح كيفية تطبيقه على صفحات الموقع في Microsoft Dynamics 365 Commerce.

يحتوي Dynamics 365 Commerce على نسق للتجارة الإلكترونية يُسمى Adventure Works. يعرض نسق Adventure Works منتجات الرياضة والاستجمام وتم تحسينه للحصول على تجربة زاخرة ومحسنة لسرد القصص. وهو يوفر مظهراً حديثاً وتخطيطات جديدة وتأثيرات حركة لإنشاء تجربة تسوق شاملة وتفاعلية على الإنترنت لعملاء التجارة الإلكترونية.

يوفر نسق Adventure Works مهام سير العمل الجديدة التالية:

- تدعم الوحدة النمطية لمشغل الفيديو الآن وظيفة العنوان والفقرة والارتباطات الخاصة بسرد قصص إضافية.
- يقوم الإجراء "إضافة إلى عربة التسوق" باستدعاء عربة تسوق مصغرة بدلاً من تقديم إخطار.
- تعد الوحدة النمطية للعرض السريع جزءا يتضمن شرائح في كل من سطح المكتب ومنافذ العرض المحمولة.
- يمكن أن تقوم عربة تسوق فارغة الآن بعروض الحملات الترويجية.

يتضمن نسق Adventure Works الوحدات النمطية لسرد القصص التالية في مكتبة الوحدة النمطية لـ Commerce:

- وحدة القائمة المتجانبة
- وحدة الميزة التفاعلية
- وحدة الاشتراك
- وحدة الصور النشطة
- وحدة قائمة الصورة

يعتبر نسق Commerce استجابة كاملة ويوفر تجربة محسنة لمنافذ العرض من خلال أجهزة سطح المكتب والأجهزة المحمولة والكمبيوتر اللوحي.

> [!IMPORTANT]
> ويتوفر نسق Adventure Works والوحدات النمطية الجديدة اعتبارا من الإصدار 10.0.20 من Dynamics 365 Commerce.

يبين الرسم التوضيحي التالي مثالا للصفحة الرئيسية التي تستخدم نسق Adventure Works.

![مثال للصفحة الرئيسية التي تستخدم نسق Adventure Works](./media/aw_b2c.PNG)

يبين الرسم التوضيحي التالي مثالا لصفحة قائمة تستخدم نسق Adventure Works.

![مثال لصفحة قائمة تستخدم نسق Adventure Works](./media/Aw_list.PNG)

يبين الرسم التوضيحي التالي مثالا لصفحة تفاصيل منتج (PDP) تستخدم نسق Adventure Works.

![مثال لصفحة تفاصيل منتج (PDP) تستخدم نسق Adventure Works](./media/aw_pdp.PNG)

## <a name="use-the-adventure-works-theme-for-b2b-sites"></a>استخدام نسق Adventure Works لمواقع B2B

يعتبر نسق Adventure Works أيضًا نسقًا مرجعيًا للمواقع من شركة إلى شركة (B2B). يتم عرض كافة الوحدات النمطية لـ B2B ومهام سير العمل في نسق Adventure Works. للحصول على معلومات حول كيفية إعداد موقع B2B، راجع [إعداد موقع B2B](./b2b/set-up-b2b-site.md).

يبين الرسم التوضيحي التالي مثالا لصفحة رئيسية لـ B2B تستخدم نسق Adventure Works.

![مثال لصفحة رئيسية لـ B2B تستخدم نسق Adventure Works](./media/aw_b2b.PNG)

## <a name="theme-extensions"></a>ملحقات النسق

يتضمن نسق Adventure Works العديد من ملحقات النسق، مثل **ملحقات العرض** وملحقات **تعريف الوحدة النمطية**. يمكن استخدام نسق Adventure Works كنسق مرجعي لإنشاء ملحقات متشابهة. على سبيل المثال ، يتم تنفيذ صفحة القائمة في نسق Adventure Works كملحق عرض يحتوي على مدقق أفقي. (حسب التباين، يتم استخدام المدقق بالجزء الأيمن في نسق Fabrikam.)

بطريقة مماثلة، تتضمن الوحدات النمطية الأخرى ملحقات تعريف الوحدة النمطية. على سبيل المثال، تتضمن [وحدة أيقونة عربة التسوق](cart-icon-module.md) فتحتين إضافيتين لـ **عربة تسوق فارغة** و **المحتوى الترويجي** يتم تنفيذها باستخدام ملحقات تعريفات الوحدة النمطية. بالإضافة إلى ذلك، تمت إضافة خاصية **شعار محمول** جديدة إلى الوحدة النمطية للرأس لدعم الشعار على نقاط عرض الأجهزة المحمولة. يتم تطبيق هذه الخاصية كملحق تعريف للوحدة النمطية للرأس.

لمزيد من المعلومات حول ملحقات النسق، راجع [ملحقات النسق](e-commerce-extensibility/theme-module-extensions.md).

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على مكتبة الوحدات](starter-kit-overview.md)

[وحدة القائمة المتجانبة](tile-list-module.md)

[وحدة الميزة التفاعلية](interactive-feature-module.md)

[وحدة الصور النشطة](active-image-module.md)

[وحدة الاشتراك](subscribe-module.md)

[وحدة قائمة الصورة](image-list-module.md)

[ملحقات النسق](e-commerce-extensibility/theme-module-extensions.md)

[وحدة رمز عربة التسوق](cart-icon-module.md)

[إعداد موقع التجارة الإلكترونية بين الشركات](./b2b/set-up-b2b-site.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
