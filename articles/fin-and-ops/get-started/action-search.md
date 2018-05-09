---
title: "البحث عن إجراء"
description: "توضح هذه المقالة وظيفة البحث عن إجراء في Microsoft Dynamics 365 for Finance and Operations. سوف تساعدك وظيفة البحث عن إجراء في العثور على الإجراءات وتشغيلها على الصفحة."
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
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 6f623c5fc9b277933c4655101fe451c87a1e5224
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---

# <a name="action-search"></a><span data-ttu-id="6f5ee-104">البحث عن إجراء</span><span class="sxs-lookup"><span data-stu-id="6f5ee-104">Action search</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f5ee-105">توضح هذه المقالة وظيفة البحث عن إجراء في Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-105">This article describes the action search functionality in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="6f5ee-106">سوف تساعدك وظيفة البحث عن إجراء في العثور على الإجراءات وتشغيلها على الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-106">Action search will help you find and run actions on a page.</span></span>

<a name="introduction"></a><span data-ttu-id="6f5ee-107">مقدمة</span><span class="sxs-lookup"><span data-stu-id="6f5ee-107">Introduction</span></span>
------------

<span data-ttu-id="6f5ee-108">تعرض الصفحات في Microsoft Dynamics 365 for Finance and Operations بشكل أساسي الأوامر في أجزاء الإجراءات؛ جزء الإجراءات المعيارية التي تظهر في أعلى الصفحة، وأشرطة الأدوات التي تظهر في أقسام متنوعة من الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-108">Pages in Microsoft Dynamics 365 for Finance and Operations primarily expose commands on Action Panes, both the standard Action Pane that appears at the top of a page and the toolbars that appear in various sections of the page.</span></span> <span data-ttu-id="6f5ee-109">في الإصدارات السابقة، تسمح لك وظيفة "التلميحات الرئيسية" الوصول بسرعة إلى أي زر في أجزاء الإجراء من خلال الضغط على مفتاح Alt، ثم مجموعة من الأحرف.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-109">In previous versions, a Key Tips feature let you quickly access any button on an Action Pane by pressing the Alt key and then a series of letters.</span></span> 

<span data-ttu-id="6f5ee-110">[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png) ولكن، في الإصدار الحالي من Finance and Operations، لم تعد ميزة التلميحات الأساسية متاحة، ولكن تم استبدالها بميزة البحث عن إجراء.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-110">[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png) However, in the current version of Finance and Operations, Key Tips are no longer available but have been replaced by the action search feature.</span></span> <span data-ttu-id="6f5ee-111">تُمكّنك هذه الميزة الجديدة من البحث بسرعة عن وتشغيل زر من أي "جزء إجراء" مرئي.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-111">This new feature lets you quickly search for and run a button from any visible Action Pane.</span></span>

## <a name="using-action-search"></a><span data-ttu-id="6f5ee-112">استخدام البحث عن إجراء</span><span class="sxs-lookup"><span data-stu-id="6f5ee-112">Using action search</span></span>
<span data-ttu-id="6f5ee-113">لاستخدام ميزة البحث عن إجراء، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-113">To use the action search feature, follow these steps.</span></span>

1.  <span data-ttu-id="6f5ee-114">في "جزء الإجراءات"، انقر فوق حقل **البحث عن إجراء**.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-114">On the Action Pane, click in the **action search** field.</span></span> <span data-ttu-id="6f5ee-115">(يحتوي حقل **البحث عن إجراء** على رمز معدسة مكبرة).</span><span class="sxs-lookup"><span data-stu-id="6f5ee-115">(The **action search** field contains a magnifying glass icon.)</span></span>
2.  <span data-ttu-id="6f5ee-116">اكتب اسم الزر كله أو جزء من اسم الزر الذي تريد تشغيله.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-116">Type all or part of the name of the button that you want to run.</span></span> <span data-ttu-id="6f5ee-117">يمكنك أيضًا البحث باستخدام الكلمات من الزر "مسار".</span><span class="sxs-lookup"><span data-stu-id="6f5ee-117">You can also search by using words from the button's "path."</span></span> <span data-ttu-id="6f5ee-118">(لمزيد من المعلومات، يُرجى الاطلاع على القسم التالي من هذه المقالة.) عادةً، سوف يظهر الزر بجانب أعلي قائمة النتائج بعد كتابة من حرفين إلى أربعة أحرف.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-118">(For more information, see the next section of this article.) Typically, a button will appear near the top of the results list after you've typed two to four characters.</span></span>
3.  <span data-ttu-id="6f5ee-119">ابحث عن وقم بتشغيل الزر في قائمة النتائج (باستخدام الماوس أو لوحة المفاتيح).</span><span class="sxs-lookup"><span data-stu-id="6f5ee-119">Find and run the button in the results list (by using your mouse or keyboard).</span></span>

<span data-ttu-id="6f5ee-120">وبعد تشغيل الزر، يتم إرجاع التركيز إلى الموضع الأخير في الصفحة، بحيث يمكنك متابعة العمل.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-120">After the button is run, the focus is returned to your last position on the page, so that you can continue to work.</span></span> 

<span data-ttu-id="6f5ee-121">[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)</span><span class="sxs-lookup"><span data-stu-id="6f5ee-121">[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)</span></span>

<span data-ttu-id="6f5ee-122">يمكنك أيضًا بدء تشغيل البحث عن إجراء بالضغط على Ctrl+/ أو Alt+Q.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-122">You can also start action search by pressing Ctrl+/ or Alt+Q.</span></span> <span data-ttu-id="6f5ee-123">اضغط على اختصار لوحة المفاتيح مرة أخرى لإرجاع التركيز إلى الموضع الأخير في الصفحة مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-123">Press the keyboard shortcut again to return the focus to your last position on the page.</span></span>

## <a name="understanding-the-results-list"></a><span data-ttu-id="6f5ee-124">فهم قائمة النتائج</span><span class="sxs-lookup"><span data-stu-id="6f5ee-124">Understanding the results list</span></span>
<span data-ttu-id="6f5ee-125">غالبًا، في Finance and Operations، يجب أن تعرف كل من موقع و سياق الزر ليكون لديك فهم واضح بوظيفة هذا الزر.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-125">Often, in Finance and Operations, you must know both the location and the context of a button to fully understand the purpose of that button.</span></span> <span data-ttu-id="6f5ee-126">وبالتالي، يتم عرض معلومات إضافية لكل عنصر في قائمة النتائج، وذلك لمساعدتك على فهم وظيفة الأزرار التي تظهر في القائمة.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-126">Therefore, additional information is shown for each item in the results list, to help you understand exactly which buttons appear in the list.</span></span> <span data-ttu-id="6f5ee-127">وبشكل خاص، يتم عرض "مسار" الزر.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-127">In particular, the "path" of the button is shown.</span></span> <span data-ttu-id="6f5ee-128">قد يتضمن هذا المسار تسميات عناصر واجهة المستخدم التالية، حسب الاقتضاء:</span><span class="sxs-lookup"><span data-stu-id="6f5ee-128">This path might include the labels of the following UI elements, as relevant:</span></span>

-   <span data-ttu-id="6f5ee-129">علامة تبويب جزء الإجراءات</span><span class="sxs-lookup"><span data-stu-id="6f5ee-129">Action Pane tab</span></span>
-   <span data-ttu-id="6f5ee-130">مجموعة الزر</span><span class="sxs-lookup"><span data-stu-id="6f5ee-130">Button group</span></span>
-   <span data-ttu-id="6f5ee-131">زر القائمة (إذا كان الزر داخل زر قائمة)</span><span class="sxs-lookup"><span data-stu-id="6f5ee-131">Menu button (if the button is inside a menu button)</span></span>
-   <span data-ttu-id="6f5ee-132">فاصل القائمة (إذا كان الزر داخل مجموعة مسماة داخل زر قائمة)</span><span class="sxs-lookup"><span data-stu-id="6f5ee-132">Menu separator (if the button is inside a named group inside a menu button)</span></span>
-   <span data-ttu-id="6f5ee-133">مجموعة أو علامة تبويب في الصفحة (على سبيل المثال، اسم علامة تبويب سريعة)</span><span class="sxs-lookup"><span data-stu-id="6f5ee-133">Group or tab on the page (for example, the name of a FastTab)</span></span>

<span data-ttu-id="6f5ee-134">على سبيل المثال، يمكنك كتابة **tot** في حقل **البحث عن إجراء** ويتم الآن فحص قائمة النتائج.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-134">For example, you typed **tot** in the **action search** field and are now examining the results list.</span></span> <span data-ttu-id="6f5ee-135">يتم تمييز الإدخال الأول، لزر يُسمى **الإجماليات**.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-135">The first entry, for a button that is named **Totals**, is highlighted.</span></span> <span data-ttu-id="6f5ee-136">كما يوضح أيضًا مسار زر **أمر المبيعات** &gt; **عرض** .</span><span class="sxs-lookup"><span data-stu-id="6f5ee-136">A button path of **Sales order** &gt; **View** is also shown.</span></span> <span data-ttu-id="6f5ee-137">يتطابق الجزء **أمر المبيعات** للمسار مع علامة التبويب **أمر المبيعات** على جزء الإجراءات، ويتطابق الجزء **عرض** للمسار مع المجموعة **عرض** على علامة التبويب هذه. بطريقة مماثلة، يعلمك جزء الزر **الخصم الإجمالي‬** (**بيع** &gt; **حساب**) أن هذا الزر يقع في المجموعة **حساب** على علامة التبويب **بيع** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-137">The **Sales order** part of the path corresponds to the **Sales order** tab on the Action Pane, and the **View** part of the path corresponds to the **View** group on that tab. Similarly, the path of the **Total discount** button (**Sell** &gt; **Calculate**) informs you that this button is located in the **Calculate** group on the **Sell** tab of the Action Pane.</span></span> <span data-ttu-id="6f5ee-138">وبالتالي، تساعدك هذه المعلومات على فهم ما هو الزر الذي سيتم تشغيله بالظبط باستخدام وظيفة بحث الإجراء (إذا قمت باختيار هذا الزر في قائمة النتائج).</span><span class="sxs-lookup"><span data-stu-id="6f5ee-138">Therefore, this information helps you understand exactly which button will be triggered by action search (if you select that button in the results list).</span></span> 

<span data-ttu-id="6f5ee-139">[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)</span><span class="sxs-lookup"><span data-stu-id="6f5ee-139">[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)</span></span> 

<span data-ttu-id="6f5ee-140">في المثال السابق، أظهرت عملية البحث عن إجراء نتائج من جزء الإجراءات القياسي في أعلى الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-140">In the previous example, action search showed results from the standard Action Pane at the top of a page.</span></span> <span data-ttu-id="6f5ee-141">ومع ذلك، يعرض البحث عن إجراء أيضًا نتائج من أشرطة الأدوات المرئية الموجودة في أماكن أخرى في الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-141">However, action search also shows results from visible toolbars that are located in other places on the page.</span></span> <span data-ttu-id="6f5ee-142">على سبيل المثال، تقوم بالبحث عن زر **المخزون الفعلي** الموجود في علامة التبويب السريعة **بنود أمر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-142">For example, you're searching for the **On-hand inventory** button that is located on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="6f5ee-143">في هذه الحالة، يُخبرك مسار الزر في قائمة النتائج (**بنود أمر المبيعات** &gt; **المخزون** &gt; **عرض**) أن هذا الزر يقع تحت **عرض** بعنوان زر قائمة **المخزون** في علامة التبويب السريعة **بنود أمر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-143">In this case, the button path in the results list (**Sales order lines** &gt; **Inventory** &gt; **View**) informs you that this button is located under the **View** heading on the **Inventory** menu button on the **Sales order lines** FastTab.</span></span> 

<span data-ttu-id="6f5ee-144">[![المخزون الفعلي](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)</span><span class="sxs-lookup"><span data-stu-id="6f5ee-144">[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)</span></span>

## <a name="action-search-vs-navigation-search"></a><span data-ttu-id="6f5ee-145">البحث عن إجراء بحث مقابل البحث عن تنقل</span><span class="sxs-lookup"><span data-stu-id="6f5ee-145">Action search vs. Navigation search</span></span>
<span data-ttu-id="6f5ee-146">وعلى الرغم من أنه يتم استخدام البحث عن إجراء للبحث عن وتشغيل الإجراءات في صفحة، إلا أن هناك آلية بحث منفصلة للبحث والتنقل بين الصفحات في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6f5ee-146">Whereas action search is intended to find and run actions on a page, there is a separate search mechanism for finding and navigating to pages in Finance and Operations.</span></span> <span data-ttu-id="6f5ee-147">للمزيد من المعلومات حول هذه الميزة، راجع مقالة [‏‫بحث التنقل‬](navigation-search.md).</span><span class="sxs-lookup"><span data-stu-id="6f5ee-147">For more information about that feature, see the [Navigation search](navigation-search.md) article.</span></span>




