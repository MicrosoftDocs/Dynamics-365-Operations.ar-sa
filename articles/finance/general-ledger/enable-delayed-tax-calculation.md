---
title: تمكين حساب الضريبة المؤجل في دفتر اليومية
description: يوضح هذا الموضوع كيفية استخدام ميزة **تمكين حساب الضريبة المؤجل في دفتر اليومية‬** لتحسين أداء حساب الضريبة عندما يكون حجم بنود دفتر اليومية ضخمًا.
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 5a8ae30a007d3e2b8b7a9bc9eb7786f6e58246d0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176188"
---
# <a name="enable-delayed-tax-calculation-on-journal"></a>تمكين حساب الضريبة المؤجل في دفتر اليومية
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

يوضح هذا الموضوع كيفية استخدام ميزة **تمكين حساب الضريبة المؤجل في دفتر اليومية‬** لتحسين أداء حساب الضريبة عندما يكون حجم بنود دفتر اليومية ضخمًا.

يتم تشغيل سلوك حساب ضريبة المبيعات الحالي في الوقت الحقيقي على دفتر اليومية عندما يقوم المستخدم بتحديث حقول الضرائب ذات الصلة، على سبيل المثال، مجموعة ضريبة المبيعات/مجموعة ضريبة مبيعات الأصناف. سيقوم أي تحديث على مستوى بنود دفتر اليومية بإعادة حساب مبلغ الضريبة في كافة بنود دفتر اليومية. من شأن ذلك أن يساعد المستخدم علي رؤية مبلغ الضريبة المحسوب في الوقت الحقيقي، ولكنه قد يؤدي أيضًا إلى حدوث مشكلة في الأداء إذا كان حجم بنود دفتر اليومية ضخمًا.

توفر هذه الميزة خيارًا لتأجيل حساب الضريبة لحل مشكلة الأداء. إذا كان هذه الميزة قيد التشغيل، سيتم حساب مبلغ الضريبة فقط عند قيام المستخدم بالنقر فوق الأمر "ضريبة المبيعات" أو ترحيل دفتر اليومية.

بإمكان المستخدم تشغيل/إيقاف تشغيل المعلمة على ثلاثة مستويات:
- بواسطة الكيان القانوني
- حسب اسم دفتر اليومية
- حسب رأس دفتر اليومية

سيعتبر النظام قيمة المعلمة في رأس دفتر اليومية قيمة نهائية. ستكون قيمة المعلمة على رأس دفتر اليومية بشكل افتراضي القيمة من اسم دفتر اليومية. ستكون قيمة المعلمة على اسم دفتر اليومية بشكل افتراضي القيمة من معلمة دفتر الأستاذ العام عند إنشاء اسم دفتر اليومية.

سيتم إخفاء الحقلين "مبلغ ضريبة المبيعات الفعلي" و"مبلغ ضريبة المبيعات المحسوب" على دفتر اليومية في حالة تشغيل هذه المعلمة. الغرض ليس إرباك المستخدم لأن قيمة هذين الحقلين ستعرض دائمًا 0 قبل ان يقوم المستخدم بتشغيل حساب الضريبة.

## <a name="enable-delayed-tax-calculation-by-legal-entity"></a>تمكين حساب الضريبة المؤجل حسب الكيان القانوني

1. انتقل إلى **دفتر الأستاذ العام > إعداد دفتر الأستاذ‬ > معلمات دفتر الأستاذ العام**.
2. انقر فوق علامة التبويب **ضريبة المبيعات**.
3. ضمن علامة‏‎ التبويب السريعة **عام**، ابحث عن المعلمة **حساب الضريبة المؤجل**، وقم بتشغيلها/إيقاف تشغيلها.

![](media/delayed-tax-calculation-gl.png)



## <a name="enable-delayed-tax-calculation-by-journal-name"></a>تمكين حساب الضريبة المؤجل حسب اسم دفتر اليومية

1. انتقل إلى **دفتر الأستاذ العام > إعداد دفتر اليومية > أسماء دفاتر اليومية**.
2. ضمن علامة‏‎ التبويب السريعة **عام**، ابحث عن المعلمة **حساب الضريبة المؤجل**، وقم بتشغيلها/إيقاف تشغيلها.

![](media/delayed-tax-calculation-journal-name.png)

## <a name="enable-delayed-tax-calculation-by-journal"></a>تمكين حساب الضريبة المؤجل حسب دفتر اليومية

1. انتقل إلى **دفتر الأستاذ العام > إدخالات دفتر اليومية > دفاتر اليومية العامة**‬
2. انقر فوق **جديد**
3. حدد اسم دفتر اليومية
4. انقر فوق **الإعداد**
5. ابحث عن المعلمة **حساب الضريبة المؤجل**، وقم بتشغيلها/إيقاف تشغيلها.

![](media/delayed-tax-calculation-journal-header.png)