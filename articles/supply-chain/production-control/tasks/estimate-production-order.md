---
title: "تقدير أمر إنتاج"
description: "يمكنك تشغيل هذا الإجراء باستخدام شركة بيانات العرض التوضيحي USMF أو البيانات الخاصة بك."
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: dadf0e87eac8522f61bb094c146e37f46a21fc09
ms.openlocfilehash: 862281adac67757e1ce0e9ddd1e96483363abb9a
ms.contentlocale: ar-sa
ms.lasthandoff: 02/06/2018

---
# <a name="estimate-a-production-order"></a><span data-ttu-id="73759-103">تقدير أمر إنتاج</span><span class="sxs-lookup"><span data-stu-id="73759-103">Estimate a production order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="73759-104">يمكنك تشغيل هذا الإجراء باستخدام شركة بيانات العرض التوضيحي USMF أو البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="73759-104">You can run this procedure by using the USMF demo data company or your own data set.</span></span> <span data-ttu-id="73759-105">وفي كلتا الحالتين، تحتاجُ إلى فتح أمر إنتاج يكون في الحالة "تم إنشاؤه".</span><span class="sxs-lookup"><span data-stu-id="73759-105">In both cases, you need to have an open production order that has the Created status.</span></span> <span data-ttu-id="73759-106">وهذا هو الإجراء الثاني من أصل سبعة إجراءات الذي سيشرح دورة حياة أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="73759-106">This is the second procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="estimate-a-production-order"></a><span data-ttu-id="73759-107">تقدير أمر إنتاج</span><span class="sxs-lookup"><span data-stu-id="73759-107">Estimate a production order</span></span>
1. <span data-ttu-id="73759-108">انتقل إلى التحكم بالإنتاج‬ > أوامر الإنتاج > كافة أوامر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="73759-108">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="73759-109">حدد أمرًا يكون في الحالة "تم إنشاؤه" في الشبكة.</span><span class="sxs-lookup"><span data-stu-id="73759-109">Select an order that has the Created status in the grid.</span></span>
3. <span data-ttu-id="73759-110">في جزء "الإجراءات"، انقر فوق "أمر إنتاج".</span><span class="sxs-lookup"><span data-stu-id="73759-110">On the Action Pane, click Production order.</span></span>
4. <span data-ttu-id="73759-111">انقر فوق "تقدير".</span><span class="sxs-lookup"><span data-stu-id="73759-111">Click Estimate.</span></span>
    * <span data-ttu-id="73759-112">في هذه الخطوة، يتم حساب التكاليف المقدرة لأمر إنتاج واحد.</span><span class="sxs-lookup"><span data-stu-id="73759-112">In this step, the estimated costs of a single production order is calculated.</span></span>   
5. <span data-ttu-id="73759-113">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="73759-113">Click OK.</span></span>

## <a name="view-the-calculation-details"></a><span data-ttu-id="73759-114">عرض تفاصيل الحساب</span><span class="sxs-lookup"><span data-stu-id="73759-114">View the calculation details</span></span>
1. <span data-ttu-id="73759-115">في جزء الإجراءات، انقر فوق "إدارة التكاليف‬".</span><span class="sxs-lookup"><span data-stu-id="73759-115">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="73759-116">انقر فوق "عرض تفاصيل الحساب"ز</span><span class="sxs-lookup"><span data-stu-id="73759-116">Click View calculation details.</span></span>
    * <span data-ttu-id="73759-117">تعرض هذه الصفحة تصنيف التكاليف.</span><span class="sxs-lookup"><span data-stu-id="73759-117">This page displays the cost breakdown.</span></span> <span data-ttu-id="73759-118">على سبيل المثال، يمكنك عرض إجمالي سعر التكلفة لكل وحدة لمنتج نهائي في الصف الأول.</span><span class="sxs-lookup"><span data-stu-id="73759-118">For example, you can view the total cost price per unit for the finished product in the first row.</span></span> <span data-ttu-id="73759-119">تحتوي الصفوف التالية على التكاليف وفقا لقائمة مكونات الصنف ومسار الإنتاج والتكاليف غير المباشرة.</span><span class="sxs-lookup"><span data-stu-id="73759-119">The subsequent rows contain costs according to the bill of materials, production route, and indirect costs.</span></span>  

