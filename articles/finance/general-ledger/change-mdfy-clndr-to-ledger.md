---
title: تغيير تقويم دفتر الأستاذ أو إعادة تعيينه
description: يشرح هذا الموضوع كيفية تغيير التقويم المعين حاليًا لدفتر الأستاذ، وكيفية تعيين تقويم جديد لدفتر الأستاذ.
author: kweekley
ms.date: 05/07/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-07
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 052b8944c0a015187d1d7c4ba3db878c52faeeea
ms.sourcegitcommit: 905a8c7a0c1bc06ada2acfba913dfe5f7b44ea16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/14/2021
ms.locfileid: "6039940"
---
# <a name="change-or-reassign-a-ledger-calendar"></a><span data-ttu-id="37e6e-103">تغيير تقويم دفتر الأستاذ أو إعادة تعيينه</span><span class="sxs-lookup"><span data-stu-id="37e6e-103">Change or reassign a ledger calendar</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37e6e-104">يشرح هذا الموضوع كيفية تغيير التقويم المعين حاليًا لدفتر الأستاذ، وكيفية تعيين تقويم جديد لدفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="37e6e-104">This topic explains how to change the calendar that is currently assigned to a ledger, and how to assign a new calendar to the ledger.</span></span>

## <a name="issue"></a><span data-ttu-id="37e6e-105">المشكلة</span><span class="sxs-lookup"><span data-stu-id="37e6e-105">Issue</span></span>

<span data-ttu-id="37e6e-106">في وقت ما، يجب على الشركات إما تغيير التقويم الحالي المخصص لدفتر الأستاذ أو تعيين تقويم جديد.</span><span class="sxs-lookup"><span data-stu-id="37e6e-106">Sometime, companies must either change the existing calendar that is assigned to a ledger or assign a new calendar.</span></span>

## <a name="resolution"></a><span data-ttu-id="37e6e-107">الحل</span><span class="sxs-lookup"><span data-stu-id="37e6e-107">Resolution</span></span>

<span data-ttu-id="37e6e-108">هناك سيناريوهان لتغيير تقويم دفتر الأستاذ أو إعادة تعيينه.</span><span class="sxs-lookup"><span data-stu-id="37e6e-108">There are two scenarios for changing or reassigning a ledger calendar.</span></span> <span data-ttu-id="37e6e-109">يتضمن السيناريو الأول تغيير تقويم موجود تم تعيينه بالفعل لدفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="37e6e-109">The first scenario involves changing an existing calendar that is already assigned to the ledger.</span></span> <span data-ttu-id="37e6e-110">يتضمن السيناريو الثاني إنشاء تقويم جديد وتعيينه لدفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="37e6e-110">The second scenario involves creating a new calendar and assigning it to the ledger.</span></span> <span data-ttu-id="37e6e-111">يمكن إجراء كلا التغييرين في أي وقت، حتى بعد ترحيل الحركات إلى دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="37e6e-111">Both changes can be done at any time, even after transactions have been posted to the ledger.</span></span>

### <a name="change-an-existing-fiscal-calendar"></a><span data-ttu-id="37e6e-112">تغيير تقويم مالي موجود</span><span class="sxs-lookup"><span data-stu-id="37e6e-112">Change an existing fiscal calendar</span></span>

<span data-ttu-id="37e6e-113">لتغيير تقويم موجود تم تعيينه لدفتر الأستاذ الخاص بك، انتقل إلى **دفتر الأستاذ العام \> إعداد دفتر الأستاذ \> دفتر الأستاذ**، وحدد ارتباط التقويم المالي لفتح صفحة **تقاويم دفتر الأستاذ**.</span><span class="sxs-lookup"><span data-stu-id="37e6e-113">To change an existing calendar that is assigned to your ledger, go to **General ledger \> Ledger setup \> Ledger**, and select the link for the fiscal calendar to open the **Ledger calendars** page.</span></span>

<span data-ttu-id="37e6e-114">هناك حدود للتغييرات التي يمكن إجراؤها على التقويم.</span><span class="sxs-lookup"><span data-stu-id="37e6e-114">There are limits to the changes that can be made to a calendar.</span></span> <span data-ttu-id="37e6e-115">على سبيل المثال، يمكنك تغيير تاريخي بدء وانتهاء *الفترات* في سنة، ولكن يمكنك تغيير تاريخ بدء وانتهاء *سنة* في التقويم.</span><span class="sxs-lookup"><span data-stu-id="37e6e-115">For example, you can change the start and end dates of the *periods* in a year, but you can't change the start and end dates of a *year* in the calendar.</span></span>

<span data-ttu-id="37e6e-116">لتغيير الفترات في سنة، حدد التقويم والسنة الملائمين.</span><span class="sxs-lookup"><span data-stu-id="37e6e-116">To change the periods in a year, select the appropriate calendar and year.</span></span> <span data-ttu-id="37e6e-117">أولاً، استخدم الزر **حذف فترة** لحذف بعض أو كل فترات التشغيل الحالية.</span><span class="sxs-lookup"><span data-stu-id="37e6e-117">First, use the use the **Delete period** button to delete some or all of the existing operating periods.</span></span> <span data-ttu-id="37e6e-118">يمكن حذف جميع فترات التشغيل باستثناء الفترة الأولى.</span><span class="sxs-lookup"><span data-stu-id="37e6e-118">All operating periods except the first can be deleted.</span></span> <span data-ttu-id="37e6e-119">استخدم بعد ذلك زر **تقسيم الفترة** لتقسيم الفترة أو الفترات المتبقية إلى فترات جديدة عن طريق إدخال تاريخ بدء مناسب للفترة التالية.</span><span class="sxs-lookup"><span data-stu-id="37e6e-119">Then use the **Divide period** button to divide the remaining period or periods into new periods by entering an appropriate start date for the next period.</span></span>

<span data-ttu-id="37e6e-120">بعد تغيير الفترات في التقويم، يجب عليك إجراء عملية **إعادة حساب فترات دفتر الأستاذ** في كل كيان قانوني (شركة) يتم تعيين التقويم له.</span><span class="sxs-lookup"><span data-stu-id="37e6e-120">After you change the periods in a calendar, you must run the **Recalculate ledger periods** process in every legal entity (company) that the calendar is assigned to.</span></span> <span data-ttu-id="37e6e-121">على الرغم من عدم وجود رسالة تحذير تذكرك بإكمال هذه الخطوة، فإن عملية إعادة الحساب مطلوبة لتحديث الفترة التي تم تعيينها لكل حركة تم ترحيلها في دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="37e6e-121">Although no warning message reminds you to complete this step, the recalculation process is required to update the period that is assigned to each posted transaction in General ledger.</span></span> <span data-ttu-id="37e6e-122">لإجراء عملية إعادة الحساب، حدد **إعادة حساب فترات دفتر الأستاذ** في صفحة **إعداد دفتر الأستاذ** في كل شركة.</span><span class="sxs-lookup"><span data-stu-id="37e6e-122">To run the recalculation process, select **Recalculate ledger periods** on the **Ledger setup** page in each company.</span></span>

<span data-ttu-id="37e6e-123">إذا لم يتم تشغيل عملية إعادة الحساب، فقد يتم تضمين أرصدة الحركات في ميزان المراجعة أو القوائم المالية بشكل غير صحيح في الفترات.</span><span class="sxs-lookup"><span data-stu-id="37e6e-123">If the recalculation process isn't run, transaction balances on a trial balance or on financial statements might be incorrectly included in periods.</span></span> <span data-ttu-id="37e6e-124">في هذه الحالة، يمكنك تصحيح الأرصدة في أي وقت عن طريق إجراء عملية إعادة الحساب.</span><span class="sxs-lookup"><span data-stu-id="37e6e-124">In this case, you can correct the balances at any time by running the recalculation process.</span></span>

### <a name="assign-a-new-fiscal-calendar"></a><span data-ttu-id="37e6e-125">تعيين تقويم مالي جديد</span><span class="sxs-lookup"><span data-stu-id="37e6e-125">Assign a new fiscal calendar</span></span>

<span data-ttu-id="37e6e-126">لتعيين تقويم مالي جديد، انتقل إلى **دفتر الأستاذ العام \> إعداد دفتر الأستاذ \> دفتر الأستاذ**، وحدد **تحرير** لوضع صفحة **دفتر الأستاذ** في وضع التحرير.</span><span class="sxs-lookup"><span data-stu-id="37e6e-126">To assign a new fiscal calendar, go to **General ledger \> Ledger setup \> Ledger**, and select **Edit** to put the **Ledger** page into edit mode.</span></span> <span data-ttu-id="37e6e-127">بعد ذلك، في حقل **التقويم المالي**، حدد تقويمًا ماليًا جديدًا.</span><span class="sxs-lookup"><span data-stu-id="37e6e-127">Then, in the **Fiscal calendar** field, select a new fiscal calendar.</span></span>

<span data-ttu-id="37e6e-128">بعد تغيير التقويم المالي لدفتر الأستاذ، يجب عليك إجراء **إعادة حساب فترات دفتر الأستاذ**.</span><span class="sxs-lookup"><span data-stu-id="37e6e-128">After you change the fiscal calendar for a ledger, you must run the **Recalculate ledger periods**.</span></span> <span data-ttu-id="37e6e-129">عند تعيين تقويم مالي جديد إلى دفتر أستاذ، تذكرك رسالة بإتمام هذه الخطوة.</span><span class="sxs-lookup"><span data-stu-id="37e6e-129">When you assign a new fiscal calendar to a ledger, a message reminds you to complete this step.</span></span> <span data-ttu-id="37e6e-130">على الرغم من أن الرسالة قد تشير إلى أن عملية إعادة الحساب اختيارية، إلا أنها ليست كذلك.</span><span class="sxs-lookup"><span data-stu-id="37e6e-130">Although the message might seem to indicate that the recalculation process is optional, it isn't.</span></span> <span data-ttu-id="37e6e-131">يلزم تحديث الفترة التي تم تعيينها لكل حركة تم ترحيلها في دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="37e6e-131">It's required to update the period that is assigned to each posted transaction in General ledger.</span></span> <span data-ttu-id="37e6e-132">لإجراء عملية إعادة الحساب، حدد **إعادة حساب فترات دفتر الأستاذ** في صفحة **إعداد دفتر الأستاذ**.</span><span class="sxs-lookup"><span data-stu-id="37e6e-132">To run the recalculation process, select **Recalculate ledger periods** on the **Ledger setup** page.</span></span>

<span data-ttu-id="37e6e-133">إذا لم يتم تشغيل عملية إعادة الحساب، فقد يتم تضمين أرصدة الحركات في ميزان المراجعة أو القوائم المالية بشكل غير صحيح في الفترات.</span><span class="sxs-lookup"><span data-stu-id="37e6e-133">If the recalculation process isn't run, transaction balances on a trial balance or on financial statements might be incorrectly included in periods.</span></span> <span data-ttu-id="37e6e-134">في هذه الحالة، يمكنك تصحيح الأرصدة في أي وقت عن طريق إجراء عملية إعادة الحساب.</span><span class="sxs-lookup"><span data-stu-id="37e6e-134">In this case, you can correct the balances at any time by running the recalculation process.</span></span>
