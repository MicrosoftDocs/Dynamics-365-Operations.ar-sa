---
title: تكوين تكامل Common Data Service
description: يُمكنك تشغيل التكامل بين Common Data Service وDynamics 365 Human Resources أو إيقاف تشغيله. يُمكنك أيضًا عرض تفاصيل المزامنة، ومسح بيانات التعقب، وإعادة مزامنة كيان للمساعدة في استكشاف الأخطاء في مشاكل البيانات وإصلاحها بين البيئتين.
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 7aad8217d48917d6855046a6810fe994f5564d94
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431304"
---
# <a name="configure-common-data-service-integration"></a><span data-ttu-id="4f02f-104">تكوين تكامل Common Data Service</span><span class="sxs-lookup"><span data-stu-id="4f02f-104">Configure Common Data Service integration</span></span>

<span data-ttu-id="4f02f-105">يُمكنك تشغيل التكامل بين Common Data Service وDynamics 365 Human Resources أو إيقاف تشغيله.</span><span class="sxs-lookup"><span data-stu-id="4f02f-105">You can turn integration between Common Data Service and Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="4f02f-106">يُمكنك أيضًا عرض تفاصيل المزامنة، ومسح بيانات التعقب، وإعادة مزامنة كيان للمساعدة في استكشاف الأخطاء في مشاكل البيانات وإصلاحها بين البيئتين.</span><span class="sxs-lookup"><span data-stu-id="4f02f-106">You can also view the synchronization details, clear tracking data, and resync an entity to help troubleshoot data issues between the two environments.</span></span>

<span data-ttu-id="4f02f-107">عند إيقاف تشغيل التكامل، يُمكن للمستخدمين إجراء تغييرات في Human Resources أو Common Data Service، ولكن لا تتم مزامنة هذه التغييرات بين البيئتين.</span><span class="sxs-lookup"><span data-stu-id="4f02f-107">When you turn off integration, users can make changes in Human Resources or Common Data Service, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="4f02f-108">بشكل افتراضي، يكون التكامل بين Human Resources وCommon Data Service متوقفًا عن التشغيل.</span><span class="sxs-lookup"><span data-stu-id="4f02f-108">By default, integration between Human Resources and Common Data Service is turned off.</span></span>

<span data-ttu-id="4f02f-109">قد ترغب في إيقاف تشغيل التكامل في هذه الحالات:</span><span class="sxs-lookup"><span data-stu-id="4f02f-109">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="4f02f-110">تقوم بتعبئة البيانات من خلال Data Management Framework ويجب عليك استيراد البيانات عدة مرات للوصول إلى حالة صحيحة.</span><span class="sxs-lookup"><span data-stu-id="4f02f-110">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="4f02f-111">توجد مشاكل في البيانات إما في Human Resources أو Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4f02f-111">There are issues with data in either Human Resources or Common Data Service.</span></span> <span data-ttu-id="4f02f-112">إذا قمت بإيقاف تشغيل التكامل، يُمكنك حذف سجل في إحدى البيئات دون حذفه في الآخر.</span><span class="sxs-lookup"><span data-stu-id="4f02f-112">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="4f02f-113">عند تشغيل التكامل مرة أخرى، سوف تتم مزامنة السجل الموجود في البيئة التي لم يتم حذفه فيها مرة أخرى إلى البيئة التي تم حذفه فيها.</span><span class="sxs-lookup"><span data-stu-id="4f02f-113">When you turn integration back on, the record in the environment where it wasn't deleted sync to the environment where it was deleted.</span></span> <span data-ttu-id="4f02f-114">تبدأ المزامنة في المرة التالية التي يتم فيها تشغيل الوظيفة الدفعية **مزامنة طلب تكامل Common Data Service المفقود**.</span><span class="sxs-lookup"><span data-stu-id="4f02f-114">Synchronization begins the next time the **Common Data Service integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="4f02f-115">عند إيقاف تشغيل تكامل البيانات، تأكد من أنك لم تقم بتحرير نفس السجل في كلتا البيئتين.</span><span class="sxs-lookup"><span data-stu-id="4f02f-115">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="4f02f-116">عند تشغيل التكامل مرة أخرى، سوف تتم مزامنة آخر سجل قمت بتحريره.</span><span class="sxs-lookup"><span data-stu-id="4f02f-116">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="4f02f-117">وبالتالي، إذا لم تقم بإجراء نفس التغييرات على السجل في كلا البيئتين، فقد يؤدي ذلك إلى فقد البيانات.</span><span class="sxs-lookup"><span data-stu-id="4f02f-117">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-common-data-service-integration-page"></a><span data-ttu-id="4f02f-118">الوصول إلى صفحة تكامل Common Data Service</span><span class="sxs-lookup"><span data-stu-id="4f02f-118">Access the Common Data Service integration page</span></span>

1. <span data-ttu-id="4f02f-119">في مثيل Human Resources الذي ترغب في عرض أو تكوين إعدادات للتكامل مع Common Data Service فيه، حدد التجانب **إدارة النظام**.</span><span class="sxs-lookup"><span data-stu-id="4f02f-119">In the Human Resources instance where you want to view or configure settings for the integration with Common Data Service, select the **System administration** tile.</span></span>

    <span data-ttu-id="4f02f-120">[![تجانب إدارة النظام](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="4f02f-120">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="4f02f-121">حدد علامة التبويب **الارتباطات**.</span><span class="sxs-lookup"><span data-stu-id="4f02f-121">Select the **Links** tab.</span></span>

    <span data-ttu-id="4f02f-122">[![علامة التبويب ارتباطات](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="4f02f-122">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="4f02f-123">تحت **عمليات التكامل**، حدد **تكوين Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="4f02f-123">Under **Integrations**, select **Common Data Service configuration**.</span></span>

    <span data-ttu-id="4f02f-124">[![ارتباط تكوين Common Data Service ](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="4f02f-124">[![Common Data Service configuration link](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a><span data-ttu-id="4f02f-125">تشغيل تكامل البيانات بين Human Resources و Common Data Service أو إيقاف تشغيله.</span><span class="sxs-lookup"><span data-stu-id="4f02f-125">Turn data integration between Human Resources and Common Data Service on or off</span></span>

- <span data-ttu-id="4f02f-126">لتشغيل التكامل، قم بتعيين خيار **تمكين التكامل إلى Common Data Service** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="4f02f-126">To turn on integration, set the **Enable the integration to the Common Data Service** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4f02f-127">عند تشغيل التكامل، سوف تتم مزامنة البيانات في المرة التالية التي يتم فيها تشغيل الوظيفة الدفعية **مزامنة طلب تكامل Common Data Service المفقود**.</span><span class="sxs-lookup"><span data-stu-id="4f02f-127">When you turn on integration, data will be synced the next time that the **Common Data Service integration missed request sync** batch job runs.</span></span> <span data-ttu-id="4f02f-128">يجب أن تكون كافة البيانات متاحة بعد اكتمال الوظيفة الدفعية.</span><span class="sxs-lookup"><span data-stu-id="4f02f-128">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="4f02f-129">لإيقاف تشغيل التكامل، قم بتعيين الخيار إلى **لا**.</span><span class="sxs-lookup"><span data-stu-id="4f02f-129">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="4f02f-130">[![تشغيل تكامل Common Data Service أو إيقاف تشغيله](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="4f02f-130">[![Turning the Common Data Service integration on or off](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="4f02f-131">عرض تفاصيل تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="4f02f-131">View data integration details</span></span>

<span data-ttu-id="4f02f-132">في علامة التبويب السريعة **الإدارة** في صفحة **تكامل Common Data Service**، يُمكنك رؤية كيف تكون السجلات مرتبطة ببعضها بين Human Resources وCommon Data Service.</span><span class="sxs-lookup"><span data-stu-id="4f02f-132">On the **Administration** FastTab of the **Common Data Service integration** page, you can see how records are linked together between Human Resources and Common Data Service.</span></span>

- <span data-ttu-id="4f02f-133">لعرض السجلات الخاصة بكيان ما، حدد الكيان في حقل **اسم كيان CDS**.</span><span class="sxs-lookup"><span data-stu-id="4f02f-133">To view the records for an entity, select the entity in the **CDS entity name** field.</span></span> <span data-ttu-id="4f02f-134">تعرض الشبكة كافة السجلات المرتبطة بالكيان المُحدد.</span><span class="sxs-lookup"><span data-stu-id="4f02f-134">The grid shows all the records that are linked to the selected entity.</span></span>

<span data-ttu-id="4f02f-135">[![عرض السجلات لكيان](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span><span class="sxs-lookup"><span data-stu-id="4f02f-135">[![Viewing the records for an entity](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span></span>

> [!NOTE]
> <span data-ttu-id="4f02f-136">حاليًا، لا يتم سرد كافة كيانات Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4f02f-136">Not all Common Data Service entities are currently listed.</span></span> <span data-ttu-id="4f02f-137">تظهر فقط الكيانات التي تدعم استخدام الحقول المخصصة في الشبكة.</span><span class="sxs-lookup"><span data-stu-id="4f02f-137">Only entities that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="4f02f-138">تتوفر الكيانات الجديدة من خلال الإصدارات المستمرة لـ Human Resourcesـ. </span><span class="sxs-lookup"><span data-stu-id="4f02f-138">New entities become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="4f02f-139">تتضمن الشبكة الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="4f02f-139">The grid includes the following fields:</span></span>

- <span data-ttu-id="4f02f-140">**اسم كيان CDS** - اسم الكيان في Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4f02f-140">**CDS entity name** – The name of the entity in Common Data Service.</span></span>
- <span data-ttu-id="4f02f-141">**مرجع كيان CDS** - المُعرف الذي يستخدمه Common Data Service لتحديد سجل.</span><span class="sxs-lookup"><span data-stu-id="4f02f-141">**CDS entity reference** – The identifier that Common Data Service uses to identify a record.</span></span> <span data-ttu-id="4f02f-142">تُكافئ هذه القيمة قيمة **RecId** لـ Human Resourcesـ.</span><span class="sxs-lookup"><span data-stu-id="4f02f-142">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="4f02f-143">يُمكنك العثور على المُعرف عندما تقوم بفتح كيان Common Data Service في Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="4f02f-143">You can find the identifier when you open the Common Data Service entity in Microsoft Excel.</span></span>
- <span data-ttu-id="4f02f-144">**اسم كيان Human Resources** - آخر كيان قام بمزامنة البيانات إلى Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4f02f-144">**Human Resources entity name** – The entity that last synced data to Common Data Service.</span></span> <span data-ttu-id="4f02f-145">يمكن أن يكون للكيان إما بادئة Common Data Service أو بادئة أخرى.</span><span class="sxs-lookup"><span data-stu-id="4f02f-145">The entity can have either the Common Data Service prefix or another prefix.</span></span>
- <span data-ttu-id="4f02f-146">**مرجع Human Resources** - قيمة **RecId** المقترنة بالسجل في Human Resources.</span><span class="sxs-lookup"><span data-stu-id="4f02f-146">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="4f02f-147">**تم حذفه من CDS** - قيمة تشير إلى ما إذا كان السجل قد تم حذفه من Common Data Service أو لا.</span><span class="sxs-lookup"><span data-stu-id="4f02f-147">**Was deleted from CDS** – A value that indicates whether the record was deleted from Common Data Service.</span></span>

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a><span data-ttu-id="4f02f-148">إزالة اقتران سجل في Human Resources من Common Data Service</span><span class="sxs-lookup"><span data-stu-id="4f02f-148">Remove the association of a record in Human Resources from Common Data Service</span></span>

<span data-ttu-id="4f02f-149">إذا واجهت مشاكل خلال مزامنة البيانات بين Human Resources و Common Data Service، فقد تكون قادرًا على حلها عن طريق مسح التعقب والسماح بإعادة مزامنة جدول التعقب.</span><span class="sxs-lookup"><span data-stu-id="4f02f-149">If you experience issues during data synchronization between Human Resources and Common Data Service, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="4f02f-150">إذا قمت بإزالة الاقتران، ثم قمت بتغيير سجل أو حذفه في Common Data Service، فلن تتم مزامنة التغييرات مع Human Resources.</span><span class="sxs-lookup"><span data-stu-id="4f02f-150">If you remove the association, and then change or delete a record in Common Data Service, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="4f02f-151">إذا قمت بإجراء تغييرات في Human Resources، يتم إنشاء سجل تعقب جديد، ويتم تحديث السجل في Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4f02f-151">If you make changes in Human Resources, a new tracking record is created, and the record is updated in Common Data Service.</span></span>

- <span data-ttu-id="4f02f-152">لإزالة اقتران سجل بين Human Resources و Common Data Service، حدد الكيان في حقل **اسم كيان CDS**، ثم حدد **مسح معلومات التعقب**.</span><span class="sxs-lookup"><span data-stu-id="4f02f-152">To remove the association of a record between Human Resources and Common Data Service, select the entity in the **CDS entity name** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="4f02f-153">[![مسح معلومات التعقب](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="4f02f-153">[![Clearing tracking information](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span></span>

<span data-ttu-id="4f02f-154">لتشغيل مزامنة كاملة على الكيان بعد مسح التتبع، راجع الإجراء التالي.</span><span class="sxs-lookup"><span data-stu-id="4f02f-154">To run a full synchronization on the entity after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a><span data-ttu-id="4f02f-155">مزامنة كيان بين Human Resources و Common Data Service</span><span class="sxs-lookup"><span data-stu-id="4f02f-155">Sync an entity between Human Resources and Common Data Service</span></span>

<span data-ttu-id="4f02f-156">استخدم هذا الإجراء في الحالات التالية:</span><span class="sxs-lookup"><span data-stu-id="4f02f-156">Use this procedure when:</span></span>

- <span data-ttu-id="4f02f-157">يستغرق ظهور التغييرات من Common Data Service في Human Resources وقتًا طويلاً.</span><span class="sxs-lookup"><span data-stu-id="4f02f-157">Changes from Common Data Service take too long to appear in Human Resources.</span></span>

- <span data-ttu-id="4f02f-158">يجب تحديث جدول التعقب بعد مسح التعقب.</span><span class="sxs-lookup"><span data-stu-id="4f02f-158">You must refresh the tracking table after clearing the tracking.</span></span>

<span data-ttu-id="4f02f-159">لتشغيل مزامنة كاملة على كيان بين Human Resources وCommon Data Service:</span><span class="sxs-lookup"><span data-stu-id="4f02f-159">To run a full synchronization on an entity between Human Resources and Common Data Service:</span></span>

1. <span data-ttu-id="4f02f-160">في حقل **اسم كيان CDS**، حدد الكيان.</span><span class="sxs-lookup"><span data-stu-id="4f02f-160">Select the entity in the **CDS entity name** field.</span></span>

2. <span data-ttu-id="4f02f-161">حدد **المزامنة الآن**.</span><span class="sxs-lookup"><span data-stu-id="4f02f-161">Select **Sync now**.</span></span>

<span data-ttu-id="4f02f-162">[![تشغيل مزامنة كاملة](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="4f02f-162">[![Running a full synchronization](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span></span>


