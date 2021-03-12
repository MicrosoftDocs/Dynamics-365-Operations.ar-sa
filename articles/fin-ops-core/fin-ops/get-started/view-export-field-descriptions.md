---
title: عرض أوصاف الحقول وتصديرها
description: توضح هذه المقالة كيفية عرض أوصاف الحقول وكيفية استخدام صفحة أوصاف الحقل لتصدير الأوصاف.
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FieldDescriptions
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 11534
ms.assetid: e2795f51-a8a7-4c74-bdb9-b1be93bdd358
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 39dd9a86ffb04d18f61c75fb2c9634e441dc823b
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797886"
---
# <a name="view-and-export-field-descriptions"></a><span data-ttu-id="82b43-103">عرض أوصاف الحقول وتصديرها</span><span class="sxs-lookup"><span data-stu-id="82b43-103">View and export field descriptions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="82b43-104">توضح هذه المقالة كيفية عرض أوصاف الحقول وكيفية استخدام صفحة أوصاف الحقل لتصدير الأوصاف.</span><span class="sxs-lookup"><span data-stu-id="82b43-104">This article describes how to view field descriptions and how to use the Field descriptions page to export descriptions.</span></span>

<span data-ttu-id="82b43-105">يتوفر لبعض الحقول الأكثر تعقيدًا أوصافًا للحقول.</span><span class="sxs-lookup"><span data-stu-id="82b43-105">Some of the more complex fields have field descriptions.</span></span> <span data-ttu-id="82b43-106">وتظهر هذه الأوصاف عند تمرير الماوس فوق حقل.</span><span class="sxs-lookup"><span data-stu-id="82b43-106">These descriptions appear when you hover over a field.</span></span> <span data-ttu-id="82b43-107">يمكنك أيضًا عرض أوصاف الحقول وتصديرها في صفحة **أوصاف الحقول**.</span><span class="sxs-lookup"><span data-stu-id="82b43-107">You can also view and export descriptions on the **Field descriptions** page.</span></span>

<span data-ttu-id="82b43-108">لا تتضمن كل الصفحات أوصاف الحقول.</span><span class="sxs-lookup"><span data-stu-id="82b43-108">Not all pages have field descriptions.</span></span> <span data-ttu-id="82b43-109">إننا نريد فقط توفير أوصاف للحقول الكثيرة التعقيدات، وليس لتلك التي يكون فيها استخدام الحقل واضحًا.</span><span class="sxs-lookup"><span data-stu-id="82b43-109">We want to provide descriptions only for the more complex fields, not where the use of the field is obvious.</span></span> <span data-ttu-id="82b43-110">وبالتالي، هناك بعض الصفحات حيث لا تتوفر أوصاف الحقول، وهناك صفحات أخرى فيها بعض الأوصاف القليلة، بينما تتضمن بعض الصفحات المعقدة الكثير من هذه الأوصاف، ومنها عدد كبير من صفحات المحددات.</span><span class="sxs-lookup"><span data-stu-id="82b43-110">Therefore, some pages don't have any field descriptions, some pages have a few descriptions, and some of the more complex pages, such as many of the parameters pages, have many descriptions.</span></span>

<span data-ttu-id="82b43-111">إذا كان لديك حق الوصول إلى بيئة التطوير، فيمكنك إضافة أوصاف حقول جديدة وتخصيص الأوصاف الموجودة.</span><span class="sxs-lookup"><span data-stu-id="82b43-111">If you have access to the development environment, you can add new field descriptions and customize existing descriptions.</span></span> <span data-ttu-id="82b43-112">على سبيل المثال، يمكنك إضافة معلومات خاصة بالشركة إلى وصف الحقل.</span><span class="sxs-lookup"><span data-stu-id="82b43-112">For example, you can add company-specific information to a field description.</span></span> <span data-ttu-id="82b43-113">لمزيد من المعلومات، راجع [تخصيص أوصاف الحقول](../../dev-itpro/user-interface/customize-field-help.md).</span><span class="sxs-lookup"><span data-stu-id="82b43-113">For more information, see [Customize field descriptions](../../dev-itpro/user-interface/customize-field-help.md).</span></span>

## <a name="see-field-descriptions-in-the-user-interface"></a><span data-ttu-id="82b43-114">الاطلاع على أوصاف الحقول في واجهة المستخدم</span><span class="sxs-lookup"><span data-stu-id="82b43-114">See field descriptions in the user interface</span></span>

<span data-ttu-id="82b43-115">يمكنك عرض أوصاف الحقول عن طريق المرور بالماوس فوق حقل.</span><span class="sxs-lookup"><span data-stu-id="82b43-115">You can view field descriptions by hovering over a field.</span></span> <span data-ttu-id="82b43-116">إذا لم يتوفر أي وصف، فسترى اسم الحقل عند تمرير الماوس فوق الحقل.</span><span class="sxs-lookup"><span data-stu-id="82b43-116">If no description is available, you see the field name when you hover over the field.</span></span>

> [!NOTE]
> <span data-ttu-id="82b43-117">في Dynamics AX 7.0 (فبراير 2016)، يمكن عرض أوصاف الحقول فقط في صفحة **أوصاف الحقول**.</span><span class="sxs-lookup"><span data-stu-id="82b43-117">In Dynamics AX 7.0 (February 2016), field descriptions can be viewed only on the **Field descriptions** page.</span></span>

<span data-ttu-id="82b43-118">يبين الرسم التوضيحي التالي وصف الحقل الذي يظهر عند تمرير الماوس فوق الحقل **تأمين الأصناف أثناء الجرد**.</span><span class="sxs-lookup"><span data-stu-id="82b43-118">The following illustration shows the field description that appears when you hover over the **Lock items during count** field.</span></span>

<span data-ttu-id="82b43-119">[![مثال عن وصف حقل](./media/field-description.png)](./media/field-description.png)</span><span class="sxs-lookup"><span data-stu-id="82b43-119">[![Example of a field description](./media/field-description.png)](./media/field-description.png)</span></span>

## <a name="use-the-field-descriptions-page-to-view-and-export-field-help"></a><span data-ttu-id="82b43-120">استخدام صفحة "أوصاف الحقول" لعرض تعليمات الحقول وتصديرها</span><span class="sxs-lookup"><span data-stu-id="82b43-120">Use the Field descriptions page to view and export field help</span></span>

<span data-ttu-id="82b43-121">تسمح لك صفحة **أوصاف الحقول** بعرض أوصاف الحقول وتصديرها.</span><span class="sxs-lookup"><span data-stu-id="82b43-121">The **Field descriptions** page lets you view and export field descriptions.</span></span> <span data-ttu-id="82b43-122">يمكنك مشاهدة الأوصاف التي تتوفر لصفحة واحدة في مرة واحدة.</span><span class="sxs-lookup"><span data-stu-id="82b43-122">You can see the descriptions that are available for one page at a time.</span></span>

### <a name="view-the-descriptions-for-a-page"></a><span data-ttu-id="82b43-123">عرض الأوصاف لصفحة</span><span class="sxs-lookup"><span data-stu-id="82b43-123">View the descriptions for a page</span></span>

<span data-ttu-id="82b43-124">لعرض أوصاف خاصة بصفحة ما، اتبع هذه الخطوة.</span><span class="sxs-lookup"><span data-stu-id="82b43-124">To view the descriptions for a page, follow this step.</span></span>

- <span data-ttu-id="82b43-125">في الحقل **تحديد صفحة‬**، اكتب اسم الصفحة.</span><span class="sxs-lookup"><span data-stu-id="82b43-125">In the **Select a page** field, type the name of the page.</span></span> <span data-ttu-id="82b43-126">أو، انقر فوق السهم لفتح قائمة بكافة الصفحات، ثم استعرض الصفحة أو قم بتصفيتها.</span><span class="sxs-lookup"><span data-stu-id="82b43-126">Alternatively, click the arrow to open a list of all the pages, and then browse or filter the list.</span></span>

<span data-ttu-id="82b43-127">يمكنك استخدام اسم الصفحة الذي يظهر في واجهة المستخدم، (على سبيل المثال **العملاء**) أو اسم الكود (اسم AOT) الذي يتوفر عندما تنقر بزر الماوس الأيمن على الصفحة، على سبيل المثال, **CustTable**.</span><span class="sxs-lookup"><span data-stu-id="82b43-127">You can use either the name of the page that is shown in the user interface (UI) (for example, **Customers**) or the code name (AOT name) that's available when you right-click a page (for example, **CustTable**).</span></span>

<span data-ttu-id="82b43-128">لمزيد من المعلومات حول الطرق المختلفة لتصفية قائمة الصفحات، راجع القسم "البحث عن صفحة" لاحقًا في هذه المقالة.</span><span class="sxs-lookup"><span data-stu-id="82b43-128">For information about the various ways to filter the list of pages, see the "Searching for a page" section later in this article.</span></span>

<span data-ttu-id="82b43-129">إذا قمت بتعيين الخيار **تضمين الحقول بدون وصف** إلى **نعم**، فستظهر كافة الحقول في الصفحة، بغض النظر عما إذا كان وصف الحقل متوفرًا.</span><span class="sxs-lookup"><span data-stu-id="82b43-129">If you set the **Include fields without a description** option to **Yes**, all the fields on the page are shown, even if they don't have a field description.</span></span>

### <a name="export-the-descriptions-for-a-page"></a><span data-ttu-id="82b43-130">تصدير الأوصاف لصفحة</span><span class="sxs-lookup"><span data-stu-id="82b43-130">Export the descriptions for a page</span></span>

<span data-ttu-id="82b43-131">لتصدير أوصاف خاصة بصفحة ما، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="82b43-131">To export the descriptions for a page, follow these steps.</span></span>

1. <span data-ttu-id="82b43-132">في الحقل **تحديد صفحة**، حدد صفحة.</span><span class="sxs-lookup"><span data-stu-id="82b43-132">In the **Select a page** field, select a page.</span></span>
2. <span data-ttu-id="82b43-133">انقر فوق الزر **فتح في Microsoft Office** في الركن العلوي الأيسر، ثم انقر فوق **FieldDescriptionTmp**.</span><span class="sxs-lookup"><span data-stu-id="82b43-133">Click the **Open in Microsoft Office** button in the upper-right corner, and then click **FieldDescriptionTmp**.</span></span>

### <a name="searching-for-a-page"></a><span data-ttu-id="82b43-134">البحث عن صفحة</span><span class="sxs-lookup"><span data-stu-id="82b43-134">Searching for a page</span></span>

<span data-ttu-id="82b43-135">هناك عدة طرق للبحث عن صفحة في الحقل **تحديد صفحة**.</span><span class="sxs-lookup"><span data-stu-id="82b43-135">There are several ways to search for a page in the **Select a page** field.</span></span> <span data-ttu-id="82b43-136">في الكثير من الحالات، ستحتاج إلى النقر فوق السهم الموجود في الحقل **تحديد صفحة** لفتح القائمة المنسدلة، ثم إجراء التحديد من قائمة الصفحات التي تمت تصفيتها.</span><span class="sxs-lookup"><span data-stu-id="82b43-136">In many cases, you must click the arrow in the **Select a page** field to open the drop-down list, and then select from a filtered list of pages.</span></span>

- <span data-ttu-id="82b43-137">اكتب جزءًا من الاسم، ثم افتح القائمة المنسدلة للتحديد من قائمة الصفحات التي تمت تصفيتها.</span><span class="sxs-lookup"><span data-stu-id="82b43-137">Type part of the name, and then open the drop-down list to select from a filtered list of pages.</span></span>
- <span data-ttu-id="82b43-138">افتح القائمة المنسدلة، ثم انقر فوق العنوان **اسم الصفحة** في أعلى القائمة، أو العنوان **اسم صفحة AOT**.</span><span class="sxs-lookup"><span data-stu-id="82b43-138">Open the drop-down list, and then click either the **Page name** heading at the top of the list or the **Page AOT name** heading.</span></span> <span data-ttu-id="82b43-139">يؤدي هذا إلى ظهور مربع حوار حيث يمكنك استخدام خيارات التصفية المتقدمة، مثل **اسم الصفحة يبدأ بـ**.</span><span class="sxs-lookup"><span data-stu-id="82b43-139">A dialog box appears, where you can use advanced filtering options, such as **Page name begins with**.</span></span>
- <span data-ttu-id="82b43-140">اكتب الاسم الكامل للصفحة.</span><span class="sxs-lookup"><span data-stu-id="82b43-140">Type the full name of the page.</span></span> <span data-ttu-id="82b43-141">عند استخدام هذا الخيار، من الأفضل فتح القائمة المنسدلة ومشاهدة العناصر الأخرى في القائمة، حتى في حالة ظهور أوصاف الحقول.</span><span class="sxs-lookup"><span data-stu-id="82b43-141">When you use this option, it's best to open the drop-down list and see what else is in the list, even if field descriptions are shown.</span></span>

    - <span data-ttu-id="82b43-142">في حال وجود تطابق تام واحد مع الاسم، فستظهر أوصاف الحقول الخاصة بهذه الصفحة.</span><span class="sxs-lookup"><span data-stu-id="82b43-142">If there is a single exact match to the name, the field descriptions for that page are shown.</span></span>
    - <span data-ttu-id="82b43-143">في حال وجود أكثر من تطابق تام، فلن تظهر أي أوصاف.</span><span class="sxs-lookup"><span data-stu-id="82b43-143">If there is more than one exact match, no descriptions are shown.</span></span> <span data-ttu-id="82b43-144">يجب فتح القائمة المنسدلة وتحديد الصفحة التي تريدها.</span><span class="sxs-lookup"><span data-stu-id="82b43-144">You must open the drop-down list and select the page that you want.</span></span>
    - <span data-ttu-id="82b43-145">إذا كان الاسم الذي كتبته جزءًا من اسم صفحة أخرى، فسترى الأوصاف الخاصة بصفحتك.</span><span class="sxs-lookup"><span data-stu-id="82b43-145">If the name that you typed is part of the name of another page, you see the descriptions for your page.</span></span> <span data-ttu-id="82b43-146">ومع ذلك، إذا قمت بفتح القائمة المنسدلة، فسترى صفحات إضافية تحتوي على هذا الاسم.</span><span class="sxs-lookup"><span data-stu-id="82b43-146">However, if you open the drop-down list, you see additional pages that contain that name.</span></span>

<span data-ttu-id="82b43-147">على سبيل المثال، لا تظهر أي أوصاف عندما تكتب **الجرد** في الحقل **تحديد صفحة**.</span><span class="sxs-lookup"><span data-stu-id="82b43-147">For example, no descriptions are shown when you type **Counting** in the **Select a page** field.</span></span> <span data-ttu-id="82b43-148">ستفتح القائمة المنسدلة وسترى صفحتين لهما الاسم نفسه وهو **الجرد** بالإضافة إلى العديد من الصفحات التي تحتوي على الكلمة "الجرد".</span><span class="sxs-lookup"><span data-stu-id="82b43-148">You open the drop-down list, and see that there are two pages that have the name **Counting** and several pages that contain the word "Counting" in the name.</span></span> <span data-ttu-id="82b43-149">إذا حددت الصفحة التي لها اسم AOT وهو **InventJournalCount**، فستظهر أوصاف الحقول الخاصة بهذه الصفحة.</span><span class="sxs-lookup"><span data-stu-id="82b43-149">If you select the page that has the AOT name **InventJournalCount**, the field descriptions are shown for that page.</span></span> <span data-ttu-id="82b43-150">ومع ذلك، إذا فتحت القائمة المنسدلة مرة أخرى، فسترى أن القائمة تتضمن الآن كافة الصفحات التي تحتوي على "InventJournalCount" كجزء من اسم AOT.</span><span class="sxs-lookup"><span data-stu-id="82b43-150">However, if you open the drop-down list again, you will see that the list now contains all pages that have "InventJournalCount" as part of their AOT name.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="82b43-151">استكشاف الأخطاء وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="82b43-151">Troubleshooting</span></span>

<span data-ttu-id="82b43-152">يوفر هذا القسم معلومات لمساعدتك في استكشاف الأخطاء التي قد تواجهك عند استخدام أوصاف الحقول وإصلاح تلك الأخطاء.</span><span class="sxs-lookup"><span data-stu-id="82b43-152">This section provides information to help you troubleshoot issues that you might encounter when you use field descriptions.</span></span>

### <a name="i-cant-find-a-field-description"></a><span data-ttu-id="82b43-153">لا يمكنني العثور على وصف الحقل</span><span class="sxs-lookup"><span data-stu-id="82b43-153">I can't find a field description</span></span>

<span data-ttu-id="82b43-154">نحن نعمل على إضافة أوصاف للحقول الأكثر تعقيدًا.</span><span class="sxs-lookup"><span data-stu-id="82b43-154">We're in the process of adding descriptions for the more complex fields.</span></span> <span data-ttu-id="82b43-155">إذا احتجت إلى مساعدة تتعلق بحقل معين، فالرجاء إعلامنا عن طريق إضافة تعليق على هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="82b43-155">If you require help for a particular field, let us know by adding a comment for this topic.</span></span>

### <a name="the-field-description-isnt-helpful"></a><span data-ttu-id="82b43-156">وصف الحقل غير مساعد.</span><span class="sxs-lookup"><span data-stu-id="82b43-156">The field description isn't helpful</span></span>

<span data-ttu-id="82b43-157">الرجاء إعلامنا برأيك عن طريق إضافة تعليق على هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="82b43-157">Let us know by adding a comment for this topic.</span></span> <span data-ttu-id="82b43-158">وقدّم لنا وصفًا للمعلومات الإضافية التي تحتاج إليها، إذا أمكنك ذلك.</span><span class="sxs-lookup"><span data-stu-id="82b43-158">If you can, describe the additional information that you require.</span></span>

### <a name="i-cant-find-a-field-on-the-field-descriptions-page"></a><span data-ttu-id="82b43-159">يتعذر عليّ العثور على حقل في صفحة أوصاف الحقول</span><span class="sxs-lookup"><span data-stu-id="82b43-159">I can't find a field on the Field descriptions page</span></span>

<span data-ttu-id="82b43-160">لإظهار كافة الحقول في صفحة، عيّن الخيار **تضمين الحقول بدون وصف** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="82b43-160">To show all the fields on a page, set the **Include fields without a description** option to **Yes**.</span></span> <span data-ttu-id="82b43-161">انقر فوق الحقل **تحديد صفحة** للتأكد من أنك حددت الصفحة الصحيحة.</span><span class="sxs-lookup"><span data-stu-id="82b43-161">Click the **Select a page** field to verify that you've selected the correct page.</span></span> <span data-ttu-id="82b43-162">إذا كان الاسم الذي كتبته جزءًا من اسم حقل آخر، فربما حددت الصفحة ذات الاسم الأطول.</span><span class="sxs-lookup"><span data-stu-id="82b43-162">If the name that you typed is part of another field name, you might have selected the page that has the longer name.</span></span>

### <a name="i-cant-find-a-page-on-the-field-descriptions-page"></a><span data-ttu-id="82b43-163">يتعذر عليّ العثور على صفحة في صفحة أوصاف الحقول</span><span class="sxs-lookup"><span data-stu-id="82b43-163">I can't find a page on the Field descriptions page</span></span>

<span data-ttu-id="82b43-164">للحصول على المعلومات حول الطرق المختلفة للعثور على الصفحات، راجع القسم "البحث عن صفحة" لاحقًا في هذه المقالة.</span><span class="sxs-lookup"><span data-stu-id="82b43-164">For information about the various way to find pages, see the "Searching for pages" section earlier in this article.</span></span> <span data-ttu-id="82b43-165">إذا كنت قد كتبت اسم الصفحة بدقة، فقد لا تظهر أوصاف الحقول إذا كان هناك أكثر من صفحة واحدة بنفس الاسم.</span><span class="sxs-lookup"><span data-stu-id="82b43-165">If you've typed the exact name of the page, the field descriptions might not be shown if more than one page has the same name.</span></span> <span data-ttu-id="82b43-166">انقر فوق السهم في الحقل **تحديد صفحة** لفتح قائمة تمت تصفيتها تتضمن الصفحات المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="82b43-166">Click the arrow in the **Select a page** field to open a filtered list of the pages that are available.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="82b43-167">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="82b43-167">Additional resources</span></span>

[<span data-ttu-id="82b43-168">تخصيص أوصاف الحقول</span><span class="sxs-lookup"><span data-stu-id="82b43-168">Customize field descriptions</span></span>](../../dev-itpro/user-interface/customize-field-help.md)
