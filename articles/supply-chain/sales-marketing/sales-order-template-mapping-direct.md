---
title: "مزامنة رؤوس وبنود أوامر المبيعات مباشرةً من Finance and Operations إلى Sales"
description: "يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة رؤوس وبنود أوامر المبيعات مباشرةً من Microsoft Dynamics 365 for Finance and Operations, Enterprise edition إلى Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
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
ms.openlocfilehash: e311b0becbb243cebdc265eccf3059eb46217dee
ms.contentlocale: ar-sa
ms.lasthandoff: 01/17/2018

---

# <a name="synchronize-sales-order-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="18da5-103">مزامنة رؤوس وبنود أوامر المبيعات مباشرةً من Finance and Operations إلى Sales</span><span class="sxs-lookup"><span data-stu-id="18da5-103">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="18da5-104">يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة رؤوس وبنود أوامر المبيعات مباشرةً من Microsoft Dynamics 365 for Finance and Operations, Enterprise edition إلى Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="18da5-104">This topic discusses the templates and underlying tasks that are used to synchronize sales order headers and lines directly from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="18da5-105">تدفق البيانات في حل العميل المتوقع إلى النقدية</span><span class="sxs-lookup"><span data-stu-id="18da5-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="18da5-106">يستخدم حل العميل المتوقع إلى النقدية ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Finance and Operations وSales.</span><span class="sxs-lookup"><span data-stu-id="18da5-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="18da5-107">تسمح قوالب حل العميل المتوقع إلى النقدية المتوفرة مع ميزة تكامل البيانات بتدفق بيانات الحسابات وجهات الاتصال والمنتجات وعروض أسعار المبيعات وأوامر المبيعات وفواتير المبيعات بين Finance and Operations وSales.</span><span class="sxs-lookup"><span data-stu-id="18da5-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="18da5-108">يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات بين Finance and Operations وSales.</span><span class="sxs-lookup"><span data-stu-id="18da5-108">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="18da5-109">[![تدفق البيانات في حل العميل المتوقع إلى النقدية](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="18da5-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="18da5-110">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="18da5-110">Templates and tasks</span></span>

<span data-ttu-id="18da5-111">للوصول إلى القوالب المتوفرة، افتح [مركز إدارة PowerApps](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="18da5-111">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="18da5-112">حدد **المشاريع**، وبعد ذلك، في الزاوية العلوية اليسرى، حدد **مشروع جديد** لتحديد القوالب العامة.</span><span class="sxs-lookup"><span data-stu-id="18da5-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="18da5-113">يتم استخدام القالب والمهام الأساسية التالية لمزامنة رؤوس وبنود أوامر المبيعات من Finance and Operations إلى Sales:</span><span class="sxs-lookup"><span data-stu-id="18da5-113">The following template and underlying tasks are used to synchronize sales order headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="18da5-114">**اسم القالب في تكامل البيانات:** أوامر المبيعات (Fin and Ops إلى Sales)‬ - مباشر</span><span class="sxs-lookup"><span data-stu-id="18da5-114">**Name of the template in Data integration:** Sales Orders (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="18da5-115">**أسماء المهام في مشروع تكامل البيانات:**</span><span class="sxs-lookup"><span data-stu-id="18da5-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="18da5-116">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="18da5-116">OrderHeader</span></span>
    - <span data-ttu-id="18da5-117">OrderLine</span><span class="sxs-lookup"><span data-stu-id="18da5-117">OrderLine</span></span>

<span data-ttu-id="18da5-118">يجب تنفيذ مهام المزامنة التالية قبل حدوث مزامنة رؤوس وبنود فواتير المبيعات.</span><span class="sxs-lookup"><span data-stu-id="18da5-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="18da5-119">‏‫المنتجات (Fin and Ops إلى Sales)‬ - مباشر</span><span class="sxs-lookup"><span data-stu-id="18da5-119">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="18da5-120">الحسابات (Sales إلى Fin and Ops) - مباشر (في حال استخدامها)</span><span class="sxs-lookup"><span data-stu-id="18da5-120">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="18da5-121">جهات الاتصال إلى العملاء (Sales إلى Fin and Ops) - مباشر (في حال استخدامها)</span><span class="sxs-lookup"><span data-stu-id="18da5-121">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="18da5-122">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="18da5-122">Entity set</span></span>

| <span data-ttu-id="18da5-123">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="18da5-123">Finance and Operations</span></span>  | <span data-ttu-id="18da5-124">مبيعات</span><span class="sxs-lookup"><span data-stu-id="18da5-124">Sales</span></span>             |
|-------------------------|-------------------|
| <span data-ttu-id="18da5-125">رؤوس أوامر المبيعات CDS</span><span class="sxs-lookup"><span data-stu-id="18da5-125">CDS sales order headers</span></span> | <span data-ttu-id="18da5-126">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="18da5-126">SalesOrders</span></span>       |
| <span data-ttu-id="18da5-127">بنود أمر مبيعات CDS</span><span class="sxs-lookup"><span data-stu-id="18da5-127">CDS sales order lines</span></span>   | <span data-ttu-id="18da5-128">SalesOrderDetails</span><span class="sxs-lookup"><span data-stu-id="18da5-128">SalesOrderDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="18da5-129">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="18da5-129">Entity flow</span></span>

<span data-ttu-id="18da5-130">يتم إنشاء أوامر المبيعات في Finance and Operations وتتم مزامنتها إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="18da5-130">Sales orders are created in Finance and Operations and synchronized to Sales.</span></span>

<span data-ttu-id="18da5-131">تساعد عوامل التصفية الموجودة في القالب على ضمان عدم تضمين غير أوامر المبيعات ذات الصلة في المزامنة:</span><span class="sxs-lookup"><span data-stu-id="18da5-131">Filters in the template help guarantee that only relevant sales orders are included in the synchronization:</span></span>

- <span data-ttu-id="18da5-132">في أمر المبيعات، سيتم تضمين كل من عميل الأمر وعميل الفوترة اللذين يتم إنشاؤهما من Sales في المزامنة.</span><span class="sxs-lookup"><span data-stu-id="18da5-132">On the sales order, both the ordering customer and the invoicing customer that originate from Sales will be included in the synchronization.</span></span> <span data-ttu-id="18da5-133">في Finance and Operations، يتم استخدام الحقلين **OrderingCustomerIsExternallyMaintained** و**InvoiceCustomerIsExternallyMaintained** لتعقب المزامنة في كيانات البيانات.</span><span class="sxs-lookup"><span data-stu-id="18da5-133">In Finance and Operations, the **OrderingCustomerIsExternallyMaintained** and **InvoiceCustomerIsExternallyMaintained** fields are used to track the synchronization in the data entities.</span></span>
- <span data-ttu-id="18da5-134">يجب تأكيد أمر المبيعات في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="18da5-134">The sales order in Finance and Operations must be confirmed.</span></span> <span data-ttu-id="18da5-135">لا تتم مزامنة غير أوامر المبيعات المؤكدة أو أوامر المبيعات التي لها حالة معالجة أعلى، مثل الحالة **مشحون** أو **مفوتر** إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="18da5-135">Only confirmed sales orders or sales orders that have a higher processing status, such as **Shipped** or **Invoiced**, are synchronized to Sales.</span></span>
- <span data-ttu-id="18da5-136">بعد إنشاء أمر مبيعات أو تعديله، يجب تنفيذ وظيفة الدُفعة **حساب إجماليات المبيعات‬** في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="18da5-136">After a sales order is created or modified, the **Calculate sales totals** batch job in Finance and Operations must be run.</span></span> <span data-ttu-id="18da5-137">لن تتم مزامنة غير أوامر المبيعات التي تم حساب إجماليات المبيعات‬ فيها إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="18da5-137">Only sales orders where sales totals are calculated will be synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="18da5-138">في الوقت الحالي، لا يتم تضمين الضريبة المرتبطة بالتكاليف في رأس أمر المبيعات في المزامنة من Finance and Operations إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="18da5-138">Currently, tax that is related to charges on the sales order header isn't included in the synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="18da5-139">يعود سبب ذلك إلى عدم دعم Sales لمعلومات الضرائب على مستوى الرأس.</span><span class="sxs-lookup"><span data-stu-id="18da5-139">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="18da5-140">ومع ذلك، يتم تضمين الضريبة المرتبطة بالتكاليف على مستوى البند في المزامنة.</span><span class="sxs-lookup"><span data-stu-id="18da5-140">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="18da5-141">حل العميل المتوقع إلى النقدية في Sales</span><span class="sxs-lookup"><span data-stu-id="18da5-141">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="18da5-142">تمت إضافة حقول جديدة إلى كيان **الأمر** وهي تظهر على الصفحة:</span><span class="sxs-lookup"><span data-stu-id="18da5-142">New fields have been added to the **Order** entity and appear on the page:</span></span>

- <span data-ttu-id="18da5-143">**تتم المحافظة عليها خارجيًا‬‏‫‬‏‫** - عيّن هذا الخيار إلى **نعم** عندما يأتي الأمر من Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="18da5-143">**Is Maintained Externally** – Set this option to **Yes** when the order is coming from Finance and Operations.</span></span>
- <span data-ttu-id="18da5-144">**حالة المعالجة** - يستخدم هذا الحقل لعرض حالة معالجة الأمر في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="18da5-144">**Processing status** – This field shows the processing status of the order in Finance and Operations.</span></span> <span data-ttu-id="18da5-145">تتوفر القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="18da5-145">The following values are available:</span></span>

    - <span data-ttu-id="18da5-146">نشط</span><span class="sxs-lookup"><span data-stu-id="18da5-146">Active</span></span>
    - <span data-ttu-id="18da5-147">أوامر المبيعات المؤكدة</span><span class="sxs-lookup"><span data-stu-id="18da5-147">Confirmed</span></span>
    - <span data-ttu-id="18da5-148">كشف التعبئة</span><span class="sxs-lookup"><span data-stu-id="18da5-148">Packing Slip</span></span>
    - <span data-ttu-id="18da5-149">مفوتر</span><span class="sxs-lookup"><span data-stu-id="18da5-149">Invoiced</span></span>
    - <span data-ttu-id="18da5-150">منتقي</span><span class="sxs-lookup"><span data-stu-id="18da5-150">Picked</span></span>
    - <span data-ttu-id="18da5-151">منتقى جزئيًا</span><span class="sxs-lookup"><span data-stu-id="18da5-151">Partially Picked</span></span>
    - <span data-ttu-id="18da5-152">معبأ جزئيًا</span><span class="sxs-lookup"><span data-stu-id="18da5-152">Partially Packed</span></span>
    - <span data-ttu-id="18da5-153">مشحون</span><span class="sxs-lookup"><span data-stu-id="18da5-153">Shipped</span></span>
    - <span data-ttu-id="18da5-154">مشحون جزئيًا</span><span class="sxs-lookup"><span data-stu-id="18da5-154">Partially Shipped</span></span>
    - <span data-ttu-id="18da5-155">مفوتر جزئيًا</span><span class="sxs-lookup"><span data-stu-id="18da5-155">Partially Invoiced</span></span>
    - <span data-ttu-id="18da5-156">تم الإلغاء</span><span class="sxs-lookup"><span data-stu-id="18da5-156">Cancelled</span></span>

<span data-ttu-id="18da5-157">يُستخدم الإعداد **لديه منتجات تتم المحافظة عليها خارجيًا فقط** في سيناريوهات أخرى لأوامر المبيعات (على سبيل المثال، مزامنة من Sales إلى Finance and Operations) للتحقق بشكل مستمر مما إذا كان أمر المبيعات يتكوّن بكامله من منتجات تتم المحافظة عليها خارجيًا.‬</span><span class="sxs-lookup"><span data-stu-id="18da5-157">The **Has Externally Maintained Products Only** setting is used in other sales order scenarios (for example, synchronization from Sales to Finance and Operation) to consistently track whether a sales order consists entirely of externally maintained products.</span></span> <span data-ttu-id="18da5-158">إذا كان أمر المبيعات يتكوّن بكامله من منتجات تتم المحافظة عليها خارجيًا، فستتم المحافظة على المنتجات في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="18da5-158">If a sales order consists entirely of externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="18da5-159">يساعد هذا الإعداد على ضمان عدم محاولة مزامنة بنود أوامر المبيعات التي تشتمل على منتجات غير معروفة إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="18da5-159">This setting helps guarantee that you don't try to synchronize sales order lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="18da5-160">تكون الأزرار **إنشاء فاتورة** و**إلغاء الأمر** و**إعادة الحساب** و**الحصول على منتجات** و**البحث عن عنوان** في صفحة **أمر المبيعات** مخفية للأوامر التي تتم المحافظة عليها خارجيًا إذ سيتم إنشاء الفواتير في Finance and Operations وستتم مزامنتها إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="18da5-160">The **Create Invoice**, **Cancel Order**, **Recalculate**, **Get Products**, and **Lookup Address** buttons on the **Sales order** page are hidden for externally maintained orders, because invoices will be created in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="18da5-161">لا يمكن تحرير صفحة الأمر، لأنه ستتم مزامنة معلومات أمر المبيعات من Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="18da5-161">The order page can't be edited, because sales order information will be synchronized from Finance and Operations.</span></span>

<span data-ttu-id="18da5-162">ستبقى حالة أمر المبيعات **نشط** للمساعدة في ضمان إمكانية انسياب التغييرات من Finance and Operations إلى أمر المبيعات في Sales.</span><span class="sxs-lookup"><span data-stu-id="18da5-162">The status of a sales order will remain **Active** to help guarantee that changes from Finance and Operations can flow to the sales order in Sales.</span></span> <span data-ttu-id="18da5-163">للتحكم في هذا السلوك، قم بتعيين الإعداد الافتراضي **Statecode \[الحالة\]** إلى **نشط** في مشروع تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="18da5-163">To control this behavior, set the default **Statecode \[Status\]** value to **Active** in the Data integration project.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="18da5-164">الشروط المسبقة وإعداد التعيين</span><span class="sxs-lookup"><span data-stu-id="18da5-164">Preconditions and mapping setup</span></span>

<span data-ttu-id="18da5-165">قبل إجراء مزامنة لأوامر المبيعات، لا بد من تحديث الإعدادات التالية في النظام.</span><span class="sxs-lookup"><span data-stu-id="18da5-165">Before you synchronize sales orders, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="18da5-166">الإعداد في Sales</span><span class="sxs-lookup"><span data-stu-id="18da5-166">Setup in Sales</span></span>

- <span data-ttu-id="18da5-167">تأكد من إعداد الأذونات للفريق الذي تم تعيين المستخدم من إعداد الاتصال في Sales إليه.</span><span class="sxs-lookup"><span data-stu-id="18da5-167">Make sure that permissions are set up for the team that the user from your Sales connection set is assigned to.</span></span> <span data-ttu-id="18da5-168">إذا كنت تستخدم بيانات العرض التوضيحي، فعادة ما يكون لدى المستخدم حق وصول المسؤول، ولكن هذا الحق لا يتوفر للفريق.</span><span class="sxs-lookup"><span data-stu-id="18da5-168">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="18da5-169">إذا لم يكن لدى الفريق حق وصول المسؤول أيضًا، عند تشغيل المشروع من تكامل البيانات، فسوف تتلقى رسالة خطأ تفيد بأن الفريق الرئيسي مفقود.</span><span class="sxs-lookup"><span data-stu-id="18da5-169">If the team doesn't also have admin access, when you run the project from Data integration, you will receive an error message that states that Principal team is missing.</span></span>

    <span data-ttu-id="18da5-170">انتقل إلى **‎الإعدادات** > **الأمان** > **الفرق**، حدد الفريق المناسب، وحدد **إدارة الأدوار**‎، ثم حدد دورًا يملك الأذونات المطلوبة على سبيل المثال، **مسؤول النظام**.</span><span class="sxs-lookup"><span data-stu-id="18da5-170">Go to **Settings** > **Security** > **Teams**, select the relevant team, select **Manage Roles**, and select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="18da5-171">انتقل إلى **الإعدادات** > **الإدارة** > **إعدادات النظام** > **Sales**، وتأكد من أنه يتم استخدام الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="18da5-171">Go to **Settings** > **Administration** > **System settings** > **Sales**, and makes sure that the following settings are used:</span></span>

    - <span data-ttu-id="18da5-172">يكون الخيار **‬‏‫استخدام حساب أسعار النظام** معينًا إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="18da5-172">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="18da5-173">يكون الحقل **طريقة حساب الخصم** معينًا إلى **صنف البند**.</span><span class="sxs-lookup"><span data-stu-id="18da5-173">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="18da5-174">الإعداد في Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="18da5-174">Setup in Finance and Operations</span></span>

<span data-ttu-id="18da5-175">انتقل إلى **المبيعات والتسويق** > **المهام الدورية** > **حساب إجماليات المبيعات**‎، وعيِّن الوظيفة لتشغيلها كوظيفة دُفعة.</span><span class="sxs-lookup"><span data-stu-id="18da5-175">Go to **Sales and marketing** > **Periodic tasks** > **Calculate sales totals**, and set the job to run as a batch job.</span></span> <span data-ttu-id="18da5-176">عيّن الخيار **‏‫حساب إجماليات أوامر المبيعات‬** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="18da5-176">Set the **Calculate totals for sales orders** option to **Yes**.</span></span> <span data-ttu-id="18da5-177">‏‫تعد هذه الخطوة هامة لأن أوامر المبيعات التي تم حساب إجماليات المبيعات‬ فيها هي فقط أوامر المبيعات التي ستتم مزامنتها إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="18da5-177">This step is important, because only sales orders where sales totals are calculated will be synchronized to Sales.</span></span> <span data-ttu-id="18da5-178">يجب أن يكون مدى تكرار وظيفة الدُفعة متوافقًا مع مدى تكرار مزامنة أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="18da5-178">The frequency of the batch job should be aligned with the frequency of sales order synchronization.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="18da5-179">إعداد مشروع تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="18da5-179">Setup in the Data integration project</span></span>

#### <a name="salesheader-task"></a><span data-ttu-id="18da5-180">مهمة SalesHeader</span><span class="sxs-lookup"><span data-stu-id="18da5-180">SalesHeader task</span></span>

- <span data-ttu-id="18da5-181">تأكد من وجود التعيين المطلوب لـ **InvoiceCountryRegionId** إلى **BillingAddress\_Country** ولـ **DeliveryCountryRegionId** إلى **DeliveryAddress\_Country**.</span><span class="sxs-lookup"><span data-stu-id="18da5-181">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country** and for **DeliveryCountryRegionId** to **DeliveryAddress\_Country**.</span></span>

    <span data-ttu-id="18da5-182">قيمة القالب هي تعيين قيمة حيث يتم تعيين العديد من البلدان أو المناطق.</span><span class="sxs-lookup"><span data-stu-id="18da5-182">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="18da5-183">تكون قائمة الأسعار مطلوبة لإنشاء الأوامر في Sales.</span><span class="sxs-lookup"><span data-stu-id="18da5-183">A price list is required in order to create orders in Sales.</span></span> <span data-ttu-id="18da5-184">حدّث تعيين القيمة لـ **pricelevelid.name \[اسم قائمة الأسعار\]** إلى قائمة الأسعار المستخدمة في Sales لكل عملة.</span><span class="sxs-lookup"><span data-stu-id="18da5-184">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="18da5-185">يمكنك استخدام قائمة الأسعار الافتراضية لعمله واحدة.</span><span class="sxs-lookup"><span data-stu-id="18da5-185">You can use the default price list for a single currency.</span></span> <span data-ttu-id="18da5-186">بدلاً من ذلك، إذا كان لديك قوائم أسعار بعملات متعددة، يمكنك استخدام تعيين قيمة.</span><span class="sxs-lookup"><span data-stu-id="18da5-186">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="18da5-187">قيمة القالب الافتراضية لـ **pricelevelid.name \[اسم قائمة الأسعار\]** تكون **CRM Service USA (نموذج)**.</span><span class="sxs-lookup"><span data-stu-id="18da5-187">The default template value for **pricelevelid.name \[Price list name\]** is **CRM Service USA (sample)**.</span></span>

#### <a name="salesline-task"></a><span data-ttu-id="18da5-188">مهمة SalesLine</span><span class="sxs-lookup"><span data-stu-id="18da5-188">SalesLine task</span></span>

- <span data-ttu-id="18da5-189">تأكد من وجود التعيين المطلوب لـ **DeliveryCountryRegionId** إلى **DeliveryAddress\_Country**.</span><span class="sxs-lookup"><span data-stu-id="18da5-189">Make sure that the required mapping exists for **DeliveryCountryRegionId** to **DeliveryAddress\_Country**.</span></span>

    <span data-ttu-id="18da5-190">قيمة القالب هي تعيين قيمة حيث يتم تعيين العديد من البلدان أو المناطق.</span><span class="sxs-lookup"><span data-stu-id="18da5-190">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="18da5-191">تأكد من وجود تعيين القيمة المطلوب لـ **SalesUnitSymbol** في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="18da5-191">Make sure that the required value map for **SalesUnitSymbol** in Finance and Operations exists.</span></span>

    <span data-ttu-id="18da5-192">يتم تعريف قيمة القالب التي لها تعيين قيمة لـ **SalesUnitSymbol** إلى **Quantity\_UOM**.</span><span class="sxs-lookup"><span data-stu-id="18da5-192">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="18da5-193">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="18da5-193">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="18da5-194">لا يتم تضمين الحقول **شروط الدفع** و**شروط الشحن** و**شروط التسليم** و**أسلوب الشحن** و**وضع التسليم** في التعيينات الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="18da5-194">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="18da5-195">لتعيين هذه الحقول، يجب إعداد تعيين قيمة خاصة بالبيانات الموجودة في المؤسسات التي تتم مزامنة الكيان بينها.</span><span class="sxs-lookup"><span data-stu-id="18da5-195">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="18da5-196">تبين الأشكال التوضيحية التالية مثالاً لتعيين قالب في تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="18da5-196">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="18da5-197">يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Sales إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="18da5-197">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="orderheader"></a><span data-ttu-id="18da5-198">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="18da5-198">OrderHeader</span></span>

![تعيين القالب في موحد البيانات](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="orderline"></a><span data-ttu-id="18da5-200">OrderLine</span><span class="sxs-lookup"><span data-stu-id="18da5-200">OrderLine</span></span>

![تعيين القالب في موحد البيانات](./media/sales-order-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="18da5-202">مواضيع مرتبطة</span><span class="sxs-lookup"><span data-stu-id="18da5-202">Related topics</span></span>

[<span data-ttu-id="18da5-203">العميل المتوقع إلى النقدية</span><span class="sxs-lookup"><span data-stu-id="18da5-203">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="18da5-204">مزامنة الحسابات مباشرةً من Sales للعملاء في Finance and Operations‎</span><span class="sxs-lookup"><span data-stu-id="18da5-204">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="18da5-205">مزامنة المنتجات مباشرةً من Finance and Operations للمنتجات في Sales‎</span><span class="sxs-lookup"><span data-stu-id="18da5-205">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="18da5-206">مزامنة جهات الاتصال مباشرةً من Sales لجهات الاتصال في Finance and Operations‎</span><span class="sxs-lookup"><span data-stu-id="18da5-206">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="18da5-207">مزامنة رؤوس وبنود فواتير المبيعات مباشرةً من Finance and Operations إلى Sales</span><span class="sxs-lookup"><span data-stu-id="18da5-207">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)




