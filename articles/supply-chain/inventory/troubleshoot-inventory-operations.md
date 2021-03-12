---
title: استكشاف أخطاء عمليات المخزون وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع عمليات المخزون.
author: sherry-zheng
manager: tfehr
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 3a22229106753d265a90f0ef05f5ac82dc745bbd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967145"
---
# <a name="troubleshoot-inventory-operations"></a><span data-ttu-id="a98fd-103">استكشاف أخطاء عمليات المخزون وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="a98fd-103">Troubleshoot inventory operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a98fd-104">يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع عمليات المخزون.</span><span class="sxs-lookup"><span data-stu-id="a98fd-104">This topic describes how to fix issues that you might encounter while you work with inventory operations.</span></span>

## <a name="i-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a><span data-ttu-id="a98fd-105">تعذر العثور علي مربع الحوار المنسدل "سير العمل" لدفاتر يوميه المخزون.</span><span class="sxs-lookup"><span data-stu-id="a98fd-105">I can't find the "Workflow" drop-down dialog box for inventory journals.</span></span>

### <a name="issue-description"></a><span data-ttu-id="a98fd-106">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="a98fd-106">Issue description</span></span>

<span data-ttu-id="a98fd-107">لا يمكنك العثور علي مربع الحوار المنسدل **سير العمل** في صفحه دفتر اليومية، أو ان عمليات سير العمل ذات الصلة غير متوفرة.</span><span class="sxs-lookup"><span data-stu-id="a98fd-107">You can't find the **Workflow** drop-down dialog box on the journal page, or related workflow operations aren't available.</span></span>

<span data-ttu-id="a98fd-108">يمكن ان تحدث هذه المشكلة لثلاثه أسباب، كما هو موضح في الأقسام الفرعية التالية.</span><span class="sxs-lookup"><span data-stu-id="a98fd-108">This issue can occur for three reasons, as described in the following subsections.</span></span>

### <a name="issue-resolution-1"></a><span data-ttu-id="a98fd-109">حل المشكلة 1</span><span class="sxs-lookup"><span data-stu-id="a98fd-109">Issue resolution 1</span></span>

<span data-ttu-id="a98fd-110">إذا كانت المشكلة تنطبق علي كافة المستخدمين ، فقد تحدث لأنه لم يتم تعيين سير عمل الاعتماد إلى اسم دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="a98fd-110">If the issue applies to all users, it might be occurring because the approval workflow hasn't been assigned to the journal name.</span></span> <span data-ttu-id="a98fd-111">لإصلاح المشكلة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="a98fd-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="a98fd-112">انتقل إلى **إدارة المخزون &gt; إعداد &gt; أسماء دفاتر اليومية &gt; المخزون**.</span><span class="sxs-lookup"><span data-stu-id="a98fd-112">Go to **Inventory Management &gt; Setup &gt; Journal names &gt; Inventory**.</span></span>
1. <span data-ttu-id="a98fd-113">في جزء القائمة، حدد اسم دفتر يومية لفتح صفحة الإعدادات الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="a98fd-113">In the list pane, select a journal name to open its settings.</span></span>
1. <span data-ttu-id="a98fd-114">في علامة التبويب السريعة **عام**، عيّن الخيار **سير عمل الاعتماد** إلى *نعم*.</span><span class="sxs-lookup"><span data-stu-id="a98fd-114">On the **General** FastTab, set the **Approval workflow** option to *Yes*.</span></span> <span data-ttu-id="a98fd-115">انقر فوق **نعم** إذا تمت مطالبتك بتأكيد التغيير.</span><span class="sxs-lookup"><span data-stu-id="a98fd-115">If you're prompted to confirm the change, select **Yes**.</span></span>
1. <span data-ttu-id="a98fd-116">في الحقل **سير العمل**، حدد سير العمل الذي تريد استخدامه لاسم دفتر اليومية المحدد.</span><span class="sxs-lookup"><span data-stu-id="a98fd-116">In the **Workflow** field, select the workflow that you want to use for the selected journal name.</span></span>

### <a name="issue-resolution-2"></a><span data-ttu-id="a98fd-117">حل المشكلة 2</span><span class="sxs-lookup"><span data-stu-id="a98fd-117">Issue resolution 2</span></span>

<span data-ttu-id="a98fd-118">إذا كان سير العمل الخاص بك يستخدم تعليمه برمجيه مخصصه، فقد تحدث مشكلات بعد ترقيه النظام.</span><span class="sxs-lookup"><span data-stu-id="a98fd-118">If your workflow uses customized code, issues might occur after you upgrade the system.</span></span> <span data-ttu-id="a98fd-119">علي سبيل المثال، في سير عمل دفتر اليومية ، قد يكون الزر **إرسال** رماديا التالي لا يمكنك تحديده لاعتماد الإرسال.</span><span class="sxs-lookup"><span data-stu-id="a98fd-119">For example, in the journal workflow, the **Submit** button might be grayed out so you can't select it to approve a submission.</span></span>

<span data-ttu-id="a98fd-120">إذا كان الزر **إرسال** رماديا، فمن المحتمل ان يكون سير العمل قد تم تخصيصه، مما يعني انه قد تم توسيع طريقه سير العمل `canSubmitToWorkflow()` الموجود في`FormDataUtil`.</span><span class="sxs-lookup"><span data-stu-id="a98fd-120">If the **Submit** button is grayed out, your workflow might have been customized, which means the method of the workflow, `canSubmitToWorkflow()` in `FormDataUtil`, has been extended.</span></span> <span data-ttu-id="a98fd-121">لحل هذه المشكلة، قم بتغيير الطريقة التي تقوم بها بتوسيع أسلوب `canSubmitToWorkflow()` لاستخدام البنية في المثال التالي.</span><span class="sxs-lookup"><span data-stu-id="a98fd-121">To fix this issue, change the way that you extend the method of the `canSubmitToWorkflow()` to use the structure in the following example.</span></span>

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

### <a name="issue-resolution-3"></a><span data-ttu-id="a98fd-122">حل المشكلة 3</span><span class="sxs-lookup"><span data-stu-id="a98fd-122">Issue resolution 3</span></span>

<span data-ttu-id="a98fd-123">إذا كانت المشكلة تنطبق فقط علي عدد قليل من المستخدمين المحددين، فقد لا يكون لدي هؤلاء المستخدمين امتيازات الأمان المطلوبة لتشغيل عمليات سير العمل في دفاتر يوميه المخزون.</span><span class="sxs-lookup"><span data-stu-id="a98fd-123">If the issue applies only to a few specific users, those users might not have the security privileges that are required to run workflow operations on inventory journals.</span></span> <span data-ttu-id="a98fd-124">تحقق من ان كل مستخدم متاثر يتمتع بامتياز أمان *سير عمل دفتر يوميه المخزون*.</span><span class="sxs-lookup"><span data-stu-id="a98fd-124">Verify that each affected user has the *Maintain inventory journal workflow* security privilege.</span></span> <span data-ttu-id="a98fd-125">افتراضيا، يتم تعيين هذا الامتياز لرسم جمركي له نفس الاسم، ويتم تطبيق تلك الرسوم علي *ادوار المستودع* وعامل *أداره المستودع*.</span><span class="sxs-lookup"><span data-stu-id="a98fd-125">By default, this privilege is assigned to a duty that has same name, and that duty is applied to the *Warehouse worker* and *Warehouse manager* roles.</span></span>

## <a name="my-inventory-journal-remains-in-system-locked-status-and-the-workflow-batch-job-doesnt-work"></a><span data-ttu-id="a98fd-126">يظل دفتر يوميه المخزون الخاص بي في حاله تامين النظام، ولا تعمل وظيفة مجموعه سير العمل.</span><span class="sxs-lookup"><span data-stu-id="a98fd-126">My inventory journal remains in system-locked status, and the workflow batch job doesn't work.</span></span>

### <a name="issue-description"></a><span data-ttu-id="a98fd-127">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="a98fd-127">Issue description</span></span>

<span data-ttu-id="a98fd-128">تم تامين أحد دفاتر يوميه المخزون من خلال عمليه أخرى ولم يتم إصدارها.</span><span class="sxs-lookup"><span data-stu-id="a98fd-128">One of your inventory journals is locked by some operation and isn't being released.</span></span> <span data-ttu-id="a98fd-129">علي سبيل المثال، في حاله حدوث خطا غير معروف اثناء الترحيل (الذي يعد عمليه تامين النظام)، فقد يظل دفتر اليومية في حاله تامين النظام.</span><span class="sxs-lookup"><span data-stu-id="a98fd-129">For example, if an unknown error occurs during posting (which is a system lock operation), the journal might remain in system-locked status.</span></span> <span data-ttu-id="a98fd-130">في هذه الحالة، سيقوم معالج عنصر عمل سير العمل بطرح خطا اثناء تامين التحقق من الصحة.</span><span class="sxs-lookup"><span data-stu-id="a98fd-130">In this case, the workflow work item handler will throw an error while it does lock validation.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a98fd-131">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="a98fd-131">Issue resolution</span></span>

<span data-ttu-id="a98fd-132">قم بتسجيل الدخول إلى مثيل SQL Server لـ Supply Chain Management، وتحقق ما إذا كان قد تم تعيين **InventJournalTable.SystemBlocked** إلى *1*.</span><span class="sxs-lookup"><span data-stu-id="a98fd-132">Sign in to the SQL Server instance for Supply Chain Management, and check whether **InventJournalTable.SystemBlocked** is set to *1*.</span></span> <span data-ttu-id="a98fd-133">وإذا كان الأمر كذلك، فتاكد من ان الدفتر لا يجب ان يكون في حاله تامين، ثم قم باعاده تعيين **InventJournalTable.SystemBlocked** إلى القيمة *0*.</span><span class="sxs-lookup"><span data-stu-id="a98fd-133">If it is, make sure that the journal should not be in locked status, and then reset **InventJournalTable.SystemBlocked** to *0*.</span></span>

## <a name="my-inventory-journal-workflow-is-never-completed-and-the-journal-cant-be-edited-or-posted"></a><span data-ttu-id="a98fd-134">لا يتم مطلقا إكمال سير عمل دفتر يوميه المخزون، ولا يمكن تحرير دفتر اليومية أو ترحيله.</span><span class="sxs-lookup"><span data-stu-id="a98fd-134">My inventory journal workflow is never completed, and the journal can't be edited or posted.</span></span>

### <a name="issue-description"></a><span data-ttu-id="a98fd-135">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="a98fd-135">Issue description</span></span>

<span data-ttu-id="a98fd-136">بعد إرسال سير عمل اعتماد دفتر اليومية، تتوقف معالجه سير العمل عن الاستجابة، ولا يمكنك تحرير دفاتر اليومية أو معالجتها.</span><span class="sxs-lookup"><span data-stu-id="a98fd-136">After you submit a journal approval workflow, workflow processing stops responding, and you can't edit or process your journals.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a98fd-137">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="a98fd-137">Issue resolution</span></span>

<span data-ttu-id="a98fd-138">هناك العديد من الأسباب التي قد لا يتم إكمال معالجه سير العمل فيها.</span><span class="sxs-lookup"><span data-stu-id="a98fd-138">There are several reasons why workflow processing might not be completed.</span></span> <span data-ttu-id="a98fd-139">التحقق من المشكلات التالية:</span><span class="sxs-lookup"><span data-stu-id="a98fd-139">Check for the following issues:</span></span>

- <span data-ttu-id="a98fd-140">انتقل إلى **أداره المخزون &gt; اعداد &gt; عمليات سير عمل الاداره**، وقم بمراجعه تكوين سير العمل المتاثر.</span><span class="sxs-lookup"><span data-stu-id="a98fd-140">Go to **Inventory management &gt; Setup &gt; Inventory management workflows**, and review the configuration of the affected workflow.</span></span> <span data-ttu-id="a98fd-141">لمزيد من المعلومات ، راجع [عمليات سير عمل اعتماد دفتر يوميه المخزون](inventory-journal-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="a98fd-141">For more information, see [Inventory journal approval workflows](inventory-journal-workflow.md).</span></span>
- <span data-ttu-id="a98fd-142">قد يواجه سير العمل استثناءا أو خطا.</span><span class="sxs-lookup"><span data-stu-id="a98fd-142">The workflow might be encountering an exception or error.</span></span> <span data-ttu-id="a98fd-143">قم بمراجعه سجل عنصر العمل الخاص بسير العمل المتاثر لمعرفه ما إذا كان يتضمن خطا في التطبيق الذي ينهي سير العمل.</span><span class="sxs-lookup"><span data-stu-id="a98fd-143">Review the work item history of the affected workflow to see whether it includes an application error that terminates the workflow.</span></span>
- <span data-ttu-id="a98fd-144">يمكن تحديث دفتر يوميه المخزون أو تحريره فقط في حاله اعتماده.</span><span class="sxs-lookup"><span data-stu-id="a98fd-144">The inventory journal can be updated or edited only if it's approved.</span></span> <span data-ttu-id="a98fd-145">وإذا كان الاسترجاع نشطا، فيمكنك محاولة استدعاء دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="a98fd-145">If recall is active, you can try to recall the journal.</span></span> <span data-ttu-id="a98fd-146">قد يتم إيقاف تنفيذ وظيفة مجموعه سير العمل مؤقتا لأسباب متعددة.</span><span class="sxs-lookup"><span data-stu-id="a98fd-146">Execution of the workflow batch job might be suspended for multiple reasons.</span></span> <span data-ttu-id="a98fd-147">قد تحدث بعض هذه الأسباب بسبب مشكله اطار عمل سير العمل.</span><span class="sxs-lookup"><span data-stu-id="a98fd-147">Some of these reasons might be caused by the workflow framework issue.</span></span>

## <a name="inventory-journal-workflow-conditions-apply-only-at-the-journal-level-not-at-the-line-level"></a><span data-ttu-id="a98fd-148">تنطبق حالات سير عمل دفتر يوميه المخزون فقط علي مستوي دفتر اليومية، وليس عند مستوي البند</span><span class="sxs-lookup"><span data-stu-id="a98fd-148">Inventory journal workflow conditions apply only at the journal level, not at the line level</span></span>

### <a name="issue-description"></a><span data-ttu-id="a98fd-149">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="a98fd-149">Issue description</span></span>

<span data-ttu-id="a98fd-150">قد تواجهك هذه المشكلة في حاله قيامك، علي سبيل المثال، بمحاولة اعداد شرط سير عمل "دفتر يوميه المخزون" علي مبلغ التكلفة.</span><span class="sxs-lookup"><span data-stu-id="a98fd-150">You might experience this issue if, for example, you try to set up an inventory journal workflow condition on the cost amount.</span></span> <span data-ttu-id="a98fd-151">قم باعداد الشرط بحيث يتم تشغيل الخطوة 1 فقط عندما يكون مبلغ التكلفة اقل من 100.</span><span class="sxs-lookup"><span data-stu-id="a98fd-151">You set up the condition so that step 1 is run only when the cost amount is less than 100.</span></span> <span data-ttu-id="a98fd-152">قم باعداد شرط آخر بحيث يتم تشغيل الخطوة 2 فقط عندما يكون مبلغ التكلفة أكثر من أو يساوي 100.</span><span class="sxs-lookup"><span data-stu-id="a98fd-152">You then set up another condition so that step 2 is run only when the cost amount is more than or equal to 100.</span></span> <span data-ttu-id="a98fd-153">وبعد ذلك، عند تشغيل سير العمل، تظهر محفوظات سير العمل بندا واحدا فقط، ويتم دائما تقييم الشرط الأول علي انه *صواب*، بغض النظر عن القيمة التي يتم إرسالها.</span><span class="sxs-lookup"><span data-stu-id="a98fd-153">Then, when the workflow is run, the workflow history shows only one line, and the first condition is always evaluated as *true*, regardless of the value that is submitted.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="a98fd-154">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="a98fd-154">Issue workaround</span></span>

<span data-ttu-id="a98fd-155">في الإصدار الحالي، تنطبق شروط سير عمل دفتر يوميه المخزون فقط علي مستوي دفتر اليومية، وليس عند مستوي البند.</span><span class="sxs-lookup"><span data-stu-id="a98fd-155">In the current release, inventory workflow conditions apply only at the journal level, not at the line level.</span></span> <span data-ttu-id="a98fd-156">يتم هذا السلوك بسبب التصميم.</span><span class="sxs-lookup"><span data-stu-id="a98fd-156">This behavior is by design.</span></span> <span data-ttu-id="a98fd-157">نوصي بتعيين معايير الشرط فقط في السمات علي مستوي دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="a98fd-157">We recommend that you set your condition criteria only on journal-level attributes.</span></span>

## <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-filter-results-as-i-expect"></a><span data-ttu-id="a98fd-158">لا يقوم جزء التصفية الموجود في الصفحة القائمة الفعلية بتصفية النتائج التي أتوقعها.</span><span class="sxs-lookup"><span data-stu-id="a98fd-158">The filter pane on the On-hand list page doesn't filter results as I expect.</span></span>

### <a name="issue-description"></a><span data-ttu-id="a98fd-159">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="a98fd-159">Issue description</span></span>

<span data-ttu-id="a98fd-160">لا تقوم عوامل التصفية في جزء التصفية الموجود في الصفحة **القائمة الفعلية**  بتصفية النتائج كما تتوقعها.</span><span class="sxs-lookup"><span data-stu-id="a98fd-160">The filters in the filter pane on the **On-hand list** page don't filter results as you expect.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a98fd-161">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="a98fd-161">Issue resolution</span></span>

<span data-ttu-id="a98fd-162">يتم هذا السلوك بسبب التصميم.</span><span class="sxs-lookup"><span data-stu-id="a98fd-162">This behavior is by design.</span></span>

<span data-ttu-id="a98fd-163">يتم تجميع صفحة  **قائمة المخزون الفعلي**  من جدول المخزون الفعلي الذي يتضمن جميع الأبعاد المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="a98fd-163">The **On-hand list** page is assembled from a detailed on-hand inventory table that includes all available dimensions.</span></span> <span data-ttu-id="a98fd-164">ومع ذلك، القائمة الموجودة في هذه الصفحة هي ملخص.</span><span class="sxs-lookup"><span data-stu-id="a98fd-164">However, the list on this page is a summary.</span></span> <span data-ttu-id="a98fd-165">وبالتالي، فقد تجمع الصفوف من الجدول المصدر عن طريق تجميع القيم وفقًا للأبعاد المعروضة.</span><span class="sxs-lookup"><span data-stu-id="a98fd-165">Therefore, it might combine rows from the source table by aggregating values according to the dimensions that are shown.</span></span>

<span data-ttu-id="a98fd-166">عوامل التصفية التي تم إعدادها في جزء عوامل التصفية على الجدول المصدر، وليس على القائمة المجمعة.</span><span class="sxs-lookup"><span data-stu-id="a98fd-166">Filters that are set up in the filter pane apply to the source table, not to the aggregated list.</span></span> <span data-ttu-id="a98fd-167">قد يؤدي هذا السلوك في بعض الأحيان إلى ظهور نتائج غير متوقعه، كما هو موضح في [الامثله التالية](inventory-on-hand-list.md#examples).</span><span class="sxs-lookup"><span data-stu-id="a98fd-167">This behavior can sometimes produce unexpected results, as shown in [these examples](inventory-on-hand-list.md#examples).</span></span>

<span data-ttu-id="a98fd-168">ومع ذلك، فإن  [عوامل التصفية المتوفرة في الشبكة](inventory-on-hand-list.md#grid-filters) *تنطبق*  على القائمة المجمعة.</span><span class="sxs-lookup"><span data-stu-id="a98fd-168">However, the [filters that are provided in the grid](inventory-on-hand-list.md#grid-filters) *do* apply to the aggregated list.</span></span> <span data-ttu-id="a98fd-169">تتضمن عوامل التصفية هذه QuickFilter في الجزء العلوي من الشبكة بالإضافة إلى عامل التصفية لكل عنوان عمود.</span><span class="sxs-lookup"><span data-stu-id="a98fd-169">These filters include both the QuickFilter at the top of the grid and the filter for each column heading.</span></span>

## <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a><span data-ttu-id="a98fd-170">لا تعمل الوحدة وكميه الوحدة بشكل صحيح في دفتر يوميه المخزون.</span><span class="sxs-lookup"><span data-stu-id="a98fd-170">The unit and unit quantity aren't working correctly in the inventory journal.</span></span>

### <a name="issue-description"></a><span data-ttu-id="a98fd-171">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="a98fd-171">Issue description</span></span>

<span data-ttu-id="a98fd-172">قد تواجه أحدي المشكلتين التاليتين أو كلتاهما عند العمل مع الوحدات والكميات في دفتر يوميه المخزون:</span><span class="sxs-lookup"><span data-stu-id="a98fd-172">You might encounter one or both of the following issues when you work with units and quantities in an inventory journal:</span></span>

- <span data-ttu-id="a98fd-173">لا يمكنك الاطلاع علي الوحدات أو كميات الوحدات في دفتر يوميه المخزون اثناء اعداد وحده تحويل للمنتج الذي تم إصداره، ولا يمكنك تغيير الوحدة في يوميه المخزون.</span><span class="sxs-lookup"><span data-stu-id="a98fd-173">You don't see units or unit quantities in the inventory journal while a unit of conversion is set up for the released product, and you can't change the unit in the inventory journal.</span></span>
- <span data-ttu-id="a98fd-174">يمكنك عرض الحقلين **الكمية** و **الوحدة** في دفتر يوميه المخزون، ولكن لا يمكنك رؤية حقل **كميه الوحدة**.</span><span class="sxs-lookup"><span data-stu-id="a98fd-174">You see the **Quantity** and **Unit** fields in the inventory journal, but you don't see the **Unit quantity** field.</span></span> <span data-ttu-id="a98fd-175">إذا قمت بتغيير الوحدة، ادخل كميه، وقم بترحيل دفتر اليومية، ويستمر دفتر اليومية في عرض وحده القياس الاصليه لهذه الكمية.</span><span class="sxs-lookup"><span data-stu-id="a98fd-175">If you change the unit, enter a quantity, and post the journal, the journal still shows the original unit of measurement for that quantity.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a98fd-176">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="a98fd-176">Issue resolution</span></span>

<span data-ttu-id="a98fd-177">لإصلاح هذه المشكلة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="a98fd-177">To fix this issue, follow these steps.</span></span>

1. <span data-ttu-id="a98fd-178">في مساحة عمل **أداره الميزات**، تاكد من تشغيل الميزة *استخدام وحده القياس وكميه الوحدات في دفاتر يوميه المخزون*.</span><span class="sxs-lookup"><span data-stu-id="a98fd-178">In the **Feature management** workspace, make sure that the *Using unit of measure and unit quantity in inventory journals* feature is turned on.</span></span> <span data-ttu-id="a98fd-179">تضيف هذه الميزة الحقلين **وحده** و **كميه الوحدة** إلى دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="a98fd-179">This feature adds the **Unit** and **Unit quantity** fields to the journal.</span></span>
1. <span data-ttu-id="a98fd-180">بعد تشغيل الميزة ، استخدم حقول **الكمية** و **كميه الوحدة** و **الوحدة** بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="a98fd-180">After the feature is turned on, use the **Quantity**, **Unit quantity**, and **Unit** fields in the following way:</span></span>

    - <span data-ttu-id="a98fd-181">**الكمية** - تحدد الكمية من خلال استخدام الوحدة الافتراضية التي تم تحديدها للمنتج الذي تم إصداره.</span><span class="sxs-lookup"><span data-stu-id="a98fd-181">**Quantity** – Specify the quantity by using the default unit that is defined for the released product.</span></span> <span data-ttu-id="a98fd-182">ومع ذلك، لا يتم إظهار الوحدة الافتراضية نفسها هنا.</span><span class="sxs-lookup"><span data-stu-id="a98fd-182">However, the default unit itself isn't shown here.</span></span> <span data-ttu-id="a98fd-183">إذا تم اعداد تحويل بين الوحدة الافتراضية والوحدة التي تم تحديدها في الحقل **الوحدة**، يتم تحديث حقل **الكمية** تلقائيا، استنادا إلى التحديدات في الحقلين **كميه الوحدة** و **الوحدة**.</span><span class="sxs-lookup"><span data-stu-id="a98fd-183">If a conversion is set up between the default unit and the unit that is selected in the **Unit** field, the **Quantity** field is automatically updated, based on the selections in the **Unit quantity** and **Unit** fields.</span></span>
    - <span data-ttu-id="a98fd-184">**كمية الوحدة** – حدد الكمية باستخدام وحدة القياس المحددة في حقل **الوحدة**.</span><span class="sxs-lookup"><span data-stu-id="a98fd-184">**Unit quantity** – Specify the quantity by using the unit that is selected in the **Unit** field.</span></span>
    - <span data-ttu-id="a98fd-185">**الوحدة** - حدد الوحدة التي سيتم تطبيقها علي القيمة في حقل **كميه الوحدات**.</span><span class="sxs-lookup"><span data-stu-id="a98fd-185">**Unit** – Select the unit to apply to the value in the **Unit quantity** field.</span></span>

## <a name="i-receive-the-following-error-message-maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a><span data-ttu-id="a98fd-186">أتلقى رسالة الخطا التالية: "الحد الأقصى لعدد الأرقام العشرية لوحده الاحتفاظ بالأسهم هي 0".</span><span class="sxs-lookup"><span data-stu-id="a98fd-186">I receive the following error message: "Maximum number of decimals for the stock keeping unit is 0."</span></span>

### <a name="issue-description"></a><span data-ttu-id="a98fd-187">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="a98fd-187">Issue description</span></span>

<span data-ttu-id="a98fd-188">عند محاولة ترحيل عمليه مخزنيه أو حجز مخزون ، ستتلقى رسالة الخطا التالية: "الحد الأقصى لعدد الأرقام العشرية لوحده الاحتفاظ بالمخزون هي 0".</span><span class="sxs-lookup"><span data-stu-id="a98fd-188">When you try to post an inventory transaction or an inventory reservation, you receive the following error message: "Maximum number of decimals for the stock keeping unit is 0."</span></span>

<span data-ttu-id="a98fd-189">تحدث هذه المشكلة عند تحديد كميه العملية المخزنية كقيمه عشريه اقل من مستوي الدقة التي يدعمها الحقل.</span><span class="sxs-lookup"><span data-stu-id="a98fd-189">This issue occurs when the inventory transaction quantity is specified as a decimal value that is below the level of precision that the field supports.</span></span> <span data-ttu-id="a98fd-190">علي سبيل المثال، تم تحديد كميه قيمتها *0.5* لحركه المخزون، ولكن يتم دعم كميات الاعداد الصحيحة فقط.</span><span class="sxs-lookup"><span data-stu-id="a98fd-190">For example, a quantity of *0.5* has been specified for an inventory transaction, but only integer quantities are supported.</span></span> <span data-ttu-id="a98fd-191">التالي، يجب ان تكون القيمة *1* بدلا من *0.5*.</span><span class="sxs-lookup"><span data-stu-id="a98fd-191">Therefore, the value should be *1* instead of *0.5*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a98fd-192">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="a98fd-192">Issue resolution</span></span>

1. <span data-ttu-id="a98fd-193">قم بتشغيل البرنامج النصي التالي علي مثيل SQL Server لتقريب الكميات في العمليات المخزنية.</span><span class="sxs-lookup"><span data-stu-id="a98fd-193">Run the following script on your SQL Server instance to round quantities in the inventory transactions.</span></span> <span data-ttu-id="a98fd-194">سيقوم هذا البرنامج النصي بتصحيح القيم الموجودة في الجدول **inventTrans**.</span><span class="sxs-lookup"><span data-stu-id="a98fd-194">This script will correct values in the **inventTrans** table.</span></span>

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. <span data-ttu-id="a98fd-195">تشغيل التحقق من التناسق الفعلي حيث يتم تشغيل خيار **إصلاح الخطأ**.</span><span class="sxs-lookup"><span data-stu-id="a98fd-195">Run an on-hand consistency check where the **fix error** option is turned on.</span></span> <span data-ttu-id="a98fd-196">سيقوم هذا الفحص بتصحيح القيم الموجودة في الجدول **inventSum**.</span><span class="sxs-lookup"><span data-stu-id="a98fd-196">This check will correct values in the **inventSum** table.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a98fd-197">نوصي بشده بتحرير البرنامج النصي كما هو مطلوب للبيئة الخاصة بك، واختباره في بيئة اختبار، ثم التحقق من البيانات الناتجة قبل تشغيل البرنامج النصي في بيئة التشغيل.</span><span class="sxs-lookup"><span data-stu-id="a98fd-197">We strongly recommend that you carefully edit the script as required for your environment, test it in a test environment, and then check the resulting data before you run the script in a production environment.</span></span>
