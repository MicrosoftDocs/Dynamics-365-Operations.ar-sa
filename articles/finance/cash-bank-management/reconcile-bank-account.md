---
title: تسوية حساب بنكي
description: يصف هذا الموضوع كيفية تسوية حساب بنكي.
author: panolte
manager: AnnBe
ms.date: 07/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: da8558f42bcd9daf95cacb17cebf4d9371dd514c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5262852"
---
# <a name="reconcile-a-bank-account"></a><span data-ttu-id="080db-103">تسوية حساب بنكي</span><span class="sxs-lookup"><span data-stu-id="080db-103">Reconcile a bank account</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="080db-104">عندما تلقى كشف حساب مصرفي، يجب عليك تسوية الحركات البنكية للكيان القانوني مع الحركات في كشف الحساب البنكي، بشكل دوري.</span><span class="sxs-lookup"><span data-stu-id="080db-104">When you receive a bank statement, you should periodically reconcile legal entity bank transactions with the transactions on the bank statement.</span></span>

<span data-ttu-id="080db-105">لا يمكنك تسوية كشف حساب بنكي مع حساب بنكي إذا كانت حالة أي من الشيكات أو مدفوعات قسيمة الإيداع المسرودة في الكشف هي **إلغاء معلق‬** في الوقت الحالي.</span><span class="sxs-lookup"><span data-stu-id="080db-105">You cannot reconcile a bank statement with a bank account if any of the checks or deposit slip payments that are listed on the statement currently have a status of **Pending cancellation**.</span></span> <span data-ttu-id="080db-106">بعد قيام أحد المراجعين بترحيل عملية عكس الشيك أو عملية إلغاء دفع قسيمة الإيداع أو قيامه برفض أي العمليتين، فلن تكون الحالة **إلغاء معلق‬**، ويمكن حينئذٍ تسوية الحساب البنكي.</span><span class="sxs-lookup"><span data-stu-id="080db-106">After a reviewer posts or rejects a check reversal or deposit slip payment cancellation, the status is no longer **Pending cancellation**, and you can reconcile the bank account.</span></span>

1.  <span data-ttu-id="080db-107">انتقل إلى **إدارة النقد والبنوك** \> **الحسابات البنكية** \> **الحسابات البنكية**.</span><span class="sxs-lookup"><span data-stu-id="080db-107">Go to **Cash and bank management** \> **Bank Accounts** \> **Bank accounts**.</span></span> <span data-ttu-id="080db-108">حدد الحساب البنكي الذي تريد تسويته مع كشف الحساب البنكي وحد **تسوية** > **تسوية الحساب**.</span><span class="sxs-lookup"><span data-stu-id="080db-108">Select the bank account to reconcile with the bank statement and select **Reconcile** > **Account reconciliation**.</span></span>

2.  <span data-ttu-id="080db-109">أدخل معلومات في الحقلين **تاريخ كشف الحساب البنكي** و **كشف الحساب البنكي**.</span><span class="sxs-lookup"><span data-stu-id="080db-109">Enter information in the **Bank statement date** and **Bank statement** fields.</span></span> <span data-ttu-id="080db-110">في الحقل **رصيد ختامي‬**، يمكنك إدخال رصيد الحساب البنكي كما يظهر في كشف الحساب البنكي.</span><span class="sxs-lookup"><span data-stu-id="080db-110">In the **Ending balance** field, you can enter the balance of the bank account as it appears on the bank statement.</span></span>

3.  <span data-ttu-id="080db-111">حدد **الحركات** لفتح صفحة‏‎ **تسوية الحساب**.</span><span class="sxs-lookup"><span data-stu-id="080db-111">Select **Transactions** to open the **Account reconciliation** page.</span></span>

4.  <span data-ttu-id="080db-112">لكل حركة مضمنة في كشف الحساب البنكي، حدد خانة الاختيار **تمت تسويته‬** إذا كان المبلغ في Dynamics 365 Finance يتطابق مع المبلغ على كشف الحساب البنكي.</span><span class="sxs-lookup"><span data-stu-id="080db-112">For each transaction that is included on the bank statement, select the **Cleared** check box if the amount in Dynamics 365 Finance corresponds to the amount on the bank statement.</span></span> <span data-ttu-id="080db-113">يمكنك أيضًا إدخال القيمة أو تعديلها في حقل **‏‫نوع الحركة البنكية‬**.</span><span class="sxs-lookup"><span data-stu-id="080db-113">You can also enter or modify the value in the **Bank transaction type** field.</span></span> <span data-ttu-id="080db-114">تعتبر قيمة الحقل هذه ضرورية لإحصائيات الحركات البنكية وبعض التقارير.</span><span class="sxs-lookup"><span data-stu-id="080db-114">This field value is important for bank transaction statistics and for some reports.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="080db-115">لا تحدد خانة الاختيار <STRONG>تمت تسويته‬</STRONG> للحركات التي لا تظهر في كشف الحساب البنكي.</span><span class="sxs-lookup"><span data-stu-id="080db-115">Do not select the <STRONG>Cleared</STRONG> check box for transactions that are not on the bank statement.</span></span> <span data-ttu-id="080db-116">سيستمر ظهور هذه الحركات في هذا الصفحة حتى تتم تسويتها مع كشف حساب بنكي مستقبلي.</span><span class="sxs-lookup"><span data-stu-id="080db-116">These transactions will continue to be displayed in on this page until they are reconciled with a future bank statement.</span></span></P>
    > <P><span data-ttu-id="080db-117">لا تتوفر خانة الاختيار <STRONG>تمت تسويته‬</STRONG> إذا كانت حالة الحركة <STRONG>إلغاء معلق‬</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="080db-117">The <STRONG>Cleared</STRONG> check box is not available if the transaction has a status of <STRONG>Pending cancellation</STRONG>.</span></span> <span data-ttu-id="080db-118">قد تظهر هذه الحالة للحركات إذا تم إعداد Finance بحيث يطالب بإرسال عمليات العكس أو الإلغاء للمراجعة قبل ترحيلها.</span><span class="sxs-lookup"><span data-stu-id="080db-118">Transactions might have this status if Finance is set up to require that reversals or cancellations be sent to review before they are posted.</span></span> <span data-ttu-id="080db-119">بعد قيام أحد المراجعين بترحيل عملية العكس أو الإلغاء، فلن تكون الحالة <STRONG>إلغاء معلق‬</STRONG>، ويمكن تسوية الحساب البنكي مع كشف الحساب البنكي.</span><span class="sxs-lookup"><span data-stu-id="080db-119">After a reviewer posts or rejects the reversal or cancellation, the status is no longer <STRONG>Pending cancellation</STRONG>, and you can reconcile the bank account with the bank statement.</span></span></P>

    
    <span data-ttu-id="080db-120">لتحديد خانة الاختيار **تمت تسويته** لفترة شيكات تظهر على كشف الحساب البنكي، حدد **تمييز فترة الشيك‬**، ثم يمكنك الإشارة إلى الفترة.</span><span class="sxs-lookup"><span data-stu-id="080db-120">To select the **Cleared** check box for an interval of checks that all are displayed on the bank statement, select **Mark check interval**, and then indicate the interval.</span></span>

5.  <span data-ttu-id="080db-121">إذا كان مبلغ حركة حساب بنكي لا يتوافق مع مبلغ الحركة في كشف الحساب البنكي، فأدخل قيمة التصحيح‬ في حقل **قيمة التصحيح‬**.</span><span class="sxs-lookup"><span data-stu-id="080db-121">If the amount for a bank account transaction does not correspond to the amount for the transaction on the bank statement, enter the amount of the correction in the **Correction amount** field.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="080db-122">إذا كانت الفترة المحاسبية للحركة المراد تصحيحها مغلقة، فلا استخدام الحقل <STRONG>قيمة التصحيح</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="080db-122">If the fiscal period of the transaction to be corrected is closed, the <STRONG>Correction amount</STRONG> field cannot be used.</span></span> <span data-ttu-id="080db-123">بدلاً من ذلك، أنشئ بندًا لديه تاريخ حركة في فترة مالية مفتوحة للتصحيح.</span><span class="sxs-lookup"><span data-stu-id="080db-123">Instead, create a line that has a transaction date that is in an open fiscal period for the correction.</span></span> <span data-ttu-id="080db-124">في هذه الحالة، يجب إضافة الأبعاد المالية التي تم استخدامها في الحركة الأصلية، وكذلك الحساب الرئيسي المقابل.</span><span class="sxs-lookup"><span data-stu-id="080db-124">In this case, you must add the financial dimensions that were used on the original transaction, and also the offset main account.</span></span></P>



6.  <span data-ttu-id="080db-125">قم بإنشاء حركات للإدخالات، مثل الرسوم والفائدة، الموجودة في كشف الحساب البنكي ولكنها غير مٌسجلة في Finance.</span><span class="sxs-lookup"><span data-stu-id="080db-125">Create transactions for entries, such as fees and interest, that are on the bank statement but that are not recorded in Finance.</span></span> <span data-ttu-id="080db-126">أدخل **نوع الحركة البنكية** والأبعاد المالية المناسبة.</span><span class="sxs-lookup"><span data-stu-id="080db-126">Enter the **Bank transaction type** and appropriate financial dimensions.</span></span>

7.  <span data-ttu-id="080db-127">نظرًا لتمييز الحركات في كشف الحساب البنكي كـ **تمت تسويته**، فإن المبلغ الموجود في الحقل **لم تتم تسويته**، والذي يُعاد حسابه باستمرار كلما قمت بإجراء تغييرات، يقترب من الصفر.</span><span class="sxs-lookup"><span data-stu-id="080db-127">As the transactions on the bank statement are marked as **Cleared**, the amount in the **Unreconciled** field, which is recalculated continuously as you make changes, approaches zero.</span></span> <span data-ttu-id="080db-128">وعندما يصل إلى الصفر، انقر فوق **تسوية الحساب** لترحيل التسوية والحركات والتصحيحات التي قمت بإنشائها.</span><span class="sxs-lookup"><span data-stu-id="080db-128">When it reaches zero, select **Reconcile account** to post the reconciliation, and the transactions and corrections that you have created.</span></span>
    
    <span data-ttu-id="080db-129">بعد ترحيل التسوية، سيتعذر مراجعة أو تصحيح الحركات التي تم تضمينها، ولن تظهر في أية تسوية حساب مستقبلية.</span><span class="sxs-lookup"><span data-stu-id="080db-129">After the reconciliation is posted, the transactions that have been included cannot be modified or corrected, and they are not displayed for future account reconciliation.</span></span>

8.  <span data-ttu-id="080db-130">لعرض الحركات البنكية التي لم تتم تسويتها بعد، استخدم التقرير **حركات بنكية لم تتم تسويتها‬**.</span><span class="sxs-lookup"><span data-stu-id="080db-130">To view bank transactions that have not yet been reconciled, use the **Unreconciled bank transactions** report.</span></span> <span data-ttu-id="080db-131">لعرض كشف الحساب البنكي لحساب بنكي، استخدم تقرير **كشف الحساب البنكي**.</span><span class="sxs-lookup"><span data-stu-id="080db-131">To view the bank statement for a bank account, use the **Bank statement** report.</span></span>

## <a name="cancel-bank-statement-reconciliation"></a><span data-ttu-id="080db-132">إلغاء كشف حساب بنكي</span><span class="sxs-lookup"><span data-stu-id="080db-132">Cancel bank statement reconciliation</span></span> 

<span data-ttu-id="080db-133">تسمح لك وظيفة تسوية كشف الحساب البنكي بإلغاء تسوية كشف الحساب البنكي.</span><span class="sxs-lookup"><span data-stu-id="080db-133">The Cancel bank statement reconciliation functionality enables you to cancel bank statement reconciliation.</span></span> <span data-ttu-id="080db-134">لاستخدام هذه الميزة، يجب تمكين وظيفة **تسوية كشف الحساب البنكي** في مساحة عمل **إدارة الميزات**.</span><span class="sxs-lookup"><span data-stu-id="080db-134">To use this feature, enable the **Cancel bank statement reconciliation** feature in the **Feature management** workspace.</span></span> <span data-ttu-id="080db-135">تحتاج أيضًا إلى تمكين‏‎ معلمة **السماح بتحرير كشف الحساب البنكي**.</span><span class="sxs-lookup"><span data-stu-id="080db-135">You also need to enable the **Allow bank statement edit** parameter.</span></span> <span data-ttu-id="080db-136">للقيام بذلك، انتقل إلى **إدارة النقد والبنوك > الإعداد > معلمات إدارة النقد والبنوك > تسوية بنكية**.</span><span class="sxs-lookup"><span data-stu-id="080db-136">To do this, go to **Cash and bank management > Setup > Cash and bank management parameters > Bank reconciliation**.</span></span>
 
<span data-ttu-id="080db-137">لا يمكن إلغاء تسويات كشف الحساب البنكي إلا بالترتيب الزمني الذي تم إدخالها به.</span><span class="sxs-lookup"><span data-stu-id="080db-137">Bank statement reconciliations can only be canceled in the chronological order in which they were entered.</span></span> <span data-ttu-id="080db-138">عند إلغاء تسوية كشف حساب بنكي، سيتم عكس التصحيحات والحركات الجديدة وسيتم وضع علامة على كافة الحركات الأخرى على أنها لم تتم تسويتها.</span><span class="sxs-lookup"><span data-stu-id="080db-138">When a bank statement reconciliation is canceled, new transactions and corrections will be reversed and all other transactions will be marked as un-reconciled.</span></span>
 
<span data-ttu-id="080db-139">لإلغاء تسوية كشف الحساب البنكي، حدد الكشف البنكي وحدد **كشف حساب بنكي > إلغاء تسوية بنكية**.</span><span class="sxs-lookup"><span data-stu-id="080db-139">To cancel bank statement reconciliation, select the bank statement and select **Bank statement > Cancel bank reconciliation**.</span></span> <span data-ttu-id="080db-140">في صفحة **إلغاء تسوية بنكية**، أدخل **كود السبب**, و **التعليق على السبب‬** و **تاريخ الإلغاء**.</span><span class="sxs-lookup"><span data-stu-id="080db-140">On the **Cancel bank reconciliation** page, provide the **Reason code**, **Reason comment**, and **Cancellation date**.</span></span> <span data-ttu-id="080db-141">حدد **موافق** لبدء الإلغاء.</span><span class="sxs-lookup"><span data-stu-id="080db-141">Select **OK** to begin cancellation.</span></span> <span data-ttu-id="080db-142">ملاحظة: يجب أن يكون تاريخ إلغاء كشف الحساب البنكي في تاريخ كشف الحساب البنكي أو بعده.</span><span class="sxs-lookup"><span data-stu-id="080db-142">Note, the bank statement cancellation date must be on or after the bank statement date.</span></span> <span data-ttu-id="080db-143">بعد إلغاء تسوية كشف الحساب البنكي، سيتم تحديث حقل **تاريخ الإلغاء** بواسطة **تاريخ الإلغاء** المقدم.</span><span class="sxs-lookup"><span data-stu-id="080db-143">After the bank statement reconciliation has canceled, the **Cancellation date** field for the bank statement will be updated with the **Cancellation date** provided.</span></span> <span data-ttu-id="080db-144">حدد زر **الحركات** لعرض الحركات التي تم إلغاء التسوية لها.</span><span class="sxs-lookup"><span data-stu-id="080db-144">Select the **Transactions** button to view the transactions for which the reconciliation was canceled.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]