---
title: إنشاء أمر مبيعات لمنتج قابل للتكوين
description: يوضح هذا الإجراء كيفية تطبيق قالب تكوين على منتج في أمر مبيعات.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 39ccb68ba76cd710412df6a46fc624608d02902b
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844527"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a>إنشاء أمر مبيعات لمنتج قابل للتكوين

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

