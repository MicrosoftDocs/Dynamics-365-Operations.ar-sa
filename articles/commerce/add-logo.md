---
title: إضافة شعار
description: يوضح هذا الموضوع كيفية إضافة شعار إلى موقعك في Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f15680deb0eab763ba68f2897139c915d1f8a6a3
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817320"
---
# <a name="add-a-logo"></a>إضافة شعار

[!include [banner](includes/banner.md)]

يوضح هذا الموضوع كيفية إضافة شعار إلى موقعك في Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>نظرة عامة

عند إنشاء موقعك، من بين الأشياء الأولى التي ربما ستقوم بها هي إضافة شعار شركتك أو علامتك التجارية إلى رأس الموقع. توفر مكتبة الوحدات النمطية في Dynamics 365 Commerce عبر الإنترنت وحدة تجعل هذه المهمة سهلة.

يمكنك إضافة شعار مباشرة إلى قالب أو تخطيط أو صفحة. بهذه الطريقة، يمكنك بسهولة تغيير الشعار الذي يظهر على صفحات أو مجموعات محددة من الصفحات. ومع ذلك، يغطي هذا الموضوع السيناريو الأكثر شيوعًا، حيث تضيف شعارك إلى جزء من الرأس يمكن إعادة استخدامه عبر جميع صفحات موقعك.

## <a name="prerequisites"></a>المتطلبات الأساسية

قبل أن تتمكن من إضافة شعار إلى جميع صفحات موقعك، ينبغي عليك إكمال هذه المهام.

1. قم بتحميل الشعار إلى مكتبة الوسائط.
1. إنشاء جزء الرأس. لمزيد من المعلومات حول كيفية إنشاء الأجزاء واستخدامها، راجع [العمل مع الأجزاء](work-with-fragments.md)
1. قم بتضمين جزء الرأس في القالب الذي تستخدمه صفحات موقعك لتخطيطها وخيارات الوحدة النمطية. لمزيد من المعلومات حول القوالب، راجع [العمل مع القوالب](work-with-templates.md).

## <a name="add-a-logo-to-a-header-fragment"></a>إضافة شعار إلى جزء الرأس

لإضافة شعار إلى جزء الرأس لموقعك، اتبع هذه الخطوات.

1. في جزء التنقل على اليسار، حدد **الأجزاء**.
1. حدد جزء الرأس الذي أنشأته، ثم حدد **تحرير**.
1. قم بتوسيع وحدة الرأس.
1. في جزء الخصائص لوحدة الرأس، قدم صورة وارتباطًا للشعار. 
1. احفظ جزء الرأس ثم انشره بعد الانتهاء من تحريره.

بعد نشر جزء الرأس المحدّث، سوف تُظهر جميع صفحات الموقع التي تستخدم القالب الذي يحتوي على جزء الرأس شعارك.

## <a name="additional-resources"></a>الموارد الإضافية

[تحديد سمة الموقع](select-site-theme.md)

[العمل CSS مع ملفات التجاوز](css-override-files.md)

[إضافة أيقونة المفضلة](add-favicon.md)

[إضافة رسالة ترحيب](add-welcome-message.md)

[إضافة إشعار لحقوق النشر](add-copyright-notice.md)

[إضافة لغات إلى الموقع الخاص بك](add-languages-to-site.md)

[إضافة تعليمات برمجية لبرنامج نصي إلى صفحات الموقع لدعم تتبع الاستخدام](add-telemetry.md)

