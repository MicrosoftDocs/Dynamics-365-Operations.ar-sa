---
title: إعداد بيانات تعريف خاصة بالتطبيق لـ RCS وER
description: يشرح هذا الموضوع كيفية إعداد بيانات التعريف الخاصة بالتطبيق لـ Regulatory configuration service (RCS) والتقارير الإلكترونية (ER).
author: NickSelin
manager: AnnBe
ms.date: 04/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3a540676ba11bc3c0fb7855a2fdaff998819dfbe
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/02/2019
ms.locfileid: "1849675"
---
# <a name="prepare-application-specific-metadata-for-rcs"></a><span data-ttu-id="8bda9-103">إعداد بيانات تعريف خاصة بالتطبيق لـ RCS</span><span class="sxs-lookup"><span data-stu-id="8bda9-103">Prepare application-specific metadata for RCS</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="8bda9-104">يقدم لك هذا الموضوع أمثلة على المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="8bda9-104">This topic walks you through examples of the following tasks:</span></span>

- [<span data-ttu-id="8bda9-105">تحضير بيانات تعريف التطبيق التي يمكن استخدامها في RCS</span><span class="sxs-lookup"><span data-stu-id="8bda9-105">Prepare application metadata that can be used in RCS</span></span>](#prepare-application-metadata-that-can-be-used-in-rcs)
- [<span data-ttu-id="8bda9-106">الوصول إلى بيانات تعريف التطبيق باستخدام تكوين ER</span><span class="sxs-lookup"><span data-stu-id="8bda9-106">Access application metadata by using an ER configuration</span></span>](#access-application-metadata-by-using-an-er-configuration)
- [<span data-ttu-id="8bda9-107">الوصول إلى بيانات تعريف التطبيق باستخدام التطبيقات المتصلة</span><span class="sxs-lookup"><span data-stu-id="8bda9-107">Access application metadata by using connected applications</span></span>](#access-application-metadata-by-using-connected-applications)

## <a name="prepare-application-metadata-that-can-be-used-in-rcs"></a><span data-ttu-id="8bda9-108">تحضير بيانات تعريف التطبيق التي يمكن استخدامها في RCS</span><span class="sxs-lookup"><span data-stu-id="8bda9-108">Prepare application metadata that can be used in RCS</span></span>

<span data-ttu-id="8bda9-109">يوضح الإجراء التالي كيفية قيام مستخدم Finance and Operations الذي يتمتع بدور **مسؤول النظام** أو **مطور التقارير الإلكترونية** بإنشاء تكوين التقارير الإلكترونية (ER) الذي يحتوي على بيانات التعريف لتطبيق Microsoft Dynamics 365 for Finance and Operations، ويتم استخدامه لتصميم تكوينات تعيين نموذج ER في Regulatory configuration service (RCS).</span><span class="sxs-lookup"><span data-stu-id="8bda9-109">The following procedure shows how a user of Finance and Operations who has the **System Administrator** or **Electronic Reporting Developer** role can create an Electronic reporting (ER) configuration that contains metadata for the Microsoft Dynamics 365 for Finance and Operations application, and that is used to design ER model mapping configurations in Regulatory configuration service (RCS).</span></span> <span data-ttu-id="8bda9-110">يتم استخدام مثال تكوين تعيين لنموذج (ER) الذي تم إنشاؤه في هذا المثال للوصول إلى حركات التجارية الخارجية.</span><span class="sxs-lookup"><span data-stu-id="8bda9-110">The sample ER model mapping configuration that is created in this example will be used to access foreign trade transactions.</span></span>

<span data-ttu-id="8bda9-111">في هذا المثال، ستحتاج إلى استخدام RCS لتصميم حل ERلـ Finance and Operations والذي سيتم استخدامه لإنشاء مستندات إلكترونية تحتوي على معلومات من مجال أعمال التجارة الخارجية.</span><span class="sxs-lookup"><span data-stu-id="8bda9-111">For this example, you want to use RCS to design an ER solution for Finance and Operations that will be used to generate electronic documents that contain information from the foreign trade business domain.</span></span> <span data-ttu-id="8bda9-112">لتحديد التعيين بين نموذج بيانات ER ومصادر البيانات المطلوبة، يجب أن يكون لديك حق الوصول إلى بيانات تعريف التطبيق لـ Finance and Operations في RCS.</span><span class="sxs-lookup"><span data-stu-id="8bda9-112">To specify the mapping between the ER data model and the sources of required data, you must have access to application metadata for Finance and Operations in RCS.</span></span> <span data-ttu-id="8bda9-113">بالتالي، كجزء من عملية تصميم حل ER، يجب تكوين بيانات تعريف ER جديدة تحتوي على جميع بيانات التعريف المطلوبة حاليًا من أجل إنشاء تقارير ER لمجال الأعمال المحدد.</span><span class="sxs-lookup"><span data-stu-id="8bda9-113">Therefore, as part of the process of designing the ER solution, you must configure a new ER metadata configuration that contains all the metadata that is currently required in order to generate ER reports for the selected business domain.</span></span>

> [!NOTE]
> <span data-ttu-id="8bda9-114">في هذا المثال، ستقوم بإنشاء تكوين لشركة نموذجية، .Litware, Inc ويمكن تنفيذ هذه الخطوات في أي شركة.</span><span class="sxs-lookup"><span data-stu-id="8bda9-114">In this example, you will create a configuration for the sample company, Litware, Inc. These steps can be performed in any company.</span></span>

1. <span data-ttu-id="8bda9-115">انتقل إلى **إدارة المؤسسة \> مساحات العمل \> إعداد التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-115">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="8bda9-116">تأكد من وجود موفر التكوين للشركة النموذجية "Litware, Inc." ومن وضع علامة عليه كـ **نشط**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-116">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="8bda9-117">إذا لم تشاهد موفر التكوين هذا، فيجب أولاً إكمال الإجراء [إنشاء موفر تكوين ووضع علامة عليه على أنه نشط‬](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="8bda9-117">If you don't see this configuration provider, complete the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> 
3. <span data-ttu-id="8bda9-118">حدد **تكوينات بيانات التعريف**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-118">Select **Metadata configurations**.</span></span>
4. <span data-ttu-id="8bda9-119">حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-119">Select **Create configuration**.</span></span>
5. <span data-ttu-id="8bda9-120">في مربع الحوار المنسدل، في الحقل **الاسم**، ادخل اسمًا.</span><span class="sxs-lookup"><span data-stu-id="8bda9-120">In the drop-down dialog box, in the **Name** field, enter a name.</span></span> <span data-ttu-id="8bda9-121">بالنسبة لهذا المثال، أدخل **بيانات تعريف التجارة الخارجية**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-121">For this example, enter **Foreign trade metadata**.</span></span>
6. <span data-ttu-id="8bda9-122">حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-122">Select **Create configuration**.</span></span>
7. <span data-ttu-id="8bda9-123">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-123">Select **Designer**.</span></span>
8. <span data-ttu-id="8bda9-124">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-124">Select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8bda9-125">يمكنك تحديد كافة بيانات التعريف إما للتطبيق بالكامل أو للنماذج أو الوحدات النمطية المحددة.</span><span class="sxs-lookup"><span data-stu-id="8bda9-125">You can select all metadata either for the whole application, or for selected models or modules.</span></span> <span data-ttu-id="8bda9-126">وفي كلتا الحالتين، يجب مراعاة أنه ستتم إضافة بيانات التعريف التالية تلقائيا: جداول السجلات والتعدادات وأنواع البيانات الملحقة (EDT).</span><span class="sxs-lookup"><span data-stu-id="8bda9-126">In both cases, be aware that the following metadata will be automatically added: tables of records, enumerations, and extended data types (EDTs).</span></span> <span data-ttu-id="8bda9-127">عندما تكون هناك أنواع إضافية من بيانات التعريف مطلوبة، فيجب إضافتها يدويًا.</span><span class="sxs-lookup"><span data-stu-id="8bda9-127">When additional types of metadata are required, they must be manually added.</span></span>

<span data-ttu-id="8bda9-128">يجب إضافة بعض بيانات التعريف المرتبطة بحركات التجارية الخارجية وتحديد عناصر بيانات التعريف يدويًا.</span><span class="sxs-lookup"><span data-stu-id="8bda9-128">You must add some metadata that is related to foreign trade transactions and manually select metadata items.</span></span>

9. <span data-ttu-id="8bda9-129">حدد **إضافة مصدر بيانات \>** سجلات جدول.</span><span class="sxs-lookup"><span data-stu-id="8bda9-129">Select **Add data source \> Table records**.</span></span>
10. <span data-ttu-id="8bda9-130">قم بالتصفية حسب قيمة **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي** في حقل **الاسم**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-130">Filter on a value of **Intrastat** in the **Name** field.</span></span>
11. <span data-ttu-id="8bda9-131">حدد سجل جدول **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-131">Select the **Intrastat** table record.</span></span>
12. <span data-ttu-id="8bda9-132">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-132">Select **OK**.</span></span>

<span data-ttu-id="8bda9-133">يجب إضافة معلومات بيانات التعريف الخاصة بجدول سجلات نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="8bda9-133">You must add metadata information about the Intrastat table of records.</span></span>

13. <span data-ttu-id="8bda9-134">في الشجرة، حدد **سجلات جدول نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\> \>العلاقات\> IntrastatCommodity (سجلات جدول EcoResCategory)**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-134">In the tree, select **Table records Intrastat \> \>Relations \> IntrastatCommodity (Table records EcoResCategory)**.</span></span>
14. <span data-ttu-id="8bda9-135">حدد **إضافة بيانات التعريف**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-135">Select **Add metadata**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8bda9-136">يجب إضافة بيانات التعريف حول العلاقات المطلوبة لجدول السجلات المحدد يدويا.</span><span class="sxs-lookup"><span data-stu-id="8bda9-136">Metadata about required relations for the selected table of records must be added manually.</span></span>

15. <span data-ttu-id="8bda9-137">حدد **إضافة مصدر البيانات**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-137">Select **Add data source**.</span></span>
16. <span data-ttu-id="8bda9-138">حدد **التعداد**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-138">Select **Enumeration**.</span></span>
17. <span data-ttu-id="8bda9-139">قم بالتصفية حسب القيمة **IntrastatDirection** في حقل **الاسم**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-139">Filter on a value of **IntrastatDirection** in the **Name** field.</span></span>
18. <span data-ttu-id="8bda9-140">حدد سجل تعداد **IntrastatDirection**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-140">Select the **IntrastatDirection** enumeration record.</span></span>
19. <span data-ttu-id="8bda9-141">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-141">Select **OK**.</span></span>
20. <span data-ttu-id="8bda9-142">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-142">Select **Save**.</span></span>
21. <span data-ttu-id="8bda9-143">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8bda9-143">Close the page.</span></span>
22. <span data-ttu-id="8bda9-144">أكمل الإصدار التمهيدي من تكوين بيانات التعريف:</span><span class="sxs-lookup"><span data-stu-id="8bda9-144">Complete the draft version of the metadata configuration:</span></span>

    1. <span data-ttu-id="8bda9-145">حدد **حالة التغيير \> مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-145">Select **Change status \> Complete**.</span></span>
    2. <span data-ttu-id="8bda9-146">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-146">Select **OK**.</span></span>
    3. <span data-ttu-id="8bda9-147">حدد الإصدار المكتمل 1.</span><span class="sxs-lookup"><span data-stu-id="8bda9-147">Select the completed version 1.</span></span>

23. <span data-ttu-id="8bda9-148">صدّر النسخة المكتملة من تكوين بيانات التعريف من التطبيق كملف XML:</span><span class="sxs-lookup"><span data-stu-id="8bda9-148">Export the completed version of the metadata configuration from the application as an XML file:</span></span>

    1. <span data-ttu-id="8bda9-149">حدد **تبادل \> تصدير كملف XML**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-149">Select **Exchange \> Export as XML file**.</span></span>
    2. <span data-ttu-id="8bda9-150">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-150">Select **OK**.</span></span>

<span data-ttu-id="8bda9-151">يتم حفظ تكوين بيانات تعريف ER الذي قمت بإنشائه كملف **Foreign trade metadata.xml**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-151">The ER metadata configuration that you created is saved as the **Foreign trade metadata.xml** file.</span></span> <span data-ttu-id="8bda9-152">يمكنك الآن استيراده إلى RCS، بحيث يمكن استخدامه كمصدر لبيانات التعريف الخاصة بمجال أعمال التجارية الخارجية في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8bda9-152">You can now import it into RCS, so that it can be used as the source of metadata for the foreign trade business domain in Finance and Operations.</span></span> <span data-ttu-id="8bda9-153">استنادا إلى هذه المعلومات، يمكنك تحديد التعيين بين بيانات تعريف التطبيق ونموذج بيانات ER.</span><span class="sxs-lookup"><span data-stu-id="8bda9-153">Based on this information, you can specify the mapping between application metadata and the ER data model.</span></span>

## <a name="access-application-metadata-by-using-an-er-configuration"></a><span data-ttu-id="8bda9-154">الوصول إلى بيانات تعريف التطبيق باستخدام تكوين ER</span><span class="sxs-lookup"><span data-stu-id="8bda9-154">Access application metadata by using an ER configuration</span></span>

<span data-ttu-id="8bda9-155">يوضح الإجراء التالي كيف يمكن لمستخدم RCS الذي يتمتع بدور **مسؤول النظام** أو **مطور التقارير الإلكترونية** تصميم تعيين نموذج ER جديد باستخدام بيانات التعريف من تطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8bda9-155">The following procedure shows how an RCS user who has the **System Administrator** or **Electronic Reporting Developer** role can design a new ER model mapping by using metadata from the Finance and Operations application.</span></span> <span data-ttu-id="8bda9-156">سيتم الوصول إلى بيانات تعريف التطبيق باستخدام تكوين بيانات تعريف ER الذي يحتوي على عينة من مجموعة بيانات التعريف للوصول إلى حركات التجارة الخارجية.</span><span class="sxs-lookup"><span data-stu-id="8bda9-156">Application metadata will be accessed by using an ER metadata configuration that contains a sample set of metadata to access foreign trade transactions.</span></span>

<span data-ttu-id="8bda9-157">قبل إكمال هذا الإجراء، يجب أن تستكمل أولا الإجراءات التالية:</span><span class="sxs-lookup"><span data-stu-id="8bda9-157">Before you can complete this procedure, you must first complete the following procedures:</span></span>

- [<span data-ttu-id="8bda9-158">إنشاء موفر تكوين ووضع علامة عليه على أنه نشط</span><span class="sxs-lookup"><span data-stu-id="8bda9-158">Create a configuration provider and mark it as active</span></span>](tasks/er-configuration-provider-mark-it-active-2016-11.md)
- [<span data-ttu-id="8bda9-159">تحضير بيانات تعريف التطبيق التي يمكن استخدامها في RCS</span><span class="sxs-lookup"><span data-stu-id="8bda9-159">Prepare application metadata that can be used in RCS</span></span>](#prepare-application-metadata-that-can-be-used-in-rcs)

1. <span data-ttu-id="8bda9-160">انتقل إلى **كافة مساحات العمل \> التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-160">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="8bda9-161">تأكد من وجود موفر التكوين للشركة النموذجية "Litware, Inc." ومن وضع علامة عليه كـ **نشط**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-161">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="8bda9-162">إذا لم تشاهد موفر التكوين هذا، فيجب أولاً إكمال الإجراء [إنشاء موفر تكوين ووضع علامة عليه على أنه نشط‬](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="8bda9-162">If you don't see this configuration provider, complete the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> 
3. <span data-ttu-id="8bda9-163">استورد تكوين بيانات تعريف ER الذي يحتوي على بيانات التعريف لتطبيق Finance and Operations والذي تم تكوينه لإنشاء مستندات إلكترونية لمجال أعمال التجارة الخارجية.</span><span class="sxs-lookup"><span data-stu-id="8bda9-163">Import the ER metadata configuration that contains metadata for the Finance and Operations application, and that is configured to generate electronic documents for the foreign trade business domain.</span></span> <span data-ttu-id="8bda9-164">لقد قمت بإنشاء تكوين بيانات تعريف ER هذا وتصديره كملف XML في إجراء [تحضير بيانات تعريف التطبيق التي يمكن استخدامها في RCS](#prepare-application-metadata-that-can-be-used-in-rcs) سابقًا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="8bda9-164">You created this ER metadata configuration and exported it as an XML file in the [Prepare application metadata that can be used in RCS](#prepare-application-metadata-that-can-be-used-in-rcs) procedure earlier in this topic.</span></span>

    1. <span data-ttu-id="8bda9-165">حدد **تكوينات بيانات التعريف**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-165">Select **Metadata configurations**.</span></span>
    2. <span data-ttu-id="8bda9-166">حدد **تبادل**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-166">Select **Exchange**.</span></span>
    3. <span data-ttu-id="8bda9-167">حدد **تحميل من ملف XML**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-167">Select **Load from XML file**.</span></span>
    4. <span data-ttu-id="8bda9-168">استعرض لتحديد ملف **Foreign trade metadata.xml**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-168">Browse to select the **Foreign trade metadata.xml** file.</span></span>
    5. <span data-ttu-id="8bda9-169">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-169">Select **OK**.</span></span>
    6. <span data-ttu-id="8bda9-170">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8bda9-170">Close the page.</span></span>

4. <span data-ttu-id="8bda9-171">إنشاء تكوين نموذج البيانات:</span><span class="sxs-lookup"><span data-stu-id="8bda9-171">Create a data model configuration:</span></span>

    1. <span data-ttu-id="8bda9-172">حدد **تكوينات إعداد التقارير‬**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-172">Select **Reporting configurations**.</span></span>
    2. <span data-ttu-id="8bda9-173">حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-173">Select **Create configuration**.</span></span>
    3. <span data-ttu-id="8bda9-174">في مربع الحوار المنسدل، في الحقل **الاسم**، أدخل **نموذج التجارة الخارجية**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-174">In the drop-down dialog box, in the **Name** field, enter **Foreign trade model**.</span></span>
    4. <span data-ttu-id="8bda9-175">حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-175">Select **Create configuration**.</span></span>
    5. <span data-ttu-id="8bda9-176">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-176">Select **Designer**.</span></span>
    6. <span data-ttu-id="8bda9-177">حدد **جديد** لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="8bda9-177">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="8bda9-178">في حقل **الاسم**، اكتب **الجذر‬**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-178">In the **Name** field, type **Root**.</span></span>
        2. <span data-ttu-id="8bda9-179">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-179">Select **Add**.</span></span>
    
    7. <span data-ttu-id="8bda9-180">حدد **جديد** لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="8bda9-180">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="8bda9-181">في حقل **الاسم**، اكتب **الحركة**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-181">In the **Name** field, type **Transaction**.</span></span>
        2. <span data-ttu-id="8bda9-182">في حقل **نوع الصنف**، حدد **قائمة سجلات**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-182">In the **Item type** field, select **Record list**.</span></span>
        3. <span data-ttu-id="8bda9-183">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-183">Select **Add**.</span></span>
 
    8. <span data-ttu-id="8bda9-184">حدد **جديد** لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="8bda9-184">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="8bda9-185">في حقل **الاسم**، اكتب **كود السلعة**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-185">In the **Name** field, type **Commodity code**.</span></span>
        2. <span data-ttu-id="8bda9-186">في الحقل **نوع الصنف**، حدد **سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-186">In the **Item type** field, select **String**.</span></span>
        3. <span data-ttu-id="8bda9-187">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-187">Select **Add**.</span></span>

    9. <span data-ttu-id="8bda9-188">حدد **جديد** لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="8bda9-188">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="8bda9-189">في حقل الاسم، اكتب **المبلغ المفوتر**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-189">In the Name field, type **Invoiced amount**.</span></span>
        2. <span data-ttu-id="8bda9-190">في الحقل **نوع الصنف**، حدد **حقيقي**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-190">In the **Item type** field, select **Real**.</span></span>
        3. <span data-ttu-id="8bda9-191">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-191">Select **Add**.</span></span>

    10. <span data-ttu-id="8bda9-192">حدد **جديد** لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="8bda9-192">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="8bda9-193">في حقل **الاسم**، اكتب **التاريخ**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-193">In the **Name** field, type **Date**.</span></span>
        2. <span data-ttu-id="8bda9-194">في الحقل **نوع الصنف**، حدد **تاريخ**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-194">In the **Item type** field, select **Date**.</span></span>
        3. <span data-ttu-id="8bda9-195">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-195">Select **Add**.</span></span>
 
    11. <span data-ttu-id="8bda9-196">حدد **إضافة \> مرجع الجذر**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-196">Select **Add \> Root reference**.</span></span>
    12. <span data-ttu-id="8bda9-197">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-197">Select **OK**.</span></span>
    13. <span data-ttu-id="8bda9-198">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-198">Select **Save**.</span></span>
    14. <span data-ttu-id="8bda9-199">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8bda9-199">Close the page.</span></span>
    15. <span data-ttu-id="8bda9-200">حدد **حالة التغيير \> مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-200">Select **Change status \> Complete**.</span></span>
    16. <span data-ttu-id="8bda9-201">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-201">Select **OK**.</span></span>

5. <span data-ttu-id="8bda9-202">إنشاء تكوين لتعيين نموذج:</span><span class="sxs-lookup"><span data-stu-id="8bda9-202">Create a model mapping configuration:</span></span>

    1. <span data-ttu-id="8bda9-203">حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-203">Select **Create configuration**.</span></span>
    2. <span data-ttu-id="8bda9-204">في مربع الحوار المنسدل، في لحقل **جديد**، أدخل **تعيين نموذج استنادًا إلى نموذج بيانات التجارة الخارجية**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-204">In the drop-down dialog box, in the **New** field, enter **Model Mapping based on data model Foreign trade model**.</span></span>
    3. <span data-ttu-id="8bda9-205">في حقل **الاسم**، اكتب **تعيين تجارة خارجية**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-205">In the **Name** field, enter **Foreign trade mapping**.</span></span>
    4. <span data-ttu-id="8bda9-206">حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-206">Select **Create configuration**.</span></span>
    5. <span data-ttu-id="8bda9-207">في علامة التبويب السريعة **المتطلبات الأساسية**، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-207">On the **Prerequisites** FastTab, select **Edit**.</span></span>
    6. <span data-ttu-id="8bda9-208">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-208">Select **New**.</span></span>
    7. <span data-ttu-id="8bda9-209">في حقل **نوع مكون المتطلبات الأساسية**، حدد **التكوين.**</span><span class="sxs-lookup"><span data-stu-id="8bda9-209">In the **Prerequisite component type** field, select **Configuration**.</span></span>
    8. <span data-ttu-id="8bda9-210">حدد تكوين **بيانات تعريف التجارة الخارجية**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-210">Select the **Foreign trade metadata** configuration.</span></span>
    9. <span data-ttu-id="8bda9-211">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-211">Select **Save**.</span></span> <span data-ttu-id="8bda9-212">لاحظ أنه تتم إضافة المرجع إلى الإصدار 1 من تكوين **بيانات تعريف التجارة الخارجية**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-212">Notice that the reference is added to version 1 of the **Foreign trade metadata** configuration.</span></span> <span data-ttu-id="8bda9-213">سيتم توفير بيانات تعريف التطبيق من هذا التكوين بينما سيتم تصميم تعيين النموذج.</span><span class="sxs-lookup"><span data-stu-id="8bda9-213">Application metadata from this configuration will be offered while the model mapping is designed.</span></span>
    10. <span data-ttu-id="8bda9-214">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8bda9-214">Close the page.</span></span>
    11. <span data-ttu-id="8bda9-215">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-215">Select **Designer**.</span></span>
    12. <span data-ttu-id="8bda9-216">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-216">Select **Designer**.</span></span>
    13. <span data-ttu-id="8bda9-217">في الشجرة، حدد **Dynamics 365 for Operations \> سجلات الجدول**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-217">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
    14. <span data-ttu-id="8bda9-218">حدد **إضافة جذر**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-218">Select **Add root**.</span></span>
    15. <span data-ttu-id="8bda9-219">في الحقل **الاسم**، أدخل **‏‫نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-219">In the **Name** field, enter **Intrastat**.</span></span>
    16. <span data-ttu-id="8bda9-220">حدد سجلات جدول **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-220">Select **Intrastat** table records.</span></span>
    17. <span data-ttu-id="8bda9-221">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-221">Select **OK**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="8bda9-222">تم عرض الجدولين فقط نظرًا لأنه تمت إضافة جدولين فقط إلى مجموعة بيانات التعريف المستخدمة حاليًا.</span><span class="sxs-lookup"><span data-stu-id="8bda9-222">Only two tables are offered, because only two tables were added to the set of metadata that is currently used.</span></span>

    18. <span data-ttu-id="8bda9-223">حدد **ربط**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-223">Select **Bind**.</span></span>
    19. <span data-ttu-id="8bda9-224">في الشجرة، حدد **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي \> AmountMST**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-224">In the tree, select **Intrastat \> AmountMST**.</span></span>
    20. <span data-ttu-id="8bda9-225">في الشجرة، حدد **الحركة = نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي \> المبلغ المفوتر**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-225">In the tree, select **Transaction = Intrastat \> Invoiced amount**.</span></span>
    21. <span data-ttu-id="8bda9-226">حدد **ربط**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-226">Select **Bind**.</span></span>
    22. <span data-ttu-id="8bda9-227">في الشجرة، حدد **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\>تاريخ الحركة**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-227">In the tree, select **Intrastat \> TransDate**.</span></span>
    23. <span data-ttu-id="8bda9-228">في الشجرة، حدد **الحركة = نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\>التاريخ**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-228">In the tree, select **Transaction = Intrastat \> Date**.</span></span>
    24. <span data-ttu-id="8bda9-229">حدد **ربط**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-229">Select **Bind**.</span></span>
    25. <span data-ttu-id="8bda9-230">في الشجرة، حدد **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\> \>العلاقات \> IntrastatCommodity\> الكود**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-230">In the tree, select **Intrastat \> \>Relations \> IntrastatCommodity \> Code**.</span></span>
    26. <span data-ttu-id="8bda9-231">في الشجرة، حدد **الحركة = نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي \> كود السلعة**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-231">In the tree, select **Transaction = Intrastat \> Commodity code**.</span></span>
    27. <span data-ttu-id="8bda9-232">حدد **ربط**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-232">Select **Bind**.</span></span>
    28. <span data-ttu-id="8bda9-233">حدد **التحقق من الصحة**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-233">Select **Validate**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="8bda9-234">بعد اكتمال التحقق من الصحة، تكون نجحت في ربط عناصر نموذج البيانات بعناصر مصادر البيانات التي تم وصفها باستخدام تفاصيل بيانات تعريف التطبيق من تكوين بيانات تعريف ER المشار إليها.</span><span class="sxs-lookup"><span data-stu-id="8bda9-234">After validation is completed, you've successfully bound elements of the data model to items of the data sources that are described by using details of the application metadata from the referenced ER metadata configuration.</span></span>

    29. <span data-ttu-id="8bda9-235">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-235">Select **Save**.</span></span>

<span data-ttu-id="8bda9-236">وحسب الحاجة، يمكنك توسيع مجموعة بيانات التعريف الموجودة في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8bda9-236">As you require, you can extend the existing set of metadata in Finance and Operations.</span></span> <span data-ttu-id="8bda9-237">ويمكنك بعد ذلك تصدير الإصدار الجديد المكتمل من تكوين بيانات تعريف ER من Finance and Operations، واستيراده إلى RCS وتحديث المتطلبات الأساسية لتكوين تعيين النموذج المكون للإشارة إصدار جديد من تكوين بيانات التعريف المستوردة.</span><span class="sxs-lookup"><span data-stu-id="8bda9-237">You can then export the new completed version of the ER metadata configuration from Finance and Operations, import it into RCS, and update the prerequisites of the configured model mapping configuration to refer to a new version of the imported metadata configuration.</span></span>

> [!NOTE]
> <span data-ttu-id="8bda9-238">وهذه الطريقة للحصول على معلومات حول بيانات تعريف التطبيق هي الوحيدة المتوفرة للتطبيقات المنشورة محليا (أي، عند استخدام بيانات العمل المحلية \[LBD\] أو في المقر نموذج النشر المستخدم لـ Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="8bda9-238">This method for getting information about application metadata is the only available method for applications that are locally deployed (that is, when a local business data \[LBD\], or on-premises, deployment model is used for Finance and Operations).</span></span>

## <a name="access-application-metadata-by-using-connected-applications"></a><span data-ttu-id="8bda9-239">الوصول إلى بيانات تعريف التطبيق باستخدام التطبيقات المتصلة</span><span class="sxs-lookup"><span data-stu-id="8bda9-239">Access application metadata by using connected applications</span></span>

<span data-ttu-id="8bda9-240">يوضح الإجراء التالي كيف يمكن لمستخدم RCS الذي يتمتع بدور **مسؤول النظام** أو **مطور التقارير الإلكترونية** تصميم تعيين نموذج ER جديد باستخدام بيانات التعريف لتطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8bda9-240">The following procedure shows how an RCS user who has the **System Administrator** or **Electronic Reporting Developer** role can design a new ER model mapping by using metadata of the Finance and Operations application.</span></span> <span data-ttu-id="8bda9-241">سيتم الوصول إلى بيانات تعريف التطبيق عبر الإنترنت باستخدام التطبيق المتصل بـ RCS.</span><span class="sxs-lookup"><span data-stu-id="8bda9-241">Application metadata will be accessed online by using RCS connected application.</span></span> <span data-ttu-id="8bda9-242">سيتم تكوين مثال لتعيين نموذج ER للوصول إلى حركات التجارة الخارجية.</span><span class="sxs-lookup"><span data-stu-id="8bda9-242">A sample ER model mapping will be configured to access foreign trade transactions.</span></span>

<span data-ttu-id="8bda9-243">لإكمال هذا الإجراء، يجب أولاً إكمال الإجراء [‏‫إنشاء موفر تكوين ووضع علامة عليه على أنه نشط](tasks/er-configuration-provider-mark-it-active-2016-11.md) في RCS.</span><span class="sxs-lookup"><span data-stu-id="8bda9-243">To complete this procedure, you must first complete the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure in RCS.</span></span> <span data-ttu-id="8bda9-244">في حالة عدم إكمال الإجراء [الوصول إلى بيانات تعريف التطبيق باستخدام تكوين ER‬](#access-application-metadata-by-using-an-er-configuration) الموضح سابقًا في هذا الموضوع، اذهب إلى  صفحة [إرشادات مهام إعداد التقارير لـ Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) لتنزيل ملفات تكوين ER التالية مقدمًا وحفظها محليًا: **Foreign trade metadata.xml** و**Foreign trade model.xml** و**Foreign trade mapping.xml**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-244">If you haven't yet completed the [Access application metadata by using an ER configuration](#access-application-metadata-by-using-an-er-configuration) procedure earlier in this topic, go to [Electronic Reporting Task Guides for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) page to download the following ER configuration files in advance and save them locally: **Foreign trade metadata.xml**, **Foreign trade model.xml**, and **Foreign trade mapping.xml**.</span></span>


### <a name="get-required-er-configurations"></a><span data-ttu-id="8bda9-245">الحصول على تكوينات ER المطلوبة</span><span class="sxs-lookup"><span data-stu-id="8bda9-245">Get required ER configurations</span></span>

<span data-ttu-id="8bda9-246">إذا أكملت بالفعل الإجراء [‏‫الوصول إلى بيانات تعريف التطبيق باستخدام تكوين ER](#access-application-metadata-by-using-an-er-configuration) الذي تم توضيحه سابقًا في هذا الموضوع، فلديك بالفعل جميع تكوينات ER المطلوبة (بيانات تعريف التجارة الخارجية والنموذج وتكوينات التعيين) في مثيل RCS الحالي.</span><span class="sxs-lookup"><span data-stu-id="8bda9-246">If you've already completed the [Access application metadata by using an ER configuration](#access-application-metadata-by-using-an-er-configuration) procedure earlier in this topic, you already have all the required ER configurations (the foreign trade metadata, model, and mapping configurations) in the current RCS instance.</span></span> <span data-ttu-id="8bda9-247">في تلك الحالة، يمكنك تخطي هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="8bda9-247">In that case, you can skip this procedure.</span></span>

1. <span data-ttu-id="8bda9-248">انتقل إلى **كافة مساحات العمل \> التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-248">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="8bda9-249">حدد **تكوينات إعداد التقارير‬**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-249">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="8bda9-250">حمّل ملفات تكوين **Foreign trade metadata.xml** و **Foreign trade model.xml** و **Foreign trade mapping.xml** مع تكرار سلسلة الخطوات التالية لكل منها:</span><span class="sxs-lookup"><span data-stu-id="8bda9-250">Load the **Foreign trade metadata.xml**, **Foreign trade model.xml**, and **Foreign trade mapping.xml** configuration files repeating the following chain of steps for each of them:</span></span>

    1. <span data-ttu-id="8bda9-251">حدد **تبادل**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-251">Select **Exchange**.</span></span>
    2. <span data-ttu-id="8bda9-252">حدد **تحميل من ملف XML**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-252">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="8bda9-253">حدد **استعراض**، وحدد ملفًا.</span><span class="sxs-lookup"><span data-stu-id="8bda9-253">Select **Browse**, and select a file.</span></span>
    4. <span data-ttu-id="8bda9-254">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-254">Select **OK**.</span></span>

### <a name="register-the-connection-with-finance-and-operations"></a><span data-ttu-id="8bda9-255">سجل الصلة مع Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8bda9-255">Register the connection with Finance and Operations</span></span>

1. <span data-ttu-id="8bda9-256">انتقل إلى **كافة مساحات العمل \> التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-256">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="8bda9-257">حدد **التطبيقات المتصلة**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-257">Select **Connected applications**.</span></span>
3. <span data-ttu-id="8bda9-258">تأكد من أن التطبيق الذي تم تكوينه يستند إلى Microsoft Azureوأنه يمكن لمستخدمي RCS الوصول إليه بشكل عام.</span><span class="sxs-lookup"><span data-stu-id="8bda9-258">Make sure that the configured application is based on Microsoft Azure, and that it is accessible in general to RCS users.</span></span> <span data-ttu-id="8bda9-259">يجب أن يكون لدى مستخدم RCS الحالي إمكانية الوصول إلى التطبيق المكون وتسجيله كمستخدم لهذا التطبيق ويشغل دورًا يعطيه امتيازات للوصول إلى بيانات تعريف التطبيق.</span><span class="sxs-lookup"><span data-stu-id="8bda9-259">The current RCS user must have access to the configured application being registered as a user of this application in a role that gives him or her privileges to access the application's metadata.</span></span>
4. <span data-ttu-id="8bda9-260">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-260">Select **New**.</span></span>
5. <span data-ttu-id="8bda9-261">في حقل **الاسم**، أدخل **MyConnectedApp** كاسم التطبيق المتصل.</span><span class="sxs-lookup"><span data-stu-id="8bda9-261">In the **Name** field, enter **MyConnectedApp** as the name of the connected application.</span></span>
6. <span data-ttu-id="8bda9-262">في حقل **التطبيق**، حدد عنوان URL للتطبيق.</span><span class="sxs-lookup"><span data-stu-id="8bda9-262">In the **Application** field, specify the URL of the application.</span></span>
7. <span data-ttu-id="8bda9-263">في حقل **المستأجر**، حدد موفر للتطبيق.</span><span class="sxs-lookup"><span data-stu-id="8bda9-263">In the **Tenant** field, specify the provider of the application.</span></span>
8. <span data-ttu-id="8bda9-264">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-264">Select **Save**.</span></span> 
9. <span data-ttu-id="8bda9-265">عند التحقق من الاتصال بالتطبيق الذي تم تكوينه، في صفحة **الاتصال بالتطبيق البعيد** حدد ارتباط **حدد هنا للاتصال بالتطبيق البعيد المحدد**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-265">When you check the connection to the configured application, on the **Connect to remote application** page, select the **Select here to connect to selected remote application** link.</span></span> 
10. <span data-ttu-id="8bda9-266">حدد **التحقق من الاتصال** للتحقق من صحة الوصول إلى التطبيق الذي تم تكوينه.</span><span class="sxs-lookup"><span data-stu-id="8bda9-266">Select **Check connection** to validate access to the configured application.</span></span>
11. <span data-ttu-id="8bda9-267">حدد **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-267">Select **Close**.</span></span>

<span data-ttu-id="8bda9-268">بعد استكمال هذا الإجراء ونجاح التحقق من صحة الاتصال، سيتم تحديث تفاصيل الإصدار والمستأجر للتطبيق الذي سيتم تكوينه في الشبكة الحالية.</span><span class="sxs-lookup"><span data-stu-id="8bda9-268">After you complete this procedure and validation of the connection succeeds, the version and tenant details for the configured application will be updated in the current grid.</span></span>

### <a name="review-the-existing-model-mapping-configuration"></a><span data-ttu-id="8bda9-269">مراجعة التكوين لتعيين نموذج موجود</span><span class="sxs-lookup"><span data-stu-id="8bda9-269">Review the existing model mapping configuration</span></span>

1. <span data-ttu-id="8bda9-270">انتقل إلى **كافة مساحات العمل \> التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-270">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="8bda9-271">حدد **تكوينات إعداد التقارير‬**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-271">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="8bda9-272">في الشجرة، حدد **نموذج التجارة الخارجية \> تعيين التجارة الخارجية**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-272">In the tree, select **Foreign trade model \> Foreign trade mapping**.</span></span>
4. <span data-ttu-id="8bda9-273">حدد علامة التبويب السريعة**المتطلبات الأساسية**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-273">Select the **Prerequisites** FasTab.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8bda9-274">حاليًا، يشير هذا التعيين إلى تكوين بيانات التعريف.</span><span class="sxs-lookup"><span data-stu-id="8bda9-274">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="8bda9-275">سيتم توفير بيانات تعريف التطبيق من هذا التكوين بينما سيتم تصميم تعيين هذا النموذج.</span><span class="sxs-lookup"><span data-stu-id="8bda9-275">Application metadata from this configuration will be offered while this model mapping is designed.</span></span>

4. <span data-ttu-id="8bda9-276">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-276">Select **Designer**.</span></span>
5. <span data-ttu-id="8bda9-277">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-277">Select **Designer**.</span></span>
6. <span data-ttu-id="8bda9-278">في الشجرة، حدد **Dynamics 365 for Operations \> سجلات الجدول**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-278">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
7. <span data-ttu-id="8bda9-279">حدد **إضافة جذر**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-279">Select **Add root**.</span></span>
8. <span data-ttu-id="8bda9-280">في الحقل **الجدول**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="8bda9-280">In the **Table** field, enter or select a value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8bda9-281">حاليًا، يشير هذا التعيين إلى تكوين بيانات التعريف.</span><span class="sxs-lookup"><span data-stu-id="8bda9-281">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="8bda9-282">سيتم توفير بيانات تعريف التطبيق من هذا التكوين بينما سيتم تصميم تعيين هذا النموذج.</span><span class="sxs-lookup"><span data-stu-id="8bda9-282">Application metadata from this configuration will be offered while this model mapping is designed.</span></span>

9. <span data-ttu-id="8bda9-283">حدد **إلغاء الأمر**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-283">Select **Cancel**.</span></span>

### <a name="assign-the-connected-application-to-a-model-mapping"></a><span data-ttu-id="8bda9-284">تخصيص تطبيق متصل لتعيين النموذج</span><span class="sxs-lookup"><span data-stu-id="8bda9-284">Assign the connected application to a model mapping</span></span>

1. <span data-ttu-id="8bda9-285">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-285">Select **Edit**.</span></span>
2. <span data-ttu-id="8bda9-286">في **حقل التطبيق المتصل**، حدد تطبيق **MyConnectedApp**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-286">In the **Connected application field**, select the **MyConnectedApp** application.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8bda9-287">يشير هذا التعيين إلى بيانات التعريف للتطبيق المتصل المحدد.</span><span class="sxs-lookup"><span data-stu-id="8bda9-287">This mapping refers to the metadata of the selected connected application.</span></span> <span data-ttu-id="8bda9-288">إذا أشار نفس التعيين إلى تكوين بيانات التعريف والتطبيق المتصل في نفس الوقت، سيتم استخدام بيانات التعريف الخاصة بالتطبيق المتصل.</span><span class="sxs-lookup"><span data-stu-id="8bda9-288">If a mapping refers to the metadata configuration and the connected application at the same time, the metadata of the connected application will be used.</span></span>

3. <span data-ttu-id="8bda9-289">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-289">Select **Designer**.</span></span>
4. <span data-ttu-id="8bda9-290">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-290">Select **Designer**.</span></span>
5. <span data-ttu-id="8bda9-291">في الشجرة، حدد **Dynamics 365 for Operations \> سجلات الجدول**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-291">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
6. <span data-ttu-id="8bda9-292">حدد **إضافة جذر**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-292">Select **Add root**.</span></span>
7. <span data-ttu-id="8bda9-293">في الحقل **الجدول**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="8bda9-293">In the **Table** field, enter or select a value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8bda9-294">في هذه النقطة، تم عرض أكثر من جدولين للتطبيق، لأن هذا التعيين يستخدم كافة بيانات التعريف للتطبيق المتصل التي تم تعيينها له.</span><span class="sxs-lookup"><span data-stu-id="8bda9-294">At this point, more than two application tables are offered, because this mapping uses all the metadata of the connected application that has been assigned to it.</span></span>

8. <span data-ttu-id="8bda9-295">حدد **إلغاء الأمر**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-295">Select **Cancel**.</span></span>
9. <span data-ttu-id="8bda9-296">حدد **التحقق من الصحة**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-296">Select **Validate**.</span></span>

<span data-ttu-id="8bda9-297">لقد قمنا الآن بربط عناصر نموذج البيانات مع عناصر مصادر البيانات التي تم وصفها باستخدام تفاصيل بيانات تعريف التطبيق المتصل التي تم تخصيصها لهذا التعيين.</span><span class="sxs-lookup"><span data-stu-id="8bda9-297">You've now bound elements of the data model to items of the data sources that are described by using details of the metadata of the connected application that has been assigned to this mapping.</span></span>

<span data-ttu-id="8bda9-298">عندما يلزم تقييم تعيين هذا النموذج باستخدام بيانات التعريف الخاصة بتطبيق من إصدار مختلف، قم بتسجيل تطبيق متصل آخر، قم تخصيصه إلى تعيين النموذج هذا، وتحقق منه مقابل بيانات التعريف الجديدة.</span><span class="sxs-lookup"><span data-stu-id="8bda9-298">When you must evaluate this model mapping by using the metadata of a different version of the application, register another connected application, assign it to this model mapping, and validate it against the new metadata.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8bda9-299">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="8bda9-299">Additional resources</span></span>

<span data-ttu-id="8bda9-300">بدلا من ذلك، يمكنك تشغيل دليل مهمة **تحضير بيانات تعريف التطبيق التي يمكن استخدامها في RCS** في Finance and Operations بالإضافة إلى دلائل مهام **الوصول إلى بيانات تعريف التطبيق باستخدام ER** و**الوصول إلى بيانات تعريف تطبيق باستخدام  التطبيقات المتصلة**.</span><span class="sxs-lookup"><span data-stu-id="8bda9-300">Alternatively, you can play the **Prepare application metadata that can be used in RCS** task guide in Finance and Operationsas as well as the **Access application metadata by using an ER configuration** and **Access application metadata by using connected applications** task guides in RCS.</span></span> <span data-ttu-id="8bda9-301">يمكن تحميل دلائل المهام هذه من صفحة [دلائل مهام التقارير الإلكترونية لـ Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739).</span><span class="sxs-lookup"><span data-stu-id="8bda9-301">These task guides can be downloaded from the [Electronic Reporting Task Guides for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) page.</span></span>
