---
title: تقسيم أصل ثابت
description: يشرح هذا الموضوع كيفية تقسيم نسبة مئوية من دفتر الأصول إلى دفتر أصول جديد.
author: saraschi2
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4e001a6fdf390c6211ba85aa327b60dcdf16d9e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176196"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="ca5e2-103">تقسيم أصل ثابت</span><span class="sxs-lookup"><span data-stu-id="ca5e2-103">Split a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ca5e2-104">يشرح هذا الموضوع كيفية تقسيم نسبة مئوية من دفتر الأصول إلى دفتر أصول جديد.</span><span class="sxs-lookup"><span data-stu-id="ca5e2-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="ca5e2-105">إنه يستخدم دور المحاسب وبيانات العرض التوضيحي USMF.‬</span><span class="sxs-lookup"><span data-stu-id="ca5e2-105">It uses the Accountant role and USMF demo data.</span></span>


## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="ca5e2-106">إنشاء أصل ثابت جديد</span><span class="sxs-lookup"><span data-stu-id="ca5e2-106">Create a new fixed asset</span></span>
1. <span data-ttu-id="ca5e2-107">في جزء التنقل، انتقل إلى **الوحدات النمطية > الأصول الثابتة > الأصول الثابتة > الأصول الثابتة‬**.</span><span class="sxs-lookup"><span data-stu-id="ca5e2-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="ca5e2-108">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="ca5e2-108">Select **New**.</span></span>
3. <span data-ttu-id="ca5e2-109">في حقل **مجموعة الأصول الثابتة**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ca5e2-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="ca5e2-110">لاحظ رقم الأصل الثابت لاستخدامه في عملية التقسيم لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="ca5e2-110">Note the fixed asset number to use in the split process later.</span></span>  
4. <span data-ttu-id="ca5e2-111">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ca5e2-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="ca5e2-112">وقم بغلق النموذج.</span><span class="sxs-lookup"><span data-stu-id="ca5e2-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="ca5e2-113">تقسيم أصل ثابت</span><span class="sxs-lookup"><span data-stu-id="ca5e2-113">Split a fixed asset</span></span>
1. <span data-ttu-id="ca5e2-114">في القائمة، ابحث عن الارتباط إلى الأصل الثابت المراد تقسيمه وحدده.</span><span class="sxs-lookup"><span data-stu-id="ca5e2-114">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="ca5e2-115">حدد **الدفاتر**.</span><span class="sxs-lookup"><span data-stu-id="ca5e2-115">Select **Books**.</span></span> <span data-ttu-id="ca5e2-116">حدد الدفتر لتقسيمه إلى الأصل الجديد.</span><span class="sxs-lookup"><span data-stu-id="ca5e2-116">Select the book to split to the new asset.</span></span>  
3. <span data-ttu-id="ca5e2-117">حدد **الوظائف**.</span><span class="sxs-lookup"><span data-stu-id="ca5e2-117">Select **Functions**.</span></span>
4. <span data-ttu-id="ca5e2-118">حدد **تقسيم الأصل الثابت**.</span><span class="sxs-lookup"><span data-stu-id="ca5e2-118">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="ca5e2-119">في حقل **إلى الأصل الثابت**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ca5e2-119">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="ca5e2-120">في الحقل **إلى دفتر‬**، حدد زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="ca5e2-120">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="ca5e2-121">في حقل **‏‫تاريخ الحركة**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="ca5e2-121">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="ca5e2-122">في الحقل **النسبة‬ المئوية**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="ca5e2-122">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="ca5e2-123">في الحقل **اسم دفتر اليومية**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ca5e2-123">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="ca5e2-124">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ca5e2-124">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="ca5e2-125">ترحيل حركة دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="ca5e2-125">Post the journal transaction</span></span>
1. <span data-ttu-id="ca5e2-126">في جزء التنقل، انتقل إلى **الوحدات النمطية > الأصول الثابتة > إدخالات دفتر اليومية‬ > دفتر يومية الأصول الثابتة‬**.</span><span class="sxs-lookup"><span data-stu-id="ca5e2-126">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="ca5e2-127">في القائمة، حدد دفتر اليومية الذي تم إنشاؤه بواسطة عملية التقسيم.</span><span class="sxs-lookup"><span data-stu-id="ca5e2-127">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="ca5e2-128">حدد **البنود**.</span><span class="sxs-lookup"><span data-stu-id="ca5e2-128">Select **Lines**.</span></span>

    - <span data-ttu-id="ca5e2-129">تحقق من بنود دفتر اليومية التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="ca5e2-129">Verify the journal lines created.</span></span>  
    - <span data-ttu-id="ca5e2-130">يتم إنشاء حركة تسوية الاستحواذ للأصل الأولي لإنقاص القيمة بالنسبة المئوية المحددة أثناء عملية التقسيم.</span><span class="sxs-lookup"><span data-stu-id="ca5e2-130">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>  
    - <span data-ttu-id="ca5e2-131">يتم إنشاء حركة استحواذ للأصل الجديد بالمبلغ نفسه.</span><span class="sxs-lookup"><span data-stu-id="ca5e2-131">An Acquisition transaction is created for the new asset for the same amount.</span></span>  

4. <span data-ttu-id="ca5e2-132">حدد **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="ca5e2-132">Select **Post**.</span></span>

