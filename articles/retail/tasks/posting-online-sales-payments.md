---
title: ترحيل الدفعات والمبيعات على الإنترنت
description: يتناول هذا الإجراء تكوين وظيفة دفعية متكررة وتشغيلها لإنشاء أوامر الشراء والمدفوعات لحركات المتجر على الإنترنت.
author: psimolin
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1d42b585a61214628980cd45a859215443ed55b5
ms.sourcegitcommit: c461758290d7ddc19f0b60701368937c35ef78b0
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/06/2019
ms.locfileid: "1864143"
---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="e48e8-103">ترحيل الدفعات والمبيعات على الإنترنت</span><span class="sxs-lookup"><span data-stu-id="e48e8-103">Posting of online sales and payments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="e48e8-104">يتناول هذا الإجراء تكوين وظيفة دفعية متكررة وتشغيلها لإنشاء أوامر الشراء والمدفوعات لحركات المتجر على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="e48e8-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span>

<span data-ttu-id="e48e8-105">إن ترحيل المبيعات والمدفوعات عبر الإنترنت عبارة عن عملية من مرحلتين.</span><span class="sxs-lookup"><span data-stu-id="e48e8-105">Posting online sales and payments is a two-stage process.</span></span>

- <span data-ttu-id="e48e8-106">سحب بيانات حركه البيع بالتجزئة عبر الإنترنت إلى HQ.</span><span class="sxs-lookup"><span data-stu-id="e48e8-106">Pulling the online retail transaction data in HQ.</span></span>
- <span data-ttu-id="e48e8-107">مزامنة الأوامر لإنشاء أوامر بيع في HQ.</span><span class="sxs-lookup"><span data-stu-id="e48e8-107">Synchronizing orders to create sales orders in HQ.</span></span>

<span data-ttu-id="e48e8-108">يمكن سحب بيانات حركه البيع بالتجزئة عبر الإنترنت إما عن طريق تشغيل الوظيفة P يدويًا أو عن طريق إنشاء وظيفة دفعية متكررة.</span><span class="sxs-lookup"><span data-stu-id="e48e8-108">Pulling the online retail transaction data can be done either by manually running the P-job or by creating a recurrent batch job.</span></span>

### <a name="manually-running-the-p-job"></a><span data-ttu-id="e48e8-109">تشغيل الوظيفة P يدويًا</span><span class="sxs-lookup"><span data-stu-id="e48e8-109">Manually running the P-job</span></span>

1. <span data-ttu-id="e48e8-110">انتقل إلى كل مساحات العمل > تكنولوجيا معلومات البيع بالتجزئة‬.</span><span class="sxs-lookup"><span data-stu-id="e48e8-110">Go to All workspaces > Retail IT.</span></span>
2. <span data-ttu-id="e48e8-111">انقر فوق جدول التوزيع.</span><span class="sxs-lookup"><span data-stu-id="e48e8-111">Click Distribution schedule.</span></span>
3. <span data-ttu-id="e48e8-112">حدد P-0001.</span><span class="sxs-lookup"><span data-stu-id="e48e8-112">Select P-0001.</span></span>
4. <span data-ttu-id="e48e8-113">اضبط مجموعات قواعد بيانات القنوات، إذا كان ذلك مطلوبًا.</span><span class="sxs-lookup"><span data-stu-id="e48e8-113">Adjust channel database groups, if required.</span></span>
5. <span data-ttu-id="e48e8-114">انقر فوق تشغيل الآن.</span><span class="sxs-lookup"><span data-stu-id="e48e8-114">Click Run now.</span></span>
6. <span data-ttu-id="e48e8-115">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="e48e8-115">Click Yes.</span></span>

### <a name="scheduling-a-recurring-p-job"></a><span data-ttu-id="e48e8-116">جدولة وظيفة P متكررة</span><span class="sxs-lookup"><span data-stu-id="e48e8-116">Scheduling a recurring P-job</span></span>

1. <span data-ttu-id="e48e8-117">انتقل إلى كل مساحات العمل > تكنولوجيا معلومات البيع بالتجزئة‬.</span><span class="sxs-lookup"><span data-stu-id="e48e8-117">Go to All workspaces > Retail IT.</span></span>
2. <span data-ttu-id="e48e8-118">انقر فوق جدول التوزيع.</span><span class="sxs-lookup"><span data-stu-id="e48e8-118">Click Distribution schedule.</span></span>
3. <span data-ttu-id="e48e8-119">حدد P-0001.</span><span class="sxs-lookup"><span data-stu-id="e48e8-119">Select P-0001.</span></span>
4. <span data-ttu-id="e48e8-120">انقر فوق "إنشاء وظيفة دفعية".</span><span class="sxs-lookup"><span data-stu-id="e48e8-120">Click Create batch job.</span></span>
5. <span data-ttu-id="e48e8-121">انقر فوق "تشغيل في الخلفية".</span><span class="sxs-lookup"><span data-stu-id="e48e8-121">Click Run in the background.</span></span>
5. <span data-ttu-id="e48e8-122">مكّن "معالجة الدُفعات".</span><span class="sxs-lookup"><span data-stu-id="e48e8-122">Enable Batch processing.</span></span>
6. <span data-ttu-id="e48e8-123">انقر فوق "تكرار".</span><span class="sxs-lookup"><span data-stu-id="e48e8-123">Click Recurrence..</span></span>
7. <span data-ttu-id="e48e8-124">حدد الخيار "‏‫لا يوجد تاريخ انتهاء‬".</span><span class="sxs-lookup"><span data-stu-id="e48e8-124">Select the No end date option.</span></span>
8. <span data-ttu-id="e48e8-125">في حقل "الجرد"، أدخل الفاصل بين عمليات التشغيل بالدقائق.</span><span class="sxs-lookup"><span data-stu-id="e48e8-125">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="e48e8-126">يكون هذا عادةً 5-10.</span><span class="sxs-lookup"><span data-stu-id="e48e8-126">Typically this would be 5-10.</span></span>
9. <span data-ttu-id="e48e8-127">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="e48e8-127">Click OK.</span></span>
10. <span data-ttu-id="e48e8-128">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="e48e8-128">Click OK.</span></span>

<span data-ttu-id="e48e8-129">يمكن مزامنة الأوامر إما عن طريق تشغيل وظيفة "مزامنة الأوامر" يدويًا أو عن طريق إنشاء وظيفة دفعية متكررة.</span><span class="sxs-lookup"><span data-stu-id="e48e8-129">Orders can be synchronized either by manually running the "Synchronize orders"-job or by creating a recurring batch job.</span></span>

### <a name="manually-running-order-synchronization"></a><span data-ttu-id="e48e8-130">تشغيل مزامنة الأوامر يدويًا</span><span class="sxs-lookup"><span data-stu-id="e48e8-130">Manually running order synchronization</span></span> 

<span data-ttu-id="e48e8-131">اتبع هذه الخطوات لتشغيل وظيفة "مزامنة الأوامر" يدويًا مرة واحدة.</span><span class="sxs-lookup"><span data-stu-id="e48e8-131">Follow these steps to manually run "Synchronize orders" job once.</span></span>

1. <span data-ttu-id="e48e8-132">انتقل إلى كافة مساحات العمل > ماليات متجر البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="e48e8-132">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="e48e8-133">انقر فوق مزامنة الأوامر.</span><span class="sxs-lookup"><span data-stu-id="e48e8-133">Click Synchronize orders.</span></span>
3. <span data-ttu-id="e48e8-134">في حقل "‏‫التدرج الهرمي للمؤسسات‬"، حدد "متاجر البيع بالتجزئة حسب المنطقة".</span><span class="sxs-lookup"><span data-stu-id="e48e8-134">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="e48e8-135">حدد إما متجر معين على الإنترنت أو حدد عقدة إذا أردت إنشاء وظيفة دفعية لمجموعة من المتاجر.</span><span class="sxs-lookup"><span data-stu-id="e48e8-135">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="e48e8-136">انقر فوق السهم لإضافة التحديد الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="e48e8-136">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="e48e8-137">انقر فوق علامة التبويب "‏‫تشغيل في الخلفية".</span><span class="sxs-lookup"><span data-stu-id="e48e8-137">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="e48e8-138">تعطيل معالجة الدُفعات</span><span class="sxs-lookup"><span data-stu-id="e48e8-138">Disable Batch processing</span></span>
6. <span data-ttu-id="e48e8-139">انقر فوق "تكرار".</span><span class="sxs-lookup"><span data-stu-id="e48e8-139">Click Recurrence.</span></span>
7. <span data-ttu-id="e48e8-140">حدد الخيار "انتهاء بعد"</span><span class="sxs-lookup"><span data-stu-id="e48e8-140">Select End After option</span></span>
8. <span data-ttu-id="e48e8-141">في الحقل "انتهاء بعد"، أدخل 1.</span><span class="sxs-lookup"><span data-stu-id="e48e8-141">In the End After field, enter 1.</span></span>
9. <span data-ttu-id="e48e8-142">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="e48e8-142">Click OK.</span></span>
10. <span data-ttu-id="e48e8-143">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="e48e8-143">Click OK.</span></span>

### <a name="scheduling-recurring-order-synchronization"></a><span data-ttu-id="e48e8-144">جدولة مزامنة الأوامر المتكررة</span><span class="sxs-lookup"><span data-stu-id="e48e8-144">Scheduling recurring order synchronization</span></span>

<span data-ttu-id="e48e8-145">يتناول هذا الإجراء تكوين وظيفة دفعية متكررة وتشغيلها لإنشاء أوامر الشراء والمدفوعات لحركات المتجر على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="e48e8-145">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="e48e8-146">ويستخدم هذا الإجراء شركة USRT في بيانات العرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="e48e8-146">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="e48e8-147">انتقل إلى كافة مساحات العمل > ماليات متجر البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="e48e8-147">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="e48e8-148">انقر فوق مزامنة الأوامر.</span><span class="sxs-lookup"><span data-stu-id="e48e8-148">Click Synchronize orders.</span></span>
3. <span data-ttu-id="e48e8-149">في حقل "‏‫التدرج الهرمي للمؤسسات‬"، حدد "متاجر البيع بالتجزئة حسب المنطقة".</span><span class="sxs-lookup"><span data-stu-id="e48e8-149">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="e48e8-150">حدد إما متجر معين على الإنترنت أو حدد عقدة إذا أردت إنشاء وظيفة دفعية لمجموعة من المتاجر.</span><span class="sxs-lookup"><span data-stu-id="e48e8-150">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="e48e8-151">انقر فوق السهم لإضافة التحديد الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="e48e8-151">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="e48e8-152">انقر فوق علامة التبويب "‏‫تشغيل في الخلفية".</span><span class="sxs-lookup"><span data-stu-id="e48e8-152">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="e48e8-153">تمكين معالجة الدُفعات</span><span class="sxs-lookup"><span data-stu-id="e48e8-153">Enable Batch processing</span></span>
6. <span data-ttu-id="e48e8-154">انقر فوق "تكرار".</span><span class="sxs-lookup"><span data-stu-id="e48e8-154">Click Recurrence.</span></span>
7. <span data-ttu-id="e48e8-155">حدد الخيار "‏‫لا يوجد تاريخ انتهاء‬".</span><span class="sxs-lookup"><span data-stu-id="e48e8-155">Select the No end date option.</span></span>
8. <span data-ttu-id="e48e8-156">في حقل "الجرد"، أدخل الفاصل بين عمليات التشغيل بالدقائق.</span><span class="sxs-lookup"><span data-stu-id="e48e8-156">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="e48e8-157">يكون هذا عادةً 2-20</span><span class="sxs-lookup"><span data-stu-id="e48e8-157">Typically this would be 2-20</span></span>
9. <span data-ttu-id="e48e8-158">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="e48e8-158">Click OK.</span></span>
10. <span data-ttu-id="e48e8-159">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="e48e8-159">Click OK.</span></span>

## <a name="data-entities-involved-in-the-process"></a><span data-ttu-id="e48e8-160">كيانات البيانات المشمولة في العملية</span><span class="sxs-lookup"><span data-stu-id="e48e8-160">Data entities involved in the process</span></span>

- <span data-ttu-id="e48e8-161">RetailTransactionTable</span><span class="sxs-lookup"><span data-stu-id="e48e8-161">RetailTransactionTable</span></span>
- <span data-ttu-id="e48e8-162">RetailTransactionAddressTrans</span><span class="sxs-lookup"><span data-stu-id="e48e8-162">RetailTransactionAddressTrans</span></span>
- <span data-ttu-id="e48e8-163">RetailTransactionInfocodeTrans</span><span class="sxs-lookup"><span data-stu-id="e48e8-163">RetailTransactionInfocodeTrans</span></span>
- <span data-ttu-id="e48e8-164">RetailTransactionTaxTrans</span><span class="sxs-lookup"><span data-stu-id="e48e8-164">RetailTransactionTaxTrans</span></span>
- <span data-ttu-id="e48e8-165">RetailTransactionSalesTrans</span><span class="sxs-lookup"><span data-stu-id="e48e8-165">RetailTransactionSalesTrans</span></span>
- <span data-ttu-id="e48e8-166">RetailTransactionTaxMeasure</span><span class="sxs-lookup"><span data-stu-id="e48e8-166">RetailTransactionTaxMeasure</span></span>
- <span data-ttu-id="e48e8-167">RetailTransactionDiscountTrans</span><span class="sxs-lookup"><span data-stu-id="e48e8-167">RetailTransactionDiscountTrans</span></span>
- <span data-ttu-id="e48e8-168">RetailTransactionTaxTransGTE</span><span class="sxs-lookup"><span data-stu-id="e48e8-168">RetailTransactionTaxTransGTE</span></span>
- <span data-ttu-id="e48e8-169">RetailTransactionMarkupTrans</span><span class="sxs-lookup"><span data-stu-id="e48e8-169">RetailTransactionMarkupTrans</span></span>
- <span data-ttu-id="e48e8-170">RetailTransactionPaymentTrans</span><span class="sxs-lookup"><span data-stu-id="e48e8-170">RetailTransactionPaymentTrans</span></span>
- <span data-ttu-id="e48e8-171">RetailTransactionAttributeTrans</span><span class="sxs-lookup"><span data-stu-id="e48e8-171">RetailTransactionAttributeTrans</span></span>
