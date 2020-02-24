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
ms.openlocfilehash: bf7f72be22539271649aa7f5541735b3d24dab66
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021464"
---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="5e451-103">ترحيل الدفعات والمبيعات على الإنترنت</span><span class="sxs-lookup"><span data-stu-id="5e451-103">Posting of online sales and payments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="5e451-104">يتناول هذا الإجراء تكوين وظيفة دفعية متكررة وتشغيلها لإنشاء أوامر الشراء والمدفوعات لحركات المتجر على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="5e451-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span>

<span data-ttu-id="5e451-105">إن ترحيل المبيعات والمدفوعات عبر الإنترنت عبارة عن عملية من مرحلتين.</span><span class="sxs-lookup"><span data-stu-id="5e451-105">Posting online sales and payments is a two-stage process.</span></span>

- <span data-ttu-id="5e451-106">سحب بيانات حركه التجارة عبر الإنترنت إلى HQ.</span><span class="sxs-lookup"><span data-stu-id="5e451-106">Pulling the online commerce transaction data in HQ.</span></span>
- <span data-ttu-id="5e451-107">مزامنة الأوامر لإنشاء أوامر بيع في HQ.</span><span class="sxs-lookup"><span data-stu-id="5e451-107">Synchronizing orders to create sales orders in HQ.</span></span>

<span data-ttu-id="5e451-108">يمكن سحب بيانات حركه عبر الإنترنت إما عن طريق تشغيل الوظيفة P يدويًا أو عن طريق إنشاء وظيفة دفعية متكررة.</span><span class="sxs-lookup"><span data-stu-id="5e451-108">Pulling the online transaction data can be done either by manually running the P-job or by creating a recurrent batch job.</span></span>

### <a name="manually-running-the-p-job"></a><span data-ttu-id="5e451-109">تشغيل الوظيفة P يدويًا</span><span class="sxs-lookup"><span data-stu-id="5e451-109">Manually running the P-job</span></span>

1. <span data-ttu-id="5e451-110">انتقل إلى كافة مساحات العمل > تكنولوجيات المعلومات للبيع بالتجزئة والتجارة.</span><span class="sxs-lookup"><span data-stu-id="5e451-110">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="5e451-111">انقر فوق جدول التوزيع.</span><span class="sxs-lookup"><span data-stu-id="5e451-111">Click Distribution schedule.</span></span>
3. <span data-ttu-id="5e451-112">حدد P-0001.</span><span class="sxs-lookup"><span data-stu-id="5e451-112">Select P-0001.</span></span>
4. <span data-ttu-id="5e451-113">اضبط مجموعات قواعد بيانات القنوات، إذا كان ذلك مطلوبًا.</span><span class="sxs-lookup"><span data-stu-id="5e451-113">Adjust channel database groups, if required.</span></span>
5. <span data-ttu-id="5e451-114">انقر فوق تشغيل الآن.</span><span class="sxs-lookup"><span data-stu-id="5e451-114">Click Run now.</span></span>
6. <span data-ttu-id="5e451-115">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="5e451-115">Click Yes.</span></span>

### <a name="scheduling-a-recurring-p-job"></a><span data-ttu-id="5e451-116">جدولة وظيفة P متكررة</span><span class="sxs-lookup"><span data-stu-id="5e451-116">Scheduling a recurring P-job</span></span>

1. <span data-ttu-id="5e451-117">انتقل إلى كافة مساحات العمل > تكنولوجيات المعلومات للبيع بالتجزئة والتجارة.</span><span class="sxs-lookup"><span data-stu-id="5e451-117">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="5e451-118">انقر فوق جدول التوزيع.</span><span class="sxs-lookup"><span data-stu-id="5e451-118">Click Distribution schedule.</span></span>
3. <span data-ttu-id="5e451-119">حدد P-0001.</span><span class="sxs-lookup"><span data-stu-id="5e451-119">Select P-0001.</span></span>
4. <span data-ttu-id="5e451-120">انقر فوق "إنشاء وظيفة دفعية".</span><span class="sxs-lookup"><span data-stu-id="5e451-120">Click Create batch job.</span></span>
5. <span data-ttu-id="5e451-121">انقر فوق "تشغيل في الخلفية".</span><span class="sxs-lookup"><span data-stu-id="5e451-121">Click Run in the background.</span></span>
5. <span data-ttu-id="5e451-122">مكّن "معالجة الدُفعات".</span><span class="sxs-lookup"><span data-stu-id="5e451-122">Enable Batch processing.</span></span>
6. <span data-ttu-id="5e451-123">انقر فوق "تكرار".</span><span class="sxs-lookup"><span data-stu-id="5e451-123">Click Recurrence..</span></span>
7. <span data-ttu-id="5e451-124">حدد الخيار "‏‫لا يوجد تاريخ انتهاء‬".</span><span class="sxs-lookup"><span data-stu-id="5e451-124">Select the No end date option.</span></span>
8. <span data-ttu-id="5e451-125">في حقل "الجرد"، أدخل الفاصل بين عمليات التشغيل بالدقائق.</span><span class="sxs-lookup"><span data-stu-id="5e451-125">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="5e451-126">يكون هذا عادةً 5-10.</span><span class="sxs-lookup"><span data-stu-id="5e451-126">Typically this would be 5-10.</span></span>
9. <span data-ttu-id="5e451-127">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="5e451-127">Click OK.</span></span>
10. <span data-ttu-id="5e451-128">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="5e451-128">Click OK.</span></span>

<span data-ttu-id="5e451-129">يمكن مزامنة الأوامر إما عن طريق تشغيل وظيفة "مزامنة الأوامر" يدويًا أو عن طريق إنشاء وظيفة دفعية متكررة.</span><span class="sxs-lookup"><span data-stu-id="5e451-129">Orders can be synchronized either by manually running the "Synchronize orders"-job or by creating a recurring batch job.</span></span>

### <a name="manually-running-order-synchronization"></a><span data-ttu-id="5e451-130">تشغيل مزامنة الأوامر يدويًا</span><span class="sxs-lookup"><span data-stu-id="5e451-130">Manually running order synchronization</span></span> 

<span data-ttu-id="5e451-131">اتبع هذه الخطوات لتشغيل وظيفة "مزامنة الأوامر" يدويًا مرة واحدة.</span><span class="sxs-lookup"><span data-stu-id="5e451-131">Follow these steps to manually run "Synchronize orders" job once.</span></span>

1. <span data-ttu-id="5e451-132">انتقل إلى كافة مساحات العمل > ماليات المتاجر.</span><span class="sxs-lookup"><span data-stu-id="5e451-132">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="5e451-133">انقر فوق مزامنة الأوامر.</span><span class="sxs-lookup"><span data-stu-id="5e451-133">Click Synchronize orders.</span></span>
3. <span data-ttu-id="5e451-134">في حقل "‏‫التدرج الهرمي للمؤسسات‬"، حدد "المتاجر حسب المنطقة".</span><span class="sxs-lookup"><span data-stu-id="5e451-134">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="5e451-135">حدد إما متجر معين على الإنترنت أو حدد عقدة إذا أردت إنشاء وظيفة دفعية لمجموعة من المتاجر.</span><span class="sxs-lookup"><span data-stu-id="5e451-135">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="5e451-136">انقر فوق السهم لإضافة التحديد الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="5e451-136">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="5e451-137">انقر فوق علامة التبويب "‏‫تشغيل في الخلفية".</span><span class="sxs-lookup"><span data-stu-id="5e451-137">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="5e451-138">تعطيل معالجة الدُفعات</span><span class="sxs-lookup"><span data-stu-id="5e451-138">Disable Batch processing</span></span>
6. <span data-ttu-id="5e451-139">انقر فوق "تكرار".</span><span class="sxs-lookup"><span data-stu-id="5e451-139">Click Recurrence.</span></span>
7. <span data-ttu-id="5e451-140">حدد الخيار "انتهاء بعد"</span><span class="sxs-lookup"><span data-stu-id="5e451-140">Select End After option</span></span>
8. <span data-ttu-id="5e451-141">في الحقل "انتهاء بعد"، أدخل 1.</span><span class="sxs-lookup"><span data-stu-id="5e451-141">In the End After field, enter 1.</span></span>
9. <span data-ttu-id="5e451-142">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="5e451-142">Click OK.</span></span>
10. <span data-ttu-id="5e451-143">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="5e451-143">Click OK.</span></span>

### <a name="scheduling-recurring-order-synchronization"></a><span data-ttu-id="5e451-144">جدولة مزامنة الأوامر المتكررة</span><span class="sxs-lookup"><span data-stu-id="5e451-144">Scheduling recurring order synchronization</span></span>

<span data-ttu-id="5e451-145">يتناول هذا الإجراء تكوين وظيفة دفعية متكررة وتشغيلها لإنشاء أوامر الشراء والمدفوعات لحركات المتجر على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="5e451-145">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="5e451-146">ويستخدم هذا الإجراء شركة USRT في بيانات العرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="5e451-146">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="5e451-147">انتقل إلى كافة مساحات العمل > ماليات المتاجر.</span><span class="sxs-lookup"><span data-stu-id="5e451-147">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="5e451-148">انقر فوق مزامنة الأوامر.</span><span class="sxs-lookup"><span data-stu-id="5e451-148">Click Synchronize orders.</span></span>
3. <span data-ttu-id="5e451-149">في حقل "‏‫التدرج الهرمي للمؤسسات‬"، حدد "المتاجر حسب المنطقة".</span><span class="sxs-lookup"><span data-stu-id="5e451-149">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="5e451-150">حدد إما متجر معين على الإنترنت أو حدد عقدة إذا أردت إنشاء وظيفة دفعية لمجموعة من المتاجر.</span><span class="sxs-lookup"><span data-stu-id="5e451-150">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="5e451-151">انقر فوق السهم لإضافة التحديد الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="5e451-151">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="5e451-152">انقر فوق علامة التبويب "‏‫تشغيل في الخلفية".</span><span class="sxs-lookup"><span data-stu-id="5e451-152">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="5e451-153">تمكين معالجة الدُفعات</span><span class="sxs-lookup"><span data-stu-id="5e451-153">Enable Batch processing</span></span>
6. <span data-ttu-id="5e451-154">انقر فوق "تكرار".</span><span class="sxs-lookup"><span data-stu-id="5e451-154">Click Recurrence.</span></span>
7. <span data-ttu-id="5e451-155">حدد الخيار "‏‫لا يوجد تاريخ انتهاء‬".</span><span class="sxs-lookup"><span data-stu-id="5e451-155">Select the No end date option.</span></span>
8. <span data-ttu-id="5e451-156">في حقل "الجرد"، أدخل الفاصل بين عمليات التشغيل بالدقائق.</span><span class="sxs-lookup"><span data-stu-id="5e451-156">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="5e451-157">يكون هذا عادةً 2-20</span><span class="sxs-lookup"><span data-stu-id="5e451-157">Typically this would be 2-20</span></span>
9. <span data-ttu-id="5e451-158">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="5e451-158">Click OK.</span></span>
10. <span data-ttu-id="5e451-159">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="5e451-159">Click OK.</span></span>

## <a name="data-entities-involved-in-the-process"></a><span data-ttu-id="5e451-160">كيانات البيانات المشمولة في العملية</span><span class="sxs-lookup"><span data-stu-id="5e451-160">Data entities involved in the process</span></span>

- <span data-ttu-id="5e451-161">RetailTransactionTable</span><span class="sxs-lookup"><span data-stu-id="5e451-161">RetailTransactionTable</span></span>
- <span data-ttu-id="5e451-162">RetailTransactionAddressTrans</span><span class="sxs-lookup"><span data-stu-id="5e451-162">RetailTransactionAddressTrans</span></span>
- <span data-ttu-id="5e451-163">RetailTransactionInfocodeTrans</span><span class="sxs-lookup"><span data-stu-id="5e451-163">RetailTransactionInfocodeTrans</span></span>
- <span data-ttu-id="5e451-164">RetailTransactionTaxTrans</span><span class="sxs-lookup"><span data-stu-id="5e451-164">RetailTransactionTaxTrans</span></span>
- <span data-ttu-id="5e451-165">RetailTransactionSalesTrans</span><span class="sxs-lookup"><span data-stu-id="5e451-165">RetailTransactionSalesTrans</span></span>
- <span data-ttu-id="5e451-166">RetailTransactionTaxMeasure</span><span class="sxs-lookup"><span data-stu-id="5e451-166">RetailTransactionTaxMeasure</span></span>
- <span data-ttu-id="5e451-167">RetailTransactionDiscountTrans</span><span class="sxs-lookup"><span data-stu-id="5e451-167">RetailTransactionDiscountTrans</span></span>
- <span data-ttu-id="5e451-168">RetailTransactionTaxTransGTE</span><span class="sxs-lookup"><span data-stu-id="5e451-168">RetailTransactionTaxTransGTE</span></span>
- <span data-ttu-id="5e451-169">RetailTransactionMarkupTrans</span><span class="sxs-lookup"><span data-stu-id="5e451-169">RetailTransactionMarkupTrans</span></span>
- <span data-ttu-id="5e451-170">RetailTransactionPaymentTrans</span><span class="sxs-lookup"><span data-stu-id="5e451-170">RetailTransactionPaymentTrans</span></span>
- <span data-ttu-id="5e451-171">RetailTransactionAttributeTrans</span><span class="sxs-lookup"><span data-stu-id="5e451-171">RetailTransactionAttributeTrans</span></span>
