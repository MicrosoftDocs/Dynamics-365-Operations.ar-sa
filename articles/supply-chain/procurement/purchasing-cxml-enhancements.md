---
title: تحسينات cXML الشراء
description: تعتمد ميزة تحسينات cXML الشراء على وظيفة الكتالوج الخارجي الموجودة، PunchOut، المستخدمة لطلبات الشراء.
author: GalynaFedorova
ms.date: 08/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatCXMLParameters, CatCXMLPurchRequest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2020-08-03
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 87dccd19ade1b27db9a6d454659fec6142de4c65
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890904"
---
# <a name="purchasing-cxml-enhancements"></a>تحسينات cXML الشراء

[!include [banner](../includes/banner.md)]

تعتمد ميزة _تحسينات cXML الشراء_ على [وظيفة الكتالوج الخارجي الموجودة](set-up-external-catalog-for-punchout.md) المستخدمة لطلبات الشراء. وتعرف هذه الوظيفة الموجودة باسم _PunchOut_. علي الرغم من أنه من غير الضروري أن ينشأ أمر شراء من طلب شراء، إلا أنه من الضروري وجود اتصال بين المورّد على أمر الشراء والمعلمات المستخدمة لإرسال مستند أمر الشراء.

## <a name="turn-on-the-purchasing-cxml-enhancements-feature"></a>تشغيل ميزة تحسينات cXML الشراء‬

لتشغيل الميزة، افتح صفحة **[إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)**، وابحث عن الميزة المسماة *تحسينات cXML الشراء*. حدد الميزة، ثم حدد **تمكين الآن** لتشغيلها. (اعتبارًا من الإصدار 10.0.21 من Supply Chain Management، يتم تشغيل هذه الميزة افتراضيًا.)

بعد تشغيل الميزة، يجب عليك تكوين الإعدادات في النواحي الثلاث التالية:

- **[معلمات cXML](#cxml-parameters)** – استخدم هذه الإعدادات لإعداد بعض المعلمات العمومية لوظيفة إرسال أوامر الشراء.
- **[إعداد المورّد](#vendor-setup)** – إذا كان يجب استخدام لغة التمييز القابلة للامتداد (cXML) للتجارة بشكل افتراضي لجميع أوامر الشراء التي يتم إنشاؤها لأي مورّد، يمكنك تعيين الخيار **إرسال أمر الشراء عبر cXML** إلى _نعم_ لذلك المورّد.
- **[الكتالوجات الخارجية](#external-catalog-setup)** – استخدم إعدادات **خصائص الأمر** الجديدة لعريف تنسيق مستند أمر الشراء وكيفية إرساله.

يلخص الرسم التوضيحي التالي هذا التكوين.

![مناطق لإعداد ميزات cXML.](media/cxml-settings-areas.png "مناطق لإعداد ميزات cXML")

علاوةً على ذلك، يجب إعداد [الوظيفة الدُفعية لطلبات أوامر الشراء](#po-batch). يتم استخدام الوظيفة الدُفعية هذه لإرسال أوامر الشراء المؤكدة.

## <a name="set-up-global-cxml-parameters"></a><a name="cxml-parameters"></a>إعداد معلمات cXML العمومية

استخدم الصفحة **معلمات cXML** لإنشاء إعدادات عمومية عليلة تنطبق على وظيفة إرسال أوامر الشراء.

![صفحة معلمات cXML.](media/cxml-parameters.png "صفحة معلمات cXML")

انتقل إلى **التدبير والتوريد‬ \> الإعداد \> إدارة cXML \> معلمات cXML**، وعيّن المعلمات التالية:

- **وضع اختبار cXML** – تؤثر هذه المعلمة العمومية على الطريقة التي يتم بها إرسال أوامر الشراء فعليًا من الوظيفة الدُفعية. حدد إحدى القيم التالية:

    - **اختبار** – في هذا الوضع، يمكن تشغيل الوظيفة الدُفعية، ويتم إنشاء مستند XML الخاص بالرسالة، ولكن لا يتم إرساله. بدلاً من ذلك، يتم حفظه في طلب أمر الشراء لأغراض المراجعة. يعد هذا الوضع مفيدًا عندما تكون في تطبيق أولي، وتريد معرفه كيفية إدخال البيانات في رسالة cXML. وقد ترغب أيضًا في إنشاء نماذج رسائل يمكن إرسالها إلى المورّد لإجراء تحقق أولي من الصحة.
    - **مباشر** – في هذا الوضع، تستخدم الميزة [إعدادات الكتالوج الخارجي](#external-catalog-setup) لإرسال كل مستند بطريقة فعلية إلى المورّد.

- **إرسال تحديثات طلب الشراء** – عيّن هذا الخيار إلى *نعم* لإرسال رسالة تحديث لأوامر الشراء. قم بتعيينه هذا الخيار إلى *لا* لمنع إرسال الرسالة. يفضل معظم المورّدين عدم تلقي رسائل تحديث. بدلاً من ذلك، يطالبون العملاء بالاتصال بهم من خلال الهاتف أو البريد الإلكتروني إذا كان من الضروري إدخال تغيير على أمر شراء. هذه المعلمة هي معلمة عمومية، ولا يمكن تحديد تجاوز على الكتالوج الخارجي لكل مورّد. سيتم وضع علامة على أمر الشراء كمحدّث إذا قمت بترحيل تأكيد ثانٍ على أمر الشراء، ولكن تم إرسال التأكيد الأول وأقر المورّد باستلامه. عند وجود تأكيد ثانٍ، ولكن لم يتم إرسال التأكيد الأول، ستتم معاملة التأكيد الثاني على أنه مستند جديد. يمكنك تأكيد أمر الشراء العدد الذي تريده من المرات حتى يتم إرسال تأكيد واحد. سيتم بعد ذلك معاملة التأكيد التالي على أنه رسالة تحديث.
- **إرسال حذف طلب الشراء** – عيّن هذا الخيار إلى *نعم* لإرسال رسالة تحديث لأوامر الشراء. قم بتعيينه هذا الخيار إلى *لا* لمنع إرسال الرسالة. يفضل معظم المورّدين عدم تلقي رسائل الحذف. بدلاً من ذلك، يطالبون العملاء بالاتصال بهم من خلال الهاتف أو البريد الإلكتروني في حال تم إرسال أمر الشراء عن طريق الخطأ. هذه المعلمة هي معلمة عمومية، ولا يمكن تحديد تجاوز على الكتالوج الخارجي لكل مورّد. سيتم وضع علامة على أمر الشراء كمحذوف إذا قمت بإلغاء أمر الشراء في Supply Chain Management.
- **أرشفة الملف** – حدد مسار الملف حيث تريد تصدير مستندات cXML المؤرشفة وحفظها. يتم استخدام المسار عند تشغيل وظيفة الحذف من الصفحة **طلب أمر الشراء**.
- **الحد الأقصى لعدد أحرف سطر الشارع** – أدخل الحد الأقصى لعدد الأحرف التي يمكن استخدامها في حقل الشارع للعناوين في مستند cXML. تؤثر هذه المعلمة العمومية على جميع المورّدين ما لم يتم تحديد تجاوز في خصائص الكتالوج الخارجي.

## <a name="set-up-vendor-purchase-orders-to-use-cxml"></a><a name="vendor-setup"></a>إعداد أوامر شراء المورّد لاستخدام cXML

في كل مرة تقوم فيها بتأكيد أمر شراء حيث تم تعيين الخيار **إرسال أمر الشراء عبر cXML** إلى _نعم_، يقوم النظام بشكل تلقائي بإنشاء رسالة cXML ويقوم بتسليمها إلى المورّد المرتبط بأمر الشراء. توجد طريقتان للتحكم في هذا الخيار لأوامر الشراء الخاصة بك:

- لإعداد مورّد بحيث يستخدم cXML بشكل تلقائي لكافة أوامر الشراء الجديدة المُنشاة من طلب، انتقل إلى **التدبير والتوريد‬ \> المورّدون \> جميع المورّدين**، وحدد أو أنشئ مورّدًا لفتح صفحة تفاصيله. بعد ذلك، على علامة التبويب السريعة **القيم الافتراضية لأمر الشراء‬‏‫**، عيّن الخيار **إرسال أمر الشراء  عبر cXML** إلى _نعم_. إذا كان من الضروري استخدام cXML تلقائيًا لأوامر الشراء الجديدة التي **لم** تنشأ من طلب، يجب عليك أيضًا تعيين خاصية الأمر **ENABLEMANUALPO** إلى _صواب_ للكتالوج الخارجي ذي الصلة، كما سيرد في القسم [تعيين خصائص الأمر](#set-order-properties) لاحقًا في هذا المقال.
- بالنسبة لأوامر الشراء الفردية، انتقل إلى **التدبير والتوريد‬ \> أوامر الشراء \> جميع أوامر الشراء**, وحدد أو أنشئ أمر شراء لفتح صفحة تفاصيله. قم بالتبديل إلى طريقة عرض **الرأس**، ثم على علامة التبويب السريعة **الإعداد**، عيّن الخيار **إرسال أمر الشراء عبر cXML** كما هو مطلوب.

![الإعدادات الافتراضية لأوامر شراء المورّد.](media/cxml-order-defaults.png "الإعدادات الافتراضية لأوامر شراء المورّد")

## <a name="set-up-an-external-catalog-to-use-cxml"></a><a name="external-catalog-setup"></a>إعداد كتالوج خارجي لاستخدام cXML

في صفحة **الكتالوجات الخارجية**، لكل واحد من الكتالوجات، يمكنك إعداد وظيفة PunchOut والوظيفة الخاصة بإرسال أوامر الشراء. للعثور على الإعدادات المناسبة، انتقل إلى **التدبير والتوريد‬ \> الكتالوجات \> الكتالوجات الخارجية**. ابدأ [بإعداد كل كتالوج كالمعتاد](set-up-external-catalog-for-punchout.md). تشتمل هذه العملية على تعيين مورّد وتحديد الفئات التي يسمح للمورّد بتوفيرها وتنشيط الكتالوج. ثم قم بتكوين الإعدادات الإضافية الموضحة في هذا القسم.

> [!NOTE]
> عندما تؤكد أمر شراء يمكن إرساله من خلال cXML، يبحث النظام عن المورّد المرتبط بأمر الشراء، ثم يبحث عن أول كتالوج خارجي مرتبط بهذا المورّد. ثم يستخدم النظام الإعدادات من هذا الكتالوج الخارجي لإرسال أمر الشراء. إذا تم إعداد كتالوجات خارجية متعددة، يستخدم النظام فقط الكتالوج الخارجي الأول الذي يعثر عليه، استنادًا إلى المورّد في أمر الشراء. وبالتالي، ننصحك بإنشاء كتالوج خارجي واحد فقط لكل مورّد.

![إعدادات الكتالوج الخارجي.](media/cxml-supplier-catalog.png "إعدادات الكتالوج الخارجي")

### <a name="set-the-punchout-protocol-type"></a>تعيين نوع بروتوكول PunchOut

على علامة التبويب السريعة **عام** في صفحة **الكتالوجات الخارجية**، عيّن الحقل **نوع بروتوكول PunchOut‬** إلى _cXML_. سيكون هذا الخيار الخيار الوحيد المتاح، ما لم يقم أحد الأطراف بتوسيع الوظيفة وتوفير خيار إضافي في الملحق

إذا كنت تستخدم أيضًا الكتالوج لـ PunchOut، فيجب عليك أيضًا [إعداد تنسيق الرسالة](set-up-external-catalog-for-punchout.md). يتم استخدام تنسيق الرسالة لتأسيس الاتصال بالمورّد في حركة PunchOut من الطلب. عند إرسال أمر شراء، يتم استخدام خصائص الأمر لتأسيس الاتصال بالمورّد.

### <a name="set-the-order-properties"></a><a name="set-order-properties"></a>تعيين خصائص الأمر

تضيف الميزة _تحسينات cXML الشراء‬_ علامة تبويب سريعة **خصائص الأمر** للكتالوجات الخارجية. توفر علامة التبويب هذه شبكة حيث يمكنك تحديد خصائص الأمر. وهي توفر أيضًا شريط أدوات. يحتوي شريط الأدوات هذا على الأزرار الثلاثة التالية التي يمكنك استخدامها لإدارة خصائص الأمر:

- **الخصائص الافتراضية** – عندما تقوم بإعداد كتالوج جديد، حدد هذا الزر لإضافة مجموعة معرفة مسبقًا من الخصائص الشائعة الاستخدام إلى الشبكة.
- **جديد** - لإضافة خاصية جديدة إلى الشبكة.
- **حذف** – لحذف الخاصية المحددة حاليًا من الشبكة. إذا قمت بحذف خاصية افتراضية بطريق الخطأ، فحدد **الخصائص الافتراضية** لاستعادة كافة الخصائص المفقودة.

في كل مرة تقوم فيها بإضافة خاصية أو أكثر إلى الشبكة، فاستخدم العمود الأيسر لتحديد قيمة لكل منها.

استخدم الخصائص الافتراضية بالطريقة التالية:

- **BUYER\_COOKIE** – يمكن استخدام حقل التعقب هذا للإشارة إلى معلومات خاصة بشركتك. ما لم يكن لديك اتفاقية مع المورّد حول كيفية استخدام هذه الخاصية، فهي ليست ذات أهمية كبيرة عند إرسال أمر شراء. وبالتالي، يجب تعيينها إلى قيمة بسيطة.
- **DELIVERTO** – عند إدخال عنوان الشحن في المستند من أمر الشراء، يُستخدم الحقل **معلومات الانتباه‬** لتعيين الحقل **DeliverTo** في رسالة XML. إذا أردت أن تكون هذه القيمة عبارة عن اسم طالب، وقمت بتعيين حقل الطالب على رأس أمر الشراء، فأدخل القيمة _الطالب_ لهذه الخاصية، بحيث يتم إدخال اسم الطالب في الحقل **DeliverTo** في XML. في هذه الحالة، سيكون عنوان البريد الإلكتروني الأساسي ورقم الهاتف اللذين يستخدمهما الطالب بدلاً من مقدم الأمر.
- **DEPLOYMENTMODE** – عيّن هذه الخاصية كما هو مطلوب من المورّد. القيم هي عادةً _PRODUCTION_ أو _TEST_. قم بتعيين القيمة استنادًا إلى اتصالاك بالمورّد. يجب أن تتطابق عادةً مع النظام المقصود خلف القيمة **ORDERCHECKURL** التي يشير إليها المورّد كنظام اختبار أو إنتاج.
- **FIXEDBILLADDRESSID** – عند تعيين الحقل **addressID** في رسالة XML، ينتقي الموقع المحدد على العنوان. إذا كانت قيمة المعرف التي أبلغت المورّد عنها تختلف عن القيمة الموجودة في موقع العنوان لسبب ما، يمكنك فرض تجاوز عن طريق تحديد القيمة هنا. والافتراض هو انك ستستخدم عنوانًا واحدًا فقط مع المورّد، وأن إعداد هذا العنوان قد تم في نظام المورّد. عنوان الفوترة هو عنوان الفاتورة الأساسي الذي تم تحديده للكيان القانوني في Supply Chain Management.
- **FIXEDSHIPADDRESSID** – عند تعيين الحقل **addressID** في رسالة XML، ينتقي الموقع المحدد على العنوان. إذا كانت قيمة المعرف التي أبلغت المورّد عنها تختلف عن القيمة الموجودة في موقع العنوان لسبب ما، يمكنك فرض تجاوز عن طريق تحديد القيمة هنا. والافتراض هو انك ستستخدم عنوانًا واحدًا فقط مع المورّد، وأن إعداد هذا العنوان قد تم في نظام المورّد. عنوان الشحن هو العنوان المحدد في رأس أمر الشراء. يقبل معظم المورّدين عناوين الرأس فقط، وليس عناوين البنود. على الرغم من وجود حقول لعناوين البنود في XML، سيتم تعيينها لعنوان الرأس.
- **FROM\_DOMAIN** – أدخل القيمة المستخدمة لإرسال مستندات أوامر الشراء. يتم توفير هذه القيمة بواسطة المورّد.
- **FROM\_IDENTITY** – أدخل القيمة المستخدمة لإرسال مستندات أوامر الشراء. يتم توفير هذه القيمة بواسطة المورّد.
- **ORDERCHECKURL** – أدخل عنوان URL لإرسال مستندات أمر الشراء إليه. يبدأ عنوان URL بـ `https://` وهو متوفر بواسطة المورّد.
- **PAYLOAD\_ID** – أدخل قيمة بادئة لمعرف الحمولة، كما هو مطلوب للعمليات التجارية الموضوعة للمورّد المحلي.
- **DOMAIN\_SENDER** – أدخل القيمة المستخدمة لإرسال مستندات أوامر الشراء. يتم توفير هذه القيمة بواسطة المورّد.
- **IDENTITY\_SENDER** – أدخل القيمة المستخدمة لإرسال مستندات أوامر الشراء. يتم توفير هذه القيمة بواسطة المورّد.
- **SHARED\_SECRET** – أدخل القيمة المستخدمة لإرسال مستندات أوامر الشراء. يتم توفير هذه القيمة بواسطة المورّد.
- **STREETLENGTH** – أدخل رقمًا يمثل الحد الأقصى لعدد الأحرف التي سيقبلها المورّد كاسم شارع. إذا تم إدخال قيمة هنا، فهي تتجاوز القيمة المحددة في صفحة **معلمات cXML**. سيقوم النظام بإزالة فواصل الأسطر والمسافات لمحاولة احتواء العنوان القياسي في Supply Chain Management في عدد الأحرف المحددة هنا. سيتم اقتطاع الأحرف الإضافية.
- **TO\_DOMAIN** – أدخل القيمة المستخدمة لإرسال مستندات أوامر الشراء. يتم توفير هذه القيمة بواسطة المورّد.
- **TO\_IDENTITY** – أدخل القيمة المستخدمة لإرسال مستندات أوامر الشراء. يتم توفير هذه القيمة بواسطة المورّد.
- **USERAGENT** – أدخل قيمة لتحديد النظام الذي تستخدمه. على سبيل المثال أدخل _Dynamics 365 Supply Chain Management_.
- **VERSION** – أدخل رقم إصدار cXML، إذا طالب المورّد بهذه المعلومات. الإصدار الافتراضي هو *1.2.008*. هذا الإصدار مستقر ويقبله معظم المورّدين.
- **RESPONSETEXT** – أدخل أي نص مخصص تتوقع أن يقوم المورّد بإرجاعه في رسالة استجابة cXML بعد إرسال الأمر. من خلال هذه الطريقة، يستطيع النظام وضع علامة على الرسالة باعتبار أنه تم _الإقرار باستلامها_. في حالة عدم تطابق الاستجابة مع النص القياسي أو نص العميل الذي تدخله هنا، سيتم وضع علامة على الطلب على أنه _خطأ_.
- **RESPONSETEXTSUB** – قم بتعيين هذه الخاصية إلى _TRUE_ إذا أردت البحث عن نص استجابة المورّد للقيم المحددة في الحقل **RESPONSETEXT**. على سبيل المثال، قد يقوم المورّد بإرجاع سلسلة طويلة تتضمن "موافق" في الاستجابة. في هذه الحالة، يمكنك إدخال _موافق_ في حقل **RESPONSETEXT** وتعيين **RESPONSETESTSUB** إلى _TRUE_ للبحث عن "موافق" في أي مكان في الاستجابة. ويمكن بعد ذلك تعيين الأمر إلى _الإقرار بالاستلام_.
- **CONTENTTYPE** – في إعداد كتالوج نموذجي، لا يلزم تعيين هذه الخاصية. إذا تلقيت رسالة الخطأ 500 للخادم من نظام المورّد عند إرسال أمر شراء، يمكنك إجراء الاختبار عن طريق تعيين هذه الخاصية إلى _FALSE_. ستقوم هذه القيمة بتغيير إعداد في طلب الويب وقد يؤدي ذلك إلى تمكين إرسال الرسالة لبعض الأنظمة  الأساسية.
- **ENABLEHEADERS** – قم بتعيين هذه الخاصية إلى _TRUE_ لإرسال الرؤوس مع أمر الشراء. يجب تعيين هذه الخاصية فقط إذا طلب المورّد ذلك. إذا قمت بتعيين هذه الخاصية إلى _TRUE_، فأضف خصائص مخصصة تستند إلى الأسماء التي يوفرها المورّد، وأضف إليها البادئة _H\__. تتضمن الأمثلة النموذجية **H\_USERID** و **H\_PASSWORD** و **H\_RECEIVERID** و **H\_ACTIONREQUEST**. يتم تضمين الخصائص المخصصة التالية في الخصائص الافتراضية:

    - **H\_USERID** – إذا طالبك الشريك التجاري بإرسال معرف مستخدم كجزء من عنوان URL لإرسال أمر شراء، أدخل القيمة هنا.
    - **H\_PASSWORD** – إذا طالبك الشريك التجاري بإرسال معرف مستخدم كجزء من عنوان URL لإرسال أمر شراء، أدخل القيمة هنا.

- **ENABLEMANUALPO** – إذا تم تعيين الخاصية إلى _TRUE_، عندما ينشئ المستخدمون أوامر الشراء يدويًا (أي عندما لا تبدأ من طلب)، سترث أوامر الشراء هذه إعداد الخيار **إرسال أمر الشراء عبر cXML** من المورّد. إذا لم يتم تعيين هذه الخاصية، أو إذا تم تعيينها إلى _FALSE_، فلن يتم تعيين الخيار **إرسال أمر الشراء عبر cXML** على رأس أمر الشراء لأوامر الشراء المُنشأة يدويًا. بالنسبة لأوامر الشراء المُنشأة من طلب، يتم دائمًا توارث الخيار **إرسال أمر الشراء عبر cXML‎** من المورّد، بغض النظر عن إعداد هذه الخاصية. لمزيد من المعلومات، راجع القسم [إعداد أوامر شراء المورّد لاستخدام cXML‬](#vendor-setup) أعلاه في هذا المقال.
- **PUNCHOUTPOONLY** – إذا تم تعيين هذه الخاصية إلى _TRUE_، فإن بنود طلب الشراء المُنشأة من عملية PunchOut وحدها ستعّين الخيار **إرسال أمر الشراء عبر cXML** على رأس أمر الشراء. علاوةً على ذلك، يجب أن يكون نوع بند طلب الشراء لجميع البنود في أمر الشراء _صنف كتالوج خارجي_. وبخلاف ذلك، لا يمكن إنشاء أمر شراء cXML.
- **PUNCHOUTSHIPTO** – إذا تم تعيين هذه الخاصية إلى _TRUE_، فسيُضاف العنوان الافتراضي للكيان القانوني إلى رسال طلب إعداد PunchOut عند قيام المستخدم بفتح كتالوج خارجي. يُضاف هذا العنوان كعنوان **ShipTo**. سيستخدم المورّدون عنوان **ShipTo** لإظهار الأسعار استنادًا إلى موقع الشركة.
- **TRACEPUNCHOUT** – قم بتعيين هذه الخاصية إلى _TRUE_ إذا تلقيت رسالة خطأ عند محاولة الاستعراض للحصول على كتالوج خارجي من الطلب سيتم بعد ذلك ملء معلومات التتبع لرسائل **PunchOutSetupRequest** و **PunchOutResponse** المرسلة بين Supply Chain Management وموقع المورّد. يمكنك عرض هذه المعلومات في صفحة **سجل رسائل سلة cXML**، التي يمكنك فتحها من الصفحة **إعداد كتالوج خارجي** لكتالوج المورّد الذي تواجه مشاكل معه. يجب تعيين هذه الخاصية إلى _TRUE_ فقط إذا كنت تقوم باستكشاف الأخطاء وإصلاحها، لأنها تنشئ مصروفات زائدة كبيرة للأداء على قاعدة البيانات لكل PunchOut. لمزيد من المعلومات، راجع القسم [عرض سجل رسائل سلة cXML لـ PunchOut‎ الكتالوج الخارجي](#message-log) لاحقًا في هذا المقال.
- **REPLACENEWLINE** – قم بتعيين هذا الخاصية إلى _TRUE_ إذا واجهت مشكلة بسبب قيام نظام المورّد بإرسال رسالة **PunchOutResponse** تتضمن أحرف أسطر جديدة (\\n). قد تحدث هذه المشكلة إذا تم تحليل رسائل المورّد من خلال برنامج وسيط أو مركز تدبير. إذا كنت تواجه مشكلة في إعداد مورّد جديد، فقم بتعيين الخاصية **TRACEPUNCHOUT** إلى _TRUE_ لعرض الرسالة **PunchOutResponse** وتحديد ما إذا كانت علامات XML مقطوعة بواسطة أحرف الأسطر الجديدة.
- **POCOMMENTS** – قم بتعيين هذه الخاصية إلى _TRUE_ إذا أردت أن يتضمن مستند cXML ملاحظات مرفقة بأمر الشراء في Supply Chain Management. يتم تضمين نص المرفق في تعليقات الرأس في رسالة أمر الشراء. لمزيد من المعلومات حول كيفية قيام النظام بتحديد هذه المرفقات ومعالجتها، راجع القسم [إرفاق الملاحظات بأمر الشراء](#attach-po-notes) لاحقًا في هذا المقال.
- **VENDCOMMENTS** – قم بتعيين هذه الخاصية إلى _TRUE_ إذا أردت أن يتضمن مستند cXML ملاحظات مرفقة بأمر الشراء في Supply Chain Management. يتم تضمين نص المرفق في تعليقات الرأس في رسالة أمر الشراء. لمزيد من المعلومات حول كيفية قيام النظام بتحديد هذه المرفقات ومعالجتها، راجع القسم [إرفاق الملاحظات بأمر الشراء](#attach-po-notes).
- **CLEANAMP** – قم بتعيين هذه الخاصية إلى _TRUE_ إذا تلقيت رسالة خطأ عند محاولة إجراء PunchOut لمورّد، ويتضمن عنوان URL المرتجع للمورّد علامات عطف (\&).
- **PUNCHOUTTZ** – قم بتعيين هذه الخاصية إلى _TRUE_ إذا كان المورّد الذي تتعامل معه يستخدم معيار  المنظمة العالمية للمواصفات (ISO) 8601 للقيام بعملية تحقق معينة من تاريخ/وقت رسالة طلب PunchOut. تستخدم Supply Chain Management تاريخ التوقيت العالمي المتفق عليه (UTC) في رسالة **PunchOutSetupRequest**. وبالتالي، عند تعيين هذه الخاصية إلى _TRUE_، يُضاف *+00:00* إلى تنسيق التاريخ/الوقت.
- **WMSADDRESSID** – قم بتعيين هذه الخاصية إلى _TRUE_ لاستخدام رقم المستودع على رأس أمر الشراء كقيمة **addressID** في عنوان **ShipTo** لطلب أمر الشراء المرسل إلى المورّد. إذا قمت بتعيين قيمة للخاصية **FIXEDSHIPADDRESSID**، فستكون لتلك القيمة الأسبقية على هذه القيمة. وبالتالي، يجب استخدام خاصية واحد أو الأخرى لتعيين قيمة **addressID** في عنوان **ShipTo** للمستند.
- **PUNCHOUTSHIPTOUSER** – تعمل هذه الخاصية مع الخاصية **PUNCHOUTSHIPTO**. إذا تم تعيين الخاصية **PUNCHOUTSHIPTO** إلى _TRUE_، فسيتم انتقاء عنوان الكيان القانوني. إذا تم تعيين **PUNCHOUTSHIPTOUSER** إلى _TRUE_، فسيتم استخدام العنوان الرئيسي من مستخدم بدلاً من عنوان الكيان القانوني.

### <a name="activate-the-external-catalog"></a>تنشيط الكتالوج الخارجي

عند الانتهاء من إعداد كافة الخصائص وتكوين الإعدادات الأخرى للكتالوج الخارجي، عد إلى علامة التبويب السريعة **عام** في صفحة **الكتالوجات الخارجية** وعيّن الخيار **نشط** إلى *نعم*.

### <a name="attach-notes-to-a-purchase-order"></a><a name="attach-po-notes"></a>إرفاق ملاحظات بأمر شراء

كما ورد في القسم [تعيين خصائص الأمر](#set-order-properties)، إذا أردت أن يتضمن cXML الذي تم تسليمه نصًا من ملاحظات مرفقة بأمر الشراء ذي الصلة و/أو سجلات المورّد، فيمكنك تعيين الخاصية **POCOMMENTS** و/أو الخاصية **VENDCOMMENTS** إلى _TRUE_ في إعداد الكتالوج الخارجي. يوفر هذا القسم المزيد من التفاصيل حول كيفية قيام النظام بتحديد هذه المرفقات ومعالجتها إذا كنت تستخدمها.

لتعيين أنواع الملاحظات التي سيقوم النظام بالبحث عنها، انتقل إلى **التدبير والتوريد‬ \> الإعداد \> النماذج \> من الإعداد**. ثم، من علامة التبويب **أمر الشراء** عيّن الحقل **تضمين مستندات من النوع** إلى نوع الملاحظات التي تريد أن تكون قادرًا على تضمينها. سيتم تضمين الملاحظات النصية فقط، وليس مرفقات المستند.

![صفحة إعداد النموذج.](media/cxml-form-setup.png "صفحة إعداد النموذج")

سيتم تضمين المرفقات مع أمر الشراء فقط إذا تم تعيين حقل **النوع** التابع لها إلى القيمة المحددة في الحقل **تضمين مستندات من النوع** وفي حال تعيين حقل **القيد** إلى _خارجي_. لإنشاء مرفقات أمر شراء أو عرضها أو تحريرها، انتقل إلى **التدبير والتوريد‬ \> جميع أوامر الشراء**، وحدد أو أنشئ أمر شراء، ثم حدد الزر **مرفقات** (رمز مشبك الورق) في الزاوية العلوية اليسرى.

![ملاحظة مرفقة تم إعدادها ليتم إرسالها إلى المورّد.](media/cxml-note-to-vendor.png "ملاحظة مرفقة تم إعدادها ليتم إرسالها إلى المورّد")

## <a name="view-the-cxml-cart-message-log-for-external-catalog-punchout"></a><a name="message-log"></a>عرض سجل رسائل سلة cXML لـ PunchOut‎ الكتالوج الخارجي

عند تعيين الحقل **نوع بروتوكول Punchout** إلى _cXML_ لكتالوج خارجي، سيلتقط النظام سجل رسائل السلة المرتجعة من المورّدين. يمكن استخدام هذا السجل لاستكشاف الأخطاء وإصلاحها ولأغراض أخرى تتعلق بالبيانات.

لفتح السجل الخاص بكتالوج خارجي، حدد الكتالوج المناسب، ثم في جزء الإجراءات، حدد **سجل رسائل سلة cXML**. تعرض الصفحة **سجل رسائل سلة cXML** قائمة بسلات التسوق المرتجعة، وXML المرتبط بتلك السلات، والبنود التي تم إنشاؤها في طلب الشراء ذي الصلة.

![صفحة سجل رسائل سلة cXML.](media/cxml-cart-message-log.png "صفحة سجل رسائل سلة cXML")

## <a name="set-the-extrinsic-elements-for-external-catalog-punchout"></a>تعيين العناصر الخارجية لـ PunchOut الكتالوج الخارجي

عند تعيين حقل **نوع بروتوكول Punchout** إلى *cXML* لكتالوج خارجي، يمكنك إضافة عناصر خارجية مخصصة سيتم إدراجها في المكان الصحيح في رسالة طلب XML.

لإضافة عناصر خارجية إلى كتالوج خارجي، اتبع الخطوات التالية.

1. انتقل إلى **التدبير والتوريد‬ \> الكتالوجات \> الكتالوجات الخارجية**.
1. حدد الكتالوج المناسب.
1. على علامة التبويب السريعة **تنسيق الرسالة**، في القسم **خارجية**، حدد **إضافة** لإضافة صف إلى الشبكة لكل عنصر خارجي تريد تضمينه. على كل صف، قم بتعيين الحقول التالية:

    - **الاسم‏‎** – أدخل اسمًا للعنصر. ستصبح هذه القيمة قيمة سمة **الاسم** لعنصر XML **الخارجي** الذي تم إنشاؤه بواسطة كل صف. ستعمل عادةً مع المورّد للموافقة على اسم كل عنصر خارجي.
    - **القيمة** – حدد قيمة للعنصر. ستصبح هذه القيمة قيمة عنصر XML الذي تم إنشاؤه بواسطة كل صف. تتوفر القيم التالية:

        - **اسم المستخدم** – استخدم اسم المستخدم الذي يجري PunchOut. وهذا الاسم هو اسم تسجيل الدخول إلى Supply Chain Management.
        - **عنوان البريد الإلكتروني للمستخدم** – استخدم عنوان البريد الإلكتروني للمستخدم‏‎ الذي يجري PunchOut. هذا العنوان هو العنوان الذي تم إعداد من قبل المستخدم على علامة تبويب **الحساب** في صفحة **خيارات المستخدم**.
        - **القيمة العشوائية**- استخدم  قيمة عشوائية فريدة.
        - **الاسم الكامل للمستخدم** – استخدم الاسم الكامل لشخص جهة الاتصال المرتبط بالمستخدم الذي ينتقل إلى الكتالوج الخارجي.
        - **الاسم الأول** – استخدم الاسم الأول لشخص جهة الاتصال المرتبط بالمستخدم الذي ينتقل إلى الكتالوج الخارجي.
        - **اسم العائلة** – استخدم اسم العائلة لشخص جهة الاتصال المرتبط بالمستخدم الذي ينتقل إلى الكتالوج الخارجي.
        - **رقم الهاتف** – استخدم رقم الهاتف الرئيسي لشخص جهة الاتصال المرتبط بالمستخدم الذي ينتقل إلى الكتالوج الخارجي.

![إعدادات العناصر الخارجية.](media/cxml-extrinsics.png "إعدادات العناصر الخارجية")

لن يتمكن المستخدم أو المسؤول من رؤية العناصر الخارجية، بسبب عدم إضافتها إلا عندما يجري المستخدم PunchOut. وسيتم إدراجها تلقائيًا بين عناصر **BuyerCookie** و **BrowserFromPost** في رسالة طلب إعداد cXML. وبالتالي، ليس من الضروري تعيينها يدويًا في XML عند إعداد الكتالوج الخارجي.

![عناصر خارجية مضافة إلى XML.](media/cxml-extrinsics-xml.png "عناصر خارجية مضافة إلى XML")

## <a name="create-and-process-a-purchase-order"></a><a name="create-po"></a>إنشاء أمر شراء ومعالجته

عند إنشاء أمر شراء لأحد المورّدين، يرث أمر الشراء هذا إعداد الخيار **إرسال أمر الشراء  عبر cXML** من ذلك المورّد. ومع ذلك، يبقى الإعداد متوفرًا على علامة التبويب السريعة **الإعداد** في طريقة عرض **الرأس** على أمر الشراء، بحيث يمكنك تغييره لاحقًا حسب الطلب.

![تعيين أمر شراء لاستخدام cXML.](media/cxml-purchase-order.png "تعيين أمر شراء لاستخدام cXML")

عند إنشاء أمر شراء من طلب شراء قادم من سير مهام PunchOut، سيتم ملء كافة تفاصيل البنود المطلوبة. يمكن بعد ذلك إضافة بنود أمر الشراء يدويًا أو نسخها من أوامر شراء أخرى. تأكد من تعيين كافة الحقول المطلوبة. تتضمن هذه الحقول المطلوبة رقم المرجع الخارجي، وهو رقم المورّد الذي سيتم استخدامه في رسالة cXML.

![مثال عن رقم مرجع خارجي.](media/cxml-line-details.png "مثال عن رقم مرجع خارجي")

عند الانتهاء من ملء كافة التفاصيل الخاصة  بأمر  الشراء، احرص على تأكيدها. لا يتم إرسال أي رسالة ما لم يتم تأكيد أمر الشراء. لتأكيد أمر شراء، في جزء الإجراءات, على علامة التبويب **الشراء**، في المجموعة **الإجراءات**، حدد **تأكيد**. 

بعد تأكيد أمر الشراء، يمكنك عرض حالة التأكيد من خلال دفاتر يومية **تأكيدات أمر الشراء**. في جزء الإجراءات, على علامة التبويب **الشراء**، في المجموعة **دفاتر اليومية**، حدد **تأكيدات أمر الشراء**.

بإمكان كل أمر شراء الحصول على تأكيدات كثيرة. توضع علامة على كل تأكيد بواسطة رقم تزايدي. في الرسم التوضيحي التالي، أمر الشراء هو *00000275*، والتأكيد هو *00000275-1*. ويعكس هذا الترقيم وظيفة Supply Chain Management القياسية، حيث يتم التعرف على التغييرات في أمر الشراء، وبالتالي نوع رسالة cXML التي يجب إرسالها إلى المورّد، استنادًا إلى التأكيد. كما يبيّنه الرسم التوضيحي، تتضمن أيضًا صفحة **تأكيدات أمر الشراء** الحقلين **حالة إرسال الأمر** و **حالة مورّد طلب الأمر**. لمزيد من المعلومات حول قيم الحالات المختلفة التي قد تشاهدها في هذه الصفحة، راجع القسم [مراقبة طلبات أوامر الشراء](#monitor-po-requests) لاحقًا في هذا المقال.

![صفحة تأكيدات أمر الشراء.](media/cxml-po-confirmations.png "صفحة تأكيدات أمر الشراء")

لعرض مزيد من المعلومات حول المستند، حدد **طلب أمر الشراء** فوق الشبكة.

تتضمن صفحة **طلب أمر الشراء** شبكتين. تحتوي الشبكة الموجودة في الجزء العلوي من الصفحة على سجل واحد لكل أمر شراء تم وضع علامة عليه للإرسال. قد تحتوي الشبكة في علامة التبويب **محفوظات طلبات أوامر الشراء** في الجزء السفلي من الصفحة على سجلات متعددة لأمر الشراء المحدد، وذلك للإشارة إلى حالة كل تأكيد. يبين الرسم التوضيحي التالي أمر الشراء 00000275 في الشبكة العلوية والمستند 00000275-1 في الشبكة على علامة التبويب **محفوظات طلبات أوامر الشراء**.

![صفحة طلب أمر الشراء.](media/cxml-po-request.png "صفحة طلب أمر الشراء")

إذا تم إعداد الوظيفة الدُفعية وتشغيلها، فسيتم إرسال المستند. يمكنك عرض تغيير الحالة بعد إرسال المستند. في الرسم التوضيحي التالي، تم تعيين حقل **حالة إرسال الأمر** إلى _مُرسل_.. تم تعيين الحقل **حالة مورّد طلب الأمر** إلى _تم الإقرار بالاستلام_ للإشارة إلى أن المورّد استلم المستند، وأنه تمكّن من قراءته وتخزينه في النظام. تعرض الشبكة في علامة التبويب **محفوظات طلبات أوامر الشراء‬‏‫** الوقت الذي تم فيه إرسال المستند. لمزيد من المعلومات حول قيم الحالات المختلفة التي قد تشاهدها في هذه الصفحة، راجع القسم [مراقبة طلبات أوامر الشراء](#monitor-po-requests).

![رسائل الحالة في صفحة طلب أمر الشراء.](media/cxml-po-request-2.png "رسائل الحالة في صفحة طلب أمر الشراء")

## <a name="schedule-the-purchase-order-request-batch-job"></a><a name="po-batch"></a>جدولة الوظيفة الدُفعية لطلب أمر الشراء

لتنشيط الوظيفة الدُفعية لإرسال طلبات أوامر الشراء، انتقل إلى **التدبير والتوريد‬ \> الإعداد \> إدارة cXML \> طلب أمر الشراء**، ثم في جزء الإجراءات، على علامة التبويب **طلب أمر الشراء** في المجموعة **دُفعة**، حدد **إرسال الوظيفة** لفتح مربع الحوار **تجهيز أمر الشراء وإرساله**. يمكنك استخدام مربع الحوار هذا لإعداد التكرار، تمامًا كما تفعل عادةً للوظائف الدُفعية في Supply Chain Management. حدد فاصلاً زمنيً، استنادً إلى حجم الأمر. علي الرغم من أنه يمكنك تشغيل الوظيفة الدُفعية كل دقيقة، إلا أنه من المستحسن على الأرجح إرسال دُفعات خلال يوم العمل، استنادًا إلى فترات الاستلام التي تتطابق مع جداول المورّدين.

على سبيل المثال، هناك سياسة لدى المورّد تشير إلى أن جميع الأوامر التي يتم استلامها عند الساعة الواحدة من بعد الظهر سيتم شحنها في نفس اليوم. في هذه الحالة، قد تحتاج إلى تشغيل الدُفعة مرات قليلة فقط خلال الصباح لتوصيل أي أوامر لديك. وسيتم بعد ذلك إرسال الأوامر المتبقية في اليوم التالي. هذا القرار هو قرار خاص بالأعمال فقط. ويمكنك مراجعته وتعيين المعلمات له وفقًا لذلك.

ستقوم العملية بالبحث عن مستندات طلب أمر الشراء ذات الحالة *قيد الانتظار*. إذا كان لديك أمر يجب إرساله إلى المورّد على الفور، يمكنك تحديد **إرسال الوظيفة** وتعيين الخيار **معالجة دُفعية** إلى *لا*.

## <a name="monitor-purchase-order-requests"></a><a name="monitor-po-requests"></a>مراقبة طلبات أوامر الشراء

### <a name="view-the-status-of-a-purchase-order"></a>عرض حالة أمر شراء

عندما يتم تأكيد الأوامر التي يمكن إرسالها عبر cXML، فإنها تنتقل إلى الحالة _قيد الانتظار_. وكما هو موضح في القسم [إنشاء أمر شراء ومعالجته‬](#create-po)، يمكنك عرض حالة أمر الشراء على الصفحة **طلب أمر الشراء**. يُحتمل وجود حالة من ضمن حالات متعددة لكل أمر شراء، وهذا يتوقف على معلماته وبياناته. يصف هذا القسم أنواع الحالات المختلفة والقيم التي يمكن أن تتضمنها. بإمكان هذه المعلومات أن تساعدك في إدارة المشاكل وفهم حالة أوامر الشراء.

![حالة أمر الشراء في صفحة طلب أمر الشراء.](media/cxml-monitor-po-request.png "حالة أمر الشراء في صفحة طلب أمر الشراء")

قد تظهر الشبكة الموجودة في الجزء العلوي من صفحة **طلب أمر الشراء** قيم الحالة التالية:

- **حالة إرسال الأمر** – بإمكان هذا الحقل أن يتضمن إحدى القيم التالية:

    - **قيد الانتظار** – ينتظر المستند كي يتم إرسالها.
    - **مُرسل** – تم إرسال المستند.
    - **متوقف‬‏‫** – تم وضع علامة _متوقف‬‏‫_ على المستند قبل إرساله. (لوضع علامة _متوقف‬‏‫_ على مستند قبل إرساله، حدد **توقف** في جزء الإجراءات في صفحة **طلب الشراء**.)
    - **أرشفة** – تمت إزالة المستند. (لإزالة مستند، حدد **إزالة** في جزء الإجراءات في صفحة **طلب الشراء**.)

- **حالة مورّد طلب الأمر‬‏‫** – بإمكان هذا الحقل أن يتضمن إحدى القيم التالية:

    - **قيد الانتظار** – ينتظر المستند كي يتم إرسالها.
    - **تم الإقرار بالاستلام** – تم الإقرار باستلام هذا المستند بواسطة المورّد. يمكنك مراجعة رسالة XML المفصلة المرتجعة من المورّد عن طريق تحديد علامة التبويب **استجابة XML‏‎** في الجزء السفلي من الصفحة.
    - **خطأ** – تم إرسال المستند إلى المورّد، ولكن حدث خطأ‏‎. يمكنك مراجعة رسالة الخطأ عن طريق تحديد علامة التبويب **استجابة XML‏‎** في الجزء السفلي من الصفحة.

قد تعرض الشبكة **محفوظات طلبات أوامر الشراء** في الجز السفلي من صفحة **طلب أمر الشراء** القيم التالية:

- **نوع طلب الأمر‬‏‫** – بإمكان هذا الحقل أن يتضمن إحدى القيم التالية:

    - **جديد** - يتم وضع علامة على البند كبند جديد مباشرة بعد تأكيد أمر الشراء.
    - **تحديث‏‎** – إذا تم بالفعل إرسال تأكيد وأقر المورّد باستلامه، فسيتم وضع علامة _تحديث‏‎_ على التأكيد التالي. سيتم إرسال التحديثات فقط عند تعيين الخيار **إرسال تحديثات طلب الشراء** إلى *نعم* في [معلمات cXML العمومية](#cxml-parameters).
    - **حذف** – إذا تم بالفعل إرسال تأكيد وأقر المورّد باستلامه، ولكن تم إلغاء أمر الشراء، فسيت وضع علامة ‬‏‫ _حذف_ على التأكيد قيد الانتظار. سيتم إرسال عمليات الحذف فقط عند تعيين الخيار **إرسال حذف طلب الشراء** إلى *نعم* في [معلمات cXML العمومية](#cxml-parameters).

- **وقت الطلب** – وقت إنشاء تأكيد الأمر. يمكنك مقارنة وقت الطلب مع وقت حالة الأمر لتحديد الوقت بين التأكيد وإقرار المورّد بالاستلام.
- **حالة إرسال الأمر** – هذا الحقل هو نفسه الحقل **حالة إرسال الأمر** في الجزء العلوي من الصفحة. إنه يتكرر هنا لتسهيل عرض الحالة عند مستوى التأكيد. إذا تم تعيين الحقل **نوع طلب الأمر** إلى *جديد*، وتمت إعادة تأكيد الأمر قبل إرسال تأكيد، يتم تعيين حقل **حالة إرسال الأمر** إلى *أرشفة*.
- **وقت حالة الأمر** – وقت التحديث الأمير لسجل محفوظات طلبات أوامر الشراء. (تتضمن التحديثات تغييرات الحالة.)
- **حالة مورّد طلب الأمر** – هذا الحقل هو نفسه الحقل **حالة مورّد طلب الأمر** في الجزء العلوي من الصفحة. إنه يتكرر هنا لتسهيل عرض الحالة عند مستوى التأكيد.
- **وقت إعادة الإرسال** – الوقت الذي تم فيه إعادة إرسال السجل.
- **عدد مرات إعادة الإرسال** – عدد المرات التي أعيد فيها إرسال السجل. يشير الرقم المرتفع إلى حالات فشل متعددة، وقد يشير بالتالي إلى وجود مشكلة في إعداد بياناتك أو إعداد بيانات المورّد.

### <a name="view-the-xml-for-a-purchase-order-request-message"></a>عرض XML لرسالة طلب أمر شراء

لعرض XML لرسالة طلب أمر الشراء، حدد علامة التبويب **نص XML للطلب** في أسفل الصفحة **طلب أمر الشراء**. بإمكان المعلومات الموجودة في علامة التبويب هذه أن تكون مفيدة أثناء الاختبار أو التحقق من صحة الأخطاء. لتسهيل قراءة المعلومات، يمكنك عرضها كرسالة منسقة. انسخ محتويات علامة التبويب إلى ملف نصي، ثم استعرضها في محرر XML.

![علامة تبويب نص XML للطلب.](media/cxml-request-xml-text.png "علامة تبويب نص XML للطلب")

### <a name="view-the-details-of-the-vendor-response"></a>عرض تفاصيل استجابة المورّد

لعرض محتوى إقرار المورّد أو استجابة خطأ، حدد علامة التبويب **استجابة XML** في أسفل صفحة **طلب أمر الشراء**.

![علامة التبويب استجابة XML.](media/cxml-response-xml.png "علامة التبويب استجابة XML")

## <a name="additional-resources"></a>الموارد الإضافية

- [إعداد كتالوج خارجي لـ PunchOut e-procurement](set-up-external-catalog-for-punchout.md)
- [استخدام الكتالوجات الخارجية للتدبير الإلكتروني PunchOut‬‬](use-external-catalogs-for-punchout.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
