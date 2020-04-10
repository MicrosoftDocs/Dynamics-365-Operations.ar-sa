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
ms.openlocfilehash: e08177aad2db2438c2d5d4ddd294c1056b88167c
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142721"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="2dfe2-103">اقتراح عمليات الاستحواذ على الأصول الثابتة‬</span><span class="sxs-lookup"><span data-stu-id="2dfe2-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2dfe2-104">يوضح هذا الموضوع كيفية الاستحواذ على أصل ثابت باستخدام مقترح الاستحواذ في دفتر يومية الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="2dfe2-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="2dfe2-105">إنه يستخدم دور المحاسب وبيانات العرض التوضيحي في الكيان القانوني USMF.</span><span class="sxs-lookup"><span data-stu-id="2dfe2-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="2dfe2-106">في جزء التنقل، انتقل إلى **الوحدات النمطية > الأصول الثابتة > إدخالات دفتر اليومية‬ > دفتر يومية الأصول الثابتة‬**.</span><span class="sxs-lookup"><span data-stu-id="2dfe2-106">In the Navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="2dfe2-107">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="2dfe2-107">Select **New**.</span></span>
3. <span data-ttu-id="2dfe2-108">في الحقل **الاسم** أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2dfe2-108">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="2dfe2-109">في جزء الإجراءات، حدد **البنود**.</span><span class="sxs-lookup"><span data-stu-id="2dfe2-109">In the action pane, select **Lines**.</span></span>
5. <span data-ttu-id="2dfe2-110">حدد **المقترحات**.</span><span class="sxs-lookup"><span data-stu-id="2dfe2-110">Select **Proposals**.</span></span>
6. <span data-ttu-id="2dfe2-111">حدد **مقترح الاستحواذ**.</span><span class="sxs-lookup"><span data-stu-id="2dfe2-111">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="2dfe2-112">حدد **عامل تصفية**.</span><span class="sxs-lookup"><span data-stu-id="2dfe2-112">Select **Filter**.</span></span> <span data-ttu-id="2dfe2-113">حدد **إعادة تعيين** لمسح القيم السابقة.</span><span class="sxs-lookup"><span data-stu-id="2dfe2-113">Select **Reset** to clear out previous values.</span></span>
8. <span data-ttu-id="2dfe2-114">حدد صف **رقم الأصل الثابت**.</span><span class="sxs-lookup"><span data-stu-id="2dfe2-114">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="2dfe2-115">في الحقل **المعايير‬**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2dfe2-115">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="2dfe2-116">عيّن المعايير المتبقية للأصول الثابتة التي تريد الاستحواذ عليها بواسطة هذا المقترح.</span><span class="sxs-lookup"><span data-stu-id="2dfe2-116">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="2dfe2-117">حدد **موافق** للخروج من الجزء.</span><span class="sxs-lookup"><span data-stu-id="2dfe2-117">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="2dfe2-118">تحقق من بنود الحركة التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="2dfe2-118">Verify the transaction lines created.</span></span>  
- <span data-ttu-id="2dfe2-119">سيتضمن مقترح الاستحواذ فقط الأصول الثابتة ذات تاريخ استحواذ وسعر استحواذ تم تعيينهما على الدفتر.</span><span class="sxs-lookup"><span data-stu-id="2dfe2-119">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="2dfe2-120">على الصفحة، حدد **الدفاتر**.</span><span class="sxs-lookup"><span data-stu-id="2dfe2-120">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="2dfe2-121">حدد **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="2dfe2-121">Select **Post**.</span></span>

