---
title: اقتراح عمليات الاستحواذ على الأصول الثابتة‬
description: يوضح هذا الموضوع كيفية الاستحواذ على أصل ثابت باستخدام مقترح الاستحواذ في دفتر يومية الأصول الثابتة.
author: saraschi2
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d529cd53b41827a78b282afd4d2c69d2f2db555e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817140"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="ebf5c-103">اقتراح عمليات الاستحواذ على الأصول الثابتة‬</span><span class="sxs-lookup"><span data-stu-id="ebf5c-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ebf5c-104">يوضح هذا الموضوع كيفية الاستحواذ على أصل ثابت باستخدام مقترح الاستحواذ في دفتر يومية الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="ebf5c-105">إنه يستخدم دور المحاسب وبيانات العرض التوضيحي في الكيان القانوني USMF.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-105">It uses the accountant role and demo data for the USMF legal entity.</span></span> <span data-ttu-id="ebf5c-106">للاستحواذ على أصل ثابت من خلال دفتر يومية مقترح الأصل الثابت، يجب أولاً إنشاء سجل الأصل الثابت، ثم تحديد سعر الاستحواذ في دفتر الأصول.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-106">To acquire a fixed asset through a fixed asset proposal journal, you must first create the fixed asset record, and then define the acquisition price in the asset book.</span></span>

## <a name="create-an-asset-acquisition-proposal"></a><span data-ttu-id="ebf5c-107">إنشاء مقترح الاستحواذ على الأصول</span><span class="sxs-lookup"><span data-stu-id="ebf5c-107">Create an asset acquisition proposal</span></span>

<span data-ttu-id="ebf5c-108">أكمل الخطوات التالية لإنشاء مقترح الاستحواذ على الأصل.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-108">Complete the following steps to create an asset acquisition proposal.</span></span> 

1. <span data-ttu-id="ebf5c-109">في جزء التنقل، انتقل إلى **الوحدات النمطية > الأصول الثابتة > إدخالات دفتر اليومية‬ > دفتر يومية الأصول الثابتة‬**.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-109">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="ebf5c-110">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-110">Select **New**.</span></span>
3. <span data-ttu-id="ebf5c-111">في الحقل **الاسم** أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-111">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="ebf5c-112">في جزء الإجراءات، حدد **البنود**.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-112">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="ebf5c-113">حدد **المقترحات**.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-113">Select **Proposals**.</span></span>
6. <span data-ttu-id="ebf5c-114">حدد **مقترح الاستحواذ**.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-114">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="ebf5c-115">حدد **عامل تصفية**.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-115">Select **Filter**.</span></span> <span data-ttu-id="ebf5c-116">حدد **إعادة تعيين** لمسح القيم السابقة.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-116">Select **Reset** to clear previous values.</span></span>
8. <span data-ttu-id="ebf5c-117">حدد صف **رقم الأصل الثابت**.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-117">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="ebf5c-118">في الحقل **المعايير‬**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-118">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="ebf5c-119">عيّن المعايير المتبقية للأصول الثابتة التي تريد الاستحواذ عليها بواسطة هذا المقترح.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-119">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="ebf5c-120">حدد **موافق** للخروج من الجزء.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-120">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="ebf5c-121">تحقق من بنود الحركة التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-121">Verify that the transaction lines are created.</span></span>  
- <span data-ttu-id="ebf5c-122">سيتضمن مقترح الاستحواذ فقط الأصول الثابتة ذات تاريخ استحواذ وسعر استحواذ تم تعيينهما على الدفتر.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-122">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="ebf5c-123">على الصفحة، حدد **الدفاتر**.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-123">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="ebf5c-124">حدد **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-124">Select **Post**.</span></span>

## <a name="include-default-financial-dimensions-in-an-acquisition-proposal"></a><span data-ttu-id="ebf5c-125">تضمين الأبعاد المالية الافتراضية في اقتراح الاستحواذ</span><span class="sxs-lookup"><span data-stu-id="ebf5c-125">Include default financial dimensions in an acquisition proposal</span></span>

<span data-ttu-id="ebf5c-126">يمكن إنشاء حركة الاستحواذ باستخدام وظائف Excel الإضافية، بالانتقال إلى **الأصول الثابتة> إدخالات دفتر اليومية> دفتر يومية الأصول الثابتة**.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-126">The acquisition transaction can be created using Excel add-ins, by going to **Fixed assets > Journal entries > Fixed asset journal**.</span></span> <span data-ttu-id="ebf5c-127">قم بإنشاء دفتر يوميه جديد وقم بالانتقال إلى قسم **البنود** في الصفحة وحدد رمز Excel، ثم حدد بند دفتر يوميه الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-127">Create a new journal and move to the **Lines** section on the page and select the Excel icon, and then select a Fixed asset journal line.</span></span> <span data-ttu-id="ebf5c-128">سيقوم النظام بإنشاء وفتح قالب Excel يمثل بنود دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-128">The system will create and open an Excel template representing journal lines.</span></span> <span data-ttu-id="ebf5c-129">يمكنك إضافة بيانات لأسطر دفتر اليومية التي تقوم بإضافتها إلى القالب، ثم نشر تلك المعلومات مرة أخرى في النظام.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-129">You can add data for the journal lines you're adding into the template, and then publish that information back into the system.</span></span> 

<span data-ttu-id="ebf5c-130">إذا تم إعداد الأبعاد الافتراضية لدفتر الأصول المحدد والأصول الثابتة المقابلة التي تم إدخالها في قالب Excel، فسيتم استدعاء الأبعاد المالية الافتراضية من البيانات الرئيسية لدفتر الأصول عند نشر دفتر اليومية من Excel إلى النظام.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-130">If default dimensions have been set up for the selected asset book and the corresponding fixed assets that were entered in the Excel template, the default financial dimensions will be called from the asset book master data when the journal is published from the Excel to the system.</span></span> <span data-ttu-id="ebf5c-131">لتضمين الأبعاد المالية في دفتر الأصول تلقائيًا أثناء نشر دفتر يومية الأصول الثابتة من وظيفة Excel الإضافية، يجب إعداد الأبعاد الافتراضية مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="ebf5c-131">To include financial dimensions on an asset book automatically while publishing the fixed asset journal from the Excel add-in, the default dimensions must be set up in advance.</span></span>  


[!INCLUDE [footer-include](../../../includes/footer-banner.md)]
