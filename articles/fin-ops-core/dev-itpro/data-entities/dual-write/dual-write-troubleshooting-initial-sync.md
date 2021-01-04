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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: a7ba4fa4771324b4bcb8464649bd8ce8f32024c0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683542"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="421f0-103">استكشاف المشاكل وإصلاحها أثناء المزامنة الأولية</span><span class="sxs-lookup"><span data-stu-id="421f0-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="421f0-104">يوفر هذا الموضوع معلومات حول استكشاف أخطاء تكامل الكتابة الثنائية وإصلاحها بين تطبيقات Finance and Operations وDataverse.</span><span class="sxs-lookup"><span data-stu-id="421f0-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="421f0-105">على وجه التحديد، يوفر هذا الموضوع المعلومات التي يمكن أن تساعدك في إصلاح المشكلات التي قد تحدث أثناء المزامنة الأولية.</span><span class="sxs-lookup"><span data-stu-id="421f0-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="421f0-106">قد تتطلب بعض المشكلات التي يتناولها هذا الموضوع إما دور إدارة النظام أو بيانات اعتماد مسؤول مستأجر  Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="421f0-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="421f0-107">يوضح القسم الخاص بكل مشكلة ما إذا كانت هناك حاجة إلى دور محدد أو بيانات اعتماد.</span><span class="sxs-lookup"><span data-stu-id="421f0-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="421f0-108">التحقق من أخطاء المزامنة الأولية في تطبيق Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="421f0-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="421f0-109">بعد تمكين قوالب التعيين، يجب أن تكون حالة المخططات **قيد التشغيل**.</span><span class="sxs-lookup"><span data-stu-id="421f0-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="421f0-110">إذا لم تكن الحالة **قيد التشغيل**، حدثت أخطاء أثناء المزامنة الأولية.</span><span class="sxs-lookup"><span data-stu-id="421f0-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="421f0-111">لعرض الأخطاء، حدد علامة التبويب **تفاصيل المزامنة الأولية** في صفحة **الكتابة الثنائية**.</span><span class="sxs-lookup"><span data-stu-id="421f0-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![خطأ في علامة التبويب تفاصيل المزامنة الأولية](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="421f0-113">لا يمكنك إكمال المزامنة الأولية: 400 طلب غير صحيح</span><span class="sxs-lookup"><span data-stu-id="421f0-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="421f0-114">**الدور المطلوب لإصلاح المشكلة:** مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="421f0-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="421f0-115">قد تتلقى رسالة الخطأ التالية عند محاولة تشغيل التعيين والمزامنة الأولية:</span><span class="sxs-lookup"><span data-stu-id="421f0-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="421f0-116">*(\[طلب غير صحيح\]، يقوم الخادم عن بُعد بإرجاع خطأ: (400) طلب غير صحيح.)، AX صادف التصدير خطأ*</span><span class="sxs-lookup"><span data-stu-id="421f0-116">*(\[Bad Request\], The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="421f0-117">فيما يلي مثال لرسالة الخطأ الكاملة.</span><span class="sxs-lookup"><span data-stu-id="421f0-117">Here is an example of the full error message.</span></span>

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

<span data-ttu-id="421f0-118">في حاله حدوث هذا الخطأ باستمرار، ولا يمكنك إكمال المزامنة الأولية، فاتبع هذه الخطوات لإصلاح هذه المشكلة.</span><span class="sxs-lookup"><span data-stu-id="421f0-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="421f0-119">سجل الدخول إلى الجهاز الظاهري (VM) لتطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="421f0-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="421f0-120">افتح وحدة التحكم بالإدارة لـ Microsoft.</span><span class="sxs-lookup"><span data-stu-id="421f0-120">Open Microsoft Management Console.</span></span>
3. <span data-ttu-id="421f0-121">في جزء **الخدمات**، تأكد من تشغيل خدمة إطار عمل التصدير الخاص باستيراد بيانات Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="421f0-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="421f0-122">وأعد تشغيلها إذا تم إيقافها، لأن المزامنة الأولية تتطلب ذلك.</span><span class="sxs-lookup"><span data-stu-id="421f0-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="421f0-123">خطأ المزامنة الأولية: 403 ممنوع</span><span class="sxs-lookup"><span data-stu-id="421f0-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="421f0-124">قد تتلقى رسالة الخطأ التالية أثناء المزامنة الأولية:</span><span class="sxs-lookup"><span data-stu-id="421f0-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="421f0-125">*(\[ممنوع\]، أرجع الخادم البعيد خطأ: (403) ممنوع.)، صادف تصدير AX خطأ*</span><span class="sxs-lookup"><span data-stu-id="421f0-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="421f0-126">لإصلاح المشكلة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="421f0-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="421f0-127">قم بتسجيل الدخول إلى تطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="421f0-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="421f0-128">في صفحة **تطبيقات Azure Active Directory**، احذف عميل **DtAppID**، ثم أضفه مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="421f0-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![عميل DtAppID في قائمة تطبيقات Azure AD](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a><span data-ttu-id="421f0-130">حالات فشل المراجع الذاتية أو المراجع الدائرية أثناء المزامنة الأولية</span><span class="sxs-lookup"><span data-stu-id="421f0-130">Self-reference or circular reference failures during initial synchronization</span></span>

<span data-ttu-id="421f0-131">قد تتلقى رسائل خطأ عند وجود مراجع ذاتية أو مراجع دائرية لدى أي من تعييناتك.</span><span class="sxs-lookup"><span data-stu-id="421f0-131">You might receive an error messages if any of your mappings have self-references or circular references.</span></span> <span data-ttu-id="421f0-132">تقع الأخطاء ضمن هذه الفئات:</span><span class="sxs-lookup"><span data-stu-id="421f0-132">The errors fall into these categories:</span></span>

- [<span data-ttu-id="421f0-133">خطأ في تعيين جدول الموردين V2–to–msdyn_vendors</span><span class="sxs-lookup"><span data-stu-id="421f0-133">Errors in the Vendors V2–to–msdyn_vendors table mapping</span></span>](#error-vendor-map)
- [<span data-ttu-id="421f0-134">خطأ في تعيين جدول العملاء V3–to–Accounts</span><span class="sxs-lookup"><span data-stu-id="421f0-134">Errors in the Customers V3–to–Accounts table mapping</span></span>](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-table-mapping"></a><a id="error-vendor-map"></a><span data-ttu-id="421f0-135">حل خطأ في تعيين جدول الموردين V2–to–msdyn_vendors</span><span class="sxs-lookup"><span data-stu-id="421f0-135">Resolve errors in the Vendors V2–to–msdyn_vendors table mapping</span></span>

<span data-ttu-id="421f0-136">قد تواجه أخطاء المزامنة الأولية لتعيين **الموردون V2** إلى **msdyn\_الموردون** إذا كانت الجداول تحتوي على صفوف حالية حيث توجد قيم في الحقول **PrimaryContactPersonId** و **InvoiceVendorAccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="421f0-136">You might encounter initial synchronization errors for the mapping of **Vendors V2** to **msdyn\_vendors** if the tables have existing rows where there are values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields.</span></span> <span data-ttu-id="421f0-137">تحدث هذه الأخطاء لأن **InvoiceVendorAccountNumber** عبارة عن حقل مرجع ذاتي و **PrimaryContactPersonId** عبارة عن مرجع دائري في تعيين المورّد.</span><span class="sxs-lookup"><span data-stu-id="421f0-137">These errors occur because **InvoiceVendorAccountNumber** is a self-referencing field, and **PrimaryContactPersonId** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="421f0-138">سيكون لرسائل الخطأ التي تتلقاها النموذج التالي.</span><span class="sxs-lookup"><span data-stu-id="421f0-138">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="421f0-139">*يتعذر حل guid الدليل للحقل: \<field\>. لم يتم العثور على قيمة البحث: \<value\>. جرّب عنوان (عناوين) URL هذا للتأكد من وجود البيانات المرجعية: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="421f0-139">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="421f0-140">فيما يلي بعض الأمثلة:</span><span class="sxs-lookup"><span data-stu-id="421f0-140">Here are some examples:</span></span>

- <span data-ttu-id="421f0-141">*يتعذر حل guid الدليل للحقل: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. لم يتم العثور على البحث: 000056. جرّب عنوان (عناوين) URL هذا للتأكد من وجود البيانات المرجعية: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="421f0-141">*Couldn't resolve the guid for the field: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="421f0-142">*يتعذر حل guid الدليل للحقل: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. لم يتم العثور على قيمة البحث: V24-1. جرّب عنوان (عناوين) URL هذا للتأكد من وجود البيانات المرجعية: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span><span class="sxs-lookup"><span data-stu-id="421f0-142">*Couldn't resolve the guid for the field: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. The lookup was not found: V24-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span></span>

<span data-ttu-id="421f0-143">إذا كانت أية صفوف في كيان مورد تتضمن قيمًا في الحقول **PrimaryContactPersonId** و **InvoiceVendorAccountNumber**، فاتبع هذه الخطوات لإكمال المزامنة الأولية.</span><span class="sxs-lookup"><span data-stu-id="421f0-143">If any rows in the vendor entity have values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields, follow these steps to complete the initial synchronization.</span></span>

1. <span data-ttu-id="421f0-144">في التطبيق Finance and Operations، احذف الحقلين **PrimaryContactPersonId** و **InvoiceVendorAccountNumber** من التعيين، ثم احفظ التعيين.</span><span class="sxs-lookup"><span data-stu-id="421f0-144">In the Finance and Operations app, delete the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields from the mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="421f0-145">في صفحة تعيين الكتابة المزدوجة **Vendors V2 (msdyn\_الموردون)**، في علامة التبويب **تعيينات الجدول**، في عامل التصفية الأيسر، حدد **Finance and Operations apps.Vendors V2**.</span><span class="sxs-lookup"><span data-stu-id="421f0-145">On the dual-write mapping page for **Vendors V2 (msdyn\_vendors)**, on the **Table mappings** tab, in the left filter, select **Finance and Operations apps.Vendors V2**.</span></span> <span data-ttu-id="421f0-146">في عامل التصفية الأيمن، حدد **Sales.Vendor**</span><span class="sxs-lookup"><span data-stu-id="421f0-146">In the right filter, select **Sales.Vendor**.</span></span>
    2. <span data-ttu-id="421f0-147">ابحث عن **primarycontactperson** للعثور على الحقل المصدر **PrimaryContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="421f0-147">Search for **primarycontactperson** to find the **PrimaryContactPersonId** source field.</span></span>
    3. <span data-ttu-id="421f0-148">حدد **الإجراءات**، ثم حدد **حذف**.</span><span class="sxs-lookup"><span data-stu-id="421f0-148">Select **Actions**, and then select **Delete**.</span></span>

        ![حذف الحقل PrimaryContactPersonId](media/vend_selfref3.png)

    4. <span data-ttu-id="421f0-150">كرر هذه الخطوات لحذف الحقل **InvoiceVendorAccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="421f0-150">Repeat these steps to delete the **InvoiceVendorAccountNumber** field.</span></span>

        ![حذف الحقل InvoiceVendorAccountNumber](media/vend-selfref4.png)

    5. <span data-ttu-id="421f0-152">احفظ التغييرات الخاصة بك للتعيين.</span><span class="sxs-lookup"><span data-stu-id="421f0-152">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="421f0-153">قم بإيقاف تشغيل تعقب كيان **المورّدون V2**.</span><span class="sxs-lookup"><span data-stu-id="421f0-153">Turn off change tracking for the **Vendors V2** entity.</span></span>

    1. <span data-ttu-id="421f0-154">في مساحة عمل **إدارة بيانات**، حدد تجانب **جداول البيانات**.</span><span class="sxs-lookup"><span data-stu-id="421f0-154">In the **Data management** workspace, select the **Data tables** tile.</span></span>
    2. <span data-ttu-id="421f0-155">حدد الكيان **المورّدون V2**.</span><span class="sxs-lookup"><span data-stu-id="421f0-155">Select the **Vendors V2** entity.</span></span>
    3. <span data-ttu-id="421f0-156">في جزء الإجراء، حدد **الخيارات**، ثم حدد **تعقب التغييرات**.</span><span class="sxs-lookup"><span data-stu-id="421f0-156">On the Action Pane, select **Options**, and then select **Change tracking**.</span></span>

        ![تحديد خيار تعقب التغييرات](media/selfref_options.png)

    4. <span data-ttu-id="421f0-158">حدد **تعطيل تعقب التغييرات**.</span><span class="sxs-lookup"><span data-stu-id="421f0-158">Select **Disable Change Tracking**.</span></span>

        ![تحديد تعطيل تعقب التغييرات](media/selfref_tracking.png)

3. <span data-ttu-id="421f0-160">قم بتشغيل المزامنة الأولية لتعيين **الموردون V2 (msdyn\_الموردون)**.</span><span class="sxs-lookup"><span data-stu-id="421f0-160">Run initial synchronization for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="421f0-161">يجب أن تنجح المزامنة الأولية بدون حدوث أية أخطاء.</span><span class="sxs-lookup"><span data-stu-id="421f0-161">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="421f0-162">قم بتشغيل المزامنة الأولية لتعيين **جهات اتصال CDS V2 (جهات الاتصال)**.</span><span class="sxs-lookup"><span data-stu-id="421f0-162">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="421f0-163">يجب مزامنة هذا التعيين إذا كنت ترغب في مزامنة حقل جهة الاتصال الرئيسية أو كيان الموردين، لأنه يجب إجراء مزامنة أولية لصفوف جهات الاتصال.</span><span class="sxs-lookup"><span data-stu-id="421f0-163">You must sync this mapping if you want to sync the primary contact field on the vendors entity, because initial synchronization must also be done for the contact rows.</span></span>
5. <span data-ttu-id="421f0-164">أضف الحقول **PrimaryContactPersonId** و **InvoiceVendorAccountNumber** إلى تعيين **الموردون V2 (msdyn\_vendors)**، ثم احفظ التعيين.</span><span class="sxs-lookup"><span data-stu-id="421f0-164">Add the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields back to the **Vendors V2 (msdyn\_vendors)** mapping, and then save the mapping.</span></span>
6. <span data-ttu-id="421f0-165">قم بتشغيل المزامنة الأولية مرة أخرى لتعيين **الموردون V2 (msdyn\_الموردون)**.</span><span class="sxs-lookup"><span data-stu-id="421f0-165">Run initial synchronization again for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="421f0-166">ستتم مزامنة كافة الصفوف بسبب إيقاف تشغيل تعقب التغييرات.</span><span class="sxs-lookup"><span data-stu-id="421f0-166">Because change tracking is turned off, all the rows will be synced.</span></span>
7. <span data-ttu-id="421f0-167">قم بتشغيل تعقب كيان **المورّدون V2** مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="421f0-167">Turn change tracking back on for the **Vendors V2** entity.</span></span>

## <a name="resolve-errors-in-the-customers-v3toaccounts-table-mapping"></a><a id="error-customer-map"></a><span data-ttu-id="421f0-168">حل أخطاء في تعيين جدول العملاء V3–to–Accounts</span><span class="sxs-lookup"><span data-stu-id="421f0-168">Resolve errors in the Customers V3–to–Accounts table mapping</span></span>

<span data-ttu-id="421f0-169">قد تواجه أخطاء المزامنة الأولية لتعيين **العملاء V3** إلى **الحسابات** إذا كانت الجداول تحتوي على صفوف حالية حيث توجد قيم في الحقول **ContactPersonID** و **InvoiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="421f0-169">You might encounter initial synchronization errors for the mapping of **Customers V3** to **Accounts** if the tables have existing rows where there are values in the **ContactPersonID** and **InvoiceAccount** fields.</span></span> <span data-ttu-id="421f0-170">يعود سبب حدوث هذه الأخطاء إلى كون **InvoiceAccount** عبارة عن حقل مرجع ذاتي و **ContactPersonId** عبارة عن مرجع دائري في تعيين المورّد.</span><span class="sxs-lookup"><span data-stu-id="421f0-170">These errors occur because **InvoiceAccount** is a self-referencing field, and **ContactPersonID** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="421f0-171">سيكون لرسائل الخطأ التي تتلقاها النموذج التالي.</span><span class="sxs-lookup"><span data-stu-id="421f0-171">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="421f0-172">*يتعذر حل guid الدليل للحقل: \<field\>. لم يتم العثور على قيمة البحث: \<value\>. جرّب عنوان (عناوين) URL هذا للتأكد من وجود البيانات المرجعية: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="421f0-172">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="421f0-173">فيما يلي بعض الأمثلة:</span><span class="sxs-lookup"><span data-stu-id="421f0-173">Here are some examples:</span></span>

- <span data-ttu-id="421f0-174">*يتعذر حل guid للحقل: primarycontactid.msdyn\_contactpersonid. لم يتم العثور على البحث: 000056. جرّب عنوان (عناوين) URL هذا للتأكد من وجود البيانات المرجعية: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="421f0-174">*Couldn't resolve the guid for the field: primarycontactid.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="421f0-175">*يتعذر حل guid للحقل: msdyn\_billingaccount.accountnumber. لم يتم العثور على البحث: 1206-1. جرّب عنوان (عناوين) URL هذا للتأكد من وجود البيانات المرجعية:`https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span><span class="sxs-lookup"><span data-stu-id="421f0-175">*Couldn't resolve the guid for the field: msdyn\_billingaccount.accountnumber. The lookup was not found: 1206-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span></span>

<span data-ttu-id="421f0-176">إذا كانت أية صفوف في كيان العميل تتضمن قيمًا في الحقول **ContactPersonID** و **InvoiceAccount**، فاتبع هذه الخطوات لإكمال المزامنة الأولية.</span><span class="sxs-lookup"><span data-stu-id="421f0-176">If any rows in the customer entity have values in the **ContactPersonID** and **InvoiceAccount** fields, follow these steps to complete the initial synchronization.</span></span> <span data-ttu-id="421f0-177">يمكنك استخدام هذا الأسلوب لأي جداول جاهزة مثل **الحسابات** و **جهات الاتصال**.</span><span class="sxs-lookup"><span data-stu-id="421f0-177">You can use this approach for any out-of-box tables, such **Accounts** and **Contacts**.</span></span>

1. <span data-ttu-id="421f0-178">في التطبيق Finance and Operations، احذف الحقلين **ContactPersonID** و **InvoiceAccount** من التعيين **العملاء V3 (الحسابات)** ثم احفظ التعيين.</span><span class="sxs-lookup"><span data-stu-id="421f0-178">In the Finance and Operations app, delete the **ContactPersonID** and **InvoiceAccount** fields from the **Customers V3 (accounts)** mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="421f0-179">في صفحة تعيين الكتابة المزدوجة **العملاء V3 (الحسابات)**، وفي علامة تبويب **تعيينات الجدول**، في عامل التصفية الأيسر، حدد **Finance and Operations app.Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="421f0-179">On the dual-write mapping page for **Customers V3 (accounts)**, on the **Table mappings** tab, in the left filter, select **Finance and Operations app.Customers V3**.</span></span> <span data-ttu-id="421f0-180">في عامل التصفية الأيسر، حدد **Dataverse.Account**.</span><span class="sxs-lookup"><span data-stu-id="421f0-180">In the right filter, select **Dataverse.Account**.</span></span>
    2. <span data-ttu-id="421f0-181">ابحث عن **contactperson** للعثور على الحقل المصدر **ContactPersonID**.</span><span class="sxs-lookup"><span data-stu-id="421f0-181">Search for **contactperson** to find the **ContactPersonID** source field.</span></span>
    3. <span data-ttu-id="421f0-182">حدد **الإجراءات**، ثم حدد **حذف**.</span><span class="sxs-lookup"><span data-stu-id="421f0-182">Select **Actions**, and then select **Delete**.</span></span>

        ![حذف الحقل ContactPersonID](media/cust_selfref3.png)

    4. <span data-ttu-id="421f0-184">كرر هذه الخطوات لحذف الحقل **‎InvoiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="421f0-184">Repeat these steps to delete the **InvoiceAccount** field.</span></span>

        ![حذف الحقل InvoiceAccount](media/cust_selfref4.png)

    5. <span data-ttu-id="421f0-186">احفظ التغييرات الخاصة بك للتعيين.</span><span class="sxs-lookup"><span data-stu-id="421f0-186">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="421f0-187">قم بإيقاف تشغيل تعقب كيان **العملاء V3**.</span><span class="sxs-lookup"><span data-stu-id="421f0-187">Turn off change tracking for the **Customers V3** entity.</span></span>

    1. <span data-ttu-id="421f0-188">في مساحة عمل **إدارة بيانات**، حدد تجانب **جداول البيانات**.</span><span class="sxs-lookup"><span data-stu-id="421f0-188">In the **Data management** workspace, select the **Data tables** tile.</span></span>
    2. <span data-ttu-id="421f0-189">حدد الكيان **العملاء V3**.</span><span class="sxs-lookup"><span data-stu-id="421f0-189">Select the **Customers V3** entity.</span></span>
    3. <span data-ttu-id="421f0-190">في جزء الإجراء، حدد **الخيارات**، ثم حدد **تعقب التغييرات**.</span><span class="sxs-lookup"><span data-stu-id="421f0-190">On the Action Pane, select **Options**, and then select **Change tracking**.</span></span>

        ![تحديد خيار تعقب التغييرات](media/selfref_options.png)

    4. <span data-ttu-id="421f0-192">حدد **تعطيل تعقب التغييرات**.</span><span class="sxs-lookup"><span data-stu-id="421f0-192">Select **Disable Change Tracking**.</span></span>

        ![تحديد تعطيل تعقب التغييرات](media/selfref_tracking.png)

3. <span data-ttu-id="421f0-194">قم بتشغيل المزامنة الأولية لتعيين **العملاء V3 (الحسابات)**.</span><span class="sxs-lookup"><span data-stu-id="421f0-194">Run initial synchronization for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="421f0-195">يجب أن تنجح المزامنة الأولية بدون حدوث أية أخطاء.</span><span class="sxs-lookup"><span data-stu-id="421f0-195">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="421f0-196">قم بتشغيل المزامنة الأولية لتعيين **جهات اتصال CDS V2 (جهات الاتصال)**.</span><span class="sxs-lookup"><span data-stu-id="421f0-196">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span>

    > [!NOTE]
    > <span data-ttu-id="421f0-197">هناك مخططان لهما نفس الاسم.</span><span class="sxs-lookup"><span data-stu-id="421f0-197">There are two maps that have the same name.</span></span> <span data-ttu-id="421f0-198">تأكد من تحديد المخطط الذي يتضمن الوصف التالي في علامة التبويب **تفاصيل**: **قالب كتابة مزدوجة للمزامنة بين FO.CDS المورّدون جهات الاتصال V2 وCDS.Contacts. بحاجة إلى حزمة جديدة \[Dynamics365SupplyChainExtended\].**</span><span class="sxs-lookup"><span data-stu-id="421f0-198">Be sure to select the map that has the following description on the **Details** tab: **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].**</span></span>

5. <span data-ttu-id="421f0-199">أعد إضافة الحقلين **InvoiceAccount** و **ContactPersonId** إلى تعيين **العملاء V3 (الحسابات)**، ثم احفظ التعيين.</span><span class="sxs-lookup"><span data-stu-id="421f0-199">Add the **InvoiceAccount** and **ContactPersonId** fields back to the **Customers V3 (Accounts)** mapping, and then save the mapping.</span></span> <span data-ttu-id="421f0-200">الحقلان **InvoiceAccount** و **ContactPersonId** هما الآن عبارة عن جزء من وضع المزامنة المباشرة مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="421f0-200">Both the **InvoiceAccount** field and the **ContactPersonId** field are now part of live synchronization mode again.</span></span> <span data-ttu-id="421f0-201">في الخطوة التالية، ستقوم بالمزامنة الأولية لهذه الحقول.</span><span class="sxs-lookup"><span data-stu-id="421f0-201">In the next step, you will do the initial synchronization for these fields.</span></span>
6. <span data-ttu-id="421f0-202">قم بتشغيل المزامنة الأولية مرة أخرى لتعيين **العملاء V3 (الحسابات)**.</span><span class="sxs-lookup"><span data-stu-id="421f0-202">Run initial synchronization again for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="421f0-203">بسبب إيقاف تشغيل تعقب التغييرات، سيؤدي تشغيل المزامنة إلى مزامنة بيانات **InvoiceAccount** و **ContactPersonId** من التطبيق Finance and Operations إلى Dataverse.</span><span class="sxs-lookup"><span data-stu-id="421f0-203">Because change tracking is turned off, the data for **InvoiceAccount** and **ContactPersonId** will be synced from the Finance and Operations app to Dataverse.</span></span>
7. <span data-ttu-id="421f0-204">لمزامنة بيانات **InvoiceAccount** و **ContactPersonId** من تطبيق Dataverse إلى Finance and Operations، فإنك تستخدم مشروع تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="421f0-204">To sync the data for **InvoiceAccount** and **ContactPersonId** from Dataverse to the Finance and Operations app, you must use a data integration project.</span></span>

    1. <span data-ttu-id="421f0-205">في Power Apps، أنشئ مشروع تكامل البيانات بين الجدولين **Sales.Account** و **Finance and Operations apps.Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="421f0-205">In Power Apps, create a data integration project between the **Sales.Account** and **Finance and Operations apps.Customers V3** tables.</span></span> <span data-ttu-id="421f0-206">يجب أن يكون اتجاه البيانات من Dataverse إلى التطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="421f0-206">The data direction must be from Dataverse to the Finance and Operations app.</span></span> <span data-ttu-id="421f0-207">لأن **InvoiceAccount** عبارة عن سمة جديدة في الكتابة المزدوجة، فقد ترغب في تخطي المزامنة الأولية لهذه السمة.</span><span class="sxs-lookup"><span data-stu-id="421f0-207">Because **InvoiceAccount** is a new attribute in dual-write, you might want to skip initial synchronization for it.</span></span> <span data-ttu-id="421f0-208">للحصول على مزيد من المعلومات، راجع [دمج البيانات في Dataverse](https://docs.microsoft.com/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="421f0-208">For more information, see [Integrate data into Dataverse](https://docs.microsoft.com/power-platform/admin/data-integrator).</span></span>

        <span data-ttu-id="421f0-209">يوضح الرسم التوضيحي التالي مشروعًا يقوم بتحديث **CustomerAccount** و **ContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="421f0-209">The following illustration shows a project that updates **CustomerAccount** and **ContactPersonId**.</span></span>

        ![مشروع تكامل البيانات لتحديث CustomerAccount وCustomerAccount](media/cust_selfref6.png)

    2. <span data-ttu-id="421f0-211">أضف معايير الشركة في عامل التصفية على جانب Dataverse، لذلك فإن الصفوف التي تطابق معايير التصفية هي وحدها التي سيتم تحديثها في التطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="421f0-211">Add the company criteria in the filter on the Dataverse side, so that only rows that match the filter criteria will be updated in the Finance and Operations app.</span></span> <span data-ttu-id="421f0-212">لإضافة عامل تصفية، حدد زر عامل التصفية.</span><span class="sxs-lookup"><span data-stu-id="421f0-212">To add a filter, select the filter button.</span></span> <span data-ttu-id="421f0-213">ثم في مربع الحوار **تحرير الاستعلام**، فإنه يمكنك إضافة استعلام عامل تصفية مثل **\_msdyn\_company\_value eq '\<guid\>'**.</span><span class="sxs-lookup"><span data-stu-id="421f0-213">Then, in the **Edit query** dialog box, you can add a filter query such as **\_msdyn\_company\_value eq '\<guid\>'**.</span></span> 

        > <span data-ttu-id="421f0-214">[ملاحظة] إذا لم يكن زر عامل التصفية موجودًا، فأنشئ تذكرة دعم كي تطلب من فريق تكامل البيانات تمكين إمكانية التصفية على المستأجر.</span><span class="sxs-lookup"><span data-stu-id="421f0-214">[NOTE] If the filter button isn't present, create a support ticket to ask the data integration team to enable the filter capability on your tenant.</span></span>

        <span data-ttu-id="421f0-215">إذا لم تقم بإدخال استعلام عامل تصفية للقيمة **\_msdyn\_company\_value**، فستتم مزامنة جميع الصفوف.</span><span class="sxs-lookup"><span data-stu-id="421f0-215">If you don't enter a filter query for **\_msdyn\_company\_value**, all the rows will be synced.</span></span>

        ![إضافة استعلام عامل تصفية](media/cust_selfref7.png)

    <span data-ttu-id="421f0-217">يتم الآن إكمال المزامنة الأولية للصفوف.</span><span class="sxs-lookup"><span data-stu-id="421f0-217">The initial synchronization of the rows is now completed.</span></span>

8. <span data-ttu-id="421f0-218">في التطبيق  Finance and Operations، قم بتشغيل تعقب التغييرات مرة أخرى للكيان **العملاء V3**.</span><span class="sxs-lookup"><span data-stu-id="421f0-218">In the Finance and Operations app, turn change tracking back on for the **Customers V3** entity.</span></span>
