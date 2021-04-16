---
title: ترحيل الدفعات والمبيعات على الإنترنت
description: يتناول هذا الإجراء تكوين وظيفة دفعية متكررة وتشغيلها لإنشاء أوامر الشراء والمدفوعات لحركات المتجر على الإنترنت.
author: psimolin
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2e482b0fb5f2cf67e687c2b278bc5b54ad09839
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802661"
---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="d6920-103">ترحيل الدفعات والمبيعات على الإنترنت</span><span class="sxs-lookup"><span data-stu-id="d6920-103">Posting of online sales and payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d6920-104">يتناول هذا الإجراء تكوين وظيفة دفعية متكررة وتشغيلها لإنشاء أوامر الشراء والمدفوعات لحركات المتجر على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="d6920-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span>

<span data-ttu-id="d6920-105">إن ترحيل المبيعات والمدفوعات عبر الإنترنت عبارة عن عملية من مرحلتين.</span><span class="sxs-lookup"><span data-stu-id="d6920-105">Posting online sales and payments is a two-stage process.</span></span>

- <span data-ttu-id="d6920-106">سحب بيانات حركه التجارة عبر الإنترنت إلى HQ.</span><span class="sxs-lookup"><span data-stu-id="d6920-106">Pulling the online commerce transaction data in HQ.</span></span>
- <span data-ttu-id="d6920-107">مزامنة الأوامر لإنشاء أوامر بيع في HQ.</span><span class="sxs-lookup"><span data-stu-id="d6920-107">Synchronizing orders to create sales orders in HQ.</span></span>

<span data-ttu-id="d6920-108">يمكن سحب بيانات حركه عبر الإنترنت إما عن طريق تشغيل الوظيفة P يدويًا أو عن طريق إنشاء وظيفة دفعية متكررة.</span><span class="sxs-lookup"><span data-stu-id="d6920-108">Pulling the online transaction data can be done either by manually running the P-job or by creating a recurrent batch job.</span></span>

### <a name="manually-running-the-p-job"></a><span data-ttu-id="d6920-109">تشغيل الوظيفة P يدويًا</span><span class="sxs-lookup"><span data-stu-id="d6920-109">Manually running the P-job</span></span>

1. <span data-ttu-id="d6920-110">انتقل إلى كافة مساحات العمل > تكنولوجيات المعلومات للبيع بالتجزئة والتجارة.</span><span class="sxs-lookup"><span data-stu-id="d6920-110">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="d6920-111">انقر فوق جدول التوزيع.</span><span class="sxs-lookup"><span data-stu-id="d6920-111">Click Distribution schedule.</span></span>
3. <span data-ttu-id="d6920-112">حدد P-0001.</span><span class="sxs-lookup"><span data-stu-id="d6920-112">Select P-0001.</span></span>
4. <span data-ttu-id="d6920-113">اضبط مجموعات قواعد بيانات القنوات، إذا كان ذلك مطلوبًا.</span><span class="sxs-lookup"><span data-stu-id="d6920-113">Adjust channel database groups, if required.</span></span>
5. <span data-ttu-id="d6920-114">انقر فوق تشغيل الآن.</span><span class="sxs-lookup"><span data-stu-id="d6920-114">Click Run now.</span></span>
6. <span data-ttu-id="d6920-115">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="d6920-115">Click Yes.</span></span>

### <a name="scheduling-a-recurring-p-job"></a><span data-ttu-id="d6920-116">جدولة وظيفة P متكررة</span><span class="sxs-lookup"><span data-stu-id="d6920-116">Scheduling a recurring P-job</span></span>

1. <span data-ttu-id="d6920-117">انتقل إلى كافة مساحات العمل > تكنولوجيات المعلومات للبيع بالتجزئة والتجارة.</span><span class="sxs-lookup"><span data-stu-id="d6920-117">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="d6920-118">انقر فوق جدول التوزيع.</span><span class="sxs-lookup"><span data-stu-id="d6920-118">Click Distribution schedule.</span></span>
3. <span data-ttu-id="d6920-119">حدد P-0001.</span><span class="sxs-lookup"><span data-stu-id="d6920-119">Select P-0001.</span></span>
4. <span data-ttu-id="d6920-120">انقر فوق "إنشاء وظيفة دفعية".</span><span class="sxs-lookup"><span data-stu-id="d6920-120">Click Create batch job.</span></span>
5. <span data-ttu-id="d6920-121">انقر فوق "تشغيل في الخلفية".</span><span class="sxs-lookup"><span data-stu-id="d6920-121">Click Run in the background.</span></span>
5. <span data-ttu-id="d6920-122">مكّن "معالجة الدُفعات".</span><span class="sxs-lookup"><span data-stu-id="d6920-122">Enable Batch processing.</span></span>
6. <span data-ttu-id="d6920-123">انقر فوق "تكرار".</span><span class="sxs-lookup"><span data-stu-id="d6920-123">Click Recurrence..</span></span>
7. <span data-ttu-id="d6920-124">حدد الخيار "‏‫لا يوجد تاريخ انتهاء‬".</span><span class="sxs-lookup"><span data-stu-id="d6920-124">Select the No end date option.</span></span>
8. <span data-ttu-id="d6920-125">في حقل "الجرد"، أدخل الفاصل بين عمليات التشغيل بالدقائق.</span><span class="sxs-lookup"><span data-stu-id="d6920-125">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="d6920-126">يكون هذا عادةً 5-10.</span><span class="sxs-lookup"><span data-stu-id="d6920-126">Typically this would be 5-10.</span></span>
9. <span data-ttu-id="d6920-127">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="d6920-127">Click OK.</span></span>
10. <span data-ttu-id="d6920-128">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="d6920-128">Click OK.</span></span>

<span data-ttu-id="d6920-129">يمكن مزامنة الأوامر إما عن طريق تشغيل وظيفة "مزامنة الأوامر" يدويًا أو عن طريق إنشاء وظيفة دفعية متكررة.</span><span class="sxs-lookup"><span data-stu-id="d6920-129">Orders can be synchronized either by manually running the "Synchronize orders"-job or by creating a recurring batch job.</span></span>

### <a name="manually-running-order-synchronization"></a><span data-ttu-id="d6920-130">تشغيل مزامنة الأوامر يدويًا</span><span class="sxs-lookup"><span data-stu-id="d6920-130">Manually running order synchronization</span></span> 

<span data-ttu-id="d6920-131">اتبع هذه الخطوات لتشغيل وظيفة "مزامنة الأوامر" يدويًا مرة واحدة.</span><span class="sxs-lookup"><span data-stu-id="d6920-131">Follow these steps to manually run "Synchronize orders" job once.</span></span>

1. <span data-ttu-id="d6920-132">انتقل إلى كافة مساحات العمل > ماليات المتاجر.</span><span class="sxs-lookup"><span data-stu-id="d6920-132">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="d6920-133">انقر فوق مزامنة الأوامر.</span><span class="sxs-lookup"><span data-stu-id="d6920-133">Click Synchronize orders.</span></span>
3. <span data-ttu-id="d6920-134">في حقل "‏‫التدرج الهرمي للمؤسسات‬"، حدد "المتاجر حسب المنطقة".</span><span class="sxs-lookup"><span data-stu-id="d6920-134">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="d6920-135">حدد إما متجر معين على الإنترنت أو حدد عقدة إذا أردت إنشاء وظيفة دفعية لمجموعة من المتاجر.</span><span class="sxs-lookup"><span data-stu-id="d6920-135">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="d6920-136">انقر فوق السهم لإضافة التحديد الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="d6920-136">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="d6920-137">انقر فوق علامة التبويب "‏‫تشغيل في الخلفية".</span><span class="sxs-lookup"><span data-stu-id="d6920-137">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="d6920-138">تعطيل معالجة الدُفعات</span><span class="sxs-lookup"><span data-stu-id="d6920-138">Disable Batch processing</span></span>
6. <span data-ttu-id="d6920-139">انقر فوق "تكرار".</span><span class="sxs-lookup"><span data-stu-id="d6920-139">Click Recurrence.</span></span>
7. <span data-ttu-id="d6920-140">حدد الخيار "انتهاء بعد"</span><span class="sxs-lookup"><span data-stu-id="d6920-140">Select End After option</span></span>
8. <span data-ttu-id="d6920-141">في الحقل "انتهاء بعد"، أدخل 1.</span><span class="sxs-lookup"><span data-stu-id="d6920-141">In the End After field, enter 1.</span></span>
9. <span data-ttu-id="d6920-142">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="d6920-142">Click OK.</span></span>
10. <span data-ttu-id="d6920-143">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="d6920-143">Click OK.</span></span>

### <a name="scheduling-recurring-order-synchronization"></a><span data-ttu-id="d6920-144">جدولة مزامنة الأوامر المتكررة</span><span class="sxs-lookup"><span data-stu-id="d6920-144">Scheduling recurring order synchronization</span></span>

<span data-ttu-id="d6920-145">يتناول هذا الإجراء تكوين وظيفة دفعية متكررة وتشغيلها لإنشاء أوامر الشراء والمدفوعات لحركات المتجر على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="d6920-145">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="d6920-146">ويستخدم هذا الإجراء شركة USRT في بيانات العرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="d6920-146">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="d6920-147">انتقل إلى كافة مساحات العمل > ماليات المتاجر.</span><span class="sxs-lookup"><span data-stu-id="d6920-147">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="d6920-148">انقر فوق مزامنة الأوامر.</span><span class="sxs-lookup"><span data-stu-id="d6920-148">Click Synchronize orders.</span></span>
3. <span data-ttu-id="d6920-149">في حقل "‏‫التدرج الهرمي للمؤسسات‬"، حدد "المتاجر حسب المنطقة".</span><span class="sxs-lookup"><span data-stu-id="d6920-149">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="d6920-150">حدد إما متجر معين على الإنترنت أو حدد عقدة إذا أردت إنشاء وظيفة دفعية لمجموعة من المتاجر.</span><span class="sxs-lookup"><span data-stu-id="d6920-150">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="d6920-151">انقر فوق السهم لإضافة التحديد الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="d6920-151">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="d6920-152">انقر فوق علامة التبويب "‏‫تشغيل في الخلفية".</span><span class="sxs-lookup"><span data-stu-id="d6920-152">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="d6920-153">تمكين معالجة الدُفعات</span><span class="sxs-lookup"><span data-stu-id="d6920-153">Enable Batch processing</span></span>
6. <span data-ttu-id="d6920-154">انقر فوق "تكرار".</span><span class="sxs-lookup"><span data-stu-id="d6920-154">Click Recurrence.</span></span>
7. <span data-ttu-id="d6920-155">حدد الخيار "‏‫لا يوجد تاريخ انتهاء‬".</span><span class="sxs-lookup"><span data-stu-id="d6920-155">Select the No end date option.</span></span>
8. <span data-ttu-id="d6920-156">في حقل "الجرد"، أدخل الفاصل بين عمليات التشغيل بالدقائق.</span><span class="sxs-lookup"><span data-stu-id="d6920-156">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="d6920-157">يكون هذا عادةً 2-20</span><span class="sxs-lookup"><span data-stu-id="d6920-157">Typically this would be 2-20</span></span>
9. <span data-ttu-id="d6920-158">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="d6920-158">Click OK.</span></span>
10. <span data-ttu-id="d6920-159">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="d6920-159">Click OK.</span></span>

## <a name="data-entities-involved-in-the-process"></a><span data-ttu-id="d6920-160">كيانات البيانات المشمولة في العملية</span><span class="sxs-lookup"><span data-stu-id="d6920-160">Data entities involved in the process</span></span>

- <span data-ttu-id="d6920-161">RetailTransactionTable</span><span class="sxs-lookup"><span data-stu-id="d6920-161">RetailTransactionTable</span></span>
- <span data-ttu-id="d6920-162">RetailTransactionAddressTrans</span><span class="sxs-lookup"><span data-stu-id="d6920-162">RetailTransactionAddressTrans</span></span>
- <span data-ttu-id="d6920-163">RetailTransactionInfocodeTrans</span><span class="sxs-lookup"><span data-stu-id="d6920-163">RetailTransactionInfocodeTrans</span></span>
- <span data-ttu-id="d6920-164">RetailTransactionTaxTrans</span><span class="sxs-lookup"><span data-stu-id="d6920-164">RetailTransactionTaxTrans</span></span>
- <span data-ttu-id="d6920-165">RetailTransactionSalesTrans</span><span class="sxs-lookup"><span data-stu-id="d6920-165">RetailTransactionSalesTrans</span></span>
- <span data-ttu-id="d6920-166">RetailTransactionTaxMeasure</span><span class="sxs-lookup"><span data-stu-id="d6920-166">RetailTransactionTaxMeasure</span></span>
- <span data-ttu-id="d6920-167">RetailTransactionDiscountTrans</span><span class="sxs-lookup"><span data-stu-id="d6920-167">RetailTransactionDiscountTrans</span></span>
- <span data-ttu-id="d6920-168">RetailTransactionTaxTransGTE</span><span class="sxs-lookup"><span data-stu-id="d6920-168">RetailTransactionTaxTransGTE</span></span>
- <span data-ttu-id="d6920-169">RetailTransactionMarkupTrans</span><span class="sxs-lookup"><span data-stu-id="d6920-169">RetailTransactionMarkupTrans</span></span>
- <span data-ttu-id="d6920-170">RetailTransactionPaymentTrans</span><span class="sxs-lookup"><span data-stu-id="d6920-170">RetailTransactionPaymentTrans</span></span>
- <span data-ttu-id="d6920-171">RetailTransactionAttributeTrans</span><span class="sxs-lookup"><span data-stu-id="d6920-171">RetailTransactionAttributeTrans</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]