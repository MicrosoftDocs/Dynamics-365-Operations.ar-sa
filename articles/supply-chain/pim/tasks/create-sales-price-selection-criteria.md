---
title: إنشاء معايير تحديد سعر المبيعات
description: يوضح هذا الإجراء كيفية إنشاء معيار تحديد سعر المبيعات لنماذج أسعار المبيعات التي تستند إلى سمة.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ed7083f289948033782f74dd9ed1b3c2d2a73aea
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568413"
---
# <a name="create-sales-price-selection-criteria"></a>إنشاء معايير تحديد سعر المبيعات

[!include [banner](../../includes/banner.md)]

يوضح هذا الإجراء كيفية إنشاء معيار تحديد سعر المبيعات لنماذج أسعار المبيعات التي تستند إلى سمة. يتطلب هذا الإجراء توفر نموذج سعر مبيعات واحد على الأقل. يستخدم هذا المثال نموذج السعر لنموذج سعر المبيعات لحل "مكبر الصوت" في شركة بيانات العرض التوضيحي USMF.‬ يستخدم مدير المنتج عادةً هذا الإجراء.

## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>إضافة معيار جديد لنموذج سعر مبيعات موجود

1. انتقل إلى **إدارة معلومات المنتج \> المنتجات \> نماذج تكوين المنتجات**.
1. في القائمة، حدد الصف الخاص بنموذج المنتج لحل "مكبر الصوت"، ولكن لا تحدد الارتباط الخاص باسم النموذج.
1. في جزء الإجراءات، حدد **النموذج**.
1. حدد **معايير نموذج السعر**.
1. حدد **جديد**.
1. في حقل **الاسم**، اكتب "مجموعة العملاء 10".
    * يتم استخدام اسم معيار نموذج السعر للمساعدة في تحديد معايير التحديد الأساسية.  
1. في حقل **نموذج السعر**، أدخل قيمة أو حددها.
1. في حقل **نوع الأمر**، حدد *أمر المبيعات*.
    * يحدد نوع الأمر حقول قاعدة البيانات التي سوف تكون متاحة لاستعلام التحديد.  
1. في حقل **صالح من**، أدخل تاريخًا.
1. في حقل **تنتهي الصلاحية في**، أدخل تاريخًا.
1. حدد **حفظ**.

## <a name="create-the-query-for-the-selection-criteria"></a>إنشاء استعلام لمعايير التحديد

1. حدد **تحرير**.
2. في حقل **الجدول**، حدد *العملاء*.
3. في حقل **الحقل**، حدد *مجموعة العملاء*.
    * في هذا المثال، سوف نستخدم مجموعة محددة من العملاء لمعايير التحديد.  
4. في حقل **المعايير**، حدد *مجموعة العملاء 10*.
5. حدد **موافق**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]