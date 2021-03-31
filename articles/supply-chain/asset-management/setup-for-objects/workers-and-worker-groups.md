---
title: عاملو الصيانة ومجموعات عاملي الصيانة
description: يشرح هذا الموضوع عاملو الصيانة ومجموعات عاملي الصيانة في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetWorkerGroupCopyFromResourceGroup, EntAssetWorkerGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 00ada9e43ae08e1757de618bd2d63dc147beeca0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5226823"
---
# <a name="maintenance-workers-and-worker-groups"></a><span data-ttu-id="fa4ec-103">عاملو الصيانة ومجموعات عاملي الصيانة</span><span class="sxs-lookup"><span data-stu-id="fa4ec-103">Maintenance workers and worker groups</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="fa4ec-104">يشرح هذا الموضوع عاملو الصيانة ومجموعات عاملي الصيانة في إدارة الأصول.</span><span class="sxs-lookup"><span data-stu-id="fa4ec-104">This topic explains maintenance workers and worker groups in Asset Management.</span></span> <span data-ttu-id="fa4ec-105">في إدارة الأصول، يمكنك توصيل عاملي الصيانة بمواقع العمل.</span><span class="sxs-lookup"><span data-stu-id="fa4ec-105">In Asset Management, you can connect maintenance workers to functional locations.</span></span> <span data-ttu-id="fa4ec-106">(لمزيد من المعلومات حول مواقع العمل، راجع [إنشاء مواقع عمل‬](../functional-locations/create-functional-locations.md).) قد تكون هذه الوظيفة مفيدة إذا كنت، على سبيل المثال، تقوم بجدولة مهمة صيانة على جهاز موجود في موقع العمل 01، وتريد تخصيص عاملي الصيانة من نفس الموقع لتنفيذ المهمة.</span><span class="sxs-lookup"><span data-stu-id="fa4ec-106">(For more information about functional locations, see [Create functional locations](../functional-locations/create-functional-locations.md).) This functionality might be useful if, for example, you're scheduling a maintenance job on a machine that is located in functional location 01, and you want to allocate maintenance workers from the same location to perform the job.</span></span>

<span data-ttu-id="fa4ec-107">يمكنك أيضًا إنشاء مجموعات عاملي الصيانة وإقران عاملي الصيانة بها.</span><span class="sxs-lookup"><span data-stu-id="fa4ec-107">You can also create maintenance worker groups and associate maintenance workers with them.</span></span> <span data-ttu-id="fa4ec-108">تكون هذه الوظيفة مفيدة عند جدولة أوامر عمل بسيطة، وتريد جدولة مجموعة من عاملي الصيانة على أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="fa4ec-108">This functionality is useful when you do simple work order scheduling, and you want to schedule a group of maintenance workers on a work order.</span></span> <span data-ttu-id="fa4ec-109">يمكنك استخدام عاملي الصيانة ومجموعات عاملي الصيانة لإعداد عاملي الصيانة المفضلين وعاملي الصيانة المسؤولين.</span><span class="sxs-lookup"><span data-stu-id="fa4ec-109">You can use maintenance workers and maintenance worker groups to set up preferred maintenance workers and responsible maintenance workers.</span></span> 


## <a name="create-workers"></a><span data-ttu-id="fa4ec-110">إنشاء معلومات العاملين</span><span class="sxs-lookup"><span data-stu-id="fa4ec-110">Create workers</span></span>

1. <span data-ttu-id="fa4ec-111">حدد **إدارة الأصول** \> **الإعداد** \> **العاملون** \> **العاملون**.</span><span class="sxs-lookup"><span data-stu-id="fa4ec-111">Select **Asset management** \> **Setup** \> **Workers** \> **Workers**.</span></span>
2. <span data-ttu-id="fa4ec-112">حدد **جديد** لإضافة عامل إلى القائمة.</span><span class="sxs-lookup"><span data-stu-id="fa4ec-112">Select **New** to add a worker to the list.</span></span>
3. <span data-ttu-id="fa4ec-113">حدد عاملاً في حقل **العامل**.</span><span class="sxs-lookup"><span data-stu-id="fa4ec-113">In the **Worker** field, select the worker.</span></span>
4. <span data-ttu-id="fa4ec-114">عيّن الخيار **نشط** إلى **نعم** لجدولة العامل على أوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="fa4ec-114">Set the **Active** option to **Yes** to schedule the worker on work orders.</span></span>

    <span data-ttu-id="fa4ec-115">على علامة التبويب السريعة **عام**، تتم تعبئة الحقلين **المورد** و **الوصف** تلقائيًا في حالة تحديد مورد للعامل.</span><span class="sxs-lookup"><span data-stu-id="fa4ec-115">On the **General** FastTab, the **Resource** and **Description** fields are automatically filled in if a resource has been selected for the worker.</span></span> <span data-ttu-id="fa4ec-116">تتم أيضًا تعبئة حقل **التقويم** تلقائيًا، شريطة إعداد العامل كمورد وتخصيص تقويم لهذا المورد في صفحة **الموارد‏‎** (**إدارة المؤسسة‬** \> **الموارد‏‎‏‎** \> **الموارد‏‎‏‎**).</span><span class="sxs-lookup"><span data-stu-id="fa4ec-116">The **Calendar** field is also automatically filled in, provided that you've set up the worker as a resource and allocated a calendar to that resource on the **Resources** page (**Organization administration** \> **Resources** \> **Resources**).</span></span>

5. <span data-ttu-id="fa4ec-117">على علامة التبويب السريعة **المجموعات** حدد **إضافة**، ثم حدد مجموعة عاملي صيانة للعامل.</span><span class="sxs-lookup"><span data-stu-id="fa4ec-117">On the **Groups** FastTab, select **Add**, and then select a maintenance worker group for the worker.</span></span> <span data-ttu-id="fa4ec-118">بإمكان عامل واحد الانتساب إلى أكثر من مجموعة واحدة.</span><span class="sxs-lookup"><span data-stu-id="fa4ec-118">A worker can be affiliated with more than one group.</span></span>
6. <span data-ttu-id="fa4ec-119">في الإعداد القياسي، يكون انتساب العامل إلى مجموعة ساري المفعول اعتبارًا من تاريخ إضافة المجموعة، ولا تنتهي صلاحيته أبدًا.</span><span class="sxs-lookup"><span data-stu-id="fa4ec-119">In the standard setup, a worker's affiliation with a group is effective from the date when you add the group, and it never expires.</span></span> <span data-ttu-id="fa4ec-120">يظهر هذا التاريخ في الحقل **ساري**.</span><span class="sxs-lookup"><span data-stu-id="fa4ec-120">This date is shown in the **Effective** field.</span></span> <span data-ttu-id="fa4ec-121">لرؤية الحقل **ساري**، حدد **عرض** \> **الكل**.</span><span class="sxs-lookup"><span data-stu-id="fa4ec-121">To see the **Effective** field, select **View** \> **All**.</span></span> <span data-ttu-id="fa4ec-122">إذا كان يجب أن يقتصر انتساب العامل إلى مجموعة على فترة محددة، فاستخدم الحقلين **ساري** و **انتهاء الصلاحية** لتحديد الفترة.</span><span class="sxs-lookup"><span data-stu-id="fa4ec-122">If the worker's affiliation with a group should be limited to a specific period, use the **Effective** and **Expiration** fields to define the period.</span></span>
7. <span data-ttu-id="fa4ec-123">على علامة التبويب السريعة **مواقع العمل**، حدد **إضافة**، ثم حدد موقع عامل لعامل الصيانة.</span><span class="sxs-lookup"><span data-stu-id="fa4ec-123">On the **Functional locations** FastTab, select **Add**, and then select a functional location for the maintenance worker.</span></span> <span data-ttu-id="fa4ec-124">حدد أيضًا الموقع الذي تريده كموقع عمل أساسي للعامل.</span><span class="sxs-lookup"><span data-stu-id="fa4ec-124">Also specify which location is the primary functional location for the worker.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fa4ec-125">عند إضافة مواقع عمل إلى عامل، تظهر كافة الأصول النشطة المرتبطة بمواقع العمل هذه في مختلف بنود القائمة، مثل **أصولي النشطة** و **مواقع العمل النشطة الخاصة بي**.</span><span class="sxs-lookup"><span data-stu-id="fa4ec-125">When you add functional locations to a worker, all active assets that are related to those functional locations appear on various menu items, such as **My active assets** and **My active functional locations**.</span></span> <span data-ttu-id="fa4ec-126">كما تظهر في عمليات البحث عن الأصول التي تظهر عند إنشاء أصل أو طلب صيانة أو أمر عمل جديد.</span><span class="sxs-lookup"><span data-stu-id="fa4ec-126">They also appear in the asset lookups that are shown when you create a new asset, maintenance request, or work order.</span></span>

    <span data-ttu-id="fa4ec-127">تعرض الحقول الموجودة في علامة التبويب السريعة **تفاصيل** عدد مجموعات عاملي الصيانة ومواقع العمل التي يرتبط بها عامل الصيانة المحدد.</span><span class="sxs-lookup"><span data-stu-id="fa4ec-127">The fields on the **Details** FastTab show the number of maintenance worker groups and functional locations that the selected maintenance worker is related to.</span></span>

## <a name="create-worker-groups"></a><span data-ttu-id="fa4ec-128">إنشاء مجموعات عاملين</span><span class="sxs-lookup"><span data-stu-id="fa4ec-128">Create worker groups</span></span>

1. <span data-ttu-id="fa4ec-129">حدد **إدارة الأصول** \> **الإعداد** \> **العاملون** \> **مجموعات عاملي الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="fa4ec-129">Select **Asset management** \> **Setup** \> **Workers** \> **Maintenance worker groups**.</span></span>
2. <span data-ttu-id="fa4ec-130">حدد **جديد** لإضافة مجموعة عاملين إلى القائمة.</span><span class="sxs-lookup"><span data-stu-id="fa4ec-130">Select **New** to add a worker group to the list.</span></span>
3. <span data-ttu-id="fa4ec-131">في الحقل **مجموعة عاملي الصيانة**، أدخل معرف مجموعة.</span><span class="sxs-lookup"><span data-stu-id="fa4ec-131">In the **Maintenance worker group** field, enter a group ID.</span></span>
4. <span data-ttu-id="fa4ec-132">في حقل **الاسم**، أدخل اسمًا.</span><span class="sxs-lookup"><span data-stu-id="fa4ec-132">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="fa4ec-133">على علامة التبويب السريعة **العاملون** حدد **إضافة**، ثم حدد عامل صيانة لمجموعة العاملين.</span><span class="sxs-lookup"><span data-stu-id="fa4ec-133">On the **Workers** FastTab, select **Add**, and then select a maintenance worker for the worker group.</span></span> <span data-ttu-id="fa4ec-134">للحصول على معلومات حول الحقلين **ساري** و **انتهاء الصلاحية**، راجع الخطوة 6 في الإجراء السابق.</span><span class="sxs-lookup"><span data-stu-id="fa4ec-134">For information about the **Effective** and **Expiration** fields, see step 6 in the previous procedure.</span></span>
6. <span data-ttu-id="fa4ec-135">حدد **نسخ من مجموعة الموارد**، لربط مجموعة موارد بمجموعة عاملي الصيانة المحددة.</span><span class="sxs-lookup"><span data-stu-id="fa4ec-135">If a resource group should be related to the selected maintenance worker group, select **Copy from resource group**.</span></span> <span data-ttu-id="fa4ec-136">في الحقل‏‎ **المجموعة**، حدد مجموعة الموارد لنسخ إعدادات التقويم منها.</span><span class="sxs-lookup"><span data-stu-id="fa4ec-136">In the **Group** field, select the resource group to copy calendar settings from.</span></span> <span data-ttu-id="fa4ec-137">ثم، في الحقل **مجموعة عاملين**، حدد مجموعة العاملين لنسخ إعدادات التقويم لمجموعة الموارد إليها.</span><span class="sxs-lookup"><span data-stu-id="fa4ec-137">Then, in the **Worker group** field, select the worker group to copy the resource group's calendar settings to.</span></span> <span data-ttu-id="fa4ec-138">تكون هذه الخطوة ذات صلة فقط إذا كنت تريد أن يستخدم عاملون الصيانة التقويم المرتبط بمورد (مركز العمل) أثناء جدولة أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="fa4ec-138">This step is relevant only if you want maintenance workers to use the calendar that is related to a resource (work center) during work order scheduling.</span></span>

    <span data-ttu-id="fa4ec-139">تعرض الحقول الموجودة في علامة التبويب السريعة **تفاصيل** عدد عاملي الصيانة الذين تم إعدادهم على مجموعة عاملي الصيانة المحددة.</span><span class="sxs-lookup"><span data-stu-id="fa4ec-139">The field on the **Details** FastTab shows the number of maintenance workers that have been set up on the selected maintenance worker group.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]