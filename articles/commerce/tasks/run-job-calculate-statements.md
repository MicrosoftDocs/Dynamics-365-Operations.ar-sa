---
title: تكوين وتشغيل وظيفة لحساب البيانات
description: يتناول هذا الإجراء تكوين الوظائف الدفعية المتكررة وتشغيلها لإنشاء وحساب كشوف الحسابات لمتجر محدد أو مجموعة من المتاجر.
author: josaw1
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 11acedb719286cc6c9c79e22e8d0ceca2368baee
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802589"
---
# <a name="configure-and-run-job-to-calculate-statements"></a><span data-ttu-id="4ef6e-103">تكوين وتشغيل وظيفة لحساب البيانات</span><span class="sxs-lookup"><span data-stu-id="4ef6e-103">Configure and run job to calculate statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4ef6e-104">يتناول هذا الإجراء تكوين الوظائف الدفعية المتكررة وتشغيلها لإنشاء وحساب كشوف الحسابات لمتجر محدد أو مجموعة من المتاجر.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-104">This procedure walks through configuring and running recurrent batch jobs to create and calculate statements for a selected store or group of stores.</span></span> <span data-ttu-id="4ef6e-105">ويستخدم هذا الإجراء شركة USRT في بيانات العرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="4ef6e-106">انتقل إلى كافة مساحات العمل > ماليات المتاجر.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-106">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="4ef6e-107">انقر فوق حساب كشوف الحسابات.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-107">Click Calculate statements.</span></span>
    * <span data-ttu-id="4ef6e-108">حدد إما متجر معين أو عقدة إذا أردت إنشاء وظيفة دفعية لمجموعة من المتاجر.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-108">Select either a specific store, or a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="4ef6e-109">انقر فوق السهم لإضافة التحديد الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-109">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="4ef6e-110">انقر فوق علامة التبويب "‏‫تشغيل في الخلفية".</span><span class="sxs-lookup"><span data-stu-id="4ef6e-110">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="4ef6e-111">ضمن معالجة الدُفعة، حدد "نعم".</span><span class="sxs-lookup"><span data-stu-id="4ef6e-111">Under Batch processing, select 'Yes'.</span></span>
5. <span data-ttu-id="4ef6e-112">انقر فوق "تكرار".</span><span class="sxs-lookup"><span data-stu-id="4ef6e-112">Click Recurrence.</span></span>
6. <span data-ttu-id="4ef6e-113">في الحقل "تاريخ البدء"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-113">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="4ef6e-114">في حقل "‏‫وقت البدء"، أدخل الوقت.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-114">In the Start time field, enter a time.</span></span>
8. <span data-ttu-id="4ef6e-115">حدد الخيار "‏‫لا يوجد تاريخ انتهاء‬".</span><span class="sxs-lookup"><span data-stu-id="4ef6e-115">Select the No end date option.</span></span>
9. <span data-ttu-id="4ef6e-116">في حقل "PatternUnit‬‬"، أدخل "الأيام".</span><span class="sxs-lookup"><span data-stu-id="4ef6e-116">In the PatternUnit field, enter 'Days'.</span></span>
10. <span data-ttu-id="4ef6e-117">في الحقل "لكل‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-117">In the Per field, enter a number.</span></span>
11. <span data-ttu-id="4ef6e-118">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="4ef6e-118">Click OK.</span></span>
12. <span data-ttu-id="4ef6e-119">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="4ef6e-119">Click OK.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]