---
title: مثال معالجة خطابات التحصيل
description: يتناول هذا الموضوع مثالًا يوضح عملية إنشاء خطابات التحصيل وطباعتها وترحيلها.
author: JodiChristiansen
ms.date: 02/03/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: fb2651644efd2cadfccb91e48c34dfddc8383e1f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021406"
---
# <a name="process-collection-letters-example"></a><span data-ttu-id="fafb2-103">مثال معالجة خطابات التحصيل</span><span class="sxs-lookup"><span data-stu-id="fafb2-103">Process collection letters example</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fafb2-104">يتناول هذا الموضوع مثالًا يوضح عملية إنشاء خطابات التحصيل وطباعتها وترحيلها.</span><span class="sxs-lookup"><span data-stu-id="fafb2-104">This topic goes through an example that shows the process of creating, printing, and posting collection letters.</span></span> <span data-ttu-id="fafb2-105">يستند المثال على خيار **تجاهل المدفوعات والإشعارات الدائنة عند حساب كود خطاب التحصيل** في الائتمان والتحصيلات.</span><span class="sxs-lookup"><span data-stu-id="fafb2-105">The example is based on the **Ignore payments and credit memos when calculating collection letter code** option in Credit and collections.</span></span> <span data-ttu-id="fafb2-106">فهو يستخدم البيانات الموجودة في الشركة التجريبية USMF وعميل جديد، US-045.</span><span class="sxs-lookup"><span data-stu-id="fafb2-106">It uses data in the USMF demo company and a new customer, US-045.</span></span>

<span data-ttu-id="fafb2-107">للبدء، انتقل إلى **الحسابات المدينة \> العملاء \> كافة العملاء**، وحدد **جديد**، ثم أدخل المعلومات المطلوبة لإنشاء العميل US-045.</span><span class="sxs-lookup"><span data-stu-id="fafb2-107">To begin, go to **Accounts receivable \> Customers \> All customers**, select **New**, and then enter the required information to create customer US-045.</span></span>

<span data-ttu-id="fafb2-108">عند الانتهاء، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="fafb2-108">When you've finished, follow these steps.</span></span>

1. <span data-ttu-id="fafb2-109">انتقال إلى **الائتمان والتحصيلات \> خطاب التحصيل \> إعداد تسلسل خطاب التحصيل**، وقم بإعداد تسلسل خطاب التحصيل كما هو موضح في الجدول التالي الذي تم تعيينه لملف تعريف ترحيل العميل.</span><span class="sxs-lookup"><span data-stu-id="fafb2-109">Go to **Credit and collections \> Collection letter \> Setup collection letter sequence**, and set up the collection letter sequence as shown in the following table that is assigned to the customer posting profile.</span></span>

|     <span data-ttu-id="fafb2-110">كود خطاب التحصيل</span><span class="sxs-lookup"><span data-stu-id="fafb2-110">Collection   letter code</span></span>      |     <span data-ttu-id="fafb2-111">الوصف</span><span class="sxs-lookup"><span data-stu-id="fafb2-111">Description</span></span>                           |     <span data-ttu-id="fafb2-112">عملة</span><span class="sxs-lookup"><span data-stu-id="fafb2-112">Currency</span></span>      |     <span data-ttu-id="fafb2-113">الحساب الرئيسي</span><span class="sxs-lookup"><span data-stu-id="fafb2-113">Main   account</span></span>        |     <span data-ttu-id="fafb2-114">الرسوم بالعملة</span><span class="sxs-lookup"><span data-stu-id="fafb2-114">Fee   in currency</span></span>     |     <span data-ttu-id="fafb2-115">الحد الأدنى من</span><span class="sxs-lookup"><span data-stu-id="fafb2-115">Minimum   over</span></span>        |     <span data-ttu-id="fafb2-116">الأيام الممتلئة</span><span class="sxs-lookup"><span data-stu-id="fafb2-116">Days   Block</span></span>      |
|---------------------------------  |---------------------------------------    |-----------------  |-----------------------    |-------------------------- |-----------------------    |---------------------  |
|     <span data-ttu-id="fafb2-117">خطاب التحصيل 1</span><span class="sxs-lookup"><span data-stu-id="fafb2-117">Collection   letter 1</span></span>         |     <span data-ttu-id="fafb2-118">الإخطار الثاني بالرسوم</span><span class="sxs-lookup"><span data-stu-id="fafb2-118">Second   notification with fee</span></span>        |     <span data-ttu-id="fafb2-119">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="fafb2-119">USD</span></span>           |                           |     <span data-ttu-id="fafb2-120">0.00</span><span class="sxs-lookup"><span data-stu-id="fafb2-120">0.00</span></span>                  |     <span data-ttu-id="fafb2-121">0.00</span><span class="sxs-lookup"><span data-stu-id="fafb2-121">0.00</span></span>                  |     <span data-ttu-id="fafb2-122">2</span><span class="sxs-lookup"><span data-stu-id="fafb2-122">2</span></span>                 |
|     <span data-ttu-id="fafb2-123">خطاب التحصيل 2</span><span class="sxs-lookup"><span data-stu-id="fafb2-123">Collection   letter 2</span></span>         |     <span data-ttu-id="fafb2-124">الإخطار الثاني بالرسوم</span><span class="sxs-lookup"><span data-stu-id="fafb2-124">Second   notification with fee</span></span>        |     <span data-ttu-id="fafb2-125">USC</span><span class="sxs-lookup"><span data-stu-id="fafb2-125">USC</span></span>           |     <span data-ttu-id="fafb2-126">403150</span><span class="sxs-lookup"><span data-stu-id="fafb2-126">403150</span></span>                |     <span data-ttu-id="fafb2-127">20.00</span><span class="sxs-lookup"><span data-stu-id="fafb2-127">20.00</span></span>                 |     <span data-ttu-id="fafb2-128">10.00</span><span class="sxs-lookup"><span data-stu-id="fafb2-128">10.00</span></span>                 |     <span data-ttu-id="fafb2-129">3</span><span class="sxs-lookup"><span data-stu-id="fafb2-129">3</span></span>                 |
|     <span data-ttu-id="fafb2-130">التحصيل</span><span class="sxs-lookup"><span data-stu-id="fafb2-130">Collection</span></span>                    |     <span data-ttu-id="fafb2-131">الإخطار النهائي بالرسوم</span><span class="sxs-lookup"><span data-stu-id="fafb2-131">Final   notification with fee</span></span>         |     <span data-ttu-id="fafb2-132">دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="fafb2-132">USD</span></span>           |     <span data-ttu-id="fafb2-133">403150</span><span class="sxs-lookup"><span data-stu-id="fafb2-133">403150</span></span>                |     <span data-ttu-id="fafb2-134">50.00</span><span class="sxs-lookup"><span data-stu-id="fafb2-134">50.00</span></span>                 |     <span data-ttu-id="fafb2-135">100.00</span><span class="sxs-lookup"><span data-stu-id="fafb2-135">100.00</span></span>                |     <span data-ttu-id="fafb2-136">15</span><span class="sxs-lookup"><span data-stu-id="fafb2-136">15</span></span>                |

<span data-ttu-id="fafb2-137">يبين الرسم التوضيحي التالي المعلومات الموجودة في الجدول كما تظهر في صفحة **خطابات التحصيل**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-137">The following illustration shows the information that's in the table as it would appear on the **Collection letters** page.</span></span> 

<span data-ttu-id="fafb2-138">[![إعداد تسلسل خطاب تحصيل](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)</span><span class="sxs-lookup"><span data-stu-id="fafb2-138">[![Setting up a collection letter sequence](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)</span></span>

 <span data-ttu-id="fafb2-139">يجب أن تقوم الآن بتعيين المعلمتين المطلوبتين لهذا المثال.</span><span class="sxs-lookup"><span data-stu-id="fafb2-139">You must now set the two parameters that are required for this example.</span></span>

2. <span data-ttu-id="fafb2-140">انتقل إلى **الائتمان والتحصيلات \> الإعداد \> معلمات الحسابات المدينة**، واتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="fafb2-140">Go to **Credit and collections \> Setup \> Accounts receivable parameters**, and follow these steps:</span></span>

    1. <span data-ttu-id="fafb2-141">في علامة تبويب **التحصيلات**، قم بتعيين خيار **تجاهل المدفوعات والإشعارات الدائنة عند حساب كود خطاب التحصيل** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-141">On the **Collections** tab, set the **Ignore payments and credit memos when calculating collection letter code** option to **Yes**.</span></span>
    2. <span data-ttu-id="fafb2-142">تأكد من تعيين حقل **إنشاء خطاب تحصيل لكل** على **العميل**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-142">Make sure that the **Create collection letter per** field is set to **Customer**.</span></span>

    <span data-ttu-id="fafb2-143">[![إعداد معلمات الحسابات المدينة لتحصيلات الائتمان](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)</span><span class="sxs-lookup"><span data-stu-id="fafb2-143">[![Setting Accounts receivable parameters for Credit collections](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)</span></span>

3. <span data-ttu-id="fafb2-144">انتقل إلى **الحسابات المدينة \> فواتير \> كافة فواتير النص الحر**، وحدد **جديد**، ثم اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="fafb2-144">Go to **Accounts receivable \> Invoices \> All free text invoices**, select **New**, and then follow these steps:</span></span>

    1. <span data-ttu-id="fafb2-145">في حقل **حساب العميل** حدد **US-045**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-145">In the **Customer account** field select **US-045**.</span></span>
    2. <span data-ttu-id="fafb2-146">في حقل **تاريخ الفاتورة**، أدخل **1/15/2021**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-146">In the **Invoice date** field, enter **1/15/2021**.</span></span>
    3. <span data-ttu-id="fafb2-147">في حقل **‏التاريخ الاستحقاق**، أدخل **1/16/2021**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-147">In the **Due date** field, enter **1/16/2021**.</span></span>
    4. <span data-ttu-id="fafb2-148">في علامة التبويب السريعة **بنود الفاتورة**، في حقل **الحساب الرئيسي**، أدخل **401100**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-148">On the **Invoice lines** FastTab, in the **Main account** field, enter **401100**.</span></span>
    5. <span data-ttu-id="fafb2-149">في الحقل **سعر الوحدة**، أدخل **500.00**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-149">In the **Unit price** field, enter **500.00**.</span></span>
    6. <span data-ttu-id="fafb2-150">حدد **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-150">Select **Post**.</span></span>

    <span data-ttu-id="fafb2-151">ينبعي الآن إدخال إشعارين دائنين للعميل.</span><span class="sxs-lookup"><span data-stu-id="fafb2-151">You must now enter two credit notes for the customer.</span></span>

4. <span data-ttu-id="fafb2-152">حدد **جديد**، ثم اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="fafb2-152">Select **New**, and then follow these steps:</span></span>

    1. <span data-ttu-id="fafb2-153">في حقل **حساب العميل**، حدد **US-045**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-153">In the **Customer account** field, select **US-045**.</span></span>
    2. <span data-ttu-id="fafb2-154">في حقل **تاريخ الفاتورة**، أدخل **1/15/2021**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-154">In the **Invoice date** field, enter **1/15/2021**.</span></span>
    3. <span data-ttu-id="fafb2-155">في حقل **‏التاريخ الاستحقاق**، أدخل **1/16/2021**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-155">In the **Due date** field, enter **1/16/2021**.</span></span>
    4. <span data-ttu-id="fafb2-156">في علامة التبويب السريعة **بنود الفاتورة**، في حقل **الحساب الرئيسي**، أدخل **401100**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-156">On the **Invoice lines** FastTab, in the **Main account** field, enter **401100**.</span></span>
    5. <span data-ttu-id="fafb2-157">في حقل **سعر الوحدة**، أدخل **100.00**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-157">In the **Unit price** field, enter **-100.00**.</span></span>
    6. <span data-ttu-id="fafb2-158">حدد **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-158">Select **Post**.</span></span>

5. <span data-ttu-id="fafb2-159">كرر الخطوة 4، ولكن أدخل **-200.00** في حقل **سعر الوحدة**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-159">Repeat step 4, but enter **-200.00** in the **Unit price** field.</span></span>
6. <span data-ttu-id="fafb2-160">انتقل إلى **الحسابات المدينة \> العملاء \> كافة العملاء**، وحدد العميل **US-045**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-160">Go to **Accounts receivable \> Customers \> All customers**, and select customer **US-045**.</span></span> <span data-ttu-id="fafb2-161">ثم في جزء الإجراء، حدد **الحركات \> الحركات** لمراجعة حركات العميل التي قمت بترحيلها في وقت سابق.</span><span class="sxs-lookup"><span data-stu-id="fafb2-161">Then, on the Action Pane, select **Transactions \> Transactions** to review the customer transactions that you posted earlier.</span></span>

    <span data-ttu-id="fafb2-162">[![مراجعة حركات العميل المرحلة](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)</span><span class="sxs-lookup"><span data-stu-id="fafb2-162">[![Reviewing the posted customer transactions](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)</span></span>

    <span data-ttu-id="fafb2-163">يجب عليك الآن إنشاء خطابات تحصيل للعميل US-045.</span><span class="sxs-lookup"><span data-stu-id="fafb2-163">You must now create collection letters for customer US-045.</span></span>

7. <span data-ttu-id="fafb2-164">انتقل إلى **الائتمان والتحصيلات \> خطاب التحصيل \> إنشاء خطابات تحصيل**، واتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="fafb2-164">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="fafb2-165">قم بتعيين خيارات **الفاتورة** و **الإشعار الائتماني** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-165">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="fafb2-166">بشكل افتراضي، يجب تعيين حقل **خطاب التحصيل** إلى **التحصيل لكل عميل**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-166">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="fafb2-167">في حقل **تاريخ خطاب التحصيل**، أدخل **1/19/2021**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-167">In the **Collection letter date** field, enter **1/19/2021**.</span></span>
    3. <span data-ttu-id="fafb2-168">في علامة التبويب السريعة **السجلات المراد تضمينها**، حدد **عامل التصفية**، ثم في حقل **حساب العميل**، أضف العميل **US-045**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-168">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="fafb2-169">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-169">Select **OK**.</span></span>
    5. <span data-ttu-id="fafb2-170">حدد **موافق** لإنشاء خطابات التحصيل.</span><span class="sxs-lookup"><span data-stu-id="fafb2-170">Select **OK** to create collection letters.</span></span>

8. <span data-ttu-id="fafb2-171">انتقل إلى **الائتمان والتحصيلات \> خطاب التحصيل \> مراجعة ومعالجة خطابات تحصيل**، واتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="fafb2-171">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="fafb2-172">لاحظ أن كود خطاب التحصيل في كل من الرأس وبنود الحركة هو **خطاب التحصيل 1** ، لان خطاب التحصيل هذا هو أول خطاب تحصيل في التسلسل.</span><span class="sxs-lookup"><span data-stu-id="fafb2-172">Notice that the collection letter code on both the header and the transaction lines is **Collection letter 1**, because this collection letter is the first collection letter in the sequence.</span></span> <span data-ttu-id="fafb2-173">(لعرض بنود الحركة، قد تحتاج إلى تحديد علامة التبويب السريعة **الحركات**)</span><span class="sxs-lookup"><span data-stu-id="fafb2-173">(To view the transaction lines, you might have to select the **Transactions** FastTab.)</span></span>

   <span data-ttu-id="fafb2-174">[![تحقق من أن نفس كود خطاب التحصيل يظهر في الرأس والبنود](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)</span><span class="sxs-lookup"><span data-stu-id="fafb2-174">[![Verifying that the same collection letter code appears on the header and the lines](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)</span></span>

    2. <span data-ttu-id="fafb2-175">في جزء الإجراءات، حدد **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-175">On the Action Pane, select **Post**.</span></span>
    3. <span data-ttu-id="fafb2-176">في حقل **تاريخ الترحيل**، أدخل **1/19/2021**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-176">In the **Posting date** field, enter **1/19/2021**.</span></span>

    <span data-ttu-id="fafb2-177">يجب عليك الآن إنشاء خطابات تحصيل مرة أخرى للعميل US-045.</span><span class="sxs-lookup"><span data-stu-id="fafb2-177">You must now create collection letters again for customer US-045.</span></span>

9. <span data-ttu-id="fafb2-178">انتقل إلى **الائتمان والتحصيلات \> خطاب التحصيل \> إنشاء خطابات تحصيل**، واتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="fafb2-178">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="fafb2-179">قم بتعيين خيارات **الفاتورة** و **الإشعار الائتماني** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-179">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="fafb2-180">بشكل افتراضي، يجب تعيين حقل **خطاب التحصيل** إلى **التحصيل لكل عميل**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-180">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="fafb2-181">في حقل **تاريخ خطاب التحصيل**، أدخل **1/23/2021**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-181">In the **Collection letter date** field, enter **1/23/2021**.</span></span>
    3. <span data-ttu-id="fafb2-182">في علامة التبويب السريعة **السجلات المراد تضمينها**، حدد **عامل التصفية**، ثم في حقل **حساب العميل**، أضف العميل **US-045**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-182">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="fafb2-183">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-183">Select **OK**.</span></span>
    5. <span data-ttu-id="fafb2-184">حدد **موافق** لإنشاء خطابات التحصيل.</span><span class="sxs-lookup"><span data-stu-id="fafb2-184">Select **OK** to create collection letters.</span></span>

10. <span data-ttu-id="fafb2-185">انتقل إلى **الائتمان والتحصيلات \> خطاب التحصيل \> مراجعة ومعالجة خطابات تحصيل**، واتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="fafb2-185">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="fafb2-186">لاحظ أن كود خطاب التحصيل في الرأس هو **خطاب التحصيل 1**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-186">Notice that the collection letter code on the header is **Collection letter 1**.</span></span> <span data-ttu-id="fafb2-187">ومع ذلك، فان الكود الموجود في بنود الحركة هو **خطاب التحصيل 2**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-187">However, the code on the transaction lines is **Collection letter 2**.</span></span>

   <span data-ttu-id="fafb2-188">[![تحقق من ظهور أكواد خطاب التحصيل مختلفة في الرأس والبنود](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)</span><span class="sxs-lookup"><span data-stu-id="fafb2-188">[![Verifies that different collection letter codes appear on the header and the lines](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)</span></span>

  <span data-ttu-id="fafb2-189">تختلف الأكواد لأن خيار **تجاهل المدفوعات والإشعارات الدائنة عند حساب كود خطاب التحصيل** تم تعيينه إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-189">The codes differ because the **Ignore payments and credit memos when calculating collection letter code** option is to **Yes**.</span></span>

  2. <span data-ttu-id="fafb2-190">لا تقم بترحيل خطاب التحصيل هذا.</span><span class="sxs-lookup"><span data-stu-id="fafb2-190">Don't post this collection letter.</span></span>

11. <span data-ttu-id="fafb2-191">انتقل إلى **الائتمان والتحصيلات \> الإعداد \> معلمات الحسابات الدائنة**، ثم في علامة تبويب **التحصيلات**، قم بتعيين خيار **تجاهل المدفوعات والإشعارات الدائنة عند حساب كود خطاب التحصيل** إلى **لا**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-191">Go to **Credit and collections \> Setup \> Accounts receivable parameters**, and then, on the **Collections** tab, set the **Ignore payments and credit memos when calculating collection letter code** option to **No**.</span></span>

    <span data-ttu-id="fafb2-192">[![إعداد خيار تجاهل المدفوعات والإشعارات الدائنة عند حساب كود خطاب التحصيل إلى لا](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)</span><span class="sxs-lookup"><span data-stu-id="fafb2-192">[![Setting the Ignore payments and credit memos when calculating collection letter code option to No](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)</span></span>

    <span data-ttu-id="fafb2-193">يجب عليك الآن إنشاء خطابات تحصيل مرة أخرى للعميل US-045.</span><span class="sxs-lookup"><span data-stu-id="fafb2-193">You must now create collection letters again for customer US-045.</span></span>

12. <span data-ttu-id="fafb2-194">انتقل إلى **الائتمان والتحصيلات \> خطاب التحصيل \> إنشاء خطابات تحصيل**، واتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="fafb2-194">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="fafb2-195">قم بتعيين خيارات **الفاتورة** و **الإشعار الائتماني** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-195">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="fafb2-196">بشكل افتراضي، يجب تعيين حقل **خطاب التحصيل** إلى **التحصيل لكل عميل**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-196">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="fafb2-197">في حقل **تاريخ خطاب التحصيل**، أدخل **1/23/2021**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-197">In the **Collection letter date** field, enter **1/23/2021**.</span></span>
    3. <span data-ttu-id="fafb2-198">في علامة التبويب السريعة **السجلات المراد تضمينها**، حدد **عامل التصفية**، ثم في حقل **حساب العميل**، أضف العميل **US-045**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-198">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="fafb2-199">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-199">Select **OK**.</span></span>
    5. <span data-ttu-id="fafb2-200">حدد **موافق** لإنشاء خطابات التحصيل.</span><span class="sxs-lookup"><span data-stu-id="fafb2-200">Select **OK** to create collection letters.</span></span>

13. <span data-ttu-id="fafb2-201">انتقل إلى **الائتمان والتحصيلات \> خطاب التحصيل \> مراجعة ومعالجة خطابات التحصيل**، ولاحظ أن كود خطاب التحصيل في كل من الرأس وبنود الحركة **خطاب التحصيل 2**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-201">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and notice that the collection letter code on both the header and the transaction lines is **Collection letter 2**.</span></span>

    <span data-ttu-id="fafb2-202">[![ظهور نفس كود خطاب التحصيل مرة أخرى في الرأس والبنود](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)</span><span class="sxs-lookup"><span data-stu-id="fafb2-202">[![Showing again that the same collection letter code appears on the header and the lines](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)</span></span>

    <span data-ttu-id="fafb2-203">يظهر نفس الكود في كل المكانين لأن خيار **تجاهل المدفوعات والإشعارات الدائنة عند حساب كود خطاب التحصيل** تم تعيينه الآن إلى **لا**.</span><span class="sxs-lookup"><span data-stu-id="fafb2-203">The same code appears in both places because the **Ignore payments and credit memos when calculating collection letter code** option is now set to **No**.</span></span>
