---
title: إعداد وتصميم تنسيقات إيصالات الاستلام
description: تصف هذه المقالة كيفية تعديل تخطيطات النماذج للتحكم في كيفية طباعة الإيصالات والفواتير والمستندات الأخرى. يتضمن Dynamics 365 Commerce مصمم تخطيط النموذج الذي يمكنك استخدامه لإنشاء مختلف أنواع تخطيطات النماذج وتعديلها بسهولة.
author: BrianShook
ms.date: 09/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFormLayout
audience: Application User
ms.reviewer: josaw
ms.custom: 57841
ms.assetid: e530dd8e-95e2-4021-90bd-ce1235f9e250
ms.search.region: global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: dac0ad75ff35367b5d6ac84c75c68e22e2cb0cb1
ms.sourcegitcommit: f4823a97c856e9a9b4ae14116a43c87f9482dd90
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/09/2021
ms.locfileid: "7779391"
---
# <a name="set-up-and-design-receipt-formats"></a>إعداد وتصميم تنسيقات إيصالات الاستلام

[!include [banner](includes/banner.md)]

تصف هذه المقالة كيفية تعديل تخطيطات النماذج للتحكم في كيفية طباعة الإيصالات والفواتير والمستندات الأخرى. يتضمن Dynamics 365 Commerce مصمم تخطيط النموذج الذي يمكنك استخدامه لإنشاء مختلف أنواع تخطيطات النماذج وتعديلها بسهولة.

> [!IMPORTANT]
> يجب عليك إعداد تخطيطات النماذج وملفات تعريف الإيصالات لطباعة الإيصالات والمستندات الأخرى من Retail Modern POS وCloud POS. يمكنك تضمين تخطيطات نموذج متعددة في ملف تعريف الإيصال.‬ ثم يمكنك تعيين ملف تعريف الإيصال إلى طابعة عن طريق تعديل ملف تعريف جهاز.

## <a name="set-up-a-receipt-format"></a>إعداد تنسيق إيصال

1. انقر فوق **Retail and Commerce** &gt; **إعداد القناة** &gt; **إعداد نقطة البيع** &gt; **نقطة البيع** &gt; **تنسيقات الإيصالات**.
2. في الصفحة **تنسيق إيصال**، انقر فوق **جديد** لإنشاء تخطيط نموذج جديد أو حدد تخطيط نموذج حالي.
3. في الحقل **تنسيق إيصال** أدخل معرفًا لتخطيط النموذج، ثم حدد نوع الإيصال الذي يتم استخدام هذا التخطيط له. يمكنك أيضًا إدخال وصف واسم مختصر للإيصال في الحقل **عنوان**.
4. في علامة التبويب السريعة **العام**، حدد خيارًا لتحديد سلوك الطباعة:

    - **الطباعة دومًا** – تتم طباعة الإيصال تلقائيًا، كما هو مناسب.
    - **عدم الطباعة** – لا يتم طباعة الإيصال.
    - **مطالبة المستخدم** – مطالبة المستخدم لطباعة الإيصال.
    - **كما هو مطلوب** – يستخدم هذا الخيار فقط لإيصالات استلام الهدايا. عند تحديد هذا الخيار، يستطيع المستخدم طباعة إيصال هدايا من الصفحة **تغيير**، في حالة طلب إيصال هدايا.

## <a name="print-images"></a>طباعة الصور

يتضمن مصمم الإيصالات متغير **شعار**. يمكنك استخدام هذا المتغير لتحديد صورة يجب طباعتها على الإيصالات. يجب أن تكون الصور التي تُطبع على الإيصالات باستخدام متغير **الشعار** من أنواع ملفات الصور النقطية الأحادية اللون (bmp.). إذا تم تحديد صورة نقطية في مصمم الإيصالات ولكنها لم تُطبع عند إرسال الإيصال إلى الطابعة، فقد يعود السبب إلى إحدى المشاكل التالية:

- حجم الملف كبير جدًا، او أبعاد البكسل في الصورة غير متوافقة مع الطابعة. في هذه الحالة، حاول تقليل دقة أو ابعاد ملف الصورة.
- لا تقوم بعض برامج تشغيل الطابعات Object Linking and Embedding for Point of Sale (OPOS) بتطبيق أسلوب **PrintMemoryBitmap** الذي تستخدمه محطات الأجهزة لطباعة صور الشعارات. في هذه الحالة، حاول إضافة العلامة التالية إلى الملف **HardwareStation.Extension.config** لمحطة الأجهزة المخصصة أو المشتركة:

    `<add name="HardwareStation.UsePrintBitmapMethod" value="true"/>`

## <a name="design-a-receipt-format"></a>تصميم تنسيق إيصال

استخدم مصمم تخطيط النماذج لإنشاء تخطيط رسومي لمستند النموذج. تحتوي صفحة **مصمم تنسيق الإيصال** على ثلاثة أجزاء: **رأس الصفحة** **والسطور** و **التذييل**. تستخدم بعض أنواع التخطيطات النماذج عناصر مشتقة من الأقسام الثلاثة جميعها، بينما تستخدم أنواع أخرى عناصر مشتقة من قسم واحد أو قسمين فقط. لعرض العناصر المتوفرة لكل قسم، انقر فوق الزر المناسب في جزء التنقل الموجود بالجانب الأيسر من الصفحة.

1. انقر فوق **Retail and Commerce** &gt; **إعداد القناة** &gt; **إعداد نقطة البيع** &gt; **نقطة البيع** &gt; **تنسيقات الإيصالات**.
2. على الصفحة **تنسيق إيصال**، حدد تخطيط نموذج ثم انقر فوق **مصمم**.
3. انقر فوق **تشغيل** للبدء في تثبيت مضيف مصمم Commerce.
4. في شريط الإعلام الذي يظهر أسفل نافذة Internet Explorer، انقر فوق **فتح** لبدء تثبيت المصمم بنقرة واحدة. (قد يظهر شريط الإعلام في موقع مختلف في مستعرضات أخرى).‬ ‏‫يُظهر مؤشر التقدم تقدم عملية التثبيت.‬
5. بعد اكتمال عملية التثبيت، أدخل اسم مستخدم Commerce وكلمة مرور، ثم انقر فوق **تسجيل الدخول** لبدء تشغيل المصمم.
6. بعد أن يتم التحقق من صحة بيانات الاعتماد الخاصة بك ويبدأ تشغيل المصمم، يمكنك بدء في تصميم تنسيق إيصال الاستلام أو تعديل تنسيق موجود.
7. لإنشاء عناصر النموذج، حدد القسم **رأس الصفحة** أو **السطور** أو **التذييل**، ثم  عنصرًا من هذا القسم إلى مساحة العمل. تحتوي معظم العناصر على متغيرات يتم ملئها تلقائيًا ببيانات من قاعدة البيانات. وتتيح لك عناصر أخرى مثل **نص** إمكانية طباعة نص مخصص على الإيصال.

    > [!NOTE]
    > يمكنك تحديد عدد السطور التي سيمتد عبر كل قسم عن طريق تعديل الرقم في الجزء الأيمن السفلي من هذا القسم. لتسهيل تعديل قسم، قم بزيادة ارتفاعه بسحب شريط تغيير الحجم بأسفل القسم. لا يؤثر ارتفاع القسم في مساحة العمل على عدد البنود في الإيصال الفعلي.

8. بعد أن تقوم بسحب عنصر إلى مساحة العمل، قم بتعيين الخصائص للجزء الموجود في جزء **معلومات الكائن** الذي يقع أسفل الصفحة. أدخل إعدادًا واحدًا أو أكثر مما يلي:

    - **محاذاة**: – يمكنك من خلال هذا الإعداد تعيين محاذاة الحقل إما على **اليسار** أو **اليمين**.
    - **حرف التعبئة** – حدد حرف المسافة البيضاء. بشكل افتراضي، يتم استخدام مساحة فارغة، ولكن يمكنك إدخال أي حرف.
    - **البادئة** – أدخل القيمة التي تظهر في بداية الحقل. لا يتم تطبيق هذا الإعداد إلا على جزء **سطور** التخطيط.
    - **أحرف** – حدد الحد الأقصى لعدد الأحرف التي يمكن أن يحتوي عليها الحقل إذا كان العنصر يحتوي على متغير. إذا كان النص الموجود في الحقل أطول من عدد الأحرف الذي تحدده، يتم اقتطاع النص لاحتوائه في الحقل.
    - **المتغير** – يتم تحديد خانة الاختيار هذه تلقائيًا إذا كان العنصر يحتوي على متغير ولا يمكن تخصيصه.
    - **نوع الخط** – قم بتعيين نمط الخط إما **عادي** أو **غامق**. تشغل الحروف المكتوبة بالخط الغامق ضعف المساحة التي تشغلها الحروف العادية. ولذلك، قد يمكن اقتطاع بعض الحروف.
    - **حجم الخط** – قم بتعيين حجم الخط **عادي** أو **غامق**. تكون الأحرف الكبيرة أكبر بمرتين من الأحرف العادية. لذلك، قد يؤدي استخدام الأحرف الكبيرة إلى تراكب النص في إيصال الاستلام.
    - **الحذف** - انقر فوق هذا الزر لإزالة الجزء المحدد من تخطيط النموذج.

## <a name="assign-receipt-profiles"></a>تعيين ملفات تعريف الإيصالات

يتم تعيين ملفات تعريف الإيصالات مباشرة إلى الطابعات من خلال ملف تعريف الجهاز.

1. افتح ملف تعريف الجهاز بواسطة النقر فوق **Retail and Commerce** &gt; **إعداد القناة** &gt; **إعداد نقطة البيع** &gt; **ملفات تعريف نقاط البيع** &gt; **ملف تعريف الأجهزة**.
2. حدد الطابعة، ثم، في الحقل **ملف تعريف الإيصال**، قم تعيين ملف تعريف الإيصال لاستخدامه في السجل.

> [!NOTE]
> إذا تم استخدام طابعتين، فيمكن استخدام طابعة واحدة لطباعة إيصالات حرارية قياسية من 40 عمودًا. يتم استخدام الطابعة الثانية بشكل نموذجي لطباعة أنواع إيصالات ملء الصفحة تتطلب المزيد من المعلومات. تتضمن أنواع الإيصالات هذه إيصالات أمر العميل وفواتير العملاء.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
