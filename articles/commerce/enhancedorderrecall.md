---
title: إعادة استدعاء عملية الأمر في نقطة البيع
description: يشرح هذا الموضوع إمكانيات الميزات المتوفرة لطلب تحسين صفحات الاستدعاء في POS.
author: hhainesms
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 41944fb7819b5527f6bc023a60acd9450d9e43c2
ms.sourcegitcommit: 25909c6ad3616e4f75a2fe006057dda18d7cc856
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/09/2020
ms.locfileid: "3974828"
---
# <a name="recall-order-operation-in-pos"></a><span data-ttu-id="71631-103">إعادة استدعاء عملية الأمر في نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="71631-103">Recall order operation in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="71631-104">توفر عمليه أمر الاستدعاء في نقطه البيع (POS) ميزات بحث وتصفيه أوامر محدثه ومعلومات أمر محدده.</span><span class="sxs-lookup"><span data-stu-id="71631-104">The Recall order operation in the Commerce point of sale (POS) provides updated order search and filtering features and order-specific information.</span></span> <span data-ttu-id="71631-105">تتوفر هذه الميزة في الإصدار 10.0.15 من Commerce والإصدارات اللاحقة.</span><span class="sxs-lookup"><span data-stu-id="71631-105">This feature is available in Commerce versions 10.0.15 and later.</span></span>

<span data-ttu-id="71631-106">لتمكين هذه الوظيفة، قم بتشغيل ميزة **عمليه أمر أعاده الاستدعاء المحسنة في POS** في مساحة عمل **أداره الميزات** في مركز Commerce الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="71631-106">To enable this functionality, turn the **Improved Recall order operation in POS** feature on in **Feature management** workspace in Commerce headquarters.</span></span> <span data-ttu-id="71631-107">بعد تمكين الميزة ، حاول تحديث [تخطيطات الشاشة](pos-screen-layouts.md)في نقطه البيع للاستفادة من الإمكانيات التي تم تغييرها.</span><span class="sxs-lookup"><span data-stu-id="71631-107">After you enable the feature, consider updating your [screen layouts](pos-screen-layouts.md) in POS to take advantage of some of the changed  capabilities.</span></span>

<span data-ttu-id="71631-108">يسمح تكوين زر عملية **أمر الاستدعاء** للمؤسسات لنشر العملية بعرض معرف مسبقا.</span><span class="sxs-lookup"><span data-stu-id="71631-108">The configuration of the **Recall order** operation button allows organizations to deploy the operation with a pre-defined display.</span></span>

![تكوين شبكة الزر](media/recallorderbuttongrid.png)

<span data-ttu-id="71631-110">وخيارات العرض كما يلي.</span><span class="sxs-lookup"><span data-stu-id="71631-110">The display options are as follows.</span></span>
- <span data-ttu-id="71631-111">**بلا** – يقوم هذا الخيار بنشر العملية بدون عرض محدد.</span><span class="sxs-lookup"><span data-stu-id="71631-111">**None** – This option deploys the operation with no specific display.</span></span> <span data-ttu-id="71631-112">عندما يقوم أحد المستخدمين بفتح العملية باستخدام هذا التكوين، ستتم مطالبتهم بالبحث عن الأوامر والبحث عنها أو الاختيار من عامل تصفيه أمر معرف مسبقا.</span><span class="sxs-lookup"><span data-stu-id="71631-112">When a user opens the operation with this configuration, they will be prompted to search and find orders or choose from a pre-defined order filter.</span></span>
- <span data-ttu-id="71631-113">**الأوامر المطلوب تنفيذها** -عندما يقوم مستخدم ببدء العملية، سيتم تشغيل استعلام تلقائيا للبحث عن قائمه بالأوامر التي سيتم استيفاؤها في المتجر وعرضها.</span><span class="sxs-lookup"><span data-stu-id="71631-113">**Orders to fulfill** – When a user launches the operation, a query will run automatically to search and display a list of orders that are to be fulfilled by the store.</span></span> <span data-ttu-id="71631-114">يتم تكوين هذه الأوامر للالتقاط في المتجر أو الشحنة المتجر ولم يتم بعد انتقاء بنود هذه الأوامر أو تعبئتها.</span><span class="sxs-lookup"><span data-stu-id="71631-114">These orders are configured for in-store pickup or store shipment and the lines of these orders have not yet been picked or packed.</span></span>
- <span data-ttu-id="71631-115">**الأوامر المطلوب تنفيذها** -عندما يقوم مستخدم ببدء العملية، سيتم تشغيل استعلام تلقائيا للبحث عن قائمه بالأوامر التي سيتم تكوينها للاستلام داخل المتجر وعرضها للمتجر الحالي للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="71631-115">**Orders to pick up** – When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for in-store pickup at the user's current store.</span></span>
- <span data-ttu-id="71631-116">**الأوامر المطلوب شحنها** - عندما يقوم مستخدم ببدء العملية، سيتم تشغيل استعلام تلقائيا للبحث عن قائمه بالأوامر التي سيتم تكوينها للشحن من المتجر الحالي للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="71631-116">**Orders to ship** - When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for shipment from the user's current store.</span></span>

<span data-ttu-id="71631-117">عند تشغيل عمليه **أمر الاستدعاء** من نقطه البيع، إذا تم تكوين العرض علي **بلا** ، سيكون بإمكان المستخدم البحث عن الأوامر واستردادها بأحدي الطرق التالية.</span><span class="sxs-lookup"><span data-stu-id="71631-117">When launching the **Recall order** operation from POS, if the display is configured to **None** , a user will be able to search and retrieve orders in one of the following ways.</span></span>
- <span data-ttu-id="71631-118">امسح الرموز الشريطية للأمر.</span><span class="sxs-lookup"><span data-stu-id="71631-118">Scan order barcodes.</span></span> <span data-ttu-id="71631-119">سيؤدي ذلك إلى البحث في رقم الأمر ومرجع القناة وحقول معرف الاستلام للتطابقات المطابقة.</span><span class="sxs-lookup"><span data-stu-id="71631-119">This will search order number, channel reference, and receipt ID fields for matches.</span></span>
- <span data-ttu-id="71631-120">حدد أيقونة **أوامر البحث** أو **البحث والتصفية** في شريط التطبيقات لاستخدام اليه التصفية لتحديد موقع الطلبات التي تفي بمعايير التصفية.</span><span class="sxs-lookup"><span data-stu-id="71631-120">Select **Search orders** or **Search and filter** icon on the AppBar to use the filtering mechanism to locate orders that meet the filter criteria.</span></span>
- <span data-ttu-id="71631-121">يمكنك الاختيار من عامل تصفيه معرف مسبقا من القائمة المنسدلة **إظهار الأوامر** (طلبات مطلوب تنفيذها أو طلبات مطلوب استلامها أو طلبات مطلوب شحنها).</span><span class="sxs-lookup"><span data-stu-id="71631-121">Choose from a pre-defined filter from the **Show Orders** drop-down menu (orders to fulfill, orders to pick up, or orders to ship).</span></span>

![القائمة الرئيسية لأوامر الاستدعاء](media/recallordermain.png)

<span data-ttu-id="71631-123">بعد تطبيق معايير البحث، سيعرض التطبيق قائمه بأوامر المبيعات المطابقة.</span><span class="sxs-lookup"><span data-stu-id="71631-123">After search criteria are applied, the application will display a list of matching sales orders.</span></span>

![تفاصيل أمر الاستدعاء](media/orderrecalldetail.png)

<span data-ttu-id="71631-125">يمكن للمستخدم تحديد أحد الأوامر في القائمة لعرض تفاصيل اضافيه.</span><span class="sxs-lookup"><span data-stu-id="71631-125">A user can select an order on the list to view additional details.</span></span> <span data-ttu-id="71631-126">تعرض لوحه المعلومات الموجودة علي الجانب الأيسر التفاصيل حول الأمر المحدد، بما في ذلك تفاصيل بند الأمر وتفاصيل التسليم وتفاصيل الإنجاز.</span><span class="sxs-lookup"><span data-stu-id="71631-126">The information panel on the right side of the screen displays specifics on the selected order, including order line details, delivery details, and fulfillment details.</span></span>

<span data-ttu-id="71631-127">من شريط التطبيقات، يمكن للمستخدم تحديد عمليه.</span><span class="sxs-lookup"><span data-stu-id="71631-127">From the AppBar, a user can select an operation.</span></span> <span data-ttu-id="71631-128">ووفقا لحاله الأمر، قد لا يتم تمكين بعض العمليات.</span><span class="sxs-lookup"><span data-stu-id="71631-128">Depending on the status of the order, certain operations may not be enabled.</span></span>

- <span data-ttu-id="71631-129">**إرجاع** – يستخدم في تنفيذ إرجاع لفاتورة واحده أو أكثر مرتبطة بامر العميل المحدد.</span><span class="sxs-lookup"><span data-stu-id="71631-129">**Return** – Executes a return for one or more invoices related to the selected customer order.</span></span>

- <span data-ttu-id="71631-130">**إلغاء الأمر** – إصدار عمليه إلغاء كامله لأمر التوريد المحدد.</span><span class="sxs-lookup"><span data-stu-id="71631-130">**Cancel** – Issue a full cancellation of the selected sales order.</span></span>

- <span data-ttu-id="71631-131">**التنفيذ** – تحويل المستخدم إلى صفحه استيفاء الأوامر، والذي سيتم تصفيته مسبقا للأمر المحدد.</span><span class="sxs-lookup"><span data-stu-id="71631-131">**Fulfill** – Transfers the user to the order fulfillment page, which will be pre-filtered for the selected order.</span></span> <span data-ttu-id="71631-132">سيتم فقط عرض سطور الأمر المفتوحة لاستيفائها بواسطة متجر المستخدم للأمر المحدد.</span><span class="sxs-lookup"><span data-stu-id="71631-132">Only order lines that are open for fulfillment by the user's store for the selected order will be displayed.</span></span>

- <span data-ttu-id="71631-133">**تحرير** – يتيح للمستخدمين اجراء تغييرات علي أمر العميل المحدد.</span><span class="sxs-lookup"><span data-stu-id="71631-133">**Edit** – Allows users to make changes to the selected customer order.</span></span>

- <span data-ttu-id="71631-134">**استلام** – بدء تشغيل تدفق الاستلام، والذي يسمح للمستخدم باختيار المنتجات التي سيتم استلامها وإنشاء حركه مبيعات للاستلام.</span><span class="sxs-lookup"><span data-stu-id="71631-134">**Pick up** – Launches the pickup flow, which allows the user to choose the products to be picked up and creates the pickup sales transaction.</span></span>
