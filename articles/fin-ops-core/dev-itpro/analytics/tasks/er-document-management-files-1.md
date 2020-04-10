---
title: التقارير الإلكترونية - استخدام ملفات إدارة المستندات في مخرجات التنسيق‬ (الجزء 1 - إعداد نموذج البيانات)
description: تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لاستخدام ملفات إدارة المستندات (مرفقات) في مخرجات التقارير الإلكترونية.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 800df13e1654bc01304411bfa52f4bbd04e6589a
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142053"
---
# <a name="er-use-document-management-files-in-format-outputs-part-1---prepare-data-model"></a><span data-ttu-id="b8a12-103">التقارير الإلكترونية - استخدام ملفات إدارة المستندات في مخرجات التنسيق‬ (الجزء 1 - إعداد نموذج البيانات)</span><span class="sxs-lookup"><span data-stu-id="b8a12-103">ER Use Document Management files in format outputs (Part 1 - Prepare data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b8a12-104">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لاستخدام ملفات إدارة المستندات (مرفقات) في مخرجات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="b8a12-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="b8a12-105">يمكن تنفيذ هذه الخطوات في أي شركة.</span><span class="sxs-lookup"><span data-stu-id="b8a12-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="b8a12-106">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "إنشاء موفر تكوين ووضع علامة عليه على أنه نشط".</span><span class="sxs-lookup"><span data-stu-id="b8a12-106">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="b8a12-107">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="b8a12-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="b8a12-108">الوصول إلى قائمة التكوينات التي توفرها Microsoft</span><span class="sxs-lookup"><span data-stu-id="b8a12-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="b8a12-109">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="b8a12-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="b8a12-110">تأكد من أن موفر 'Litware, Inc.'</span><span class="sxs-lookup"><span data-stu-id="b8a12-110">Make sure that the 'Litware, Inc.'</span></span> <span data-ttu-id="b8a12-111">متوفر ومن وضع علامة عليه كنشط.</span><span class="sxs-lookup"><span data-stu-id="b8a12-111">provider is available and marked as active.</span></span>  

2. <span data-ttu-id="b8a12-112">حدد الموفر 'Litware, Inc.'</span><span class="sxs-lookup"><span data-stu-id="b8a12-112">Select the 'Litware, Inc.'</span></span> <span data-ttu-id="b8a12-113">.</span><span class="sxs-lookup"><span data-stu-id="b8a12-113">provider.</span></span>
3. <span data-ttu-id="b8a12-114">انقر فوق "المستودعات".</span><span class="sxs-lookup"><span data-stu-id="b8a12-114">Click Repositories.</span></span>

    <span data-ttu-id="b8a12-115">إذا كان مخزن من نوع "موارد العمليات" موجودًا بالفعل، فيمكنك تجاوز الخطوات المتبقية في المهمة الفرعية الحالية.</span><span class="sxs-lookup"><span data-stu-id="b8a12-115">If a repository of the 'Operations resources' type already exists, skip the remaining steps of the current sub-task.</span></span>  

4. <span data-ttu-id="b8a12-116">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="b8a12-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="b8a12-117">في الحقل "نوع مستودع التكوين"، أدخل "موارد العمليات".</span><span class="sxs-lookup"><span data-stu-id="b8a12-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="b8a12-118">انقر فوق إنشاء مستودع.</span><span class="sxs-lookup"><span data-stu-id="b8a12-118">Click Create repository.</span></span>
7. <span data-ttu-id="b8a12-119">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="b8a12-119">Click OK.</span></span>

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a><span data-ttu-id="b8a12-120">الحصول على تكوينات نموذج فاتورة العميل التي توفرها Microsoft</span><span class="sxs-lookup"><span data-stu-id="b8a12-120">Get the Customer invoice model configurations provided by Microsoft</span></span>
1. <span data-ttu-id="b8a12-121">انقر فوق "إظهار عوامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="b8a12-121">Click Show filters.</span></span>
2. <span data-ttu-id="b8a12-122">طبّق عوامل التصفية التالية: أدخل قيمة عامل التصفية "موارد العمليات" في حقل "الاسم" باستخدام عامل التصفية "يبدأ بـ"‬‏‫؛ أدخل قيمة عامل التصفية "" في حقل "الوصف" باستخدام عامل التصفية "يبدأ بـ".</span><span class="sxs-lookup"><span data-stu-id="b8a12-122">Apply the following filters: Enter a filter value of "Operations resources" on the "Name" field using the "begins with" filter operator; Enter a filter value of "" on the "Description" field using the "begins with" filter operator</span></span>
3. <span data-ttu-id="b8a12-123">انقر فوق "إظهار عوامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="b8a12-123">Click Show filters.</span></span>
4. <span data-ttu-id="b8a12-124">انقر فوق "فتح".</span><span class="sxs-lookup"><span data-stu-id="b8a12-124">Click Open.</span></span>
5. <span data-ttu-id="b8a12-125">في الشجرة، حدد "نموذج فاتورة العميل".</span><span class="sxs-lookup"><span data-stu-id="b8a12-125">In the tree, select 'Customer invoice model'.</span></span>

    <span data-ttu-id="b8a12-126">حدد تكوين النموذج "نموذج فاتورة العميل" لاستيراده.</span><span class="sxs-lookup"><span data-stu-id="b8a12-126">Select the model configuration 'Customer invoice model' to import it.</span></span>  

6. <span data-ttu-id="b8a12-127">انقر فوق "استيراد".</span><span class="sxs-lookup"><span data-stu-id="b8a12-127">Click Import.</span></span>

    <span data-ttu-id="b8a12-128">انقر فوق "استيراد" للإصدار 1 من التكوين المحدد.</span><span class="sxs-lookup"><span data-stu-id="b8a12-128">Click Import for version 1 of the selected configuration.</span></span>  

7. <span data-ttu-id="b8a12-129">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="b8a12-129">Click Yes.</span></span>
8. <span data-ttu-id="b8a12-130">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b8a12-130">Close the page.</span></span>
9. <span data-ttu-id="b8a12-131">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b8a12-131">Close the page.</span></span>
10. <span data-ttu-id="b8a12-132">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="b8a12-132">Click Reporting configurations.</span></span>
11. <span data-ttu-id="b8a12-133">في الشجرة، حدد "نموذج فاتورة العميل".</span><span class="sxs-lookup"><span data-stu-id="b8a12-133">In the tree, select 'Customer invoice model'.</span></span>

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a><span data-ttu-id="b8a12-134">أنشئ النموذج المشتق لدعم الوصول إلى ملفات "إدارة المستندات".</span><span class="sxs-lookup"><span data-stu-id="b8a12-134">Create the derived model to support access to the Document Management files.</span></span>
<span data-ttu-id="b8a12-135">ستقوم بإنشاء تكوين خاص بك لنموذج فاتورة العميل يكون مشتقًا من التكوين الذي توفره Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b8a12-135">You will create our own configuration of the Customer invoice model deriving it from the configuration provided by Microsoft.</span></span> <span data-ttu-id="b8a12-136">سوف تستخدم هذا التكوين لتطبيق الوصول إلى ملفات "إدارة المستندات" وجعله متوفرًا للمستندات الإلكترونية التي ستقوم بإنشائها استنادًا إلى هذا النموذج.</span><span class="sxs-lookup"><span data-stu-id="b8a12-136">You will use this configuration to implement access to the Document Management files and make them available for electronic documents that you will create based on this model.</span></span>  
1. <span data-ttu-id="b8a12-137">انقر فوق "إنشاء تكوين" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="b8a12-137">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="b8a12-138">في الحقل "جديد"، أدخل "مشتق من اسم: نموذج فاتورة العميل، Microsoft".</span><span class="sxs-lookup"><span data-stu-id="b8a12-138">In the New field, enter 'Derive from Name: Customer invoice model, Microsoft'.</span></span>
3. <span data-ttu-id="b8a12-139">في الحقل "الاسم، اكتب "نموذج فاتورة العميل (مخصص)".</span><span class="sxs-lookup"><span data-stu-id="b8a12-139">In the Name field, type 'Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="b8a12-140">وانقر فوق إنشاء تكوين.</span><span class="sxs-lookup"><span data-stu-id="b8a12-140">Click Create configuration.</span></span>

