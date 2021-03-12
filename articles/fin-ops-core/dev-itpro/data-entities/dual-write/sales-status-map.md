---
title: إعداد التعيين أعمدة حالة أمر المبيعات
description: يوضح هذا الموضوع كيفية إعداد أعمدة حالات أمر المبيعات للكتابة المزدوجة.
author: dasani-madipalli
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: damadipa
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: cc70501d231390ea15104d508a36300a1b2cd44c
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744289"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-columns"></a><span data-ttu-id="34831-103">إعداد التعيين أعمدة حالة أمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="34831-103">Set up the mapping for the sales order status columns</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="34831-104">تحتوي الأعمدة التي تشير إلى حالة أمر المبيعات على قيم تعداد مختلفة في Microsoft Dynamics 365 Supply Chain Management وDynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="34831-104">The columns that indicate sales order status have different enumeration values in Microsoft Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="34831-105">هناك حاجة إلى إعداد إضافي لتعيين هذه الأعمدة في الكتابة المزدوجة.</span><span class="sxs-lookup"><span data-stu-id="34831-105">Additional setup is required to map these columns in dual-write.</span></span>

## <a name="columns-in-supply-chain-management"></a><span data-ttu-id="34831-106">الأعمدة في Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="34831-106">columns in Supply Chain Management</span></span>

<span data-ttu-id="34831-107">في Supply Chain Management، يعكس العمودان حالة أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="34831-107">In Supply Chain Management, two columns reflect the status of the sales order.</span></span> <span data-ttu-id="34831-108">العمودان اللذان يجب عليكما تعيينهما هما **الحالة** و **حالة المستند**.</span><span class="sxs-lookup"><span data-stu-id="34831-108">The columns that you must map are **Status** and **Document Status**.</span></span>

<span data-ttu-id="34831-109">يحدد تعداد **الحالة** الحالة الإجمالية  للأمر.</span><span class="sxs-lookup"><span data-stu-id="34831-109">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="34831-110">تظهر هذه الحالة على رأس الأمر.</span><span class="sxs-lookup"><span data-stu-id="34831-110">This status is shown on the order header.</span></span>

<span data-ttu-id="34831-111">يتضمن تعداد **الحالة** القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="34831-111">The **Status** enumeration has the following values:</span></span>

- <span data-ttu-id="34831-112">أمر مفتوح</span><span class="sxs-lookup"><span data-stu-id="34831-112">Open Order</span></span>
- <span data-ttu-id="34831-113">تم التسليم</span><span class="sxs-lookup"><span data-stu-id="34831-113">Delivered</span></span>
- <span data-ttu-id="34831-114">مفوتر</span><span class="sxs-lookup"><span data-stu-id="34831-114">Invoiced</span></span>
- <span data-ttu-id="34831-115">تم الإلغاء</span><span class="sxs-lookup"><span data-stu-id="34831-115">Cancelled</span></span>

<span data-ttu-id="34831-116">يحدد تعداد **حالة المستند** أحدث مستند تم إنشاؤه للأمر.</span><span class="sxs-lookup"><span data-stu-id="34831-116">The **Document Status** enumeration specifies the most recent document that was generated for the order.</span></span> <span data-ttu-id="34831-117">على سبيل المثال، إذا تم تأكيد الأمر، فإن هذا المستند هو تأكيد أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="34831-117">For example, if the order is confirmed, this document is a sales order confirmation.</span></span> <span data-ttu-id="34831-118">إذا تمت فوترة أمر المبيعات بشكل جزئي، ثم تم تأكيد البند المتبقي، تبقى حالة المستند **فاتورة**، بسبب إنشاء الفاتورة لاحقًا في العملية.</span><span class="sxs-lookup"><span data-stu-id="34831-118">If a sales order is partially invoiced, and then the remaining line is confirmed, the document status remains **Invoice**, because the invoice is generated later in the process.</span></span>

<span data-ttu-id="34831-119">يتضمن تعداد **حالة المستند** القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="34831-119">The **Document Status** enumeration has the following values:</span></span>

- <span data-ttu-id="34831-120">التأكيد</span><span class="sxs-lookup"><span data-stu-id="34831-120">Confirmation</span></span>
- <span data-ttu-id="34831-121">قائمة الانتقاء</span><span class="sxs-lookup"><span data-stu-id="34831-121">Picking List</span></span>
- <span data-ttu-id="34831-122">كشف التعبئة</span><span class="sxs-lookup"><span data-stu-id="34831-122">Packing Slip</span></span>
- <span data-ttu-id="34831-123">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="34831-123">Invoice</span></span>

## <a name="columns-in-sales"></a><span data-ttu-id="34831-124">أعمده في المبيعات</span><span class="sxs-lookup"><span data-stu-id="34831-124">columns in Sales</span></span>

<span data-ttu-id="34831-125">في Sales، يشير العمودان إلى حالة الأمر.</span><span class="sxs-lookup"><span data-stu-id="34831-125">In Sales, two columns indicate the status of the order.</span></span> <span data-ttu-id="34831-126">العمودان اللذان يجب عليكما تعيينهما هما **الحالة** و **حالة المعالجة‬**.</span><span class="sxs-lookup"><span data-stu-id="34831-126">The columns that you must map are **Status** and **Processing Status**.</span></span>

<span data-ttu-id="34831-127">يحدد تعداد **الحالة** الحالة الإجمالية  للأمر.</span><span class="sxs-lookup"><span data-stu-id="34831-127">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="34831-128">لديه القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="34831-128">It has the following values:</span></span>

- <span data-ttu-id="34831-129">نشط</span><span class="sxs-lookup"><span data-stu-id="34831-129">Active</span></span>
- <span data-ttu-id="34831-130">‏‫مُرسل</span><span class="sxs-lookup"><span data-stu-id="34831-130">Submitted</span></span>
- <span data-ttu-id="34831-131">تم الاستيفاء</span><span class="sxs-lookup"><span data-stu-id="34831-131">Fulfilled</span></span>
- <span data-ttu-id="34831-132">مفوتر</span><span class="sxs-lookup"><span data-stu-id="34831-132">Invoiced</span></span>
- <span data-ttu-id="34831-133">تم الإلغاء</span><span class="sxs-lookup"><span data-stu-id="34831-133">Cancelled</span></span>

<span data-ttu-id="34831-134">تم تقديم تعداد **حالة المعالجة** بحيث يمكن تعيين الحالة بدقة أكبر مع Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="34831-134">The **Processing Status** enumeration was introduced so that the status can be mapped more accurately with Supply Chain Management.</span></span>

<span data-ttu-id="34831-135">يعرض الجدول التالي تعيين **حالة المعالجة** في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="34831-135">The following table shows the mapping of **Processing Status** in Supply Chain Management.</span></span>

| <span data-ttu-id="34831-136">حالة المعالجة</span><span class="sxs-lookup"><span data-stu-id="34831-136">Processing Status</span></span>   | <span data-ttu-id="34831-137">الحالة في Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="34831-137">Status in Supply Chain Management</span></span> | <span data-ttu-id="34831-138">حالة المستند في Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="34831-138">Document Status in Supply Chain Management</span></span> |
|---------------------|-----------------------------------|--------------------------------------------|
| <span data-ttu-id="34831-139">نشط</span><span class="sxs-lookup"><span data-stu-id="34831-139">Active</span></span>              | <span data-ttu-id="34831-140">أمر مفتوح</span><span class="sxs-lookup"><span data-stu-id="34831-140">Open Order</span></span>                        | <span data-ttu-id="34831-141">لا شيء</span><span class="sxs-lookup"><span data-stu-id="34831-141">None</span></span>                                       |
| <span data-ttu-id="34831-142">تاريخ التأكيد</span><span class="sxs-lookup"><span data-stu-id="34831-142">Confirmed</span></span>           | <span data-ttu-id="34831-143">أمر مفتوح</span><span class="sxs-lookup"><span data-stu-id="34831-143">Open Order</span></span>                        | <span data-ttu-id="34831-144">التأكيد</span><span class="sxs-lookup"><span data-stu-id="34831-144">Confirmation</span></span>                               |
| <span data-ttu-id="34831-145">منتقي</span><span class="sxs-lookup"><span data-stu-id="34831-145">Picked</span></span>              | <span data-ttu-id="34831-146">أمر مفتوح</span><span class="sxs-lookup"><span data-stu-id="34831-146">Open Order</span></span>                        | <span data-ttu-id="34831-147">قائمة الانتقاء</span><span class="sxs-lookup"><span data-stu-id="34831-147">Picking List</span></span>                               |
| <span data-ttu-id="34831-148">تم تسليمه بشكل جزئي</span><span class="sxs-lookup"><span data-stu-id="34831-148">Partially Delivered</span></span> | <span data-ttu-id="34831-149">أمر مفتوح</span><span class="sxs-lookup"><span data-stu-id="34831-149">Open Order</span></span>                        | <span data-ttu-id="34831-150">كشف التعبئة</span><span class="sxs-lookup"><span data-stu-id="34831-150">Packing Slip</span></span>                               |
| <span data-ttu-id="34831-151">تم التسليم</span><span class="sxs-lookup"><span data-stu-id="34831-151">Delivered</span></span>           | <span data-ttu-id="34831-152">تم التسليم</span><span class="sxs-lookup"><span data-stu-id="34831-152">Delivered</span></span>                         | <span data-ttu-id="34831-153">كشف التعبئة</span><span class="sxs-lookup"><span data-stu-id="34831-153">Packing Slip</span></span>                               |
| <span data-ttu-id="34831-154">مفوتر جزئيًا</span><span class="sxs-lookup"><span data-stu-id="34831-154">Partially Invoiced</span></span>  | <span data-ttu-id="34831-155">تم التسليم</span><span class="sxs-lookup"><span data-stu-id="34831-155">Delivered</span></span>                         | <span data-ttu-id="34831-156">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="34831-156">Invoice</span></span>                                    |
| <span data-ttu-id="34831-157">مفوتر</span><span class="sxs-lookup"><span data-stu-id="34831-157">Invoiced</span></span>            | <span data-ttu-id="34831-158">مفوتر</span><span class="sxs-lookup"><span data-stu-id="34831-158">Invoiced</span></span>                          | <span data-ttu-id="34831-159">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="34831-159">Invoice</span></span>                                    |
| <span data-ttu-id="34831-160">تم الإلغاء</span><span class="sxs-lookup"><span data-stu-id="34831-160">Cancelled</span></span>           | <span data-ttu-id="34831-161">تم الإلغاء</span><span class="sxs-lookup"><span data-stu-id="34831-161">Cancelled</span></span>                         | <span data-ttu-id="34831-162">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="34831-162">Not applicable</span></span>                             |

<span data-ttu-id="34831-163">يعرض الجدول التالي تعيين **حالة المعالجة** بين Sales وSupply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="34831-163">The following table shows the mapping of **Processing Status** between Sales and Supply Chain Management.</span></span>

| <span data-ttu-id="34831-164">حالة المعالجة</span><span class="sxs-lookup"><span data-stu-id="34831-164">Processing Status</span></span>   | <span data-ttu-id="34831-165">الحالة في Sales</span><span class="sxs-lookup"><span data-stu-id="34831-165">Status in Sales</span></span> | <span data-ttu-id="34831-166">الحالة في Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="34831-166">Status in Supply Chain Management</span></span> |
|---------------------|-----------------|-----------------------------------|
| <span data-ttu-id="34831-167">نشط</span><span class="sxs-lookup"><span data-stu-id="34831-167">Active</span></span>              | <span data-ttu-id="34831-168">نشط</span><span class="sxs-lookup"><span data-stu-id="34831-168">Active</span></span>          | <span data-ttu-id="34831-169">أمر مفتوح</span><span class="sxs-lookup"><span data-stu-id="34831-169">Open Order</span></span>                        |
| <span data-ttu-id="34831-170">تاريخ التأكيد</span><span class="sxs-lookup"><span data-stu-id="34831-170">Confirmed</span></span>           | <span data-ttu-id="34831-171">‏‫مُرسل</span><span class="sxs-lookup"><span data-stu-id="34831-171">Submitted</span></span>       | <span data-ttu-id="34831-172">أمر مفتوح</span><span class="sxs-lookup"><span data-stu-id="34831-172">Open Order</span></span>                        |
| <span data-ttu-id="34831-173">منتقي</span><span class="sxs-lookup"><span data-stu-id="34831-173">Picked</span></span>              | <span data-ttu-id="34831-174">‏‫مُرسل</span><span class="sxs-lookup"><span data-stu-id="34831-174">Submitted</span></span>       | <span data-ttu-id="34831-175">أمر مفتوح</span><span class="sxs-lookup"><span data-stu-id="34831-175">Open Order</span></span>                        |
| <span data-ttu-id="34831-176">تم تسليمه بشكل جزئي</span><span class="sxs-lookup"><span data-stu-id="34831-176">Partially Delivered</span></span> | <span data-ttu-id="34831-177">نشط</span><span class="sxs-lookup"><span data-stu-id="34831-177">Active</span></span>          | <span data-ttu-id="34831-178">أمر مفتوح</span><span class="sxs-lookup"><span data-stu-id="34831-178">Open Order</span></span>                        |
| <span data-ttu-id="34831-179">مفوتر جزئيًا</span><span class="sxs-lookup"><span data-stu-id="34831-179">Partially Invoiced</span></span>  | <span data-ttu-id="34831-180">نشط</span><span class="sxs-lookup"><span data-stu-id="34831-180">Active</span></span>          | <span data-ttu-id="34831-181">أمر مفتوح</span><span class="sxs-lookup"><span data-stu-id="34831-181">Open Order</span></span>                        |
| <span data-ttu-id="34831-182">مفوتر جزئيًا</span><span class="sxs-lookup"><span data-stu-id="34831-182">Partially Invoiced</span></span>  | <span data-ttu-id="34831-183">تم الاستيفاء</span><span class="sxs-lookup"><span data-stu-id="34831-183">Fulfilled</span></span>       | <span data-ttu-id="34831-184">تم التسليم</span><span class="sxs-lookup"><span data-stu-id="34831-184">Delivered</span></span>                         |
| <span data-ttu-id="34831-185">مفوتر</span><span class="sxs-lookup"><span data-stu-id="34831-185">Invoiced</span></span>            | <span data-ttu-id="34831-186">مفوتر</span><span class="sxs-lookup"><span data-stu-id="34831-186">Invoiced</span></span>        | <span data-ttu-id="34831-187">مفوتر</span><span class="sxs-lookup"><span data-stu-id="34831-187">Invoiced</span></span>                          |
| <span data-ttu-id="34831-188">تم الإلغاء</span><span class="sxs-lookup"><span data-stu-id="34831-188">Cancelled</span></span>           | <span data-ttu-id="34831-189">تم الإلغاء</span><span class="sxs-lookup"><span data-stu-id="34831-189">Cancelled</span></span>       | <span data-ttu-id="34831-190">مُلغاة</span><span class="sxs-lookup"><span data-stu-id="34831-190">Cancelled</span></span>                         |

## <a name="setup"></a><span data-ttu-id="34831-191">الإعداد</span><span class="sxs-lookup"><span data-stu-id="34831-191">Setup</span></span>

<span data-ttu-id="34831-192">لإعداد التعيين لأعمدة حالات أمر المبيعات، يجب تمكين السمتين **IsSOPIntegrationEnabled** و **isIntegrationUser**.</span><span class="sxs-lookup"><span data-stu-id="34831-192">To set up the mapping for the sales order status columns, you must enable the **IsSOPIntegrationEnabled** and **isIntegrationUser** attributes.</span></span>

<span data-ttu-id="34831-193">لتمكين السمة **IsSOPIntegrationEnabled**‎، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="34831-193">To enable the **IsSOPIntegrationEnabled** attribute, follow these steps.</span></span>

1. <span data-ttu-id="34831-194">في المستعرض، انتقل إلى `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span><span class="sxs-lookup"><span data-stu-id="34831-194">In a browser, go to `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span></span> <span data-ttu-id="34831-195">استبدل **\<test-name\>** بارتباط شركتك إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="34831-195">Replace **\<test-name\>** with your company's link to Sales.</span></span>
2. <span data-ttu-id="34831-196">في الصفحة المفتوحة، ابحث عن **organizationid**، ودوّن القيمة.</span><span class="sxs-lookup"><span data-stu-id="34831-196">On the page that is opened, find **organizationid**, and make a note of the value.</span></span>

    ![البحث عن organizationid](media/sales-map-orgid.png)

3. <span data-ttu-id="34831-198">في Sales، افتح وحدة تحكم المستعرض، وقم بتشغيل البرنامج النصي التالي.</span><span class="sxs-lookup"><span data-stu-id="34831-198">In Sales, open the browser console, and run following script.</span></span> <span data-ttu-id="34831-199">استخدم القيمة **organizationid** من الخطوة 2.</span><span class="sxs-lookup"><span data-stu-id="34831-199">Use the **organizationid** value from step 2.</span></span>

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on row update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![التعليمات البرمجية JavaScript في وحدة تحكم المستعرض](media/sales-map-script.png)

4. <span data-ttu-id="34831-201">تأكد من تعيين **IsSOPIntegrationEnabled** إلى **صواب**.</span><span class="sxs-lookup"><span data-stu-id="34831-201">Verify that **IsSOPIntegrationEnabled** is set to **true**.</span></span> <span data-ttu-id="34831-202">استخدم عنوان URL من الخطوة 1 للتدقيق في القيمة.</span><span class="sxs-lookup"><span data-stu-id="34831-202">Use the URL from step 1 to check the value.</span></span>

    ![تعيين IsSOPIntegrationEnabled إلى صواب.](media/sales-map-integration-enabled.png)

<span data-ttu-id="34831-204">لتمكين السمة **isIntegrationUser‎**‎، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="34831-204">To enable the **isIntegrationUser** attribute, follow these steps.</span></span>

1. <span data-ttu-id="34831-205">في Sales، انتقل إلى **إعداد \> التخصيص \> تخصيص النظام**، حدد **جدول المستخدم**، ثم افتح  **النموذج \> المستخدم**.</span><span class="sxs-lookup"><span data-stu-id="34831-205">In Sales, go to **Setting \> Customization \> Customize the System**, select **User table**, and then open **Form \> User**.</span></span>

    ![فتح نموذج المستخدم](media/sales-map-user.png)

2. <span data-ttu-id="34831-207">في "مستكشف الحقول"، ابحث عن **وضع مستخدم التكامل**، ثم انقر نقرًا مزدوجًا فوقه لإضافته إلى النموذج.</span><span class="sxs-lookup"><span data-stu-id="34831-207">In Field Explorer, find **Integration user mode**, and double-click it to add it to the form.</span></span> <span data-ttu-id="34831-208">احفظ التغيير.</span><span class="sxs-lookup"><span data-stu-id="34831-208">Save your change.</span></span>

    ![إضافة عمود وضع مستخدم التكامل إلى النموذج](media/sales-map-field-explorer.png)

3. <span data-ttu-id="34831-210">في Sales، انتقل إلى **الإعداد \> الأمان \> المستخدمون**، وقم بتغيير طريقة العرض من **المستخدمون الممكّنون** إلى **مستخدمو التطبيق**.</span><span class="sxs-lookup"><span data-stu-id="34831-210">In Sales, go to **Setting \> Security \> Users**, and change the view from **Enabled Users** to **Application Users**.</span></span>

    ![تغيير طريقة العرض من "المستخدمون الممكّنون" إلى "مستخدمو التطبيق"](media/sales-map-enabled-users.png)

4. <span data-ttu-id="34831-212">حدد الإدخالين لـ **DualWrite IntegrationUser**.</span><span class="sxs-lookup"><span data-stu-id="34831-212">Select the two entries for **DualWrite IntegrationUser**.</span></span>

    ![قائمة مستخدمي التطبيق](media/sales-map-user-mode.png)

5. <span data-ttu-id="34831-214">قم بتغيير قيمة عمود **وضع مستخدم التكامل** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="34831-214">Change the value of the **Integration user mode** column to **Yes**.</span></span>

    ![تغيير قيمة عمود وضع مستخدم التكامل](media/sales-map-user-mode-yes.png)

<span data-ttu-id="34831-216">أصبحت الآن أوامر مبيعاتك معيّنة.</span><span class="sxs-lookup"><span data-stu-id="34831-216">Your sales orders are now mapped.</span></span>
