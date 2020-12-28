---
title: مزامنة الحسابات مباشرةً من Sales إلى العملاء في Supply Chain Management‎
description: يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة الحسابات من Dynamics 365 Sales إلى Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 10/25/2018
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
ms.openlocfilehash: 8aa03f94e0fb89a6d34ce014dbb6004a1a666327
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529200"
---
# <a name="synchronize-accounts-directly-from-sales-to-customers-in-supply-chain-management"></a><span data-ttu-id="ec641-103">مزامنة الحسابات مباشرةً من Sales إلى العملاء في Supply Chain Management‎</span><span class="sxs-lookup"><span data-stu-id="ec641-103">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="ec641-104">قبل أن تتمكن من استخدام حل العميل المتوقع إلى النقدية، يجب عليك الاطلاع على [تكامل البيانات في Common Data Service للتطبيقات‏‎](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="ec641-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="ec641-105">يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة الحسابات من Dynamics 365 Sales إلى Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ec641-105">This topic discusses the templates and underlying tasks that are used to synchronize accounts directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="ec641-106">تدفق البيانات في حل العميل المتوقع إلى النقدية</span><span class="sxs-lookup"><span data-stu-id="ec641-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="ec641-107">يستخدم حل العميل المتوقع إلى النقدية ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Supply Chain Management وSales.</span><span class="sxs-lookup"><span data-stu-id="ec641-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span>  <span data-ttu-id="ec641-108">تسمح قوالب حل العميل المتوقع إلى النقدية المتوفرة مع ميزة تكامل البيانات بتدفق بيانات الحسابات وجهات الاتصال والمنتجات وعروض أسعار المبيعات وأوامر المبيعات وفواتير المبيعات بين Supply Chain Management وSales.</span><span class="sxs-lookup"><span data-stu-id="ec641-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="ec641-109">يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات بين Supply Chain Management وSales.</span><span class="sxs-lookup"><span data-stu-id="ec641-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="ec641-110">[![تدفق البيانات في حل العميل المتوقع إلى النقدية](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="ec641-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="ec641-111">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="ec641-111">Templates and tasks</span></span>

<span data-ttu-id="ec641-112">للوصول إلى القوالب المتوفرة، افتح [Power Apps مركز الإدارة](https://preview.admin.powerapps.com/dataintegration) .</span><span class="sxs-lookup"><span data-stu-id="ec641-112">To access the available templates, open [Power Apps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="ec641-113">حدد **المشاريع**، وبعد ذلك، في الزاوية العلوية اليسرى، حدد **مشروع جديد** لتحديد القوالب العامة.</span><span class="sxs-lookup"><span data-stu-id="ec641-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="ec641-114">يتم استخدام القالب والمهمة الأساسية التالية لمزامنة الحسابات من Sales إلى Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="ec641-114">The following template and underlying task are used to synchronize accounts from Sales to Supply Chain Management:</span></span>

- <span data-ttu-id="ec641-115">**اسم القالب في تكامل البيانات:** الحسابات (Sales إلى Fin and Ops) - مباشر</span><span class="sxs-lookup"><span data-stu-id="ec641-115">**Name of the template in Data integration:** Accounts (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="ec641-116">**اسم المهمة في المشروع:** الحسابات - العملاء</span><span class="sxs-lookup"><span data-stu-id="ec641-116">**Name of the task in the project:** Accounts - Customers</span></span>

<span data-ttu-id="ec641-117">لا توجد مهام مزامنة مطلوبة قبل إجراء مزامنة الحساب/العميل.</span><span class="sxs-lookup"><span data-stu-id="ec641-117">No synchronization tasks are required before Account/Customer synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="ec641-118">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="ec641-118">Entity set</span></span>

| <span data-ttu-id="ec641-119">ال‏‏مبيعات</span><span class="sxs-lookup"><span data-stu-id="ec641-119">Sales</span></span>    | <span data-ttu-id="ec641-120">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="ec641-120">Supply Chain Management</span></span> |
|----------|------------------------|
| <span data-ttu-id="ec641-121">الحسابات</span><span class="sxs-lookup"><span data-stu-id="ec641-121">Accounts</span></span> | <span data-ttu-id="ec641-122">العملاء V2</span><span class="sxs-lookup"><span data-stu-id="ec641-122">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="ec641-123">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="ec641-123">Entity flow</span></span>

<span data-ttu-id="ec641-124">تُدار الحسابات في Sales وتتم مزامنتها إلى Supply Chain Management: كعملاء.</span><span class="sxs-lookup"><span data-stu-id="ec641-124">Accounts are managed in Sales and synchronized to Supply Chain Management as customers.</span></span> <span data-ttu-id="ec641-125">يتم تعيين الخاصية **تتم المحافظة عليها خارجيًا** على هؤلاء العملاء إلى **نعم** لتعقب العملاء الناشئين من Sales.</span><span class="sxs-lookup"><span data-stu-id="ec641-125">The **Is Externally Maintained** property on these customers is set to **Yes** to track customers that originate from Sales.</span></span> <span data-ttu-id="ec641-126">أثناء الفوترة، يتم استخدام هذه المعلومات لتصفية الفواتير التي سيتم مزامنتها إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="ec641-126">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="ec641-127">حل العميل المتوقع إلى النقدية في Sales</span><span class="sxs-lookup"><span data-stu-id="ec641-127">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="ec641-128">يتوفر حقل **رقم الحساب** في صفحة **الحساب**.</span><span class="sxs-lookup"><span data-stu-id="ec641-128">The **Account Number** field is available on the **Account** page.</span></span> <span data-ttu-id="ec641-129">تم إنشاء مفتاح طبيعي وفريد له لدعم التكامل.</span><span class="sxs-lookup"><span data-stu-id="ec641-129">It has been made a natural and unique key in order to support the integration.</span></span> <span data-ttu-id="ec641-130">قد تؤثر ميزة المفتاح الطبيعي في حل إدارة علاقات العملاء (CRM)‬ على العملاء الذين يستخدمون حقل **رقم الحساب**، ولكنهم لا يستخدمون قيم **رقم الحساب** لكل حساب.</span><span class="sxs-lookup"><span data-stu-id="ec641-130">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** field, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="ec641-131">في الوقت الحالي، لا يدعم حل التكامل هذه الحالة.</span><span class="sxs-lookup"><span data-stu-id="ec641-131">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="ec641-132">عند إنشاء حساب جديد، إذا لم تكن قيمة **رقم الحساب** موجودة، فسيتم إنشاؤها تلقائيًا باستخدام تسلسل رقمي.</span><span class="sxs-lookup"><span data-stu-id="ec641-132">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="ec641-133">تتكون القيمة من **ACC**، يليه تسلسل رقمي متزايد ثم لاحقة من ستة أحرف.</span><span class="sxs-lookup"><span data-stu-id="ec641-133">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="ec641-134">فيما يلي مثال على ذلك: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="ec641-134">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="ec641-135">عند تطبيق حل التكامل على Sales، يقوم برنامج نصي للترقية بتعيين حقل **رقم الحساب** للحسابات الموجودة في Sales.</span><span class="sxs-lookup"><span data-stu-id="ec641-135">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** field for existing accounts in Sales.</span></span> <span data-ttu-id="ec641-136">في حال عدم وجود قيم في **رقم الحساب**، سيتم استخدام التسلسل الرقمي الذي تم ذكره في وقت سابق.</span><span class="sxs-lookup"><span data-stu-id="ec641-136">If there are no **Account Number** values, the number sequence that was mentioned earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="ec641-137">الشروط المسبقة وإعداد التعيين</span><span class="sxs-lookup"><span data-stu-id="ec641-137">Preconditions and mapping setup</span></span>

- <span data-ttu-id="ec641-138">يجب تحديث تعيين **CustomerGroupId** إلى قيمة صالحة في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ec641-138">The **CustomerGroupId** mapping must be updated to a valid value in Supply Chain Management.</span></span> <span data-ttu-id="ec641-139">يمكنك تحديد قيمة افتراضية، أو يمكنك تعيين القيمة باستخدام تعيين القيمة.</span><span class="sxs-lookup"><span data-stu-id="ec641-139">You can specify a default value, or you can set the value by using a value map.</span></span>

    <span data-ttu-id="ec641-140">قيمة القالب الافتراضية هي **10**.</span><span class="sxs-lookup"><span data-stu-id="ec641-140">The default template value is **10**.</span></span>

- <span data-ttu-id="ec641-141">عن طريق إضافة التعيينات التالية، يمكنك المساعدة على تقليل عدد التحديثات اليدوية المطلوبة في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ec641-141">By adding the following mappings, you can help reduce the number of manual updates that are required in Supply Chain Management.</span></span> <span data-ttu-id="ec641-142">يمكنك استخدام قيمة افتراضية قيمة أو تعيين قيمة من، على سبيل المثال، **البلد/المنطقة** أو **المدينة**.</span><span class="sxs-lookup"><span data-stu-id="ec641-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="ec641-143">**SiteId** – الموقع مطلوب لإنشاء بنود أوامر المبيعات وعروض الأسعار في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ec641-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="ec641-144">يمكن أخذ موقع افتراضي إما من المنتج، أو من العميل من رأس الأمر.</span><span class="sxs-lookup"><span data-stu-id="ec641-144">A default site can be taken either from the product, or from the customer from the order header.</span></span>

        <span data-ttu-id="ec641-145">قيمة القالب الافتراضية هي **1**.</span><span class="sxs-lookup"><span data-stu-id="ec641-145">The default template value is **1**.</span></span>

    - <span data-ttu-id="ec641-146">**WarehouseId** – المستودع مطلوب لمعالجة بنود أوامر المبيعات وعروض الأسعار في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ec641-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="ec641-147">يمكن أخذ مستودع افتراضي إما من المنتج، أو من العميل من رأس الأمر في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ec641-147">A default warehouse can be taken either from the product, or from the customer from the order header in Supply Chain Management.</span></span>

        <span data-ttu-id="ec641-148">قيمة القالب الافتراضية هي **13**.</span><span class="sxs-lookup"><span data-stu-id="ec641-148">The default template value is **13**.</span></span>

    - <span data-ttu-id="ec641-149">**LanguageId‎** – الموقع مطلوب لإنشاء بنود أوامر المبيعات وعروض الأسعار في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ec641-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Supply Chain Management.</span></span> <span data-ttu-id="ec641-150">بشكل افتراضي، يتم استخدام اللغة من رأس الأمر من العميل.</span><span class="sxs-lookup"><span data-stu-id="ec641-150">By default, the language from the order header from the customer is used.</span></span>

        <span data-ttu-id="ec641-151">قيمة القالب الافتراضية هي **ar-sa**.</span><span class="sxs-lookup"><span data-stu-id="ec641-151">The default template value is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="ec641-152">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="ec641-152">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="ec641-153">لا يتم تضمين الحقول **شروط الدفع** و **شروط الشحن** و **شروط التسليم** و **أسلوب الشحن** و **وضع التسليم** في التعيينات الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="ec641-153">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="ec641-154">لتعيين هذه الحقول، يجب إعداد تعيين قيمة خاصة بالبيانات الموجودة في المؤسسات التي تتم مزامنة الكيان بينها.</span><span class="sxs-lookup"><span data-stu-id="ec641-154">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="ec641-155">تبين الأشكال التوضيحية التالية مثالاً لتعيين قالب في تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="ec641-155">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="ec641-156">يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Sales إلى Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ec641-156">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

![تعيين القالب في تكامل البيانات](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a><span data-ttu-id="ec641-158">مواضيع مرتبطة</span><span class="sxs-lookup"><span data-stu-id="ec641-158">Related topics</span></span>


[<span data-ttu-id="ec641-159">العميل المتوقع إلى النقدية</span><span class="sxs-lookup"><span data-stu-id="ec641-159">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="ec641-160">مزامنة الحسابات مباشرةً من Sales إلى العملاء في Supply Chain Management‎</span><span class="sxs-lookup"><span data-stu-id="ec641-160">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="ec641-161">مزامنة جهات الاتصال مباشرةً من Sales إلى جهات الاتصال أو العملاء في Supply Chain Management‎</span><span class="sxs-lookup"><span data-stu-id="ec641-161">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="ec641-162">مزامنة أوامر المبيعات مباشرة بين Sales وSupply Chain Management</span><span class="sxs-lookup"><span data-stu-id="ec641-162">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="ec641-163">مزامنة رؤوس وبنود فواتير المبيعات مباشرةً من Supply Chain Management إلى Sales</span><span class="sxs-lookup"><span data-stu-id="ec641-163">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)

