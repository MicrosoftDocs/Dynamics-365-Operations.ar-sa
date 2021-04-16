---
title: إنشاء تكوينات ER في RCS وتحميلها إلى المستودع العمومي
description: يشرح هذه الموضوع كيفية إنشاء تكوين التقارير الإلكترونية (ER) في خدمات Microsoft Regulatory Configuration Services (RCS) وتحميلها إلى المستودع العمومي.
author: JaneA07
ms.date: 09/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: a138fd4b525077f12f6575f4b10f682728b71203
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838709"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a><span data-ttu-id="24a95-103">إنشاء تكوينات ER في Regulatory Configuration Services (RCS) وتحميلها إلى المستودع العمومي</span><span class="sxs-lookup"><span data-stu-id="24a95-103">Create ER configurations in Regulatory Configuration Services (RCS) and upload them to the Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="24a95-104">يمكنك استخدام خدمات Microsoft Regulatory Configuration Services (RCS) لتصميم تكوينات التقارير الإلكترونية (ER) ثم نشرها بحيث يمكن استخدامها في المؤسسة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="24a95-104">You can use Microsoft Regulatory Configuration Services (RCS) to design Electronic reporting (ER) configurations and publish them so that they can be used in your organization.</span></span>

<span data-ttu-id="24a95-105">توضح الإجراءات التالية كيفية قيام مستخدم بدور مسؤول النظام أو مطور التقارير الإلكترونية بإنشاء إصدار مشتق من تكوين ER تم تكوينه في مثيل RCS، ثم تحميل التكوين المشتق إلى المستودع العمومي.</span><span class="sxs-lookup"><span data-stu-id="24a95-105">The following procedures explain how a user in the System Administrator or Electronic Reporting Developer role can create a derived version of an ER configuration that has been configured in an RCS instance, and then upload the derived configuration to the Global repository.</span></span> 

<span data-ttu-id="24a95-106">قبل إكمال هذه الإجراءات، يجب أن تستكمل أولا المتطلبات الأساسية التالية:</span><span class="sxs-lookup"><span data-stu-id="24a95-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="24a95-107">الوصول إلى مثيل RCS.</span><span class="sxs-lookup"><span data-stu-id="24a95-107">Access an RCS instance.</span></span>
- <span data-ttu-id="24a95-108">إنشاء موفر تكوين نشط.</span><span class="sxs-lookup"><span data-stu-id="24a95-108">Create an active configuration provider.</span></span> <span data-ttu-id="24a95-109">لمزيد من المعلومات، راجع [إنشاء موفري التكوين ووضع علامة عليهم كنشطين](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="24a95-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="24a95-110">يجب أيضا التأكد من أنه تم توفير بيئة RCS لشركك.</span><span class="sxs-lookup"><span data-stu-id="24a95-110">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="24a95-111">في تطبيق Finance and Operations، انتقل إلى **إدارة المؤسسات** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="24a95-111">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="24a95-112">في حالة عدم توفير بيئة RCS للشركة الخاصة بك، حدد **Regulatory services - التكوين الخارجي**، واتبع الإرشادات لتوفير بيئة.</span><span class="sxs-lookup"><span data-stu-id="24a95-112">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="24a95-113">إذا تم بالفعل توفير بيئة RCS لشركك، استخدم عنوان URL للصفحة للوصول إليه عن طريق تحديد خيار تسجيل الدخول.</span><span class="sxs-lookup"><span data-stu-id="24a95-113">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a><span data-ttu-id="24a95-114">إنشاء إصدار مشتق من تكوين في RCS</span><span class="sxs-lookup"><span data-stu-id="24a95-114">Create a derived version of a configuration in RCS</span></span>

1. <span data-ttu-id="24a95-115">في مساحة عمل **التقارير الإلكترونية**، تحقق من أن لديك موفر تكوين نشط لمؤسسك.</span><span class="sxs-lookup"><span data-stu-id="24a95-115">In the **Electronic reporting** workspace, verify that you have an active configuration provider for your organization.</span></span> 
2. <span data-ttu-id="24a95-116">حدد **تكوينات إعداد التقارير‬**.</span><span class="sxs-lookup"><span data-stu-id="24a95-116">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="24a95-117">حدد التكوين الذي ترغب في اشتقاق إصدار جديد منه.</span><span class="sxs-lookup"><span data-stu-id="24a95-117">Select the configuration that you want to derive a new version from.</span></span> <span data-ttu-id="24a95-118">يمكن استخدام حقل عامل التصفية فو الشجرة لتضييق البحث.</span><span class="sxs-lookup"><span data-stu-id="24a95-118">You can use the filter field above the tree to narrow your search.</span></span>
4. <span data-ttu-id="24a95-119">حدد **إنشاء تكوين** \> **مشتق من الاسم**.</span><span class="sxs-lookup"><span data-stu-id="24a95-119">Select **Create configuration** \> **Derive from Name**.</span></span>
5. <span data-ttu-id="24a95-120">أدخل اسمًا ووصفًا، ثم حدد **إنشاء التكوين** لإنشاء إصدار مشتق جديد.</span><span class="sxs-lookup"><span data-stu-id="24a95-120">Enter a name and description, and then select **Create configuration** to create a new derived version.</span></span>
6. <span data-ttu-id="24a95-121">حدد التكوين المشتق حديثا، وأضف وصفًا للإصدار، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="24a95-121">Select the newly derived configuration, add a description of the version, and then select **OK**.</span></span> <span data-ttu-id="24a95-122">يتم تغيير حالة التكوين إلى **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="24a95-122">The status of the configuration to is changed to **Completed**.</span></span>

![إصدار التكوين الجديد في RCS](media/RCS_CompleteConfig.JPG)

> [!NOTE]
> <span data-ttu-id="24a95-124">عند تغيير حالة التكوين، قد تستلم رسالة خطأ خاصة بالتحقق من الصحة تتعلق بالتطبيقات المتصلة.</span><span class="sxs-lookup"><span data-stu-id="24a95-124">When the configuration status is changed, you might receive a validation error message that is related to the connected applications.</span></span> <span data-ttu-id="24a95-125">لإيقاف تشغيل التحقق من الصحة، في جزء الإجراءات في علامة التبويب **التكوينات**، حدد **معلمات المستخدم**، ثم قم بتعيين الخيار **تخطي التحقق من الصحة عند تغير حالة التكوين وتغير العنوان الأساسي** إلى **نعم**</span><span class="sxs-lookup"><span data-stu-id="24a95-125">To turn off the validation, on the Action Pane on the **Configurations** tab, select **User parameters**, and then set the **Skip validation at configuration's status change and rebase** option to **Yes**</span></span> 

## <a name="upload-a-configuration-to-the-global-repository"></a><span data-ttu-id="24a95-126">تحميل تكوين إلى المستودع العمومي</span><span class="sxs-lookup"><span data-stu-id="24a95-126">Upload a configuration to the Global repository</span></span>

<span data-ttu-id="24a95-127">لمشاركه التكوين الجديد أو المشتق مع مؤسستك، يمكنك تحميله إلى المستودع العمومي.</span><span class="sxs-lookup"><span data-stu-id="24a95-127">To share a new or derived configuration with your organization, you can upload it to the Global repository.</span></span>

1. <span data-ttu-id="24a95-128">حدد الإصدار المكتمل من التكوين، ثم حدد **تحميل إلى المستودع**.</span><span class="sxs-lookup"><span data-stu-id="24a95-128">Select the completed version of the configuration, and then select **Upload into repository**.</span></span>
2. <span data-ttu-id="24a95-129">حدد الخيار **عمومي (Microsoft)**، ثم حدد **تحميل**.</span><span class="sxs-lookup"><span data-stu-id="24a95-129">Select the **Global (Microsoft)** option, and then select **Upload**.</span></span>

    ![خيارات التحميل إلى المستودع](media/RCS_Upload_to_GlobalRepo_options.JPG)

3. <span data-ttu-id="24a95-131">في مربع رسالة التأكيد، حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="24a95-131">In the confirmation message box, select **Yes**.</span></span> 
4. <span data-ttu-id="24a95-132">قم بتحديث وصف الإصدار كما هو مطلوب، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="24a95-132">Update the description of the version as required, and then select **OK**.</span></span> 

<span data-ttu-id="24a95-133">يتم تحديث حالة التكوين إلى **مشاركة**، ويتم تحميل التكوين إلى المستودع العمومي.</span><span class="sxs-lookup"><span data-stu-id="24a95-133">The status of the configuration is updated to **Share**, and the configuration is uploaded to the Global repository.</span></span> <span data-ttu-id="24a95-134">ومن هناك، يمكنك التعامل معه بالطرق التالية:</span><span class="sxs-lookup"><span data-stu-id="24a95-134">From there, you can work with it in the following ways:</span></span>

- <span data-ttu-id="24a95-135">استيراده إلى مثيل Dynamics 365 الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="24a95-135">Import it into your Dynamics 365 instance.</span></span> <span data-ttu-id="24a95-136">لمزيد من المعلومات، راجع [ (ER)استيراد التكوينات من RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span><span class="sxs-lookup"><span data-stu-id="24a95-136">For more information, see [(ER) Import configurations from RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span></span>
- <span data-ttu-id="24a95-137">مشاركته مع جهة خارجية أو مؤسسة خارجية، راجع [RCS مشاركة تكوينات التقارير الإلكترونية (ER) مع المؤسسات الخارجية](rcs-global-repo-share-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="24a95-137">Share it with a third party or an external organization, see [RCS Share Electronic reporting (ER) configurations with external organizations](rcs-global-repo-share-configuration.md)</span></span>

    ![إصدار تكوين نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي لـ Contoso في المستودع العمومي](media/RCS_Config_upload_GlobalRepo.JPG)

## <a name="delete-a-configuration-from-the-global-repository"></a><span data-ttu-id="24a95-139">حذف تكوين من المستودع العمومي</span><span class="sxs-lookup"><span data-stu-id="24a95-139">Delete a configuration from the Global repository</span></span>
<span data-ttu-id="24a95-140">قم بإكمال الخطوات التالية لحذف تكوين أنشأته مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="24a95-140">Complete the following steps to delete a configuration that your organization has created.</span></span>

1. <span data-ttu-id="24a95-141">في مساحة عمل **التقارير الإلكترونية**، تأكد من أن حالة موفر التكوين هي **نشط**.</span><span class="sxs-lookup"><span data-stu-id="24a95-141">In the **Electronic reporting** workspace, verify that your configuration provider is **Active**.</span></span> <span data-ttu-id="24a95-142">لمزيد من المعلومات، راجع [إنشاء موفري التكوين ووضع علامة عليهم كنشطين](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="24a95-142">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
2. <span data-ttu-id="24a95-143">على موفر التكوين النشط، حدد **المستودع**.</span><span class="sxs-lookup"><span data-stu-id="24a95-143">On your active configuration provider, select **repository**.</span></span>
3. <span data-ttu-id="24a95-144">حدد نوع المستودع **عمومي**، ثم حدد **فتح**.</span><span class="sxs-lookup"><span data-stu-id="24a95-144">Select the repository type **Global**, and select **Open**.</span></span>
4. <span data-ttu-id="24a95-145">على علامة التبويب السريعة **التصفية**، ابحث عن التكوين الذي تريد حذفه باستخدام وظيفة **التصفية**.</span><span class="sxs-lookup"><span data-stu-id="24a95-145">On the **Filter** FastTab, find the configuration that you want to delete by using the **Filter** functionality.</span></span>
5. <span data-ttu-id="24a95-146">على علامة التبويب السريعة **الإصدار**، حدد إصدار التكوين الذي ترغب في حذفه، ثم حدد **حذف**:</span><span class="sxs-lookup"><span data-stu-id="24a95-146">On the **Version** FastTab, select the version of the configuration that you want to delete, and then select **Delete**:</span></span>

    ![حذف تكوين من المستودع العمومي](media/RCS_Delete_from_GlobalRepo.JPG)

6. <span data-ttu-id="24a95-148">في مربع رسالة التأكيد، حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="24a95-148">In the confirmation message box, select **Yes**.</span></span>

    ![حذف رسالة تأكيد إصدار التكوين](media/RCS_Delete_from_GlobalRepo_Msg.JPG)
 
<span data-ttu-id="24a95-150">يتم حذف إصدار التكوين، وتظهر رسالة التأكيد.</span><span class="sxs-lookup"><span data-stu-id="24a95-150">The configuration version is deleted, and confirmation message is shown.</span></span> 

> [!NOTE]
> <span data-ttu-id="24a95-151">يمكن حذف التكوينات فقط من قبل موفر التكوين الذي قام بإنشائها.</span><span class="sxs-lookup"><span data-stu-id="24a95-151">Configurations can only be deleted by the Configuration provider that created them.</span></span> <span data-ttu-id="24a95-152">إذا تمت مشاركة التكوين مع مؤسسة أخرى، فيجب إلغاء مشاركة التكوين  قبل أن تتمكن من حذفه.</span><span class="sxs-lookup"><span data-stu-id="24a95-152">If the configuration has been shared with another organization, the configuration will need to be unshared before you delete it.</span></span>
 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]