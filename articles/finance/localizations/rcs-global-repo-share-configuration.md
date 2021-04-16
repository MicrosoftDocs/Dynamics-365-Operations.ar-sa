---
title: مشاركة تكوينات ER في RCS/المستودع العمومي مع المؤسسات الخارجية
description: يشرح هذه الموضوع كيفية مشاركة تكوينات التقارير الإلكترونية (ER) في خدمات Microsoft Regulatory Configuration Services (RCS)/المستودع العمومي مباشرة مع مؤسسات خارجية.
author: JaneA07
ms.date: 05/04/2020
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
ms.openlocfilehash: ace62319bbfa38bcf4be7157882dd0c8989e25bc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838735"
---
# <a name="share-electronic-reporting-er-configurations-in-regulatory-configuration-services-rcs-global-repository-with-external-organizations"></a><span data-ttu-id="c5f6b-103">مشاركة تكوينات التقارير الإلكترونية (ER) في خدمات Regulatory Configuration Services (RCS)/المستودع العمومي مع مؤسسات خارجية.</span><span class="sxs-lookup"><span data-stu-id="c5f6b-103">Share Electronic reporting (ER) configurations in Regulatory Configuration Services (RCS) Global repository with external organizations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c5f6b-104">يمكنك استخدام خدمات Microsoft Regulatory Configuration Services (RCS) لمشاركة تكوينات التقارير الإلكترونية (ER) ثم نشرها إلى مؤسسات خارجية.</span><span class="sxs-lookup"><span data-stu-id="c5f6b-104">You can use Microsoft Regulatory Configuration Services (RCS) to share Electronic reporting (ER) configurations and then publish them to external organizations.</span></span>

<span data-ttu-id="c5f6b-105">توضح الإجراءات التالية كيف يمكن لمستخدم RCS مشاركه إصدار من تكوين ER الذي تم تكوينه في مثيل RCS مع مؤسسة خارجية.</span><span class="sxs-lookup"><span data-stu-id="c5f6b-105">The following procedures explain how an RCS user can share a version of an ER configuration that has been configured in an RCS instance with an external organization.</span></span> <span data-ttu-id="c5f6b-106">قبل إكمال هذه الإجراءات، يجب أن تستكمل أولا المتطلبات الأساسية التالية:</span><span class="sxs-lookup"><span data-stu-id="c5f6b-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="c5f6b-107">الوصول إلى مثيل RCS.</span><span class="sxs-lookup"><span data-stu-id="c5f6b-107">Access an RCS instance.</span></span>
- <span data-ttu-id="c5f6b-108">إنشاء موفر تكوين نشط.</span><span class="sxs-lookup"><span data-stu-id="c5f6b-108">Create an active configuration provider.</span></span> <span data-ttu-id="c5f6b-109">لمزيد من المعلومات، راجع [إنشاء موفري التكوين ووضع علامة عليهم كنشطين](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="c5f6b-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
- <span data-ttu-id="c5f6b-110">إنشاء إصدار جديد من تكوين ER وتحميله.</span><span class="sxs-lookup"><span data-stu-id="c5f6b-110">Create and upload a new version of an ER configuration.</span></span> <span data-ttu-id="c5f6b-111">لمزيد من المعلومات، راجع [إنشاء إصدار جديد من تكوين التقارير الإلكترونية (ER) وتحميله](rcs-global-repo-upload.md).</span><span class="sxs-lookup"><span data-stu-id="c5f6b-111">For more information, see [Create and upload a new version of an Electronic reporting (ER) configuration](rcs-global-repo-upload.md).</span></span>

<span data-ttu-id="c5f6b-112">يجب أيضا التأكد من أنه تم توفير بيئة RCS لشركك.</span><span class="sxs-lookup"><span data-stu-id="c5f6b-112">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="c5f6b-113">في تطبيق Finance and Operations، انتقل إلى **إدارة المؤسسات** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="c5f6b-113">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="c5f6b-114">في حالة عدم توفير بيئة RCS للشركة الخاصة بك، حدد **Regulatory services - التكوين الخارجي**، واتبع الإرشادات لتوفير بيئة.</span><span class="sxs-lookup"><span data-stu-id="c5f6b-114">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="c5f6b-115">إذا تم بالفعل توفير بيئة RCS لشركك، استخدم عنوان URL للصفحة للوصول إليه عن طريق تحديد خيار تسجيل الدخول.</span><span class="sxs-lookup"><span data-stu-id="c5f6b-115">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="verify-the-configuration-that-you-want-to-share"></a><span data-ttu-id="c5f6b-116">التحقق من التكوين الذي تريد مشاركته</span><span class="sxs-lookup"><span data-stu-id="c5f6b-116">Verify the configuration that you want to share</span></span>

<span data-ttu-id="c5f6b-117">اتبع الخطوات التالية للتحقق من تحميل التكوين الذي ترغب في مشاركته بالفعل إلى المستودع العمومي.</span><span class="sxs-lookup"><span data-stu-id="c5f6b-117">Follow these steps to verify that the configuration that you want to share has already been uploaded to the Global repository.</span></span>

1. <span data-ttu-id="c5f6b-118">في مساحة عمل **التقارير الإلكترونية**، حدد **المستودعات** الخاصة بموفر التكوين.</span><span class="sxs-lookup"><span data-stu-id="c5f6b-118">In the **Electronic reporting** workspace, select **Repositories** for your configuration provider.</span></span>

    ![موفرو التكوين](media/1_RCS_Repo_for_config_provider.JPG)

2. <span data-ttu-id="c5f6b-120">حدد **المستودع االعمومي** \> **فتح**.</span><span class="sxs-lookup"><span data-stu-id="c5f6b-120">Select **Global repository** \> **Open**.</span></span>
3. <span data-ttu-id="c5f6b-121">ابحث عن التكوين الذي تريد مشاركته.</span><span class="sxs-lookup"><span data-stu-id="c5f6b-121">Search for the configuration that you want to share.</span></span> <span data-ttu-id="c5f6b-122">يمكن استخدام حقل عامل التصفية لتضييق البحث.</span><span class="sxs-lookup"><span data-stu-id="c5f6b-122">You can use the filter field to narrow your search.</span></span> <span data-ttu-id="c5f6b-123">إذا لم تتمكن من العثور على التكوين في المستودع العمومي، فاتبع الخطوات الواردة في [إنشاء إصدار جديد من تكوين التقارير الإلكترونية (ER) وتحميله](rcs-global-repo-upload.md).</span><span class="sxs-lookup"><span data-stu-id="c5f6b-123">If you can't find the configuration in the Global repository, follow the steps in [Create and upload a new version of an Electronic reporting (ER) configuration](rcs-global-repo-upload.md).</span></span>

## <a name="share-er-configurations-with-external-organizations"></a><span data-ttu-id="c5f6b-124">مشاركة تكوينات ER مع المؤسسات الخارجية</span><span class="sxs-lookup"><span data-stu-id="c5f6b-124">Share ER configurations with external organizations</span></span>

<span data-ttu-id="c5f6b-125">بعد إنشاء تكوين تحت موفر التكوين الخاص بك، يمكنك مشاركته مباشرة مع المؤسسات الخارجية باستخدام علامة التبويب السريعة **مشاركة مع** في صفحة **مستودع التكوين العمومي**.</span><span class="sxs-lookup"><span data-stu-id="c5f6b-125">After a configuration has been created under your configuration provider, you can share it directly with external organizations by using the **Shared with** FastTab on the **Global configuration repository** page.</span></span>

1. <span data-ttu-id="c5f6b-126">في مساحة عمل **التقارير الإلكترونية**، حدد **المستودعات** الخاصة بموفر التكوين.</span><span class="sxs-lookup"><span data-stu-id="c5f6b-126">In the **Electronic reporting** workspace, select **Repositories** for your configuration provider.</span></span>
2. <span data-ttu-id="c5f6b-127">حدد **المستودع االعمومي** \> **فتح**.</span><span class="sxs-lookup"><span data-stu-id="c5f6b-127">Select **Global repository** \> **Open**.</span></span> 
3. <span data-ttu-id="c5f6b-128">تحديد التكوين الذي تريد مشاركته</span><span class="sxs-lookup"><span data-stu-id="c5f6b-128">Select the configuration that you want to share.</span></span>
4. <span data-ttu-id="c5f6b-129">في علامة التبويب السريعة **مشاركة مع**، حدد **المؤسسة**.</span><span class="sxs-lookup"><span data-stu-id="c5f6b-129">On the **Shared with** FastTab, select **Organization**.</span></span>

    ![علامة التبويب السريعة مشاركة مع](media/1_RCS_Repo_for_Share_with_org.JPG)

5. <span data-ttu-id="c5f6b-131">في مربع الحوار، أدخل اسم المجال للمؤسسة الخارجية، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c5f6b-131">In the dialog box, enter the domain name for the external organization, and then select **OK**.</span></span>

    ![مربع الحوار "مشاركة إصدار التكوين مع مؤسسة خارجية"](media/1_RCS_Repo_for_Share_with_form.JPG)

<span data-ttu-id="c5f6b-133">تتم مشاركة التكوين مع المؤسسة الخارجية ويكون متوفرا لهذه المؤسسة في المستودع العمومي.</span><span class="sxs-lookup"><span data-stu-id="c5f6b-133">The configuration is shared with the external organization and is available to that organization in the Global repository.</span></span> <span data-ttu-id="c5f6b-134">ومن هناك، يمكن استيرادها إلى مثيل المؤسسة لـ RCS أو إلى مثيلات تطبيقات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c5f6b-134">From there, it can be imported into the organization's instance of RCS or into its instances of Finance and Operations apps.</span></span>

6. <span data-ttu-id="c5f6b-135">لإلغاء مشاركة تكوين تمت مشاركته مسبقًا مع مؤسسة خارجية، حدد التكوين وانقر فوق **إلغاء المشاركة**، ثم حدد **موافق**</span><span class="sxs-lookup"><span data-stu-id="c5f6b-135">To unshare a configuration that has been previously shared with an external organization, select the configuration and click **Unshare**, and then select **OK**</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]