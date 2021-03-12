---
title: إدارة المهام في نقطة البيع
description: يصف هذا الموضوع إدارة المهام في تطبيق نقطة البيع (POS) لـ Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 889cc90b534de33ccd0e2bea367b2da42b5d72e0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006175"
---
# <a name="task-management-in-pos"></a><span data-ttu-id="4e658-103">إدارة المهام في نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="4e658-103">Task management in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4e658-104">يصف هذا الموضوع إدارة المهام في تطبيق نقطة البيع (POS) لـ Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4e658-104">This topic describes task management in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

## <a name="overview"></a><span data-ttu-id="4e658-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="4e658-105">Overview</span></span>

<span data-ttu-id="4e658-106">يحتوي تطبيق نقطة البيع لـ Dynamics 365 Commerce على ميزات إداره المهام تتيح لمديري المتاجر والعاملين فيها القدرة على إدارة المهام وتحديث حاله المهام.</span><span class="sxs-lookup"><span data-stu-id="4e658-106">The Dynamics 365 Commerce POS application has task management features that let store managers and workers manage tasks and update task status.</span></span> <span data-ttu-id="4e658-107">يمكن للعاملين في المتجر الوصول للمهام إما بتحديد لوحة **المهام** على الصفحة الرئيسية لنقطة البيع أو عن طريق تحديد إعلامات المهام.</span><span class="sxs-lookup"><span data-stu-id="4e658-107">Store workers can access tasks either by selecting the **Tasks** tile on the POS home page or by selecting task notifications.</span></span> <span data-ttu-id="4e658-108">افتراضيًا، يتم نقل عمال المتجر إلى علامة التبويب **مهامي** حيث يمكنهم عرض المهام التي تم تعيينها لهم.</span><span class="sxs-lookup"><span data-stu-id="4e658-108">By default, store workers are taken to the **My tasks** tab, where they can view the tasks that are assigned to them.</span></span> <span data-ttu-id="4e658-109">ومع ذلك، يمكنهم التبديل بسهولة إلى علامات التبويب **مهام متأخرة** و **مهام متفوحة** و **قوائم المهام**.</span><span class="sxs-lookup"><span data-stu-id="4e658-109">However, they can easily switch to the **Overdue tasks**, **Open tasks**, and **Task lists** tabs.</span></span>

## <a name="task-operations-for-store-managers"></a><span data-ttu-id="4e658-110">عمليات المهام لمديري المتجر</span><span class="sxs-lookup"><span data-stu-id="4e658-110">Task operations for store managers</span></span>

<span data-ttu-id="4e658-111">يمكن لمديري المتاجر تنفيذ عمليات المهام التالية في تطبيق نقطه البيع باستخدام الأزرار الموجودة على شريط الأوامر:</span><span class="sxs-lookup"><span data-stu-id="4e658-111">Store managers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="4e658-112">**تعيين** - تعيين المهام المحددة لعامل متجر.</span><span class="sxs-lookup"><span data-stu-id="4e658-112">**Assign** – Assign selected tasks to a store worker.</span></span>
- <span data-ttu-id="4e658-113">**حاله المهمة** – تغيير حالة المهام المحددة.</span><span class="sxs-lookup"><span data-stu-id="4e658-113">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="4e658-114">**عامل التصفية** - افتراضيا، يتم عرض المهام النشطة فقط.</span><span class="sxs-lookup"><span data-stu-id="4e658-114">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="4e658-115">ومع ذلك، بتطبيق عوامل التصفية، يمكن للمديرين عرض كافة المهام، حتى المهام التي تم إكمالها أو إلغاؤها.</span><span class="sxs-lookup"><span data-stu-id="4e658-115">However, by applying filters, managers can view all tasks, even tasks that have been completed or canceled.</span></span>
- <span data-ttu-id="4e658-116">**مهمة جديدة** – قم بإنشاء مهمة ضمن قائمة مهام موجودة أو إنشاء مهمة ذات هدف مفرد.</span><span class="sxs-lookup"><span data-stu-id="4e658-116">**New task** – Create a task under an existing task list, or create an single-purpose task.</span></span>

<span data-ttu-id="4e658-117">يمكن لعمال المتاجر تنفيذ عمليات المهام التالية في تطبيق نقطه البيع باستخدام الأزرار الموجودة على شريط الأوامر:</span><span class="sxs-lookup"><span data-stu-id="4e658-117">Store workers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="4e658-118">**حاله المهمة** – تغيير حالة المهام المحددة.</span><span class="sxs-lookup"><span data-stu-id="4e658-118">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="4e658-119">**عامل التصفية** - افتراضيا، يتم عرض المهام النشطة فقط.</span><span class="sxs-lookup"><span data-stu-id="4e658-119">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="4e658-120">ومع ذلك، بتطبيق عوامل التصفية، يمكن للعمال عرض كافة المهام، حتى المهام التي تم إكمالها أو إلغاؤها.</span><span class="sxs-lookup"><span data-stu-id="4e658-120">However, by applying filters, workers can view all tasks, even tasks that have been completed or canceled.</span></span>

<span data-ttu-id="4e658-121">يوضح الرسم التوضيحي التالي علامة التبويب **مهامي** في تطبيق نقطة البيع لـ Commerce.</span><span class="sxs-lookup"><span data-stu-id="4e658-121">The following illustration shows the **My tasks** tab in the Commerce POS application.</span></span>

![علامة تبويب المهام في تطبيق نقطه البيع لـ Commerce](media/POS-task-management.png)

<span data-ttu-id="4e658-123">يبين الرسم التوضيحي التالي علامة التبويب **قوائم المهام**.</span><span class="sxs-lookup"><span data-stu-id="4e658-123">The following illustration shows the **Task lists** tab.</span></span>

![علامة تبويب قوائم المهام في تطبيق نقطه البيع لـ Commerce](media/POS-task-lists-management.png)

## <a name="additional-resources"></a><span data-ttu-id="4e658-125">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="4e658-125">Additional resources</span></span>

[<span data-ttu-id="4e658-126">نظرة عامة حول إدارة المهام</span><span class="sxs-lookup"><span data-stu-id="4e658-126">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="4e658-127">تكوين إدارة المهام</span><span class="sxs-lookup"><span data-stu-id="4e658-127">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="4e658-128">إنشاء قوائم مهام وإضافة مهام</span><span class="sxs-lookup"><span data-stu-id="4e658-128">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="4e658-129">تعيين قوائم المهام إلى المتاجر أو الموظفين</span><span class="sxs-lookup"><span data-stu-id="4e658-129">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)
