---
title: "إعداد الشحن"
description: "يشرح هذا الموضوع كيفية تكوين عمليات مخزون الشحن الوارد."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventJournalOwnershipChange, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 220804
ms.assetid: 88822f78-4de5-462c-a55f-1f766c572719
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 41c1b8de0aae24efb30a670d3109b6d65e6abd9c
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-consignment"></a>إعداد الشحن

[!include[banner](../includes/banner.md)]


يشرح هذا الموضوع كيفية تكوين عمليات مخزون الشحن الوارد.

إن مخزون الشحن هو المخزون الذي يملكه المورد، ولكنه مخزن في موقعك. عندما تصبح جاهزًا لاستهلاك المخزون أو استخدامه، يمكنك الحصول على ملكية المخزون. يصف هذا الموضوع الإعداد المطلوب لتمكين عمليات الشحن. للحصول على مزيد من المعلومات حول عمليات الشحن، راجع [الشحن](consignment.md).

## <a name="inventory-owners"></a>ملاك المخزون
من أجل تسجيل المخزون الفعلي للشحن الوارد، يجب تعريف المالك المورّد. ويتم ذلك في صفحة **مالك المخزون**. عند تحديد **حساب المورد**، يؤدي ذلك إلى إنشاء القيم الافتراضية لحقلي **الاسم** و **المالك**. ستكون القيمة في حقل **المالك** مرئية للمورد، لذا قد ترغب في تغييرها إذا لم يكن من السهل على الأشخاص الخارجيين التعرف على أسماء حسابات المورد. من الممكن تحرير حقل **المالك**، لكن فقط إلى المرحلة التي تقوم فيها بحفظ سجل **مالك المخزون**. تتم تعبئة حقل **الاسم** باسم الطرف الذي يقترن حساب المورد به، ولا يمكن تغيير ذلك.

[![ملاك المخزون](./media/inventory-owners.png)](./media/inventory-owners.png)

## <a name="tracking-dimension-group"></a>مجموعة أبعاد التعقب
يجب أن تقترن الأصناف التي سيتم استخدامها في عمليات الشحن **بمجموعة أبعاد التعقب** حيث تم تعيين بُعد **المالك** إلى **نشط**. في بُعد المالك، يكون الخياران **المخزون الفعلي** و**المخزون المالي** محددين بشكل دائم. ولا يتم تحديد الخيار **خطة التغطية حسب البُعد‬** إطلاقًا.

[![مجموعة أبعاد التعقب](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)

## <a name="inventory-ownership-change-journal"></a>دفتر يومية تغييرات ملكية المخزون
يُستخدم **دفتر يومية تغيير ملكية المخزون**لتسجيل تحويل ملكية مخزون الشحن من المورّد إلى الكيان القانوني الذي يستهلكه. وكما هو الحال في أي دفتر يومية مخزون، يجب تعريفه بواسطة اسم دفتر يومية المخزون. يتم إنشاء هذه الأسماء في صفحة **أسماء دفتر يومية المخزون** الصفحة، ويجب تعيين **نوع دفتر اليومية** إلى **تغيير الملكية**.

[![دفتر يومية تغييرات ملكية المخزون](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>تعاون المورد في عمليات الشحن
عندما يستخدم الموردون واجهة تعاون المورد، يمكنهم استخدامها لمراقبة استهلاك المخزون في موقعك. لمزيد من المعلومات حول إعداد الموردين لاستخدام تعاون المورِّد‏‎، راجع [تكوين الأمان لمستخدمي تعاون المورِّد](../procurement/configure-security-vendor-portal-users.md).

