---
title: اعتبارات تحسين محرك البحث (SEO) لموقعك
description: يغطي هذا الموضوع اعتبارات تحسين محرك البحث (SEO) للموقع الخاص بك من التطوير إلى الإنتاج.
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 639d6fa74954b5f74560c7e51523ab2b4d2b7f62
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989342"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a>اعتبارات تحسين محرك البحث (SEO) لموقعك


[!include [banner](includes/banner.md)]

يغطي هذا الموضوع اعتبارات تحسين محرك البحث (SEO) للموقع الخاص بك من التطوير إلى الإنتاج.

## <a name="a-site-that-is-under-development"></a>موقع تحت التطوير

بينما يكون الموقع تحت التطوير، يجب أن تحتوي كافة الصفحات على علامات التعريف **NOINDEX** و **NOFOLLOW**، بحيث لا تقوم محركات البحث بفهرسة الصفحات وتخزين إصدارات تطوير الموقع الخاص بك في ذاكرة التخزين المؤقت الخاصة بك للقيام بهذا التكوين، يجب عليك إضافة الوحدة النمطية الافتراضية لعلامات التعريف إلى قالب صفحة الموقع. ستتوفر خصائص علامات التعريف الافتراضية في قسم خصائص SEO في محرر الصفحة. يمكنك استخدام هذه الخصائص لإدارة علامات التعريف.

## <a name="soft-launch-of-a-site"></a>التشغيل التجريبي لموقع

أثناء "التشغيل التجريبي"، يقتصر توافر موقع ويب على جمهور أو سوق قبل الإصدار الكامل. إذا قمت بالتشغيل التجريبي لموقع الويب الخاص بك، فإنه يجب عليك ترك علامات التعريف **NOINDEX** من مكانها. وبهذه الطريقة، فإنك تساعد على ضمان اقتصار التشغيل التجريبي على جمهور محدد تود أن يصل إلى الموقع.

## <a name="a-site-that-is-in-production"></a>موقع قيد الإنتاج

عندما يكون موقع قيد الإنتاج، يجب عليك التأكد من وضع علامات على كافة صفحات الموقع بشكل صحيح. تستخدم Microsoft Dynamics 365 Commerce المعلومات التي يتم إدخالها لصفحة لإظهار كافة معلومات SEO في تلك الصفحة. توفر الوحدات النمطية التالية هذه الوظيفة: ملخص صفحة الفئة وملخص صفحة القائمة وملخص صفحة المنتج.

لتحسين فهرسه محرك البحث، يستخدم إطار العمل الظاهر كلاً من المعومات وخصائص SEO التي تم تكوينها في Dynamics 365 Commerce والمعلومات الخاصة بالوحدة النمطية. بالنسبة للموقع الموجود في الإنتاج، يجب التأكد من أن الملف robots.txt يسمح بفهرسة موقعك بالكامل، وإنه يحتوي على ارتباطات إلى مستند خريطة الموقع المنشور الخاص بك. يجب عليك تشغيل وظيفة إنشاء خريطة الموقع عند **إعدادات الموقع \> خريطة الموقع ممكنة**.

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a>إعدادات SEO الخاصة بالصفحة للمعاينة الداخلية وشرائح الجمهور المحدودة وكافة شرائح الجمهور.

لأن Dynamics 365 Commerce يدعم المعاينات المصادقة "ما تشاهده هو ما تحصل عليه"(WYSIWYG) في أداة إنشاء الصفحات المرئية، يستطيع المؤلفون إعداد محتوى الصفحة دون القلق عن المعلومات التي ستصبح مرئية إلى زائري الموقع. إذا كان يجب نشر الصفحة، ولكن يجب أن يكون العرض الخاص بها محدودًا، فإنها يجب أن تحتوي على علامة تعريف **NOINDEX**، بحيث لن تتم فهرستها بواسطة محركات البحث. وبعد ذلك، عندما تكون الصفحة جاهزة لكافة شرائح الجمهور المستهدفة، يجب أن تكون كافة بيانات تعريف SEO الأساسية موجودة، لزيادة فعالية فهرسة محرك البحث. بالإضافة إلى ذلك، يجب إزالة علامة التعريف **NOLIMIT**.

## <a name="additional-resources"></a>الموارد الإضافية

[إدارة المستخدمين والأدوار في التجارة الإلكترونية](manage-ecommerce-users-roles.md)

[إضافة تعليمات برمجية لبرنامج نصي إلى صفحات الموقع لدعم تتبع الاستخدام](add-telemetry.md)

[إدارة سياسة أمان المحتوى (CSP)](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]