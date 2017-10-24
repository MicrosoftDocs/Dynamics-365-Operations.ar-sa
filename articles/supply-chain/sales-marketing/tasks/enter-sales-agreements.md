--- 
title: "إدخال اتفاقيات البيع"
description: "يوضح هذا الإجراء كيفية إنشاء اتفاقية بيع تلزم أحد العملاء بشراء منتج بمبلغ متفق عليه مع مرور الوقت مقابل الحصول على خصومات خاصة."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 8c11164f7edb8e05b93f3c58b9707c0bf2482228
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="enter-sales-agreements"></a><span data-ttu-id="fbb95-103">إدخال اتفاقيات البيع</span><span class="sxs-lookup"><span data-stu-id="fbb95-103">Enter sales agreements</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fbb95-104">يوضح لك هذا الإجراء كيفية إنشاء اتفاقية بيع تلزم أحد عملائك بشراء منتج بمبلغ</span><span class="sxs-lookup"><span data-stu-id="fbb95-104">This procedure shows you how to create a sales agreement that commits one of your customers to buy a product for an</span></span>

<span data-ttu-id="fbb95-105">متفق عليه مع مرور الوقت في مقابل الحصول على خصومات خاصة.</span><span class="sxs-lookup"><span data-stu-id="fbb95-105">agreed amount over time in exchange for special discounts.</span></span> <span data-ttu-id="fbb95-106">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF أو باستخدام بياناتك الخاصة.</span><span class="sxs-lookup"><span data-stu-id="fbb95-106">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-sales-agreement-header"></a><span data-ttu-id="fbb95-107">إعداد عنوان اتفاقية البيع</span><span class="sxs-lookup"><span data-stu-id="fbb95-107">Set up sales agreement header</span></span>
1. <span data-ttu-id="fbb95-108">انتقل إلى المبيعات والتسويق > اتفاقيات المبيعات > اتفاقية البيع.</span><span class="sxs-lookup"><span data-stu-id="fbb95-108">Go to Sales and marketing > Sales agreements > Sales agreements.</span></span>
2. <span data-ttu-id="fbb95-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="fbb95-109">Click New.</span></span>
3. <span data-ttu-id="fbb95-110">في الحقل "حساب العميل"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="fbb95-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="fbb95-111">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="fbb95-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="fbb95-112">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="fbb95-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="fbb95-113">في حقل "تصنيف اتفاقيات البيع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="fbb95-113">In the Sales agreement classification field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="fbb95-114">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="fbb95-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="fbb95-115">قم بتوسيع القسم "عام".</span><span class="sxs-lookup"><span data-stu-id="fbb95-115">Expand the General section.</span></span>
9. <span data-ttu-id="fbb95-116">في حقل "الالتزام الافتراضي"، حدد "‏‫الالتزام بقيمة المنتجات".</span><span class="sxs-lookup"><span data-stu-id="fbb95-116">In the Default commitment field, select 'Product value commitment'.</span></span>
    * <span data-ttu-id="fbb95-117">نوع الالتزام هو معيار إلزامي يجب عليك تعيينه إلى الاتفاقية لتحديد كيفية الوفاء بعقد الاتفاقية.</span><span class="sxs-lookup"><span data-stu-id="fbb95-117">A commitment type is a mandatory criterion that you must assign to the agreement to define how the agreement contract will be fulfilled.</span></span> <span data-ttu-id="fbb95-118">تمكنك الأنواع الاًربعة المحددة مسبقًا من إعداد هدف التزام العميل، الموضح ككمية أو قيمة.</span><span class="sxs-lookup"><span data-stu-id="fbb95-118">The four predefined types let you set up the customer's commitment target, expressed as a quantity or a value.</span></span> <span data-ttu-id="fbb95-119">ولا يمكن تطبيق نوع الالتزام بالكمية إلا لمنتج معين، ولكن الأنواع المعتمدة على القيمة قابلة للتطبيق على مبيعات المنتجات المحددة وغير المحددة.</span><span class="sxs-lookup"><span data-stu-id="fbb95-119">The quantity commitment type can only be applied to a specific product, but the value-based types are applicable to sales of both specific and non-specific products.</span></span>  
10. <span data-ttu-id="fbb95-120">في حقل "‏‫تاريخ انتهاء الصلاحية"، قم بتعيين التاريخ لتاريخ في المستقبل عندما ترغب في إنهاء صلاحية الاتفاقية.</span><span class="sxs-lookup"><span data-stu-id="fbb95-120">In the Expiration date field, set the date to a future date when you want the agreement to expire.</span></span>
11. <span data-ttu-id="fbb95-121">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="fbb95-121">Click OK.</span></span>

## <a name="set-up-product-value-commitment-lines"></a><span data-ttu-id="fbb95-122">إعداد بنود الالتزام بقيمة المنتجات</span><span class="sxs-lookup"><span data-stu-id="fbb95-122">Set up product value commitment lines</span></span>
1. <span data-ttu-id="fbb95-123">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="fbb95-123">Click Add line.</span></span>
2. <span data-ttu-id="fbb95-124">في الحقل "رقم الصنف"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="fbb95-124">In the Item number field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="fbb95-125">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="fbb95-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="fbb95-126">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="fbb95-126">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="fbb95-127">يؤثر نوع الالتزام الذي تم اختياره للاتفاقية على نوع المعلومات التي يمكنك إدخالها لبنود الاتفاقية.</span><span class="sxs-lookup"><span data-stu-id="fbb95-127">The type of commitment that you have chosen for the agreement affects the kind of information you can enter for the agreement lines.</span></span> <span data-ttu-id="fbb95-128">على سبيل المثال، بالنسبة للاتفاقية المعتمدة على القيمة، يجب تحديد المبلغ الصافي الإجمالي (بالعملة المتفق عليها) التي تلزم العميل بشراء سلع منك.</span><span class="sxs-lookup"><span data-stu-id="fbb95-128">For example, for a value-based agreement you must specify the total net amount (in the agreed currency) for which the customer commits to buys goods from you.</span></span> <span data-ttu-id="fbb95-129">في هذا المثال، لا يتوفر حقلا الكمية والوحدة في البند لأنك تقوم بإنشاء اتفاقية للعميل لشراء قيمة معينة للمنتج.</span><span class="sxs-lookup"><span data-stu-id="fbb95-129">In this example the Quantity and Unit fields on the line are unavailable because you’re creating an agreement for the customer to buy a specific value of a product.</span></span>   
5. <span data-ttu-id="fbb95-130">في حقل "المبلغ الصافي"، أدخل المبلغ النقدي الذي التزم العميل بشرائه.</span><span class="sxs-lookup"><span data-stu-id="fbb95-130">In the Net amount field, enter the monetary amount that the customer has committed to buying.</span></span>
6. <span data-ttu-id="fbb95-131">في حقل "نسبة الخصم"، أدخل قيمة النسبة مئوية التي سيتم تطبيقها على بنود أمر المبيعات الخاص بالعميل المرتبطة بهذه الاتفاقية.</span><span class="sxs-lookup"><span data-stu-id="fbb95-131">In the Discount percent field, enter a percentage value that will apply to the customer's sales order lines that are linked to this agreement.</span></span>
7. <span data-ttu-id="fbb95-132">قم بتوسيع قسم "تفاصيل البند".</span><span class="sxs-lookup"><span data-stu-id="fbb95-132">Expand the Line details section.</span></span>
8. <span data-ttu-id="fbb95-133">حدد "نعم" في حقل "‏‫فرض الحد الأقصى‬".</span><span class="sxs-lookup"><span data-stu-id="fbb95-133">Select Yes in the Max is enforced field.</span></span>
    * <span data-ttu-id="fbb95-134">تحديد الحد الأقصى المفروض يعني أن المبلغ الإجمالي لكافة بنود أمر المبيعات التي تستخدم أسعار خاصة للالتزام و/أو خصومات و/أو شروط الدفع يجب ألا يتجاوز المبلغ المحدد في الالتزام.</span><span class="sxs-lookup"><span data-stu-id="fbb95-134">Selecting Max is enforced means that the total amount of all the sales order lines that use the commitment's special prices, discounts and/or payment terms must not exceed the amount specified on the commitment.</span></span>  
    * <span data-ttu-id="fbb95-135">يحدد الحد الأقصى والأدنى للمبالغ الصادرة نطاق القيم التي يجب أن يتم بيعها في كل أمر مبيعات يستخدم الاتفاقية المحددة.</span><span class="sxs-lookup"><span data-stu-id="fbb95-135">The minimum and maximum release amounts specify a range of values that must be sold on each sales order that uses the selected agreement.</span></span>   
9. <span data-ttu-id="fbb95-136">قم بتوسيع قسم الرأس "اتفاقية البيع".</span><span class="sxs-lookup"><span data-stu-id="fbb95-136">Expand the Sales agreement header section.</span></span>
    * <span data-ttu-id="fbb95-137">ما لم يتم تعيين حالة الاتفاقية إلى فعالة، لا يمكن ربط أوامر المبيعات بالاتفاقية، وبالتالي لا يمكنها المساهمة في تنفيذ هذه الاتفاقية.</span><span class="sxs-lookup"><span data-stu-id="fbb95-137">Unless the status of the agreement is set to Effective, sales orders cannot be associated with the agreement and can therefore not contribute to the fulfilment of that agreement.</span></span> <span data-ttu-id="fbb95-138">يمكنك تغيير الحالة يدويًا في هذه المرحلة.</span><span class="sxs-lookup"><span data-stu-id="fbb95-138">You can change the status manually at this stage.</span></span> <span data-ttu-id="fbb95-139">ومع ذلك، عادة ما يتم تغيير الحالة عندما تقوم بتأكيد الاتفاقية للعميل.</span><span class="sxs-lookup"><span data-stu-id="fbb95-139">However, the status would normally be changed when you confirm the agreement for the customer.</span></span>  
10. <span data-ttu-id="fbb95-140">في جزء الإجراءات، انقر فوق "اتفاقيات المبيعات".</span><span class="sxs-lookup"><span data-stu-id="fbb95-140">On the Action Pane, click Sales agreement.</span></span>
11. <span data-ttu-id="fbb95-141">انقر فوق"تأكيد".</span><span class="sxs-lookup"><span data-stu-id="fbb95-141">Click Confirmation.</span></span>
    * <span data-ttu-id="fbb95-142">تأكد من أنه تم تعيين الخيار "تمييز الاتفاقية كاتفاقية فعالة" على "نعم".</span><span class="sxs-lookup"><span data-stu-id="fbb95-142">Make sure that the Mark agreement as effective option is set to Yes.</span></span>  
12. <span data-ttu-id="fbb95-143">حدد "نعم" في حقل "طباعة التقرير‬".</span><span class="sxs-lookup"><span data-stu-id="fbb95-143">Select Yes in the Print report field.</span></span>
13. <span data-ttu-id="fbb95-144">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="fbb95-144">Click OK.</span></span>
14. <span data-ttu-id="fbb95-145">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="fbb95-145">Close the page.</span></span>
    * <span data-ttu-id="fbb95-146">تكون الاتفاقية فعالة الآن ويمكنك البدء في ربط طلبات العميل بالاتفاقية، لمقابلة الهدف الإلزامي.</span><span class="sxs-lookup"><span data-stu-id="fbb95-146">The agreement is now effective and you can start linking the customer's orders to the agreement, to offset against the committed target.</span></span>  


