---
title: "مزامنة الحسابات مباشرةً من Sales للعملاء في Finance and Operations‎"
description: "يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة حسابات من Microsoft Dynamics 365 for Sales إلى Microsoft Dynamics 365 for Finance and Operations."
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 8a4a0487bd13094c96c2804acd1ebadbcfa6bf41
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---

# <a name="synchronize-accounts-directly-from-sales-to-customers-in-finance-and-operations"></a><span data-ttu-id="c00f6-103">مزامنة الحسابات مباشرةً من Sales إلى العملاء في Finance and Operations‎</span><span class="sxs-lookup"><span data-stu-id="c00f6-103">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>

[!INCLUDE [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="c00f6-104">قبل أن تتمكن من استخدام حل العميل المتوقع إلى النقدية، يجب عليك الاطلاع على [تكامل بيانات Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="c00f6-104">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

<span data-ttu-id="c00f6-105">يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة حسابات مباشرةً من Microsoft Dynamics 365 for Sales إلى Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c00f6-105">This topic discusses the templates and underlying tasks that are used to synchronize accounts directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="c00f6-106">تدفق البيانات في حل العميل المتوقع إلى النقدية</span><span class="sxs-lookup"><span data-stu-id="c00f6-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="c00f6-107">يستخدم حل العميل المتوقع إلى النقدية ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Finance and Operations وSales.</span><span class="sxs-lookup"><span data-stu-id="c00f6-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span>  <span data-ttu-id="c00f6-108">تسمح قوالب حل العميل المتوقع إلى النقدية المتوفرة مع ميزة تكامل البيانات بتدفق بيانات الحسابات وجهات الاتصال والمنتجات وعروض أسعار المبيعات وأوامر المبيعات وفواتير المبيعات بين Finance and Operations وSales.</span><span class="sxs-lookup"><span data-stu-id="c00f6-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="c00f6-109">يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات بين Finance and Operations وSales.</span><span class="sxs-lookup"><span data-stu-id="c00f6-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="c00f6-110">[![تدفق البيانات في حل العميل المتوقع إلى النقدية](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="c00f6-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="c00f6-111">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="c00f6-111">Templates and tasks</span></span>

<span data-ttu-id="c00f6-112">للوصول إلى القوالب المتوفرة، افتح [مركز إدارة PowerApps](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="c00f6-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="c00f6-113">حدد **المشاريع**، وبعد ذلك، في الزاوية العلوية اليسرى، حدد **مشروع جديد** لتحديد القوالب العامة.</span><span class="sxs-lookup"><span data-stu-id="c00f6-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="c00f6-114">يتم استخدام القالب والمهمة الأساسية التالية لمزامنة الحسابات من Sales إلى Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="c00f6-114">The following template and underlying task are used to synchronize accounts from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="c00f6-115">**اسم القالب في تكامل البيانات:** الحسابات (Sales إلى Fin and Ops) - مباشر</span><span class="sxs-lookup"><span data-stu-id="c00f6-115">**Name of the template in Data integration:** Accounts (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="c00f6-116">**اسم المهمة في المشروع:** الحسابات - العملاء</span><span class="sxs-lookup"><span data-stu-id="c00f6-116">**Name of the task in the project:** Accounts - Customers</span></span>

<span data-ttu-id="c00f6-117">لا توجد مهام مزامنة مطلوبة قبل إجراء مزامنة الحساب/العميل.</span><span class="sxs-lookup"><span data-stu-id="c00f6-117">No synchronization tasks are required before Account/Customer synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="c00f6-118">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="c00f6-118">Entity set</span></span>

| <span data-ttu-id="c00f6-119">مبيعات</span><span class="sxs-lookup"><span data-stu-id="c00f6-119">Sales</span></span>    | <span data-ttu-id="c00f6-120">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c00f6-120">Finance and Operations</span></span> |
|----------|------------------------|
| <span data-ttu-id="c00f6-121">الحسابات</span><span class="sxs-lookup"><span data-stu-id="c00f6-121">Accounts</span></span> | <span data-ttu-id="c00f6-122">العملاء V2</span><span class="sxs-lookup"><span data-stu-id="c00f6-122">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="c00f6-123">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="c00f6-123">Entity flow</span></span>

<span data-ttu-id="c00f6-124">تُدار الحسابات في Sales وتتم مزامنتها إلى Finance and Operations كعملاء.</span><span class="sxs-lookup"><span data-stu-id="c00f6-124">Accounts are managed in Sales and synchronized to Finance and Operations as customers.</span></span> <span data-ttu-id="c00f6-125">يتم تعيين الخاصية **تتم المحافظة عليها خارجيًا** على هؤلاء العملاء إلى **نعم** لتعقب العملاء الناشئين من Sales.</span><span class="sxs-lookup"><span data-stu-id="c00f6-125">The **Is Externally Maintained** property on these customers is set to **Yes** to track customers that originate from Sales.</span></span> <span data-ttu-id="c00f6-126">أثناء الفوترة، يتم استخدام هذه المعلومات لتصفية الفواتير التي سيتم مزامنتها إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="c00f6-126">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="c00f6-127">حل العميل المتوقع إلى النقدية في Sales</span><span class="sxs-lookup"><span data-stu-id="c00f6-127">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="c00f6-128">يتوفر حقل **رقم الحساب** في صفحة **الحساب**.</span><span class="sxs-lookup"><span data-stu-id="c00f6-128">The **Account Number** field is available on the **Account** page.</span></span> <span data-ttu-id="c00f6-129">تم إنشاء مفتاح طبيعي وفريد له لدعم التكامل.</span><span class="sxs-lookup"><span data-stu-id="c00f6-129">It has been made a natural and unique key in order to support the integration.</span></span> <span data-ttu-id="c00f6-130">قد تؤثر ميزة المفتاح الطبيعي في حل إدارة علاقات العملاء (CRM)‬ على العملاء الذين يستخدمون حقل **رقم الحساب**، ولكنهم لا يستخدمون قيم **رقم الحساب** لكل حساب.</span><span class="sxs-lookup"><span data-stu-id="c00f6-130">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** field, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="c00f6-131">في الوقت الحالي، لا يدعم حل التكامل هذه الحالة.</span><span class="sxs-lookup"><span data-stu-id="c00f6-131">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="c00f6-132">عند إنشاء حساب جديد، إذا لم تكن قيمة **رقم الحساب** موجودة، فسيتم إنشاؤها تلقائيًا باستخدام تسلسل رقمي.</span><span class="sxs-lookup"><span data-stu-id="c00f6-132">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="c00f6-133">تتكون القيمة من **ACC**، يليه تسلسل رقمي متزايد ثم لاحقة من ستة أحرف.</span><span class="sxs-lookup"><span data-stu-id="c00f6-133">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="c00f6-134">فيما يلي مثال على ذلك: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="c00f6-134">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="c00f6-135">عند تطبيق حل التكامل على Sales، يقوم برنامج نصي للترقية بتعيين حقل **رقم الحساب** للحسابات الموجودة في Sales.</span><span class="sxs-lookup"><span data-stu-id="c00f6-135">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** field for existing accounts in Sales.</span></span> <span data-ttu-id="c00f6-136">في حال عدم وجود قيم في **رقم الحساب**، سيتم استخدام التسلسل الرقمي الذي تم ذكره في وقت سابق.</span><span class="sxs-lookup"><span data-stu-id="c00f6-136">If there are no **Account Number** values, the number sequence that was mentioned earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="c00f6-137">الشروط المسبقة وإعداد التعيين</span><span class="sxs-lookup"><span data-stu-id="c00f6-137">Preconditions and mapping setup</span></span>

- <span data-ttu-id="c00f6-138">يجب تحديث تعيين **CustomerGroupId** إلى قيمة صالحة في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c00f6-138">The **CustomerGroupId** mapping must be updated to a valid value in Finance and Operations.</span></span> <span data-ttu-id="c00f6-139">يمكنك تحديد قيمة افتراضية، أو يمكنك تعيين القيمة باستخدام تعيين القيمة.</span><span class="sxs-lookup"><span data-stu-id="c00f6-139">You can specify a default value, or you can set the value by using a value map.</span></span>

    <span data-ttu-id="c00f6-140">قيمة القالب الافتراضية هي **10**.</span><span class="sxs-lookup"><span data-stu-id="c00f6-140">The default template value is **10**.</span></span>

- <span data-ttu-id="c00f6-141">عن طريق إضافة التعيينات التالية، يمكنك المساعدة على تقليل عدد التحديثات اليدوية المطلوبة في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c00f6-141">By adding the following mappings, you can help reduce the number of manual updates that are required in Finance and Operations.</span></span> <span data-ttu-id="c00f6-142">يمكنك استخدام قيمة افتراضية قيمة أو تعيين قيمة من، على سبيل المثال، **البلد/المنطقة** أو **المدينة**.</span><span class="sxs-lookup"><span data-stu-id="c00f6-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="c00f6-143">**SiteId** – الموقع مطلوب لإنشاء بنود أوامر المبيعات وعروض الأسعار في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c00f6-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="c00f6-144">يمكن أخذ موقع افتراضي إما من المنتج، أو من العميل من رأس الأمر.</span><span class="sxs-lookup"><span data-stu-id="c00f6-144">A default site can be taken either from the product, or from the customer from the order header.</span></span>

        <span data-ttu-id="c00f6-145">قيمة القالب الافتراضية هي **1**.</span><span class="sxs-lookup"><span data-stu-id="c00f6-145">The default template value is **1**.</span></span>

    - <span data-ttu-id="c00f6-146">**WarehouseId** – المستودع مطلوب لمعالجة بنود أوامر المبيعات وعروض الأسعار في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c00f6-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="c00f6-147">يمكن أخذ مستودع افتراضي إما من المنتج، أو من العميل من رأس الأمر في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c00f6-147">A default warehouse can be taken either from the product, or from the customer from the order header in Finance and Operations.</span></span>

        <span data-ttu-id="c00f6-148">قيمة القالب الافتراضية هي **13**.</span><span class="sxs-lookup"><span data-stu-id="c00f6-148">The default template value is **13**.</span></span>

    - <span data-ttu-id="c00f6-149">**LanguageId** – اللغة مطلوبة لإنشاء أوامر المبيعات وعروض الأسعار في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c00f6-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="c00f6-150">بشكل افتراضي، يتم استخدام اللغة من رأس الأمر من العميل.</span><span class="sxs-lookup"><span data-stu-id="c00f6-150">By default, the language from the order header from the customer is used.</span></span>

        <span data-ttu-id="c00f6-151">قيمة القالب الافتراضية هي **ar-sa**.</span><span class="sxs-lookup"><span data-stu-id="c00f6-151">The default template value is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c00f6-152">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="c00f6-152">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="c00f6-153">لا يتم تضمين الحقول **شروط الدفع** و**شروط الشحن** و**شروط التسليم** و**أسلوب الشحن** و**وضع التسليم** في التعيينات الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="c00f6-153">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="c00f6-154">لتعيين هذه الحقول، يجب إعداد تعيين قيمة خاصة بالبيانات الموجودة في المؤسسات التي تتم مزامنة الكيان بينها.</span><span class="sxs-lookup"><span data-stu-id="c00f6-154">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="c00f6-155">تبين الأشكال التوضيحية التالية مثالاً لتعيين قالب في تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="c00f6-155">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="c00f6-156">يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Sales إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c00f6-156">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

![تعيين القالب في تكامل البيانات](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a><span data-ttu-id="c00f6-158">مواضيع مرتبطة</span><span class="sxs-lookup"><span data-stu-id="c00f6-158">Related topics</span></span>


[<span data-ttu-id="c00f6-159">العميل المتوقع إلى النقدية</span><span class="sxs-lookup"><span data-stu-id="c00f6-159">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="c00f6-160">مزامنة الحسابات مباشرةً من Sales للعملاء في Finance and Operations‎</span><span class="sxs-lookup"><span data-stu-id="c00f6-160">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="c00f6-161">مزامنة جهات الاتصال مباشرةً من Sales لجهات الاتصال في Finance and Operations‎</span><span class="sxs-lookup"><span data-stu-id="c00f6-161">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="c00f6-162">مزامنة رؤوس وبنود أوامر المبيعات مباشرةً من Finance and Operations إلى Sales</span><span class="sxs-lookup"><span data-stu-id="c00f6-162">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="c00f6-163">مزامنة رؤوس وبنود فواتير المبيعات مباشرةً من Finance and Operations إلى Sales</span><span class="sxs-lookup"><span data-stu-id="c00f6-163">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)


