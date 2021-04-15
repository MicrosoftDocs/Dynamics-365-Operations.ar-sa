---
title: إدارة دورة حياة تكوين إعداد التقارير الإلكترونية
description: يُوضح هذا الموضوع كيفية إدارة دورة حياة تكوينات التقارير الإلكترونية لحل Microsoft Dynamics 365 Finance.
author: NickSelin
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 165f2c981b550f8a6fd4d2ce08763e6fa3c8b6e7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750096"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a><span data-ttu-id="d27f6-103">إدارة دورة حياة تكوين إعداد التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="d27f6-103">Manage the Electronic reporting (ER) configuration lifecycle</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d27f6-104">يُوضح هذا الموضوع كيفية إدارة دورة حياة تكوينات التقارير الإلكترونية لحل Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="d27f6-104">This topic describes how to manage the lifecycle of Electronic reporting (ER) configurations for Microsoft Dynamics 365 Finance.</span></span>

## <a name="overview"></a><span data-ttu-id="d27f6-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="d27f6-105">Overview</span></span>

<span data-ttu-id="d27f6-106">تُعد التقارير الإلكترونية محركًا يدعم المستندات الإلكترونية المطلوبة قانونًا والخاصة ببلد معين.</span><span class="sxs-lookup"><span data-stu-id="d27f6-106">Electronic reporting (ER) is an engine that supports statutory required and country-specific electronic documents.</span></span> <span data-ttu-id="d27f6-107">بشكل عام، تفترض التقارير الإلكترونية إمكانية تنفيذ المهام التالية لمستند إلكتروني واحد.</span><span class="sxs-lookup"><span data-stu-id="d27f6-107">In general, ER assumes an ability to perform the following tasks for a single electronic document.</span></span> <span data-ttu-id="d27f6-108">للحصول على مزيد من التفاصيل، راجع [نظرة عامة على التقارير الإلكترونية (ER)](general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="d27f6-108">For more details, see [Electronic reporting (ER) overview](general-electronic-reporting.md).</span></span>

- <span data-ttu-id="d27f6-109">تصميم قالب لمستند إلكتروني:</span><span class="sxs-lookup"><span data-stu-id="d27f6-109">Design a template for an electronic document:</span></span>

    - <span data-ttu-id="d27f6-110">تحديد مصادر البيانات اللازمة التي يمكن تقديمها في هذا المستند:</span><span class="sxs-lookup"><span data-stu-id="d27f6-110">Identify the required sources of data that can be presented in the document:</span></span>

        - <span data-ttu-id="d27f6-111">البيانات الرئيسية مثل جداول البيانات وكيانات البيانات والفئات.</span><span class="sxs-lookup"><span data-stu-id="d27f6-111">Underlying data, such as data tables, data entities, and classes.</span></span>
        - <span data-ttu-id="d27f6-112">خصائص خاصة بالعملية مثل تاريخ ووقت التنفيذ والمنطقة الزمنية.</span><span class="sxs-lookup"><span data-stu-id="d27f6-112">Process-specific properties, such as execution date and time, and time zone.</span></span>
        - <span data-ttu-id="d27f6-113">معلمات إدخال المستخدم، يتم تحديدها من قِبل المستخدم في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="d27f6-113">User input parameters, specified by the end user at run time.</span></span>

    - <span data-ttu-id="d27f6-114">تعريف عناصر المستندات اللازمة، فضلاً عن مخططها لتحديد تنسيق المستند النهائي.</span><span class="sxs-lookup"><span data-stu-id="d27f6-114">Define the required document elements and their topology to specify a final document format.</span></span>
    - <span data-ttu-id="d27f6-115">تكوين تدفق البيانات المطلوب من مصادر البيانات المحددة إلى عناصر المستند المحددة (عبر ارتباطات مصادر البيانات بمكونات تنسيق المستند) وتحديد منطق التحكم في العملية.</span><span class="sxs-lookup"><span data-stu-id="d27f6-115">Configure the desired flow of data from selected data sources to defined document elements (via data source bindings to document format components), and specify process control logic.</span></span>

- <span data-ttu-id="d27f6-116">جعل قالب متوفرًا بحيث يمكن استخدامه في مثيلات أخرى:</span><span class="sxs-lookup"><span data-stu-id="d27f6-116">Make a template available so that it can be used in other instances:</span></span>

    - <span data-ttu-id="d27f6-117">تحويل قالب مستند تم إنشاؤه إلى تكوين التقارير الإلكترونية وتصدير التكوين من المثيل الحالي كحزمة XML يمكن تخزينها محليًا أو في LCS.</span><span class="sxs-lookup"><span data-stu-id="d27f6-117">Transform a document template that was created into an ER configuration, and export the configuration from the current application instance as an XML package that can be stored either locally or in LCS.</span></span>
    - <span data-ttu-id="d27f6-118">تحويل تكوين التقارير الإلكترونية إلى قالب مستند تطبيق.</span><span class="sxs-lookup"><span data-stu-id="d27f6-118">Transform an ER configuration into an application document template.</span></span>
    - <span data-ttu-id="d27f6-119">استيراد حزمة XML مخزنة محليًا أو في LCS إلى المثيل الحالي.</span><span class="sxs-lookup"><span data-stu-id="d27f6-119">Import an XML package that is stored either locally or in LCS into the current instance.</span></span>

- <span data-ttu-id="d27f6-120">تخصيص قالب مستند إلكتروني:</span><span class="sxs-lookup"><span data-stu-id="d27f6-120">Customize the template of an electronic document:</span></span>

    - <span data-ttu-id="d27f6-121">إحضار قالب من LCS إلى المثيل الحالي كتكوين تقرير إلكتروني.</span><span class="sxs-lookup"><span data-stu-id="d27f6-121">Bring a template from LCS into the current instance as an ER configuration.</span></span>
    - <span data-ttu-id="d27f6-122">تصميم إصدار مخصص من تكوين تقرير إلكتروني، والاحتفاظ بمرجع إلى الإصدار الأساسي.</span><span class="sxs-lookup"><span data-stu-id="d27f6-122">Design a custom version of an ER configuration, and keep a reference to the base version.</span></span>

- <span data-ttu-id="d27f6-123">دمج قالب بعملية تجارية معينة، بحيث يكون متوفرًا في التطبيق:</span><span class="sxs-lookup"><span data-stu-id="d27f6-123">Integrate a template with a particular business process, so that it's available in the application:</span></span>

    - <span data-ttu-id="d27f6-124">تكوين الإعدادات بحيث يبدأ التطبيق باستخدام تكوين التقارير الإلكترونية، من خلال الإشارة إلى ذلك التكوين في معلمة مرتبطة بالعملية.</span><span class="sxs-lookup"><span data-stu-id="d27f6-124">Configure settings so that the application starts to use an ER configuration, by referring to that configuration in a process-related parameter.</span></span> <span data-ttu-id="d27f6-125">على سبيل المثال، يمكنك الإشارة إلى تكوين التقرير الإلكتروني في طريقة دفع حسابات دائنة لإنشاء رسالة دفع إلكترونية لمعالجة الفواتير.</span><span class="sxs-lookup"><span data-stu-id="d27f6-125">For example, refer to the ER configuration in a specific Accounts payable payment method to generate an electronic payment message for processing invoices.</span></span>

- <span data-ttu-id="d27f6-126">استخدام قالب في عملية تجارية معينة:</span><span class="sxs-lookup"><span data-stu-id="d27f6-126">Use a template in a specific business process:</span></span>

    - <span data-ttu-id="d27f6-127">‏‫تشغيل تكوين تقرير إلكتروني في عملية تجارية معينة.</span><span class="sxs-lookup"><span data-stu-id="d27f6-127">Run an ER configuration in a specific business process.</span></span> <span data-ttu-id="d27f6-128">على سبيل المثال، لإنشاء رسالة دفع إلكترونية لمعالجة الفواتير عند تحديد طريقة دفع تشير إلى تكوين تقرير إلكتروني.</span><span class="sxs-lookup"><span data-stu-id="d27f6-128">For example, to generate an electronic payment message for processing invoices when a payment method that references the ER configuration is selected.</span></span>

## <a name="concepts"></a><span data-ttu-id="d27f6-129">المفاهيم</span><span class="sxs-lookup"><span data-stu-id="d27f6-129">Concepts</span></span>
<span data-ttu-id="d27f6-130">تقترن الأدوار والأنشطة ذات الصلة التالية بدورة حياة تكوين التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="d27f6-130">The following roles and related activities are associated with the ER configuration lifecycle.</span></span>

| <span data-ttu-id="d27f6-131">الدور</span><span class="sxs-lookup"><span data-stu-id="d27f6-131">Role</span></span>                                       | <span data-ttu-id="d27f6-132">الأنشطة</span><span class="sxs-lookup"><span data-stu-id="d27f6-132">Activities</span></span>                                                      | <span data-ttu-id="d27f6-133">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="d27f6-133">Description</span></span> |
|--------------------------------------------|-----------------------------------------------------------------|-------------|
| <span data-ttu-id="d27f6-134">مستشار وظيفي لإعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="d27f6-134">Electronic reporting functional consultant</span></span> | <span data-ttu-id="d27f6-135">إنشاء وإدارة مكونات التقارير الإلكترونية (نماذج وتنسيقات).</span><span class="sxs-lookup"><span data-stu-id="d27f6-135">Create and manage ER components (models and formats).</span></span>           | <span data-ttu-id="d27f6-136">رجل أعمال يصمم نماذج بيانات خاصة بمجال التقارير الإلكترونية ويصمم القوالب المطلوبة للمستندات الإلكترونية ويربطها معًا وفقًا لذلك.</span><span class="sxs-lookup"><span data-stu-id="d27f6-136">A business person who designs ER domain–specific data models, designs the required templates for electronic documents, and binds them accordingly.</span></span> |
| <span data-ttu-id="d27f6-137">مطور إعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="d27f6-137">Electronic reporting developer</span></span>             | <span data-ttu-id="d27f6-138">إنشاء وإدارة تعيينات نموذج البيانات.</span><span class="sxs-lookup"><span data-stu-id="d27f6-138">Create and manage data model mappings.</span></span>                          | <span data-ttu-id="d27f6-139">الأخصائي الذي يحدد مصادر بيانات Finance المطلوبة ويربطها بنماذج البيانات الخاصة بمجال التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="d27f6-139">A specialist who selects the required Finance data sources and binds them to ER domain–specific data models.</span></span> |
| <span data-ttu-id="d27f6-140">المشرف على المحاسبة</span><span class="sxs-lookup"><span data-stu-id="d27f6-140">Accounting supervisor</span></span>                      | <span data-ttu-id="d27f6-141">تكوين الإعدادات المتعلقة بالعملية التي تشير إلى نتائج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="d27f6-141">Configure process-related settings that reference ER artifacts.</span></span> | <span data-ttu-id="d27f6-142">على سبيل المثال، دور **المشرف على المحاسبة** الذي يسمح باستخدام إعدادات تكوين التقارير الإلكترونية في طريقة دفع حسابات دائنة معينة لإنشاء رسالة دفع إلكترونية لمعالجة الفواتير.</span><span class="sxs-lookup"><span data-stu-id="d27f6-142">For example, an **Accounting supervisor** role that allows the settings of an ER configuration to be used in a particular Accounts payable payment method to generate an electronic payment message for processing invoices.</span></span> |
| <span data-ttu-id="d27f6-143">موظف مدفوعات الحسابات الدائنة</span><span class="sxs-lookup"><span data-stu-id="d27f6-143">Accounts payable payments clerk</span></span>            | <span data-ttu-id="d27f6-144">استخدام نتائج التقارير الإلكترونية في عملية تجارية معينة:</span><span class="sxs-lookup"><span data-stu-id="d27f6-144">Use ER artifacts in a specific business process.</span></span>                | <span data-ttu-id="d27f6-145">على سبيل المثال، دور **موظف مدفوعات الحسابات الدائنة** الذي يسمح بإنشاء رسائل دفع إلكترونية لمعالجة الفواتير، استنادًا إلى تنسيق التقارير الإلكترونية الذي تم تكوينه لطريقة دفع محددة.</span><span class="sxs-lookup"><span data-stu-id="d27f6-145">For example, an **Accounts payable payments clerk** role that allows electronic payment messages to be generated for processing invoices, based on the ER format that is configured for a specific payment method.</span></span> |

## <a name="er-configuration-development-lifecycle"></a><span data-ttu-id="d27f6-146">دورة حياة تطوير تكوين التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="d27f6-146">ER configuration development lifecycle</span></span>
<span data-ttu-id="d27f6-147">للأسباب التالية المتعلقة بتكوين التقارير الإلكترونية، ننصحك بأن تقوم بتصميم تكوينات التقارير الإلكترونية في بيئة تطوير، كمثيل Finance and Operations منفصل:</span><span class="sxs-lookup"><span data-stu-id="d27f6-147">For the following ER-related reasons, we recommend that you design ER configurations in the development environment, as a separate instance of Finance and Operations:</span></span>

- <span data-ttu-id="d27f6-148">باستطاعة المستخدمين الذين يؤدون دور **مطور إعداد التقارير الإلكتروني** أو **مستشار وظيفي لإعداد التقارير الإلكتروني‬** تحرير التكوينات وتشغيلها لأغراض الاختبار.</span><span class="sxs-lookup"><span data-stu-id="d27f6-148">Users in either the **Electronic reporting developer** role or the **Electronic reporting functional consultant** role can edit configurations and run them for testing purposes.</span></span> <span data-ttu-id="d27f6-149">باستطاعة هذا السيناريو أن يؤدي إلى استدعاءات أساليب الفئات والجداول التي يمكن أن تكون ضارة لبيانات الأعمال وأداء المثيل.</span><span class="sxs-lookup"><span data-stu-id="d27f6-149">This scenario can cause calls of methods of classes and tables that might harm business data and the performance of the instance.</span></span>
- <span data-ttu-id="d27f6-150">لا تتقيد استدعاءات أساليب الفئات والجداول كمصادر بيانات التقارير الإلكترونية لتكوينات التقارير الإلكترونية بنقاط دخول ومحتوى الشركة المسجل.</span><span class="sxs-lookup"><span data-stu-id="d27f6-150">Calls of methods of classes and tables as ER data sources of ER configurations aren't restricted by entry points and logged company content.</span></span> <span data-ttu-id="d27f6-151">وبالتالي، يستطيع المستخدمون الذين يؤدون دور **مطور إعداد التقارير الإلكتروني‬** أو **مستشار وظيفي لإعداد التقارير الإلكتروني‬** الوصول إلى بيانات الأعمال الحساسة.</span><span class="sxs-lookup"><span data-stu-id="d27f6-151">Therefore, users in either the **Electronic reporting developer** role or the **Electronic reporting functional consultant** role can access business-sensitive data.</span></span>

<span data-ttu-id="d27f6-152">يمكن تحميل تكوينات التقارير الإلكترونية التي تم تصميمها في بيئة التطوير إلى بيئة الاختبار لتقييم التكوين (تكامل العملية المناسب وصحة النتائج والأداء) وضمان الجودة مثل صحة حقوق الوصول المدفوعة بالأدوار والفصل بين المهام.</span><span class="sxs-lookup"><span data-stu-id="d27f6-152">ER configurations that are designed in the development environment can be uploaded to the test environment for the configuration evaluation (proper process integration, correctness of results, and performance) and quality assurance, such as correctness of role-driven access rights and segregation of duties.</span></span> <span data-ttu-id="d27f6-153">يمكن استخدام الميزات التي تتيح تبادل تكوين التقارير الإلكترونية لهذا الغرض.</span><span class="sxs-lookup"><span data-stu-id="d27f6-153">The features that enable ER configuration interchange can be used for this purpose.</span></span> <span data-ttu-id="d27f6-154">وأخيراً، يمكن تحميل تكوينات التقارير الإلكترونية مثبتة الكفاءة إلى LCS، حيث يمكن مشاركتها مع المشتركين في الخدمة أو إلى بيئة الإنتاج للاستخدام الداخلي‬‏‫، كما يظهر في التوضيح التالي.‬</span><span class="sxs-lookup"><span data-stu-id="d27f6-154">Finally, proven ER configurations can be uploaded either to LCS, where they can be shared with service subscribers, or to the production environment for internal use, such as shown in the following illustration.</span></span>

![دورة حياة تكوين التقارير الإلكترونية](./media/ger-configuration-lifecycle.png)

## <a name="additional-resources"></a><span data-ttu-id="d27f6-156">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="d27f6-156">Additional resources</span></span>

[<span data-ttu-id="d27f6-157">نظرة عامة حول التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="d27f6-157">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]