---
title: إدخال اتفاقيات البيع
description: يشرح هذا الموضوع كيفية إنشاء اتفاقية بيع تلزم أحد العملاء بشراء منتج بمبلغ متفق عليه مع مرور الوقت مقابل الحصول على خصومات خاصة.
author: omulvad
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreementCreate, SalesAgreement, InventItemIdLookupSimple, AgreementConfirmRunForm, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7699f426c102b4ae2610db0851ddd127e514b652
ms.sourcegitcommit: 6545bef4584d72dd7789f2d3935cf00ac8f489b0
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/13/2019
ms.locfileid: "1871019"
---
# <a name="enter-sales-agreements"></a><span data-ttu-id="05185-103">إدخال اتفاقيات البيع</span><span class="sxs-lookup"><span data-stu-id="05185-103">Enter sales agreements</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="05185-104">يشرح هذا الموضوع كيفية إنشاء اتفاقية بيع تلزم أحد العملاء بشراء منتج بمبلغ متفق عليه مع مرور الوقت مقابل الحصول على خصومات خاصة.</span><span class="sxs-lookup"><span data-stu-id="05185-104">This topic explains how to create a sales agreement that commits one of your customers to buy a product for an agreed amount over time in exchange for special discounts.</span></span> <span data-ttu-id="05185-105">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF أو باستخدام بياناتك الخاصة.</span><span class="sxs-lookup"><span data-stu-id="05185-105">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-sales-agreement-header"></a><span data-ttu-id="05185-106">إعداد عنوان اتفاقية البيع</span><span class="sxs-lookup"><span data-stu-id="05185-106">Set up sales agreement header</span></span>
1. <span data-ttu-id="05185-107">في جزء التنقل، انتقل إلى **الوحدات النمطية > المبيعات والتسويق > اتفاقيات البيع > اتفاقيات البيع**.</span><span class="sxs-lookup"><span data-stu-id="05185-107">In the navigation pane, go to **Modules > Sales and marketing > Sales agreements > Sales agreements**.</span></span>
2. <span data-ttu-id="05185-108">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="05185-108">Select **New**.</span></span>
3. <span data-ttu-id="05185-109">في حقل **حساب العميل**، حدد السجل المطلوب من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="05185-109">In the **Customer account** field, select the desired record from the drop-down menu.</span></span>
4. <span data-ttu-id="05185-110">في حقل **تصنيف اتفاقيات البيع‬**، حدد السجل المطلوب من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="05185-110">In the **Sales agreement classification** field, select the desired record from the drop-down menu.</span></span>
5. <span data-ttu-id="05185-111">قم بتوسيع القسم **عام**.</span><span class="sxs-lookup"><span data-stu-id="05185-111">Expand the **General** section.</span></span>
6. <span data-ttu-id="05185-112">في حقل **الالتزام الافتراضي**، حدد **الالتزام بقيمة المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="05185-112">In the **Default commitment** field, select **Product value commitment**.</span></span> <span data-ttu-id="05185-113">نوع الالتزام هو معيار إلزامي يجب عليك تعيينه إلى الاتفاقية لتحديد كيفية الوفاء بعقد الاتفاقية.</span><span class="sxs-lookup"><span data-stu-id="05185-113">A commitment type is a mandatory criterion that you must assign to the agreement to define how the agreement contract will be fulfilled.</span></span> <span data-ttu-id="05185-114">تمكنك الأنواع الاًربعة المحددة مسبقًا من إعداد هدف التزام العميل، الموضح ككمية أو قيمة.</span><span class="sxs-lookup"><span data-stu-id="05185-114">The four predefined types let you set up the customer's commitment target, expressed as a quantity or a value.</span></span> <span data-ttu-id="05185-115">ولا يمكن تطبيق نوع الالتزام بالكمية إلا لمنتج معين، ولكن الأنواع المعتمدة على القيمة قابلة للتطبيق على مبيعات المنتجات المحددة وغير المحددة.</span><span class="sxs-lookup"><span data-stu-id="05185-115">The quantity commitment type can only be applied to a specific product, but the value-based types are applicable to sales of both specific and non-specific products.</span></span>  
7. <span data-ttu-id="05185-116">في حقل **تاريخ انتهاء الصلاحية**، قم بتعيين التاريخ إلى تاريخ في المستقبل عندما ترغب في إنهاء صلاحية الاتفاقية.</span><span class="sxs-lookup"><span data-stu-id="05185-116">In the **Expiration date** field, set the date to a future date when you want the agreement to expire.</span></span>
8. <span data-ttu-id="05185-117">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="05185-117">Select **OK**.</span></span>

## <a name="set-up-product-value-commitment-lines"></a><span data-ttu-id="05185-118">إعداد بنود الالتزام بقيمة المنتجات</span><span class="sxs-lookup"><span data-stu-id="05185-118">Set up product value commitment lines</span></span>
1. <span data-ttu-id="05185-119">حدد **إضافة بند**.</span><span class="sxs-lookup"><span data-stu-id="05185-119">Select **Add line**.</span></span>
2. <span data-ttu-id="05185-120">في الحقل **رقم الصنف**، انقر فوق السجل المطلوب من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="05185-120">In the **Item number** field, select the desired record from the drop-down menu.</span></span> <span data-ttu-id="05185-121">يؤثر نوع الالتزام الذي تم اختياره للاتفاقية على نوع المعلومات التي يمكنك إدخالها لبنود الاتفاقية.</span><span class="sxs-lookup"><span data-stu-id="05185-121">The type of commitment that you have chosen for the agreement affects the kind of information you can enter for the agreement lines.</span></span> <span data-ttu-id="05185-122">على سبيل المثال، بالنسبة للاتفاقية المعتمدة على القيمة، يجب تحديد المبلغ الصافي الإجمالي (بالعملة المتفق عليها) التي تلزم العميل بشراء سلع منك.</span><span class="sxs-lookup"><span data-stu-id="05185-122">For example, for a value-based agreement you must specify the total net amount (in the agreed currency) for which the customer commits to buys goods from you.</span></span> <span data-ttu-id="05185-123">في هذا المثال، لا يتوفر حقلا **الكمية** و**الوحدة** في البند لأنك تقوم بإنشاء اتفاقية للعميل لشراء قيمة معينة للمنتج.</span><span class="sxs-lookup"><span data-stu-id="05185-123">In this example the **Quantity** and **Unit** fields on the line are unavailable because you’re creating an agreement for the customer to buy a specific value of a product.</span></span>   
3. <span data-ttu-id="05185-124">في حقل **المبلغ الصافي**، أدخل المبلغ النقدي الذي التزم العميل بتخصيصه للشراء.</span><span class="sxs-lookup"><span data-stu-id="05185-124">In the **Net amount** field, enter the monetary amount that the customer has committed to buying.</span></span>
4. <span data-ttu-id="05185-125">في حقل **نسبة الخصم**، أدخل قيمة النسبة مئوية التي سيتم تطبيقها على بنود أمر المبيعات الخاص بالعميل المرتبطة بهذه الاتفاقية.</span><span class="sxs-lookup"><span data-stu-id="05185-125">In the **Discount percent** field, enter a percentage value that will apply to the customer's sales order lines that are linked to this agreement.</span></span>
5. <span data-ttu-id="05185-126">قم بتوسيع قسم **تفاصيل البند**.</span><span class="sxs-lookup"><span data-stu-id="05185-126">Expand the **Line details** section.</span></span>
6. <span data-ttu-id="05185-127">حدد **نعم** في حقل **فرض الحد الأقصى**.</span><span class="sxs-lookup"><span data-stu-id="05185-127">Select **Yes** in the **Max is enforced** field.</span></span>
    - <span data-ttu-id="05185-128">يعني تحديد **فرض الحد الأقصى** أن المبلغ الإجمالي لكافة بنود أمر المبيعات التي تستخدم أسعارًا خاصة للالتزام و/أو خصومات و/أو شروط الدفع يجب ألا يتجاوز المبلغ المحدد في الالتزام.</span><span class="sxs-lookup"><span data-stu-id="05185-128">Selecting **Max is enforced** means that the total amount of all the sales order lines that use the commitment's special prices, discounts and/or payment terms must not exceed the amount specified on the commitment.</span></span>  
    - <span data-ttu-id="05185-129">يحدد الحد الأقصى والأدنى للمبالغ الصادرة نطاق القيم التي يجب أن يتم بيعها في كل أمر مبيعات يستخدم الاتفاقية المحددة.</span><span class="sxs-lookup"><span data-stu-id="05185-129">The minimum and maximum release amounts specify a range of values that must be sold on each sales order that uses the selected agreement.</span></span>   
7. <span data-ttu-id="05185-130">قم بتوسيع قسم **رأس اتفاقية البيع‬**.</span><span class="sxs-lookup"><span data-stu-id="05185-130">Expand the **Sales agreement header** section.</span></span> <span data-ttu-id="05185-131">ما لم يتم تعيين حالة الاتفاقية إلى **فعالة**، لا يمكن ربط أوامر المبيعات بالاتفاقية، وبالتالي لا يمكنها المساهمة في تنفيذ هذه الاتفاقية.</span><span class="sxs-lookup"><span data-stu-id="05185-131">Unless the status of the agreement is set to **Effective**, sales orders cannot be associated with the agreement and can therefore not contribute to the fulfilment of that agreement.</span></span> <span data-ttu-id="05185-132">يمكنك تغيير الحالة يدويًا في هذه المرحلة.</span><span class="sxs-lookup"><span data-stu-id="05185-132">You can change the status manually at this stage.</span></span> <span data-ttu-id="05185-133">ومع ذلك، عادة ما يتم تغيير الحالة عندما تقوم بتأكيد الاتفاقية للعميل.</span><span class="sxs-lookup"><span data-stu-id="05185-133">However, the status would normally be changed when you confirm the agreement for the customer.</span></span>  
8. <span data-ttu-id="05185-134">في جزء الإجراءات، انقر فوق **اتفاقيات المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="05185-134">On the Action Pane, select **Sales agreement**.</span></span>
9. <span data-ttu-id="05185-135">حدد **تأكيد**.</span><span class="sxs-lookup"><span data-stu-id="05185-135">Select **Confirmation**.</span></span> <span data-ttu-id="05185-136">تأكد من تعيين الخيار **تمييز الاتفاقية كاتفاقية فعالة** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="05185-136">Make sure that the **Mark agreement as effective** option is set to **Yes**.</span></span>  
10. <span data-ttu-id="05185-137">حدد **نعم** في حقل **طباعة التقرير‬**.</span><span class="sxs-lookup"><span data-stu-id="05185-137">Select **Yes** in the **Print report** field.</span></span>
11. <span data-ttu-id="05185-138">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="05185-138">Select **OK**.</span></span>
12. <span data-ttu-id="05185-139">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="05185-139">Close the page.</span></span> <span data-ttu-id="05185-140">أصبحت الاتفاقية الآن سارية المفعول.</span><span class="sxs-lookup"><span data-stu-id="05185-140">The agreement is now effective.</span></span> <span data-ttu-id="05185-141">يمكنك بدء ربط طلبات العميل بالاتفاقية، لمقابلة الهدف الذي تم الالتزام به.</span><span class="sxs-lookup"><span data-stu-id="05185-141">You can start linking the customer's orders to the agreement to offset against the committed target.</span></span>  

