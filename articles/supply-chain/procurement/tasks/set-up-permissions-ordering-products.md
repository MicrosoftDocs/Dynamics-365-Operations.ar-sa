--- 
title: "إعداد الأذونات لطلب المنتجات بالنيابة عن شخص آخر"
description: "يوضح هذا الإجراء كيفية منح العاملين الإذن الذي يسمح لهم بإعداد طلبات شراء نيابة عن عاملين آخرين."
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchReqAuthorization, HcmWorkerLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 35688d191cef06cc15251a6e10a2e8c9afb0e08b
ms.contentlocale: ar-sa
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a><span data-ttu-id="1e772-103">إعداد الأذونات لطلب المنتجات بالنيابة عن شخص آخر</span><span class="sxs-lookup"><span data-stu-id="1e772-103">Set up permissions for ordering products on behalf of someone else</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1e772-104">يوضح هذا الإجراء كيفية منح العاملين الإذن الذي يسمح لهم بإعداد طلبات شراء نيابة عن عاملين آخرين.</span><span class="sxs-lookup"><span data-stu-id="1e772-104">This procedure shows how to grant workers permission to prepare purchase requisitions on behalf of other workers.</span></span> <span data-ttu-id="1e772-105">بمعنى آخر، بإمكان "معد" طلب شراء إنشاء طلب من أجل "طالب" آخر.</span><span class="sxs-lookup"><span data-stu-id="1e772-105">In other words, a purchase requisition “preparer” can create a requisition for another “requester.”</span></span> <span data-ttu-id="1e772-106">يبين الإجراء أيضًا كيفية منح أذونات لأحد العاملين لطلب أصناف وخدمات في كيانات قانونية أو وحدات تشغيل مختلفة.</span><span class="sxs-lookup"><span data-stu-id="1e772-106">The procedure also shows how to grant a worker permission to order items and services in different legal entities or operating units.</span></span> <span data-ttu-id="1e772-107">يقوم مدير المشتريات عادةً بتنفيذ هذه المهام.</span><span class="sxs-lookup"><span data-stu-id="1e772-107">Typically, these tasks are performed by a purchasing manager.</span></span> <span data-ttu-id="1e772-108">يمكنك استخدام هذا الإجراء إما على بيانات خاصة بشركة بيانات العرض التوضيحي USMF أو على بياناتك الخاصة.</span><span class="sxs-lookup"><span data-stu-id="1e772-108">You can use this procedure either on data for the USMF demo company or on your own data.</span></span>


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a><span data-ttu-id="1e772-109">منح الإذن لإدخال طلبات الشراء بالنيابة عن عامل آخر</span><span class="sxs-lookup"><span data-stu-id="1e772-109">Grant permission to enter purchase requisitions on behalf of another worker</span></span>
1. <span data-ttu-id="1e772-110">انتقل إلى التدبير وتحديد الموارد > إعداد > السياسات > أذونات طلبات الشراء.</span><span class="sxs-lookup"><span data-stu-id="1e772-110">Go to Procurement and sourcing > Setup > Policies > Purchase requisition permissions.</span></span>
    * <span data-ttu-id="1e772-111">تأكد من تعيين حقل "طريقة العرض الحالية" إلى "حسب المُعِد".</span><span class="sxs-lookup"><span data-stu-id="1e772-111">Make sure that the Current view field is set to By preparer.</span></span>  <span data-ttu-id="1e772-112">تعرض القائمة في الجزء الأيمن الأشخاص الذين يمكن منحهم الإذن لتجهيز طلبات نيابة عن أشخاص آخرين.</span><span class="sxs-lookup"><span data-stu-id="1e772-112">The list in the left pane shows the people who can be granted permission to prepare requisitions on behalf of other people.</span></span>  
2. <span data-ttu-id="1e772-113">حدد الشخص الذي تريد منحه الإذن (المُعِد).</span><span class="sxs-lookup"><span data-stu-id="1e772-113">Select the person to grant permission to (the preparer).</span></span>
3. <span data-ttu-id="1e772-114">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="1e772-114">Click Add.</span></span>
4. <span data-ttu-id="1e772-115">ابحث عن الشخص لإضافته كطالب وحدده.</span><span class="sxs-lookup"><span data-stu-id="1e772-115">Find and select the person to add as a requester.</span></span>
    * <span data-ttu-id="1e772-116">الطالب هو الشخص الذي يستطيع المُعِد إنشاء طلبات بالنيابة عنه.</span><span class="sxs-lookup"><span data-stu-id="1e772-116">The requester is the person that the preparer can create requisitions on behalf of.</span></span>  
    * <span data-ttu-id="1e772-117">في حقل "التخويل"، حدد "محدد‬" إذا كان يتوجب على المُعِد أن يكون قادرًا على إنشاء طلبات شراء نيابة عن العامل المحدد.</span><span class="sxs-lookup"><span data-stu-id="1e772-117">In the Authorization field, select Specific if the preparer should be able to create purchase requisitions on behalf of the selected worker.</span></span> <span data-ttu-id="1e772-118">حدد "إعداد التقارير" إذا كان يتوجب على المُعِد أيضًا أن يكون قادرًا على إنشاء طلبات شراء نيابة عن جميع العاملين الذين يقدمون التقارير إلى هذا العامل.</span><span class="sxs-lookup"><span data-stu-id="1e772-118">Select Reporting if the preparer should also be able to create purchase requisitions on behalf of all workers who report to that worker.</span></span>  
5. <span data-ttu-id="1e772-119">في الحقل سارٍ، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="1e772-119">In the Effective field, enter a date.</span></span>
6. <span data-ttu-id="1e772-120">في الحقل "تاريخ انتهاء الصلاحية"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="1e772-120">In the Expiration field, enter a date.</span></span>

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a><span data-ttu-id="1e772-121">عرض المُعدين الذين لديهم إذن إنشاء طلبات الشراء لعامل محدد</span><span class="sxs-lookup"><span data-stu-id="1e772-121">View preparers who have permission to create purchase requisitions for a selected worker</span></span>
1. <span data-ttu-id="1e772-122">في حقل طريقة العرض الحالية، حدد "حسب الطالب".</span><span class="sxs-lookup"><span data-stu-id="1e772-122">In the Current view field, select 'By requester'.</span></span>
    * <span data-ttu-id="1e772-123">تُظهر طريقة العرض هذه قائمة المُعِدين الذين تم منحهم أذونات لإنشاء طلبات الشراء بالنيابة عن عامل محدد.</span><span class="sxs-lookup"><span data-stu-id="1e772-123">This view shows a list of preparers who have been granted permission to create purchase requisitions on behalf of a selected worker.</span></span>  
2. <span data-ttu-id="1e772-124">استخدم "عامل التصفية السريع" للبحث عن العامل الذي قمت بإضافته كطالب.</span><span class="sxs-lookup"><span data-stu-id="1e772-124">Use the Quick Filter to find the worker that you just added as the requester.</span></span>
3. <span data-ttu-id="1e772-125">حدد الطالب.</span><span class="sxs-lookup"><span data-stu-id="1e772-125">Select the requester.</span></span>
    * <span data-ttu-id="1e772-126">تعرض قائمة المُعِدين الأشخاص الذين لديهم الإذن لطلب أصناف بالنيابة عن الطالب الذي تم تحديده في الجزء الأيمن.</span><span class="sxs-lookup"><span data-stu-id="1e772-126">The Preparer list shows the people who have permission to order items on behalf of the requester who is selected in the left pane.</span></span>   <span data-ttu-id="1e772-127">يمكنك إضافة المزيد من المُعِدين هنا.</span><span class="sxs-lookup"><span data-stu-id="1e772-127">You can add additional preparers here.</span></span>   <span data-ttu-id="1e772-128">كما تتيح لك طريقة العرض هذه منح الطالب إذنًا يسمح له بإنشاء طلبات في كيانات قانونية ووحدات تشغيل ليست الكيان القانوني الأساسي أو وحدة التشغيل الأساسية لذلك الشخص.</span><span class="sxs-lookup"><span data-stu-id="1e772-128">This view also lets you grant the requester permission to create requisitions in legal entities and operating units that aren't that person's primary legal entity or operating unit.</span></span>  


