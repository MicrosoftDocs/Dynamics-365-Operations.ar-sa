---
title: معالة عمليات التقاط أمر العميل في نقطة البيع
description: يوضح هذا الموضوع الوظيفة المتوفرة في تطبيق نقطm البيع (POS) لمعالج عمليات انتقاء أمر العميل.
author: Hhainesms
manager: annbe
ms.date: 01/06/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 2156542ed0932fab6fb4fa4035e009ad89eeb18f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003743"
---
# <a name="process-customer-order-pickups-in-pos"></a><span data-ttu-id="e7ac8-103">معالة عمليات التقاط أمر العميل في نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="e7ac8-103">Process customer order pickups in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e7ac8-104">عند إنشاء [أمر عميل](customer-orders-overview.md) للانتقاء للمتجر، يمكن لمستخدم المتجر استخدام تطبيق نقطة بيع (POS) لبدء انتقاء المخزون.</span><span class="sxs-lookup"><span data-stu-id="e7ac8-104">When a [customer order](customer-orders-overview.md) is created for store pickup, a store user can use the point of sale (POS) application to start the pickup of inventory.</span></span> <span data-ttu-id="e7ac8-105">سوف تقوم نقطة البيع بتشغيل التقاط الدفع النهائي حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="e7ac8-105">POS will run the final payment capture as required.</span></span> <span data-ttu-id="e7ac8-106">كما ستقوم بإكمال المخزون والترحيل المالي للكميات التي يتم انتقاؤها.</span><span class="sxs-lookup"><span data-stu-id="e7ac8-106">It will also complete the inventory and financial posting for the quantities that are picked up.</span></span>

<span data-ttu-id="e7ac8-107">إذا كنت مستخدمًا لمتجر، فيمكنك إجراء التقاط باستخدام إما عملية **استدعاء أمر** أو **عملية استيفاء الأمر** في نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="e7ac8-107">If you're a store user, you can perform the pickup by using either the **Recall order** operation or the **Order fulfillment** operation in POS.</span></span> <span data-ttu-id="e7ac8-108">لجعل **عملية الانتقاء** متاحة، يجب أولا اتباع إحدى الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="e7ac8-108">To make the **Pick up** operation available, you must first follow one of these steps:</span></span>

- <span data-ttu-id="e7ac8-109">لاستخدام عملية **استدعاء الأمر**، قم بالبحث عن الأمر الذي سيتم انتقاؤه وحدده.</span><span class="sxs-lookup"><span data-stu-id="e7ac8-109">To use the **Recall order** operation, search for and select the order that will be picked up.</span></span>
- <span data-ttu-id="e7ac8-110">لاستخدام **عملية استيفاء الأمر**، قم بالبحث عن بنود أمر واحد أو أكثر وحدده.</span><span class="sxs-lookup"><span data-stu-id="e7ac8-110">To use the **Order fulfillment** operation, search for and select one or more order lines.</span></span>

<span data-ttu-id="e7ac8-111">إذا لم يتم تكوين الأمر المحدد أو بنود الأمر لالتقاطها في هذا المتجر المحدد، أو إذا كان الأمر قد تم انتقاؤه بالكامل، فلن تكون عملية **الانتقاء** متاحة.</span><span class="sxs-lookup"><span data-stu-id="e7ac8-111">If the selected order or order lines aren't configured for pickup at that specific store, or if the order has already been fully picked up, the **Pick up** operation will be unavailable.</span></span>

![عملية الانتقاء](media/pickupoperation.png)

<span data-ttu-id="e7ac8-113">في Microsoft Dynamics 365 Commerce الإصدار 10.0.17 والأحدث، يمكن تشغيل ميزة **تجربة المستخدم المحسنة لانتقاء طلب المعالجة في نقطة البيع** من خلال إدارة الميزات في المركز الرئيسي لـ Commerce.</span><span class="sxs-lookup"><span data-stu-id="e7ac8-113">In Microsoft Dynamics 365 Commerce version 10.0.17 and later, the **Improved user experience for pick up order processing in Point of Sale** feature can be turned on through Feature management in Commerce headquarters.</span></span> <span data-ttu-id="e7ac8-114">إذا تم إيقاف تشغيل هذه الميزة، فلن يتمكن المستخدمون من تحديد كميات الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="e7ac8-114">If this feature is turned off, users can't select pickup quantities.</span></span> <span data-ttu-id="e7ac8-115">افتراضيًا، تكون الكمية الكاملة التي تم طلبها للبند هي الكمية التي سيتم انتقاؤها.</span><span class="sxs-lookup"><span data-stu-id="e7ac8-115">By default, the full quantity that was ordered for the line is the quantity that will be picked up.</span></span> <span data-ttu-id="e7ac8-116">يمكن أن تكون هذه التجربة منوطة بالمشكلات، لأن المستخدمين قد ينسون تحديد بعض الأصناف لالتقاطها عند قيامهم بإجراء التقاط من خلال استيفاء الأمر.</span><span class="sxs-lookup"><span data-stu-id="e7ac8-116">This experience can be problematic, because users might forget to select some items for pickup when they perform the pickup through order fulfillment.</span></span>

<span data-ttu-id="e7ac8-117">تمنح ميزة **تجربة المستخدم المحسنة لانتقاء طلب المعالجة في نقطة البيع** للمستخدمين المزيد من التحكم في تحديد المنتجات التي سيتم انتقاؤها وكمية تلك المنتجات التي سيتم انتقاؤها.</span><span class="sxs-lookup"><span data-stu-id="e7ac8-117">The **Improved user experience for pick up order processing in Point of Sale** feature gives users more control over the selection of products that will be picked up and the quantity of those products that will be picked up.</span></span> <span data-ttu-id="e7ac8-118">لا يجب على المستخدمين تحديد كل بند من أوامر المبيعات في صفحة استيفاء الأوامر قبل تحديد **انتقاء**.</span><span class="sxs-lookup"><span data-stu-id="e7ac8-118">Users don't have to select every line of the sales order on the order fulfillment page before they select **Pick up**.</span></span> <span data-ttu-id="e7ac8-119">سيتم عرض كافة الأصناف التي يمكن انتقاؤها.</span><span class="sxs-lookup"><span data-stu-id="e7ac8-119">All the items that can be picked up will be shown.</span></span> <span data-ttu-id="e7ac8-120">يمكن للمستخدمين تحديد بنود متعددة للالتقاطها حتى في حالة تحديد خط إنتاج واحد فقط.</span><span class="sxs-lookup"><span data-stu-id="e7ac8-120">Users can specify multiple lines for pickup even if only one product line is selected.</span></span>

<span data-ttu-id="e7ac8-121">عندما يتم تشغيل **تجربة المستخدم المحسنة لانتقاء طلب المعالجة في نقطة البيع**، وقمت بتحديد **عملية الانتقاء**، فسوف ينظهر مربع حوار **الانتقاء**.</span><span class="sxs-lookup"><span data-stu-id="e7ac8-121">When the **Improve user experience for pick up order processing in Point of Sale** feature is turned on, and you select the **Pick up** operation, the **Pick up** dialog box appears.</span></span> <span data-ttu-id="e7ac8-122">هناك، يمكنك تحديد الأصناف والكميات التي سيتم انتقاؤها.</span><span class="sxs-lookup"><span data-stu-id="e7ac8-122">There, you can select the items and quantities that will be picked up.</span></span> <span data-ttu-id="e7ac8-123">بشكل افتراضي، يتم اعتبار أي كمية مطلوبة لها مخزون بالحالة منتقاة أو معبأة مؤهلة للالتقاط.</span><span class="sxs-lookup"><span data-stu-id="e7ac8-123">By default, any ordered quantity that has inventory in a picked or packed state is considered eligible for pickup.</span></span> <span data-ttu-id="e7ac8-124">بشكل افتراضي، يتم تعيين تلك الكمية ككمية انتقاء.</span><span class="sxs-lookup"><span data-stu-id="e7ac8-124">By default, that quantity is set as the pickup quantity.</span></span> <span data-ttu-id="e7ac8-125">يمكنك تغيير الكمية التي تم إدخالها، بشرط أن تكون الكمية ليست 0 (صفرا) ولا تتجاوز الكمية الإجمالية المفتوحة (أي بالحالة غير مفوترة) للبند المحدد.</span><span class="sxs-lookup"><span data-stu-id="e7ac8-125">You can change the quantity that was entered, provided that the quantity isn't 0 (zero) and doesn't exceed the total open (that is, non-invoiced) quantity for the selected line.</span></span>

![مربع الحوار انتقاء](media/pickupselect.png)

<span data-ttu-id="e7ac8-127">بعد تحديد الكميات التي سيتم انتقاؤها ثم تحديد **انتقاء**"، تظهر صفحة الحركة.</span><span class="sxs-lookup"><span data-stu-id="e7ac8-127">After you select the quantities that will be picked up and then select **Pick up**, the transaction page appears.</span></span> <span data-ttu-id="e7ac8-128">إذا تم تشغيل ميزة [مدفوعات القناة متعددة الاتجاهات](omni-channel-payments.md)، وكانت هناك مدفوعات بطاقة ائتمان معتمدة مسبقا في الملف، فيجب عليك تطبيق الدفع.</span><span class="sxs-lookup"><span data-stu-id="e7ac8-128">If the [omni-channel payments](omni-channel-payments.md) feature is turned on, and there are pre-authorized credit card payments on file, you must apply the payment.</span></span>

<span data-ttu-id="e7ac8-129">في صفحة الحركة، يقوم النظام بحساب المبالغ المستحقة عن طريق حساب الإجمالي المستحق لأصناف الانتقاء المحددة ثم يطرح أي ودائع تم تطبيقها مسبقا أو مدفوعات بطاقة ائتمان معتمدة.</span><span class="sxs-lookup"><span data-stu-id="e7ac8-129">On the transaction page, the system calculates the amounts that are due by calculating the total that is due for the selected pickup items and then subtracting any previously applied deposits or authorized credit card payments.</span></span> <span data-ttu-id="e7ac8-130">يجب عليك معالجة الدفع لإكمال حركة الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="e7ac8-130">You must process payment to complete the pickup transaction.</span></span> <span data-ttu-id="e7ac8-131">في حالة تكوين [تخطيط الشاشة](pos-screen-layouts.md) لصفحة الحركة بحيث تشتمل على عملية **إنجاز الحركة**، ولا يوجد أي مبلغ مستحق، فيمكنك إكمال الحركة دون تحديد طريقة الدفع.</span><span class="sxs-lookup"><span data-stu-id="e7ac8-131">If the [screen layout](pos-screen-layouts.md) of the transaction page is configured so that it includes the **Conclude transaction** operation, and no amount is due, you can complete the transaction without selecting a payment method.</span></span> <span data-ttu-id="e7ac8-132">في حالة عدم توفر عملية **إنجاز الحركة**، يمكنك تحديد الارتباط **مبلغ $0.00 مستحق** في جزء **الإجماليات** لإنجاز الحركة دون الحاجة إلى تحديد طريقة الدفع.</span><span class="sxs-lookup"><span data-stu-id="e7ac8-132">If the **Conclude transaction** operation isn't available, you can select the **$0.00 amount due** link in the **Totals** pane to conclude the transaction without having to select a payment method.</span></span>

![صفحة الحركة لحركة انتقاء أمر العميل](media/pickupcart.png)

## <a name="changing-pickup-lines-or-quantities"></a><span data-ttu-id="e7ac8-134">تغيير بنود الانتقاء أو كمياته</span><span class="sxs-lookup"><span data-stu-id="e7ac8-134">Changing pickup lines or quantities</span></span>

<span data-ttu-id="e7ac8-135">إذا كان من الضروري تغيير كمية الانتقاء بعد تحديد الأصناف التي سيتم انتقاؤها، فيمكنك تحديد **تعيين الكمية**.</span><span class="sxs-lookup"><span data-stu-id="e7ac8-135">If you must change the pickup quantity after you've selected the items that will be picked up, you can select **Set quantity**.</span></span> <span data-ttu-id="e7ac8-136">لا يمكنك تعيين كمية الانتقاء إلى **0** (صفر) أو زيادتها إلى قيمة تتجاوز الكمية غير المفوتره المتبقية للبند المطلوب.</span><span class="sxs-lookup"><span data-stu-id="e7ac8-136">You can't set the pickup quantity to **0** (zero) or increase it to a value that exceeds the non-invoiced quantity that remains for the ordered line.</span></span> <span data-ttu-id="e7ac8-137">لإزالة بند انتقاء من سلة الحركات، حدد **إلغاء الحركة**.</span><span class="sxs-lookup"><span data-stu-id="e7ac8-137">To remove a pickup line from the transaction cart, select **Void transaction**.</span></span> <span data-ttu-id="e7ac8-138">سيتم إيقاف الحركة الحالية، وسيتم إعادة تشغيل تدفق عملية **الانتقاء**.</span><span class="sxs-lookup"><span data-stu-id="e7ac8-138">The current transaction will be stopped, and the flow for the **Pick up** operation will be restarted.</span></span>

<span data-ttu-id="e7ac8-139">إذا كانت **تجربة المستخدم المحسنة لانتقاء طلب المعالجة في نقطة البيع** قيد التشغيل، فيمكن للمؤسسات إضافة زر لعملية **تغيير بنود الانتقاء** في تخطيط الشاشة لصفحة الحركة.</span><span class="sxs-lookup"><span data-stu-id="e7ac8-139">If the **Improve user experience for pick up order processing in Point of Sale** feature is turned on, organizations can add a button for the **Change pickup lines** operation to the screen layout of the transaction page.</span></span> <span data-ttu-id="e7ac8-140">بعد إنشاء سلة حركة الانتقاء في نقطة البيع وتحديد الأصناف، يمكنك تحديد **تغيير بنود الانتقاء** إذا كان من الضروري تغيير أصناف الانتقاء ولكن لا ترغب في إلغاء الحركة بالكامل.</span><span class="sxs-lookup"><span data-stu-id="e7ac8-140">After you create the pickup transaction cart in POS and select items, you can select **Change pickup lines** if you must change the pickup items but don't want to void the whole transaction.</span></span> <span data-ttu-id="e7ac8-141">في مربع الحوار **تغيير بنود الانتقاء** الذي يظهر، يمكنك تغيير أصناف الانتقاء وكمياته.</span><span class="sxs-lookup"><span data-stu-id="e7ac8-141">In the **Change pickup lines** dialog box that appears, you can change the pickup items and quantities.</span></span> <span data-ttu-id="e7ac8-142">بعد ذلك يتم تحديث سلة الحركات لتعكس التغييرات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="e7ac8-142">The transaction cart is then updated to reflect your changes.</span></span>

![مربع الحوار تغيير أصناف الانتقاء](media/pickupchange.png)