---
title: إعداد بيانات تعريف التطبيق لاستخدامها في RCS
description: يوضح هذا الموضوع كيفيه إنشاء تكوين جديد لاعداد التقارير يحتوي علي بيانات تعريف التطبيق.
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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d5f55d089a88642cb2bda70274472ad0f0e45cd7
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/30/2021
ms.locfileid: "5094230"
---
# <a name="prepare-application-metadata-to-be-used-in-rcs"></a><span data-ttu-id="d5a2f-103">إعداد بيانات تعريف التطبيق لاستخدامها في RCS</span><span class="sxs-lookup"><span data-stu-id="d5a2f-103">Prepare application metadata to be used in RCS</span></span>
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d5a2f-104">توضح الخطوات التالية كيف يمكن لمستخدم يشغل دور المسؤول نظام أو مطور التقارير الإلكترونية إنشاء تكوين التقارير الإلكترونية الجديدة (ER) التي تحتوي علي بيانات تعريف التطبيق لتصميم تكوينات تعيين نموذج ER في Regulatory configuration servic (RCS).</span><span class="sxs-lookup"><span data-stu-id="d5a2f-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains application metadata for designing ER model mapping configurations in Regulatory configuration service (RCS).</span></span> <span data-ttu-id="d5a2f-105">يتم استخدام هذا التكوين لتصميم نموذج تكوين تعيين لنموذج ER للوصول إلى حركات التجارية الخارجية.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-105">This configuration will be used for designing a sample ER model mapping configuration to access foreign trade transactions.</span></span> <span data-ttu-id="d5a2f-106">في هذا المثال، ستقوم بإنشاء تكوين لشركة نموذج، .Litware, Inc ويمكن تنفيذ هذه الخطوات في أي شركة.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company.</span></span> <span data-ttu-id="d5a2f-107">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الموضوع، [إنشاء موفرات تكوين وتحديدها بالحالة نشط](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="d5a2f-107">To complete these steps, you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d5a2f-108">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="d5a2f-108">Prerequisites</span></span>
1.    <span data-ttu-id="d5a2f-109">انتقل إلى **إدارة المؤسسة** > **مساحات العمل‬** > **إعداد التقارير الإلكترونية**‬.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-109">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2.    <span data-ttu-id="d5a2f-110">تأكد من وجود موفر التكوين للشركة النموذجية "Litware, Inc." ومن وضع علامة عليه كـ **نشط**.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="d5a2f-111">في حالة عدم رؤية موفر التكوين هذا، أكمل الخطوات المذكورة في الإجراء [إنشاء موفرات تكوين وتحديدها بالحالة نشط‬](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="d5a2f-111">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3.    <span data-ttu-id="d5a2f-112">انقر فوق **تكوينات بيانات التعريف**.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-112">Click **Metadata configurations**.</span></span> 
4.    <span data-ttu-id="d5a2f-113">افترض أنه سيتم استخدام RCS لتصميم حل ER لتطبيق Finance and Operations والذي سيتم استخدامه لإنشاء مستندات إلكترونية تحتوي على معلومات من مجال أعمال التجارة الخارجية.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-113">Assume that RCS will be used to design an ER solution for a Finance and Operation application that will generate electronic documents that contain information from foreign trade business domain.</span></span> <span data-ttu-id="d5a2f-114">لتحديد التعيين بين نموذج بيانات ER ومصادر البيانات المطلوبة، يجب أن يكون لديك حق الوصول إلى بيانات تعريف تطبيق Finance and Operations في RCS.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-114">To specify the mapping between ER data model and sources of required data, in RCS we need to have access to metadata of the Finance and Operation application.</span></span> <span data-ttu-id="d5a2f-115">وبالتالي، كجزء من عملية تصميم حل ER، نكوِّن بيانات تعريف ER جديدة تحتوي على جميع بيانات التعريف المطلوبة حاليًا من أجل إنشاء تقارير ER لمجال الأعمال المحدد.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-115">Therefore, as part of designing ER solution we configure a new ER metadata configuration containing all metadata that is currently required for generation ER reports for selected business domain.</span></span> 

## <a name="add-metadata-configuration"></a><span data-ttu-id="d5a2f-116">إضافة تكوين ‏‫بيانات التعريف‬</span><span class="sxs-lookup"><span data-stu-id="d5a2f-116">Add metadata configuration</span></span> 
1.    <span data-ttu-id="d5a2f-117">انقر فوق **إنشاء تكوين** لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-117">Click **Create configuration** to open the drop dialog.</span></span> 
2.    <span data-ttu-id="d5a2f-118">اكتب في حقل **الاسم** "بيانات تعريف التجارة الخارجية".</span><span class="sxs-lookup"><span data-stu-id="d5a2f-118">In the **Name** field, type 'Foreign trade metadata'.</span></span> 
3.    <span data-ttu-id="d5a2f-119">وانقر فوق **إنشاء تكوين**.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-119">Click **Create configuration**.</span></span> 
4.    <span data-ttu-id="d5a2f-120">انقر فوق **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-120">Click **Designer**.</span></span> 
5.    <span data-ttu-id="d5a2f-121">انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-121">Click **Add**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d5a2f-122">يمكنك تحديد كل بيانات التعريف للتطبيق بالكامل أو النماذج المحددة أو الوحدات النمطية المحددة.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-122">You can select all metadata for the entire application or selected models or selected modules.</span></span> <span data-ttu-id="d5a2f-123">يجب مراعاة أنه في هذه الحالة ستتم إضافة بيانات التعريف التالية تلقائيًا: جداول السجلات والتعدادات وأنواع البيانات الملحقة.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-123">Be aware that in this case the following metadata will be automatically added: tables of records, enumerations, and extended data types.</span></span> <span data-ttu-id="d5a2f-124">عند الحاجة لأنواع إضافية من بيانات التعريف، يجب إضافتها يدويًا.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-124">When additional types of metadata are needed, they must be added manually.</span></span> 
 
<span data-ttu-id="d5a2f-125">تتوفر لدينا بعض بيانات التعريف المرتبطة بحركات التجارية الخارجية عن طريق تحديد عناصر بيانات التعريف يدويًا.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-125">We have some foreign trade transactions related metadata by selecting metadata items manually.</span></span> 
  
6.    <span data-ttu-id="d5a2f-126">انقر فوق **إضافة مصدر بيانات**.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-126">Click **Add data source**.</span></span> 
7.    <span data-ttu-id="d5a2f-127">انقر **سجلات الجدول**.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-127">Click **Table records**.</span></span> 
8.    <span data-ttu-id="d5a2f-128">استخدم عامل التصفية السريع في حقل **الاسم** بالقيمة "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي".</span><span class="sxs-lookup"><span data-stu-id="d5a2f-128">Use the Quick Filter to filter on the **Name** field with a value of 'Intrastat'.</span></span> 
9.    <span data-ttu-id="d5a2f-129">حدد سجل جدول **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي**.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-129">Select the **Intrastat** table record.</span></span> 
10.    <span data-ttu-id="d5a2f-130">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-130">Click **OK**.</span></span>
  
<span data-ttu-id="d5a2f-131">لقد أضفنا معلومات بيانات التعريف الخاصة بجدول سجلات نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-131">We added metadata information about the Intrastat table of records.</span></span> 
  
11.    <span data-ttu-id="d5a2f-132">في الشجرة، وسع **علاقات** **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي بسجلات الجدول**\>.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-132">In the tree, expand **Table records Intrastat**\>**Relations**.</span></span> 
12.    <span data-ttu-id="d5a2f-133">في الشجرة، حدد **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي بسجلات الجدول**\>**Relations\IntrastatCommodity (سجلات جدول EcoResCategory)**.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-133">In the tree, select **Table records Intrastat**\>**Relations\IntrastatCommodity (Table records EcoResCategory)**.</span></span>     
13.    <span data-ttu-id="d5a2f-134">انقر فوق **إضافة بيانات تعريف**.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-134">Click **Add metadata**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d5a2f-135">يجب إضافة بيانات التعريف حول العلاقات المطلوبة لجدول السجلات المحدد يدويًا.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-135">Metadata about required relations for selected table of records must be added manually.</span></span> 
  
16.    <span data-ttu-id="d5a2f-136">انقر فوق **إضافة مصدر بيانات**.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-136">Click **Add data source**.</span></span> 
17.    <span data-ttu-id="d5a2f-137">انقر فوق **تعداد**.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-137">Click **Enumeration**.</span></span> 
18.    <span data-ttu-id="d5a2f-138">استخدم عامل التصفية السريع في حقل **الاسم** بالقيمة "IntrastatDirection".</span><span class="sxs-lookup"><span data-stu-id="d5a2f-138">Use the Quick Filter to filter on the **Name** field with a value of 'IntrastatDirection'.</span></span> 
19.    <span data-ttu-id="d5a2f-139">حدد سجل **تعداد IntrastatDirection**.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-139">Select the **IntrastatDirection enumeration** record.</span></span> 
20.    <span data-ttu-id="d5a2f-140">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-140">Click **OK**.</span></span> 
21.    <span data-ttu-id="d5a2f-141">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-141">Click **Save**.</span></span>  
22.    <span data-ttu-id="d5a2f-142">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-142">Close the page.</span></span> 
  
## <a name="complete-the-draft-version-of-metadata-configuration"></a><span data-ttu-id="d5a2f-143">أكمل الإصدار التمهيدي لتكوين بيانات التعريف</span><span class="sxs-lookup"><span data-stu-id="d5a2f-143">Complete the draft version of metadata configuration</span></span>
1.    <span data-ttu-id="d5a2f-144">انقر فوق **تغيير الحالة**.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-144">Click **Change status**.</span></span> 
2.    <span data-ttu-id="d5a2f-145">انقر فوق **إكمال**.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-145">Click **Complete**.</span></span> 
3.    <span data-ttu-id="d5a2f-146">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-146">Click **OK**.</span></span> 
4.    <span data-ttu-id="d5a2f-147">حدد الإصدار المكتمل **1**.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-147">Select the completed version **1**.</span></span> 
  
## <a name="export-the-completed-version-of-metadata-configuration-from-application-as-xml-file"></a><span data-ttu-id="d5a2f-148">صدّر النسخة المكتملة من تكوين بيانات التعريف من التطبيق كملف XML</span><span class="sxs-lookup"><span data-stu-id="d5a2f-148">Export the completed version of metadata configuration from application as XML file</span></span>
1.    <span data-ttu-id="d5a2f-149">انقر فوق **تبادل**.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-149">Click **Exchange**.</span></span> 
2.    <span data-ttu-id="d5a2f-150">انقر فوق **تصدير كملف XML**.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-150">Click **Export as XML file**.</span></span> 
3.    <span data-ttu-id="d5a2f-151">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-151">Click **OK**.</span></span> 
    
<span data-ttu-id="d5a2f-152">تم حفظ تكوين بيانات تعريف ER الذي تم إنشاؤه كملف XML يمكن استيراده إلى RCS واستخدامه كمصدر للمعلومات حول بيانات التعريف الخاصة بمجال الأعمال التجارية الخارجية.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-152">The created ER metadata configuration has been saved as XML file that can be imported to RCS and used as the source of information about metadata for the foreign trade business domain.</span></span> <span data-ttu-id="d5a2f-153">استنادا إلى هذه المعلومات، يمكننا تحديد التعيين بين بيانات تعريف التطبيق ونموذج بيانات ER.</span><span class="sxs-lookup"><span data-stu-id="d5a2f-153">Based on this information, we can specify the mapping between application metadata and ER data model.</span></span>
