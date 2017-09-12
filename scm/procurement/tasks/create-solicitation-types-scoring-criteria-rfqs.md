--- 
title: "إنشاء أنواع طلبات ومعايير تسجيل النقاط‬ لطلبات عروض الأسعار"
description: "يوضح هذا الدليل كيفية إنشاء نوع طلب وربطه بأسلوب تسجيل النقاط."
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 095855d552d228375635bdbaa9fca37c47a3b952
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a><span data-ttu-id="25083-103">إنشاء أنواع طلبات ومعايير تسجيل النقاط‬ لطلبات عروض الأسعار</span><span class="sxs-lookup"><span data-stu-id="25083-103">Create solicitation types and scoring criteria for RFQs</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="25083-104">يوضح هذا الدليل كيفية إنشاء نوع طلب وربطه بأسلوب تسجيل النقاط.</span><span class="sxs-lookup"><span data-stu-id="25083-104">This guide shows you how to create a solicitation type and associate this with a scoring method.</span></span> <span data-ttu-id="25083-105">ويُظهر أيضًا كيفية استخدام نوع الطلب على طلب عرض أسعار (RFQ) الذي يعيّن عندئذٍ أسلوب تسجيل النقاط الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="25083-105">It also shows how to use the solicitation type on a request for quotation (RFQ) which then sets the default scoring method.</span></span> <span data-ttu-id="25083-106">يقوم عادةً مدير المشتريات بتنفيذ هذه المهام.</span><span class="sxs-lookup"><span data-stu-id="25083-106">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="25083-107">يمكنك استخدام هذا الإجراء في شركة بيانات العرض التقديمي USMF، أو في البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="25083-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="25083-108">يجب أن يكون لديك أسلوب تسجيل نقاط قبل البدء.</span><span class="sxs-lookup"><span data-stu-id="25083-108">You need to have a scoring method available before you start.</span></span>


## <a name="create-a-solicitation-type"></a><span data-ttu-id="25083-109">إنشاء نوع طلب</span><span class="sxs-lookup"><span data-stu-id="25083-109">Create a solicitation type</span></span>
1. <span data-ttu-id="25083-110">انتقل إلى التدبير وتحديد الموارد > إعداد > طلب عرض أسعار > نوع الطلب.</span><span class="sxs-lookup"><span data-stu-id="25083-110">Go to Procurement and sourcing > Setup > Request for quotation > Solicitation type.</span></span>
2. <span data-ttu-id="25083-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="25083-111">Click New.</span></span>
3. <span data-ttu-id="25083-112">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="25083-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="25083-113">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="25083-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="25083-114">في حقل "أسلوب تسجيل النقاط"، حدد أسلوب تسجيل النقاط الذي تريد استخدامه لنوع الطلب هذا.</span><span class="sxs-lookup"><span data-stu-id="25083-114">In the Scoring method field, select the scoring method that you want to use for this solicitation type.</span></span>
6. <span data-ttu-id="25083-115">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="25083-115">Click Save.</span></span>
7. <span data-ttu-id="25083-116">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="25083-116">Close the page.</span></span>

## <a name="use-the-solicitation-type"></a><span data-ttu-id="25083-117">استخدام نوع الطلب</span><span class="sxs-lookup"><span data-stu-id="25083-117">Use the solicitation type</span></span>
1. <span data-ttu-id="25083-118">انتقل إلى التدبير وتحديد الموارد > طلبات عروض الأسعار‬ > كل طلبات عروض الأسعار‬.</span><span class="sxs-lookup"><span data-stu-id="25083-118">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="25083-119">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="25083-119">Click New.</span></span>
3. <span data-ttu-id="25083-120">في الحقل "نوع الطلب"، حدد نوع الطلب الذي قمت بإنشائه للتوّ.</span><span class="sxs-lookup"><span data-stu-id="25083-120">In the Solicitation type field, select the solicitation type that you have just created.</span></span> 
4. <span data-ttu-id="25083-121">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="25083-121">Click OK.</span></span>
5. <span data-ttu-id="25083-122">انقر فوق "معايير تسجيل النقاط".</span><span class="sxs-lookup"><span data-stu-id="25083-122">Click Scoring criteria.</span></span>
    * <span data-ttu-id="25083-123">معايير تسجيل النقاط التي تظهر هي تلك المعايير الخاصة بأسلوب تسجيل النقاط المقترن بنوع الطلب.</span><span class="sxs-lookup"><span data-stu-id="25083-123">The scoring criteria that are shown are the ones from the scoring method that you associated with the solicitation type.</span></span> <span data-ttu-id="25083-124">يمكنك اختيار إضافة معايير أو حذفها في هذه الصفحة.</span><span class="sxs-lookup"><span data-stu-id="25083-124">You can choose to add or delete criteria on this page.</span></span> <span data-ttu-id="25083-125">من الممكن أيضًا إضافة معايير جديدة عن طريق نسخها من أساليب أخرى لتسجيل النقاط.</span><span class="sxs-lookup"><span data-stu-id="25083-125">It's also possible to add new criteria by copying them from other scoring methods.</span></span>  
6. <span data-ttu-id="25083-126">انقر فوق "نسخ المعايير".</span><span class="sxs-lookup"><span data-stu-id="25083-126">Click Copy criteria.</span></span>
7. <span data-ttu-id="25083-127">في الحقل "أسلوب تسجيل النقاط"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="25083-127">In the Scoring method field, enter or select a value.</span></span>
8. <span data-ttu-id="25083-128">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="25083-128">Click OK.</span></span>
9. <span data-ttu-id="25083-129">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="25083-129">Close the page.</span></span>


