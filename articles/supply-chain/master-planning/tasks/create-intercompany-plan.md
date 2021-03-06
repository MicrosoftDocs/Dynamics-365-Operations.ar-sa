---
title: إنشاء خطة بين الشركات الشقيقة
description: يوضح هذا الإجراء كيفية إنشاء خطة بين الشركات شقيقة.
author: ShylaThompson
manager: tfehr
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c368e461860a41d0110f5aed79c2aac49c437d68
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011388"
---
# <a name="create-an-intercompany-plan"></a>إنشاء خطة بين الشركات الشقيقة

[!include [banner](../../includes/banner.md)]

يوضح هذا الإجراء كيفية إنشاء خطة بين الشركات شقيقة. شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.


## <a name="set-up-an-intercompany-planning-group"></a>إعداد مجموعة تخطيط بين الشركات الشقيقة 
1. في **جزء التنقل**، انتقل إلى **الوحدات النمطية > التخطيط الرئيسي > الإعداد > مجموعات التخطيط بين الشركات الشقيقة‬**. 
2. استخدم عامل التصفية السريع للبحث عن السجلات. على سبيل المثال، قم بإجراء التصفية على حقل الاسم بقيمة '10'.
3. في القائمة، قم بوضع علامة للصف المحدد.
4. انقر فوق **حذف**. تُعد هذه الخطوة ضرورية من أجل تقصير تشغيل التخطيط بين الشركات الشقيقة.   سيقوم التخطيط بين الشركات الشقيقة بتشغيل التخطيط الرئيسي في كل الشركات في مجموعة تخطيط، بدءًا من تسلسل الجدولة الأدنى.  
5. انقر فوق **نعم**.
6. قم بإغلاق الصفحة.

## <a name="create-an-intercompany-plan"></a>إنشاء خطة بين الشركات الشقيقة
1. في **جزء التنقل**، انتقل إلى **الوحدات النمطية > التخطيط الرئيسي > مساحات العمل > التخطيط الرئيسي‬**.
2. انقر فوق **تخطيط رئيسي بين الشركات الشقيقة**.  
3. في الحقل **مجموعة التخطيط بين الشركات الشقيقة‬**، انقر فوق زر القائمة المنسدلة لفتح البحث.
4. في القائمة، انقر فوق الارتباط في الصف المحدد. حدد مجموعة التخطيط بين الشركات الشقيقة 10.  
5. في الحقل **عدد تكرارات التخطيط بين الشركات الشقيقة**، أدخل '2'. هناك عضوان في مجموعة التخطيط بين الشركات الشقيقة 10. من أجل نشر التأخيرات من الشركة المصدر (USMF) إلى شركة العميل (DEMF)، سوف تحتاج إلى تشغيل التخطيط بين الشقيقة في الشركتين مرتين. سيقوم التكرار الأول بنشر الطلب وتحديد حالات التأخير في الشركة المصدر (USMF). أما التكرار الثاني فسيقوم بنشر التأخيرات من USMF إلى DEMF.  
6. في الحقل **التكرار الأول‬**، حدد "إعادة إنشاء‬".
7. في الحقل **التكرارات اللاحقة‬‬**،  حدد "إعادة إنشاء‬"‬.
8. في الحقل **عدد السلاسل**، أدخل رقمًا. يمثل هذا عدد السلاسل المتوازية التي تستخدم للتخطيط.  
9. انقر فوق **موافق**.

## <a name="view-the-result-of-the-plan"></a>عرض نتيجة الخطة
1. في الحقل **الخطة**، انقر فوق زر القائمة المنسدلة لفتح البحث.
2. في القائمة، انقر فوق الارتباط في الصف المحدد. انقر فوق ارتباط StaticPlan. عليك أن تكون في شركة USMF.  
3. انقر فوق **الأوامر المخططة**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]