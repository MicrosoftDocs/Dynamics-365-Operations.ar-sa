---
title: تكوين إدارة المهام
description: يوضح هذا الموضوع كيفية تكوين ميزات إدارة المهام في Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: ba2283bbfa2fdce75d3fbef6fcff47dd872c7998
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478034"
---
# <a name="configure-task-management"></a><span data-ttu-id="e2e6b-103">تكوين إدارة المهام</span><span class="sxs-lookup"><span data-stu-id="e2e6b-103">Configure task management</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e2e6b-104">يوضح هذا الموضوع كيفية تكوين ميزات إدارة المهام في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-104">This topic describes how to configure task management features in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e2e6b-105">قبل أن يتمكن مديرو وموظفو Dynamics 365 Commerce من استخدام ميزات إدارة المهام في Commerce، يجب أولاً تكوين إدارة المهام.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-105">Before Dynamics 365 Commerce managers and employees can use the task management features in Commerce, task management must be configured.</span></span> <span data-ttu-id="e2e6b-106">وتشمل خطوات التكوين منح الأذونات للمديرين والموظفين، وتوزيع الأذونات على عملاء نقطة البيع (POS) وإعداد إعلامات نقطة البيع، وتكوين لوحة **المهام** على الصفحة الرئيسية لتطبيق نقطه البيع.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-106">Configuration steps include granting permissions to managers and employees, distributing permissions to point of sale (POS) clients, setting up POS notifications, and configuring the **Tasks** tile on the home page of a POS application.</span></span>

## <a name="configure-permissions-for-store-managers"></a><span data-ttu-id="e2e6b-107">تكوين أذونات لمديري المتاجر</span><span class="sxs-lookup"><span data-stu-id="e2e6b-107">Configure permissions for store managers</span></span>

<span data-ttu-id="e2e6b-108">يمكن لكل العاملين في أي متجر عرض كافة المهام التي تم تعيينها لهذا المتجر.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-108">Every worker in a given store can view all tasks that are assigned to that store.</span></span> <span data-ttu-id="e2e6b-109">كما يمكنهم أيضا تحديث حالة المهام التي تم تعيينها لهم.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-109">They can also update the status of the tasks that are assigned to them.</span></span> <span data-ttu-id="e2e6b-110">ومع ذلك، يجب أن يتوفر لشخصيات مثل مديري المتجر أذونات إدارة المهام لإدارة المهام التي تم تعيينها إلى المتجر ولإنشاء مهام ذات غرض واحد.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-110">However, personas such as store managers must have task management permissions to manage tasks that are assigned to the store and to create single-purpose tasks.</span></span>

<span data-ttu-id="e2e6b-111">لتكوين أذونات إدارة المهام لمديري المتجر، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-111">To configure task management permissions for store managers, follow these steps.</span></span>

1. <span data-ttu-id="e2e6b-112">انتقل إلى **Retail and Commerce \> الموظفون \> ‏‫مجموعات الأذونات‬**.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-112">Go to **Retail and Commerce \> Employees \> Permission groups**.</span></span>
1. <span data-ttu-id="e2e6b-113">حدد مجموعة أذونات معينة (على سبيل المثال **المدير**) ثم حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-113">Select a specific permission group (for example, **Manager**), and then select **Edit**.</span></span>
1. <span data-ttu-id="e2e6b-114">في علامة التبويب السرعية **الأذونات** قم بتعيين خيار **السماح بإدارة المهام** إلى **نعم.**</span><span class="sxs-lookup"><span data-stu-id="e2e6b-114">On the **Permissions** FastTab, set the **Allow task management** option to **Yes**.</span></span>
1. <span data-ttu-id="e2e6b-115">على علامة التبويب السريعة **الإخطارات** قم بإضافة عملية **إدارة المهام** ، وأدخل قيمة في حقل **ترتيب العرض**.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-115">On the **Notifications** FastTab, add the **Task management** operation, and enter a value in the **Display order** field.</span></span> <span data-ttu-id="e2e6b-116">على سبيل المثال، أدخل **2** إذا كانت قيمة العميلة **‏‫تنفيذ الأمر‬** لـ **ترتيب العرض** هي **1** بالفعل.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-116">For example, enter **2** if the **Order fulfillment** operation already has a **Display order** value of **1**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="e2e6b-117">إذا كان يجب أن يتوفر للشخصيات الأخرى بخلاف المديرين أذونات إدارة المهام في نقطة البيع، فيمكنك منح الإذن للفرد.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-117">If a non-manager persona must have task management permissions in the POS, you can grant permission to the individual.</span></span> <span data-ttu-id="e2e6b-118">أو، يمكنك إنشاء مجموعة أذونات جديده لغير المديرين وتعيين الخيار **السماح بإدارة المهام** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-118">Alternatively, you can create a new permission group for non-managers and set the **Allow task management** option to **Yes**.</span></span>

<span data-ttu-id="e2e6b-119">يبين الرسم التوضيحي التالي كيفية تكوين أذونات إدارة المهام لمديري المتجر.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-119">The following illustration shows how to configure task management permissions for store managers.</span></span>

![تكوين أذونات إدارة المهام لمديري المتجر](media/HQ-POS-Tasks-Notifications-User-Permission.png)

## <a name="configure-permissions-for-employees"></a><span data-ttu-id="e2e6b-121">تكوين الأذونات للموظفين</span><span class="sxs-lookup"><span data-stu-id="e2e6b-121">Configure permissions for employees</span></span>

<span data-ttu-id="e2e6b-122">يجب أن يتوفر لدى الموظفين أذونات لإنشاء قوائم مهام، وإدارة معايير التعيين، وتكوين تكرار أي قائمة مهام.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-122">Employees must have permissions to create task lists, manage assignment criteria, and configure the recurrence of any task list.</span></span> <span data-ttu-id="e2e6b-123">لتكوين هذه الأذونات، قم بتعيين الموظفين على دور **مدير مهمة البيع بالتجزئة**.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-123">To configure these permissions, you assign employees to the **Retail task manager** role.</span></span>

<span data-ttu-id="e2e6b-124">لتكوين الأذونات لموظف، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-124">To configure permissions for an employee, follow these steps.</span></span>

1. <span data-ttu-id="e2e6b-125">انتقل إلى **Retail and Commerce \> الموظفون \> المستخدمون**.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-125">Go to **Retail and Commerce \> Employees \> Users**.</span></span>
1. <span data-ttu-id="e2e6b-126">حدد موظفًا.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-126">Select an employee.</span></span>
1. <span data-ttu-id="e2e6b-127">في علامة التبويب السريعة، **أدوار المستخدم** حدد **تعيين‏‎ الأدوار**.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-127">On the **User's roles** FastTab, select **Assign roles**.</span></span>
1. <span data-ttu-id="e2e6b-128">في مربع الحوار **تعيين أدوار للمستخدم** حدد دور **مدير مهمة البيع بالتجزئة** ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-128">In the **Assign roles to user** dialog box, select the **Retail task manager** role, and then select **OK**.</span></span>

## <a name="distribute-permissions-to-pos-clients"></a><span data-ttu-id="e2e6b-129">توزيع الأذونات على عملاء نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="e2e6b-129">Distribute permissions to POS clients</span></span>

<span data-ttu-id="e2e6b-130">قبل أن يتمكن الموظفون من استخدام عملاء نقطة البيع ، يجب توزيع الأذونات ومزامنتها مع هؤلاء العملاء.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-130">Before employees can use POS clients, permissions must be distributed and synced to those clients.</span></span>

<span data-ttu-id="e2e6b-131">لتوزيع الأذونات على عملاء نقطة البيع ، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-131">To distribute permissions to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="e2e6b-132">انتقل إلى **البيع بالتجزئة والتجارة \> تكنولوجيا معلومات البيع بالتجزئة والتجارة \> جدول التوزيع**.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-132">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="e2e6b-133">حدد جدول توزيع **1060** (**الفريق‬**) ثم حدد **تشغيل الآن**.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-133">Select the **1060** (**Staff**) distribution schedule, and then select **Run now**.</span></span>
1. <span data-ttu-id="e2e6b-134">حدد جدول توزيع **1070** (**تكوين القناة**) ثم حدد **تشغيل الآن**.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-134">Select the **1070** (**Channel configuration**) distribution schedule, and then select **Run now**.</span></span>

## <a name="configure-pos-notifications-for-tasks"></a><span data-ttu-id="e2e6b-135">تكوين إخطارات نقطة البيع للمهام</span><span class="sxs-lookup"><span data-stu-id="e2e6b-135">Configure POS notifications for tasks</span></span>

<span data-ttu-id="e2e6b-136">يجب تكوين إداره المهام بحيث تتوفر الإخطارات في تطبيق نقطه البيع.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-136">Task management must be configured so that notifications are available in the POS application.</span></span>

<span data-ttu-id="e2e6b-137">لتكوين إخطارات نقطة البيع للمهام اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-137">To configure POS notifications for tasks, follow these steps.</span></span>

1. <span data-ttu-id="e2e6b-138">انتقل إلى **Retail and Commerce \> إعداد القناة \> إعداد نقطة البيع \> نقطة البيع \> عمليات نقطة البيع**.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-138">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="e2e6b-139">ابحث عن العملية **1400** (**إدارة المهام**) ، وحدد خانة الاختيار **تمكين الإخطارات** لها.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-139">Find operation **1400** (**Task management**), and select the **Enable notifications** check box for it.</span></span>

<span data-ttu-id="e2e6b-140">يبين الرسم التوضيحي التالية عملية **إدارة المهام** في صفحة **عمليات نقطة البيع**.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-140">The following illustration shows the **Task management** operation on the **POS operations** page.</span></span>

![عمليه إدارة المهام في صفحة عمليات POS](media/HQ-POS-Tasks-Notifications.png)

<span data-ttu-id="e2e6b-142">لمزيد من المعلومات حول كيفية تكوين إخطارات نقاط البيع، راجع [‏‫إظهار إخطارات الأوامر في نقطة البيع (POS)](notifications-pos.md).</span><span class="sxs-lookup"><span data-stu-id="e2e6b-142">For more information about how to configure POS notifications, see [Show order notifications in the point of sale (POS)](notifications-pos.md).</span></span>

## <a name="configure-the-tasks-tile-on-a-pos-application-home-page"></a><span data-ttu-id="e2e6b-143">تكوين لوحة المهام على الصفحة الرئيسية لتطبيق نقطه البيع</span><span class="sxs-lookup"><span data-stu-id="e2e6b-143">Configure the Tasks tile on a POS application home page</span></span>

<span data-ttu-id="e2e6b-144">قبل تكوين لوحة **المهام** على الصفحة الرئيسية لتطبيق نقطه البيع، راجع [تخطيطات الشاشة الخاصة بنقطة البيع (POS)‬](pos-screen-layouts.md) للحصول على معلومات حول كيفية تكوين الأزرار الجديدة وإضافتها إلى تخطيط شاشة نقطة البيع (POS).</span><span class="sxs-lookup"><span data-stu-id="e2e6b-144">Before you configure the **Tasks** tile on the home page of a POS application, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information about how to configure and add new buttons to a POS screen layout.</span></span>

<span data-ttu-id="e2e6b-145">لتكوين لوحة **المهام** على الصفحة الرئيسية لتطبيق نقطه البيع، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-145">To configure the **Tasks** tile on a POS application home page, follow these steps.</span></span>

1. <span data-ttu-id="e2e6b-146">انتقل إلى **Retail and Commerce \> إعداد القناة \> إعداد نقطة البيع \> نقطة البيع \> تخطيطات الشاشة**.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-146">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> Screen layouts**.</span></span>
1. <span data-ttu-id="e2e6b-147">حدد تخطيط شاشة وحدد حجم التخطيط ، ثم حدد شريط أوامر.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-147">Select a screen layout, select a layout size, and select a button grid.</span></span>
1. <span data-ttu-id="e2e6b-148">على علامة التبويب السريعة **‏‫أشرطة الأوامر‬** حدد **المصمم** لتحرير شريط الأوامر المحدد.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-148">On the **Button grids** FastTab, select **Designer** to edit the selected button grid.</span></span>
1. <span data-ttu-id="e2e6b-149">قم بإضافة لوحة **المهام** إلى القسم المناسب للصفحة الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-149">Add a **Tasks** tile to the appropriate section of the home page.</span></span>

<span data-ttu-id="e2e6b-150">يبين الرسم التوضيحي التالي مثالاً للوحة **المهام** في صفحة رئيسية لنقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-150">The following illustration shows an example of a **Tasks** tile on a POS home page.</span></span>

![لوحة المهام على الصفحة الرئيسية لنقطة البيع](media/POS-home-screen-tasks-button-image.png)

## <a name="additional-resources"></a><span data-ttu-id="e2e6b-152">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="e2e6b-152">Additional resources</span></span>

[<span data-ttu-id="e2e6b-153">نظرة عامة حول إدارة المهام</span><span class="sxs-lookup"><span data-stu-id="e2e6b-153">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="e2e6b-154">إنشاء قوائم مهام وإضافة مهام</span><span class="sxs-lookup"><span data-stu-id="e2e6b-154">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="e2e6b-155">تعيين قوائم المهام إلى المتاجر أو الموظفين</span><span class="sxs-lookup"><span data-stu-id="e2e6b-155">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="e2e6b-156">إدارة المهام في نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="e2e6b-156">Task management in POS</span></span>](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
