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
ms.openlocfilehash: 76e64d483e833782733277a64d8dc37cbeba6130
ms.sourcegitcommit: 011468a6cffea8641bebc2922e0676d9f44b36fc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/06/2021
ms.locfileid: "5857360"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a><span data-ttu-id="21ef3-103">الترقية إلى الطرف ونموذج دفتر العناوين العمومي</span><span class="sxs-lookup"><span data-stu-id="21ef3-103">Upgrade to the party and global address book model</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="21ef3-104">يساعدك [قالب Azure Data Factory](https://aka.ms/dual-write-gab-adf) على ترقية بيانات جدول **حساب** و **جهة اتصال** و **مورّد** موجود في الكتابة المزدوجة إلى نموذج الطرف ودفتر العناوين العمول</span><span class="sxs-lookup"><span data-stu-id="21ef3-104">The [Azure Data Factory template](https://aka.ms/dual-write-gab-adf) helps you upgrade existing **Account**, **Contact**, and **Vendor** table data in dual-write to the party and global address book model.</span></span> <span data-ttu-id="21ef3-105">يقوم القالب بتسوية البيانات من تطبيقات Finance and Operations وتطبيقات مشاركة العميل.</span><span class="sxs-lookup"><span data-stu-id="21ef3-105">The template reconciles the data from both Finance and Operations apps and customer engagement applications.</span></span> <span data-ttu-id="21ef3-106">في نهاية العملية، سيتم إنشاء حقلي **الطرف** و **جهة الاتصال** لسجلات **الطرف** وربطها بسجلات **الحساب** و **جهة الاتصال** و **المورّد** في تطبيقات مشاركة العميل.</span><span class="sxs-lookup"><span data-stu-id="21ef3-106">At the end of the process, **Party** and **Contact** fields for **Party** records will be created and associated with **Account**, **Contact**, and **Vendor** records in customer engagement applications.</span></span> <span data-ttu-id="21ef3-107">يتم إنشاء ملف csv. (`FONewParty.csv`) لإنشاء سجلات **طرف** جديدة داخل تطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="21ef3-107">A .csv file (`FONewParty.csv`) is generated to create new **Party** records inside the Finance and Operations app.</span></span> <span data-ttu-id="21ef3-108">يوفر هذا الموضوع الإرشادات الخاصة باستخدام قالب Data Factory وترقية البيانات.</span><span class="sxs-lookup"><span data-stu-id="21ef3-108">This topic provides the instructions to use the Data Factory template and upgrade your data.</span></span>

<span data-ttu-id="21ef3-109">إذا لم يكن لديك أي تخصيصات، فيمكنك استخدام القالب كما هو.</span><span class="sxs-lookup"><span data-stu-id="21ef3-109">If you don’t have any customizations, you can use the template as-is.</span></span> <span data-ttu-id="21ef3-110">إذا كانت لديك تخصيصات لسجلات **الحساب** و **جهة الاتصال** و **المورّد**، فيجب تعديل القالب باستخدام الإرشادات التالية.</span><span class="sxs-lookup"><span data-stu-id="21ef3-110">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template using the following instructions.</span></span>

> [!Note]
> <span data-ttu-id="21ef3-111">يساعدك القالب على ترقية بيانات **الطرف**.</span><span class="sxs-lookup"><span data-stu-id="21ef3-111">The template helps to upgrade only the **Party** data.</span></span> <span data-ttu-id="21ef3-112">سيتم تضمين العناوين البريدية والإلكترونية في إصدار مستقبلي.</span><span class="sxs-lookup"><span data-stu-id="21ef3-112">In a future release, postal and electronic addresses will be included.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="21ef3-113">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="21ef3-113">Prerequisites</span></span>

<span data-ttu-id="21ef3-114">هذه المتطلبات الأساسية مطلوبة:</span><span class="sxs-lookup"><span data-stu-id="21ef3-114">These prerequisites are required:</span></span>

+ [<span data-ttu-id="21ef3-115">اشتراك Azure</span><span class="sxs-lookup"><span data-stu-id="21ef3-115">Azure subscription</span></span>](https://portal.azure.com/)
+ [<span data-ttu-id="21ef3-116">الوصول إلى القالب</span><span class="sxs-lookup"><span data-stu-id="21ef3-116">Access to the template</span></span>](https://aka.ms/dual-write-gab-adf)
+ <span data-ttu-id="21ef3-117">أنت عميل موجود للكتابة المزدوجة.</span><span class="sxs-lookup"><span data-stu-id="21ef3-117">You are an existing dual-write customer.</span></span>

## <a name="prepare-for-the-upgrade"></a><span data-ttu-id="21ef3-118">التحضير للترقية</span><span class="sxs-lookup"><span data-stu-id="21ef3-118">Prepare for the upgrade</span></span>

+ <span data-ttu-id="21ef3-119">**متزامنة بالكامل**: البيئتان في حالة متزامنة بالكامل لسجلات **الحساب (العميل)** و **جهة الاتصال** و **المورّد**.</span><span class="sxs-lookup"><span data-stu-id="21ef3-119">**Fully synched**: Both environments are fully synched state for **Account (Customer)**, **Contact**, and **Vendor**.</span></span>
+ <span data-ttu-id="21ef3-120">**مفاتيح التكامل**: تستخدم جداول **الحساب (العميل)** و **جهة الاتصال** و **المورّد** في تطبيقات مشاركة العميل مفاتيح التكامل المشحونة الجاهزة.</span><span class="sxs-lookup"><span data-stu-id="21ef3-120">**Integration keys**: **Account (Customer)**, **Contact**, and **Vendor** tables in customer engagement apps are using the integration keys that shipped out-of-the-box.</span></span> <span data-ttu-id="21ef3-121">إذا قمت بتخصيص مفاتيح التكامل، فيجب تخصيص القالب.</span><span class="sxs-lookup"><span data-stu-id="21ef3-121">If you customized the integration keys, you must customize the template.</span></span>
+ <span data-ttu-id="21ef3-122">**رقم الطرف**: سيكون لجميع سجلات **الحساب (العميل)** و **جهة الاتصال** و **المورّد** التي سيتم ترقيتها رقم **طرف**.</span><span class="sxs-lookup"><span data-stu-id="21ef3-122">**Party number**: All **Account (Customer)**, **Contact**, and **Vendor** records that will be upgraded have a **Party** number.</span></span> <span data-ttu-id="21ef3-123">سيتم تجاهل السجلات التي لا تحتوي على رقم **طرف**.</span><span class="sxs-lookup"><span data-stu-id="21ef3-123">Records without a **Party** number will be ignored.</span></span> <span data-ttu-id="21ef3-124">إذا كنت ترغب في ترقية تلك السجلات، فيمكنك إضافة رقم **طرف** إليها قبل بدء عملية الترقية.</span><span class="sxs-lookup"><span data-stu-id="21ef3-124">If you want to upgrade those records, add a **Party** number to them before you start the upgrade process.</span></span>
+ <span data-ttu-id="21ef3-125">**انقطاع العمل في النظام**: أثناء عملية الترقية، يجب عليك وضع بيئات Finance and Operations وبيئات مشاركة العميل في وضع عدم الاتصال.</span><span class="sxs-lookup"><span data-stu-id="21ef3-125">**System outage**: During the upgrade process, you will have to take both the Finance and Operations and customer engagement environments offline.</span></span>
+ <span data-ttu-id="21ef3-126">**لقطة**: خذ لقطات لتطبيقات Finance and Operations وتطبيقات مشاركة العميل.</span><span class="sxs-lookup"><span data-stu-id="21ef3-126">**Snapshot**: Take snapshots of both the Finance and Operations and customer engagement apps.</span></span> <span data-ttu-id="21ef3-127">استخدم اللقطات لاسترجاع الحالة السابقة إذا احتجت لذلك.</span><span class="sxs-lookup"><span data-stu-id="21ef3-127">Use the snapshots to restore the previous state if you need to.</span></span>

## <a name="deployment"></a><span data-ttu-id="21ef3-128">النشر</span><span class="sxs-lookup"><span data-stu-id="21ef3-128">Deployment</span></span>

1. <span data-ttu-id="21ef3-129">نزّل القالب من [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span><span class="sxs-lookup"><span data-stu-id="21ef3-129">Download the template from [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span></span>

2. <span data-ttu-id="21ef3-130">سجل دخولك إلى [Microsoft Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="21ef3-130">Sign in to [Microsoft Azure](https://portal.azure.com/).</span></span>

3. <span data-ttu-id="21ef3-131">أنشئ [مجموعة موارد](https://docs.microsoft.com/azure/azure-resource-manager/management/manage-resource-groups-portal).</span><span class="sxs-lookup"><span data-stu-id="21ef3-131">Create a [resource group](https://docs.microsoft.com/azure/azure-resource-manager/management/manage-resource-groups-portal).</span></span>

4. <span data-ttu-id="21ef3-132">أنشئ [حساب تخزين](https://docs.microsoft.com/azure/storage/common/storage-account-create?tabs=azure-portal) في مجموعة الموارد التي أنشأتها.</span><span class="sxs-lookup"><span data-stu-id="21ef3-132">Create a [storage account](https://docs.microsoft.com/azure/storage/common/storage-account-create?tabs=azure-portal) in the resource group that you created.</span></span>

5. <span data-ttu-id="21ef3-133">أنشئ [مصنع بيانات](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-portal) في مجموعة الموارد أعلاه التي أنشأتها.</span><span class="sxs-lookup"><span data-stu-id="21ef3-133">Create a [data factory](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-portal) in above resource group that you created.</span></span>

6. <span data-ttu-id="21ef3-134">افتح مصنع البيانات وحدد اللوحة **التأليف والمراقبة**.</span><span class="sxs-lookup"><span data-stu-id="21ef3-134">Open the data factory and select the **Author & Monitor** tile.</span></span>

7. <span data-ttu-id="21ef3-135">على علامة التبويب **إدارة**، حدد **قالب ARM**.</span><span class="sxs-lookup"><span data-stu-id="21ef3-135">On the **Manage** tab, select **ARM template**.</span></span>

8. <span data-ttu-id="21ef3-136">حدد **استيراد قالب ARM** لاستيراد قالب **الطرف‏‎**.</span><span class="sxs-lookup"><span data-stu-id="21ef3-136">Select the **Import ARM template** to import the **Party** template.</span></span>

9. <span data-ttu-id="21ef3-137">استورد القالب إلى مصنع البيانات.</span><span class="sxs-lookup"><span data-stu-id="21ef3-137">Import the template into the data factory.</span></span> <span data-ttu-id="21ef3-138">أدخل القيم التالية في **تفاصيل المشروع** و **تفاصيل المثيل**.</span><span class="sxs-lookup"><span data-stu-id="21ef3-138">Enter the following values for **Project details** and **Instance details**.</span></span>

    <span data-ttu-id="21ef3-139">الحقل</span><span class="sxs-lookup"><span data-stu-id="21ef3-139">Field</span></span> | <span data-ttu-id="21ef3-140">قيمة</span><span class="sxs-lookup"><span data-stu-id="21ef3-140">Value</span></span>
    ---|---
    <span data-ttu-id="21ef3-141">الاشتراك</span><span class="sxs-lookup"><span data-stu-id="21ef3-141">Subscription</span></span> | <span data-ttu-id="21ef3-142">اشتراك Azure</span><span class="sxs-lookup"><span data-stu-id="21ef3-142">Azure subscription</span></span>
    <span data-ttu-id="21ef3-143">مجموعة الموارد</span><span class="sxs-lookup"><span data-stu-id="21ef3-143">Resource group</span></span> | <span data-ttu-id="21ef3-144">قدم المورد نفسه الذي يتم إنشاء حساب التخزين ضمنه.</span><span class="sxs-lookup"><span data-stu-id="21ef3-144">Provide same resource under which storage account is created.</span></span>
    <span data-ttu-id="21ef3-145">المنطقة</span><span class="sxs-lookup"><span data-stu-id="21ef3-145">Region</span></span> | <span data-ttu-id="21ef3-146">حدد منطقة.</span><span class="sxs-lookup"><span data-stu-id="21ef3-146">Specify region.</span></span>
    <span data-ttu-id="21ef3-147">اسم المصنع</span><span class="sxs-lookup"><span data-stu-id="21ef3-147">Factory Name</span></span> | <span data-ttu-id="21ef3-148">حدد اسم المصنع.</span><span class="sxs-lookup"><span data-stu-id="21ef3-148">Specify factory name.</span></span>
    <span data-ttu-id="21ef3-149">FO Linked Service_service Principal Key</span><span class="sxs-lookup"><span data-stu-id="21ef3-149">FO Linked Service_service Principal Key</span></span> | <span data-ttu-id="21ef3-150">حدد مفتاح التطبيق.</span><span class="sxs-lookup"><span data-stu-id="21ef3-150">Specify the application's key.</span></span>
    <span data-ttu-id="21ef3-151">Azure Blob Storage_connection String</span><span class="sxs-lookup"><span data-stu-id="21ef3-151">Azure Blob Storage_connection String</span></span> | <span data-ttu-id="21ef3-152">سلسلة اتصال مخزن البيانات الثنائية كبيرة الحجم لـ Azure.‬</span><span class="sxs-lookup"><span data-stu-id="21ef3-152">Azure Blob storage connection string.</span></span>
    <span data-ttu-id="21ef3-153">Dynamics Crm Linked Service_password</span><span class="sxs-lookup"><span data-stu-id="21ef3-153">Dynamics Crm Linked Service_password</span></span> | <span data-ttu-id="21ef3-154">كلمة المرور الخاصة بحساب المستخدم الذي حددته كاسم المستخدم.</span><span class="sxs-lookup"><span data-stu-id="21ef3-154">The password for the user account you specified as the username.</span></span>
    <span data-ttu-id="21ef3-155">FO Linked Service_properties_type Properties_url</span><span class="sxs-lookup"><span data-stu-id="21ef3-155">FO Linked Service_properties_type Properties_url</span></span>  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    <span data-ttu-id="21ef3-156">FO Linked Service_properties_type Properties_tenant</span><span class="sxs-lookup"><span data-stu-id="21ef3-156">FO Linked Service_properties_type Properties_tenant</span></span> | <span data-ttu-id="21ef3-157">حدد معلومات المستأجر (اسم المجال أو معرف المستأجر) الذي يوجد تطبيقك ضمنه.</span><span class="sxs-lookup"><span data-stu-id="21ef3-157">Specify the tenant information (domain name or tenant ID) under which your application resides.</span></span>
    <span data-ttu-id="21ef3-158">FO Linked Service_properties_type Properties_aad Resource Id</span><span class="sxs-lookup"><span data-stu-id="21ef3-158">FO Linked Service_properties_type Properties_aad Resource Id</span></span> | `https://sampledynamics.sandboxoperationsdynamics.com`
    <span data-ttu-id="21ef3-159">FO Linked Service_properties_type Properties_service Principal Id</span><span class="sxs-lookup"><span data-stu-id="21ef3-159">FO Linked Service_properties_type Properties_service Principal Id</span></span> | <span data-ttu-id="21ef3-160">حدد معرف عميل التطبيق.</span><span class="sxs-lookup"><span data-stu-id="21ef3-160">Specify the application's client ID.</span></span>
    <span data-ttu-id="21ef3-161">Dynamics Crm Linked Service_properties_type Properties_username</span><span class="sxs-lookup"><span data-stu-id="21ef3-161">Dynamics Crm Linked Service_properties_type Properties_username</span></span> | <span data-ttu-id="21ef3-162">اسم المستخدم الذي سيتصل بـ Dynamics.</span><span class="sxs-lookup"><span data-stu-id="21ef3-162">The username to connect to Dynamics.</span></span>

    <span data-ttu-id="21ef3-163">لمزيد من المعلومات، راجع [ترقية قالب إدارة الموارد يدويًا لكل بيئة](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)، و[خصائص الخدمة المرتبطة](https://docs.microsoft.com/azure/data-factory/connector-dynamics-ax#linked-service-properties)، و[نسخ البيانات باستخدام Azure Data Factory](https://docs.microsoft.com/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span><span class="sxs-lookup"><span data-stu-id="21ef3-163">For more information, see [Manually promote a Resource Manager template for each environment](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Linked service properties](https://docs.microsoft.com/azure/data-factory/connector-dynamics-ax#linked-service-properties), and [Copy data using Azure Data Factory](https://docs.microsoft.com/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span></span>

10. <span data-ttu-id="21ef3-164">بعد عملية النشر، تحقق من صحة مجموعات البيانات وتدفق البيانات والخدمة المرتبطة لمصنع البيانات.</span><span class="sxs-lookup"><span data-stu-id="21ef3-164">After deployment, validate the datasets, data flow, and linked service of the data factory.</span></span>

   ![مجموعات البيانات وتدفق البيانات والخدمة المرتبطة](media/data-factory-validate.png)

11. <span data-ttu-id="21ef3-166">انتقل إلى **إدارة**.</span><span class="sxs-lookup"><span data-stu-id="21ef3-166">Navigate to **Manage**.</span></span> <span data-ttu-id="21ef3-167">ضمن **الاتصالات**، حدد **الخدمة المرتبطة**.</span><span class="sxs-lookup"><span data-stu-id="21ef3-167">Under **Connections**, select **Linked Service**.</span></span> <span data-ttu-id="21ef3-168">حدد **DynamicsCrmLinkedService**.</span><span class="sxs-lookup"><span data-stu-id="21ef3-168">Select **DynamicsCrmLinkedService**.</span></span> <span data-ttu-id="21ef3-169">في النموذج **تحرير الخدمة المرتبطة (Dynamics CRM)**، أدخل القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="21ef3-169">In the **Edit linked service (Dynamics CRM)** form, enter the following values:</span></span>

    <span data-ttu-id="21ef3-170">الحقل</span><span class="sxs-lookup"><span data-stu-id="21ef3-170">Field</span></span> | <span data-ttu-id="21ef3-171">قيمة</span><span class="sxs-lookup"><span data-stu-id="21ef3-171">Value</span></span>
    ---|---
    <span data-ttu-id="21ef3-172">الاسم</span><span class="sxs-lookup"><span data-stu-id="21ef3-172">Name</span></span> | <span data-ttu-id="21ef3-173">DynamicsCrmLinkedService</span><span class="sxs-lookup"><span data-stu-id="21ef3-173">DynamicsCrmLinkedService</span></span>
    <span data-ttu-id="21ef3-174">الوصف</span><span class="sxs-lookup"><span data-stu-id="21ef3-174">Description</span></span> | <span data-ttu-id="21ef3-175">الخدمات المرتبطة للاتصال بمثيل CRM لإحضار بيانات الوحدات</span><span class="sxs-lookup"><span data-stu-id="21ef3-175">Linked services to connect with CRM instance to fetch entities data</span></span>
    <span data-ttu-id="21ef3-176">الاتصال عبر وقت تشغيل التكامل</span><span class="sxs-lookup"><span data-stu-id="21ef3-176">Connect via integration runtime</span></span> | <span data-ttu-id="21ef3-177">AutoResolvelntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="21ef3-177">AutoResolvelntegrationRuntime</span></span>
    <span data-ttu-id="21ef3-178">نوع النشر</span><span class="sxs-lookup"><span data-stu-id="21ef3-178">Deployment type</span></span> | <span data-ttu-id="21ef3-179">عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="21ef3-179">Online</span></span>
    <span data-ttu-id="21ef3-180">Uri الخاص بالخدمة</span><span class="sxs-lookup"><span data-stu-id="21ef3-180">Service Uri</span></span> | `https://<organization-name>.crm[x].dynamics.com`
    <span data-ttu-id="21ef3-181">نوع المصادقة</span><span class="sxs-lookup"><span data-stu-id="21ef3-181">Authentication type</span></span> | <span data-ttu-id="21ef3-182">Office365</span><span class="sxs-lookup"><span data-stu-id="21ef3-182">Office365</span></span>
    <span data-ttu-id="21ef3-183">اسم المستخدم</span><span class="sxs-lookup"><span data-stu-id="21ef3-183">User name</span></span> |
    <span data-ttu-id="21ef3-184">كلمة المرور أو Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="21ef3-184">Password or Azure Key Vault</span></span> | <span data-ttu-id="21ef3-185">كلمة المرور</span><span class="sxs-lookup"><span data-stu-id="21ef3-185">Password</span></span>
    <span data-ttu-id="21ef3-186">كلمة المرور</span><span class="sxs-lookup"><span data-stu-id="21ef3-186">Password</span></span> |

## <a name="run-the-template"></a><span data-ttu-id="21ef3-187">تشغيل القالب</span><span class="sxs-lookup"><span data-stu-id="21ef3-187">Run the template</span></span>

1. <span data-ttu-id="21ef3-188">أوقف الكتابة المزدوجة في **الحساب** و **جهة  الاتصال** و **المورّد** باستخدام تطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="21ef3-188">Stop the following **Account**, **Contact**, and **Vendor** dual-write using the Finance and Operations app.</span></span>

    + <span data-ttu-id="21ef3-189">العملاء V3 (الحسابات)</span><span class="sxs-lookup"><span data-stu-id="21ef3-189">Customers V3(accounts)</span></span>
    + <span data-ttu-id="21ef3-190">العملاء V3 (جهات الاتصال)</span><span class="sxs-lookup"><span data-stu-id="21ef3-190">Customers V3(contacts)</span></span>
    + <span data-ttu-id="21ef3-191">جهات اتصال CDS‏ V2 (جهات الاتصال)</span><span class="sxs-lookup"><span data-stu-id="21ef3-191">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="21ef3-192">جهات اتصال CDS‏ V2 (جهات الاتصال)</span><span class="sxs-lookup"><span data-stu-id="21ef3-192">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="21ef3-193">المورّد V2 ‏(msdyn_vendor)</span><span class="sxs-lookup"><span data-stu-id="21ef3-193">Vendor V2 (msdyn_vendor)</span></span>

2. <span data-ttu-id="21ef3-194">تأكد من إزالة الخرائط من الجدول `msdy_dualwriteruntimeconfig` في Dataverse.</span><span class="sxs-lookup"><span data-stu-id="21ef3-194">Make sure the maps are removed from the `msdy_dualwriteruntimeconfig` table in Dataverse.</span></span>

3. <span data-ttu-id="21ef3-195">ثبّت [حلول الكتابة المزدوجة للطرف ودفتر العناوين العمومي](https://aka.ms/dual-write-gab) من AppSource.</span><span class="sxs-lookup"><span data-stu-id="21ef3-195">Install [Dual-write Party and Global Address Book Solutions](https://aka.ms/dual-write-gab) from AppSource.</span></span>

4. <span data-ttu-id="21ef3-196">في تطبيق Finance and Operations، إذا كانت الجداول التالية تحتوي على بيانات، فشغّل **المزامنة الأولية** لها.</span><span class="sxs-lookup"><span data-stu-id="21ef3-196">In the Finance and Operations app, if the following tables contain data, then run **Initial Sync** for them.</span></span>

    + <span data-ttu-id="21ef3-197">التحيات</span><span class="sxs-lookup"><span data-stu-id="21ef3-197">Salutations</span></span>
    + <span data-ttu-id="21ef3-198">أنواع الخصائص الشخصية</span><span class="sxs-lookup"><span data-stu-id="21ef3-198">Personal character types</span></span>
    + <span data-ttu-id="21ef3-199">الختام الإطرائي</span><span class="sxs-lookup"><span data-stu-id="21ef3-199">Complimentary closing</span></span>
    + <span data-ttu-id="21ef3-200">ألقاب جهات الاتصال</span><span class="sxs-lookup"><span data-stu-id="21ef3-200">Contact person titles</span></span>
    + <span data-ttu-id="21ef3-201">أدوار صنع القرار</span><span class="sxs-lookup"><span data-stu-id="21ef3-201">Decision making roles</span></span>
    + <span data-ttu-id="21ef3-202">مستويات الولاء</span><span class="sxs-lookup"><span data-stu-id="21ef3-202">Loyalty levels</span></span>

5. <span data-ttu-id="21ef3-203">في تطبيق مشاركة العميل، قم بتعطيل خطوات المكون الإضافي التالية.</span><span class="sxs-lookup"><span data-stu-id="21ef3-203">In the customer engagement app, disable the following plugin steps.</span></span>

    + <span data-ttu-id="21ef3-204">تحديث الحساب</span><span class="sxs-lookup"><span data-stu-id="21ef3-204">Account Update</span></span>
         + <span data-ttu-id="21ef3-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: تحديث حساب</span><span class="sxs-lookup"><span data-stu-id="21ef3-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="21ef3-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: تحديث حساب</span><span class="sxs-lookup"><span data-stu-id="21ef3-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="21ef3-207">تحديث جهة الاتصال</span><span class="sxs-lookup"><span data-stu-id="21ef3-207">Contact Update</span></span>
         + <span data-ttu-id="21ef3-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: تحديث جهة اتصال</span><span class="sxs-lookup"><span data-stu-id="21ef3-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="21ef3-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: تحديث جهة اتصال</span><span class="sxs-lookup"><span data-stu-id="21ef3-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="21ef3-210">msdyn_party Update</span><span class="sxs-lookup"><span data-stu-id="21ef3-210">msdyn_party Update</span></span>
         + <span data-ttu-id="21ef3-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: تحديث msdyn_party</span><span class="sxs-lookup"><span data-stu-id="21ef3-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="21ef3-212">msdyn_vendor Update</span><span class="sxs-lookup"><span data-stu-id="21ef3-212">msdyn_vendor Update</span></span>
         + <span data-ttu-id="21ef3-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: تحديث msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="21ef3-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

6. <span data-ttu-id="21ef3-214">في تطبيق مشاركة العميل، قم بتعطيل عمليات سير العمل التالية.</span><span class="sxs-lookup"><span data-stu-id="21ef3-214">In the customer engagement app, disable the following workflows:</span></span>

    + <span data-ttu-id="21ef3-215">إنشاء الموردين في جدول الحسابات</span><span class="sxs-lookup"><span data-stu-id="21ef3-215">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="21ef3-216">إنشاء الموردين في جدول الحسابات</span><span class="sxs-lookup"><span data-stu-id="21ef3-216">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="21ef3-217">إنشاء مورّدين من نوع الشخص في جدول جهات الاتصال</span><span class="sxs-lookup"><span data-stu-id="21ef3-217">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="21ef3-218">إنشاء الموردين من نوع الشخص في جدول الموردين</span><span class="sxs-lookup"><span data-stu-id="21ef3-218">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="21ef3-219">تحديث الموردين في جدول الحسابات</span><span class="sxs-lookup"><span data-stu-id="21ef3-219">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="21ef3-220">تحديث الموردين في جدول الموردين</span><span class="sxs-lookup"><span data-stu-id="21ef3-220">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="21ef3-221">تحديث الموردين من نوع الشخص في جدول جهات الاتصال</span><span class="sxs-lookup"><span data-stu-id="21ef3-221">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="21ef3-222">تحديث الموردين من نوع الشخص في جدول الموردين</span><span class="sxs-lookup"><span data-stu-id="21ef3-222">Update Vendors of type Person in Vendors Table</span></span>

7. <span data-ttu-id="21ef3-223">في مصنع البيانات، قم بتشغيل القالب عن طريق تحديد **تشغيل الآن** كما هو موضح في الصورة التالية.</span><span class="sxs-lookup"><span data-stu-id="21ef3-223">In the data factory, run the template by selecting **Trigger now** as shown in the following image.</span></span> <span data-ttu-id="21ef3-224">قد تتطلب هذه العملية بضع ساعات لتكتمل بالاستناد إلى حجم البيانات.</span><span class="sxs-lookup"><span data-stu-id="21ef3-224">This process might take a few hours to complete based on the data volume.</span></span>

    ![تشغيل المشغل](media/data-factory-trigger.png)

    > [!NOTE]
    > <span data-ttu-id="21ef3-226">إذا كانت لديك تخصيصات لسجلات **الحساب** و **جهة الاتصال** و **المورّد**، فيجب تعديل القالب.</span><span class="sxs-lookup"><span data-stu-id="21ef3-226">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template.</span></span>

8. <span data-ttu-id="21ef3-227">استورد سجلات **الطرف** الجديد في تطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="21ef3-227">Import the new **Party** records in the Finance and Operations app.</span></span>

    + <span data-ttu-id="21ef3-228">نزّل الملف `FONewParty.csv` من مخزن البيانات الثنائية كبيرة الحجم لـ Azure.</span><span class="sxs-lookup"><span data-stu-id="21ef3-228">Download the `FONewParty.csv` file from Azure blob storage.</span></span> <span data-ttu-id="21ef3-229">المسار هو `partybootstrapping/output/FONewParty.csv`.</span><span class="sxs-lookup"><span data-stu-id="21ef3-229">The path is `partybootstrapping/output/FONewParty.csv`.</span></span>
    + <span data-ttu-id="21ef3-230">حوّل الملف `FONewParty.csv` إلى ملف Excel واستورد ملف Excel إلى تطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="21ef3-230">Convert the `FONewParty.csv` file into an Excel file and import the Excel file into the Finance and Operations app.</span></span>  <span data-ttu-id="21ef3-231">إذا نجحت عملية استيراد csv، فيمكنك استيراد ملف csv مباشرة.</span><span class="sxs-lookup"><span data-stu-id="21ef3-231">If the csv import works for you, you can import csv file directly.</span></span> <span data-ttu-id="21ef3-232">قد يستغرق تشغيل عملية الاستيراد بضع ساعات، بحسب حجم البيانات.</span><span class="sxs-lookup"><span data-stu-id="21ef3-232">The import could take a few hours to run, depending on the data volume.</span></span> <span data-ttu-id="21ef3-233">لمزيد من المعلومات راجع [نظرة عامة حول وظائف استيراد البيانات وتصديرها](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job).</span><span class="sxs-lookup"><span data-stu-id="21ef3-233">For more information, see [Data import and export jobs overview](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job).</span></span>

    ![استيراد سجلات طرف Datavers](media/data-factory-import-party.png)

9. <span data-ttu-id="21ef3-235">في تطبيقات مشاركة العميل، قم بتمكين خطوات المكون الإضافي التالية:</span><span class="sxs-lookup"><span data-stu-id="21ef3-235">In the customer engagement apps, enable the following plugin steps:</span></span>

    + <span data-ttu-id="21ef3-236">تحديث الحساب</span><span class="sxs-lookup"><span data-stu-id="21ef3-236">Account Update</span></span>
         + <span data-ttu-id="21ef3-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: تحديث حساب</span><span class="sxs-lookup"><span data-stu-id="21ef3-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="21ef3-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: تحديث حساب</span><span class="sxs-lookup"><span data-stu-id="21ef3-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="21ef3-239">تحديث جهة الاتصال</span><span class="sxs-lookup"><span data-stu-id="21ef3-239">Contact Update</span></span>
         + <span data-ttu-id="21ef3-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: تحديث جهة اتصال</span><span class="sxs-lookup"><span data-stu-id="21ef3-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="21ef3-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: تحديث جهة اتصال</span><span class="sxs-lookup"><span data-stu-id="21ef3-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="21ef3-242">msdyn_party Update</span><span class="sxs-lookup"><span data-stu-id="21ef3-242">msdyn_party Update</span></span>
         + <span data-ttu-id="21ef3-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: تحديث msdyn_party</span><span class="sxs-lookup"><span data-stu-id="21ef3-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="21ef3-244">msdyn_vendor Update</span><span class="sxs-lookup"><span data-stu-id="21ef3-244">msdyn_vendor Update</span></span>
         + <span data-ttu-id="21ef3-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: تحديث msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="21ef3-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

10. <span data-ttu-id="21ef3-246">في تطبيقات مشاركة العميل، قم بتنشيط عمليات سير العمل التالية إذا قمت بإلغاء تنشيطها في الخطوات السابقة:</span><span class="sxs-lookup"><span data-stu-id="21ef3-246">In the customer engagement apps, activate the following workflows if you deactivated them in previous steps:</span></span>

    + <span data-ttu-id="21ef3-247">إنشاء الموردين في جدول الحسابات</span><span class="sxs-lookup"><span data-stu-id="21ef3-247">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="21ef3-248">إنشاء الموردين في جدول الحسابات</span><span class="sxs-lookup"><span data-stu-id="21ef3-248">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="21ef3-249">إنشاء مورّدين من نوع الشخص في جدول جهات الاتصال</span><span class="sxs-lookup"><span data-stu-id="21ef3-249">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="21ef3-250">إنشاء الموردين من نوع الشخص في جدول الموردين</span><span class="sxs-lookup"><span data-stu-id="21ef3-250">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="21ef3-251">تحديث الموردين في جدول الحسابات</span><span class="sxs-lookup"><span data-stu-id="21ef3-251">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="21ef3-252">تحديث الموردين في جدول الموردين</span><span class="sxs-lookup"><span data-stu-id="21ef3-252">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="21ef3-253">تحديث الموردين من نوع الشخص في جدول جهات الاتصال</span><span class="sxs-lookup"><span data-stu-id="21ef3-253">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="21ef3-254">تحديث الموردين من نوع الشخص في جدول الموردين</span><span class="sxs-lookup"><span data-stu-id="21ef3-254">Update Vendors of type Person in Vendors Table</span></span>

11. <span data-ttu-id="21ef3-255">شغّل الخرائط ذات الصلة **بالطرف** كما هو موضح في [الطرف ودفتر العناوين العمومي](party-gab.md).</span><span class="sxs-lookup"><span data-stu-id="21ef3-255">Run the **Party**-related maps as instructed in [Party and global address book](party-gab.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="21ef3-256">استكشاف الأخطاء وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="21ef3-256">Troubleshooting</span></span>

1. <span data-ttu-id="21ef3-257">في حالة فشل العملية، أعد تشغيل مصنع البيانات بدءًا من النشاط الفاشل.</span><span class="sxs-lookup"><span data-stu-id="21ef3-257">In the process fails, rerun the data factory starting from the failed activity.</span></span>
2. <span data-ttu-id="21ef3-258">يتم إنشاء بعض الملفات بواسطة مصنع البيانات الذي يمكنك استخدامه لغرض التحقق من صحة البيانات.</span><span class="sxs-lookup"><span data-stu-id="21ef3-258">Some files are generated by the data factory that you can use for data validation purpose.</span></span>
3. <span data-ttu-id="21ef3-259">يتم تشغيل مصنع البيانات استنادًا إلى ملفات csv المفصولة بفواصل.</span><span class="sxs-lookup"><span data-stu-id="21ef3-259">The data factory runs based on csv files that are comma-delimited.</span></span> <span data-ttu-id="21ef3-260">إذا كانت هناك قيمة حقل تتضمن فاصلة، فقد تتداخل مع النتائج.</span><span class="sxs-lookup"><span data-stu-id="21ef3-260">If there is a field value that has a comma, it may interfere with the results.</span></span> <span data-ttu-id="21ef3-261">تحتاج إلى إزالة الفواصل.</span><span class="sxs-lookup"><span data-stu-id="21ef3-261">You need to remove the commas.</span></span>
4. <span data-ttu-id="21ef3-262">توفر علامة التبويب **المراقبة** معلومات حول كافة الخطوات والبيانات التي تمت معالجتها.</span><span class="sxs-lookup"><span data-stu-id="21ef3-262">The **Monitoring** tab provides information about all steps and data processed.</span></span> <span data-ttu-id="21ef3-263">حدد خطوة معينة لتصحيحها.</span><span class="sxs-lookup"><span data-stu-id="21ef3-263">Select a specific step to debug it.</span></span>

    ![علامة تبويب المراقبة](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a><span data-ttu-id="21ef3-265">اعرف المزيد عن القالب</span><span class="sxs-lookup"><span data-stu-id="21ef3-265">Learn more about the template</span></span>

<span data-ttu-id="21ef3-266">يمكنك العثور علي تعليقات على القالب في ملف [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).</span><span class="sxs-lookup"><span data-stu-id="21ef3-266">You can find comments for the template the [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md) file.</span></span>
