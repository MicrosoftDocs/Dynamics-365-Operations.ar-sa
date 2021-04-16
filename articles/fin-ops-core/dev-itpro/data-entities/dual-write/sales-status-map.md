---
title: إعداد التعيين أعمدة حالة أمر المبيعات
description: يوضح هذا الموضوع كيفية إعداد أعمدة حالات أمر المبيعات للكتابة المزدوجة.
author: dasani-madipalli
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 9afa64df73aa17e7a15a0ee4f4529ac74bcd3c67
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750704"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-columns"></a><span data-ttu-id="947d7-103">إعداد التعيين أعمدة حالة أمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="947d7-103">Set up the mapping for the sales order status columns</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="947d7-104">تحتوي الأعمدة التي تشير إلى حالة أمر المبيعات على قيم تعداد مختلفة في Microsoft Dynamics 365 Supply Chain Management وDynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="947d7-104">The columns that indicate sales order status have different enumeration values in Microsoft Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="947d7-105">هناك حاجة إلى إعداد إضافي لتعيين هذه الأعمدة في الكتابة المزدوجة.</span><span class="sxs-lookup"><span data-stu-id="947d7-105">Additional setup is required to map these columns in dual-write.</span></span>

## <a name="columns-in-supply-chain-management"></a><span data-ttu-id="947d7-106">الأعمدة في Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="947d7-106">columns in Supply Chain Management</span></span>

<span data-ttu-id="947d7-107">في Supply Chain Management، يعكس العمودان حالة أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="947d7-107">In Supply Chain Management, two columns reflect the status of the sales order.</span></span> <span data-ttu-id="947d7-108">العمودان اللذان يجب عليكما تعيينهما هما **الحالة** و **حالة المستند**.</span><span class="sxs-lookup"><span data-stu-id="947d7-108">The columns that you must map are **Status** and **Document Status**.</span></span>

<span data-ttu-id="947d7-109">يحدد تعداد **الحالة** الحالة الإجمالية  للأمر.</span><span class="sxs-lookup"><span data-stu-id="947d7-109">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="947d7-110">تظهر هذه الحالة على رأس الأمر.</span><span class="sxs-lookup"><span data-stu-id="947d7-110">This status is shown on the order header.</span></span>

<span data-ttu-id="947d7-111">يتضمن تعداد **الحالة** القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="947d7-111">The **Status** enumeration has the following values:</span></span>

- <span data-ttu-id="947d7-112">أمر مفتوح</span><span class="sxs-lookup"><span data-stu-id="947d7-112">Open Order</span></span>
- <span data-ttu-id="947d7-113">تم التسليم</span><span class="sxs-lookup"><span data-stu-id="947d7-113">Delivered</span></span>
- <span data-ttu-id="947d7-114">مفوتر</span><span class="sxs-lookup"><span data-stu-id="947d7-114">Invoiced</span></span>
- <span data-ttu-id="947d7-115">تم الإلغاء</span><span class="sxs-lookup"><span data-stu-id="947d7-115">Cancelled</span></span>

<span data-ttu-id="947d7-116">يحدد تعداد **حالة المستند** أحدث مستند تم إنشاؤه للأمر.</span><span class="sxs-lookup"><span data-stu-id="947d7-116">The **Document Status** enumeration specifies the most recent document that was generated for the order.</span></span> <span data-ttu-id="947d7-117">على سبيل المثال، إذا تم تأكيد الأمر، فإن هذا المستند هو تأكيد أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="947d7-117">For example, if the order is confirmed, this document is a sales order confirmation.</span></span> <span data-ttu-id="947d7-118">إذا تمت فوترة أمر المبيعات بشكل جزئي، ثم تم تأكيد البند المتبقي، تبقى حالة المستند **فاتورة**، بسبب إنشاء الفاتورة لاحقًا في العملية.</span><span class="sxs-lookup"><span data-stu-id="947d7-118">If a sales order is partially invoiced, and then the remaining line is confirmed, the document status remains **Invoice**, because the invoice is generated later in the process.</span></span>

<span data-ttu-id="947d7-119">يتضمن تعداد **حالة المستند** القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="947d7-119">The **Document Status** enumeration has the following values:</span></span>

- <span data-ttu-id="947d7-120">التأكيد</span><span class="sxs-lookup"><span data-stu-id="947d7-120">Confirmation</span></span>
- <span data-ttu-id="947d7-121">قائمة الانتقاء</span><span class="sxs-lookup"><span data-stu-id="947d7-121">Picking List</span></span>
- <span data-ttu-id="947d7-122">كشف التعبئة</span><span class="sxs-lookup"><span data-stu-id="947d7-122">Packing Slip</span></span>
- <span data-ttu-id="947d7-123">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="947d7-123">Invoice</span></span>

## <a name="columns-in-sales"></a><span data-ttu-id="947d7-124">أعمده في المبيعات</span><span class="sxs-lookup"><span data-stu-id="947d7-124">columns in Sales</span></span>

<span data-ttu-id="947d7-125">في Sales، يشير العمودان إلى حالة الأمر.</span><span class="sxs-lookup"><span data-stu-id="947d7-125">In Sales, two columns indicate the status of the order.</span></span> <span data-ttu-id="947d7-126">العمودان اللذان يجب عليكما تعيينهما هما **الحالة** و **حالة المعالجة‬**.</span><span class="sxs-lookup"><span data-stu-id="947d7-126">The columns that you must map are **Status** and **Processing Status**.</span></span>

<span data-ttu-id="947d7-127">يحدد تعداد **الحالة** الحالة الإجمالية  للأمر.</span><span class="sxs-lookup"><span data-stu-id="947d7-127">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="947d7-128">لديه القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="947d7-128">It has the following values:</span></span>

- <span data-ttu-id="947d7-129">نشط</span><span class="sxs-lookup"><span data-stu-id="947d7-129">Active</span></span>
- <span data-ttu-id="947d7-130">‏‫مُرسل</span><span class="sxs-lookup"><span data-stu-id="947d7-130">Submitted</span></span>
- <span data-ttu-id="947d7-131">تم الاستيفاء</span><span class="sxs-lookup"><span data-stu-id="947d7-131">Fulfilled</span></span>
- <span data-ttu-id="947d7-132">مفوتر</span><span class="sxs-lookup"><span data-stu-id="947d7-132">Invoiced</span></span>
- <span data-ttu-id="947d7-133">تم الإلغاء</span><span class="sxs-lookup"><span data-stu-id="947d7-133">Cancelled</span></span>

<span data-ttu-id="947d7-134">تم تقديم تعداد **حالة المعالجة** بحيث يمكن تعيين الحالة بدقة أكبر مع Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="947d7-134">The **Processing Status** enumeration was introduced so that the status can be mapped more accurately with Supply Chain Management.</span></span>

<span data-ttu-id="947d7-135">يعرض الجدول التالي تعيين **حالة المعالجة** في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="947d7-135">The following table shows the mapping of **Processing Status** in Supply Chain Management.</span></span>

| <span data-ttu-id="947d7-136">حالة المعالجة</span><span class="sxs-lookup"><span data-stu-id="947d7-136">Processing Status</span></span>   | <span data-ttu-id="947d7-137">الحالة في Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="947d7-137">Status in Supply Chain Management</span></span> | <span data-ttu-id="947d7-138">حالة المستند في Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="947d7-138">Document Status in Supply Chain Management</span></span> |
|---------------------|-----------------------------------|--------------------------------------------|
| <span data-ttu-id="947d7-139">نشط</span><span class="sxs-lookup"><span data-stu-id="947d7-139">Active</span></span>              | <span data-ttu-id="947d7-140">أمر مفتوح</span><span class="sxs-lookup"><span data-stu-id="947d7-140">Open Order</span></span>                        | <span data-ttu-id="947d7-141">لا شيء</span><span class="sxs-lookup"><span data-stu-id="947d7-141">None</span></span>                                       |
| <span data-ttu-id="947d7-142">تاريخ التأكيد</span><span class="sxs-lookup"><span data-stu-id="947d7-142">Confirmed</span></span>           | <span data-ttu-id="947d7-143">أمر مفتوح</span><span class="sxs-lookup"><span data-stu-id="947d7-143">Open Order</span></span>                        | <span data-ttu-id="947d7-144">التأكيد</span><span class="sxs-lookup"><span data-stu-id="947d7-144">Confirmation</span></span>                               |
| <span data-ttu-id="947d7-145">منتقي</span><span class="sxs-lookup"><span data-stu-id="947d7-145">Picked</span></span>              | <span data-ttu-id="947d7-146">أمر مفتوح</span><span class="sxs-lookup"><span data-stu-id="947d7-146">Open Order</span></span>                        | <span data-ttu-id="947d7-147">قائمة الانتقاء</span><span class="sxs-lookup"><span data-stu-id="947d7-147">Picking List</span></span>                               |
| <span data-ttu-id="947d7-148">تم تسليمه بشكل جزئي</span><span class="sxs-lookup"><span data-stu-id="947d7-148">Partially Delivered</span></span> | <span data-ttu-id="947d7-149">أمر مفتوح</span><span class="sxs-lookup"><span data-stu-id="947d7-149">Open Order</span></span>                        | <span data-ttu-id="947d7-150">كشف التعبئة</span><span class="sxs-lookup"><span data-stu-id="947d7-150">Packing Slip</span></span>                               |
| <span data-ttu-id="947d7-151">تم التسليم</span><span class="sxs-lookup"><span data-stu-id="947d7-151">Delivered</span></span>           | <span data-ttu-id="947d7-152">تم التسليم</span><span class="sxs-lookup"><span data-stu-id="947d7-152">Delivered</span></span>                         | <span data-ttu-id="947d7-153">كشف التعبئة</span><span class="sxs-lookup"><span data-stu-id="947d7-153">Packing Slip</span></span>                               |
| <span data-ttu-id="947d7-154">مفوتر جزئيًا</span><span class="sxs-lookup"><span data-stu-id="947d7-154">Partially Invoiced</span></span>  | <span data-ttu-id="947d7-155">تم التسليم</span><span class="sxs-lookup"><span data-stu-id="947d7-155">Delivered</span></span>                         | <span data-ttu-id="947d7-156">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="947d7-156">Invoice</span></span>                                    |
| <span data-ttu-id="947d7-157">مفوتر</span><span class="sxs-lookup"><span data-stu-id="947d7-157">Invoiced</span></span>            | <span data-ttu-id="947d7-158">مفوتر</span><span class="sxs-lookup"><span data-stu-id="947d7-158">Invoiced</span></span>                          | <span data-ttu-id="947d7-159">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="947d7-159">Invoice</span></span>                                    |
| <span data-ttu-id="947d7-160">تم الإلغاء</span><span class="sxs-lookup"><span data-stu-id="947d7-160">Cancelled</span></span>           | <span data-ttu-id="947d7-161">تم الإلغاء</span><span class="sxs-lookup"><span data-stu-id="947d7-161">Cancelled</span></span>                         | <span data-ttu-id="947d7-162">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="947d7-162">Not applicable</span></span>                             |

<span data-ttu-id="947d7-163">يعرض الجدول التالي تعيين **حالة المعالجة** بين Sales وSupply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="947d7-163">The following table shows the mapping of **Processing Status** between Sales and Supply Chain Management.</span></span>

| <span data-ttu-id="947d7-164">حالة المعالجة</span><span class="sxs-lookup"><span data-stu-id="947d7-164">Processing Status</span></span>   | <span data-ttu-id="947d7-165">الحالة في Sales</span><span class="sxs-lookup"><span data-stu-id="947d7-165">Status in Sales</span></span> | <span data-ttu-id="947d7-166">الحالة في Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="947d7-166">Status in Supply Chain Management</span></span> |
|---------------------|-----------------|-----------------------------------|
| <span data-ttu-id="947d7-167">نشط</span><span class="sxs-lookup"><span data-stu-id="947d7-167">Active</span></span>              | <span data-ttu-id="947d7-168">نشط</span><span class="sxs-lookup"><span data-stu-id="947d7-168">Active</span></span>          | <span data-ttu-id="947d7-169">أمر مفتوح</span><span class="sxs-lookup"><span data-stu-id="947d7-169">Open Order</span></span>                        |
| <span data-ttu-id="947d7-170">تاريخ التأكيد</span><span class="sxs-lookup"><span data-stu-id="947d7-170">Confirmed</span></span>           | <span data-ttu-id="947d7-171">‏‫مُرسل</span><span class="sxs-lookup"><span data-stu-id="947d7-171">Submitted</span></span>       | <span data-ttu-id="947d7-172">أمر مفتوح</span><span class="sxs-lookup"><span data-stu-id="947d7-172">Open Order</span></span>                        |
| <span data-ttu-id="947d7-173">منتقي</span><span class="sxs-lookup"><span data-stu-id="947d7-173">Picked</span></span>              | <span data-ttu-id="947d7-174">‏‫مُرسل</span><span class="sxs-lookup"><span data-stu-id="947d7-174">Submitted</span></span>       | <span data-ttu-id="947d7-175">أمر مفتوح</span><span class="sxs-lookup"><span data-stu-id="947d7-175">Open Order</span></span>                        |
| <span data-ttu-id="947d7-176">تم تسليمه بشكل جزئي</span><span class="sxs-lookup"><span data-stu-id="947d7-176">Partially Delivered</span></span> | <span data-ttu-id="947d7-177">نشط</span><span class="sxs-lookup"><span data-stu-id="947d7-177">Active</span></span>          | <span data-ttu-id="947d7-178">أمر مفتوح</span><span class="sxs-lookup"><span data-stu-id="947d7-178">Open Order</span></span>                        |
| <span data-ttu-id="947d7-179">مفوتر جزئيًا</span><span class="sxs-lookup"><span data-stu-id="947d7-179">Partially Invoiced</span></span>  | <span data-ttu-id="947d7-180">نشط</span><span class="sxs-lookup"><span data-stu-id="947d7-180">Active</span></span>          | <span data-ttu-id="947d7-181">أمر مفتوح</span><span class="sxs-lookup"><span data-stu-id="947d7-181">Open Order</span></span>                        |
| <span data-ttu-id="947d7-182">مفوتر جزئيًا</span><span class="sxs-lookup"><span data-stu-id="947d7-182">Partially Invoiced</span></span>  | <span data-ttu-id="947d7-183">تم الاستيفاء</span><span class="sxs-lookup"><span data-stu-id="947d7-183">Fulfilled</span></span>       | <span data-ttu-id="947d7-184">تم التسليم</span><span class="sxs-lookup"><span data-stu-id="947d7-184">Delivered</span></span>                         |
| <span data-ttu-id="947d7-185">مفوتر</span><span class="sxs-lookup"><span data-stu-id="947d7-185">Invoiced</span></span>            | <span data-ttu-id="947d7-186">مفوتر</span><span class="sxs-lookup"><span data-stu-id="947d7-186">Invoiced</span></span>        | <span data-ttu-id="947d7-187">مفوتر</span><span class="sxs-lookup"><span data-stu-id="947d7-187">Invoiced</span></span>                          |
| <span data-ttu-id="947d7-188">تم الإلغاء</span><span class="sxs-lookup"><span data-stu-id="947d7-188">Cancelled</span></span>           | <span data-ttu-id="947d7-189">تم الإلغاء</span><span class="sxs-lookup"><span data-stu-id="947d7-189">Cancelled</span></span>       | <span data-ttu-id="947d7-190">مُلغاة</span><span class="sxs-lookup"><span data-stu-id="947d7-190">Cancelled</span></span>                         |

## <a name="setup"></a><span data-ttu-id="947d7-191">الإعداد</span><span class="sxs-lookup"><span data-stu-id="947d7-191">Setup</span></span>

<span data-ttu-id="947d7-192">لإعداد التعيين لأعمدة حالات أمر المبيعات، يجب تمكين السمتين **IsSOPIntegrationEnabled** و **isIntegrationUser**.</span><span class="sxs-lookup"><span data-stu-id="947d7-192">To set up the mapping for the sales order status columns, you must enable the **IsSOPIntegrationEnabled** and **isIntegrationUser** attributes.</span></span>

<span data-ttu-id="947d7-193">لتمكين السمة **IsSOPIntegrationEnabled**‎، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="947d7-193">To enable the **IsSOPIntegrationEnabled** attribute, follow these steps.</span></span>

1. <span data-ttu-id="947d7-194">في المستعرض، انتقل إلى `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span><span class="sxs-lookup"><span data-stu-id="947d7-194">In a browser, go to `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span></span> <span data-ttu-id="947d7-195">استبدل **\<test-name\>** بارتباط شركتك إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="947d7-195">Replace **\<test-name\>** with your company's link to Sales.</span></span>
2. <span data-ttu-id="947d7-196">في الصفحة المفتوحة، ابحث عن **organizationid**، ودوّن القيمة.</span><span class="sxs-lookup"><span data-stu-id="947d7-196">On the page that is opened, find **organizationid**, and make a note of the value.</span></span>

    ![البحث عن organizationid](media/sales-map-orgid.png)

3. <span data-ttu-id="947d7-198">في Sales، افتح وحدة تحكم المستعرض، وقم بتشغيل البرنامج النصي التالي.</span><span class="sxs-lookup"><span data-stu-id="947d7-198">In Sales, open the browser console, and run following script.</span></span> <span data-ttu-id="947d7-199">استخدم القيمة **organizationid** من الخطوة 2.</span><span class="sxs-lookup"><span data-stu-id="947d7-199">Use the **organizationid** value from step 2.</span></span>

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

4. <span data-ttu-id="947d7-201">تأكد من تعيين **IsSOPIntegrationEnabled** إلى **صواب**.</span><span class="sxs-lookup"><span data-stu-id="947d7-201">Verify that **IsSOPIntegrationEnabled** is set to **true**.</span></span> <span data-ttu-id="947d7-202">استخدم عنوان URL من الخطوة 1 للتدقيق في القيمة.</span><span class="sxs-lookup"><span data-stu-id="947d7-202">Use the URL from step 1 to check the value.</span></span>

    ![تعيين IsSOPIntegrationEnabled إلى صواب.](media/sales-map-integration-enabled.png)

<span data-ttu-id="947d7-204">لتمكين السمة **isIntegrationUser‎**‎، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="947d7-204">To enable the **isIntegrationUser** attribute, follow these steps.</span></span>

1. <span data-ttu-id="947d7-205">في Sales، انتقل إلى **إعداد \> التخصيص \> تخصيص النظام**، حدد **جدول المستخدم**، ثم افتح  **النموذج \> المستخدم**.</span><span class="sxs-lookup"><span data-stu-id="947d7-205">In Sales, go to **Setting \> Customization \> Customize the System**, select **User table**, and then open **Form \> User**.</span></span>

    ![فتح نموذج المستخدم](media/sales-map-user.png)

2. <span data-ttu-id="947d7-207">في "مستكشف الحقول"، ابحث عن **وضع مستخدم التكامل**، ثم انقر نقرًا مزدوجًا فوقه لإضافته إلى النموذج.</span><span class="sxs-lookup"><span data-stu-id="947d7-207">In Field Explorer, find **Integration user mode**, and double-click it to add it to the form.</span></span> <span data-ttu-id="947d7-208">احفظ التغيير.</span><span class="sxs-lookup"><span data-stu-id="947d7-208">Save your change.</span></span>

    ![إضافة عمود وضع مستخدم التكامل إلى النموذج](media/sales-map-field-explorer.png)

3. <span data-ttu-id="947d7-210">في Sales، انتقل إلى **الإعداد \> الأمان \> المستخدمون**، وقم بتغيير طريقة العرض من **المستخدمون الممكّنون** إلى **مستخدمو التطبيق**.</span><span class="sxs-lookup"><span data-stu-id="947d7-210">In Sales, go to **Setting \> Security \> Users**, and change the view from **Enabled Users** to **Application Users**.</span></span>

    ![تغيير طريقة العرض من "المستخدمون الممكّنون" إلى "مستخدمو التطبيق"](media/sales-map-enabled-users.png)

4. <span data-ttu-id="947d7-212">حدد الإدخالين لـ **DualWrite IntegrationUser**.</span><span class="sxs-lookup"><span data-stu-id="947d7-212">Select the two entries for **DualWrite IntegrationUser**.</span></span>

    ![قائمة مستخدمي التطبيق](media/sales-map-user-mode.png)

5. <span data-ttu-id="947d7-214">قم بتغيير قيمة عمود **وضع مستخدم التكامل** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="947d7-214">Change the value of the **Integration user mode** column to **Yes**.</span></span>

    ![تغيير قيمة عمود وضع مستخدم التكامل](media/sales-map-user-mode-yes.png)

<span data-ttu-id="947d7-216">أصبحت الآن أوامر مبيعاتك معيّنة.</span><span class="sxs-lookup"><span data-stu-id="947d7-216">Your sales orders are now mapped.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]