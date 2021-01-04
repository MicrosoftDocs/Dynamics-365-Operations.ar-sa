---
title: استكشاف المشاكل وإصلاحها في المزامنة المباشرة
description: يوفر هذا الموضوع استكشاف الأخطاء وإصلاحها الذي يمكن أن يساعدك في إصلاح مشكلات المزامنة المباشرة.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: ca12759096bd1bafda0a5eee18287a694083db69
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685553"
---
# <a name="troubleshoot-live-synchronization-issues"></a><span data-ttu-id="51589-103">استكشاف المشاكل وإصلاحها في المزامنة المباشرة</span><span class="sxs-lookup"><span data-stu-id="51589-103">Troubleshoot live synchronization issues</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="51589-104">يوفر هذا الموضوع معلومات حول استكشاف أخطاء تكامل الكتابة الثنائية وإصلاحها بين تطبيقات Finance and Operations وDataverse.</span><span class="sxs-lookup"><span data-stu-id="51589-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="51589-105">على وجه التحديد، يوفر هذا الموضوع استكشاف الأخطاء وإصلاحها الذي يمكن أن يساعدك في إصلاح مشكلات المزامنة المباشرة.</span><span class="sxs-lookup"><span data-stu-id="51589-105">Specifically, it provides information that can help you fix issues with live synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="51589-106">قد تتطلب بعض المشكلات التي يتناولها هذا الموضوع إما دور إدارة النظام أو بيانات اعتماد مسؤول مستأجر  Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="51589-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="51589-107">يوضح القسم الخاص بكل مشكلة ما إذا كانت هناك حاجة إلى دور محدد أو بيانات اعتماد.</span><span class="sxs-lookup"><span data-stu-id="51589-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-row-in-a-finance-and-operations-app"></a><span data-ttu-id="51589-108">تطرح المزامنة المباشرة خطأ ممنوع 403 عند إنشاء صف في تطبيق Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="51589-108">Live synchronization throws a 403 Forbidden error when you create a row in a Finance and Operations app</span></span>

<span data-ttu-id="51589-109">قد تظهر رسالة الخطأ التالية عند إنشاء صف في تطبيق Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="51589-109">You might receive the following error message when you create a row in a Finance and Operations app:</span></span>

<span data-ttu-id="51589-110">*\[{\\"الخطأ\\":{\\"الكود\\":\\"0x80072560\\"،\\"الرسالة\\":\\"المستخدم ليس عضوا في المؤسسة.\\"}}\]، أرجع الخادم البعيد الخطأ: (403) ممنوع."}}".*</span><span class="sxs-lookup"><span data-stu-id="51589-110">*\[{\\"error\\":{\\"code\\":\\"0x80072560\\",\\"message\\":\\"The user is not a member of the organization.\\"}}\], The remote server returned an error: (403) Forbidden."}}".*</span></span>

<span data-ttu-id="51589-111">لإصلاح هذه المشكلة، اتبع الخطوات الموجودة في [متطلبات النظام والمتطلبات الأساسية](requirements-and-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="51589-111">To fix the issue, follow the steps in [System requirements and prerequisites](requirements-and-prerequisites.md).</span></span> <span data-ttu-id="51589-112">لإكمال هذه الخطوات، يجب أن يكون لدى مستخدمي تطبيق الكتابة الثنائية الذين تم إنشاؤهم في Dataverse دور مسؤول النظام.</span><span class="sxs-lookup"><span data-stu-id="51589-112">To complete those steps, the dual-write application users who are created in Dataverse must have the system admin role.</span></span> <span data-ttu-id="51589-113">يجب أن يكون لدى الفريق المالك الافتراضي دور مسؤول النظام أيضًا.</span><span class="sxs-lookup"><span data-stu-id="51589-113">The default owning team must also have the system admin role.</span></span>

## <a name="live-synchronization-for-any-entity-consistently-throws-a-similar-error-when-you-create-a-row-in-a-finance-and-operations-app"></a><span data-ttu-id="51589-114">تطرح المزامنة المباشرة لأي كيان باستمرار خطأ مشابهًا عند إنشاء صف في تطبيق Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="51589-114">Live synchronization for any entity consistently throws a similar error when you create a row in a Finance and Operations app</span></span>

<span data-ttu-id="51589-115">**الدور المطلوب لإصلاح المشكلة:** مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="51589-115">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="51589-116">قد تتلقى رسالة خطأ مثل الرسالة التالية في كل مرة تحاول فيها حفظ بيانات الكيان في تطبيق Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="51589-116">You might receive an error message like the following every time that you try to save entity data in a Finance and Operations app:</span></span>

<span data-ttu-id="51589-117">*لا يمكن حفظ التغييرات التي تم اجراؤها علي قاعده البيانات. ولا يمكن لوحدة العمل تنفيذ الحركة. وتتعذر كتابة البيانات إلى وحدات قياس الكيانات. وفشلت عمليات الكتابة إلى UnitOfMeasureEntity مع ظهور رسالة الخطأ "تتعذر المزامنة مع وحدات قياس الكيانات.*</span><span class="sxs-lookup"><span data-stu-id="51589-117">*Cannot save the changes to the database. Unit of Work can not commit transaction. Unable to write data to entity uoms. Writes to UnitOfMeasureEntity failed with error message Unable to sync with entity uoms.*</span></span>

<span data-ttu-id="51589-118">لإصلاح المشكلة، يجب التأكد من وجود بيانات مرجع المتطلبات الأساسية في كل من تطبيق Finance and Operations وDataverse.</span><span class="sxs-lookup"><span data-stu-id="51589-118">To fix the issue, you must make sure that the prerequisite reference data exists in both the Finance and Operations app and Dataverse.</span></span> <span data-ttu-id="51589-119">علي سبيل المثال، إذا كان العميل الموجود في تطبيق Finance and Operationsينتمي إلى مجموعة عملاء محددة، فتأكد من وجود مجموعة العملاء في Dataverse.</span><span class="sxs-lookup"><span data-stu-id="51589-119">For example, if the customer that you're in the Finance and Operations app belongs to a specific customer group, make sure that the customer group exists in Dataverse.</span></span>

<span data-ttu-id="51589-120">في حالة وجود بيانات على كلا الجانبين، وقمت بالتأكد من أن المشكلة غير مرتبطة بالبيانات، فاتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="51589-120">If data exists on both sides, and you've confirmed that the issue isn't data-related, follow these steps.</span></span>

1. <span data-ttu-id="51589-121">أوقف الكيان المرتبط.</span><span class="sxs-lookup"><span data-stu-id="51589-121">Stop the related entity.</span></span>
2. <span data-ttu-id="51589-122">قم بتسجيل الدخول إلى تطبيق Finance and Operations، وتأكد من أن الصفوف الخاصة بالكيان الفاشل موجودة في الجدولين DualWriteProjectConfiguration وDualWriteProjectFieldConfiguration.</span><span class="sxs-lookup"><span data-stu-id="51589-122">Sign in to the Finance and Operations app, and make sure that rows for the failing entity exist in the DualWriteProjectConfiguration and DualWriteProjectFieldConfiguration tables.</span></span> <span data-ttu-id="51589-123">على سبيل المثال، فيما يلي ما يبدو عليه الاستعلام في حالة فشل كيان **العملاء**.</span><span class="sxs-lookup"><span data-stu-id="51589-123">For example, here is what the query looks like if the **Customers** entity is failing.</span></span>

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. <span data-ttu-id="51589-124">في حالة وجود صفوف للكيان الفاشل حتى بعد إيقاف تعيين الجدول، فاحذف الصفوف المرتبطة بالكيان الفاشل.</span><span class="sxs-lookup"><span data-stu-id="51589-124">If there are rows for the failing entity even after you stop the table mapping, delete the rows that are related to the failing entity.</span></span> <span data-ttu-id="51589-125">دوّن ملاحظm عن العمود **projectname** في جدول DualWriteProjectConfiguration، ثم قم بإحضار السجل في الجدول DualWriteProjectFieldConfiguration باستخدام اسم المشروع لحذف الصف.</span><span class="sxs-lookup"><span data-stu-id="51589-125">Make a note of the **projectname** column in the DualWriteProjectConfiguration table, and fetch the record in the DualWriteProjectFieldConfiguration table by using the project name to delete the row.</span></span>
4. <span data-ttu-id="51589-126">ابدأ تعيين الجدول.</span><span class="sxs-lookup"><span data-stu-id="51589-126">Start the table mapping.</span></span> <span data-ttu-id="51589-127">تحقق مما إذا كانت ستتم مزامنة البيانات دون أي مشكلات.</span><span class="sxs-lookup"><span data-stu-id="51589-127">Validate whether the data is synced without any issues.</span></span>

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a><span data-ttu-id="51589-128">معالجة أخطاء امتيازات القراءة أو الكتابة عند إنشاء بيانات في تطبيق Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="51589-128">Handle read or write privilege errors when you create data in a Finance and Operations app</span></span>

<span data-ttu-id="51589-129">قد تظهر رسالة الخطأ "طلب غير صحيح" المشابهة للمثال التالي عند إنشاء بيانات في تطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="51589-129">You might receive a "Bad Request" error message that resembles the following example when you create data in a Finance and Operations app.</span></span>

![مثال لرسالة الخطأ "طلب غير صحيح"](media/error_record_id_source.png)

<span data-ttu-id="51589-131">لإصلاح هذه المشكلة، يجب عليك تعيين دور الأمان الصحيح إلى فريق العمل في فريق Dynamics 365 Sales المعين أو وحدة الأعمال الخاصة بـ Dynamics 365 Customer Service لتمكين الامتيازات المفقودة.</span><span class="sxs-lookup"><span data-stu-id="51589-131">To fix the issue, you must assign the correct security role to the team of the mapped Dynamics 365 Sales or Dynamics 365 Customer Service business unit to enable the missing privilege.</span></span>

1. <span data-ttu-id="51589-132">في تطبيق Finance and Operations، ابحث عن وحدة الأعمال التي تم تعيينها في مجموعة اتصال تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="51589-132">In the Finance and Operations app, find the business unit that is mapped in the Data Integration connection set.</span></span>

    ![تعيين المؤسسة](media/mapped_business_unit.png)

2. <span data-ttu-id="51589-134">قم بتسجيل الدخول إلى البيئة الموجودة في التطبيق المستند إلى النموذج في Dynamics 365، وانتقل إلى **الإعداد \>الأمان**، وابحث عن فريق وحدة الأعمال المعيّنة.</span><span class="sxs-lookup"><span data-stu-id="51589-134">Sign in to the environment in the model-driven app in Dynamics 365, navigate to **Setting \> Security**, and find the team of the mapped business unit.</span></span>

    ![فريق وحدة الأعمال المعيّنة](media/setting_security_page.png)

3. <span data-ttu-id="51589-136">افتح الصفحة الخاصة بالفريق للتحرير، ثم حدد **إدارة الأدوار** لفتح مربع الحوار **إدارة أدوار الفريق**.</span><span class="sxs-lookup"><span data-stu-id="51589-136">Open the page for the team for editing, and then select **Manage roles** to open the **Manage Team Roles** dialog box.</span></span>

    ![الزر إدارة الأدوار](media/manage_team_roles.png)

4. <span data-ttu-id="51589-138">قم بتعيين الدور الذي يحتوي على امتياز القراءة/الكتابة للجداول ذات الصلة، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="51589-138">Assign the role that has the read/write privilege for the relevant tables, and then select **OK**.</span></span>

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a><span data-ttu-id="51589-139">إصلاح مشكلات المزامنة في بيئة تحتوي على بيئة Dataverse تم تغييرها مؤخرًا</span><span class="sxs-lookup"><span data-stu-id="51589-139">Fix synchronization issues in an environment that has a recently changed Dataverse environment</span></span>

<span data-ttu-id="51589-140">**الدور المطلوب لإصلاح المشكلة:** مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="51589-140">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="51589-141">قد تظهر رسالة الخطأ التالية عند إنشاء البيانات في تطبيق Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="51589-141">You might receive the following error message when you create data in a Finance and Operations app:</span></span>

<span data-ttu-id="51589-142">*{"entityName":"CustCustomerV3Entity"،"executionStatus":2,"fieldResponses":\[\]،"recordResponses":\[{"errorMessage":"\*\*يتعذر إنشاء الحمولة للكيان CustCustomerV3Entity*\* فشل إنشاء logDateTime":"2019-08-27T18:51:52.5843124Z"،"verboseError":"Payload"،" مع ظهور الخطأ عنوان URL غير صالح: عنوان URI فارغ."}\]،"isErrorCountUpdated":true}\*</span><span class="sxs-lookup"><span data-stu-id="51589-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Unable to generate payload for entity CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Payload creation failed with error Invalid URI: The URI is empty."}\],"isErrorCountUpdated":true}*</span></span>

<span data-ttu-id="51589-143">فيما يلي النمط الذي يبدو عليه الخطأ في التطبيق المستند إلى النموذج في Dynamics 365:</span><span class="sxs-lookup"><span data-stu-id="51589-143">Here is what the error looks like in the model-driven app in Dynamics 365:</span></span>

<span data-ttu-id="51589-144">*حدث خطأ غير متوقع من رمز ISV. (ErrorType = ClientError) استثناء غير متوقع من المكون الإضافي (تنفيذ): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: فشلت معالجة حساب الكيان - (فشلت محاولة الاتصال لأن الطرف المتصل لم يستجب بشكل صحيح بعد فترة من الوقت أو فشل الاتصال القائم لأن المضيف المتصل فشل في الاستجابة*</span><span class="sxs-lookup"><span data-stu-id="51589-144">*An unexpected error occurred from ISV code. (ErrorType = ClientError) Unexpected exception from plug-in (Execute): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: failed to process entity account - (A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond*</span></span>

<span data-ttu-id="51589-145">يحدث هذا الخطأ عند إعادة تعيين بيئة Dataverse بشكل غير صحيح في نفس الوقت الذي تحاول فيه إنشاء البيانات في تطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="51589-145">This error occurs when the Dataverse environment is incorrectly reset at the same time that you try to create data in the Finance and Operations app.</span></span>

<span data-ttu-id="51589-146">لإصلاح المشكلة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="51589-146">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="51589-147">قم بتسجيل الدخول إلى الجهاز الظاهري لـ Finance and Operations، وافتح SQL Server Management STUDIO (ssms) ، وابحث عن الصفوف في الجدول DUALWRITEPROJECTCONFIGURATIONENTITY حيث **internalentityname** يساوي **العملاء V3** و **externalentityname** يساوي **الحسابات**.</span><span class="sxs-lookup"><span data-stu-id="51589-147">Sign in to the Finance and Operations virtual machine (VM), open SQL Server Management Studio (SSMS), and look for rows in the DUALWRITEPROJECTCONFIGURATIONENTITY table where **internalentityname** equals **Customers V3** and **externalentityname** equals **accounts**.</span></span> <span data-ttu-id="51589-148">فيما يلي الشكل الذي يبدو عليه الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="51589-148">Here is what the query looks like.</span></span>

    ```sql
    select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and EXTERNALENTITYNAME = 'accounts'
    ```

2. <span data-ttu-id="51589-149">استخدم اسم المشروع من نتائج الاستعلام السابق لتشغيل الاستعلام التالي.</span><span class="sxs-lookup"><span data-stu-id="51589-149">Use the project name from the results of the previous query to run the following query.</span></span>

    ```sql
    select \* 
    from DUALWRITEPROJECTFIELDCONFIGURATION 
    where projectname = <project name from previous query>
    ```

3. <span data-ttu-id="51589-150">تأكد من أن العمود **externalenvironmentURL** على عنوان URL الصحيح للتطبيق أو Dataverse.</span><span class="sxs-lookup"><span data-stu-id="51589-150">Make sure that the **externalenvironmentURL** column has the correct Dataverse or app URL.</span></span> <span data-ttu-id="51589-151">احذف أي صفوف مكررة تشير إلى عنوان URL غير الصحيح لـ Dataverse.</span><span class="sxs-lookup"><span data-stu-id="51589-151">Delete any duplicate rows that point to the wrong Dataverse URL.</span></span> <span data-ttu-id="51589-152">احذف الصفوف المقابلة في جدولي DUALWRITEPROJECTFIELDCONFIGURATION وDUALWRITEPROJECTCONFIGURATION.</span><span class="sxs-lookup"><span data-stu-id="51589-152">Delete the corresponding rows in the DUALWRITEPROJECTFIELDCONFIGURATION and DUALWRITEPROJECTCONFIGURATION tables.</span></span>
4. <span data-ttu-id="51589-153">أوقف تعيين الجدول، ثم أعد تشغيله</span><span class="sxs-lookup"><span data-stu-id="51589-153">Stop the table mapping, and then restart it</span></span>
