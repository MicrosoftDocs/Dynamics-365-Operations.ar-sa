---
title: شحن أوامر المبيعات دون تخزين
description: يوضح هذا الدليل كيفية تحديث أمر مبيعات عند شحن المنتجات إلى العميل.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, SalesTableLineQuantity, CustPackingSlipJournal
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae70e09dbc4da90b7d1802d076384eae2d00da0e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555783"
---
# <a name="ship-sales-orders-without-warehousing"></a><span data-ttu-id="8fb9b-103">شحن أوامر المبيعات دون تخزين</span><span class="sxs-lookup"><span data-stu-id="8fb9b-103">Ship sales orders without warehousing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8fb9b-104">يوضح هذا الدليل كيفية تحديث أمر مبيعات عند شحن المنتجات إلى العميل.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-104">This guide demonstrates how to update a sales order when products are shipped to the customer.</span></span> <span data-ttu-id="8fb9b-105">وينطبق الدليل على تدفق التنفيذ الذي لا يتم إعداده لإدارة المستودعات (ليس المستودع الأساسية أو المتقدم)، ولذلك لا يتطلب تسجيل انتقاء المنتجات قبل الشحن.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-105">The guide is applicable to the fulfillment flow that is not set up for warehouse management (neither basic or advanced warehousing), and therefore does not require product picking to be registered before shipment.</span></span> <span data-ttu-id="8fb9b-106">يمكنك تنفيذ هذا الإجراء في البيانات الخاصة بك أو في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-106">You can run this procedure on your own data or in demo data company USMF.</span></span> <span data-ttu-id="8fb9b-107">في الحالتين، قبل أن تبدأ هذه المهمة، أنشئ أمر مبيعات لمنتج مسجل في المخزون كميته أكبر من 1.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-107">In both cases, before you start this task, create a sales order for an inventoried product with a quantity of greater than 1.</span></span> <span data-ttu-id="8fb9b-108">لتجنب حدوث خطأ في الترحيل، يجب عليك أن تتأكد من أن كمية المنتج الفعلية في الموقع والمستودع التي حددتها في الأمر تغطي كمية الأمر.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-108">To avoid a posting error, you need to check that the product's on-hand quantity in the site and warehouse that you’ve selected on the order covers the order quantity.</span></span>


## <a name="post-packing-slip-for-an-order"></a><span data-ttu-id="8fb9b-109">ترحيل إيصال التعبئة لأمر</span><span class="sxs-lookup"><span data-stu-id="8fb9b-109">Post packing slip for an order</span></span>
1. <span data-ttu-id="8fb9b-110">انتقل إلى المبيعات والتسويق > أوامر المبيعات > كافة أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-110">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="8fb9b-111">في القائمة، ابحث عن الأمر الذي قمت بإنشائه لهذه المهمة وحدده.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-111">In the list, find and select the order you have created for this task.</span></span>
3. <span data-ttu-id="8fb9b-112">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="8fb9b-113">في "جزء الإجراءات"، انقر فوق "انتقاء وتعبئة‬".</span><span class="sxs-lookup"><span data-stu-id="8fb9b-113">On the Action Pane, click Pick and pack.</span></span>
5. <span data-ttu-id="8fb9b-114">انقر فوق "ترحيل إيصال التعبئة".</span><span class="sxs-lookup"><span data-stu-id="8fb9b-114">Click Post packing slip.</span></span>
6. <span data-ttu-id="8fb9b-115">قم بتوسيع القسم "المعلمات" أو طيه.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-115">Expand or collapse the Parameters section.</span></span>
7. <span data-ttu-id="8fb9b-116">في الحقل "الكمية"، حدد "الكل".</span><span class="sxs-lookup"><span data-stu-id="8fb9b-116">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="8fb9b-117">تشمل الخيارات الأخرى "التسليم الآن" و"منتقاة".</span><span class="sxs-lookup"><span data-stu-id="8fb9b-117">Other options include Deliver now and Picked.</span></span> <span data-ttu-id="8fb9b-118">إذا كان من المقرر شحن بند أمر جزئيًا وكان الحقل "التسليم الآن" ببند الأمر يحتوي على كمية، يمكنك تحديد "التسليم الآن".</span><span class="sxs-lookup"><span data-stu-id="8fb9b-118">If the order line is to be shipped partially and the Deliver now field on the order line contains a quantity, you would select Deliver now.</span></span> <span data-ttu-id="8fb9b-119">إذا تضمن تدفق تنفيذ المؤسسة انتقاء كعملية منفصلة تتم إدارتها وتسجيلها باستخدام قائمة انتقاء، يمكنك اختيار "منتقاة".</span><span class="sxs-lookup"><span data-stu-id="8fb9b-119">If your organization's fulfillment flow includes picking as a separate process that is managed by and registered with a picking list, you would select Picked.</span></span>  
    * <span data-ttu-id="8fb9b-120">تحقق من تعيين خيار الترحيل على "نعم".</span><span class="sxs-lookup"><span data-stu-id="8fb9b-120">Check that the Posting option is set to Yes.</span></span>  
8. <span data-ttu-id="8fb9b-121">قم بتعيين الخيار "طباعة إيصال التعبئة" على "نعم".</span><span class="sxs-lookup"><span data-stu-id="8fb9b-121">Set the Print packing slip option to Yes.</span></span>
    * <span data-ttu-id="8fb9b-122">تحتوي علامة التبويب "نظرة عامة" على إيصالات التعبئة المقرر إنشاؤها في هذا الترحيل.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-122">The Overview tab contains a list of packing slips to be generated in this posting.</span></span> <span data-ttu-id="8fb9b-123">في حالة شحن أمر فردي، عادة ما سيكون هناك إيصال تعبئة واحد.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-123">If you are shipping an individual order, there will typically be one packing slip.</span></span> <span data-ttu-id="8fb9b-124">ومع ذلك، إذا كان من المقرر شحن بنود ذلك الأمر من مواقع مختلفة، سيتم تقسيم الترحيل تلقائياً إلى العدد المناسب من المستندات.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-124">However, if that order's lines are to be shipped from different sites, posting will automatically be split into the appropriate number of documents.</span></span> <span data-ttu-id="8fb9b-125">وهذا شرط إلزامي لا يمكن تغييره.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-125">This is a mandatory condition that cannot be changed.</span></span> <span data-ttu-id="8fb9b-126">وبالمثل، سيتم أيضًا تقسيم الترحيل إلى وثائق متعددة إذا كان سيتم شحن بنود الأمر إلى عناوين تسليم مختلفة، وتم إعداد سياسة الشحن على المطالبة بعملية تقسيم.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-126">Similarly, the posting will also be split into multiple documents if the order’s lines are to be shipped to different delivery addresses, and the shipping policy is set up to require a split.</span></span>  
9. <span data-ttu-id="8fb9b-127">في علامة التبويب "البنود"، حدد الصف الخاص ببند الأمر الذي سيتم شحنه.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-127">On the Lines tab, select the row for the order line to be shipped.</span></span>
10. <span data-ttu-id="8fb9b-128">في الحقل "تحديث"، أدخل رقمًا أقل من الكمية الأصلية.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-128">In the Update field, enter a number lower than the original quantity.</span></span>
11. <span data-ttu-id="8fb9b-129">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="8fb9b-129">Click OK.</span></span>
12. <span data-ttu-id="8fb9b-130">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-130">Click Yes.</span></span>
13. <span data-ttu-id="8fb9b-131">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-131">Close the page.</span></span>
14. <span data-ttu-id="8fb9b-132">في جزء الإجراءات، انقر فوق "خيارات".</span><span class="sxs-lookup"><span data-stu-id="8fb9b-132">On the Action Pane, click Options.</span></span>
15. <span data-ttu-id="8fb9b-133">انقر فوق "تغيير طريقة العرض‬".</span><span class="sxs-lookup"><span data-stu-id="8fb9b-133">Click Change view.</span></span>
16. <span data-ttu-id="8fb9b-134">انقر فوق "عرض الرأس".</span><span class="sxs-lookup"><span data-stu-id="8fb9b-134">Click Header view.</span></span>
    * <span data-ttu-id="8fb9b-135">إذا تم شحن جميع البنود بالأمر بالكامل، ستتغير حالة الأمر من "مفتوح" إلى " تم تسليمه".</span><span class="sxs-lookup"><span data-stu-id="8fb9b-135">If all of the lines on the order have been fully shipped, the order status changes from Open to Delivered.</span></span>  
    * <span data-ttu-id="8fb9b-136">في هذا المثال، تم شحن بند الأمر جزئيًا.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-136">In this example, the order line has been shipped partially.</span></span> <span data-ttu-id="8fb9b-137">وهذا هو سبب بقاء حالة الأمر "مفتوح".</span><span class="sxs-lookup"><span data-stu-id="8fb9b-137">This is why the the order status remains Open.</span></span>     
    * <span data-ttu-id="8fb9b-138">تم تعيين الحقل "حالة المستند" على "إيصال التعبئة" لأنه تم شحن بند أمر واحد على الأقل.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-138">The Document status field is set to Packing slip because at least one of the order lines have been shipped.</span></span>  
17. <span data-ttu-id="8fb9b-139">في جزء "الإجراءات"، انقر فوق "عام".</span><span class="sxs-lookup"><span data-stu-id="8fb9b-139">On the Action Pane, click General.</span></span>
18. <span data-ttu-id="8fb9b-140">انقر فوق "كمية البند".</span><span class="sxs-lookup"><span data-stu-id="8fb9b-140">Click Line quantity.</span></span>
19. <span data-ttu-id="8fb9b-141">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-141">Close the page.</span></span>
20. <span data-ttu-id="8fb9b-142">في "جزء الإجراءات"، انقر فوق "انتقاء وتعبئة‬".</span><span class="sxs-lookup"><span data-stu-id="8fb9b-142">On the Action Pane, click Pick and pack.</span></span>
21. <span data-ttu-id="8fb9b-143">انقر فوق "إيصال التعبئة".</span><span class="sxs-lookup"><span data-stu-id="8fb9b-143">Click Packing slip.</span></span>
    * <span data-ttu-id="8fb9b-144">تحتوي الصفحة "دفتر يومية إيصالات التعبئة" على جميع مستندات إيصالات التعبئة التي تم إنشاؤها للأمر.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-144">The Packing slip journal page contains all the packing slip documents that were generated for your order.</span></span> <span data-ttu-id="8fb9b-145">ويمكنك مراجعة تفاصيل كل مستند وطباعتها، إذا كنت ترغب في هذا.</span><span class="sxs-lookup"><span data-stu-id="8fb9b-145">You can review details of each document and print them, if you wish.</span></span>  

