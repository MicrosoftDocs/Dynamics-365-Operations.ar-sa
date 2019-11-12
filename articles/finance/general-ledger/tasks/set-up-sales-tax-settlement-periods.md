---
title: إعداد فترات تسوية ضريبة المبيعات
description: يشرح هذا الموضوع كيفية إعداد ‏‫فترات تسوية ضريبة المبيعات‬ في Dynamics 365 Finance.
author: twheeloc
manager: AnnBe
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c17a0240c29dad58c958ab1ce844ee5d8384bd1f
ms.sourcegitcommit: 574309903f15eeab7911091114885b5c7279d22a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/24/2019
ms.locfileid: "2658919"
---
# <a name="set-up-sales-tax-settlement-periods"></a>إعداد فترات تسوية ضريبة المبيعات

[!include [task guide banner](../../includes/task-guide-banner.md)]

يشرح هذا الموضوع كيفية إعداد ‏‫فترات تسوية ضريبة المبيعات‬. تحتوي فترات تسوية ضرائب المبيعات على معلومات عن الفترات الزمنية التي يجب خلالها الإبلاغ عن الضرائب ودفعها. يمكن تشغيل عملية التسوية لفترة تسوية وفترة تاريخ محددة. وستتم تسوية كافة أكواد الضرائب المقترنة بفترة التسوية. بالاستناد إلى إعداد هيئة ضريبة المبيعات ذات الصلة، يتم ترحيل الالتزام الضريبي إما إلى حساب مورّد أو حساب دفتر أستاذ عام.

تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.

1. في جزء التنقل، انتقل إلى **الوحدات النمطية > الضريبة > الضرائب غير المباشرة > ضريبة المبيعات > فترات تسوية ضرائب المبيعات‬**.
2. حدد **جديد**.
3. في الحقل **فترة التسوية‬**، اكتب قيمة.
4. في حقل **الوصف**، اكتب قيمة.
5. في الحقل **الهيئة‬**، حدد هيئة ضريبة المبيعات التي تستلم التقارير والمدفوعات التي يتم إنشاؤها لفترة التسوية.
6. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
7. في حقل **شروط الدفع**، حدد السجل المطلوب في القائمة المنسدلة. يمكن إعداد هيئة ضريبة المبيعات ذات الصلة كمورّد، وستنشئ تسوية ضريبة المبيعات فاتورة مورّد مفتوحة. تحدد شروط الدفع تاريخ الاستحقاق الخاص بفاتورة المورّد المفتوحة.  
8. حدد نوعًا للفترات الزمنية للتسوية.
9. أدخل عدد وحدات الفترة الزمنية لكل فترة. على سبيل المثال، يتكون ربع السنة من 3 أشهر.
10. حدد خانة الاختيار **استخدم معالجة الدُفعة لتسوية ضريبة المبيعات‬** أو قم بإلغاء تحديدها. يمكن معالجة عملية التسوية لفترة التسوية كوظيفة دفعية في الخلفية. ينصح بهذا الأمر لعدد كبير من حركات ضريبة ضمن فترة زمنية.  
    > [!NOTE]
    > في الوقت الحالي، هذا الخيار غير معتمد في أسبانيا واليابان وهولندا.
11. حدد خانة الاختيار **منع إنشاء حركات الضرائب المقابلة‬** أو قم بإلغاء تحديدها. بشكل افتراضي، يقوم النظام بإنشاء حركات الضرائب المقابلة‬ خلال عملية التسوية، مما يؤدي إلى حدوث مشكلات في الأداء في حال وجود عدد كبير من حركات الضريبة خلال فترة زمنية. حدد خانة الاختيار لمنع إنشاء حركات الضرائب المقابلة.
12. وسّع علامة التبويب **الفترات الزمنية**.
13. حدد **إضافة**.
14. أدخل تاريخًا في الحقل **من تاريخ**.
15. في الحقل **إلى تاريخ**، أدخل تاريخًا.
16. حدد **الفترة الزمنية الجديدة**. بمجرد إدخال الفترة الزمنية الأولى، يمكن إنشاء فترات جديدة تلقائيًا. ويمكنك العودة وإضافة فترات زمنية جديدة كما هو مطلوب.  
17. قم بإغلاق الصفحة.
