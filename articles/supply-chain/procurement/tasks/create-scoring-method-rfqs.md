--- 
title: "إنشاء أسلوب تسجيل النقاط لطلبات عروض الأسعار"
description: "يوضح هذا الإجراء كيفية إنشاء أسلوب تسجيل النقاط."
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: c432649f22be344d1cb27304edd837727507b35d
ms.contentlocale: ar-sa
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-scoring-method-for-rfqs"></a><span data-ttu-id="c5ab0-103">إنشاء أسلوب تسجيل النقاط لطلبات عروض الأسعار</span><span class="sxs-lookup"><span data-stu-id="c5ab0-103">Create a scoring method for RFQs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c5ab0-104">يوضح هذا الإجراء كيفية إنشاء أسلوب تسجيل النقاط.</span><span class="sxs-lookup"><span data-stu-id="c5ab0-104">This procedure shows you how to create a scoring method.</span></span> <span data-ttu-id="c5ab0-105">إن أسلوب تسجيل النقاط عبارة عن مجموعة من المعايير التي يمكن استخدامها لمقارنة العطاءات التي تم إرسالها في الرد على طلب عرض الأسعار (RFQ).</span><span class="sxs-lookup"><span data-stu-id="c5ab0-105">A scoring method is a set of criteria that can be used to compare bids that are sent in reply to a request for quotation (RFQ).</span></span> <span data-ttu-id="c5ab0-106">على سبيل المثال، قد تريد تقييم مورّد على أدائه السابق، أو تقييم مستوى صداقة البيئة لدى الشركة أو مستوى تعاونها، أو قد ترغب في مقارنة العطاءات استنادًا إلى السعر.</span><span class="sxs-lookup"><span data-stu-id="c5ab0-106">For example, you might want to rate a vendor on past performance, or rate whether the company is environmentally friendly or a good collaborator, or you might want to compare bids based on price.</span></span> <span data-ttu-id="c5ab0-107">يمكن إقران أسلوب تسجيل النقاط بنوع الطلب كأسلوب تسجيل النقاط الافتراضي لطلبات عرض الأسعار من ذلك النوع.</span><span class="sxs-lookup"><span data-stu-id="c5ab0-107">The scoring method can be associated with a solicitation type as the default scoring method for RFQs of that type.</span></span> <span data-ttu-id="c5ab0-108">يقوم عادةً مدير المشتريات بتنفيذ هذه المهام.</span><span class="sxs-lookup"><span data-stu-id="c5ab0-108">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="c5ab0-109">يمكنك استخدام هذا الإجراء في شركة بيانات العرض التقديمي USMF، أو في البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="c5ab0-109">You can use this procedure in demo data company USMF or on your own data.</span></span>

1. <span data-ttu-id="c5ab0-110">انتقل إلى التدبير وتحديد الموارد > إعداد > طلب عرض أسعار > أسلوب تسجيل النقاط.</span><span class="sxs-lookup"><span data-stu-id="c5ab0-110">Go to Procurement and sourcing > Setup > Request for quotation > Scoring method.</span></span>
2. <span data-ttu-id="c5ab0-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="c5ab0-111">Click New.</span></span>
3. <span data-ttu-id="c5ab0-112">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c5ab0-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="c5ab0-113">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c5ab0-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="c5ab0-114">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="c5ab0-114">Click Save.</span></span>
6. <span data-ttu-id="c5ab0-115">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="c5ab0-115">Click New.</span></span>
7. <span data-ttu-id="c5ab0-116">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c5ab0-116">In the Name field, type a value.</span></span>
8. <span data-ttu-id="c5ab0-117">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c5ab0-117">In the Description field, type a value.</span></span>
    * <span data-ttu-id="c5ab0-118">يظهر هذا الوصف جنبًا إلى جنب مع اسم أسلوب تسجيل النقاط عندما يتم تحديد أسلوب تسجيل النقاط لطلب عرض الأسعار.</span><span class="sxs-lookup"><span data-stu-id="c5ab0-118">This description is shown along with the scoring method name when a scoring method is selected for an RFQ.</span></span>  
9. <span data-ttu-id="c5ab0-119">في الحقل "بداية النطاق‬‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="c5ab0-119">In the Range from field, enter a number.</span></span>
    * <span data-ttu-id="c5ab0-120">يحدد النطاق ما يستطيع أخصائي التدبير إدخاله كنقاط.</span><span class="sxs-lookup"><span data-stu-id="c5ab0-120">The range limits what the procurement professional can enter as a score.</span></span> <span data-ttu-id="c5ab0-121">عند وجود معايير متعددة لتسجيل النقاط في طلب عرض الأسعار، تضاف النقاط التي تم إدخالها إلى بعضها ويصبح المجموع متوفرًا للسماح بمقارنة العطاءات.</span><span class="sxs-lookup"><span data-stu-id="c5ab0-121">When there are multiple scoring criteria on an RFQ, the scores that have been entered are added to each other and the sum is made available to allow the bids to be compared.</span></span>  
10. <span data-ttu-id="c5ab0-122">في الحقل "نهاية النطاق‬‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="c5ab0-122">In the Range to field, enter a number.</span></span>
11. <span data-ttu-id="c5ab0-123">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="c5ab0-123">Click New.</span></span>
12. <span data-ttu-id="c5ab0-124">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c5ab0-124">In the Name field, type a value.</span></span>
13. <span data-ttu-id="c5ab0-125">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c5ab0-125">In the Description field, type a value.</span></span>
14. <span data-ttu-id="c5ab0-126">في الحقل "بداية النطاق‬‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="c5ab0-126">In the Range from field, enter a number.</span></span>
15. <span data-ttu-id="c5ab0-127">في الحقل "نهاية النطاق‬‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="c5ab0-127">In the Range to field, enter a number.</span></span>


