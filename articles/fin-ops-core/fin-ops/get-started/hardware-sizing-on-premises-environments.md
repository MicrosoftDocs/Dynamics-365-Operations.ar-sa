---
title: متطلبات ضبط حجم الأجهزة للبيئات المحلية
description: يسرد هذا الموضوع متطلبات ضبط حجم الأجهزة للبيئات المحلية.
author: sericks007
ms.date: 11/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 55651
ms.assetid: ''
ms.search.region: Global
ms.author: chwolf
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: c5e6e96ea1ce821233d7104bb9a7af8e793f4264
ms.sourcegitcommit: 2f766e5bb8574d250f19180ff2e101e895097713
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923470"
---
# <a name="hardware-sizing-requirements-for-on-premises-environments"></a><span data-ttu-id="205e2-103">متطلبات ضبط حجم الأجهزة للبيئات المحلية</span><span class="sxs-lookup"><span data-stu-id="205e2-103">Hardware sizing requirements for on-premises environments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="205e2-104">قبل أن تبدأ عملية ضبط حجم الأجهزة والبنية الأساسية لبيئة محلية، عليك الاطلاع على [متطلبات النظام لعمليات النشر على السحابة](system-requirements.md) و[إرشادات الإعداد والنشر](../../dev-itpro/deployment/setup-deploy-on-premises-environments.md) لتكوين فهم ثابت للبنية الأساسية.</span><span class="sxs-lookup"><span data-stu-id="205e2-104">Before you begin the hardware and infrastructure sizing process for an on-premises environment, familiarize yourself with the [System requirements for cloud deployments](system-requirements.md) and [Setup and deployment instructions](../../dev-itpro/deployment/setup-deploy-on-premises-environments.md) to gain a solid understanding off the underlying infrastructure.</span></span>

> [!NOTE]
> <span data-ttu-id="205e2-105">يُرجى إيلاء اهتمام بالغ بأفضل الممارسات لإعداد النظام للحصول على الأداء الأمثل.</span><span class="sxs-lookup"><span data-stu-id="205e2-105">Pay close attention to the system setup best practices for optimum performance.</span></span>

<span data-ttu-id="205e2-106">بعد الانتهاء من مراجعة الوثائق، يمكنك بدء عملية تقييم حجم الحركات والمستخدمين المتزامنين وضبط حجم بيئتك استنادًا إلى معدل الإنتاجية‬ الأساسية.</span><span class="sxs-lookup"><span data-stu-id="205e2-106">After you have reviewed the documentation, you can start the process of estimating your transactional and concurrent user volume and sizing your environment based on the average core throughput.</span></span>

## <a name="factors-that-affect-sizing"></a><span data-ttu-id="205e2-107">العوامل التي تؤثر على ضبط الحجم</span><span class="sxs-lookup"><span data-stu-id="205e2-107">Factors that affect sizing</span></span>

<span data-ttu-id="205e2-108">تساهم كافة العوامل التي تظهر في الرسم التوضيحي التالي في ضبط الحجم.</span><span class="sxs-lookup"><span data-stu-id="205e2-108">All the factors shown in the following illustration contribute to sizing.</span></span> <span data-ttu-id="205e2-109">بقدر ما كانت المعلومات التي يتم جمعها مفصلة، زادت دقة تحديد ضبط الحجم.</span><span class="sxs-lookup"><span data-stu-id="205e2-109">The more detailed information that is collected, the more precisely you can determine sizing.</span></span> <span data-ttu-id="205e2-110">ستكون عملية ضبط حجم الأجهزة، بدون بيانات داعمة، غير دقيقة على الأرجح.</span><span class="sxs-lookup"><span data-stu-id="205e2-110">Hardware sizing, without supporting data, is likely to be inaccurate.</span></span> <span data-ttu-id="205e2-111">الحد الأدنى المطلق لمتطلبات البيانات الضرورية هو بنود حمل الحركة الأقصى بالساعة.</span><span class="sxs-lookup"><span data-stu-id="205e2-111">The absolute minimum requirement for necessary data is the peak transaction line load per hour.</span></span>

<span data-ttu-id="205e2-112">[![ضبط حجم الأجهزة للبيئات المحلية](./media/lbd-sizing-01.png)](./media/lbd-sizing-01.png)</span><span class="sxs-lookup"><span data-stu-id="205e2-112">[![Hardware sizing for on-premises environments](./media/lbd-sizing-01.png)](./media/lbd-sizing-01.png)</span></span>

<span data-ttu-id="205e2-113">العنصر الأول والأكثر أهمية المطلوب لتقييم ضبط الحجم بدقة هو ملف تعريف الحركة أو وصف الحركة، ويمكن عرضه من اليسار إلى اليمين.</span><span class="sxs-lookup"><span data-stu-id="205e2-113">Viewed from left to right, the first and most important factor needed to accurately estimate sizing is a transaction profile or a transaction characterization.</span></span> <span data-ttu-id="205e2-114">من الضروري العثور دائمًا على حجم الحركات الأقصى في الساعة.</span><span class="sxs-lookup"><span data-stu-id="205e2-114">It's important to always find the peak transactional volume per hour.</span></span> <span data-ttu-id="205e2-115">إذا كان هناك عدة فترات ذروة، يجب عندئذٍ تحديد هذه الفترات بدقة.</span><span class="sxs-lookup"><span data-stu-id="205e2-115">If there are multiple peak periods, then these periods need to be accurately defined.</span></span>

<span data-ttu-id="205e2-116">بما أنك تفهم حمل العمل الذي يؤثر على بنيتك الأساسية، تحتاج أيضًا إلى فهم المزيد من التفاصيل حول العوامل التالية:</span><span class="sxs-lookup"><span data-stu-id="205e2-116">As you understand the load that impacts your infrastructure, you also need to understand more detail about these factors:</span></span>

- <span data-ttu-id="205e2-117">**الحركات** – تتضمن الحركات عادة ذروات معينة خلال اليوم/الأسبوع.</span><span class="sxs-lookup"><span data-stu-id="205e2-117">**Transactions** – Typically transactions have certain peaks throughout the day/week.</span></span> <span data-ttu-id="205e2-118">وهذا يتوقف بشكل أساسي على نوع الحركة.</span><span class="sxs-lookup"><span data-stu-id="205e2-118">This mostly depends on the transaction type.</span></span> <span data-ttu-id="205e2-119">تُظهر إدخالات الوقت والمصروفات عادة الذروات مرة واحدة في الأسبوع، بينما تأتي إدخالات أوامر المبيعات في أغلب الأحيان بشكل مجمع عبر التكامل أو تنتقل ببطء خلال اليوم.</span><span class="sxs-lookup"><span data-stu-id="205e2-119">Time and expense entries usually show peaks once per week, whereas Sales order entries often come in bulk via integration or trickle in during the day.</span></span>
- <span data-ttu-id="205e2-120">**عدد المستخدمين المتزامنين** - عدد المستخدمين المتزامنين هو عامل ضبط الحجم الثاني الأكثر أهمية.</span><span class="sxs-lookup"><span data-stu-id="205e2-120">**Number of concurrent users** – The number of concurrent users is the second most important sizing factor.</span></span> <span data-ttu-id="205e2-121">لا يمكنك الحصول على تقديرات ضبط الحجم بطريقة موثوقة استنادًا إلى عدد المستخدمين المتزامنين، وبالتالي إذا كانت هذه البيانات الوحيدة المتوفرة لك، فعليك تقدير رقم تقريبي، ثم معاودة زيارة هذا عندما يصبح لديك المزيد من البيانات.</span><span class="sxs-lookup"><span data-stu-id="205e2-121">You cannot reliably get sizing estimates based on the number of concurrent users, so if this is the only data you have available, estimate an approximate number, and then revisit this when you have more data.</span></span> <span data-ttu-id="205e2-122">يعني تعريف المستخدم المتزامن بطريقة متزامنة أن:</span><span class="sxs-lookup"><span data-stu-id="205e2-122">An accurate concurrent user definition means that:</span></span>

    - <span data-ttu-id="205e2-123">المستخدمين الذين لديهم اسماء ليسوا من المستخدمين المتزامنين.</span><span class="sxs-lookup"><span data-stu-id="205e2-123">Named users are not concurrent users.</span></span>
    - <span data-ttu-id="205e2-124">المستخدمين المتزامنين هم دائمًا مجموعة فرعية من المستخدمين الذين لديهم أسماء.</span><span class="sxs-lookup"><span data-stu-id="205e2-124">Concurrent users are always a subset of named users.</span></span> 
    - <span data-ttu-id="205e2-125">يحدد أقصى حمل عمل الحد الأقصى للتزامن لضبط الحجم.</span><span class="sxs-lookup"><span data-stu-id="205e2-125">Peak workload defines the maximum concurrency for sizing.</span></span>

    <span data-ttu-id="205e2-126">تعني المعايير الخاصة بالمستخدمين المتزامنين أن المستخدم يفي بكل المعايير التالية:</span><span class="sxs-lookup"><span data-stu-id="205e2-126">Criteria for concurrent users is that the user meets all the following criteria:</span></span>

    - <span data-ttu-id="205e2-127">سجل دخوله.</span><span class="sxs-lookup"><span data-stu-id="205e2-127">Logged on.</span></span>
    - <span data-ttu-id="205e2-128">عمل الحركات/الاستعلامات في وقت الجرد.</span><span class="sxs-lookup"><span data-stu-id="205e2-128">Working transactions/inquiries at the time of counting.</span></span>
    - <span data-ttu-id="205e2-129">ليست جلسة عمل خاملة.</span><span class="sxs-lookup"><span data-stu-id="205e2-129">Not an idle session.</span></span>

- <span data-ttu-id="205e2-130">**تكوين البيانات** – يتعلق هذا الخيار بشكل خاص بكيفية إعداد النظام وتكوينه.</span><span class="sxs-lookup"><span data-stu-id="205e2-130">**Data composition** – This is mostly about how your system will be set up and configured.</span></span> <span data-ttu-id="205e2-131">على سبيل المثال، عدد الكيانات القانونية التي ستكون لديك، وعدد الأصناف، وعدد مستويات قائمة مكونات الصنف ومدى تعقيد إعداد الأمان لديك.</span><span class="sxs-lookup"><span data-stu-id="205e2-131">For example, how many legal entities you will have, how many items, how many BOM levels, and how complex your security setup will be.</span></span> <span data-ttu-id="205e2-132">قد يؤثر كل واحد من هذه العوامل بشكل بسيط على الأداء، وبالتالي يمكن تعويض هذه العوامل باستخدام الخيارات الذكية عندما يتعلق الأمر بالبنية الأساسية.</span><span class="sxs-lookup"><span data-stu-id="205e2-132">Each of those factors may have a small impact on performance, so these factors can be offset by using smart choices when it comes to infrastructure.</span></span>
- <span data-ttu-id="205e2-133">**الملحقات** - بإمكان التخصيصات أن تكون بسيطة أو معقدة.</span><span class="sxs-lookup"><span data-stu-id="205e2-133">**Extensions** – Customizations can be simple or complex.</span></span> <span data-ttu-id="205e2-134">يؤثر عدد التخصيصات وطبيعة التعقيدات والاستخدام بشكل مختلف على حجم البنية الأساسية المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="205e2-134">The number of customizations and the nature of complexity and usage has a varied impact on the size of the infrastructure needed.</span></span> <span data-ttu-id="205e2-135">بالنسبة إلى التخصيصات المعقدة، من المستحسن إجراء تقييمات للأداء للتأكد من أنها لم تخضع للاختبار للتأكد من كفاءتها فحسب بل أيضًا للمساعدة في فهم احتياجات البنية الأساسية.</span><span class="sxs-lookup"><span data-stu-id="205e2-135">For complex customizations, it's advised to conduct performance evaluations to ensure that they are not only tested for efficiency but also help understand the infrastructure needs.</span></span> <span data-ttu-id="205e2-136">يكون هذا الأمر أكثر أهمية عندما لا يتم ترميز الملحقات وفقًا لأفضل الممارسات من حيث الأداء وإمكانية التوسع.</span><span class="sxs-lookup"><span data-stu-id="205e2-136">This is even more critical when the extensions are not coded according to best practices for performance and scalability.</span></span>
- <span data-ttu-id="205e2-137">**إعداد التقارير والتحليلات** - تتضمن هذه العوامل عادةً تشغيل استعلامات كبيرة في مقابل مختلف قواعد البيانات في النظام.</span><span class="sxs-lookup"><span data-stu-id="205e2-137">**Reporting and analytics** – These factors typically include running heavy queries against the various databases in the system.</span></span> <span data-ttu-id="205e2-138">سوف يساعدك فهم وخفض تكرار تشغيل التقارير المكلفة في فهم تأثيرها.</span><span class="sxs-lookup"><span data-stu-id="205e2-138">Understanding and reducing the frequency when expensive reports run will help you understand the impact of them.</span></span>
- <span data-ttu-id="205e2-139">**حلول من جهات أخرى** - هذه الحلول، مثل ISVs، لها النتائج والتوصيات نفسها كما للملحقات.</span><span class="sxs-lookup"><span data-stu-id="205e2-139">**Third-party solutions** – These solutions, like ISVs, have the same implications and recommendations as extensions.</span></span>

## <a name="sizing-your-environment"></a><span data-ttu-id="205e2-140">تغيير حجم بيئتك</span><span class="sxs-lookup"><span data-stu-id="205e2-140">Sizing your environment</span></span>

<span data-ttu-id="205e2-141">لفهم متطلبات ضبط الحجم، يجب عليك معرفة الحجم أقصى للحركات التي تحتاج إلى معالجتها.</span><span class="sxs-lookup"><span data-stu-id="205e2-141">To understand your sizing requirements, you need to know the peak volume of transactions that you need to process.</span></span> <span data-ttu-id="205e2-142">تعتبر معظم الأنظمة مساعدة، مثل أداة تقارير الإدارة‬ أو SSRS، ذات مستوى أقل من المهام الحرجة.</span><span class="sxs-lookup"><span data-stu-id="205e2-142">Most auxiliary systems, like Management Reporter or SSRS, are less mission critical.</span></span> <span data-ttu-id="205e2-143">ونتيجة لذلك، يركز هذا المستند في أغلب الأحيان على AOS وSQL Server.</span><span class="sxs-lookup"><span data-stu-id="205e2-143">As a result, this document focuses mostly on AOS and SQL Server.</span></span>

> [!NOTE]
> <span data-ttu-id="205e2-144">بشكل عام، تتوسع مستويات الحوسبة ويجب إعدادها بطراز N + 1 المناسب، مما يعني أنك إذا كنت تعمل على تقدير ثلاثة AOS، فعليك إضافة AOS رابع.</span><span class="sxs-lookup"><span data-stu-id="205e2-144">In general, the compute tiers scale out and should be set up in an N+1 fashion, meaning if you estimate three AOS, add a fourth AOS.</span></span> <span data-ttu-id="205e2-145">يجب إعداد مستوى قاعدة البيانات باختيار الإعداد "Always On العالي التوافر".</span><span class="sxs-lookup"><span data-stu-id="205e2-145">The database tier should be set up in an Always On highly-available setup.</span></span>

## <a name="sql-server-oltp"></a><span data-ttu-id="205e2-146">SQL Server (OLTP)</span><span class="sxs-lookup"><span data-stu-id="205e2-146">SQL Server (OLTP)</span></span>

### <a name="sizing"></a><span data-ttu-id="205e2-147">ضبط الحجم</span><span class="sxs-lookup"><span data-stu-id="205e2-147">Sizing</span></span>

- <span data-ttu-id="205e2-148">بنود الحركة من 3K إلى 15K في الساعة لكل مركز في خادم قاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="205e2-148">3K to 15K transaction lines per hour per core on DB server.</span></span>
- <span data-ttu-id="205e2-149">نسبة مركز AOS-to-SQL الأساسية 3:1 لـ SQL Server الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="205e2-149">Typical AOS-to-SQL core ratio 3:1 for the primary SQL Server.</span></span> <span data-ttu-id="205e2-150">الحاجة إلى مراكز إضافية استنادًا إلى تكوين التوافر العالي الذي تم اختياره.</span><span class="sxs-lookup"><span data-stu-id="205e2-150">Additional cores are required based on the chosen high availability configuration.</span></span>

    - <span data-ttu-id="205e2-151">قد تنقص معالجة عمليات قاعدة البيانات هذه النسبة إلى 2:1.</span><span class="sxs-lookup"><span data-stu-id="205e2-151">Processing database-heavy operations may regress this to 2:1.</span></span>

- <span data-ttu-id="205e2-152">تؤثر العوامل التالية على الاختلافات:</span><span class="sxs-lookup"><span data-stu-id="205e2-152">The following factors influence variations:</span></span>

    - <span data-ttu-id="205e2-153">إعدادات المحددات قيد الاستخدام.</span><span class="sxs-lookup"><span data-stu-id="205e2-153">Parameter settings in use.</span></span>
    - <span data-ttu-id="205e2-154">مستويات الملحقات.</span><span class="sxs-lookup"><span data-stu-id="205e2-154">Levels of extensions.</span></span>
    - <span data-ttu-id="205e2-155">استخدام وظائف إضافية، مثل سجل وتنبيهات قاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="205e2-155">Usage of additional functionality, such as database log and alerts.</span></span> <span data-ttu-id="205e2-156">ستؤدي عمليات تسجيل الدخول القصوى إلى قاعدة البيانات إلى تقليل الإنتاجية في الساعة لكل مركز إلى أقل من بنود 3K.</span><span class="sxs-lookup"><span data-stu-id="205e2-156">Extreme database logging will further reduce throughput per hour per core below 3K lines.</span></span>
    - <span data-ttu-id="205e2-157">تعقيدات تركيب البيانات - دليل حسابات بسيط في مقابل دليل حسابات ذي تفاصيل دقيقة لديه نتائج على الإنتاجية (كمثال).</span><span class="sxs-lookup"><span data-stu-id="205e2-157">Complexity of data composition – A simple chart of accounts versus a detailed fine-grained chart of accounts has implications on throughput (as an example).</span></span>
    - <span data-ttu-id="205e2-158">وصف الحركة.</span><span class="sxs-lookup"><span data-stu-id="205e2-158">Transaction characterization.</span></span>
    - <span data-ttu-id="205e2-159">ذاكرة سعتها من 2 غيغابايت إلى 16 جيجابايت لكل مركز.</span><span class="sxs-lookup"><span data-stu-id="205e2-159">2 GB to 16 GB memory for each core.</span></span>
    - <span data-ttu-id="205e2-160">قواعد بيانات مساعدة على خادم قاعدة البيانات مثل قواعد بيانات أداة تقارير الإدارة وSSRS.</span><span class="sxs-lookup"><span data-stu-id="205e2-160">Auxiliary databases on DB server such as Management reporter and SSRS databases.</span></span>
    - <span data-ttu-id="205e2-161">قاعدة البيانات المؤقتة = 15% من حجم قاعدة البيانات، مع عدد من الملفات بقدر عدد المعالجات المادية.</span><span class="sxs-lookup"><span data-stu-id="205e2-161">Temp DB = 15% of DB size, with as many files as physical processors.</span></span>
    - <span data-ttu-id="205e2-162">حجم شبكة SAN وسرعة نقل البيانات استنادًا إلى الحجم الإجمالي/استخدام الحركات المتزامنة.</span><span class="sxs-lookup"><span data-stu-id="205e2-162">SAN size and throughput based on total concurrent transaction volume/usage.</span></span>

### <a name="high-availability"></a><span data-ttu-id="205e2-163">التوافر العالي</span><span class="sxs-lookup"><span data-stu-id="205e2-163">High availability</span></span>

<span data-ttu-id="205e2-164">نوصي دائمًا باستخدام SQL Server في نظام مجموعة أو إعداد نسخ مطابق.</span><span class="sxs-lookup"><span data-stu-id="205e2-164">We recommend always utilizing SQL Server in either a cluster or mirroring setup.</span></span> <span data-ttu-id="205e2-165">يجب أن تتضمن عقدة SQL الثانية عدد المراكز نفسه كما في العقدة الأساسية.</span><span class="sxs-lookup"><span data-stu-id="205e2-165">The second SQL node should have the same number of cores as the primary node.</span></span>

### <a name="active-directory-federation-services-ad-fs"></a><span data-ttu-id="205e2-166">خدمات الأمان المشترك لـ Active Directory (AD FS)</span><span class="sxs-lookup"><span data-stu-id="205e2-166">Active Directory Federation Services (AD FS)</span></span>

<span data-ttu-id="205e2-167">بالنسبة إلى ضبط حجم AD FS، راجع [وثائق القدرة الإنتاجية لخادم AD FS](/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity).</span><span class="sxs-lookup"><span data-stu-id="205e2-167">For AD FS sizing, see the [AD FS Server Capacity documentation](/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity).</span></span>

<span data-ttu-id="205e2-168">يتوفر [جدول بيانات ضبط الحجم](https://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx) لتخطيط عدد المثيلات في عملية النشر.</span><span class="sxs-lookup"><span data-stu-id="205e2-168">A [sizing spreadsheet](https://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx) is available for planning the number of instances in your deployment.</span></span>

## <a name="aos-online-and-batch"></a><span data-ttu-id="205e2-169">AOS (عبر الإنترنت ودُفعة)</span><span class="sxs-lookup"><span data-stu-id="205e2-169">AOS (Online and batch)</span></span>

### <a name="sizing"></a><span data-ttu-id="205e2-170">ضبط الحجم</span><span class="sxs-lookup"><span data-stu-id="205e2-170">Sizing</span></span>

- <span data-ttu-id="205e2-171">ضبط الحجم حسب حجم/استخدام الحركة</span><span class="sxs-lookup"><span data-stu-id="205e2-171">Sizing by transaction volume/usage</span></span>

    - <span data-ttu-id="205e2-172">بنود 2K إلى 6K لكل مركز</span><span class="sxs-lookup"><span data-stu-id="205e2-172">2K to 6K lines per core</span></span>
    - <span data-ttu-id="205e2-173">16 غيغابايت لكل مثيل</span><span class="sxs-lookup"><span data-stu-id="205e2-173">16 GB per instance</span></span>
    - <span data-ttu-id="205e2-174">صندوق قياسي- من 4 مراكز إلى 24 مركزًا</span><span class="sxs-lookup"><span data-stu-id="205e2-174">Standard box – 4 to 24 cores</span></span>
    - <span data-ttu-id="205e2-175">من 10 إلى 15 مستخدم Enterprise لكل مركز</span><span class="sxs-lookup"><span data-stu-id="205e2-175">10 to 15 Enterprise users per core</span></span>
    - <span data-ttu-id="205e2-176">من 15 إلى 25 مستخدم Activity لكل مركز</span><span class="sxs-lookup"><span data-stu-id="205e2-176">15 to 25 Activity users per core</span></span>
    - <span data-ttu-id="205e2-177">من 25 إلى 50 مستخدم Team لكل مركز</span><span class="sxs-lookup"><span data-stu-id="205e2-177">25 to 50 Team members per core</span></span>

- <span data-ttu-id="205e2-178">الدُفعة</span><span class="sxs-lookup"><span data-stu-id="205e2-178">Batch</span></span>

    - <span data-ttu-id="205e2-179">من 1 إلى 4 سلاسل مجموعة لكل مركز</span><span class="sxs-lookup"><span data-stu-id="205e2-179">1 to 4 batch threads per core</span></span>
    - <span data-ttu-id="205e2-180">الحجم استنادًا إلى وصف نافذة الدُفعة</span><span class="sxs-lookup"><span data-stu-id="205e2-180">Size based on batch window characterization</span></span>

- <span data-ttu-id="205e2-181">لاحظ أن AOS وإدارة البيانات والدُفعة موجودة على نفس دور في Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="205e2-181">Note that the AOS, Data Management, and Batch are on the same role in the Service Fabric.</span></span> <span data-ttu-id="205e2-182">إنك تحتاج إلى ضبط حجم أحمال العمل الثلاثة هذه مجتمعة، وليس فصلها كما في Microsoft Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="205e2-182">You need to size for these three workloads combined, and not separate these like in Microsoft Dynamics AX 2012.</span></span>
- <span data-ttu-id="205e2-183">تنطبق هنا عوامل الاختلاف نفسها لـ SQL Server.</span><span class="sxs-lookup"><span data-stu-id="205e2-183">The same variability factors for SQL Server apply here.</span></span>

### <a name="high-availability"></a><span data-ttu-id="205e2-184">التوافر العالي</span><span class="sxs-lookup"><span data-stu-id="205e2-184">High availability</span></span>

- <span data-ttu-id="205e2-185">تأكد من توفر 1 إلى 2 خادم AOS أكثر مما قدّرته على الأقل.</span><span class="sxs-lookup"><span data-stu-id="205e2-185">Ensure that you have at least 1 to 2 more AOS available than you estimate.</span></span>
- <span data-ttu-id="205e2-186">تأكد من توفر 3 إلى 4 من الأجهزة المضيفة على الأقل.</span><span class="sxs-lookup"><span data-stu-id="205e2-186">Ensure that you have at least 3 to 4 virtual hosts available.</span></span>

## <a name="management-reporter"></a><span data-ttu-id="205e2-187">أداة تقارير الإدارة</span><span class="sxs-lookup"><span data-stu-id="205e2-187">Management reporter</span></span>

<span data-ttu-id="205e2-188">في معظم الحالات، من المفترض أن يعمل الحد الأدنى من المتطلبات الموصى بها باستخدام عقدتين بشكل جيد.</span><span class="sxs-lookup"><span data-stu-id="205e2-188">In most cases, unless used extensively, the recommended minimum requirements using two nodes should work well.</span></span> <span data-ttu-id="205e2-189">سوف تحتاج إلى أكثر من عقدتين فقط في الحالات حيث يكون الاستخدام كثيفًا.</span><span class="sxs-lookup"><span data-stu-id="205e2-189">Only in cases where there is heavy use will you need more than two nodes.</span></span> <span data-ttu-id="205e2-190">يُرجى التوسع حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="205e2-190">Please scale as needed.</span></span>

## <a name="sql-server-reporting-services"></a><span data-ttu-id="205e2-191">خدمات تقارير SQL Server</span><span class="sxs-lookup"><span data-stu-id="205e2-191">SQL Server Reporting Services</span></span>

<span data-ttu-id="205e2-192">بالنسبة إلى إصدار التوفر العام، يمكن نشر عقده SSRS واحدة فقط.</span><span class="sxs-lookup"><span data-stu-id="205e2-192">For the general availability release, only one SSRS node can be deployed.</span></span> <span data-ttu-id="205e2-193">راقب عقده SSRS أثناء الاختبار، واعمل على زيادة عدد المراكز المتاحة لـ SSRS بحسب الاحتياجات.</span><span class="sxs-lookup"><span data-stu-id="205e2-193">Monitor your SSRS node while testing and increase the number of cores available for SSRS on a need basis.</span></span> <span data-ttu-id="205e2-194">تأكد من أن لديك عقدة ثانوية تم تكوينها مسبقًا متوفرة على مضيف ظاهري يختلف عن SSRS VM.</span><span class="sxs-lookup"><span data-stu-id="205e2-194">Make sure that you have a preconfigured secondary node available on a virtual host that is different than the SSRS VM.</span></span> <span data-ttu-id="205e2-195">يعتبر هذا مهمًا إذا كان هناك مشكلة في الجهاز الظاهري الذي يستضيف SSRS أو المضيف الظاهري.</span><span class="sxs-lookup"><span data-stu-id="205e2-195">This is important if there is an issue with the virtual machine that hosts SSRS or the virtual host.</span></span> <span data-ttu-id="205e2-196">إذا كان الأمر كذلك، فقد يلزم استبدالها.</span><span class="sxs-lookup"><span data-stu-id="205e2-196">If this the case, they would need to be replaced.</span></span>

## <a name="environment-orchestrator"></a><span data-ttu-id="205e2-197">منسق البيئة</span><span class="sxs-lookup"><span data-stu-id="205e2-197">Environment Orchestrator</span></span>

<span data-ttu-id="205e2-198">إن خدمة المنسق هي الخدمة التي تعمل على إدارة عملية النشر والاتصالات ذات الصلة بـ LCS.</span><span class="sxs-lookup"><span data-stu-id="205e2-198">The Orchestrator service is the service that manages your deployment and the related communication with LCS.</span></span> <span data-ttu-id="205e2-199">يتم نشر الخدمة كخدمة Service Fabric الأساسية وتتطلب ثلاثة أجهزة ظاهرية على الأقل.</span><span class="sxs-lookup"><span data-stu-id="205e2-199">This service is deployed as the primary Service Fabric service and requires at least three VMs.</span></span> <span data-ttu-id="205e2-200">تقع هذه الخدمة في موقع مشترك مع خدمات تنسيق Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="205e2-200">This service is co-located with the Service Fabric orchestration services.</span></span> <span data-ttu-id="205e2-201">ويجب أن يتم ضبط حجم ذلك لحمل العمل الأقصى في نظام المجموعة.</span><span class="sxs-lookup"><span data-stu-id="205e2-201">This and should be sized to the peak load of the cluster.</span></span> <span data-ttu-id="205e2-202">لمزيد من المعلومات، راجع [تخطيط وإعداد نشر مجموعة Service Fabric مستقلة](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).</span><span class="sxs-lookup"><span data-stu-id="205e2-202">For more information, see [Plan and prepare your Service Fabric Standalone cluster deployment](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).</span></span>

## <a name="virtualization-and-oversubscription"></a><span data-ttu-id="205e2-203">المحاكاة الافتراضية والاشتراك الزائد</span><span class="sxs-lookup"><span data-stu-id="205e2-203">Virtualization and oversubscription</span></span>

<span data-ttu-id="205e2-204">يجب أن تتم استضافة الخدمات ذات المهام الحرجة مثل AOS على الأجهزة الظاهرية المضيفة التي تم تخصيص موارد لها - المراكز والذاكرة والقرص.</span><span class="sxs-lookup"><span data-stu-id="205e2-204">Mission critical services like the AOS should be hosted on Virtual hosts that have dedicated resources – cores, memory, and disk.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]