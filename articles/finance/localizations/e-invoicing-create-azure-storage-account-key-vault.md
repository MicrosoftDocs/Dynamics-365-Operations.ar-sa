---
title: إنشاء حساب تخزين ومخزن رئيسي في Azure
description: يشرح هذا الموضوع كيفية إنشاء حساب تخزين ومخزن رئيسي في Azure.
author: gionoder
ms.date: 04/29/2021
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
ms.openlocfilehash: 5c2ddad10f9cbedd77a04fe0f42bdc217fd43344
ms.sourcegitcommit: 54d3ec0c006bfa9d2b849590205be08551c4e0f0
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/30/2021
ms.locfileid: "5963222"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a><span data-ttu-id="88918-103">إنشاء حساب تخزين ومخزن رئيسي في Azure</span><span class="sxs-lookup"><span data-stu-id="88918-103">Create an Azure storage account and a key vault</span></span>

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="88918-104">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="88918-104">Prerequisites</span></span>

<span data-ttu-id="88918-105">قبل أن تتمكن من استكمال الخطوات في هذا الموضوع، يجب التأكد من إتمام المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="88918-105">Before you can complete the steps in this topic, you must make sure that the following tasks have been completed:</span></span>

- <span data-ttu-id="88918-106">إنشاء مورد مخزن رئيسي في Azure.</span><span class="sxs-lookup"><span data-stu-id="88918-106">Create a key vault resource in Azure.</span></span> <span data-ttu-id="88918-107">لمزيد من المعلومات، راجع [حول Azure Key Vault](/azure/key-vault/general/overview).</span><span class="sxs-lookup"><span data-stu-id="88918-107">For more information, see [About Azure Key Vault](/azure/key-vault/general/overview).</span></span>
- <span data-ttu-id="88918-108">إنشاء حساب تخزين Azure (مخزن بيانات ثنائية كبيرة الحجم).</span><span class="sxs-lookup"><span data-stu-id="88918-108">Create an Azure storage account (Blob storage).</span></span> <span data-ttu-id="88918-109">لمزيد من المعلومات، راجع [المحافظة على حساب تخزين Azure](/azure/storage/blobs/).</span><span class="sxs-lookup"><span data-stu-id="88918-109">For more information, see [Maintaining Azure Storage Account](/azure/storage/blobs/).</span></span>

## <a name="overview"></a><span data-ttu-id="88918-110">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="88918-110">Overview</span></span>

<span data-ttu-id="88918-111">في هذا الموضوع، ستقوم بإكمال خطوتين أساسيتين:</span><span class="sxs-lookup"><span data-stu-id="88918-111">In this topic, you will complete two main steps:</span></span>

- <span data-ttu-id="88918-112">إعداد حساب تخزين Azure للحصول على URI حساب التخزين.</span><span class="sxs-lookup"><span data-stu-id="88918-112">Set up the Azure storage account to get the storage account URI.</span></span>
- <span data-ttu-id="88918-113">إعداد المخزن الرئيسي لتخزين URI حساب التخزين.</span><span class="sxs-lookup"><span data-stu-id="88918-113">Set up the key vault to store the storage account URI.</span></span>

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a><span data-ttu-id="88918-114">إعداد حساب تخزين Azure للحصول على URI حساب التخزين</span><span class="sxs-lookup"><span data-stu-id="88918-114">Set up the Azure storage account to get the storage account URI</span></span>

1. <span data-ttu-id="88918-115">افتح حساب التخزين الذي تخطط لاستخدامه مع الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="88918-115">Open the storage account that you plan to use with Electronic invoicing.</span></span>
2. <span data-ttu-id="88918-116">انتقل إلى **خدمة الكائن الثنائي كبير الحجم** \> **الحاويات**، وأنشئ حاوية جديدة.</span><span class="sxs-lookup"><span data-stu-id="88918-116">Go to **Blob service** \> **Containers**, and create a new container.</span></span>
3. <span data-ttu-id="88918-117">أدخل اسمًا للحاوية، وقم بتعيين حقل **مستوى الوصول العام** إلى **خاص (لا وصول مجهول الهوية)**.</span><span class="sxs-lookup"><span data-stu-id="88918-117">Enter a name for the container, and set the **Public access level** field to **Private (no anonymous access)**.</span></span>
4. <span data-ttu-id="88918-118">افتح الحاوية، وانتقل إلى **الإعدادات \> سياسة الوصول**.</span><span class="sxs-lookup"><span data-stu-id="88918-118">Open the container, and go to **Settings \> Access policy**.</span></span>
5. <span data-ttu-id="88918-119">حدد **إضافة سياسة** لإضافة سياسة وصول مخزّنة.</span><span class="sxs-lookup"><span data-stu-id="88918-119">Select **Add policy** to add a stored access policy.</span></span>
6. <span data-ttu-id="88918-120">قم بتعيين حقلي **المعرف** و **الأذونات** كما تقتضي الحاجة.</span><span class="sxs-lookup"><span data-stu-id="88918-120">Set the **Identifier** and **Permissions** fields as appropriate.</span></span> <span data-ttu-id="88918-121">في حقل **الأذونات**، يجب تحديد كافة الأذونات.</span><span class="sxs-lookup"><span data-stu-id="88918-121">In the **Permissions** field, you should select all permissions.</span></span>

    ![منح إذن تخزين كائن ثنائي كبير الحجم](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. <span data-ttu-id="88918-123">أدخل تاريخي البدء وانتهاء الصلاحية.</span><span class="sxs-lookup"><span data-stu-id="88918-123">Enter the start and expiry dates.</span></span> <span data-ttu-id="88918-124">يجب أن يكون تاريخ انتهاء الصلاحية في المستقبل.</span><span class="sxs-lookup"><span data-stu-id="88918-124">The expiry date should be in future.</span></span>
8. <span data-ttu-id="88918-125">حدد **موافق** لحفظ السياسة، ثم احفظ تغييراتك إلى الحاوية.</span><span class="sxs-lookup"><span data-stu-id="88918-125">Select **OK** to save the policy, and then save your changes to the container.</span></span>
9. <span data-ttu-id="88918-126">عد إلى حساب التخزين، وافتح **مستكشف التخزين (معاينه)**.</span><span class="sxs-lookup"><span data-stu-id="88918-126">Return to the storage account, and open **Storage Explorer (preview)**.</span></span>
10. <span data-ttu-id="88918-127">انقر بزر الماوس الأيمن فوق الحاوية، ثم حدد **الحصول على توقيع الوصول المشترك**.</span><span class="sxs-lookup"><span data-stu-id="88918-127">Right-click the container, and then select **Get Shared Access Signature**.</span></span>
11. <span data-ttu-id="88918-128">في مربع الحوار **توقيع الوصول المشترك**، قم بنسخ القيمة وتخزينها في الحقل **URI**.</span><span class="sxs-lookup"><span data-stu-id="88918-128">In the **Shared Access Signature** dialog box, copy and store the value in the **URI** field.</span></span> <span data-ttu-id="88918-129">سيتم استخدام هذه القيمة في الإجراء التالي وستتم الإشارة إليها على أنها *URI‏‎ توقيع الوصول المشترك*.</span><span class="sxs-lookup"><span data-stu-id="88918-129">This value will be used in the next procedure and will be referred to as the *shared access signature URI*.</span></span>

    ![تحديد قيمة URI ونسخها](media/e-Invoicing-services-create-azure-resources-select-and-copy-uri.png)

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a><span data-ttu-id="88918-131">إعداد المخزن الرئيسي لتخزين URI حساب التخزين</span><span class="sxs-lookup"><span data-stu-id="88918-131">Set up the key vault to store the storage account URI</span></span>

1. <span data-ttu-id="88918-132">افتح المخزن الرئيسي الذي تخطط لاستخدامه مع الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="88918-132">Open the key vault that you intend to use with Electronic invoicing.</span></span>
2. <span data-ttu-id="88918-133">انتقل إلى **الإعدادات** \> **الأسرار**، ثم حدد **إنشاء/استيراد** لإنشاء سر جديد.</span><span class="sxs-lookup"><span data-stu-id="88918-133">Go to **Settings** \> **Secrets**, and then select **Generate/Import** to create a new secret.</span></span>
3. <span data-ttu-id="88918-134">في الصفحة **إنشاء سر**، في الحقل **خيارات التحميل**، حدد **يدوي**.</span><span class="sxs-lookup"><span data-stu-id="88918-134">On the **Create a secret** page, in the **Upload options** field, select **Manual**.</span></span>
4. <span data-ttu-id="88918-135">أدخل اسم السر.</span><span class="sxs-lookup"><span data-stu-id="88918-135">Enter the name of the secret.</span></span> <span data-ttu-id="88918-136">سيتم استخدام هذا الاسم أثناء إعداد الخدمة في Regulatory Configuration Services (RCS)، وستتم الإشارة إليها على أنه *اسم سر المخزن الرئيسي*.</span><span class="sxs-lookup"><span data-stu-id="88918-136">This name will be used during setup of the service in Regulatory Configuration Service (RCS) and will be referred to as the *key vault secret name*.</span></span>
5. <span data-ttu-id="88918-137">في حقل **القيمة**، حدد **URI توقيع الوصول المشترك**، ثم حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="88918-137">In the **Value** field, select **Shared Access Signature URI**, and then select **Create**.</span></span>
6. <span data-ttu-id="88918-138">قم بإعداد سياسة الوصول لمنح الفوترة الإلكترونية المستوى الصحيح من الوصول الآمن إلى السر الذي أنشأته.</span><span class="sxs-lookup"><span data-stu-id="88918-138">Set up the access policy to grant Electronic invoicing the correct level of secure access to the secret you created.</span></span> <span data-ttu-id="88918-139">انتقل إلى **الإعدادات \> سياسة الوصول**، وحدد **إضافة سياسة وصول**.</span><span class="sxs-lookup"><span data-stu-id="88918-139">Go to **Settings \> Access policy**, and select **Add Access Policy**.</span></span>
7. <span data-ttu-id="88918-140">عيّن أذونات السر لعمليات **الحصول** و **القائمة**.</span><span class="sxs-lookup"><span data-stu-id="88918-140">Set the secret permissions for the **Get** and **List** operations.</span></span>

    ![منح حق الوصول إلى الخدمة](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. <span data-ttu-id="88918-142">عيّن أذونات الشهادة لعمليات **الحصول** و **القائمة**.</span><span class="sxs-lookup"><span data-stu-id="88918-142">Set the certificate permissions for **Get** and **List** operations.</span></span>

    ![منح إذن الشهادة](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. <span data-ttu-id="88918-144">في حقل **الرئيسي**، حدد **بلا تحديد**.</span><span class="sxs-lookup"><span data-stu-id="88918-144">In the **Select principal** field, select **None selected**.</span></span>
10. <span data-ttu-id="88918-145">في مربع الحوار **الرئيسي**، حدد الرئيسي عن طريق إضافة **خدمة الفوترة الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="88918-145">In the **Principal** dialog box, select the principal by adding **e-Invoicing Service**.</span></span>
11. <span data-ttu-id="88918-146">حدد **إضافة**، ثم حدد **حفظ تغييرات المخزن الرئيسي**.</span><span class="sxs-lookup"><span data-stu-id="88918-146">Select **Add**, and then select **Save Key Vault changes**.</span></span>
12. <span data-ttu-id="88918-147">في الصفحة **نظرة عامة**، انسخ قيمة **اسم DNS** للمخزن الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="88918-147">On the **Overview** page, copy the **DNS name** value for the key vault.</span></span> <span data-ttu-id="88918-148">سيتم استخدام هذه القيمة أثناء إعداد الخدمة في RCS وستتم الإشارة إليها على أنها *URI‏‎ المخزن الرئيسي*.</span><span class="sxs-lookup"><span data-stu-id="88918-148">This value will be used during setup of the service in RCS and will be referred as the *key vault URI*.</span></span>

> [!NOTE]
> <span data-ttu-id="88918-149">للحصول على أمان إضافي على حساب التخزين، قم بتكوين Azure Defender للتخزين.</span><span class="sxs-lookup"><span data-stu-id="88918-149">For additional security on the storage account, configure the Azure Defender for Storage.</span></span>
> 
> <span data-ttu-id="88918-150">لمزيد من المعلومات، راجع [مقدمة إلى Azure Defender للتخزين](/azure/security-center/defender-for-storage-introduction).</span><span class="sxs-lookup"><span data-stu-id="88918-150">For more information, see [Introduction to Azure Defender for Storage](/azure/security-center/defender-for-storage-introduction).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
