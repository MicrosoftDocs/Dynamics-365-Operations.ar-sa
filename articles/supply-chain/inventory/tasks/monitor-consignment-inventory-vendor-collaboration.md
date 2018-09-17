--- 
title: "مراقبة مخزون الشحن باستخدام تعاون المورّد"
description: "يوضح هذا الإجراء كيفية استخدام تعاون المورّد لعرض معلومات حول مستوى مخزون المنتج الذي قمت بوضعها في الشحن مع عميل."
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ConsignmentProductReceiptLines, PurchVendorPortalConfirmedOrders, DefaultDashboard, ConsignmentVendorPortalOnhand
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 567be29bd9989b3471b22d5a970ed0e51e4549ec
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a>مراقبة مخزون الشحن باستخدام تعاون المورّد

[!include [task guide banner](../../includes/task-guide-banner.md)]

يوضح هذا الإجراء كيفية استخدام تعاون المورّد لعرض معلومات حول مستوى مخزون المنتج الذي قمت بوضعها في الشحن مع عميل. يمكنك أيضًا مراقبة استهلاك المخزون عند يأخذ العميل ملكية المخزون. يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF. يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.


## <a name="view-consumed-inventory"></a>عرض المخزون المستهلك
1. انتقل إلى تعاون المورد‬ > مخزون الشحن‬ > المنتجات التي تم استلامها من مخزون الشحن‬.
    * تعرض القائمة بنود إيصال استلام المنتجات‬ التي تم إنشاؤها عندما تغيرت ملكية مخزون الشحن من المورّد إلى العميل. قد تحتاج إلى التمرير إلى اليمين لعرض الكميات ومعلومات أخرى. ويمكنك استخدام المعلومات الموجودة في هذه القائمة لإنشاء فواتير للعميل. يمكنك أيضًا تصدير البيانات إلى Microsoft Excel.   
2. انقر فوق "عرض أمر الشراء‬".
3. قم بتوسيع قسم "تفاصيل البند".
    * يتم وضع علامة "الشحن" على البند، ويوضح مقطع الرأس أن حالة أمر الشراء هي "مستلم".  
4. قم بإغلاق الصفحة.

## <a name="view-on-hand-inventory"></a>عرض المخزون الفعلي
1. انتقل إلى تعاون المورد‬ > مخزون الشحن‬ > مخزون الشحن الفعلي‬‬.
    * تظهر الصفحة "مخزون الشحن الفعلي‬" المخزون الذي تملكه في مستودع العميل. يمكنك إظهار أبعاد إضافية، مثل الموقع والمستودع، بالنقر فوق علامة التبويب "عرض الأبعاد‬".   


