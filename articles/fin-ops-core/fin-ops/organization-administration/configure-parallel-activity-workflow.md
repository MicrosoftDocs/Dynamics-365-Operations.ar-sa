---
title: تكوين أنشطة موازية في سير عمل
description: لتكوين نشاط موازٍ، أكمل الإجراءات التالية في محرر سير العمل.
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8043e2854ccc8db0128969ffe36a5517a12c37ac
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693344"
---
# <a name="configure-parallel-activities-in-a-workflow"></a><span data-ttu-id="df3a3-103">تكوين أنشطة موازية في سير عمل</span><span class="sxs-lookup"><span data-stu-id="df3a3-103">Configure parallel activities in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="df3a3-104">لتكوين نشاط موازٍ، أكمل الإجراءات التالية في محرر سير العمل.</span><span class="sxs-lookup"><span data-stu-id="df3a3-104">To configure a parallel activity, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="df3a3-105">يتكون النشاط الموازي من فروع سير العمل التي يتم تشغيلها في نفس الوقت.</span><span class="sxs-lookup"><span data-stu-id="df3a3-105">A parallel activity consists of workflow branches that run at the same time.</span></span>

## <a name="name-a-parallel-activity"></a><span data-ttu-id="df3a3-106">تسمية نشاط موازٍ</span><span class="sxs-lookup"><span data-stu-id="df3a3-106">Name a parallel activity</span></span>

<span data-ttu-id="df3a3-107">اتبع الخطوات التالية لإدخال اسم للنشاط الموازي.</span><span class="sxs-lookup"><span data-stu-id="df3a3-107">Follow these steps to enter a name for a parallel activity.</span></span>

1. <span data-ttu-id="df3a3-108">انقر بالزر الأيمن فوق النشاط الموازي، ثم انقر فوق **خصائص** لفتح النموذج **خصائص**.</span><span class="sxs-lookup"><span data-stu-id="df3a3-108">Right-click the parallel activity, and then click **Properties** to open the **Properties** form.</span></span>
2. <span data-ttu-id="df3a3-109">في الجزء الأيمن، انقر فوق **الإعدادات الأساسية‬**.</span><span class="sxs-lookup"><span data-stu-id="df3a3-109">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="df3a3-110">في حقل **الاسم**، أدخل اسمًا فريدًا للنشاط الموازي.</span><span class="sxs-lookup"><span data-stu-id="df3a3-110">In the **Name** field, enter a unique name for the parallel activity.</span></span>
4. <span data-ttu-id="df3a3-111">انقر فوق **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="df3a3-111">Click **Close**.</span></span>

## <a name="configure-the-branches-of-a-parallel-activity"></a><span data-ttu-id="df3a3-112">تكوين فروع النشاط الموازي</span><span class="sxs-lookup"><span data-stu-id="df3a3-112">Configure the branches of a parallel activity</span></span>

<span data-ttu-id="df3a3-113">اتبع هذه الخطوات لإضافة وتكوين فروع هذا النشاط الموازي.</span><span class="sxs-lookup"><span data-stu-id="df3a3-113">Follow these steps to add and configure the branches of this parallel activity.</span></span>

1. <span data-ttu-id="df3a3-114">انقر نقرًا مزدوجًا فوق النشاط الموازي لعرض فروع النشاط الموازي.</span><span class="sxs-lookup"><span data-stu-id="df3a3-114">Double-click the parallel activity to display the branches of the parallel activity.</span></span>
2. <span data-ttu-id="df3a3-115">لإضافة فرع، اسحب عنصر **الفرع** من ناحية **عناصر سير العمل** إلى نقطة إدراج على لوحة الرسم.</span><span class="sxs-lookup"><span data-stu-id="df3a3-115">To add a branch, drag the **Branch** element from the **Workflow elements** area to an insertion point on the canvas.</span></span> <span data-ttu-id="df3a3-116">يظهر الرسم التوضيحي التالي نقطة إدراج.</span><span class="sxs-lookup"><span data-stu-id="df3a3-116">The following figure shows an insertion point.</span></span>

    ![نقطة الإدراج](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > <span data-ttu-id="df3a3-118">ليس لترتيب الفروع أي أهمية لأن جميع فروع النشاط الموازي تعمل في الوقت نفسه.</span><span class="sxs-lookup"><span data-stu-id="df3a3-118">The order of the branches is not important because all the branches of a parallel activity run at the same time.</span></span>

3. <span data-ttu-id="df3a3-119">لتكوين كل فرع، راجع [تكوين أفرع موازية في سير عمل](configure-parallel-branch-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="df3a3-119">To configure each branch, see [Configure parallel branches in a workflow](configure-parallel-branch-workflow.md).</span></span>
