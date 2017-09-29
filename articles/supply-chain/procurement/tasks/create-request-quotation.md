--- 
title: "إنشاء طلب لعرض الأسعار"
description: "يوضح هذا الإجراء كيفية إنشاء طلب عرض أسعار."
author: mkirknel
manager: AnnBe
ms.date: 11/02/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 331f516f3483acd79be4ef7b95b53adcfbef1ae2
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-request-for-quotation"></a><span data-ttu-id="00565-103">إنشاء طلب لعرض الأسعار</span><span class="sxs-lookup"><span data-stu-id="00565-103">Create a request for quotation</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="00565-104">يوضح هذا الإجراء كيفية إنشاء طلب عرض أسعار.</span><span class="sxs-lookup"><span data-stu-id="00565-104">This procedure shows you how to create a request for quotation.</span></span> <span data-ttu-id="00565-105">يتم إجراء هذا عادة عن طريق وكيل شراء.</span><span class="sxs-lookup"><span data-stu-id="00565-105">This would typically be done by a purchasing agent.</span></span> <span data-ttu-id="00565-106">يمكنك استخدام هذا الإجراء في شركة بيانات العرض التقديمي USMF، أو في البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="00565-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="00565-107">إنك بحاجة إلى إعداد أنواع الطلبات قبل البدء.</span><span class="sxs-lookup"><span data-stu-id="00565-107">You need to have set up solicitation types before you start.</span></span> <span data-ttu-id="00565-108">بمجرد إكمال هذه المهمة وإنشاء وإرسال RFQ، فإنه يمكنك حينها إدخال ردود كل مورد ومقارنتها ومنح العقد.</span><span class="sxs-lookup"><span data-stu-id="00565-108">Once you’ve completed this task and you’ve created and sent an RFQ you can then enter the replies per vendor, compare them, and award the contract.</span></span>


## <a name="prepare-a-new-rfq"></a><span data-ttu-id="00565-109">إعداد RFQ جديد</span><span class="sxs-lookup"><span data-stu-id="00565-109">Prepare a new RFQ</span></span>
1. <span data-ttu-id="00565-110">انتقل إلى التدبير وتحديد الموارد > طلبات عروض الأسعار‬ > كل طلبات عروض الأسعار‬.</span><span class="sxs-lookup"><span data-stu-id="00565-110">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="00565-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="00565-111">Click New.</span></span>
    * <span data-ttu-id="00565-112">تتوفر أنواع الشراء التالية: أمر الشراء (هذا هو الإعداد الافتراضي): مستند يؤكد عرض بشراء المنتجات أو قبول عرض ببيع المنتجات مقابل أجر.</span><span class="sxs-lookup"><span data-stu-id="00565-112">The following purchase types are available: Purchase order (this is the default): a document that confirms the offer to buy products, or the acceptance of an offer to sell products in exchange for payment.</span></span> <span data-ttu-id="00565-113">طلب الشراء: يتم تحديد هذا النوع تلقائيًا إذا قمت بإنشاء RFQ مباشرةً من طلب الشراء.</span><span class="sxs-lookup"><span data-stu-id="00565-113">Purchase requisition: this type is automatically selected if you create an RFQ directly from a purchase requisition.</span></span> <span data-ttu-id="00565-114">إذا قمت بتحديد هذا الاختبار يدويًا، فستحصل على خطأ.</span><span class="sxs-lookup"><span data-stu-id="00565-114">If you manually select this option, you’ll get an error.</span></span> <span data-ttu-id="00565-115">اتفاقية الشراء: اتفاقية بشراء كمية محددة أو قيمة منتج بمرور الوقت.</span><span class="sxs-lookup"><span data-stu-id="00565-115">Purchase agreement: an agreement to purchase a specific quantity or value of product over time.</span></span> <span data-ttu-id="00565-116">إذا قمت بتحديد هذا الخيار، فإنه يجب عليك تحديد نطاق التاريخ الذي ينطبق على اتفاقية الشراء.</span><span class="sxs-lookup"><span data-stu-id="00565-116">If you select this option, you must select the date range that applies to the purchase agreement.</span></span>  
3. <span data-ttu-id="00565-117">في حقل "‏‫عنوان المستند"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="00565-117">In the Document title field, type a value.</span></span>
4. <span data-ttu-id="00565-118">في الحقل "نوع الطلب"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="00565-118">In the Solicitation type field, enter or select a value.</span></span>
    * <span data-ttu-id="00565-119">إذا كان أسلوب النقاط مرتبطًا بنوع الطلب، ستكون هذه هي طريقة تسجيل النقاط الافتراضية لـ RFQ الذي تقوم بإنشائه.</span><span class="sxs-lookup"><span data-stu-id="00565-119">If a scoring method is associated with the solicitation type, this will be the default scoring method for the RFQ that you’re creating.</span></span> <span data-ttu-id="00565-120">من الممكن تغيير طريقة تسجيل النقاط فيما بعد.</span><span class="sxs-lookup"><span data-stu-id="00565-120">It is possible to change the scoring method later.</span></span>  
    * <span data-ttu-id="00565-121">في حقل "‏‫تاريخ التسليم‬"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="00565-121">In the Delivery date field, enter a date.</span></span>  
    * <span data-ttu-id="00565-122">حدد التاريخ الذي تريد استلام الأصناف المطلوبة فيه.</span><span class="sxs-lookup"><span data-stu-id="00565-122">Select the date by which you want to receive the items.</span></span>  
    * <span data-ttu-id="00565-123">في الحقل "تاريخ ووقت انتهاء الصلاحية"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="00565-123">In the Expiration date and time field, enter a date and time.</span></span>  
    * <span data-ttu-id="00565-124">حدد التاريخ والوقت الذيين يجب أن يستجيب الموردين فيهما على RFQ.</span><span class="sxs-lookup"><span data-stu-id="00565-124">Specify the date and time by which vendors must respond to the RFQ.</span></span>  
5. <span data-ttu-id="00565-125">في الحقل "المستودع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="00565-125">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="00565-126">سيكون عنوان المستودع هو العنوان الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="00565-126">The delivery address will default to the warehouse address.</span></span>  
6. <span data-ttu-id="00565-127">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="00565-127">Click OK.</span></span>

## <a name="add-lines"></a><span data-ttu-id="00565-128">إضافة بنود</span><span class="sxs-lookup"><span data-stu-id="00565-128">Add lines</span></span>
    * <span data-ttu-id="00565-129">بعد أن قمت بتحديده المعلومات الأساسية حول طلب عرض الأسعار الخاص بك، يمكنك تحديد السلع أو الخدمات التي تريد من الموردين تقديم عطاءات لها.</span><span class="sxs-lookup"><span data-stu-id="00565-129">After you’ve specified the basic information about your RFQ, you specify the goods or services that you want vendors to bid on.</span></span> <span data-ttu-id="00565-130">يُعد العنصر هو نوع الصنف الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="00565-130">Item is the default line type.</span></span>   
1. <span data-ttu-id="00565-131">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="00565-131">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="00565-132">إذا كنت تستخدم USMF، فإنه يمكنك تحديد T0020.</span><span class="sxs-lookup"><span data-stu-id="00565-132">If you're using USMF, you can select T0020.</span></span>  
2. <span data-ttu-id="00565-133">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="00565-133">In the Quantity field, enter a number.</span></span>
3. <span data-ttu-id="00565-134">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="00565-134">Click Add line.</span></span>
4. <span data-ttu-id="00565-135">في حقل "نوع البند"، حدد فئة.</span><span class="sxs-lookup"><span data-stu-id="00565-135">In the Line type field, select 'Category'.</span></span>
    * <span data-ttu-id="00565-136">يمكنك استخدام نوع سطر الفئة لإنشاء طلبات RFQ لبضائع غير مخزونة أو خدمات.</span><span class="sxs-lookup"><span data-stu-id="00565-136">You can use the Category line type to create RFQs for non-inventory goods or services.</span></span> <span data-ttu-id="00565-137">ثم تحتاج إلى تحديد نوع البضائع أو الخدمات من التسلسل الهرمي لكتالوجات التدبير.</span><span class="sxs-lookup"><span data-stu-id="00565-137">You then need to select the type of goods or services from a hierarchy of procurement categories.</span></span>  
5. <span data-ttu-id="00565-138">في الحقل "فئة التدبير"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="00565-138">In the Procurement category field, enter or select a value.</span></span>
6. <span data-ttu-id="00565-139">في الحقل "اسم المنتج"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="00565-139">In the Product name field, type a value.</span></span>
7. <span data-ttu-id="00565-140">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="00565-140">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="00565-141">في الحقل "وحدة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="00565-141">In the Unit field, enter or select a value.</span></span>

## <a name="add-vendors"></a><span data-ttu-id="00565-142">إضافة مورّدون</span><span class="sxs-lookup"><span data-stu-id="00565-142">Add vendors</span></span>
1. <span data-ttu-id="00565-143">انقر فوق العنوان للتغيير من عرض الخطوط إلى عرض العنوان.</span><span class="sxs-lookup"><span data-stu-id="00565-143">Click Header to change from the Lines view to the Header view.</span></span> 
2. <span data-ttu-id="00565-144">قم بتوسيع قسم المورد.</span><span class="sxs-lookup"><span data-stu-id="00565-144">Expand the Vendor section.</span></span>
3. <span data-ttu-id="00565-145">انقر فوق إضافة المورّدين تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="00565-145">Click Auto-add vendors.</span></span>
    * <span data-ttu-id="00565-146">يمكنك إضافة موردين إلى RFQ تلقائيًا، استناداً إلى فئة تدبير الأصناف المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="00565-146">You can add vendors to the RFQ automatically, based on the procurement category of the items requested.</span></span> <span data-ttu-id="00565-147">إذا لم يكن هناك أي موردين معتمدين للفئات المدرجة في البنود، يمكنك إضافة الموردين يدويًا.</span><span class="sxs-lookup"><span data-stu-id="00565-147">If there are no vendors approved for the categories included in the lines you can add vendors manually.</span></span>  
4. <span data-ttu-id="00565-148">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="00565-148">Click Add.</span></span>
5. <span data-ttu-id="00565-149">في الحقل "حساب المورد"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="00565-149">In the Vendor account field, enter or select a value.</span></span>
6. <span data-ttu-id="00565-150">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="00565-150">Click Add.</span></span>
7. <span data-ttu-id="00565-151">في الحقل "حساب المورد"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="00565-151">In the Vendor account field, enter or select a value.</span></span>
    * <span data-ttu-id="00565-152">بمجرد تحديد مورد، يتم إنشاء الحالة.</span><span class="sxs-lookup"><span data-stu-id="00565-152">Once you’ve selected a vendor, the status is Created.</span></span> <span data-ttu-id="00565-153">هذا يعني أنه قد تم حفظ معلومات المورد في RFQ، ولكنك لم ترسل الـ RFQ إلى المورد.</span><span class="sxs-lookup"><span data-stu-id="00565-153">This means that the vendor information has been saved in the RFQ, but you have not sent the RFQ to the vendor.</span></span> <span data-ttu-id="00565-154">يمكنك إضافة مورد إلى RFQ بغض النظر عن حالة المورد.</span><span class="sxs-lookup"><span data-stu-id="00565-154">You can add a vendor to an RFQ regardless of the vendor status.</span></span>  

## <a name="send-the-rfq-to-vendors"></a><span data-ttu-id="00565-155">إرسال RFQ للموردين</span><span class="sxs-lookup"><span data-stu-id="00565-155">Send the RFQ to vendors</span></span>
1. <span data-ttu-id="00565-156">انقر فوق "إرسال".</span><span class="sxs-lookup"><span data-stu-id="00565-156">Click Send.</span></span>
    * <span data-ttu-id="00565-157">في صفحة إرسال طلب عرض أسعار، تحقق من أن الموردين في القائمة هم من تريد أن يتلقوا RFQ.</span><span class="sxs-lookup"><span data-stu-id="00565-157">In the Sending request for quotation page, check that the vendors in the list are the ones that you want to receive the RFQ.</span></span>  
2. <span data-ttu-id="00565-158">انقر فوق طباعة.</span><span class="sxs-lookup"><span data-stu-id="00565-158">Click Print.</span></span>
    * <span data-ttu-id="00565-159">يسمح لك مربع الحوار بطباعة RFQ.</span><span class="sxs-lookup"><span data-stu-id="00565-159">This dialog allows you to print the RFQ.</span></span> <span data-ttu-id="00565-160">إذا قمت باختيار طباعة ورقة رد، فإنه يتم تحديد محتويات هذا في محددات التدبير والتوريد.</span><span class="sxs-lookup"><span data-stu-id="00565-160">If you choose to print a reply sheet, the contents of this are defined in Procurement and Sourcing parameters.</span></span> <span data-ttu-id="00565-161">لاختيار كيفية طباعة كشوف الرد، بمجرد أن يتم فتح مربع الحوار طباعة، انقر فوق خيارات الطباعة المتقدمة.</span><span class="sxs-lookup"><span data-stu-id="00565-161">To choose how to print reply sheets, once you’ve opened the Print dialog, click Advanced printing options.</span></span> <span data-ttu-id="00565-162">ستتم طباعة RFQ واحد لكل مورد يحتوي على البنود التي تكون بحالة تم الإنشاء أو مرسل.</span><span class="sxs-lookup"><span data-stu-id="00565-162">One RFQ will be printed for each vendor containing the lines that have the status of Created or Sent.</span></span> <span data-ttu-id="00565-163">لن تتم طباعة البنود الملغية والبنود ذات البنود المسجلة.</span><span class="sxs-lookup"><span data-stu-id="00565-163">Canceled lines and lines with registered replies will not be printed.</span></span>   
3. <span data-ttu-id="00565-164">انقر فوق "إلغاء".</span><span class="sxs-lookup"><span data-stu-id="00565-164">Click Cancel.</span></span>
4. <span data-ttu-id="00565-165">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="00565-165">Click OK.</span></span>
5. <span data-ttu-id="00565-166">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="00565-166">Close the page.</span></span>
6. <span data-ttu-id="00565-167">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="00565-167">Close the page.</span></span>

## <a name="view-the-rfq-journal"></a><span data-ttu-id="00565-168">عرض دفتر يومية RFQ</span><span class="sxs-lookup"><span data-stu-id="00565-168">View the RFQ journal</span></span>
1. <span data-ttu-id="00565-169">انتقل إلى التدبير وتحديد الموارد > طلبات عروض الأسعار > طلب متابعة عروض الأسعار > طلب دفاتر يومية عروض الأسعار.</span><span class="sxs-lookup"><span data-stu-id="00565-169">Go to Procurement and sourcing > Requests for quotations > Request for quotations follow-up > Request for quotation journals.</span></span>
2. <span data-ttu-id="00565-170">انقر فوق معاينة/طباعة.</span><span class="sxs-lookup"><span data-stu-id="00565-170">Click Preview/Print.</span></span>
3. <span data-ttu-id="00565-171">انقر فوق "معاينة الأصل".</span><span class="sxs-lookup"><span data-stu-id="00565-171">Click Original preview.</span></span>
4. <span data-ttu-id="00565-172">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="00565-172">Close the page.</span></span>
5. <span data-ttu-id="00565-173">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="00565-173">Close the page.</span></span>


