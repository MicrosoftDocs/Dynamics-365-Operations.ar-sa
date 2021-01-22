---
title: إعادة تقييم العملة الأجنبية للحسابات الدائنة والحسابات المدينة
description: بإمكان التقلبات في أسعار الصرف أن تؤدي إلى حدوث اختلافات في القيمة النظرية (القيمة الدفترية) للحركات المفتوحة بالعملات الأجنبية بمرور الوقت. توفر هذه المقالة معلومات حول عملية إعادة تقييم العملة الأجنبية التي تقوم بتشغيلها لتحديث قيمة الحركات المفتوحة في الحسابات الدائنة والحسابات المدينة.
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustExchRateAdjustment, VendExchRateAdjustment
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14211
ms.assetid: defb1ea5-1f3e-4859-87d8-3f9954d3f388
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb7a101fa9ef84ec3873bcd8054b8198db8d58c9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188385"
---
# <a name="foreign-currency-revaluation-for-accounts-payable-and-accounts-receivable"></a><span data-ttu-id="ec94c-104">إعادة تقييم العملة الأجنبية للحسابات الدائنة والحسابات المدينة</span><span class="sxs-lookup"><span data-stu-id="ec94c-104">Foreign currency revaluation for Accounts payable and Accounts receivable</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec94c-105">بإمكان التقلبات في أسعار الصرف أن تؤدي إلى حدوث اختلافات في القيمة النظرية (القيمة الدفترية) للحركات المفتوحة بالعملات الأجنبية بمرور الوقت.</span><span class="sxs-lookup"><span data-stu-id="ec94c-105">Fluctuations in exchange rates cause the theoretical value (book value) of open transactions in foreign currencies to vary over time.</span></span> <span data-ttu-id="ec94c-106">توفر هذه المقالة معلومات حول عملية إعادة تقييم العملة الأجنبية التي تقوم بتشغيلها لتحديث قيمة الحركات المفتوحة في الحسابات الدائنة والحسابات المدينة.</span><span class="sxs-lookup"><span data-stu-id="ec94c-106">This article provides information about the foreign currency revaluation process that you run to update the value of open transactions in Accounts payable and Accounts receivable.</span></span> 

<span data-ttu-id="ec94c-107">تختلف القيمة النظرية (القيمة الدفترية) الخاصة بحركات مفتوحة بالعملات الأجنبية من وقتٍ لآخر بسبب التغييرات في سعر الصرف.</span><span class="sxs-lookup"><span data-stu-id="ec94c-107">The theoretical value, or book value, of open transactions in foreign currencies varies over time because of fluctuations in exchange rates.</span></span> <span data-ttu-id="ec94c-108">ولتحديث قيمة حركات مفتوحة في الحسابات الدائنة والحسابات المدينة، قم بتشغيل عملية إعادة تقييم العملة الأجنبية.</span><span class="sxs-lookup"><span data-stu-id="ec94c-108">To update the value of open transactions in Accounts payable and Accounts receivable, run the foreign currency revaluation process.</span></span> <span data-ttu-id="ec94c-109">ويمكن تشغيل إعادة تقييم العملة الأجنبية للحسابات الدائنة والحسابات المدينة.</span><span class="sxs-lookup"><span data-stu-id="ec94c-109">Foreign currency revaluation can be run for both Accounts payable and Accounts receivable.</span></span> <span data-ttu-id="ec94c-110">وتستخدم العملية سعر صرف جديدًا لإعادة تقييم مبالغ مفتوحة، أو لم مبالغ لم تتم تسويتها، في تاريخ محدد.</span><span class="sxs-lookup"><span data-stu-id="ec94c-110">The process uses a new exchange rate to revalue the open amounts, or not settled amounts, on a specified date.</span></span> <span data-ttu-id="ec94c-111">‏‫وستؤدي الاختلافات بين المبالغ الأصلية والمبالغ التي تمت إعادة تقييمها إلى ظهور ربح غير محقق أو خسارة لكل حركة مفتوحة.</span><span class="sxs-lookup"><span data-stu-id="ec94c-111">The differences between the original posted amounts and the revalued amounts will cause an unrealized gain or loss for each open transaction.</span></span> <span data-ttu-id="ec94c-112">ويتم فيما بعد تحديث دفاتر الأستاذ الفرعية للحسابات الدائنة والحسابات المدينة لعكس الخسائر أو الأرباح غير المحققة، ويتم ترحيل إدخال محاسبة إلى دفتر الأستاذ العام.‬</span><span class="sxs-lookup"><span data-stu-id="ec94c-112">The Accounts payable and Accounts receivable subledgers are then updated to reflect the unrealized gain or loss, and an accounting entry is posted to General ledger.</span></span>

## <a name="simulate-a-foreign-currency-revaluation"></a><span data-ttu-id="ec94c-113">محاكاة إعادة تقييم العملة الأجنبية</span><span class="sxs-lookup"><span data-stu-id="ec94c-113">Simulate a foreign currency revaluation</span></span>
<span data-ttu-id="ec94c-114">وقبل إعادة تقييم مبالغ العملات الأجنبية في الحركات المفتوحة، يمكنك تشغيل تقرير محاكاة إعادة تقييم العملة الأجنبية لنفس التاريخ والطريقة.</span><span class="sxs-lookup"><span data-stu-id="ec94c-114">Before you revalue foreign currency amounts on open transactions, you can run a simulation report of the foreign currency revaluation for the same date and method.</span></span> <span data-ttu-id="ec94c-115">ولتشغيل تقرير المحاكاة، في صفحة **إعادة تقييم العملة الأجنبية**، انقر فوق الزر **محاكاة**.</span><span class="sxs-lookup"><span data-stu-id="ec94c-115">To run the simulation report, on the **Foreign currency revaluation** page, click the **Simulation** button.</span></span> <span data-ttu-id="ec94c-116">ويوفر التقرير معاينة لمبلغ الخسارة أو الأرباح غير المحققة، استناداً إلى المعلمات التي تم تحديدها للمحاكاة.</span><span class="sxs-lookup"><span data-stu-id="ec94c-116">The report provides a preview of the unrealized gain or loss amount, based on the parameters that are defined for the simulation.</span></span>

## <a name="process-a-foreign-currency-revaluation"></a><span data-ttu-id="ec94c-117">معالجة إعادة تقييم عملة أجنبية</span><span class="sxs-lookup"><span data-stu-id="ec94c-117">Process a foreign currency revaluation</span></span>
<span data-ttu-id="ec94c-118">‏‫استخدم صفحة **إعادة تقييم العملة الأجنبية** ضمن **المهام الدورية** لإعادة تقييم الحركات المفتوحة.</span><span class="sxs-lookup"><span data-stu-id="ec94c-118">Use the **Foreign currency revaluation** page under **Periodic tasks** to revalue open transactions.</span></span> <span data-ttu-id="ec94c-119">ويمكنك تشغيل العملية في الوقت الحقيقي أو جدولتها لتشغيلها باستخدام دُفعة.</span><span class="sxs-lookup"><span data-stu-id="ec94c-119">You can run the process in real time or schedule it to run by using a batch.</span></span> <span data-ttu-id="ec94c-120">وعندما تقوم بتحديد إعدادات عملية إعادة التقييم، تأكد من التحقق من ما إذا كنت تريد طباعة تقرير بالنتائج.</span><span class="sxs-lookup"><span data-stu-id="ec94c-120">When you define the settings for the revaluation process, be sure to verify whether you want to print a report of the results.</span></span> <span data-ttu-id="ec94c-121">ولا يمكن إعادة طباعة تقرير إعادة التقييم بعد اكتمال العملية.‬</span><span class="sxs-lookup"><span data-stu-id="ec94c-121">The revaluation report can't be reprinted after the process is completed.</span></span> <span data-ttu-id="ec94c-122">وفي حالة إنشاء تقرير إعادة تقييم العملات الأجنبية، سوف تظهر مختلف الأرصدة على مستوى العميل/المورد ومستوى العملة:</span><span class="sxs-lookup"><span data-stu-id="ec94c-122">If you generate the foreign currency revaluation report, it will show various balances at the customer/vendor level and the currency level:</span></span>

-   <span data-ttu-id="ec94c-123">أرصدة العملاء أو الموردين التي تشتمل على حركات العملة الأجنبية والتي تمت إعادة تقييمها.</span><span class="sxs-lookup"><span data-stu-id="ec94c-123">The balances of customers or vendors that have foreign currency transactions that have been revalued.</span></span> <span data-ttu-id="ec94c-124">وتم توضيح الأرصدة التالية:</span><span class="sxs-lookup"><span data-stu-id="ec94c-124">The following balances are shown:</span></span>
    -   <span data-ttu-id="ec94c-125">مجموع الرصيد الأصلي بالعملة الأجنبية.</span><span class="sxs-lookup"><span data-stu-id="ec94c-125">The total original balance in the foreign currency.</span></span>
    -   <span data-ttu-id="ec94c-126">إجمالي مبلغ العملة الأجنبية ‬بعملة المحاسبة، اعتبارًا من عملية إعادة التقييم السابقة.</span><span class="sxs-lookup"><span data-stu-id="ec94c-126">The total foreign currency amount in the accounting currency, as of the previous revaluation.</span></span>
    -   <span data-ttu-id="ec94c-127">إجمالي مبلغ العملة الأجنبية ‬بعملة المحاسبة، اعتبارًا من عملية إعادة التقييم الحالية.</span><span class="sxs-lookup"><span data-stu-id="ec94c-127">The total foreign currency amount in the accounting currency, as of the current revaluation.</span></span>
    -   <span data-ttu-id="ec94c-128">الفرق بين عمليتي إعادة التقييم السابقة والحالية.</span><span class="sxs-lookup"><span data-stu-id="ec94c-128">The difference between the previous and current revaluation.</span></span> <span data-ttu-id="ec94c-129">هذا الفرق عبارة عن الخسائر أو الأرباح غير المحققة الإضافية.</span><span class="sxs-lookup"><span data-stu-id="ec94c-129">This difference is the additional unrealized gain or loss.</span></span>
-   <span data-ttu-id="ec94c-130">إجمالي الأرباح غير المحققة أو الخسارة لكل عملة.</span><span class="sxs-lookup"><span data-stu-id="ec94c-130">The total unrealized gain or loss for each currency.</span></span>

<span data-ttu-id="ec94c-131">يتم حفظ سجل في كل مرة تقوم فيها بتشغيل إعادة تقييم عمله أجنبية.</span><span class="sxs-lookup"><span data-stu-id="ec94c-131">A record is kept every time that you run a foreign currency revaluation.</span></span> <span data-ttu-id="ec94c-132">من السجل في صفحة **تقييم العملة الأجنبية**، حدد **الحركات** لعرض قائمة مفصلة من الحركات التي تم إنشاؤها بسبب إعادة التقييم.</span><span class="sxs-lookup"><span data-stu-id="ec94c-132">From the record on the **Foreign currency valuation** page, select **Transactions** to view the detailed list of transactions that were created because of the revaluation.</span></span> <span data-ttu-id="ec94c-133">‏‫وتمثل كل حركة إيصال الحركة المفتوحة التي تمت إعادة تقييمها.</span><span class="sxs-lookup"><span data-stu-id="ec94c-133">Each voucher transaction represents the open transaction that was revalued.</span></span> <span data-ttu-id="ec94c-134">وإذا تمت إعادة تقييم حركة مفتوحة أكثر من مرة، فسترى اثنين من السجلات التي تستخدم نفس الإيصال.</span><span class="sxs-lookup"><span data-stu-id="ec94c-134">If an open transaction was revalued more than one time, you will see two records that use the same voucher.</span></span> <span data-ttu-id="ec94c-135">وسيكون أحدهما لإلغاء الخسائر أو الأرباح غير المحققة، وسيكون السجل الآخر للخسائر أو الأرباح غير المحققة الجديدة.‬</span><span class="sxs-lookup"><span data-stu-id="ec94c-135">One record will be for the reversal of the previous unrealized gain or loss, and the other record will be for the new unrealized gain or loss.</span></span> <span data-ttu-id="ec94c-136">ولتشغيل عملية إعادة التقييم، انقر فوق الزر **إعادة تقييم العملة الأجنبية**.</span><span class="sxs-lookup"><span data-stu-id="ec94c-136">To run the revaluation process, click the **Foreign currency revaluation** button.</span></span> <span data-ttu-id="ec94c-137">حدد الإعدادات المناسبة للمعلمات التالية:</span><span class="sxs-lookup"><span data-stu-id="ec94c-137">Define appropriate settings for the following parameters:</span></span>

-   <span data-ttu-id="ec94c-138">**الطريقة** – الطريقة التي تم استخدامها في وظيفة إعادة تقييم العملة الأجنبية المحددة:</span><span class="sxs-lookup"><span data-stu-id="ec94c-138">**Method** – The method that is used in the selected foreign currency revaluation job:</span></span>
    -   <span data-ttu-id="ec94c-139">**قياسي** – يتم ترحيل مهام إعادة تقييم العملة الأجنبية بغض النظر عما إذا كانت النتيجة ربحًا أو خسارة.</span><span class="sxs-lookup"><span data-stu-id="ec94c-139">**Standard** – Foreign currency revaluation jobs are posted, regardless of whether the result is a profit or a loss.</span></span>
    -   <span data-ttu-id="ec94c-140">**الحد الأدنى** – يتم ترحيل مهام إعادة تقييم العملة الأجنبية فقط إذا كانت النتيجة خسارة.</span><span class="sxs-lookup"><span data-stu-id="ec94c-140">**Minimum** – Foreign currency revaluation jobs are posted only if the result is a loss.</span></span>
    -   <span data-ttu-id="ec94c-141">**تاريخ الفاتورة** – تستخدم مهام إعادة تقييم العملة الأجنبية سعر صرف الحركات، الذي يتم إعادة تقييمه إلى قيمته الأصلية بعملة المحاسبة.</span><span class="sxs-lookup"><span data-stu-id="ec94c-141">**Invoice date** – Foreign currency revaluation jobs use the original exchange rate of the transactions, which are revalued to their original value in the accounting currency.</span></span> <span data-ttu-id="ec94c-142">يتم إلغاء تأثير أي عملية إعادة تقييم سابقة للعملة الأجنبية.</span><span class="sxs-lookup"><span data-stu-id="ec94c-142">The effect of any prior foreign currency revaluation is canceled.</span></span>
-   <span data-ttu-id="ec94c-143">**التاريخ المحدد** – التاريخ الذي يُعثر فيه على كل الحركات التي قمت بفتح مبالغ لها (لم تقم بالتسوية) في ذلك التاريخ.</span><span class="sxs-lookup"><span data-stu-id="ec94c-143">**Considered date** – The date when all transactions that have open (not settled) amounts on that date are found.</span></span> <span data-ttu-id="ec94c-144">يُعاد تقييم مبالغ العملات الأجنبية باستخدام أسعار الصرف التي تم إدخالها في صفحة **أسعار صرف العملة الأجنبية** للتاريخ المحدد.</span><span class="sxs-lookup"><span data-stu-id="ec94c-144">Foreign currency amounts are revalued by using the exchange rates that are entered on the **Currency exchange rates** page for the considered date.</span></span> <span data-ttu-id="ec94c-145">وعندما يُعاد تقييم مبالغ العملات الأجنبية في تاريخ محدد، يصبح هذا التاريخ هو آخر تاريخ لإعادة تقييم العملة الأجنبية للحركات التي تم تعديلها.</span><span class="sxs-lookup"><span data-stu-id="ec94c-145">When foreign currency amounts are revalued on a considered date, this date becomes the last foreign currency revaluation date for the transactions that are adjusted.</span></span> <span data-ttu-id="ec94c-146">وإذا أجريت إعادة تقييم عملة أجنبية لتاريخ اعتباري يسبق التاريخ الأخير لإعادة تقييم العملة الأجنبية في الحركات التي تمت تسويتها بالفعل، لا تتم تسوية الحركات المفتوحة في التاريخ الاعتباري السابق وإنما تتم تسوية الحركات التي لها تاريخ أحدث لإعادة تقييم العملة الأجنبية بواسطة الوظيفة الدورية.</span><span class="sxs-lookup"><span data-stu-id="ec94c-146">If you run foreign currency revaluation for a considered date that is earlier than the last foreign currency revaluation date on transactions that have already been adjusted, the periodic job doesn't adjust transactions that are open on the earlier considered date, but that have a more recent last foreign currency revaluation date.</span></span>
-   <span data-ttu-id="ec94c-147">**تاريخ السعر** – التاريخ الذي يحدد سعر الصرف الذي يتم استخدامه في حركة إعادة تقييم العملة الأجنبية.</span><span class="sxs-lookup"><span data-stu-id="ec94c-147">**Date of rate** – The date that determines the exchange rate that is used in the foreign currency revaluation.</span></span>
-   <span data-ttu-id="ec94c-148">**استخدام ملف تعريف الترحيل من** – ملف تعريف الترحيل المستخدم لإدخال الحساب الأساسي الافتراضي للحسابات المدينة أو الحسابات الدائنة للقيود المحاسبية لحركات إعادة تقييم العملة الأجنبية:</span><span class="sxs-lookup"><span data-stu-id="ec94c-148">**Use posting profile from** – The posting profile that is used to enter the default main account for Accounts receivable or Accounts payable for the accounting entries of the  foreign currency revaluation transactions:</span></span>
    -   <span data-ttu-id="ec94c-149">**الترحيل** – يتم استخدام ملف تعريف الترحيل الخاص بحركة العميل.</span><span class="sxs-lookup"><span data-stu-id="ec94c-149">**Posting** – The posting profile of the customer transaction is used.</span></span>
    -   <span data-ttu-id="ec94c-150">**تحديد** – أدخل ملف تعريف الترحيل في حقل**ملف تعريف الترحيل**.</span><span class="sxs-lookup"><span data-stu-id="ec94c-150">**Select** – Enter the posting profile in the **Posting profile** field.</span></span>
-   <span data-ttu-id="ec94c-151">**ملف تعريف الترحيل** – في حالة تحديد **تحديد** في حقل **استخدام ملف تعريف الترحيل من**، يحدد ملف تعريف الترحيل الذي تقوم بإدخاله في الحقل ملف تعريف الترحيل الخاص بحركات إعادة تقييم العملة الأجنبية.</span><span class="sxs-lookup"><span data-stu-id="ec94c-151">**Posting profile** – If **Select** is selected in the **Use posting profile from** field, the posting profile that you enter in this field determines the posting profile of the foreign currency revaluation transactions.</span></span>
-   <span data-ttu-id="ec94c-152">**الأبعاد المالية** – الأبعاد المالية التي يتم ترحيلها في الإدخالات المحاسبية لحركات إعادة تقييم العملة الأجنبية:</span><span class="sxs-lookup"><span data-stu-id="ec94c-152">**Financial dimensions** – The financial dimensions that are posted on the accounting entries of the foreign currency revaluation transactions:</span></span>
    -   <span data-ttu-id="ec94c-153">**لا شيء** – لا يتم ترحيل أي أبعاد مالية.</span><span class="sxs-lookup"><span data-stu-id="ec94c-153">**None** – No financial dimensions are posted.</span></span> <span data-ttu-id="ec94c-154">إذا كان لديك بعد مالي مطلوب في بنية الحساب الخاص بك، لا تزال تعمل عملية إعادة التقييم وتقوم بإنشاء الإدخالات المحاسبية التي لا تشتمل على أي أبعاد مالية.</span><span class="sxs-lookup"><span data-stu-id="ec94c-154">If you have a required financial dimension in your account structure, the revaluation process is still run and creates accounting entries that have no financial dimensions.</span></span> <span data-ttu-id="ec94c-155">سوف تتلقى رسالة تحذير أولاً، بحيث يمكنك إلغاء إعادة التقييم.</span><span class="sxs-lookup"><span data-stu-id="ec94c-155">You will receive a warning message first, so that you can cancel the revaluation.</span></span>
    -   <span data-ttu-id="ec94c-156">**الجدول** – يتم ترحيل الأبعاد المالية لحساب العميل أو حساب المورد في حركات إعادة تقييم العملة الأجنبية.</span><span class="sxs-lookup"><span data-stu-id="ec94c-156">**Table** – The financial dimensions of the customer account or vendor account are posted on the foreign currency revaluation transactions.</span></span>
    -   <span data-ttu-id="ec94c-157">**الترحيل** – يتم ترحيل الأبعاد المالية للحركة التي تتم إعادة تقييمها في حركات إعادة تقييم العملة الأجنبية.</span><span class="sxs-lookup"><span data-stu-id="ec94c-157">**Posting** – The financial dimensions of the transaction that is being revalued are posted on the foreign currency revaluation transactions.</span></span> <span data-ttu-id="ec94c-158">بشكل افتراضي، سيتم استخدام الأبعاد المالية من حساب دفتر أستاذ الحسابات المدينة/الحسابات الدائنة للحركة الأصلية للحساب الرئيسي للحسابات المدينة/الحسابات الدائنة لحركة إعادة التقييم، وسيتم استخدام الأبعاد المالية من حساب دفتر أستاذ مصروفات/أصول/إيرادات الحركة الأصلية للحساب الرئيسي للخسائر/الأرباح غير المحققة لحركة إعادة التقييم.</span><span class="sxs-lookup"><span data-stu-id="ec94c-158">By default, the financial dimensions from the original transaction's AR/AP ledger account will be used for the revaluation transaction's AR/AP main account, and the financial dimensions from the original transaction's expense/asset/revenue ledger account will be used for the revaluation transaction's unrealized gain/loss main account.</span></span>



