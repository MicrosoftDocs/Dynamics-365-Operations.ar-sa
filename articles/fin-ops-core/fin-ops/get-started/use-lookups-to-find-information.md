---
title: البحث عن المعلومات باستخدام عمليات البحث
description: في هذا الموضوع، سوف تتعلم بشأن ميزات البحث هذه، وسوف تحصل على نصائح مفيدة للوصول إلى أقصى استفادة ممكنة عند استخدامك لعمليات البحث في النظام.
author: jasongre
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 269934
ms.assetid: f20cbd2c-14e0-47e7-b351-8e60d3537f96
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: adb8e1a0fef93fdd66a4cbac82689ff7a19aca4a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754766"
---
# <a name="find-information-by-using-lookups"></a><span data-ttu-id="0fd3e-103">البحث عن المعلومات باستخدام عمليات البحث</span><span class="sxs-lookup"><span data-stu-id="0fd3e-103">Find information by using lookups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0fd3e-104">يتضمن عدد كبير من الحقول وظيفة البحث التي تساعدك في العثور على القيمة الصحيحة أو المطلوبة بسهولة.</span><span class="sxs-lookup"><span data-stu-id="0fd3e-104">Many fields have lookups that can help you easily find the correct or desired value.</span></span> <span data-ttu-id="0fd3e-105">تمت إضافة العديد من التحسينات لـعمليات البحث والتي جعلت عناصر التحكم هذه أكثر قابلية للاستخدام، وعززت من إنتاجية المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="0fd3e-105">Several enhancements have been added to lookups that make these controls more usable and make users more productive.</span></span> <span data-ttu-id="0fd3e-106">في هذا الموضوع، سوف تتعلم بشأن هذه الميزات الجديد للبحث، وسوف تحصل على نصائح مفيدة للوصول إلى أقصى استفادة ممكنة عند استخدامك لـ Lookups في النظام.</span><span class="sxs-lookup"><span data-stu-id="0fd3e-106">In this topic, you will learn about these new lookup features and will receive some helpful tips to get the optimal use out of lookups in the system.</span></span>

## <a name="responsive-lookups"></a><span data-ttu-id="0fd3e-107">عمليات البحث التفاعلية</span><span class="sxs-lookup"><span data-stu-id="0fd3e-107">Responsive lookups</span></span>

<span data-ttu-id="0fd3e-108">في الإصدارات السابقة، عند التفاعل مع عنصر التحكم في البحث، كان يتعين على المستخدم اتخاذ إجراء صريح لفتح القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="0fd3e-108">In previous versions, when interacting with a lookup control, a user would have to take an explicit action to open the drop-down menu.</span></span> <span data-ttu-id="0fd3e-109">وقد يكون هذا من خلال كتابة علامة نجمة(\*) في عنصر التحكم لتصفية البحث استناداً إلى القيمة الحالية لعنصر التحكم، أو النقر فوق زر القائمة المنسدلة، أو باستخدام اختصارات لوحة المفاتيح **Alt**+**سهم لأسفل**.</span><span class="sxs-lookup"><span data-stu-id="0fd3e-109">This may have been by typing an asterisk (\*) in the control to filter the lookup based on the current value of the control, clicking the drop-down button, or by using the **Alt**+**Down arrow** keyboard shortcut.</span></span> <span data-ttu-id="0fd3e-110">تم تعديل عناصر التحكم في البحث بالطرق التالية لتتماشي بشكل أفضل مع ممارسات الويب الحالية:</span><span class="sxs-lookup"><span data-stu-id="0fd3e-110">Lookup controls have been modified in the following ways to better align with current web practices:</span></span>

- <span data-ttu-id="0fd3e-111">سوف يتم الآن فتح قوائم عمليات البحث المنسدلة تلقائيًا بعد توقف بسيط في الكتابة باستخدام محتويات القائمة المنسدلة بناءً على قيمة عنصر التحكم في البحث.</span><span class="sxs-lookup"><span data-stu-id="0fd3e-111">Lookup drop-down menus will now open automatically after a slight pause in typing, with the drop-down menu contents filtered based on the lookup control's value.</span></span>

    <span data-ttu-id="0fd3e-112">لاحظ أن السلوك القديم لفتح القائمة المنسدلة تلقائياً بعد كتابة علامة نجمة (\*) تم إهماله.</span><span class="sxs-lookup"><span data-stu-id="0fd3e-112">Note that the old behavior of automatic opening of the dropdown after typing an asterisk (\*) has been deprecated.</span></span>

- <span data-ttu-id="0fd3e-113">بعد فتح قائمة البحث المنسدلة، يحدث ما يلي:</span><span class="sxs-lookup"><span data-stu-id="0fd3e-113">After the lookup drop-down menu has opened, the following will occur:</span></span>

    - <span data-ttu-id="0fd3e-114">يظل المؤشر في عنصر تحكم البحث (بدلًا من التركيز على الانتقال إلى القائمة المنسدلة)، لذا يمكنك الاستمرار في إجراء تعديلات على قيمة عنصر التحكم.</span><span class="sxs-lookup"><span data-stu-id="0fd3e-114">The cursor will stay in the lookup control (instead of focus moving into the drop-down menu) so you can continue to make modifications to the control's value.</span></span> <span data-ttu-id="0fd3e-115">ولكن، لا يزال المستخدم قادرأ على استخدام **سهم لأعلى** و **سهم لأسفل** لتغيير الصفوف في القائمة المنسدلة، والضغط على "أدخل" لتحديد الصف الحالي في القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="0fd3e-115">However, the user can still use the **Up arrow** and **Down arrow** to change rows in the drop-down menu, and enter to select the current row in the drop-down menu.</span></span>
    - <span data-ttu-id="0fd3e-116">سوف يتم ضبط محتويات القائمة المنسدلة بعد إجراء أي تعديلات على قيمة عنصر تحكم البحث.</span><span class="sxs-lookup"><span data-stu-id="0fd3e-116">The contents of the drop-down menu will adjust after any modifications are made to the lookup control's value.</span></span>

<span data-ttu-id="0fd3e-117">على سبيل المثال، اعتبر أن هناك حقل بحث يسمي **المدينة**.</span><span class="sxs-lookup"><span data-stu-id="0fd3e-117">For example, consider a lookup field called **City**.</span></span>

<span data-ttu-id="0fd3e-118">عندما يكون التركيز في حقل **المدينة**، يمكنك بدء البحث عن المدينة التي تريدها عن طريق كتابة بعض الأحرف، مثل "العمود".</span><span class="sxs-lookup"><span data-stu-id="0fd3e-118">When focus is in the **City** field, you can start looking for the city that you want by typing a few letters, like "col."</span></span> <span data-ttu-id="0fd3e-119">بعد التوقف عن الكتابة، سوف يفتح البحث تلقائياً، ويقوم بتصفية تلك المدن التي تبدأ بـ "العمود".</span><span class="sxs-lookup"><span data-stu-id="0fd3e-119">After you stop typing, the lookup will open automatically, filtered to those cities that begin with "col".</span></span>

<span data-ttu-id="0fd3e-120">[![typeaheadLookupExample](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png)</span><span class="sxs-lookup"><span data-stu-id="0fd3e-120">[![typeaheadLookupExample](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png)</span></span>

<span data-ttu-id="0fd3e-121">في هذه المرحلة، يظل المؤشر في حقل البحث.</span><span class="sxs-lookup"><span data-stu-id="0fd3e-121">At this point, the cursor is still in the lookup field.</span></span> <span data-ttu-id="0fd3e-122">إذا تابعت الكتابة، لتكون القيمة "العمود"، فمن ثم يتم ضبط محتويات البحث تلقائيًا لتعكس أحدث قيمة في عنصر التحكم.</span><span class="sxs-lookup"><span data-stu-id="0fd3e-122">If you continue typing so the value is "colum," the lookup contents adjust automatically to reflect the latest value in the control.</span></span>

![updateFilterLookupExample](./media/updatefilterlookupexample.png)

<span data-ttu-id="0fd3e-124">على الرغم من أن التركيز لا يزال في عنصر التحكم البحث، ألا يمكنك أيضا استخدام مفاتيح **سهم لأعلى** أو **سهم لأسفل** لتمييز الصف الذي ترغب في تحديده.</span><span class="sxs-lookup"><span data-stu-id="0fd3e-124">Even though focus is still in the lookup control, you can also use the **Up arrow** or **Down arrow** keys to highlight the row that you want to select.</span></span> <span data-ttu-id="0fd3e-125">إذا قمت بالضغط على زر **إدخال** فسوف يتم تحديد الصف المميز من البحث، وسوف يتم تحديث قيمة عنصر التحكم.</span><span class="sxs-lookup"><span data-stu-id="0fd3e-125">If you press **Enter** the highlighted row will be selected from the lookup and the control's value will be updated.</span></span>

![changingSelectionLookup](./media/changingselectionlookup.png)

## <a name="typing-in-more-than-ids"></a><span data-ttu-id="0fd3e-127">الكتابة في أكثر من مُعرف</span><span class="sxs-lookup"><span data-stu-id="0fd3e-127">Typing in more than IDs</span></span>

<span data-ttu-id="0fd3e-128">عند إدخال البيانات، فمن الطبيعي للمستخدمين محاولة تحديد أي كيان مثل العميل أو المورد، باستخدام الاسم بدلاً من المعرف الذي يمثل الكيان.</span><span class="sxs-lookup"><span data-stu-id="0fd3e-128">When entering data, it's natural for users to attempt to identify an entity, such as a customer or vendor, in terms of the name rather than an identifier representing the entity.</span></span> <span data-ttu-id="0fd3e-129">العديد من عمليات البحث (وليس كلها) الآن تسمح بإدخال البيانات السياقية.</span><span class="sxs-lookup"><span data-stu-id="0fd3e-129">Many (but not all) lookups now allow contextual data entry.</span></span> <span data-ttu-id="0fd3e-130">تسمح هذه الميزة الفعالة للمستخدم بكتابة المُعرف أو الاسم المقابل داخل عنصر تحكم البحث.</span><span class="sxs-lookup"><span data-stu-id="0fd3e-130">This powerful feature allows the user to type the ID or the corresponding name into the lookup control.</span></span>

<span data-ttu-id="0fd3e-131">على سبيل المثال، خذ بعين الاعتبار حقل **حساب العميل** عند إنشاء أمر توريد.</span><span class="sxs-lookup"><span data-stu-id="0fd3e-131">For example, consider the **Customer account** field when creating a sales order.</span></span> <span data-ttu-id="0fd3e-132">يظهر هذا الحقل **"معرف الحساب"** للعميل، ولكن عادةً ما يفضل المستخدم إدخال **اسم الحساب** بدلاً من **"معرف الحساب"** لهذا الحقل عند إنشاء أمر توريد، مثل ""Forest Wholesales" بدلاً من "US-003."</span><span class="sxs-lookup"><span data-stu-id="0fd3e-132">This field shows the **Account ID** for the customer, but a user would typically prefer to enter an **Account name** instead of an **Account ID** for this field when creating a sales order, such as "Forest Wholesales" instead of "US-003."</span></span>

<span data-ttu-id="0fd3e-133">في حالة بدء المستخدم إدخال **"معرف الحساب"** داخل البحث، فسوف تُفتح القائمة المنسدلة تلقائياً كما هو موضح في القسم السابق، وسوف يرى المستخدم البحث كما هو موضح أدناه.</span><span class="sxs-lookup"><span data-stu-id="0fd3e-133">If the user started to enter an **Account ID** into the lookup control, the drop-down menu would automatically open as described in the previous section and the user would see the lookup as shown below.</span></span>

<span data-ttu-id="0fd3e-134">[![البحث بحسب السياق عندما يتم إدخال معرف حساب العميل ](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)</span><span class="sxs-lookup"><span data-stu-id="0fd3e-134">[![Contextual lookup when a customer account ID is entered](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)</span></span>

<span data-ttu-id="0fd3e-135">ولكن، يمكن للمستخدم أيضا الآن إدخال بداية **اسم الحساب**.</span><span class="sxs-lookup"><span data-stu-id="0fd3e-135">However, the user can also now enter the beginning of an **Account name** as well.</span></span> <span data-ttu-id="0fd3e-136">إذا تم الكشف عنه، فمن ثم يرى المستخدم البحث التالي.</span><span class="sxs-lookup"><span data-stu-id="0fd3e-136">If this is detected, then the user will see the following lookup.</span></span> <span data-ttu-id="0fd3e-137">لاحظ كيف يتم نقل عمود **الاسم** ليكون العمود الأول في البحث، وكيف يتم فرز البحث وتصفيته بناءً على عمود **الاسم**.</span><span class="sxs-lookup"><span data-stu-id="0fd3e-137">Notice how the **Name** column is moved to be the first column in the lookup, and how the lookup is sorted and filtered based on the **Name** column.</span></span>

<span data-ttu-id="0fd3e-138">[![البحث بحسب السياق عندما يتم إدخال اسم العميل](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)</span><span class="sxs-lookup"><span data-stu-id="0fd3e-138">[![Contextual lookup when a customer name is entered](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)</span></span>

## <a name="using-grid-column-headers-for-more-advanced-filtering-and-sorting"></a><span data-ttu-id="0fd3e-139">استخدام رؤوس أعمدة الشبكة لتصفية وفرز أكثر تقدمًا</span><span class="sxs-lookup"><span data-stu-id="0fd3e-139">Using grid column headers for more advanced filtering and sorting</span></span>

<span data-ttu-id="0fd3e-140">عززت تحسينات البحث التي تمت مناقشتها في القسمين السابقين بصورة كبيرة من قدرة المستخدم على التنقل بين السطور في البحث بناءً علي بدء البحث بـحقل **المُعرف** أو **الاسم** الحقل في البحث.</span><span class="sxs-lookup"><span data-stu-id="0fd3e-140">The lookup enhancements discussed in the previous two sections greatly improve a user's ability to navigate the rows in a lookup based on a "begins with" search of the **ID** or **Name** field in the lookup.</span></span> <span data-ttu-id="0fd3e-141">ومع ذلك، هناك حالات يحتاج فيها المستخدم إلى تصفية أكثر تقدمًا (أو فرز) للعثور على الصف الصحيح.</span><span class="sxs-lookup"><span data-stu-id="0fd3e-141">However, there are situations in which more advanced filtering (or sorting) is needed to find the correct row.</span></span> <span data-ttu-id="0fd3e-142">في هذه الحالات، يحتاج المستخدم إلى استخدام خيارات التصفية والفرز في رؤوس أعمدة الشبكة داخل البحث.</span><span class="sxs-lookup"><span data-stu-id="0fd3e-142">In these situations, the user needs to use the filtering and sorting options in the grid column headers inside the lookup.</span></span> <span data-ttu-id="0fd3e-143">على سبيل المثال، اعتبر أن موظفًا أدخل بنود أمر المبيعات والذي يحتاج إلى تحديد "الكبل" الصحيح كمنتج.</span><span class="sxs-lookup"><span data-stu-id="0fd3e-143">For example, consider an employee entering a sales order line who needs to locate the right "cable" as the product.</span></span> <span data-ttu-id="0fd3e-144">في هذه الحالة، لا يُعد كتابة "كابل" داخل عنصر تحكم **رقم الصنف** أمرًا مفيدًا، حيث أنه لا توجد أسماء منتجات تبدأ بـ"كبل".</span><span class="sxs-lookup"><span data-stu-id="0fd3e-144">Typing "cable" into the **Item number** control isn't helpful, as there are no product names that begin with "cable."</span></span>

![emptyitemlookup](./media/emptyitemlookup.png)

<span data-ttu-id="0fd3e-146">بدلاً من ذلك، يحتاج المستخدم إلى مسح قيمة عنصر تحكم البحث، وفتح قائمة البحث المنسدلة، وتصفية القائمة المنسدلة باستخدام رأس عمود الشبكة، كما هو موضح أدناه.</span><span class="sxs-lookup"><span data-stu-id="0fd3e-146">Instead, the user needs to clear the value of the lookup control, open the lookup drop-down menu, and filter the drop-down menu using the grid column header, as shown below.</span></span> <span data-ttu-id="0fd3e-147">يمكن لمستخدم الماوس (أو اللمس) النقر ببساطة (أو لمس) أي رأس عمود للوصول إلى خيارات التصفية والفرز لذلك العمود.</span><span class="sxs-lookup"><span data-stu-id="0fd3e-147">A mouse (or touch) user can simply click (or touch) any column header to access the filtering and sorting options for that column.</span></span> <span data-ttu-id="0fd3e-148">بالنسبة إلى مستخدم لوحة المفاتيح، يحتاج المستخدم بكل بساطة إلى الضغط على **Alt**+**سهم** **للأسفل** مرة ثانية لنقل التركيز إلى القائمة المنسدلة، ويمكنه بعد ذلك الضغط على المفتاح tab للانتقال إلى العمود الصحيح، ثم على **Ctrl**+**G** لفتح القائمة المنسدلة لرأس عمود الشبكة.</span><span class="sxs-lookup"><span data-stu-id="0fd3e-148">For a keyboard user, the user simply needs to press **Alt**+**Down** **arrow** a second time to move focus into the drop-down menu, after which the user can tab to the correct column, and then press **Ctrl**+**G** to open the grid column header drop-down menu.</span></span>

<span data-ttu-id="0fd3e-149">[![gridfilteritemlookup](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png)</span><span class="sxs-lookup"><span data-stu-id="0fd3e-149">[![gridfilteritemlookup](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png)</span></span>

<span data-ttu-id="0fd3e-150">بعد تطبيق عامل التصفية (أنظر الصورة أدناه)، يمكن للمستخدم العثور على وتحديد الصف كالمعتاد.</span><span class="sxs-lookup"><span data-stu-id="0fd3e-150">After the filter has been applied (see the image below), the user can find and select the row as usual.</span></span>

![filtereditemlookup](./media/filtereditemlookup.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]