---
title: الأسئلة المتداولة حول العرض المباشر
description: يسرد هذا الموضوع الأسئلة المتداولة حول كيفية القيام بالعرض المباشر باستخدام مشروع تنفيذ Dynamics 365 Human Resources.
author: rachel-profitt
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e5b0f58c7ebf03466805d20806316f6f1c32e4a4
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/04/2022
ms.locfileid: "8695349"
---
# <a name="go-live-faq"></a>الأسئلة المتداولة حول العرض المباشر 


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



يسرد هذا الموضوع الأسئلة المتداولة حول كيفية القيام بالعرض المباشر باستخدام مشروع تنفيذ Dynamics 365 Human Resources. 

## <a name="when-can-i-configure-and-request-my-production-environment"></a>متى يمكنني تكوين بيئة تشغيل وطلبها؟ 

وعادة ما يتم نشر بيئة التشغيل بعد تلبية المعايير التالية:

- تكون كافة التخصيصات كاملة الأكواد.
- تم إكمال اختبارات قبول المستخدم (UAT).
- قام العميل بتسجيل الخروج من الحل.
- لا توجد مشكلات حظر عن العرض المباشر. 

عندما يكون العملاء المؤهلين في هذه المرحلة، سيعمل فريق Microsoft FastTrack بفريق المشروع على القيام بتقييم العرض المباشر. 

## <a name="what-are-the-prerequisites-to-deploying-a-production-environment"></a>ما المتطلبات الأساسية لنشر بيئة تشغيل؟ 

للحصول على قائمة بالمتطلبات الأساسية، راجع [إعداد العرض المباشر](hr-admin-go-live-prepare.md). 

## <a name="what-is-a-go-live-assessment"></a>ما المقصود بتقييم العرض المباشر؟  

يُعد تقييم العرض المباشر جزءًا من  [برنامج Microsoft FastTrack](/dynamics365/fasttrack/). أثناء هذه المراجعة، يقيم مهندس الحلول ما إذا كان مشروع التنفيذ جاهزًا للتحول الناجح والعرض المباشر. هذه المراجعة إلزامية بالنسبة لكل مشروع تنفيذ قبل أن تتمكن من طلب العرض المباشر في بيئة التشغيل. 

## <a name="our-sandbox-environments-are-deployed-in-the-central-us-datacenter-we-want-our-production-environments-to-be-deployed-in-the-west-us-datacenter-can-i-select-west-us-as-the-datacenter-in-my-production-configuration"></a>يتم نشر بيئات الحماية في مركز بيانات وسط الولايات المتحدة. نحن نريد نشر بيئات التشغيل التابعة لنا في مركز بيانات غرب الولايات المتحدة. هل يمكنني تحديد غرب الولايات المتحدة كمركز بيانات في تكوين التشغيل؟ 

لا تقيدك خدمات LCS عن تحديد مركز بيانات مختلف عند نشر بيئة موارد بشرية، ولكننا نوصي بشدة بعدم تحديد مركز بيانات مختلف.  

إذا كنت ترغب في أن تكون بيئة التشغيل الخاصة بك في مركز بيانات غرب الولايات المتحدة، يجب أولاً إعادة نشر بيئات الحماية الخاصة بك على مركز بيانات غرب الولايات المتحدة واختبارها وتسجيل الخروج منها. 

للحصول على معلومات حول تحديد مركز البيانات الصحيح، راجع [متطلبات الشبكة](../fin-ops-core/fin-ops/get-started/system-requirements.md#network-requirements). 

## <a name="what-level-of-access-do-i-have-to-the-azure-resources-for-my-human-resources-environments"></a>ما مستوى الوصول الذي يوجد لدي لموارد Azure لبيئات الموارد البشرية الخاصة بي؟  

يقتصر الوصول إلى بيئات الموارد البشرية. لا يمكنك الوصول إلى الجهاز الظاهري (VM) أو Microsoft Internet Information Services (IIS). ولا يمكنك أيضًا الوصول إلى قاعدة البيانات عبر Microsoft SQL Server Management Studio. 

على الرغم من أنه يتعذر عليك الوصول إلى موارد Azure الخاصة بك أو بيئة Dynamics 365 Human Resources مباشرة، إلا أنه توجد ميزات إضافية يمكنك استخدامها للوصول إلى البيانات الخاصة بك:

- يمكنك نشر قاعدة بيانات Azure SQL في مستأجر Azure الخاص بك واستخدام ميزة "‏‫إحضار قاعدة بياناتك الخاصة" (BYOD) لمزامنة البيانات. لمزيد من المعلومات، راجع [إحضار قاعدة بياناتك الخاصة‬ (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md).

- يمكنك استخدام تكامل Dataverse لمزامنة تحديد الكيانات في قاعدة بيانات Dataverse. لمزيد من المعلومات، راجع [جداول Dataverse](hr-developer-entities.md). 

## <a name="how-often-is-my-production-database-backed-up"></a>كم مرة يتم نسخ قاعدة بيانات الإنتاج احتياطيًا؟ 

تتم حماية قواعد البيانات بواسطة النسخ الاحتياطي التلقائي بالتكرارات التالية:

| نوع النسخ الاحتياطي | التكرار |
| --- | --- |
| عملية النسخ الاحتياطي الكاملة لقاعدة البيانات‬ | أسبوعي |
| نسخ احتياطي تفاضلي لقاعدة بيانات | كل 12-24 ساعة |
| نسخ احتياطي لسجل الحركة | كل 5 إلى 10 دقائق |

تحتفظ Microsoft بالنسخ الاحتياطية الكافية للسماح لاستعادة النقطة الزمنية (PITR) خلال الـ 14 يومًا الماضية. 

للحصول على مزيد من المعلومات، راجع  [تعرف على عمليات النسخ الاحتياطي التلقائي لقاعدة بيانات SQL](/azure/azure-sql/database/automated-backups-overview?tabs=single-database). 

## <a name="can-i-request-a-copy-of-the-backup-of-my-production-database"></a>هل يمكنني طلب نسخة من النسخ الاحتياطي لقاعدة بيانات الإنتاج الخاصة بي؟ 

الرقم ومع ذلك، يمكنك إرسال طلب خدمة تحديث قاعدة البيانات لنسخ بيئة التشغيل الخاصة بك إلى بيئة الحماية. يمكنك نشر قاعدة بيانات Azure SQL في مستأجر Azure الخاص بك واستخدام ميزة BYOD لمزامنة البيانات من بيئة التشغيل الخاصة بك. لمزيد من المعلومات، راجع [إحضار قاعدة بياناتك الخاصة‬ (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md). 

## <a name="how-do-i-move-my-sandbox-environment-to-production-for-go-live"></a>كيف يمكنني نقل بيئة الحماية الخاصة بك إلى إنتاج العرض المباشر؟ 

ونظرًا لأن ميزة النسخ غير متاحة لنقل البيئة الخاصة بك من بيئة الحماية إلى بيئة التشغيل، فإنه يجب عليك استخدام حزم البيانات لنقل البيانات إلى بيئة التشغيل الخاصة بك.  

نوصي بالاحتفاظ بقائمة واضحة من الكيانات التي تم تكوينها في بيئة الحماية خلال المشروع. ثم اختبار عملية التكوين المرحلي وترحيل أية حزم بيانات مطلوبة للانتقال للعرض المباشر. يجب عليك نقل أية حزم بيانات يدويًا إلى بيئة التشغيل عندما تكون جاهزًا للعرض المباشر. 

## <a name="what-should-i-do-if-my-production-environment-is-down"></a>ما الذي ينبغي على فعله إذا ما توقفت بيئة التشغيل الخاصة بي؟ 

للإبلاغ عن انقطاع الإنتاج، اتبع العملية الموضحة في [الإبلاغ عن انقطاع الإنتاج](../fin-ops-core/dev-itpro/lifecycle-services/report-production-outage.md). 

 ## <a name="see-also"></a>راجع أيضًا

 [الإعداد للعرض المباشر](hr-admin-go-live-prepare.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
