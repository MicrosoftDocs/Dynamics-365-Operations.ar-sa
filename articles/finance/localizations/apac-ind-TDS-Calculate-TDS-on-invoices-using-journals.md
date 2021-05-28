---
title: حساب TDS على الفواتير باستخدام دفاتر اليومية
description: يسرد هذا الموضوع خطوات حساب الضريبة المخصومة في المصدر (TDS) على دفاتر اليومية.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: d68e1b3a4dc31823ec56a525149f16bdc23c0883
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023012"
---
# <a name="calculate-tds-on-invoices-using-journals"></a>حساب TDS على الفواتير باستخدام دفاتر اليومية

[!include [banner](../includes/banner.md)]

يسرد هذا الموضوع خطوات حساب الضريبة المخصومة في المصدر (TDS) على دفاتر اليومية.

ابدأ بفتح الصفحة **دفاتر اليومية العامة** (**دفتر الأستاذ العام > إدخالات دفتر اليومية > دفاتر اليومية العامة**).

[![دفاتر اليومية العامة](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)

1. قم بإنشاء بنود دفتر اليومية باستخدام نماذج دفاتر اليومية التي يتم سردها في الجدول. حدد نوع الحساب ونوع الحساب المقابل، ثم أدخل مبلغ الحركة. 

   > [!NOTE]
   > في الصفحة **دفتر يومية اعتماد الفواتير**، حدد **البحث عن إيصالات** وحدد فواتير لحساب TDS بها. اعرض الفواتير التي تم إنشاؤها في الصفحة **سجل الفواتير** أو الصفحة **البحث عن إيصالات**.  

2. في علامة التبويب **عام** من الصفحة **إيصال دفتر اليومية**، قم بعرض أو تعديل مجموعة TDS الافتراضية المحددة للمورد أو العميل، في الحقل **مجموعة TDS** يعتمد مبلغ TDS الذي يتم حسابه في بنود دفتر اليومية على المعادلة المحددة لأكواد الضريبة TDS المدرجة في الحقل **مجموعة TDS**. 

   > [!NOTE]
   > لا يتوفر الحقل **مجموعة ضريبة الخصم**  والحقل **مجموعة TCS** عندما تقوم بتحديد مجموعة TDS في الحقل **مجموعة TDS**. يتوفر الحقل **مجموعة ضريبة الخصم** في الصفحة **دفتر اليومية العام** فقط. يتم حساب TDS فقط إذا تم تحديد خانة اختيار **حساب ضريبة الخصم** للمورد أو العميل في الصفحتين **جميع الموردين** أو **جميع العملاء**.   

3. حدد علامة التبويب **معلومات الضريبة**: حدد العناوين البديلة لشركة يتم إعدادها للشركة في هذا الحقل، إذا لزم الأمر. يمكنك عرض اسم الشركة في الحقل **الاسم**، الموجود ضمن مجموعة الحقل **معلومات الشركة**. 

4. تعرض طبيعة فئة المقيم للمورد أو العميل في الحقل **طبيعة حقل المقيم**، والتي توجد ضمن مجموعة الحقل **ضريبة الخصم**. في الحقل **رقم حساب الضريبة** (**TAN**)، اعرض TAN الخاص باسم الشركة المحدد الذي يتم عرضه.  

5. حدد **ضريبة الخصم** في قائمة **ضريبة الخصم** لفتح الصفحة **حركات ضريبة الخصم المؤقتة**. يتم عرض الحقول التالية في الجزء العلوي من الصفحة **حركات ضريبة الخصم المؤقتة**.

   - **إجمالي مبلغ ضريبة الخصم** - إجمالي TDS المحسوب للحركة لمجموعة TDS.

   - **القيمة** - النسبة المئوية الإجمالية المستخدمة لحساب TDS الخاصة بالحركة. يستند إجمالي النسبة المئوية إلى المعادلة التي يتم تحديدها لأكواد الضريبة TDS المرتبطة بمجموعة TDS.

   - **إجمالي مبلغ ضريبة الخصم المعدل** - إجمالي مبلغ TDS المعدل لكافة أكواد الضريبة في مجموعة TDS.

   - **TDS** - في حالة تحديده، يتم إرفاق مجموعة TDS بالحركة.

  تعرض الحقول الموجودة على علامات التبويب **نظرة عامة** و **عام** و **التعديل** في الصفحة **حركات ضريبة الخصم المؤقتة** تفاصيل مبلغ TDS المحسوب ومبلغ TDS المعدل لكل كود ضريبة TDS مرفق بالمجموعة TDS.

6. حدد **الحد** لفتح الصفجة **الحد**. اعرض الحد والحد الاستثنائي المحدد لمكون الضريبة TDS المرفق بكود ضريبة TDS محدد في هذه الصفحة.

   حدد **مصمم الصيغ** لفتح النموذج **مصمم الصيغة**. اعرض المعادلة المحددة لكود ضريبة TDS محدد في هذه الصفحة. قم بإغلاق الصفحات **مصمم المعادلة** و **حركات ضريبة الخصم المؤقتة** للرجوع إلى الصفحة **إيصال دفتر اليومية**.

8. أدخل التفاصيل الأخرى المطلوبة. تحقق من صحة دفتر اليومية وقم بترحيله. يتم ترحيل مبلغ TDS الذي يتم حسابه على فواتير الشراء إلى الحساب الدائن. يتم ترحيل مبلغ TDS الذي يتم حسابه في فواتير المبيعات إلى الحساب المدين الذي يتم تحديده لكل كود ضريبة TDS في المجموعة TDS. يتم تحديد الحسابات الدائنة أو الحسابات المدينة لأكواد ضريبة TDS في الصفحة **أكواد ضريبة الخصم**.

9. حدد **ضريبة الخصم المرحلة** لفتح الصفحة **حركات** **ضريبة** **الحركات**. في الحقل **القيمة**، يتم عرض إجمالي النسبة المئوية المستخدمة لحساب TDS للحركة.

   تعرض الحقول الموجودة على علامات التبويب **نظرة عامة** و **عام** و **مبلغ** في الصفحة حركات ضريبة الخصم المؤقتة تفاصيل مبلغ TDS المحسوب ومبلغ TDS المعدل لكل كود ضريبة TDS مرفق بالمجموعة TDS.