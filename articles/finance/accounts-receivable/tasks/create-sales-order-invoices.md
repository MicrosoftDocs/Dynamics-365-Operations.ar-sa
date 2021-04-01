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
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4d2e1dd552f529d09756c1ddeec39fc54a1f073a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241576"
---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="31cda-103">إنشاء فواتير أمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="31cda-103">Create sales order invoices</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="31cda-104">يوضح دليل المهمة هذا فوترة أمر مبيعات، بما في ذلك دمج الفواتير ومعالجة الدُفعة.</span><span class="sxs-lookup"><span data-stu-id="31cda-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="31cda-105">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="31cda-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="31cda-106">إنشاء فاتورة من أمر مبيعات</span><span class="sxs-lookup"><span data-stu-id="31cda-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="31cda-107">انتقل إلى **جزء التنقل > الوحدات النمطية > الحسابات المدينة > الأوامر > أوامر المبيعات المشحونة وغير المفوترة‬**.</span><span class="sxs-lookup"><span data-stu-id="31cda-107">Go to **Navigation pane > Modules > Accounts receivable > Orders > Shipped but not invoiced sales orders**.</span></span>
2. <span data-ttu-id="31cda-108">حدد أمر مبيعات من القائمة.</span><span class="sxs-lookup"><span data-stu-id="31cda-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="31cda-109">في **جزء الإجراءات **، انقر فوق** فاتورة > عام > فاتورة**.</span><span class="sxs-lookup"><span data-stu-id="31cda-109">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span> <span data-ttu-id="31cda-110">لاحظ أن أمر المبيعات هذا لديه إيصالات تعبئة متعددة مقترنة به.</span><span class="sxs-lookup"><span data-stu-id="31cda-110">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="31cda-111">وسوف يعرض كلمة <multiple> فقط بدلاً من رقم إيصال التعبئة.</span><span class="sxs-lookup"><span data-stu-id="31cda-111">It will only show the word <multiple> instead of the packing slip number.</span></span>  
4. <span data-ttu-id="31cda-112">قم بتوسيع قسم **المحددات**.</span><span class="sxs-lookup"><span data-stu-id="31cda-112">Expand the **Parameters** section.</span></span>
    - <span data-ttu-id="31cda-113">يجب تعيين الترحيل إلى "نعم" لترحيل الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="31cda-113">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="31cda-114">يمكنك أيضًا إيقاف ترحيل الفاتورة وطباعتها فقط.</span><span class="sxs-lookup"><span data-stu-id="31cda-114">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="31cda-115">ومع ذلك، يمكنك تحقيق نفس النتيجة عن طريق إنشاء فاتورة مبدئية بدلاً من فاتورة.</span><span class="sxs-lookup"><span data-stu-id="31cda-115">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    - <span data-ttu-id="31cda-116">وهذا الخيار يُستخدم لوظائف الدُفعات.</span><span class="sxs-lookup"><span data-stu-id="31cda-116">This option is used for batch jobs.</span></span> <span data-ttu-id="31cda-117">ويتم إجراء الاستعلام عند تشغيل وظيفة الدُفعة.</span><span class="sxs-lookup"><span data-stu-id="31cda-117">The query is run when the batch job is run.</span></span>
5. <span data-ttu-id="31cda-118">في الحقل **طباعة**، حدد "بعد".</span><span class="sxs-lookup"><span data-stu-id="31cda-118">In the **Print** field, select 'After'.</span></span>
6. <span data-ttu-id="31cda-119">حدد **نعم** في **طباعة الفاتورة**.</span><span class="sxs-lookup"><span data-stu-id="31cda-119">Select **Yes** for **Print invoice**.</span></span> <span data-ttu-id="31cda-120">بإمكان إدارة الطباعة‬ طباعة نسخ متعددة من الفاتورة وأيضًا إرسال الفاتورة عبر البريد الإلكتروني كملف PDF.</span><span class="sxs-lookup"><span data-stu-id="31cda-120">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
7. <span data-ttu-id="31cda-121">في الحقل **طباعة التكاليف**، حدد "تلخيص‬".</span><span class="sxs-lookup"><span data-stu-id="31cda-121">In the **Print charges** field, select 'Summarize'.</span></span>
8. <span data-ttu-id="31cda-122">في حقل **فحص الحد الائتماني‬**، حدد "الرصيد'.</span><span class="sxs-lookup"><span data-stu-id="31cda-122">In the **Check credit limit** field, select 'Balance'.</span></span>
9. <span data-ttu-id="31cda-123">وانقر فوق **إلغاء الأمر**.</span><span class="sxs-lookup"><span data-stu-id="31cda-123">Click **Cancel**.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="31cda-124">دمج أوامر في فاتورة واحدة</span><span class="sxs-lookup"><span data-stu-id="31cda-124">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="31cda-125">انتقل إلى **جزء التنقل > الوحدات النمطية > الحسابات المدينة > الأوامر > كافة أوامر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="31cda-125">Go to **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="31cda-126">حدد موقع عميل لديه عدة فواتير مفتوحة.</span><span class="sxs-lookup"><span data-stu-id="31cda-126">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="31cda-127">حدد أوامر مبيعات مفتوحة متعددة من نفس العميل.</span><span class="sxs-lookup"><span data-stu-id="31cda-127">Select multiple open sales orders from the same customer.</span></span>
4. <span data-ttu-id="31cda-128">في **جزء الإجراءات **، انقر فوق** فاتورة > عام > فاتورة**.</span><span class="sxs-lookup"><span data-stu-id="31cda-128">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span>
5. <span data-ttu-id="31cda-129">قم بتوسيع قسم **المحددات**.</span><span class="sxs-lookup"><span data-stu-id="31cda-129">Expand the **Parameters** section.</span></span>
6. <span data-ttu-id="31cda-130">في حقل **الكمية** ، حدد "الكل".</span><span class="sxs-lookup"><span data-stu-id="31cda-130">In the **Quantity** field, select 'All'.</span></span> <span data-ttu-id="31cda-131">لاحظ أن مقطع النظرة العامة يتضمن فاتورتين مدرجتين فيه.</span><span class="sxs-lookup"><span data-stu-id="31cda-131">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="31cda-132">لنعمل الآن على دمجهما في فاتورة واحدة.</span><span class="sxs-lookup"><span data-stu-id="31cda-132">Now let's merge them into a single invoice.</span></span>  
7. <span data-ttu-id="31cda-133">في الحقل **تحديث ملخص لـ‬**، حدد "حساب الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="31cda-133">In the **Summary update for** field, select 'Invoice account'.</span></span>
8. <span data-ttu-id="31cda-134">انقر فوق **ترتيب** لدمج أوامر المبيعات في فاتورة واحدة.</span><span class="sxs-lookup"><span data-stu-id="31cda-134">Click **Arrange** to merge the sales orders into a single invoice.</span></span> <span data-ttu-id="31cda-135">تم الآن دمج أمري المبيعات في فاتورة واحدة.</span><span class="sxs-lookup"><span data-stu-id="31cda-135">The two sales orders are now merged into a single invoice.</span></span>   
9. <span data-ttu-id="31cda-136">وانقر فوق **إلغاء الأمر**.</span><span class="sxs-lookup"><span data-stu-id="31cda-136">Click **Cancel**.</span></span>
10. <span data-ttu-id="31cda-137">انقر فوق **نعم**.</span><span class="sxs-lookup"><span data-stu-id="31cda-137">Click **Yes**.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="31cda-138">ترحيل الفواتير في دُفعة</span><span class="sxs-lookup"><span data-stu-id="31cda-138">Post invoices in a batch</span></span>
1. <span data-ttu-id="31cda-139">انتقل إلى **جزء التنقل > الوحدات النمطية > الحسابات المدينة > الفواتير > فوترة الدُفعة‬ > فاتورة‬**.</span><span class="sxs-lookup"><span data-stu-id="31cda-139">Go to **Navigation pane > Modules > Accounts receivable > Invoices > Batch invoicing > Invoice**.</span></span>
2. <span data-ttu-id="31cda-140">انقر فوق **تحديد**.</span><span class="sxs-lookup"><span data-stu-id="31cda-140">Click **Select**.</span></span>
3. <span data-ttu-id="31cda-141">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="31cda-141">Click **OK**.</span></span>
4. <span data-ttu-id="31cda-142">انقر فوق **دُفعة**.</span><span class="sxs-lookup"><span data-stu-id="31cda-142">Click **Batch**.</span></span>
5. <span data-ttu-id="31cda-143">في **معالجة الدُفعة**، حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="31cda-143">Select **Yes** in **Batch processing**.</span></span>
6. <span data-ttu-id="31cda-144">انقر فوق **التكرار**.</span><span class="sxs-lookup"><span data-stu-id="31cda-144">Click **Recurrence**.</span></span>
7. <span data-ttu-id="31cda-145">حدد **الأيام‬**.</span><span class="sxs-lookup"><span data-stu-id="31cda-145">Select **Days**.</span></span>
8. <span data-ttu-id="31cda-146">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="31cda-146">Click **OK**.</span></span>
9. <span data-ttu-id="31cda-147">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="31cda-147">Click **OK**.</span></span>
10. <span data-ttu-id="31cda-148">وانقر فوق **إلغاء الأمر**.</span><span class="sxs-lookup"><span data-stu-id="31cda-148">Click **Cancel**.</span></span>
11. <span data-ttu-id="31cda-149">انقر فوق **نعم**.</span><span class="sxs-lookup"><span data-stu-id="31cda-149">Click **Yes**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]