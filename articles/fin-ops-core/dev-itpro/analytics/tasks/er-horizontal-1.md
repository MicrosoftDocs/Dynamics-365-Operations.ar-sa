---
title: التقارير الإلكترونية - استخدام النطاقات القابلة للتوسيع أفقيًا لإضافة الأعمدة بشكل حيوي في تقارير Excel (الجزء 1 - تصميم التنسيق)
description: توضح هذه المقالة كيفية تكوين تنسيق إعداد التقارير الإلكترونية (ER) لإنشاء أوراق عمل OPENXML بملفات (Excel). (جزء 1)
author: kfend
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
ms.openlocfilehash: 3fa8dcac309220d05225e87fd29ef6b741bfcc54
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290413"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-1---design-format"></a>التقارير الإلكترونية - استخدام النطاقات القابلة للتوسيع أفقيًا لإضافة الأعمدة بشكل حيوي في تقارير Excel (الجزء 1 - تصميم التنسيق)

[!include [banner](../../includes/banner.md)]

تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق التقارير الإلكترونية لإنشاء التقارير كملفات أوراق عمل (Excel) تنسيق OPENXML حيث يمكن إنشاء الأعمدة المطلوبة بطريقة ديناميكية كنطاقات قابلة للتوسيع أفقيًا. يمكن تنفيذ هذه الخطوات في أي شركة.

لإكمال هذه الخطوات، يجب عليك أولاً إكمال خطوط دلائل المهام الثلاث التالية:

"التقارير الإلكترونية- إنشاء موفر تكوين ووضع علامة عليه على أنه نشط"

"التقارير الإلكترونية - استخدام الأبعاد المالية كمصدر بيانات (الجزء 1 - تصميم نموذج البيانات):

"التقارير الإلكترونية - استخدام الأبعاد المالية كمصدر بيانات (الجزء 2 - تعيين النموذج)"

يجب أيضًا تنزيل نسخة محلية من القالب وحفظها مع نموذج التقرير الموجود هنا، [عينة تقرير خدمة ويب للأبعاد المالية](https://download.microsoft.com/download/3/1/3/313e2090-bc0a-421f-bf96-c58da9bc0dea/SampleFinDimWsReport.xlsx).

يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.

## <a name="create-a-new-report-configuration"></a>إنشاء تكوين تقرير جديد

1. انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.
2. في الشجرة، حدد `Financial dimensions sample model`.
3. انقر فوق "إنشاء تكوين" لفتح مربع حوار الإسقاط‬.
4. في الحقل "جديد"، أدخل `Format based on data model Financial dimensions sample model`.
    * استخدم النموذج الذي تم إنشاؤه مسبقًا كمصدر بيانات للتقرير الجديد.  
5. في حقل الاسم، اكتب`Sample report with horizontally expandable ranges`.
    * نموذج تقرير مع نطاقات قابلة للتوسيع أفقيًا  
6. في حقل "الوصف"، اكتب `To make Excel output with dynamically adding columns`.
    * لإنشاء مخرجات Excel من خلال إضافة الأعمدة بشكل حيوي  
7. في الحقل "تعريف نموذج البيانات"، حدد "الإدخال".
8. وانقر فوق إنشاء تكوين.

## <a name="design-the-report-format"></a>تصميم تنسيق التقرير

1. انقر فوق المصمم.
2. قم بتشغيل زر التبديل `Show details`.
3. في جزء الإجراءات، انقر فوق "استيراد".
4. انقر فوق استيراد من "Excel".
5. انقر فوق "المرفقات".
    * استورد قالب التقرير. استخدم ملف Excel الذي قمت بتحميله لذلك.  
6. انقر فوق جديد.
7. انقر فوق "ملف".
8. قم بإغلاق الصفحة.
9. في حقل "القالب"، أدخل قيمة أو حددها.
    * حدد القالب الذي تم تنزيله.  
10. انقر فوق "موافق".
    * أضف مجموعة جديدة لإنشاء مخرجات Excel بطريقة ديناميكية باستخدام العدد الذي حددته من الأعمدة (في نموذج حوار المستخدم) للأبعاد المالية. ستمثل كل خلية لكل عمود اسم بُعد مالي واحد.  
11. انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.
12. في الشجرة، حدد `Excel\Range`.
13. في الحقل "نطاق Excel"، اكتب `DimNames`.
    * DimNames  
14. في الحقل "اتجاه النسخ المتماثل"، حدد `Horizontal`.
15. انقر فوق موافق.
16. في الشجرة، حدد `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal`.
17. انقر فوق "تحريك لأعلى".
18. في الشجرة، حدد `Excel = "SampleFinDimWsReport"\Cell<DimNames>`.
19. انقر فوق "قص".
20. في الشجرة، حدد `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal`.
21. انقر فوق "لصق".
22. في الشجرة، قم بتوسيع `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal`.
23. في الشجرة، قم بتوسيع `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical`.
24. في الشجرة، قم بتوسيع `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical`.
25. في الشجرة، حدد `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical`.
    * أضف مجموعة جديدة لإنشاء مخرجات Excel بطريقة ديناميكية باستخدام العدد الذي حددته من الأعمدة (في نموذج حوار المستخدم) للأبعاد المالية. ستمثل كل خلية لكل عمود قيمة بُعد مالي واحدة لكل حركة تقرير.  
26. انقر فوق "إضافة نطاق".
27. في الحقل "نطاق Excel"، اكتب `DimValues`.
    * DimValues  
28. في الحقل "اتجاه النسخ المتماثل"، حدد `Horizontal`.
29. انقر فوق موافق.
30. في الشجرة، حدد `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>`.
31. انقر فوق "قص".
32. في الشجرة، حدد `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal`.
33. انقر فوق "لصق".
34. في الشجرة، قم بتوسيع `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal`.

## <a name="map-format-elements-to-data-sources"></a>تعيين عناصر التنسيق إلى مصادر بيانات

1. انقر فوق علامة التبويب "التعيين".
2. في الشجرة، قم بتوسيع `model: Data model Financial dimensions sample model`.
3. في الشجرة، قم بتوسيع `model: Data model Financial dimensions sample model\Journal: Record list`.
4. في الشجرة، قم بتوسيع `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list`.
5. في الشجرة، قم بتوسيع `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list`.
6. في الشجرة، حدد `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>`.
7. في الشجرة، حدد `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String`.
8. انقر فوق "ربط".
9. في الشجرة، حدد `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal`.
10. في الشجرة، حدد `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list`.
11. انقر فوق "ربط".
12. في الشجرة، حدد `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>`.
13. في الشجرة، حدد `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real`.
14. انقر فوق "ربط".
15. في الشجرة، حدد `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>`.
16. في الشجرة، حدد `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real`.
17. انقر فوق "ربط".
18. في الشجرة، حدد `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>`.
19. في الشجرة، حدد `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String`.
20. انقر فوق "ربط".
21. في الشجرة، حدد `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>`.
22. في الشجرة، حدد `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date`.
23. انقر فوق "ربط".
24. في الشجرة، حدد `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>`.
25. في الشجرة، حدد `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String`.
26. انقر فوق "ربط".
27. في الشجرة، حدد `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>`.
28. في الشجرة، حدد `model: Data model Financial dimensions sample model\Journal: Record list\Batch: String`.
29. انقر فوق "ربط".
30. في الشجرة، حدد `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical`.
31. في الشجرة، حدد `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list`.
32. انقر فوق "ربط".
33. في الشجرة، حدد `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>`.
34. في الشجرة، حدد `model: Data model Financial dimensions sample model\Journal: Record list\Batch: String`.
35. انقر فوق "ربط".
36. في الشجرة، حدد `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical`.
37. في الشجرة، حدد `model: Data model Financial dimensions sample model\Journal: Record list`.
38. انقر فوق "ربط".
39. في الشجرة، قم بتوسيع `model: Data model Financial dimensions sample model\Dimensions setting: Record list`.
40. في الشجرة، حدد `model: Data model Financial dimensions sample model\Dimensions setting: Record list\Code: String`.
41. في الشجرة، حدد `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>`.
42. انقر فوق "ربط".
43. في الشجرة، حدد `model: Data model Financial dimensions sample model\Dimensions setting: Record list`.
44. في الشجرة، حدد `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal`.
45. انقر فوق "ربط".
46. في الشجرة، حدد `Excel = "SampleFinDimWsReport"\Cell<CompanyName>`.
47. في الشجرة، حدد `model: Data model Financial dimensions sample model\Company: String`.
48. انقر فوق "ربط".
49. انقر فوق حفظ.
50. قم بإغلاق الصفحة.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
