--- 
title: " ترحيل الدفعات والمبيعات على الإنترنت"
description: "يتناول هذا الإجراء تكوين وظيفة دفعية متكررة وتشغيلها لإنشاء أوامر الشراء والمدفوعات لحركات المتجر على الإنترنت."
author: jashanno
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
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: b1ec55edb0799ff141c77575ce53ab0313d9cca9
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---
# <a name="post-online-sales-and-payments"></a><span data-ttu-id="5d71b-103"> ترحيل الدفعات والمبيعات على الإنترنت</span><span class="sxs-lookup"><span data-stu-id="5d71b-103">Post online sales and payments</span></span>

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="5d71b-104">يتناول هذا الإجراء تكوين وظيفة دفعية متكررة وتشغيلها لإنشاء أوامر الشراء والمدفوعات لحركات المتجر على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="5d71b-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="5d71b-105">ويستخدم هذا الإجراء شركة USRT في بيانات العرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="5d71b-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="5d71b-106">انتقل إلى كافة مساحات العمل > ماليات متجر البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="5d71b-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="5d71b-107">انقر فوق مزامنة الأوامر.</span><span class="sxs-lookup"><span data-stu-id="5d71b-107">Click Synchronize orders.</span></span>
3. <span data-ttu-id="5d71b-108">في حقل "‏‫التدرج الهرمي للمؤسسات‬"، حدد "متاجر البيع بالتجزئة حسب المنطقة".</span><span class="sxs-lookup"><span data-stu-id="5d71b-108">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="5d71b-109">حدد إما متجر معين على الإنترنت أو حدد عقدة إذا أردت إنشاء وظيفة دفعية لمجموعة من المتاجر.</span><span class="sxs-lookup"><span data-stu-id="5d71b-109">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="5d71b-110">انقر فوق السهم لإضافة التحديد الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="5d71b-110">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="5d71b-111">انقر فوق علامة التبويب "‏‫تشغيل في الخلفية".</span><span class="sxs-lookup"><span data-stu-id="5d71b-111">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="5d71b-112">حدد خانة الاختيار "معالجة الدُفعة" أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="5d71b-112">Check or uncheck the Batch processing checkbox.</span></span>
6. <span data-ttu-id="5d71b-113">انقر فوق "تكرار".</span><span class="sxs-lookup"><span data-stu-id="5d71b-113">Click Recurrence.</span></span>
7. <span data-ttu-id="5d71b-114">حدد الخيار "‏‫لا يوجد تاريخ انتهاء‬".</span><span class="sxs-lookup"><span data-stu-id="5d71b-114">Select the No end date option.</span></span>
8. <span data-ttu-id="5d71b-115">في حقل "العدد"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="5d71b-115">In the Count field, enter a number.</span></span>
9. <span data-ttu-id="5d71b-116">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="5d71b-116">Click OK.</span></span>
10. <span data-ttu-id="5d71b-117">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="5d71b-117">Click OK.</span></span>


