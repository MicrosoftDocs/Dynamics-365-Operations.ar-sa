---
title: التأخيرات
description: يوفر هذا الموضوع معلومات حول التواريخ المتأخرة في التخطيط الرئيسي. التاريخ المتأخر هو تاريخ استحقاق واقعي تتلقاه الحركة إذا كان أقرب تاريخ تنفيذ يحسبه التخطيط الرئيسي أحدث من التاريخ المطلوب.
author: roxanadiaconu
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 195a966ea8baee7783af84ec5f178d7c35ee5cea
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207077"
---
# <a name="delays"></a><span data-ttu-id="8ce5b-104">التأخيرات</span><span class="sxs-lookup"><span data-stu-id="8ce5b-104">Delays</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ce5b-105">يوفر هذا الموضوع معلومات حول التواريخ المتأخرة في التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="8ce5b-105">This topic provides information about delayed dates in master planning.</span></span> <span data-ttu-id="8ce5b-106">التاريخ المتأخر هو تاريخ استحقاق واقعي تتلقاه الحركة إذا كان أقرب تاريخ تنفيذ يحسبه التخطيط الرئيسي أحدث من التاريخ المطلوب.</span><span class="sxs-lookup"><span data-stu-id="8ce5b-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="8ce5b-107">يمكن للتخطيط الرئيسي حساب أول تاريخ استيفاء للحركة، استناداً إلى أوقات الإنتاج، وتوافر المواد، وتوافر القدرة، ومعلمات التخطيط المختلفة.</span><span class="sxs-lookup"><span data-stu-id="8ce5b-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="8ce5b-108">وإذا كان التخطيط الرئيسي يحسب تاريخ أمر يسبق التاريخ الحالي، فلا يمكن تنفيذ هذا الأمر في الوقت المحدد.</span><span class="sxs-lookup"><span data-stu-id="8ce5b-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="8ce5b-109">ولذلك، يتم تأخير الأمر.</span><span class="sxs-lookup"><span data-stu-id="8ce5b-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="8ce5b-110">وفي هذه الحالة، يقوم التخطيط الرئيسي بالتخطيط مستقبلاً للأمر بدءًا من التاريخ الحالي، ويتضمن أوقات الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="8ce5b-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="8ce5b-111">وتبدأ أوقات الإنتاج هذه بأية أصناف مكونات ذات مستوى منخفض.</span><span class="sxs-lookup"><span data-stu-id="8ce5b-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="8ce5b-112">ويتلقى الأمر تاريخًا متأخرًا فيما بعد.</span><span class="sxs-lookup"><span data-stu-id="8ce5b-112">The order then receives a delayed date.</span></span> <span data-ttu-id="8ce5b-113">والتاريخ المتأخر عبارة عن تاريخ استحقاق واقعي، استناداً إلى البيانات الحالية.</span><span class="sxs-lookup"><span data-stu-id="8ce5b-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="8ce5b-114">كما يحسب التخطيط الرئيسي عدد أيام التأخير.</span><span class="sxs-lookup"><span data-stu-id="8ce5b-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="8ce5b-115">وفي بعض الحالات، قد تختار عدم حساب حالات التأخير، مثل عندما يعرف المستخدمون أنه يمكنهم تعجيل أوقات الإنتاج عن طريق تحديد أوضاع التسليم البديلة.</span><span class="sxs-lookup"><span data-stu-id="8ce5b-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="8ce5b-116">ويمكنك تكوين الكيفية التي يتم بها حساب حالات التأخير لمجموعة تغطية.</span><span class="sxs-lookup"><span data-stu-id="8ce5b-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="8ce5b-117">ويمكنك فيما بعد إرفاق مجموعة التغطية بصنف لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="8ce5b-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="8ce5b-118">وفي صفحة **معلمات التخطيط الرئيسي**، يمكنك تعيين وقت البدء لحساب حالات التأخير.</span><span class="sxs-lookup"><span data-stu-id="8ce5b-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="8ce5b-119">وإذا تم تنفيذ أحد الأوامر بعد هذا الوقت، فستتم عندئذٍ إضافة تأخير ليوم واحد إلى تاريخ تأخر الأمر.</span><span class="sxs-lookup"><span data-stu-id="8ce5b-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

> [!NOTE]
> <span data-ttu-id="8ce5b-120">في الإصدارات السابقة، كانت التأخيرات المحسوبة تُعرف باسم *رسائل العمليات الآجلة‬*, وكان التاريخ المتأخر يُعرف باسم *تاريخ العمليات الآجلة*، وكان يشار إلى الحركة المتأخرة على أنها *حركة تم تعيينها للمستقبل*.</span><span class="sxs-lookup"><span data-stu-id="8ce5b-120">In earlier versions, calculated delays were known as *futures messages*, the delayed date was known as the *futures date*, and a delayed transaction was referred to as *a transaction that was future set*.</span></span>

## <a name="limited-delays-in-production-setup-with-multiple-bom-levels"></a><span data-ttu-id="8ce5b-121">حالات تأخير محدودة في إعداد الإنتاج مع مستويات متعددة لقائمة مكونات الصنف‬</span><span class="sxs-lookup"><span data-stu-id="8ce5b-121">Limited delays in production setup with multiple BOM levels</span></span>
<span data-ttu-id="8ce5b-122">عندما تعمل مع حالات تأخير في إعداد الإنتاج لديه مستويات متعددة لقائمة مكونات الصنف‬، من الضروري الملاحظة أنه سيتم تحديث فقط الأصناف الموجودة فوق الصنف (في بنية قائمة مكونات الصنف‬) التي تسبب التأخير، كجزء من تشغيل التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="8ce5b-122">When you work with delays in a production setup that has multiple BOM levels, it is important to note that only the items directly above the item (in the BOM structure) causing the delay, will be updated with a delay as part of the master planning run.</span></span> <span data-ttu-id="8ce5b-123">أما الأصناف الأخرى في بنية قائمة مكونات الصنف فلن يتم تطبيق التأخير عليها حتى تشغيل التخطيط الرئيسي الأول، عند اعتماد الأمر المخطط للمستوى العلوي أو تأكيده.</span><span class="sxs-lookup"><span data-stu-id="8ce5b-123">Other items in the BOM structure will not get the delay applied until the first master planning run, when the planned order for the top level is approved or firmed.</span></span> 

<span data-ttu-id="8ce5b-124">لحل هذه القيود المعروفة، يمكن اعتماد أوامر الإنتاج الموجودة في أعلى بنية قائمة مكونات الصنف والتي فيها حالات تأخير (أو تأكيدها) قبل تشغيل التخطيط الرئيسي التالي.</span><span class="sxs-lookup"><span data-stu-id="8ce5b-124">To work around this known limitation, the production orders on the top of the BOM structure with delays can be approved (or firmed) prior to the next master planning run.</span></span> <span data-ttu-id="8ce5b-125">وبهذه الطريقة، سيتم الاحتفاظ بالتأخير من أمر الإنتاج المخطط المعتمد، وسيتم تحديث كافة المكونات الأساسية وفقًا لذلك.</span><span class="sxs-lookup"><span data-stu-id="8ce5b-125">This way the delay from the delayed approved planned production order will be kept and all underlying components will be updated accordingly.</span></span>
<span data-ttu-id="8ce5b-126">كما يمكن استخدام رسائل الاجراءات سيتم الأوامر المخططة التي يمكن نقلها إلى تاريخ لاحق بسبب حالات التأخير في بنية قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="8ce5b-126">Action messages can also be used to identify planned orders that can be moved to a later date, due to other delays in the BOM structure.</span></span>

## <a name="desired-date"></a><span data-ttu-id="8ce5b-127">التاريخ المطلوب</span><span class="sxs-lookup"><span data-stu-id="8ce5b-127">Desired date</span></span>

<span data-ttu-id="8ce5b-128">في صفحة **الأمر المخطط**، ضمن علامة التبويب **تأخيرات** يوجد **التاريخ المطلوب‬** للأمر المخطط.</span><span class="sxs-lookup"><span data-stu-id="8ce5b-128">On the **Planned order** page, under the **Delays** tab is the **Desired date** for the planned order.</span></span> <span data-ttu-id="8ce5b-129">يعتبر التاريخ المطلوب للأمر المخطط التاريخ الأساسي للتأخيرات، وهو تاريخ محسوب يساوي **التاريخ المطلوب** المحسوب من **صافي المتطلبات**.</span><span class="sxs-lookup"><span data-stu-id="8ce5b-129">The desired date of a planned order is the base date for delays, which is a computed date that equals the **Requested date** calculated from the **Net Requirement**.</span></span> <span data-ttu-id="8ce5b-130">إذا كان الأمر المخطط عبارة عن بند في قائمة مكونات الصنف أو بند إنتاج أو بند كانبان، فإن التاريخ المطلوب يستند إلى **تاريخ الطلب** ولن يظهر التاريخ المطلوب في صفحة **الأمر المخطط**.</span><span class="sxs-lookup"><span data-stu-id="8ce5b-130">If the planned order is a BOM line, production line or kanban line, the desired date is based on the **Requirement date** and the desired date will not be shown on the **Planned order** page.</span></span>

<a name="additional-resources"></a><span data-ttu-id="8ce5b-131">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="8ce5b-131">Additional resources</span></span>
--------

[<span data-ttu-id="8ce5b-132">إعدادات التغطية</span><span class="sxs-lookup"><span data-stu-id="8ce5b-132">Coverage settings</span></span>](coverage-settings.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]