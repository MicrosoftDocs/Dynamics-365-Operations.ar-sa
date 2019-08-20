---
title: إنشاء تخطيط مستودع جديد
description: يوضح هذا الإجراء كيفية إعداد معلومات حول المواقع الموجودة في مستودع.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f0a52c5d68816a81a94db019387b9ea3ec3efc5a
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845512"
---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="c99b5-103">إنشاء تخطيط مستودع جديد</span><span class="sxs-lookup"><span data-stu-id="c99b5-103">Create a new warehouse layout</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c99b5-104">يوضح هذا الإجراء كيفية إعداد معلومات حول المواقع الموجودة في مستودع.</span><span class="sxs-lookup"><span data-stu-id="c99b5-104">This procedure shows you how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="c99b5-105">ينطبق هذا فقط على المستودعات التي تم إنشاؤها باستخدام "التخزين الأساسي" في الوحدة النمطية لإدارة المخزون، وليس على المستودعات التي تم إنشاؤها في الوحدة النمطية لإدارة المستودعات.</span><span class="sxs-lookup"><span data-stu-id="c99b5-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="c99b5-106">يمكنك استخدام هذا الإجراء في شركة بيانات العرض التوضيحي USMF أو باستخدام بياناتك الخاصة.</span><span class="sxs-lookup"><span data-stu-id="c99b5-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="c99b5-107">تعيين سعة الموقع الافتراضي</span><span class="sxs-lookup"><span data-stu-id="c99b5-107">Set the default location capacity</span></span>
1. <span data-ttu-id="c99b5-108">انتقل إلى إدارة المخزون > الإعداد > معلمات إدارة المستودعات والمخزون‬.</span><span class="sxs-lookup"><span data-stu-id="c99b5-108">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="c99b5-109">انقر فوق علامة التبويب "المواقع".</span><span class="sxs-lookup"><span data-stu-id="c99b5-109">Click the Locations tab.</span></span>
3. <span data-ttu-id="c99b5-110">أدخل رقمًا في الحقل "العرض القياسي‬".</span><span class="sxs-lookup"><span data-stu-id="c99b5-110">In the Standard width field, enter a number.</span></span>
4. <span data-ttu-id="c99b5-111">أدخل رقمًا في الحقل "العمق القياسي‬".</span><span class="sxs-lookup"><span data-stu-id="c99b5-111">In the Standard depth field, enter a number.</span></span>
5. <span data-ttu-id="c99b5-112">أدخل رقمًا في الحقل "الارتفاع القياسي‬".</span><span class="sxs-lookup"><span data-stu-id="c99b5-112">In the Standard height field, enter a number.</span></span>
6. <span data-ttu-id="c99b5-113">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="c99b5-113">Click Save.</span></span>
7. <span data-ttu-id="c99b5-114">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c99b5-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="c99b5-115">تحديد تنسيق اسم الموقع</span><span class="sxs-lookup"><span data-stu-id="c99b5-115">Define the location name format</span></span>
1. <span data-ttu-id="c99b5-116">انتقل إلى إدارة المخزون > إعداد > تصنيف المخزون > المستودعات.</span><span class="sxs-lookup"><span data-stu-id="c99b5-116">Go to Inventory management > Setup > Inventory breakdown > Warehouses.</span></span>
2. <span data-ttu-id="c99b5-117">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="c99b5-117">Click New.</span></span>
3. <span data-ttu-id="c99b5-118">في الحقل "المستودع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c99b5-118">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="c99b5-119">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c99b5-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="c99b5-120">في الحقل "الموقع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="c99b5-120">In the Site field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="c99b5-121">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c99b5-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="c99b5-122">بدّل توسيع المقطع "أسماء المواقع".</span><span class="sxs-lookup"><span data-stu-id="c99b5-122">Toggle the expansion of the Location names section.</span></span>
    * <span data-ttu-id="c99b5-123">الخيارات في هذا القسم تحديد التنسيق الافتراضي لأسماء المواقع.</span><span class="sxs-lookup"><span data-stu-id="c99b5-123">The options in this section define the default format for location names.</span></span> <span data-ttu-id="c99b5-124">في هذا المثال، سوف ندرج رقم الممر ورقم الحامل ورقم الرف.</span><span class="sxs-lookup"><span data-stu-id="c99b5-124">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
8. <span data-ttu-id="c99b5-125">قم بتعيين خيار "تضمين الممر‬" إلى "نعم".</span><span class="sxs-lookup"><span data-stu-id="c99b5-125">Set the Include aisle option to Yes.</span></span>
9. <span data-ttu-id="c99b5-126">قم بتعيين خيار "تضمين الحامل‬‬" إلى "نعم".</span><span class="sxs-lookup"><span data-stu-id="c99b5-126">Set the Include rack option to Yes.</span></span> 
10. <span data-ttu-id="c99b5-127">في حقل "التنسيق" للحامل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c99b5-127">In the Format field, for the rack, type a value.</span></span>
    * <span data-ttu-id="c99b5-128">على سبيل المثال: -##</span><span class="sxs-lookup"><span data-stu-id="c99b5-128">For example: -##</span></span>  
11. <span data-ttu-id="c99b5-129">قم بتعيين خيار "تضمين الرف" إلى "نعم".</span><span class="sxs-lookup"><span data-stu-id="c99b5-129">Set the Include shelf option to Yes.</span></span>
12. <span data-ttu-id="c99b5-130">في حقل "التنسيق" للرف، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c99b5-130">In the Format field, for the shelf, type a value.</span></span>
    * <span data-ttu-id="c99b5-131">على سبيل المثال: -##</span><span class="sxs-lookup"><span data-stu-id="c99b5-131">For example: -##</span></span>  

## <a name="define-warehouse-locations"></a><span data-ttu-id="c99b5-132">تحديد مواقع المستودعات</span><span class="sxs-lookup"><span data-stu-id="c99b5-132">Define warehouse locations</span></span>
1. <span data-ttu-id="c99b5-133">في جزء الإجراءات، انقر فوق "مستودع".</span><span class="sxs-lookup"><span data-stu-id="c99b5-133">On the Action Pane, click Warehouse.</span></span>
2. <span data-ttu-id="c99b5-134">انقر فوق "معالج المواقع".</span><span class="sxs-lookup"><span data-stu-id="c99b5-134">Click Location Wizard.</span></span>
3. <span data-ttu-id="c99b5-135">انقر فوق التالي.</span><span class="sxs-lookup"><span data-stu-id="c99b5-135">Click Next.</span></span>
4. <span data-ttu-id="c99b5-136">إلغاء تحديد خيار المساحات الخارجية</span><span class="sxs-lookup"><span data-stu-id="c99b5-136">De-select the Outbound docks option</span></span>
5. <span data-ttu-id="c99b5-137">إلغاء تحديد خيار مواقع الكميات الكبيرة</span><span class="sxs-lookup"><span data-stu-id="c99b5-137">De-select the Bulk locations option</span></span>
6. <span data-ttu-id="c99b5-138">انقر فوق التالي.</span><span class="sxs-lookup"><span data-stu-id="c99b5-138">Click Next.</span></span>
7. <span data-ttu-id="c99b5-139">انقر فوق التالي.</span><span class="sxs-lookup"><span data-stu-id="c99b5-139">Click Next.</span></span>
8. <span data-ttu-id="c99b5-140">انقر فوق التالي.</span><span class="sxs-lookup"><span data-stu-id="c99b5-140">Click Next.</span></span>
9. <span data-ttu-id="c99b5-141">انقر فوق التالي.</span><span class="sxs-lookup"><span data-stu-id="c99b5-141">Click Next.</span></span>
10. <span data-ttu-id="c99b5-142">انقر فوق التالي.</span><span class="sxs-lookup"><span data-stu-id="c99b5-142">Click Next.</span></span>
11. <span data-ttu-id="c99b5-143">انقر فوق التالي.</span><span class="sxs-lookup"><span data-stu-id="c99b5-143">Click Next.</span></span>
12. <span data-ttu-id="c99b5-144">انقر فوق التالي.</span><span class="sxs-lookup"><span data-stu-id="c99b5-144">Click Next.</span></span>
    * <span data-ttu-id="c99b5-145">لاحظ أن الأبعاد الفعلية على هذه الصفحة هي تلك التي قمت بتعيينها في بداية هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="c99b5-145">Note that the physical dimensions shown on this page are the ones that you set at the start of this procedure.</span></span>  
13. <span data-ttu-id="c99b5-146">انقر فوق التالي.</span><span class="sxs-lookup"><span data-stu-id="c99b5-146">Click Next.</span></span>
14. <span data-ttu-id="c99b5-147">انقر فوق إنهاء.</span><span class="sxs-lookup"><span data-stu-id="c99b5-147">Click Finish.</span></span>
15. <span data-ttu-id="c99b5-148">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c99b5-148">Close the page.</span></span>
16. <span data-ttu-id="c99b5-149">قم بتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c99b5-149">Refresh the page.</span></span>

