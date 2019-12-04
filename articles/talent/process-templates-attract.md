---
title: إنشاء قالب عملية تعيين في Attract
description: يوفر هذا الموضوع معلومات حول كيفية إنشاء قالب عملية تعيين في Attract.
author: andreabichsel
manager: AnnBe
ms.date: 10/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: AX 8.1
ms.openlocfilehash: 82046d43cf7366b760c140bdb8b017337b4f41da
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832548"
---
# <a name="create-a-hiring-process-template-in-attract"></a><span data-ttu-id="d79c6-103">إنشاء قالب عملية تعيين في Attract</span><span class="sxs-lookup"><span data-stu-id="d79c6-103">Create a hiring process template in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d79c6-104">يحتوي *قالب عملية التوظيف* على كافة الأنشطة التي ينبغي تضمينها كجزء من عملية توظيف لوظيفة ما.</span><span class="sxs-lookup"><span data-stu-id="d79c6-104">A *hiring process template* contains all the activities that should be included as part of the hiring process for a job.</span></span> <span data-ttu-id="d79c6-105">يصف هذا الموضوع عناصر قالب العملية في Dynamics 365 Talent: AttractMicrosoft.</span><span class="sxs-lookup"><span data-stu-id="d79c6-105">This topic describes the elements of a process template in Microsoft Dynamics 365 Talent: Attract.</span></span> <span data-ttu-id="d79c6-106">ويشرح أيضًا كيفية إنشاء قالب.</span><span class="sxs-lookup"><span data-stu-id="d79c6-106">It also explains how to create a template.</span></span>

> [!NOTE]
> <span data-ttu-id="d79c6-107">تعتبر عملية إنشاء قالب جزءًا من المكون الإضافي Comprehensive Hiring في Attract.</span><span class="sxs-lookup"><span data-stu-id="d79c6-107">Template creation is part of the Comprehensive Hiring Add-on for Attract.</span></span>

## <a name="template-management"></a><span data-ttu-id="d79c6-108">إدارة القوالب</span><span class="sxs-lookup"><span data-stu-id="d79c6-108">Template management</span></span>

<span data-ttu-id="d79c6-109">بإمكان لمؤسسات تحديد ما إذا كان باستطاعة أعضاء الفريق أو المسوؤلين فقط إنشاء قوالب العملية في Attract.</span><span class="sxs-lookup"><span data-stu-id="d79c6-109">Organizations can decide whether team members or only admins can create process templates in Attract.</span></span> <span data-ttu-id="d79c6-110">لتكوين إدارة القوالب، انتقل إلى **مركز الإدارة** \> **إدارة القوالب**.</span><span class="sxs-lookup"><span data-stu-id="d79c6-110">To configure template management, go to **Admin Center** \> **Template management**.</span></span> <span data-ttu-id="d79c6-111">للسماح لأعضاء الفريق بإنشاء قوالبهم الخاصة، قم بتشغيل إدارة القوالب.</span><span class="sxs-lookup"><span data-stu-id="d79c6-111">To let team members create their own templates, turn on template management.</span></span> <span data-ttu-id="d79c6-112">إذا لم تقم بتشغيل إدارة القوالب، فسيتمكن المسؤولون فقط من إنشاء القوالب.</span><span class="sxs-lookup"><span data-stu-id="d79c6-112">If you don't turn on template management, only admins can create templates.</span></span>

## <a name="default-template"></a><span data-ttu-id="d79c6-113">القالب الافتراضي</span><span class="sxs-lookup"><span data-stu-id="d79c6-113">Default template</span></span>

<span data-ttu-id="d79c6-114">وحدهم المسؤولون يمكنهم تعيين القالب الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="d79c6-114">Only admins can set the default template.</span></span> <span data-ttu-id="d79c6-115">ويُستخدم القالب الافتراضي إذا لم يتم تحديد قالب أثناء إنشاء وظيفة.</span><span class="sxs-lookup"><span data-stu-id="d79c6-115">The default template is used if a template isn't selected when a job is created.</span></span> <span data-ttu-id="d79c6-116">لتعيين القالب الافتراضي، انتقل إلى **مركز الإدارة** \> **إدارة القوالب**.</span><span class="sxs-lookup"><span data-stu-id="d79c6-116">To set the default template, go to **Admin Center** \> **Template management**.</span></span> <span data-ttu-id="d79c6-117">على بطاقة القالب الذي يجب أن يكون القالب الافتراضي، حدد زر علامة القطع (**...**)، ثم حدد **تعيين كافتراضي**.</span><span class="sxs-lookup"><span data-stu-id="d79c6-117">On the card for the template that should be the default template, select the ellipsis button (**...**), and then select **Set as default**.</span></span>

## <a name="create-a-process-template"></a><span data-ttu-id="d79c6-118">إنشاء قالب عملية</span><span class="sxs-lookup"><span data-stu-id="d79c6-118">Create a process template</span></span>

<span data-ttu-id="d79c6-119">بإمكان المسؤولين ومسؤولي التعيين ومدراء التوظيف إنشاء قوالب عمليات.</span><span class="sxs-lookup"><span data-stu-id="d79c6-119">Admins, recruiters, and hiring managers can create process templates.</span></span> <span data-ttu-id="d79c6-120">يتكوّن قالب العملية من *المراحل* و*الأنشطة*.</span><span class="sxs-lookup"><span data-stu-id="d79c6-120">A process template consists of *stages* and *activities*.</span></span> <span data-ttu-id="d79c6-121">بإمكان المراحل تجميع نشاط واحد أو أكث معًا.</span><span class="sxs-lookup"><span data-stu-id="d79c6-121">Stages group together one or more activities.</span></span> <span data-ttu-id="d79c6-122">بشكل افتراضي، يحتوي كل قالب عملية على أنشطة الموظف المتوقع واستمارة التقديم والعر.</span><span class="sxs-lookup"><span data-stu-id="d79c6-122">By default, every process template has Prospect, Application, and Offer activities.</span></span> <span data-ttu-id="d79c6-123">ويمكن إعادة تسمية المراحل التي تحتوي على هذه الأنشطة.</span><span class="sxs-lookup"><span data-stu-id="d79c6-123">The stages that contain these activities can be renamed.</span></span> <span data-ttu-id="d79c6-124">يمكنك إضافة المزيد من المراحل عن طريق تحديد **+ مرحلة جديدة**.</span><span class="sxs-lookup"><span data-stu-id="d79c6-124">You can add more stages by selecting **+ New Stage**.</span></span> <span data-ttu-id="d79c6-125">يمكنك إضافة الأنشطة إلى مرحلة أما عن طريق سحبها إلى المرحلة المناسبة أو بواسطة النقر المزدوج فوقها في قائمة الأنشطة.</span><span class="sxs-lookup"><span data-stu-id="d79c6-125">You can add activities to a stage either by dragging them to the appropriate stage or by double-clicking them in the activity list.</span></span>

> [!NOTE]
> <span data-ttu-id="d79c6-126">تظهر أسماء المراحل للمرشحين في صفحة **حالة استمارة التقديم**.</span><span class="sxs-lookup"><span data-stu-id="d79c6-126">Stage names are visible to candidates on the **Application status** page.</span></span> <span data-ttu-id="d79c6-127">يجب مراعاة هذا الواقع عندما تختار أسماء للمراحل.</span><span class="sxs-lookup"><span data-stu-id="d79c6-127">You should consider this fact when you choose names for stages.</span></span>

<span data-ttu-id="d79c6-128">لمزيد من المعلومات حول الأنشطة، راجع [الأنشطة في عمليات التوظيف](./activities-attract.md).</span><span class="sxs-lookup"><span data-stu-id="d79c6-128">To learn more about activities, see [Activities in hiring processes](./activities-attract.md).</span></span>

<span data-ttu-id="d79c6-129">اتبع هذه الخطوات لإنشاء قالب عملية التوظيف.</span><span class="sxs-lookup"><span data-stu-id="d79c6-129">Follow these steps to create a hiring process template.</span></span>

1. <span data-ttu-id="d79c6-130">انتقل إلى **القوالب**.</span><span class="sxs-lookup"><span data-stu-id="d79c6-130">Go to **Templates**.</span></span>
2. <span data-ttu-id="d79c6-131">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="d79c6-131">Select **New**.</span></span>
3. <span data-ttu-id="d79c6-132">في حقل **اسم القالب**، أدخل اسمًا للقالب، ثم حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="d79c6-132">In the **Template name** field, enter a name for the template, and then select **Create**.</span></span>
4. <span data-ttu-id="d79c6-133">في قائمة **اختيار عملية الموافقة**، حدد **افتراضي** لطلب الموافقة لوظيفة.</span><span class="sxs-lookup"><span data-stu-id="d79c6-133">In the **Choose the approval process** list, select **Default** to require approval for a job.</span></span>
5. <span data-ttu-id="d79c6-134">حدد لتمكين أو تعطيل الموظفين المتوقعين.</span><span class="sxs-lookup"><span data-stu-id="d79c6-134">Select to enable or disable prospects.</span></span>
6. <span data-ttu-id="d79c6-135">اختياري: إضافة أو إزالة المراحل.</span><span class="sxs-lookup"><span data-stu-id="d79c6-135">Optional: Add or remove stages.</span></span>

    - <span data-ttu-id="d79c6-136">لإضافة مرحلة، حدد **+ مرحلة جديدة**.</span><span class="sxs-lookup"><span data-stu-id="d79c6-136">To add a stage, select **+ New Stage**.</span></span>
    - <span data-ttu-id="d79c6-137">لإزالة مرحلة، قم بتمرير مؤشر الماوس فوقها، ثم حدد زر سلة المهملات الذي يظهر.</span><span class="sxs-lookup"><span data-stu-id="d79c6-137">To remove a stage, hover the pointer over the stage, and then select the trash can button that appears.</span></span>

        > [!NOTE]
        > <span data-ttu-id="d79c6-138">لا يمكن إزالة مراحل الموظف المتوقع واستمارة التقديم والعرض، ولكن يمكن إعادة تسميتها.</span><span class="sxs-lookup"><span data-stu-id="d79c6-138">Prospect, Application, and Offer stages can't be removed, but they can be renamed.</span></span>

7. <span data-ttu-id="d79c6-139">اختياري: إضافة أو إزالة الأنشطة.</span><span class="sxs-lookup"><span data-stu-id="d79c6-139">Optional: Add or remove activities.</span></span>

    - <span data-ttu-id="d79c6-140">لإضافة نشاط، اسحبه من قائمة الأنشطة على الجانب الأيسر إلى المرحلة المناسبة.</span><span class="sxs-lookup"><span data-stu-id="d79c6-140">To add an activity, drag it from the activity list on the right to the appropriate stage.</span></span> <span data-ttu-id="d79c6-141">أو انقر نقرًا مزدوجًا فوق النشاط، وحدد المرحلة لإضافته إليها.</span><span class="sxs-lookup"><span data-stu-id="d79c6-141">Alternatively, double-click the activity, and then select the stage to add it to.</span></span>
    - <span data-ttu-id="d79c6-142">لإزالة نشاط، قم بتوسيعه، ثم حدد زر سلة المهملات في رأس النشاط.</span><span class="sxs-lookup"><span data-stu-id="d79c6-142">To remove an activity, expand it, and then select the trash can button on the activity header.</span></span>

8. <span data-ttu-id="d79c6-143">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="d79c6-143">Select **Save**.</span></span>
