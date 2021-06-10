---
title: نسخ مثيل
description: يمكنك استخدام Microsoft Dynamics Lifecycle Services (LCS) لنسخ قاعدة بيانات Microsoft Dynamics 365 Human Resources إلى بيئة وضع الحماية.
author: andreabichsel
ms.date: 07/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8961b7156f52e48dbfcf7efb14e50316e81fcfff
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053673"
---
# <a name="copy-an-instance"></a><span data-ttu-id="95c25-103">نسخ مثيل</span><span class="sxs-lookup"><span data-stu-id="95c25-103">Copy an instance</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="95c25-104">يمكنك استخدام Microsoft Dynamics Lifecycle Services (LCS) لنسخ قاعدة بيانات Microsoft Dynamics 365 Human Resources إلى بيئة وضع الحماية.</span><span class="sxs-lookup"><span data-stu-id="95c25-104">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="95c25-105">إذا كان لديك بيئة وضع حماية أخرى، يمكنك أيضًا نسخ قاعدة البيانات من تلك البيئة إلى بيئة وضع حماية مستهدفة.</span><span class="sxs-lookup"><span data-stu-id="95c25-105">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="95c25-106">لنسخ مثيل، ضع التلميحات التالية في الاعتبار:</span><span class="sxs-lookup"><span data-stu-id="95c25-106">To copy an instance, keep the following tips in mind:</span></span>

- <span data-ttu-id="95c25-107">يجب أن يكون مثيل Human Resources الذي ترغب في استبداله بيئة وضع الحماية.</span><span class="sxs-lookup"><span data-stu-id="95c25-107">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="95c25-108">يجب أن تكون البيئات التي تقوم بالنسخ منها وإليها في نفس المنطقة.</span><span class="sxs-lookup"><span data-stu-id="95c25-108">The environments you're copying from and to must be in the same region.</span></span> <span data-ttu-id="95c25-109">لا يُمكنك النسخ عبر المناطق.</span><span class="sxs-lookup"><span data-stu-id="95c25-109">You can't copy across regions.</span></span>

- <span data-ttu-id="95c25-110">يجب أن تكون مسؤولًا في البيئة الهدف بحيث يُمكنك تسجيل الدخول إليها بعد نسخ المثيل.</span><span class="sxs-lookup"><span data-stu-id="95c25-110">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="95c25-111">عند نسخ قاعدة Human Resources، لا تقوم بنسخ العناصر (التطبيقات أو البيانات) المُضمنة في بيئة Microsoft Power Apps.</span><span class="sxs-lookup"><span data-stu-id="95c25-111">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft Power Apps environment.</span></span> <span data-ttu-id="95c25-112">للحصول على معلومات حول كيفية نسخ العناصر في بيئة Power Apps، راجع [نسخ بيئة ](/power-platform/admin/copy-environment).</span><span class="sxs-lookup"><span data-stu-id="95c25-112">For information about how to copy elements in a Power Apps environment, see [Copy an environment](/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="95c25-113">يجب أن تكون بيئة Power Apps التي تريد استبدالها بيئة وضع الحماية.</span><span class="sxs-lookup"><span data-stu-id="95c25-113">The Power Apps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="95c25-114">يجب أن تكون مسؤول مستأجر عمومي لتغيير بيئة انتاج Power Apps إلى بيئة حماية.</span><span class="sxs-lookup"><span data-stu-id="95c25-114">You must be a global tenant admin to change a Power Apps production environment to a sandbox environment.</span></span> <span data-ttu-id="95c25-115">لمزيد من المعلومات حول تغيير بيئة Power Apps، راجع [تبديل مثيل](/dynamics365/admin/switch-instance).</span><span class="sxs-lookup"><span data-stu-id="95c25-115">For more information about changing a Power Apps environment, see [Switch an instance](/dynamics365/admin/switch-instance).</span></span>

- <span data-ttu-id="95c25-116">إذا قمت بنسخ مثيل إلى بيئة الحماية الخاصة بك وترغب في دمج بيئة الحماية مع Dataverse ، فمن ثم يجب عليك إعادة تطبيق الحقول المخصصة على جداول Dataverse.</span><span class="sxs-lookup"><span data-stu-id="95c25-116">If you copy an instance into your sandbox environment and want to integrate your sandbox environment with Dataverse, you must reapply custom fields to Dataverse tables.</span></span> <span data-ttu-id="95c25-117">راجع [تطبيق الحقول المخصصة علي Dataverse](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).</span><span class="sxs-lookup"><span data-stu-id="95c25-117">See [Apply custom fields to Dataverse](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="95c25-118">تأثيرات نسخ قاعدة بيانات Human Resources</span><span class="sxs-lookup"><span data-stu-id="95c25-118">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="95c25-119">تحدث الأحداث التالية عندما تقوم بنسخ قاعدة بيانات Human Resources:</span><span class="sxs-lookup"><span data-stu-id="95c25-119">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="95c25-120">تؤدي عمليه النسخ إلى مسح قاعده البيانات الموجودة في البيئة الهدف.</span><span class="sxs-lookup"><span data-stu-id="95c25-120">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="95c25-121">بعد اكتمال عملية النسخ، لا يُمكنك استرجاع قاعدة البيانات الموجودة.</span><span class="sxs-lookup"><span data-stu-id="95c25-121">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="95c25-122">لن تكون البيئة الهدف متوفرة حتى اكتمال عملية النسخ.</span><span class="sxs-lookup"><span data-stu-id="95c25-122">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="95c25-123">لا يتم نسخ المستندات الموجودة في مخزن البيانات الثنائية الكبيرة الحجم لـ Microsoft Azure من بيئة إلى أخرى.</span><span class="sxs-lookup"><span data-stu-id="95c25-123">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="95c25-124">ونتيجة لذلك، لن يتم نسخ أي مستندات وقوالب مرفقة وسوف تظل في البيئة المصدر.</span><span class="sxs-lookup"><span data-stu-id="95c25-124">As a result, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="95c25-125">لن يكون جميع المستخدمين باستثناء المستخدم المسؤول وحسابات مستخدمين الخدمة الداخليين الأخرى متوفرة.</span><span class="sxs-lookup"><span data-stu-id="95c25-125">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="95c25-126">يُمكن للمستخدم المسؤول حذف البيانات أو جعلها مبهمة قبل السماح لمستخدمين آخرين العودة إلى النظام.</span><span class="sxs-lookup"><span data-stu-id="95c25-126">The Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="95c25-127">يجب على المستخدم المسؤول إجراء تغييرات التكوينات المطلوبة، مثل إعادة توصيل النقاط النهائية للتكامل إلى خدمات أو عناوين URL مُعينة.</span><span class="sxs-lookup"><span data-stu-id="95c25-127">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="95c25-128">نسخ قاعدة بيانات Human Resources</span><span class="sxs-lookup"><span data-stu-id="95c25-128">Copy the Human Resources database</span></span>

<span data-ttu-id="95c25-129">لإكمال هذه المهمة، يجب عليك أولًا نسخ مثيل، ثم تسجيل الدخول إلى مركز مسؤول Microsoft Power Platform لنسخ بيئة Power Apps الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="95c25-129">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your Power Apps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="95c25-130">عندما تقوم بنسخ مثيل، يتم مسح قاعدة البيانات في المثيل الهدف.</span><span class="sxs-lookup"><span data-stu-id="95c25-130">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="95c25-131">المثيل الهدف غير متوفر في أثناء هذه العملية.</span><span class="sxs-lookup"><span data-stu-id="95c25-131">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="95c25-132">قم بتسجيل الدخول إلى LCS، وحدد مشروع LCS الذي يحتوي على المثيل الذي ترغب في نسخه.</span><span class="sxs-lookup"><span data-stu-id="95c25-132">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="95c25-133">في مشروع LCS، حدد تجانب **"إدارة تطبيق Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="95c25-133">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="95c25-134">حدد المثيل المراد نسخه، ثم حدد **نسخ**.</span><span class="sxs-lookup"><span data-stu-id="95c25-134">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="95c25-135">في جزء المهام **نسخ مثيل**، حدد المثيل المراد استبداله، ثم حدد **نسخ**.</span><span class="sxs-lookup"><span data-stu-id="95c25-135">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="95c25-136">انتظر حتي يتم تحديث قيمة حقل **نسخ الحالة** إلى **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="95c25-136">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="95c25-137">حدد مثيلًا لاستبداله</span><span class="sxs-lookup"><span data-stu-id="95c25-137">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="95c25-138">حدد **Power Platform**، وقم بتسجيل الدخول إلى مركز مسؤول Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="95c25-138">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="95c25-139">حدد Power Platform</span><span class="sxs-lookup"><span data-stu-id="95c25-139">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="95c25-140">حدد بيئة Power Apps المراد نسخها، ثم حدد **نسخ**.</span><span class="sxs-lookup"><span data-stu-id="95c25-140">Select the Power Apps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="95c25-141">عند اكتمال عمليه النسخ ، قم بتسجيل الدخول إلى المثيل الهدف، وتمكين تكامل Dataverse.</span><span class="sxs-lookup"><span data-stu-id="95c25-141">When the copy process is completed, sign in to the target instance, and enable Dataverse integration.</span></span> <span data-ttu-id="95c25-142">لمزيد من المعلومات والتعليمات، راجع [تكوين تكامل Dataverse ](./hr-admin-integration-common-data-service.md).</span><span class="sxs-lookup"><span data-stu-id="95c25-142">For more information and instructions, see [Configure Dataverse integration](./hr-admin-integration-common-data-service.md).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="95c25-143">عناصر البيانات والحالات</span><span class="sxs-lookup"><span data-stu-id="95c25-143">Data elements and statuses</span></span>

<span data-ttu-id="95c25-144">لا يتم نسخ عناصر البيانات التالية عندما تقوم بنسخ مثيل Human Resources:</span><span class="sxs-lookup"><span data-stu-id="95c25-144">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="95c25-145">عناوين البريد الكتروني في الجدول **LogisticsElectronicAddress**</span><span class="sxs-lookup"><span data-stu-id="95c25-145">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="95c25-146">سجل الوظيفة الدفعية في الجداول **BatchJobHistory** و **BatchHistory** و **BatchConstraintHistory**. </span><span class="sxs-lookup"><span data-stu-id="95c25-146">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="95c25-147">كلمة مرور البروتوكول البسيط لنقل رسائل البريد (SMTP) في جدول **SysEmailSMTPPassword**.</span><span class="sxs-lookup"><span data-stu-id="95c25-147">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="95c25-148">خادم ترحيل SMTP في الجدول **SysEmailParameters** </span><span class="sxs-lookup"><span data-stu-id="95c25-148">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="95c25-149">إعدادات إدارة الطباعة في جداول **PrintMgmtSettings** و **PrintMgmtDocInstance** </span><span class="sxs-lookup"><span data-stu-id="95c25-149">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="95c25-150">سجلات البيئة المُحددة في جداول **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, و **BatchServerGroup** </span><span class="sxs-lookup"><span data-stu-id="95c25-150">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="95c25-151">مرفقات المستندات في جدول DocuValue.</span><span class="sxs-lookup"><span data-stu-id="95c25-151">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="95c25-152">تتضمن هذه المرفقات أي قوالب Microsoft Office تم استبدالها في البيئة المصدر</span><span class="sxs-lookup"><span data-stu-id="95c25-152">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="95c25-153">سلسلة الاتصال في جدول **PersonnelIntegrationConfiguration** </span><span class="sxs-lookup"><span data-stu-id="95c25-153">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="95c25-154">لم يتم نسخ بعض هذه العناصر لأنها خاصة ببيئة معينة.</span><span class="sxs-lookup"><span data-stu-id="95c25-154">Some of these elements aren't copied because they're environment-specific.</span></span> <span data-ttu-id="95c25-155">تتضمن الأمثلة سجلات **BatchServerConfig** و **SysCorpNetPrinters**. </span><span class="sxs-lookup"><span data-stu-id="95c25-155">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="95c25-156">لا يتم نسخ العناصر الأخرى بسبب حجم تذاكر الدعم.</span><span class="sxs-lookup"><span data-stu-id="95c25-156">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="95c25-157">على سبيل المثال:</span><span class="sxs-lookup"><span data-stu-id="95c25-157">For example:</span></span>

- <span data-ttu-id="95c25-158">يجوز إرسال رسائل بريد إلكتروني مُكررة لأن SMTP لا يزال ممُكنًا في بيئة (حماية) اختبار قبول المستخدم.</span><span class="sxs-lookup"><span data-stu-id="95c25-158">Duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment.</span></span>

- <span data-ttu-id="95c25-159">قد يتم إرسال رسائل تكامل غير صحيحة لأن الوظائف الدفعية لا تزال ممكنة.</span><span class="sxs-lookup"><span data-stu-id="95c25-159">Invalid integration messages might be sent because batch jobs are still enabled.</span></span>

- <span data-ttu-id="95c25-160">قد يتم تمكين المستخدمين قبل أن يتمكن المسؤولون من تنفيذ إجراءات تنظيف ما بعد التحديث.</span><span class="sxs-lookup"><span data-stu-id="95c25-160">Users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="95c25-161">بالإضافة إلى ذلك، تتغير الحالات التالية عند نسخ مثيل:</span><span class="sxs-lookup"><span data-stu-id="95c25-161">Also, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="95c25-162">تم تعيين كافة المستخدمين باستثناء المسؤول إلى **مُعطل**.</span><span class="sxs-lookup"><span data-stu-id="95c25-162">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="95c25-163">يتم تعيين كافة الوظائف الدفعية، باستثناء بعض وظائف النظام، إلى **اقتطاع**.</span><span class="sxs-lookup"><span data-stu-id="95c25-163">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="95c25-164">مسؤول البيئة</span><span class="sxs-lookup"><span data-stu-id="95c25-164">Environment admin</span></span>

<span data-ttu-id="95c25-165">يتم استبدال كافة المستخدمين في بيئة الحماية الهدف، بما في ذلك المسؤولين، بالمستخدمين في البيئة المصدر.</span><span class="sxs-lookup"><span data-stu-id="95c25-165">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="95c25-166">قبل نسخ مثيل، تأكد من أنك مسؤول في البيئة المصدر.</span><span class="sxs-lookup"><span data-stu-id="95c25-166">Before you copy an instance, be sure that you're an Administrator in the source environment.</span></span> <span data-ttu-id="95c25-167">إذا لم تقم بذلك، فلن تتمكن من تسجيل الدخول إلى بيئة الحماية الهدف بعد اكتمال عملية النسخ.</span><span class="sxs-lookup"><span data-stu-id="95c25-167">If you aren't, you can't sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="95c25-168">يتم تعطيل كافة المستخدمين غير المسؤولين في بيئة الحماية الهدف لمنع تسجيلات الدخول غير المرعوب فيها في بيئة الحماية.</span><span class="sxs-lookup"><span data-stu-id="95c25-168">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="95c25-169">يمكن للمسؤولين إعادة تمكين المستخدمين عند الحاجة.</span><span class="sxs-lookup"><span data-stu-id="95c25-169">Administrators can reenable users if needed.</span></span>

## <a name="apply-custom-fields-to-dataverse"></a><span data-ttu-id="95c25-170">تطبيق الحقول المخصصة على Dataverse</span><span class="sxs-lookup"><span data-stu-id="95c25-170">Apply custom fields to Dataverse</span></span>

<span data-ttu-id="95c25-171">إذا قمت بنسخ مثيل إلى بيئة الحماية الخاصة بك وترغب في دمج بيئة الحماية مع Dataverse ، فمن ثم يجب عليك إعادة تطبيق الحقول المخصصة على جداول Dataverse.</span><span class="sxs-lookup"><span data-stu-id="95c25-171">If you copy an instance into your sandbox environment and want to integrate your sandbox environment with Dataverse, you must reapply custom fields to Dataverse tables.</span></span>

<span data-ttu-id="95c25-172">بالنسبة لكل حقل مخصص معروض في جداول Dataverse، قم بالخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="95c25-172">For each custom field that's exposed on Dataverse tables, do the following steps:</span></span>

1. <span data-ttu-id="95c25-173">انتقل إلى الحقل المخصص، وحدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="95c25-173">Go to the custom field and select **Edit**.</span></span>

2. <span data-ttu-id="95c25-174">قم بإلغاء تحديد حقل **ممّكن** لكل كيان cdm_\* تم تمكين الحقل المخصص فيه. </span><span class="sxs-lookup"><span data-stu-id="95c25-174">Unselect the **Enabled** field for each cdm_\* entity that the custom field is enabled on.</span></span>

3. <span data-ttu-id="95c25-175">حدد **تطبيق التغييرات**.</span><span class="sxs-lookup"><span data-stu-id="95c25-175">Select **Apply Changes**.</span></span>

4. <span data-ttu-id="95c25-176">حدد **تحرير** مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="95c25-176">Select **Edit** again.</span></span>

5. <span data-ttu-id="95c25-177">حدد حقل **ممّكن** لكل كيان cdm_\* تم تمكين الحقل المخصص فيه. </span><span class="sxs-lookup"><span data-stu-id="95c25-177">Select the **Enabled** field for each cdm_\* entity that the custom field is enabled on.</span></span>

6. <span data-ttu-id="95c25-178">حدد **تطبيق التغييرات** مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="95c25-178">Select **Apply Changes** again.</span></span>

<span data-ttu-id="95c25-179">تطالبك عمليات إلغاء التحديد وتطبيق التغييرات وإعادة التحديد وإعادة تطبيق التغييرات تحديث المخطط في Dataverse لتضمين الحقول المخصصة.</span><span class="sxs-lookup"><span data-stu-id="95c25-179">The process of unselecting, applying changes, reselecting, and reapplying changes prompts the schema to update in Dataverse to include the custom fields.</span></span>

<span data-ttu-id="95c25-180">لمزيد من المعلومات حول الحقول المخصصة، راجع [‏‫إنشاء حقول مخصصة والعمل باستخدامها‬](../fin-ops-core/fin-ops/get-started/user-defined-fields.md).</span><span class="sxs-lookup"><span data-stu-id="95c25-180">For more information about custom fields, see [Create and work with custom fields](../fin-ops-core/fin-ops/get-started/user-defined-fields.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="95c25-181">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="95c25-181">See also</span></span>

[<span data-ttu-id="95c25-182">تزويد Human Resources</span><span class="sxs-lookup"><span data-stu-id="95c25-182">Provision Human Resources</span></span>](hr-admin-setup-provision.md)</br>
[<span data-ttu-id="95c25-183">إزالة مثيل</span><span class="sxs-lookup"><span data-stu-id="95c25-183">Remove an instance</span></span>](hr-admin-setup-remove-instance.md)</br>
[<span data-ttu-id="95c25-184">تحديث العملية</span><span class="sxs-lookup"><span data-stu-id="95c25-184">Update process</span></span>](hr-admin-setup-update-process.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]