---
title: جداول التسليم
description: تتيح لك جداول التسليم إمكانية تتبع كمية بند الأمر عند استخدام عمليات تسليم متعددة لأمر مبيعات أو عرض أسعار مبيعات أو أمر شراء واحد.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 3dbd66d499b5d5f9f8ef21c0ce3752031a5f4672
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193772"
---
# <a name="delivery-schedules"></a><span data-ttu-id="0eceb-103">جداول التسليم</span><span class="sxs-lookup"><span data-stu-id="0eceb-103">Delivery schedules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0eceb-104">تتيح لك جداول التسليم إمكانية تتبع كمية بند الأمر عند استخدام عمليات تسليم متعددة لأمر مبيعات أو عرض أسعار مبيعات أو أمر شراء واحد.</span><span class="sxs-lookup"><span data-stu-id="0eceb-104">Delivery schedules allow you to track order line quantity when you are using multiple deliveries for a single sales order, sales quotation, or purchase order.</span></span>

<span data-ttu-id="0eceb-105">‏‫استخدم جدول تسليم عندما يجب أن يتم تسليم إجمالي الكمية في بند الأمر أو عرض الأسعار في العديد من عمليات الشحن.</span><span class="sxs-lookup"><span data-stu-id="0eceb-105">Use a delivery schedule when the total quantity on an order or quotation line must be delivered in multiple shipments.</span></span> <span data-ttu-id="0eceb-106">ويتم تمثيل الشحنات الفردية بواسطة بنود التسليم.</span><span class="sxs-lookup"><span data-stu-id="0eceb-106">Individual shipments are represented by delivery lines.</span></span> <span data-ttu-id="0eceb-107">يشكل بندا تسليم أو أكثر جدول تسليم واحد.</span><span class="sxs-lookup"><span data-stu-id="0eceb-107">Two or more delivery lines make up one delivery schedule.</span></span> <span data-ttu-id="0eceb-108">بإمكان بنود التسليم أن تتضمن تواريخ تسليم وكميات وأوضاع تسليم وأبعاد تخزين مختلفة، مثل الموقع والمستودع.</span><span class="sxs-lookup"><span data-stu-id="0eceb-108">The delivery lines can have different delivery dates, quantities, modes of delivery, and storage dimensions, such as site and warehouse.</span></span>  

<span data-ttu-id="0eceb-109">**مثال على جدول التسليم**</span><span class="sxs-lookup"><span data-stu-id="0eceb-109">**Example of a delivery schedule**</span></span>

| <span data-ttu-id="0eceb-110">الصنف</span><span class="sxs-lookup"><span data-stu-id="0eceb-110">Item</span></span>                              | <span data-ttu-id="0eceb-111">قيمة</span><span class="sxs-lookup"><span data-stu-id="0eceb-111">Value</span></span>                                    |
|-----------------------------------|------------------------------------------|
| <span data-ttu-id="0eceb-112">إجمالي الأمر (بند الأمر الأصلي)</span><span class="sxs-lookup"><span data-stu-id="0eceb-112">Total order (original order line)</span></span> | <span data-ttu-id="0eceb-113">600 كرسي</span><span class="sxs-lookup"><span data-stu-id="0eceb-113">600 chairs</span></span>                               |
| <span data-ttu-id="0eceb-114">جدول التسليم المطلوب</span><span class="sxs-lookup"><span data-stu-id="0eceb-114">Requested delivery schedule</span></span>       | <span data-ttu-id="0eceb-115">100 كرسي لكل شهر</span><span class="sxs-lookup"><span data-stu-id="0eceb-115">100 chairs per month</span></span>                     |
| <span data-ttu-id="0eceb-116">إطار الوقت المطلوب للتسليم</span><span class="sxs-lookup"><span data-stu-id="0eceb-116">Requested time frame for delivery</span></span> | <span data-ttu-id="0eceb-117">6 أشهر، في اليوم الأول من كل شهر</span><span class="sxs-lookup"><span data-stu-id="0eceb-117">6 months, on the first day of each month</span></span> |

<span data-ttu-id="0eceb-118">في هذا السيناريو، يطلب العميل تسليم 600 كرسي على دُفعات من 100 كرسي خلال فترة ستة أشهر.</span><span class="sxs-lookup"><span data-stu-id="0eceb-118">In this scenario, the customer requests delivery of 600 chairs in batches of 100 chairs over a period of six months.</span></span> <span data-ttu-id="0eceb-119">ولتعقب شروط التسليم، يمكنك إنشاء جدول تسليم.</span><span class="sxs-lookup"><span data-stu-id="0eceb-119">To keep track of the delivery requirements, you create a delivery schedule.</span></span> <span data-ttu-id="0eceb-120">وفي صفحة جدولة التسليم، يمكنك إنشاء ستة بنود تسليم منفصلة.</span><span class="sxs-lookup"><span data-stu-id="0eceb-120">On the delivery schedule page, you create six separate delivery lines.</span></span> <span data-ttu-id="0eceb-121">ويحتوي كل بند تسليم على 100 كرسي ويشير إلى تاريخ تسليم هذه الكراسي البالغ عددها 100.</span><span class="sxs-lookup"><span data-stu-id="0eceb-121">Each delivery line contains 100 chairs and indicates the delivery date for those 100 chairs.</span></span> <span data-ttu-id="0eceb-122">وفي هذه الحالة، تتم إزاحة كل بند في أول الشهر لمدة ستة أشهر متتالية.</span><span class="sxs-lookup"><span data-stu-id="0eceb-122">In this case, each line is offset on the first of the month for six consecutive months.</span></span>  

<span data-ttu-id="0eceb-123">وعندما تقوم بإنشاء جدول تسليم، يتغير نوع بند الأمر الأصلي تلقائياً إلى **بند الأمر مع عدة عمليات تسليم**.</span><span class="sxs-lookup"><span data-stu-id="0eceb-123">When you create a delivery schedule, the type of the original order line is automatically changed to **Order line with multiple deliveries**.</span></span> <span data-ttu-id="0eceb-124">يُشار إلى البند من هذا النوع كبند تجاري ويتم تمييزه بواسطة رمز.</span><span class="sxs-lookup"><span data-stu-id="0eceb-124">A line of this type is referred to as a commercial line and is marked by an icon.</span></span> <span data-ttu-id="0eceb-125">تم وضع علامة على بند التسليم برمز مختلف.</span><span class="sxs-lookup"><span data-stu-id="0eceb-125">The delivery line is marked by a different icon.</span></span> <span data-ttu-id="0eceb-126">‏‫إذا قمت بتغيير كمية في بند تسليم، يتم تحديث البند التجاري للكمية الإجمالية لجدول التسليم.</span><span class="sxs-lookup"><span data-stu-id="0eceb-126">If you change a quantity on a delivery line, the commercial line is updated to the total quantity of the delivery schedule.</span></span> <span data-ttu-id="0eceb-127">وإذا حددت اتفاقية تجارة خصمًا إجماليًا للأمر، يضمن جدول التسليم أن يكون الأمر مؤهلاً للحصول على إجمالي خصم الأمر، حتى عندما ينقسم الأمر إلى عمليات تسليم منفصلة.‬</span><span class="sxs-lookup"><span data-stu-id="0eceb-127">If a trade agreement has defined a total discount for the order, the delivery schedule ensures that your order is eligible for the total order discount, even when the order is split into separate deliveries.</span></span>  

<span data-ttu-id="0eceb-128">تتم معالجة الأوامر المشتملة على جدول تسليم مقابل بنود التسليم.</span><span class="sxs-lookup"><span data-stu-id="0eceb-128">Orders that have a delivery schedule are processed against the delivery lines.</span></span> <span data-ttu-id="0eceb-129">تتضمن المعالجة ترحيل إيصالات التعبئة، وعمليات استلام المنتجات، والفواتير.</span><span class="sxs-lookup"><span data-stu-id="0eceb-129">Processing includes the posting of packing slips, product receipts, and invoicing.</span></span>  

<span data-ttu-id="0eceb-130">لا تُظهر نسخ المستندات المطبوعة للأوامر وعروض الأسعار التي تشمل جدول تسليم إلا بنود التسليم.</span><span class="sxs-lookup"><span data-stu-id="0eceb-130">Document printouts of orders and quotations that have a delivery schedule show only the delivery lines.</span></span> <span data-ttu-id="0eceb-131">ولا تُظهر البنود الأصلية (البنود التجارية).</span><span class="sxs-lookup"><span data-stu-id="0eceb-131">They don't show the original lines (commercial lines).</span></span> <span data-ttu-id="0eceb-132">**ملاحظة:** بالإضافة إلى ذلك، لا تظهر سوى بنود التسليم عند تنفيذ هذه الإجراءات:</span><span class="sxs-lookup"><span data-stu-id="0eceb-132">**Note:** In addition, only the delivery lines are shown when you perform these actions:</span></span>

-   <span data-ttu-id="0eceb-133">ترحيل</span><span class="sxs-lookup"><span data-stu-id="0eceb-133">Post</span></span>
-   <span data-ttu-id="0eceb-134">نسخ الصفحات</span><span class="sxs-lookup"><span data-stu-id="0eceb-134">Copy pages</span></span>
-   <span data-ttu-id="0eceb-135">استعراض التقارير وصفحات القوائم</span><span class="sxs-lookup"><span data-stu-id="0eceb-135">Browse list pages and reports</span></span>

<span data-ttu-id="0eceb-136">عند تأكيد عروض أسعار المبيعات، تُظهر أوامر المبيعات الناتجة جدول التسليم الكامل، حتى بنود الأمر التي تشتمل على عمليات تسليم متعددة.</span><span class="sxs-lookup"><span data-stu-id="0eceb-136">When you confirm sales quotations, the resulting sales orders show the whole delivery schedule, even the order lines that have multiple deliveries.</span></span> <span data-ttu-id="0eceb-137">وبالإضافة إلى ذلك، يتم عرض جدول التسليم الكامل على كافة الصفحات الرئيسية، مثل أوامر المبيعات وعروض أسعار المبيعات وأوامر الشراء.</span><span class="sxs-lookup"><span data-stu-id="0eceb-137">In addition, the whole delivery schedule is shown on all the major pages, such as sales orders, sales quotations, and purchase orders.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]