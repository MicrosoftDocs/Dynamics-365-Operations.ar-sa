---
title: الوحدة النمطية لمنتقي البلد/المنطقة
description: يصف هذا الموضوع الوحدة النمطية لمنطقي البلد/المنطقة ويصف كيفية تكوينها في Microsoft Dynamics 365 Commerce.
author: stuharg
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2021-08-12
ms.dyn365.ops.version: Release 10.0.22
ms.openlocfilehash: 3134e10c096525ec2d82365a25eff16a3c5d5e11
ms.sourcegitcommit: d420b96d37093c26f0e99c548f036eb49a15ec30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/03/2021
ms.locfileid: "7472561"
---
# <a name="countryregion-picker-module"></a>الوحدة النمطية لمنتقي البلد/المنطقة

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

يصف هذا الموضوع الوحدة النمطية لمنطقي البلد/المنطقة ويصف كيفية تكوينها في Microsoft Dynamics 365 Commerce.

تستخدم الوحدة النمطية لمنتقي البلد/المنطقة ميزة [الكشف عن المواقع الجغرافية وإعادة التوجيه](geo-detection-redirection.md) في Dynamics 365 Commerce لإظهار عناوين url الموصي بها للعملاء الذين يقومون بطلب عنوان URL لموقع تجارة إلكترونية غير مرتبط بالبلد أو المنطقة الخاصة بهم.

على سبيل المثال، يطلب أحد العملاء في كندا عنوان URL لموقع غير مرتبط بكندا. وفي هذه الحالة، تعرض الوحدة النمطية لمنتقي البلد/المنطقة مربع حوار ينصح بعناوين URL الخاصة بالمواقع المقترنة بكندا. يبين الرسم التوضيحي التالي مثالاً عن مربع الحوار منطقة البلد/المنطقة.

![مثال لمربع حوار منتقي البلد/المنطقة في الصفحة الرئيسية.](./media/Geo_country-region-module-insitu.png)

## <a name="countryregion-picker-module-properties&quot;></a>خصائص الوحدة النمطية لمنتقي البلد/المنطقة

| اسم الخاصية              | قيمة       | الوصف |
| -------------------------- | ----------- | ----------- |
| العنوان‬                    | النص        | العنوان الذي يظهر أعلى مربع الحوار. |
| العنوان الفرعي                 | النص        | العنوان الفرعي الذي يظهر أسفل العنوان. |
| البلد: سلسلة العرض    | النص        | اسم العرض لخيار URL (على سبيل المثال، &quot;كندا"). |
| البلد: سلسلة العرض الفرعية | النص        | سلسلة عرض اختيارية فرعية لخيار URL (على سبيل المثال، "الإنجليزية" أو "الفرنسية"). |
| البلد: صورة البلد     | أصل الوسائط | صوره اختيارية مقترنة بخيار URL (على سبيل المثال، صورة لعلم كندا). |
| البلد: عنوان URL للبلد       | النص        | عنوان URL المتوافق مع القناة والإعدادات المحلية التي تم تكوينها للبلد أو المنطقة في صفحة **القنوات** في منشئ المواقع التجارية (**إعدادات الموقع\>القنوات**). يجب أن يتطابق عنوان URL هذا تماماً مع عنوان URL الذي تم تكوينه في صفحة **القنوات**. |
| ارتباط الإجراء                | ارتباط الإجراء | ارتباط اختياري يظهر أسفل مربع الحوار. على سبيل المثال، يمكن أن يشير هذا الارتباط إلى صفحة داخلية توفر قائمة بكافة البلدان والمناطق التي يدعمها الموقع. |

## <a name="add-a-countryregion-picker-module-to-a-page"></a>إضافة الوحدة النمطية لمنتقي البلد/المنطقة إلى صفحة

يمكن إضافة الوحدة النمطية لمنتقي البلد/المنطقة إلى الوحدة النمطية للرأس أما بشكل مباشر أو عن طريق جزء مشترك. لمزيد من المعلومات حول الوحدات النمطية للرأس، راجع [الوحدة النمطية للرأس](author-header-module.md).

## <a name="configure-the-countryregion-picker-module-in-commerce-site-builder"></a>تكوين الوحدة النمطية لمنتقي البلد/المنطقة في منشئ موقع التجارة

> [!NOTE]
> يجب تكوين عناوين URL التي توصي بها لعملائك ككائنات البلد في الوحدة النمطية لمنتقي البلد/المنطقة.

لكل عنوان URL ترغب في عرضه والتوصية به للعملاء، اتبع هذه الخطوات في منشئ موقع التجارة.

1. حدد فتحة الوحدة النمطية لمنتقي البلد/المنطقة.
1. في الجزء الخصائص، ضمن **قائمة البلدان**، حدد **إضافة بلد**.
1. حدد مربع **بلد جديد**.
1. في حقل **سلسلة العرض**، أدخل اسم العرض (على سبيل المثال، **كندا**).
1. اختياري: في حقل **السلسلة الفرعية للعرض**، أدخل سلسلة عرض فرعية (على سبيل المثال، **الفرنسية** أو **fr-ca**).
1. اختياري: حدد صورة من مكتبة الوسائط.
1. في الحقل **URL للبلد**، أدخل URL. يجب أن يتطابق عنوان URL هذا تماماً مع عنوان URL الذي يظهر في صفحة **القنوات** ويتم تعيينه إلى القناة، بما في ذلك الإعدادات المحلية المقترنة بالبلد أو المنطقة.
1. حدد **موافق**.
1. كرر هذه الخطوات مع أي عناوين URL أخرى تريد أن تعرضها الوحدة النمطية لمنتقي البلد/المنطقة.

## <a name="additional-resources"></a>الموارد الإضافية

[إعداد الكشف عن المناطق الجغرافية وإعادة التوجيه](geo-detection-redirection.md)

[نظرة عامة على مكتبة الوحدات](starter-kit-overview.md)

[وحدة الرأس](author-header-module.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]