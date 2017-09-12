---
title: "إصدار أوامر الإنتاج"
description: "أمر الإنتاج الذي تم إصداره هو أمر تم تخويله للإنتاج. يُستخدم المصطلح \"تم الإصدار\" لوصف حالة في دورة حياة أمر الإنتاج، حيث يُتاح أمر الإنتاج للتنفيذ في صالة الإنتاج ولعمليات المستودع."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdParmRelease
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2414
ms.assetid: 50c2257b-2924-44f5-b7c1-11f498092053
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: aa38c50a58bed5702332182b9e0827b863f536f7
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---

# <a name="release-production-orders"></a><span data-ttu-id="08202-104">إصدار أوامر الإنتاج</span><span class="sxs-lookup"><span data-stu-id="08202-104">Release production orders</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="08202-105">أمر الإنتاج الذي تم إصداره هو أمر تم تخويله للإنتاج.</span><span class="sxs-lookup"><span data-stu-id="08202-105">A released production order is an order that has been authorized for production.</span></span> <span data-ttu-id="08202-106">يُستخدم المصطلح "تم الإصدار" لوصف حالة في دورة حياة أمر الإنتاج، حيث يُتاح أمر الإنتاج للتنفيذ في صالة الإنتاج ولعمليات المستودع.</span><span class="sxs-lookup"><span data-stu-id="08202-106">The term Released is used to describe a state in the production order life cycle, where the production order is available for execution on the production shop floor and for warehouse processes.</span></span> 

<a name="characteristics-of-the-released-state"></a><span data-ttu-id="08202-107">خصائص الحالة الصادرة</span><span class="sxs-lookup"><span data-stu-id="08202-107">Characteristics of the Released state</span></span>
-------------------------------------

<span data-ttu-id="08202-108">الحالة **الصادرة** هي حالة في دورة حياة أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="08202-108">The **Released** state is one state in the production order life cycle.</span></span> <span data-ttu-id="08202-109">وتتوفر أوامر الإنتاج الموجودة بحالة **صادرة** للتنفيذ في صالة الإنتاج ولعمليات المستودع.</span><span class="sxs-lookup"><span data-stu-id="08202-109">Production orders that are in the **Released** state are available for execution on the production shop floor and for warehouse processes.</span></span> <span data-ttu-id="08202-110">تشمل الحالة **صادرة** الخصائص التالية:</span><span class="sxs-lookup"><span data-stu-id="08202-110">The **Released** state has the following characteristics:</span></span>

-   <span data-ttu-id="08202-111">يمكن تغيير أمر إنتاج إلى الحالة **صادرة** من أمر الإنتاج أو باستخدام عملية دُفعية.</span><span class="sxs-lookup"><span data-stu-id="08202-111">A production order can be changed to the **Released** state either from the production order or by using a batch process.</span></span> <span data-ttu-id="08202-112">كما يمكن تحديث أمر الإنتاج تلقائياً من أوامر الإنتاج المخططة التي تم تأكيدها باستخدام حقل **الحد الزمني للتأكيد‬** في صفحة **الخطة الرئيسية**.</span><span class="sxs-lookup"><span data-stu-id="08202-112">The production order can also be updated automatically from planned production orders that are firmed by using the **Firming time fence** field on the **Master plan** page.</span></span>
-   <span data-ttu-id="08202-113">الحالة **صادرة** عبارة عن إشارة للعمال في صالة الإنتاج لبدء تنفيذ وظائف الإنتاج في صالة الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="08202-113">The **Released** state is the signal for the shop floor operators (operators) to start executing the production jobs on the shop floor.</span></span>
-   <span data-ttu-id="08202-114">توفر أوراق الإنتاج، مثل بطاقات المسار، ووظائف المسار، وبطاقات الوظائف معلومات حول وظائف الإنتاج ويمكن إصدارها.</span><span class="sxs-lookup"><span data-stu-id="08202-114">Production papers, such as route cards, route jobs, and jobs cards provide information about production jobs and can be issued.</span></span>
-   <span data-ttu-id="08202-115">للحصول على المواد المحجوزة فعلياً، يتم إنشاء عمل مستودع لانتقاء المواد لأمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="08202-115">For materials that are physically reserved, warehouse work is generated to pick materials for the production order.</span></span>

## <a name="releasing-jobs-to-the-shop-floor"></a><span data-ttu-id="08202-116">تحرير الوظائف في صالة الإنتاج</span><span class="sxs-lookup"><span data-stu-id="08202-116">Releasing jobs to the shop floor</span></span>
<span data-ttu-id="08202-117">بعد إصدار أمر إنتاج، تصبح وظائف الإنتاج التي ترتبط بالأمر مرئية وجاهزة للتسجيل.</span><span class="sxs-lookup"><span data-stu-id="08202-117">After a production order is released, production jobs that are related to the order are visible and ready for registration.</span></span> <span data-ttu-id="08202-118">‏‫ويمكن للعمال إجراء تسجيلات الوظائف، مثل البدء، والإيقاف، والإكمال سواء في صفحة **الوحدة الطرفية لبطاقة الوظيفة** أو صفحة **جهاز بطاقة الوظيفة**.</span><span class="sxs-lookup"><span data-stu-id="08202-118">The operators can make job registrations, such as Start, Stop, and Completion, on either the **Job card terminal** page or the **Job card device** page.</span></span> <span data-ttu-id="08202-119">ويتم تحويل الوقت والكمية المسجلين تلقائياً من صفحات التسجيل إلى دفاتر يومية الإنتاج لتعقب الوقت والكمية المستهلكين.‬</span><span class="sxs-lookup"><span data-stu-id="08202-119">The registered time and quantity are automatically transferred from the registration pages to production journals to keep track of the consumed time and quantity.</span></span>

## <a name="route-cards"></a><span data-ttu-id="08202-120">بطاقات المسار</span><span class="sxs-lookup"><span data-stu-id="08202-120">Route cards</span></span>
<span data-ttu-id="08202-121">تقدم بطاقة المسار نظرة عامة على المعلومات الواردة من المسار وإعدادات العملية ومن طرق جدولة العمليات والوظائف.</span><span class="sxs-lookup"><span data-stu-id="08202-121">A route card provides an overview of information that comes from route and operation setups, and from operation and job scheduling methods.</span></span>

## <a name="route-jobs"></a><span data-ttu-id="08202-122">قوائم المهام</span><span class="sxs-lookup"><span data-stu-id="08202-122">Route jobs</span></span>
<span data-ttu-id="08202-123">تسرد وظيفة المسار كل وظيفة لعملية معينة بالتفصيل وتتضمن أوقات الإعداد والعملية والانتظار والنقل.</span><span class="sxs-lookup"><span data-stu-id="08202-123">A route job lists each job of an operation in detail, and includes setup, process, queue, and transportation times.</span></span> <span data-ttu-id="08202-124">فمثلاً، قد تتطلب عملية مثل الدهان إجراء وظائف فردية مثل وقت الإعداد ووقت التشغيل لعملية الدهان ووقت الانتظار للتجفيف.</span><span class="sxs-lookup"><span data-stu-id="08202-124">For example, an operation such as painting might require individual jobs, such as setup time, run time for the painting process, and queue time for drying.</span></span>

## <a name="job-cards"></a><span data-ttu-id="08202-125">بطاقات الوظيفة</span><span class="sxs-lookup"><span data-stu-id="08202-125">Job cards</span></span>
<span data-ttu-id="08202-126">تسرد بطاقة الوظيفة أرقام الوظيفة الفردية لعملية بعينها.</span><span class="sxs-lookup"><span data-stu-id="08202-126">A job card lists the individual job numbers of a particular operation.</span></span> <span data-ttu-id="08202-127">وتظهر وظيفة واحدة في كل صفحة.</span><span class="sxs-lookup"><span data-stu-id="08202-127">One job appears on each page.</span></span> <span data-ttu-id="08202-128">وترد الوظائف المتضمنة في بطاقة الوظيفة، وأوقات تقديرها، من معلومات المسار وإعداد العملية.</span><span class="sxs-lookup"><span data-stu-id="08202-128">The jobs that are included on a job card, and their estimated times, come from the route and operation setup information.</span></span> <span data-ttu-id="08202-129">ومن بطاقة وظيفة، يمكنك فتح صفحة **بنود دفتر يومية الإنتاج**، و**بطاقة الوظيفة**.</span><span class="sxs-lookup"><span data-stu-id="08202-129">From a job card, you can open the **Production journal lines**, **job card** page.</span></span> <span data-ttu-id="08202-130">ويمكن للأشخاص الذين يقومون بتشغيل موارد العمليات تقديم ملاحظات حول عملية الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="08202-130">People who run operations resources can provide feedback about the production process.</span></span> <span data-ttu-id="08202-131">وتوجد حقول يمكن إدخال إحصاءات الاستهلاك فيها وكذلك معلومات أخرى مثل كمية الأخطاء.</span><span class="sxs-lookup"><span data-stu-id="08202-131">There are fields where you can enter consumption statistics and information such as the error quantity.</span></span>

## <a name="warehouse-work-for-raw-material-picking"></a><span data-ttu-id="08202-132">عمل المستودع لانتقاء المواد الخام</span><span class="sxs-lookup"><span data-stu-id="08202-132">Warehouse work for raw material picking</span></span>
<span data-ttu-id="08202-133">ويتم إنشاء عمل لانتقاء المواد الخام أثناء الإصدار.</span><span class="sxs-lookup"><span data-stu-id="08202-133">Work for raw material picking is generated during release.</span></span> <span data-ttu-id="08202-134">‏‫ويتم إنشاء العمل فقط لكمية المواد التي تم حجزها فعلياً لأمر الإنتاج قبل إصدار الأمر.</span><span class="sxs-lookup"><span data-stu-id="08202-134">Work is generated only for the quantity of materials that was physically reserved for the production order before the order was released.</span></span> <span data-ttu-id="08202-135">ويُتطلب الإعداد التالي لإنشاء عمل مستودع لانتقاء المواد الخام:‬</span><span class="sxs-lookup"><span data-stu-id="08202-135">The following setup is required to generate warehouse work for raw material picking:</span></span>

-   <span data-ttu-id="08202-136">توجيه موقع لانتقاء المواد الخام يحدد موقع المستودع لانتقاء المواد في</span><span class="sxs-lookup"><span data-stu-id="08202-136">A location directive for raw materials picking that determines which warehouse location to pick the materials in</span></span>
-   <span data-ttu-id="08202-137">قالب موجه للمواد الخام، حيث تم تكوين سياسات لتنفيذ العمل في المستودع</span><span class="sxs-lookup"><span data-stu-id="08202-137">A wave template for raw materials, where policies for the execution of warehouse work are configured</span></span>
-   <span data-ttu-id="08202-138">موقع مدخلات إنتاج يحدد مكان وضع المواد</span><span class="sxs-lookup"><span data-stu-id="08202-138">A production input location that determines where materials are put</span></span>





