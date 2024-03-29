---
title: تخصيص الوقت للوظائف في مجموعة الوظائف‬
description: في تنفيذ التصنيع، يمكنك تجميع الوظائف. يمكنك عندئذٍ بدء مهام متعددة في نفس الوقت في صفحة قائمة الوظائف.
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgBundleSlize, JmgProdParameters, JmgRegistration
audience: Application User
ms.reviewer: kamaybac
ms.custom: 55591
ms.assetid: 358efce7-73c8-4d2a-a7f7-cb99b88ab6ee
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb0236f9f39afc67cb5c8cedecee5278a6555d03deefb859fc134a4a4160285b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766597"
---
# <a name="allocate-time-to-jobs-in-a-job-bundle"></a>تخصيص الوقت للوظائف في مجموعة الوظائف‬

[!include [banner](../includes/banner.md)]

في تنفيذ التصنيع، يمكنك تجميع الوظائف. يمكنك عندئذٍ بدء مهام متعددة في نفس الوقت في صفحة قائمة الوظائف.

إذا قمت بتجميع الوظائف، يجب تحديد كيفية تخصيص وقت التسجيل الإجمالي لكافة الوظائف لكل وظيفة. ويمكنك تحديد التوزيع عن طريق تحديد أحد الخيارات التالية في حقل **نوع المجموعة** في صفحة **مفاتيح التوزيع**:

-   **التقدير** – يتم تقسيم الوقت بين الوظائف وفقًا للوقت المقدر للوظائف.
-   **الوظائف** – يتم تقسيم الوقت وفقًا لإجمالي الوظائف المجمعة ومقدار الوقت الذي استغرقه إنهاء كافة الوظائف.
-   **الوقت الصافي** – يتم تقسيم الوقت بالتساوي بين الوظائف الموجودة ضمن المجموعة في أي وقت.
-   **الوقت الفعلي** – يتم توزيع الوقت الفعلي لأداء الوظيفة. ويمكن حساب التكلفة على أساس تكلفة الرواتب الفعلية. **ملاحظة:** يتوفر مفتاح توزيع **الوقت الحقيقي** فقط إذا كانت شركتك تستخدم وظيفة كشوف المرتبات في الوقت والحضور.

توضح الأمثلة التالية نتائج مفاتيح التوزيع المختلفة.

## <a name="example-scenario"></a>سيناريو كمثال
يجب إكمال ثلاث وظائف في قائمة انتظار العمل الخاصة بك. ويمكنك بدء الوظيفة الأولى، وبينما هذه الوظيفة قيد التقدم، تبدأ الوظيفتين الثانية والثالثة. ولذلك، هناك مجموعة من ثلاث وظائف. يعرض الجدول التالي وقت الإنتاج المقدر لكل وظيفة.

| الوظيفة   | وقت الإنتاج |
|-------|-----------------|
| المهمة الأولى | 1 ساعة          |
| المهمة الثانية | ثلاث ساعات         |
| المهمة الثالثة | 4 ساعات         |
| الإجمالي | ثمان ساعات         |

يوضح الجدول التالي ساعات العمل الفعلية التي يتم قضاؤها في كل وظيفة.

| الوظيفة    | وقت البدء | وقت الانتهاء | وقت المجموعة |
|--------|------------|----------|-------------|
| المهمة الأولى  | 00:09      | 11:00    | ساعتان     |
| المهمة الثانية  | 10:00      | 13:00    | ثلاث ساعات     |
| المهمة الثالثة  | 10:00      | 00:15    | خمس ساعات     |
| تجميع | 00:09      | 00:15    | ست ساعات     |

تصف الأقسام التالية نتائج الوقت المحسوب لكل مفتاح توزيع.

## <a name="estimation-allocation-key"></a>مفتاح توزيع التقدير
يوضح الجدول التالي معادلة حساب الوقت الموزع. فيما يلي المعادلة: الوقت لكل وظيفة - إجمالي وقت المجموعة × (وقت الوظيفة المقدر ÷ إجمالي الوقت المقدر)

| الوظيفة   | المعادلة           | الوقت الموزع |
|-------|-------------------|----------------|
| المهمة الأولى | 6 × (1 ÷ 8) ساعات | 0.75 ساعة      |
| المهمة الثانية | 6 × (3 ÷ 8) ساعات | 2.25 ساعات     |
| المهمة الثالثة | 6 × (4 ÷ 8) ساعات | 3.00 ساعات     |

## <a name="jobs-allocation-key"></a>مفتاح توزيع الوظائف
يوضح الجدول التالي معادلة حساب الوقت الموزع. فيما يلي المعادلة: الوقت لكل وظيفة = إجمالي وقت المجموعة ÷ عدد الوظائف

| الوظيفة   | المعادلة | الوقت الموزع |
|-------|---------|----------------|
| المهمة الأولى | 6 ÷ 3   | ساعتان        |
| المهمة الثانية | 6 ÷ 3   | ساعتان        |
| المهمة الثالثة | 6 ÷ 3   | ساعتان        |

## <a name="net-time-allocation-key"></a>مفتاح توزيع الوقت الصافي
يوضح الجدول التالي معادلة حساب الوقت الموزع. فيما يلي المعادلة: الوقت المحسوب لكل إبلاغ = وقت المجموعة ÷ عدد الوظائف

| مثال                       | 09:00–10:00 (ساعة واحدة) | 10:00–11:00 (ساعة واحدة) | 11:00–13:00 (ساعتان) | 13:00–15:00 (ساعتان) | الوقت الموزع |
|------------------------------|----------------------|----------------------|-----------------------|-----------------------|----------------|
| عدد الوظائف في المجموعة | 1                    | 3                    | 2                     | 1                     | غير قابل للتطبيق |
| المهمة الأولى                        | 1 ÷ 1 = ساعة واحدة       | 1 ÷ 3 = 0.33 ساعة    | غير قابل للتطبيق        | غير قابل للتطبيق        | 1.33 ساعة     |
| المهمة الثانية                        | غير قابل للتطبيق       | 1 ÷ 3 = 0.33 ساعة    | 2 ÷ 2 = ساعة واحدة        | غير قابل للتطبيق        | 1.33 ساعة     |
| المهمة الثالثة                        | غير قابل للتطبيق       | 1 ÷ 3 = 0.33 ساعة    | 2 ÷ 2 = ساعة واحدة        | 2 ÷ 1 = ساعتان       | 3.33 ساعات     |

## <a name="real-time-allocation-key"></a>مفتاح توزيع الوقت الفعلي
إذا أردت حساب تكاليف الإنتاج استناداً إلى التكاليف الفعلية، يجب عليك مسح خيار **فئة التكلفة** في صفحة **القيم الافتراضية لأوامر الإنتاج**. يوضح الجدول التالي معادلة حساب الوقت الموزع. فيما يلي المعادلة: الوقت الفعلي لكل وظيفة = الوقت الفعلي في مجموعة

| الوظيفة   | الوقت الفعلي |
|-------|-------------|
| المهمة الأولى | ساعتان     |
| المهمة الثانية | ثلاث ساعات     |
| المهمة الثالثة | خمس ساعات     |

خذ بعين الاعتبار الوظائف الثلاث التي يتم تنفيذها بواسطة عامل بأجر حسب الساعة مبلغ 12.00 دولاراً أمريكيًا. لم يتم تقديم أية مكافآت أو علاوات خاصة بالوقت الإضافي في الوقت الذي استغرقته الوظائف. ولقد عمل العامل في هذه الوظائف المجمعة الثلاث لوقت يقدر إجمالاً بست ساعات. ولذلك، تكلفة الراتب تساوي 6 × 12.00 دولاراً أمريكيًا = 72.00 دولاراً أمريكيًا. وعند استخدام توزيع الوقت الفعلي، تتم إعادة حساب التكلفة لكل ساعة باستخدام العامل من معادلة الوقت الصافية. كما يتم عندئذ تحويل الوقت الفعلي الذي قضي في كل وظيفة مع سعر التكلفة المصححة لكل ساعة. في هذا المثال، تم قضاء ست ساعات على الرغم من توزيع عشر ساعات. يوضح الجدول التالي معادلة حساب التكلفة. فيما يلي المعادلة: التكلفة لكل ساعة = (وقت المجموعة ككل لكل وظيفة (الوقت الصافي) ÷ الوقت الفعلي لكل وظيفة) × سعر التكلفة القياسي لكل ساعة

| الوظيفة   | حساب التكلفة المصححة لكل ساعة | التكلفة المصححة لكل ساعة | الوقت الموزع | التكلفة الإجمالية لوظيفة |
|-------|----------------------------------------|-------------------------|----------------|-------------------|
| الوظيفة 1 | (1.33 ÷ 2) × دولارًا أمريكيًا 12.00                 | 8.00 دولارًا أمريكيًا                | ساعتان        | 16.00 دولارًا أمريكيًا         |
| الوظيفة 2 | (1.33 ÷ 3) × 12.00 دولارًا أمريكيًا                 | 5.33 دولار أمريكي                | ثلاث ساعات        | 16.00 دولارًا أمريكيًا         |
| الوظيفة 3 | (3.33 ÷ 5) × دولارًا أمريكيًا 12.00                 | 8.00 دولارًا أمريكيًا                | خمس ساعات        | 40.00 دولارًا أمريكيًا         |

يتم ترحيل التكلفة المصححة لكل ساعة ووقت الوظيفة في دفتر يومية الإنتاج. **ملاحظة:** إذا قمت بتحديد خيار **فئة التكلفة** في علامة التبويب **عام** في صفحة **القيم الافتراضية لأوامر الإنتاج**، يتم نقل الوقت الفعلي لكل مهمة يتم نقل إلى دفتر يومية إنتاج، حيث يتم تطبيق التكلفة لفئة التكلفة الخاصة بالوظيفة المحددة.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]