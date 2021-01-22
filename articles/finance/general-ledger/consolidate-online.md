---
title: عمليات الدمج المالية عبر الإنترنت
description: يصف هذا الموضوع عمليات الدمج المالية في دفتر الأستاذ العام.
author: aprilolson
manager: AnnBe
ms.date: 07/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 86be6d4cc0af3f2fd92523d4ecd3825f2383fc48
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770725"
---
# <a name="online-financial-consolidations"></a><span data-ttu-id="129a5-103">عمليات الدمج المالية عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="129a5-103">Online financial consolidations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="129a5-104">يصف هذا الموضوع عمليات الدمج المالية في دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="129a5-104">This topic describes online financial consolidations in General ledger.</span></span> <span data-ttu-id="129a5-105">قبل قراءة هذا الموضوع، احرص على قراءة الموضوع [نظرة عامة على عمليات الدمج المالية وتحويل العملات‬](financial-consolidations-currency-translation.md).</span><span class="sxs-lookup"><span data-stu-id="129a5-105">Before you read this topic, be sure to read the [Financial consolidations and currency translation overview](financial-consolidations-currency-translation.md) topic.</span></span>

<span data-ttu-id="129a5-106">بعد إكمال عملية الإعداد، أدخل تفاصيل الدمج في صفحة **الدمج [عبر الإنترنت]**.</span><span class="sxs-lookup"><span data-stu-id="129a5-106">After you've completed your setup, you enter the details of the consolidation on the **Consolidate [Online]** page.</span></span> <span data-ttu-id="129a5-107">عند الانتهاء من ذلك، يمكنك النقر فوق **موافق** أو **دُفعة** لمعالجة الدمج.</span><span class="sxs-lookup"><span data-stu-id="129a5-107">When you've finished, you can click **OK** or **Batch** to process the consolidation.</span></span>

## <a name="criteria"></a><span data-ttu-id="129a5-108">معايير</span><span class="sxs-lookup"><span data-stu-id="129a5-108">Criteria</span></span>
<span data-ttu-id="129a5-109">على علامة التبويب **معايير** في صفحة **الدمج [عبر الإنترنت]**، يمكنك تحديد الحسابات والفترات الزمنية ونوع البيانات الجاري دمجها.</span><span class="sxs-lookup"><span data-stu-id="129a5-109">On the **Criteria** tab of the **Consolidate [Online]** page, you define the accounts, the periods, and the type of data that is being consolidated.</span></span>

<span data-ttu-id="129a5-110">![علامة التبويب المعايير](./media/criteria-consolidate-online.png "علامة التبويب المعايير")</span><span class="sxs-lookup"><span data-stu-id="129a5-110">![Criteria tab](./media/criteria-consolidate-online.png "Criteria tab")</span></span>

<span data-ttu-id="129a5-111">فيما يلي شرح لمختلف الحقول في علامة التبويب هذه:</span><span class="sxs-lookup"><span data-stu-id="129a5-111">Here is an explanation of the various fields on this tab:</span></span>

- <span data-ttu-id="129a5-112">**الوصف** – إدخال وصف دقيق للفترة التي تعمل على دمجها.</span><span class="sxs-lookup"><span data-stu-id="129a5-112">**Description** – Enter a precise description for the period that you're consolidating.</span></span>
- <span data-ttu-id="129a5-113">**الحساب الرئيسي** – استخدم الحقول الموجودة في هذا المقطع لتحديد الحسابات الرئيسية التي ستتم معالجتها.</span><span class="sxs-lookup"><span data-stu-id="129a5-113">**Main account** – Use the fields in this section to define the main accounts that will be processed.</span></span>

    - <span data-ttu-id="129a5-114">**من** و**إلى** – تحديد نطاق حسابات لمعالجتها.</span><span class="sxs-lookup"><span data-stu-id="129a5-114">**From** and **To** – Specify a range of accounts to process.</span></span> <span data-ttu-id="129a5-115">إذا تركت هذه الحقول فارغة، سيتم نقل جميع الحسابات من جميع الشركات إلى شركة الدمج.</span><span class="sxs-lookup"><span data-stu-id="129a5-115">If you leave these fields blank, all accounts from all companies will be moved to the consolidation company.</span></span> <span data-ttu-id="129a5-116">وبالتي، إذا كنت تعمل على دمج أربع شركات، وهناك دليل حسابات مختلف لدى كل شركة، فسيتم إنشاء جميع الحسابات من الشركات الأربع كلها في شركة الدمج.</span><span class="sxs-lookup"><span data-stu-id="129a5-116">Therefore, if you're consolidating four companies, and each company has a different chart of accounts, all accounts from all four companies will be created in the consolidation company.</span></span>
    - <span data-ttu-id="129a5-117">**استخدام حساب الدمج** – إذا قمت بتعيين هذا الخيار إلى **نعم**، يصبح الحقل **تحديد حساب دمج من‬** متوفرًا.</span><span class="sxs-lookup"><span data-stu-id="129a5-117">**Use consolidation account** – If you set this option to **Yes**, the **Select consolidation account from** field becomes available.</span></span> <span data-ttu-id="129a5-118">في هذا الحقل، حدد إن كان يجب دمج جميع الحسابات في حساب الدمج الذي تم تعيينه في صفحة **الحسابات الرئيسية**، أو إن كنت ترغب في تحديد الحساب من إحدى مجموعات حسابات الدمج.</span><span class="sxs-lookup"><span data-stu-id="129a5-118">In this field, select whether all accounts should be consolidated to the consolidation account that is set on the **Main accounts** page, or whether you want to select the account from one of the consolidation account groups.</span></span>
    - <span data-ttu-id="129a5-119">**مجموعة حسابات الدمج** – حدد المجموعة المراد استخدامها لتعيين الحساب الرئيسي للدمج.</span><span class="sxs-lookup"><span data-stu-id="129a5-119">**Consolidation account group** – Select the group to use for the main account mapping for the consolidation.</span></span>

- <span data-ttu-id="129a5-120">**فترة الدمج** – استخدم الحقول الموجودة في هذا المقطع لتحديد فترة الدمج‏‎.</span><span class="sxs-lookup"><span data-stu-id="129a5-120">**Consolidation period** – Use the fields in this section to define the consolidation period.</span></span>

    - <span data-ttu-id="129a5-121">**من** و**إلى** – تحديد نطاق تواريخ للدمج.</span><span class="sxs-lookup"><span data-stu-id="129a5-121">**From** and **To** – Specify a range of dates for the consolidation.</span></span> <span data-ttu-id="129a5-122">إذا تركت هذه الحقول فارغة، ستتم معالجة عملية الدمج لجميع الفترات المحددة في تقويم دفتر الأستاذ للشركة.</span><span class="sxs-lookup"><span data-stu-id="129a5-122">If you leave these fields blank, the consolidation will be processed for all periods that are defined in the ledger calendar for the company.</span></span> <span data-ttu-id="129a5-123">ونحن نوصي بعدم ترك هذه الحقول فارغة.</span><span class="sxs-lookup"><span data-stu-id="129a5-123">We don't recommend that you leave these fields blank.</span></span>
    - <span data-ttu-id="129a5-124">**تضمين المبالغ الفعلية** - عيّن هذا الخيار إلى **نعم** لدمج البيانات الفعلية.</span><span class="sxs-lookup"><span data-stu-id="129a5-124">**Include actual amounts** – Set this option to **Yes** to consolidate your actual data.</span></span>
    - <span data-ttu-id="129a5-125">**تضمين مبالغ الموازنة** - عيّن هذا الخيار إلى **نعم** لدمج البيانات من سجل الموازنة.</span><span class="sxs-lookup"><span data-stu-id="129a5-125">**Include budget amounts** – Set this option to **Yes** to consolidate data from the budget register.</span></span>
    - <span data-ttu-id="129a5-126">**‏‫إعادة إنشاء أرصدة خلال عملية الدمج‬** - لا ننصح بتعيين هذا الخيار إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="129a5-126">**Rebuild balances during consolidation** – We don't recommend that you set this option to **Yes**.</span></span> <span data-ttu-id="129a5-127">بدلاً من ذلك، يمكنك إعادة إنشاء الأرصدة كوظيفة دُفعية منفصلة.</span><span class="sxs-lookup"><span data-stu-id="129a5-127">Instead, rebuild balances as a separate batch job.</span></span>

- <span data-ttu-id="129a5-128">**نماذج الموازنة** - إذا حددت دمج بيانات الموازنة، فاستخدم الحقول الموجودة في هذا المقطع لتحديد نماذج الموازنة.</span><span class="sxs-lookup"><span data-stu-id="129a5-128">**Budget models** – If you've selected to consolidate budget data, use the fields in this section to define the budget models.</span></span>

    - <span data-ttu-id="129a5-129">**من** و**إلى** – تحديد نطاق نماذج لمعالجتها.</span><span class="sxs-lookup"><span data-stu-id="129a5-129">**From** and **To** – Specify the range of models to use.</span></span>
    - <span data-ttu-id="129a5-130">**نوع سعر الموازنة‬** – تحديد نوع سعر الموازنة‬ المطلوب استخدامه لتحويل عملة من بيانات الموازنة.</span><span class="sxs-lookup"><span data-stu-id="129a5-130">**Budget rate type** – Select the type of budget rate to use for currency translation of budget data.</span></span>

## <a name="financial-dimensions"></a><span data-ttu-id="129a5-131">الأبعاد المالية</span><span class="sxs-lookup"><span data-stu-id="129a5-131">Financial dimensions</span></span>
<span data-ttu-id="129a5-132">على علامة التبويب **الأبعاد المالية**، يمكنك تحديد الأبعاد التي ينبغي تضمينها في شركة الدمج.</span><span class="sxs-lookup"><span data-stu-id="129a5-132">On the **Financial dimensions** tab, you define the dimensions that should be included in the consolidation company.</span></span> <span data-ttu-id="129a5-133">لتحديد بُعد، عيّن حقل **المواصفات** إلى **بعد**، ثم حدد ترتيب الأبعاد في شركة الدمج.</span><span class="sxs-lookup"><span data-stu-id="129a5-133">To select a dimension, set the **Specification** field to **Dimension**, and then define the order of the dimension in the consolidation company.</span></span>

<span data-ttu-id="129a5-134">![علامة التبويب الأبعاد المالية](./media/financial-dimensions-cons.png "علامة التبويب الأبعاد المالية")</span><span class="sxs-lookup"><span data-stu-id="129a5-134">![Financial dimensions tab](./media/financial-dimensions-cons.png "Financial dimensions tab")</span></span>

<span data-ttu-id="129a5-135">بغض النظر عن الترتيب الذي تحدده، سيكون **الحساب الرئيسي** دائمًا المقطع الأول.</span><span class="sxs-lookup"><span data-stu-id="129a5-135">Regardless of the order that you define, **Main account** will always be the first segment.</span></span>

## <a name="legal-entities"></a><span data-ttu-id="129a5-136">الكيانات القانونية</span><span class="sxs-lookup"><span data-stu-id="129a5-136">Legal entities</span></span>
<span data-ttu-id="129a5-137">على علامة تبويب **الكيانات القانونية**، يمكنك تحديد الشركات التي ينبغي تضمينها في شركة الدمج.</span><span class="sxs-lookup"><span data-stu-id="129a5-137">On the **Legal entities** tab, you define the companies that should be included in the consolidation company.</span></span> <span data-ttu-id="129a5-138">يمكنك أيضًا تحديد النسبة المئوية للملكية لهذه الشركات.</span><span class="sxs-lookup"><span data-stu-id="129a5-138">You also define the ownership percentage of those companies.</span></span> <span data-ttu-id="129a5-139">إذا قمت بتحديد ملكية بنسبة أقل من 100 بالمائة، سيتم تجميع النسبة المئوية المحددة لشركة الدمج.</span><span class="sxs-lookup"><span data-stu-id="129a5-139">If you specify less than 100-percent ownership, the specified percentage will be rolled up to the consolidation company.</span></span> <span data-ttu-id="129a5-140">فيما يتعلق بفروق التحويلات‬‏‎، يُستخدم الحقل **نوع حساب فروق التحويلات‬** لتحديد الحساب الرئيسي من الإعداد الموجود في صفحة **حسابات الحركات التلقائية‬**.</span><span class="sxs-lookup"><span data-stu-id="129a5-140">For any translation differences, the **Account type for conversion differences** field is used to select the main account from the setup on the **Accounts for automatic transactions** page.</span></span>

<span data-ttu-id="129a5-141">![علامة التبويب الكيانات القانونية](./media/legal-entities-cons.png "علامة التبويب الكيانات القانونية")</span><span class="sxs-lookup"><span data-stu-id="129a5-141">![Legal entities tab](./media/legal-entities-cons.png "Legal entities tab")</span></span>

<span data-ttu-id="129a5-142">![صفحة حسابات الحركات التلقائية](./media/accounts-for-automatic-cons.png "صفحة حسابات الحركات التلقائية")</span><span class="sxs-lookup"><span data-stu-id="129a5-142">![Accounts for automatic transactions page](./media/accounts-for-automatic-cons.png "Accounts for automatic transactions page")</span></span>

## <a name="elimination"></a><span data-ttu-id="129a5-143">استبعاد</span><span class="sxs-lookup"><span data-stu-id="129a5-143">Elimination</span></span>
<span data-ttu-id="129a5-144">على علامة تبويب **الاستبعاد**، لديك ثلاثة خيارات لمعالجة الاستبعادات:</span><span class="sxs-lookup"><span data-stu-id="129a5-144">On the **Elimination** tab, you have three options for processing eliminations:</span></span>

- <span data-ttu-id="129a5-145">حدد قاعدة الاستبعاد، ثم في الحقل **خيارات المقترح‬**، حدد **مقترح فقط**.</span><span class="sxs-lookup"><span data-stu-id="129a5-145">Select the elimination rule, and then, in the **Proposal options** field, select **Proposal only**.</span></span> <span data-ttu-id="129a5-146">سيقوم هذا الخيار بمعالجة الاستبعاد أثناء عملية الدمج، ولكنه لن يقوم بترحيل كل شيء في خطوة واحدة.</span><span class="sxs-lookup"><span data-stu-id="129a5-146">This option will process the elimination during the consolidation process, but it won't post everything in one step.</span></span> <span data-ttu-id="129a5-147">يمكن ترحيل دفتر اليومية في يوم لاحق.</span><span class="sxs-lookup"><span data-stu-id="129a5-147">You can post the journal later.</span></span>
- <span data-ttu-id="129a5-148">حدد قاعدة الاستبعاد، ثم في الحقل **خيارات المقترح‬**، حدد **ترحيل فقط**.</span><span class="sxs-lookup"><span data-stu-id="129a5-148">Select the elimination rule, and then, in the **Proposal options** field, select **Post only**.</span></span> <span data-ttu-id="129a5-149">سيقوم هذا الخيار بمعالجة الاستبعاد أثناء عملية الدمج، وسيقوم بترحيل كل شيء في خطوة واحدة.</span><span class="sxs-lookup"><span data-stu-id="129a5-149">This option will process the elimination during the consolidation process and will post everything in one step.</span></span>
- <span data-ttu-id="129a5-150">قم بتشغيل مقترح استبعاد بشكل منفصل عن عملية الدمج باستخدام دفتر يومية الاستبعاد.</span><span class="sxs-lookup"><span data-stu-id="129a5-150">Run an elimination proposal separately from the consolidation process by using the elimination journal.</span></span>

<span data-ttu-id="129a5-151">![علامة التبويب استبعاد](./media/elimination-cons-onl.png "علامة التبويب استبعاد")</span><span class="sxs-lookup"><span data-stu-id="129a5-151">![Elimination tab](./media/elimination-cons-onl.png "Elimination tab")</span></span>

<span data-ttu-id="129a5-152">لمزيد من المعلومات عن الاستبعادات، راجع [قواعد الاستبعاد](./elimination-rules.md).</span><span class="sxs-lookup"><span data-stu-id="129a5-152">For more information about eliminations, see [Elimination rules](./elimination-rules.md).</span></span>

## <a name="currency-translation"></a><span data-ttu-id="129a5-153">تحويل العملة</span><span class="sxs-lookup"><span data-stu-id="129a5-153">Currency translation</span></span>
<span data-ttu-id="129a5-154">على علامة التبويب **تحويل العملة‬**، حدد الكيان القانوني والحساب ونوع سعر الصرف والسعر.</span><span class="sxs-lookup"><span data-stu-id="129a5-154">On the **Currency translation** tab, you define the legal entity, account and exchange rate type, and rate.</span></span> <span data-ttu-id="129a5-155">تتوفر ثلاثة خيارات في الحقل **تطبيق سعر الصرف من**:</span><span class="sxs-lookup"><span data-stu-id="129a5-155">Three options are available in the **Apply exchange rate from** field:</span></span>

- <span data-ttu-id="129a5-156">**تاريخ الدمج** – سيتم استخدام تاريخ الدمج للحصول على سعر الصرف.</span><span class="sxs-lookup"><span data-stu-id="129a5-156">**Consolidation date** – The date of the consolidation will be used to get the exchange rate.</span></span> <span data-ttu-id="129a5-157">يعادل هذا السعر السعر الفوري أو سعر نهاية الشهر.</span><span class="sxs-lookup"><span data-stu-id="129a5-157">This rate is equivalent to the spot or month-end rate.</span></span> <span data-ttu-id="129a5-158">سترى معاينة للسعر، ولكن لن تتمكن من تحريره.</span><span class="sxs-lookup"><span data-stu-id="129a5-158">You will see a preview of the rate, but you can't edit it.</span></span>
- <span data-ttu-id="129a5-159">**تاريخ الحركة** – التاريخ الذي سيتم فيه استخدام كل حركة لتحديد سعر صرف.</span><span class="sxs-lookup"><span data-stu-id="129a5-159">**Transaction date** – The date of each transaction will be used to select an exchange rate.</span></span> <span data-ttu-id="129a5-160">يُستخدم هذا الخيار في الكثير من الأحيان للأصول الثابتة وغالبًا ما يشار إليه بالسعر السابق.</span><span class="sxs-lookup"><span data-stu-id="129a5-160">This option is most often used for fixed assets and is often referred to as a historical rate.</span></span> <span data-ttu-id="129a5-161">لا يمكنك رؤية معاينة للسعر نظرًا لوجود أسعار كثيرة لمختلف الحركات في نطاق الحساب.</span><span class="sxs-lookup"><span data-stu-id="129a5-161">You can't see a preview of the rate, because there will be many rates for the various transactions in the account range.</span></span>
- <span data-ttu-id="129a5-162">**سعر معرف من قِبل المستخدم‬** – بعد تحديد هذا الخيار، يمكنك إدخال سعر الصرف الذي تريده</span><span class="sxs-lookup"><span data-stu-id="129a5-162">**User defined rate** – After you select this option, you can enter the exchange rate that you want.</span></span> <span data-ttu-id="129a5-163">قد يكون هذا الخيار مفيدًا لمتوسط أسعار الصرف أو إذا كنت تقوم بالدمج مقابل سعر صرف ثابت.</span><span class="sxs-lookup"><span data-stu-id="129a5-163">This option can be useful for average exchange rates or if you're consolidating against a fixed exchange rate.</span></span>

<span data-ttu-id="129a5-164">![علامة التبويب تحويل العملة](./media/currency-translation-cons-online.png "علامة التبويب تحويل العملة")</span><span class="sxs-lookup"><span data-stu-id="129a5-164">![Currency translation tab](./media/currency-translation-cons-online.png "Currency translation tab")</span></span>

## <a name="additional-resources"></a><span data-ttu-id="129a5-165">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="129a5-165">Additional resources</span></span>

<span data-ttu-id="129a5-166">لمزيد من المعلومات حول الدمج وتحويل العملة‬، راجع الموضوع الأصل لهذا الموضوع، [نظرة عامة على عمليات الدمج المالية وتحويل العملات‬](./financial-consolidations-currency-translation.md).</span><span class="sxs-lookup"><span data-stu-id="129a5-166">For more information about consolidation and currency translations, see the parent topic of this topic, [Financial consolidations and currency translation overview](./financial-consolidations-currency-translation.md).</span></span>

<span data-ttu-id="129a5-167">لمزيد من المعلومات حول السيناريوهات حيث قد تنشئ قوائم مالية مدمجة، راجع [إنشاء قوائم مالية مدمجة‬](./generating-consolidated-financial-statements.md).</span><span class="sxs-lookup"><span data-stu-id="129a5-167">For information about scenarios where you might generate consolidate financial statements, see [Generate consolidated financial statements](./generating-consolidated-financial-statements.md).</span></span>