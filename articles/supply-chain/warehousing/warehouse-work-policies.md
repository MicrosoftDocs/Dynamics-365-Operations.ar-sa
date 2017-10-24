---
title: "سياسات عمل المستودع"
description: "تتحكم سياسات عمل المستودع فيما إذا كان عمل المستودع ينشأ نتيجة عمليات المستودع في التصنيع، استنادًا إلى نوع أمر العمل وموقع المخزون والمنتج."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 196561
ms.assetid: cbf48ec6-1836-48d5-ad66-a9b534af1786
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: ec7dd3b91851729e866bc90ca85a118839f9d71d
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="warehouse-work-policies"></a><span data-ttu-id="14096-103">سياسات عمل المستودع</span><span class="sxs-lookup"><span data-stu-id="14096-103">Warehouse work policies</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="14096-104">تتحكم سياسات عمل المستودع في Microsoft Dynamics 365 for Finance and Operations, Enterprise edition فيما إذا كان عمل المستودع ينشأ نتيجة عمليات المستودع في التصنيع، استنادًا إلى نوع أمر العمل وموقع المخزون والمنتج.</span><span class="sxs-lookup"><span data-stu-id="14096-104">Warehouse work policies in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition control whether warehouse work is created by warehouse processes in manufacturing, based on work order type, inventory location, and product.</span></span>

<span data-ttu-id="14096-105">تتحكم سياسة العمل هذه في إنشاء عمل المستودع لعمليات المستودع في التصنيع.</span><span class="sxs-lookup"><span data-stu-id="14096-105">This work policy controls whether warehouse work is created for warehouse processes in manufacturing.</span></span> <span data-ttu-id="14096-106">ويمكنك إعداد سياسة العمل باستخدام مجموعة تتكون من **أنواع أوامر العمل** و**موقع المخزون** و**منتج**.</span><span class="sxs-lookup"><span data-stu-id="14096-106">You can set up the work policy by using a combination of **work order types**, an **inventory location**, and a **product**.</span></span> <span data-ttu-id="14096-107">‏‫على سبيل المثال، يتم الإبلاغ عن المنتج L0101 على أنه منتج منتهٍ في موقع المخرجات 001.</span><span class="sxs-lookup"><span data-stu-id="14096-107">For example, product L0101 is reported as finished to output location 001.</span></span> <span data-ttu-id="14096-108">ويتم في وقت لاحق استهلاك البضائع المنتهية في أمر إنتاج آخر في موقع المخرجات 001.</span><span class="sxs-lookup"><span data-stu-id="14096-108">The finished good is later consumed in another production order at output location 001.</span></span> <span data-ttu-id="14096-109">في هذه الحالة، يمكنك إعداد سياسة عمل لمنع إنشاء العمل المتعلق بتخزين البضائع المنتهية عند الإبلاغ عن المنتج L0101 على أنه منتج منتهٍ في موقع المخرجات 001.</span><span class="sxs-lookup"><span data-stu-id="14096-109">In this case, you can set up a work policy to prevent the work for finished goods put-away from being created when you report product L0101 as finished to output location 001.</span></span> <span data-ttu-id="14096-110">تُعد سياسة العمل كيانًا فرديًا يمكن وصفه من خلال المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="14096-110">The work policy is an individual entity that can be described through the following information:</span></span>

-   <span data-ttu-id="14096-111">**اسم سياسة العمل**(المعرف الفريد لسياسة العمل)</span><span class="sxs-lookup"><span data-stu-id="14096-111">**Work policy name** (the unique identifier of the work policy)</span></span>
-   <span data-ttu-id="14096-112">**أنواع أوامر العمل**و**طريقة إنشاء العمل‬**</span><span class="sxs-lookup"><span data-stu-id="14096-112">**Work order types** and **Work creation method**</span></span>
-   <span data-ttu-id="14096-113">**مواقع المخزون**</span><span class="sxs-lookup"><span data-stu-id="14096-113">**Inventory locations**</span></span>
-   <span data-ttu-id="14096-114">**المنتجات**</span><span class="sxs-lookup"><span data-stu-id="14096-114">**Products**</span></span>

## <a name="work-order-types"></a><span data-ttu-id="14096-115">أنواع أمر العمل</span><span class="sxs-lookup"><span data-stu-id="14096-115">Work order types</span></span>
<span data-ttu-id="14096-116">يمكنك تحديد أنواع أوامر العمل التالية:</span><span class="sxs-lookup"><span data-stu-id="14096-116">You can select the following work order types:</span></span>

-   <span data-ttu-id="14096-117">تخزين البضائع المنتهية</span><span class="sxs-lookup"><span data-stu-id="14096-117">Finished goods put away</span></span>
-   <span data-ttu-id="14096-118">تخزين منتج مساعد ومنتج ثانوي</span><span class="sxs-lookup"><span data-stu-id="14096-118">Co-product and by-product put away</span></span>
-   <span data-ttu-id="14096-119">انتقاء المواد الخام</span><span class="sxs-lookup"><span data-stu-id="14096-119">Raw material picking</span></span>

<span data-ttu-id="14096-120">يتضمن الحقل **طريقة إنشاء العمل‬** القيمة **أبدًا‬**.</span><span class="sxs-lookup"><span data-stu-id="14096-120">The **Work creation method** field has the value **Never**.</span></span> <span data-ttu-id="14096-121">تشير هذه القيمة إلى أن سياسة العمل سوف تمنع إنشاء عمل المستودع لنوع أمر العمل المحدد.</span><span class="sxs-lookup"><span data-stu-id="14096-121">This value indicates that the work policy will prevent warehouse work from being created for the selected work order type.</span></span>

## <a name="inventory-locations"></a><span data-ttu-id="14096-122">مواقع المخزون</span><span class="sxs-lookup"><span data-stu-id="14096-122">Inventory locations</span></span>
<span data-ttu-id="14096-123">يمكنك تحديد موقع تنطبق عليه سياسة العمل.</span><span class="sxs-lookup"><span data-stu-id="14096-123">You can select a location that the work policy applies to.</span></span> <span data-ttu-id="14096-124">في حال عدم وجود أي موقع مقترن بسياسة عمل، لن تنطبق سياسة العمل على أي عملية.</span><span class="sxs-lookup"><span data-stu-id="14096-124">If no location is associated with a work policy, the work policy doesn’t apply to any processes.</span></span> <span data-ttu-id="14096-125">في صفحة **المواقع**، يمكنك أيضًا تحديد أو إلغاء تحديد سياسة العمل لموقع معين.</span><span class="sxs-lookup"><span data-stu-id="14096-125">On the **Locations** page, you can also select or cancel the selection of the work policy for a specific location.</span></span>

## <a name="products"></a><span data-ttu-id="14096-126">المنتجات</span><span class="sxs-lookup"><span data-stu-id="14096-126">Products</span></span>
<span data-ttu-id="14096-127">يمكنك تحديد منتج تنطبق عليه سياسة العمل.</span><span class="sxs-lookup"><span data-stu-id="14096-127">You can select a product that the work policy applies to.</span></span> <span data-ttu-id="14096-128">ويمكنك تطبيق سياسة العمل على كل المنتجات أو على منتجات محددة.</span><span class="sxs-lookup"><span data-stu-id="14096-128">You can apply the work policy to either all products or selected products.</span></span>

## <a name="example"></a><span data-ttu-id="14096-129">مثال</span><span class="sxs-lookup"><span data-stu-id="14096-129">Example</span></span>
<span data-ttu-id="14096-130">في المثال التالي، هناك أمرا إنتاج، PRD-001 وPRD-00*2*.</span><span class="sxs-lookup"><span data-stu-id="14096-130">In the following example, there are two production orders, PRD-001 and PRD-00*2*.</span></span> <span data-ttu-id="14096-131">يتضمن أمر الإنتاج PRD-001 عملية تسمى **التجميع**، حيث يتم الإبلاغ عن المنتج SC1 كمنتج منتهٍ في الموقع O1.</span><span class="sxs-lookup"><span data-stu-id="14096-131">Production order PRD-001 has an operation that is named **Assembly**, where product SC1 is being reported as finished to location O1.</span></span> <span data-ttu-id="14096-132">أما أمر الإنتاج PRD-002 فلديه عملية تسمى **الطلاء** وهو يستهلك المنتج SC1 من الموقع O1.</span><span class="sxs-lookup"><span data-stu-id="14096-132">Production order PRD-002 has an operation that is named **Painting** and consumes product SC1 from location O1.</span></span> <span data-ttu-id="14096-133">يستهلك أمر الإنتاج PRD-002 أيضًا المواد الخام RM1 من الموقع O1.</span><span class="sxs-lookup"><span data-stu-id="14096-133">Production order PRD-002 also consumes raw material RM1 from location O1.</span></span> <span data-ttu-id="14096-134">تكون المواد الخام RM1 مخزنة في موقع المستودع BULK-001 وسيتم نقل هذه المواد إلى الموقع O1 بواسطة عامل المستودع لانتقاء المواد الخام.</span><span class="sxs-lookup"><span data-stu-id="14096-134">RM1 is stored in warehouse location BULK-001 and will be picked to location O1 by warehouse work for raw material picking.</span></span> <span data-ttu-id="14096-135">يتم إنشاء عمل الانتقاء عند إصدار أمر الإنتاج PRD-002.</span><span class="sxs-lookup"><span data-stu-id="14096-135">The picking work is generated when production PRD-002 is released.</span></span> 

<span data-ttu-id="14096-136">[![سياسات عمل المستودع](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span><span class="sxs-lookup"><span data-stu-id="14096-136">[![Warehouse work policies](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span></span> 

<span data-ttu-id="14096-137">عندما تخطط لتكوين سياسة عمل المستودع لهذا السيناريو، يجب مراعاة المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="14096-137">When you plan to configure a warehouse work policy for this scenario, you should consider the following information:</span></span>

-   <span data-ttu-id="14096-138">عمل المستودع لتخزين البضائع المنتهية غير مطلوب عند التبليغ عن المنتج SC1 كمنتج منتهٍ من أمر الإنتاج PRD-001 إلى الموقع O1.</span><span class="sxs-lookup"><span data-stu-id="14096-138">Warehouse work for finished goods put-away isn’t required when you report product SC1 as finished from production order PRD-001 to location O1.</span></span> <span data-ttu-id="14096-139">وسبب ذلك هو أن عملية **الطلاء** لأمر الإنتاج PRD-002 تستهلك المنتج SC1 في الموقع نفسه.</span><span class="sxs-lookup"><span data-stu-id="14096-139">This is because the **Painting** operation for production order PRD-002 consumes SC1 at the same location.</span></span>
-   <span data-ttu-id="14096-140">عمل المستودع لانتقاء المواد الخام مطلوب لنقل المواد الخام RM1 من موقع المستودع BULK-001 إلى الموقع O1.</span><span class="sxs-lookup"><span data-stu-id="14096-140">Warehouse work for raw material picking is required in order to move raw material RM1 from warehouse location BULK-001 to location O1.</span></span>

<span data-ttu-id="14096-141">إليك مثال عن سياسة العمل التي يمكنك إعدادها، استنادًا إلى هذه الاعتبارات.</span><span class="sxs-lookup"><span data-stu-id="14096-141">Here is an example of the work policy that you can set up, based on these considerations.</span></span>

|                                         |                                                       |
|-----------------------------------------|-------------------------------------------------------|
|<span data-ttu-id="14096-142">**اسم سياسة العمل**</span><span class="sxs-lookup"><span data-stu-id="14096-142">**Work policy name**</span></span><br>                 |<span data-ttu-id="14096-143">**أنواع أمر العمل**</span><span class="sxs-lookup"><span data-stu-id="14096-143">**Work order types**</span></span><br>                               |
| <span data-ttu-id="14096-144">لا تخزين 01     \`</span><span class="sxs-lookup"><span data-stu-id="14096-144">No put away 01     \`</span></span>                    |<span data-ttu-id="14096-145">- تخزين البضائع المنتهية</span><span class="sxs-lookup"><span data-stu-id="14096-145">- Finished good put away</span></span><br>                           |
|                                         |<span data-ttu-id="14096-146">**المواقع**</span><span class="sxs-lookup"><span data-stu-id="14096-146">**Locations**</span></span><br>                                      |
|                                         |<span data-ttu-id="14096-147">- O1</span><span class="sxs-lookup"><span data-stu-id="14096-147">- O1</span></span>   |                                               |
|                                         |<span data-ttu-id="14096-148">**المنتجات**</span><span class="sxs-lookup"><span data-stu-id="14096-148">**Products**</span></span> <br>                                      |
|                                         |<span data-ttu-id="14096-149">- SC1</span><span class="sxs-lookup"><span data-stu-id="14096-149">- SC1</span></span>                                                  |

<span data-ttu-id="14096-150">توفر الإجراءات التالية إرشادات خطوة بخطوة حول كيفية إعداد سياسة عمل المستودع لهذا السيناريو.</span><span class="sxs-lookup"><span data-stu-id="14096-150">The following procedures provide step-by-step instructions about how to set up the warehouse work policy for this scenario.</span></span> <span data-ttu-id="14096-151">كما سيتم وصف إعداد نموذجي يظهر كيفية الإبلاغ عن أمر إنتاج كمنتهٍ إلى موقع لا غير خاضع للتحكم بواسطة لوحة الترخيص.‬</span><span class="sxs-lookup"><span data-stu-id="14096-151">A sample setup showing how to report a production order as finished to a location that isn’t license plate–controlled is also described.</span></span>

## <a name="set-up-a-warehouse-work-policy"></a><span data-ttu-id="14096-152">إعداد سياسة عمل المستودع</span><span class="sxs-lookup"><span data-stu-id="14096-152">Set up a warehouse work policy</span></span>
<span data-ttu-id="14096-153">لا تشمل عمليات المستودع دائمًا عمل المستودع.</span><span class="sxs-lookup"><span data-stu-id="14096-153">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="14096-154">بتحديد سياسة العمل، يمكنك منع إنشاء عمل لانتقاء المواد الخام وتخزين البضائع المنتهية لمجموعة من المنتجات في مواقع محددة.</span><span class="sxs-lookup"><span data-stu-id="14096-154">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="14096-155">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="14096-155">The USMF demo data company was used to create this procedure.</span></span> 

<span data-ttu-id="14096-156">الخطوات (21)</span><span class="sxs-lookup"><span data-stu-id="14096-156">STEPS (21)</span></span>

|     |                                                                            |
|-----|----------------------------------------------------------------------------|
| <span data-ttu-id="14096-157">1</span><span class="sxs-lookup"><span data-stu-id="14096-157">1.</span></span>  | <span data-ttu-id="14096-158">انتقل إلى إدارة المستودعات &gt; الإعداد &gt; العمل &gt; سياسات العمل.</span><span class="sxs-lookup"><span data-stu-id="14096-158">Go to Warehouse management &gt; Setup &gt; Work &gt; Work policies.</span></span>        |
| <span data-ttu-id="14096-159">2</span><span class="sxs-lookup"><span data-stu-id="14096-159">2.</span></span>  | <span data-ttu-id="14096-160">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="14096-160">Click New.</span></span>                                                                 |
| <span data-ttu-id="14096-161">3</span><span class="sxs-lookup"><span data-stu-id="14096-161">3.</span></span>  | <span data-ttu-id="14096-162">في الحقل "اسم سياسة العمل"، اكتب "لا عمل تخزين".</span><span class="sxs-lookup"><span data-stu-id="14096-162">In the Work policy name field, type 'No put-away work'.</span></span>                    |
| <span data-ttu-id="14096-163">4</span><span class="sxs-lookup"><span data-stu-id="14096-163">4.</span></span>  | <span data-ttu-id="14096-164">انقر فوق حفظ.</span><span class="sxs-lookup"><span data-stu-id="14096-164">Click Save.</span></span>                                                                |
| <span data-ttu-id="14096-165">5.</span><span class="sxs-lookup"><span data-stu-id="14096-165">5.</span></span>  | <span data-ttu-id="14096-166">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="14096-166">Click Add.</span></span>                                                                 |
| <span data-ttu-id="14096-167">6.</span><span class="sxs-lookup"><span data-stu-id="14096-167">6.</span></span>  | <span data-ttu-id="14096-168">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="14096-168">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="14096-169">7.</span><span class="sxs-lookup"><span data-stu-id="14096-169">7.</span></span>  | <span data-ttu-id="14096-170">في الحقل "نوع طلب العمل"، حدد "تخزين البضائع المنتهية".</span><span class="sxs-lookup"><span data-stu-id="14096-170">In the Work order type field, select 'Finished goods put away'.</span></span>            |
| <span data-ttu-id="14096-171">8.</span><span class="sxs-lookup"><span data-stu-id="14096-171">8.</span></span>  | <span data-ttu-id="14096-172">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="14096-172">Click Add.</span></span>                                                                 |
| <span data-ttu-id="14096-173">9.</span><span class="sxs-lookup"><span data-stu-id="14096-173">9.</span></span>  | <span data-ttu-id="14096-174">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="14096-174">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="14096-175">10.</span><span class="sxs-lookup"><span data-stu-id="14096-175">10.</span></span> | <span data-ttu-id="14096-176">في الحقل "نوع طلب العمل"، حدد "مخزون المنتج المساعد والمنتج الثانوي".</span><span class="sxs-lookup"><span data-stu-id="14096-176">In the Work order type field, select 'Co-product and by-product put away'.</span></span> |
| <span data-ttu-id="14096-177">11.</span><span class="sxs-lookup"><span data-stu-id="14096-177">11.</span></span> | <span data-ttu-id="14096-178">قم بتوسيع مقطع "مواقع المخزون".</span><span class="sxs-lookup"><span data-stu-id="14096-178">Expand the Inventory locations section.</span></span>                                    |
| <span data-ttu-id="14096-179">12.</span><span class="sxs-lookup"><span data-stu-id="14096-179">12.</span></span> | <span data-ttu-id="14096-180">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="14096-180">Click Add.</span></span>                                                                 |
| <span data-ttu-id="14096-181">13.</span><span class="sxs-lookup"><span data-stu-id="14096-181">13.</span></span> | <span data-ttu-id="14096-182">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="14096-182">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="14096-183">14.</span><span class="sxs-lookup"><span data-stu-id="14096-183">14.</span></span> | <span data-ttu-id="14096-184">في قائمة المستودع، أدخل "51".</span><span class="sxs-lookup"><span data-stu-id="14096-184">In the Warehouse list, enter '51'.</span></span>                                         |
| <span data-ttu-id="14096-185">15.</span><span class="sxs-lookup"><span data-stu-id="14096-185">15.</span></span> | <span data-ttu-id="14096-186">في الحقل "الموقع"، أدخل قيمة "001" أو حددها.</span><span class="sxs-lookup"><span data-stu-id="14096-186">In the Location field, enter or select '001'.</span></span>                              |
| <span data-ttu-id="14096-187">16.</span><span class="sxs-lookup"><span data-stu-id="14096-187">16.</span></span> | <span data-ttu-id="14096-188">قم بتوسيع قسم "المنتجات".</span><span class="sxs-lookup"><span data-stu-id="14096-188">Expand the Products section.</span></span>                                               |
| <span data-ttu-id="14096-189">17.</span><span class="sxs-lookup"><span data-stu-id="14096-189">17.</span></span> | <span data-ttu-id="14096-190">في الحقل "‏‫قسم المنتج‬"، حدد "محدد".</span><span class="sxs-lookup"><span data-stu-id="14096-190">In the Product selection field, select 'Selected'.</span></span>                         |
| <span data-ttu-id="14096-191">18.</span><span class="sxs-lookup"><span data-stu-id="14096-191">18.</span></span> | <span data-ttu-id="14096-192">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="14096-192">Click Add.</span></span>                                                                 |
| <span data-ttu-id="14096-193">19.</span><span class="sxs-lookup"><span data-stu-id="14096-193">19.</span></span> | <span data-ttu-id="14096-194">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="14096-194">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="14096-195">20.</span><span class="sxs-lookup"><span data-stu-id="14096-195">20.</span></span> | <span data-ttu-id="14096-196">في الحقل "رقم الصنف"، أدخل "L0101" أو حددها.</span><span class="sxs-lookup"><span data-stu-id="14096-196">In the Item number field, enter or select 'L0101'.</span></span>                         |
| <span data-ttu-id="14096-197">21.</span><span class="sxs-lookup"><span data-stu-id="14096-197">21.</span></span> | <span data-ttu-id="14096-198">انقر فوق حفظ.</span><span class="sxs-lookup"><span data-stu-id="14096-198">Click Save.</span></span>                                                                |

## <a name="report-a-production-order-as-finished-to-a-location-that-isnt-license-platecontrolled"></a><span data-ttu-id="14096-199">الإبلاغ عن أمر إنتاج كمنتهٍ في موقع غير خاضع لمراقبة لوحة ترخيص</span><span class="sxs-lookup"><span data-stu-id="14096-199">Report a production order as finished to a location that isn’t license plate–controlled</span></span>
<span data-ttu-id="14096-200">يعرض هذا الإجراء مثالاً للإبلاغ عن منتج كمنتهٍ إلى موقع غير خاضع لمراقبة لوحة الترخيص.</span><span class="sxs-lookup"><span data-stu-id="14096-200">This procedure shows an example of reporting as finished to a location that isn't license plate–controlled.</span></span> <span data-ttu-id="14096-201">تُعد سياسة العمل القابلة للتطبيق المتطلب الأساسي لهذه المهمة.</span><span class="sxs-lookup"><span data-stu-id="14096-201">An applicable work policy is the prerequisite for this task.</span></span> <span data-ttu-id="14096-202">يعرض الإجراء السابق إعداد سياسة العمل.</span><span class="sxs-lookup"><span data-stu-id="14096-202">The previous procedure shows the setup of the work policy.</span></span> 

<span data-ttu-id="14096-203">الخطوات (25)</span><span class="sxs-lookup"><span data-stu-id="14096-203">STEPS (25)</span></span>

<table>
<tbody>
<tr>
<td colspan="3"><span data-ttu-id="14096-204"><strong>المهمة الفرعية: إعداد موقع المخرجات.</strong></span><span class="sxs-lookup"><span data-stu-id="14096-204"><strong>Sub-task: Set up an output location.</strong></span></span></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td><span data-ttu-id="14096-205">انتقل إلى إدارة المؤسسة &gt; الموارد &gt; مجموعات الموارد.</span><span class="sxs-lookup"><span data-stu-id="14096-205">Go to Organization administration &gt; Resources &gt; Resource groups.</span></span></td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td><span data-ttu-id="14096-206">في القائمة، حدد مجموعة الموارد "5102".</span><span class="sxs-lookup"><span data-stu-id="14096-206">In the list, select resource group '5102'.</span></span></td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td><span data-ttu-id="14096-207">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="14096-207">Click Edit.</span></span></td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td><span data-ttu-id="14096-208">في الحقل "مستودع المخرجات"، أدخل "51".</span><span class="sxs-lookup"><span data-stu-id="14096-208">In the Output warehouse field, enter '51'.</span></span></td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td><span data-ttu-id="14096-209">في الحقل "موقع الإخراج"، أدخل "001".</span><span class="sxs-lookup"><span data-stu-id="14096-209">In the Output location field, enter '001'.</span></span></td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td><span data-ttu-id="14096-210">الموقع 001 غير خاضع للتحكم بواسطة لوحة الترخيص.</span><span class="sxs-lookup"><span data-stu-id="14096-210">Location 001 isn't a license plate–controlled location.</span></span> <span data-ttu-id="14096-211">يمكنك إعداد موقع إخراج غير لوحة غير مرخصة فقط في حالة وجود سياسة عمل قابلة للتطبيق للموقع.</span><span class="sxs-lookup"><span data-stu-id="14096-211">You can set up a non–license plate output location only if an applicable work policy exists for the location.</span></span></td>
</tr>
<tr>
<td colspan="3"><span data-ttu-id="14096-212"><strong>المهمة الفرعية: إنشاء أمر الإنتاج والإبلاغ عنه كمنتهٍ.</strong></span><span class="sxs-lookup"><span data-stu-id="14096-212"><strong>Sub-task: Create a production order and report it as finished.</strong></span></span></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td><span data-ttu-id="14096-213">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="14096-213">Close the page.</span></span></td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td><span data-ttu-id="14096-214">انتقل إلى التحكم بالإنتاج‬ &gt; أوامر الإنتاج &gt; كافة أوامر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="14096-214">Go to Production control &gt; Production orders &gt; All production orders.</span></span></td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td><span data-ttu-id="14096-215">انقر فوق "أمر إنتاج جديد".</span><span class="sxs-lookup"><span data-stu-id="14096-215">Click New production order.</span></span></td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td><span data-ttu-id="14096-216">في الحقل "رقم الصنف"، أدخل "L0101".</span><span class="sxs-lookup"><span data-stu-id="14096-216">In the Item number field, enter 'L0101'.</span></span></td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td><span data-ttu-id="14096-217">انقر فوق إنشاء.</span><span class="sxs-lookup"><span data-stu-id="14096-217">Click Create.</span></span></td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td><span data-ttu-id="14096-218">في جزء الإجراءات، انقر فوق "أمر إنتاج".</span><span class="sxs-lookup"><span data-stu-id="14096-218">On the Action Pane, click Production order.</span></span></td>
</tr>
<tr>
<td></td>
<td>7.</td>
<td><span data-ttu-id="14096-219">انقر فوق "تقدير".</span><span class="sxs-lookup"><span data-stu-id="14096-219">Click Estimate.</span></span></td>
</tr>
<tr>
<td></td>
<td>8.</td>
<td><span data-ttu-id="14096-220">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="14096-220">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>9.</td>
<td><span data-ttu-id="14096-221">انقر فوق "بدء".</span><span class="sxs-lookup"><span data-stu-id="14096-221">Click Start.</span></span></td>
</tr>
<tr>
<td></td>
<td>10.</td>
<td><span data-ttu-id="14096-222">انقر فوق علامة التبويب عام.</span><span class="sxs-lookup"><span data-stu-id="14096-222">Click the General tab.</span></span></td>
</tr>
<tr>
<td></td>
<td>11.</td>
<td><span data-ttu-id="14096-223">في الحقل "‏‫استهلاك قائمة مكونات الصنف التلقائي‬"، حدد "أبدًا".</span><span class="sxs-lookup"><span data-stu-id="14096-223">In the Automatic BOM consumption field, select 'Never'.</span></span></td>
</tr>
<tr>
<td></td>
<td>12.</td>
<td><span data-ttu-id="14096-224">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="14096-224">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>13.</td>
<td><span data-ttu-id="14096-225">انقر فوق "الإبلاغ كمنتهٍ".</span><span class="sxs-lookup"><span data-stu-id="14096-225">Click Report as finished.</span></span></td>
</tr>
<tr>
<td></td>
<td>14.</td>
<td><span data-ttu-id="14096-226">انقر فوق علامة التبويب عام.</span><span class="sxs-lookup"><span data-stu-id="14096-226">Click the General tab.</span></span></td>
</tr>
<tr>
<td></td>
<td>15.</td>
<td><span data-ttu-id="14096-227">حدد "نعم" في الحقل "قبول الخطأ".</span><span class="sxs-lookup"><span data-stu-id="14096-227">Select Yes in the Accept error field.</span></span></td>
</tr>
<tr>
<td></td>
<td>16.</td>
<td><span data-ttu-id="14096-228">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="14096-228">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>17.</td>
<td><span data-ttu-id="14096-229">في جزء الإجراءات، انقر فوق "مستودع".</span><span class="sxs-lookup"><span data-stu-id="14096-229">On the Action Pane, click Warehouse.</span></span></td>
</tr>
<tr>
<td></td>
<td>18.</td>
<td><span data-ttu-id="14096-230">انقر فوق تفاصيل العمل.</span><span class="sxs-lookup"><span data-stu-id="14096-230">Click Work details.</span></span></td>
</tr>
<tr>
<td></td>
<td>19.</td>
<td><span data-ttu-id="14096-231">عندما تم الإبلاغ عن أمر الإنتاج كمنته، فإنه لا يتم إنشاء عمل للتخزين.</span><span class="sxs-lookup"><span data-stu-id="14096-231">When the production order was reported as finished, no work was generated for put-away.</span></span> <span data-ttu-id="14096-232">يحدث هذا لأنه يتم تعريف سياسة عمل تمنع إنشاء العمل عندما يتم الإبلاغ عن المنتج L0101 كمنته للموقع 001.</span><span class="sxs-lookup"><span data-stu-id="14096-232">This occurs because a work policy is defined that prevents work from being generated when product L0101 is reported as finished to location 001.</span></span></td>
</tr>
</tbody>
</table>




