---
title: الترقية إلى الطرف ونموذج دفتر العناوين العمومي
description: يصف هذا الموضوع كيفية ترقية بيانات الكتابة المزدوجة إلى الطرف ونموذج دفتر العناوين العمومي‬.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 90ddbe704ab21d62752b581a813601e8986c2103
ms.sourcegitcommit: 180548e3c10459776cf199989d3753e0c1555912
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/28/2021
ms.locfileid: "6112663"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a><span data-ttu-id="693b7-103">الترقية إلى الطرف ونموذج دفتر العناوين العمومي</span><span class="sxs-lookup"><span data-stu-id="693b7-103">Upgrade to the party and global address book model</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="693b7-104">يساعدك قالب [Microsoft Azure Data Factory](https://aka.ms/dual-write-gab-adf) على ترقية بيانات جدول **حساب** و **جهة اتصال** و **مورّد** موجود في الكتابة المزدوجة إلى نموذج الطرف ودفتر العناوين العمومي.</span><span class="sxs-lookup"><span data-stu-id="693b7-104">The [Microsoft Azure Data Factory template](https://aka.ms/dual-write-gab-adf) helps you upgrade existing **Account**, **Contact**, and **Vendor** table data in dual-write to the party and global address book model.</span></span> <span data-ttu-id="693b7-105">يقوم القالب بتسوية البيانات من تطبيقات finance and operations وتطبيقات customer engagement.</span><span class="sxs-lookup"><span data-stu-id="693b7-105">The template reconciles the data from both finance and operations apps and customer engagement applications.</span></span> <span data-ttu-id="693b7-106">في نهاية العملية، سيتم إنشاء حقلي **الطرف** و **جهة الاتصال** لسجلات **الطرف** وربطها بسجلات **الحساب** و **جهة الاتصال** و **المورّد** في تطبيقات مشاركة العميل.</span><span class="sxs-lookup"><span data-stu-id="693b7-106">At the end of the process, **Party** and **Contact** fields for **Party** records will be created and associated with **Account**, **Contact**, and **Vendor** records in customer engagement applications.</span></span> <span data-ttu-id="693b7-107">يتم إنشاء ملف .csv (`FONewParty.csv`) لإنشاء سجلات **طرف** جديدة داخل تطبيق finance and operations.</span><span class="sxs-lookup"><span data-stu-id="693b7-107">A .csv file (`FONewParty.csv`) is generated to create new **Party** records inside the finance and operations app.</span></span> <span data-ttu-id="693b7-108">يوفر هذا الموضوع الإرشادات الخاصة حول كيفية استخدام قالب Data Factory وترقية البيانات.</span><span class="sxs-lookup"><span data-stu-id="693b7-108">This topic provides instructions about how to use the Data Factory template and upgrade your data.</span></span>

<span data-ttu-id="693b7-109">إذا لم يكن لديك أي تخصيصات، فيمكنك استخدام القالب كما هو.</span><span class="sxs-lookup"><span data-stu-id="693b7-109">If you don’t have any customizations, you can use the template as is.</span></span> <span data-ttu-id="693b7-110">إذا كانت لديك تخصيصات لسجلات **الحساب** و **جهة الاتصال** و **المورّد**، فيجب تعديل القالب باستخدام الإرشادات التالية.</span><span class="sxs-lookup"><span data-stu-id="693b7-110">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template using the following instructions.</span></span>

> [!NOTE]
> <span data-ttu-id="693b7-111">يساعدك القالب على ترقية بيانات **الطرف** فقط.</span><span class="sxs-lookup"><span data-stu-id="693b7-111">The template only upgrades the **Party** data.</span></span> <span data-ttu-id="693b7-112">سيتم تضمين العناوين البريدية والإلكترونية في إصدار مستقبلي.</span><span class="sxs-lookup"><span data-stu-id="693b7-112">In a future release, postal and electronic addresses will be included.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="693b7-113">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="693b7-113">Prerequisites</span></span>

<span data-ttu-id="693b7-114">المتطلبات الأساسية التالية مطلوبة للترقية إلى الطرف ونموذج دفتر العناوين العمومي:</span><span class="sxs-lookup"><span data-stu-id="693b7-114">The following prerequisites are required to upgrade to the party and global address book model:</span></span>

+ [<span data-ttu-id="693b7-115">اشتراك Azure</span><span class="sxs-lookup"><span data-stu-id="693b7-115">Azure subscription</span></span>](https://portal.azure.com/)
+ [<span data-ttu-id="693b7-116">الوصول إلى القالب</span><span class="sxs-lookup"><span data-stu-id="693b7-116">Access to the template</span></span>](https://aka.ms/dual-write-gab-adf)
+ <span data-ttu-id="693b7-117">يجب أن تكون عميل موجود للكتابة المزدوجة.</span><span class="sxs-lookup"><span data-stu-id="693b7-117">You must be an existing dual-write customer.</span></span>

## <a name="prepare-for-the-upgrade"></a><span data-ttu-id="693b7-118">التحضير للترقية</span><span class="sxs-lookup"><span data-stu-id="693b7-118">Prepare for the upgrade</span></span>
<span data-ttu-id="693b7-119">الأنشطة التالية ضرورية للتحضير للترقية:</span><span class="sxs-lookup"><span data-stu-id="693b7-119">The following activities are needed to prepare for the upgrade:</span></span>

+ <span data-ttu-id="693b7-120">**متزامنة بالكامل**: البيئتان في حالة متزامنة بالكامل لسجلات **الحساب (العميل)** و **جهة الاتصال** و **المورّد**.</span><span class="sxs-lookup"><span data-stu-id="693b7-120">**Fully synced**: Both environments are in a fully synced state for **Account (Customer)**, **Contact**, and **Vendor**.</span></span>
+ <span data-ttu-id="693b7-121">**مفاتيح التكامل**: تستخدم جداول **الحساب (العميل)** و **جهة الاتصال** و **المورّد** في تطبيقات مشاركة العميل مفاتيح التكامل المشحونة الجاهزة.</span><span class="sxs-lookup"><span data-stu-id="693b7-121">**Integration keys**: **Account (Customer)**, **Contact**, and **Vendor** tables in customer engagement apps are using the integration keys that shipped out-of-the-box.</span></span> <span data-ttu-id="693b7-122">إذا قمت بتخصيص مفاتيح التكامل، فيجب تخصيص القالب.</span><span class="sxs-lookup"><span data-stu-id="693b7-122">If you customized the integration keys, you must customize the template.</span></span>
+ <span data-ttu-id="693b7-123">**رقم الطرف**: سيكون لجميع سجلات **الحساب (العميل)** و **جهة الاتصال** و **المورّد** التي سيتم ترقيتها رقم **طرف**.</span><span class="sxs-lookup"><span data-stu-id="693b7-123">**Party number**: All **Account (Customer)**, **Contact**, and **Vendor** records that will be upgraded have a **Party** number.</span></span> <span data-ttu-id="693b7-124">سيتم تجاهل السجلات التي لا تحتوي على رقم **طرف**.</span><span class="sxs-lookup"><span data-stu-id="693b7-124">Records without a **Party** number will be ignored.</span></span> <span data-ttu-id="693b7-125">إذا كنت ترغب في ترقية تلك السجلات، فيمكنك إضافة رقم **طرف** إليها قبل بدء عملية الترقية.</span><span class="sxs-lookup"><span data-stu-id="693b7-125">If you want to upgrade those records, add a **Party** number to them before you start the upgrade process.</span></span>
+ <span data-ttu-id="693b7-126">**انقطاع العمل في النظام**: أثناء عملية الترقية، يجب عليك وضع بيئات finance and operations وبيئات مشاركة العميل في وضع عدم الاتصال.</span><span class="sxs-lookup"><span data-stu-id="693b7-126">**System outage**: During the upgrade process, you will have to take both the finance and operations and customer engagement environments offline.</span></span>
+ <span data-ttu-id="693b7-127">**لقطة**: خذ لقطات لتطبيقات finance and operations وتطبيقات customer engagement.</span><span class="sxs-lookup"><span data-stu-id="693b7-127">**Snapshot**: Take snapshots of both the finance and operations apps and customer engagement apps.</span></span> <span data-ttu-id="693b7-128">استخدم اللقطات لاسترجاع الحالة السابقة إذا احتجت لذلك.</span><span class="sxs-lookup"><span data-stu-id="693b7-128">Use the snapshots to restore the previous state if you need to.</span></span>

## <a name="deployment"></a><span data-ttu-id="693b7-129">النشر</span><span class="sxs-lookup"><span data-stu-id="693b7-129">Deployment</span></span>

1. <span data-ttu-id="693b7-130">نزّل القالب من [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span><span class="sxs-lookup"><span data-stu-id="693b7-130">Download the template from [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span></span>

2. <span data-ttu-id="693b7-131">سجل دخولك إلى [Microsoft Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="693b7-131">Sign in to [Microsoft Azure](https://portal.azure.com/).</span></span>

3. <span data-ttu-id="693b7-132">أنشئ [مجموعة موارد](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span><span class="sxs-lookup"><span data-stu-id="693b7-132">Create a [resource group](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span></span>

4. <span data-ttu-id="693b7-133">أنشئ [حساب تخزين](/azure/storage/common/storage-account-create?tabs=azure-portal) في مجموعة الموارد التي أنشأتها.</span><span class="sxs-lookup"><span data-stu-id="693b7-133">Create a [storage account](/azure/storage/common/storage-account-create?tabs=azure-portal) in the resource group that you created.</span></span>

5. <span data-ttu-id="693b7-134">أنشئ [مصنع بيانات](/azure/data-factory/quickstart-create-data-factory-portal) في مجموعة الموارد أعلاه التي أنشأتها.</span><span class="sxs-lookup"><span data-stu-id="693b7-134">Create a [data factory](/azure/data-factory/quickstart-create-data-factory-portal) in above resource group that you created.</span></span>

6. <span data-ttu-id="693b7-135">افتح مصنع البيانات وحدد اللوحة **التأليف والمراقبة**.</span><span class="sxs-lookup"><span data-stu-id="693b7-135">Open the data factory and select the **Author & Monitor** tile.</span></span>

7. <span data-ttu-id="693b7-136">على علامة التبويب **إدارة**، حدد **قالب ARM**.</span><span class="sxs-lookup"><span data-stu-id="693b7-136">On the **Manage** tab, select **ARM template**.</span></span>

8. <span data-ttu-id="693b7-137">حدد **استيراد قالب ARM** لاستيراد قالب **الطرف‏‎**.</span><span class="sxs-lookup"><span data-stu-id="693b7-137">Select the **Import ARM template** to import the **Party** template.</span></span>

9. <span data-ttu-id="693b7-138">استورد القالب إلى مصنع البيانات.</span><span class="sxs-lookup"><span data-stu-id="693b7-138">Import the template into the data factory.</span></span> <span data-ttu-id="693b7-139">أدخل القيم التالية في **تفاصيل المشروع** و **تفاصيل المثيل**.</span><span class="sxs-lookup"><span data-stu-id="693b7-139">Enter the following values for **Project details** and **Instance details**.</span></span>

    <span data-ttu-id="693b7-140">الحقل</span><span class="sxs-lookup"><span data-stu-id="693b7-140">Field</span></span> | <span data-ttu-id="693b7-141">قيمة</span><span class="sxs-lookup"><span data-stu-id="693b7-141">Value</span></span>
    ---|---
    <span data-ttu-id="693b7-142">الاشتراك</span><span class="sxs-lookup"><span data-stu-id="693b7-142">Subscription</span></span> | <span data-ttu-id="693b7-143">اشتراك Azure</span><span class="sxs-lookup"><span data-stu-id="693b7-143">Azure subscription</span></span>
    <span data-ttu-id="693b7-144">مجموعة الموارد</span><span class="sxs-lookup"><span data-stu-id="693b7-144">Resource group</span></span> | <span data-ttu-id="693b7-145">قدم المورد نفسه الذي يتم إنشاء حساب التخزين ضمنه.</span><span class="sxs-lookup"><span data-stu-id="693b7-145">Provide same resource under which storage account is created.</span></span>
    <span data-ttu-id="693b7-146">المنطقة</span><span class="sxs-lookup"><span data-stu-id="693b7-146">Region</span></span> | <span data-ttu-id="693b7-147">حدد منطقة.</span><span class="sxs-lookup"><span data-stu-id="693b7-147">Specify region.</span></span>
    <span data-ttu-id="693b7-148">اسم المصنع</span><span class="sxs-lookup"><span data-stu-id="693b7-148">Factory Name</span></span> | <span data-ttu-id="693b7-149">حدد اسم المصنع.</span><span class="sxs-lookup"><span data-stu-id="693b7-149">Specify factory name.</span></span>
    <span data-ttu-id="693b7-150">FO Linked Service_service Principal Key</span><span class="sxs-lookup"><span data-stu-id="693b7-150">FO Linked Service_service Principal Key</span></span> | <span data-ttu-id="693b7-151">حدد مفتاح التطبيق.</span><span class="sxs-lookup"><span data-stu-id="693b7-151">Specify the application's key.</span></span>
    <span data-ttu-id="693b7-152">Azure Blob Storage_connection String</span><span class="sxs-lookup"><span data-stu-id="693b7-152">Azure Blob Storage_connection String</span></span> | <span data-ttu-id="693b7-153">سلسلة اتصال مخزن البيانات الثنائية كبيرة الحجم لـ Azure.‬</span><span class="sxs-lookup"><span data-stu-id="693b7-153">Azure Blob storage connection string.</span></span>
    <span data-ttu-id="693b7-154">Dynamics Crm Linked Service_password</span><span class="sxs-lookup"><span data-stu-id="693b7-154">Dynamics Crm Linked Service_password</span></span> | <span data-ttu-id="693b7-155">كلمة المرور الخاصة بحساب المستخدم الذي حددته كاسم المستخدم.</span><span class="sxs-lookup"><span data-stu-id="693b7-155">The password for the user account you specified as the username.</span></span>
    <span data-ttu-id="693b7-156">FO Linked Service_properties_type Properties_url</span><span class="sxs-lookup"><span data-stu-id="693b7-156">FO Linked Service_properties_type Properties_url</span></span>  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    <span data-ttu-id="693b7-157">FO Linked Service_properties_type Properties_tenant</span><span class="sxs-lookup"><span data-stu-id="693b7-157">FO Linked Service_properties_type Properties_tenant</span></span> | <span data-ttu-id="693b7-158">حدد معلومات المستأجر (اسم المجال أو معرف المستأجر) الذي يوجد تطبيقك ضمنه.</span><span class="sxs-lookup"><span data-stu-id="693b7-158">Specify the tenant information (domain name or tenant ID) under which your application resides.</span></span>
    <span data-ttu-id="693b7-159">FO Linked Service_properties_type Properties_aad Resource Id</span><span class="sxs-lookup"><span data-stu-id="693b7-159">FO Linked Service_properties_type Properties_aad Resource Id</span></span> | `https://sampledynamics.sandboxoperationsdynamics.com`
    <span data-ttu-id="693b7-160">FO Linked Service_properties_type Properties_service Principal Id</span><span class="sxs-lookup"><span data-stu-id="693b7-160">FO Linked Service_properties_type Properties_service Principal Id</span></span> | <span data-ttu-id="693b7-161">حدد معرف عميل التطبيق.</span><span class="sxs-lookup"><span data-stu-id="693b7-161">Specify the application's client ID.</span></span>
    <span data-ttu-id="693b7-162">Dynamics Crm Linked Service_properties_type Properties_username</span><span class="sxs-lookup"><span data-stu-id="693b7-162">Dynamics Crm Linked Service_properties_type Properties_username</span></span> | <span data-ttu-id="693b7-163">اسم المستخدم الذي سيتصل بـ Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="693b7-163">The username to connect to Dynamics 365.</span></span>

    <span data-ttu-id="693b7-164">للحصول على معلومات إضافية، ارجع إلى المواضيع التالية:</span><span class="sxs-lookup"><span data-stu-id="693b7-164">For additional information, refer to the following topics:</span></span> 
    
    - [<span data-ttu-id="693b7-165">ترقية قالب Resource Manager يدويًا لكل بيئة</span><span class="sxs-lookup"><span data-stu-id="693b7-165">Manually promote a Resource Manager template for each environment</span></span>](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [<span data-ttu-id="693b7-166">خصائص الخدمة المرتبطة</span><span class="sxs-lookup"><span data-stu-id="693b7-166">Linked service properties</span></span>](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [<span data-ttu-id="693b7-167">نسخ البيانات باستخدام Azure Data Factory</span><span class="sxs-lookup"><span data-stu-id="693b7-167">Copy data using Azure Data Factory</span></span>](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. <span data-ttu-id="693b7-168">بعد عملية النشر، تحقق من صحة مجموعات البيانات وتدفق البيانات والخدمة المرتبطة لمصنع البيانات.</span><span class="sxs-lookup"><span data-stu-id="693b7-168">After deployment, validate the datasets, data flow, and linked service of the data factory.</span></span>

   ![مجموعات البيانات وتدفق البيانات والخدمة المرتبطة](media/data-factory-validate.png)

11. <span data-ttu-id="693b7-170">انتقل إلى **إدارة**.</span><span class="sxs-lookup"><span data-stu-id="693b7-170">Navigate to **Manage**.</span></span> <span data-ttu-id="693b7-171">ضمن **الاتصالات**، حدد **الخدمة المرتبطة**.</span><span class="sxs-lookup"><span data-stu-id="693b7-171">Under **Connections**, select **Linked Service**.</span></span> <span data-ttu-id="693b7-172">حدد **DynamicsCrmLinkedService**.</span><span class="sxs-lookup"><span data-stu-id="693b7-172">Select **DynamicsCrmLinkedService**.</span></span> <span data-ttu-id="693b7-173">في النموذج **تحرير الخدمة المرتبطة (Dynamics CRM)**، أدخل القيم التالية.</span><span class="sxs-lookup"><span data-stu-id="693b7-173">In the **Edit linked service (Dynamics CRM)** form, enter the following values.</span></span>

    <span data-ttu-id="693b7-174">الحقل</span><span class="sxs-lookup"><span data-stu-id="693b7-174">Field</span></span> | <span data-ttu-id="693b7-175">قيمة</span><span class="sxs-lookup"><span data-stu-id="693b7-175">Value</span></span>
    ---|---
    <span data-ttu-id="693b7-176">الاسم</span><span class="sxs-lookup"><span data-stu-id="693b7-176">Name</span></span> | <span data-ttu-id="693b7-177">DynamicsCrmLinkedService</span><span class="sxs-lookup"><span data-stu-id="693b7-177">DynamicsCrmLinkedService</span></span>
    <span data-ttu-id="693b7-178">الوصف</span><span class="sxs-lookup"><span data-stu-id="693b7-178">Description</span></span> | <span data-ttu-id="693b7-179">الخدمات المرتبطة للاتصال بمثيل CRM لإحضار بيانات الوحدات</span><span class="sxs-lookup"><span data-stu-id="693b7-179">Linked services to connect with CRM instance to fetch entities data</span></span>
    <span data-ttu-id="693b7-180">الاتصال عبر وقت تشغيل التكامل</span><span class="sxs-lookup"><span data-stu-id="693b7-180">Connect via integration runtime</span></span> | <span data-ttu-id="693b7-181">AutoResolvelntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="693b7-181">AutoResolvelntegrationRuntime</span></span>
    <span data-ttu-id="693b7-182">نوع النشر</span><span class="sxs-lookup"><span data-stu-id="693b7-182">Deployment type</span></span> | <span data-ttu-id="693b7-183">عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="693b7-183">Online</span></span>
    <span data-ttu-id="693b7-184">Uri الخاص بالخدمة</span><span class="sxs-lookup"><span data-stu-id="693b7-184">Service Uri</span></span> | `https://<organization-name>.crm[x].dynamics.com`
    <span data-ttu-id="693b7-185">نوع المصادقة</span><span class="sxs-lookup"><span data-stu-id="693b7-185">Authentication type</span></span> | <span data-ttu-id="693b7-186">Office365</span><span class="sxs-lookup"><span data-stu-id="693b7-186">Office365</span></span>
    <span data-ttu-id="693b7-187">اسم المستخدم</span><span class="sxs-lookup"><span data-stu-id="693b7-187">User name</span></span> |
    <span data-ttu-id="693b7-188">كلمة المرور أو Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="693b7-188">Password or Azure Key Vault</span></span> | <span data-ttu-id="693b7-189">كلمة المرور</span><span class="sxs-lookup"><span data-stu-id="693b7-189">Password</span></span>
    <span data-ttu-id="693b7-190">كلمة المرور</span><span class="sxs-lookup"><span data-stu-id="693b7-190">Password</span></span> |

## <a name="run-the-template"></a><span data-ttu-id="693b7-191">تشغيل القالب</span><span class="sxs-lookup"><span data-stu-id="693b7-191">Run the template</span></span>

1. <span data-ttu-id="693b7-192">أوقف الخرائط ثنائية الكتابة في **الحساب** و **جهة الاتصال** و **المورّد** باستخدام تطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="693b7-192">Stop the following **Account**, **Contact**, and **Vendor** dual-write maps using the Finance and Operations app.</span></span>

    + <span data-ttu-id="693b7-193">العملاء V3 (الحسابات)</span><span class="sxs-lookup"><span data-stu-id="693b7-193">Customers V3(accounts)</span></span>
    + <span data-ttu-id="693b7-194">العملاء V3 (جهات الاتصال)</span><span class="sxs-lookup"><span data-stu-id="693b7-194">Customers V3(contacts)</span></span>
    + <span data-ttu-id="693b7-195">جهات اتصال CDS‏ V2 (جهات الاتصال)</span><span class="sxs-lookup"><span data-stu-id="693b7-195">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="693b7-196">جهات اتصال CDS‏ V2 (جهات الاتصال)</span><span class="sxs-lookup"><span data-stu-id="693b7-196">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="693b7-197">المورّد V2 ‏(msdyn_vendor)</span><span class="sxs-lookup"><span data-stu-id="693b7-197">Vendor V2 (msdyn_vendor)</span></span>

2. <span data-ttu-id="693b7-198">تأكد من إزالة الخرائط من الجدول `msdy_dualwriteruntimeconfig` في Dataverse.</span><span class="sxs-lookup"><span data-stu-id="693b7-198">Make sure the maps are removed from the `msdy_dualwriteruntimeconfig` table in Dataverse.</span></span>

3. <span data-ttu-id="693b7-199">ثبّت [حلول الكتابة المزدوجة للطرف ودفتر العناوين العمومي](https://aka.ms/dual-write-gab) من AppSource.</span><span class="sxs-lookup"><span data-stu-id="693b7-199">Install [Dual-write Party and Global Address Book Solutions](https://aka.ms/dual-write-gab) from AppSource.</span></span>

4. <span data-ttu-id="693b7-200">في تطبيق the finance and operations، إذا كانت الجداول التالية تحتوي على بيانات، فشغّل **المزامنة الأولية** لها.</span><span class="sxs-lookup"><span data-stu-id="693b7-200">In the finance and operations app, if the following tables contain data, then run **Initial Sync** for them.</span></span>

    + <span data-ttu-id="693b7-201">التحيات</span><span class="sxs-lookup"><span data-stu-id="693b7-201">Salutations</span></span>
    + <span data-ttu-id="693b7-202">أنواع الخصائص الشخصية</span><span class="sxs-lookup"><span data-stu-id="693b7-202">Personal character types</span></span>
    + <span data-ttu-id="693b7-203">الختام الإطرائي</span><span class="sxs-lookup"><span data-stu-id="693b7-203">Complimentary closing</span></span>
    + <span data-ttu-id="693b7-204">ألقاب جهات الاتصال</span><span class="sxs-lookup"><span data-stu-id="693b7-204">Contact person titles</span></span>
    + <span data-ttu-id="693b7-205">أدوار صنع القرار</span><span class="sxs-lookup"><span data-stu-id="693b7-205">Decision making roles</span></span>
    + <span data-ttu-id="693b7-206">مستويات الولاء</span><span class="sxs-lookup"><span data-stu-id="693b7-206">Loyalty levels</span></span>

5. <span data-ttu-id="693b7-207">في تطبيق customer engagement، قم بتعطيل خطوات المكون الإضافي التالية.</span><span class="sxs-lookup"><span data-stu-id="693b7-207">In the customer engagement app, disable the following plug-in steps.</span></span>

    + <span data-ttu-id="693b7-208">تحديث الحساب</span><span class="sxs-lookup"><span data-stu-id="693b7-208">Account Update</span></span>
         + <span data-ttu-id="693b7-209">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: تحديث حساب</span><span class="sxs-lookup"><span data-stu-id="693b7-209">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="693b7-210">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: تحديث حساب</span><span class="sxs-lookup"><span data-stu-id="693b7-210">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="693b7-211">تحديث جهة الاتصال</span><span class="sxs-lookup"><span data-stu-id="693b7-211">Contact Update</span></span>
         + <span data-ttu-id="693b7-212">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: تحديث جهة اتصال</span><span class="sxs-lookup"><span data-stu-id="693b7-212">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="693b7-213">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: تحديث جهة اتصال</span><span class="sxs-lookup"><span data-stu-id="693b7-213">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="693b7-214">msdyn_party Update</span><span class="sxs-lookup"><span data-stu-id="693b7-214">msdyn_party Update</span></span>
         + <span data-ttu-id="693b7-215">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: تحديث msdyn_party</span><span class="sxs-lookup"><span data-stu-id="693b7-215">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="693b7-216">msdyn_vendor Update</span><span class="sxs-lookup"><span data-stu-id="693b7-216">msdyn_vendor Update</span></span>
         + <span data-ttu-id="693b7-217">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: تحديث msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="693b7-217">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

6. <span data-ttu-id="693b7-218">في تطبيق مشاركة العميل، قم بتعطيل عمليات سير العمل التالية.</span><span class="sxs-lookup"><span data-stu-id="693b7-218">In the customer engagement app, disable the following workflows:</span></span>

    + <span data-ttu-id="693b7-219">إنشاء الموردين في جدول الحسابات</span><span class="sxs-lookup"><span data-stu-id="693b7-219">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="693b7-220">إنشاء الموردين في جدول الحسابات</span><span class="sxs-lookup"><span data-stu-id="693b7-220">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="693b7-221">إنشاء مورّدين من نوع الشخص في جدول جهات الاتصال</span><span class="sxs-lookup"><span data-stu-id="693b7-221">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="693b7-222">إنشاء الموردين من نوع الشخص في جدول الموردين</span><span class="sxs-lookup"><span data-stu-id="693b7-222">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="693b7-223">تحديث الموردين في جدول الحسابات</span><span class="sxs-lookup"><span data-stu-id="693b7-223">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="693b7-224">تحديث الموردين في جدول الموردين</span><span class="sxs-lookup"><span data-stu-id="693b7-224">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="693b7-225">تحديث الموردين من نوع الشخص في جدول جهات الاتصال</span><span class="sxs-lookup"><span data-stu-id="693b7-225">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="693b7-226">تحديث الموردين من نوع الشخص في جدول الموردين</span><span class="sxs-lookup"><span data-stu-id="693b7-226">Update Vendors of type Person in Vendors Table</span></span>

7. <span data-ttu-id="693b7-227">في مصنع البيانات، قم بتشغيل القالب عن طريق تحديد **تشغيل الآن** كما هو موضح في الصورة التالية.</span><span class="sxs-lookup"><span data-stu-id="693b7-227">In the data factory, run the template by selecting **Trigger now** as shown in the following image.</span></span> <span data-ttu-id="693b7-228">قد تتطلب هذه العملية بضع ساعات لتكتمل بالاستناد إلى حجم البيانات.</span><span class="sxs-lookup"><span data-stu-id="693b7-228">This process might take a few hours to complete based on the data volume.</span></span>

    ![تشغيل المشغل](media/data-factory-trigger.png)

    > [!NOTE]
    > <span data-ttu-id="693b7-230">إذا كانت لديك تخصيصات **الحساب** و **جهة الاتصال** و **المورّد**، فيجب تعديل القالب.</span><span class="sxs-lookup"><span data-stu-id="693b7-230">If you have customizations for **Account**, **Contact**, and **Vendor**, then you need to modify the template.</span></span>

8. <span data-ttu-id="693b7-231">استورد سجلات **الطرف** الجديد في تطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="693b7-231">Import the new **Party** records in the Finance and Operations app.</span></span>

    + <span data-ttu-id="693b7-232">نزّل الملف `FONewParty.csv` من مخزن البيانات الثنائية كبيرة الحجم لـ Azure.</span><span class="sxs-lookup"><span data-stu-id="693b7-232">Download the `FONewParty.csv` file from Azure blob storage.</span></span> <span data-ttu-id="693b7-233">المسار هو `partybootstrapping/output/FONewParty.csv`.</span><span class="sxs-lookup"><span data-stu-id="693b7-233">The path is `partybootstrapping/output/FONewParty.csv`.</span></span>
    + <span data-ttu-id="693b7-234">حول الملف `FONewParty.csv` إلى ملف Excel وقم باستيراد ملف Excel إلى تطبيق finance and operations.</span><span class="sxs-lookup"><span data-stu-id="693b7-234">Convert the `FONewParty.csv` file into an Excel file and import the Excel file into the finance and operations app.</span></span> <span data-ttu-id="693b7-235">إذا نجحت عملية استيراد csv، فيمكنك استيراد ملف csv مباشرة.</span><span class="sxs-lookup"><span data-stu-id="693b7-235">If the csv import works for you, you can import the csv file directly.</span></span> <span data-ttu-id="693b7-236">قد يستغرق تشغيل عملية الاستيراد بضع ساعات، بحسب حجم البيانات.</span><span class="sxs-lookup"><span data-stu-id="693b7-236">The import could take a few hours to run, depending on the data volume.</span></span> <span data-ttu-id="693b7-237">لمزيد من المعلومات راجع [نظرة عامة حول وظائف استيراد البيانات وتصديرها](../data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="693b7-237">For more information, see [Data import and export jobs overview](../data-import-export-job.md).</span></span>

    ![استيراد سجلات طرف Datavers](media/data-factory-import-party.png)

9. <span data-ttu-id="693b7-239">في تطبيقات customer engagement، قم بتمكين خطوات المكون الإضافي التالية:</span><span class="sxs-lookup"><span data-stu-id="693b7-239">In the customer engagement apps, enable the following plug-in steps:</span></span>

    + <span data-ttu-id="693b7-240">تحديث الحساب</span><span class="sxs-lookup"><span data-stu-id="693b7-240">Account Update</span></span>
         + <span data-ttu-id="693b7-241">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: تحديث حساب</span><span class="sxs-lookup"><span data-stu-id="693b7-241">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="693b7-242">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: تحديث حساب</span><span class="sxs-lookup"><span data-stu-id="693b7-242">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="693b7-243">تحديث جهة الاتصال</span><span class="sxs-lookup"><span data-stu-id="693b7-243">Contact Update</span></span>
         + <span data-ttu-id="693b7-244">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: تحديث جهة اتصال</span><span class="sxs-lookup"><span data-stu-id="693b7-244">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="693b7-245">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: تحديث جهة اتصال</span><span class="sxs-lookup"><span data-stu-id="693b7-245">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="693b7-246">msdyn_party Update</span><span class="sxs-lookup"><span data-stu-id="693b7-246">msdyn_party Update</span></span>
         + <span data-ttu-id="693b7-247">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: تحديث msdyn_party</span><span class="sxs-lookup"><span data-stu-id="693b7-247">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="693b7-248">msdyn_vendor Update</span><span class="sxs-lookup"><span data-stu-id="693b7-248">msdyn_vendor Update</span></span>
         + <span data-ttu-id="693b7-249">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: تحديث msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="693b7-249">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

10. <span data-ttu-id="693b7-250">في تطبيقات مشاركة العميل، قم بتنشيط عمليات سير العمل التالية إذا قمت بإلغاء تنشيطها في الخطوات السابقة:</span><span class="sxs-lookup"><span data-stu-id="693b7-250">In the customer engagement apps, activate the following workflows if you deactivated them in previous steps:</span></span>

    + <span data-ttu-id="693b7-251">إنشاء الموردين في جدول الحسابات</span><span class="sxs-lookup"><span data-stu-id="693b7-251">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="693b7-252">إنشاء الموردين في جدول الحسابات</span><span class="sxs-lookup"><span data-stu-id="693b7-252">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="693b7-253">إنشاء مورّدين من نوع الشخص في جدول جهات الاتصال</span><span class="sxs-lookup"><span data-stu-id="693b7-253">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="693b7-254">إنشاء الموردين من نوع الشخص في جدول الموردين</span><span class="sxs-lookup"><span data-stu-id="693b7-254">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="693b7-255">تحديث الموردين في جدول الحسابات</span><span class="sxs-lookup"><span data-stu-id="693b7-255">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="693b7-256">تحديث الموردين في جدول الموردين</span><span class="sxs-lookup"><span data-stu-id="693b7-256">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="693b7-257">تحديث الموردين من نوع الشخص في جدول جهات الاتصال</span><span class="sxs-lookup"><span data-stu-id="693b7-257">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="693b7-258">تحديث الموردين من نوع الشخص في جدول الموردين</span><span class="sxs-lookup"><span data-stu-id="693b7-258">Update Vendors of type Person in Vendors Table</span></span>

11. <span data-ttu-id="693b7-259">شغّل الخرائط ذات الصلة **بالطرف** كما هو موضح في [الطرف ودفتر العناوين العمومي](party-gab.md).</span><span class="sxs-lookup"><span data-stu-id="693b7-259">Run the **Party**-related maps as instructed in [Party and global address book](party-gab.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="693b7-260">استكشاف الأخطاء وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="693b7-260">Troubleshooting</span></span>

1. <span data-ttu-id="693b7-261">في حالة فشل العملية، أعد تشغيل مصنع البيانات بدءًا من النشاط الفاشل.</span><span class="sxs-lookup"><span data-stu-id="693b7-261">If the process fails, rerun the data factory starting from the failed activity.</span></span>
2. <span data-ttu-id="693b7-262">يتم إنشاء بعض الملفات بواسطة مصنع البيانات الذي يمكنك استخدامه لغرض التحقق من صحة البيانات.</span><span class="sxs-lookup"><span data-stu-id="693b7-262">Some files are generated by the data factory that you can use for data validation purpose.</span></span>
3. <span data-ttu-id="693b7-263">يتم تشغيل مصنع البيانات استنادًا إلى ملفات csv المفصولة بفواصل.</span><span class="sxs-lookup"><span data-stu-id="693b7-263">The data factory runs based on csv files that are comma-delimited.</span></span> <span data-ttu-id="693b7-264">إذا كانت هناك قيمة حقل تتضمن فاصلة، فقد تتداخل مع النتائج.</span><span class="sxs-lookup"><span data-stu-id="693b7-264">If there is a field value that has a comma, it may interfere with the results.</span></span> <span data-ttu-id="693b7-265">تحتاج إلى إزالة الفواصل.</span><span class="sxs-lookup"><span data-stu-id="693b7-265">You need to remove the commas.</span></span>
4. <span data-ttu-id="693b7-266">توفر علامة التبويب **المراقبة** معلومات حول كافة الخطوات والبيانات التي تمت معالجتها.</span><span class="sxs-lookup"><span data-stu-id="693b7-266">The **Monitoring** tab provides information about all steps and data processed.</span></span> <span data-ttu-id="693b7-267">حدد خطوة معينة لتصحيحها.</span><span class="sxs-lookup"><span data-stu-id="693b7-267">Select a specific step to debug it.</span></span>

    ![علامة تبويب المراقبة](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a><span data-ttu-id="693b7-269">اعرف المزيد عن القالب</span><span class="sxs-lookup"><span data-stu-id="693b7-269">Learn more about the template</span></span>

<span data-ttu-id="693b7-270">يمكنك الحصول على معلومات إضافية حول القالب في [التعليقات الخاصة بالأداة التمهيدية لقالب Azure Data Factory](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).</span><span class="sxs-lookup"><span data-stu-id="693b7-270">You can find additional information about the template in [Comments for Azure Data Factory template readme](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).</span></span>
