---
title: تكوين وإدارة تسجيل قاعده البيانات
description: يمكنك تعقب التغييرات في الجداول والحقول في Dynamics 365 Human Resources بتسجيل قاعده البيانات.
author: Darinkramer
manager: AnnBe
ms.date: 06/10/2020
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
ms.author: dkrame
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3dc4658a0a13af95978c66f5aab882902f754a2d
ms.sourcegitcommit: 88f38d584c5befb96e4d1daab4b28af5519ef125
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/11/2020
ms.locfileid: "3443559"
---
# <a name="configure-and-manage-database-logging"></a><span data-ttu-id="01c68-103">تكوين وإدارة تسجيل قاعده البيانات</span><span class="sxs-lookup"><span data-stu-id="01c68-103">Configure and manage database logging</span></span>

<span data-ttu-id="01c68-104">يمكنك تعقب التغييرات في الجداول والحقول في Dynamics 365 Human Resources بتسجيل قاعده البيانات.</span><span class="sxs-lookup"><span data-stu-id="01c68-104">You can track changes to tables and fields in Dynamics 365 Human Resources with database logging.</span></span> <span data-ttu-id="01c68-105">يصف هذا الموضوع كيفية:</span><span class="sxs-lookup"><span data-stu-id="01c68-105">This topic describes how to:</span></span>

- <span data-ttu-id="01c68-106">إدارة الأمان والأداء لتسجيل قاعده البيانات</span><span class="sxs-lookup"><span data-stu-id="01c68-106">Manage security and performance for database logging</span></span>
- <span data-ttu-id="01c68-107">إعداد تسجيل قاعدة البيانات</span><span class="sxs-lookup"><span data-stu-id="01c68-107">Set up database logging</span></span>
- <span data-ttu-id="01c68-108">تنظيف سجلات قواعد البيانات</span><span class="sxs-lookup"><span data-stu-id="01c68-108">Clean up database logs</span></span>

## <a name="overview-of-database-logging"></a><span data-ttu-id="01c68-109">نظرة عامة حول تسجيل قاعده البيانات</span><span class="sxs-lookup"><span data-stu-id="01c68-109">Overview of database logging</span></span>

<span data-ttu-id="01c68-110">يتعقب تسجيل قاعدة البيانات التغييرات في الجداول والحقول في Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="01c68-110">Database logging tracks specific changes to Microsoft Dynamics 365 Human Resources tables and fields.</span></span> <span data-ttu-id="01c68-111">وتتضمن هذه التغييرات الإدراج أو التحديث أو الحذف.</span><span class="sxs-lookup"><span data-stu-id="01c68-111">These changes include inserting, updating, or deleting.</span></span> <span data-ttu-id="01c68-112">يُخزن تسجيل قاعده البيانات سجلا بالتغييرات في الجداول أو الحقول في جدول سجل قاعده البيانات.</span><span class="sxs-lookup"><span data-stu-id="01c68-112">Database logging stores a record of changes to tables or fields in the database log table.</span></span>

<span data-ttu-id="01c68-113">تشمل استخدامات الأعمال الخاصة بتسجيل قاعده البيانات ما يلي:</span><span class="sxs-lookup"><span data-stu-id="01c68-113">The business uses of database logging include:</span></span>

- <span data-ttu-id="01c68-114">إنشاء سجل تدقيق للتغييرات إلى جداول معينة تحتوي علي معلومات حساسة.</span><span class="sxs-lookup"><span data-stu-id="01c68-114">Creating an audit record of changes to specific tables that contain sensitive information.</span></span>
- <span data-ttu-id="01c68-115">تعقب الحركات الفردية.</span><span class="sxs-lookup"><span data-stu-id="01c68-115">Tracking single transactions.</span></span> <span data-ttu-id="01c68-116">لا يعتبر تسجيل قاعده البيانات معدا لتعقب الحركات المؤتمتة التي يتم تشغيلها في مهام المجموعات.</span><span class="sxs-lookup"><span data-stu-id="01c68-116">Database logging isn't intended for tracking automated transactions that run in batch jobs.</span></span>

## <a name="security-for-database-logging"></a><span data-ttu-id="01c68-117">الأمان لتسجيل قاعده البيانات</span><span class="sxs-lookup"><span data-stu-id="01c68-117">Security for database logging</span></span>

<span data-ttu-id="01c68-118">يمكن أن تحتوي سجلات البيانات على بيانات حساسة.</span><span class="sxs-lookup"><span data-stu-id="01c68-118">Database logs can contain sensitive data.</span></span> <span data-ttu-id="01c68-119">تقييد الوصول ليشمل فقط الأدوار الأمنيه التي تحتاج إلى الوصول إلى بيانات السجل.</span><span class="sxs-lookup"><span data-stu-id="01c68-119">Limit access to include only security roles that need access to the log data.</span></span>

## <a name="database-logging-and-performance"></a><span data-ttu-id="01c68-120">تسجيل قاعده البيانات وأداءها</span><span class="sxs-lookup"><span data-stu-id="01c68-120">Database logging and performance</span></span>

<span data-ttu-id="01c68-121">يمكن أن يكون تسجيل قاعده البيانات مكلفًا من حيث استخدام الموارد وأدارتها رغم أهميتة الكبيرة من منظور الاعمال.</span><span class="sxs-lookup"><span data-stu-id="01c68-121">While valuable from a business perspective, database logging can be expensive in resource use and management.</span></span> <span data-ttu-id="01c68-122">تشمل عواقب الأداء الخاصة بتسجيل قاعده البيانات ما يلي:</span><span class="sxs-lookup"><span data-stu-id="01c68-122">The performance implications of database logging include:</span></span>

- <span data-ttu-id="01c68-123">يمكن أن يزيد حجم جدول سجل قاعده البيانات بسرعة مما يؤدي إلى زيادة في حجم قاعده البيانات.</span><span class="sxs-lookup"><span data-stu-id="01c68-123">The database log table can grow quickly and cause an increase in the size of the database.</span></span> <span data-ttu-id="01c68-124">تعتمد النمو علة كميه البيانات المسجلة التي تقرر الاحتفاظ بها.</span><span class="sxs-lookup"><span data-stu-id="01c68-124">Growth depends on the amount of logged data that you decide to keep.</span></span> <span data-ttu-id="01c68-125">افتراضياً، يحتفظ جدول سجل قاعده البيانات بـ 30 يوما فقط من بيانات السجل.</span><span class="sxs-lookup"><span data-stu-id="01c68-125">By default, the database log table maintains only 30 days of log data.</span></span> 

- <span data-ttu-id="01c68-126">يمكن ان يؤثر تسجيل قاعده البيانات سلبًا على العمليات التلقائية التي تعمل لفترة طويلة‬، مثل عمليات استيراد البيانات التي تعمل لفترة طويلة‬.</span><span class="sxs-lookup"><span data-stu-id="01c68-126">Database logging can adversely affect long-running automated processes, such as long-running data imports.</span></span>

### <a name="best-practices"></a><span data-ttu-id="01c68-127">أفضل الممارسات</span><span class="sxs-lookup"><span data-stu-id="01c68-127">Best practices</span></span>

<span data-ttu-id="01c68-128">ولتحسين الأداء، يمكن تقييد إدخالات السجل بتحديد حقول معينة لتسجيلها بدلاً من جداول بأكملها.</span><span class="sxs-lookup"><span data-stu-id="01c68-128">To improve performance, limit log entries by selecting specific fields to log instead of whole tables.</span></span> <span data-ttu-id="01c68-129">للمساعدة في الحفاظ علي الأداء العام، يكون تسجيل قاعده البيانات محدودًا بـ 20 جدولاً.</span><span class="sxs-lookup"><span data-stu-id="01c68-129">To help maintain overall performance, database logging is limited to 20 tables.</span></span>

> [!NOTE]
> <span data-ttu-id="01c68-130">يمكن تسجيل التحديثات فقط للحقول المفردة.</span><span class="sxs-lookup"><span data-stu-id="01c68-130">Only updates can be logged for individual fields.</span></span>

## <a name="set-up-database-logging"></a><span data-ttu-id="01c68-131">إعداد تسجيل قاعدة البيانات</span><span class="sxs-lookup"><span data-stu-id="01c68-131">Set up database logging</span></span>

<span data-ttu-id="01c68-132">يمكنك استخدام معالج **تسجيل قاعدة البيانات** لإعداد تسجيل قاعده البيانات.</span><span class="sxs-lookup"><span data-stu-id="01c68-132">You can use the **Logging database changes** wizard to set up database logging.</span></span> <span data-ttu-id="01c68-133">ويوفر المعالج طريقةمرنة لاعداد التسجيل للجداول أو الحقول.</span><span class="sxs-lookup"><span data-stu-id="01c68-133">The wizard provides a flexible way to set up logging for tables or fields.</span></span>

1. <span data-ttu-id="01c68-134">انتقل إلى **إدارة النظام > الارتباطات > قواعد البيانات > إعداد سجل قاعدة البيانات**.</span><span class="sxs-lookup"><span data-stu-id="01c68-134">Go to **System administration > Links > Database > Database log setup**.</span></span> <span data-ttu-id="01c68-135">حدد **جديد** لبدء معالج **تغييرات قاعدة بيانات التسجيل**.</span><span class="sxs-lookup"><span data-stu-id="01c68-135">Select **New** to start the **Logging database changes** wizard.</span></span>
2. <span data-ttu-id="01c68-136">أكمل المعالج.</span><span class="sxs-lookup"><span data-stu-id="01c68-136">Complete the wizard.</span></span>

## <a name="clean-up-database-logs"></a><span data-ttu-id="01c68-137">تنظيف سجلات قواعد البيانات</span><span class="sxs-lookup"><span data-stu-id="01c68-137">Clean up database logs</span></span>

<span data-ttu-id="01c68-138">يمكنك حذف كافة سجلات قاعده البيانات أو جزء منها، باستخدام الخيارات التالية:</span><span class="sxs-lookup"><span data-stu-id="01c68-138">You can delete all or part of the database logs, using the following options:</span></span>

- <span data-ttu-id="01c68-139">حدد كافة السجلات لجدول معين.</span><span class="sxs-lookup"><span data-stu-id="01c68-139">Select all logs for a particular table.</span></span>
- <span data-ttu-id="01c68-140">حدد أنواع معينه من سجل قواعد البيانات.</span><span class="sxs-lookup"><span data-stu-id="01c68-140">Select specific types of database log.</span></span>
- <span data-ttu-id="01c68-141">حدد تاريخ ووقت إنشاء سجل.</span><span class="sxs-lookup"><span data-stu-id="01c68-141">Select a date and time that a log was created.</span></span>

<span data-ttu-id="01c68-142">لإعداد ‏‫تنظيف سجل قاعدة البيانات، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="01c68-142">To set up database log cleanup, follow these steps:</span></span> 

1. <span data-ttu-id="01c68-143">انتقل إلى **إدارة النظام > الارتباطات > قواعد البيانات > سجل قاعدة البيانات**.</span><span class="sxs-lookup"><span data-stu-id="01c68-143">Go to **System administration > Links > Database > Database log**.</span></span> <span data-ttu-id="01c68-144">حدد **‏‫تنظيف السجل**.</span><span class="sxs-lookup"><span data-stu-id="01c68-144">Select **Clean up log**.</span></span>

2. <span data-ttu-id="01c68-145">اختر أسلوبا لتحديد السجلات المراد حذفها من خلال إدخال أحد الخيارات التالية:</span><span class="sxs-lookup"><span data-stu-id="01c68-145">Choose a method of selecting logs to delete by entering one of the following options:</span></span>

   - <span data-ttu-id="01c68-146">ID الجدول</span><span class="sxs-lookup"><span data-stu-id="01c68-146">Table ID</span></span>
   - <span data-ttu-id="01c68-147">نوع السجل</span><span class="sxs-lookup"><span data-stu-id="01c68-147">Type of log</span></span>
   - <span data-ttu-id="01c68-148">تاريخ  ووقت الإنشاء</span><span class="sxs-lookup"><span data-stu-id="01c68-148">Created date and time</span></span>

3. <span data-ttu-id="01c68-149">استخدم علامة التبويب **‏‫تنظيف سجل قاعدة البيانات** لتحديد وقت تشغيل مهمة تنظيف السجل.</span><span class="sxs-lookup"><span data-stu-id="01c68-149">Use the **Database log cleanup** tab to determine when to run the log cleanup task.</span></span> <span data-ttu-id="01c68-150">بشكل افتراضي، تتوفر سجلات قاعده البيانات لمده 30 يوما.</span><span class="sxs-lookup"><span data-stu-id="01c68-150">By default, database logs are available for 30 days.</span></span>
