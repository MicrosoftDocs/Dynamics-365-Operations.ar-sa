---
title: أداره وحدات مقياس السحابة والحافة لأحمال عمل التصنيع وإدارة المستودع
description: يوفر هذا الموضوع معلومات حول وحدات مقياس السحابة والحافة لأحمال التصنيع وأداره المستودع.
author: cabeln
manager: ''
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: fb0d8e0226b11e93503979c202da917de1df6319
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240427"
---
# <a name="cloud-and-edge-scale-units-for-manufacturing-and-warehouse-management-workloads"></a><span data-ttu-id="c21bb-103">أداره وحدات مقياس السحابة والحافة لأحمال عمل التصنيع وإدارة المستودع</span><span class="sxs-lookup"><span data-stu-id="c21bb-103">Cloud and edge scale units for manufacturing and warehouse management workloads</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="c21bb-104">وحدات مقياس السحابة والحافة تتيح امكانيه توزيع أحمال العمل وتنفيذ المستودعات بين البيئات المختلفة.</span><span class="sxs-lookup"><span data-stu-id="c21bb-104">Cloud and edge scale units enable distribution of shop floor and warehouse execution workloads among different environments.</span></span> <span data-ttu-id="c21bb-105">يمكن ان تساعد هذه الوظيفة علي تحسين الأداء ومنع انقطاع الخدمات وزيادة وقت العمل.</span><span class="sxs-lookup"><span data-stu-id="c21bb-105">This functionality can help improve performance, prevent service interruptions, and maximize uptime.</span></span> <span data-ttu-id="c21bb-106">يتم توفيرها بواسطة الوظائف الاضافيه التالية:</span><span class="sxs-lookup"><span data-stu-id="c21bb-106">It's provided by the following add-ins:</span></span>

- <span data-ttu-id="c21bb-107">وظيفة اضافيه لوحده مقياس السحابة لـ Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="c21bb-107">Cloud Scale Unit Add-in for Dynamics 365 Supply Chain Management</span></span>
- <span data-ttu-id="c21bb-108">وظيفة اضافيه لوحده مقياس الحافة لـ Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="c21bb-108">Edge Scale Unit Add-in for Dynamics 365 Supply Chain Management</span></span>

<span data-ttu-id="c21bb-109">ويجب ان تكون الشركات التي تعمل مع التصنيع والتوزيع قادره علي تشغيل عمليات الاعمال الرئيسية 24/7 ، بدون انقطاع وعند المقياس.</span><span class="sxs-lookup"><span data-stu-id="c21bb-109">Companies that work with manufacturing and distribution must be able to run key business processes 24/7, without interruption and at scale.</span></span> <span data-ttu-id="c21bb-110">تتيح وحدات مقياس السحابة والحافة للشركات امكانيه تشغيل عمليات تصنيع المهام الرئيسية والمصنعة بدون انقطاع ، حتى في حاله مواجهه اتصال الشبكة أو مشكلات زمن الانتقال.</span><span class="sxs-lookup"><span data-stu-id="c21bb-110">Cloud and edge scale units enable companies to run key mission-critical manufacturing and warehouse processes without interruption, even when faced with occasional network connectivity or latency issues.</span></span>

## <a name="public-preview-information"></a><span data-ttu-id="c21bb-111">معلومات المعاينة العامة</span><span class="sxs-lookup"><span data-stu-id="c21bb-111">Public preview information</span></span>

<span data-ttu-id="c21bb-112">توفر المعاينة بيئة واحده تعمل كلوحه وصل تستند إلى السحابة لبيئة Dynamics 365 Supply Chain Management الخاصة بك وبيئة واحده تعمل كوحدة مقياس السحابة.</span><span class="sxs-lookup"><span data-stu-id="c21bb-112">The preview provides one environment that functions as a cloud-based hub of your Dynamics 365 Supply Chain Management environment and one environment that functions as a cloud scale unit.</span></span>

<!-- You will also be able to use Local Business Data (LBD) to configure an on-premises environment as an edge scale unit for the hub you received as part of the preview program.-->

### <a name="preview-availability"></a><span data-ttu-id="c21bb-113">معاينه الاتاحه</span><span class="sxs-lookup"><span data-stu-id="c21bb-113">Preview availability</span></span>

<span data-ttu-id="c21bb-114">تتوفر المعاينة لوحدات القياس الخاصة بالسحابة والحافة لعملاء موجودين في Supply Chain Management في 2020 أكتوبر.</span><span class="sxs-lookup"><span data-stu-id="c21bb-114">The preview for cloud and edge scale units becomes available for existing customers of Supply Chain Management in October 2020.</span></span>

<span data-ttu-id="c21bb-115">للوصول إلى إصدار معاينه أكتوبر 10.0.15/Platform تحديث 39 للنشر في Lifecycle Services (LCS) من [Microsoft Dynamics ](https://lcs.dynamics.com/v2)، يجب ان تكون جزءا من برنامج الوصول المبكر (المعروف أيضا باسم PEAP) لـ Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c21bb-115">To access the October preview release 10.0.15/Platform update 39 for deployment in your [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/v2) environment, you must be part of the preview early access program (also known as PEAP) for Supply Chain Management.</span></span> <span data-ttu-id="c21bb-116">يمكنك الانضمام إلى PEAP إذا كنت عضوا بالفعل في [برنامج Dynamics Insider Program الأوسع](https://experience.dynamics.com/insider).</span><span class="sxs-lookup"><span data-stu-id="c21bb-116">You can join PEAP if you're already a member of the broader [Dynamics Insider Program](https://experience.dynamics.com/insider).</span></span> <span data-ttu-id="c21bb-117">قم فقط بتحديد البرنامج المحدد الذي يسمي "Finance & Operations: معاينه برنامج الوصول المبكر (PEAP)".</span><span class="sxs-lookup"><span data-stu-id="c21bb-117">Just select the specific program that is named "Finance & Operations: Preview early access program (PEAP)."</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c21bb-118">تتوفر امكانيه وحده قياس المكونات لـ Supply Chain Management فقط إذا قمت بالموافقة علي شروط [معاينة السحابة + الحافة لـ Finance and Operations](https://Aka.ms/SCMCnETerms).</span><span class="sxs-lookup"><span data-stu-id="c21bb-118">The scale unit capability for Supply Chain Management is made available only if you agree to the [Cloud + Edge Preview for Finance and Operations terms](https://Aka.ms/SCMCnETerms).</span></span>

### <a name="data-processing-for-the-preview"></a><span data-ttu-id="c21bb-119">معالجه البيانات للمعاينة</span><span class="sxs-lookup"><span data-stu-id="c21bb-119">Data processing for the preview</span></span>

<span data-ttu-id="c21bb-120">خلال المعاينة العامة ، ستتم استضافه بعض خدمات الاداره فقط في الولايات المتحدة.</span><span class="sxs-lookup"><span data-stu-id="c21bb-120">During the public preview, some management services will only be hosted in the United States.</span></span> <span data-ttu-id="c21bb-121">ومع ذلك ، عندما تصبح الميزة متوفرة بصفه عامه ، ستتوفر خدمات الاداره هذه في كافة المواقع الجغرافية المعتمدة من قبل Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c21bb-121">However, when the feature becomes generally available, these management services will be available in all geographies supported by Supply Chain Management.</span></span> <span data-ttu-id="c21bb-122">وهذا ما يؤثر علي نقل وتخزين المعلومات الاداريه المستخدمة من قبل أداره وحده المقياس ، بما في ذلك:</span><span class="sxs-lookup"><span data-stu-id="c21bb-122">This affects the transfer and storage of administrative information used by the scale unit manager, including:</span></span>

- <span data-ttu-id="c21bb-123">أسماء المستاجرين ومعرفاتهم</span><span class="sxs-lookup"><span data-stu-id="c21bb-123">Your tenant names and IDs</span></span>
- <span data-ttu-id="c21bb-124">معرفات مشروع LCS الخاص بك</span><span class="sxs-lookup"><span data-stu-id="c21bb-124">Your LCS project IDs</span></span>
- <span data-ttu-id="c21bb-125">رسائل البريد الكتروني للمسؤول التي يتم استخدامها لتسجيل الدخول</span><span class="sxs-lookup"><span data-stu-id="c21bb-125">Administrator emails used to sign in</span></span>
- <span data-ttu-id="c21bb-126">معرفات البيئة لوحدات الوصل ووحدات القياس</span><span class="sxs-lookup"><span data-stu-id="c21bb-126">Environment IDs for hub and scale units</span></span>
- <span data-ttu-id="c21bb-127">تكوينات أحمال العمل</span><span class="sxs-lookup"><span data-stu-id="c21bb-127">Workload configurations</span></span>
- <span data-ttu-id="c21bb-128">المقاييس المجمعة (مثل زمن الانتقال والانتاجيه) التي يتم عرضها في صفحه تحليل المخطط</span><span class="sxs-lookup"><span data-stu-id="c21bb-128">Collected metrics (such as latency and throughput) which are displayed on the map analysis page</span></span>

<span data-ttu-id="c21bb-129">سيتم حذف البيانات التي تم نقلها إلى وتخزينها في مراكز بيانات امريكيه عند إيقاف تشغيل بيئات المعاينة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="c21bb-129">Data transferred to and stored in the US data centers will be deleted when your preview environments are shut down.</span></span>

### <a name="sign-up-for-the-preview"></a><span data-ttu-id="c21bb-130">التسجيل للمعاينة</span><span class="sxs-lookup"><span data-stu-id="c21bb-130">Sign up for the preview</span></span>

<span data-ttu-id="c21bb-131">للتسجيل للحصول علي معاينه السحابة والحافة لـ Supply Chain Management، يجب ان يكون لدي مؤسستك بيئة سحابه Supply Chain Management المباشرة بالفعل.</span><span class="sxs-lookup"><span data-stu-id="c21bb-131">To sign up for the cloud and edge preview for Supply Chain Management, your organization must already have a live Supply Chain Management cloud environment.</span></span>

<span data-ttu-id="c21bb-132">إمكانيات وحده المقياس في المعاينة العامة حاليا.</span><span class="sxs-lookup"><span data-stu-id="c21bb-132">The scale unit capabilities are currently in public preview.</span></span> <span data-ttu-id="c21bb-133">عند التسجيل ، يجب استخدام حساب مستخدم علي المستاجر المحدد.</span><span class="sxs-lookup"><span data-stu-id="c21bb-133">When you sign up, you must use a user account on the specific tenant.</span></span> <span data-ttu-id="c21bb-134">يجب أيضا ان تكون مالك مشروع أو مسؤول بيئة في LCS لمشروع Dynamics 365 LCS النشط في هذا المستاجر.</span><span class="sxs-lookup"><span data-stu-id="c21bb-134">You must also be a project owner or an environment admin in LCS for an active Dynamics 365 LCS project in that tenant.</span></span>

<span data-ttu-id="c21bb-135">عند الاشتراك في المعاينة ، ستقوم بتحديد المستاجر والانتقال خلال خطوات تسجيل الدخول.</span><span class="sxs-lookup"><span data-stu-id="c21bb-135">When you sign up for the preview, you will select a tenant and go through the sign-up steps.</span></span> <span data-ttu-id="c21bb-136">بمجرد ان تتمكن Microsoft من تخصيص سعة المعاينة ، سنرسل لك رسالة بريد الكتروني تتضمن تفاصيل التقديم ورموز العرض الترويجي لبيئتين (مركز ووحده قياس) لمشروع LCS المناسب.</span><span class="sxs-lookup"><span data-stu-id="c21bb-136">As soon as Microsoft can allocate preview capacity, we will send you an email that includes the provisioning details and the promotion (promo) codes for two environments (a hub and a scale unit) for the appropriate LCS project.</span></span> <span data-ttu-id="c21bb-137">ستتمكن عندئذ من نشر البيئتين كبيئات اليه تحديد صلاحيات المستوي 2.</span><span class="sxs-lookup"><span data-stu-id="c21bb-137">You will then be able to deploy the two environments as tier-2 sandbox environments.</span></span> <span data-ttu-id="c21bb-138">ستكون هذه البيئات صالحه 60 يوما من تاريخ إنشاء أكواد العرض الترويجي.</span><span class="sxs-lookup"><span data-stu-id="c21bb-138">Those environments will be valid 60 days from the creation date of the promo codes.</span></span> <span data-ttu-id="c21bb-139">يجب عدم استخدام البيئتين حتى يتم إكمال الخطوة الموضحة في الفقرة التالية.</span><span class="sxs-lookup"><span data-stu-id="c21bb-139">You should not use the two environments until the step that is described in the next paragraph is completed.</span></span>

<span data-ttu-id="c21bb-140">بعد التاكيد علي البيئة التي تم فيها نشر البيئتين باستخدام رموز العرض الترويجي، سيتم تكوين أحد البيئات للعمل كموزع ، سيتم تكوين البيئة الأخرى للعمل كوحدة قياس.</span><span class="sxs-lookup"><span data-stu-id="c21bb-140">After you confirm with Microsoft that the two environments have been deployed by using the promo codes, one of the environments will be configured to work as a hub, and the other will be configured to work as a scale unit.</span></span> <span data-ttu-id="c21bb-141">ويمكنك بعد ذلك تكوين وحدات المقياس وتوزيع أداره المستودع المحددة وغير أحمال التصنيع باستخدام [مدخل أداره الوحدات الخاص بالمقياس](https://aka.ms/SCMSUM).</span><span class="sxs-lookup"><span data-stu-id="c21bb-141">You can then configure the scale units and deploy selected warehouse management and manufacturing workloads by using the [Scale Unit Manager portal](https://aka.ms/SCMSUM).</span></span>

<span data-ttu-id="c21bb-142">سيتم حذف بيئات المعاينة تلقائيا بعد 60 يوما.</span><span class="sxs-lookup"><span data-stu-id="c21bb-142">Preview environments will automatically be deleted after 60 days.</span></span> <span data-ttu-id="c21bb-143">ومع ذلك ، قد يتم حذفها في الحال إذا كانت تبدو غير مستخدمه.</span><span class="sxs-lookup"><span data-stu-id="c21bb-143">However, they might be deleted sooner if it appears that they aren't being used.</span></span> <span data-ttu-id="c21bb-144">بعد حذف بيئات المعاينة ، يمكنك التسجيل والدخول في قائمه الانتظار لنشر جديد للمعاينة.</span><span class="sxs-lookup"><span data-stu-id="c21bb-144">After your preview environments have been deleted, you can sign up and queue up for a new preview deployment.</span></span>

<span data-ttu-id="c21bb-145">للتسجيل في المعاينة ، انتقل إلى [مدخل أداره الوحدات المقياس](https://aka.ms/SCMSUM).</span><span class="sxs-lookup"><span data-stu-id="c21bb-145">To sign up for the preview, go to the [Scale Unit Manager portal](https://aka.ms/SCMSUM).</span></span>

### <a name="limitations-that-apply-during-the-preview-period"></a><span data-ttu-id="c21bb-146">القيود التي يتم تطبيقها اثناء فتره المعاينة</span><span class="sxs-lookup"><span data-stu-id="c21bb-146">Limitations that apply during the preview period</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c21bb-147">بالنسبة للمرحلة الاوليه من برنامج المعاينة لهذه الميزة ، فان Microsoft تعتمد فقط لوحات الوصل التي لها وحدات مقياس السحابة ، وليس المراكز التي تحتوي علي وحدات مقياس الحافة.</span><span class="sxs-lookup"><span data-stu-id="c21bb-147">For the initial phase of the preview program for this feature, Microsoft is supporting only hubs that have cloud scale units, not hubs that have edge scale units.</span></span> <span data-ttu-id="c21bb-148">وحدات مقياس الحافة مثبته بشكل محلي ومن المتوقع ان تكون متوفرة اثناء مرحله قادمه من البرنامج.</span><span class="sxs-lookup"><span data-stu-id="c21bb-148">Edge scale units are installed on-premises and are expected to become available during an upcoming phase of the program.</span></span>

<span data-ttu-id="c21bb-149">نظرا لان وحدات مقياس السحابة والحافة هي ميزه معاينه ، فان الخدمات المرتبطة بها تتوفر حاليا في البلدان والمناطق المحدودة.</span><span class="sxs-lookup"><span data-stu-id="c21bb-149">Because cloud and edge scale units are a preview feature, services that are related to them are currently available in limited countries and regions.</span></span> <span data-ttu-id="c21bb-150">بتمكين وحدات مقياس السحابة والحافة ، فانك أفيرم علي ان تفهم ان بعض البيانات المرتبطة بتكوين ومعالجه وحدات مقياس السحابة والحافة قد تكون مخزنه في مركز بيانات يقع في الولايات المتحدة.</span><span class="sxs-lookup"><span data-stu-id="c21bb-150">By enabling cloud and edge scale units, you affirm that you understand that some data that is related to the configuration and processing of cloud and edge scale units might be stored in a data center that is located in the United States.</span></span> <span data-ttu-id="c21bb-151">بتمكين وحدات القياس الخاصة بالسحابة والحافة ، فانك توافق أيضا علي شروط [معاينة السحابة +الحافة لـ Finance and Operations](https://Aka.ms/SCMCnETerms).</span><span class="sxs-lookup"><span data-stu-id="c21bb-151">By enabling cloud and edge scale units, you also agree to the [Cloud + Edge Preview for Finance and Operations terms](https://Aka.ms/SCMCnETerms).</span></span> <span data-ttu-id="c21bb-152">لمعرفه المزيد حول وحدات مقياس السحابة والحافة ، راجع [الوثائق](https://aka.ms/scmcne).</span><span class="sxs-lookup"><span data-stu-id="c21bb-152">To learn more about cloud and edge scale units, see the [documentation](https://aka.ms/scmcne).</span></span>

<span data-ttu-id="c21bb-153">تعد خصوصيتك مهمة لشركه Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c21bb-153">Your privacy is important to Microsoft.</span></span> <span data-ttu-id="c21bb-154">لمعرفه المزيد ، أقرا [بيان الخصوصية](https://aka.ms/privacy).</span><span class="sxs-lookup"><span data-stu-id="c21bb-154">To learn more, read our [Privacy Statement](https://aka.ms/privacy).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c21bb-155">لا يتم دعم بعض وظائف الاعمال بشكل كامل في المعاينة العامة عند استخدام حمل العمل على وحدات القياس.</span><span class="sxs-lookup"><span data-stu-id="c21bb-155">Some business functionality isn't fully supported in the public preview when workloads are used on scale units.</span></span> <span data-ttu-id="c21bb-156">لمزيد من المعلومات حول أحمال العمل التشغيلية، راجع الأقسام لاحقاً في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="c21bb-156">For more information about the functional workloads, see the sections later in this topic.</span></span>

## <a name="scale-units-and-dedicated-workloads"></a><span data-ttu-id="c21bb-157">قياس الوحدات وأحمال العمل المخصصة</span><span class="sxs-lookup"><span data-stu-id="c21bb-157">Scale units and dedicated workloads</span></span>

:::image type="content" source="./media/cloud_edge-HeroDiagram.png" alt-text="Dynamics 365 مع وحدات قياس":::

<span data-ttu-id="c21bb-159">تقوم وحدات قياس الوحدات بتوسيع بيئة مركز Supply Chain Management المركزي عن طريق أضافه قدره معالجه مخصصه.</span><span class="sxs-lookup"><span data-stu-id="c21bb-159">Scale units extend your central Supply Chain Management hub environment by adding dedicated processing capacity.</span></span> <span data-ttu-id="c21bb-160">يمكن تشغيل وحدات القياس في السحابة.</span><span class="sxs-lookup"><span data-stu-id="c21bb-160">Scale units can run in the cloud.</span></span> <span data-ttu-id="c21bb-161">وبدلا من ذلك ، يمكنها العمل علي الحافة الداخلية في المرافق المحلية.</span><span class="sxs-lookup"><span data-stu-id="c21bb-161">Alternatively, they can run on the edge at your local facility premises.</span></span> <span data-ttu-id="c21bb-162">يمكن قطع الاتصال بوحدات المقياس بشكل مؤقت من بيئة المركز.</span><span class="sxs-lookup"><span data-stu-id="c21bb-162">Scale units can temporarily be disconnected from the hub environment.</span></span> <span data-ttu-id="c21bb-163">وعند الاتصال ، تقوم وحدات القياس باستلام كافة المعلومات المطلوبة لتشغيل المعالجة المخصصة لأحمال العمل المعينة.</span><span class="sxs-lookup"><span data-stu-id="c21bb-163">When they are connected, scale units receive all the information that is required to run the dedicated processing for assigned workloads.</span></span>

:::image type="content" source="media/cloud_edge-previewoptions.png" alt-text="قياس خيارات الوحدة في المعاينة العامة":::

<span data-ttu-id="c21bb-165">بالنسبة للمعاينة العامة ، يمكنك تكوين بيئة موزع بأحمال العمليات المحددة علي وحده مقياس السحابة باستخدام مدخل أداره الوحدات المقياس.</span><span class="sxs-lookup"><span data-stu-id="c21bb-165">For the public preview, you can configure a hub environment with selected workloads on a cloud scale unit by using the Scale Unit Manager portal.</span></span> <span data-ttu-id="c21bb-166">يمكن أيضا للمشاركين الذين لديهم حق الوصول إلى بيئة بيانات العمل المحلية (LBD) تكوين بيئة LBD كوحدة مقياس الحافة.</span><span class="sxs-lookup"><span data-stu-id="c21bb-166">Preview participants who have access to a Local Business Data (LBD) on-premises environment can also configure the LBD environment as an edge scale unit.</span></span>

<span data-ttu-id="c21bb-167">حمل العمل هو مجموعه محدده من وظائف الاعمال التي يمكن تحليلها إلى وحده المقياس وتفويضها اليها.</span><span class="sxs-lookup"><span data-stu-id="c21bb-167">A workload is a defined set of business functionality that can be factored out and delegated to a scale unit.</span></span> <span data-ttu-id="c21bb-168">في الوقت الحالي ، تتميز المعاينة بنوعين من أنواع أحمال التحميل:</span><span class="sxs-lookup"><span data-stu-id="c21bb-168">Currently, the preview features two types of workloads:</span></span>

- <span data-ttu-id="c21bb-169">التنفيذ التصنيعي</span><span class="sxs-lookup"><span data-stu-id="c21bb-169">Manufacturing execution</span></span>
- <span data-ttu-id="c21bb-170">إدارة المستودعات</span><span class="sxs-lookup"><span data-stu-id="c21bb-170">Warehouse management</span></span>

<span data-ttu-id="c21bb-171">يمكنك تعيين واحد من كل نوع من أنواع حمل العمل لكل وحده قياس.</span><span class="sxs-lookup"><span data-stu-id="c21bb-171">You can assign one of each type of workload per scale unit.</span></span> 

### <a name="dedicated-manufacturing-execution-workload-capabilities-in-a-scale-unit"></a><span data-ttu-id="c21bb-172">إمكانيات حمل عمل تنفيذ التصنيع المخصص في وحده قياس</span><span class="sxs-lookup"><span data-stu-id="c21bb-172">Dedicated manufacturing execution workload capabilities in a scale unit</span></span>

<span data-ttu-id="c21bb-173">بالنسبة لتنفيذ عمليه التصنيع ، تقوم وحدات السحابة والحافة بتسليم الإمكانيات التالية ، حتى إذا لم تكن وحدات الحافة متصلة بالسحابة:</span><span class="sxs-lookup"><span data-stu-id="c21bb-173">For manufacturing execution, cloud and edge scale units deliver the following capabilities, even when the edge units aren't connected to the cloud:</span></span>

- <span data-ttu-id="c21bb-174">ويمكن لمشرفي حاله العمل ومشرفي حاله العمل الوصول إلى خطه الإنتاج الجاهزة.</span><span class="sxs-lookup"><span data-stu-id="c21bb-174">Machine operators and shop floor supervisors can access the operational production plan.</span></span>
- <span data-ttu-id="c21bb-175">يمكن لعوامل تشغيل الجهاز الحفاظ علي الخطة محدثه عن طريق تشغيل وظائف التصنيع المنفصلة وعمليات التصنيع.</span><span class="sxs-lookup"><span data-stu-id="c21bb-175">Machine operators can keep the plan up to date by running discrete and process manufacturing jobs.</span></span>
- <span data-ttu-id="c21bb-176">يمكن لمشرف حاله العمل تسويه خطه التشغيل.</span><span class="sxs-lookup"><span data-stu-id="c21bb-176">The shop floor supervisor can adjust the operational plan.</span></span>
- <span data-ttu-id="c21bb-177">يمكن للعاملين الوصول إلى الوقت والحضور لبدء العمل وإنهاء العمل علي الحافة ، وذلك لضمان حساب دفع العامل الصحيح.</span><span class="sxs-lookup"><span data-stu-id="c21bb-177">Workers can access time and attendance for clock-in and clock-out on the edge, to ensure correct worker pay calculation.</span></span>

<span data-ttu-id="c21bb-178">لمزيد من المعلومات ، راجع [التفاصيل الخاصة بحمل عمل وحده قياس التصنيع](cloud-edge-workload-manufacturing.md).</span><span class="sxs-lookup"><span data-stu-id="c21bb-178">For more information, see the [manufacturing scale unit workload details](cloud-edge-workload-manufacturing.md).</span></span>

### <a name="dedicated-warehouse-management-workload-capabilities-in-a-scale-unit"></a><span data-ttu-id="c21bb-179">إمكانيات حمل عمل إدارة المستودعات المخصصة في وحده قياس</span><span class="sxs-lookup"><span data-stu-id="c21bb-179">Dedicated warehouse management workload capabilities in a scale unit</span></span>

<span data-ttu-id="c21bb-180">بالنسبة لإدارة المستودعات، تقوم وحدات السحابة والحافة بتسليم الإمكانيات التالية ، حتى إذا لم تكن وحدات الحافة متصلة بالسحابة:</span><span class="sxs-lookup"><span data-stu-id="c21bb-180">For warehouse management, cloud and edge scale units deliver the following capabilities, even when edge units aren't connected to the cloud:</span></span>

- <span data-ttu-id="c21bb-181">معالجة أساليب الموجه المحددة لأوامر المبيعات وتزويد الطلبات</span><span class="sxs-lookup"><span data-stu-id="c21bb-181">Processing of selected wave methods is enabled for sales orders and demand replenishment.</span></span>
- <span data-ttu-id="c21bb-182">يمكن للعاملين في المستودع تشغيل المبيعات ومستودع تزويد الطلبات باستخدام تطبيق المستودع.</span><span class="sxs-lookup"><span data-stu-id="c21bb-182">Warehouse workers can run sales and demand replenishment warehouse work by using the warehouse app.</span></span>
- <span data-ttu-id="c21bb-183">يمكن للعاملين في المستودع الاستعلام عن المخزون الفعلي باستخدام تطبيق المستودع.</span><span class="sxs-lookup"><span data-stu-id="c21bb-183">Warehouse workers can inquire into on-hand inventory by using the warehouse app.</span></span>
- <span data-ttu-id="c21bb-184">يمكن للعاملين في المستودع إنشاء وتشغيل حركة المخزون باستخدام تطبيق المستودع.</span><span class="sxs-lookup"><span data-stu-id="c21bb-184">Warehouse workers can create and run inventory movements by using the warehouse app.</span></span>
- <span data-ttu-id="c21bb-185">يمكن لعمال المستودع تسجيل أوامر الشراء وعمل التخزين باستخدام تطبيق المستود</span><span class="sxs-lookup"><span data-stu-id="c21bb-185">Warehouse workers can register purchase orders and do putaway by using the warehouse app.</span></span>

<span data-ttu-id="c21bb-186">لمزيد من المعلومات ، راجع [التفاصيل الخاصة بحمل عمل وحده قياس المستودع](cloud-edge-workload-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="c21bb-186">For more information, see the [warehouse scale unit workload details](cloud-edge-workload-warehousing.md).</span></span>

## <a name="onboard-scale-units-for-your-supply-chain-management-environment"></a><span data-ttu-id="c21bb-187">وحدات قياس الإعداد لبيئة Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="c21bb-187">Onboard scale units for your Supply Chain Management environment</span></span>

### <a name="deploy-the-preview-for-cloud-and-edge-scale-units"></a><span data-ttu-id="c21bb-188">توزيع المعاينة لوحدات مقياس السحابة والحافة</span><span class="sxs-lookup"><span data-stu-id="c21bb-188">Deploy the preview for cloud and edge scale units</span></span>

<span data-ttu-id="c21bb-189">يبين الرسم التوضيحي التالي تدفق التسجيل والتزويد للمعاينة العامة لوحدات مقياس السحابة.</span><span class="sxs-lookup"><span data-stu-id="c21bb-189">The following illustration shows the sign-up and provisioning flow for the public preview for cloud scale units.</span></span>

:::image type="content" source="media/cloud_edge-previewsignup.png" alt-text="معاينه خطوات التسجيل":::

### <a name="select-your-lcs-project-tenant-and-the-detailed-preview-process"></a><span data-ttu-id="c21bb-191">حدد مستاجر المشروع الLCS الخاص بك وعمليه المعاينة التفصيلية</span><span class="sxs-lookup"><span data-stu-id="c21bb-191">Select your LCS project tenant and the detailed preview process</span></span>

<span data-ttu-id="c21bb-192">في المعاينة العامة ، [يعرض مدخل أداره وحده المقياس](https://aka.ms/SCMSUM) قائمه بالمستاجرين التي يكون الحساب الخاص بك جزءا منها ، والمكان الذي تكون فيه مالكا أو مسؤول بيئة لمشروع LCS.</span><span class="sxs-lookup"><span data-stu-id="c21bb-192">In the public preview, the [Scale Unit Manager portal](https://aka.ms/SCMSUM) shows the list of tenants that your account is part of, and where you're an owner or environment admin for an LCS project.</span></span>

<span data-ttu-id="c21bb-193">إذا لم تكن المستاجر الذي تبحث عنه موجودا في هذه القائمة ، انتقل إلى [LCS ](https://lcs.dynamics.com/v2) ، وتاكد من انك اما مسؤول البيئة أو مالك المشروع لمشروع LCS لذلك المستاجر.</span><span class="sxs-lookup"><span data-stu-id="c21bb-193">If the tenant that you're looking for isn't in this list, go to [LCS](https://lcs.dynamics.com/v2), and make sure that you're either an environment admin or a project owner of the LCS project for that tenant.</span></span> <span data-ttu-id="c21bb-194">لاحظ انه لا يتم تخويل حسابات Azure Active Directory (Azure AD) فقط من المستاجر المحدد لإكمال تجربه التسجيل.</span><span class="sxs-lookup"><span data-stu-id="c21bb-194">Note that only Azure Active Directory (Azure AD) accounts from the selected tenant are authorized to complete the sign-up experience.</span></span>

> [!NOTE]
> <span data-ttu-id="c21bb-195">بعد تطبيق التغييرات علي LCS ، قد يستغرق الحصول علي قائمه المستاجرين ما يصل إلى 30 دقيقه.</span><span class="sxs-lookup"><span data-stu-id="c21bb-195">After you apply changes to LCS, it might take up to 30 minutes for the list of tenants to reflect the changes.</span></span>

<span data-ttu-id="c21bb-196">بالنسبة لكل مستاجر ، تعرض القائمة حاله تسجيل الاشتراكات.</span><span class="sxs-lookup"><span data-stu-id="c21bb-196">For each tenant, the list shows the sign-up status.</span></span>

:::image type="content" source="media/cloud_edge-Signup1.png" alt-text="خيار التسجيل للمستأجر":::

<span data-ttu-id="c21bb-198">حدد الرابط **انقر هنا للتسجيل** لتسجيل مستاجر LCS الخاص بك للمساهمة في المعاينة.</span><span class="sxs-lookup"><span data-stu-id="c21bb-198">Select the **Click here to sign up** link to sign up your LCS tenant to participate in the preview.</span></span> <span data-ttu-id="c21bb-199">يجب قبول البنود.</span><span class="sxs-lookup"><span data-stu-id="c21bb-199">You must accept the terms.</span></span> <span data-ttu-id="c21bb-200">كما يجب توفير عنوان البريد الكتروني الخاص بالعمل حتى تتمكن Microsoft من إرسال المراسلات التي تتعلق بعمليه معاينه التسجيل.</span><span class="sxs-lookup"><span data-stu-id="c21bb-200">You must also supply a business email address where Microsoft can send communications that are related the preview sign-up process.</span></span>

:::image type="content" source="media/cloud_edge-Signup2.png" alt-text="إرسال التسجيل لمستأجر":::

<span data-ttu-id="c21bb-202">وسوف تقوم Microsoft بمراجعه طلبك واعلامك بالخطوات التالية عن طريق إرسال بريد الكتروني إلى العنوان الذي قمت بتوفيره في نموذج التسجيل.</span><span class="sxs-lookup"><span data-stu-id="c21bb-202">Microsoft will review your request and inform you about the next steps by sending an email to the address that you supplied on the sign-up form.</span></span>

<span data-ttu-id="c21bb-203">بعد ان يتم منحك الوصول إلى برنامج المعاينة ، ستتلقى رمزين ترويجيين لمشروع LCS الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="c21bb-203">After you've been granted access to the preview program, you will receive two promo codes for your LCS project.</span></span> <span data-ttu-id="c21bb-204">يمكنك الآن استخدام هذه الأكواد الترويجية لتوزيع بيئتين في LCS.</span><span class="sxs-lookup"><span data-stu-id="c21bb-204">You can now use those promo codes to deploy two environments in LCS.</span></span> <span data-ttu-id="c21bb-205">يجب ان تستخدم البيئات 10.0.15 إصدار PEAP أو أحدث.</span><span class="sxs-lookup"><span data-stu-id="c21bb-205">The environments must use PEAP release 10.0.15 or later.</span></span> <span data-ttu-id="c21bb-206">عند الانتهاء من تطبيق الأكواد الترويجية، قم باعلام Microsoft (كما هو موضح) ، بحيث يمكننا الانتهاء من تمكين البيئات لميزات المعاينة.</span><span class="sxs-lookup"><span data-stu-id="c21bb-206">When you've finished applying the promo codes, notify Microsoft (as instructed), so that we can finish enabling the environments for the preview features.</span></span> <span data-ttu-id="c21bb-207">ستساعدك Microsoft علي معرفه متى تكتمل خطوه التكوين هذه.</span><span class="sxs-lookup"><span data-stu-id="c21bb-207">Microsoft will let you know when this configuration step is completed.</span></span>

<span data-ttu-id="c21bb-208">يمكنك الآن بدء تكوين وحدات المقياس وأحمال العمليات في بيئة المعاينة.</span><span class="sxs-lookup"><span data-stu-id="c21bb-208">You can now start to configure scale units and workloads in your preview environment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c21bb-209">عند تكوين وحدات مقياس السحابة ، يمكنك [القيام بكافة الخطوات المطلوبة في مدخل أداره وحده القياس](#scale-unit-manager-portal).</span><span class="sxs-lookup"><span data-stu-id="c21bb-209">When you configure cloud scale units, you can [do all the required steps in the Scale Unit Manager portal](#scale-unit-manager-portal).</span></span>
<!-- 
> If want to use edge scale units with your preview deployment, you must do all scale unit configuration in the user interface on the hub as described in [Configure the hub environment for use with edge scale units](cloud-edge-edge-scale-units-lbd.md#configure-the-hub-environment). You can't use Scale Unit Manager portal if you include an edge scale unit. -->

### <a name="manage-cloud-scale-units-and-workloads-by-using-the-scale-unit-manager-portal"></a><a name="scale-unit-manager-portal"></a><span data-ttu-id="c21bb-210">أداره وحدات قياس السحابة ووحدات التحميل باستخدام مدخل أداره وحدات المقياس</span><span class="sxs-lookup"><span data-stu-id="c21bb-210">Manage cloud scale units and workloads by using the Scale Unit Manager portal</span></span>

<span data-ttu-id="c21bb-211">انتقل إلى [مدخل أداره وحدات المقياس](https://aka.ms/SCMSUM)، ثم قم بتسجيل الدخول باستخدام حساب المستاجر الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="c21bb-211">Go to the [Scale Unit Manager portal](https://aka.ms/SCMSUM), and sign in by using your tenant account.</span></span> <span data-ttu-id="c21bb-212">في صفحه **تكوين وحدات المقياس**، يمكنك أضافه بيئة مركز إذا لم تكن مدرجه بالفعل.</span><span class="sxs-lookup"><span data-stu-id="c21bb-212">On the **Configure scale units** page, you can add a hub environment if it isn't already listed.</span></span> <span data-ttu-id="c21bb-213">يمكنك بعد ذلك تحديد المركز الذي تريد تكوينه بوحدات القياس وأحمال العمل.</span><span class="sxs-lookup"><span data-stu-id="c21bb-213">You can then select the hub that you want to configure with scale units and workloads.</span></span>

:::image type="content" source="media/cloud_edge-Manage.png" alt-text="تجربة وحده القياس وأداره أحمال العمل":::

<span data-ttu-id="c21bb-215">لأضافه وحده قياس واحده أو أكثر متاحه في الطبولوجيا، حدد **أضافه وحدات قياس**.</span><span class="sxs-lookup"><span data-stu-id="c21bb-215">To add one or more scale units that are available in your topology, select **Add scale units**.</span></span> <span data-ttu-id="c21bb-216">في المعاينة ، يجب ان تري وحده مقياس السحابة التي قمت بنشرها من أحد الرموز الترويجية التي تم تلقيها كجزء من برنامج المعاينة.</span><span class="sxs-lookup"><span data-stu-id="c21bb-216">In the preview, you should see the cloud scale unit that you deployed from one of the promo codes that you received as part of the preview program.</span></span>

<!--  [!IMPORTANT]
> In the public preview, the Scale Unit Manager portal shows the cloud scale unit that you received as part of the preview program. Any edge scale unit that you created based on an LBD configuration can't be managed in the Scale Unit Manager portal yet. For configuration details, see [Deploy custom edge scale units on custom hardware using LBD](cloud-edge-edge-scale-units-lbd.md) -->

<span data-ttu-id="c21bb-217">في علامة التبويب **أحمال العمل المعرفة**، استخدم الزر **إنشاء حمل عمل** لأضافه حمل العمل أو أداره المستودعات إلى أحدي وحدات القياس الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="c21bb-217">On the **Defined workloads** tab, use the **Create workload** button to add a warehouse management or manufacturing execution workload to one of your scale units.</span></span> <span data-ttu-id="c21bb-218">بالنسبة لكل حمل عمل ، يجب تحديد سياق العمليات التي ستكون ملكا لحمل العمل.</span><span class="sxs-lookup"><span data-stu-id="c21bb-218">For each workload, you must specify the context of the processes that will be owned by the workload.</span></span> <span data-ttu-id="c21bb-219">بالنسبة لأحمال العمليات لأداره المستودعات ، يكون السياق مستودعا معينا في موقع محدد وكيان قانوني.</span><span class="sxs-lookup"><span data-stu-id="c21bb-219">For warehouse management workloads, the context is a specific warehouse in a specific site and legal entity.</span></span> <span data-ttu-id="c21bb-220">بالنسبة لأحمال تنفيذ التصنيع ، يعد السياق موقعا محددا في أحد الكيانات القانونية.</span><span class="sxs-lookup"><span data-stu-id="c21bb-220">For manufacturing execution workloads, the context is a specific site in a legal entity.</span></span>

:::image type="content" source="media/cloud_edge-DefineWorkload.png" alt-text="إنشاء حمل العمل":::

> [!IMPORTANT]
> <span data-ttu-id="c21bb-222">لا يتيح لك مدخل أداره الوحدات في المعاينة أزاله أحمال العمل من وحدات القياس أو إلغاء تعيين وحده مقياس من المركز بعد اجراء التعيين.</span><span class="sxs-lookup"><span data-stu-id="c21bb-222">The Scale Unit Manager portal in the preview doesn't let you remove workloads from scale units or unassign a scale unit from a hub after the assignment is made.</span></span> <span data-ttu-id="c21bb-223">إذا كان من الضروري أزاله أحد التعيينات ، اتصل بالشخص المسؤول لأداره برنامج المعاينة.</span><span class="sxs-lookup"><span data-stu-id="c21bb-223">If you must remove an assignment, reach out to your contact person for preview program management.</span></span>

<!-- ### Create an edge scale unit using your custom on-premises hardware appliance

In the public preview, you can create on-premises edge scale units on your custom hardware using the LBD environments. For details, see [Deploy custom edge scale units on custom hardware using LBD](cloud-edge-edge-scale-units-lbd.md). -->


[!INCLUDE[footer-include](../../includes/footer-banner.md)]