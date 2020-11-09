---
title: إعداد التعيين  لحقول حالات أمر المبيعات
description: يوضح هذا الموضوع كيفية إعداد حقول حالات أمر المبيعات للكتابة المزدوجة.
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
ms.openlocfilehash: 5855581100606003c1faf6b88a0ab234ae378893
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997664"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-fields"></a><span data-ttu-id="0f640-103">إعداد التعيين  لحقول حالات أمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="0f640-103">Set up the mapping for the sales order status fields</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0f640-104">تحتوي الحقول التي تشير إلى حالة أمر المبيعات على قيم تعداد مختلفة في Microsoft Dynamics 365 Supply Chain Management وDynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="0f640-104">The fields that indicate sales order status have different enumeration values in Microsoft Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="0f640-105">هناك حاجة إلى إعداد إضافي لتعيين هذه الحقول في الكتابة المزدوجة.</span><span class="sxs-lookup"><span data-stu-id="0f640-105">Additional setup is required to map these fields in dual-write.</span></span>

## <a name="fields-in-supply-chain-management"></a><span data-ttu-id="0f640-106">الحقول في Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="0f640-106">Fields in Supply Chain Management</span></span>

<span data-ttu-id="0f640-107">في Supply Chain Management، يعكس حقلان حالة أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="0f640-107">In Supply Chain Management, two fields reflect the status of the sales order.</span></span> <span data-ttu-id="0f640-108">الحقلان اللذان يجب عليكما تعيينهما هما **الحالة** و **حالة المستند**.</span><span class="sxs-lookup"><span data-stu-id="0f640-108">The fields that you must map are **Status** and **Document Status**.</span></span>

<span data-ttu-id="0f640-109">يحدد تعداد **الحالة** الحالة الإجمالية  للأمر.</span><span class="sxs-lookup"><span data-stu-id="0f640-109">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="0f640-110">تظهر هذه الحالة على رأس الأمر.</span><span class="sxs-lookup"><span data-stu-id="0f640-110">This status is shown on the order header.</span></span>

<span data-ttu-id="0f640-111">يتضمن تعداد **الحالة** القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="0f640-111">The **Status** enumeration has the following values:</span></span>

- <span data-ttu-id="0f640-112">أمر مفتوح</span><span class="sxs-lookup"><span data-stu-id="0f640-112">Open Order</span></span>
- <span data-ttu-id="0f640-113">تم التسليم</span><span class="sxs-lookup"><span data-stu-id="0f640-113">Delivered</span></span>
- <span data-ttu-id="0f640-114">مفوتر</span><span class="sxs-lookup"><span data-stu-id="0f640-114">Invoiced</span></span>
- <span data-ttu-id="0f640-115">تم الإلغاء</span><span class="sxs-lookup"><span data-stu-id="0f640-115">Cancelled</span></span>

<span data-ttu-id="0f640-116">يحدد تعداد **حالة المستند** أحدث مستند تم إنشاؤه للأمر.</span><span class="sxs-lookup"><span data-stu-id="0f640-116">The **Document Status** enumeration specifies the most recent document that was generated for the order.</span></span> <span data-ttu-id="0f640-117">على سبيل المثال، إذا تم تأكيد الأمر، فإن هذا المستند هو تأكيد أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="0f640-117">For example, if the order is confirmed, this document is a sales order confirmation.</span></span> <span data-ttu-id="0f640-118">إذا تمت فوترة أمر المبيعات بشكل جزئي، ثم تم تأكيد البند المتبقي، تبقى حالة المستند **فاتورة** ، بسبب إنشاء الفاتورة لاحقًا في العملية.</span><span class="sxs-lookup"><span data-stu-id="0f640-118">If a sales order is partially invoiced, and then the remaining line is confirmed, the document status remains **Invoice** , because the invoice is generated later in the process.</span></span>

<span data-ttu-id="0f640-119">يتضمن تعداد **حالة المستند** القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="0f640-119">The **Document Status** enumeration has the following values:</span></span>

- <span data-ttu-id="0f640-120">التأكيد</span><span class="sxs-lookup"><span data-stu-id="0f640-120">Confirmation</span></span>
- <span data-ttu-id="0f640-121">قائمة الانتقاء</span><span class="sxs-lookup"><span data-stu-id="0f640-121">Picking List</span></span>
- <span data-ttu-id="0f640-122">كشف التعبئة</span><span class="sxs-lookup"><span data-stu-id="0f640-122">Packing Slip</span></span>
- <span data-ttu-id="0f640-123">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="0f640-123">Invoice</span></span>

## <a name="fields-in-sales"></a><span data-ttu-id="0f640-124">الحقول في Sales</span><span class="sxs-lookup"><span data-stu-id="0f640-124">Fields in Sales</span></span>

<span data-ttu-id="0f640-125">في Sales، يشير حقلان إلى حالة الأمر.</span><span class="sxs-lookup"><span data-stu-id="0f640-125">In Sales, two fields indicate the status of the order.</span></span> <span data-ttu-id="0f640-126">الحقلان اللذان يجب عليكما تعيينهما هما **الحالة** و **حالة المعالجة‬**.</span><span class="sxs-lookup"><span data-stu-id="0f640-126">The fields that you must map are **Status** and **Processing Status**.</span></span>

<span data-ttu-id="0f640-127">يحدد تعداد **الحالة** الحالة الإجمالية  للأمر.</span><span class="sxs-lookup"><span data-stu-id="0f640-127">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="0f640-128">لديه القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="0f640-128">It has the following values:</span></span>

- <span data-ttu-id="0f640-129">نشط</span><span class="sxs-lookup"><span data-stu-id="0f640-129">Active</span></span>
- <span data-ttu-id="0f640-130">‏‫مُرسل</span><span class="sxs-lookup"><span data-stu-id="0f640-130">Submitted</span></span>
- <span data-ttu-id="0f640-131">تم الاستيفاء</span><span class="sxs-lookup"><span data-stu-id="0f640-131">Fulfilled</span></span>
- <span data-ttu-id="0f640-132">مفوتر</span><span class="sxs-lookup"><span data-stu-id="0f640-132">Invoiced</span></span>
- <span data-ttu-id="0f640-133">تم الإلغاء</span><span class="sxs-lookup"><span data-stu-id="0f640-133">Cancelled</span></span>

<span data-ttu-id="0f640-134">تم تقديم تعداد **حالة المعالجة** بحيث يمكن تعيين الحالة بدقة أكبر مع Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0f640-134">The **Processing Status** enumeration was introduced so that the status can be mapped more accurately with Supply Chain Management.</span></span>

<span data-ttu-id="0f640-135">يعرض الجدول التالي تعيين **حالة المعالجة** في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0f640-135">The following table shows the mapping of **Processing Status** in Supply Chain Management.</span></span>

| <span data-ttu-id="0f640-136">حالة المعالجة</span><span class="sxs-lookup"><span data-stu-id="0f640-136">Processing Status</span></span>   | <span data-ttu-id="0f640-137">الحالة في Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="0f640-137">Status in Supply Chain Management</span></span> | <span data-ttu-id="0f640-138">حالة المستند في Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="0f640-138">Document Status in Supply Chain Management</span></span> |
|---------------------|-----------------------------------|--------------------------------------------|
| <span data-ttu-id="0f640-139">نشط</span><span class="sxs-lookup"><span data-stu-id="0f640-139">Active</span></span>              | <span data-ttu-id="0f640-140">أمر مفتوح</span><span class="sxs-lookup"><span data-stu-id="0f640-140">Open Order</span></span>                        | <span data-ttu-id="0f640-141">لا شيء</span><span class="sxs-lookup"><span data-stu-id="0f640-141">None</span></span>                                       |
| <span data-ttu-id="0f640-142">تاريخ التأكيد</span><span class="sxs-lookup"><span data-stu-id="0f640-142">Confirmed</span></span>           | <span data-ttu-id="0f640-143">أمر مفتوح</span><span class="sxs-lookup"><span data-stu-id="0f640-143">Open Order</span></span>                        | <span data-ttu-id="0f640-144">التأكيد</span><span class="sxs-lookup"><span data-stu-id="0f640-144">Confirmation</span></span>                               |
| <span data-ttu-id="0f640-145">منتقي</span><span class="sxs-lookup"><span data-stu-id="0f640-145">Picked</span></span>              | <span data-ttu-id="0f640-146">أمر مفتوح</span><span class="sxs-lookup"><span data-stu-id="0f640-146">Open Order</span></span>                        | <span data-ttu-id="0f640-147">قائمة الانتقاء</span><span class="sxs-lookup"><span data-stu-id="0f640-147">Picking List</span></span>                               |
| <span data-ttu-id="0f640-148">تم تسليمه بشكل جزئي</span><span class="sxs-lookup"><span data-stu-id="0f640-148">Partially Delivered</span></span> | <span data-ttu-id="0f640-149">أمر مفتوح</span><span class="sxs-lookup"><span data-stu-id="0f640-149">Open Order</span></span>                        | <span data-ttu-id="0f640-150">كشف التعبئة</span><span class="sxs-lookup"><span data-stu-id="0f640-150">Packing Slip</span></span>                               |
| <span data-ttu-id="0f640-151">تم التسليم</span><span class="sxs-lookup"><span data-stu-id="0f640-151">Delivered</span></span>           | <span data-ttu-id="0f640-152">تم التسليم</span><span class="sxs-lookup"><span data-stu-id="0f640-152">Delivered</span></span>                         | <span data-ttu-id="0f640-153">كشف التعبئة</span><span class="sxs-lookup"><span data-stu-id="0f640-153">Packing Slip</span></span>                               |
| <span data-ttu-id="0f640-154">مفوتر جزئيًا</span><span class="sxs-lookup"><span data-stu-id="0f640-154">Partially Invoiced</span></span>  | <span data-ttu-id="0f640-155">تم التسليم</span><span class="sxs-lookup"><span data-stu-id="0f640-155">Delivered</span></span>                         | <span data-ttu-id="0f640-156">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="0f640-156">Invoice</span></span>                                    |
| <span data-ttu-id="0f640-157">مفوتر</span><span class="sxs-lookup"><span data-stu-id="0f640-157">Invoiced</span></span>            | <span data-ttu-id="0f640-158">مفوتر</span><span class="sxs-lookup"><span data-stu-id="0f640-158">Invoiced</span></span>                          | <span data-ttu-id="0f640-159">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="0f640-159">Invoice</span></span>                                    |
| <span data-ttu-id="0f640-160">تم الإلغاء</span><span class="sxs-lookup"><span data-stu-id="0f640-160">Cancelled</span></span>           | <span data-ttu-id="0f640-161">تم الإلغاء</span><span class="sxs-lookup"><span data-stu-id="0f640-161">Cancelled</span></span>                         | <span data-ttu-id="0f640-162">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="0f640-162">Not applicable</span></span>                             |

<span data-ttu-id="0f640-163">يعرض الجدول التالي تعيين **حالة المعالجة** بين Sales وSupply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0f640-163">The following table shows the mapping of **Processing Status** between Sales and Supply Chain Management.</span></span>

| <span data-ttu-id="0f640-164">حالة المعالجة</span><span class="sxs-lookup"><span data-stu-id="0f640-164">Processing Status</span></span>   | <span data-ttu-id="0f640-165">الحالة في Sales</span><span class="sxs-lookup"><span data-stu-id="0f640-165">Status in Sales</span></span> | <span data-ttu-id="0f640-166">الحالة في Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="0f640-166">Status in Supply Chain Management</span></span> |
|---------------------|-----------------|-----------------------------------|
| <span data-ttu-id="0f640-167">نشط</span><span class="sxs-lookup"><span data-stu-id="0f640-167">Active</span></span>              | <span data-ttu-id="0f640-168">نشط</span><span class="sxs-lookup"><span data-stu-id="0f640-168">Active</span></span>          | <span data-ttu-id="0f640-169">أمر مفتوح</span><span class="sxs-lookup"><span data-stu-id="0f640-169">Open Order</span></span>                        |
| <span data-ttu-id="0f640-170">تاريخ التأكيد</span><span class="sxs-lookup"><span data-stu-id="0f640-170">Confirmed</span></span>           | <span data-ttu-id="0f640-171">‏‫مُرسل</span><span class="sxs-lookup"><span data-stu-id="0f640-171">Submitted</span></span>       | <span data-ttu-id="0f640-172">أمر مفتوح</span><span class="sxs-lookup"><span data-stu-id="0f640-172">Open Order</span></span>                        |
| <span data-ttu-id="0f640-173">منتقي</span><span class="sxs-lookup"><span data-stu-id="0f640-173">Picked</span></span>              | <span data-ttu-id="0f640-174">‏‫مُرسل</span><span class="sxs-lookup"><span data-stu-id="0f640-174">Submitted</span></span>       | <span data-ttu-id="0f640-175">أمر مفتوح</span><span class="sxs-lookup"><span data-stu-id="0f640-175">Open Order</span></span>                        |
| <span data-ttu-id="0f640-176">تم تسليمه بشكل جزئي</span><span class="sxs-lookup"><span data-stu-id="0f640-176">Partially Delivered</span></span> | <span data-ttu-id="0f640-177">نشط</span><span class="sxs-lookup"><span data-stu-id="0f640-177">Active</span></span>          | <span data-ttu-id="0f640-178">أمر مفتوح</span><span class="sxs-lookup"><span data-stu-id="0f640-178">Open Order</span></span>                        |
| <span data-ttu-id="0f640-179">مفوتر جزئيًا</span><span class="sxs-lookup"><span data-stu-id="0f640-179">Partially Invoiced</span></span>  | <span data-ttu-id="0f640-180">نشط</span><span class="sxs-lookup"><span data-stu-id="0f640-180">Active</span></span>          | <span data-ttu-id="0f640-181">أمر مفتوح</span><span class="sxs-lookup"><span data-stu-id="0f640-181">Open Order</span></span>                        |
| <span data-ttu-id="0f640-182">مفوتر جزئيًا</span><span class="sxs-lookup"><span data-stu-id="0f640-182">Partially Invoiced</span></span>  | <span data-ttu-id="0f640-183">تم الاستيفاء</span><span class="sxs-lookup"><span data-stu-id="0f640-183">Fulfilled</span></span>       | <span data-ttu-id="0f640-184">تم التسليم</span><span class="sxs-lookup"><span data-stu-id="0f640-184">Delivered</span></span>                         |
| <span data-ttu-id="0f640-185">مفوتر</span><span class="sxs-lookup"><span data-stu-id="0f640-185">Invoiced</span></span>            | <span data-ttu-id="0f640-186">مفوتر</span><span class="sxs-lookup"><span data-stu-id="0f640-186">Invoiced</span></span>        | <span data-ttu-id="0f640-187">مفوتر</span><span class="sxs-lookup"><span data-stu-id="0f640-187">Invoiced</span></span>                          |
| <span data-ttu-id="0f640-188">تم الإلغاء</span><span class="sxs-lookup"><span data-stu-id="0f640-188">Cancelled</span></span>           | <span data-ttu-id="0f640-189">تم الإلغاء</span><span class="sxs-lookup"><span data-stu-id="0f640-189">Cancelled</span></span>       | <span data-ttu-id="0f640-190">تم الإلغاء</span><span class="sxs-lookup"><span data-stu-id="0f640-190">Cancelled</span></span>                         |

## <a name="setup"></a><span data-ttu-id="0f640-191">الإعداد</span><span class="sxs-lookup"><span data-stu-id="0f640-191">Setup</span></span>

<span data-ttu-id="0f640-192">لإعداد التعيين لحقول حالات أمر المبيعات، يجب تمكين السمتين **IsSOPIntegrationEnabled** و **isIntegrationUser**.</span><span class="sxs-lookup"><span data-stu-id="0f640-192">To set up the mapping for the sales order status fields, you must enable the **IsSOPIntegrationEnabled** and **isIntegrationUser** attributes.</span></span>

<span data-ttu-id="0f640-193">لتمكين السمة **IsSOPIntegrationEnabled** ‎، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="0f640-193">To enable the **IsSOPIntegrationEnabled** attribute, follow these steps.</span></span>

1. <span data-ttu-id="0f640-194">في المستعرض، انتقل إلى `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span><span class="sxs-lookup"><span data-stu-id="0f640-194">In a browser, go to `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span></span> <span data-ttu-id="0f640-195">استبدل **\<test-name\>** بارتباط شركتك إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="0f640-195">Replace **\<test-name\>** with your company's link to Sales.</span></span>
2. <span data-ttu-id="0f640-196">في الصفحة المفتوحة، ابحث عن **organizationid** ، ودوّن القيمة.</span><span class="sxs-lookup"><span data-stu-id="0f640-196">On the page that is opened, find **organizationid** , and make a note of the value.</span></span>

    ![البحث عن organizationid](media/sales-map-orgid.png)

3. <span data-ttu-id="0f640-198">في Sales، افتح وحدة تحكم المستعرض، وقم بتشغيل البرنامج النصي التالي.</span><span class="sxs-lookup"><span data-stu-id="0f640-198">In Sales, open the browser console, and run following script.</span></span> <span data-ttu-id="0f640-199">استخدم القيمة **organizationid** من الخطوة 2.</span><span class="sxs-lookup"><span data-stu-id="0f640-199">Use the **organizationid** value from step 2.</span></span>

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on record update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![التعليمات البرمجية JavaScript في وحدة تحكم المستعرض](media/sales-map-script.png)

4. <span data-ttu-id="0f640-201">تأكد من تعيين **IsSOPIntegrationEnabled** إلى **صواب**.</span><span class="sxs-lookup"><span data-stu-id="0f640-201">Verify that **IsSOPIntegrationEnabled** is set to **true**.</span></span> <span data-ttu-id="0f640-202">استخدم عنوان URL من الخطوة 1 للتدقيق في القيمة.</span><span class="sxs-lookup"><span data-stu-id="0f640-202">Use the URL from step 1 to check the value.</span></span>

    ![تعيين IsSOPIntegrationEnabled إلى صواب.](media/sales-map-integration-enabled.png)

<span data-ttu-id="0f640-204">لتمكين السمة **isIntegrationUser‎** ‎، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="0f640-204">To enable the **isIntegrationUser** attribute, follow these steps.</span></span>

1. <span data-ttu-id="0f640-205">في Sales، انتقل إلى **إعداد \> التخصيص \> تخصيص النظام** ، حدد **كيان المستخدم** ، ثم افتح  **النموذج \> المستخدم**.</span><span class="sxs-lookup"><span data-stu-id="0f640-205">In Sales, go to **Setting \> Customization \> Customize the System** , select **User entity** , and then open **Form \> User**.</span></span>

    ![فتح نموذج المستخدم](media/sales-map-user.png)

2. <span data-ttu-id="0f640-207">في "مستكشف الحقول"، ابحث عن **وضع مستخدم التكامل** ، ثم انقر نقرًا مزدوجًا فوقه لإضافته إلى النموذج.</span><span class="sxs-lookup"><span data-stu-id="0f640-207">In Field Explorer, find **Integration user mode** , and double-click it to add it to the form.</span></span> <span data-ttu-id="0f640-208">احفظ التغيير.</span><span class="sxs-lookup"><span data-stu-id="0f640-208">Save your change.</span></span>

    ![إضافة حقل وضع مستخدم التكامل إلى النموذج](media/sales-map-field-explorer.png)

3. <span data-ttu-id="0f640-210">في Sales، انتقل إلى **الإعداد \> الأمان \> المستخدمون** ، وقم بتغيير طريقة العرض من **المستخدمون الممكّنون** إلى **مستخدمو التطبيق**.</span><span class="sxs-lookup"><span data-stu-id="0f640-210">In Sales, go to **Setting \> Security \> Users** , and change the view from **Enabled Users** to **Application Users**.</span></span>

    ![تغيير طريقة العرض من "المستخدمون الممكّنون" إلى "مستخدمو التطبيق"](media/sales-map-enabled-users.png)

4. <span data-ttu-id="0f640-212">حدد الإدخالين لـ **DualWrite IntegrationUser**.</span><span class="sxs-lookup"><span data-stu-id="0f640-212">Select the two entries for **DualWrite IntegrationUser**.</span></span>

    ![قائمة مستخدمي التطبيق](media/sales-map-user-mode.png)

5. <span data-ttu-id="0f640-214">قم بتغيير قيمة **وضع مستخدم التكامل** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="0f640-214">Change the value of the **Integration user mode** field to **Yes**.</span></span>

    ![تغيير قيمة وضع مستخدم التكامل](media/sales-map-user-mode-yes.png)

<span data-ttu-id="0f640-216">أصبحت الآن أوامر مبيعاتك معيّنة.</span><span class="sxs-lookup"><span data-stu-id="0f640-216">Your sales orders are now mapped.</span></span>
