---
title: اختر تكنولوجيا تكامل البيانات
description: يوفر هذا المقال الإرشادات حول العديد من الخيارات للتكامل مع البيانات التي تتم ادارتها بواسطة Human Resources، ويصف خصائص تقنيات التكامل المختلفة بحيث يمكن للمكاملين اتخاذ قرارات بشان أفضل التقنيات الملائمة احتياجاتهم.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: f2de5dd41c00e6546b4a4feadaf5774430d572bb
ms.sourcegitcommit: 13c4a6f98ccce243d6befde90992aefcf562bdab
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029878"
---
# <a name="choose-a-data-integration-technology"></a>اختر تكنولوجيا تكامل البيانات

يدير Dynamics 365 Human Resources بيانات الأعمال المفيدة في العديد من عمليات الأعمال. يوفر هذا المقال الإرشادات حول العديد من الخيارات للتكامل مع البيانات التي تتم ادارتها بواسطة Human Resources، ويصف خصائص تقنيات التكامل المختلفة بحيث يمكن للمكاملين اتخاذ قرارات بشان أفضل التقنيات الملائمة احتياجاتهم.

## <a name="data-integration-vision"></a>رؤية تكامل البيانات

وتري Microsoft بيانات الأعمال كأصل أساسي يجعل شركتك فريدة. بيانات أعمالك ذات قيمة عالية. تتعلق البيانات التي يتم جمعها وصيانتها بواسطة جزء من الأعمال بالبيانات التي يتم جمعها بواسطة جزء آخر من الأعمال، ويمكن استخدام هذه العلاقات لتحسين عمليات الأعمال وذكاء الأعمال في مؤسستك. يُعد توفير وصول سهل وآمن ومستقر لبيانات أعمالك، بغض النظر عن النظام "الذي يمتلك" البيانات أحد المبادئ الأساسية للرؤية التي لدينا لتكامل البيانات مع Human Resources.

قديمًا، كان تكامل البيانات بين الأنظمة المتعددة صعبًا.
تتخذ Microsoft خطوات لتسهيل تكامل البيانات، ولقد تحققت خطوة كبيرة نحو هذا الهدف من خلال [Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)

للمضي قدمًا، يعمل Human Resources على جعل Common Data Service هي الواجهة العامة المفضلة لبيانات Human Resources. وبمرور الوقت، فإننا نتوقع أن أهم البيانات التي تتم إدارتها بواسطة Human Resources سوف يتم عرضها في Common Data Service. نوصي بأن يكون Common Data Service هو التقنية الخاصة بالاختيار لمعظم تطبيقات التكامل. في حين نُدرك أن جميع البيانات التي قد يطلبها تطبيقك قد لا تكون موجودة حاليًا في Common Data Service، وأن الجداول الزمنية لمشروعك قد تتطلب تقنية بديلة، يرجى إعلامنا عندما لا يفي Common Data Service باحتياجات التكامل الخاصة بك.

## <a name="integration-technologies"></a>تقنيات التكامل

تصف الأقسام التالية تقنيات تكامل البيانات المختلفة المتوفرة للاستخدام مع Human Resources.

### <a name="common-data-service-entities"></a>كيانات Common Data Service

تُعد Common Data Service هي واجهة البيانات العامة المفضلة لـ Human Resources. تُبنى Common Data Service على نظام أساسي ناضج، نشأ من نظام أساسي Dynamics 365 “XRM”، الذي تُبنى عليه حلول [Dynamics 365 Customer Engagement](https://docs.microsoft.com/dynamics365/#pivot=business-apps&panel=customer-engagement) .

يوفر Common Data Service نظامًا أساسيًا لكيانات البيانات وAPI للوصول إلى هذه الكيانات. عند نشر "Human Resources" في مؤسستك، يتم توصيل "Human Resources" بمثيل Common Data Service ويتم نشر الكيانات التي تحتفظ ببيانات "Human Resources" في مثيل Common Data Service ، مما يجعل الكيانات وبياناتها متاحة لأي تطبيق يمكن الاتصال بمثيل Common Data Service . بناءً على تطبيقات Human Resources التي تستخدمها، يقوم Human Resources إما بأداء عمليات البيانات مباشرة في مقابل كيانات Common Data Service (هذه هي الحالة بالنسبة لـ Attract و Onboard) أو مزامنة البيانات إلى/من كيانات Common Data Service.

بمجرد وجود كيانات البيانات التي تكشف البيانات التي تتطلبها التطبيقات المدمجة في Common Data Service، يمكنك الاستفادة الكاملة من [Common Data Service وواجهات برمجة التطبيقات التي تدعمها](https://docs.microsoft.com/powerapps/#pivot=home&panel=developer) يُعد [Dynamics 365 Web API](https://docs.microsoft.com/dynamics365/customer-engagement/developer/use-microsoft-dynamics-365-web-api)من بين واجهات برمجة التطبيقات المدعومة، والتي توفر تطبيق OData للوصول إلى بيانات Common Data Service .

تعد كيانات Common Data Service وواجهات برمجة التطبيقات المرتبطة بها أفضل خيار للوصول إلى بيانات Human Resources من تطبيقات الويب وخدمات الويب / واجهات برمجة التطبيقات ومن أي تطبيق آخر يتصل بموجزات OData.

> [!NOTE]
> بقرارك جعل Common Data Service واجهة البيانات المُفضلة لـ Human Resources الحديثة نسبيًا، فقد تجد أن كيانات بيانات Human Resources التي تحتاجها للتكامل غير متاحة في Common Data Service<sup>1</sup>. إذا لم تكن كيانات Human Resources المطلوبة للتكامل متاحة بعد، فسوف تحتاج إلى انتظار إتاحة كيانات البيانات أو سوف تحتاج إلى استخدام أحد تقنيات التكامل الأخرى الموضحة أعلاه.
> 
> افتراضيًا ، يتم إيقاف تكامل Common Data Service في بيئات جديدة لا تتضمن بيانات العرض التوضيحي المُدخلة. يتم تشغيله في بيئات جديدة تتضمن بيانات العرض التوضيحي، وتبدأ البيئات في مزامنة البيانات عند توفيرها. بعد تجهيز البيئة الخاصة بك لمزامنة البيانات، يمكنك تشغيل التكامل.

<sup>1</sup>للحصول على قائمة بكيانات Human Resources المتاحة في Common Data Service، راجع [Human Resources و Common Data Service](https://docs.microsoft.com/dynamics365/unified-operations/talent/corehrentities) بالنسبة إلى Attract و Onboard، تتوفر جميع الكيانات في Common Data Service.

### <a name="dmfdixf-entities"></a>كيانات DMF/DIXF

توفر Human Resources، المبنية أساسًا على نفس النظام الأساسي مثل تطبيقات Finance and Operations ، [Data Management Framework(DMF)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)، الذي يُعرف أحيانًا أيضًا باسم إطار عمل استيراد البيانات أو DIXF، ومجموعة من كيانات البيانات التي يمكن استخدامها لاستيراد / تصدير البيانات إلى/من Human Resources. عندما تكون كيانات Common Data Service هي واجهة تكامل البيانات المفضلة لـ Human Resources، سوف تظل كيانات DMF مفيدة في بعض الحالات، مثل:

- كيانات Common Data Service غير متوفرة بعد.

- يتطلب التكامل قدرات استيراد/تصدير بيانات مجمعة عالية الأداء.

توفر كيانات DMF حاليًا تغطية البيانات الأكثر اكتمالًا لبيانات Human Resources.

يُعد DMF غير مناسبًا لعمليات الدمج في الوقت الحقيقي (على سبيل المثال: عندما تكون ملاحظات المستخدم الفورية مطلوبة في واجهة المستخدم)، نظرًا لأن عمليات الحزمة هي مهام دفعية مجدولة، وغالبًا ما يكون لها حد أدني من زمن الانتقال من 1-2 دقيقة قبل أن تقوم خدمه الدفعة بانتقاء الوظيفة للتنفيذ، بالإضافة إلى أي وقت يلزم لإكمال عملية الاستيراد/التصدير.

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

يوفر DMF أيضًا ميزة فعالة (تعرف عادةً باسم [إحضار قاعدة بياناتك الخاصة](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/export-entities-to-your-own-database)، أو BYOD) التي تسمح لـ Human Resources بتصدير البيانات إلى قاعدة بيانات SQL Microsoft Azure الخاصة بك. يوفر ذلك مرونة هائلة، لأنه عندما تكون البيانات موجودة في قاعدة بيانات SQL الخاصة بك، يمكنك الاستفادة من أي تطبيقات أو برنامج وسيط يمكنها الاتصال بمخزن بيانات SQL.

ينبغي وضع BYOD في الاعتبار كحلًا للقراءة فقط. بينما يمكنك معالجة وتخزين أي بيانات تريدها في قاعدة بيانات Azure SQL (مثل مزج البيانات)، فلن تتم مزامنة البيانات المخزنة في قاعدة بيانات SQL Azure مرة أخرى إلى Human Resources. 

يُعد BYOD مناسبًا لحلول التقارير، وتكامل البيانات، ومزج البيانات، كمصدر للبيانات لتدفقات [Azure Data Factory](https://docs.microsoft.com/azure/data-factory/) .

> [!NOTE]
> لا يتوافر BYOD بالنسبة إلى Attract و Onboard.

### <a name="odata-enabled-entities"></a>كيانات OData الممكنة

يتم أيضًا تمكين معظم كيانات DMF للوصول من خلال خدمة بيانات Human Resources (OData). وعادةً ما تنطبق أيضًا الوثائق المتوفرة لخدمة [Finance and Operations OData](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/odata)على Human Resources، على الرغم من أنه لن يتم تطبيق الوثائق المتعلقة بإنشاء كياناتك المكشوفة على OData.

في أثناء تنفيذ Common Data Service وOData الموفرة بواسطة Common Data Service (على الرغم من أن[ Web API لـ Dynamics 365](https://docs.microsoft.com/previous-versions/dynamicscrm-2016/developers-guide/mt593051(v=crm.8))) مُفضلة على خدمة بيانات Human Resources، وتحتوي خدمة بيانات Human Resources حاليًا على أكثر تغطية كيان كاملة لبيانات Human Resources.

### <a name="excel-add-in"></a>‏‫الوظيفة الإضافية لـ Excel

تقوم [الوظيفة الإضافية لـ Excel](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in?toc=/dynamics365/unified-operations/talent/toc.json) باستخدام الكيانات الممكنة لـ OData أسفل السطح. ويوفر طريقة مناسبة للمستخدم النهائي لاسترداد بيانات Human Resources وتعديلها من خلال واجهة مستخدم Excel المألوفة.

تكون الوظيفة الإضافية لـ Excel مناسبة لعمليات استيراد/تصدير البيانات المخصصة بواسطة خبراء مجال الأعمال. بالنسبة لتكامل البيانات المتكررة التي تتطلب أتمته تلقائية برمجية، سوف تكون تقنية تكامل أخرى أكثر ملائمة.

### <a name="data-integrator"></a>موحد البيانات

توفر تجربة مسؤول Common Data Service [خدمة موحد البيانات](https://docs.microsoft.com/powerapps/administrator/data-integrator) التي يمكن استخدامها لعمليات تكامل البيانات من/إلى Common Data Service. يمكن استخدام موحد البيانات لتحديد مشاريع التكامل (غالبًا ما تستند إلى قوالب محددة مسبقًا صممها مطورو التطبيقات خصيصًا لتكاملات محددة). يمكن جدولة مشاريع التكامل لتعمل تلقائيًا وفقًا لجدول زمني متكرر أو تشغيلها يدويًا.

تعد مشاريع موحد البيانات مناسبة لعمليات تكامل دُفعات Common Data Service وتُمثل خيارًا ممتازًا للتكاملات بين مجموعة تطبيقات Dynamics 365. على سبيل المثال، توفر Microsoft قالب تكامل بيانات جاهز يمكن استخدامه لدمج البيانات من Human Resources إلى Dynamics 365 Finance. للمزيد من المعلومات، راجع [التكامل من Dynamics 365 Human Resources إلى Dynamics 365 Finance](hr-admin-integration-finance.md).

### <a name="power-query"></a>Power Query

يدعم موحد البيانات أيضًا [Power Query](https://docs.microsoft.com/power-query/power-query-what-is-power-query) (من خلال [ميزة الاستعلام المتقدمة](https://docs.microsoft.com/powerapps/administrator/data-integrator#advanced-data-transformation-and-filtering)).
يوفر Power Query تصفية مرنة وفعالة للبيانات والتحويل، ويشمل ذلك لغة معادلة M الغنية، والتي ستكون على الأرجح مألوفة لهؤلاء الذين لديهم خبرة في تطوير تقارير Power BI .

## <a name="deciding-on-an-integration-technology"></a>اتخاذ قرار بشأن تقنية التكامل

ومع توافر العديد من تقنيات التكامل المختلفة، يُشكل أحيانًا اتخاذ قرار بشأن نهج التكامل المٌستخدم ضغطًا. بمرور الوقت، وبصفة خاصة مع اكتمال تغطية البيانات في Common Data Service، سيصبح القرار أسهل، حيث تكون Common Data Service هي واجهة البيانات المفضلة في معظم الحالات. ولكن حتى ذلك الحين، قد تجد أن Common Data Service لا يلبي احتياجاتك بعد. يساعد الجدول التالي في تلخيص بعض الصفات المميزة الأساسية لخيارات تقنيات التكامل المختلفة.

| التقنية/الأداة/API    | عمليات تكامل متكررة                   | متزامن/غير متزامن                    | الوصول المبرمج من خلال API        | وحدات تخزين البيانات المناسبة                                   | تغطية البيانات                       |
|------------------------|------------------------------------------|---------------------------------------------|-------------------------------------------|------------------------------------------------------------|-------------------------------------|
| كيانات Common Data Service .           | نعم ، باستخدام موحد البيانات أو البرنامج الوسيط | مزامنة دفعة Async (من خلال موحد البيانات) | نعم، من خلال واجهة API الويب لـ Dynamics 365 (OData) | تختلف بناءً على حالة الاستخدام (تدعم الترحيل للاستخدام التفاعلي) | تحسين<sup>2</sup>                       |
| كيانات DMF           | نعم ، مجدول من خلال برنامج وسيط        | Async، دفعة                                | نعم ، خلال واجهة برمجة تطبيق REST لحزمة DMF         | عالي (مئات الآلاف من السجلات)                    | قصوى                                |
| واجهة تطبيق البرمجيات REST لحزمة DMF   | نعم ، مجدول من خلال برنامج وسيط        | Async، دفعة                                | ‏‏نعم                                       | عالي (مئات الآلاف من السجلات)                    | API تدعم كافة كيانات DMF       |
| BYOD                   | نعم، مجدولة بواسطة المسؤول في Human Resources        | Async، دفعة                                | لا<sup>3</sup>                                    | عالي (مئات الآلاف من السجلات)                    | تدعم كافة كيانات DMF           |
| كيانات OData الممكنة | نعم ، باستخدام برنامج وسيط                    | مزامنة                                        | نعم ، من خلال خدمة بيانات Human Resources (OData)  | تختلف بناءً على حالة الاستخدام (تدعم الترحيل للاستخدام التفاعلي) | قصوى                                |
| ‏‫الوظيفة الإضافية لـ Excel           | لا                                       | مزامنة                                        | لا                                        | متوسط (عشرات الآلاف من السجلات)                      | يدعم كافة كيانات OData الممكنة |
| موحد البيانات        | نعم ، مجدول في موحد البيانات        | Async، دفعة                                | لا                                        | يختلف بناءً على حالة الاستخدام                                       | يدعم كافة كيانات Common Data Service           |

<sup>2</sup> تستثمر Microsoft بشكل كبير في زيادة تغطية البيانات لكيانات Common Data Service، وتوصي بـ Common Data Service باعتبارها واجهة البيانات المفضلة عند توفر التغطية. حاليًا، تُعد تغطية البيانات في Common Data Service منخفضة مقارنة بـ DMF والكيانات الممكنة لـ OData.

<sup>3</sup> يُمكن الوصول إلى قاعدة بيانات SQL برمجيًا.

## <a name="summary"></a>ملخص

تمثل بيانات أعمالك أصلًا قميًا، ولكن يُمكن أن تقل هذه القيمة إلى حد كبير إذا كان من الصعب استخدام البيانات لأغراض معينة (مثل إعداد التقارير أو مزج البيانات أو تخصيص التطبيقات). يوفر Dynamics 365 Human Resources العديد من التقنيات للعمل باستخدام البيانات خارج واجهة مستخدم تطبيق Human Resources (UI)، مما يسمح بتكامل التطبيقات للوصول إلى البيانات. وضح هذا الموضوع تقنيات التكامل المتوفرة وبعضًا من خصائصها الرئيسية. وينبغي أن تساعدك هذه المعلومات على اتخاذ قرارات أفضل فيما يتعلق بالمناهج التي يتعين تحسينها لمشاريعك المتكاملة.

