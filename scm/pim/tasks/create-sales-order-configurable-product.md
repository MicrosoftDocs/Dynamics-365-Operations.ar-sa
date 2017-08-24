--- 
title: "إنشاء أمر مبيعات لمنتج قابل للتكوين"
description: "يوضح هذا الإجراء كيفية تطبيق قالب تكوين على منتج في أمر مبيعات."
author: BibiSp
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bibis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 6546d504a2fda255cb5183408dfe84a3074543ab
ms.contentlocale: ar-sa
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-sales-order-for-a-configurable-product"></a>إنشاء أمر مبيعات لمنتج قابل للتكوين

[!include[task guide banner](../../includes/task-guide-banner.md)]

يوضح هذا الإجراء كيفية تطبيق قالب تكوين على منتج في أمر مبيعات. يستخدم هذا المثال نموذج مكبر الصوت المتطور D0006 في شركة بيانات العرض التوضيحي USMF. يستخدم معالج أمر المبيعات عادةً هذا الإجراء.


## <a name="create-a-sales-order"></a>إنشاء أمر مبيعات
1. انقر فوق "الاستعلام عن أمر المبيعات ومعالجته‬".
2. انقر فوق "جديد".
3. انقر فوق "أمر المبيعات".
4. في حقل "حساب العميل"، حدد US-001. 
5. انقر فوق "موافق".
6. في حقل "رقم الصنف"، حدد D0006.
    * لتنفيذ هذه المهمة، يجب تحديد منتج قابل للتكوين.  
7. انقر فوق "المنتج والتوريد".
8. انقر فوق تكوين البند.
    * لاحظ أن السعر قد تغيّر، استنادًا إلى التكوين الذي تم تحديده، وأن الحقل "تضمين الكبل" أصبح الآن معينًا إلى True.  
    * لاحظ أنه تم تحديد السعر الافتراضي والإعدادات للكبل.  
9. انقر فوق تحميل القالب.
    * يوضح هذا المثال كيفية تطبيق قالب لتحديد تكوين معرّف مسبقًا. إذا كنت تستخدم هذا الإجراء كدليل مهمة وأردت رؤية قيم السمات الأخرى المتوفرة، فيجب النقر فوق الزر "إلغاء التأمين".  
10. انقر فوق "موافق".
11. انقر فوق "موافق".
12. قم بتوسيع قسم "تفاصيل البند".
13. انقر فوق علامة التبويب "المنتج".
    * تم الآن إدراج تكوين الصنف ضمن أبعاد المنتج.  
14. قم بإغلاق الصفحة.

## <a name="select-the-product-configuration"></a>تحديد تكوين المنتج


