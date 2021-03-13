---
title: الوصول إلى بيانات تعريف التطبيق باستخدام التطبيقات المتصلة
description: توضح الخطوات الواردة في هذا الموضوع كيف يمكن لمستخدم Regulatory configuration service ‎‎ تصميم تعيين جديد لنموذج التقارير الإلكترونية باستخدام بيانات التعريف.
author: NickSelin
manager: AnnBe
ms.date: 06/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 457d5760fb704b7a93ce16c081b7c5e6d0ff19c1
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093320"
---
# <a name="access-application-metadata-by-using-connected-applications"></a><span data-ttu-id="24b8f-103">الوصول إلى بيانات تعريف التطبيق باستخدام التطبيقات المتصلة</span><span class="sxs-lookup"><span data-stu-id="24b8f-103">Access application metadata by using connected applications</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="24b8f-104">تشرح الخطوات التالية كيف يمكن لمستخدم Regulatory configuration service (RCS) بدور مسؤول النظام أو مطور التقارير الإلكتروني تصميم تعيين جديد لنموذج التقارير الإلكترونية (ER) باستخدام بيانات التعريف في تطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="24b8f-104">The following steps explain how a Regulatory configuration service (RCS) user in the System Administrator or Electronic Reporting Developer role can design a new Electronic reporting (ER) model mapping by using metadata in Finance and Operations.</span></span> <span data-ttu-id="24b8f-105">سيتم الوصول إلى بيانات تعريف التطبيق عبر الإنترنت باستخدام التطبيق المتصل بـ RCS.</span><span class="sxs-lookup"><span data-stu-id="24b8f-105">Application metadata will be accessed online by using the RCS connected application.</span></span> <span data-ttu-id="24b8f-106">سيتم تكوين مثال لتعيين نموذج ER للوصول إلى حركات التجارة الخارجية.</span><span class="sxs-lookup"><span data-stu-id="24b8f-106">Sample ER model mapping will be configured to access foreign trade transactions.</span></span> <span data-ttu-id="24b8f-107">لإكمال هذه الخطوات، في RCS يجب أولاً إكمال الخطوات المذكورة في الموضوع، [إنشاء موفرات تكوين وتحديدها بالحالة نشط](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="24b8f-107">To complete these steps, in RCS you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="24b8f-108">في حالة عدم إكمال الخطوات الموجودة في الموضوع، [الوصول إلى بيانات تعريف التطبيق باستخدام تكوين ER‬](access-application-metadata-er-configuration.md)[، انتقل إلى صفحة أمثلة التقارير الإلكترونية](https://go.microsoft.com/fwlink/?linkid=862266) لتنزيل تكوينات ER التالية وحفظها: Foreign trade metadata.xml؛ Foreign trade model.xml؛ Foreign trade mapping.xml؛ ثم استكمل الخطوات في الإجراء</span><span class="sxs-lookup"><span data-stu-id="24b8f-108">If you have not completed the steps in the topic, [Access application metadata by using ER configuration](access-application-metadata-er-configuration.md), go to the [Electronic reporting examples page](https://go.microsoft.com/fwlink/?linkid=862266) to download and save the following ER configurations: Foreign trade metadata.xml; Foreign trade model.xml; Foreign trade mapping.xml, and then complete the steps in the procedure.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="24b8f-109">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="24b8f-109">Prerequisites</span></span>
1. <span data-ttu-id="24b8f-110">انتقل إلى **كل مساحات العمل‬** > **إعداد التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-110">Go to **All workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="24b8f-111">تأكد من وجود موفر التكوين للشركة النموذجية "Litware, Inc." ومن وضع علامة عليه كـ **نشط**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-111">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="24b8f-112">في حالة عدم رؤية موفر التكوين هذا، أكمل الخطوات المذكورة في الإجراء [إنشاء موفرات تكوين وتحديدها بالحالة نشط‬](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="24b8f-112">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 

## <a name="get-required-er-configurations"></a><span data-ttu-id="24b8f-113">الحصول على تكوينات ER المطلوبة</span><span class="sxs-lookup"><span data-stu-id="24b8f-113">Get required ER configurations</span></span>
1. <span data-ttu-id="24b8f-114">انقر فوق **تكوينات إعداد التقارير‬**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-114">Click **Reporting configurations**.</span></span> 
2. <span data-ttu-id="24b8f-115">إذا أكملت بالفعل الخطوات الموجودة في الإجراء [‫الوصول إلى بيانات تعريف التطبيق باستخدام تكوين ER](access-application-metadata-er-configuration.md)، فلديك بالفعل تكوينات ER الضرورية (بيانات تعريف التجارة الخارجية والطراز والتعيين) في مثيل RCS الحالي.</span><span class="sxs-lookup"><span data-stu-id="24b8f-115">If you already completed the steps in the [Access application metadata by using ER configuration](access-application-metadata-er-configuration.md) procedure, you already have all necessary ER configurations (foreign trade metadata, model and mapping configurations) in the current RCS instance.</span></span> <span data-ttu-id="24b8f-116">يمكنك تخطي جميع الخطوات المتبقية في هذه المهمة الفرعية.</span><span class="sxs-lookup"><span data-stu-id="24b8f-116">You can skip all the remaining steps of this sub-task.</span></span> 
3. <span data-ttu-id="24b8f-117">انقر فوق **تبادل**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-117">Click **Exchange**.</span></span> 
4. <span data-ttu-id="24b8f-118">انقر فوق **تحميل من ملف XML**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-118">Click **Load from XML file**.</span></span> 
5. <span data-ttu-id="24b8f-119">انقر فوق **استعراض** وحدد ملف **Foreign trade metadata.xml**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-119">Click **Browse** and select the **Foreign trade metadata.xml** file.</span></span> 
6. <span data-ttu-id="24b8f-120">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-120">Click **OK**.</span></span> 
7. <span data-ttu-id="24b8f-121">انقر فوق **تبادل**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-121">Click **Exchange**.</span></span> 
8. <span data-ttu-id="24b8f-122">انقر فوق **تحميل من ملف XML**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-122">Click **Load from XML file**.</span></span> 
9. <span data-ttu-id="24b8f-123">انقر فوق **استعراض** وحدد ملف **Foreign trade model.xml**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-123">Click **Browse** and select the **Foreign trade model.xml** file.</span></span> 
10. <span data-ttu-id="24b8f-124">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-124">Click **OK**.</span></span> 
11. <span data-ttu-id="24b8f-125">انقر فوق **تبادل**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-125">Click **Exchange**.</span></span> 
12. <span data-ttu-id="24b8f-126">انقر فوق **تحميل من ملف XML**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-126">Click **Load from XML file**.</span></span> 
13. <span data-ttu-id="24b8f-127">انقر فوق **استعراض** وحدد ملف **Foreign trade mapping.xml**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-127">Click **Browse** and select the **Foreign trade mapping.xml** file.</span></span> 
14. <span data-ttu-id="24b8f-128">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-128">Click **OK**.</span></span> 

## <a name="register-a-connected-application"></a><span data-ttu-id="24b8f-129">تسجيل تطبيق متصل</span><span class="sxs-lookup"><span data-stu-id="24b8f-129">Register a connected application</span></span>
1. <span data-ttu-id="24b8f-130">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="24b8f-130">Close the page.</span></span> 
2. <span data-ttu-id="24b8f-131">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="24b8f-131">Close the page.</span></span> 
3. <span data-ttu-id="24b8f-132">انتقل إلى **كل مساحات العمل‬** > **إعداد التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-132">Go to **All workspaces** > **Electronic reporting**.</span></span> 
4. <span data-ttu-id="24b8f-133">انقر فوق **التطبيقات المتصلة**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-133">Click **Connected applications**.</span></span> 
5. <span data-ttu-id="24b8f-134">تأكد من أن التطبيق الذي تم تكوينه يعتمد على Azure ويمكن لمستخدم RCS الحالي الوصول إليه.</span><span class="sxs-lookup"><span data-stu-id="24b8f-134">Make sure that the configured application is Azure based and accessible for the current RCS user.</span></span> <span data-ttu-id="24b8f-135">ومن المطلوب أيضًا أن يكون لدى مستخدم RCS الحالي إمكانية الوصول إلى التطبيق المحدد وتسجيله كمستخدم لهذا التطبيق بحيث يشغل دورًا يعطيه امتيازات للوصول إلى بيانات تعريف التطبيق.</span><span class="sxs-lookup"><span data-stu-id="24b8f-135">It is also required that the current RCS user has access to the selected application and has been registered as a user of this application playing a role giving them privileges to access application's metadata.</span></span> 
6. <span data-ttu-id="24b8f-136">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-136">Click **New**.</span></span> 
7. <span data-ttu-id="24b8f-137">في حقل **الاسم**، اكتب 'MyConnectedApp'.</span><span class="sxs-lookup"><span data-stu-id="24b8f-137">In the **Name** field, type 'MyConnectedApp'.</span></span> 
8. <span data-ttu-id="24b8f-138">في حقل **التطبيق**، اكتب 'https:// mycompany.operations.dynamics.com '.</span><span class="sxs-lookup"><span data-stu-id="24b8f-138">In the **Application** field, type 'https:// mycompany.operations.dynamics.com'.</span></span> 
9. <span data-ttu-id="24b8f-139">في حقل **المستأجر**، اكتب 'mycompany.onmicrosoft.com'.</span><span class="sxs-lookup"><span data-stu-id="24b8f-139">In the **Tenant** field, type 'mycompany.onmicrosoft.com'.</span></span> 
10. <span data-ttu-id="24b8f-140">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-140">Click **Save**.</span></span> 
11. <span data-ttu-id="24b8f-141">عند التحقق من الاتصال بالتطبيق الذي تم تكوينه، في صفحة **الاتصال بالتطبيق البعيد** انقر فوق **انقر هنا للاتصال بارتباط التطبيق البعيد المحدد**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-141">When you check connection to configured application, on the **Connect to remote application** page click **Click here to connect to selected remote application** link.</span></span> 
12. <span data-ttu-id="24b8f-142">انقر فوق **التحقق من الاتصال**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-142">Click **Check connection**.</span></span> 
13. <span data-ttu-id="24b8f-143">انقر فوق **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-143">Click **Close**.</span></span> 
14. <span data-ttu-id="24b8f-144">عند نجاح التحقق من الاتصال، سيتم تحديث تفاصيل الإصدار والمستأجر للتطبيق الذي تم تكوينه في الشبكة الحالية.</span><span class="sxs-lookup"><span data-stu-id="24b8f-144">When the connection validation succeeded, version and tenant details will be updated for the configured application in the current grid.</span></span> 

## <a name="review-existing-model-mapping-configuration"></a><span data-ttu-id="24b8f-145">مراجعة التكوين لتعيين نموذج موجود</span><span class="sxs-lookup"><span data-stu-id="24b8f-145">Review existing model mapping configuration</span></span>
1. <span data-ttu-id="24b8f-146">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="24b8f-146">Close the page.</span></span> 
2. <span data-ttu-id="24b8f-147">انقر فوق **تكوينات إعداد التقارير‬**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-147">Click **Reporting configurations**.</span></span> 
3. <span data-ttu-id="24b8f-148">في الشجرة، قم بتوسيع **نموذج التجارة الخارجية**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-148">In the tree, expand **Foreign trade model**.</span></span> 
4. <span data-ttu-id="24b8f-149">في الشجرة، حدد **نموذج التجارة الخارجية\تعيين التجارة الخارجية**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-149">In the tree, select **Foreign trade model\Foreign trade mapping**.</span></span> 
5. <span data-ttu-id="24b8f-150">قم بتوسيع قسم **المتطلبات الأساسية‬**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-150">Expand the **Prerequisites** section.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="24b8f-151">حاليًا، يشير هذا التعيين إلى تكوين بيانات التعريف.</span><span class="sxs-lookup"><span data-stu-id="24b8f-151">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="24b8f-152">سيتم توفير بيانات تعريف التطبيق من هذا التكوين بينما سيتم تصميم تعيين النموذج هذا.</span><span class="sxs-lookup"><span data-stu-id="24b8f-152">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 

6. <span data-ttu-id="24b8f-153">انقر فوق **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-153">Click **Designer**.</span></span> 
7. <span data-ttu-id="24b8f-154">انقر فوق **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-154">Click **Designer**.</span></span> 
8. <span data-ttu-id="24b8f-155">في الشجرة، حدد **Dynamics 365 for Operations\سجلات الجداول**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-155">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
9. <span data-ttu-id="24b8f-156">انقر فوق **إضافة جذر**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-156">Click **Add root**.</span></span> 
10. <span data-ttu-id="24b8f-157">في الحقل **الجدول**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="24b8f-157">In the **Table** field, enter or select a value.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="24b8f-158">حاليًا، يشير هذا التعيين إلى تكوين بيانات التعريف.</span><span class="sxs-lookup"><span data-stu-id="24b8f-158">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="24b8f-159">سيتم توفير بيانات تعريف التطبيق من هذا التكوين بينما سيتم تصميم تعيين النموذج هذا.</span><span class="sxs-lookup"><span data-stu-id="24b8f-159">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 

11. <span data-ttu-id="24b8f-160">وانقر فوق **إلغاء الأمر**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-160">Click **Cancel**.</span></span> 
12. <span data-ttu-id="24b8f-161">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="24b8f-161">Close the page.</span></span> 
13. <span data-ttu-id="24b8f-162">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="24b8f-162">Close the page.</span></span> 

## <a name="assign-connected-application-to-model-mapping"></a><span data-ttu-id="24b8f-163">تخصيص تطبيق متصل لتعيين النموذج</span><span class="sxs-lookup"><span data-stu-id="24b8f-163">Assign connected application to model mapping</span></span> 
1. <span data-ttu-id="24b8f-164">انقر فوق **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-164">Click **Edit**.</span></span> 
2. <span data-ttu-id="24b8f-165">حدد التطبيق **MyConnectedApp**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-165">Select **MyConnectedApp** application.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="24b8f-166">يشير هذا التعيين حاليًا إلى بيانات التعريف للتطبيق المتصل المحدد.</span><span class="sxs-lookup"><span data-stu-id="24b8f-166">Currently, this mapping refers to the metadata of the selected connected application.</span></span> <span data-ttu-id="24b8f-167">عندما يشير نفس التعيين إلى تكوين بيانات التعريف والتطبيق المتصل في نفس الوقت، يتم استخدام بيانات التعريف الخاصة بالتطبيق المتصل.</span><span class="sxs-lookup"><span data-stu-id="24b8f-167">When the same mapping refers to metadata configuration and connected application at the same time, metadata of the connected application will be used.</span></span> 

3. <span data-ttu-id="24b8f-168">انقر فوق **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-168">Click **Designer**.</span></span> 
4. <span data-ttu-id="24b8f-169">انقر فوق **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-169">Click **Designer**.</span></span> 
5. <span data-ttu-id="24b8f-170">في الشجرة، حدد **Dynamics 365 for Operations\سجلات الجداول**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-170">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
6. <span data-ttu-id="24b8f-171">انقر فوق **إضافة جذر**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-171">Click **Add root**.</span></span> 
7. <span data-ttu-id="24b8f-172">في الحقل **الجدول**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="24b8f-172">In the **Table** field, enter or select a value.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="24b8f-173">تم عرض أكثر من جدولين للتطبيق الآن لأن هذا التعيين يستخدم كافة بيانات التعريف للتطبيق المتصل التي تم تعيينها له.</span><span class="sxs-lookup"><span data-stu-id="24b8f-173">More than two application tables were offered now as this mapping uses all the metadata of the connected application that has been assigned for it.</span></span> 

8. <span data-ttu-id="24b8f-174">وانقر فوق **إلغاء الأمر**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-174">Click **Cancel**.</span></span> 
9. <span data-ttu-id="24b8f-175">انقر فوق **التحقق من الصحة**.</span><span class="sxs-lookup"><span data-stu-id="24b8f-175">Click **Validate**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="24b8f-176">لقد نجحنا في ربط عناصر نموذج البيانات مع عناصر مصادر البيانات التي تم وصفها باستخدام تفاصيل بيانات تعريف التطبيق المتصل التي تم تخصيصها لهذا التعيين.</span><span class="sxs-lookup"><span data-stu-id="24b8f-176">We successfully bound elements of data model with items of data sources that are described by using details of metadata of the connected application that has been assigned for this mapping.</span></span> 

10. <span data-ttu-id="24b8f-177">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="24b8f-177">Close the page.</span></span> 
11. <span data-ttu-id="24b8f-178">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="24b8f-178">Close the page.</span></span> 

<span data-ttu-id="24b8f-179">عندما تحتاج إلى تقييم تعيين هذا النموذج باستخدام بيانات التعريف الخاصة بتطبيق من إصدار مختلف، قم بتسجيل تطبيق متصل آخر، قم تخصيصه إلى تعيين النموذج هذا وتحقق منه مقابل بيانات التعريف الجديدة.</span><span class="sxs-lookup"><span data-stu-id="24b8f-179">When you need to evaluate this model mapping by using metadata of a different version application, register another connected application, assign it to this model mapping and validate it against new metadata.</span></span>
