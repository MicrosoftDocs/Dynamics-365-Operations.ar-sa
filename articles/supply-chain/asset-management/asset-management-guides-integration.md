---
title: تكامل Dynamics 365 Supply Chain Management (إدارة الأصول) مع Dynamics 365 Guides
description: يوضح هذا الموضوع كيفية تكامل الوحدة النمطية لإداره الأصول في Microsoft  Dynamics 365 Supply Chain Management مع Dynamics 365 Guides للاستفادة من دلائل الحقيقة المختلطة في مهام سير عمل الخدمات اليومية والصيانة.
author: kamaybac
ms.date: 04/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-28
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 50cfea6656e1f13532b018784fa64b2aac10fc7f
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908557"
---
# <a name="integrate-dynamics-365-supply-chain-management-asset-management-with-dynamics-365-guides"></a>تكامل Dynamics 365 Supply Chain Management (إدارة الأصول) مع Dynamics 365 Guides

يمكنك تكامل الوحدة النمطية **لإداره الأصول** في Microsoft Dynamics 365 Supply Chain Management مع Dynamics 365 Guides للاستفادة من دلائل الحقيقة المختلطة في مهام سير عمل الخدمات اليومية والصيانة. إذا كان الدليل مقترنا بأمر عمل إداره الأصول، فان العامل الذي يفتح قائمه فحص الصيانة الخاصة بأمر العمل في Supply Chain Management (Dynamics 365) للأجهزة المحمولة يري هذا الدليل متوفرًا. يمكن للعامل بعد ذلك العثور علي الدليل وفتحه في تطبيق Dynamics 365 Guides HoloLens.

## <a name="prerequisites"></a>المتطلبات الأساسية

قبل إرفاق الأدلة بأوامر عمل إداره الأصول، يجب عليك إكمال هذه المتطلبات الاساسيه:

- [إعداد Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) الإصدار 10.0.9 أو إصدار لاحق
- [قم بتشغيل الكتابة المزدوجة لتطبيقات Supply Chain Management](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).
- [قم بتشغيل إصدار التقييم](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) لميزة **MRGuidesFeature** . (بالنسبة لبيئات الإنتاج، يجب أولا إرسال بطاقة دعم لكي تتم إضافه المستأجر الخاص بك إلى مجموعة التقييم).
- [قم بتشغيل مفاتيح التكوين التالية](/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) في صفحة **تكوين الترخيص**:

    - إدارة الاصول \> الحقيقة المختلطة لإدارة الأصول
    - الحقيقة المختلطة \> دليل الحقيقة المختلطة

- [إعداد Dynamics 365 Guides](/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) الإصدار 200.0.0.96 أو إصدار لاحق

## <a name="use-dynamics-365-guides-with-asset-management"></a>استخدام Dynamics 365 Guides مع إدارة الأصول

لإقران دليل، يمكنك استخدام بند قائمه فحص الصيانة في إداره الأصول. يمكنك إنشاء الاقتران من خلال قالب قائمة فحص الصيانة أو نوع مهمة صيانة أو أمر عمل، نظرا لان الثلاثة تحتوي علي بنود قائمة فحص الصيانة. يمكنك توفير الوقت باستخدام قالب، وذلك لأنه يمكن اقران قالب بكافة أنواع مهام الصيانة التي تستخدمه. على سبيل المثال، يرتبط الدليل المرتبط بنوع مهمة صيانة تلقائيا بكافة أوامر العمل التي تحدد نوع المهمة هذا. ومن ناحية أخرى، يكون الدليل المرتبط مباشره بأمر العمل موجودًا فقط لأمر العمل هذا.

### <a name="associate-a-guide-with-a-maintenance-checklist-template"></a>إقران دليل بقالب قائمه فحص صيانة

لإقران دليل بقالب قائمه فحص صيانة، اتبع الخطوات التالية.

1. قم بإنشاء دليل باستخدام تطبيق Dynamics 365 Guides للكمبيوتر الشخصي وتطبيق HoloLens. لمزيد من المعلومات حول كيفية إنشاء دليل، راجع المواضيع التالية:

    - [استخدام تطبيق الكمبيوتر الشخصي لإنشاء دليل](/dynamics365/mixed-reality/guides/pc-app-overview)
    - [استخدام تطبيق HoloLens لوضع الهولوغرام الخاصة بك](/dynamics365/mixed-reality/guides/hololens-app-overview)

1. في Supply Chain Management، [قم بإنشاء قالب قائمة فحص صيانة](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template).
1. قم باقران الدليل الذي قمت بإنشاءه ببند قائمه فحص الصيانة في قالب قائمه فحص الصيانة الجديدة:

    1. في علامة التبويب السريعة **بنود قائمة فحص الصيانة** حدد البند الذي تريد إقران الدليل به.
    1. في علامة التبويب السريعة **الأدلة المرتبطة** ، حدد **إضافة دليل**.

        ![إقران دليل ببند قائمة فحص صيانة](media/am-guides-integration-add-guide.png "إقران دليل ببند قائمة فحص صيانة")

    1. في حقل **الاسم** حدد دليلا، ثم حدد **حفظ**.

        ![تحديد دليل في حقل الاسم](media/am-guides-integration-select-guide.png "تحديد دليل في حقل الاسم")

1. قم بإقران قالب قائمه فحص الصيانةبنوع مهمة:

    1. [قم بإنشاء نوع مهمة صيانة](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type) ، أو حدد نوع مهمة صيانة موجود.
    1. في جزء الاجراءات، حدد **الإعدادات الافتراضية لنوع مهمة الصيانة‬**.

        ![زر الإعدادات الافتراضية لنوع مهمة الصيانة](media/am-guides-integration-job-defaults.png "زر الإعدادات الافتراضية لنوع مهمة الصيانة")

    1. قم بإنشاء بند، ثم حدد **حفظ**.

        ![إنشاء بند](media/am-guides-integration-add-line.png "إنشاء بند")

    1. في جزء الإجراءات‬، حدد **قائمة فحص الصيانة**.

        ![زر قائمة فحص الصيانة](media/am-guides-integration-maintenance-checklist.png "زر قائمة فحص الصيانة")

    1. في علامة التبويب السريعة **بنود قائمة فحص الصيانة** قم بإضافه بند، ثم قم بتغيير قيمة حقل **النوع** إلى **قالب**.

        ![تغيير قيمة النوع](media/am-guides-integration-checklist-lines.png "تغيير قيمة النوع")

    1. في علامة التبويب السريعة **تفاصيل البند** ، في حقل **القالب** حدد القالب الذي قمت باقران الدليل به، ثم حدد **حفظ**.

        ![تحديد قالب](media/am-guides-integration-checklist-line-details.png "تحديد قالب")

1. [قم بإنشاء أمر عمل](work-orders/manually-created-workorders.md#create-work-order) ، ثم حدد نوع مهمة الصيانة التي تستخدم قالب قائمه فحص الصيانة الذي قمت بربطه بالدليل. يقترن الدليل تلقائيا بأمر العمل.

    ![تحديد نوع مهمة الصيانة](media/am-guides-integration-create-work-order.png "تحديد نوع مهمة الصيانة")

1. عرض الدليل المرتبط بامر العمل والعاملين:

    1. افتح [‏‫مساحة العمل المحمولة للأصل‬](asset-management-mobile-workspace.md) للوصول إلى أمر العمل.
    1. [افتح قائمة فحص الصيانة](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job) الخاصة بامر العمل.
    1. حدد بند قائمة فحص لعرض الدليل المقترن.

        ![الدليل المقترن ببند قائمة الفحص](media/am-guides-integration-show-guide.png "الدليل المقترن ببند قائمة الفحص")

    1. افتح الدليل على HoloLens.

        ![فتح الدليل على HoloLens](media/am-guides-integration-hololens-select.png "فتح الدليل على HoloLens").

> [!NOTE]
> يمكنك أيضا إقران دليل مباشره في قائمه فحص الصيانة لأمر عمل أو نوع مهمة.

> [!IMPORTANT]
> هناك مشكله معروفه عندما تقوم بإقران قالب قائمه فحص صيانة بنوع مهمة صيانة افتراضيه، لا يظهر الدليل المرتبط بالقالب على علامة التبويب السريعة **الدلائل المقترنة** بصفحة **الإعدادات الافتراضية لنوع مهمة الصيانة‬**. ومع ذلك، سيظهر الدليل بعد تطبيق نوع المهمة علي أمر العمل على علامة التبويب السريعة **الدلائل المقترنة**.

## <a name="see-also"></a>راجع أيضًا

- [نظرة عامة على الكتابة المزدوجة](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview.md)
- [نظرة عامة على إدارة الأصول](index.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]