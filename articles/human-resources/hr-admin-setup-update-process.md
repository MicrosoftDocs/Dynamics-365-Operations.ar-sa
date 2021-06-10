---
title: تحديث العملية
description: إن Microsoft Dynamics 365 Human Resources عبارة عن خدمة تأجير برامج (SaaS) حقيقية توفر تحديثات خدمة مستمرة بدون لمس للتغييرات في التطبيق والنظام الأساسي.
author: andreabichsel
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2466c53885340991aeeb0a07af83517473b332b6
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053625"
---
# <a name="update-process"></a>تحديث العملية

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يُعد Microsoft Dynamics 365 Human Resources بمثابة خدمة تأجير برامج (SaaS) حقيقة توفير تحديثات خدمة مستمرة بدون لمس. تحتوي هذه التحديثات على تغييرات في كل من التطبيق والنظام الأساسي التي غالبًا ما توفر تحسينات هامة للخدمة، بما في ذلك التحديثات التنظيمية.

## <a name="update-policy"></a>سياسة التحديث

يتم إصدار التحديثات في وتيرة منتظمة لجميع البيئات. يتم دعم Human Resources وفقًا لـ [سياسة دورة حياة Microsoft](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy)،  التي توفر إرشادات متناسقة ومتوقعة لتوفر الدعم.

## <a name="release-cadence"></a>وتيرة الإصدار 

يتم تطبيق تحديثات Human Resources على كافة البيئات تلقائيًا. يوفر Human Resources نوعين من الإصدارات:

- **تحديثات الخدمة**: تتم التحديثات كل أسبوعين وتشمل إصلاحات الأخطاء والميزات الجديدة. وتتضمن تحديثات الخدمة أيضًا تحديثا النظام الأساسي المطبقة عند إصدارها. للحصول على فكرة عن وقت إصدار تحديثات النظام الأساسي، راجع [الجدول 3: إصدارات النظام الأساسي](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md#table-3-platform-releases). تحتوي التحديثات كل أسبوعين على عملية تمهيدية عامة مقسمة عبر مناطق. لمزيد من المعلومات حول التحديثات كل أسبوعين، راجع [راجع ما هو الجديد أو المتغير في Dynamics 365 Human Resources](hr-admin-whats-new.md).

    يتم تحديث كافة مراكز بيانات المدعومة كل أسبوعين، ما لم يرد خلاف ذلك. يتم تضمين مناطق الولايات المتحدة الأمريكية وأوروبا والمملكة المتحدة وآسيا وكندا في التحديثات كل أسبوعين. 

- **تحديثات حل Dataverse**: تُجرى هذه التحديثات كل ستة أسابيع تقريبًا، حسب الحاجة. وهي تتضمن كيانات جديدة وتغييرات للكيانات الموجودة في Dataverse. وتصدر هذه التحديثات لنفس المناطق بوصفها التحديثات كل أسبوعين، وتستغرق حوالي ستة أسابيع للنسخ المتماثل عبر كافة مراكز البيانات. قد تتوافق أو لا تتوافق تحديثات الحلول مع تحديثات الخدمة كل أسبوعين.

> [!NOTE]
> تتوفر تحديثات الحلول في كافة مراكز البيانات بمجرد إصدارها. إذا كنت لا ترغب في انتظار التحديثات للنسخ المتماثل تلقائيًا، يُمكن تطبيق هذه التحديثات يدويًا على أي بيئة في أي مركز بيانات.

عند الحاجة، يوفر Human Resources أيضًا الأنواع التالية من الإصلاحات:

- **مراجعة (إصلاح عاجل)**: إصلاحات الأخطاء التي قد تحدث مع أو بعيدًا عن إصدار تحديث الخدمة كل أسبوعين

- **إصلاح طارئ**: يُمكن أن تشمل الاصلاحات العاجلة الاستباقية والتفاعلية ذات الطبيعة المستقلة التكوين فقط أو تغييرات الكود لحل مشاكل العرض المباشر، وقد تحدث بغض النظر عن إصدار تحديث الخدمة كل أسبوعين.

تتم مراجعة الإصدارات واختبارها والتحقق من صحتها في بيئة داخلية. بعد تسجيل الخروج من الإصدارات، يتم نشرها بعد ذلك إلى الإنتاج.

## <a name="release-cadence-exceptions-in-2021"></a>إصدار استثناءات الوتيرة في 2021

لحساب الإجازات، يكون جدول الإصدار لشهري نوفمبر وديسمبر 2021 كالتالي:

- إصدار شهر نوفمبر: 1 نوفمبر - 14 نوفمبر
- إصدار شهر ديسمبر: 29 نوفمبر - 12 ديسمبر
 
سيتم استئناف وتيرة الإصدار من أسبوعين بالشكل المعتاد في 10 يناير 2022.

## <a name="communications"></a>المراسلات

يُمكنك معرفة ما هو الموجود في الأعمال الخاصة بـ Human Resources وما قمنا بإصداره في المواقع التالية:

- [مخطط Dynamics 365 Human Resources ](https://dynamics.microsoft.com/roadmap/human-resources/)

- [خطط إصدار Dynamics 365](/dynamics365/release-plans/)

- [ما الجديد أو المتغير‬ في Dynamics 365 Human Resources](hr-admin-whats-new.md)

- [البحث عن المشاكل في Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs.md) (لإصلاح الأخطاء المتعلقة بالنظام الأساسي فقط)

- [مدونة Human Resources](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [مجتمع Human Resources Yammer](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a>ميزات المعاينة في بيئة الحماية

يُمكنك التحقق من صحة ميزات المعاينة في بيئة الحماية قبل تمكينها في بيئة الإنتاج الخاصة بك. لمزيد من المعلومات حول تمكين الميزات، راجع [نظرة عامة على إدارة الميزات](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

تبقي كافة الميزات الجديدة في معاينه لمده 30 يوما على الأقل، وبشكل نموذجي 30-60 يوما. تتوفر الميزات الرئيسية بشكل عام في أكتوبر و ابريل من كل عام يتبع فتره المعاينة. بمجرد ان تشاهد إمكانيات جديده في مساحة عمل إدارة الميزات، يمكنك تشغيلها. قد تكون بعض الميزات قيد التشغيل بشكل افتراضي.

في بعض الأوقات، سيتم تشغيل ميزه متكاملة بشكل افتراضي ولا يمكن إيقاف تشغيلها (على سبيل المثال مساحة عمل إدارة الميزات).

وبمجرد توفر إحدى الميزات بصفه عامه، قد يتم تشغيلها أو إيقاف تشغيلها في بيئات الإنتاج. وتشير مساحة عمل إدارة الميزات إلى ان ميزه المعاينة ستصبح إلزاميه. وعاده ما يكون هذا التاريخ في يوم 1 أكتوبر أو 1 إبريل لكي تتم محاذاته مع خطط الإصدار نصف السنوية. لا يمكنك إيقاف تشغيل الميزات الإلزامية. وحتى تصبح إلزاميا، يمكنك تشغيل أحدي الميزات وإيقاف تشغيلها في كافة البيئات.

نوصي بشدة بمعاينة الميزات في بيئة الحماية أو البيئة التجريبية. من الأفضل إنشاء نسخة من بيئة الإنتاج الحالية أو قاعدة البيانات في بيئة الحماية بحيث يمكنك الحصول على التجربة الكاملة للميزات الجديدة مع الميزات الجديدة مع البيانات الخاصة بك.

لمزيد من المعلومات حول توفير بيئة حماية، راجع [توفير مشروع Human Resources](hr-admin-setup-provision.md). لإزالة بيئة اختبار، راجع [إزالة مثيل](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment). 

## <a name="report-bugs"></a>الإبلاغ عن الأخطاء

أثناء اختبار ميزات المعاينة أو تجربة إمكانيات جديدة، قد تجد عناصر لا تعمل بالشكل المتوقع. يُرجى الإبلاغ عن أي أخطاء من خلال [دعم Microsoft Dynamics 365](https://dynamics.microsoft.com/support/).

## <a name="see-also"></a>راجع أيضًا

[خطط إصدار Dynamics 365 و Power Platform](/dynamics365/release-plans)</br>
[ما هو الجديد أو المتغير في Dynamics 365 Human Resources](hr-admin-whats-new.md)</br>
[سياسة دورة حياة البرامج](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]