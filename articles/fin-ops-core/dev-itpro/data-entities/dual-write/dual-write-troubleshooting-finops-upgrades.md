---
title: استكشاف المشاكل من ترقيات تطبيقات Finance and Operations
description: يوفر هذا الموضوع استكشاف الأخطاء وإصلاحها الذي يمكن أن يساعدك في إصلاح المشكلات ذات الصلة بترقيات تطبيقات Finance and Operations.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: ae54ffc9f7a97793dfaddc29f5aae66e5b06c931
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561192"
---
# <a name="troubleshoot-issues-from-upgrades-of-finance-and-operations-apps"></a><span data-ttu-id="11497-103">استكشاف المشاكل من ترقيات تطبيقات Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="11497-103">Troubleshoot issues from upgrades of Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="11497-104">يوفر هذا الموضوع معلومات حول استكشاف أخطاء تكامل الكتابة الثنائية وإصلاحها بين تطبيقات Finance and Operations وDataverse.</span><span class="sxs-lookup"><span data-stu-id="11497-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="11497-105">على وجه التحديد، يوفر هذا الموضوع المعلومات التي يمكن أن تساعدك في إصلاح المشكلات ذات الصلة بترقيات تطبيقات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="11497-105">Specifically, it provides information that can help you fix issues that are related to upgrades of Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="11497-106">قد تتطلب بعض المشكلات التي يتناولها هذا الموضوع إما دور إدارة النظام أو بيانات اعتماد مسؤول مستأجر  Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="11497-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="11497-107">يوضح القسم الخاص بكل مشكلة ما إذا كانت هناك حاجة إلى دور محدد أو بيانات اعتماد.</span><span class="sxs-lookup"><span data-stu-id="11497-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="database-synchronization-errors"></a><span data-ttu-id="11497-108">أخطاء مزامنة قواعد البيانات</span><span class="sxs-lookup"><span data-stu-id="11497-108">Database synchronization errors</span></span>

<span data-ttu-id="11497-109">**الدور المطلوب لإصلاح المشكلة:** مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="11497-109">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="11497-110">قد تظهر رسالة خطأ مشابهة للمثال التالي عند محاولة استخدام جدول **DualWriteProjectConfiguration** لتحديث تطبيق Finance and Operations إلى تحديث النظام الأساسي 30.</span><span class="sxs-lookup"><span data-stu-id="11497-110">You might receive an error message that resembles the following example when you try to use the **DualWriteProjectConfiguration** table to update a Finance and Operations app to Platform update 30.</span></span>

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

<span data-ttu-id="11497-111">لإصلاح المشكلة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="11497-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="11497-112">سجل الدخول إلى الجهاز الظاهري (VM) لتطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="11497-112">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="11497-113">افتح Visual Studio كمسؤول، ثم افتح شجره مكونات البرنامج (AOT).</span><span class="sxs-lookup"><span data-stu-id="11497-113">Open Visual Studio as an admin, and open the Application Object Tree (AOT).</span></span>
3. <span data-ttu-id="11497-114">ابحث عن **DualWriteProjectConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="11497-114">Search for **DualWriteProjectConfiguration**.</span></span>
4. <span data-ttu-id="11497-115">في شجرة مكونات المنتج، انقر بزر الماوس الأيمن فوق **DualWriteProjectConfiguration**، ثم حدد **إضافة إلى مشروع جديد**.</span><span class="sxs-lookup"><span data-stu-id="11497-115">In the AOT, right-click **DualWriteProjectConfiguration**, and select **Add to new project**.</span></span> <span data-ttu-id="11497-116">حدد **موافق** لإنشاء المشروع الجديد الذي يستخدم الخيارات الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="11497-116">Select **OK** to create the new project that uses default options.</span></span>
5. <span data-ttu-id="11497-117">في مستكشف الحلول، انقر بزر الماوس الأيمن فوق **خصائص المشروع**، وقم بتعيين **مزامنة قاعدة البيانات عند الإنشاء** إلى **True**.</span><span class="sxs-lookup"><span data-stu-id="11497-117">In Solution Explorer, right-click **Project properties**, and set **Synchronize Database on Build** to **True**.</span></span>
6. <span data-ttu-id="11497-118">قم ببناء المشروع وتأكد من نجاح البنية.</span><span class="sxs-lookup"><span data-stu-id="11497-118">Build the project, and confirm that the build is successful.</span></span>
7. <span data-ttu-id="11497-119">في قائمة **Dynamics 365**، حدد **مزامنة قاعدة البيانات**.</span><span class="sxs-lookup"><span data-stu-id="11497-119">On the **Dynamics 365** menu, select **Synchronize database**.</span></span>
8. <span data-ttu-id="11497-120">حدد **مزامنة** لإجراء مزامنة كاملة لقاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="11497-120">Select **Synchronize** to do a full database synchronization.</span></span>
9. <span data-ttu-id="11497-121">بعد نجاح مزامنة قاعده البيانات بالكامل، أعد تشغيل خطوة مزامنة قاعده البيانات في Microsoft Dynamics Lifecycle Services ‏(LCS) واستخدم البرامج النصية الخاصة بالترقية اليدوية حسب الحاجة، حتى يمكنك الاستمرار في عمليه التحديث.</span><span class="sxs-lookup"><span data-stu-id="11497-121">After the full database synchronization is successful, rerun the database synchronization step in Microsoft Dynamics Lifecycle Services (LCS) and use the manual upgrade scripts as applicable, so that you can proceed with the update.</span></span>

## <a name="missing-table-columns-issue-on-maps"></a><span data-ttu-id="11497-122">إصدار أعمده الجدول المفقودة في التعيينات</span><span class="sxs-lookup"><span data-stu-id="11497-122">Missing table columns issue on maps</span></span>

<span data-ttu-id="11497-123">**الدور المطلوب لإصلاح المشكلة:** مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="11497-123">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="11497-124">في صفحة **الكتابة الثنائية**، قد تتلقي رسالة خطأ مشابهة للمثال التالي:</span><span class="sxs-lookup"><span data-stu-id="11497-124">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="11497-125">*حقل المصدر المفقود \<field name\> في المخطط.*</span><span class="sxs-lookup"><span data-stu-id="11497-125">*Missing source field \<field name\> in the schema.*</span></span>

![مثال لرسالة الخطأ عمود المصدر مفقود](media/error_missing_field.png)

<span data-ttu-id="11497-127">لإصلاح هذه المشكلة، اتبع أولاً الخطوات التالية للتأكد من وجود الأعمدة في الجدول.</span><span class="sxs-lookup"><span data-stu-id="11497-127">To fix the issue, first follow these steps to make sure that the columns are in the table.</span></span>

1. <span data-ttu-id="11497-128">سجل الدخول إلى الجهاز الظاهري لتطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="11497-128">Sign in to the VM for the Finance and Operations app.</span></span>
2. <span data-ttu-id="11497-129">انتقل إلى **مساحات العمل \> إدارة البيانات**، حدد تجانب **معلمات إطارات العمل**، ثم في علامة التبويب **إعدادات الجدول**، حدد **تحديث قائمة الجداول** لتحديث الجداول.</span><span class="sxs-lookup"><span data-stu-id="11497-129">Go to **Workspaces \> Data management**, select the **Framework parameters** tile, and then, on the **Table settings** tab, select **Refresh table list** to refresh the tables.</span></span>
3. <span data-ttu-id="11497-130">انتقل إلى **مساحات العمل \> إدارة البيانات**، وحدد علامة التبويب **جداول البيانات**، ثم تأكد من إدارج الجدول.</span><span class="sxs-lookup"><span data-stu-id="11497-130">Go to **Workspaces \> Data management**, select the **Data tables** tab, and make sure that the table is listed.</span></span> <span data-ttu-id="11497-131">إذا لم يكن الجدول مدرجًا، فقم بتسجيل الدخول إلى الجهاز الظاهري لتطبيق Finance and Operations، وتأكد من توفر الجدول.</span><span class="sxs-lookup"><span data-stu-id="11497-131">If the table isn't listed, sign in to the VM for the Finance and Operations app, and make sure the table is available.</span></span>
4. <span data-ttu-id="11497-132">افتح صفحة **تعيين الجدول** من صفحة **الكتابة الثنائية** في تطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="11497-132">Open the **Table mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="11497-133">حدد **تحديث قائمة الجداول** لملء الأعمدة تلقائيًا في تعيينات الجداول.</span><span class="sxs-lookup"><span data-stu-id="11497-133">Select **Refresh table list** to automatically fill the columns in the table mappings.</span></span>

<span data-ttu-id="11497-134">في حالة استمرار إصلاح المشكلة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="11497-134">If the issue still isn't fixed, follow these steps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="11497-135">ترشدك هذه الخطوات خلال عملية حذف أحد الجداول ثم إضافته مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="11497-135">These steps guide you through the process of deleting a table and then adding it again.</span></span> <span data-ttu-id="11497-136">لتجنب المشكلات، تأكد من اتباع الخطوات بدقة.</span><span class="sxs-lookup"><span data-stu-id="11497-136">To avoid issues, be sure to follow the steps exactly.</span></span>

1. <span data-ttu-id="11497-137">في تطبيق Finance and Operations، انتقل إلى **مساحات العمل\> إدارة البيانات**، ثم حدد تجانب **جداول البيانات**.</span><span class="sxs-lookup"><span data-stu-id="11497-137">In the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Data tables** tile.</span></span>
2. <span data-ttu-id="11497-138">ابحث عن الجدول الذي يفتقد إلى السمة.</span><span class="sxs-lookup"><span data-stu-id="11497-138">Find the table that is missing the attribute.</span></span> <span data-ttu-id="11497-139">انقر فوق **تعديل تعيين هدف** في شريط الأدوات.</span><span class="sxs-lookup"><span data-stu-id="11497-139">Click **Modify target mapping** in the toolbar.</span></span>
3. <span data-ttu-id="11497-140">في الجزء **تعيين التشغيل المرحلي إلى الهدف**، انقر فوق **إنشاء تعيين للمصدر**.</span><span class="sxs-lookup"><span data-stu-id="11497-140">On the **Map staging to target** pane, click **Generate mapping**.</span></span>
4. <span data-ttu-id="11497-141">افتح صفحة **تعيين الجدول** من صفحة **الكتابة الثنائية** في تطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="11497-141">Open the **Table mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="11497-142">إذا كان لا يتم ملء السمة تلقائيًا في التعيين، فقم بإضافتها يدويا بالنقر فوق زر **إضافة سمة** ثم النقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="11497-142">If the attribute is not auto-populated on the map, add it manually by clicking **Add attribute** button and then clicking **Save**.</span></span> 
6. <span data-ttu-id="11497-143">حدد التعيين ثم انقر فوق **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="11497-143">Select the map and click **Run**.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]