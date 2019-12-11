---
title: حالات المستند ودوره الحياة
description: يتناول هذا الموضوع العديد من حالات المستندات المختلفة لعناصر الصفحات في Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a34d10edbf84ac1814afdc7107727aea68a303e0
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770402"
---
# <a name="document-states-and-lifecycle"></a>حالات المستند ودوره الحياة

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

يتناول هذا الموضوع العديد من حالات المستندات المختلفة لعناصر الصفحات في Microsoft Dynamics 365 Commerce.

## <a name="document-state-descriptions"></a>أوصاف حالة المستند

يسرد الموضوع [عناصر الصفحة](page-elements-overview.md) الأنواع المختلفة من المستندات في نظام إدارة المحتوي (CMS). يمكن أن يكون لأنواع المستندات العديد من الحالات في أداة التأليف. تساعد حالات المستند علي منع تعارض البيانات وفرض التحكم في الإصدار. وهي تحدد من يمكنه تغيير المستندات، ومتى يمكن تغيير المستندات، ومتى يمكن عرض التغييرات بواسطة أشخاص آخرين.

يوضح الجدول التالي حالات المستند المحتملة لعناصر الصفحة في Commerce.

| حالة المستند | ‏‏الوصف |
|---|---|
| تم السداد مع الخروج | عندما يتم سحب عنصر CMS إليك، لا يمكن تحريره بواسطة أيًا من مستخدمي النظام المصادقين الآخرين. وتكون أي تغييرات تُجريها علي العنصر مرئية لك فقط. |
| تم الإيداع | عند إيداع عنصر CMS، تكون كافة التغييرات مرئية لمستخدمي النظام المصادقين الآخرين، ويمكن لهؤلاء المستخدمين سحب العنصر وتحريره. تقوم كل عمليه إيداع بإنشاء سجل إصدار مستند في سجل الصنف. |
| منشور | عند نشر عنصر CMS، يتم نقله إلى موقعك المباشر ويصبح قابلاً للاكتشاف علي الإنترنت بواسطة المستخدمين الخارجيين غير المُصادقين. لا يمكن نشر الأصناف إلا إذا تم إيداعها. |
| محفوظ | يمكن حفظ التغييرات التي تم اجراؤها علي عنصر CMS مسحوب إلى CMS قبل إيداع العنصر أو نشره. ولا تظهر هذه التغييرات المحفوظة لمستخدمي النظام المُصادقين الآخرين حتى يتم إيداع العنصر. و تكون مرئية للمستخدمين الخارجيين إلى أن يتم نشر العنصر. |
| تم تجاهل السحب | عند تجاهل عنصر CMS تم سحبه، يتم حذف كافة التغييرات المحفوظة، ويتم إرجاع الصنف إلى الإصدار الذي تم إيداعه مؤخرًا. |

## <a name="additional-resources"></a>الموارد الإضافية

[طرق إضافة المحتوى](add-manage-content.md)

[مصطلحات نموذج الصفحة](page-elements-overview.md)

[العمل باستخدام الوحدات النمطية](work-with-modules.md)

[العمل باستخدام الأجزاء](work-with-fragments.md)

[نظرة عامة على القوالب والتخطيطات](templates-layouts-overview.md)

[تخصيص التنقل في الموقع](customize-site-navigation.md)
