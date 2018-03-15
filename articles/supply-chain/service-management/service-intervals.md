---
title: "فترات الخدمة"
description: "تشير فترة الخدمة إلى تكرار إنشاء بنود أمر الخدمة من أجل بنود اتفاقية الخدمة عند قيامك بإنشاء أوامر الخدمة."
author: YuyuScheller
manager: AnnBe
ms.date: 02/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 4ea10e4c0fbfd21538bba16d2b01deb3e4b3a10d
ms.openlocfilehash: 4a51a3c3483e81cefdaf3d8e62a4f1f47fcd706b
ms.contentlocale: ar-sa
ms.lasthandoff: 02/20/2018

---

# <a name="service-intervals"></a><span data-ttu-id="d7aa8-103">فترات الخدمة</span><span class="sxs-lookup"><span data-stu-id="d7aa8-103">Service intervals</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d7aa8-104">تشير فترة اتفاقية الخدمة إلى تكرار إنشاء بنود أمر الخدمة من أجل بنود اتفاقية الخدمة عند قيامك بإنشاء أوامر الخدمة تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-104">The service agreement interval indicates the frequency with which service order lines are created for service agreement lines when you create service orders automatically.</span></span>

<span data-ttu-id="d7aa8-105">عند قيامك بإنشاء أوامر الخدمة تلقائيًا، يتم إنشاء بنود أمر الخدمة وفقًا للفترة التي حددتها لبند اتفاقية الخدمة من تاريخ بدء بند الاتفاقية.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-105">When you create service orders automatically, service order lines are created according to the interval that you have specified for the service agreement line from the start date of the agreement line.</span></span>

<span data-ttu-id="d7aa8-106">إذا كان حقل **الفترة** في بند اتفاقية الخدمة في الصفحة **اتفاقيات الخدمة** فارغًا، فهذا يعني أن البند عبارة عن حدث لمرة واحدة، ولا يُستخدم لإنشاء أوامر خدمة بشكلٍ متكرر.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-106">If the **Interval** field of a service agreement line in the **Service agreements** page is blank, the line is a one-time event, and it is not used to create service orders repeatedly.</span></span>

## <a name="example"></a><span data-ttu-id="d7aa8-107">مثال</span><span class="sxs-lookup"><span data-stu-id="d7aa8-107">Example</span></span>

<span data-ttu-id="d7aa8-108">يوضح هذا المثال كيفية تأثير فترة الخدمة على بنود اتفاقية الخدمة وبنود أمر الخدمة في أمر خدمة.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-108">This example illustrates how a service interval will affect service agreement lines and service order lines on a service order.</span></span>

### <a name="create-a-service-agreement"></a><span data-ttu-id="d7aa8-109">إنشاء اتفاقية خدمة</span><span class="sxs-lookup"><span data-stu-id="d7aa8-109">Create a service agreement</span></span>

<span data-ttu-id="d7aa8-110">تنشئ أولاً اتفاقية الخدمة وتعين الخيار **تجميع أوامر الخدمة** إلى **حسب اتفاقية الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-110">First, you create a service agreement and set the **Combine service orders** option to **By service agreement**.</span></span>

1. <span data-ttu-id="d7aa8-111">انقر فوق **اتفاقيات الخدمة**</span><span class="sxs-lookup"><span data-stu-id="d7aa8-111">Click **Service agreements**</span></span>
2. <span data-ttu-id="d7aa8-112">في **جزء الإجراءات**، على علامة تبويب **اتفاقية الخدمة**، في المجموعة **جديد**، انقر فوق **اتفاقية الخدمة** لإنشاء اتفاقية خدمة جديدة.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-112">On the **Action Pane**, on the **Service agreement** tab, in the **New** group, click **Service agreement** to create a new service agreement.</span></span>
3. <span data-ttu-id="d7aa8-113">أدخل وصفًا، وحدد مشروعًا في حقل **معرّف المشروع**، وأدخل تاريخًا في حقل **تاريخ البدء**.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-113">Enter a description, select a project in the **Project ID** field, and enter a date in the **Start date** field.</span></span>
4. <span data-ttu-id="d7aa8-114">في الحقل **تجميع أوامر الخدمة**، حدد **حسب اتفاقية الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-114">In the **Combine service orders** field, select **By service agreement**.</span></span>

<span data-ttu-id="d7aa8-115">لقد قمت الآن بإنشاء اتفاقية الخدمة التالية:</span><span class="sxs-lookup"><span data-stu-id="d7aa8-115">You have now created the following service agreement:</span></span>

| <span data-ttu-id="d7aa8-116">Project</span><span class="sxs-lookup"><span data-stu-id="d7aa8-116">Project</span></span>      | <span data-ttu-id="d7aa8-117">تاريخ البدء</span><span class="sxs-lookup"><span data-stu-id="d7aa8-117">Start date</span></span>                                                                         |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d7aa8-118">مشروعك</span><span class="sxs-lookup"><span data-stu-id="d7aa8-118">Your project</span></span> | <span data-ttu-id="d7aa8-119">التاريخ الذي حددته للمشروع.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-119">The date you specified for the project.</span></span> <span data-ttu-id="d7aa8-120">في هذا المثال، يتم استخدام التاريخ الحالي.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-120">In this example, the current date is used.</span></span> |

### <a name="create-a-service-agreement-line"></a><span data-ttu-id="d7aa8-121">إنشاء بند اتفاقية الخدمة</span><span class="sxs-lookup"><span data-stu-id="d7aa8-121">Create a service agreement line</span></span>

<span data-ttu-id="d7aa8-122">بعد ذلك، ستقوم بإنشاء بند اتفاقية خدمة لديه نوع الحركة **ساعة**.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-122">Next, you create a service agreement line that has the transaction type **Hour**.</span></span>

<span data-ttu-id="d7aa8-123">لإكمال هذا الجزء من المثال، يجب عليك إنشاء فترة خدمة تبلغ 10 أيام في صفحة **فترات الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-123">To complete this part of the example, you must create a service interval of 10 days in the **Service intervals** page.</span></span> 

1. <span data-ttu-id="d7aa8-124">حدد اتفاقية الخدمة التي قمت بإنشائها.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-124">Select the service agreement that you just created.</span></span> 
2. <span data-ttu-id="d7aa8-125">على علامة التبويب السريعة **بنود**، انقر فوق الزر **إضافة** لإنشاء بند جديد في الجزء السفلي من صفحة **اتفاقيات الخدمة**</span><span class="sxs-lookup"><span data-stu-id="d7aa8-125">On the **Lines** FastTab, click the **Add** button to create a new line in the lower pane of the **Service agreements** page.</span></span>
3. <span data-ttu-id="d7aa8-126">في الحقل **نوع الحركة**، **ساعة**.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-126">In the **Transaction type** field, select **Hour**.</span></span>
4. <span data-ttu-id="d7aa8-127">في حقل **العامل**، حدد العامل الذي سيقوم بتسليم الخدمة.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-127">In the **Worker** field, select the worker who will deliver the service.</span></span>
5. <span data-ttu-id="d7aa8-128">في الحقل **فاصل الخدمة**، حدد فترة 10 أيام.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-128">In the **Service interval** field, select the 10 days interval.</span></span>

<span data-ttu-id="d7aa8-129">لقد قمت الآن بإنشاء بند اتفاقية خدمة مع المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="d7aa8-129">You have now created a service agreement line with the following information:</span></span>

| <span data-ttu-id="d7aa8-130">نوع الحركة</span><span class="sxs-lookup"><span data-stu-id="d7aa8-130">Transaction type</span></span> | <span data-ttu-id="d7aa8-131">تاريخ البدء</span><span class="sxs-lookup"><span data-stu-id="d7aa8-131">Start date</span></span>                               | <span data-ttu-id="d7aa8-132">فترة الخدمة</span><span class="sxs-lookup"><span data-stu-id="d7aa8-132">Service interval</span></span> |
|------------------|------------------------------------------|------------------|
| <span data-ttu-id="d7aa8-133">ساعة</span><span class="sxs-lookup"><span data-stu-id="d7aa8-133">Hour</span></span>             | <span data-ttu-id="d7aa8-134">التاريخ الحالي.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-134">The current date.</span></span>                        | <span data-ttu-id="d7aa8-135">كل 10 أيام</span><span class="sxs-lookup"><span data-stu-id="d7aa8-135">Every 10 days</span></span>    |
| <span data-ttu-id="d7aa8-136">العامل</span><span class="sxs-lookup"><span data-stu-id="d7aa8-136">Worker</span></span>           | <span data-ttu-id="d7aa8-137">العامل الذي سينفذ بالخدمة.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-137">The worker who will perform the service.</span></span> |                  |

<span data-ttu-id="d7aa8-138">لا يوجد إطار زمني محدد للبند.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-138">There is no time window specified for the line.</span></span> 

### <a name="create-planned-service-orders"></a><span data-ttu-id="d7aa8-139">إنشاء أوامر الخدمة المخططة</span><span class="sxs-lookup"><span data-stu-id="d7aa8-139">Create planned service orders</span></span>

<span data-ttu-id="d7aa8-140">يمكنك الآن إنشاء أوامر الخدمة المخططة وبنود أوامر الخدمة للشهر القادم.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-140">You can now create planned service orders and service order lines for the coming month.</span></span>

1. <span data-ttu-id="d7aa8-141">في صفحة **اتفاقيات الخدمة**، على **جزء الإجراءات**، على علامة التبويب **تسليم**، انقر فوق **أوامر الخدمة المخططة**.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-141">In the **Service agreements** page, on the **Action Pane**, on the **Deliver** tab, click **Planned service orders**.</span></span>
2. <span data-ttu-id="d7aa8-142">في صفحة **إنشاء أوامر الخدمة**، أدخل التاريخ الحالي في الحقل **من تاريخ** وأدخل تاريخًا يقع بعد شهر واحد من التاريخ الحالي في الحقل **إلى تاريخ**.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-142">In the **Create service orders** page, enter the current date in the **From date** field and a date that is one month from the current date in the **To date** field.</span></span>
3. <span data-ttu-id="d7aa8-143">عيّن المربع المنزلق **ساعة** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-143">Set the **Hour** slider to **Yes**.</span></span> 
4. <span data-ttu-id="d7aa8-144">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-144">Click **OK**.</span></span>

<span data-ttu-id="d7aa8-145">نظرًا لعدم وجود تجميع على أمر الخدمة (يتم تحديده بواسطة الخيار **حسب اتفاقية الخدمة** في حقل **دمج أوامر الخدمة**)، يتم إنشاء بند أمر خدمة واحد لكل أمر خدمة.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-145">Because there is no grouping on the service order (defined by the **By service agreement** option in the **Combine service orders** field), one service order line is created per service order.</span></span>

### <a name="service-orders-created"></a><span data-ttu-id="d7aa8-146">أوامر الخدمة التي تم إنشاؤها</span><span class="sxs-lookup"><span data-stu-id="d7aa8-146">Service orders created</span></span>

<span data-ttu-id="d7aa8-147">تقع بنود أوامر الخدمة الثلاثة التي تم إنشاؤها ضمن الإطار الزمني الذي حددته في مربع الحوار **إنشاء أوامر الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-147">Three service order lines have been created within the time frame that you specified in the **Create service orders** dialog box.</span></span> <span data-ttu-id="d7aa8-148">يمكنك عرض بنود أوامر الخدمة في صفحة **اتفاقيات الخدمة** (**جزء الإجراءات** \> علامة التبويب **تسليم** الزر \>**عرض**).</span><span class="sxs-lookup"><span data-stu-id="d7aa8-148">You can view the service order lines in the **Service agreements** page (**Action Pane** \> **Deliver** tab \>**View** button).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7aa8-149">مواضيع مرتبطة</span><span class="sxs-lookup"><span data-stu-id="d7aa8-149">Related topics</span></span>

[<span data-ttu-id="d7aa8-150">إعداد الفواصل الزمنية لخدمة</span><span class="sxs-lookup"><span data-stu-id="d7aa8-150">Set up service intervals</span></span>](set-up-service-intervals.md)  

