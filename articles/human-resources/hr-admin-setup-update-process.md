---
title: تحديث العملية
description: إن Microsoft Dynamics 365 Human Resources عبارة عن خدمة تأجير برامج (SaaS) حقيقية توفر تحديثات خدمة مستمرة بدون لمس للتغييرات في التطبيق والنظام الأساسي.
author: andreabichsel
manager: AnnBe
ms.date: 02/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 006f3c7218436c1c70e29e51f8b1b784ae36b2dd
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431166"
---
# <a name="update-process"></a>تحديث العملية

يُعد Microsoft Dynamics 365 Human Resources بمثابة خدمة تأجير برامج (SaaS) حقيقة توفير تحديثات خدمة مستمرة بدون لمس. تحتوي هذه التحديثات على تغييرات في كل من التطبيق والنظام الأساسي التي غالبًا ما توفر تحسينات هامة للخدمة، بما في ذلك التحديثات التنظيمية.

## <a name="update-policy"></a>سياسة التحديث

يتم إصدار التحديثات في وتيرة منتظمة لجميع البيئات. يتم دعم Human Resources وفقًا لـ [سياسة دورة حياة Microsoft](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy)،  التي توفر إرشادات متناسقة ومتوقعة لتوفر الدعم.

## <a name="release-cadence"></a>وتيرة الإصدار

يتم تطبيق تحديثات Human Resources على كافة البيئات تلقائيًا. يوفر Human Resources نوعين من الإصدارات:

- **تحديثات الخدمة**: تتم التحديثات كل أسبوعين وتشمل إصلاحات الأخطاء والميزات الجديدة. وتتضمن تحديثات الخدمة أيضًا تحديثا النظام الأساسي المطبقة عند إصدارها. للحصول على فكرة عن وقت إصدار تحديثات النظام الأساسي، راجع [الجدول 3: إصدارات النظام الأساسي](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases). تحتوي التحديثات كل أسبوعين على عملية تمهيدية عامة مقسمة عبر مناطق. لمزيد من المعلومات حول التحديثات كل أسبوعين، راجع [راجع ما هو الجديد أو المتغير في Dynamics 365 Human Resources](hr-admin-whats-new.md).

    يتم تحديث كافة مراكز بيانات المدعومة كل أسبوعين، ما لم يرد خلاف ذلك. يتم تضمين مناطق الولايات المتحدة الأمريكية وأوروبا والمملكة المتحدة وآسيا وكندا في التحديثات كل أسبوعين. 

- **تحديثات حل Common Data Service**: تُجرى هذه التحديثات كل ستة أسابيع تقريبًا، حسب الحاجة. وهي تتضمن كيانات جديدة وتغييرات للكيانات الموجودة في Common Data Service. وتصدر هذه التحديثات لنفس المناطق بوصفها التحديثات كل أسبوعين، وتستغرق حوالي ستة أسابيع للنسخ المتماثل عبر كافة مراكز البيانات. قد تتوافق أو لا تتوافق تحديثات الحلول مع تحديثات الخدمة كل أسبوعين.

> [!NOTE]
> تتوفر تحديثات الحلول في كافة مراكز البيانات بمجرد إصدارها. إذا كنت لا ترغب في انتظار التحديثات للنسخ المتماثل تلقائيًا، يُمكن تطبيق هذه التحديثات يدويًا على أي بيئة في أي مركز بيانات.

عند الحاجة، يوفر Human Resources أيضًا الأنواع التالية من الإصلاحات:

- **مراجعة (إصلاح عاجل)**: إصلاحات الأخطاء التي قد تحدث مع أو بعيدًا عن إصدار تحديث الخدمة كل أسبوعين

- **إصلاح طارئ**: يُمكن أن تشمل الاصلاحات العاجلة الاستباقية والتفاعلية ذات الطبيعة المستقلة التكوين فقط أو تغييرات الكود لحل مشاكل العرض المباشر، وقد تحدث بغض النظر عن إصدار تحديث الخدمة كل أسبوعين.

تتم مراجعة الإصدارات واختبارها والتحقق من صحتها في بيئة داخلية. بعد تسجيل الخروج من الإصدارات، يتم نشرها بعد ذلك إلى الإنتاج.

## <a name="release-cadence-exceptions-in-2020"></a>إصدار استثناءات الوتيرة في 2020

تعتبر التواريخ التالية استثناءات لجدول الإصدار المنتظم:

| التاريخ | ‏‏الوصف |
| --- | --- |
| أسبوع من 23 نوفمبر | لا توجد تحديثات |
| أسبوع من 14 ديسمبر | تحديثات ثانوية فقط |
| أسبوع من 21 ديسمبر | لا توجد تحديثات |
| أسبوع من 28 ديسمبر | لا توجد تحديثات |

## <a name="communications"></a>المراسلات

يُمكنك معرفة ما هو الموجود في الأعمال الخاصة بـ Human Resources وما قمنا بإصداره في المواقع التالية:

- [مخطط Dynamics 365 Human Resources ](https://dynamics.microsoft.com/roadmap/human-resources/)

- [خطط إصدار Dynamics 365](https://docs.microsoft.com/dynamics365/release-plans/)

- [ما الجديد أو المتغير‬ في Dynamics 365 Human Resources](hr-admin-whats-new.md)

- [البحث عن المشاكل في Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (لإصلاح الأخطاء المتعلقة بالنظام الأساسي فقط)

- [مدونة Human Resources](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [مجتمع Human Resources Yammer](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a>ميزات المعاينة في بيئة الحماية

يُمكنك التحقق من صحة ميزات المعاينة في بيئة الحماية قبل تمكينها في بيئة الإنتاج الخاصة بك. لمزيد من المعلومات حول تمكين الميزات، راجع [نظرة عامة على إدارة الميزات](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

تبقي كافة الميزات الجديدة في معاينه لمده 30 يوما على الأقل، وبشكل نموذجي 30-60 يوما. تتوفر الميزات الرئيسية بشكل عام في أكتوبر و ابريل من كل عام يتبع فتره المعاينة. بمجرد ان تشاهد إمكانيات جديده في مساحة عمل إدارة الميزات، يمكنك تشغيلها. قد تكون بعض الميزات قيد التشغيل بشكل افتراضي.

في بعض الأوقات، سيتم تشغيل ميزه متكاملة بشكل افتراضي ولا يمكن إيقاف تشغيلها (على سبيل المثال مساحة عمل إدارة الميزات).

وبمجرد توفر إحدى الميزات بصفه عامه، قد يتم تشغيلها أو إيقاف تشغيلها في بيئات الإنتاج. وتشير مساحة عمل إدارة الميزات إلى ان ميزه المعاينة ستصبح إلزاميه. وعاده ما يكون هذا التاريخ في يوم 1 أكتوبر أو 1 إبريل لكي تتم محاذاته مع خطط الإصدار نصف السنوية. لا يمكنك إيقاف تشغيل الميزات الإلزامية. وحتى تصبح إلزاميا، يمكنك تشغيل أحدي الميزات وإيقاف تشغيلها في كافة البيئات.

نوصي بشدة بمعاينة الميزات في بيئة الحماية أو البيئة التجريبية. من الأفضل إنشاء نسخة من بيئة الإنتاج الحالية أو قاعدة البيانات في بيئة الحماية بحيث يمكنك الحصول على التجربة الكاملة للميزات الجديدة مع الميزات الجديدة مع البيانات الخاصة بك.

لمزيد من المعلومات حول توفير بيئة حماية، راجع [توفير مشروع Human Resources](hr-admin-setup-provision.md). لإزالة بيئة اختبار، راجع [إزالة مثيل](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment). 

## <a name="report-bugs"></a>الإبلاغ عن الأخطاء

أثناء اختبار ميزات المعاينة أو تجربة إمكانيات جديدة، قد تجد عناصر لا تعمل بالشكل المتوقع. يُرجى الإبلاغ عن أي أخطاء من خلال [دعم Microsoft Dynamics 365](https://dynamics.microsoft.com/support/).

## <a name="see-also"></a>راجع أيضًا

[خطط إصدار Dynamics 365 و Power Platform](https://docs.microsoft.com/dynamics365/release-plans)</br>
[ما هو الجديد أو المتغير في Dynamics 365 Human Resources](hr-admin-whats-new.md)</br>
[سياسة دورة حياة البرامج](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy)

