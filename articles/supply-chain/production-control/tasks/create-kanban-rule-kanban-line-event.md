---
title: إنشاء قاعدة كانبان باستخدام حدث بند كانبان
description: ينشئ هذا الإجراء قاعدة كانبان باستخدام إعداد حدث بند كانبان للضغط على المشغّل من نشاط معالجة.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7aaf959db0f0a136fc615f9a57ec787ef6cf2ad
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579150"
---
# <a name="create-a-kanban-rule-using-a-kanban-line-event"></a>إنشاء قاعدة كانبان باستخدام حدث بند كانبان

[!include [banner](../../includes/banner.md)]

ينشئ هذا الإجراء قاعدة كانبان باستخدام إعداد حدث بند كانبان للضغط على المشغّل من نشاط معالجة. يتم تشغيل قاعدة كانبان بواسطة نشاط معالجة كانبان، مع كمية مساوية لـ 25 أو أكبر من 25 لكل منها. شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USMF.‬ هذه المهمة مخصصة لمهندس العمليات أو مدير تدفق القيم عند قيامه بتحضير عملية إنتاج منتج جديد أو معدل في بيئة محدودة.


## <a name="create-a-kanban-rule"></a>إنشاء قاعدة كانبان
1. انتقل إلى إدارة معلومات المنتج‬ > خلية عمل Lean manufacturing > قواعد كنبان.
2. انقر فوق "جديد".
3. في الحقل "إستراتيجية التزويد"، حدد "الحدث".
    * يؤدي ذلك إلى إنشاء كانبان من الطلب مباشرة. ويتم استخدامه لتعيين القواعد التي تحدد سيناريو إدراج في الأمر.  
4. في الحقل "نشاط الخطة الأول"، أدخل قيمة أو حددها.
    * أدخل SpeakerAssemblyAndPolish أو حدده. يجب أن يكون النشاط الأول لقاعدة كانبان للتصنيع عبارة عن نشاط معالجة في تدفق الإنتاج. عندما تحدد النشاط، يتم نسخ تواريخ صلاحية النشاط إلى تواريخ صلاحية قاعدة كانبان.  
5. قم بتوسيع القسم "التفاصيل".
6. في حقل "المنتج"، اكتب "L0001".
7. قم بتوسيع القسم "الأحداث".
8. في الحقل "حدث سطر كانبان"، حدد "تلقائي".
    * يؤدي ذلك إلى إنشاء كانبان الحدث عند الطلب.  يُستخدم الحقل لتكوين قواعد كانبان التي تزود المواد المطلوبة لنشاط عملية نهائية. عند تحديد "تلقائي"، يتم إنشاء كانبان الحدث مع الطلب. يوصي بهذا الإعداد إذا كنت تتوقع تنفيذ الإنتاج في نفس اليوم.  
9. قم بتعيين الحد الأدنى لكمية الحدث على "25".
    * يتم إنشاء كانبان الأحداث عندما تكون كمية الطلب مساوية لهذا الحقل أو أكبر منه. يُعد ذلك مفيدًا إذا كنت تريد إنتاج كمية طلب أقل من هذا الحقل على جهاز وكمية أكبر من هذا الحقل على جهاز آخر.  
10. انقر فوق "حفظ".

## <a name="create-sales-order-and-trigger-kanban-chain"></a>إنشاء أمر مبيعات وتشغيل سلسلة كانبان
1. انتقل إلى المبيعات والتسويق > أوامر المبيعات > كافة أوامر المبيعات.
2. انقر فوق "جديد".
3. في الحقل "حساب العميل"، أدخل قيمة أو حددها.
    * حدد حساب العميل US-003, Forest Wholesales.  
4. انقر فوق "موافق".
5. في الحقل "رقم الصنف، اكتب "L0001".
    * L0001 هو الصنف الذي قمت بإنشاء قاعدة كانبان له.  
6. تعيين الكمية إلى "27".
    * لأن 27 أكبر من الحد الأدنى للكمية 25 في قاعدة كانبان، سيؤدي ذلك إلى تشغيل كانبان حدث.  
7. في الحقل "الموقع"، اكتب ''1".
8. في الحقل "المستودع"، أدخل قيمة أو حددها.
    * حديد المستودع 13.  
9. انقر فوق "حفظ".

## <a name="view-the-kanban-generated-by-the-kanban-rule"></a>عرض كانبان الذي تم إنشاؤه باستخدام قاعدة كانبان
1. انتقل إلى إدارة معلومات المنتج‬ > خلية عمل Lean manufacturing > قواعد كنبان.
2. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
3. قم بتوسيع القسم "كانبان".
    * لاحظ أنه قد تم إنشاء كانبان لـ 27 لمعالجة النشاط استنادًا إلى قاعدة كانبان التي تم إنشاؤها.  
    * هذه هي الخطوة الأخيرة.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]