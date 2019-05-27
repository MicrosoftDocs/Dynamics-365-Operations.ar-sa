---
title: إعادة تصور تقارير المصروفات
description: يوفر هذا الموضوع معلومات حول التجربة المعاد تصميمها وتصورها لإدخال تقرير المصروفات في Microsoft Dynamics 365 for Finance and Operations. تعمل التجربة الجديدة على تبسيط عملية إكمال تقارير المصروفات وتقليل الوقت المطلوب.
author: ryansandness
manager: AnnBe
ms.date: 05/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 3039cda3f2cf9259ca06207bdf941bc6b0fb28e1
ms.sourcegitcommit: be447fc81bc874982bc0185fcb4d87d99bd742c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538670"
---
# <a name="expense-reports-reimagined"></a><span data-ttu-id="1a948-104">إعادة تصور تقارير المصروفات</span><span class="sxs-lookup"><span data-stu-id="1a948-104">Expense reports reimagined</span></span>

[!include[banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="1a948-105">تمت إعادة تصميم إدخال تقرير المصروفات لتبسيط عملية إكمال تقارير المصروفات وتقليل الوقت المطلوب.</span><span class="sxs-lookup"><span data-stu-id="1a948-105">Expense report entry has been redesigned to simplify the process of completing expense reports and decrease the time that is required.</span></span> <span data-ttu-id="1a948-106">فيما يلي المكونات الرئيسية لتجربة المصروفات الجديدة:</span><span class="sxs-lookup"><span data-stu-id="1a948-106">Here are the major components of the new expense experience:</span></span>

- <span data-ttu-id="1a948-107">تسمح لك مساحة عمل "إدارة المصروفات" الجديدة بالوصول إلى مصروفات المفوض.</span><span class="sxs-lookup"><span data-stu-id="1a948-107">A new expense management workspace that lets you access your delegate's expenses.</span></span>
- <span data-ttu-id="1a948-108">تجربة جديدة تتعلق بمطابقة الإيصالات لإظهار الإيصالات على مستوى الرأس بشكل أفضل وتبسيط عملية إرفاق الإيصالات ببنود المصروفات.</span><span class="sxs-lookup"><span data-stu-id="1a948-108">A new receipt matching experience to better show header-level receipts and simplify the process of attaching receipts to expense lines.</span></span>
- <span data-ttu-id="1a948-109">شبكة جديدة للقراءة فقط تسمح لك بعرض العديد من بنود المصروفات وأعمدة البيانات الإضافية.</span><span class="sxs-lookup"><span data-stu-id="1a948-109">A new read-only grid that lets you view many more expense lines and additional columns of data.</span></span> <span data-ttu-id="1a948-110">يمكنك الآن رؤية كافة البنود المفصلة والمقسمة مع مصروفاتها الأصلية.</span><span class="sxs-lookup"><span data-stu-id="1a948-110">You can now see all itemized and split lines, together with their parent expenses.</span></span>
- <span data-ttu-id="1a948-111">جزء مبسط لتحرير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="1a948-111">A simplified pane for editing expenses.</span></span>
- <span data-ttu-id="1a948-112">رسائل معاد تصميها تتعلق بالأخطاء والتحذيرات والسياسات تضمن حصولك على السياق الصحيح لفهم المشكلة وكيفية حلها.</span><span class="sxs-lookup"><span data-stu-id="1a948-112">Redesigned error, warning, and policy messages to help guarantee that you have the correct context to understand what the issue is and how to resolve it.</span></span> <span data-ttu-id="1a948-113">قامت Microsoft بإزالة العديد من الرسائل التي ظهرت قبل أن يحصل المستخدمون على فرصة لإكمال مهامهم ومعالجة المشكلات، مثل رسالة التفصيل غير المكتملة.</span><span class="sxs-lookup"><span data-stu-id="1a948-113">Microsoft has removed many messages that appeared before users had an opportunity to complete their tasks and address the issues, such as the incomplete itemization message.</span></span>
- <span data-ttu-id="1a948-114">صفحة جديدة لتحديد الحقول المطلوبة من قبل مؤسستك، والحقول الاختيارية والحقول التي لا يجب التقاطها.</span><span class="sxs-lookup"><span data-stu-id="1a948-114">A new page for specifying which fields are required by your organization, which fields are optional, and which fields should not be captured.</span></span> <span data-ttu-id="1a948-115">ستساعد هذه الصفحة على تقليل عدد الحقول التي يجب تعيينها من قبل المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="1a948-115">This page will help reduce the number of fields that users must to set.</span></span>
- <span data-ttu-id="1a948-116">شكل وأسلوب عرض جديد لتقارير المصروفات، حتى لا تبدو التقارير وكأنها مصممة للأشخاص المعنيين بالحسابات.</span><span class="sxs-lookup"><span data-stu-id="1a948-116">A new look and feel for expense reports, so that the reports no longer seem as though they were designed for accounting personas.</span></span>

<span data-ttu-id="1a948-117">لتشغيل التجربة الجديدة، استخدم مساحة عمل **إدارة الميزات** لتشغيل ميزة **إعادة تصور تقارير المصروفات‬**.</span><span class="sxs-lookup"><span data-stu-id="1a948-117">To turn on the new experience, use the **Feature management** workspace to turn on the **Expense reports re-imagined** feature.</span></span> <span data-ttu-id="1a948-118">عند تشغيل هذه الميزة، تحدث الإجراءات التالية:</span><span class="sxs-lookup"><span data-stu-id="1a948-118">When you turn on this feature, the following actions occur:</span></span>

- <span data-ttu-id="1a948-119">يتم استبدال مساحة عمل المصروفات الموجودة بمساحة العمل الجديدة.</span><span class="sxs-lookup"><span data-stu-id="1a948-119">The existing expense workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="1a948-120">يُضاف عنصر قائمة جديد لرؤية حقل المصروفات.</span><span class="sxs-lookup"><span data-stu-id="1a948-120">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="1a948-121">لا تتم إزالة أي عناصر قائمة موجودة لتقارير المصروفات (الصفحة الموجودة) أو حقول تقرير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="1a948-121">No existing menu items for expense reports (the existing page) or expense report fields are removed.</span></span>
- <span data-ttu-id="1a948-122">ما زالت عمليات سير العمل والموافقات تنقلك إلى صفحة تقارير المصروفات الموجودة.</span><span class="sxs-lookup"><span data-stu-id="1a948-122">Workflows and any approvals still take you to the existing expense reports page.</span></span>

## <a name="getting-started-video-for-new-users"></a><span data-ttu-id="1a948-123">فيديو الشروع في العمل للمستخدمين الجدد</span><span class="sxs-lookup"><span data-stu-id="1a948-123">Getting started video for new users</span></span>

<span data-ttu-id="1a948-124">يمكنك مشاهدة فيديو قصير يعرض الميزات الرئيسية لإدخال المصروفات.</span><span class="sxs-lookup"><span data-stu-id="1a948-124">You can watch a short video that shows the main features of expense entry.</span></span>

> [!NOTE]
> <span data-ttu-id="1a948-125">الفيديو غير متوفر بعد.</span><span class="sxs-lookup"><span data-stu-id="1a948-125">The video isn't available yet.</span></span> <span data-ttu-id="1a948-126">سيتم تحديث هذا الموضوع عندما يصبح الفيديو متوفرًا.</span><span class="sxs-lookup"><span data-stu-id="1a948-126">This topic will be updated when the video is available.</span></span>

## <a name="new-features"></a><span data-ttu-id="1a948-127">الميزات الجديدة</span><span class="sxs-lookup"><span data-stu-id="1a948-127">New features</span></span>

| <span data-ttu-id="1a948-128">الميزة الجديدة</span><span class="sxs-lookup"><span data-stu-id="1a948-128">New feature</span></span> | <span data-ttu-id="1a948-129">الوصف</span><span class="sxs-lookup"><span data-stu-id="1a948-129">Description</span></span> |
|---|----|
| <span data-ttu-id="1a948-130">رؤية حقل المصروفات</span><span class="sxs-lookup"><span data-stu-id="1a948-130">Expense field visibility</span></span> | <span data-ttu-id="1a948-131">تتيح لك صفحة الإعداد الجديدة بتحديد الحقول التي يجب تعطيلها للمؤسسة والحقول المطلوبة والحقول الموصي بها.</span><span class="sxs-lookup"><span data-stu-id="1a948-131">A new setup page lets you specify which fields should be disabled for an organization, which fields should be required, and which fields are recommended.</span></span> |
| <span data-ttu-id="1a948-132">الحقول المطلوبة</span><span class="sxs-lookup"><span data-stu-id="1a948-132">Required fields</span></span> | <span data-ttu-id="1a948-133">يتيح لك التكوين البسيط الجديد بجعل بعض الحقول مطلوبة دون الحاجة إلى استخدام اطار عمل السياسة.</span><span class="sxs-lookup"><span data-stu-id="1a948-133">New simple configuration lets you make some fields required without having to use the policy framework.</span></span> |
| <span data-ttu-id="1a948-134">حقول اختيارية</span><span class="sxs-lookup"><span data-stu-id="1a948-134">Optional fields</span></span> | <span data-ttu-id="1a948-135">تمت إضافة صفحة ثانية للحقول الاختيارية.</span><span class="sxs-lookup"><span data-stu-id="1a948-135">A second page for optional fields is added.</span></span> <span data-ttu-id="1a948-136">وبهذه الطريقة، لن يشعر الموظفون بأنه يتعين عليهم تعيين الحقول، ولكن الوصول إلى الحقول ما زال سهلاً.</span><span class="sxs-lookup"><span data-stu-id="1a948-136">In this way, employees won't feel as if they must set the fields, but the fields are still easily accessible.</span></span> |
| <span data-ttu-id="1a948-137">إضافة الإيصالات غير المرفقة</span><span class="sxs-lookup"><span data-stu-id="1a948-137">Add unattached receipts</span></span> | <span data-ttu-id="1a948-138">القدرة على إضافة إيصالات غير مرفقة إلى تقرير المصروفات مرئية بشكل أفضل من مساحة العمل وفي تقرير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="1a948-138">The ability to add unattached receipts to expense report is more visible from the workspace and on the expense report.</span></span> |
| <span data-ttu-id="1a948-139">مراسلة محسنة</span><span class="sxs-lookup"><span data-stu-id="1a948-139">Improved messaging</span></span> | <span data-ttu-id="1a948-140">هناك رؤية أفضل لبنود المصروفات التي تتضمن تحذيرات أو أخطاء.</span><span class="sxs-lookup"><span data-stu-id="1a948-140">There is better visibility into expense lines that have warnings or errors.</span></span> |
| <span data-ttu-id="1a948-141">تقليل عدد الرسائل في شريط الرسائل</span><span class="sxs-lookup"><span data-stu-id="1a948-141">Reduction in messages in the message bar</span></span>| <span data-ttu-id="1a948-142">تم تقليل عدد رسائل سجل المعلومات، وتم بذل جهود لمنع الرسائل المكررة من الظهور في العديد من الحالات.</span><span class="sxs-lookup"><span data-stu-id="1a948-142">The number of Infolog messages was decreased, and an effort was made to prevent duplicate messages from appearing in many cases.</span></span> |
| <span data-ttu-id="1a948-143">إجراءات عامة مجمعة معًا</span><span class="sxs-lookup"><span data-stu-id="1a948-143">Grouped together common actions</span></span> | <span data-ttu-id="1a948-144">تم تنظيف الواجهة من خلال إضافة زر إجراءات جديد لمعظم الإجراءات العامة على مستوى البنود وإضافة زر علامة القطع (...) إلى الرأس وغيرها من الإجراءات الأخرى التي لا تتكرر كثيرًا.</span><span class="sxs-lookup"><span data-stu-id="1a948-144">The interface was cleaned up with the addition of a new actions button for most of the common line-level actions and the addition of an ellipsis button (...) for header and other less frequent actions.</span></span> |
| <span data-ttu-id="1a948-145">مساحة عمل جديدة لزيادة الرؤية</span><span class="sxs-lookup"><span data-stu-id="1a948-145">New workspace to increase visibility</span></span> | <span data-ttu-id="1a948-146">توحد مساحة العمل الجديدة الميزات والارتباطات التي تتيح للمستخدمين الانتقال إلى مناطق مختلفة.</span><span class="sxs-lookup"><span data-stu-id="1a948-146">A new workspace unifies features and links that let users move to different areas.</span></span> |
| <span data-ttu-id="1a948-147">إضافة المصروفات والإيصالات الموجودة اثناء إنشاء تقرير المصروفات</span><span class="sxs-lookup"><span data-stu-id="1a948-147">Add existing expenses and receipts during expense creation</span></span> | <span data-ttu-id="1a948-148">عند إنشاء تقارير المصروفات، يمكنك إضافة كافة المصروفات والإيصالات أو مصروفات وإيصالات محددة.</span><span class="sxs-lookup"><span data-stu-id="1a948-148">When you create expense reports, you can add all or selected expenses and receipts.</span></span> |
| <span data-ttu-id="1a948-149">حاسبة سعر الصرف</span><span class="sxs-lookup"><span data-stu-id="1a948-149">Exchange rate calculator</span></span> | <span data-ttu-id="1a948-150">تمت إضافة حاسبة سعر الصرف التي تتيح لك حساب سعر الصرف لحركات ضرورية متعددة العملات.</span><span class="sxs-lookup"><span data-stu-id="1a948-150">An exchange rate calculator is added that lets you calculate the exchange rate for out-of-pocket multicurrency transactions.</span></span> |
| <span data-ttu-id="1a948-151">حفظ بنود مصروفات جديده وإضافتها</span><span class="sxs-lookup"><span data-stu-id="1a948-151">Save and add new expense lines</span></span> | <span data-ttu-id="1a948-152">يتوفر الزران **حفظ** و**جديد** عند إدخال مصروفات جديدة لمساعدتك على إدخال بنود المصروفات بسرعة.</span><span class="sxs-lookup"><span data-stu-id="1a948-152">**Save** and **New** buttons are available when new expenses are entered, to help you quickly enter expense lines.</span></span> |
| <span data-ttu-id="1a948-153">رؤية أفضل للبنود المقسمة والمفصلة</span><span class="sxs-lookup"><span data-stu-id="1a948-153">Better visibility into split and itemized lines</span></span> | <span data-ttu-id="1a948-154">تُضاف البنود المفصلة والمقسمة مباشرةً إلى قائمة المصروفات لزيادة الرؤية ومساعدتك على تحديد ما إذا كان هناك أخطاء في السياسة أو أخطاء أخرى.</span><span class="sxs-lookup"><span data-stu-id="1a948-154">Itemized and split lines are added directly to the list of expenses, to increase visibility and help you easily determine whether there are policy errors or other errors.</span></span> |
| <span data-ttu-id="1a948-155">إظهار الإيصالات اثناء التفصيل</span><span class="sxs-lookup"><span data-stu-id="1a948-155">Show receipts during itemization</span></span> | <span data-ttu-id="1a948-156">يمكن إظهار الإيصالات اثناء التفصيل.</span><span class="sxs-lookup"><span data-stu-id="1a948-156">Receipts can be shown during itemization.</span></span> |

<span data-ttu-id="1a948-157">يركز الإصدار الأولي على سيناريوهات إدخال المصروفات.</span><span class="sxs-lookup"><span data-stu-id="1a948-157">The initial release is focused on expense entry scenarios.</span></span> <span data-ttu-id="1a948-158">وسيواصل سيناريو مراجعة تقرير المصروفات أو الموافقة عليه استخدام الصفحة الموجودة لإدخال المصروفات.</span><span class="sxs-lookup"><span data-stu-id="1a948-158">Any expense report review or approval scenario will continue to use the existing expense entry page.</span></span>

<span data-ttu-id="1a948-159">الميزات التالية موجودة في الصفحة الموجودة ولكنها غير موجودة بعد في الصفحة الجديدة.</span><span class="sxs-lookup"><span data-stu-id="1a948-159">The following features are present on the existing page but aren't yet present on the new page.</span></span> <span data-ttu-id="1a948-160">وسيُعاد تقديم هذه الميزات عبر الإصدارات المتعددة التالية:</span><span class="sxs-lookup"><span data-stu-id="1a948-160">These features will be reintroduced over the next several releases:</span></span>

- <span data-ttu-id="1a948-161">الموافقات</span><span class="sxs-lookup"><span data-stu-id="1a948-161">Approvals</span></span>
- <span data-ttu-id="1a948-162">الموافقات على الحسابات الدائنة والقدرة على تحرير المحاسبة</span><span class="sxs-lookup"><span data-stu-id="1a948-162">Accounts payable approvals and the ability to edit the accounting</span></span>
- <span data-ttu-id="1a948-163">نقاط إدخال متعددة</span><span class="sxs-lookup"><span data-stu-id="1a948-163">Multiple entry points</span></span>
- <span data-ttu-id="1a948-164">تكامل طلب السفر‬</span><span class="sxs-lookup"><span data-stu-id="1a948-164">Travel requisition integration</span></span>
- <span data-ttu-id="1a948-165">كيان بيانات لرؤية حقل المصروفات</span><span class="sxs-lookup"><span data-stu-id="1a948-165">Data entity for expense field visibility</span></span>
- <span data-ttu-id="1a948-166">إدخال المصروفات اليومية</span><span class="sxs-lookup"><span data-stu-id="1a948-166">Entry for per-diem expenses</span></span>
- <span data-ttu-id="1a948-167">سير العمل على مستوى البند</span><span class="sxs-lookup"><span data-stu-id="1a948-167">Line-level workflow</span></span>
- <span data-ttu-id="1a948-168">دعم المعتمد المؤقت</span><span class="sxs-lookup"><span data-stu-id="1a948-168">Interim approver support</span></span>
- <span data-ttu-id="1a948-169">تفصيل متقدم</span><span class="sxs-lookup"><span data-stu-id="1a948-169">Advanced itemization</span></span>
