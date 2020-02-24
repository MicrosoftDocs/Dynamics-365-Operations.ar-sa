---
title: تكوين وتشغيل وظيفة لحساب البيانات
description: يتناول هذا الإجراء تكوين الوظائف الدفعية المتكررة وتشغيلها لإنشاء وحساب كشوف الحسابات لمتجر محدد أو مجموعة من المتاجر.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 52798303ef5d96a44270f971703928d0c6c4c2c1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021459"
---
# <a name="configure-and-run-job-to-calculate-statements"></a><span data-ttu-id="35ca1-103">تكوين وتشغيل وظيفة لحساب البيانات</span><span class="sxs-lookup"><span data-stu-id="35ca1-103">Configure and run job to calculate statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="35ca1-104">يتناول هذا الإجراء تكوين الوظائف الدفعية المتكررة وتشغيلها لإنشاء وحساب كشوف الحسابات لمتجر محدد أو مجموعة من المتاجر.</span><span class="sxs-lookup"><span data-stu-id="35ca1-104">This procedure walks through configuring and running recurrent batch jobs to create and calculate statements for a selected store or group of stores.</span></span> <span data-ttu-id="35ca1-105">ويستخدم هذا الإجراء شركة USRT في بيانات العرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="35ca1-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="35ca1-106">انتقل إلى كافة مساحات العمل > ماليات المتاجر.</span><span class="sxs-lookup"><span data-stu-id="35ca1-106">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="35ca1-107">انقر فوق حساب كشوف الحسابات.</span><span class="sxs-lookup"><span data-stu-id="35ca1-107">Click Calculate statements.</span></span>
    * <span data-ttu-id="35ca1-108">حدد إما متجر معين أو عقدة إذا أردت إنشاء وظيفة دفعية لمجموعة من المتاجر.</span><span class="sxs-lookup"><span data-stu-id="35ca1-108">Select either a specific store, or a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="35ca1-109">انقر فوق السهم لإضافة التحديد الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="35ca1-109">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="35ca1-110">انقر فوق علامة التبويب "‏‫تشغيل في الخلفية".</span><span class="sxs-lookup"><span data-stu-id="35ca1-110">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="35ca1-111">ضمن معالجة الدُفعة، حدد "نعم".</span><span class="sxs-lookup"><span data-stu-id="35ca1-111">Under Batch processing, select 'Yes'.</span></span>
5. <span data-ttu-id="35ca1-112">انقر فوق "تكرار".</span><span class="sxs-lookup"><span data-stu-id="35ca1-112">Click Recurrence.</span></span>
6. <span data-ttu-id="35ca1-113">في الحقل "تاريخ البدء"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="35ca1-113">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="35ca1-114">في حقل "‏‫وقت البدء"، أدخل الوقت.</span><span class="sxs-lookup"><span data-stu-id="35ca1-114">In the Start time field, enter a time.</span></span>
8. <span data-ttu-id="35ca1-115">حدد الخيار "‏‫لا يوجد تاريخ انتهاء‬".</span><span class="sxs-lookup"><span data-stu-id="35ca1-115">Select the No end date option.</span></span>
9. <span data-ttu-id="35ca1-116">في حقل "PatternUnit‬‬"، أدخل "الأيام".</span><span class="sxs-lookup"><span data-stu-id="35ca1-116">In the PatternUnit field, enter 'Days'.</span></span>
10. <span data-ttu-id="35ca1-117">في الحقل "لكل‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="35ca1-117">In the Per field, enter a number.</span></span>
11. <span data-ttu-id="35ca1-118">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="35ca1-118">Click OK.</span></span>
12. <span data-ttu-id="35ca1-119">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="35ca1-119">Click OK.</span></span>

