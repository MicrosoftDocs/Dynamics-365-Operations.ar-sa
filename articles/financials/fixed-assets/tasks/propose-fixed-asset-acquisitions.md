---
title: اقتراح عمليات الاستحواذ على الأصول الثابتة‬
description: يوضح هذا الموضوع كيفية الاستحواذ على أصل ثابت باستخدام مقترح الاستحواذ في دفتر يومية الأصول الثابتة.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b35b13dc266fd5bccde437526400832d394b9aa
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839895"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="a60e5-103">اقتراح عمليات الاستحواذ على الأصول الثابتة‬</span><span class="sxs-lookup"><span data-stu-id="a60e5-103">Propose fixed asset acquisitions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a60e5-104">يوضح هذا الموضوع كيفية الاستحواذ على أصل ثابت باستخدام مقترح الاستحواذ في دفتر يومية الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="a60e5-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="a60e5-105">إنه يستخدم دور المحاسب وبيانات العرض التوضيحي في الكيان القانوني USMF.</span><span class="sxs-lookup"><span data-stu-id="a60e5-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="a60e5-106">في جزء التنقل، انتقل إلى **الوحدات النمطية > الأصول الثابتة > إدخالات دفتر اليومية‬ > دفتر يومية الأصول الثابتة‬**.</span><span class="sxs-lookup"><span data-stu-id="a60e5-106">In the Navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="a60e5-107">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="a60e5-107">Select **New**.</span></span>
3. <span data-ttu-id="a60e5-108">في الحقل **الاسم** أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="a60e5-108">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="a60e5-109">في جزء الإجراءات، حدد **البنود**.</span><span class="sxs-lookup"><span data-stu-id="a60e5-109">In the action pane, select **Lines**.</span></span>
5. <span data-ttu-id="a60e5-110">حدد **المقترحات**.</span><span class="sxs-lookup"><span data-stu-id="a60e5-110">Select **Proposals**.</span></span>
6. <span data-ttu-id="a60e5-111">حدد **مقترح الاستحواذ**.</span><span class="sxs-lookup"><span data-stu-id="a60e5-111">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="a60e5-112">حدد **عامل تصفية**.</span><span class="sxs-lookup"><span data-stu-id="a60e5-112">Select **Filter**.</span></span> <span data-ttu-id="a60e5-113">حدد **إعادة تعيين** لمسح القيم السابقة.</span><span class="sxs-lookup"><span data-stu-id="a60e5-113">Select **Reset** to clear out previous values.</span></span>
8. <span data-ttu-id="a60e5-114">حدد صف **رقم الأصل الثابت**.</span><span class="sxs-lookup"><span data-stu-id="a60e5-114">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="a60e5-115">في الحقل **المعايير‬**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="a60e5-115">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="a60e5-116">عيّن المعايير المتبقية للأصول الثابتة التي تريد الاستحواذ عليها بواسطة هذا المقترح.</span><span class="sxs-lookup"><span data-stu-id="a60e5-116">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="a60e5-117">حدد **موافق** للخروج من الجزء.</span><span class="sxs-lookup"><span data-stu-id="a60e5-117">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="a60e5-118">تحقق من بنود الحركة التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="a60e5-118">Verify the transaction lines created.</span></span>  
- <span data-ttu-id="a60e5-119">سيتضمن مقترح الاستحواذ فقط الأصول الثابتة ذات تاريخ استحواذ وسعر استحواذ تم تعيينهما على الدفتر.</span><span class="sxs-lookup"><span data-stu-id="a60e5-119">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="a60e5-120">على الصفحة، حدد **الدفاتر**.</span><span class="sxs-lookup"><span data-stu-id="a60e5-120">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="a60e5-121">حدد **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="a60e5-121">Select **Post**.</span></span>

