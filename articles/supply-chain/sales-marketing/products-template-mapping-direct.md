---
title: مزامنة المنتجات مباشرةً من Supply Chain Management إلى المنتجات في Sales‎‎
description: يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة المنتجات من Dynamics 365 Supply Chain Management إلى Dynamics 365 Sales.
author: ChristianRytt
manager: tfehr
ms.date: 06/10/2019
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
ms.openlocfilehash: 6ffd55585ff43f993876de6c669eb61e74a9fd79
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527304"
---
# <a name="synchronize-products-directly-from-supply-chain-management-to-products-in-sales"></a><span data-ttu-id="5c20f-103">مزامنة المنتجات مباشرةً من Supply Chain Management إلى المنتجات في Sales‎‎</span><span class="sxs-lookup"><span data-stu-id="5c20f-103">Synchronize products directly from Supply Chain Management to products in Sales</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="5c20f-104">قبل أن تتمكن من استخدام حل العميل المتوقع إلى النقدية، يجب عليك الاطلاع على [تكامل البيانات في Common Data Service للتطبيقات‏‎](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="5c20f-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="5c20f-105">يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة المنتجات مباشرة من Dynamics 365 Supply Chain Management إلى Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="5c20f-105">This topic discusses the templates and underlying tasks that are used to synchronize products directly from Dynamics 365 Supply Chain Management to Dynamics 365 Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="5c20f-106">تدفق البيانات في حل العميل المتوقع إلى النقدية</span><span class="sxs-lookup"><span data-stu-id="5c20f-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="5c20f-107">يستخدم حل العميل المتوقع إلى النقدية ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Supply Chain Management وSales.</span><span class="sxs-lookup"><span data-stu-id="5c20f-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="5c20f-108">تسمح قوالب حل العميل المتوقع إلى النقدية المتوفرة مع ميزة تكامل البيانات بتدفق بيانات الحسابات وجهات الاتصال والمنتجات وعروض أسعار المبيعات وأوامر المبيعات وفواتير المبيعات بين Supply Chain Management وSales.</span><span class="sxs-lookup"><span data-stu-id="5c20f-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="5c20f-109">يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات بين Supply Chain Management وSales.</span><span class="sxs-lookup"><span data-stu-id="5c20f-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="5c20f-110">[![تدفق البيانات في حل العميل المتوقع إلى النقدية](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="5c20f-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="5c20f-111">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="5c20f-111">Templates and tasks</span></span>

<span data-ttu-id="5c20f-112">للوصول إلى القوالب المتوفرة، افتح [Power Apps مركز الإدارة](https://admin.powerapps.com/dataintegration) .</span><span class="sxs-lookup"><span data-stu-id="5c20f-112">To access the available templates, open [Power Apps Admin Center](https://admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="5c20f-113">حدد **المشاريع**، وبعد ذلك، في الزاوية العلوية اليسرى، حدد **مشروع جديد** لتحديد القوالب العامة.</span><span class="sxs-lookup"><span data-stu-id="5c20f-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="5c20f-114">يتم استخدام القالب والمهام الأساسية التالية لمزامنة المنتجات من Supply Chain Management إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="5c20f-114">The following template and underlying tasks are used to synchronize products from Supply Chain Management to Sales.</span></span>

- <span data-ttu-id="5c20f-115">**اسم القالب في تكامل البيانات:** المنتجات (Supply Chain Management إلى Sales) - مباشر</span><span class="sxs-lookup"><span data-stu-id="5c20f-115">**Name of the template in Data integration:** Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="5c20f-116">**اسم المهمة في مشروع تكامل البيانات:** المنتجات</span><span class="sxs-lookup"><span data-stu-id="5c20f-116">**Name of the task in the Data integration project:** Products</span></span>

<span data-ttu-id="5c20f-117">لا توجد مهام مزامنة مطلوبة قبل إجراء مزامنة المنتج.</span><span class="sxs-lookup"><span data-stu-id="5c20f-117">No synchronization tasks are required before product synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="5c20f-118">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="5c20f-118">Entity set</span></span>

| <span data-ttu-id="5c20f-119">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5c20f-119">Supply Chain Management</span></span>    | <span data-ttu-id="5c20f-120">ال‏‏مبيعات</span><span class="sxs-lookup"><span data-stu-id="5c20f-120">Sales</span></span>    |
|----------------------------|----------|
| <span data-ttu-id="5c20f-121">منتجات قابلة للبيع تم إصدارها</span><span class="sxs-lookup"><span data-stu-id="5c20f-121">Sellable released products</span></span> | <span data-ttu-id="5c20f-122">المنتجات</span><span class="sxs-lookup"><span data-stu-id="5c20f-122">Products</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="5c20f-123">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="5c20f-123">Entity flow</span></span>

<span data-ttu-id="5c20f-124">تُدار المنتجات في Supply Chain Management وتتم مزامنتها إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="5c20f-124">Products are managed in Supply Chain Management and synchronized to Sales.</span></span> <span data-ttu-id="5c20f-125">‏‫يقوم كيان البيانات **منتجات قابلة للبيع تم إصدارها** في Supply Chain Management بتصدير المنتجات *القابلة للبيع* فقط.</span><span class="sxs-lookup"><span data-stu-id="5c20f-125">The **Sellable released products** data entity in Supply Chain Management exports only products that are *sellable*.</span></span> <span data-ttu-id="5c20f-126">المنتجات القابلة للبيع هي المنتجات التي تشتمل على المعلومات المطلوبة لكي يتم استخدامها في أمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="5c20f-126">Sellable products are products that have the information that they require in order to be used on a sales order.</span></span> <span data-ttu-id="5c20f-127">تنطبق القواعد نفسها عند التحقق من صحة منتج باستخدام وظيفة **التحقق من الصحة** في صفحة **المنتج الذي تم إصداره**.</span><span class="sxs-lookup"><span data-stu-id="5c20f-127">The same rules apply when a product is validated by using the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="5c20f-128">يتم استخدام رقم المنتج كمفتاح.</span><span class="sxs-lookup"><span data-stu-id="5c20f-128">The product number is used as a key.</span></span> <span data-ttu-id="5c20f-129">لذلك، عند مزامنة متغيرات المنتج إلى Sales، يكون لكل متغير منتج معرف فردي له.</span><span class="sxs-lookup"><span data-stu-id="5c20f-129">Therefore, when product variants are synchronized to Sales, each product variant has an individual product ID.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="5c20f-130">حل العميل المتوقع إلى النقدية في Sales</span><span class="sxs-lookup"><span data-stu-id="5c20f-130">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="5c20f-131">في Sales، تمت إضافة حقل جديد على المنتجات وهو **تتم المحافظة عليها خارجيًا** للإشارة إلى المحافظة على منتج محدد خارجيًا‬‏‫‏‎.</span><span class="sxs-lookup"><span data-stu-id="5c20f-131">In Sales, a new **Is Externally Maintained** field has been added on products to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="5c20f-132">يتم تعيين القيمة إلى **نعم** بشكل افتراضي أثناء عملية الاستيراد إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="5c20f-132">By default, the value is set to **Yes** during an import to Sales.</span></span> <span data-ttu-id="5c20f-133">تتوفر القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="5c20f-133">The following values are available:</span></span>

- <span data-ttu-id="5c20f-134">**نعم** – إنشاء المنتج من Supply Chain Management ولن يكون قابلاً للتحرير في Sales.</span><span class="sxs-lookup"><span data-stu-id="5c20f-134">**Yes** – The product originated from Supply Chain Management and won't be editable in Sales.</span></span>
- <span data-ttu-id="5c20f-135">**لا** - المنتج تم إدخاله مباشرةً في Sales.</span><span class="sxs-lookup"><span data-stu-id="5c20f-135">**No** – The product was entered directly in Sales.</span></span>
- <span data-ttu-id="5c20f-136">**(فارغ)** - المنتج موجود في Sales قبل تمكين ‏‫حل العميل المتوقع إلى النقدية.</span><span class="sxs-lookup"><span data-stu-id="5c20f-136">**(Blank)** – The product existed in Sales before the Prospect to cash solution was enabled.</span></span>

<span data-ttu-id="5c20f-137">يُساعد الحقل **تتم المحافظة عليها خارجيًا** في ضمان عدم مزامنة غير عروض الأسعار وأوامر المبيعات التي تشتمل على منتجات تتم المحافظة عليها خارجيًا إلى Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5c20f-137">The **Is Externally Maintained** field helps ensure that only quotations and sales orders that have externally maintained products will be synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="5c20f-138">تُضاف المنتجات التي تتم المحافظة عليها خارجيًا بشكل تلقائي إلى أول قائمة أسعار صالحة لها العملة نفسها.</span><span class="sxs-lookup"><span data-stu-id="5c20f-138">Externally maintained products are automatically added to the first valid price list that has the same currency.</span></span> <span data-ttu-id="5c20f-139">يتم تنظيم قوائم الأسعار أبجديًا بالاسم.</span><span class="sxs-lookup"><span data-stu-id="5c20f-139">Price lists are organized alphabetically by name.</span></span> <span data-ttu-id="5c20f-140">يتم استخدام سعر مبيعات المنتج من Supply Chain Management على أنه السعر على قائمة الأسعار.</span><span class="sxs-lookup"><span data-stu-id="5c20f-140">The product sales price from Supply Chain Management is used as the price on the price list.</span></span> <span data-ttu-id="5c20f-141">لذلك، يجب أن تكون هناك قائمة أسعار في Sales لكل عملة مبيعات منتج في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5c20f-141">Therefore, there must be a price list in Sales for every product sales currency in Supply Chain Management.</span></span> <span data-ttu-id="5c20f-142">يتم تعيين العملة على المنتجات القابلة البيع إلى عملة المحاسبة في الكيان القانوني الذي تم تصدير المنتج منه.</span><span class="sxs-lookup"><span data-stu-id="5c20f-142">The currency on the released sellable products is set to the accounting currency in the legal entity that the product is exported from.</span></span>

> [!NOTE]
> - <span data-ttu-id="5c20f-143">لن تنجح عملية مزامنة المنتج إلا في حال وجود قائمة أسعار تحتوي على عمله مطابقة.</span><span class="sxs-lookup"><span data-stu-id="5c20f-143">Product synchronization will not succeed unless there is a price list that has a matching currency.</span></span>
> - <span data-ttu-id="5c20f-144">يمكنك التحكم في قائمة الأسعار المستخدمة مع التكامل عن طريق تعيين pricelevelid.name [قائمة الأسعار الافتراضية (الاسم)] في مشروع تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="5c20f-144">You can control the used price list with the integration by mapping the pricelevelid.name [Default Price List (Name)] in the Data Integration project.</span></span> <span data-ttu-id="5c20f-145">يجب أن يكون الإدخال بجميع الأحرف الصغيرة.</span><span class="sxs-lookup"><span data-stu-id="5c20f-145">The input has to be in all lowercase letters.</span></span> <span data-ttu-id="5c20f-146">على سبيل المثال، قد يكون الإعداد الافتراضي لقائمة أسعار في Sales مسماة 'قياسي': حقل الوجهة: pricelevelid.name [قائمة الأسعار الافتراضية (الاسم)] ونوع التعيين: [ { "transformType": "افتراضي"، "defaultValue": "قياسي" } ].</span><span class="sxs-lookup"><span data-stu-id="5c20f-146">For example, the default for a price list in Sales named ‘Standard’ would be: Destination field: pricelevelid.name [Default Price List (Name)] and Map type: [ { "transformType": "Default", "defaultValue": "standard" } ].</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="5c20f-147">الشروط المسبقة وإعداد التعيين</span><span class="sxs-lookup"><span data-stu-id="5c20f-147">Preconditions and mapping setup</span></span>

- <span data-ttu-id="5c20f-148">قبل أن تقوم بتشغيل المزامنة للمرة الأولى، يتعين عليك ملء جدول المنتج المميز للمنتجات الموجودة في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5c20f-148">Before you run the synchronization for the first time, you must fill the Distinct product table for existing products in Supply Chain Management.</span></span> <span data-ttu-id="5c20f-149">لن تتم مزامنة المنتجات الموجودة حتى استكمال هذه الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="5c20f-149">Existing products won't be synchronized until this job is completed.</span></span>

    1. <span data-ttu-id="5c20f-150">في Supply Chain Management، استخدم "البحث" للبحث عن **تعبئة جدول المنتج المميز‬**.</span><span class="sxs-lookup"><span data-stu-id="5c20f-150">In Supply Chain Management, use Search to search for **Populate distinct product table**.</span></span>
    2. <span data-ttu-id="5c20f-151">حدد **تعبئة جدول المنتج المميز‬** لتشغيل الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="5c20f-151">Select **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="5c20f-152">يجب تشغيل هذه المهمة مرة واحدة فقط.</span><span class="sxs-lookup"><span data-stu-id="5c20f-152">This job must be run only one time.</span></span>

- <span data-ttu-id="5c20f-153">تأكد من أن تعيين القيمة المطلوب لوحدة القياس الخاصة بالبيع (UOM) بين Supply Chain Management وSales موجود في تعيين **SalesUnitSymbol** إلى **DefaultUnit (الاسم)**.</span><span class="sxs-lookup"><span data-stu-id="5c20f-153">Make sure that the required value map for the selling unit of measure (UOM) between Supply Chain Management and Sales exists in the mapping of **SalesUnitSymbol** to **DefaultUnit (Name)**.</span></span>
- <span data-ttu-id="5c20f-154">قم بتحديث تعيين القيمة لـ **مجموعة الوحدات** (**defaultuomscheduleid.name**) لمطابقة **مجموعات الوحدات** في Sales.</span><span class="sxs-lookup"><span data-stu-id="5c20f-154">Update the value map for **Unit group** (**defaultuomscheduleid.name**) so that it matches **Unit groups** in Sales.</span></span>

    <span data-ttu-id="5c20f-155">قيمة القالب الافتراضية هي **الوحدة الافتراضية**.</span><span class="sxs-lookup"><span data-stu-id="5c20f-155">The default template value is **Default unit**.</span></span>

- <span data-ttu-id="5c20f-156">تأكد من أن وحدات القياس الخاصة بالبيع لجميع المنتجات من Supply Chain Management موجودة في Sales.</span><span class="sxs-lookup"><span data-stu-id="5c20f-156">Make sure that the selling UOMs for all products from Supply Chain Management exist in Sales.</span></span>
- <span data-ttu-id="5c20f-157">تأكد من وجود قوائم أسعار في Sales لكل عملة مبيعات منتج في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5c20f-157">Make sure that price lists exist in Sales for every product sales currency in Supply Chain Management.</span></span>
- <span data-ttu-id="5c20f-158">عند إنشاء منتجات في Sales، يمكن أن يكون لها الحالة **مسودة** أو **نشطة**.</span><span class="sxs-lookup"><span data-stu-id="5c20f-158">When products are created in Sales, they can have a status of **Draft** or **Active**.</span></span> <span data-ttu-id="5c20f-159">يتم التحكم في السلوك في **الإعدادات** > **الإدارة** > **إعدادات النظام** > **المبيعات** في Sales.</span><span class="sxs-lookup"><span data-stu-id="5c20f-159">The behavior is controlled at **Settings** > **Administration** > **System settings** > **Sales** in Sales.</span></span>

    <span data-ttu-id="5c20f-160">يجب تنشيط المنتجات التي لها الحالة **مسودة** عند إنشائها قبل أن يمكن إضافتها إلى عروض الأسعار أو أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="5c20f-160">Products that have **Draft** status when they are created must be activated before they can be added to quotations or sales orders.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="5c20f-161">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="5c20f-161">Template mapping in Data integration</span></span>

<span data-ttu-id="5c20f-162">يبين الشكل التوضيحي التالي مثالاً لتعيين قالب في تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="5c20f-162">The following illustration shows an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="5c20f-163">يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Sales إلى Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5c20f-163">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

![تعيين القالب في موحد البيانات](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a><span data-ttu-id="5c20f-165">مواضيع مرتبطة</span><span class="sxs-lookup"><span data-stu-id="5c20f-165">Related topics</span></span>

[<span data-ttu-id="5c20f-166">العميل المتوقع إلى النقدية</span><span class="sxs-lookup"><span data-stu-id="5c20f-166">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="5c20f-167">مزامنة الحسابات مباشرةً من Sales إلى العملاء في Supply Chain Management‎</span><span class="sxs-lookup"><span data-stu-id="5c20f-167">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="5c20f-168">مزامنة جهات الاتصال مباشرةً من Sales إلى جهات الاتصال أو العملاء في Supply Chain Management‎</span><span class="sxs-lookup"><span data-stu-id="5c20f-168">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="5c20f-169">مزامنة أوامر المبيعات مباشرة بين Sales وSupply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5c20f-169">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="5c20f-170">مزامنة رؤوس وبنود فواتير المبيعات مباشرةً من Supply Chain Management إلى Sales</span><span class="sxs-lookup"><span data-stu-id="5c20f-170">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)



