---
title: نظرة عامة على التجميع والاستبعاد
description: توفر هذه المقالة معلومات عامة حول عملية التوحيد والاستبعاد. وتتضمن أيضًا إجابات على بعض الأسئلة المتداولة.
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerConsolidate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13151
ms.assetid: 9d8f55cb-b2cf-4e01-89cf-0e21f5c8ae1f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 566b1ecef3f9e540c651fe214accadcf32f4fbed
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772043"
---
# <a name="consolidation-and-elimination-overview"></a><span data-ttu-id="6f7b1-104">نظرة عامة على التجميع والاستبعاد</span><span class="sxs-lookup"><span data-stu-id="6f7b1-104">Consolidation and elimination overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f7b1-105">توفر هذه المقالة معلومات عامة حول عملية التوحيد والاستبعاد.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-105">This article provides general information about the consolidation and elimination process.</span></span> <span data-ttu-id="6f7b1-106">وتتضمن أيضًا إجابات على بعض الأسئلة المتداولة.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-106">It includes answers to some frequently asked questions.</span></span>

<span data-ttu-id="6f7b1-107">عند تجميع البيانات، يتم تجميع النتائج المالية لعدد من الشركات التابعة في نتائج شركة مجمعة واحدة.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-107">When you consolidate data, the financial results for multiple subsidiary companies are combined into results for a single, consolidated company.</span></span> <span data-ttu-id="6f7b1-108">وقد تكون الشركات التابعة موجودة في إصدارات أو أنظمة مختلفة، وقد لا تكون مملوكة بالكامل، ويمكنها استخدام عملات مختلفة.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-108">Subsidiaries might be on different versions or systems, they might not be fully owned, and they might use different currencies.</span></span> <span data-ttu-id="6f7b1-109">وهناك عدة خيارات لتجميع البيانات:</span><span class="sxs-lookup"><span data-stu-id="6f7b1-109">There are multiple options for consolidating data:</span></span>

-   <span data-ttu-id="6f7b1-110">**التجميع على الإنترنت** - يقوم هذا الخيار بتجميع الأرصدة اليومية حسب الحسابات والأبعاد المحددة، ويخزنها في شركة مجمعة.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-110">**Consolidate online** – This option consolidates daily balances by the selected accounts and dimensions, and stores them in a consolidation company.</span></span>
-   <span data-ttu-id="6f7b1-111">**التقارير المالية** - يتيح هذا الخيار تجميع الحركات والأرصدة، ويمكن إنشاؤه في أي وقت.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-111">**Financial reporting** – This option enables consolidation of transactions and balances, and can be generated at any time.</span></span> <span data-ttu-id="6f7b1-112">يمكن إنشاء مستويات متعددة من التدرج هرمي، ويمكن الاطلاع على عملات التقارير المتعددة.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-112">Multiple levels of hierarchies can be created, and multiple reporting currencies can be viewed.</span></span>
-   <span data-ttu-id="6f7b1-113">**التجميع مع الاستيراد** - يستورد هذا الخيار أرصدة الواردات إلى شركة مجمعة.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-113">**Consolidate with import** – This option imports balances into a consolidation company.</span></span>
-   <span data-ttu-id="6f7b1-114">**تصدير أرصدة الشركة** - يوفر هذا الخيار ملف تصدير لأرصدة الشركة.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-114">**Export company balances** – This option provides an export file of company balances.</span></span> <span data-ttu-id="6f7b1-115">وبعد ذلك، يمكن استيراد الملف إلى حالات أو أنظمة أخرى.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-115">The file can then be imported into other instances or systems.</span></span> <span data-ttu-id="6f7b1-116">كما يمكن استخدام التقارير المالية لتصدير الأرصدة إلى ملف Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-116">Financial reporting can also be used to export the balances to a Microsoft Excel file.</span></span>

<span data-ttu-id="6f7b1-117">يمكن الإبلاغ عن عمليات الاستبعاد بطرق متعددة:</span><span class="sxs-lookup"><span data-stu-id="6f7b1-117">Eliminations can be reported in multiple ways:</span></span>

-   <span data-ttu-id="6f7b1-118">يمكن إعداد قواعد الاستبعاد في النظام، وبعد ذلك معالجتها أثناء عملية التجميع أو من خلال مقترح استبعاد.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-118">Elimination rules can be set up in the system, and then processed during the consolidation process or through an elimination proposal.</span></span> <span data-ttu-id="6f7b1-119">ويمكن ترحيل القواعد لأي شركة قامت بتحديد **‏‫يُستخدم لعملية الاستبعاد المالي‬** في إعداد الكيان القانوني.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-119">The rules can be posted to any company that has **Use for financial elimination process** selected in the legal entity setup.</span></span>
-   <span data-ttu-id="6f7b1-120">يمكن إنشاء شركة مستقلة واستخدامها لتحديد وترحيل حركات الاستبعاد يدوياً.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-120">A separate company can be created and used to manually determine and post elimination transactions.</span></span> <span data-ttu-id="6f7b1-121">يمكن استخدام هذه الشركة في عملية التجميع أو في التقارير المالية.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-121">This company can be used in the consolidation process or in financial reporting.</span></span>
-   <span data-ttu-id="6f7b1-122">يمكن تصفية الحسابات والأبعاد المالية التي يتم استخدامها لتحديد نشاط بين الشركات الشقيقة في تعريف صف أو عمود في التقارير المالية، ويمكن استخدام قدرات التنقل الكاملة.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-122">The accounts and financial dimensions that are used to determine intercompany activity can be filtered on a row definition or column definition in Financial reporting, and full drill-down capabilities can be used.</span></span> <span data-ttu-id="6f7b1-123">يمكن بعذلك استخدام عمود أو صف محسوب لإزالة الحسابات والأبعاد المالية من الإجمالي المجمع.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-123">A calculated column or row can then be used to remove the accounts and financial dimensions from the consolidated total.</span></span>

<span data-ttu-id="6f7b1-124">هناك العديد من سيناريوهات التجميع، ويمكن لكل طريقة معالجة السيناريوهات بطرق مختلفة.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-124">There are many consolidation scenarios, and each method can handle the scenarios in different ways.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="6f7b1-125">الأسئلة المتداولة</span><span class="sxs-lookup"><span data-stu-id="6f7b1-125">Frequently asked questions</span></span>
1.  <span data-ttu-id="6f7b1-126">أفضل ترحيل عمليات الاستبعاد في قاعدة بيانات.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-126">I prefer to post eliminations in a database.</span></span> <span data-ttu-id="6f7b1-127">ما خياراتي المتاحة؟</span><span class="sxs-lookup"><span data-stu-id="6f7b1-127">What are my options?</span></span>

<span data-ttu-id="6f7b1-128">لديك خيارات متعددة.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-128">You have multiple options.</span></span> <span data-ttu-id="6f7b1-129">ويمكنك استخدام خيار **التجميع على الإنترنت**، وتضمين عمليات الاستبعاد أثناء العملية أو كاقتراح.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-129">You can use the **Consolidate online** option, and include eliminations during the process or as a proposal.</span></span> <span data-ttu-id="6f7b1-130">وسيتم ترحيل الحركات في الشركة الموحدة.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-130">The transactions will be posted in the consolidation company.</span></span> <span data-ttu-id="6f7b1-131">وبدلاً من ذلك، يمكنك الحصول على شركة مستقلة تقوم يدوياً بإنشاء عمليات الاستبعاد فيها، ثم استخدام تلك الشركة في التقارير المالية أو في عملية التجميع.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-131">Alternatively, you can have a separate company that you manually create the eliminations in, and then use that company in Financial reporting or in the consolidation process.</span></span>

2.  <span data-ttu-id="6f7b1-132">نحن بحاجة إلى نتائجنا المجمعة بعملات التقارير المتعددة.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-132">We need our consolidated results in multiple reporting currencies.</span></span>

<span data-ttu-id="6f7b1-133">يشتمل خيار **التقارير المالية** على خيار تقارير غير محدودة.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-133">The **Financial reporting** option has unlimited reporting currencies.</span></span> <span data-ttu-id="6f7b1-134">ويتم تحويل البيانات أثناء إنشاء التقرير، استناداً إلى سعر صرف العملة وطريقة تحويل العملة اللذين تم تعيينهما في الحساب الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-134">The data is translated during report generation, based on the exchange rate type and currency translation method that are set on the main account.</span></span> <span data-ttu-id="6f7b1-135">ومع ذلك، نظراً لأن خيار **التجميع على الإنترنت** يشتمل على عملة تقارير واحدة فقط، يُتطلب وجود شركة موحدة لكل عملة تقارير إذا استخدمت هذا الخيار.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-135">However, because the **Consolidate online** option has only one reporting currency, a consolidated company is required for each reporting currency if you use that option.</span></span> <span data-ttu-id="6f7b1-136">خيار **التقارير المالية** هو الطريقة الموصى به.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-136">The **Financial reporting** option is the recommended method.</span></span>

3.  <span data-ttu-id="6f7b1-137">أريد أن أرى تفاصيل مستوى الحركة لكل شركة.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-137">I want to see transaction-level detail for each company.</span></span>

<span data-ttu-id="6f7b1-138">خيار **التقارير المالية** هو الحل، لأنه يمكن عرض تفاصيل مستوى الحركة للعديد من الشركات المدرجة في تعريف شجرة التقارير.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-138">The **Financial reporting** option is the solution, because transaction-level detail can be viewed for as many companies as are included in the reporting tree definition.</span></span>

4.  <span data-ttu-id="6f7b1-139">نستخدم تخطيط الموازنة أو التحكم في الموازنة، ويجب أن يتم دمجها.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-139">We are using budget planning or budget control, and it must be consolidated.</span></span>
<span data-ttu-id="6f7b1-140">خيار **التقارير المالية** هو الحل لتجميع بيانات لتخطيط الموازنة أو مراقبة الموازنة.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-140">The **Financial reporting** option is the solution to consolidate any budget planning or budget control data.</span></span>

5.  <span data-ttu-id="6f7b1-141">تنتشر الشركات التابعة لنا في جميع أنحاء العالم، ولدينا مخططات حسابات متعددة.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-141">Our subsidiaries are spread throughout the world, and we have multiple charts of accounts.</span></span> <span data-ttu-id="6f7b1-142">ما أفضل طريقة لتجميع البيانات الخاصة بنا؟</span><span class="sxs-lookup"><span data-stu-id="6f7b1-142">What is the best method for consolidating our data?</span></span>

<span data-ttu-id="6f7b1-143">لديك خيارات متعددة عندما يجب أن تقوم بمعالجة مخططات حسابات متعددة.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-143">You have multiple options when you must handle multiple charts of accounts.</span></span> <span data-ttu-id="6f7b1-144">ويمكنك استخدام خيار **التجميع على الإنترنت**، ثم اختيار استخدام إما حساب التجميع الذي تم تحديده في الحساب الرئيسي أو مجموعة حساب تجميع.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-144">You can use the **Consolidate online** option, and then choose to use either the consolidation account that is defined on the main account or a consolidation account group.</span></span> <span data-ttu-id="6f7b1-145">كما يمكنك استخدام خيار **التقارير المالية**، وتضمين ارتباطات متعددة للأبعاد المالية في تعريف الصف، وتعيين الحسابات.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-145">You can also use the **Financial reporting** option, include multiple links to the financial dimensions in the row definition, and map the accounts.</span></span>

6.  <span data-ttu-id="6f7b1-146">نتطلب عدة مستويات للتجميع.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-146">We require multiple levels of consolidation.</span></span> <span data-ttu-id="6f7b1-147">وبعبارة أخرى، نقوم أولاً بتوحيد فروعنا الأوروبية بلجنيه الإسترليني (GBP).</span><span class="sxs-lookup"><span data-stu-id="6f7b1-147">In other words, we first consolidate all our European subsidiaries to the British pound (GBP).</span></span> <span data-ttu-id="6f7b1-148">وبعد ذلك، نحصل على تلك البيانات ونقوم بتحويل المبلغ المجمع إلى الدولارات الأمريكية.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-148">We then take that data and translate the consolidated amount to US dollars.</span></span> <span data-ttu-id="6f7b1-149">كيف يمكننا أن نفعل ذلك؟</span><span class="sxs-lookup"><span data-stu-id="6f7b1-149">How can we do this?</span></span>

<span data-ttu-id="6f7b1-150">عند تطلب وجود مستويات متعددة للتجميع، يتم استخدام عملات مختلفة عند كل مستوى، ويجب عليك استخدام خيار **التجميع على الإنترنت**.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-150">When multiple levels of consolidation are required, and different currencies are used at each level, you must use the **Consolidate online** option.</span></span> <span data-ttu-id="6f7b1-151">ويجب إنشاء عدة شركات تجميع تختلف في عملات المحاسبة والتقارير الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-151">Multiple consolidation companies must be created that differ in their accounting and reporting currencies.</span></span> <span data-ttu-id="6f7b1-152">ويجب إجراء التجميع عدة مرات بعد ذلك.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-152">The consolidation must then be run multiple times.</span></span> <span data-ttu-id="6f7b1-153">ويقوم خيار **التقارير المالية** دائمًا بالتحويل من كل عملة محاسبة للشركة المصدر إلى العملة المحددة.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-153">The **Financial reporting** option always translates from each source company's accounting currency to the selected currency.</span></span>

7.  <span data-ttu-id="6f7b1-154">لدينا فروع على نظام مختلف.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-154">We have subsidiaries on a different system.</span></span> <span data-ttu-id="6f7b1-155">كيف يمكننا دمجها؟</span><span class="sxs-lookup"><span data-stu-id="6f7b1-155">How can we consolidate them?</span></span>

<span data-ttu-id="6f7b1-156">استخدم خيار **التجميع مع الاستيراد** لتجميع الأرصدة في شركة تجميع.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-156">Use the **Consolidate with import** option to bring the balances into a consolidation company.</span></span>

8.  <span data-ttu-id="6f7b1-157">بعض الشركات التابعة لنا ليست مملوكة لنا بالكامل.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-157">Some of our subsidiaries are not fully owned.</span></span> <span data-ttu-id="6f7b1-158">ما أفضل طريقة لدمجها؟</span><span class="sxs-lookup"><span data-stu-id="6f7b1-158">What is the best method for consolidating them?</span></span>

<span data-ttu-id="6f7b1-159">لديك العديد من الخيارات للشركات التابعة المملوكة جزئيًا.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-159">You have multiple options for partially owned subsidiaries.</span></span> <span data-ttu-id="6f7b1-160">باستخدام خيار **التقارير المالية**، يمكنك تحديد تعريف شجرة تقارير والملكية.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-160">By using the **Financial reporting** option, you can define a reporting tree definition and the ownership.</span></span> <span data-ttu-id="6f7b1-161">كما يمكنك استخدام صف أو عمود محسوب لتمثيل المقدار المملوك جزئيًا.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-161">You can also use a calculated row or column to represent the partially owned amount.</span></span> <span data-ttu-id="6f7b1-162">ويمكنك حتى إظهار مصلحة الأقلية كصف خاص بها في تقرير.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-162">You can even show the minority interest as its own row on a report.</span></span> <span data-ttu-id="6f7b1-163">كما يمكنك استخدام خيار **التجميع على الإنترنت**.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-163">You can also use the **Consolidate online** option.</span></span> <span data-ttu-id="6f7b1-164">تشتمل علامة التبويب **الكيانات القانونية** على عمود **الملكية**، حيث يمكنك تحديد النسبة المئوية التي تملكها الشركة الأم.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-164">The **Legal entities** tab has an **Ownership** column, where you can define the percentage that is owned by the parent company.</span></span>

9.  <span data-ttu-id="6f7b1-165">يجب على مؤسستنا إظهار عمليات التجميع حسب وحدة الأعمال أو تحتاج إلى استخدام التدرجات الهرمية للمؤسسات.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-165">Our organization must show consolidations by business unit or wants to use the organization hierarchies.</span></span>

<span data-ttu-id="6f7b1-166">خيار **التقارير المالية** هو الحل.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-166">The **Financial reporting** option is the solution.</span></span> <span data-ttu-id="6f7b1-167">ويمكن الإبلاغ عن التدرجات الهرمية للمؤسسات التي تشمل الكيانات القانونية أو الأبعاد المالية فيها في التقارير المالية.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-167">Organization hierarchies that have legal entities or financial dimensions in them can be reported on in Financial reporting.</span></span> <span data-ttu-id="6f7b1-168">كما يمكنك إنشاء التدرجات الهرمية متعددة المستويات الخاصة بك باستخدام تعريف شجرة تقرير يحتوي على مجموعة من الكيانات القانونية وقيم الأبعاد.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-168">You can also create your own multilevel hierarchies by using a reporting tree definition that has a combination of legal entities and dimension values.</span></span>

10. <span data-ttu-id="6f7b1-169">لدينا أكثر من مثيل واحد للنظام.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-169">We have more than one instance of the system.</span></span>

<span data-ttu-id="6f7b1-170">باستخدام خيار **تصدير أرصدة الشركة** للتصدير من مثيل واحد، ثم باستخدام خيار **التجميع مع الاستيراد** في المثيل الآخر، يمكنك تجميع البيانات.</span><span class="sxs-lookup"><span data-stu-id="6f7b1-170">By using the **Export company balances** option to export from one instance and then using the **Consolidate with import** option on the other instance, you can consolidate the data.</span></span>


<span data-ttu-id="6f7b1-171">لمزيد من المعلومات، راجع [إعادة تقييم العملة في شركة موحدة](../general-ledger/currency-revaluation-consolidation-company.md).</span><span class="sxs-lookup"><span data-stu-id="6f7b1-171">For more information, see [Currency revaluation in a consolidation company](../general-ledger/currency-revaluation-consolidation-company.md).</span></span>

