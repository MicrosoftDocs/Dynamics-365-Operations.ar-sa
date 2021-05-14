---
title: الترقية إلى الطرف ونموذج دفتر العناوين العمومي
description: يصف هذا الموضوع كيفية ترقية بيانات الكتابة المزدوجة إلى الطرف ونموذج دفتر العناوين العمومي‬.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 32128d48bfac195530d70b60e67cfd4921fc001e
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941073"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a><span data-ttu-id="f3381-103">الترقية إلى الطرف ونموذج دفتر العناوين العمومي</span><span class="sxs-lookup"><span data-stu-id="f3381-103">Upgrade to the party and global address book model</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="f3381-104">يساعدك [قالب Azure Data Factory](https://aka.ms/dual-write-gab-adf) على ترقية بيانات جدول **حساب** و **جهة اتصال** و **مورّد** موجود في الكتابة المزدوجة إلى نموذج الطرف ودفتر العناوين العمول</span><span class="sxs-lookup"><span data-stu-id="f3381-104">The [Azure Data Factory template](https://aka.ms/dual-write-gab-adf) helps you upgrade existing **Account**, **Contact**, and **Vendor** table data in dual-write to the party and global address book model.</span></span> <span data-ttu-id="f3381-105">يقوم القالب بتسوية البيانات من تطبيقات Finance and Operations وتطبيقات مشاركة العميل.</span><span class="sxs-lookup"><span data-stu-id="f3381-105">The template reconciles the data from both Finance and Operations apps and customer engagement applications.</span></span> <span data-ttu-id="f3381-106">في نهاية العملية، سيتم إنشاء حقلي **الطرف** و **جهة الاتصال** لسجلات **الطرف** وربطها بسجلات **الحساب** و **جهة الاتصال** و **المورّد** في تطبيقات مشاركة العميل.</span><span class="sxs-lookup"><span data-stu-id="f3381-106">At the end of the process, **Party** and **Contact** fields for **Party** records will be created and associated with **Account**, **Contact**, and **Vendor** records in customer engagement applications.</span></span> <span data-ttu-id="f3381-107">يتم إنشاء ملف csv. (`FONewParty.csv`) لإنشاء سجلات **طرف** جديدة داخل تطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f3381-107">A .csv file (`FONewParty.csv`) is generated to create new **Party** records inside the Finance and Operations app.</span></span> <span data-ttu-id="f3381-108">يوفر هذا الموضوع الإرشادات الخاصة باستخدام قالب Data Factory وترقية البيانات.</span><span class="sxs-lookup"><span data-stu-id="f3381-108">This topic provides the instructions to use the Data Factory template and upgrade your data.</span></span>

<span data-ttu-id="f3381-109">إذا لم يكن لديك أي تخصيصات، فيمكنك استخدام القالب كما هو.</span><span class="sxs-lookup"><span data-stu-id="f3381-109">If you don’t have any customizations, you can use the template as-is.</span></span> <span data-ttu-id="f3381-110">إذا كانت لديك تخصيصات لسجلات **الحساب** و **جهة الاتصال** و **المورّد**، فيجب تعديل القالب باستخدام الإرشادات التالية.</span><span class="sxs-lookup"><span data-stu-id="f3381-110">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template using the following instructions.</span></span>

> [!Note]
> <span data-ttu-id="f3381-111">يساعدك القالب على ترقية بيانات **الطرف**.</span><span class="sxs-lookup"><span data-stu-id="f3381-111">The template helps to upgrade only the **Party** data.</span></span> <span data-ttu-id="f3381-112">سيتم تضمين العناوين البريدية والإلكترونية في إصدار مستقبلي.</span><span class="sxs-lookup"><span data-stu-id="f3381-112">In a future release, postal and electronic addresses will be included.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f3381-113">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="f3381-113">Prerequisites</span></span>

<span data-ttu-id="f3381-114">هذه المتطلبات الأساسية مطلوبة:</span><span class="sxs-lookup"><span data-stu-id="f3381-114">These prerequisites are required:</span></span>

+ [<span data-ttu-id="f3381-115">اشتراك Azure</span><span class="sxs-lookup"><span data-stu-id="f3381-115">Azure subscription</span></span>](https://portal.azure.com/)
+ [<span data-ttu-id="f3381-116">الوصول إلى القالب</span><span class="sxs-lookup"><span data-stu-id="f3381-116">Access to the template</span></span>](https://aka.ms/dual-write-gab-adf)
+ <span data-ttu-id="f3381-117">أنت عميل موجود للكتابة المزدوجة.</span><span class="sxs-lookup"><span data-stu-id="f3381-117">You are an existing dual-write customer.</span></span>

## <a name="prepare-for-the-upgrade"></a><span data-ttu-id="f3381-118">التحضير للترقية</span><span class="sxs-lookup"><span data-stu-id="f3381-118">Prepare for the upgrade</span></span>

+ <span data-ttu-id="f3381-119">**متزامنة بالكامل**: البيئتان في حالة متزامنة بالكامل لسجلات **الحساب (العميل)** و **جهة الاتصال** و **المورّد**.</span><span class="sxs-lookup"><span data-stu-id="f3381-119">**Fully synched**: Both environments are fully synched state for **Account (Customer)**, **Contact**, and **Vendor**.</span></span>
+ <span data-ttu-id="f3381-120">**مفاتيح التكامل**: تستخدم جداول **الحساب (العميل)** و **جهة الاتصال** و **المورّد** في تطبيقات مشاركة العميل مفاتيح التكامل المشحونة الجاهزة.</span><span class="sxs-lookup"><span data-stu-id="f3381-120">**Integration keys**: **Account (Customer)**, **Contact**, and **Vendor** tables in customer engagement apps are using the integration keys that shipped out-of-the-box.</span></span> <span data-ttu-id="f3381-121">إذا قمت بتخصيص مفاتيح التكامل، فيجب تخصيص القالب.</span><span class="sxs-lookup"><span data-stu-id="f3381-121">If you customized the integration keys, you must customize the template.</span></span>
+ <span data-ttu-id="f3381-122">**رقم الطرف**: سيكون لجميع سجلات **الحساب (العميل)** و **جهة الاتصال** و **المورّد** التي سيتم ترقيتها رقم **طرف**.</span><span class="sxs-lookup"><span data-stu-id="f3381-122">**Party number**: All **Account (Customer)**, **Contact**, and **Vendor** records that will be upgraded have a **Party** number.</span></span> <span data-ttu-id="f3381-123">سيتم تجاهل السجلات التي لا تحتوي على رقم **طرف**.</span><span class="sxs-lookup"><span data-stu-id="f3381-123">Records without a **Party** number will be ignored.</span></span> <span data-ttu-id="f3381-124">إذا كنت ترغب في ترقية تلك السجلات، فيمكنك إضافة رقم **طرف** إليها قبل بدء عملية الترقية.</span><span class="sxs-lookup"><span data-stu-id="f3381-124">If you want to upgrade those records, add a **Party** number to them before you start the upgrade process.</span></span>
+ <span data-ttu-id="f3381-125">**انقطاع العمل في النظام**: أثناء عملية الترقية، يجب عليك وضع بيئات Finance and Operations وبيئات مشاركة العميل في وضع عدم الاتصال.</span><span class="sxs-lookup"><span data-stu-id="f3381-125">**System outage**: During the upgrade process, you will have to take both the Finance and Operations and customer engagement environments offline.</span></span>
+ <span data-ttu-id="f3381-126">**لقطة**: خذ لقطات لتطبيقات Finance and Operations وتطبيقات مشاركة العميل.</span><span class="sxs-lookup"><span data-stu-id="f3381-126">**Snapshot**: Take snapshots of both the Finance and Operations and customer engagement apps.</span></span> <span data-ttu-id="f3381-127">استخدم اللقطات لاسترجاع الحالة السابقة إذا احتجت لذلك.</span><span class="sxs-lookup"><span data-stu-id="f3381-127">Use the snapshots to restore the previous state if you need to.</span></span>

## <a name="deployment"></a><span data-ttu-id="f3381-128">النشر</span><span class="sxs-lookup"><span data-stu-id="f3381-128">Deployment</span></span>

1. <span data-ttu-id="f3381-129">نزّل القالب من [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span><span class="sxs-lookup"><span data-stu-id="f3381-129">Download the template from [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span></span>

2. <span data-ttu-id="f3381-130">سجل دخولك إلى [Microsoft Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="f3381-130">Sign in to [Microsoft Azure](https://portal.azure.com/).</span></span>

3. <span data-ttu-id="f3381-131">أنشئ [مجموعة موارد](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span><span class="sxs-lookup"><span data-stu-id="f3381-131">Create a [resource group](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span></span>

4. <span data-ttu-id="f3381-132">أنشئ [حساب تخزين](/azure/storage/common/storage-account-create?tabs=azure-portal) في مجموعة الموارد التي أنشأتها.</span><span class="sxs-lookup"><span data-stu-id="f3381-132">Create a [storage account](/azure/storage/common/storage-account-create?tabs=azure-portal) in the resource group that you created.</span></span>

5. <span data-ttu-id="f3381-133">أنشئ [مصنع بيانات](/azure/data-factory/quickstart-create-data-factory-portal) في مجموعة الموارد أعلاه التي أنشأتها.</span><span class="sxs-lookup"><span data-stu-id="f3381-133">Create a [data factory](/azure/data-factory/quickstart-create-data-factory-portal) in above resource group that you created.</span></span>

6. <span data-ttu-id="f3381-134">افتح مصنع البيانات وحدد اللوحة **التأليف والمراقبة**.</span><span class="sxs-lookup"><span data-stu-id="f3381-134">Open the data factory and select the **Author & Monitor** tile.</span></span>

7. <span data-ttu-id="f3381-135">على علامة التبويب **إدارة**، حدد **قالب ARM**.</span><span class="sxs-lookup"><span data-stu-id="f3381-135">On the **Manage** tab, select **ARM template**.</span></span>

8. <span data-ttu-id="f3381-136">حدد **استيراد قالب ARM** لاستيراد قالب **الطرف‏‎**.</span><span class="sxs-lookup"><span data-stu-id="f3381-136">Select the **Import ARM template** to import the **Party** template.</span></span>

9. <span data-ttu-id="f3381-137">استورد القالب إلى مصنع البيانات.</span><span class="sxs-lookup"><span data-stu-id="f3381-137">Import the template into the data factory.</span></span> <span data-ttu-id="f3381-138">أدخل القيم التالية في **تفاصيل المشروع** و **تفاصيل المثيل**.</span><span class="sxs-lookup"><span data-stu-id="f3381-138">Enter the following values for **Project details** and **Instance details**.</span></span>

    <span data-ttu-id="f3381-139">الحقل</span><span class="sxs-lookup"><span data-stu-id="f3381-139">Field</span></span> | <span data-ttu-id="f3381-140">قيمة</span><span class="sxs-lookup"><span data-stu-id="f3381-140">Value</span></span>
    ---|---
    <span data-ttu-id="f3381-141">الاشتراك</span><span class="sxs-lookup"><span data-stu-id="f3381-141">Subscription</span></span> | <span data-ttu-id="f3381-142">اشتراك Azure</span><span class="sxs-lookup"><span data-stu-id="f3381-142">Azure subscription</span></span>
    <span data-ttu-id="f3381-143">مجموعة الموارد</span><span class="sxs-lookup"><span data-stu-id="f3381-143">Resource group</span></span> | <span data-ttu-id="f3381-144">قدم المورد نفسه الذي يتم إنشاء حساب التخزين ضمنه.</span><span class="sxs-lookup"><span data-stu-id="f3381-144">Provide same resource under which storage account is created.</span></span>
    <span data-ttu-id="f3381-145">المنطقة</span><span class="sxs-lookup"><span data-stu-id="f3381-145">Region</span></span> | <span data-ttu-id="f3381-146">حدد منطقة.</span><span class="sxs-lookup"><span data-stu-id="f3381-146">Specify region.</span></span>
    <span data-ttu-id="f3381-147">اسم المصنع</span><span class="sxs-lookup"><span data-stu-id="f3381-147">Factory Name</span></span> | <span data-ttu-id="f3381-148">حدد اسم المصنع.</span><span class="sxs-lookup"><span data-stu-id="f3381-148">Specify factory name.</span></span>
    <span data-ttu-id="f3381-149">FO Linked Service_service Principal Key</span><span class="sxs-lookup"><span data-stu-id="f3381-149">FO Linked Service_service Principal Key</span></span> | <span data-ttu-id="f3381-150">حدد مفتاح التطبيق.</span><span class="sxs-lookup"><span data-stu-id="f3381-150">Specify the application's key.</span></span>
    <span data-ttu-id="f3381-151">Azure Blob Storage_connection String</span><span class="sxs-lookup"><span data-stu-id="f3381-151">Azure Blob Storage_connection String</span></span> | <span data-ttu-id="f3381-152">سلسلة اتصال مخزن البيانات الثنائية كبيرة الحجم لـ Azure.‬</span><span class="sxs-lookup"><span data-stu-id="f3381-152">Azure Blob storage connection string.</span></span>
    <span data-ttu-id="f3381-153">Dynamics Crm Linked Service_password</span><span class="sxs-lookup"><span data-stu-id="f3381-153">Dynamics Crm Linked Service_password</span></span> | <span data-ttu-id="f3381-154">كلمة المرور الخاصة بحساب المستخدم الذي حددته كاسم المستخدم.</span><span class="sxs-lookup"><span data-stu-id="f3381-154">The password for the user account you specified as the username.</span></span>
    <span data-ttu-id="f3381-155">FO Linked Service_properties_type Properties_url</span><span class="sxs-lookup"><span data-stu-id="f3381-155">FO Linked Service_properties_type Properties_url</span></span>  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    <span data-ttu-id="f3381-156">FO Linked Service_properties_type Properties_tenant</span><span class="sxs-lookup"><span data-stu-id="f3381-156">FO Linked Service_properties_type Properties_tenant</span></span> | <span data-ttu-id="f3381-157">حدد معلومات المستأجر (اسم المجال أو معرف المستأجر) الذي يوجد تطبيقك ضمنه.</span><span class="sxs-lookup"><span data-stu-id="f3381-157">Specify the tenant information (domain name or tenant ID) under which your application resides.</span></span>
    <span data-ttu-id="f3381-158">FO Linked Service_properties_type Properties_aad Resource Id</span><span class="sxs-lookup"><span data-stu-id="f3381-158">FO Linked Service_properties_type Properties_aad Resource Id</span></span> | `https://sampledynamics.sandboxoperationsdynamics.com`
    <span data-ttu-id="f3381-159">FO Linked Service_properties_type Properties_service Principal Id</span><span class="sxs-lookup"><span data-stu-id="f3381-159">FO Linked Service_properties_type Properties_service Principal Id</span></span> | <span data-ttu-id="f3381-160">حدد معرف عميل التطبيق.</span><span class="sxs-lookup"><span data-stu-id="f3381-160">Specify the application's client ID.</span></span>
    <span data-ttu-id="f3381-161">Dynamics Crm Linked Service_properties_type Properties_username</span><span class="sxs-lookup"><span data-stu-id="f3381-161">Dynamics Crm Linked Service_properties_type Properties_username</span></span> | <span data-ttu-id="f3381-162">اسم المستخدم الذي سيتصل بـ Dynamics.</span><span class="sxs-lookup"><span data-stu-id="f3381-162">The username to connect to Dynamics.</span></span>

    <span data-ttu-id="f3381-163">لمزيد من المعلومات، راجع [ترقية قالب إدارة الموارد يدويًا لكل بيئة](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)، و[خصائص الخدمة المرتبطة](/azure/data-factory/connector-dynamics-ax#linked-service-properties)، و[نسخ البيانات باستخدام Azure Data Factory](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span><span class="sxs-lookup"><span data-stu-id="f3381-163">For more information, see [Manually promote a Resource Manager template for each environment](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Linked service properties](/azure/data-factory/connector-dynamics-ax#linked-service-properties), and [Copy data using Azure Data Factory](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span></span>

10. <span data-ttu-id="f3381-164">بعد عملية النشر، تحقق من صحة مجموعات البيانات وتدفق البيانات والخدمة المرتبطة لمصنع البيانات.</span><span class="sxs-lookup"><span data-stu-id="f3381-164">After deployment, validate the datasets, data flow, and linked service of the data factory.</span></span>

   ![مجموعات البيانات وتدفق البيانات والخدمة المرتبطة](media/data-factory-validate.png)

11. <span data-ttu-id="f3381-166">انتقل إلى **إدارة**.</span><span class="sxs-lookup"><span data-stu-id="f3381-166">Navigate to **Manage**.</span></span> <span data-ttu-id="f3381-167">ضمن **الاتصالات**، حدد **الخدمة المرتبطة**.</span><span class="sxs-lookup"><span data-stu-id="f3381-167">Under **Connections**, select **Linked Service**.</span></span> <span data-ttu-id="f3381-168">حدد **DynamicsCrmLinkedService**.</span><span class="sxs-lookup"><span data-stu-id="f3381-168">Select **DynamicsCrmLinkedService**.</span></span> <span data-ttu-id="f3381-169">في النموذج **تحرير الخدمة المرتبطة (Dynamics CRM)**، أدخل القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="f3381-169">In the **Edit linked service (Dynamics CRM)** form, enter the following values:</span></span>

    <span data-ttu-id="f3381-170">الحقل</span><span class="sxs-lookup"><span data-stu-id="f3381-170">Field</span></span> | <span data-ttu-id="f3381-171">قيمة</span><span class="sxs-lookup"><span data-stu-id="f3381-171">Value</span></span>
    ---|---
    <span data-ttu-id="f3381-172">الاسم</span><span class="sxs-lookup"><span data-stu-id="f3381-172">Name</span></span> | <span data-ttu-id="f3381-173">DynamicsCrmLinkedService</span><span class="sxs-lookup"><span data-stu-id="f3381-173">DynamicsCrmLinkedService</span></span>
    <span data-ttu-id="f3381-174">الوصف</span><span class="sxs-lookup"><span data-stu-id="f3381-174">Description</span></span> | <span data-ttu-id="f3381-175">الخدمات المرتبطة للاتصال بمثيل CRM لإحضار بيانات الوحدات</span><span class="sxs-lookup"><span data-stu-id="f3381-175">Linked services to connect with CRM instance to fetch entities data</span></span>
    <span data-ttu-id="f3381-176">الاتصال عبر وقت تشغيل التكامل</span><span class="sxs-lookup"><span data-stu-id="f3381-176">Connect via integration runtime</span></span> | <span data-ttu-id="f3381-177">AutoResolvelntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f3381-177">AutoResolvelntegrationRuntime</span></span>
    <span data-ttu-id="f3381-178">نوع النشر</span><span class="sxs-lookup"><span data-stu-id="f3381-178">Deployment type</span></span> | <span data-ttu-id="f3381-179">عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="f3381-179">Online</span></span>
    <span data-ttu-id="f3381-180">Uri الخاص بالخدمة</span><span class="sxs-lookup"><span data-stu-id="f3381-180">Service Uri</span></span> | `https://<organization-name>.crm[x].dynamics.com`
    <span data-ttu-id="f3381-181">نوع المصادقة</span><span class="sxs-lookup"><span data-stu-id="f3381-181">Authentication type</span></span> | <span data-ttu-id="f3381-182">Office365</span><span class="sxs-lookup"><span data-stu-id="f3381-182">Office365</span></span>
    <span data-ttu-id="f3381-183">اسم المستخدم</span><span class="sxs-lookup"><span data-stu-id="f3381-183">User name</span></span> |
    <span data-ttu-id="f3381-184">كلمة المرور أو Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="f3381-184">Password or Azure Key Vault</span></span> | <span data-ttu-id="f3381-185">كلمة المرور</span><span class="sxs-lookup"><span data-stu-id="f3381-185">Password</span></span>
    <span data-ttu-id="f3381-186">كلمة المرور</span><span class="sxs-lookup"><span data-stu-id="f3381-186">Password</span></span> |

## <a name="run-the-template"></a><span data-ttu-id="f3381-187">تشغيل القالب</span><span class="sxs-lookup"><span data-stu-id="f3381-187">Run the template</span></span>

1. <span data-ttu-id="f3381-188">أوقف الكتابة المزدوجة في **الحساب** و **جهة  الاتصال** و **المورّد** باستخدام تطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f3381-188">Stop the following **Account**, **Contact**, and **Vendor** dual-write using the Finance and Operations app.</span></span>

    + <span data-ttu-id="f3381-189">العملاء V3 (الحسابات)</span><span class="sxs-lookup"><span data-stu-id="f3381-189">Customers V3(accounts)</span></span>
    + <span data-ttu-id="f3381-190">العملاء V3 (جهات الاتصال)</span><span class="sxs-lookup"><span data-stu-id="f3381-190">Customers V3(contacts)</span></span>
    + <span data-ttu-id="f3381-191">جهات اتصال CDS‏ V2 (جهات الاتصال)</span><span class="sxs-lookup"><span data-stu-id="f3381-191">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="f3381-192">جهات اتصال CDS‏ V2 (جهات الاتصال)</span><span class="sxs-lookup"><span data-stu-id="f3381-192">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="f3381-193">المورّد V2 ‏(msdyn_vendor)</span><span class="sxs-lookup"><span data-stu-id="f3381-193">Vendor V2 (msdyn_vendor)</span></span>

2. <span data-ttu-id="f3381-194">تأكد من إزالة الخرائط من الجدول `msdy_dualwriteruntimeconfig` في Dataverse.</span><span class="sxs-lookup"><span data-stu-id="f3381-194">Make sure the maps are removed from the `msdy_dualwriteruntimeconfig` table in Dataverse.</span></span>

3. <span data-ttu-id="f3381-195">ثبّت [حلول الكتابة المزدوجة للطرف ودفتر العناوين العمومي](https://aka.ms/dual-write-gab) من AppSource.</span><span class="sxs-lookup"><span data-stu-id="f3381-195">Install [Dual-write Party and Global Address Book Solutions](https://aka.ms/dual-write-gab) from AppSource.</span></span>

4. <span data-ttu-id="f3381-196">في تطبيق Finance and Operations، إذا كانت الجداول التالية تحتوي على بيانات، فشغّل **المزامنة الأولية** لها.</span><span class="sxs-lookup"><span data-stu-id="f3381-196">In the Finance and Operations app, if the following tables contain data, then run **Initial Sync** for them.</span></span>

    + <span data-ttu-id="f3381-197">التحيات</span><span class="sxs-lookup"><span data-stu-id="f3381-197">Salutations</span></span>
    + <span data-ttu-id="f3381-198">أنواع الخصائص الشخصية</span><span class="sxs-lookup"><span data-stu-id="f3381-198">Personal character types</span></span>
    + <span data-ttu-id="f3381-199">الختام الإطرائي</span><span class="sxs-lookup"><span data-stu-id="f3381-199">Complimentary closing</span></span>
    + <span data-ttu-id="f3381-200">ألقاب جهات الاتصال</span><span class="sxs-lookup"><span data-stu-id="f3381-200">Contact person titles</span></span>
    + <span data-ttu-id="f3381-201">أدوار صنع القرار</span><span class="sxs-lookup"><span data-stu-id="f3381-201">Decision making roles</span></span>
    + <span data-ttu-id="f3381-202">مستويات الولاء</span><span class="sxs-lookup"><span data-stu-id="f3381-202">Loyalty levels</span></span>

5. <span data-ttu-id="f3381-203">في تطبيق مشاركة العميل، قم بتعطيل خطوات المكون الإضافي التالية.</span><span class="sxs-lookup"><span data-stu-id="f3381-203">In the customer engagement app, disable the following plugin steps.</span></span>

    + <span data-ttu-id="f3381-204">تحديث الحساب</span><span class="sxs-lookup"><span data-stu-id="f3381-204">Account Update</span></span>
         + <span data-ttu-id="f3381-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: تحديث حساب</span><span class="sxs-lookup"><span data-stu-id="f3381-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="f3381-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: تحديث حساب</span><span class="sxs-lookup"><span data-stu-id="f3381-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="f3381-207">تحديث جهة الاتصال</span><span class="sxs-lookup"><span data-stu-id="f3381-207">Contact Update</span></span>
         + <span data-ttu-id="f3381-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: تحديث جهة اتصال</span><span class="sxs-lookup"><span data-stu-id="f3381-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="f3381-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: تحديث جهة اتصال</span><span class="sxs-lookup"><span data-stu-id="f3381-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="f3381-210">msdyn_party Update</span><span class="sxs-lookup"><span data-stu-id="f3381-210">msdyn_party Update</span></span>
         + <span data-ttu-id="f3381-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: تحديث msdyn_party</span><span class="sxs-lookup"><span data-stu-id="f3381-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="f3381-212">msdyn_vendor Update</span><span class="sxs-lookup"><span data-stu-id="f3381-212">msdyn_vendor Update</span></span>
         + <span data-ttu-id="f3381-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: تحديث msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="f3381-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

6. <span data-ttu-id="f3381-214">في تطبيق مشاركة العميل، قم بتعطيل عمليات سير العمل التالية.</span><span class="sxs-lookup"><span data-stu-id="f3381-214">In the customer engagement app, disable the following workflows:</span></span>

    + <span data-ttu-id="f3381-215">إنشاء الموردين في جدول الحسابات</span><span class="sxs-lookup"><span data-stu-id="f3381-215">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="f3381-216">إنشاء الموردين في جدول الحسابات</span><span class="sxs-lookup"><span data-stu-id="f3381-216">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="f3381-217">إنشاء مورّدين من نوع الشخص في جدول جهات الاتصال</span><span class="sxs-lookup"><span data-stu-id="f3381-217">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="f3381-218">إنشاء الموردين من نوع الشخص في جدول الموردين</span><span class="sxs-lookup"><span data-stu-id="f3381-218">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="f3381-219">تحديث الموردين في جدول الحسابات</span><span class="sxs-lookup"><span data-stu-id="f3381-219">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="f3381-220">تحديث الموردين في جدول الموردين</span><span class="sxs-lookup"><span data-stu-id="f3381-220">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="f3381-221">تحديث الموردين من نوع الشخص في جدول جهات الاتصال</span><span class="sxs-lookup"><span data-stu-id="f3381-221">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="f3381-222">تحديث الموردين من نوع الشخص في جدول الموردين</span><span class="sxs-lookup"><span data-stu-id="f3381-222">Update Vendors of type Person in Vendors Table</span></span>

7. <span data-ttu-id="f3381-223">في مصنع البيانات، قم بتشغيل القالب عن طريق تحديد **تشغيل الآن** كما هو موضح في الصورة التالية.</span><span class="sxs-lookup"><span data-stu-id="f3381-223">In the data factory, run the template by selecting **Trigger now** as shown in the following image.</span></span> <span data-ttu-id="f3381-224">قد تتطلب هذه العملية بضع ساعات لتكتمل بالاستناد إلى حجم البيانات.</span><span class="sxs-lookup"><span data-stu-id="f3381-224">This process might take a few hours to complete based on the data volume.</span></span>

    ![تشغيل المشغل](media/data-factory-trigger.png)

    > [!NOTE]
    > <span data-ttu-id="f3381-226">إذا كانت لديك تخصيصات لسجلات **الحساب** و **جهة الاتصال** و **المورّد**، فيجب تعديل القالب.</span><span class="sxs-lookup"><span data-stu-id="f3381-226">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template.</span></span>

8. <span data-ttu-id="f3381-227">استورد سجلات **الطرف** الجديد في تطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f3381-227">Import the new **Party** records in the Finance and Operations app.</span></span>

    + <span data-ttu-id="f3381-228">نزّل الملف `FONewParty.csv` من مخزن البيانات الثنائية كبيرة الحجم لـ Azure.</span><span class="sxs-lookup"><span data-stu-id="f3381-228">Download the `FONewParty.csv` file from Azure blob storage.</span></span> <span data-ttu-id="f3381-229">المسار هو `partybootstrapping/output/FONewParty.csv`.</span><span class="sxs-lookup"><span data-stu-id="f3381-229">The path is `partybootstrapping/output/FONewParty.csv`.</span></span>
    + <span data-ttu-id="f3381-230">حوّل الملف `FONewParty.csv` إلى ملف Excel واستورد ملف Excel إلى تطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f3381-230">Convert the `FONewParty.csv` file into an Excel file and import the Excel file into the Finance and Operations app.</span></span>  <span data-ttu-id="f3381-231">إذا نجحت عملية استيراد csv، فيمكنك استيراد ملف csv مباشرة.</span><span class="sxs-lookup"><span data-stu-id="f3381-231">If the csv import works for you, you can import csv file directly.</span></span> <span data-ttu-id="f3381-232">قد يستغرق تشغيل عملية الاستيراد بضع ساعات، بحسب حجم البيانات.</span><span class="sxs-lookup"><span data-stu-id="f3381-232">The import could take a few hours to run, depending on the data volume.</span></span> <span data-ttu-id="f3381-233">لمزيد من المعلومات راجع [نظرة عامة حول وظائف استيراد البيانات وتصديرها](../data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="f3381-233">For more information, see [Data import and export jobs overview](../data-import-export-job.md).</span></span>

    ![استيراد سجلات طرف Datavers](media/data-factory-import-party.png)

9. <span data-ttu-id="f3381-235">في تطبيقات مشاركة العميل، قم بتمكين خطوات المكون الإضافي التالية:</span><span class="sxs-lookup"><span data-stu-id="f3381-235">In the customer engagement apps, enable the following plugin steps:</span></span>

    + <span data-ttu-id="f3381-236">تحديث الحساب</span><span class="sxs-lookup"><span data-stu-id="f3381-236">Account Update</span></span>
         + <span data-ttu-id="f3381-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: تحديث حساب</span><span class="sxs-lookup"><span data-stu-id="f3381-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="f3381-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: تحديث حساب</span><span class="sxs-lookup"><span data-stu-id="f3381-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="f3381-239">تحديث جهة الاتصال</span><span class="sxs-lookup"><span data-stu-id="f3381-239">Contact Update</span></span>
         + <span data-ttu-id="f3381-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: تحديث جهة اتصال</span><span class="sxs-lookup"><span data-stu-id="f3381-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="f3381-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: تحديث جهة اتصال</span><span class="sxs-lookup"><span data-stu-id="f3381-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="f3381-242">msdyn_party Update</span><span class="sxs-lookup"><span data-stu-id="f3381-242">msdyn_party Update</span></span>
         + <span data-ttu-id="f3381-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: تحديث msdyn_party</span><span class="sxs-lookup"><span data-stu-id="f3381-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="f3381-244">msdyn_vendor Update</span><span class="sxs-lookup"><span data-stu-id="f3381-244">msdyn_vendor Update</span></span>
         + <span data-ttu-id="f3381-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: تحديث msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="f3381-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

10. <span data-ttu-id="f3381-246">في تطبيقات مشاركة العميل، قم بتنشيط عمليات سير العمل التالية إذا قمت بإلغاء تنشيطها في الخطوات السابقة:</span><span class="sxs-lookup"><span data-stu-id="f3381-246">In the customer engagement apps, activate the following workflows if you deactivated them in previous steps:</span></span>

    + <span data-ttu-id="f3381-247">إنشاء الموردين في جدول الحسابات</span><span class="sxs-lookup"><span data-stu-id="f3381-247">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="f3381-248">إنشاء الموردين في جدول الحسابات</span><span class="sxs-lookup"><span data-stu-id="f3381-248">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="f3381-249">إنشاء مورّدين من نوع الشخص في جدول جهات الاتصال</span><span class="sxs-lookup"><span data-stu-id="f3381-249">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="f3381-250">إنشاء الموردين من نوع الشخص في جدول الموردين</span><span class="sxs-lookup"><span data-stu-id="f3381-250">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="f3381-251">تحديث الموردين في جدول الحسابات</span><span class="sxs-lookup"><span data-stu-id="f3381-251">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="f3381-252">تحديث الموردين في جدول الموردين</span><span class="sxs-lookup"><span data-stu-id="f3381-252">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="f3381-253">تحديث الموردين من نوع الشخص في جدول جهات الاتصال</span><span class="sxs-lookup"><span data-stu-id="f3381-253">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="f3381-254">تحديث الموردين من نوع الشخص في جدول الموردين</span><span class="sxs-lookup"><span data-stu-id="f3381-254">Update Vendors of type Person in Vendors Table</span></span>

11. <span data-ttu-id="f3381-255">شغّل الخرائط ذات الصلة **بالطرف** كما هو موضح في [الطرف ودفتر العناوين العمومي](party-gab.md).</span><span class="sxs-lookup"><span data-stu-id="f3381-255">Run the **Party**-related maps as instructed in [Party and global address book](party-gab.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="f3381-256">استكشاف الأخطاء وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="f3381-256">Troubleshooting</span></span>

1. <span data-ttu-id="f3381-257">في حالة فشل العملية، أعد تشغيل مصنع البيانات بدءًا من النشاط الفاشل.</span><span class="sxs-lookup"><span data-stu-id="f3381-257">In the process fails, rerun the data factory starting from the failed activity.</span></span>
2. <span data-ttu-id="f3381-258">يتم إنشاء بعض الملفات بواسطة مصنع البيانات الذي يمكنك استخدامه لغرض التحقق من صحة البيانات.</span><span class="sxs-lookup"><span data-stu-id="f3381-258">Some files are generated by the data factory that you can use for data validation purpose.</span></span>
3. <span data-ttu-id="f3381-259">يتم تشغيل مصنع البيانات استنادًا إلى ملفات csv المفصولة بفواصل.</span><span class="sxs-lookup"><span data-stu-id="f3381-259">The data factory runs based on csv files that are comma-delimited.</span></span> <span data-ttu-id="f3381-260">إذا كانت هناك قيمة حقل تتضمن فاصلة، فقد تتداخل مع النتائج.</span><span class="sxs-lookup"><span data-stu-id="f3381-260">If there is a field value that has a comma, it may interfere with the results.</span></span> <span data-ttu-id="f3381-261">تحتاج إلى إزالة الفواصل.</span><span class="sxs-lookup"><span data-stu-id="f3381-261">You need to remove the commas.</span></span>
4. <span data-ttu-id="f3381-262">توفر علامة التبويب **المراقبة** معلومات حول كافة الخطوات والبيانات التي تمت معالجتها.</span><span class="sxs-lookup"><span data-stu-id="f3381-262">The **Monitoring** tab provides information about all steps and data processed.</span></span> <span data-ttu-id="f3381-263">حدد خطوة معينة لتصحيحها.</span><span class="sxs-lookup"><span data-stu-id="f3381-263">Select a specific step to debug it.</span></span>

    ![علامة تبويب المراقبة](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a><span data-ttu-id="f3381-265">اعرف المزيد عن القالب</span><span class="sxs-lookup"><span data-stu-id="f3381-265">Learn more about the template</span></span>

<span data-ttu-id="f3381-266">يمكنك العثور علي تعليقات على القالب في ملف [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).</span><span class="sxs-lookup"><span data-stu-id="f3381-266">You can find comments for the template the [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md) file.</span></span>