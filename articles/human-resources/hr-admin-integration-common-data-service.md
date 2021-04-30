---
title: تكوين تكامل Dataverse
description: يُمكنك تشغيل التكامل بين Microsoft Dataverse وDynamics 365 Human Resources أو إيقاف تشغيله. يُمكنك أيضًا عرض تفاصيل المزامنة، ومسح بيانات التعقب، وإعادة مزامنة جدول للمساعدة في استكشاف الأخطاء في مشاكل البيانات وإصلاحها بين البيئتين.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bf406a954f5bb8b49627b58a901d0721cdad407b
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890018"
---
# <a name="configure-dataverse-integration"></a><span data-ttu-id="9ea82-104">تكوين تكامل Dataverse</span><span class="sxs-lookup"><span data-stu-id="9ea82-104">Configure Dataverse integration</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="9ea82-105">يُمكنك تشغيل التكامل بين Microsoft Dataverse وDynamics 365 Human Resources أو إيقاف تشغيله.</span><span class="sxs-lookup"><span data-stu-id="9ea82-105">You can turn integration between Microsoft Dataverse and Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="9ea82-106">يُمكنك أيضًا عرض تفاصيل المزامنة، ومسح بيانات التعقب، وإعادة مزامنة جدول للمساعدة في استكشاف الأخطاء في مشاكل البيانات وإصلاحها بين البيئتين.</span><span class="sxs-lookup"><span data-stu-id="9ea82-106">You can also view the synchronization details, clear tracking data, and resync a table to help troubleshoot data issues between the two environments.</span></span>

> [!NOTE]
> <span data-ttu-id="9ea82-107">لمزيد من المعلومات حول Dataverse (المعروف في السابق باسم Common Data Service) وتحديثات المصطلحات، راجع [الجديد في Microsoft Dataverse؟](/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="9ea82-107">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="9ea82-108">عند إيقاف تشغيل التكامل، يُمكن للمستخدمين إجراء تغييرات في Human Resources أو Dataverse، ولكن لا تتم مزامنة هذه التغييرات بين البيئتين.</span><span class="sxs-lookup"><span data-stu-id="9ea82-108">When you turn off integration, users can make changes in Human Resources or Dataverse, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="9ea82-109">بشكل افتراضي، يكون التكامل بين Human Resources وDataverse متوقفًا عن التشغيل.</span><span class="sxs-lookup"><span data-stu-id="9ea82-109">By default, integration between Human Resources and Dataverse is turned off.</span></span>

<span data-ttu-id="9ea82-110">قد ترغب في إيقاف تشغيل التكامل في هذه الحالات:</span><span class="sxs-lookup"><span data-stu-id="9ea82-110">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="9ea82-111">تقوم بتعبئة البيانات من خلال Data Management Framework ويجب عليك استيراد البيانات عدة مرات للوصول إلى حالة صحيحة.</span><span class="sxs-lookup"><span data-stu-id="9ea82-111">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="9ea82-112">توجد مشاكل في البيانات إما في Human Resources أو Dataverse.</span><span class="sxs-lookup"><span data-stu-id="9ea82-112">There are issues with data in either Human Resources or Dataverse.</span></span> <span data-ttu-id="9ea82-113">إذا قمت بإيقاف تشغيل التكامل، يُمكنك حذف سجل في إحدى البيئات دون حذفه في الآخر.</span><span class="sxs-lookup"><span data-stu-id="9ea82-113">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="9ea82-114">عند تشغيل التكامل مرة أخرى، سوف تتم مزامنة السجل الموجود في البيئة التي لم يتم حذفه فيها مرة أخرى إلى البيئة التي تم حذفه فيها.</span><span class="sxs-lookup"><span data-stu-id="9ea82-114">When you turn integration back on, the record in the environment where it wasn't deleted sync to the environment where it was deleted.</span></span> <span data-ttu-id="9ea82-115">تبدأ المزامنة في المرة التالية التي يتم فيها تشغيل الوظيفة الدفعية **مزامنة طلب تكامل Dataverse المفقود**.</span><span class="sxs-lookup"><span data-stu-id="9ea82-115">Synchronization begins the next time the **Dataverse integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="9ea82-116">عند إيقاف تشغيل تكامل البيانات، تأكد من أنك لم تقم بتحرير نفس السجل في كلتا البيئتين.</span><span class="sxs-lookup"><span data-stu-id="9ea82-116">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="9ea82-117">عند تشغيل التكامل مرة أخرى، سوف تتم مزامنة آخر سجل قمت بتحريره.</span><span class="sxs-lookup"><span data-stu-id="9ea82-117">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="9ea82-118">وبالتالي، إذا لم تقم بإجراء نفس التغييرات على السجل في كلا البيئتين، فقد يؤدي ذلك إلى فقد البيانات.</span><span class="sxs-lookup"><span data-stu-id="9ea82-118">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-dataverse-integration-page"></a><span data-ttu-id="9ea82-119">الوصول إلى صفحة تكامل Dataverse</span><span class="sxs-lookup"><span data-stu-id="9ea82-119">Access the Dataverse integration page</span></span>

1. <span data-ttu-id="9ea82-120">في مثيل Human Resources الذي ترغب في عرض أو تكوين إعدادات للتكامل مع Dataverse فيه، حدد التجانب **إدارة النظام**.</span><span class="sxs-lookup"><span data-stu-id="9ea82-120">In the Human Resources instance where you want to view or configure settings for the integration with Dataverse, select the **System administration** tile.</span></span>

    <span data-ttu-id="9ea82-121">[![تجانب إدارة النظام](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="9ea82-121">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="9ea82-122">حدد علامة التبويب **الارتباطات**.</span><span class="sxs-lookup"><span data-stu-id="9ea82-122">Select the **Links** tab.</span></span>

    <span data-ttu-id="9ea82-123">[![علامة التبويب ارتباطات](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="9ea82-123">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="9ea82-124">تحت **عمليات التكامل**، حدد **تكوين Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="9ea82-124">Under **Integrations**, select **Dataverse configuration**.</span></span>

    <span data-ttu-id="9ea82-125">[![ارتباط تكوين Dataverse ](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)</span><span class="sxs-lookup"><span data-stu-id="9ea82-125">[![Dataverse configuration link](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-dataverse-on-or-off"></a><span data-ttu-id="9ea82-126">تشغيل تكامل البيانات بين Human Resources و Dataverse أو إيقاف تشغيله.</span><span class="sxs-lookup"><span data-stu-id="9ea82-126">Turn data integration between Human Resources and Dataverse on or off</span></span>

- <span data-ttu-id="9ea82-127">لتشغيل التكامل، قم بتعيين خيار **تمكين تكامل Dataverse** إلى  إلى **نعم** في صفحة **تكامل Microsoft Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="9ea82-127">To turn on integration, set the **Enable Dataverse integration** option to **Yes** on the **Microsoft Dataverse integration** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9ea82-128">عند تشغيل التكامل، سوف تتم مزامنة البيانات في المرة التالية التي يتم فيها تشغيل الوظيفة الدفعية **مزامنة طلب تكامل Dataverse المفقود**.</span><span class="sxs-lookup"><span data-stu-id="9ea82-128">When you turn on integration, data will be synced the next time that the **Dataverse integration missed request sync** batch job runs.</span></span> <span data-ttu-id="9ea82-129">يجب أن تكون كافة البيانات متاحة بعد اكتمال الوظيفة الدفعية.</span><span class="sxs-lookup"><span data-stu-id="9ea82-129">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="9ea82-130">لإيقاف تشغيل التكامل، قم بتعيين الخيار إلى **لا**.</span><span class="sxs-lookup"><span data-stu-id="9ea82-130">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="9ea82-131">[![تشغيل تكامل Dataverse أو إيقاف تشغيله](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)</span><span class="sxs-lookup"><span data-stu-id="9ea82-131">[![Turning the Dataverse integration on or off](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)</span></span>

> [!WARNING]
> <span data-ttu-id="9ea82-132">نوصي بضرورة إيقاف تشغيل تكامل Dataverse أثناء تنفيذ مهام ترحيل البيانات.</span><span class="sxs-lookup"><span data-stu-id="9ea82-132">We strongly recommend turning off Dataverse integration while performing data migration tasks.</span></span> <span data-ttu-id="9ea82-133">بإمكان تحميلات البيانات الكبيرة أن تؤثر على الأداء بشكل ملحوظ.</span><span class="sxs-lookup"><span data-stu-id="9ea82-133">Large data uploads can significantly impact performance.</span></span> <span data-ttu-id="9ea82-134">على سبيل المثال، قد يستغرق تحميل 2000 عامل ساعات متعددة عند تمكين التكامل، وأقل من ساعة عند تعطيله.</span><span class="sxs-lookup"><span data-stu-id="9ea82-134">For example, uploading 2000 workers can take several hours when integration is enabled, and less than one hour when it's disabled.</span></span> <span data-ttu-id="9ea82-135">الأرقام المتوفرة في هذا المثال هي لأغراء العرض التوضيحي فقط.</span><span class="sxs-lookup"><span data-stu-id="9ea82-135">The numbers provided in this example are for demonstration purposes only.</span></span> <span data-ttu-id="9ea82-136">يمكن أن يختلف مقدار الوقت الدقيق الذي تستغرقه عملية استيراد السجلات بشكل كبير استنادًا إلى العديد من العوامل.</span><span class="sxs-lookup"><span data-stu-id="9ea82-136">The exact amount of time it takes to import records can vary greatly based on many factors.</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="9ea82-137">عرض تفاصيل تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="9ea82-137">View data integration details</span></span>

<span data-ttu-id="9ea82-138">في علامة التبويب السريعة **الإدارة** في صفحة **تكامل Microsoft Dataverse**، يُمكنك رؤية كيف ترتبط البنود ببعضها بين Human Resources وDataverse.</span><span class="sxs-lookup"><span data-stu-id="9ea82-138">On the **Administration** FastTab of the **Microsoft Dataverse integration** page, you can see how rows are linked together between Human Resources and Dataverse.</span></span>

- <span data-ttu-id="9ea82-139">لعرض الصفوف الخاصة بأحد الجداول، حدد الجدول في حقل **جدول Dataverse**</span><span class="sxs-lookup"><span data-stu-id="9ea82-139">To view the rows for a table, select the table in the **Dataverse table** field.</span></span> <span data-ttu-id="9ea82-140">تعرض الشبكة كافة الصفوف المرتبطة بالجدول المُحدد.</span><span class="sxs-lookup"><span data-stu-id="9ea82-140">The grid shows all the rows that are linked to the selected table.</span></span>

> [!NOTE]
> <span data-ttu-id="9ea82-141">حاليًا، لا يتم سرد كافة جداول Dataverse.</span><span class="sxs-lookup"><span data-stu-id="9ea82-141">Not all Dataverse tables are currently listed.</span></span> <span data-ttu-id="9ea82-142">تظهر فقط الجداول التي تدعم استخدام الحقول المخصصة في الشبكة.</span><span class="sxs-lookup"><span data-stu-id="9ea82-142">Only tables that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="9ea82-143">تتوفر الجداول الجديدة من خلال الإصدارات المستمرة لـ Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9ea82-143">New tables become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="9ea82-144">تتضمن الشبكة الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="9ea82-144">The grid includes the following fields:</span></span>

- <span data-ttu-id="9ea82-145">**جدول Dataverse** – اسم الجدول في Dataverse.</span><span class="sxs-lookup"><span data-stu-id="9ea82-145">**Dataverse table** – The name of the table in Dataverse.</span></span>
- <span data-ttu-id="9ea82-146">**مرجع جدول Dataverse** – المعرف الذي يستخدمه Dataverse لتعريف سجل.</span><span class="sxs-lookup"><span data-stu-id="9ea82-146">**Dataverse table reference** – The identifier that Dataverse uses to identify a record.</span></span> <span data-ttu-id="9ea82-147">تُكافئ هذه القيمة قيمة **RecId** لـ Human Resourcesـ.</span><span class="sxs-lookup"><span data-stu-id="9ea82-147">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="9ea82-148">يُمكنك العثور على المُعرف عندما تقوم بفتح جدول Dataverse في Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="9ea82-148">You can find the identifier when you open the Dataverse table in Microsoft Excel.</span></span>
- <span data-ttu-id="9ea82-149">**اسم كيان Human Resources** - آخر كيان Human Resources تمت مزامنة بياناته إلى Dataverse.</span><span class="sxs-lookup"><span data-stu-id="9ea82-149">**Human Resources entity name** – The Human Resources entity that last synced data to Dataverse.</span></span> <span data-ttu-id="9ea82-150">يمكن أن يكون للكيان إما بادئة Dataverse أو بادئة أخرى.</span><span class="sxs-lookup"><span data-stu-id="9ea82-150">The entity can have either the Dataverse prefix or another prefix.</span></span>
- <span data-ttu-id="9ea82-151">**مرجع Human Resources** - قيمة **RecId** المقترنة بالسجل في Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9ea82-151">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="9ea82-152">**محذوف من Dataverse** – قيمة تشير إلى ما إذا كان الصف قد تم حذفه من Dataverse أم لا.</span><span class="sxs-lookup"><span data-stu-id="9ea82-152">**Deleted from Dataverse** – A value that indicates whether the row was deleted from Dataverse.</span></span>

> [!NOTE]
> <span data-ttu-id="9ea82-153">السجلات في Human Resources التي تتوافق مع الصفوف في Dataverse.</span><span class="sxs-lookup"><span data-stu-id="9ea82-153">Records in Human Resources correspond to rows in Dataverse.</span></span>

## <a name="remove-the-association-of-a-human-resources-record-from-a-dataverse-row"></a><span data-ttu-id="9ea82-154">إزالة اقتران سجل Human Resources من صف Dataverse</span><span class="sxs-lookup"><span data-stu-id="9ea82-154">Remove the association of a Human Resources record from a Dataverse row</span></span>

<span data-ttu-id="9ea82-155">إذا واجهت مشاكل خلال مزامنة البيانات بين Human Resources و Dataverse، فقد تكون قادرًا على حلها عن طريق مسح التعقب والسماح بإعادة مزامنة جدول التعقب.</span><span class="sxs-lookup"><span data-stu-id="9ea82-155">If you experience issues during data synchronization between Human Resources and Dataverse, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="9ea82-156">إذا قمت بإزالة الاقتران، ثم قمت بتغيير صف أو حذفه في Dataverse، فلن تتم مزامنة التغييرات مع Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9ea82-156">If you remove the association, and then change or delete a row in Dataverse, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="9ea82-157">إذا قمت بإجراء تغييرات في Human Resources، يتم إنشاء سجل تعقب جديد، ويتم تحديث الصف في Dataverse.</span><span class="sxs-lookup"><span data-stu-id="9ea82-157">If you make changes in Human Resources, a new tracking record is created, and the row is updated in Dataverse.</span></span>

- <span data-ttu-id="9ea82-158">لإزالة اقتران سجل Human Resources و صف Dataverse، حدد الجدول في حقل **جدول Dataverse**، ثم حدد **مسح معلومات التعقب**.</span><span class="sxs-lookup"><span data-stu-id="9ea82-158">To remove the association of a Human Resources record and a Dataverse row, select the table in the **Dataverse table** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="9ea82-159">[![مسح معلومات التعقب](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="9ea82-159">[![Clearing tracking information](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)</span></span>

<span data-ttu-id="9ea82-160">لتشغيل مزامنة كاملة على الجدول بعد مسح التتبع، راجع الإجراء التالي.</span><span class="sxs-lookup"><span data-stu-id="9ea82-160">To run a full synchronization on the table after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-a-table-between-human-resources-and-dataverse"></a><span data-ttu-id="9ea82-161">مزامنة جدول بين Human Resources وDataverse</span><span class="sxs-lookup"><span data-stu-id="9ea82-161">Sync a table between Human Resources and Dataverse</span></span>

<span data-ttu-id="9ea82-162">استخدم هذا الإجراء في الحالات التالية:</span><span class="sxs-lookup"><span data-stu-id="9ea82-162">Use this procedure when:</span></span>

- <span data-ttu-id="9ea82-163">يستغرق ظهور التغييرات من Dataverse في Human Resources وقتًا طويلاً.</span><span class="sxs-lookup"><span data-stu-id="9ea82-163">Changes from Dataverse take too long to appear in Human Resources.</span></span>

- <span data-ttu-id="9ea82-164">يجب تحديث جدول التعقب بعد مسح التعقب.</span><span class="sxs-lookup"><span data-stu-id="9ea82-164">You must refresh the tracking table after clearing the tracking.</span></span>

<span data-ttu-id="9ea82-165">لتشغيل مزامنة كاملة على جدول بين Human Resources وDataverse:</span><span class="sxs-lookup"><span data-stu-id="9ea82-165">To run a full synchronization on a table between Human Resources and Dataverse:</span></span>

1. <span data-ttu-id="9ea82-166">حدد نوع الجدول في الحقل **جدول Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="9ea82-166">Select the table in the **Dataverse table** field.</span></span>

2. <span data-ttu-id="9ea82-167">حدد **المزامنة الآن**.</span><span class="sxs-lookup"><span data-stu-id="9ea82-167">Select **Sync now**.</span></span>

<span data-ttu-id="9ea82-168">[![تشغيل مزامنة كاملة](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="9ea82-168">[![Running a full synchronization](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="9ea82-169">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="9ea82-169">See also</span></span>

[<span data-ttu-id="9ea82-170">جداول Dataverse</span><span class="sxs-lookup"><span data-stu-id="9ea82-170">Dataverse tables</span></span>](hr-developer-entities.md)<br>
[<span data-ttu-id="9ea82-171">تكوين جداول Dataverse الظاهرية</span><span class="sxs-lookup"><span data-stu-id="9ea82-171">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="9ea82-172">الأسئلة المتداولة حول الجداول الظاهرية في Human Resources</span><span class="sxs-lookup"><span data-stu-id="9ea82-172">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="9ea82-173">ما هو Microsoft Dataverse؟</span><span class="sxs-lookup"><span data-stu-id="9ea82-173">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="9ea82-174">تحديثات المصطلحات</span><span class="sxs-lookup"><span data-stu-id="9ea82-174">Terminology updates</span></span>](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]