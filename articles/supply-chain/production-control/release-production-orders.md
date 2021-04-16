---
title: إصدار أوامر الإنتاج
description: أمر الإنتاج الذي تم إصداره هو أمر تم تخويله للإنتاج. يُستخدم المصطلح "تم الإصدار" لوصف حالة في دورة حياة أمر الإنتاج، حيث يُتاح أمر الإنتاج للتنفيذ في صالة الإنتاج ولعمليات المستودع.
author: johanhoffmann
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProdParmRelease
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2414
ms.assetid: 50c2257b-2924-44f5-b7c1-11f498092053
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 118b0d6300647135b22e42cc84a79f07e48d7ef4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811692"
---
# <a name="release-production-orders"></a><span data-ttu-id="f7c54-104">إصدار أوامر الإنتاج</span><span class="sxs-lookup"><span data-stu-id="f7c54-104">Release production orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f7c54-105">أمر الإنتاج الذي تم إصداره هو أمر تم تخويله للإنتاج.</span><span class="sxs-lookup"><span data-stu-id="f7c54-105">A released production order is an order that has been authorized for production.</span></span> <span data-ttu-id="f7c54-106">يُستخدم المصطلح "تم الإصدار" لوصف حالة في دورة حياة أمر الإنتاج، حيث يُتاح أمر الإنتاج للتنفيذ في صالة الإنتاج ولعمليات المستودع.</span><span class="sxs-lookup"><span data-stu-id="f7c54-106">The term Released is used to describe a state in the production order life cycle, where the production order is available for execution on the production shop floor and for warehouse processes.</span></span>

## <a name="characteristics-of-the-released-state"></a><span data-ttu-id="f7c54-107">خصائص الحالة الصادرة</span><span class="sxs-lookup"><span data-stu-id="f7c54-107">Characteristics of the Released state</span></span>

<span data-ttu-id="f7c54-108">الحالة **الصادرة** هي حالة في دورة حياة أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="f7c54-108">The **Released** state is one state in the production order life cycle.</span></span> <span data-ttu-id="f7c54-109">وتتوفر أوامر الإنتاج الموجودة بحالة **صادرة** للتنفيذ في صالة الإنتاج ولعمليات المستودع.</span><span class="sxs-lookup"><span data-stu-id="f7c54-109">Production orders that are in the **Released** state are available for execution on the production shop floor and for warehouse processes.</span></span> <span data-ttu-id="f7c54-110">تشمل الحالة **صادرة** الخصائص التالية:</span><span class="sxs-lookup"><span data-stu-id="f7c54-110">The **Released** state has the following characteristics:</span></span>

- <span data-ttu-id="f7c54-111">يمكن تغيير أمر إنتاج إلى الحالة **صادرة** من أمر الإنتاج أو باستخدام عملية دُفعية.</span><span class="sxs-lookup"><span data-stu-id="f7c54-111">A production order can be changed to the **Released** state either from the production order or by using a batch process.</span></span> <span data-ttu-id="f7c54-112">كما يمكن تحديث أمر الإنتاج تلقائياً من أوامر الإنتاج المخططة التي تم تأكيدها باستخدام حقل **الحد الزمني للتأكيد‬** في صفحة **الخطة الرئيسية**.</span><span class="sxs-lookup"><span data-stu-id="f7c54-112">The production order can also be updated automatically from planned production orders that are firmed by using the **Firming time fence** field on the **Master plan** page.</span></span>
- <span data-ttu-id="f7c54-113">الحالة **صادرة** عبارة عن إشارة للعمال في صالة الإنتاج لبدء تنفيذ وظائف الإنتاج في صالة الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="f7c54-113">The **Released** state is the signal for the shop floor operators (operators) to start executing the production jobs on the shop floor.</span></span>
- <span data-ttu-id="f7c54-114">توفر أوراق الإنتاج، مثل بطاقات المسار، ووظائف المسار، وبطاقات الوظائف معلومات حول وظائف الإنتاج ويمكن إصدارها.</span><span class="sxs-lookup"><span data-stu-id="f7c54-114">Production papers, such as route cards, route jobs, and jobs cards provide information about production jobs and can be issued.</span></span>
- <span data-ttu-id="f7c54-115">للحصول على المواد المحجوزة فعلياً، يتم إنشاء عمل مستودع لانتقاء المواد لأمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="f7c54-115">For materials that are physically reserved, warehouse work is generated to pick materials for the production order.</span></span>

## <a name="releasing-jobs-to-the-shop-floor"></a><span data-ttu-id="f7c54-116">تحرير الوظائف في صالة الإنتاج</span><span class="sxs-lookup"><span data-stu-id="f7c54-116">Releasing jobs to the shop floor</span></span>

<span data-ttu-id="f7c54-117">بعد إصدار أمر إنتاج، تصبح وظائف الإنتاج التي ترتبط بالأمر مرئية وجاهزة للتسجيل.</span><span class="sxs-lookup"><span data-stu-id="f7c54-117">After a production order is released, production jobs that are related to the order are visible and ready for registration.</span></span> <span data-ttu-id="f7c54-118">‏‫ويمكن للعمال إجراء تسجيلات الوظائف، مثل البدء، والإيقاف، والإكمال سواء في صفحة **الوحدة الطرفية لبطاقة الوظيفة** أو صفحة **جهاز بطاقة الوظيفة**.</span><span class="sxs-lookup"><span data-stu-id="f7c54-118">The operators can make job registrations, such as Start, Stop, and Completion, on either the **Job card terminal** page or the **Job card device** page.</span></span> <span data-ttu-id="f7c54-119">ويتم تحويل الوقت والكمية المسجلين تلقائياً من صفحات التسجيل إلى دفاتر يومية الإنتاج لتعقب الوقت والكمية المستهلكين.‬</span><span class="sxs-lookup"><span data-stu-id="f7c54-119">The registered time and quantity are automatically transferred from the registration pages to production journals to keep track of the consumed time and quantity.</span></span>

## <a name="route-cards"></a><span data-ttu-id="f7c54-120">بطاقات المسار</span><span class="sxs-lookup"><span data-stu-id="f7c54-120">Route cards</span></span>

<span data-ttu-id="f7c54-121">تقدم بطاقة المسار نظرة عامة على المعلومات الواردة من المسار وإعدادات العملية ومن طرق جدولة العمليات والوظائف.</span><span class="sxs-lookup"><span data-stu-id="f7c54-121">A route card provides an overview of information that comes from route and operation setups, and from operation and job scheduling methods.</span></span>

## <a name="route-jobs"></a><span data-ttu-id="f7c54-122">قوائم المهام</span><span class="sxs-lookup"><span data-stu-id="f7c54-122">Route jobs</span></span>

<span data-ttu-id="f7c54-123">تسرد وظيفة المسار كل وظيفة لعملية معينة بالتفصيل وتتضمن أوقات الإعداد والعملية والانتظار والنقل.</span><span class="sxs-lookup"><span data-stu-id="f7c54-123">A route job lists each job of an operation in detail, and includes setup, process, queue, and transportation times.</span></span> <span data-ttu-id="f7c54-124">فمثلاً، قد تتطلب عملية مثل الدهان إجراء وظائف فردية مثل وقت الإعداد ووقت التشغيل لعملية الدهان ووقت الانتظار للتجفيف.</span><span class="sxs-lookup"><span data-stu-id="f7c54-124">For example, an operation such as painting might require individual jobs, such as setup time, run time for the painting process, and queue time for drying.</span></span>

## <a name="job-cards"></a><span data-ttu-id="f7c54-125">بطاقات الوظيفة</span><span class="sxs-lookup"><span data-stu-id="f7c54-125">Job cards</span></span>

<span data-ttu-id="f7c54-126">تسرد بطاقة الوظيفة أرقام الوظيفة الفردية لعملية بعينها.</span><span class="sxs-lookup"><span data-stu-id="f7c54-126">A job card lists the individual job numbers of a particular operation.</span></span> <span data-ttu-id="f7c54-127">وتظهر وظيفة واحدة في كل صفحة.</span><span class="sxs-lookup"><span data-stu-id="f7c54-127">One job appears on each page.</span></span> <span data-ttu-id="f7c54-128">وترد الوظائف المتضمنة في بطاقة الوظيفة، وأوقات تقديرها، من معلومات المسار وإعداد العملية.</span><span class="sxs-lookup"><span data-stu-id="f7c54-128">The jobs that are included on a job card, and their estimated times, come from the route and operation setup information.</span></span> <span data-ttu-id="f7c54-129">ومن بطاقة وظيفة، يمكنك فتح صفحة **بنود دفتر يومية الإنتاج**، و **بطاقة الوظيفة**.</span><span class="sxs-lookup"><span data-stu-id="f7c54-129">From a job card, you can open the **Production journal lines**, **job card** page.</span></span> <span data-ttu-id="f7c54-130">ويمكن للأشخاص الذين يقومون بتشغيل موارد العمليات تقديم ملاحظات حول عملية الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="f7c54-130">People who run operations resources can provide feedback about the production process.</span></span> <span data-ttu-id="f7c54-131">وتوجد حقول يمكن إدخال إحصاءات الاستهلاك فيها وكذلك معلومات أخرى مثل كمية الأخطاء.</span><span class="sxs-lookup"><span data-stu-id="f7c54-131">There are fields where you can enter consumption statistics and information such as the error quantity.</span></span>

## <a name="warehouse-work-for-raw-material-picking"></a><span data-ttu-id="f7c54-132">عمل المستودع لانتقاء المواد الخام</span><span class="sxs-lookup"><span data-stu-id="f7c54-132">Warehouse work for raw material picking</span></span>

<span data-ttu-id="f7c54-133">ويتم إنشاء عمل لانتقاء المواد الخام أثناء الإصدار.</span><span class="sxs-lookup"><span data-stu-id="f7c54-133">Work for raw material picking is generated during release.</span></span> <span data-ttu-id="f7c54-134">‏‫ويتم إنشاء العمل فقط لكمية المواد التي تم حجزها فعلياً لأمر الإنتاج قبل إصدار الأمر.</span><span class="sxs-lookup"><span data-stu-id="f7c54-134">Work is generated only for the quantity of materials that was physically reserved for the production order before the order was released.</span></span> <span data-ttu-id="f7c54-135">ويُتطلب الإعداد التالي لإنشاء عمل مستودع لانتقاء المواد الخام:‬</span><span class="sxs-lookup"><span data-stu-id="f7c54-135">The following setup is required to generate warehouse work for raw material picking:</span></span>

- <span data-ttu-id="f7c54-136">توجيه موقع لانتقاء المواد الخام يحدد موقع المستودع لانتقاء المواد في</span><span class="sxs-lookup"><span data-stu-id="f7c54-136">A location directive for raw materials picking that determines which warehouse location to pick the materials in</span></span>
- <span data-ttu-id="f7c54-137">قالب موجه للمواد الخام، حيث تم تكوين سياسات لتنفيذ العمل في المستودع</span><span class="sxs-lookup"><span data-stu-id="f7c54-137">A wave template for raw materials, where policies for the execution of warehouse work are configured</span></span>
- <span data-ttu-id="f7c54-138">موقع مدخلات إنتاج يحدد مكان وضع المواد</span><span class="sxs-lookup"><span data-stu-id="f7c54-138">A production input location that determines where materials are put</span></span>

<span data-ttu-id="f7c54-139">عند استخدام المواقع التي يتم التحكم فيها من خلال لوحة الترخيص، يمكنك اختيار ما إذا كان يجب انتقاء الكمية المطلوبة أو الكمية الكاملة المتاحة للصنف أثناء معالجة أعمال انتقاء المواد الخام.</span><span class="sxs-lookup"><span data-stu-id="f7c54-139">When using license plate controlled locations, you can choose whether the ordered quantity or the full quantity available for the item should be picked while processing the raw material picking work.</span></span> <span data-ttu-id="f7c54-140">لتعيين هذا الخيار:</span><span class="sxs-lookup"><span data-stu-id="f7c54-140">To set this option:</span></span>

1. <span data-ttu-id="f7c54-141">انتقل إلى **إدارة معلومات المنتج \> المنتجات \> المنتجات الصادرة**، وافتح العنصر ذي الصلة.</span><span class="sxs-lookup"><span data-stu-id="f7c54-141">Go to **Product information management \> Products \> Released products** and open the relevant item.</span></span>
1. <span data-ttu-id="f7c54-142">قم بتوسيع علامة التبويب السريع **المستودع**.</span><span class="sxs-lookup"><span data-stu-id="f7c54-142">Expand the **Warehouse** FastTab.</span></span>
1. <span data-ttu-id="f7c54-143">حدد أحد الخيارات التالية لحقل **انتقاء المواد في مواقع لوحات الترخيص**:</span><span class="sxs-lookup"><span data-stu-id="f7c54-143">Select one of the following options for the  **Material picking in license plate locations** field:</span></span>
    - <span data-ttu-id="f7c54-144">*انتقاء الأوامر*: يجب اختيار الكمية المطلوبة فقط.</span><span class="sxs-lookup"><span data-stu-id="f7c54-144">*Order picking*: Only the ordered quantity should be picked.</span></span>
    - <span data-ttu-id="f7c54-145">*التشغيل المرحلي*: كلما كان ذلك ممكنًا، يجب اختيار الكمية الكاملة المتوفرة على لوحة الترخيص.</span><span class="sxs-lookup"><span data-stu-id="f7c54-145">*Staging*: Whenever possible, the full quantity available at the license plate should be picked.</span></span> <span data-ttu-id="f7c54-146">لكي يتمكن العامل من اختيار الكمية الكاملة للوحة الترخيص، يجب ألا تحتوي لوحة الترخيص على عناصر مختلطة ويجب ألا تحتوي على أبعاد مختلطة.</span><span class="sxs-lookup"><span data-stu-id="f7c54-146">For a worker to be able to pick the full license plate quantity, the license plate must not contain mixed items and must not have mixed dimensions.</span></span> <span data-ttu-id="f7c54-147">إذا كانت لوحة الترخيص تحتوي على أبعاد أو عناصر مختلطة، فسيستمر الانتقاء كما لو كان مضبوطًا على *انتقاء الأوامر*.</span><span class="sxs-lookup"><span data-stu-id="f7c54-147">If the license plate contains mixed dimensions or items, the pick will proceed as if it were set to *Order picking*.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]