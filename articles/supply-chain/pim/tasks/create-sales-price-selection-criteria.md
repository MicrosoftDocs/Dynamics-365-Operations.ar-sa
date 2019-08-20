---
title: إنشاء معايير تحديد سعر المبيعات
description: يوضح هذا الإجراء كيفية إنشاء معيار تحديد سعر المبيعات لنماذج أسعار المبيعات التي تستند إلى سمة.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72940f719baca5e8042c2f2caa8abbacb7d8264e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844479"
---
# <a name="create-sales-price-selection-criteria"></a>إنشاء معايير تحديد سعر المبيعات

[!include [task guide banner](../../includes/task-guide-banner.md)]

يوضح هذا الإجراء كيفية إنشاء معيار تحديد سعر المبيعات لنماذج أسعار المبيعات التي تستند إلى سمة. يتطلب هذا الإجراء توفر نموذج سعر مبيعات واحد على الأقل. يستخدم هذا المثال نموذج السعر لنموذج سعر المبيعات لحل "مكبر الصوت" في شركة بيانات العرض التوضيحي USMF.‬ يستخدم مدير المنتج عادةً هذا الإجراء.


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>إضافة معيار جديد لنموذج سعر مبيعات موجود
1. انقر فوق "تعريف نموذج متغير المنتج"ز
2. انقر فوق "نماذج تكوين المنتجات".
3. في القائمة، حدد الصف الخاص بنموذج المنتج لحل "مكبر الصوت"، ولكن لا تنقر فوق الارتباط الخاص باسم النموذج.
4. في جزء الإجراءات، انقر فوق "النموذج".
5. انقر فوق "معايير نموذج السعر".
6. انقر فوق "جديد".
7. في الحقل "الاسم، اكتب "مجموعة العملاء 10".
    * يتم استخدام اسم معيار نموذج السعر للمساعدة في تحديد معايير التحديد الأساسية.  
8. في الحقل "نموذج السعر"، أدخل قيمة أو حددها.
9. في الحقل "نوع الأمر"، حدد "أمر المبيعات".
    * يحدد نوع الأمر حقول قاعدة البيانات التي سوف تكون متاحة لاستعلام التحديد.  
10. في الحقل "صالح من"، أدخل تاريخًا.
11. في الحقل "تنتهي الصلاحية في‬"، أدخل تاريخًا.
12. انقر فوق "حفظ".

## <a name="create-the-query-for-the-selection-criteria"></a>إنشاء استعلام لمعايير التحديد
1. انقر فوق "تحرير".
2. في الحقل "جدول"، حدد "العملاء". 
3. في حقل "الحقل"، حدد "مجموعة العملاء".
    * في هذا المثال، سوف نستخدم مجموعة محددة من العملاء لمعايير التحديد.  
4. في حقل "المعايير"، حدد "مجموعة العملاء 10". 
5. انقر فوق "موافق".

