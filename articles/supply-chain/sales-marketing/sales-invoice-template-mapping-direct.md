---
title: "مزامنة رؤوس وبنود فواتير المبيعات مباشرةً من Finance and Operations إلى Sales"
description: "يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة رؤوس وبنود فواتير المبيعات مباشرةً من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Sales."
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
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: afbf4a24b737cf7221bac4b688b8801b1bcd839c
ms.contentlocale: ar-sa
ms.lasthandoff: 03/26/2018

---

# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="e8902-103">مزامنة رؤوس وبنود فواتير المبيعات مباشرةً من Finance and Operations إلى Sales</span><span class="sxs-lookup"><span data-stu-id="e8902-103">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e8902-104">يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة رؤوس وبنود فواتير المبيعات مباشرةً من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="e8902-104">This topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines directly from Microsoft Dynamics 365 for Finance and Operations, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="e8902-105">تدفق البيانات في حل العميل المتوقع إلى النقدية</span><span class="sxs-lookup"><span data-stu-id="e8902-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="e8902-106">يستخدم حل العميل المتوقع إلى النقدية ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Finance and Operations وSales.</span><span class="sxs-lookup"><span data-stu-id="e8902-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="e8902-107">تسمح قوالب حل العميل المتوقع إلى النقدية المتوفرة مع ميزة تكامل البيانات بتدفق بيانات الحسابات وجهات الاتصال والمنتجات وعروض أسعار المبيعات وأوامر المبيعات وفواتير المبيعات بين Finance and Operations وSales.</span><span class="sxs-lookup"><span data-stu-id="e8902-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="e8902-108">يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات بين Finance and Operations وSales.</span><span class="sxs-lookup"><span data-stu-id="e8902-108">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="e8902-109">[![تدفق البيانات في حل العميل المتوقع إلى النقدية](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="e8902-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="e8902-110">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="e8902-110">Templates and tasks</span></span>

<span data-ttu-id="e8902-111">للوصول إلى القوالب المتوفرة، افتح [مركز إدارة PowerApps](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="e8902-111">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="e8902-112">حدد **المشاريع**، وبعد ذلك، في الزاوية العلوية اليسرى، حدد **مشروع جديد** لتحديد القوالب العامة.</span><span class="sxs-lookup"><span data-stu-id="e8902-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="e8902-113">يتم استخدام القالب والمهام الأساسية التالية لمزامنة رؤوس وبنود فواتير المبيعات من Finance and Operations إلى Sales:</span><span class="sxs-lookup"><span data-stu-id="e8902-113">The following template and underlying tasks are used to synchronize sales invoice headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="e8902-114">**اسم القالب في تكامل البيانات:** فواتير المبيعات (Fin and Ops إلى Sales)‬ - مباشر</span><span class="sxs-lookup"><span data-stu-id="e8902-114">**Name of the template in Data integration:** Sales Invoices (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="e8902-115">**أسماء المهام في مشروع تكامل البيانات:**</span><span class="sxs-lookup"><span data-stu-id="e8902-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="e8902-116">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="e8902-116">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="e8902-117">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="e8902-117">SalesInvoiceLine</span></span>

<span data-ttu-id="e8902-118">يجب تنفيذ مهام المزامنة التالية قبل حدوث مزامنة رؤوس وبنود فواتير المبيعات.</span><span class="sxs-lookup"><span data-stu-id="e8902-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="e8902-119">‏‫المنتجات (Fin and Ops إلى Sales)‬ - مباشر</span><span class="sxs-lookup"><span data-stu-id="e8902-119">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="e8902-120">الحسابات (Sales إلى Fin and Ops) - مباشر (في حال استخدامها)</span><span class="sxs-lookup"><span data-stu-id="e8902-120">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="e8902-121">جهات الاتصال (Sales إلى Fin and Ops) - مباشر (في حال استخدامها)</span><span class="sxs-lookup"><span data-stu-id="e8902-121">Contacts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="e8902-122">رأس وبنود أوامر المبيعات (Fin and Ops إلى Sales) - مباشر</span><span class="sxs-lookup"><span data-stu-id="e8902-122">Sales order header and lines (Fin and Ops to Sales) - Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="e8902-123">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="e8902-123">Entity set</span></span>

| <span data-ttu-id="e8902-124">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e8902-124">Finance and Operations</span></span>                               | <span data-ttu-id="e8902-125">مبيعات</span><span class="sxs-lookup"><span data-stu-id="e8902-125">Sales</span></span>          |
|------------------------------------------------------|----------------|
| <span data-ttu-id="e8902-126">رؤوس فواتير مبيعات العملاء التي تم الاحتفاظ بها خارجيًا</span><span class="sxs-lookup"><span data-stu-id="e8902-126">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="e8902-127">الفواتير</span><span class="sxs-lookup"><span data-stu-id="e8902-127">Invoices</span></span>       |
| <span data-ttu-id="e8902-128">بنود فواتير مبيعات العملاء التي تم الاحتفاظ بها خارجيًا</span><span class="sxs-lookup"><span data-stu-id="e8902-128">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="e8902-129">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="e8902-129">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="e8902-130">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="e8902-130">Entity flow</span></span>

<span data-ttu-id="e8902-131">يتم إنشاء فواتير المبيعات في Finance and Operations وتتم مزامنتها إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="e8902-131">Sales invoices are created in Finance and Operations and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="e8902-132">في الوقت الحالي، لا يتم تضمين الضريبة المرتبطة بالتكاليف في رأس فاتورة المبيعات في المزامنة من Finance and Operations إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="e8902-132">Currently, tax that is related to charges on the sales invoice header isn't included in the synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="e8902-133">يعود سبب ذلك إلى عدم دعم Sales لمعلومات الضرائب على مستوى الرأس.</span><span class="sxs-lookup"><span data-stu-id="e8902-133">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="e8902-134">ومع ذلك، يتم تضمين الضريبة المرتبطة بالتكاليف على مستوى البند في المزامنة.</span><span class="sxs-lookup"><span data-stu-id="e8902-134">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="e8902-135">حل العميل المتوقع إلى النقدية في Sales</span><span class="sxs-lookup"><span data-stu-id="e8902-135">Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="e8902-136">تمت إضافة حقل **رقم الفاتورة** إلى كيان **الفاتورة** ويتم عرضه على الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e8902-136">An **Invoice number** field has been added to the **Invoice** entity and appears on the page.</span></span>
- <span data-ttu-id="e8902-137">يكون الزر **إنشاء فاتورة** في صفحة **أمر المبيعات** مخفيًا لأن إنشاء الفواتير سيتم في Finance and Operations وستتم مزامنتها إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="e8902-137">The **Create invoice** button on the **Sales order** page is hidden, because invoices will be created in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="e8902-138">لا تكون صفحة **الفاتورة** قابلة للتحرير لأن مزامنة الفواتير ستتم من Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e8902-138">The **Invoice** page can't be edited, because invoices will be synchronized from Finance and Operations.</span></span>
- <span data-ttu-id="e8902-139">تتغير **حالة أمر المبيعات** تلقائيًا إلى **مفوتر** عندما تتم مزامنة الفاتورة ذات الصلة من Finance and Operations إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="e8902-139">The **Sales order status** value is automatically changed to **Invoiced** when the related invoice from Finance and Operations has been synchronized to Sales.</span></span> <span data-ttu-id="e8902-140">بالإضافة إلى ذلك، يتم تعيين مالك أمر المبيعات الذي تم إنشاء الفاتورة منه كمالك للفاتورة.</span><span class="sxs-lookup"><span data-stu-id="e8902-140">Additionally, the owner of the sales order that the invoice was created from is assigned as the owner of the invoice.</span></span> <span data-ttu-id="e8902-141">لذلك، يمكن لمالك أمر المبيعات عرض الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="e8902-141">Therefore, the owner of the sales order can view the invoice.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="e8902-142">الشروط المسبقة وإعداد التعيين</span><span class="sxs-lookup"><span data-stu-id="e8902-142">Preconditions and mapping setup</span></span>

<span data-ttu-id="e8902-143">قبل إجراء مزامنة لفواتير المبيعات، لا بد من تحديث الإعدادات التالية في النظام.</span><span class="sxs-lookup"><span data-stu-id="e8902-143">Before you synchronize sales invoices, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="e8902-144">الإعداد في Sales</span><span class="sxs-lookup"><span data-stu-id="e8902-144">Setup in Sales</span></span>

<span data-ttu-id="e8902-145">انتقل إلى **الإعدادات** > **الإدارة** > **إعدادات النظام** > **Sales**، وتأكد من أنه يتم استخدام الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="e8902-145">Go to **Settings** > **Administration** > **System settings** > **Sales**, and make sure that the following settings are used:</span></span>

- <span data-ttu-id="e8902-146">يكون الخيار **‬‏‫استخدام حساب أسعار النظام** معينًا إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="e8902-146">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
- <span data-ttu-id="e8902-147">يكون الحقل **طريقة حساب الخصم** معينًا إلى **صنف البند**.</span><span class="sxs-lookup"><span data-stu-id="e8902-147">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="e8902-148">إعداد مشروع تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="e8902-148">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="e8902-149">SalesInvoiceHeader task</span><span class="sxs-lookup"><span data-stu-id="e8902-149">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="e8902-150">تأكد من وجود التعيين المطلوب لـ **InvoiceCountryRegionId** إلى **BillingAddress\_Country**.</span><span class="sxs-lookup"><span data-stu-id="e8902-150">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country**.</span></span>

    <span data-ttu-id="e8902-151">قيمة القالب هي تعيين قيمة حيث يتم تعيين العديد من البلدان أو المناطق.</span><span class="sxs-lookup"><span data-stu-id="e8902-151">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="e8902-152">تكون قائمة الأسعار مطلوبة لإنشاء الفواتير في Sales.</span><span class="sxs-lookup"><span data-stu-id="e8902-152">A price list is required in order to create invoices in Sales.</span></span> <span data-ttu-id="e8902-153">حدّث تعيين القيمة لـ **pricelevelid.name \[اسم قائمة الأسعار\]** إلى قائمة الأسعار المستخدمة في Sales لكل عملة.</span><span class="sxs-lookup"><span data-stu-id="e8902-153">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="e8902-154">يمكنك استخدام قائمة الأسعار الافتراضية لعمله واحدة.</span><span class="sxs-lookup"><span data-stu-id="e8902-154">You can use the default price list for a single currency.</span></span> <span data-ttu-id="e8902-155">بدلاً من ذلك، إذا كان لديك قوائم أسعار بعملات متعددة، يمكنك استخدام تعيين قيمة.</span><span class="sxs-lookup"><span data-stu-id="e8902-155">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="e8902-156">قيمة القالب لـ **pricelevelid.name \[اسم قائمة الأسعار\]** هي تعيين قيمة يستند إلى العملة بالدولار الأمريكي = CRM Service USA (نموذج).</span><span class="sxs-lookup"><span data-stu-id="e8902-156">The template value for **pricelevelid.name \[Price list name\]** is a value map that is based on currency with USD = CRM Service USA (sample).</span></span>  
    
#### <a name="salesinvoiceline-task"></a><span data-ttu-id="e8902-157">مهمة SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="e8902-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="e8902-158">تأكد من وجود التعيين المطلوب لـ **وحدة القياس**.</span><span class="sxs-lookup"><span data-stu-id="e8902-158">Make sure that the required mapping exists for **Unit of measure**.</span></span>
- <span data-ttu-id="e8902-159">تأكد من وجود تعيين القيمة المطلوب لـ **SalesUnitSymbol** في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e8902-159">Make sure that the required value map for **SalesUnitSymbol** in Finance and Operations exists.</span></span>

    <span data-ttu-id="e8902-160">يتم تعريف قيمة القالب التي لها تعيين قيمة لـ **SalesUnitSymbol** إلى **Quantity\_UOM**.</span><span class="sxs-lookup"><span data-stu-id="e8902-160">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="e8902-161">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="e8902-161">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="e8902-162">لا يتم تضمين الحقول **شروط الدفع** و**شروط الشحن** و**شروط التسليم** و**أسلوب الشحن** و**وضع التسليم** في التعيينات الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="e8902-162">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="e8902-163">لتعيين هذه الحقول، يجب إعداد تعيين قيمة خاصة بالبيانات الموجودة في المؤسسات التي تتم مزامنة الكيان بينها.</span><span class="sxs-lookup"><span data-stu-id="e8902-163">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="e8902-164">تبين الأشكال التوضيحية التالية مثالاً لتعيين قالب في تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="e8902-164">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="e8902-165">يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Sales إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e8902-165">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="salesinvoiceheader"></a><span data-ttu-id="e8902-166">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="e8902-166">SalesInvoiceHeader</span></span>

![تعيين القالب في تكامل البيانات](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a><span data-ttu-id="e8902-168">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="e8902-168">SalesInvoiceLine</span></span>

![تعيين القالب في تكامل البيانات](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="e8902-170">مواضيع مرتبطة</span><span class="sxs-lookup"><span data-stu-id="e8902-170">Related topics</span></span>

[<span data-ttu-id="e8902-171">العميل المتوقع إلى النقدية</span><span class="sxs-lookup"><span data-stu-id="e8902-171">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="e8902-172">مزامنة الحسابات مباشرةً من Sales للعملاء في Finance and Operations‎</span><span class="sxs-lookup"><span data-stu-id="e8902-172">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="e8902-173">مزامنة المنتجات مباشرةً من Finance and Operations إلى المنتجات في Sales‎</span><span class="sxs-lookup"><span data-stu-id="e8902-173">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="e8902-174">مزامنة جهات الاتصال مباشرةً من Sales إلى جهات الاتصال في Finance and Operations‎</span><span class="sxs-lookup"><span data-stu-id="e8902-174">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="e8902-175">مزامنة رؤوس وبنود أوامر المبيعات مباشرةً من Finance and Operations إلى Sales</span><span class="sxs-lookup"><span data-stu-id="e8902-175">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)







