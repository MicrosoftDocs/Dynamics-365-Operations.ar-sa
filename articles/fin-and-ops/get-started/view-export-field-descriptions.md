---
title: "عرض أوصاف الحقول وتصديرها"
description: "توضح هذه المقالة كيفية عرض أوصاف الحقول وكيفية استخدام صفحة أوصاف الحقل لتصدير الأوصاف."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: FieldDescriptions
audience: Application User, Developer, IT Pro
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 11534
ms.assetid: e2795f51-a8a7-4c74-bdb9-b1be93bdd358
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6426f208a51ffbf72c6faa8cb281aba2984052d7
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="view-and-export-field-descriptions"></a><span data-ttu-id="49aac-103">عرض أوصاف الحقول وتصديرها</span><span class="sxs-lookup"><span data-stu-id="49aac-103">View and export field descriptions</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="49aac-104">توضح هذه المقالة كيفية عرض أوصاف الحقول وكيفية استخدام صفحة أوصاف الحقل لتصدير الأوصاف.</span><span class="sxs-lookup"><span data-stu-id="49aac-104">This article describes how to view field descriptions and how to use the Field descriptions page to export descriptions.</span></span>

<span data-ttu-id="49aac-105">يتضمن Microsoft Dynamics 365 for Finance and Operations أوصافًا لبعض الحقول الأكثر تعقيدًا.</span><span class="sxs-lookup"><span data-stu-id="49aac-105">Microsoft Dynamics 365 for Finance and Operations has descriptions for some of the more complex fields.</span></span> <span data-ttu-id="49aac-106">وتظهر هذه الأوصاف عند تمرير الماوس فوق حقل.</span><span class="sxs-lookup"><span data-stu-id="49aac-106">These descriptions appear when you hover over a field.</span></span> <span data-ttu-id="49aac-107">يمكنك أيضًا عرض أوصاف الحقول وتصديرها في صفحة **أوصاف الحقول**.</span><span class="sxs-lookup"><span data-stu-id="49aac-107">You can also view and export descriptions on the **Field descriptions** page.</span></span> 

<span data-ttu-id="49aac-108">لا تتضمن كل الصفحات أوصاف الحقول.</span><span class="sxs-lookup"><span data-stu-id="49aac-108">Not all pages have field descriptions.</span></span> <span data-ttu-id="49aac-109">إننا نريد فقط توفير أوصاف للحقول الكثيرة التعقيدات، وليس لتلك التي يكون فيها استخدام الحقل واضحًا.</span><span class="sxs-lookup"><span data-stu-id="49aac-109">We want to provide descriptions only for the more complex fields, not where the use of the field is obvious.</span></span> <span data-ttu-id="49aac-110">وبالتالي، هناك بعض الصفحات حيث لا تتوفر أوصاف الحقول، وهناك صفحات أخرى فيها بعض الأوصاف القليلة، بينما تتضمن بعض الصفحات المعقدة الكثير من هذه الأوصاف، ومنها عدد كبير من صفحات المحددات.</span><span class="sxs-lookup"><span data-stu-id="49aac-110">Therefore, some pages don't have any field descriptions, some pages have a few descriptions, and some of the more complex pages, such as many of the parameters pages, have many descriptions.</span></span> 

<span data-ttu-id="49aac-111">إذا كان لديك حق الوصول إلى بيئة التطوير في Finance and Operations، فيمكنك إضافة أوصاف حقول جديدة وتخصيص الأوصاف الموجودة.</span><span class="sxs-lookup"><span data-stu-id="49aac-111">If you have access to the Finance and Operations development environment, you can add new field descriptions and customize existing descriptions.</span></span> <span data-ttu-id="49aac-112">على سبيل المثال، يمكنك إضافة معلومات خاصة بالشركة إلى وصف الحقل.</span><span class="sxs-lookup"><span data-stu-id="49aac-112">For example, you can add company-specific information to a field description.</span></span> <span data-ttu-id="49aac-113">لمزيد من المعلومات، راجع [تعليمات تخصيص الحقل](../../dev-itpro/user-interface/customize-field-help.md).</span><span class="sxs-lookup"><span data-stu-id="49aac-113">For more information, see [Customize field help](../../dev-itpro/user-interface/customize-field-help.md).</span></span>

## <a name="see-field-descriptions-in-the-user-interface"></a><span data-ttu-id="49aac-114">الاطلاع على أوصاف الحقول في واجهة المستخدم</span><span class="sxs-lookup"><span data-stu-id="49aac-114">See field descriptions in the user interface</span></span>
<span data-ttu-id="49aac-115">يمكنك عرض أوصاف الحقول عن طريق المرور بالماوس فوق حقل.</span><span class="sxs-lookup"><span data-stu-id="49aac-115">You can view field descriptions by hovering over a field.</span></span> <span data-ttu-id="49aac-116">إذا لم يتوفر أي وصف، فسترى اسم الحقل عند تمرير الماوس فوق الحقل.</span><span class="sxs-lookup"><span data-stu-id="49aac-116">If no description is available, you see the field name when you hover over the field.</span></span> <span data-ttu-id="49aac-117">(ملاحظة: في Dynamics AX 7.0 (فبراير 2016)، يمكن عرض أوصاف الحقول فقط في صفحة **أوصاف الحقول**.) ‏‫يبين الرسم التوضيحي التالي وصف الحقل الذي يظهر عند تمرير الماوس فوق الحقل **تأمين الأصناف أثناء الجرد**.</span><span class="sxs-lookup"><span data-stu-id="49aac-117">(Note: In Dynamics AX 7.0 (February 2016), field descriptions can be viewed only on the **Field descriptions** page.) The following illustration shows the field description that appears when you hover over the **Lock items during count** field.</span></span> 

<span data-ttu-id="49aac-118">[![مثال عن وصف حقل](./media/field-description.png)](./media/field-description.png)</span><span class="sxs-lookup"><span data-stu-id="49aac-118">[![Example of a field description](./media/field-description.png)](./media/field-description.png)</span></span>

## <a name="use-the-field-descriptions-page-to-view-and-export-field-help"></a><span data-ttu-id="49aac-119">استخدام صفحة "أوصاف الحقول" لعرض تعليمات الحقول وتصديرها</span><span class="sxs-lookup"><span data-stu-id="49aac-119">Use the Field descriptions page to view and export field help</span></span>
<span data-ttu-id="49aac-120">تسمح لك صفحة **أوصاف الحقول** بعرض أوصاف الحقول وتصديرها.</span><span class="sxs-lookup"><span data-stu-id="49aac-120">The **Field descriptions** page lets you view and export field descriptions.</span></span> <span data-ttu-id="49aac-121">يمكنك مشاهدة الأوصاف التي تتوفر لصفحة واحدة في مرة واحدة.</span><span class="sxs-lookup"><span data-stu-id="49aac-121">You can see the descriptions that are available for one page at a time.</span></span>

### <a name="view-the-descriptions-for-a-page"></a><span data-ttu-id="49aac-122">عرض الأوصاف لصفحة</span><span class="sxs-lookup"><span data-stu-id="49aac-122">View the descriptions for a page</span></span>

<span data-ttu-id="49aac-123">لعرض أوصاف خاصة بصفحة ما، اتبع هذه الخطوة.</span><span class="sxs-lookup"><span data-stu-id="49aac-123">To view the descriptions for a page, follow this step.</span></span>

-   <span data-ttu-id="49aac-124">في الحقل **تحديد صفحة‬**، اكتب اسم الصفحة.</span><span class="sxs-lookup"><span data-stu-id="49aac-124">In the **Select a page** field, type the name of the page.</span></span> <span data-ttu-id="49aac-125">أو، انقر فوق السهم لفتح قائمة بكافة الصفحات، ثم استعرض الصفحة أو قم بتصفيتها.</span><span class="sxs-lookup"><span data-stu-id="49aac-125">Alternatively, click the arrow to open a list of all the pages, and then browse or filter the list.</span></span>

<span data-ttu-id="49aac-126">يمكنك استخدام اسم الصفحة الذي يظهر في واجهة المستخدم، (على سبيل المثال **العملاء**) أو اسم الكود (اسم AOT) الذي يتوفر عندما تنقر بزر الماوس الأيمن على الصفحة، على سبيل المثال, **CustTable**).</span><span class="sxs-lookup"><span data-stu-id="49aac-126">You can use either the name of the page that is shown in the user interface (UI) (for example, **Customers**) or the code name (AOT name) that's available when you right-click a page (for example, **CustTable**).</span></span> 

<span data-ttu-id="49aac-127">لمزيد من المعلومات حول الطرق المختلفة لتصفية قائمة الصفحات، راجع القسم "البحث عن صفحة" لاحقًا في هذه المقالة.</span><span class="sxs-lookup"><span data-stu-id="49aac-127">For information about the various ways to filter the list of pages, see the "Searching for a page" section later in this article.</span></span> 

<span data-ttu-id="49aac-128">إذا قمت بتعيين الخيار **تضمين الحقول بدون وصف** إلى **نعم**، فستظهر كافة الحقول في الصفحة، بغض النظر عما إذا كان وصف الحقل متوفرًا.</span><span class="sxs-lookup"><span data-stu-id="49aac-128">If you set the **Include fields without a description** option to **Yes**, all the fields on the page are shown, even if they don't have a field description.</span></span>

### <a name="export-the-descriptions-for-a-page"></a><span data-ttu-id="49aac-129">تصدير الأوصاف لصفحة</span><span class="sxs-lookup"><span data-stu-id="49aac-129">Export the descriptions for a page</span></span>

<span data-ttu-id="49aac-130">لتصدير أوصاف خاصة بصفحة ما، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="49aac-130">To export the descriptions for a page, follow these steps.</span></span>

1.  <span data-ttu-id="49aac-131">في الحقل **تحديد صفحة**، حدد صفحة.</span><span class="sxs-lookup"><span data-stu-id="49aac-131">In the **Select a page** field, select a page.</span></span>
2.  <span data-ttu-id="49aac-132">انقر فوق الزر **فتح في Microsoft Office** في الركن العلوي الأيسر، ثم انقر فوق **FieldDescriptionTmp**.</span><span class="sxs-lookup"><span data-stu-id="49aac-132">Click the **Open in Microsoft Office** button in the upper-right corner, and then click **FieldDescriptionTmp**.</span></span>

### <a name="searching-for-a-page"></a><span data-ttu-id="49aac-133">البحث عن صفحة</span><span class="sxs-lookup"><span data-stu-id="49aac-133">Searching for a page</span></span>

<span data-ttu-id="49aac-134">هناك عدة طرق للبحث عن صفحة في الحقل **تحديد صفحة**.</span><span class="sxs-lookup"><span data-stu-id="49aac-134">There are several ways to search for a page in the **Select a page** field.</span></span> <span data-ttu-id="49aac-135">في الكثير من الحالات، ستحتاج إلى النقر فوق السهم الموجود في الحقل **تحديد صفحة** لفتح القائمة المنسدلة، ثم إجراء التحديد من قائمة الصفحات التي تمت تصفيتها.</span><span class="sxs-lookup"><span data-stu-id="49aac-135">In many cases, you must click the arrow in the **Select a page** field to open the drop-down list, and then select from a filtered list of pages.</span></span>

-   <span data-ttu-id="49aac-136">اكتب جزءًا من الاسم، ثم افتح القائمة المنسدلة للتحديد من قائمة الصفحات التي تمت تصفيتها.</span><span class="sxs-lookup"><span data-stu-id="49aac-136">Type part of the name, and then open the drop-down list to select from a filtered list of pages.</span></span>
-   <span data-ttu-id="49aac-137">افتح القائمة المنسدلة، ثم انقر فوق العنوان **اسم الصفحة** في أعلى القائمة، أو العنوان **اسم صفحة AOT**.</span><span class="sxs-lookup"><span data-stu-id="49aac-137">Open the drop-down list, and then click either the **Page name** heading at the top of the list or the **Page AOT name** heading.</span></span> <span data-ttu-id="49aac-138">يؤدي هذا إلى ظهور مربع حوار حيث يمكنك استخدام خيارات التصفية المتقدمة، مثل **اسم الصفحة يبدأ بـ**.</span><span class="sxs-lookup"><span data-stu-id="49aac-138">A dialog box appears, where you can use advanced filtering options, such as **Page name begins with**.</span></span>
-   <span data-ttu-id="49aac-139">اكتب الاسم الكامل للصفحة.</span><span class="sxs-lookup"><span data-stu-id="49aac-139">Type the full name of the page.</span></span> <span data-ttu-id="49aac-140">عند استخدام هذا الخيار، من الأفضل فتح القائمة المنسدلة ومشاهدة العناصر الأخرى في القائمة، حتى في حالة ظهور أوصاف الحقول.</span><span class="sxs-lookup"><span data-stu-id="49aac-140">When you use this option, it's best to open the drop-down list and see what else is in the list, even if field descriptions are shown.</span></span>
    -   <span data-ttu-id="49aac-141">في حال وجود تطابق تام واحد مع الاسم، فستظهر أوصاف الحقول الخاصة بهذه الصفحة.</span><span class="sxs-lookup"><span data-stu-id="49aac-141">If there is a single exact match to the name, the field descriptions for that page are shown.</span></span>
    -   <span data-ttu-id="49aac-142">في حال وجود أكثر من تطابق تام، فلن تظهر أي أوصاف.</span><span class="sxs-lookup"><span data-stu-id="49aac-142">If there is more than one exact match, no descriptions are shown.</span></span> <span data-ttu-id="49aac-143">يجب فتح القائمة المنسدلة وتحديد الصفحة التي تريدها.</span><span class="sxs-lookup"><span data-stu-id="49aac-143">You must open the drop-down list and select the page that you want.</span></span>
    -   <span data-ttu-id="49aac-144">إذا كان الاسم الذي كتبته جزءًا من اسم صفحة أخرى، فسترى الأوصاف الخاصة بصفحتك.</span><span class="sxs-lookup"><span data-stu-id="49aac-144">If the name that you typed is part of the name of another page, you see the descriptions for your page.</span></span> <span data-ttu-id="49aac-145">ومع ذلك، إذا قمت بفتح القائمة المنسدلة، فسترى صفحات إضافية تحتوي على هذا الاسم.</span><span class="sxs-lookup"><span data-stu-id="49aac-145">However, if you open the drop-down list, you see additional pages that contain that name.</span></span>

<span data-ttu-id="49aac-146">على سبيل المثال، لا تظهر أي أوصاف عندما تكتب **الجرد** في الحقل ****تحديد صفحة****.</span><span class="sxs-lookup"><span data-stu-id="49aac-146">For example, no descriptions are shown when you type **Counting** in the ****Select a page**** field.</span></span> <span data-ttu-id="49aac-147">ستفتح القائمة المنسدلة وسترى صفحتين لهما الاسم نفسه وهو **الجرد** بالإضافة إلى العديد من الصفحات التي تحتوي على الكلمة "الجرد".</span><span class="sxs-lookup"><span data-stu-id="49aac-147">You open the drop-down list, and see that there are two pages that have the name **Counting** and several pages that contain the word "Counting" in the name.</span></span> <span data-ttu-id="49aac-148">إذا حددت الصفحة التي لها اسم AOT وهو **InventJournalCount**، فستظهر أوصاف الحقول الخاصة بهذه الصفحة.</span><span class="sxs-lookup"><span data-stu-id="49aac-148">If you select the page that has the AOT name **InventJournalCount**, the field descriptions are shown for that page.</span></span> <span data-ttu-id="49aac-149">ومع ذلك، إذا فتحت القائمة المنسدلة مرة أخرى، فسترى أن القائمة تتضمن الآن كافة الصفحات التي تحتوي على "InventJournalCount" كجزء من اسم AOT.</span><span class="sxs-lookup"><span data-stu-id="49aac-149">However, if you open the drop-down list again, you will see that the list now contains all pages that have "InventJournalCount" as part of their AOT name.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="49aac-150">استكشاف الأخطاء وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="49aac-150">Troubleshooting</span></span>
<span data-ttu-id="49aac-151">يوفر هذا القسم معلومات لمساعدتك في استكشاف الأخطاء التي قد تواجهك عند استخدام أوصاف الحقول وإصلاح تلك الأخطاء.</span><span class="sxs-lookup"><span data-stu-id="49aac-151">This section provides information to help you troubleshoot issues that you might encounter when you use field descriptions.</span></span>

### <a name="i-cant-find-a-field-description"></a><span data-ttu-id="49aac-152">لا يمكنني العثور على وصف الحقل</span><span class="sxs-lookup"><span data-stu-id="49aac-152">I can't find a field description</span></span>

<span data-ttu-id="49aac-153">نحن نعمل على إضافة أوصاف للحقول الأكثر تعقيدً.</span><span class="sxs-lookup"><span data-stu-id="49aac-153">We’re in the process of adding descriptions for the more complex fields.</span></span> <span data-ttu-id="49aac-154">إذا احتجت إلى مساعدة تتعلق بحقل معين، فالرجاء إعلامنا عن طريق إضافة تعليق على هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="49aac-154">If you require help for a particular field, let us know by adding a comment for this topic.</span></span>

### <a name="the-field-description-isnt-helpful"></a><span data-ttu-id="49aac-155">وصف الحقل غير مساعد.</span><span class="sxs-lookup"><span data-stu-id="49aac-155">The field description isn't helpful</span></span>

<span data-ttu-id="49aac-156">الرجاء إعلامنا برأيك عن طريق إضافة تعليق على هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="49aac-156">Let us know by adding a comment for this topic.</span></span> <span data-ttu-id="49aac-157">وقدّم لنا وصفًا للمعلومات الإضافية التي تحتاج إليها، إذا أمكنك ذلك.</span><span class="sxs-lookup"><span data-stu-id="49aac-157">If you can, describe the additional information that you require.</span></span>

### <a name="i-cant-find-a-field-on-the-field-descriptions-page"></a><span data-ttu-id="49aac-158">يتعذر عليّ العثور على حقل في صفحة أوصاف الحقول</span><span class="sxs-lookup"><span data-stu-id="49aac-158">I can't find a field on the Field descriptions page</span></span>

<span data-ttu-id="49aac-159">لإظهار كافة الحقول في صفحة، عيّن الخيار **تضمين الحقول بدون وصف** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="49aac-159">To show all the fields on a page, set the **Include fields without a description** option to **Yes**.</span></span> <span data-ttu-id="49aac-160">انقر فوق الحقل **تحديد صفحة** للتأكد من أنك حددت الصفحة الصحيحة.</span><span class="sxs-lookup"><span data-stu-id="49aac-160">Click the **Select a page** field to verify that you've selected the correct page.</span></span> <span data-ttu-id="49aac-161">إذا كان الاسم الذي كتبته جزءًا من اسم حقل آخر، فربما حددت الصفحة ذات الاسم الأطول.</span><span class="sxs-lookup"><span data-stu-id="49aac-161">If the name that you typed is part of another field name, you might have selected the page that has the longer name.</span></span>

### <a name="i-cant-find-a-page-on-the-field-descriptions-page"></a><span data-ttu-id="49aac-162">يتعذر عليّ العثور على صفحة في صفحة أوصاف الحقول</span><span class="sxs-lookup"><span data-stu-id="49aac-162">I can't find a page on the Field descriptions page</span></span>

<span data-ttu-id="49aac-163">للحصول على المعلومات حول الطرق المختلفة للعثور على الصفحات، راجع القسم "البحث عن صفحة" لاحقًا في هذه المقالة.</span><span class="sxs-lookup"><span data-stu-id="49aac-163">For information about the various way to find pages, see the "Searching for pages" section earlier in this article.</span></span> <span data-ttu-id="49aac-164">إذا كنت قد كتبت اسم الصفحة بدقة، فقد لا تظهر أوصاف الحقول إذا كان هناك أكثر من صفحة واحدة بنفس الاسم.</span><span class="sxs-lookup"><span data-stu-id="49aac-164">If you've typed the exact name of the page, the field descriptions might not be shown if more than one page has the same name.</span></span> <span data-ttu-id="49aac-165">انقر فوق السهم في الحقل **تحديد صفحة** لفتح قائمة تمت تصفيتها تتضمن الصفحات المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="49aac-165">Click the arrow in the **Select a page** field to open a filtered list of the pages that are available.</span></span>

<a name="see-also"></a><span data-ttu-id="49aac-166">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="49aac-166">See also</span></span>
--------

[<span data-ttu-id="49aac-167">تعليمات تخصيص الحقل</span><span class="sxs-lookup"><span data-stu-id="49aac-167">Customize field help</span></span>](../../dev-itpro/user-interface/customize-field-help.md)





