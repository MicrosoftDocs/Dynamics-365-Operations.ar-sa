---
title: "خيارات حركات الأصول الثابتة"
description: "توضح هذه المقالة الطرق المختلفة لإنشاء حركات الأصول الثابتة."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 9be300652e3de23554e1e61e32f1b0070e08099b
ms.contentlocale: ar-sa
ms.lasthandoff: 08/07/2018

---

# <a name="fixed-asset-transaction-options"></a><span data-ttu-id="1b174-103">خيارات حركات الأصول الثابتة</span><span class="sxs-lookup"><span data-stu-id="1b174-103">Fixed asset transaction options</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1b174-104">توضح هذه المقالة الطرق المختلفة لإنشاء حركات الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="1b174-104">This article describes the different methods available to create fixed asset transactions.</span></span>

<span data-ttu-id="1b174-105">يمكن إعداد الأصول الثابتة لتتكامل مع الحسابات الدائنة والحسابات المدينة والتدبير والمصادر ودفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="1b174-105">You can set up Fixed assets for integration with Accounts payable, Accounts receivable, Procurement and sourcing, and General ledger.</span></span> <span data-ttu-id="1b174-106">يمكنك أيضًا تحويل الأصناف من إدارة المخزون إلى الأصول الثابتة إذا أردت استخدامها داخليًا.</span><span class="sxs-lookup"><span data-stu-id="1b174-106">You can also transfer items in Inventory management to Fixed assets if you want to use those items internally.</span></span>

## <a name="accounts-payable"></a><span data-ttu-id="1b174-107">حسابات دائنة</span><span class="sxs-lookup"><span data-stu-id="1b174-107">Accounts payable</span></span>
<span data-ttu-id="1b174-108">يمكنك إدخال حركات الأصول الثابتة في صفحة إيصال دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="1b174-108">You can enter Fixed assets transactions in the Journal voucher page.</span></span> <span data-ttu-id="1b174-109">ويمكن فتح هذه الصفحة من صفحة دفتر يومية الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="1b174-109">This page can be opened from the Invoice journal page.</span></span> <span data-ttu-id="1b174-110">كما يمكنك فتح صفحة إيصال دفتر اليومية من صفحة دفتر يومية اعتماد الفواتير.</span><span class="sxs-lookup"><span data-stu-id="1b174-110">You can also open the Journal voucher page from the Invoice approval journal page.</span></span> <span data-ttu-id="1b174-111">وفي حقل نوع الحساب المقابل، حدد الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="1b174-111">In the Offset account type field, select Fixed assets.</span></span> <span data-ttu-id="1b174-112">وبعد ذلك، في حقل الحساب المقابل، حدد رقم أصل ثابت.</span><span class="sxs-lookup"><span data-stu-id="1b174-112">Then, in the Offset account field, select a fixed asset number.</span></span> <span data-ttu-id="1b174-113">في علامة التبويب "الأصول الثابتة"، أدخل القيم في حقلي "نوع الحركة" و"الدفاتر".</span><span class="sxs-lookup"><span data-stu-id="1b174-113">On the Fixed assets tab, enter values in the Transaction type and Book fields.</span></span>

## <a name="accounts-receivable"></a><span data-ttu-id="1b174-114">الحسابات المدينة</span><span class="sxs-lookup"><span data-stu-id="1b174-114">Accounts receivable</span></span>
<span data-ttu-id="1b174-115">يمكنك إدخال حركات الأصول الثابتة في صفحة فاتورة النص الحر.</span><span class="sxs-lookup"><span data-stu-id="1b174-115">You can enter Fixed assets transactions in the Free text invoice page.</span></span>  <span data-ttu-id="1b174-116">وفي صفحة فاتورة النص الحر في شبكة بنود الفاتورة، حدد صنف بند.‬</span><span class="sxs-lookup"><span data-stu-id="1b174-116">In the Free text invoice page, in the Invoice lines grid, select a line item.</span></span> <span data-ttu-id="1b174-117">انقر فوق علامة التبويب السريعة تفاصيل البند.</span><span class="sxs-lookup"><span data-stu-id="1b174-117">Click the Line details FastTab.</span></span> <span data-ttu-id="1b174-118">أدخل رقم الأصل الثابت والدفتر لحركة التخلص.</span><span class="sxs-lookup"><span data-stu-id="1b174-118">Enter the fixed asset number and book for the disposal transaction.</span></span> <span data-ttu-id="1b174-119">في فاتورة النص الحر، تكون حركة الأصل الثابت دائمًا من نوع ‏‫التخلص - البيع‬.</span><span class="sxs-lookup"><span data-stu-id="1b174-119">For free text invoices, the fixed asset transaction type is always Disposal - sale.</span></span>

## <a name="procurement-and-sourcing"></a><span data-ttu-id="1b174-120">التدبير وتحديد الموارد</span><span class="sxs-lookup"><span data-stu-id="1b174-120">Procurement and sourcing</span></span>
<span data-ttu-id="1b174-121">يمكنك إدخال حركات الأصول الثابتة في صفحة أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="1b174-121">You can enter Fixed assets transactions in the Purchase order page.</span></span> <span data-ttu-id="1b174-122">وأدخل المعلومات المطلوبة لإنشاء أمر شراء، ثم انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="1b174-122">Enter the required information to create a purchase order, and then click OK.</span></span> <span data-ttu-id="1b174-123">وفي صفحة "أمر الشراء"، انقر فوق علامة التبويب السريعة تفاصيل بند.</span><span class="sxs-lookup"><span data-stu-id="1b174-123">In the Purchase order page, click the Line details FastTab.</span></span> <span data-ttu-id="1b174-124">وبعد ذلك، في علامة التبويب الأصول الثابتة، أدخل معلومات حول الأصل الثابت.</span><span class="sxs-lookup"><span data-stu-id="1b174-124">Then, on the Fixed assets tab, enter information about the fixed asset.</span></span> 

<span data-ttu-id="1b174-125">لترحيل حركة استحواذ لأصل ثابت موجود، حدد رقم الأصل الثابت والدفتر ونوع الحركة.</span><span class="sxs-lookup"><span data-stu-id="1b174-125">To post an acquisition transaction for an existing fixed asset, specify the fixed asset number, book, and transaction type.</span></span> <span data-ttu-id="1b174-126">لا يمكن ترحيل الأصل الثابت في حالة فقدان أي من هذه المعلومات.</span><span class="sxs-lookup"><span data-stu-id="1b174-126">The fixed asset cannot be posted if any of this information is missing.</span></span> <span data-ttu-id="1b174-127">لترحيل حركة امتلاك لأصل ثابت جديد، حدد خيار أصل ثابت جديد؟، ثم قم بتحديد مجموعة الأصل الثابت لتعيين الأصل الثابت الجديد لها.</span><span class="sxs-lookup"><span data-stu-id="1b174-127">To post an acquisition transaction for a new fixed asset, select the New fixed asset? option, and then select the fixed asset group to assign the new asset to.</span></span> <span data-ttu-id="1b174-128">برغم هذا لا تتوفر حقول أصول ثابتة لسطر، إذا كان الصنف في مجموعة نموذج مخزون تستخدم نموذج مخزون تكلفة قياسي.</span><span class="sxs-lookup"><span data-stu-id="1b174-128">However, no fixed asset fields are available for a line if the item is in an inventory model group that uses a standard cost inventory model.</span></span> <span data-ttu-id="1b174-129">بالإضافة إلى ذلك، تحدد الخيارات التي تم تحديدها في صفحة معلمات الأصول الثابتة ما إذا كان يمكنك ترحيل حركات الامتلاك من وحدات الشراء.</span><span class="sxs-lookup"><span data-stu-id="1b174-129">Additionally, the options that are defined in the Fixed assets parameters page determine whether you can post acquisition transactions from the purchasing modules.</span></span> 

<span data-ttu-id="1b174-130">عند استخدام أمر شراء أو مخزون دفتر يومية الأصول الثابتة لامتلاك الأصول الثابتة، تتأثر قيمة المخزون.</span><span class="sxs-lookup"><span data-stu-id="1b174-130">When a purchase order or the Inventory to fixed assets journal is used to acquire fixed assets, the inventory value is affected.</span></span>

## <a name="general-ledger"></a><span data-ttu-id="1b174-131">دفتر الأستاذ العام</span><span class="sxs-lookup"><span data-stu-id="1b174-131">General ledger</span></span>
<span data-ttu-id="1b174-132">يمكن ترحيل أي نوع حركة أصل ثابت في صفحة دفتر اليومية العام.</span><span class="sxs-lookup"><span data-stu-id="1b174-132">Any fixed asset transaction type can be posted in the General journal page.</span></span> <span data-ttu-id="1b174-133">يمكنك أيضا استخدام دفاتر يومية الأصول الثابتة لترحيل حركات الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="1b174-133">You can also use journals in Fixed assets to post fixed asset transactions.</span></span>

## <a name="options-for-entering-fixed-asset-transaction-types"></a><span data-ttu-id="1b174-134">خيارات إدخال أنواع حركات الأصول الثابتة</span><span class="sxs-lookup"><span data-stu-id="1b174-134">Options for entering fixed asset transaction types</span></span>


| <span data-ttu-id="1b174-135">نوع الحركة</span><span class="sxs-lookup"><span data-stu-id="1b174-135">Transaction type</span></span>                    | <span data-ttu-id="1b174-136">الوحدة النمطية</span><span class="sxs-lookup"><span data-stu-id="1b174-136">Module</span></span>                   | <span data-ttu-id="1b174-137">الخيارات</span><span class="sxs-lookup"><span data-stu-id="1b174-137">Options</span></span>                                   |
|-------------------------------------|--------------------------|-------------------------------------------|
| <span data-ttu-id="1b174-138">الاستحواذ، تسوية الاستحواذ‬</span><span class="sxs-lookup"><span data-stu-id="1b174-138">Acquisition, Acquisition adjustment</span></span> | <span data-ttu-id="1b174-139">الأصول الثابتة</span><span class="sxs-lookup"><span data-stu-id="1b174-139">Fixed assets</span></span>             | <span data-ttu-id="1b174-140">الأصول الثابتة، مخزون الأصول الثابتة</span><span class="sxs-lookup"><span data-stu-id="1b174-140">Fixed assets, Inventory to fixed assets</span></span>   |
|                                     | <span data-ttu-id="1b174-141">دفتر الأستاذ العام</span><span class="sxs-lookup"><span data-stu-id="1b174-141">General ledger</span></span>           | <span data-ttu-id="1b174-142">دفتر اليومية العام</span><span class="sxs-lookup"><span data-stu-id="1b174-142">General journal</span></span>                           |
|                                     | <span data-ttu-id="1b174-143">حسابات دائنة</span><span class="sxs-lookup"><span data-stu-id="1b174-143">Accounts payable</span></span>         | <span data-ttu-id="1b174-144">دفتر يومية الفواتير، دفتر يومية اعتماد الفواتير</span><span class="sxs-lookup"><span data-stu-id="1b174-144">Invoice journal, Invoice approval journal</span></span> |
|                                     | <span data-ttu-id="1b174-145">التدبير وتحديد الموارد</span><span class="sxs-lookup"><span data-stu-id="1b174-145">Procurement and sourcing</span></span> | <span data-ttu-id="1b174-146">أمر شراء</span><span class="sxs-lookup"><span data-stu-id="1b174-146">Purchase order</span></span>                            |
| <span data-ttu-id="1b174-147">الإهلاك</span><span class="sxs-lookup"><span data-stu-id="1b174-147">Depreciation</span></span>                        | <span data-ttu-id="1b174-148">الأصول الثابتة</span><span class="sxs-lookup"><span data-stu-id="1b174-148">Fixed assets</span></span>             | <span data-ttu-id="1b174-149">الأصول الثابتة</span><span class="sxs-lookup"><span data-stu-id="1b174-149">Fixed assets</span></span>                              |
|                                     | <span data-ttu-id="1b174-150">دفتر الأستاذ العام</span><span class="sxs-lookup"><span data-stu-id="1b174-150">General ledger</span></span>           | <span data-ttu-id="1b174-151">دفتر اليومية العام</span><span class="sxs-lookup"><span data-stu-id="1b174-151">General journal</span></span>                           |
| <span data-ttu-id="1b174-152">التخلص</span><span class="sxs-lookup"><span data-stu-id="1b174-152">Disposal</span></span>                            | <span data-ttu-id="1b174-153">الأصول الثابتة</span><span class="sxs-lookup"><span data-stu-id="1b174-153">Fixed assets</span></span>             | <span data-ttu-id="1b174-154">الأصول الثابتة</span><span class="sxs-lookup"><span data-stu-id="1b174-154">Fixed assets</span></span>                              |
| <span data-ttu-id="1b174-155">** **</span><span class="sxs-lookup"><span data-stu-id="1b174-155">** **</span></span>                               | <span data-ttu-id="1b174-156">دفتر الأستاذ العام</span><span class="sxs-lookup"><span data-stu-id="1b174-156">General ledger</span></span>           | <span data-ttu-id="1b174-157">دفتر اليومية العام</span><span class="sxs-lookup"><span data-stu-id="1b174-157">General journal</span></span>                           |
| <span data-ttu-id="1b174-158">** **</span><span class="sxs-lookup"><span data-stu-id="1b174-158">** **</span></span>                               | <span data-ttu-id="1b174-159">الحسابات المدينة</span><span class="sxs-lookup"><span data-stu-id="1b174-159">Accounts receivable</span></span>      | <span data-ttu-id="1b174-160">فاتورة ذات نص حر</span><span class="sxs-lookup"><span data-stu-id="1b174-160">Free text invoice</span></span>                         |



<span data-ttu-id="1b174-161">لمزيد من المعلومات، راجع [تكامل الأصول الثابتة](fixed-asset-integration.md).</span><span class="sxs-lookup"><span data-stu-id="1b174-161">For more information, see [Fixed assets integration](fixed-asset-integration.md).</span></span>




