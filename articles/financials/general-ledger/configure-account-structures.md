---
title: "تكوين بنيات حساب"
description: "يوفر هذا الموضوع معلومات عن بنيات الحساب والأبعاد المالية."
author: aprilolson
manager: AnnBe
ms.date: 05/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8435389a523d8393e9d4daa0cb1244203c0dbb12
ms.openlocfilehash: a0665f5aec2a0809ecb383c1d4adf4c2072c9569
ms.contentlocale: ar-sa
ms.lasthandoff: 05/21/2018

---

# <a name="configure-account-structures"></a><span data-ttu-id="07aff-103">تكوين بنيات حساب</span><span class="sxs-lookup"><span data-stu-id="07aff-103">Configure account structures</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="07aff-104">تستخدم بنيات الحساب الحساب الرئيسي والأبعاد المالية لإنشاء مجموعة من القواعد التي تحدد الأمر والقيم المستخدمة عند إدخال رقم الحساب.</span><span class="sxs-lookup"><span data-stu-id="07aff-104">Account structures use the main account and financial dimensions to create a set of rules that determine the order and values used when entering the account number.</span></span> <span data-ttu-id="07aff-105">يمكنك إعداد العديد من بنيات الحساب التي تحتاجها للعمل.</span><span class="sxs-lookup"><span data-stu-id="07aff-105">You can set up as many account structures as you need for your business.</span></span> <span data-ttu-id="07aff-106">يتم تعيين بنيات الحسابات لإعداد دفتر الأستاذ للشركة، وبالتالي يمكن مشاركتها.</span><span class="sxs-lookup"><span data-stu-id="07aff-106">The account structures are assigned to a company’s ledger setup, so they can be shared.</span></span>

<span data-ttu-id="07aff-107">عندما يتم إنشاء بنية حساب، يكون أقصى عدد للشرائح هو 11.</span><span class="sxs-lookup"><span data-stu-id="07aff-107">When creating an account structure, the maximum number of segments is 11.</span></span> <span data-ttu-id="07aff-108">إذا كنت بحاجة إلى شرائح أكثر من هذا، قم بتقييم إعدادك ومتطلباتك بالكامل، لأنها ستؤثر على تجربة المستخدم.</span><span class="sxs-lookup"><span data-stu-id="07aff-108">If you need more segments than this, thoroughly evaluate your setup and requirements, as it will impact the user experience.</span></span> <span data-ttu-id="07aff-109">ضع في اعتبارك إذا ما كانت الشريحة محددة في سيناريو إعداد التقرير باستخدام التدرج الهرمي بدلاً من وقت إدخال البيانات أو باستخدام حقل محدد من قبل المستخدم.</span><span class="sxs-lookup"><span data-stu-id="07aff-109">Consider if a segment could be derived in a reporting scenario using a hierarchy instead of during data entry, or by using a user-defined field.</span></span> <span data-ttu-id="07aff-110">على سبيل المثال، إذا كنت تريد الإبلاغ عن موقع، لكن يمكنك تقرير الموقع حسب القسم أو مركز التكلفة، لن تكون بحاجة إلى موقع كبُعد مالي.</span><span class="sxs-lookup"><span data-stu-id="07aff-110">For example, if you want to report on location, but you can figure location by department or cost center, you would not need location as a financial dimension.</span></span> <span data-ttu-id="07aff-111">بعد التقييم، إذا قمت بتحديد أنك بحاجة إلى أكثر من 11 شريحة، فإنه يمكنك إضافة شرائح إضافية باستخدام قواعد متقدمة.</span><span class="sxs-lookup"><span data-stu-id="07aff-111">If after evaluation you do determine more than 11 segments are needed, you can add additional segments using advanced rules.</span></span>

<span data-ttu-id="07aff-112">تتطلب بنيات الحساب الحساب الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="07aff-112">Account structures require the main account.</span></span> <span data-ttu-id="07aff-113">لا يتطلب الحساب الرئيسي أن يكون الشريحة الأولى في البنية، ولكنه لا يُحدد بنية الحساب التي يتم استخدامها أثناء إدخال رقم الحساب.</span><span class="sxs-lookup"><span data-stu-id="07aff-113">The main account does not need to be the first segment in the structure, but it does identify what account structure is being used during the account number entry.</span></span> <span data-ttu-id="07aff-114">بسبب هذا، يمكن أن تكون قيمة حساب رئيسي موجودة في بنية واحدة معينة إلى دفتر الأستاذ حتى لا تتداخل.</span><span class="sxs-lookup"><span data-stu-id="07aff-114">Because of this, a main account value can only exist in one structure assigned to the ledger so that they do not overlap.</span></span> <span data-ttu-id="07aff-115">بعد أن يتم تحديد بنية الحساب، فإنه تتم تصفية قائمة القيم المسموحة لإرشاد المستخدم خلال اختيار قيم الأبعاد الصالحة فقط، مما يعمل على تقليل احتمالية إدخال دفتر اليومية غير الصحيحة.</span><span class="sxs-lookup"><span data-stu-id="07aff-115">After the account structure is identified, the allowed values list is filtered to guide the user through picking only valid dimension values, decreasing the possibility of an incorrect journal entry.</span></span>

> [!NOTE] 
> <span data-ttu-id="07aff-116">إذا كنت تخطط للميزانية مقابل بُعد مالي، فإنها يجب أن تكون جزءًا من بنية الحساب.</span><span class="sxs-lookup"><span data-stu-id="07aff-116">If you plan to budget against a financial dimension, it will need to be part of an account structure.</span></span> <span data-ttu-id="07aff-117">إعداد الميزانية لا يستخدم قواعد متقدمة حاليًا.</span><span class="sxs-lookup"><span data-stu-id="07aff-117">Budgeting does not currently utilize advanced rules.</span></span>

## <a name="example"></a><span data-ttu-id="07aff-118">مثال</span><span class="sxs-lookup"><span data-stu-id="07aff-118">Example</span></span>
<span data-ttu-id="07aff-119">لتوضيح أفضل ممارسة لإعداد بنية حساب، فلنفترض أن شركة تريد تعقب حسابات الميزانية العمومية (100000..399999) في الحساب ومستوى بُعد مالي لوحدة الشركة.</span><span class="sxs-lookup"><span data-stu-id="07aff-119">To illustrate a best practice for setting up an account structure, let's assume that a company wants to track their balance sheet accounts (100000..399999) at the account and business unit financial dimension level.</span></span> <span data-ttu-id="07aff-120">بالنسبة لحسابات الإيراد والنفقات (400000..999999)، فإنها تتعقب وحدة أعمال البُعد المالي والقسم ومركز التكلفة.</span><span class="sxs-lookup"><span data-stu-id="07aff-120">For revenue and expense accounts (400000..999999), they track financial dimensions Business Unit, Department, and Cost center.</span></span> <span data-ttu-id="07aff-121">إذا قامت بتنفيذ عملية بيع، فإنها ترغب كذلك في تعقب العميل.</span><span class="sxs-lookup"><span data-stu-id="07aff-121">If they make a sale, they also like to track Customer.</span></span> <span data-ttu-id="07aff-122">باستخدام هذا السيناريو، فقد يُوصى بالحصول على بنيتي حساب معينة إلى دفتر أستاذ الشركة - بنية لحسابات الميزانية العمومية وبنية لحسابات الربح والخسارة.</span><span class="sxs-lookup"><span data-stu-id="07aff-122">Using this scenario, it would be recommended to have two account structures assigned to the company’s ledger - one for Balance sheet accounts, and one for Profit and Loss accounts.</span></span> <span data-ttu-id="07aff-123">لتحسين تجربة المستخدم والتحقق من صحتها، فإنه ينبغي أن يكون العميل قاعدة متقدمة يتم استخدامها عندما يتم استخدام حساب المبيعات فقط.</span><span class="sxs-lookup"><span data-stu-id="07aff-123">To optimize the user experience and validation, Customer should be an advanced rule that is only used when a sales account is used.</span></span>

<span data-ttu-id="07aff-124">**بنية حساب ميزانية عمومية**</span><span class="sxs-lookup"><span data-stu-id="07aff-124">**Balance sheet account structure**</span></span>

|<span data-ttu-id="07aff-125">الحساب الرئيسي</span><span class="sxs-lookup"><span data-stu-id="07aff-125">Main account</span></span>          | <span data-ttu-id="07aff-126">وحدة الأعمال</span><span class="sxs-lookup"><span data-stu-id="07aff-126">Business unit</span></span>    |
|----------------------|-----------|
|<span data-ttu-id="07aff-127">100000..399999</span><span class="sxs-lookup"><span data-stu-id="07aff-127">100000..399999</span></span> | <span data-ttu-id="07aff-128">\*;” “</span><span class="sxs-lookup"><span data-stu-id="07aff-128">\*;” “</span></span>|

<span data-ttu-id="07aff-129">**بنية حساب الربح والخسارة**</span><span class="sxs-lookup"><span data-stu-id="07aff-129">**Profit and loss account structure**</span></span>

|<span data-ttu-id="07aff-130">الحساب الرئيسي</span><span class="sxs-lookup"><span data-stu-id="07aff-130">Main account</span></span>          | <span data-ttu-id="07aff-131">وحدة الأعمال</span><span class="sxs-lookup"><span data-stu-id="07aff-131">Business unit</span></span>    |<span data-ttu-id="07aff-132">القسم</span><span class="sxs-lookup"><span data-stu-id="07aff-132">Department</span></span>          | <span data-ttu-id="07aff-133">مركز التكلفة</span><span class="sxs-lookup"><span data-stu-id="07aff-133">Cost center</span></span>    |
|----------------------|-----------|----------------------|-----------|
|<span data-ttu-id="07aff-134">400000..999999</span><span class="sxs-lookup"><span data-stu-id="07aff-134">400000..999999</span></span> | <span data-ttu-id="07aff-135">\*;” “</span><span class="sxs-lookup"><span data-stu-id="07aff-135">\*;” “</span></span>|<span data-ttu-id="07aff-136">\*;” “</span><span class="sxs-lookup"><span data-stu-id="07aff-136">\*;” “</span></span>|<span data-ttu-id="07aff-137">\*;” “</span><span class="sxs-lookup"><span data-stu-id="07aff-137">\*;” “</span></span>|<span data-ttu-id="07aff-138">\*;” “</span><span class="sxs-lookup"><span data-stu-id="07aff-138">\*;” “</span></span>|

<span data-ttu-id="07aff-139">**قاعدة متقدمة لإضافة عميل**</span><span class="sxs-lookup"><span data-stu-id="07aff-139">**Advanced rule for adding a Customer**</span></span>

<span data-ttu-id="07aff-140">المعايير: عندما يكون الحساب الرئيسي بين 400000 و499999، قم بأضف عميل.</span><span class="sxs-lookup"><span data-stu-id="07aff-140">Criteria: Where Main account is between 400000 and 499999, then add customer.</span></span> <span data-ttu-id="07aff-141">لا يمكن أن يُترك فارغًا.</span><span class="sxs-lookup"><span data-stu-id="07aff-141">It cannot be left blank.</span></span>

|<span data-ttu-id="07aff-142">العميل</span><span class="sxs-lookup"><span data-stu-id="07aff-142">Customer</span></span>         |
|-----------------|
|* |

<span data-ttu-id="07aff-143">في هذا المثال المبسط، يُسمح بكل القيم والفراغات، لذلك فإنه يتم استخدام \* و" ".</span><span class="sxs-lookup"><span data-stu-id="07aff-143">In this simplified example, all values and blank are allowed so \* and “ “ are used.</span></span>

## <a name="segments-and-allowed-values"></a><span data-ttu-id="07aff-144">المقاطع والقيم المسموح بها</span><span class="sxs-lookup"><span data-stu-id="07aff-144">Segments and allowed values</span></span>
<span data-ttu-id="07aff-145">يقدم قسم **الشرائح** و **تفاصيل القيم المسموح بها** شبكة مثل تجربة إدخال القواعد التي سيتم اتباعها عند التحقق من الصحة أثناء النشر.</span><span class="sxs-lookup"><span data-stu-id="07aff-145">The **Segments** and **Allowed values details** section provides a grid like experience for entering the rules that will be followed on validation during posting.</span></span> <span data-ttu-id="07aff-146">يمكنك الكتابة مباشرة في الخلايا داخل الشبكة أو استيرادها من Excel أو استخدام قسم **تفاصيل القيم المسموح بها** لإرشادك خلالها.</span><span class="sxs-lookup"><span data-stu-id="07aff-146">You can type directly in the cells in the grid, import it from Excel, or use the **Allowed value details** section to guide you through it.</span></span>

<span data-ttu-id="07aff-147">يرشدك القسم **تفاصيل القيم المسموح بها** خلال عملية إنشاء المعايير باستخدام **العوامل** مثل البدء بـ ويكون بين ويتضمن والعديد من العوامل.</span><span class="sxs-lookup"><span data-stu-id="07aff-147">The **Allowed value details** section guides you through creating criteria using **Operators** such as begins with, is between, includes, and many others.</span></span>

<span data-ttu-id="07aff-148">[![السماح بالقيم](./media/account.png)](./media/account.png)</span><span class="sxs-lookup"><span data-stu-id="07aff-148">[![Allow values](./media/account.png)](./media/account.png)</span></span> 

## <a name="more-than-7-criteria-needed"></a><span data-ttu-id="07aff-149">أكثر من 7 معايير ضرورية</span><span class="sxs-lookup"><span data-stu-id="07aff-149">More than 7 criteria needed</span></span>

<span data-ttu-id="07aff-150">إذا كان لديك أكثر من 7 معايير تحتاج إليها، فإنه يمكنك الاستمرار في إضافتها في السطر التالي.</span><span class="sxs-lookup"><span data-stu-id="07aff-150">If you have more than 7 criteria that are needed, you can continue adding them on the next line.</span></span> <span data-ttu-id="07aff-151">ستُلاحظ عند العمل في القسم **تفاصيل القيم المسموح بها** أن المعايير **+إضافة جديد** لم تعد نشطة بعد الآن بعد أن يتم إدخال المعايير السابعة.</span><span class="sxs-lookup"><span data-stu-id="07aff-151">You will notice when working in the **Allowed value details** section that the **+Add new** criteria is nt longer active after the seventh criteria is entered.</span></span> <span data-ttu-id="07aff-152">وهذا بسبب العديد من العوامل مثل:</span><span class="sxs-lookup"><span data-stu-id="07aff-152">This is due to many factors such as:</span></span> 
 - <span data-ttu-id="07aff-153">عرض العمود</span><span class="sxs-lookup"><span data-stu-id="07aff-153">Column width</span></span> 
 - <span data-ttu-id="07aff-154">كيف يتم تخزين البيانات</span><span class="sxs-lookup"><span data-stu-id="07aff-154">How the data is stored</span></span> 
 - <span data-ttu-id="07aff-155">أداء عنصر تحكم **تفاصيل القيم المسموح بها**</span><span class="sxs-lookup"><span data-stu-id="07aff-155">Performance of the **Allowed value details** control</span></span>
 - <span data-ttu-id="07aff-156">الاستخدام</span><span class="sxs-lookup"><span data-stu-id="07aff-156">Usability</span></span>  
 
<span data-ttu-id="07aff-157">للاستمرار في إضافة معايير إضافية، انقر فوق **التكرار في الشريحة** و **قسم القيم المسموح بها**.</span><span class="sxs-lookup"><span data-stu-id="07aff-157">To continue to add additional criteria, click **Duplicate in the Segment** and **Allowed values section**.</span></span> <span data-ttu-id="07aff-158">وسينسخ هذا المعايير إلى سطر جديد.</span><span class="sxs-lookup"><span data-stu-id="07aff-158">This will copy the criteria to a new line.</span></span> <span data-ttu-id="07aff-159">يمكنك حينها الكتابة فوق القسم **تفاصيل القيم المسموح بها** أو تعديله.</span><span class="sxs-lookup"><span data-stu-id="07aff-159">You can then type over or modify the **Allowed value details** section.</span></span>

<span data-ttu-id="07aff-160">(ارتباط إلى الفيديو الذي سيتم إنشاؤه)</span><span class="sxs-lookup"><span data-stu-id="07aff-160">(LINK TO VIDEO THAT WILL BE CREATED)</span></span>

## <a name="best-practices"></a><span data-ttu-id="07aff-161">أفضل الممارسات</span><span class="sxs-lookup"><span data-stu-id="07aff-161">Best practices</span></span>
<span data-ttu-id="07aff-162">عند إعداد بنيات حسابك، توجد بعض أفضل الممارسات التي يمكنك اتباعها.</span><span class="sxs-lookup"><span data-stu-id="07aff-162">When setting up your account structures there are some best practices you can follow.</span></span> <span data-ttu-id="07aff-163">وعلى الرغم من ذلك، يكون هذا إرشاد فقط، لذلك ينبغي وضع مناقشة كاملة عن شركتك وخطة النمو وخطة الصيانة في الاعتبار كجزء من تلك المناقشة.</span><span class="sxs-lookup"><span data-stu-id="07aff-163">However, this is only guidance so a holistic discussion about your business, growth plan, and maintenance plan should be considered as part of that discussion.</span></span>

- <span data-ttu-id="07aff-164">قم بعمل حساب رئيسي أولاً أو قريب من بنية الحساب قدر المستطاع، لذلك، يحصل المستخدمون على أفضل تجربة إرشادية يستطيعون الوصول إليها أثناء إدخال الحساب.</span><span class="sxs-lookup"><span data-stu-id="07aff-164">Make main account first or as close to the front of the account structure as possible, so users get the best guided experience they can during account entry.</span></span>

- <span data-ttu-id="07aff-165">قم بإعادة استخدام بنيات الحساب قدر الإمكان لتقليل الصيانة عبر الكيانات القانونية.</span><span class="sxs-lookup"><span data-stu-id="07aff-165">Reuse account structures as much as possible to reduce maintenance across your legal entities.</span></span>

- <span data-ttu-id="07aff-166">بالنسبة إلى الاختلافات بين الكيانات القانونية، ضع في اعتبارك استخدام القواعد المتقدمة حتى يمكن إعادة استخدام بنيات الحساب.</span><span class="sxs-lookup"><span data-stu-id="07aff-166">For variations across legal entities, consider using advanced rules so that account structures can be reused.</span></span>

- <span data-ttu-id="07aff-167">عند تعريف القيم المسموحة، استخدم النطاقات وأحرف البدل قدر المستطاع.</span><span class="sxs-lookup"><span data-stu-id="07aff-167">When defining allowed values, use ranges and wildcards as much as possible.</span></span> <span data-ttu-id="07aff-168">وهذا لا يسمح لك بالنمو والتغيير دون صيانة فقط، ولكن يقوم النظام بالتنفيذ بشكل أكثر مثالية باستخدام هذا التكوين أيضًا.</span><span class="sxs-lookup"><span data-stu-id="07aff-168">This not only allows you to grow and change without maintenance, but the system also performs more ideally with this configuration.</span></span>

- <span data-ttu-id="07aff-169">لا تقتصر على وضع علامة نجمية لكل شريحة في بنية الحساب، بل اعتمد على القواعد المتقدمة فقط.</span><span class="sxs-lookup"><span data-stu-id="07aff-169">Do not just put an asterisk for every segment in the account structure and then solely rely on the advanced rules.</span></span> <span data-ttu-id="07aff-170">قد يصعب إدارة هذا وغالبًا ما يؤدي إلى خطأ المستخدم أثناء الصيانة التي يمكن أن تجعل النظام غير قادر على النشر.</span><span class="sxs-lookup"><span data-stu-id="07aff-170">This can be difficult to manage and often leads to user error during maintenance that can make the system unable to post.</span></span>

## <a name="account-structure-activation"></a><span data-ttu-id="07aff-171">تنشيط بنية الحساب</span><span class="sxs-lookup"><span data-stu-id="07aff-171">Account structure activation</span></span>
<span data-ttu-id="07aff-172">عندما تكون راضيًا بالإعداد الجديد أو بالتغيير إلى بنية الحساب، فإنه يجب تنشيطه.</span><span class="sxs-lookup"><span data-stu-id="07aff-172">When you are satifisfied with your new setup or a change to an account structure, you must activate it.</span></span> <span data-ttu-id="07aff-173">إذا تم تعيين بنية حساب إلى دفتر الأستاذ، يمكن أن يكون هذا التنشيط عملية طويلة المدة، لأن كل المعاملات غير المنشورة في النظام يجب مزامنتها للبنية الجديدة.</span><span class="sxs-lookup"><span data-stu-id="07aff-173">If an account structure is assigned to a ledger, this activation can be a long running process, as all unposted transactions in the system must be synced to the new structure.</span></span> <span data-ttu-id="07aff-174">لن تتأثر المعاملات المنشورة بتغييرات بنية الحساب.</span><span class="sxs-lookup"><span data-stu-id="07aff-174">Posted transactions are not impacted with account structure changes.</span></span>

<span data-ttu-id="07aff-175">للحصول على المزيد من المعلومات، راجع [خطط دليل الحسابات الخاص بك‬‏‫](plan-chart-of-accounts.md)، و [الأبعاد المالية](financial-dimensions.md) و [‬‏‫إدخال مجموعات الحسابات والأبعاد (عنصر تحكم في الإدخال المقسم)](enter-account-dimension-combinations-segmented-entry-control.md).</span><span class="sxs-lookup"><span data-stu-id="07aff-175">For more information, see [Plan your chart of accounts](plan-chart-of-accounts.md), [Financial dimensions](financial-dimensions.md) and [Enter account and dimension combinations (segmented entry control)](enter-account-dimension-combinations-segmented-entry-control.md).</span></span>
