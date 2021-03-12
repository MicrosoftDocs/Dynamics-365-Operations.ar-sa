---
title: جداول التسليم
description: تتيح لك جداول التسليم إمكانية تتبع كمية بند الأمر عند استخدام عمليات تسليم متعددة لأمر مبيعات أو عرض أسعار مبيعات أو أمر شراء واحد.
author: ShylaThompson
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchDeliverySchedule, SalesDeliverySchedule, SalesQuotationDeliverySchedule, SalesQuotationDeliverySchedule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 213984
ms.assetid: 44cac104-c36c-4371-a992-9178b3fd65e9
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dfc9467e6c7df70ce749f531bab447513ea3349e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998568"
---
# <a name="delivery-schedules"></a><span data-ttu-id="8a4d7-103">جداول التسليم</span><span class="sxs-lookup"><span data-stu-id="8a4d7-103">Delivery schedules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8a4d7-104">تتيح لك جداول التسليم إمكانية تتبع كمية بند الأمر عند استخدام عمليات تسليم متعددة لأمر مبيعات أو عرض أسعار مبيعات أو أمر شراء واحد.</span><span class="sxs-lookup"><span data-stu-id="8a4d7-104">Delivery schedules allow you to track order line quantity when you are using multiple deliveries for a single sales order, sales quotation, or purchase order.</span></span>

<span data-ttu-id="8a4d7-105">‏‫استخدم جدول تسليم عندما يجب أن يتم تسليم إجمالي الكمية في بند الأمر أو عرض الأسعار في العديد من عمليات الشحن.</span><span class="sxs-lookup"><span data-stu-id="8a4d7-105">Use a delivery schedule when the total quantity on an order or quotation line must be delivered in multiple shipments.</span></span> <span data-ttu-id="8a4d7-106">ويتم تمثيل الشحنات الفردية بواسطة بنود التسليم.</span><span class="sxs-lookup"><span data-stu-id="8a4d7-106">Individual shipments are represented by delivery lines.</span></span> <span data-ttu-id="8a4d7-107">يشكل بندا تسليم أو أكثر جدول تسليم واحد.</span><span class="sxs-lookup"><span data-stu-id="8a4d7-107">Two or more delivery lines make up one delivery schedule.</span></span> <span data-ttu-id="8a4d7-108">وبإمكان بنود التسليم أن تتضمن تواريخ تسليم وكميات وأوضاع تسليم وأبعاد تخزين مختلفة، مثل الموقع والمستودع.</span><span class="sxs-lookup"><span data-stu-id="8a4d7-108">The delivery lines can have different delivery dates, quantities, modes of delivery, and storage dimensions, such as site and warehouse.</span></span>  

<span data-ttu-id="8a4d7-109">**مثال على جدول التسليم**</span><span class="sxs-lookup"><span data-stu-id="8a4d7-109">**Example of a delivery schedule**</span></span>

|                                   |                                          |
|-----------------------------------|------------------------------------------|
| <span data-ttu-id="8a4d7-110">إجمالي الأمر (بند الأمر الأصلي)</span><span class="sxs-lookup"><span data-stu-id="8a4d7-110">Total order (original order line)</span></span> | <span data-ttu-id="8a4d7-111">600 كرسي</span><span class="sxs-lookup"><span data-stu-id="8a4d7-111">600 chairs</span></span>                               |
| <span data-ttu-id="8a4d7-112">جدول التسليم المطلوب</span><span class="sxs-lookup"><span data-stu-id="8a4d7-112">Requested delivery schedule</span></span>       | <span data-ttu-id="8a4d7-113">100 كرسي لكل شهر</span><span class="sxs-lookup"><span data-stu-id="8a4d7-113">100 chairs per month</span></span>                     |
| <span data-ttu-id="8a4d7-114">إطار الوقت المطلوب للتسليم</span><span class="sxs-lookup"><span data-stu-id="8a4d7-114">Requested time frame for delivery</span></span> | <span data-ttu-id="8a4d7-115">6 أشهر، في اليوم الأول من كل شهر</span><span class="sxs-lookup"><span data-stu-id="8a4d7-115">6 months, on the first day of each month</span></span> |

<span data-ttu-id="8a4d7-116">في هذا السيناريو، يطلب العميل تسليم 600 كرسي على دُفعات من 100 كرسي خلال فترة ستة أشهر.</span><span class="sxs-lookup"><span data-stu-id="8a4d7-116">In this scenario, the customer requests delivery of 600 chairs in batches of 100 chairs over a period of six months.</span></span> <span data-ttu-id="8a4d7-117">ولتعقب شروط التسليم، يمكنك إنشاء جدول تسليم.</span><span class="sxs-lookup"><span data-stu-id="8a4d7-117">To keep track of the delivery requirements, you create a delivery schedule.</span></span> <span data-ttu-id="8a4d7-118">وفي صفحة جدولة التسليم، يمكنك إنشاء ستة بنود تسليم منفصلة.</span><span class="sxs-lookup"><span data-stu-id="8a4d7-118">On the delivery schedule page, you create six separate delivery lines.</span></span> <span data-ttu-id="8a4d7-119">ويحتوي كل بند تسليم على 100 كرسي ويشير إلى تاريخ تسليم هذه الكراسي البالغ عددها 100.</span><span class="sxs-lookup"><span data-stu-id="8a4d7-119">Each delivery line contains 100 chairs and indicates the delivery date for those 100 chairs.</span></span> <span data-ttu-id="8a4d7-120">وفي هذه الحالة، تتم إزاحة كل بند في أول الشهر لمدة ستة أشهر متتالية.</span><span class="sxs-lookup"><span data-stu-id="8a4d7-120">In this case, each line is offset on the first of the month for six consecutive months.</span></span>  

<span data-ttu-id="8a4d7-121">وعندما تقوم بإنشاء جدول تسليم، يتغير نوع بند الأمر الأصلي تلقائياً إلى **بند الأمر مع عدة عمليات تسليم**.</span><span class="sxs-lookup"><span data-stu-id="8a4d7-121">When you create a delivery schedule, the type of the original order line is automatically changed to **Order line with multiple deliveries**.</span></span> <span data-ttu-id="8a4d7-122">يُشار إلى البند من هذا النوع كبند تجاري ويتم تمييزه بواسطة رمز.</span><span class="sxs-lookup"><span data-stu-id="8a4d7-122">A line of this type is referred to as a commercial line and is marked by an icon.</span></span> <span data-ttu-id="8a4d7-123">تم وضع علامة على بند التسليم برمز مختلف.</span><span class="sxs-lookup"><span data-stu-id="8a4d7-123">The delivery line is marked by a different icon.</span></span> <span data-ttu-id="8a4d7-124">‏‫إذا قمت بتغيير كمية في بند تسليم، يتم تحديث البند التجاري للكمية الإجمالية لجدول التسليم.</span><span class="sxs-lookup"><span data-stu-id="8a4d7-124">If you change a quantity on a delivery line, the commercial line is updated to the total quantity of the delivery schedule.</span></span> <span data-ttu-id="8a4d7-125">وإذا حددت اتفاقية تجارة خصمًا إجماليًا للأمر، يضمن جدول التسليم أن يكون الأمر مؤهلاً للحصول على إجمالي خصم الأمر، حتى عندما ينقسم الأمر إلى عمليات تسليم منفصلة.‬</span><span class="sxs-lookup"><span data-stu-id="8a4d7-125">If a trade agreement has defined a total discount for the order, the delivery schedule ensures that your order is eligible for the total order discount, even when the order is split into separate deliveries.</span></span>  

<span data-ttu-id="8a4d7-126">تتم معالجة الأوامر المشتملة على جدول تسليم مقابل بنود التسليم.</span><span class="sxs-lookup"><span data-stu-id="8a4d7-126">Orders that have a delivery schedule are processed against the delivery lines.</span></span> <span data-ttu-id="8a4d7-127">تتضمن المعالجة ترحيل إيصالات التعبئة، وعمليات استلام المنتجات، والفواتير.</span><span class="sxs-lookup"><span data-stu-id="8a4d7-127">Processing includes the posting of packing slips, product receipts, and invoicing.</span></span>  

<span data-ttu-id="8a4d7-128">لا تُظهر نسخ المستندات المطبوعة للأوامر وعروض الأسعار التي تشمل جدول تسليم إلا بنود التسليم.</span><span class="sxs-lookup"><span data-stu-id="8a4d7-128">Document printouts of orders and quotations that have a delivery schedule show only the delivery lines.</span></span> <span data-ttu-id="8a4d7-129">ولا تُظهر البنود الأصلية (البنود التجارية).</span><span class="sxs-lookup"><span data-stu-id="8a4d7-129">They don't show the original lines (commercial lines).</span></span> <span data-ttu-id="8a4d7-130">**ملاحظة:** بالإضافة إلى ذلك، لا تظهر سوى بنود التسليم عند تنفيذ هذه الإجراءات:</span><span class="sxs-lookup"><span data-stu-id="8a4d7-130">**Note:** In addition, only the delivery lines are shown when you perform these actions:</span></span>

-   <span data-ttu-id="8a4d7-131">ترحيل</span><span class="sxs-lookup"><span data-stu-id="8a4d7-131">Post</span></span>
-   <span data-ttu-id="8a4d7-132">نسخ الصفحات</span><span class="sxs-lookup"><span data-stu-id="8a4d7-132">Copy pages</span></span>
-   <span data-ttu-id="8a4d7-133">استعراض التقارير وصفحات القوائم</span><span class="sxs-lookup"><span data-stu-id="8a4d7-133">Browse list pages and reports</span></span>

<span data-ttu-id="8a4d7-134">عند تأكيد عروض أسعار المبيعات، تُظهر أوامر المبيعات الناتجة جدول التسليم الكامل، حتى بنود الأمر التي تشتمل على عمليات تسليم متعددة.</span><span class="sxs-lookup"><span data-stu-id="8a4d7-134">When you confirm sales quotations, the resulting sales orders show the whole delivery schedule, even the order lines that have multiple deliveries.</span></span> <span data-ttu-id="8a4d7-135">وبالإضافة إلى ذلك، يتم عرض جدول التسليم الكامل على كافة الصفحات الرئيسية، مثل أوامر المبيعات وعروض أسعار المبيعات وأوامر الشراء.</span><span class="sxs-lookup"><span data-stu-id="8a4d7-135">In addition, the whole delivery schedule is shown on all the major pages, such as sales orders, sales quotations, and purchase orders.</span></span>



