--- 
title: " إنشاء حزم المنتجات لأوامر الشراء"
description: "يتناول هذا الإجراء إنشاء حزمة منتجات واستخدامها على أمر شراء."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: a3be1e7aca7f0382aea55fa8a371c33c8b53df95
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="create-product-packages-for-purchase-orders"></a><span data-ttu-id="11905-103"> إنشاء حزم المنتجات لأوامر الشراء</span><span class="sxs-lookup"><span data-stu-id="11905-103">Create product packages for purchase orders</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="11905-104">يتناول هذا الإجراء إنشاء حزمة منتجات واستخدامها على أمر شراء.</span><span class="sxs-lookup"><span data-stu-id="11905-104">This procedure walks through creating a product package and using it on a purchase order.</span></span> <span data-ttu-id="11905-105">سيتم استخدام أمر الشراء لإنشاء أمر لمجموعة من المنتجات محددة مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="11905-105">The purchase order will be used to create an order for a pre-defined set of products.</span></span> <span data-ttu-id="11905-106">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USRT.</span><span class="sxs-lookup"><span data-stu-id="11905-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-product-package"></a><span data-ttu-id="11905-107">إنشاء حزمة المنتجات</span><span class="sxs-lookup"><span data-stu-id="11905-107">Create a product package</span></span>
1. <span data-ttu-id="11905-108">انتقل إلى البيع بالتجزئة والتجارة > إدارة المخزون > التزويد > حزم المنتجات.</span><span class="sxs-lookup"><span data-stu-id="11905-108">Go to Retail and commerce > Inventory management > Replenishment > Product packages.</span></span>
2. <span data-ttu-id="11905-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="11905-109">Click New.</span></span>
3. <span data-ttu-id="11905-110">في حقل "رقم الحزمة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="11905-110">In the Package number field, type a value.</span></span>
4. <span data-ttu-id="11905-111">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="11905-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="11905-112">في الحقل "حساب المورّد‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="11905-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="11905-113">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="11905-113">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="11905-114">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="11905-114">Click Add.</span></span>
8. <span data-ttu-id="11905-115">في حقل "رقم الصنف"، اكتب "0160".</span><span class="sxs-lookup"><span data-stu-id="11905-115">In the Item number field, type '0160'.</span></span>
9. <span data-ttu-id="11905-116">في حقل "الحجم"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="11905-116">In the Size field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="11905-117">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="11905-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="11905-118">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="11905-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="11905-119">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="11905-119">Click Add.</span></span>
13. <span data-ttu-id="11905-120">في حقل "رقم الصنف"، اكتب "0160".</span><span class="sxs-lookup"><span data-stu-id="11905-120">In the Item number field, type '0160'.</span></span>
14. <span data-ttu-id="11905-121">في حقل "‏‫رقم المتغير‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="11905-121">In the Variant number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="11905-122">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="11905-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="11905-123">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="11905-123">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="11905-124">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="11905-124">Click Add.</span></span>
18. <span data-ttu-id="11905-125">في حقل "رقم الصنف"، اكتب "0175".</span><span class="sxs-lookup"><span data-stu-id="11905-125">In the Item number field, type '0175'.</span></span>
19. <span data-ttu-id="11905-126">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="11905-126">In the Quantity field, enter a number.</span></span>
20. <span data-ttu-id="11905-127">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="11905-127">Click Save.</span></span>
21. <span data-ttu-id="11905-128">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="11905-128">Close the page.</span></span>

## <a name="add-package-to-puchase-order"></a><span data-ttu-id="11905-129">إضافة حزمة إلى أمر الشراء</span><span class="sxs-lookup"><span data-stu-id="11905-129">Add package to puchase order</span></span>
1. <span data-ttu-id="11905-130">انتقل إلى الحسابات الدائنة > أوامر الشراء > جميع أوامر الشراء.</span><span class="sxs-lookup"><span data-stu-id="11905-130">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="11905-131">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="11905-131">Click New.</span></span>
3. <span data-ttu-id="11905-132">في الحقل "حساب المورّد‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="11905-132">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="11905-133">في القائمة، حدد نفس المورد الذي تم إنشاء حزمة المنتجات له مسبقًا، إذا تم تحديد مورد.</span><span class="sxs-lookup"><span data-stu-id="11905-133">In the list, select the same vendor that the product package was previously created for, if a vendor was selected.</span></span>
5. <span data-ttu-id="11905-134">بدّل توسيع المقطع "عام".</span><span class="sxs-lookup"><span data-stu-id="11905-134">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="11905-135">في الحقل "الموقع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="11905-135">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="11905-136">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="11905-136">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="11905-137">في الحقل "المستودع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="11905-137">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="11905-138">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="11905-138">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="11905-139">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="11905-139">Click OK.</span></span>
11. <span data-ttu-id="11905-140">بدّل توسيع المقطع "تفاصيل البنود‬‬".</span><span class="sxs-lookup"><span data-stu-id="11905-140">Toggle the expansion of the Line details section.</span></span>
12. <span data-ttu-id="11905-141">انقر فوق علامة التبويب حزم المنتجات.</span><span class="sxs-lookup"><span data-stu-id="11905-141">Click the Product packages tab.</span></span>
13. <span data-ttu-id="11905-142">انقر فوق سطر أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="11905-142">Click Purchase order line.</span></span>
14. <span data-ttu-id="11905-143">انقر فوق إنشاء بنود من الحزمة.</span><span class="sxs-lookup"><span data-stu-id="11905-143">Click Create lines from package.</span></span>
15. <span data-ttu-id="11905-144">في القائمة، ابحث عن حزمة المنتجات التي تم إنشاؤها في الخطوة السابقة وحددها.</span><span class="sxs-lookup"><span data-stu-id="11905-144">In the list, find and select the product package created in previous step.</span></span>
16. <span data-ttu-id="11905-145">في الحقل "الكمية"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="11905-145">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="11905-146">انقر فوق "إنشاء".</span><span class="sxs-lookup"><span data-stu-id="11905-146">Click Create.</span></span>
18. <span data-ttu-id="11905-147">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="11905-147">Click Save.</span></span>


