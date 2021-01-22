---
title: إعداد موارد Azure لذكاء IoT
description: يشرح هذا الموضوع كيفية إنشاء وتكوين موارد Microsoft Azure التي تتطلبها لذكاء IoT.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1277d2ab8bb1f2925874f7469250e164f6bde62d
ms.sourcegitcommit: 49f3011b8a6d8cdd038e153d8cb3cf773be25ae4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4014902"
---
# <a name="set-up-azure-resources-for-iot-intelligence"></a><span data-ttu-id="45002-103">إعداد موارد Azure لذكاء IoT</span><span class="sxs-lookup"><span data-stu-id="45002-103">Set up Azure resources for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="45002-104">يشرح هذا الموضوع كيفية إنشاء وتكوين موارد Microsoft Azure التي تتطلبها لذكاء IoT.</span><span class="sxs-lookup"><span data-stu-id="45002-104">This topic explains how to create and configure the Microsoft Azure resources that you require for IoT Intelligence.</span></span>

## <a name="create-azure-resources"></a><span data-ttu-id="45002-105">إنشاء موارد Azure</span><span class="sxs-lookup"><span data-stu-id="45002-105">Create Azure resources</span></span>

<span data-ttu-id="45002-106">اتبع هذه الخطوات لإنشاء مركز IoT وذاكرة تخزين Redis مؤقتة والمخزن الرئيسي الذي يمكن الوصول إليه من خلال Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="45002-106">Follow these steps to create an IoT hub, a Redis cache, and a key vault that can be accessed by Microsoft Dynamics 365 Supply Chain Management.</span></span>

### <a name="verify-that-the-microsoft-dynamics-erp-microservices-first-party-app-id-is-in-your-tenant"></a><span data-ttu-id="45002-107">التحقق من أن معرف تطبيق الطرف الأول لـ Microsoft Dynamics ERP Microservices موجود في المستأجر الخاص بك</span><span class="sxs-lookup"><span data-stu-id="45002-107">Verify that the Microsoft Dynamics ERP Microservices first-party app ID is in your tenant</span></span>

<span data-ttu-id="45002-108">للتحقق من وجود معرف التطبيق لتطبيق الطرف الأول لـ Microsoft Dynamics ERP Microservices في المستأجر الخاص بك، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="45002-108">To verify that the app ID for the Microsoft Dynamics ERP Microservices first-party app is in your tenant, follow these steps.</span></span>

1. <span data-ttu-id="45002-109">سجل الدخول إلى مدخل Azure على العنوان <https://portal.azure.com>.</span><span class="sxs-lookup"><span data-stu-id="45002-109">Sign in to the Azure portal at <https://portal.azure.com>.</span></span>
2. <span data-ttu-id="45002-110">الانتقال إلى **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="45002-110">Go to **Azure Active Directory**.</span></span>
3. <span data-ttu-id="45002-111">انتقل إلى **تطبيقات Enterprise**.</span><span class="sxs-lookup"><span data-stu-id="45002-111">Go to **Enterprise applications**.</span></span>
4. <span data-ttu-id="45002-112">في حقل **نوع التطبيق** ، حدد **تطبيقات Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="45002-112">In the **Application type** field, select **Microsoft applications**.</span></span>
5. <span data-ttu-id="45002-113">في حقل بحث، أدخل **Microsoft Dynamics ERP Microservices**.</span><span class="sxs-lookup"><span data-stu-id="45002-113">In the search field, enter **Microsoft Dynamics ERP Microservices**.</span></span>
6. <span data-ttu-id="45002-114">تحقق من أن **Microsoft Dynamics ERP Microservices** موجودة في القائمة.</span><span class="sxs-lookup"><span data-stu-id="45002-114">Verify that **Microsoft Dynamics ERP Microservices** is in the list.</span></span> <span data-ttu-id="45002-115">التطبيقات الأخرى لها أسماء مشابهة.</span><span class="sxs-lookup"><span data-stu-id="45002-115">Other applications have similar names.</span></span> <span data-ttu-id="45002-116">لذلك، تأكد من العثور على التطبيق الصحيح.</span><span class="sxs-lookup"><span data-stu-id="45002-116">Therefore, make sure that you find the correct application.</span></span> <span data-ttu-id="45002-117">معرف التطبيق هو **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="45002-117">The app ID is **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

    <span data-ttu-id="45002-118">إذا لم يكن التطبيق موجودًا في القائمة، فيجب عليك إضافته إلى المستأجر الخاص بك:</span><span class="sxs-lookup"><span data-stu-id="45002-118">If the application isn't in the list, you must add it to your tenant:</span></span>

    1. <span data-ttu-id="45002-119">في مدخل Azure، وفي شريط الأدوات، حدد الزر لفتح Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="45002-119">In the Azure portal, on the toolbar, select the button to open Azure Cloud Shell.</span></span>
    2. <span data-ttu-id="45002-120">قم بتشغيل الأمر **Install-Module AzureAD**.</span><span class="sxs-lookup"><span data-stu-id="45002-120">Run the command **Install-Module AzureAD**.</span></span> <span data-ttu-id="45002-121">أدخل **Y** لتثبيت الوحدة النمطية.</span><span class="sxs-lookup"><span data-stu-id="45002-121">Enter **Y** to install the module.</span></span>
    3. <span data-ttu-id="45002-122">قم بتشغيل الأمر **Get-InstalledModule -Name "AzureAD"** للتحقق من أنه تم تثبيت الوحدة النمطية.</span><span class="sxs-lookup"><span data-stu-id="45002-122">Run the command **Get-InstalledModule -Name "AzureAD"** to verify that the module is installed.</span></span>
    4. <span data-ttu-id="45002-123">قم بتشغيل الأمر **Connect-AzureAD -Confirm** لتشغيل المصادقة.</span><span class="sxs-lookup"><span data-stu-id="45002-123">Run the command **Connect-AzureAD -Confirm** to run the authentication.</span></span>
    5. <span data-ttu-id="45002-124">قم بتشغيل الأمر **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="45002-124">Run the command **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

    <span data-ttu-id="45002-125">يمكنك الآن تكرار الخطوات من 1 إلى 6 للتحقق من أن معرف التطبيق موجود في المستأجر الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="45002-125">You can now repeat steps 1 through 6 to verify that the app ID is in your tenant.</span></span>

### <a name="create-a-key-vault-resource"></a><span data-ttu-id="45002-126">إنشاء مورد مخزن رئيسي</span><span class="sxs-lookup"><span data-stu-id="45002-126">Create a key vault resource</span></span>

<span data-ttu-id="45002-127">لإنشاء مورد مخزن رئيسي اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="45002-127">To create a key vault resource, follow these steps.</span></span>

1. <span data-ttu-id="45002-128">في مدخل Azure، قم بإنشاء مجموعة موارد أو انتقل إليها.</span><span class="sxs-lookup"><span data-stu-id="45002-128">In the Azure portal, create or go to a resource group.</span></span>
2. <span data-ttu-id="45002-129">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="45002-129">Select **Add**.</span></span>
3. <span data-ttu-id="45002-130">في صفحة **جديد** ، في الحقل بحث، أدخل **المخزن الرئيسي**.</span><span class="sxs-lookup"><span data-stu-id="45002-130">On the **New** page, in the search field, enter **Key vault**.</span></span> <span data-ttu-id="45002-131">ثم حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="45002-131">Then select **Create**.</span></span>
4. <span data-ttu-id="45002-132">في صفحة **إنشاء مخزن رئيسي** ، في حقل **اسم المخزن الرئيسي** ، ادخل اسمًا.</span><span class="sxs-lookup"><span data-stu-id="45002-132">On the **Create key vault** page, in the **Key vault name** field, enter a name.</span></span>
5. <span data-ttu-id="45002-133">راجع القيم الافتراضية، ثم حدد **مراجعة + إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="45002-133">Review the default values, and then select **Review + create**.</span></span>
6. <span data-ttu-id="45002-134">حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="45002-134">Select **Create**.</span></span>

<span data-ttu-id="45002-135">يتم إنشاء المخزن الرئيسي في الخلفية.</span><span class="sxs-lookup"><span data-stu-id="45002-135">The key vault is created in the background.</span></span>

### <a name="create-an-iot-hub-resource"></a><span data-ttu-id="45002-136">إنشاء مورد لمركز IoT</span><span class="sxs-lookup"><span data-stu-id="45002-136">Create an IoT hub resource</span></span>

<span data-ttu-id="45002-137">لإنشاء مورد لمركز IoT اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="45002-137">To create an IoT hub resource, follow these steps.</span></span>

1. <span data-ttu-id="45002-138">قم بإنشاء مجموعة موارد أو اذهب إليها.</span><span class="sxs-lookup"><span data-stu-id="45002-138">Create or go to a resource group.</span></span>
2. <span data-ttu-id="45002-139">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="45002-139">Select **Add**.</span></span>
3. <span data-ttu-id="45002-140">في صفحة **جديد** ، في الحقل بحث، أدخل **مركز IoT**.</span><span class="sxs-lookup"><span data-stu-id="45002-140">On the **New** page, in the search field, enter **Iot Hub**.</span></span> <span data-ttu-id="45002-141">ثم حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="45002-141">Then select **Create**.</span></span>
4. <span data-ttu-id="45002-142">ثم في حقل **اسم مركز IoT** ، أدخل اسمًا.</span><span class="sxs-lookup"><span data-stu-id="45002-142">In the **IoT hub name** field, enter a name.</span></span>
5. <span data-ttu-id="45002-143">راجع القيم الافتراضية، ثم حدد **مراجعة + إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="45002-143">Review the default values, and then select **Review + create**.</span></span>
6. <span data-ttu-id="45002-144">حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="45002-144">Select **Create**.</span></span>

<span data-ttu-id="45002-145">يتم إنشاء مركز IoT في الخلفية.</span><span class="sxs-lookup"><span data-stu-id="45002-145">The IoT hub is created in the background.</span></span>

> [!NOTE]
> <span data-ttu-id="45002-146">نوصي بأن تقوم بإنشاء مورد لمركز IoT واحد فقط لكل بيئة.</span><span class="sxs-lookup"><span data-stu-id="45002-146">We recommend that you create only one IoT hub resource per environment.</span></span>

### <a name="create-a-redis-cache-resource"></a><span data-ttu-id="45002-147">إنشاء مورد ذاكرة تخزين Redis مؤقتة</span><span class="sxs-lookup"><span data-stu-id="45002-147">Create a Redis cache resource</span></span>

<span data-ttu-id="45002-148">لإنشاء مورد ذاكرة تخزين Redis مؤقتة اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="45002-148">To create a Redis cache resource, follow these steps.</span></span>

1. <span data-ttu-id="45002-149">قم بإنشاء مجموعة موارد أو اذهب إليها.</span><span class="sxs-lookup"><span data-stu-id="45002-149">Create or go to a resource group.</span></span>
2. <span data-ttu-id="45002-150">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="45002-150">Select **Add**.</span></span>
3. <span data-ttu-id="45002-151">في صفحة **جديد** ، في الحقل بحث، أدخل **ذاكرة تخزين Azure المؤقتة لـ Redis**.</span><span class="sxs-lookup"><span data-stu-id="45002-151">On the **New** page, in the search field, enter **Azure Cache for Redis**.</span></span> <span data-ttu-id="45002-152">ثم حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="45002-152">Then select **Create**.</span></span>
4. <span data-ttu-id="45002-153">في حقل **اسم DNS** ، أدخل اسمًا.</span><span class="sxs-lookup"><span data-stu-id="45002-153">In the **DNS name** field, enter a name.</span></span>
5. <span data-ttu-id="45002-154">راجع القيم الافتراضية، ثم حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="45002-154">Review the default values, and then select **Create**.</span></span>

<span data-ttu-id="45002-155">يتم إنشاء ذاكرة تخزين Redis المؤقتة في الخلفية.</span><span class="sxs-lookup"><span data-stu-id="45002-155">The Redis cache is created in the background.</span></span>

> [!NOTE]
> <span data-ttu-id="45002-156">نوصي بأن تقوم بإنشاء ذاكرة تخزين Redis مؤقتة واحدة فقط لكل بيئة.</span><span class="sxs-lookup"><span data-stu-id="45002-156">We recommend that you create only one Redis cache per environment.</span></span>

<span data-ttu-id="45002-157">تم إنشاء كافة الموارد الآن.</span><span class="sxs-lookup"><span data-stu-id="45002-157">All the resources have now been created.</span></span>

## <a name="configure-the-azure-resources"></a><span data-ttu-id="45002-158">تكوين موارد Azure</span><span class="sxs-lookup"><span data-stu-id="45002-158">Configure the Azure resources</span></span>

### <a name="configure-the-iot-hub"></a><span data-ttu-id="45002-159">تكوين مركز IoT</span><span class="sxs-lookup"><span data-stu-id="45002-159">Configure the IoT hub</span></span>

<span data-ttu-id="45002-160">لتكوين مركز IoT، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="45002-160">To configure the IoT hub, follow these steps.</span></span>

1. <span data-ttu-id="45002-161">في الموارد الخاصة بك، حدد مورد مركز IoT.</span><span class="sxs-lookup"><span data-stu-id="45002-161">In your resources, select the IoT hub resource.</span></span>
2. <span data-ttu-id="45002-162">في جزء التنقل الأيسر، حدد **نقاط النهاية المضمنة**.</span><span class="sxs-lookup"><span data-stu-id="45002-162">In the left navigation pane, select **Built-in endpoints**.</span></span>
3. <span data-ttu-id="45002-163">ضمن **مجموعات العملاء** ، قم بلصق مجموعات العملاء التالية.</span><span class="sxs-lookup"><span data-stu-id="45002-163">Under **Consumer groups** , paste the following consumer groups.</span></span> <span data-ttu-id="45002-164">وتتوافق مجموعات العملاء هذه مع السيناريوهات الجاهزة.</span><span class="sxs-lookup"><span data-stu-id="45002-164">These consumer groups correspond to the out-of-box scenarios.</span></span>

    + <span data-ttu-id="45002-165">microsoft.dynamics.iotintelligence-1</span><span class="sxs-lookup"><span data-stu-id="45002-165">microsoft.dynamics.iotintelligence-1</span></span>
    + <span data-ttu-id="45002-166">microsoft.dynamics.iotintelligence-2</span><span class="sxs-lookup"><span data-stu-id="45002-166">microsoft.dynamics.iotintelligence-2</span></span>
    + <span data-ttu-id="45002-167">microsoft.dynamics.iotintelligence-3</span><span class="sxs-lookup"><span data-stu-id="45002-167">microsoft.dynamics.iotintelligence-3</span></span>

### <a name="configure-the-key-vault"></a><span data-ttu-id="45002-168">تكوين المخزن الرئيسي</span><span class="sxs-lookup"><span data-stu-id="45002-168">Configure the key vault</span></span>

<span data-ttu-id="45002-169">لتكوين المخزن الرئيسي، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="45002-169">To configure the key vault, follow these steps.</span></span>

1. <span data-ttu-id="45002-170">في الموارد الخاصة بك، حدد مورد المخزن الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="45002-170">In your resources, select the key vault resource.</span></span>
2. <span data-ttu-id="45002-171">في جزء التنقل الأيسر، حدد **نُهج الوصول**.</span><span class="sxs-lookup"><span data-stu-id="45002-171">In the left navigation pane, select **Access policies**.</span></span>
3. <span data-ttu-id="45002-172">حدد **إضافة نهج وصول**.</span><span class="sxs-lookup"><span data-stu-id="45002-172">Select **Add an access policy**.</span></span>
4. <span data-ttu-id="45002-173">في صحفة **إضافة نهج وصول** ، في حقل **أذونات السر** ، حدد **حصول عليه** و **قائمة**.</span><span class="sxs-lookup"><span data-stu-id="45002-173">On the **Add access policy** page, in the **Secret permissions** field, select **Get** and **List**.</span></span>
5. <span data-ttu-id="45002-174">انقر فوق **تحديد الرئيسي**.</span><span class="sxs-lookup"><span data-stu-id="45002-174">Click in the **Select principal**.</span></span>
6. <span data-ttu-id="45002-175">في مربع الحوار **الرئيسي** ، ابحث عن **Microsoft Dynamics ERP Microservices** وحدده.</span><span class="sxs-lookup"><span data-stu-id="45002-175">In the **Principal** dialog box, search for and select **Microsoft Dynamics ERP Microservices**.</span></span> <span data-ttu-id="45002-176">ثم حدد **تحديد**.</span><span class="sxs-lookup"><span data-stu-id="45002-176">Then select **Select**.</span></span>
7. <span data-ttu-id="45002-177">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="45002-177">Select **Add**.</span></span>
8. <span data-ttu-id="45002-178">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="45002-178">Select **Save**.</span></span>

<span data-ttu-id="45002-179">يمكن للتطبيق الآن الوصول إلى الأسرار في المخزن الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="45002-179">The app now has access to the secrets in the key vault.</span></span>

### <a name="save-the-iot-hub-connection-string-secret"></a><span data-ttu-id="45002-180">حفظ السر الخاص بسلسلة اتصال مركز IoT</span><span class="sxs-lookup"><span data-stu-id="45002-180">Save the IoT hub connection string secret</span></span>

<span data-ttu-id="45002-181">لحفظ السر الخاص بسلسلة اتصال مركز IoT، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="45002-181">To save the secret for the IoT hub connection string, follow these steps.</span></span>

1. <span data-ttu-id="45002-182">في الموارد الخاصة بك، حدد مورد مركز IoT.</span><span class="sxs-lookup"><span data-stu-id="45002-182">In your resources, select the IoT hub resource.</span></span>
2. <span data-ttu-id="45002-183">في جزء التنقل الأيسر، حدد **نقاط النهاية المضمنة**.</span><span class="sxs-lookup"><span data-stu-id="45002-183">In the left navigation pane, select **Built-in endpoints**.</span></span>
3. <span data-ttu-id="45002-184">انسخ القيمة في حقل **نقطه نهاية متوافقة مع مركز الأحداث**.</span><span class="sxs-lookup"><span data-stu-id="45002-184">Copy the value in the **Event Hub-compatible endpoint** field.</span></span>
4. <span data-ttu-id="45002-185">انتقل إلى مورد المخزن الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="45002-185">Go to the key vault resource.</span></span>
5. <span data-ttu-id="45002-186">في جزء التنقل الأيسر، حدد **الأسرار**.</span><span class="sxs-lookup"><span data-stu-id="45002-186">In the left navigation pane, select **Secrets**.</span></span>
6. <span data-ttu-id="45002-187">حدد **إنشاء/استيراد**.</span><span class="sxs-lookup"><span data-stu-id="45002-187">Select **Generate/Import**.</span></span>
7. <span data-ttu-id="45002-188">في حقل **الاسم** ، أدخل اسمًا.</span><span class="sxs-lookup"><span data-stu-id="45002-188">In the **Name** field, enter a name.</span></span>
8. <span data-ttu-id="45002-189">في حقل **القيمة** ، ألصق قيمة نقطة النهاية التي قمت بنسخها سابقا.</span><span class="sxs-lookup"><span data-stu-id="45002-189">In the **Value** field, paste the endpoint value that you copied earlier.</span></span>
9. <span data-ttu-id="45002-190">حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="45002-190">Select **Create**.</span></span>

### <a name="save-the-redis-cache-connection-string-secret"></a><span data-ttu-id="45002-191">حفظ السر الخاص بسلسلة اتصال ذاكرة تخزين Redis المؤقتة</span><span class="sxs-lookup"><span data-stu-id="45002-191">Save the Redis cache connection string secret</span></span>

<span data-ttu-id="45002-192">لحفظ السر الخاص بسلسلة اتصال ذاكرة تخزين Redis المؤقتة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="45002-192">To save the secret for the Redis cache connection string, follow these steps.</span></span>

1. <span data-ttu-id="45002-193">في الموارد الخاصة بك، حدد مورد ذاكرة تخزين Redis المؤقتة.</span><span class="sxs-lookup"><span data-stu-id="45002-193">In your resources, select the Redis cache resource.</span></span>
2. <span data-ttu-id="45002-194">حدد **مفاتيح الوصول**.</span><span class="sxs-lookup"><span data-stu-id="45002-194">Select **Access keys**.</span></span>
3. <span data-ttu-id="45002-195">انسخ القيمة في حقل **سلسلة الاتصال الأساسية**.</span><span class="sxs-lookup"><span data-stu-id="45002-195">Copy the value in the **Primary connection string** field.</span></span>
4. <span data-ttu-id="45002-196">انتقل إلى مورد المخزن الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="45002-196">Go to the key vault resource.</span></span>
5. <span data-ttu-id="45002-197">في جزء التنقل الأيسر، حدد **الأسرار**.</span><span class="sxs-lookup"><span data-stu-id="45002-197">In the left navigation pane, select **Secrets**.</span></span>
6. <span data-ttu-id="45002-198">حدد **إنشاء/استيراد**.</span><span class="sxs-lookup"><span data-stu-id="45002-198">Select **Generate/Import**.</span></span>
7. <span data-ttu-id="45002-199">في حقل **الاسم** ، أدخل اسمًا.</span><span class="sxs-lookup"><span data-stu-id="45002-199">In the **Name** field, enter a name.</span></span>
8. <span data-ttu-id="45002-200">في حقل **القيمة** ، ألصق سلسلة الاتصال التي قمت بنسخها سابقًا.</span><span class="sxs-lookup"><span data-stu-id="45002-200">In the **Value** field, paste the connection string that you copied earlier.</span></span>
9. <span data-ttu-id="45002-201">حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="45002-201">Select **Create**.</span></span>

> [!NOTE]
> <span data-ttu-id="45002-202">كلما قمت بتحديث أحد سلاسل الاتصال، يجب عليك أيضا تحديث قيم الأسرار.</span><span class="sxs-lookup"><span data-stu-id="45002-202">Whenever you update one of the connection strings, you must also update the secret values.</span></span>

<span data-ttu-id="45002-203">لقد انتهيت الآن من توفير موارد Azure المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="45002-203">You've now finished provisioning the required Azure resources.</span></span> <span data-ttu-id="45002-204">والخطوة التالية هي [تثبيت الوظيفة الإضافية لذكاء IoT في Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="45002-204">The next step is to [install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span></span>