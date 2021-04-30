---
title: عكس حركات الإيجار المرحّلة
description: يوضح هذا الموضوع كيفية عكس حركة إيجار مرحلة. يمكن عكس أية حركة يتم إنشاؤها خلال تأجير الأصول.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseLeaseTransactions
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 55eb7c5f2419bf1cb2ac0a33a82ab931a3ef380f
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881532"
---
# <a name="reverse-posted-lease-transactions"></a><span data-ttu-id="4dd9b-104">عكس حركات الإيجار المرحّلة</span><span class="sxs-lookup"><span data-stu-id="4dd9b-104">Reverse posted lease transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4dd9b-105">يمكن عكس أية حركة يتم إنشاؤها خلال تأجير الأصول.</span><span class="sxs-lookup"><span data-stu-id="4dd9b-105">Any transaction that is created through Asset leasing can be reversed.</span></span> <span data-ttu-id="4dd9b-106">الحركات التي يتم إلغاؤها خلال تحديث تأجير الأصول بيانات الإيجار الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="4dd9b-106">Transactions that are reversed through Asset leasing update your lease data.</span></span> <span data-ttu-id="4dd9b-107">وبالتالي، فإنها تقوم أيضًا بتحديث قيم الحمل الخاصة بالتزامات الإيجار وحق استخدام الأصل.</span><span class="sxs-lookup"><span data-stu-id="4dd9b-107">Therefore, they also update the carrying values of the lease liability and right-of-use (ROU) asset.</span></span>

<span data-ttu-id="4dd9b-108">لإنشاء حركة عكس الإيجار، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="4dd9b-108">To create a reversing transaction for a lease, follow these steps.</span></span>

1. <span data-ttu-id="4dd9b-109">إما في الصفحة **حركات الأصول** أو الصفحة **حركات الالتزام**، حدد الحركة، ثم حدد **عكس الحركة**.</span><span class="sxs-lookup"><span data-stu-id="4dd9b-109">On either the **Asset transactions** page or the **Liability transactions** page, select the transaction, and then select **Reverse transaction**.</span></span>
2. <span data-ttu-id="4dd9b-110">في مربع الحوار الذي يظهر، يمكنك تحرير التاريخ الذي سيتم فيه ترحيل الإدخال المعكوس.</span><span class="sxs-lookup"><span data-stu-id="4dd9b-110">In the dialog box that appears, you can edit the date when the reversing entry will be posted.</span></span> <span data-ttu-id="4dd9b-111">افتراضيًا، يتم تعيين الحقل **التاريخ** على تاريخ ترحيل الحركة الخاص بالحركة التي قمت بتحديدها.</span><span class="sxs-lookup"><span data-stu-id="4dd9b-111">By default, the **Date** field is set to the transaction posting date of the transaction that you selected.</span></span> <span data-ttu-id="4dd9b-112">لا يمكن ترحيل إدخال العكس قبل تاريخ الترحيل الأصلي للحركة المحددة.</span><span class="sxs-lookup"><span data-stu-id="4dd9b-112">The reversing entry can't be posted earlier than the original posting date of the selected transaction.</span></span>
3. <span data-ttu-id="4dd9b-113">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="4dd9b-113">Select **OK**.</span></span> <span data-ttu-id="4dd9b-114">يتم ترحيل إدخال دفتر اليومية الذي يعكس الإدخال الذي قمت بتحديده.</span><span class="sxs-lookup"><span data-stu-id="4dd9b-114">A journal entry is posted that reverses the entry that you selected.</span></span> <span data-ttu-id="4dd9b-115">يتم عرض العكس في الصفحة **حركات الأصول** أو **حركات الالتزام**، ويتم تحديث صافي إجمالي الرصيد الحالي الذي يتم عرضه في الصفحة.</span><span class="sxs-lookup"><span data-stu-id="4dd9b-115">The reversal is shown on the **Asset transactions** or **Liability transactions** page, and the net total of the current balance that is shown on the page is updated.</span></span>

<span data-ttu-id="4dd9b-116">عند تحديد **عكس التتبع**، يظهر مربع حوار يعرض الحركات الأصلية والحركات المعكوسة، مع الرقم المرتبط الذي يعرف *برقم التتبع*.</span><span class="sxs-lookup"><span data-stu-id="4dd9b-116">When you select **Reverse tracing**, a dialog box appears that shows both the original transactions and the reversed transactions, together with a linked number that is known as a *trace number*.</span></span> <span data-ttu-id="4dd9b-117">لجعل عمليات العكس أكثر سهولة لفهم وتحسين الرؤية، فإنه يمكنك أيضًا تتبع عمليات العكس باستخدام جداول الإيجار.</span><span class="sxs-lookup"><span data-stu-id="4dd9b-117">To make the reversals easier to understand and to improve visibility, you can also track reversals by using the lease schedules.</span></span>

<span data-ttu-id="4dd9b-118">يعرض الحقل **رقم دفتر اليومية الأحدث** الموجود في الصفحة **الجدول** أرقام دفاتر اليومية الخاصة بالحركات.</span><span class="sxs-lookup"><span data-stu-id="4dd9b-118">The **Latest journal number** field on the **Schedule** page shows the journal numbers of transactions.</span></span> <span data-ttu-id="4dd9b-119">عند عكس إحدى الحركات، يتم تحديث هذا الحقل برقم دفتر اليومية الخاص بحركة العكس.</span><span class="sxs-lookup"><span data-stu-id="4dd9b-119">When a transaction is reversed, this field is updated with the journal number of a reversing transaction.</span></span> <span data-ttu-id="4dd9b-120">بالإضافة إلى ذلك، يتم تحديد خانة الاختيار **معكوس** للإشارة إلى أنه قد تم عكس الحركة، ويتم تحديد الحقل **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="4dd9b-120">Additionally, the **Reversed** check box is selected to indicate that the transaction is reversed, and the **Posted** field is selected.</span></span>

## <a name="revoke-a-reversed-transaction"></a><span data-ttu-id="4dd9b-121">إبطال حركة معكوسة</span><span class="sxs-lookup"><span data-stu-id="4dd9b-121">Revoke a reversed transaction</span></span>

<span data-ttu-id="4dd9b-122">لإبطال حركة معكوسة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="4dd9b-122">To revoke a reversed transaction, follow these steps.</span></span>

1. <span data-ttu-id="4dd9b-123">في الصفحة **الجدولة** أو الصفحة **الحركات**، حدد الحركة الأصلية.</span><span class="sxs-lookup"><span data-stu-id="4dd9b-123">On either the **Schedule** page or the **Transactions** page, select the original transaction.</span></span>
2. <span data-ttu-id="4dd9b-124">اتبع إحدى الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="4dd9b-124">Follow one of these steps:</span></span>

    - <span data-ttu-id="4dd9b-125">إذا قمت بتحديد الحركة في الصفحة **الجدول**، اتبع الخطوات الخاصة بإنشاء دفتر يومية في [إنشاء إدخالات دفتر يومية في دُفعة شهريًا](create-monthly-journals-batch.md).</span><span class="sxs-lookup"><span data-stu-id="4dd9b-125">If you selected the transaction on the **Schedule** page, follow the steps for creating a journal in [Create monthly journal entries in a batch](create-monthly-journals-batch.md).</span></span> <span data-ttu-id="4dd9b-126">يجب عليك ترحيل دفتر اليومية يدويًا.</span><span class="sxs-lookup"><span data-stu-id="4dd9b-126">You must manually post the journal.</span></span>
    - <span data-ttu-id="4dd9b-127">إذا قمت بتحديد الحركة الصفحة **الحركات**، فحدد **عكس الحركة**.</span><span class="sxs-lookup"><span data-stu-id="4dd9b-127">If you selected the transaction on the **Transactions** page, select **Reverse transaction**.</span></span> <span data-ttu-id="4dd9b-128">تظهر رسالة توضح أن هذا الإبطال عبارة عن إبطال لعملية عكس سابقة، ويمكنك تحرير تاريخ الترحيل لهذا الإبطال.</span><span class="sxs-lookup"><span data-stu-id="4dd9b-128">You receive a message that states that this revocation is a revocation of an earlier reversal, and that you can edit the posting date for this revocation.</span></span> <span data-ttu-id="4dd9b-129">ومع ذلك، فإن عمليات التحقق من الأعمال العامة تؤثر على التواريخ التي يمكن إدخالها في الحقل **التاريخ**.</span><span class="sxs-lookup"><span data-stu-id="4dd9b-129">However, general business validations affect the dates that can be entered in the **Date** field.</span></span> 

3. <span data-ttu-id="4dd9b-130">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="4dd9b-130">Select **OK**.</span></span> <span data-ttu-id="4dd9b-131">يتم ترحيل إدخال دفتر اليومية الذي يعكس الإدخال الذي قمت بتحديده.</span><span class="sxs-lookup"><span data-stu-id="4dd9b-131">A journal entry is posted that reverses the entry that you selected.</span></span> <span data-ttu-id="4dd9b-132">يتم عرض العكس في الصفحة **الحركات**، ويتم استعادة صافي إجمالي الرصيد الحالي إلى ما كانت عليه قبل عملية العكس الأول.</span><span class="sxs-lookup"><span data-stu-id="4dd9b-132">The reversal is shown on the **Transactions** page, and the net total current balance is restored to what it was before the first reversal.</span></span> <span data-ttu-id="4dd9b-133">وبالتالي، يكون تأثير العكس على الأرصدة سلبيًا.</span><span class="sxs-lookup"><span data-stu-id="4dd9b-133">Therefore, the impact that the reversal had on the balances is negated.</span></span>

<span data-ttu-id="4dd9b-134">عند تحديد **عكس التتبع**، يظهر مربع الحوار الذي يعرض الحركات الأصلية والحركات المعكوسة، مع رقم التتبع المرتبط.</span><span class="sxs-lookup"><span data-stu-id="4dd9b-134">When you select **Reverse tracing**, a dialog box appears that shows both the original transactions and the reversed transactions, together with a linked trace number.</span></span>

<span data-ttu-id="4dd9b-135">كما يمكنك أيضًا تتبع عمليات الإبطال باستخدام صفحة **الجداول** المناسبة.</span><span class="sxs-lookup"><span data-stu-id="4dd9b-135">You can also track revocations by using the appropriate **Schedules** page.</span></span> <span data-ttu-id="4dd9b-136">يتم إلغاء الحقل **عكس**، بينما يتم تحديد الحقل **دفتر اليومية المرحل**.</span><span class="sxs-lookup"><span data-stu-id="4dd9b-136">The **Reverse** field is cleared, whereas the **Journal posted** field is selected.</span></span> <span data-ttu-id="4dd9b-137">بالإضافة إلى ذلك، يتم تحديث الحقل **رقم دفتر اليومية الأحدث** برقم دفتر اليومية لحركة الإبطال، ويتم تحديث الحقل **رقم دفتر اليومية** برقم دفتر اليومية العكسي.</span><span class="sxs-lookup"><span data-stu-id="4dd9b-137">Additionally, the **Latest journal number** field is updated with the journal number of the revocation transaction, and the **Journal number** field is updated with the reversal journal number.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
