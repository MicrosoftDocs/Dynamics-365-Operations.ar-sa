--- 
title: "تحديد مجموعة الموارد التصنيع المنفصلة"
description: "مجموعة الموارد هي مجموعة من موارد العمليات تتطابق عادة مع التنظيم المادي لخلايا العمل، المعرفة بخطوط صفراء في صالة الإنتاج."
author: sorenva
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: e1be950a7d1d7548aced041a189222b472d767cf
ms.contentlocale: ar-sa
ms.lasthandoff: 08/07/2018

---
# <a name="define-discrete-manufacturing-resource-group"></a><span data-ttu-id="9d1e1-103">تحديد مجموعة الموارد التصنيع المنفصلة</span><span class="sxs-lookup"><span data-stu-id="9d1e1-103">Define discrete manufacturing resource group</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9d1e1-104">مجموعة الموارد هي مجموعة من موارد العمليات تتطابق عادة مع التنظيم المادي لخلايا العمل، المعرفة بخطوط صفراء في صالة الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="9d1e1-104">A resource group is a set of operations resources that typically correspond to the physical organization of work cells, defined by yellow lines on the production shop floor.</span></span> <span data-ttu-id="9d1e1-105">يوضح هذا الإجراء كيفية تعريف مجموعة موارد لاستخدامها في عملية إنتاج منفصلة.</span><span class="sxs-lookup"><span data-stu-id="9d1e1-105">This procedure shows you how to define a resource group for use in discrete production.</span></span> <span data-ttu-id="9d1e1-106">يمكنك استعراض هذا الإجراء في شركة بيانات العرض التوضيحي USMF، أو باستخدام البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="9d1e1-106">You can walk through this procedure in demo data company USMF, or use your own data.</span></span>

1. <span data-ttu-id="9d1e1-107">انتقل إلى مجموعات الموارد.</span><span class="sxs-lookup"><span data-stu-id="9d1e1-107">Go to Resource groups.</span></span>
2. <span data-ttu-id="9d1e1-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="9d1e1-108">Click New.</span></span>
3. <span data-ttu-id="9d1e1-109">في حقل مجموعة "الموارد"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="9d1e1-109">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="9d1e1-110">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="9d1e1-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9d1e1-111">في حقل "الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="9d1e1-111">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="9d1e1-112">في حقل وحدة "الإنتاج"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="9d1e1-112">In the Production unit field, enter or select a value.</span></span>

## <a name="define-default-operational-parameters"></a><span data-ttu-id="9d1e1-113">تعريف محددات التشغيل الافتراضية</span><span class="sxs-lookup"><span data-stu-id="9d1e1-113">Define default operational parameters</span></span>
1. <span data-ttu-id="9d1e1-114">وسّع مقطع "العملية".</span><span class="sxs-lookup"><span data-stu-id="9d1e1-114">Expand the Operation section.</span></span>
2. <span data-ttu-id="9d1e1-115">في حقل النسبة المئوية للخردة، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="9d1e1-115">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="9d1e1-116">في حقل فئة "الإعداد"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="9d1e1-116">In the Setup category field, enter or select a value.</span></span>
4. <span data-ttu-id="9d1e1-117">في حقل "وقت التشغيل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="9d1e1-117">In the Run time category field, enter or select a value.</span></span>
5. <span data-ttu-id="9d1e1-118">في حقل النسبة المئوية لجدولة العمليات، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="9d1e1-118">In the Operations scheduling percentage field, enter a number.</span></span>

## <a name="define-operating-hours"></a><span data-ttu-id="9d1e1-119">تحديد ساعات التشغيل</span><span class="sxs-lookup"><span data-stu-id="9d1e1-119">Define operating hours</span></span>
1. <span data-ttu-id="9d1e1-120">وسّع مقطع "التقويمات".</span><span class="sxs-lookup"><span data-stu-id="9d1e1-120">Expand the Calendars section.</span></span>
2. <span data-ttu-id="9d1e1-121">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="9d1e1-121">Click Add.</span></span>
3. <span data-ttu-id="9d1e1-122">في حقل "التقويم"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="9d1e1-122">In the Calendar field, enter or select a value.</span></span>

## <a name="add-operations-resources"></a><span data-ttu-id="9d1e1-123">إضافة موارد العمليات</span><span class="sxs-lookup"><span data-stu-id="9d1e1-123">Add operations resources</span></span>
1. <span data-ttu-id="9d1e1-124">وسّع مقطع "الموارد".</span><span class="sxs-lookup"><span data-stu-id="9d1e1-124">Expand the Resources section.</span></span>
2. <span data-ttu-id="9d1e1-125">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="9d1e1-125">Click Add.</span></span>
3. <span data-ttu-id="9d1e1-126">في حقل "المورد"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="9d1e1-126">In the Resource field, enter or select a value.</span></span>
4. <span data-ttu-id="9d1e1-127">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="9d1e1-127">Click Add.</span></span>
5. <span data-ttu-id="9d1e1-128">في حقل "المورد"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="9d1e1-128">In the Resource field, enter or select a value.</span></span>
6. <span data-ttu-id="9d1e1-129">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="9d1e1-129">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="9d1e1-130">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="9d1e1-130">In the list, click the link in the selected row.</span></span>


