---
title: "استخدام عمليات البحث للعثور على المعلومات"
description: "في Microsoft Dynamics 365 for Finance and Operations، يحتوي العديد من الحقول على وظيفة البحث التي تساعدك في العثور على القيمة الصحيحة أو المطلوبة بسهولة. تمت إضافة العديد من التحسينات لـعمليات البحث والتي جعلت عناصر التحكم هذه أكثر قابلية للاستخدام، وعززت من إنتاجية المستخدمين. في هذا الموضوع، سوف تتعلم بشأن هذه الميزات الجديد للبحث، وسوف تحصل على نصائح مفيدة للوصول إلى أقصى استفادة ممكنة عند استخدامك لـ Lookups في النظام."
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 269934
ms.assetid: f20cbd2c-14e0-47e7-b351-8e60d3537f96
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 013901724864092571099835b2c71b297710ff03
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="use-lookups-to-find-information"></a><span data-ttu-id="13213-105">استخدام عمليات البحث للعثور على المعلومات</span><span class="sxs-lookup"><span data-stu-id="13213-105">Use lookups to find information</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="13213-106">في Microsoft Dynamics 365 for Finance and Operations، يحتوي العديد من الحقول على وظيفة البحث التي تساعدك في العثور على القيمة الصحيحة أو المطلوبة بسهولة.</span><span class="sxs-lookup"><span data-stu-id="13213-106">In Microsoft Dynamics 365 for Finance and Operations, many fields have lookups that can help you easily find the correct or desired value.</span></span> <span data-ttu-id="13213-107">تمت إضافة العديد من التحسينات لـعمليات البحث والتي جعلت عناصر التحكم هذه أكثر قابلية للاستخدام، وعززت من إنتاجية المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="13213-107">Several enhancements have been added to lookups that make these controls more usable and make users more productive.</span></span> <span data-ttu-id="13213-108">في هذا الموضوع، سوف تتعلم بشأن هذه الميزات الجديد للبحث، وسوف تحصل على نصائح مفيدة للوصول إلى أقصى استفادة ممكنة عند استخدامك لـ Lookups في النظام.</span><span class="sxs-lookup"><span data-stu-id="13213-108">In this topic, you will learn about these new lookup features and will receive some helpful tips to get the optimal use out of lookups in the system.</span></span>  

<a name="responsive-lookups"></a><span data-ttu-id="13213-109">عمليات البحث التفاعلية</span><span class="sxs-lookup"><span data-stu-id="13213-109">Responsive lookups</span></span>
------------------

<span data-ttu-id="13213-110">في الإصدارات السابقة من Finance and Operations، عند التفاعل مع عنصر التحكم في البحث، كان يتعين على المستخدم اتخاذ إجراء صريح لفتح القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="13213-110">In previous versions of Finance and Operations, when interacting with a lookup control, a user would have to take an explicit action to open the drop-down menu.</span></span> <span data-ttu-id="13213-111">وقد يكون هذا من خلال كتابة علامة نجمة(\*) في عنصر التحكم لتصفية البحث استناداً إلى القيمة الحالية لعنصر التحكم، أو النقر فوق زر القائمة المنسدلة، أو باستخدام اختصارات لوحة المفاتيح **Alt**+**سهم لأسفل**.</span><span class="sxs-lookup"><span data-stu-id="13213-111">This may have been by typing an asterisk (\*) in the control to filter the lookup based on the current value of the control, clicking the drop-down button, or by using the **Alt**+**Down arrow** keyboard shortcut.</span></span> <span data-ttu-id="13213-112">تم تعديل عناصر التحكم في البحث بالطرق التالية لتتماشي بشكل أفضل مع ممارسات الويب الحالية:</span><span class="sxs-lookup"><span data-stu-id="13213-112">Lookup controls have been modified in the following ways to better align with current web practices:</span></span>

-   <span data-ttu-id="13213-113">سوف يتم الآن فتح قوائم عمليات البحث المنسدلة تلقائيًا بعد توقف بسيط في الكتابة باستخدام محتويات القائمة المنسدلة بناءً على قيمة عنصر التحكم في البحث.</span><span class="sxs-lookup"><span data-stu-id="13213-113">Lookup drop-down menus will now open automatically after a slight pause in typing, with the drop-down menu contents filtered based on the lookup control's value.</span></span>
    -   <span data-ttu-id="13213-114">لاحظ أن السلوك القديم لفتح القائمة المنسدلة تلقائياً بعد كتابة علامة نجمة (\*) تم إهماله.</span><span class="sxs-lookup"><span data-stu-id="13213-114">Note that the old behavior of automatic opening of the dropdown after typing an asterisk (\*) has been deprecated.</span></span>
-   <span data-ttu-id="13213-115">بعد فتح قائمة البحث المنسدلة، يحدث ما يلي:</span><span class="sxs-lookup"><span data-stu-id="13213-115">After the lookup drop-down menu has opened, the following will occur:</span></span>
    -   <span data-ttu-id="13213-116">يظل المؤشر في عنصر تحكم البحث (بدلًا من التركيز على الانتقال إلى القائمة المنسدلة)، لذا يمكنك الاستمرار في إجراء تعديلات على قيمة عنصر التحكم.</span><span class="sxs-lookup"><span data-stu-id="13213-116">The cursor will stay in the lookup control (instead of focus moving into the drop-down menu) so you can continue to make modifications to the control's value.</span></span> <span data-ttu-id="13213-117">ولكن، لا يزال المستخدم قادرأ على استخدام **سهم لأعلى** و **سهم لأسفل** لتغيير الصفوف في القائمة المنسدلة، والضغط على "أدخل" لتحديد الصف الحالي في القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="13213-117">However, the user can still use the **Up arrow** and **Down arrow** to change rows in the drop-down menu, and enter to select the current row in the drop-down menu.</span></span>
    -   <span data-ttu-id="13213-118">سوف يتم ضبط محتويات القائمة المنسدلة بعد إجراء أي تعديلات على قيمة عنصر تحكم البحث.</span><span class="sxs-lookup"><span data-stu-id="13213-118">The contents of the drop-down menu will adjust after any modifications are made to the lookup control's value.</span></span>

<span data-ttu-id="13213-119">على سبيل المثال، اعتبر أن هناك حقل بحث يسمي **المدينة**.</span><span class="sxs-lookup"><span data-stu-id="13213-119">For example, consider a lookup field called **City**.</span></span> 

<span data-ttu-id="13213-120">عندما يكون التركيز في حقل **المدينة**، يمكنك بدء البحث عن المدينة التي تريدها عن طريق كتابة بعض الأحرف، مثل "العمود".</span><span class="sxs-lookup"><span data-stu-id="13213-120">When focus is in the **City** field, you can start looking for the city that you want by typing a few letters, like "col."</span></span>  <span data-ttu-id="13213-121">بعد التوقف عن الكتابة، سوف يفتح البحث تلقائياً، ويقوم بتصفية تلك المدن التي تبدأ بـ "العمود".</span><span class="sxs-lookup"><span data-stu-id="13213-121">After you stop typing, the lookup will open automatically, filtered to those cities that begin with "col".</span></span> 

<span data-ttu-id="13213-122">[![typeaheadLookupExample](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png)</span><span class="sxs-lookup"><span data-stu-id="13213-122">[![typeaheadLookupExample](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png)</span></span> 

<span data-ttu-id="13213-123">في هذه المرحلة، يظل المؤشر في حقل البحث.</span><span class="sxs-lookup"><span data-stu-id="13213-123">At this point, the cursor is still in the lookup field.</span></span> <span data-ttu-id="13213-124">إذا تابعت الكتابة، لتكون القيمة "العمود"، فمن ثم يتم ضبط محتويات البحث تلقائيًا لتعكس أحدث قيمة في عنصر التحكم.</span><span class="sxs-lookup"><span data-stu-id="13213-124">If you continue typing so the value is "colum," the lookup contents adjust automatically to reflect the latest value in the control.</span></span> 

![updateFilterLookupExample](./media/updatefilterlookupexample.png) 

<span data-ttu-id="13213-126">على الرغم من أن التركيز لا يزال في عنصر التحكم البحث، ألا يمكنك أيضا استخدام مفاتيح **سهم لأعلى** أو **سهم لأسفل** لتمييز الصف الذي ترغب في تحديده.</span><span class="sxs-lookup"><span data-stu-id="13213-126">Even though focus is still in the lookup control, you can also use the **Up arrow** or **Down arrow** keys to highlight the row that you want to select.</span></span> <span data-ttu-id="13213-127">إذا قمت بالضغط على زر **إدخال** فسوف يتم تحديد الصف المميز من البحث، وسوف يتم تحديث قيمة عنصر التحكم.</span><span class="sxs-lookup"><span data-stu-id="13213-127">If you press **Enter** the highlighted row will be selected from the lookup and the control's value will be updated.</span></span> 

![changingSelectionLookup](./media/changingselectionlookup.png)

## <a name="typing-in-more-than-ids"></a><span data-ttu-id="13213-129">الكتابة في أكثر من مُعرف</span><span class="sxs-lookup"><span data-stu-id="13213-129">Typing in more than IDs</span></span>
<span data-ttu-id="13213-130">عند إدخال البيانات، فمن الطبيعي للمستخدمين محاولة تحديد أي كيان مثل العميل أو المورد، باستخدام الاسم بدلاً من المعرف الذي يمثل الكيان.</span><span class="sxs-lookup"><span data-stu-id="13213-130">When entering data, it's natural for users to attempt to identify an entity, such as a customer or vendor, in terms of the name rather than an identifier representing the entity.</span></span> <span data-ttu-id="13213-131">في الإصدار الحالي من Finance and Operations، يسمح العديد من عمليات البحث (لكن ليس كلها) الآن بإدخال البيانات حسب السياق.</span><span class="sxs-lookup"><span data-stu-id="13213-131">In the current version of Finance and Operations, many (but not all) lookups now allow contextual data entry.</span></span> <span data-ttu-id="13213-132">تسمح هذه الميزة الفعالة للمستخدم بكتابة المُعرف أو الاسم المقابل داخل عنصر تحكم البحث.</span><span class="sxs-lookup"><span data-stu-id="13213-132">This powerful feature allows the user to type the ID or the corresponding name into the lookup control.</span></span> 

<span data-ttu-id="13213-133">على سبيل المثال، خذ بعين الاعتبار حقل **حساب العميل** عند إنشاء أمر توريد.</span><span class="sxs-lookup"><span data-stu-id="13213-133">For example, consider the **Customer account** field when creating a sales order.</span></span> <span data-ttu-id="13213-134">يظهر هذا الحقل **"معرف الحساب"** للعميل، ولكن عادةً ما يفضل المستخدم إدخال **اسم الحساب** بدلاً من **"معرف الحساب"** لهذا الحقل عند إنشاء أمر توريد، مثل ""Forest Wholesales" بدلاً من "US-003."</span><span class="sxs-lookup"><span data-stu-id="13213-134">This field shows the **Account ID** for the customer, but a user would typically prefer to enter an **Account name** instead of an **Account ID** for this field when creating a sales order, such as "Forest Wholesales" instead of "US-003."</span></span>

<span data-ttu-id="13213-135">في حالة بدء المستخدم إدخال **"معرف الحساب"** داخل البحث، فسوف تُفتح القائمة المنسدلة تلقائياً كما هو موضح في القسم السابق، وسوف يرى المستخدم البحث كما هو موضح أدناه.</span><span class="sxs-lookup"><span data-stu-id="13213-135">If the user started to enter an **Account ID** into the lookup control, the drop-down menu would automatically open as described in the previous section and the user would see the lookup as shown below.</span></span>

<span data-ttu-id="13213-136">[![البحث بحسب السياق عندما يتم إدخال معرف حساب العميل ](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)</span><span class="sxs-lookup"><span data-stu-id="13213-136">[![Contextual lookup when a customer account ID is entered](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)</span></span>

<span data-ttu-id="13213-137">ولكن، يمكن للمستخدم أيضا الآن إدخال بداية **اسم الحساب**.</span><span class="sxs-lookup"><span data-stu-id="13213-137">However, the user can also now enter the beginning of an **Account name** as well.</span></span> <span data-ttu-id="13213-138">إذا تم الكشف عنه، فمن ثم يرى المستخدم البحث التالي.</span><span class="sxs-lookup"><span data-stu-id="13213-138">If this is detected, then the user will see the following lookup.</span></span> <span data-ttu-id="13213-139">لاحظ كيف يتم نقل عمود **الاسم** ليكون العمود الأول في البحث، وكيف يتم فرز البحث وتصفيته بناءً على عمود **الاسم**.</span><span class="sxs-lookup"><span data-stu-id="13213-139">Notice how the **Name** column is moved to be the first column in the lookup, and how the lookup is sorted and filtered based on the **Name** column.</span></span>

<span data-ttu-id="13213-140">[![البحث بحسب السياق عندما يتم إدخال اسم العميل](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)</span><span class="sxs-lookup"><span data-stu-id="13213-140">[![Contextual lookup when a customer name is entered](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)</span></span>

## <a name="using-grid-column-headers-for-more-advanced-filtering-and-sorting"></a><span data-ttu-id="13213-141">استخدام رؤوس أعمدة الشبكة لتصفية وفرز أكثر تقدمًا</span><span class="sxs-lookup"><span data-stu-id="13213-141">Using grid column headers for more advanced filtering and sorting</span></span>
<span data-ttu-id="13213-142">عززت تحسينات البحث التي تمت مناقشتها في القسمين السابقين بصورة كبيرة من قدرة المستخدم على التنقل بين السطور في البحث بناءً علي بدء البحث بـحقل **المُعرف** أو **الاسم** الحقل في البحث.</span><span class="sxs-lookup"><span data-stu-id="13213-142">The lookup enhancements discussed in the previous two sections greatly improve a user's ability to navigate the rows in a lookup based on a "begins with" search of the **ID** or **Name** field in the lookup.</span></span> <span data-ttu-id="13213-143">ومع ذلك، هناك حالات يحتاج فيها المستخدم إلى تصفية أكثر تقدمًا (أو فرز) للعثور على الصف الصحيح.</span><span class="sxs-lookup"><span data-stu-id="13213-143">However, there are situations in which more advanced filtering (or sorting) is needed to find the correct row.</span></span> <span data-ttu-id="13213-144">في هذه الحالات، يحتاج المستخدم إلى استخدام خيارات التصفية والفرز في رؤوس أعمدة الشبكة داخل البحث.</span><span class="sxs-lookup"><span data-stu-id="13213-144">In these situations, the user needs to use the filtering and sorting options in the grid column headers inside the lookup.</span></span> <span data-ttu-id="13213-145">على سبيل المثال، اعتبر أن موظفًا أدخل بنود أمر المبيعات والذي يحتاج إلى تحديد "الكبل" الصحيح كمنتج.</span><span class="sxs-lookup"><span data-stu-id="13213-145">For example, consider an employee entering a sales order line who needs to locate the right "cable" as the product.</span></span> <span data-ttu-id="13213-146">في هذه الحالة، لا يُعد كتابة "كابل" داخل عنصر تحكم **رقم الصنف** أمرًا مفيدًا، حيث أنه لا توجد أسماء منتجات تبدأ بـ"كبل".</span><span class="sxs-lookup"><span data-stu-id="13213-146">Typing "cable" into the **Item number** control isn't helpful, as there are no product names that begin with "cable."</span></span> 

![emptyitemlookup](./media/emptyitemlookup.png) 

<span data-ttu-id="13213-148">بدلاً من ذلك، يحتاج المستخدم إلى مسح قيمة عنصر تحكم البحث، وفتح قائمة البحث المنسدلة، وتصفية القائمة المنسدلة باستخدام رأس عمود الشبكة، كما هو موضح أدناه.</span><span class="sxs-lookup"><span data-stu-id="13213-148">Instead, the user needs to clear the value of the lookup control, open the lookup drop-down menu, and filter the drop-down menu using the grid column header, as shown below.</span></span> <span data-ttu-id="13213-149">يمكن لمستخدم الماوس (أو اللمس) النقر ببساطة (أو لمس) أي رأس عمود للوصول إلى خيارات التصفية والفرز لذلك العمود.</span><span class="sxs-lookup"><span data-stu-id="13213-149">A mouse (or touch) user can simply click (or touch) any column header to access the filtering and sorting options for that column.</span></span> <span data-ttu-id="13213-150">بالنسبة إلى مستخدم لوحة المفاتيح، يحتاج المستخدم بكل بساطة إلى الضغط على **Alt**+**سهم** **للأسفل** مرة ثانية لنقل التركيز إلى القائمة المنسدلة، ويمكنه بعد ذلك الضغط على المفتاح tab للانتقال إلى العمود الصحيح، ثم على **Ctrl**+**G** لفتح القائمة المنسدلة لرأس عمود الشبكة.</span><span class="sxs-lookup"><span data-stu-id="13213-150">For a keyboard user, the user simply needs to press **Alt**+**Down** **arrow** a second time to move focus into the drop-down menu, after which the user can tab to the correct column, and then press **Ctrl**+**G** to open the grid column header drop-down menu.</span></span> 

<span data-ttu-id="13213-151">[![gridfilteritemlookup](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png)</span><span class="sxs-lookup"><span data-stu-id="13213-151">[![gridfilteritemlookup](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png)</span></span> 

<span data-ttu-id="13213-152">بعد تطبيق عامل التصفية (أنظر الصورة أدناه)، يمكن للمستخدم العثور على وتحديد الصف كالمعتاد.</span><span class="sxs-lookup"><span data-stu-id="13213-152">After the filter has been applied (see the image below), the user can find and select the row as usual.</span></span> 

![filtereditemlookup](./media/filtereditemlookup.png)




