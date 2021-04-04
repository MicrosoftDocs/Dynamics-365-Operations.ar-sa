---
title: بدء استخدام إدارة خدمة الوظيفة الإضافية للفوترة الإلكترونية
description: يوضح هذا الموضوع كيفية بدء استخدام الوظيفة الإضافية للفوترة الإلكترونية.
author: gionoder
manager: AnnBe
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 05b00380cec7511adad2467d3f252799a4aaee5c
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592516"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a><span data-ttu-id="c0d7b-103">بدء استخدام إدارة خدمة الوظيفة الإضافية للفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="c0d7b-103">Get started with Electronic invoicing add-on service administration</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="c0d7b-104">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="c0d7b-104">Prerequisites</span></span>

<span data-ttu-id="c0d7b-105">قبل أن تتمكن من استكمال الإجراءات في هذا الموضوع، يجب إتمام المهام المتطلبات التالية:</span><span class="sxs-lookup"><span data-stu-id="c0d7b-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="c0d7b-106">يجب أن يكون لديك حق الوصول إلى حساب Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="c0d7b-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="c0d7b-107">يجب ان يكون لديك مشروع LCS يتضمن إصدار 10.0.17 أو إصدار أحدث من Microsoft Dynamics 365 Finance وDynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-107">You must have an LCS project that includes version 10.0.17 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="c0d7b-108">بالإضافة إلى ذلك، يجب أن يتم نشر هذه التطبيقات في أحد مناطق Azure الجغرافية التالية:</span><span class="sxs-lookup"><span data-stu-id="c0d7b-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="c0d7b-109">شرق الولايات المتحدة</span><span class="sxs-lookup"><span data-stu-id="c0d7b-109">East US</span></span>
    - <span data-ttu-id="c0d7b-110">غرب الولايات المتحدة</span><span class="sxs-lookup"><span data-stu-id="c0d7b-110">West US</span></span>
    - <span data-ttu-id="c0d7b-111">شمال الاتحاد الأوروبي</span><span class="sxs-lookup"><span data-stu-id="c0d7b-111">North EU</span></span>
    - <span data-ttu-id="c0d7b-112">غرب الاتحاد الأوروبي</span><span class="sxs-lookup"><span data-stu-id="c0d7b-112">West EU</span></span>

- <span data-ttu-id="c0d7b-113">يجب أن يكون لديك حق الوصول إلى حساب Dynamics 365 Regulatory Configuration Services (RCS)</span><span class="sxs-lookup"><span data-stu-id="c0d7b-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="c0d7b-114">يجب تشغيل ميزة العولمة لحساب RCS في إدارة الميزات.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="c0d7b-115">لمزيد من المعلومات، راجع [Regulatory Configuration Services (RCS) - ميزات العولمة](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="c0d7b-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="c0d7b-116">يجب إنشاء مخزن رئيسي وحساب تخزين في Azure.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="c0d7b-117">لمزيد من المعلومات، راجع [إنشاء حساب تخزين وKey Vault ومخزن رئيسي](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="c0d7b-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a><span data-ttu-id="c0d7b-118">تثبيت الوظيفة الإضافية للخدمات المصغرة في Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="c0d7b-118">Install the add-on for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="c0d7b-119">سجل دخولك إلى حساب LCS.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="c0d7b-120">حدد تجانب **إدارة ميزة المعاينة**.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="c0d7b-121">في قسم **ميزات المعاينة العامة**، حدد **خدمة الفوترة الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="c0d7b-122">تأكد من تعيين خيار **‬‏‫ميزة المعاينه ممكنة** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>
5. <span data-ttu-id="c0d7b-123">في لوحة معلومات LCS، حدد مشروع توزيع LCS الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-123">On your LCS dashboard, select your LCS deployment project.</span></span> <span data-ttu-id="c0d7b-124">يجب أن يكون مشروع LCS قيد التشغيل.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-124">The LCS project must be running.</span></span>
7. <span data-ttu-id="c0d7b-125">على علامة التبويب **الوظائف الإضافية للبيئة**، حدد **تثبيت وظيفة إضافية جديدة**.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-125">On the **Environment add-ins** tab, select **Install a new add-in**.</span></span>
8. <span data-ttu-id="c0d7b-126">حدد **خدمات الفوترة الإلكترونية** وفي حقل **معرف تطبيق AAD**، أدخل **091c98b0-a1c9-4b02-b62c-7753395ccabe**</span><span class="sxs-lookup"><span data-stu-id="c0d7b-126">Select **e-invoicing Services** and in the **AAD application ID** field, enter **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span></span> <span data-ttu-id="c0d7b-127">هذه قيمة ثابتة.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-127">This is a fixed value.</span></span>
10. <span data-ttu-id="c0d7b-128">في الحقل **معرف مستأجر AAD**، أدخل معرف المستأجر لحساب اشتراك Azure.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-128">In the **AAD tenant ID** field, enter the tenant ID of your Azure subscription account.</span></span>
11. <span data-ttu-id="c0d7b-129">راجع البنود والشروط، ثم حدد خانة الاختيار.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-129">Review the terms and conditions, and then select the check box.</span></span>
12. <span data-ttu-id="c0d7b-130">حدد **تثبيت**.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-130">Select **Install**.</span></span>


## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="c0d7b-131">إعداد المعلمات لتكامل RCS باستخدام الوظيفة الإضافية للفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="c0d7b-131">Set up the parameters for RCS integration with the Electronic invoicing add-on</span></span>

1. <span data-ttu-id="c0d7b-132">سجل دخولك إلى حساب RCS.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-132">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="c0d7b-133">في مساحة عمل **التقارير الإلكترونية**، في قسم **الارتباطات‬ ذات الصلة**، حدد **معلمات التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-133">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="c0d7b-134">في علامة تبويب **خدمة الفوترة الإلكترونية**، في حقل **URI لنقطة نهاية الخدمة**، أدخل نقطة نهاية الخدمة المناسبة لمنطقة Azure الجغرافية الخاصة بك، كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-134">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="c0d7b-135">منطقة Azure الجغرافية لمركز البيانات</span><span class="sxs-lookup"><span data-stu-id="c0d7b-135">Datacenter Azure geography</span></span> | <span data-ttu-id="c0d7b-136">عنوان URI لنقطة نهاية الخدمة</span><span class="sxs-lookup"><span data-stu-id="c0d7b-136">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="c0d7b-137">شرق الولايات المتحدة</span><span class="sxs-lookup"><span data-stu-id="c0d7b-137">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="c0d7b-138">غرب الولايات المتحدة</span><span class="sxs-lookup"><span data-stu-id="c0d7b-138">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="c0d7b-139">شمال الاتحاد الأوروبي</span><span class="sxs-lookup"><span data-stu-id="c0d7b-139">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="c0d7b-140">غرب الاتحاد الأوروبي</span><span class="sxs-lookup"><span data-stu-id="c0d7b-140">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="c0d7b-141">تأكد من أنه تم تعيين حقل **معرف التطبيق** إلى **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-141">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="c0d7b-142">هذه القيمة هي قيمة ثابتة.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-142">This value is a fixed value.</span></span>
5. <span data-ttu-id="c0d7b-143">في الحقل **معرف بيئة LCS**، أدخل معرف حساب اشتراك LCS.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-143">In the **LCS Environment Id** field, enter the ID of your LCS subscription account.</span></span>
6. <span data-ttu-id="c0d7b-144">حدد **حفظ** ثم قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-144">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-secret"></a><span data-ttu-id="c0d7b-145">إنشاء سر المخزن الرئيسي</span><span class="sxs-lookup"><span data-stu-id="c0d7b-145">Create Key Vault secret</span></span>

1. <span data-ttu-id="c0d7b-146">سجل دخولك إلى حساب RCS.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-146">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="c0d7b-147">في مساحة عمل **ميزات العولمة**، في قسم **البيئة**، حدد الإطار المتجانب **الوظيفة الإضافية للفوترة الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-147">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing add-on** tile.</span></span>
3. <span data-ttu-id="c0d7b-148">في صفحة **إعدادات البيئة**، في جزء الإجراء، حدد **بيئة الخدمة**، ثم حدد **معلمات المخزن الرئيسي**.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-148">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="c0d7b-149">حدد **جديد** لإنشاء سر المخزن الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-149">Select **New** to create a key vault secret.</span></span>
5. <span data-ttu-id="c0d7b-150">في حقل **الاسم**، أدخل اسم سر المخزن الرئيسي</span><span class="sxs-lookup"><span data-stu-id="c0d7b-150">In the **Name** field, enter the name of the key vault secret.</span></span> <span data-ttu-id="c0d7b-151">في الحقل **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-151">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="c0d7b-152">في حقل **URI للمخزن الرئيسي** ، قم بلصق السر من المخزن الرئيسي لـ Azure.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-152">In the **Key Vault URI** field, paste the secret from Azure Key Vault.</span></span>
7. <span data-ttu-id="c0d7b-153">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-153">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="c0d7b-154">إنشاء سر حساب التخزين</span><span class="sxs-lookup"><span data-stu-id="c0d7b-154">Create Storage account secret</span></span>

1. <span data-ttu-id="c0d7b-155">انتقل إلى **إدارة النظام** > **إعداد** > **معلمات المخزن الرئيسي**، وحدد سر المخزن الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-155">Go to **System administration** > **Setup** > **Key Vault parameters**, and select a Key vault secret.</span></span>
2. <span data-ttu-id="c0d7b-156">في قسم **الشهادات**، حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-156">In the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="c0d7b-157">في حقل **الاسم**، أدخل اسم سر حساب التخزين وفي حقل **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-157">In the **Name** field, enter the name of the storage account secret and in the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="c0d7b-158">في حقل **النوع**، حدد **الشهادة**.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-158">In the **Type** field, select **Certificate**.</span></span>
5. <span data-ttu-id="c0d7b-159">حدد **حفظ** ثم قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-159">Select **Save**, and then close the page.</span></span>

## <a name="create-a-digital-certificate-secret"></a><span data-ttu-id="c0d7b-160">إنشاء كلمة سر لشهادة رقمية</span><span class="sxs-lookup"><span data-stu-id="c0d7b-160">Create a digital certificate secret</span></span>

1. <span data-ttu-id="c0d7b-161">انتقل إلى **إدارة النظام** > **إعداد** > **معلمات المخزن الرئيسي**، وحدد سر المخزن الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-161">Go to **System administration** > **Setup** > **Key Vault parameters**, and select a Key vault secret.</span></span>
2. <span data-ttu-id="c0d7b-162">في قسم **الشهادات**، حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-162">In the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="c0d7b-163">في حقل **الاسم**، أدخل اسم سر الشهادة الرقمية وفي حقل **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-163">In the **Name** field, enter the name of the digital certificate secret and in the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="c0d7b-164">في حقل **النوع**، حدد **الشهادة**.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-164">In the **Type** field, select **Certificate**.</span></span>
5. <span data-ttu-id="c0d7b-165">حدد **حفظ** ثم قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-165">Select **Save**, and then close the page.</span></span>

## <a name="create-an-electronic-invoicing-add-on-environment"></a><span data-ttu-id="c0d7b-166">إنشاء بيئة الوظيفة الإضافية للفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="c0d7b-166">Create an Electronic invoicing add-on environment</span></span>

1. <span data-ttu-id="c0d7b-167">سجل دخولك إلى حساب RCS.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-167">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="c0d7b-168">في مساحة عمل **ميزات العولمة**، في قسم **البيئة**، حدد الإطار المتجانب **الوظيفة الإضافية للفوترة الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-168">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing add-on** tile.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="c0d7b-169">إنشاء بيئة خدمة</span><span class="sxs-lookup"><span data-stu-id="c0d7b-169">Create a service environment</span></span>

1. <span data-ttu-id="c0d7b-170">في صفحة **إعدادات البيئة**، وفي جزء الإجراء، حدد **بيئة الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-170">On the **Environment setups** page, on the Action Pane, select **Service environment**.</span></span>
2. <span data-ttu-id="c0d7b-171">حدد **جديد** لإنشاء بيئة خدمة جديدة.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-171">Select **New** to create a new service environment.</span></span>
3. <span data-ttu-id="c0d7b-172">في حقل **الاسم**، أدخل اسم بيئة الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-172">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="c0d7b-173">في الحقل **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-173">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="c0d7b-174">في حقل **سر رمز SAS المميز للتخزين**، حدد اسم حساب التخزين الذي يجب استخدامه لمصادقة الوصول إلى حساب التخزين.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-174">In the **Storage SAS token secret** field, select the name of the storage account secret that must be used to authenticate access to the storage account.</span></span>
5. <span data-ttu-id="c0d7b-175">في قسم **المستخدمون**، حدد **إضافة** لإضافة مستخدم يسمح له بإرسال الفواتير الإلكترونية من خلال البيئة والاتصال أيضًا بحساب التخزين.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-175">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
6. <span data-ttu-id="c0d7b-176">في حقل **معرف المستخدم**، ادخل الاسم المستعار للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-176">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="c0d7b-177">ثم، في حقل **‏‫البريد الإلكتروني**، أدخل عنوان البريد الإلكتروني للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-177">In the **Email** field, enter the user's email address.</span></span>
7. <span data-ttu-id="c0d7b-178">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-178">Select **Save**.</span></span>
8. <span data-ttu-id="c0d7b-179">إذا كانت الفواتير الخاصة ببلدك/منطقتك تتطلب سلسلة من الشهادات لتطبيق التوقيعات الرقمية، ففي جزء الإجراء، حدد **معلمات المخزن الرئيسي**، ثم حدد **تسلسل الشهادات** واتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-179">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>

    1. <span data-ttu-id="c0d7b-180">حدد **جديد** لإنشاء سلسلة من الشهادات.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-180">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="c0d7b-181">في حقل **الاسم**، أدخل اسم تسلسل الشهادات.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-181">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="c0d7b-182">في الحقل **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-182">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="c0d7b-183">في قسم **الشهادات**، حدد **إضافة** لإضافة شهادة إلى السلسلة.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-183">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="c0d7b-184">استخدم الزر **لأعلى** أو **لأسفل** لتغيير موضع الشهادة في السلسلة.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-184">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="c0d7b-185">حدد **حفظ** ثم قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-185">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="c0d7b-186">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-186">Close the page.</span></span>
9. <span data-ttu-id="c0d7b-187">في صفحة **بيئة الخدمة**، في جزء الإجراءات، حدد **نشر** لنشر البيئة إلى السحابة.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-187">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="c0d7b-188">تغيرت القيمة في حقل **الحالة** إلى **منشور**.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-188">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="c0d7b-189">إنشاء تطبيق متصل</span><span class="sxs-lookup"><span data-stu-id="c0d7b-189">Create a connected application</span></span>

1. <span data-ttu-id="c0d7b-190">في صفحة **إعدادات البيئة**، في جزء الإجراء ، حدد **التطبيقات المتصلة**.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-190">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="c0d7b-191">حدد **جديد** لإنشاء تطبيق متصل.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-191">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="c0d7b-192">في حقل **الاسم**، أدخل اسم التطبيق المراد الاتصال به.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-192">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="c0d7b-193">في حقل **التطبيق**، أدخل عنوان URL الخاص ببيئة Finance وSupply Chain Management المراد الاتصال بها.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-193">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="c0d7b-194">في حقل **المستأجر**، أدخل المستأجر الخاص ببيئة Finance وSupply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-194">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="c0d7b-195">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-195">Select **Save**.</span></span>
6. <span data-ttu-id="c0d7b-196">في جزء الإجراء ، حدد **فحص اتصال** لاختبار الاتصال مع البيئة.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-196">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="c0d7b-197">ثم أغلق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-197">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="c0d7b-198">ربط التطبيقات المتصلة بالبيئات</span><span class="sxs-lookup"><span data-stu-id="c0d7b-198">Link connected applications to environments</span></span>

1. <span data-ttu-id="c0d7b-199">في صفحة **إعدادات البيئة**، حدد **جديد** لتعيين تطبيق متصل لإحدى البيئات.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-199">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="c0d7b-200">في حقل **التطبيق المتصل**، حدد أحد التطبيقات المتصلة.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-200">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="c0d7b-201">في حقل **بيئة الخدمة**، حدد بيئة الخدمة.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-201">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="c0d7b-202">حدد **حفظ** ثم قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-202">Select **Save**, and then close the page.</span></span>

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="c0d7b-203">إعداد الوظيفة الإضافية للفوترة الإلكترونية في Finance وSupply Chain Management</span><span class="sxs-lookup"><span data-stu-id="c0d7b-203">Set up the Electronic invoicing add-on integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="c0d7b-204">تشغيل ميزة تكامل الوظيفة الإضافية الفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="c0d7b-204">Turn on the Electronic invoicing add-on integration feature</span></span>

1. <span data-ttu-id="c0d7b-205">سجل دخولك إلى مثيل Finance أو Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-205">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="c0d7b-206">في مساحة عمل **إدارة الميزات**، ابحث عن ميزة **تكامل الوظيفة الإضافية للفوترة الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-206">In the **Feature management** workspace, search for the **Electronic invoicing add-on integration** feature.</span></span> <span data-ttu-id="c0d7b-207">إذا لم تظهر هذه الميزة على الصفحة ، فحدد **التحقق من وجود تحديثات**.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-207">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="c0d7b-208">حدد الميزة، ثم حدد **تمكين الآن**.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-208">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="c0d7b-209">إعداد URL نقطة نهاية الخدمة</span><span class="sxs-lookup"><span data-stu-id="c0d7b-209">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="c0d7b-210">انتقل إلى **إدارة المؤسسة \> الإعداد \> معلمات المستندات الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-210">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="c0d7b-211">في علامة تبويب **خدمة الإرسال**، في حقل **URL لنقطة نهاية الخدمة**، أدخل نقطة نهاية الخدمة المناسبة لمنطقة Azure الجغرافية الخاصة بك، كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-211">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="c0d7b-212">منطقة Azure الجغرافية لمركز البيانات</span><span class="sxs-lookup"><span data-stu-id="c0d7b-212">Datacenter Azure geography</span></span> | <span data-ttu-id="c0d7b-213">عنوان URL لنقطة نهاية الخدمة</span><span class="sxs-lookup"><span data-stu-id="c0d7b-213">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="c0d7b-214">شرق الولايات المتحدة</span><span class="sxs-lookup"><span data-stu-id="c0d7b-214">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="c0d7b-215">غرب الولايات المتحدة</span><span class="sxs-lookup"><span data-stu-id="c0d7b-215">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="c0d7b-216">شمال الاتحاد الأوروبي</span><span class="sxs-lookup"><span data-stu-id="c0d7b-216">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="c0d7b-217">غرب الاتحاد الأوروبي</span><span class="sxs-lookup"><span data-stu-id="c0d7b-217">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="c0d7b-218">في حقل **البيئة**، أدخل اسم بيئة الوظيفة الإضافية للفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-218">In the **Environment** field, enter the name of the Electronic invoicing add-on environment.</span></span>
4. <span data-ttu-id="c0d7b-219">حدد **حفظ** ثم قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c0d7b-219">Select **Save**, and then close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
