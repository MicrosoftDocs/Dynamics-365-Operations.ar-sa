---
title: وجهات إعداد التقارير الإلكترونية (ER)‬
description: يوفر هذا الموضوع معلومات حول إدارة وجهات إعداد التقارير الإلكترونية‬ (ER) وأنواع الوجهات المدعومة واعتبارات الأمان.
author: nselin
manager: AnnBe
ms.date: 01/21/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 725ded9d777a65e5a38a7971c1da8cb74cf0dd47
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097271"
---
# <a name="electronic-reporting-er-destinations"></a>وجهات إعداد التقارير الإلكترونية (ER)‬

[!include [banner](../includes/banner.md)]

يمكنك تكوين وجهة لكل تكوين تنسيق بتقرير إلكتروني (ER) ومكون المخرجات (مجلد أو ملف). يمكن للمستخدمين الذين تتوفر لديهم حقوق الوصول المناسبة تعديل إعدادات الوجهة أيضًا في وقت التشغيل. يشرح هذا الموضوع إدارة وجهات التقارير الإلكترونية وأنواع الوجهات المدعومة واعتبارات الأمان.

عادة ما تحتوي تكوينات تنسيقات إعداد التقارير الإلكترونية على مكون مخرجات واحد على الأقل، وهو ملف. بشكل عام، تتضمن التكوينات مكونات مخرجات ملفات متعددة من أنواع مختلفة (على سبيل المثال، XML أو TXT أو XLSX أو DOCX أو PDF) يتم تجميعها في مجلد واحد أو عدة مجلدات. تسمح لك إدارة وجهات التقارير الإلكترونية بإجراء تكوين مسبق لما يحدث عند تشغيل كل مكون. عند تشغيل تكوين، يظهر بشكل افتراضي مربع حوار يمكنك من حفظ الملف أو فتحه. ويحدث السلوك نفسه أيضًا عند استيراد تكوين إعداد تقارير إلكترونية وعدم تكوين أي وجهات محددة له. بعد إنشاء وجهة لمكون المخرجات الرئيسي، تتجاوز تلك الوجهة السلوك الافتراضي، ويتم إرسال المجلد أو الملف وفقًا لإعدادات الوجهة.

## <a name="availability-and-general-prerequisites"></a>التوافر والشروط الأساسية

لا تتوفر وظائف وجهات إعداد التقارير الإلكترونية في Microsoft Dynamics AX 7.0 (فبراير 2016). لذلك يجب تثبيت Microsoft Dynamics 365 for Operations بالإصدار 1611 (نوفمبر 2016) أو إصدار لاحق لاستخدام أنواع الوجهات التالية:

- [البريد الإلكتروني](er-destination-type-email.md)
- [الأرشيف](er-destination-type-archive.md)
- [الملف](er-destination-type-file.md)
- [الشاشة](er-destination-type-screen.md)
- [Power BI](er-destination-type-powerbi.md)

بدلًا من ذلك، يمكنك تثبيت أحد المتطلبات الأساسية التالية. ولكن يجب أن تدرك أن هذه البدائل تقدم تجربة وجهة إعداد تقارير إلكترونية أكثر محدودية.

- الإصدار 7.0.1 من تطبيق Microsoft Dynamics AX (مايو 2016)
- [الإصلاح العاجل لتطبيق إدارة وجهة إعداد التقارير الإلكترونية](https://fix.lcs.dynamics.com/issue/results/?q=3160213)

يوجد أيضًا نوع وجهة [للطباعة](er-destination-type-print.md). لاستخدامه، يجب تثبيت Microsoft Dynamics 365 Finance بالإصدار 10.0.9 (أبريل 2020).

## <a name="overview"></a>نظرة عامة

لا يمكنك إعداد وجهات إلا لتكوينات إعداد التقارير الإلكترونية التي تم [استيرادها](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) في مثيل Finance الحالي، وللتنسيقات المتوفرة في صفحة **تكوينات إعداد التقارير الإلكترونية**. تتوفر وظيفة إدارة وجة إعداد التقارير الإلكترونية في **إدارة المؤسسة** \> **إعداد التقارير الإلكترونية** \> **وجهة إعداد التقارير الإلكترونية**.

### <a name="default-behavior"></a>السلوك الافتراضي

يعتمد السلوك الافتراضي لتكوين تنسيق ER على نوع التنفيذ الذي تحدده عند بدء تنسيق ER.

في مربع الحوار **‏‫تقرير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬** ، في علامة التبويب السريعة **‏‫تشغيل في الخلفية‬** ، إذا قمت بتعيين خيار **‏‫معالجة الدُفعات** إلى **لا** ، يتم تشغيل التنسيق ER علي الفور في الوضع التفاعلي. عند إتمام هذا التنفيذ بنجاح، يتم توفير المستند الصادر الذي تم إنشاؤه للتنزيل.

إذا قمت بتعيين خيار **معالجة الدُفعات** إلى **نعم** ، يتم تشغيل تنسيق ER في وضع [دُفعة](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/batch-processing-overview). يتم إنشاء الوظيفة الدُفعية المناسبة، استنادا إلى المعلمات التي تحددها في علامة التبويب **تشغيل في الخلفية** لمربع حوار **معلمات ER**.

> [!NOTE]
> يعلمك وصف الوظيفة بتشغيل تعيين تنسيق ER. ويحتوي أيضًا على اسم مكون ER الذي تم تنفيذه.

[![تشغيل تنسيق ER](./media/ER_Destinations-RunInBatchMode.png)](./media/ER_Destinations-RunInBatchMode.png)

يمكنك العثور على معلومات حول هذه الوظيفة في عده أماكن:

- انتقل إلى **عادي** \> **استعلامات** \> **الوظائف الدُفعية** \> **‏‫الوظائف الدفعية الخاصة بي‬** للتحقق من حاله الوظيفة المجدولة.
- انتقل إلى **إدارة المؤسسة‬** \> **التقارير الإلكترونية** \> **وظائف إعداد التقارير الإلكترونية** لفحص حاله الوظيفة المجدولة ونتائج التنفيذ للوظيفة المكتملة. عند إتمام تنفيذ الوظيفة بنجاح، حدد **إظهار الملفات** على صفحة **وظائف إعداد التقارير الإلكترونية‬‬‬‏‫** للحصول علي مستند صادر تم إنشاؤه.

    > [!NOTE]
    > يتم تخزين هذا المستند كمرفق لسجل الوظيفة الحالية ويتم التحكم فيه بواسطة إطار عمل [إدارة المستندات](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management). [نوع المستند](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) المستخدم لتخزين نتائج ER من هذا النوع يتم تكوينه في [معلمات ER](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).

- في صفحة **وظائف إعداد التقارير الإلكترونية** ، حدد **إظهار الملفات** لعرض قائمه بآيه أخطاء وتحذيرات تم إنشاؤها اثناء تنفيذ الوظيفة.

    [![مراجعة قائمة وظائف ER](./media/ER_Destinations-ReviewERJobs.png)](./media/ER_Destinations-ReviewERJobs.png)

### <a name="user-configured-behavior"></a>سلوك مكون من قبل المستخدم

في صفحة **وجهة إعداد التقارير الإلكترونية**، يمكنك تجاوز السلوك الافتراضي لتكوين. لا تظهر التكوينات المستوردة في هذه الصفحة حتى تحدد **جديد**، ثم تحدد تكوينًا لإنشاء إعدادات وجهة له في حقل **المرجع**.

[![تحديد تكوين في حقل المرجع](./media/ER_Destinations-SelectFormat.png)](./media/ER_Destinations-SelectFormat.png)

وبعد إنشاء مرجع، يمكنك إنشاء وجهه ملف لكل مكون مخرجات **مجلد** أو **ملف** لتنسيق إعداد التقارير الإلكترونية المشار إليه.

[![إنشاء وجهة الملف](./media/ER_Destinations-ConfigureElementDestination.png)](./media/ER_Destinations-ConfigureElementDestination.png)

ويمكنك عندئذٍ تمكين الوجهات الفردية وتعطيلها لوجهة الملف في مربع الحوار **إعدادات الوجهة‬**. يُستخدم الزر **إعدادات** الزر للتحكم في كافة الوجهات لوجهة ملف محدد. في مربع الحوار **إعدادات الوجهة**، يمكنك التحكم في كل وجهة على حدة بإعداد الخيار **ممكّن‬** لها.

ملاحظة: في إصدارات Finance **السابقة للإصدار 10.0.9** يمكنك إنشاء **وجهة ملف واحد** لكل مكون مخرجات من التنسيق نفسه، مثل مجلد أو ملف تم تحديده في حقل **اسم الملف**. ولكن في **الإصدار 10.0.9 والإصدارات اللاحقة** يمكنك إنشاء **وجهات ملفات متعددة** لكل مكون مخرجات بنفس التنسيق.

على سبيل المثال، يمكنك استخدام هذه الإمكانية لتكوين وجهات الملف لمكون ملف يتم استخدامه لإنشاء مستند صادر بتنسيق Excel. يمكن تكوين وجهة واحدة ([الأرشيف](er-destination-type-archive.md)) لتخزين ملف excel الأصلي في أرشيف وظائف إعداد التقارير الإلكترونية، ويمكن تكوين وجهة أخرى ([البريد الإلكتروني](er-destination-type-email.md))[ لتحويل](#OutputConversionToPDF) ملف excel إلى تنسيق pdf وإرسال ملف PDF بالبريد الإلكتروني في وقت واحد.

[![تكوين وجهات متعددة لعنصر بتنسيق واحد](./media/ER_Destinations-SampleDestinations.png)](./media/ER_Destinations-SampleDestinations.png)

عند تشغيل التنسيق الخاص ب ER ، يتم دوما تشغيل كافة الوجات التي تم تكوينها لمكونات التنسيق. بالاضافه إلى ذلك، في **إصدار ال10.0.17 المالي** والإصدارات التالية، تم تحسين وظيفة وجات ER ويسمح لك الآن بتكوين مجموعات مختلفه من الوجهات لأحد التنسيقات المفردة ل ER. يقوم هذا التكوين بتمييز كل مجموعه تم تكوينها لاجراء مستخدم معين. تم [توسيع](er-apis-app10-0-17.md) واجهه برمجه التطبيقات ل ER حتى يمكن توفير اجراء يقوم المستخدم باجراءه عن طريق تشغيل أحد تنسيقات ER. يتم تمرير كود الاجراء المتوفر إلى وجهات ER. يمكنك تشغيل وجهات مختلفه لتنسيق ER، وذلك وفقا لكود الاجراء المتوفر. لمزيد من المعلومات، راجع [تكوين وجهات ER المعتمدة علي الاجراء](er-action-dependent-destinations.md).

## <a name="destination-types"></a>أنواع الوجهات

الوجهات التالية مدعومة حاليًا لتنسيقات إعداد التقارير الإلكترونية. ويمكنك تعطيل كافة الأنواع أو تمكينها في الوقت نفسه. وبهذه الطريقة، يمكنك إما عدم القيام بأي شيء أو إرسال المكون إلى جميع الجهات المكّونة.

- [البريد الإلكتروني](er-destination-type-email.md)
- [الأرشيف](er-destination-type-archive.md)
- [الملف](er-destination-type-file.md)
- [الشاشة](er-destination-type-screen.md)
- [Power BI](er-destination-type-powerbi.md)
- [طباعة](er-destination-type-print.md)

## <a name="applicability"></a>إمكانية التطبيق

يمكنك إعداد تكوينات فقط لوجهات التقارير الإلكترونية التي تم استيرادها، وللتنسيقات المتوفرة في صفحة **تكوينات التقارير الإلكترونية**.

> [!NOTE]
> الوجهات المكونة خاصة بشركة معينة. إذا كنت تخطط لاستخدام أحد تنسيقات إعداد التقارير الإلكترونية في شركات مختلفة من مثيل Finance الحالي، يجب تكوين وجهات لتنسيق إعداد التقارير الإلكترونية هذا لكل شركة من هذه الشركات.

عندما تقوم بتكوين وجهات ملف لتنسيق محدد، فإنك تكوِّنها للتنسيق بالكامل.

[![ارتباط التكوين](./media/ER_Destinations-ConfigurationLink.png)](./media/ER_Destinations-ConfigurationLink.png)

وفي الوقت نفسه، قد يكون لديك [إصدارات](general-electronic-reporting.md#component-versioning) متعددة من التنسيق الذي تم استيراده إلى مثيل Finance الحالي. يمكنك عرضها بتحديد ارتباط **التكوين** الذي يتم عرضه عند تحديد حقل **المرجع**.

[![إصدارات التكوين](./media/ER_Destinations-ConfigurationVersions.png)](./media/ER_Destinations-ConfigurationVersions.png)

بصورة افتراضية، لا يتم تطبيق الوجهات المكونة إلا عند تشغيل إصدار تنسيق إعداد التقارير الإلكترونية بالحالة **مكتمل** أو **مشترك**. ولكن يجب في بعض الأحيان استخدام الوجهات المكونة عند تشغيل إصدار المسودة لتنسيق إعداد التقارير الإلكترونية. على سبيل المثال تعدِّل إصدار مسودة من تنسيق لديك، وترغب في استخدام وجهات مكونة لاختبار كيفية تسليم المخرجات التي يتم إنشاؤها. اتبع الخطوات التالية لتطبيق الوجهات لتنسيق إعداد التقارير الإلكترونية عند تشغيل إصدار المسودة.

1. انتقل إلى **إدارة المؤسسة** \> **التقارير الإلكترونية** \> **التكوينات**.
2. في صفحة **التكوينات**، في جزء الإجراءات، في علامة التبويب **التكوينات**، في مجموعة **الإعدادات المتقدمة**، حدد **معلمات المستخدمين**.
3. عيِّن الخيار **استخدام الوجهات للحالة مسودة** على **نعم**.

[![خيار استخدام الوجهات للحالة مسودة](./media/ER_Destinations-UserSetting1.png)](./media/ER_Destinations-UserSetting1.png)

لاستخدام إصدار المسودة لتنسيق إعداد التقارير الإلكترونية، يجب وضع علامة على تنسيق إعداد التقارير الإلكترونية وفقًا لذلك.

1. انتقل إلى **إدارة المؤسسة** \> **التقارير الإلكترونية** \> **التكوينات**.
2. في صفحة **التكوينات**، في جزء الإجراءات، في علامة التبويب **التكوينات**، في مجموعة **الإعدادات المتقدمة**، حدد **معلمات المستخدمين**.
3. عيّن الخيار **تشغيل الإعداد** على **نعم**.

[![خيار تشغيل الإعداد](./media/ER_Destinations-UserSetting2.png)](./media/ER_Destinations-UserSetting2.png)

بعد إكتمال هذا الإعداد، يصبح الخيار **تشغيل المسودة** متوفرًا لتنسيقات إعداد التقارير الإلكترونية التي تقوم بتعديلها. عيِّن هذا الخيار على **نعم** لبدء استخدام إصدار المسودة من التنسيق عند تشغيل التنسيق.

[![خيار تشغيل المسودة](./media/ER_Destinations-FormatSetting.png)](./media/ER_Destinations-FormatSetting.png)

## <a name="destination-failure-handling"></a><a name="DestinationFailure"></a>معالجة فشل الوجهة

عادة ما يتم تشغيل تنسيق إعداد التثارير الإلكترونية في نطاق عملية تجارية محددة. ولكن يجب في بعض الأحيان اعتبار تسليم المستند الصادر الذي يتم إنشاؤه أثناء تنفيذ أحد تنسيقات إعداد التقارير الإلكترونية جزءًا من هذه العملية التجارية. وفي هذه الحالة، في حالة فشل تسليم المستند الصادر الذي تم إنشاؤه إلى وجهة مكونة، يجب إلغاء تنفيذ العملية التجارية. لتكوين وجهة إعداد التقارير الإلكترونية المناسبة، حدد الخيار **إيقاف المعالجة عند الفشل**.

على سبيل المثال، تقوم بتكوين معالجة دفع مورد حتى يتم تشغيل تنسيق إعداد التقارير الإلكترونية لـ **تحويل ائتمان‬ ISO20022** لإنشاء ملف الدفع والمستندات المكملة (على سبيل المثال، خطاب الإرفاق وتقرير التحكم). في حالة ضرورة معالجة الدفع بنجاح فقط في حالة تسليم خطاب الإرفاق بالبريد الإلكتروني، يجب تحديد خانة الاختيار **إيقاف المعالجة عند الفشل** لمكون **CoveringLetter** في وجهه الملف المناسبة، كما هو موضح في الرسم التوضيحي التالي. في هذه الحالة، سيتم تغيير حالة الدفع المحددة للمعالجة من **لا شيء** إلى **تم الإرسال** فقط عند قبول خطاب الإرفاق الذي تم إنشاؤه للتسليم بنجاح بواسطة موفر بريد إلكتروني تم تكوينه في مثيل Finance.

[![فشل معالجة تكوين العملية لوجهة الملف](./media/ER_Destinations-StopProcessingAtDestinationFailure.png)](./media/ER_Destinations-StopProcessingAtDestinationFailure.png)

في حالة مسح خانة الاختيار **إيقاف المعالجة عند الفشل** لمكون **CoveringLetter** في الوجهة، سيتم اعتبار إتمام الدفع بنجاح حتى لو لم يتم تسليم خطاب الإرفاق عبر البريد الإلكتروني بنجاح. سيتم تغيير حالة الدفع من **لا شيء** إلى **تم الإرسال** حتى في حالة تعذر إرسال خطاب الإرفاق لفقدان عنوان البريد الكتروني للمستلم أو المرسل أو عدم صحته على سبيل المثال.

## <a name="output-conversion-to-pdf"></a><a name="OutputConversionToPDF"></a>تحويل المخرجات إلى PDF

يمكنك استخدام خيار تحويل إلى PDF لتحويل المخرجات في Microsoft Office بتنسيق (Excel أو Word) إلى تنسيق PDF.

### <a name="make-pdf-conversion-available"></a>إتاحة التحويل إلى PDF

لإتاحة خيار التحويل إلى PDF في مثيل Finance الحالي، افتح مساحة عمل **إدارة الميزات**، وشغل ميزة **تحويل مستندات إعداد التقارير الإلكترونية الصادرة من تنسيقات Microsoft Office إلى PDF**.

[![ميزة تشغيل تحويل المستندات الصادرة إلى PDF في إدارة الميزات](./media/ER_Destinations-EnablePdfConversionFeature.png)](./media/ER_Destinations-EnablePdfConversionFeature.png)

### <a name="applicability"></a>إمكانية التطبيق

لا يمكن تشغيل خيار التحويل إلى PDF إلا لمكونات الملفات المستخدمة لإنشاء مخرجات بتنسيق Office (Word أو Excel) (**ملف Excel**). عند تشغيل هذا الخيار، يتم تحويل المخرجات التي يتم إنشاؤها بتنسيق Office تلقائيًا إلى تنسيق PDF.

### <a name="limitations"></a>قيود

> [!NOTE]
> هذه الميزة هي ميزة معاينة وهي خاضعة لشروط الاستخدام الموضحة في [شروط الاستخدام الإضافية لمعاينات المستخدمة لمعاينات Microsoft Dynamics 365](https://go.microsoft.com/fwlink/?linkid=2105274).

لا يكون خيار التحويل إلى PDF إلا لعمليات نشر المجموعة فقط.

يوجد حد أقصى لمستند PDF الناتج بطول 300 صفحة.

في Finance **الإصدار 10.0.9**، لا يتم دعم إلا اتجاه الصفحة الأفقي فقط في مستند PDF الذي يتم إنتاجه من مخرجات Excel. في Finance **الإصدار 10.0.10 (مايو 2020) أو أحدث**، يمكنك [تحديد اتجاه الصفحة](#SelectPdfPageOrientation) في مستند PDF التي يتم إنتاجها من مخرجات Excel أثناء قيامك بتكوين وجهة ER.

لا يتم استخدام إلا خطوط النظام الشائعة لنظام تشغيل Window لتحويل مخرجات لا تحتوي على خطوط مضمنة.

### <a name="use-the-pdf-conversion-option"></a>استخدام خيار التحويل إلى PDF

لتشغيل التحويل إلى PDF لوجهة ملف، حدد خانة الاختيار **التحويل إلى PDF**.

[![تشغيل التحويل إلى PDF لوجهة ملف](./media/ER_Destinations-TurnOnPDFConversion.png)](./media/ER_Destinations-TurnOnPDFConversion.png)

### <a name=""></a><a name="SelectPdfPageOrientation">حدد اتجاه صفحة تحويل PDF</a>

إذا قمت بإنشاء تكوين ER بتنسيق Excel وتريد تحويله إلى تنسيق PDF، يمكنك تعيين اتجاه مستند PDF. عندما تقوم بتحديد خانة الاختيار **التحويل إلى PDF** لتشغيل تحويل PDF لوجهm ملف تنتج ملف مخرجات بتنسيق Excel، فإن حقل **اتجاه الصفحة** يصبح متاحًا على علامة التبويب السريع **إعدادات تحويل PDF**. في حقل **اتجاه الصفحة**، حدد الاتجاه المفضل.

[![حدد اتجاه صفحة تحويل PDF](./media/ER_Destinations-SelectPDFConversionPageOrientation.png)](./media/ER_Destinations-SelectPDFConversionPageOrientation.png)

> [!NOTE]
> حتى يكون لديك خيار لتحديد اتجاه صفحه PDF، يجب عليك تثبيت Finance، الإصدار 10.0.10 أو إصدار لاحق.
>
> يتم تطبيق اتجاه الصفحة المحدد على كافة تكوينات ER التي تم إنشاؤها بتنسيق Excel ثم يتم تحويلها إلى تنسيق PDF.
>
> إذا تم تحويل تكوين ER باستخدام تنسيق Word إلى تنسيق PDF محول، فان اتجاه المستند الخاص بـ PDF يتم الحصول عليه من مستند Word.

## <a name="security-considerations"></a>اعتبارات الأمان

يتم استخدام نوعين من الامتيازات والواجبات لوجهات التقارير الإلكترونية. يتحكم أحد النوعين في قدرة المستخجم العامة على الاحتفاظ بالوجهات التي تم تكوينها لكيان قانوني (أي التحكم في الوصول إلى صفحة **وجهات إعداد التقارير الإلكترونية**). أما النوع الآخر فيتحكم في قدرة مستخدم التطبيق على تجاوز، في وقت التشغيل، إعدادات الوجهة التي تم تكوينها بواسطة مطور إعداد التقارير الإلكترونية أو مستشار وظائف إعداد التقارير الإلكترونية.

| الدور (اسم AOT)                     | اسم الدور                                  | الواجب (اسم AOT)                     | اسم المهمة                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| ERDeveloper                         | مطور التقارير الإلكترونية             | ERFormatDestinationConfigure        | تكوين وجهة ‏‫تنسيق التقارير الإلكترونية‬                |
| ERFunctionalConsultant              | مستشار وظائف التقارير الإلكترونية | ERFormatDestinationConfigure        | تكوين وجهة ‏‫تنسيق التقارير الإلكترونية‬                |
| PaymAccountsPayablePaymentsClerk    | موظف مدفوعات الحسابات الدائنة            | ERFormatDestinationRuntimeConfigure | تكوين وجهة ‏‫تنسيق التقارير الإلكترونية‬ أثناء وقت التشغيل |
| PaymAccountsReceivablePaymentsClerk | موظف مدفوعات الحسابات المدينة         | ERFormatDestinationRuntimeConfigure | تكوين وجهة ‏‫تنسيق إعداد التقارير الإلكترونية‬ أثناء وقت التشغيل |

> [!NOTE]
> يتم استخدام امتيازين في الواجبات السابقة. هذان الامتيازان لهما الأسماء نفسها للواجبات المناظرة: **ERFormatDestinationConfigure** و **ERFormatDestinationRuntimeConfigure**.

## <a name="frequently-asked-questions"></a>الأسئلة المتداولة

### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>لقد قمت باستيراد تكوينات الإلكترونية، وأراها فقط على صفحة تكوينات التقارير الإلكترونية. ولكن لماذا لا يمكنني رؤيتها في صفحة وجهات التقارير الإلكترونية؟

تأكد من تحديد **جديد**، ثم حدد تكوين في حقل **المرجع**. لا تظهر صفحات **وجهات إعداد التقارير الإلكترونية** إلا التكوينات التي تم تكوين الوجهات لها.

### <a name="is-there-any-way-to-define-which-microsoft-azure-storage-account-and-azure-blob-storage-are-used"></a>هل ثمة طريقة لتحديد حساب تخزين Microsoft Azure ومخزن البيانات الثنائية الكبيرة الحجم لـ Azure المستخدمين؟

الرقم يتم تحديد تخزين Microsoft Azure الافتراضي واستخدامه لنظام إدارة المستندات.

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>ما هو غرض وجهة الملف في إعداد الوجهة؟ ما الذي يفعله هذا الإعداد؟

يتم استخدام وجهه **الملف** للتحكم في أحد مربعات الحوار في مستعرض الويب الخاص بك عند تشغيل تنسيق ER في الوضع التبادلي. في حالة تمكين هذه الوجهة، أو في حالة عدم تحديد وجهة لتكوين، يظهر مربع حوار الفتح أو الحفظ في مستعرض الويب بعد إنشاء ملف مخرجات.

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>هل يمكنك إعطاء مثال عن معادلة تشير إلى حساب مورّد يمكنني إرسال بريد إلكتروني له؟

تتعلق المعادلة بتكوين التقارير الإلكترونية. على سبيل المثال، إذا كنت تستخدم تكوين نقل الائتمان ISO 20022، فيمكنك استخدام **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID** أو **model.Payments.Creditor.Identification.SourceID** للحصول على حساب مورّد مقترن.

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-grouped-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>يحتوي أحد تكوينات التنسيق لديّ على ملفات متعددة مجمعة في مجلد واحد (على سبيل المثال، يحتوي Folder1 على File1 وFile2 وFile3). كيف يمكنني إعداد الوجهات بحيث لا يتم إنشاء Folder1.zip على الإطلاق ويتم إرسال File1 بواسطة البريد الإلكتروني وإرسال File2 إلى SharePoint ويمكنني فتح File3 فور تشغيل التكوين؟

يجب أن يكون التنسيق متوفرًا في تكوينات إعداد التقارير الإلكترونية. وباستيفاء هذا المتطلب الأساسي، افتح صفحة **وجهة إعداد التقارير الإلكترونية**، وأنشئ مرجعًا جديدًا للتكوين. بعد ذلك، يجب أن يكون لديك أربع وجهات للملفات، واحدة لكل مكون مخرجات. أنشئ وجهة الملف الأول مع إعطائها اسم مثل **Folder**، وحدد اسم ملف يمثل مجلدًا في تكوينك. ثم حدد **الإعدادات**، وتأكد من تعطيل جميع الوجهات. بالنسبة إلى وجهة الملف هذه، لن يتم إنشاء المجلد. بشكل افتراضي، وبسبب تبعيات التدرج الهرمي بين الملفات والمجلدات الأصلية، سوف تتصرف الملفات بنفس الطريقة. بعبارات أخرى، لن يتم إرسالها إلى أي مكان. لتجاوز هذا السلوك الافتراضي، يجب عليك إنشاء ثلاث وجهات ملفات إضافية، وجهة لكل ملف. في إعدادات الوجهة لكل ملف، يجب تمكين الوجهة التي يجب إرسال الملف إليها.

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على إعداد التقارير الإلكترونية (ER)](general-electronic-reporting.md)

[تكوين وجهات ER المعتمدة علي الاجراء](er-action-dependent-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]