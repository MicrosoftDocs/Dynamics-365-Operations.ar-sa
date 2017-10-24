--- 
title: "إعداد نموذج بيانات لاستخدام ملفات إدارة المستندات في مخرجات تنسيق للتقارير الإلكترونية (ER)"
description: "تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لاستخدام ملفات إدارة المستندات (مرفقات) في مخرجات التقارير الإلكترونية."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 5d224afd799306828a59e97f7f3bcd4cb831537c
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="prepare-data-model-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a><span data-ttu-id="553d0-103">إعداد نموذج بيانات لاستخدام ملفات إدارة المستندات في مخرجات تنسيق للتقارير الإلكترونية (ER)</span><span class="sxs-lookup"><span data-stu-id="553d0-103">Prepare data model to use Document Management files in format outputs for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="553d0-104">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لاستخدام ملفات إدارة المستندات (مرفقات) في مخرجات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="553d0-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="553d0-105">يمكن تنفيذ هذه الخطوات في أي شركة.</span><span class="sxs-lookup"><span data-stu-id="553d0-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="553d0-106">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "إنشاء موفر تكوين ووضع علامة عليه على أنه نشط".</span><span class="sxs-lookup"><span data-stu-id="553d0-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="553d0-107">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="553d0-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="553d0-108">الوصول إلى قائمة التكوينات التي توفرها Microsoft</span><span class="sxs-lookup"><span data-stu-id="553d0-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="553d0-109">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="553d0-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="553d0-110">تأكد من أن موفر 'Litware, Inc.'</span><span class="sxs-lookup"><span data-stu-id="553d0-110">Make sure that the 'Litware, Inc.'</span></span> <span data-ttu-id="553d0-111">متوفر ومن وضع علامة عليه كنشط.</span><span class="sxs-lookup"><span data-stu-id="553d0-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="553d0-112">حدد الموفر 'Litware, Inc.'</span><span class="sxs-lookup"><span data-stu-id="553d0-112">Select the 'Litware, Inc.'</span></span> <span data-ttu-id="553d0-113">.</span><span class="sxs-lookup"><span data-stu-id="553d0-113">provider.</span></span>
3. <span data-ttu-id="553d0-114">انقر فوق "المستودعات".</span><span class="sxs-lookup"><span data-stu-id="553d0-114">Click Repositories.</span></span>
    * <span data-ttu-id="553d0-115">إذا كان مخزن من نوع "موارد العمليات" موجودًا بالفعل، فيمكنك تجاوز الخطوات المتبقية في المهمة الفرعية الحالية.</span><span class="sxs-lookup"><span data-stu-id="553d0-115">If a repository of the 'Operations resources' type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="553d0-116">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="553d0-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="553d0-117">في الحقل "نوع مستودع التكوين"، أدخل "موارد العمليات".</span><span class="sxs-lookup"><span data-stu-id="553d0-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="553d0-118">انقر فوق إنشاء مستودع.</span><span class="sxs-lookup"><span data-stu-id="553d0-118">Click Create repository.</span></span>
7. <span data-ttu-id="553d0-119">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="553d0-119">Click OK.</span></span>

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a><span data-ttu-id="553d0-120">الحصول على تكوينات نموذج فاتورة العميل التي توفرها Microsoft</span><span class="sxs-lookup"><span data-stu-id="553d0-120">Get the Customer invoice model configurations provided by Microsoft</span></span>
1. <span data-ttu-id="553d0-121">انقر فوق "إظهار عوامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="553d0-121">Click Show filters.</span></span>
2. <span data-ttu-id="553d0-122">طبّق عوامل التصفية التالية: أدخل قيمة عامل التصفية "موارد العمليات" في حقل "الاسم" باستخدام عامل التصفية "يبدأ بـ"‬‏‫؛ أدخل قيمة عامل التصفية "" في حقل "الوصف" باستخدام عامل التصفية "يبدأ بـ".</span><span class="sxs-lookup"><span data-stu-id="553d0-122">Apply the following filters: Enter a filter value of "Operations resources" on the "Name" field using the "begins with" filter operator; Enter a filter value of "" on the "Description" field using the "begins with" filter operator</span></span>
3. <span data-ttu-id="553d0-123">انقر فوق "إظهار عوامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="553d0-123">Click Show filters.</span></span>
4. <span data-ttu-id="553d0-124">انقر فوق "فتح".</span><span class="sxs-lookup"><span data-stu-id="553d0-124">Click Open.</span></span>
5. <span data-ttu-id="553d0-125">في الشجرة، حدد "نموذج فاتورة العميل".</span><span class="sxs-lookup"><span data-stu-id="553d0-125">In the tree, select 'Customer invoice model'.</span></span>
    * <span data-ttu-id="553d0-126">حدد تكوين النموذج "نموذج فاتورة العميل" لاستيراده.</span><span class="sxs-lookup"><span data-stu-id="553d0-126">Select the model configuration 'Customer invoice model' to import it.</span></span>  
6. <span data-ttu-id="553d0-127">انقر فوق "استيراد".</span><span class="sxs-lookup"><span data-stu-id="553d0-127">Click Import.</span></span>
    * <span data-ttu-id="553d0-128">انقر فوق "استيراد" للإصدار 1 من التكوين المحدد.</span><span class="sxs-lookup"><span data-stu-id="553d0-128">Click Import for version 1 of the selected configuration.</span></span>  
7. <span data-ttu-id="553d0-129">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="553d0-129">Click Yes.</span></span>
8. <span data-ttu-id="553d0-130">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="553d0-130">Close the page.</span></span>
9. <span data-ttu-id="553d0-131">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="553d0-131">Close the page.</span></span>
10. <span data-ttu-id="553d0-132">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="553d0-132">Click Reporting configurations.</span></span>
11. <span data-ttu-id="553d0-133">في الشجرة، حدد "نموذج فاتورة العميل".</span><span class="sxs-lookup"><span data-stu-id="553d0-133">In the tree, select 'Customer invoice model'.</span></span>

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a><span data-ttu-id="553d0-134">أنشئ النموذج المشتق لدعم الوصول إلى ملفات "إدارة المستندات".</span><span class="sxs-lookup"><span data-stu-id="553d0-134">Create the derived model to support access to the Document Management files.</span></span>
    * <span data-ttu-id="553d0-135">ستقوم بإنشاء تكوين خاص بك لنموذج فاتورة العميل يكون مشتقًا من التكوين الذي توفره Microsoft.</span><span class="sxs-lookup"><span data-stu-id="553d0-135">You will create our own configuration of the Customer invoice model deriving it from the configuration provided by Microsoft.</span></span> <span data-ttu-id="553d0-136">سوف تستخدم هذا التكوين لتطبيق الوصول إلى ملفات "إدارة المستندات" وجعله متوفرًا للمستندات الإلكترونية التي ستقوم بإنشائها استنادًا إلى هذا النموذج.</span><span class="sxs-lookup"><span data-stu-id="553d0-136">You will use this configuration to implement access to the Document Management files and make them available for electronic documents that you will create based on this model.</span></span>  
1. <span data-ttu-id="553d0-137">انقر فوق "إنشاء تكوين" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="553d0-137">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="553d0-138">في الحقل "جديد"، أدخل "مشتق من اسم: نموذج فاتورة العميل، Microsoft".</span><span class="sxs-lookup"><span data-stu-id="553d0-138">In the New field, enter 'Derive from Name: Customer invoice model, Microsoft'.</span></span>
3. <span data-ttu-id="553d0-139">في الحقل "الاسم، اكتب "نموذج فاتورة العميل (مخصص)".</span><span class="sxs-lookup"><span data-stu-id="553d0-139">In the Name field, type 'Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="553d0-140">نموذج فاتورة العميل (مخصص)</span><span class="sxs-lookup"><span data-stu-id="553d0-140">Customer invoice model (custom)</span></span>  
4. <span data-ttu-id="553d0-141">وانقر فوق إنشاء تكوين.</span><span class="sxs-lookup"><span data-stu-id="553d0-141">Click Create configuration.</span></span>


