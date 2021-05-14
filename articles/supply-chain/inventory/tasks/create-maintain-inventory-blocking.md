---
title: إنشاء وصيانة حظر المخزون
description: يصف هذا الموضوع كيفية استخدام حظر المخزون لمنع حجز المخزون الفعلي المتاح بواسطة مستندات المصدر الصادرة الأخرى.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e9aa38ca52da577fff258bb330922ad7f4044330
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956148"
---
# <a name="create-and-maintain-an-inventory-blocking"></a><span data-ttu-id="775b9-103">إنشاء وصيانة حظر المخزون</span><span class="sxs-lookup"><span data-stu-id="775b9-103">Create and maintain an inventory blocking</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="775b9-104">يصف هذا الموضوع كيفية استخدام حظر المخزون لمنع حجز المخزون الفعلي المتاح بواسطة مستندات المصدر الصادرة الأخرى.</span><span class="sxs-lookup"><span data-stu-id="775b9-104">This topic describes how to use an inventory blocking to prevent physical on-hand inventory from being reserved by other outbound source documents.</span></span> <span data-ttu-id="775b9-105">قبل أن تبدأ الإجراءات في هذا الموضوع، يجب أن يكون لديك عنصر يتوفر له المخزون الفعلي المتاح.</span><span class="sxs-lookup"><span data-stu-id="775b9-105">Before you start the procedures in this topic, you must have an item that physical on-hand inventory is available for.</span></span>

## <a name="block-inventory"></a><span data-ttu-id="775b9-106">حظر المخزون</span><span class="sxs-lookup"><span data-stu-id="775b9-106">Block inventory</span></span>

<span data-ttu-id="775b9-107">لإنشاء سجل حظر مخزون بحيث يتم حظر المخزون، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="775b9-107">To create an inventory blocking record so that inventory is blocked, follow these steps.</span></span>

1. <span data-ttu-id="775b9-108">انتقل إلى **إدارة المخزون \> المهام الدورية \> حظر المخزون**.</span><span class="sxs-lookup"><span data-stu-id="775b9-108">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="775b9-109">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="775b9-109">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="775b9-110">في رأس سجل الحظر الجديد، قم بتعيين حقل **رقم العنصر** إلى العنصر الذي تريد حظره، وأدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="775b9-110">On the header of the new blocking record, set the **Item number** field to the item that you want to block, and enter a description.</span></span>
1. <span data-ttu-id="775b9-111">في علامة التبويب السريعة **عام**، في حقل **الكمية**، أدخل عدد العناصر المراد حظرها.</span><span class="sxs-lookup"><span data-stu-id="775b9-111">On the **General** FastTab, in the **Quantity** field, enter the number of items to block.</span></span>
1. <span data-ttu-id="775b9-112">في علامة التبويب **أبعاد المخزون**، حدد الموقع والمستودع حيث توجد العناصر التي تريد حظرها حاليًا.</span><span class="sxs-lookup"><span data-stu-id="775b9-112">On the **Inventory dimensions** FastTab, specify the site and warehouse where the items that you want to block are currently located.</span></span>
1. <span data-ttu-id="775b9-113">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="775b9-113">On the Action Pane, select **Save**.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="775b9-114">تحديث شروط حظر المخزون</span><span class="sxs-lookup"><span data-stu-id="775b9-114">Update the conditions of the inventory blocking</span></span>

<span data-ttu-id="775b9-115">لتحديث سجل حظر المخزون، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="775b9-115">To update an inventory blocking record, follow these steps.</span></span>

1. <span data-ttu-id="775b9-116">انتقل إلى **إدارة المخزون \> المهام الدورية \> حظر المخزون**.</span><span class="sxs-lookup"><span data-stu-id="775b9-116">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="775b9-117">في جزء القائمة، حدد سجل الحظر ذي الصلة.</span><span class="sxs-lookup"><span data-stu-id="775b9-117">In the list pane, select the relevant blocking record.</span></span>
1. <span data-ttu-id="775b9-118">قم بتحرير السجل كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="775b9-118">Edit the record as required.</span></span> <span data-ttu-id="775b9-119">على سبيل المثال، يمكنك تغيير قيمة حقل **التاريخ المتوقع** للإشارة إلى الوقت المتوقع فيه أن يصبح المخزون الموقوف متاحًا للحجز.</span><span class="sxs-lookup"><span data-stu-id="775b9-119">For example, you might change the value of the **Expected date** field to indicate when the blocked inventory is expected to become available for reservation.</span></span> <span data-ttu-id="775b9-120">في حالة تحديد خيار **الإيصالات المتوقعة**، سيظهر التاريخ على الحركة المتوقعة.</span><span class="sxs-lookup"><span data-stu-id="775b9-120">If the **Expected receipts** option is selected, the date will appear on the expected transaction.</span></span> <span data-ttu-id="775b9-121">(يتم تحديد خيار **الإيصالات المتوقعة** افتراضيًا عندما تنشئ سجل حظر يدويًا.)</span><span class="sxs-lookup"><span data-stu-id="775b9-121">(The **Expected receipts** option is selected by default when you manually create a blocking record.)</span></span>
1. <span data-ttu-id="775b9-122">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="775b9-122">On the Action Pane, select **Save**.</span></span>

## <a name="unblock-inventory"></a><span data-ttu-id="775b9-123">إلغاء حظر المخزون</span><span class="sxs-lookup"><span data-stu-id="775b9-123">Unblock inventory</span></span>

<span data-ttu-id="775b9-124">لإزالة سجل حظر مخزون بحيث يتم إلغاء حظر المخزون، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="775b9-124">To remove an inventory blocking record so that inventory is unblocked, follow these steps.</span></span>

1. <span data-ttu-id="775b9-125">انتقل إلى **إدارة المخزون \> المهام الدورية \> حظر المخزون**.</span><span class="sxs-lookup"><span data-stu-id="775b9-125">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="775b9-126">في جزء القائمة، حدد سجل الحظر ذي الصلة.</span><span class="sxs-lookup"><span data-stu-id="775b9-126">In the list pane, select the relevant blocking record.</span></span>
1. <span data-ttu-id="775b9-127">في جزء الإجراءات، حدد **حذف**.</span><span class="sxs-lookup"><span data-stu-id="775b9-127">On the Action Pane, select **Delete**.</span></span>
1. <span data-ttu-id="775b9-128">يُطلب منك تأكيد العملية.</span><span class="sxs-lookup"><span data-stu-id="775b9-128">You're prompted to confirm the operation.</span></span> <span data-ttu-id="775b9-129">للمتابعة، حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="775b9-129">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="775b9-130">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="775b9-130">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
