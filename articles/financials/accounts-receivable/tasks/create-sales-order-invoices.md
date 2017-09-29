--- 
title: "إنشاء فواتير أمر المبيعات"
description: "يوضح دليل المهمة هذا فوترة أمر مبيعات، بما في ذلك دمج الفواتير ومعالجة الدُفعة."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 4b72d5b283f9401d358ee68f4650c486ebb2fd7d
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="e1c87-103">إنشاء فواتير أمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="e1c87-103">Create sales order invoices</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e1c87-104">يوضح دليل المهمة هذا فوترة أمر مبيعات، بما في ذلك دمج الفواتير ومعالجة الدُفعة.</span><span class="sxs-lookup"><span data-stu-id="e1c87-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="e1c87-105">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="e1c87-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="e1c87-106">إنشاء فاتورة من أمر مبيعات</span><span class="sxs-lookup"><span data-stu-id="e1c87-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="e1c87-107">انتقل إلى الحسابات المدينة > الأوامر‬ > أوامر المبيعات المشحونة وغير المفوترة‬.</span><span class="sxs-lookup"><span data-stu-id="e1c87-107">Go to Accounts receivable > Orders > Shipped but not invoiced sales orders.</span></span>
2. <span data-ttu-id="e1c87-108">حدد أمر مبيعات من القائمة.</span><span class="sxs-lookup"><span data-stu-id="e1c87-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="e1c87-109">في جزء "الإجراءات"، انقر فوق "فاتورة".</span><span class="sxs-lookup"><span data-stu-id="e1c87-109">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="e1c87-110">انقر فوق "فاتورة".</span><span class="sxs-lookup"><span data-stu-id="e1c87-110">Click Invoice.</span></span>
    * <span data-ttu-id="e1c87-111">لاحظ أن أمر المبيعات هذا لديه إيصالات تعبئة متعددة مقترنة به.</span><span class="sxs-lookup"><span data-stu-id="e1c87-111">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="e1c87-112">وسوف يعرض كلمة <multiple> فقط بدلاً من رقم إيصال التعبئة.</span><span class="sxs-lookup"><span data-stu-id="e1c87-112">It will only show the word <multiple> instead of the packing slip number.</span></span>  
5. <span data-ttu-id="e1c87-113">وسّع مقطع "المحددات".</span><span class="sxs-lookup"><span data-stu-id="e1c87-113">Expand the Parameters section.</span></span>
    * <span data-ttu-id="e1c87-114">يجب تعيين الترحيل إلى "نعم" لترحيل الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="e1c87-114">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="e1c87-115">يمكنك أيضًا إيقاف ترحيل الفاتورة وطباعتها فقط.</span><span class="sxs-lookup"><span data-stu-id="e1c87-115">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="e1c87-116">ومع ذلك، يمكنك تحقيق نفس النتيجة عن طريق إنشاء فاتورة مبدئية بدلاً من فاتورة.</span><span class="sxs-lookup"><span data-stu-id="e1c87-116">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    * <span data-ttu-id="e1c87-117">وهذا الخيار يُستخدم لوظائف الدُفعات.</span><span class="sxs-lookup"><span data-stu-id="e1c87-117">This option is used for batch jobs.</span></span> <span data-ttu-id="e1c87-118">ويتم إجراء الاستعلام عند تشغيل وظيفة الدُفعة.</span><span class="sxs-lookup"><span data-stu-id="e1c87-118">The query is run when the batch job is run.</span></span>    
6. <span data-ttu-id="e1c87-119">في الحقل "طباعة"، حدد "بعد".</span><span class="sxs-lookup"><span data-stu-id="e1c87-119">In the Print field, select 'After'.</span></span>
7. <span data-ttu-id="e1c87-120">حدد "نعم" لطباعة الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="e1c87-120">Select Yes for Print invoice.</span></span>
    * <span data-ttu-id="e1c87-121">بإمكان إدارة الطباعة‬ طباعة نسخ متعددة من الفاتورة وأيضًا إرسال الفاتورة عبر البريد الإلكتروني كملف PDF.</span><span class="sxs-lookup"><span data-stu-id="e1c87-121">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
8. <span data-ttu-id="e1c87-122">في الحقل "طباعة التكاليف‬"، حدد "تلخيص‬".</span><span class="sxs-lookup"><span data-stu-id="e1c87-122">In the Print charges field, select 'Summarize'.</span></span>
9. <span data-ttu-id="e1c87-123">في حقل "فحص الحد الائتماني‬"، حدد "الرصيد'.</span><span class="sxs-lookup"><span data-stu-id="e1c87-123">In the Check credit limit field, select 'Balance'.</span></span>
10. <span data-ttu-id="e1c87-124">انقر فوق "إلغاء".</span><span class="sxs-lookup"><span data-stu-id="e1c87-124">Click Cancel.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="e1c87-125">دمج أوامر في فاتورة واحدة</span><span class="sxs-lookup"><span data-stu-id="e1c87-125">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="e1c87-126">انتقل إلى الحسابات المدينة > الأوامر > كافة أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="e1c87-126">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="e1c87-127">حدد موقع عميل لديه عدة فواتير مفتوحة.</span><span class="sxs-lookup"><span data-stu-id="e1c87-127">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="e1c87-128">حدد أمر توريد مفتوح.</span><span class="sxs-lookup"><span data-stu-id="e1c87-128">Select an open sales order.</span></span>
4. <span data-ttu-id="e1c87-129">حدد أمر مبيعات آخر مفتوحًا للعميل نفسه.</span><span class="sxs-lookup"><span data-stu-id="e1c87-129">Select another open sales order for the same customer.</span></span>
5. <span data-ttu-id="e1c87-130">في جزء "الإجراءات"، انقر فوق "فاتورة".</span><span class="sxs-lookup"><span data-stu-id="e1c87-130">On the Action Pane, click Invoice.</span></span>
6. <span data-ttu-id="e1c87-131">انقر فوق "فاتورة".</span><span class="sxs-lookup"><span data-stu-id="e1c87-131">Click Invoice.</span></span>
7. <span data-ttu-id="e1c87-132">وسّع مقطع "المحددات".</span><span class="sxs-lookup"><span data-stu-id="e1c87-132">Expand the Parameters section.</span></span>
8. <span data-ttu-id="e1c87-133">في الحقل "الكمية"، حدد "الكل".</span><span class="sxs-lookup"><span data-stu-id="e1c87-133">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="e1c87-134">لاحظ أن مقطع النظرة العامة يتضمن فاتورتين مدرجتين فيه.</span><span class="sxs-lookup"><span data-stu-id="e1c87-134">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="e1c87-135">لنعمل الآن على دمجهما في فاتورة واحدة.</span><span class="sxs-lookup"><span data-stu-id="e1c87-135">Now let's merge them into a single invoice.</span></span>  
9. <span data-ttu-id="e1c87-136">في الحقل "تحديث ملخص لـ‬"، حدد "حساب الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="e1c87-136">In the Summary update for field, select 'Invoice account'.</span></span>
10. <span data-ttu-id="e1c87-137">انقر فوق "ترتيب" لدمج أوامر المبيعات في فاتورة واحدة.</span><span class="sxs-lookup"><span data-stu-id="e1c87-137">Click Arrange to merge the sales orders into a single invoice.</span></span>
    * <span data-ttu-id="e1c87-138">تم الآن دمج أمري المبيعات في فاتورة واحدة.</span><span class="sxs-lookup"><span data-stu-id="e1c87-138">The two sales orders are now merged into a single invoice.</span></span>   
11. <span data-ttu-id="e1c87-139">انقر فوق "إلغاء".</span><span class="sxs-lookup"><span data-stu-id="e1c87-139">Click Cancel.</span></span>
12. <span data-ttu-id="e1c87-140">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="e1c87-140">Click Yes.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="e1c87-141">ترحيل الفواتير في دُفعة</span><span class="sxs-lookup"><span data-stu-id="e1c87-141">Post invoices in a batch</span></span>
1. <span data-ttu-id="e1c87-142">انتقل إلى الحسابات المدينة > الفواتير > فوترة الدُفعة‬ > فاتورة.</span><span class="sxs-lookup"><span data-stu-id="e1c87-142">Go to Accounts receivable > Invoices > Batch invoicing > Invoice.</span></span>
2. <span data-ttu-id="e1c87-143">انقر فوق تحديد.</span><span class="sxs-lookup"><span data-stu-id="e1c87-143">Click Select.</span></span>
3. <span data-ttu-id="e1c87-144">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="e1c87-144">Click OK.</span></span>
4. <span data-ttu-id="e1c87-145">انقر فوق "دُفعة".</span><span class="sxs-lookup"><span data-stu-id="e1c87-145">Click Batch.</span></span>
5. <span data-ttu-id="e1c87-146">انقر فوق "نعم" لتشغيل معالجة الدُفعة.</span><span class="sxs-lookup"><span data-stu-id="e1c87-146">Click on Yes to turn on batch processing.</span></span>
6. <span data-ttu-id="e1c87-147">انقر فوق "تكرار".</span><span class="sxs-lookup"><span data-stu-id="e1c87-147">Click Recurrence.</span></span>
7. <span data-ttu-id="e1c87-148">حدد "الأيام‬".</span><span class="sxs-lookup"><span data-stu-id="e1c87-148">Select Days</span></span>
8. <span data-ttu-id="e1c87-149">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="e1c87-149">Click OK.</span></span>
9. <span data-ttu-id="e1c87-150">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="e1c87-150">Click OK.</span></span>
10. <span data-ttu-id="e1c87-151">انقر فوق "إلغاء".</span><span class="sxs-lookup"><span data-stu-id="e1c87-151">Click Cancel.</span></span>
11. <span data-ttu-id="e1c87-152">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="e1c87-152">Click Yes.</span></span>


