--- 
title: "تكوين وتشغيل وظيفة لحساب البيانات"
description: "يتناول هذا الإجراء تكوين الوظائف الدفعية المتكررة وتشغيلها لإنشاء وحساب كشوف الحسابات لمتجر محدد أو مجموعة من المتاجر."
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: f52603672e95d0ae4973844851c4ed260484e5f0
ms.contentlocale: ar-sa
ms.lasthandoff: 09/14/2018

---
# <a name="configure-and-run-job-to-calculate-statements"></a><span data-ttu-id="1d1c6-103">تكوين وتشغيل وظيفة لحساب البيانات</span><span class="sxs-lookup"><span data-stu-id="1d1c6-103">Configure and run job to calculate statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="1d1c6-104">يتناول هذا الإجراء تكوين الوظائف الدفعية المتكررة وتشغيلها لإنشاء وحساب كشوف الحسابات لمتجر محدد أو مجموعة من المتاجر.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-104">This procedure walks through configuring and running recurrent batch jobs to create and calculate statements for a selected store or group of stores.</span></span> <span data-ttu-id="1d1c6-105">ويستخدم هذا الإجراء شركة USRT في بيانات العرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="1d1c6-106">انتقل إلى كافة مساحات العمل > ماليات متجر البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="1d1c6-107">انقر فوق حساب كشوف الحسابات.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-107">Click Calculate statements.</span></span>
    * <span data-ttu-id="1d1c6-108">حدد إما متجر معين أو عقدة إذا أردت إنشاء وظيفة دفعية لمجموعة من المتاجر.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-108">Select either a specific store, or a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="1d1c6-109">انقر فوق السهم لإضافة التحديد الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-109">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="1d1c6-110">انقر فوق علامة التبويب "‏‫تشغيل في الخلفية".</span><span class="sxs-lookup"><span data-stu-id="1d1c6-110">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="1d1c6-111">ضمن معالجة الدُفعة، حدد "نعم".</span><span class="sxs-lookup"><span data-stu-id="1d1c6-111">Under Batch processing, select 'Yes'.</span></span>
5. <span data-ttu-id="1d1c6-112">انقر فوق "تكرار".</span><span class="sxs-lookup"><span data-stu-id="1d1c6-112">Click Recurrence.</span></span>
6. <span data-ttu-id="1d1c6-113">في الحقل "تاريخ البدء"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-113">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="1d1c6-114">في حقل "‏‫وقت البدء"، أدخل الوقت.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-114">In the Start time field, enter a time.</span></span>
8. <span data-ttu-id="1d1c6-115">حدد الخيار "‏‫لا يوجد تاريخ انتهاء‬".</span><span class="sxs-lookup"><span data-stu-id="1d1c6-115">Select the No end date option.</span></span>
9. <span data-ttu-id="1d1c6-116">في حقل "PatternUnit‬‬"، أدخل "الأيام".</span><span class="sxs-lookup"><span data-stu-id="1d1c6-116">In the PatternUnit field, enter 'Days'.</span></span>
10. <span data-ttu-id="1d1c6-117">في الحقل "لكل‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-117">In the Per field, enter a number.</span></span>
11. <span data-ttu-id="1d1c6-118">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="1d1c6-118">Click OK.</span></span>
12. <span data-ttu-id="1d1c6-119">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="1d1c6-119">Click OK.</span></span>


