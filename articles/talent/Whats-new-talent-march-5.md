---
title: ما الجديد أو المتغير في Dynamics 365 Talent (5 مارس 2019)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 855eafaca88d180997cf5a68c7f0fe975c177f88
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898909"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-5-2019"></a>ما الجديد أو المتغير في Dynamics 365 Talent (5 مارس 2019)

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Talent.

## <a name="changes-in-attract"></a>التغييرات في Attract

### <a name="extending-option-sets-in-attract"></a>توسيع مجموعات الخيارات في Attract

في Attract، توجد حقول متعددة هي عبارة عن مجموعات خيارات ضمن Common Data Service. تم تقديم قدرات جديدة لتوسيع مجموعات الخيارات، بدءًا من حقل سبب **الرفض**، وحقل **نوع التوظيف** وحقل **نوع الأقدمية**.

> [!IMPORTANT]
> يتطلب نشر إعلانات الوظائف في وظيفة LinkedIn استخدام الحقلين **نوع التوظيف** و**نوع الأقدمية** في صفحة **تفاصيل الوظيفة**. تلقى القيم الافتراضية في هذه الحقول دعم LinkedIn القيم وتظهر عند نشر الوظيفة. إذا كنت تنشر إعلانات الوظائف في LinkedIn وقمت بتعديل قيم مجموعة الخيارات الحالية لهذه الحقول، فسيستمر نشر إعلان الوظيفة، ولكن LinkedIn لن يعرض القيم المخصصة **نوع التوظيف** و**نوع الأقدمية**.

## <a name="changes-in-onboarding"></a>التغييرات في Onboarding

### <a name="private-preview-for-onboard-teams"></a>معاينة خاصة لفرق Onboard
يمكنك الآن بسهولة المشاركة والتعاون على قوالب عبر المؤسسة بأكملها. للحصول على مزيد من المعلومات، راجع [مشاركة أفضل الممارسات عبر مؤسستك بكاملها باستخدام فرق Onboard](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams).

### <a name="private-preview-for-assignee-placeholders"></a>معاينة خاصة للعناصر النائبة للمعهود إليه
يمكنك إثراء قوالبك عن طريق تعيين الأنشطة إلى أدوار بدلاً من تعيينها إلى أفراد. ويتم عندئذٍ تعيين أدوار إلى الأفراد عن إنشاء الدليل. للحصول على مزيد من المعلومات، راجع [تسهيل إدارة الدليل عن طريق تعيين الأنشطة إلى أدوار](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles).

## <a name="changes-in-core-hr"></a>التغييرات في Core HR
**الإصدار 8.1.2178**

### <a name="configure-workflow-to-auto-approve-or-follow-workflow-when-an-hr-or-line-manager-submits-or-updates-time-off-requests"></a>تكوين سير عمل للموافقة التلقائية أو متابعة سير العمل عندما يقوم قسم الموارد البشرية أو مدير مباشر بإرسال أو تحديث طلبات الإجازات
تمت إضافة شروط سير عمل جديدة للسماح بالموافقة التلقائية على طلبات الإجازات المرسلة بواسطة مدير الموظف أو قسم الموارد البشرية. هناك طريقة لتحقيق هذه الموافقة التلقائية على سير العمل وهي تمكين إجراء تلقائي على سير عمل الموافقة.

تتضمن الشروط المضافة:

- مرسل بواسطة‬ - يُستخدم هذا الخيار لتقييم معرّف مستخدم النظام للمستخدم الذي أرسل الطلب إلى سير العمل.
- مرسل بالنيابة عن ‬- يُستخدم هذا الخيار لتقييم ما إذا تم إرسال طلب إجازة نيابة عن العامل المقترن بالطلب.
- مرسل بواسطة الموارد البشرية- يُستخدم هذا الخيار لتقييم ما إذا كان مستخدم النظام الذي أرسل الطلب إلى سير العمل يؤدي دورًا خاصًا بالموارد البشرية.
- مرسل بواسطة المدير‬ - يُستخدم هذا الخيار لتقييم ما إذا كان المستخدم الذي أرسل طلب الإجازة إلى سير العمل هو مدير التدرج الهرمي المباشر للعامل المقترن بالطلب.

### <a name="enable-employee-fixed-compensation-for-future-position-assignments"></a>تمكين التعويض الثابت للموظف لتعيينات المناصب المستقبلية
من الطبيعي أن ينضم الموظفون إلى مؤسسة مع تاريخ بدء مستقبلي. سيسمح هذا التغيير بتحديد التعويض الثابت للموظفين الذين لديهم تعيينات مناصب مستقبلية.

### <a name="position-payroll-fields-are-blank-when-editing-the-position"></a>حقول كشوف الرواتب للمناصب فارغة عند تحرير المنصب
نتيجة هذا التغيير، عند طلب تغييرات على المناصب الموجودة، ستتضمن الآن حقول كشوف الرواتب القيم الحالية بشكل افتراضي.

### <a name="other-miscellaneous-bug-fixes"></a>إصلاحات أخطاء متنوعة أخرى
يتضمن هذا الإصدار إصلاحات أخطاء ثانوية أخرى:

### <a name="upgrade-to-common-data-service"></a>الترقية إلى Common Data Service
تقترب المواعيد النهائية للترقية إلى Common Data Service بسرعة. سجّل دخولك إلى مركز إدارة Power Apps لتحديد ما إذا كانت قاعدة بياناتك تحتاج إلى ترقية. للحصول على مزيد من المعلومات حول المواعيد النهائية والخطوات الضرورية للترقية، راجع [الترقية إلى Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).

## <a name="coming-soon"></a>قريبًا

###  <a name="advanced-compensation-security-fixed-and-variable"></a>أمان التعويض المتقدم (التعويض الثابت والمتغير)
في عدد كبير من المؤسسات، بإمكان مدراء التعويضات والمزايا فقط الوصول إلى سجلات تعويض معينة، مثل سجلات المدراء التنفيذيين أو الموظفين في الأقاليم. سيسمح لك هذا التغيير بإدارة خطط التعويض لمجموعات مختلفة من الموظفين في المؤسسة والمحافظة عليها. يمكن تعيين أدوار أمان إلى خطط التعويض الثابت والمتغير، مما يحدد حق الوصول إلى الخطط وبيانات الموظفين ذات الصلة بها، على سبيل المثال، معلومات حول الرواتب وسجلات المكافآت. الأدوار التي ستتمكن من الوصول لمعالجة تعويضات هؤلاء الموظفين هي فقط الأدوار التي تملك حق الوصول المحدد.

###  <a name="platform-update-24-for-finance-and-operations"></a>Platform update 24 لـ Finance and Operations
للحصول على تفاصيل إضافية حول Platform update 24 لـ Finance and Operations، راجع [الميزات الجديدة أو المتغيرة في Finance and Operations platform update 24 (مارس 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).
