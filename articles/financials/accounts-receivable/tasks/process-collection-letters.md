--- 
title: "معالجة خطابات التحصيل"
description: "يوضح هذا الإجراء كيفية إنشاء وطباعة وترحيل خطابات التحصيل."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 12/04/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.translationtype: HT
ms.sourcegitcommit: 18eaadf417ce6d0aacf0b13b3e4f857e06031e66
ms.openlocfilehash: 8a3f74d2891c050294e089eae14ba2386449d7c9
ms.contentlocale: ar-sa
ms.lasthandoff: 01/22/2019

---
# <a name="process-collection-letters"></a><span data-ttu-id="b5b12-103">معالجة خطابات التحصيل</span><span class="sxs-lookup"><span data-stu-id="b5b12-103">Process collection letters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b5b12-104">يوضح هذا الإجراء كيفية إنشاء وطباعة وترحيل خطابات التحصيل.</span><span class="sxs-lookup"><span data-stu-id="b5b12-104">This procedure shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="b5b12-105">تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="b5b12-105">This task uses the USMF demo company.</span></span>

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="b5b12-106">إعداد تسلسل خطاب تحصيل بملف تعريف الترحيل</span><span class="sxs-lookup"><span data-stu-id="b5b12-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="b5b12-107">انتقل إلى **التحصيلات والائتمان > الإعداد > ملفات تعريف ترحيل العميل**.</span><span class="sxs-lookup"><span data-stu-id="b5b12-107">Go to **Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="b5b12-108">انقر فوق **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="b5b12-108">Click **Edit**.</span></span>
3. <span data-ttu-id="b5b12-109">حدد تسلسل خطاب التحصيل من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="b5b12-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="b5b12-110">إذا كنت لا تريد إنشاء خطابات تحصيل للحركات باستخدام ملف تعريف الترحيل هذا، فاترك الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="b5b12-110">If you do not want to generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
4. <span data-ttu-id="b5b12-111">قم بتوسيع علامة التبويب "‏‫تقييدات الجداول"‬ لتغيير الطريقة التي تتم بها معالجة خطابات التحصيل.</span><span class="sxs-lookup"><span data-stu-id="b5b12-111">Expand the table restriction tab to change the way that collection letters are processed.</span></span> <span data-ttu-id="b5b12-112">إذا تم تعيين هذا الحقل إلى **نعم**، فسيتم إنشاء خطابات التحصيل لملف تعريف الترحيل هذا.</span><span class="sxs-lookup"><span data-stu-id="b5b12-112">If this field is set to **Yes**, then collection letters will be created for this posting profile.</span></span>  

## <a name="create-collection-letters"></a><span data-ttu-id="b5b12-113">إنشاء خطابات تحصيل</span><span class="sxs-lookup"><span data-stu-id="b5b12-113">Create collection letters</span></span>
1. <span data-ttu-id="b5b12-114">انتقل إلى **الائتمان والتحصيلات > خطاب التحصيل > إنشاء خطابات التحصيل**.</span><span class="sxs-lookup"><span data-stu-id="b5b12-114">Go to **Credit and collections > Collection letter > Create collection letters**.</span></span>
2. <span data-ttu-id="b5b12-115">حدد أنواع الحركات التي سيتم تحصيل الخطابات لها.</span><span class="sxs-lookup"><span data-stu-id="b5b12-115">Select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="b5b12-116">سيتم تضمين كافة الحركات المفتوحة لهذه الأنواع في الحساب.</span><span class="sxs-lookup"><span data-stu-id="b5b12-116">All of the open transactions for these types will be included in the calculation.</span></span>  
2. <span data-ttu-id="b5b12-117">حدد خيارًا في حقل **خطاب التحصيل**.</span><span class="sxs-lookup"><span data-stu-id="b5b12-117">In the **Collection letter** field, select an option.</span></span>
3. <span data-ttu-id="b5b12-118">أدخل تاريخ خطاب التحصيل.</span><span class="sxs-lookup"><span data-stu-id="b5b12-118">Enter the date of the collection letter.</span></span>
4. <span data-ttu-id="b5b12-119">حدد ملف تعريف ترحيل إذا قمت بتغيير **استخدام ملف تعريف الترحيل من** إلى **تحديد**.</span><span class="sxs-lookup"><span data-stu-id="b5b12-119">Select a posting profile if you changed **Use posting profile from** to **Select**.</span></span> <span data-ttu-id="b5b12-120">هناك خياران لملفات تعريف الترحيل:</span><span class="sxs-lookup"><span data-stu-id="b5b12-120">There are two posting profile options:</span></span>   
   - <span data-ttu-id="b5b12-121">**الحساب** – تستخدم ملف تعريف الترحيل الذي تم تعيينه لحساب العميل لكل إشعار فائدة.</span><span class="sxs-lookup"><span data-stu-id="b5b12-121">**Account** – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   
   - <span data-ttu-id="b5b12-122">**تحديد** – استخدم ملف تعريف الترحيل الذي حددته في الحقل **ملف تعريف الترحيل**.</span><span class="sxs-lookup"><span data-stu-id="b5b12-122">**Select** – Use the posting profile that you select in the **Posting profile** field.</span></span>  
5. <span data-ttu-id="b5b12-123">وسّع القسم **السجلات المطلوب تضمينها**.</span><span class="sxs-lookup"><span data-stu-id="b5b12-123">Expand the **Records to include** section.</span></span>
6. <span data-ttu-id="b5b12-124">انقر فوق **تصفية**.</span><span class="sxs-lookup"><span data-stu-id="b5b12-124">Click **Filter**.</span></span>
7. <span data-ttu-id="b5b12-125">في حقل **المعايير**، أدخل معرّف العميل.</span><span class="sxs-lookup"><span data-stu-id="b5b12-125">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="b5b12-126">على سبيل المثال، أدخل "US-001".</span><span class="sxs-lookup"><span data-stu-id="b5b12-126">For example, enter 'US-001'.</span></span>
8. <span data-ttu-id="b5b12-127">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b5b12-127">Click **OK**.</span></span>
9. <span data-ttu-id="b5b12-128">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b5b12-128">Click **OK**.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="b5b12-129">طباعة خطابات التحصيل</span><span class="sxs-lookup"><span data-stu-id="b5b12-129">Print collection letters</span></span>
1. <span data-ttu-id="b5b12-130">انتقل إلى **خطاب التحصيل > مراجعة خطابات التحصيل ومعالجتها**.</span><span class="sxs-lookup"><span data-stu-id="b5b12-130">Go to **Credit and collections > Collection letter > Review and process collection letters**.</span></span>
2. <span data-ttu-id="b5b12-131">في حقل **الحالة**، حدد **تم إنشاؤه**.</span><span class="sxs-lookup"><span data-stu-id="b5b12-131">In the **Status** field, select **Created**.</span></span>
3. <span data-ttu-id="b5b12-132">في الحقل **مطبوع**، حدد **غير مطبوع**.</span><span class="sxs-lookup"><span data-stu-id="b5b12-132">In the **Printed** field, select **Not printed**.</span></span>
4. <span data-ttu-id="b5b12-133">انقر فوق **طباعة**.</span><span class="sxs-lookup"><span data-stu-id="b5b12-133">Click **Print**.</span></span>
5. <span data-ttu-id="b5b12-134">انقر فوق **إشعار خطاب التحصيل**.</span><span class="sxs-lookup"><span data-stu-id="b5b12-134">Click **Collection letter note**.</span></span>
6. <span data-ttu-id="b5b12-135">وسّع القسم **السجلات المطلوب تضمينها**.</span><span class="sxs-lookup"><span data-stu-id="b5b12-135">Expand the **Records to include** section.</span></span>
7. <span data-ttu-id="b5b12-136">أدخل تاريخ الإيقاف للترحيلات.</span><span class="sxs-lookup"><span data-stu-id="b5b12-136">Enter the cutoff date for postings.</span></span>
8. <span data-ttu-id="b5b12-137">انقر فوق **موافق** لطباعة خطاب التحصيل.</span><span class="sxs-lookup"><span data-stu-id="b5b12-137">Click **OK** to print the collection letter.</span></span>
9. <span data-ttu-id="b5b12-138">قم بترحيل خطاب التحصيل.</span><span class="sxs-lookup"><span data-stu-id="b5b12-138">Post the collection letter.</span></span>
   1. <span data-ttu-id="b5b12-139">انقر فوق **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="b5b12-139">Click **Post**.</span></span>
   2. <span data-ttu-id="b5b12-140">أدخل تاريخ الترحيل لخطاب التحصيل.</span><span class="sxs-lookup"><span data-stu-id="b5b12-140">Enter the posting date for the collection letter.</span></span>
   3. <span data-ttu-id="b5b12-141">وسّع القسم **السجلات المطلوب تضمينها**.</span><span class="sxs-lookup"><span data-stu-id="b5b12-141">Expand the **Records to include** section.</span></span>
   4. <span data-ttu-id="b5b12-142">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b5b12-142">Click **OK**.</span></span>
   5. <span data-ttu-id="b5b12-143">في حقل **الحالة**، حدد **مرحّل**.</span><span class="sxs-lookup"><span data-stu-id="b5b12-143">In the **Status** field, select **Posted**.</span></span>
   6. <span data-ttu-id="b5b12-144">في الحقل **مطبوع**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="b5b12-144">In the **Printed** field, select an option.</span></span>

## <a name="control-collection-letters-at-the-customer-level"></a><span data-ttu-id="b5b12-145">مراقبة خطابات التحصيل ومستوى العميل</span><span class="sxs-lookup"><span data-stu-id="b5b12-145">Control collection letters at the customer level</span></span>
<span data-ttu-id="b5b12-146">يمكنك أيضًا إعداد خطابات تحصيل على مستوى العميل لتمكين تعقب كود خطاب التحصيل لكل حركة، غير أن معالجة خطابات التحصيل سوف تستند إلى مستوى خطاب تحصيل فردي تم تخزينه للعميل.</span><span class="sxs-lookup"><span data-stu-id="b5b12-146">You can also set up collection letters at the customer level so that the collection letter code for each transaction is tracked, but the collection letter processing will be based on a single collection letter level that is stored for the customer.</span></span> <span data-ttu-id="b5b12-147">سيحتوى خطاب التحصيل الفردي على جميع الحركات المستحقة للعميل.</span><span class="sxs-lookup"><span data-stu-id="b5b12-147">The single collection letter will contain all transactions that are overdue for the customer.</span></span> <span data-ttu-id="b5b12-148">نظرًا لتعقب أيام السماح الآن على مستوى العميل، لن يتم إرسال خطاب التحصيل التالي إلا بعد انقضاء أيام السماح لخطاب التحصيل التالي في التسلسل، حتى لو أصبحت الحركات مستحقة بعد إرسال خطاب التحصيل الأخير.</span><span class="sxs-lookup"><span data-stu-id="b5b12-148">Because the grace days are now tracked on the customer level, the next collection letter will not be sent until the number of grace days has passed for the next collection letter in the sequence, even though transactions become overdue after the last collection letter was sent.</span></span> <span data-ttu-id="b5b12-149">يؤدي هذا الخيار إلى خفض عدد خطابات التحصيل التي ترسلها إلى كل عميل,</span><span class="sxs-lookup"><span data-stu-id="b5b12-149">This option reduces the number of collection letters you will send per customer.</span></span> 

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a><span data-ttu-id="b5b12-150">إعداد العميل لمراقبة التحصيل ومستوى العميل</span><span class="sxs-lookup"><span data-stu-id="b5b12-150">Set up the customer to control collection letters at the customer level</span></span>
1.  <span data-ttu-id="b5b12-151">انتقل إلى **عمليات التحصيل والائتمان‬ > إعداد > محددات الحسابات المدينة‬** وانقر فوق علامة تبويب **التحصيلات**.</span><span class="sxs-lookup"><span data-stu-id="b5b12-151">Go to **Credit and collections > Setup > Accounts receivable parameters** and click the **Collections** tab.</span></span> 
2.  <span data-ttu-id="b5b12-152">غيّر قيمة **إنشاء خطاب تحصيل لكل‬** إلى **عميل**.</span><span class="sxs-lookup"><span data-stu-id="b5b12-152">Change the value of **Create collection letter per** to **Customer**.</span></span> 
3.  <span data-ttu-id="b5b12-153">انتقل إلى **خطاب التحصيل > مراجعة خطابات التحصيل ومعالجتها**.</span><span class="sxs-lookup"><span data-stu-id="b5b12-153">Go to **Credit and collections > Collection letter > Review and process collection letters**.</span></span> <span data-ttu-id="b5b12-154">سيتم إنشاء خطاب تحصيل واحد فقط لعميل مع جميع الحركات المستحقة.</span><span class="sxs-lookup"><span data-stu-id="b5b12-154">Only one collection letter will be generated for a customer with all the overdue transactions.</span></span>

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a><span data-ttu-id="b5b12-155">تجاهل المدفوعات والإشعارات الدائنة عند حساب كود خطاب التحصيل</span><span class="sxs-lookup"><span data-stu-id="b5b12-155">Ignore payments and credit memos when calculating the collection letter code</span></span>
<span data-ttu-id="b5b12-156">إذا قمت بتضمين المدفوعات والإشعارات الدائنة في الحركات التي سيتم تضمينها في خطابات التحصيل، قد يكون لديك مدفوعات وإشعارات دائنة ستؤدي إلى تشغيل حساب تحصيل.</span><span class="sxs-lookup"><span data-stu-id="b5b12-156">If you include payments and credit memos in the transactions that will be included in the collection letters, you may have payments or credit memos that will trigger a collection letter.</span></span> <span data-ttu-id="b5b12-157">يمكنك التحكم في كيفية قيام المدفوعات والإشعارات الدائنة بالتحكم في كود خطاب التحصيل عن طريقة تغيير القيمة في المعلمة **تجاهل المدفوعات والإشعارات الدائنة عند حساب كود خطاب التحصيل‬**.</span><span class="sxs-lookup"><span data-stu-id="b5b12-157">You can control how payments and credit memos control the collection letter code by changing the value of the **Ignore payments and credit memos when calculating the collection letter code** parameter.</span></span> 

<span data-ttu-id="b5b12-158">لتجاهل المدفوعات والإشعارات الدائنة عند حساب كود خطاب التحصيل، قم بما يلي:</span><span class="sxs-lookup"><span data-stu-id="b5b12-158">To ignore payments and credit memos when calculating the collection letter code, do the following.</span></span>
1. <span data-ttu-id="b5b12-159">انتقل إلى **عمليات التحصيل والائتمان‬ > إعداد > محددات الحسابات المدينة‬** وانقر فوق علامة تبويب **التحصيلات**.</span><span class="sxs-lookup"><span data-stu-id="b5b12-159">Go to **Credit and collections > Setup > Accounts receivable parameters** and click the **Collections** tab.</span></span> 
2. <span data-ttu-id="b5b12-160">قم بتغيير قيمة **تجاهل المدفوعات والإشعارات الدائنة عند حساب كود خطاب التحصيل** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="b5b12-160">Change the value of **Ignore payments and credit memos when calculating the collection letter code** to **Yes**.</span></span>

