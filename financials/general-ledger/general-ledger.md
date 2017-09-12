---
title: "الصفحة الرئيسية لإعداد التقارير المالية ودفتر الأستاذ العام"
description: "استخدام دفتر الأستاذ العام لتحديد السجلات المالية للكيانات القانونية وإدارتها. دفتر الأستاذ العام هو سجل إدخالات الدائن والمدين. تم تصنيف هذه الإدخالات باستخدام الحسابات المدرجة في دليل الحسابات."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 78f3d9c27767c089ac686f333cae3cb50c03ee18
ms.contentlocale: ar-sa
ms.lasthandoff: 07/18/2017

---

# <a name="general-ledger"></a><span data-ttu-id="6af01-105">دفتر الأستاذ العام</span><span class="sxs-lookup"><span data-stu-id="6af01-105">General ledger</span></span> 

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6af01-106">استخدام دفتر الأستاذ العام لتحديد السجلات المالية للكيانات القانونية وإدارتها.</span><span class="sxs-lookup"><span data-stu-id="6af01-106">Use General ledger to define and manage the legal entity’s financial records.</span></span> <span data-ttu-id="6af01-107">دفتر الأستاذ العام هو سجل إدخالات الدائن والمدين.</span><span class="sxs-lookup"><span data-stu-id="6af01-107">The general ledger is a register of debit and credit entries.</span></span> <span data-ttu-id="6af01-108">تم تصنيف هذه الإدخالات باستخدام الحسابات المدرجة في دليل الحسابات.</span><span class="sxs-lookup"><span data-stu-id="6af01-108">These entries are classified using the accounts that are listed in a chart of accounts.</span></span> 

<span data-ttu-id="6af01-109">يمكنك تخصيص المبالغ النقدية أو توزيعها لحساب واحد أو أكثر، أو مجموعات الأبعاد والحسابات على أساس قواعد التخصيص.</span><span class="sxs-lookup"><span data-stu-id="6af01-109">You can allocate, or distribute, monetary amounts to one or more accounts or account and dimension combinations based on allocation rules.</span></span> <span data-ttu-id="6af01-110">هناك نوعان لعمليات التخصيص: الثابتة والمتغيرة.</span><span class="sxs-lookup"><span data-stu-id="6af01-110">There are two types of allocations: fixed and variable.</span></span> <span data-ttu-id="6af01-111">ويمكنك أيضًا تسوية الحركات بين حسابات دفتر الأستاذ وإعادة تقييم مبالغ العملة.</span><span class="sxs-lookup"><span data-stu-id="6af01-111">You can also settle transactions between ledger accounts and revalue currency amounts.</span></span> <span data-ttu-id="6af01-112">في نهاية السنة المالية، يجب عليك إنشاء حركات الإقفال، وتحضير حساباتك للسنة المالية التالية.</span><span class="sxs-lookup"><span data-stu-id="6af01-112">At the end of a fiscal year, you must generate closing transactions and prepare your accounts for the next fiscal year.</span></span> <span data-ttu-id="6af01-113">يمكنك استخدام وظيفة الدمج لتجميع النتائج المالية لعديد من الكيانات القانونية التابعة في نتائج لمؤسسة واحدة مدمجة.</span><span class="sxs-lookup"><span data-stu-id="6af01-113">You can use the consolidation functionality to combine the financial results for several subsidiary legal entities into results for a single, consolidated organization.</span></span> <span data-ttu-id="6af01-114">بإمكان الشركات التابعة أن تكون في قاعدة بيانات Microsoft Dynamics 365 for Finance and Operations نفسها أو في قواعد بيانات منفصلة.</span><span class="sxs-lookup"><span data-stu-id="6af01-114">The subsidiaries can be in the same Microsoft Dynamics 365 for Finance and Operations database or in separate databases.</span></span>

# <a name="sales-tax"></a><span data-ttu-id="6af01-115">ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="6af01-115">Sales tax</span></span>
<span data-ttu-id="6af01-116">تقوم كافة الشركات بجمع الضرائب ودفعها للعديد من هيئات الضرائب.</span><span class="sxs-lookup"><span data-stu-id="6af01-116">Every company collects and pays taxes to various tax authorities.</span></span> <span data-ttu-id="6af01-117">تختلف القواعد والمعدلات حسب البلد/المنطقة، والدولة، والمقاطعة، والمدينة.</span><span class="sxs-lookup"><span data-stu-id="6af01-117">The rules and rates vary by country/region, state, county, and city.</span></span> <span data-ttu-id="6af01-118">وبالإضافة إلى ذلك، يجب تحديث القواعد دورياً عند تغيير هيئات الضرائب لمتطلباتها.</span><span class="sxs-lookup"><span data-stu-id="6af01-118">In addition, the rules must be updated periodically when tax authorities change their requirements.</span></span> <span data-ttu-id="6af01-119">وتتضمن أكواد ضريبة المبيعات المعلومات الأساسية المطلوبة حول الكم الذي يجب جمعه ودفعه لهيئات الضرائب.</span><span class="sxs-lookup"><span data-stu-id="6af01-119">Sales tax codes contain the basic information about how much you collect and pay to the authorities.</span></span> <span data-ttu-id="6af01-120">عند إعداد أكواد ضريبة المبيعات، يمكنك تحديد المبالغ أو النسب المئوية التي يجب تجميعها.</span><span class="sxs-lookup"><span data-stu-id="6af01-120">When you set up sales tax codes, you define the amounts or percentages that must be collected.</span></span> <span data-ttu-id="6af01-121">يمكنك أيضا تعريف الأساليب المختلفة التي يتم من خلالها تطبيق هذه المبالغ أو النسب المئوية على مبالغ الحركة.</span><span class="sxs-lookup"><span data-stu-id="6af01-121">You also define the various methods by which those amounts or percentages are applied to transaction amounts.</span></span> <span data-ttu-id="6af01-122">وتوفر المواضيع الموجودة في هذا القسم معلومات حول كيفية إعداد أكواد ضريبة المبيعات للطرق والمعدلات التي تتطلبها هيئات الضرائب الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="6af01-122">The topics in this section provide information about how to set up sales tax codes for the methods and rates that your tax authorities require.</span></span>







