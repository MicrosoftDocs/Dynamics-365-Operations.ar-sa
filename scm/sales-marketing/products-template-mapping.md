---
title: "مزامنة المنتجات من Finance and Operations إلى المنتجات في Sales"
description: "يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة المنتجات من Microsoft Dynamics 365 for Finance and Operations, Enterprise edition إلى Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 07/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: ChristianRytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 2f14b06b57930256f9211f2085512aa589df083e
ms.contentlocale: ar-sa
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-products-from-finance-and-operations-to-products-in-sales"></a><span data-ttu-id="647d2-103">مزامنة المنتجات من Finance and Operations إلى المنتجات في Sales</span><span class="sxs-lookup"><span data-stu-id="647d2-103">Synchronize products from Finance and Operations to products in Sales</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="647d2-104">قبل أن تتمكن من استخدام حل العميل المتوقع إلى النقدية، يجب عليك الاطلاع على [تكامل بيانات Dynamics 365](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="647d2-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="647d2-105">يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة المنتجات من Microsoft Dynamics 365 for Finance and Operations, Enterprise edition إلى Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="647d2-105">This topic discusses the templates and underlying tasks that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="template-and-task"></a><span data-ttu-id="647d2-106">القالب والمهمة</span><span class="sxs-lookup"><span data-stu-id="647d2-106">Template and task</span></span>

<span data-ttu-id="647d2-107">يتم استخدام القوالب والمهام الأساسية التالية لمزامنة المنتجات من Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations) إلى Microsoft Dynamics 365 for Sales (Sales).</span><span class="sxs-lookup"><span data-stu-id="647d2-107">The following templates and underlying tasks are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations) to Microsoft Dynamics 365 for Sales (Sales).</span></span>

-   <span data-ttu-id="647d2-108">اسم القالب: المنتجات (Fin and Ops إلى Sales)</span><span class="sxs-lookup"><span data-stu-id="647d2-108">Name of template: Products (Fin and Ops to Sales)</span></span>

-   <span data-ttu-id="647d2-109">اسم المهمة في المشروع: المنتجات</span><span class="sxs-lookup"><span data-stu-id="647d2-109">Name of task in project: Products</span></span>

<span data-ttu-id="647d2-110">مهام المزامنة المطلوبة قبل مزامنة المنتج: بلا</span><span class="sxs-lookup"><span data-stu-id="647d2-110">Sync tasks required prior to Product sync: None</span></span>

## <a name="entity-set"></a><span data-ttu-id="647d2-111">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="647d2-111">Entity set</span></span>

| <span data-ttu-id="647d2-112">**Finance and Operations**</span><span class="sxs-lookup"><span data-stu-id="647d2-112">**Finance and Operations**</span></span> | <span data-ttu-id="647d2-113">**CDS**</span><span class="sxs-lookup"><span data-stu-id="647d2-113">**CDS**</span></span> | <span data-ttu-id="647d2-114">**المبيعات**</span><span class="sxs-lookup"><span data-stu-id="647d2-114">**Sales**</span></span>  |
|----------------------------|---------|------------|
| <span data-ttu-id="647d2-115">منتجات قابلة للبيع تم إصدارها</span><span class="sxs-lookup"><span data-stu-id="647d2-115">Sellable released products</span></span> | <span data-ttu-id="647d2-116">منتج</span><span class="sxs-lookup"><span data-stu-id="647d2-116">Product</span></span> | <span data-ttu-id="647d2-117">المنتجات</span><span class="sxs-lookup"><span data-stu-id="647d2-117">Products</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="647d2-118">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="647d2-118">Entity flow</span></span>

<span data-ttu-id="647d2-119">تُدار المنتجات في Finance and Operations وتتم مزامنتها إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="647d2-119">Products are managed in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="647d2-120">يقوم كيان البيانات **منتجات قابلة للبيع تم إصدارها‬** في Finance and Operations بتصدير المنتجات القابلة للبيع فقط، مما يعني أن المنتجات تتضمن المعلومات المطلوبة لاستخدامها في أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="647d2-120">The data entity **Sellable released products** in Finance and Operations only exports products that are sellable, which means that products have the information required to be used on a sales order.</span></span> <span data-ttu-id="647d2-121">تنطبق القواعد نفسها عند التحقق من صحة منتج باستخدام وظيفة **التحقق من الصحة** في صفحة **المنتج الذي تم إصداره**.</span><span class="sxs-lookup"><span data-stu-id="647d2-121">The same rules apply when a product is validated with the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="647d2-122">يُستخدم **رقم المنتج** كمفتاح، مما يعني مزامنة متغيرات المنتج إلى CDS وSales مع **معرفات منتجات** فردية لكل **متغير منتج**.</span><span class="sxs-lookup"><span data-stu-id="647d2-122">The **Product number** is used as key, meaning that product variants are synchronized to CDS and Sales with individual **Product IDs** per **Product variant**.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="647d2-123">حل العميل المتوقع إلى النقدية في Sales</span><span class="sxs-lookup"><span data-stu-id="647d2-123">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="647d2-124">في Sales، يُضاف حقل جديد على المنتجات **تتم المحافظة عليها خارجيًا‬‏‫** للإشارة إلى المحافظة على منتج محدد خارجيًا‬‏‫‏‎.</span><span class="sxs-lookup"><span data-stu-id="647d2-124">In Sales, a new field on the products **Is Externally Maintained** is added to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="647d2-125">يتم تعيين القيمة إلى **نعم** بشكل افتراضي أثناء عملية الاستيراد إلى Sales.</span><span class="sxs-lookup"><span data-stu-id="647d2-125">The value is set to **Yes** by default during import to Sales.</span></span>

-   <span data-ttu-id="647d2-126">**تتم المحافظة عليها خارجيًا‬‏‫ = نعم**: ينشأ المنتج من Finance and Operations ولن يكون قابلاً للتحرير في Sales.</span><span class="sxs-lookup"><span data-stu-id="647d2-126">**Is Externally Maintained = Yes**: Product originates from Finance and Operations and will not be editable in Sales.</span></span>

-   <span data-ttu-id="647d2-127">**تتم المحافظة عليها خارجيًا‬‏‫ = لا**: يتم إدخال المنتج مباشرةً في Sales.</span><span class="sxs-lookup"><span data-stu-id="647d2-127">**Is Externally Maintained = No**: Product is entered directly in Sales.</span></span>

-   <span data-ttu-id="647d2-128">**تتم المحافظة عليها خارجيًا = فارغ**: المنتج موجود في Sales قبل تمكين حل العميل المتوقع إلى النقدية.</span><span class="sxs-lookup"><span data-stu-id="647d2-128">**Is Externally Maintained = Blank**: Product exists in Sales prior to enabling the Prospect to cash solution.</span></span>

<span data-ttu-id="647d2-129">تُستخدم معلومات **تتم المحافظة عليها خارجيًا** لضمان إمكانية مزامنة فقط **عروض الأسعار** و**أوامر المبيعات** ذات **منتجات تتم المحافظة عليها خارجيًا** إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="647d2-129">The **Is Externally Maintained** information is used to ensure that only **Quotes** and **Sales orders** with **Externally maintained products** will sync to Finance and Operations.</span></span>

<span data-ttu-id="647d2-130">تُضاف **المنتجات التي تتم المحافظة عليها خارجيًا** بشكل تلقائي إلى أول **قائمة أسعار** صالحة باستخدام العملة نفسها.</span><span class="sxs-lookup"><span data-stu-id="647d2-130">**Externally maintained products** are automatically added to the first valid **Price list** with the same currency.</span></span> <span data-ttu-id="647d2-131">لاحظ أن القائمة مرتبة أبجديًا حسب **الاسم**.</span><span class="sxs-lookup"><span data-stu-id="647d2-131">Note that the list is organized alphabetically by **Name**.</span></span> <span data-ttu-id="647d2-132">يتم استخدام سعر مبيعات المنتج من Finance and Operations كسعر على **قائمة الأسعار**.</span><span class="sxs-lookup"><span data-stu-id="647d2-132">The product sales price from Finance and Operations is used as price on the **Price list**.</span></span> <span data-ttu-id="647d2-133">وهذا يعني أنه من الضروري وجود **قائمة أسعار** في Sales لكل **عملة بيع المنتج** في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="647d2-133">This means that it is required to have a **Price list** in Sales for each **Product sales currency** in Finance and Operations.</span></span> <span data-ttu-id="647d2-134">يتم تعيين العملة على المنتجات القابلة البيع إلى عمله المحاسبة في الكيان القانوني، الذي تم تصدير المنتج منه.</span><span class="sxs-lookup"><span data-stu-id="647d2-134">Currency on the released sellable products is set to the accounting currency in the legal entity, from which the product is exported.</span></span>

> [!NOTE]
> <span data-ttu-id="647d2-135">لن تنجح عملية مزامنة المنتج من دون **قائمة أسعار** مع العملة المطابقة.</span><span class="sxs-lookup"><span data-stu-id="647d2-135">Product sync will not succeed without a **Price list** with the matching currency.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="647d2-136">الشروط المسبقة وإعداد التعيين</span><span class="sxs-lookup"><span data-stu-id="647d2-136">Preconditions and mapping setup</span></span>

-   <span data-ttu-id="647d2-137">قبل أن تقوم بتشغيل المزامنة الأولى، يتعين عليك ملء **جدول المنتج المميز** للمنتجات الموجودة في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="647d2-137">Before you run the very first sync, you must populate the **Distinct product table** for existing products in Finance and Operations.</span></span> <span data-ttu-id="647d2-138">لن تتم مزامنة المنتجات الموجودة حتى استكمال هذه الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="647d2-138">Existing products will not be synchronized until this job is completed.</span></span>

    -   <span data-ttu-id="647d2-139">في Finance and Operations، استخدم "البحث" للبحث عن **تعبئة جدول المنتج المميز‬**.</span><span class="sxs-lookup"><span data-stu-id="647d2-139">In Finance and Operations, use Search to search for **Populate distinct product table**.</span></span>

    -   <span data-ttu-id="647d2-140">انقر فوق **تعبئة جدول المنتج المميز‬** لتشغيل الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="647d2-140">Click the **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="647d2-141">يجب تشغيل هذه الوظيفة مرة واحدة فقط.</span><span class="sxs-lookup"><span data-stu-id="647d2-141">This job only needs to be run once.</span></span>

-   <span data-ttu-id="647d2-142">تأكد من أن **ValueMap** المطلوب من أجل **وحدة القياس** (UOM) الخاصة بالبيع في Finance and Operations موحود في تعيين **المصدر -\> CDS SalesUnitSymbol / DefaultSellingUnitOfMeasure**.</span><span class="sxs-lookup"><span data-stu-id="647d2-142">Ensure that the needed **ValueMap** for selling **Unit of measure** (UOM) in Finance and Operations exists in the **Source -\> CDS mapping SalesUnitSymbol / DefaultSellingUnitOfMeasure**.</span></span>

-   <span data-ttu-id="647d2-143">تأكد من أن **الأرقام العشرية المعتمدة** لوحدة القياس تتطابق مع متطلباتك في **CDS-\> الوجهة**.</span><span class="sxs-lookup"><span data-stu-id="647d2-143">Ensure that **Decimals supported** for UOM match your requirements in **CDS -\> Destination**.</span></span> <span data-ttu-id="647d2-144">إذا احتجت إلى قيم مختلفة لكل وحدة قياس، فيمكن إجراء ذلك من خلال **ValueMap** من الوحدة، على سبيل المثال، [كل واحد: 0] & [رطل: 2].</span><span class="sxs-lookup"><span data-stu-id="647d2-144">If you require different values per UOM, this can be done with **ValueMap** from Unit, for example, [Each : 0] & [Pound : 2].</span></span>

    -   <span data-ttu-id="647d2-145">قيمة القالب هي بشكل افتراضي 0.</span><span class="sxs-lookup"><span data-stu-id="647d2-145">Template value is defaulted to 0.</span></span>

-   <span data-ttu-id="647d2-146">قم بتحديث **معرف مؤسسة CDS Organization_OrganizationId** في **المصدر -\> CDS**.</span><span class="sxs-lookup"><span data-stu-id="647d2-146">Update the **CDS Organization ID Organization_OrganizationId** in **Source -\> CDS**.</span></span>

    -   <span data-ttu-id="647d2-147">قيمة القالب هي بشكل افتراضي ORG001.</span><span class="sxs-lookup"><span data-stu-id="647d2-147">Template value is defaulted to ORG001.</span></span>

-   <span data-ttu-id="647d2-148">قم بتحديث **ValueMap** من أجل **مجموعة الوحدات** (**defaultuomscheduleid.name**) في **CDS -\> الوجهة** لمطابقة **مجموعات الوحدات** في Sales.</span><span class="sxs-lookup"><span data-stu-id="647d2-148">Update **ValueMap** for **Unit group** (**defaultuomscheduleid.name**) in **CDS -\> Destination** to match the **Unit groups** in Sales.</span></span>

    -   <span data-ttu-id="647d2-149">قيمة القالب هي بشكل افتراضي **الوحدة الافتراضية**.</span><span class="sxs-lookup"><span data-stu-id="647d2-149">Template value is defaulted to **Default unit**.</span></span>

-   <span data-ttu-id="647d2-150">تأكد من وجود كافة وحدات القياس الخاصة ببيع المنتجات من Finance and Operations في Sales مع قيمة **قوائم انتقاء CDS**.</span><span class="sxs-lookup"><span data-stu-id="647d2-150">Ensure that all products selling UOMs from Finance and Operations exist in Sales with the **CDS picklists** value.</span></span>

-   <span data-ttu-id="647d2-151">تأكد من أن **قوائم الأسعار** الموجودة في Sales لكل عملة مبيعات المنتج في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="647d2-151">Ensure that **Price lists** exist in Sales for each product sales currency in Finance and Operations.</span></span>

-   <span data-ttu-id="647d2-152">يمكن إنشاء المنتجات في Sales بالحالة **مسودة** أو **نشطة**.</span><span class="sxs-lookup"><span data-stu-id="647d2-152">Products can be created in Sales with status **Draft** or **Active**.</span></span> <span data-ttu-id="647d2-153">ويتم التحكم في ذلك بواسطة **إعدادات النظام** ضمن **Sales** في Sales.</span><span class="sxs-lookup"><span data-stu-id="647d2-153">This is controlled in **System settings** under **Sales** in Sales.</span></span>

    -   <span data-ttu-id="647d2-154">يجب تنشيط المنتجات التي تم إنشاؤها بالحالة "مسودة" قبل إضافتها إلى **عرض أسعار** أو **أمر مبيعات**.</span><span class="sxs-lookup"><span data-stu-id="647d2-154">Products created with draft status need to be activated before they can be added to **Quote** or **Sales order**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="647d2-155">تعيين القالب في موحد البيانات</span><span class="sxs-lookup"><span data-stu-id="647d2-155">Template mapping in data integrator</span></span>

<span data-ttu-id="647d2-156">تبين الأشكال التوضيحية التالية مثالاً لتعيين قالب في موحد البيانات.</span><span class="sxs-lookup"><span data-stu-id="647d2-156">The following illustrations show an example of a template mapping in data integrator.</span></span>

![تعيين القالب في موحد البيانات](./media/products-template-mapping-data-integrator-1.png)

![تعيين القالب للمنتجات في موحد البيانات](./media/products-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="647d2-159">مواضيع مرتبطة</span><span class="sxs-lookup"><span data-stu-id="647d2-159">Related topics</span></span>

[<span data-ttu-id="647d2-160">مزامنة الحسابات من Sales إلى العملاء في Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="647d2-160">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="647d2-161">مزامنة جهات الاتصال من Sales إلى جهات الاتصال أو العملاء في Finance and Operations‎</span><span class="sxs-lookup"><span data-stu-id="647d2-161">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="647d2-162">مزامنة رؤوس وبنود عروض أسعار المبيعات من Sales إلى Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="647d2-162">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)


