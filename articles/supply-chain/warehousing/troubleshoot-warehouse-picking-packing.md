---
title: استكشاف أخطاء الانتقاء والتعبئة واصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء انتقاء وتعبئة Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 01e33b63e09a035f5243bd57faf53b522737c987
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223232"
---
# <a name="troubleshoot-picking-and-packing"></a><span data-ttu-id="904ce-103">استكشاف أخطاء الانتقاء والتعبئة واصلاحها</span><span class="sxs-lookup"><span data-stu-id="904ce-103">Troubleshoot picking and packing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="904ce-104">يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء انتقاء وتعبئة Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="904ce-104">This topic describes how to fix common issues that you might encounter while you pick and pack in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-dimension-location-cant-be-left-blank-if-dimension-serial-number-is-set"></a><span data-ttu-id="904ce-105">أتلقى رسالة الخطا التالية: "لا يمكن ترك موقع البعد فارغا إذا تم تعيين الرقم المسلسل للبعد."</span><span class="sxs-lookup"><span data-stu-id="904ce-105">I receive the following error message: "Dimension location can't be left blank if dimension serial number is set."</span></span>

### <a name="issue-description"></a><span data-ttu-id="904ce-106">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="904ce-106">Issue description</span></span>

<span data-ttu-id="904ce-107">تظهر رسالة الخطا هذه إذا قمت بإنشاء أمر لصنف مسلسل باستخدام مستودع ممكن لأداره المستودعات المتقدمة (WMS)، ثم بعد اكتمال العمل ، فانك تحاول تاكيد الشحن.</span><span class="sxs-lookup"><span data-stu-id="904ce-107">You receive this error message if you create a transfer order for a serial item by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="904ce-108">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="904ce-108">Issue resolution</span></span>

<span data-ttu-id="904ce-109">حقل **موقع الاستلام الافتراضي** فارغ لمخزن بضاعة بالطريق للمستودع "من".</span><span class="sxs-lookup"><span data-stu-id="904ce-109">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="904ce-110">لحل هذه المشكلة ، حدد موقع استلام افتراضي في مخزن البضاعة بالطريق.</span><span class="sxs-lookup"><span data-stu-id="904ce-110">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="904ce-111">تاكد من ان هذا الموقع هو لوحه الترخيص – التي يتم التحكم بها.</span><span class="sxs-lookup"><span data-stu-id="904ce-111">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-invalid-license-plate"></a><span data-ttu-id="904ce-112">أتلقى رسالة الخطا التالية: "لوحه ترخيص غير صالحه".</span><span class="sxs-lookup"><span data-stu-id="904ce-112">I receive the following error message: "Invalid license plate."</span></span>

### <a name="issue-description"></a><span data-ttu-id="904ce-113">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="904ce-113">Issue description</span></span>

<span data-ttu-id="904ce-114">تظهر رسالة الخطا هذه في تطبيق المستودع عند مسح معرف لوحه الترخيص.</span><span class="sxs-lookup"><span data-stu-id="904ce-114">You receive this error message in the warehouse app when you scan a license plate ID.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="904ce-115">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="904ce-115">Issue resolution</span></span>

<span data-ttu-id="904ce-116">تاكد من وجود معرف لوح الترخيص في جدول لوحات الترخيص ، وان الأصناف والكميات الموجودة في لوحه الترخيص متوفرة (بمعني آخر ، فهي لا يتم حظرها).</span><span class="sxs-lookup"><span data-stu-id="904ce-116">Make sure that the license plate ID exists in the license plates table, and that the items and quantities on the license plate are available (in other words, they aren't blocked).</span></span>

## <a name="i-receive-the-following-error-message-field-load-weight-1-can-only-contain-positive-numbers-update-has-been-canceled"></a><span data-ttu-id="904ce-117">أتلقى رسالة الخطا التالية: "يمكن ان يحتوي الحقل 'وزن التحميل' (=- %1) علي أرقام موجبه فقط.</span><span class="sxs-lookup"><span data-stu-id="904ce-117">I receive the following error message: "Field 'Load weight'(=-%1) can only contain positive numbers.</span></span> <span data-ttu-id="904ce-118">تم إلغاء التحديث."</span><span class="sxs-lookup"><span data-stu-id="904ce-118">Update has been canceled."</span></span>

### <a name="issue-description"></a><span data-ttu-id="904ce-119">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="904ce-119">Issue description</span></span>

<span data-ttu-id="904ce-120">تظهر رسالة الخطا هذه في حاله وجود عمل مفتوح عند معالجه العمل من مواقع التعبئة إلى مواقع التقسيم أو من المواقع المرحلية لإرساء المواقع.</span><span class="sxs-lookup"><span data-stu-id="904ce-120">You receive this error message if there is open work when you process work from packing locations to staging locations, or from staging locations to dock locations.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="904ce-121">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="904ce-121">Issue resolution</span></span>

<span data-ttu-id="904ce-122">لحل هذه المشكلة ، انتقل إلى **إدار النظام \> المهام الدورية \> قاعدة البيانات \> فحص الاتساق**، ثم قم بتشغيل عمليه **فحص اتساق وزن الحمولة للمستودع**.</span><span class="sxs-lookup"><span data-stu-id="904ce-122">To fix this issue, go to **System administration \> Periodic tasks \> Database \> Consistency check**, and run the process for **Warehouse load weight consistency check**.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="904ce-123">أتلقى رسالة الخطا التالية: "الكمية غير صالحة للوحدة %1."</span><span class="sxs-lookup"><span data-stu-id="904ce-123">I receive the following error message: "The quantity is not valid for unit %1."</span></span>

### <a name="issue-description"></a><span data-ttu-id="904ce-124">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="904ce-124">Issue description</span></span>

<span data-ttu-id="904ce-125">تظهر رسالة الخطا هذه عند محاولة تنفيذ عمليه *انتقاء التقسيم* عبر عده مجموعات.</span><span class="sxs-lookup"><span data-stu-id="904ce-125">You receive this error message when you try to perform a *split pick* across multiple batches.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="904ce-126">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="904ce-126">Issue resolution</span></span>

<span data-ttu-id="904ce-127">يجب ان يستخدم العامل الخاص بالمستودع عمليه *الانتقاء القصير* في تطبيق المستودع.</span><span class="sxs-lookup"><span data-stu-id="904ce-127">The warehouse worker must use the *Short picking* process in the warehouse app.</span></span> <span data-ttu-id="904ce-128">إذا كنت تحاول انتقاء مجموعات متعددة من نفس الموقع، يمكنك أيضا استخدام الخيار **كامل** في تطبيق المستودع.</span><span class="sxs-lookup"><span data-stu-id="904ce-128">If you're trying to pick multiple batches from the same location, you can also use the **Full** option in the warehouse app.</span></span>

## <a name="i-cant-move-inventory-to-a-location-that-is-license-platecontrolled"></a><span data-ttu-id="904ce-129">لا يمكن نقل المخزون إلى موقع يتم التحكم فيه بواسطة لوحه الترخيص.</span><span class="sxs-lookup"><span data-stu-id="904ce-129">I can't move inventory to a location that is license plate–controlled.</span></span>

### <a name="issue-description"></a><span data-ttu-id="904ce-130">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="904ce-130">Issue description</span></span>

<span data-ttu-id="904ce-131">لا يمكنك تقليل الكميات المنتقية في التحميل.</span><span class="sxs-lookup"><span data-stu-id="904ce-131">You can't reduce picked quantities on a load.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="904ce-132">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="904ce-132">Issue resolution</span></span>

<span data-ttu-id="904ce-133">في الإصدارات الأقدم، لا يمكنك تقليل الكميات المنتقية في التحميل.</span><span class="sxs-lookup"><span data-stu-id="904ce-133">In earlier versions, you can't reduce picked quantities on a load.</span></span> <span data-ttu-id="904ce-134">ومع ذلك ، يمكنك الآن إلغاء الانتقاء إلى لوح الترخيص الذي يتحكم فيه الموقع.</span><span class="sxs-lookup"><span data-stu-id="904ce-134">However, you can now unpick to a license plate–controlled location.</span></span> <span data-ttu-id="904ce-135">يجب تحديد كل من قيمه **الموقع** وقيمه **لوحه الترخيص** لبند التحميل في الصفحة **تقليل الكمية المنتقية**.</span><span class="sxs-lookup"><span data-stu-id="904ce-135">You must specify both a **Location** value and a **License plate** value for the load line on the **Reduce picked quantity** page.</span></span>

## <a name="can-i-print-a-delivery-note-or-packing-content-by-warehouse"></a><span data-ttu-id="904ce-136">هل يمكنني طباعه مذكرة التسليم أو محتوي التعبئة حسب المستودع؟</span><span class="sxs-lookup"><span data-stu-id="904ce-136">Can I print a delivery note or packing content by warehouse?</span></span>

### <a name="issue-description"></a><span data-ttu-id="904ce-137">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="904ce-137">Issue description</span></span>

<span data-ttu-id="904ce-138">الرغبة في طباعه مذكرة التسليم أو محتوي التعبئة حسب المستودع أو الموقع في صفحه **تحديث سطر قالب تدقيق العمل**.</span><span class="sxs-lookup"><span data-stu-id="904ce-138">You want to print a delivery note or packing content by warehouse or site on the **Work audit template line update** page.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="904ce-139">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="904ce-139">Issue resolution</span></span>

<span data-ttu-id="904ce-140">عند طباعه مستند باستخدام إعدادات أداره الطباعة ، قم بتقييد النطاق (الموقع/المستودع) من خلال أداره الطباعة بدلا من تحديد **إعدادات تحرير الطباعة** في صفحه **تحديث سطر قالب تدقيق العمل**.</span><span class="sxs-lookup"><span data-stu-id="904ce-140">When you print a document by using Print management settings, limit the scope (site/warehouse) through Print management instead of by selecting **Edit print settings** on the **Work audit template line update** page.</span></span>

## <a name="i-cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a><span data-ttu-id="904ce-141">لا يمكنني إلغاء إيصال التعبئة بعد ترحيله من أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="904ce-141">I can't cancel a packing slip after it's posted from a sales order.</span></span>

### <a name="issue-description"></a><span data-ttu-id="904ce-142">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="904ce-142">Issue description</span></span>

<span data-ttu-id="904ce-143">عند تمكين عمليات الانتقاء والشحن لـ WMS، لا يمكنك إلغاء إيصال تعبئة بعد ترحيله من أمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="904ce-143">When picking and shipping processes are enabled for WMS, you can't cancel a packing slip after it's posted from a sales order.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="904ce-144">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="904ce-144">Issue resolution</span></span>

<span data-ttu-id="904ce-145">لتصحيح إيصالات التعبئة التي تم ترحيلها للأصناف التي تم تمكينها لـ WMS، يجب القيام بالترحيل من التحميل، وليس من الأمر.</span><span class="sxs-lookup"><span data-stu-id="904ce-145">To correct posted packing slips for items that are enabled for WMS, the posting must occur from the load, not from the order.</span></span> <span data-ttu-id="904ce-146">قامت Microsoft بتقييم هذه المشكلة وقامت بتحديد انها قيد ميزه.</span><span class="sxs-lookup"><span data-stu-id="904ce-146">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="904ce-147">بشكل عام ، يمكن ان يكون أمر التوريد الذي تم انتقاؤه وشحنه خلال عمليات أداره المستودعات هو إيصال التعبئةيتم تحديثه من الحمل أو الشحن ومستند أمر المبيعات نفسه.</span><span class="sxs-lookup"><span data-stu-id="904ce-147">In general, a sales order that has been picked and shipped through warehouse management processes can be packing slip–updated from the load or shipment and the sales order document itself.</span></span> <span data-ttu-id="904ce-148">ومع ذلك ، إذا قام إيصال التعبئة بتحديث أمر المبيعات من مستند أمر المبيعات، لا يمكن اجراء إلغاء إيصال التعبئة من التحميل أو أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="904ce-148">However, if you packing slip–update the sales order from the sales order document, packing slip reversal still can't be done from the load or sales order.</span></span> <span data-ttu-id="904ce-149">التالي ، نوصي باستخدام ترحيل إيصال التعبئة من التحميل.</span><span class="sxs-lookup"><span data-stu-id="904ce-149">Therefore, we recommend that you use the packing slip posting from the load.</span></span> <span data-ttu-id="904ce-150">في هذه الحالة ، سيتم تمكين إلغاء الذي يجب القيام به من التحميل.</span><span class="sxs-lookup"><span data-stu-id="904ce-150">In this case, the reversal that must be done from the load will be enabled.</span></span>

## <a name="i-receive-the-following-error-message-not-enough-work-can-be-found-for-cluster"></a><span data-ttu-id="904ce-151">يتم عرض الرسالة التالية: "لا يمكن العثور على عمل كافي لنظام المجموعة".</span><span class="sxs-lookup"><span data-stu-id="904ce-151">I receive the following error message: "Not enough work can be found for cluster."</span></span>

### <a name="issue-description"></a><span data-ttu-id="904ce-152">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="904ce-152">Issue description</span></span>

<span data-ttu-id="904ce-153">عند استخدامك عمليه *انتقاء نظام المجموعة الموجهة بواسطة النظام*، إذا قمت بتكوين ملف تعريف لنظام مجموعه حيث يمكن انتقاء ، علي سبيل المثال ، 10 مواضع ، فان العملية تعمل كما هو مخطط له عند وجود عمل كاف لانتقاء 10 مناصب.</span><span class="sxs-lookup"><span data-stu-id="904ce-153">When you use the *System directed cluster picking* process, if you configure a cluster profile where, for example, 10 positions can be picked, the process works as planned when there is enough work to pick to 10 positions.</span></span> <span data-ttu-id="904ce-154">ومع ذلك ، إذا كان هناك ثمانيه مناصب للانتقاء فقط ، ستتلقى رسالة الخطا هذه ، لأنه لا يوجد عمل كاف لنظام مجموعه واحد.</span><span class="sxs-lookup"><span data-stu-id="904ce-154">However, if there are only eight positions to pick, you receive this error message, because there isn't enough work for one cluster.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="904ce-155">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="904ce-155">Issue resolution</span></span>

<span data-ttu-id="904ce-156">لحل هذه المشكلة ، قم بتحرير ملف تعريف المجموعة ، وقم بتعيين خيار **تنشيط المناصب** إلى *لا*.</span><span class="sxs-lookup"><span data-stu-id="904ce-156">To fix this issue, edit the cluster profile, and set the **Activate positions** option to *No*.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]