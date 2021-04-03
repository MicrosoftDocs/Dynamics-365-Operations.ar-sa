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
ms.openlocfilehash: 18ba781795058de6228c712c6a22e59038e96368
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478352"
---
# <a name="task-management-in-pos"></a><span data-ttu-id="69efe-103">إدارة المهام في نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="69efe-103">Task management in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="69efe-104">يصف هذا الموضوع إدارة المهام في تطبيق نقطة البيع (POS) لـ Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="69efe-104">This topic describes task management in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

<span data-ttu-id="69efe-105">يحتوي تطبيق نقطة البيع لـ Dynamics 365 Commerce على ميزات إداره المهام تتيح لمديري المتاجر والعاملين فيها القدرة على إدارة المهام وتحديث حاله المهام.</span><span class="sxs-lookup"><span data-stu-id="69efe-105">The Dynamics 365 Commerce POS application has task management features that let store managers and workers manage tasks and update task status.</span></span> <span data-ttu-id="69efe-106">يمكن للعاملين في المتجر الوصول للمهام إما بتحديد لوحة **المهام** على الصفحة الرئيسية لنقطة البيع أو عن طريق تحديد إعلامات المهام.</span><span class="sxs-lookup"><span data-stu-id="69efe-106">Store workers can access tasks either by selecting the **Tasks** tile on the POS home page or by selecting task notifications.</span></span> <span data-ttu-id="69efe-107">افتراضيًا، يتم نقل عمال المتجر إلى علامة التبويب **مهامي** حيث يمكنهم عرض المهام التي تم تعيينها لهم.</span><span class="sxs-lookup"><span data-stu-id="69efe-107">By default, store workers are taken to the **My tasks** tab, where they can view the tasks that are assigned to them.</span></span> <span data-ttu-id="69efe-108">ومع ذلك، يمكنهم التبديل بسهولة إلى علامات التبويب **مهام متأخرة** و **مهام متفوحة** و **قوائم المهام**.</span><span class="sxs-lookup"><span data-stu-id="69efe-108">However, they can easily switch to the **Overdue tasks**, **Open tasks**, and **Task lists** tabs.</span></span>

## <a name="task-operations-for-store-managers"></a><span data-ttu-id="69efe-109">عمليات المهام لمديري المتجر</span><span class="sxs-lookup"><span data-stu-id="69efe-109">Task operations for store managers</span></span>

<span data-ttu-id="69efe-110">يمكن لمديري المتاجر تنفيذ عمليات المهام التالية في تطبيق نقطه البيع باستخدام الأزرار الموجودة على شريط الأوامر:</span><span class="sxs-lookup"><span data-stu-id="69efe-110">Store managers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="69efe-111">**تعيين** - تعيين المهام المحددة لعامل متجر.</span><span class="sxs-lookup"><span data-stu-id="69efe-111">**Assign** – Assign selected tasks to a store worker.</span></span>
- <span data-ttu-id="69efe-112">**حاله المهمة** – تغيير حالة المهام المحددة.</span><span class="sxs-lookup"><span data-stu-id="69efe-112">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="69efe-113">**عامل التصفية** - افتراضيا، يتم عرض المهام النشطة فقط.</span><span class="sxs-lookup"><span data-stu-id="69efe-113">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="69efe-114">ومع ذلك، بتطبيق عوامل التصفية، يمكن للمديرين عرض كافة المهام، حتى المهام التي تم إكمالها أو إلغاؤها.</span><span class="sxs-lookup"><span data-stu-id="69efe-114">However, by applying filters, managers can view all tasks, even tasks that have been completed or canceled.</span></span>
- <span data-ttu-id="69efe-115">**مهمة جديدة** – قم بإنشاء مهمة ضمن قائمة مهام موجودة أو إنشاء مهمة ذات هدف مفرد.</span><span class="sxs-lookup"><span data-stu-id="69efe-115">**New task** – Create a task under an existing task list, or create an single-purpose task.</span></span>

<span data-ttu-id="69efe-116">يمكن لعمال المتاجر تنفيذ عمليات المهام التالية في تطبيق نقطه البيع باستخدام الأزرار الموجودة على شريط الأوامر:</span><span class="sxs-lookup"><span data-stu-id="69efe-116">Store workers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="69efe-117">**حاله المهمة** – تغيير حالة المهام المحددة.</span><span class="sxs-lookup"><span data-stu-id="69efe-117">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="69efe-118">**عامل التصفية** - افتراضيا، يتم عرض المهام النشطة فقط.</span><span class="sxs-lookup"><span data-stu-id="69efe-118">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="69efe-119">ومع ذلك، بتطبيق عوامل التصفية، يمكن للعمال عرض كافة المهام، حتى المهام التي تم إكمالها أو إلغاؤها.</span><span class="sxs-lookup"><span data-stu-id="69efe-119">However, by applying filters, workers can view all tasks, even tasks that have been completed or canceled.</span></span>

<span data-ttu-id="69efe-120">يوضح الرسم التوضيحي التالي علامة التبويب **مهامي** في تطبيق نقطة البيع لـ Commerce.</span><span class="sxs-lookup"><span data-stu-id="69efe-120">The following illustration shows the **My tasks** tab in the Commerce POS application.</span></span>

![علامة تبويب المهام في تطبيق نقطه البيع لـ Commerce](media/POS-task-management.png)

<span data-ttu-id="69efe-122">يبين الرسم التوضيحي التالي علامة التبويب **قوائم المهام**.</span><span class="sxs-lookup"><span data-stu-id="69efe-122">The following illustration shows the **Task lists** tab.</span></span>

![علامة تبويب قوائم المهام في تطبيق نقطه البيع لـ Commerce](media/POS-task-lists-management.png)

## <a name="additional-resources"></a><span data-ttu-id="69efe-124">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="69efe-124">Additional resources</span></span>

[<span data-ttu-id="69efe-125">نظرة عامة حول إدارة المهام</span><span class="sxs-lookup"><span data-stu-id="69efe-125">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="69efe-126">تكوين إدارة المهام</span><span class="sxs-lookup"><span data-stu-id="69efe-126">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="69efe-127">إنشاء قوائم مهام وإضافة مهام</span><span class="sxs-lookup"><span data-stu-id="69efe-127">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="69efe-128">تعيين قوائم المهام إلى المتاجر أو الموظفين</span><span class="sxs-lookup"><span data-stu-id="69efe-128">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
