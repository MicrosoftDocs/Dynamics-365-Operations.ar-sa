---
title: تخطيط بين الشركات الشقيقة
description: يوضح هذا الموضوع التخطيط بين الشركات الشقيقة ويوضح كيفيه تكوين التخطيط بين الشركات الشقيقة بتحسين التخطيط في Microsoft Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: dd498489e18eaba81720757faa14c0bf7b7d67f1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263388"
---
# <a name="intercompany-planning"></a><span data-ttu-id="52f96-103">تخطيط بين الشركات الشقيقة</span><span class="sxs-lookup"><span data-stu-id="52f96-103">Intercompany planning</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="52f96-104">بالنسبة لبعض المؤسسات ، تعتمد عمليات التجهيزات علي كيانات قانونيه أخرى (الشركات) في المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="52f96-104">For some organizations, logistics operations depend on other legal entities (companies) in the organization.</span></span> <span data-ttu-id="52f96-105">تتم معالجه هذه العمليات باستخدام المبيعات والمشتريات بين الشركات الشقيقة ، نظرا لان كل كيان قانوني يحتوي علي دليل حسابات منفصل.</span><span class="sxs-lookup"><span data-stu-id="52f96-105">These operations are handled by using intercompany sales and purchases, because each legal entity has a separate chart of accounts.</span></span>

<span data-ttu-id="52f96-106">يوضح هذا الموضوع التخطيط بين الشركات الشقيقة ويوضح كيفيه تكوين التخطيط بين الشركات الشقيقة بتحسين التخطيط في Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="52f96-106">This topic describes intercompany planning and explains how to configure intercompany planning with Planning Optimization in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="52f96-107">يستخدم هذا الموضوع الشروط الهامه التالية للشركات الشقيقة:</span><span class="sxs-lookup"><span data-stu-id="52f96-107">This topic uses the following important intercompany terms:</span></span>

- <span data-ttu-id="52f96-108">**المراحل التمهيدية** – مرجع نسبي في سلسله توريد أو شركة.</span><span class="sxs-lookup"><span data-stu-id="52f96-108">**Upstream** – A relative reference in a firm or supply chain.</span></span> <span data-ttu-id="52f96-109">وهي تشير إلى الحركة في اتجاه مورد المادة الخام.</span><span class="sxs-lookup"><span data-stu-id="52f96-109">It indicates movement in the direction of the raw material supplier.</span></span>
- <span data-ttu-id="52f96-110">**المراحل النهائية** – مرجع نسبي في سلسله توريد أو شركة.</span><span class="sxs-lookup"><span data-stu-id="52f96-110">**Downstream** – A relative reference in a firm or supply chain.</span></span> <span data-ttu-id="52f96-111">وهي تشير إلى الحركة في اتجاه العميل.</span><span class="sxs-lookup"><span data-stu-id="52f96-111">It indicates movement in the direction of the customer.</span></span>
- <span data-ttu-id="52f96-112">**الطلب المخطط بين الشركات الشقيقة** – طلب مخطط لمنتج في شركه ، استنادا إلى الطلب المخطط للمنتج من شركه في البداية.</span><span class="sxs-lookup"><span data-stu-id="52f96-112">**Planned intercompany demand** – Planned demand for a product in a company, based on planned demand for the product from a downstream company.</span></span>

<span data-ttu-id="52f96-113">في التخطيط الرئيسي ، يمكن ان تتضمن الخطة في أحدي الشركات طلبا مشتركا بين شركات شقيقه والمرتبطة بأوامر مخططه من خطه في شركه أخرى.</span><span class="sxs-lookup"><span data-stu-id="52f96-113">In master planning, a plan in one company can include planned intercompany demand that is related to planned orders from a plan in another company.</span></span> <span data-ttu-id="52f96-114">هذه القدرة مفيده ، لأنها توفر رؤية كامله في الأوامر المخططة عبر الشركات.</span><span class="sxs-lookup"><span data-stu-id="52f96-114">This capability is useful, because it provides full visibility into planned orders across companies.</span></span> <span data-ttu-id="52f96-115">كما يضمن إنشاء كافة أوامر التوريد المخططة المطلوبة ، لكن دون الحاجة إلى تاكيد ان الأوامر المخططة قد تم تاكيدها للطلب بين الشركات الشقيقة.</span><span class="sxs-lookup"><span data-stu-id="52f96-115">It also ensures that all required planned supply orders are created, but without requiring that planned orders be firmed for the intercompany demand.</span></span>

<span data-ttu-id="52f96-116">إذا قمت بتشغيل التخطيط الرئيسي من الخطة الرئيسية التي تشتمل علي الطلب اللاحق المخطط ، فانه سيتم تضمين أوامر الشراء المخططة من الموردين المرتبطين بالشركات الشقيقة في الخطة كطلب.</span><span class="sxs-lookup"><span data-stu-id="52f96-116">If you run master planning from a master plan that includes planned downstream demand, planned purchase orders from the related intercompany vendors will be included in the plan as demand.</span></span>

## <a name="required-setup"></a><span data-ttu-id="52f96-117">الإعداد المطلوب</span><span class="sxs-lookup"><span data-stu-id="52f96-117">Required setup</span></span>

<span data-ttu-id="52f96-118">لاستخدام تخطيط بين الشركات الشقيقة ، يجب اعداد النظام بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="52f96-118">To use intercompany planning, you must prepare your system in the following way:</span></span>

1. <span data-ttu-id="52f96-119">يجب إصدار المنتجات ذات الصلة في كافة الشركات ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="52f96-119">The relevant products must be released in all the relevant companies.</span></span> <span data-ttu-id="52f96-120">للحصول على مزيد من المعلومات، راجع [تكوين واستخدام التجارة بين الشركات الشقيقة في Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) في Microsoft Learn.</span><span class="sxs-lookup"><span data-stu-id="52f96-120">For more information, see [Configure and use intercompany trade in Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) on Microsoft Learn.</span></span>
1. <span data-ttu-id="52f96-121">يجب ان تتم تغطيه الطلب اللاحق بواسطة عمليات الشراء من مورد لديه علاقة بين الشركات الشقيقة وابعاد المخزون الافتراضية ذات الصلة (الموقع والمستودع) علي العميل.</span><span class="sxs-lookup"><span data-stu-id="52f96-121">Downstream demand must be covered by purchases from a vendor that has an intercompany relation to the upstream company and relevant default inventory dimensions (site and warehouse) on the customer.</span></span> <span data-ttu-id="52f96-122">للحصول على مزيد من المعلومات، راجع [تكوين واستخدام التجارة بين الشركات الشقيقة في Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) في Microsoft Learn.</span><span class="sxs-lookup"><span data-stu-id="52f96-122">For more information, see [Configure and use intercompany trade in Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) on Microsoft Learn.</span></span>
1. <span data-ttu-id="52f96-123">يجب ان تشتمل الخطة الرئيسية في شركة المراحل التمهيدية علي الطلب اللاحق المخطط ، كما يجب تحديد الشركة المرتبطة والخطة الرئيسية في الخطط اللاحقة.</span><span class="sxs-lookup"><span data-stu-id="52f96-123">The master plan in the upstream company must include planned downstream demand, and the relevant company and master plan must be specified in the downstream plans.</span></span>

## <a name="include-planned-downstream-demand"></a><span data-ttu-id="52f96-124">تضمين المطلب اللاحق المخطط</span><span class="sxs-lookup"><span data-stu-id="52f96-124">Include planned downstream demand</span></span>

<span data-ttu-id="52f96-125">اتبع هذه الخطوات لتكوين خطه رئيسيه بحيث تتضمن طلب المراحل النهائية المخططة.</span><span class="sxs-lookup"><span data-stu-id="52f96-125">Follow these steps to configure your master plan so that it includes planned downstream demand.</span></span>

1. <span data-ttu-id="52f96-126">انتقل إلى **التخطيط الرئيسي \> الإعداد \> الخطط \> الخطط الرئيسية**.</span><span class="sxs-lookup"><span data-stu-id="52f96-126">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="52f96-127">حدد خطه رئيسيه أو قم بإنشائها.</span><span class="sxs-lookup"><span data-stu-id="52f96-127">Select or create a master plan.</span></span>
1. <span data-ttu-id="52f96-128">في علامة التبويب السريعة **التخطيط بين الشركات الشقيقة**، اضبط الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="52f96-128">On the **Intercompany planning** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="52f96-129">**تضمين طلب المراحل النهائية المخطط** - قم بتعيين هذا الخيار إلى *نعم* لتمكين التخطيط بين الشركات الشقيقة للخطة الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="52f96-129">**Include planned downstream demand** – Set this option to *Yes* to enable intercompany planning for the master plan.</span></span>
    - <span data-ttu-id="52f96-130">**خطط المراحل النهائية** - إذا قمت بتعيين الخيار **تضمين طلب المراحل النهائية المخطط** إلى *نعم*، استخدم شريط الادوات والشبكة لأضافه الخطط الرئيسية المطلوبة من الشركات الأخرى.</span><span class="sxs-lookup"><span data-stu-id="52f96-130">**Downstream plans** – If you set the **Include planned downstream demand** option to *Yes*, use the toolbar and grid to add the desired master plans from other companies.</span></span>

## <a name="peg-across-companies-by-using-multilevel-pegging"></a><span data-ttu-id="52f96-131">التثبيت عبر الشركات باستخدام تثبيت متعدد متعدد المستويات</span><span class="sxs-lookup"><span data-stu-id="52f96-131">Peg across companies by using multilevel pegging</span></span>

<span data-ttu-id="52f96-132">في تثبيت السعر متعدد المستويات ، يمكنك عرض السعر عبر الشركات لرؤية مصدر الطلب الاولي الذي يتم تغطيته بواسطة التوريد.</span><span class="sxs-lookup"><span data-stu-id="52f96-132">In multilevel pegging, you can view pegging across companies to see the initial source of demand that is being covered by a supply.</span></span>

<span data-ttu-id="52f96-133">لعرض معلومات تثبيت السعر متعددة المستويات ، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="52f96-133">To view multilevel pegging information, follow these steps.</span></span>

1. <span data-ttu-id="52f96-134">انتقل إلى **التخطيط الرئيسي \> التخطيط الرئيسي \> الطلبات المخططة**.</span><span class="sxs-lookup"><span data-stu-id="52f96-134">Go to **Master planning \> Master planning \> Planned orders**.</span></span>
1. <span data-ttu-id="52f96-135">يتيح تحديد أمر مخطط أو فتحه.</span><span class="sxs-lookup"><span data-stu-id="52f96-135">Select or open a planned order.</span></span>
1. <span data-ttu-id="52f96-136">في جزء الإجراء، ضمن علامة التبويب **العرض**، في مجموعة **‏‫المتطلبات**، حدد **تثبيت متعدد المستويات**.</span><span class="sxs-lookup"><span data-stu-id="52f96-136">On the Action Pane, on the **View** tab, in the **Requirements** group, select **Multilevel pegging**.</span></span>

### <a name="intercompany-example-that-involves-two-companies"></a><span data-ttu-id="52f96-137">مثال علي شركات شقيقه يتضمن شركتان</span><span class="sxs-lookup"><span data-stu-id="52f96-137">Intercompany example that involves two companies</span></span>

<span data-ttu-id="52f96-138">بالنسبة لهذا المثال ، يتم إنشاء أمر إنتاج مخطط في الشركة USMF لتغطيه أمر التوريد في الشركة DEMF.</span><span class="sxs-lookup"><span data-stu-id="52f96-138">For this example, a planned production order is created in the USMF company to cover a sales order in the DEMF company.</span></span> <span data-ttu-id="52f96-139">وفي أوسمف ، يتم تخطيط الطلب المباشر حسب الطلب بين الشركات الشقيقة.</span><span class="sxs-lookup"><span data-stu-id="52f96-139">In USMF, the direct demand is planned intercompany demand.</span></span> <span data-ttu-id="52f96-140">لكي يظهر هذا الطلب في USMF، يتم تشغيل التخطيط الرئيسي أولا في DEMF ثم في USMF.</span><span class="sxs-lookup"><span data-stu-id="52f96-140">To make this demand appear in USMF, master planning is run first in DEMF and then in USMF.</span></span>

<span data-ttu-id="52f96-141">يبين الرسم التوضيحي التالي كيفيه ظهور هذا المثال علي الصفحة **تثبيت متعدد المستويات** لأمر الإنتاج المخطط.</span><span class="sxs-lookup"><span data-stu-id="52f96-141">The following illustration shows how this example might appear on the **Multilevel pegging** page for the planned production order.</span></span>

![مثال علي شركات شقيقه يتضمن شركتان](media/IntercompanyPlanning1.png)

### <a name="intercompany-example-that-involves-three-companies"></a><span data-ttu-id="52f96-143">مثال علي شركات شقيقه يتضمن ثلاث شركات</span><span class="sxs-lookup"><span data-stu-id="52f96-143">Intercompany example that involves three companies</span></span>

<span data-ttu-id="52f96-144">بالنسبة لهذا المثال ، يتم إنشاء أمر شراء مخطط في الشركة USMF لتغطيه أمر التوريد في الشركة FRRT.</span><span class="sxs-lookup"><span data-stu-id="52f96-144">For this example, a planned purchase order is created in the USMF company to cover a sales order in the FRRT company.</span></span> <span data-ttu-id="52f96-145">وفي شركات DEMF وUSMF، يتم تخطيط الطلب المباشر حسب الطلب بين الشركات الشقيقة.</span><span class="sxs-lookup"><span data-stu-id="52f96-145">In the DEMF and USMF companies, the direct demand is planned intercompany demand.</span></span> <span data-ttu-id="52f96-146">لكي يظهر هذا الطلب في USMF، يتم تشغيل التخطيط الرئيسي أولا في FRRT ثم في DEMF وفي النهاية في USMF.</span><span class="sxs-lookup"><span data-stu-id="52f96-146">To make this demand appear in USMF, master planning is run first in FRRT, then in DEMF, and finally in USMF.</span></span>

<span data-ttu-id="52f96-147">يبين الرسم التوضيحي التالي كيفيه ظهور هذا المثال علي الصفحة **تثبيت متعدد المستويات** لأمر الإنتاج المخطط.</span><span class="sxs-lookup"><span data-stu-id="52f96-147">The following illustration shows how this example might appear on the **Multilevel pegging** page for the planned production order.</span></span>

![مثال علي شركات شقيقه يتضمن ثلاث شركات](media/IntercompanyPlanning2.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]