---
title: تمرير الأصناف المرتجعة إلى الفحص
description: عند تسجيل صنف مرتجع، فحدد أنه ينبغي إرسال صنف للفحص قبل إرجاعه إلى المخزون أو التخلص منه بطريقة أخرى.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSJournalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 70aafb752b2c847d5d48236fd5d201a73e088c24
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556773"
---
# <a name="pass-returned-items-on-to-inspection"></a><span data-ttu-id="a1136-103">تمرير الأصناف المرتجعة إلى الفحص</span><span class="sxs-lookup"><span data-stu-id="a1136-103">Pass returned items on to inspection</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a1136-104">عند تسجيل صنف مرتجع، فربما تحدد أنه ينبغي إرسال صنف للفحص قبل إرجاعه إلى المخزون أو التخلص منه بطريقة أخرى.</span><span class="sxs-lookup"><span data-stu-id="a1136-104">When registering a returned item, you may determine that an item should be sent for inspection before it is returned to inventory or disposed of in some other way.</span></span>

1.  <span data-ttu-id="a1136-105">انقر فوق **إدارة المخزون** \> **دفتر اليومية** \> **وصول الصنف‬** \> **وصول الصنف‬**.</span><span class="sxs-lookup"><span data-stu-id="a1136-105">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Item arrival**.</span></span>
    
    <span data-ttu-id="a1136-106">\-أو-</span><span class="sxs-lookup"><span data-stu-id="a1136-106">\-or-</span></span>
    
    <span data-ttu-id="a1136-107">انقر فوق **إدارة المخزون** \> **دفتر اليومية** \> **وصول الصنف‬** \> **مدخلات الإنتاج**.</span><span class="sxs-lookup"><span data-stu-id="a1136-107">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Production input**.</span></span>

2.  <span data-ttu-id="a1136-108">في نموذج **دفتر يومية الموقع**، سجل استلام صنف كما هو معتاد. </span><span class="sxs-lookup"><span data-stu-id="a1136-108">On the **Location journal** form, register the receipt of an item as usual.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="a1136-109">للحصول على مزيد من المعلومات حول تسجيل استلام الأصناف المرتجعة، راجع <A href="register-the-receipt-of-returned-items.md">تسجيل استلام الأصناف المرتجعة</A></span><span class="sxs-lookup"><span data-stu-id="a1136-109">For information about registering the receipt of returned items, see <A href="register-the-receipt-of-returned-items.md">Register the receipt of returned items</A></span></span></P>



3.  <span data-ttu-id="a1136-110">في علامة تبويب **قيم افتراضية**، في منطقة **وضع المعالجة**، حدد خانة **إدارة العزل**.</span><span class="sxs-lookup"><span data-stu-id="a1136-110">On the **Default values** tab, in the **Mode of handling** area, select the **Quarantine management** box.</span></span>

<span data-ttu-id="a1136-111">سوف يؤدي هذا إلى مطالبة النظام بإنشاء أمر إدخال مخزن الفحص، وسوف يستجيب الشخص أو القسم الذي يجري عمليات الفحص لهذا الأمر باستخدام النموذج **أمر العزل**.</span><span class="sxs-lookup"><span data-stu-id="a1136-111">This will prompt the system to create a quarantine order, and the person or department that performs inspections will respond to this order using the **Quarantine order** form.</span></span>

## <a name="see-also"></a><span data-ttu-id="a1136-112">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="a1136-112">See also</span></span>

[<span data-ttu-id="a1136-113">أخذ الأصناف المرتجعة عبر الفحص</span><span class="sxs-lookup"><span data-stu-id="a1136-113">Take returned items through inspection</span></span>](take-returned-items-through-inspection.md)

[<span data-ttu-id="a1136-114">تحديد كيفية التخلص من الأصناف المرتجعة</span><span class="sxs-lookup"><span data-stu-id="a1136-114">Specify how to dispose of returned items</span></span>](specify-how-to-dispose-of-returned-items.md)

