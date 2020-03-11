---
title: تكوين وتشغيل وظيفة لترحيل البيانات
description: يتناول هذا الإجراء تكوين الوظيفة الدفعية المتكررة وتشغيلها لترحيل كشوف الحسابات لمتجر محدد أو مجموعة من المتاجر.
author: josaw1
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 09a47e268e271cf86e63ceff913435842f017bb5
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021455"
---
# <a name="configure-and-run-job-to-post-statements"></a><span data-ttu-id="b83fb-103">تكوين وتشغيل وظيفة لترحيل البيانات</span><span class="sxs-lookup"><span data-stu-id="b83fb-103">Configure and run job to post statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="b83fb-104">يتناول هذا الإجراء تكوين الوظيفة الدفعية المتكررة وتشغيلها لترحيل كشوف الحسابات لمتجر محدد أو مجموعة من المتاجر.</span><span class="sxs-lookup"><span data-stu-id="b83fb-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="b83fb-105">ويستخدم هذا الإجراء شركة USRT في بيانات العرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="b83fb-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="b83fb-106">انتقل إلى كل مساحات العمل > ..</span><span class="sxs-lookup"><span data-stu-id="b83fb-106">Go to All workspaces > ..</span></span> <span data-ttu-id="b83fb-107">> ماليات المتاجر.</span><span class="sxs-lookup"><span data-stu-id="b83fb-107">> Store financials.</span></span>
2. <span data-ttu-id="b83fb-108">انقر فوق "ترحيل الكشوف على دُفعات".</span><span class="sxs-lookup"><span data-stu-id="b83fb-108">Click Post statements in batch.</span></span>
    * <span data-ttu-id="b83fb-109">حدد تدرجًا هرميًا تنظيميًا ثم في شجرة عُقد المؤسسة‬، حدد عقدة أو مخزنًا فرديًا.</span><span class="sxs-lookup"><span data-stu-id="b83fb-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="b83fb-110">حدد عقدة إذا أردت إنشاء وظيفة دفعية لمجموعة من المتاجر.</span><span class="sxs-lookup"><span data-stu-id="b83fb-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="b83fb-111">انقر فوق السهم لإضافة التحديد الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="b83fb-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="b83fb-112">انقر فوق علامة التبويب "تشغيل في الخلفية". ![تشغيل في الخلفية](../dev-itpro/media/runbackground.png "تشغيل في الخلفية")</span><span class="sxs-lookup"><span data-stu-id="b83fb-112">Click the Run in the background tab. ![Run in the background](../dev-itpro/media/runbackground.png "Run in the background")</span></span> 
4. <span data-ttu-id="b83fb-113">حدد خانة الاختيار "معالجة الدُفعة" أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="b83fb-113">Check or uncheck the Batch processing checkbox.</span></span>
<span data-ttu-id="b83fb-114">![معالجة الدُفعات](../dev-itpro/media/batchprocessing.png "معالجة الدفعات والتكرار")</span><span class="sxs-lookup"><span data-stu-id="b83fb-114">![Batch Processing](../dev-itpro/media/batchprocessing.png "Batch Processing & Recurrance")</span></span> 
5. <span data-ttu-id="b83fb-115">انقر فوق "تكرار".</span><span class="sxs-lookup"><span data-stu-id="b83fb-115">Click Recurrence.</span></span>
6. <span data-ttu-id="b83fb-116">في الحقل "تاريخ البدء"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="b83fb-116">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="b83fb-117">في حقل "‏‫وقت البدء"، أدخل الوقت.</span><span class="sxs-lookup"><span data-stu-id="b83fb-117">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="b83fb-118">اختر ما إذا أردت إنهاء التكرار بعد عدد معين من عمليات التشغيل، في تاريخ محدد، أو أبدًا.</span><span class="sxs-lookup"><span data-stu-id="b83fb-118">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="b83fb-119">ثم اختر الخيارات المختلفة لتحديد عدد المرات التي تريد فيها تشغيل الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="b83fb-119">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="b83fb-120">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="b83fb-120">Click OK.</span></span>
9. <span data-ttu-id="b83fb-121">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="b83fb-121">Click OK.</span></span>
