---
title: "مزامنة المنتجات مباشرةً من Finance and Operations للمنتجات في Sales‎"
description: "يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة المنتجات من Microsoft Dynamics 365 for Finance and Operations, Enterprise edition إلى Microsoft Dynamics 365 for Sales."
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
ms.sourcegitcommit: 0d409b3b7f19ca31d9c720bca191f1ddba81caa3
ms.openlocfilehash: def88c291538e3ef278c51e4b87462782e222de2
ms.contentlocale: ar-sa
ms.lasthandoff: 03/13/2018

---

# <a name="synchronize-products-directly-from-finance-and-operations-to-products-in-sales"></a><span data-ttu-id="80269-103">مزامنة المنتجات مباشرةً من Finance and Operations للمنتجات في Sales‎</span><span class="sxs-lookup"><span data-stu-id="80269-103">Synchronize products directly from Finance and Operations to products in Sales</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="80269-104">قبل أن تتمكن من استخدام حل العميل المتوقع إلى النقدية، يجب عليك الاطلاع على [تكامل بيانات Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="80269-104">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

<span data-ttu-id="80269-105">يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة المنتجات مباشرةً من Microsoft Dynamics 365 for Finance and Operations, Enterprise edition إلى Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="80269-105">This topic discusses the templates and underlying tasks that are used to synchronize products directly from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="80269-106">تدفق البيانات في حل العميل المتوقع إلى النقدية</span><span class="sxs-lookup"><span data-stu-id="80269-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="80269-107">يستخدم حل العميل المتوقع إلى النقدية ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Finance and Operations وSales.</span><span class="sxs-lookup"><span data-stu-id="80269-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="80269-108">تسمح قوالب حل العميل المتوقع إلى النقدية المتوفرة مع ميزة تكامل البيانات بتدفق بيانات الحسابات وجهات الاتصال والمنتجات وعروض أسعار المبيعات وأوامر المبيعات وفواتير المبيعات بين Finance and Operations وSales.</span><span class="sxs-lookup"><span data-stu-id="80269-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="80269-109">يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات بين Finance and Operations وSales.</span><span class="sxs-lookup"><span data-stu-id="80269-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="80269-110">[![تدفق البيانات في حل العميل المتوقع إلى النقدية](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="80269-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="80269-111">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="80269-111">Templates and tasks</span></span>

<span data-ttu-id="80269-112">للوصول إلى القوالب المتوفرة، افتح [مركز إدارة PowerApps](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="80269-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="80269-113">حدد **المشاريع**، وبعد ذلك، في الزاوية العلوية اليسرى، حدد **مشروع جديد** لتحديد القوالب العامة.</span><span class="sxs-lookup"><span data-stu-id="80269-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="80269-114">يتم استخدام القوالب والمهام الأساسية التالية لمزامنة المنتجات من Finance and Operations إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="80269-114">The following template and underlying tasks are used to synchronize products from Finance and Operations to Sales.</span></span>

- <span data-ttu-id="80269-115">**اسم القالب في تكامل البيانات:** المنتجات (Fin and Ops إلى Sales) - مباشر</span><span class="sxs-lookup"><span data-stu-id="80269-115">**Name of the template in Data integration:** Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="80269-116">**اسم المهمة في مشروع تكامل البيانات:** المنتجات</span><span class="sxs-lookup"><span data-stu-id="80269-116">**Name of the task in the Data integration project:** Products</span></span>

<span data-ttu-id="80269-117">لا توجد مهام مزامنة مطلوبة قبل إجراء مزامنة المنتج.</span><span class="sxs-lookup"><span data-stu-id="80269-117">No synchronization tasks are required before product synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="80269-118">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="80269-118">Entity set</span></span>

| <span data-ttu-id="80269-119">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="80269-119">Finance and Operations</span></span>     | <span data-ttu-id="80269-120">مبيعات</span><span class="sxs-lookup"><span data-stu-id="80269-120">Sales</span></span>    |
|----------------------------|----------|
| <span data-ttu-id="80269-121">منتجات قابلة للبيع تم إصدارها</span><span class="sxs-lookup"><span data-stu-id="80269-121">Sellable released products</span></span> | <span data-ttu-id="80269-122">المنتجات</span><span class="sxs-lookup"><span data-stu-id="80269-122">Products</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="80269-123">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="80269-123">Entity flow</span></span>

<span data-ttu-id="80269-124">تُدار المنتجات في Finance and Operations وتتم مزامنتها إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="80269-124">Products are managed in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="80269-125">‏‫يقوم كيان البيانات **منتجات قابلة للبيع تم إصدارها** في Finance and Operations بتصدير المنتجات *القابلة للبيع* فقط.</span><span class="sxs-lookup"><span data-stu-id="80269-125">The **Sellable released products** data entity in Finance and Operations exports only products that are *sellable*.</span></span> <span data-ttu-id="80269-126">المنتجات القابلة للبيع هي المنتجات التي تشتمل على المعلومات المطلوبة لكي يتم استخدامها في أمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="80269-126">Sellable products are products that have the information that they require in order to be used on a sales order.</span></span> <span data-ttu-id="80269-127">تنطبق القواعد نفسها عند التحقق من صحة منتج باستخدام وظيفة **التحقق من الصحة** في صفحة **المنتج الذي تم إصداره**.</span><span class="sxs-lookup"><span data-stu-id="80269-127">The same rules apply when a product is validated by using the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="80269-128">يتم استخدام رقم المنتج كمفتاح.</span><span class="sxs-lookup"><span data-stu-id="80269-128">The product number is used as a key.</span></span> <span data-ttu-id="80269-129">لذلك، عند مزامنة متغيرات المنتج إلى Sales، يكون لكل متغير منتج معرف فردي له.</span><span class="sxs-lookup"><span data-stu-id="80269-129">Therefore, when product variants are synchronized to Sales, each product variant has an individual product ID.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="80269-130">حل العميل المتوقع إلى النقدية في Sales</span><span class="sxs-lookup"><span data-stu-id="80269-130">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="80269-131">في Sales، تمت إضافة حقل جديد على المنتجات وهو **تتم المحافظة عليها خارجيًا** للإشارة إلى المحافظة على منتج محدد خارجيًا‬‏‫‏‎.</span><span class="sxs-lookup"><span data-stu-id="80269-131">In Sales, a new **Is Externally Maintained** field has been added on products to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="80269-132">يتم تعيين القيمة إلى **نعم** بشكل افتراضي أثناء عملية الاستيراد إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="80269-132">By default, the value is set to **Yes** during an import to Sales.</span></span> <span data-ttu-id="80269-133">تتوفر القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="80269-133">The following values are available:</span></span>

- <span data-ttu-id="80269-134">**نعم** - المنتج تم إنشاؤه من Finance and Operations ولن يكون قابلاً للتحرير في Sales.</span><span class="sxs-lookup"><span data-stu-id="80269-134">**Yes** – The product originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="80269-135">**لا** - المنتج تم إدخاله مباشرةً في Sales.</span><span class="sxs-lookup"><span data-stu-id="80269-135">**No** – The product was entered directly in Sales.</span></span>
- <span data-ttu-id="80269-136">**(فارغ)** - المنتج موجود في Sales قبل تمكين ‏‫حل العميل المتوقع إلى النقدية.</span><span class="sxs-lookup"><span data-stu-id="80269-136">**(Blank)** – The product existed in Sales before the Prospect to cash solution was enabled.</span></span>

<span data-ttu-id="80269-137">يُساعد الحقل **تتم المحافظة عليها خارجيًا** في ضمان عدم مزامنة غير عروض الأسعار وأوامر المبيعات التي تشتمل على منتجات تتم المحافظة عليها خارجيًا إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="80269-137">The **Is Externally Maintained** field helps guarantee that only quotations and sales orders that have externally maintained products will be synchronized to Finance and Operations.</span></span>

<span data-ttu-id="80269-138">تُضاف المنتجات التي تتم المحافظة عليها خارجيًا بشكل تلقائي إلى أول قائمة أسعار صالحة لها العملة نفسها.</span><span class="sxs-lookup"><span data-stu-id="80269-138">Externally maintained products are automatically added to the first valid price list that has the same currency.</span></span> <span data-ttu-id="80269-139">يتم تنظيم قوائم الأسعار أبجديًا بالاسم.</span><span class="sxs-lookup"><span data-stu-id="80269-139">Price lists are organized alphabetically by name.</span></span> <span data-ttu-id="80269-140">يتم استخدام سعر مبيعات المنتج من Finance and Operations على أنه السعر على قائمة الأسعار.</span><span class="sxs-lookup"><span data-stu-id="80269-140">The product sales price from Finance and Operations is used as the price on the price list.</span></span> <span data-ttu-id="80269-141">لذلك، يجب أن تكون هناك قائمة أسعار في Sales لكل عملة مبيعات منتج في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="80269-141">Therefore, there must be a price list in Sales for every product sales currency in Finance and Operations.</span></span> <span data-ttu-id="80269-142">يتم تعيين العملة على المنتجات القابلة البيع إلى عملة المحاسبة في الكيان القانوني الذي تم تصدير المنتج منه.</span><span class="sxs-lookup"><span data-stu-id="80269-142">The currency on the released sellable products is set to the accounting currency in the legal entity that the product is exported from.</span></span>

> [!NOTE]
> <span data-ttu-id="80269-143">لن تنجح عملية مزامنة المنتج إلا في حال وجود قائمة أسعار تحتوي على عمله مطابقة.</span><span class="sxs-lookup"><span data-stu-id="80269-143">Product synchronization won't succeed unless there is a price list that has a matching currency.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="80269-144">الشروط المسبقة وإعداد التعيين</span><span class="sxs-lookup"><span data-stu-id="80269-144">Preconditions and mapping setup</span></span>

- <span data-ttu-id="80269-145">قبل أن تقوم بتشغيل المزامنة للمرة الأولى، يتعين عليك ملء جدول المنتج المميز للمنتجات الموجودة في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="80269-145">Before you run the synchronization for the first time, you must fill the Distinct product table for existing products in Finance and Operations.</span></span> <span data-ttu-id="80269-146">لن تتم مزامنة المنتجات الموجودة حتى استكمال هذه الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="80269-146">Existing products won't be synchronized until this job is completed.</span></span>

    1. <span data-ttu-id="80269-147">في Finance and Operations، استخدم "البحث" للبحث عن **تعبئة جدول المنتج المميز‬**.</span><span class="sxs-lookup"><span data-stu-id="80269-147">In Finance and Operations, use Search to search for **Populate distinct product table**.</span></span>
    2. <span data-ttu-id="80269-148">حدد **تعبئة جدول المنتج المميز‬** لتشغيل الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="80269-148">Select **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="80269-149">يجب تشغيل هذه المهمة مرة واحدة فقط.</span><span class="sxs-lookup"><span data-stu-id="80269-149">This job must be run only one time.</span></span>

- <span data-ttu-id="80269-150">تأكد من أن تعيين القيمة المطلوب لوحدة القياس الخاصة بالبيع (UOM) بين Finance and Operations وSales موجود في تعيين **SalesUnitSymbol** إلى **DefaultUnit (الاسم)**.</span><span class="sxs-lookup"><span data-stu-id="80269-150">Make sure that the required value map for the selling unit of measure (UOM) between Finance and Operations and Sales exists in the mapping of **SalesUnitSymbol** to **DefaultUnit (Name)**.</span></span>
- <span data-ttu-id="80269-151">قم بتحديث تعيين القيمة لـ**مجموعة الوحدات** (**defaultuomscheduleid.name**) لمطابقة **مجموعات الوحدات** في Sales.</span><span class="sxs-lookup"><span data-stu-id="80269-151">Update the value map for **Unit group** (**defaultuomscheduleid.name**) so that it matches **Unit groups** in Sales.</span></span>

    <span data-ttu-id="80269-152">قيمة القالب الافتراضية هي **الوحدة الافتراضية**.</span><span class="sxs-lookup"><span data-stu-id="80269-152">The default template value is **Default unit**.</span></span>

- <span data-ttu-id="80269-153">تأكد من أن وحدات القياس الخاصة بالبيع لجميع المنتجات من Finance and Operations موجودة في Sales.</span><span class="sxs-lookup"><span data-stu-id="80269-153">Make sure that the selling UOMs for all products from Finance and Operations exist in Sales.</span></span>
- <span data-ttu-id="80269-154">تأكد من وجود قوائم أسعار في Sales لكل عملة مبيعات منتج في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="80269-154">Make sure that price lists exist in Sales for every product sales currency in Finance and Operations.</span></span>
- <span data-ttu-id="80269-155">عند إنشاء منتجات في Sales، يمكن أن يكون لها الحالة **مسودة** أو **نشطة**.</span><span class="sxs-lookup"><span data-stu-id="80269-155">When products are created in Sales, they can have a status of **Draft** or **Active**.</span></span> <span data-ttu-id="80269-156">يتم التحكم في السلوك في **الإعدادات** > **الإدارة** > **إعدادات النظام** > **المبيعات** في Sales.</span><span class="sxs-lookup"><span data-stu-id="80269-156">The behavior is controlled at **Settings** > **Administration** > **System settings** > **Sales** in Sales.</span></span>

    <span data-ttu-id="80269-157">يجب تنشيط المنتجات التي لها الحالة **مسودة** عند إنشائها قبل أن يمكن إضافتها إلى عروض الأسعار أو أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="80269-157">Products that have **Draft** status when they are created must be activated before they can be added to quotations or sales orders.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="80269-158">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="80269-158">Template mapping in Data integration</span></span>

<span data-ttu-id="80269-159">يبين الشكل التوضيحي التالي مثالاً لتعيين قالب في تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="80269-159">The following illustration shows an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="80269-160">يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Sales إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="80269-160">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

![تعيين القالب في موحد البيانات](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a><span data-ttu-id="80269-162">مواضيع مرتبطة</span><span class="sxs-lookup"><span data-stu-id="80269-162">Related topics</span></span>

[<span data-ttu-id="80269-163">العميل المتوقع إلى النقدية</span><span class="sxs-lookup"><span data-stu-id="80269-163">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="80269-164">مزامنة الحسابات مباشرةً من Sales للعملاء في Finance and Operations‎</span><span class="sxs-lookup"><span data-stu-id="80269-164">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="80269-165">مزامنة جهات الاتصال مباشرةً من Sales لجهات الاتصال في Finance and Operations‎</span><span class="sxs-lookup"><span data-stu-id="80269-165">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="80269-166">مزامنة رؤوس وبنود أوامر المبيعات مباشرةً من Finance and Operations إلى Sales</span><span class="sxs-lookup"><span data-stu-id="80269-166">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="80269-167">مزامنة رؤوس وبنود فواتير المبيعات مباشرةً من Finance and Operations إلى Sales</span><span class="sxs-lookup"><span data-stu-id="80269-167">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)




