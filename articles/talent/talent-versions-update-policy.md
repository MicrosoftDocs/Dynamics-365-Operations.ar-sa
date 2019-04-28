---
title: متطلبات النظام وسياسة التحديث في Talent
description: يسرد هذا الموضوع متطلبات Dynamics 365 for Talent. وقد تم أيضًا توضيح سياسة التحديث.
author: andreabichsel
manager: AnnBe
ms.date: 04/04/2017
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
ms.openlocfilehash: 2389f00b22ec3b5284eeffb2c015533b7a3d13e0
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/19/2019
ms.locfileid: "856291"
---
# <a name="talent-system-requirements-and-update-policy"></a>متطلبات النظام وسياسة التحديث في Talent

[!include [banner](includes/banner.md)]

يسرد هذا الموضوع متطلبات Microsoft Dynamics 365 for Talent. وقد تم أيضًا توضيح سياسة التحديث.

## <a name="supported-web-browsers"></a>مستعرضات الويب المدعومة

يمكن تشغيل تطبيق ويب Dynamics 365 for Talent في أيٍّ من مستعرضات الويب التالية التي تعمل على أنظمة التشغيل المحددة: 

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
> * تم تصميم Dynamics 365 for Talent للشبكات مع زمن وصول من 250-300 مللي ثانية أو أقل. زمن الوصول هذا هو زمن الوصول من عميل المستعرض إلى مركز بيانات Microsoft Azure الذي يستضيف Dynamics 365 for Talent. نوصي باختبار زمن وصول الشبكة على [www.azurespeed.com](https://www.azurespeed.com "اختبار زمن وصول Azure").
> * تعتمد متطلبات عرض النطاق الترددي لتطبيق Dynamics 365 for Talent على السيناريو. تتطلب السيناريوهات الأكثر شيوعاً عرض نطاق ترددي لأكثر من 50 كيلو بايت في الثانية (KBps).
> 
> [!WARNING]
> لا تقم بحساب متطلبات النطاق الترددي من موقع عميل من خلال ضرب عدد المستخدمين في متطلبات الحد الأدنى للنطاق الترددي. يُصعب للغاية حساب الاستخدام المستزامن لموقع ما. بالنسبة إلى العملاء المهتمين بمتطلبات النطاق الترددي، يمكنهم استخدام إصدارًا تجريبيًا من Dynamics 365 for Talent.

## <a name="supported-microsoft-office-applications"></a>تطبيقات Microsoft Office المدعومة

* لتثبيت الوظائف الإضافية لكل من Microsoft Excel وWord، يجب أن يكون Microsoft Office 2016 for Windows أو Mac مثبتًا على جهازك. للحصول على مزيد من التفاصيل حول متطلبات الإصدار، راجع [استكشاف أخطاء تكامل Office‏ وإصلاحها](../dev-itpro/office-integration/office-integration-troubleshooting.md "استكشاف أخطاء تكامل Office‏ وإصلاحها").
* لعرض المستندات التي تم إنشاؤها بواسطة وظيفة التصدير إلى Word أو التصدير إلى Excel، يجب عليك تثبيت Microsoft Office 2007 أو إصدار لاحق.

## <a name="update-policy"></a>سياسة التحديث

يتم تقديم الخدمات لتطبيق Microsoft Dynamics 365 for Talent في إطار عرض سحابي. تعتبر تحديثات Dynamics 365 for Talent متواصلة ومطبقة بشكل تلقائي بواسطة Microsoft.

يتم إصدار التحديثات في وتيرة منتظمة، وستخضع جميع البيئات لعمليات التحديث.  يتم دعم Dynamics 365 for Talent تماشيًا مع [دورة حياة دعم Microsoft](https://support.microsoft.com/en-us/gp/lifecycle#gp/OSSLpolicy "دورة حياة دعم Microsoft")، التي توفر إرشادات متناسقة ومتوقعة لتوفر دعم المنتج.
