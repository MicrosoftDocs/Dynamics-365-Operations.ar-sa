---
title: "متطلبات النظام"
description: "يسرد هذا الموضوع متطلبات النظام للإصدار الحالي من Microsoft Dynamics 365 للعمليات."
author: sericks007
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 9220c093d3f6d6700127c93651db4083be300311
ms.lasthandoff: 03/31/2017


---

# <a name="system-requirements"></a>متطلبات النظام

يسرد هذا الموضوع متطلبات النظام للإصدار الحالي من Microsoft Dynamics 365 للعمليات.

<a name="supported-web-browsers"></a>مستعرضات الويب المدعومة
----------------------

تشغيل Microsoft Dynamics 365 لعمليات تطبيق ويب في أي من مستعرضات ويب التالية التي تعمل على أنظمة التشغيل المحدد:

-   حافة Microsoft (أحدث نسخة متاحة للجمهور) على Windows 10
-   Internet Explorer 11 على Windows 10 أو Windows 8.1 أو Windows 7
-   جوجل كروم (أحدث نسخة متاحة للجمهور) على قرص Windows 10 أو Windows 8.1 ويندوز 8 Windows 7 أو 10 العلاقة جوجل
-   Apple Safari (أحدث نسخة متاحة للجمهور) على Mac OS X (يوسمايت) 10، 10، 10، 11 (كابيتان) أو 10، 12 (سيراليون) أو أي باد

للعثور على أحدث إصدار لكل مستعرض ويب، انتقل إلى موقع ويب الشركة المصنعة للبرنامج. **ملاحظات:**

-   لالتقاط الصور التي تم إنشاؤها من "مسجل المهام" وتضمينها في مستندات Microsoft Word، يجب أن يكون ملحق كروم مثبت. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/operations/dev-itpro/user-interface/task-recorder).-->
-   بدء تشغيل محرر سير العمل كتطبيق ClickOnce. حافة Microsoft وبرنامج Internet Explorer (على إصدار معتمد من Microsoft Windows) تدعم تطبيقات ClickOnce. يتطلب التطبيق ClickOnce محرر سير نظام تشغيل 64 بت متوافق.
-   بدء تشغيل "مصمم التقرير" للإبلاغ المالي كتطبيق ClickOnce. أنه يتطلب نظام تشغيل 64 بت متوافق. إذا كنت تستخدم الكروم، يجب تثبيت ملحق ClickOnce من أجل تحميل العميل مصمم التقرير. إذا كنت تستخدم الكروم بوضع التخفي، تأكد من أن الملحق ClickOnce ممكن أيضا لوضع التخفي.

### <a name="supported-web-browsers-for-retail-cloud-pos"></a>مستعرضات الويب المدعومة لـ "نقطة بيع مجموعة النظراء للبيع بالتجزئة"

تشغيل "نقطة سحابة" البيع بالتجزئة لديناميات 365 للعمليات في أي من مستعرضات ويب التالية التي تعمل على أنظمة التشغيل المحدد:

-   حافة Microsoft (أحدث نسخة متاحة للجمهور) على Windows 10
-   Internet Explorer 11 على Windows 10 أو Windows 8.1 أو Windows 7
-   كروم (أحدث نسخة متاحة للجمهور) على Windows 10 أو Windows 8.1 ويندوز 7

## <a name="network-requirements"></a>متطلبات الشبكة
-   صمم للشبكات dynamics 365 للعمليات مع زمن أقل من 150 مللي ثانية (ms). هذا هو زمن الوصول من عميل مستعرض إلى مركز البيانات Microsoft Azure الذي يستضيف 365 ديناميات عمليات. نوصي باختبار استتار الشبكة في <http://www.azurespeed.com>.
-   تعتمد متطلبات عرض النطاق الترددي لديناميات 365 للعمليات على السيناريو الخاص بك. تتطلب السيناريوهات الأكثر شيوعاً عرض النطاق ترددي لأكثر من 50 كيلو بايت في الثانية (KBps). عرض نطاق ترددي من المستحسن، للحالات التي لديها متطلبات الحمولة العالية، مثل وحدات السيناريو التي تتضمن التخصيص واسعة النطاق، أو مساحات العمل.

بشكل عام، يتم تحسين 365 ديناميات عمليات للإنترنت. عدد الجولات من عميل مستعرض إلى مركز البيانات Azure صغيرة جداً، ويتم ضغط حمولة كاملة. **تحذير:** عدم حساب متطلبات عرض النطاق الترددي من موقع عميل بضرب عدد المستخدمين بمتطلبات الحد الأدنى من عرض النطاق الترددي. من الصعب حساب الاستخدام المتزامن لموقع ما. للعملاء المهتمين بمتطلبات عرض النطاق الترددي، استخدام صيغة معاينة لديناميات 365 للعمليات.

## <a name="net-framework-requirements"></a>متطلبات برنامج.NET framework
يتطلب dynamics 365 لعمليات الإصدار 4.6.2 من برنامج.NET Framework لكافة انقر فوق-مرة التطبيقات، مثل عامل وثيقة التوجيه. للحصول على إرشادات التثبيت، راجع [تثبيت.NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-microsoft-office-applications"></a>تطبيقات Microsoft Office المعتمدة
-   لتشغيل Microsoft Excel و Word الإضافية، يجب أن يكون لديك Microsoft Office 2016 ل Windows أو Mac مثبتة. للحصول على مزيد من التفاصيل حول متطلبات الإصدار، راجع [استكشاف تكامل Office](/dynamics365/operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   لعرض المستندات التي تم إنشاؤها بواسطة التصدير إلى وظائف Word أو التصدير إلى Excel، يجب أن يكون لديك Microsoft Office 2007 أو الإصدار الأحدث مثبتاً.

## <a name="retail-modern-pos-requirements"></a>متطلبات POS الحديثة البيع بالتجزئة
### <a name="supported-operating-systems"></a>أنظمة التشغيل المدعومة

-   نقطة البيع بالتجزئة الحديثة تطبيق 32 بت، ولكن سيتم تشغيله على أبنية كل من x86 و x64.
-   نقطة البيع بالتجزئة الحديثة معتمد فقط في إصدارات Windows 10 Pro المؤسسة والمؤسسة طويلة الأجل معالجة الفرع (لتسب).

### <a name="minimum-system-requirements"></a>متطلبات النظام الحد الأدنى

-   الحد الأدنى من القرار المعتمدة هي 1280 × 1024.
-   يجب أن يطابق الكمبيوتر يشغل "نقطة البيع بالتجزئة الحديثة" على هذه المتطلبات:
    -   يجب، كحد أدنى، معالج الثنائي الذي يتم تشغيله في أقل من 2 غيغا هرتز (GHz).
    -   يجب، كحد أدنى، 3 غيغابايت (GB) من ذاكرة الوصول العشوائي.
    -   يجب أن يكون لديك الوصول إلى إنترنت.

## <a name="retail-hardware-station-requirements"></a>متطلبات محطة الأجهزة البيع بالتجزئة
### <a name="supported-operating-systems"></a>أنظمة التشغيل المدعومة

-   محطة أجهزة البيع بالتجزئة تطبيق 32 بت، ولكن فستعمل على أبنية كلا x86 و x64.
-   يتم اعتماد محطة أجهزة البيع بالتجزئة على أنظمة التشغيل التالية:
    -   إصدارات ويندوز 7 الفنية والمؤسسات وفي نهاية المطاف **ملاحظة:** ويندوز 7 معتمد فقط إذا تم تثبيت Internet Explorer 11 يدوياً على النظام.
    -   إصدارات Windows Professional 1 تحديث 8.1 والمؤسسه المضمنة
    -   إصدارات Windows 10 Pro المؤسسة ومؤسسة لتسب

### <a name="minimum-system-requirements"></a>متطلبات النظام الحد الأدنى

الكمبيوتر يجب أن تفي بجميع متطلبات النظام لتثبيت واستخدام العناصر التالية:

-   Internet Information Services ‏(IIS)
-   أجهزة خارجية

## <a name="retail-store-scale-unit-requirements"></a>متطلبات "وحدة المقياس مخزن" البيع بالتجزئة
### <a name="supported-operating-systems"></a>أنظمة التشغيل المدعومة

-   متجر وحدة المقياس تطبيق 32 بت، ولكن فستعمل على أبنية كل من x86 و x64.
-   يتم اعتماد وحدة المقياس متجر على أنظمة التشغيل التالية:
    -   إصدارات ويندوز 7 الفنية والمؤسسات وفي نهاية المطاف
    -   إصدارات Windows Professional 1 تحديث 8.1 والمؤسسه المضمنة
    -   إصدارات Windows 10 Pro المؤسسة ومؤسسة لتسب

### <a name="minimum-system-requirements"></a>متطلبات النظام الحد الأدنى

-   4 غيغابايت من ذاكرة الوصول العشوائي
-   سرعة وحدة المعالجة المركزية ذروة 1.6 GHz كل معالج (مركزين على الحد الأدنى).
-   10 غيغابايت على الأقل من المساحة الحرة (قاعدة قناة يمكن أن تتطلب قدرا كبيرا من مساحة).

### <a name="recommended-system-requirements"></a>متطلبات النظام الموصى بها

-   6 غيغابايت من ذاكرة الوصول العشوائي
-   2.4 سرعة غيغا هرتز i7 (أو ما يعادلها) الذروة وحدة المعالجة المركزية للمركز (المراكز الأربعة مستحسن.)
-   10 غيغابايت على الأقل من المساحة الحرة (قاعدة قناة يمكن أن تتطلب قدرا كبيرا من مساحة).

## <a name="requirements-for-development-on-local-vms"></a>متطلبات للتطوير في نظام رصد السفن المحلية
للحصول على معلومات حول متطلبات التنمية على الأجهزة الظاهرية المحلي (نظام رصد السفن)، انظر [VM التشغيل المحلي](/dynamics365/operations/dev-itpro/dev-tools/access-instances#vm-that-is-running-in-premises).

<a name="see-also"></a>راجع أيضًا
--------

[الحصول على نسخة تقييم من 365 ديناميات العمليات](/dynamics365/operations/dev-itpro/dev-tools/get-evaluation-copy)


