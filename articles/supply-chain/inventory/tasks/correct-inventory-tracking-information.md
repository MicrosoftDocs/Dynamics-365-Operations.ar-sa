---
title: تصحيح معلومات تعقب المخزون
description: يرشدك هذا الإجراء خلال عملية إنشاء وترحيل دفتر يومية تحويل المخزون من أجل تصحيح معلومات تعقب المخزون.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventBatchIdLookup, InventLocationIdLookup, InventDimTracking, InventTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8269e5119e45522373eca6cb8fb06bfb94a37566
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845560"
---
# <a name="correct-inventory-tracking-information"></a>تصحيح معلومات تعقب المخزون

[!include [task guide banner](../../includes/task-guide-banner.md)]

يرشدك هذا الإجراء خلال عملية إنشاء وترحيل دفتر يومية تحويل المخزون من أجل تصحيح معلومات تعقب المخزون. في هذا المثال، سنقوم بتحديث المعلومات من عنصر التحكم في الدفعة من خلال تغيير المجموعة المسجلة بشكل غير صحيح إلى دفعة أخرى. يمكنك استعراض هذا الإجراء في عنوان USPI بشركة بيانات العرض التوضيحي، أو باستخدام البيانات الخاصة بك. إذا كنت تستخدم البيانات الخاصة بك، فستحتاج إلى وجود عنصر تم تمكين دفعته، ويجب ألا يكون متحكمًا في موقعه. يجب أن يكون لديك أيضًا اسم دفتر يومية مخزون تم إعداده لعمليات نقل المخزون. وقد تُنفذ هذه المهام في العادة عن طريق موظف مستودع.


## <a name="create-an-inventory-transfer-journal"></a>إنشاء دفتر يومية تحويل مخزون
1. انتقل إلى "التحويل".
2. انقر فوق "جديد".
3. في الحقل "الاسم"، أدخل قيمة أو حددها.
4. انقر فوق "موافق".

## <a name="create-journal-lines"></a>إنشاء بنود دفتر اليومية
1. انقر فوق "جديد".
2. في الحقل "رقم الصنف"، أدخل قيمة أو حددها.
    * إذا كنت تستخدم USPI، فحدد الصنف M5003.  
3. في حقل الكمية، أدخل رقمًا.
4. انقر فوق علامة التبويب "أبعاد المخزون".
5. في حقل "رقم الدفعة"، أدخل قيمة أو حددها.
6. في حقل "الموقع"، أدخل قيمة أو حددها.
7. في الحقل "المستودع"، أدخل قيمة أو حددها.
8. في حقل "رقم الدفعة"، أدخل قيمة أو حددها.

## <a name="post-the-journal"></a>ترحيل دفتر اليومية
1. انقر فوق "ترحيل".
2. انقر فوق "موافق".

## <a name="check-tracing-information"></a>تحقق من معلومات التتبع
1. انقر فوق المخزون.
2. انقر فوق "تعقب".
3. انقر فوق "موافق".
    * باستخدام معلومات التتبع هذه، يمكنك إجراء التتبع الخلفي للدفعة التي قمت بتصحيح المخزون منها.  يمكنك أيضا استخدام صفحة تتبع الصنف لمشاهدة هذه المعلومات.  
4. قم بإغلاق الصفحة.

## <a name="check-inventory-transactions"></a>تحقق من حركات المخزون
1. انقر فوق المخزون.
2. انقر فوق "الحركات".
    * هنا يمكنك أن ترى الحركات التي تم إنشاؤها عندما قمت بترحيل دفتر اليومية الخاص بك.   

