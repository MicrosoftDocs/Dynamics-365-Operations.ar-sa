---
title: إعداد الأذونات لطلب المنتجات بالنيابة عن شخص آخر
description: يشرح هذا الموضوع كيفية منح العاملين الإذن الذي يسمح لهم بإعداد طلبات شراء نيابة عن عاملين آخرين.
author: mkirknel
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqAuthorization, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 145d8a0e341857bf238fc934cd668ff12b8505b8
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421416"
---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a><span data-ttu-id="eff7d-103">إعداد الأذونات لطلب المنتجات بالنيابة عن شخص آخر</span><span class="sxs-lookup"><span data-stu-id="eff7d-103">Set up permissions for ordering products on behalf of someone else</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eff7d-104">يشرح هذا الموضوع كيفية منح العاملين الإذن الذي يسمح لهم بإعداد طلبات شراء نيابة عن عاملين آخرين.</span><span class="sxs-lookup"><span data-stu-id="eff7d-104">This topic explains how to grant workers permission to prepare purchase requisitions on behalf of other workers.</span></span> <span data-ttu-id="eff7d-105">بمعنى آخر، بإمكان "معد" طلب شراء إنشاء طلب من أجل "طالب" آخر.</span><span class="sxs-lookup"><span data-stu-id="eff7d-105">In other words, a purchase requisition "preparer" can create a requisition for another "requester."</span></span> <span data-ttu-id="eff7d-106">يبين الإجراء أيضًا كيفية منح أذونات لأحد العاملين لطلب أصناف وخدمات في كيانات قانونية أو وحدات تشغيل مختلفة.</span><span class="sxs-lookup"><span data-stu-id="eff7d-106">The procedure also shows how to grant a worker permission to order items and services in different legal entities or operating units.</span></span> <span data-ttu-id="eff7d-107">يقوم مدير المشتريات عادةً بتنفيذ هذه المهام.</span><span class="sxs-lookup"><span data-stu-id="eff7d-107">Typically, these tasks are performed by a purchasing manager.</span></span> <span data-ttu-id="eff7d-108">يمكنك استخدام هذا الإجراء إما على بيانات خاصة بشركة بيانات العرض التوضيحي USMF أو على بياناتك الخاصة.</span><span class="sxs-lookup"><span data-stu-id="eff7d-108">You can use this procedure either on data for the USMF demo company or on your own data.</span></span>


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a><span data-ttu-id="eff7d-109">منح الإذن لإدخال طلبات الشراء بالنيابة عن عامل آخر</span><span class="sxs-lookup"><span data-stu-id="eff7d-109">Grant permission to enter purchase requisitions on behalf of another worker</span></span>
1. <span data-ttu-id="eff7d-110">في جزء التنقل، انتقل إلى **الوحدات النمطية > التدبير والتوريد‬ > الإعداد > السياسات > أذونات طلبات الشراء**.</span><span class="sxs-lookup"><span data-stu-id="eff7d-110">In the navigation pane, go to **Modules > Procurement and sourcing > Setup > Policies > Purchase requisition permissions**.</span></span> <span data-ttu-id="eff7d-111">تأكد من تعيين حقل **طريقة العرض الحالية** إلى **حسب المُعِد**.</span><span class="sxs-lookup"><span data-stu-id="eff7d-111">Make sure that the **Current view** field is set to **By preparer**.</span></span> <span data-ttu-id="eff7d-112">تعرض القائمة في الجزء الأيمن الأشخاص الذين يمكن منحهم الإذن لتجهيز طلبات نيابة عن أشخاص آخرين.</span><span class="sxs-lookup"><span data-stu-id="eff7d-112">The list in the left pane shows the people who can be granted permission to prepare requisitions on behalf of other people.</span></span>  
2. <span data-ttu-id="eff7d-113">حدد الشخص الذي تريد منحه الإذن (المُعِد).</span><span class="sxs-lookup"><span data-stu-id="eff7d-113">Select the person to grant permission to (the preparer).</span></span>
3. <span data-ttu-id="eff7d-114">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="eff7d-114">Select **Add**.</span></span>
4. <span data-ttu-id="eff7d-115">ابحث عن الشخص لإضافته كطالب وحدده.</span><span class="sxs-lookup"><span data-stu-id="eff7d-115">Find and select the person to add as a requester.</span></span>
    - <span data-ttu-id="eff7d-116">الطالب هو الشخص الذي يستطيع المُعِد إنشاء طلبات بالنيابة عنه.</span><span class="sxs-lookup"><span data-stu-id="eff7d-116">The requester is the person that the preparer can create requisitions on behalf of.</span></span>  
    - <span data-ttu-id="eff7d-117">في حقل **التخويل**، حدد **محدد‬** إذا كان يتوجب على المُعِد أن يكون قادرًا على إنشاء طلبات شراء نيابة عن العامل المحدد.</span><span class="sxs-lookup"><span data-stu-id="eff7d-117">In the **Authorization** field, select **Specific** if the preparer should be able to create purchase requisitions on behalf of the selected worker.</span></span> <span data-ttu-id="eff7d-118">حدد **إعداد التقارير** إذا كان يتوجب على المُعِد أيضًا أن يكون قادرًا على إنشاء طلبات شراء نيابة عن جميع العاملين الذين يقدمون التقارير إلى هذا العامل.</span><span class="sxs-lookup"><span data-stu-id="eff7d-118">Select **Reporting** if the preparer should also be able to create purchase requisitions on behalf of all workers who report to that worker.</span></span>  
5. <span data-ttu-id="eff7d-119">أدخل تاريخًا في الحقل **سارٍ**.</span><span class="sxs-lookup"><span data-stu-id="eff7d-119">In the **Effective** field, enter a date.</span></span>
6. <span data-ttu-id="eff7d-120">في الحقل **تاريخ انتهاء الصلاحية**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="eff7d-120">In the **Expiration** field, enter a date.</span></span>

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a><span data-ttu-id="eff7d-121">عرض المُعدين الذين لديهم إذن إنشاء طلبات الشراء لعامل محدد</span><span class="sxs-lookup"><span data-stu-id="eff7d-121">View preparers who have permission to create purchase requisitions for a selected worker</span></span>
1. <span data-ttu-id="eff7d-122">في حقل **طريقة العرض الحالية**، حدد **حسب الطالب**.</span><span class="sxs-lookup"><span data-stu-id="eff7d-122">In the **Current view** field, select **By requester**.</span></span> <span data-ttu-id="eff7d-123">تُظهر طريقة العرض هذه قائمة المُعِدين الذين تم منحهم أذونات لإنشاء طلبات الشراء بالنيابة عن عامل محدد.</span><span class="sxs-lookup"><span data-stu-id="eff7d-123">This view shows a list of preparers who have been granted permission to create purchase requisitions on behalf of a selected worker.</span></span>  
2. <span data-ttu-id="eff7d-124">استخدم "عامل التصفية السريع" للبحث عن العامل الذي قمت بإضافته كطالب.</span><span class="sxs-lookup"><span data-stu-id="eff7d-124">Use the Quick Filter to find the worker that you just added as the requester.</span></span>
3. <span data-ttu-id="eff7d-125">حدد الطالب.</span><span class="sxs-lookup"><span data-stu-id="eff7d-125">Select the requester.</span></span> <span data-ttu-id="eff7d-126">تعرض قائمة المُعِدين الأشخاص الذين لديهم الإذن لطلب أصناف بالنيابة عن الطالب الذي تم تحديده في الجزء الأيمن.</span><span class="sxs-lookup"><span data-stu-id="eff7d-126">The Preparer list shows the people who have permission to order items on behalf of the requester who is selected in the left pane.</span></span>  <span data-ttu-id="eff7d-127">يمكنك إضافة المزيد من المُعِدين هنا.</span><span class="sxs-lookup"><span data-stu-id="eff7d-127">You can add additional preparers here.</span></span> <span data-ttu-id="eff7d-128">كما تتيح لك طريقة العرض هذه منح الطالب إذنًا يسمح له بإنشاء طلبات في كيانات قانونية ووحدات تشغيل ليست الكيان القانوني الأساسي أو وحدة التشغيل الأساسية لذلك الشخص.</span><span class="sxs-lookup"><span data-stu-id="eff7d-128">This view also lets you grant the requester permission to create requisitions in legal entities and operating units that aren't that person's primary legal entity or operating unit.</span></span>  

