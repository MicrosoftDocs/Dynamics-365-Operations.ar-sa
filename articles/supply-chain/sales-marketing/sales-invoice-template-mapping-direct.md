---
title: مزامنة رؤوس وبنود فواتير المبيعات مباشرةً من Supply Chain Management إلى Sales
description: يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة رؤوس وبنود فواتير المبيعات مباشرةً من Dynamics 365 Supply Chain Management إلى Dynamics 365 Sales.
author: ChristianRytt
manager: tfehr
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 6cbc4d86ac41d90480428ec5439d1360c4d67137
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215966"
---
# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="fb6a6-103">مزامنة رؤوس وبنود فاتورة المبيعات مباشرةً من Finance and Operations إلى Sales</span><span class="sxs-lookup"><span data-stu-id="fb6a6-103">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fb6a6-104">يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة رؤوس وبنود فواتير المبيعات مباشرةً من Dynamics 365 Supply Chain Management إلى Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="fb6a6-104">This topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines directly from Dynamics 365 Supply Chain Management to Dynamics 365 Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="fb6a6-105">تدفق البيانات في حل العميل المتوقع إلى النقدية</span><span class="sxs-lookup"><span data-stu-id="fb6a6-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="fb6a6-106">يستخدم حل العميل المتوقع إلى النقدية ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Supply Chain Management وSales.</span><span class="sxs-lookup"><span data-stu-id="fb6a6-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="fb6a6-107">تسمح قوالب حل العميل المتوقع إلى النقدية المتوفرة مع ميزة تكامل البيانات بتدفق بيانات الحسابات وجهات الاتصال والمنتجات وعروض أسعار المبيعات وأوامر المبيعات وفواتير المبيعات بين Supply Chain Management وSales.</span><span class="sxs-lookup"><span data-stu-id="fb6a6-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="fb6a6-108">يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات بين Supply Chain Management وSales.</span><span class="sxs-lookup"><span data-stu-id="fb6a6-108">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="fb6a6-109">[![تدفق البيانات في حل العميل المتوقع إلى النقدية](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="fb6a6-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="fb6a6-110">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="fb6a6-110">Templates and tasks</span></span>

<span data-ttu-id="fb6a6-111">للوصول إلى القوالب المتوفرة، افتح [Power Apps مركز الإدارة](https://preview.admin.powerapps.com/dataintegration) .</span><span class="sxs-lookup"><span data-stu-id="fb6a6-111">To access the available templates, open [Power Apps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="fb6a6-112">حدد **المشاريع**، وبعد ذلك، في الزاوية العلوية اليسرى، حدد **مشروع جديد** لتحديد القوالب العامة.</span><span class="sxs-lookup"><span data-stu-id="fb6a6-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="fb6a6-113">يتم استخدام القالب والمهام الأساسية التالية لمزامنة رؤوس وبنود فاتورة المبيعات من Supply Chain Management إلى المبيعات:</span><span class="sxs-lookup"><span data-stu-id="fb6a6-113">The following template and underlying tasks are used to synchronize sales invoice headers and lines from Supply Chain Management to Sales:</span></span>

- <span data-ttu-id="fb6a6-114">**اسم القالب في تكامل البيانات:** فواتير المبيعات (Fin and Ops إلى Sales)‬ - مباشر</span><span class="sxs-lookup"><span data-stu-id="fb6a6-114">**Name of the template in Data integration:** Sales Invoices (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="fb6a6-115">**أسماء المهام في مشروع تكامل البيانات:**</span><span class="sxs-lookup"><span data-stu-id="fb6a6-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="fb6a6-116">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="fb6a6-116">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="fb6a6-117">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="fb6a6-117">SalesInvoiceLine</span></span>

<span data-ttu-id="fb6a6-118">يجب تنفيذ مهام المزامنة التالية قبل حدوث مزامنة رؤوس وبنود فواتير المبيعات.</span><span class="sxs-lookup"><span data-stu-id="fb6a6-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="fb6a6-119">المنتجات (من Supply Chain Management إلى Sales) - مباشر</span><span class="sxs-lookup"><span data-stu-id="fb6a6-119">Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="fb6a6-120">الحسابات (من Sales إلى Supply Chain Management) - مباشر (إذا ما تم استخدامه)</span><span class="sxs-lookup"><span data-stu-id="fb6a6-120">Accounts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="fb6a6-121">جهات الاتصال (Sales إلى Supply Chain Management) - مباشر (إذا ما تم استخدامه)</span><span class="sxs-lookup"><span data-stu-id="fb6a6-121">Contacts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="fb6a6-122">رؤوس وبنود أوامر المبيعات (من Supply Chain Management إلى Sales) - مباشرةً</span><span class="sxs-lookup"><span data-stu-id="fb6a6-122">Sales order header and lines (Supply Chain Management to Sales) - Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="fb6a6-123">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="fb6a6-123">Entity set</span></span>

| <span data-ttu-id="fb6a6-124">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="fb6a6-124">Supply Chain Management</span></span>                              | <span data-ttu-id="fb6a6-125">ال‏‏مبيعات</span><span class="sxs-lookup"><span data-stu-id="fb6a6-125">Sales</span></span>          |
|------------------------------------------------------|----------------|
| <span data-ttu-id="fb6a6-126">رؤوس فواتير مبيعات العملاء التي تم الاحتفاظ بها خارجيًا</span><span class="sxs-lookup"><span data-stu-id="fb6a6-126">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="fb6a6-127">الفواتير</span><span class="sxs-lookup"><span data-stu-id="fb6a6-127">Invoices</span></span>       |
| <span data-ttu-id="fb6a6-128">بنود فواتير مبيعات العملاء التي تم الاحتفاظ بها خارجيًا</span><span class="sxs-lookup"><span data-stu-id="fb6a6-128">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="fb6a6-129">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="fb6a6-129">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="fb6a6-130">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="fb6a6-130">Entity flow</span></span>

<span data-ttu-id="fb6a6-131">يتم إنشاء فواتير المبيعات في Supply Chain Management وتتم مزامنتها إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="fb6a6-131">Sales invoices are created in Supply Chain Management and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="fb6a6-132">في الوقت الحالي، لا يتم تضمين الضريبة المرتبطة بالتكاليف في رأس فاتورة المبيعات في المزامنة من Supply Chain Management إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="fb6a6-132">Currently, tax that is related to charges on the sales invoice header isn't included in the synchronization from Supply Chain Managements to Sales.</span></span> <span data-ttu-id="fb6a6-133">يعود سبب ذلك إلى عدم دعم Sales لمعلومات الضرائب على مستوى الرأس.</span><span class="sxs-lookup"><span data-stu-id="fb6a6-133">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="fb6a6-134">ومع ذلك، يتم تضمين الضريبة المرتبطة بالتكاليف على مستوى البند في المزامنة.</span><span class="sxs-lookup"><span data-stu-id="fb6a6-134">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="fb6a6-135">حل العميل المتوقع إلى النقدية في Sales</span><span class="sxs-lookup"><span data-stu-id="fb6a6-135">Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="fb6a6-136">تمت إضافة حقل **رقم الفاتورة** إلى كيان **الفاتورة** ويتم عرضه على الصفحة.</span><span class="sxs-lookup"><span data-stu-id="fb6a6-136">An **Invoice number** field has been added to the **Invoice** entity and appears on the page.</span></span>
- <span data-ttu-id="fb6a6-137">يكون الزر **إنشاء فاتورة** في صفحة **أمر المبيعات** مخفيًا لأن إنشاء الفواتير سيتم في Supply Chain Management وستتم مزامنتها إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="fb6a6-137">The **Create invoice** button on the **Sales order** page is hidden, because invoices will be created in Supply Chain Management and synchronized to Sales.</span></span> <span data-ttu-id="fb6a6-138">لا تكون صفحة **الفاتورة** قابلة للتحرير، لأن مزامنة الفواتير ستتم من Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="fb6a6-138">The **Invoice** page can't be edited, because invoices will be synchronized from Supply Chain Management.</span></span>
- <span data-ttu-id="fb6a6-139">تتغير **حالة أمر المبيعات** تلقائيًا إلى **مفوتر** عندما تتم مزامنة الفاتورة ذات الصلة من Supply Chain Management إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="fb6a6-139">The **Sales order status** value is automatically changed to **Invoiced** when the related invoice from Supply Chain Management has been synchronized to Sales.</span></span> <span data-ttu-id="fb6a6-140">بالإضافة إلى ذلك، يتم تعيين مالك أمر المبيعات الذي تم إنشاء الفاتورة منه كمالك للفاتورة.</span><span class="sxs-lookup"><span data-stu-id="fb6a6-140">Additionally, the owner of the sales order that the invoice was created from is assigned as the owner of the invoice.</span></span> <span data-ttu-id="fb6a6-141">لذلك، يمكن لمالك أمر المبيعات عرض الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="fb6a6-141">Therefore, the owner of the sales order can view the invoice.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="fb6a6-142">الشروط المسبقة وإعداد التعيين</span><span class="sxs-lookup"><span data-stu-id="fb6a6-142">Preconditions and mapping setup</span></span>

<span data-ttu-id="fb6a6-143">قبل إجراء مزامنة لفواتير المبيعات، لا بد من تحديث الإعدادات التالية في النظام.</span><span class="sxs-lookup"><span data-stu-id="fb6a6-143">Before you synchronize sales invoices, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="fb6a6-144">الإعداد في Sales</span><span class="sxs-lookup"><span data-stu-id="fb6a6-144">Setup in Sales</span></span>

<span data-ttu-id="fb6a6-145">انتقل إلى **الإعدادات** > **الإدارة** > **إعدادات النظام** > **Sales**، وتأكد من أنه يتم استخدام الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="fb6a6-145">Go to **Settings** > **Administration** > **System settings** > **Sales**, and make sure that the following settings are used:</span></span>

- <span data-ttu-id="fb6a6-146">يكون الخيار **‬‏‫استخدام حساب أسعار النظام** معينًا إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="fb6a6-146">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
- <span data-ttu-id="fb6a6-147">يكون الحقل **طريقة حساب الخصم** معينًا إلى **صنف البند**.</span><span class="sxs-lookup"><span data-stu-id="fb6a6-147">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="fb6a6-148">إعداد مشروع تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="fb6a6-148">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="fb6a6-149">SalesInvoiceHeader task</span><span class="sxs-lookup"><span data-stu-id="fb6a6-149">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="fb6a6-150">تأكد من وجود التعيين المطلوب لـ **InvoiceCountryRegionId** إلى **BillingAddress\_Country**.</span><span class="sxs-lookup"><span data-stu-id="fb6a6-150">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country**.</span></span>

    <span data-ttu-id="fb6a6-151">قيمة القالب هي تعيين قيمة حيث يتم تعيين العديد من البلدان أو المناطق.</span><span class="sxs-lookup"><span data-stu-id="fb6a6-151">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="fb6a6-152">تكون قائمة الأسعار مطلوبة لإنشاء الفواتير في Sales.</span><span class="sxs-lookup"><span data-stu-id="fb6a6-152">A price list is required in order to create invoices in Sales.</span></span> <span data-ttu-id="fb6a6-153">حدّث تعيين القيمة لـ **pricelevelid.name \[اسم قائمة الأسعار\]** إلى قائمة الأسعار المستخدمة في Sales لكل عملة.</span><span class="sxs-lookup"><span data-stu-id="fb6a6-153">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="fb6a6-154">يمكنك استخدام قائمة الأسعار الافتراضية لعمله واحدة.</span><span class="sxs-lookup"><span data-stu-id="fb6a6-154">You can use the default price list for a single currency.</span></span> <span data-ttu-id="fb6a6-155">بدلاً من ذلك، إذا كان لديك قوائم أسعار بعملات متعددة، يمكنك استخدام تعيين قيمة.</span><span class="sxs-lookup"><span data-stu-id="fb6a6-155">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="fb6a6-156">قيمة القالب لـ **pricelevelid.name \[اسم قائمة الأسعار\]** هي تعيين قيمة يستند إلى العملة بالدولار الأمريكي = CRM Service USA (نموذج).</span><span class="sxs-lookup"><span data-stu-id="fb6a6-156">The template value for **pricelevelid.name \[Price list name\]** is a value map that is based on currency with USD = CRM Service USA (sample).</span></span>  
    
#### <a name="salesinvoiceline-task"></a><span data-ttu-id="fb6a6-157">مهمة SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="fb6a6-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="fb6a6-158">تأكد من وجود التعيين المطلوب لـ **وحدة القياس**.</span><span class="sxs-lookup"><span data-stu-id="fb6a6-158">Make sure that the required mapping exists for **Unit of measure**.</span></span>
- <span data-ttu-id="fb6a6-159">تأكد من وجود تعيين القيمة المطلوب لـ **SalesUnitSymbol** في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="fb6a6-159">Make sure that the required value map for **SalesUnitSymbol** in Supply Chain Management exists.</span></span>

    <span data-ttu-id="fb6a6-160">يتم تعريف قيمة القالب التي لها تعيين قيمة لـ **SalesUnitSymbol** إلى **Quantity\_UOM**.</span><span class="sxs-lookup"><span data-stu-id="fb6a6-160">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="fb6a6-161">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="fb6a6-161">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="fb6a6-162">لا يتم تضمين الحقول **شروط الدفع** و**شروط الشحن** و**شروط التسليم** و**أسلوب الشحن** و**وضع التسليم** في التعيينات الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="fb6a6-162">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="fb6a6-163">لتعيين هذه الحقول، يجب إعداد تعيين قيمة خاصة بالبيانات الموجودة في المؤسسات التي تتم مزامنة الكيان بينها.</span><span class="sxs-lookup"><span data-stu-id="fb6a6-163">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="fb6a6-164">تبين الأشكال التوضيحية التالية مثالاً لتعيين قالب في تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="fb6a6-164">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="fb6a6-165">يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Sales إلى Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="fb6a6-165">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

### <a name="salesinvoiceheader"></a><span data-ttu-id="fb6a6-166">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="fb6a6-166">SalesInvoiceHeader</span></span>

![تعيين القالب في تكامل البيانات](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a><span data-ttu-id="fb6a6-168">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="fb6a6-168">SalesInvoiceLine</span></span>

![تعيين القالب في تكامل البيانات](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="fb6a6-170">مواضيع مرتبطة</span><span class="sxs-lookup"><span data-stu-id="fb6a6-170">Related topics</span></span>

[<span data-ttu-id="fb6a6-171">العميل المتوقع إلى النقدية</span><span class="sxs-lookup"><span data-stu-id="fb6a6-171">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="fb6a6-172">مزامنة الحسابات مباشرةً من Sales إلى العملاء في Supply Chain Management‎</span><span class="sxs-lookup"><span data-stu-id="fb6a6-172">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="fb6a6-173">مزامنة المنتجات مباشرةً من Supply Chain Management إلى المنتجات في Sales‎‎</span><span class="sxs-lookup"><span data-stu-id="fb6a6-173">Synchronize products directly from Supply Chain Management to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="fb6a6-174">مزامنة جهات الاتصال مباشرةً من Sales إلى جهات الاتصال أو العملاء في Supply Chain Management‎</span><span class="sxs-lookup"><span data-stu-id="fb6a6-174">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="fb6a6-175">مزامنة أوامر المبيعات مباشرة بين Sales وSupply Chain Management</span><span class="sxs-lookup"><span data-stu-id="fb6a6-175">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)
