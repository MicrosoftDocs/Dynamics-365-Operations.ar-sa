---
title: اعتماد موردين لمنتجات محددة
description: يوضح هذا الإجراء كيفية اعتماد الموردين لمنتجات محددة.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, PdsApprovedVendorList, VendTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8f2cd1badb0b924150ab51ef2efc049e6666562a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "360108"
---
# <a name="approve-vendors-for-specific-products"></a><span data-ttu-id="0c18a-103">اعتماد موردين لمنتجات محددة</span><span class="sxs-lookup"><span data-stu-id="0c18a-103">Approve vendors for specific products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0c18a-104">يوضح هذا الإجراء كيفية اعتماد الموردين لمنتجات محددة.</span><span class="sxs-lookup"><span data-stu-id="0c18a-104">This procedure shows you how to approve vendors for specific products.</span></span> <span data-ttu-id="0c18a-105">يسمح لك بالتحكم في الموردين الذين يمكن استخدامهم عند إضافة المنتج إلى أمر شراء.</span><span class="sxs-lookup"><span data-stu-id="0c18a-105">This allows you to control which vendors can be used when the product is added to a purchase order.</span></span> <span data-ttu-id="0c18a-106">يمكنك استخدام هذا الإجراء في شركة بيانات العرض التوضيحي USMF أو باستخدام بياناتك الخاصة.</span><span class="sxs-lookup"><span data-stu-id="0c18a-106">You can use this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="0c18a-107">وعادة ما تُنفذ هذه المهمة عن طريق مدير شراء.</span><span class="sxs-lookup"><span data-stu-id="0c18a-107">This task would typically be carried out by a Purchasing manager.</span></span>

1. <span data-ttu-id="0c18a-108">انتقل إلى إدارة معلومات المنتج > المنتجات > المنتجات الصادرة.</span><span class="sxs-lookup"><span data-stu-id="0c18a-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="0c18a-109">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="0c18a-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="0c18a-110">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="0c18a-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="0c18a-111">توسيع القسم "الشراء".</span><span class="sxs-lookup"><span data-stu-id="0c18a-111">Expand the Purchase section.</span></span>
    * <span data-ttu-id="0c18a-112">في حالة وجود مورد رئيسي معروض في حقل المورد، فإنك تحتاج إلى إضافة هذا المورد كمورد معتمد بالخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="0c18a-112">If there is a primary vendor shown in the Vendor field, then you need to add this vendor as an approved vendor in the following steps.</span></span> <span data-ttu-id="0c18a-113">دون ملاحظة عن رقم المورد، في حالة ظهور أحدهم.</span><span class="sxs-lookup"><span data-stu-id="0c18a-113">Make a note of the vendor number, if one is shown.</span></span>  
5. <span data-ttu-id="0c18a-114">في جزء الإجراءات، انقر فوق "شراء".</span><span class="sxs-lookup"><span data-stu-id="0c18a-114">On the Action Pane, click Purchase.</span></span>
6. <span data-ttu-id="0c18a-115">انقر فوق إعداد.</span><span class="sxs-lookup"><span data-stu-id="0c18a-115">Click Setup.</span></span>
7. <span data-ttu-id="0c18a-116">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="0c18a-116">Click Add.</span></span>
8. <span data-ttu-id="0c18a-117">في الحقل "مورد"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="0c18a-117">In the Vendor field, enter or select a value.</span></span>
    * <span data-ttu-id="0c18a-118">حدد المورد المعتمد.</span><span class="sxs-lookup"><span data-stu-id="0c18a-118">Select the approved vendor.</span></span> <span data-ttu-id="0c18a-119">يجب أن يكون بند واحد من البنود على الأقل المورد الأساسي إذا كان هناك واحدًا في سجل المنتج.</span><span class="sxs-lookup"><span data-stu-id="0c18a-119">At least one of the lines has to be the primary vendor if there was one in the product record.</span></span> <span data-ttu-id="0c18a-120">إذا قمت بتدوين ملاحظة برقم المورد في وقت سابق، حدده هنا.</span><span class="sxs-lookup"><span data-stu-id="0c18a-120">If you made a note of the vendor number earlier, select it here.</span></span>  
9. <span data-ttu-id="0c18a-121">في الحقل "تاريخ انتهاء الصلاحية"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="0c18a-121">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="0c18a-122">اختر تاريخًا بعد بضعة أشهر قادمة.</span><span class="sxs-lookup"><span data-stu-id="0c18a-122">Choose a date a that is a few months ahead.</span></span>  
10. <span data-ttu-id="0c18a-123">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="0c18a-123">Click Add.</span></span>
11. <span data-ttu-id="0c18a-124">في الحقل "مورد"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="0c18a-124">In the Vendor field, enter or select a value.</span></span>
12. <span data-ttu-id="0c18a-125">في الحقل "تاريخ انتهاء الصلاحية"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="0c18a-125">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="0c18a-126">اختر تاريخًا يختلف عن تاريخ انتهاء الصلاحية السابق.</span><span class="sxs-lookup"><span data-stu-id="0c18a-126">Choose a date that is different than the previous expiration date.</span></span>  
13. <span data-ttu-id="0c18a-127">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0c18a-127">Close the page.</span></span>
14. <span data-ttu-id="0c18a-128">انقر فوق المورِّدين المعتمَدين.</span><span class="sxs-lookup"><span data-stu-id="0c18a-128">Click Approved vendors.</span></span>
15. <span data-ttu-id="0c18a-129">في الحقل "تاريخ انتهاء الصلاحية"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="0c18a-129">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="0c18a-130">هذا التاريخ بمثابة عامل تصفية لذلك فإنه يمكنك رؤية من هم الموردين المعتمدين، حتى تاريخ معين.</span><span class="sxs-lookup"><span data-stu-id="0c18a-130">This date acts as a filter so you can see who the approved vendors are, up to a certain date.</span></span>  
16. <span data-ttu-id="0c18a-131">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0c18a-131">Close the page.</span></span>
17. <span data-ttu-id="0c18a-132">انقر فوق الفترة الفعالة.</span><span class="sxs-lookup"><span data-stu-id="0c18a-132">Click Effective period.</span></span>
18. <span data-ttu-id="0c18a-133">في الحقل إظهار صلاحية الموردين المنتهية صلاحيتهم حسب"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="0c18a-133">In the Show vendors expired by field, enter a date.</span></span>
    * <span data-ttu-id="0c18a-134">يمكنك استخدام هذه الصفحة لتحديد الموردين حيث ستنتهي حالة الموافقة بعد تاريخ معين.</span><span class="sxs-lookup"><span data-stu-id="0c18a-134">You can use this page to identify vendors where the approval status will expire after a certain date.</span></span>  
19. <span data-ttu-id="0c18a-135">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0c18a-135">Close the page.</span></span>
20. <span data-ttu-id="0c18a-136">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="0c18a-136">Click Edit.</span></span>
21. <span data-ttu-id="0c18a-137">في الحقل "أسلوب التحقق من المورد المعتمد"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="0c18a-137">In the Approved vendor check method field, select an option.</span></span>
    * <span data-ttu-id="0c18a-138">يسمح لك هذا الحقل بتحديد السياسة لما ينبغي أن يحدث إذا تمت إضافة المنتج إلى بند أمر الشراء حيث لا يكون المورد مورد معتمد.</span><span class="sxs-lookup"><span data-stu-id="0c18a-138">This field allows you to select the policy for what should happen if the product is added to a purchase order line where the vendor is not an approved vendor.</span></span>  
22. <span data-ttu-id="0c18a-139">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="0c18a-139">Click Save.</span></span>
23. <span data-ttu-id="0c18a-140">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0c18a-140">Close the page.</span></span>
24. <span data-ttu-id="0c18a-141">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0c18a-141">Close the page.</span></span>
25. <span data-ttu-id="0c18a-142">انتقل إلى التدبير وتحديد الموار > الموردون > علاقات المورد/الصنف‬ > قائمة المورِّدين المعتمدَين حسب الصنف.</span><span class="sxs-lookup"><span data-stu-id="0c18a-142">Go to Procurement and sourcing > Vendors > Vendor/item relations > Approved vendor list by item.</span></span>
    * <span data-ttu-id="0c18a-143">تقدم لك هذه الصفحة نظرة عامة حول كافة المنتجات والموردين المعتمدين.</span><span class="sxs-lookup"><span data-stu-id="0c18a-143">This page gives you an overview of all products and the approved vendors.</span></span>  
26. <span data-ttu-id="0c18a-144">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0c18a-144">Close the page.</span></span>
27. <span data-ttu-id="0c18a-145">انتقل إلى ‏‫التدبير والتوريد > الموردون > جميع الموردين.</span><span class="sxs-lookup"><span data-stu-id="0c18a-145">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
    * <span data-ttu-id="0c18a-146">يمكنك أيضًا البدء من مورد ثم الانتقال إلى قائمة المنتجات المعتمدة لحساب المورد هذا.</span><span class="sxs-lookup"><span data-stu-id="0c18a-146">You can also start from a vendor and then go to the list of approved products for that vendor account.</span></span>  
28. <span data-ttu-id="0c18a-147">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="0c18a-147">In the list, find and select the desired record.</span></span>
29. <span data-ttu-id="0c18a-148">في جزء الإجراءات، انقر فوق التدبير.</span><span class="sxs-lookup"><span data-stu-id="0c18a-148">On the Action Pane, click Procurement.</span></span>
30. <span data-ttu-id="0c18a-149">انقر فوق قائمة المورِّد المعتمد حسب المورِّد.</span><span class="sxs-lookup"><span data-stu-id="0c18a-149">Click Approved vendor list by vendor.</span></span>
31. <span data-ttu-id="0c18a-150">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0c18a-150">Close the page.</span></span>
32. <span data-ttu-id="0c18a-151">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0c18a-151">Close the page.</span></span>

