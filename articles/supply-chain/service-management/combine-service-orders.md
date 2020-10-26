---
title: تجميع أوامر الخدمة
description: يمكنك تجميع أوامر الخدمة.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 17fbed59b1fe7bec80f25f74451872efd61bed62
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976990"
---
# <a name="combine-service-orders"></a><span data-ttu-id="076b7-103">تجميع أوامر الخدمة</span><span class="sxs-lookup"><span data-stu-id="076b7-103">Combine service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="076b7-104">عندما تقوم بإنشاء بنود أوامر الخدمة تلقائياً في نموذج **اتفاقيات الخدمات** ، يمكنك اختيار أحد الخيارات التالية لتحديد الطريقة التي ترغب في تجميعهم حسبها:</span><span class="sxs-lookup"><span data-stu-id="076b7-104">When you create service order lines automatically in the **Service agreements** form, you can choose one of the following options to specify how you want to group them:</span></span>

  - <span data-ttu-id="076b7-105">**بواسطة اتفاقية الخدمات**</span><span class="sxs-lookup"><span data-stu-id="076b7-105">**By service agreement**</span></span>

  - <span data-ttu-id="076b7-106">**بواسطة مهمة الخدمة**</span><span class="sxs-lookup"><span data-stu-id="076b7-106">**By service task**</span></span>

  - <span data-ttu-id="076b7-107">**بواسطة الموظف**</span><span class="sxs-lookup"><span data-stu-id="076b7-107">**By employee**</span></span>

  - <span data-ttu-id="076b7-108">**بواسطة كائن الخدمة**</span><span class="sxs-lookup"><span data-stu-id="076b7-108">**By service object**</span></span>

## <a name="example"></a><span data-ttu-id="076b7-109">مثال</span><span class="sxs-lookup"><span data-stu-id="076b7-109">Example</span></span>

<span data-ttu-id="076b7-110">تقوم بإنشاء اتفاقية خدمة بتاريخ بدء في 03-31-2007.</span><span class="sxs-lookup"><span data-stu-id="076b7-110">You create a service agreement that has a start date on 03-31-2007.</span></span> <span data-ttu-id="076b7-111">في الحقل **تجميع أوامر الخدمة** ، حدد **بواسطة كائن الخدمة** .</span><span class="sxs-lookup"><span data-stu-id="076b7-111">In the **Combine service orders** field, you specify **By service object** .</span></span> <span data-ttu-id="076b7-112">ثم تقوم بعد ذلك بإنشاء بنود اتفاقية الخدمة التالية:</span><span class="sxs-lookup"><span data-stu-id="076b7-112">You then create the following service agreement lines:</span></span>

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
<th><p><span data-ttu-id="076b7-113">رقم سطر الاتفاقية</span><span class="sxs-lookup"><span data-stu-id="076b7-113">Agreement line number</span></span></p></th>
<th><p><span data-ttu-id="076b7-114">نوع الحركة</span><span class="sxs-lookup"><span data-stu-id="076b7-114">Transaction type</span></span></p></th>
<th><p><span data-ttu-id="076b7-115">الوصف</span><span class="sxs-lookup"><span data-stu-id="076b7-115">Description</span></span></p></th>
<th><p><span data-ttu-id="076b7-116">الفترة</span><span class="sxs-lookup"><span data-stu-id="076b7-116">Interval</span></span></p></th>
<th><p><span data-ttu-id="076b7-117">كائن الخدمة</span><span class="sxs-lookup"><span data-stu-id="076b7-117">Service object</span></span></p></th>
<th><p><span data-ttu-id="076b7-118">تاريخ البدء</span><span class="sxs-lookup"><span data-stu-id="076b7-118">Start date</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="076b7-119">1</span><span class="sxs-lookup"><span data-stu-id="076b7-119">1</span></span></p></td>
<td><p><span data-ttu-id="076b7-120"><strong>ساعة</strong></span><span class="sxs-lookup"><span data-stu-id="076b7-120"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="076b7-121">SAL1</span><span class="sxs-lookup"><span data-stu-id="076b7-121">SAL1</span></span></p></td>
<td><p><span data-ttu-id="076b7-122">أسبوعيًا</span><span class="sxs-lookup"><span data-stu-id="076b7-122">Weekly</span></span></p></td>
<td><p><span data-ttu-id="076b7-123">X1-</span><span class="sxs-lookup"><span data-stu-id="076b7-123">X-1</span></span></p></td>
<td><p><span data-ttu-id="076b7-124">01/04/2007</span><span class="sxs-lookup"><span data-stu-id="076b7-124">04-01-2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="076b7-125">2</span><span class="sxs-lookup"><span data-stu-id="076b7-125">2</span></span></p></td>
<td><p><span data-ttu-id="076b7-126"><strong>ساعة</strong></span><span class="sxs-lookup"><span data-stu-id="076b7-126"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="076b7-127">SAL2</span><span class="sxs-lookup"><span data-stu-id="076b7-127">SAL2</span></span></p></td>
<td><p><span data-ttu-id="076b7-128">نصف أسبوعي</span><span class="sxs-lookup"><span data-stu-id="076b7-128">Biweekly</span></span></p></td>
<td><p><span data-ttu-id="076b7-129">X-2</span><span class="sxs-lookup"><span data-stu-id="076b7-129">X-2</span></span></p></td>
<td><p><span data-ttu-id="076b7-130">01/04/2007</span><span class="sxs-lookup"><span data-stu-id="076b7-130">04-01-2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="076b7-131">3</span><span class="sxs-lookup"><span data-stu-id="076b7-131">3</span></span></p></td>
<td><p><span data-ttu-id="076b7-132"><strong>ساعة</strong></span><span class="sxs-lookup"><span data-stu-id="076b7-132"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="076b7-133">SAL3</span><span class="sxs-lookup"><span data-stu-id="076b7-133">SAL3</span></span></p></td>
<td><p><span data-ttu-id="076b7-134">أسبوعيًا</span><span class="sxs-lookup"><span data-stu-id="076b7-134">Weekly</span></span></p></td>
<td><p><span data-ttu-id="076b7-135">X-2</span><span class="sxs-lookup"><span data-stu-id="076b7-135">X-2</span></span></p></td>
<td><p><span data-ttu-id="076b7-136">01/04/2007</span><span class="sxs-lookup"><span data-stu-id="076b7-136">04-01-2007</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="076b7-137">ولم تقم بتحديد إطارات زمنية لأي بند من بنود اتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="076b7-137">You do not specify time windows for any of the service agreement lines.</span></span> <span data-ttu-id="076b7-138">لذلك، لن يتم نقل بنود اتفاقية الخدمة من اليوم المحسوب الذي وقعت فيه.</span><span class="sxs-lookup"><span data-stu-id="076b7-138">Therefore, the service order lines will not move from the calculated day on which they fall.</span></span>

<span data-ttu-id="076b7-139">بعد ذلك، قمت بإنشاء بنود أوامر الخدمة من النموذج **إنشاء أوامر الخدمة** من 04-01-2007 حتى 04-30-2007.</span><span class="sxs-lookup"><span data-stu-id="076b7-139">Next, you generate service order lines from the **Create service orders** form from 04-01-2007 until 04-30-2007.</span></span>

<span data-ttu-id="076b7-140">وفي الإجمالي تم إنشاء 10 أوامر خدمة.</span><span class="sxs-lookup"><span data-stu-id="076b7-140">In total, 10 service orders are created.</span></span> <span data-ttu-id="076b7-141">ونظرًا لأن الإعداد المجمع الذي قمت بتحديده كان **بواسطة كائن الخدمة** ، فإن كافة أوامر الخدمة التي تم إنشاؤها تتضمن بنود أمر خدمة مع كائن خدمة معين واحد فقط.</span><span class="sxs-lookup"><span data-stu-id="076b7-141">Because the combined setting that you selected was **By service object** , all service orders that are created have only service order lines with one specific service object.</span></span> <span data-ttu-id="076b7-142">ويتم تجميع بنود أوامر الخدمة التي تم إنشاؤها من اتفاقية الخدمة والتي لها نفس تاريخ الخدمة ونفس الكائن في نفس أمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="076b7-142">Service order lines that are generated from the service agreement and have the same service date and object are combined on the same service order.</span></span>


> [!NOTE]
> <P><span data-ttu-id="076b7-143">في هذا المثال، لا يتضمن التقويم المحدد في نموذج <STRONG>محددات إدارة الخدمة</STRONG> أي أيام مغلقة.</span><span class="sxs-lookup"><span data-stu-id="076b7-143">In this example, the calendar that is specified in the <STRONG>Service management parameters</STRONG> form has no closed days.</span></span></P>



<span data-ttu-id="076b7-144">يحدث تجميع بنود أوامر الخدمة الإضافية في أوامر الخدمة وفقًا لأي إطار زمني تقوم بتحديده ضمن بنود اتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="076b7-144">Additional grouping of service order lines into service orders occurs according to any time window that you specify on the service agreement lines.</span></span>

## <a name="see-also"></a><span data-ttu-id="076b7-145">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="076b7-145">See also</span></span>

[<span data-ttu-id="076b7-146">إنشاء أوامر الخدمة تلقائيًا</span><span class="sxs-lookup"><span data-stu-id="076b7-146">Create service orders automatically</span></span>](create-service-orders-automatically.md)

  


