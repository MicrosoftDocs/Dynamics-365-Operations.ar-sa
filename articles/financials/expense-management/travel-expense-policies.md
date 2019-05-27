---
title: تعريف سياسات المصروفات
description: يمكنك تعريف سياسات المصروفات التي يجب على العاملين اتباعها عند إدخال تقارير المصروفات وطلبات السفر‬ وإرسالها في Microsoft Dynamics 365 for Finance and Operations.
author: ryansandness
manager: AnnBe
ms.date: 04/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9f0ff56f0ff106bc168b6a27612e08743a539a07
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/07/2019
ms.locfileid: "1514429"
---
# <a name="expense-policies"></a><span data-ttu-id="3e8dc-103">سياسات المصروفات</span><span class="sxs-lookup"><span data-stu-id="3e8dc-103">Expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3e8dc-104">يمكنك تعريف السياسات التي يجب على العاملين اتباعها عند إدخال تقارير المصروفات وطلبات السفر‬ وإرسالها.</span><span class="sxs-lookup"><span data-stu-id="3e8dc-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="3e8dc-105">حيث يمكن أن يساعد تنفيذ سياسات المصروفات في إدارة المصروفات بفعالية.</span><span class="sxs-lookup"><span data-stu-id="3e8dc-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="3e8dc-106">على سبيل المثال، يمكن تعيين سياسة لمصروفات السفر في مدينة الرياض، تفيد بعدم تجاوز تكلفة الإقامة فيها 250 ريالاً سعوديًا في الليلة الواحدة.</span><span class="sxs-lookup"><span data-stu-id="3e8dc-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="3e8dc-107">إذا قدم عامل تقرير مصروفات أو طلب سفر يتجاوز فيه سعر الغرفة هذا المبلغ، فسوف يقوم النظام بإخطار</span><span class="sxs-lookup"><span data-stu-id="3e8dc-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="3e8dc-108">العامل أنه قد تم تجاوز مبلغ السياسة الخاص بالمصروفات.</span><span class="sxs-lookup"><span data-stu-id="3e8dc-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="3e8dc-109">يمكنك تكوين الرسالة التي سيستلمها العامل عندما</span><span class="sxs-lookup"><span data-stu-id="3e8dc-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="3e8dc-110">تحدد السياسة.</span><span class="sxs-lookup"><span data-stu-id="3e8dc-110">define the policy.</span></span>      
        
<span data-ttu-id="3e8dc-111">يمكنك تحديد ثلاثة أنواع للسياسة:</span><span class="sxs-lookup"><span data-stu-id="3e8dc-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="3e8dc-112">تحذير – يسمح للعامل بإرسال تقرير مصروفات أو طلب سفر، ولكن ستوضع علامة على المصروفات لجميع المعتمدين</span><span class="sxs-lookup"><span data-stu-id="3e8dc-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="3e8dc-113">لإعداد تقرير بها.</span><span class="sxs-lookup"><span data-stu-id="3e8dc-113">for later reporting.</span></span>        

- <span data-ttu-id="3e8dc-114">خطأ - يتطلب من العامل مراجعة المصروفات لتتوافق مع السياسة قبل إرسال تقرير المصروفات أو طلب السفر.</span><span class="sxs-lookup"><span data-stu-id="3e8dc-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="3e8dc-115">المبرِر - يتطلب من العامل أو المدير إدخال مبرِر لتجاوز مبلغ السياسة قبل إرسال تقرير المصروفات أو طلب السفر.</span><span class="sxs-lookup"><span data-stu-id="3e8dc-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

# <a name="policy-tips"></a><span data-ttu-id="3e8dc-116">تلميحات السياسة</span><span class="sxs-lookup"><span data-stu-id="3e8dc-116">Policy tips</span></span>
<span data-ttu-id="3e8dc-117">فيما يلي بعض الاقتراحات التي يمكنها مساعدتك أثناء إنشاء سياسات جديدة لإدارة المصروفات.</span><span class="sxs-lookup"><span data-stu-id="3e8dc-117">Here are a few suggestions that can assist you whe creating new policies for expense management.</span></span> 
* <span data-ttu-id="3e8dc-118">يسري مفعول السياسة عند إنشائها، ولن تكون سارية المفعول عند إنشائها في تاريخ يقع بعد تاريخ حدوث المصروفات.</span><span class="sxs-lookup"><span data-stu-id="3e8dc-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="3e8dc-119">على سبيل المثال، إذا أردت إنشاء سياسة جديدة اليوم لفرض الحد الأقصى لمصروفات الوجبات بحيث يساوي 50 دولارًا، فلن يتم التدقيق في أي مصروفات موجودة تم إدخالها اعتبارًا من الأمس في مقابل هذه السياسة.</span><span class="sxs-lookup"><span data-stu-id="3e8dc-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="3e8dc-120">عند إنشاء سياسة لفئة مصروفات يمكن تفصيلها، يمكنك إضافة شرط لنوع بند المصروفات.</span><span class="sxs-lookup"><span data-stu-id="3e8dc-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="3e8dc-121">قد لا تكون بعض السياسات ذات معنى بالنسبة إلى البنود المفصلة، مثلاً عند المطالبة بإيصال استلام، ويجب تطبيقها فقط على مستوى بند الرأس أو بند غير مفصل.</span><span class="sxs-lookup"><span data-stu-id="3e8dc-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 

# <a name="when-to-evaluate-policies"></a><span data-ttu-id="3e8dc-122">متى يجب تقييم السياسة</span><span class="sxs-lookup"><span data-stu-id="3e8dc-122">When to evaluate policies</span></span>

<span data-ttu-id="3e8dc-123">في معلمات إدارة المصروفات، يوجد خيار لتقييم سياسات إدارة المصروفات عند حفظ بند أو عند إرسال تقرير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="3e8dc-123">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="3e8dc-124">إذا اخترت تقييم وقت حفظ البند، فهذا يضمن حصول المستخدمين على رؤية مبكرة على المهام التي يجب عليهم القيام بها لإكمال تقرير مصروفاتهم مرة واحدة.</span><span class="sxs-lookup"><span data-stu-id="3e8dc-124">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="3e8dc-125">وإلا، فيمكنك تأخير تقييم السياسة وتوفير الوقت إذا حدثت عملية التحقق من الصحة في النهاية، أثناء الإرسال إلى سير العمل.</span><span class="sxs-lookup"><span data-stu-id="3e8dc-125">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>
