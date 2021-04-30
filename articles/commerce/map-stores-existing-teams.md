---
title: تعيين المتاجر والفرق عند وجود فرق موجودة مسبقًا في Microsoft Teams
description: يغطي هذا الموضوع كيفيه تعيين المتاجر والفرق المقابلة في مقارات Dynamics 365 Commerce إذا كانت مؤسستك قد إنشات بالفعل فرقا في العمل Microsoft Teams قبل تكامل Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5a711c1057b87bd792755ef91a84d1c28879c590
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908485"
---
# <a name="map-stores-and-teams-if-there-are-pre-existing-teams-in-microsoft-teams"></a><span data-ttu-id="ef79f-103">تعيين المتاجر والفرق عند وجود فرق موجودة مسبقًا في Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="ef79f-103">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ef79f-104">يغطي هذا الموضوع كيفيه تعيين المتاجر والفرق المقابلة في مقارات Dynamics 365 Commerce إذا كانت مؤسستك قد إنشات بالفعل فرقا في العمل Microsoft Teams قبل تكامل Commerce.</span><span class="sxs-lookup"><span data-stu-id="ef79f-104">This topic covers how to map stores and corresponding teams in Dynamics 365 Commerce headquarters if your organization has already created teams in Microsoft Teams before Commerce integration.</span></span>

<span data-ttu-id="ef79f-105">قد يكون لدي مؤسستك فرق تم إنشاؤها لبعض أو كل المتاجر قبل تكامل Dynamics 365 Commerce وMicrosoft Teams.</span><span class="sxs-lookup"><span data-stu-id="ef79f-105">Your organization may have teams created for some or all of your stores before integrating Dynamics 365 Commerce and Microsoft Teams.</span></span> <span data-ttu-id="ef79f-106">إذا كانت هذه هي الحالة، لإنشاء مزامنة المهام بين نقطة بيع Commerce وMicrosoft Teams يجب عليك تقديم تعيين المتاجر والفريق المقابل في مقر Commerce.</span><span class="sxs-lookup"><span data-stu-id="ef79f-106">If this is the case, to establish task synchronization between Commerce POS and Microsoft Teams you must provide the mapping of stores and corresponding team in Commerce headquarters.</span></span>

## <a name="map-stores-and-corresponding-teams-in-commerce-headquarters"></a><span data-ttu-id="ef79f-107">تعيين المتاجر والفرق المقابلة في مقرات Commerce</span><span class="sxs-lookup"><span data-stu-id="ef79f-107">Map stores and corresponding teams in Commerce headquarters</span></span> 

<span data-ttu-id="ef79f-108">لتعيين المتاجر والفرق المقابلة في مقرات Commerce، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="ef79f-108">To map stores and corresponding teams in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="ef79f-109">انتقل إلى **إدارة النظام \> مساحة العمل \> إدارة البيانات**.</span><span class="sxs-lookup"><span data-stu-id="ef79f-109">Go to **System Administration \> Workspace \> Data management**.</span></span>
1. <span data-ttu-id="ef79f-110">حدد **تصدير**.</span><span class="sxs-lookup"><span data-stu-id="ef79f-110">Select **Export**.</span></span> 
1. <span data-ttu-id="ef79f-111">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="ef79f-111">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="ef79f-112">ضمن **اسم المجموعة**، أدخل "تصدير تعيين Teams".</span><span class="sxs-lookup"><span data-stu-id="ef79f-112">Under **Group name**, enter "Export Teams mapping".</span></span>
1. <span data-ttu-id="ef79f-113">في علامة التبويب السريع **الكيانات المحددة**، حدد **إضافة كيان**.</span><span class="sxs-lookup"><span data-stu-id="ef79f-113">On the **Selected entities** FastTab, select **Add entity**.</span></span> <span data-ttu-id="ef79f-114">يظهر مربع الحوار **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="ef79f-114">The **Add entity** dialog box appears.</span></span>  
1. <span data-ttu-id="ef79f-115">في القائمة المنسدلة **اسم الكيان**، حدد **تعيين Teams بين المصدر والفريق**.</span><span class="sxs-lookup"><span data-stu-id="ef79f-115">In the **Entity name** drop-down list, select **Teams mapping between source and team**.</span></span>
1. <span data-ttu-id="ef79f-116">في القائمة المنسدلة **تنسيق البيانات الهدف**، حدد **CSV**.</span><span class="sxs-lookup"><span data-stu-id="ef79f-116">In the **Target data format** drop-down list, select **CSV**.</span></span>
1. <span data-ttu-id="ef79f-117">حدد **إضافة**، ثم حدد **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="ef79f-117">Select **Add**, and then select **Close**.</span></span>
1. <span data-ttu-id="ef79f-118">في أعلي الجانب الأيسر ضمن جزء الاجراء، حدد **تصدير الآن**.</span><span class="sxs-lookup"><span data-stu-id="ef79f-118">On the top left under the Action Pane, select **Export now**.</span></span>
1. <span data-ttu-id="ef79f-119">ضمن **حالة معالجة الكيان**، حدد **تنزيل الملف**.</span><span class="sxs-lookup"><span data-stu-id="ef79f-119">Under **Entity processing status**, select **Download file**.</span></span>
1. <span data-ttu-id="ef79f-120">في ملف CSV الذي تم تصديره، ادخل قيم **SOURCETYPE**، و **SOURCEID**، و **TEAMID** على النحو التالي:</span><span class="sxs-lookup"><span data-stu-id="ef79f-120">In the exported CSV file, enter values for **SOURCETYPE**, **SOURCEID**, and **TEAMID** as follows:</span></span>
    - <span data-ttu-id="ef79f-121">بالنسبة إلى **SOURCETYPE**، أدخل "RetailStore".</span><span class="sxs-lookup"><span data-stu-id="ef79f-121">For **SOURCETYPE**, enter "RetailStore".</span></span> 
    - <span data-ttu-id="ef79f-122">بالنسبة إلى **SOURCEID**، أدخل رقم المتجر (على سبيل المثال، "000135" لمتجر سان فرانسيسكو).</span><span class="sxs-lookup"><span data-stu-id="ef79f-122">For **SOURCEID**, enter the store number (for example, "000135" for the San Francisco store).</span></span> <span data-ttu-id="ef79f-123">يمكنك العثور على أرقام المتجر في **Retail وCommerce \> القنوات \> المتاجر**.</span><span class="sxs-lookup"><span data-stu-id="ef79f-123">You can find store numbers at **Retail and Commerce \> Channels \> Stores**.</span></span>
    - <span data-ttu-id="ef79f-124">بالنسبة إلى **TEAMID**، أدخل معرف الفريق المقابل من Microsoft Teams (على سبيل المثال، "5f8bc92b-6aa8-451e-85d1-3949c01ddc6c").</span><span class="sxs-lookup"><span data-stu-id="ef79f-124">For **TEAMID**, enter the corresponding team ID from Microsoft Teams (for example, "5f8bc92b-6aa8-451e-85d1-3949c01ddc6c").</span></span> <span data-ttu-id="ef79f-125">يمكنك العثور على معلومات معرف الفريق في [admin.teams.microsoft.com](https://admin.teams.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="ef79f-125">You can find team ID information at [admin.teams.microsoft.com](https://admin.teams.microsoft.com).</span></span>
1. <span data-ttu-id="ef79f-126">احفظ ملف CSV في جهازك المحلي.</span><span class="sxs-lookup"><span data-stu-id="ef79f-126">Save the CSV file to your local machine.</span></span>
1. <span data-ttu-id="ef79f-127">انتقل إلى **إدارة النظام \> مساحة العمل \> إدارة البيانات**، ثم حدد **استيراد**.</span><span class="sxs-lookup"><span data-stu-id="ef79f-127">Go to **System Administration \> Workspace \> Data management**, and then select **Import**.</span></span>
1. <span data-ttu-id="ef79f-128">في علامة التبويب السريع **الكيانات المحددة**، حدد **إضافة ملف**.</span><span class="sxs-lookup"><span data-stu-id="ef79f-128">On the **Selected entities** FastTab, select **Add file**.</span></span> <span data-ttu-id="ef79f-129">يظهر مربع الحوار **إضافة ملف**.</span><span class="sxs-lookup"><span data-stu-id="ef79f-129">The **Add file** dialog box appears.</span></span>
1. <span data-ttu-id="ef79f-130">في القائمة المنسدلة **اسم الكيان**، حدد **تعيين Teams بين المصدر والفريق**.</span><span class="sxs-lookup"><span data-stu-id="ef79f-130">In the **Entity name** drop-down list, select **Teams mapping between source and team**.</span></span>
1. <span data-ttu-id="ef79f-131">في القائمة المنسدلة **تنسيق البيانات المصدر**، حدد **CSV**.</span><span class="sxs-lookup"><span data-stu-id="ef79f-131">In the **Source data format** drop-down list, select **CSV**.</span></span>
1. <span data-ttu-id="ef79f-132">حدد **تحميل وإضافة**، وحدد ملف CSV الذي قمت بحفظه مسبقًا، ثم حدد **فتح**.</span><span class="sxs-lookup"><span data-stu-id="ef79f-132">Select **Upload and add**, select the CSV file that you saved previously, and then select **Open**.</span></span>
1. <span data-ttu-id="ef79f-133">في مربع الحوار **إضافة ملف**، حدد **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="ef79f-133">In the **Add file** dialog box, select **Close**.</span></span>
1. <span data-ttu-id="ef79f-134">في جزء الاجراء، حدد **حفظ**، ثم حدد **استيراد**.</span><span class="sxs-lookup"><span data-stu-id="ef79f-134">On the Action Pane, select **Save** , and then select **Import**.</span></span>

<span data-ttu-id="ef79f-135">توضح صورة المثال التالي مجموعة **تصدير تعيين Teams** في Commerce مع عناصر **إضافة الكيان** وتمييز رؤوس ملف CSV المُصدَّر.</span><span class="sxs-lookup"><span data-stu-id="ef79f-135">The following example image shows the **Export teams mapping** group in Commerce with **Add entity** elements and the exported CSV file headers highlighted.</span></span>

![تصدير مجموعة تعيين الفرق في Commerce مع إضافة عناصر الكيان وتمييز رؤوس ملف CSV المُصدَرة](media/d365-commerce-data-mgmt-export-entity.png)

> [!NOTE]
> <span data-ttu-id="ef79f-137">بعد إكمال الخطوات السابقة، اتبع الخطوات الواردة في [مزامنة إدارة المهام بين Microsoft Teams ونقطة البيع](synchronize-tasks-teams-pos.md) لمزامنة إدارة المهام.</span><span class="sxs-lookup"><span data-stu-id="ef79f-137">After you complete the preceeding steps, follow the steps in [Synchronize task management between Microsoft Teams and POS](synchronize-tasks-teams-pos.md) to synchronize task management.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="ef79f-138">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="ef79f-138">Additional resources</span></span>

[<span data-ttu-id="ef79f-139">نظرة عامة على تكامل Dynamics 365 Commerce وMicrosoft Teams</span><span class="sxs-lookup"><span data-stu-id="ef79f-139">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="ef79f-140">تمكين تكامل Dynamics 365 Commerce وMicrosoft Teams</span><span class="sxs-lookup"><span data-stu-id="ef79f-140">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="ef79f-141">توفير Microsoft Teams من Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="ef79f-141">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="ef79f-142">مزامنة إدارة المهام بين Microsoft Teams ونقطة بيع Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="ef79f-142">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="ef79f-143">إدارة أدوار المستخدمين في Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="ef79f-143">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="ef79f-144">الأسئلة الشائعة حول تكامل Dynamics 365 Commerce وMicrosoft Teams</span><span class="sxs-lookup"><span data-stu-id="ef79f-144">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
