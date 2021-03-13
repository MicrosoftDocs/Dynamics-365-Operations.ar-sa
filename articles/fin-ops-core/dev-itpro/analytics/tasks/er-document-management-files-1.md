---
title: التقارير الإلكترونية - استخدام ملفات إدارة المستندات في مخرجات التنسيق‬ (الجزء 1 - إعداد نموذج البيانات)
description: يوضح هذا الموضوع كيفيه تكوين تنسيق التقارير الكترونيه (ER) لاستخدام ملفات أداره المستندات (المرفقات) في إخراج ER. (جزء 1)
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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bff518c60f0f36bdc88245d79bd82f0c4d0599ed
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092631"
---
# <a name="er-use-document-management-files-in-format-outputs-part-1---prepare-data-model"></a><span data-ttu-id="0faae-104">التقارير الإلكترونية - استخدام ملفات إدارة المستندات في مخرجات التنسيق‬ (الجزء 1 - إعداد نموذج البيانات)</span><span class="sxs-lookup"><span data-stu-id="0faae-104">ER Use Document Management files in format outputs (Part 1 - Prepare data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0faae-105">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لاستخدام ملفات إدارة المستندات (مرفقات) في مخرجات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="0faae-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="0faae-106">يمكن تنفيذ هذه الخطوات في أي شركة.</span><span class="sxs-lookup"><span data-stu-id="0faae-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="0faae-107">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "إنشاء موفر تكوين ووضع علامة عليه على أنه نشط".</span><span class="sxs-lookup"><span data-stu-id="0faae-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="0faae-108">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="0faae-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="0faae-109">الوصول إلى قائمة التكوينات التي توفرها Microsoft</span><span class="sxs-lookup"><span data-stu-id="0faae-109">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="0faae-110">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="0faae-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="0faae-111">تأكد من أن موفر 'Litware, Inc.'</span><span class="sxs-lookup"><span data-stu-id="0faae-111">Make sure that the 'Litware, Inc.'</span></span> <span data-ttu-id="0faae-112">متوفر ومن وضع علامة عليه كنشط.</span><span class="sxs-lookup"><span data-stu-id="0faae-112">provider is available and marked as active.</span></span>  

2. <span data-ttu-id="0faae-113">حدد الموفر 'Litware, Inc.'</span><span class="sxs-lookup"><span data-stu-id="0faae-113">Select the 'Litware, Inc.'</span></span> <span data-ttu-id="0faae-114">.</span><span class="sxs-lookup"><span data-stu-id="0faae-114">provider.</span></span>
3. <span data-ttu-id="0faae-115">انقر فوق "المستودعات".</span><span class="sxs-lookup"><span data-stu-id="0faae-115">Click Repositories.</span></span>

    <span data-ttu-id="0faae-116">إذا كان مخزن من نوع "موارد العمليات" موجودًا بالفعل، فيمكنك تجاوز الخطوات المتبقية في المهمة الفرعية الحالية.</span><span class="sxs-lookup"><span data-stu-id="0faae-116">If a repository of the 'Operations resources' type already exists, skip the remaining steps of the current sub-task.</span></span>  

4. <span data-ttu-id="0faae-117">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="0faae-117">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="0faae-118">في الحقل "نوع مستودع التكوين"، أدخل "موارد العمليات".</span><span class="sxs-lookup"><span data-stu-id="0faae-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="0faae-119">انقر فوق إنشاء مستودع.</span><span class="sxs-lookup"><span data-stu-id="0faae-119">Click Create repository.</span></span>
7. <span data-ttu-id="0faae-120">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="0faae-120">Click OK.</span></span>

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a><span data-ttu-id="0faae-121">الحصول على تكوينات نموذج فاتورة العميل التي توفرها Microsoft</span><span class="sxs-lookup"><span data-stu-id="0faae-121">Get the Customer invoice model configurations provided by Microsoft</span></span>
1. <span data-ttu-id="0faae-122">انقر فوق "إظهار عوامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="0faae-122">Click Show filters.</span></span>
2. <span data-ttu-id="0faae-123">طبّق عوامل التصفية التالية: أدخل قيمة عامل التصفية "موارد العمليات" في حقل "الاسم" باستخدام عامل التصفية "يبدأ بـ"‬‏‫؛ أدخل قيمة عامل التصفية "" في حقل "الوصف" باستخدام عامل التصفية "يبدأ بـ".</span><span class="sxs-lookup"><span data-stu-id="0faae-123">Apply the following filters: Enter a filter value of "Operations resources" on the "Name" field using the "begins with" filter operator; Enter a filter value of "" on the "Description" field using the "begins with" filter operator</span></span>
3. <span data-ttu-id="0faae-124">انقر فوق "إظهار عوامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="0faae-124">Click Show filters.</span></span>
4. <span data-ttu-id="0faae-125">انقر فوق "فتح".</span><span class="sxs-lookup"><span data-stu-id="0faae-125">Click Open.</span></span>
5. <span data-ttu-id="0faae-126">في الشجرة، حدد "نموذج فاتورة العميل".</span><span class="sxs-lookup"><span data-stu-id="0faae-126">In the tree, select 'Customer invoice model'.</span></span>

    <span data-ttu-id="0faae-127">حدد تكوين النموذج "نموذج فاتورة العميل" لاستيراده.</span><span class="sxs-lookup"><span data-stu-id="0faae-127">Select the model configuration 'Customer invoice model' to import it.</span></span>  

6. <span data-ttu-id="0faae-128">انقر فوق "استيراد".</span><span class="sxs-lookup"><span data-stu-id="0faae-128">Click Import.</span></span>

    <span data-ttu-id="0faae-129">انقر فوق "استيراد" للإصدار 1 من التكوين المحدد.</span><span class="sxs-lookup"><span data-stu-id="0faae-129">Click Import for version 1 of the selected configuration.</span></span>  

7. <span data-ttu-id="0faae-130">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="0faae-130">Click Yes.</span></span>
8. <span data-ttu-id="0faae-131">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0faae-131">Close the page.</span></span>
9. <span data-ttu-id="0faae-132">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0faae-132">Close the page.</span></span>
10. <span data-ttu-id="0faae-133">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="0faae-133">Click Reporting configurations.</span></span>
11. <span data-ttu-id="0faae-134">في الشجرة، حدد "نموذج فاتورة العميل".</span><span class="sxs-lookup"><span data-stu-id="0faae-134">In the tree, select 'Customer invoice model'.</span></span>

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a><span data-ttu-id="0faae-135">أنشئ النموذج المشتق لدعم الوصول إلى ملفات "إدارة المستندات".</span><span class="sxs-lookup"><span data-stu-id="0faae-135">Create the derived model to support access to the Document Management files.</span></span>
<span data-ttu-id="0faae-136">ستقوم بإنشاء تكوين خاص بك لنموذج فاتورة العميل يكون مشتقًا من التكوين الذي توفره Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0faae-136">You will create our own configuration of the Customer invoice model deriving it from the configuration provided by Microsoft.</span></span> <span data-ttu-id="0faae-137">سوف تستخدم هذا التكوين لتطبيق الوصول إلى ملفات "إدارة المستندات" وجعله متوفرًا للمستندات الإلكترونية التي ستقوم بإنشائها استنادًا إلى هذا النموذج.</span><span class="sxs-lookup"><span data-stu-id="0faae-137">You will use this configuration to implement access to the Document Management files and make them available for electronic documents that you will create based on this model.</span></span>  
1. <span data-ttu-id="0faae-138">انقر فوق "إنشاء تكوين" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="0faae-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="0faae-139">في الحقل "جديد"، أدخل "مشتق من اسم: نموذج فاتورة العميل، Microsoft".</span><span class="sxs-lookup"><span data-stu-id="0faae-139">In the New field, enter 'Derive from Name: Customer invoice model, Microsoft'.</span></span>
3. <span data-ttu-id="0faae-140">في الحقل "الاسم، اكتب "نموذج فاتورة العميل (مخصص)".</span><span class="sxs-lookup"><span data-stu-id="0faae-140">In the Name field, type 'Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="0faae-141">وانقر فوق إنشاء تكوين.</span><span class="sxs-lookup"><span data-stu-id="0faae-141">Click Create configuration.</span></span>

