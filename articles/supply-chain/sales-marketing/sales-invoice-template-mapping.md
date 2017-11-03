---
title: "مزامنة رؤوس وبنود فواتير المبيعات من Finance and Operations إلى Sales"
description: "يناقش الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة رؤوس وبنود فواتير المبيعات من Microsoft Dynamics 365 for Sales إلى Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition إلى Microsoft Dynamics 365 for Sales."
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 22ab02555dcac850b18aac9564af41d6c627eade
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-invoice-headers-and-lines-from-finance-and-operations-to-sales"></a><span data-ttu-id="d3d2e-103">مزامنة رؤوس وبنود فواتير المبيعات من Finance and Operations إلى Sales</span><span class="sxs-lookup"><span data-stu-id="d3d2e-103">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d3d2e-104">يناقش الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة رؤوس وبنود فواتير المبيعات من Microsoft Dynamics 365 for Sales إلى Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition إلى Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="d3d2e-104">The topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="d3d2e-105">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="d3d2e-105">Templates and tasks</span></span>

<span data-ttu-id="d3d2e-106">يتم استخدام القوالب والمهام الأساسية التالية لمزامنة رؤوس وبنود فواتير المبيعات من Finance and Operations إلى Sales:</span><span class="sxs-lookup"><span data-stu-id="d3d2e-106">The following templates and underlying tasks are used to synchronize sales invoice headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="d3d2e-107">**اسم القالب في تكامل البيانات**</span><span class="sxs-lookup"><span data-stu-id="d3d2e-107">**Name of the template in Data integration**</span></span> 

     - <span data-ttu-id="d3d2e-108">فواتر المبيعات (Fin and Ops إلى Sales)</span><span class="sxs-lookup"><span data-stu-id="d3d2e-108">Sales Invoices (Fin and Ops to Sales)</span></span>

- <span data-ttu-id="d3d2e-109">**أسماء المهام في مشروع تكامل البيانات**</span><span class="sxs-lookup"><span data-stu-id="d3d2e-109">**Names of the tasks in the Data integration project**</span></span>

    - <span data-ttu-id="d3d2e-110">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="d3d2e-110">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="d3d2e-111">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="d3d2e-111">SalesInvoiceLine</span></span>

<span data-ttu-id="d3d2e-112">مهام المزامنة المطلوبة قبل مزامنة رأس وبنود فواتير المبيعات:</span><span class="sxs-lookup"><span data-stu-id="d3d2e-112">Sync tasks required prior to Sales invoice header and lines synchronization:</span></span>
-   <span data-ttu-id="d3d2e-113">المنتجات (Fin and Ops إلى Sales)</span><span class="sxs-lookup"><span data-stu-id="d3d2e-113">Products (Fin and Ops to Sales)</span></span>
-   <span data-ttu-id="d3d2e-114">الحسابات (Sales إلى Fin and Ops) (في حال استخدامها)</span><span class="sxs-lookup"><span data-stu-id="d3d2e-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
-   <span data-ttu-id="d3d2e-115">جهات الاتصال (Sales إلى Fin and Ops) (في حال استخدامها)</span><span class="sxs-lookup"><span data-stu-id="d3d2e-115">Contacts (Sales to Fin and Ops) (if used)</span></span>
-   <span data-ttu-id="d3d2e-116">رأس وبنود أوامر المبيعات (Fin and Ops إلى Sales)</span><span class="sxs-lookup"><span data-stu-id="d3d2e-116">Sales order header and lines (Fin and Ops to Sales)</span></span>

## <a name="entity-set"></a><span data-ttu-id="d3d2e-117">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="d3d2e-117">Entity set</span></span>

| <span data-ttu-id="d3d2e-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d3d2e-118">Finance and Operations</span></span>                               | <span data-ttu-id="d3d2e-119">Common Data Service (CDS)</span><span class="sxs-lookup"><span data-stu-id="d3d2e-119">Common Data Service (CDS)</span></span>              | <span data-ttu-id="d3d2e-120">مبيعات</span><span class="sxs-lookup"><span data-stu-id="d3d2e-120">Sales</span></span>          |
|------------------------------------------------------|------------------|----------------|
| <span data-ttu-id="d3d2e-121">رؤوس فواتير مبيعات العملاء التي تم الاحتفاظ بها خارجيًا</span><span class="sxs-lookup"><span data-stu-id="d3d2e-121">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="d3d2e-122">SalesInvoice</span><span class="sxs-lookup"><span data-stu-id="d3d2e-122">SalesInvoice</span></span>     | <span data-ttu-id="d3d2e-123">الفواتير</span><span class="sxs-lookup"><span data-stu-id="d3d2e-123">Invoices</span></span>       |
| <span data-ttu-id="d3d2e-124">بنود فواتير مبيعات العملاء التي تم الاحتفاظ بها خارجيًا</span><span class="sxs-lookup"><span data-stu-id="d3d2e-124">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="d3d2e-125">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="d3d2e-125">SalesInvoiceLine</span></span> | <span data-ttu-id="d3d2e-126">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="d3d2e-126">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="d3d2e-127">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="d3d2e-127">Entity flow</span></span>

<span data-ttu-id="d3d2e-128">يتم إنشاء فواتير المبيعات في Finance and Operations وتتم مزامنتها إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="d3d2e-128">Sales invoices are created in Finance and Operations and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="d3d2e-129">لا يتم تضمين الضريبة المرتبطة بالتكاليف في **رأس فاتورة المبيعات** في الوقت الحالي من Finance and Operations إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="d3d2e-129">Tax related to charges on the **Sales invoice header** is currently not included in synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="d3d2e-130">يعود سبب ذلك إلى عدم اعتماد Sales معلومات الضرائب على مستوى الرأس.</span><span class="sxs-lookup"><span data-stu-id="d3d2e-130">This is because Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="d3d2e-131">يتم تضمين الضريبة المتعلقة بالمصاريف على مستوى البنود.</span><span class="sxs-lookup"><span data-stu-id="d3d2e-131">Tax related to charges at the line level is included.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="d3d2e-132">حل العميل المتوقع إلى النقدية في Sales</span><span class="sxs-lookup"><span data-stu-id="d3d2e-132">Prospect to cash solution for Sales</span></span>

-  <span data-ttu-id="d3d2e-133">يُضاف **حقل رقم الفاتورة** إلى كيان **الفاتورة** ويتم عرضه على الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d3d2e-133">An **Invoice number field** is added to the **Invoice** entity and displayed on the page.</span></span>
 
-  <span data-ttu-id="d3d2e-134">يكون الزر **إنشاء فاتورة** في صفحة **أمر المبيعات** مخفيًا لأن إنشاء الفواتير سيتم في Finance and Operations وستتم مزامنتها إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="d3d2e-134">The **Create invoice** button on the **Sales order** page is hidden because invoices will be created in Finance and Operations and synced to Sales.</span></span> <span data-ttu-id="d3d2e-135">لا تكون صفحة **الفاتورة** قابلة للتحرير لأن مزامنة الفواتير ستتم من Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d3d2e-135">The **Invoice** page is non-editable because invoices will be synced from Finance and Operations.</span></span>
 
-  <span data-ttu-id="d3d2e-136">تتغير **حالة أمر المبيعات** تلقائيًا إلى **مفوتر** عندما تتم مزامنة الفاتورة ذات الصلة من Finance and Operations إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="d3d2e-136">The **Sales order status** changes automatically to **Invoiced** when the related invoice from Finance and Operations has been  synchronized to Sales.</span></span> <span data-ttu-id="d3d2e-137">بالإضافة إلى ذلك، يتم تعيين مالك أمر المبيعات الذي تم إنشاء الفاتورة له كمالك للفاتورة.</span><span class="sxs-lookup"><span data-stu-id="d3d2e-137">Also, the owner of the sales order from which the invoice was created is assigned as the owner of the invoice.</span></span> <span data-ttu-id="d3d2e-138">يؤدي ذلك إلى منح المالك أمر المبيعات القدرة على عرض الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="d3d2e-138">This gives the owner of the sales order the ability to view the invoice.</span></span>
 
## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="d3d2e-139">الشروط المسبقة وإعداد التعيين</span><span class="sxs-lookup"><span data-stu-id="d3d2e-139">Preconditions and mapping setup</span></span>

<span data-ttu-id="d3d2e-140">قبل إجراء مزامنة لفواتير المبيعات، لا بد من تحديث الأنظمة بالإعداد التالي:</span><span class="sxs-lookup"><span data-stu-id="d3d2e-140">Before synchronizing sales invoices, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="d3d2e-141">الإعداد في Sales</span><span class="sxs-lookup"><span data-stu-id="d3d2e-141">Setup in Sales</span></span>

- <span data-ttu-id="d3d2e-142">ضمن **الإعدادات** > **الإدارة** > **إعدادات النظام** > **Sales**، تأكد من تعيين الخيار **استخدام حساب أسعار النظام** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="d3d2e-142">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Use system prizing calculation system** is set to **Yes**.</span></span> 

- <span data-ttu-id="d3d2e-143">ضمن **الإعدادات** > **الإدارة** > **إعدادات النظام** > **Sales**، تأكد من تعيين الخيار **أسلوب حساب الخصم** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="d3d2e-143">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Discount calculation method** is set to **Line item**.</span></span> 

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="d3d2e-144">إعداد مشروع تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="d3d2e-144">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="d3d2e-145">SalesInvoiceHeader task</span><span class="sxs-lookup"><span data-stu-id="d3d2e-145">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="d3d2e-146">حدّث تعيين **معرف مؤسسة CDS** في **المصدر** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="d3d2e-146">Update the mapping for **CDS Organization ID** in **Source** > **CDS**.</span></span> 

    -  <span data-ttu-id="d3d2e-147">قيمة القالب الافتراضية للخيار **SalesOrder_Organization_OrganizationId** هي ORG001.</span><span class="sxs-lookup"><span data-stu-id="d3d2e-147">Default template value for **SalesOrder_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="d3d2e-148">قيمة القالب الافتراضية للخيار **Account_Organization_OrganizationId** هي ORG001.</span><span class="sxs-lookup"><span data-stu-id="d3d2e-148">Default template value for **Account_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="d3d2e-149">قيمة القالب الافتراضية للخيار **Organization_OrganizationId** هي ORG001.</span><span class="sxs-lookup"><span data-stu-id="d3d2e-149">Default template value for **Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="d3d2e-150">تأكد من وجود التعيين المطلوب في **المصدر** > **CDS لـ InvoiceCountryRegionId** إلى **BillingAddress_Country**.</span><span class="sxs-lookup"><span data-stu-id="d3d2e-150">Ensure that the needed mapping exists in **Source** > **CDS for InvoiceCountryRegionId** to **BillingAddress_Country**.</span></span>

    -  <span data-ttu-id="d3d2e-151">قيمة القالب هي **ValueMap** مع تعيين عدد من الدول.</span><span class="sxs-lookup"><span data-stu-id="d3d2e-151">Template value is **ValueMap** with a number of countries mapped.</span></span>

- <span data-ttu-id="d3d2e-152">**قائمة الأسعار** مطلوبة لإنشاء الفواتير في Sales.</span><span class="sxs-lookup"><span data-stu-id="d3d2e-152">**Price list** is required to create invoices in Sales.</span></span> <span data-ttu-id="d3d2e-153">حدّث **ValueMap** في **CDS** > **وجهة pricelevelid.name [اسم قائمة الأسعار]** إلى **قائمة الأسعار** المستخدمة في Sales لكل عملة.</span><span class="sxs-lookup"><span data-stu-id="d3d2e-153">Update the **ValueMap** in **CDS** > **Destination for pricelevelid.name [Price List Name]** to the **Price list** used in Sales per currency.</span></span> <span data-ttu-id="d3d2e-154">يمكنك استخدام إعداد **قائمة الأسعار** الافتراضية لعملة واحدة أو استخدام **ValueMap** إذا كان لديك **قوائم أسعار** بعملات متعددة.</span><span class="sxs-lookup"><span data-stu-id="d3d2e-154">You can either use the default **Price list** for single currency or use **ValueMap** if you have **Price lists** in multiple currencies.</span></span>

    -  <span data-ttu-id="d3d2e-155">قيمة قالب **pricelevelid.name [اسم قائمة الأسعار]** هي **ValueMap** استنادًا إلى **العملة**.</span><span class="sxs-lookup"><span data-stu-id="d3d2e-155">Template value for **pricelevelid.name [Price List Name]** is **ValueMap** based on **Currency**.</span></span>
    -  <span data-ttu-id="d3d2e-156">usd: CRM Service USA (نموذج).</span><span class="sxs-lookup"><span data-stu-id="d3d2e-156">usd: CRM Service USA (sample).</span></span> 

#### <a name="salesinvoiceline-task"></a><span data-ttu-id="d3d2e-157">مهمة SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="d3d2e-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="d3d2e-158">تأكد من وجود التعيين المطلوب في **المصدر** > **CDS لوحدة القياس**.</span><span class="sxs-lookup"><span data-stu-id="d3d2e-158">Ensure that the needed mapping exists in **Source** > **CDS for Unit of measure**.</span></span>

- <span data-ttu-id="d3d2e-159">تأكد من أن **ValueMap** المطلوبة من أجل **SalesUnitSymbol** في Finance and Operations موجودة في **المصدر** > **تعيين CDS**.</span><span class="sxs-lookup"><span data-stu-id="d3d2e-159">Ensure that the needed **ValueMap** for **SalesUnitSymbol** in Finance and Operations exists in the **Source** > **CDS mapping**.</span></span> 
    
    - <span data-ttu-id="d3d2e-160">تم تعريف قيمة القالب بوسطة **ValueMap** من أجل **SalesUnitSymbol to Quantity_UOM**.</span><span class="sxs-lookup"><span data-stu-id="d3d2e-160">Template value with **ValueMap** is defined for **SalesUnitSymbol to Quantity_UOM**.</span></span>
    
-  <span data-ttu-id="d3d2e-161">حدّث تعيين **معرف مؤسسة CDS في المصدر** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="d3d2e-161">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span> 

    -  <span data-ttu-id="d3d2e-162">قيمة القالب الافتراضية للخيار **SalesInvoicer_Organization_OrganizationId** هي ORG001.</span><span class="sxs-lookup"><span data-stu-id="d3d2e-162">Default template value for **SalesInvoicer_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="d3d2e-163">قيمة القالب الافتراضية للخيار **Product_Organization_OrganizationId** هي ORG001.</span><span class="sxs-lookup"><span data-stu-id="d3d2e-163">Default template value for **Product_Organization_OrganizationId** is ORG001.</span></span>
 
## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="d3d2e-164">تعيين القالب في موحد البيانات</span><span class="sxs-lookup"><span data-stu-id="d3d2e-164">Template mapping in Data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="d3d2e-165">لا تشكل خيارات **شروط الدفع** و**شروط الشحن** و**شروط التسليم** و**أسلوب الشحن** و**وضع التسليم** جزءًا من التعيينات الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="d3d2e-165">**Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** are not part of the default mappings.</span></span> <span data-ttu-id="d3d2e-166">يتطلب تعيين هذه الحقول إعداد تعيين القيمة، وهي خاصة بالبيانات الموجودة في المؤسسات التي تتم مزامنة الكيان بينها.</span><span class="sxs-lookup"><span data-stu-id="d3d2e-166">Mapping of these fields requires value mapping to be set up, which is specific to the data in the organizations between which the entity is synchronized.</span></span>

<span data-ttu-id="d3d2e-167">تبين الأشكال التوضيحية التالية مثالاً لتعيين قالب في موحد البيانات.</span><span class="sxs-lookup"><span data-stu-id="d3d2e-167">The following illustrations show an example of a template mapping in data integrator.</span></span>

![تعيين القالب في موحد البيانات](./media/sales-invoice-template-mapping-data-integrator-1.png)

![تعيين القالب في موحد البيانات](./media/sales-invoice-template-mapping-data-integrator-2.png)

![تعيين القالب في موحد البيانات](./media/sales-invoice-template-mapping-data-integrator-3.png)

![تعيين القالب في موحد البيانات](./media/sales-invoice-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="d3d2e-172">مواضيع مرتبطة</span><span class="sxs-lookup"><span data-stu-id="d3d2e-172">Related topics</span></span>

[<span data-ttu-id="d3d2e-173">مزامنة المنتجات من Finance and Operations إلى المنتجات في Sales</span><span class="sxs-lookup"><span data-stu-id="d3d2e-173">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="d3d2e-174">مزامنة الحسابات من Sales للعملاء في Finance and Operations‎</span><span class="sxs-lookup"><span data-stu-id="d3d2e-174">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="d3d2e-175">مزامنة جهات الاتصال من Sales لجهات الاتصال في Finance and Operations‎</span><span class="sxs-lookup"><span data-stu-id="d3d2e-175">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="d3d2e-176">مزامنة رؤوس وبنود عرض أسعار المبيعات‬ من Sales إلى Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d3d2e-176">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="d3d2e-177">مزامنة رؤوس وبنود أوامر المبيعات من Finance and Operations إلى Sales</span><span class="sxs-lookup"><span data-stu-id="d3d2e-177">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)


