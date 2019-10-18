---
title: الاحتفاظ بالأوامر المخططة
description: تقدم هذا الموضوع معلومات حول الأوامر المخططة. وهي تصف كيف يمكنك تحديث حالة الأوامر المخططة وتأكيدها وتصفية الأوامر المخططة ذات الحالة نفسها لأمر مخطط محدد.
author: roxanadiaconu
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ddf2c7b4c67bec6c29387c78d1fdb021d85d702
ms.sourcegitcommit: 620e15555d176eec3905b48d5001af1c50107ce6
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/09/2019
ms.locfileid: "1993430"
---
# <a name="maintain-planned-orders"></a><span data-ttu-id="f3671-104">الاحتفاظ بالأوامر المخططة</span><span class="sxs-lookup"><span data-stu-id="f3671-104">Maintain planned orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f3671-105">تقدم هذا الموضوع معلومات حول الأوامر المخططة.</span><span class="sxs-lookup"><span data-stu-id="f3671-105">This topic provides information about how to manage planned orders.</span></span> <span data-ttu-id="f3671-106">وهي تصف كيف يمكنك تحديث حالة الأوامر المخططة وتأكيدها وتصفية الأوامر المخططة ذات الحالة نفسها لأمر مخطط محدد.</span><span class="sxs-lookup"><span data-stu-id="f3671-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="f3671-107">يمكنك إدارة الأوامر المخططة من مساحة عمل **التخطيط الرئيسي**، أو قائمة **الأمر المخطط**، أو قوائم **أوامر الإنتاج المخططة**، و**أوامر الشراء المخططة**، و**التحويل المخطط**.</span><span class="sxs-lookup"><span data-stu-id="f3671-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> 

## <a name="planned-order-status"></a><span data-ttu-id="f3671-108">حالة الأمر المخطط</span><span class="sxs-lookup"><span data-stu-id="f3671-108">Planned order status</span></span>
<span data-ttu-id="f3671-109">يمكنك استخدام حقل **الحالة** للمساعدة في تتبع تقدمك.</span><span class="sxs-lookup"><span data-stu-id="f3671-109">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="f3671-110">يتم استخدام القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="f3671-110">The following values are used:</span></span>

-   <span data-ttu-id="f3671-111">عندما يُنشئ التخطيط الرئيسي أوامر مخططة، تكون حالة الأوامر المخططة **غير معالجة**.</span><span class="sxs-lookup"><span data-stu-id="f3671-111">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="f3671-112">وإذا قررت عدم تأكيد أمر مخطط، فيمكنك منحه الحالة **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="f3671-112">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="f3671-113">إذا كنت ترغب في تأكيد أمر مخطط، يُمكنك تغيير الحالة إلى **موافق عليه**.</span><span class="sxs-lookup"><span data-stu-id="f3671-113">If you want to firm a planned order, you can change the status to **Approved**.</span></span> <span data-ttu-id="f3671-114">ويتم مراعاة الأوامر المُخططة التي لها حالة **موافق عليه** من خلال التخطيط الرئيسي، بحيث لا يتم تعديلها أو حذفها.</span><span class="sxs-lookup"><span data-stu-id="f3671-114">Planned orders with **Approved** status are respected by master planning, so they are not modified or deleted.</span></span> 

## <a name="firming-planned-orders"></a><span data-ttu-id="f3671-115">تأكيد الأوامر المخططة</span><span class="sxs-lookup"><span data-stu-id="f3671-115">Firming planned orders</span></span> 
<span data-ttu-id="f3671-116">ومن خلال تأكيد الأوامر المخططة، يتم إنشاء الأوامر الحقيقية.</span><span class="sxs-lookup"><span data-stu-id="f3671-116">By firming planned orders, real orders are created.</span></span> <span data-ttu-id="f3671-117">وهي تُعرف أيضًا باسم *مُصدرة* أو *أوامر مفتوحة*.</span><span class="sxs-lookup"><span data-stu-id="f3671-117">These are also know as *released* or *open orders*.</span></span> <span data-ttu-id="f3671-118">عند تأكيد أمر مخطط، يتم نقله إلى مقطع الأوامر في الوحدة النمطية ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="f3671-118">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span>

<span data-ttu-id="f3671-119">يُمكنك تحديد خيارين تأكيد من صفحة **الأوامر المخططة**:</span><span class="sxs-lookup"><span data-stu-id="f3671-119">You can select two firming options from the **Planned orders** page:</span></span>

-   <span data-ttu-id="f3671-120">**تأكيد**- سوف يؤكد هذا على أمر واحد أو عدة أوامر مخططة مُحددة.</span><span class="sxs-lookup"><span data-stu-id="f3671-120">**Firm** – This will firm one or multiple selected planned orders.</span></span>
-   <span data-ttu-id="f3671-121">**تأكيد الكل** -سوف يؤكد هذا جميع الأوامر المخططة في عامل التصفية.</span><span class="sxs-lookup"><span data-stu-id="f3671-121">**Firm all** – This will firm all planned orders in the filter.</span></span> <span data-ttu-id="f3671-122">باستخدام **تأكيد الكل** فلن تكون مُضطرًا لتحديد الأمر المخطط، حيث سوف يتم تأكيد جميع الأوامر المخططة الموجودة في عامل التصفية.</span><span class="sxs-lookup"><span data-stu-id="f3671-122">Using **Firm all** you don’t have to select the planned order, all planned orders within the filter will be firmed.</span></span> <span data-ttu-id="f3671-123">وقد يكون هذا الخيار مُفيدّا إذا كنت تقوم بتأكيد عدد كبير من الأوامر المخططة.</span><span class="sxs-lookup"><span data-stu-id="f3671-123">This option can be useful if you are firming a high number of planned orders.</span></span>

> [!NOTE]
> <span data-ttu-id="f3671-124">يُمكنك تتبع أمر مخطط تم تأكيده من **سجل التأكيد** الموجود في **نموذج الأوامر المخططة > عرض >  سجل التأكيد**.</span><span class="sxs-lookup"><span data-stu-id="f3671-124">You can track a planned order that was firmed from **Firming history** under **Planned orders form > View > Firming history**.</span></span>

## <a name="parallelize-firming"></a><span data-ttu-id="f3671-125">موازاة التأكيد</span><span class="sxs-lookup"><span data-stu-id="f3671-125">Parallelize firming</span></span>
<span data-ttu-id="f3671-126">إذا كنت تخطط لتأكيد عدة أوامر في الوقت نفسه، فإن التوازي يُمكنه تحسين وقت التشغيل أو الأداء.</span><span class="sxs-lookup"><span data-stu-id="f3671-126">If you are planning to firm many orders at the same time, parallelizing the run can improve the run time or performance.</span></span> <span data-ttu-id="f3671-127">يتوفر هذا الخيار عند تأكيد عدة أوامر مخططة إما باستخدام **تأكيد** أو **تأكيد الكل**.</span><span class="sxs-lookup"><span data-stu-id="f3671-127">This option is available when firming multiple planned orders with either **Firm** or **Firm all**.</span></span> <span data-ttu-id="f3671-128">تتوفر المعلمات التالية:</span><span class="sxs-lookup"><span data-stu-id="f3671-128">The following parameters are available:</span></span>

-   <span data-ttu-id="f3671-129">**تأكيد متوازي**- إذا كان الخيار هو **نعم**، فسوف يتم موازة عملية التأكيد مع عدد السلاسل المُحددة في **عدد السلاسل**.</span><span class="sxs-lookup"><span data-stu-id="f3671-129">**Parallelize firming** – If **Yes**, the firming process will be parallelized with the number of threads defined in **Number of threads**.</span></span>
-   <span data-ttu-id="f3671-130">**عدد السلاسل**- يتحكم في عدد السلاسل المستخدمة لموازة عملية التأكيد.</span><span class="sxs-lookup"><span data-stu-id="f3671-130">**Number of threads** – Controls the number of threads used to parallelize the firming process.</span></span> <span data-ttu-id="f3671-131">تظهر المُعلمة فقط عندما يتم تعيين **تأكيد موازي** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="f3671-131">The parameter is only shown when **Parallelize firming** is set to **Yes**.</span></span>


<a name="additional-resources"></a><span data-ttu-id="f3671-132">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="f3671-132">Additional resources</span></span>
--------

[<span data-ttu-id="f3671-133">الخطط الرئيسية</span><span class="sxs-lookup"><span data-stu-id="f3671-133">Master plans</span></span>](master-plans.md)



