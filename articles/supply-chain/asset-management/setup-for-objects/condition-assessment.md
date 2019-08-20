---
title: تقييم الحالة
description: يشرح هذا الموضوع كيفية إنشاء قالب تقييم الحالة والتسجيل على أصل في إدارة الأصول.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5294325f67f0484b39194b5bd9784a2e612001a4
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783032"
---
# <a name="condition-assessment"></a><span data-ttu-id="6d08b-103">تقييم الحالة</span><span class="sxs-lookup"><span data-stu-id="6d08b-103">Condition assessment</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="6d08b-104">يشرح هذا الموضوع كيفية إنشاء قالب تقييم الحالة والتسجيل على أصل في إدارة الأصول.</span><span class="sxs-lookup"><span data-stu-id="6d08b-104">This topic explains how to create a condition assessment template and registration on an asset in Asset Management.</span></span> <span data-ttu-id="6d08b-105">يتم تنفيذ تقييم الحالة على فترات زمنية منتظمة، والهدف الرئيسي هو إنشاء بيانات الحالة على الأصول والمحافظة بها.</span><span class="sxs-lookup"><span data-stu-id="6d08b-105">Condition assessment is performed at regular intervals, and the primary objective is to create and maintain condition data on assets.</span></span> <span data-ttu-id="6d08b-106">ومن المهم، إذا نظرنا إليه من منظور الصيانة الوقائية، مراقبة المعلومات الأساسية مثل الحالة الراهنة، والمدة المتبقية من العمر.</span><span class="sxs-lookup"><span data-stu-id="6d08b-106">Seen from a preventive maintenance perspective, it is important to monitor key information such as current condition, and remaining life span.</span></span> <span data-ttu-id="6d08b-107">وعلاوة على ذلك، إذا قمت بإجراء تقييم الحالة على فترات منتظمة، سوف تكون قادرًا على مراقبة ومقارنة الشروط المطبّقة على الآلات في المصنع.</span><span class="sxs-lookup"><span data-stu-id="6d08b-107">Furthermore, if you carry out condition assessment at regular intervals, you will be able to monitor and compare conditions on the machinery in your factory.</span></span>

<span data-ttu-id="6d08b-108">يمكن استخدام تقييم الحالة لقياس ومراقبة العديد من الشروط المطبقة على المعدات.</span><span class="sxs-lookup"><span data-stu-id="6d08b-108">Condition assessment can be used to measure and monitor many conditions on your equipment.</span></span> <span data-ttu-id="6d08b-109">مثال: يمكنك قياس الاهتزازات على الآلات.</span><span class="sxs-lookup"><span data-stu-id="6d08b-109">Example: You could measure vibrations on your machinery.</span></span> <span data-ttu-id="6d08b-110">بعد تسجيل قياسات الاهتزاز في إدارة الأصول على أنواع مختلفة من المعدات، يمكنك البحث عن أحدث تقييم مسجل وعرض قياسات الاهتزاز.</span><span class="sxs-lookup"><span data-stu-id="6d08b-110">After you have registered vibration measurements in Asset Management on various types of equipment, you can search for the latest registered assessment and view vibration measurements.</span></span>

<span data-ttu-id="6d08b-111">يتم إنشاء تقييم الحالة على الأصول.</span><span class="sxs-lookup"><span data-stu-id="6d08b-111">Condition assessment is created on assets.</span></span> <span data-ttu-id="6d08b-112">يمكنك إعداد قالب تقييم حالة على نوع أصل قبل تنفيذ إجراء تقييم الحالة.</span><span class="sxs-lookup"><span data-stu-id="6d08b-112">You set up a condition assessment template on an asset type before you carry out the condition assessment procedure.</span></span> <span data-ttu-id="6d08b-113">والسبب في استخدام قوالب تقييم الحالة هو تجنب تباين بيانات الحالة المطبّقة على الأصول المماثلة.</span><span class="sxs-lookup"><span data-stu-id="6d08b-113">The reason for using templates for condition assessment is to avoid variation of condition data on similar assets.</span></span> <span data-ttu-id="6d08b-114">تسلسل إعداد واستخدام تقييم الحالة في إدارة الأصول هو: أولاً عليك إعداد قوالب تقييم الحالة المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="6d08b-114">The sequence for setting up and using condition assessment in Asset Management is: First you set up the required condition assessment templates.</span></span> <span data-ttu-id="6d08b-115">بعد ذلك، يمكنك إقران القوالب بأنواع الأصول في نموذج **أنواع الأصول**.</span><span class="sxs-lookup"><span data-stu-id="6d08b-115">Next, you associate templates with asset types in the **Asset types** form.</span></span> <span data-ttu-id="6d08b-116">وأخيراً، يمكنك إنشاء تسجيلات تقييم الحالة على أصل في نموذج **الأصل**.</span><span class="sxs-lookup"><span data-stu-id="6d08b-116">Finally, you can create condition assessment registrations on an asset in the **Asset** form.</span></span>

## <a name="create-a-condition-assessment-template"></a><span data-ttu-id="6d08b-117">إنشاء قالب تقييم حالة</span><span class="sxs-lookup"><span data-stu-id="6d08b-117">Create a condition assessment template</span></span>

1. <span data-ttu-id="6d08b-118">حدد **إدارة الأصول** > **الإعداد** > **أنواع الأصول** > **تقييم الحالة**.</span><span class="sxs-lookup"><span data-stu-id="6d08b-118">Select **Asset management** > **Setup** > **Asset types** > **Condition assessment**.</span></span>
2. <span data-ttu-id="6d08b-119">حدد **جديد** لإنشاء قالب جديد.</span><span class="sxs-lookup"><span data-stu-id="6d08b-119">Select **New** to create a new template.</span></span>
3. <span data-ttu-id="6d08b-120">في حقل **القالب** أدخل معرف القالب.</span><span class="sxs-lookup"><span data-stu-id="6d08b-120">Insert and ID for the template in the **Template** field.</span></span>
4. <span data-ttu-id="6d08b-121">في حقل **الاسم** أدخل اسمًا للقالب.</span><span class="sxs-lookup"><span data-stu-id="6d08b-121">Insert a name for the template in the **Name** field.</span></span>
5. <span data-ttu-id="6d08b-122">في علامة التبويب السريعة **بنود تقييم الحالة**، أضف البنود المطلوبة لتقييم الحالة، بما في ذلك اختيار نوع الحالة المطبّقة المناسبة ووحدة القياس.</span><span class="sxs-lookup"><span data-stu-id="6d08b-122">On the **Condition assessment lines** FastFab, add the lines required for the condition assessment, including selection of the appropriate condition type and measurement unit.</span></span>
6. <span data-ttu-id="6d08b-123">على علامة التبويب السريعة **أنواع الأصول**، أضف أنواع الأصول التي يجب أن تستخدم قالب تقييم الحالة.</span><span class="sxs-lookup"><span data-stu-id="6d08b-123">On the **Asset types** FastTab, add the asset types that should use the condition assessment template.</span></span>
7. <span data-ttu-id="6d08b-124">في حقول **البنود** و**أنواع الأصول** في مجموعة **التفاصيل** عند أعلى الشاشة، سترى عدد بنود التقييم وأنواع الأصول المرتبطة بقالب تقييم الحالة المحدد.</span><span class="sxs-lookup"><span data-stu-id="6d08b-124">In the **Lines** and **Asset types** fields in the **Details** group at the top of the screen, you will see the number of assessment lines and asset types related to the selected condition assessment template.</span></span>


## <a name="create-condition-assessment-registration-on-an-asset"></a><span data-ttu-id="6d08b-125">إنشاء تسجيل تقييم الحالة على أصل</span><span class="sxs-lookup"><span data-stu-id="6d08b-125">Create condition assessment registration on an asset</span></span>

1. <span data-ttu-id="6d08b-126">حدد **إدارة الأصول** > **عام** > **الأصول** > **كل الأصول**.</span><span class="sxs-lookup"><span data-stu-id="6d08b-126">Select **Asset management** > **Common** > **Assets** > **All Assets**.</span></span>
2. <span data-ttu-id="6d08b-127">في القائمة، حدد الأصل الذي تريد إنشاء تسجيل تقييم حالة له.</span><span class="sxs-lookup"><span data-stu-id="6d08b-127">In the list, select the asset for which you want to create a condition assessment registration.</span></span>
3. <span data-ttu-id="6d08b-128">في علامة التبويب **عام**، انقر فوق **تقييم الحالة**.</span><span class="sxs-lookup"><span data-stu-id="6d08b-128">On the **General** tab, click **Condition assessment**.</span></span>
4. <span data-ttu-id="6d08b-129">انقر فوق **جديد** لإنشاء تسجيل جديد.</span><span class="sxs-lookup"><span data-stu-id="6d08b-129">Click **New** to make a new registration.</span></span>
5. <span data-ttu-id="6d08b-130">حدد تاريخ تقييم الحالة في حقل **التاريخ**.</span><span class="sxs-lookup"><span data-stu-id="6d08b-130">Select the date for the condition assessment in the **Date** field.</span></span>
6. <span data-ttu-id="6d08b-131">حدد اسم العامل الذي قام بتسجيل التقييم في حقل **العامل**.</span><span class="sxs-lookup"><span data-stu-id="6d08b-131">Select the name of the worker who carried out the assessment registration in the **Worker** field.</span></span>
7. <span data-ttu-id="6d08b-132">في حقل **البنود**، سترى عدد بنود التقييم التي تم إعدادها في تقييم الحالة.</span><span class="sxs-lookup"><span data-stu-id="6d08b-132">In the **Lines** field, you see the number of assessment lines set up on the condition assessment.</span></span>
8. <span data-ttu-id="6d08b-133">حدد قالبًا لتقييم الحالة في حقل **القالب**.</span><span class="sxs-lookup"><span data-stu-id="6d08b-133">Select a template for the condition assessment in the **Template** field.</span></span> <span data-ttu-id="6d08b-134">يتم إدراج اسم القالب تلقائيًا في حقل **الاسم**، ويتم إدراج بنود التسجيل ذات الصلة في علامة التبويب السريعة **بنود تقييم الحالة**.</span><span class="sxs-lookup"><span data-stu-id="6d08b-134">The name of the template is automatically inserted in the **Name** field, and the related registration lines are inserted on the **Condition assessment lines** FastTab.</span></span>
9. <span data-ttu-id="6d08b-135">يمكنك إدخال ملاحظات تتعلق بتقييم الحالة المحدد في علامة التبويب السريعة **الملاحظات**.</span><span class="sxs-lookup"><span data-stu-id="6d08b-135">You can insert notes relating to the selected condition assessment on the **Notes** FastTab.</span></span>
10. <span data-ttu-id="6d08b-136">لكل بند تقييم حالة، أدخل بيانات القياس في حقل **القيمة**.</span><span class="sxs-lookup"><span data-stu-id="6d08b-136">For each condition assessment line, insert measurement data in the **Value** field.</span></span>
11. <span data-ttu-id="6d08b-137">يمكنك إدخال تعليق يرتبط ببند التسجيل المحدد في علامة التبويب السريعة **بنود تقييم الحالة** > حقل **التعليقات**.</span><span class="sxs-lookup"><span data-stu-id="6d08b-137">You can insert a comment relating to the selected registration line on the **Condition assessment lines** FastTab > **Comments** field.</span></span> <span data-ttu-id="6d08b-138">إذا قمت بإضافة تعليق على بند، فسيتم تحديد خانة الاختيار **التعليق** تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="6d08b-138">If you add a comment on a line, the **Comment** check box is automatically selected.</span></span>

<span data-ttu-id="6d08b-139">بعد إجراء تسجيل تقييم حالة على أصل، يمكنك طباعة تقرير تقييم الحالة.</span><span class="sxs-lookup"><span data-stu-id="6d08b-139">After you have made a condition assessment registration on an asset, you can print a condition assessment report.</span></span>

>[!NOTE]
><span data-ttu-id="6d08b-140">يمكنك أيضًا تسجيل تقييم الحالة في أمر عمل (**إدارة الأصول** > **عام** > **أوامر العمل** > **كل أوامر العمل** >  زر **تقييم الحالة**.)</span><span class="sxs-lookup"><span data-stu-id="6d08b-140">You can also register condition assessment on a work order (**Asset management** > **Common** > **Work orders** > **All Work orders** > **Condition assessment** button.)</span></span>
