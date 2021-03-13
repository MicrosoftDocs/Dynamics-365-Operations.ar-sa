---
title: بدء استخدام إدارة خدمة الوظيفة الإضافية للفوترة الإلكترونية
description: يوضح هذا الموضوع كيفية بدء استخدام الوظيفة الإضافية للفوترة الإلكترونية.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
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
ms.openlocfilehash: 111ec65aa826795125d4a9ce835f72e1a0f41b7b
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104338"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a><span data-ttu-id="4a883-103">بدء استخدام إدارة خدمة الوظيفة الإضافية للفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="4a883-103">Get started with Electronic invoicing add-on service administration</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="4a883-104">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="4a883-104">Prerequisites</span></span>

<span data-ttu-id="4a883-105">قبل أن تتمكن من استكمال الإجراءات في هذا الموضوع، يجب إتمام المهام المتطلبات التالية:</span><span class="sxs-lookup"><span data-stu-id="4a883-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="4a883-106">يجب أن يكون لديك حق الوصول إلى حساب Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="4a883-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="4a883-107">يجب ان يكون لديك مشروع LCS يتضمن إصدار 10.0.13 أو إصدار أحدث من Microsoft Dynamics 365 Finance وDynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4a883-107">You must have an LCS project that includes version 10.0.13 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="4a883-108">بالإضافة إلى ذلك، يجب أن يتم نشر هذه التطبيقات في أحد مناطق Azure الجغرافية التالية:</span><span class="sxs-lookup"><span data-stu-id="4a883-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="4a883-109">شرق الولايات المتحدة</span><span class="sxs-lookup"><span data-stu-id="4a883-109">East US</span></span>
    - <span data-ttu-id="4a883-110">غرب الولايات المتحدة</span><span class="sxs-lookup"><span data-stu-id="4a883-110">West US</span></span>
    - <span data-ttu-id="4a883-111">شمال الاتحاد الأوروبي</span><span class="sxs-lookup"><span data-stu-id="4a883-111">North EU</span></span>
    - <span data-ttu-id="4a883-112">غرب الاتحاد الأوروبي</span><span class="sxs-lookup"><span data-stu-id="4a883-112">West EU</span></span>

- <span data-ttu-id="4a883-113">يجب أن يكون لديك حق الوصول إلى حساب Dynamics 365 Regulatory Configuration Services (RCS)</span><span class="sxs-lookup"><span data-stu-id="4a883-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="4a883-114">يجب تشغيل ميزة العولمة لحساب RCS في إدارة الميزات.</span><span class="sxs-lookup"><span data-stu-id="4a883-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="4a883-115">لمزيد من المعلومات، راجع [Regulatory Configuration Services (RCS) - ميزات العولمة](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="4a883-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="4a883-116">يجب إنشاء مخزن رئيسي وحساب تخزين في Azure.</span><span class="sxs-lookup"><span data-stu-id="4a883-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="4a883-117">لمزيد من المعلومات، راجع [إنشاء حساب تخزين وKey Vault ومخزن رئيسي](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="4a883-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a><span data-ttu-id="4a883-118">تثبيت الوظيفة الإضافية للخدمات المصغرة في Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="4a883-118">Install the add-on for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="4a883-119">سجل دخولك إلى حساب LCS.</span><span class="sxs-lookup"><span data-stu-id="4a883-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="4a883-120">حدد تجانب **إدارة ميزة المعاينة**.</span><span class="sxs-lookup"><span data-stu-id="4a883-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="4a883-121">في قسم **ميزات المعاينة العامة**، حدد **خدمة الفوترة الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="4a883-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="4a883-122">تأكد من تعيين خيار **‬‏‫ميزة المعاينه ممكنة** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="4a883-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>

## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="4a883-123">إعداد المعلمات لتكامل RCS باستخدام الوظيفة الإضافية للفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="4a883-123">Set up the parameters for RCS integration with the Electronic invoicing add-on</span></span>

1. <span data-ttu-id="4a883-124">سجل دخولك إلى حساب RCS.</span><span class="sxs-lookup"><span data-stu-id="4a883-124">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="4a883-125">في مساحة عمل **التقارير الإلكترونية**، في قسم **الارتباطات‬ ذات الصلة**، حدد **معلمات التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="4a883-125">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="4a883-126">في علامة تبويب **خدمة الفوترة الإلكترونية**، في حقل **URI لنقطة نهاية الخدمة**، أدخل نقطة نهاية الخدمة المناسبة لمنطقة Azure الجغرافية الخاصة بك، كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="4a883-126">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="4a883-127">منطقة Azure الجغرافية لمركز البيانات</span><span class="sxs-lookup"><span data-stu-id="4a883-127">Datacenter Azure geography</span></span> | <span data-ttu-id="4a883-128">عنوان URI لنقطة نهاية الخدمة</span><span class="sxs-lookup"><span data-stu-id="4a883-128">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="4a883-129">شرق الولايات المتحدة</span><span class="sxs-lookup"><span data-stu-id="4a883-129">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="4a883-130">غرب الولايات المتحدة</span><span class="sxs-lookup"><span data-stu-id="4a883-130">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="4a883-131">شمال الاتحاد الأوروبي</span><span class="sxs-lookup"><span data-stu-id="4a883-131">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="4a883-132">غرب الاتحاد الأوروبي</span><span class="sxs-lookup"><span data-stu-id="4a883-132">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="4a883-133">تأكد من أنه تم تعيين حقل **معرف التطبيق** إلى **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="4a883-133">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="4a883-134">هذه القيمة هي قيمة ثابتة.</span><span class="sxs-lookup"><span data-stu-id="4a883-134">This value is a fixed value.</span></span>
5. <span data-ttu-id="4a883-135">في الحقل **معرف بيئة LCS**، أدخل معرف حساب اشتراك LCS.</span><span class="sxs-lookup"><span data-stu-id="4a883-135">In the **LCS Environment Id** field, enter the ID of your LCS subscription account.</span></span>
6. <span data-ttu-id="4a883-136">حدد **حفظ** ثم قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="4a883-136">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-secret"></a><span data-ttu-id="4a883-137">إنشاء سر المخزن الرئيسي</span><span class="sxs-lookup"><span data-stu-id="4a883-137">Create Key Vault secret</span></span>

1. <span data-ttu-id="4a883-138">سجل دخولك إلى حساب RCS.</span><span class="sxs-lookup"><span data-stu-id="4a883-138">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="4a883-139">في مساحة العمل **ميزة العولمة**، في قسم **البيئة**، حدد الإطار المتجانب **الفوترة الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="4a883-139">In the **Globalization feature** workspace, in the **Environment** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="4a883-140">في صفحة **إعدادات البيئة**، في جزء الإجراء، حدد **بيئة الخدمة**، ثم حدد **معلمات المخزن الرئيسي**.</span><span class="sxs-lookup"><span data-stu-id="4a883-140">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="4a883-141">حدد **جديد** لإنشاء سر المخزن الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="4a883-141">Select **New** to create a key vault secret.</span></span>
5. <span data-ttu-id="4a883-142">في حقل **الاسم**، أدخل اسم سر المخزن الرئيسي</span><span class="sxs-lookup"><span data-stu-id="4a883-142">In the **Name** field, enter the name of the key vault secret.</span></span> <span data-ttu-id="4a883-143">في الحقل **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="4a883-143">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="4a883-144">في حقل **URI للمخزن الرئيسي** ، قم بلصق السر من المخزن الرئيسي لـ Azure.</span><span class="sxs-lookup"><span data-stu-id="4a883-144">In the **Key Vault URI** field, paste the secret from Azure Key Vault.</span></span>
7. <span data-ttu-id="4a883-145">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="4a883-145">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="4a883-146">إنشاء سر حساب التخزين</span><span class="sxs-lookup"><span data-stu-id="4a883-146">Create Storage account secret</span></span>

1. <span data-ttu-id="4a883-147">في صفحة **معلمات المخزن الرئيسي**، في قسم **الشهادات**، حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="4a883-147">On **Key vault parameters** page, in the **Certificates** section, select **Add**.</span></span>
2. <span data-ttu-id="4a883-148">في حقل **الاسم**، أدخل نفس سر حساب التخزين.</span><span class="sxs-lookup"><span data-stu-id="4a883-148">In the **Name** field, enter the same of the storage account secret.</span></span> <span data-ttu-id="4a883-149">في الحقل **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="4a883-149">In the **Description** field, enter a description.</span></span>
3. <span data-ttu-id="4a883-150">في حقل **النوع**، حدد **الشهادة**.</span><span class="sxs-lookup"><span data-stu-id="4a883-150">In the **Type** field, select **Certificate**.</span></span>
4. <span data-ttu-id="4a883-151">حدد **حفظ** ثم قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="4a883-151">Select **Save**, and then close the page.</span></span>

## <a name="create-an-electronic-invoicing-add-on-environment"></a><span data-ttu-id="4a883-152">إنشاء بيئة الوظيفة الإضافية للفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="4a883-152">Create an Electronic invoicing add-on environment</span></span>

1. <span data-ttu-id="4a883-153">سجل دخولك إلى حساب RCS.</span><span class="sxs-lookup"><span data-stu-id="4a883-153">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="4a883-154">في مساحة العمل **ميزة العولمة**، في قسم **البيئة**، حدد الإطار المتجانب **الفوترة الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="4a883-154">In the **Globalization feature** workspace, in the **Environment** section, select the **e-Invoicing** tile.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="4a883-155">إنشاء بيئة خدمة</span><span class="sxs-lookup"><span data-stu-id="4a883-155">Create a service environment</span></span>

1. <span data-ttu-id="4a883-156">في صفحة **إعدادات البيئة**، في جزء الإجراء ، حدد **بيئة الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="4a883-156">On the **Environment setups** page, on the action Pane, select **Service environment**.</span></span>
2. <span data-ttu-id="4a883-157">حدد **جديد** لإنشاء بيئة خدمة جديدة.</span><span class="sxs-lookup"><span data-stu-id="4a883-157">Select **New** to create a new service environment.</span></span>
3. <span data-ttu-id="4a883-158">في حقل **الاسم**، أدخل اسم بيئة الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="4a883-158">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="4a883-159">في الحقل **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="4a883-159">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="4a883-160">في حقل **سر الرمز SAS المميز للتخزين**، حدد اسم الشهادة التي يجب استخدامها لمصادقm الوصول إلى حساب التخزين.</span><span class="sxs-lookup"><span data-stu-id="4a883-160">In the **Storage SAS token secret** field, select the name of the certificate that must be used to authenticate access to the storage account.</span></span>
5. <span data-ttu-id="4a883-161">في قسم **المستخدمون**، حدد **إضافة** لإضافة مستخدم يسمح له بإرسال الفواتير الإلكترونية من خلال البيئة والاتصال أيضًا بحساب التخزين.</span><span class="sxs-lookup"><span data-stu-id="4a883-161">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
6. <span data-ttu-id="4a883-162">في حقل **معرف المستخدم**، ادخل الاسم المستعار للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="4a883-162">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="4a883-163">ثم، في حقل **‏‫البريد الإلكتروني**، أدخل عنوان البريد الإلكتروني للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="4a883-163">In the **Email** field, enter the user's email address.</span></span>
7. <span data-ttu-id="4a883-164">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="4a883-164">Select **Save**.</span></span>
8. <span data-ttu-id="4a883-165">إذا كانت الفواتير الخاصة ببلدك/منطقتك تتطلب سلسلة من الشهادات لتطبيق التوقيعات الرقمية، ففي جزء الإجراء، حدد **معلمات المخزن الرئيسي**، ثم حدد **تسلسل الشهادات** واتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="4a883-165">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>

    1. <span data-ttu-id="4a883-166">حدد **جديد** لإنشاء سلسلة من الشهادات.</span><span class="sxs-lookup"><span data-stu-id="4a883-166">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="4a883-167">في حقل **الاسم**، أدخل اسم تسلسل الشهادات.</span><span class="sxs-lookup"><span data-stu-id="4a883-167">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="4a883-168">في الحقل **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="4a883-168">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="4a883-169">في قسم **الشهادات**، حدد **إضافة** لإضافة شهادة إلى السلسلة.</span><span class="sxs-lookup"><span data-stu-id="4a883-169">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="4a883-170">استخدم الزر **لأعلى** أو **لأسفل** لتغيير موضع الشهادة في السلسلة.</span><span class="sxs-lookup"><span data-stu-id="4a883-170">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="4a883-171">حدد **حفظ** ثم قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="4a883-171">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="4a883-172">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="4a883-172">Close the page.</span></span>
9. <span data-ttu-id="4a883-173">في صفحة **بيئة الخدمة**، في جزء الإجراءات، حدد **نشر** لنشر البيئة إلى السحابة.</span><span class="sxs-lookup"><span data-stu-id="4a883-173">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="4a883-174">تغيرت القيمة في حقل **الحالة** إلى **منشور**.</span><span class="sxs-lookup"><span data-stu-id="4a883-174">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="4a883-175">إنشاء تطبيق متصل</span><span class="sxs-lookup"><span data-stu-id="4a883-175">Create a connected application</span></span>

1. <span data-ttu-id="4a883-176">في صفحة **إعدادات البيئة**، في جزء الإجراء ، حدد **التطبيقات المتصلة**.</span><span class="sxs-lookup"><span data-stu-id="4a883-176">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="4a883-177">حدد **جديد** لإنشاء تطبيق متصل.</span><span class="sxs-lookup"><span data-stu-id="4a883-177">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="4a883-178">في حقل **الاسم**، أدخل اسم التطبيق المراد الاتصال به.</span><span class="sxs-lookup"><span data-stu-id="4a883-178">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="4a883-179">في حقل **التطبيق**، أدخل عنوان URL الخاص ببيئة Finance وSupply Chain Management المراد الاتصال بها.</span><span class="sxs-lookup"><span data-stu-id="4a883-179">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="4a883-180">في حقل **المستأجر**، أدخل المستأجر الخاص ببيئة Finance وSupply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4a883-180">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="4a883-181">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="4a883-181">Select **Save**.</span></span>
6. <span data-ttu-id="4a883-182">في جزء الإجراء ، حدد **فحص اتصال** لاختبار الاتصال مع البيئة.</span><span class="sxs-lookup"><span data-stu-id="4a883-182">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="4a883-183">ثم أغلق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="4a883-183">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="4a883-184">ربط التطبيقات المتصلة بالبيئات</span><span class="sxs-lookup"><span data-stu-id="4a883-184">Link connected applications to environments</span></span>

1. <span data-ttu-id="4a883-185">في صفحة **إعدادات البيئة**، حدد **جديد** لتعيين تطبيق متصل لإحدى البيئات.</span><span class="sxs-lookup"><span data-stu-id="4a883-185">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="4a883-186">في حقل **التطبيق المتصل**، حدد أحد التطبيقات المتصلة.</span><span class="sxs-lookup"><span data-stu-id="4a883-186">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="4a883-187">في حقل **بيئة الخدمة**، حدد بيئة الخدمة.</span><span class="sxs-lookup"><span data-stu-id="4a883-187">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="4a883-188">حدد **حفظ** ثم قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="4a883-188">Select **Save**, and then close the page.</span></span>

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="4a883-189">إعداد الوظيفة الإضافية للفوترة الإلكترونية في Finance وSupply Chain Management</span><span class="sxs-lookup"><span data-stu-id="4a883-189">Set up the Electronic invoicing add-on integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="4a883-190">تشغيل ميزة تكامل الوظيفة الإضافية الفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="4a883-190">Turn on the Electronic invoicing add-on integration feature</span></span>

1. <span data-ttu-id="4a883-191">سجل دخولك إلى مثيل Finance أو Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4a883-191">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="4a883-192">في مساحة عمل **إدارة الميزات**، ابحث عن ميزة **تكامل الوظيفة الإضافية للفوترة الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="4a883-192">In the **Feature management** workspace, search for the **Electronic invoicing add-on integration** feature.</span></span> <span data-ttu-id="4a883-193">إذا لم تظهر هذه الميزة على الصفحة ، فحدد **التحقق من وجود تحديثات**.</span><span class="sxs-lookup"><span data-stu-id="4a883-193">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="4a883-194">حدد الميزة، ثم حدد **تمكين الآن**.</span><span class="sxs-lookup"><span data-stu-id="4a883-194">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="4a883-195">إعداد URL نقطة نهاية الخدمة</span><span class="sxs-lookup"><span data-stu-id="4a883-195">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="4a883-196">انتقل إلى **إدارة المؤسسة \> الإعداد \> معلمات المستندات الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="4a883-196">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="4a883-197">في علامة تبويب **خدمة الإرسال**، في حقل **URL لنقطة نهاية الخدمة**، أدخل نقطة نهاية الخدمة المناسبة لمنطقة Azure الجغرافية الخاصة بك، كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="4a883-197">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="4a883-198">منطقة Azure الجغرافية لمركز البيانات</span><span class="sxs-lookup"><span data-stu-id="4a883-198">Datacenter Azure geography</span></span> | <span data-ttu-id="4a883-199">عنوان URL لنقطة نهاية الخدمة</span><span class="sxs-lookup"><span data-stu-id="4a883-199">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="4a883-200">شرق الولايات المتحدة</span><span class="sxs-lookup"><span data-stu-id="4a883-200">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="4a883-201">غرب الولايات المتحدة</span><span class="sxs-lookup"><span data-stu-id="4a883-201">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="4a883-202">شمال الاتحاد الأوروبي</span><span class="sxs-lookup"><span data-stu-id="4a883-202">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="4a883-203">غرب الاتحاد الأوروبي</span><span class="sxs-lookup"><span data-stu-id="4a883-203">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="4a883-204">في حقل **البيئة**، أدخل اسم بيئة الوظيفة الإضافية للفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="4a883-204">In the **Environment** field, enter the name of the Electronic invoicing add-on environment.</span></span>
4. <span data-ttu-id="4a883-205">حدد **حفظ** ثم قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="4a883-205">Select **Save**, and then close the page.</span></span>
