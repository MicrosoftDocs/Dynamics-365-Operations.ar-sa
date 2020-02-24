---
title: تعليق حركة واستئنافها في نقطة البيع (POS)
description: يشرح هذا الموضوع كيف يستطيع المستخدمون تعليق حركات قيد التقدم ثم استئنافها لاحقًا على سجل آخر باستخدام Dynamics 365 Commerce.
author: jblucher
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f513e2d857908f2b95d27bf48ff1e826724d7cbf
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021532"
---
# <a name="suspend-and-resume-a-transaction-in-the-point-of-sale-pos"></a><span data-ttu-id="c3285-103">تعليق حركة واستئنافها في نقطة البيع (POS)</span><span class="sxs-lookup"><span data-stu-id="c3285-103">Suspend and resume a transaction in the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="c3285-104">باستطاعة مستخدمي نقطة البيع (POS) تعليق حركات قيد التقدم ثم استئنافها لاحقًا على سجل آخر باستخدام.</span><span class="sxs-lookup"><span data-stu-id="c3285-104">Point of sale (POS) users can suspend in-progress transactions, and then resume them later or on a different register.</span></span> <span data-ttu-id="c3285-105">في أغلب الأحيان، يتم تعطيل الحركات لتحرير سجل بسرعة لمهمة أخرى من دون فقدان أي تقدم تحقق على الحركة الحالية.</span><span class="sxs-lookup"><span data-stu-id="c3285-105">Transactions are often suspended to quickly free up a register for a different task without losing any progress on the current transaction.</span></span> <span data-ttu-id="c3285-106">على سبيل المثال، يبدأ موظف المتجر معالجة حركة العميل على جهاز محمول ولكن يجب عليه إكمالها على سجل فيه درج نقدية‬‬.</span><span class="sxs-lookup"><span data-stu-id="c3285-106">For example, a store associate starts to process a customer's transaction on a mobile device but must complete it on a register that has a cash drawer.</span></span> <span data-ttu-id="c3285-107">في هذه الحالة، يستطيع موظف المتجر تعليق الحركة على الجهاز المحمول ثم استدعاءها على سجل.</span><span class="sxs-lookup"><span data-stu-id="c3285-107">In this case, the store associate can suspend the transaction on the mobile device, and then recall and resume it on a register.</span></span>

## <a name="configure-suspend-and-resume-functionality"></a><span data-ttu-id="c3285-108">تكوين وظيفة التعليق والاستئناف</span><span class="sxs-lookup"><span data-stu-id="c3285-108">Configure suspend and resume functionality</span></span>

### <a name="pos-operations"></a><span data-ttu-id="c3285-109">عمليات POS</span><span class="sxs-lookup"><span data-stu-id="c3285-109">POS operations</span></span>

<span data-ttu-id="c3285-110">تسمح عمليتان من [عمليات نقطة البيع (POS)](pos-operations.md) لنقطة البيع بدعم سيناريوهات التعليق والاستئناف.</span><span class="sxs-lookup"><span data-stu-id="c3285-110">Two [POS operations](pos-operations.md) let the POS support suspend and resume scenarios.</span></span> <span data-ttu-id="c3285-111">يمكنك تعيين هذه العمليات إلى [شبكات الأزرار](pos-screen-layouts.md) في صفحة الحركة أو صفحة الترحيب.</span><span class="sxs-lookup"><span data-stu-id="c3285-111">You can assign these operations to [button grids](pos-screen-layouts.md) on the transaction page or the welcome page.</span></span>

- <span data-ttu-id="c3285-112">503: تعليق الحركة</span><span class="sxs-lookup"><span data-stu-id="c3285-112">503: Suspend transaction</span></span>
- <span data-ttu-id="c3285-113">504: استدعاء الحركة</span><span class="sxs-lookup"><span data-stu-id="c3285-113">504: Recall transaction</span></span>

### <a name="receipt-template"></a><span data-ttu-id="c3285-114">قالب الإيصال</span><span class="sxs-lookup"><span data-stu-id="c3285-114">Receipt template</span></span>

<span data-ttu-id="c3285-115">يمكن تكوين نقطة البيع لإنشاء إيصال مطبوع عند تعليق الحركة.</span><span class="sxs-lookup"><span data-stu-id="c3285-115">The POS can be configured to generate a printed slip when a transaction is suspended.</span></span> <span data-ttu-id="c3285-116">بعد ذلك، يمكن استخدام هذا الإيصال لتمكين التعرف على الحركة واستدعائها بسرعة.</span><span class="sxs-lookup"><span data-stu-id="c3285-116">That slip can then be used to quickly identify and recall the transaction later.</span></span>

<span data-ttu-id="c3285-117">لتمكين نقطة البيع من طباعة إيصال، يجب إضافة تنسيق إيصال **تعليق الحركة** إلى ملف تعريف إيصال المتجر.</span><span class="sxs-lookup"><span data-stu-id="c3285-117">To enable the POS to print a slip, you must add the **Suspended transaction** receipt format to the store's receipt profile.</span></span> <span data-ttu-id="c3285-118">يمكنك تصميم تنسيق الإيصال بحيث يتضمن أو يستبعد تفاصيل معينة حول الحركة.</span><span class="sxs-lookup"><span data-stu-id="c3285-118">You can design the receipt format so that it includes or excludes specific details about the transaction.</span></span> <span data-ttu-id="c3285-119">على سبيل المثال، بإمكان التنسيق أن يتضمن كودًا شريطيًا لدعم المسح الضوئي.</span><span class="sxs-lookup"><span data-stu-id="c3285-119">For example, the format can include a barcode to support scanning.</span></span>

### <a name="receipt-numbering"></a><span data-ttu-id="c3285-120">ترقيم الإيصال</span><span class="sxs-lookup"><span data-stu-id="c3285-120">Receipt numbering</span></span>

<span data-ttu-id="c3285-121">فيما يتعلق بأنواع حركات نقطة البيع الأخرى التي تنشئ إيصالاً مطبوعًا، يمكنك تحديد تسلسل رقمي للحركات المعلقة في القسم **ترقيم الإيصال** في ملف تعريف الوظائف في المتجر.</span><span class="sxs-lookup"><span data-stu-id="c3285-121">As for other POS transaction types that generate a printed receipt, you can define a number sequence for suspended transactions in the **Receipt numbering** section of the store's functionality profile.</span></span>

### <a name="void-when-closing-shift"></a><span data-ttu-id="c3285-122">ملغى عند إغلاق الوردية</span><span class="sxs-lookup"><span data-stu-id="c3285-122">Void when closing shift</span></span>

<span data-ttu-id="c3285-123">يمكنك استخدام الخيار **ملغى عند إغلاق الوردية‬** للطلب من المستخدمين إما بإكمال الحركات المعلقة أو إلغائها قبل إغلاق الوردية.</span><span class="sxs-lookup"><span data-stu-id="c3285-123">You can use the **Void when closing shift** option to require that users either complete or void any suspended transactions before they close their shift.</span></span> <span data-ttu-id="c3285-124">أثناء عملية **إغلاق الوردية**، ستقوم نقطة البيع بمطالبة المستخدمين بعرض الحركات المعلقة أو إلغائها.</span><span class="sxs-lookup"><span data-stu-id="c3285-124">During the **Close shift** operation, the POS will prompt users to either view or void any outstanding suspended transactions.</span></span>

## <a name="suspend-and-resume-a-transaction"></a><span data-ttu-id="c3285-125">تعليق حركة واستئنافها</span><span class="sxs-lookup"><span data-stu-id="c3285-125">Suspend and resume a transaction</span></span>

### <a name="suspend-a-transaction"></a><span data-ttu-id="c3285-126">تعليق حركة</span><span class="sxs-lookup"><span data-stu-id="c3285-126">Suspend a transaction</span></span>

<span data-ttu-id="c3285-127">بإمكان المستخدمين الذين لديهم امتيازات كافية، والذين لديهم تخطيط شاشة يتضمن عملية **تعليق الحركة** إيقاف حركة ما لتمكين استدعائها في وقت لاحق أو على سجل آخر.</span><span class="sxs-lookup"><span data-stu-id="c3285-127">Users who have sufficient privileges, and who have a screen layout that includes the **Suspend transaction** operation, can suspend a transaction so that it can be recalled later or on a different register.</span></span>

<span data-ttu-id="c3285-128">يمكنك تعليق الحركات فقط إذا **لم** تتضمن الأنواع التالية من البنود:</span><span class="sxs-lookup"><span data-stu-id="c3285-128">Transactions can be suspended only if they do **not** contain the following types of lines:</span></span>

- <span data-ttu-id="c3285-129">بنود دفع نشطة</span><span class="sxs-lookup"><span data-stu-id="c3285-129">Active payment lines</span></span>
- <span data-ttu-id="c3285-130">بنود بطاقة هدايا (إما لإصدار بطاقة هدايا أو لإضافة بطاقة هدايا)</span><span class="sxs-lookup"><span data-stu-id="c3285-130">Gift card lines (either to issue a gift card or to add to the gift card balance)</span></span>

<span data-ttu-id="c3285-131">لا تؤثر الحركة المعلقة على معلومات المبيعات أو معلومات توافر المخزون في المتجر.</span><span class="sxs-lookup"><span data-stu-id="c3285-131">A suspended transaction doesn't affect sales information or inventory availability information for the store.</span></span>

### <a name="resume-a-suspended-transaction"></a><span data-ttu-id="c3285-132">استئناف حركة معلقة</span><span class="sxs-lookup"><span data-stu-id="c3285-132">Resume a suspended transaction</span></span>

<span data-ttu-id="c3285-133">يمكن استدعاء الحركات المعلقة واستئنافها في المتجر نفسه من قبل أي مستخدم لديه امتيازات كافية، ولديه أيضًا تخطيط شاشة يتضمن عملية **استدعاء الحركة**.</span><span class="sxs-lookup"><span data-stu-id="c3285-133">Suspended transactions can be recalled and resumed in the same store by any user who has sufficient privileges, and who also has a layout that includes the **Recall transaction** operation.</span></span>

<span data-ttu-id="c3285-134">لاستدعاء حركة معلقة بسرعة وسهولة، يمكنك إجراء مسح ضوئي للكود الشريطي على الإيصال مطبوع أثناء عرض قائمة الحركات من عملية **استدعاء الحركة**.</span><span class="sxs-lookup"><span data-stu-id="c3285-134">To quickly and easily recall a suspended transaction, scan the barcode on the printed slip while you're viewing the list of transactions from the **Recall transaction** operation.</span></span>

### <a name="considerations-for-offline-mode"></a><span data-ttu-id="c3285-135">اعتبارات لوضع العمل دون اتصال</span><span class="sxs-lookup"><span data-stu-id="c3285-135">Considerations for offline mode</span></span>

- <span data-ttu-id="c3285-136">في وضع عدم الاتصال، لا يمكن استئناف الحركات التي تم تعليقها عندما كانت نقطة البيع في وضع الاتصال، نظرًا لتعذر مزامنة البيانات إلى قاعدة البيانات غير المتصلة.</span><span class="sxs-lookup"><span data-stu-id="c3285-136">Any transaction that is suspended while the POS is in online mode can't be resumed in offline mode, because the data isn't synced to the offline database.</span></span>
- <span data-ttu-id="c3285-137">إذا قمت بتعليق حركة أثناء وجود نقطة البيع في وضع عدم الاتصال، فيمكنك استدعاء هذه الحركة في وضع عدم الاتصال، شريطة ألا تكون نقطة البيع قد عادت إلى وضع الاتصال في أي وقت منذ أن قمت بتعليق الحركة.</span><span class="sxs-lookup"><span data-stu-id="c3285-137">If you suspend a transaction while the POS is in offline mode, you can recall it in offline mode, provided that the POS wasn't switched back to online mode at any time since you suspended the transaction.</span></span> <span data-ttu-id="c3285-138">عند تبديل نقطة البيع إلى وضع الاتصال، يتم نقله البيانات المتعلقة بالحركات المعلقة إلى قاعدة البيانات المتصلة وتتم إزالتها من قاعدة البيانات غير المتصلة.</span><span class="sxs-lookup"><span data-stu-id="c3285-138">When the POS is switched back to online mode, data about suspended transactions is moved to the online database and removed from the offline database.</span></span> <span data-ttu-id="c3285-139">وبالتالي، يمكن استئناف الحركات فقط في وضع الاتصال.</span><span class="sxs-lookup"><span data-stu-id="c3285-139">Therefore, the transactions can be resumed only in online mode.</span></span> <span data-ttu-id="c3285-140">إذا أعدت تبديل نقطة البيع إلى وضع عدم الاتصال، فسيتعذر عليك استئناف هذه الحركات المعلقة، وذلك بسبب إزالتها من قاعدة البيانات غير المتصلة.</span><span class="sxs-lookup"><span data-stu-id="c3285-140">If you switch the POS back to offline mode, you won't be able to resume those suspended transaction, because they have already been removed from the offline database.</span></span>

### <a name="void-a-suspended-transaction"></a><span data-ttu-id="c3285-141">إلغاء حركة معلقة</span><span class="sxs-lookup"><span data-stu-id="c3285-141">Void a suspended transaction</span></span>

<span data-ttu-id="c3285-142">يمكن إلغاء حركة معلقة إما عن طريق استدعائها ثم تنفيذ عملية **إلغاء الحركة**، أو عن طريق تحديد الحركة في قائمة **استدعاء الحركة** وتحديد **ملغي** في شريط التطبيق.</span><span class="sxs-lookup"><span data-stu-id="c3285-142">You can void suspended transactions either by recalling the transaction and then performing the **Void transaction** operation, or by selecting the transaction in the **Recall transaction** list and selecting **Void** on the app bar.</span></span> <span data-ttu-id="c3285-143">بدلاً من ذلك، يمكن تكوين المتجر لمطالبة المستخدمين بإلغاء الحركات المعلقة عند إغلاق وردية عملهم.</span><span class="sxs-lookup"><span data-stu-id="c3285-143">Alternatively, the store can be configured to prompt users to void suspended transactions when they close their shift.</span></span>
