---
title: التقارير الإلكترونية - تكوين التنسيق لتنفيذ عمليات الجرد والتجميع (الجزء 1 - إنشاء التنسيق)
description: تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لتنفيذ عمليات الجرد والتجميع بالاستناد إلى البيانات الخاصة بالمخرجات النصية المُنشأة بالفعل.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a7a2559bdadbfc74a14bd0e7add9c2f794226e0b
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141915"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1---create-format"></a><span data-ttu-id="0a1e3-103">التقارير الإلكترونية - تكوين التنسيق لتنفيذ عمليات الجرد والتجميع (الجزء 1 - إنشاء التنسيق)</span><span class="sxs-lookup"><span data-stu-id="0a1e3-103">ER Configure format to do counting and summing (Part 1 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0a1e3-104">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لتنفيذ عمليات الجرد والتجميع بالاستناد إلى البيانات الخاصة بالمخرجات النصية المُنشأة بالفعل.</span><span class="sxs-lookup"><span data-stu-id="0a1e3-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="0a1e3-105">يمكن تنفيذ هذه الخطوات في أي شركة.</span><span class="sxs-lookup"><span data-stu-id="0a1e3-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="0a1e3-106">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "إنشاء موفر تكوين ووضع علامة عليه على أنه نشط".</span><span class="sxs-lookup"><span data-stu-id="0a1e3-106">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="0a1e3-107">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="0a1e3-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="0a1e3-108">الوصول إلى قائمة التكوينات التي توفرها Microsoft</span><span class="sxs-lookup"><span data-stu-id="0a1e3-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="0a1e3-109">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="0a1e3-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="0a1e3-110">تأكد من أن موفر “Litware, Inc.”</span><span class="sxs-lookup"><span data-stu-id="0a1e3-110">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="0a1e3-111">متوفر ومن وضع علامة عليه كنشط.</span><span class="sxs-lookup"><span data-stu-id="0a1e3-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="0a1e3-112">حدد الموفر “Litware, Inc.”</span><span class="sxs-lookup"><span data-stu-id="0a1e3-112">Select the "Litware, Inc."</span></span> <span data-ttu-id="0a1e3-113">.</span><span class="sxs-lookup"><span data-stu-id="0a1e3-113">provider.</span></span>
3. <span data-ttu-id="0a1e3-114">انقر فوق "المستودعات".</span><span class="sxs-lookup"><span data-stu-id="0a1e3-114">Click Repositories.</span></span>
    * <span data-ttu-id="0a1e3-115">إذا كان مخزن من نوع "موارد العمليات" موجودًا بالفعل، فيمكنك تجاوز الخطوات المتبقية في المهمة الفرعية الحالية.</span><span class="sxs-lookup"><span data-stu-id="0a1e3-115">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="0a1e3-116">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="0a1e3-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="0a1e3-117">في الحقل "نوع مستودع التكوين"، أدخل "موارد العمليات".</span><span class="sxs-lookup"><span data-stu-id="0a1e3-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="0a1e3-118">انقر فوق إنشاء مستودع.</span><span class="sxs-lookup"><span data-stu-id="0a1e3-118">Click Create repository.</span></span>
7. <span data-ttu-id="0a1e3-119">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="0a1e3-119">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="0a1e3-120">الحصول على تكوينات نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي التي توفرها Microsoft</span><span class="sxs-lookup"><span data-stu-id="0a1e3-120">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="0a1e3-121">انقر فوق "فتح".</span><span class="sxs-lookup"><span data-stu-id="0a1e3-121">Click Open.</span></span>
2. <span data-ttu-id="0a1e3-122">في الشجرة، حدد "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬\نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (DE)"</span><span class="sxs-lookup"><span data-stu-id="0a1e3-122">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="0a1e3-123">انقر فوق "استيراد".</span><span class="sxs-lookup"><span data-stu-id="0a1e3-123">Click Import.</span></span>
    * <span data-ttu-id="0a1e3-124">انقر فوق "استيراد" للإصدار 1.1 من التكوين المحدد.</span><span class="sxs-lookup"><span data-stu-id="0a1e3-124">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="0a1e3-125">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="0a1e3-125">Click Yes.</span></span>
5. <span data-ttu-id="0a1e3-126">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0a1e3-126">Close the page.</span></span>
6. <span data-ttu-id="0a1e3-127">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0a1e3-127">Close the page.</span></span>
7. <span data-ttu-id="0a1e3-128">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="0a1e3-128">Click Reporting configurations.</span></span>
8. <span data-ttu-id="0a1e3-129">في الشجرة، قم بتوسيع "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي".</span><span class="sxs-lookup"><span data-stu-id="0a1e3-129">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="0a1e3-130">في الشجرة، حدد "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬\نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (DE)"</span><span class="sxs-lookup"><span data-stu-id="0a1e3-130">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>

