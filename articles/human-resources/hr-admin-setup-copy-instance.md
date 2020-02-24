---
title: نسخ مثيل
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0bbe325edb65cad0c1912e0a6ade559e5675dc58
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2020
ms.locfileid: "3007912"
---
# <a name="copy-an-instance"></a><span data-ttu-id="3bb62-102">نسخ مثيل</span><span class="sxs-lookup"><span data-stu-id="3bb62-102">Copy an instance</span></span>

<span data-ttu-id="3bb62-103">يمكنك استخدام Microsoft Dynamics Lifecycle Services (LCS) لنسخ قاعدة بيانات Microsoft Dynamics 365 Human Resources إلى بيئة وضع الحماية.</span><span class="sxs-lookup"><span data-stu-id="3bb62-103">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="3bb62-104">إذا كان لديك بيئة وضع حماية أخرى ، يمكنك أيضًا نسخ قاعدة البيانات من تلك البيئة إلى بيئة وضع حماية مستهدفة.</span><span class="sxs-lookup"><span data-stu-id="3bb62-104">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="3bb62-105">لنسخ مثيل، تحتاج إلى التأكد من التالي:</span><span class="sxs-lookup"><span data-stu-id="3bb62-105">To copy an instance, you need to ensure the following:</span></span>

- <span data-ttu-id="3bb62-106">يجب أن يكون مثيل Human Resources الذي ترغب في استبداله بيئة وضع الحماية.</span><span class="sxs-lookup"><span data-stu-id="3bb62-106">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="3bb62-107">يجب أن تكون البيئات التي تقوم بالنسخ منها وإليها في نفس المنطقة.</span><span class="sxs-lookup"><span data-stu-id="3bb62-107">The environments you are copying from and to must be in the same region.</span></span> <span data-ttu-id="3bb62-108">لا يُمكنك النسخ عبر المناطق.</span><span class="sxs-lookup"><span data-stu-id="3bb62-108">You can't copy across regions.</span></span>

- <span data-ttu-id="3bb62-109">يجب أن تكون مسؤولًا في البيئة الهدف بحيث يُمكنك تسجيل الدخول إليها بعد نسخ المثيل.</span><span class="sxs-lookup"><span data-stu-id="3bb62-109">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="3bb62-110">عند نسخ قاعدة Human Resources، لا تقوم بنسخ العناصر (التطبيقات أو البيانات) المُضمنة في بيئة Microsoft PowerApps.</span><span class="sxs-lookup"><span data-stu-id="3bb62-110">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft PowerApps environment.</span></span> <span data-ttu-id="3bb62-111">للحصول على معلومات حول كيفية نسخ العناصر في بيئة PowerApps ، راجع [نسخ بيئة ](https://docs.microsoft.com/power-platform/admin/copy-environment).</span><span class="sxs-lookup"><span data-stu-id="3bb62-111">For information about how to copy elements in a PowerApps environment, see [Copy an environment](https://docs.microsoft.com/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="3bb62-112">يجب أن تكون بيئة PowerApps التي تريد استبدالها بيئة وضع الحماية.</span><span class="sxs-lookup"><span data-stu-id="3bb62-112">The PowerApps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="3bb62-113">يجب أن تكون مسؤول مستأجر عمومي لتغيير بيئة انتاج PowerApps إلى بيئة حماية.</span><span class="sxs-lookup"><span data-stu-id="3bb62-113">You must be a global tenant admin to change a PowerApps production environment to a sandbox environment.</span></span> <span data-ttu-id="3bb62-114">لمزيد من المعلومات حول تغيير بيئة PowerApps، راجع [تبديل مثيل](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span><span class="sxs-lookup"><span data-stu-id="3bb62-114">For more information about changing a PowerApps environment, see [Switch an instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="3bb62-115">تأثيرات نسخ قاعدة بيانات Human Resources</span><span class="sxs-lookup"><span data-stu-id="3bb62-115">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="3bb62-116">تحدث الأحداث التالية عندما تقوم بنسخ قاعدة بيانات Human Resources:</span><span class="sxs-lookup"><span data-stu-id="3bb62-116">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="3bb62-117">تؤدي عمليه النسخ إلى مسح قاعده البيانات الموجودة في البيئة الهدف.</span><span class="sxs-lookup"><span data-stu-id="3bb62-117">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="3bb62-118">بعد اكتمال عملية النسخ، لا يُمكنك استرجاع قاعدة البيانات الموجودة.</span><span class="sxs-lookup"><span data-stu-id="3bb62-118">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="3bb62-119">لن تكون البيئة الهدف متوفرة حتى اكتمال عملية النسخ.</span><span class="sxs-lookup"><span data-stu-id="3bb62-119">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="3bb62-120">لا يتم نسخ المستندات الموجودة في مخزن البيانات الثنائية الكبيرة الحجم لـ Microsoft Azure من بيئة إلى أخرى.</span><span class="sxs-lookup"><span data-stu-id="3bb62-120">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="3bb62-121">وبالتالي، لن يتم نسخ أي مستندات وقوالب مرفقة وسوف تظل في البيئة المصدر.</span><span class="sxs-lookup"><span data-stu-id="3bb62-121">Therefore, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="3bb62-122">لن يكون جميع المستخدمين باستثناء المستخدم المسؤول وحسابات مستخدمين الخدمة الداخليين الأخرى متوفرة.</span><span class="sxs-lookup"><span data-stu-id="3bb62-122">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="3bb62-123">بالتالي، يُمكن للمستخدم المسؤول حذف البيانات أو جعلها مبهمة قبل السماح لمستخدمين آخرين العودة إلى النظام.</span><span class="sxs-lookup"><span data-stu-id="3bb62-123">Therefore, the Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="3bb62-124">يجب على المستخدم المسؤول إجراء تغييرات التكوينات المطلوبة، مثل إعادة توصيل النقاط النهائية للتكامل إلى خدمات أو عناوين URL مُعينة.</span><span class="sxs-lookup"><span data-stu-id="3bb62-124">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="3bb62-125">نسخ قاعدة بيانات Human Resources</span><span class="sxs-lookup"><span data-stu-id="3bb62-125">Copy the Human Resources database</span></span>

<span data-ttu-id="3bb62-126">لإكمال هذه المهمة، يجب عليك أولًا نسخ مثيل، ثم تسجيل الدخول إلى مركز مسؤول Microsoft Power Platform لنسخ بيئة PowerApps الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="3bb62-126">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your PowerApps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="3bb62-127">عندما تقوم بنسخ مثيل، يتم مسح قاعدة البيانات في المثيل الهدف.</span><span class="sxs-lookup"><span data-stu-id="3bb62-127">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="3bb62-128">المثيل الهدف غير متوفر في أثناء هذه العملية.</span><span class="sxs-lookup"><span data-stu-id="3bb62-128">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="3bb62-129">قم بتسجيل الدخول إلى LCS، وحدد مشروع LCS الذي يحتوي على المثيل الذي ترغب في نسخه.</span><span class="sxs-lookup"><span data-stu-id="3bb62-129">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="3bb62-130">في مشروع LCS، حدد تجانب **"إدارة تطبيق Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="3bb62-130">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="3bb62-131">حدد المثيل المراد نسخه ، ثم حدد **نسخ**.</span><span class="sxs-lookup"><span data-stu-id="3bb62-131">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="3bb62-132">في جزء المهام **نسخ مثيل** ، حدد المثيل المراد استبداله، ثم حدد **نسخ**.</span><span class="sxs-lookup"><span data-stu-id="3bb62-132">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="3bb62-133">انتظر حتي يتم تحديث قيمة حقل **نسخ الحالة** إلى **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="3bb62-133">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="3bb62-134">حدد مثيلًا لاستبداله</span><span class="sxs-lookup"><span data-stu-id="3bb62-134">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="3bb62-135">حدد **Power Platform**، وقم بتسجيل الدخول إلى مركز مسؤول Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="3bb62-135">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="3bb62-136">حدد Power Platform</span><span class="sxs-lookup"><span data-stu-id="3bb62-136">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="3bb62-137">حدد بيئة PowerApps المراد نسخها، ثم حدد **نسخ**.</span><span class="sxs-lookup"><span data-stu-id="3bb62-137">Select the PowerApps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="3bb62-138">عند اكتمال عمليه النسخ ، قم بتسجيل الدخول إلى المثيل الهدف، وتمكين تكامل Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3bb62-138">When the copy process is completed, sign in to the target instance, and enable Common Data Service integration.</span></span> <span data-ttu-id="3bb62-139">لمزيد من المعلومات والتعليمات، راجع [تكوين تكامل Common Data Service ](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span><span class="sxs-lookup"><span data-stu-id="3bb62-139">For more information and instructions, see [Configure Common Data Service integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="3bb62-140">عناصر البيانات والحالات</span><span class="sxs-lookup"><span data-stu-id="3bb62-140">Data elements and statuses</span></span>

<span data-ttu-id="3bb62-141">لا يتم نسخ عناصر البيانات التالية عندما تقوم بنسخ مثيل Human Resources:</span><span class="sxs-lookup"><span data-stu-id="3bb62-141">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="3bb62-142">عناوين البريد الكتروني في الجدول **LogisticsElectronicAddress**</span><span class="sxs-lookup"><span data-stu-id="3bb62-142">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="3bb62-143">سجل الوظيفة الدفعية في الجداول **BatchJobHistory** و **BatchHistory** و **BatchConstraintHistory**. </span><span class="sxs-lookup"><span data-stu-id="3bb62-143">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="3bb62-144">كلمة مرور البروتوكول البسيط لنقل رسائل البريد (SMTP) في جدول **SysEmailSMTPPassword**.</span><span class="sxs-lookup"><span data-stu-id="3bb62-144">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="3bb62-145">خادم ترحيل SMTP في الجدول **SysEmailParameters** </span><span class="sxs-lookup"><span data-stu-id="3bb62-145">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="3bb62-146">إعدادات إدارة الطباعة في جداول **PrintMgmtSettings** و **PrintMgmtDocInstance** </span><span class="sxs-lookup"><span data-stu-id="3bb62-146">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="3bb62-147">سجلات البيئة المُحددة في جداول **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, و **BatchServerGroup** </span><span class="sxs-lookup"><span data-stu-id="3bb62-147">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="3bb62-148">مرفقات المستندات في جدول DocuValue.</span><span class="sxs-lookup"><span data-stu-id="3bb62-148">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="3bb62-149">تتضمن هذه المرفقات أي قوالب Microsoft Office تم استبدالها في البيئة المصدر</span><span class="sxs-lookup"><span data-stu-id="3bb62-149">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="3bb62-150">سلسلة الاتصال في جدول **PersonnelIntegrationConfiguration** </span><span class="sxs-lookup"><span data-stu-id="3bb62-150">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="3bb62-151">لم يتم نسخ بعض هذه العناصر لأنها خاصة ببيئة معينة.</span><span class="sxs-lookup"><span data-stu-id="3bb62-151">Some of these elements aren't copied because they are environment-specific.</span></span> <span data-ttu-id="3bb62-152">تتضمن الأمثلة سجلات **BatchServerConfig** و **SysCorpNetPrinters**. </span><span class="sxs-lookup"><span data-stu-id="3bb62-152">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="3bb62-153">لا يتم نسخ العناصر الأخرى بسبب حجم تذاكر الدعم.</span><span class="sxs-lookup"><span data-stu-id="3bb62-153">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="3bb62-154">على سبيل المثال، يجوز إرسال رسائل البريد الإلكتروني المُكررة لأن SMTP لا يزال مُمكننًا في بيئة اختبار قبول المستخدم (الحماية)، وقد يتم إرسال رسائل تكامل غير صالحة لأن الوظائف الدفعية لا تزال ممكنة، ويجوز تمكين المستخدمين قبل أن يتمكن المسؤولون من تنفيذ إجراءات تنظيف ما بعد التحديث.</span><span class="sxs-lookup"><span data-stu-id="3bb62-154">For example, duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment, invalid integration messages might be sent because batch jobs are still enabled, and users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="3bb62-155">بالإضافة إلى ذلك، تتغير الحالات التالية عند نسخ مثيل:</span><span class="sxs-lookup"><span data-stu-id="3bb62-155">In addition, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="3bb62-156">تم تعيين كافة المستخدمين باستثناء المسؤول إلى **مُعطل**.</span><span class="sxs-lookup"><span data-stu-id="3bb62-156">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="3bb62-157">يتم تعيين كافة الوظائف الدفعية، باستثناء بعض وظائف النظام، إلى **اقتطاع**.</span><span class="sxs-lookup"><span data-stu-id="3bb62-157">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="3bb62-158">مسؤول البيئة</span><span class="sxs-lookup"><span data-stu-id="3bb62-158">Environment admin</span></span>

<span data-ttu-id="3bb62-159">يتم استبدال كافة المستخدمين في بيئة الحماية الهدف، بما في ذلك المسؤولين، بالمستخدمين في البيئة المصدر.</span><span class="sxs-lookup"><span data-stu-id="3bb62-159">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="3bb62-160">قبل نسخ مثيل، تأكد من أنك مسؤول في البيئة الهدف.</span><span class="sxs-lookup"><span data-stu-id="3bb62-160">Before you copy an instance, be sure that you're an Administrator in the target environment.</span></span> <span data-ttu-id="3bb62-161">إذا لم تقم بذلك، فلن تتمكن من تسجيل الدخول إلى بيئة الحماية الهدف بعد اكتمال عملية النسخ.</span><span class="sxs-lookup"><span data-stu-id="3bb62-161">If you aren't, you won't be able to sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="3bb62-162">يتم تعطيل كافة المستخدمين غير المسؤولين في بيئة الحماية الهدف لمنع تسجيلات الدخول غير المرعوب فيها في بيئة الحماية.</span><span class="sxs-lookup"><span data-stu-id="3bb62-162">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="3bb62-163">يمكن للمسؤولين إعادة تمكين المستخدمين عند الحاجة.</span><span class="sxs-lookup"><span data-stu-id="3bb62-163">Administrators can reenable users if needed.</span></span>
