---
title: جدولة أمر إنتاج بواسطة جدولة العمليات وجدولة الوظائف
description: يركز هذا الموضوع على جدولة أمر إنتاج بواسطة جدولة العمليات وجدولة الوظائف.
author: ChristianRytt
manager: tfehr
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bbb4da093cd8a0fc6cd85e1f93dfb91f0fb8a382
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981121"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a>جدولة أمر إنتاج بواسطة جدولة العمليات وجدولة الوظائف

[!include [banner](../../includes/banner.md)]

يركز هذا الموضوع على جدولة أمر إنتاج بواسطة جدولة العمليات وجدولة الوظائف. لا يتم إنشاء أي وظائف بواسطة جدولة العمليات، بينما يتم إنشاء الوظائف بواسطة جدولة الوظائف. شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USMF.‬ تم تخصيص هذا الإجراء لمدير الإنتاج أو مخطط الإنتاج أو المشرف على صالة الإنتاج‬ في بيئة تصنيع منفصلة.


## <a name="create-a-production-order"></a>إنشاء أمر إنتاج
1. في جزء التنقل، انتقل إلى **الوحدات النمطية > ‏‫التحكم بالإنتاج‬ > أوامر الإنتاج > جميع أوامر الإنتاج**.
2. حدد **أمر إنتاج جديد**.
3. في الحقل **رقم الصنف**، أدخل قيمة أو حددها. حدد رقم الصنف **D0001**.  
4. حدد **إنشاء**.

## <a name="schedule-operations-for-the-production-order"></a>جدولة العمليات لأمر الإنتاج
1. ضع علامة على الصف الذي تم إنشاؤه حديثًا.      
2. في جزء الإجراءات، حدد **جدول**.
3. حدد **جدولة العمليات**.
4. في الحقل **اتجاه الجدولة**، حدد **بدءًا من تاريخ الجدولة**.
5. أدخل تاريخًا في حقل **تاريخ الجدولة**. حدد تاريخًا في المستقبل، على سبيل المثال، اليوم بالإضافة إلى أسبوع واحد. مع تحديد اتجاه الجدولة، سيتم إجراء جدولة آجلة لأمر الإنتاج من هذا التاريخ.  
6. حدد **موافق**.
7. في القائمة، قم بوضع علامة للصف المحدد. لاحظ أن الحالة تغيّرت إلى **مجدول**. 
8. حدد **كل الوظائف‬**. لاحظ أنه لم يتم إنشاء أي وظائف بواسطة جدولة العمليات.  
9. قم بإغلاق الصفحة.

## <a name="schedule-jobs-for-the-production-order"></a>جدولة المهام لأمر الإنتاج
1. في جزء الإجراءات، حدد **جدول**.
2. حدد **جدولة الوظائف**.
3. في الحقل **اتجاه الجدولة**، حدد **بدءًا من تاريخ الجدولة**.
4. أدخل تاريخًا في حقل **تاريخ الجدولة**. حدد تاريخًا في المستقبل، على سبيل المثال، اليوم بالإضافة إلى أسبوع واحد. مع تحديد اتجاه الجدولة، سيتم إجراء جدولة آجلة لأمر الإنتاج من هذا التاريخ.  
5. حدد **موافق**.
6. في جزء الإجراءات، حدد **أمر إنتاج**.
7. حدد **كل الوظائف‬**. لاحظ أنه تم إنشاء 5 وظائف بواسطة جدولة الوظائف على المسار النشط.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]