---
title: مدقق تناسق حركة البيع بالتجزئة
description: يصف هذا الموضوع وظيفة مدقق تناسق الحركة في Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 3da8bdf6feb932e074680b6cb80e1b7b71f9a82b
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004241"
---
# <a name="retail-transaction-consistency-checker"></a><span data-ttu-id="6f584-103">مدقق تناسق حركة البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="6f584-103">Retail transaction consistency checker</span></span>


[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

<span data-ttu-id="6f584-104">يصف هذا الموضوع وظيفة مدقق تناسق الحركة في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6f584-104">This topic describes the transaction consistency checker functionality in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="6f584-105">يحدد مدقق التناسق الحركات غير المتناسقة ويعزلها قبل انتقائها من قبل عملية ترحيل كشف الحساب.</span><span class="sxs-lookup"><span data-stu-id="6f584-105">The consistency checker identifies and isolates inconsistent transactions before they are picked up by the statement posting process.</span></span>

<span data-ttu-id="6f584-106">عند ترحيل كشف حساب، قد يفشل الترحيل بسبب وجود بيانات غير متناسقة في جداول حركات التجارة.</span><span class="sxs-lookup"><span data-stu-id="6f584-106">When a statement is posted, posting can fail due to inconsistent data in the commerce transaction tables.</span></span> <span data-ttu-id="6f584-107">قد يعود سبب المشكلة في البيانات إلى ظهور مشاكل غير متوقعة في تطبيق نقطة البيع (POS)، أو إذا تم استيراد الحركات بشكل غير صحيح من أنظمة نقطة البيع الخارجية.</span><span class="sxs-lookup"><span data-stu-id="6f584-107">The data issue may be caused by unforeseen issues in the point of sale (POS) application, or if transactions were incorrectly imported from third-party POS systems.</span></span> <span data-ttu-id="6f584-108">تشتمل الأمثلة حول كيفية ظهور حالات عدم التناسق هذه على ما يلي:</span><span class="sxs-lookup"><span data-stu-id="6f584-108">Examples of how these inconsistencies may appear include:</span></span> 

- <span data-ttu-id="6f584-109">إجمالي الحركة في جدول الرأس غير متطابق مع إجمالي الحركة في البنود.</span><span class="sxs-lookup"><span data-stu-id="6f584-109">The transaction total on the header table does not match the transaction total on the lines.</span></span>
- <span data-ttu-id="6f584-110">عدد البنود في جدول الرأس غير متطابق مع عدد البنود في جدول الحركة.</span><span class="sxs-lookup"><span data-stu-id="6f584-110">The line count on the header table does not match with the number of lines in the transaction table.</span></span>
- <span data-ttu-id="6f584-111">الضرائب في جدول الرأس غير متطابقة مع قيمة الضريبة في البنود.</span><span class="sxs-lookup"><span data-stu-id="6f584-111">Taxes on the header table do not match the tax amount on the lines.</span></span> 

<span data-ttu-id="6f584-112">عندما تنتقي عمليات ترحيل كشوف الحسابات حركات غير متناسقة، يتم إنشاء دفاتر يومية دفعات وفواتير مبيعات غير متناسقة، وتفشل عملية ترحيل كشف الحساب بكاملها نتيجة لذلك.</span><span class="sxs-lookup"><span data-stu-id="6f584-112">When inconsistent transactions are picked up by the statement posting process, inconsistent sales invoices and payment journals are created, and the entire statement posting process fails as a result.</span></span> <span data-ttu-id="6f584-113">تشتمل عملية استرداد كشوف الحسابات من حالة من هذا النوع على عمليات إصلاح معقدة للبيانات عبر جداول حركات متعددة.</span><span class="sxs-lookup"><span data-stu-id="6f584-113">Recovering the statements from such a state involves complex data fixes across multiple transaction tables.</span></span> <span data-ttu-id="6f584-114">يمنع مدقق تناسق الحركة حدوث مثل هذه المشاكل.</span><span class="sxs-lookup"><span data-stu-id="6f584-114">The transaction consistency checker prevents such issues.</span></span>

<span data-ttu-id="6f584-115">يوضح المخطط التالي عملية الترحيل باستخدام مدقق تناسق الحركة.</span><span class="sxs-lookup"><span data-stu-id="6f584-115">The following chart illustrates the posting process with the transaction consistency checker.</span></span>

<span data-ttu-id="6f584-116">![عمليه ترحيل كشف الحساب مع مدقق تناسق الحركة](./media/validchecker.png "عمليه ترحيل كشف الحساب مع مدقق تناسق حركة البيع بالتجزئة")</span><span class="sxs-lookup"><span data-stu-id="6f584-116">![Statement posting process with transaction consistency checker](./media/validchecker.png "Statement posting process with retail transaction consistency checker")</span></span>

<span data-ttu-id="6f584-117">تدقق العملية الدُفعية **التحقق من صحة الحركات** في تناسق جداول حركات التجارة للسيناريوهات التالية.</span><span class="sxs-lookup"><span data-stu-id="6f584-117">The **Validate store transactions** batch process checks the consistency of the commerce transaction tables for the following scenarios.</span></span>

- <span data-ttu-id="6f584-118">**حساب العميل** – التأكد من أن حساب العميل في جداول الحركات موجود في المقر الرئيسي للعميل.</span><span class="sxs-lookup"><span data-stu-id="6f584-118">**Customer account** – Validates that the customer account in the transaction tables exists in the HQ customer master.</span></span>
- <span data-ttu-id="6f584-119">**عدد البنود** – التأكد من أن عدد البنود، كما تم تسجيله في جدول رأس الحركة، يتطابق مع أرقام البنود في جداول حركة مبيعات.</span><span class="sxs-lookup"><span data-stu-id="6f584-119">**Line count** – Validates that the number of lines, as captured on the transaction header table, matches the number of lines in the sales transaction tables.</span></span>
- <span data-ttu-id="6f584-120">**السعر يشمل الضريبة** – التأكد من أن المعلمة **السعر يشمل الضريبة** متناسقة عبر بنود الحركة.</span><span class="sxs-lookup"><span data-stu-id="6f584-120">**Price includes tax** – Validates that the **Price includes tax** parameter is consistent across transaction lines.</span></span>
- <span data-ttu-id="6f584-121">**مبلغ الدفع** - يتحقق من مطابقة سجلات الدفع مع مبلغ الدفع في الرأس.</span><span class="sxs-lookup"><span data-stu-id="6f584-121">**Payment amount** - Validates that the payment records match the payment amount on header.</span></span>
- <span data-ttu-id="6f584-122">**إجمالي المبلغ** – التأكد من ان إجمالي المبلغ في الرأس هو مجموع المبالغ الصافية الموجودة في البنود بالإضافة إلى مبلغ الضريبة.</span><span class="sxs-lookup"><span data-stu-id="6f584-122">**Gross amount** – Validates that the gross amount on the header is the sum of the net amounts on the lines plus the tax amount.</span></span>
- <span data-ttu-id="6f584-123">**المبلع الصافي** – التأكد من ان المبلغ الصافي‏‎ في الرأس هو مجموع المبالغ الصافية الموجودة في البنود بالإضافة إلى مبلغ الضريبة.</span><span class="sxs-lookup"><span data-stu-id="6f584-123">**Net amount** – Validates that the net amount on the header is the sum of the net amounts on the lines.</span></span>
- <span data-ttu-id="6f584-124">**دفع بالزيادة/بالنقصان‬** – التأكد من أن الفرق بين إجمالي المبلغ على الرأس ومبلغ الدفع لا يتجاوز تكوين دفع بالزيادة/بالنقصان.</span><span class="sxs-lookup"><span data-stu-id="6f584-124">**Under / Over payment** – Validates that the difference between the gross amount on the header and the payment amount doesn't exceed the maximum underpayment/overpayment configuration.</span></span>
- <span data-ttu-id="6f584-125">**مبلغ الخصم** – التأكد من تناسق مبلغ الخصم في جداول الخصم ومبلغ الخصم في جداول بنود الحركة، وأن مبلغ الخصم في الرأس هو مجموع مبالغ الخصم في البنود.</span><span class="sxs-lookup"><span data-stu-id="6f584-125">**Discount amount** – Validates that the discount amount on the discount tables and the discount amount on the transaction line tables are consistent, and that the discount amount on the header is the sum of the discount amounts on the lines.</span></span>
- <span data-ttu-id="6f584-126">**خصم البند** – التأكد من أن خصم البند على بند الحركة هو مجموع كافة البنود في جدول الخصم الذي يتوافق مع بند الحركة.</span><span class="sxs-lookup"><span data-stu-id="6f584-126">**Line discount** – Validates that the line discount on the transaction line is the sum of all the lines in the discount table that corresponds to the transaction line.</span></span>
- <span data-ttu-id="6f584-127">**صنف بطاقة الهدايا‬** – لا يدعم Commerce إرجاع أصناف بطاقة الهدايا.</span><span class="sxs-lookup"><span data-stu-id="6f584-127">**Gift card item** – Commerce doesn't support the return of gift card items.</span></span> <span data-ttu-id="6f584-128">ومع ذلك، يمكن صرف الرصيد في بطاقة الهدايا. عند معالجة صنف بطاقة هدايا كبند مرتجع بدلاً من بند مصروف، فهو يفشل في عملية ترحيل كشوف الحسابات.</span><span class="sxs-lookup"><span data-stu-id="6f584-128">However, the balance on a gift card can be cashed out. Any gift card item that is processed as a return line instead of a cash-out line fails the statement posting process.</span></span> <span data-ttu-id="6f584-129">تضمن عملية التحقق من الصحة التي تتم على أصناف بطاقة الهدايا أن تكون فقط عناصر بنود بطاقة الهدايا المرتجعة على جداول الحركات هي البنود المصروفة في بطاقة الهدايا.</span><span class="sxs-lookup"><span data-stu-id="6f584-129">The validation process for gift card items helps guarantee that the only return gift card line items on the transaction tables are gift card cash-out lines.</span></span>
- <span data-ttu-id="6f584-130">**السعر السالب** – يتحقق من عدم وجود بنود حركة ذات سعر سالب.</span><span class="sxs-lookup"><span data-stu-id="6f584-130">**Negative price** – Validates that there are no negative price transaction lines.</span></span>
- <span data-ttu-id="6f584-131">**الصنف والمتغير** – التأكد من أن الأصناف والمتغيرات في بنود الحركة موجودة في الملف الرئيسي للصنف والمتغير.</span><span class="sxs-lookup"><span data-stu-id="6f584-131">**Item & Variant** – Validates that items and variants on the transaction lines exist in the item and variant master file.</span></span>
- <span data-ttu-id="6f584-132">**مبلغ الضريبة** - التحقق من مطابقة سجلات الضريبة‏‎ مع مبالغ الضريبة على البنود.</span><span class="sxs-lookup"><span data-stu-id="6f584-132">**Tax amount** - Validates that tax records match the tax amounts on the lines.</span></span>
- <span data-ttu-id="6f584-133">**الرقم التسلسلي** - التحقق من وجود الرقم التسلسلي في بنود الحركة للأصناف التي يتم التحكم فيها بواسطة الرقم التسلسلي.</span><span class="sxs-lookup"><span data-stu-id="6f584-133">**Serial number** - Validates that the serial number is present in the transaction lines for items that are controlled by serial number.</span></span>
- <span data-ttu-id="6f584-134">**علامة‬** - التحقق من أن العلامة على الكمية وصافي المبلغ هي نفسها في جميع بنود الحركة.</span><span class="sxs-lookup"><span data-stu-id="6f584-134">**Sign** - Validates that the sign on the quantity and the net amount are the same in all the transaction lines.</span></span>
- <span data-ttu-id="6f584-135">**تاريخ العمل** - التحقق من أن الفترات المالية لجميع تواريخ العمل الخاصة بالحركات مفتوحة.</span><span class="sxs-lookup"><span data-stu-id="6f584-135">**Business date** - Validates that the financial periods for all the business dates for the transactions are open.</span></span>

## <a name="set-up-the-consistency-checker"></a><span data-ttu-id="6f584-136">إعداد مدقق التناسق</span><span class="sxs-lookup"><span data-stu-id="6f584-136">Set up the consistency checker</span></span>

<span data-ttu-id="6f584-137">قم بتكوين العملية الدُفعية "التحقق من صحة حركات المتجر‬" في **Retail and Commerce \> تكنولوجيا معلومات Retail and Commerce \> ترحيل نقطة البيع**، لعمليات التشغيل الدورية.</span><span class="sxs-lookup"><span data-stu-id="6f584-137">Configure the "Validate store transactions" batch process, at **Retail and Commerce \> Retail and Commerce IT \> POS posting**, for periodic runs.</span></span> <span data-ttu-id="6f584-138">يمكن جدولة الوظيفة الدُفعية استنادًا إلى التدرج الهرمي للمؤسسات في المتجر، بطريقة مماثلة لكيفية إعداد العمليتين "حساب الكشوف على دُفعات‬" و"ترحيل الكشوف على دُفعات‬".</span><span class="sxs-lookup"><span data-stu-id="6f584-138">The batch job can be scheduled based on store organization hierarchy, similar to how the "Calculate statement in batch" and "Post statement in batch" processes are set up.</span></span> <span data-ttu-id="6f584-139">من المستحسن تكوين هذه العملية الدُفعية لتشغيلها عدة مرات في اليوم وجدولتها بحيث يتم تشغيلها في نهاية كل تنفيذ لوظيفة P.</span><span class="sxs-lookup"><span data-stu-id="6f584-139">We recommend that you configure this batch process to run multiple times in a day and schedule it so that it runs at the end of every P-job execution.</span></span>

## <a name="results-of-validation-process"></a><span data-ttu-id="6f584-140">نتائج التحقق من الصحة</span><span class="sxs-lookup"><span data-stu-id="6f584-140">Results of validation process</span></span>

<span data-ttu-id="6f584-141">توضع علامة نتائج التحقق من الصحة التي تقوم بها العملية الدُفعية على الحركة المناسبة.</span><span class="sxs-lookup"><span data-stu-id="6f584-141">The results of the validation check by the batch process are tagged on the appropriate transaction.</span></span> <span data-ttu-id="6f584-142">يكون الحقل **حالة التحقق من الصحة** على سجل الحركة معينًا إلى **ناجح‬** أو **خطأ**، ويظهر تاريخ تشغيل عملية التحقق من الصحة الأخيرة في الحقل **وقت آخر عملية تحقق من الصحة**.</span><span class="sxs-lookup"><span data-stu-id="6f584-142">The **Validation status** field on the transaction record is either set to **Successful** or **Error**, and the date of the last validation run appears on the **Last validation time** field.</span></span>

<span data-ttu-id="6f584-143">لعرض نص وصفي للخطأ المتعلق بفشل التحقق من الصحة، حدد سجل حركة المتجر الملائم، ثم انقر فوق الزر **أخطاء التحقق من الصحة**.</span><span class="sxs-lookup"><span data-stu-id="6f584-143">To view more descriptive error text relating to a validation failure, select the relevant store transaction record and click the **Validation errors** button.</span></span>

<span data-ttu-id="6f584-144">لن تتضمن كشوف الحسابات الحركات التي لم تنجح في عملية التحقق من الصحة والحركات التي لم يتم بعد التحقق من صحتها.</span><span class="sxs-lookup"><span data-stu-id="6f584-144">Transactions that fail the validation check and transactions that have not yet been validated will not be pulled into statements.</span></span> <span data-ttu-id="6f584-145">أثناء عملية "حساب كشف الحساب"، سيتم يتم إبلاغ المستخدمين عن وجود حركات كان يجب تضمينها في كشف الحساب ولكن لم يتم تضمينها فيه.</span><span class="sxs-lookup"><span data-stu-id="6f584-145">During the "Calculate statement" process, users will be notified if there are transactions that could have been included in the statement but weren't.</span></span>

<span data-ttu-id="6f584-146">إذا تم العثور على خطأ يتعلق بالتحقق من الصحة، فإن الطريقة الوحيدة لإصلاحه هو الاتصال بدعم Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6f584-146">If a validation error is found, the only way to fix the error is to contact Microsoft Support.</span></span> <span data-ttu-id="6f584-147">في إصدار مستقبلي، سنضيف ميزة تسمح للمستخدمين بإصلاح السجلات التي فشلت عبر واجهة المستخدم.</span><span class="sxs-lookup"><span data-stu-id="6f584-147">In a future release, capability will be added so that users can fix the records that failed through the user interface.</span></span> <span data-ttu-id="6f584-148">وسنوفر أيضًا قدرات التسجيل والتدقيق لتتبع محفوظات التعديلات.</span><span class="sxs-lookup"><span data-stu-id="6f584-148">Logging and auditing capabilities will also be made available to trace the history of the modifications.</span></span>

> [!NOTE]
> <span data-ttu-id="6f584-149">سنضيف المزيد من قواعد التحقق من الصحة لدعم سيناريوهات إضافية في إصدار مستقبلي.</span><span class="sxs-lookup"><span data-stu-id="6f584-149">Additional validation rules to support more scenarios will be added in a future release.</span></span>
