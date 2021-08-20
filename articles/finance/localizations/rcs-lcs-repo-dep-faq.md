---
title: إهلاك تخزين Regulatory Configuration Service (RCS) - Lifecycle Services (LCS)
description: يوفر هذا الموضوع معلومات حول إهلاك تخزين Microsoft Dynamics Lifecycle Services (LCS) الذي يتم التخطيط له كجزء من نشر المستودع العالمي Regulatory Configuration Service (RCS).
author: JaneA07
ms.date: 05/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, LCS storage, LCS storage deprecation
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.19
ms.openlocfilehash: 7a738af04da4425e76bd3b224400f91bc4eb8364d323da67ea457eaba9e65643
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782188"
---
# <a name="regulatory-configuration-service-rcs--lifecycle-services-lcs-storage-deprecation"></a>إهلاك تخزين Regulatory Configuration Service (RCS) – Lifecycle Services (LCS)

[!include [banner](../includes/banner.md)]

يتم إهمال استخدام Microsoft Dynamics Lifecycle Services (LCS) كمستودع تخزين لتكوينات التقارير الإلكترونية (ER). سيتضمن هذا الإهلاك التغييرات التالية:

- ولن يتم بعد ذلك نشر التكوينات التي تنتجها Microsoft والتي يتم استخدامها في تطبيقات Microsoft Dynamics 365 إلى مكتبة الأصل المشترك في LCS. وبدلاً من ذلك، سيتم نشرها فقط من خلال المستودع العمومي RCS. ومع ذلك ستستمر تكوينات Dynamics AX 2012 ليتم نشرها على مكتبة الأصل المشترك في LCS حتى انتهاء دورة الحياة لـ AX 2012.
- سيتم إلغاء تنشيط الوظيفة التي تتيح لك إمكانية تحميل التكوينات إلى مكتبة أصول المشروع في LCS من تطبيقات Finance and Operations، ومن RCS. ومع ذلك، سيظل بإمكانك استخدام المستعرض في LCS لتحميل التكوينات إلى مكتبة أصول المشروع. وبالتالي، سيظل بإمكانك إضافة تكوينات إلى LCS بحيث يمكن تضمينها في حزم الحلول.
- سيظل استيراد التكوينات من LCS متوفرًا ومدعومًا في تطبيقات Finance and Operations، وفي RCS، لبعض الوقت. ومع ذلك، سيتم إهمال الوظيفة في نهاية المطاف. (سيتم الإعلان عن تاريخ الإهلاك الفعلي لاحقًا.)

## <a name="deprecation-notice"></a>إشعار إهلاك

سيتم إرسال إهلاك استخدام LCS كمخزن في [‏‫الميزات التي تمت إزالتها أو إهمالها‬ في Dynamics 365 Finance - إشعار إهلاك LCS](../get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release). تاريخ الإهلاك المخطط هو 1 ابريل، 2022.

## <a name="key-features"></a>الميزات الرئيسية

- يمكنك استخدام RCS لإنشاء التكوينات وتحريرها. يمكنك بعد ذلك دفع هذه التكوينات مباشرة من المصمم إلى التطبيق المتصل. وبالتالي، يمكنك تغيير واختبار التكوينات الخاصة بك سريعًا.
- المستودع العمومي هو المخزن المركزي لكافة تكوينات التقارير الإلكترونية.

## <a name="guidance-for-one-time-and-ongoing-actions"></a>إرشادات الإجراءات التي يتم اتخاذها مرة واحدة ومستمرة

يصف هذا القسم مجموعة من الخطوات التي يجب إكمالها مرة واحدة. كما يصف الخطوات التي يجب إكمالها بشكل مستمر فيما بعد.

### <a name="one-time-action"></a>إجراء يتم اتخاذه مرة واحدة

قم باستيراد كافة التكوينات المطلوبة من LCS إلى RCS، ثم قم بنشرها من RCS إلى المستودع العمومي. إذا كنت تستخدم مكتبات أصول خاصة بالمشروع لتخزين التكوينات المشتقة في LCS، فإنه يجب إكمال الخطوات التالية أثناء استمرار الوصول إلى LCS.

1. في حالة عدم توفر مثيل RCS بالفعل، قم بتوفير واحدًا. لمزيد من المعلومات، راجع [نظرة عامة على RCS](rcs-overview.md).
2. في مثيل RCS المتوفر، لكل مشروع LCS في مكتبة الأصول التي تتضمن تكوينات التقارير الإلكترونية المشتقة، قم بتسجيل مستودع LCS المناسب.
3. قم باستيراد تكوينات التقارير الإلكترونية من مستودعات LCS إلى RCS. لمزيد من المعلومات، راجع [استيراد تكوينات التقارير الإلكترونية من LCS](../../dev-itpro/analytics/tasks/er-import-configuration-lifecycle-services.md).
4. إذا لم يتم توفير المستودع العمومي تلقائيًا، فقم بتسجيله في RCS.
5. قم بتحميل كافة التكوينات المشتقة من مثيل RCS الحالي إلى المستودع العمومي. استخدم ميزة **حزم التكوين التي تسمح للمستخدم بتحميل كافة التكوينات إلى المستودع العالمي في عملية واحدة** للمساعدة في إجراء التحميل. لمزيد من المعلومات، راجع [تحميل المستودع العالمي RCS](rcs-global-repo-upload.md).

### <a name="going-forward"></a>من الآن فصاعدًا

استخدم أدوات تصميم مرئية في RCS لإنشاء كافة التكوينات الجديدة. ثم، قم بتحميل تكوينات إلى المستودع العمومي للتخزين. لمزيد من المعلومات، راجع [إنشاء تكوين التقارير الإلكترونية في RCS والتحميل إلى المستودع العمومي](rcs-global-repo-upload.md).

## <a name="frequently-asked-questions"></a>الأسئلة المتداولة

### <a name="does-this-change-mean-that-lcs-cant-be-used-as-central-storage-for-configurations"></a>هل يعني هذا التغيير أنه لا يمكن استخدام LCS كمخزن مركزي لعمليات التكوين؟

نعم. سيتم إهلاك الوظيفة التي تتيح لك إمكانية تحميل التكوينات إلى مكتبة أصول المشروع في LCS من تطبيقات Finance and Operations. ومع ذلك، لا يزال بإمكانك استخدام المستعرض في LCS لتحميل التكوينات إلى مكتبة أصول المشروع على النحو الذي تريده.

### <a name="i-thought-that-rcs-was-a-replacement-repository-for-importing-global-template-files-i-didnt-think-that-its-used-to-store-configurations-which-is-correct"></a>أعتقد أن RCS كان مخزنًا بديلاً لاستيراد ملفات القوالب العمومية. لم أعتقد بأنه يتم استخدامه لتخزين التكوينات. هذا صحيح؟

RCS هي خدمة تصميم لإنشاء تكوينات التقارير الإلكترونية وتحريرها. يحتوي RCS على المستودع الخاص به والذي يُعرف باسم المستودع العمومي. يتم استخدام هذا المستودع لتخزين التكوينات التي يتم إنشاؤها في RCS. بعد إهلاك استخدام LCS كوحدة تخزين، سيكون المستودع العمومي هو مصدر فردي لتكوينات Microsoft. يجب إكمال إجراء يتم اتخاذه مرة واحدة لاستيراد كافة التكوينات التي تتطلبها من LCS إلى RCS ثم نشرها من RCS إلى المستودع العمومي.

### <a name="without-lcs-what-is-the-suggested-way-to-store-configurations-so-that-test-and-production-configurations-can-easily-be-managed-and-transferred"></a>بدون LCS، ما الطريقة المقترحة لتخزين التكوينات بحيث يمكن إدارة تكوينات "الاختبار" و "الإنتاج" وتحويلها بسهولة؟

يستخدم RCS مفهوم *التطبيق المتصل*. يُشكّل التطبيق المتصل اتصالاً بين RCS وأي مثيل لتطبيقات Finance and Operations: لأنه يمكن استخدام RCS لتحرير التكوينات، يمكن استخدام التطبيق المتصل لدفع التكوينات مباشرة من المصمم إلى بيئات تطبيقات Finance and Operations. ولذلك، يمكنك تغيير واختبار التكوينات الخاصة بك سريعًا بدلاً من الاضطرار إلى الانتقال خلال التخزين على مستوى مشروع LCS.

### <a name="are-there-any-examples-that-show-the-setup-and-management"></a>هل توجد أية أمثلة تظهر الإعداد والإدارة؟

لا توجد أمثلة، ولكن يمكنك إكمال الخطوات السابقة في هذا الموضوع لترحيل التكوينات الخاصة بك إلى المستودع العمومي لـ RCS.
