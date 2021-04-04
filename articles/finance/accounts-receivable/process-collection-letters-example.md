---
title: مثال معالجة خطابات التحصيل
description: يتناول هذا الموضوع مثالًا يوضح عملية إنشاء خطابات التحصيل وطباعتها وترحيلها.
author: JodiChristiansen
manager: AnnBe
ms.date: 02/03/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: df4252513f9e3a02632561b4e465c98edc888ea7
ms.sourcegitcommit: 4ecc1bf82fbb04882d7ef5e1994ef3c07ef953dc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/08/2021
ms.locfileid: "5558301"
---
# <a name="process-collection-letters-example"></a><span data-ttu-id="26da1-103">مثال معالجة خطابات التحصيل</span><span class="sxs-lookup"><span data-stu-id="26da1-103">Process collection letters example</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="26da1-104">يتناول هذا الموضوع مثالًا يوضح عملية إنشاء خطابات التحصيل وطباعتها وترحيلها.</span><span class="sxs-lookup"><span data-stu-id="26da1-104">This topic goes through an example that shows the process of creating, printing, and posting collection letters.</span></span> <span data-ttu-id="26da1-105">يستند المثال على خيار **تجاهل المدفوعات والإشعارات الدائنة عند حساب كود خطاب التحصيل** في الائتمان والتحصيلات.</span><span class="sxs-lookup"><span data-stu-id="26da1-105">The example is based on the **Ignore payments and credit memos when calculating collection letter code** option in Credit and collections.</span></span> <span data-ttu-id="26da1-106">فهو يستخدم البيانات الموجودة في الشركة التجريبية USMF وعميل جديد، US-045.</span><span class="sxs-lookup"><span data-stu-id="26da1-106">It uses data in the USMF demo company and a new customer, US-045.</span></span>

<span data-ttu-id="26da1-107">للبدء، انتقل إلى **الحسابات المدينة \> العملاء \> كافة العملاء**، وحدد **جديد**، ثم أدخل المعلومات المطلوبة لإنشاء العميل US-045.</span><span class="sxs-lookup"><span data-stu-id="26da1-107">To begin, go to **Accounts receivable \> Customers \> All customers**, select **New**, and then enter the required information to create customer US-045.</span></span>

<span data-ttu-id="26da1-108">عند الانتهاء، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="26da1-108">When you've finished, follow these steps.</span></span>

1. <span data-ttu-id="26da1-109">انتقال إلى **الائتمان والتحصيلات \> خطاب التحصيل \> إعداد تسلسل خطاب التحصيل**، وقم بإعداد تسلسل خطاب التحصيل كما هو موضح في الجدول التالي الذي تم تعيينه لملف تعريف ترحيل العميل.</span><span class="sxs-lookup"><span data-stu-id="26da1-109">Go to **Credit and collections \> Collection letter \> Setup collection letter sequence**, and set up the collection letter sequence as shown in the following table that is assigned to the customer posting profile.</span></span>

|     <span data-ttu-id="26da1-110">كود خطاب التحصيل</span><span class="sxs-lookup"><span data-stu-id="26da1-110">Collection   letter code</span></span>      |     <span data-ttu-id="26da1-111">الوصف</span><span class="sxs-lookup"><span data-stu-id="26da1-111">Description</span></span>                           |     <span data-ttu-id="26da1-112">عملة</span><span class="sxs-lookup"><span data-stu-id="26da1-112">Currency</span></span>      |     <span data-ttu-id="26da1-113">الحساب الرئيسي</span><span class="sxs-lookup"><span data-stu-id="26da1-113">Main   account</span></span>        |     <span data-ttu-id="26da1-114">الرسوم بالعملة</span><span class="sxs-lookup"><span data-stu-id="26da1-114">Fee   in currency</span></span>     |     <span data-ttu-id="26da1-115">الحد الأدنى من</span><span class="sxs-lookup"><span data-stu-id="26da1-115">Minimum   over</span></span>        |     <span data-ttu-id="26da1-116">الأيام الممتلئة</span><span class="sxs-lookup"><span data-stu-id="26da1-116">Days   Block</span></span>      |
|---------------------------------  |---------------------------------------    |-----------------  |-----------------------    |-------------------------- |-----------------------    |---------------------  |
|     <span data-ttu-id="26da1-117">خطاب التحصيل 1</span><span class="sxs-lookup"><span data-stu-id="26da1-117">Collection   letter 1</span></span>         |     <span data-ttu-id="26da1-118">الإخطار الثاني بالرسوم</span><span class="sxs-lookup"><span data-stu-id="26da1-118">Second   notification with fee</span></span>        |     <span data-ttu-id="26da1-119">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="26da1-119">USD</span></span>           |                           |     <span data-ttu-id="26da1-120">0.00</span><span class="sxs-lookup"><span data-stu-id="26da1-120">0.00</span></span>                  |     <span data-ttu-id="26da1-121">0.00</span><span class="sxs-lookup"><span data-stu-id="26da1-121">0.00</span></span>                  |     <span data-ttu-id="26da1-122">2</span><span class="sxs-lookup"><span data-stu-id="26da1-122">2</span></span>                 |
|     <span data-ttu-id="26da1-123">خطاب التحصيل 2</span><span class="sxs-lookup"><span data-stu-id="26da1-123">Collection   letter 2</span></span>         |     <span data-ttu-id="26da1-124">الإخطار الثاني بالرسوم</span><span class="sxs-lookup"><span data-stu-id="26da1-124">Second   notification with fee</span></span>        |     <span data-ttu-id="26da1-125">USC</span><span class="sxs-lookup"><span data-stu-id="26da1-125">USC</span></span>           |     <span data-ttu-id="26da1-126">403150</span><span class="sxs-lookup"><span data-stu-id="26da1-126">403150</span></span>                |     <span data-ttu-id="26da1-127">20.00</span><span class="sxs-lookup"><span data-stu-id="26da1-127">20.00</span></span>                 |     <span data-ttu-id="26da1-128">10.00</span><span class="sxs-lookup"><span data-stu-id="26da1-128">10.00</span></span>                 |     <span data-ttu-id="26da1-129">3</span><span class="sxs-lookup"><span data-stu-id="26da1-129">3</span></span>                 |
|     <span data-ttu-id="26da1-130">التحصيل</span><span class="sxs-lookup"><span data-stu-id="26da1-130">Collection</span></span>                    |     <span data-ttu-id="26da1-131">الإخطار النهائي بالرسوم</span><span class="sxs-lookup"><span data-stu-id="26da1-131">Final   notification with fee</span></span>         |     <span data-ttu-id="26da1-132">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="26da1-132">USD</span></span>           |     <span data-ttu-id="26da1-133">403150</span><span class="sxs-lookup"><span data-stu-id="26da1-133">403150</span></span>                |     <span data-ttu-id="26da1-134">50.00</span><span class="sxs-lookup"><span data-stu-id="26da1-134">50.00</span></span>                 |     <span data-ttu-id="26da1-135">100.00</span><span class="sxs-lookup"><span data-stu-id="26da1-135">100.00</span></span>                |     <span data-ttu-id="26da1-136">15</span><span class="sxs-lookup"><span data-stu-id="26da1-136">15</span></span>                |

<span data-ttu-id="26da1-137">يبين الرسم التوضيحي التالي المعلومات الموجودة في الجدول كما تظهر في صفحة **خطابات التحصيل**.</span><span class="sxs-lookup"><span data-stu-id="26da1-137">The following illustration shows the information that's in the table as it would appear on the **Collection letters** page.</span></span> 

<span data-ttu-id="26da1-138">[![إعداد تسلسل خطاب تحصيل](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)</span><span class="sxs-lookup"><span data-stu-id="26da1-138">[![Setting up a collection letter sequence](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)</span></span>

 <span data-ttu-id="26da1-139">يجب أن تقوم الآن بتعيين المعلمتين المطلوبتين لهذا المثال.</span><span class="sxs-lookup"><span data-stu-id="26da1-139">You must now set the two parameters that are required for this example.</span></span>

2. <span data-ttu-id="26da1-140">انتقل إلى **الائتمان والتحصيلات \> الإعداد \> معلمات الحسابات المدينة**، واتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="26da1-140">Go to **Credit and collections \> Setup \> Accounts receivable parameters**, and follow these steps:</span></span>

    1. <span data-ttu-id="26da1-141">في علامة تبويب **التحصيلات**، قم بتعيين خيار **تجاهل المدفوعات والإشعارات الدائنة عند حساب كود خطاب التحصيل** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="26da1-141">On the **Collections** tab, set the **Ignore payments and credit memos when calculating collection letter code** option to **Yes**.</span></span>
    2. <span data-ttu-id="26da1-142">تأكد من تعيين حقل **إنشاء خطاب تحصيل لكل** على **العميل**.</span><span class="sxs-lookup"><span data-stu-id="26da1-142">Make sure that the **Create collection letter per** field is set to **Customer**.</span></span>

    <span data-ttu-id="26da1-143">[![إعداد معلمات الحسابات المدينة لتحصيلات الائتمان](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)</span><span class="sxs-lookup"><span data-stu-id="26da1-143">[![Setting Accounts receivable parameters for Credit collections](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)</span></span>

3. <span data-ttu-id="26da1-144">انتقل إلى **الحسابات المدينة \> فواتير \> كافة فواتير النص الحر**، وحدد **جديد**، ثم اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="26da1-144">Go to **Accounts receivable \> Invoices \> All free text invoices**, select **New**, and then follow these steps:</span></span>

    1. <span data-ttu-id="26da1-145">في حقل **حساب العميل** حدد **US-045**.</span><span class="sxs-lookup"><span data-stu-id="26da1-145">In the **Customer account** field select **US-045**.</span></span>
    2. <span data-ttu-id="26da1-146">في حقل **تاريخ الفاتورة**، أدخل **1/15/2021**.</span><span class="sxs-lookup"><span data-stu-id="26da1-146">In the **Invoice date** field, enter **1/15/2021**.</span></span>
    3. <span data-ttu-id="26da1-147">في حقل **‏التاريخ الاستحقاق**، أدخل **1/16/2021**.</span><span class="sxs-lookup"><span data-stu-id="26da1-147">In the **Due date** field, enter **1/16/2021**.</span></span>
    4. <span data-ttu-id="26da1-148">في علامة التبويب السريعة **بنود الفاتورة**، في حقل **الحساب الرئيسي**، أدخل **401100**.</span><span class="sxs-lookup"><span data-stu-id="26da1-148">On the **Invoice lines** FastTab, in the **Main account** field, enter **401100**.</span></span>
    5. <span data-ttu-id="26da1-149">في الحقل **سعر الوحدة**، أدخل **500.00**.</span><span class="sxs-lookup"><span data-stu-id="26da1-149">In the **Unit price** field, enter **500.00**.</span></span>
    6. <span data-ttu-id="26da1-150">حدد **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="26da1-150">Select **Post**.</span></span>

    <span data-ttu-id="26da1-151">ينبعي الآن إدخال إشعارين دائنين للعميل.</span><span class="sxs-lookup"><span data-stu-id="26da1-151">You must now enter two credit notes for the customer.</span></span>

4. <span data-ttu-id="26da1-152">حدد **جديد**، ثم اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="26da1-152">Select **New**, and then follow these steps:</span></span>

    1. <span data-ttu-id="26da1-153">في حقل **حساب العميل**، حدد **US-045**.</span><span class="sxs-lookup"><span data-stu-id="26da1-153">In the **Customer account** field, select **US-045**.</span></span>
    2. <span data-ttu-id="26da1-154">في حقل **تاريخ الفاتورة**، أدخل **1/15/2021**.</span><span class="sxs-lookup"><span data-stu-id="26da1-154">In the **Invoice date** field, enter **1/15/2021**.</span></span>
    3. <span data-ttu-id="26da1-155">في حقل **‏التاريخ الاستحقاق**، أدخل **1/16/2021**.</span><span class="sxs-lookup"><span data-stu-id="26da1-155">In the **Due date** field, enter **1/16/2021**.</span></span>
    4. <span data-ttu-id="26da1-156">في علامة التبويب السريعة **بنود الفاتورة**، في حقل **الحساب الرئيسي**، أدخل **401100**.</span><span class="sxs-lookup"><span data-stu-id="26da1-156">On the **Invoice lines** FastTab, in the **Main account** field, enter **401100**.</span></span>
    5. <span data-ttu-id="26da1-157">في حقل **سعر الوحدة**، أدخل **100.00**.</span><span class="sxs-lookup"><span data-stu-id="26da1-157">In the **Unit price** field, enter **-100.00**.</span></span>
    6. <span data-ttu-id="26da1-158">حدد **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="26da1-158">Select **Post**.</span></span>

5. <span data-ttu-id="26da1-159">كرر الخطوة 4، ولكن أدخل **-200.00** في حقل **سعر الوحدة**.</span><span class="sxs-lookup"><span data-stu-id="26da1-159">Repeat step 4, but enter **-200.00** in the **Unit price** field.</span></span>
6. <span data-ttu-id="26da1-160">انتقل إلى **الحسابات المدينة \> العملاء \> كافة العملاء**، وحدد العميل **US-045**.</span><span class="sxs-lookup"><span data-stu-id="26da1-160">Go to **Accounts receivable \> Customers \> All customers**, and select customer **US-045**.</span></span> <span data-ttu-id="26da1-161">ثم في جزء الإجراء، حدد **الحركات \> الحركات** لمراجعة حركات العميل التي قمت بترحيلها في وقت سابق.</span><span class="sxs-lookup"><span data-stu-id="26da1-161">Then, on the Action Pane, select **Transactions \> Transactions** to review the customer transactions that you posted earlier.</span></span>

    <span data-ttu-id="26da1-162">[![مراجعة حركات العميل المرحلة](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)</span><span class="sxs-lookup"><span data-stu-id="26da1-162">[![Reviewing the posted customer transactions](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)</span></span>

    <span data-ttu-id="26da1-163">يجب عليك الآن إنشاء خطابات تحصيل للعميل US-045.</span><span class="sxs-lookup"><span data-stu-id="26da1-163">You must now create collection letters for customer US-045.</span></span>

7. <span data-ttu-id="26da1-164">انتقل إلى **الائتمان والتحصيلات \> خطاب التحصيل \> إنشاء خطابات تحصيل**، واتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="26da1-164">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="26da1-165">قم بتعيين خيارات **الفاتورة** و **الإشعار الائتماني** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="26da1-165">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="26da1-166">بشكل افتراضي، يجب تعيين حقل **خطاب التحصيل** إلى **التحصيل لكل عميل**.</span><span class="sxs-lookup"><span data-stu-id="26da1-166">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="26da1-167">في حقل **تاريخ خطاب التحصيل**، أدخل **1/19/2021**.</span><span class="sxs-lookup"><span data-stu-id="26da1-167">In the **Collection letter date** field, enter **1/19/2021**.</span></span>
    3. <span data-ttu-id="26da1-168">في علامة التبويب السريعة **السجلات المراد تضمينها**، حدد **عامل التصفية**، ثم في حقل **حساب العميل**، أضف العميل **US-045**.</span><span class="sxs-lookup"><span data-stu-id="26da1-168">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="26da1-169">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="26da1-169">Select **OK**.</span></span>
    5. <span data-ttu-id="26da1-170">حدد **موافق** لإنشاء خطابات التحصيل.</span><span class="sxs-lookup"><span data-stu-id="26da1-170">Select **OK** to create collection letters.</span></span>

8. <span data-ttu-id="26da1-171">انتقل إلى **الائتمان والتحصيلات \> خطاب التحصيل \> مراجعة ومعالجة خطابات تحصيل**، واتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="26da1-171">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="26da1-172">لاحظ أن كود خطاب التحصيل في كل من الرأس وبنود الحركة هو **خطاب التحصيل 1** ، لان خطاب التحصيل هذا هو أول خطاب تحصيل في التسلسل.</span><span class="sxs-lookup"><span data-stu-id="26da1-172">Notice that the collection letter code on both the header and the transaction lines is **Collection letter 1**, because this collection letter is the first collection letter in the sequence.</span></span> <span data-ttu-id="26da1-173">(لعرض بنود الحركة، قد تحتاج إلى تحديد علامة التبويب السريعة **الحركات**)</span><span class="sxs-lookup"><span data-stu-id="26da1-173">(To view the transaction lines, you might have to select the **Transactions** FastTab.)</span></span>

   <span data-ttu-id="26da1-174">[![تحقق من أن نفس كود خطاب التحصيل يظهر في الرأس والبنود](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)</span><span class="sxs-lookup"><span data-stu-id="26da1-174">[![Verifying that the same collection letter code appears on the header and the lines](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)</span></span>

    2. <span data-ttu-id="26da1-175">في جزء الإجراءات، حدد **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="26da1-175">On the Action Pane, select **Post**.</span></span>
    3. <span data-ttu-id="26da1-176">في حقل **تاريخ الترحيل**، أدخل **1/19/2021**.</span><span class="sxs-lookup"><span data-stu-id="26da1-176">In the **Posting date** field, enter **1/19/2021**.</span></span>

    <span data-ttu-id="26da1-177">يجب عليك الآن إنشاء خطابات تحصيل مرة أخرى للعميل US-045.</span><span class="sxs-lookup"><span data-stu-id="26da1-177">You must now create collection letters again for customer US-045.</span></span>

9. <span data-ttu-id="26da1-178">انتقل إلى **الائتمان والتحصيلات \> خطاب التحصيل \> إنشاء خطابات تحصيل**، واتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="26da1-178">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="26da1-179">قم بتعيين خيارات **الفاتورة** و **الإشعار الائتماني** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="26da1-179">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="26da1-180">بشكل افتراضي، يجب تعيين حقل **خطاب التحصيل** إلى **التحصيل لكل عميل**.</span><span class="sxs-lookup"><span data-stu-id="26da1-180">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="26da1-181">في حقل **تاريخ خطاب التحصيل**، أدخل **1/23/2021**.</span><span class="sxs-lookup"><span data-stu-id="26da1-181">In the **Collection letter date** field, enter **1/23/2021**.</span></span>
    3. <span data-ttu-id="26da1-182">في علامة التبويب السريعة **السجلات المراد تضمينها**، حدد **عامل التصفية**، ثم في حقل **حساب العميل**، أضف العميل **US-045**.</span><span class="sxs-lookup"><span data-stu-id="26da1-182">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="26da1-183">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="26da1-183">Select **OK**.</span></span>
    5. <span data-ttu-id="26da1-184">حدد **موافق** لإنشاء خطابات التحصيل.</span><span class="sxs-lookup"><span data-stu-id="26da1-184">Select **OK** to create collection letters.</span></span>

10. <span data-ttu-id="26da1-185">انتقل إلى **الائتمان والتحصيلات \> خطاب التحصيل \> مراجعة ومعالجة خطابات تحصيل**، واتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="26da1-185">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="26da1-186">لاحظ أن كود خطاب التحصيل في الرأس هو **خطاب التحصيل 1**.</span><span class="sxs-lookup"><span data-stu-id="26da1-186">Notice that the collection letter code on the header is **Collection letter 1**.</span></span> <span data-ttu-id="26da1-187">ومع ذلك، فان الكود الموجود في بنود الحركة هو **خطاب التحصيل 2**.</span><span class="sxs-lookup"><span data-stu-id="26da1-187">However, the code on the transaction lines is **Collection letter 2**.</span></span>

   <span data-ttu-id="26da1-188">[![تحقق من ظهور أكواد خطاب التحصيل مختلفة في الرأس والبنود](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)</span><span class="sxs-lookup"><span data-stu-id="26da1-188">[![Verifies that different collection letter codes appear on the header and the lines](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)</span></span>

  <span data-ttu-id="26da1-189">تختلف الأكواد لأن خيار **تجاهل المدفوعات والإشعارات الدائنة عند حساب كود خطاب التحصيل** تم تعيينه إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="26da1-189">The codes differ because the **Ignore payments and credit memos when calculating collection letter code** option is to **Yes**.</span></span>

  2. <span data-ttu-id="26da1-190">لا تقم بترحيل خطاب التحصيل هذا.</span><span class="sxs-lookup"><span data-stu-id="26da1-190">Don't post this collection letter.</span></span>

11. <span data-ttu-id="26da1-191">انتقل إلى **الائتمان والتحصيلات \> الإعداد \> معلمات الحسابات الدائنة**، ثم في علامة تبويب **التحصيلات**، قم بتعيين خيار **تجاهل المدفوعات والإشعارات الدائنة عند حساب كود خطاب التحصيل** إلى **لا**.</span><span class="sxs-lookup"><span data-stu-id="26da1-191">Go to **Credit and collections \> Setup \> Accounts receivable parameters**, and then, on the **Collections** tab, set the **Ignore payments and credit memos when calculating collection letter code** option to **No**.</span></span>

    <span data-ttu-id="26da1-192">[![إعداد خيار تجاهل المدفوعات والإشعارات الدائنة عند حساب كود خطاب التحصيل إلى لا](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)</span><span class="sxs-lookup"><span data-stu-id="26da1-192">[![Setting the Ignore payments and credit memos when calculating collection letter code option to No](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)</span></span>

    <span data-ttu-id="26da1-193">يجب عليك الآن إنشاء خطابات تحصيل مرة أخرى للعميل US-045.</span><span class="sxs-lookup"><span data-stu-id="26da1-193">You must now create collection letters again for customer US-045.</span></span>

12. <span data-ttu-id="26da1-194">انتقل إلى **الائتمان والتحصيلات \> خطاب التحصيل \> إنشاء خطابات تحصيل**، واتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="26da1-194">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="26da1-195">قم بتعيين خيارات **الفاتورة** و **الإشعار الائتماني** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="26da1-195">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="26da1-196">بشكل افتراضي، يجب تعيين حقل **خطاب التحصيل** إلى **التحصيل لكل عميل**.</span><span class="sxs-lookup"><span data-stu-id="26da1-196">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="26da1-197">في حقل **تاريخ خطاب التحصيل**، أدخل **1/23/2021**.</span><span class="sxs-lookup"><span data-stu-id="26da1-197">In the **Collection letter date** field, enter **1/23/2021**.</span></span>
    3. <span data-ttu-id="26da1-198">في علامة التبويب السريعة **السجلات المراد تضمينها**، حدد **عامل التصفية**، ثم في حقل **حساب العميل**، أضف العميل **US-045**.</span><span class="sxs-lookup"><span data-stu-id="26da1-198">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="26da1-199">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="26da1-199">Select **OK**.</span></span>
    5. <span data-ttu-id="26da1-200">حدد **موافق** لإنشاء خطابات التحصيل.</span><span class="sxs-lookup"><span data-stu-id="26da1-200">Select **OK** to create collection letters.</span></span>

13. <span data-ttu-id="26da1-201">انتقل إلى **الائتمان والتحصيلات \> خطاب التحصيل \> مراجعة ومعالجة خطابات التحصيل**، ولاحظ أن كود خطاب التحصيل في كل من الرأس وبنود الحركة **خطاب التحصيل 2**.</span><span class="sxs-lookup"><span data-stu-id="26da1-201">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and notice that the collection letter code on both the header and the transaction lines is **Collection letter 2**.</span></span>

    <span data-ttu-id="26da1-202">[![ظهور نفس كود خطاب التحصيل مرة أخرى في الرأس والبنود](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)</span><span class="sxs-lookup"><span data-stu-id="26da1-202">[![Showing again that the same collection letter code appears on the header and the lines](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)</span></span>

    <span data-ttu-id="26da1-203">يظهر نفس الكود في كل المكانين لأن خيار **تجاهل المدفوعات والإشعارات الدائنة عند حساب كود خطاب التحصيل** تم تعيينه الآن إلى **لا**.</span><span class="sxs-lookup"><span data-stu-id="26da1-203">The same code appears in both places because the **Ignore payments and credit memos when calculating collection letter code** option is now set to **No**.</span></span>
