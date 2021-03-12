---
title: إدارة عقود الإيجار من خلال إطار عمل استيراد الإيجار
description: يشرح هذا الموضوع كيفية استخدام إطار عمل استيراد عقد الإيجار لتعديل عقود إيجار متعددة في نفس الوقت.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7df2f55f596cab54315c2da2ec0492422514f49c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971293"
---
# <a name="manage-leases-through-the-lease-import-framework"></a><span data-ttu-id="71cf7-103">إدارة عقود الإيجار من خلال إطار عمل استيراد الإيجار</span><span class="sxs-lookup"><span data-stu-id="71cf7-103">Manage leases through the Lease import framework</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="71cf7-104">يشرح هذا الموضوع كيفية استخدام إطار عمل استيراد عقد الإيجار لتعديل عقود إيجار متعددة في خطوة واحدة.</span><span class="sxs-lookup"><span data-stu-id="71cf7-104">This topic explains how to use the Lease import framework to adjust multiple leases in one step.</span></span> <span data-ttu-id="71cf7-105">وباستخدام هذه الإمكانية، يمكنك توفير الوقت، ويمكنك أيضًا التأكد من المزيد من التعديلات الدقيقة عن طريق تقليل فرصة الخطأ البشري.</span><span class="sxs-lookup"><span data-stu-id="71cf7-105">By using this capability, you can save time, and you can also ensure more accurate adjustments by reducing the chance of human error.</span></span> <span data-ttu-id="71cf7-106">بالإضافة إلى ذلك، يمكن لهذه القدرة توصيل Microsoft Dynamics 365 Finance بكيانات بيانات خارجية لتحميل البيانات بكفاءة.</span><span class="sxs-lookup"><span data-stu-id="71cf7-106">Additionally, this capability can connect Microsoft Dynamics 365 Finance with external data entities to efficiently upload data.</span></span>

<span data-ttu-id="71cf7-107">يمكن استخدام كيانات البيانات التالية لتكامل تأجير الأصول مع الأنظمة الخارجية:</span><span class="sxs-lookup"><span data-stu-id="71cf7-107">The following data entities can be used to integrate Asset leasing with external systems:</span></span>

- <span data-ttu-id="71cf7-108">مراحل عقد الإيجار</span><span class="sxs-lookup"><span data-stu-id="71cf7-108">Lease staging</span></span>
- <span data-ttu-id="71cf7-109">مراحل عقد الدفع</span><span class="sxs-lookup"><span data-stu-id="71cf7-109">Payment contract staging</span></span>
- <span data-ttu-id="71cf7-110">مراحل عقد قيد التنفيذ</span><span class="sxs-lookup"><span data-stu-id="71cf7-110">Executory contract staging</span></span>

<span data-ttu-id="71cf7-111">يمكنك استخدام عملية الاستيراد لتسوية عقد إيجار أو تحديث المعلومات غير المالية أو إضافة عقود إيجار جديدة.</span><span class="sxs-lookup"><span data-stu-id="71cf7-111">You can use the import process to adjust a lease, update non-financial information, or add new leases.</span></span> <span data-ttu-id="71cf7-112">يمكنك عرض بيانات التأجير وتحريرها قبل استيرادها.</span><span class="sxs-lookup"><span data-stu-id="71cf7-112">You can view and edit the leasing data before you import it.</span></span>

<span data-ttu-id="71cf7-113">يمكن أن يقوم النظام بتشغيل العمليات الثلاثة التالية من خلال مجموعة استيراد عقد الإيجار.</span><span class="sxs-lookup"><span data-stu-id="71cf7-113">The system can run the following three processes through the lease import suite.</span></span>

| <span data-ttu-id="71cf7-114">نوع العملية</span><span class="sxs-lookup"><span data-stu-id="71cf7-114">Process type</span></span>  | <span data-ttu-id="71cf7-115">الوصف</span><span class="sxs-lookup"><span data-stu-id="71cf7-115">Description</span></span> |
|---------------|-------------|
| <span data-ttu-id="71cf7-116">إضافة سجل</span><span class="sxs-lookup"><span data-stu-id="71cf7-116">Add record</span></span>    | <span data-ttu-id="71cf7-117">تعمل عقود الإيجار التي تم ترحيلها والتي تحتيو على نوع العملية هذا على إنشاء عقد الإيجار في النظام.</span><span class="sxs-lookup"><span data-stu-id="71cf7-117">Migrated leases that have this process type create a lease in the system.</span></span> <span data-ttu-id="71cf7-118">ويجب تأكيد جدول الدفع يدويًا، ويجب ترحيل إدخال دفتر يومية التقييم الأولي يدويًا بعد الترحيل.</span><span class="sxs-lookup"><span data-stu-id="71cf7-118">The payment schedule must be manually confirmed, and the initial recognition journal entry must be manually posted after the migration.</span></span> |
| <span data-ttu-id="71cf7-119">تحديث السجل</span><span class="sxs-lookup"><span data-stu-id="71cf7-119">Update record</span></span> | <span data-ttu-id="71cf7-120">تعمل عقود الإيجار التي تم ترحيلها والتي تحتوي على نوع العملية هذا على تحديث قيم الحقول لعقد إيجار موجود بالفعل في النظام.</span><span class="sxs-lookup"><span data-stu-id="71cf7-120">Migrated leases that have this process type update field values for a lease that is already in the system.</span></span> <span data-ttu-id="71cf7-121">يتم تحديث الحقول التي تم تحديدها في الصفحة **تحديث تحديد الحقول** فقط.</span><span class="sxs-lookup"><span data-stu-id="71cf7-121">Only the fields that have been selected on the **Update fields selection** page are updated.</span></span> <span data-ttu-id="71cf7-122">ونوصي بتحديد الحقول غير المالية في الصفحة **تحديث تحديد الحقول**، نظرًا لأن نوع العملية هذا لا يقوم بتعديل عقد الإيجار.</span><span class="sxs-lookup"><span data-stu-id="71cf7-122">We recommended that you select non-financial fields on the **Update fields selection** page, because this process type doesn't adjust the lease.</span></span> |
| <span data-ttu-id="71cf7-123">تسوية السجل</span><span class="sxs-lookup"><span data-stu-id="71cf7-123">Adjust record</span></span> | <span data-ttu-id="71cf7-124">تعمل عقود الإيجار التي تم ترحيلها والتي تحتوي على نوع العملية هذا على تعديل عقد الإيجار.</span><span class="sxs-lookup"><span data-stu-id="71cf7-124">Migrated leases that have this process type adjust the lease.</span></span> <span data-ttu-id="71cf7-125">تؤدي هذه التسوية إلى تعديل الإيجار المالي لعقد الإيجار.</span><span class="sxs-lookup"><span data-stu-id="71cf7-125">This adjustment causes a financial lease modification of the lease.</span></span> <span data-ttu-id="71cf7-126">بعد معالجة عقد الإيجار، يقوم النظام بإنشاء جدول دفع جديد باستخدام البيانات الجديدة من مجموعة استيراد عقد الإيجار.</span><span class="sxs-lookup"><span data-stu-id="71cf7-126">After the lease is processed, the system creates a new payment schedule by using the new data from the lease import suite.</span></span> <span data-ttu-id="71cf7-127">لا يقوم النظام بتأكيد جدول الدفع أو ترحيل إدخال دفتر يومية التسوية.</span><span class="sxs-lookup"><span data-stu-id="71cf7-127">The system doesn't confirm the payment schedule or post the adjustment journal entry.</span></span> |

<span data-ttu-id="71cf7-128">بعد تحميل المعلومات عبر مساحة عمل **إدارة البيانات**، قم بفتح الصفحة **استيراد الرأس** (**تأجير الأصول \> إطار عمل استيراد عقد الإيجار \> استيراد رأس**).</span><span class="sxs-lookup"><span data-stu-id="71cf7-128">After information is uploaded through the **Data management** workspace, open the **Import header** page (**Asset leasing \> Lease import framework \> Import header**).</span></span> <span data-ttu-id="71cf7-129">تسرد هذه الصفحة كافة عمليات استيراد كيانات البيانات الثلاثة التي تم سردها مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="71cf7-129">This page lists all imports of the three data entities that were listed earlier.</span></span>

<span data-ttu-id="71cf7-130">لعرض بيانات تقسيم عقد الإيجار قبل تشغيل المعالجة، حدد **البيانات المرحلية**.</span><span class="sxs-lookup"><span data-stu-id="71cf7-130">To view the lease staging data before processing is run, select **Staging data**.</span></span>

<span data-ttu-id="71cf7-131">تتيح لك دالة المقارنة سجل تقوم باستيراده بالسجل المطابق الموجود مسبقًا في النظام.</span><span class="sxs-lookup"><span data-stu-id="71cf7-131">The compare function lets you compare a record that you're importing with the corresponding record that's already in your system.</span></span> <span data-ttu-id="71cf7-132">لمقارنة سجل عقد إيجار فردي، حدد عقد إيجار، ثم حدد **مقارنة**.</span><span class="sxs-lookup"><span data-stu-id="71cf7-132">To compare an individual lease record, select a lease, and then select **Compare**.</span></span> <span data-ttu-id="71cf7-133">يجب عليك إكمال هذه الخطوة لإنشاء تقرير **الاختلافات** قبل ترحيل سجلات عقد الإيجار.</span><span class="sxs-lookup"><span data-stu-id="71cf7-133">You should complete this step to generate a **Differences** report before you migrate the lease records.</span></span> <span data-ttu-id="71cf7-134">تقوم دالة المقارنة بمقارنة القيم الموجودة في البيانات المرحلية بقيم عقود الإيجار الموجودة حاليًا في النظام.</span><span class="sxs-lookup"><span data-stu-id="71cf7-134">The Compare functionality compares the values in the staging data to the values for leases that are currently in the system.</span></span>

> [!NOTE]
> <span data-ttu-id="71cf7-135">لا تعمل دالة المقارنة مع عقود الإيجار التي تحتوي على نوع عملية **إضافة سجل**، لأنه لا يوجد شيء لمقارنته مع عقد الإيجار ذلك.</span><span class="sxs-lookup"><span data-stu-id="71cf7-135">The Compare functionality doesn't work for leases that have the **Add record** process type, because there is nothing to compare against that lease.</span></span>
>
> <span data-ttu-id="71cf7-136">لمقارنة عقود إيجار متعددة في نفس الوقت، انتقل إلى **تأجير الأصل \> إطار عمل استيراد عقد الإيجار \> دوري \> مقارنة**، ثم حدد **مقارنة**.</span><span class="sxs-lookup"><span data-stu-id="71cf7-136">To compare multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic \> Compare**, and select **Compare**.</span></span>

<span data-ttu-id="71cf7-137">بالنسبة لكل كيان، يمكنك عرض الاختلافات بين الموجودة حاليًا في النظام وما هو موجود في الجداول المرحلية:</span><span class="sxs-lookup"><span data-stu-id="71cf7-137">For each entity, you can view the differences between what is currently in the system and what is in the staging tables.</span></span> <span data-ttu-id="71cf7-138">بالنسبة لكل كيان في الجداول المرحلية، حدد **عرض الاختلافات**.</span><span class="sxs-lookup"><span data-stu-id="71cf7-138">For each entity in the staging tables, select **See differences**.</span></span> <span data-ttu-id="71cf7-139">يعرض مربع الحوار الذي يُظهر القيمة الحالية والقيمة المرحلية المقترحة.</span><span class="sxs-lookup"><span data-stu-id="71cf7-139">The dialog box that appears shows the current value and the proposed staging value.</span></span>

<span data-ttu-id="71cf7-140">يمكنك أيضًا تحديث القيمة المرحلية وذلك بتغييرها في العمود **القيمة الجديدة** ثم تحديد **تحديث القيمة المرحلية**.</span><span class="sxs-lookup"><span data-stu-id="71cf7-140">You can also update the staging value by changing it in the **New Value** column and then selecting **Update staging**.</span></span>

<span data-ttu-id="71cf7-141">يمكنك التحقق من صحة عقود الإيجار لضمان أن السجلات يمكن إحضارها إلى النظام دون تقديم أخطاء.</span><span class="sxs-lookup"><span data-stu-id="71cf7-141">You can validate leases to ensure that the records can be brought into the system without introducing errors.</span></span> <span data-ttu-id="71cf7-142">قبل ترحيل سجل عقد الإيجار، يقوم النظام بتشغيل العديد من عمليات التحقق للتأكد من أنه سيتم استيراد السجل بنجاح.</span><span class="sxs-lookup"><span data-stu-id="71cf7-142">Before a lease record is migrated, the system runs several validations to ensure that the record will be successfully imported.</span></span> <span data-ttu-id="71cf7-143">للتحقق من صحة عقد الإيجار الفردي، حدد **التحقق من الصحة**.</span><span class="sxs-lookup"><span data-stu-id="71cf7-143">To validate an individual lease, select **Validate**.</span></span>

> [!NOTE]
> <span data-ttu-id="71cf7-144">للتحقق من صحة عقود إيجار متعددة في نفس الوقت، انتقل إلى **تأجير الأصل \> إطار عمل استيراد عقد الإيجار \> دوري \> التحقق من الصحة**، ثم حدد **مقارنة**.</span><span class="sxs-lookup"><span data-stu-id="71cf7-144">To validate multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic \> Validate**, and select **Compare**.</span></span>

<span data-ttu-id="71cf7-145">لمعالجة عقد إيجار فردي، حدد **ترحيل سجلات عقد الإيجار** في الصفحة **استيراد الرأس**.</span><span class="sxs-lookup"><span data-stu-id="71cf7-145">To process an individual lease, select **Migrate lease records** on the **Import header** page.</span></span> <span data-ttu-id="71cf7-146">عند ترحيل عقد الإيجار، يقوم النظام بتنفيذ الإجراء المحدد في الحقل **نوع العملية**.</span><span class="sxs-lookup"><span data-stu-id="71cf7-146">When a lease is migrated, the system performs the action that is specified in the **Process type** field.</span></span>

> [!NOTE]
> <span data-ttu-id="71cf7-147">للتحقق من صحة عقود إيجار متعددة في نفس الوقت، انتقل إلى **تأجير الأصل \> إطار عمل استيراد عقد الإيجار \> دوري \> التحقق من الصحة**، ثم حدد **مقارنة**.</span><span class="sxs-lookup"><span data-stu-id="71cf7-147">To validate multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic \> Validate**, and select **Compare**.</span></span>

<span data-ttu-id="71cf7-148">بعد مقارنة عقود الإيجار، فإنه يمكنك تشغيل تقرير لعرض الاختلافات الخاصة بكل عقد إيجار يتم تضمينه في مُعرف الاستيراد.</span><span class="sxs-lookup"><span data-stu-id="71cf7-148">After the leases are compared, you can run a report to view the differences for each lease that is included in the import ID.</span></span> <span data-ttu-id="71cf7-149">لتشغيل التقرير لأحد عقود الإيجار، حدد عقد الإيجار في البيانات المرحلية، ثم حدد **مقارنة تقرير وعرضه \> تقرير الاختلافات**.</span><span class="sxs-lookup"><span data-stu-id="71cf7-149">To run the report for one lease, select that lease in the staging data, and then select **Compare and view report \> Differences report**.</span></span>

> [!NOTE]
> <span data-ttu-id="71cf7-150">للتحقق من صحة عقود إيجار متعددة في نفس الوقت، انتقل إلى **تأجير الأصل \> الاستعمالات والتقارير \> تقرير الاختلافات**، وحدد **مقارنة**.</span><span class="sxs-lookup"><span data-stu-id="71cf7-150">To validate multiple leases at the same time, go to **Asset leasing \> Inquiries and reports \> Differences report**, and select **Compare**.</span></span>

## <a name="set-up-update-fields"></a><span data-ttu-id="71cf7-151">إعداد تحديث الحقول</span><span class="sxs-lookup"><span data-stu-id="71cf7-151">Set up update fields</span></span>

<span data-ttu-id="71cf7-152">إذا كنت تستخدم إطار عمل استيراد عقود الإيجار لتحديث عقود الإيجار، وإن نوع العملية هو **تحديث سجل**، فإنه يمكنك تحديد حقول معينة لتحديثها.</span><span class="sxs-lookup"><span data-stu-id="71cf7-152">If you're using the Lease import framework to update leases, and the process type is **Update record**, you can select specific fields to update.</span></span>

1. <span data-ttu-id="71cf7-153">انتقل إلى **تأجير الأصل \> إطار عمل استيراد عقد الإيجار \> إعداد \> تحديث تحديد الحقل**.</span><span class="sxs-lookup"><span data-stu-id="71cf7-153">Go to **Asset leasing \> Lease import framework \> Setup \> Update field selection**.</span></span>
2. <span data-ttu-id="71cf7-154">في الصفحة التي تظهر، حدد الحقول المراد تحديثها، ثم حدد السهم الأخضر لنقلها إلى القائمة **الحقول المحددة**.</span><span class="sxs-lookup"><span data-stu-id="71cf7-154">On the page that appears, select the fields to update, and then select the green arrow to move them to the **Selected fields** list.</span></span> <span data-ttu-id="71cf7-155">يمكن تحديث الحقول الموجودة فقط في القائمة **الحقول المحددة** باستخدام مجموعة استيراد عقد الإيجار.</span><span class="sxs-lookup"><span data-stu-id="71cf7-155">Only fields in the **Selected fields** list can be updated by using the lease import suite.</span></span>
