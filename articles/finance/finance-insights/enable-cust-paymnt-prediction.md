---
title: تمكين توقعات دفع العميل (معاينة)
description: يوضح هذا الموضوع كيفية تشغيل وتكوين ميزة توقعات دفع العميل في Finance Insights.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: e10aa9342ec9f089ef8ecec5e1221a31c580fc87
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644983"
---
# <a name="enable-customer-payment-predictions-preview"></a><span data-ttu-id="48c19-103">تمكين توقعات دفع العميل (معاينة)</span><span class="sxs-lookup"><span data-stu-id="48c19-103">Enable customer payment predictions (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="48c19-104">يوضح هذا الموضوع كيفية تشغيل وتكوين ميزة توقعات دفع العميل في Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="48c19-104">This topic explains how to turn on and configure the Customer payment predictions feature in Finance insights.</span></span> <span data-ttu-id="48c19-105">يمكنك تشغيل الميزة في مساحة عمل **إدارة الميزات** وأدخل إعدادات التكوين في الصفحة **معلمات Financial insights**.</span><span class="sxs-lookup"><span data-stu-id="48c19-105">You turn on the feature in the **Feature management** workspace and enter configuration settings on the **Financial insights parameters** page.</span></span> <span data-ttu-id="48c19-106">يتضمن هذا الموضوع أيضًا معلومات يمكن أن تساعدك في استخدام الميزة بفاعلية.</span><span class="sxs-lookup"><span data-stu-id="48c19-106">This topic also includes information that can help you effectively use the feature.</span></span>

> [!NOTE]
> <span data-ttu-id="48c19-107">قبل إكمال الخطوات التالية، تأكد من إكمال الخطوات الأساسية في الموضوع [تكوين Financial insights](configure-for-fin-insites.md).</span><span class="sxs-lookup"><span data-stu-id="48c19-107">Before you complete the following steps, be sure to complete the prerequisite steps in the [Configure for Finance insights](configure-for-fin-insites.md) topic.</span></span>

1. <span data-ttu-id="48c19-108">استخدم المعلومات من صفحة البيئة في Microsoft Dynamics Lifecycle Services (LCS) للاتصال بالمثيل الأساسي لـ Azure SQL لتلك البيئة.</span><span class="sxs-lookup"><span data-stu-id="48c19-108">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="48c19-109">قم بتشغيل الأمر Transact-SQL (T-SQL) لتشغيل إصدارات التقييم لبيئة وضع الحماية.</span><span class="sxs-lookup"><span data-stu-id="48c19-109">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="48c19-110">(قد تضطر إلى تشغيل الوصول إلى عنوان IP الخاص بك في LCS قبل أن تتمكن من الاتصال بخادم كائن التطبيق عن بُعد \[AOS\].)</span><span class="sxs-lookup"><span data-stu-id="48c19-110">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED, PARTITION) VALUES ('PayPredEnableFeature', 1, 5637144576)`

    > [!NOTE]
    > <span data-ttu-id="48c19-111">إذا كان نشر Microsoft Dynamics 365 Finance عبارة عن نشر Service Fabric، فإنه يمكنك تخطي هذه الخطوة.</span><span class="sxs-lookup"><span data-stu-id="48c19-111">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="48c19-112">يجب أن يكون فريق Finance insights قد قام بالفعل بتشغيل إصدار التقييم.</span><span class="sxs-lookup"><span data-stu-id="48c19-112">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="48c19-113">إذا لم تر الميزة في مساحة عمل **إدارة الميزات**، أو إذا واجهتك مشكلات عند محاولة تشغيلها، تواصل على <fiap@microsoft.com></span><span class="sxs-lookup"><span data-stu-id="48c19-113">If you don't see the feature in the **Feature management** workspace, or if experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span>

2. <span data-ttu-id="48c19-114">تشغيل ميزة معلومات دفع العميل:</span><span class="sxs-lookup"><span data-stu-id="48c19-114">Turn on the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="48c19-115">انتقل إلى **إدارة النظام \> مساحات العمل \> إدارة الميزات**.</span><span class="sxs-lookup"><span data-stu-id="48c19-115">Go to **System administration \> Workspaces \> Feature management**.</span></span>
    2. <span data-ttu-id="48c19-116">ابحث عن الميزة التي تسمى **معلومات دفع العميل (معاينة)‬**.</span><span class="sxs-lookup"><span data-stu-id="48c19-116">Find the feature that is named **Customer payment insights (preview)**.</span></span>
    3. <span data-ttu-id="48c19-117">حدد **تمكين الآن**.</span><span class="sxs-lookup"><span data-stu-id="48c19-117">Select **Enable now**.</span></span>

    <span data-ttu-id="48c19-118">تم تشغيل ميزة معلومات دفع العميل الآن وأصبحت جاهزة ليتم تكوينها.</span><span class="sxs-lookup"><span data-stu-id="48c19-118">The Customer payment insights feature is now turned on and ready to be configured.</span></span>

3. <span data-ttu-id="48c19-119">تكوين ميزة معلومات دفع العميل:</span><span class="sxs-lookup"><span data-stu-id="48c19-119">Configure the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="48c19-120">انتقل إلى **عمليات التحصيل والائتمان \> الإعداد \> Finance insights \> معلمات Finance insights**.</span><span class="sxs-lookup"><span data-stu-id="48c19-120">Go to **Credit and collections \> Setup \> Finance insights \> Finance insights parameters**.</span></span>

        <span data-ttu-id="48c19-121">[![صفحة معلمات Financial insights قبل تكوين الميزة](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span><span class="sxs-lookup"><span data-stu-id="48c19-121">[![Financial insights parameters page before the feature is configured](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span></span>

    2. <span data-ttu-id="48c19-122">في الصفحة **معلمات Financial insights**، في علامة التبويب **معلومات دفع العميل**، حدد الارتباط **عرض حقول البيانات المستخدمة في نموذج التنبؤ** لفتح الصفحة **حقول البيانات لنموذج التنبؤ**.</span><span class="sxs-lookup"><span data-stu-id="48c19-122">On the **Financial insights parameters** page, on the **Customer payment insights** tab, select the **View the data fields used in the prediction model** link to open the **Data fields for prediction model** page.</span></span> <span data-ttu-id="48c19-123">هناك، يمكنك عرض القائمة الافتراضية للحقول المستخدمة لإنشاء نموذج التنبؤ الخاص بالذكاء الاصطناعي (AI) لتوقعات دفع العميل.</span><span class="sxs-lookup"><span data-stu-id="48c19-123">There, you can view the default list of fields that are used to create the artificial intelligence (AI) prediction model for customer payment predictions.</span></span>

        <span data-ttu-id="48c19-124">لاستخدام قائمة الحقول الافتراضية لإنشاء نموذج التنبؤ، قم بإغلاق الصفحة **حقول البيانات لصفحة نموذج التنبؤ**، ثم، في الصفحة **معلمات Financial insights**، قم بتعيين الخيار **تمكين الميزة** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="48c19-124">To use the default list of fields to create the prediction model, close the **Data fields for prediction model** page, and then, on the **Financial insights parameters** page, set the **Enable feature** option to **Yes**.</span></span>

    3. <span data-ttu-id="48c19-125">حدد فترة الحركة "متأخر جدًا" لتحديد ما إذا كان دلو التنبؤ **متأخر جدًا** تعني لشركتك أم لا.</span><span class="sxs-lookup"><span data-stu-id="48c19-125">Specify the "very late" transaction period to define what the **Very late** prediction bucket means for your business.</span></span>

        <span data-ttu-id="48c19-126">بالنسبة لكل فاتورة مفتوحة، يقوم النظام بالتوقع إلى احتمالية الدفع في ثلاثة دلو **في الوقت المحدد** و **متأخر** و **متأخر جدًا**.</span><span class="sxs-lookup"><span data-stu-id="48c19-126">For each open invoice, the system predicts the probability of payment in three buckets: **On time**, **Late**, and **Very late**.</span></span>

        - <span data-ttu-id="48c19-127">**في الوقت المحدد** يتضمن هذا الدلو المدفوعات المتوقعة التي يتم دفعها في أو قبل تاريخ استحقاق الحركة.</span><span class="sxs-lookup"><span data-stu-id="48c19-127">**On time** – This bucket includes payments that are predicted to be paid on or before the transaction due date.</span></span>
        - <span data-ttu-id="48c19-128">**متأخر** – يتضمن هذا الدلو المدفوعات المتوقعة التي يتم دفعها بعد تاريخ استحقاق الحركة ولكن قبل بدء فترة الحركة "متأخر جدًا".</span><span class="sxs-lookup"><span data-stu-id="48c19-128">**Late** – This bucket includes payments that are predicted to be paid after the transaction due date but before the start of the "very late" transaction period.</span></span>
        - <span data-ttu-id="48c19-129">**متأخر جدًا** – يتضمن هذا الدلو المدفوعات المتوقعة التي يتم دفعها بعد بدء الحركة "متأخر جدًا".</span><span class="sxs-lookup"><span data-stu-id="48c19-129">**Very late** – This bucket includes payments that are predicted to be paid after the start of the "very late" transaction period.</span></span>

        > [!NOTE]
        > <span data-ttu-id="48c19-130">إذا قمت بتغيير فترة الحركة "متأخر جدا" وحدد **تغيير الحد** بعد أن تم إنشاء نموذج التنبؤ AI الخاص بمدفوعات العميل، فإنه سيتم حذف نموذج التنبؤ الموجود وإنشاء نموذج جديد.</span><span class="sxs-lookup"><span data-stu-id="48c19-130">If you change the "very late" transaction period and select **Change late threshold** after the AI prediction model for customer payments has been created, the existing prediction model is deleted, and a new model is created.</span></span> <span data-ttu-id="48c19-131">سيقوم نموذج التنبؤ الجديد بنقل الحركات إلى فترة "متأخر جدا"، وذلك استنادًا إلى الإعدادات التي تم إدخالها لتعريفها.</span><span class="sxs-lookup"><span data-stu-id="48c19-131">The new prediction model will move transactions into the "very late" period, based on the settings that were entered to define it.</span></span>

    4. <span data-ttu-id="48c19-132">بعد الانتهاء من تحديد فترة الحركة "متأخر جدًا"، حدد **إنشاء نموذج توقع** لإنشاء نموذج التنبؤ.</span><span class="sxs-lookup"><span data-stu-id="48c19-132">After you've finished defining the "very late" transaction period, select **Create prediction model** to create the prediction model.</span></span> <span data-ttu-id="48c19-133">يعرض القسم **نموذج التنبؤ** على الصفحة **معلمات Financial insights** حالة نموذج التنبؤ.</span><span class="sxs-lookup"><span data-stu-id="48c19-133">The **Prediction model** section on the **Financial insights parameters** page shows the status of the prediction model.</span></span>

        > [!NOTE]
        > <span data-ttu-id="48c19-134">في أي وقت يتم فيه إنشاء نموذج التنبؤ، فإنه يمكن تحديد **إعادة تعيين إنشاء نموذج** لإعادة تشغيل العملية.</span><span class="sxs-lookup"><span data-stu-id="48c19-134">At any time while the prediction model is being created, you can select **Reset model creation** to restart the process.</span></span>

    <span data-ttu-id="48c19-135">لقد تم تكوين الميزة الآن وهي جاهزة للاستخدام.</span><span class="sxs-lookup"><span data-stu-id="48c19-135">The feature has now been configured and is ready to be used.</span></span>

<span data-ttu-id="48c19-136">بعد أن تم تشغيل الميزة وتكوينها، وإنشاء نموذج التنبؤ والعمل، يعرض القسم **نموذج التنبؤ** في الصفحة **معلمات Financial insights** دقة النموذج، كما هو موضح في الرسم التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="48c19-136">After the feature has been turned on and configured, and the prediction model has been created and is working, the **Prediction model** section of the **Financial insights parameters** page shows the accuracy of the model, as shown in the following illustration.</span></span>

<span data-ttu-id="48c19-137">[![دقة نموذج التنبؤ في صفحة معلمات Financial insights](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span><span class="sxs-lookup"><span data-stu-id="48c19-137">[![Accuracy of the prediction model on the Financial insights parameters page](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span></span>

## <a name="release-details"></a><span data-ttu-id="48c19-138">تفاصيل الإصدار</span><span class="sxs-lookup"><span data-stu-id="48c19-138">Release details</span></span>

<span data-ttu-id="48c19-139">تتوفر معاينة عامة لـ Finance insights لعمليات النشر التجريبية في الولايات المتحدة الأميركية وأوروبا والمملكة المتحدة.</span><span class="sxs-lookup"><span data-stu-id="48c19-139">Finance insights public preview is available for trial deployments in the United States of America, Europe, and the United Kingdom.</span></span> <span data-ttu-id="48c19-140">تُعد Microsoft دعمًا إضافيًا بشكل متزايد للعديد من المناطق.</span><span class="sxs-lookup"><span data-stu-id="48c19-140">Microsoft is incrementally adding support for more regions.</span></span>

<span data-ttu-id="48c19-141">يمكن أن يتم تشغيل ميزات المعاينة العامة ويجب تشغيلها فقط في بيئات الحماية لتحديد صلاحيات المستوى 2.</span><span class="sxs-lookup"><span data-stu-id="48c19-141">Public preview features can and should be turned on only in Tier-2 sandbox environments.</span></span> <span data-ttu-id="48c19-142">لا يمكن ترحيل نماذج الإعداد وAI التي يتم إنشاؤها في بيئة الحماية إلى بيئة التشغيل.</span><span class="sxs-lookup"><span data-stu-id="48c19-142">Setup and AI models that are created in a sandbox environment can't be migrated to a production environment.</span></span> <span data-ttu-id="48c19-143">لمزيد من المعلومات، راجع [شروط الاستخدام الإضافية لمعاينات Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).</span><span class="sxs-lookup"><span data-stu-id="48c19-143">For more information, see [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="48c19-144">إشعار الخصوصية</span><span class="sxs-lookup"><span data-stu-id="48c19-144">Privacy notice</span></span>

<span data-ttu-id="48c19-145">إن المعاينات (1) قد تستخدم تدابير أقل تتعلق بالخصوصية وإجراءات الأمان مقارنةً بخدمة Dynamics 365 Finance and Operations‏، و(2) لا يتم تضمينها في اتفاقية مستوى الخدمة (SLA) لهذه الخدمة، و(3) يجب ألا يتم استخدامها لمعالجة البيانات الشخصية أو البيانات الأخرى التي تخضع لمتطلبات التوافق القانونية أو التنظيمية، و(4) هي ذات دعم محدود.</span><span class="sxs-lookup"><span data-stu-id="48c19-145">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
