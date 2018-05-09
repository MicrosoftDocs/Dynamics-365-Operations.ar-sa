---
title: "مزامنة أوامر المبيعات مباشرةً بين Finance and Operations وSales"
description: "يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لتشغيل مزامنة أوامر المبيعات مباشرةً بين Microsoft Dynamics 365 for Sales وMicrosoft Dynamics 365 for Finance and Operations."
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2018
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 089f429357ca3adefdc4e444abde3715aed979c3
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---

# <a name="synchronization-of-sales-orders-directly-between-sales-and-finance-and-operations"></a><span data-ttu-id="711c5-103">مزامنة أوامر المبيعات مباشرةً بين Finance and Operations وSales</span><span class="sxs-lookup"><span data-stu-id="711c5-103">Synchronization of sales orders directly between Sales and Finance and Operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="711c5-104">يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لتشغيل مزامنة أوامر المبيعات مباشرةً بين Microsoft Dynamics 365 for Sales وMicrosoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="711c5-104">The topic discusses the templates and underlying tasks that are used to run synchronization of sales orders directly between Microsoft Dynamics 365 for Sales and Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="711c5-105">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="711c5-105">Templates and tasks</span></span>

<span data-ttu-id="711c5-106">للوصول إلى القوالب المتوفرة، افتح [مركز إدارة PowerApps](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="711c5-106">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="711c5-107">حدد **المشاريع**، وبعد ذلك، في الزاوية العلوية اليسرى، حدد **مشروع جديد** لتحديد القوالب العامة.</span><span class="sxs-lookup"><span data-stu-id="711c5-107">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="711c5-108">يتم استخدام القوالب والمهام الأساسية التالية لتشغيل مزامنة أوامر المبيعات مباشرةً بين Sales وFinance and Operations:</span><span class="sxs-lookup"><span data-stu-id="711c5-108">The following templates and underlying tasks are used to run synchronization of sales orders directly between Sales and Finance and Operations:</span></span>

- <span data-ttu-id="711c5-109">**أسماء القوالب في تكامل البيانات:**</span><span class="sxs-lookup"><span data-stu-id="711c5-109">**Names of the templates in Data integration:**</span></span> 

    - <span data-ttu-id="711c5-110">أوامر المبيعات (Sales إلى Fin and Ops) - مباشر</span><span class="sxs-lookup"><span data-stu-id="711c5-110">Sales Orders (Sales to Fin and Ops) - Direct</span></span>
    - <span data-ttu-id="711c5-111">أوامر المبيعات (Fin and Ops إلى Sales) - مباشر</span><span class="sxs-lookup"><span data-stu-id="711c5-111">Sales Orders (Fin and Ops to Sales) - Direct</span></span>

- <span data-ttu-id="711c5-112">**أسماء المهام في مشروع تكامل البيانات:**</span><span class="sxs-lookup"><span data-stu-id="711c5-112">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="711c5-113">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="711c5-113">OrderHeader</span></span>
    - <span data-ttu-id="711c5-114">OrderLine</span><span class="sxs-lookup"><span data-stu-id="711c5-114">OrderLine</span></span>

<span data-ttu-id="711c5-115">يجب تنفيذ مهام المزامنة التالية قبل حدوث مزامنة رؤوس وبنود فواتير المبيعات.</span><span class="sxs-lookup"><span data-stu-id="711c5-115">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="711c5-116">‏‫المنتجات (Fin and Ops إلى Sales)‬ - مباشر</span><span class="sxs-lookup"><span data-stu-id="711c5-116">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="711c5-117">الحسابات (Sales إلى Fin and Ops) - مباشر (في حال استخدامها)</span><span class="sxs-lookup"><span data-stu-id="711c5-117">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="711c5-118">جهات الاتصال إلى العملاء (Sales إلى Fin and Ops) - مباشر (في حال استخدامها)</span><span class="sxs-lookup"><span data-stu-id="711c5-118">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="711c5-119">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="711c5-119">Entity set</span></span>

| <span data-ttu-id="711c5-120">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="711c5-120">Finance and Operations</span></span>  | <span data-ttu-id="711c5-121">مبيعات</span><span class="sxs-lookup"><span data-stu-id="711c5-121">Sales</span></span>             |
|-------------------------|-------------------|
| <span data-ttu-id="711c5-122">رؤوس أوامر المبيعات CDS</span><span class="sxs-lookup"><span data-stu-id="711c5-122">CDS sales order headers</span></span> | <span data-ttu-id="711c5-123">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="711c5-123">SalesOrders</span></span>       |
| <span data-ttu-id="711c5-124">بنود أمر مبيعات CDS</span><span class="sxs-lookup"><span data-stu-id="711c5-124">CDS sales order lines</span></span>   | <span data-ttu-id="711c5-125">SalesOrderDetails</span><span class="sxs-lookup"><span data-stu-id="711c5-125">SalesOrderDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="711c5-126">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="711c5-126">Entity flow</span></span>

<span data-ttu-id="711c5-127">‏‫يتم إنشاء أوامر المبيعات في Sales وتتم مزامنتها إلى Finance and Operations عند **تشغيل المشروع** لأحد المشاريع استنادًا إلى القالب **أوامر المبيعات (Sales إلى Fin and Ops) - مباشر**.</span><span class="sxs-lookup"><span data-stu-id="711c5-127">Sales orders are created in Sales and synchronized to Finance and Operations when **Run project** is triggered for a project based on the **Sales Orders (Sales to Fin and Ops) - Direct** template.</span></span> <span data-ttu-id="711c5-128">لا يمكنك تنشيط ومزامنة الأوامر من Sales إلا إذا كانت جميع **منتجات الأوامر** تتكون من المنتجات التي تتم المحافظة عليها خارجيًا.</span><span class="sxs-lookup"><span data-stu-id="711c5-128">You can only activate and synchronize orders from Sales if all **Order Products** consist of products that are externally maintained.</span></span> <span data-ttu-id="711c5-129">لذلك، قد لا يكون هناك أي منتجات مدونة.</span><span class="sxs-lookup"><span data-stu-id="711c5-129">Therefore, there can be no write-in products.</span></span> <span data-ttu-id="711c5-130">بعد تنشيط الأمر، يصبح أمر المبيعات للقراءة فقط في واجهة المستخدم (UI).</span><span class="sxs-lookup"><span data-stu-id="711c5-130">After the order is activated, the sales order becomes read-only in the user interface (UI).</span></span> <span data-ttu-id="711c5-131">عند هذه النقطة، يتم إجراء التحديثات من Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="711c5-131">At that point, the updates are made from Finance and Operations.</span></span> <span data-ttu-id="711c5-132">بعد حصول أمر المبيعات على الحالة **مؤكد**، يمكن استخدام المشروع الذي يستند القالب **أوامر المبيعات (Fin and Ops إلى Sales) - مباشر** لمزامنة التحديثات أو حالة الاستيفاء من Finance and Operations إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="711c5-132">After the sales order has a status of **Confirmed**, the a project based on the **Sales Orders (Fin and Ops to Sales) - Direct** template can be used to synchronize updates or fulfillment status from Finance and Operations to Sales.</span></span>

<span data-ttu-id="711c5-133">لا يتعين عليك إنشاء الأوامر في Sales.</span><span class="sxs-lookup"><span data-stu-id="711c5-133">You don't have to create orders in Sales.</span></span> <span data-ttu-id="711c5-134">يمكنك إنشاء أوامر المبيعات الجديدة في Finance and Operations بدلاً من ذلك.</span><span class="sxs-lookup"><span data-stu-id="711c5-134">You can create new sales orders in Finance and Operations instead.</span></span> <span data-ttu-id="711c5-135">بعد حصول أمر المبيعات على الحالة **مؤكد**، تتم مزامنته إلى Sales كما هو موضح في الفقرة السابقة.</span><span class="sxs-lookup"><span data-stu-id="711c5-135">After a sales order has a status of **Confirmed**, it's synchronized to Sales as described in the previous paragraph.</span></span>

<span data-ttu-id="711c5-136">في Finance and operations، تساعد عوامل التصفية الموجودة في القالب على ضمان عدم تضمين غير أوامر المبيعات ذات الصلة في المزامنة:</span><span class="sxs-lookup"><span data-stu-id="711c5-136">In Finance and operations, filters in the template help guarantee that only the relevant sales orders are included in the synchronization:</span></span>

- <span data-ttu-id="711c5-137">في أمر المبيعات، يجب إنشاء كل من عميل الأمر وعميل الفوترة من Sales ليتم تضمينه في المزامنة.</span><span class="sxs-lookup"><span data-stu-id="711c5-137">On the sales order, both the ordering customer and the invoicing customer have to originate from Sales to be included in the synchronization.</span></span> <span data-ttu-id="711c5-138">في Finance and Operations، يتم استخدام الحقلين **OrderingCustomerIsExternallyMaintained** و**InvoiceCustomerIsExternallyMaintained** لتصفية أوامر المبيعات من كيانات البيانات.</span><span class="sxs-lookup"><span data-stu-id="711c5-138">In Finance and Operations, the **OrderingCustomerIsExternallyMaintained** and **InvoiceCustomerIsExternallyMaintained** fields are used to filter sales orders from the data entities.</span></span>
- <span data-ttu-id="711c5-139">يجب تأكيد أمر المبيعات في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="711c5-139">The sales order in Finance and Operations must be confirmed.</span></span> <span data-ttu-id="711c5-140">لا تتم مزامنة غير أوامر المبيعات المؤكدة أو أوامر المبيعات التي لها حالة معالجة أعلى، مثل الحالة **مشحون** أو **مفوتر** إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="711c5-140">Only confirmed sales orders or sales orders that have a higher processing status, such as **Shipped** or **Invoiced**, are synchronized to Sales.</span></span>
- <span data-ttu-id="711c5-141">بعد إنشاء أمر مبيعات أو تعديله، يجب تنفيذ وظيفة الدُفعة **حساب إجماليات المبيعات‬** في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="711c5-141">After a sales order is created or modified, the **Calculate sales totals** batch job in Finance and Operations must be run.</span></span> <span data-ttu-id="711c5-142">لن تتم مزامنة غير أوامر المبيعات التي تم حساب إجماليات المبيعات‬ فيها إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="711c5-142">Only sales orders where sales totals are calculated will be synchronized to Sales.</span></span>

## <a name="freight-tax"></a><span data-ttu-id="711c5-143">ضريبة الشحن</span><span class="sxs-lookup"><span data-stu-id="711c5-143">Freight tax</span></span>

<span data-ttu-id="711c5-144">لا يدعم Sales الضريبة على مستوى الرأس، لأنه يتم تخزين الضريبة على مستوى البند.</span><span class="sxs-lookup"><span data-stu-id="711c5-144">Sales doesn't support tax at the header level, because tax is stored at the line level.</span></span> <span data-ttu-id="711c5-145">لدعم الضريبة على مستوى الرأس من Finance and Operations، مثل الضريبة على الشحن، يقوم النظام بمزامنة الضريبة إلى Sales على أنها منتج مدون بالاسم **ضريبة الشحن**، ويكون له مبلغ الضريبة من Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="711c5-145">To support tax at the header level from Finance and Operations, such as tax on freight, the system synchronizes tax to Sales as a write-in product that is named **Freight Tax**, and that has the tax amount from Finance and Operations.</span></span> <span data-ttu-id="711c5-146">بهذه الطريقة، يمكن استخدام عملية حساب السعر القياسي في Sales للإجماليات، حتى في حالة وجود ضريبة على مستوى الرأس من Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="711c5-146">In this way, the standard price calculation in Sales can be used for totals, even when there is tax at the header level from Finance and Operations.</span></span>

## <a name="discount-calculation-and-rounding"></a><span data-ttu-id="711c5-147">حساب الخصومات وتقريبها</span><span class="sxs-lookup"><span data-stu-id="711c5-147">Discount calculation and rounding</span></span>

<span data-ttu-id="711c5-148">يختلف نموذج حساب الخصم في Sales عن نموذج حساب الخصم في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="711c5-148">The discount calculation model in Sales differs from the discount calculation model in Finance and Operations.</span></span> <span data-ttu-id="711c5-149">في Finance and Operations، يمكن أن يكون مبلغ الخصم النهائي على بند مبيعات نتيجة لمجموعة من مبالغ الخصم ونسبه المئوية.</span><span class="sxs-lookup"><span data-stu-id="711c5-149">In Finance and Operations, the final discount amount on a sales line can be the result of a combination of discount amounts and discount percentages.</span></span> <span data-ttu-id="711c5-150">إذا كان مبلغ الخصم النهائي هذا مُقسمًا على الكمية في البند، فيمكن أن يحدث تقريب.</span><span class="sxs-lookup"><span data-stu-id="711c5-150">If this final discount amount is divided by the quantity on the line, rounding can occur.</span></span> <span data-ttu-id="711c5-151">ومع ذلك، لا يؤخذ هذا التقريب في الاعتبار في حالة مزامنة مبلغ خصم تقريبي لكل وحدة إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="711c5-151">However, this rounding isn't considered if a rounded per-unit discount amount is synchronized to Sales.</span></span> <span data-ttu-id="711c5-152">للمساعدة في ضمان مزامنة مبلغ الخصم الكامل من بند مبيعات في Finance and Operations بشكل صحيح إلى Sales، يجب مزامنة المبلغ الكامل دون تقسيمه على كمية البند.</span><span class="sxs-lookup"><span data-stu-id="711c5-152">To help guarantee that the full discount amount from a sales line in Finance and Operations is correctly synchronized to Sales, the full amount must be synchronized without being divided by the line quantity.</span></span> <span data-ttu-id="711c5-153">لذلك، يجب عليك تحديد **طريقة حساب الخصم** كـ **صنف بند** في Sales.</span><span class="sxs-lookup"><span data-stu-id="711c5-153">Therefore, you must define the **Discount calculation method** as **Line item** in Sales.</span></span>

<span data-ttu-id="711c5-154">عند مزامنة بند أمر مبيعات من Sales إلى Finance and Operations، يتم استخدام مبلغ خصم البند الكامل.</span><span class="sxs-lookup"><span data-stu-id="711c5-154">When a sales order line is synchronized from Sales to Finance and Operations, the full line discount amount is used.</span></span> <span data-ttu-id="711c5-155">نظرًا لأن Finance and Operations لا يحتوي على حقل يمكنه تخزين مبلغ الخصم الكامل لأحد البنود، يتم تقسيم المبلغ على الكمية ويتم تخزينه في الحقل **خصم البند**.</span><span class="sxs-lookup"><span data-stu-id="711c5-155">Because Finance and Operations has no field that can store the full discount amount for a line, the amount is divided by the quantity and stored in the **Line discount** field.</span></span> <span data-ttu-id="711c5-156">يتم تخزين أي تقريب يحدث في هذا التقسيم في الحقل **تكاليف المبيعات** في بند المبيعات.</span><span class="sxs-lookup"><span data-stu-id="711c5-156">Any rounding that occurs in this division is stored in the **Sales charges** field on the sales line.</span></span>

### <a name="example"></a><span data-ttu-id="711c5-157">مثال</span><span class="sxs-lookup"><span data-stu-id="711c5-157">Example</span></span>

<span data-ttu-id="711c5-158">**المزامنة من Sales إلى Finance and Operations**</span><span class="sxs-lookup"><span data-stu-id="711c5-158">**Synchronization from Sales to Finance and Operations**</span></span>

- <span data-ttu-id="711c5-159">**Sales:** الكمية = 3، خصم لكل بند = 10.00 دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="711c5-159">**Sales:** Quantity = 3, per-line discount = $10.00</span></span>
- <span data-ttu-id="711c5-160">**Finance and Operations:** الكمية = 3، مبلغ الخصم لكل بند = 3.33 دولار أمريكي، تكلفة المبيعات = 0.01 دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="711c5-160">**Finance and Operations:** Quantity = 3, line discount amount = $3.33, sales charge = -$0.01</span></span> 

<span data-ttu-id="711c5-161">**المزامنة من Finance and Operations إلى Sales**</span><span class="sxs-lookup"><span data-stu-id="711c5-161">**Synchronization from Finance and Operations to Sales**</span></span>

- <span data-ttu-id="711c5-162">**Finance and Operations:** الكمية = 3، مبلغ الخصم لكل بند = 3.33 دولار أمريكي، تكلفة المبيعات = 0.01 دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="711c5-162">**Finance and Operations:** Quantity = 3, line discount amount = $3.33, sales charge = -$0.01</span></span>
- <span data-ttu-id="711c5-163">**Sales:** الكمية = 3، خصم لكل بند = (3 × 3.33 دولار أمريكي) + 0.01 دولار أمريكي = 10.00 دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="711c5-163">**Sales:** Quantity = 3, per-line discount = (3 × $3.33) + $0.01 = $10.00</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="711c5-164">حل العميل المتوقع إلى النقدية في Sales</span><span class="sxs-lookup"><span data-stu-id="711c5-164">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="711c5-165">تمت إضافة حقول جديدة إلى كيان **الأمر** وهي تظهر على الصفحة:</span><span class="sxs-lookup"><span data-stu-id="711c5-165">New fields have been added to the **Order** entity and appear on the page:</span></span>

- <span data-ttu-id="711c5-166">**تتم المحافظة عليها خارجيًا‬‏‫‬‏‫** - عيّن هذا الخيار إلى **نعم** عندما يأتي الأمر من Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="711c5-166">**Is Maintained Externally** – Set this option to **Yes** when the order is coming from Finance and Operations.</span></span>
- <span data-ttu-id="711c5-167">**حالة المعالجة** - يستخدم هذا الحقل لعرض حالة معالجة الأمر في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="711c5-167">**Processing status** – This field shows the processing status of the order in Finance and Operations.</span></span> <span data-ttu-id="711c5-168">تتوفر القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="711c5-168">The following values are available:</span></span>

    - <span data-ttu-id="711c5-169">**مسودة** – الحالة الأولية عند إنشاء أمر في Sales.</span><span class="sxs-lookup"><span data-stu-id="711c5-169">**Draft** – The initial status when an order is created in Sales.</span></span> <span data-ttu-id="711c5-170">في Sales، لا يمكن تحرير إلا الأوامر التي بحالة المعالجة هذه.</span><span class="sxs-lookup"><span data-stu-id="711c5-170">In Sales, only orders with this processing status can be edited.</span></span>
    - <span data-ttu-id="711c5-171">**نشط** – الحالة بعد تنشيط الأمر في Sales باستخدام الزر **تنشيط**.</span><span class="sxs-lookup"><span data-stu-id="711c5-171">**Active** – The status after the order is activated in Sales by using the **Activate** button.</span></span>
    - <span data-ttu-id="711c5-172">**أوامر المبيعات المؤكدة**</span><span class="sxs-lookup"><span data-stu-id="711c5-172">**Confirmed**</span></span>
    - <span data-ttu-id="711c5-173">**كشف التعبئة**</span><span class="sxs-lookup"><span data-stu-id="711c5-173">**Packing Slip**</span></span>
    - <span data-ttu-id="711c5-174">**مفوتر**</span><span class="sxs-lookup"><span data-stu-id="711c5-174">**Invoiced**</span></span>
    - <span data-ttu-id="711c5-175">**منتقي**</span><span class="sxs-lookup"><span data-stu-id="711c5-175">**Picked**</span></span>
    - <span data-ttu-id="711c5-176">**منتقى جزئيًا**</span><span class="sxs-lookup"><span data-stu-id="711c5-176">**Partially Picked**</span></span>
    - <span data-ttu-id="711c5-177">**معبأ جزئيًا**</span><span class="sxs-lookup"><span data-stu-id="711c5-177">**Partially Packed**</span></span>
    - <span data-ttu-id="711c5-178">**مشحون**</span><span class="sxs-lookup"><span data-stu-id="711c5-178">**Shipped**</span></span>
    - <span data-ttu-id="711c5-179">**مشحون جزئيًا**</span><span class="sxs-lookup"><span data-stu-id="711c5-179">**Partially Shipped**</span></span>
    - <span data-ttu-id="711c5-180">**مفوتر جزئيًا**</span><span class="sxs-lookup"><span data-stu-id="711c5-180">**Partially Invoiced**</span></span>
    - <span data-ttu-id="711c5-181">**تم الإلغاء**</span><span class="sxs-lookup"><span data-stu-id="711c5-181">**Cancelled**</span></span>

<span data-ttu-id="711c5-182">يتم استخدام الإعداد **لديه منتجات تتم المحافظة عليها خارجيًا فقط** أثناء تنشيط الأمر للتحقق بشكل مستمر مما إذا كان أمر المبيعات يتكوّن بكامله من منتجات تتم المحافظة عليها خارجيًا.</span><span class="sxs-lookup"><span data-stu-id="711c5-182">The **Has Externally Maintained Products Only** setting is used during order activation to consistently track whether a sales order consists entirely of externally maintained products.</span></span> <span data-ttu-id="711c5-183">إذا كان أمر المبيعات يتكوّن بكامله من منتجات تتم المحافظة عليها خارجيًا، فستتم المحافظة على المنتجات في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="711c5-183">If a sales order consists entirely of externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="711c5-184">يساعد هذا الإعداد على ضمان عدم تنشيط أو محاولة مزامنة بنود أوامر المبيعات التي تشتمل على منتجات غير معروفة إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="711c5-184">This setting helps guarantee that you don't activate and try to synchronize sales order lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="711c5-185">تكون الأزرار **إنشاء فاتورة** و**إلغاء الأمر** و**إعادة الحساب** و**الحصول على منتجات** و**البحث عن عنوان** في صفحة **أمر المبيعات** مخفية للأوامر التي تتم المحافظة عليها خارجيًا إذ سيتم إنشاء الفواتير في Finance and Operations وستتم مزامنتها إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="711c5-185">The **Create Invoice**, **Cancel Order**, **Recalculate**, **Get Products**, and **Lookup Address** buttons on the **Sales order** page are hidden for externally maintained orders, because invoices will be created in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="711c5-186">لا يمكن تحرير هذه الأوامر، لأنه ستتم مزامنة معلومات أمر المبيعات من Finance and Operations بعد التنشيط.</span><span class="sxs-lookup"><span data-stu-id="711c5-186">These orders can't be edited, because sales order information will be synchronized from Finance and Operations after activation.</span></span>

<span data-ttu-id="711c5-187">ستبقى حالة أمر المبيعات **نشطة** للمساعدة في ضمان إمكانية انسياب التغييرات من Finance and Operations إلى أمر المبيعات في Sales.</span><span class="sxs-lookup"><span data-stu-id="711c5-187">The sales order status will remain **Active** to help guarantee that changes from Finance and Operations can flow to the sales order in Sales.</span></span> <span data-ttu-id="711c5-188">للتحكم في هذا السلوك، قم بتعيين الإعداد الافتراضي **Statecode \[الحالة\]** إلى **نشط** في مشروع تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="711c5-188">To control this behavior, set the default **Statecode \[Status\]** value to **Active** in the Data integration project.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="711c5-189">الشروط المسبقة وإعداد التعيين</span><span class="sxs-lookup"><span data-stu-id="711c5-189">Preconditions and mapping setup</span></span>

<span data-ttu-id="711c5-190">قبل إجراء مزامنة لأوامر المبيعات، لا بد من تحديث الإعدادات التالية في النظام.</span><span class="sxs-lookup"><span data-stu-id="711c5-190">Before you synchronize sales orders, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="711c5-191">الإعداد في Sales</span><span class="sxs-lookup"><span data-stu-id="711c5-191">Setup in Sales</span></span>

- <span data-ttu-id="711c5-192">تأكد من إعداد الأذونات للفريق الذي تم تعيين المستخدم من إعداد الاتصال في Sales إليه.</span><span class="sxs-lookup"><span data-stu-id="711c5-192">Make sure that permissions are set up for the team that the user from your Sales connection set is assigned to.</span></span> <span data-ttu-id="711c5-193">إذا كنت تستخدم بيانات العرض التوضيحي، فعادة ما يكون لدى المستخدم حق وصول المسؤول، ولكن هذا الحق لا يتوفر للفريق.</span><span class="sxs-lookup"><span data-stu-id="711c5-193">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="711c5-194">إذا لم يكن لدى الفريق حق وصول المسؤول، عند تشغيل المشروع من تكامل البيانات، فسوف تتلقى رسالة خطأ تفيد بأن الفريق الرئيسي مفقود.</span><span class="sxs-lookup"><span data-stu-id="711c5-194">If the team doesn't have admin access, when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="711c5-195">انتقل إلى **الإعدادات** &gt; **الأمان** &gt; **الفرق**، حدد الفريق المناسب، وحدد **إدارة الأدوار**، ثم حدد دورًا يملك الأذونات المطلوبة على سبيل المثال، **مسؤول النظام**.</span><span class="sxs-lookup"><span data-stu-id="711c5-195">Go to **Settings** &gt; **Security** &gt; **Teams**, select the relevant team, select **Manage Roles**, and select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="711c5-196">للتأكد من صحة حساب الخصومات في كل من Sales وFinance and Operations، يجب تعيين **طريقة حساب الخصم** إلى **صنف البند**.</span><span class="sxs-lookup"><span data-stu-id="711c5-196">To ensure correct calculation of discounts in both Sales and Finance and Operations **Discount calculation method** must be set to **Line item**.</span></span>
- <span data-ttu-id="711c5-197">انتقل إلى **الإعدادات** &gt; **الإدارة** &gt; **إعدادات النظام** &gt; **Sales**‎، وتأكد من أنه يتم استخدام الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="711c5-197">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="711c5-198">يكون الخيار **‬‏‫استخدام حساب أسعار النظام** معينًا إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="711c5-198">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="711c5-199">يكون الحقل **طريقة حساب الخصم** معينًا إلى **صنف البند**.</span><span class="sxs-lookup"><span data-stu-id="711c5-199">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="711c5-200">الإعداد في Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="711c5-200">Setup in Finance and Operations</span></span>

- <span data-ttu-id="711c5-201">انتقل إلى **المبيعات والتسويق**&gt;**المهام الدورية**&gt;**حساب إجماليات المبيعات**، وعيِّن الوظيفة لتشغيلها كوظيفة دُفعة.</span><span class="sxs-lookup"><span data-stu-id="711c5-201">Go to **Sales and marketing** &gt; **Periodic tasks** &gt; **Calculate sales totals**, and set the job to run as a batch job.</span></span> <span data-ttu-id="711c5-202">عيّن الخيار **‏‫حساب إجماليات أوامر المبيعات‬** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="711c5-202">Set the **Calculate totals for sales orders** option to **Yes**.</span></span> <span data-ttu-id="711c5-203">‏‫تعد هذه الخطوة هامة لأن أوامر المبيعات التي تم حساب إجماليات المبيعات‬ فيها هي فقط أوامر المبيعات التي ستتم مزامنتها إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="711c5-203">This step is important, because only sales orders where sales totals are calculated will be synchronized to Sales.</span></span> <span data-ttu-id="711c5-204">يجب أن يكون مدى تكرار وظيفة الدُفعة متوافقًا مع مدى تكرار مزامنة أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="711c5-204">The frequency of the batch job should be aligned with the frequency of sales order synchronization.</span></span>

### <a name="setup-in-the-sales-orders-sales-to-fin-and-ops---direct-data-integration-project"></a><span data-ttu-id="711c5-205">الإعداد في مشروع تكامل البيانات: أوامر المبيعات (Sales إلى Fin and Ops)‬ - مباشر</span><span class="sxs-lookup"><span data-stu-id="711c5-205">Setup in the Sales Orders (Sales to Fin and Ops) - Direct Data integration project</span></span>

- <span data-ttu-id="711c5-206">تأكد من وجود التعيين المطلوب لـ **Shipto\_country** إلى **DeliveryAddressCountryRegionISOCode**.</span><span class="sxs-lookup"><span data-stu-id="711c5-206">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="711c5-207">يمكنك تعيين قيمة افتراضية فارغة في تعيين القيمة لتجنب الاضطرار إلى إدخال بلد للأوامر المحلية.</span><span class="sxs-lookup"><span data-stu-id="711c5-207">You can make blank a default value in the value map to avoid having to type country for national orders.</span></span> <span data-ttu-id="711c5-208">عيّن الجانب الأيمن إلى "فارغ"، وعيّن الجانب الأيسر إلى البلد أو المنطقة المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="711c5-208">Set the left side to 'Blank', and set the right side to the desired country or region.</span></span>

    <span data-ttu-id="711c5-209">قيمة القالب هي تعيين قيمة حيث يتم تعيين العديد من البلدان أو المناطق، وحيث "فارغ" = US.</span><span class="sxs-lookup"><span data-stu-id="711c5-209">The template value is a value map where several countries or regions are mapped, and where 'Blank' = US.</span></span>

### <a name="setup-in-the-sales-orders-fin-and-ops-to-sales---direct-data-integration-project"></a><span data-ttu-id="711c5-210">الإعداد في مشروع تكامل البيانات: أوامر المبيعات (Fin and Ops إلى Sales)‬ - مباشر</span><span class="sxs-lookup"><span data-stu-id="711c5-210">Setup in the Sales Orders (Fin and Ops to Sales) - Direct Data integration project</span></span>

#### <a name="salesheader-task"></a><span data-ttu-id="711c5-211">مهمة SalesHeader</span><span class="sxs-lookup"><span data-stu-id="711c5-211">SalesHeader task</span></span>

- <span data-ttu-id="711c5-212">تكون قائمة الأسعار مطلوبة لإنشاء الأوامر في Sales.</span><span class="sxs-lookup"><span data-stu-id="711c5-212">A price list is required in order to create orders in Sales.</span></span> <span data-ttu-id="711c5-213">حدّث تعيين القيمة لـ **pricelevelid.name \[اسم قائمة الأسعار\]** إلى قائمة الأسعار المستخدمة في Sales لكل عملة.</span><span class="sxs-lookup"><span data-stu-id="711c5-213">Update the value map for **pricelevelid.name \[Price List Name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="711c5-214">يمكنك استخدام قائمة الأسعار الافتراضية لعمله واحدة.</span><span class="sxs-lookup"><span data-stu-id="711c5-214">You can use the default price list for a single currency.</span></span> <span data-ttu-id="711c5-215">بدلاً من ذلك، إذا كان لديك قوائم أسعار بعملات متعددة، يمكنك استخدام تعيين قيمة.</span><span class="sxs-lookup"><span data-stu-id="711c5-215">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="711c5-216">قيمة القالب الافتراضية لـ **pricelevelid.name \[اسم قائمة الأسعار\]** تكون **CRM Service USA (نموذج)**.</span><span class="sxs-lookup"><span data-stu-id="711c5-216">The default template value for **pricelevelid.name \[Price List Name\]** is **CRM Service USA (sample)**.</span></span>

#### <a name="salesline-task"></a><span data-ttu-id="711c5-217">مهمة SalesLine</span><span class="sxs-lookup"><span data-stu-id="711c5-217">SalesLine task</span></span>

- <span data-ttu-id="711c5-218">تأكد من وجود تعيين القيمة المطلوب لـ **SalesUnitSymbol** في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="711c5-218">Make sure that the required value map for **SalesUnitSymbol** in Finance and Operations exists.</span></span>
- <span data-ttu-id="711c5-219">تأكد من تحديد الوحدات المطلوبة في Sales.</span><span class="sxs-lookup"><span data-stu-id="711c5-219">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="711c5-220">يتم تعريف قيمة القالب التي لها تعيين قيمة لـ **SalesUnitSymbol** إلى **oumid.name**.</span><span class="sxs-lookup"><span data-stu-id="711c5-220">A template value that has a value map is defined for **SalesUnitSymbol** to **oumid.name**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="711c5-221">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="711c5-221">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="711c5-222">لا تشكل الحقول **شروط الدفع** و**شروط الشحن** و**شروط التسليم** و**أسلوب الشحن** و**وضع التسليم** جزءًا من التعيينات الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="711c5-222">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="711c5-223">لتعيين هذه الحقول، يجب إعداد تعيين قيمة خاصة بالبيانات الموجودة في المؤسسات التي تتم مزامنة الكيان بينها.</span><span class="sxs-lookup"><span data-stu-id="711c5-223">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="711c5-224">تبين الأشكال التوضيحية التالية مثالاً لتعيين قالب في تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="711c5-224">The following illustrations show an example of a template mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="711c5-225">يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Sales إلى Finance and Operations أو من Finance and Operations إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="711c5-225">The mapping shows which field information will be synchronized from Sales to Finance and Operations, or from Finance and Operations to Sales.</span></span>

### <a name="sales-orders-fin-and-ops-to-sales---direct-orderheader"></a><span data-ttu-id="711c5-226">أوامر المبيعات (Fin and Ops إلى Sales) - مباشر: OrderHeader</span><span class="sxs-lookup"><span data-stu-id="711c5-226">Sales Orders (Fin and Ops to Sales) - Direct: OrderHeader</span></span>

<span data-ttu-id="711c5-227">[![تعيين القالب في تكامل البيانات](./media/sales-order-direct-template-mapping-data-integrator-1.png)](./media/sales-order-direct-template-mapping-data-integrator-1.png)</span><span class="sxs-lookup"><span data-stu-id="711c5-227">[![Template mapping in Data integration](./media/sales-order-direct-template-mapping-data-integrator-1.png)](./media/sales-order-direct-template-mapping-data-integrator-1.png)</span></span>

### <a name="sales-orders-fin-and-ops-to-sales---direct-orderline"></a><span data-ttu-id="711c5-228">أوامر المبيعات (Fin and Ops إلى Sales) - مباشر: OrderLine</span><span class="sxs-lookup"><span data-stu-id="711c5-228">Sales Orders (Fin and Ops to Sales) - Direct: OrderLine</span></span>

<span data-ttu-id="711c5-229">[![تعيين القالب في تكامل البيانات](./media/sales-order-direct-template-mapping-data-integrator-2.png)](./media/sales-order-direct-template-mapping-data-integrator-2.png)</span><span class="sxs-lookup"><span data-stu-id="711c5-229">[![Template mapping in Data integration](./media/sales-order-direct-template-mapping-data-integrator-2.png)](./media/sales-order-direct-template-mapping-data-integrator-2.png)</span></span>

### <a name="sales-orders-sales-to-fin-and-ops---direct-orderheader"></a><span data-ttu-id="711c5-230">أوامر المبيعات (Sales إلى Fin and Ops) - مباشر: OrderHeader</span><span class="sxs-lookup"><span data-stu-id="711c5-230">Sales Orders (Sales to Fin and Ops) - Direct: OrderHeader</span></span>

<span data-ttu-id="711c5-231">[![تعيين القالب في تكامل البيانات](./media/sales-order-direct-template-mapping-data-integrator-3.png)](./media/sales-order-direct-template-mapping-data-integrator-3.png)</span><span class="sxs-lookup"><span data-stu-id="711c5-231">[![Template mapping in Data integration](./media/sales-order-direct-template-mapping-data-integrator-3.png)](./media/sales-order-direct-template-mapping-data-integrator-3.png)</span></span>

### <a name="sales-orders-sales-to-fin-and-ops---direct-orderline"></a><span data-ttu-id="711c5-232">أوامر المبيعات (Sales إلى Fin and Ops) - مباشر: OrderLine</span><span class="sxs-lookup"><span data-stu-id="711c5-232">Sales Orders (Sales to Fin and Ops) - Direct: OrderLine</span></span>

<span data-ttu-id="711c5-233">[![تعيين القالب في تكامل البيانات](./media/sales-order-direct-template-mapping-data-integrator-4.png)](./media/sales-order-direct-template-mapping-data-integrator-4.png)</span><span class="sxs-lookup"><span data-stu-id="711c5-233">[![Template mapping in Data integration](./media/sales-order-direct-template-mapping-data-integrator-4.png)](./media/sales-order-direct-template-mapping-data-integrator-4.png)</span></span>

## <a name="related-topics"></a><span data-ttu-id="711c5-234">مواضيع مرتبطة</span><span class="sxs-lookup"><span data-stu-id="711c5-234">Related topics</span></span>

[<span data-ttu-id="711c5-235">العميل المتوقع إلى النقدية</span><span class="sxs-lookup"><span data-stu-id="711c5-235">Prospect to cash</span></span>](prospect-to-cash.md)

