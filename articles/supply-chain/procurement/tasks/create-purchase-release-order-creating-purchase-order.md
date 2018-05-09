--- 
title: "إنشاء أمر إصدار شراء عند إنشاء أمر الشراء"
description: "يوضح هذا الإجراء كيفية استخدام اتفاقية شراء عند إنشاء أمر شراء."
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2a5fde13fac7f0523c098f750d897ca5da06473b
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-purchase-release-order-when-creating-the-purchase-order"></a><span data-ttu-id="c8a01-103">إنشاء أمر إصدار شراء عند إنشاء أمر الشراء</span><span class="sxs-lookup"><span data-stu-id="c8a01-103">Create a purchase release order when creating the purchase order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c8a01-104">يوضح هذا الإجراء كيفية استخدام اتفاقية شراء عند إنشاء أمر شراء.</span><span class="sxs-lookup"><span data-stu-id="c8a01-104">This procedure shows how to use a purchase agreement when you create a purchase order.</span></span> <span data-ttu-id="c8a01-105">يجب تطبيق اتفاقية الشراء هذه عند إنشاء أمر الشراء لأن هناك شروط عامة يجب نسخها إلى رأس أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="c8a01-105">The purchase agreement has to be applied when you create the purchase order because there are general terms that should be copied to the purchase order header.</span></span> <span data-ttu-id="c8a01-106">وعادة ما تُنفذ هذه المهمة عن طريق وكيل شراء.</span><span class="sxs-lookup"><span data-stu-id="c8a01-106">Typically this task would be carried out by a purchasing agent.</span></span> <span data-ttu-id="c8a01-107">كمتطلب أساسي لهذا الدليل، يجب أن يكون لديك اتفاقية شراء فعالة مع التزام كمية منتج لأحد الموردين والأصناف.</span><span class="sxs-lookup"><span data-stu-id="c8a01-107">As a prerequisite for this guide, you must have an effective purchase agreement with a product quantity commitment for a vendor and items.</span></span> <span data-ttu-id="c8a01-108">يمكن استخدام نفس الإجراء إذا كانت لديك اتفاقية شراء بأنواع أخرى من الالتزامات.</span><span class="sxs-lookup"><span data-stu-id="c8a01-108">The same procedure can be used if you have a purchase agreement with other types of commitments.</span></span> <span data-ttu-id="c8a01-109">يمكنك تنفيذ هذا الدليل في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="c8a01-109">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="c8a01-110">إذا كنت تستخدم USMF، يمكنك تشغيل الدليل "إنشاء اتفاقية شراء" أولاً لإعداد الشروط المسبقة اللازمة لهذا الدليل.</span><span class="sxs-lookup"><span data-stu-id="c8a01-110">If you’re using USMF, you can run the “Create a purchase agreement” guide first to set up the necessary preconditions for this guide.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="c8a01-111">إنشاء أمر شراء</span><span class="sxs-lookup"><span data-stu-id="c8a01-111">Create a purchase order</span></span>
1. <span data-ttu-id="c8a01-112">افتح مساحة عمل إعداد أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="c8a01-112">Open the purchase order preparation workspace.</span></span>
2. <span data-ttu-id="c8a01-113">انقر فوق "أمر شراء جديد".</span><span class="sxs-lookup"><span data-stu-id="c8a01-113">Click New purchase order.</span></span>
3. <span data-ttu-id="c8a01-114">في الحقل "حساب المورّد‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="c8a01-114">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="c8a01-115">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c8a01-115">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="c8a01-116">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c8a01-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="c8a01-117">بدّل توسيع المقطع "عام".</span><span class="sxs-lookup"><span data-stu-id="c8a01-117">Toggle the expansion of the General section.</span></span>
7. <span data-ttu-id="c8a01-118">في الحقل "اتفاقيات الشراء"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="c8a01-118">In the Purchase agreement field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c8a01-119">يتم هنا سرد جميع الاتفاقيات المتوفرة للمورد.</span><span class="sxs-lookup"><span data-stu-id="c8a01-119">All available agreements for the vendor are listed here.</span></span> <span data-ttu-id="c8a01-120">ابحث عن الاتفاقية الفعالة التي تريد استخدامها.</span><span class="sxs-lookup"><span data-stu-id="c8a01-120">Find the effective agreement that you want to use.</span></span>  
8. <span data-ttu-id="c8a01-121">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c8a01-121">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="c8a01-122">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="c8a01-122">Click Yes.</span></span>
10. <span data-ttu-id="c8a01-123">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c8a01-123">Click OK.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="c8a01-124">إضافة بند</span><span class="sxs-lookup"><span data-stu-id="c8a01-124">Add a line</span></span>
1. <span data-ttu-id="c8a01-125">في الحقل "رقم الصنف" اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c8a01-125">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="c8a01-126">إذا كانت هناك أبعاد معينة للمخزون أو الموقع خاصة بالالتزام، فعليك إدخال نفس القيم في بند أمر الشراء لاستخدام الاتفاقية.</span><span class="sxs-lookup"><span data-stu-id="c8a01-126">If there are specific inventory or location dimensions on the commitment you must enter the same values on the purchase order line to make use of the agreement.</span></span>  
2. <span data-ttu-id="c8a01-127">في الحقل "الموقع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="c8a01-127">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c8a01-128">قد يتم ملء الموقع بالفعل بالقيمة الافتراضية من الأمر أو من المورد.</span><span class="sxs-lookup"><span data-stu-id="c8a01-128">The site may already be populated with the default value from the order, or from the vendor.</span></span> <span data-ttu-id="c8a01-129">إذا كانت هذه هي الحالة، فقم بتخطي هذه الخطوة.</span><span class="sxs-lookup"><span data-stu-id="c8a01-129">If this is the case, skip this step.</span></span>  
3. <span data-ttu-id="c8a01-130">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c8a01-130">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="c8a01-131">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c8a01-131">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="c8a01-132">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="c8a01-132">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="c8a01-133">تحقق من صحة نسخ السعر من الالتزام.</span><span class="sxs-lookup"><span data-stu-id="c8a01-133">Validate that the price is copied from the commitment.</span></span>  

## <a name="look-up-the-commitment"></a><span data-ttu-id="c8a01-134">البحث عن الالتزام</span><span class="sxs-lookup"><span data-stu-id="c8a01-134">Look up the commitment</span></span>
1. <span data-ttu-id="c8a01-135">انقر فوق "تحديث البند".</span><span class="sxs-lookup"><span data-stu-id="c8a01-135">Click Update line.</span></span>
2. <span data-ttu-id="c8a01-136">انقر فوق "تم الإرفاق".</span><span class="sxs-lookup"><span data-stu-id="c8a01-136">Click Attached.</span></span>
    * <span data-ttu-id="c8a01-137">هنا يمكنك الحصول على تفاصيل اتفاقية الشراء.</span><span class="sxs-lookup"><span data-stu-id="c8a01-137">Here you can get details for the purchase agreement.</span></span> <span data-ttu-id="c8a01-138">على سبيل المثال، يمكنك أن ترى السعر وما إذا كانت السعر والخصم ثابتين، وهو ما يعني أنه إذا قمت بتغيير السعر أو الخصم في أمر الشراء إلى قيمة مختلفة عما هو محدد في الالتزام، فسيقوم النظام بإزالة الارتباط حتى لا يفي بند أمر الشراء بالالتزام.</span><span class="sxs-lookup"><span data-stu-id="c8a01-138">For example, you can see the price and whether the price and discount are fixed, which means that if you change price or discount on the purchase order to a different value than on the commitment, the system will remove the link so the purchase order line does not fulfill the commitment.</span></span> <span data-ttu-id="c8a01-139">ويمكنك أيضا الاطلاع على ما إذا كان الخيار "الحد الأقصى مفروض" محددًا، وهو ما يعني أنه لا يمكن تجاوز الكمية المحددة بالالتزام من خلال جمع كافة المشتريات التي تفي بالالتزام.</span><span class="sxs-lookup"><span data-stu-id="c8a01-139">You can also see if the Max is enforced option is selected, which means that the quantity on the commitment cannot be exceeded by summing all of the purchases that fulfill the commitment.</span></span>  
3. <span data-ttu-id="c8a01-140">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c8a01-140">Close the page.</span></span>

## <a name="look-up-the-purchase-agreement"></a><span data-ttu-id="c8a01-141">البحث عن اتفاقية الشراء</span><span class="sxs-lookup"><span data-stu-id="c8a01-141">Look up the purchase agreement</span></span>
1. <span data-ttu-id="c8a01-142">في جزء "الإجراءات"، انقر فوق "عام".</span><span class="sxs-lookup"><span data-stu-id="c8a01-142">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="c8a01-143">انقر فوق "اتفاقية الشراء".</span><span class="sxs-lookup"><span data-stu-id="c8a01-143">Click Purchase agreement.</span></span>
3. <span data-ttu-id="c8a01-144">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c8a01-144">Close the page.</span></span>
4. <span data-ttu-id="c8a01-145">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c8a01-145">Close the page.</span></span>


