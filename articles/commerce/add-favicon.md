---
title: إضافة أيقونة المفضلة
description: ‏‫يوضح هذا الموضوع كيفية إضافة أيقونة مفضلة إلى الموقع الخاص بك.‬
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 18e12cbe46650fcf024a56b6de9a8cb2903d2bf8
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914553"
---
# <a name="add-a-favicon"></a>إضافة أيقونة المفضلة

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

‏‫يوضح هذا الموضوع كيفية إضافة أيقونة مفضلة إلى الموقع الخاص بك.‬

## <a name="overview"></a>نظرة عامة

وأيقونة المفضلة هي ملف رسومي صغير يتم عرضة على علامة تبويب مستعرض ويب، في شريط العنوان، وفي محفوظات الاستعراض، وفي الإشارات المرجعية أو المفضلة، من بين أماكن أخرى. نوصي أن تقوم بإضافة أيقونة المفضلة إلى موقعك، لأنها تعرض وتعزز علامتك التجارية، وتساعد في تمييز موقعك عن المواقع الأخرى التي يزورها عملائك.

على الرغم من أنه يُمكنك إضافة عدة أيقونات للمفضلة بأحجام مختلفة وأنواع ملفات إلى موقعك، ويوضح هذا الموضوع كيفية إضافة أيقونة مفضلة واحدة. ولكن، يتم استخدام نفس العملية والموقع لإضافة أكثر من أيقونة المفضلة.

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a>تحميل أيقونة المفضلة إلى مجموعة أصول الموقع الخاص بك

لتحميل أيقونة المفضلة إلى مجموعة أصول الموقع الخاص بك، اتبع الخطوات التالية.

1. انتقل إلى **الأصول \> تحميل \> تحميل الأصول**.
1. ابحث عن أيقونة المفضلة في نظام ملفاتك المحلي وحددها.
1. ادخل تجانب، ثم حدد **موافق**. 
1. في جزء الخصائص الموجود على اليمين، انسخ عنوان URL العمومي لأيقونة المفضلة.

> [!NOTE]
> إذا لم تقم بتحديد خيار **نشر الأصول بعد التحميل** ، يجب عليك العودة إلى صفحة **الأصول** ، ونشر أيقونة المفضلة يدويًا في وقت لاحق.

## <a name="create-the-html-for-the-favicon"></a>قم بإنشاء HTML لأيقونة المفضلة

لإنشاء HTML لأيقونة المفضلة، استخدم جزء HTML التالي. بالنسبة للسمة **href** ،استبدل **"عنوان URL\_العمومي\_لـ\_أيقونة المفضلة\_الخاصة بك"** بعنوان URL الذي قمت بنسخه سابقًا.

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="add-the-html-for-the-favicon-to-the-head-element-of-your-pages"></a>إضافة HTML لأيقونة المفضلة إلى عنصر \<العنوان\> في الصفحات الخاصة بك

لإضافة أيقونة المفضلة إلى موقعك، استخدم نفس الإجراء المستخدم لإضافة أي نوع من HTML أو البرنامج النصي إلى عنصر **\<العنوان\>** لصفحات موقعك.

## <a name="additional-resources"></a>الموارد الإضافية

[إضافة شعار](add-logo.md)

[تحديد سمة الموقع](select-site-theme.md)

[العمل CSS مع ملفات التجاوز](css-override-files.md)

[إضافة رسالة ترحيب](add-welcome-message.md)

[إضافة إشعار لحقوق النشر](add-copyright-notice.md)

[إضافة لغات إلى الموقع الخاص بك](add-languages-to-site.md)

[إضافة تعليمات برمجية لبرنامج نصي إلى صفحات الموقع لدعم تتبع الاستخدام](add-telemetry.md)

