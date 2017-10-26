---
title: "إدارة عمال المستودعات"
description: "توضح هذه المقالة الطريقة التي يمكنك من خلالها استخدام Dynamics 365 for Finance and Operations للمساعدة في مراقبة ورصد العمل الذي يقوم به الموظفون في مستودعاتك."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmWorker, InventLocation, WHSLaborStandards, WHSWorker, WHSWorkTable, WHSWorkTableListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72891
ms.assetid: feaa6f15-49d2-41f5-9b87-453463c52e4e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0b91c139987473be65fddf8b05759a5ad6f6c223
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="manage-warehouse-workers"></a><span data-ttu-id="ff8d1-103">إدارة عمال المستودعات</span><span class="sxs-lookup"><span data-stu-id="ff8d1-103">Manage warehouse workers</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ff8d1-104">توضح هذه المقالة الطريقة التي يمكنك من خلالها استخدام Dynamics 365 for Finance and Operations, Enterprise edition للمساعدة في مراقبة ورصد العمل الذي يقوم به الموظفون في مستودعاتك.</span><span class="sxs-lookup"><span data-stu-id="ff8d1-104">This article describes how you can use Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to help control and monitor the work that's carried out by employees in your warehouses.</span></span>

<span data-ttu-id="ff8d1-105">إذا كنت تستخدم الوظيفة في إدارة المستودعات، فإنه تتم الإشارة إلى جميع عمليات عمال المستودع كـ *عمل*.</span><span class="sxs-lookup"><span data-stu-id="ff8d1-105">If you're using the functionality in Warehouse management, all warehouse worker operations are referred to as *work*.</span></span> <span data-ttu-id="ff8d1-106">ويتم تسجيل العمل، مثل الانتقاء والنقل وجرد المخزون الفعلي باستخدام الأجهزة المحمولة.</span><span class="sxs-lookup"><span data-stu-id="ff8d1-106">Work such as picking, moving, and counting on-hand inventory is recorded by using mobile devices.</span></span> <span data-ttu-id="ff8d1-107">وقبل أن يمكن لعامل مستودع تنفيذ العمل، يجب إقرانه أو إقرانها بعامل في الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="ff8d1-107">Before a warehouse worker can perform work, he or she must be associated with a worker in Human resources.</span></span> <span data-ttu-id="ff8d1-108">ويمكن أن يشتمل كل حساب **عامل** على عدة مستخدمين لعمل المستودع مقترنين به.</span><span class="sxs-lookup"><span data-stu-id="ff8d1-108">Each **Worker** account can have multiple warehouse work users associated with it.</span></span> <span data-ttu-id="ff8d1-109">ويمكن لمستخدمي العمل أولئك العمل في مستودعات مختلفة ويمكنهم الحصول على مستويات مختلفة من الوصول إلى مختلف قوائم الأجهزة المحمولة.</span><span class="sxs-lookup"><span data-stu-id="ff8d1-109">Those work users can work in different warehouses and can have different levels of access to the various mobile device menus.</span></span> <span data-ttu-id="ff8d1-110">ويمكنك اعتبار مستخدمي عمل المستودع كعمليات تسجيل دخول متعددة للعامل المحدد.</span><span class="sxs-lookup"><span data-stu-id="ff8d1-110">You can think of the warehouse work users as multiple logons for the selected worker.</span></span> <span data-ttu-id="ff8d1-111">ويمتلك كل مستخدم عمل مستودعًا افتراضيًا، ويتم عرض مهام سير عمل معينة بواسطة عناصر القوائم المتوفرة لمستخدم العمل هذا.</span><span class="sxs-lookup"><span data-stu-id="ff8d1-111">Each work user has a default warehouse, and specific workflows are exposed by the menus items that are available to that work user.</span></span> 

<span data-ttu-id="ff8d1-112">ولإنشاء مستخدم عمل جديد، في صفحة **العاملين**، في علامة التبويب **عام** في قسم **المستودعات**، انقر فوق **العامل**.</span><span class="sxs-lookup"><span data-stu-id="ff8d1-112">To create a new work user, on the **Workers** page, on the **General** tab, in the **Warehouses** section, click **Worker**.</span></span> <span data-ttu-id="ff8d1-113">ويجب عليك تحديد معرف مستخدم، واسم مستخدم، ومستودع افتراضي، واسم قائمة.</span><span class="sxs-lookup"><span data-stu-id="ff8d1-113">You must specify a user ID, a user name, a default warehouse, and a menu name.</span></span> <span data-ttu-id="ff8d1-114">ويتم تحميل هذه القائمة عندما يقوم المستخدم بتسجيل الدخول إلى "مدخل الأجهزة المحمولة في المستودع"، وتتيح لك تحديد عناصر القائمة التي يمتلك المستخدم حق الوصول إليها.</span><span class="sxs-lookup"><span data-stu-id="ff8d1-114">This menu is loaded when the user signs in to the Warehouse Mobile Device Portal, and lets you define which menu items the user has access to.</span></span> 

<span data-ttu-id="ff8d1-115">وكجزء من الإعداد لكل مستخدم عمل، يمكنك أيضًا تحديد مهام سير عمل معينة.</span><span class="sxs-lookup"><span data-stu-id="ff8d1-115">As part of the setup for each work user, you can also define specific process workflows.</span></span> <span data-ttu-id="ff8d1-116">على سبيل المثال، يمكنك استخدام حقل **عبارة عن مشرف على الجرد الدوري‬** لتحديد ما إذا كان المستخدم يمكنه معالجة تعديلات اختلافات دورة الجرد أثناء عملية جرد، أو ما إذا كانت هذه التعديلات يجب أولاً مراجعتها بواسطة شخص آخر.</span><span class="sxs-lookup"><span data-stu-id="ff8d1-116">For example, you can use the **Is a cycle count supervisor** field to specify whether the user can process adjustments to cycle counting discrepancies during a counting operation, or whether these adjustments must first be reviewed by another person.</span></span>

## <a name="defining-labor-standards"></a><span data-ttu-id="ff8d1-117">تحديد معايير العمل</span><span class="sxs-lookup"><span data-stu-id="ff8d1-117">Defining labor standards</span></span>
<span data-ttu-id="ff8d1-118">تتيح لك صفحة **معايير العمل** تحديد طرق الحساب التي يستخدمها النظام لحساب الوقت المقدر الذي ينبغي أن يتطلبه نوع معين من العمل.</span><span class="sxs-lookup"><span data-stu-id="ff8d1-118">The **Labor standards** page lets you define the calculation methods that the system uses to calculate the estimated time that a particular type of work should require.</span></span> <span data-ttu-id="ff8d1-119">ويمكن تعيين هذا التعريف على مستوى عام أو على مستوى معين.</span><span class="sxs-lookup"><span data-stu-id="ff8d1-119">This definition can be set on a generic level or on a specific level.</span></span> <span data-ttu-id="ff8d1-120">على سبيل المثال، يمكنك تحديد الوقت الذي يجب أن يكون مطلوبًا من أجل معالجة انتقاء أمر مبيعات لكل وزن لتعريف وحدة محددة عند استخدام عملية انتقاء محددة.</span><span class="sxs-lookup"><span data-stu-id="ff8d1-120">For example, you can define the time that should be required in order to process a sales order pick per weight for a specific unit definition when a specific picking process is used.</span></span> <span data-ttu-id="ff8d1-121">وفي نفس الوقت، يمكنك تسجيل الوقت، استناداً إلى طريقة حساب أخرى لعملية وضع قائمة الجرد الفعلي التي يتم انتقاؤها.</span><span class="sxs-lookup"><span data-stu-id="ff8d1-121">At the same time, you can record the time, based on another calculation method, for the put operation of the on-hand inventory that is picked.</span></span> 

<span data-ttu-id="ff8d1-122">ولتمكين معايير العمل التي قمت بتحديدها، يجب عليك تحديد خيار **السماح بمعايير العمل** لكل مستودع يتم فيه استخدام معايير العمل.</span><span class="sxs-lookup"><span data-stu-id="ff8d1-122">To enable the labor standards that you've defined, you must select the **Allow labor standards** option for each warehouse where labor standards will be used.</span></span>

## <a name="monitoring-and-controlling-warehouse-work"></a><span data-ttu-id="ff8d1-123">رصد ومراقبة العمل في المستودع</span><span class="sxs-lookup"><span data-stu-id="ff8d1-123">Monitoring and controlling warehouse work</span></span>
<span data-ttu-id="ff8d1-124">تتيح لك صفحة **كافة الأعمال** مراقبة والاحتفاظ بكافة الأعمال المخططة، وقيد التقدم، والمكتملة.</span><span class="sxs-lookup"><span data-stu-id="ff8d1-124">The **All work** page lets you monitor and maintain all work that is planned, in progress, and completed.</span></span> <span data-ttu-id="ff8d1-125">ومن هذه الصفحة، يمكنك تحديث العمليات المختلفة، مثل تعيينات مستخدم عمل المستودع وأولوية العمل.</span><span class="sxs-lookup"><span data-stu-id="ff8d1-125">From this page, you can update various processes, such as warehouse work user assignments and work priority.</span></span> <span data-ttu-id="ff8d1-126">كما يمكنك التنقل في التفاصيل المتعلقة ببنود العمل ورأس العمل لفهم عمليات العمل المتوقعة أو المكتملة.</span><span class="sxs-lookup"><span data-stu-id="ff8d1-126">You can also drill down into the details that are related to the work header and work lines to gain an understanding of the expected or completed work processes.</span></span> 

<span data-ttu-id="ff8d1-127">وإذا قمت بتمكين خيار **معايير العمل**، يمكنك مشاهدة الوقت المقدر المحسوب للعمل.</span><span class="sxs-lookup"><span data-stu-id="ff8d1-127">If you enable the **Labor standards** option, you can see the calculated estimated time for the work.</span></span> <span data-ttu-id="ff8d1-128">وبعد ذلك، عند معالجة العمل، سيظهر الوقت الفعلي لكل عملية عمل أيضًا.</span><span class="sxs-lookup"><span data-stu-id="ff8d1-128">Then, when the work is processed, the actual time will also be shown for each work operation.</span></span> <span data-ttu-id="ff8d1-129">وبهذه الطريقة، يمكنك مقارنة عمليات حساب الوقت المقدر للوقت الفعلي.</span><span class="sxs-lookup"><span data-stu-id="ff8d1-129">In this way, you can compare the estimated time calculations to the actual time.</span></span> 

<span data-ttu-id="ff8d1-130">بالإضافة إلى ذلك، يمكنك استخدام الوقت المقدر في القواعد لتقسيم العمل تلقائياً أثناء إنشاء العمل.</span><span class="sxs-lookup"><span data-stu-id="ff8d1-130">Additionally, you can use the estimated time in the rules for automatically splitting work during work creation.</span></span> <span data-ttu-id="ff8d1-131">وبهذه الطريقة، يمكنك تحميل عمل الموازنة، استنادًا إلى الوقت المتوقع لإكمال المهام.</span><span class="sxs-lookup"><span data-stu-id="ff8d1-131">In this way, you can load balance work, based on the expected time to complete the tasks.</span></span> 

<span data-ttu-id="ff8d1-132">ويمكن أن يساعد تحليل الوقت المستخدم لمعالجة عناصر العمل على تشغيل التحسينات في الكفاءة الخاصة بعمال المستودع.</span><span class="sxs-lookup"><span data-stu-id="ff8d1-132">Analysis of the time that is used to process work items can help drive improvements in the warehouse workers’ efficiency.</span></span> <span data-ttu-id="ff8d1-133">تتوفر التقارير التالية للمساعدة في هذا التحليل:</span><span class="sxs-lookup"><span data-stu-id="ff8d1-133">The following reports are available to help with this analysis:</span></span>

-   <span data-ttu-id="ff8d1-134">**العمل حسب المستخدم** – يعرض هذا التقرير إنتاجية العامل، استناداً إلى الأوقاتت الفعلية مقابل الأوقات المتوقعة.</span><span class="sxs-lookup"><span data-stu-id="ff8d1-134">**Labor by user** – This report shows worker productivity, based on actual times against expected times.</span></span>
-   <span data-ttu-id="ff8d1-135">**‏‫العمل حسب نوع حركة العمل** – يمكنك استخدام هذا التقرير لتحري أوجه القصور في عمليات مستودع معين.</span><span class="sxs-lookup"><span data-stu-id="ff8d1-135">**Labor by work transaction type** – You can use this report to investigate inefficiencies in specific warehouse processes.</span></span> <span data-ttu-id="ff8d1-136">على سبيل المثال، لاحظت أن عمليات انتقاء أوامر التحويل تستغرق وقتاً أطول هذا الأسبوع  مقارنةً بالأسابيع السابقة.</span><span class="sxs-lookup"><span data-stu-id="ff8d1-136">For example, you notice that picks for transfer orders are taking longer this week than in previous weeks.</span></span> <span data-ttu-id="ff8d1-137">ويمكنك بعد ذلك استخدام هذه المعلومات لإجراء مزيد من التحقيقات.</span><span class="sxs-lookup"><span data-stu-id="ff8d1-137">You can then use this information for further investigation.</span></span>




