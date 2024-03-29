---
title: إنشاء قاعدة كانبان لحدث المبيعات
description: يركز هذا الإجراء على الإعداد المطلوب لإنشاء قاعدة كانبان يتم تشغيلها أثناء إنشاء أمر مبيعات.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3cd2b579e542b9f905fc51b63f2120e5a5c883ae
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566637"
---
# <a name="create-a-sales-event-kanban-rule"></a>إنشاء قاعدة كانبان لحدث المبيعات

[!include [banner](../../includes/banner.md)]

يركز هذا الإجراء على الإعداد المطلوب لإنشاء قاعدة كانبان يتم تشغيلها أثناء إنشاء أمر مبيعات. تزود قاعدة كانبان الخاصة بالحدث المتطلبات التي تنشأ من بنود أمر المبيعات. شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF. هذا الإجراء مخصص لمهندس العمليات أو مدير تدفق القيم عند تحضيرهم لإنتاج منتج جديد أو معدل.




## <a name="create-a-new-kanban-rule"></a>إنشاء قاعدة كانبان جديدة
1. انتقل إلى قواعد كانبان.
2. انقر فوق "جديد".
3. في الحقل "إستراتيجية التزويد"، حدد "الحدث".
    * يعني تحديد الحدث تشغيل قاعدة كانبان بواسطة الحدث، على سبيل المثال، إنشاء بند أمر مبيعات.   يتم تطبيق هذا على المناطق التي يجب أن يغطي كل كانبان طلب محدد.  
4. في الحقل "نشاط الخطة الأول"، أدخل قيمة أو حددها.
    * حدد "التجميع النهائي".  
5. قم بتوسيع القسم "التفاصيل".
6. في الحقل "المنتج"، أدخل قيمة أو حددها.
    * حدد "L0050".  

## <a name="define-an-event"></a>تحديد حدث
1. قم بتوسيع القسم "الأحداث".
2. في الحقل "حدث المبيعات"، حدد "تلقائي".
    * بتحديد "تلقائي" لحدث المبيعات، سيتم تشغيل قاعدة كانبان هذه تلقائياً عندما يطابق بند مبيعات المنتج وموقع الاستلام. في هذا الإجراء، يُستخدم المنتج L0050 بالمستودع 13.  
3. قم بتعيين الحد الأدنى لكمية الحدث على "50".
    * بتعيين الحد الأدنى 50 لكمية الحدث، لن يتم تشغيل قاعدة كانبان إلا بواسطة الأحداث التي تكون كميتها 50 أو أكثر.  
4. قم بتوسيع القسم "تدفق الإنتاج".
    * لاحظ أن موقع الاستلام هو المستودع 13. وهذا يعني أنه سيتم تشغيل قاعدة كانبان هذه لهذا الموقع.  
    * في هذا المثال، سيشغل بند مبيعات للمنتج L0050، بكمية 50 أو أكثر في المستودع 13، قاعدة كانبان هذه.  

## <a name="create-sales-line-to-trigger-event-kanban-rule"></a>إنشاء بند مبيعات لتشغيل قاعدة كانبان خاصة بحدث
1. انتقل إلى "كافة أوامر المبيعات‬".
    * يتم عرض تحذير عند حفظ قاعدة كانبان، وهو ما يعني أنه سيتم إنشاء كانبان في الوقت الفعلي أثناء إنشاء أمر مبيعات.  
2. انقر فوق "جديد".
3. في الحقل "حساب العميل"، أدخل قيمة أو حددها.
    * على سبيل المثال، حدد "الولايات المتحدة-003".  
4. انقر فوق "موافق".
5. في الحقل "رقم الصنف، اكتب "L0050".
6. في الحقل "الموقع"، اكتب ''1".
    * حدد "الموقع 1" لأن المستودع 13 موجود بالموقع 1.  
7. في الحقل "المستودع"، أدخل قيمة أو حددها.
    * قم بتعيين المستودع على 13.  
8. تعيين الكمية إلى "75".
    * أدخل كمية 50 أو أكثر، لتشغيل قاعدة كانبان التي تم إنشاؤها.  

## <a name="verify-that-kanban-is-created"></a>التحقق من إنشاء تلك الكانبان
1. انقر فوق "المنتج والتوريد".
2. انقر فوق "عرض شجرة تثبيت السعر".
    * لاحظ أنه يتم إنشاء كانبان بنفس الكمية كبند المبيعات. ويمكنك أيضًا مشاهدة إصدارات المواد اللازمة لإنتاج L0050. وهذه هي الخطوة الأخيرة في هذا الإجراء.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]