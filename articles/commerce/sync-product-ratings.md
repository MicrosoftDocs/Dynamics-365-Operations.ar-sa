---
title: مزامنة تقييمات المنتجات في Dynamics 365 Commerce
description: يوضح هذا الموضوع كيفية مزامنة تقييمات المنتجات في Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: dec87b548f3a218e1f833b752305f373e893b14c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4409959"
---
# <a name="sync-product-ratings-in-dynamics-365-commerce"></a><span data-ttu-id="c47ee-103">مزامنة تقييمات المنتجات في Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="c47ee-103">Sync product ratings in Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c47ee-104">يوضح هذا الموضوع كيفية مزامنة تقييمات المنتجات في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c47ee-104">This topic describes how to sync product ratings in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c47ee-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="c47ee-105">Overview</span></span>

<span data-ttu-id="c47ee-106">لاستهلاك تقييمات المنتجات في النقاط متعددة الاتجاهات، كما هو الحال في نقطة البيع (POS) وفي مراكز الاتصال، فإنه يجب استيراد تقييمات المنتجات من خدمة التقييمات والمراجعات إلى قاعدة بيانات قناة Commerce.</span><span class="sxs-lookup"><span data-stu-id="c47ee-106">To consume product ratings in omnichannels, such as at the point of sale (POS) and in call centers, product ratings from the ratings and reviews service must be imported into the Commerce channel database.</span></span> <span data-ttu-id="c47ee-107">عندما تتوفر تقييمات المنتجات في نقاط متعددة الاتجاهات، فإنها يمكن أن تساعد العملاء بشكل غير مباشر أثناء التفاعلات مع شركاء المبيعات.</span><span class="sxs-lookup"><span data-stu-id="c47ee-107">When product ratings are made available in omnichannels, they can help customers indirectly during their interactions with sales associates.</span></span>

<span data-ttu-id="c47ee-108">يصف هذا الموضوع المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="c47ee-108">This topic describes following tasks:</span></span>

1. <span data-ttu-id="c47ee-109">يمكنك تكوين **مهمة مزامنة تقييمات المنتجات** كمهمة مجموعه لمزامنة تصنيفات المنتجات من **خدمه التقييمات والمراجعات**.</span><span class="sxs-lookup"><span data-stu-id="c47ee-109">Configure **Product ratings sync job** as a batch job to synchronize product ratings from the **Ratings and Reviews service**.</span></span>
1. <span data-ttu-id="c47ee-110">تحقق من أن وظيفة الدفعية الخاصة بمزامنة تصنيف المنتجات ناجحة.</span><span class="sxs-lookup"><span data-stu-id="c47ee-110">Verify that the batch job for product rating synchronization was successful.</span></span>
1. <span data-ttu-id="c47ee-111">اجعل تقييمات المنتجات متوفرة عند نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="c47ee-111">Make product ratings available at the POS.</span></span>

## <a name="configure-a-batch-job-to-synchronize-product-ratings"></a><span data-ttu-id="c47ee-112">تكوين وظيفة دفعية في لمزامنة تقييمات المنتجات</span><span class="sxs-lookup"><span data-stu-id="c47ee-112">Configure a batch job to synchronize product ratings</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c47ee-113">قبل البدء، تأكد من تثبيت الإصدار 10.0.6 أو الأحدث من Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c47ee-113">Before you start, make sure that version 10.0.6 or later of Dynamics 365 Commerce is installed.</span></span>

### <a name="initialize-the-commerce-scheduler"></a><span data-ttu-id="c47ee-114">تهيئة مجدول التجارة</span><span class="sxs-lookup"><span data-stu-id="c47ee-114">Initialize the commerce scheduler</span></span>

<span data-ttu-id="c47ee-115">لتهيئة مجدول التجارة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="c47ee-115">To initialize the commerce scheduler, follow these steps.</span></span>

1. <span data-ttu-id="c47ee-116">انتقل إلى **البيع بالتجزئة والتجارة \> إعداد المقر الرئيسي \> مجدول Commerce \>تهيئة مجدول التجارة**.</span><span class="sxs-lookup"><span data-stu-id="c47ee-116">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Initialize commerce scheduler**.</span></span> <span data-ttu-id="c47ee-117">بدلاً من ذلك، ابحث عن "تهيئة مجدول التجارة".</span><span class="sxs-lookup"><span data-stu-id="c47ee-117">Alternatively, search for "Initialize commerce scheduler."</span></span>
1. <span data-ttu-id="c47ee-118">في مربع الحوار **تهيئة مجدول التجارة**، تأكد من أنه يتم إعداد الخيار **حذف تكوين موجود** على **لا**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c47ee-118">In the **Initialize commerce scheduler** dialog box, make sure that the **Delete existing configuration** option is set to **No**, and then select **OK**.</span></span>

### <a name="verify-the-retailproductrating-subjob"></a><span data-ttu-id="c47ee-119">تحقق من الوظيفة الفرعية RetailProductRating</span><span class="sxs-lookup"><span data-stu-id="c47ee-119">Verify the RetailProductRating subjob</span></span>

<span data-ttu-id="c47ee-120">للتحقق من أن الوظيفة الفرعية **RetailProductRating** موجودة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="c47ee-120">To verify that the **RetailProductRating** subjob exists, follow these steps.</span></span>

1. <span data-ttu-id="c47ee-121">انتقل إلى **البيع بالتجزئة والتجارة \> إعداد المقر الرئيسي \> مجدول Commerce \>الوظائف الفرعية للمجدول**.</span><span class="sxs-lookup"><span data-stu-id="c47ee-121">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Scheduler subjobs**.</span></span> <span data-ttu-id="c47ee-122">وبدلاً من ذلك، ابحث عن "وظائف المجدول الفرعية".</span><span class="sxs-lookup"><span data-stu-id="c47ee-122">Alternatively, search for "Scheduler subjobs."</span></span>
1. <span data-ttu-id="c47ee-123">في قائمة الوظيفة الفرعية، قم بإيجاد عن الوظيفة الفرعية **RetailProductRating** أو قم بالبحث عنها.</span><span class="sxs-lookup"><span data-stu-id="c47ee-123">In the subjob list, find or search for the **RetailProductRating** subjob.</span></span>

<span data-ttu-id="c47ee-124">يبين الرسم التوضيحي التالي مثالاً على تفاصيل الوظيفة الفرعية في Commerce.</span><span class="sxs-lookup"><span data-stu-id="c47ee-124">The following illustration shows an example of the subjob details in Commerce.</span></span>

![تفاصيل الوظيفة الفرعية RetailProductRating](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> <span data-ttu-id="c47ee-126">في حالة عدم العثور على الوظيفة الفرعية **RetailProductRating**، فقد تكون قد قمت بالفعل بتشغيل وظيفة **مزامنة تقييمات المنتجات** ووظيفة **1040 CDX** قبل تهيئة مجدول Commerce.</span><span class="sxs-lookup"><span data-stu-id="c47ee-126">If you don't find the **RetailProductRating** subjob, you might already have run the **Sync product ratings** job and the **1040 CDX** job before you initialized the Commerce scheduler.</span></span> <span data-ttu-id="c47ee-127">في هذه الحالة، اتبع هذه الخطوات لتشغيل وظيفة **مزامنة البيانات بالكامل**.</span><span class="sxs-lookup"><span data-stu-id="c47ee-127">In this case, follow these steps to run the **Full data sync** job.</span></span>

> 1. <span data-ttu-id="c47ee-128">انتقل إلى **البيع بالتجزئة والتجارة \> إعداد المقر الرئيسي \> مجدول Commerce \> قاعدة بيانات القناة**.</span><span class="sxs-lookup"><span data-stu-id="c47ee-128">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span> <span data-ttu-id="c47ee-129">بدلاً من ذلك، ابحث عن "قاعدة بيانات القناة".</span><span class="sxs-lookup"><span data-stu-id="c47ee-129">Alternatively, search for "Channel database."</span></span>
> 1. <span data-ttu-id="c47ee-130">حدد قاعدة بيانات القناة لمزامنتها.</span><span class="sxs-lookup"><span data-stu-id="c47ee-130">Select the channel database to sync.</span></span>
> 1. <span data-ttu-id="c47ee-131">في جزء الإجراء، حدد **مزامنة البيانات بالكامل**.</span><span class="sxs-lookup"><span data-stu-id="c47ee-131">On the action pane, select **Full data sync**.</span></span>
> 1. <span data-ttu-id="c47ee-132">في مربع الحوار المنسدل **تحديد جدول توزيع**، حدد **1040 - منتجات**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c47ee-132">In the **Select a distribution schedule** drop-down dialog box, select **1040 - products**, and then select **OK**.</span></span>
> 1. <span data-ttu-id="c47ee-133">كرر خطوات الإجراء السابق للتحقق من أنه قد تم إنشاء الوظيفة الفرعية **RetailProductRating**.</span><span class="sxs-lookup"><span data-stu-id="c47ee-133">Repeat the steps of the previous procedure to verify that the **RetailProductRating** subjob has been created.</span></span>

### <a name="import-product-ratings"></a><span data-ttu-id="c47ee-134">استيراد تقييمات المنتجات</span><span class="sxs-lookup"><span data-stu-id="c47ee-134">Import product ratings</span></span>

<span data-ttu-id="c47ee-135">لاستيراد تقييمات المنتجات في Commerce من خدمة التقييمات والمراجعات، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="c47ee-135">To import product ratings into Commerce from the ratings and reviews service, follow these steps.</span></span>

1. <span data-ttu-id="c47ee-136">انتقل إلى **البيع بالتجزئة والتجارة \> إعداد المراكز الرئيسية \> مجدول Commerce \> مزامنة وظيفة تقييمات المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="c47ee-136">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Sync product ratings job**.</span></span> <span data-ttu-id="c47ee-137">بدلاً من ذلك، ابحث عن "مزامنة وظيفة تقييمات المنتجات".</span><span class="sxs-lookup"><span data-stu-id="c47ee-137">Alternatively, search for "Sync product ratings job."</span></span>
1. <span data-ttu-id="c47ee-138">في مربع حوار **سحب تقييمات المنتج**، في علامة التبويب السريعة **تشغيل في الخلفية**، حدد **التكرار**.</span><span class="sxs-lookup"><span data-stu-id="c47ee-138">In the **Pull product ratings** dialog box, on the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="c47ee-139">في مربع الحوار **تعريف التكرار**، قم بإعداد نمط التكرار.</span><span class="sxs-lookup"><span data-stu-id="c47ee-139">In the **Define recurrence** dialog box, set up a recurrence pattern.</span></span> <span data-ttu-id="c47ee-140">(القيمة المقترحة هي ساعتين). لا تقم بجدولة تكرار أقل من ساعة واحدة.</span><span class="sxs-lookup"><span data-stu-id="c47ee-140">(The suggested value is two hours.) Don't schedule a recurrence that is less than one hour.</span></span>
1. <span data-ttu-id="c47ee-141">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c47ee-141">Select **OK**.</span></span>
1. <span data-ttu-id="c47ee-142">قم بتعيين الخيار **معالجة دفعة** على **نعم**.</span><span class="sxs-lookup"><span data-stu-id="c47ee-142">Set the **Batch process** option to **Yes**.</span></span> <span data-ttu-id="c47ee-143">ويساعد هذا الإعداد على ضمان أنك ستتمكن من تدقيق السجلات والتحقق من حالة تشغيل وظيفة الدفعية.</span><span class="sxs-lookup"><span data-stu-id="c47ee-143">This setting helps guarantee that you will be able to audit the logs and verify the status of batch job runs.</span></span>
1. <span data-ttu-id="c47ee-144">حدد **موافق** لجدولة الوظيفة الدفعية.</span><span class="sxs-lookup"><span data-stu-id="c47ee-144">Select **OK** to schedule the batch job.</span></span>

<span data-ttu-id="c47ee-145">يبين الرسم التوضيحي التالي مثالاً على تكوين الوظيفة الدفعية في Commerce.</span><span class="sxs-lookup"><span data-stu-id="c47ee-145">The following illustration shows an example of batch job configuration in Commerce.</span></span>

![تكوين وظيفة دفعية لتقييمات المنتجات المتزامنة](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a><span data-ttu-id="c47ee-147">التحقق من أن وظيفة الدفعية الخاصة بمزامنة تصنيف المنتجات ناجحة</span><span class="sxs-lookup"><span data-stu-id="c47ee-147">Verify that the batch job for product rating synchronization was successful</span></span>

<span data-ttu-id="c47ee-148">للتحقق من نجاح وظيفة دفعية **تقييمات المنتجات المتزامنة**، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="c47ee-148">To verify that the **Sync product ratings** batch job was successful, follow these steps.</span></span>

1. <span data-ttu-id="c47ee-149">انتقل إلى **البيع بالتجزئة والتجارة \> مسؤول النظام \> استعلامات \> وظائف دفعية** أو إذا كنت تستخدم وحدة حفظ المخزون (SKU) لـ Retail and Commerce فقط بدلاً من ذلك، **البيع بالتجزئة والتجارة \> الاستعلامات والتقارير \> وظائف دفعية**.</span><span class="sxs-lookup"><span data-stu-id="c47ee-149">Go to **Retail and Commerce \> System administrator \> Inquiries \> Batch jobs** or, if you're using a Commerce-only stock keeping unit (SKU), **Retail and Commerce \> Inquiries and reports \> Batch jobs** instead.</span></span> <span data-ttu-id="c47ee-150">بدلاً من ذلك، ابحث عن "الوظائف الدفعية".</span><span class="sxs-lookup"><span data-stu-id="c47ee-150">Alternatively, search for "Batch jobs."</span></span>
1. <span data-ttu-id="c47ee-151">لعرض تفاصيل الوظيفة الدفعية، في قائمة الوظيفة الدفعية، في العمود **وصف الوظيفة**، ابحث عن وصف يحتوي على "سحب تقييمات المنتجات".</span><span class="sxs-lookup"><span data-stu-id="c47ee-151">To view the details of the batch job, in the batch job list, in the **Job description** column, search for a description that contains "Pull product ratings."</span></span>
1. <span data-ttu-id="c47ee-152">حدد معرف الوظيفة لعرض تفاصيل وظيفة الدفعية،+ مثل تاريخ/وقت البدء المجدول ونص التكرار.</span><span class="sxs-lookup"><span data-stu-id="c47ee-152">Select the job ID to view the batch job details, such as the scheduled start date/time and the recurrence text.</span></span>

<span data-ttu-id="c47ee-153">يبين الرسم التوضيحي التالي مثالاً لتفاصيل وظيفة الدفعية في Commerce عندما تتم جدولة وظيفة الدفعية لتشغيل الفترات مدتها ساعتين.</span><span class="sxs-lookup"><span data-stu-id="c47ee-153">The following illustration shows an example of the batch job details in Commerce when the batch job is scheduled to run at two-hour intervals.</span></span>

![تفاصيل وظيفة الدفعية لتقييمات المنتجات المتزامنة](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a><span data-ttu-id="c47ee-155">جعل تقييمات المنتجات متوفرة عند نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="c47ee-155">Make product ratings available at the POS</span></span>

<span data-ttu-id="c47ee-156">حل التقييمات والمراجعات في Dynamics 365 Commerce حل متعدد الاتجاهات.</span><span class="sxs-lookup"><span data-stu-id="c47ee-156">The ratings and reviews solution in Dynamics 365 Commerce is an omnichannel solution.</span></span> <span data-ttu-id="c47ee-157">ومع ذلك، لا يتم عرض تقييمات المنتجات في نقطة البيع بالوضع الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="c47ee-157">However, products ratings aren't shown at the POS by default.</span></span> <span data-ttu-id="c47ee-158">لمساعده العملاء في المتاجر، راجع التقييمات والمراجعات عندما يتم الحصول عليها بواسطة إقرانات المبيعات، يجب عليك تشغيل تقييمات المنتجات في نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="c47ee-158">To help customers in stores see ratings and reviews when they are being helped by sales associates, you must turn on product ratings at the POS.</span></span>

<span data-ttu-id="c47ee-159">لتشغيل تقييمات المنتج في نقطة البيع‬، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="c47ee-159">To turn on product ratings at the POS, follow these steps.</span></span>

1. <span data-ttu-id="c47ee-160">انتقل إلى **البيع بالتجزئة والتجارة \> إعداد Commerce \> المعلمات \> معلمات Commerce**.</span><span class="sxs-lookup"><span data-stu-id="c47ee-160">Go to **Retail and Commerce \> Commerce setup \> Parameters \> Commerce parameters**.</span></span> <span data-ttu-id="c47ee-161">بدلاً من ذلك، ابحث عن "معلمات Commerce".</span><span class="sxs-lookup"><span data-stu-id="c47ee-161">Alternatively, search for "Commerce parameters."</span></span>
1. <span data-ttu-id="c47ee-162">في علامة التبويب **معلمات التكوين**، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="c47ee-162">On the **Configuration parameters** tab, select **New**.</span></span>
1. <span data-ttu-id="c47ee-163">أدخل اسمًا مثل **RatingsAndReviews.EnableProductRatingsForRetailStores**، وقم بتعيين القيمة على **حقيقة**.</span><span class="sxs-lookup"><span data-stu-id="c47ee-163">Enter a name such as **RatingsAndReviews.EnableProductRatingsForRetailStores**, and set the value to **true**.</span></span>
1. <span data-ttu-id="c47ee-164">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="c47ee-164">Select **Save**.</span></span>
1. <span data-ttu-id="c47ee-165">انتقل إلى **البيع بالتجزئة والتجارة \> تكنولوجيا معلومات البيع بالتجزئة والتجارة \> جدول التوزيع**.</span><span class="sxs-lookup"><span data-stu-id="c47ee-165">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span> <span data-ttu-id="c47ee-166">بدلاً من ذلك، ابحث عن "جدول توزيع".</span><span class="sxs-lookup"><span data-stu-id="c47ee-166">Alternatively, search for "Distribution schedule."</span></span>
1. <span data-ttu-id="c47ee-167">في قائمة الوظيفة ، حدد **1110** (**التكوين العمومي**)، ثم حدد **تشغيل الآن**.</span><span class="sxs-lookup"><span data-stu-id="c47ee-167">In the job list, select **1110** (**Global configuration**), and then select **Run now**.</span></span>
1. <span data-ttu-id="c47ee-168">بعد تشغيل الوظيفة بنجاح، تحقق من أن تقييمات المنتجات يتم عرضها الآن في نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="c47ee-168">After the job has successfully run, verify that products ratings are now shown at the POS.</span></span>

<span data-ttu-id="c47ee-169">يبين الرسم التوضيحي التالي مثالاً لتكوين معلمات Commerce لعرض تقييمات المنتجات في نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="c47ee-169">The following illustration shows an example of the configuration of the Commerce parameters to turn on product ratings at the POS.</span></span>

![تكوين معلمات Commerce لتقييمات المنتجات في نقطة البيع](media/rnr-hq-enable-ratings-in-pos.png)

<span data-ttu-id="c47ee-171">يبين الرسم التوضيحي التالي مثالاً لتقييمات المنتجات في نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="c47ee-171">The following illustration shows an example of product ratings at the POS.</span></span>

![تقييمات المنتجات في نقطة البيع](media/rnr-pos-catalog-ratings.png)

<span data-ttu-id="c47ee-173">يبين الرسم التوضيحي التالي مثالاً لتقييمات المنتجات في قنوات مركز الاتصال.</span><span class="sxs-lookup"><span data-stu-id="c47ee-173">The following illustration shows an example of product ratings in call center channels.</span></span>

![تقييمات المنتجات في قناة مركز الاتصال](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a><span data-ttu-id="c47ee-175">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="c47ee-175">Additional resources</span></span>

[<span data-ttu-id="c47ee-176">نظرة عامة على التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="c47ee-176">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="c47ee-177">الموافقة على استخدام التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="c47ee-177">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="c47ee-178">إدارة التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="c47ee-178">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="c47ee-179">تكوين التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="c47ee-179">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)
