---
title: إنشاء مقترح الإهلاك
description: يصف هذا الموضوع كيفية عمل مقترحات دُفعة الإهلاك ويشرح كيفية اقتراح إهلاك الأصول الثابتة.
author: abruer
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 90c24e9d89c055ea95ca5f25cd85ef4042476a90
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867597"
---
# <a name="create-a-depreciation-proposal"></a><span data-ttu-id="c5ae2-103">إنشاء مقترح الإهلاك</span><span class="sxs-lookup"><span data-stu-id="c5ae2-103">Create a depreciation proposal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c5ae2-104">يصف هذا الموضوع كيفية عمل مقترحات دُفعة الإهلاك ويشرح كيفية اقتراح إهلاك الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="c5ae2-104">This topic describes how depreciation batch proposals work and explains how to propose depreciation for fixed assets.</span></span> <span data-ttu-id="c5ae2-105">تستخدم هذه المهمة شركة العرض التوضيحي USMF ودور المحاسب.</span><span class="sxs-lookup"><span data-stu-id="c5ae2-105">This task uses the USMF demo company and the accountant role.</span></span>


## <a name="create-a-depreciation-proposal"></a><span data-ttu-id="c5ae2-106">إنشاء مقترح الإهلاك</span><span class="sxs-lookup"><span data-stu-id="c5ae2-106">Create a depreciation proposal</span></span>
1. <span data-ttu-id="c5ae2-107">في جزء التنقل، انتقل إلى **الوحدات النمطية > الأصول الثابتة > إدخالات دفتر اليومية‬ > إنشاء مقترح الإهلاك‬‬**.</span><span class="sxs-lookup"><span data-stu-id="c5ae2-107">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Create depreciation proposal**.</span></span>
2. <span data-ttu-id="c5ae2-108">في الحقل **اسم دفتر اليومية‬**، حدد خيارًا من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="c5ae2-108">In the **Name of journal** field, select an option from the drop-down menu.</span></span>
3. <span data-ttu-id="c5ae2-109">في الحقل **إلى تاريخ**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="c5ae2-109">In the **To date** field, enter a date.</span></span>

    - <span data-ttu-id="c5ae2-110">حدد الخيار **تلخيص الإهلاك** لتلخيص عمليات الإهلاك الشهرية في بند واحد بدفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="c5ae2-110">Select the **Summarize depreciation** option to summarize monthly depreciations into one journal line.</span></span>  
    - <span data-ttu-id="c5ae2-111">على سبيل المثال، إذا كانت قيمة "إلى تاريخ" 31 مارس 2015، يتم إنشاء الوصف التالي: "الإهلاك منذ 31 يناير 2015."</span><span class="sxs-lookup"><span data-stu-id="c5ae2-111">For example, if the To date value is March 31, 2015, the following description is generated: “Depreciation since January 31, 2015.”</span></span> <span data-ttu-id="c5ae2-112">يتم عندئذٍ تعيين حقل **التاريخ** في بنود دفتر اليومية المقترحة إلى 31 مارس 2015.</span><span class="sxs-lookup"><span data-stu-id="c5ae2-112">The **Date** field on the proposed journal lines is then set to March 31, 2015.</span></span>  
    - <span data-ttu-id="c5ae2-113">يمكن تصفية مقترح الإهلاك حسب الأصول أو مجموعة الأصول أو معايير أخرى باستخدام خيار **التصفية**.</span><span class="sxs-lookup"><span data-stu-id="c5ae2-113">The depreciation proposal can be filtered by asset, asset group, or other criteria using the **Filter** option.</span></span>  
    - <span data-ttu-id="c5ae2-114">عندما تستخدم النموذج **إنشاء مقترحات استحواذ أو إهلاك للأصول الثابتة‬**، يمكنك اقتراح الإهلاك بدفعات.</span><span class="sxs-lookup"><span data-stu-id="c5ae2-114">When you use the **Create acquisition or depreciation proposals for fixed assets** form, you can propose depreciation in batches.</span></span> <span data-ttu-id="c5ae2-115">يوصى بهذا الإجراء للمقترحات الكبيرة التي ستستخدم المزيد من موارد النظام.</span><span class="sxs-lookup"><span data-stu-id="c5ae2-115">This is recommended for larger proposals that will use more system resources.</span></span> <span data-ttu-id="c5ae2-116">إذا حددت خيار الدُفعة، فيمكنك الاستمرار في إكمال مهام أخرى خلال هذه الفترة.</span><span class="sxs-lookup"><span data-stu-id="c5ae2-116">If you select the batch option, you can still complete other tasks during that time.</span></span> <span data-ttu-id="c5ae2-117">عند اقتراح الإهلاك بهذه الطريقة، يتم حساب الإهلاك لنماذج القيمة للأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="c5ae2-117">When you propose depreciation in this way, depreciation is calculated for value models for fixed assets.</span></span>  

4. <span data-ttu-id="c5ae2-118">حدد **إنشاء دفتر اليومية**.</span><span class="sxs-lookup"><span data-stu-id="c5ae2-118">Select **Create journal**.</span></span>

## <a name="review-depreciation-entries"></a><span data-ttu-id="c5ae2-119">مراجعة إدخالات الإهلاك</span><span class="sxs-lookup"><span data-stu-id="c5ae2-119">Review depreciation entries</span></span>
1. <span data-ttu-id="c5ae2-120">في جزء التنقل، انتقل إلى **الوحدات النمطية > الأصول الثابتة > إدخالات دفتر اليومية‬ > دفتر يومية الأصول الثابتة‬**.</span><span class="sxs-lookup"><span data-stu-id="c5ae2-120">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="c5ae2-121">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c5ae2-121">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c5ae2-122">حدد **البنود**.</span><span class="sxs-lookup"><span data-stu-id="c5ae2-122">Select **Lines**.</span></span>
4. <span data-ttu-id="c5ae2-123">حدد **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="c5ae2-123">Select **Post**.</span></span>

