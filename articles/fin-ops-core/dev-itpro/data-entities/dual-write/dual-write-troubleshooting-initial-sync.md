---
title: استكشاف المشاكل وإصلاحها أثناء المزامنة الأولية
description: يوفر هذا الموضوع استكشاف الأخطاء وإصلاحها الذي يمكن أن يساعدك في إصلاح المشكلات التي قد تحدث أثناء المزامنة الأولية.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 10065039fce441d7f96f700ff826d959e96f2479
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410071"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="4c62d-103">استكشاف المشاكل وإصلاحها أثناء المزامنة الأولية</span><span class="sxs-lookup"><span data-stu-id="4c62d-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4c62d-104">يوفر هذا الموضوع معلومات حول استكشاف أخطاء تكامل الكتابة الثنائية وإصلاحها بين تطبيقات Finance and Operations وCommon Data Service.</span><span class="sxs-lookup"><span data-stu-id="4c62d-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="4c62d-105">على وجه التحديد، يوفر هذا الموضوع المعلومات التي يمكن أن تساعدك في إصلاح المشكلات التي قد تحدث أثناء المزامنة الأولية.</span><span class="sxs-lookup"><span data-stu-id="4c62d-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4c62d-106">قد تتطلب بعض المشكلات التي يتناولها هذا الموضوع إما دور إدارة النظام أو بيانات اعتماد مسؤول مستأجر  Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="4c62d-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="4c62d-107">يوضح القسم الخاص بكل مشكلة ما إذا كانت هناك حاجة إلى دور محدد أو بيانات اعتماد.</span><span class="sxs-lookup"><span data-stu-id="4c62d-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="4c62d-108">التحقق من أخطاء المزامنة الأولية في تطبيق Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4c62d-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="4c62d-109">بعد تمكين قوالب التعيين، يجب أن تكون حالة المخططات **قيد التشغيل**.</span><span class="sxs-lookup"><span data-stu-id="4c62d-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="4c62d-110">إذا لم تكن الحالة **قيد التشغيل**، حدثت أخطاء أثناء المزامنة الأولية.</span><span class="sxs-lookup"><span data-stu-id="4c62d-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="4c62d-111">لعرض الأخطاء، حدد علامة التبويب **تفاصيل المزامنة الأولية** في صفحة **الكتابة الثنائية**.</span><span class="sxs-lookup"><span data-stu-id="4c62d-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![علامة التبويب تفاصيل المزامنة الأولية](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="4c62d-113">لا يمكنك إكمال المزامنة الأولية: 400 طلب غير صحيح</span><span class="sxs-lookup"><span data-stu-id="4c62d-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="4c62d-114">**الدور المطلوب لإصلاح المشكلة:** مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="4c62d-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="4c62d-115">قد تتلقى رسالة الخطأ التالية عند محاولة تشغيل التعيين والمزامنة الأولية:</span><span class="sxs-lookup"><span data-stu-id="4c62d-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="4c62d-116">*أرجع الخادم البعيد الخطأ: (400) طلب غير صحيح.)، صادف تصدير AX خطأ*</span><span class="sxs-lookup"><span data-stu-id="4c62d-116">*The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="4c62d-117">فيما يلي مثال لرسالة الخطأ الكاملة.</span><span class="sxs-lookup"><span data-stu-id="4c62d-117">Here is an example of the full error message.</span></span>

```console
Dual write Initial Sync completed with status: Error. Following are the details:
Executed leg: From AX Financial dimensions to CRM msdyn_dimensionattributes
with exported records count: 0, ImportRecordsErrorCount: 0,
ImportRecordsInsertedCount: 0 and ImportRecordsUpdatedCount: 0
ErrorsDetails:
Dual write Initial sync failed
Message: ([Bad Request], The remote server returned an error: (400) Bad Request.), AX export encountered an error
Stacktrace: at
Microsoft.Dynamics.Integrator.QueryGenerator.AxClient.\<ExportAxPackage\>d__16.MoveNext()
in X:\\bt\\1024532\\repo\\src\\Core\\QueryGenerator\\AxClient.cs:line 265
\--- End of stack trace from previous location where exception was thrown ---
at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
at Microsoft.D365.ServicePlatform.Context.ServiceContext.Activity.\<ExecuteAsync\>d__11\`2.MoveNext()
\--- End of stack trace from previous location where exception was thrown ---
```

<span data-ttu-id="4c62d-118">في حاله حدوث هذا الخطأ باستمرار، ولا يمكنك إكمال المزامنة الأولية، فاتبع هذه الخطوات لإصلاح هذه المشكلة.</span><span class="sxs-lookup"><span data-stu-id="4c62d-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="4c62d-119">سجل الدخول إلى الجهاز الظاهري (VM) لتطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4c62d-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="4c62d-120">افتح وحدة التحكم بالإدارة لـ Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4c62d-120">Open Microsoft Management Console.</span></span>
3. <span data-ttu-id="4c62d-121">في جزء **الخدمات**، تأكد من تشغيل خدمة إطار عمل التصدير الخاص باستيراد بيانات Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="4c62d-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="4c62d-122">وأعد تشغيلها إذا تم إيقافها، لأن المزامنة الأولية تتطلب ذلك.</span><span class="sxs-lookup"><span data-stu-id="4c62d-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="4c62d-123">خطأ المزامنة الأولية: 403 ممنوع</span><span class="sxs-lookup"><span data-stu-id="4c62d-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="4c62d-124">قد تتلقى رسالة الخطأ التالية أثناء المزامنة الأولية:</span><span class="sxs-lookup"><span data-stu-id="4c62d-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="4c62d-125">*(\[ممنوع\]، أرجع الخادم البعيد خطأ: (403) ممنوع.)، صادف تصدير AX خطأ*</span><span class="sxs-lookup"><span data-stu-id="4c62d-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="4c62d-126">لإصلاح المشكلة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="4c62d-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="4c62d-127">قم بتسجيل الدخول إلى تطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4c62d-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="4c62d-128">في صفحة **تطبيقات Azure Active Directory**، احذف عميل **DtAppID**، ثم أضفه مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="4c62d-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![قائمة تطبيقات Azure AD](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a><span data-ttu-id="4c62d-130">حالات فشل المراجع الذاتية أو المراجع الدائرية أثناء المزامنة الأولية</span><span class="sxs-lookup"><span data-stu-id="4c62d-130">Self-reference or circular-reference failures during initial synchronization</span></span>

<span data-ttu-id="4c62d-131">قد تتلقى رسائل خطأ عند وجود مراجع ذاتية أو مراجع دائرية لدى أي من تعييناتك.</span><span class="sxs-lookup"><span data-stu-id="4c62d-131">You might receive an error messages if any of your mappings have self-references or circular references.</span></span> <span data-ttu-id="4c62d-132">تقع الأخطاء ضمن هذه الفئات:</span><span class="sxs-lookup"><span data-stu-id="4c62d-132">The errors fall into these categories:</span></span>

- [<span data-ttu-id="4c62d-133">تعيين كيان المورّدون V2 في مقابل msdyn_vendors</span><span class="sxs-lookup"><span data-stu-id="4c62d-133">Vendors V2 to msdyn_vendors entity mapping</span></span>](#error-vendor-map)
- [<span data-ttu-id="4c62d-134">تعيين كيان العملاء V3 في مقابل الحسابات</span><span class="sxs-lookup"><span data-stu-id="4c62d-134">Customers V3 to Accounts entity mapping</span></span>](#error-customer-map)

## <a name="resolve-an-error-in-vendors-v2-to-msdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a><span data-ttu-id="4c62d-135">حل خطأ في تعيين كيان المورّدون V2 في مقابل msdyn_vendors</span><span class="sxs-lookup"><span data-stu-id="4c62d-135">Resolve an error in Vendors V2 to msdyn_vendors entity mapping</span></span>

<span data-ttu-id="4c62d-136">قد تواجه أخطاء المزامنة الأولية التالية على تعيين **المورّدون V2** في مقابل **msdyn_vendors** إذا تضمنت الكيانات سجلات موجودة لديها قيم في الحقلين **PrimaryContactPersonId** و**InvoiceVendorAccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="4c62d-136">You might run into the following initial sync errors on the **Vendors V2** to **msdyn_vendors** mapping if the entities have existing records with values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields.</span></span> <span data-ttu-id="4c62d-137">يعود سبب ذلك إلى كون **InvoiceVendorAccountNumber** عبارة عن حقل مرجع ذاتي و**PrimaryContactPersonId** عبارة عن مرجع دائري في تعيين المورّد.</span><span class="sxs-lookup"><span data-stu-id="4c62d-137">This because **InvoiceVendorAccountNumber** is a self-referencing field, and **PrimaryContactPersonId** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="4c62d-138">*تعذّر حل guid للحقل: <field>. لم يتم العثور على قيمة البحث: <value>. جرّب عنوان (عناوين) URL هذا للتأكد من وجود البيانات المرجعية: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span><span class="sxs-lookup"><span data-stu-id="4c62d-138">*Couldn't resolve the guid for the field: <field>. The lookup was not found: <value>. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span></span>

<span data-ttu-id="4c62d-139">فيما يلي بعض الأمثلة:</span><span class="sxs-lookup"><span data-stu-id="4c62d-139">Here are a couple of examples:</span></span>

- <span data-ttu-id="4c62d-140">*تعذّر حل guid للحقل: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. لم يتم العثور على قيمة البحث: 000056. جرّب عنوان (عناوين) URL هذا للتأكد من وجود البيانات المرجعية: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span><span class="sxs-lookup"><span data-stu-id="4c62d-140">*Couldn't resolve the guid for the field: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span></span>
- <span data-ttu-id="4c62d-141">*تعذّر حل guid للحقل: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. لم يتم العثور على قيمة البحث: V24-1. جرّب عنوان (عناوين) URL هذا للتأكد من وجود البيانات المرجعية: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*</span><span class="sxs-lookup"><span data-stu-id="4c62d-141">*Couldn't resolve the guid for the field: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. The lookup was not found: V24-1. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*</span></span>

<span data-ttu-id="4c62d-142">إذا كانت لديك سجلات تتضمن قيمًا في هذه الحقول في كيان المورّد، فاتبع الخطوات في القسم أدناه لإكمال المزامنة الأولية.</span><span class="sxs-lookup"><span data-stu-id="4c62d-142">If you have records with values in these fields in the vendor entity follow the steps in the below section to complete initial sync successfully.</span></span>

1. <span data-ttu-id="4c62d-143">في التطبيق Finance and Operations، احذف الحقلين **PrimaryContactPersonId** و**InvoiceVendorAccountNumber** من التعيين واحفظ التغييرات.</span><span class="sxs-lookup"><span data-stu-id="4c62d-143">In the Finance and Operations app, delete the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields from the mapping and save the changes.</span></span>

    1. <span data-ttu-id="4c62d-144">انتقل إلى صفحة تعيين الكتابة المزدوجة **المورّدون V2 (msdyn_vendors)**، وحدد علامة تبويب **تعيينات الكيان**. في عامل التصفية الأيسر، حدد **Finance and Operations apps.Vendors V2**.</span><span class="sxs-lookup"><span data-stu-id="4c62d-144">Navigate to the dual-write mapping page for **Vendors V2 (msdyn_vendors)**, and select the **Entity mappings** tab. In the left filter, select **Finance and Operations apps.Vendors V2**.</span></span> <span data-ttu-id="4c62d-145">في عامل التصفية الأيمن، حدد **Sales.Vendor**</span><span class="sxs-lookup"><span data-stu-id="4c62d-145">In the right filter, select **Sales.Vendor**.</span></span>

    2. <span data-ttu-id="4c62d-146">ابحث عن **primarycontactperson** للعثور على الحقل المصدر **PrimaryContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="4c62d-146">Search for **primarycontactperson** to find the source field **PrimaryContactPersonId**.</span></span>
    
    3. <span data-ttu-id="4c62d-147">انقر فوق زر **الإجراءات**، وحدد **حذف**.</span><span class="sxs-lookup"><span data-stu-id="4c62d-147">Click the **Actions** button, and select **Delete**.</span></span>
    
        ![مرجع ذاتي أو دائري 3](media/vend_selfref3.png)
    
    4. <span data-ttu-id="4c62d-149">كرر الإجراء لحذف الحقل **InvoiceVendorAccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="4c62d-149">Repeat to delete the **InvoiceVendorAccountNumber** field.</span></span>
    
        ![مرجع ذاتي أو دائري 4](media/vend-selfref4.png)
    
    5. <span data-ttu-id="4c62d-151">احفظ تغييرات التعيين.</span><span class="sxs-lookup"><span data-stu-id="4c62d-151">Save the mapping changes.</span></span>

2. <span data-ttu-id="4c62d-152">عطّل تعقب التغييرات لكيان **المورّدون V2**.</span><span class="sxs-lookup"><span data-stu-id="4c62d-152">Disable the change tracking for the **Vendors V2** entity.</span></span>

    1. <span data-ttu-id="4c62d-153">انتقل إلى **إدارة البيانات \> كيانات البيانات**.</span><span class="sxs-lookup"><span data-stu-id="4c62d-153">Navigate to **Data management \> Data Entities**.</span></span>
    
    2. <span data-ttu-id="4c62d-154">حدد الكيان **المورّدون V2**.</span><span class="sxs-lookup"><span data-stu-id="4c62d-154">Select the **Vendors V2** entity.</span></span>
    
    3. <span data-ttu-id="4c62d-155">انقر فوق **خيارات** من شريط القوائم، ثم فوق **تعقب التغييرات**.</span><span class="sxs-lookup"><span data-stu-id="4c62d-155">Click **Options** from the menu bar, and then **Change tracking**.</span></span>
    
        ![مرجع ذاتي أو دائري 5](media/selfref_options.png)
    
    4. <span data-ttu-id="4c62d-157">انقر فوق **تعطيل تعقب التغييرات**.</span><span class="sxs-lookup"><span data-stu-id="4c62d-157">Click **Disable Change Tracking**.</span></span>
    
        ![مرجع ذاتي أو دائري 6](media/selfref_tracking.png)

3. <span data-ttu-id="4c62d-159">قم بتشغيل المزامنة الأولية لتعيين **المورّدون V2 (msdyn_vendors)**.</span><span class="sxs-lookup"><span data-stu-id="4c62d-159">Run the initial sync of **Vendors V2 (msdyn_vendors)** mapping.</span></span> <span data-ttu-id="4c62d-160">يجب أن تنجح المزامنة الأولية بدون حدوث أي أخطاء.</span><span class="sxs-lookup"><span data-stu-id="4c62d-160">The initial sync should run successfully without any errors.</span></span>

4. <span data-ttu-id="4c62d-161">قم بتشغيل المزامنة الأولية لتعيين **جهات اتصال CDS V2 (جهات الاتصال)**.</span><span class="sxs-lookup"><span data-stu-id="4c62d-161">Run the initial sync for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="4c62d-162">يجب مزامنة هذا التعيين إذا كنت ترغب في مزامنة حقل جهة الاتصال الرئيسية أو كيان الموردين لأنه يجب إجراء مزامنة أولية لسجلات جهات الاتصال.</span><span class="sxs-lookup"><span data-stu-id="4c62d-162">You must sync this mapping if you want to sync primary contact field on vendors entity as the contacts records also need to be initial synced.</span></span>

5. <span data-ttu-id="4c62d-163">أعد إضافة الحقلين **PrimaryContactPersonId** و**InvoiceVendorAccountNumber** إلى تعيين **المورّدون V2 (msdyn_vendors)** واحفظ التعيين.</span><span class="sxs-lookup"><span data-stu-id="4c62d-163">Add the fields **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** back to the **Vendors V2 (msdyn_vendors)** mapping and save the mapping.</span></span>

6. <span data-ttu-id="4c62d-164">قم بتشغيل المزامنة الأولية من جديد لتعيين **المورّدون V2 (msdyn_vendors)**.</span><span class="sxs-lookup"><span data-stu-id="4c62d-164">Run the initial sync again for the **Vendors V2 (msdyn_vendors)** mapping.</span></span> <span data-ttu-id="4c62d-165">ستتم مزامنة كافة السجلات بسبب تعطيل تعقب التغييرات.</span><span class="sxs-lookup"><span data-stu-id="4c62d-165">All the records will be synced, because change tracking is disabled.</span></span>

7. <span data-ttu-id="4c62d-166">مكّن تعقب التغييرات لكيان **المورّدون V2**.</span><span class="sxs-lookup"><span data-stu-id="4c62d-166">Enable change tracking for the **Vendors V2** entity.</span></span>

## <a name="resolve-an-error-in-customers-v3-to-accounts-entity-mapping"></a><a id="error-customer-map"></a><span data-ttu-id="4c62d-167">حل خطأ في تعيين كيان العملاء V3 في مقابل الحسابات</span><span class="sxs-lookup"><span data-stu-id="4c62d-167">Resolve an error in Customers V3 to Accounts entity mapping</span></span>

<span data-ttu-id="4c62d-168">قد تواجه أخطاء المزامنة الأولية التالية على تعيين **العملاء V3** في مقابل **الحسابات** إذا تضمنت الكيانات سجلات موجودة لديها قيم في الحقلين **ContactPersonID** و**InvoiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="4c62d-168">You might run into the following initial sync errors on the **Customers V3** to **Accounts** mapping if the entities have existing records with values in the **ContactPersonID** and **InvoiceAccount** fields.</span></span> <span data-ttu-id="4c62d-169">يعود سبب ذلك إلى كون **InvoiceAccount** عبارة عن حقل مرجع ذاتي و**ContactPersonId** عبارة عن مرجع دائري في تعيين المورّد.</span><span class="sxs-lookup"><span data-stu-id="4c62d-169">This because **InvoiceAccount** is a self-referencing field, and **ContactPersonID** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="4c62d-170">*تعذّر حل guid للحقل: <field>. لم يتم العثور على قيمة البحث: <value>. جرّب عنوان (عناوين) URL هذا للتأكد من وجود البيانات المرجعية: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span><span class="sxs-lookup"><span data-stu-id="4c62d-170">*Couldn't resolve the guid for the field: <field>. The lookup was not found: <value>. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span></span>

- <span data-ttu-id="4c62d-171">*تعذّر حل guid للحقل: primarycontactid.msdyn_contactpersonid. لم يتم العثور على قيمة البحث: 000056. جرّب عنوان (عناوين) URL هذا للتأكد من وجود البيانات المرجعية: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span><span class="sxs-lookup"><span data-stu-id="4c62d-171">*Couldn't resolve the guid for the field: primarycontactid.msdyn_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span></span>
- <span data-ttu-id="4c62d-172">*تعذّر حل guid للحقل: msdyn_billingaccount.accountnumber. لم يتم العثور على قيمة البحث: 1206-1. جرّب عنوان (عناوين) URL هذا للتأكد من وجود البيانات المرجعية: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*</span><span class="sxs-lookup"><span data-stu-id="4c62d-172">*Couldn't resolve the guid for the field: msdyn_billingaccount.accountnumber. The lookup was not found: 1206-1. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*</span></span>

<span data-ttu-id="4c62d-173">إذا كانت لديك سجلات تتضمن قيمًا في هذه الحقول في كيان العميل، فاتبع الخطوات في القسم أدناه لإكمال المزامنة الأولية.</span><span class="sxs-lookup"><span data-stu-id="4c62d-173">If you have records with values in these fields in the customer entity follow the steps in the below section to complete initial sync successfully.</span></span> <span data-ttu-id="4c62d-174">يمكنك استخدام هذا الأسلوب لأي كيانات جاهزة مثل الحسابات وجهات الاتصال.</span><span class="sxs-lookup"><span data-stu-id="4c62d-174">You can use this approach for any out-of-the-box entities such Accounts and Contacts.</span></span>

1. <span data-ttu-id="4c62d-175">في التطبيق Finance and Operations، احذف الحقلين **ContactPersonID** و**InvoiceAccount** من التعيين **العملاء V3 (الحسابات)** واحفظ التعيين.</span><span class="sxs-lookup"><span data-stu-id="4c62d-175">In the Finance and Operations app, delete the fields **ContactPersonID** and **InvoiceAccount** from the **Customers V3 (accounts)** mapping and save the mapping.</span></span>

    1. <span data-ttu-id="4c62d-176">انتقل إلى صفحة تعيين الكتابة المزدوجة **العملاء V3 (الحسابات)**، وحدد علامة تبويب **تعيينات الكيان**. في عامل التصفية الأيسر، حدد **Finance and Operations app.Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="4c62d-176">Navigate to the dual-write mapping page for **Customers V3 (accounts)**, select the **Entity mappings** tab. In the left filter, select **Finance and Operations app.Customers V3**.</span></span> <span data-ttu-id="4c62d-177">في عامل التصفية الأيسر، حدد **Common Data Service.Account**.</span><span class="sxs-lookup"><span data-stu-id="4c62d-177">In the right filter, select **Common Data Service.Account**.</span></span>

    2. <span data-ttu-id="4c62d-178">ابحث عن **contactperson** للعثور على الحقل المصدر **ContactPersonID**.</span><span class="sxs-lookup"><span data-stu-id="4c62d-178">Search for **contactperson** to find the source field **ContactPersonID**.</span></span>
    
    3. <span data-ttu-id="4c62d-179">انقر فوق زر **الإجراءات**، وحدد **حذف**.</span><span class="sxs-lookup"><span data-stu-id="4c62d-179">Click the **Actions** button, and select **Delete**.</span></span>
    
        ![مرجع ذاتي أو دائري 3](media/cust_selfref3.png)
    
    4. <span data-ttu-id="4c62d-181">كرر الإجراء لحذف الحقل **InvoiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="4c62d-181">Repeat to delete the **InvoiceAccount** field.</span></span>
    
        ![مرجع ذاتي أو دائري](media/cust_selfref4.png)
    
    5. <span data-ttu-id="4c62d-183">احفظ تغييرات التعيين.</span><span class="sxs-lookup"><span data-stu-id="4c62d-183">Save the mapping changes.</span></span>

2. <span data-ttu-id="4c62d-184">عطّل تعقب التغييرات لكيان **العملاء V3**.</span><span class="sxs-lookup"><span data-stu-id="4c62d-184">Disable the change tracking for the **Customers V3** entity.</span></span>

    1. <span data-ttu-id="4c62d-185">انتقل إلى **إدارة البيانات \> كيانات البيانات**.</span><span class="sxs-lookup"><span data-stu-id="4c62d-185">Navigate to **Data management \> Data Entities**.</span></span>
    
    2. <span data-ttu-id="4c62d-186">حدد الكيان **العملاء V3**.</span><span class="sxs-lookup"><span data-stu-id="4c62d-186">Select the **Customers V3** entity.</span></span>
    
    3. <span data-ttu-id="4c62d-187">انقر فوق **خيارات** من شريط القوائم، ثم فوق **تعقب التغييرات**.</span><span class="sxs-lookup"><span data-stu-id="4c62d-187">Click **Options** from the menu bar, and then **Change tracking**.</span></span>
    
        ![مرجع ذاتي أو دائري 5](media/selfref_options.png)
    
    4. <span data-ttu-id="4c62d-189">انقر فوق **تعطيل تعقب التغييرات**.</span><span class="sxs-lookup"><span data-stu-id="4c62d-189">Click **Disable Change Tracking**.</span></span>
    
        ![مرجع ذاتي أو دائري 6](media/selfref_tracking.png)

3. <span data-ttu-id="4c62d-191">قم بتشغيل المزامنة الأولية لتعيين **العملاء V3 (الحسابات)**.</span><span class="sxs-lookup"><span data-stu-id="4c62d-191">Run the initial sync for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="4c62d-192">يجب أن تنجح المزامنة الأولية بدون حدوث أي أخطاء.</span><span class="sxs-lookup"><span data-stu-id="4c62d-192">The initial sync should run successfully without any errors.</span></span>

4. <span data-ttu-id="4c62d-193">قم بتشغيل المزامنة الأولية لتعيين **جهات اتصال CDS V2 (جهات الاتصال)**.</span><span class="sxs-lookup"><span data-stu-id="4c62d-193">Run the initial sync for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="4c62d-194">هناك خريطتان بالاسم نفسه.</span><span class="sxs-lookup"><span data-stu-id="4c62d-194">There are 2 maps with the same name.</span></span> <span data-ttu-id="4c62d-195">حدد الخريطة التي تتضمن الوصف **قالب كتابة مزدوجة للمزامنة بين FO.CDS المورّدون جهات الاتصال V2 وCDS.Contacts. بحاجة إلى حزمة جديدة \[Dynamics365SupplyChainExtended\].**</span><span class="sxs-lookup"><span data-stu-id="4c62d-195">Select the one with the description **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].**</span></span> <span data-ttu-id="4c62d-196">على علامة التبويب **تفاصيل** للخريطة.</span><span class="sxs-lookup"><span data-stu-id="4c62d-196">on the **Details** tab of the map.</span></span>

5. <span data-ttu-id="4c62d-197">أعد إضافة الحقلين **InvoiceAccount** و**ContactPersonId** إلى تعيين **العملاء V3 (الحسابات)** واحفظ التعيين.</span><span class="sxs-lookup"><span data-stu-id="4c62d-197">Add the fields **InvoiceAccount** and **ContactPersonId** back to the **Customers V3 (Accounts)** mapping and save the mapping.</span></span> <span data-ttu-id="4c62d-198">الحقلان **InvoiceAccount** و**ContactPersonId** هما الآن من جديد عبارة عن جزء من وضع المزامنة المباشرة.</span><span class="sxs-lookup"><span data-stu-id="4c62d-198">Now, both the **InvoiceAccount** field and the **ContactPersonId** field are again part of live sync mode.</span></span> <span data-ttu-id="4c62d-199">في الخطوة التالية، ستكمل المزامنة الأولية لهذه الحقول.</span><span class="sxs-lookup"><span data-stu-id="4c62d-199">In the next step, you complete the initial sync for these fields.</span></span>

6. <span data-ttu-id="4c62d-200">قم بتشغيل المزامنة الأولية من جديد لتعيين **العملاء V3 (الحسابات)**.</span><span class="sxs-lookup"><span data-stu-id="4c62d-200">Run the initial sync again for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="4c62d-201">بسبب تعطيل تعقب التغييرات، سيؤدي تشغيل المزامنة إلى مزامنة بيانات **InvoiceAccount** و**ContactPersonId** من التطبيق Finance and Operations إلى Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4c62d-201">Because change tracking is disabled, running the sync will sync the data for **InvoiceAccount** and **ContactPersonId** from the Finance and Operations app to Common Data Service.</span></span>

7. <span data-ttu-id="4c62d-202">لمزامنة بيانات **InvoiceAccount** و**ContactPersonId** من Common Data Service إلى Finance and Operations، تستخدم مشروع تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="4c62d-202">To sync the data for **InvoiceAccount** and **ContactPersonId** from Common Data Service to the Finance and Operations, you use a data integration project.</span></span>

    1. <span data-ttu-id="4c62d-203">في Power Apps، أنشئ مشروع تكامل البيانات بين الكيانين **Sales.Account** و**Finance and Operations apps.Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="4c62d-203">In Power Apps, create a data integration project between the **Sales.Account** and **Finance and Operations apps.Customers V3** entities.</span></span> <span data-ttu-id="4c62d-204">يجب أن يكون اتجاه البيانات من Common Data Service إلى التطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4c62d-204">The data direction must be from Common Data Service to the Finance and Operations app.</span></span>  <span data-ttu-id="4c62d-205">لأن **InvoiceAccount** عبارة عن سمة جديدة في الكتابة المزدوجة، فقد ترغب في تخطي المزامنة الأولية لهذه السمة.</span><span class="sxs-lookup"><span data-stu-id="4c62d-205">Because **InvoiceAccount** is a new attribute in dual-write, you may want to skip initial sync for this attribute.</span></span> <span data-ttu-id="4c62d-206">للحصول على مزيد من المعلومات، راجع [دمج البيانات في Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="4c62d-206">For more information, see [Integrate data into Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span></span>

        <span data-ttu-id="4c62d-207">تظهر الصورة التالية مشروعًا يقوم بتحديث **CustomerAccount** و**ContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="4c62d-207">The following image shows a project that updates **CustomerAccount** and **ContactPersonId**.</span></span>

        ![مرجع ذاتي أو دائري](media/cust_selfref6.png)

    2. <span data-ttu-id="4c62d-209">أضف معايير الشركة في عامل التصفية على جانب Common Data Service، لأنه السجلات التي تطابق معايير التصفية هي وحدها التي سيتم تحديثها في التطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4c62d-209">Add the company criteria in the filter on Common Data Service side, because only the records that match filter criteria will be updated in the Finance and Operations app.</span></span> <span data-ttu-id="4c62d-210">لإضافة عامل تصفية، انقر فوق أيقونة التصفية.</span><span class="sxs-lookup"><span data-stu-id="4c62d-210">To add a filter, click the filter icon.</span></span> <span data-ttu-id="4c62d-211">في مربع الحوار **تحرير الاستعلام**، يمكنك إضافة استعلام تصفية مثل **_msdyn_company_value eq '\<guid\>'**.</span><span class="sxs-lookup"><span data-stu-id="4c62d-211">In the **Edit query** dialog, you can add a filter query like **_msdyn_company_value eq '\<guid\>'**.</span></span> <span data-ttu-id="4c62d-212">إذا لم تكن أيقونة التصفية موجودة، فأنشئ تذكرة دعم كي تطلب من فريق تكامل البيانات تمكين إمكانية التصفية على المستأجر.</span><span class="sxs-lookup"><span data-stu-id="4c62d-212">If the filter icon is not present, create a support ticket to ask the data integration team to enable the filter capability on your tenant.</span></span> <span data-ttu-id="4c62d-213">إذا لم تقم بإدخال استعلام تصفية للقيمة **_msdyn_company_value**، فستتم مزامنة جميع السجلات.</span><span class="sxs-lookup"><span data-stu-id="4c62d-213">If you do not enter a filter query for **_msdyn_company_value**, then all the records are synced.</span></span>

        ![مرجع ذاتي أو دائري](media/cust_selfref7.png)

        <span data-ttu-id="4c62d-215">يؤدي ذلك إلى إكمال المزامنة الأولية للسجلات.</span><span class="sxs-lookup"><span data-stu-id="4c62d-215">This completes the initial sync of the records.</span></span>

8. <span data-ttu-id="4c62d-216">مكّن تعقب التغييرات لكيان **العملاء V3** في التطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4c62d-216">Enable change tracking for the **Customers V3** entity in the Finance and Operations app.</span></span>

