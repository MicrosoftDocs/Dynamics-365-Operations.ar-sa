---
title: الوصول إلى بيانات تعريف التطبيق باستخدام تكوين ER
description: يصف الموضوع كيف يمكن لمستخدم Regulatory configuration service ‎‎(RCS) تصميم تعيين جديد لنموذج التقارير الإلكترونية (ER) باستخدام بيانات التعريف.
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 91c50047781fdc21c9157ceb634822c6cfb5a075
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559641"
---
# <a name="access-application-metadata-by-using-er-configuration"></a><span data-ttu-id="80111-103">الوصول إلى بيانات تعريف التطبيق باستخدام تكوين ER</span><span class="sxs-lookup"><span data-stu-id="80111-103">Access application metadata by using ER configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="80111-104">تشرح الخطوات التالية كيف يمكن لمستخدم Regulatory configuration service (RCS) يؤدي دور مسؤول النظام أو مطور التقارير الإلكترونية تصميم تعيين جديد لنموذج التقارير الإلكترونية (ER) باستخدام بيانات تعريف التطبيق.</span><span class="sxs-lookup"><span data-stu-id="80111-104">The following steps explain how a Regulatory configuration service (RCS) user in the System Administrator or Electronic Reporting Developer role can design a new Electronic reporting (ER) model mapping by using the application metadata.</span></span> <span data-ttu-id="80111-105">سيتم الوصول إلى بيانات تعريف التطبيق باستخدام تكوين بيانات تعريف ER الذي يحتوي على عينة من مجموعة بيانات التعريف للوصول إلى حركات التجارة الخارجية.</span><span class="sxs-lookup"><span data-stu-id="80111-105">Application metadata will be accessed by using an ER metadata configuration that contains a sample set of metadata to access foreign trade transactions.</span></span> <span data-ttu-id="80111-106">لإكمال هذه الخطوات، في RCS يجب أولا استكمال الخطوات في موضوع، [إنشاء موفري التكوين وتعليمهم كنشطين](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="80111-106">To complete these steps, in RCS you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> <span data-ttu-id="80111-107">بعد ذلك، أكمل الخطوات في الموضوع، [إعداد بيانات تعريف التطبيق لاستخدامها في RCS](prepare-application-metadata-rcs.md).</span><span class="sxs-lookup"><span data-stu-id="80111-107">Then complete the steps in the topic, [Prepare application metadata to be used in RCS](prepare-application-metadata-rcs.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="80111-108">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="80111-108">Prerequisites</span></span>
1. <span data-ttu-id="80111-109">انتقل إلى **كل مساحات العمل‬** > **إعداد التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="80111-109">Go to **All workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="80111-110">تأكد من وجود موفر التكوين للشركة النموذجية "Litware, Inc." ومن وضع علامة عليه كـ **نشط**.</span><span class="sxs-lookup"><span data-stu-id="80111-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="80111-111">في حالة عدم رؤية موفر التكوين هذا، أكمل الخطوات المذكورة في الإجراء [إنشاء موفرات تكوين وتحديدها بالحالة نشط‬](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="80111-111">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 

## <a name="import-metadata-configuration"></a><span data-ttu-id="80111-112">استيراد ‏‫بيانات التعريف‬</span><span class="sxs-lookup"><span data-stu-id="80111-112">Import metadata configuration</span></span> 
1. <span data-ttu-id="80111-113">انقر فوق **تكوينات بيانات التعريف**.</span><span class="sxs-lookup"><span data-stu-id="80111-113">Click **Metadata configurations**.</span></span> 
2. <span data-ttu-id="80111-114">استورد تكوين بيانات تعريف التقارير الإلكترونية التي تحتوي على بيانات التعريف التي تم تكوينها لإنشاء مستندات إلكترونية لشركة التجارة الخارجية.</span><span class="sxs-lookup"><span data-stu-id="80111-114">Import the ER metadata configuration that contains metadata that has been configured to generate electronic documents for foreign trade business.</span></span> <span data-ttu-id="80111-115">تم تصدير تكوين بيانات تعريف ER هذه كملف XML في حين تم استكمال الخطوات في [تجهيز بيانات تعريف التطبيق المراد استخدامها في RCS](prepare-application-metadata-rcs.md).</span><span class="sxs-lookup"><span data-stu-id="80111-115">This ER metadata configuration has been exported as XML file while the steps in the [Prepare application metadata to be used in RCS](prepare-application-metadata-rcs.md) procedure have been completed.</span></span> 
3. <span data-ttu-id="80111-116">انقر فوق **تبادل**.</span><span class="sxs-lookup"><span data-stu-id="80111-116">Click **Exchange**.</span></span> 
4. <span data-ttu-id="80111-117">انقر فوق **تحميل من ملف XML**.</span><span class="sxs-lookup"><span data-stu-id="80111-117">Click **Load from XML file**.</span></span> 
5. <span data-ttu-id="80111-118">انقر فوق **استعراض** وحدد ملف 'Foreign trade metadata.xml'.</span><span class="sxs-lookup"><span data-stu-id="80111-118">Click **Browse** and select the 'Foreign trade metadata.xml' file.</span></span> 
6. <span data-ttu-id="80111-119">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="80111-119">Click **OK**.</span></span> 
7. <span data-ttu-id="80111-120">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="80111-120">Close the page.</span></span> 

## <a name="create-data-model-configuration"></a><span data-ttu-id="80111-121">إنشاء تكوين نموذج البيانات</span><span class="sxs-lookup"><span data-stu-id="80111-121">Create data model configuration</span></span>
1. <span data-ttu-id="80111-122">انقر فوق **تكوينات إعداد التقارير‬**.</span><span class="sxs-lookup"><span data-stu-id="80111-122">Click **Reporting configurations**.</span></span> 
2. <span data-ttu-id="80111-123">انقر فوق **إنشاء تكوين** لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="80111-123">Click **Create configuration** to open the drop dialog.</span></span> 
3. <span data-ttu-id="80111-124">في حقل **الاسم**، اكتب 'نموذج تجارة خارجية'.</span><span class="sxs-lookup"><span data-stu-id="80111-124">In the **Name** field, type 'Foreign trade model'.</span></span> 
4. <span data-ttu-id="80111-125">وانقر فوق **إنشاء تكوين**.</span><span class="sxs-lookup"><span data-stu-id="80111-125">Click **Create configuration**.</span></span> 
5. <span data-ttu-id="80111-126">انقر فوق **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="80111-126">Click **Designer**.</span></span> 
6. <span data-ttu-id="80111-127">انقر فوق **جديد**  لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="80111-127">Click **New** to open the drop dialog.</span></span> 
7. <span data-ttu-id="80111-128">في حقل **الاسم**، اكتب "الجذر"‬.</span><span class="sxs-lookup"><span data-stu-id="80111-128">In the **Name** field, type 'Root'.</span></span> 
8. <span data-ttu-id="80111-129">انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="80111-129">Click **Add**.</span></span> 
9. <span data-ttu-id="80111-130">انقر فوق **جديد**  لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="80111-130">Click **New** to open the drop dialog.</span></span> 
10.    <span data-ttu-id="80111-131">في حقل **الاسم**، اكتب 'حركة'.</span><span class="sxs-lookup"><span data-stu-id="80111-131">In the **Name** field, type 'Transaction'.</span></span> 
11.    <span data-ttu-id="80111-132">في حقل **نوع الصنف**، حدد **قائمة سجلات**.</span><span class="sxs-lookup"><span data-stu-id="80111-132">In the **Item type** field, select **Record list**.</span></span> 
12.    <span data-ttu-id="80111-133">انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="80111-133">Click **Add**.</span></span> 
13.    <span data-ttu-id="80111-134">انقر فوق **جديد**  لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="80111-134">Click **New** to open the drop dialog.</span></span> 
14.    <span data-ttu-id="80111-135">في حقل **الاسم**، اكتب 'كود السلعة'.</span><span class="sxs-lookup"><span data-stu-id="80111-135">In the **Name** field, type 'Commodity code'.</span></span> 
15.    <span data-ttu-id="80111-136">في الحقل **نوع الصنف**، حدد **سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="80111-136">In the **Item type** field, select **String**.</span></span> 
16.    <span data-ttu-id="80111-137">انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="80111-137">Click **Add**.</span></span> 
17.    <span data-ttu-id="80111-138">انقر فوق **جديد**  لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="80111-138">Click **New** to open the drop dialog.</span></span> 
18.    <span data-ttu-id="80111-139">في حقل **الاسم**، اكتب 'المبلغ المفوتر'.</span><span class="sxs-lookup"><span data-stu-id="80111-139">In the **Name** field, type 'Invoiced amount'.</span></span> 
19.    <span data-ttu-id="80111-140">في الحقل **نوع الصنف**، حدد **حقيقي**.</span><span class="sxs-lookup"><span data-stu-id="80111-140">In the **Item type** field, select **Real**.</span></span> 
20.    <span data-ttu-id="80111-141">انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="80111-141">Click **Add**.</span></span> 
21.    <span data-ttu-id="80111-142">انقر فوق **جديد**  لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="80111-142">Click **New** to open the drop dialog.</span></span> 
22.    <span data-ttu-id="80111-143">في حقل **الاسم**، اكتب 'التاريخ'.</span><span class="sxs-lookup"><span data-stu-id="80111-143">In the **Name** field, type 'Date'.</span></span> 
23.    <span data-ttu-id="80111-144">في الحقل **نوع الصنف**، حدد **تاريخ**.</span><span class="sxs-lookup"><span data-stu-id="80111-144">In the **Item type** field, select **Date**.</span></span> 
24.    <span data-ttu-id="80111-145">انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="80111-145">Click **Add**.</span></span> 
25.    <span data-ttu-id="80111-146">انقر فوق **المرجع الجذر**.</span><span class="sxs-lookup"><span data-stu-id="80111-146">Click **Root reference**.</span></span> 
26.    <span data-ttu-id="80111-147">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="80111-147">Click **OK**.</span></span> 
27.    <span data-ttu-id="80111-148">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="80111-148">Click **Save**.</span></span> 
28.    <span data-ttu-id="80111-149">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="80111-149">Close the page.</span></span> 
29.    <span data-ttu-id="80111-150">انقر فوق **تغيير الحالة**.</span><span class="sxs-lookup"><span data-stu-id="80111-150">Click **Change status**.</span></span> 
30.    <span data-ttu-id="80111-151">انقر فوق **إكمال**.</span><span class="sxs-lookup"><span data-stu-id="80111-151">Click **Complete**.</span></span> 
31.    <span data-ttu-id="80111-152">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="80111-152">Click **OK**.</span></span> 

## <a name="create-model-mapping-configuration"></a><span data-ttu-id="80111-153">إنشاء تكوين لتعيين نموذج</span><span class="sxs-lookup"><span data-stu-id="80111-153">Create model mapping configuration</span></span> 
1. <span data-ttu-id="80111-154">انقر فوق **إنشاء تكوين** لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="80111-154">Click **Create configuration** to open the drop dialog.</span></span> 
2. <span data-ttu-id="80111-155">في الحقل **جديد**، أدخل 'تعيين نموذج استنادًا إلى نموذج بيانات التجارة الخارجية'.</span><span class="sxs-lookup"><span data-stu-id="80111-155">In the **New** field, enter 'Model Mapping based on data model Foreign trade model'.</span></span> 
3. <span data-ttu-id="80111-156">في حقل **الاسم**، اكتب 'تعيين تجارة خارجية'.</span><span class="sxs-lookup"><span data-stu-id="80111-156">In the **Name** field, type 'Foreign trade mapping'.</span></span> 
4. <span data-ttu-id="80111-157">وانقر فوق **إنشاء تكوين**.</span><span class="sxs-lookup"><span data-stu-id="80111-157">Click **Create configuration**.</span></span> 
5. <span data-ttu-id="80111-158">قم بتوسيع قسم **المتطلبات الأساسية‬**.</span><span class="sxs-lookup"><span data-stu-id="80111-158">Expand the **Prerequisites** section.</span></span> 
6. <span data-ttu-id="80111-159">انقر فوق **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="80111-159">Click **Edit**.</span></span> 
7. <span data-ttu-id="80111-160">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="80111-160">Click **New**.</span></span> 
8. <span data-ttu-id="80111-161">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="80111-161">In the list, mark the selected row.</span></span> 
9. <span data-ttu-id="80111-162">في حقل **نوع مكون المتطلبات الأساسية**، حدد **التكوين.**</span><span class="sxs-lookup"><span data-stu-id="80111-162">In the **Prerequisite component type** field, select **Configuration**.</span></span> 
10.    <span data-ttu-id="80111-163">حدد تكوين **بيانات تعريف التجارة الخارجية**.</span><span class="sxs-lookup"><span data-stu-id="80111-163">Select **Foreign trade metadata** configuration.</span></span> 
11.    <span data-ttu-id="80111-164">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="80111-164">Click **Save**.</span></span> 
12.    <span data-ttu-id="80111-165">أضفنا المرجع إلى الإصدار 1 من تكوين "بيانات تعريف التجارة الخارجية".</span><span class="sxs-lookup"><span data-stu-id="80111-165">We added the reference to the version 1 of the 'Foreign trade metadata' configuration.</span></span> <span data-ttu-id="80111-166">سيتم توفير بيانات تعريف التطبيق من هذا التكوين بينما سيتم تصميم تعيين النموذج هذا.</span><span class="sxs-lookup"><span data-stu-id="80111-166">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 
13.    <span data-ttu-id="80111-167">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="80111-167">Close the page.</span></span> 
14.    <span data-ttu-id="80111-168">انقر فوق **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="80111-168">Click **Designer**.</span></span> 
15.    <span data-ttu-id="80111-169">انقر فوق **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="80111-169">Click **Designer**.</span></span> 
16.    <span data-ttu-id="80111-170">في الشجرة، حدد **Dynamics 365 for Operations\سجلات الجداول**.</span><span class="sxs-lookup"><span data-stu-id="80111-170">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
17.    <span data-ttu-id="80111-171">انقر فوق **إضافة جذر**.</span><span class="sxs-lookup"><span data-stu-id="80111-171">Click **Add root**.</span></span> 
18.    <span data-ttu-id="80111-172">في حقل **الاسم**، اكتب '‏‫نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي'.</span><span class="sxs-lookup"><span data-stu-id="80111-172">In the **Name** field, type 'Intrastat'.</span></span> 
19.    <span data-ttu-id="80111-173">حدد سجلات جدول **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي**.</span><span class="sxs-lookup"><span data-stu-id="80111-173">Select **Intrastat** table records.</span></span> 
20.    <span data-ttu-id="80111-174">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="80111-174">Click **OK**.</span></span> 

> [!NOTE]
> <span data-ttu-id="80111-175">تم عرض الجدولين الوحيدين باعتبارها الجدولين الوحيدين الذين تمت إضافتهما إلى مجموعة بيانات التعريف المستخدمة حاليًا.</span><span class="sxs-lookup"><span data-stu-id="80111-175">The only 2 tables were offered as the only 2 tables were added into the set of metadata which is currently in use.</span></span> 

21.    <span data-ttu-id="80111-176">انقر فوق **ربط**.</span><span class="sxs-lookup"><span data-stu-id="80111-176">Click **Bind**.</span></span> 
22.    <span data-ttu-id="80111-177">في الشجرة، قم بتوسيع **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬**.</span><span class="sxs-lookup"><span data-stu-id="80111-177">In the tree, expand **Intrastat**.</span></span> 
23.    <span data-ttu-id="80111-178">في الشجرة، حدد **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي/AmountMST**.</span><span class="sxs-lookup"><span data-stu-id="80111-178">In the tree, select **Intrastat\AmountMST**.</span></span> 
24.    <span data-ttu-id="80111-179">في الشجرة، قم بتوسيع **الحركة = نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬**.</span><span class="sxs-lookup"><span data-stu-id="80111-179">In the tree, expand **Transaction = Intrastat**.</span></span> 
25.    <span data-ttu-id="80111-180">في الشجرة، حدد **الحركات = نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي/مبلغ الفاتورة**.</span><span class="sxs-lookup"><span data-stu-id="80111-180">In the tree, select **Transaction = Intrastat\Invoiced amount**.</span></span> 
26.    <span data-ttu-id="80111-181">انقر فوق **ربط**.</span><span class="sxs-lookup"><span data-stu-id="80111-181">Click **Bind**.</span></span> 
27.    <span data-ttu-id="80111-182">في الشجرة، حدد **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي/TransDate**.</span><span class="sxs-lookup"><span data-stu-id="80111-182">In the tree, select **Intrastat\TransDate**.</span></span> 
28.    <span data-ttu-id="80111-183">في الشجرة، حدد **الحركة = نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\التاريخ**.</span><span class="sxs-lookup"><span data-stu-id="80111-183">In the tree, select **Transaction = Intrastat\Date**.</span></span> 
29.    <span data-ttu-id="80111-184">انقر فوق **ربط**.</span><span class="sxs-lookup"><span data-stu-id="80111-184">Click **Bind**.</span></span> 
30.    <span data-ttu-id="80111-185">في الشجرة، قم بتوسيع **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\>العلاقات**.</span><span class="sxs-lookup"><span data-stu-id="80111-185">In the tree, expand **Intrastat\>Relations**.</span></span> 
31.    <span data-ttu-id="80111-186">في الشجرة، قم بتوسيع **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\>Relations\IntrastatCommodity**.</span><span class="sxs-lookup"><span data-stu-id="80111-186">In the tree, expand **Intrastat\>Relations\IntrastatCommodity**.</span></span> 
32.    <span data-ttu-id="80111-187">في الشجرة، حدد **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\>Relations\IntrastatCommodity\Code**.</span><span class="sxs-lookup"><span data-stu-id="80111-187">In the tree, select **Intrastat\>Relations\IntrastatCommodity\Code**.</span></span> 
33.    <span data-ttu-id="80111-188">في الشجرة، حدد **الحركات = نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي/كود السلعة**.</span><span class="sxs-lookup"><span data-stu-id="80111-188">In the tree, select **Transaction = Intrastat\Commodity code**.</span></span> 
34.    <span data-ttu-id="80111-189">انقر فوق **ربط**.</span><span class="sxs-lookup"><span data-stu-id="80111-189">Click **Bind**.</span></span> 
35.    <span data-ttu-id="80111-190">انقر فوق **التحقق من الصحة**.</span><span class="sxs-lookup"><span data-stu-id="80111-190">Click **Validate**.</span></span> 

> [!NOTE]
> <span data-ttu-id="80111-191">لقد نجحنا في ربط عناصر نموذج البيانات مع عناصر مصادر البيانات التي تم وصفها باستخدام تفاصيل بيانات تعريف التطبيق من تكوين بيانات تعريف ER المشار إليها.</span><span class="sxs-lookup"><span data-stu-id="80111-191">We have successfully bound elements of data model with items of data sources that are described by using details of application metadata from the referred ER metadata configuration.</span></span> 
36.    <span data-ttu-id="80111-192">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="80111-192">Click **Save**.</span></span> 
37.    <span data-ttu-id="80111-193">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="80111-193">Close the page.</span></span> 
38.    <span data-ttu-id="80111-194">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="80111-194">Close the page.</span></span> 
39.    <span data-ttu-id="80111-195">عند الحاجة، يمكنك توسيع مجموعة بيانات التعريف الموجودة ثم تصدير الإصدار الجديد المكتمل من تكوين بيانات تعريف التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="80111-195">When needed, you can extend the existing set of metadata and then export the new completed version of ER metadata configuration.</span></span> <span data-ttu-id="80111-196">ثم يمكنك استيرادها إلى RCS، وتحديث المتطلبات الأساسية لتكوين تعيين النموذج المكوّن الذي يشير إلى إصدار جديد من تكوين بيانات التعريف المستوردة.</span><span class="sxs-lookup"><span data-stu-id="80111-196">You can then import it to RCS, and update the prerequisites of the configured model mapping configuration referring to a new version of imported metadata configuration.</span></span> 

> [!NOTE]
> <span data-ttu-id="80111-197">تعتبر هذه الطريقة للحصول على معلومات حول بيانات تعريف التطبيق الطريقة الوحيدة المتوفرة للتطبيقات المنشورة محليًا (عند استخدام نموذج نشر بيانات العمل المحلية (LBD) أو في الموقع المحلي).</span><span class="sxs-lookup"><span data-stu-id="80111-197">This way of getting information about application metadata is the only one available for locally deployed applications (when local business data (LBD), or on-premises, deployment model is used).</span></span>
        


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]