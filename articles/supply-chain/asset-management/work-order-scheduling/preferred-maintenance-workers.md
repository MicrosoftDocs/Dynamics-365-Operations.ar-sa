---
title: إعداد عمال الصيانة المفضلين
description: يشرح هذا الموضوع كيفية إعداد عاملي الصيانة المفضلين في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkerPreferred
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c0637609a34890360a3b81355a8d21ef1b9faf8c
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888919"
---
# <a name="set-up-preferred-maintenance-workers"></a><span data-ttu-id="61501-103">إعداد عمال الصيانة المفضلين</span><span class="sxs-lookup"><span data-stu-id="61501-103">Set up preferred maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="61501-104">أثناء جدولة أوامر العمل، يمكنك تعيين تفضيل تتعلق بعامل الصيانة أو مجموعة العاملين التي يتم تعيينها لإكمال أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="61501-104">During work order scheduling, you can make a preference regarding which maintenance worker or worker group is allocated to complete the work order.</span></span> <span data-ttu-id="61501-105">يعتبر استخدام هذه الوظيفة أمرًا اختياريًا، ولكن من شأنها أن تساعدك على اختيار عامل الصيانة الذي يتمتع بالمعاملات اللازمة لإكمال مهمة ما، استنادًا إلى مهارات العامل واختصاصاته.</span><span class="sxs-lookup"><span data-stu-id="61501-105">The use of this functionality is optional, but it can help you make a choice for the most qualified maintenance worker to complete a job, based on worker skills and competencies.</span></span> <span data-ttu-id="61501-106">ستتم جدولة فقط عاملي الصيانة المتاحين في وقت الجدولة.</span><span class="sxs-lookup"><span data-stu-id="61501-106">Only maintenance workers that are available at scheduling time will be scheduled.</span></span> <span data-ttu-id="61501-107">إذا كان إعداد عامل صيانة مفضل يتطابق مع أحد أوامر العمل أثناء الجدولة، ولكن عامل الصيانة تم تعيينه لتنفيذ مهام أخرى، فستتم جدولة أمر العمل لعامل صيانة آخر يكون متاحًا.</span><span class="sxs-lookup"><span data-stu-id="61501-107">If a preferred maintenance worker setup matches a work order during scheduling, but the maintenance worker is allocated to other jobs, the work order will be scheduled to another available maintenance worker.</span></span>

<span data-ttu-id="61501-108">قبل أن تتمكن من إعداد عمال الصيانة المفضلين، فإنه يجب عليك أولاً إعداد عمال الصيانة ومجموعات العاملين.</span><span class="sxs-lookup"><span data-stu-id="61501-108">Before you can set up preferred maintenance workers, you must first set up the maintenance workers and worker groups.</span></span> <span data-ttu-id="61501-109">للحصول على معلومات حول كيفية إعداد عاملي الصيانة ومجموعات العاملين، راجع [‏‫عاملو ومجموعات عاملي الصيانة](../setup-for-objects/workers-and-worker-groups.md).</span><span class="sxs-lookup"><span data-stu-id="61501-109">For a description about how to set up maintenance workers and worker groups, see to [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

## <a name="set-up-preferred-workers"></a><span data-ttu-id="61501-110">إعداد العاملين المفضلين</span><span class="sxs-lookup"><span data-stu-id="61501-110">Set up preferred workers</span></span>

<span data-ttu-id="61501-111">بإمكان عامل صيانة مفضل أو مجموعة عاملي صيانة مفضلين بعنصر أو أكثر من العناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="61501-111">A preferred maintenance worker or worker group can be related to one or more of the following:</span></span>

- <span data-ttu-id="61501-112">المعاملات</span><span class="sxs-lookup"><span data-stu-id="61501-112">trade</span></span>  
- <span data-ttu-id="61501-113">متغير نوع مهمة الصيانة</span><span class="sxs-lookup"><span data-stu-id="61501-113">maintenance job type variant</span></span>  
- <span data-ttu-id="61501-114">نوع مهمة الصيانة</span><span class="sxs-lookup"><span data-stu-id="61501-114">maintenance job type</span></span>  
- <span data-ttu-id="61501-115">فئة نوع مهمة الصيانة</span><span class="sxs-lookup"><span data-stu-id="61501-115">maintenance job type category</span></span>  
- <span data-ttu-id="61501-116">أصل</span><span class="sxs-lookup"><span data-stu-id="61501-116">asset</span></span>  
- <span data-ttu-id="61501-117">نوع الأصل</span><span class="sxs-lookup"><span data-stu-id="61501-117">asset type</span></span>  

<span data-ttu-id="61501-118">كلما زاد عدد التحديدات التي تجريها لنفس السجل، يكون إعدادك أكثر تحديدًا.</span><span class="sxs-lookup"><span data-stu-id="61501-118">The more selections you make for the same record, the more specific your setup will be.</span></span>

1. <span data-ttu-id="61501-119">انقر فوق **إدارة الأصول‏‎** > **الإعداد** > **العاملون** > **‏‫عمال الصيانة المفضلون‬**.</span><span class="sxs-lookup"><span data-stu-id="61501-119">Click **Asset management** > **Setup** > **Workers** > **Preferred maintenance workers**.</span></span>

2. <span data-ttu-id="61501-120">انقر فوق **جديد** لإنشاء سجل جديد.</span><span class="sxs-lookup"><span data-stu-id="61501-120">Click **New** to create a new record.</span></span>

3. <span data-ttu-id="61501-121">ابدأ بإنشاء عامل صيانة "افتراضي" أو مجموعة عاملين "افتراضية".</span><span class="sxs-lookup"><span data-stu-id="61501-121">Start by creating a "default" maintenance worker or worker group.</span></span> <span data-ttu-id="61501-122">وهذا يعني انك تجري تحديدًا فقط في الحقل **مجموعة عاملي الصيانة المفضلين** أو الحقل **عامل الصيانة المفضل**.</span><span class="sxs-lookup"><span data-stu-id="61501-122">This means that you only make a selection in the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field.</span></span> <span data-ttu-id="61501-123">في لقطة الشاشة أدناه، يمكنك رؤية مثال في السجل الأول الذي تم فيه تحديد "طلبات" **مجموعة عاملي الصيانة المفضلين**.</span><span class="sxs-lookup"><span data-stu-id="61501-123">In the screenshot below, you see an example in the first record in which "Requests" is selected as **Preferred maintenance worker group**.</span></span>

    [!NOTE] <span data-ttu-id="61501-124">سيتم استخدام الإعداد الافتراضي أثناء جدولة أمر العمل إذا لم تطابق تركيبة أخرى أكثر تحديداً محتويات أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="61501-124">The default setup will be used during work order scheduling if no other, more specific, combination matches the contents of the work order.</span></span>

4. <span data-ttu-id="61501-125">كرر الخطوة 2 لإنشاء سجل جديد.</span><span class="sxs-lookup"><span data-stu-id="61501-125">Repeat step 2 to create a new record.</span></span> <span data-ttu-id="61501-126">قم بإجراء التحديدات المطلوبة، استنادًا إلى مستوى التفاصيل للعامل المفضل أو مجموعة العاملين المفضلة.</span><span class="sxs-lookup"><span data-stu-id="61501-126">Make the required selections, depending on the detail level for the preferred worker or worker group.</span></span> 

    <span data-ttu-id="61501-127">*مثال:* في لقطة الشاشة الموجودة أدناه، في السجل السادس، تم تحديد عامل الصيانة شون ريتشاردسون كعامل مفضل.</span><span class="sxs-lookup"><span data-stu-id="61501-127">*Example:* In the screenshot below, in the sixth record, the maintenance worker Shawn Richardson is selected as preferred worker.</span></span> <span data-ttu-id="61501-128">سيتم تحديده بشكل تلقائي أثناء جدولة أمر العمل الذي يتضمن الأصل "BP1-03-02" ونوع مهمة الصيانة "تقييم المنشأة"، إذا كان متاحًا في الوقت المجدول.</span><span class="sxs-lookup"><span data-stu-id="61501-128">He will automatically be selected during scheduling of a work order that includes the asset "CH-BP1-03-02 and the maintenance job type "Facility assessment", if he is available at the scheduled time.</span></span>

    [!NOTE] <span data-ttu-id="61501-129">بشكل عام، عند تحديد عامل صيانة مفضل أثناء جدولة أمر العمل، تستعرض إدارة الصيانة جميع سجلات **عمال الصيانة المفضلون‬** للتحقق من وجود تطابق محتمل، مع التحقق أولاً ودائمًا من التركيبة الأكثر تحديدًا.</span><span class="sxs-lookup"><span data-stu-id="61501-129">Generally, when a preferred maintenance worker is selected during work order scheduling, Asset Management goes through all **Preferred maintenance workers** records to check for a possible match, always checking the most specific combination first.</span></span> <span data-ttu-id="61501-130">وإذا لم يتم العثور على أي تطابق، يُستخدم السجل "الافتراضي" الذي يتضمن تحديدًا إما في الحقل **مجموعة عاملي الصيانة المفضلين** أو الحقل **عامل‏‎ الصيانة المفضل**.</span><span class="sxs-lookup"><span data-stu-id="61501-130">If no match is found, the "default" record with a selection in either the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field is used.</span></span>

![الشكل 1](media/02-work-order-scheduling.png)

<span data-ttu-id="61501-132">يمكنك أيضًا إعداد عاملي الصيانة *المسؤولين* الذين يمكن تحديدهم عند إنشاء طلب صيانة أو أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="61501-132">You can also set up *responsible* maintenance workers who can be selected when a maintenance request or a work order is created.</span></span> <span data-ttu-id="61501-133">يمكنك تحرير التحديد في **جميع أوامر العمل** و**وجميع طلبات الصيانة**، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="61501-133">You can edit the selection in **All work orders** and **All maintenance requests**, if required.</span></span> <span data-ttu-id="61501-134">لمزيد من المعلومات، ارجع إلى [عاملو الصيانة المسؤولون‬](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="61501-134">For more information, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>

<span data-ttu-id="61501-135">أثناء جدولة أمر عمل، يتم حساب نقاط مختلفة لتحديد العاملين الذين يجب عليهم إكمال وظائف ذات صلة بأمر عمل (يتم إعداد هذه النقاط في **محددات إدارة الأصول‬** > الارتباط **جدولة أمر العمل‬**).</span><span class="sxs-lookup"><span data-stu-id="61501-135">During work order scheduling, different scores are calculated to determine which workers should complete the jobs related to a work order (those scores are set up in **Asset management parameters** > **Work order scheduling** link).</span></span> <span data-ttu-id="61501-136">في حال حصول عاملي صيانة مفضلين أو أكثر أو عاملي صيانة مسؤولين أو أكثر على النقاط نفسها أثناء جدولة أمر العمل، فسيتم اختيار عامل واحد بشكل عشوائي.</span><span class="sxs-lookup"><span data-stu-id="61501-136">If two or more preferred maintenance workers or responsible maintenance workers get the same score during work order scheduling, one worker is randomly selected.</span></span> <span data-ttu-id="61501-137">والا، فسيتم دائمًا تعيين العامل الذي يحظى بأعلى مجموع نقاط لإكمال أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="61501-137">Otherwise, it is always the worker with the highest score who is allocated to complete a work order.</span></span>

