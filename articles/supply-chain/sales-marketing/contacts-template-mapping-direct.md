---
title: مزامنة جهات الاتصال مباشرةً من Sales إلى جهات الاتصال أو العملاء في Supply Chain Management‎
description: يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة كيانات جهات الاتصال (جهات الاتصال) وجهات الاتصال (العملاء) من Dynamics 365 Sales إلى Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 141464f2ce7cb4ccfd2a8fb7a266e657e8f52015
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814111"
---
# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-supply-chain-management"></a><span data-ttu-id="a5233-103">مزامنة جهات الاتصال مباشرةً من Sales إلى جهات الاتصال أو العملاء في Supply Chain Management‎</span><span class="sxs-lookup"><span data-stu-id="a5233-103">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="a5233-104">قبل أن تتمكن من استخدام حل العميل المتوقع إلى النقدية، يجب عليك الاطلاع على [تكامل البيانات في Common Data Service للتطبيقات‏‎](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="a5233-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="a5233-105">يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة كيانات جهات الاتصال (جهات الاتصال) وجهات الاتصال (العملاء) مباشرةً من Dynamics 365 Sales إلى Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a5233-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) and Contact (Customers) entities directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="a5233-106">تدفق البيانات في حل العميل المتوقع إلى النقدية</span><span class="sxs-lookup"><span data-stu-id="a5233-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="a5233-107">يستخدم حل العميل المتوقع إلى النقدية ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Supply Chain Management وSales.</span><span class="sxs-lookup"><span data-stu-id="a5233-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="a5233-108">تسمح قوالب حل العميل المتوقع إلى النقدية المتوفرة مع ميزة تكامل البيانات بتدفق بيانات الحسابات وجهات الاتصال والمنتجات وعروض أسعار المبيعات وأوامر المبيعات وفواتير المبيعات بين Supply Chain Management وSales.</span><span class="sxs-lookup"><span data-stu-id="a5233-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="a5233-109">يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات بين Supply Chain Management وSales.</span><span class="sxs-lookup"><span data-stu-id="a5233-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="a5233-110">[![تدفق البيانات في حل العميل المتوقع إلى النقدية](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="a5233-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="a5233-111">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="a5233-111">Templates and tasks</span></span>

<span data-ttu-id="a5233-112">للوصول إلى القوالب المتوفرة، افتح [مركز إدارة PowerApps](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="a5233-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="a5233-113">حدد **المشاريع**، وبعد ذلك، في الزاوية العلوية اليسرى، حدد **مشروع جديد** لتحديد القوالب العامة.</span><span class="sxs-lookup"><span data-stu-id="a5233-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="a5233-114">يتم استخدام القوالب والمهام الأساسية التالية لمزامنة كيانات جهة الاتصال (جهات الاتصال) في Sales إلى كيانات جهة الاتصال (العملاء) في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a5233-114">The following templates and underlying tasks are used to synchronize Contact (Contacts) entities in Sales to Contact (Customers) entities in Supply Chain Management.</span></span>

- <span data-ttu-id="a5233-115">**أسماء القوالب في تكامل البيانات**</span><span class="sxs-lookup"><span data-stu-id="a5233-115">**Names of the templates in Data integration**</span></span>

    - <span data-ttu-id="a5233-116">جهات الاتصال (Sales إلى Supply Chain Management) - مباشر</span><span class="sxs-lookup"><span data-stu-id="a5233-116">Contacts (Sales to Supply Chain Management) - Direct</span></span>
    - <span data-ttu-id="a5233-117">جهات الاتصال إلى العميل (Sales إلى Supply Chain Management) - مباشر</span><span class="sxs-lookup"><span data-stu-id="a5233-117">Contacts to Customer (Sales to Supply Chain Management) - Direct</span></span>

- <span data-ttu-id="a5233-118">**أسماء المهام في مشروع تكامل البيانات**</span><span class="sxs-lookup"><span data-stu-id="a5233-118">**Names of the tasks in the Data integration project**</span></span>

    - <span data-ttu-id="a5233-119">جهات الاتصال</span><span class="sxs-lookup"><span data-stu-id="a5233-119">Contacts</span></span>
    - <span data-ttu-id="a5233-120">ContactToCustomer</span><span class="sxs-lookup"><span data-stu-id="a5233-120">ContactToCustomer</span></span>

<span data-ttu-id="a5233-121">يجب تنفيذ مهمة المزامنة التالية قبل إجراء مزامنة جهة الاتصال: الحسابات (Sales إلى Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="a5233-121">The following synchronization task is required before contact synchronization can occur: Accounts (Sales to Supply Chain Management)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="a5233-122">مجموعات الكيانات</span><span class="sxs-lookup"><span data-stu-id="a5233-122">Entity sets</span></span>

| <span data-ttu-id="a5233-123">ال‏‏مبيعات</span><span class="sxs-lookup"><span data-stu-id="a5233-123">Sales</span></span>    | <span data-ttu-id="a5233-124">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="a5233-124">Supply Chain Management</span></span> |
|----------|------------------------|
| <span data-ttu-id="a5233-125">جهات الاتصال</span><span class="sxs-lookup"><span data-stu-id="a5233-125">Contacts</span></span> | <span data-ttu-id="a5233-126">جهات اتصال CDS</span><span class="sxs-lookup"><span data-stu-id="a5233-126">CDS Contacts</span></span>           |
| <span data-ttu-id="a5233-127">جهات الاتصال</span><span class="sxs-lookup"><span data-stu-id="a5233-127">Contacts</span></span> | <span data-ttu-id="a5233-128">العملاء V2</span><span class="sxs-lookup"><span data-stu-id="a5233-128">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="a5233-129">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="a5233-129">Entity flow</span></span>

<span data-ttu-id="a5233-130">تُدار الحسابات في Sales وتتم مزامنتها إلى Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a5233-130">Contacts are managed in Sales and synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="a5233-131">يمكن أن تصبح جهة اتصال في Sales إما جهة اتصال أو عميل في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a5233-131">A contact in Sales can become either a contact or a customer in Supply Chain Management.</span></span> <span data-ttu-id="a5233-132">لتحديد ما إذا كانت جهة اتصال في Sales يفترض أن تتم مزامنتها إلى Supply Chain Management كجهة اتصال أو كعميل، يبحث النظام في الخصائص التالية في جهة الاتصال في Sales:</span><span class="sxs-lookup"><span data-stu-id="a5233-132">To determine whether a contact in Sales should be synchronized to Supply Chain Management as a contact or a customer, the system looks at the following properties on the contact in Sales:</span></span>

- <span data-ttu-id="a5233-133">**المزامنة إلى عميل في Supply Chain Management:** جهات الاتصال حيث تم تعيين **هو عميل نشط** إلى **نعم**</span><span class="sxs-lookup"><span data-stu-id="a5233-133">**Synchronization to a customer in Supply Chain Management:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="a5233-134">**المزامنة إلى جهة اتصال في Supply Chain Management:** جهات الاتصال حيث تم تعيين **هو عميل نشط** إلى **لا** وحيث تشير **الشركة** (الحساب الأصل‬/جهة الاتصال الأصل) إلى حساب (وليس إلى جهة اتصال)</span><span class="sxs-lookup"><span data-stu-id="a5233-134">**Synchronization to a contact in Supply Chain Management:** Contacts where **Is Active Customer** is set to **No** and **Company** (parent account/contact) points to an account (not a contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="a5233-135">حل العميل المتوقع إلى النقدية في Sales</span><span class="sxs-lookup"><span data-stu-id="a5233-135">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="a5233-136">تمت إضافة حقل **هو عميل نشط** جديد إلى جهة الاتصال.</span><span class="sxs-lookup"><span data-stu-id="a5233-136">A new **Is Active Customer** field has been added to the contact.</span></span> <span data-ttu-id="a5233-137">يستخدم هذا الحقل للتمييز بين جهات الاتصال التي لها نشاط في مجال المبيعات وجهات الاتصال التي ليس لديها نشاط في مجال المبيعات.</span><span class="sxs-lookup"><span data-stu-id="a5233-137">This field is used to differentiate contacts that have sales activity and contacts that don't have sales activity.</span></span> <span data-ttu-id="a5233-138">تم تعيين **هو عميل نشط** إلى **نعم** فقط لجهات الاتصال التي لديها عروض أسعار أو أوامر أو فواتير ذات صلة.</span><span class="sxs-lookup"><span data-stu-id="a5233-138">**Is Active Customer** is set to **Yes** only for contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="a5233-139">تتم مزامنة جهات الاتصال هذه فقط إلى Supply Chain Management كعملاء.</span><span class="sxs-lookup"><span data-stu-id="a5233-139">Only those contacts are synchronized to Supply Chain Management as customers.</span></span>

<span data-ttu-id="a5233-140">تمت إضافة حقل **IsCompanyAnAccount‎** جديد إلى جهة الاتصال.</span><span class="sxs-lookup"><span data-stu-id="a5233-140">A new **IsCompanyAnAccount** field has been added to the contact.</span></span> <span data-ttu-id="a5233-141">يشير هذا الحقل إلى ما إذا كانت جهة الاتصال مرتبطة بشركة (الحساب الأصل‬/جهة الاتصال الأصل) من النوع **حساب**.</span><span class="sxs-lookup"><span data-stu-id="a5233-141">This field indicates whether a contact is linked to a company (parent account/contact) of the **Account** type.</span></span> <span data-ttu-id="a5233-142">يتم استخدام هذه المعلومات لتحديد جهات الاتصال التي يجب أن تتم مزامنتها إلى Supply Chain Management كجهات اتصال.</span><span class="sxs-lookup"><span data-stu-id="a5233-142">This information is used to identify contacts that should be synchronized to Supply Chain Management as contacts.</span></span>

<span data-ttu-id="a5233-143">تمت إضافة حقل **رقم جهة الاتصال** جديد إلى جهة الاتصال للمساعدة في ضمان مفتاح طبيعي وفريد للتكامل.</span><span class="sxs-lookup"><span data-stu-id="a5233-143">A new **Contact Number** field has been added to the contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="a5233-144">عند إنشاء جهة اتصال جديدة، يتم إنشاء قيمة **رقم جهة الاتصال** بشكل تلقائي باستخدام تسلسل رقمي.</span><span class="sxs-lookup"><span data-stu-id="a5233-144">When a new contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="a5233-145">تتكون القيمة من **CON**، يليه تسلسل رقمي متزايد ثم لاحقة من ستة أحرف.</span><span class="sxs-lookup"><span data-stu-id="a5233-145">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="a5233-146">فيما يلي مثال على ذلك: **CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="a5233-146">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="a5233-147">عند تطبيق حل التكامل لـ Sales، يقوم برنامج نصي للترقية بتعيين حقل **رقم جهة الاتصال** لجهات الاتصال الموجودة باستخدام التسلسل الرقمي الذي تم ذكره سابقًا.</span><span class="sxs-lookup"><span data-stu-id="a5233-147">When the integration solution for Sales is applied, an upgrade script sets the **Contact Number** field for existing contacts by using the number sequence that was mentioned earlier.</span></span> <span data-ttu-id="a5233-148">يقوم أيضًا البرنامج النصي للترقية بتعيين الحقل **هو عميل نشط** إلى **نعم** لأي من جهات الاتصال التي لديها نشاط في مجال المبيعات.</span><span class="sxs-lookup"><span data-stu-id="a5233-148">The upgrade script also sets the **Is Active Customer** field to **Yes** for any contacts that have sales activity.</span></span>

## <a name="in-supply-chain-management"></a><span data-ttu-id="a5233-149">في Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="a5233-149">In Supply Chain Management</span></span>

<span data-ttu-id="a5233-150">توضع علامة على جهات الاتصال باستخدام الخاصية **IsContactPersonExternallyMaintained**.</span><span class="sxs-lookup"><span data-stu-id="a5233-150">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="a5233-151">تشير هذه الخاصية إلى الاحتفاظ بجهة اتصال معينة خارجيًا.</span><span class="sxs-lookup"><span data-stu-id="a5233-151">This property indicates that a given contact is maintained externally.</span></span> <span data-ttu-id="a5233-152">في هذه الحالة، يتم الاحتفاظ بجهات الاتصال التي تم الاحتفاظ بها خارجيًا في Sales.</span><span class="sxs-lookup"><span data-stu-id="a5233-152">In this case, externally maintained contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="a5233-153">الشروط المسبقة وإعداد التعيين</span><span class="sxs-lookup"><span data-stu-id="a5233-153">Preconditions and mapping setup</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="a5233-154">جهة اتصال إلى عميل</span><span class="sxs-lookup"><span data-stu-id="a5233-154">Contact to customer</span></span>

- <span data-ttu-id="a5233-155">**CustomerGroup** مطلوب في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a5233-155">**CustomerGroup** is required in Supply Chain Management.</span></span> <span data-ttu-id="a5233-156">للمساعدة على منع أخطاء المزامنة، يمكنك تحديد قيمة افتراضية في التعيين.</span><span class="sxs-lookup"><span data-stu-id="a5233-156">To help prevent synchronization errors, you can specify a default value in the mapping.</span></span> <span data-ttu-id="a5233-157">يتم عندئذٍ استخدام هذه القيمة الافتراضية إذا ترك الحقل فارغًا في Sales.</span><span class="sxs-lookup"><span data-stu-id="a5233-157">That default value is then used if the field is left blank in Sales.</span></span>

    <span data-ttu-id="a5233-158">قيمة القالب الافتراضية هي **10**.</span><span class="sxs-lookup"><span data-stu-id="a5233-158">The default template value is **10**.</span></span>

- <span data-ttu-id="a5233-159">عن طريق إضافة التعيينات التالية، يمكنك المساعدة على تقليل عدد التحديثات اليدوية المطلوبة في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a5233-159">By adding the following mappings, you can help reduce the number of manual updates that are required in Supply Chain Management.</span></span> <span data-ttu-id="a5233-160">يمكنك استخدام قيمة افتراضية قيمة أو تعيين قيمة من، على سبيل المثال، **البلد/المنطقة** أو **المدينة**.</span><span class="sxs-lookup"><span data-stu-id="a5233-160">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="a5233-161">**SiteId** - يمكن أيضًا تعريف موقع افتراضي على المنتجات في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a5233-161">**SiteId** – A default site can also be defined on products in Supply Chain Management.</span></span> <span data-ttu-id="a5233-162">الموقع مطلوب لإنشاء أوامر المبيعات وعروض الأسعار في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a5233-162">A site is required in order to generate quotations and sales orders in Supply Chain Management.</span></span>

        <span data-ttu-id="a5233-163">قيمة قالب **SiteId** غير محددة.</span><span class="sxs-lookup"><span data-stu-id="a5233-163">A template value for **SiteId** isn't defined.</span></span>

    - <span data-ttu-id="a5233-164">**WarehouseId‎** - يمكن أيضًا تعريف مستودع افتراضي على المنتجات في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a5233-164">**WarehouseId** – A default warehouse can also be defined on products in Supply Chain Management.</span></span> <span data-ttu-id="a5233-165">المستودع مطلوب لإنشاء أوامر المبيعات وعروض الأسعار في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a5233-165">A warehouse is required in order to generate quotations and sales orders in Supply Chain Management.</span></span>

        <span data-ttu-id="a5233-166">قيمة قالب **WarehouseId** غير محددة.</span><span class="sxs-lookup"><span data-stu-id="a5233-166">A template value for **WarehouseId** isn't defined.</span></span>

    - <span data-ttu-id="a5233-167">**LanguageId‎** – الموقع مطلوب لإنشاء بنود أوامر المبيعات وعروض الأسعار في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a5233-167">**LanguageId** – A language is required in order to generate quotations and sales orders in Supply Chain Management.</span></span>
    
        <span data-ttu-id="a5233-168">قيمة القالب الافتراضية هي **ar-sa**.</span><span class="sxs-lookup"><span data-stu-id="a5233-168">The default template value for is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="a5233-169">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="a5233-169">Template mapping in Data integration</span></span>

<span data-ttu-id="a5233-170">تبين الأشكال التوضيحية التالية مثالاً لتعيين قالب في تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="a5233-170">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="a5233-171">يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Sales إلى Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a5233-171">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="a5233-172">جهة اتصال إلى جهة اتصال</span><span class="sxs-lookup"><span data-stu-id="a5233-172">Contact to contact</span></span>

![تعيين القالب في موحد البيانات](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a><span data-ttu-id="a5233-174">جهة اتصال إلى عميل</span><span class="sxs-lookup"><span data-stu-id="a5233-174">Contact to customer</span></span>

![تعيين القالب في موحد البيانات](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a><span data-ttu-id="a5233-176">مواضيع مرتبطة</span><span class="sxs-lookup"><span data-stu-id="a5233-176">Related topics</span></span>

[<span data-ttu-id="a5233-177">العميل المتوقع إلى النقدية</span><span class="sxs-lookup"><span data-stu-id="a5233-177">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="a5233-178">مزامنة الحسابات مباشرةً من Sales إلى العملاء في Supply Chain Management‎</span><span class="sxs-lookup"><span data-stu-id="a5233-178">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="a5233-179">مزامنة المنتجات مباشرةً من Supply Chain Management إلى المنتجات في Sales‎‎</span><span class="sxs-lookup"><span data-stu-id="a5233-179">Synchronize products directly from Supply Chain Management to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="a5233-180">مزامنة أوامر المبيعات مباشرة بين Sales وSupply Chain Management</span><span class="sxs-lookup"><span data-stu-id="a5233-180">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="a5233-181">مزامنة رؤوس وبنود فواتير المبيعات مباشرةً من Supply Chain Management إلى Sales</span><span class="sxs-lookup"><span data-stu-id="a5233-181">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)


