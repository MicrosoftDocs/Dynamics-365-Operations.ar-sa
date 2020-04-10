---
title: إنشاء تخطيط مستودع جديد
description: يصف هذا الموضوع كيفية إعداد المعلومات حول المواقع في مستودع.
author: perlynne
manager: AnnBe
ms.date: 07/29/2019
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
ms.openlocfilehash: 399c87c2e5ad26d5ccc1618cfb6520de3fcdc644
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145653"
---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="b8558-103">إنشاء تخطيط مستودع جديد</span><span class="sxs-lookup"><span data-stu-id="b8558-103">Create a new warehouse layout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b8558-104">يصف هذا الموضوع كيفية إعداد المعلومات حول المواقع في مستودع.</span><span class="sxs-lookup"><span data-stu-id="b8558-104">This topic describes how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="b8558-105">ينطبق هذا فقط على المستودعات التي تم إنشاؤها باستخدام "التخزين الأساسي" في الوحدة النمطية لإدارة المخزون، وليس على المستودعات التي تم إنشاؤها في الوحدة النمطية لإدارة المستودعات.</span><span class="sxs-lookup"><span data-stu-id="b8558-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="b8558-106">يمكنك استخدام هذا الإجراء في شركة بيانات العرض التوضيحي USMF أو باستخدام بياناتك الخاصة.</span><span class="sxs-lookup"><span data-stu-id="b8558-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="b8558-107">تعيين سعة الموقع الافتراضي</span><span class="sxs-lookup"><span data-stu-id="b8558-107">Set the default location capacity</span></span>
1. <span data-ttu-id="b8558-108">في جزء التنقل، انتقل إلى **الوحدات النمطية > إدارة المخزون > الإعداد > محددات إدارة المستودعات والمخزون‬**.</span><span class="sxs-lookup"><span data-stu-id="b8558-108">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory and warehouse management parameters**.</span></span>
2. <span data-ttu-id="b8558-109">حدد علامة تبويب **المواقع**:</span><span class="sxs-lookup"><span data-stu-id="b8558-109">Select the **Locations** tab.</span></span>
3. <span data-ttu-id="b8558-110">أدخل رقمًا في الحقل **العرض القياسي**.</span><span class="sxs-lookup"><span data-stu-id="b8558-110">In the **Standard width** field, enter a number.</span></span>
4. <span data-ttu-id="b8558-111">أدخل رقمًا في الحقل **العمق القياسي‬**.</span><span class="sxs-lookup"><span data-stu-id="b8558-111">In the **Standard depth** field, enter a number.</span></span>
5. <span data-ttu-id="b8558-112">أدخل رقمًا في الحقل **الارتفاع القياسي‬**.</span><span class="sxs-lookup"><span data-stu-id="b8558-112">In the **Standard height** field, enter a number.</span></span>
6. <span data-ttu-id="b8558-113">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="b8558-113">Select **Save**.</span></span>
7. <span data-ttu-id="b8558-114">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b8558-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="b8558-115">تحديد تنسيق اسم الموقع</span><span class="sxs-lookup"><span data-stu-id="b8558-115">Define the location name format</span></span>
1. <span data-ttu-id="b8558-116">في جزء التنقل، انتقل إلى **الوحدات النمطية > إدارة المخزون > الإعداد > تصنيف المخزون‬ > المستودعات**.</span><span class="sxs-lookup"><span data-stu-id="b8558-116">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory breakdown > Warehouses**.</span></span>
2. <span data-ttu-id="b8558-117">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="b8558-117">Select **New**.</span></span>
3. <span data-ttu-id="b8558-118">في الحقل **المستودع**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b8558-118">In the **Warehouse** field, type a value.</span></span>
4. <span data-ttu-id="b8558-119">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b8558-119">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="b8558-120">في حقل **الموقع**، حدد السجل المطلوب في البحث.</span><span class="sxs-lookup"><span data-stu-id="b8558-120">In the **Site** field, select the desired record in the lookup.</span></span>
6. <span data-ttu-id="b8558-121">بدّل توسيع القسم **أسماء المواقع**.</span><span class="sxs-lookup"><span data-stu-id="b8558-121">Toggle the expansion of the **Location names** section.</span></span> <span data-ttu-id="b8558-122">الخيارات في هذا القسم تحديد التنسيق الافتراضي لأسماء المواقع.</span><span class="sxs-lookup"><span data-stu-id="b8558-122">The options in this section define the default format for location names.</span></span> <span data-ttu-id="b8558-123">في هذا المثال، سوف ندرج رقم الممر ورقم الحامل ورقم الرف.</span><span class="sxs-lookup"><span data-stu-id="b8558-123">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
7. <span data-ttu-id="b8558-124">قم بتعيين خيار **تضمين الممر‬** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="b8558-124">Set the **Include aisle** option to **Yes**.</span></span>
8. <span data-ttu-id="b8558-125">قم بتعيين خيار **تضمين الحامل** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="b8558-125">Set the **Include rack** option to **Yes**.</span></span> 
9. <span data-ttu-id="b8558-126">في حقل **التنسيق** للحامل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b8558-126">In the **Format** field, for the rack, type a value.</span></span>
10. <span data-ttu-id="b8558-127">قم بتعيين خيار **تضمين الرف** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="b8558-127">Set the **Include shelf** option to **Yes**.</span></span>
11. <span data-ttu-id="b8558-128">في حقل **التنسيق** للرف، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b8558-128">In the **Format** field, for the shelf, type a value.</span></span>

## <a name="define-warehouse-locations"></a><span data-ttu-id="b8558-129">تحديد مواقع المستودعات</span><span class="sxs-lookup"><span data-stu-id="b8558-129">Define warehouse locations</span></span>
1. <span data-ttu-id="b8558-130">في جزء الإجراءات، حدد **المستودع**.</span><span class="sxs-lookup"><span data-stu-id="b8558-130">On the Action Pane, select **Warehouse**.</span></span>
2. <span data-ttu-id="b8558-131">حدد **معالج الموقع**.</span><span class="sxs-lookup"><span data-stu-id="b8558-131">Select **Location Wizard**.</span></span>
3. <span data-ttu-id="b8558-132">حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="b8558-132">Select **Next**.</span></span>
4. <span data-ttu-id="b8558-133">إلغاء تحديد الخيار **مساحات خارجية**</span><span class="sxs-lookup"><span data-stu-id="b8558-133">De-select the **Outbound docks** option</span></span>
5. <span data-ttu-id="b8558-134">إلغاء تحديد خيار **مواقع الكميات الكبيرة**</span><span class="sxs-lookup"><span data-stu-id="b8558-134">De-select the **Bulk locations** option</span></span>
6. <span data-ttu-id="b8558-135">حدد **التالي** إلى ان تصل إلى الخيار لتحديد **إنهاء.**</span><span class="sxs-lookup"><span data-stu-id="b8558-135">Select **Next** until you come to the option to select **Finish**.</span></span>
7. <span data-ttu-id="b8558-136">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b8558-136">Close the page.</span></span>
8. <span data-ttu-id="b8558-137">قم بتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b8558-137">Refresh the page.</span></span>

