---
title: تكوين تكامل Common Data Service
description: يُمكنك تشغيل التكامل بين Common Data Service ومثيل Microsoft Dynamics 365 Human Resources أو إيقاف تشغيله. يُمكنك أيضًا عرض تفاصيل المزامنة، ومسح بيانات التعقب، وإعادة مزامنة كيان للمساعدة في استكشاف الأخطاء في مشاكل البيانات وإصلاحها بين البيئتين.
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
ms.openlocfilehash: 042daf3fdf7a906086af726472da050467d217e3
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2020
ms.locfileid: "3007932"
---
# <a name="configure-common-data-service-integration"></a><span data-ttu-id="3287b-104">تكوين تكامل Common Data Service</span><span class="sxs-lookup"><span data-stu-id="3287b-104">Configure Common Data Service integration</span></span>

<span data-ttu-id="3287b-105">يُمكنك تشغيل التكامل بين Common Data Service ومثيل Microsoft Dynamics 365 Human Resources أو إيقاف تشغيله.</span><span class="sxs-lookup"><span data-stu-id="3287b-105">You can turn integration between Common Data Service and an instance of Microsoft Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="3287b-106">يُمكنك أيضًا عرض تفاصيل المزامنة، ومسح بيانات التعقب، وإعادة مزامنة كيان للمساعدة في استكشاف الأخطاء في مشاكل البيانات وإصلاحها بين البيئتين.</span><span class="sxs-lookup"><span data-stu-id="3287b-106">You can also view the synchronization details, clear tracking data, and resync an entity to help troubleshoot data issues between the two environments.</span></span>

<span data-ttu-id="3287b-107">عند إيقاف تشغيل التكامل، يُمكن للمستخدمين إجراء تغييرات في Human Resources أو Common Data Service، ولكن لا تتم مزامنة هذه التغييرات بين البيئتين.</span><span class="sxs-lookup"><span data-stu-id="3287b-107">When you turn off integration, users can make changes in Human Resources or Common Data Service, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="3287b-108">وبشكل افتراضي، يتم إيقاف أو تشغيل التكامل بين Human Resources و Common Data Service، بناءً على وجود بيانات العرض التوضيحي في البيئات:</span><span class="sxs-lookup"><span data-stu-id="3287b-108">By default, integration between Human Resources and Common Data Service is turned either off or on, depending on the presence of demo data in the environments:</span></span>

- <span data-ttu-id="3287b-109">**إيقاف** للبيئات الجديدة التي لا تشمل بيانات العرض التوضيحي</span><span class="sxs-lookup"><span data-stu-id="3287b-109">**Off** for new environments that don't include demo data</span></span>
- <span data-ttu-id="3287b-110">**تشغيل** للبيئات الجديدة التي تشمل بيانات العرض التوضيحي</span><span class="sxs-lookup"><span data-stu-id="3287b-110">**On** for new environments that include demo data</span></span>

<span data-ttu-id="3287b-111">سوف تبدأ البيئات الجديدة التي تتضمن بيانات العرض التوضيحي بمزامنة البيانات عند توفيرها.</span><span class="sxs-lookup"><span data-stu-id="3287b-111">New environments that include demo data will start to sync data when they are provisioned.</span></span>

<span data-ttu-id="3287b-112">قد ترغب في إيقاف تشغيل التكامل في هذه الحالات:</span><span class="sxs-lookup"><span data-stu-id="3287b-112">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="3287b-113">تقوم بتعبئة البيانات من خلال Data Management Framework ويجب عليك استيراد البيانات عدة مرات للوصول إلى حالة صحيحة.</span><span class="sxs-lookup"><span data-stu-id="3287b-113">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="3287b-114">توجد مشاكل في البيانات إما في Human Resources أو Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3287b-114">There are issues with data in either Human Resources or Common Data Service.</span></span> <span data-ttu-id="3287b-115">إذا قمت بإيقاف تشغيل التكامل، يُمكنك حذف سجل في إحدى البيئات دون حذفه في الآخر.</span><span class="sxs-lookup"><span data-stu-id="3287b-115">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="3287b-116">عند تشغيل التكامل مرة أخرى، سوف تتم مزامنة السجل الموجود في البيئة التي لم يتم حذفه فيها مرة أخرى إلى البيئة التي تم حذفه فيها.</span><span class="sxs-lookup"><span data-stu-id="3287b-116">When you turn integration back on, the record in the environment where it wasn't deleted will be synced back to the environment where it was deleted.</span></span> <span data-ttu-id="3287b-117">تبدأ المزامنة في المرة التالية التي يتم فيها تشغيل الوظيفة الدفعية **مزامنة طلب تكامل Common Data Service المفقود**.</span><span class="sxs-lookup"><span data-stu-id="3287b-117">Synchronization begins the next time the **Common Data Service integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="3287b-118">عند إيقاف تشغيل تكامل البيانات، تأكد من أنك لم تقم بتحرير نفس السجل في كلتا البيئتين.</span><span class="sxs-lookup"><span data-stu-id="3287b-118">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="3287b-119">عند تشغيل التكامل مرة أخرى، سوف تتم مزامنة آخر سجل قمت بتحريره.</span><span class="sxs-lookup"><span data-stu-id="3287b-119">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="3287b-120">وبالتالي، إذا لم تقم بإجراء نفس التغييرات على السجل في كلا البيئتين، فقد يؤدي ذلك إلى فقد البيانات.</span><span class="sxs-lookup"><span data-stu-id="3287b-120">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-common-data-service-integration-page"></a><span data-ttu-id="3287b-121">الوصول إلى صفحة تكامل Common Data Service</span><span class="sxs-lookup"><span data-stu-id="3287b-121">Access the Common Data Service integration page</span></span>

1. <span data-ttu-id="3287b-122">في مثيل Human Resources الذي ترغب في عرض أو تكوين إعدادات للتكامل مع Common Data Service فيه، حدد التجانب **إدارة النظام**.</span><span class="sxs-lookup"><span data-stu-id="3287b-122">In the Human Resources instance where you want to view or configure settings for the integration with Common Data Service, select the **System administration** tile.</span></span>

    <span data-ttu-id="3287b-123">[![تجانب إدارة النظام](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="3287b-123">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="3287b-124">حدد علامة التبويب **الارتباطات**.</span><span class="sxs-lookup"><span data-stu-id="3287b-124">Select the **Links** tab.</span></span>

    <span data-ttu-id="3287b-125">[![علامة التبويب ارتباطات](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="3287b-125">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="3287b-126">تحت **عمليات التكامل**، حدد **تكوين Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="3287b-126">Under **Integrations**, select **Common Data Service configuration**.</span></span>

    <span data-ttu-id="3287b-127">[![ارتباط تكوين Common Data Service ](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="3287b-127">[![Common Data Service configuration link](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a><span data-ttu-id="3287b-128">تشغيل تكامل البيانات بين Human Resources و Common Data Service أو إيقاف تشغيله.</span><span class="sxs-lookup"><span data-stu-id="3287b-128">Turn data integration between Human Resources and Common Data Service on or off</span></span>

- <span data-ttu-id="3287b-129">لتشغيل التكامل، قم بتعيين خيار **تمكين التكامل إلى Common Data Service** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="3287b-129">To turn on integration, set the **Enable the integration to the Common Data Service** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3287b-130">عند تشغيل التكامل، سوف تتم مزامنة البيانات في المرة التالية التي يتم فيها تشغيل الوظيفة الدفعية **مزامنة طلب تكامل Common Data Service المفقود**.</span><span class="sxs-lookup"><span data-stu-id="3287b-130">When you turn on integration, data will be synced the next time that the **Common Data Service integration missed request sync** batch job runs.</span></span> <span data-ttu-id="3287b-131">يجب أن تكون كافة البيانات متاحة بعد اكتمال الوظيفة الدفعية.</span><span class="sxs-lookup"><span data-stu-id="3287b-131">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="3287b-132">لإيقاف تشغيل التكامل، قم بتعيين الخيار إلى **لا**.</span><span class="sxs-lookup"><span data-stu-id="3287b-132">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="3287b-133">[![تشغيل تكامل Common Data Service أو إيقاف تشغيله](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="3287b-133">[![Turning the Common Data Service integration on or off](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="3287b-134">عرض تفاصيل تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="3287b-134">View data integration details</span></span>

<span data-ttu-id="3287b-135">في علامة التبويب السريعة **الإدارة** في صفحة **تكامل Common Data Service** ، يُمكنك رؤية كيف تكون السجلات مرتبطة ببعضها بين Human Resources وCommon Data Service.</span><span class="sxs-lookup"><span data-stu-id="3287b-135">On the **Administration** FastTab of the **Common Data Service integration** page, you can see how records are linked together between Human Resources and Common Data Service.</span></span>

- <span data-ttu-id="3287b-136">لعرض السجلات الخاصة بكيان ما، حدد الكيان في حقل **اسم كيان CDS**.</span><span class="sxs-lookup"><span data-stu-id="3287b-136">To view the records for an entity, select the entity in the **CDS entity name** field.</span></span> <span data-ttu-id="3287b-137">تعرض الشبكة كافة السجلات المرتبطة بالكيان المُحدد.</span><span class="sxs-lookup"><span data-stu-id="3287b-137">The grid shows all the records that are linked to the selected entity.</span></span>

<span data-ttu-id="3287b-138">[![عرض السجلات لكيان](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span><span class="sxs-lookup"><span data-stu-id="3287b-138">[![Viewing the records for an entity](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span></span>

> [!NOTE]
> <span data-ttu-id="3287b-139">حاليًا، لا يتم سرد كافة كيانات Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3287b-139">Not all Common Data Service entities are currently listed.</span></span> <span data-ttu-id="3287b-140">تظهر فقط الكيانات التي تدعم استخدام الحقول المخصصة في الشبكة.</span><span class="sxs-lookup"><span data-stu-id="3287b-140">Only entities that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="3287b-141">تتوفر الكيانات الجديدة من خلال الإصدارات المستمرة لـ Human Resourcesـ. </span><span class="sxs-lookup"><span data-stu-id="3287b-141">New entities become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="3287b-142">تتضمن الشبكة الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="3287b-142">The grid includes the following fields:</span></span>

- <span data-ttu-id="3287b-143">**اسم كيان CDS** - اسم الكيان في Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3287b-143">**CDS entity name** – The name of the entity in Common Data Service.</span></span>
- <span data-ttu-id="3287b-144">**مرجع كيان CDS** - المُعرف الذي يستخدمه Common Data Service لتحديد سجل.</span><span class="sxs-lookup"><span data-stu-id="3287b-144">**CDS entity reference** – The identifier that Common Data Service uses to identify a record.</span></span> <span data-ttu-id="3287b-145">تُكافئ هذه القيمة قيمة **RecId** لـ Human Resourcesـ.</span><span class="sxs-lookup"><span data-stu-id="3287b-145">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="3287b-146">يُمكنك العثور على المُعرف عندما تقوم بفتح كيان Common Data Service في Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="3287b-146">You can find the identifier when you open the Common Data Service entity in Microsoft Excel.</span></span>
- <span data-ttu-id="3287b-147">**اسم كيان Human Resources** - آخر كيان قام بمزامنة البيانات إلى Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3287b-147">**Human Resources entity name** – The entity that last synced data to Common Data Service.</span></span> <span data-ttu-id="3287b-148">يمكن أن يكون للكيان إما بادئة Common Data Service أو بادئة أخرى.</span><span class="sxs-lookup"><span data-stu-id="3287b-148">The entity can have either the Common Data Service prefix or another prefix.</span></span>
- <span data-ttu-id="3287b-149">**مرجع Human Resources** - قيمة **RecId** المقترنة بالسجل في Human Resources.</span><span class="sxs-lookup"><span data-stu-id="3287b-149">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="3287b-150">**تم حذفه من CDS** - قيمة تشير إلى ما إذا كان السجل قد تم حذفه من Common Data Service أو لا.</span><span class="sxs-lookup"><span data-stu-id="3287b-150">**Was deleted from CDS** – A value that indicates whether the record was deleted from Common Data Service.</span></span>

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a><span data-ttu-id="3287b-151">إزالة اقتران سجل في Human Resources من Common Data Service</span><span class="sxs-lookup"><span data-stu-id="3287b-151">Remove the association of a record in Human Resources from Common Data Service</span></span>

<span data-ttu-id="3287b-152">إذا واجهت مشاكل خلال مزامنة البيانات بين Human Resources و Common Data Service، فقد تكون قادرًا على حلها عن طريق مسح التعقب والسماح بإعادة مزامنة جدول التعقب.</span><span class="sxs-lookup"><span data-stu-id="3287b-152">If you experience issues during data synchronization between Human Resources and Common Data Service, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="3287b-153">إذا قمت بإزالة الاقتران، ثم قمت بتغيير سجل أو حذفه في Common Data Service ، فلن تتم مزامنة التغييرات مع Human Resources.</span><span class="sxs-lookup"><span data-stu-id="3287b-153">If you remove the association, and then change or delete a record in Common Data Service, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="3287b-154">إذا قمت بإجراء تغييرات في Human Resources، يتم إنشاء سجل تعقب جديد، ويتم تحديث السجل في Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3287b-154">If you make changes in Human Resources, a new tracking record is created, and the record is updated in Common Data Service.</span></span>

- <span data-ttu-id="3287b-155">لإزالة اقتران سجل بين Human Resources و Common Data Service، حدد الكيان في حقل **اسم كيان CDS** ، ثم حدد **مسح معلومات التعقب**.</span><span class="sxs-lookup"><span data-stu-id="3287b-155">To remove the association of a record between Human Resources and Common Data Service, select the entity in the **CDS entity name** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="3287b-156">[![مسح معلومات التعقب](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="3287b-156">[![Clearing tracking information](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span></span>

<span data-ttu-id="3287b-157">لتشغيل مزامنة كاملة على الكيان بعد مسح التتبع، راجع الإجراء التالي.</span><span class="sxs-lookup"><span data-stu-id="3287b-157">To run a full synchronization on the entity after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a><span data-ttu-id="3287b-158">مزامنة كيان بين Human Resources و Common Data Service</span><span class="sxs-lookup"><span data-stu-id="3287b-158">Sync an entity between Human Resources and Common Data Service</span></span>

<span data-ttu-id="3287b-159">استخدم هذا الإجراء إذا استغرقت التغييرات من Common Data Service وقتًا طويلًا للظهور في Human Resources، أو إذا كان يجب عليك تحديث جدول التعقب بعد قيامك بمسح التتبع.</span><span class="sxs-lookup"><span data-stu-id="3287b-159">Use this procedure if changes from Common Data Service are taking too long to appear in Human Resources, or if you must refresh the tracking table after you clear the tracking.</span></span>

- <span data-ttu-id="3287b-160">لتشغيل مزامنة كاملة على كيان بين Human Resources و Common Data Service ، حدد الكيان في حقل **اسم كيان CDS** ، ثم حدد **المزامنة الآن**.</span><span class="sxs-lookup"><span data-stu-id="3287b-160">To run a full synchronization on an entity between Human Resources and Common Data Service, select the entity in the **CDS entity name** field, and then select **Sync now**.</span></span>

<span data-ttu-id="3287b-161">[![تشغيل مزامنة كاملة](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="3287b-161">[![Running a full synchronization](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span></span>


