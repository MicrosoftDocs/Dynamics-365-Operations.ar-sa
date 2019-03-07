---
title: إدخال عطاءات RFQ ومنح العقود ومقارنتها
description: يوضح هذا الإجراء كيفية إدخال الردود إلى RFQ والنتيجة ومقارنة العطاءات، وبعد ذلك منح العطاء إلى أحد الموردين.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, PurchRFQCaseTable, PurchRFQReplyTable, PurchRFQCompare, PurchRFQEditLines, PurchRFQEditLinesParameters, PurchTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7cd4876acfebcc9595abb358cfc9b355e93041d6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "349988"
---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a><span data-ttu-id="7cc77-103">إدخال عطاءات RFQ ومنح العقود ومقارنتها</span><span class="sxs-lookup"><span data-stu-id="7cc77-103">Enter and compare RFQ bids, and award contracts</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7cc77-104">يوضح هذا الإجراء كيفية إدخال الردود إلى RFQ والنتيجة ومقارنة العطاءات، وبعد ذلك منح العطاء إلى أحد الموردين.</span><span class="sxs-lookup"><span data-stu-id="7cc77-104">This procedure shows you how to enter replies to an RFQ, score and compare bids, and then award the bid to one of the vendors.</span></span> <span data-ttu-id="7cc77-105">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="7cc77-105">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="7cc77-106">قبل البدء، يجب أن يكون لديك RFQ يشتمل على بندين تم إرسالها إلى اثنين من الموردين على الأقل.</span><span class="sxs-lookup"><span data-stu-id="7cc77-106">Before you start, you must have an RFQ with two lines that has been sent to at least two vendors.</span></span> <span data-ttu-id="7cc77-107">يمكنك تشغيل الإجراء "إنشاء طلب عرض أسعار" كشرط مسبق لإنشاء هذا.</span><span class="sxs-lookup"><span data-stu-id="7cc77-107">You can run the "Create a request for quotation" procedure as a prerequisite to create this.</span></span> <span data-ttu-id="7cc77-108">إنك تحتاج إلى إعداد معايير تسجيل النقاط قبل أن يمكنك القيام بهذا الإجرء.</span><span class="sxs-lookup"><span data-stu-id="7cc77-108">You need to have set up scoring criteria before you can run this procedure.</span></span>


## <a name="enter-a-reply-from-a-vendor"></a><span data-ttu-id="7cc77-109">أدخل رد من المورد</span><span class="sxs-lookup"><span data-stu-id="7cc77-109">Enter a reply from a vendor</span></span>
1. <span data-ttu-id="7cc77-110">انتقل إلى التدبير وتحديد الموارد > طلبات عروض الأسعار‬ > كل طلبات عروض الأسعار‬.</span><span class="sxs-lookup"><span data-stu-id="7cc77-110">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="7cc77-111">حدد RFQ يحتوي على حالة مرسل وانقر فوق الارتباط الموجود في رقم حالة طلب عرض أسعار.</span><span class="sxs-lookup"><span data-stu-id="7cc77-111">Select an RFQ that has a status of Sent and click the link on the Request for quotation case number.</span></span>
    * <span data-ttu-id="7cc77-112">يجب أن يتم إرسال RFQ إلى 2 من الموردين على الأقل.</span><span class="sxs-lookup"><span data-stu-id="7cc77-112">The RFQ should have been sent to at least 2 vendors.</span></span>  
3. <span data-ttu-id="7cc77-113">انقر فوق العنوان للانتقال إلى قائمة الموردين.</span><span class="sxs-lookup"><span data-stu-id="7cc77-113">Click Header to go to the list of vendors.</span></span>
4. <span data-ttu-id="7cc77-114">حدد المورد الذي تريد تدخل له رد على طلب RFQ.</span><span class="sxs-lookup"><span data-stu-id="7cc77-114">Select the vendor for whom you want to enter a response on the RFQ.</span></span>
5. <span data-ttu-id="7cc77-115">انقر فوق إدخال رد.</span><span class="sxs-lookup"><span data-stu-id="7cc77-115">Click Enter reply.</span></span>
6. <span data-ttu-id="7cc77-116">في جزء الإجراءات، انقر فوق رد.</span><span class="sxs-lookup"><span data-stu-id="7cc77-116">On the Action Pane, click Reply.</span></span>
7. <span data-ttu-id="7cc77-117">انقر فوق نسخ بيانات للرد.</span><span class="sxs-lookup"><span data-stu-id="7cc77-117">Click Copy data to reply.</span></span>
    * <span data-ttu-id="7cc77-118">سيقوم هذا الإجراء بنسخ البيانات المحددة، على سبيل المثال، الكمية من حالة RFQ إلى رد RFQ.</span><span class="sxs-lookup"><span data-stu-id="7cc77-118">This action will copy selected data, for example, the quantity from the RFQ case to the RFQ reply.</span></span> <span data-ttu-id="7cc77-119">بدلاً من ذلك يمكنك تخطي هذا الإجراء وتعبئة كافة حقول الاستجابة يدويًا عندما تقوم بتحرير الرد.</span><span class="sxs-lookup"><span data-stu-id="7cc77-119">Alternatively you can skip this action and fill in all the response fields manually when you edit the reply.</span></span>  
8. <span data-ttu-id="7cc77-120">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="7cc77-120">Click Edit.</span></span>
9. <span data-ttu-id="7cc77-121">في حقل "سعر الوحدة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="7cc77-121">In the Unit price field, enter a number.</span></span>
10. <span data-ttu-id="7cc77-122">اختر بند عرض الأسعار الآخر.</span><span class="sxs-lookup"><span data-stu-id="7cc77-122">Choose the other quotation line.</span></span>
11. <span data-ttu-id="7cc77-123">في حقل "سعر الوحدة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="7cc77-123">In the Unit price field, enter a number.</span></span>

## <a name="score-the-bid"></a><span data-ttu-id="7cc77-124">تقييم العطاء</span><span class="sxs-lookup"><span data-stu-id="7cc77-124">Score the bid</span></span>
1. <span data-ttu-id="7cc77-125">انقر فوق رأس الصفحة للانتقال إلى تسجيل نقاط العطاء.</span><span class="sxs-lookup"><span data-stu-id="7cc77-125">Click Header to go to the scoring of the bid.</span></span>
2. <span data-ttu-id="7cc77-126">قم بتوسيع قسم تسجيل نقاط العطاء.</span><span class="sxs-lookup"><span data-stu-id="7cc77-126">Expand the Bid scoring section.</span></span>
3. <span data-ttu-id="7cc77-127">في حقل النقاط، أدخل رقمًا لأحد معايير تسجيل النقاط.</span><span class="sxs-lookup"><span data-stu-id="7cc77-127">In the Score field, enter a number for one of the scoring criteria.</span></span>
    * <span data-ttu-id="7cc77-128">إذا قمت بالتمرير على واحدة من معايير تسجيل النقاط، يظهر تلميح النطاق الذي لديك لتسجل به.</span><span class="sxs-lookup"><span data-stu-id="7cc77-128">If you hover over one of the scoring criteria a tooltip shows the range that you have to score within.</span></span> <span data-ttu-id="7cc77-129">في هذا العرض يمكنك إضافة رقم بين 1 و5 لأي معيار من المعايير.</span><span class="sxs-lookup"><span data-stu-id="7cc77-129">In this demo you can add a number between 1 and 5 to any of the criteria.</span></span>  
4. <span data-ttu-id="7cc77-130">حدد معيار تسجيل نقاط آخر.</span><span class="sxs-lookup"><span data-stu-id="7cc77-130">Select another scoring criterion.</span></span>
5. <span data-ttu-id="7cc77-131">في حقل النقاط، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="7cc77-131">In the Score field, enter a number.</span></span>
6. <span data-ttu-id="7cc77-132">قم بتوسيع قسم الاستبيانات.</span><span class="sxs-lookup"><span data-stu-id="7cc77-132">Expand the Questionnaires section.</span></span>
    * <span data-ttu-id="7cc77-133">إذا كان لحالة RFQ استبيان تم إرساله إلى الموردين، فإنه يمكنك إدخال ردودها في قسم الاستبيان.</span><span class="sxs-lookup"><span data-stu-id="7cc77-133">If the RFQ case has a questionnaire that was sent to the vendors, you can enter their responses in the questionnaire section.</span></span>  
7. <span data-ttu-id="7cc77-134">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7cc77-134">Close the page.</span></span>

## <a name="enter-a-reply-for-another-vendor"></a><span data-ttu-id="7cc77-135">أدخل رد لمورد آخر</span><span class="sxs-lookup"><span data-stu-id="7cc77-135">Enter a reply for another vendor</span></span>
1. <span data-ttu-id="7cc77-136">حدد المورد التالي بمسح المورد الذي أدخلت الرد له للتو ثم حدد الصف للمورد التالي.</span><span class="sxs-lookup"><span data-stu-id="7cc77-136">Select the next vendor by clearing the vendor you have just entered the reply for and then selecting the row for the next vendor.</span></span>
2. <span data-ttu-id="7cc77-137">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="7cc77-137">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="7cc77-138">انقر فوق إدخال رد.</span><span class="sxs-lookup"><span data-stu-id="7cc77-138">Click Enter reply.</span></span>
4. <span data-ttu-id="7cc77-139">انقر فوق نسخ بيانات للرد.</span><span class="sxs-lookup"><span data-stu-id="7cc77-139">Click Copy data to reply.</span></span>
5. <span data-ttu-id="7cc77-140">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="7cc77-140">Click Edit.</span></span>
6. <span data-ttu-id="7cc77-141">في حقل "سعر الوحدة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="7cc77-141">In the Unit price field, enter a number.</span></span>
7. <span data-ttu-id="7cc77-142">اختر بند عرض الأسعار الآخر.</span><span class="sxs-lookup"><span data-stu-id="7cc77-142">Choose the other quotation line.</span></span>
8. <span data-ttu-id="7cc77-143">في حقل "سعر الوحدة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="7cc77-143">In the Unit price field, enter a number.</span></span>

## <a name="score-the-second-bid"></a><span data-ttu-id="7cc77-144">تقييم العطاء الثاني</span><span class="sxs-lookup"><span data-stu-id="7cc77-144">Score the second bid</span></span>
1. <span data-ttu-id="7cc77-145">انقر فوق رأس الصفحة للانتقال إلى تسجيل نقاط العطاء.</span><span class="sxs-lookup"><span data-stu-id="7cc77-145">Click Header to go to scoring of the bid.</span></span>
2. <span data-ttu-id="7cc77-146">في حقل النقاط، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="7cc77-146">In the Score field, enter a number.</span></span>
3. <span data-ttu-id="7cc77-147">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="7cc77-147">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="7cc77-148">في حقل النقاط، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="7cc77-148">In the Score field, enter a number.</span></span>

## <a name="compare-the-replies"></a><span data-ttu-id="7cc77-149">مقارنة الردود</span><span class="sxs-lookup"><span data-stu-id="7cc77-149">Compare the replies</span></span>
1. <span data-ttu-id="7cc77-150">في جزء "الإجراءات"، انقر فوق "عام".</span><span class="sxs-lookup"><span data-stu-id="7cc77-150">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="7cc77-151">انقر فوق مقارنة الردود.</span><span class="sxs-lookup"><span data-stu-id="7cc77-151">Click Compare replies.</span></span>
3. <span data-ttu-id="7cc77-152">في حقل الرتبة، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="7cc77-152">In the Rank field, enter a number.</span></span>
    * <span data-ttu-id="7cc77-153">تعرض هذه الصفحة المزايدات بالعنوان والبنود والنتيجة الإجمالية على مستوى العنوان.</span><span class="sxs-lookup"><span data-stu-id="7cc77-153">This page shows the bids with the header and lines, and the total score on the header level.</span></span> <span data-ttu-id="7cc77-154">يمكنك مقارنة البنود بفرز في الشبكة حيث تكون البنود القابلة للمقارنة جنبًا إلى جنب.</span><span class="sxs-lookup"><span data-stu-id="7cc77-154">You can compare the lines by sorting in the grid so that comparable lines are next to each other.</span></span> <span data-ttu-id="7cc77-155">كما تتضمن المعلومات:   الكمية: الكمية التي حدد المورّد سعرها.</span><span class="sxs-lookup"><span data-stu-id="7cc77-155">The information also includes:   Quantity: The quantity quoted by the vendor.</span></span> <span data-ttu-id="7cc77-156">وهذه الكمية قد لا تساوي الكمية الموجودة في RFQ.</span><span class="sxs-lookup"><span data-stu-id="7cc77-156">This might not equal the quantity specified in the RFQ.</span></span>   <span data-ttu-id="7cc77-157">المبلغ الصافي: السعر الذي حدده المورد، بعد طرح أي خصومات، على الأصناف الموجودة في البند.</span><span class="sxs-lookup"><span data-stu-id="7cc77-157">Net amount: The price quoted by a vendor, after subtracting any discounts, for the items on the line.</span></span>   <span data-ttu-id="7cc77-158">الانحراف: عدد الأيام التي تخلف عنها تاريخ التسليم الموجودة برأس العطاء أو بند الرد مقارنة بتاريخ التسليم المطلوب في رأس RFQ أو بند RFQ.</span><span class="sxs-lookup"><span data-stu-id="7cc77-158">Deviation: The number of days that the delivery date in the bid header or line deviates from the requested delivery date in the RFQ header or RFQ line.</span></span>   <span data-ttu-id="7cc77-159">يمكنك إدخال ترتيب لكل عرض.</span><span class="sxs-lookup"><span data-stu-id="7cc77-159">You can enter a rank for each bid.</span></span>  
4. <span data-ttu-id="7cc77-160">حدد سطر العنوان للعطاء الآخر المراد ترتيبه.</span><span class="sxs-lookup"><span data-stu-id="7cc77-160">Select the header line for the other bid that you want to rank.</span></span>
5. <span data-ttu-id="7cc77-161">في حقل الرتبة، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="7cc77-161">In the Rank field, enter a number.</span></span>
6. <span data-ttu-id="7cc77-162">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="7cc77-162">Click Save.</span></span>

## <a name="reject-a-bid"></a><span data-ttu-id="7cc77-163">رفض عطاء</span><span class="sxs-lookup"><span data-stu-id="7cc77-163">Reject a bid</span></span>
1. <span data-ttu-id="7cc77-164">حدد سطر العنوان للعطاء المراد رفضه.</span><span class="sxs-lookup"><span data-stu-id="7cc77-164">Select the header line for the bid that you want to reject.</span></span>
    * <span data-ttu-id="7cc77-165">يمكنك فقط قبول أو رفض أو إرجاع العطاء أو البنود في عطاء واحد في كل مرة.</span><span class="sxs-lookup"><span data-stu-id="7cc77-165">You can only accept, reject, or return one bid or lines within one bid at a time.</span></span>  
2. <span data-ttu-id="7cc77-166">حدد خانة الاختيار "وضع علامة".</span><span class="sxs-lookup"><span data-stu-id="7cc77-166">Select the Mark check box.</span></span>
    * <span data-ttu-id="7cc77-167">إذا حددت خانة الاختيار "وضع علامة" على رأس العطاء، فسيتم تمييز كافة البنود أيضًا.</span><span class="sxs-lookup"><span data-stu-id="7cc77-167">If you select the Mark check box on the Header of the bid then all the lines will be marked as well.</span></span> <span data-ttu-id="7cc77-168">كما يمكنك اختيار وضع علامة على مجموعة فرعية من البنود لرفضها أو قبولها.</span><span class="sxs-lookup"><span data-stu-id="7cc77-168">You could also choose to mark a subset of the lines within the bid to reject or accept those.</span></span> <span data-ttu-id="7cc77-169">من الممكن قبول عطاء مورد واحد لبعض بنود RFQ، ثم منح بنود RFQ الأخرى إلى مورد مختلف، ومع ذلك فإنك تحتاج إلى القيام بهذا في خطوتين، عطاء واحد في كل مرة.</span><span class="sxs-lookup"><span data-stu-id="7cc77-169">It’s possible to accept one vendor’s bid for some lines of an RFQ, and then award other RFQ lines to a different vendor, however you need to do this in 2 steps, one bid at a time.</span></span> <span data-ttu-id="7cc77-170">في حالة وجود بنود بديلة، يمكنك فقط قبول بند العطاء الأصلي أو البديل الخاص به لكن ليس كلاهما.</span><span class="sxs-lookup"><span data-stu-id="7cc77-170">If alternate lines are present, you can only accept either the original bid line or its alternate, but not both.</span></span>  
3. <span data-ttu-id="7cc77-171">انقر فوق رفض.</span><span class="sxs-lookup"><span data-stu-id="7cc77-171">Click Reject.</span></span>
4. <span data-ttu-id="7cc77-172">انقر فوق "المعلمات" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="7cc77-172">Click Parameters to open the drop dialog.</span></span>
5. <span data-ttu-id="7cc77-173">في حقل "‏‫رفض السبب"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="7cc77-173">In the Reason reject field, enter or select a value.</span></span>
    * <span data-ttu-id="7cc77-174">سيتم تخزين سبب الرفض على الرد.</span><span class="sxs-lookup"><span data-stu-id="7cc77-174">The reason for rejection will be stored on the reply.</span></span>  
6. <span data-ttu-id="7cc77-175">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="7cc77-175">Click OK.</span></span>
7. <span data-ttu-id="7cc77-176">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="7cc77-176">Click OK.</span></span>
8. <span data-ttu-id="7cc77-177">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7cc77-177">Close the page.</span></span>
9. <span data-ttu-id="7cc77-178">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7cc77-178">Close the page.</span></span>
10. <span data-ttu-id="7cc77-179">قم بتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7cc77-179">Refresh the page.</span></span>

## <a name="accept-a-bid"></a><span data-ttu-id="7cc77-180">قبول عطاء</span><span class="sxs-lookup"><span data-stu-id="7cc77-180">Accept a bid</span></span>
1. <span data-ttu-id="7cc77-181">حدد العرض الذي تريد قبوله، ثم انقر فوق الارتباط في حقل طلب عرض الأسعار.</span><span class="sxs-lookup"><span data-stu-id="7cc77-181">Select the bid that you want to accept and then click the link in the Request for quotation field.</span></span>
2. <span data-ttu-id="7cc77-182">في جزء الإجراءات، انقر فوق رد.</span><span class="sxs-lookup"><span data-stu-id="7cc77-182">On the Action Pane, click Reply.</span></span>
3. <span data-ttu-id="7cc77-183">انقر فوق "قبول".</span><span class="sxs-lookup"><span data-stu-id="7cc77-183">Click Accept.</span></span>
    * <span data-ttu-id="7cc77-184">إذا كنت قد وضعت علامة على بنود معينة وليس غيرها فسيتضمن إجراء القبول البنود المحددة فقط.</span><span class="sxs-lookup"><span data-stu-id="7cc77-184">If you have marked specific lines and not others then the accept action will only include the marked lines.</span></span> <span data-ttu-id="7cc77-185">إذا كنت تريد قبول كافة البنود الموجودة في العطاء، فلا يجب عليك وضع علامة على البنود.</span><span class="sxs-lookup"><span data-stu-id="7cc77-185">If you want to accept all lines on the bid then you do not have to mark the lines.</span></span>  
4. <span data-ttu-id="7cc77-186">انقر فوق "المعلمات" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="7cc77-186">Click Parameters to open the drop dialog.</span></span>
    * <span data-ttu-id="7cc77-187">هذا يسمح لك بتسجيل سبب لقبول العطاء.</span><span class="sxs-lookup"><span data-stu-id="7cc77-187">This allows you to record a reason for accepting the bid.</span></span> <span data-ttu-id="7cc77-188">سيتم تخزين السبب على العطاء.</span><span class="sxs-lookup"><span data-stu-id="7cc77-188">The reason will be stored on the bid.</span></span>  
5. <span data-ttu-id="7cc77-189">في حقل "‏‫قبول السبب"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="7cc77-189">In the Reason accept field, enter or select a value.</span></span>
6. <span data-ttu-id="7cc77-190">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="7cc77-190">Click OK.</span></span>
7. <span data-ttu-id="7cc77-191">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="7cc77-191">Click OK.</span></span>
    * <span data-ttu-id="7cc77-192">عند النقر فوق "موافق"، يقوم هذا بإنشاء أمر شراء استنادًا إلى البنود التي سيتم تضمينها في قبول RFQ.</span><span class="sxs-lookup"><span data-stu-id="7cc77-192">When you click OK this generates a purchase order based on the lines that are included in the RFQ acceptance.</span></span> <span data-ttu-id="7cc77-193">إذا كان هناك عطاءات أخرى لم تتم معالجتها (قبول أو رفض أو إرجاع) ثم سيطالبك النظام برفض العطاءات الباقية.</span><span class="sxs-lookup"><span data-stu-id="7cc77-193">If there are other bids that have not been processed (accepted, rejected, or returned) then the system will prompt you to reject the remaining bids.</span></span>  

## <a name="view-the-purchase-order-thats-been-generated"></a><span data-ttu-id="7cc77-194">اعرض أمر الشراء الذي تم تكوينه.</span><span class="sxs-lookup"><span data-stu-id="7cc77-194">View the purchase order that's been generated</span></span>
1. <span data-ttu-id="7cc77-195">في جزء "الإجراءات"، انقر فوق "عام".</span><span class="sxs-lookup"><span data-stu-id="7cc77-195">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="7cc77-196">انقر فوق "أمر الشراء".</span><span class="sxs-lookup"><span data-stu-id="7cc77-196">Click Purchase order.</span></span>
    * <span data-ttu-id="7cc77-197">هنا يمكنك رؤية أمر الشراء الذي تم إنشاؤه عندما قمت بقبول العطاء.</span><span class="sxs-lookup"><span data-stu-id="7cc77-197">Here you can see the purchase order that was generated when you accepted the bid.</span></span>  
3. <span data-ttu-id="7cc77-198">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7cc77-198">Close the page.</span></span>
4. <span data-ttu-id="7cc77-199">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7cc77-199">Close the page.</span></span>
5. <span data-ttu-id="7cc77-200">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7cc77-200">Close the page.</span></span>
6. <span data-ttu-id="7cc77-201">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7cc77-201">Close the page.</span></span>

