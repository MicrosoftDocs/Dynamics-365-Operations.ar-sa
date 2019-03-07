---
title: ترحيل الدفعات والمبيعات على الإنترنت
description: يتناول هذا الإجراء تكوين وظيفة دفعية متكررة وتشغيلها لإنشاء أوامر الشراء والمدفوعات لحركات المتجر على الإنترنت.
author: jashanno
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
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 13839bbe6ca03f3cfc7036fce87477bf7d5af2a7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "353484"
---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="87027-103">ترحيل الدفعات والمبيعات على الإنترنت</span><span class="sxs-lookup"><span data-stu-id="87027-103">Posting of online sales and payments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="87027-104">يتناول هذا الإجراء تكوين وظيفة دفعية متكررة وتشغيلها لإنشاء أوامر الشراء والمدفوعات لحركات المتجر على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="87027-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="87027-105">ويستخدم هذا الإجراء شركة USRT في بيانات العرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="87027-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="87027-106">انتقل إلى كافة مساحات العمل > ماليات متجر البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="87027-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="87027-107">انقر فوق مزامنة الأوامر.</span><span class="sxs-lookup"><span data-stu-id="87027-107">Click Synchronize orders.</span></span>
3. <span data-ttu-id="87027-108">في حقل "‏‫التدرج الهرمي للمؤسسات‬"، حدد "متاجر البيع بالتجزئة حسب المنطقة".</span><span class="sxs-lookup"><span data-stu-id="87027-108">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="87027-109">حدد إما متجر معين على الإنترنت أو حدد عقدة إذا أردت إنشاء وظيفة دفعية لمجموعة من المتاجر.</span><span class="sxs-lookup"><span data-stu-id="87027-109">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="87027-110">انقر فوق السهم لإضافة التحديد الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="87027-110">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="87027-111">انقر فوق علامة التبويب "‏‫تشغيل في الخلفية".</span><span class="sxs-lookup"><span data-stu-id="87027-111">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="87027-112">حدد خانة الاختيار "معالجة الدُفعة" أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="87027-112">Check or uncheck the Batch processing checkbox.</span></span>
6. <span data-ttu-id="87027-113">انقر فوق "تكرار".</span><span class="sxs-lookup"><span data-stu-id="87027-113">Click Recurrence.</span></span>
7. <span data-ttu-id="87027-114">حدد الخيار "‏‫لا يوجد تاريخ انتهاء‬".</span><span class="sxs-lookup"><span data-stu-id="87027-114">Select the No end date option.</span></span>
8. <span data-ttu-id="87027-115">في حقل "العدد"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="87027-115">In the Count field, enter a number.</span></span>
9. <span data-ttu-id="87027-116">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="87027-116">Click OK.</span></span>
10. <span data-ttu-id="87027-117">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="87027-117">Click OK.</span></span>

