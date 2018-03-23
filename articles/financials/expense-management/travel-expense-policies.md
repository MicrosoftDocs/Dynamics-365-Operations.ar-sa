---
title: "تعريف سياسات المصروفات"
description: "يمكنك تعريف سياسات المصروفات التي يجب على العاملين اتباعها عند إدخال تقارير المصروفات وطلبات السفر‬ وإرسالها في Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: b52fe81015a324bde07f387b42b834b79dc7c2da
ms.contentlocale: ar-sa
ms.lasthandoff: 03/13/2018

---

# <a name="expense-policies"></a><span data-ttu-id="08b63-103">سياسات المصروفات</span><span class="sxs-lookup"><span data-stu-id="08b63-103">Expense policies</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="08b63-104">يمكنك تعريف السياسات التي يجب على العاملين اتباعها عند إدخال تقارير المصروفات وطلبات السفر‬ وإرسالها.</span><span class="sxs-lookup"><span data-stu-id="08b63-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="08b63-105">حيث يمكن أن يساعد تنفيذ سياسات المصروفات في إدارة المصروفات بفعالية.</span><span class="sxs-lookup"><span data-stu-id="08b63-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="08b63-106">على سبيل المثال، يمكن تعيين سياسة لمصروفات السفر في مدينة الرياض، تفيد بعدم تجاوز تكلفة الإقامة فيها 250 ريالاً سعوديًا في الليلة الواحدة.</span><span class="sxs-lookup"><span data-stu-id="08b63-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="08b63-107">إذا قدم عامل تقرير مصروفات أو طلب سفر يتجاوز فيه سعر الغرفة هذا المبلغ، فسوف يقوم النظام بإخطار</span><span class="sxs-lookup"><span data-stu-id="08b63-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="08b63-108">العامل أنه قد تم تجاوز مبلغ السياسة الخاص بالمصروفات.</span><span class="sxs-lookup"><span data-stu-id="08b63-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="08b63-109">يمكنك تكوين الرسالة التي سيستلمها العامل عندما</span><span class="sxs-lookup"><span data-stu-id="08b63-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="08b63-110">تحدد السياسة.</span><span class="sxs-lookup"><span data-stu-id="08b63-110">define the policy.</span></span>      
        
<span data-ttu-id="08b63-111">يمكنك تحديد ثلاثة أنواع للسياسة:</span><span class="sxs-lookup"><span data-stu-id="08b63-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="08b63-112">تحذير – يسمح للعامل بإرسال تقرير مصروفات أو طلب سفر، ولكن ستوضع علامة على المصروفات لجميع المعتمدين</span><span class="sxs-lookup"><span data-stu-id="08b63-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
<span data-ttu-id="08b63-113">لإعداد تقرير بها.</span><span class="sxs-lookup"><span data-stu-id="08b63-113">for later reporting.</span></span>        

- <span data-ttu-id="08b63-114">خطأ - يتطلب من العامل مراجعة المصروفات لتتوافق مع السياسة قبل إرسال تقرير المصروفات أو طلب السفر.</span><span class="sxs-lookup"><span data-stu-id="08b63-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="08b63-115">المبرِر - يتطلب من العامل أو المدير إدخال مبرِر لتجاوز مبلغ السياسة قبل إرسال تقرير المصروفات أو طلب السفر.</span><span class="sxs-lookup"><span data-stu-id="08b63-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        
 
 <span data-ttu-id="08b63-116">يمكن أيضًا إعداد نطاق تاريخ تكون خلاله سياسات المصروفات سارية المفعول.</span><span class="sxs-lookup"><span data-stu-id="08b63-116">You can also set up a date range for which expense policies are in effect.</span></span> <span data-ttu-id="08b63-117">على سبيل المثال، يمكن أن تكون تكلفة رحلات السفر بين الدانمارك</span><span class="sxs-lookup"><span data-stu-id="08b63-117">For example, airline fares for flights between Denmark</span></span>      
 <span data-ttu-id="08b63-118">ومدينة نيويورك غالية الثمن أثناء ذروة موسم السفر خلال العطلات.</span><span class="sxs-lookup"><span data-stu-id="08b63-118">and New York City can be expensive during the peak holiday travel season.</span></span> <span data-ttu-id="08b63-119">يمكنك تحديد قاعدة لتحديد مصروفات الرحلة بحيث تقيد</span><span class="sxs-lookup"><span data-stu-id="08b63-119">You can define a flight expense rule that restricts the</span></span>      
 <span data-ttu-id="08b63-120">تكلفة الرحلات الجوية إلى مدينة نيويورك إلى حد 5000 كورونا دانمركية، ويمكنك تحديد تفعيل هذه القاعدة خلال الفترة من 15 مارس و</span><span class="sxs-lookup"><span data-stu-id="08b63-120">cost of flights to New York City to a limit of DKK 5000, and you can specify that this rule be in effect between March 15 and</span></span>      
 <span data-ttu-id="08b63-121">15 سبتمبر.</span><span class="sxs-lookup"><span data-stu-id="08b63-121">September 15.</span></span>

