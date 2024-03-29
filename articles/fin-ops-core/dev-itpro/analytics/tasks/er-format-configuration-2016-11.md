---
title: التقارير الإلكترونية - إنشاء تكوين تنسيق (نوفمبر 2016)
description: توضح هذه المقالة كيفية إنشاء تكوين تنسيق للتقارير الإلكترونية (ER).
author: kfend
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
ms.openlocfilehash: 3c705add64a46c4cce5127f16fae45edba1bc001
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290713"
---
# <a name="er-create-a-format-configuration-november-2016"></a>التقارير الإلكترونية - إنشاء تكوين تنسيق (نوفمبر 2016)

[!include [banner](../../includes/banner.md)]

تشرح هذه المقالة كيف يمكن لمستخدم يؤدي دور مسؤول النظام أو مطور التقارير الإلكترونية إنشاء تكوين تنسيق لإنشاء التقارير الإلكترونية (ER). وسيحدد هذا التكوين تنسيق المستندات الإلكترونية المستخدمة لمعالجة المدفوعات. في هذا المثال، ستقوم بإنشاء تكوين تنسيق لشركة عينة، .Litware, Inc. ولإكمال هذه الخطوات، يجب عليك أولاً إكمال الخطوات المذكورة في الإجراء "تعيين النموذج لمصادر البيانات المحددة".


## <a name="create-a-new-format-configuration"></a>قم بإنشاء تكوين تنسيق جديد
1. انتقل إلى **إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني**‬.
2. انقر فوق **تكوينات إعداد التقارير‬**.
3. في الشجرة، حدد **المدفوعات (نموذج مبسط)**.
4. انقر فوق **إنشاء تكوين** لفتح مربع حوار الإسقاط‬.

 > [!NOTE]
 > إذا لم يظهر الخيار **إنشاء تكوين**، فعليك تكوين وضع التصميم في صفحة **معلمات ‏‫إعداد التقارير الإلكترونية**. 
 
5. في الحقل **جديد**، أدخل **التنسيق استناداً إلى نموذج الدفع الخاص بنموذج البيانات**.
6. في الحقل **الاسم**، اكتب **BACS (وهمية من المملكة المتحدة)**.
7. في حقل **الوصف**، اكتب **تنسيق دفع المورد BACS (وهمية من المملكة المتحدة)**.
    * يتم تلقائيًا إدخال موفر التكوين النشط هنا. سيكون هذا الموفر قادرًا على المحافظة على هذا التكوين. باستطاعة موفرين آخرين استخدام هذا التكوين، ولكن لن يكون باستطاعتهم المحافظة عليه.  
    * يمكن تعريف تنسيق معين لوثيقة إلكترونية. اترك هذا الحقل فارغاً إذا كنت تريد تحديد تنسيق في وقت التشغيل.  
8. في الحقل **تعريف نموذج البيانات**، أدخل قيمة أو حددها.
9. وانقر فوق **إنشاء تكوين**. تم إنشاء تكوين جديد. يمكن استخدام الإصدار التمهيدي لتخزين تنسيق التصميم لإدارة الوثائق الإلكترونية.  

## <a name="design-the-format-of-an-electronic-document"></a>تصميم تنسيق مستند إلكتروني
1. انقر فوق **المصمم**.
2. انقر فوق **إضافة جذر** لفتح مربع حوار الإسقاط‬.
3. في الشجرة، حدد **Common\File**.
4. في حقل **الاسم**، اكتب **Xml**.
5. في حقل **الترميز**، اكتب **UTF-8**.
6. وانقر فوق **موافق**.
7. النقر فوق **إضافة**.
8. في الشجرة، **XML\العنصر**.
9. في الحقل **الاسم**، اكتب **رسالة**.
10. وانقر فوق **موافق**.
11. في الشجرة، حدد **Xml\الرسالة**.
12. انقر فوق **إضافة عنصر**.
13. في حقل **الاسم**، اكتب **تاريخ المعالجة**.
14. وانقر فوق **موافق**.
15. انقر فوق **إضافة عنصر**.
16. في حقل الاسم، اكتب **MessageId**.
17. وانقر فوق **موافق**.
18. انقر فوق **إضافة عنصر**.
19. في حقل **الاسم**، اكتب **دفعات**.
20. وانقر فوق **موافق**.
21. في الشجرة، حدد **Xml\الرسالة\المدفوعات**.
22. انقر فوق **إضافة عنصر**.
23. في الحقل **الاسم**، اكتب **الصنف**.
24. وانقر فوق **موافق**.
25. في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف**.
26. النقر فوق **إضافة**.
27. في الشجرة، حدد **XML\سمة**.
28. في حقل الاسم، اكتب **المعرف**.
29. وانقر فوق **موافق**.
30. النقر فوق **إضافة**.
31. في الشجرة، **XML\العنصر**.
32. في حقل الاسم، اكتب **المورّد**.
33. وانقر فوق **موافق**.
34. في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\المورّد**.
35. انقر فوق **إضافة عنصر**.
36. في الحقل "الاسم"، اكتب **الاسم**.
37. وانقر فوق **موافق**.
38. انقر فوق **إضافة عنصر**.
39. في الحقل **الاسم**، اكتب **البنك**.
40. وانقر فوق **موافق**.
41. في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\المورّد\البنك**.
42. انقر فوق **إضافة عنصر**.
43. في الحقل **الاسم**، اكتب **RoutingNumber**.
44. وانقر فوق **موافق**.
45. انقر فوق **إضافة عنصر**.
46. في الحقل **الاسم**، اكتب **AccountNumber**.
47. وانقر فوق **موافق**.
48. في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\المورّد**.
49. انقر فوق **نسخ**.
50. في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف**.
51. انقر فوق **لصق**.
52. في الحقل **الاسم**، اكتب **الممول‬**.
53. في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف**.
54. انقر فوق **إضافة عنصر**.
55. في الحقل **الاسم**، اكتب **العملة**.
56. وانقر فوق **موافق**.
57. انقر فوق **إضافة عنصر**.
58. في الحقل **الاسم**، اكتب **الوصف**.
59. وانقر فوق **موافق**.
60. انقر فوق **إضافة عنصر**.
61. في الحقل "الاسم"، اكتب **TransDate**.
62. وانقر فوق **موافق**.
63. انقر فوق **إضافة عنصر**.
64. في الحقل "الاسم"، اكتب **المبلغ**.
65. وانقر فوق **موافق**.

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a>إعداد مكونات التنسيق لتعيينها لعناصر نماذج البيانات
1. في الشجرة، حدد **Xml\الرسالة\ProcessingDate**.
2. انقر فوق **إضافة** لفتح مربع حوار الإسقاط.
3. في الشجرة، حدد **النص\DateTime**.
4. في الحقل **التنسيق**، اكتب **yyyy-MM-dd**.
5. وانقر فوق **موافق**.
6. في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\TransDate**.
7. انقر فوق **إضافة التاريخ والوقت**.
8. في الحقل **التنسيق**، اكتب **yyyy-MM-dd**.
9. في الحقل نوع **التاريخ والوقت**، حدد **التاريخ**.
10. وانقر فوق **موافق**.
11. في الشجرة، حدد **Xml\الرسالة\MessageId**.
12. انقر فوق **إضافة** لفتح مربع حوار الإسقاط.
13. في الشجرة، حدد **نص\سلسلة**.
14. وانقر فوق **موافق**.
15. في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\المورّد\الاسم**.
16. انقر فوق **إضافة سلسلة**.
17. وانقر فوق **موافق**.
18. في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\المورّد\البنك\RoutingNumber**.
19. انقر فوق **إضافة سلسلة**.
20. وانقر فوق **موافق**.
21. في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\المورّد\البنك\AccountNumber**.
22. انقر فوق **إضافة سلسلة**.
23. وانقر فوق **موافق**.
24. في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\الممول\الاسم**.
25. انقر فوق **إضافة سلسلة**.
26. وانقر فوق **موافق**.
27. في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\الممول\البنك\RoutingNumber**.
28. انقر فوق **إضافة سلسلة**.
29. وانقر فوق **موافق**.
30. في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\الممول\البنك\AccountNumber**.
31. انقر فوق **إضافة سلسلة**.
32. وانقر فوق **موافق**.
33. في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\العملة**.
34. انقر فوق **إضافة سلسلة**.
35. وانقر فوق **موافق**.
36. في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\الوصف**.
37. انقر فوق **إضافة سلسلة**.
38. وانقر فوق **موافق**.
39. في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\المبلغ**.‬
40. انقر فوق **إضافة سلسلة**.
41. وانقر فوق **موافق**.
42. انقر فوق **حفظ**.
43. قم بإغلاق الصفحة.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
