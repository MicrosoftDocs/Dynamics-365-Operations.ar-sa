---
title: "مزامنة رؤوس وبنود عروض أسعار المبيعات من Sales إلى Finance and Operations"
description: "يناقش الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة رؤوس وبنود عروض أسعار المبيعات من Microsoft Dynamics 365 for Sales إلى Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: d34c808bce5b61b528f50224e3a72590476d8e55
ms.contentlocale: ar-sa
ms.lasthandoff: 01/17/2018

---

# <a name="synchronize-sales-quotation-headers-and-lines-from-sales-to-finance-and-operations"></a><span data-ttu-id="58527-103">مزامنة رؤوس وبنود عروض أسعار المبيعات من Sales إلى Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="58527-103">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="58527-104">قبل أن تتمكن من استخدام حل العميل المتوقع إلى النقدية، يجب عليك الاطلاع على [تكامل بيانات Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="58527-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="58527-105">يناقش الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة رؤوس وبنود عروض أسعار المبيعات من Microsoft Dynamics 365 for Sales (Sales) إلى Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="58527-105">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span> 

## <a name="template-and-tasks"></a><span data-ttu-id="58527-106">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="58527-106">Template and tasks</span></span>

<span data-ttu-id="58527-107">يتم استخدام القوالب والمهام الأساسية التالية لمزامنة رؤوس وبنود عروض أسعار المبيعات من Sales إلى Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="58527-107">The following templates and underlying tasks are used to synchronize sales quotation headers and lines from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="58527-108">**اسم القالب:** عروض أسعار المبيعات (Sales إلى Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="58527-108">**Name of the template:** Sales Quotes (Sales to Fin and Ops)</span></span>
- <span data-ttu-id="58527-109">**أسماء المهام في المشروع:**</span><span class="sxs-lookup"><span data-stu-id="58527-109">**Names of the tasks in the project:**</span></span>

    - <span data-ttu-id="58527-110">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="58527-110">QuoteHeader</span></span>
    - <span data-ttu-id="58527-111">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="58527-111">QuoteLine</span></span>

<span data-ttu-id="58527-112">يجب تنفيذ مهام المزامنة التالية قبل حدوث مزامنة رؤوس وبنود عروض أسعار المبيعات.</span><span class="sxs-lookup"><span data-stu-id="58527-112">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="58527-113">المنتجات (Fin and Ops إلى Sales)</span><span class="sxs-lookup"><span data-stu-id="58527-113">Products (Fin and Ops to Sales)</span></span>
- <span data-ttu-id="58527-114">الحسابات (Sales إلى Fin and Ops) (في حال استخدامها)</span><span class="sxs-lookup"><span data-stu-id="58527-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
- <span data-ttu-id="58527-115">جهات الاتصال إلى العملاء (Sales إلى Fin and Ops) (في حال استخدامها)</span><span class="sxs-lookup"><span data-stu-id="58527-115">Contacts to Customers (Sales to Fin and Ops) (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="58527-116">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="58527-116">Entity set</span></span>

| <span data-ttu-id="58527-117">مبيعات</span><span class="sxs-lookup"><span data-stu-id="58527-117">Sales</span></span>        | <span data-ttu-id="58527-118">CDS</span><span class="sxs-lookup"><span data-stu-id="58527-118">CDS</span></span>           | <span data-ttu-id="58527-119">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="58527-119">Finance and Operations</span></span>    |
|--------------|---------------|---------------------------|
| <span data-ttu-id="58527-120">الاقتباسات</span><span class="sxs-lookup"><span data-stu-id="58527-120">Quotes</span></span>       | <span data-ttu-id="58527-121">عرض الأسعار</span><span class="sxs-lookup"><span data-stu-id="58527-121">Quotation</span></span>     | <span data-ttu-id="58527-122">رؤوس عروض أسعار المبيعات</span><span class="sxs-lookup"><span data-stu-id="58527-122">Sales quotation headers</span></span>   |
| <span data-ttu-id="58527-123">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="58527-123">QuoteDetails</span></span> | <span data-ttu-id="58527-124">QuotationLine</span><span class="sxs-lookup"><span data-stu-id="58527-124">QuotationLine</span></span> | <span data-ttu-id="58527-125">بنود عروض أسعار مبيعات CDS</span><span class="sxs-lookup"><span data-stu-id="58527-125">CDS sales quotation lines</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="58527-126">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="58527-126">Entity flow</span></span>

<span data-ttu-id="58527-127">يتم إنشاء عروض أسعار المبيعات في Sales وتتم مزامنتها إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="58527-127">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="58527-128">تتم مزامنة عروض أسعار المبيعات من Sales فقط إذا تحققت الشروط التالية:</span><span class="sxs-lookup"><span data-stu-id="58527-128">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="58527-129">تتم المحافظة على كافة المنتجات الموجودة في بنود عروض أسعار المبيعات خارجيًا.</span><span class="sxs-lookup"><span data-stu-id="58527-129">All products on the sales quotation lines are externally maintained.</span></span>
- <span data-ttu-id="58527-130">عرض أسعار المبيعات نشط أو تم تنشيطه.</span><span class="sxs-lookup"><span data-stu-id="58527-130">The sales quotation is active or activated.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="58527-131">حل العميل المتوقع إلى النقدية في Sales</span><span class="sxs-lookup"><span data-stu-id="58527-131">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="58527-132">تمت إضافة الحقل **لديه منتجات تتم المحافظة عليها خارجيًا فقط** إلى كيان عروض الأسعار للتحقق بشكل مستمر مما إذا كان عرض أسعار المبيعات يتكوّن بكامله من منتجات تتم المحافظة عليها خارجيًا.</span><span class="sxs-lookup"><span data-stu-id="58527-132">The **Has Externally Maintained Products Only** field has been added to the Quote entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="58527-133">إذا كان لعرض الأسعار منتجات تتم المحافظة عليها خارجيًا فقط، فستتم المحافظة على المنتجات في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="58527-133">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="58527-134">يساعد هذا السلوك على ضمان عدم محاولتك مزامنة بنود عروض أسعار المبيعات مع منتجات غير معروفة بالنسبة إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="58527-134">This behavior helps guarantee that you don't try to synchronize sales quotation lines with products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="58527-135">يتم تحديث كافة المنتجات والبنود في عرض الأسعار بواسطة معلومات **لديه منتجات تتم المحافظة عليها خارجيًا فقط** من رأس عرض الأسعار.</span><span class="sxs-lookup"><span data-stu-id="58527-135">All products and lines on the quotation are updated with the **Has Externally Maintained Products Only** information from the quotation header.</span></span> <span data-ttu-id="58527-136">يمكن العثور على هذه المعلومات في حقل **لدى عرض الأسعار منتجات تتم المحافظة عليها خارجيًا فقط** في كيان بنود عرض الأسعار.</span><span class="sxs-lookup"><span data-stu-id="58527-136">This information can be found in the **Quote Has Externally Maintained Products Only** field on the Quote line entity.</span></span>

<span data-ttu-id="58527-137">تخضع حقول **الخصم** و**التكاليف** و**الضريبة** لمراقبة إعداد معقد في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="58527-137">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="58527-138">لا يعتمد هذا الإعداد حاليًا تعيين التكامل.</span><span class="sxs-lookup"><span data-stu-id="58527-138">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="58527-139">في التصميم الحالي، تخضع حقول **السعر** و**الخصم** و**التكاليف**، و**الضريبة** لتطبيق Finance and Operations الذي يتولى إدارتها.</span><span class="sxs-lookup"><span data-stu-id="58527-139">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are mastered and handled by Finance and Operations.</span></span>

<span data-ttu-id="58527-140">في Sales، يجعل الحل الحقول التالية للقراءة فقط، نظرًا لعدم مزامنة القيم إلى Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="58527-140">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="58527-141">**حقول للقراءة فقط في رأس عرض أسعار المبيعات:** ‏‫% الخصم‬، الخصم، مبلغ الشحن</span><span class="sxs-lookup"><span data-stu-id="58527-141">**Read-only fields on the sales quotation header:** Discount %, Discount, Freight Amount</span></span>
- <span data-ttu-id="58527-142">**حقول للقراءة فقط في بنود عرض أسعار المبيعات:** الضريبة</span><span class="sxs-lookup"><span data-stu-id="58527-142">**Read-only fields on sales quotation lines:** Tax</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="58527-143">الشروط المسبقة وإعداد التعيين</span><span class="sxs-lookup"><span data-stu-id="58527-143">Preconditions and mapping setup</span></span>

<span data-ttu-id="58527-144">قبل إجراء مزامنة لأوامر المبيعات، لا بد من تحديث الأنظمة بالإعداد التالي:</span><span class="sxs-lookup"><span data-stu-id="58527-144">Before synchronizing sales orders, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="58527-145">الإعداد في Sales</span><span class="sxs-lookup"><span data-stu-id="58527-145">Setup in Sales</span></span>

- <span data-ttu-id="58527-146">انتقل إلى **الإعدادات** &gt; **الإدارة** &gt; **إعدادات النظام** &gt; **Sales**، وتأكد من تعيين حقل **أسلوب حساب الخصم** إلى **لكل وحدة**.</span><span class="sxs-lookup"><span data-stu-id="58527-146">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the **Discount calculation method** field is set to **Per unit**.</span></span> <span data-ttu-id="58527-147">يساعد هذا الإعداد على ضمان مطابقة خصم البند من Sales مع الإعداد في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="58527-147">This setting helps guarantee that the line item discount from Sales matches the setting in Finance and Operations.</span></span> <span data-ttu-id="58527-148">وإلا، فلن يكون الخصم صحيحًا في Finance and Operations، لأن Finance and Operations سيقرأ الخصم على شكل خصم لكل وحدة حتى لو كان عبارة عن خصم لكل بند في Sales.</span><span class="sxs-lookup"><span data-stu-id="58527-148">Otherwise, the discount won't be correct in Finance and Operations, because Finance and Operations will read the discount as a per-unit discount even if it was a per-line discount in Sales.</span></span>

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="58527-149">الإعداد في Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="58527-149">Setup in Finance and Operations</span></span>

- <span data-ttu-id="58527-150">انتقل إلى **الحسابات المدينة** &gt; **الإعداد** &gt; **محددات الحسابات المدينة**.</span><span class="sxs-lookup"><span data-stu-id="58527-150">Go to **Accounts receivable** &gt; **Setup** &gt; **Account receivable parameters**.</span></span> <span data-ttu-id="58527-151">على علامة التبويب **التسلسل الرقمي**، حدد التسلسل الرقمي لعروض أسعار المبيعات، ثم انقر فوق **عرض التفاصيل**.</span><span class="sxs-lookup"><span data-stu-id="58527-151">On the **Number sequence** tab, select the number sequence for sales quotations, and then click **View details**.</span></span> <span data-ttu-id="58527-152">ثم، ضمن **الإعداد العام‬**، قم بتعيين الحقل **يدوي** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="58527-152">Then, under **General Setup**, set the **Manual** field to **Yes**.</span></span>
- <span data-ttu-id="58527-153">انتقل إلى **الحسابات المدينة** &gt; **الإعداد** &gt; **محددات الحسابات المدينة**.</span><span class="sxs-lookup"><span data-stu-id="58527-153">Go to **Accounts receivable** &gt; **Setup** &gt; **Accounts receivable parameters**.</span></span> <span data-ttu-id="58527-154">ثم، على علامة تبويب **الشحنات**، قم بتعيين حقل **التحكم في تاريخ التسليم** إلى **بلا**.</span><span class="sxs-lookup"><span data-stu-id="58527-154">Then, on the **Shipments** tab, set the **Delivery date control** field to **None**.</span></span> <span data-ttu-id="58527-155">يساعد هذا الإعداد على منع المزامنة من الفشل لعروض أسعار المبيعات.</span><span class="sxs-lookup"><span data-stu-id="58527-155">This setting helps prevent synchronization from failing for sales quotations.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="58527-156">إعداد مشروع تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="58527-156">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="58527-157">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="58527-157">QuoteHeader</span></span>

- <span data-ttu-id="58527-158">الحقل **تاريخ التسليم المطلوب** غير مطلوب في Finance and Operations، وسيحدث فشل في المزامنة في حالة ترك الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="58527-158">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="58527-159">لمنع حدوث هذه المشكلة، إذا كان الحقل فارغًا، يتم أخذ تاريخ افتراضي من **المصدر &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="58527-159">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="58527-160">يجب تحديث التاريخ إلى قيمة مفضلة.</span><span class="sxs-lookup"><span data-stu-id="58527-160">The date should be updated to a preferred value.</span></span> <span data-ttu-id="58527-161">في الوقت الحالي، لا يمكنك إدخال قيمة مثل **اليوم** لتمثيل تاريخ اليوم.</span><span class="sxs-lookup"><span data-stu-id="58527-161">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="58527-162">يجب إدخال تاريخ معين.</span><span class="sxs-lookup"><span data-stu-id="58527-162">You must enter a specific date.</span></span> <span data-ttu-id="58527-163">قيمة القالب الافتراضية للخيار **تاريخ التسليم المطلوب** هي **1/1/2020**.</span><span class="sxs-lookup"><span data-stu-id="58527-163">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="58527-164">يجب ملء الحقل **"كود بلد/منطقة العنوان** في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="58527-164">The **Address Country region code** field is required in Finance and Operations.</span></span> <span data-ttu-id="58527-165">للمساعدة في منع أخطاء المزامنة، يمكنك تحديد قيمة افتراضية يتم استخدامها في حالة ترك الحقل فارغًا في Sales.</span><span class="sxs-lookup"><span data-stu-id="58527-165">To help prevent synchronization errors, you can specify a default value that is used if the field is left blank in Sales.</span></span> <span data-ttu-id="58527-166">هذه القيمة الافتراضية مفيدة هي أيضًا، لأنه لا يترتب عليك إدخال قيمة يدويًا في حقل **منطقة البلد‬** للعناوين المحلية.</span><span class="sxs-lookup"><span data-stu-id="58527-166">This default value is also useful, because you don't have to manually enter a value in the **Country region** field for local addresses.</span></span> <span data-ttu-id="58527-167">لا توجد قيمة قالب افتراضي لـ **DeliveryAddressCountryRegionISOCode**.</span><span class="sxs-lookup"><span data-stu-id="58527-167">There is no default template value for **DeliveryAddressCountryRegionISOCode**.</span></span>
- <span data-ttu-id="58527-168">قم بتحديث تعيين **معرف مؤسسة CDS** في **المصدر &gt; CDS** بحيث يتطابق مع **مؤسسة CDS** في كيان المؤسسة:</span><span class="sxs-lookup"><span data-stu-id="58527-168">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="58527-169">قيمة القالب الافتراضية للخيار **Organization_OrganizationId** هي **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="58527-169">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="58527-170">قيمة القالب الافتراضية للخيار **Account_Organization_OrganizationId** هي **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="58527-170">The default template value for **Account_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="58527-171">قيمة القالب الافتراضية للخيار **InvoiceAccount_OrganizationId** هي **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="58527-171">The default template value for **InvoiceAccount_OrganizationId** is **ORG001**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="58527-172">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="58527-172">QuoteLine</span></span>

- <span data-ttu-id="58527-173">قم بتحديث تعيين **معرف مؤسسة CDS** في **المصدر &gt; CDS** بحيث يتطابق مع **مؤسسة CDS** في كيان المؤسسة:</span><span class="sxs-lookup"><span data-stu-id="58527-173">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="58527-174">قيمة القالب الافتراضية للخيار **Organization_OrganizationId** هي **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="58527-174">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="58527-175">قيمة القالب الافتراضية للخيار **Product_Organization_Organization_OrganizationId** هي **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="58527-175">The default template value for **Product_Organization_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="58527-176">قيمة القالب الافتراضية للخيار **Quotation_Organization_Organization_OrganizationId** هي **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="58527-176">The default template value for **Quotation_Organization_Organization_OrganizationId** is **ORG001**.</span></span>

- <span data-ttu-id="58527-177">الحقل **تاريخ التسليم المطلوب** غير مطلوب في Finance and Operations، وسيحدث فشل في المزامنة في حالة ترك الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="58527-177">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="58527-178">لمنع حدوث هذه المشكلة، إذا كان الحقل فارغًا، يتم أخذ تاريخ افتراضي من **المصدر &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="58527-178">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="58527-179">يجب تحديث التاريخ إلى قيمة مفضلة.</span><span class="sxs-lookup"><span data-stu-id="58527-179">The date should be updated to a preferred value.</span></span> <span data-ttu-id="58527-180">في الوقت الحالي، لا يمكنك إدخال قيمة مثل **اليوم** لتمثيل تاريخ اليوم.</span><span class="sxs-lookup"><span data-stu-id="58527-180">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="58527-181">يجب إدخال تاريخ معين.</span><span class="sxs-lookup"><span data-stu-id="58527-181">You must enter a specific date.</span></span> <span data-ttu-id="58527-182">قيمة القالب الافتراضية للخيار **تاريخ التسليم المطلوب** هي **1/1/2020**.</span><span class="sxs-lookup"><span data-stu-id="58527-182">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="58527-183">يمكنك إضافة التعيينات التالية من **CDS &gt; الوجهة** للمساعدة في ضمان استيراد بنود عروض الأسعار إلى Finance and Operations إذا لم يكن هناك معلومات افتراضية من العميل أو المنتج:</span><span class="sxs-lookup"><span data-stu-id="58527-183">You can add the following mappings from **CDS &gt; Destination** to help guarantee that quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="58527-184">**SiteId** – الموقع مطلوب لإنشاء بنود أوامر المبيعات وعروض الأسعار في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="58527-184">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="58527-185">لا توجد قيمة قالب افتراضي لـ **SiteId**.</span><span class="sxs-lookup"><span data-stu-id="58527-185">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="58527-186">**WarehouseId** – المستودع مطلوب لمعالجة بنود أوامر المبيعات وعروض الأسعار في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="58527-186">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="58527-187">لا توجد قيمة قالب افتراضي لـ **WarehouseId‎**.</span><span class="sxs-lookup"><span data-stu-id="58527-187">There is no default template value for **WarehouseId**.</span></span>

- <span data-ttu-id="58527-188">تأكد من أن تعيين القيمة المطلوب لوحدة القياس الخاصة بالبيع (UOM) في Finance and Operations موجود في تعيين **CDS &gt; الوجهة** للخيار **Quantity_UOM** إلى **SALESUNITSYMBOL**.</span><span class="sxs-lookup"><span data-stu-id="58527-188">Make sure that the required value map for the selling unit of measure (UOM) in Finance and Operations exists in the **CDS &gt; Destination** mapping for **Quantity_UOM** to **SALESUNITSYMBOL**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="58527-189">تعيين القالب في موحد البيانات</span><span class="sxs-lookup"><span data-stu-id="58527-189">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="58527-190">تخضع حقول **الخصم** و**التكاليف** و**الضريبة** لمراقبة إعداد معقد في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="58527-190">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="58527-191">لا يعتمد هذا الإعداد حاليًا تعيين التكامل.</span><span class="sxs-lookup"><span data-stu-id="58527-191">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="58527-192">في التصميم الحالي، يتولى Finance and Operations إدارة حقول **السعر** و**الخصم** و**التكاليف**، و**الضريبة**.</span><span class="sxs-lookup"><span data-stu-id="58527-192">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="58527-193">لا تشكل الحقول **شروط الدفع** و**شروط الشحن** و**شروط التسليم** و**أسلوب الشحن** و**وضع التسليم** جزءًا من التعيينات الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="58527-193">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="58527-194">لتعيين هذه الحقول، يجب إعداد تعيين قيمة خاصة بالبيانات الموجودة في المؤسسات التي تتم مزامنة الكيان بينها.</span><span class="sxs-lookup"><span data-stu-id="58527-194">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="58527-195">تبين الأشكال التوضيحية التالية مثالاً لتعيين قالب في موحد البيانات.</span><span class="sxs-lookup"><span data-stu-id="58527-195">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="58527-196">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="58527-196">QuoteHeader</span></span>

![تعيين القالب في موحد البيانات](./media/sales-quotation-template-mapping-data-integrator-1.png)

![تعيين القالب في موحد البيانات](./media/sales-quotation-template-mapping-data-integrator-2.png)

### <a name="quoteline"></a><span data-ttu-id="58527-199">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="58527-199">QuoteLine</span></span>

![تعيين القالب في موحد البيانات](./media/sales-quotation-template-mapping-data-integrator-3.png)

![تعيين القالب في موحد البيانات](./media/sales-quotation-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a><span data-ttu-id="58527-202">مواضيع مرتبطة</span><span class="sxs-lookup"><span data-stu-id="58527-202">Related topics</span></span>

[<span data-ttu-id="58527-203">مزامنة المنتجات من Finance and Operations إلى المنتجات في Sales</span><span class="sxs-lookup"><span data-stu-id="58527-203">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="58527-204">مزامنة الحسابات من Sales للعملاء في Finance and Operations‎</span><span class="sxs-lookup"><span data-stu-id="58527-204">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="58527-205">مزامنة جهات الاتصال من Sales إلى جهات الاتصال أو العملاء في Finance and Operations‎</span><span class="sxs-lookup"><span data-stu-id="58527-205">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)



