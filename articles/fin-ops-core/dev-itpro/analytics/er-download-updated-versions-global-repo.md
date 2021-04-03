---
title: استيراد إصدارات محدثه من تكوينات ER
description: يشرح هذا الموضوع كيفية استيراد إصدارات محدثة من تكوينات التقارير الإلكترونية (ER) من المستودع العمومي لخدمة التكوين.
author: NickSelin
manager: AnnBe
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 0c65315c4fa6a42b4bbb0d008b58f8df9cc0ea3d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561868"
---
# <a name="import-updated-versions-of-er-configurations"></a><span data-ttu-id="cd1fe-103">استيراد إصدارات محدثه من تكوينات ER</span><span class="sxs-lookup"><span data-stu-id="cd1fe-103">Import updated versions of ER configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd1fe-104">يتم استخدام [مستودعات](general-electronic-reporting.md#Repository) التقارير الإلكترونية (ER) لمشاركة [تكوينات ER](general-electronic-reporting.md#Configuration).</span><span class="sxs-lookup"><span data-stu-id="cd1fe-104">Electronic reporting (ER) [repositories](general-electronic-reporting.md#Repository) are used to share [ER configurations](general-electronic-reporting.md#Configuration).</span></span> <span data-ttu-id="cd1fe-105">يمكنك [استيراد](download-electronic-reporting-configuration-lcs.md) تكوينات ER من مستودعات مختلفة إلى المثيل الخاص بك من Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="cd1fe-105">You can [import](download-electronic-reporting-configuration-lcs.md) ER configurations from different repositories into your instance of Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="cd1fe-106">عند استيراد تكوينات ER، [يمكن لموفري التكوين](general-electronic-reporting.md#Provider) نشر مستودعات [بإصدارات](general-electronic-reporting.md#component-versioning) جديدة بحيث يمكن مشاركتها.</span><span class="sxs-lookup"><span data-stu-id="cd1fe-106">When you import ER configurations, [configuration providers](general-electronic-reporting.md#Provider) can publish new [versions](general-electronic-reporting.md#component-versioning) repositories so that they can be shared.</span></span>

<span data-ttu-id="cd1fe-107">يشرح هذا الموضوع كيفية استيراد إصدارات محدثة من تكوينات التقارير الإلكترونية (ER) من المستودع العمومي لخدمة التكوين.</span><span class="sxs-lookup"><span data-stu-id="cd1fe-107">This topic explains how to import updated versions of ER configurations from the Global repository of the Configuration service.</span></span> <span data-ttu-id="cd1fe-108">لمزيد من المعلومات، راجع [Microsoft Dynamics 365 for Finance and Operations -‏ Regulatory Services، خدمة التكوين](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span><span class="sxs-lookup"><span data-stu-id="cd1fe-108">For more information, see [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, Configuration service](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span></span>

## <a name="review-the-available-updated-versions"></a><span data-ttu-id="cd1fe-109">مراجعة الإصدارات المحدثة المتوفرة</span><span class="sxs-lookup"><span data-stu-id="cd1fe-109">Review the available updated versions</span></span>

1. <span data-ttu-id="cd1fe-110">سجّل الدخول إلى Finance باستخدام أحد الأدوار التالية:</span><span class="sxs-lookup"><span data-stu-id="cd1fe-110">Sign in to Finance by using one of the following roles:</span></span>

    - <span data-ttu-id="cd1fe-111">مطور إعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="cd1fe-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="cd1fe-112">مستشار وظيفي لإعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="cd1fe-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="cd1fe-113">مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="cd1fe-113">System administrator</span></span>

2. <span data-ttu-id="cd1fe-114">انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="cd1fe-114">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="cd1fe-115">في الصفحة **تكوينات الترجمة**، في قسم **الارتباطات المتعلقة**، حدد **استيراد تحديثات إصدارات التكوينات** .</span><span class="sxs-lookup"><span data-stu-id="cd1fe-115">On the **Localization configurations** page, in the **Related links** section, select **Import configurations versions updates**.</span></span>

    ![صفحة تكوينات الترجمة](./media/er-download-updated-versions-global-repo1.png)

4. <span data-ttu-id="cd1fe-117">في مربع الحوار **استيراد تحديثات تكوينات التقارير الإلكترونية**، في حقل **وضع التشغيل**، حدد **إظهار التحديثات المتوفرة فقط**.</span><span class="sxs-lookup"><span data-stu-id="cd1fe-117">In the **Import electronic reporting configurations versions updates** dialog box, in the **Run mode** field, select **Only show available updates**.</span></span> <span data-ttu-id="cd1fe-118">ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="cd1fe-118">Then select **OK**.</span></span> 

    ![يتم تعيين الحقل وضع التشغيل لإظهار التحديثات المتوفرة فقط](./media/er-download-updated-versions-global-repo2.png)

5. <span data-ttu-id="cd1fe-120">راجع الرسائل التي تتلقاها.</span><span class="sxs-lookup"><span data-stu-id="cd1fe-120">Review the messages that you receive.</span></span> <span data-ttu-id="cd1fe-121">توفر هذه الرسائل المعلومات التالية حول تكوينات ER في مثيل Finance الحالي وكيفية مقارنتها بمحتوى المستودع العمومي:</span><span class="sxs-lookup"><span data-stu-id="cd1fe-121">These messages provide the following information about the ER configurations in the current Finance instance and how they compare to the content of the Global repository:</span></span>

    - <span data-ttu-id="cd1fe-122">العدد الإجمالي لتكوينات ER</span><span class="sxs-lookup"><span data-stu-id="cd1fe-122">The total number of ER configurations</span></span>
    - <span data-ttu-id="cd1fe-123">تكوينات ER غير الموجودة في المستودع العمومي</span><span class="sxs-lookup"><span data-stu-id="cd1fe-123">ER configurations that aren't present in the Global repository</span></span>
    - <span data-ttu-id="cd1fe-124">تكوينات ER التي يتوفر لها أحدث إصدار بالفعل في مثيل Finance الحالي (لعرض القائمة الكاملة لتكوينات ER هذه، حدد ارتباط **تفاصيل الرسالة**.)</span><span class="sxs-lookup"><span data-stu-id="cd1fe-124">ER configurations for which the latest version is already available in the current Finance instance (To view the full list of these ER configurations, select the **Message details** link.)</span></span>

        ![رسالة "تم بالفعل استيراد أحدث إصدارات من التكوينات التالية" وتفاصيل الرسالة](./media/er-download-updated-versions-global-repo3.png)

    - <span data-ttu-id="cd1fe-126">تكوينات ER التي يتوفر لها أحدث إصدار بالفعل في المستودع العمومي ويمكن استيراده مثيل Finance الحالي (لعرض القائمة الكاملة لتكوينات ER هذه، حدد ارتباط **تفاصيل الرسالة**.)</span><span class="sxs-lookup"><span data-stu-id="cd1fe-126">ER configurations for which the latest version is available in the Global repository and can be imported into the current Finance instance (To view the full list of these ER configurations, select the **Message details** link.)</span></span>

        ![رسالة "التحديثات المتوفرة" وتفاصيل الرسالة](./media/er-download-updated-versions-global-repo4.png)

## <a name="import-available-updated-versions"></a><span data-ttu-id="cd1fe-128">استيراد الإصدارات المحدثة المتوفرة</span><span class="sxs-lookup"><span data-stu-id="cd1fe-128">Import available updated versions</span></span>

1. <span data-ttu-id="cd1fe-129">سجّل الدخول إلى Finance باستخدام أحد الأدوار التالية:</span><span class="sxs-lookup"><span data-stu-id="cd1fe-129">Sign in to Finance by using one of the following roles:</span></span>

    - <span data-ttu-id="cd1fe-130">مطور إعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="cd1fe-130">Electronic reporting developer</span></span>
    - <span data-ttu-id="cd1fe-131">مستشار وظيفي لإعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="cd1fe-131">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="cd1fe-132">مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="cd1fe-132">System administrator</span></span>

2. <span data-ttu-id="cd1fe-133">انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="cd1fe-133">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="cd1fe-134">في الصفحة **تكوينات الترجمة**، في قسم **الارتباطات المتعلقة**، حدد **استيراد تحديثات إصدارات التكوينات** .</span><span class="sxs-lookup"><span data-stu-id="cd1fe-134">On the **Localization configurations** page, in the **Related links** section, select **Import configurations versions updates**.</span></span>
4. <span data-ttu-id="cd1fe-135">في مربع الحوار **استيراد تحديثات إصدارات تكوينات التقارير الإلكترونية**، في الحقل **وضع التشغيل**، حدد **استيراد التحديثات الأخيرة** لاستيراد أحدث إصدارات من تكوينات ER من المستودع العمومي إلى مثيل Finance الحالي.</span><span class="sxs-lookup"><span data-stu-id="cd1fe-135">In the **Import electronic reporting configurations versions updates** dialog box, in the **Run mode** field, select **Import latest updates** to import the latest versions of ER configurations from the Global repository into the current Finance instance.</span></span>
5. <span data-ttu-id="cd1fe-136">لجدولة مهمة دفعة لعملية الاستيراد، في علامة التبويب السريعة **التشغيل في الخلفية**، قم بتعيين خيار **معالجة الدفعات** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="cd1fe-136">To schedule a batch job for the import, on the **Run in the background** FastTab, set the **Batch processing** option to **Yes**.</span></span> <span data-ttu-id="cd1fe-137">إذا كنت تريد تكرار الاستيراد بشكل دوري، فقم بتكوين التكرار المطلوب.</span><span class="sxs-lookup"><span data-stu-id="cd1fe-137">If you want to repeat the import periodically, configure the required recurrence.</span></span>

    ![تعيين حقل وضع التشغيل لاستيراد آخر التحديثات](./media/er-download-updated-versions-global-repo5.png)

6. <span data-ttu-id="cd1fe-139">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="cd1fe-139">Select **OK**.</span></span>
7. <span data-ttu-id="cd1fe-140">لمعرفه إصدارات التكوين التي تم استيرادها، اتبع إحدى الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="cd1fe-140">To learn what configuration versions have been imported, follow one of these steps:</span></span>

    - <span data-ttu-id="cd1fe-141">إذا قمت بتشغيل الاستيراد بطريقة تفاعليه بدلا من استخدام مهمة دفعة، فراجع الرسائل التي تتلقاها.</span><span class="sxs-lookup"><span data-stu-id="cd1fe-141">If you run the import interactively instead of using a batch job, review the messages that you receive.</span></span>

        ![الرسائل المستلمة أثناء تشغيل الاستيراد التفاعلي](./media/er-download-updated-versions-global-repo6.png)

    - <span data-ttu-id="cd1fe-143">إذا قمت بتشغيل الاستيراد في وضع الدفعة، فاتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="cd1fe-143">If you run the import in batch mode, follow these steps:</span></span>

        1. <span data-ttu-id="cd1fe-144">انتقل إلى **عام** \> **الاستعلامات** \> **الوظائف الدفعية** \> **الوظائف الدفعية الخاصة بي**.</span><span class="sxs-lookup"><span data-stu-id="cd1fe-144">Go to **Common** \> **Inquiries** \> **Batch jobs** \> **My batch jobs**.</span></span>
        2. <span data-ttu-id="cd1fe-145">ابحث عن وظيفة **استيراد تحديثات إصدارات تكوينات التقارير الإلكترونية**، ثم في جزء الإجراءات، في علامة التبويب **الوظيفة الدفعية**، حدد **سجل الوظيفة الدفعية** لعرض سجل الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="cd1fe-145">Find and select the **Import electronic reporting configurations versions updates** job, and then, on the Action Pane, on the **Batch job** tab, select **Batch job history** to view the job history.</span></span>
        3. <span data-ttu-id="cd1fe-146">في صفحة **سجل الوظيفة الدفعية**، حدد **السجل**.</span><span class="sxs-lookup"><span data-stu-id="cd1fe-146">On the **Batch job history** page, select **Log**.</span></span> <span data-ttu-id="cd1fe-147">ثم، في الرسالة التي تتلقاها، حدد ارتباط **تفاصيل الرسالة** لعرض سجل الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="cd1fe-147">Then, in the message that you receive, select the **Message details** link to view the job log.</span></span>

        ![سجل الوظيفة](./media/er-download-updated-versions-global-repo7.png)

> [!IMPORTANT]
> <span data-ttu-id="cd1fe-149">لا نوصي بجدولة وظيفة دفعية متكررة لاستيراد إصدارات محدثة من تكوينات ER مباشرة من المستودع العمومي إلى بيئة إنتاج، نظرًا لأن الإصدارات المستوردة ستكون متاحة فورا للاستخدام.</span><span class="sxs-lookup"><span data-stu-id="cd1fe-149">We don't recommend that you schedule a recurring batch job to import updated versions of ER configurations directly from the Global repository into a production environment, because the imported versions will immediately be available for use.</span></span> <span data-ttu-id="cd1fe-150">بدلا من ذلك، استخدم هذا الأسلوب لنشر إصدارات تكوينات ER إلى بيئة وضع الحماية.</span><span class="sxs-lookup"><span data-stu-id="cd1fe-150">Instead, use this approach to deploy versions of ER configurations to a sandbox environment.</span></span> <span data-ttu-id="cd1fe-151">ويمكن بعد ذلك تقييمها في بيئة وضع الحماية قبل نشرها إلى بيئة إنتاج.</span><span class="sxs-lookup"><span data-stu-id="cd1fe-151">They can then be evaluated in the sandbox environment before they are deployed to a production environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cd1fe-152">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="cd1fe-152">Additional resources</span></span>

- [<span data-ttu-id="cd1fe-153">نظرة عامة على إعداد التقارير الإلكترونية (ER)</span><span class="sxs-lookup"><span data-stu-id="cd1fe-153">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="cd1fe-154">تنزيل تكوينات التقارير الإلكترونية من المستودع العمومي لخدمة التكوين</span><span class="sxs-lookup"><span data-stu-id="cd1fe-154">Download ER configurations from the Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]