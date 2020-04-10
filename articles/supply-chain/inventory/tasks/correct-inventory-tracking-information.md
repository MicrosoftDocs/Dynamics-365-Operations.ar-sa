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
ms.openlocfilehash: 5155ada23fe4f559c79964e6bd10d86712009d1d
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145748"
---
# <a name="correct-inventory-tracking-information"></a>تصحيح معلومات تعقب المخزون

[!include [banner](../../includes/banner.md)]

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

