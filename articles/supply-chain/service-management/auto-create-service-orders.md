---
title: إنشاء أوامر الخدمة تلقائيًا
description: يمكنك إنشاء أوامر الخدمة التي تستند إلى اتفاقية الخدمة طوال فترة سيران اتفاقية الخدمة.
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
ms.openlocfilehash: 53369ef2b7ff93ae4f0523accbc31cc88575a383
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010662"
---
# <a name="automatically-create-service-orders"></a><span data-ttu-id="c8fee-103">إنشاء أوامر الخدمة تلقائيًا</span><span class="sxs-lookup"><span data-stu-id="c8fee-103">Automatically create service orders</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="c8fee-104">يمكنك إنشاء أوامر الخدمة التي تستند إلى اتفاقية الخدمة طوال فترة سيران اتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="c8fee-104">You can generate service orders that are based on a service agreement for the valid period of the service agreement.</span></span>

<span data-ttu-id="c8fee-105">يتم إرفاق أوامر الخدمة التي تقوم بإنشائها من اتفاقية الخدمة إلى اتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="c8fee-105">The service orders that you generate from a service agreement are all attached to the service agreement.</span></span>

<span data-ttu-id="c8fee-106">يتم إنشاء أوامر الخدمة تلقائيًا من الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="c8fee-106">Service orders are generated automatically from the following settings:</span></span>

  - <span data-ttu-id="c8fee-107">فترة اتفاقية الخدمة التي يتم إعدادها في بنود اتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="c8fee-107">The service agreement interval that is set up in the service agreement lines.</span></span> <span data-ttu-id="c8fee-108">تشير فترة اتفاقية الخدمة إلى تكرار إنشاء بنود أمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="c8fee-108">The service agreement interval indicates the frequency that service-order lines are created.</span></span> <span data-ttu-id="c8fee-109">لمزيد من المعلومات، راجع [فترات الخدمة](service-intervals.md).</span><span class="sxs-lookup"><span data-stu-id="c8fee-109">For more information, see [Service intervals](service-intervals.md).</span></span>

  - <span data-ttu-id="c8fee-110">الفترة التي تحددها للخدمة في حقول **من تاريخ** و **إلى تاريخ** في نموذج **إنشاء أوامر خدمة**.</span><span class="sxs-lookup"><span data-stu-id="c8fee-110">The period that you specify to define the service period in the **From date** and **To date** fields in the **Create service orders** form.</span></span> <span data-ttu-id="c8fee-111">لمزيد من المعلومات، راجع [إنشاء أوامر الخدمة تلقائيًا](create-service-orders-automatically.md).</span><span class="sxs-lookup"><span data-stu-id="c8fee-111">For more information, see [Create service orders automatically](create-service-orders-automatically.md).</span></span>

  - <span data-ttu-id="c8fee-112">خيار **تجميع أوامر الخدمة** في رأس اتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="c8fee-112">The **Combine service orders** option on the service agreement header.</span></span> <span data-ttu-id="c8fee-113">يحدد هذا الخيار ما إذا كان سيتم إنشاء بنود أمر الخدمة من اتفاقية الخدمة، ويجمع أوامر الخدمة حسب الموظف أو مهمة الخدمة أو كائن الخدمة أو اتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="c8fee-113">This option defines whether service order lines generated from a service agreement, combines service orders according to employee, service task, service object, or service agreement.</span></span> <span data-ttu-id="c8fee-114">لمزيد من المعلومات، راجع [تجميع أوامر الخدمة](combine-service-orders.md).</span><span class="sxs-lookup"><span data-stu-id="c8fee-114">For more information, see [Combine service orders](combine-service-orders.md).</span></span>

  - <span data-ttu-id="c8fee-115">خيار **الإطار الزمني** في بند اتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="c8fee-115">The **Time window** option on the service agreement line.</span></span> <span data-ttu-id="c8fee-116">يحدد الإطار الزمني إلى أي مدى يُمكن نقل أمر خدمة فيما يتصل بتاريخه المحسوب.</span><span class="sxs-lookup"><span data-stu-id="c8fee-116">The time window defines how far a service order line can move with regard to its calculated date.</span></span> <span data-ttu-id="c8fee-117">لمزيدٍ من المعلومات، راجع [الإطارات الزمنية](time-windows.md).</span><span class="sxs-lookup"><span data-stu-id="c8fee-117">For more information, see [Time windows](time-windows.md).</span></span>


> [!NOTE]
> <P><span data-ttu-id="c8fee-118">إذا لم يكن اليوم المحدد لأمر خدمة مفتوحًا في التقويم الذي حددته في النموذج <STRONG>محددات اتفاقية الخدمة</STRONG>، فستتسلم رسالة بأن هناك تعارضًا في التقويم.</span><span class="sxs-lookup"><span data-stu-id="c8fee-118">If the day that is specified for a service order is not open in the calendar that you have selected in the <STRONG>Service management parameters</STRONG> form, a message will indicate that there is a calendar conflict.</span></span> <span data-ttu-id="c8fee-119">يُمكنك تجاهل الرسالة بشكل آمن، ويتم إنشاء أمر خدمة، حتى في حالة غلق اليوم في التقويم.</span><span class="sxs-lookup"><span data-stu-id="c8fee-119">You can safely ignore the message; the service order will be created, even though the day is closed on the calendar.</span></span></P>

## <a name="example-1"></a><span data-ttu-id="c8fee-120">مثال 1</span><span class="sxs-lookup"><span data-stu-id="c8fee-120">Example 1</span></span>

<span data-ttu-id="c8fee-121">تستمر اتفاقية الخدمة من 1 يناير 2012 حتى 31 ديسمبر 2012.</span><span class="sxs-lookup"><span data-stu-id="c8fee-121">The service agreement lasts from January 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="c8fee-122">إذا كانت فترة الخدمة التي حددتها في نموذج **إنشاء أوامر الخدمة** من 1 نوفمبر 2012 حتى 1 فبراير 2013، يتم إنشاء أوامر الخدمة من 1 نوفمبر 2012 حتى 31 ديسمبر 2012.</span><span class="sxs-lookup"><span data-stu-id="c8fee-122">If the service period that you specify in the **Create service orders** form is from November 1, 2012 until February 1, 2013, service orders are created from November 1, 2012 until December 31, 2012.</span></span>

## <a name="example-2"></a><span data-ttu-id="c8fee-123">مثال 2</span><span class="sxs-lookup"><span data-stu-id="c8fee-123">Example 2</span></span>

<span data-ttu-id="c8fee-124">تستمر اتفاقية الخدمة من 1 يناير 2012 حتى 31 ديسمبر 2012.</span><span class="sxs-lookup"><span data-stu-id="c8fee-124">The service agreement lasts from January 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="c8fee-125">يتم إرفاق بندين من اتفاقية خدمة في اتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="c8fee-125">Two service agreement lines are attached to the service agreement.</span></span> <span data-ttu-id="c8fee-126">يحتوي بند اتفاقية الخدمة الأول على تاريخ بدء 2 يناير 2012 وتاريخ انتهاء في 1 مارس 2012.</span><span class="sxs-lookup"><span data-stu-id="c8fee-126">The first service agreement line has a starting date on January 2, 2012 and an ending date on March 1, 2012.</span></span> <span data-ttu-id="c8fee-127">يحتوي بند اتفاقية الخدمة الثاني على تاريخ بدء 1 أبريل 2012 وتاريخ انتهاء في 31 ديسمبر 2012.</span><span class="sxs-lookup"><span data-stu-id="c8fee-127">The second service agreement line has a starting date on April 1, 2012 and an ending date on December 31, 2012.</span></span> <span data-ttu-id="c8fee-128">عليك تحديد فترة في نموذج **إنشاء أوامر الخدمة** التي تكون من 1 أكتوبر 2012 حتى 31 ديسمبر 2012.</span><span class="sxs-lookup"><span data-stu-id="c8fee-128">You specify a period in the **Create service orders** form that is from October 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="c8fee-129">وبالتالي، يتم إنشاء أوامر الخدمة فقط لبند اتفاقية الخدمة الثاني لأن تاريخ بدء وانتهاء بند الاتفاقية الأول يقع قبل الفترة التي قمت بتحديدها لأمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="c8fee-129">Therefore, service orders are generated only for the second agreement line, because the starting date and ending date of the first agreement line are before the period that you specified for the service order.</span></span>

  


