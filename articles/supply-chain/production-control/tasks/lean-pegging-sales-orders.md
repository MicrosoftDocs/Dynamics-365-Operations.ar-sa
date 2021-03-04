---
title: تثبيت السعر محدود الفاقد من أوامر المبيعات
description: يركز هذا الإجراء على التحقق من صحة شجرة تثبيت السعر من سطر المبيعات حيثما يتم إنتاج الصنف بحلول كانبان.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e429fef6101f611d7a2c1b5323d6fe1e39d1cdd3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421335"
---
# <a name="lean-pegging-from-sales-orders"></a>تثبيت السعر محدود الفاقد من أوامر المبيعات

[!include [banner](../../includes/banner.md)]

يركز هذا الإجراء على التحقق من صحة شجرة تثبيت السعر من سطر المبيعات حيثما يتم إنتاج الصنف بحلول كانبان. بعد التحقق من صحة شجرة تثبيت السعر، يتم تخطيط كافة وظائف كانبان. وهذا مفيد لسيناريوهات الطلبات حيث يحتاج متلقي الطلب إلى التأكد من أنه يمكن بدء الإنتاج على الفور. شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF. ويُعد هذا الإجراء مخصصًا لمتلقي الطلب المتقدم في شركة lean.


## <a name="create-a-sales-order-for-a-kanban-controlled-item"></a>إنشاء أمر مبيعات لعنصر التحكم في كانبان
1. انتقل إلى "كافة أوامر المبيعات‬".
2. انقر فوق "جديد".
3. في الحقل "حساب العميل"، أدخل قيمة أو حددها.
    * استخدم US-001.  
4. انقر فوق "موافق".
5. في الحقل "رقم الصنف، اكتب "L0001".
6. تعيين الكمية إلى "30".
    * من المهم أن تكون الكمية أكبر من 24 من أجل تشغيل قاعدة كانبان الحدث.  

## <a name="open-a-pegging-tree"></a>فتح شجرة تثبيت السعر 
1. انقر فوق "المنتج والتوريد".
2. انقر فوق "عرض شجرة تثبيت السعر".
    * لاحظ أن شجرة تثبيت السعر توضح كافة مستويات تثبيت السعر المطلوبة لسطر أمر المبيعات. في هذه الحالة، هناك مستويان من كانبان وكافة المكونات المطلوبة.  

## <a name="plan-the-pegging-tree"></a>تخطيط شجرة تثبيت السعر
1. في الشجرة، حدد "سطر المبيعات 000832\Kanban 000558".
2. قم بتوسيع قسم "وظائف كانبان".
    * لاحظ أنه لم يتم تخطيط حالة الوظيفة لوظيفة كانبان.  
3. انقر فوق تخطيط شجرة تثبيت السعر بالكامل.
    * وهذا سيقوم بتخطيط كافة وظائف كانبان في شجرة تثبيت السعر، وتغيير حالة الوظيفة من غير مخططة إلى مخططة.  
4. قم بتحديث الصفحة.
    * لاحظ أنه تم تغيير حالة وظيفة كانبان من غير مخططة إلى مخططة.  
5. في الشجرة، حدد "سطر المبيعات 000832\Kanban 000558\Issue لـ L0001\Kanban 000559".
    * كما تم تخطيط الوظيفة لكانبان الثاني، لأنه تم تخطيط شجرة تثبيت السعر بالكامل. لاحظ أنه تم تغيير حالة وظيفة كانبان من غير مخططة إلى مخططة.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]