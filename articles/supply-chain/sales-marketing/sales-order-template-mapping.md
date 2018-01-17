---
title: "مزامنة رؤوس وبنود أوامر المبيعات من Finance and Operations إلى Sales"
description: "يناقش الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة رؤوس وبنود أوامر المبيعات من Microsoft Dynamics 365 for Sales إلى Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition إلى Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
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
ms.openlocfilehash: d7e4c435a3344f6a5d66e1889b633d80cda085eb
ms.contentlocale: ar-sa
ms.lasthandoff: 01/17/2018

---

# <a name="synchronize-sales-order-headers-and-lines-from-finance-and-operations-to-sales"></a><span data-ttu-id="feba7-103">مزامنة رؤوس وبنود أوامر المبيعات من Finance and Operations إلى Sales</span><span class="sxs-lookup"><span data-stu-id="feba7-103">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="feba7-104">يناقش الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة رؤوس وبنود أوامر المبيعات من Microsoft Dynamics 365 for Sales إلى Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition إلى Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="feba7-104">The topic discusses the templates and underlying tasks that are used to synchronize sales order headers and lines from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span> 

## <a name="template-and-tasks"></a><span data-ttu-id="feba7-105">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="feba7-105">Template and tasks</span></span>

<span data-ttu-id="feba7-106">يتم استخدام القوالب والمهام الأساسية التالية لمزامنة رؤوس وبنود أوامر المبيعات من Finance and Operations إلى Sales:</span><span class="sxs-lookup"><span data-stu-id="feba7-106">The following templates and underlying tasks are used to synchronize sales order headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="feba7-107">**اسم القالب في تكامل البيانات**</span><span class="sxs-lookup"><span data-stu-id="feba7-107">**Name of template in Data integration**</span></span> 

    - <span data-ttu-id="feba7-108">أوامر المبيعات (Fin and Ops إلى Sales)</span><span class="sxs-lookup"><span data-stu-id="feba7-108">Sales Orders (Fin and Ops to Sales)</span></span>
    
- <span data-ttu-id="feba7-109">**أسماء المهام في مشروع تكامل البيانات**</span><span class="sxs-lookup"><span data-stu-id="feba7-109">**Names of tasks in Data integration project**</span></span>

    - <span data-ttu-id="feba7-110">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="feba7-110">OrderHeader</span></span>
    - <span data-ttu-id="feba7-111">OrderLine</span><span class="sxs-lookup"><span data-stu-id="feba7-111">OrderLine</span></span>

<span data-ttu-id="feba7-112">مهام المزامنة المطلوبة قبل مزامنة رأس وبنود فواتير المبيعات:</span><span class="sxs-lookup"><span data-stu-id="feba7-112">Sync tasks required prior to Sales invoice header and lines sync:</span></span>

- <span data-ttu-id="feba7-113">المنتجات (Fin and Ops إلى Sales)</span><span class="sxs-lookup"><span data-stu-id="feba7-113">Products (Fin and Ops to Sales)</span></span>
- <span data-ttu-id="feba7-114">الحسابات (Sales إلى Fin and Ops) (في حال استخدامها)</span><span class="sxs-lookup"><span data-stu-id="feba7-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
- <span data-ttu-id="feba7-115">جهات الاتصال إلى العملاء (Sales إلى Fin and Ops) (في حال استخدامها)</span><span class="sxs-lookup"><span data-stu-id="feba7-115">Contacts to Customers (Sales to Fin and Ops) (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="feba7-116">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="feba7-116">Entity set</span></span>

| <span data-ttu-id="feba7-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="feba7-117">Finance and Operations</span></span> |    <span data-ttu-id="feba7-118">Common Data Service (CDS)</span><span class="sxs-lookup"><span data-stu-id="feba7-118">Common Data Service (CDS)</span></span>         |     <span data-ttu-id="feba7-119">مبيعات</span><span class="sxs-lookup"><span data-stu-id="feba7-119">Sales</span></span>      |
|------------------------|----------------|----------------|
| <span data-ttu-id="feba7-120">رؤوس أوامر المبيعات CDS</span><span class="sxs-lookup"><span data-stu-id="feba7-120">CDS sales order headers</span></span>| <span data-ttu-id="feba7-121">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="feba7-121">SalesOrder</span></span>     | <span data-ttu-id="feba7-122">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="feba7-122">SalesOrders</span></span> |
| <span data-ttu-id="feba7-123">بنود أمر مبيعات CDS</span><span class="sxs-lookup"><span data-stu-id="feba7-123">CDS sales order lines</span></span>  | <span data-ttu-id="feba7-124">SalesOrderLine</span><span class="sxs-lookup"><span data-stu-id="feba7-124">SalesOrderLine</span></span> | <span data-ttu-id="feba7-125">SalesOrderDetails</span><span class="sxs-lookup"><span data-stu-id="feba7-125">SalesOrderDetails</span></span>|

## <a name="entity-flow"></a><span data-ttu-id="feba7-126">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="feba7-126">Entity flow</span></span>

<span data-ttu-id="feba7-127">يتم إنشاء أوامر المبيعات في Finance and Operations وتتم مزامنتها إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="feba7-127">Sales orders are created in Finance and Operations and synchronized to Sales.</span></span>

<span data-ttu-id="feba7-128">تضمن عوامل التصفية الموجودة في القالب من تضمين فقط أوامر المبيعات ذات الصلة فقط في المزامنة:</span><span class="sxs-lookup"><span data-stu-id="feba7-128">Filters in the template ensure that only relevant sales orders are included in the synchronization:</span></span>

- <span data-ttu-id="feba7-129">ستتضمن عملية المزامنة عملاء الطلب والفوترة في أمر المبيعات الذي ينشأ من Sales.</span><span class="sxs-lookup"><span data-stu-id="feba7-129">Both ordering and invoicing customer on the sales order that originate from Sales will be included in the synchronization.</span></span> <span data-ttu-id="feba7-130">في Finance and Operations، يتم استخدام الحقلين **OrderingCustomerIsExternallyMaintained** و**InvoiceCustomerIsExternallyMaintained** لتعقب المزامنة في كيانات البيانات.</span><span class="sxs-lookup"><span data-stu-id="feba7-130">In Finance and Operations, the fields **OrderingCustomerIsExternallyMaintained** and **InvoiceCustomerIsExternallyMaintained** are used to track the synchronization in the data entities.</span></span>

- <span data-ttu-id="feba7-131">يجب تأكيد **أمر المبيعات** في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="feba7-131">The **Sales order** in Finance and Operations must be confirmed.</span></span> <span data-ttu-id="feba7-132">وحدها أوامر المبيعات المؤكدة أو أوامر المبيعات ذات حالة معالجة أعلى، مثل الحالة "مشحون" أو "مفوتر"، تتم مزامنتها إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="feba7-132">Only the confirmed sales orders or sales orders with higher processing status, for example, Shipped or Invoiced status, are synchronized to Sales.</span></span>

- <span data-ttu-id="feba7-133">بعد إنشاء أمر مبيعات أو تعديله، يجب تنفيذ الوظيفة الدفعية **حساب إجماليات المبيعات‬** في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="feba7-133">After creating or modifying a sales order, the batch job **Calculate sales totals** in Finance and Operations must be executed.</span></span> <span data-ttu-id="feba7-134">وحدها أوامر المبيعات التي تم حساب إجماليات المبيعات‬ فيها ستتم مزامنتها إلى CDS وSales.</span><span class="sxs-lookup"><span data-stu-id="feba7-134">Only the sales orders with sales totals calculated will be synced to CDS and Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="feba7-135">لا يتم تضمين الضريبة المرتبطة بالتكاليف في **رأس أمر المبيعات‬** في الوقت الحالي من Finance and Operations إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="feba7-135">Tax related to charges on the **Sales order header** is currently not included in synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="feba7-136">يعود سبب ذلك إلى عدم اعتماد Sales معلومات الضرائب على مستوى الرأس.</span><span class="sxs-lookup"><span data-stu-id="feba7-136">This is because Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="feba7-137">يتم تضمين الضريبة المتعلقة بالمصاريف على مستوى البنود.</span><span class="sxs-lookup"><span data-stu-id="feba7-137">Tax related to charges at the line level is included.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="feba7-138">حل العميل المتوقع إلى النقدية في Sales</span><span class="sxs-lookup"><span data-stu-id="feba7-138">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="feba7-139">تظهر على الصفحة الحقول الجديدة المضافة إلى كيان **الأمر**:</span><span class="sxs-lookup"><span data-stu-id="feba7-139">New fields are added to the **Order** entity and displayed on the page:</span></span>

- <span data-ttu-id="feba7-140">**تتم المحافظة عليها خارجيًا‬‏‫‬‏‫** - عيّن هذا الخيار إلى **نعم** عندما يأتي الأمر من Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="feba7-140">**Is Maintained Externally** - Set to **Yes** when the order is coming from Finance and Operations.</span></span>

- <span data-ttu-id="feba7-141">**حالة المعالجة** - يستخدم لعرض حالة معالجة الأمر في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="feba7-141">**Processing status** - Used to show the processing status of the order in Finance and Operations.</span></span> <span data-ttu-id="feba7-142">القيم هي:</span><span class="sxs-lookup"><span data-stu-id="feba7-142">Values are:</span></span>

    - <span data-ttu-id="feba7-143">نشط</span><span class="sxs-lookup"><span data-stu-id="feba7-143">Active</span></span>
    - <span data-ttu-id="feba7-144">أوامر المبيعات المؤكدة</span><span class="sxs-lookup"><span data-stu-id="feba7-144">Confirmed</span></span>
    - <span data-ttu-id="feba7-145">كشف التعبئة</span><span class="sxs-lookup"><span data-stu-id="feba7-145">Packing Slip</span></span>
    - <span data-ttu-id="feba7-146">مفوتر</span><span class="sxs-lookup"><span data-stu-id="feba7-146">Invoiced</span></span>
    - <span data-ttu-id="feba7-147">منتقي</span><span class="sxs-lookup"><span data-stu-id="feba7-147">Picked</span></span>
    - <span data-ttu-id="feba7-148">منتقى جزئيًا</span><span class="sxs-lookup"><span data-stu-id="feba7-148">Partially Picked</span></span>
    - <span data-ttu-id="feba7-149">معبأ جزئيًا</span><span class="sxs-lookup"><span data-stu-id="feba7-149">Partially Packed</span></span>
    - <span data-ttu-id="feba7-150">مشحون</span><span class="sxs-lookup"><span data-stu-id="feba7-150">Shipped</span></span>
    - <span data-ttu-id="feba7-151">مشحون جزئيًا</span><span class="sxs-lookup"><span data-stu-id="feba7-151">Partially Shipped</span></span>
    - <span data-ttu-id="feba7-152">مفوتر جزئيًا</span><span class="sxs-lookup"><span data-stu-id="feba7-152">Partially Invoiced</span></span>
    - <span data-ttu-id="feba7-153">تم الإلغاء</span><span class="sxs-lookup"><span data-stu-id="feba7-153">Cancelled</span></span>

<span data-ttu-id="feba7-154">يُستخدم الإعداد **لديه منتجات تتم المحافظة عليها خارجيًا فقط** في سيناريوهات أخرى لأوامر المبيعات (مزامنة من Sales إلى Finance and Operations) لتعقب ما إذا كان أمر المبيعات عبارة عن **منتجات تتم المحافظة عليها خارجيًا** بشكل كامل، وفي هذه الحالة تتم المحافظة على المنتجات في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="feba7-154">The **Has Externally Maintained Products Only** setting is used in other sales order scenarios (from Sales to Finance and Operation sync) to consistently keep track of whether the sales order is made up entirely of **Externally Maintained Products**, in which case products are maintained in Finance and Operations.</span></span> <span data-ttu-id="feba7-155">يضمن هذا السلوك عدم محاولتك مزامنة بنود أمر المبيعات مع منتجات غير معروفة بالنسبة إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="feba7-155">This ensures that you don't try to sync sales order lines with products that are unknown to Finance and Operations.</span></span>
 
<span data-ttu-id="feba7-156">تكون الأزرار **"إنشاء فاتورة"** و**إلغاء الأمر** و**إعادة حساب** و**الحصول على منتجات"** و**البحث عن عنوان** على **أمر المبيعات** مخفية للأوامر التي تتم المحافظة عليها خارجيًا إذ سيتم إنشاء الفواتير في Finance and Operations وستتم مزامنتها إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="feba7-156">The **Create Invoice**, **Cancel Order**, **Recalculate**, **Get Products** and **Lookup Address** buttons on the **Sales order** page are hidden for externally maintained orders because invoices will be created in Finance and Operations and synced to Sales.</span></span> <span data-ttu-id="feba7-157">لا تكون صفحة الأمر قابلة للتحرير لأن مزامنة معلومات أمر المبيعات ستتم من Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="feba7-157">The order page is non-editable because sales order information will be synced from Finance and Operations.</span></span>
 
<span data-ttu-id="feba7-158">سوف تبقى **حالة أمر المبيعات** نشطة للتأكد من إمكانية انسياب التغييرات من Finance and Operations إلى **أمر المبيعات‏‎** في Sales.</span><span class="sxs-lookup"><span data-stu-id="feba7-158">The **Sales order status** will remain active to ensure that changes from Finance and Operations can flow to the **Sales order** in Sales.</span></span> <span data-ttu-id="feba7-159">يتم التحكم في ذلك من خلال تعيين الإعداد الافتراضي **Statecode [الحالة]** إلى **نشط** في مشروع تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="feba7-159">This is controlled by setting the default **Statecode [Status]** to **Active** in the Data integration project.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="feba7-160">الشروط المسبقة وإعداد التعيين</span><span class="sxs-lookup"><span data-stu-id="feba7-160">Preconditions and mapping setup</span></span> 

<span data-ttu-id="feba7-161">قبل إجراء مزامنة لأوامر المبيعات، لا بد من تحديث الأنظمة بالإعداد التالي:</span><span class="sxs-lookup"><span data-stu-id="feba7-161">Before synchronizing sales orders, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="feba7-162">الإعداد في Sales</span><span class="sxs-lookup"><span data-stu-id="feba7-162">Setup in Sales</span></span>

- <span data-ttu-id="feba7-163">تحقق من أذونات الفريق الذي تم تعيين المستخدم (من **إعداد الاتصال** في Sales) إليه.</span><span class="sxs-lookup"><span data-stu-id="feba7-163">Ensure permissions for the team that the user (from your Sales **Connection set**) is assigned to.</span></span> <span data-ttu-id="feba7-164">إذا كنت تستخدم بيانات العرض التوضيحي، فعادةً ما يكون لدى المستخدم حق وصول المسؤول، ولكن هذا الحق لا يتوفر للفريق.</span><span class="sxs-lookup"><span data-stu-id="feba7-164">If you are using demo data, usually the user has admin access, but not the team.</span></span> <span data-ttu-id="feba7-165">من دون ذلك سوف تتلقى رسالة خطأ تفيد بأن الفريق الرئيسي مفقود عند تشغيل المشروع من موحد البيانات.</span><span class="sxs-lookup"><span data-stu-id="feba7-165">Without this you will get an error that Principal team is missing when running the project from Data integrator.</span></span> 

    - <span data-ttu-id="feba7-166">ضمن **الإعدادات** > **الأمان** > **الفرق**، حدد الفريق المناسب، وانقر فوق **إدارة الأدوار** وحدد دورًا باستخدام الأذونات المطلوبة على سبيل المثال، مسؤول النظام.</span><span class="sxs-lookup"><span data-stu-id="feba7-166">Under **Settings** > **Security** > **Teams**, select the relevant team, click **Manage Roles** and select a role with the desired permissions e.g. System Administrator.</span></span>

- <span data-ttu-id="feba7-167">ضمن **الإعدادات** > **الإدارة** > **إعدادات النظام** > **Sales**، تأكد من تعيين الخيار **استخدام حساب أسعار النظام** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="feba7-167">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Use system prizing calculation system** is set to **Yes**.</span></span> 

- <span data-ttu-id="feba7-168">ضمن **الإعدادات** > **الإدارة** > **إعدادات النظام** > **Sales**، تأكد من تعيين الخيار **أسلوب حساب الخصم** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="feba7-168">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Discount calculation method** is set to **Line item**.</span></span> 

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="feba7-169">الإعداد في Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="feba7-169">Setup in Finance and Operations</span></span>

<span data-ttu-id="feba7-170">عيّن **المبيعات والتسويق** > **المهام الدورية** > **حساب إجماليات المبيعات‬** لتشغيلها كوظيفة دفعية، مع تعيين **حساب إجماليات أوامر المبيعات‬** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="feba7-170">Set **Sales and marketing** > **Periodic tasks** > **Calculate sales totals** to run as a batch job, with **Calculate totals for sales orders** set to **Yes**.</span></span> <span data-ttu-id="feba7-171">يُعد هذا الأمر ضروريًا لأن أوامر المبيعات التي تم حساب إجماليات المبيعات‬ فيها هي فقط أوامر المبيعات التي ستتم مزامنتها إلى CDS وSales.</span><span class="sxs-lookup"><span data-stu-id="feba7-171">This is important because only the sales orders with sales totals calculated will be synced to CDS and Sales.</span></span> <span data-ttu-id="feba7-172">يجب أن يكون مدى تكرار الوظيفة الدفعية متوافقًا مع مدى تكرار مزامنة أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="feba7-172">The frequency of the batch job should be alligned with the frequency of the sales order synchronization.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="feba7-173">إعداد مشروع تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="feba7-173">Setup in the Data integration project</span></span>

#### <a name="salesheader-task"></a><span data-ttu-id="feba7-174">مهمة SalesHeader</span><span class="sxs-lookup"><span data-stu-id="feba7-174">SalesHeader task</span></span>

- <span data-ttu-id="feba7-175">حدّث تعيين **معرف مؤسسة CDS في المصدر** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="feba7-175">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span>

    - <span data-ttu-id="feba7-176">قيمة القالب الافتراضية للخيار **Account_Organization_OrganizationId** هي ORG001.</span><span class="sxs-lookup"><span data-stu-id="feba7-176">Default template value for **Account_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="feba7-177">قيمة القالب الافتراضية للخيار **InvoiceAccount_Organization_OrganizationId** هي ORG001.</span><span class="sxs-lookup"><span data-stu-id="feba7-177">Default template value for **InvoiceAccount_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="feba7-178">قيمة القالب الافتراضية للخيار **Organization_OrganizationId** هي ORG001.</span><span class="sxs-lookup"><span data-stu-id="feba7-178">Default template value for **Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="feba7-179">تأكد من وجود التعيين المطلوب في **المصدر** > **CDS لـ InvoiceCountryRegionId إلى BillingAddress_Country** ولـ **DeliveryCountryRegionId إلى DeliveryAddress_Country**.</span><span class="sxs-lookup"><span data-stu-id="feba7-179">Ensure that the needed mapping exists in **Source** > **CDS for InvoiceCountryRegionId to BillingAddress_Country** and for **DeliveryCountryRegionId to DeliveryAddress_Country**.</span></span>

    - <span data-ttu-id="feba7-180">قيمة القالب هي **ValueMap** مع تعيين عدد من الدول.</span><span class="sxs-lookup"><span data-stu-id="feba7-180">Template value is **ValueMap** with a number of countries mapped.</span></span>

- <span data-ttu-id="feba7-181">**قائمة الأسعار** مطلوبة لإنشاء الأوامر في Sales.</span><span class="sxs-lookup"><span data-stu-id="feba7-181">**Price list** is required to create orders in Sales.</span></span> <span data-ttu-id="feba7-182">حدّث **ValueMap** في **CDS** > **وجهة** لـ **pricelevelid.name [اسم قائمة الأسعار]** إلى **قائمة الأسعار** المستخدمة في Sales لكل عملة.</span><span class="sxs-lookup"><span data-stu-id="feba7-182">Update the **ValueMap** in **CDS** > **Destination** for **pricelevelid.name [Price List Name]** to the **Price list** used in Sales per currency.</span></span> <span data-ttu-id="feba7-183">يمكنك استخدام إعداد **قائمة الأسعار** الافتراضية لعملة واحدة أو استخدام **ValueMap** إذا كان لديك **قوائم أسعار** بعملات متعددة.</span><span class="sxs-lookup"><span data-stu-id="feba7-183">You can either used the default **Price list** for single currency or use **ValueMap** if you have **Price lists** in multiple currencies.</span></span>
    
    - <span data-ttu-id="feba7-184">قيمة القالب الافتراضية للخيار **pricelevelid.name [اسم قائمة الأسعار]** هو CRM Service USA (نموذج).</span><span class="sxs-lookup"><span data-stu-id="feba7-184">Default template value for **pricelevelid.name [Price List Name]** is CRM Service USA (sample).</span></span> 

#### <a name="salesline-task"></a><span data-ttu-id="feba7-185">مهمة SalesLine</span><span class="sxs-lookup"><span data-stu-id="feba7-185">SalesLine task</span></span>

- <span data-ttu-id="feba7-186">حدّث تعيين **معرف مؤسسة CDS في المصدر** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="feba7-186">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span> 
    
    - <span data-ttu-id="feba7-187">قيمة القالب الافتراضية للخيار **SalesOrder_Organization_OrganizationId** هي ORG001.</span><span class="sxs-lookup"><span data-stu-id="feba7-187">Default template value for **SalesOrder_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="feba7-188">قيمة القالب الافتراضية للخيار **Product_Organization_OrganizationId** هي ORG001.</span><span class="sxs-lookup"><span data-stu-id="feba7-188">Default template value for **Product_Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="feba7-189">تأكد من وجود التعيين المطلوب في **المصدر** > **CDS** لـ **DeliveryCountryRegionId** إلى **DeliveryAddress_Country**.</span><span class="sxs-lookup"><span data-stu-id="feba7-189">Ensure that the needed mapping exists in **Source** > **CDS** for **DeliveryCountryRegionId** to **DeliveryAddress_Country**.</span></span>

    - <span data-ttu-id="feba7-190">قيمة القالب هي **ValueMap** مع تعيين عدد من الدول.</span><span class="sxs-lookup"><span data-stu-id="feba7-190">Template value is **ValueMap** with a number of countries mapped.</span></span>
    
- <span data-ttu-id="feba7-191">تأكد من أن **ValueMap** المطلوبة من أجل **SalesUnitSymbol** في Finance and Operations موجودة في **المصدر** > **تعيين CDS**.</span><span class="sxs-lookup"><span data-stu-id="feba7-191">Ensure that the needed **ValueMap** for **SalesUnitSymbol** in Finance and Operations exists in the **Source** > **CDS mapping**.</span></span>

    - <span data-ttu-id="feba7-192">تم تعريف قيمة القالب بوسطة **ValueMap** من أجل **SalesUnitSymbol to Quantity_UOM**.</span><span class="sxs-lookup"><span data-stu-id="feba7-192">Template value with **ValueMap** is defined for **SalesUnitSymbol to Quantity_UOM**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="feba7-193">تعيين القالب في موحد البيانات</span><span class="sxs-lookup"><span data-stu-id="feba7-193">Template mapping in data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="feba7-194">لا تشكل الحقول **شروط الدفع** و**شروط الشحن** و**شروط التسليم** و**أسلوب الشحن** و**وضع التسليم** جزءًا من التعيينات الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="feba7-194">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="feba7-195">لتعيين هذه الحقول، يجب إعداد تعيين قيمة خاصة بالبيانات الموجودة في المؤسسات التي تتم مزامنة الكيان بينها.</span><span class="sxs-lookup"><span data-stu-id="feba7-195">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="feba7-196">تبين الأشكال التوضيحية التالية مثالاً لتعيين قالب في موحد البيانات.</span><span class="sxs-lookup"><span data-stu-id="feba7-196">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="orderheader"></a><span data-ttu-id="feba7-197">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="feba7-197">OrderHeader</span></span>

![تعيين القالب في موحد البيانات](./media/sales-order-template-mapping-data-integrator-1.png)

![تعيين القالب في موحد البيانات](./media/sales-order-template-mapping-data-integrator-2.png)

### <a name="orderline"></a><span data-ttu-id="feba7-200">OrderLine</span><span class="sxs-lookup"><span data-stu-id="feba7-200">OrderLine</span></span>

![تعيين القالب في موحد البيانات](./media/sales-order-template-mapping-data-integrator-3.png)

![تعيين القالب في موحد البيانات](./media/sales-order-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="feba7-203">مواضيع مرتبطة</span><span class="sxs-lookup"><span data-stu-id="feba7-203">Related topics</span></span>

[<span data-ttu-id="feba7-204">مزامنة المنتجات من Finance and Operations إلى المنتجات في Sales</span><span class="sxs-lookup"><span data-stu-id="feba7-204">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="feba7-205">مزامنة الحسابات من Sales للعملاء في Finance and Operations‎</span><span class="sxs-lookup"><span data-stu-id="feba7-205">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="feba7-206">مزامنة جهات الاتصال من Sales لجهات الاتصال في Finance and Operations‎</span><span class="sxs-lookup"><span data-stu-id="feba7-206">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="feba7-207">مزامنة رؤوس وبنود عرض أسعار المبيعات‬ من Sales إلى Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="feba7-207">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="feba7-208">مزامنة رؤوس وبنود فواتير المبيعات من Finance and Operations إلى Sales</span><span class="sxs-lookup"><span data-stu-id="feba7-208">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)


