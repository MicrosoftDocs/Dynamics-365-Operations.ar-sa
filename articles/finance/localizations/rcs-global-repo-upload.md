---
title: إنشاء تكوينات ER في RCS وتحميلها إلى المستودع العمومي
description: يشرح هذه الموضوع كيفية إنشاء تكوين التقارير الإلكترونية (ER) في خدمات Microsoft Regulatory Configuration Services (RCS) وتحميلها إلى المستودع العمومي.
author: JaneA07
manager: AnnBe
ms.date: 05/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 0e194a8b777f984412d81e315f92ab4bb8a3b0c9
ms.sourcegitcommit: 204cec8ca2a6c4474d21dbcd408e369131a47856
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/13/2020
ms.locfileid: "3371229"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a><span data-ttu-id="56d20-103">إنشاء تكوينات ER في Regulatory Configuration Services (RCS) وتحميلها إلى المستودع العمومي</span><span class="sxs-lookup"><span data-stu-id="56d20-103">Create ER configurations in Regulatory Configuration Services (RCS) and upload them to the Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="56d20-104">يمكنك استخدام خدمات Microsoft Regulatory Configuration Services (RCS) لتصميم تكوينات التقارير الإلكترونية (ER) ثم نشرها بحيث يمكن استخدامها في المؤسسة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="56d20-104">You can use Microsoft Regulatory Configuration Services (RCS) to design Electronic reporting (ER) configurations and publish them so that they can be used in your organization.</span></span>

<span data-ttu-id="56d20-105">توضح الإجراءات التالية كيفية قيام مستخدم بدور مسؤول النظام أو مطور التقارير الإلكترونية بإنشاء إصدار مشتق من تكوين ER تم تكوينه في مثيل RCS، ثم تحميل التكوين المشتق إلى المستودع العمومي.</span><span class="sxs-lookup"><span data-stu-id="56d20-105">The following procedures explain how a user in the System Administrator or Electronic Reporting Developer role can create a derived version of an ER configuration that has been configured in an RCS instance, and then upload the derived configuration to the Global repository.</span></span> 

<span data-ttu-id="56d20-106">قبل إكمال هذه الإجراءات، يجب أن تستكمل أولا المتطلبات الأساسية التالية:</span><span class="sxs-lookup"><span data-stu-id="56d20-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="56d20-107">الوصول إلى مثيل RCS.</span><span class="sxs-lookup"><span data-stu-id="56d20-107">Access an RCS instance.</span></span>
- <span data-ttu-id="56d20-108">إنشاء موفر تكوين نشط.</span><span class="sxs-lookup"><span data-stu-id="56d20-108">Create an active configuration provider.</span></span> <span data-ttu-id="56d20-109">لمزيد من المعلومات، راجع [إنشاء موفري التكوين ووضع علامة عليهم كنشطين](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="56d20-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="56d20-110">يجب أيضا التأكد من أنه تم توفير بيئة RCS لشركك.</span><span class="sxs-lookup"><span data-stu-id="56d20-110">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="56d20-111">في تطبيق Finance and Operations، انتقل إلى **إدارة المؤسسات** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="56d20-111">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="56d20-112">في حالة عدم توفير بيئة RCS للشركة الخاصة بك، حدد **Regulatory services - التكوين الخارجي**، واتبع الإرشادات لتوفير بيئة.</span><span class="sxs-lookup"><span data-stu-id="56d20-112">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="56d20-113">إذا تم بالفعل توفير بيئة RCS لشركك، استخدم عنوان URL للصفحة للوصول إليه عن طريق تحديد خيار تسجيل الدخول.</span><span class="sxs-lookup"><span data-stu-id="56d20-113">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a><span data-ttu-id="56d20-114">إنشاء إصدار مشتق من تكوين في RCS</span><span class="sxs-lookup"><span data-stu-id="56d20-114">Create a derived version of a configuration in RCS</span></span>

1. <span data-ttu-id="56d20-115">في مساحة عمل **التقارير الإلكترونية**، تحقق من أن لديك موفر تكوين نشط لمؤسسك.</span><span class="sxs-lookup"><span data-stu-id="56d20-115">In the **Electronic reporting** workspace, verify that you have an active configuration provider for your organization.</span></span> 
2. <span data-ttu-id="56d20-116">حدد **تكوينات إعداد التقارير‬**.</span><span class="sxs-lookup"><span data-stu-id="56d20-116">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="56d20-117">حدد التكوين الذي ترغب في اشتقاق إصدار جديد منه.</span><span class="sxs-lookup"><span data-stu-id="56d20-117">Select the configuration that you want to derive a new version from.</span></span> <span data-ttu-id="56d20-118">يمكن استخدام حقل عامل التصفية فو الشجرة لتضييق البحث.</span><span class="sxs-lookup"><span data-stu-id="56d20-118">You can use the filter field above the tree to narrow your search.</span></span>
4. <span data-ttu-id="56d20-119">حدد **إنشاء تكوين** \> **مشتق من الاسم**.</span><span class="sxs-lookup"><span data-stu-id="56d20-119">Select **Create configuration** \> **Derive from Name**.</span></span>
5. <span data-ttu-id="56d20-120">أدخل اسمًا ووصفًا، ثم حدد **إنشاء التكوين** لإنشاء إصدار مشتق جديد.</span><span class="sxs-lookup"><span data-stu-id="56d20-120">Enter a name and description, and then select **Create configuration** to create a new derived version.</span></span>
6. <span data-ttu-id="56d20-121">حدد التكوين المشتق حديثا، وأضف وصفًا للإصدار، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="56d20-121">Select the newly derived configuration, add a description of the version, and then select **OK**.</span></span> <span data-ttu-id="56d20-122">يتم تغيير حالة التكوين إلى **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="56d20-122">The status of the configuration to is changed to **Completed**.</span></span>

![إصدار التكوين الجديد في RCS](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_CompleteConfig.JPG)

> [!NOTE]
> <span data-ttu-id="56d20-124">عند تغيير حالة التكوين، قد تستلم رسالة خطأ خاصة بالتحقق من الصحة تتعلق بالتطبيقات المتصلة.</span><span class="sxs-lookup"><span data-stu-id="56d20-124">When the configuration status is changed, you might receive a validation error message that is related to the connected applications.</span></span> <span data-ttu-id="56d20-125">لإيقاف تشغيل التحقق من الصحة، في جزء الإجراءات في علامة التبويب **التكوينات**، حدد **معلمات المستخدم**، ثم قم بتعيين الخيار **تخطي التحقق من الصحة عند تغير حالة التكوين وتغير العنوان الأساسي** إلى **نعم**</span><span class="sxs-lookup"><span data-stu-id="56d20-125">To turn off the validation, on the Action Pane on the **Configurations** tab, select **User parameters**, and then set the **Skip validation at configuration's status change and rebase** option to **Yes**</span></span> 

## <a name="upload-a-configuration-to-the-global-repository"></a><span data-ttu-id="56d20-126">تحميل تكوين إلى المستودع العمومي</span><span class="sxs-lookup"><span data-stu-id="56d20-126">Upload a configuration to the Global repository</span></span>

<span data-ttu-id="56d20-127">لمشاركه التكوين الجديد أو المشتق مع مؤسستك، يمكنك تحميله إلى المستودع العمومي.</span><span class="sxs-lookup"><span data-stu-id="56d20-127">To share a new or derived configuration with your organization, you can upload it to the Global repository.</span></span>

1. <span data-ttu-id="56d20-128">حدد الإصدار المكتمل من التكوين، ثم حدد **تحميل إلى المستودع**.</span><span class="sxs-lookup"><span data-stu-id="56d20-128">Select the completed version of the configuration, and then select **Upload into repository**.</span></span>
2. <span data-ttu-id="56d20-129">حدد الخيار **عمومي (Microsoft)**، ثم حدد **تحميل**.</span><span class="sxs-lookup"><span data-stu-id="56d20-129">Select the **Global (Microsoft)** option, and then select **Upload**.</span></span>

    ![خيارات التحميل إلى المستودع](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_Upload_to_GlobalRepo_options.JPG)

3. <span data-ttu-id="56d20-131">في مربع رسالة التأكيد، حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="56d20-131">In the confirmation message box, select **Yes**.</span></span> 
4. <span data-ttu-id="56d20-132">قم بتحديث وصف الإصدار كما هو مطلوب، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="56d20-132">Update the description of the version as required, and then select **OK**.</span></span> 

<span data-ttu-id="56d20-133">يتم تحديث حالة التكوين إلى **مشاركة**، ويتم تحميل التكوين إلى المستودع العمومي.</span><span class="sxs-lookup"><span data-stu-id="56d20-133">The status of the configuration is updated to **Share**, and the configuration is uploaded to the Global repository.</span></span> <span data-ttu-id="56d20-134">ومن هناك، يمكنك التعامل معه بالطرق التالية:</span><span class="sxs-lookup"><span data-stu-id="56d20-134">From there, you can work with it in the following ways:</span></span>

- <span data-ttu-id="56d20-135">استيراده إلى مثيل Dynamics 365 الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="56d20-135">Import it into your Dynamics 365 instance.</span></span> <span data-ttu-id="56d20-136">لمزيد من المعلومات، راجع [ (ER)استيراد التكوينات من RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span><span class="sxs-lookup"><span data-stu-id="56d20-136">For more information, see [(ER) Import configurations from RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span></span>
- <span data-ttu-id="56d20-137">مشاركته مع جهة خارجية أو مؤسسة خارجية، راجع [RCS مشاركة تكوينات التقارير الإلكترونية (ER) مع المؤسسات الخارجية](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/rcs-global-share-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="56d20-137">Share it with a third party or an external organization, see [RCS Share Electronic reporting (ER) configurations with external organizations](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/rcs-global-share-configuration.md)</span></span>

![إصدار تكوين نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي لـ Contoso في المستودع العمومي](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_Config_upload_GlobalRepo.JPG)
