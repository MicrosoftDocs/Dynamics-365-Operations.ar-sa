---
title: إعداد عنصر قائمة جهاز محمول لتوفير نظرة عامة على بنود الانتقاء
description: يوضح هذا الموضوع كيف يمكن التحديد وقت ظهور قائمة تتضمن جميع بنود العمل للعاملين في المستودع الذين يقومون بمعالجة عمل المستودع على جهاز محمول. قد تكون هذه الإمكانية مفيدة للعاملين في المستودع الذين يحتاجون في أغلب الأحيان إلى نظرة عامة على بنود الانتقاء في أمر العمل لتمكينه من تحسين تسلسل الانتقاء.
author: MarkusFogelberg
manager: tfehr
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 3a2c8a69a2c64214a38a654042ea2f62575e7f52
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421249"
---
# <a name="set-up-a-mobile-device-menu-item-to-provide-a-pick-line-overview"></a><span data-ttu-id="a2d39-104">إعداد عنصر قائمة جهاز محمول لتوفير نظرة عامة على بنود الانتقاء</span><span class="sxs-lookup"><span data-stu-id="a2d39-104">Set up a mobile device menu item to provide a pick line overview</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="a2d39-105">يوضح هذا الموضوع كيفية تكوين الخيارات المتعلقة بالنظرة العامة على بنود الانتقاء لعناصر قائمة الجهاز المحمول المستخدمة لمعالجة عمل الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="a2d39-105">This topic explains how to configure options that are related to the pick line overview for mobile device menu items that are used to process picking work.</span></span> <span data-ttu-id="a2d39-106">تسمح النظرة العامة على بنود الانتقاء للعاملين في المستودع بعرض قائمة تتضمن جميع بنود العمل المرتبطة بمهمتهم الحالية والتحديد من هذه القائمة.</span><span class="sxs-lookup"><span data-stu-id="a2d39-106">The pick line overview lets warehouse workers view and select from a list of all the work lines that are related to their current task.</span></span> <span data-ttu-id="a2d39-107">بإمكان هذه الإمكانية أن تساعد العاملين على تحسين تسلسل الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="a2d39-107">This capability can help workers optimize their picking sequence.</span></span> <span data-ttu-id="a2d39-108">توفر الميزة خيار تحل محل الزر **تخطي** القياسي الذي يسمح للعاملين بالتنقل عبر البنود كل بند على حدة، بترتيب ثابت.</span><span class="sxs-lookup"><span data-stu-id="a2d39-108">The feature provides options that replace the standard **Skip** button that lets workers cycle through the lines one at a time, in a fixed order.</span></span> <span data-ttu-id="a2d39-109">(ومع ذلك، يبقى خيار استخدام هذا الزر متوفرًا.)</span><span class="sxs-lookup"><span data-stu-id="a2d39-109">(However, the option to use that button is still available.)</span></span>

<span data-ttu-id="a2d39-110">بإمكان المسؤولين تكوين كل عنصر قائمة بشكل فردي للتحكم في مكان وزمان قيام تطبيق المستودع بتقديم النظرة العامة على بنود الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="a2d39-110">Admins can configure each menu item individually to control how, when, and where the warehouse app presents the pick line overview.</span></span>

## <a name="turn-on-the-work-pick-line-overview-feature"></a><span data-ttu-id="a2d39-111">تشغيل ميزة النظرة العامة على بنود انتقاء العمل</span><span class="sxs-lookup"><span data-stu-id="a2d39-111">Turn on the Work pick line overview feature</span></span>

<span data-ttu-id="a2d39-112">قبل أن تتمكن من استخدام هذه الميزة، يجب تشغيلها في النظام.</span><span class="sxs-lookup"><span data-stu-id="a2d39-112">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="a2d39-113">يمكن للمسؤولين استخدام إعدادات [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها إذا كانت مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="a2d39-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="a2d39-114">في مساحة عمل **إدارة الميزات**، تكون هذه الميزة مدرجة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="a2d39-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="a2d39-115">**الوحدة:** _إدارة المستودعات_</span><span class="sxs-lookup"><span data-stu-id="a2d39-115">**Module:** _Warehouse management_</span></span>
- <span data-ttu-id="a2d39-116">**اسم الميزة:** _نظرة عامة على بنود انتقاء العمل_</span><span class="sxs-lookup"><span data-stu-id="a2d39-116">**Feature name:** _Work pick line overview_</span></span>

## <a name="configure-menu-items-to-show-a-list-of-all-work-lines"></a><span data-ttu-id="a2d39-117">تكوين عناصر القائمة لإظهار قائمة بكافة بنود العمل</span><span class="sxs-lookup"><span data-stu-id="a2d39-117">Configure menu items to show a list of all work lines</span></span>

<span data-ttu-id="a2d39-118">لإعداد عنصر قائمة جهاز محمول لتوفير نظرة عامة على بنود الانتقاء، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="a2d39-118">To set up a mobile device menu item to provide a pick line overview, follow these steps.</span></span>

1. <span data-ttu-id="a2d39-119">انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> عناصر قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="a2d39-119">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="a2d39-120">حدد أو أنشئ عنصر قائمة يرتبط بعمل الانتقاء، ثم قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="a2d39-120">Select or create a menu item that is related to picking work, and set the following values:</span></span>

    - <span data-ttu-id="a2d39-121">**الوضع:** *العمل*</span><span class="sxs-lookup"><span data-stu-id="a2d39-121">**Mode:** *Work*</span></span>
    - <span data-ttu-id="a2d39-122">**استخدام العمل الموجود:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="a2d39-122">**Use existing work:** *Yes*</span></span>
    - <span data-ttu-id="a2d39-123">**موجّه بواسطة:** *موجّه بواسطة المستخدم* أو *موجّه بواسطة النظام*</span><span class="sxs-lookup"><span data-stu-id="a2d39-123">**Directed by:** *User directed* or *System directed*</span></span>

    <span data-ttu-id="a2d39-124">لمزيد من المعلومات حول كيفية إنشاء عناصر القائمة واستخدام الإعدادات المختلفة المتوفرة في صفحة **عناصر قائمة الجهاز المحمول**، راجع [إعداد الأجهزة المحمولة لعمل المستودع](configure-mobile-devices-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="a2d39-124">For more information about how to create menu items and use the various settings that are available on the **Mobile device menu items** page, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>

1. <span data-ttu-id="a2d39-125">على علامة التبويب السريعة **عام**، قم بتكوين الميزة عن طريق إعداد الحقل **إظهار قائمة بنود العمل** إلى إحدى القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="a2d39-125">On the **General** FastTab, configure the feature by setting the **Show work line list** field to one of the following values:</span></span>

    - <span data-ttu-id="a2d39-126">**العرض فقط عند الطلب** – يستطيع العاملون اختيار رؤية قائمة الانتقاء عن طريق تحديد الزر  **تخطي إلى** في تطبيق المستودع.</span><span class="sxs-lookup"><span data-stu-id="a2d39-126">**Show only upon request** – Workers can choose to view the pick line list by selecting the **Skip to** button in the warehouse app.</span></span>
    - <span data-ttu-id="a2d39-127">**إظهار في بداية كل انتقاء** – يرى العاملون القائمة في كل مرة يبدأون فيها أو يكملون بند انتقاء.</span><span class="sxs-lookup"><span data-stu-id="a2d39-127">**Show at the start of every pick** – Workers see the list every time that they start or finish a pick line.</span></span> <span data-ttu-id="a2d39-128">كما يمكنهم عرض القائمة مرة أخرى بتحديد الزر **تخطي إلى** في تطبيق المستودع.</span><span class="sxs-lookup"><span data-stu-id="a2d39-128">They can also view the list again by selecting the **Skip to** button in the warehouse app.</span></span>
    - <span data-ttu-id="a2d39-129">**إظهار في بداية الانتقاء الأول فقط** – يري العاملون القائمة في كل مرة يبدأون عمل الانتقاء الجديد، ولكن ليس بعد كل بند</span><span class="sxs-lookup"><span data-stu-id="a2d39-129">**Show at the start of the first pick only** – Workers see the list every time that they start new picking work, but not after each line.</span></span> <span data-ttu-id="a2d39-130">كما يمكنهم عرض القائمة مرة أخرى بتحديد الزر **تخطي إلى** في تطبيق المستودع.</span><span class="sxs-lookup"><span data-stu-id="a2d39-130">They can also view the list again by selecting the **Skip to** button in the warehouse app.</span></span>
    - <span data-ttu-id="a2d39-131">**عدم العرض مطلقًا** – يظهر الزر **تخطي** القياسي في تطبيق المستودع، ويكون عرض قائمة بنود العمل متوقفًا.</span><span class="sxs-lookup"><span data-stu-id="a2d39-131">**Never show** – The standard **Skip** button appears in the warehouse app, and display of the work line list is turned off.</span></span> <span data-ttu-id="a2d39-132">يسمح الزر **تخطي** للعاملين بالتنقل عبر البنود كل بند على حدة، بترتيب ثابت.‬</span><span class="sxs-lookup"><span data-stu-id="a2d39-132">The **Skip** button lets workers cycle through the lines one at a time, in a fixed order.</span></span> <span data-ttu-id="a2d39-133">كما يمكنهم التنقل عبر القائمة بالقدر الذي يحتاجون إليه، إلى أن تتم معالجة كافة البنود.</span><span class="sxs-lookup"><span data-stu-id="a2d39-133">They can also cycle through the list as many times as they require, until all lines have been processed.</span></span>

1. <span data-ttu-id="a2d39-134">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="a2d39-134">On the Action Pane, select **Save**.</span></span>

    <span data-ttu-id="a2d39-135">إذا قمت بتعيين الحقل **إظهار قائمة بنود العمل** إلى أي قيمة  باستثناء *عدم العرض مطلقًا*، يصبح الزر **قائمة الحقول** على جزء الإجراءات متوفرًا.</span><span class="sxs-lookup"><span data-stu-id="a2d39-135">If you set the **Show work line list** field to any value except *Never show*, the **Field list** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="a2d39-136">في جزء الإجراءات، حدد **قائمة الحقول**.</span><span class="sxs-lookup"><span data-stu-id="a2d39-136">On the Action Pane, select **Field list**.</span></span>
1. <span data-ttu-id="a2d39-137">في الصفحة **قائمة الحقول**، قم بتكوين المعلومات التي يعرضها تطبيق المستودع لكل بند في القائمة.</span><span class="sxs-lookup"><span data-stu-id="a2d39-137">On the **Field list** page, configure the information that the warehouse app shows for each line in the list.</span></span>

    - <span data-ttu-id="a2d39-138">يتم دائمًا تعيين الحقل **عنصر التحكم الأساسي** إلى *LineNum*.</span><span class="sxs-lookup"><span data-stu-id="a2d39-138">The **Primary control** field is always set to *LineNum*.</span></span> <span data-ttu-id="a2d39-139">وبالتالي، يبدأ كل صف في القائمة برقم بند.</span><span class="sxs-lookup"><span data-stu-id="a2d39-139">Therefore, each row in the list begins with a line number.</span></span>
    - <span data-ttu-id="a2d39-140">استخدم حقول **حقل العرض** المتبقية لإضافة ما يصل إلى سبعة حقول عرض إضافية، وفق احتياجاتك.</span><span class="sxs-lookup"><span data-stu-id="a2d39-140">Use the remaining **Display field** fields to add up to seven additional display fields, as you require.</span></span> <span data-ttu-id="a2d39-141">في كل حقل **حقل العرض**، حدد اسم حقل بند العمل.</span><span class="sxs-lookup"><span data-stu-id="a2d39-141">In each **Display field** field, select the name of a work line field.</span></span> <span data-ttu-id="a2d39-142">سيقوم كل بند بعد ذلك بإظهار قيمة لهذا الحقل.</span><span class="sxs-lookup"><span data-stu-id="a2d39-142">Each line will then show a value for that field.</span></span> <span data-ttu-id="a2d39-143">ستظهر القيم بحسب ترتيب تحديدها.</span><span class="sxs-lookup"><span data-stu-id="a2d39-143">The values will be shown in the order that you select here.</span></span> <span data-ttu-id="a2d39-144">يمكنك ترك بعض حقول **حقل العرض** فارغة إذا لم تطلب القيم السبع كلها.</span><span class="sxs-lookup"><span data-stu-id="a2d39-144">You can leave some of the **Display field** fields blank if you don't require all seven values.</span></span>

1. <span data-ttu-id="a2d39-145">في جزء الإجراءات، حدد **حفظ**، ثم أغلق صفحة **قائمة الحقول**.</span><span class="sxs-lookup"><span data-stu-id="a2d39-145">On the Action Pane, select **Save**, and then close the **Field list** page.</span></span>
