---
title: "إنشاء مقترح الإهلاك"
description: "يصف هذا الإجراء كيفية عمل مقترحات دفعات الإهلاك ويشرح كيفية اقتراح الإهلاك للأصول الثابتة."
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: d11554ee5f26ef5a85e799194d2f75757a31c254
ms.contentlocale: ar-sa
ms.lasthandoff: 09/14/2018

---

# <a name="create-depreciation-proposal"></a><span data-ttu-id="aba71-103">إنشاء مقترح الإهلاك</span><span class="sxs-lookup"><span data-stu-id="aba71-103">Create depreciation proposal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="aba71-104">يصف هذا الإجراء كيفية عمل مقترحات دفعات الإهلاك ويشرح كيفية اقتراح الإهلاك للأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="aba71-104">This procedure describes how depreciation batch proposals work and explains how to propose depreciation for fixed assets.</span></span> <span data-ttu-id="aba71-105">تستخدم هذه المهمة شركة العرض التوضيحي USMF ودور المحاسب.</span><span class="sxs-lookup"><span data-stu-id="aba71-105">This task uses the USMF demo company and the accountant role.</span></span>


## <a name="create-depreciation-proposal"></a><span data-ttu-id="aba71-106">إنشاء مقترح الإهلاك</span><span class="sxs-lookup"><span data-stu-id="aba71-106">Create depreciation proposal</span></span>
1. <span data-ttu-id="aba71-107">انتقل إلى الأصول الثابتة > إدخالات دفتر اليومية‬ > إنشاء مقترح الإهلاك‬‬.</span><span class="sxs-lookup"><span data-stu-id="aba71-107">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="aba71-108">في الحقل "اسم دفتر اليومية"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="aba71-108">In the Name of journal field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="aba71-109">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="aba71-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="aba71-110">في الحقل "إلى تاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="aba71-110">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="aba71-111">حدد الخيار "تلخيص الإهلاك‬" لتلخيص عمليات الإهلاك الشهرية في بند واحد بدفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="aba71-111">Select the Summarize depreciation option to summarize monthly depreciations into one journal line.</span></span>  
    * <span data-ttu-id="aba71-112">على سبيل المثال، إذا كانت قيمة "إلى تاريخ" 31 مارس 2015، يتم إنشاء الوصف التالي: "الإهلاك منذ 31 يناير 2015."</span><span class="sxs-lookup"><span data-stu-id="aba71-112">For example, if the To date value is March 31, 2015, the following description is generated: “Depreciation since January 31, 2015.”</span></span> <span data-ttu-id="aba71-113">يتم عندئذٍ تعيين حقل "التاريخ" في بنود دفتر اليومية المقترحة إلى 31 مارس 2015.</span><span class="sxs-lookup"><span data-stu-id="aba71-113">The Date field on the proposed journal lines is then set to March 31, 2015.</span></span>  
    * <span data-ttu-id="aba71-114">يمكن تصفية مقترح الإهلاك حسب الأصول أو مجموعة الأصول أو معايير أخرى باستخدام خيار التصفية.</span><span class="sxs-lookup"><span data-stu-id="aba71-114">The depreciation proposal can be filtered by asset, asset group, or other criteria using the Filter option.</span></span>  
    * <span data-ttu-id="aba71-115">عندما تستخدم النموذج "إنشاء مقترحات استحواذ أو إهلاك للأصول الثابتة‬"، يمكنك اقتراح الإهلاك بدفعات.</span><span class="sxs-lookup"><span data-stu-id="aba71-115">When you use the Create acquisition or depreciation proposals for fixed assets form, you can propose depreciation in batches.</span></span> <span data-ttu-id="aba71-116">يوصى بهذا الإجراء للمقترحات الكبيرة التي ستستخدم المزيد من موارد النظام.</span><span class="sxs-lookup"><span data-stu-id="aba71-116">This is recommended for larger proposals that will use more system resources.</span></span> <span data-ttu-id="aba71-117">إذا حددت خيار الدُفعة، فيمكنك الاستمرار في إكمال مهام أخرى خلال هذه الفترة.</span><span class="sxs-lookup"><span data-stu-id="aba71-117">If you select the batch option, you can still complete other tasks during that time.</span></span> <span data-ttu-id="aba71-118">عند اقتراح الإهلاك بهذه الطريقة، يتم حساب الإهلاك لنماذج القيمة للأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="aba71-118">When you propose depreciation in this way, depreciation is calculated for value models for fixed assets.</span></span>  
5. <span data-ttu-id="aba71-119">انقر فوق "إنشاء دفتر اليومية".</span><span class="sxs-lookup"><span data-stu-id="aba71-119">Click Create journal.</span></span>

## <a name="review-depreciation-entries"></a><span data-ttu-id="aba71-120">مراجعة إدخالات الإهلاك</span><span class="sxs-lookup"><span data-stu-id="aba71-120">Review depreciation entries</span></span>
1. <span data-ttu-id="aba71-121">انتقل إلى الأصول الثابتة > إدخالات دفتر اليومية‬ > دفتر يومية الأصول الثابتة‬.</span><span class="sxs-lookup"><span data-stu-id="aba71-121">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="aba71-122">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="aba71-122">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="aba71-123">انقر فوق البنود.</span><span class="sxs-lookup"><span data-stu-id="aba71-123">Click Lines.</span></span>
4. <span data-ttu-id="aba71-124">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="aba71-124">Click Post.</span></span>


