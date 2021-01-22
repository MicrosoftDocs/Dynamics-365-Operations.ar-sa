---
title: إنشاء دفتر يومية شطب لعميل
description: سيُظهر لك دليل المهمة هذا كيفية إعداد محددات عمليات الشطب ثم شطب الحركات من صفحة "التحصيلات" وصفحة "فتح فواتير العملاء‬" وصفحة "العميل".
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, CustPosting, DefaultDashboard, CustCollectionsPoolsListPage, CustWriteOff, LedgerJournalTable, LedgerJournalTransDaily, CustCollections, CustOpenInvoicesListPage, CustTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd97f91f1ba53b56150b556fffdfed10a0c8911a
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140227"
---
# <a name="create-a-write-off-journal-for-a-customer"></a><span data-ttu-id="d3c07-103">إنشاء دفتر يومية شطب لعميل</span><span class="sxs-lookup"><span data-stu-id="d3c07-103">Create a write-off journal for a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d3c07-104">سيُظهر لك دليل المهمة هذا كيفية إعداد محددات عمليات الشطب ثم شطب الحركات من صفحة "التحصيلات" وصفحة "فتح فواتير العملاء‬" وصفحة "العميل".</span><span class="sxs-lookup"><span data-stu-id="d3c07-104">This task guide will show you how to set up the parameters for write-offs and then write off transactions from the Collections page, the Open customer invoices page, and the Customer page.</span></span> <span data-ttu-id="d3c07-105">تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="d3c07-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-the-write-off-parameters"></a><span data-ttu-id="d3c07-106">إعداد محددات الشطب</span><span class="sxs-lookup"><span data-stu-id="d3c07-106">Set up the write off parameters</span></span>
1. <span data-ttu-id="d3c07-107">انتقل إلى **جزء التنقل > الوحدات النمطية‬ > عمليات التحصيل والائتمان‬ > الإعداد > معلمات الحسابات المدينة**.</span><span class="sxs-lookup"><span data-stu-id="d3c07-107">Go to **Navigation pane > Modules > Credit and collections > Setup > Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="d3c07-108">انقر فوق علامة التبويب **التحصيلات‬**.</span><span class="sxs-lookup"><span data-stu-id="d3c07-108">Click the **Collections** tab.</span></span>
3. <span data-ttu-id="d3c07-109">قم بتوسيع أو طي القسم **شطب**.</span><span class="sxs-lookup"><span data-stu-id="d3c07-109">Expand or collapse the **Write-off** section.</span></span>
    - <span data-ttu-id="d3c07-110">**دفتر يومية الشطب** هو دفتر اليومية العام الذي سيحتفظ بحركات الشطب التي تقوم بإنشائها.</span><span class="sxs-lookup"><span data-stu-id="d3c07-110">The **Write-off journal** is the general journal that will hold the write-off transactions that you create.</span></span>  
    - <span data-ttu-id="d3c07-111">يمكنك إرفاق كود سبب لكل عملية شطب.</span><span class="sxs-lookup"><span data-stu-id="d3c07-111">You can attach a reason code to every write-off.</span></span> <span data-ttu-id="d3c07-112">ويمكنك تجاوز هذا الإعداد الافتراضي عند إجراء الشطب.</span><span class="sxs-lookup"><span data-stu-id="d3c07-112">You can override this default at the time of the write-off.</span></span>  
    - <span data-ttu-id="d3c07-113">عيّن الخيار **فصل ضريبة المبيعات‬** إلى "نعم" إذا كنت تريد فصل ضريبة المبيعات عن الحركة الأصلية في عملية الشطب.</span><span class="sxs-lookup"><span data-stu-id="d3c07-113">Set the **Separate sales tax** to Yes if you want to separate the sales tax from the original transaction in the write-off.</span></span>  
4. <span data-ttu-id="d3c07-114">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d3c07-114">Close the page.</span></span>
5. <span data-ttu-id="d3c07-115">انتقل إلى **التحصيلات والائتمان > الإعداد > ملفات تعريف ترحيل العميل**.</span><span class="sxs-lookup"><span data-stu-id="d3c07-115">Go to **Credit and collections > Setup > Customer posting profiles**.</span></span> <span data-ttu-id="d3c07-116">سيتم استخدام حساب الشطب كحساب المصروفات أو تسوية الحجز في دفتر اليومية العام.</span><span class="sxs-lookup"><span data-stu-id="d3c07-116">The write-off account will be used as the expense account or reserve adjustment in the general journal.</span></span>
6. <span data-ttu-id="d3c07-117">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d3c07-117">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a><span data-ttu-id="d3c07-118">شطب رصيد عميل من صفحة الأرصدة المتقادمة</span><span class="sxs-lookup"><span data-stu-id="d3c07-118">Write off a customer balance from the aged balances page</span></span>
1. <span data-ttu-id="d3c07-119">انتقل إلى **التحصيلات والائتمان > التحصيلات > الأرصدة المتقادمة**.</span><span class="sxs-lookup"><span data-stu-id="d3c07-119">Go to **Credit and collections > Collections > Aged balances**.</span></span>
2. <span data-ttu-id="d3c07-120">ضع علامة على الصف للعميل الذي تريد شطبه.</span><span class="sxs-lookup"><span data-stu-id="d3c07-120">Mark the row for the customer that you want to write off.</span></span> <span data-ttu-id="d3c07-121">على سبيل المثال، ضع علامة على البند الذي يتضمن Birch Company.</span><span class="sxs-lookup"><span data-stu-id="d3c07-121">For example, mark the line with Birch Company on it.</span></span>
3. <span data-ttu-id="d3c07-122">في **جزء الإجراءات**، انقر فوق **تحصيل**.</span><span class="sxs-lookup"><span data-stu-id="d3c07-122">On the **Action Pane**, click **Collect**.</span></span>
4. <span data-ttu-id="d3c07-123">انقر فوق **شطب**.</span><span class="sxs-lookup"><span data-stu-id="d3c07-123">Click **Write off**.</span></span>
5. <span data-ttu-id="d3c07-124">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d3c07-124">Click **OK**.</span></span>
6. <span data-ttu-id="d3c07-125">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d3c07-125">Close the page.</span></span>
7. <span data-ttu-id="d3c07-126">انتقل إلى **جزء التنقل > الوحدات النمطية > دفتر الأستاذ العام > إدخالات دفتر اليومية > دفاتر اليومية العامة‬**.</span><span class="sxs-lookup"><span data-stu-id="d3c07-126">Go to **Navigation pane > Modules > General ledger > Journal entries > General journals**.</span></span>
8. <span data-ttu-id="d3c07-127">حدد رقم دُفعة دفتر اليومية لدفتر اليومية الذي يحتوي على الشطب الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="d3c07-127">Select the journal batch number for the journal that contains your write-off.</span></span> <span data-ttu-id="d3c07-128">يتم إنشاء بند واحد لعكس رصيد العميل.</span><span class="sxs-lookup"><span data-stu-id="d3c07-128">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="d3c07-129">يتم إنشاء بند واحد أو أكثر لترحيل الشطب إلى حساب الشطب.</span><span class="sxs-lookup"><span data-stu-id="d3c07-129">One or more lines are created to post the write-off to the write-off account.</span></span>  
9. <span data-ttu-id="d3c07-130">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d3c07-130">Close the page.</span></span>
10. <span data-ttu-id="d3c07-131">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d3c07-131">Close the page.</span></span>

## <a name="write-off-transactions-from-the-collections-form"></a><span data-ttu-id="d3c07-132">شطب الحركات من نموذج التحصيلات</span><span class="sxs-lookup"><span data-stu-id="d3c07-132">Write off transactions from the collections form.</span></span>
1. <span data-ttu-id="d3c07-133">انتقل إلى **التحصيلات والائتمان > التحصيلات > الأرصدة المتقادمة**.</span><span class="sxs-lookup"><span data-stu-id="d3c07-133">Go to **Credit and collections > Collections > Aged balances**.</span></span>
2. <span data-ttu-id="d3c07-134">حدد اسم العميل الذي تريد شطب الحركات الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="d3c07-134">Select the name of the customer that has the transactions that you want to write off.</span></span> <span data-ttu-id="d3c07-135">على سبيل المثال، حدد Cave Wholesales (US-004).</span><span class="sxs-lookup"><span data-stu-id="d3c07-135">For example, select Cave Wholesales (US-004).</span></span>
3. <span data-ttu-id="d3c07-136">ضع علامة على الصف للحركة الأولى.</span><span class="sxs-lookup"><span data-stu-id="d3c07-136">Mark the row for the first transaction.</span></span>
4. <span data-ttu-id="d3c07-137">ضع علامة على الصف للحركة الثانية.</span><span class="sxs-lookup"><span data-stu-id="d3c07-137">Mark the row for the second transaction.</span></span>
5. <span data-ttu-id="d3c07-138">انقر فوق **شطب**.</span><span class="sxs-lookup"><span data-stu-id="d3c07-138">Click **Write off**.</span></span>
6. <span data-ttu-id="d3c07-139">في الحقل **تعليق على السبب‬**، اكتب "ديون مشكوك في تحصيلها".</span><span class="sxs-lookup"><span data-stu-id="d3c07-139">In the **Reason comment** field, type 'Bad debts'.</span></span>
7. <span data-ttu-id="d3c07-140">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d3c07-140">Click **OK**.</span></span>
8. <span data-ttu-id="d3c07-141">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d3c07-141">Close the page.</span></span>
9. <span data-ttu-id="d3c07-142">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d3c07-142">Close the page.</span></span>
10. <span data-ttu-id="d3c07-143">انتقل إلى **دفتر الأستاذ العام > إدخالات دفتر اليومية > دفاتر اليومية العامة**‬.</span><span class="sxs-lookup"><span data-stu-id="d3c07-143">Go to **General ledger > Journal entries > General journals**.</span></span>
11. <span data-ttu-id="d3c07-144">حدد رقم دُفعة دفتر اليومية لدفتر اليومية الذي يحتوي على الشطب الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="d3c07-144">Select the journal batch number for the journal that contains your write-off.</span></span> <span data-ttu-id="d3c07-145">يتم إنشاء بند واحد لعكس رصيد العميل.</span><span class="sxs-lookup"><span data-stu-id="d3c07-145">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="d3c07-146">يتم إنشاء بند واحد أو أكثر لترحيل الشطب إلى حساب الشطب.</span><span class="sxs-lookup"><span data-stu-id="d3c07-146">One or more lines are created to post the write-off to the write-off account.</span></span>  
12. <span data-ttu-id="d3c07-147">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d3c07-147">Close the page.</span></span>
13. <span data-ttu-id="d3c07-148">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d3c07-148">Close the page.</span></span>

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a><span data-ttu-id="d3c07-149">شطب فاتورة من صفحة فواتير العملاء المفتوحة</span><span class="sxs-lookup"><span data-stu-id="d3c07-149">Write off an invoice from the Open customers invoices page</span></span>
1. <span data-ttu-id="d3c07-150">انتقل إلى **جزء التنقل > الوحدات النمطية > الحسابات المدينة > الفواتير > فواتير العملاء المفتوحة‬**.</span><span class="sxs-lookup"><span data-stu-id="d3c07-150">Go to **Navigation pane > Modules > Accounts receivable > Invoices > Open customer invoices**.</span></span>
2. <span data-ttu-id="d3c07-151">ضع علامة على البند للفاتورة.</span><span class="sxs-lookup"><span data-stu-id="d3c07-151">Mark the line for an invoice.</span></span> <span data-ttu-id="d3c07-152">على سبيل المثال، ضع علامة على البند لـ CIV-000667.</span><span class="sxs-lookup"><span data-stu-id="d3c07-152">For example, mark the line for CIV-000667.</span></span>
3. <span data-ttu-id="d3c07-153">في **جزء الإجراءات**، انقر فوق **فاتورة**.</span><span class="sxs-lookup"><span data-stu-id="d3c07-153">On the **Action Pane**, click **Invoice**.</span></span>
4. <span data-ttu-id="d3c07-154">انقر فوق **شطب**.</span><span class="sxs-lookup"><span data-stu-id="d3c07-154">Click **Write off**.</span></span>
5. <span data-ttu-id="d3c07-155">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d3c07-155">Click **OK**.</span></span>
6. <span data-ttu-id="d3c07-156">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d3c07-156">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-customer-page"></a><span data-ttu-id="d3c07-157">شطب رصيد عميل من صفحة العميل</span><span class="sxs-lookup"><span data-stu-id="d3c07-157">Write off a customer balance from the customer page</span></span>
1. <span data-ttu-id="d3c07-158">انتقل إلى **الحسابات المدينة > العملاء > كافة العملاء**‬.</span><span class="sxs-lookup"><span data-stu-id="d3c07-158">Go to **Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="d3c07-159">حدد حساب عميل.</span><span class="sxs-lookup"><span data-stu-id="d3c07-159">Select a customer account.</span></span> <span data-ttu-id="d3c07-160">على سبيل المثال، حدد US-001 (Contoso Retail San Diego).</span><span class="sxs-lookup"><span data-stu-id="d3c07-160">For example, select US-001 (Contoso Retail San Diego).</span></span>
3. <span data-ttu-id="d3c07-161">في **جزء الإجراءات**، انقر فوق **تحصيل**.</span><span class="sxs-lookup"><span data-stu-id="d3c07-161">On the **Action Pane**, click **Collect**.</span></span>
4. <span data-ttu-id="d3c07-162">انقر فوق **شطب**.</span><span class="sxs-lookup"><span data-stu-id="d3c07-162">Click **Write off**.</span></span>
5. <span data-ttu-id="d3c07-163">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d3c07-163">Click **OK**.</span></span>
6. <span data-ttu-id="d3c07-164">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d3c07-164">Close the page.</span></span>
