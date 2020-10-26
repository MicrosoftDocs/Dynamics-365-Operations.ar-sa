---
title: شحن أوامر المبيعات دون تخزينها
description: يوضح هذا الموضوع كيفية تحديث أمر مبيعات عند شحن المنتجات إلى العميل.
author: omulvad
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, SalesTableLineQuantity, CustPackingSlipJournal
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b6b1dbb4d53785c226f7c9d40339d9dd19f47152
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2020
ms.locfileid: "3984144"
---
# <a name="ship-sales-orders-without-warehousing"></a><span data-ttu-id="063b3-103">شحن أوامر المبيعات دون تخزينها</span><span class="sxs-lookup"><span data-stu-id="063b3-103">Ship sales orders without warehousing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="063b3-104">يوضح هذا الموضوع كيفية تحديث أمر مبيعات عند شحن المنتجات إلى العميل.</span><span class="sxs-lookup"><span data-stu-id="063b3-104">This topic explains how to update a sales order when products are shipped to the customer.</span></span> <span data-ttu-id="063b3-105">وينطبق الدليل على تدفق التنفيذ الذي لا يتم إعداده لإدارة المستودعات (ليس المستودع الأساسية أو المتقدم)، ولذلك لا يتطلب تسجيل انتقاء المنتجات قبل الشحن.</span><span class="sxs-lookup"><span data-stu-id="063b3-105">The guide is applicable to the fulfillment flow that is not set up for warehouse management (neither basic or advanced warehousing), and therefore does not require product picking to be registered before shipment.</span></span> <span data-ttu-id="063b3-106">يمكنك تنفيذ هذا الإجراء في البيانات الخاصة بك أو في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="063b3-106">You can run this procedure on your own data or in demo data company USMF.</span></span> <span data-ttu-id="063b3-107">في الحالتين، قبل أن تبدأ هذه المهمة، أنشئ أمر مبيعات لمنتج مسجل في المخزون كميته أكبر من 1.</span><span class="sxs-lookup"><span data-stu-id="063b3-107">In both cases, before you start this task, create a sales order for an inventoried product with a quantity of greater than 1.</span></span> <span data-ttu-id="063b3-108">لتجنب حدوث خطأ في الترحيل، يجب عليك أن تتأكد من أن كمية المنتج الفعلية في الموقع والمستودع التي حددتها في الأمر تغطي كمية الأمر.</span><span class="sxs-lookup"><span data-stu-id="063b3-108">To avoid a posting error, you need to check that the product's on-hand quantity in the site and warehouse that you've selected on the order covers the order quantity.</span></span>

## <a name="post-packing-slip-for-an-order"></a><span data-ttu-id="063b3-109">ترحيل إيصال التعبئة لأمر</span><span class="sxs-lookup"><span data-stu-id="063b3-109">Post packing slip for an order</span></span>
1. <span data-ttu-id="063b3-110">في جزء التنقل، انتقل إلى **الوحدات النمطية > المبيعات والتسويق > أوامر المبيعات > كافة أوامر المبيعات** .</span><span class="sxs-lookup"><span data-stu-id="063b3-110">In the navigation pane, go to **Modules > Sales and marketing > Sales orders > All sales orders** .</span></span>
2. <span data-ttu-id="063b3-111">في القائمة، ابحث عن الأمر الذي قمت بإنشائه لهذه المهمة وحدده.</span><span class="sxs-lookup"><span data-stu-id="063b3-111">In the list, find and select the order you have created for this task.</span></span>
3. <span data-ttu-id="063b3-112">في "جزء الإجراءات"، انقر فوق **انتقاء وتعبئة** .</span><span class="sxs-lookup"><span data-stu-id="063b3-112">On the Action Pane, select **Pick and pack** .</span></span>
4. <span data-ttu-id="063b3-113">حدد **ترحيل إيصال التعبئة‬** .</span><span class="sxs-lookup"><span data-stu-id="063b3-113">Select **Post packing slip** .</span></span>
5. <span data-ttu-id="063b3-114">قم بتوسيع القسم **المعلمات** أو طيه.</span><span class="sxs-lookup"><span data-stu-id="063b3-114">Expand or collapse the **Parameters** section.</span></span>
6. <span data-ttu-id="063b3-115">في حقل **الكمية** ، حدد **الكل** .</span><span class="sxs-lookup"><span data-stu-id="063b3-115">In the **Quantity** field, select **All** .</span></span>
    - <span data-ttu-id="063b3-116">تشمل الخيارات الأخرى **التسليم الآن** و **منتقاة** .</span><span class="sxs-lookup"><span data-stu-id="063b3-116">Other options include **Deliver now** and **Picked** .</span></span> <span data-ttu-id="063b3-117">إذا كان من المقرر شحن بند أمر جزئيًا وكان الحقل **التسليم الآن** على بند الأمر يحتوي على كمية، فيمكنك تحديد **التسليم الآن** .</span><span class="sxs-lookup"><span data-stu-id="063b3-117">If the order line is to be shipped partially and the **Deliver now** field on the order line contains a quantity, you would select **Deliver now** .</span></span> <span data-ttu-id="063b3-118">إذا تضمن تدفق تنفيذ المؤسسة الانتقاء كعملية منفصلة تتم إدارتها وتسجيلها باستخدام قائمة انتقاء، يمكنك اختيار **منتقاة** .</span><span class="sxs-lookup"><span data-stu-id="063b3-118">If your organization's fulfillment flow includes picking as a separate process that is managed by and registered with a picking list, you would select **Picked** .</span></span>  
    - <span data-ttu-id="063b3-119">تأكد من تعيين **خيار الترحيل** إلى **نعم** .</span><span class="sxs-lookup"><span data-stu-id="063b3-119">Check that the **Posting** option is set to **Yes** .</span></span>  
7. <span data-ttu-id="063b3-120">عيّن الخيار **طباعة إيصال التعبئة** إلى **نعم** .</span><span class="sxs-lookup"><span data-stu-id="063b3-120">Set the **Print packing slip** option to **Yes** .</span></span> <span data-ttu-id="063b3-121">تحتوي علامة التبويب **نظرة عامة** على إيصالات التعبئة المقرر إنشاءها في هذا الترحيل.</span><span class="sxs-lookup"><span data-stu-id="063b3-121">The **Overview** tab contains a list of packing slips to be generated in this posting.</span></span> <span data-ttu-id="063b3-122">في حالة شحن أمر فردي، عادة ما سيكون هناك إيصال تعبئة واحد.</span><span class="sxs-lookup"><span data-stu-id="063b3-122">If you are shipping an individual order, there will typically be one packing slip.</span></span> <span data-ttu-id="063b3-123">ومع ذلك، إذا كان من المقرر شحن بنود ذلك الأمر من مواقع مختلفة، سيتم تقسيم الترحيل تلقائياً إلى العدد المناسب من المستندات.</span><span class="sxs-lookup"><span data-stu-id="063b3-123">However, if that order's lines are to be shipped from different sites, posting will automatically be split into the appropriate number of documents.</span></span> <span data-ttu-id="063b3-124">وهذا شرط إلزامي لا يمكن تغييره.</span><span class="sxs-lookup"><span data-stu-id="063b3-124">This is a mandatory condition that cannot be changed.</span></span> <span data-ttu-id="063b3-125">وبالمثل، سيتم أيضًا تقسيم الترحيل إلى وثائق متعددة إذا كان سيتم شحن بنود الأمر إلى عناوين تسليم مختلفة، وتم إعداد سياسة الشحن على المطالبة بعملية تقسيم.</span><span class="sxs-lookup"><span data-stu-id="063b3-125">Similarly, the posting will also be split into multiple documents if the order's lines are to be shipped to different delivery addresses, and the shipping policy is set up to require a split.</span></span>  
8. <span data-ttu-id="063b3-126">في علامة التبويب **البنود** ، حدد الصف الخاص ببند الأمر الذي سيتم شحنه.</span><span class="sxs-lookup"><span data-stu-id="063b3-126">On the **Lines** tab, select the row for the order line to be shipped.</span></span>
9. <span data-ttu-id="063b3-127">في الحقل **تحديث** ، أدخل رقمًا أقل من الكمية الأصلية.</span><span class="sxs-lookup"><span data-stu-id="063b3-127">In the **Update** field, enter a number lower than the original quantity.</span></span>
10. <span data-ttu-id="063b3-128">حدد **موافق** .</span><span class="sxs-lookup"><span data-stu-id="063b3-128">Select **OK** .</span></span>
11. <span data-ttu-id="063b3-129">حدد **نعم** .</span><span class="sxs-lookup"><span data-stu-id="063b3-129">Select **Yes** .</span></span>
12. <span data-ttu-id="063b3-130">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="063b3-130">Close the page.</span></span>
13. <span data-ttu-id="063b3-131">في جزء الإجراءات، حدد **خيارات** .</span><span class="sxs-lookup"><span data-stu-id="063b3-131">On the Action Pane, select **Options** .</span></span>
14. <span data-ttu-id="063b3-132">حدد **تغيير طريقة العرض** .</span><span class="sxs-lookup"><span data-stu-id="063b3-132">Select **Change view** .</span></span>
15. <span data-ttu-id="063b3-133">حدد **طريقة عرض الرأس** .</span><span class="sxs-lookup"><span data-stu-id="063b3-133">Select **Header view** .</span></span>
    - <span data-ttu-id="063b3-134">إذا تم شحن جميع البنود بالأمر بالكامل، ستتغير حالة الأمر من "مفتوح" إلى " تم تسليمه".</span><span class="sxs-lookup"><span data-stu-id="063b3-134">If all of the lines on the order have been fully shipped, the order status changes from Open to Delivered.</span></span>  
    - <span data-ttu-id="063b3-135">في هذا المثال، تم شحن بند الأمر جزئيًا.</span><span class="sxs-lookup"><span data-stu-id="063b3-135">In this example, the order line has been shipped partially.</span></span> <span data-ttu-id="063b3-136">وهذا هو سبب بقاء حالة الأمر "مفتوح".</span><span class="sxs-lookup"><span data-stu-id="063b3-136">This is why the the order status remains Open.</span></span>     
    - <span data-ttu-id="063b3-137">تم تعيين الحقل **حالة المستند** إلى "إيصال التعبئة" لأنه تم شحن بند أمر واحد على الأقل.</span><span class="sxs-lookup"><span data-stu-id="063b3-137">The **Document status** field is set to Packing slip because at least one of the order lines have been shipped.</span></span>  
16. <span data-ttu-id="063b3-138">في جزء الإجراءات، حدد **عام** .</span><span class="sxs-lookup"><span data-stu-id="063b3-138">On the Action Pane, select **General** .</span></span>
17. <span data-ttu-id="063b3-139">حدد **كمية البند** .</span><span class="sxs-lookup"><span data-stu-id="063b3-139">Select **Line quantity** .</span></span>
18. <span data-ttu-id="063b3-140">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="063b3-140">Close the page.</span></span>
19. <span data-ttu-id="063b3-141">في "جزء الإجراءات"، انقر فوق **انتقاء وتعبئة** .</span><span class="sxs-lookup"><span data-stu-id="063b3-141">On the Action Pane, select **Pick and pack** .</span></span>
20. <span data-ttu-id="063b3-142">حدد **إيصال تعبئة** .</span><span class="sxs-lookup"><span data-stu-id="063b3-142">Select **Packing slip** .</span></span> <span data-ttu-id="063b3-143">تحتوي الصفحة **دفتر يومية إيصالات التعبئة** على جميع مستندات إيصالات التعبئة التي تم إنشاؤها للأمر.</span><span class="sxs-lookup"><span data-stu-id="063b3-143">The **Packing slip journal** page contains all the packing slip documents that were generated for your order.</span></span> <span data-ttu-id="063b3-144">ويمكنك مراجعة تفاصيل كل مستند وطباعتها، إذا كنت ترغب في هذا.</span><span class="sxs-lookup"><span data-stu-id="063b3-144">You can review details of each document and print them, if you wish.</span></span>  

