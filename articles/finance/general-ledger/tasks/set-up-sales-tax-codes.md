---
title: إعداد أكواد ضريبة المبيعات
description: توضح هذه المقالة كيفية إعداد ‏‫أكواد ضريبة المبيعات‬ في Dynamics 365 Finance.
author: twheeloc
ms.date: 09/27/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b12133583f40cc17cb85f6dbd86697592af25caf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858457"
---
# <a name="set-up-sales-tax-codes"></a>إعداد أكواد ضريبة المبيعات

[!include [banner](../../includes/banner.md)]

توضح هذه المقالة كيفية إعداد ‏‫أكواد ضريبة المبيعات‬. يتم إنشاء أكواد ضريبة المبيعات لكل ضريبة أو رسم غير مباشر يلزم على الكيان القانوني حسابه وتحصيله ودفعه لهيئات ضريبة المبيعات.

تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.

1. انتقل إلى **جزء التنقل > الضريبة > الضرائب غير المباشرة > ضريبة المبيعات > أكواد ضريبة المبيعات**.
2. حدد **جديد**.
3. في الحقل **كود ضريبة المبيعات**، اكتب قيمة.
4. في الحقل **الاسم**، اكتب قيمة.
5. حدد **فترة تسوية** عن طريق فتح القائمة المنسدلة لتحديد هيئة ضريبة المبيعات حيث يجب الإبلاغ عن ضريبة المبيعات ودفعها ولتحديد الفترات الزمنية للإبلاغ والدفع.
6. حدد **مجموعة ترحيل دفتر أستاذ** لتحديد الحسابات الرئيسية لترحيل ضريبة المبيعات إلى دفتر الأستاذ العام.
7. وسّع علامة التبويب السريعة **الحساب**. تتضمن هذه حقولاً متعددة تتحكم في كيفية حساب مبالغ ضريبة المبيعات. إملأ هذه الحقول حسب الحاجة.  
8. في **جزء الإجراءات** في أعلى الواجهة، حدد **كود ضريبة المبيعات**.
9. حدد **القيم**.
10. أدخل قيمة كود الضريبة هذا في عمود **القيمة**.

    على علامة التبويب السريعة **الحساب** ـ في الحقل **الأصل**، إذا تم تحديد **المبلغ لكل وحدة‬** فسيتم ضرب القيمة في الكمية على الحركة لحساب مبلغ ضريبة المبيعات.  إذا لم يكن كود الضريبة عبارة عن ضريبة تستند إلى وحدة، فستكون القيمة عبارة عن نسبة مئوية مطبقة على الأصل لكود الضريبة هذا لحساب مبلغ ضريبة المبيعات.     

11. حدد **حفظ**.
12. قم بإغلاق الصفحة.
13. حدد **حفظ**.

اعتبارًا من الإصدار 10.0.22 من 365 Finance Microsoft Dynamics، إذا كنت تستخدم [خدمة الضريبة](../../localizations/global-tax-calcuation-service-overview.md)، وتم تمكين الميزة [**دعم أرقام تسجيل ضريبة القيمة المضافة المتعددة‬**](../../localizations/emea-multiple-vat-registration-numbers.md) في **إدارة الميزات**، فيمكنك استخدام **نوع الضريبة** لتحديد نوع كود الضريبة. تتوفر القيم التالية:

- ضريبة قيمة مضافة قياسية
- ضريبة القيمة المضافة المخفضة
- ضريبة القيمة المضافة 0%
- العوائد
- أخرى

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
