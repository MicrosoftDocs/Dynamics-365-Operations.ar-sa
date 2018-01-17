---
title: "إعادة تعيين متجر بيانات للتقارير المالية"
description: "يشرح هذا الموضوع كيفية إعادة تعيين متجر بيانات التقارير المالية."
author: aolson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: aloson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 5b956dcc5a4a93033396ae0ffcf8b7aeba2cf3f2
ms.openlocfilehash: a07e8b5bae2c4f71e9212cd2f8080d2481769818
ms.contentlocale: ar-sa
ms.lasthandoff: 12/14/2017

---

# <a name="reset-the-financial-reporting-data-mart"></a><span data-ttu-id="9b3c0-103">إعادة تعيين متجر بيانات للتقارير المالية</span><span class="sxs-lookup"><span data-stu-id="9b3c0-103">Reset the Financial reporting data mart</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9b3c0-104">يشرح هذا الموضوع كيفية إعادة تعيين متجر بيانات التقارير المالية للإصدارات التالية:</span><span class="sxs-lookup"><span data-stu-id="9b3c0-104">This topic explains how to reset the Financial reporting data mart for the following versions:</span></span>

- <span data-ttu-id="9b3c0-105">إصدار التقارير المالية في Microsoft Dynamics 365 for Finance and Operations رقم 7.2.6.0 وإصدار أحدث</span><span class="sxs-lookup"><span data-stu-id="9b3c0-105">Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.2.6.0 and later</span></span>
- <span data-ttu-id="9b3c0-106">إصدار التقارير المالية في Microsoft Dynamics 365 for Finance and Operations رقم 7.0.10000.4 وإصدار أحدث</span><span class="sxs-lookup"><span data-stu-id="9b3c0-106">Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.0.10000.4 and later</span></span>
- <span data-ttu-id="9b3c0-107">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (محلي)</span><span class="sxs-lookup"><span data-stu-id="9b3c0-107">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (on-premises)</span></span>

<span data-ttu-id="9b3c0-108">‏‫للحصول على إصدار التقارير المالية 7.2.6.0 لـ Finance and Operations، يمكنك تنزيل قاعدة المعارف KB 4052514 من <https://fix.lcs.dynamics.com/Issue/Resolved?kb=4052514>.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-108">To get Finance and Operations Financial reporting release 7.2.6.0, you can download KB 4052514 from <https://fix.lcs.dynamics.com/Issue/Resolved?kb=4052514>.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-7260-and-later"></a><span data-ttu-id="9b3c0-109">إعادة تعيين متجر بيانات التقارير المالية لإصدار التقارير المالية لـ Finance and Operations رقم 7.2.6.0 أو إصدار أحدث</span><span class="sxs-lookup"><span data-stu-id="9b3c0-109">Reset the Financial reporting data mart for Finance and Operations Financial reporting release 7.2.6.0 and later</span></span>

### <a name="reset-the-financial-reporting-data-mart-from-report-designer"></a><span data-ttu-id="9b3c0-110">إعادة تعيين متجر بيانات التقارير المالية من مصمم التقارير</span><span class="sxs-lookup"><span data-stu-id="9b3c0-110">Reset the Financial reporting data mart from Report designer</span></span>

> [!NOTE]
> <span data-ttu-id="9b3c0-111">الخطوات المذكورة في هذه العملية مدعومة لإصدار التقارير المالية لـ Finance and Operations رقم 7.2.6.0 وإصدار أحدث.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-111">The steps in this process are supported for Finance and Operations Financial reporting release 7.2.6.0 and later.</span></span> <span data-ttu-id="9b3c0-112">إذا كان لديك إصدار سابق، فاتصل بفريق الدعم للحصول على المساعدة.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-112">If you have an earlier release, contact the Support team for assistance.</span></span>

<span data-ttu-id="9b3c0-113">في السيناريوهات المحددة، قد تحتاج إلى إعادة تعيين متجر البيانات للتقارير المالية.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-113">In specific scenarios, you might have to reset the data mart for Financial reporting.</span></span> <span data-ttu-id="9b3c0-114">يمكنك إكمال هذه المهمة في عميل مصمم التقارير.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-114">You can complete this task in the Report designer client.</span></span> <span data-ttu-id="9b3c0-115">فيما يلي بعض السيناريوهات التي قد تحتاج إلى إعادة تعيين متجر البيانات:</span><span class="sxs-lookup"><span data-stu-id="9b3c0-115">Here are some scenarios where you might have to reset the data mart:</span></span>

- <span data-ttu-id="9b3c0-116">تمت استعادة قاعدة بيانات Finance and Operations، ولكن لم تتم استعادة قاعدة بيانات متجر البيانات.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-116">The Finance and Operations database was restored, but the data mart database wasn't restored.</span></span>
- <span data-ttu-id="9b3c0-117">تشاهد بيانات غير صحيحة لفترة.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-117">You see incorrect data for a period.</span></span>
- <span data-ttu-id="9b3c0-118">يرشدك الدعم إلى إعادة تعيين متجر البيانات كجزء من إحدى خطوات استكشاف الأخطاء وإصلاحها.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-118">Support instructs you to reset the data mart as part of a troubleshooting step.</span></span>

<span data-ttu-id="9b3c0-119">يجب ألا تتم إعادة تعيين متجر البيانات إلا عندما يكون مقدار المعالجة في قاعدة البيانات صغيرًا.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-119">The data mart reset should be done only during times when the amount of processing on the database is small.</span></span> <span data-ttu-id="9b3c0-120">لن تتوفر التقارير المالية أثناء عملية إعادة التعيين.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-120">Financial reporting will be unavailable during the reset process.</span></span>

#### <a name="reset-the-data-mart"></a><span data-ttu-id="9b3c0-121">إعادة تعيين متجر البيانات</span><span class="sxs-lookup"><span data-stu-id="9b3c0-121">Reset the data mart</span></span>

<span data-ttu-id="9b3c0-122">لإعادة تعيين متجر البيانات، في مصمم التقرير، على القائمة **أدوات**، حدد **إعادة تعيين متجر البيانات**.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-122">To reset the data mart, in Report designer, on the **Tools** menu, select **Reset Data Mart**.</span></span> <span data-ttu-id="9b3c0-123">يحتوي مربع الحوار الذي يظهر على قسمين: **الإحصاءات** و**إعادة التعيين**.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-123">The dialog box that appears has two sections: **Statistics** and **Reset**.</span></span>

<span data-ttu-id="9b3c0-124">[![إعادة تعيين مربع حوار متجر البيانات](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span><span class="sxs-lookup"><span data-stu-id="9b3c0-124">[![Reset Data Mart dialog box](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span></span>

##### <a name="integration-attempts"></a><span data-ttu-id="9b3c0-125">محاولات التكامل:</span><span class="sxs-lookup"><span data-stu-id="9b3c0-125">Integration attempts</span></span>

<span data-ttu-id="9b3c0-126">تعرض شبكة **محاولات التكامل** عدد المرات محاولة النظام دمج الحركات.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-126">The **Integration attempts** grid shows how many times the system has tried to integrate transactions.</span></span> <span data-ttu-id="9b3c0-127">يواصل النظام محاولة تكامل البيانات خلال فترة من الأيام إذا لم تنجح المحاولات القليلة الأولى.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-127">The system continues to try to integrate data over a period of days if the first few attempts aren't successful.</span></span> <span data-ttu-id="9b3c0-128">ستعرف أنه يجب إعادة تعيين متجر البيانات إذا كان عدد المحاولات 8 أو أكثر، وإذا كان لديك العديد من مجموعات الأبعاد أو سجلات الحركات.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-128">You will know that the data mart must be reset is if the number of attempts is 8 or more, and if there are many Dimension combination or Transaction records.</span></span> <span data-ttu-id="9b3c0-129">في هذه الحالة، لن يتم الإبلاغ عن البيانات.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-129">In this situation, the data won't be reported on.</span></span>

##### <a name="data-status"></a><span data-ttu-id="9b3c0-130">حالة البيانات</span><span class="sxs-lookup"><span data-stu-id="9b3c0-130">Data status</span></span>

<span data-ttu-id="9b3c0-131">توفر شبكة **حالة البيانات** لقطة للحركات وأسعار الصرف وقيم الأبعاد في متجر البيانات.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-131">The **Data status** grid provides a snapshot of the transactions, exchange rates, and dimension values in the data mart.</span></span> <span data-ttu-id="9b3c0-132">يشير عدد كبير من السجلات التالفة إلى التحديثات الهائلة التي تم إجراؤها على السجلات.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-132">A large number of stale records indicates that numerous updates to the records have occurred.</span></span> <span data-ttu-id="9b3c0-133">قد يتسبب هذا الموقف في ظهور أوقات إنشاء تقارير أبطأ.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-133">This situation might cause slower report generation times.</span></span>

##### <a name="misaligned-main-account-categories"></a><span data-ttu-id="9b3c0-134">فئات الحساب الرئيسي التي تمت محاذاتها بشكل غير صحيح</span><span class="sxs-lookup"><span data-stu-id="9b3c0-134">Misaligned main account categories</span></span>

<span data-ttu-id="9b3c0-135">إذا كنت تستخدم إصدار أقدم من إصدار التقارير المالية 7.2.1 لـ Microsoft Dynamics 365 for Finance and Operations، فقد تضطر إلى إعادة تعيين متجر البيانات إذا قمت بإعادة تسمية حسابات ونقلها بين فئات الحسابات.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-135">If you're using a release that is earlier than Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.2.1, you might have to reset the data mart if you rename accounts and move accounts between account categories.</span></span> <span data-ttu-id="9b3c0-136">قد تؤدي هذه الإجراءات إلى محاذاة فئات الحسابات الرئيسية بطريقة خاطئة.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-136">These actions can cause main account categories to become misaligned.</span></span> <span data-ttu-id="9b3c0-137">يعرض حقل **فئات الحسابات الرئيسية التي تمت محاذاتها طريقة خاطئة** ما إذا كنت تواجه هذه المشكلة أو لا.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-137">The **Misaligned main account categories** field shows whether you're experiencing that issue.</span></span>

### <a name="reset-the-data-mart-in-finance-and-operations-financial-reporting-release-7260"></a><span data-ttu-id="9b3c0-138">إعادة تعيين متجر البيانات في إصدار التقارير المالية 7.2.6.0 لـ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9b3c0-138">Reset the data mart in Finance and Operations Financial reporting release 7.2.6.0</span></span>

<span data-ttu-id="9b3c0-139">لإعادة تعيين متجر البيانات في إصدار التقارير المالية 7.2.6.0 لـ Finance and Operations والإصدارات السابقة له، في مربع الحوار **"إعادة تعيين متجر البيانات"**، حدد خانة الاختيار **إعادة تعيين متجر البيانات**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-139">To reset the data mart in Finance and Operations Financial reporting release 7.2.6.0 and earlier, in the **Reset Data Mart** dialog box, select the **Reset data mart** check box, and then select **OK**.</span></span> <span data-ttu-id="9b3c0-140">يجب عليك إعادة تعيين متجر البيانات فقط أثناء وقت التعطل المجدول.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-140">You should reset the data mart only during scheduled downtime.</span></span>

<span data-ttu-id="9b3c0-141">[![إعادة تعيين خانة اختيار متجر البيانات](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span><span class="sxs-lookup"><span data-stu-id="9b3c0-141">[![Reset data mart check box](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span></span>

### <a name="reset-the-data-mart-and-select-a-reason-in-microsoft-dynamics-365-for-finance-and-operations-financial-reporting-release-730"></a><span data-ttu-id="9b3c0-142">إعادة تعيين متجر البيانات وتحديد أحد الأسباب في إصدار التقارير المالية 7.3.0 لـ Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9b3c0-142">Reset the data mart and select a reason in Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.3.0</span></span>

<span data-ttu-id="9b3c0-143">إذا وجدت أن إعادة تعيين متجر بيانات مطلوبة، فحدد خانة الاختيار **إعادة تعيين متجر البيانات**، ثم حدد أحد الأسباب في حقل **السبب**.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-143">If you determine that a data mart reset is required, select the **Reset data mart** check box, and then select a reason in the **Reason** field.</span></span> <span data-ttu-id="9b3c0-144">يتوفر الخياران التاليان:</span><span class="sxs-lookup"><span data-stu-id="9b3c0-144">The following options are available:</span></span>

- <span data-ttu-id="9b3c0-145">**البيانات المفقودة أو غير الصحيحة** -وفقًا للإحصاءات، لقد حددت أنك البيانات قد تكون مفقودة.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-145">**Missing or incorrect data** – Based on the statistics, you've determined that data might be missing.</span></span> <span data-ttu-id="9b3c0-146">قبل المتابعة، نوصي بأن تعمل مع الدعم لتحديد السبب الجذري.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-146">Before you continue, we recommend that you work with Support to determine the root cause.</span></span>
- <span data-ttu-id="9b3c0-147">**استعادة قاعدة البيانات** – تمت استعادة قاعدة بيانات Finance and Operations، ولكن لم تتم استعادة قاعدة البيانات لمتجر بيانات التقارير المالية.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-147">**Restore database** – The Finance and Operations database was restored, but the database for the Financial reporting data mart wasn't restored.</span></span>
- <span data-ttu-id="9b3c0-148">**أخرى** -في حالة إعادة تعيين متجر البيانات لسبب آخر.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-148">**Other** – You're resetting the data mart for another reason.</span></span> <span data-ttu-id="9b3c0-149">إذا كنت معنياً بأن هناك مشكلة، فاتصل بالدعم للتعرف عليها.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-149">If you're concerned that there is an issue, contact Support to identify it.</span></span>

<span data-ttu-id="9b3c0-150">[![إعادة تعيين متجر البيانات](./media/Integration.png)](./media/Integration.png)</span><span class="sxs-lookup"><span data-stu-id="9b3c0-150">[![Reset data mart](./media/Integration.png)](./media/Integration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="9b3c0-151">تحقق أن جميع مهام إعادة تعيين متجر البيانات قد أكملت تحميل أولي قبل أن تبدأ إعادة تعيين.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-151">Verify that all data mart reset tasks have completed an initial load before you begin a reset.</span></span> <span data-ttu-id="9b3c0-152">يمكنك تأكيد ذلك عن طريق البحث عن قيمة في العمود "‏‫وقت آخر تشغيل‬" عن طريق تحديد **أدوات** &gt; **حالة التكامل**.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-152">You can confirm this by looking for a value in the Last Runtime column by selecting **Tools** &gt; **Integration status**.</span></span>

#### <a name="clear-users-and-companies"></a><span data-ttu-id="9b3c0-153">مسح المستخدمين والشركات</span><span class="sxs-lookup"><span data-stu-id="9b3c0-153">Clear users and companies</span></span>

<span data-ttu-id="9b3c0-154">حدد خانة الاختيار **إلغاء تحديد المستخدمين والشركات** في حالة استعادة قاعدة البيانات الخاصة بك، ولكن قمت بعد ذلك إجراء أي تغييرات على المستخدمين أو الشركات.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-154">Select the **Clear users and companies** check box if you restored your database, but you then made changes to users or companies.</span></span> <span data-ttu-id="9b3c0-155">يجب ألا تحدد خانة الاختيار هذه إلا في النادر.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-155">You should rarely have to select this check box.</span></span>

<span data-ttu-id="9b3c0-156">عندما تكون مستعدًا لبدء عملية إعادة التعيين، حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-156">When you're ready to start the reset process, select **OK**.</span></span> <span data-ttu-id="9b3c0-157">أنت مطالب بتأكيد أنك مستعد لبدء العملية.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-157">You're prompted to confirm that you're ready to start the process.</span></span> <span data-ttu-id="9b3c0-158">تجدر الإشارة إلى أن التقارير المالية لن تتوفر أثناء إعادة التعيين وتكامل البيانات الأولية التي تحدث بعد ذلك.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-158">Note that Financial reporting won't be available during the reset and the initial data integration that occurs afterward.</span></span>

<span data-ttu-id="9b3c0-159">إذا كنت ترغب في مراجعة حالة التكامل، فحدد **أدوات**&gt;**حالة التكامل** لمشاهدة آخر مرة تم تشغيل التكامل فيها وحالة ذلك.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-159">If you want to review the status of the integration, select **Tools** &gt; **Integration status** to see the last time that the integration was run and the status.</span></span>

<span data-ttu-id="9b3c0-160">[![عرض حالة التكامل](./media/New-integration.PNG)](./media/New-integration.PNG)</span><span class="sxs-lookup"><span data-stu-id="9b3c0-160">[![View the status of the integration](./media/New-integration.PNG)](./media/New-integration.PNG)</span></span>

> [!NOTE]
> <span data-ttu-id="9b3c0-161">تنتهي عملية إعادة التعيين عند إظهار كافة التعيينات في الحالة RanToCompletion وظهور "‏‫اكتمل التكامل" في نافذة "حالة التكامل" في الركن السفلي الأيمن.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-161">The reset is finished when all mappings show the status of RanToCompletion and the Integration Status window says “Integration complete” in the bottom-left corner.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-70100004-and-later"></a><span data-ttu-id="9b3c0-162">إعادة تعيين متجر بيانات التقارير المالية لإصدار التقارير المالية لـ Finance and Operations رقم 7.0.10000.4 أو إصدار أحدث</span><span class="sxs-lookup"><span data-stu-id="9b3c0-162">Reset the Financial reporting data mart for Finance and Operations Financial reporting release 7.0.10000.4 and later</span></span>

<span data-ttu-id="9b3c0-163">إذا قمت في أي وقت باستعادة قاعدة بيانات Finance and Operations من نسخة احتياطية أو نسخ قاعدة البيانات من بيئة أخرى، فيجب اتباع الخطوات الواردة في هذا الموضوع للمساعدة على ضمان أن متجر بيانات التقارير المالية يستخدم قاعدة بيانات Finance and Operations التي تمت استعادتها بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-163">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this section to help guarantee that the Financial reporting data mart correctly uses the restored Finance and Operations database.</span></span>

> [!NOTE]
> <span data-ttu-id="9b3c0-164">الخطوات الواردة في هذه العملية مدعومة لإصدار 7.0.1 من تطبيق Microsoft Dynamics AX (مايو 2016) (إصدار التطبيق 7.0.1265.23014 وإصدار التقارير المالية 7.0.10000.4) والإصدار الأحدث.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-164">The steps in this process are supported for Microsoft Dynamics AX application version 7.0.1 (May 2016) (application build 7.0.1265.23014 and Financial reporting build 7.0.10000.4) and later.</span></span> <span data-ttu-id="9b3c0-165">إذا كان لديك إصدار سابق من Finance and Operations، فاتصل بفريق الدعم للمساعدة.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-165">If you have an earlier version of Finance and Operations, contact Support for assistance.</span></span>

### <a name="export-report-definitions"></a><span data-ttu-id="9b3c0-166">تصدير تعريفات التقارير</span><span class="sxs-lookup"><span data-stu-id="9b3c0-166">Export report definitions</span></span>

<span data-ttu-id="9b3c0-167">أولاً، اتبع هذه الخطوات لتصدير تصميمات التقارير من "مصمم التقارير".</span><span class="sxs-lookup"><span data-stu-id="9b3c0-167">First, follow these steps to export the report designs from Report designer.</span></span>

1. <span data-ttu-id="9b3c0-168">في مصمم التقارير، حدد **الشركة** &gt; **مجموعات كتل الإنشاء**.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-168">In Report designer, select **Company** &gt; **Building Block Groups**.</span></span>
2. <span data-ttu-id="9b3c0-169">حدد مجموعة كتلة الإنشاء لتصديرها، ثم حدد **تصدير**.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-169">Select the building block group to export, and then select **Export**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9b3c0-170">ملاحظة: بالنسبة إلى Finance and Operations، يتم دعم مجموعة واحدة فقط من كتل الإنشاء، وهي المجموعة **الافتراضية**.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-170">For Finance and Operations, only one building block group is supported, **Default**.</span></span>

3. <span data-ttu-id="9b3c0-171">حدد تعريفات التقارير لتصديرها:</span><span class="sxs-lookup"><span data-stu-id="9b3c0-171">Select the report definitions to export:</span></span>

    - <span data-ttu-id="9b3c0-172">لتصدير كل تعريفات التقارير وكتل الإنشاء المقترنة، حدد **تحديد الكل**.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-172">To export all your report definitions and the associated building blocks, select **Select All**.</span></span>
    - <span data-ttu-id="9b3c0-173">لتصدير مجموعات محددة من التقارير أو الصفوف أو الأعمدة أو الأشجار أو الأبعاد، حدد علامة التبويب المناسبة ثم حدد العناصر المراد تصديرها.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-173">To export specific reports, rows, columns, trees, or dimension sets, select the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="9b3c0-174">اضغط باستمرار على المفتاح Ctrl لتحديد عدة عناصر على علامة تبويب. عندما تحدد تقارير لتصديرها، سيتم تحديد الصفوف والأعمدة والأشجار ومجموعات الأبعاد ذات الصلة.‬</span><span class="sxs-lookup"><span data-stu-id="9b3c0-174">Press and hold the Ctrl key to select multiple items on a tab. When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4. <span data-ttu-id="9b3c0-175">حدد **تصدير**.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-175">Select **Export**.</span></span>
5. <span data-ttu-id="9b3c0-176">أدخل اسم ملف وحدد موقعًا آمنًا حيث تريد حفظ تعريفات التقارير التي تم تصديرها.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-176">Enter a file name, and select a secure location where you want to save the exported report definitions.</span></span>
6. <span data-ttu-id="9b3c0-177">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-177">Select **Save**.</span></span>

<span data-ttu-id="9b3c0-178">يمكنك نسخ أو تحميل الملف إلى موقع آمن.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-178">You can copy or upload the file to a secure location.</span></span> <span data-ttu-id="9b3c0-179">وبهذه الطريقة، يمكن استيراد الملف في بيئة مختلفة فيما بعد.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-179">In this way, the file can be imported into a different environment later.</span></span> <span data-ttu-id="9b3c0-180">لمزيد من المعلومات حول كيفية استخدام حساب Microsoft Azure storage، راجع [نقل البيانات باستخدام أداة سطر الأوامر المساعدة AzCopy](/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="9b3c0-180">For information about how to use a Microsoft Azure storage account, see [Transfer data with the AzCopy Command-Line Utility](/azure/storage/storage-use-azcopy).</span></span>

> [!NOTE]
> <span data-ttu-id="9b3c0-181">لا تقدم Microsoft حساب تخزين كجزء من اتفاقية Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-181">Microsoft doesn't provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="9b3c0-182">يجب عليك شراء حساب تخزين أو استخدام حساب تخزين من اشتراك Azure منفصل.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-182">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span>

> [!WARNING]
> <span data-ttu-id="9b3c0-183">يجب مراعاة سلوك محرك الأقراص D على أجهزة Azure الظاهرية (VMs).</span><span class="sxs-lookup"><span data-stu-id="9b3c0-183">Be aware of the behavior of drive D on Azure virtual machines (VMs).</span></span> <span data-ttu-id="9b3c0-184">لا تقم بشكل دائم بتخزين مجموعة الكتل البرمجية الإنشائية المُصدَر الخاصة بك على محرك الأقراص D. وللحصول على مزيد من المعلومات حول محركات الأقراص المؤقتة، راجع [التعرف على محرك الأقراص المؤقت على الأجهزة الظاهرية من Windows Azure](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span><span class="sxs-lookup"><span data-stu-id="9b3c0-184">Don't permanently store your exported building block groups on drive D. For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

### <a name="stop-services"></a><span data-ttu-id="9b3c0-185">وقف الخدمات</span><span class="sxs-lookup"><span data-stu-id="9b3c0-185">Stop services</span></span>

<span data-ttu-id="9b3c0-186">سيكون لخدمات Microsoft Windows التالية اتصالات مفتوحة بقاعدة بيانات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-186">The following Microsoft Windows services will have open connections to the Finance and Operations database.</span></span> <span data-ttu-id="9b3c0-187">ولذلك، يجب عليك استخدام سطح المكتب البعيد من Microsoft للاتصال بجميع أجهزة الكمبيوتر الموجودة في البيئة، ثم استخدام services.msc لإيقاف هذه الخدمات.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-187">Therefore, you must use Microsoft Remote Desktop to connect to all the computers in the environment and then use services.msc to stop these services.</span></span>

- <span data-ttu-id="9b3c0-188">خدمة النشر على شبكة الإنترنت العالمية (على جميع أجهزة الكمبيوتر التي تعمل بنظام خوادم كائنات التطبيقات [AOS])</span><span class="sxs-lookup"><span data-stu-id="9b3c0-188">World wide web publishing service (on all Application Object Servers [AOS] computers)</span></span>
- <span data-ttu-id="9b3c0-189">خدمة إدارة الدفعة لـ Microsoft Dynamics 365 for Finance and Operations (على أجهزة الكمبيوتر التي لا تعمل بنظام AOS فقط)</span><span class="sxs-lookup"><span data-stu-id="9b3c0-189">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="9b3c0-190">خدمة عملية 2012 لأداة تقارير الإدارة (على أجهزة كمبيوتر BI فقط)</span><span class="sxs-lookup"><span data-stu-id="9b3c0-190">Management Reporter 2012 Process Service (on Business intelligence [BI] computers only)</span></span>

### <a name="reset"></a><span data-ttu-id="9b3c0-191">إعادة التعيين</span><span class="sxs-lookup"><span data-stu-id="9b3c0-191">Reset</span></span>

#### <a name="download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="9b3c0-192">تنزيل موقع حزمة MinorVersionDataUpgrade.zip الأحدث</span><span class="sxs-lookup"><span data-stu-id="9b3c0-192">Download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="9b3c0-193">قم بتنزيل حزمة MinorVersionDataUpgrade.zip الأحدث.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-193">Download the latest MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="9b3c0-194">للحصول على إرشادات حول كيفية العثور على وتنزيل الإصدار الصحيح من حزمة ترقية البيانات، راجع[تنزيل حزمة ترقية البيانات الأحدث والقابلة للنشر](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span><span class="sxs-lookup"><span data-stu-id="9b3c0-194">For instructions about how to find and download the correct version of the data upgrade package, see the[Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span></span> 

<span data-ttu-id="9b3c0-195">لا حاجة إلى إجراء عملية ترقية لتنزيل حزمة MinorVersionDataUpgrade.zip.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-195">An upgrade isn't required in order to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="9b3c0-196">ولذلك، ماعليك سوى اتباع الخطوات الواردة في قسم "تنزيل حزمة ترقية البيانات الأحدث والقابلة للنشر" في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-196">Therefore, you just have follow the steps in the "Download the latest data upgrade deployable package" section of that topic.</span></span> <span data-ttu-id="9b3c0-197">يمكنك تخطي كل الخطوات الأخرى في الموضوع.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-197">You can skip all the other steps in the topic.</span></span>

#### <a name="run-scripts-against-the-finance-and-operations-database"></a><span data-ttu-id="9b3c0-198">تشغيل البرامج النصية مقابل قاعدة بيانات Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9b3c0-198">Run scripts against the Finance and Operations database</span></span>

<span data-ttu-id="9b3c0-199">تشغيل البرامج النصية التالية مقابل قاعدة بيانات Finance and Operations (وليس مقابل قاعدة بيانات التقارير المالية):</span><span class="sxs-lookup"><span data-stu-id="9b3c0-199">Run the following scripts against the Finance and Operations database (not against the Financial reporting database):</span></span>

- <span data-ttu-id="9b3c0-200">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="9b3c0-200">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
- <span data-ttu-id="9b3c0-201">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="9b3c0-201">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="9b3c0-202">تساعد هذه البرامج النصية على ضمان صحة إعدادات تتبع المستخدمين والأدوار والتغييرات.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-202">These scripts help guarantee that the users, roles, and change tracking settings are correct.</span></span>

#### <a name="run-a-windows-powershell-command-to-reset-the-database"></a><span data-ttu-id="9b3c0-203">تشغيل أمر Windows PowerShell لإعادة تعيين قاعدة البيانات</span><span class="sxs-lookup"><span data-stu-id="9b3c0-203">Run a Windows PowerShell command to reset the database</span></span>

<span data-ttu-id="9b3c0-204">على كمبيوتر AOS، ابدأ تشغيل Microsoft Windows PowerShell كمسؤول، وقم بتشغيل الأوامر التالية لإعادة تعيين التكامل بين التقارير المالية لـ Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-204">On the AOS computer, start Microsoft Windows PowerShell as an administrator, and run the following commands to reset the integration between Finance and Operations and Financial reporting.</span></span>

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail "<reason for resetting>"
```

<span data-ttu-id="9b3c0-205">فيما يلي توضيح للمعلمات في أمر **Reset-DatamartIntegration**:</span><span class="sxs-lookup"><span data-stu-id="9b3c0-205">Here is an explanation of the parameters in the **Reset-DatamartIntegration** command:</span></span>

- <span data-ttu-id="9b3c0-206">القيم الصالحة لـ **-Reason** هي **SERVICING**، و**BADDATA**، و**OTHER**.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-206">The valid values for **-Reason** are **SERVICING**, **BADDATA**, and **OTHER**.</span></span>
- <span data-ttu-id="9b3c0-207">معلمة **-ReasonDetail** عبارة عن نص حر.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-207">The **-ReasonDetail** parameter is free text.</span></span>
- <span data-ttu-id="9b3c0-208">سيتم تسجيل السبب وتفاصيل السبب في مراقبة القياس عن بعد/البيئة.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-208">The reason and reason detail will be recorded in telemetry/environment monitoring.</span></span>

> [!NOTE]
> <span data-ttu-id="9b3c0-209">بعد تشغيل الأوامر، سوف يُطلب منك إدخال **ص** لتأكيد رغبتك في إعادة تعيين قاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-209">After you run the commands, you will be asked to enter **Y** to confirm that you want to reset the database.</span></span>

#### <a name="restart-services"></a><span data-ttu-id="9b3c0-210">إعادة تشغيل الخدمات</span><span class="sxs-lookup"><span data-stu-id="9b3c0-210">Restart services</span></span>

<span data-ttu-id="9b3c0-211">استخدم services.msc لإعادة تشغيل الخدمات التي قمت بوقفها في وقت سابق:</span><span class="sxs-lookup"><span data-stu-id="9b3c0-211">Use services.msc to restart the services that you stopped earlier:</span></span>

- <span data-ttu-id="9b3c0-212">خدمة النشر على شبكة الإنترنت العالمية (على كافة أجهزة الكمبيوتر التي تعمل بنظام AOS)</span><span class="sxs-lookup"><span data-stu-id="9b3c0-212">World wide web publishing service (on all AOS computers)</span></span>
- <span data-ttu-id="9b3c0-213">خدمة إدارة الدفعة لـ Microsoft Dynamics 365 for Finance and Operations (على أجهزة الكمبيوتر التي لا تعمل بنظام AOS فقط)</span><span class="sxs-lookup"><span data-stu-id="9b3c0-213">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="9b3c0-214">خدمة عملية 2012 لإدارة تقارير الأداة (على أجهزة كمبيوتر BI فقط)</span><span class="sxs-lookup"><span data-stu-id="9b3c0-214">Management Reporter 2012 Process Service (on BI computers only)</span></span>

#### <a name="import-report-definitions"></a><span data-ttu-id="9b3c0-215">استيراد تعريفات التقارير</span><span class="sxs-lookup"><span data-stu-id="9b3c0-215">Import report definitions</span></span>

<span data-ttu-id="9b3c0-216">استورد تصاميم التقارير من مصمم التقارير باستخدام الملف الذي تم إنشاؤه أثناء عملية التصدير.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-216">Import your report designs from Report designer by using the file that was created during the export.</span></span>

1. <span data-ttu-id="9b3c0-217">في مصمم التقارير، حدد **الشركة** &gt; **مجموعات كتل الإنشاء**.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-217">In Report designer, select **Company** &gt; **Building Block Groups**.</span></span>
2. <span data-ttu-id="9b3c0-218">حدد مجموعة كتلة الإنشاء لتصديرها، ثم حدد **تصدير**.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-218">Select the building block group to export, and then select **Export**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9b3c0-219">ملاحظة: بالنسبة إلى Finance and Operations، يتم دعم مجموعة واحدة فقط من كتل الإنشاء، وهي المجموعة **الافتراضية**.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-219">For Finance and Operations, only one building block group is supported, **Default**.</span></span>

3. <span data-ttu-id="9b3c0-220">حدد كتلة الإنشاء **الافتراضية**، ثم حدد **استيراد**.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-220">Select the **Default** building block, and then select **Import**.</span></span>
4. <span data-ttu-id="9b3c0-221">حدد الملف الذي يحتوي على تعاريف التقارير التي تم تصديرها، ثم حدد **فتح**.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-221">Select the file that contains the exported report definitions, and then select **Open**.</span></span>
5. <span data-ttu-id="9b3c0-222">في مربع حوار **استيراد**، حدد تعريفات التقارير المطلوب استيرادها:</span><span class="sxs-lookup"><span data-stu-id="9b3c0-222">In the **Import** dialog box, select the report definitions to import:</span></span>

    - <span data-ttu-id="9b3c0-223">لاستيراد كل تعاريف التقارير وكتل الإنشاء المقترنة، حدد **تحديد الكل**.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-223">To import all the report definitions and the associated building blocks, select **Select All**.</span></span>
    - <span data-ttu-id="9b3c0-224">لاستيراد تقارير أو صفوف أو أعمدة أو أشجار أو مجموعات أبعاد محددة، حدد التقارير أو الصفوف أو الأعمدة أو الأشجار أو مجموعات الأبعاد المطلوب استيرادها.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-224">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6. <span data-ttu-id="9b3c0-225">حدد **استيراد**.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-225">Select **Import**.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-on-premises"></a><span data-ttu-id="9b3c0-226">إعادة تعيين متجر بيانات التقارير المالية لـ Finance and Operations (محلي)</span><span class="sxs-lookup"><span data-stu-id="9b3c0-226">Reset the Financial reporting data mart for Finance and Operations (on-premises)</span></span>

1. <span data-ttu-id="9b3c0-227">أرشد جميع المستخدمين إلى الخروج من منطقة التقارير المالية ومصمم التقارير في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-227">Instruct all users to exit Report designer and the Financial reporting area of Finance and Operations.</span></span>
2. <span data-ttu-id="9b3c0-228">قم بتشغيل البرنامج النصي التالي مقابل قاعدة بيانات التقارير المالية (MRDB).</span><span class="sxs-lookup"><span data-stu-id="9b3c0-228">Run the following script against the Financial reporting database (MRDB).</span></span>

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ```

3. <span data-ttu-id="9b3c0-229">قم بتقطيع أو حذف جميع السجلات من جدول FINANCIALREPORTS في قاعدة بيانات Finance and Operations ‏(AXDB).</span><span class="sxs-lookup"><span data-stu-id="9b3c0-229">Truncate or delete all records from the FINANCIALREPORTS table in the Finance and Operations database (AXDB).</span></span>
4. <span data-ttu-id="9b3c0-230">قم بتقطيع أو حذف جميع السجلات من جدول FINANCIALREPORTVERSION، إذا كان هذا الجدول موجودًا في قاعدة بيانات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-230">Truncate or delete all records from the FINANCIALREPORTVERSION table, if this table exists in the Finance and Operations database.</span></span> <span data-ttu-id="9b3c0-231">في حالة عدم وجود الجدول في قاعدة بيانات Finance and Operations، تجاوز هذه الخطوة.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-231">If the table doesn't exist in the Finance and Operations database, skip this step.</span></span>
5. <span data-ttu-id="9b3c0-232">قم بتشغيل البرنامج النصي **ResetDatamart.sql** مقابل قاعدة بيانات التقارير المالية.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-232">Run the **ResetDatamart.sql** script against the Financial reporting database.</span></span> <span data-ttu-id="9b3c0-233">يقوم هذا البرنامج النصي بتعطيل تكامل متجر البيانات، ويحذف كافة بيانات متجر البيانات، ثم يعيد تمكين تكامل متجر البيانات.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-233">This script disables the data mart integration, deletes all the data mart data, and then reenables the data mart integration.</span></span>

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ------------------------------
    PRINT 'Drop archive tables'
    ------------------------------
    DECLARE @tableId nvarchar(max)
    DECLARE dropCursor CURSOR LOCAL FAST_FORWARD FOR
    SELECT Id FROM [Datamart].Archive
    OPEN dropCursor
    FETCH NEXT FROM dropCursor INTO @tableId
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'FactStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].FactStaging' + @tableId)
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationStaging' + @tableId)
        FETCH NEXT FROM dropCursor INTO @tableId
    END
    CLOSE dropCursor
    DEALLOCATE dropCursor
    IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationProcessing' and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationProcessing')
    ------------------------------
    PRINT 'Begin Truncating tables'
    ------------------------------
    DECLARE @tablename nvarchar(200)
    DECLARE @schemaname nvarchar(200)
    DECLARE clear_tables CURSOR
        FOR SELECT TABLE_NAME, TABLE_SCHEMA FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'Datamart' AND TABLE_TYPE='BASE TABLE'
    PRINT 'remove check constraints'
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename + '] NOCHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'delete data from tables and rebuild indexes'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
            IF(EXISTS (select TOP 1 1 from sys.foreign_keys where referenced_object_id = OBJECT_ID(@schemaname + '.' + @tablename)) OR
            EXISTS(SELECT TOP 1 1 FROM sys.sql_expression_dependencies sed
            INNER JOIN sys.objects o ON sed.referencing_id = o.[object_id]
            WHERE o.[type] = 'V' 
            AND referenced_schema_name = @schemaname
            AND referenced_entity_name = @tablename))
            BEGIN
            PRINT 'deleting from ' + @tablename
            EXEC('DELETE FROM [' + @schemaname + '].[' + @tablename + ']')
            END
            ELSE
            BEGIN
            PRINT 'truncating from ' + @tablename
            EXEC('TRUNCATE TABLE [' + @schemaname + '].[' + @tablename + ']')
            END
        END
        EXEC('ALTER INDEX ALL ON [' + @schemaname + '].[' + @tablename + '] REBUILD')
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'reenable check constraints'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename +'] WITH CHECK CHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    DEALLOCATE clear_tables
    ------------------------------
    PRINT 'Complete Truncating tables'
    ------------------------------
    ------------------------------
    PRINT 'Remove indexes from DimensionCombination'
    ------------------------------
    DECLARE @indexname nvarchar(200)
    DECLARE drop_indexes CURSOR
    FOR SELECT Name FROM sys.indexes WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]') AND is_primary_key = 0
    OPEN drop_indexes
    FETCH NEXT FROM drop_indexes INTO @indexname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('DROP INDEX [' + @indexname + '] on [Datamart].[DimensionCombination]')
        FETCH NEXT FROM drop_indexes INTO @indexname
    END
    CLOSE drop_indexes
    DEALLOCATE drop_indexes
    ------------------------------
    PRINT 'Drop Columns on DimensionCombination'
    ------------------------------
    DECLARE @objectname nvarchar(200)
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId', 'InactiveDimensions')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombination] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationResolving'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationResolving]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationResolving] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationStaging'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationStaging]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'OrganizationId', 'Description', 'SourceKey', 'OrganizationKey', 'FreshnessDate')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationStaging] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationUnreferenced'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationUnreferenced]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationUnreferenced] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionValueAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionValueAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('DimensionValueId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionValueAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on FactAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[FactAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('FactId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[FactAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalance'
    ------------------------------
    DECLARE @name nvarchar(200)
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalance'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    -- Rebuild dropped indexes that are dynamic
    EXEC [Datamart].ConfigureIndexesAndConstraints
    ------------------------------------------
    ------------------------------------------
    PRINT 'Reset the map tokens'
    UPDATE [Connector].[Map] SET InitalLoad = 0, ReaderToken=NULL, LastQuerySuccess='1900-01-01' WHERE MapId IN (SELECT t.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Reset the tasks'
    UPDATE [Scheduling].[TaskState] SET StateType = 0, Progress = 0.0, LastRunTime = NULL, NextRunTime = NULL WHERE TaskId IN (SELECT ts.[TaskId]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8'))
    PRINT 'Enable integration tasks, RunImmediately'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 1, StartBoundary = '1900-01-01' 
    WHERE Id in (SELECT [id] from @triggerIds WHERE taskTypeId = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Enable the Maintenance Task'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 0, StartBoundary = GETDATE() WHERE Id in
    (SELECT [id] from @triggerIds WHERE taskTypeId = 'D81C1197-D486-4FB7-AF8C-078C110893A0')
    ------------------------------------------
    ------------------------------------------
    ```

6. <span data-ttu-id="9b3c0-234">بعد إعادة التعيين، يمكنك التحقق من إعادة تحميل البيانات يدوياً عن طريق تشغيل الاستعلام التالي مقابل قاعدة بيانات التقارير المالية.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-234">After the reset, you can manually verify the data reload by running the following query against the Financial reporting database.</span></span>

    ```
    select ReaderObjectName, WriterObjectName, LastRunTime, StateType from Connector.MapsWithDetail with (nolock)
    ```

    <span data-ttu-id="9b3c0-235">تأكد من أن جميع الصفوف تحتوي على قيمة **LastRunTime** ومن تعيين **StateType** على **5**.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-235">Confirm that all rows have a **LastRunTime** value, and that **StateType** is set to **5**.</span></span> <span data-ttu-id="9b3c0-236">تشير قيمة **StateType** البالغة **5** إلى أنه تمت إعادة تحميل البيانات بنجاح.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-236">A **StateType** value of **5** indicates that the data was successfully reloaded.</span></span> <span data-ttu-id="9b3c0-237">تشير القيمة البالغة **7** إلى حالة خطأ.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-237">A value of **7** indicates a faulted state.</span></span> <span data-ttu-id="9b3c0-238">في بعض الأحيان، تشتمل خريطة التدرج الهرمي للمؤسسات على هذه الحالة في أول مرة لتشغيلها.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-238">Sometimes, the Organization Hierarchy map has this state the first time that it runs.</span></span> <span data-ttu-id="9b3c0-239">ومع ذلك، يجب أن يتم حل حالة الخطأ تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="9b3c0-239">However, the faulted state but should be automatically resolved.</span></span>

