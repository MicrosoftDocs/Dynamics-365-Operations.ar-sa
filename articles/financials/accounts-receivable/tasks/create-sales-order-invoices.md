---
title: إنشاء فواتير أمر المبيعات
description: يوضح دليل المهمة هذا فوترة أمر مبيعات، بما في ذلك دمج الفواتير ومعالجة الدُفعة.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a57d204c0dcb44cbce7a0cc4d2f00b75b57e219
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565196"
---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="82a70-103">إنشاء فواتير أمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="82a70-103">Create sales order invoices</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="82a70-104">يوضح دليل المهمة هذا فوترة أمر مبيعات، بما في ذلك دمج الفواتير ومعالجة الدُفعة.</span><span class="sxs-lookup"><span data-stu-id="82a70-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="82a70-105">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="82a70-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="82a70-106">إنشاء فاتورة من أمر مبيعات</span><span class="sxs-lookup"><span data-stu-id="82a70-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="82a70-107">انتقل إلى الحسابات المدينة > الأوامر‬ > أوامر المبيعات المشحونة وغير المفوترة‬.</span><span class="sxs-lookup"><span data-stu-id="82a70-107">Go to Accounts receivable > Orders > Shipped but not invoiced sales orders.</span></span>
2. <span data-ttu-id="82a70-108">حدد أمر مبيعات من القائمة.</span><span class="sxs-lookup"><span data-stu-id="82a70-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="82a70-109">في جزء "الإجراءات"، انقر فوق "فاتورة".</span><span class="sxs-lookup"><span data-stu-id="82a70-109">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="82a70-110">انقر فوق "فاتورة".</span><span class="sxs-lookup"><span data-stu-id="82a70-110">Click Invoice.</span></span>
    * <span data-ttu-id="82a70-111">لاحظ أن أمر المبيعات هذا لديه إيصالات تعبئة متعددة مقترنة به.</span><span class="sxs-lookup"><span data-stu-id="82a70-111">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="82a70-112">وسوف يعرض كلمة <multiple> فقط بدلاً من رقم إيصال التعبئة.</span><span class="sxs-lookup"><span data-stu-id="82a70-112">It will only show the word <multiple> instead of the packing slip number.</span></span>  
5. <span data-ttu-id="82a70-113">وسّع مقطع "المحددات".</span><span class="sxs-lookup"><span data-stu-id="82a70-113">Expand the Parameters section.</span></span>
    * <span data-ttu-id="82a70-114">يجب تعيين الترحيل إلى "نعم" لترحيل الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="82a70-114">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="82a70-115">يمكنك أيضًا إيقاف ترحيل الفاتورة وطباعتها فقط.</span><span class="sxs-lookup"><span data-stu-id="82a70-115">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="82a70-116">ومع ذلك، يمكنك تحقيق نفس النتيجة عن طريق إنشاء فاتورة مبدئية بدلاً من فاتورة.</span><span class="sxs-lookup"><span data-stu-id="82a70-116">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    * <span data-ttu-id="82a70-117">وهذا الخيار يُستخدم لوظائف الدُفعات.</span><span class="sxs-lookup"><span data-stu-id="82a70-117">This option is used for batch jobs.</span></span> <span data-ttu-id="82a70-118">ويتم إجراء الاستعلام عند تشغيل وظيفة الدُفعة.</span><span class="sxs-lookup"><span data-stu-id="82a70-118">The query is run when the batch job is run.</span></span>    
6. <span data-ttu-id="82a70-119">في الحقل "طباعة"، حدد "بعد".</span><span class="sxs-lookup"><span data-stu-id="82a70-119">In the Print field, select 'After'.</span></span>
7. <span data-ttu-id="82a70-120">حدد "نعم" لطباعة الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="82a70-120">Select Yes for Print invoice.</span></span>
    * <span data-ttu-id="82a70-121">بإمكان إدارة الطباعة‬ طباعة نسخ متعددة من الفاتورة وأيضًا إرسال الفاتورة عبر البريد الإلكتروني كملف PDF.</span><span class="sxs-lookup"><span data-stu-id="82a70-121">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
8. <span data-ttu-id="82a70-122">في الحقل "طباعة التكاليف‬"، حدد "تلخيص‬".</span><span class="sxs-lookup"><span data-stu-id="82a70-122">In the Print charges field, select 'Summarize'.</span></span>
9. <span data-ttu-id="82a70-123">في حقل "فحص الحد الائتماني‬"، حدد "الرصيد'.</span><span class="sxs-lookup"><span data-stu-id="82a70-123">In the Check credit limit field, select 'Balance'.</span></span>
10. <span data-ttu-id="82a70-124">انقر فوق "إلغاء".</span><span class="sxs-lookup"><span data-stu-id="82a70-124">Click Cancel.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="82a70-125">دمج أوامر في فاتورة واحدة</span><span class="sxs-lookup"><span data-stu-id="82a70-125">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="82a70-126">انتقل إلى الحسابات المدينة > الأوامر > كافة أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="82a70-126">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="82a70-127">حدد موقع عميل لديه عدة فواتير مفتوحة.</span><span class="sxs-lookup"><span data-stu-id="82a70-127">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="82a70-128">حدد أمر توريد مفتوح.</span><span class="sxs-lookup"><span data-stu-id="82a70-128">Select an open sales order.</span></span>
4. <span data-ttu-id="82a70-129">حدد أمر مبيعات آخر مفتوحًا للعميل نفسه.</span><span class="sxs-lookup"><span data-stu-id="82a70-129">Select another open sales order for the same customer.</span></span>
5. <span data-ttu-id="82a70-130">في جزء "الإجراءات"، انقر فوق "فاتورة".</span><span class="sxs-lookup"><span data-stu-id="82a70-130">On the Action Pane, click Invoice.</span></span>
6. <span data-ttu-id="82a70-131">انقر فوق "فاتورة".</span><span class="sxs-lookup"><span data-stu-id="82a70-131">Click Invoice.</span></span>
7. <span data-ttu-id="82a70-132">وسّع مقطع "المحددات".</span><span class="sxs-lookup"><span data-stu-id="82a70-132">Expand the Parameters section.</span></span>
8. <span data-ttu-id="82a70-133">في الحقل "الكمية"، حدد "الكل".</span><span class="sxs-lookup"><span data-stu-id="82a70-133">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="82a70-134">لاحظ أن مقطع النظرة العامة يتضمن فاتورتين مدرجتين فيه.</span><span class="sxs-lookup"><span data-stu-id="82a70-134">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="82a70-135">لنعمل الآن على دمجهما في فاتورة واحدة.</span><span class="sxs-lookup"><span data-stu-id="82a70-135">Now let's merge them into a single invoice.</span></span>  
9. <span data-ttu-id="82a70-136">في الحقل "تحديث ملخص لـ‬"، حدد "حساب الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="82a70-136">In the Summary update for field, select 'Invoice account'.</span></span>
10. <span data-ttu-id="82a70-137">انقر فوق "ترتيب" لدمج أوامر المبيعات في فاتورة واحدة.</span><span class="sxs-lookup"><span data-stu-id="82a70-137">Click Arrange to merge the sales orders into a single invoice.</span></span>
    * <span data-ttu-id="82a70-138">تم الآن دمج أمري المبيعات في فاتورة واحدة.</span><span class="sxs-lookup"><span data-stu-id="82a70-138">The two sales orders are now merged into a single invoice.</span></span>   
11. <span data-ttu-id="82a70-139">انقر فوق "إلغاء".</span><span class="sxs-lookup"><span data-stu-id="82a70-139">Click Cancel.</span></span>
12. <span data-ttu-id="82a70-140">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="82a70-140">Click Yes.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="82a70-141">ترحيل الفواتير في دُفعة</span><span class="sxs-lookup"><span data-stu-id="82a70-141">Post invoices in a batch</span></span>
1. <span data-ttu-id="82a70-142">انتقل إلى الحسابات المدينة > الفواتير > فوترة الدُفعة‬ > فاتورة.</span><span class="sxs-lookup"><span data-stu-id="82a70-142">Go to Accounts receivable > Invoices > Batch invoicing > Invoice.</span></span>
2. <span data-ttu-id="82a70-143">انقر فوق تحديد.</span><span class="sxs-lookup"><span data-stu-id="82a70-143">Click Select.</span></span>
3. <span data-ttu-id="82a70-144">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="82a70-144">Click OK.</span></span>
4. <span data-ttu-id="82a70-145">انقر فوق "دُفعة".</span><span class="sxs-lookup"><span data-stu-id="82a70-145">Click Batch.</span></span>
5. <span data-ttu-id="82a70-146">انقر فوق "نعم" لتشغيل معالجة الدُفعة.</span><span class="sxs-lookup"><span data-stu-id="82a70-146">Click on Yes to turn on batch processing.</span></span>
6. <span data-ttu-id="82a70-147">انقر فوق "تكرار".</span><span class="sxs-lookup"><span data-stu-id="82a70-147">Click Recurrence.</span></span>
7. <span data-ttu-id="82a70-148">حدد "الأيام‬".</span><span class="sxs-lookup"><span data-stu-id="82a70-148">Select Days</span></span>
8. <span data-ttu-id="82a70-149">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="82a70-149">Click OK.</span></span>
9. <span data-ttu-id="82a70-150">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="82a70-150">Click OK.</span></span>
10. <span data-ttu-id="82a70-151">انقر فوق "إلغاء".</span><span class="sxs-lookup"><span data-stu-id="82a70-151">Click Cancel.</span></span>
11. <span data-ttu-id="82a70-152">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="82a70-152">Click Yes.</span></span>

