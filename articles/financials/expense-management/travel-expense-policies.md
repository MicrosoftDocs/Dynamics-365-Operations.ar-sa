---
title: "تعريف سياسات المصروفات"
description: "يمكنك تعريف سياسات المصروفات التي يجب على العاملين اتباعها عند إدخال تقارير المصروفات وطلبات السفر‬ وإرسالها في Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition."
author: saraschi2
manager: AnnBe
ms.date: 09/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi2
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 9a5ce1a3b6519b510c9f5aa5618ab91f77a2d91a
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="expense-policies"></a><span data-ttu-id="04a5b-103">سياسات المصروفات</span><span class="sxs-lookup"><span data-stu-id="04a5b-103">Expense policies</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="04a5b-104">يمكنك تعريف السياسات التي يجب على العاملين اتباعها عند إدخال تقارير المصروفات وطلبات السفر‬ وإرسالها.</span><span class="sxs-lookup"><span data-stu-id="04a5b-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span> <span data-ttu-id="04a5b-105">حيث يمكن أن يساعد تنفيذ سياسات المصروفات في إدارة المصروفات بفعالية.</span><span class="sxs-lookup"><span data-stu-id="04a5b-105">Implementing expense policies can help you manage expenses effectively.</span></span> 

<span data-ttu-id="04a5b-106">على سبيل المثال، يمكن تعيين سياسة لمصروفات السفر في مدينة الرياض، تفيد بعدم تجاوز تكلفة الإقامة فيها 250 ريالاً سعوديًا في الليلة الواحدة.</span><span class="sxs-lookup"><span data-stu-id="04a5b-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span> <span data-ttu-id="04a5b-107">إذا قام أحد الموظفين بإرسال تقرير مصروفات أو طلب سفر حيث تجاوز معدل مصروفات الغرفة بالفندق هذا المبلغ، فإن النظام سيخطر المستخدم بأنه قد تجاوز المبلغ الذي حددته السياسة والمتعلق بالمصروفات.</span><span class="sxs-lookup"><span data-stu-id="04a5b-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="04a5b-108">يمكنك تكوين الرسالة التي سيستلمها العامل عندما تحدد السياسة.</span><span class="sxs-lookup"><span data-stu-id="04a5b-108">You can configure the message that the worker will receive when you define the policy.</span></span> 

<span data-ttu-id="04a5b-109">يمكنك تحديد ثلاثة أنواع للسياسة:</span><span class="sxs-lookup"><span data-stu-id="04a5b-109">You can define three types of policies:</span></span> 

 - <span data-ttu-id="04a5b-110">تحذير – يسمح للعامل بإرسال تقرير مصروفات أو طلب سفر، ولكن ستوضع علامة على المصروفات لجميع المعتمدين</span><span class="sxs-lookup"><span data-stu-id="04a5b-110">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>  
 <span data-ttu-id="04a5b-111">لإعداد تقرير بها.</span><span class="sxs-lookup"><span data-stu-id="04a5b-111">for later reporting.</span></span> 
 - <span data-ttu-id="04a5b-112">خطأ - يتطلب من العامل مراجعة المصروفات لتتوافق مع السياسة قبل إرسال تقرير المصروفات أو طلب السفر.</span><span class="sxs-lookup"><span data-stu-id="04a5b-112">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span> 
 - <span data-ttu-id="04a5b-113">المبرِر - يتطلب من العامل أو المدير إدخال مبرِر لتجاوز مبلغ السياسة قبل إرسال تقرير المصروفات أو طلب السفر.</span><span class="sxs-lookup"><span data-stu-id="04a5b-113">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span> 

<span data-ttu-id="04a5b-114">يمكن أيضًا إعداد نطاق تاريخ تكون خلاله سياسات المصروفات سارية المفعول.</span><span class="sxs-lookup"><span data-stu-id="04a5b-114">You can also set up a date range for which expense policies are in effect.</span></span> <span data-ttu-id="04a5b-115">على سبيل المثال، يمكن أن تكون تكلفة رحلات السفر جوًا بين الرياض والقاهرة غالية الثمن أثناء ذروة موسم السفر خلال الأعياد.</span><span class="sxs-lookup"><span data-stu-id="04a5b-115">For example, airline fares for flights between Denmark and New York City can be expensive during the peak holiday travel season.</span></span> <span data-ttu-id="04a5b-116">ويمكن تحديد قاعدة لتحديد نفقات الرحلات الجوية تقيد تكلفة الرحلات الجوية إلى مدينة الرياض بحيث لا تتجاوز 2000 ريال سعودي ويمكن تحديد تفعيل هذه القاعدة خلال الفترة من 15 مارس إلى 15 سبتمبر.</span><span class="sxs-lookup"><span data-stu-id="04a5b-116">You can define a flight expense rule that restricts the cost of flights to New York City to a limit of DKK 5000, and you can specify that this rule be in effect between March 15 and September 15.</span></span> 

