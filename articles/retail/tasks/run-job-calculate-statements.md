--- 
title: " تكوين وتشغيل وظيفة لحساب كشوف الحساب"
description: "يتناول هذا الإجراء تكوين الوظائف الدفعية المتكررة وتشغيلها لإنشاء وحساب كشوف الحسابات لمتجر محدد أو مجموعة من المتاجر."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6d98adc919d50957b92a879b69517e0a826ea45f
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---
# <a name="configure-and-run-a-job-to-calculate-statements"></a><span data-ttu-id="9df00-103"> تكوين وتشغيل وظيفة لحساب كشوف الحساب</span><span class="sxs-lookup"><span data-stu-id="9df00-103">Configure and run a job to calculate statements</span></span>

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="9df00-104">يتناول هذا الإجراء تكوين الوظائف الدفعية المتكررة وتشغيلها لإنشاء وحساب كشوف الحسابات لمتجر محدد أو مجموعة من المتاجر.</span><span class="sxs-lookup"><span data-stu-id="9df00-104">This procedure walks through configuring and running recurrent batch jobs to create and calculate statements for a selected store or group of stores.</span></span> <span data-ttu-id="9df00-105">ويستخدم هذا الإجراء شركة USRT في بيانات العرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="9df00-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="9df00-106">انتقل إلى كافة مساحات العمل > ماليات متجر البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="9df00-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="9df00-107">انقر فوق حساب كشوف الحسابات.</span><span class="sxs-lookup"><span data-stu-id="9df00-107">Click Calculate statements.</span></span>
    * <span data-ttu-id="9df00-108">حدد إما متجر معين أو عقدة إذا أردت إنشاء وظيفة دفعية لمجموعة من المتاجر.</span><span class="sxs-lookup"><span data-stu-id="9df00-108">Select either a specific store, or a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="9df00-109">انقر فوق السهم لإضافة التحديد الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="9df00-109">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="9df00-110">انقر فوق علامة التبويب "‏‫تشغيل في الخلفية".</span><span class="sxs-lookup"><span data-stu-id="9df00-110">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="9df00-111">ضمن معالجة الدُفعة، حدد "نعم".</span><span class="sxs-lookup"><span data-stu-id="9df00-111">Under Batch processing, select 'Yes'.</span></span>
5. <span data-ttu-id="9df00-112">انقر فوق "تكرار".</span><span class="sxs-lookup"><span data-stu-id="9df00-112">Click Recurrence.</span></span>
6. <span data-ttu-id="9df00-113">في الحقل "تاريخ البدء"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="9df00-113">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="9df00-114">في حقل "‏‫وقت البدء"، أدخل الوقت.</span><span class="sxs-lookup"><span data-stu-id="9df00-114">In the Start time field, enter a time.</span></span>
8. <span data-ttu-id="9df00-115">حدد الخيار "‏‫لا يوجد تاريخ انتهاء‬".</span><span class="sxs-lookup"><span data-stu-id="9df00-115">Select the No end date option.</span></span>
9. <span data-ttu-id="9df00-116">في حقل "PatternUnit‬‬"، أدخل "الأيام".</span><span class="sxs-lookup"><span data-stu-id="9df00-116">In the PatternUnit field, enter 'Days'.</span></span>
10. <span data-ttu-id="9df00-117">في الحقل "لكل‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="9df00-117">In the Per field, enter a number.</span></span>
11. <span data-ttu-id="9df00-118">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="9df00-118">Click OK.</span></span>
12. <span data-ttu-id="9df00-119">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="9df00-119">Click OK.</span></span>


