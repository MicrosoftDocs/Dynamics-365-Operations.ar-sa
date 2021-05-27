---
title: ملفات تعريف الشهادات المعرفة من قِبل المستخدمين لمتاجر البيع بالتجزئة
description: يقدم هذا الموضوع نظره عامه حول كيفيه استخدام الشهادات في متاجر البيع بالتجزئة.
author: josaw
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 44042fc43fa3b43358120fb6f8f633abeae7005f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020303"
---
# <a name="user-defined-certificate-profiles-for-retail-stores"></a><span data-ttu-id="d6d42-103">ملفات تعريف الشهادات المعرفة من قِبل المستخدمين لمتاجر البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="d6d42-103">User-defined certificate profiles for retail stores</span></span>

[!include [banner](../includes/banner.md)]


## <a name="overview"></a><span data-ttu-id="d6d42-104">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="d6d42-104">Overview</span></span>

<span data-ttu-id="d6d42-105">يوفر هذا الموضوع نظرة عامة حول ملفات تعريف الشهادات المتوفرة في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d6d42-105">This topic provides an overview of the certificate profiles that are available in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="d6d42-106">تعمل هذه الوظيفة علي توسيع ميزه [أداره قنوات البيع بالتجزئة](../dev-itpro/manage-secrets.md)عن طريق أضافه دعم للشهادات المحلية.</span><span class="sxs-lookup"><span data-stu-id="d6d42-106">This functionality extends the [Manage secrets for retail channels](../dev-itpro/manage-secrets.md) feature by adding support for local certificates.</span></span>

<span data-ttu-id="d6d42-107">اثناء تشغيل نقطه البيع (POS) في الوضع "غير متصل"، لا يمكن الوصول إلى الشهادات المخزنة في المخزن الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="d6d42-107">While the point of sale (POS) is running in offline mode, it can't access the certificates that are stored in the key vault.</span></span> <span data-ttu-id="d6d42-108">يجب استخدام الشهادة المحلية بدلا منها.</span><span class="sxs-lookup"><span data-stu-id="d6d42-108">The local certificate should be used instead.</span></span> <span data-ttu-id="d6d42-109">الإمكانات التالية مدعومة:</span><span class="sxs-lookup"><span data-stu-id="d6d42-109">The following capabilities are supported:</span></span>

- <span data-ttu-id="d6d42-110">استخدام الشهادات المحلية في سيناريوهات الاحتياطي للمخزن الرئيسي</span><span class="sxs-lookup"><span data-stu-id="d6d42-110">Using local certificates in key vault fallback scenarios</span></span>
- <span data-ttu-id="d6d42-111">استخدام الشهادات المحلية بدون المخزن الرئيسي (علي سبيل المثال، في تثبيت محلي)</span><span class="sxs-lookup"><span data-stu-id="d6d42-111">Using local certificates without a key vault (for example in an on-premises installation)</span></span>
- <span data-ttu-id="d6d42-112">تحديث تدريجي للشهادات، حيث تستخدم بعض المخازن والوحدات الطرفية إصدارا جديدا للشهادة، ولكن بعض المتاجر والوحدات الطرفية الأخرى تستمر في استخدام الإصدار السابق</span><span class="sxs-lookup"><span data-stu-id="d6d42-112">Gradual update of certificates, where some stores and terminals use a new version of the certificate, but other stores and terminals continue to use the previous version</span></span>

<span data-ttu-id="d6d42-113">تمكنك وظيفة ملفات تعريف الشهادات من تحديد الشهادة الافتراضية وتعيين الترتيب الذي يتم من خلاله البحث في الشهادات الموجودة في نفس ملف تعريف الشهادة.</span><span class="sxs-lookup"><span data-stu-id="d6d42-113">The certificate profiles functionality lets you specify a default certificate and set the order that certificates in the same certificate profile are searched in.</span></span> <span data-ttu-id="d6d42-114">توفر هذه الوظيفة أيضا أسلوب اعداد مشابه للشهادات المحلية وشهادات المخزن الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="d6d42-114">This functionality also provides a similar setup approach for local certificates and Key Vault certificates.</span></span> <span data-ttu-id="d6d42-115">يمكنك أضافه إعدادات خاصه بالشركة للشهادات، ولكن يمكن استخدام معرف الشركة المشتركة الفريد لكل شهادة في قنوات التجارة.</span><span class="sxs-lookup"><span data-stu-id="d6d42-115">You can add company-specific settings for certificates, but the unique cross-company identifier for each certificate can be used in the Commerce channels.</span></span>

### <a name="scenarios"></a><span data-ttu-id="d6d42-116">السيناريوهات</span><span class="sxs-lookup"><span data-stu-id="d6d42-116">Scenarios</span></span>

<span data-ttu-id="d6d42-117">تدعم وظيفة ملفات تعريف الشهادات السيناريوهات التالية في قنوات التجارة:</span><span class="sxs-lookup"><span data-stu-id="d6d42-117">The certificate profiles functionality supports the following scenarios in the Commerce channels:</span></span>

- <span data-ttu-id="d6d42-118">استخدم الشهادات المحلية في سيناريوهات الاحتياطي للمخزن الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="d6d42-118">Use a local certificate in key vault fallback scenarios.</span></span> <span data-ttu-id="d6d42-119">فيما يلي بعض الأمثلة عن هذه سيناريوهات الاحتياطي هذه:</span><span class="sxs-lookup"><span data-stu-id="d6d42-119">Here are some examples of these fallback scenarios:</span></span>

    - <span data-ttu-id="d6d42-120">لا يمكن الوصول إلى مساحة التخزين في المخزن الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="d6d42-120">The key vault storage isn't accessible.</span></span>
    - <span data-ttu-id="d6d42-121">لم يتم العثور علي شهادة في مساحة التخزين في المخزن الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="d6d42-121">A certificate isn't found in the key vault storage.</span></span>
    - <span data-ttu-id="d6d42-122">نقطه البيع قيد التشغيل في وضع عدم الاتصال.</span><span class="sxs-lookup"><span data-stu-id="d6d42-122">The POS is running in offline mode.</span></span>

- <span data-ttu-id="d6d42-123">استخدام الشهادات المحلية بدون تخزينها في المخزن الرئيسي (علي سبيل المثال، في تثبيت محلي)</span><span class="sxs-lookup"><span data-stu-id="d6d42-123">Use local certificates, but without storing them in the key vault (for example, in an on-premises installation).</span></span>
- <span data-ttu-id="d6d42-124">قم بتحديث تدريجي للشهادات، حيث يتم استخدام إصدار جديد من الشهادة فقط في المتاجر أو علي الوحدات الطرفية التي يكون فيها الإصدار الجديد متاحا بالفعل.</span><span class="sxs-lookup"><span data-stu-id="d6d42-124">Do a gradual update of certificates, where a new version of the certificate is used only in stores or on terminals where the new version is already available.</span></span>
- <span data-ttu-id="d6d42-125">استخدم نفس الشهادة في العديد من الشركات.</span><span class="sxs-lookup"><span data-stu-id="d6d42-125">Use the same certificate in several companies.</span></span>

## <a name="set-up-certificate-profiles"></a><span data-ttu-id="d6d42-126">إعداد ملفات تعريف الشهادات</span><span class="sxs-lookup"><span data-stu-id="d6d42-126">Set up certificate profiles</span></span>

<span data-ttu-id="d6d42-127">يوضح الاجراء التالي كيفيه اعداد ملفات تعريف الشهادات.</span><span class="sxs-lookup"><span data-stu-id="d6d42-127">The following procedure explains how to set up certificate profiles.</span></span> <span data-ttu-id="d6d42-128">قبل استخدام ملفات تعريف الشهادات في قنوات التجارة، اتبع الخطوات التالية لتكوين الإعدادات.</span><span class="sxs-lookup"><span data-stu-id="d6d42-128">Before you use certificate profiles in the Commerce channels, follow these steps to configure the settings.</span></span>

1. <span data-ttu-id="d6d42-129">في مساحة عمل **أداره الميزات**، قم بتشغيل ميزة **ملفات تعريف الشهادات المعرفة من قبل المستخدم لمخازن البيع بالتجزئة**.</span><span class="sxs-lookup"><span data-stu-id="d6d42-129">In the **Feature management** workspace, turn on the **User-defined certificate profiles for retail stores** feature.</span></span>
2. <span data-ttu-id="d6d42-130">انتقل إلى **إدارة النظام \> الإعداد \> ملفات تعريف الشهادات**.</span><span class="sxs-lookup"><span data-stu-id="d6d42-130">Go to **System administration \> Setup \> Certificate profiles**.</span></span>
3. <span data-ttu-id="d6d42-131">قم بإنشاء سجل، ثم قم بتعيين حقول **ملفات تعريف الشهادات** و **الاسم** و **الوصف**.</span><span class="sxs-lookup"><span data-stu-id="d6d42-131">Create a record, and set the **Certificate profile**, **Name**, and **Description** fields for it.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d6d42-132">ملف تعريف الشهادة هو معرف فريد لأحدي الشهادات عبر كافة الشركات ومكونات التجارة.</span><span class="sxs-lookup"><span data-stu-id="d6d42-132">The certificate profile is a unique identifier of a certificate across all companies and Commerce components.</span></span>

3. <span data-ttu-id="d6d42-133">في علامة التبويب **الكيانات القانونية**، قم باضافه بند وحدد الكيان القانوني (الشركة) الذي يجب استخدام ملف تعريف الشهادة الحالية له.</span><span class="sxs-lookup"><span data-stu-id="d6d42-133">On the **Legal entities** tab, add a line, and select the legal entity (company) that the current certificate profile should be used for.</span></span> <span data-ttu-id="d6d42-134">إذا كان يجب استخدام ملف تعريف الشهادة للعديد من الكيانات القانونية، كرر هذه الخطوة لأضافه بند لكل كيان قانوني إضافي.</span><span class="sxs-lookup"><span data-stu-id="d6d42-134">If the certificate profile should be used for multiple legal entities, repeat this step to add a line for each additional legal entity.</span></span>
4. <span data-ttu-id="d6d42-135">حدد **الإعدادات** لفتح صفحه **إعدادات ملف تعريف الشهادات**، حيث يمكنك إدخال إعدادات خاصه بالشركة لملف تعريف الشهادات.</span><span class="sxs-lookup"><span data-stu-id="d6d42-135">Select **Settings** to open the **Certificate profile settings** page, where you can enter company-specific settings for the certificate profile.</span></span>

### <a name="certificate-profile-settings"></a><span data-ttu-id="d6d42-136">إعدادات ملفات تعريف الشهادات</span><span class="sxs-lookup"><span data-stu-id="d6d42-136">Certificate profile settings</span></span>

<span data-ttu-id="d6d42-137">عند تحديد **الإعدادات** لبنود ملف تعريف الشهادات، تظهر صفحه **إعدادات ملف تعريف الشهادة**.</span><span class="sxs-lookup"><span data-stu-id="d6d42-137">When you select **Settings** for certificate profile lines, the **Certificate profile settings** page appears.</span></span> <span data-ttu-id="d6d42-138">تتيح لك هذه الصفحة تحديد الشهادات التي يمكن استخدامها عند استدعاء ملف تعريف الشهادات الحالي في قنوات التجارة.</span><span class="sxs-lookup"><span data-stu-id="d6d42-138">This page lets you specify which certificates can be used when the current certificate profile is called in the Commerce channels.</span></span> <span data-ttu-id="d6d42-139">يمكنك أيضا تحديد الترتيب الذي يجب ان يتم البحث فيه عن الشهادات.</span><span class="sxs-lookup"><span data-stu-id="d6d42-139">You can also specify the order that certificates should be searched in.</span></span>

> [!NOTE]
> <span data-ttu-id="d6d42-140">يتم تعيين حقل **الأولوية** تلقائيا.</span><span class="sxs-lookup"><span data-stu-id="d6d42-140">The **Priority** field is automatically set.</span></span> <span data-ttu-id="d6d42-141">وتمثل القيمة **1** اعلي اولويه.</span><span class="sxs-lookup"><span data-stu-id="d6d42-141">A value of **1** represents the highest priority.</span></span> <span data-ttu-id="d6d42-142">عند أضافه سطر جديد في صفحه **إعدادات ملف تعريف الشهادات**، يتم تعيين الاولويه الخاصة به إلى رقم يكون واحدا أو أكثر من اولويه السطر السابق.</span><span class="sxs-lookup"><span data-stu-id="d6d42-142">When a new line is added on the **Certificate profile settings** page, its priority is set to a number that is one more than the priority of the previous line.</span></span> <span data-ttu-id="d6d42-143">لتغيير الاولويه لبند معين، حدد البند، ثم حدد اما **التحرك لاعلي** لزيادة الاولويه أو **التحرك لأسفل** لتقليل الاولويه.</span><span class="sxs-lookup"><span data-stu-id="d6d42-143">To change the priority of a specific line, select the line, and then select either **Move up** to increase the priority or **Move down** to decrease the priority.</span></span>

<span data-ttu-id="d6d42-144">عند أضافه بند جديد إلى صفحه **إعدادات ملف تعريف الشهادة**، قم بتعيين الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="d6d42-144">When you add a new line to the **Certificate profile settings** page, set the following fields:</span></span>

- <span data-ttu-id="d6d42-145">**نوع الموقع** – حدد الموقع الذي تم تخزين الشهادة فيه.</span><span class="sxs-lookup"><span data-stu-id="d6d42-145">**Location type** – Select the location where the certificate is stored.</span></span> <span data-ttu-id="d6d42-146">يشتمل هذا الحقل علي قيمتين محتملتين: **الشهادة المحلية** و **المخزن الرئيسي**.</span><span class="sxs-lookup"><span data-stu-id="d6d42-146">This field has two possible values: **Local certificate** and **Key Vault**.</span></span>
- <span data-ttu-id="d6d42-147">**شهادة المخزن الرئيسي** -هذا الحقل مطلوب إذا قمت بتعيين **حقل نوع الموقع** إلى **المخزن الرئيسي**.</span><span class="sxs-lookup"><span data-stu-id="d6d42-147">**Key Vault certificate** – This field is required if you set the **Location type** field to **Key Vault**.</span></span> <span data-ttu-id="d6d42-148">يتم استخدام ذلك لتعيين كلمه سر لشهادة المخزن الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="d6d42-148">Use it to specify a Key Vault certificate secret.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d6d42-149">قبل استخدام شهادة المخزن الرئيسي في ملفات تعريف الشهادات، تاكد من تحميل شهادة إلى مساحة تخزين المخازن الرئيسية، ثم اتبع الإرشادات الموجودة في اعداد [عميل Azure Key Vault](../../finance/localizations/setting-up-azure-key-vault-client.md).</span><span class="sxs-lookup"><span data-stu-id="d6d42-149">Before you use a Key Vault certificate in certificate profiles, be sure to upload a certificate to the key vault storage, and follow the instructions in [Set up the Azure Key Vault client](../../finance/localizations/setting-up-azure-key-vault-client.md).</span></span>

- <span data-ttu-id="d6d42-150">**اسم المتجر** – هذا الحقل اختياري ولا يتوفر الا إذا قمت بتعيين حقل **نوع الموقع** إلى **شهادة محليه**.</span><span class="sxs-lookup"><span data-stu-id="d6d42-150">**Store name** – This field is optional and is available only if you set the **Location type** field to **Local certificate**.</span></span> <span data-ttu-id="d6d42-151">يتم استخدام ذلك لتحديد اسم المتجر الافتراضي الذي يجب استخدامه للبحث في الشهادات المحلية.</span><span class="sxs-lookup"><span data-stu-id="d6d42-151">Use it to specify a default store name that should be used to search local certificates.</span></span>
- <span data-ttu-id="d6d42-152">**موقع المتجر** – هذا الحقل اختياري ولا يتوفر الا إذا قمت بتعيين حقل **نوع الموقع** إلى **شهادة محليه**.</span><span class="sxs-lookup"><span data-stu-id="d6d42-152">**Store location** – This field is optional and is available only if you set the **Location type** field to **Local certificate**.</span></span> <span data-ttu-id="d6d42-153">يتم استخدام ذلك لتحديد موقع المتجر الافتراضي الذي يجب استخدامه للبحث في الشهادات المحلية.</span><span class="sxs-lookup"><span data-stu-id="d6d42-153">Use it to specify a default store location that should be used to search local certificates.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d6d42-154">تتم أضافه اسم المتجر وموقع التخزين الافتراضيين لتبسيط عمليه البحث عن الشهادات المحلية في Commerce Runtime.</span><span class="sxs-lookup"><span data-stu-id="d6d42-154">The default store name and store location are added to simplify the process of searching local certificates in the Commerce runtime.</span></span> <span data-ttu-id="d6d42-155">يتضمن X509StoreProvider قائمه بالمجلدات التي يتم تخزين الشهادات بها.</span><span class="sxs-lookup"><span data-stu-id="d6d42-155">X509StoreProvider has a list of folders where certificates are stored.</span></span> <span data-ttu-id="d6d42-156">إذا لم يتم تحديد اسم المتجر الافتراضي وموقع المتجر الافتراضي، X509StoreProvider يحاول العثور علي شهادة في المجلدات الأخرى في القائمة الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="d6d42-156">If the default store name and the default store location aren't specified, X509StoreProvider tries to find a certificate in the other folders on its list.</span></span>

- <span data-ttu-id="d6d42-157">**بصمة الإبهام** – هذا الحقل مطلوب ولا يتوفر الا إذا قمت بتعيين حقل **نوع الموقع** إلى **شهادة محليه**.</span><span class="sxs-lookup"><span data-stu-id="d6d42-157">**Thumbprint** – This field is required and available only if you set the **Location type** field to **Local certificate**.</span></span> <span data-ttu-id="d6d42-158">استخدمه لتحديد بصمه إبهام الشهادة.</span><span class="sxs-lookup"><span data-stu-id="d6d42-158">Use it to specify the certificate thumbprint.</span></span>
- <span data-ttu-id="d6d42-159">**التعليقات** – هذا الحقل اختياري ويتيح للمستخدمين إدخال الملاحظات.</span><span class="sxs-lookup"><span data-stu-id="d6d42-159">**Comments** – This field is optional and lets users enter notes.</span></span>

### <a name="workflow-searching-certificates-in-the-commerce-runtime"></a><span data-ttu-id="d6d42-160">سير العمل: البحث في الشهادات في Commerce Runtime</span><span class="sxs-lookup"><span data-stu-id="d6d42-160">Workflow: Searching certificates in the Commerce runtime</span></span>

<span data-ttu-id="d6d42-161">وفيما يلي سير العمل الأساسي الذي يستخدم للبحث عن أحدي الشهادات عند استدعاء ملف تعريف الشهادة في Commerce Runtime.</span><span class="sxs-lookup"><span data-stu-id="d6d42-161">Here is the basic workflow that is used to search for a certificate when a certificate profile is called in the Commerce runtime.</span></span>

1. <span data-ttu-id="d6d42-162">يحدد النظام ما إذا كان ملف تعريف الشهادة يحتوي علي إعدادات خاصه بالشركة للكيان القانوني الحالي.</span><span class="sxs-lookup"><span data-stu-id="d6d42-162">The system identifies whether the certificate profile has company-specific settings for the current legal entity.</span></span>
1. <span data-ttu-id="d6d42-163">ويحاول النظام العثور علي الشهادة باستخدام القيم الموجودة في صفحة **إعدادات ملف تعريف الشهادة** للبند حيث تم تعيين الحقل **الأولولية**  إلى **1**.</span><span class="sxs-lookup"><span data-stu-id="d6d42-163">The system tries to find the certificate by using the values on the **Certificate profile settings** page for the line where the **Priority** field is set to **1**.</span></span>

    - <span data-ttu-id="d6d42-164">إذا تم تعيين حقل **نوع الموقع** إلى **مخزن رئيسي**، سيتم استخدام قيمه الحقل **سر شهادة المخزن الرئيسي** للبحث عن الشهادة في الصفحة **معلمات المخزن الرئيسي**.</span><span class="sxs-lookup"><span data-stu-id="d6d42-164">If the **Location type** field is set to **Key Vault**, the value of the **Key Vault certificate secret** field is used to search for the certificate on the **Key vault parameters** page.</span></span> <span data-ttu-id="d6d42-165">يتم بعد ذلك البحث عن الشهادة في مساحة تخزين المخزن الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="d6d42-165">The certificate is then searched for in the key vault storage.</span></span>
    - <span data-ttu-id="d6d42-166">إذا تم تعيين الحقل **نوع الموقع** إلى **الشهادة المحلية**، يقوم X509StoreProvider أولا بالبحث عن الشهادة باستخدام اسم المتجر وموقع المتجر الافتراضي، في حاله تحديد هذه المعلمات.</span><span class="sxs-lookup"><span data-stu-id="d6d42-166">If the **Location type** field is set to **Local certificate**, X509StoreProvider first searches for the certificate by using the default store name and store location, if these parameters are specified.</span></span> <span data-ttu-id="d6d42-167">ثم يبحث في كافة المجلدات الأخرى الموجودة علي قائمه المجلدات الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="d6d42-167">It then searches in all other folders on its list of folders.</span></span>

1. <span data-ttu-id="d6d42-168">في حاله عدم العثور علي الشهادة، يتم تكرار العملية للسطر حيث تم إعداد الحقل **الأولولية** على **2**، وهكذا.</span><span class="sxs-lookup"><span data-stu-id="d6d42-168">If the certificate isn't found, the process is repeated for the line where the **Priority** field is set to **2**, and so on.</span></span>

> [!NOTE]
> <span data-ttu-id="d6d42-169">إذا لم يكن لملف تعريف الشهادة إعدادات للكيان القانوني الحالي ، أو في حاله عدم نجاح البحث عن الشهادات لكافة السطور في صفحه **إعدادات ملف تعريف الشهادة**، لا يتم العثور علي الشهادة.</span><span class="sxs-lookup"><span data-stu-id="d6d42-169">If the certificate profile has no settings for the current legal entity, or if the certificate search is unsuccessful for all lines on the **Certificate profile settings** page, the certificate isn't found.</span></span>

#### <a name="caching-the-results-of-certificate-searches"></a><span data-ttu-id="d6d42-170">التخزين المؤقت لنتائج عمليات البحث في الشهادات</span><span class="sxs-lookup"><span data-stu-id="d6d42-170">Caching the results of certificate searches</span></span>

<span data-ttu-id="d6d42-171">تم التخزين المؤقت لنتائج عمليات البحث في الشهادات.</span><span class="sxs-lookup"><span data-stu-id="d6d42-171">The results of certificate searches are cached.</span></span> <span data-ttu-id="d6d42-172">يكون وقت انتهاء الصلاحية الافتراضي لذاكره التخزين المؤقت ساعة واحده.</span><span class="sxs-lookup"><span data-stu-id="d6d42-172">The default expiration time for a cache is one hour.</span></span> <span data-ttu-id="d6d42-173">ومع ذلك، يمكن تخصيص هذا الوقت وتعيينه إلى الحد الأقصى لقيمه 24 ساعة.</span><span class="sxs-lookup"><span data-stu-id="d6d42-173">However, this time can be customized and can be set to a maximum value of 24 hours.</span></span>

### <a name="gradual-update"></a><span data-ttu-id="d6d42-174">تحديث تدريجي</span><span class="sxs-lookup"><span data-stu-id="d6d42-174">Gradual update</span></span>

<span data-ttu-id="d6d42-175">في حاله تقديم إصدار جديد من الشهادة، وعدم امكانيه تحديثها في كافة المتاجر في نفس الوقت، تقوم وظيفة ملفات تعريف الشهادات بتمكين تحديث الشهادة تدريجيا.</span><span class="sxs-lookup"><span data-stu-id="d6d42-175">If a new version of the certificate is introduced, but it can't be updated in all stores at the same time, the certificate profiles functionality enables the certificate to be updated gradually.</span></span>

1. <span data-ttu-id="d6d42-176">البحث عن ملف تعريف الشهادة والبند الذي يجب تحديثه ، ثم تحديد **الإعدادات**.</span><span class="sxs-lookup"><span data-stu-id="d6d42-176">Find a certificate profile and the line that should be updated, and then select **Settings**.</span></span>
1. <span data-ttu-id="d6d42-177">قم باضافه بند، وحدد الإعدادات المرتبطة بأحدث إصدار من الشهادة.</span><span class="sxs-lookup"><span data-stu-id="d6d42-177">Add a line, and specify settings that are related to the latest version of the certificate.</span></span>
1. <span data-ttu-id="d6d42-178">قم بزيادة قيمه **الاولويه** للسطر الجديد.</span><span class="sxs-lookup"><span data-stu-id="d6d42-178">Increase the **Priority** value of the new line.</span></span> <span data-ttu-id="d6d42-179">استخدم الزر **تحريك لاعلي** لتحريك الخط بحيث يكون فوق السطر الخاص بالإصدار السابق لنفس الشهادة.</span><span class="sxs-lookup"><span data-stu-id="d6d42-179">Use the **Move up** button to move the line so that it's above the line for the previous version of the same certificate.</span></span>

> [!NOTE]
> <span data-ttu-id="d6d42-180">في Commerce Runtime، يتم استدعاء الإصدار الجديد من الشهادة أولا.</span><span class="sxs-lookup"><span data-stu-id="d6d42-180">In the Commerce runtime, the new version of the certificate will be called first.</span></span> <span data-ttu-id="d6d42-181">إذا لم يتم تحديث الشهادة بعد ذلك في متجر معين أو في وحده طرفيه معينه، سيتم استدعاء الإصدار السابق.</span><span class="sxs-lookup"><span data-stu-id="d6d42-181">If the certificate hasn't yet been updated in a specific store or on a specific terminal, the previous version will be called.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]