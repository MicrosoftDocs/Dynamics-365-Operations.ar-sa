---
title: استحقاق تكلفة المشروع في إيصالات الشراء
description: يوضح هذا الموضوع كيفية تعقب تكاليف المشروع المستحقة من إيصالات الشراء في Dynamics 365 FinanceMicrosoft.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostControlCommittedCost
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 0a930b4921a29d5ce561ce0e958733f0c3261b81
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439904"
---
# <a name="project-cost-accrual-on-purchase-receipts"></a><span data-ttu-id="a8d0f-103">استحقاق تكلفة المشروع في إيصالات الشراء</span><span class="sxs-lookup"><span data-stu-id="a8d0f-103">Project cost accrual on purchase receipts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a8d0f-104">يوضح هذا الموضوع كيفية تعقب تكاليف المشروع المستحقة من إيصالات الشراء في Dynamics 365 FinanceMicrosoft.</span><span class="sxs-lookup"><span data-stu-id="a8d0f-104">This topic describes how accrued project costs from purchase receipts can be tracked in Microsoft Dynamics 365 Finance.</span></span> 

<span data-ttu-id="a8d0f-105">عادةً ما تصل فواتير المشروع لاحقًا بعد تسليم البضائع والخدمات، مما قد يكون له تأثير كبير على مؤشرات الأداء الرئيسية للمشروع.</span><span class="sxs-lookup"><span data-stu-id="a8d0f-105">Invoices for a project often arrive later than the goods and services are delivered, which might have a significant impact on project key performance indicators (KPIs).</span></span> <span data-ttu-id="a8d0f-106">من المهم أن تكون قادرًا على تعقب هذه الحركات في كل من التقارير المالية وتقارير المشروع.</span><span class="sxs-lookup"><span data-stu-id="a8d0f-106">It important to be able to track these transactions in both financial and project reports.</span></span>

<span data-ttu-id="a8d0f-107">يوضح سيناريو المثال التالي هذا الأمر.</span><span class="sxs-lookup"><span data-stu-id="a8d0f-107">The following example scenario illustrates this.</span></span> 

<span data-ttu-id="a8d0f-108">بدأت Contoso للاستشارات مشروع نشر سحابة جديد.</span><span class="sxs-lookup"><span data-stu-id="a8d0f-108">Contoso Consulting has started a new cloud deployment project.</span></span> <span data-ttu-id="a8d0f-109">يتم إنشاء أمر لشراء جهاز كمبيوتر للمشروع.</span><span class="sxs-lookup"><span data-stu-id="a8d0f-109">A purchase order is created to buy a computer for the project.</span></span> <span data-ttu-id="a8d0f-110">سوف يتكلف جهاز الكمبيوتر 1500 دولار، وسوف تتكلف خدمة تركيبه 150 دولار.</span><span class="sxs-lookup"><span data-stu-id="a8d0f-110">The computer will cost $1500 and installation services will cost $150.</span></span> <span data-ttu-id="a8d0f-111">قام المورد بتسليم جهاز الكمبيوتر وتركيبه، ولكن لم تصل الفاتورة إلى Contoso للاستشارات بعد.</span><span class="sxs-lookup"><span data-stu-id="a8d0f-111">The vendor has delivered and installed the computer, but the invoice has not yet reached Contoso Consulting.</span></span> <span data-ttu-id="a8d0f-112">يريد مدير المشروع رؤية تكاليف المشروع المستحقة والتي تبلغ 1650 دولار قبل تسليم الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="a8d0f-112">The project manager would like to see project cost accrual of $1650 before the invoice gets delivered.</span></span> <span data-ttu-id="a8d0f-113">يجب أن تنعكس التكلفة في البيانات المالية النهاية الشهر الخاصة بالشركة.</span><span class="sxs-lookup"><span data-stu-id="a8d0f-113">This cost should also be reflected in the company's month end financial statements.</span></span> 

<span data-ttu-id="a8d0f-114">يلزم تسجيل التكلفة المستحقة في كل من المستوى المالي ومستوى المشروع لأغراض إعداد التقارير.</span><span class="sxs-lookup"><span data-stu-id="a8d0f-114">The accrued cost needs to be recorded on both the financial level and project level for reporting purposes.</span></span> <span data-ttu-id="a8d0f-115">يمكن تعقب التحديث المالي لاستلام المنتج بالنسبة للصنف وفئات التدبير.</span><span class="sxs-lookup"><span data-stu-id="a8d0f-115">The financial update of the product receipt can be tracked for the item and procurement categories.</span></span> 

<span data-ttu-id="a8d0f-116">بالنسبة للأصناف، على صفحة **محددات الحسابات الدائنة**، حدد خيار **ترحيل إيصالات استلام المنتجات إلى دفتر الأستاذ**.</span><span class="sxs-lookup"><span data-stu-id="a8d0f-116">For items, on the **Accounts payable parameters** page, select the **Post product receipts to ledger** option.</span></span>
<span data-ttu-id="a8d0f-117">[![صفحة معلمات الحسابات الدائنة](./media/accruals1-1024x409.png)](./media/accruals1.png)</span><span class="sxs-lookup"><span data-stu-id="a8d0f-117">[![Accounts payable parameters page](./media/accruals1-1024x409.png)](./media/accruals1.png)</span></span> 

<span data-ttu-id="a8d0f-118">بالنسبة لفئات المشتريات، على صفحة **قاعدة سياسة الفئة**، حدد السياسات **الشرائية**، ومن ثم حدد **استحقاق مصروفات الشراء عند الاستلام** لكل فئة تدبير.</span><span class="sxs-lookup"><span data-stu-id="a8d0f-118">For procurement categories, on the **Category policy rule** page, select **Purchasing** policies, and then select **Accrue purchase expense on receipt** for each procurement category.</span></span>
<span data-ttu-id="a8d0f-119">[![صفحة قاعدة سياسة الفئة](./media/accruals2-1024x569.png)](./media/accruals2.png)</span><span class="sxs-lookup"><span data-stu-id="a8d0f-119">[![Category policy rule page](./media/accruals2-1024x569.png)](./media/accruals2.png)</span></span> 

<span data-ttu-id="a8d0f-120">سوف تستخدم حسابات **نفقات الشراء غير المفوترة** و **استحقاق الشراء** في **إعداد الترحيل** عند ترحيل الإيصالات المتعلقة باستلام المنتجات.</span><span class="sxs-lookup"><span data-stu-id="a8d0f-120">The **Purchase expenditure un-invoiced** and **Purchase accrual** accounts in **Posting setup** will be used when vouchers that are related to the product receipt are posted.</span></span>

<span data-ttu-id="a8d0f-121">باستخدام نفس السيناريو، لنرى كيف سيؤثر ترحيل إيصال منتج على دفتر الأستاذ العام ومعلومات المشروع.</span><span class="sxs-lookup"><span data-stu-id="a8d0f-121">Using this same scenario, let's see how posting a product receipt will impact General ledger and Project information.</span></span> 

<span data-ttu-id="a8d0f-122">**الخطوة 1:** إنشاء وتأكيد أمر شراء جديد للمشروع لتسجيل شراء كمبيوتر بسرع 1500 دولار وخدمات تركيب بسعر 150 دولار.</span><span class="sxs-lookup"><span data-stu-id="a8d0f-122">**Step 1:** Create and confirm a new purchase order for the project to record the purchase of a computer for $1500 and installation services for $150.</span></span>
<span data-ttu-id="a8d0f-123">[![إنشاء أمر شراء جديد](./media/accruals4-1024x497.png)](./media/accruals4.png)</span><span class="sxs-lookup"><span data-stu-id="a8d0f-123">[![Create new purchase order](./media/accruals4-1024x497.png)](./media/accruals4.png)</span></span> 

<span data-ttu-id="a8d0f-124">عند تأكيد أمر الشراء، يتم إنشاء حركات للتكلفة الإلزامية الخاصة بالمشروع.</span><span class="sxs-lookup"><span data-stu-id="a8d0f-124">When the purchase order is confirmed, transactions for the committed cost are created for the project.</span></span> 
<span data-ttu-id="a8d0f-125">[![الحركات التي تم إنشاؤها](./media/accruals5-1024x219.png)](./media/accruals5.png)</span><span class="sxs-lookup"><span data-stu-id="a8d0f-125">[![Transactions created](./media/accruals5-1024x219.png)](./media/accruals5.png)</span></span> 

> [!NOTE]
> <span data-ttu-id="a8d0f-126">سوف يكون للحركات المخصصة للتكلفة الإلزامية حقل **"أصل الحركة"** والذي يتم تعيينه إلى **"أمر الشراء"**.</span><span class="sxs-lookup"><span data-stu-id="a8d0f-126">The transactions for the committed cost will have the **Transaction Origin** field set to **Purchase Order**.</span></span> <span data-ttu-id="a8d0f-127">لا يؤدي إنشاء وتأكيد أمر شراء إلى إنشاء حركات لمشروع.</span><span class="sxs-lookup"><span data-stu-id="a8d0f-127">Creating and confirming a purchase order does not create transactions for a project.</span></span> 

<span data-ttu-id="a8d0f-128">**الخطوة 2:** تم تسليم البضائع والخدمات، وتم تسجيل استلام منتج.</span><span class="sxs-lookup"><span data-stu-id="a8d0f-128">**Step 2:** Goods and services get delivered and a product receipt is registered.</span></span> 

<span data-ttu-id="a8d0f-129">سوف يؤدي ترحيل استلام منتج إلى إنشاء وترحيل إيصال إلى دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="a8d0f-129">Posting a product receipt will generate and post a voucher to the ledger.</span></span> <span data-ttu-id="a8d0f-130">سوف يقوم الإيصال بخصم نفقات الشراء والحسابات غير المفوترة وحساب استحقاق شراء الائتمان.</span><span class="sxs-lookup"><span data-stu-id="a8d0f-130">The voucher will debit the purchase expenditure, un-invoiced account, and credit purchase accrual account.</span></span> 
<span data-ttu-id="a8d0f-131">[![حركات الإيصال](./media/accruals6-1024x214.png)](./media/accruals6.png)</span><span class="sxs-lookup"><span data-stu-id="a8d0f-131">[![Voucher transactions](./media/accruals6-1024x214.png)](./media/accruals6.png)</span></span>

> [!NOTE]
> <span data-ttu-id="a8d0f-132">سوف يستخدم ترحيل إيصال إعداد الترحيل لفئات التدبير والمنتجات، ولن يقوم بترحيل الإعداد لفئات المشروع.</span><span class="sxs-lookup"><span data-stu-id="a8d0f-132">Posting a product receipt will use the posting setup for procurement categories and products, and not the posting setup for the project categories.</span></span> <span data-ttu-id="a8d0f-133">ولإظهار الأثر المالي لاستحقاقات الشراء بشكل صحيح، يلزم محاذاة هذا الإعداد.</span><span class="sxs-lookup"><span data-stu-id="a8d0f-133">In order to correctly reflect financial impact of purchase accruals, this setup needs to be aligned.</span></span> 

<span data-ttu-id="a8d0f-134">من الممكن تعيين فئات التدبير لفئات المشروع على **فئة التدبير**.</span><span class="sxs-lookup"><span data-stu-id="a8d0f-134">It is possible to map procurement categories to project categories on the **Procurement category** page.</span></span>
<span data-ttu-id="a8d0f-135">[![اسم فئة التدبير](./media/accruals7-1024x390.png)](./media/accruals7.png)</span><span class="sxs-lookup"><span data-stu-id="a8d0f-135">[![Procurement category page](./media/accruals7-1024x390.png)](./media/accruals7.png)</span></span>

<span data-ttu-id="a8d0f-136">**خطوة 3:** إنشاء مسودة فاتورة مورد.</span><span class="sxs-lookup"><span data-stu-id="a8d0f-136">**Step 3:** Create a draft vendor invoice.</span></span> 

<span data-ttu-id="a8d0f-137">لا يؤثر ترحيل إيصال منتج على معلومات المشروع.</span><span class="sxs-lookup"><span data-stu-id="a8d0f-137">Posting a product receipt does not impact project information.</span></span> <span data-ttu-id="a8d0f-138">وكحل لهذا الأمر، يمكنك إنشاء مسودة فاتورة مورد مباشرة بعد ترحيل إيصال الشراء.</span><span class="sxs-lookup"><span data-stu-id="a8d0f-138">As a workaround, you could generate a draft vendor invoice right after posting the purchase receipt.</span></span> <span data-ttu-id="a8d0f-139">انتقل إلى صفحة **أمر الشراء** &gt; **علامة تبويب الفاتورة** &gt; **إنشاء** &gt; **الفاتورة**.</span><span class="sxs-lookup"><span data-stu-id="a8d0f-139">Go to the **Purchase Order** page &gt; **Invoice tab** &gt; **Generate** &gt; **Invoice**.</span></span> <span data-ttu-id="a8d0f-140">يؤدي هذا إلى إنشاء مستند فاتورة معلقة تُحدث معلومات المشروع.</span><span class="sxs-lookup"><span data-stu-id="a8d0f-140">This creates a pending invoice document that updates project information.</span></span> 

<span data-ttu-id="a8d0f-141">سوف يؤدي إنشاء مسودة فاتورة مورد إلى إنشاء حركات مشروع معلقة.</span><span class="sxs-lookup"><span data-stu-id="a8d0f-141">Creating a draft vendor invoice will generate pending project transactions.</span></span> 
<span data-ttu-id="a8d0f-142">[![حركات المشروع المعلقة](./media/accruals8-1024x225.png)](./media/accruals8.png)</span><span class="sxs-lookup"><span data-stu-id="a8d0f-142">[![Pending project transactions](./media/accruals8-1024x225.png)](./media/accruals8.png)</span></span> 

<span data-ttu-id="a8d0f-143">في صفحة **التكلفة الإلزامية**، سيتم إغلاق السجلات التي تم إنشاؤها في الخطوة 1 وسيتم إنشاء سجلات جديدة لتعكس التزام التكلفة الوارد من فاتورة المورد المعلقة.</span><span class="sxs-lookup"><span data-stu-id="a8d0f-143">In the **Committed cost** page, records created in step 1 will be closed and new records will be created to reflect cost commitment coming from the pending vendor invoice.</span></span> <span data-ttu-id="a8d0f-144">سوف يتم تعيين حقل **أصل الحركة** للتكلفة الإلزامية إلى **فاتورة المورد**.</span><span class="sxs-lookup"><span data-stu-id="a8d0f-144">The **Transaction origin** field for the committed cost will be set to **Vendor invoice**.</span></span>
<span data-ttu-id="a8d0f-145">[![صفحة التكاليف الإلزامية](./media/accruals9-1024x200.png)](./media/accruals9.png)</span><span class="sxs-lookup"><span data-stu-id="a8d0f-145">[![Commited costs page](./media/accruals9-1024x200.png)](./media/accruals9.png)</span></span>

<span data-ttu-id="a8d0f-146">سوف تظل فاتورة المورد في وضع معلق حتى وصول فاتور المورد الفعلية.</span><span class="sxs-lookup"><span data-stu-id="a8d0f-146">The vendor invoice will remain in a pending state until the actual vendor invoice arrives.</span></span>



