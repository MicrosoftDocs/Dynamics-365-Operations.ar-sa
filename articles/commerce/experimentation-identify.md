---
title: تحديد الفرضية وتحديد المقاييس الخاصة بتجربة
description: يوضح هذا الموضوع كيفيه تحديد مقاييس الفرضية والنجاح لتجربه تقوم بتشغيلها علي موقع ويب خاص بالتجارة الكترونيه في Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 99642861d69b7545f03c6ed2c2650eadeb377534
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930130"
---
# <a name="identify-a-hypothesis-and-determine-success-metrics-for-an-experiment"></a>تحديد الفرضية وتحديد المقاييس الخاصة بتجربة
تتضمن المرحلة الاولي في دوره حياه التجربة تعريف الفرضية للتجربة وتحديد القياسات التي ستتعقبها لتقييم النجاح. يوضح الرسم التخطيطي التالي كافة الخطوات المتضمنة في [اعداد وتشغيل تجربه](experimentation-overview.md)  علي أحد مواقع التجارة الالكترونيه في Dynamics 365 Commerce. وتتم تغطيه الخطوات الاضافيه في موضوعات منفصلة. 

[![رحلة مستخدم التجربة - التحديد](./media/experimentation_identify.svg)](./media/experimentation_identify.svg#lightbox)

الفرضية هو البيان الذي يمكنك التنبؤ بنتيجة التجربة فيه. تنتقل العديد من العوامل إلى تعريف الفرضية، علي سبيل المثال، البحث عن سلوك المستخدم وبيانات موقع الويب التي قمت بتجميعها. باستخدام الفرضية، ستقوم بتعريف الافتراضات أو النظرية التي ترغب في التحقق من صحتها بتجربتك. قد يكون الهدف من المفترض هو ان تكون " *صوره لقميص أبيض علي الصفحة الرئيسية تؤدي إلى تحريك معدل تتبع الاستخدام أكثر من السترات الزرقاء اثناء شهور الصيف نظرا لان الأشخاص يرغبون في وجود شيء خفيف ولون خفيف في الصيف.* " في هذه الحالة، ستقوم بإنشاء التنوعات التي تتضمن القميص الأبيض والسترة الزرقاء، ونشر كل منهما في نفس الوقت.

للتحقق من صحة الفرضية، يجب ان يتم ربط نجاح أو فشل التجربة مباشره بإجراءات المستخدم؛ علي سبيل المثال، إذا قام مستخدم موقع ويب بالنقر فوق ارتباط أو زر. يجب ان تتوافق هذه الإجراءات مع الاحداث التي سيتم الاعلام عنها لتعقب خدمه الجهة الأخرى الخاصة بالتجربة. بمرور الوقت، سيتم تدوين النسبة المئوية للمستخدمين الذين ياخذون الاجراء كقياس يمكنك استخدامه لإنشاء تقارير واجراء تحليلات. قم بالرجوع إلى [احداث مكون التجارة الخاصة بالتشخيص](dev-itpro/retail-component-events-diagnostics-troubleshooting.md)وموضوع استكشاف الأخطاء وإصلاحها لمراجعه كافة الاحداث والسمات المتاحة.

## <a name="previous-step"></a>الخطوة السابقة
[الاختبار في Dynamics 365 Commerce](experimentation-overview.md)


## <a name="next-step"></a>الخطوة التالية
[إعداد تجربة](experimentation-setup.md)
