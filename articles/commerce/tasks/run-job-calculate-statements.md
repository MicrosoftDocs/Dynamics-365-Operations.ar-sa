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
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8366bfff16bac8ef8f7b15cb97417d474b52f59c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232751"
---
# <a name="configure-and-run-job-to-calculate-statements"></a><span data-ttu-id="2561b-103">تكوين وتشغيل وظيفة لحساب البيانات</span><span class="sxs-lookup"><span data-stu-id="2561b-103">Configure and run job to calculate statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2561b-104">يتناول هذا الإجراء تكوين الوظائف الدفعية المتكررة وتشغيلها لإنشاء وحساب كشوف الحسابات لمتجر محدد أو مجموعة من المتاجر.</span><span class="sxs-lookup"><span data-stu-id="2561b-104">This procedure walks through configuring and running recurrent batch jobs to create and calculate statements for a selected store or group of stores.</span></span> <span data-ttu-id="2561b-105">ويستخدم هذا الإجراء شركة USRT في بيانات العرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="2561b-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="2561b-106">انتقل إلى كافة مساحات العمل > ماليات المتاجر.</span><span class="sxs-lookup"><span data-stu-id="2561b-106">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="2561b-107">انقر فوق حساب كشوف الحسابات.</span><span class="sxs-lookup"><span data-stu-id="2561b-107">Click Calculate statements.</span></span>
    * <span data-ttu-id="2561b-108">حدد إما متجر معين أو عقدة إذا أردت إنشاء وظيفة دفعية لمجموعة من المتاجر.</span><span class="sxs-lookup"><span data-stu-id="2561b-108">Select either a specific store, or a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="2561b-109">انقر فوق السهم لإضافة التحديد الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="2561b-109">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="2561b-110">انقر فوق علامة التبويب "‏‫تشغيل في الخلفية".</span><span class="sxs-lookup"><span data-stu-id="2561b-110">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="2561b-111">ضمن معالجة الدُفعة، حدد "نعم".</span><span class="sxs-lookup"><span data-stu-id="2561b-111">Under Batch processing, select 'Yes'.</span></span>
5. <span data-ttu-id="2561b-112">انقر فوق "تكرار".</span><span class="sxs-lookup"><span data-stu-id="2561b-112">Click Recurrence.</span></span>
6. <span data-ttu-id="2561b-113">في الحقل "تاريخ البدء"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="2561b-113">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="2561b-114">في حقل "‏‫وقت البدء"، أدخل الوقت.</span><span class="sxs-lookup"><span data-stu-id="2561b-114">In the Start time field, enter a time.</span></span>
8. <span data-ttu-id="2561b-115">حدد الخيار "‏‫لا يوجد تاريخ انتهاء‬".</span><span class="sxs-lookup"><span data-stu-id="2561b-115">Select the No end date option.</span></span>
9. <span data-ttu-id="2561b-116">في حقل "PatternUnit‬‬"، أدخل "الأيام".</span><span class="sxs-lookup"><span data-stu-id="2561b-116">In the PatternUnit field, enter 'Days'.</span></span>
10. <span data-ttu-id="2561b-117">في الحقل "لكل‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="2561b-117">In the Per field, enter a number.</span></span>
11. <span data-ttu-id="2561b-118">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="2561b-118">Click OK.</span></span>
12. <span data-ttu-id="2561b-119">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="2561b-119">Click OK.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]