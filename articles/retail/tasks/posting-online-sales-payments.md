--- 
title: " ترحيل الدفعات والمبيعات على الإنترنت"
description: "يتناول هذا الإجراء تكوين وظيفة دفعية متكررة وتشغيلها لإنشاء أوامر الشراء والمدفوعات لحركات المتجر على الإنترنت."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 3799515c538826ac2a0b37a26e83f375591f9813
ms.contentlocale: ar-sa
ms.lasthandoff: 01/19/2018

---
# <a name="post-online-sales-and-payments"></a><span data-ttu-id="c8a96-103"> ترحيل الدفعات والمبيعات على الإنترنت</span><span class="sxs-lookup"><span data-stu-id="c8a96-103">Post online sales and payments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="c8a96-104">يتناول هذا الإجراء تكوين وظيفة دفعية متكررة وتشغيلها لإنشاء أوامر الشراء والمدفوعات لحركات المتجر على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="c8a96-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="c8a96-105">ويستخدم هذا الإجراء شركة USRT في بيانات العرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="c8a96-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="c8a96-106">انتقل إلى كافة مساحات العمل > ماليات متجر البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="c8a96-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="c8a96-107">انقر فوق مزامنة الأوامر.</span><span class="sxs-lookup"><span data-stu-id="c8a96-107">Click Synchronize orders.</span></span>
3. <span data-ttu-id="c8a96-108">في حقل "‏‫التدرج الهرمي للمؤسسات‬"، حدد "متاجر البيع بالتجزئة حسب المنطقة".</span><span class="sxs-lookup"><span data-stu-id="c8a96-108">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="c8a96-109">حدد إما متجر معين على الإنترنت أو حدد عقدة إذا أردت إنشاء وظيفة دفعية لمجموعة من المتاجر.</span><span class="sxs-lookup"><span data-stu-id="c8a96-109">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="c8a96-110">انقر فوق السهم لإضافة التحديد الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="c8a96-110">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="c8a96-111">انقر فوق علامة التبويب "‏‫تشغيل في الخلفية".</span><span class="sxs-lookup"><span data-stu-id="c8a96-111">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="c8a96-112">حدد خانة الاختيار "معالجة الدُفعة" أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="c8a96-112">Check or uncheck the Batch processing checkbox.</span></span>
6. <span data-ttu-id="c8a96-113">انقر فوق "تكرار".</span><span class="sxs-lookup"><span data-stu-id="c8a96-113">Click Recurrence.</span></span>
7. <span data-ttu-id="c8a96-114">حدد الخيار "‏‫لا يوجد تاريخ انتهاء‬".</span><span class="sxs-lookup"><span data-stu-id="c8a96-114">Select the No end date option.</span></span>
8. <span data-ttu-id="c8a96-115">في حقل "العدد"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="c8a96-115">In the Count field, enter a number.</span></span>
9. <span data-ttu-id="c8a96-116">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c8a96-116">Click OK.</span></span>
10. <span data-ttu-id="c8a96-117">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c8a96-117">Click OK.</span></span>


