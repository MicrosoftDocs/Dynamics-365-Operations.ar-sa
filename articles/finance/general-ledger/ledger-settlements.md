---
title: تسويات دفتر الأستاذ
description: يشرح هذا الموضوع كيفية استخدام الصفحة "تسويات دفتر الأستاذ‬" لتسوية حركات دفتر الأستاذ وعكس التسويات.
author: mikefalkner
manager: aolson
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransSettlement
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-11-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: d41a69bed3d1340736cc7df35aa3ded032d4d79d
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977109"
---
# <a name="ledger-settlements"></a><span data-ttu-id="50344-103">تسويات دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="50344-103">Ledger settlements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="50344-104">تتيح لك تسويات دفتر الأستاذ بمطابقة الحركات المدينة والدائنة في دفتر الأستاذ العام، ووضع علامة عليها كحركات تمت تسويتها.</span><span class="sxs-lookup"><span data-stu-id="50344-104">Ledger settlements let you match debit and credit transactions in the general ledger, and mark them as settled.</span></span> <span data-ttu-id="50344-105">ومن خلال هذه الطريقة، يمكنك التأكد من أن الحركات ذات الصلة قد تم تمسحها.</span><span class="sxs-lookup"><span data-stu-id="50344-105">In this way, you can make sure that related transactions have been cleared.</span></span> <span data-ttu-id="50344-106">ويمكنك أيضًا عكس التسويات إذا تم إنشاؤها عن طريق الخطأ.</span><span class="sxs-lookup"><span data-stu-id="50344-106">You can also reverse settlements if they were made by mistake.</span></span>

## <a name="enable-advanced-ledger-settlements"></a><span data-ttu-id="50344-107">تمكين تسويات دفتر الأستاذ المتقدم</span><span class="sxs-lookup"><span data-stu-id="50344-107">Enable advanced ledger settlements</span></span>

<span data-ttu-id="50344-108">توفر لك صفحة تسويات دفتر الأستاذ المتقدم‬ قدرات إضافية لتصفية الحركات وتحديدها.</span><span class="sxs-lookup"><span data-stu-id="50344-108">The advanced ledger settlements page provides additional capabilities for filtering and selecting transactions.</span></span> <span data-ttu-id="50344-109">لتمكين صفحة تسويات دفتر الأستاذ المتقدم‬، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="50344-109">To enable advanced ledger settlements page, follow these steps.</span></span>

1. <span data-ttu-id="50344-110">حدد **دفتر الأستاذ العام** \> **إعداد دفتر الأستاذ‬** \> **معلمات دفتر الأستاذ العام** .</span><span class="sxs-lookup"><span data-stu-id="50344-110">Select **General ledger** \> **Ledger setup** \> **General ledger parameters** .</span></span> 
2. <span data-ttu-id="50344-111">على علامة التبويب **تسويات دفتر الأستاذ** ، عيّن الخيار **تسوية دفتر الأستاذ المتقدم** إلى **نعم** لتشغيل وظيفة تسوية دفتر الأستاذ المتقدم.</span><span class="sxs-lookup"><span data-stu-id="50344-111">On the **Ledger settlements** tab, set the **Advanced ledger settlement** option to **Yes** to turn on the advanced ledger settlement functionality.</span></span> <span data-ttu-id="50344-112">سينك استخدام الصفحة **تسويات دفتر الأستاذ** عندما تحدد **تسويات دفتر الأستاذ** في **المهام الدورية** .</span><span class="sxs-lookup"><span data-stu-id="50344-112">The advanced **Ledger settlements** page will be used when you select **Ledger settlements** in the **Periodic tasks** .</span></span> 
3. <span data-ttu-id="50344-113">يجب إدخال قائمة الحسابات المراد استخدامها لتسويات دفتر الأستاذ لكل دليل حسابات‬.</span><span class="sxs-lookup"><span data-stu-id="50344-113">You must enter the list of accounts to use for ledger settlements for each chart of accounts.</span></span> <span data-ttu-id="50344-114">ويتم استخدام هذه القائمة لتصفية قائمة الحركات التي تظهر في صفحة **تسويات دفتر الأستاذ** .</span><span class="sxs-lookup"><span data-stu-id="50344-114">This list is used to filter the list of transactions that appears on the **Ledger settlements** page.</span></span> <span data-ttu-id="50344-115">في قائمة **دليل الحسابات** ، حدد دليل حسابات، ثم حدد **جديد** لإضافة حسابات جديدة إلى القائمة.</span><span class="sxs-lookup"><span data-stu-id="50344-115">In the **Chart of accounts** list, select a chart of accounts, and then select **New** to add new accounts to the list.</span></span>

## <a name="settle-transactions-by-using-the-advanced-ledger-settlements-page"></a><span data-ttu-id="50344-116">تسوية الحركات باستخدام صفحة تسويات دفتر الأستاذ المتقدم</span><span class="sxs-lookup"><span data-stu-id="50344-116">Settle transactions by using the advanced ledger settlements page</span></span>

<span data-ttu-id="50344-117">لتسوية حركات دفتر الأستاذ، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="50344-117">To settle ledger transactions, follow these steps.</span></span>

1. <span data-ttu-id="50344-118">حدد **دفتر الأستاذ العام** \> **المهام الدورية** \> **تسويات دفتر الأستاذ** .</span><span class="sxs-lookup"><span data-stu-id="50344-118">Select **General ledger** \> **Periodic tasks** \> **Ledger settlements** .</span></span>
2. <span data-ttu-id="50344-119">قم بتعيين عوامل التصفية في أعلى الصفحة:</span><span class="sxs-lookup"><span data-stu-id="50344-119">Set the filters at the top of the page:</span></span>

    - <span data-ttu-id="50344-120">حدد نطاق تاريخ، أو حدد **كود الفاصل الزمني‬** لتعبئة نطاق التاريخ بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="50344-120">Select a date range, or select **Date interval code** to automatically fill in the date range.</span></span>
    - <span data-ttu-id="50344-121">قم بتغيير طبقة الترحيل كما تريد.</span><span class="sxs-lookup"><span data-stu-id="50344-121">Change the posting layer as you require.</span></span>
    - <span data-ttu-id="50344-122">لعرض حساب دفتر الأستاذ والأبعاد بشكل منفصل، حدد مجموعة أبعاد مالية.</span><span class="sxs-lookup"><span data-stu-id="50344-122">To show the ledger account and dimensions separately, select a financial dimension set.</span></span>

3. <span data-ttu-id="50344-123">حدد **عرض الحركات** لعرض كافة الحركات التي تطابق عوامل التصفية التي قمت بتعيين وقائمة بالحسابات التي قمت بتحديدها عند إعداد دليل الحسابات في القسم السابق.</span><span class="sxs-lookup"><span data-stu-id="50344-123">Select **Display transactions** to show all the transactions that match the filters that you set and the list of accounts that you specified when you set up the chart of accounts list in the previous section.</span></span> <span data-ttu-id="50344-124">إذا قمت بتغيير أي من عوامل التصفية أو مجموعات الأبعاد، فيجب تحديد **عرض الحركات** مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="50344-124">If you change any of the filters or the dimension sets, you must select **Display transactions** again.</span></span>
4. <span data-ttu-id="50344-125">حدد بندًا أو أكثر تريد أخذه في الاعتبار للتسوية.</span><span class="sxs-lookup"><span data-stu-id="50344-125">Select one or more lines that you're considering for settlement.</span></span> <span data-ttu-id="50344-126">تتزايد أو تتناقص قيمة حقل **المبلغ المحدد** في أعلى الصفحة حسب المبلغ الإجمالي في البنود التي حددتها.</span><span class="sxs-lookup"><span data-stu-id="50344-126">The value of the **Selected amount** field at the top of the page increases or decreases by the total amount on the lines that you selected.</span></span>
5. <span data-ttu-id="50344-127">بعد الانتهاء من تحديد الحركات، حدد **علامة التحديد** .</span><span class="sxs-lookup"><span data-stu-id="50344-127">After you've finished selecting transactions, select **Mark selected** .</span></span> <span data-ttu-id="50344-128">تظهر علامة اختيار في العمود **معلّم** لكل حركة من الحركات التي حددتها.</span><span class="sxs-lookup"><span data-stu-id="50344-128">A check mark appears in the **Marked** column for each transaction that you selected.</span></span> <span data-ttu-id="50344-129">علاوةً على ذلك، تتزايد أو تتناقص قيمة حقل **المبلغ المحدد** في أعلى الشبكة حسب المبلغ الإجمالي في البنود التي حددتها.</span><span class="sxs-lookup"><span data-stu-id="50344-129">Additionally, the value of the **Marked amount** field above the grid increases or decreases by the total amount on the lines that you marked.</span></span>
6. <span data-ttu-id="50344-130">عندما تكون قيمة **المبلغ المحدد** عبارة عن **0** (صفر)، حدد **تسوية الحركات المميزة‬** .</span><span class="sxs-lookup"><span data-stu-id="50344-130">When the **Marked amount** value is **0** (zero), select **Settle marked transactions** .</span></span> <span data-ttu-id="50344-131">يتم تحديث حالة الحركات المميزة إلى **تمت التسوية** .</span><span class="sxs-lookup"><span data-stu-id="50344-131">The status of the marked transactions is updated to **Settled** .</span></span>

## <a name="make-transactions-easier-to-find"></a><span data-ttu-id="50344-132">تسهيل العثور على الحركات</span><span class="sxs-lookup"><span data-stu-id="50344-132">Make transactions easier to find</span></span>

<span data-ttu-id="50344-133">تتضمن صفحة **تسويات دفتر الأستاذ** قدرات تسهّل رؤية الحركات التي تحتاج إليها للتسوية.</span><span class="sxs-lookup"><span data-stu-id="50344-133">The **Ledger settlements** page includes capabilities that make it easier to see the transactions that you need for settlement.</span></span>

- <span data-ttu-id="50344-134">يقوم الزر **إلغاء علامة التحديد‬** بمسح الحقل **معلّم** لكافة البنود المحددة.</span><span class="sxs-lookup"><span data-stu-id="50344-134">The **Unmark selected** button clears the **Marked** field for all lines that are selected.</span></span>
- <span data-ttu-id="50344-135">يسمح لك عامل التصفية **معلّم** بتصفية الحركات استنادًا إلى ما إذا كان الحقل **معلّم** التابع لها محددًا أم ملغى تحديده.</span><span class="sxs-lookup"><span data-stu-id="50344-135">The **Marked** filter lets you filter transactions based on whether the **Marked** field for them is selected or cleared.</span></span>
- <span data-ttu-id="50344-136">يسمح لك عامة التصفية **حالة** بتصفية الحركات استنادًا إلى ما إذا كانت حالتها **تمت التسوية** أو **لم تتم التسوية‬** .</span><span class="sxs-lookup"><span data-stu-id="50344-136">The **Status** filter lets you filter transactions based on whether their status is **Settled** or **Not settled** .</span></span>
- <span data-ttu-id="50344-137">يسمح لك الزر **فرز حسب المبلغ المطلق** بفرز المبالغ حسب القيمة المطلقة، بحيث يمكنك تجميع معا المبالغ الدائنة والمدينة ذات القيمة نفسها.</span><span class="sxs-lookup"><span data-stu-id="50344-137">The **Sort by absolute amount** button lets you sort the amounts by absolute value, so that you can group together debits and credits that have the same amount.</span></span>

## <a name="reverse-a-settlement"></a><span data-ttu-id="50344-138">عكس تسوية</span><span class="sxs-lookup"><span data-stu-id="50344-138">Reverse a settlement</span></span>

<span data-ttu-id="50344-139">يمكنك عكس تسوية تمت عن طريق الخطأ.</span><span class="sxs-lookup"><span data-stu-id="50344-139">You can reverse a settlement that was made by mistake.</span></span>

1. <span data-ttu-id="50344-140">اتبع الخطوات من 1 إلى 3 في القسم "صفحة تسوية الحركات باستخدام صفحة تسويات دفتر الأستاذ المتقدم‬" لإظهار الحركات التي تبحث عنها.</span><span class="sxs-lookup"><span data-stu-id="50344-140">Follow steps 1 through 3 in the "Settle transactions by using advanced ledger settlements page" section to show the transactions that you're looking for.</span></span>
2. <span data-ttu-id="50344-141">في عامل التصفية **حالة** ، حدد **تمت التسوية** .</span><span class="sxs-lookup"><span data-stu-id="50344-141">In the **Status** filter, select **Settled** .</span></span>
3. <span data-ttu-id="50344-142">حدد بندًا أو أكثر تريد أخذه في الاعتبار لعكس التسوية.</span><span class="sxs-lookup"><span data-stu-id="50344-142">Select one or more lines that you're considering for reversal.</span></span> <span data-ttu-id="50344-143">تتزايد أو تتناقص قيمة حقل **المبلغ المحدد** في أعلى الصفحة حسب المبلغ الإجمالي في البنود التي حددتها.</span><span class="sxs-lookup"><span data-stu-id="50344-143">The value of the **Selected amount** field at the top of the page increases or decreases by the total amount on the lines that you selected.</span></span>
4. <span data-ttu-id="50344-144">بعد الانتهاء من تحديد الحركات، حدد **علامة التحديد** .</span><span class="sxs-lookup"><span data-stu-id="50344-144">After you've finished selecting transactions, select **Mark selected** .</span></span> <span data-ttu-id="50344-145">تظهر علامة اختيار في العمود **معلّم** لكل حركة من الحركات التي حددتها.</span><span class="sxs-lookup"><span data-stu-id="50344-145">A check mark appears in the **Marked** column for each transaction that you selected.</span></span> <span data-ttu-id="50344-146">علاوةً على ذلك، تتزايد أو تتناقص قيمة حقل **المبلغ المحدد** في أعلى الصفحة حسب المبلغ الإجمالي في البنود التي حددتها.</span><span class="sxs-lookup"><span data-stu-id="50344-146">Additionally, the value of the **Marked amount** field at the top of the page increases or decreases by the total amount on the lines that you marked.</span></span>
5. <span data-ttu-id="50344-147">عندما تكون قيمة **المبلغ المحدد** عبارة عن **0** (صفر)، حدد **عكس الحركات المميزة‬** .</span><span class="sxs-lookup"><span data-stu-id="50344-147">When the **Marked amount** value is **0** (zero), select **Reverse marked transactions** .</span></span> <span data-ttu-id="50344-148">يتم تحديث حالة الحركات المميزة إلى **لم تتم التسوية** .</span><span class="sxs-lookup"><span data-stu-id="50344-148">The status of the marked transactions is updated to **Not settled** .</span></span>

## <a name="update-the-list-of-accounts-that-are-included-in-the-list-of-transactions"></a><span data-ttu-id="50344-149">تحديث قائمة الحسابات المضمنة في قائمة الحركات</span><span class="sxs-lookup"><span data-stu-id="50344-149">Update the list of accounts that are included in the list of transactions</span></span>

<span data-ttu-id="50344-150">حدد **حسابات تسوية دفتر الأستاذ** لفتح مربع حوار حيث يمكنك تحرير الحسابات التي تم تضمينها في قائمة الحركات.</span><span class="sxs-lookup"><span data-stu-id="50344-150">Select **Ledger settlement accounts** to open a dialog box where you can edit the accounts that are included in the list of transactions.</span></span> <span data-ttu-id="50344-151">حدد **جديد** لإضافة حسابات جديدة إلى القائمة.</span><span class="sxs-lookup"><span data-stu-id="50344-151">Select **New** to add new accounts to the list.</span></span> <span data-ttu-id="50344-152">ويتم استخدام هذه القائمة لتصفية قائمة الحركات التي تظهر في صفحة **تسويات دفتر الأستاذ** .</span><span class="sxs-lookup"><span data-stu-id="50344-152">This list is used to filter the list of transactions that appears on the **Ledger settlements** page.</span></span>
