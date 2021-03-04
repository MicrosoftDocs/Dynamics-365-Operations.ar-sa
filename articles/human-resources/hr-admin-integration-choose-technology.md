---
title: اختيار تقنية تكامل بيانات
description: يقدم هذا المقال معلومات حول التكامل مع البيانات المدارة بواسطة Human Resources. وهو يصف تقنيات تكامل مختلفة لمساعدتك على تحديد أفضل التقنيات التي تناسب احتياجاتك.
author: andreabichsel
manager: AnnBe
ms.date: 02/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9e6eeac66cff24d193e30aa942039707fc0aed52
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528331"
---
# <a name="choose-a-data-integration-technology"></a>اختيار تقنية تكامل بيانات

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يقدم هذا المقال معلومات للتكامل مع البيانات المدارة بواسطة Dynamics 365 Human Resources. وهو يصف تقنيات تكامل مختلفة لمساعدتك على تحديد أفضل التقنيات التي تناسب احتياجاتك.

## <a name="data-integration-background"></a>خلفية تكامل البيانات

تعتبر بيانات العمل بمثابة أصل أساسي يجعل شركتك فريدة. بيانات أعمالك ذات قيمة عالية. يمكنك استخدام العلاقات بين البيانات التي تم جمعها من خلال أعمالك لتحسين العمليات التجارية والمعلومات المهنية عبر مؤسستك. نحن نبذل جهودًا كثيرة لتوفير وصول سهل وآمن ومستقر إلى بيانات عملك بصرف النظر عن النظام الذي تأتي منه هذه البيانات.

قديمًا، كان تكامل البيانات بين الأنظمة المتعددة صعبًا.
تتخذ Microsoft خطوات لتسهيل تكامل البيانات، ولقد تحققت خطوة كبيرة نحو هذا الهدف من خلال [Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)

يعمل Human Resources على جعل Common Data Service الواجهة العامة المفضلة لبيانات Human Resources. وبمرور الوقت، فإننا نتوقع أن أهم البيانات التي تتم إدارتها بواسطة Human Resources سوف يتم عرضها في Common Data Service. نوصي بأن يكون Common Data Service هو التقنية الخاصة بالاختيار لمعظم تطبيقات التكامل.

نحن ندرك أن Common Data Service قد لا يتضمن جميع البيانات التي يحتاج إليها تطبيقك. كما ندرك أن المخطط الزمني لمشروعك قد يتطلب تقنية بديلة. احرص على إعلامنا عند يتبين لك أن Common Data Service لا يلبي متطلبات التكامل.

## <a name="integration-technologies"></a>تقنيات التكامل

تصف الأقسام التالية تقنيات تكامل البيانات المختلفة المتوفرة للاستخدام مع Human Resources.

### <a name="common-data-service-entities"></a>كيانات Common Data Service

تُعد Common Data Service هي واجهة البيانات العامة المفضلة لـ Human Resources. وقد تطور من النظام الأساسي Dynamics 365 XRM، الذي تستخدمه حلول [Dynamics 365 Customer Engagement](https://docs.microsoft.com/dynamics365/#pivot=business-apps&panel=customer-engagement).

يوفر Common Data Service نظامًا أساسيًا وواجهات API لكيانات البيانات. سوف يتصل Human Resources بمثيل Common Data Service عندما تنشره. وتنتشر كيانات بيانات Human Resources في مثيل Common Data Service هذا. تتوفر الكيانات وبياناتها لأي تطبيق يمكنه الاتصال بمثيل Common Data Service. يقوم Human Resources بمزامنة البيانات إلى كيانات Common Data Service ومنها.

عندما تكون وحدات البيانات المطلوبة من قبل تطبيقاتك التي تتكامل في Common Data Service، يمكنك أن تستخدم بشكل كامل [Common Data Service وواجهات API التي يدعمها](https://docs.microsoft.com/powerapps/#pivot=home&panel=developer). يُعد [Dynamics 365 Web API](https://docs.microsoft.com/dynamics365/customer-engagement/developer/use-microsoft-dynamics-365-web-api)من بين واجهات برمجة التطبيقات المدعومة، والتي توفر تطبيق OData للوصول إلى بيانات Common Data Service .

تعد كيانات Common Data Service وواجهات برمجة التطبيقات المرتبطة بها أفضل خيار للوصول إلى بيانات Human Resources من تطبيقات الويب وخدمات الويب / واجهات برمجة التطبيقات ومن أي تطبيق آخر يتصل بموجزات OData.

> [!NOTE]
> مع قرار جعل Common Data Service واجهة البيانات المُفضلة لـ Human Resources الحديثة نسبيًا، قد تجد أن كيانات بيانات Human Resources التي تحتاجها للتكامل غير متاحة بعد في Common Data Service.
</br>
> للحصول على قائمة بكيانات Human Resources المتاحة في Common Data Service، راجع [Human Resources وCommon Data Service](https://docs.microsoft.com/dynamics365/unified-operations/talent/corehrentities).
> </br>
> إذا لم تكن كيانات Human Resources المطلوبة للتكامل متاحة بعد، فسوف تحتاج إلى انتظار إتاحة كيانات البيانات أو استخدام إحدى تقنيات التكامل الأخرى الموضحة أعلاه.
> </br>
> بشكل افتراضي، يكون تكامل Common Data Service متوقفًا عن التشغيل في البيئات الجديدة التي لا تتضمن بيانات العرض التوضيحي المتوفرة. يتم تشغيله في بيئات جديدة تتضمن بيانات العرض التوضيحي، وتبدأ البيئات في مزامنة البيانات عند توفيرها. بعد تجهيز البيئة الخاصة بك لمزامنة البيانات، يمكنك تشغيل التكامل.

### <a name="dmfdixf-entities"></a>كيانات DMF/DIXF

تم بناء Human Resources بشكل أساسي بالاستناد إلى النظام الأساسي نفسه لتطبيقات Finance and Operations، وهو يوفر [إطار عمل إدارة البيانات (DMF)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json). ويعرف DMF أيضًا باسم إطار عمل استيراد/تصدير البيانات (DIXF). يوفر Human Resources مجموعة من كيانات البيانات التي يمكنك استخدامها لاستيراد بيانات Human Resources وتصديرها. في حين تعتبر كيانات Common Data Service واجهة تكامل البيانات المفضلة لـ Human Resources، ما زالت كيانات DMF مفيدة في بعض الحالات، مثل:

- كيانات Common Data Service غير متوفرة بعد.

- يتطلب التكامل قدرات استيراد/تصدير بيانات مجمعة عالية الأداء.

توفر كيانات DMF حاليًا تغطية البيانات الأكثر اكتمالًا لبيانات Human Resources.

لا يعتبر DMF مناسبًا لعمليات التكامل في الوقت الحقيقي، كما هو الحال عندما تحتاج إلى تعليقات المستخدم الفورية في واجهة المستخدم. وتعتبر عمليات الحزمة بمثابة وظائف دفعية مجدولة، وغالبًا ما يكون لها حد أدني من زمن الانتقال من دقيقة إلى دقيقتين قبل أن تقوم خدمه الدفعة بانتقاء الوظيفة للتنفيذ، بالإضافة إلى أي وقت يلزم لإكمال عملية الاستيراد/التصدير.‬

قد يكون خيار DMF هو الخيار الأفضل عندما تكون هناك حاجة إلى إنتاجية عالية (مثل عملية الاستيراد/التصدير المجدولة لعدة آلاف من السجلات كل ليلة).

> [!NOTE]
> لا يتوفر DMF بالنسبة إلى Attract و Onboard.

### <a name="dmf-package-rest-api"></a>واجهة تطبيق البرمجيات REST لحزمة DMF

يوفر DMF [واجهة تطبيق البرمجيات REST](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-management-api) لمعالجة حزم البيانات. يمكن استخدام واجهة برمجة التطبيقات هذه للتفاعل برمجيًا مع DMF، مما يسمح بإجراءات مثل:

- استيراد حزمة بيانات.

- تصدير حزمة بيانات.

- التحقق من حالة عملية الاستيراد / التصدير.

تكون واجهة برمجة التطبيقات REST في حزمة DMF مدعومة بشكل كامل في Human Resources: Core HR.

### <a name="azure-sql-db-byod"></a>قاعدة بيانات Azure SQL (BYOD)

يوفر DMF أيضًا ميزة فعالة (تعرف باسم [إحضار قاعدة بياناتك الخاصة](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/export-entities-to-your-own-database)، أو BYOD) التي تسمح لـ Human Resources بتصدير البيانات إلى قاعدة بيانات SQL Microsoft Azure. توفر هذه القدرة مرونة هائلة. عندما تكون البيانات موجودة في قاعدة بيانات SQL خاصة بك، يمكنك الاستفادة من أي تطبيق أو برنامج وسيط يمكنه الاتصال بمخزن بيانات SQL.

إحضار قاعدة بياناتك الخاصة (BYOD) هو بشكل أساسي حل للقراءة فقط. بينما يمكنك معالجة وتخزين أي بيانات تريدها في قاعدة بيانات Azure SQL (مثل مزج البيانات)، لن تتم مزامنة البيانات المخزنة في قاعدة بيانات SQL Azure مع Human Resources.

يُعد BYOD مناسبًا لحلول التقارير، وتكامل البيانات، ومزج البيانات، كمصدر للبيانات لتدفقات [Azure Data Factory](https://docs.microsoft.com/azure/data-factory/) .

> [!NOTE]
> لا يتوافر BYOD بالنسبة إلى Attract و Onboard.

### <a name="odata-enabled-entities"></a>كيانات OData الممكنة

يتم أيضًا تمكين معظم كيانات DMF للوصول من خلال خدمة بيانات Human Resources (OData). تنطبق الوثائق المتوفرة [Finance and Operations لخدمة OData](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/odata) على Human Resources، باستثناء ما يتعلق بإنشاء كياناتك الخاصة المكشوفة على OData.‬

في أثناء تنفيذ Common Data Service وOData الموفرة بواسطة Common Data Service (على الرغم من أن[ Web API لـ Dynamics 365](https://docs.microsoft.com/previous-versions/dynamicscrm-2016/developers-guide/mt593051(v=crm.8))) مُفضلة على خدمة بيانات Human Resources، وتحتوي خدمة بيانات Human Resources حاليًا على أكثر تغطية كيان كاملة لبيانات Human Resources.

### <a name="excel-add-in"></a>‏‫الوظيفة الإضافية لـ Excel

تقوم [الوظيفة الإضافية لـ Excel](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in?toc=/dynamics365/unified-operations/talent/toc.json) باستخدام الكيانات الممكنة لـ OData أسفل السطح. ويوفر طريقة مناسبة للمستخدم النهائي لاسترداد بيانات Human Resources وتعديلها من خلال واجهة مستخدم Excel المألوفة.

تكون الوظيفة الإضافية لـ Excel مناسبة لعمليات استيراد/تصدير البيانات المخصصة بواسطة خبراء مجال الأعمال. بالنسبة لتكامل البيانات المتكررة التي تتطلب أتمته تلقائية برمجية، سوف تكون تقنية تكامل أخرى أكثر ملائمة.

### <a name="data-integrator"></a>موحد البيانات

يمكنك استخدام [خدمة موحد البيانات](https://docs.microsoft.com/powerapps/administrator/data-integrator) لدمج البيانات إلى ومن Common Data Service. تسمح لك خدمة موحد البيانات بتحديد مشاريع التكامل ، غالبًا ما تستند إلى قوالب محددة مسبقًا صممها مطورو التطبيقات خصيصًا لتكاملات محددة. يمكن جدولة مشاريع التكامل لتعمل تلقائيًا وفقًا لجدول زمني متكرر أو تشغيلها يدويًا.

تكون مشاريع موحد البيانات مناسبة لعمليات تكامل دُفعات Common Data Service. وهي تُمثل خيارًا ممتازًا للتكاملات بين مجموعة تطبيقات Dynamics 365.‬ على سبيل المثال، توفر Microsoft قالب موحد بيانات يمكن استخدامه لدمج البيانات من Human Resources إلى Dynamics 365 Finance. يمكنك معرفة المزيد حول القالب في تكامل [من Dynamics 365 Human Resources إلى Dynamics 365 Finance](hr-admin-integration-finance.md).

### <a name="power-query"></a>Power Query

يدعم موحد البيانات [Power Query](https://docs.microsoft.com/power-query/power-query-what-is-power-query) من خلال [ميزة الاستعلام المتقدمة](https://docs.microsoft.com/powerapps/administrator/data-integrator#advanced-data-transformation-and-filtering). يوفر Power Query إمكانية تصفية وتحويل البيانات بطريقة مرنة وفعالة، بما في ذلك لغة معادلة M الغنية. من المرجح أن يكون Power Query مألوفًا لهؤلاء الذين لديهم خبرة في تطوير تقارير‏‬‏ Power BI.

## <a name="deciding-on-an-integration-technology"></a>اتخاذ قرار بشأن تقنية التكامل

ومع توافر العديد من تقنيات التكامل المختلفة، يُشكل أحيانًا اتخاذ قرار بشأن نهج التكامل المٌستخدم ضغطًا. مع اكتمال تغطية البيانات في Common Data Service، سيصبح القرار أسهل، عندما تصبح Common Data Service واجهة البيانات المفضلة في معظم الحالات. ولكن حتى ذلك الحين، قد تجد أن Common Data Service لا يلبي احتياجاتك بعد. يلخص الجدول التالي بعض الصفات المميزة الأساسية لخيارات تقنية التكامل.

| التقنية/الأداة/API    | عمليات تكامل متكررة                   | متزامن/غير متزامن                    | الوصول المبرمج من خلال API        | وحدات تخزين البيانات المناسبة                                   | تغطية البيانات                       |
|------------------------|------------------------------------------|---------------------------------------------|-------------------------------------------|------------------------------------------------------------|-------------------------------------|
| كيانات Common Data Service .           | نعم ، باستخدام موحد البيانات أو البرنامج الوسيط | مزامنة دفعة Async (من خلال موحد البيانات) | نعم، من خلال واجهة API الويب لـ Dynamics 365 (OData) | تختلف بناءً على حالة الاستخدام (تدعم الترحيل للاستخدام التفاعلي) | تحسين<sup>2</sup>                       |
| كيانات DMF           | نعم ، مجدول من خلال برنامج وسيط        | Async، دفعة                                | نعم ، خلال واجهة برمجة تطبيق REST لحزمة DMF         | عالي (مئات الآلاف من السجلات)                    | قصوى                                |
| واجهة تطبيق البرمجيات REST لحزمة DMF   | نعم ، مجدول من خلال برنامج وسيط        | Async، دفعة                                | ‏‏نعم                                       | عالي (مئات الآلاف من السجلات)                    | API تدعم كافة كيانات DMF       |
| BYOD                   | نعم، مجدولة بواسطة المسؤول في Human Resources        | Async، دفعة                                | لا<sup>3</sup>                                    | عالي (مئات الآلاف من السجلات)                    | تدعم كافة كيانات DMF           |
| كيانات OData الممكنة | نعم ، باستخدام برنامج وسيط                    | مزامنة                                        | نعم ، من خلال خدمة بيانات Human Resources (OData)  | تختلف بناءً على حالة الاستخدام (تدعم الترحيل للاستخدام التفاعلي) | قصوى                                |
| ‏‫الوظيفة الإضافية لـ Excel           | لا                                       | مزامنة                                        | لا                                        | متوسط (عشرات الآلاف من السجلات)                      | يدعم كافة كيانات OData الممكنة |
| موحد البيانات        | نعم ، مجدول في موحد البيانات        | Async، دفعة                                | لا                                        | يختلف بناءً على حالة الاستخدام                                       | يدعم كافة كيانات Common Data Service           |

<sup>2</sup>تستثمر Microsoft بشكل كبير في زيادة تغطية البيانات لكيانات Common Data Service. نوصي باستخدام Common Data Service عندما تصبح التغطية متاحة. حاليًا، تُعد تغطية البيانات في Common Data Service منخفضة مقارنة بـ DMF والكيانات الممكّنة لـ OData.

<sup>3</sup> يُمكن الوصول إلى قاعدة بيانات SQL برمجيًا.


[!INCLUDE[footer-include](../includes/footer-banner.md)]