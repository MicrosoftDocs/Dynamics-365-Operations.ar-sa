---
title: متطلبات نظام Talent
description: يسرد هذا الموضوع متطلبات Dynamics 365 Talent.
author: andreabichsel
manager: AnnBe
ms.date: 10/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 509827d5736887f56e7754a0760af7dea76277f7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460194"
---
# <a name="talent-system-requirements"></a>متطلبات نظام Talent

[!include [banner](includes/banner.md)]

يصف هذا الموضوع متطلبات Microsoft Dynamics 365 Talent، بما في ذلك Attract وOnboard. كما يوضح البلدان والمناطق التي يتوفر فيها Talent، بالإضافة إلى معلومات حول لغات وترجمة بيانات Talent. علاوةً على ذلك، يوفر هذا الموضوع سياسة تحديث Talent.

## <a name="supported-web-browsers"></a>مستعرضات الويب المدعومة

يمكن تشغيل Microsoft Dynamics 365 Talent في أيٍّ من مستعرضات الويب التالية التي تعمل على أنظمة التشغيل المحددة: 

*   Microsoft Edge (أحدث إصدار تمت إتاحته للجمهور) على Windows 10
*   Internet Explorer 11 على Windows 10 أو Windows 8.1 أو Windows 7
*   Google Chrome (أحدث إصدار تمت إتاحته للجمهور)
*   Apple Safari (أحدث إصدار تمت إتاحته للجمهور)

للعثور على أحدث إصدار لكل مستعرض ويب، انتقل إلى موقع ويب الشركة المصنعة للبرنامج. 

> [!NOTE]
> * لالتقاط الصور التي تم إنشاؤها من مسجل المهام، وتضمينها في مستندات Microsoft Word، يجب عليك تثبيت ملحق Chrome. 
> * تم بدء تشغيل محرر سير العمل كتطبيق ClickOnce. يدعم كل من Microsoft Edge وInternet Explorer (على إصدار معتمد من Microsoft Windows) فقط تطبيقات ClickOnce. يتطلب تطبيق ClickOnce محرر سير العمل نظام تشغيل متوافق 64 بت.
> * لمعاينة ملفات PDF، ننصح باستخدام المستعرضات الحديثة مثل Microsoft Edge (آخر إصدار متوفر للجمهور) على نظام التشغيل Windows 10 أو Google Chrome (آخر إصدار متوفر للجمهور) على نظام التشغيل Windows 10 أو Windows 8.1 أو Windows 8 أو Windows 7 أو الكمبيوتر اللوحي Google Nexus 10.
>   متطلبات الشبكة
> * تم تصميم Dynamics 365 Talent للشبكات مع زمن وصول من 250-300 مللي ثانية أو أقل. زمن الوصول هذا هو زمن الوصول من عميل المستعرض إلى مركز بيانات Microsoft Azure الذي يستضيف Talent. نوصي باختبار زمن وصول الشبكة على [www.azurespeed.com](https://www.azurespeed.com "اختبار زمن انتقال Azure").
> * تعتمد متطلبات عرض النطاق الترددي لتطبيق Talent على السيناريو. تتطلب السيناريوهات الأكثر شيوعاً عرض نطاق ترددي لأكثر من 50 كيلو بايت في الثانية (KBps).
> 
> [!WARNING]
> لا تقم بحساب متطلبات النطاق الترددي من موقع عميل من خلال ضرب عدد المستخدمين في متطلبات الحد الأدنى للنطاق الترددي. يُصعب للغاية حساب الاستخدام المستزامن لموقع ما. بالنسبة إلى العملاء المهتمين بمتطلبات النطاق الترددي، يمكنهم استخدام إصدارًا تجريبيًا من Talent.

## <a name="supported-microsoft-office-applications"></a>تطبيقات Microsoft Office المدعومة

* لتثبيت الوظائف الإضافية لكل من Microsoft Excel وWord، يجب أن يكون Microsoft Office 2016 for Windows أو Mac مثبتًا على جهازك. للحصول على مزيد من التفاصيل حول متطلبات الإصدار، راجع [استكشاف وإصلاح مشاكل تكامل Office](../dev-itpro/office-integration/office-integration-troubleshooting.md "استكشاف أخطاء تكامل Office وإصلاحها").
* لعرض المستندات التي تم إنشاؤها بواسطة وظيفة التصدير إلى Word أو التصدير إلى Excel، يجب عليك تثبيت Microsoft Office 2007 أو إصدار لاحق.

## <a name="regional-availability-languages-and-localization"></a>التوافر الإقليمي واللغات والترجمة

يمكنك تنزيل ملف PDF للبلدان والمناطق واللغات التي تدعم Talent في [التوافر الدولي لتطبيق Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability). 

> [!NOTE]
> وعلى الرغم من ترجمة واجهة المستخدم إلى لغات أخرى، يتم تخزين كافة بيانات المستخدم باللغة التي تم إدخالها بها. يمكنك إنشاء رسائل البريد الكتروني والقوالب بلغات أخرىـ ولكن بعض البيانات مثل معلومات الجدولة لا تتوفر حاليًا إلا باللغة الإنجليزية.

إذا كنت مطور برامج تهتم بإنشاء تخصيصات خاصة ببلد أو منطقة، أو في إنشاء حل لبلد أو منطقة لا تدعمها حاليًا Microsoft، فراجع [العولمة](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).

