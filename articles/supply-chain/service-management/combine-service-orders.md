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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 55de251f7f9cdbae99eaec13d4ddd7d3bf26b2bb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996666"
---
# <a name="combine-service-orders"></a><span data-ttu-id="2c919-103">تجميع أوامر الخدمة</span><span class="sxs-lookup"><span data-stu-id="2c919-103">Combine service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="2c919-104">عندما تقوم بإنشاء بنود أوامر الخدمة تلقائياً في نموذج **اتفاقيات الخدمات**، يمكنك اختيار أحد الخيارات التالية لتحديد الطريقة التي ترغب في تجميعهم حسبها:</span><span class="sxs-lookup"><span data-stu-id="2c919-104">When you create service order lines automatically in the **Service agreements** form, you can choose one of the following options to specify how you want to group them:</span></span>

  - <span data-ttu-id="2c919-105">**بواسطة اتفاقية الخدمات**</span><span class="sxs-lookup"><span data-stu-id="2c919-105">**By service agreement**</span></span>

  - <span data-ttu-id="2c919-106">**بواسطة مهمة الخدمة**</span><span class="sxs-lookup"><span data-stu-id="2c919-106">**By service task**</span></span>

  - <span data-ttu-id="2c919-107">**بواسطة الموظف**</span><span class="sxs-lookup"><span data-stu-id="2c919-107">**By employee**</span></span>

  - <span data-ttu-id="2c919-108">**بواسطة كائن الخدمة**</span><span class="sxs-lookup"><span data-stu-id="2c919-108">**By service object**</span></span>

## <a name="example"></a><span data-ttu-id="2c919-109">مثال</span><span class="sxs-lookup"><span data-stu-id="2c919-109">Example</span></span>

<span data-ttu-id="2c919-110">تقوم بإنشاء اتفاقية خدمة بتاريخ بدء في 03-31-2007.</span><span class="sxs-lookup"><span data-stu-id="2c919-110">You create a service agreement that has a start date on 03-31-2007.</span></span> <span data-ttu-id="2c919-111">في الحقل **تجميع أوامر الخدمة**، حدد **بواسطة كائن الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="2c919-111">In the **Combine service orders** field, you specify **By service object**.</span></span> <span data-ttu-id="2c919-112">ثم تقوم بعد ذلك بإنشاء بنود اتفاقية الخدمة التالية:</span><span class="sxs-lookup"><span data-stu-id="2c919-112">You then create the following service agreement lines:</span></span>

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
<th><p><span data-ttu-id="2c919-113">رقم سطر الاتفاقية</span><span class="sxs-lookup"><span data-stu-id="2c919-113">Agreement line number</span></span></p></th>
<th><p><span data-ttu-id="2c919-114">نوع الحركة</span><span class="sxs-lookup"><span data-stu-id="2c919-114">Transaction type</span></span></p></th>
<th><p><span data-ttu-id="2c919-115">الوصف</span><span class="sxs-lookup"><span data-stu-id="2c919-115">Description</span></span></p></th>
<th><p><span data-ttu-id="2c919-116">الفترة</span><span class="sxs-lookup"><span data-stu-id="2c919-116">Interval</span></span></p></th>
<th><p><span data-ttu-id="2c919-117">كائن الخدمة</span><span class="sxs-lookup"><span data-stu-id="2c919-117">Service object</span></span></p></th>
<th><p><span data-ttu-id="2c919-118">تاريخ البدء</span><span class="sxs-lookup"><span data-stu-id="2c919-118">Start date</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2c919-119">1</span><span class="sxs-lookup"><span data-stu-id="2c919-119">1</span></span></p></td>
<td><p><span data-ttu-id="2c919-120"><strong>ساعة</strong></span><span class="sxs-lookup"><span data-stu-id="2c919-120"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="2c919-121">SAL1</span><span class="sxs-lookup"><span data-stu-id="2c919-121">SAL1</span></span></p></td>
<td><p><span data-ttu-id="2c919-122">أسبوعيًا</span><span class="sxs-lookup"><span data-stu-id="2c919-122">Weekly</span></span></p></td>
<td><p><span data-ttu-id="2c919-123">X1-</span><span class="sxs-lookup"><span data-stu-id="2c919-123">X-1</span></span></p></td>
<td><p><span data-ttu-id="2c919-124">01/04/2007</span><span class="sxs-lookup"><span data-stu-id="2c919-124">04-01-2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c919-125">2</span><span class="sxs-lookup"><span data-stu-id="2c919-125">2</span></span></p></td>
<td><p><span data-ttu-id="2c919-126"><strong>ساعة</strong></span><span class="sxs-lookup"><span data-stu-id="2c919-126"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="2c919-127">SAL2</span><span class="sxs-lookup"><span data-stu-id="2c919-127">SAL2</span></span></p></td>
<td><p><span data-ttu-id="2c919-128">نصف أسبوعي</span><span class="sxs-lookup"><span data-stu-id="2c919-128">Biweekly</span></span></p></td>
<td><p><span data-ttu-id="2c919-129">X-2</span><span class="sxs-lookup"><span data-stu-id="2c919-129">X-2</span></span></p></td>
<td><p><span data-ttu-id="2c919-130">01/04/2007</span><span class="sxs-lookup"><span data-stu-id="2c919-130">04-01-2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c919-131">3</span><span class="sxs-lookup"><span data-stu-id="2c919-131">3</span></span></p></td>
<td><p><span data-ttu-id="2c919-132"><strong>ساعة</strong></span><span class="sxs-lookup"><span data-stu-id="2c919-132"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="2c919-133">SAL3</span><span class="sxs-lookup"><span data-stu-id="2c919-133">SAL3</span></span></p></td>
<td><p><span data-ttu-id="2c919-134">أسبوعيًا</span><span class="sxs-lookup"><span data-stu-id="2c919-134">Weekly</span></span></p></td>
<td><p><span data-ttu-id="2c919-135">X-2</span><span class="sxs-lookup"><span data-stu-id="2c919-135">X-2</span></span></p></td>
<td><p><span data-ttu-id="2c919-136">01/04/2007</span><span class="sxs-lookup"><span data-stu-id="2c919-136">04-01-2007</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2c919-137">ولم تقم بتحديد إطارات زمنية لأي بند من بنود اتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="2c919-137">You do not specify time windows for any of the service agreement lines.</span></span> <span data-ttu-id="2c919-138">لذلك، لن يتم نقل بنود اتفاقية الخدمة من اليوم المحسوب الذي وقعت فيه.</span><span class="sxs-lookup"><span data-stu-id="2c919-138">Therefore, the service order lines will not move from the calculated day on which they fall.</span></span>

<span data-ttu-id="2c919-139">بعد ذلك، قمت بإنشاء بنود أوامر الخدمة من النموذج **إنشاء أوامر الخدمة** من 04-01-2007 حتى 04-30-2007.</span><span class="sxs-lookup"><span data-stu-id="2c919-139">Next, you generate service order lines from the **Create service orders** form from 04-01-2007 until 04-30-2007.</span></span>

<span data-ttu-id="2c919-140">وفي الإجمالي تم إنشاء 10 أوامر خدمة.</span><span class="sxs-lookup"><span data-stu-id="2c919-140">In total, 10 service orders are created.</span></span> <span data-ttu-id="2c919-141">ونظرًا لأن الإعداد المجمع الذي قمت بتحديده كان **بواسطة كائن الخدمة**، فإن كافة أوامر الخدمة التي تم إنشاؤها تتضمن بنود أمر خدمة مع كائن خدمة معين واحد فقط.</span><span class="sxs-lookup"><span data-stu-id="2c919-141">Because the combined setting that you selected was **By service object**, all service orders that are created have only service order lines with one specific service object.</span></span> <span data-ttu-id="2c919-142">ويتم تجميع بنود أوامر الخدمة التي تم إنشاؤها من اتفاقية الخدمة والتي لها نفس تاريخ الخدمة ونفس الكائن في نفس أمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="2c919-142">Service order lines that are generated from the service agreement and have the same service date and object are combined on the same service order.</span></span>


> [!NOTE]
> <P><span data-ttu-id="2c919-143">في هذا المثال، لا يتضمن التقويم المحدد في نموذج <STRONG>محددات إدارة الخدمة</STRONG> أي أيام مغلقة.</span><span class="sxs-lookup"><span data-stu-id="2c919-143">In this example, the calendar that is specified in the <STRONG>Service management parameters</STRONG> form has no closed days.</span></span></P>



<span data-ttu-id="2c919-144">يحدث تجميع بنود أوامر الخدمة الإضافية في أوامر الخدمة وفقًا لأي إطار زمني تقوم بتحديده ضمن بنود اتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="2c919-144">Additional grouping of service order lines into service orders occurs according to any time window that you specify on the service agreement lines.</span></span>

## <a name="see-also"></a><span data-ttu-id="2c919-145">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="2c919-145">See also</span></span>

[<span data-ttu-id="2c919-146">إنشاء أوامر الخدمة تلقائيًا</span><span class="sxs-lookup"><span data-stu-id="2c919-146">Create service orders automatically</span></span>](create-service-orders-automatically.md)

  


