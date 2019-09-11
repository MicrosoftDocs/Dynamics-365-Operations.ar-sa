---
title: وقت تعطل الصيانة
description: يصف هذا الموضوع وقت تعطل الصيانة في إدارة الأصول.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.openlocfilehash: cc79dc1b5911679586fa560142ada5add1a881d2
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918234"
---
# <a name="maintenance-downtime"></a><span data-ttu-id="16c07-103">وقت تعطل الصيانة</span><span class="sxs-lookup"><span data-stu-id="16c07-103">Maintenance downtime</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="16c07-104">يمكن إنشاء تسجيلات وقت تعطل الصيانة على الأصل المحدد في أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="16c07-104">You can create maintenance downtime registrations on the asset selected on a work order.</span></span> <span data-ttu-id="16c07-105">ويكون ذلك مفيدًا إذا كنت ترغب في تسجيل وقت تعطل الصيانة على جهاز واحد أو أكثر في منطقه الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="16c07-105">This is useful if you want to register maintenance downtime on one or more machines in the production area.</span></span> <span data-ttu-id="16c07-106">ستقوم أولاً بإنشاء أكواد أسباب وقت تعطل الصيانة التي ترغب في استخدامها، على سبيل المثال، التقسيم والتوقف المخطط.</span><span class="sxs-lookup"><span data-stu-id="16c07-106">First, you create the maintenance downtime reason codes that you want to use, for example, breakdown and planned stop.</span></span> <span data-ttu-id="16c07-107">يتم ذلك في **أكواد أسباب وقت تعطل الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="16c07-107">This is done in **Maintenance downtime reason codes**.</span></span> <span data-ttu-id="16c07-108">بعد ذلك، يمكن إنشاء تسجيلات وقت تعطل الصيانة في **وقت تعطل الصيانة** وإضافة أكواد الأسباب ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="16c07-108">Next, you can create maintenance downtime registrations in **Maintenance downtime** and add the relevant reason codes.</span></span>

## <a name="create-maintenance-downtime-reason-codes"></a><span data-ttu-id="16c07-109">إنشاء أكواد أسباب وقت تعطل الصيانة</span><span class="sxs-lookup"><span data-stu-id="16c07-109">Create maintenance downtime reason codes</span></span>

1. <span data-ttu-id="16c07-110">انقر فوق **إدارة الأصول** > **الإعداد** > **أوامر العمل** > **أكواد أسباب وقت تعطل الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="16c07-110">Click **Asset management** > **Setup** > **Work orders** > **Maintenance downtime reason codes**.</span></span>

2. <span data-ttu-id="16c07-111">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="16c07-111">Click **New**.</span></span>

3. <span data-ttu-id="16c07-112">أدخل معرفًا في حقل **كود سبب وقت تعطل الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="16c07-112">Insert an ID in the **Maintenance downtime reason code** field.</span></span>

4. <span data-ttu-id="16c07-113">في حقل **الاسم** أدخل اسمًا لكود السبب.</span><span class="sxs-lookup"><span data-stu-id="16c07-113">Insert a name for the reason code in the **Name** field.</span></span>

5. <span data-ttu-id="16c07-114">حدد خانة الاختيار **تضمين KPI** إذا كان يجب تضمين كود السبب في حسابات مؤشرات الأداء الأساسية للأصول‬‏‫.</span><span class="sxs-lookup"><span data-stu-id="16c07-114">Select the **KPI include** check box if the reason code should be included in asset KPI calculations.</span></span> <span data-ttu-id="16c07-115">بشكل عام، لا يجب تضمين توقفات الإنتاج المخططة في حسابات مؤشرات الأداء الأساسية، لأنها لا تؤثر على الأداء المتوقع.</span><span class="sxs-lookup"><span data-stu-id="16c07-115">Generally, planned production stops should not be included in KPI calculations as they do not impact expected performance.</span></span>

6. <span data-ttu-id="16c07-116">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="16c07-116">Click **Save**.</span></span>

![الشكل 1](media/15-work-orders.png)


<span data-ttu-id="16c07-118">عند إنشاء أكواد أسباب وقت تعطل الصيانة التي ترغب في استخدامها، يمكن إنشاء تسجيلات وقت تعطل الصيانة الخاصة بأوامر العمل والأصول.</span><span class="sxs-lookup"><span data-stu-id="16c07-118">When you have created the maintenance downtime reason codes you want to use, you can create maintenance downtime registrations for work orders and assets.</span></span>


## <a name="create-maintenance-downtime-registrations"></a><span data-ttu-id="16c07-119">إنشاء تسجيلات وقت تعطل الصيانة</span><span class="sxs-lookup"><span data-stu-id="16c07-119">Create maintenance downtime registrations</span></span>

1. <span data-ttu-id="16c07-120">انقر فوق **إدارة الأصول** > **عام** > **أوامر العمل** > **جميع أوامر العمل** أو **أوامر العمل النشطة**.</span><span class="sxs-lookup"><span data-stu-id="16c07-120">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="16c07-121">حدد أمر العمل وانقر فوق **وقت تعطل الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="16c07-121">Select the work order and click **Maintenance downtime**.</span></span>

3. <span data-ttu-id="16c07-122">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="16c07-122">Click **New**.</span></span>

4. <span data-ttu-id="16c07-123">قم بإدراج التاريخ والفترة الزمنية لتسجيل وقت تعطل الصيانة في الحقلين **من** و**إلى**.</span><span class="sxs-lookup"><span data-stu-id="16c07-123">Insert date and time interval for the maintenance downtime registration in the **From** and **To** fields.</span></span>

5. <span data-ttu-id="16c07-124">عندما تغادر الحقل **إلى**، يتم إدراج المدة بالساعات بشكل تلقائي في حقل **المدة**.</span><span class="sxs-lookup"><span data-stu-id="16c07-124">When you leave the **To** field, the duration in hours is automatically inserted in the **Duration** field.</span></span>

6. <span data-ttu-id="16c07-125">حدد كود سبب في حقل **كود سبب وقت تعطل الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="16c07-125">Select a reason code in the **maintenance downtime reason code** field.</span></span>

7. <span data-ttu-id="16c07-126">كرر الخطوات من 3 إلى 6 لإضافة المزيد من التسجيلات.</span><span class="sxs-lookup"><span data-stu-id="16c07-126">Repeat steps 3-6 if you want to add more registrations.</span></span>

8. <span data-ttu-id="16c07-127">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="16c07-127">Click **Save**.</span></span>


![الشكل 2](media/16-work-orders.png)


<span data-ttu-id="16c07-129">يتوقف التقويم المستخدم في حساب تسجيل وقت تعطل الصيانة على تحديدك في إعداد الأصول والمعلمات.</span><span class="sxs-lookup"><span data-stu-id="16c07-129">The calendar used to calculate a maintenance downtime registration depends on your selection in the setup of assets and parameters.</span></span> <span data-ttu-id="16c07-130">إذا تم تحديد مورد على أحد الأصول في **كل الأصول** > علامة التبويب السريعة **الأصل الثابت** > حقل **المورد**، فسيتم استخدام إعداد التقويم لمجموعة الموارد المقترنة، كما هو مبين في الشكل التالي.</span><span class="sxs-lookup"><span data-stu-id="16c07-130">If a resource is selected on an asset in **All assets** > **Fixed asset** FastTab > **Resource** field, the calendar set up for the associated resource group is used, as shown in the following figure.</span></span>

![الشكل 3](media/17-work-orders.png)


<span data-ttu-id="16c07-132">إذا لم يتم تحديد أي مورد على الأصل، فسيتم استخدام التقويم القياسي المحدد في **محددات إدارة الأصول**، كما هو مبين في الشكل التالي.</span><span class="sxs-lookup"><span data-stu-id="16c07-132">If no resource is selected on the asset, the standard calendar selected in **Asset management parameters** is used, as shown in the following figure.</span></span>

![الشكل 4](media/18-work-orders.png)


<span data-ttu-id="16c07-134">انقر فوق **إدارة أصول المؤسسة** > **استعلامات** > **وقت تعطل الصيانة** للاطلاع على نظرة عامة على تسجيلات وقت تعطل الصيانة.</span><span class="sxs-lookup"><span data-stu-id="16c07-134">Click **Enterprise asset management** > **Inquiries** > **Maintenance downtime** to see an overview of all maintenance downtime registrations.</span></span>

>[!NOTE]
><span data-ttu-id="16c07-135">تم إعداد كافة التقويمات المستخدمة في الوحدة النمطية **إدارة الأصول** في **إدارة المؤسسة** > **الإعداد** > **التقويمات** > **التقويمات**.</span><span class="sxs-lookup"><span data-stu-id="16c07-135">All calendars used in the **Asset Management** module are set up in **Organization administration** > **Setup** > **Calendars** > **Calendars**.</span></span>

