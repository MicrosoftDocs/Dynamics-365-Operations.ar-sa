---
title: "متطلبات النظام وسياسة التحديث في Dynamics 365 for Talent"
description: "يسرد هذا الموضوع متطلبات Dynamics 365 for Talent. وقد تم أيضًا توضيح سياسة التحديث."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: Talent, update policy, requirements, system requirements
audience: Application User, IT Pro
ms.reviewer: rschloma
ms.search.scope: AX 7.2.0, Operations, Core
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: fc8102d945faf9ad533f57ec1a45b0e0dc344963
ms.openlocfilehash: c5942ecb80047628c863deb878c0959727ab57bb
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="microsoft-dynamics-365-for-talent-system-requirements-and-update-policy"></a>متطلبات النظام وسياسة التحديث في Microsoft Dynamics 365 for Talent

[!include[banner](includes/banner.md)]


يسرد هذا الموضوع متطلبات Microsoft Dynamics 365 for Talent. وقد تم أيضًا توضيح سياسة التحديث.

## <a name="supported-web-browsers"></a>مستعرضات الويب المدعومة

يمكن تشغيل تطبيق ويب Microsoft Dynamics 365 for Talent في أيٍّ من مستعرضات الويب التالية التي تعمل على أنظمة التشغيل المحددة: 

*   Microsoft Edge (أحدث إصدار تمت إتاحته للجمهور) على Windows 10
*   Internet Explorer 11 على Windows 10 أو Windows 8.1 أو Windows 7
*   Google Chrome (أحدث إصدار تمت إتاحته) على Windows 10 أو Windows 8.1 أو Windows 8 أو Windows 7 أو Google Nexus 10 tablet
*   Apple Safari (أحدث إصدار تمت إتاحته) على Mac OS X 10.10 ‏(Yosemite)‏ أو 10.11 (El Capitan)‏ أو 10.12 (Sierra) أو Apple iPad

للعثور على أحدث إصدار لكل مستعرض ويب، انتقل إلى موقع ويب الشركة المصنعة للبرنامج. 

> [!NOTE]
> * لالتقاط الصور التي إنشاؤها من مسجل المهام، وتضمينها في مستندات Microsoft Word، يجب عليك تثبيت ملحق Chrome. 
> * تم بدء تشغيل محرر سير العمل كتطبيق ClickOnce. تدعم Microsoft Edge و Internet Explorer فقط (على الإصدارات المعتمدة من Microsoft Windows) تطبيقات ClickOnce. يتطلب تطبيق ClickOnce محرر سير العمل نظام تشغيل متوافق 64 بت.
> * لمعاينة ملفات PDF، ننصح باستخدام المستعرضات الحديثة مثل Microsoft Edge (آخر إصدار متوفر للجمهور) على نظام التشغيل Windows 10 أو Google Chrome (آخر إصدار متوفر للجمهور) على نظام التشغيل Windows 10 أو Windows 8.1 أو Windows 8 أو Windows 7 أو الكمبيوتر اللوحي Google Nexus 10.
متطلبات الشبكة
> * تم تصميم Dynamics 365 for Talent للشبكات ذات زمن وصول من 250-300 مللي ثانية أو أقل. هذا هو زمن الوصول من عميل مستعرض إلى مركز بيانات Microsoft Azure الذي يستضيف Dynamics 365 for Talent. نوصي بأن تقوم باختبار زمن وصول الشبكة في [www.azurespeed.com] (http://www.azurespeed.com "Azure Latency Test").
> * تتوقف متطلبات عرض النطاق الترددي لـ Dynamics 365 for Talent على السيناريو لديك. تتطلب السيناريوهات الأكثر شيوعاً عرض نطاق ترددي لأكثر من 50 كيلو بايت في الثانية (KBps).

> [!WARNING]
> لا تقم بحساب متطلبات النطاق الترددي من موقع عميل من خلال ضرب عدد المستخدمين في متطلبات الحد الأدنى للنطاق الترددي. يُصعب للغاية حساب الاستخدام المستزامن لموقع ما. بالنسبة للعملاء المهتمين بشأن متطلبات النطاق الترددي، يمكنهم استخدام إصدار المعاينة من Dynamics 365 for Talent.

## <a name="supported-microsoft-office-applications"></a>تطبيقات Microsoft Office المعتمدة

*   لتثبيت الوظائف الإضافية لـ Microsoft Excel و Word، يجب أن يكون لديك Microsoft Office 2016 لـ Windows أو Mac مثبتًا. للحصول على مزيد من التفاصيل حول متطلبات الإصدار، راجع [استكشاف وإصلاح مشاكل تكامل Office] (../dev-itpro/office-integration/office-integration-troubleshooting.md "استكشاف وإصلاح مشاكل تكامل Office").
*   لعرض المستندات التي تم إنشاؤها بواسطة التصدير إلى وظائف Word أو التصدير إلى Excel، يجب عليك تثبيت Microsoft Office 2007 أو الإصدار الأحدث.

## <a name="update-policy"></a>سياسة التحديث

تتم خدمة Microsoft Dynamics 365 for Talent على أنه عرض سحابة. يتم تحديث Dynamics 365 for Talent بشكل مستمر، ويتم تطبيق التحديثات تلقائيًا بواسطة Microsoft.

يتم إصدار التحديثات في وتيرة منتظمة، وستخضع جميع البيئات لعمليات التحديث.  يتم دعم Dynamics 365 for Talent تماشيًا مع [سياسة Microsoft Support Lifecycle] (https://support.microsoft.com/en-us/gp/lifecycle#gp/OSSLpolicy "Microsoft Support Lifecycle")، التي توفر إرشادات متناسقة ومتوقعة لتوافر دعم المنتج.

