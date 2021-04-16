---
title: إعادة استدعاء عملية الأمر في نقطة البيع
description: يشرح هذا الموضوع إمكانيات الميزات المتوفرة لطلب تحسين صفحات الاستدعاء في POS.
author: hhainesms
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2f7ad4f53917bb607afe84a2c457518c3f8f7a08
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799085"
---
# <a name="recall-order-operation-in-pos"></a><span data-ttu-id="35954-103">إعادة استدعاء عملية الأمر في نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="35954-103">Recall order operation in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="35954-104">توفر ‏ عملية **إعادة استدعاء الأمر** في نقطة بيع (POS) Commerce ميزات بحث وتصفية مُحدّثة ومعلومات خاصة بالأمر.</span><span class="sxs-lookup"><span data-stu-id="35954-104">The **Recall order** operation in the Commerce point of sale (POS) provides updated order search and filtering features and order-specific information.</span></span> <span data-ttu-id="35954-105">تتوفر هذه الميزة في الإصدار 10.0.15 من Commerce والإصدارات اللاحقة.</span><span class="sxs-lookup"><span data-stu-id="35954-105">This feature is available in Commerce versions 10.0.15 and later.</span></span>

<span data-ttu-id="35954-106">لتمكين هذه الوظيفة، قم بتشغيل ميزة **عمليه أمر أعاده الاستدعاء المحسنة في POS** في مساحة عمل **أداره الميزات** في مركز Commerce الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="35954-106">To enable this functionality, turn the **Improved Recall order operation in POS** feature on in **Feature management** workspace in Commerce headquarters.</span></span> <span data-ttu-id="35954-107">بعد تمكين الميزة ، حاول تحديث [تخطيطات الشاشة](pos-screen-layouts.md)في نقطه البيع للاستفادة من الإمكانيات التي تم تغييرها.</span><span class="sxs-lookup"><span data-stu-id="35954-107">After you enable the feature, consider updating your [screen layouts](pos-screen-layouts.md) in POS to take advantage of some of the changed  capabilities.</span></span>

<span data-ttu-id="35954-108">يسمح تكوين زر عملية **أمر الاستدعاء** للمؤسسات لنشر العملية بعرض معرف مسبقا.</span><span class="sxs-lookup"><span data-stu-id="35954-108">The configuration of the **Recall order** operation button allows organizations to deploy the operation with a pre-defined display.</span></span>

![تكوين شبكة الزر](media/recallorderbuttongrid.png)

<span data-ttu-id="35954-110">وخيارات العرض كما يلي.</span><span class="sxs-lookup"><span data-stu-id="35954-110">The display options are as follows.</span></span>
- <span data-ttu-id="35954-111">**بلا** – يقوم هذا الخيار بنشر العملية بدون عرض محدد.</span><span class="sxs-lookup"><span data-stu-id="35954-111">**None** – This option deploys the operation with no specific display.</span></span> <span data-ttu-id="35954-112">عندما يقوم أحد المستخدمين بفتح العملية باستخدام هذا التكوين، ستتم مطالبتهم بالبحث عن الأوامر والبحث عنها أو الاختيار من عامل تصفيه أمر معرف مسبقا.</span><span class="sxs-lookup"><span data-stu-id="35954-112">When a user opens the operation with this configuration, they will be prompted to search and find orders or choose from a pre-defined order filter.</span></span>
- <span data-ttu-id="35954-113">**الأوامر المطلوب تنفيذها** -عندما يقوم مستخدم ببدء العملية، سيتم تشغيل استعلام تلقائيا للبحث عن قائمه بالأوامر التي سيتم استيفاؤها بواسطة المتجر الحالي للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="35954-113">**Orders to fulfill** – When a user launches the operation, a query will run automatically to search and display a list of orders that are to be fulfilled by the user's current store.</span></span> <span data-ttu-id="35954-114">يتم تكوين هذه الأوامر للالتقاط في المتجر أو الشحنة المتجر ولم يتم بعد انتقاء بنود هذه الأوامر أو تعبئتها.</span><span class="sxs-lookup"><span data-stu-id="35954-114">These orders are configured for in-store pickup or store shipment and the lines of these orders have not yet been picked or packed.</span></span>
- <span data-ttu-id="35954-115">**الأوامر المطلوب تنفيذها** -عندما يقوم مستخدم ببدء العملية، سيتم تشغيل استعلام تلقائيا للبحث عن قائمه بالأوامر التي سيتم تكوينها للاستلام داخل المتجر وعرضها للمتجر الحالي للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="35954-115">**Orders to pick up** – When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for in-store pickup at the user's current store.</span></span>
- <span data-ttu-id="35954-116">**الأوامر المطلوب شحنها** - عندما يقوم مستخدم ببدء العملية، سيتم تشغيل استعلام تلقائيا للبحث عن قائمه بالأوامر التي سيتم تكوينها للشحن من المتجر الحالي للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="35954-116">**Orders to ship** - When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for shipment from the user's current store.</span></span>

<span data-ttu-id="35954-117">عند تشغيل عمليه **أمر الاستدعاء** من نقطه البيع، إذا تم تكوين العرض علي **بلا**، سيكون بإمكان المستخدم البحث عن الأوامر واستردادها بأحدي الطرق التالية.</span><span class="sxs-lookup"><span data-stu-id="35954-117">When launching the **Recall order** operation from POS, if the display is configured to **None**, a user will be able to search and retrieve orders in one of the following ways.</span></span>
- <span data-ttu-id="35954-118">امسح الرموز الشريطية للأمر.</span><span class="sxs-lookup"><span data-stu-id="35954-118">Scan order barcodes.</span></span> <span data-ttu-id="35954-119">سيؤدي ذلك إلى البحث في رقم الأمر ومرجع القناة وحقول معرف الاستلام للتطابقات المطابقة.</span><span class="sxs-lookup"><span data-stu-id="35954-119">This will search order number, channel reference, and receipt ID fields for matches.</span></span>
- <span data-ttu-id="35954-120">حدد أيقونة **أوامر البحث** أو **البحث والتصفية** في شريط التطبيقات لاستخدام اليه التصفية لتحديد موقع الطلبات التي تفي بمعايير التصفية.</span><span class="sxs-lookup"><span data-stu-id="35954-120">Select **Search orders** or **Search and filter** icon on the AppBar to use the filtering mechanism to locate orders that meet the filter criteria.</span></span>
- <span data-ttu-id="35954-121">يمكنك الاختيار من عامل تصفيه معرف مسبقا من القائمة المنسدلة **إظهار الأوامر** (طلبات مطلوب تنفيذها أو طلبات مطلوب استلامها أو طلبات مطلوب شحنها).</span><span class="sxs-lookup"><span data-stu-id="35954-121">Choose from a pre-defined filter from the **Show Orders** drop-down menu (orders to fulfill, orders to pick up, or orders to ship).</span></span>

![القائمة الرئيسية لأوامر الاستدعاء](media/recallordermain.png)

<span data-ttu-id="35954-123">بعد تطبيق معايير البحث، سيعرض التطبيق قائمه بأوامر المبيعات المطابقة.</span><span class="sxs-lookup"><span data-stu-id="35954-123">After search criteria are applied, the application will display a list of matching sales orders.</span></span> <span data-ttu-id="35954-124">من المهم ملاحظة أنه عند استخدام خيارات البحث/التصفية، لا يجب أن تكون الأوامر التي تم استردادها مرتبطة بالمتجر الحالي للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="35954-124">It's important to note that when using the search/filter options, the orders retrieved do not have to be orders linked to the user's current store.</span></span> <span data-ttu-id="35954-125">ستقوم عملية البحث هذه باسترداد أي أمر عميل يطابق معايير البحث، حتى في حالة إنشاء الأمر أو تعيينه للاستيفاء بواسطة مخزن/قناة أو موقع مستودع آخر.</span><span class="sxs-lookup"><span data-stu-id="35954-125">This search process will retrieve and display any customer order that matches the search criteria, even if the order was created or set to be fulfilled by another store/channel or warehouse location.</span></span>

![تفاصيل أمر الاستدعاء](media/orderrecalldetail.png)

<span data-ttu-id="35954-127">يمكن للمستخدم تحديد أحد الأوامر في القائمة لعرض تفاصيل اضافيه.</span><span class="sxs-lookup"><span data-stu-id="35954-127">A user can select an order on the list to view additional details.</span></span> <span data-ttu-id="35954-128">تعرض لوحه المعلومات الموجودة علي الجانب الأيسر التفاصيل حول الأمر المحدد، بما في ذلك تفاصيل بند الأمر وتفاصيل التسليم وتفاصيل الإنجاز.</span><span class="sxs-lookup"><span data-stu-id="35954-128">The information panel on the right side of the screen displays specifics on the selected order, including order line details, delivery details, and fulfillment details.</span></span>

<span data-ttu-id="35954-129">من شريط التطبيقات، يمكن للمستخدم تحديد عمليه.</span><span class="sxs-lookup"><span data-stu-id="35954-129">From the AppBar, a user can select an operation.</span></span> <span data-ttu-id="35954-130">ووفقا لحاله الأمر، قد لا يتم تمكين بعض العمليات.</span><span class="sxs-lookup"><span data-stu-id="35954-130">Depending on the status of the order, certain operations may not be enabled.</span></span>

- <span data-ttu-id="35954-131">**إرجاع** – يقوم ببدء عملية إنشاء مرتجع لآية منتجات مفوترة في أمر العميل المحدد.</span><span class="sxs-lookup"><span data-stu-id="35954-131">**Return** – Initiates the process of creating a return for any of the invoiced products on the selected customer order.</span></span>

- <span data-ttu-id="35954-132">**إلغاء الأمر** – إصدار عمليه إلغاء كامله لأمر التوريد المحدد.</span><span class="sxs-lookup"><span data-stu-id="35954-132">**Cancel** – Issue a full cancellation of the selected sales order.</span></span> <span data-ttu-id="35954-133">لن يكون هذا الخيار متاحا للأوامر التي تم بدؤها من خلال قناة مركز اتصال ولا يمكن استخدامه لإلغاء أمر جزئيًا.</span><span class="sxs-lookup"><span data-stu-id="35954-133">This option will not be available for orders initiated through a call center channel and cannot be used to partially cancel an order.</span></span>

- <span data-ttu-id="35954-134">**التنفيذ** – تحويل المستخدم إلى صفحه استيفاء الأوامر، والذي سيتم تصفيته مسبقا للأمر المحدد.</span><span class="sxs-lookup"><span data-stu-id="35954-134">**Fulfill** – Transfers the user to the order fulfillment page, which will be pre-filtered for the selected order.</span></span> <span data-ttu-id="35954-135">سيتم فقط عرض سطور الأمر المفتوحة لاستيفائها بواسطة متجر المستخدم للأمر المحدد.</span><span class="sxs-lookup"><span data-stu-id="35954-135">Only order lines that are open for fulfillment by the user's store for the selected order will be displayed.</span></span>

- <span data-ttu-id="35954-136">**تحرير** – يتيح للمستخدمين اجراء تغييرات علي أمر العميل المحدد.</span><span class="sxs-lookup"><span data-stu-id="35954-136">**Edit** – Allows users to make changes to the selected customer order.</span></span> <span data-ttu-id="35954-137">تكون الأوامر قابلة للتحرير فقط في [سيناريوهات معينة](customer-orders-overview.md#edit-an-existing-customer-order).</span><span class="sxs-lookup"><span data-stu-id="35954-137">Orders are only editable in [certain scenarios](customer-orders-overview.md#edit-an-existing-customer-order).</span></span>

- <span data-ttu-id="35954-138">**الانتقاء** – يتم توفير هذا الخيار إذا كان الأمر يحتوي على بند واحد أو أكثر تم تعيينه للالتقاط في المتجر الحالي للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="35954-138">**Pick up** – This option will be available if the order has one or more lines designated for pickup at the user's current store.</span></span> <span data-ttu-id="35954-139">تقوم هذه العملية ببدء تدفق الاستلام، والذي يسمح للمستخدم باختيار المنتجات التي سيتم استلامها وإنشاء حركة مبيعات للاستلام.</span><span class="sxs-lookup"><span data-stu-id="35954-139">This operation launches the pickup flow, which allows the user to choose the products to be picked up and creates the pickup sales transaction.</span></span>

## <a name="add-notifications-to-the-recall-order-operation"></a><span data-ttu-id="35954-140">إضافة إخطارات لعملية استدعاء أمر</span><span class="sxs-lookup"><span data-stu-id="35954-140">Add notifications to the recall order operation</span></span>

<span data-ttu-id="35954-141">في الإصدار 10.0.18 والإصدارات الأحدث، يمكنك تكوين إخطارات نقطة البيع وتنبيهات اللوحات المباشرة لعملية **استدعاء الأمر** عند الرغبة في ذلك.</span><span class="sxs-lookup"><span data-stu-id="35954-141">In version 10.0.18 and later, you can configure POS notifications and live tile alerts for the **Order Recall** operation if desired.</span></span> <span data-ttu-id="35954-142">لمزيد من المعلومات، راجع [إظهار إخطارات الأمر في نقطة البيع (POS)](notifications-pos.md).</span><span class="sxs-lookup"><span data-stu-id="35954-142">For more information, see [Show order notifications in the point of sale (POS)](notifications-pos.md).</span></span>  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
