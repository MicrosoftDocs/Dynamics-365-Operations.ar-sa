---
title: متطلبات النظام
description: توضح هذه المقالة متطلبات Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 52ef0176926fd6c5c5d2bc852080dde5273d05d0f2edd20e091d97c71e503dce
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6761082"
---
# <a name="system-requirements"></a>متطلبات النظام

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

توضح هذه المقالة متطلبات Microsoft Dynamics 365 Human Resources. كما يوضح البلدان والمناطق التي يتوفر فيها Human Resources، بالإضافة إلى معلومات حول لغات وترجمة بيانات Human Resources.

## <a name="supported-web-browsers"></a>مستعرضات الويب المدعومة

يمكن تشغيل Human Resources في أيٍّ من مستعرضات الويب التالية التي تعمل على أنظمة التشغيل المحددة: 

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
> * تم تصميم لـ Human Resourcesلشبكات مع زمن وصول من 250-300 مللي ثانية أو أقل. يمثل هذا زمن الوصول من عميل المستعرض إلى مركز بيانات Microsoft Azure الذي يستضيف Human Resources. نوصي باختبار زمن وصول الشبكة على [www.azurespeed.com](https://www.azurespeed.com "اختبار زمن انتقال Azure").
> * تعتمد متطلبات عرض النطاق الترددي لتطبيق Human Resources على السيناريو الخاص بك. تتطلب السيناريوهات الأكثر شيوعاً عرض نطاق ترددي لأكثر من 50 كيلو بايت في الثانية (KBps).
> 
> [!WARNING]
> لا تقم بحساب متطلبات النطاق الترددي من موقع عميل من خلال ضرب عدد المستخدمين في متطلبات الحد الأدنى للنطاق الترددي. يُصعب للغاية حساب الاستخدام المستزامن لموقع ما. بالنسبة إلى العملاء المهتمين بمتطلبات النطاق الترددي، يمكنهم استخدام إصدارًا تجريبيًا من Human Resources.

## <a name="supported-microsoft-office-applications"></a>تطبيقات Microsoft Office المدعومة

* لتثبيت الوظائف الإضافية لكل من Microsoft Excel وWord، يجب أن يكون Microsoft Office 2016 for Windows أو Mac مثبتًا على جهازك. للحصول على مزيد من التفاصيل حول متطلبات الإصدار، راجع [استكشاف وإصلاح مشاكل تكامل Office](../fin-ops-core/dev-itpro/office-integration/office-integration-troubleshooting.md "استكشاف أخطاء تكامل Office وإصلاحها").
* لعرض المستندات التي تم إنشاؤها بواسطة وظيفة التصدير إلى Word أو التصدير إلى Excel، يجب عليك تثبيت Microsoft Office 2007 أو إصدار لاحق.

## <a name="regional-availability-languages-and-localization"></a>التوافر الإقليمي واللغات والترجمة

يمكنك تنزيل ملف PDF للبلدان والمناطق واللغات التي تدعم Human Resources في [التوافر الدولي لتطبيق Microsoft Dynamics 365](/dynamics365/get-started/availability). 

> [!NOTE]
> وعلى الرغم من ترجمة واجهة المستخدم إلى لغات أخرى، يتم تخزين كافة بيانات المستخدم باللغة التي تم إدخالها بها. يمكنك إنشاء رسائل البريد الكتروني والقوالب بلغات أخرىـ ولكن بعض البيانات مثل معلومات الجدولة لا تتوفر حاليًا إلا باللغة الإنجليزية.

إذا كنت مطور برامج تهتم بإنشاء تخصيصات خاصة ببلد أو منطقة، أو في إنشاء حل لبلد أو منطقة لا تدعمها حاليًا Microsoft، فراجع [العولمة](/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).


[!INCLUDE[footer-include](../includes/footer-banner.md)]