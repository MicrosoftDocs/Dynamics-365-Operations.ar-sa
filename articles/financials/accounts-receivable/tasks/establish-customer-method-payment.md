--- 
title: "‏‫وضع طريقة دفع العميل‬"
description: "إنشاء طريقة دفع لمدفوعات العميل."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: cabcfe83ac83a8210ce4e0d46a08acdc48f4bf3b
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="establish-customer-method-of-payment"></a><span data-ttu-id="b32be-103">‏‫وضع طريقة دفع العميل‬</span><span class="sxs-lookup"><span data-stu-id="b32be-103">Establish customer method of payment</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b32be-104">إنشاء طريقة دفع لمدفوعات العميل.</span><span class="sxs-lookup"><span data-stu-id="b32be-104">Create a method of payment for customer payments.</span></span> <span data-ttu-id="b32be-105">تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="b32be-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="b32be-106">انتقل إلى الحسابات المدينة > إعداد الدفعات > طرق الدفع.</span><span class="sxs-lookup"><span data-stu-id="b32be-106">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="b32be-107">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="b32be-107">Click New.</span></span>
3. <span data-ttu-id="b32be-108">في الحقل "طريقة الدفع"، أدخل معرفًا لطريقة الدفع.</span><span class="sxs-lookup"><span data-stu-id="b32be-108">In the Method of payment field, enter an ID for the method of payment.</span></span>
    * <span data-ttu-id="b32be-109">يظهر معرف طريقة الدفع على الفواتير والمدفوعات، لذا اجعله وصفيًا قدر الإمكان لفهم نوع الدفع الذي سيتم تسجيله، ولأي حساب بنكي.</span><span class="sxs-lookup"><span data-stu-id="b32be-109">The Method of payment ID is shown on invoices and payments, so make it descriptive enough to understand what type of payment is being recorded, and for what bank account.</span></span>  
4. <span data-ttu-id="b32be-110">في الحقل "الوصف"، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="b32be-110">In the Description field, enter a description.</span></span>
5. <span data-ttu-id="b32be-111">حدد حالة الدفع المطلوبة لترحيل لمدفوعات.</span><span class="sxs-lookup"><span data-stu-id="b32be-111">Select what payment status is required in order for payments to be posted.</span></span>
    * <span data-ttu-id="b32be-112">عند إنشاء دفعة العميل، لا يمكن ترحيلها إلا عندما تكون حالة الدفع مطابقة لحالة الدفع التي قمت بتعريفها هنا.</span><span class="sxs-lookup"><span data-stu-id="b32be-112">When creating a customer payment, it can only be posted when the payment status matches the payment status you define here.</span></span>  
6. <span data-ttu-id="b32be-113">حدد كيفية إنشاء مدفوعات العملاء للفواتير.</span><span class="sxs-lookup"><span data-stu-id="b32be-113">Select how customers payments should be created for invoices.</span></span>
    * <span data-ttu-id="b32be-114">يستخدم هذا الخيار فقط عند تشغيل مقترح دفع.</span><span class="sxs-lookup"><span data-stu-id="b32be-114">This option is only used when running a payment proposal.</span></span> <span data-ttu-id="b32be-115">يمكن استخدام مقترح الدفع لمدفوعات العميل عند إجراء خصومات مباشرة وسحب الأموال من الحسابات البنكية للعملاء.</span><span class="sxs-lookup"><span data-stu-id="b32be-115">A payment proposal could be used for customer payments when doing direct debits, and pulling the funds from the customers' bank accounts.</span></span>  
7. <span data-ttu-id="b32be-116">حدد نوع الدفع.</span><span class="sxs-lookup"><span data-stu-id="b32be-116">Select the type of payment.</span></span>
    * <span data-ttu-id="b32be-117">سيساعد نوع الدفع في تحديد ما إذا كانت عملية التحقق من الصحة ستحدث أم لا على الدفع.</span><span class="sxs-lookup"><span data-stu-id="b32be-117">The payment type will help determine whether some validation will occur or not on the payment.</span></span>  
8. <span data-ttu-id="b32be-118">حدد أنواع الحسابات التي سيتم ترحيل المدفوعات إليها.</span><span class="sxs-lookup"><span data-stu-id="b32be-118">Select what account type payments will post to.</span></span>
    * <span data-ttu-id="b32be-119">بشكل عام، يمكن تحديد "البنك" لهذا الخيار.</span><span class="sxs-lookup"><span data-stu-id="b32be-119">Typically, Bank would be selected for this option.</span></span>  
9. <span data-ttu-id="b32be-120">حدد الحساب البنكي الذي سيتم تسجيل هذه الدفعة فيه.</span><span class="sxs-lookup"><span data-stu-id="b32be-120">Select the bank account into which this payment will be recorded.</span></span>
10. <span data-ttu-id="b32be-121">أدخل نوع الحركة البنكية لتحديد نوع الدفع المستخدم من قبل البنك الذي تتعامل معه.</span><span class="sxs-lookup"><span data-stu-id="b32be-121">Enter the Bank transaction type to identify the type of payment used by your bank.</span></span>
    * <span data-ttu-id="b32be-122">يُستخدم نوع الحركة البنكية المستخدمة أثناء عملية التسويات البنكية، وبإمكانه تسهيل عملية التسوية.</span><span class="sxs-lookup"><span data-stu-id="b32be-122">The bank transaction type is used during the bank reconciliation process, and can make reconciliation easier.</span></span>  
11. <span data-ttu-id="b32be-123">حدد ما إذا كان سيتم ترحيل هذه الدفعة هذه مؤقتًا إلى حساب مؤقت.</span><span class="sxs-lookup"><span data-stu-id="b32be-123">Select whether this payment will temporarily post to a bridging account.</span></span>
    * <span data-ttu-id="b32be-124">إذا كنت تريد تجربة الوقت العائم لإجراء مخالصة مع المصرف، فاستخدم وظيفة المرحلة المؤقتة.</span><span class="sxs-lookup"><span data-stu-id="b32be-124">If you want to try the float time for a payment to clear the bank, use the Bridging functionality.</span></span> <span data-ttu-id="b32be-125">سيتم ترحيل الدفع مؤقتًا إلى حساب دفتر أستاذ حتى تتم المخالصة مع البنك، وفي هذا الوقت ستتنقل الدفعة إلى الحساب البنكي الذي قمت بتعريفه هنا.</span><span class="sxs-lookup"><span data-stu-id="b32be-125">The payment will temporarily post to a Ledger account until it clears the bank, at which time the payment will move to the bank account you defined here.</span></span>  
12. <span data-ttu-id="b32be-126">أدخل الحساب الرئيسي المستخدم للترحيل المؤقت.</span><span class="sxs-lookup"><span data-stu-id="b32be-126">Enter the main account used for the bridging posting.</span></span>
    * <span data-ttu-id="b32be-127">هذا هو الحساب الرئيسي الذي سيتم ترحيل الدفعة إليه بشكل مؤقت عند استخدام المرحلة المؤقتة.</span><span class="sxs-lookup"><span data-stu-id="b32be-127">This is the main account to which the payment will temporarily post if using bridging.</span></span>  
13. <span data-ttu-id="b32be-128">استخدم علامة التبويب "تنسيق الملف" لتحديد الإعداد لعمليات الدفع الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="b32be-128">Use the File format tab to define setting for electronic payments.</span></span>
14. <span data-ttu-id="b32be-129">استخدم علامة التبويب "التحكم في الدفع" لتحديد الحقول الإلزامية.</span><span class="sxs-lookup"><span data-stu-id="b32be-129">Use the Payment control tab to define fields that are mandatory.</span></span>
    * <span data-ttu-id="b32be-130">على سبيل المثال، إذا كنت تطالب بأن يتم إيداع كافة المدفوعات بطريقة الدفع هذه، فيمكنك تحديد هذا الخيار في علامة التبويب هذه.</span><span class="sxs-lookup"><span data-stu-id="b32be-130">For example, if you require all payments with this method of payment to be deposited, you can choose that option on this tab.</span></span>  
15. <span data-ttu-id="b32be-131">استخدم علامة التبويب "سمات الدفع‬" لتحديد سمات الدفع التي تريد استخدامه لطريقة الدفع هذه.</span><span class="sxs-lookup"><span data-stu-id="b32be-131">Use the Payment atrributes tab to define which payment attributes you want to use for this method of payment.</span></span>
16. <span data-ttu-id="b32be-132">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="b32be-132">Click Save.</span></span>


