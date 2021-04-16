---
title: أرشفة حركات المخزون
description: يوضح هذا الموضوع كيفية أرشفة بيانات حركة المخزون للمساعدة في تحسين أداء النظام.
author: sherry-zheng
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransArchiveProcessForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: bacc27c1a9066892c51110d28ba9a2ad26bebe77
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839285"
---
# <a name="archive-inventory-transactions"></a><span data-ttu-id="72577-103">أرشفة حركات المخزون</span><span class="sxs-lookup"><span data-stu-id="72577-103">Archive inventory transactions</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="72577-104">بمرور الوقت، سيستمر جدول حركات المخزون (`InventTrans`) في النمو وزيادة الحجم واستهلاك مساحة قاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="72577-104">Over time, the inventory transactions table (`InventTrans`) will continue to grow and consume more database space.</span></span> <span data-ttu-id="72577-105">وبالتالي، ستصبح الاستعلامات التي يتم إجراؤها على الجدول أبطأ تدريجياً.</span><span class="sxs-lookup"><span data-stu-id="72577-105">Therefore, queries that are made against the table will gradually become slower.</span></span> <span data-ttu-id="72577-106">يصف هذا الموضوع كيف يمكنك استخدام ميزة *أرشيف حركات المخزون* لأرشفة البيانات حول حركات المخزون للمساعدة في تحسين أداء النظام.</span><span class="sxs-lookup"><span data-stu-id="72577-106">This topic describes how you can use the *Inventory transactions archive* feature to archive data about inventory transactions to help improve system performance.</span></span>

> [!NOTE]
> <span data-ttu-id="72577-107">يمكن أرشفة حركات المخزون التي تم تحديثها ماليًا فقط في فترة دفتر الأستاذ المُقفلة المحددة.</span><span class="sxs-lookup"><span data-stu-id="72577-107">Only financially updated inventory transactions can be archived in a selected closed ledger period.</span></span> <span data-ttu-id="72577-108">ولكي تتم أرشفتها، ينبغي أن تكون لحركات المخزون الصادرة المحدثة ماليًا في حالة إصدار *مُباع*، وينبغي أن تكون حركات المخزون الواردة في حالة استلام *مشتراة*.</span><span class="sxs-lookup"><span data-stu-id="72577-108">To be archived, financially updated outbound inventory transactions must have an issue status of *Sold*, and inbound inventory transactions must have a receipt status of *Purchased*.</span></span>

<span data-ttu-id="72577-109">عند أرشفة حركات المخزون، يتم نقل جميع الحركات ذات الصلة إلى الجدول `InventTransArchive` .</span><span class="sxs-lookup"><span data-stu-id="72577-109">When you archive inventory transactions, all related transactions are moved to the `InventTransArchive` table.</span></span> <span data-ttu-id="72577-110">تتم أرشفة حركات إصدار المخزون وحركات استلام المخزون بشكل منفصل، استنادًا إلى مجموعة معرّف الصنف (`itemId`) ومعرف بُعد المخزون (`inventDimId`)، ويتم وضعها في الإصدار الملخص وحركات الاستلام الملخصة.</span><span class="sxs-lookup"><span data-stu-id="72577-110">Inventory issue transactions and inventory receipt transactions are archived separately, based on the combination of the item ID (`itemId`) and inventory dimension ID (`inventDimId`), and they are put into the summarized issue and summarized receipt transactions.</span></span>

<span data-ttu-id="72577-111">إذا احتوت مجموعة `itemId` و `inventDimId` على حركة استلام أو إصدار واحدة فقط، فلن تتم أرشفة الحركة.</span><span class="sxs-lookup"><span data-stu-id="72577-111">If an `itemId` and `inventDimId` combination contains only one receipt or issue transaction, the transaction won't be archived.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="72577-112">تشغيل الميزة في النظام</span><span class="sxs-lookup"><span data-stu-id="72577-112">Turn on the feature in your system</span></span>

<span data-ttu-id="72577-113">إذا لم يتضمن نظامك الميزات الموضحة في هذا الموضوع بالفعل، فانتقل إلى [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)، وقم بتشغيل ميزة *أرشيف حركات المخزون*.</span><span class="sxs-lookup"><span data-stu-id="72577-113">If your system doesn't already include the features that is described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Inventory transactions archive* feature.</span></span>

## <a name="things-to-consider-before-you-archive-inventory-transactions"></a><span data-ttu-id="72577-114">الأشياء الواجب مراعاتها قبل أرشفة حركات المخزون</span><span class="sxs-lookup"><span data-stu-id="72577-114">Things to consider before you archive inventory transactions</span></span>

<span data-ttu-id="72577-115">قبل أرشفة حركات المخزون، ينبغي مراعاة سيناريوهات الأعمال التالية، لأنها ستتأثر بالعملية:</span><span class="sxs-lookup"><span data-stu-id="72577-115">Before you archive inventory transactions, you should consider the following business scenarios, because they will be affected by the operation:</span></span>

- <span data-ttu-id="72577-116">عند تدقيق حركات المخزون من المستندات ذات الصلة، مثل بنود أمر الشراء، سيتم عرضها على أنها مؤرشفة.</span><span class="sxs-lookup"><span data-stu-id="72577-116">When you audit inventory transactions from related documents, such as purchase order lines, they will be shown as archived.</span></span> <span data-ttu-id="72577-117">لمراجعه الحركات المؤرشفة، ينبغي الانتقال إلى **إدارة المخزون\> المهام الدورية \> مسح \> أرشيف حركات المخزون**.</span><span class="sxs-lookup"><span data-stu-id="72577-117">To review the archived transactions, you must go to **Inventory management \> Periodic tasks \> Clean up \> Inventory transactions archive**.</span></span>
- <span data-ttu-id="72577-118">لا يمكن إلغاء إقفال المخزون للفترات المؤرشفة.</span><span class="sxs-lookup"><span data-stu-id="72577-118">Inventory closing can't be canceled for archived periods.</span></span> <span data-ttu-id="72577-119">قبل أن تتمكن من إلغاء إقفال المخزون، ينبغي عليك عكس أرشيف حركة المخزون للفترة ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="72577-119">Before you can cancel an inventory closing, you must reverse the inventory transaction archive for the relevant period.</span></span>
- <span data-ttu-id="72577-120">لا يمكن اجراء تحويل التكاليف القياسية‬ للفترات المؤرشفة.</span><span class="sxs-lookup"><span data-stu-id="72577-120">Standard cost conversion can't be done for archived periods.</span></span> <span data-ttu-id="72577-121">قبل أن تتمكن من إجراء تحويل التكاليف القياسية، يتعين عكس أرشيف حركة المخزون للفترة ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="72577-121">Before you can do standard cost conversion, you must reverse the inventory transaction archive for the relevant period.</span></span>
- <span data-ttu-id="72577-122">ستتأثر تقارير المخزون التي يتم الحصول عليها من حركات المخزون عند أرشفة حركات المخزون.</span><span class="sxs-lookup"><span data-stu-id="72577-122">Inventory reports that are sourced from inventory transactions will be affected when you archive inventory transactions.</span></span> <span data-ttu-id="72577-123">تتضمن هذه التقارير تقرير تقادم المخزون وتقارير قيمة المخزون.</span><span class="sxs-lookup"><span data-stu-id="72577-123">These reports include the inventory aging report and inventory value reports.</span></span>
- <span data-ttu-id="72577-124">قد تتأثر التنبؤ بالمخزون إذا تم تشغيله خلال الفترة الزمنية للفترات المؤرشفة.</span><span class="sxs-lookup"><span data-stu-id="72577-124">Inventory forecasts might be affected if they are run during the time horizon of archived periods.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="72577-125">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="72577-125">Prerequisites</span></span>

<span data-ttu-id="72577-126">يمكن أرشفة حركات المخزون فقط خلال الفترات التي يتم فيها استيفاء الشروط التالية:</span><span class="sxs-lookup"><span data-stu-id="72577-126">Inventory transactions can be archived only during periods where the following conditions are met:</span></span>

- <span data-ttu-id="72577-127">يتعين إقفال فترة دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="72577-127">The ledger period must be closed.</span></span>
- <span data-ttu-id="72577-128">ينبغي تشغيل إقفال المخزون في أو بعد تاريخ الفترة الخاصة بالأرشيف.</span><span class="sxs-lookup"><span data-stu-id="72577-128">Inventory closing must be run on or after the to-period date of the archive.</span></span>
- <span data-ttu-id="72577-129">ينبغي أن تكون الفترة قبل عام واحد على الأقل من تاريخ فترة بدء الأرشيف.</span><span class="sxs-lookup"><span data-stu-id="72577-129">The period must be at least one year before the from-period date of the archive.</span></span>
- <span data-ttu-id="72577-130">يتعين ألا يكون هناك أي عمليات إعادة حساب المخزون الحالية.</span><span class="sxs-lookup"><span data-stu-id="72577-130">There must not be any existing inventory recalculations.</span></span>

## <a name="archive-inventory-transactions"></a><span data-ttu-id="72577-131">أرشفة حركات المخزون</span><span class="sxs-lookup"><span data-stu-id="72577-131">Archive inventory transactions</span></span>

<span data-ttu-id="72577-132">لأرشفة حركات المخزون، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="72577-132">To archive inventory transactions, follow these steps.</span></span>

1. <span data-ttu-id="72577-133">الانتقال إلى **إدارة المخزون** \> **المهام الدورية** \> **مسح** \> **أرشيف حركات المخزون**.</span><span class="sxs-lookup"><span data-stu-id="72577-133">Go to **Inventory management** \> **Periodic tasks** \> **Clean up** \> **Inventory transaction archive**.</span></span>

    <span data-ttu-id="72577-134">تظهر صفحة **أرشيف حركات المخزون** وتعرض قائمة بسجلات العمليات المؤرشفة.</span><span class="sxs-lookup"><span data-stu-id="72577-134">The **Inventory transactions archive** page appears and shows a list of archived process records.</span></span>

    <span data-ttu-id="72577-135">![صفحة أرشيف حركات المخزون](media/archive-inventory-empty.png "صفحة أرشيف حركات المخزون")</span><span class="sxs-lookup"><span data-stu-id="72577-135">![Inventory transactions archive page](media/archive-inventory-empty.png "Inventory transactions archive page")</span></span>

1. <span data-ttu-id="72577-136">في جزء الاجراء، حدد **أرشيف حركات المخزون** لإنشاء أرشيف حركات المخزون.</span><span class="sxs-lookup"><span data-stu-id="72577-136">On the Action Pane, select **Inventory transactions archive** to create an inventory transaction archive.</span></span>
1. <span data-ttu-id="72577-137">في مربع الحوار **أرشيف حركات المخزون** ، في علامة التبويب السريعة **المعلمات** ، عيّن الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="72577-137">In the **Inventory transactions archive** dialog box, on the **Parameters** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="72577-138">**من تاريخ إقفال فترة دفتر الاستاذ** - حدد تاريخ أول حركة لتضمينها في الأرشيف.</span><span class="sxs-lookup"><span data-stu-id="72577-138">**From date in closed ledger period** – Select the earliest transaction date to include in the archive.</span></span>
    - <span data-ttu-id="72577-139">**إلى تاريخ إقفال فترة دفتر الاستاذ** - حدد تاريخ أخر حركة لتضمينها في الأرشيف.</span><span class="sxs-lookup"><span data-stu-id="72577-139">**To date in closed ledger period** – Select the latest transaction date to include in the archive.</span></span>

    <span data-ttu-id="72577-140">![مربع حوار أرشيف حركات المخزون](media/archive-inventory-dates.png "مربع حوار أرشيف حركات المخزون")</span><span class="sxs-lookup"><span data-stu-id="72577-140">![Inventory transactions archive dialog box](media/archive-inventory-dates.png "Inventory transactions archive dialog box")</span></span>

    > [!NOTE]
    > <span data-ttu-id="72577-141">ستتوفر فقط الفترات التي تلبي [المتطلبات الأساسية](#prerequisites) للتحديد.</span><span class="sxs-lookup"><span data-stu-id="72577-141">Only periods that meet the [prerequisites](#prerequisites) will be available for selection.</span></span>

1. <span data-ttu-id="72577-142">في علامة التبويب السريعة **تشغيل في الخلفية** ، قم بإعداد تفاصيل معالجة الدُفعات كما تريد.</span><span class="sxs-lookup"><span data-stu-id="72577-142">On the **Run in the background** FastTab, set up batch processing details as you require.</span></span> <span data-ttu-id="72577-143">اتبع الخطوات المعتادة للوظائف الدفعية في Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="72577-143">Follow the usual steps for batch jobs in Microsoft Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="72577-144">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="72577-144">Select **OK**.</span></span>
1. <span data-ttu-id="72577-145">تظهر رسالة تُطالبك بتأكيد الرغبة في المتابعة.</span><span class="sxs-lookup"><span data-stu-id="72577-145">You receive a message that prompts you to confirm that you want to continue.</span></span> <span data-ttu-id="72577-146">أقرا الرسالة بعناية، ثم حدد **نعم** إذا كنت ترغب في المتابعة.</span><span class="sxs-lookup"><span data-stu-id="72577-146">Read the message carefully, and then select **Yes** if you want to continue.</span></span>

    <span data-ttu-id="72577-147">تتلقى رسالة توضح أنه تمت إضافة وظيفة أرشيف حركات المخزون إلى قائمه انتظار الدُفعة.</span><span class="sxs-lookup"><span data-stu-id="72577-147">You receive a message that states that your inventory transactions archive job has been added to the batch queue.</span></span> <span data-ttu-id="72577-148">ستبدا الوظيفة الآن في أرشفة حركات المخزون من الفترة المحددة.</span><span class="sxs-lookup"><span data-stu-id="72577-148">The job will now start to archive inventory transactions from the selected period.</span></span>

## <a name="view-archived-inventory-transactions"></a><span data-ttu-id="72577-149">عرض حركات المخزون المؤرشفة</span><span class="sxs-lookup"><span data-stu-id="72577-149">View archived inventory transactions</span></span>

<span data-ttu-id="72577-150">تعرض صفحة **أرشيف حركات المخزون** كامل محفوظات الأرشفة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="72577-150">The **Inventory transactions archive** page shows your full archiving history.</span></span> <span data-ttu-id="72577-151">يعرض كل صف في الشبكة معلومات مثل تاريخ إنشاء الأرشيف والمستخدم الذي أنشأه وحالته.</span><span class="sxs-lookup"><span data-stu-id="72577-151">Each row in the grid shows information such as the date when the archive was created, the user who created it, and its status.</span></span>

<span data-ttu-id="72577-152">![أرشفة المحفوظات في صفحة أرشيف حركات المخزون](media/archive-inventory-full.png "أرشفة المحفوظات في صفحة أرشيف حركات المخزون")</span><span class="sxs-lookup"><span data-stu-id="72577-152">![Archiving history on the Inventory transactions archive page](media/archive-inventory-full.png "Archiving history on the Inventory transactions archive page")</span></span>

<span data-ttu-id="72577-153">في القائمة المنسدلة أعلى الصفحة، حدد إحدى القيم التالية لتصفية الأرشيفات التي تظهر في الشبكة:</span><span class="sxs-lookup"><span data-stu-id="72577-153">In the drop-down list at the top of the page select one of the following values to filter the archives that are shown in the grid:</span></span>

- <span data-ttu-id="72577-154">**نشط** -عرض الأرشيفات النشطة فقط، وليس الأرشيفات المعكوسة.</span><span class="sxs-lookup"><span data-stu-id="72577-154">**Active** – Show only active archives, not reversed archives.</span></span>
- <span data-ttu-id="72577-155">**الكل** – عرض كافة الأرشيفات، النشطة والمعكوسة.</span><span class="sxs-lookup"><span data-stu-id="72577-155">**All** – Show all archives, both active and reversed.</span></span>

<span data-ttu-id="72577-156">لكل أرشيف في الشبكة، يتم توفير المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="72577-156">For each archive in the grid, the following information is provided:</span></span>

- <span data-ttu-id="72577-157">**نشط** – تشير علامة الاختيار إلى أن الأرشيف نشط.</span><span class="sxs-lookup"><span data-stu-id="72577-157">**Active** – A check mark indicates that the archive is active.</span></span>
- <span data-ttu-id="72577-158">**من تاريخ** – تاريخ أقدم حركة يمكن تضمينها في الأرشيف.</span><span class="sxs-lookup"><span data-stu-id="72577-158">**From date** – The date of the oldest transaction that can be included in the archive.</span></span>
- <span data-ttu-id="72577-159">**إلى تاريخ** – تاريخ أخر حركة يمكن تضمينها في الأرشيف.</span><span class="sxs-lookup"><span data-stu-id="72577-159">**To date** – The date of the latest transaction that can be included in the archive.</span></span>
- <span data-ttu-id="72577-160">**مُجدول بواسطة** - حساب المستخدم الذي قام بإنشاء الأرشيف.</span><span class="sxs-lookup"><span data-stu-id="72577-160">**Scheduled by** – The user account that created the archive.</span></span>
- <span data-ttu-id="72577-161">**تم التنفيذ** - تاريخ إنشاء الأرشيف.</span><span class="sxs-lookup"><span data-stu-id="72577-161">**Executed** – The date when the archive was created.</span></span>
- <span data-ttu-id="72577-162">**عكسي** – تشير علامة الاختيار إلى أن الأرشيف قد تم عكسه.</span><span class="sxs-lookup"><span data-stu-id="72577-162">**Reverse** – A check mark indicates that the archive has been reversed.</span></span>
- <span data-ttu-id="72577-163">**إيقاف التحديث الحالي** – تشير علامة الاختيار إلى أن الأرشيف قيد التقدم، ولكن تم إيقافه مؤقتًا.</span><span class="sxs-lookup"><span data-stu-id="72577-163">**Stop current update** – A check mark indicates that the archive is in progress, but it has been paused.</span></span>
- <span data-ttu-id="72577-164">**الحالة** – حالة معالجة الأرشيف.</span><span class="sxs-lookup"><span data-stu-id="72577-164">**State** – The processing status of the archive.</span></span> <span data-ttu-id="72577-165">وتكون القيم المحتملة هي *الانتظار*، و *قيد التقدم*، و *منتهي*.</span><span class="sxs-lookup"><span data-stu-id="72577-165">The possible values are *Waiting*, *In progress*, and *Finished*.</span></span>

<span data-ttu-id="72577-166">يوفر شريط الأدوات أعلى الشبكة الأزرار التالية التي يمكنك استخدامها للعمل مع أرشيف محدد:</span><span class="sxs-lookup"><span data-stu-id="72577-166">The toolbar above the grid provides the following buttons that you can use to work with a selected archive:</span></span>

- <span data-ttu-id="72577-167">**الحركات المؤرشفة** – عرض التفاصيل الكاملة للأرشيف المحدد.</span><span class="sxs-lookup"><span data-stu-id="72577-167">**Archived transactions** – View the full details of the selected archive.</span></span> <span data-ttu-id="72577-168">تعرض صفحة **الحركات المؤرشفة** التي تعرض كافة الحركات في الأرشيف.</span><span class="sxs-lookup"><span data-stu-id="72577-168">The **Archived transactions** page that appears shows all the transactions in the archive.</span></span>

    <span data-ttu-id="72577-169">![صفحة الحركات المؤرشفة](media/archive-inventory-transactions.png "صفحة الحركات المؤرشفة")</span><span class="sxs-lookup"><span data-stu-id="72577-169">![Archived transactions page](media/archive-inventory-transactions.png "Archived transactions page")</span></span>

    <span data-ttu-id="72577-170">لعرض مزيد من المعلومات حول حركة معينة في صفحة **الحركات المؤرشفة** ، حددها في الشبكة، ثم في جزء الإجراءات، حدد **تفاصيل الحركة المؤرشفة**.</span><span class="sxs-lookup"><span data-stu-id="72577-170">To view more information about a specific transaction on the **Archived transactions** page, select it in the grid, and then, on the Action Pane, select **Archived transaction details**.</span></span> <span data-ttu-id="72577-171">تعرض صفحة **تفاصيل الحركة المؤرشفة** معلومات مثل ترحيل دفتر الأستاذ ومراجع دفتر الأستاذ الفرعي ذات الصلة والأبعاد المالية.</span><span class="sxs-lookup"><span data-stu-id="72577-171">The **Archived transaction details** page that appears shows information such as the ledger posting, related subledger references, and financial dimensions.</span></span>

- <span data-ttu-id="72577-172">**إيقاف الأرشفة** - إيقاف مؤقت للأرشيف المحدد الذي تتم معالجته حاليًا.</span><span class="sxs-lookup"><span data-stu-id="72577-172">**Pause archiving** – Pause a selected archive that is currently being processed.</span></span> <span data-ttu-id="72577-173">لا يسري الإيقاف المؤقت إلا بعد إنشاء مهمة الأرشفة.</span><span class="sxs-lookup"><span data-stu-id="72577-173">The pause takes effect only after the archiving task has been generated.</span></span> <span data-ttu-id="72577-174">لذلك، قد يكون هناك تأخير قصير قبل تفعيل الإيقاف المؤقت.</span><span class="sxs-lookup"><span data-stu-id="72577-174">Therefore, there might be a short delay before the pause takes effect.</span></span> <span data-ttu-id="72577-175">في حالة إيقاف الأرشيف بشكل مؤقت، تظهر علامة اختيار في الحقل **إيقاف التحديث الحالي** .</span><span class="sxs-lookup"><span data-stu-id="72577-175">If an archive has been paused, a check mark appears in its **Stop current update** field.</span></span>
- <span data-ttu-id="72577-176">**استئناف الأرشفة** - استئناف المعالجة لأرشيف محدد متوقف مؤقتًا حاليًا.</span><span class="sxs-lookup"><span data-stu-id="72577-176">**Resume archiving** – Resume processing for a selected archive that is currently paused.</span></span>
- <span data-ttu-id="72577-177">**عكسي** - عكس الأرشيف المحدد.</span><span class="sxs-lookup"><span data-stu-id="72577-177">**Reverse** – Reverse the selected archive.</span></span> <span data-ttu-id="72577-178">لا يمكنك عكس أرشيف إلا إذا تم تعيين حقل **الحالة** على *مُنتهي*.</span><span class="sxs-lookup"><span data-stu-id="72577-178">You can reverse an archive only if its **State** field is set to *Finished*.</span></span> <span data-ttu-id="72577-179">إذا تم عكس أحد الأرشيفات، فستظهر علامة اختيار في الحقل **عكسي** الخاص به.</span><span class="sxs-lookup"><span data-stu-id="72577-179">If an archive has been reversed, a check mark appears in its **Reverse** field.</span></span>