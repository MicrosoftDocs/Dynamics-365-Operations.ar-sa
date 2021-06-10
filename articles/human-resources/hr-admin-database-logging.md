---
title: تكوين وإدارة تسجيل قاعده البيانات
description: يمكنك تعقب التغييرات في الجداول والحقول في Dynamics 365 Human Resources بتسجيل قاعده البيانات.
author: andreabichsel
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ae974436469c00a3df6fd40d9d60521a0883a917
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054802"
---
# <a name="configure-and-manage-database-logging"></a><span data-ttu-id="07050-103">تكوين وإدارة تسجيل قاعده البيانات</span><span class="sxs-lookup"><span data-stu-id="07050-103">Configure and manage database logging</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="07050-104">يمكنك تعقب التغييرات في الجداول والحقول في Dynamics 365 Human Resources بتسجيل قاعده البيانات.</span><span class="sxs-lookup"><span data-stu-id="07050-104">You can track changes to tables and fields in Dynamics 365 Human Resources with database logging.</span></span> <span data-ttu-id="07050-105">يصف هذا الموضوع كيفية:</span><span class="sxs-lookup"><span data-stu-id="07050-105">This topic describes how to:</span></span>

- <span data-ttu-id="07050-106">إدارة الأمان والأداء لتسجيل قاعده البيانات</span><span class="sxs-lookup"><span data-stu-id="07050-106">Manage security and performance for database logging</span></span>
- <span data-ttu-id="07050-107">إعداد تسجيل قاعدة البيانات</span><span class="sxs-lookup"><span data-stu-id="07050-107">Set up database logging</span></span>
- <span data-ttu-id="07050-108">تنظيف سجلات قواعد البيانات</span><span class="sxs-lookup"><span data-stu-id="07050-108">Clean up database logs</span></span>

## <a name="overview-of-database-logging"></a><span data-ttu-id="07050-109">نظرة عامة حول تسجيل قاعده البيانات</span><span class="sxs-lookup"><span data-stu-id="07050-109">Overview of database logging</span></span>

<span data-ttu-id="07050-110">يتعقب تسجيل قاعدة البيانات التغييرات في الجداول والحقول في Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="07050-110">Database logging tracks specific changes to Microsoft Dynamics 365 Human Resources tables and fields.</span></span> <span data-ttu-id="07050-111">وتتضمن هذه التغييرات الإدراج أو التحديث أو الحذف.</span><span class="sxs-lookup"><span data-stu-id="07050-111">These changes include inserting, updating, or deleting.</span></span> <span data-ttu-id="07050-112">يُخزن تسجيل قاعده البيانات سجلا بالتغييرات في الجداول أو الحقول في جدول سجل قاعده البيانات.</span><span class="sxs-lookup"><span data-stu-id="07050-112">Database logging stores a record of changes to tables or fields in the database log table.</span></span>

<span data-ttu-id="07050-113">تشمل استخدامات الأعمال الخاصة بتسجيل قاعده البيانات ما يلي:</span><span class="sxs-lookup"><span data-stu-id="07050-113">The business uses of database logging include:</span></span>

- <span data-ttu-id="07050-114">إنشاء سجل تدقيق للتغييرات إلى جداول معينة تحتوي علي معلومات حساسة.</span><span class="sxs-lookup"><span data-stu-id="07050-114">Creating an audit record of changes to specific tables that contain sensitive information.</span></span>
- <span data-ttu-id="07050-115">تعقب الحركات الفردية.</span><span class="sxs-lookup"><span data-stu-id="07050-115">Tracking single transactions.</span></span> <span data-ttu-id="07050-116">لا يعتبر تسجيل قاعده البيانات معدا لتعقب الحركات المؤتمتة التي يتم تشغيلها في مهام المجموعات.</span><span class="sxs-lookup"><span data-stu-id="07050-116">Database logging isn't intended for tracking automated transactions that run in batch jobs.</span></span>

## <a name="security-for-database-logging"></a><span data-ttu-id="07050-117">الأمان لتسجيل قاعده البيانات</span><span class="sxs-lookup"><span data-stu-id="07050-117">Security for database logging</span></span>

<span data-ttu-id="07050-118">يمكن أن تحتوي سجلات البيانات على بيانات حساسة.</span><span class="sxs-lookup"><span data-stu-id="07050-118">Database logs can contain sensitive data.</span></span> <span data-ttu-id="07050-119">تقييد الوصول ليشمل فقط الأدوار الأمنيه التي تحتاج إلى الوصول إلى بيانات السجل.</span><span class="sxs-lookup"><span data-stu-id="07050-119">Limit access to include only security roles that need access to the log data.</span></span>

## <a name="database-logging-and-performance"></a><span data-ttu-id="07050-120">تسجيل قاعده البيانات وأداءها</span><span class="sxs-lookup"><span data-stu-id="07050-120">Database logging and performance</span></span>

<span data-ttu-id="07050-121">يمكن أن يكون تسجيل قاعده البيانات مكلفًا من حيث استخدام الموارد وأدارتها رغم أهميتة الكبيرة من منظور الاعمال.</span><span class="sxs-lookup"><span data-stu-id="07050-121">While valuable from a business perspective, database logging can be expensive in resource use and management.</span></span> <span data-ttu-id="07050-122">تشمل عواقب الأداء الخاصة بتسجيل قاعده البيانات ما يلي:</span><span class="sxs-lookup"><span data-stu-id="07050-122">The performance implications of database logging include:</span></span>

- <span data-ttu-id="07050-123">يمكن أن يزيد حجم جدول سجل قاعده البيانات بسرعة مما يؤدي إلى زيادة في حجم قاعده البيانات.</span><span class="sxs-lookup"><span data-stu-id="07050-123">The database log table can grow quickly and cause an increase in the size of the database.</span></span> <span data-ttu-id="07050-124">تعتمد النمو علة كميه البيانات المسجلة التي تقرر الاحتفاظ بها.</span><span class="sxs-lookup"><span data-stu-id="07050-124">Growth depends on the amount of logged data that you decide to keep.</span></span> <span data-ttu-id="07050-125">افتراضياً، يحتفظ جدول سجل قاعده البيانات بـ 30 يوما فقط من بيانات السجل.</span><span class="sxs-lookup"><span data-stu-id="07050-125">By default, the database log table maintains only 30 days of log data.</span></span> 

- <span data-ttu-id="07050-126">يمكن ان يؤثر تسجيل قاعده البيانات سلبًا على العمليات التلقائية التي تعمل لفترة طويلة‬، مثل عمليات استيراد البيانات التي تعمل لفترة طويلة‬.</span><span class="sxs-lookup"><span data-stu-id="07050-126">Database logging can adversely affect long-running automated processes, such as long-running data imports.</span></span>

### <a name="best-practices"></a><span data-ttu-id="07050-127">أفضل الممارسات</span><span class="sxs-lookup"><span data-stu-id="07050-127">Best practices</span></span>

<span data-ttu-id="07050-128">ولتحسين الأداء، يمكن تقييد إدخالات السجل بتحديد حقول معينة لتسجيلها بدلاً من جداول بأكملها.</span><span class="sxs-lookup"><span data-stu-id="07050-128">To improve performance, limit log entries by selecting specific fields to log instead of whole tables.</span></span> <span data-ttu-id="07050-129">للمساعدة في الحفاظ علي الأداء العام، يكون تسجيل قاعده البيانات محدودًا بـ 20 جدولاً.</span><span class="sxs-lookup"><span data-stu-id="07050-129">To help maintain overall performance, database logging is limited to 20 tables.</span></span>

> [!NOTE]
> <span data-ttu-id="07050-130">يمكن تسجيل التحديثات فقط للحقول المفردة.</span><span class="sxs-lookup"><span data-stu-id="07050-130">Only updates can be logged for individual fields.</span></span>

## <a name="set-up-database-logging"></a><span data-ttu-id="07050-131">إعداد تسجيل قاعدة البيانات</span><span class="sxs-lookup"><span data-stu-id="07050-131">Set up database logging</span></span>

<span data-ttu-id="07050-132">يمكنك استخدام معالج **تسجيل قاعدة البيانات** لإعداد تسجيل قاعده البيانات.</span><span class="sxs-lookup"><span data-stu-id="07050-132">You can use the **Logging database changes** wizard to set up database logging.</span></span> <span data-ttu-id="07050-133">ويوفر المعالج طريقةمرنة لاعداد التسجيل للجداول أو الحقول.</span><span class="sxs-lookup"><span data-stu-id="07050-133">The wizard provides a flexible way to set up logging for tables or fields.</span></span>

1. <span data-ttu-id="07050-134">انتقل إلى **إدارة النظام > الارتباطات > قواعد البيانات > إعداد سجل قاعدة البيانات**.</span><span class="sxs-lookup"><span data-stu-id="07050-134">Go to **System administration > Links > Database > Database log setup**.</span></span> <span data-ttu-id="07050-135">حدد **جديد** لبدء معالج **تغييرات قاعدة بيانات التسجيل**.</span><span class="sxs-lookup"><span data-stu-id="07050-135">Select **New** to start the **Logging database changes** wizard.</span></span>
2. <span data-ttu-id="07050-136">حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="07050-136">Select **Next**.</span></span> 
3. <span data-ttu-id="07050-137">في صفحة **الجداول والحقول** في المعالج، حدد الجداول والحقول التي ترغب في تمكين تسجيل قاعده البيانات عليها، ثم حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="07050-137">On the **Tables and fields** page of the wizard, select the the tables and fields on which you want to enable database logging, and select **Next**.</span></span>

   > [!Note]
   > <span data-ttu-id="07050-138">لا يتوفر تسجيل قاعدة البيانات في جميع الجداول في قاعدة بيانات Human Resources.</span><span class="sxs-lookup"><span data-stu-id="07050-138">Database logging is not available on all tables in the Human Resources database.</span></span> <span data-ttu-id="07050-139">يؤدي تحديد **إظهار كل الجداول** أسفل القائمة توسع قائمة الجداول والحقول لإظهار جميع جداول قاعدة البيانات التي يتوفر لها تسجيل قاعدة البيانات، ولكن هذه ستكون مجموعة فرعية من القائمة الكاملة لجداول قاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="07050-139">Selecting **Show all tables** below the list expands the list of tables and fields to show all database tables for which database logging is available, but this will be a subset of the full list of database tables.</span></span>

4. <span data-ttu-id="07050-140">في صفحة **أنواع التغيير** في المعالج، حدد عمليات البيانات التي تريد تعقب التغييرات الخاصة بها لكل من الجداول والحقول، ثم حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="07050-140">On the **Types of change** page of the wizard, select the data operations for which you want to track changes for each of the tables and fields, and select **Next**.</span></span> <span data-ttu-id="07050-141">انظر الجدول أدناه للحصول على وصف لعمليات البيانات المتاحة للتسجيل.</span><span class="sxs-lookup"><span data-stu-id="07050-141">See the table below for a description of the data operations that are available for logging.</span></span>
5. <span data-ttu-id="07050-142">في صفحة **الإنهاء**، قم بمراجعه التغييرات التي ستُجرى، وحدد **إنهاء**.</span><span class="sxs-lookup"><span data-stu-id="07050-142">On the **Finish** page, review the changes that will be made, and select **Finish**.</span></span>

| <span data-ttu-id="07050-143">العملية</span><span class="sxs-lookup"><span data-stu-id="07050-143">Operation</span></span> | <span data-ttu-id="07050-144">الوصف</span><span class="sxs-lookup"><span data-stu-id="07050-144">Description</span></span> |
| -- | -- |
| <span data-ttu-id="07050-145">تعقب الحركات الجديدة</span><span class="sxs-lookup"><span data-stu-id="07050-145">Track new transactions</span></span> | <span data-ttu-id="07050-146">قم بإنشاء سجل للسجلات الجديدة التي تم إنشاؤها في الجدول.</span><span class="sxs-lookup"><span data-stu-id="07050-146">Create a log for new records that are created in the table.</span></span> |
| <span data-ttu-id="07050-147">تحديث</span><span class="sxs-lookup"><span data-stu-id="07050-147">Update</span></span> | <span data-ttu-id="07050-148">أنشئ سجلاً لتحديثات سجلات الجدول، أو تحديثات الحقول المحددة بشكل فردي في الجدول.</span><span class="sxs-lookup"><span data-stu-id="07050-148">Create a log for updates to table records, or updates to individually selected fields in the table.</span></span> <span data-ttu-id="07050-149">إذا قمت بتحديد تسجيل التحديثات الخاصة بالجدول، سيتم إنشاء سجل سجل في كل مره يتم اجراء تحديث علي اي حقل من السجلات في الجدول.</span><span class="sxs-lookup"><span data-stu-id="07050-149">If you select to log updates for the table, then a log record is created each time an update is made to any field of any record on the table.</span></span> <span data-ttu-id="07050-150">إذا قمت بتحديد تسجيل التحديثات لحقول معينه، سيتم إنشاء سجل سجل فقط عند اجراء تحديثات علي حقول سجلات الجدول.</span><span class="sxs-lookup"><span data-stu-id="07050-150">If you select to log updates for specific fields, then a log record is created only when updates are made to those fields of table records.</span></span> |
| <span data-ttu-id="07050-151">Delete</span><span class="sxs-lookup"><span data-stu-id="07050-151">Delete</span></span> | <span data-ttu-id="07050-152">إنشاء سجل للسجلات المحذوفة من الجدول.</span><span class="sxs-lookup"><span data-stu-id="07050-152">Create a log for records deleted from the table.</span></span> |
| <span data-ttu-id="07050-153">إعادة تسمية المفتاح</span><span class="sxs-lookup"><span data-stu-id="07050-153">Rename key</span></span> | <span data-ttu-id="07050-154">إنشاء سجل سجل عند أعاده تسميه مفتاح جدول.</span><span class="sxs-lookup"><span data-stu-id="07050-154">Create a log record when a table key is renamed.</span></span> |


## <a name="clean-up-database-logs"></a><span data-ttu-id="07050-155">تنظيف سجلات قواعد البيانات</span><span class="sxs-lookup"><span data-stu-id="07050-155">Clean up database logs</span></span>

<span data-ttu-id="07050-156">يمكنك حذف كافة سجلات قاعده البيانات أو جزء منها، باستخدام الخيارات التالية:</span><span class="sxs-lookup"><span data-stu-id="07050-156">You can delete all or part of the database logs, using the following options:</span></span>

- <span data-ttu-id="07050-157">حدد كافة السجلات لجدول معين.</span><span class="sxs-lookup"><span data-stu-id="07050-157">Select all logs for a particular table.</span></span>
- <span data-ttu-id="07050-158">حدد أنواع معينه من سجل قواعد البيانات.</span><span class="sxs-lookup"><span data-stu-id="07050-158">Select specific types of database log.</span></span>
- <span data-ttu-id="07050-159">حدد تاريخ ووقت إنشاء سجل.</span><span class="sxs-lookup"><span data-stu-id="07050-159">Select a date and time that a log was created.</span></span>

<span data-ttu-id="07050-160">لإعداد ‏‫تنظيف سجل قاعدة البيانات، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="07050-160">To set up database log cleanup, follow these steps:</span></span> 

1. <span data-ttu-id="07050-161">انتقل إلى **إدارة النظام > الارتباطات > قواعد البيانات > سجل قاعدة البيانات**.</span><span class="sxs-lookup"><span data-stu-id="07050-161">Go to **System administration > Links > Database > Database log**.</span></span> <span data-ttu-id="07050-162">حدد **‏‫تنظيف السجل**.</span><span class="sxs-lookup"><span data-stu-id="07050-162">Select **Clean up log**.</span></span>

2. <span data-ttu-id="07050-163">اختر أسلوبا لتحديد السجلات المراد حذفها من خلال إدخال أحد الخيارات التالية:</span><span class="sxs-lookup"><span data-stu-id="07050-163">Choose a method of selecting logs to delete by entering one of the following options:</span></span>

   - <span data-ttu-id="07050-164">ID الجدول</span><span class="sxs-lookup"><span data-stu-id="07050-164">Table ID</span></span>
   - <span data-ttu-id="07050-165">نوع السجل</span><span class="sxs-lookup"><span data-stu-id="07050-165">Type of log</span></span>
   - <span data-ttu-id="07050-166">تاريخ  ووقت الإنشاء</span><span class="sxs-lookup"><span data-stu-id="07050-166">Created date and time</span></span>

3. <span data-ttu-id="07050-167">استخدم علامة التبويب **‏‫تنظيف سجل قاعدة البيانات** لتحديد وقت تشغيل مهمة تنظيف السجل.</span><span class="sxs-lookup"><span data-stu-id="07050-167">Use the **Database log cleanup** tab to determine when to run the log cleanup task.</span></span> <span data-ttu-id="07050-168">بشكل افتراضي، تتوفر سجلات قاعده البيانات لمده 30 يوما.</span><span class="sxs-lookup"><span data-stu-id="07050-168">By default, database logs are available for 30 days.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
