---
title: استحقاق تكلفة المشروع في إيصالات الشراء
description: يوضح هذا الموضوع كيفية تعقب تكاليف المشروع المستحقة من إيصالات الشراء في Microsoft Dynamics 365 for Finance and Operations.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostControlCommittedCost
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: bc822652abbba68f094fe5b8a65f796165a92c4c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556675"
---
# <a name="project-cost-accrual-on-purchase-receipts"></a><span data-ttu-id="a5561-103">استحقاق تكلفة المشروع في إيصالات الشراء</span><span class="sxs-lookup"><span data-stu-id="a5561-103">Project cost accrual on purchase receipts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a5561-104">يوضح هذا الموضوع كيفية تعقب تكاليف المشروع المستحقة من إيصالات الشراء في Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a5561-104">This topic describes how accrued project costs from purchase receipts can be tracked in Microsoft Dynamics 365 for Finance and Operations.</span></span> 

<span data-ttu-id="a5561-105">عادةً ما تصل فواتير المشروع لاحقًا بعد تسليم البضائع والخدمات، مما قد يكون له تأثير كبير على مؤشرات الأداء الرئيسية للمشروع.</span><span class="sxs-lookup"><span data-stu-id="a5561-105">Invoices for a project often arrive later than the goods and services are delivered, which might have a significant impact on project key performance indicators (KPIs).</span></span> <span data-ttu-id="a5561-106">من المهم أن تكون قادرًا على تعقب هذه الحركات في كل من التقارير المالية وتقارير المشروع.</span><span class="sxs-lookup"><span data-stu-id="a5561-106">It important to be able to track these transactions in both financial and project reports.</span></span>

<span data-ttu-id="a5561-107">يوضح سيناريو المثال التالي هذا الأمر.</span><span class="sxs-lookup"><span data-stu-id="a5561-107">The following example scenario illustrates this.</span></span> 

<span data-ttu-id="a5561-108">بدأت Contoso للاستشارات مشروع نشر سحابة جديد.</span><span class="sxs-lookup"><span data-stu-id="a5561-108">Contoso Consulting has started a new cloud deployment project.</span></span> <span data-ttu-id="a5561-109">يتم إنشاء أمر لشراء جهاز كمبيوتر للمشروع.</span><span class="sxs-lookup"><span data-stu-id="a5561-109">A purchase order is created to buy a computer for the project.</span></span> <span data-ttu-id="a5561-110">سوف يتكلف جهاز الكمبيوتر 1500 دولار، وسوف تتكلف خدمة تركيبه 150 دولار.</span><span class="sxs-lookup"><span data-stu-id="a5561-110">The computer will cost $1500 and installation services will cost $150.</span></span> <span data-ttu-id="a5561-111">قام المورد بتسليم جهاز الكمبيوتر وتركيبه، ولكن لم تصل الفاتورة إلى Contoso للاستشارات بعد.</span><span class="sxs-lookup"><span data-stu-id="a5561-111">The vendor has delivered and installed the computer, but the invoice has not yet reached Contoso Consulting.</span></span> <span data-ttu-id="a5561-112">يريد مدير المشروع رؤية تكاليف المشروع المستحقة والتي تبلغ 1650 دولار قبل تسليم الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="a5561-112">The project manager would like to see project cost accrual of $1650 before the invoice gets delivered.</span></span> <span data-ttu-id="a5561-113">يجب أن تنعكس التكلفة في البيانات المالية النهاية الشهر الخاصة بالشركة.</span><span class="sxs-lookup"><span data-stu-id="a5561-113">This cost should also be reflected in the company's month end financial statements.</span></span> 

<span data-ttu-id="a5561-114">يلزم تسجيل التكلفة المستحقة في كل من المستوى المالي ومستوى المشروع لأغراض إعداد التقارير.</span><span class="sxs-lookup"><span data-stu-id="a5561-114">The accrued cost needs to be recorded on both the financial level and project level for reporting purposes.</span></span> <span data-ttu-id="a5561-115">في Finance and Operations، يمكن تعقب التحديث المالي لاستلام المنتج بالنسبة للصنف وفئات التدبير.</span><span class="sxs-lookup"><span data-stu-id="a5561-115">In Finance and Operations, the financial update of the product receipt can be tracked for the item and procurement categories.</span></span> 

<span data-ttu-id="a5561-116">بالنسبة للأصناف، على صفحة **محددات الحسابات الدائنة**، حدد خيار **ترحيل إيصالات استلام المنتجات إلى دفتر الأستاذ**.</span><span class="sxs-lookup"><span data-stu-id="a5561-116">For items, on the **Accounts payable parameters** page, select the **Post product receipts to ledger** option.</span></span>
<span data-ttu-id="a5561-117">[![الاستحقاقات1](./media/accruals1-1024x409.png)](./media/accruals1.png)</span><span class="sxs-lookup"><span data-stu-id="a5561-117">[![accruals1](./media/accruals1-1024x409.png)](./media/accruals1.png)</span></span> 

<span data-ttu-id="a5561-118">بالنسبة لفئات المشتريات، على صفحة **قاعدة سياسة الفئة**، حدد السياسات **الشرائية**، ومن ثم حدد **استحقاق مصروفات الشراء عند الاستلام** لكل فئة تدبير.</span><span class="sxs-lookup"><span data-stu-id="a5561-118">For procurement categories, on the **Category policy rule** page, select **Purchasing** policies, and then select **Accrue purchase expense on receipt** for each procurement category.</span></span>
<span data-ttu-id="a5561-119">[![استحقاقات2](./media/accruals2-1024x569.png)](./media/accruals2.png)</span><span class="sxs-lookup"><span data-stu-id="a5561-119">[![accruals2](./media/accruals2-1024x569.png)](./media/accruals2.png)</span></span> 

<span data-ttu-id="a5561-120">سوف تستخدم حسابات **نفقات الشراء غير المفوترة** و **استحقاق الشراء** في **إعداد الترحيل** عند ترحيل الإيصالات المتعلقة باستلام المنتجات.</span><span class="sxs-lookup"><span data-stu-id="a5561-120">The **Purchase expenditure un-invoiced** and **Purchase accrual** accounts in **Posting setup** will be used when vouchers that are related to the product receipt are posted.</span></span>
<span data-ttu-id="a5561-121">[![استحقاقات3](./media/accruals3-1024x429.png)](./media/accruals3.png)</span><span class="sxs-lookup"><span data-stu-id="a5561-121">[![accruals3](./media/accruals3-1024x429.png)](./media/accruals3.png)</span></span> 

<span data-ttu-id="a5561-122">باستخدام نفس السيناريو، لنرى كيف سيؤثر ترحيل إيصال منتج على دفتر الأستاذ العام ومعلومات المشروع.</span><span class="sxs-lookup"><span data-stu-id="a5561-122">Using this same scenario, let's see how posting a product receipt will impact General ledger and Project information.</span></span> 

<span data-ttu-id="a5561-123">**الخطوة 1:** إنشاء وتأكيد أمر شراء جديد للمشروع لتسجيل شراء كمبيوتر بسرع 1500 دولار وخدمات تركيب بسعر 150 دولار.</span><span class="sxs-lookup"><span data-stu-id="a5561-123">**Step 1:** Create and confirm a new purchase order for the project to record the purchase of a computer for $1500 and installation services for $150.</span></span>
<span data-ttu-id="a5561-124">[![استحقاقات4](./media/accruals4-1024x497.png)](./media/accruals4.png)</span><span class="sxs-lookup"><span data-stu-id="a5561-124">[![accruals4](./media/accruals4-1024x497.png)](./media/accruals4.png)</span></span> 

<span data-ttu-id="a5561-125">عند تأكيد أمر الشراء، يتم إنشاء حركات للتكلفة الإلزامية الخاصة بالمشروع.</span><span class="sxs-lookup"><span data-stu-id="a5561-125">When the purchase order is confirmed, transactions for the committed cost are created for the project.</span></span> 
<span data-ttu-id="a5561-126">[![استحقاقات5](./media/accruals5-1024x219.png)](./media/accruals5.png)</span><span class="sxs-lookup"><span data-stu-id="a5561-126">[![accruals5](./media/accruals5-1024x219.png)](./media/accruals5.png)</span></span> 

> [!NOTE]
> <span data-ttu-id="a5561-127">سوف يكون للحركات المخصصة للتكلفة الإلزامية حقل **"أصل الحركة"** والذي يتم تعيينه إلى **"أمر الشراء"**.</span><span class="sxs-lookup"><span data-stu-id="a5561-127">The transactions for the committed cost will have the **Transaction Origin** field set to **Purchase Order**.</span></span> <span data-ttu-id="a5561-128">لا يؤدي إنشاء وتأكيد أمر شراء إلى إنشاء حركات لمشروع.</span><span class="sxs-lookup"><span data-stu-id="a5561-128">Creating and confirming a purchase order does not create transactions for a project.</span></span> 

<span data-ttu-id="a5561-129">**الخطوة 2:** تم تسليم البضائع والخدمات، وتم تسجيل استلام منتج.</span><span class="sxs-lookup"><span data-stu-id="a5561-129">**Step 2:** Goods and services get delivered and a product receipt is registered.</span></span> 

<span data-ttu-id="a5561-130">سوف يؤدي ترحيل استلام منتج إلى إنشاء وترحيل إيصال إلى دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="a5561-130">Posting a product receipt will generate and post a voucher to the ledger.</span></span> <span data-ttu-id="a5561-131">سوف يقوم الإيصال بخصم نفقات الشراء والحسابات غير المفوترة وحساب استحقاق شراء الائتمان.</span><span class="sxs-lookup"><span data-stu-id="a5561-131">The voucher will debit the purchase expenditure, un-invoiced account, and credit purchase accrual account.</span></span> 
<span data-ttu-id="a5561-132">[![استحقاقات6](./media/accruals6-1024x214.png)](./media/accruals6.png)</span><span class="sxs-lookup"><span data-stu-id="a5561-132">[![accruals6](./media/accruals6-1024x214.png)](./media/accruals6.png)</span></span>

> [!NOTE]
> <span data-ttu-id="a5561-133">سوف يستخدم ترحيل إيصال إعداد الترحيل لفئات التدبير والمنتجات، ولن يقوم بترحيل الإعداد لفئات المشروع.</span><span class="sxs-lookup"><span data-stu-id="a5561-133">Posting a product receipt will use the posting setup for procurement categories and products, and not the posting setup for the project categories.</span></span> <span data-ttu-id="a5561-134">ولإظهار الأثر المالي لاستحقاقات الشراء بشكل صحيح، يلزم محاذاة هذا الإعداد.</span><span class="sxs-lookup"><span data-stu-id="a5561-134">In order to correctly reflect financial impact of purchase accruals, this setup needs to be aligned.</span></span> 

<span data-ttu-id="a5561-135">من الممكن تعيين فئات التدبير لفئات المشروع على **فئة التدبير**.</span><span class="sxs-lookup"><span data-stu-id="a5561-135">It is possible to map procurement categories to project categories on the **Procurement category** page.</span></span>
<span data-ttu-id="a5561-136">[![استحقاقات7](./media/accruals7-1024x390.png)](./media/accruals7.png)</span><span class="sxs-lookup"><span data-stu-id="a5561-136">[![accruals7](./media/accruals7-1024x390.png)](./media/accruals7.png)</span></span>

<span data-ttu-id="a5561-137">**خطوة 3:** إنشاء مسودة فاتورة مورد.</span><span class="sxs-lookup"><span data-stu-id="a5561-137">**Step 3:** Create a draft vendor invoice.</span></span> 

<span data-ttu-id="a5561-138">في Finance and Operations، لا يؤثر ترحيل إيصال منتج على معلومات المشروع.</span><span class="sxs-lookup"><span data-stu-id="a5561-138">In Finance and Operations, posting a product receipt does not impact project information.</span></span> <span data-ttu-id="a5561-139">وكحل لهذا الأمر، يمكنك إنشاء مسودة فاتورة مورد مباشرة بعد ترحيل إيصال الشراء.</span><span class="sxs-lookup"><span data-stu-id="a5561-139">As a workaround, you could generate a draft vendor invoice right after posting the purchase receipt.</span></span> <span data-ttu-id="a5561-140">انتقل إلى صفحة **أمر الشراء** &gt; **علامة تبويب الفاتورة** &gt; **إنشاء** &gt; **الفاتورة**.</span><span class="sxs-lookup"><span data-stu-id="a5561-140">Go to the **Purchase Order** page &gt; **Invoice tab** &gt; **Generate** &gt; **Invoice**.</span></span> <span data-ttu-id="a5561-141">يؤدي هذا إلى إنشاء مستند فاتورة معلقة تُحدث معلومات المشروع.</span><span class="sxs-lookup"><span data-stu-id="a5561-141">This creates a pending invoice document that updates project information.</span></span> 

<span data-ttu-id="a5561-142">سوف يؤدي إنشاء مسودة فاتورة مورد إلى إنشاء حركات مشروع معلقة.</span><span class="sxs-lookup"><span data-stu-id="a5561-142">Creating a draft vendor invoice will generate pending project transactions.</span></span> 
<span data-ttu-id="a5561-143">[![استحقاقات8](./media/accruals8-1024x225.png)](./media/accruals8.png)</span><span class="sxs-lookup"><span data-stu-id="a5561-143">[![accruals8](./media/accruals8-1024x225.png)](./media/accruals8.png)</span></span> 

<span data-ttu-id="a5561-144">في صفحة **التكلفة الإلزامية**، سيتم إغلاق السجلات التي تم إنشاؤها في الخطوة 1 وسيتم إنشاء سجلات جديدة لتعكس التزام التكلفة الوارد من فاتورة المورد المعلقة.</span><span class="sxs-lookup"><span data-stu-id="a5561-144">In the **Committed cost** page, records created in step 1 will be closed and new records will be created to reflect cost commitment coming from the pending vendor invoice.</span></span> <span data-ttu-id="a5561-145">سوف يتم تعيين حقل **أصل الحركة** للتكلفة الإلزامية إلى **فاتورة المورد**.</span><span class="sxs-lookup"><span data-stu-id="a5561-145">The **Transaction origin** field for the committed cost will be set to **Vendor invoice**.</span></span>
<span data-ttu-id="a5561-146">[![استحقاقات9](./media/accruals9-1024x200.png)](./media/accruals9.png)</span><span class="sxs-lookup"><span data-stu-id="a5561-146">[![accruals9](./media/accruals9-1024x200.png)](./media/accruals9.png)</span></span>

<span data-ttu-id="a5561-147">سوف تظل فاتورة المورد في وضع معلق حتى وصول فاتور المورد الفعلية.</span><span class="sxs-lookup"><span data-stu-id="a5561-147">The vendor invoice will remain in a pending state until the actual vendor invoice arrives.</span></span>



