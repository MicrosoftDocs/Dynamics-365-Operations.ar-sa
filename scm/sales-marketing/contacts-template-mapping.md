---
title: "مزامنة جهات الاتصال من Sales إلى جهات الاتصال أو العملاء في Finance and Operations‎"
description: "يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة جهة الاتصال (جهات الاتصال) وجهة الاتصال (العملاء) من Microsoft Dynamics 365 for Sales إلى Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
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
ms.openlocfilehash: 7a856a9460d092925a34a0733f37f89354c2ddf1
ms.contentlocale: ar-sa
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-contacts-from-sales-to-contacts-or-customers-in-finance-and-operations"></a><span data-ttu-id="1526c-103">مزامنة جهات الاتصال من Sales إلى جهات الاتصال أو العملاء في Finance and Operations‎</span><span class="sxs-lookup"><span data-stu-id="1526c-103">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="1526c-104">قبل أن تتمكن من استخدام حل العميل المتوقع إلى النقدية، يجب عليك الاطلاع على [تكامل بيانات Dynamics 365](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="1526c-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="1526c-105">يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة كيانات جهة الاتصال (جهات الاتصال) وجهة الاتصال (العملاء) من Microsoft Dynamics 365 for Sales (Sales) إلى Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="1526c-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) entities and Contact (Customers) from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="1526c-106">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="1526c-106">Templates and tasks</span></span>

<span data-ttu-id="1526c-107">يتم استخدام القوالب والمهام الأساسية التالية لمزامنة جهة الاتصال (جهات الاتصال) في Sales إلى جهة الاتصال (العملاء) في Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="1526c-107">The following templates and underlying tasks are used to synchronize Contact (Contacts) in Sales to Contact (Customers) in Finance and Operations:</span></span>

- <span data-ttu-id="1526c-108">**أسماء القوالب:**</span><span class="sxs-lookup"><span data-stu-id="1526c-108">**Names of the templates:**</span></span>

    - <span data-ttu-id="1526c-109">جهات اتصال إلى جهة اتصال (Sales إلى Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="1526c-109">Contacts to Contact (Sales to Fin and Ops)</span></span>
    - <span data-ttu-id="1526c-110">جهات اتصال إلى عميل (Sales إلى Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="1526c-110">Contacts to Customer (Sales to Fin and Ops)</span></span>

- <span data-ttu-id="1526c-111">**أسماء المهام في المشروع:**</span><span class="sxs-lookup"><span data-stu-id="1526c-111">**Names of the tasks in the project:**</span></span>

    - <span data-ttu-id="1526c-112">جهات الاتصال</span><span class="sxs-lookup"><span data-stu-id="1526c-112">Contacts</span></span>
    - <span data-ttu-id="1526c-113">ContactToCustomer</span><span class="sxs-lookup"><span data-stu-id="1526c-113">ContactToCustomer</span></span>

<span data-ttu-id="1526c-114">يجب تنفيذ مهمة مزامنة التالية قبل مزامنة جهات الاتصال: الحسابات (Sales إلى Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="1526c-114">The following synchronization task is required before Contact synchronization: Accounts (Sales to Fin and Ops)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="1526c-115">مجموعات الكيانات</span><span class="sxs-lookup"><span data-stu-id="1526c-115">Entity sets</span></span>

| <span data-ttu-id="1526c-116">ال‏‏مبيعات</span><span class="sxs-lookup"><span data-stu-id="1526c-116">Sales</span></span>    | <span data-ttu-id="1526c-117">CDS</span><span class="sxs-lookup"><span data-stu-id="1526c-117">CDS</span></span>     | <span data-ttu-id="1526c-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1526c-118">Finance and Operations</span></span> |
|----------|---------|------------------------|
| <span data-ttu-id="1526c-119">جهات الاتصال</span><span class="sxs-lookup"><span data-stu-id="1526c-119">Contacts</span></span> | <span data-ttu-id="1526c-120">جهة الاتصال</span><span class="sxs-lookup"><span data-stu-id="1526c-120">Contact</span></span> | <span data-ttu-id="1526c-121">جهات اتصال CDS</span><span class="sxs-lookup"><span data-stu-id="1526c-121">CDS Contacts</span></span>           |
| <span data-ttu-id="1526c-122">جهات الاتصال</span><span class="sxs-lookup"><span data-stu-id="1526c-122">Contacts</span></span> | <span data-ttu-id="1526c-123">الحساب</span><span class="sxs-lookup"><span data-stu-id="1526c-123">Account</span></span> | <span data-ttu-id="1526c-124">العملاء V2</span><span class="sxs-lookup"><span data-stu-id="1526c-124">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="1526c-125">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="1526c-125">Entity flow</span></span>

<span data-ttu-id="1526c-126">تُدار جهات الاتصال في Sales، وتتم مزامنتها إلى Common Data Service (CDS) وFinance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1526c-126">Contacts are managed in Sales, and are synchronized to Common Data Service (CDS) and Finance and Operations.</span></span>

<span data-ttu-id="1526c-127">يمكن أن تصبح جهة اتصال في Sales جهة اتصال في CDS وFinance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1526c-127">A Contact in Sales can become a Contact in CDS and Finance and Operations.</span></span> <span data-ttu-id="1526c-128">أو، يمكنها أن تصبح حسابًا في CDS وعميلاً في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1526c-128">Alternatively, it can become an Account in CDS and a Customer in Finance and Operations.</span></span> <span data-ttu-id="1526c-129">لتحديد ما إذا كان يجب انتقاء جهة اتصال في Sales لمزامنتها إلى CDS وFinance and Operations (على سبيل المثال، جهات اتصال في Sales &gt; جهة اتصال في CDS &gt; جهات اتصال في Finance and Operations)، يبحث النظام عن الخصائص التالية على جهة الاتصال في Sales.</span><span class="sxs-lookup"><span data-stu-id="1526c-129">To determine whether a contact should be picked up in Sales for synchronization to CDS and Finance and Operations (for example, Contacts in Sales &gt; Contact in CDS &gt; Contacts in Finance and Operations), the system looks at the following properties on Contact in Sales:</span></span>

- <span data-ttu-id="1526c-130">**مزامنة إلى الحساب في CDS وFinance and Operations:** جهات الاتصال حيث تم تعيين **هو عميل نشط** إلى **نعم**</span><span class="sxs-lookup"><span data-stu-id="1526c-130">**Sync to Account in CDS and Customer in Finance and Operations:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="1526c-131">**مزامنة إلى جهة الاتصال في CDS وFinance and Operations:** جهات الاتصال حيث تم تعيين **هو عميل نشط** إلى **لا** وحيث تشير **الشركة** (الحساب الأصل‬/جهة الاتصال الأصل) إلى حساب (وليس إلى جهة اتصال)</span><span class="sxs-lookup"><span data-stu-id="1526c-131">**Sync to Contact in CDS and Contact in Finance and Operations:** Contacts where **Is Active Customer** is set to **No** and **Company** (Parent Account/Contact) points to an Account (not a Contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="1526c-132">حل العميل المتوقع إلى النقدية في Sales</span><span class="sxs-lookup"><span data-stu-id="1526c-132">Prospect to cash solution for Sales</span></span> 

<span data-ttu-id="1526c-133">تمت إضافة حقل **هو عميل نشط** جديد إلى جهة الاتصال.</span><span class="sxs-lookup"><span data-stu-id="1526c-133">A new **Is Active Customer** field has been added to the Contact.</span></span> <span data-ttu-id="1526c-134">يستخدم هذا الحقل للتمييز بين جهات الاتصال التي لها نشاط في مجال المبيعات وجهات الاتصال التي ليس لديها نشاط في مجال المبيعات.</span><span class="sxs-lookup"><span data-stu-id="1526c-134">This field is used to differentiate Contacts that have sales activity and Contacts that don't have sales activity.</span></span> <span data-ttu-id="1526c-135">تم تعيين **هو عميل نشط** إلى **نعم** فقط لجهات الاتصال التي لديها عروض أسعار أو أوامر أو فواتير ذات صلة.</span><span class="sxs-lookup"><span data-stu-id="1526c-135">**Is Active Customer** is set to **Yes** only for Contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="1526c-136">تتم مزامنة جهات الاتصال هذه فقط إلى Finance and Operations كعملاء.</span><span class="sxs-lookup"><span data-stu-id="1526c-136">Only those Contacts are synchronized to Finance and Operations as Customers.</span></span>

<span data-ttu-id="1526c-137">تمت إضافة حقل **IsCompanyAnAccount‎** جديد إلى جهة الاتصال.</span><span class="sxs-lookup"><span data-stu-id="1526c-137">A new **IsCompanyAnAccount** field has been added to the Contact.</span></span> <span data-ttu-id="1526c-138">يستخدم هذا الحقل للإشارة إلى ما إذا كانت جهة الاتصال مرتبطة بشركة (الحساب الأصل‬/جهة الاتصال الأصل) من النوع **حساب**.</span><span class="sxs-lookup"><span data-stu-id="1526c-138">This field is used to indicate whether a Contact is linked to a Company (Parent Account/Contact) of the **Account** type.</span></span> <span data-ttu-id="1526c-139">يتم استخدام هذه المعلومات لتحديد جهات الاتصال التي يجب أن تتم مزامنتها إلى Finance and Operations كجهات اتصال.</span><span class="sxs-lookup"><span data-stu-id="1526c-139">This information is used to identify Contacts that should be synchronized to Finance and Operations as Contacts.</span></span>

<span data-ttu-id="1526c-140">تمت إضافة حقل **رقم جهة الاتصال** جديد إلى جهة الاتصال للمساعدة في ضمان مفتاح طبيعي وفريد للتكامل.</span><span class="sxs-lookup"><span data-stu-id="1526c-140">A new **Contact Number** field has been added to the Contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="1526c-141">عند إنشاء جهة اتصال جديدة، يتم إنشاء **رقم جهة الاتصال** بشكل تلقائي باستخدام تسلسل رقمي.</span><span class="sxs-lookup"><span data-stu-id="1526c-141">When a new Contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="1526c-142">تتكون القيمة من **CON**، يليه تسلسل رقمي متزايد ثم لاحقة من ستة أحرف.</span><span class="sxs-lookup"><span data-stu-id="1526c-142">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="1526c-143">فيما يلي مثال على ذلك: **CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="1526c-143">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="1526c-144">عند إضافة حل تكامل Sales إلى Sales، يقوم برنامج نصي للترقية بتعيين حقل **رقم جهة الاتصال** لجهات الاتصال الموجودة باستخدام التسلسل الرقمي الذي تمت مناقشته سابقًا.</span><span class="sxs-lookup"><span data-stu-id="1526c-144">When the integration solution for Sales is added to Sales, an upgrade script sets the **Contact Number** field for existing Contacts by using the number sequence that was discussed earlier.</span></span> <span data-ttu-id="1526c-145">يقوم أيضًا البرنامج النصي للترقية بتعيين الحقل **هو عميل نشط** إلى **نعم** لأي من جهات الاتصال التي لديها نشاط في مجال المبيعات.</span><span class="sxs-lookup"><span data-stu-id="1526c-145">The upgrade script also sets the **Is Active Customer** field to **Yes** for any Contacts that have sales activity.</span></span>

## <a name="in-finance-and-operations"></a><span data-ttu-id="1526c-146">في Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1526c-146">In Finance and Operations</span></span> 

<span data-ttu-id="1526c-147">توضع علامة على جهات الاتصال باستخدام الخاصية **IsContactPersonExternallyMaintained**.</span><span class="sxs-lookup"><span data-stu-id="1526c-147">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="1526c-148">تشير هذه الخاصية إلى المحافظة على جهة اتصال معينة خارجيًا.</span><span class="sxs-lookup"><span data-stu-id="1526c-148">This property indicates that a given Contact is maintained externally.</span></span> <span data-ttu-id="1526c-149">في هذه الحالة، تتم المحافظة على جهات الاتصال التي تتم المحافظة عليها خارجيًا في Sales.</span><span class="sxs-lookup"><span data-stu-id="1526c-149">In this case, externally maintained Contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="1526c-150">الشروط المسبقة وإعداد التعيين</span><span class="sxs-lookup"><span data-stu-id="1526c-150">Preconditions and mapping setup</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="1526c-151">جهة اتصال إلى جهة اتصال</span><span class="sxs-lookup"><span data-stu-id="1526c-151">Contact to Contact</span></span>

- <span data-ttu-id="1526c-152">قم بتحديث **معرف مؤسسة** في تعيين **المصدر &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="1526c-152">Update **CDS Organization ID** in the **Source &gt; CDS** mapping.</span></span>

    - <span data-ttu-id="1526c-153">قيمة القالب الافتراضية للخيار **Organization_OrganizationId [معرف المؤسسة]** هي **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="1526c-153">The default template value for **Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>
    - <span data-ttu-id="1526c-154">قيمة القالب الافتراضية للخيار **PrimaryAccount_Organization_OrganizationId [معرف المؤسسة]** هي **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="1526c-154">The default template value for **PrimaryAccount_Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>

- <span data-ttu-id="1526c-155">يجب ملء **"كود بلد/منطقة العنوان** في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1526c-155">**Address Country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="1526c-156">لتجنب أخطاء المزامنة، يمكنك تحديد قيمة افتراضية في تعيين **CDS &gt; Operations**.</span><span class="sxs-lookup"><span data-stu-id="1526c-156">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Operations** mapping.</span></span> <span data-ttu-id="1526c-157">يتم عندئذٍ استخدام هذه القيمة الافتراضية إذا ترك الحقل فارغًا في Sales.</span><span class="sxs-lookup"><span data-stu-id="1526c-157">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="1526c-158">قيمة القالب الافتراضية للخيار **PrimaryAddressCountryRegionISOCode** هي **USA**.</span><span class="sxs-lookup"><span data-stu-id="1526c-158">The default template value for **PrimaryAddressCountryRegionISOCode** is **USA**.</span></span>
- <span data-ttu-id="1526c-159">تأكد من وجود قيمة للحقل التالي في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1526c-159">Make sure that a value for the following field exists in Finance and Operations.</span></span> <span data-ttu-id="1526c-160">إذا لم تكن المعلومات مطلوبة في Finance and Operations، يمكنك إزالة التعيين من تعيين **CDS &gt; الوجهة**.</span><span class="sxs-lookup"><span data-stu-id="1526c-160">If the information isn't required in Finance and Operations, you can remove the mapping from the **CDS &gt; Destination** mapping.</span></span>

    - <span data-ttu-id="1526c-161">**اسم الحقل في Finance and Operations:** القرار</span><span class="sxs-lookup"><span data-stu-id="1526c-161">**Field name in Finance and Operations:** Decision</span></span>
    - <span data-ttu-id="1526c-162">**التعيين:** PrimaryAccountRole = DecisionMakingRole</span><span class="sxs-lookup"><span data-stu-id="1526c-162">**Mapping:** PrimaryAccountRole = DecisionMakingRole</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="1526c-163">جهة اتصال إلى عميل</span><span class="sxs-lookup"><span data-stu-id="1526c-163">Contact to Customer</span></span>

- <span data-ttu-id="1526c-164">قم بتحديث **معرف مؤسسة** في تعيين **المصدر &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="1526c-164">Update **CDS Organization ID** in the **Source &gt; CDS** mapping.</span></span> <span data-ttu-id="1526c-165">قيمة القالب الافتراضية للخيار **Organization_OrganizationId [معرف المؤسسة]** هي **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="1526c-165">The default template value for **Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>
- <span data-ttu-id="1526c-166">يجب ملء **"كود بلد/منطقة العنوان** في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1526c-166">**Address Country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="1526c-167">لتجنب أخطاء المزامنة، يمكنك تحديد قيمة افتراضية في تعيين **CDS &gt; الوجهة**.</span><span class="sxs-lookup"><span data-stu-id="1526c-167">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Destination** mapping.</span></span> <span data-ttu-id="1526c-168">يتم عندئذٍ استخدام هذه القيمة الافتراضية إذا ترك الحقل فارغًا في Sales.</span><span class="sxs-lookup"><span data-stu-id="1526c-168">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="1526c-169">قيمة القالب الافتراضية للخيار **PrimaryAddressCountryRegionISOCode** هي **USA**.</span><span class="sxs-lookup"><span data-stu-id="1526c-169">The default template value for **PrimaryAddressCountryRegionISOCode** is **USA**.</span></span>
- <span data-ttu-id="1526c-170">يجب ملء **CustomerGroup** في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1526c-170">**CustomerGroup** is required in Finance and Operations.</span></span> <span data-ttu-id="1526c-171">لتجنب أخطاء المزامنة، يمكنك تحديد قيمة افتراضية في تعيين **CDS &gt; الوجهة**.</span><span class="sxs-lookup"><span data-stu-id="1526c-171">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Destination** mapping.</span></span> <span data-ttu-id="1526c-172">يتم عندئذٍ استخدام هذه القيمة الافتراضية إذا ترك الحقل فارغًا في Sales.</span><span class="sxs-lookup"><span data-stu-id="1526c-172">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="1526c-173">قيمة القالب الافتراضية للخيار **CustomerGroupId** هي **10**.</span><span class="sxs-lookup"><span data-stu-id="1526c-173">The default template value for **CustomerGroupId** is **10**.</span></span>
- <span data-ttu-id="1526c-174">عن طريق إضافة التعيينات التالية من **‎CDS &gt;الوجهة**، يمكنك المساعدة على تقليل عدد التحديثات اليدوية في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1526c-174">By adding the following mappings from **CDS &gt; Destination**, you can help reduce the number of manual updates that are in Finance and Operations.</span></span> <span data-ttu-id="1526c-175">يمكنك استخدام قيمة افتراضية قيمة أو تعيين قيمة من، على سبيل المثال، **البلد/المنطقة** أو **المدينة**.</span><span class="sxs-lookup"><span data-stu-id="1526c-175">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="1526c-176">**SiteId** - يمكن أيضًا تعريف موقع افتراضي على المنتجات في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1526c-176">**SiteId** - A default site can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="1526c-177">يكون الموقع مطلوبًا لإنشاء بنود أوامر المبيعات وعروض الأسعار في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1526c-177">A site is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="1526c-178">قيمة قالب **SiteId** غير محددة.</span><span class="sxs-lookup"><span data-stu-id="1526c-178">A template value for **SiteId** isn't defined.</span></span>
    - <span data-ttu-id="1526c-179">**WarehouseId** - يمكن أيضًا تعريف مستودع افتراضي على المنتجات في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1526c-179">**WarehouseId** - A default warehouse can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="1526c-180">يكون المستودع مطلوبًا لإنشاء بنود أوامر المبيعات وعروض الأسعار في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1526c-180">A warehouse is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="1526c-181">قيمة قالب **WarehouseId** غير محددة.</span><span class="sxs-lookup"><span data-stu-id="1526c-181">A template value for **WarehouseId** isn't defined.</span></span>
    - <span data-ttu-id="1526c-182">**LanguageId** – اللغة مطلوبة لإنشاء أوامر المبيعات وعروض الأسعار في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1526c-182">**LanguageId** - A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="1526c-183">قيمة القالب الافتراضية للخيار **LanguageId** هي **en-us**.</span><span class="sxs-lookup"><span data-stu-id="1526c-183">The default template value for **LanguageId** is **en-us**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="1526c-184">تعيين القالب في موحد البيانات</span><span class="sxs-lookup"><span data-stu-id="1526c-184">Template mapping in data integrator</span></span>

<span data-ttu-id="1526c-185">تبين الأشكال التوضيحية التالية مثالاً لتعيين قالب في موحد البيانات.</span><span class="sxs-lookup"><span data-stu-id="1526c-185">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="1526c-186">جهة اتصال إلى جهة اتصال</span><span class="sxs-lookup"><span data-stu-id="1526c-186">Contact to Contact</span></span>

![تعيين القالب في موحد البيانات](./media/contacts-template-mapping-data-integrator-1.png)

![تعيين القالب لجهات الاتصال في موحد البيانات](./media/contacts-template-mapping-data-integrator-2.png)

### <a name="contact-to-customer"></a><span data-ttu-id="1526c-189">جهة اتصال إلى عميل</span><span class="sxs-lookup"><span data-stu-id="1526c-189">Contact to Customer</span></span>

![تعيين القالب في موحد البيانات](./media/contacts-template-mapping-data-integrator-3.png)

![تعيين القالب لجهات الاتصال في موحد البيانات](./media/contacts-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="1526c-192">مواضيع مرتبطة</span><span class="sxs-lookup"><span data-stu-id="1526c-192">Related topics</span></span>

[<span data-ttu-id="1526c-193">مزامنة المنتجات من Finance and Operations إلى المنتجات في Sales</span><span class="sxs-lookup"><span data-stu-id="1526c-193">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="1526c-194">مزامنة الحسابات من Sales إلى العملاء في Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1526c-194">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="1526c-195">مزامنة رؤوس وبنود عروض أسعار المبيعات من Sales إلى Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1526c-195">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

