---
title: تعريف سياسات المصروفات
description: يمكنك تعريف سياسات المصروفات التي يجب على العاملين اتباعها عند إدخال تقارير المصروفات وطلبات السفر‬ وإرسالها في Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 22504e0e26c025d117f29dee3b59b41d508e7724
ms.sourcegitcommit: 4f90b9ddedf312e75a714e0ec7f7ee5fd43cac6a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/21/2020
ms.locfileid: "3389705"
---
# <a name="define-expense-policies"></a><span data-ttu-id="95e85-103">تعريف سياسات المصروفات</span><span class="sxs-lookup"><span data-stu-id="95e85-103">Define expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="95e85-104">يمكنك تعريف السياسات التي يجب على العاملين اتباعها عند إدخال تقارير المصروفات وطلبات السفر‬ وإرسالها.</span><span class="sxs-lookup"><span data-stu-id="95e85-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="95e85-105">حيث يمكن أن يساعد تنفيذ سياسات المصروفات في إدارة المصروفات بفعالية.</span><span class="sxs-lookup"><span data-stu-id="95e85-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="95e85-106">على سبيل المثال، يمكن تعيين سياسة لمصروفات السفر في مدينة الرياض، تفيد بعدم تجاوز تكلفة الإقامة فيها 250 ريالاً سعوديًا في الليلة الواحدة.</span><span class="sxs-lookup"><span data-stu-id="95e85-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="95e85-107">إذا قدم عامل تقرير مصروفات أو طلب سفر يتجاوز فيه سعر الغرفة هذا المبلغ، فسوف يقوم النظام بإخطار</span><span class="sxs-lookup"><span data-stu-id="95e85-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="95e85-108">العامل أنه قد تم تجاوز مبلغ السياسة الخاص بالمصروفات.</span><span class="sxs-lookup"><span data-stu-id="95e85-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="95e85-109">يمكنك تكوين الرسالة التي سيستلمها العامل عندما</span><span class="sxs-lookup"><span data-stu-id="95e85-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="95e85-110">تحدد السياسة.</span><span class="sxs-lookup"><span data-stu-id="95e85-110">define the policy.</span></span>      
        
<span data-ttu-id="95e85-111">يمكنك تحديد ثلاثة أنواع للسياسة:</span><span class="sxs-lookup"><span data-stu-id="95e85-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="95e85-112">تحذير – يسمح للعامل بإرسال تقرير مصروفات أو طلب سفر، ولكن ستوضع علامة على المصروفات لجميع المعتمدين</span><span class="sxs-lookup"><span data-stu-id="95e85-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="95e85-113">لإعداد تقرير بها.</span><span class="sxs-lookup"><span data-stu-id="95e85-113">for later reporting.</span></span>        

- <span data-ttu-id="95e85-114">خطأ - يتطلب من العامل مراجعة المصروفات لتتوافق مع السياسة قبل إرسال تقرير المصروفات أو طلب السفر.</span><span class="sxs-lookup"><span data-stu-id="95e85-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="95e85-115">المبرِر - يتطلب من العامل أو المدير إدخال مبرِر لتجاوز مبلغ السياسة قبل إرسال تقرير المصروفات أو طلب السفر.</span><span class="sxs-lookup"><span data-stu-id="95e85-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="95e85-116">تلميحات السياسة</span><span class="sxs-lookup"><span data-stu-id="95e85-116">Policy tips</span></span>
<span data-ttu-id="95e85-117">فيما يلي بعض الاقتراحات التي يمكنها مساعدتك أثناء إنشاء سياسات جديدة لإدارة المصروفات.</span><span class="sxs-lookup"><span data-stu-id="95e85-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="95e85-118">يسري مفعول السياسة عند إنشائها، ولن تكون سارية المفعول عند إنشائها في تاريخ يقع بعد تاريخ حدوث المصروفات.</span><span class="sxs-lookup"><span data-stu-id="95e85-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="95e85-119">على سبيل المثال، إذا أردت إنشاء سياسة جديدة اليوم لفرض الحد الأقصى لمصروفات الوجبات بحيث يساوي 50 دولارًا، فلن يتم التدقيق في أي مصروفات موجودة تم إدخالها اعتبارًا من الأمس في مقابل هذه السياسة.</span><span class="sxs-lookup"><span data-stu-id="95e85-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="95e85-120">عند إنشاء سياسة لفئة مصروفات يمكن تفصيلها، يمكنك إضافة شرط لنوع بند المصروفات.</span><span class="sxs-lookup"><span data-stu-id="95e85-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="95e85-121">قد لا تكون بعض السياسات ذات معنى بالنسبة إلى البنود المفصلة، مثلاً عند المطالبة بإيصال استلام، ويجب تطبيقها فقط على مستوى بند الرأس أو بند غير مفصل.</span><span class="sxs-lookup"><span data-stu-id="95e85-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="95e85-122">يتم تقييم سياسات إدارة المصروفات مقابل الكيان المصدر بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="95e85-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="95e85-123">بالنسبة للسيناريوهات بين الشركات الشقيقة، يمكنك تعيين السياسة التي سيتم تقييمها مقابل الكيان الوجهة (الكيان المقترض) بدلا من ذلك.</span><span class="sxs-lookup"><span data-stu-id="95e85-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="95e85-124">لتشغيل السياسات مقابل الكيان الوجهة، قم بتشغيل ميزة "تقييم سياسة المصروفات مقابل الكيان القانوني المقترض" في مساحة عمل **إدارة الميزات**.</span><span class="sxs-lookup"><span data-stu-id="95e85-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="95e85-125">متى يجب تقييم السياسة</span><span class="sxs-lookup"><span data-stu-id="95e85-125">When to evaluate policies</span></span>

<span data-ttu-id="95e85-126">في معلمات إدارة المصروفات، يوجد خيار لتقييم سياسات إدارة المصروفات عند حفظ بند أو عند إرسال تقرير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="95e85-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="95e85-127">إذا اخترت تقييم وقت حفظ البند، فهذا يضمن حصول المستخدمين على رؤية مبكرة على المهام التي يجب عليهم القيام بها لإكمال تقرير مصروفاتهم مرة واحدة.</span><span class="sxs-lookup"><span data-stu-id="95e85-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="95e85-128">وإلا، فيمكنك تأخير تقييم السياسة وتوفير الوقت إذا حدثت عملية التحقق من الصحة في النهاية، أثناء الإرسال إلى سير العمل.</span><span class="sxs-lookup"><span data-stu-id="95e85-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>
