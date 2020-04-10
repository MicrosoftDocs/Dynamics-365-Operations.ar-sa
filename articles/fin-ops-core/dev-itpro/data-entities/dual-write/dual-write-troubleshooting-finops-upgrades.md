---
title: استكشاف المشاكل ذات الصلة بترقيات تطبيقات Finance and Operations
description: يوفر هذا الموضوع استكشاف الأخطاء وإصلاحها الذي يمكن أن يساعدك في إصلاح المشكلات ذات الصلة بترقيات تطبيقات Finance and Operations.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 59384d8e8d043eb14231a471c7218ced2dddf739
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172867"
---
# <a name="troubleshoot-issues-related-to-upgrades-of-finance-and-operations-apps"></a><span data-ttu-id="e2261-103">استكشاف المشاكل ذات الصلة بترقيات تطبيقات Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e2261-103">Troubleshoot issues related to upgrades of Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="e2261-104">يوفر هذا الموضوع معلومات حول استكشاف أخطاء تكامل الكتابة الثنائية وإصلاحها بين تطبيقات Finance and Operations وCommon Data Service.</span><span class="sxs-lookup"><span data-stu-id="e2261-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="e2261-105">على وجه التحديد، يوفر هذا الموضوع المعلومات التي يمكن أن تساعدك في إصلاح المشكلات ذات الصلة بترقيات تطبيقات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e2261-105">Specifically, it provides information that can help you fix issues that are related to upgrades of Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e2261-106">قد تتطلب بعض المشكلات التي يتناولها هذا الموضوع إما دور إدارة النظام أو بيانات اعتماد مسؤول مستأجر  Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="e2261-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="e2261-107">يوضح القسم الخاص بكل مشكلة ما إذا كانت هناك حاجة إلى دور محدد أو بيانات اعتماد.</span><span class="sxs-lookup"><span data-stu-id="e2261-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="database-synchronization-errors"></a><span data-ttu-id="e2261-108">أخطاء مزامنة قواعد البيانات</span><span class="sxs-lookup"><span data-stu-id="e2261-108">Database synchronization errors</span></span>

<span data-ttu-id="e2261-109">**الدور المطلوب لإصلاح المشكلة:** مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="e2261-109">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="e2261-110">قد تظهر رسالة خطأ مشابهة للمثال التالي عند محاولة استخدام كيان **DualWriteProjectConfiguration** لتحديث تطبيق Finance and Operations إلى تحديث النظام الأساسي 30.</span><span class="sxs-lookup"><span data-stu-id="e2261-110">You might receive an error message that resembles the following example when you try to use the **DualWriteProjectConfiguration** entity to update a Finance and Operations app to Platform update 30.</span></span>

```console
Infolog diagnostic message: 'Cannot select a record in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

<span data-ttu-id="e2261-111">لإصلاح المشكلة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="e2261-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="e2261-112">سجل الدخول إلى الجهاز الظاهري (VM) لتطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e2261-112">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="e2261-113">افتح Visual Studio كمسؤول، ثم افتح شجره مكونات البرنامج (AOT).</span><span class="sxs-lookup"><span data-stu-id="e2261-113">Open Visual Studio as an admin, and open the Application Object Tree (AOT).</span></span>
3. <span data-ttu-id="e2261-114">ابحث عن **DualWriteProjectConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="e2261-114">Search for **DualWriteProjectConfiguration**.</span></span>
4. <span data-ttu-id="e2261-115">في شجرة مكونات المنتج، انقر بزر الماوس الأيمن فوق **DualWriteProjectConfiguration**، ثم حدد **إضافة إلى مشروع جديد**.</span><span class="sxs-lookup"><span data-stu-id="e2261-115">In the AOT, right-click **DualWriteProjectConfiguration**, and select **Add to new project**.</span></span> <span data-ttu-id="e2261-116">حدد **موافق** لإنشاء المشروع الجديد الذي يستخدم الخيارات الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="e2261-116">Select **OK** to create the new project that uses default options.</span></span>
5. <span data-ttu-id="e2261-117">في مستكشف الحلول، انقر بزر الماوس الأيمن فوق **خصائص المشروع**، وقم بتعيين **مزامنة قاعدة البيانات عند الإنشاء** إلى **True**.</span><span class="sxs-lookup"><span data-stu-id="e2261-117">In Solution Explorer, right-click **Project properties**, and set **Synchronize Database on Build** to **True**.</span></span>
6. <span data-ttu-id="e2261-118">قم ببناء المشروع وتأكد من نجاح البنية.</span><span class="sxs-lookup"><span data-stu-id="e2261-118">Build the project, and confirm that the build is successful.</span></span>
7. <span data-ttu-id="e2261-119">في قائمة **Dynamics 365**، حدد **مزامنة قاعدة البيانات**.</span><span class="sxs-lookup"><span data-stu-id="e2261-119">On the **Dynamics 365** menu, select **Synchronize database**.</span></span>
8. <span data-ttu-id="e2261-120">حدد **مزامنة** لإجراء مزامنة كاملة لقاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="e2261-120">Select **Synchronize** to do a full database synchronization.</span></span>
9. <span data-ttu-id="e2261-121">بعد نجاح مزامنة قاعده البيانات بالكامل، أعد تشغيل خطوة مزامنة قاعده البيانات في Microsoft Dynamics Lifecycle Services ‏(LCS) واستخدم البرامج النصية الخاصة بالترقية اليدوية حسب الحاجة، حتى يمكنك الاستمرار في عمليه التحديث.</span><span class="sxs-lookup"><span data-stu-id="e2261-121">After the full database synchronization is successful, rerun the database synchronization step in Microsoft Dynamics Lifecycle Services (LCS) and use the manual upgrade scripts as applicable, so that you can proceed with the update.</span></span>

## <a name="missing-entity-fields-issue-on-maps"></a><span data-ttu-id="e2261-122">مشكلة حقول الكيانات المفقودة في المخططات</span><span class="sxs-lookup"><span data-stu-id="e2261-122">Missing entity fields issue on maps</span></span>

<span data-ttu-id="e2261-123">**الدور المطلوب لإصلاح المشكلة:** مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="e2261-123">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="e2261-124">في صفحة **الكتابة الثنائية**، قد تتلقي رسالة خطأ مشابهة للمثال التالي:</span><span class="sxs-lookup"><span data-stu-id="e2261-124">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="e2261-125">*حقل المصدر المفقود \<اسم الحقل\> في المخطط.*</span><span class="sxs-lookup"><span data-stu-id="e2261-125">*Missing source field \<field name\> in the schema.*</span></span>

![مثال لرسالة الخطأ حقل المصدر مفقود](media/error_missing_field.png)

<span data-ttu-id="e2261-127">لإصلاح هذه المشكلة، اتبع أولاً الخطوات التالية للتأكد من وجود الحقول في الكيان.</span><span class="sxs-lookup"><span data-stu-id="e2261-127">To fix the issue, first follow these steps to make sure that the fields are in the entity.</span></span>

1. <span data-ttu-id="e2261-128">سجل الدخول إلى الجهاز الظاهري لتطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e2261-128">Sign in to the VM for the Finance and Operations app.</span></span>
2. <span data-ttu-id="e2261-129">انتقل إلى **مساحات العمل \> إدارة البيانات**، حدد تجانب **معلمات إطارات العمل**، ثم في علامة التبويب **إعدادات الكيان**، حدد **تحديث قائمة الكيانات** لتحديث الكيانات.</span><span class="sxs-lookup"><span data-stu-id="e2261-129">Go to **Workspaces \> Data management**, select the **Framework parameters** tile, and then, on the **Entity settings** tab, select **Refresh entity list** to refresh the entities.</span></span>
3. <span data-ttu-id="e2261-130">انتقل إلى **مساحات العمل \> إدارة البيانات**، وحدد علامة التبويب **كيانات البيانات**، ثم تأكد من إدارج الكيان.</span><span class="sxs-lookup"><span data-stu-id="e2261-130">Go to **Workspaces \> Data management**, select the **Data entities** tab, and make sure that the entity is listed.</span></span> <span data-ttu-id="e2261-131">إذا لم يكن الكيان مدرجًا، فقم بتسجيل الدخول إلى الجهاز الظاهري لتطبيق Finance and Operations، وتأكد من توفر الكيان.</span><span class="sxs-lookup"><span data-stu-id="e2261-131">If the entity isn't listed, sign in to the VM for the Finance and Operations app, and make sure the entity is available.</span></span>
4. <span data-ttu-id="e2261-132">افتح صفحة **تعيين الكيان** من صفحة **الكتابة الثنائية** في تطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e2261-132">Open the **Entity mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="e2261-133">حدد **تحديث قائمة الكيانات** لملء الحقول تلقائيًا في تعيينات الكيانات.</span><span class="sxs-lookup"><span data-stu-id="e2261-133">Select **Refresh entity list** to automatically fill the fields in the entity mappings.</span></span>

<span data-ttu-id="e2261-134">في حالة استمرار إصلاح المشكلة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="e2261-134">If the issue still isn't fixed, follow these steps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e2261-135">ترشدك هذه الخطوات خلال عملية حذف أحد الكيانات ثم إضافته مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="e2261-135">These steps guide you through the process of deleting an entity and then adding it again.</span></span> <span data-ttu-id="e2261-136">لتجنب المشكلات، تأكد من اتباع الخطوات بدقة.</span><span class="sxs-lookup"><span data-stu-id="e2261-136">To avoid issues, be sure to follow the steps exactly.</span></span>

1. <span data-ttu-id="e2261-137">في تطبيق Finance and Operations، انتقل إلى **مساحات العمل\> إدارة البيانات**، ثم حدد تجانب **كيانات البيانات**.</span><span class="sxs-lookup"><span data-stu-id="e2261-137">In the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Data entities** tile.</span></span>
2. <span data-ttu-id="e2261-138">ابحث عن الكيان الذي يفتقد إلى الحقل.</span><span class="sxs-lookup"><span data-stu-id="e2261-138">Find the entity that is missing the field.</span></span> <span data-ttu-id="e2261-139">قم بتدوين الكيان الهدف والجدول المرحلي واسم الكيان وقيم الأعمدة الأخرى.</span><span class="sxs-lookup"><span data-stu-id="e2261-139">Make a note of the target entity, staging table, entity name, and other column values.</span></span>
3. <span data-ttu-id="e2261-140">إذا كانت أي مجموعة من المجموعات المعالجة الخاصة بك تعتمد على هذا الكيان، فاتخذ الاجراء المناسب لمجموعات المعالجة قبل حذف الكيان.</span><span class="sxs-lookup"><span data-stu-id="e2261-140">If any of your processing groups depend on this entity, take appropriate action for the processing groups before you delete the entity.</span></span>
4. <span data-ttu-id="e2261-141">احذف الكيان الذي يفتقد إلى الحقل.</span><span class="sxs-lookup"><span data-stu-id="e2261-141">Delete the entity that is missing the field.</span></span>
5. <span data-ttu-id="e2261-142">حدد **جديد**، وأضف الكيان مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="e2261-142">Select **New**, and add the entity back.</span></span> <span data-ttu-id="e2261-143">حدد القيم التي قمت بتدوين ملاحظة لها في الخطوة 2.</span><span class="sxs-lookup"><span data-stu-id="e2261-143">Specify the values that you made a note of in step 2.</span></span>
6. <span data-ttu-id="e2261-144">افتح صفحة **تعيين الكيان** من صفحة **الكتابة الثنائية** في تطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e2261-144">Open the **Entity mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
7. <span data-ttu-id="e2261-145">حدد **تحديث قائمة الكيانات** لملء الحقول تلقائيًا في تعيينات الكيانات.</span><span class="sxs-lookup"><span data-stu-id="e2261-145">Select **Refresh entity list** to automatically fill the fields in the entity mappings.</span></span>
