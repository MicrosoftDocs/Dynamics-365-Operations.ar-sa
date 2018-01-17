---
title: "مزامنة الحسابات من Sales إلى العملاء في Finance and Operations"
description: "يناقش الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة حسابات من Microsoft Dynamics 365 for Sales إلى Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
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
ms.openlocfilehash: f1ddb3853d1cf0613ab324bb35c3f15ad1f4f984
ms.contentlocale: ar-sa
ms.lasthandoff: 01/17/2018

---

# <a name="synchronize-accounts-from-sales-to-customers-in-finance-and-operations"></a><span data-ttu-id="fa514-103">مزامنة الحسابات من Sales إلى العملاء في Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="fa514-103">Synchronize accounts from Sales to customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="fa514-104">قبل أن تتمكن من استخدام حل العميل المتوقع إلى النقدية، يجب عليك الاطلاع على [تكامل بيانات Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="fa514-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="fa514-105">يناقش الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة الحسابات من Microsoft Dynamics 365 for Sales (Sales) إلى Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="fa514-105">The topic discusses the templates and underlying tasks that are used to synchronize accounts from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span>

## <a name="template-and-task"></a><span data-ttu-id="fa514-106">القالب والمهمة</span><span class="sxs-lookup"><span data-stu-id="fa514-106">Template and task</span></span>

<span data-ttu-id="fa514-107">يتم استخدام القوالب والمهام الأساسية التالية لمزامنة الحسابات من Sales إلى Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="fa514-107">The following templates and underlying tasks are used to synchronize accounts from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="fa514-108">**اسم القالب:** الحسابات (Sales إلى Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="fa514-108">**Name of the template:** Accounts (Sales to Fin and Ops)</span></span>
- <span data-ttu-id="fa514-109">**اسم المهمة في المشروع:** الحسابات - الحساب - العملاء</span><span class="sxs-lookup"><span data-stu-id="fa514-109">**Name of the task in the project:** Accounts - Account - Customers</span></span>

<span data-ttu-id="fa514-110">مهام المزامنة المطلوبة قبل مزامنة الحساب/العميل: بلا</span><span class="sxs-lookup"><span data-stu-id="fa514-110">Sync tasks required prior to Account / Customer sync: None</span></span>

## <a name="entity-set"></a><span data-ttu-id="fa514-111">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="fa514-111">Entity set</span></span>

| <span data-ttu-id="fa514-112">ال‏‏مبيعات</span><span class="sxs-lookup"><span data-stu-id="fa514-112">Sales</span></span>    | <span data-ttu-id="fa514-113">CDS</span><span class="sxs-lookup"><span data-stu-id="fa514-113">CDS</span></span>     | <span data-ttu-id="fa514-114">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="fa514-114">Finance and Operations</span></span> |
|----------|---------|------------------------|
| <span data-ttu-id="fa514-115">الحسابات</span><span class="sxs-lookup"><span data-stu-id="fa514-115">Accounts</span></span> | <span data-ttu-id="fa514-116">الحساب</span><span class="sxs-lookup"><span data-stu-id="fa514-116">Account</span></span> | <span data-ttu-id="fa514-117">العملاء</span><span class="sxs-lookup"><span data-stu-id="fa514-117">Customers</span></span>              |

## <a name="entity-flow"></a><span data-ttu-id="fa514-118">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="fa514-118">Entity flow</span></span>

<span data-ttu-id="fa514-119">تُدار الحسابات في Sales وتتم مزامنتها إلى Finance and Operations كعملاء.</span><span class="sxs-lookup"><span data-stu-id="fa514-119">Accounts are managed in Sales and synchronized to Finance and Operations as Customers.</span></span> <span data-ttu-id="fa514-120">يتم تعيين الخاصية **تتم المحافظة عليها خارجيًا** على هؤلاء العملاء إلى **نعم** لتعقب العملاء الناشئين من Sales.</span><span class="sxs-lookup"><span data-stu-id="fa514-120">The **Is Externally Maintained** property on these Customers is set to **Yes** to track Customers that originate from Sales.</span></span> <span data-ttu-id="fa514-121">أثناء الفوترة، يتم استخدام هذه المعلومات لتصفية الفواتير التي سيتم مزامنتها إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="fa514-121">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="fa514-122">حل العميل المتوقع إلى النقدية في Sales</span><span class="sxs-lookup"><span data-stu-id="fa514-122">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="fa514-123">يتوفر حقل **رقم الحساب** في صفحة **الحساب**.</span><span class="sxs-lookup"><span data-stu-id="fa514-123">The **Account Number** field is available on the **Account** page.</span></span> <span data-ttu-id="fa514-124">تم إنشاء مفتاح طبيعي وفريد له لدعم التكامل.</span><span class="sxs-lookup"><span data-stu-id="fa514-124">It has been made a natural and unique key to support the integration.</span></span> <span data-ttu-id="fa514-125">قد تؤثر ميزة المفتاح الطبيعي في حل إدارة علاقات العملاء (CRM)‬ على العملاء الذين يستخدمون حقل **رقم الحساب**، ولكنهم لا يستخدمون قيم **رقم الحساب** لكل حساب.</span><span class="sxs-lookup"><span data-stu-id="fa514-125">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** field, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="fa514-126">في الوقت الحالي، لا يدعم حل التكامل هذه الحالة.</span><span class="sxs-lookup"><span data-stu-id="fa514-126">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="fa514-127">عند إنشاء حساب جديد، إذا لم تكن قيمة **رقم الحساب** موجودة، فسيتم إنشاؤها تلقائيًا باستخدام تسلسل رقمي.</span><span class="sxs-lookup"><span data-stu-id="fa514-127">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="fa514-128">تتكون القيمة من **ACC**، يليه تسلسل رقمي متزايد ثم لاحقة من ستة أحرف.</span><span class="sxs-lookup"><span data-stu-id="fa514-128">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="fa514-129">فيما يلي مثال على ذلك: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="fa514-129">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="fa514-130">عند تطبيق حل التكامل على Sales، يقوم برنامج نصي للترقية بتعيين حقل **رقم الحساب** للحسابات الموجودة في Sales.</span><span class="sxs-lookup"><span data-stu-id="fa514-130">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** field for existing accounts in Sales.</span></span> <span data-ttu-id="fa514-131">في حال عدم وجود قيم في **رقم الحساب**، سيتم استخدام التسلسل الرقمي الذي تم وصفه في وقت سابق.</span><span class="sxs-lookup"><span data-stu-id="fa514-131">If there are no **Account Number** values, the number sequence that was described earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="fa514-132">الشروط المسبقة وإعداد التعيين</span><span class="sxs-lookup"><span data-stu-id="fa514-132">Preconditions and mapping setup</span></span>

- <span data-ttu-id="fa514-133">يجب تحديث تعيين **CustomerGroupId** من **CDS &gt; الوجهة** إلى قيمة صالحة في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="fa514-133">**CustomerGroupId** mapping from **CDS &gt; Destination** must be updated to a valid value in Finance and Operations.</span></span> <span data-ttu-id="fa514-134">يمكنك تحديد قيمة افتراضية، أو يمكنك تعيين القيمة باستخدام تعيين القيمة.</span><span class="sxs-lookup"><span data-stu-id="fa514-134">You can specify a default value, or you can set the value by using a value map.</span></span> <span data-ttu-id="fa514-135">قيمة القالب الافتراضية هي **10**.</span><span class="sxs-lookup"><span data-stu-id="fa514-135">The default template value is **10**.</span></span>
- <span data-ttu-id="fa514-136">يجب ملء **"كود بلد/منطقة العنوان** في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="fa514-136">**Address country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="fa514-137">لتجنب أخطاء المزامنة، يمكنك تحديد قيمة افتراضية في التعيين من **CDS &gt; الوجهة**.</span><span class="sxs-lookup"><span data-stu-id="fa514-137">To avoid synchronization errors, you can specify a default value in the mapping from **CDS &gt; Destination**.</span></span> <span data-ttu-id="fa514-138">يتم عندئذٍ استخدام هذه القيمة الافتراضية إذا ترك الحقل فارغًا في Sales.</span><span class="sxs-lookup"><span data-stu-id="fa514-138">That default value is then used if the field is left blank in Sales.</span></span>

    - <span data-ttu-id="fa514-139">قيمة القالب الافتراضية للخيار **AddressCountryRegionISOCode** هي **USA**.</span><span class="sxs-lookup"><span data-stu-id="fa514-139">The default template value for **AddressCountryRegionISOCode** is **USA**.</span></span>
    - <span data-ttu-id="fa514-140">قيمة القالب الافتراضية للخيار **DeliveryAddressCountryRegionISOCode** هي **USA**.</span><span class="sxs-lookup"><span data-stu-id="fa514-140">The default template value for **DeliveryAddressCountryRegionISOCode** is **USA**.</span></span>

- <span data-ttu-id="fa514-141">عن طريق إضافة التعيينات التالية من **‎CDS &gt;الوجهة**، يمكنك المساعدة على تقليل عدد التحديثات اليدوية المطلوبة في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="fa514-141">By adding the following mappings from **CDS &gt; Destination**, you can help reduce the number of manual updates that are required in Finance and Operations.</span></span> <span data-ttu-id="fa514-142">يمكنك استخدام قيمة افتراضية قيمة أو تعيين قيمة من، على سبيل المثال، **البلد/المنطقة** أو **المدينة**.</span><span class="sxs-lookup"><span data-stu-id="fa514-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="fa514-143">**SiteId** – الموقع مطلوب لإنشاء بنود أوامر المبيعات وعروض الأسعار في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="fa514-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="fa514-144">يمكن أخذ موقع افتراضي إما من المنتج، أو من العميل من رأس الأمر.</span><span class="sxs-lookup"><span data-stu-id="fa514-144">A default site can be taken either from the product, or from the customer from the order header.</span></span> <span data-ttu-id="fa514-145">قيمة القالب الافتراضية للخيار **SiteId‎** هي **1**.</span><span class="sxs-lookup"><span data-stu-id="fa514-145">The default template value for **SiteId** is **1**.</span></span>
    - <span data-ttu-id="fa514-146">**WarehouseId** – المستودع مطلوب لمعالجة بنود أوامر المبيعات وعروض الأسعار في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="fa514-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="fa514-147">يمكن أخذ مستودع افتراضي إما من المنتج، أو من العميل من رأس الأمر في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="fa514-147">A default warehouse can be taken either from the product, or from the customer from the order header in Finance and Operations.</span></span> <span data-ttu-id="fa514-148">قيمة القالب الافتراضية للخيار **WarehouseId** هي **13**.</span><span class="sxs-lookup"><span data-stu-id="fa514-148">The default template value for **WarehouseId** is **13**.</span></span>
    - <span data-ttu-id="fa514-149">**LanguageId** – اللغة مطلوبة لإنشاء أوامر المبيعات وعروض الأسعار في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="fa514-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="fa514-150">بشكل افتراضي، يتم استخدام اللغة من رأس الأمر من العميل.</span><span class="sxs-lookup"><span data-stu-id="fa514-150">By default, the language from the order header from the customer is used.</span></span> <span data-ttu-id="fa514-151">قيمة القالب الافتراضية للخيار **LanguageId** هي **en-us**.</span><span class="sxs-lookup"><span data-stu-id="fa514-151">The default template value for **LanguageId** is **en-us**.</span></span>

- <span data-ttu-id="fa514-152">تحديث معرف مؤسسة CDS (**Organization_OrganizationId**) في تعيين**المصدر &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="fa514-152">Update the CDS organization ID (**Organization_OrganizationId**) in the **Source &gt; CDS** mapping.</span></span> <span data-ttu-id="fa514-153">قيمة القالب الافتراضية هي **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="fa514-153">The default template value is **ORG001**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="fa514-154">تعيين القالب في موحد البيانات</span><span class="sxs-lookup"><span data-stu-id="fa514-154">Template mapping in data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="fa514-155">لا يتم تضمين الحقول **شروط الدفع** و**شروط الشحن** و**شروط التسليم** و**أسلوب الشحن** و**وضع التسليم** في التعيينات الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="fa514-155">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="fa514-156">لتعيين هذه الحقول، يجب إعداد تعيين قيمة.</span><span class="sxs-lookup"><span data-stu-id="fa514-156">To map these fields, you must set up a value mapping.</span></span> <span data-ttu-id="fa514-157">تعتبر تعيينات القيم خاصة بالبيانات الموجودة في المؤسسات التي تتم مزامنة الكيان بينها.</span><span class="sxs-lookup"><span data-stu-id="fa514-157">Value mappings are specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="fa514-158">تبين الأشكال التوضيحية التالية مثالاً لتعيين قالب في موحد البيانات.</span><span class="sxs-lookup"><span data-stu-id="fa514-158">The following illustrations show an example of a template mapping in data integrator.</span></span>

![تعيين القالب في موحد البيانات](./media/accounts-template-mapping-data-integrator-1.png)

![تعيين القالب للحسابات في موحد البيانات](./media/accounts-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="fa514-161">مواضيع مرتبطة</span><span class="sxs-lookup"><span data-stu-id="fa514-161">Related topics</span></span>

[<span data-ttu-id="fa514-162">مزامنة المنتجات من Finance and Operations إلى المنتجات في Sales</span><span class="sxs-lookup"><span data-stu-id="fa514-162">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="fa514-163">مزامنة جهات الاتصال من Sales إلى جهات الاتصال أو العملاء في Finance and Operations‎</span><span class="sxs-lookup"><span data-stu-id="fa514-163">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="fa514-164">مزامنة رؤوس وبنود عرض أسعار المبيعات‬ من Sales إلى Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="fa514-164">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="fa514-165">مزامنة رؤوس وبنود أوامر المبيعات من Finance and Operations إلى Sales</span><span class="sxs-lookup"><span data-stu-id="fa514-165">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)

[<span data-ttu-id="fa514-166">مزامنة رؤوس وبنود فواتير المبيعات من Finance and Operations إلى Sales</span><span class="sxs-lookup"><span data-stu-id="fa514-166">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)




