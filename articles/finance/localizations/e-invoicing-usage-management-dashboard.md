---
title: لوحة معلومات إدارة الاستخدام
description: يشرح هذا الموضوع كيفية استخدام لوحة معلومات إدارة الاستخدام لمراقبة استخدام خدمة الفوترة الإلكترونية والحفاظ على توافقها.
author: gionoder
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 411c2d33c81738dcacfb7c8feec991d0fd06fb78
ms.sourcegitcommit: 9069a8511dfe11d09a2b51d32547ba10fea48bed
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/02/2021
ms.locfileid: "6130496"
---
# <a name="usage-management-dashboard"></a><span data-ttu-id="2103c-103">لوحة معلومات إدارة الاستخدام</span><span class="sxs-lookup"><span data-stu-id="2103c-103">Usage management dashboard</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2103c-104">تساعدك **لوحة المعلومات** في مراقبة استخدام خدمة الفوترة الإلكترونية، وبالتالي تساعد مؤسستك في أن تظل متوافقة فيما يتعلق بالاستخدام الشهري.</span><span class="sxs-lookup"><span data-stu-id="2103c-104">The **Usage management** dashboard helps you monitor usage of the Electronic Invoicing service, and therefore helps your organization remain compliant in terms of its monthly usage.</span></span> <span data-ttu-id="2103c-105">يتم تحديد التوافق عن طريق حساب حجم الإرسال ومقارنته بالحجم المكتسب لعمليات الإرسال لتحديد أية انحرافات بين الحجم المكتسب والحجم المستخدم.</span><span class="sxs-lookup"><span data-stu-id="2103c-105">Compliance is determined by calculating the submission volume and comparing it with the acquired volume of submissions to identify any deviations between the acquired volume and the used volume.</span></span>

<span data-ttu-id="2103c-106">تتضمن لوحة المعلومات المؤشرات التالية:</span><span class="sxs-lookup"><span data-stu-id="2103c-106">The dashboard includes the following indicators:</span></span>

- <span data-ttu-id="2103c-107">مؤشر تكلفة واحد يمكنك استخدامه لمراقبة الاستهلاك لأغراض توافق الترخيص:</span><span class="sxs-lookup"><span data-stu-id="2103c-107">One cost indicator that you can use to monitor consumption for licensing compliance purposes:</span></span>

    - <span data-ttu-id="2103c-108">الاستخدام في الشهر (تصدير)</span><span class="sxs-lookup"><span data-stu-id="2103c-108">Usage per month (export)</span></span>

- <span data-ttu-id="2103c-109">ثلاث مؤشرات تشغيل يمكنك استخدامها لتعقب استخدام خدمة الفوترة الإلكترونية لأغراض الإدارة:</span><span class="sxs-lookup"><span data-stu-id="2103c-109">Three operational indicators that you can use to track usage of the Electronic Invoicing service for management purposes:</span></span>

    - <span data-ttu-id="2103c-110">الاستخدام حسب الميزة</span><span class="sxs-lookup"><span data-stu-id="2103c-110">Usage by feature</span></span>
    - <span data-ttu-id="2103c-111">الاستخدام حسب البيئة</span><span class="sxs-lookup"><span data-stu-id="2103c-111">Usage by environment</span></span>
    - <span data-ttu-id="2103c-112">الاستخدام في الشهر (استيراد)</span><span class="sxs-lookup"><span data-stu-id="2103c-112">Usage per month (import)</span></span>

## <a name="measurement-scope"></a><span data-ttu-id="2103c-113">نطاق القياس</span><span class="sxs-lookup"><span data-stu-id="2103c-113">Measurement scope</span></span>

- <span data-ttu-id="2103c-114">وحدة القياس:</span><span class="sxs-lookup"><span data-stu-id="2103c-114">Unit of measure:</span></span> 

    <span data-ttu-id="2103c-115">تحسب لوحة المعلومات **إدارة الاستخدام** إرسال مستندات الأعمال والفواتير الإلكترونية التي تم استيرادها.</span><span class="sxs-lookup"><span data-stu-id="2103c-115">The **Usage management** dashboard counts the submission of business documents and imported electronic invoices.</span></span>

- <span data-ttu-id="2103c-116">المؤسسة:</span><span class="sxs-lookup"><span data-stu-id="2103c-116">Organization:</span></span> 

    <span data-ttu-id="2103c-117">يتم تلخيص الجرد بواسطة معرف المستأجر الخاص بمؤسسك، بغض النظر عن عدد مثيلات Microsoft Dynamics 365 Finance أو Dynamics 365 Supply Chain Management أو عدد الكيانات القانونية التي يتم فيها تمكين خدمة الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="2103c-117">Counting is summarized by the tenant ID of your organization, regardless of the number of instances of Microsoft Dynamics 365 Finance or Dynamics 365 Supply Chain Management, or the number of legal entities where the Electronic Invoicing service is enabled.</span></span>


## <a name="indicator-usage-per-month-export"></a><span data-ttu-id="2103c-118">المؤشر: الاستخدام لكل شهر (تصدير)</span><span class="sxs-lookup"><span data-stu-id="2103c-118">Indicator: Usage per month (export)</span></span>

<span data-ttu-id="2103c-119">يوفر هذا المؤشر تفاصيل عن الفواتير الإلكترونية التي تصدرها مؤسستك خلال فترة محددة.</span><span class="sxs-lookup"><span data-stu-id="2103c-119">This indicator provides details about the electronic invoices that your organization issues during a defined period.</span></span>

### <a name="scope"></a><span data-ttu-id="2103c-120">النطاق</span><span class="sxs-lookup"><span data-stu-id="2103c-120">Scope</span></span>
- <span data-ttu-id="2103c-121">عدد مستندات الأعمال التي يتم تقديمها من Finance و Supply Chain Management إلى خدمة الفوترة الإلكترونية، بغض النظر عن عدد البنود التي تحتوي عليها مستندات الأعمال.</span><span class="sxs-lookup"><span data-stu-id="2103c-121">The number of business documents that are submitted from Finance and Supply Chain Management to the Electronic Invoicing service, regardless of number of lines that those business documents contain.</span></span>
- <span data-ttu-id="2103c-122">عدد مستندات الأعمال التي تم إرسالها والتي تمت معالجتها بنجاح بواسطة خدمة الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="2103c-122">The number of submitted business documents that are successfully processed by the Electronic Invoicing service.</span></span> <span data-ttu-id="2103c-123">ويعتبر أنه تمت معالجة المستند بنجاح عند اكتمال تدفق الإجراءات المحددة في إعداد الميزة.</span><span class="sxs-lookup"><span data-stu-id="2103c-123">A document is considered successfully processed when the flow of actions that are defined in the feature setup is completed.</span></span>

> [!NOTE]
> <span data-ttu-id="2103c-124">عند إرسال فاتورة إلكترونية إلى خدمة ويب خارجية، يكون الجرد مستقلاً عن نتائج معالجة خدمة الويب (تم قبولها أو رفضها أو خطأ التحقق من صحة مخطط).</span><span class="sxs-lookup"><span data-stu-id="2103c-124">When an electronic invoice is submitted to an external web service, counting is independent of the results of web service processing (accepted, rejected, or schema validation error).</span></span> <span data-ttu-id="2103c-125">في حالة استلام خدمة الويب والاستجابة إلى الطلب من خدمة الفوترة الإلكترونية، يعتبر التسليم جردًا صالحًا.</span><span class="sxs-lookup"><span data-stu-id="2103c-125">If the web service received and responded to the request from the Electronic Invoicing service, the submission is considered a valid counting.</span></span>

- <span data-ttu-id="2103c-126">**استثناء:** لا يتم حساب مستندات الأعمال إذا تم إعادة إرسالها من Finance و Supply Chain Management إلى خدمة الفوترة الإلكترونية، كما هو الحال في السيناريوهات التي يلزم بها إعادة التقديم لمستند الأعمال لتغيير حالة الفاتورة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="2103c-126">**Exception:** Business documents aren't counted if they are resubmitted from Finance and Supply Chain Management to the Electronic Invoicing service, such as in the scenarios where a resubmission of the same business document is required to change the status of the electronic invoice.</span></span> <span data-ttu-id="2103c-127">على سبيل المثال، يتم حساب الفاتورة الإلكترونية البرازيلية (المستند المالي) على إنها صالحة، ولكن لا يتم حساب طلب إلغائها.</span><span class="sxs-lookup"><span data-stu-id="2103c-127">For example, issuance of a Brazilian electronic invoice (fiscal document) is counted as valid, but the cancellation request for it isn't counted.</span></span>


### <a name="calculation"></a><span data-ttu-id="2103c-128">حساب</span><span class="sxs-lookup"><span data-stu-id="2103c-128">Calculation</span></span>

<span data-ttu-id="2103c-129">يتم حساب حساب الرصيد على النحو التالي:</span><span class="sxs-lookup"><span data-stu-id="2103c-129">The calculation of the balance is calculated as follows:</span></span>

<span data-ttu-id="2103c-130">الرصيد = مجاني + مشترى – مستخدم</span><span class="sxs-lookup"><span data-stu-id="2103c-130">Balance = Free + Purchased – Used</span></span>

<span data-ttu-id="2103c-131">المكان:</span><span class="sxs-lookup"><span data-stu-id="2103c-131">Where:</span></span>

- <span data-ttu-id="2103c-132">مجاني:</span><span class="sxs-lookup"><span data-stu-id="2103c-132">Free:</span></span>
  
    <span data-ttu-id="2103c-133">كمية مجانية من مستندات الأعمال التي يمكن للعميل إرسالها كل شهر.</span><span class="sxs-lookup"><span data-stu-id="2103c-133">A free volume of business documents the customer can submit per month.</span></span> <span data-ttu-id="2103c-134">ويتضمن حزمة مكونة من 100 من مستندات الأعمال يمكن إرسالها إلى خدمة الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="2103c-134">It includes a package of 100 business documents that can be submitted to the Electronic Invoicing service.</span></span> <span data-ttu-id="2103c-135">ولا تعتبر الكمية المجانية تراكمية، ولن يتم تجاوز أي رصيد متبقي إلى الفترة التالية.</span><span class="sxs-lookup"><span data-stu-id="2103c-135">Free volume isn't cumulative, and any remaining balance isn't rolled over to the next period.</span></span>
  
- <span data-ttu-id="2103c-136">المشترى:</span><span class="sxs-lookup"><span data-stu-id="2103c-136">Purchased:</span></span>
  
    <span data-ttu-id="2103c-137">حزمة مكونة من 1,000 من مستندات الأعمال يمكن إرسالها إلى خدمة الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="2103c-137">A package of 1,000 business documents that can be submitted to the Electronic Invoicing service.</span></span> <span data-ttu-id="2103c-138">يجب الحصول على هذه الحزمة لمؤسسك على أساس شهري.</span><span class="sxs-lookup"><span data-stu-id="2103c-138">This package must be acquired for your organization on a monthly basis.</span></span> <span data-ttu-id="2103c-139">ولا تعتبر كمية المشترى تراكمية، ولن يتم تجاوز أي رصيد متبقي إلى الفترة التالية.</span><span class="sxs-lookup"><span data-stu-id="2103c-139">Purchased volume isn't cumulative, and any remaining balance isn't rolled over to the next period.</span></span>
  
- <span data-ttu-id="2103c-140">مستخدم:</span><span class="sxs-lookup"><span data-stu-id="2103c-140">Used:</span></span> 

    <span data-ttu-id="2103c-141">عدد عمليات إرسال مستندات الأعمال إلى خدمة الفوترة الإلكترونية وفقًا للمعايير المحددة.</span><span class="sxs-lookup"><span data-stu-id="2103c-141">The count of business document submissions to the Electronic Invoicing service according to defined criteria.</span></span>
   
> [!IMPORTANT]
> <span data-ttu-id="2103c-142">إذا كانت المؤسسة الخاصة بك تخطط تجاوز الحجم الشهري لعمليات الإرسال المجانية التي يبلغ عددها 100، فقم بشراء الحجم للتأكد من أنك تظل متوافق مع سياسة Microsoft licensing لخدمة الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="2103c-142">If your organization plans to exceed the monthly volume of 100 free submissions, purchase the peak volume to ensure that you remain compliant with the Microsoft licensing policy for the Electronic Invoicing service.</span></span>
>
> <span data-ttu-id="2103c-143">حاليًا، يجب إدخال الحجم الذي تم شراؤه يدويًا، وفقًا لتاريخ الاستحواذ، كحزم متعددة تتضمن 1,000 عملية من عمليات الإرسال.</span><span class="sxs-lookup"><span data-stu-id="2103c-143">Currently, purchased volume must be manually entered, according to the date of acquisition, as multiple packages of 1,000 submissions.</span></span>

## <a name="indicator-usage-by-feature"></a><span data-ttu-id="2103c-144">المؤشر: الاستخدام بواسطة الميزة</span><span class="sxs-lookup"><span data-stu-id="2103c-144">Indicator: Usage by feature</span></span>

<span data-ttu-id="2103c-145">يوضح هذا المؤشر استخدام ميزات الفوترة الإلكترونية لإصدار الفواتير الإلكترونية خلال فترة محددة.</span><span class="sxs-lookup"><span data-stu-id="2103c-145">This indicator shows the usage of electronic invoicing features for issuance of electronic invoices during a defined period.</span></span>

- <span data-ttu-id="2103c-146">حساب:</span><span class="sxs-lookup"><span data-stu-id="2103c-146">Calculation:</span></span>
  
    <span data-ttu-id="2103c-147">مستخدم = عدد المرات التي تم فيها استخدام كافة ميزات الفوترة الإلكترونية أثناء إرسال مستندات الأعمال إلى خدمة الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="2103c-147">Used = The count of how many times each electronic invoicing feature was used during the submission of business documents to the Electronic Invoicing service.</span></span>

## <a name="indicator-usage-by-environment"></a><span data-ttu-id="2103c-148">المؤشر: الاستخدام بواسطة البيئة</span><span class="sxs-lookup"><span data-stu-id="2103c-148">Indicator: Usage by environment</span></span>

<span data-ttu-id="2103c-149">يعرض هذا المؤشر استخدام بيئات خدمة الفوترة الإلكترونية خلال فترة محددة.</span><span class="sxs-lookup"><span data-stu-id="2103c-149">This indicator shows the usage of electronic invoicing service environments during a defined period.</span></span>

- <span data-ttu-id="2103c-150">حساب:</span><span class="sxs-lookup"><span data-stu-id="2103c-150">Calculation:</span></span>
    
    <span data-ttu-id="2103c-151">مستخدم = عدد المرات التي تم فيها استخدام كافة بيئات خدمة الفوترة الإلكترونية أثناء إرسال مستندات الأعمال إلى خدمة الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="2103c-151">Used = The count of how many times each electronic invoicing service environment was used during the submission of business documents to the Electronic Invoicing service.</span></span>

## <a name="indicator-usage-per-month-import"></a><span data-ttu-id="2103c-152">المؤشر: الاستخدام لكل شهر (استيراد)</span><span class="sxs-lookup"><span data-stu-id="2103c-152">Indicator: Usage per month (import)</span></span>

<span data-ttu-id="2103c-153">يعرض هذا المؤشر حجم استيراد الفواتير الإلكترونية بواسطة خدمة الفوترة الإلكترونية في Finance و Supply Chain Management خلال فترة محددة.</span><span class="sxs-lookup"><span data-stu-id="2103c-153">This indicator shows the volume of importation of electronic invoices by Electronic Invoicing service into Finance and Supply Chain Management during a defined period.</span></span>

- <span data-ttu-id="2103c-154">النطاق:</span><span class="sxs-lookup"><span data-stu-id="2103c-154">Scope:</span></span>

    <span data-ttu-id="2103c-155">الفواتير الإلكترونية التي يتم استيرادها إلى Finance و Supply Chain Management، بغض النظر عن عدد البنود التي تحتويها الفواتير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="2103c-155">Electronic invoices that are imported into Finance and Supply Chain Management, regardless of the number of lines that those electronic invoices contain.</span></span>

- <span data-ttu-id="2103c-156">حساب:</span><span class="sxs-lookup"><span data-stu-id="2103c-156">Calculation:</span></span>

    <span data-ttu-id="2103c-157">مستلم = عدد الفواتير الإلكترونية المستوردة إلى Finance و Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="2103c-157">Received = The count of imported electronic invoices into Finance and Supply Chain Management.</span></span>

## <a name="functions"></a><span data-ttu-id="2103c-158">الوظائف</span><span class="sxs-lookup"><span data-stu-id="2103c-158">Functions</span></span>
### <a name="purchase"></a><span data-ttu-id="2103c-159">الشراء</span><span class="sxs-lookup"><span data-stu-id="2103c-159">Purchase</span></span>

<span data-ttu-id="2103c-160">في علامة التبويب **الاستخدام لكل شهر (تصدير)‬**، حدد **الشراء** لتسجيل عدد عمليات الإرسال التي تم الحصول عليها.</span><span class="sxs-lookup"><span data-stu-id="2103c-160">On the **Usage per month (export)** tab, select **Purchase** to manually register the amount of acquired submissions.</span></span>

<span data-ttu-id="2103c-161">بالنسبة للتاريخ المحدد، حدد **جديد** ثم أدخل عدد **الحزم** التي تم الحصول عليها في ذلك التاريخ.</span><span class="sxs-lookup"><span data-stu-id="2103c-161">For a given date, select **New** and enter the number of **Packages** acquired for on that date.</span></span>

<span data-ttu-id="2103c-162">يتم حساب **الكمية** بالصورة:</span><span class="sxs-lookup"><span data-stu-id="2103c-162">The **Quantity** is calculated as:</span></span>

<span data-ttu-id="2103c-163">الكمية = الحزم \* 1.000</span><span class="sxs-lookup"><span data-stu-id="2103c-163">Quantity = Packages \* 1.000</span></span>

<span data-ttu-id="2103c-164">تعكس **الكمية** المحسوبة في **المشترى** من المؤشر **الاستخدام لكل شهر (تصدير)‬**.</span><span class="sxs-lookup"><span data-stu-id="2103c-164">The calculated **Quantity** reflects in the **Purchased** from the indicator **Usage per month (export)**.</span></span>

### <a name="update"></a><span data-ttu-id="2103c-165">تحديث</span><span class="sxs-lookup"><span data-stu-id="2103c-165">Update</span></span>

<span data-ttu-id="2103c-166">في جزء الإجراءات، حدد **تحديث** لتحديث الحساب وتحديث البيانات المعروضة في الصفحة وفي المخطط.</span><span class="sxs-lookup"><span data-stu-id="2103c-166">On the Action Pane, select **Update** to refresh the calculation and update the data shown on the page and in the chart.</span></span>

### <a name="reset-history-data"></a><span data-ttu-id="2103c-167">إعادة تعيين بيانات المحفوظات</span><span class="sxs-lookup"><span data-stu-id="2103c-167">Reset history data</span></span>

<span data-ttu-id="2103c-168">في جزء الإجراءات، حدد **إعادة تعيين بيانات المحفوظات** لتحديث قاعدة البيانات التي يتم حساب المؤشرات منها.</span><span class="sxs-lookup"><span data-stu-id="2103c-168">On the Action Pane, select **Reset history data** to refresh the database from where the indicators are calculated.</span></span>




> [!NOTE]
> <span data-ttu-id="2103c-169">لا تعرض لوحة معلومات **إدارة الاستخدام** المبالغ النقدية.</span><span class="sxs-lookup"><span data-stu-id="2103c-169">The **Usage management** dashboard doesn't show monetary amounts.</span></span> <span data-ttu-id="2103c-170">وبدلاً من ذلك، فإنها تعرض حجم عمليات الإرسال التي تم جردها والمستندات التي تم استيرادها فقط.</span><span class="sxs-lookup"><span data-stu-id="2103c-170">Instead, it shows only the volume of counted submissions and imported documents.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
