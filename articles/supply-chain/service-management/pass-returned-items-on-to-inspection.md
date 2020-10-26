---
title: تمرير الأصناف المرتجعة إلى الفحص
description: عند تسجيل صنف مرتجع، فحدد أنه ينبغي إرسال صنف للفحص قبل إرجاعه إلى المخزون أو التخلص منه بطريقة أخرى.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSJournalTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6e8205db277715f4f4f9c1ee589f264c0ded6617
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983809"
---
# <a name="pass-returned-items-on-to-inspection"></a><span data-ttu-id="a1ee0-103">تمرير الأصناف المرتجعة إلى الفحص</span><span class="sxs-lookup"><span data-stu-id="a1ee0-103">Pass returned items on to inspection</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a1ee0-104">عند تسجيل صنف مرتجع، فربما تحدد أنه ينبغي إرسال صنف للفحص قبل إرجاعه إلى المخزون أو التخلص منه بطريقة أخرى.</span><span class="sxs-lookup"><span data-stu-id="a1ee0-104">When registering a returned item, you may determine that an item should be sent for inspection before it is returned to inventory or disposed of in some other way.</span></span>

1.  <span data-ttu-id="a1ee0-105">انقر فوق **إدارة المخزون** \> **دفتر اليومية** \> **وصول الصنف‬** \> **وصول الصنف‬** .</span><span class="sxs-lookup"><span data-stu-id="a1ee0-105">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Item arrival** .</span></span>
    
    <span data-ttu-id="a1ee0-106">\-أو-</span><span class="sxs-lookup"><span data-stu-id="a1ee0-106">\-or-</span></span>
    
    <span data-ttu-id="a1ee0-107">انقر فوق **إدارة المخزون** \> **دفتر اليومية** \> **وصول الصنف‬** \> **مدخلات الإنتاج** .</span><span class="sxs-lookup"><span data-stu-id="a1ee0-107">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Production input** .</span></span>

2.  <span data-ttu-id="a1ee0-108">في نموذج **دفتر يومية الموقع** ، سجل استلام صنف كما هو معتاد. </span><span class="sxs-lookup"><span data-stu-id="a1ee0-108">On the **Location journal** form, register the receipt of an item as usual.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="a1ee0-109">للحصول على مزيد من المعلومات حول تسجيل استلام الأصناف المرتجعة، راجع <A href="register-the-receipt-of-returned-items.md">تسجيل استلام الأصناف المرتجعة</A></span><span class="sxs-lookup"><span data-stu-id="a1ee0-109">For information about registering the receipt of returned items, see <A href="register-the-receipt-of-returned-items.md">Register the receipt of returned items</A></span></span></P>



3.  <span data-ttu-id="a1ee0-110">في علامة تبويب **قيم افتراضية** ، في منطقة **وضع المعالجة** ، حدد خانة **إدارة العزل** .</span><span class="sxs-lookup"><span data-stu-id="a1ee0-110">On the **Default values** tab, in the **Mode of handling** area, select the **Quarantine management** box.</span></span>

<span data-ttu-id="a1ee0-111">سوف يؤدي هذا إلى مطالبة النظام بإنشاء أمر إدخال مخزن الفحص، وسوف يستجيب الشخص أو القسم الذي يجري عمليات الفحص لهذا الأمر باستخدام النموذج **أمر العزل** .</span><span class="sxs-lookup"><span data-stu-id="a1ee0-111">This will prompt the system to create a quarantine order, and the person or department that performs inspections will respond to this order using the **Quarantine order** form.</span></span>

## <a name="see-also"></a><span data-ttu-id="a1ee0-112">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="a1ee0-112">See also</span></span>

[<span data-ttu-id="a1ee0-113">أخذ الأصناف المرتجعة عبر الفحص</span><span class="sxs-lookup"><span data-stu-id="a1ee0-113">Take returned items through inspection</span></span>](take-returned-items-through-inspection.md)

[<span data-ttu-id="a1ee0-114">تحديد كيفية التخلص من الأصناف المرتجعة</span><span class="sxs-lookup"><span data-stu-id="a1ee0-114">Specify how to dispose of returned items</span></span>](specify-how-to-dispose-of-returned-items.md)

