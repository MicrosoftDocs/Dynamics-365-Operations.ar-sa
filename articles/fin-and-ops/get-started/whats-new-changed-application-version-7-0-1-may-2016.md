---
title: ما الجديد أو المتغير في الإصدار 7.0.1 من تطبيق Dynamics AX (مايو 2016)
description: تصف هذه المقالة الميزات الجديدة أو المتغيرة في الإصدار 7.0.1 من تطبيق Microsoft Dynamics AX. تم إطلاق هذا الإصدار في مايو 2016 ورقم الإصدار هو 7.0.1265.23014.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.custom: 91213
ms.assetid: f0bbc78f-87fc-40e9-b46a-6655893f69be
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 6bd40873d6890bc837188cba1aa1125d874f6bda
ms.sourcegitcommit: 299e20b59ebefa584ed46a13da3f1a7ff709e43c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2019
ms.locfileid: "1863455"
---
# <a name="whats-new-or-changed-in-dynamics-ax-application-version-701-may-2016"></a><span data-ttu-id="113d0-104">ما الجديد أو المتغير في الإصدار 7.0.1 من تطبيق Dynamics AX (مايو 2016)</span><span class="sxs-lookup"><span data-stu-id="113d0-104">What's new or changed in Dynamics AX application version 7.0.1 (May 2016)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="113d0-105">تصف هذه المقالة الميزات الجديدة أو المتغيرة في الإصدار 7.0.1 من تطبيق Microsoft Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="113d0-105">This article describes features that are either new or changed in Microsoft Dynamics AX application version 7.0.1.</span></span> <span data-ttu-id="113d0-106">تم إطلاق هذا الإصدار في مايو 2016 ورقم الإصدار هو 7.0.1265.23014.</span><span class="sxs-lookup"><span data-stu-id="113d0-106">This version was released in May 2016 and has a build number of 7.0.1265.23014.</span></span>

## <a name="electronic-reporting-er"></a><span data-ttu-id="113d0-107">إعداد التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="113d0-107">Electronic reporting (ER)</span></span>

| <span data-ttu-id="113d0-108">ما الذي يمكنك فعله؟</span><span class="sxs-lookup"><span data-stu-id="113d0-108">What can you do?</span></span> | <span data-ttu-id="113d0-109">لماذا يعتبر هذا الأمر مهمًا؟</span><span class="sxs-lookup"><span data-stu-id="113d0-109">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="113d0-110">تكوين شاشة وقت التشغيل لتصميم التقارير الإلكترونية، لتمكين المستخدمين من تحديد الأبعاد المالية التي يريدونها.</span><span class="sxs-lookup"><span data-stu-id="113d0-110">Configure a run-time dialog box for designing Electronic reporting (ER) reports, so that users can select the financial dimensions that they want.</span></span> | <span data-ttu-id="113d0-111">في وقت التشغيل، في مربع الحوار الخاص بتشغيل تقرير إلكتروني، يستطيع المستخدمون تحديد أبعاد مالية متعددة.</span><span class="sxs-lookup"><span data-stu-id="113d0-111">At run time, in the dialog box for running an ER report, users can select multiple financial dimensions.</span></span> <span data-ttu-id="113d0-112">وستظهر تفاصيل الأبعاد المالية المحددة في المستند الإلكتروني الذي يتم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="113d0-112">The details of the selected financial dimensions will be displayed in the electronic document that is generated.</span></span> |
| <span data-ttu-id="113d0-113">تكوين الوصول إلى أبعاد مالية متعددة أثناء تصميم تقرير إلكتروني، عبر عملية تعيين واحدة إلى مصدر البيانات المطلوب.</span><span class="sxs-lookup"><span data-stu-id="113d0-113">Configure access to multiple financial dimensions during the design of an ER report, via a single mapping to the desired data source.</span></span> | <span data-ttu-id="113d0-114">يمكن استخدام تكوين التقارير الإلكترونية نفسه لإنشاء مستندات إلكترونية تمثل البيانات الخاصة بالحركات‬ إلى جانب تفاصيل الأبعاد المالية، بغض النظر عن عدد الأبعاد المالية التي تم تحديدها من قبل المستخدم أو تكوينها للكيان القانوني أو مثيله الحالي.</span><span class="sxs-lookup"><span data-stu-id="113d0-114">The same ER report configuration can be used to generate electronic documents that present transactional data together with details of financial dimensions, regardless of the number of financial dimensions that are either selected by the user or configured for the current legal entity or instance.</span></span> |
| <span data-ttu-id="113d0-115">تكوين تقرير إلكتروني لإدخال البيانات في أعمدة تم إنشاؤها بشكل حيوي من مستند إلكتروني تم إنشاؤه بتنسيق ورقة العمل OPENXML.</span><span class="sxs-lookup"><span data-stu-id="113d0-115">Configure an ER report to enter data in dynamically generated columns of an electronic document that is created in OPENXML worksheet format.</span></span> | <span data-ttu-id="113d0-116">بإمكان التقرير الإلكتروني إدخال بيانات في ورقة عمل OPENXML تم إنشاؤها، عبر تكرار الأعمدة أفقيًا.</span><span class="sxs-lookup"><span data-stu-id="113d0-116">An ER report can enter data in an OPENXML worksheet that is generated, via horizontally replicating columns.</span></span> <span data-ttu-id="113d0-117">لذلك، يمكن إعادة استخدام تكوين التقارير الإلكترونية نفسه لإنشاء مستندات إلكترونية تحتوي على عدد مختلف من الأعمدة تم إنشاؤها بشكل حيوي.</span><span class="sxs-lookup"><span data-stu-id="113d0-117">Therefore, the same ER report configuration can be reused to generate electronic documents that have a different number of dynamically generated columns.</span></span> |
| <span data-ttu-id="113d0-118">تكوين وجهات التقرير الإلكتروني بحيث يتم توجيه نتيجة مخرجات التنسيق إلى الوجهة المحددة: الملف أو البريد الإلكتروني أو الأرشيف (مجلد Microsoft SharePoint أو Microsoft Azure Storage).</span><span class="sxs-lookup"><span data-stu-id="113d0-118">Configure ER destinations so that the output result of a format is directed to specific destination: file, email, or archive (Microsoft SharePoint folder or Microsoft Azure Storage).</span></span> | <span data-ttu-id="113d0-119">في السابق، كان تشغيل تكوين التقارير الإلكترونية يؤدي إلى ظهور مربع رسالة يطالب المستخدم بحفظ الملف أو فتحه.</span><span class="sxs-lookup"><span data-stu-id="113d0-119">Previously, when you ran an ER configuration, a message box appeared that required user action to save or open a file.</span></span> <span data-ttu-id="113d0-120">يمكنك الآن إجراء تكوين مسبق لوجهة كل تكوين تنسيق لكل واحد من مكونات المخرجات (مجلد أو ملف) بشكل منفصل.</span><span class="sxs-lookup"><span data-stu-id="113d0-120">You can now pre-configure a destination for each format configuration and for each output component (a folder or a file) separately.</span></span> <span data-ttu-id="113d0-121">باستطاعة المستخدمين الذين تتوفر لديهم حقوق الوصول المناسبة تعديل إعدادات الوجهة أيضًا في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="113d0-121">Users who have appropriate access rights can also modify destination settings at run time.</span></span> |

## <a name="pos--microsoft-dynamics-ax-retail"></a><span data-ttu-id="113d0-122">نقطة البيع – Microsoft Dynamics AX Retail</span><span class="sxs-lookup"><span data-stu-id="113d0-122">POS – Microsoft Dynamics AX Retail</span></span>

| <span data-ttu-id="113d0-123">ما الذي يمكنك فعله؟</span><span class="sxs-lookup"><span data-stu-id="113d0-123">What can you do?</span></span> | <span data-ttu-id="113d0-124">لماذا يعتبر هذا الأمر مهمًا؟</span><span class="sxs-lookup"><span data-stu-id="113d0-124">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="113d0-125">استخدام مستعرض Google Chrome.</span><span class="sxs-lookup"><span data-stu-id="113d0-125">Use the Google Chrome browser.</span></span> | <span data-ttu-id="113d0-126">باستطاعة بائعي التجزئة الآن بدء Cloud POS من المستعرض Chrome، ويمكنهم تجربة كافة الوظائف المتوفرة في إصدار Microsoft Edge وInternet Explorer من Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="113d0-126">Retailers can now start Cloud POS from the Chrome browser, and can experience all the functionality that is available in the Microsoft Edge and Internet Explorer version of Cloud POS.</span></span> |

## <a name="financial-reporting"></a><span data-ttu-id="113d0-127">التقارير المالية</span><span class="sxs-lookup"><span data-stu-id="113d0-127">Financial reporting</span></span>

| <span data-ttu-id="113d0-128">ما الذي يمكنك فعله؟</span><span class="sxs-lookup"><span data-stu-id="113d0-128">What can you do?</span></span> | <span data-ttu-id="113d0-129">لماذا يعتبر هذا الأمر مهمًا؟</span><span class="sxs-lookup"><span data-stu-id="113d0-129">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="113d0-130">إعادة إنشاء مجموعة فرعية من بيانات المستودع للتقارير المالية.</span><span class="sxs-lookup"><span data-stu-id="113d0-130">Rebuild the Financial reporting data mart.</span></span> | <span data-ttu-id="113d0-131">عندما تنقل قواعد بيانات Dynamics AX بين بيئات مختلفة أو عندما تجري تغييرات أخرى سريعة الانتشار، قد يلزم إعادة إنشاء قاعدة بيانات التقارير المالية.</span><span class="sxs-lookup"><span data-stu-id="113d0-131">When you move Dynamics AX databases between environments or make other invasive changes to the environment, the Financial reporting database might have to be rebuilt.</span></span> <span data-ttu-id="113d0-132">يتوفر الآن البرنامج النصي Windows PowerShell لإعادة إنشاء قاعدة البيانات نيابة عنك.‬</span><span class="sxs-lookup"><span data-stu-id="113d0-132">A Windows PowerShell script is now provided to rebuild the database for you.</span></span> |
| <span data-ttu-id="113d0-133">لم يعد باستطاعتك الآن تحديد خيارات مصمم التقارير غير الصالحة.</span><span class="sxs-lookup"><span data-stu-id="113d0-133">You can no longer select report designer options that aren't valid.</span></span> | <span data-ttu-id="113d0-134">لا ينطبق الكثير من خيارات مصمم التقارير التي تم استخدامها في الإصدارات المتوفرة في السوق من Management reporter على هذا الإصدار من Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="113d0-134">Several report designer options that were used in the in-market versions of Management reporter don't apply to this version of Dynamics AX.</span></span> <span data-ttu-id="113d0-135">‏‫تتعلق هذه الخيارات بتصميم التقارير المالية ومخرجاتها وارتباطاتها.</span><span class="sxs-lookup"><span data-stu-id="113d0-135">These options were related to financial report design, output, and linking.</span></span> <span data-ttu-id="113d0-136">وقد تمت إزالة هذه الخيارات من مصمم التقارير المالية لمنع حدوث أخطاء من قِبل المستخدم.‬</span><span class="sxs-lookup"><span data-stu-id="113d0-136">These options have been removed from the financial report designer to prevent user errors.</span></span> |

## <a name="financial-management"></a><span data-ttu-id="113d0-137">الإدارة المالية</span><span class="sxs-lookup"><span data-stu-id="113d0-137">Financial management</span></span>

| <span data-ttu-id="113d0-138">ما الذي يمكنك فعله؟</span><span class="sxs-lookup"><span data-stu-id="113d0-138">What can you do?</span></span> | <span data-ttu-id="113d0-139">لماذا يعتبر هذا الأمر مهمًا؟</span><span class="sxs-lookup"><span data-stu-id="113d0-139">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="113d0-140">إنشاء ملفات الدفع الإيجابي لمدفوعات الحسابات الدائنة.</span><span class="sxs-lookup"><span data-stu-id="113d0-140">Generate positive pay files for accounts payable payments.</span></span> | <span data-ttu-id="113d0-141">يمكن إنشاء ملفات الدفع الإيجابي للمساعدة في منع تزوير الشيكات المصرفية.</span><span class="sxs-lookup"><span data-stu-id="113d0-141">Positive pay files can be generated to help prevent check fraud.</span></span> |

## <a name="warehouse-and-production"></a><span data-ttu-id="113d0-142">المستودع والإنتاج</span><span class="sxs-lookup"><span data-stu-id="113d0-142">Warehouse and production</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="113d0-143">ما الذي يمكنك فعله؟</span><span class="sxs-lookup"><span data-stu-id="113d0-143">What can you do?</span></span></th>
<th><span data-ttu-id="113d0-144">لماذا يعتبر هذا الأمر مهمًا؟</span><span class="sxs-lookup"><span data-stu-id="113d0-144">Why is this important?</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="113d0-145">تعريف سياسة عمل المستودع التي تتحكم في إنشاء عمل لمجموعة من المنتجات في مواقع محددة.</span><span class="sxs-lookup"><span data-stu-id="113d0-145">Define a warehouse work policy that controls the creation of work for a set of products at specific locations.</span></span></td>
<td><span data-ttu-id="113d0-146">عمليات المستودع لا تشتمل دائمًا على العمل.</span><span class="sxs-lookup"><span data-stu-id="113d0-146">Warehouse processes don't always include work.</span></span> <span data-ttu-id="113d0-147">باستخدام سياسة عمل المستودع الجديدة، يمكنك منع إنشاء عمل لانتقاء المواد الخام ووضع البضائع المنتهية بعيدًا لمجموعة من المنتجات في مواقع محددة.</span><span class="sxs-lookup"><span data-stu-id="113d0-147">By using the new warehouse work policy, you can prevent work from being created for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="113d0-148">تحديد عدم خضوع موقع مخرجات الإنتاج لمراقبة لوحة ترخيص.</span><span class="sxs-lookup"><span data-stu-id="113d0-148">Specify that a production output location isn't license plate–controlled.</span></span></td>
<td><span data-ttu-id="113d0-149">يمكنك الآن تحديد عدم خضوع موقع مخرجات الإنتاج لمراقبة لوحة ترخيص.</span><span class="sxs-lookup"><span data-stu-id="113d0-149">You can now specify that a product output location isn't license plate–controlled.</span></span> <span data-ttu-id="113d0-150">على سبيل المثال، تعتبر هذه الميزة مفيدة عندما يقوم أمر إنتاج تمهيدي بالإبلاغ عن الأصناف كمنتهية بشكل مباشر إلى موقع يعمل كموقع إدخال إنتاج أمر إنتاج نهائي.</span><span class="sxs-lookup"><span data-stu-id="113d0-150">For example, this feature is useful when an upstream production order reports items as finished directly to a location that acts as production input location for a downstream production order.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="113d0-151">دعم قوائم مكونات الصنف‬ التي تتضمن أصنافًا ذات أبعاد منتجات مختلفة من نفس الصنف.</span><span class="sxs-lookup"><span data-stu-id="113d0-151">Support BOMs that include items with different product dimensions of the same item.</span></span></td>
<td><span data-ttu-id="113d0-152">عند استخدام بُعد واحد أو أبعاد متعددة من المنتج في عملية الإنتاج، قد تجد نفسك في حالات حيث تريد إنتاج أحد الأصناف، استنادًا إلى متغير آخر من الصنف نفسه.</span><span class="sxs-lookup"><span data-stu-id="113d0-152">When using one or multiple of the product dimensions in production, you can have situations where you would like to produce an item, based on a different variant of the same item.</span></span> <span data-ttu-id="113d0-153">لمزيد من المعلومات، راجع <a href="https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/">هذه المدوّنة</a>.</span><span class="sxs-lookup"><span data-stu-id="113d0-153">For more information, see <a href="https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/">this blog</a>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="113d0-154">استبعاد أوامر الإنتاج ذات الهياكل الدائرية عند المستوى الأول من قوائم مكونات الصنف من عملية الحساب على مستوى هذه القوائم من أجل التخطيط للموارد المادية.</span><span class="sxs-lookup"><span data-stu-id="113d0-154">Production orders with circular structures at the first level of their BOMs are excluded from BOM level calculation for material resource planning.</span></span></td>
<td><span data-ttu-id="113d0-155">من غير الممكن تعيين المستويات الصحيحة لقوائم مكونات الصنف إلى متغيرات المنتجات في أوامر الإنتاج التي تتسبب في حدوث التدوير في التدرج الهرمي لقوائم مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="113d0-155">It is not possible to assign correct BOM levels to product variants for production orders that cause circularity in the BOM hierarchy.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="113d0-156">حساب مستويات منفصلة لقوائم مكونات الصنف من أجل التخطيط للموارد المادية وحساب التكلفة:</span><span class="sxs-lookup"><span data-stu-id="113d0-156">Calculate separate BOM levels for material resource planning and cost calculation:</span></span>
<ul>
<li><span data-ttu-id="113d0-157">بالنسبة إلى لتخطيط للموارد المادية، يتم حساب مستويات قوائم مكونات الصنف في جدول <strong>ReqItemLevel</strong> الجديد.</span><span class="sxs-lookup"><span data-stu-id="113d0-157">For material resource planning, BOM levels are calculated in the new <strong>ReqItemLevel</strong> table.</span></span> <span data-ttu-id="113d0-158">ويتم تجاهل أوامر الإنتاج المنتهية في الحساب.</span><span class="sxs-lookup"><span data-stu-id="113d0-158">Ended production orders are ignored in the calculation.</span></span></li>
<li><span data-ttu-id="113d0-159">بالنسبة إلى حساب تكلفة الإنتاج، يتم حساب مستويات قوائم مكونات الصنف في <strong>InventTable</strong>.</span><span class="sxs-lookup"><span data-stu-id="113d0-159">For production cost calculation, BOM levels are calculated in the <strong>InventTable</strong>.</span></span> <span data-ttu-id="113d0-160">ويتم تضمين أوامر الإنتاج المنتهية في الحساب.</span><span class="sxs-lookup"><span data-stu-id="113d0-160">Ended production orders are included in the calculation.</span></span></li>
</ul>
</td>
<td>
<ul>
<li><span data-ttu-id="113d0-161">عند تشغيل التخطيط للموارد المادية، على سبيل المثال، جدولة التخطيط الرئيسي وعملية تحديد إجمالي المكونات المطلوبة‬، يجب أن يتم حساب فقط مستويات قوائم مكونات الصنف المستخدمة لتخطيط الموارد المادية.</span><span class="sxs-lookup"><span data-stu-id="113d0-161">When running material resource planning, for example, master planning plan scheduling and explosion, only BOM levels used for material resource planning need to be recalculated.</span></span> <span data-ttu-id="113d0-162">وبكلمات أخرى، لا حاجة إلى حساب مستويات قوائم مكونات الصنف المستخدمة لحساب تكاليف الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="113d0-162">In other words, there is no need to calculate BOM levels used for production costing calculation.</span></span></li>
<li><span data-ttu-id="113d0-163">عند تشغيل عمليات التكاليف، على سبيل المثال، إقفال المخزون، يجب إعادة حساب فقط مستويات قائمة مكونات الصنف المستخدمة لحساب تكاليف الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="113d0-163">When running costing operations, for example, inventory closing, only BOM levels used for production costing calculation need to be recalculated.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="113d0-164">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="113d0-164">Additional resources</span></span>

[<span data-ttu-id="113d0-165">الجديد أو المتغير</span><span class="sxs-lookup"><span data-stu-id="113d0-165">What's new or changed</span></span>](whats-new-changed.md)

[<span data-ttu-id="113d0-166">دلائل المهام الجديدة أو المحدثة (مايو 2016)</span><span class="sxs-lookup"><span data-stu-id="113d0-166">New or updated task guides (May 2016)</span></span>](new-updated-task-guides-available-may-2016.md)
