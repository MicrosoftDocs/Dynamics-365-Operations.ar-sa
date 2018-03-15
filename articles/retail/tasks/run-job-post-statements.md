--- 
title: " تكوين وتشغيل وظيفة لترحيل كشوف الحساب"
description: "يتناول هذا الإجراء تكوين الوظيفة الدفعية المتكررة وتشغيلها لترحيل كشوف الحسابات لمتجر محدد أو مجموعة من المتاجر."
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
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: f3587fe70dc6a0d8330063db77e625040a53da98
ms.contentlocale: ar-sa
ms.lasthandoff: 02/07/2018

---
# <a name="configure-and-run-a-job-to-post-statements"></a><span data-ttu-id="2c7e4-103"> تكوين وتشغيل وظيفة لترحيل كشوف الحساب</span><span class="sxs-lookup"><span data-stu-id="2c7e4-103">Configure and run a job to post statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="2c7e4-104">يتناول هذا الإجراء تكوين الوظيفة الدفعية المتكررة وتشغيلها لترحيل كشوف الحسابات لمتجر محدد أو مجموعة من المتاجر.</span><span class="sxs-lookup"><span data-stu-id="2c7e4-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="2c7e4-105">ويستخدم هذا الإجراء شركة USRT في بيانات العرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="2c7e4-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="2c7e4-106">انتقل إلى كل مساحات العمل > ..</span><span class="sxs-lookup"><span data-stu-id="2c7e4-106">Go to All workspaces > ..</span></span> <span data-ttu-id="2c7e4-107">> ماليات متجر البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="2c7e4-107">> Retail store financials.</span></span>
2. <span data-ttu-id="2c7e4-108">انقر فوق ترحيل كشوف الحسابات.</span><span class="sxs-lookup"><span data-stu-id="2c7e4-108">Click Post statements.</span></span>
    * <span data-ttu-id="2c7e4-109">حدد تدرجًا هرميًا تنظيميًا ثم في شجرة عُقد المؤسسة‬، حدد عقدة أو مخزنًا فرديًا.</span><span class="sxs-lookup"><span data-stu-id="2c7e4-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="2c7e4-110">حدد عقدة إذا أردت إنشاء وظيفة دفعية لمجموعة من المتاجر.</span><span class="sxs-lookup"><span data-stu-id="2c7e4-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="2c7e4-111">انقر فوق السهم لإضافة التحديد الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="2c7e4-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="2c7e4-112">انقر فوق علامة التبويب "‏‫تشغيل في الخلفية".</span><span class="sxs-lookup"><span data-stu-id="2c7e4-112">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="2c7e4-113">حدد خانة الاختيار "معالجة الدُفعة" أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="2c7e4-113">Check or uncheck the Batch processing checkbox.</span></span>
5. <span data-ttu-id="2c7e4-114">انقر فوق "تكرار".</span><span class="sxs-lookup"><span data-stu-id="2c7e4-114">Click Recurrence.</span></span>
6. <span data-ttu-id="2c7e4-115">في الحقل "تاريخ البدء"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="2c7e4-115">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="2c7e4-116">في حقل "‏‫وقت البدء"، أدخل الوقت.</span><span class="sxs-lookup"><span data-stu-id="2c7e4-116">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="2c7e4-117">اختر ما إذا أردت إنهاء التكرار بعد عدد معين من عمليات التشغيل، في تاريخ محدد، أو أبدًا.</span><span class="sxs-lookup"><span data-stu-id="2c7e4-117">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="2c7e4-118">ثم اختر الخيارات المختلفة لتحديد عدد المرات التي تريد فيها تشغيل الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="2c7e4-118">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="2c7e4-119">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="2c7e4-119">Click OK.</span></span>
9. <span data-ttu-id="2c7e4-120">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="2c7e4-120">Click OK.</span></span>


