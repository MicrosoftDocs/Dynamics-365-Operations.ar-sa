---
title: أسئلة شائعة حول دمج البنية الأساسية لـ Dynamics 365 Human Resources
description: يجيب هذا الموضوع على الأسئلة المتداولة حول دمج البنية التحتية لتطبيقي Microsoft Dynamics 365 Human Resources وFinance and Operations.
author: rachel-profitt
ms.date: 07/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fee4fea9b67ff8a0c8d813940a65cf882bd13abe
ms.sourcegitcommit: bf2daeccbe3f2826e734f409bfc823820144aa23
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/15/2021
ms.locfileid: "6617981"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-faq"></a>أسئلة شائعة حول دمج البنية الأساسية لـ Dynamics 365 Human Resources

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يجيب هذا الموضوع على الأسئلة المتداولة حول دمج البنية التحتية لتطبيقي Microsoft Dynamics 365 Human Resources وFinance and Operations.

## <a name="what-is-the-dynamics-365-human-resources-infrastructure-merge"></a>ما هو دمج البنية الأساسية لـ Dynamics 365 Human Resources؟

Dynamics 365 Human Resources هو تطبيق مستقل يستخدم بنية أساسية مختلفة عن تطبيقات Finance and Operations الأخرى، مثل Dynamics 365 Finance وDynamics 365 Supply Chain Management وDynamics 365 Commerce وDynamics 365 Project Operations. سيجلب دمج البنية الأساسية لـ Dynamics 365 Human Resources إلى نفس البنية الأساسية مثل تطبيقات Finance and Operations الأخرى.

## <a name="value-and-benefits-of-the-infrastructure-merge"></a>قيمة وفوائد دمج البنية الأساسية

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-what-benefits-will-we-see-from-these-changes"></a>تستخدم المؤسسة Dynamics 365 Human Resources لإدارة عمليات الموارد البشرية الخاصة بها. ما هي الفوائد التي سنراها من هذه التغييرات؟

- هذه التغييرات تزيل مجموعات متعددة من قدرات الموارد البشرية (الموارد البشرية) في Dynamics 365.
- فهي توفر Microsoft Power Platform كلا من القابلية للتوسعة، وطريقة لتوسيع منطق العمل وخيارات الميزة.
- فهي تحقق الاتساق بين Dynamics 365 Human Resources وتطبيقات Finance and Operations أخرى من حيث إدارة دورة حياة التطبيق (ALM) وMicrosoft Dynamics Lifecycle Services (LCS) والتوافر الجغرافي والقابلية للتوسعة وغيرها.
- فهي تتيح لك الاستفادة من الخدمات والأدوات المشتركة، وتساعد على تقليل التكاليف.

### <a name="my-organization-uses-dynamics-365-human-resources-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-benefits-will-we-see-from-these-changes"></a>تستخدم المؤسسة Dynamics 365 Human Resources في Dynamics 365 Finance، Supply Chain Management أو Commerce، أو Project Operations. ما هي الفوائد التي سنراها من هذه التغييرات؟

وستكون القدرات والاستثمارات التي تم إجراؤها Dynamics 365 Human Resources متاحة الآن للعملاء الذين يستخدمون وحدة الموارد البشرية في Dynamics 365 Finance. وتشمل بعض هذه القدرات إدارة الإجازات والغياب، وإدارة الاستحقاقات، وإدارة المهام.

### <a name="will-i-lose-any-features-or-capabilities-that-i-currently-use"></a>هل سأفقد أي ميزات أو قدرات أستخدمها حاليا؟

سيكون هناك تكافؤ وظيفي بين Dynamics 365 Human Resources وحدة الموارد البشرية في تطبيقات Finance and Operations. Dynamics 365 Human Resources سوف تأخذ الأسبقية لميزات مفضلة. لمزيد من المعلومات، راجع [‏‫نظرة عامة على إدارة الميزات](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="will-the-experience-change-for-my-users"></a>هل ستتغير التجربة بالنسبة للمستخدمين؟

ستتم إدارة قدرات الموارد البشرية الجديدة من خلال إدارة الميزات. سيقرر العملاء ما إذا كانوا يرغبون في استيعابها. في بعض الحالات، قد يتم تعديل القدرات. وفي هذه الحالات، ستقدم الوثائق.

### <a name="how-does-this-change-affect-me-if-i-am-an-existing-customer-and-i-use-both-the-hr-module-on-the-finance-and-operations-infrastructure-and-dynamics-365-human-resources-through-custom-integrations"></a>كيف يؤثر هذا التغيير علي إذا كنت عميلا موجودا، وكنت أستخدم كلا من وحدة الموارد البشرية في البنية الأساسية لـ Finance and Operations وDynamics 365 Human Resources ومن خلال عمليات التكامل المخصصة؟

لن تكون هناك حاجة إلى عمليات تكامل مخصصة بين Dynamics 365 Human Resources الوحدة النمطية للموارد البشرية في Dynamics 365 Finance. ستتواجد جميع بيانات الموارد البشرية في نفس قاعدة البيانات مثل تطبيقات Finance and Operations الأخرى.

## <a name="migration-from-dynamics-365-human-resources-to-finance-and-operations-apps"></a>الترحيل من Dynamics 365 Human Resources إلى تطبيقات Finance and Operations

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-hr-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>تستخدم مؤسستي Dynamics 365 Human Resources لإدارة عمليات الموارد البشرية الخاصة بها. ما الذي يجب أن نخطط له للهجرة إلى التجربة الجديدة؟

إذا كانت مؤسستك تستخدم Dynamics 365 Human Resources ولكنها لا تستخدم أي تطبيقات Finance and Operations أخرى، سيتم ترحيل بيئة الموارد البشرية إلى البنية التحتية الجديدة. وسيتم أتمتة جزء كبير من عملية الترحيل هذه. ستكون العمليات في مكان لترحيل قاعدة البيانات ومزامنتها مع البنية الأساسية الجديدة.

بالإضافة إلى ذلك، سيتم وضع الأدوات بحيث يمكنك اختبار عملية الترحيل والتحقق من صحة البيانات والخبرة قبل ترحيل بيئة التشغيل الخاصة بك.

إذا كانت مؤسستك تستخدم Dynamics 365 Human Resources وتطبيقات Finance and Operations  الأخرى، فعليك التخطيط لمزيد من الوقت للتحقق من الصحة لضمان ترحيل بياناتك بشكل صحيح إلى البيئة الجديدة. سوف يترتب على الترحيل إلى البنية الأساسية الجديدة دمج البيانات من بيئة الموارد البشرية مع بيئة Finance and Operations الخاصة بك. وسوف تكون الأدوات في مكان لأتمتة بقدر ما يمكن عملية دمج البيانات. ومع ذلك، تتطلب مثيلات البيانات المتعارضة إدخال المستخدم لتحديد كيفية حل التعارض. سيتعين على المستخدمين والمسؤولين إدارة تعيينات البيانات حيث توجد تعارضات واختبار الترحيل في بيئات وضع الحماية قبل ترحيل بيئة التشغيل الخاصة بك.

### <a name="my-organization-uses-dynamics-365-human-resources-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>تستخدم المؤسسة Dynamics 365 Human Resources في Dynamics 365 Finance، Supply Chain Management أو Commerce، أو Project Operations. ما الذي يجب أن نخطط له للهجرة إلى التجربة الجديدة؟

بالنسبة للمؤسسات التي تستخدم وحدة الموارد البشرية في تطبيقات Finance and Operations، سيتم تطبيق وظيفة الميزة الجديدة من Dynamics 365 Human Resources على البيئة الخاصة بك من خلال عملية تحديث الإصدار الواحد القياسية. يمكنك توقع رؤية الوظيفة الجديدة في البيئة الخاصة بك كما تصبح متوفرة في كل تحديث. يمكنك استخدام إدارة الميزات لتشغيل الميزات الجديدة. ومع ذلك، يجب أن تخطط للتحقق من صحة هذه الميزات. اتبع العمليات التي لديك في مكان للتحقق من صحة التحديثات الأخرى إلى البيئة الخاصة بك. لمزيد من المعلومات حول كيفية تطبيق التحديثات على تطبيقات Finance and Operations، راجع [نظرة عامة على إصدار واحد](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="when-will-my-organization-be-migrated"></a>متى سيتم ترحيل المؤسسة الخاصة بي؟

يعتمد الترحيل لكل مؤسسة على التكوين الحالي والاستعداد للانتقال إلى البنية الأساسية الجديدة. هذه التواريخ عرضة للتغيير.

- ستتلقى المؤسسات التي تستخدم حاليا وحدة الموارد البشرية في تطبيقات Finance and Operations وظيفة الموارد البشرية لـ Dynamics 365 Human Resources كجزء من عملية تحديث الإصدار الواحد العادية. ومن المقرر أن تصبح الميزات الجديدة متاحة بشكل عام ابتداء من أكتوبر 2021.
- وستتاح للمؤسسات التي تستخدم حاليا فقط Dynamics 365 Human Resources إمكانية الوصول إلى أدوات الترحيل حتى تتمكن من بدء اختبار الترحيل وبدءه في منتصف عام 2022. لم يتم بعد تحديد تاريخ إتمام الترحيل إلى البنية الأساسية الجديدة. ومع ذلك، سيكون على الأقل سنة واحدة بعد التاريخ عندما تصبح أدوات الترحيل متوفرة.
- وستتاح للمؤسسات التي تستخدم حاليا فقط Dynamics 365 Human Resources و تطبيقات Finance and Operations الأخرى إمكانية الوصول إلى أدوات الترحيل حتى تتمكن من بدء اختبار الترحيل وبدءه في منتصف عام 2022. لم يتم بعد تحديد تاريخ إتمام الترحيل إلى البنية الأساسية الجديدة. ومع ذلك، سيكون على الأقل سنة واحدة بعد التاريخ عندما تصبح أدوات الترحيل متوفرة.

لمزيد من المعلومات حول الميزات الجديدة لـ Dynamics 365 Human Resources، راجع [ما الجديد أو الذي تم تغييره في الموارد البشرية](./hr-admin-whats-new.md).

### <a name="i-am-using-new-capabilities-that-are-available-only-in-dynamics-365-human-resources-such-as-leave-and-absence-and-benefits-management-will-these-capabilities-now-be-available-in-the-human-resources-module-on-the-finance-and-operations-infrastructure-too"></a>أنا أستخدم قدرات جديدة متوفرة فقط في Dynamics 365 Human Resources (مثل **إجازة والغياب** و **إدارة الفوائد**). هل ستتوفر هذه القدرات الآن في وحدة الموارد البشرية المتعلقة بالبنية الأساسية لـ Finance and Operations أيضا؟

نعم، ستعمل جميع الوحدات من Dynamics 365 Human Resources كما هي في تطبيقات Finance and Operations، وسيكون هناك تكافؤ ميزة بنسبة 100 في المائة. كجزء من استراتيجية الترحيل الشاملة للعملاء الذين يستخدمون هذه القدرات حاليا في الموارد البشرية، سيتم ترحيل بيانات العملاء بحيث تستمر في العمل على البنية الأساسية لـ Finance and Operations.

### <a name="i-use-the-new-dynamics-365-human-resources-benefits-management-capabilities-ive-built-custom-integrations-with-the-hr-module-on-the-finance-and-operations-infrastructure-so-that-i-can-take-advantage-of-the-payroll-capabilities-by-using-benefits-data-will-these-custom-integrations-be-required-going-forward"></a>يمكنني استخدام قدرات إدارة فوائد Dynamics 365 Human Resources الجديدة. لقد بنيت التكامل المخصص مع وحدة الموارد البشرية على البنية الأساسية Finance and Operations حتى أتمكن من الاستفادة من قدرات الرواتب باستخدام بيانات الفوائد. هل ستكون هذه التكاملات المخصصة مطلوبة للمضي قدما؟

كجزء من دمج البنية الأساسية، يتم إحضار بيانات الموارد البشرية إلى نفس قاعدة البيانات مثل تطبيقات Finance and Operations الأخرى. لن يكون التكامل بين الوحدات النمطية في تطبيقات Finance and Operations مطلوبا بعد الآن.

### <a name="my-organization-uses-one-or-more-isv-solutions-with-dynamics-365-human-resources-will-our-isv-solutions-be-migrated-automatically"></a>تستخدم المؤسسة الخاصة بي حل ISV واحد أو أكثر مع Dynamics 365 Human Resources. هل سيتم ترحيل حلول ISV تلقائيا؟

تختلف تجربة الترحيل لكل مورد برامج مستقل (ISV) الحل، اعتمادا على أسلوب التكامل للحل. ستعمل Microsoft بشكل وثيق مع ISVs لضمان الانتقال السلس إلى البنية الأساسية الجديدة.

### <a name="my-organization-uses-linkedin-talent-hub-integration-with-dynamics-365-human-resources-will-this-integration-continue-to-work-after-the-infrastructure-change-is-completed"></a>تستخدم منظمتي تكامل LinkedIn Talent Hub مع Dynamics 365 Human Resources. هل سيستمر هذا التكامل في العمل بعد اكتمال تغيير البنية الأساسية؟

نعم، سيستمر تكامل مركز المواهب في LinkedIn في العمل بعد الترحيل إلى البنية الأساسية الجديدة.

### <a name="my-organization-uses-the-human-resources-app-for-teams-will-the-app-continue-to-work-after-the-infrastructure-change-is-completed"></a>تستخدم منظمتي تطبيق الموارد البشرية لـ Teams. هل سيستمر هذا التطبيق في العمل بعد اكتمال تغيير البنية الأساسية؟

نعم، سيستمر تطبيق الموارد البشرية في العمل بعد الترحيل إلى البنية الأساسية الجديدة.

### <a name="my-organization-has-configured-custom-security-in-dynamics-365-human-resources-will-our-custom-security-still-be-applied-after-the-infrastructure-change-is-completed"></a>قامت مؤسستي بتكوين أمان مخصص في Dynamics 365 Human Resources. هل سيظل أماننا المخصص مطبقا بعد اكتمال تغيير البنية الأساسية؟

نعم، سيتم تضمين تكوينات الأمان المخصصة في ترحيل البيانات إلى البنية الأساسية الجديدة.

### <a name="we-are-using-data-integrator-to-move-data-between-dynamics-365-human-resources-and-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected"></a>نحن نستخدم "تكامل البيانات" لنقل البيانات بين تطبيقي Dynamics 365 Human Resources وFinance and Operations. كيف ستتأثر البيانات التي يتم دمجها حاليا؟

تتم مزامنة بيانات الموارد البشرية التي يتم إتقانها حاليا في Dynamics 365 Human Resources مع Dataverse. يمكن بعد ذلك استخدام "تكامل البيانات" للتزامن أحادي الاتجاه مع تطبيقات Finance and Operations. بعد الترحيل إلى البنية الأساسية الجديدة، ستكون بيانات الموارد البشرية أصلية في تطبيقات Finance and Operations. لن تكون هناك حاجة إلى تكامل البيانات لمزامنة البيانات بين تطبيقات Finance and Operations والموارد البشرية.

ستستمر جداول البيانات الأصلية Dataverse الحالية للموارد البشرية في مزامنة البيانات من البيئة على البنية الأساسية الجديدة. سيتم تحويل الكيانات لدعم الكتابة المزدوجة. أي تكاملات بيانات أخرى تم تكوينها عبر "تكامل البيانات" مقابل هذه الجداول لتطبيقات Dynamics 365 الأخرى ستستمر في العمل كما تم تكوينها حاليا.

### <a name="we-are-using-dual-write-to-move-hr-data-between-dataverse-and-other-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected-by-the-migration-to-the-new-infrastructure"></a>نحن نستخدم الكتابة المزدوجة لنقل بيانات الموارد البشرية بين تطبيقات Dataverse وتطبيقات Finance and Operations الأخرى. كيف ستتأثر البيانات التي يجري دمجها حاليا بالهجرة إلى البنية الأساسية الجديدة؟

ستكون بيانات الموارد البشرية أصلية في تطبيقات Finance and Operations على البنية الأساسية الجديدة. ثم سيتم استخدام الكتابة المزدوجة لنقل بيانات الموارد البشرية بين البيئة الجديدة وبيئة Dataverse.

### <a name="we-have-built-custom-integrations-from-dynamics-365-human-resources-to-one-or-more-external-systems-will-we-have-to-develop-new-integrations-after-the-infrastructure-change-is-completed"></a>لقد بنينا تكاملات مخصصة من Dynamics 365 Human Resources إلى نظام خارجي واحد أو أكثر. هل سنستمر في تطوير التكامل الجديد بعد اكتمال تغيير البنية الأساسية؟

يعتمد ذلك على نقطة نهاية التكامل. لمزيد من المعلومات حول تقنيات التكامل المتوفرة في تطبيقات Finance and Operations، وكيفية اختيار أفضل تقنية تكامل، راجع [نظرة عامة على التكامل](../fin-ops-core/dev-itpro/data-entities/integration-overview.md).

### <a name="we-have-extended-dataverse-for-dynamics-365-human-resources-will-these-extensions-be-migrated-automatically"></a>لقد مددنا Dataverse لـ Dynamics 365 Human Resources. هل سيتم ترحيل هذه التمديدات تلقائيا؟

إذا كانت بيئات Dynamics 365 Human Resources وFinance and Operations التي سيتم ربطها في البيئة على البنية الأساسية الجديدة متصلة بنفس بيئة Dataverse، سيستمر اتصال التطبيقين بنفس بيئة Dataverse بعد الترحيل. لذلك، لا يلزم ترحيل أي ملحقات Dataverse.

لكن، إذا كانت بيئات Dynamics 365 Human Resources وFinance and Operations مرتبطة حاليًا ببيئات Dataverse منفصلة، سيستمر ربط بيئتي Dataverse بحيث يستمر الارتباط ببيئة واحدة على البنية الأساسية. لترحيل Dataverseهذا، يمكن توصيل جداول Dataverse القياسية إلى حلول الموارد البشرية وإعادة مزامنتها مع بيئة Dataverse الجديدة. ومع ذلك، لن يتم ترحيل أي ملحقات لبيئة Dataverse تلقائيا ولكن يجب إعادة نشرها في البيئة الجديدة. نوصي باستخدام الحلول المدارة لإدارة إضافات Dataverse. لمزيد من المعلومات، راجع [مقدمة للحلول](https://docs.microsoft.com/powerapps/developer/data-platform/introduction-solutions).

### <a name="we-have-configured-microsoft-power-automate-flows-andor-microsoft-power-apps-to-work-with-dynamics-365-human-resources-will-these-microsoft-power-platform-components-be-migrated-and-work-automatically-after-the-infrastructure-change-is-completed"></a>لقد قمنا بتكوين تدفقات Microsoft Power Automate و/أو Microsoft Power Apps للعمل مع Dynamics 365 Human Resources. هل سيتم ترحيل مكونات Microsoft Power Platform هذه والعمل تلقائيا بعد اكتمال تغيير البنية الأساسية؟

تدفقات Power Apps، Power Automate، وتخصيصات Microsoft Power Platform الأخرى مشابهة لإضافات Dataverse. يعتمد ما إذا كانت تعمل تلقائيا بعد الترحيل إلى البنية الأساسية الجديدة على ما إذا كان تطبيق الموارد البشرية وتطبيقات Finance and Operations متصلين بنفس بيئة Power Apps قبل الترحيل.

إذا كانت التطبيقات متصلة حاليا بنفس بيئة Power Apps، فسيستمر اتصالها ببيئة Power Apps تلك بعد الترحيل إلى البنية الأساسية الجديدة. في هذه الحالة، سوف تستمر عمليات التدفق Power Apps, Power Automate وتخصيصات Microsoft Power Platform الأخرى في العمل بدون أي تكوين إضافي. نوصي باستخدام الحلول المدارة لإدارة إضافات التطبيقات على Dataverse. لمزيد من المعلومات، راجع [مقدمة للحلول](https://docs.microsoft.com/powerapps/developer/data-platform/introduction-solutions).

ومع ذلك، إذا كان تطبيق الموارد البشرية وتطبيقات Finance and Operations متصلين ببيئات Power Apps منفصلة، يجب دمجهما كجزء من الترحيل. تتطلب هذه المهمة إعادة توزيع Power Apps والتخصيصات الأخرى في البيئة الجديدة.

### <a name="we-have-enabled-dataverse-virtual-tables-for-dynamics-365-human-resources-what-will-happen-to-these-tables-during-the-migration"></a>لقد قمنا بتمكين جداول Dataverse ظاهرية لـ Dynamics 365 Human Resources. ماذا سيحدث لهذه الجداول أثناء الترحيل؟

بعد الترحيل، إذا ظلت البيئة على البنية التحتية الجديدة متصلة ببيئة Dataverse المتصلة حاليا بـ Dynamics 365 Human Resources، فإن جداول Dataverse الظاهرية التي تم إنشاؤها في تلك البيئة ستستمر في العمل بدون أي تكوين إضافي.

ومع ذلك، إذا كانت البيئة على البنية الأساسية الجديدة متصلة ببيئة Dataverse مختلفة بعد الترحيل، يجب إعادة إنشاء الجداول الظاهرية في بيئة Dataverse الجديدة.

### <a name="we-have-developed-an-integration-by-using-the-applicant-tracking-system-ats-api-payroll-api-dataverse-virtual-tables-for-dynamics-365-human-resources-or-other-entities-in-the-dataverse-web-api-will-these-integrations-continue-to-work-after-the-infrastructure-change-is-completed"></a>لقد قمنا بتطوير تكامل باستخدام واجهة برمجة تطبيقات نظام تتبع المتقدمين (ATS) أو واجهة برمجة تطبيقات الرواتب والجداول Dataverse الافتراضية لـ Dynamics 365 Human Resources ، أو كيانات أخرى في واجهة برمجة تطبيقات الويب لـ Dataverse. هل ستستمر هذه التكاملات في العمل بعد اكتمال تغيير البنية الأساسية؟

بعد الترحيل، إذا ظلت البيئة على البنية التحتية الجديدة متصلة ببيئة Dataverse المتصلة حاليا بـ Dynamics 365 Human Resources، فإن أية تكاملات تم تطويرها بناء على واجهة برمجة تطبيقات الويب لـ Dataverse ستستمر في العمل بعد انتهاء التكامل.

لكن، إذا ظلت البيئة على البنية التحتية الجديدة متصلة ببيئة Dataverse مختلفة بعد الترحيل، فإن أية تكاملات تم تطويرها بناء على واجهة برمجة تطبيقات الويب لـ Dataverse ستحتاج إلى إعادة تكوين لتتصل ببيئة Dataverse الجديدة.

### <a name="is-there-an-impact-on-the-azure-region-when-my-environment-is-migrated"></a>هل هناك تأثير على منطقة Azure عند ترحيل البيئة الخاصة بي؟

من المتوقع أن تبقى بيئة الموارد البشرية الخاصة بك عادة في نفس المنطقة Azure أثناء الترحيل. يحدث الاستثناء الوحيد إذا سيتم دمج بيئة الموارد البشرية مع بيئة Finance and Operations في منطقة مختلفة. في هذه الحالة، سيتم ترحيل بيئة الموارد البشرية إلى منطقة Azure في بيئة Finance and Operations.

### <a name="my-organization-depends-on-workflows-in-dynamics-365-human-resources-for-one-or-more-business-processes-will-the-workflows-be-migrated-automatically"></a>تعتمد مؤسستي على مهام سير العمل في Dynamics 365 Human Resources لعملية عمل واحدة أو أكثر. هل سيتم ترحيل عمليات سير العمل هذه تلقائيا؟

نعم، سيتم ترحيل تكوينات سير العمل ومحفوظات سير العمل وسير العمل الحالي قيد التنفيذ.

### <a name="what-training-and-resources-will-be-available-to-help-with-the-migration-process"></a>ما التدريب والموارد التي ستتوفر للمساعدة في عملية الترحيل؟

سيتم توفير الوثائق الكاملة لوصف كل خطوة من عملية الترحيل بالتفصيل. وقد تتوفر أيضا موارد تدريبية إضافية، مثل أشرطة الفيديو وحلقات العمل، حسب الحاجة.

### <a name="my-organization-has-created-saved-views-in-dynamics-365-human-resources-to-improve-the-usability-of-the-interface-will-the-saved-views-be-migrated-automatically"></a>أنشأت المؤسسة طرق عرض Dynamics 365 Human Resources محفوظة لتحسين قابلية استخدام الواجهة. هل سيتم ترحيل طرق العرض المحفوظة هذه تلقائيا؟

نعم، سيتم ترحيل طرق العرض المحفوظة إلى البنية الأساسية الجديدة.

### <a name="we-are-using-ceridian-with-dynamics-365-human-resources-will-the-ceridian-integration-be-available-after-the-infrastructure-change-is-completed"></a>نحن نستخدم Ceridian مع Dynamics 365 Human Resources. هل سيستمر تكامل Ceridian هذا متاحًا بعد اكتمال تغيير البنية الأساسية؟ 

سيتم ترحيل التكامل مع Ceridian إلى التكامل المستندة إلى واجهة برمجة التطبيقات الرواتب. لن يتم ترحيل التكامل المستند إلى الملفات الموجود حاليا في Dynamics 365 Human Resources إلى بنية Finance and Operations أساسية. لمزيد من المعلومات، راجع [مقدمة لواجهة برمجة تطبيقات كشف الرواتب](./hr-admin-integration-payroll-api-introduction.md).

### <a name="how-will-the-migration-affect-the-service-update-process"></a>كيف ستؤثر عملية الترحيل على عملية تحديث الخدمة؟

بعد الترحيل، سيكون لدى العملاء مرونة أكبر بكثير من حيث ALM وتحديثات الخدمة. لن يتم تطبيق تحديثات الخدمة تلقائيا على بيئات الموارد البشرية. بدلا من ذلك، ستتبع الخدمة عمليات تحديث خدمة الإصدار واحد والوظائف. لذلك، ستكون خيارات التكوين للتحديثات متوفرة من خلال LCS. لمزيد من المعلومات، راجع [نظرة عامة حول One Version](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="how-will-the-migration-affect-my-lcs-project-for-dynamics-365-human-resources"></a>كيف ستؤثر الهجرة على مشروع LCS الخاص بي لـ Dynamics 365 Human Resources؟

الترحيل إلى البنية الأساسية الجديدة سينقل إدارة بيئات Dynamics 365 Human Resources إلى مشروع تنفيذ LCS. إذا تم دمج ترحيل Dynamics 365 Human Resources مع بيئة Finance and Operations موجودة، سيتم دمج مشروع LCS للموارد البشرية في مشروع تطبيق LCS لتطبيق Finance and Operations. إذا كنت تستخدم Dynamics 365 Human Resources حاليا فقط، سيتم إنشاء مشروع تنفيذ LCS جديد، وسيتم ترحيل مشروع LCS للموارد البشرية الحالي إلى المشروع الجديد.

سيكون المشروع الجديد هو نفس نوع المشروع الذي تستخدمه تطبيقات Finance and Operations. وسوف يكون لها نفس الميزات والوظائف لإدارة البيئة. للحصول على مزيد من المعلومات، راجع [موارد Lifecycle Services](../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

### <a name="we-have-linked-our-task-recordings-to-the-business-process-modeler-in-human-resources-how-will-the-business-process-modeler-be-migrated-and-merged-into-lcs"></a>لقد ربطنا تسجيلات مهامنا بأداة تكوين عمليات الأعمال في الموارد البشرية. كيف سيتم ترحيل "أداة تكوين عمليات الأعمال" ودمجه في LCS؟

سيتم ترحيل مكتبات العمليات التجارية لمشروع LCS إلى مشروع LCS الجديد للموارد البشرية.

### <a name="my-organization-currently-uses-only-dynamics-365-human-resources-what-resources-are-available-so-that-we-can-learn-more-about-the-development-capabilities-after-the-infrastructure-change-is-completed"></a>تستخدم المؤسسة حاليا فقط Dynamics 365 Human Resources. ما هي الموارد المتاحة حتى نتمكن من معرفة المزيد عن قدرات التطوير بعد اكتمال تغيير البنية الأساسية؟

وستكون خيارات القابلية للتوسعة Microsoft Power Platform وخيارات القابلية للتوسعة Finance and Operations متاحة ويمكن استخدامها لأغراض التطوير. لمزيد من المعلومات، راجع [تطوير الصفحة الرئيسية وتخصيصها](../fin-ops-core/dev-itpro/dev-tools/developer-home-page.md).

### <a name="we-have-enabled-features-in-dynamics-365-human-resources-will-these-features-be-enabled-automatically-during-the-migration"></a>لقد قمنا بتمكين الميزات في Dynamics 365 Human Resources. هل سيتم تمكين هذه الميزات تلقائيا أثناء الترحيل؟

سيتم تحديد ما إذا كان يتم تمكين ميزة تلقائيا في البنية الأساسية الجديدة بشكل فردي لكل ميزة. سيتم تضمين هذه المعلومات في وثائق الميزة.

### <a name="what-happens-to-my-byod-database-during-the-migration"></a>ماذا يحدث لقاعدة بيانات BYOD الخاصة بي أثناء الترحيل؟

استيراد وتصدير التكوينات لإحضار قاعدة البيانات الخاصة بك (BYOD) سيتم ترحيلها إلى البنية الأساسية الجديدة.

### <a name="what-happens-to-my-azure-data-lake-during-the-migration"></a>ماذا يحدث لـ Azure Data Lake الخاص بي أثناء الترحيل؟

أي تصدير يتم تكوينه حاليا لـ Azure Data Lake Storage في تطبيقات Finance and Operations سيحافظ على نفس التكوين بعد الترحيل.

### <a name="we-are-currently-using-dynamics-ax-2012-will-the-upgrade-tools-that-are-currently-available-be-used-to-upgrade-the-hr-module-in-ax-2012-to-dynamics-365-human-resources"></a>نحن نستخدم حاليا Dynamics AX 2012. هل سيتم استخدام أدوات الترقية المتوفرة حاليا لترقية وحدة الموارد البشرية في AX 2012 إلى Dynamics 365 Human Resources؟

نعم. سيتم دمج Dynamics 365 Human Resources في قاعدة التعليمات البرمجية المدمجة والبنية الأساسية لتطبيقات Finance and Operations. سوف تستخدم الترقية من Dynamics AX 2012 إلى Dynamics 365 Human Resources نفس مسار الترقية والأدوات المستخدمة للترقية إلى أحدث إصدار من تطبيقات Finance and Operations.

### <a name="we-use-document-handling-with-dynamics-365-human-resources-what-will-happen-to-the-documents-during-the-migration"></a>نحن نستخدم معالجة المستندات مع Dynamics 365 Human Resources. ماذا سيحدث للمستندات أثناء الترحيل؟

ستبقى المستندات في مخزن المستندات الموجود. وسيتم إعادة تشكيلها للبيئة في البنية الأساسية الجديدة.

### <a name="what-happens-to-the-batch-jobs-that-we-have-configured-in-dynamics-365-human-resources-after-the-migration"></a>ماذا يحدث لوظائف الدفعة التي قمنا بتكوينها في Dynamics 365 Human Resources بعد الترحيل؟

سيتم ترحيل مهام الدفعات القابلة للتطبيق تلقائيا إلى البنية الأساسية الجديدة.

## <a name="licensing-impact"></a>تأثير الترخيص

لا تحل هذه الوثائق محل أي من الوثائق القانونية التي تغطي حقوق الاستخدام أو تحل محلها.

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-does-our-licensing-or-cost-change"></a>تستخدم المؤسسة Dynamics 365 Human Resources لإدارة عمليات الموارد البشرية الخاصة بها. هل يتغير ترخيصنا أو التكلفة؟

لن يتأثر العملاء الذين اشتروا تراخيص Dynamics 365 Human Resources. لا يوجد ترحيل ترخيص لهؤلاء العملاء. ولن تكون وحدة حفظ المخزون (SKU) الإضافية الخاصة بالموارد البشرية قابلة للتطبيق بعد الآن. بدلا من ذلك ، يمكن للعملاء اختيار شراء بيئة اختبار من المستوى 2 للتطبيقات Finance and Operations بتكلفة أقل قليلا. سيتم ترحيل العملاء الحاليين الذين اشتروا بيئة اختبار من المستوى 2 للموارد البشرية إلى بيئة اختبار من المستوى 2 لتطبيقات Finance and Operations دون أي تكلفة إضافية.

### <a name="my-organization-uses-dynamics-365-human-resources-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-does-my-licensing-or-cost-change"></a>تستخدم المؤسسة Dynamics 365 Human Resources في Dynamics 365 Finance، Supply Chain Management أو Commerce، أو Project Operations. هل يتغير ترخيصي أو التكلفة؟

يمكن للمستخدمين الحاليين لتطبيقات Dynamics 365 ومستخدمي Dynamics 365 Finance وSupply Chain Management وCommerce وProject Operations الوصول إلى الموارد البشرية كجزء من هذه التراخيص حتى فبراير 2025 أو حتى انتهاء صلاحية اتفاقية الترخيص الحالية ، أيهما أبكر. يمكنك اختيار الانتقال إلى تراخيص الموارد البشرية في وقت سابق إذا كان يساعدك على تحقيق وفورات أفضل في التكاليف. بدءا من فبراير 2025 ، يجب على جميع عملاء CSP و EA الحاليين إيقاف تشغيل وحدة الموارد البشرية وشراء تراخيص الموارد البشرية للاستفادة من القدرات الجديدة التي يتم إحضارها إلى تطبيقات Finance and Operations.

### <a name="my-organization-is-live-with-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-will-we-be-required-to-purchase-an-additional-environment-to-support-the-infrastructure-merge"></a>تستخدم مؤسستي البث المباشر مع  Dynamics 365 Finance، أو Supply Chain Management، أو Commerce، أو Project Operations. هل سيطلب منا شراء بيئة إضافية لدعم دمج البنية الأساسية؟

لا يلزم توفير بيئات إضافية لدعم تغيير البنية الأساسية.

### <a name="where-should-i-go-if-i-have-additional-questions-about-product-licensing"></a>أين يجب أن أذهب إذا كانت لدي أسئلة إضافية حول ترخيص المنتج؟

إذا كانت لديك أسئلة ترخيص، يمكنك العثور على مزيد من المعلومات حول [Biz Apps Hub - D365 Pricing and Licensing](https://businessapplications.transform.microsoft.com/resources/pricing-and-licensing?tab=grandfathering). إذا لم تساعد هذه المعلومات في المشكلة، افتح طلبا باستخدام LicenseQ.
