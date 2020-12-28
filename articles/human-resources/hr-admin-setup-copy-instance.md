---
title: نسخ مثيل
description: يمكنك استخدام Microsoft Dynamics Lifecycle Services (LCS) لنسخ قاعدة بيانات Microsoft Dynamics 365 Human Resources إلى بيئة وضع الحماية.
author: andreabichsel
manager: AnnBe
ms.date: 07/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 40ca0a4d9733fc2a163daa4ea1c27a3bfae6d3bf
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527827"
---
# <a name="copy-an-instance"></a><span data-ttu-id="69aae-103">نسخ مثيل</span><span class="sxs-lookup"><span data-stu-id="69aae-103">Copy an instance</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="69aae-104">يمكنك استخدام Microsoft Dynamics Lifecycle Services (LCS) لنسخ قاعدة بيانات Microsoft Dynamics 365 Human Resources إلى بيئة وضع الحماية.</span><span class="sxs-lookup"><span data-stu-id="69aae-104">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="69aae-105">إذا كان لديك بيئة وضع حماية أخرى، يمكنك أيضًا نسخ قاعدة البيانات من تلك البيئة إلى بيئة وضع حماية مستهدفة.</span><span class="sxs-lookup"><span data-stu-id="69aae-105">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="69aae-106">لنسخ مثيل، ضع التلميحات التالية في الاعتبار:</span><span class="sxs-lookup"><span data-stu-id="69aae-106">To copy an instance, keep the following tips in mind:</span></span>

- <span data-ttu-id="69aae-107">يجب أن يكون مثيل Human Resources الذي ترغب في استبداله بيئة وضع الحماية.</span><span class="sxs-lookup"><span data-stu-id="69aae-107">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="69aae-108">يجب أن تكون البيئات التي تقوم بالنسخ منها وإليها في نفس المنطقة.</span><span class="sxs-lookup"><span data-stu-id="69aae-108">The environments you're copying from and to must be in the same region.</span></span> <span data-ttu-id="69aae-109">لا يُمكنك النسخ عبر المناطق.</span><span class="sxs-lookup"><span data-stu-id="69aae-109">You can't copy across regions.</span></span>

- <span data-ttu-id="69aae-110">يجب أن تكون مسؤولًا في البيئة الهدف بحيث يُمكنك تسجيل الدخول إليها بعد نسخ المثيل.</span><span class="sxs-lookup"><span data-stu-id="69aae-110">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="69aae-111">عند نسخ قاعدة Human Resources، لا تقوم بنسخ العناصر (التطبيقات أو البيانات) المُضمنة في بيئة Microsoft Power Apps.</span><span class="sxs-lookup"><span data-stu-id="69aae-111">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft Power Apps environment.</span></span> <span data-ttu-id="69aae-112">للحصول على معلومات حول كيفية نسخ العناصر في بيئة Power Apps، راجع [نسخ بيئة ](https://docs.microsoft.com/power-platform/admin/copy-environment).</span><span class="sxs-lookup"><span data-stu-id="69aae-112">For information about how to copy elements in a Power Apps environment, see [Copy an environment](https://docs.microsoft.com/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="69aae-113">يجب أن تكون بيئة Power Apps التي تريد استبدالها بيئة وضع الحماية.</span><span class="sxs-lookup"><span data-stu-id="69aae-113">The Power Apps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="69aae-114">يجب أن تكون مسؤول مستأجر عمومي لتغيير بيئة انتاج Power Apps إلى بيئة حماية.</span><span class="sxs-lookup"><span data-stu-id="69aae-114">You must be a global tenant admin to change a Power Apps production environment to a sandbox environment.</span></span> <span data-ttu-id="69aae-115">لمزيد من المعلومات حول تغيير بيئة Power Apps، راجع [تبديل مثيل](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span><span class="sxs-lookup"><span data-stu-id="69aae-115">For more information about changing a Power Apps environment, see [Switch an instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span></span>

- <span data-ttu-id="69aae-116">إذا قمت بنسخ مثيل إلى بيئة الحماية الخاصة بك وترغب في دمج بيئة الحماية مع Common Data Service ، فمن ثم يجب عليك إعادة تطبيق الحقول المخصصة على كيانات Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="69aae-116">If you copy an instance into your sandbox environment and want to integrate your sandbox environment with Common Data Service, you must reapply custom fields to Common Data Service entities.</span></span> <span data-ttu-id="69aae-117">راجع [تطبيق الحقول المخصصة علي Common Data Service](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).</span><span class="sxs-lookup"><span data-stu-id="69aae-117">See [Apply custom fields to Common Data Service](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="69aae-118">تأثيرات نسخ قاعدة بيانات Human Resources</span><span class="sxs-lookup"><span data-stu-id="69aae-118">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="69aae-119">تحدث الأحداث التالية عندما تقوم بنسخ قاعدة بيانات Human Resources:</span><span class="sxs-lookup"><span data-stu-id="69aae-119">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="69aae-120">تؤدي عمليه النسخ إلى مسح قاعده البيانات الموجودة في البيئة الهدف.</span><span class="sxs-lookup"><span data-stu-id="69aae-120">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="69aae-121">بعد اكتمال عملية النسخ، لا يُمكنك استرجاع قاعدة البيانات الموجودة.</span><span class="sxs-lookup"><span data-stu-id="69aae-121">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="69aae-122">لن تكون البيئة الهدف متوفرة حتى اكتمال عملية النسخ.</span><span class="sxs-lookup"><span data-stu-id="69aae-122">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="69aae-123">لا يتم نسخ المستندات الموجودة في مخزن البيانات الثنائية الكبيرة الحجم لـ Microsoft Azure من بيئة إلى أخرى.</span><span class="sxs-lookup"><span data-stu-id="69aae-123">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="69aae-124">ونتيجة لذلك، لن يتم نسخ أي مستندات وقوالب مرفقة وسوف تظل في البيئة المصدر.</span><span class="sxs-lookup"><span data-stu-id="69aae-124">As a result, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="69aae-125">لن يكون جميع المستخدمين باستثناء المستخدم المسؤول وحسابات مستخدمين الخدمة الداخليين الأخرى متوفرة.</span><span class="sxs-lookup"><span data-stu-id="69aae-125">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="69aae-126">يُمكن للمستخدم المسؤول حذف البيانات أو جعلها مبهمة قبل السماح لمستخدمين آخرين العودة إلى النظام.</span><span class="sxs-lookup"><span data-stu-id="69aae-126">The Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="69aae-127">يجب على المستخدم المسؤول إجراء تغييرات التكوينات المطلوبة، مثل إعادة توصيل النقاط النهائية للتكامل إلى خدمات أو عناوين URL مُعينة.</span><span class="sxs-lookup"><span data-stu-id="69aae-127">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="69aae-128">نسخ قاعدة بيانات Human Resources</span><span class="sxs-lookup"><span data-stu-id="69aae-128">Copy the Human Resources database</span></span>

<span data-ttu-id="69aae-129">لإكمال هذه المهمة، يجب عليك أولًا نسخ مثيل، ثم تسجيل الدخول إلى مركز مسؤول Microsoft Power Platform لنسخ بيئة Power Apps الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="69aae-129">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your Power Apps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="69aae-130">عندما تقوم بنسخ مثيل، يتم مسح قاعدة البيانات في المثيل الهدف.</span><span class="sxs-lookup"><span data-stu-id="69aae-130">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="69aae-131">المثيل الهدف غير متوفر في أثناء هذه العملية.</span><span class="sxs-lookup"><span data-stu-id="69aae-131">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="69aae-132">قم بتسجيل الدخول إلى LCS، وحدد مشروع LCS الذي يحتوي على المثيل الذي ترغب في نسخه.</span><span class="sxs-lookup"><span data-stu-id="69aae-132">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="69aae-133">في مشروع LCS، حدد تجانب **"إدارة تطبيق Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="69aae-133">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="69aae-134">حدد المثيل المراد نسخه، ثم حدد **نسخ**.</span><span class="sxs-lookup"><span data-stu-id="69aae-134">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="69aae-135">في جزء المهام **نسخ مثيل**، حدد المثيل المراد استبداله، ثم حدد **نسخ**.</span><span class="sxs-lookup"><span data-stu-id="69aae-135">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="69aae-136">انتظر حتي يتم تحديث قيمة حقل **نسخ الحالة** إلى **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="69aae-136">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="69aae-137">حدد مثيلًا لاستبداله</span><span class="sxs-lookup"><span data-stu-id="69aae-137">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="69aae-138">حدد **Power Platform**، وقم بتسجيل الدخول إلى مركز مسؤول Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="69aae-138">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="69aae-139">حدد Power Platform</span><span class="sxs-lookup"><span data-stu-id="69aae-139">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="69aae-140">حدد بيئة Power Apps المراد نسخها، ثم حدد **نسخ**.</span><span class="sxs-lookup"><span data-stu-id="69aae-140">Select the Power Apps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="69aae-141">عند اكتمال عمليه النسخ ، قم بتسجيل الدخول إلى المثيل الهدف، وتمكين تكامل Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="69aae-141">When the copy process is completed, sign in to the target instance, and enable Common Data Service integration.</span></span> <span data-ttu-id="69aae-142">لمزيد من المعلومات والتعليمات، راجع [تكوين تكامل Common Data Service ](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span><span class="sxs-lookup"><span data-stu-id="69aae-142">For more information and instructions, see [Configure Common Data Service integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="69aae-143">عناصر البيانات والحالات</span><span class="sxs-lookup"><span data-stu-id="69aae-143">Data elements and statuses</span></span>

<span data-ttu-id="69aae-144">لا يتم نسخ عناصر البيانات التالية عندما تقوم بنسخ مثيل Human Resources:</span><span class="sxs-lookup"><span data-stu-id="69aae-144">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="69aae-145">عناوين البريد الكتروني في الجدول **LogisticsElectronicAddress**</span><span class="sxs-lookup"><span data-stu-id="69aae-145">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="69aae-146">سجل الوظيفة الدفعية في الجداول **BatchJobHistory** و **BatchHistory** و **BatchConstraintHistory**. </span><span class="sxs-lookup"><span data-stu-id="69aae-146">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="69aae-147">كلمة مرور البروتوكول البسيط لنقل رسائل البريد (SMTP) في جدول **SysEmailSMTPPassword**.</span><span class="sxs-lookup"><span data-stu-id="69aae-147">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="69aae-148">خادم ترحيل SMTP في الجدول **SysEmailParameters** </span><span class="sxs-lookup"><span data-stu-id="69aae-148">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="69aae-149">إعدادات إدارة الطباعة في جداول **PrintMgmtSettings** و **PrintMgmtDocInstance** </span><span class="sxs-lookup"><span data-stu-id="69aae-149">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="69aae-150">سجلات البيئة المُحددة في جداول **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, و **BatchServerGroup** </span><span class="sxs-lookup"><span data-stu-id="69aae-150">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="69aae-151">مرفقات المستندات في جدول DocuValue.</span><span class="sxs-lookup"><span data-stu-id="69aae-151">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="69aae-152">تتضمن هذه المرفقات أي قوالب Microsoft Office تم استبدالها في البيئة المصدر</span><span class="sxs-lookup"><span data-stu-id="69aae-152">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="69aae-153">سلسلة الاتصال في جدول **PersonnelIntegrationConfiguration** </span><span class="sxs-lookup"><span data-stu-id="69aae-153">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="69aae-154">لم يتم نسخ بعض هذه العناصر لأنها خاصة ببيئة معينة.</span><span class="sxs-lookup"><span data-stu-id="69aae-154">Some of these elements aren't copied because they're environment-specific.</span></span> <span data-ttu-id="69aae-155">تتضمن الأمثلة سجلات **BatchServerConfig** و **SysCorpNetPrinters**. </span><span class="sxs-lookup"><span data-stu-id="69aae-155">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="69aae-156">لا يتم نسخ العناصر الأخرى بسبب حجم تذاكر الدعم.</span><span class="sxs-lookup"><span data-stu-id="69aae-156">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="69aae-157">على سبيل المثال:</span><span class="sxs-lookup"><span data-stu-id="69aae-157">For example:</span></span>

- <span data-ttu-id="69aae-158">يجوز إرسال رسائل بريد إلكتروني مُكررة لأن SMTP لا يزال ممُكنًا في بيئة (حماية) اختبار قبول المستخدم.</span><span class="sxs-lookup"><span data-stu-id="69aae-158">Duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment.</span></span>

- <span data-ttu-id="69aae-159">قد يتم إرسال رسائل تكامل غير صحيحة لأن الوظائف الدفعية لا تزال ممكنة.</span><span class="sxs-lookup"><span data-stu-id="69aae-159">Invalid integration messages might be sent because batch jobs are still enabled.</span></span>

- <span data-ttu-id="69aae-160">قد يتم تمكين المستخدمين قبل أن يتمكن المسؤولون من تنفيذ إجراءات تنظيف ما بعد التحديث.</span><span class="sxs-lookup"><span data-stu-id="69aae-160">Users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="69aae-161">بالإضافة إلى ذلك، تتغير الحالات التالية عند نسخ مثيل:</span><span class="sxs-lookup"><span data-stu-id="69aae-161">Also, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="69aae-162">تم تعيين كافة المستخدمين باستثناء المسؤول إلى **مُعطل**.</span><span class="sxs-lookup"><span data-stu-id="69aae-162">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="69aae-163">يتم تعيين كافة الوظائف الدفعية، باستثناء بعض وظائف النظام، إلى **اقتطاع**.</span><span class="sxs-lookup"><span data-stu-id="69aae-163">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="69aae-164">مسؤول البيئة</span><span class="sxs-lookup"><span data-stu-id="69aae-164">Environment admin</span></span>

<span data-ttu-id="69aae-165">يتم استبدال كافة المستخدمين في بيئة الحماية الهدف، بما في ذلك المسؤولين، بالمستخدمين في البيئة المصدر.</span><span class="sxs-lookup"><span data-stu-id="69aae-165">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="69aae-166">قبل نسخ مثيل، تأكد من أنك مسؤول في البيئة المصدر.</span><span class="sxs-lookup"><span data-stu-id="69aae-166">Before you copy an instance, be sure that you're an Administrator in the source environment.</span></span> <span data-ttu-id="69aae-167">إذا لم تقم بذلك، فلن تتمكن من تسجيل الدخول إلى بيئة الحماية الهدف بعد اكتمال عملية النسخ.</span><span class="sxs-lookup"><span data-stu-id="69aae-167">If you aren't, you can't sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="69aae-168">يتم تعطيل كافة المستخدمين غير المسؤولين في بيئة الحماية الهدف لمنع تسجيلات الدخول غير المرعوب فيها في بيئة الحماية.</span><span class="sxs-lookup"><span data-stu-id="69aae-168">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="69aae-169">يمكن للمسؤولين إعادة تمكين المستخدمين عند الحاجة.</span><span class="sxs-lookup"><span data-stu-id="69aae-169">Administrators can reenable users if needed.</span></span>

## <a name="apply-custom-fields-to-common-data-service"></a><span data-ttu-id="69aae-170">تطبيق الحقول المخصصة على Common Data Service</span><span class="sxs-lookup"><span data-stu-id="69aae-170">Apply custom fields to Common Data Service</span></span>

<span data-ttu-id="69aae-171">إذا قمت بنسخ مثيل إلى بيئة الحماية الخاصة بك وترغب في دمج بيئة الحماية مع Common Data Service ، فمن ثم يجب عليك إعادة تطبيق الحقول المخصصة على كيانات Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="69aae-171">If you copy an instance into your sandbox environment and want to integrate your sandbox environment with Common Data Service, you must reapply custom fields to Common Data Service entities.</span></span>

<span data-ttu-id="69aae-172">بالنسبة لكل حقل مخصص معروض في كيانات Common Data Service ، قم بالخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="69aae-172">For each custom field that's exposed on Common Data Service entities, do the following steps:</span></span>

1. <span data-ttu-id="69aae-173">انتقل إلى الحقل المخصص، وحدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="69aae-173">Go to the custom field and select **Edit**.</span></span>

2. <span data-ttu-id="69aae-174">قم بإلغاء تحديد حقل **ممّكن** لكل كيان cdm_\* تم تمكين الحقل المخصص فيه. </span><span class="sxs-lookup"><span data-stu-id="69aae-174">Unselect the **Enabled** field for each cdm_\* entity that the custom field is enabled on.</span></span>

3. <span data-ttu-id="69aae-175">حدد **تطبيق التغييرات**.</span><span class="sxs-lookup"><span data-stu-id="69aae-175">Select **Apply Changes**.</span></span>

4. <span data-ttu-id="69aae-176">حدد **تحرير** مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="69aae-176">Select **Edit** again.</span></span>

5. <span data-ttu-id="69aae-177">حدد حقل **ممّكن** لكل كيان cdm_\* تم تمكين الحقل المخصص فيه. </span><span class="sxs-lookup"><span data-stu-id="69aae-177">Select the **Enabled** field for each cdm_\* entity that the custom field is enabled on.</span></span>

6. <span data-ttu-id="69aae-178">حدد **تطبيق التغييرات** مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="69aae-178">Select **Apply Changes** again.</span></span>

<span data-ttu-id="69aae-179">تطالبك عمليات إلغاء التحديد وتطبيق التغييرات وإعادة التحديد وإعادة تطبيق التغييرات تحديث المخطط في Common Data Service لتضمين الحقول المخصصة.</span><span class="sxs-lookup"><span data-stu-id="69aae-179">The process of unselecting, applying changes, reselecting, and reapplying changes prompts the schema to update in Common Data Service to include the custom fields.</span></span>

<span data-ttu-id="69aae-180">لمزيد من المعلومات حول الحقول المخصصة، راجع [‏‫إنشاء حقول مخصصة والعمل باستخدامها‬](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/user-defined-fields).</span><span class="sxs-lookup"><span data-stu-id="69aae-180">For more information about custom fields, see [Create and work with custom fields](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/user-defined-fields).</span></span>

## <a name="see-also"></a><span data-ttu-id="69aae-181">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="69aae-181">See also</span></span>

[<span data-ttu-id="69aae-182">تزويد Human Resources</span><span class="sxs-lookup"><span data-stu-id="69aae-182">Provision Human Resources</span></span>](hr-admin-setup-provision.md)</br>
[<span data-ttu-id="69aae-183">إزالة مثيل</span><span class="sxs-lookup"><span data-stu-id="69aae-183">Remove an instance</span></span>](hr-admin-setup-remove-instance.md)</br>
[<span data-ttu-id="69aae-184">تحديث العملية</span><span class="sxs-lookup"><span data-stu-id="69aae-184">Update process</span></span>](hr-admin-setup-update-process.md)

