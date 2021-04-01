---
title: اقتراح عمليات الاستحواذ على الأصول الثابتة‬
description: يوضح هذا الموضوع كيفية الاستحواذ على أصل ثابت باستخدام مقترح الاستحواذ في دفتر يومية الأصول الثابتة.
author: saraschi2
manager: AnnBe
ms.date: 07/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 426a5e42c1fc26958ab37eddd915334f8b0e19cc
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205018"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="39340-103">اقتراح عمليات الاستحواذ على الأصول الثابتة‬</span><span class="sxs-lookup"><span data-stu-id="39340-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="39340-104">يوضح هذا الموضوع كيفية الاستحواذ على أصل ثابت باستخدام مقترح الاستحواذ في دفتر يومية الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="39340-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="39340-105">إنه يستخدم دور المحاسب وبيانات العرض التوضيحي في الكيان القانوني USMF.</span><span class="sxs-lookup"><span data-stu-id="39340-105">It uses the accountant role and demo data for the USMF legal entity.</span></span> <span data-ttu-id="39340-106">للاستحواذ على أصل ثابت من خلال دفتر يومية مقترح الأصل الثابت، يجب أولاً إنشاء سجل الأصل الثابت، ثم تحديد سعر الاستحواذ في دفتر الأصول.</span><span class="sxs-lookup"><span data-stu-id="39340-106">To acquire a fixed asset through a fixed asset proposal journal, you must first create the fixed asset record, and then define the acquisition price in the asset book.</span></span>

1. <span data-ttu-id="39340-107">في جزء التنقل، انتقل إلى **الوحدات النمطية > الأصول الثابتة > إدخالات دفتر اليومية‬ > دفتر يومية الأصول الثابتة‬**.</span><span class="sxs-lookup"><span data-stu-id="39340-107">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="39340-108">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="39340-108">Select **New**.</span></span>
3. <span data-ttu-id="39340-109">في الحقل **الاسم** أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="39340-109">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="39340-110">في جزء الإجراءات، حدد **البنود**.</span><span class="sxs-lookup"><span data-stu-id="39340-110">In the action pane, select **Lines**.</span></span>
5. <span data-ttu-id="39340-111">حدد **المقترحات**.</span><span class="sxs-lookup"><span data-stu-id="39340-111">Select **Proposals**.</span></span>
6. <span data-ttu-id="39340-112">حدد **مقترح الاستحواذ**.</span><span class="sxs-lookup"><span data-stu-id="39340-112">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="39340-113">حدد **عامل تصفية**.</span><span class="sxs-lookup"><span data-stu-id="39340-113">Select **Filter**.</span></span> <span data-ttu-id="39340-114">حدد **إعادة تعيين** لمسح القيم السابقة.</span><span class="sxs-lookup"><span data-stu-id="39340-114">Select **Reset** to clear out previous values.</span></span>
8. <span data-ttu-id="39340-115">حدد صف **رقم الأصل الثابت**.</span><span class="sxs-lookup"><span data-stu-id="39340-115">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="39340-116">في الحقل **المعايير‬**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="39340-116">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="39340-117">عيّن المعايير المتبقية للأصول الثابتة التي تريد الاستحواذ عليها بواسطة هذا المقترح.</span><span class="sxs-lookup"><span data-stu-id="39340-117">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="39340-118">حدد **موافق** للخروج من الجزء.</span><span class="sxs-lookup"><span data-stu-id="39340-118">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="39340-119">تحقق من بنود الحركة التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="39340-119">Verify the transaction lines created.</span></span>  
- <span data-ttu-id="39340-120">سيتضمن مقترح الاستحواذ فقط الأصول الثابتة ذات تاريخ استحواذ وسعر استحواذ تم تعيينهما على الدفتر.</span><span class="sxs-lookup"><span data-stu-id="39340-120">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="39340-121">على الصفحة، حدد **الدفاتر**.</span><span class="sxs-lookup"><span data-stu-id="39340-121">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="39340-122">حدد **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="39340-122">Select **Post**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]