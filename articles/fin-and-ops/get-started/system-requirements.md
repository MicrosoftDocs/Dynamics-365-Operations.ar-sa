---
title: "متطلبات النظام لعمليات النشر في السحابة"
description: "يسرد هذا الموضوع متطلبات النظام للإصدار الحالي من Microsoft Dynamics 365 for Finance and Operations, Enterprise edition لعمليات النشر في السحابة."
author: sericks007
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 83637b4b2ccc01950e68569b3b8bee1a7cd69855
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="system-requirements-for-cloud-deployments"></a>متطلبات النظام لعمليات النشر في السحابة

[!include[banner](../includes/banner.md)]

يسرد هذا الموضوع متطلبات النظام للإصدار الحالي من Microsoft Dynamics 365 for Finance and Operations, Enterprise edition لعمليات النشر في السحابة. قبل تثبيت Finance and Operations، عندما تكون هذه الخطوة ملائمة، تحقق من أن النظام الذي تستخدمه يستوفي الحد الأدنى من متطلبات الشبكة والأجهزة والبرامج أو يتجاوزه.

## <a name="supported-web-browsers"></a>مستعرضات الويب المدعومة
يمكن تشغيل تطبيق ويب في أيٍّ من مستعرضات الويب التالية التي تعمل على أنظمة التشغيل المحددة:

-   Microsoft Edge (أحدث إصدار تمت إتاحته للجمهور) على Windows 10
-   Internet Explorer 11 على Windows 10 أو Windows 8.1 أو Windows 7
-   Google Chrome (أحدث إصدار تمت إتاحته) على Windows 10 أو Windows 8.1 أو Windows 8 أو Windows 7 أو Google Nexus 10 tablet
-   Apple Safari (أحدث إصدار تمت إتاحته) على Mac OS X 10.10 ‏(Yosemite)‏ أو 10.11 (El Capitan)‏ أو 10.12 (Sierra) أو Apple iPad

للعثور على أحدث إصدار لكل مستعرض ويب، انتقل إلى موقع ويب الشركة المصنعة للبرنامج. 

> [!NOTE]
> -   يجب عليك تثبيت ملحق Chrome التجريبي لتمكين مسجل المهام من أخذ صور للقطات الشاشة وتضمينها في مستندات Microsoft Word الناشئة. <!---For instructions about how to install the extension, see [Screenshot Extension setup](../../dev-itpro/user-interface/task-recorder).-->
> -   تم بدء تشغيل محرر سير العمل كتطبيق ClickOnce. تدعم Microsoft Edge و Internet Explorer فقط (على الإصدارات المعتمدة من Microsoft Windows) تطبيقات ClickOnce. يتطلب تطبيق ClickOnce محرر سير العمل نظام تشغيل متوافق 64 بت.
> -   بدء تشغيل مصمم التقرير للتقارير المالية كتطبيق ClickOnce. يحتاج هذا إلى نظام تشغيل متوافق 64 بت. إذا كنت تستخدم Chrome، فيجب تثبيت ملحق ClickOnce لتنزيل عميل مصمم التقارير. إذا كنت تستخدم Chrome مع وضع التخفي، فتأكد من تمكين الملحق ClickOnce لوضع التخفي أيضًا.
> -   لمعاينة ملفات PDF، ننصح باستخدام مستعرضات مثل Microsoft Edge (آخر إصدار متوفر للجمهور) على نظام التشغيل Windows 10 أو Google Chrome (آخر إصدار متوفر للجمهور) على نظام التشغيل Windows 10 أو Windows 8.1 أو Windows 8 أو Windows 7 أو الكمبيوتر اللوحي Google Nexus 10.

### <a name="supported-web-browsers-for-retail-cloud-pos"></a>مستعرضات الويب المدعومة لـ "نقطة بيع مجموعة النظراء للبيع بالتجزئة"

يمكن تشغيل نقطة بيع مجموعة البيع بالتجزئة‬ في أيٍّ من مستعرضات الويب التالية التي تعمل على أنظمة التشغيل المحددة:

-   Microsoft Edge (أحدث إصدار تمت إتاحته للجمهور) على Windows 10
-   Internet Explorer 11 على Windows 10 أو Windows 8.1 أو Windows 7
-   Chrome (أحدث نسخة متاحة للجمهور) على Windows 10 أو Windows 8.1 أو Windows 7

## <a name="network-requirements"></a>متطلبات الشبكة
-   تم تصميم Finance and Operations للشبكات التي لديها زمن وصول من 250-300 ملي ثانية أو أقل. زمن الوصول هذا هو زمن الوصول من عميل مستعرض إلى مركز بيانات Microsoft Azure الذي يستضيف Finance and Operations. نوصي باختبار زمن وصول الشبكة على <http://www.azurespeed.com>.
-   تعتمد متطلبات عرض النطاق الترددي لـ Finance and Operations على السيناريو الخاص بك. تتطلب السيناريوهات الأكثر شيوعاً عرض نطاق ترددي لأكثر من 50 كيلو بايت في الثانية (KBps). ولكننا نوصي باستخدام عرض نطاق ترددي أعلى، بالنسبة للسيناريوهات التي لها متطلبات حمولة عالية، مثل السيناريوهات التي تشتمل على مساحات عمل أو تخصيص مكثف.

وبوجه عام، تم تحسين Finance and Operations للإنترنت. يعتبر عدد الجولات من عميل مستعرض إلى مركز بيانات Azure صغير جدًا، ويتم ضغط حمولة كاملة. 

> [!WARNING]
> لا تقم بحساب متطلبات عرض النطاق الترددي من موقع عميل من خلال ضرب عدد المستخدمين في متطلبات الحد الأدنى لعرض النطاق الترددي. يُصعب للغاية حساب الاستخدام المستزامن لموقع ما. بالنسبة للعملاء المهتمين بشأن متطلبات النطاق الترددي، يجب عليهم استخدام إصدار المعاينة من Finance and Operations.

## <a name="net-framework-requirements"></a>متطلبات .NET Framework
يتطلب Finance and Operations الإصدار 4.6.2 من Microsoft .NET Framework لجميع تطبيقات ClickOnce، مثل وكيل توجيه المستند. للحصول على إرشادات التثبيت، راجع [تثبيت.NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-microsoft-office-applications"></a>تطبيقات Microsoft Office المعتمدة
يتم اعتماد تطبيقات Microsoft Office التالية أثناء عمليات نشر Finance and Operations في السحابة وفي الموقع المحلي:

-   لتثبيت الوظائف الإضافية لـ Microsoft Excel و Word، يجب أن يكون لديك Microsoft Office 2016 لـ Windows أو Mac مثبتًا. للحصول على مزيد من المعلومات حول متطلبات الإصدار، راجع [استكشاف وإصلاح مشاكل تكامل Office](../../dev-itpro/office-integration/office-integration-troubleshooting.md).
-   لعرض المستندات التي تم إنشاؤها بواسطة التصدير إلى وظائف Word أو التصدير إلى Excel، يجب عليك تثبيت Microsoft Office 2007 أو الإصدار الأحدث.

## <a name="retail-modern-pos-requirements"></a>متطلبات نقطة بيع حديثة

> [!NOTE]
> إذا كانت نقطة البيع الحديثة للبيع بالتجزئة تستخدم قاعدة بيانات دون اتصال، فيجب أن يفي الكمبيوتر كافة متطلبات النظام في Microsoft SQL Server. سوف تعمل قاعدة البيانات دون اتصال لنقطة البيع الحديثة للبيع بالتجزئة على Microsoft SQL Server 2012 مع Service Pack 3 أو إصدار لاحق، وMicrosoft SQL Server 2014 مع Service Pack 2 أو إصدار لاحق، وMicrosoft SQL Server 2016. نحن ننصحك بأن تستخدم دائمًا أحدث إصدار متوفر، وأن تقوم بتثبيت كافة حزم الخدمة الأحدث.

### <a name="supported-operating-systems"></a>أنظمة التشغيل المدعومة

-   نقطة البيع الحديثة للبيع بالتجزئة هي تطبيق 32 بت، ولكن سيتم تشغيله على كل من بنى x86 وx64.
-   نقطة البيع الحديثة للبيع بالتجزئة مدعومة فقط في إصدارات Windows 10 Pro وEnterprise و Enterprise Long Term Servicing Branch.

### <a name="minimum-system-requirements"></a>الحد الأدنى لمتطلبات النظام

-   الحد الأدنى من الدقة المدعومة هو 1280* 1024.
-   يجب أن يلبي جهاز الحاسوب الذي يشغل نقطة البيع الحديثة للبيع بالتجزئة، هذه المتطلبات:

    -   يجب أن يكون، وبحد أدنى، يحتوي على معالج ثنائي الذاكرة يشغل ما لا يقل عن 2 غيغا هرتز.
    -   يجب أن يكون به ذاكرة وصول عشوائي (RAM) من 3 غيغابايت بحد أدنى.
    -   يجب أن يتوفر لديه الوصول إلى الإنترنت.

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

-   يتضمن موصل Microsoft Dynamics AX مثبتين منفصلين، أحدهما لخدمة Async Server Connector service والآخر لخدمة Real-time لتطبيق Dynamics AX 2012 R3.
-   المكونان عبارة عن تطبيقات 32 بت، ولكن يمكن تشغيلها على بنيتي x86 وx64.
-   يتم دعم المكونين في أنظمة التشغيل التالية:

    -   إصدارات Windows 7 Professional و Enterprise و Ultimate
    -   إصدارات Windows 8.1 Update 1 Professional وEnterprise وEmbedded
    -   إصدارات Windows 10 Pro وEnterprise وEnterprise LTSB
    -   Microsoft Windows Server 2012 R2 وMicrosoft Windows Server 2016

### <a name="minimum-system-requirements"></a>الحد الأدنى لمتطلبات النظام
-   2 غيغابايت من ذاكرة الوصول العشوائي (RAM) (السعة الموصى بها 4 غيغابايت من ذاكرة الوصول العشوائي.)
-   سرعة وحدة المعالجة المركزية وقت الذروة قدرتها 1.6 غيغاهرتز لكل معالج (الحد الأدنى ذاكرتان أساسيتان).
-   10 غيغابايت على الأقل من المساحة الحرة (يمكن لقاعدة بيانات القناة أن تتطلب قدر أكبر من المساحة.)

## <a name="requirements-for-development-on-local-vms"></a>متطلبات للتطوير في الأجهزة الظاهرية المحلية
للحصول على معلومات حول متطلبات التطوير على الأجهزة الظاهرية المحلية (الأجهزة الظاهرية)، راجع [تشغيل الأجهزة الظاهرية محليًا](../../dev-itpro/dev-tools/access-instances.md).


## <a name="see-also"></a>راجع أيضًا

[الحصول على نسخة تقييم لـ Dynamics 365 for Finance and Operations, Enterprise edition](../../dev-itpro/dev-tools/get-evaluation-copy.md)

