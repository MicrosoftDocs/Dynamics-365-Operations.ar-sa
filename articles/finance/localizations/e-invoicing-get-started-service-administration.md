---
title: البدء باستخدام إدارة خدمة الفوترة الإلكترونية
description: يوضح هذا الموضوع كيفية بدء استخدام الفوترة الإلكترونية.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ec431cb4a3620459d905f64a80fd820a2113290f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840138"
---
# <a name="get-started-with-electronic-invoicing-service-administration"></a><span data-ttu-id="b0131-103">البدء باستخدام إدارة خدمة الفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="b0131-103">Get started with Electronic invoicing service administration</span></span>

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="b0131-104">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="b0131-104">Prerequisites</span></span>

<span data-ttu-id="b0131-105">قبل أن تتمكن من استكمال الإجراءات في هذا الموضوع، يجب إتمام المهام المتطلبات التالية:</span><span class="sxs-lookup"><span data-stu-id="b0131-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="b0131-106">يجب أن يكون لديك حق الوصول إلى حساب Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="b0131-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="b0131-107">يجب ان يكون لديك مشروع LCS يتضمن إصدار 10.0.17 أو إصدار أحدث من Microsoft Dynamics 365 Finance وDynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b0131-107">You must have an LCS project that includes version 10.0.17 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="b0131-108">بالإضافة إلى ذلك، يجب أن يتم نشر هذه التطبيقات في أحد مناطق Azure الجغرافية التالية:</span><span class="sxs-lookup"><span data-stu-id="b0131-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="b0131-109">شرق الولايات المتحدة</span><span class="sxs-lookup"><span data-stu-id="b0131-109">East US</span></span>
    - <span data-ttu-id="b0131-110">غرب الولايات المتحدة</span><span class="sxs-lookup"><span data-stu-id="b0131-110">West US</span></span>
    - <span data-ttu-id="b0131-111">شمال الاتحاد الأوروبي</span><span class="sxs-lookup"><span data-stu-id="b0131-111">North EU</span></span>
    - <span data-ttu-id="b0131-112">غرب الاتحاد الأوروبي</span><span class="sxs-lookup"><span data-stu-id="b0131-112">West EU</span></span>

- <span data-ttu-id="b0131-113">يجب أن يكون لديك حق الوصول إلى حساب Dynamics 365 Regulatory Configuration Services (RCS)</span><span class="sxs-lookup"><span data-stu-id="b0131-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="b0131-114">يجب تشغيل ميزة العولمة لحساب RCS في إدارة الميزات.</span><span class="sxs-lookup"><span data-stu-id="b0131-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="b0131-115">لمزيد من المعلومات، راجع [Regulatory Configuration Services (RCS) - ميزات العولمة](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="b0131-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="b0131-116">يجب إنشاء مخزن رئيسي وحساب تخزين في Azure.</span><span class="sxs-lookup"><span data-stu-id="b0131-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="b0131-117">لمزيد من المعلومات، راجع [إنشاء حساب تخزين وKey Vault ومخزن رئيسي](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="b0131-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a><span data-ttu-id="b0131-118">تثبيت الوظيفة الإضافية للخدمات المصغرة في Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="b0131-118">Install the add-in for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="b0131-119">سجل دخولك إلى حساب LCS.</span><span class="sxs-lookup"><span data-stu-id="b0131-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="b0131-120">حدد تجانب **إدارة ميزة المعاينة**.</span><span class="sxs-lookup"><span data-stu-id="b0131-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="b0131-121">في قسم **ميزات المعاينة العامة**، حدد **خدمة الفوترة الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="b0131-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="b0131-122">تأكد من تعيين خيار **‬‏‫ميزة المعاينه ممكنة** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="b0131-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>
5. <span data-ttu-id="b0131-123">في لوحة معلومات LCS، حدد مشروع توزيع LCS الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="b0131-123">On your LCS dashboard, select your LCS deployment project.</span></span> <span data-ttu-id="b0131-124">يجب أن يكون مشروع LCS قيد التشغيل.</span><span class="sxs-lookup"><span data-stu-id="b0131-124">The LCS project must be running.</span></span>
7. <span data-ttu-id="b0131-125">على علامة التبويب **الوظائف الإضافية للبيئة**، حدد **تثبيت وظيفة إضافية جديدة**.</span><span class="sxs-lookup"><span data-stu-id="b0131-125">On the **Environment add-ins** tab, select **Install a new add-in**.</span></span>
8. <span data-ttu-id="b0131-126">حدد **خدمات الفوترة الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="b0131-126">Select **e-invoicing Services**.</span></span>
9. <span data-ttu-id="b0131-127">في حقل **معرف تطبيق AAD**، أدخل **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span><span class="sxs-lookup"><span data-stu-id="b0131-127">In the **AAD application ID** field, enter **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span></span> <span data-ttu-id="b0131-128">هذه قيمة ثابتة.</span><span class="sxs-lookup"><span data-stu-id="b0131-128">This is a fixed value.</span></span>
10. <span data-ttu-id="b0131-129">في الحقل **معرف مستأجر AAD**، أدخل معرف المستأجر لحساب اشتراك Azure.</span><span class="sxs-lookup"><span data-stu-id="b0131-129">In the **AAD tenant ID** field, enter the tenant ID of your Azure subscription account.</span></span>
11. <span data-ttu-id="b0131-130">راجع البنود والشروط، ثم حدد خانة الاختيار.</span><span class="sxs-lookup"><span data-stu-id="b0131-130">Review the terms and conditions, and then select the check box.</span></span>
12. <span data-ttu-id="b0131-131">حدد **تثبيت**.</span><span class="sxs-lookup"><span data-stu-id="b0131-131">Select **Install**.</span></span>


## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a><span data-ttu-id="b0131-132">إعداد المعلمات لتكامل RCS باستخدام الفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="b0131-132">Set up the parameters for RCS integration with Electronic invoicing</span></span>

1. <span data-ttu-id="b0131-133">سجل دخولك إلى حساب RCS.</span><span class="sxs-lookup"><span data-stu-id="b0131-133">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="b0131-134">في مساحة عمل **التقارير الإلكترونية**، في قسم **الارتباطات‬ ذات الصلة**، حدد **معلمات التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="b0131-134">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="b0131-135">في علامة تبويب **خدمة الفوترة الإلكترونية**، في حقل **URI لنقطة نهاية الخدمة**، أدخل نقطة نهاية الخدمة المناسبة لمنطقة Azure الجغرافية الخاصة بك، كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="b0131-135">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="b0131-136">منطقة Azure الجغرافية لمركز البيانات</span><span class="sxs-lookup"><span data-stu-id="b0131-136">Datacenter Azure geography</span></span> | <span data-ttu-id="b0131-137">عنوان URI لنقطة نهاية الخدمة</span><span class="sxs-lookup"><span data-stu-id="b0131-137">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="b0131-138">شرق الولايات المتحدة</span><span class="sxs-lookup"><span data-stu-id="b0131-138">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="b0131-139">غرب الولايات المتحدة</span><span class="sxs-lookup"><span data-stu-id="b0131-139">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="b0131-140">شمال الاتحاد الأوروبي</span><span class="sxs-lookup"><span data-stu-id="b0131-140">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="b0131-141">غرب الاتحاد الأوروبي</span><span class="sxs-lookup"><span data-stu-id="b0131-141">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="b0131-142">تأكد من أنه تم تعيين حقل **معرف التطبيق** إلى **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="b0131-142">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="b0131-143">هذه القيمة هي قيمة ثابتة.</span><span class="sxs-lookup"><span data-stu-id="b0131-143">This value is a fixed value.</span></span>
5. <span data-ttu-id="b0131-144">في الحقل **معرف بيئة LCS**، أدخل معرف بيئة LCS.</span><span class="sxs-lookup"><span data-stu-id="b0131-144">In the **LCS Environment Id** field, enter the ID of your LCS environment.</span></span>
6. <span data-ttu-id="b0131-145">حدد **حفظ** ثم قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b0131-145">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-references"></a><span data-ttu-id="b0131-146">إنشاء مراجع المخزن الرئيسي</span><span class="sxs-lookup"><span data-stu-id="b0131-146">Create Key Vault references</span></span>

1. <span data-ttu-id="b0131-147">سجل دخولك إلى حساب RCS.</span><span class="sxs-lookup"><span data-stu-id="b0131-147">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="b0131-148">في مساحة عمل **ميزات العولمة**، في قسم **البيئة**، حدد الإطار المتجانب **الفوترة الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="b0131-148">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing** tile.</span></span>
3. <span data-ttu-id="b0131-149">في صفحة **إعدادات البيئة**، في جزء الإجراء، حدد **بيئة الخدمة**، ثم حدد **معلمات المخزن الرئيسي**.</span><span class="sxs-lookup"><span data-stu-id="b0131-149">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="b0131-150">حدد **جديد** لإنشاء مرجع المخزن الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="b0131-150">Select **New** to create a key vault reference.</span></span>
5. <span data-ttu-id="b0131-151">في حقل **الاسم**، أدخل اسم مرجع المخزن الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="b0131-151">In the **Name** field, enter the name of the key vault reference.</span></span> <span data-ttu-id="b0131-152">في الحقل **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="b0131-152">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="b0131-153">في حقل **URI للمخزن الرئيسي**، قم بلصق سر المخزن الرئيسي من مخزن Azure الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="b0131-153">In the **Key Vault URI** field, paste the key vault secret from Azure Key Vault.</span></span> <span data-ttu-id="b0131-154">لمزيد من المعلومات، راجع [إنشاء حساب تخزين وKey Vault ومخزن رئيسي](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="b0131-154">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
7. <span data-ttu-id="b0131-155">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="b0131-155">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="b0131-156">إنشاء سر حساب التخزين</span><span class="sxs-lookup"><span data-stu-id="b0131-156">Create Storage account secret</span></span>

1. <span data-ttu-id="b0131-157">في صفحة **إعدادات البيئة**، في جزء الإجراء، حدد **بيئة الخدمة** > **معلمات المخزن الرئيسي**.</span><span class="sxs-lookup"><span data-stu-id="b0131-157">On the **Environment setups** page, on the Action Pane, select **Service environment** > **Key Vault parameters**.</span></span>
2. <span data-ttu-id="b0131-158">حدد **مرجع المخزن الرئيسي** وفي قسم **الشهادات**، حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="b0131-158">Select a **Key Vault reference** and in the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="b0131-159">في حقل **الاسم**، أدخل اسم سر حساب التخزين.</span><span class="sxs-lookup"><span data-stu-id="b0131-159">In the **Name** field, enter the name of the storage account secret.</span></span> <span data-ttu-id="b0131-160">لمزيد من المعلومات، راجع [إنشاء حساب تخزين وKey Vault ومخزن رئيسي](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="b0131-160">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
4. <span data-ttu-id="b0131-161">في الحقل **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="b0131-161">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="b0131-162">في حقل **النوع**، حدد **سر**.</span><span class="sxs-lookup"><span data-stu-id="b0131-162">In the **Type** field, select **Secret**.</span></span>
6. <span data-ttu-id="b0131-163">حدد **حفظ** ثم قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b0131-163">Select **Save**, and then close the page.</span></span>

## <a name="create-a-digital-certificate-secret"></a><span data-ttu-id="b0131-164">إنشاء كلمة سر لشهادة رقمية</span><span class="sxs-lookup"><span data-stu-id="b0131-164">Create a digital certificate secret</span></span>

1. <span data-ttu-id="b0131-165">في صفحة **إعدادات البيئة**، في جزء الإجراء، حدد **بيئة الخدمة**، ثم حدد **معلمات المخزن الرئيسي**.</span><span class="sxs-lookup"><span data-stu-id="b0131-165">On the **Environment setups** page, on the action Pane, select **Service environment** and then select **Key Vault parameters**.</span></span>
2. <span data-ttu-id="b0131-166">حدد **مرجع المخزن الرئيسي** ثم في قسم **الشهادات**، حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="b0131-166">Select a **Key Vault reference** and then in the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="b0131-167">في حقل **الاسم**، أدخل اسم سر الشهادة الرقمية.</span><span class="sxs-lookup"><span data-stu-id="b0131-167">In the **Name** field, enter the name of the digital certificate secret.</span></span> <span data-ttu-id="b0131-168">لمزيد من المعلومات، راجع [إنشاء حساب تخزين وKey Vault ومخزن رئيسي](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="b0131-168">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
4. <span data-ttu-id="b0131-169">في الحقل **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="b0131-169">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="b0131-170">في حقل **النوع**، حدد **الشهادة**.</span><span class="sxs-lookup"><span data-stu-id="b0131-170">In the **Type** field, select **Certificate**.</span></span>
6. <span data-ttu-id="b0131-171">حدد **حفظ** ثم قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b0131-171">Select **Save**, and then close the page.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="b0131-172">إنشاء بيئة خدمة</span><span class="sxs-lookup"><span data-stu-id="b0131-172">Create a service environment</span></span>

1. <span data-ttu-id="b0131-173">سجل دخولك إلى حساب RCS.</span><span class="sxs-lookup"><span data-stu-id="b0131-173">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="b0131-174">في مساحة عمل **ميزات العولمة**، في قسم **البيئة**، حدد الإطار المتجانب **الفوترة الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="b0131-174">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing** tile.</span></span>
3. <span data-ttu-id="b0131-175">في صفحة **إعدادات البيئة**، وفي جزء الإجراء، حدد **بيئة الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="b0131-175">On the **Environment setups** page, on the Action Pane, select **Service environment**.</span></span>
4. <span data-ttu-id="b0131-176">حدد **جديد** لإنشاء بيئة خدمة جديدة.</span><span class="sxs-lookup"><span data-stu-id="b0131-176">Select **New** to create a new service environment.</span></span>
5. <span data-ttu-id="b0131-177">في حقل **الاسم**، أدخل اسم بيئة الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="b0131-177">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="b0131-178">في الحقل **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="b0131-178">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="b0131-179">في حقل **سر رمز SAS المميز للتخزين**، حدد اسم حساب التخزين الذي يجب استخدامه لمصادقة الوصول إلى حساب التخزين.</span><span class="sxs-lookup"><span data-stu-id="b0131-179">In the **Storage SAS token secret** field, select the name of the storage account secret that must be used to authenticate access to the storage account.</span></span>
7. <span data-ttu-id="b0131-180">في قسم **المستخدمون**، حدد **إضافة** لإضافة مستخدم يسمح له بإرسال الفواتير الإلكترونية من خلال البيئة والاتصال أيضًا بحساب التخزين.</span><span class="sxs-lookup"><span data-stu-id="b0131-180">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
8. <span data-ttu-id="b0131-181">في حقل **معرف المستخدم**، ادخل الاسم المستعار للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="b0131-181">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="b0131-182">ثم، في حقل **‏‫البريد الإلكتروني**، أدخل عنوان البريد الإلكتروني للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="b0131-182">In the **Email** field, enter the user's email address.</span></span>
9. <span data-ttu-id="b0131-183">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="b0131-183">Select **Save**.</span></span>
10. <span data-ttu-id="b0131-184">إذا كانت الفواتير الخاصة ببلدك/منطقتك تتطلب سلسلة من الشهادات لتطبيق التوقيعات الرقمية، ففي جزء الإجراء، حدد **معلمات المخزن الرئيسي**، ثم حدد **تسلسل الشهادات** واتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="b0131-184">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>
    1. <span data-ttu-id="b0131-185">حدد **جديد** لإنشاء سلسلة من الشهادات.</span><span class="sxs-lookup"><span data-stu-id="b0131-185">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="b0131-186">في حقل **الاسم**، أدخل اسم تسلسل الشهادات.</span><span class="sxs-lookup"><span data-stu-id="b0131-186">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="b0131-187">في الحقل **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="b0131-187">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="b0131-188">في قسم **الشهادات**، حدد **إضافة** لإضافة شهادة إلى السلسلة.</span><span class="sxs-lookup"><span data-stu-id="b0131-188">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="b0131-189">استخدم الزر **لأعلى** أو **لأسفل** لتغيير موضع الشهادة في السلسلة.</span><span class="sxs-lookup"><span data-stu-id="b0131-189">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="b0131-190">حدد **حفظ** ثم قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b0131-190">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="b0131-191">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b0131-191">Close the page.</span></span>
11. <span data-ttu-id="b0131-192">في صفحة **بيئة الخدمة**، في جزء الإجراءات، حدد **نشر** لنشر البيئة إلى السحابة.</span><span class="sxs-lookup"><span data-stu-id="b0131-192">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="b0131-193">تغيرت القيمة في حقل **الحالة** إلى **منشور**.</span><span class="sxs-lookup"><span data-stu-id="b0131-193">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="b0131-194">إنشاء تطبيق متصل</span><span class="sxs-lookup"><span data-stu-id="b0131-194">Create a connected application</span></span>

1. <span data-ttu-id="b0131-195">في صفحة **إعدادات البيئة**، في جزء الإجراء ، حدد **التطبيقات المتصلة**.</span><span class="sxs-lookup"><span data-stu-id="b0131-195">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="b0131-196">حدد **جديد** لإنشاء تطبيق متصل.</span><span class="sxs-lookup"><span data-stu-id="b0131-196">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="b0131-197">في حقل **الاسم**، أدخل اسم التطبيق المراد الاتصال به.</span><span class="sxs-lookup"><span data-stu-id="b0131-197">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="b0131-198">في حقل **التطبيق**، أدخل عنوان URL الخاص ببيئة Finance وSupply Chain Management المراد الاتصال بها.</span><span class="sxs-lookup"><span data-stu-id="b0131-198">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="b0131-199">في حقل **المستأجر**، أدخل المستأجر الخاص ببيئة Finance وSupply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b0131-199">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="b0131-200">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="b0131-200">Select **Save**.</span></span>
6. <span data-ttu-id="b0131-201">في جزء الإجراء ، حدد **فحص اتصال** لاختبار الاتصال مع البيئة.</span><span class="sxs-lookup"><span data-stu-id="b0131-201">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="b0131-202">ثم أغلق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b0131-202">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="b0131-203">ربط التطبيقات المتصلة بالبيئات</span><span class="sxs-lookup"><span data-stu-id="b0131-203">Link connected applications to environments</span></span>

1. <span data-ttu-id="b0131-204">في صفحة **إعدادات البيئة**، حدد **جديد** لتعيين تطبيق متصل لإحدى البيئات.</span><span class="sxs-lookup"><span data-stu-id="b0131-204">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="b0131-205">في حقل **التطبيق المتصل**، حدد أحد التطبيقات المتصلة.</span><span class="sxs-lookup"><span data-stu-id="b0131-205">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="b0131-206">في حقل **بيئة الخدمة**، حدد بيئة الخدمة.</span><span class="sxs-lookup"><span data-stu-id="b0131-206">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="b0131-207">حدد **حفظ** ثم قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b0131-207">Select **Save**, and then close the page.</span></span>

## <a name="set-up-electronic-invoicing-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="b0131-208">إعداد تكامل الفوترة الإلكترونية في Finance وSupply Chain Management</span><span class="sxs-lookup"><span data-stu-id="b0131-208">Set up Electronic invoicing integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-integration-feature"></a><span data-ttu-id="b0131-209">تشغيل ميزة تكامل الفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="b0131-209">Turn on the Electronic invoicing integration feature</span></span>

1. <span data-ttu-id="b0131-210">سجل دخولك إلى مثيل Finance أو Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b0131-210">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="b0131-211">في مساحة عمل **إدارة الميزات**، ابحث عن ميزة **تكامل الفوترة الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="b0131-211">In the **Feature management** workspace, search for the **Electronic invoicing integration** feature.</span></span> <span data-ttu-id="b0131-212">إذا لم تظهر هذه الميزة على الصفحة ، فحدد **التحقق من وجود تحديثات**.</span><span class="sxs-lookup"><span data-stu-id="b0131-212">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="b0131-213">حدد الميزة، ثم حدد **تمكين الآن**.</span><span class="sxs-lookup"><span data-stu-id="b0131-213">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="b0131-214">إعداد URL نقطة نهاية الخدمة</span><span class="sxs-lookup"><span data-stu-id="b0131-214">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="b0131-215">انتقل إلى **إدارة المؤسسة \> الإعداد \> معلمات المستندات الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="b0131-215">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="b0131-216">في علامة تبويب **خدمة الإرسال**، في حقل **URL لنقطة نهاية الخدمة**، أدخل نقطة نهاية الخدمة المناسبة لمنطقة Azure الجغرافية الخاصة بك، كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="b0131-216">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="b0131-217">منطقة Azure الجغرافية لمركز البيانات</span><span class="sxs-lookup"><span data-stu-id="b0131-217">Datacenter Azure geography</span></span> | <span data-ttu-id="b0131-218">عنوان URL لنقطة نهاية الخدمة</span><span class="sxs-lookup"><span data-stu-id="b0131-218">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="b0131-219">شرق الولايات المتحدة</span><span class="sxs-lookup"><span data-stu-id="b0131-219">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="b0131-220">غرب الولايات المتحدة</span><span class="sxs-lookup"><span data-stu-id="b0131-220">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="b0131-221">شمال الاتحاد الأوروبي</span><span class="sxs-lookup"><span data-stu-id="b0131-221">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="b0131-222">غرب الاتحاد الأوروبي</span><span class="sxs-lookup"><span data-stu-id="b0131-222">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="b0131-223">في حقل **البيئة**، أدخل اسم بيئة الخدمة المنشورة في الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="b0131-223">In the **Environment** field, enter the name of the service environment published in Electronic invoicing.</span></span>
4. <span data-ttu-id="b0131-224">حدد **حفظ** ثم قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b0131-224">Select **Save**, and then close the page.</span></span>

### <a name="enable-flighting-keys"></a><span data-ttu-id="b0131-225">تمكين مفاتيح الطيران</span><span class="sxs-lookup"><span data-stu-id="b0131-225">Enable Flighting keys</span></span>

<span data-ttu-id="b0131-226">قم بتمكين مفاتيح الطيران لـ Microsoft Dynamics 365 Finance أو Microsoft Dynamics 365 Supply Chain Management الإصدار 10.0.17 أو إصدار أقدم.</span><span class="sxs-lookup"><span data-stu-id="b0131-226">Enable Flight keys for  Microsoft Dynamics 365 Finance or  Microsoft Dynamics 365 Supply Chain Management versions 10.0.17 or earlier.</span></span> 
1. <span data-ttu-id="b0131-227">قم بتنفيذ أمر SQL التالي:</span><span class="sxs-lookup"><span data-stu-id="b0131-227">Execute the following SQL command:</span></span>

    <span data-ttu-id="b0131-228">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)</span><span class="sxs-lookup"><span data-stu-id="b0131-228">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)</span></span>
    
    <span data-ttu-id="b0131-229">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)</span><span class="sxs-lookup"><span data-stu-id="b0131-229">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)</span></span>

2. <span data-ttu-id="b0131-230">تنفيذ أمر IISreset لجميع خوادم كائنات التطبيقات.</span><span class="sxs-lookup"><span data-stu-id="b0131-230">Perform an IISreset command for all AOS's.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
