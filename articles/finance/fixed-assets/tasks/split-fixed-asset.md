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
ms.openlocfilehash: 40703622bc8c7a21451d31e7606596c5edbe90f7
ms.sourcegitcommit: 51e626675b0130fa32a84ce2d9119b68ea928018
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4000283"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="649e3-103">تقسيم أصل ثابت</span><span class="sxs-lookup"><span data-stu-id="649e3-103">Split a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="649e3-104">يشرح هذا الموضوع كيفية تقسيم نسبة مئوية من دفتر الأصول إلى دفتر أصول جديد.</span><span class="sxs-lookup"><span data-stu-id="649e3-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="649e3-105">إنه يستخدم دور المحاسب وبيانات العرض التوضيحي USMF.‬</span><span class="sxs-lookup"><span data-stu-id="649e3-105">It uses the Accountant role and USMF demo data.</span></span>

## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="649e3-106">إنشاء أصل ثابت جديد</span><span class="sxs-lookup"><span data-stu-id="649e3-106">Create a new fixed asset</span></span>

1. <span data-ttu-id="649e3-107">في جزء التنقل، انتقل إلى **الوحدات النمطية \> الأصول الثابتة \> الأصول الثابتة \> الأصول الثابتة‬**.</span><span class="sxs-lookup"><span data-stu-id="649e3-107">In the navigation pane, go to **Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="649e3-108">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="649e3-108">Select **New**.</span></span>
3. <span data-ttu-id="649e3-109">في حقل **مجموعة الأصول الثابتة** ، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="649e3-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="649e3-110">لاحظ رقم الأصل الثابت لاستخدامه في عملية التقسيم لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="649e3-110">Note the fixed asset number to use in the split process later.</span></span>
4. <span data-ttu-id="649e3-111">في حقل **الاسم** ، أدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="649e3-111">In the **Name** field, enter a value.</span></span>
5. <span data-ttu-id="649e3-112">وقم بغلق النموذج.</span><span class="sxs-lookup"><span data-stu-id="649e3-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="649e3-113">تقسيم أصل ثابت</span><span class="sxs-lookup"><span data-stu-id="649e3-113">Split a fixed asset</span></span>

<span data-ttu-id="649e3-114">قبل تقسيم الأصل الذي تم إهلاكه بالكامل، يجب تغيير حالة دفتر الأصول يدويا من **مُقفل** إلى **مفتوح**.</span><span class="sxs-lookup"><span data-stu-id="649e3-114">Before a fully depreciated asset is split, the asset book status should be manually changed from **Closed** to **Open**.</span></span> <span data-ttu-id="649e3-115">هذه الخطوة مطلوبه نظرا لأنه يجب أن تكون حالة الدفتر **مفتوح** إذا كان من الضروري ترحيل الحركات للأصل (على سبيل المثال، لبيع التخلص).</span><span class="sxs-lookup"><span data-stu-id="649e3-115">This step is required because the book status has to be **Open** if you must post transactions for the asset (for example, for a disposal sale).</span></span> <span data-ttu-id="649e3-116">بعد تغيير حالة دفتر الأصول، اتبع هذه الخطوات لتقسيم الأصل.</span><span class="sxs-lookup"><span data-stu-id="649e3-116">After the asset book status is changed, follow these steps to split the asset.</span></span>

1. <span data-ttu-id="649e3-117">في القائمة، ابحث عن الارتباط إلى الأصل الثابت المراد تقسيمه وحدده.</span><span class="sxs-lookup"><span data-stu-id="649e3-117">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="649e3-118">حدد **الدفاتر**.</span><span class="sxs-lookup"><span data-stu-id="649e3-118">Select **Books**.</span></span> <span data-ttu-id="649e3-119">حدد الدفتر لتقسيمه إلى الأصل الجديد.</span><span class="sxs-lookup"><span data-stu-id="649e3-119">Select the book to split to the new asset.</span></span>
3. <span data-ttu-id="649e3-120">حدد **الوظائف**.</span><span class="sxs-lookup"><span data-stu-id="649e3-120">Select **Functions**.</span></span>
4. <span data-ttu-id="649e3-121">حدد **تقسيم الأصل الثابت**.</span><span class="sxs-lookup"><span data-stu-id="649e3-121">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="649e3-122">في حقل **إلى الأصل الثابت** ، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="649e3-122">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="649e3-123">في الحقل **إلى دفتر‬** ، حدد زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="649e3-123">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="649e3-124">في حقل **‏‫تاريخ الحركة** ، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="649e3-124">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="649e3-125">في الحقل **النسبة‬ المئوية** ، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="649e3-125">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="649e3-126">في الحقل **اسم دفتر اليومية** ، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="649e3-126">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="649e3-127">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="649e3-127">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="649e3-128">ترحيل حركة دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="649e3-128">Post the journal transaction</span></span>

1. <span data-ttu-id="649e3-129">في جزء التنقل، انتقل إلى **الوحدات النمطية \> الأصول الثابتة \> إدخالات دفتر اليومية‬ \> دفتر يومية الأصول الثابتة‬**.</span><span class="sxs-lookup"><span data-stu-id="649e3-129">In the navigation pane, go to **Modules \> Fixed assets \> Journal entries \> Fixed assets journal**.</span></span>
2. <span data-ttu-id="649e3-130">في القائمة، حدد دفتر اليومية الذي تم إنشاؤه بواسطة عملية التقسيم.</span><span class="sxs-lookup"><span data-stu-id="649e3-130">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="649e3-131">حدد **البنود**.</span><span class="sxs-lookup"><span data-stu-id="649e3-131">Select **Lines**.</span></span>

    - <span data-ttu-id="649e3-132">تحقق من بنود دفتر اليومية التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="649e3-132">Verify the journal lines created.</span></span>
    - <span data-ttu-id="649e3-133">يتم إنشاء حركة تسوية الاستحواذ للأصل الأولي لإنقاص القيمة بالنسبة المئوية المحددة أثناء عملية التقسيم.</span><span class="sxs-lookup"><span data-stu-id="649e3-133">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>
    - <span data-ttu-id="649e3-134">يتم إنشاء حركة استحواذ للأصل الجديد بالمبلغ نفسه.</span><span class="sxs-lookup"><span data-stu-id="649e3-134">An Acquisition transaction is created for the new asset for the same amount.</span></span>

4. <span data-ttu-id="649e3-135">حدد **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="649e3-135">Select **Post**.</span></span>
