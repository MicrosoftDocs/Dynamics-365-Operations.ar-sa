---
title: إقفال السنة المالية
description: ينقلك هذا الإجراء عبر عملية إقفال نهاية السنة التي تحول الأرصدة إلى سنة مالية جديدة.
author: aprilolson
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, LedgerFiscalCloseGroup, LedgerFiscalCloseAddLedger, SysLookupMultiSelectGrid, LedgerFiscalCloseRunGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 593ab5b45cc0c2e1a8b876aa89de014fd9df1a13
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3137936"
---
# <a name="close-the-fiscal-year"></a><span data-ttu-id="4e6e5-103">إقفال السنة المالية</span><span class="sxs-lookup"><span data-stu-id="4e6e5-103">Close the fiscal year</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4e6e5-104">ينقلك هذا الإجراء عبر عملية إقفال نهاية السنة التي تحول الأرصدة إلى سنة مالية جديدة.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-104">This procedure steps through the year end close process that transfers balances to a new fiscal year.</span></span>


## <a name="validate-year-end-close-parameters"></a><span data-ttu-id="4e6e5-105">التحقق من صحة محددات إقفال نهاية السنة</span><span class="sxs-lookup"><span data-stu-id="4e6e5-105">Validate year-end close parameters</span></span>
1. <span data-ttu-id="4e6e5-106">انتقل إلى **جزء التنقل > الوحدات النمطية > دفتر الأستاذ العام > إعداد دفتر الأستاذ > محددات دفتر الأستاذ العام‬**.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-106">Go to **Navigation pane > Modules > General ledger > Ledger setup > General ledger parameters**.</span></span>
2. <span data-ttu-id="4e6e5-107">قم بتوسيع مقطع **إقفال نهاية السنة**.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-107">Expand the **Fiscal year close** section.</span></span>
3. <span data-ttu-id="4e6e5-108">حدد "نعم" أو "لا" للخيار **حذف حركات الإقفال السنوية أثناء التحويل**.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-108">Select 'Yes' or 'No' for the **Delete close-of-year transactions during transfer** option.</span></span>
    
    <span data-ttu-id="4e6e5-109">إذا تم بالفعل إقفال السنة المالية ويجري تشغيل إقفال نهاية السنة مرة أخرى، فإن هذا الإعداد يُعد مهمًا.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-109">If the fiscal year has already been closed and the year-end close is being run again, this setting is important.</span></span> <span data-ttu-id="4e6e5-110">إذا تم تعيين الخيار إلى "نعم"، فسيتم حذف الإيصال الخاص بإقفال نهاية السنة الماضية، وسيتم إنشاء إيصال جديد لكل الأرصدة الأولية للحسابات.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-110">If set to Yes, the voucher for the previous year-end close will be deleted, and a new voucher will be created for all accounts beginning balances.</span></span> <span data-ttu-id="4e6e5-111">أما إذا تم تعيينه إلى "لا"، فإن الإيصال السابق سوف يبقى وسيتم إنشاء إيصال جديد فقط لتسوية الإدخالات التي تم ترحيلها بعد إقفال نهاية السنة الماضية.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-111">If set to No, the previous voucher will remain and a new voucher will only be created for adjusting entries that were posted after the last year-end close.</span></span>

4. <span data-ttu-id="4e6e5-112">حدد "نعم" أو "لا" للخيار **إنشاء حركات إقفال أثناء التحويل**.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-112">Select 'Yes' or 'No' for the **Create closing transactions during transfer** option.</span></span>

    <span data-ttu-id="4e6e5-113">إذا تم تعيين الخيار إلى "نعم"، فسيتم إنشاء حركتين.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-113">If set to Yes, two transactions are created.</span></span> <span data-ttu-id="4e6e5-114">يتم إنشاء إيصال واحد في السنة المالية الجاري إقفالها لكي تصبح أرصدة حسابات دفتر الأستاذ للأرباح والخسائر بقيمة صفر، ويتم إنشاء إيصال ثانٍ في السنة المالية التالية للأرصدة الأولية.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-114">One voucher is created in the fiscal year being closed to bring the balances of the P&L ledger accounts down to zero and a second voucher is created in the next fiscal year for the beginning balances.</span></span> <span data-ttu-id="4e6e5-115">أما إذا تم تعيين الخيار إلى "لا"، فسيتم إنشاء إيصال واحد في السنة المالية التالية للأرصدة الأولية.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-115">If set to No, a single voucher is created in the next fiscal year for the beginning balances.</span></span>  

5. <span data-ttu-id="4e6e5-116">حدد "نعم" أو "لا" للخيار **تعيين حالة السنة المالية إلى مقفلة بشكل دائم‬**.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-116">Select 'Yes' or 'No' for the **Set fiscal year status to permanently closed** option.</span></span>

    <span data-ttu-id="4e6e5-117">إذا تم تعيين الخيار إلى "نعم"، فسيتم تعيين حالة السنة المالية إلى "تم الإقفال بشكل دائم‬".</span><span class="sxs-lookup"><span data-stu-id="4e6e5-117">If set to Yes, the fiscal year status will be set to Permanently closed.</span></span>  <span data-ttu-id="4e6e5-118">ونظرًا لتعذر إعادة فتح سنة مقفلة بشكل دائم، فمن المستحسن تعيين هذا الخيار إلى "لا".</span><span class="sxs-lookup"><span data-stu-id="4e6e5-118">Because a permanently closed year cannot be reopened, it would be a best practice to set this option to No.</span></span>  

6. <span data-ttu-id="4e6e5-119">حدد "نعم" أو "لا" للخيار **ما إذا كان يجب إدخال رقم إيصال أثناء عملية إقفال نهاية السنة**.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-119">Select 'Yes' or 'No' for the **Voucher number must be filled in during the year end close** option.</span></span>

    <span data-ttu-id="4e6e5-120">إذا تم تعيين هذا الخيار إلى "نعم"، فيجب إدخال رقم إيصال يدويًا أثناء عملية إقفال نهاية السنة.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-120">If set to Yes, a voucher number must be manually entered during the year end close process.</span></span> <span data-ttu-id="4e6e5-121">لا يستخدم تسلسل الرقمي لإنشاء رقم الإيصال هذا.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-121">A number sequence is not used to generate this voucher number.</span></span> <span data-ttu-id="4e6e5-122">من المستحسن تعيين هذا الخيار إلى "نعم".</span><span class="sxs-lookup"><span data-stu-id="4e6e5-122">It's a best practice to set this to Yes.</span></span>  

7. <span data-ttu-id="4e6e5-123">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-123">Close the page.</span></span>
8. <span data-ttu-id="4e6e5-124">انتقل إلى **دفتر الأستاذ العام > إقفال الفترة > إقفال نهاية السنة**.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-124">Go to **General ledger > Period close > Year end close**.</span></span>
9. <span data-ttu-id="4e6e5-125">انقر فوق **جديد** لإنشاء قالب إقفال نهاية السنة.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-125">Click **New** to create a year-end close template.</span></span>

    <span data-ttu-id="4e6e5-126">يمكن إنشاء قالب لمجموعة من الكيانات القانونية لتشغيل إقفال نهاية السنة لها.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-126">A template can be created for a group of legal entities for which to run the year-end close.</span></span> <span data-ttu-id="4e6e5-127">يمكنك إعادة استخدام هذا القالب سنة بعد سنة.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-127">This template can be reused year after year.</span></span>  

10. <span data-ttu-id="4e6e5-128">في الحقل **اسم المجموعة**، أدخل اسمًا لقالب إقفال نهاية السنة.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-128">In the **Group name** field, enter a year-end close template name..</span></span>
11. <span data-ttu-id="4e6e5-129">في حقل **التقويم المالي**، حدد السنة المالية التي سيتم إنشاء القالب لها.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-129">In the **Fiscal calendar** field, select the fiscal year for which the template will be created.</span></span>

    <span data-ttu-id="4e6e5-130">يمكن تجميع معًا فقط الكيانات القانونية التي تستخدم السنة المالية نفسها في قالب إقفال نهاية السنة.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-130">Only legal entities which use the same fiscal year can be grouped together in the year-end close template.</span></span> <span data-ttu-id="4e6e5-131">وهذا لأن تنفيذ إقفال نهاية السنة يتم عن طريق تحديد سنة مالية، وليس تاريخ.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-131">This is because the year end close is done by selecting a fiscal year, not a date.</span></span>  

12. <span data-ttu-id="4e6e5-132">في **جزء الإجراءات**، انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-132">On the **Action pane**, click **Save**.</span></span>
13. <span data-ttu-id="4e6e5-133">في قسم **الكيانات القانونية**، انقر فوق **إضافة‏‎** لتحديد الكيانات القانونية لهذا القالب.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-133">In the **Legal entities** section, click **Add** to select the legal entities for this template.</span></span>
    
    <span data-ttu-id="4e6e5-134">يمكن إضافة الكيانات القانونية إما بتحديد الكيانات القانونية أو بتحديد تدرج هرمي تنظيمي.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-134">Legal entities can be added by either selecting the legal entities or by selecting an organizational hierarchy.</span></span>  <span data-ttu-id="4e6e5-135">ستُضاف فقط الكيانات القانونية مع التدرج الهرمي التنظيمي حيث تم تحديد تقويم السنة المالية نفسها.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-135">Only legal entities with the organizational hierarchy with the same fiscal calendar selected will be added.</span></span>  

14. <span data-ttu-id="4e6e5-136">حدد الكيانات القانونية أو التدرج الهرمي التنظيمي.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-136">Select either the legal entities or the organizational hierarchy.</span></span>
15. <span data-ttu-id="4e6e5-137">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-137">Click **OK**.</span></span>
16. <span data-ttu-id="4e6e5-138">حدد "نعم" أو "لا" في **تحويل أبعاد الميزانية العمومية‬**.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-138">Select 'Yes' or 'No' in the **Transfer balance sheet dimension**.</span></span>

    <span data-ttu-id="4e6e5-139">من المستحسن تعيين هذا الخيار إلى "نعم" لحسابات الميزانية العمومية.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-139">It's best practice to set this option to Yes for Balance sheet accounts.</span></span> <span data-ttu-id="4e6e5-140">من شأن هذا الأمر أن يؤدي إلى المحافظة على الأبعاد المالية على الحركات التي تم ترحيلها عند إنشاء الأرصدة الأولية لحسابات الميزانية العمومية.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-140">This will maintain the financial dimensions on posted transactions when creating the beginning balances for the balance sheet accounts.</span></span> <span data-ttu-id="4e6e5-141">لحسابات الأرباح والخسائر، يمكنك اختيار المحافظة على الأبعاد المالية (‏‫إغلاق الكل‬) عندما يتم نقل الأرصدة إلى الأرباح المحتجزة‬ أو يمكنك اختيار استبدال الأبعاد المالية بقيمة بُعد مختلفة (إغلاق واحد‬).</span><span class="sxs-lookup"><span data-stu-id="4e6e5-141">For profit and loss accounts, you can select to maintain the financial dimensions (Close all) when the balances are moved to Retained earnings or you can select to have the financial dimensions replaced with a different dimension value (Close single).</span></span> <span data-ttu-id="4e6e5-142">إذا اخترت "إغلاق واحد"، فيمكنك تحديد قيمة بعد محددة لكل بعد أو حتى اختيار ترك القيمة فارغة.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-142">If you choose Close single, you can define a specific dimension value for each dimension or even choose to leave it blank.</span></span>  

17. <span data-ttu-id="4e6e5-143">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-143">Click **Save**.</span></span>
18. <span data-ttu-id="4e6e5-144">ابدأ إقفال نهاية السنة باختيار **إجراء الإقفال المالي‬** في **جزء الإجراءات**.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-144">Start the year-end close by choosing **Run fiscal close** on the **Action Pane**.</span></span> <span data-ttu-id="4e6e5-145">سيتم تشغيل إقفال نهاية السنة للقالب المحدد.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-145">The year-end close will be run for the selected template.</span></span>  
19. <span data-ttu-id="4e6e5-146">حدد كل الكيانات القانونية أو مجموعة فرعية لها من القالب لتشغيل إقفال نهاية السنة لها.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-146">Select all or a subset of legal entities from the template for which to run the year-end close.</span></span>

    <span data-ttu-id="4e6e5-147">عند تشغيل إقفال نهاية السنة للمرة الأولى، وللحصول على الأرصدة الأولية، قد تختار معظم المؤسسات تشغيل إقفال نهاية السنة لجميع الكيانات القانونية داخل القالب.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-147">When first running the year-end close, to get beginning balance,s most organizations may choose to run the year-end close for all legal entities within the template.</span></span> <span data-ttu-id="4e6e5-148">إذا تمت تسوية الإدخالات بعد ذلك، فقد تختار تشغيل إقفال نهاية السنة فقط للكيانات القانونية التي تتضمن تسوية.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-148">If adjusting entries are made after that, you may choose to run the year-end close for only the legal entities that have adjustments.</span></span>  

20. <span data-ttu-id="4e6e5-149">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-149">Click **OK**.</span></span>
21. <span data-ttu-id="4e6e5-150">حدد السنة المالية لتشغيل إقفال نهاية السنة لها.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-150">Select the fiscal year for which to run the year-end close.</span></span>
22. <span data-ttu-id="4e6e5-151">في حقل **الإيصال**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-151">In the **Voucher field**, type a value.</span></span> <span data-ttu-id="4e6e5-152">من المستحسن تضمين السنة المالية في رقم الإيصال، لتسهيل العثور على إيصال إقفال نهاية السنة المنشأ.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-152">It's best practice to include the fiscal year in the voucher number, to make it easier to find the year-end close voucher that is created.</span></span>  
23. <span data-ttu-id="4e6e5-153">يتم تشغيل إقفال نهاية السنة بشكل افتراضي في الوضع الدفعي.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-153">The year-end close defaults to run in batch.</span></span> <span data-ttu-id="4e6e5-154">من المستحسن تشغيل العمليات طويلة الأمد في الوضع الدفعي.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-154">It's best practice for long-running processes to run in batch mode.</span></span> <span data-ttu-id="4e6e5-155">هذه هي عادة إحدى هذه العمليات، ولهذا السبب فإن الإعداد الافتراضي هو استخدام الوضع الدفعي.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-155">This is typically one of those processes, which is why the default is to use batch mode.</span></span>  
24. <span data-ttu-id="4e6e5-156">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="4e6e5-156">Click **OK**.</span></span>

