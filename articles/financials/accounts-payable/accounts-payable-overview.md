---
title: "تكوين الحسابات الدائنة"
description: "تصف هذه المقالة الصفحات التي تستخدمها لإعداد الوظائف الأساسية والاختيارية للحسابات الدائنة في Microsoft Dynamics 365 for Finance and Operations, Enterprise edition. وتصف أيضًا خطوات الإعداد التي يجب إكمالها قبل بدء إعداد الحسابات الدائنة."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankAccountTable, DeliveryMode, PaymTerm, VendGroup, VendParameters, VendPaymMode, VendTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 24671
ms.assetid: 82561fe7-b2d6-464c-9347-79d0ce0f9743
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 49e5c81dda8434a6e02106a8d7ee10233e43d172
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="configure-accounts-payable"></a><span data-ttu-id="6ea03-104">تكوين الحسابات الدائنة</span><span class="sxs-lookup"><span data-stu-id="6ea03-104">Configure Accounts payable</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6ea03-105">تصف هذه المقالة الصفحات التي تستخدمها لإعداد الوظائف الأساسية والاختيارية للحسابات الدائنة في Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span><span class="sxs-lookup"><span data-stu-id="6ea03-105">This article describes the pages that you use to set up basic and optional functionality for Accounts payable in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> <span data-ttu-id="6ea03-106">وتصف أيضًا خطوات الإعداد التي يجب إكمالها قبل بدء إعداد الحسابات الدائنة.</span><span class="sxs-lookup"><span data-stu-id="6ea03-106">It also describes setup steps that you must complete before you start to set up Accounts payable.</span></span>

<a name="prerequisites-for-accounts-payable-setup"></a><span data-ttu-id="6ea03-107">المتطلبات الأساسية لإعداد الحسابات الدائنة</span><span class="sxs-lookup"><span data-stu-id="6ea03-107">Prerequisites for Accounts payable setup</span></span>
----------------------------------------

<span data-ttu-id="6ea03-108">قبل أن يمكنك إعداد الحسابات الدائنة، يجب عليك إكمال الإعداد التالي:</span><span class="sxs-lookup"><span data-stu-id="6ea03-108">Before you can set up Accounts payable, you must complete the following setup:</span></span>

-   <span data-ttu-id="6ea03-109">في دفتر الأستاذ العام:</span><span class="sxs-lookup"><span data-stu-id="6ea03-109">In General ledger:</span></span>
    -   <span data-ttu-id="6ea03-110">في حالة قيامك بالتخطيط لاستخدام دفاتر يومية المدفوعات، فقم إعداد دفاتر يومية المدفوعات.</span><span class="sxs-lookup"><span data-stu-id="6ea03-110">If you plan to use payment journals, set up payment journals.</span></span>
    -   <span data-ttu-id="6ea03-111">إذا كنت تخطط لإجراء تسويات سعر الصرف، فقم بإعداد أكواد العملة في صفحة العملات، وقم بإعداد أنواع سعر الصرف في صفحة أنواع سعر الصرف، وقم بإعداد أسعار صرف العملات في صفحة أسعار صرف العملة.</span><span class="sxs-lookup"><span data-stu-id="6ea03-111">If you plan to run exchange rate adjustments, set up currency codes on the Currencies page, set up exchange rate types on the Exchange rate types page, and set up currency exchange rates on the Currency exchange rates page.</span></span>
-   <span data-ttu-id="6ea03-112">في إدارة النقد والبنوك، قم بإعداد الحسابات البنكية المراد استخدامها مع طرق الدفع.</span><span class="sxs-lookup"><span data-stu-id="6ea03-112">In Cash and bank management, set up bank accounts to use with methods of payment.</span></span>

## <a name="setup-pages-for-accounts-payable"></a><span data-ttu-id="6ea03-113">إعداد الصفحات للحسابات الدائنة</span><span class="sxs-lookup"><span data-stu-id="6ea03-113">Setup pages for Accounts payable</span></span>

<span data-ttu-id="6ea03-114">استخدم الصفحات التالية لإعداد الوظيفة الرئيسية للحسابات الدائنة لكل كيان قانوني.</span><span class="sxs-lookup"><span data-stu-id="6ea03-114">Use the following pages to set up the basic functionality of Accounts payable for each legal entity.</span></span> <span data-ttu-id="6ea03-115">ويتم سرد الصفحات حسب الترتيب الموصى به للإعداد.</span><span class="sxs-lookup"><span data-stu-id="6ea03-115">The pages are listed in the recommended order of setup.</span></span> <span data-ttu-id="6ea03-116">لتسهيل عملية الإعداد، فإنه يمكنك إنشاء قوالب من السجلات الأولى التي تقوم بإنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="6ea03-116">To make the setup process easier, you can create templates from the first records that you create.</span></span> <span data-ttu-id="6ea03-117">وفي القالب، يتم عادةً إدخال القيم في العديد من الحقول لتعكس الميزات التي ترغب المؤسسة في تنفيذها لنوعية محددة من الموردين.</span><span class="sxs-lookup"><span data-stu-id="6ea03-117">In a template, values are typically entered in many fields to reflect the features that the organization wants to implement for a particular type of vendor.</span></span>
1.  <span data-ttu-id="6ea03-118">في صفحة شروط الدفع، حدد شروط الدفع التي تقوم بتعيينها لأوامر المبيعات، وأوامر الشراء، والعملاء، والموردين، والتي تحدد تواريخ استحقاق الفواتير.</span><span class="sxs-lookup"><span data-stu-id="6ea03-118">On the Terms of payment page, define the terms of payment that you assign to sales orders, purchase orders, customers, and vendors, and that determine invoice due dates.</span></span> <span data-ttu-id="6ea03-119">للحصول على مزيد من المعلومات، راجع [تحديد رسوم دفع المورّد](tasks/define-vendor-payment-fees.md).</span><span class="sxs-lookup"><span data-stu-id="6ea03-119">For more information, see [Define vendor payment fees](tasks/define-vendor-payment-fees.md).</span></span>
2.  <span data-ttu-id="6ea03-120">في صفحة طرق الدفع - الموردون، قم بإنشاء والاحتفاظ بمعلومات حول كيفية دفع المؤسسة للموردين الخاصين بها.</span><span class="sxs-lookup"><span data-stu-id="6ea03-120">On the Methods of payment - vendors page, create and maintain information about how the organization pays its vendors.</span></span>
3.  <span data-ttu-id="6ea03-121">في صفحة مجموعات الموردين، قم بإنشاء والاحتفاظ بمجموعات الموردين الذين يتشاركون في المعلمات المهمة الخاصة بالترحيل، والتسوية والدفع، وإعداد التقارير، والتنبؤ.</span><span class="sxs-lookup"><span data-stu-id="6ea03-121">On the Vendor groups page, create and maintain groups of vendors that share important parameters for posting, settlement and payment, reporting, and forecasting.</span></span>
4.  <span data-ttu-id="6ea03-122">في صفحة ملفات تعريف ترحيل الموردين، حدد طريقة ترحيل حركات الموردين إلى دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="6ea03-122">On the Vendor posting profiles page, define how vendor transactions are posted to the general ledger.</span></span>
5.  <span data-ttu-id="6ea03-123">في صفحة معلمات الحسابات الدائنة، قم بإعداد الإعدادات الافتراضية التي يتم تطبيقها في حالة عدم تحديد إعداد أكثر تحديدًا، ومعلمات لأنواع متعددة من الوظائف، والمسلسلات الرقمية المتعددة للحسابات الدائنة.</span><span class="sxs-lookup"><span data-stu-id="6ea03-123">On the Accounts payable parameters page, set up default settings that are applied if a more specific setting isn't specified, parameters for various kinds of functionality, and the various number sequences for Accounts payable.</span></span>
6.  <span data-ttu-id="6ea03-124">في صفحة إعداد النماذج، حدد التنسيق الخاص بالمستندات المتعددة المتعلقة بالموردين والتي تستخدمها المؤسسة لتتبع عمليات الاستلام من الموردين وإدخال أسباب تدفق المدفوعات إلى الموردين.</span><span class="sxs-lookup"><span data-stu-id="6ea03-124">On the Form setup page, define the format of various documents that are related to vendors, and that the organization uses to keep track of receipts from vendors and enter reasons for the flow of payments to vendors.</span></span>
7.  <span data-ttu-id="6ea03-125">في صفحة الموردين، قم بإنشاء والاحتفاظ بحسابات الموردين، وكذلك الهيئات الضريبية التي تقوم مؤسستك بتقديم تقارير ضرائب المبيعات إليها.</span><span class="sxs-lookup"><span data-stu-id="6ea03-125">On the Vendors page, create and maintain vendor accounts, and also the tax authorities that your organization reports sales taxes to.</span></span>

## <a name="optional-setup-pages-for-accounts-payable"></a><span data-ttu-id="6ea03-126">صفحات الإعداد الاختياري للحسابات الدائنة</span><span class="sxs-lookup"><span data-stu-id="6ea03-126">Optional setup pages for Accounts payable</span></span>
<span data-ttu-id="6ea03-127">بالإضافة إلى الوظائف الأساسية، تشتمل الحسابات الدائنة على وظائف أخرى يمكنك إعدادها.</span><span class="sxs-lookup"><span data-stu-id="6ea03-127">In addition to the basic functionality, Accounts payable has other functionality that you can set up.</span></span>

<span data-ttu-id="6ea03-128">يتم تنظيم صفحات الإعداد الإضافية حسب الوظائف الأساسية.</span><span class="sxs-lookup"><span data-stu-id="6ea03-128">The additional setup pages are organized by functionality.</span></span>

<span data-ttu-id="6ea03-129">**السياسات**</span><span class="sxs-lookup"><span data-stu-id="6ea03-129">**Policies**</span></span>
-   <span data-ttu-id="6ea03-130">في صفحة سياسة فاتورة المورد، قم بإعداد سياسات فاتورة المورد.</span><span class="sxs-lookup"><span data-stu-id="6ea03-130">On the Vendor invoice policy page, set up vendor invoice policies.</span></span>

<span data-ttu-id="6ea03-131">**مطابقة الفاتورة**</span><span class="sxs-lookup"><span data-stu-id="6ea03-131">**Invoice matching**</span></span>

-   <span data-ttu-id="6ea03-132">في صفحة تفاوتات إجماليات الفواتير، قم بإعداد التفاوتات لإجماليات الفواتير.</span><span class="sxs-lookup"><span data-stu-id="6ea03-132">On the Invoice totals tolerances page, set up tolerances for invoice totals.</span></span>
-   <span data-ttu-id="6ea03-133">في صفحة سياسة المطابقة، قم بإعداد سياسات المطابقة الثنائية والثلاثية.</span><span class="sxs-lookup"><span data-stu-id="6ea03-133">On the Matching policy page, set up two-way and three-way matching policies.</span></span>
-   <span data-ttu-id="6ea03-134">في صفحة تفاوتات الأسعار، قم بإعداد التفاوتات لأسعار الوحدة.</span><span class="sxs-lookup"><span data-stu-id="6ea03-134">On the Price tolerances page, set up tolerances for unit prices.</span></span>
-   <span data-ttu-id="6ea03-135">في صفحة مجموعات تفاوت سعر الصنف، قم بإعداد مجموعات التفاوتات لأسعار الأصناف.</span><span class="sxs-lookup"><span data-stu-id="6ea03-135">On the Item price tolerance groups page, set up tolerance groups for item prices.</span></span>
-   <span data-ttu-id="6ea03-136">في صفحة مجموعات تفاوتات أسعار الموردين، قم بإعداد مجموعات التفاوتات لأسعار الموردين.</span><span class="sxs-lookup"><span data-stu-id="6ea03-136">On the Vendor price tolerance groups page, set up  tolerance groups for vendor prices.</span></span>
-   <span data-ttu-id="6ea03-137">في صفحة تفاوتات المصاريف، قم بإعداد التفاوتات للمصاريف.</span><span class="sxs-lookup"><span data-stu-id="6ea03-137">On the Charges tolerances page, set up tolerances for charges.</span></span>

<span data-ttu-id="6ea03-138">**سير العمل**</span><span class="sxs-lookup"><span data-stu-id="6ea03-138">**Workflow**</span></span>

-   <span data-ttu-id="6ea03-139">في صفحة عمليات سير عمل الحسابات الدائنة، قم بإعداد تكوينات سير العمل لاعتمادات دفتر اليومية وطلبات الشراء.</span><span class="sxs-lookup"><span data-stu-id="6ea03-139">On the Accounts payable workflows page, set up workflow configurations for journal approvals and purchase requisitions.</span></span>

<span data-ttu-id="6ea03-140">**الأسباب**</span><span class="sxs-lookup"><span data-stu-id="6ea03-140">**Reasons**</span></span>

-   <span data-ttu-id="6ea03-141">في صفحة أسباب المورد، قم بإعداد أكواد السبب.</span><span class="sxs-lookup"><span data-stu-id="6ea03-141">On the Vendor reasons page, set up reason codes.</span></span>

<span data-ttu-id="6ea03-142">**المصاريف**</span><span class="sxs-lookup"><span data-stu-id="6ea03-142">**Charges**</span></span>

-   <span data-ttu-id="6ea03-143">في صفحة كود المصاريف، قم بإعداد أكواد للمصاريف التي يتم استخدامها في أوامر الشراء.</span><span class="sxs-lookup"><span data-stu-id="6ea03-143">On the Charges code page, set up codes for the charges that are used in purchase orders.</span></span>
-   <span data-ttu-id="6ea03-144">في صفحة مجموعة مصاريف الموردين، قم بإنشاء وصيانة مجموعات المصاريف للموردين.</span><span class="sxs-lookup"><span data-stu-id="6ea03-144">On the Vendor charges group page, create and maintain charges groups for vendors.</span></span>
-   <span data-ttu-id="6ea03-145">في صفحة مجموعة مصاريف الأصناف،قم بإنشاء وصيانة مجموعات المصاريف للأصناف.</span><span class="sxs-lookup"><span data-stu-id="6ea03-145">On the Item charge groups page, create and maintain charges groups for items.</span></span>
-   <span data-ttu-id="6ea03-146">في صفحة المصاريف التلقائية، حدد المصاريف التي يتم تعيينها للأوامر تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="6ea03-146">On the Auto charges page, define the charges that are automatically assigned to orders.</span></span>

<span data-ttu-id="6ea03-147">**الأصناف المكملة**</span><span class="sxs-lookup"><span data-stu-id="6ea03-147">**Supplementary items**</span></span>

-   <span data-ttu-id="6ea03-148">في مجموعات الأصناف التكميلية في صفحة - المورد،قم بإنشاء وصيانة مجموعات الأصناف المكملة للموردين.</span><span class="sxs-lookup"><span data-stu-id="6ea03-148">On the Supplementary item groups - Vendor page, create and maintain supplementary item groups for vendors.</span></span>
-   <span data-ttu-id="6ea03-149">في مجموعات الأصناف التكميلية في صفحة - المخزون،قم بإنشاء وصيانة مجموعات الأصناف المكلمة للأصناف.</span><span class="sxs-lookup"><span data-stu-id="6ea03-149">On the Supplementary item groups - Inventory page, create and maintain supplementary item groups for items.</span></span>

<span data-ttu-id="6ea03-150">**التوزيع**</span><span class="sxs-lookup"><span data-stu-id="6ea03-150">**Distribution**</span></span>

-   <span data-ttu-id="6ea03-151">في صفحة شروط التسليم،قم بإنشاء شروط تحويل أحد الأصناف من البائع إلى المشتري والاحتفاظ بها.</span><span class="sxs-lookup"><span data-stu-id="6ea03-151">On the Terms of delivery page, create and maintain the conditions for an item's transfer from seller to buyer.</span></span>
-   <span data-ttu-id="6ea03-152">في صفحة طرق التسليم،قم بإنشاء وسائل النقل المستخدمة عند تسليم أحد الأوامر من البائع إلى المشتري والاحتفاظ بها.</span><span class="sxs-lookup"><span data-stu-id="6ea03-152">On the Modes of delivery page, create and maintain the methods of transport that are used when an order is delivered from the seller to the buyer.</span></span>
-   <span data-ttu-id="6ea03-153">في صفحة أكواد الوجهة،قم بإنشاء معرفات وأوصاف لوجهات التسليم والاحتفاظ بها.</span><span class="sxs-lookup"><span data-stu-id="6ea03-153">On the Destination codes page, create and maintain identifiers and descriptions for delivery destinations.</span></span>

<span data-ttu-id="6ea03-154">**النماذج**</span><span class="sxs-lookup"><span data-stu-id="6ea03-154">**Forms**</span></span>

-   <span data-ttu-id="6ea03-155">في صفحة نماذج الإشعارات،قم بإنشاء النص القياسي الذي يظهر في صفحات متنوعة.</span><span class="sxs-lookup"><span data-stu-id="6ea03-155">On the Form notes page, create the standard text that appears on various pages.</span></span>
-   <span data-ttu-id="6ea03-156">في صفحة محددات فرز النماذج،قم بإعداد ترتيبات الفرز للطلبات، وقوائم الاستلام، وإيصالات التعبئة، والفواتير.</span><span class="sxs-lookup"><span data-stu-id="6ea03-156">On the Form sorting parameters page, set up the sorting order for requisitions, receipt lists, packing slips, and invoices.</span></span>
-   <span data-ttu-id="6ea03-157">في صفحة إعداد إدارة الطباعة، قم بإعداد معلومات إدارة الطباعة لأصول ونسخ الصفحات.</span><span class="sxs-lookup"><span data-stu-id="6ea03-157">On the Print management setup page, set up print management information for originals and copies of pages.</span></span>

<span data-ttu-id="6ea03-158">**المدفوعات**</span><span class="sxs-lookup"><span data-stu-id="6ea03-158">**Payments**</span></span>

-   <span data-ttu-id="6ea03-159">في صفحة الخصومات النقدية،قم بإعداد وإدارة الشروط الخاصة بالحصول على الخصومات النقدية.</span><span class="sxs-lookup"><span data-stu-id="6ea03-159">On the Cash discounts page, set up and manage the terms for obtaining cash discounts.</span></span> <span data-ttu-id="6ea03-160">يتم ربط أكواد الخصومات النقدية بالموردين وتُطبق على أوامر الشراء.</span><span class="sxs-lookup"><span data-stu-id="6ea03-160">The cash discount codes are linked to vendors and are applied to purchase orders.</span></span>
-   <span data-ttu-id="6ea03-161">في صفحة جداول الدفع، قم بإعداد جداول الدفع التي يتم استخدامها لإدارة دفعات الأقساط للموردين.</span><span class="sxs-lookup"><span data-stu-id="6ea03-161">On the Payment schedules page, set up the payment schedules that are used to manage installment payments to vendors.</span></span>
-   <span data-ttu-id="6ea03-162">في صفحة أيام الدفع، قم بتحديد أيام الدفع المستخدمة في حساب تواريخ الاستحقاق وتحديد أيام دفع ليوم محدد في الأسبوع أو الشهر.</span><span class="sxs-lookup"><span data-stu-id="6ea03-162">On the Payment days page, define the payment days that are used to calculate due dates, and specify payment days for a specific day of the week or month.</span></span>
-   <span data-ttu-id="6ea03-163">في صفحة رسوم الدفع، قم بإنشاء رسوم الدفع المتعلقة بالموردين والاحتفاظ بها.</span><span class="sxs-lookup"><span data-stu-id="6ea03-163">On the Payment fee page, create and maintain the payment fees that are associated with vendors.</span></span>
-   <span data-ttu-id="6ea03-164">في صفحة تعليمات الدفع، قم بإنشاء وصيانة تعليمات الدفع.</span><span class="sxs-lookup"><span data-stu-id="6ea03-164">On the Payment instruction page, create and maintain payment instructions.</span></span>

<span data-ttu-id="6ea03-165">**الإحصاءات**</span><span class="sxs-lookup"><span data-stu-id="6ea03-165">**Statistics**</span></span>

-   <span data-ttu-id="6ea03-166">في صفحة تعريفات فترة التقادم، قم بإعداد فواصل زمنية محددة بواسطة المستخدم لتحليل توزيع الاستحقاق لحسابات الموردين.</span><span class="sxs-lookup"><span data-stu-id="6ea03-166">On the Aging period definitions page, set up user-defined intervals that are used to analyze the maturity distribution of vendor accounts.</span></span>
-   <span data-ttu-id="6ea03-167">في صفحة نوع العمل، قم بإنشاء أكواد نوع العمل (LOB) التي تم تعيينها للموردين.</span><span class="sxs-lookup"><span data-stu-id="6ea03-167">On the Line of business page, create the line of business (LOB) codes that are assigned to vendors.</span></span>

<span data-ttu-id="6ea03-168">**ضريبة 1099**</span><span class="sxs-lookup"><span data-stu-id="6ea03-168">**Tax 1099**</span></span>

-   <span data-ttu-id="6ea03-169">في صفحة **حقول 1099**، قم بالتحقق من وتحديث الحد الأدنى من المبالغ التي يجب الإبلاغ عنها لخدمة الإيرادات الداخلية (IRS)، استناداً إلى آخر متطلبات IRS.</span><span class="sxs-lookup"><span data-stu-id="6ea03-169">On the **1099 fields** page, verify and update the minimum amounts that must be reported to the Internal Revenue Service (IRS), based on the latest IRS requirements.</span></span>

## <a name="optional-setup-for-other-modules"></a><span data-ttu-id="6ea03-170">**الإعداد الاختياري للوحدات الأخرى**</span><span class="sxs-lookup"><span data-stu-id="6ea03-170">**Optional setup for other modules**</span></span>
<span data-ttu-id="6ea03-171">**إدارة المؤسسة**</span><span class="sxs-lookup"><span data-stu-id="6ea03-171">**Organization administration**</span></span>

-   <span data-ttu-id="6ea03-172">في صفحة المسلسلات الرقمية، قم بإعداد مجموعات المسلسلات الرقمية لأرقام الفواتير.</span><span class="sxs-lookup"><span data-stu-id="6ea03-172">On the Number sequences page, set up number sequence groups for invoice numbers.</span></span>
-   <span data-ttu-id="6ea03-173">في الصفحات التالية، قم بإعداد معلومات العنوان:</span><span class="sxs-lookup"><span data-stu-id="6ea03-173">On the following pages, set up address information:</span></span>
    -   <span data-ttu-id="6ea03-174">إعداد العنوان</span><span class="sxs-lookup"><span data-stu-id="6ea03-174">Address setup</span></span>
    -   <span data-ttu-id="6ea03-175">أكواد NAF</span><span class="sxs-lookup"><span data-stu-id="6ea03-175">NAF codes</span></span>
    -   <span data-ttu-id="6ea03-176">استيراد الأكواد /الأرقام البريدية</span><span class="sxs-lookup"><span data-stu-id="6ea03-176">Import ZIP/postal codes</span></span>

<span data-ttu-id="6ea03-177">**دفتر الأستاذ العام**</span><span class="sxs-lookup"><span data-stu-id="6ea03-177">**General ledger**</span></span>

-   <span data-ttu-id="6ea03-178">صفحة الأبعاد المالية، قم بتحديد الأبعاد المالية.</span><span class="sxs-lookup"><span data-stu-id="6ea03-178">On the Financial dimensions page, set up financial dimensions.</span></span>
-   <span data-ttu-id="6ea03-179">في الصفحات التالية، قم بإعداد معلومات الضريبة:</span><span class="sxs-lookup"><span data-stu-id="6ea03-179">On the following pages, set up tax information:</span></span>
    -   <span data-ttu-id="6ea03-180">أكواد ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="6ea03-180">Sales tax codes</span></span>
    -   <span data-ttu-id="6ea03-181">مجموعات ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="6ea03-181">Sales tax groups</span></span>
    -   <span data-ttu-id="6ea03-182">مجموعات ضريبة المبيعات للأصناف</span><span class="sxs-lookup"><span data-stu-id="6ea03-182">Item sales tax groups</span></span>
    -   <span data-ttu-id="6ea03-183">مجموعة الحساب</span><span class="sxs-lookup"><span data-stu-id="6ea03-183">Account group</span></span>
    -   <span data-ttu-id="6ea03-184">أكواد الإعفاء من ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="6ea03-184">Sales tax exempt codes</span></span>
    -   <span data-ttu-id="6ea03-185">سلطات ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="6ea03-185">Sales tax jurisdictions</span></span>
    -   <span data-ttu-id="6ea03-186">هيئات ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="6ea03-186">Sales tax authorities</span></span>
    -   <span data-ttu-id="6ea03-187">فترات تسوية ضرائب المبيعات</span><span class="sxs-lookup"><span data-stu-id="6ea03-187">Sales tax settlement periods</span></span>

<span data-ttu-id="6ea03-188">**إدارة النقد والبنوك**</span><span class="sxs-lookup"><span data-stu-id="6ea03-188">**Cash and bank management**</span></span>

-   <span data-ttu-id="6ea03-189">في صفحة أكواد أغراض الدفع، قم بإعداد كود غرض البنك المركزي.</span><span class="sxs-lookup"><span data-stu-id="6ea03-189">On the Payment purpose codes page, set up the Central Bank purpose code.</span></span>






