---
title: وقت تعطل الصيانة
description: يصف هذا الموضوع وقت تعطل الصيانة في إدارة الأصول.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
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
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ad9f1b2a0e63b4fb0d6daceb451c3a1dc1ec7de7
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626129"
---
# <a name="maintenance-downtime"></a><span data-ttu-id="2cd09-103">وقت تعطل الصيانة</span><span class="sxs-lookup"><span data-stu-id="2cd09-103">Maintenance downtime</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="2cd09-104">يمكن إنشاء تسجيلات وقت تعطل الصيانة على الأصل المحدد في أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="2cd09-104">You can create maintenance downtime registrations on the asset that is selected on a work order.</span></span> <span data-ttu-id="2cd09-105">وتكون هذه الإمكانية مفيدة إذا كنت ترغب في تسجيل وقت تعطل الصيانة على جهاز واحد أو أكثر في منطقه الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="2cd09-105">This capability is useful if you want to register maintenance downtime on one or more machines in the production area.</span></span> <span data-ttu-id="2cd09-106">تقوم أولاً بإنشاء أكواد أسباب وقت تعطل الصيانة التي ترغب في استخدامها، على سبيل المثال، **التفصيل** و **التوقف المخطط**.</span><span class="sxs-lookup"><span data-stu-id="2cd09-106">You first create the maintenance downtime reason codes that you want to use, such as **Breakdown** and **Planned stop**.</span></span> <span data-ttu-id="2cd09-107">يتم إجراء هذه الخطوة في صفحة **أكواد أسباب وقت تعطل الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="2cd09-107">This step is done on the **Maintenance downtime reason codes** page.</span></span> <span data-ttu-id="2cd09-108">بعد ذلك، يمكنك إنشاء تسجيلات وقت تعطل الصيانة في صفحة **وقت تعطل الصيانة** وإضافة أكواد أسباب وقت تعطل الصيانة ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="2cd09-108">You can then create maintenance downtime registrations on the **Maintenance downtime** page and add the relevant maintenance downtime reason codes.</span></span>

## <a name="create-maintenance-downtime-reason-codes"></a><span data-ttu-id="2cd09-109">إنشاء أكواد أسباب وقت تعطل الصيانة</span><span class="sxs-lookup"><span data-stu-id="2cd09-109">Create maintenance downtime reason codes</span></span>

1. <span data-ttu-id="2cd09-110">حدد **إدارة الأصول** > **إعداد** > **أوامر العمل** > **أكواد أسباب وقت تعطل الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="2cd09-110">Select **Asset management** > **Setup** > **Work orders** > **Maintenance downtime reason codes**.</span></span>

2. <span data-ttu-id="2cd09-111">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="2cd09-111">Select **New**.</span></span>

3. <span data-ttu-id="2cd09-112">في الحقل **كود سبب وقت تعطل الصيانة** ، ادخل معرفًا لكود سبب وقت تعطل الصيانة.</span><span class="sxs-lookup"><span data-stu-id="2cd09-112">In the **Maintenance downtime reason code** field, enter an ID for the maintenance downtime reason code.</span></span>

4. <span data-ttu-id="2cd09-113">في حقل **الاسم**، أدخل اسمًا.</span><span class="sxs-lookup"><span data-stu-id="2cd09-113">In the **Name** field, enter a name.</span></span>

5. <span data-ttu-id="2cd09-114">حدد خانه الاختيار **تضمين KPI** إذا كان يجب تضمين كود السبب في حسابات مؤشرات الأداء الرئيسية (KPIs) للأصل.</span><span class="sxs-lookup"><span data-stu-id="2cd09-114">Select the **KPI include** check box if the reason code should be included in calculations of key performance indicators (KPIs) for the asset.</span></span> <span data-ttu-id="2cd09-115">وبشكل عام، لا يجب تضمين توقفات الإنتاج المخططة في حسابات مؤشرات الأداء الأساسية، لأنها لا تؤثر على الأداء المتوقع.</span><span class="sxs-lookup"><span data-stu-id="2cd09-115">In general, planned production stops should not be included in KPI calculations, because they don't affect expected performance.</span></span>

6. <span data-ttu-id="2cd09-116">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="2cd09-116">Select **Save**.</span></span>

<span data-ttu-id="2cd09-117">يبين الرسم التوضيحي أدناه مثالًا لصفحة **أكواد أسباب وقت تعطل الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="2cd09-117">The illustration below shows an example of the **Maintenance downtime reason codes** page.</span></span>

![الشكل 1](media/15-work-orders.png)

<span data-ttu-id="2cd09-119">بعد إنشاء أكواد أسباب وقت تعطل الصيانة التي ترغب في استخدامها، يمكن إنشاء تسجيلات وقت تعطل الصيانة الخاصة بأوامر العمل والأصول.</span><span class="sxs-lookup"><span data-stu-id="2cd09-119">After you've created the maintenance downtime reason codes that you want to use, you can create maintenance downtime registrations for work orders and assets.</span></span>


## <a name="create-maintenance-downtime-registrations"></a><span data-ttu-id="2cd09-120">إنشاء تسجيلات وقت تعطل الصيانة</span><span class="sxs-lookup"><span data-stu-id="2cd09-120">Create maintenance downtime registrations</span></span>

1. <span data-ttu-id="2cd09-121">انقر فوق **إدارة الأصول** > **عام** > **أوامر العمل** > **جميع أوامر العمل** أو **أوامر العمل النشطة**.</span><span class="sxs-lookup"><span data-stu-id="2cd09-121">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="2cd09-122">حدد أمر العمل، ثم من علامة التبويب **أمر العمل** ، في مجموعة **الأصول** ، حدد **وقت تعطل الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="2cd09-122">Select the work order, and then, on the **Work order** tab, in the **Asset** group, select **Maintenance downtime**.</span></span>

3. <span data-ttu-id="2cd09-123">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="2cd09-123">Select **New**.</span></span>

4. <span data-ttu-id="2cd09-124">حدد التاريخ والفترة الزمنية لتسجيل وقت تعطل الصيانة في الحقلين **من** و **إلى** .</span><span class="sxs-lookup"><span data-stu-id="2cd09-124">In the **From** and **To** fields, define the date and time interval for the maintenance downtime registration.</span></span>

>[!NOTE]
><span data-ttu-id="2cd09-125">عندما تغادر الحقل **إلى**، يتم إدراج المدة بالساعات بشكل تلقائي في حقل **المدة**.</span><span class="sxs-lookup"><span data-stu-id="2cd09-125">When you leave the **To** field, the duration in hours is automatically inserted in the **Duration** field.</span></span>

5. <span data-ttu-id="2cd09-126">حدد كود السبب في حقل **كود سبب وقت تعطل الصيانة** .</span><span class="sxs-lookup"><span data-stu-id="2cd09-126">In the **maintenance downtime reason code** field, select a reason code.</span></span>

6. <span data-ttu-id="2cd09-127">كرر الخطوات من 3 إلى 5 لإضافة مزيد من التسجيلات.</span><span class="sxs-lookup"><span data-stu-id="2cd09-127">Repeat steps 3 through 5 to add more registrations.</span></span>

7. <span data-ttu-id="2cd09-128">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="2cd09-128">Select **Save**.</span></span>

<span data-ttu-id="2cd09-129">يبين الرسم التوضيحي أدناه مثالاً على تسجيل وقت تعطل الصيانة.</span><span class="sxs-lookup"><span data-stu-id="2cd09-129">The illustration below shows an example of maintenance downtime registration.</span></span>

![الشكل 2](media/16-work-orders.png)

<span data-ttu-id="2cd09-131">يتوقف التقويم المستخدم في حساب تسجيل وقت تعطل الصيانة على تحديدك في إعداد الأصول والمعلمات.</span><span class="sxs-lookup"><span data-stu-id="2cd09-131">The calendar that is used to calculate a maintenance downtime registration depends on your selection in the setup of assets and parameters.</span></span> <span data-ttu-id="2cd09-132">إذا تم تحديد مورد على أحد الأصول في حقل **مورد** على علامة التبويب السريعة **الأصل الثابت** لصفحة **كافة الأصول** ، فسيتم استخدام إعداد التقويم لمجموعة الموارد المقترنة، كما هو مبين في الشكل التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="2cd09-132">If a resource is selected on an asset in the **Resource** field on the **Fixed asset** FastTab of the **All assets** page, the calendar that is set up for the associated resource group is used, as shown in the following illustration.</span></span>

![الشكل 3](media/17-work-orders.png)

<span data-ttu-id="2cd09-134">إذا لم يتم تحديد أي مورد على الأصل، فسيتم استخدام التقويم القياسي المحدد في صفحة **معلمات إدارة الأصول** ، كما هو مبين في الشكل التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="2cd09-134">If no resource is selected on the asset, the standard calendar that is selected on the **Asset management parameters** page is used, as shown in the following illustration.</span></span>

![الشكل 4](media/18-work-orders.png)

<span data-ttu-id="2cd09-136">انقر فوق **إدارة الأصول** > **استعلامات** > **وقت تعطل الصيانة** للاطلاع على نظرة عامة على تسجيلات وقت تعطل الصيانة.</span><span class="sxs-lookup"><span data-stu-id="2cd09-136">To see an overview of all maintenance downtime registrations, click **Asset management** > **Inquiries** > **Maintenance downtime**.</span></span>

>[!NOTE]
><span data-ttu-id="2cd09-137">تم إعداد كافة التقويمات المستخدمة في الوحدة النمطية **إدارة الأصول** في **إدارة المؤسسة** > **إعداد** > **التقويمات** > **التقويمات**.</span><span class="sxs-lookup"><span data-stu-id="2cd09-137">All calendars that are used in the **Asset Management** module are set up in **Organization administration** > **Setup** > **Calendars** > **Calendars**.</span></span>

