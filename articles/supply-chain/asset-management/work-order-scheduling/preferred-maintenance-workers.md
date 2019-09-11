---
title: إعداد عمال الصيانة المفضلين
description: يشرح هذا الموضوع كيفية إعداد عاملي الصيانة المفضلين في إدارة الأصول.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8f26be81e7057d0cea1473d81452216251633ad9
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887401"
---
# <a name="preferred-maintenance-workers"></a><span data-ttu-id="9943e-103">عمال الصيانة المفضلون</span><span class="sxs-lookup"><span data-stu-id="9943e-103">Preferred maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="9943e-104">يمكنك تعيين تفضيلات تتعلق بعاملي الصيانة الذين يتم تعيينهم لإكمال أوامر العمل أثناء جدولة أوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="9943e-104">You can make a preference regarding which maintenance workers are allocated to complete work orders during work order scheduling.</span></span> <span data-ttu-id="9943e-105">يعتبر استخدام هذه الوظيفة أمرًا اختياريًا، ولكن من شأنها أن تساعدك على اختيار عامل الصيانة الذي يتمتع بالمعاملات اللازمة لإكمال مهمة ما، استنادًا إلى مهارات العامل واختصاصاته.</span><span class="sxs-lookup"><span data-stu-id="9943e-105">The use of this functionality is optional, but it can help you make a choice for the most qualified maintenance worker to complete a job, based on worker skills and competencies.</span></span> <span data-ttu-id="9943e-106">وبالتالي، أثناء جدولة أمر العمل، يتم استخدام الإعداد **عمال الصيانة المفضلون** لتحديد ما إذا كان يجب جدولة عامل صيانة معين أو مجموعة معينة من عاملي الصيانة لتنفيذ أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="9943e-106">Therefore, during work order scheduling, the setup in **Preferred maintenance workers** is used to determine if a specific maintenance worker or worker group should be scheduled for a work order.</span></span> <span data-ttu-id="9943e-107">ستتم جدولة فقط عاملي الصيانة المتاحين في وقت الجدولة.</span><span class="sxs-lookup"><span data-stu-id="9943e-107">Only maintenance workers that are available at scheduling time will be scheduled.</span></span> <span data-ttu-id="9943e-108">إذا كان إعداد عامل صيانة مفضل يتطابق مع أحد أوامر العمل أثناء الجدولة، ولكن عامل الصيانة تم تعيينه لتنفيذ مهام أخرى، فستتم جدولة أمر العمل لعامل صيانة آخر يكون متاحًا.</span><span class="sxs-lookup"><span data-stu-id="9943e-108">If a preferred maintenance worker setup matches a work order during scheduling, but the maintenance worker is allocated to other jobs, the work order will be scheduled to another, available, maintenance worker.</span></span>

<span data-ttu-id="9943e-109">قبل أن تتمكن من إعداد عاملي الصيانة المفضلين، يجب أولاً إعداد عاملي الصيانة ومجموعات عاملي الصيانة التي يجب أن تكون متاحة للاختيار.</span><span class="sxs-lookup"><span data-stu-id="9943e-109">Before you can set up preferred maintenance workers, you must first set up the maintenance workers and worker groups that should be available for selection.</span></span> <span data-ttu-id="9943e-110">يمكنك مراجعة [عاملو الصيانة ومجموعات عاملي الصيانة‬](../setup-for-objects/workers-and-worker-groups.md) للحصول على معلومات حول كيفيه إعداد عاملي الصيانة ومجموعات عاملي الصيانة.</span><span class="sxs-lookup"><span data-stu-id="9943e-110">Refer to [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md) for a description on how to set up maintenance workers and worker groups.</span></span>

## <a name="set-up-preferred-workers"></a><span data-ttu-id="9943e-111">إعداد العاملين المفضلين</span><span class="sxs-lookup"><span data-stu-id="9943e-111">Set up preferred workers</span></span>

<span data-ttu-id="9943e-112">بإمكان عامل صيانة مفضل أو مجموعة عاملي صيانة مفضلين الارتباط بعنصر معين من العناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="9943e-112">A preferred maintenance worker or worker group can be related to a specific</span></span>

- <span data-ttu-id="9943e-113">المعاملات</span><span class="sxs-lookup"><span data-stu-id="9943e-113">trade</span></span>  
- <span data-ttu-id="9943e-114">متغير نوع مهمة الصيانة</span><span class="sxs-lookup"><span data-stu-id="9943e-114">maintenance job type variant</span></span>  
- <span data-ttu-id="9943e-115">نوع مهمة الصيانة</span><span class="sxs-lookup"><span data-stu-id="9943e-115">maintenance job type</span></span>  
- <span data-ttu-id="9943e-116">فئة نوع مهمة الصيانة</span><span class="sxs-lookup"><span data-stu-id="9943e-116">maintenance job type category</span></span>  
- <span data-ttu-id="9943e-117">أصل</span><span class="sxs-lookup"><span data-stu-id="9943e-117">asset</span></span>  
- <span data-ttu-id="9943e-118">نوع الأصل</span><span class="sxs-lookup"><span data-stu-id="9943e-118">asset type</span></span>  

<span data-ttu-id="9943e-119">أو تركيبة من هذه التحديدات.</span><span class="sxs-lookup"><span data-stu-id="9943e-119">or a combination of those selections.</span></span> <span data-ttu-id="9943e-120">كلما زاد عدد التحديدات التي تجريها لنفس السجل، يكون إعدادك أكثر تحديدًا.</span><span class="sxs-lookup"><span data-stu-id="9943e-120">The more selections you make for the same record, the more specific your setup will be.</span></span>

1. <span data-ttu-id="9943e-121">انقر فوق **إدارة الأصول‏‎** > **الإعداد** > **العاملون** > **‏‫عمال الصيانة المفضلون‬**.</span><span class="sxs-lookup"><span data-stu-id="9943e-121">Click **Asset management** > **Setup** > **Workers** > **Preferred maintenance workers**.</span></span>

2. <span data-ttu-id="9943e-122">انقر فوق **جديد** لإنشاء سجل جديد.</span><span class="sxs-lookup"><span data-stu-id="9943e-122">Click **New** to create a new record.</span></span>

3. <span data-ttu-id="9943e-123">ابدأ بإنشاء إعداد "افتراضي" لعامل صيانة أو مجموعة من عاملي الصيانة لا يتضمن أي تحديدات في الحقول التي تظهر في القائمة النقطية أعلاه.</span><span class="sxs-lookup"><span data-stu-id="9943e-123">Start by creating a "default" maintenance worker or worker group setup that has no selections in the fields shown in the bullet list above.</span></span> <span data-ttu-id="9943e-124">وهذا يعني انك تجري تحديدًا فقط في الحقل **مجموعة عاملي الصيانة المفضلين** أو الحقل **عامل الصيانة المفضل**.</span><span class="sxs-lookup"><span data-stu-id="9943e-124">This means that you only make a selection in the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field.</span></span> <span data-ttu-id="9943e-125">في الشكل أدناه، يمكنك رؤية مثال في السجل الأول الذي تم فيه تحديد "طلبات" كمجموعة من عاملي الصيانة المفضلين.</span><span class="sxs-lookup"><span data-stu-id="9943e-125">In the figure below, you see an example in the first record in which "Requests" is selected as preferred maintenance worker group.</span></span>

>[!NOTE]
><span data-ttu-id="9943e-126">سيتم استخدام الإعداد الافتراضي أثناء جدولة أمر العمل إذا لم تطابق تركيبة أخرى أكثر تحديدًا محتويات أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="9943e-126">The default setup will be used during work order scheduling in case no other, more specific, combination matches the contents of the work order during work order scheduling.</span></span>

4. <span data-ttu-id="9943e-127">كرر الخطوة 2 لإنشاء سجل جديد.</span><span class="sxs-lookup"><span data-stu-id="9943e-127">Repeat step 2 to create a new record.</span></span> <span data-ttu-id="9943e-128">قم بإجراء التحديدات المطلوبة، استنادًا إلى مستوى التفاصيل للعامل المفضل أو مجموعة العاملين المفضلة.</span><span class="sxs-lookup"><span data-stu-id="9943e-128">Make the required selections, depending on the detail level for the preferred worker or worker group.</span></span> <span data-ttu-id="9943e-129">*مثال:* في الشكل الموجود أدناه، في السجل السادس، تم تحديد عامل الصيانة شون ريتشاردسون كعامل مفضل.</span><span class="sxs-lookup"><span data-stu-id="9943e-129">*Example:* In the figure below, in the sixth record, the maintenance worker Shawn Richardson is selected as preferred worker.</span></span> <span data-ttu-id="9943e-130">سيتم تحديده بشكل تلقائي أثناء جدولة أمر العمل الذي يتضمن الأصل "BP1-03-02" ونوع مهمة الصيانة "تقييم المنشأة"، إذا كان متاحًا في الوقت المجدول.</span><span class="sxs-lookup"><span data-stu-id="9943e-130">He will automatically be selected during scheduling of a work order that includes the asset "CH-BP1-03-02 and the maintennace job type "Facility assessment", if he is available at the scheduled time.</span></span>

>[!NOTE]
><span data-ttu-id="9943e-131">بشكل عام، عند تحديد عامل صيانة مفضل أثناء جدولة أمر العمل، تستعرض إدارة الصيانة جميع سجلات **عمال الصيانة المفضلون‬** للتحقق من وجود تطابق محتمل، مع التحقق أولاً ودائمًا من التركيبة الأكثر تحديدًا.</span><span class="sxs-lookup"><span data-stu-id="9943e-131">Generally, when a preferred maintenance worker is selected during work order scheduling, Asset Management goes through all **Preferred maintenance workers** records to check for a possible match, always checking the most specific combination first.</span></span> <span data-ttu-id="9943e-132">وإذا لم يتم العثور على أي تطابق، يُستخدم السجل "الافتراضي" الذي يتضمن تحديدًا إما في الحقل **مجموعة عاملي الصيانة المفضلين** أو الحقل **عامل‏‎ الصيانة المفضل**.</span><span class="sxs-lookup"><span data-stu-id="9943e-132">If no match is found, the "default" record with a selection in either the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field is used.</span></span>


![الشكل 1](media/02-work-order-scheduling.png)

<span data-ttu-id="9943e-134">يمكنك أيضًا إعداد عاملي الصيانة المسؤولين الذين يمكن تحديدهم عند إنشاء طلب صيانة أو أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="9943e-134">You can also set up responsible maintenance workers who can be selected when a maintenance request or a work order is created.</span></span> <span data-ttu-id="9943e-135">في **جميع أوامر العمل** و**وجميع طلبات الصيانة**، يمكنك تحرير التحديد، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="9943e-135">In **All work orders** and **All maintenance requests**, you can edit the selection, if required.</span></span> <span data-ttu-id="9943e-136">لمزيد من المعلومات، يمكنك مراجعة [عاملو الصيانة المسؤولون‬](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="9943e-136">Refer to [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md) for more information.</span></span>

<span data-ttu-id="9943e-137">أثناء جدولة أمر عمل، يتم حساب نقاط مختلفة لتحديد العاملين الذين يجب عليهم إكمال وظائف ذات صلة بأمر عمل (يتم إعداد هذه النقاط في **محددات إدارة الأصول‬** > الارتباط **جدولة أمر العمل‬**).</span><span class="sxs-lookup"><span data-stu-id="9943e-137">During work order scheduling, different scores are calculated to determine which workers should complete the jobs related to a work order (those scores are set up in **Asset management parameters** > **Work order scheduling** link).</span></span> <span data-ttu-id="9943e-138">في حال حصول عاملي صيانة مفضلين أو أكثر أو عاملي صيانة مسؤولين أو أكثر على النقاط نفسها أثناء جدولة أمر العمل، فسيتم اختيار عامل واحد بشكل عشوائي.</span><span class="sxs-lookup"><span data-stu-id="9943e-138">If two or more preferred maintenance workers or responsible maintenance workers get the same score during work order scheduling, one worker is randomly selected.</span></span> <span data-ttu-id="9943e-139">والا، فسيتم دائمًا تعيين العامل الذي يحظى بأعلى مجموع نقاط لإكمال أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="9943e-139">Otherwise, it is always the worker with the highest score who is allocated to complete a work order.</span></span>

