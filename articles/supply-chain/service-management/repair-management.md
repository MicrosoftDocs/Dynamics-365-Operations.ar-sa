---
title: إدارة الإصلاح
description: قم بتجميع المشكلات بشكل منظم لمساعدتك على اقتراح الحلول التي ظهر نجاحها في الماضي.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAConditionTable, SMASymptomArea, SMADiagnosisArea, SMAResolutionTable, SMARepairStage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ebb9833be5e51fe59e9895e67cd8e55058078aa
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001324"
---
# <a name="repair-management"></a>إدارة الإصلاح       

[!include [banner](../includes/banner.md)]


لإدارة الإصلاح يمكنك تجميع المشكلات بشكل نظامي. وهذا يساعدك في اقتراح الحلول التي ظهر نجاحها في الماضي.

قم بإعداد الأعراض والتشخيصات وإعدادات الحل. بعد ذلك يمكن تطبيقها كل هذا عند استلام عنصر مشابه لإصلاحه. يمكنك أيضًا إعداد مراحل الإصلاح والتي يمكنها متابعة تقدم إصلاح المشكلة.

## <a name="setting-up-repair-management"></a>إعداد إدارة الإصلاح

استخدام نماذج الإعداد التالية لإدخال المعلومات التي سيتم استخدامها لتحديد الأعراض والتشخيص والحل للإصلاح.

1.  انقر فوق **إدارة الخدمة** \> **الإعداد** \> **الإصلاح** \> **شروط**.

2.  انقر فوق **إدارة الخدمة** \> **الإعداد** \> **الإصلاح** \> **مناطق الأعراض**.

3.  انقر فوق **إدارة الخدمة** \> **الإعداد** \> **الإصلاح** \> **مناطق التشخيص**.

4.  انقر فوق **إدارة الخدمة** \> **الإعداد** \> **الإصلاح** \> **الحلول**.

5.  انقر فوق **إدارة الخدمة** \> **الإعداد** \> **الإصلاح** \> **مراحل الإصلاح**.

## <a name="symptoms-and-conditions"></a>الأعراض والشروط

تصف الأعراض يشخص العميل المشكلة. تتضمن الأعراض ملاحظات العميل التي تشير إلى الحاجة إلى الإصلاح.

يمكنك إعداد مناطق الأعراض وأكوادها والحالات. تغطي مناطق الأعراض منطقة القصور، ويغطي كود الأعراض أعراض القصور. يصف الشرط الحالة أو البيئة الموجودة عند حدوث المشكلة.

**مثال**

إحضار كمبيوتر للإصلاح نظراً لتعطل محرك الأقراص الثابتة بعد فترة ممتدة من الاستخدام. إخفاق محرك الأقراص الثابتة يؤدي إلى خطأ شاشة زرقاء. أدخل الفني الذي استلم الكمبيوتر الأعراض والشروط التالية:

1.  منطقة الأعراض هي محرك الأقراص الثابتة

2.  كود الأعراض هو خطأ شاشة زرقاء

3.  الشرط هو تعطل القرص الثابت بعد الاستخدام لفترة طويلة

## <a name="diagnosis-and-resolutions"></a>التشخيصات والحلول

تحتوي حقول التشخيص والحل على عبارات من منظور الإصلاح. وهي الخطوات التي مر بها الفني لاستقصاء المشكلة.

وتغطي منطقة التشخيصات العملية التي يجب إجراؤها لحل المشكلة. ويعتبر كود التشخيص هو كيفية معالجة المشكلة، وقد يكون الحل هو أن العنصر قد تم إصلاحه أو استبداله أو أن العميل قد قام بإلغاء الطلب. فمثلاً، إذا تم إصلاح الكمبيوتر، فقد تكون منطقة التشخيصات هي "جزء معيب"، ويكون كود التشخيص هو "تم تثبيت بطاقة فيديو جديدة"، ويكون الحل هو "تم استبداله".

## <a name="repair-stages"></a>مراحل الإصلاح

تبين مراحل الإصلاح مدى التقدم في عملية الإصلاح. وتكون المحددة الخاصة بتوقيع مرحلة الإصلاح هي **منتهي** التي تشير إلى أن بند الإصلاح قد اكتمل، وقد تم تسجيل تاريخ الانتهاء ووقته.

## <a name="applying-repair-management"></a>تطبيق إدارة الإصلاح

لتطبيق إدارة الإصلاح على أحد العناصر، يجب أن يتم إعداد هذا العنصر بعلاقة كائن الخدمة في أمر الخدمة. ومن أمر الخدمة يمكنك إنشاء بند إصلاح بالمعلومات حول المشكلة الحالية. وفي بند الإصلاح يمكنك تعريف كائن الخدمة الذي يتم إصلاحه والمعلومات حول الأعراض والتشخيص والتنفيذ. كما يمكنك إنشاء إشعار لبند الإصلاح.

كما يمكنك إنشاء بنود إصلاح لكل خطوة في عملية الإصلاح.

## <a name="create-a-repair-line-on-a-service-order"></a>إنشاء بند إصلاح في أمر خدمة

1.  انقر فوق **إدارة الخدمة** \> **عام** \> **أوامر الخدمات** \> **أوامر الخدمات**.

2.  حدد أمر الخدمة الذي يحتوي على الكائن المراد إصلاحه.

3.  انقر فوق **الإصلاح** \> **بنود الإصلاح** لفتح نموذج **بنود الإصلاح**.

4.  واضغط على CTRL+N لإنشاء بند جديد.

5.  حدد أحد كائنات الخدمة. يمكن تحديد أي كائن من كائنات الخدمة التي تم إعدادها بعلاقة كائن في أمر الخدمة.

6.  حدد أيًا من الأعراض أو التشخيصات أو قيم التنفيذ التي تم تعينها مسبقًا وذات الصلة في بند الإصلاح ثم انقر فوق علامة التبويب **ملاحظة** لإنشاء ملاحظة في بند الإصلاح إذا كانت هناك حاجة إلى ذلك.

7.  اضغط على CTRL+S لحفظ بند الإصلاح الجديد. يتم تحديث حقل **تاريخ ووقت الإنشاء‬** في علامة التبويب **عام** في النموذج **بنود الإصلاح** بوقت الحفظ.

## <a name="tracking-progress-and-resolving-a-repair-issue"></a>تعقب التقدم وحل مشكلة إصلاح

يمكن تعيين مراحل الإصلاح لبند الإصلاح لأجل تعقب تقدم الإصلاح.

عند حل إصلاح مشكلة، يمكنك إغلاق بند الإصلاح. قم بتعيين مرحلة الإصلاح على مرحلة مع تمكين خاصية **منتهى**. يتم تسجيل التاريخ والوقت الحاليين كوقت الانتهاء في البند.

## <a name="close-a-repair-line-for-a-resolved-issue"></a>إغلاق بند الإصلاح لمشكلة تم حلها

1.  افتح النموذج **بنود الإصلاح**. اتبع الإجراء المذكور سابقًا في هذا الموضوع لإنشاء بند إصلاح.

2.  حدد بند الإصلاح الذي يحتوي على المشكلة المراد إغلاقها.

3.  في الحقل **مرحلة الإصلاح**، حدد المرحلة التي تم تمكين الخاصية **منتهي** بها.

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]