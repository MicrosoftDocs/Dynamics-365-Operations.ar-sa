---
title: "مزامنة المنتجات من Finance and Operations إلى المنتجات في Sales"
description: "يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة المنتجات من Microsoft Dynamics 365 for Finance and Operations, Enterprise edition إلى Microsoft Dynamics 365 for Sales."
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
ms.openlocfilehash: b949701604d0cbca2728a0055d52f7385106082b
ms.contentlocale: ar-sa
ms.lasthandoff: 01/17/2018

---

# <a name="synchronize-products-from-finance-and-operations-to-products-in-sales"></a><span data-ttu-id="94790-103">مزامنة المنتجات من Finance and Operations إلى المنتجات في Sales</span><span class="sxs-lookup"><span data-stu-id="94790-103">Synchronize products from Finance and Operations to products in Sales</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="94790-104">قبل أن تتمكن من استخدام حل العميل المتوقع إلى النقدية، يجب عليك الاطلاع على [تكامل بيانات Dynamics 365](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="94790-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="94790-105">يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة المنتجات من Microsoft Dynamics 365 for Finance and Operations, Enterprise edition إلى Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="94790-105">This topic discusses the templates and underlying tasks that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="template-and-task"></a><span data-ttu-id="94790-106">القالب والمهمة</span><span class="sxs-lookup"><span data-stu-id="94790-106">Template and task</span></span>

<span data-ttu-id="94790-107">يتم استخدام القوالب والمهام الأساسية التالية لمزامنة المنتجات من Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations) إلى Microsoft Dynamics 365 for Sales (Sales).</span><span class="sxs-lookup"><span data-stu-id="94790-107">The following templates and underlying tasks are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations) to Microsoft Dynamics 365 for Sales (Sales).</span></span>

-   <span data-ttu-id="94790-108">اسم القالب: المنتجات (Fin and Ops إلى Sales)</span><span class="sxs-lookup"><span data-stu-id="94790-108">Name of template: Products (Fin and Ops to Sales)</span></span>

-   <span data-ttu-id="94790-109">اسم المهمة في المشروع: المنتجات</span><span class="sxs-lookup"><span data-stu-id="94790-109">Name of task in project: Products</span></span>

<span data-ttu-id="94790-110">مهام المزامنة المطلوبة قبل مزامنة المنتج: بلا</span><span class="sxs-lookup"><span data-stu-id="94790-110">Sync tasks required prior to Product sync: None</span></span>

## <a name="entity-set"></a><span data-ttu-id="94790-111">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="94790-111">Entity set</span></span>

| <span data-ttu-id="94790-112">**Finance and Operations**</span><span class="sxs-lookup"><span data-stu-id="94790-112">**Finance and Operations**</span></span> | <span data-ttu-id="94790-113">**CDS**</span><span class="sxs-lookup"><span data-stu-id="94790-113">**CDS**</span></span> | <span data-ttu-id="94790-114">**المبيعات**</span><span class="sxs-lookup"><span data-stu-id="94790-114">**Sales**</span></span>  |
|----------------------------|---------|------------|
| <span data-ttu-id="94790-115">منتجات قابلة للبيع تم إصدارها</span><span class="sxs-lookup"><span data-stu-id="94790-115">Sellable released products</span></span> | <span data-ttu-id="94790-116">منتج</span><span class="sxs-lookup"><span data-stu-id="94790-116">Product</span></span> | <span data-ttu-id="94790-117">المنتجات</span><span class="sxs-lookup"><span data-stu-id="94790-117">Products</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="94790-118">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="94790-118">Entity flow</span></span>

<span data-ttu-id="94790-119">تُدار المنتجات في Finance and Operations وتتم مزامنتها إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="94790-119">Products are managed in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="94790-120">يقوم كيان البيانات **منتجات قابلة للبيع تم إصدارها‬** في Finance and Operations بتصدير المنتجات القابلة للبيع فقط، مما يعني أن المنتجات تتضمن المعلومات المطلوبة لاستخدامها في أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="94790-120">The data entity **Sellable released products** in Finance and Operations only exports products that are sellable, which means that products have the information required to be used on a sales order.</span></span> <span data-ttu-id="94790-121">تنطبق القواعد نفسها عند التحقق من صحة منتج باستخدام وظيفة **التحقق من الصحة** في صفحة **المنتج الذي تم إصداره**.</span><span class="sxs-lookup"><span data-stu-id="94790-121">The same rules apply when a product is validated with the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="94790-122">يُستخدم **رقم المنتج** كمفتاح، مما يعني مزامنة متغيرات المنتج إلى CDS وSales مع **معرفات منتجات** فردية لكل **متغير منتج**.</span><span class="sxs-lookup"><span data-stu-id="94790-122">The **Product number** is used as key, meaning that product variants are synchronized to CDS and Sales with individual **Product IDs** per **Product variant**.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="94790-123">حل العميل المتوقع إلى النقدية في Sales</span><span class="sxs-lookup"><span data-stu-id="94790-123">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="94790-124">في Sales، يُضاف حقل جديد على المنتجات **تتم المحافظة عليها خارجيًا‬‏‫** للإشارة إلى المحافظة على منتج محدد خارجيًا‬‏‫‏‎.</span><span class="sxs-lookup"><span data-stu-id="94790-124">In Sales, a new field on the products **Is Externally Maintained** is added to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="94790-125">يتم تعيين القيمة إلى **نعم** بشكل افتراضي أثناء عملية الاستيراد إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="94790-125">The value is set to **Yes** by default during import to Sales.</span></span>

-   <span data-ttu-id="94790-126">**تتم المحافظة عليها خارجيًا‬‏‫ = نعم**: ينشأ المنتج من Finance and Operations ولن يكون قابلاً للتحرير في Sales.</span><span class="sxs-lookup"><span data-stu-id="94790-126">**Is Externally Maintained = Yes**: Product originates from Finance and Operations and will not be editable in Sales.</span></span>

-   <span data-ttu-id="94790-127">**تتم المحافظة عليها خارجيًا‬‏‫ = لا**: يتم إدخال المنتج مباشرةً في Sales.</span><span class="sxs-lookup"><span data-stu-id="94790-127">**Is Externally Maintained = No**: Product is entered directly in Sales.</span></span>

-   <span data-ttu-id="94790-128">**تتم المحافظة عليها خارجيًا = فارغ**: المنتج موجود في Sales قبل تمكين حل العميل المتوقع إلى النقدية.</span><span class="sxs-lookup"><span data-stu-id="94790-128">**Is Externally Maintained = Blank**: Product exists in Sales prior to enabling the Prospect to cash solution.</span></span>

<span data-ttu-id="94790-129">تُستخدم معلومات **تتم المحافظة عليها خارجيًا** لضمان إمكانية مزامنة فقط **عروض الأسعار** و**أوامر المبيعات** ذات **منتجات تتم المحافظة عليها خارجيًا** إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="94790-129">The **Is Externally Maintained** information is used to ensure that only **Quotes** and **Sales orders** with **Externally maintained products** will sync to Finance and Operations.</span></span>

<span data-ttu-id="94790-130">تُضاف **المنتجات التي تتم المحافظة عليها خارجيًا** بشكل تلقائي إلى أول **قائمة أسعار** صالحة باستخدام العملة نفسها.</span><span class="sxs-lookup"><span data-stu-id="94790-130">**Externally maintained products** are automatically added to the first valid **Price list** with the same currency.</span></span> <span data-ttu-id="94790-131">لاحظ أن القائمة مرتبة أبجديًا حسب **الاسم**.</span><span class="sxs-lookup"><span data-stu-id="94790-131">Note that the list is organized alphabetically by **Name**.</span></span> <span data-ttu-id="94790-132">يتم استخدام سعر مبيعات المنتج من Finance and Operations كسعر على **قائمة الأسعار**.</span><span class="sxs-lookup"><span data-stu-id="94790-132">The product sales price from Finance and Operations is used as price on the **Price list**.</span></span> <span data-ttu-id="94790-133">وهذا يعني أنه من الضروري وجود **قائمة أسعار** في Sales لكل **عملة بيع المنتج** في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="94790-133">This means that it is required to have a **Price list** in Sales for each **Product sales currency** in Finance and Operations.</span></span> <span data-ttu-id="94790-134">يتم تعيين العملة على المنتجات القابلة البيع إلى عمله المحاسبة في الكيان القانوني، الذي تم تصدير المنتج منه.</span><span class="sxs-lookup"><span data-stu-id="94790-134">Currency on the released sellable products is set to the accounting currency in the legal entity, from which the product is exported.</span></span>

> [!NOTE]
> <span data-ttu-id="94790-135">لن تنجح عملية مزامنة المنتج من دون **قائمة أسعار** مع العملة المطابقة.</span><span class="sxs-lookup"><span data-stu-id="94790-135">Product sync will not succeed without a **Price list** with the matching currency.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="94790-136">الشروط المسبقة وإعداد التعيين</span><span class="sxs-lookup"><span data-stu-id="94790-136">Preconditions and mapping setup</span></span>

-   <span data-ttu-id="94790-137">قبل أن تقوم بتشغيل المزامنة الأولى، يتعين عليك ملء **جدول المنتج المميز** للمنتجات الموجودة في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="94790-137">Before you run the very first sync, you must populate the **Distinct product table** for existing products in Finance and Operations.</span></span> <span data-ttu-id="94790-138">لن تتم مزامنة المنتجات الموجودة حتى استكمال هذه الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="94790-138">Existing products will not be synchronized until this job is completed.</span></span>

    -   <span data-ttu-id="94790-139">في Finance and Operations، استخدم "البحث" للبحث عن **تعبئة جدول المنتج المميز‬**.</span><span class="sxs-lookup"><span data-stu-id="94790-139">In Finance and Operations, use Search to search for **Populate distinct product table**.</span></span>

    -   <span data-ttu-id="94790-140">انقر فوق **تعبئة جدول المنتج المميز‬** لتشغيل الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="94790-140">Click the **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="94790-141">يجب تشغيل هذه الوظيفة مرة واحدة فقط.</span><span class="sxs-lookup"><span data-stu-id="94790-141">This job only needs to be run once.</span></span>

-   <span data-ttu-id="94790-142">تأكد من أن **ValueMap** المطلوب من أجل **وحدة القياس** (UOM) الخاصة بالبيع في Finance and Operations موحود في تعيين **المصدر -\> CDS SalesUnitSymbol / DefaultSellingUnitOfMeasure**.</span><span class="sxs-lookup"><span data-stu-id="94790-142">Ensure that the needed **ValueMap** for selling **Unit of measure** (UOM) in Finance and Operations exists in the **Source -\> CDS mapping SalesUnitSymbol / DefaultSellingUnitOfMeasure**.</span></span>

-   <span data-ttu-id="94790-143">قم بتحديث **معرف مؤسسة CDS Organization_OrganizationId** في **المصدر -\> CDS**.</span><span class="sxs-lookup"><span data-stu-id="94790-143">Update the **CDS Organization ID Organization_OrganizationId** in **Source -\> CDS**.</span></span>

    -   <span data-ttu-id="94790-144">قيمة القالب هي بشكل افتراضي ORG001.</span><span class="sxs-lookup"><span data-stu-id="94790-144">Template value is defaulted to ORG001.</span></span>

-   <span data-ttu-id="94790-145">قم بتحديث **ValueMap** من أجل **مجموعة الوحدات** (**defaultuomscheduleid.name**) في **CDS -\> الوجهة** لمطابقة **مجموعات الوحدات** في Sales.</span><span class="sxs-lookup"><span data-stu-id="94790-145">Update **ValueMap** for **Unit group** (**defaultuomscheduleid.name**) in **CDS -\> Destination** to match the **Unit groups** in Sales.</span></span>

    -   <span data-ttu-id="94790-146">قيمة القالب هي بشكل افتراضي **الوحدة الافتراضية**.</span><span class="sxs-lookup"><span data-stu-id="94790-146">Template value is defaulted to **Default unit**.</span></span>

-   <span data-ttu-id="94790-147">تأكد من وجود كافة وحدات القياس الخاصة ببيع المنتجات من Finance and Operations في Sales مع قيمة **قوائم انتقاء CDS**.</span><span class="sxs-lookup"><span data-stu-id="94790-147">Ensure that all products selling UOMs from Finance and Operations exist in Sales with the **CDS picklists** value.</span></span>

-   <span data-ttu-id="94790-148">تأكد من أن **قوائم الأسعار** الموجودة في Sales لكل عملة مبيعات المنتج في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="94790-148">Ensure that **Price lists** exist in Sales for each product sales currency in Finance and Operations.</span></span>

-   <span data-ttu-id="94790-149">يمكن إنشاء المنتجات في Sales بالحالة **مسودة** أو **نشطة**.</span><span class="sxs-lookup"><span data-stu-id="94790-149">Products can be created in Sales with status **Draft** or **Active**.</span></span> <span data-ttu-id="94790-150">ويتم التحكم في ذلك بواسطة **إعدادات النظام** ضمن **Sales** في Sales.</span><span class="sxs-lookup"><span data-stu-id="94790-150">This is controlled in **System settings** under **Sales** in Sales.</span></span>

    -   <span data-ttu-id="94790-151">يجب تنشيط المنتجات التي تم إنشاؤها بالحالة "مسودة" قبل إضافتها إلى **عرض أسعار** أو **أمر مبيعات**.</span><span class="sxs-lookup"><span data-stu-id="94790-151">Products created with draft status need to be activated before they can be added to **Quote** or **Sales order**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="94790-152">تعيين القالب في موحد البيانات</span><span class="sxs-lookup"><span data-stu-id="94790-152">Template mapping in data integrator</span></span>

<span data-ttu-id="94790-153">تبين الأشكال التوضيحية التالية مثالاً لتعيين قالب في موحد البيانات.</span><span class="sxs-lookup"><span data-stu-id="94790-153">The following illustrations show an example of a template mapping in data integrator.</span></span>

![تعيين القالب في موحد البيانات](./media/products-template-mapping-data-integrator-1.png)

![تعيين القالب للمنتجات في موحد البيانات](./media/products-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="94790-156">مواضيع مرتبطة</span><span class="sxs-lookup"><span data-stu-id="94790-156">Related topics</span></span>

[<span data-ttu-id="94790-157">مزامنة الحسابات من Sales إلى العملاء في Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="94790-157">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="94790-158">مزامنة جهات الاتصال من Sales لجهات الاتصال في Finance and Operations‎</span><span class="sxs-lookup"><span data-stu-id="94790-158">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="94790-159">مزامنة رؤوس وبنود عرض أسعار المبيعات‬ من Sales إلى Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="94790-159">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="94790-160">مزامنة رؤوس وبنود أوامر المبيعات من Finance and Operations إلى Sales</span><span class="sxs-lookup"><span data-stu-id="94790-160">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)

[<span data-ttu-id="94790-161">مزامنة رؤوس وبنود فواتير المبيعات من Finance and Operations إلى Sales</span><span class="sxs-lookup"><span data-stu-id="94790-161">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)


