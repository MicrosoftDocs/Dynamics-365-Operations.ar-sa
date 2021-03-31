---
title: إنشاء طلب لعرض الأسعار
description: يوضح هذا الإجراء كيفية إنشاء طلب عرض أسعار.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, PurchCreateRFQCase, InventLocationIdLookup, PurchRFQCaseTable, InventItemIdLookupSimple, EcoResCategorySingleLookup, UnitOfMeasureLookup, PurchRFQEditLines, PurchRFQEditLinesPrintOptions, VendRFQJournal, SrsReportViewerForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cc3646fb9b66fa926a9532696414943fc1345b75
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211876"
---
# <a name="create-a-request-for-quotation"></a><span data-ttu-id="31cc8-103">إنشاء طلب لعرض الأسعار</span><span class="sxs-lookup"><span data-stu-id="31cc8-103">Create a request for quotation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="31cc8-104">يوضح هذا الإجراء كيفية إنشاء طلب عرض أسعار.</span><span class="sxs-lookup"><span data-stu-id="31cc8-104">This procedure shows you how to create a request for quotation.</span></span> <span data-ttu-id="31cc8-105">يتم إجراء هذا عادة عن طريق وكيل شراء.</span><span class="sxs-lookup"><span data-stu-id="31cc8-105">This would typically be done by a purchasing agent.</span></span> <span data-ttu-id="31cc8-106">يمكنك استخدام هذا الإجراء في شركة بيانات العرض التقديمي USMF، أو في البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="31cc8-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="31cc8-107">إنك بحاجة إلى إعداد أنواع الطلبات قبل البدء.</span><span class="sxs-lookup"><span data-stu-id="31cc8-107">You need to have set up solicitation types before you start.</span></span> <span data-ttu-id="31cc8-108">بمجرد إكمال هذه المهمة وإنشاء وإرسال RFQ، فإنه يمكنك حينها إدخال ردود كل مورد ومقارنتها ومنح العقد.</span><span class="sxs-lookup"><span data-stu-id="31cc8-108">Once you've completed this task and you've created and sent an RFQ you can then enter the replies per vendor, compare them, and award the contract.</span></span>


## <a name="prepare-a-new-rfq"></a><span data-ttu-id="31cc8-109">إعداد RFQ جديد</span><span class="sxs-lookup"><span data-stu-id="31cc8-109">Prepare a new RFQ</span></span>
1. <span data-ttu-id="31cc8-110">انتقل إلى **جزء التنقل > الوحدات النمطية > التدبير والتوريد > طلبات عروض الأسعار > كل طلبات عروض الأسعار**‬.</span><span class="sxs-lookup"><span data-stu-id="31cc8-110">Go to **Navigation pane > Modules > Procurement and sourcing > Requests for quotations > All requests for quotations**.</span></span>
2. <span data-ttu-id="31cc8-111">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="31cc8-111">Click **New**.</span></span>
    <span data-ttu-id="31cc8-112">تتوفر أنواع الشراء التالية: أمر الشراء (هذا هو الإعداد الافتراضي): مستند يؤكد عرض بشراء المنتجات أو قبول عرض ببيع المنتجات مقابل أجر.</span><span class="sxs-lookup"><span data-stu-id="31cc8-112">The following purchase types are available: Purchase order (this is the default): a document that confirms the offer to buy products, or the acceptance of an offer to sell products in exchange for payment.</span></span> <span data-ttu-id="31cc8-113">طلب الشراء: يتم تحديد هذا النوع تلقائيًا إذا قمت بإنشاء RFQ مباشرةً من طلب الشراء.</span><span class="sxs-lookup"><span data-stu-id="31cc8-113">Purchase requisition: this type is automatically selected if you create an RFQ directly from a purchase requisition.</span></span> <span data-ttu-id="31cc8-114">إذا قمت بتحديد هذا الاختبار يدويًا، فستحصل على خطأ.</span><span class="sxs-lookup"><span data-stu-id="31cc8-114">If you manually select this option, you'll get an error.</span></span> <span data-ttu-id="31cc8-115">اتفاقية الشراء: اتفاقية بشراء كمية محددة أو قيمة منتج بمرور الوقت.</span><span class="sxs-lookup"><span data-stu-id="31cc8-115">Purchase agreement: an agreement to purchase a specific quantity or value of product over time.</span></span> <span data-ttu-id="31cc8-116">إذا قمت بتحديد هذا الخيار، فإنه يجب عليك تحديد نطاق التاريخ الذي ينطبق على اتفاقية الشراء.</span><span class="sxs-lookup"><span data-stu-id="31cc8-116">If you select this option, you must select the date range that applies to the purchase agreement.</span></span>  
3. <span data-ttu-id="31cc8-117">في حقل **عنوان المستند**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="31cc8-117">In the **Document title** field, type a value.</span></span>
4. <span data-ttu-id="31cc8-118">في الحقل **نوع الطلب**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="31cc8-118">In the **Solicitation type** field, enter or select a value.</span></span>
    + <span data-ttu-id="31cc8-119">إذا كان أسلوب النقاط مرتبطًا بنوع الطلب، ستكون هذه هي طريقة تسجيل النقاط الافتراضية لـ RFQ الذي تقوم بإنشائه.</span><span class="sxs-lookup"><span data-stu-id="31cc8-119">If a scoring method is associated with the solicitation type, this will be the default scoring method for the RFQ that you're creating.</span></span> <span data-ttu-id="31cc8-120">من الممكن تغيير طريقة تسجيل النقاط فيما بعد.</span><span class="sxs-lookup"><span data-stu-id="31cc8-120">It is possible to change the scoring method later.</span></span>  
    + <span data-ttu-id="31cc8-121">في حقل **‏‫تاريخ التسليم‬**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="31cc8-121">In the **Delivery date** field, enter a date.</span></span>  
    + <span data-ttu-id="31cc8-122">حدد التاريخ الذي تريد استلام الأصناف المطلوبة فيه.</span><span class="sxs-lookup"><span data-stu-id="31cc8-122">Select the date by which you want to receive the items.</span></span>  
    + <span data-ttu-id="31cc8-123">في الحقل **تاريخ ووقت انتهاء الصلاحية**، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="31cc8-123">In the **Expiration date and time** field, enter a date and time.</span></span>  
    + <span data-ttu-id="31cc8-124">حدد التاريخ والوقت الذيين يجب أن يستجيب الموردين فيهما على RFQ.</span><span class="sxs-lookup"><span data-stu-id="31cc8-124">Specify the date and time by which vendors must respond to the RFQ.</span></span>  
5. <span data-ttu-id="31cc8-125">في الحقل **المستودع**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="31cc8-125">In the **Warehouse field**, enter or select a value.</span></span> <span data-ttu-id="31cc8-126">سيكون عنوان المستودع هو العنوان الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="31cc8-126">The delivery address will default to the warehouse address.</span></span>  
6. <span data-ttu-id="31cc8-127">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="31cc8-127">Click **OK**.</span></span>

## <a name="add-lines"></a><span data-ttu-id="31cc8-128">إضافة بنود</span><span class="sxs-lookup"><span data-stu-id="31cc8-128">Add lines</span></span>

<span data-ttu-id="31cc8-129">بعد أن قمت بتحديده المعلومات الأساسية حول طلب عرض الأسعار الخاص بك، يمكنك تحديد السلع أو الخدمات التي تريد من الموردين تقديم عطاءات لها.</span><span class="sxs-lookup"><span data-stu-id="31cc8-129">After you've specified the basic information about your RFQ, you specify the goods or services that you want vendors to bid on.</span></span> <span data-ttu-id="31cc8-130">يُعد العنصر هو نوع الصنف الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="31cc8-130">Item is the default line type.</span></span>

1. <span data-ttu-id="31cc8-131">في الحقل **رقم الصنف**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="31cc8-131">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="31cc8-132">إذا كنت تستخدم USMF، فإنه يمكنك تحديد T0020.</span><span class="sxs-lookup"><span data-stu-id="31cc8-132">If you're using USMF, you can select T0020.</span></span>  
2. <span data-ttu-id="31cc8-133">في الحقل **الكمية**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="31cc8-133">In the **Quantity** field, enter a number.</span></span>
3. <span data-ttu-id="31cc8-134">انقر فوق **إضافة بند**.</span><span class="sxs-lookup"><span data-stu-id="31cc8-134">Click **Add line**.</span></span>
4. <span data-ttu-id="31cc8-135">في حقل **نوع البند**، حدد فئة.</span><span class="sxs-lookup"><span data-stu-id="31cc8-135">In the **Line type** field, select 'Category'.</span></span> <span data-ttu-id="31cc8-136">يمكنك استخدام نوع سطر الفئة لإنشاء طلبات RFQ لبضائع غير مخزونة أو خدمات.</span><span class="sxs-lookup"><span data-stu-id="31cc8-136">You can use the Category line type to create RFQs for non-inventory goods or services.</span></span> <span data-ttu-id="31cc8-137">ثم تحتاج إلى تحديد نوع البضائع أو الخدمات من التسلسل الهرمي لكتالوجات التدبير.</span><span class="sxs-lookup"><span data-stu-id="31cc8-137">You then need to select the type of goods or services from a hierarchy of procurement categories.</span></span>  
5. <span data-ttu-id="31cc8-138">في الحقل **فئة التدبير**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="31cc8-138">In the **Procurement category** field, enter or select a value.</span></span>
6. <span data-ttu-id="31cc8-139">في الحقل **اسم المنتج**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="31cc8-139">In the **Product name** field, type a value.</span></span>
7. <span data-ttu-id="31cc8-140">في الحقل **الكمية**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="31cc8-140">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="31cc8-141">في الحقل **وحدة**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="31cc8-141">In the **Unit** field, enter or select a value.</span></span>

## <a name="add-vendors"></a><span data-ttu-id="31cc8-142">إضافة مورّدون</span><span class="sxs-lookup"><span data-stu-id="31cc8-142">Add vendors</span></span>
1. <span data-ttu-id="31cc8-143">انقر فوق **الرأس** للتغيير من عرض الخطوط إلى عرض الرأس‬.</span><span class="sxs-lookup"><span data-stu-id="31cc8-143">Click **Header** to change from the Lines view to the Header view.</span></span> 
2. <span data-ttu-id="31cc8-144">قم بتوسيع قسم **المورد**.</span><span class="sxs-lookup"><span data-stu-id="31cc8-144">Expand the **Vendor** section.</span></span>
3. <span data-ttu-id="31cc8-145">انقر فوق **إضافة المورّدين تلقائيًا**.</span><span class="sxs-lookup"><span data-stu-id="31cc8-145">Click **Auto-add vendors**.</span></span> <span data-ttu-id="31cc8-146">يمكنك إضافة موردين إلى RFQ تلقائيًا، استناداً إلى فئة تدبير الأصناف المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="31cc8-146">You can add vendors to the RFQ automatically, based on the procurement category of the items requested.</span></span> <span data-ttu-id="31cc8-147">إذا لم يكن هناك أي موردين معتمدين للفئات المدرجة في البنود، يمكنك إضافة الموردين يدويًا.</span><span class="sxs-lookup"><span data-stu-id="31cc8-147">If there are no vendors approved for the categories included in the lines you can add vendors manually.</span></span>  
4. <span data-ttu-id="31cc8-148">انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="31cc8-148">Click **Add**.</span></span>
5. <span data-ttu-id="31cc8-149">في الحقل **حساب المورد**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="31cc8-149">In the **Vendor account** field, enter or select a value.</span></span>
6. <span data-ttu-id="31cc8-150">انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="31cc8-150">Click **Add**.</span></span>
7. <span data-ttu-id="31cc8-151">في الحقل **حساب المورد**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="31cc8-151">In the **Vendor account** field, enter or select a value.</span></span> <span data-ttu-id="31cc8-152">بمجرد تحديد مورد، يتم إنشاء الحالة.</span><span class="sxs-lookup"><span data-stu-id="31cc8-152">Once you've selected a vendor, the status is Created.</span></span> <span data-ttu-id="31cc8-153">هذا يعني أنه قد تم حفظ معلومات المورد في RFQ، ولكنك لم ترسل الـ RFQ إلى المورد.</span><span class="sxs-lookup"><span data-stu-id="31cc8-153">This means that the vendor information has been saved in the RFQ, but you have not sent the RFQ to the vendor.</span></span> <span data-ttu-id="31cc8-154">يمكنك إضافة مورد إلى RFQ بغض النظر عن حالة المورد.</span><span class="sxs-lookup"><span data-stu-id="31cc8-154">You can add a vendor to an RFQ regardless of the vendor status.</span></span>  

## <a name="send-the-rfq-to-vendors"></a><span data-ttu-id="31cc8-155">إرسال RFQ للموردين</span><span class="sxs-lookup"><span data-stu-id="31cc8-155">Send the RFQ to vendors</span></span>
1. <span data-ttu-id="31cc8-156">في **جزء الإجراءات**، انقر فوق **إرسال**.</span><span class="sxs-lookup"><span data-stu-id="31cc8-156">On the **Action Pane**, click **Send**.</span></span> <span data-ttu-id="31cc8-157">في صفحة إرسال طلب عرض أسعار، تحقق من أن الموردين في القائمة هم من تريد أن يتلقوا RFQ.</span><span class="sxs-lookup"><span data-stu-id="31cc8-157">In the Sending request for quotation page, check that the vendors in the list are the ones that you want to receive the RFQ.</span></span>  
2. <span data-ttu-id="31cc8-158">انقر فوق **طباعة**.</span><span class="sxs-lookup"><span data-stu-id="31cc8-158">Click **Print**.</span></span> <span data-ttu-id="31cc8-159">يسمح لك مربع الحوار بطباعة RFQ.</span><span class="sxs-lookup"><span data-stu-id="31cc8-159">This dialog allows you to print the RFQ.</span></span> <span data-ttu-id="31cc8-160">إذا قمت باختيار طباعة ورقة رد، فإنه يتم تحديد محتويات هذا في محددات التدبير والتوريد.</span><span class="sxs-lookup"><span data-stu-id="31cc8-160">If you choose to print a reply sheet, the contents of this are defined in Procurement and Sourcing parameters.</span></span> <span data-ttu-id="31cc8-161">لاختيار كيفية طباعة كشوف الرد، بمجرد أن يتم فتح مربع الحوار طباعة، انقر فوق خيارات الطباعة المتقدمة.</span><span class="sxs-lookup"><span data-stu-id="31cc8-161">To choose how to print reply sheets, once you've opened the Print dialog, click Advanced printing options.</span></span> <span data-ttu-id="31cc8-162">ستتم طباعة RFQ واحد لكل مورد يحتوي على البنود التي تكون بحالة تم الإنشاء أو مرسل.</span><span class="sxs-lookup"><span data-stu-id="31cc8-162">One RFQ will be printed for each vendor containing the lines that have the status of Created or Sent.</span></span> <span data-ttu-id="31cc8-163">لن تتم طباعة البنود الملغية والبنود ذات البنود المسجلة.</span><span class="sxs-lookup"><span data-stu-id="31cc8-163">Canceled lines and lines with registered replies will not be printed.</span></span>   
3. <span data-ttu-id="31cc8-164">وانقر فوق **إلغاء الأمر**.</span><span class="sxs-lookup"><span data-stu-id="31cc8-164">Click **Cancel**.</span></span>
4. <span data-ttu-id="31cc8-165">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="31cc8-165">Click **OK**.</span></span>
5. <span data-ttu-id="31cc8-166">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="31cc8-166">Close the page.</span></span>
6. <span data-ttu-id="31cc8-167">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="31cc8-167">Close the page.</span></span>

## <a name="view-the-rfq-journal"></a><span data-ttu-id="31cc8-168">عرض دفتر يومية RFQ</span><span class="sxs-lookup"><span data-stu-id="31cc8-168">View the RFQ journal</span></span>
1. <span data-ttu-id="31cc8-169">انتقل إلى **التدبير وتحديد الموارد > طلبات عروض الأسعار > طلب متابعة عروض الأسعار > طلب دفاتر يومية عروض الأسعار**.</span><span class="sxs-lookup"><span data-stu-id="31cc8-169">Go to **Procurement and sourcing > Requests for quotations > Request for quotations follow-up > Request for quotation journals**.</span></span>
2. <span data-ttu-id="31cc8-170">انقر فوق **معاينة/طباعة**.</span><span class="sxs-lookup"><span data-stu-id="31cc8-170">Click **Preview/Print**.</span></span>
3. <span data-ttu-id="31cc8-171">انقر فوق **معاينة الأصل**.</span><span class="sxs-lookup"><span data-stu-id="31cc8-171">Click **Original preview**.</span></span>
4. <span data-ttu-id="31cc8-172">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="31cc8-172">Close the page.</span></span>
5. <span data-ttu-id="31cc8-173">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="31cc8-173">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]