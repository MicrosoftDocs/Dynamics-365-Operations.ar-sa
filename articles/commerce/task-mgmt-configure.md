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
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 9a4775c2dba2b9aa8e671ab6c246000303b3a37e
ms.sourcegitcommit: 80cbb7d22267aa6a0ae0568d0063fb95556958a5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/11/2020
ms.locfileid: "3036845"
---
# <a name="configure-task-management"></a><span data-ttu-id="cb819-103">تكوين إدارة المهام</span><span class="sxs-lookup"><span data-stu-id="cb819-103">Configure task management</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cb819-104">يوضح هذا الموضوع كيفية تكوين ميزات إدارة المهام في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="cb819-104">This topic describes how to configure task management features in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="cb819-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="cb819-105">Overview</span></span>

<span data-ttu-id="cb819-106">قبل أن يتمكن مديرو وموظفو Dynamics 365 Commerce من استخدام ميزات إدارة المهام في Commerce، يجب أولاً تكوين إدارة المهام.</span><span class="sxs-lookup"><span data-stu-id="cb819-106">Before Dynamics 365 Commerce managers and employees can use the task management features in Commerce, task management must be configured.</span></span> <span data-ttu-id="cb819-107">وتشمل خطوات التكوين منح الأذونات للمديرين والموظفين، وتوزيع الأذونات على عملاء نقطة البيع (POS) وإعداد إعلامات نقطة البيع، وتكوين لوحة **المهام** على الصفحة الرئيسية لتطبيق نقطه البيع.</span><span class="sxs-lookup"><span data-stu-id="cb819-107">Configuration steps include granting permissions to managers and employees, distributing permissions to point of sale (POS) clients, setting up POS notifications, and configuring the **Tasks** tile on the home page of a POS application.</span></span>

## <a name="configure-permissions-for-store-managers"></a><span data-ttu-id="cb819-108">تكوين أذونات لمديري المتاجر</span><span class="sxs-lookup"><span data-stu-id="cb819-108">Configure permissions for store managers</span></span>

<span data-ttu-id="cb819-109">يمكن لكل العاملين في أي متجر عرض كافة المهام التي تم تعيينها لهذا المتجر.</span><span class="sxs-lookup"><span data-stu-id="cb819-109">Every worker in a given store can view all tasks that are assigned to that store.</span></span> <span data-ttu-id="cb819-110">كما يمكنهم أيضا تحديث حالة المهام التي تم تعيينها لهم.</span><span class="sxs-lookup"><span data-stu-id="cb819-110">They can also update the status of the tasks that are assigned to them.</span></span> <span data-ttu-id="cb819-111">ومع ذلك، يجب أن يتوفر لشخصيات مثل مديري المتجر أذونات إدارة المهام لإدارة المهام التي تم تعيينها إلى المتجر ولإنشاء مهام ذات غرض واحد.</span><span class="sxs-lookup"><span data-stu-id="cb819-111">However, personas such as store managers must have task management permissions to manage tasks that are assigned to the store and to create single-purpose tasks.</span></span>

<span data-ttu-id="cb819-112">لتكوين أذونات إدارة المهام لمديري المتجر، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="cb819-112">To configure task management permissions for store managers, follow these steps.</span></span>

1. <span data-ttu-id="cb819-113">انتقل إلى **Retail and Commerce \> الموظفون \> ‏‫مجموعات الأذونات‬**.</span><span class="sxs-lookup"><span data-stu-id="cb819-113">Go to **Retail and Commerce \> Employees \> Permission groups**.</span></span>
1. <span data-ttu-id="cb819-114">حدد مجموعة أذونات معينة (على سبيل المثال **المدير**) ثم حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="cb819-114">Select a specific permission group (for example, **Manager**), and then select **Edit**.</span></span>
1. <span data-ttu-id="cb819-115">في علامة التبويب السرعية **الأذونات** قم بتعيين خيار **السماح بإدارة المهام** إلى **نعم.**</span><span class="sxs-lookup"><span data-stu-id="cb819-115">On the **Permissions** FastTab, set the **Allow task management** option to **Yes**.</span></span>
1. <span data-ttu-id="cb819-116">على علامة التبويب السريعة **الإخطارات** قم بإضافة عملية **إدارة المهام** ، وأدخل قيمة في حقل **ترتيب العرض**.</span><span class="sxs-lookup"><span data-stu-id="cb819-116">On the **Notifications** FastTab, add the **Task management** operation, and enter a value in the **Display order** field.</span></span> <span data-ttu-id="cb819-117">على سبيل المثال، أدخل **2** إذا كانت قيمة العميلة **‏‫تنفيذ الأمر‬** لـ **ترتيب العرض** هي **1** بالفعل.</span><span class="sxs-lookup"><span data-stu-id="cb819-117">For example, enter **2** if the **Order fulfillment** operation already has a **Display order** value of **1**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="cb819-118">إذا كان يجب أن يتوفر للشخصيات الأخرى بخلاف المديرين أذونات إدارة المهام في نقطة البيع، فيمكنك منح الإذن للفرد.</span><span class="sxs-lookup"><span data-stu-id="cb819-118">If a non-manager persona must have task management permissions in the POS, you can grant permission to the individual.</span></span> <span data-ttu-id="cb819-119">أو، يمكنك إنشاء مجموعة أذونات جديده لغير المديرين وتعيين الخيار **السماح بإدارة المهام** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="cb819-119">Alternatively, you can create a new permission group for non-managers and set the **Allow task management** option to **Yes**.</span></span>

<span data-ttu-id="cb819-120">يبين الرسم التوضيحي التالي كيفية تكوين أذونات إدارة المهام لمديري المتجر.</span><span class="sxs-lookup"><span data-stu-id="cb819-120">The following illustration shows how to configure task management permissions for store managers.</span></span>

![تكوين أذونات إدارة المهام لمديري المتجر](media/HQ-POS-Tasks-Notifications-User-Permission.png)

## <a name="configure-permissions-for-employees"></a><span data-ttu-id="cb819-122">تكوين الأذونات للموظفين</span><span class="sxs-lookup"><span data-stu-id="cb819-122">Configure permissions for employees</span></span>

<span data-ttu-id="cb819-123">يجب أن يتوفر لدى الموظفين أذونات لإنشاء قوائم مهام، وإدارة معايير التعيين، وتكوين تكرار أي قائمة مهام.</span><span class="sxs-lookup"><span data-stu-id="cb819-123">Employees must have permissions to create task lists, manage assignment criteria, and configure the recurrence of any task list.</span></span> <span data-ttu-id="cb819-124">لتكوين هذه الأذونات، قم بتعيين الموظفين على دور **مدير مهمة البيع بالتجزئة**.</span><span class="sxs-lookup"><span data-stu-id="cb819-124">To configure these permissions, you assign employees to the **Retail task manager** role.</span></span>

<span data-ttu-id="cb819-125">لتكوين الأذونات لموظف، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="cb819-125">To configure permissions for an employee, follow these steps.</span></span>

1. <span data-ttu-id="cb819-126">انتقل إلى **Retail and Commerce \> الموظفون \> المستخدمون**.</span><span class="sxs-lookup"><span data-stu-id="cb819-126">Go to **Retail and Commerce \> Employees \> Users**.</span></span>
1. <span data-ttu-id="cb819-127">حدد موظفًا.</span><span class="sxs-lookup"><span data-stu-id="cb819-127">Select an employee.</span></span>
1. <span data-ttu-id="cb819-128">في علامة التبويب السريعة، **أدوار المستخدم** حدد **تعيين‏‎ الأدوار**.</span><span class="sxs-lookup"><span data-stu-id="cb819-128">On the **User's roles** FastTab, select **Assign roles**.</span></span>
1. <span data-ttu-id="cb819-129">في مربع الحوار **تعيين أدوار للمستخدم** حدد دور **مدير مهمة البيع بالتجزئة** ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="cb819-129">In the **Assign roles to user** dialog box, select the **Retail task manager** role, and then select **OK**.</span></span>

## <a name="distribute-permissions-to-pos-clients"></a><span data-ttu-id="cb819-130">توزيع الأذونات على عملاء نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="cb819-130">Distribute permissions to POS clients</span></span>

<span data-ttu-id="cb819-131">قبل أن يتمكن الموظفون من استخدام عملاء نقطة البيع ، يجب توزيع الأذونات ومزامنتها مع هؤلاء العملاء.</span><span class="sxs-lookup"><span data-stu-id="cb819-131">Before employees can use POS clients, permissions must be distributed and synced to those clients.</span></span>

<span data-ttu-id="cb819-132">لتوزيع الأذونات على عملاء نقطة البيع ، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="cb819-132">To distribute permissions to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="cb819-133">انتقل إلى **البيع بالتجزئة والتجارة \> تكنولوجيا معلومات البيع بالتجزئة والتجارة \> جدول التوزيع**.</span><span class="sxs-lookup"><span data-stu-id="cb819-133">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="cb819-134">حدد جدول توزيع **1060** (**الفريق‬**) ثم حدد **تشغيل الآن**.</span><span class="sxs-lookup"><span data-stu-id="cb819-134">Select the **1060** (**Staff**) distribution schedule, and then select **Run now**.</span></span>
1. <span data-ttu-id="cb819-135">حدد جدول توزيع **1070** (**تكوين القناة**) ثم حدد **تشغيل الآن**.</span><span class="sxs-lookup"><span data-stu-id="cb819-135">Select the **1070** (**Channel configuration**) distribution schedule, and then select **Run now**.</span></span>

## <a name="configure-pos-notifications-for-tasks"></a><span data-ttu-id="cb819-136">تكوين إخطارات نقطة البيع للمهام</span><span class="sxs-lookup"><span data-stu-id="cb819-136">Configure POS notifications for tasks</span></span>

<span data-ttu-id="cb819-137">يجب تكوين إداره المهام بحيث تتوفر الإخطارات في تطبيق نقطه البيع.</span><span class="sxs-lookup"><span data-stu-id="cb819-137">Task management must be configured so that notifications are available in the POS application.</span></span>

<span data-ttu-id="cb819-138">لتكوين إخطارات نقطة البيع للمهام اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="cb819-138">To configure POS notifications for tasks, follow these steps.</span></span>

1. <span data-ttu-id="cb819-139">انتقل إلى **Retail and Commerce \> إعداد القناة \> إعداد نقطة البيع \> نقطة البيع \> عمليات نقطة البيع**.</span><span class="sxs-lookup"><span data-stu-id="cb819-139">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="cb819-140">ابحث عن العملية **1400** (**إدارة المهام**) ، وحدد خانة الاختيار **تمكين الإخطارات** لها.</span><span class="sxs-lookup"><span data-stu-id="cb819-140">Find operation **1400** (**Task management**), and select the **Enable notifications** check box for it.</span></span>

<span data-ttu-id="cb819-141">يبين الرسم التوضيحي التالية عملية **إدارة المهام** في صفحة **عمليات نقطة البيع**.</span><span class="sxs-lookup"><span data-stu-id="cb819-141">The following illustration shows the **Task management** operation on the **POS operations** page.</span></span>

![عمليه إدارة المهام في صفحة عمليات POS](media/HQ-POS-Tasks-Notifications.png)

<span data-ttu-id="cb819-143">لمزيد من المعلومات حول كيفية تكوين إخطارات نقاط البيع، راجع [‏‫إظهار إخطارات الأوامر في نقطة البيع (POS)](notifications-pos.md).</span><span class="sxs-lookup"><span data-stu-id="cb819-143">For more information about how to configure POS notifications, see [Show order notifications in the point of sale (POS)](notifications-pos.md).</span></span>

## <a name="configure-the-tasks-tile-on-a-pos-application-home-page"></a><span data-ttu-id="cb819-144">تكوين لوحة المهام على الصفحة الرئيسية لتطبيق نقطه البيع</span><span class="sxs-lookup"><span data-stu-id="cb819-144">Configure the Tasks tile on a POS application home page</span></span>

<span data-ttu-id="cb819-145">قبل تكوين لوحة **المهام** على الصفحة الرئيسية لتطبيق نقطه البيع، راجع [تخطيطات الشاشة الخاصة بنقطة البيع (POS)‬](pos-screen-layouts.md) للحصول على معلومات حول كيفية تكوين الأزرار الجديدة وإضافتها إلى تخطيط شاشة نقطة البيع (POS).</span><span class="sxs-lookup"><span data-stu-id="cb819-145">Before you configure the **Tasks** tile on the home page of a POS application, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information about how to configure and add new buttons to a POS screen layout.</span></span>

<span data-ttu-id="cb819-146">لتكوين لوحة **المهام** على الصفحة الرئيسية لتطبيق نقطه البيع، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="cb819-146">To configure the **Tasks** tile on a POS application home page, follow these steps.</span></span>

1. <span data-ttu-id="cb819-147">انتقل إلى **Retail and Commerce \> إعداد القناة \> إعداد نقطة البيع \> نقطة البيع \> تخطيطات الشاشة**.</span><span class="sxs-lookup"><span data-stu-id="cb819-147">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> Screen layouts**.</span></span>
1. <span data-ttu-id="cb819-148">حدد تخطيط شاشة وحدد حجم التخطيط ، ثم حدد شريط أوامر.</span><span class="sxs-lookup"><span data-stu-id="cb819-148">Select a screen layout, select a layout size, and select a button grid.</span></span>
1. <span data-ttu-id="cb819-149">على علامة التبويب السريعة **‏‫أشرطة الأوامر‬** حدد **المصمم** لتحرير شريط الأوامر المحدد.</span><span class="sxs-lookup"><span data-stu-id="cb819-149">On the **Button grids** FastTab, select **Designer** to edit the selected button grid.</span></span>
1. <span data-ttu-id="cb819-150">قم بإضافة لوحة **المهام** إلى القسم المناسب للصفحة الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="cb819-150">Add a **Tasks** tile to the appropriate section of the home page.</span></span>

<span data-ttu-id="cb819-151">يبين الرسم التوضيحي التالي مثالاً للوحة **المهام** في صفحة رئيسية لنقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="cb819-151">The following illustration shows an example of a **Tasks** tile on a POS home page.</span></span>

![لوحة المهام على الصفحة الرئيسية لنقطة البيع](media/POS-home-screen-tasks-button-image.png)

## <a name="additional-resources"></a><span data-ttu-id="cb819-153">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="cb819-153">Additional resources</span></span>

[<span data-ttu-id="cb819-154">نظرة عامة حول إدارة المهام</span><span class="sxs-lookup"><span data-stu-id="cb819-154">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="cb819-155">إنشاء قوائم مهام وإضافة مهام</span><span class="sxs-lookup"><span data-stu-id="cb819-155">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="cb819-156">تعيين قوائم المهام إلى المتاجر أو الموظفين</span><span class="sxs-lookup"><span data-stu-id="cb819-156">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="cb819-157">إدارة المهام في نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="cb819-157">Task management in POS</span></span>](task-mgmt-POS.md)
