---
title: إعداد بيانات تعريف التطبيق لاستخدامها في RCS
description: توضح الخطوات الواردة في هذا الموضوع كيف يمكن للمستخدم إنشاء تكوين التقارير الإلكترونية الجديدة (ER) التي تحتوي علي بيانات تعريف التطبيق لتصميم تكوينات تعيين نموذج ER في Regulatory configuration servic (RCS).
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3d091cd835cfcb7164f83259b69e3bc1d7c09dc4
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143144"
---
# <a name="prepare-application-metadata-to-be-used-in-rcs"></a><span data-ttu-id="ba185-103">إعداد بيانات تعريف التطبيق لاستخدامها في RCS</span><span class="sxs-lookup"><span data-stu-id="ba185-103">Prepare application metadata to be used in RCS</span></span>
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ba185-104">توضح الخطوات التالية كيف يمكن لمستخدم يشغل دور المسؤول نظام أو مطور التقارير الإلكترونية إنشاء تكوين التقارير الإلكترونية الجديدة (ER) التي تحتوي علي بيانات تعريف التطبيق لتصميم تكوينات تعيين نموذج ER في Regulatory configuration servic (RCS).</span><span class="sxs-lookup"><span data-stu-id="ba185-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains application metadata for designing ER model mapping configurations in Regulatory configuration service (RCS).</span></span> <span data-ttu-id="ba185-105">يتم استخدام هذا التكوين لتصميم نموذج تكوين تعيين لنموذج ER للوصول إلى حركات التجارية الخارجية.</span><span class="sxs-lookup"><span data-stu-id="ba185-105">This configuration will be used for designing a sample ER model mapping configuration to access foreign trade transactions.</span></span> <span data-ttu-id="ba185-106">في هذا المثال، ستقوم بإنشاء تكوين لشركة نموذج، .Litware, Inc ويمكن تنفيذ هذه الخطوات في أي شركة.</span><span class="sxs-lookup"><span data-stu-id="ba185-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company.</span></span> <span data-ttu-id="ba185-107">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الموضوع، [إنشاء موفرات تكوين وتحديدها بالحالة نشط](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="ba185-107">To complete these steps, you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ba185-108">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="ba185-108">Prerequisites</span></span>
1.    <span data-ttu-id="ba185-109">انتقل إلى **إدارة المؤسسة** > **مساحات العمل‬** > **إعداد التقارير الإلكترونية**‬.</span><span class="sxs-lookup"><span data-stu-id="ba185-109">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2.    <span data-ttu-id="ba185-110">تأكد من وجود موفر التكوين للشركة النموذجية "Litware, Inc." ومن وضع علامة عليه كـ **نشط**.</span><span class="sxs-lookup"><span data-stu-id="ba185-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="ba185-111">في حالة عدم رؤية موفر التكوين هذا، أكمل الخطوات المذكورة في الإجراء [إنشاء موفرات تكوين وتحديدها بالحالة نشط‬](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="ba185-111">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3.    <span data-ttu-id="ba185-112">انقر فوق **تكوينات بيانات التعريف**.</span><span class="sxs-lookup"><span data-stu-id="ba185-112">Click **Metadata configurations**.</span></span> 
4.    <span data-ttu-id="ba185-113">افترض أنه سيتم استخدام RCS لتصميم حل ER لتطبيق Finance and Operations والذي سيتم استخدامه لإنشاء مستندات إلكترونية تحتوي على معلومات من مجال أعمال التجارة الخارجية.</span><span class="sxs-lookup"><span data-stu-id="ba185-113">Assume that RCS will be used to design an ER solution for a Finance and Operation application that will generate electronic documents that contain information from foreign trade business domain.</span></span> <span data-ttu-id="ba185-114">لتحديد التعيين بين نموذج بيانات ER ومصادر البيانات المطلوبة، يجب أن يكون لديك حق الوصول إلى بيانات تعريف تطبيق Finance and Operations في RCS.</span><span class="sxs-lookup"><span data-stu-id="ba185-114">To specify the mapping between ER data model and sources of required data, in RCS we need to have access to metadata of the Finance and Operation application.</span></span> <span data-ttu-id="ba185-115">وبالتالي، كجزء من عملية تصميم حل ER، نكوِّن بيانات تعريف ER جديدة تحتوي على جميع بيانات التعريف المطلوبة حاليًا من أجل إنشاء تقارير ER لمجال الأعمال المحدد.</span><span class="sxs-lookup"><span data-stu-id="ba185-115">Therefore, as part of designing ER solution we configure a new ER metadata configuration containing all metadata that is currently required for generation ER reports for selected business domain.</span></span> 

## <a name="add-metadata-configuration"></a><span data-ttu-id="ba185-116">إضافة تكوين ‏‫بيانات التعريف‬</span><span class="sxs-lookup"><span data-stu-id="ba185-116">Add metadata configuration</span></span> 
1.    <span data-ttu-id="ba185-117">انقر فوق **إنشاء تكوين** لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="ba185-117">Click **Create configuration** to open the drop dialog.</span></span> 
2.    <span data-ttu-id="ba185-118">اكتب في حقل **الاسم** "بيانات تعريف التجارة الخارجية".</span><span class="sxs-lookup"><span data-stu-id="ba185-118">In the **Name** field, type 'Foreign trade metadata'.</span></span> 
3.    <span data-ttu-id="ba185-119">وانقر فوق **إنشاء تكوين**.</span><span class="sxs-lookup"><span data-stu-id="ba185-119">Click **Create configuration**.</span></span> 
4.    <span data-ttu-id="ba185-120">انقر فوق **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="ba185-120">Click **Designer**.</span></span> 
5.    <span data-ttu-id="ba185-121">انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="ba185-121">Click **Add**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ba185-122">يمكنك تحديد كل بيانات التعريف للتطبيق بالكامل أو النماذج المحددة أو الوحدات النمطية المحددة.</span><span class="sxs-lookup"><span data-stu-id="ba185-122">You can select all metadata for the entire application or selected models or selected modules.</span></span> <span data-ttu-id="ba185-123">يجب مراعاة أنه في هذه الحالة ستتم إضافة بيانات التعريف التالية تلقائيًا: جداول السجلات والتعدادات وأنواع البيانات الملحقة.</span><span class="sxs-lookup"><span data-stu-id="ba185-123">Be aware that in this case the following metadata will be automatically added: tables of records, enumerations, and extended data types.</span></span> <span data-ttu-id="ba185-124">عند الحاجة لأنواع إضافية من بيانات التعريف، يجب إضافتها يدويًا.</span><span class="sxs-lookup"><span data-stu-id="ba185-124">When additional types of metadata are needed, they must be added manually.</span></span> 
 
<span data-ttu-id="ba185-125">تتوفر لدينا بعض بيانات التعريف المرتبطة بحركات التجارية الخارجية عن طريق تحديد عناصر بيانات التعريف يدويًا.</span><span class="sxs-lookup"><span data-stu-id="ba185-125">We have some foreign trade transactions related metadata by selecting metadata items manually.</span></span> 
  
6.    <span data-ttu-id="ba185-126">انقر فوق **إضافة مصدر بيانات**.</span><span class="sxs-lookup"><span data-stu-id="ba185-126">Click **Add data source**.</span></span> 
7.    <span data-ttu-id="ba185-127">انقر **سجلات الجدول**.</span><span class="sxs-lookup"><span data-stu-id="ba185-127">Click **Table records**.</span></span> 
8.    <span data-ttu-id="ba185-128">استخدم عامل التصفية السريع في حقل **الاسم** بالقيمة "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي".</span><span class="sxs-lookup"><span data-stu-id="ba185-128">Use the Quick Filter to filter on the **Name** field with a value of 'Intrastat'.</span></span> 
9.    <span data-ttu-id="ba185-129">حدد سجل جدول **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي**.</span><span class="sxs-lookup"><span data-stu-id="ba185-129">Select the **Intrastat** table record.</span></span> 
10.    <span data-ttu-id="ba185-130">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ba185-130">Click **OK**.</span></span>
  
<span data-ttu-id="ba185-131">لقد أضفنا معلومات بيانات التعريف الخاصة بجدول سجلات نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="ba185-131">We added metadata information about the Intrastat table of records.</span></span> 
  
11.    <span data-ttu-id="ba185-132">في الشجرة، وسع **علاقات** **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي بسجلات الجدول**\>.</span><span class="sxs-lookup"><span data-stu-id="ba185-132">In the tree, expand **Table records Intrastat**\>**Relations**.</span></span> 
12.    <span data-ttu-id="ba185-133">في الشجرة، حدد **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي بسجلات الجدول**\>**Relations\IntrastatCommodity (سجلات جدول EcoResCategory)**.</span><span class="sxs-lookup"><span data-stu-id="ba185-133">In the tree, select **Table records Intrastat**\>**Relations\IntrastatCommodity (Table records EcoResCategory)**.</span></span>     
13.    <span data-ttu-id="ba185-134">انقر فوق **إضافة بيانات تعريف**.</span><span class="sxs-lookup"><span data-stu-id="ba185-134">Click **Add metadata**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ba185-135">يجب إضافة بيانات التعريف حول العلاقات المطلوبة لجدول السجلات المحدد يدويًا.</span><span class="sxs-lookup"><span data-stu-id="ba185-135">Metadata about required relations for selected table of records must be added manually.</span></span> 
  
16.    <span data-ttu-id="ba185-136">انقر فوق **إضافة مصدر بيانات**.</span><span class="sxs-lookup"><span data-stu-id="ba185-136">Click **Add data source**.</span></span> 
17.    <span data-ttu-id="ba185-137">انقر فوق **تعداد**.</span><span class="sxs-lookup"><span data-stu-id="ba185-137">Click **Enumeration**.</span></span> 
18.    <span data-ttu-id="ba185-138">استخدم عامل التصفية السريع في حقل **الاسم** بالقيمة "IntrastatDirection".</span><span class="sxs-lookup"><span data-stu-id="ba185-138">Use the Quick Filter to filter on the **Name** field with a value of 'IntrastatDirection'.</span></span> 
19.    <span data-ttu-id="ba185-139">حدد سجل **تعداد IntrastatDirection**.</span><span class="sxs-lookup"><span data-stu-id="ba185-139">Select the **IntrastatDirection enumeration** record.</span></span> 
20.    <span data-ttu-id="ba185-140">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ba185-140">Click **OK**.</span></span> 
21.    <span data-ttu-id="ba185-141">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="ba185-141">Click **Save**.</span></span>  
22.    <span data-ttu-id="ba185-142">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ba185-142">Close the page.</span></span> 
  
## <a name="complete-the-draft-version-of-metadata-configuration"></a><span data-ttu-id="ba185-143">أكمل الإصدار التمهيدي لتكوين بيانات التعريف</span><span class="sxs-lookup"><span data-stu-id="ba185-143">Complete the draft version of metadata configuration</span></span>
1.    <span data-ttu-id="ba185-144">انقر فوق **تغيير الحالة**.</span><span class="sxs-lookup"><span data-stu-id="ba185-144">Click **Change status**.</span></span> 
2.    <span data-ttu-id="ba185-145">انقر فوق **إكمال**.</span><span class="sxs-lookup"><span data-stu-id="ba185-145">Click **Complete**.</span></span> 
3.    <span data-ttu-id="ba185-146">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ba185-146">Click **OK**.</span></span> 
4.    <span data-ttu-id="ba185-147">حدد الإصدار المكتمل **1**.</span><span class="sxs-lookup"><span data-stu-id="ba185-147">Select the completed version **1**.</span></span> 
  
## <a name="export-the-completed-version-of-metadata-configuration-from-application-as-xml-file"></a><span data-ttu-id="ba185-148">صدّر النسخة المكتملة من تكوين بيانات التعريف من التطبيق كملف XML</span><span class="sxs-lookup"><span data-stu-id="ba185-148">Export the completed version of metadata configuration from application as XML file</span></span>
1.    <span data-ttu-id="ba185-149">انقر فوق **تبادل**.</span><span class="sxs-lookup"><span data-stu-id="ba185-149">Click **Exchange**.</span></span> 
2.    <span data-ttu-id="ba185-150">انقر فوق **تصدير كملف XML**.</span><span class="sxs-lookup"><span data-stu-id="ba185-150">Click **Export as XML file**.</span></span> 
3.    <span data-ttu-id="ba185-151">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ba185-151">Click **OK**.</span></span> 
    
<span data-ttu-id="ba185-152">تم حفظ تكوين بيانات تعريف ER الذي تم إنشاؤه كملف XML يمكن استيراده إلى RCS واستخدامه كمصدر للمعلومات حول بيانات التعريف الخاصة بمجال الأعمال التجارية الخارجية.</span><span class="sxs-lookup"><span data-stu-id="ba185-152">The created ER metadata configuration has been saved as XML file that can be imported to RCS and used as the source of information about metadata for the foreign trade business domain.</span></span> <span data-ttu-id="ba185-153">استنادا إلى هذه المعلومات، يمكننا تحديد التعيين بين بيانات تعريف التطبيق ونموذج بيانات ER.</span><span class="sxs-lookup"><span data-stu-id="ba185-153">Based on this information, we can specify the mapping between application metadata and ER data model.</span></span>