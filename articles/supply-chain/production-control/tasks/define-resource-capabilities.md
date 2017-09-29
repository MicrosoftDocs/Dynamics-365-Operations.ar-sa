--- 
title: "تحديد قدرات الموارد"
description: "تصف قدرات الموارد ما يمكن لموارد العمليات القيام به."
author: sorenva
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 99c230c0e6a580f77d863b6f0be298615966c479
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="define-resource-capabilities"></a><span data-ttu-id="0de54-103">تحديد قدرات الموارد</span><span class="sxs-lookup"><span data-stu-id="0de54-103">Define resource capabilities</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0de54-104">تصف قدرات الموارد ما يمكن لموارد العمليات القيام به.</span><span class="sxs-lookup"><span data-stu-id="0de54-104">Resource capabilities describe what operations resources can do.</span></span> <span data-ttu-id="0de54-105">أثناء الجدولة، تتم مطابقة متطلبات كل وظيفة وعملية مع قدرات الموارد المتاحة.</span><span class="sxs-lookup"><span data-stu-id="0de54-105">During scheduling, the requirements of each job and operation are matched against the capabilities of the available resources.</span></span> <span data-ttu-id="0de54-106">سيساعدك دليل المهام هذا في إنشاء قدرة مورد وتعيينها إلى مورد.</span><span class="sxs-lookup"><span data-stu-id="0de54-106">This task guide will help you create a resource capability and assign it to a resource.</span></span> <span data-ttu-id="0de54-107">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USMF.‬</span><span class="sxs-lookup"><span data-stu-id="0de54-107">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-resource-capability"></a><span data-ttu-id="0de54-108">إنشاء قدرة مورد</span><span class="sxs-lookup"><span data-stu-id="0de54-108">Create a resource capability</span></span>
1. <span data-ttu-id="0de54-109">انتقل إلى "قدرات الموارد".</span><span class="sxs-lookup"><span data-stu-id="0de54-109">Go to Resource capabilities.</span></span>
2. <span data-ttu-id="0de54-110">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="0de54-110">Click New.</span></span>
3. <span data-ttu-id="0de54-111">في حقل "القدرة"، اكتب معرف قدرة المورد.</span><span class="sxs-lookup"><span data-stu-id="0de54-111">In the Capability field, type the ID of the resource capability.</span></span>
    * <span data-ttu-id="0de54-112">لعملية معينة، استخدم معرف القدرة لتحديد أن الموارد يجب أن يكون لديها هذه القدرة لتنفيذ العملية.</span><span class="sxs-lookup"><span data-stu-id="0de54-112">For a given operation, you use the capability ID to specify that resources must have this capability to perform the operation.</span></span>  
4. <span data-ttu-id="0de54-113">في حقل "الوصف"، أدخل وصفًا للقدرة.</span><span class="sxs-lookup"><span data-stu-id="0de54-113">In the Description field, enter a description of the capability.</span></span>

## <a name="assign-capability-to-a-resource"></a><span data-ttu-id="0de54-114">تعيين قدرة إلى مورد</span><span class="sxs-lookup"><span data-stu-id="0de54-114">Assign capability to a resource</span></span>
1. <span data-ttu-id="0de54-115">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="0de54-115">Click Add.</span></span>
2. <span data-ttu-id="0de54-116">في حقل "المورد"، اكتب معرف المورد.</span><span class="sxs-lookup"><span data-stu-id="0de54-116">In the Resource field, type the ID of the resource.</span></span>
    * <span data-ttu-id="0de54-117">يمكن تعيين قدرة مورد إلى مورد واحد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="0de54-117">A resource capability can be assigned to one or more resources.</span></span>  
3. <span data-ttu-id="0de54-118">في الحقل "تاريخ انتهاء الصلاحية"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="0de54-118">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="0de54-119">يمكنك استخدام هذا الحقل لتحديد مورد لديه القدرة لفترة محددة من الوقت فقط.</span><span class="sxs-lookup"><span data-stu-id="0de54-119">You can use this field to specify that a resource has the capability for only a limited time.</span></span>  
4. <span data-ttu-id="0de54-120">في حقل "الأولوية"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="0de54-120">In the Priority field, enter a number.</span></span>
    * <span data-ttu-id="0de54-121">عندما تقوم بجدولة الوظائف والعمليات، يمكنك تحديد ما إذا كان سيتم تحديد الموارد حسب الأولوية.</span><span class="sxs-lookup"><span data-stu-id="0de54-121">When you schedule jobs and operations, you can specify whether to select resources by priority.</span></span> <span data-ttu-id="0de54-122">إذا اخترت القيام بذلك، وكان باستطاعة أكثر من مورد واحد تنفيذ الوظيفة أو العملية في الموعد المطلوب، سيتم تحديد المورد الذي لديه أدنى أولوية فيما يتعلق بالقدرة اللازمة.</span><span class="sxs-lookup"><span data-stu-id="0de54-122">If you choose to do this, and more than one resource can perform the job or operation by the requested date, the resource that has the lowest priority with respect to the required capability is selected.</span></span>  
5. <span data-ttu-id="0de54-123">في حقل "المستوى"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="0de54-123">In the Level field, enter a number.</span></span>
    * <span data-ttu-id="0de54-124">عندما تحدد أن وظيفة أو عملية تحتاج إلى قدرة معينة، يمكنك أيضًا تحديد المستوى الأدنى المطلوب.</span><span class="sxs-lookup"><span data-stu-id="0de54-124">When you specify that a job or operation requires a particular capability, you can also specify the minimum level that is required.</span></span> <span data-ttu-id="0de54-125">استخدم مستوى القدرة للتمييز بين الموارد التي يمكنها تنفيذ نفس الوظيفة، ولكن بسرعات ونقاط القوة وأحجام مختلفة وهكذا.</span><span class="sxs-lookup"><span data-stu-id="0de54-125">Use the capability level to differentiate resources that can perform the same job, but at different speeds, strengths, sizes, and so on.</span></span>  


