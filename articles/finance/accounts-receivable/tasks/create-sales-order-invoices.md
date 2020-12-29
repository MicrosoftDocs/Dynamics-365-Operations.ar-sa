---
title: إنشاء فواتير أمر المبيعات
description: يوضح دليل المهمة هذا فوترة أمر مبيعات، بما في ذلك دمج الفواتير ومعالجة الدُفعة.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c504ef36f61613c7aa7db5a1e5ddba6e69cd7285
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440076"
---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="eba5e-103">إنشاء فواتير أمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="eba5e-103">Create sales order invoices</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eba5e-104">يوضح دليل المهمة هذا فوترة أمر مبيعات، بما في ذلك دمج الفواتير ومعالجة الدُفعة.</span><span class="sxs-lookup"><span data-stu-id="eba5e-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="eba5e-105">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="eba5e-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="eba5e-106">إنشاء فاتورة من أمر مبيعات</span><span class="sxs-lookup"><span data-stu-id="eba5e-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="eba5e-107">انتقل إلى **جزء التنقل > الوحدات النمطية > الحسابات المدينة > الأوامر > أوامر المبيعات المشحونة وغير المفوترة‬**.</span><span class="sxs-lookup"><span data-stu-id="eba5e-107">Go to **Navigation pane > Modules > Accounts receivable > Orders > Shipped but not invoiced sales orders**.</span></span>
2. <span data-ttu-id="eba5e-108">حدد أمر مبيعات من القائمة.</span><span class="sxs-lookup"><span data-stu-id="eba5e-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="eba5e-109">في **جزء الإجراءات **، انقر فوق** فاتورة > عام > فاتورة**.</span><span class="sxs-lookup"><span data-stu-id="eba5e-109">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span> <span data-ttu-id="eba5e-110">لاحظ أن أمر المبيعات هذا لديه إيصالات تعبئة متعددة مقترنة به.</span><span class="sxs-lookup"><span data-stu-id="eba5e-110">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="eba5e-111">وسوف يعرض كلمة <multiple> فقط بدلاً من رقم إيصال التعبئة.</span><span class="sxs-lookup"><span data-stu-id="eba5e-111">It will only show the word <multiple> instead of the packing slip number.</span></span>  
4. <span data-ttu-id="eba5e-112">قم بتوسيع قسم **المحددات**.</span><span class="sxs-lookup"><span data-stu-id="eba5e-112">Expand the **Parameters** section.</span></span>
    - <span data-ttu-id="eba5e-113">يجب تعيين الترحيل إلى "نعم" لترحيل الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="eba5e-113">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="eba5e-114">يمكنك أيضًا إيقاف ترحيل الفاتورة وطباعتها فقط.</span><span class="sxs-lookup"><span data-stu-id="eba5e-114">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="eba5e-115">ومع ذلك، يمكنك تحقيق نفس النتيجة عن طريق إنشاء فاتورة مبدئية بدلاً من فاتورة.</span><span class="sxs-lookup"><span data-stu-id="eba5e-115">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    - <span data-ttu-id="eba5e-116">وهذا الخيار يُستخدم لوظائف الدُفعات.</span><span class="sxs-lookup"><span data-stu-id="eba5e-116">This option is used for batch jobs.</span></span> <span data-ttu-id="eba5e-117">ويتم إجراء الاستعلام عند تشغيل وظيفة الدُفعة.</span><span class="sxs-lookup"><span data-stu-id="eba5e-117">The query is run when the batch job is run.</span></span>
5. <span data-ttu-id="eba5e-118">في الحقل **طباعة**، حدد "بعد".</span><span class="sxs-lookup"><span data-stu-id="eba5e-118">In the **Print** field, select 'After'.</span></span>
6. <span data-ttu-id="eba5e-119">حدد **نعم** في **طباعة الفاتورة**.</span><span class="sxs-lookup"><span data-stu-id="eba5e-119">Select **Yes** for **Print invoice**.</span></span> <span data-ttu-id="eba5e-120">بإمكان إدارة الطباعة‬ طباعة نسخ متعددة من الفاتورة وأيضًا إرسال الفاتورة عبر البريد الإلكتروني كملف PDF.</span><span class="sxs-lookup"><span data-stu-id="eba5e-120">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
7. <span data-ttu-id="eba5e-121">في الحقل **طباعة التكاليف**، حدد "تلخيص‬".</span><span class="sxs-lookup"><span data-stu-id="eba5e-121">In the **Print charges** field, select 'Summarize'.</span></span>
8. <span data-ttu-id="eba5e-122">في حقل **فحص الحد الائتماني‬**، حدد "الرصيد'.</span><span class="sxs-lookup"><span data-stu-id="eba5e-122">In the **Check credit limit** field, select 'Balance'.</span></span>
9. <span data-ttu-id="eba5e-123">وانقر فوق **إلغاء الأمر**.</span><span class="sxs-lookup"><span data-stu-id="eba5e-123">Click **Cancel**.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="eba5e-124">دمج أوامر في فاتورة واحدة</span><span class="sxs-lookup"><span data-stu-id="eba5e-124">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="eba5e-125">انتقل إلى **جزء التنقل > الوحدات النمطية > الحسابات المدينة > الأوامر > كافة أوامر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="eba5e-125">Go to **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="eba5e-126">حدد موقع عميل لديه عدة فواتير مفتوحة.</span><span class="sxs-lookup"><span data-stu-id="eba5e-126">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="eba5e-127">حدد أوامر مبيعات مفتوحة متعددة من نفس العميل.</span><span class="sxs-lookup"><span data-stu-id="eba5e-127">Select multiple open sales orders from the same customer.</span></span>
4. <span data-ttu-id="eba5e-128">في **جزء الإجراءات **، انقر فوق** فاتورة > عام > فاتورة**.</span><span class="sxs-lookup"><span data-stu-id="eba5e-128">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span>
5. <span data-ttu-id="eba5e-129">قم بتوسيع قسم **المحددات**.</span><span class="sxs-lookup"><span data-stu-id="eba5e-129">Expand the **Parameters** section.</span></span>
6. <span data-ttu-id="eba5e-130">في حقل **الكمية** ، حدد "الكل".</span><span class="sxs-lookup"><span data-stu-id="eba5e-130">In the **Quantity** field, select 'All'.</span></span> <span data-ttu-id="eba5e-131">لاحظ أن مقطع النظرة العامة يتضمن فاتورتين مدرجتين فيه.</span><span class="sxs-lookup"><span data-stu-id="eba5e-131">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="eba5e-132">لنعمل الآن على دمجهما في فاتورة واحدة.</span><span class="sxs-lookup"><span data-stu-id="eba5e-132">Now let's merge them into a single invoice.</span></span>  
7. <span data-ttu-id="eba5e-133">في الحقل **تحديث ملخص لـ‬**، حدد "حساب الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="eba5e-133">In the **Summary update for** field, select 'Invoice account'.</span></span>
8. <span data-ttu-id="eba5e-134">انقر فوق **ترتيب** لدمج أوامر المبيعات في فاتورة واحدة.</span><span class="sxs-lookup"><span data-stu-id="eba5e-134">Click **Arrange** to merge the sales orders into a single invoice.</span></span> <span data-ttu-id="eba5e-135">تم الآن دمج أمري المبيعات في فاتورة واحدة.</span><span class="sxs-lookup"><span data-stu-id="eba5e-135">The two sales orders are now merged into a single invoice.</span></span>   
9. <span data-ttu-id="eba5e-136">وانقر فوق **إلغاء الأمر**.</span><span class="sxs-lookup"><span data-stu-id="eba5e-136">Click **Cancel**.</span></span>
10. <span data-ttu-id="eba5e-137">انقر فوق **نعم**.</span><span class="sxs-lookup"><span data-stu-id="eba5e-137">Click **Yes**.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="eba5e-138">ترحيل الفواتير في دُفعة</span><span class="sxs-lookup"><span data-stu-id="eba5e-138">Post invoices in a batch</span></span>
1. <span data-ttu-id="eba5e-139">انتقل إلى **جزء التنقل > الوحدات النمطية > الحسابات المدينة > الفواتير > فوترة الدُفعة‬ > فاتورة‬**.</span><span class="sxs-lookup"><span data-stu-id="eba5e-139">Go to **Navigation pane > Modules > Accounts receivable > Invoices > Batch invoicing > Invoice**.</span></span>
2. <span data-ttu-id="eba5e-140">انقر فوق **تحديد**.</span><span class="sxs-lookup"><span data-stu-id="eba5e-140">Click **Select**.</span></span>
3. <span data-ttu-id="eba5e-141">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="eba5e-141">Click **OK**.</span></span>
4. <span data-ttu-id="eba5e-142">انقر فوق **دُفعة**.</span><span class="sxs-lookup"><span data-stu-id="eba5e-142">Click **Batch**.</span></span>
5. <span data-ttu-id="eba5e-143">في **معالجة الدُفعة**، حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="eba5e-143">Select **Yes** in **Batch processing**.</span></span>
6. <span data-ttu-id="eba5e-144">انقر فوق **التكرار**.</span><span class="sxs-lookup"><span data-stu-id="eba5e-144">Click **Recurrence**.</span></span>
7. <span data-ttu-id="eba5e-145">حدد **الأيام‬**.</span><span class="sxs-lookup"><span data-stu-id="eba5e-145">Select **Days**.</span></span>
8. <span data-ttu-id="eba5e-146">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="eba5e-146">Click **OK**.</span></span>
9. <span data-ttu-id="eba5e-147">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="eba5e-147">Click **OK**.</span></span>
10. <span data-ttu-id="eba5e-148">وانقر فوق **إلغاء الأمر**.</span><span class="sxs-lookup"><span data-stu-id="eba5e-148">Click **Cancel**.</span></span>
11. <span data-ttu-id="eba5e-149">انقر فوق **نعم**.</span><span class="sxs-lookup"><span data-stu-id="eba5e-149">Click **Yes**.</span></span>

