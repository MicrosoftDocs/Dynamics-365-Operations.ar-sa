---
title: "التأخيرات"
description: "توفر هذه المقالة معلومات حول التواريخ المتأخرة في التخطيط الرئيسي. التاريخ المتأخر هو تاريخ استحقاق واقعي تتلقاه الحركة إذا كان أقرب تاريخ تنفيذ يحسبه التخطيط الرئيسي أحدث من التاريخ المطلوب."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ed0df1abbf4f70ea70046eff7b91a25fdd59016c
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="delays"></a><span data-ttu-id="e34c5-104">التأخيرات</span><span class="sxs-lookup"><span data-stu-id="e34c5-104">Delays</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e34c5-105">توفر هذه المقالة معلومات حول التواريخ المتأخرة في التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="e34c5-105">This article provides information about delayed dates in master planning.</span></span> <span data-ttu-id="e34c5-106">التاريخ المتأخر هو تاريخ استحقاق واقعي تتلقاه الحركة إذا كان أقرب تاريخ تنفيذ يحسبه التخطيط الرئيسي أحدث من التاريخ المطلوب.</span><span class="sxs-lookup"><span data-stu-id="e34c5-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="e34c5-107">يمكن للتخطيط الرئيسي حساب أول تاريخ استيفاء للحركة، استناداً إلى أوقات الإنتاج، وتوافر المواد، وتوافر القدرة، ومعلمات التخطيط المختلفة.</span><span class="sxs-lookup"><span data-stu-id="e34c5-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="e34c5-108">وإذا كان التخطيط الرئيسي يحسب تاريخ أمر يسبق التاريخ الحالي، فلا يمكن تنفيذ هذا الأمر في الوقت المحدد.</span><span class="sxs-lookup"><span data-stu-id="e34c5-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="e34c5-109">ولذلك، يتم تأخير الأمر.</span><span class="sxs-lookup"><span data-stu-id="e34c5-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="e34c5-110">وفي هذه الحالة، يقوم التخطيط الرئيسي بالتخطيط مستقبلاً للأمر بدءًا من التاريخ الحالي، ويتضمن أوقات الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="e34c5-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="e34c5-111">وتبدأ أوقات الإنتاج هذه بأية أصناف مكونات ذات مستوى منخفض.</span><span class="sxs-lookup"><span data-stu-id="e34c5-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="e34c5-112">ويتلقى الأمر تاريخًا متأخرًا فيما بعد.</span><span class="sxs-lookup"><span data-stu-id="e34c5-112">The order then receives a delayed date.</span></span> <span data-ttu-id="e34c5-113">والتاريخ المتأخر عبارة عن تاريخ استحقاق واقعي، استناداً إلى البيانات الحالية.</span><span class="sxs-lookup"><span data-stu-id="e34c5-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="e34c5-114">كما يحسب التخطيط الرئيسي عدد أيام التأخير.</span><span class="sxs-lookup"><span data-stu-id="e34c5-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="e34c5-115">وفي بعض الحالات، قد تختار عدم حساب حالات التأخير، مثل عندما يعرف المستخدمون أنه يمكنهم تعجيل أوقات الإنتاج عن طريق تحديد أوضاع التسليم البديلة.</span><span class="sxs-lookup"><span data-stu-id="e34c5-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="e34c5-116">ويمكنك تكوين الكيفية التي يتم بها حساب حالات التأخير لمجموعة تغطية.</span><span class="sxs-lookup"><span data-stu-id="e34c5-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="e34c5-117">ويمكنك فيما بعد إرفاق مجموعة التغطية بصنف لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="e34c5-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="e34c5-118">وفي صفحة **معلمات التخطيط الرئيسي**، يمكنك تعيين وقت البدء لحساب حالات التأخير.</span><span class="sxs-lookup"><span data-stu-id="e34c5-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="e34c5-119">وإذا تم تنفيذ أحد الأوامر بعد هذا الوقت، فستتم عندئذٍ إضافة تأخير ليوم واحد إلى تاريخ تأخر الأمر.</span><span class="sxs-lookup"><span data-stu-id="e34c5-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

<span data-ttu-id="e34c5-120">**ملاحظة:** في الإصدارات السابقة، تُعرف التأخيرات المحسوبة بـ *رسائل العمليات الآجلة*، ويُعرف التاريخ المتأخر بـ *تاريخ العمليات الآجلة*، وتمت الإشارة إلى حركة متأخرة باعتبارها *حركة تم تعيينها للمستقبل*.</span><span class="sxs-lookup"><span data-stu-id="e34c5-120">**Note:** In earlier versions, calculated delays were known as *futures messages*, the delayed date was known as the *futures date*, and a delayed transaction was referred to as *a transaction that was future set*.</span></span>

<a name="see-also"></a><span data-ttu-id="e34c5-121">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="e34c5-121">See also</span></span>
--------

[<span data-ttu-id="e34c5-122">إعدادات التغطية</span><span class="sxs-lookup"><span data-stu-id="e34c5-122">Coverage settings</span></span>](coverage-settings.md)




