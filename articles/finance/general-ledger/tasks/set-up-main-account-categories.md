---
title: إعداد فئات الحساب الرئيسي
description: يشرح هذا الموضوع كيفية إعداد ‏‫فئات الحساب الرئيسية في Dynamics 365 Finance.
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 957fdc184410dc85f54cd3163799a9003f0727bb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222205"
---
# <a name="set-up-main-account-categories"></a>إعداد فئات الحساب الرئيسي

[!include [banner](../../includes/banner.md)]

يشرح هذا الموضوع كيفية إعداد ‏‫فئات الحساب الرئيسية. يتم استخدام فئات الحساب الرئيسي للتقارير الافتراضية في الإبلاغ المالي وفي Power BI. يمكن إعادة تسمية فئات الحساب الرئيسي التي تم إنشاؤها بشكل افتراضي ولكن لا يمكن حذفها. يمكن إنشاء فئات حساب إضافية واستخدامها لأغراض إعداد التقارير والتحليل. يستخدم هذا الموضوع شركة العرض التجريبي "USMF".

## <a name="create-a-main-account-category"></a>إنشاء فئة حساب رئيسي
1. في جزء التنقل، انتقل إلى **الوحدات النمطية > دفتر الأستاذ العام > دليل الحسابات > الحسابات > فئات الحساب الرئيسية‬**.
2. حدد **جديد**.
3. أدخل اسمًا فريدًا في حقل **فئة الحساب الرئيسي** .
4. في الحقل **الوصف**، أدخل وصفًا لفئة الحساب الرئيسي.
5. في الحقل **نوع الحساب الرئيسي**، حدد نوع الحساب الرئيسي الذي سيتم ربطه بالفئة.

## <a name="link-main-accounts-to-account-category"></a>ربط الحسابات الرئيسية بفئة حساب
1. انقر فوق **ربط الحسابات الرئيسية**.
2. في القائمة، حدد الحسابات الرئيسية لتعيينها إلى فئة الحساب الرئيسي عن طريق تحديد خانات الاختيار في العمود **مرتبط**. سيؤدي تعيين الحسابات الرئيسية لفئة حساب رئيسي إلى تجميع أرصدة الحسابات عند استخدام هذه الفئة للتقارير المالية والتحليل المالي.  
3. حدد الخيار **مرتبط** أو قم بإلغاء تحديده لاختيار الحسابات الرئيسية.
4. حدد **موافق**.
5. حدد **نعم**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]