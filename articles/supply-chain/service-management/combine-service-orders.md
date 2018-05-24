---
title: "تجميع أوامر الخدمة"
description: "يمكنك تجميع أوامر الخدمة."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 8bc28d03d36d184e4bf41de2c50dac15e6d7813c
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---

# <a name="combine-service-orders"></a><span data-ttu-id="cc459-103">تجميع أوامر الخدمة</span><span class="sxs-lookup"><span data-stu-id="cc459-103">Combine service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="cc459-104">عندما تقوم بإنشاء بنود أوامر الخدمة تلقائياً في نموذج **اتفاقيات الخدمات**، يمكنك اختيار أحد الخيارات التالية لتحديد الطريقة التي ترغب في تجميعهم حسبها:</span><span class="sxs-lookup"><span data-stu-id="cc459-104">When you create service order lines automatically in the **Service agreements** form, you can choose one of the following options to specify how you want to group them:</span></span>

  - <span data-ttu-id="cc459-105">**بواسطة اتفاقية الخدمات**</span><span class="sxs-lookup"><span data-stu-id="cc459-105">**By service agreement**</span></span>

  - <span data-ttu-id="cc459-106">**بواسطة مهمة الخدمة**</span><span class="sxs-lookup"><span data-stu-id="cc459-106">**By service task**</span></span>

  - <span data-ttu-id="cc459-107">**بواسطة الموظف**</span><span class="sxs-lookup"><span data-stu-id="cc459-107">**By employee**</span></span>

  - <span data-ttu-id="cc459-108">**بواسطة كائن الخدمة**</span><span class="sxs-lookup"><span data-stu-id="cc459-108">**By service object**</span></span>

## <a name="example"></a><span data-ttu-id="cc459-109">مثال</span><span class="sxs-lookup"><span data-stu-id="cc459-109">Example</span></span>

<span data-ttu-id="cc459-110">تقوم بإنشاء اتفاقية خدمة بتاريخ بدء في 03-31-2007.</span><span class="sxs-lookup"><span data-stu-id="cc459-110">You create a service agreement that has a start date on 03-31-2007.</span></span> <span data-ttu-id="cc459-111">في الحقل **تجميع أوامر الخدمة**، حدد **بواسطة كائن الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="cc459-111">In the **Combine service orders** field, you specify **By service object**.</span></span> <span data-ttu-id="cc459-112">ثم تقوم بعد ذلك بإنشاء بنود اتفاقية الخدمة التالية:</span><span class="sxs-lookup"><span data-stu-id="cc459-112">You then create the following service agreement lines:</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cc459-113">رقم سطر الاتفاقية</span><span class="sxs-lookup"><span data-stu-id="cc459-113">Agreement line number</span></span></p></th>
<th><p><span data-ttu-id="cc459-114">نوع الحركة</span><span class="sxs-lookup"><span data-stu-id="cc459-114">Transaction type</span></span></p></th>
<th><p><span data-ttu-id="cc459-115">الوصف</span><span class="sxs-lookup"><span data-stu-id="cc459-115">Description</span></span></p></th>
<th><p><span data-ttu-id="cc459-116">الفترة</span><span class="sxs-lookup"><span data-stu-id="cc459-116">Interval</span></span></p></th>
<th><p><span data-ttu-id="cc459-117">كائن الخدمة</span><span class="sxs-lookup"><span data-stu-id="cc459-117">Service object</span></span></p></th>
<th><p><span data-ttu-id="cc459-118">تاريخ البدء</span><span class="sxs-lookup"><span data-stu-id="cc459-118">Start date</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cc459-119">1</span><span class="sxs-lookup"><span data-stu-id="cc459-119">1</span></span></p></td>
<td><p><span data-ttu-id="cc459-120"><strong>ساعة</strong></span><span class="sxs-lookup"><span data-stu-id="cc459-120"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="cc459-121">SAL1</span><span class="sxs-lookup"><span data-stu-id="cc459-121">SAL1</span></span></p></td>
<td><p><span data-ttu-id="cc459-122">أسبوعيًا</span><span class="sxs-lookup"><span data-stu-id="cc459-122">Weekly</span></span></p></td>
<td><p><span data-ttu-id="cc459-123">X1-</span><span class="sxs-lookup"><span data-stu-id="cc459-123">X-1</span></span></p></td>
<td><p><span data-ttu-id="cc459-124">01/04/2007</span><span class="sxs-lookup"><span data-stu-id="cc459-124">04-01-2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc459-125">2</span><span class="sxs-lookup"><span data-stu-id="cc459-125">2</span></span></p></td>
<td><p><span data-ttu-id="cc459-126"><strong>ساعة</strong></span><span class="sxs-lookup"><span data-stu-id="cc459-126"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="cc459-127">SAL2</span><span class="sxs-lookup"><span data-stu-id="cc459-127">SAL2</span></span></p></td>
<td><p><span data-ttu-id="cc459-128">نصف أسبوعي</span><span class="sxs-lookup"><span data-stu-id="cc459-128">Biweekly</span></span></p></td>
<td><p><span data-ttu-id="cc459-129">X-2</span><span class="sxs-lookup"><span data-stu-id="cc459-129">X-2</span></span></p></td>
<td><p><span data-ttu-id="cc459-130">01/04/2007</span><span class="sxs-lookup"><span data-stu-id="cc459-130">04-01-2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc459-131">3</span><span class="sxs-lookup"><span data-stu-id="cc459-131">3</span></span></p></td>
<td><p><span data-ttu-id="cc459-132"><strong>ساعة</strong></span><span class="sxs-lookup"><span data-stu-id="cc459-132"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="cc459-133">SAL3</span><span class="sxs-lookup"><span data-stu-id="cc459-133">SAL3</span></span></p></td>
<td><p><span data-ttu-id="cc459-134">أسبوعيًا</span><span class="sxs-lookup"><span data-stu-id="cc459-134">Weekly</span></span></p></td>
<td><p><span data-ttu-id="cc459-135">X-2</span><span class="sxs-lookup"><span data-stu-id="cc459-135">X-2</span></span></p></td>
<td><p><span data-ttu-id="cc459-136">01/04/2007</span><span class="sxs-lookup"><span data-stu-id="cc459-136">04-01-2007</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cc459-137">ولم تقم بتحديد إطارات زمنية لأي بند من بنود اتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="cc459-137">You do not specify time windows for any of the service agreement lines.</span></span> <span data-ttu-id="cc459-138">لذلك، لن يتم نقل بنود اتفاقية الخدمة من اليوم المحسوب الذي وقعت فيه.</span><span class="sxs-lookup"><span data-stu-id="cc459-138">Therefore, the service order lines will not move from the calculated day on which they fall.</span></span>

<span data-ttu-id="cc459-139">بعد ذلك، قمت بإنشاء بنود أوامر الخدمة من النموذج **إنشاء أوامر الخدمة** من 04-01-2007 حتى 04-30-2007.</span><span class="sxs-lookup"><span data-stu-id="cc459-139">Next, you generate service order lines from the **Create service orders** form from 04-01-2007 until 04-30-2007.</span></span>

<span data-ttu-id="cc459-140">وفي الإجمالي تم إنشاء 10 أوامر خدمة.</span><span class="sxs-lookup"><span data-stu-id="cc459-140">In total, 10 service orders are created.</span></span> <span data-ttu-id="cc459-141">ونظرًا لأن الإعداد المجمع الذي قمت بتحديده كان **بواسطة كائن الخدمة**، فإن كافة أوامر الخدمة التي تم إنشاؤها تتضمن بنود أمر خدمة مع كائن خدمة معين واحد فقط.</span><span class="sxs-lookup"><span data-stu-id="cc459-141">Because the combined setting that you selected was **By service object**, all service orders that are created have only service order lines with one specific service object.</span></span> <span data-ttu-id="cc459-142">ويتم تجميع بنود أوامر الخدمة التي تم إنشاؤها من اتفاقية الخدمة والتي لها نفس تاريخ الخدمة ونفس الكائن في نفس أمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="cc459-142">Service order lines that are generated from the service agreement and have the same service date and object are combined on the same service order.</span></span>


> [!NOTE]
> <P><span data-ttu-id="cc459-143">في هذا المثال، لا يتضمن التقويم المحدد في نموذج <STRONG>محددات إدارة الخدمة</STRONG> أي أيام مغلقة.</span><span class="sxs-lookup"><span data-stu-id="cc459-143">In this example, the calendar that is specified in the <STRONG>Service management parameters</STRONG> form has no closed days.</span></span></P>



<span data-ttu-id="cc459-144">يحدث تجميع بنود أوامر الخدمة الإضافية في أوامر الخدمة وفقًا لأي إطار زمني تقوم بتحديده ضمن بنود اتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="cc459-144">Additional grouping of service order lines into service orders occurs according to any time window that you specify on the service agreement lines.</span></span>

## <a name="see-also"></a><span data-ttu-id="cc459-145">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="cc459-145">See also</span></span>

[<span data-ttu-id="cc459-146">إنشاء أوامر الخدمة تلقائيًا</span><span class="sxs-lookup"><span data-stu-id="cc459-146">Create service orders automatically</span></span>](create-service-orders-automatically.md)

  



