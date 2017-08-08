---
title: "متطلبات النظام"
description: "يسرد هذا الموضوع متطلبات النظام للإصدار الحالي من Microsoft Dynamics 365 Finance and Operations, Enterprise edition لعمليات النشر في السحابة وفي الموقع المحلي."
author: sericks007
manager: AnnBe
ms.date: 07/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: robinr
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30T00:00:00.000Z
ms.dyn365.ops.version: Platform update 2
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 871ba89973f6af341c536f67db056bebb54600b3
ms.contentlocale: ar-sa
ms.lasthandoff: 07/25/2017

---

# <a name="system-requirements"></a>متطلبات النظام

[!include[banner](../includes/banner.md)]


يسرد هذا الموضوع متطلبات النظام للإصدار الحالي من Microsoft Dynamics 365 Finance and Operations, Enterprise edition، لعمليات النشر في السحابة وفي الموقع المحلي. قبل تثبيت Finance and Operations، عندما يكون ذلك ملائمًا، تحقق من أن النظام الذي تستخدمه يستوفي الحد الأدنى من متطلبات الشبكة والأجهزة والبرامج أو يتجاوزه.


## <a name="supported-microsoft-office-applications"></a>تطبيقات Microsoft Office المعتمدة
يتم اعتماد تطبيقات Office التالية أثناء عمليات نشر Finance and Operations في السحابة وفي الموقع المحلي.
-   لتثبيت الوظائف الإضافية لـ Microsoft Excel و Word، يجب أن يكون لديك Microsoft Office 2016 لـ Windows أو Mac مثبتًا. للحصول على مزيد من التفاصيل حول متطلبات الإصدار، راجع [استكشاف وإصلاح مشاكل تكامل Office](/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   لعرض المستندات التي تم إنشاؤها بواسطة التصدير إلى وظائف Word أو التصدير إلى Excel، يجب عليك تثبيت Microsoft Office 2007 أو الإصدار الأحدث.

# <a name="system-requirements-specific-to-cloud-deployments"></a>متطلبات النظام الخاصة بعمليات النشر في السحابة
## <a name="network-requirements"></a>متطلبات الشبكة
-   تم تصميم Finance and Operations للشبكات مع زمن وصول من 250-300 مللي ثانية أو أقل. هذا هو زمن الوصول من عميل مستعرض إلى مركز بيانات Microsoft Azure الذي يستضيف Finance and Operations. نوصي باختبار زمن وصول الشبكة على <http://www.azurespeed.com>.
-   تعتمد متطلبات عرض النطاق الترددي لـ Finance and Operations على السيناريو الخاص بك. تتطلب السيناريوهات الأكثر شيوعاً عرض نطاق ترددي لأكثر من 50 كيلو بايت في الثانية (KBps). ولكن، بالنسبة للسيناريوهات التي لها متطلبات حمولة عالية، مثل مساحات العمل أو السيناريوهات التي تشمل تخصيص واسع، فنوصي بأكثر من عرض نطاق ترددي.

وبوجه عام، تم تحسين Finance and Operations للإنترنت. يعتبر عدد الجولات من عميل مستعرض إلى مركز البيانات Azure صغير جدًا، ويتم ضغط حمولة كاملة. 

> [!WARNING]
> لا تقم بحساب متطلبات النطاق الترددي من موقع عميل من خلال ضرب عدد المستخدمين في متطلبات الحد الأدنى للنطاق الترددي. يُصعب للغاية حساب الاستخدام المستزامن لموقع ما. بالنسبة للعملاء المهتمين بشأن متطلبات النطاق الترددي، استخدام إصدار المعاينة لـ Finance and Operations.

## <a name="net-framework-requirements"></a>متطلبات .NET Framework
يتطلب Finance and Operations الإصدار 4.6.2 من .NET Framework لجميع تطبيقات النقرة الواحدة، مثل عامل توجيه المستند. للحصول على إرشادات التثبيت، راجع [تثبيت.NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-web-browsers"></a>مستعرضات الويب المدعومة
يمكن تشغيل تطبيق ويب في أيٍّ من مستعرضات الويب التالية التي تعمل على أنظمة التشغيل المحددة:


-   Microsoft Edge (أحدث إصدار تمت إتاحته للجمهور) على Windows 10
-   Internet Explorer 11 على Windows 10 أو Windows 8.1 أو Windows 7
-   Google Chrome (أحدث إصدار تمت إتاحته) على Windows 10 أو Windows 8.1 أو Windows 8 أو Windows 7 أو Google Nexus 10 tablet
-   Apple Safari (أحدث إصدار تمت إتاحته) على Mac OS X 10.10 ‏(Yosemite)‏ أو 10.11 (El Capitan)‏ أو 10.12 (Sierra) أو Apple iPad

للعثور على أحدث إصدار لكل مستعرض ويب، انتقل إلى موقع ويب الشركة المصنعة للبرنامج. 

> [!NOTE]
> -   يجب عليك تثبيت ملحق Chrome التجريبي للسماح بالتقاط صور للقطات الشاشة بواسطة مسجل المهام، وتضمينها في مستندات Microsoft Word الناشئة. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/unified-operations/dev-itpro/user-interface/task-recorder).-->
> -   تم بدء تشغيل محرر سير العمل كتطبيق ClickOnce. تدعم Microsoft Edge و Internet Explorer فقط (على الإصدارات المعتمدة من Microsoft Windows) تطبيقات ClickOnce. يتطلب تطبيق ClickOnce محرر سير العمل نظام تشغيل متوافق 64 بت.
> -   بدء تشغيل مصمم التقرير للتقارير المالية كتطبيق ClickOnce. يتطلب هذا نظام تشغيل متوافق 64 بت. إذا كنت تستخدم Chrome، يجب تثبيت ملحق ClickOnce لتنزيل عميل مصمم التقارير. إذا كنت تستخدم Chrome مع وضع التخفي، تأكد من تمكين الملحق ClickOnce لوضع التخفي أيضًا.
> -   لمعاينة ملفات PDF، ننصح باستخدام مستعرضات مثل Microsoft Edge (آخر إصدار متوفر للجمهور) على نظام التشغيل Windows 10 أو Google Chrome (آخر إصدار متوفر للجمهور) على نظام التشغيل Windows 10 أو Windows 8.1 أو Windows 8 أو Windows 7 أو الكمبيوتر اللوحي Google Nexus 10.


### <a name="supported-web-browsers-for-retail-cloud-pos"></a>مستعرضات الويب المدعومة لـ "نقطة بيع مجموعة النظراء للبيع بالتجزئة"

يمكن تشغيل نقطة بيع مجموعة البيع بالتجزئة‬ في أيٍّ من مستعرضات الويب التالية التي تعمل على أنظمة التشغيل المحددة:

-   Microsoft Edge (أحدث إصدار تمت إتاحته للجمهور) على Windows 10
-   Internet Explorer 11 على Windows 10 أو Windows 8.1 أو Windows 7
-   Chrome (أحدث نسخة متاحة للجمهور) على Windows 10 أو Windows 8.1 أو Windows 7

## <a name="retail-modern-pos-requirements"></a>متطلبات نقطة بيع حديثة
### <a name="supported-operating-systems"></a>أنظمة التشغيل المدعومة

-   نقطة البيع الحديثة للبيع بالتجزئة هي تطبيق 32 بت، ولكن سيتم تشغيله على كل من بنى x86 وx64.
-   نقطة البيع الحديثة للبيع بالتجزئة مدعومة فقط في إصدارات Windows 10 Pro وEnterprise و Enterprise Long Term Servicing Branch.

### <a name="minimum-system-requirements"></a>الحد الأدنى لمتطلبات النظام

-   الحد الأدنى من الدقة المدعومة هو 1280* 1024.
-   يجب أن يلبي جهاز الحاسوب الذي يشغل نقطة البيع الحديثة للبيع بالتجزئة، هذه المتطلبات:
    -   يجب أن يكون، وبحد أدنى، يحتوي على معالج ثنائي الذاكرة يشغل ما لا يقل عن 2 غيغا هرتز.
    -   يجب أن يكون به ذاكرة وصول عشوائي (RAM) 3 غيغابايت بحد أدنى.
    -   يجب أن يحتوي على صلاحية الوصول إلى الإنترنت.

## <a name="retail-hardware-station-requirements"></a>متطلبات Retail Hardware Station.
### <a name="supported-operating-systems"></a>أنظمة التشغيل المدعومة

-   Retail hardware station هي تطبيق 32 بت، ولكن سيتم تشغيله على كل من بنى x86 وx64.
-   يتم اعتماد Retail hardware station على أنظمة التشغيل التالية:
    -   إصدارات Windows 7 Professional و Enterprise و Ultimate 
    
    > [!NOTE]
    > يتم دعم نظام التشغيل Windows 7 فقط عند تثبيت Internet Explorer 11 يدويًا على النظام.

    -   إصدارات Windows 8.1 Update 1 Professional وEnterprise وEmbedded
    -   إصدارات Windows 10 Pro وEnterprise وEnterprise LTSB

### <a name="minimum-system-requirements"></a>الحد الأدنى لمتطلبات النظام

يجب أن يلبي جهاز الكمبيوتر جميع متطلبات النظام لتثبيت واستخدام العناصر التالية:

-   Internet Information Services ‏(IIS)
-   جهاز الطرف الآخر

## <a name="retail-store-scale-unit-requirements"></a>متطلبات وحدة قياس متجر البيع بالتجزئة
### <a name="supported-operating-systems"></a>أنظمة التشغيل المدعومة

-   وحدة قياس متجر البيع بالتجزئة هي تطبيق 32 بت، ولكن سيتم تشغيله على كل من بنى x86 وx64.
-   يتم اعتماد وحدة قياس متجر البيع بالتجزئة على أنظمة التشغيل التالية:
    -   إصدارات Windows 7 Professional و Enterprise و Ultimate
    -   إصدارات Windows 8.1 Update 1 Professional وEnterprise وEmbedded
    -   إصدارات Windows 10 Pro وEnterprise وEnterprise LTSB

### <a name="minimum-system-requirements"></a>الحد الأدنى لمتطلبات النظام

-   4 غيغابايت من ذاكرة الوصول العشوائي
-   سرعة وحدة المعالجة المركزية وقت الذروة قدرتها 1.6 غيغاهرتز لكل معالج (الحد الأدنى ذاكرتان أساسيتان).
-   10 غيغابايت على الأقل من المساحة الحرة (يمكن لقاعدة بيانات القناة أن تتطلب قدر أكبر من المساحة.)

### <a name="recommended-system-requirements"></a>متطلبات النظام الموصى بها

-   6 غيغابايت من ذاكرة الوصول العشوائي
-   2.4 غيغاهرتز لـ i7 (أو ما يعادلها) لسرعة وحدة المعالجة المركزية وقت الذروة للذاكرة الواحدة (يوصي بوجود أربعة ذواكر أساسية.)
-   10 غيغابايت على الأقل من المساحة الحرة (يمكن لقاعدة بيانات القناة أن تتطلب قدر أكبر من المساحة.)

## <a name="connector-requirements"></a>متطلبات الموصل
### <a name="supported-operating-systems"></a>أنظمة التشغيل المدعومة

-   يتضمن موصل Microsoft Dynamics AX مثبتين منفصلين، **Async Server Connector service** و**خدمة Real-time لتطبيق Dynamics AX 2012 R3**.
-   المكونان عبارة عن تطبيقات 32 بت، ولكن يمكن تشغيلها على بنيتي x86 وx64.
-   يتم دعم المكونين في أنظمة التشغيل التالية:
    -   إصدارات Windows 7 Professional و Enterprise و Ultimate
    -   إصدارات Windows 8.1 Update 1 Professional وEnterprise وEmbedded
    -   إصدارات Windows 10 Pro وEnterprise وEnterprise LTSB
    -   Windows Server 2012 R2 وWindows Server 2016

### <a name="minimum-system-requirements"></a>الحد الأدنى لمتطلبات النظام

-   2 غيغابايت من ذاكرة الوصول العشوائي، السعة الموصى بها 4 غيغابايت من ذاكرة الوصول العشوائي
-   سرعة وحدة المعالجة المركزية وقت الذروة قدرتها 1.6 غيغاهرتز لكل معالج (الحد الأدنى ذاكرتان أساسيتان).
-   10 غيغابايت على الأقل من المساحة الحرة (يمكن لقاعدة بيانات القناة أن تتطلب قدر أكبر من المساحة.)

## <a name="requirements-for-development-on-local-vms"></a>متطلبات للتطوير في الأجهزة الظاهرية المحلية
للحصول على معلومات حول متطلبات التطوير على الأجهزة الظاهرية المحلية (الأجهزة الظاهرية)، راجع [تشغيل الأجهزة الظاهرية محليًا](../dev-tools/access-instances.md).

# <a name="system-requirements-for-on-premises-deployments"></a>متطلبات النظام لعمليات النشر المحلي

## <a name="network-requirements"></a>متطلبات الشبكة
باستطاعة Finance and Operations (محلي) العمل على الشبكات التي تستخدم الإصدار 4 من بروتوكول الإنترنت (IPv4) أو الإصدار 6 من بروتوكول الإنترنت (IPv6). خذ بعين الاعتبار بيئة الشبكة عندما تضع خطة للنظام واتبع الإرشادات التالية.

### <a name="network-response-time"></a>وقت استجابة الشبكة
يسرد الجدول التالي الحد الأدنى لمتطلبات الشبكة للاتصال بين مستعرض الويب وخادم كائن التطبيق (AOS)، وللاتصال بين AOS وقاعدة البيانات في نظام محلي.

| القيمة     | مستعرض ويب إلى AOS | AOS إلى قاعدة بيانات                                            |
|-----------|--------------------|------------------------------------------------------------|
| عرض النطاق الترددي | 50 كيلوبايت في الثانية لكل مستخدم   | 100 ميغابايت في الثانية                                                   |
| زمن الوصول   | < 250-300 ملي ثانية       | < 1 ملي ثانية (الشبكة المحلية فقط). يجب أن يتواجد كل من AOS وقاعدة البيانات في موقع مشترك. |

- تم تصميم Finance and Operations (محلي) للشبكات التي لديها زمن وصول من 250-300 ملي ثانية أو أقل. زمن الوصول هذا هو زمن الوصول من عميل المستعرض إلى مركز البيانات الذي يستضيف Finance and Operations.
- تتوقف متطلبات عرض النطاق الترددي لـ Finance and Operations (محلي) على السيناريو الخاص بك. تتطلب وحدات السيناريو النموذجية عرض نطاق ترددي مقداره أكثر من 50 كيلوبايت في الثانية (KBps) بين المستعرض والملقم التمويل والعمليات. ولكن، بالنسبة للسيناريوهات التي لها متطلبات حمولة عالية، مثل مساحات العمل أو السيناريوهات التي تتضمن عمليات تخصيص مكثفة، من المستحسن استخدام عرض نطاق ترددي أعلى وهو يتوقف على الاستخدام.
لا يتم اعتماد عمليات النشر حيث يوجد AOS وقاعدة بيانات SQL Server في مراكز بيانات مختلفة. يجب أن يتواجد كل من AOS وقاعدة بيانات SQL Server في موقع مشترك. بشكل عام، تم تحسين Finance and Operations لتقليل الجولات من المستعرض إلى الخادم والعكس. يعتبر عدد الجولات من عميل مستعرض إلى مركز البيانات إما صفرًا أو جولة واحدة لكل تفاعل من تفاعلات المستخدم، ويتم ضغط الحمولة.

> [!WARNING]
> لا تقم بحساب متطلبات عرض النطاق الترددي من موقع عميل من خلال ضرب عدد المستخدمين في متطلبات الحد الأدنى لعرض النطاق الترددي. يُصعب للغاية حساب الاستخدام المستزامن لموقع ما. نوصي باستخدام محاكاة واقعية في مقابل بيئة Finance and Operations غير منتجة كأفضل مقياس للأداء لحالتك المعينة. 

### <a name="lan-environments"></a>بيئات الشبكة المحلية (LAN)
في بيئات الشبكة المحلية (LAN)، لا حاجة إلى Microsoft Remote Desktop في Microsoft Windows Server للاتصال بتطبيق Finance and Operations. ومع ذلك، قد يكون ضروريًا لعمليات الصيانة على الأجهزة الظاهرية الي تشكل عمليات النشر على الخادم.

### <a name="wan-environments"></a>بيئات الشبكة الواسعة (WAN)
في بيئات الشبكة الواسعة (WAN)، لا حاجة إلى سطح المكتب البعيد في Windows Server للاتصال بتطبيق Finance and Operations.

### <a name="internet-connectivity-requirements"></a>متطلبات اتصال الإنترنت
لا يحتاج Finance and Operations (محلي) إلى اتصال الإنترنت من محطات عمل المستخدم النهائي. ومع ذلك، لن تكون بعض الميزات متوفرة من دون اتصال الإنترنت.

| عميل المستعرض | يعتبر سيناريو الإنترانت من دون اتصال الإنترنت بمثابة نقطة تصميم لخيار النشر المحلي. لن تتوفر بعض الميزات التي تتطلب خدمات سحابية، مثل التعليمات ومكتبات دلائل المهام في LCS. |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| الخادم         | يجب أن يكون كل من AOS أو مستوى Service Fabric قادرًا على التواصل مع LCS. لا يحتاج العميل القائم على المستعرض المحلي إلى الوصول إلى الإنترنت.                                                                                |
| بيانات تتبع الاستخدام      | قد يتم فقدان بيانات تتبع الاستخدام في حال تعرض الاتصال لحالات مقاطعة طويلة. لا تتأثر حالات المقاطعة التي يتعرض لها الاتصال بـ LCS على الأداء الوظيفي للتطبيق المحلي.                                                |
| LCS            | الاتصال بـ LCS مطلوب لعمليات النشر ونشر التعليمات البرمجية ونشر عمليات الصيانة.                                                                                                                                 |
## <a name="telemetry-data-transfer-to-the-cloud"></a>نقل بيانات تتبع الاستخدام إلى السحابة
يتم تخزين معظم بيانات تتبع الاستخدام محليًا ويمكن الوصول إليها باستخدام "عارض الأحداث" في Microsoft Windows. يتم تحويل مجموعة فرعية صغيرة من بيانات تتبع الاستخدام إلى تدفق بيانات تتبع الاستخدام من Microsoft في السحابة لعمليات التشخيص. لا تشكل بيانات العملاء والبيانات القابلة للتعريف بواسطة المستخدم جزءًا من بيانات تتبع الاستخدام المرسلة إلى Microsoft. يتم إرسال أسماء الأجهزة الظاهرية إلى Microsoft للمساعدة في إدارة البيئة وعمليات التشخيص من مدخل LCS.

## <a name="domain-requirements"></a>متطلبات المجال
خذ بعين الاعتبار متطلبات المجال التالية عند تثبيت Finance and Operations (محلي):

- يجب أن تنتمي الأجهزة الظاهرية التي تستضيف Finance and Operations (محلي) إلى مجال Active Directory. يتم تكوين خدمات دليل Active Directory (AD DS) في الوضع الأصلي.
- يجب أن تتوفر لدى الأجهزة الظاهرية التي تقوم بتشغيل مكونات Finance and Operations (on-premises) حق الوصول إلى بعضها البعض وهي مكونة في خدمات مجال Active Directory. 
- يجب تشغيل وحدة التحكم بالمجال على Microsoft Windows Server 2016.

## <a name="hardware-requirements"></a>متطلبات الأجهزة
يصف هذا القسم الأجهزة المطلوبة لتشغيل Finance and Operations (محلي).
استنادًا إلى تكوين النظام وتكوين البيانات والتطبيقات والميزات التي قررت استخدامها، سوف تختلف المتطلبات الفعلية للأجهزة. فيما يلي بعض العوامل التي قد تؤثر على الخيار الخاص بالأجهزة المناسبة لتطبيق Finance and Operations (محلي):

- عدد الحركات بالساعة.
- عدد المستخدمين المتزامنين‬.

## <a name="minimum-infrastructure-requirements"></a>الحد الأدنى لمتطلبات البنية الأساسية
يستخدم Finance and Operations (محلي) Microsoft Azure Service Fabric لاستضافة خدمات كل من AOS والدُفعات وإدارة البيانات وأداة تقارير الإدارة ومنسق البيئة. لا تتم استضافة Microsoft SQL Server Reporting Services (SSRS) في نظام مجموعة Service Fabric.
يجب إعداد SQL Server في إعداد HADRON ذي التوافر العالي الذي يتضمن عقدتين على الأقل لاستخدام الإنتاج.
يظهر الشكل التالي الحد الأدنى الموصى به لعدد العقد في نظام مجموعة Service Fabric.

[![عدد العقد الموصى به لنظام مجموعة service fabric](./media/system-reqs-on-premises-01.png)](./media/system-reqs-on-premises-01.png) 

## <a name="processor-and-ram-requirements"></a>متطلبات المعالج وذاكرة الوصول العشوائي (RAM)
يسرد الجدول التالي عدد المعالجات ومقدار ذاكرة الوصول العشوائي (RAM) المطلوبة لكل من الأدوار المطلوبة لتشغيل خيار النشر هذا. للحصول على مزيد من المعلومات، اقرأ التوصية المتعلقة بالحد الأدنى من المتطلبات لنظام المجموعة المستقل Service Fabric، [تخطيط وإعداد عملية نشر نظام المجموعة المستقل Service Fabric](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

> [!NOTE]
> إذا تم تثبيت برامج Microsoft أخرى على نفس الكمبيوتر، فيجب أن يلتزم النظام أيضًا بمتطلبات الأجهزة لذلك البرنامج. من المستحسن تقييد تطبيقات الخادم الأخرى على نفس الكمبيوتر مثل AOS بغيغابايت واحد من ذاكرة الوصول العشوائي (RAM).

**تغيير الحجم حسب الدور ونوع الطبولوجيا**

| الطبولوجيا‏‎   | الدور (نوع العقدة)              | مراكز المعالج الموصى بها | حجم الذاكرة المستحسن (GB) |
|------------|-------------------------------|-----------------------------|-------------------------|
| الإنتاج | AOS، إدارة البيانات، الدُفعة   | 8                           | 24                      |
|            | أداة تقارير الإدارة           | 4                           | 16                      |
|            | خدمات تقارير SQL Server | 4                           | 16                      |
|            | المنسق                  | 4                           | 16                      |
| وضع الحماية‬    | AOS، إدارة البيانات، الدُفعة   | 4                           | 24                      |
|            | أداة تقارير الإدارة           | 4                           | 16                      |
|            | خدمات تقارير SQL Server | 4                           | 16                      |
|            | المنسق                  | 4                           | 16                      |

**تقديرات تغيير الحجم الأدنى للإنتاج ونشر وضع الحماية**\*

| الطبولوجيا‏‎                                  | الدور                          | عدد المثيلات |
|-------------------------------------------|-------------------------------|---------------------|
| الإنتاج                                | AOS (إدارة البيانات، الدُفعة)  | 3                   |
|                                           | أداة تقارير الإدارة           | 2                   |
|                                           | خدمات تقارير SQL Server | 1                   |
|                                           | المنسق\*\*                | 3                   |
| وضع الحماية‬                                   | AOS، إدارة البيانات، الدُفعة   | 2                   |
|                                           | أداة تقارير الإدارة           | 1                   |
|                                           | خدمات تقارير SQL Server | 1                   |
|                                           | المنسق                  | 3                   |
| *طبولوجيا ملخص الإنتاج ووضع الحماية* |                               | 16                  |

\*يتم التحقق من صحة هذه الأرقام بواسطة عملاء المعاينة وقد يتم ضبطها بحسب الحاجة استنادًا إلى هذه الملاحظات.

\*\*تم تعيين المنسق كنوع عقدة أساسي، وسيتم استخدامه لتشغيل خدمات Service Fabric أيضًا.

**تقديرات SQL Server الخلفي وAD الأولية**

[![تقديرات SQL Server الخلفي وAD الأولية](./media/system-reqs-on-premises-02.PNG)](./media/system-reqs-on-premises-02.PNG) 

\*تتوقف أحجام SQL Server إلى حد بعيد على أحمال العمل. للحصول على مزيد من المعلومات، راجع القسم [ضبط حجم الأجهزة للبيئات المحلية](#Hardware-sizing-for-on-premises-environments).

## <a name="storage"></a>مساحة التخزين

- **AOS** -سوف يستخدم Finance and Operations (محلي) مشاركة Server Message Block (SMB) 3.0 لتخزين البيانات غير المهيكلة. للحصول على مزيد من المعلومات، راجع [مساحات التخزين المباشرة في Windows Server 2016](/windows-server/storage/storage-spaces/storage-spaces-direct-overview).
- **SQL** - الخيارات القابلة للعمل:
    - إعداد محرك الأقراص ذي الحالة الصلبة (SSD) العالي التوافر.
    - شبكة منطقة تخزين (SAN) تم تحسينها لإنتاجية OLTP.
    - مساحة تخزين متصلة بشكل مباشر (DAS) عالية الأداء 
- **عمليات الإدخال/الإخراج في الثانية لكل من SQL Server وإدارة البيانات** - يجب أن تتضمن مساحة التخزين لكل من إدارة البيانات وSQL Server على 2,000 عملية إدخال/إخراج في الثانية على الأقل. تتوقف عمليات الإدخال/الإخراج في الثانية للإنتاج على العديد من العوامل. للحصول على مزيد من المعلومات، راجع القسم "ضبط حجم الأجهزة للبيئات المحلية". 
- **عمليات الإدخال/الإخراج في الثانية للأجهزة الظاهرية** -يجب أن يتضمن كل جهاز ظاهري 100 عملية إدخال/إخراج في الثانية على الأقل 100 للكتابة.

## <a name="virtual-host-requirements"></a>متطلبات الأجهزة المضيفة الظاهرية
عند إعداد الأجهزة المضيفة الظاهرية لبيئة Finance and Operations (محلي)، راجع الإرشادات التالية: [تخطيط وإعداد نظام مجموعة Service Fabric](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) و[وصف نظام مجموعة Service Fabric](/azure/service-fabric/service-fabric-cluster-resource-manager-cluster-description). يجب أن يتضمن كل جهاز مضيف ظاهري العدد الكافي من المراكز للبنية الأساسية التي يجري ضبط حجمها من أجله. تعتبر الإعدادات المتقدمة المتعددة ممكنة، حيث يقيم SQL Server على الجهاز الفعلي ولكن كل شيء آخر تحوّل إلى افتراضي. إذا تحوّل SQL Server إلى افتراضي، فيجب أن يكون النظام الفرعي للقرص عبارة عن SAN سريعة أو شيء مكافئ لها. في جميع الحالات، تأكد من أن الإعداد الأساسي للمضيف ظاهري عالي التوافر ومتكرر. في جميع الحالات، عند استخدام المحاكاة الافتراضية، يجب عدم أخذ لقطات للأجهزة الظاهرية.

## <a name="software-requirements-for-all-server-computers"></a>متطلبات البرامج لكافة أجهزة كمبيوتر الخادم
يجب أن تكون البرامج التالية موجودة على الكمبيوتر قبل تثبيت أي من مكونات Finance and Operations (محلي):

- Microsoft .NET Framework 4.5.1 أو إصدار لاحق
- Service Fabric لمزيد من المعلومات، راجع [تخطيط وإعداد نظام مجموعة Service Fabric](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

## <a name="supported-server-operating-systems"></a>أنظمة تشغيل الخادم المعتمدة
يسرد الجدول التالي أنظمة تشغيل الخادم المعتمدة لمكونات Finance and Operations.

| نظام التشغيل                                     | ملاحظات                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------|
| Microsoft Windows Server 2016 Datacenter أو Standard | تتعلق هذه المتطلبات بقاعدة البيانات ونظام مجموعة Service Fabric الذي يستضيف AOS. |

## <a name="software-requirements-for-database-servers"></a>متطلبات البرامج لخوادم قاعدة البيانات

- يتم دعم إصدارات 64 بت فقط من SQL Server 2016.
- في بيئة إنتاج، من المستحسن أن تقوم بتثبيت آخر تحديث تراكمي (CU) لإصدار SQL Server الذي تستخدمه.
- يدعم Finance and Operations (محلي) ترتيبات Unicode التي لا تتحسس حالة الأحرف وتتحسس علامات التمييز وكانا ولا تتحسس العرض. يجب أن يكون الترتيب مطابقًا لإعدادات Windows المحلية لأجهزة الكمبيوتر التي تقوم بتشغيل مثيلات AOS. إذا كنت تقوم بإعداد عملية تثبيت جديدة، فمن المستحسن أن تحدد ترتيب Windows بدلاً من ترتيب SQL Server. للحصول على مزيد من المعلومات حول كيفية تحديد ترتيب لقاعدة بيانات SQL Server، راجع [وثائق SQL Server](/sql/sql-server/sql-server-technical-documentation).
يسرد الجدول التالي إصدارات SQL Server المعتمدة لقواعد بيانات Finance and Operations. للحصول على مزيد من المعلومات، راجع الحد الأدنى من متطلبات الأجهزة في [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-2016).

| الطلب                                                      | ملاحظات                                                                                                                     |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Microsoft SQL Server 2016 Standard Edition أو Enterprise Edition | بالنسبة إلى متطلبات الأجهزة لـ SQL Server 2016، راجع [متطلبات الأجهزة والبرامج لتثبيت SQL Server 2016](/sql/sql-server/install/hardware-and-software-requirements-for-installing-sql-server). |

## <a name="software-requirements-for-client-computers"></a>متطلبات البرامج لأجهزة كمبيوتر العميل
يمكن تشغيل تطبيق الويب Finance and Operations على أي جهاز يتضمن مستعرض ويب يتوافق مع HTML5.0. تتضمن مجموعات الجهاز/المستعرض المعينة التي أقرتها Microsoft:

- Microsoft Edge (أحدث إصدار تمت إتاحته للجمهور) على Windows 10
- Internet Explorer 11 على Windows 10 أو Windows 8.1 أو Windows 7
- Google Chrome (أحدث إصدار تمت إتاحته) على Windows 10 أو Windows 8.1 أو Windows 8 أو Windows 7 أو Google Nexus 10 tablet
- Apple Safari (أحدث إصدار تمت إتاحته) على Mac OS X 10.10 ‏(Yosemite)‏ أو 10.11 (El Capitan)‏ أو 10.12 (Sierra) أو Apple iPad

## <a name="software-requirements-for-active-directory-federation-services"></a>متطلبات البرامج لخدمات الأمان المشترك لـ Active Directory 
خدمات الأمان المشترك لـ Active directory (AD FS) في نظام التشغيل Windows Server 2016

يجب أن تكون وحدة التحكم بالمجال Windows Server 2012 R2 أو إصدار أحدث مع مستوى وظائفي للمجال من 2012 R2 أو أكبر

لمزيد من المعلومات حول المستويات الوظيفية للمجال، راجع: 
- [ما هي المستويات الوظيفية لـ Active Directory](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
- [التعرف على المستويات الوظيفية لخدمات مجال Active Directory](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)
 
## <a name="hardware-and-software-requirements-for-retail-components"></a>متطلبات الأجهزة والبرامج لمكونات البيع بالتجزئة
لا يتضمن Finance and Operations (محلي) مكونات البيع بالتجزئة في الوقت الحالي.

<a name="see-also"></a>راجع أيضًا
--------

[الحصول على نسخة تقييم لـ Dynamics 365 for Finance and Operations, Enterprise edition](/dynamics365/unified-operations/dev-itpro/dev-tools/get-evaluation-copy)

