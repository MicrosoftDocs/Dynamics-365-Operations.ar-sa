---
title: مراقبة ساعات العمل
description: يشرح هذا الموضوع مراقبة ساعات العمل في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetHourControl
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cc4382d72e032fdfad05f2077ffe8e41e64c6a55
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018461"
---
# <a name="work-hour-control"></a><span data-ttu-id="0025f-103">مراقبة ساعات العمل</span><span class="sxs-lookup"><span data-stu-id="0025f-103">Work hour control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="0025f-104">في إدارة الأصول، يمكنك حساب الساعات للحصول عل نظرة عامة على الساعات الفعلية مقارنةً بساعات الموازنة على الأصول أو مواقع العمل أو أوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="0025f-104">In Asset Management, you can calculate hours to get an overview of actual hours compared to budget hours on assets, functional locations, or work orders.</span></span> <span data-ttu-id="0025f-105">تستند الساعات الفعلية إلى الحركات المرحّلة.</span><span class="sxs-lookup"><span data-stu-id="0025f-105">Actual hours are based on posted transactions.</span></span>

## <a name="work-hour-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="0025f-106">مراقبة ساعات العمل للأصول ومواقع العمل وأوامر العمل</span><span class="sxs-lookup"><span data-stu-id="0025f-106">Work hour control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="0025f-107">تعتبر العمليات الحسابية التي يتم تنفيذها للأصول ومواقع العمل وأوامر العمل مماثلة تقريبًا.</span><span class="sxs-lookup"><span data-stu-id="0025f-107">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="0025f-108">الفرق الوحيد هو أنه يمكنك أيضًا تضمين أصول فرعية ومواقع فرعية في حسابك فيما يتعلق بالأصول ومواقع العمل.</span><span class="sxs-lookup"><span data-stu-id="0025f-108">Only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="0025f-109">التاريخ هو تاريخ الحركة عندما تم إنشاء التسجيل.</span><span class="sxs-lookup"><span data-stu-id="0025f-109">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="0025f-110">انقر فوق **إدارة الأصول** > **استعلامات** > **الأصول‏‎** > **مراقبة ساعات الأصول** أو **مراقبة ساعات مواقع العمل** أو **إدارة الأصول** > **استعلامات‏‎** > **أوامر العمل** > **مراقبة ساعات أوامر العمل**.</span><span class="sxs-lookup"><span data-stu-id="0025f-110">Click **Asset management** > **Inquiries** > **Assets** > **Asset hour control** or **Functional location hour control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order hour control**.</span></span>

2. <span data-ttu-id="0025f-111">في مربع الحوار **مراقبة ساعات الأصول**.</span><span class="sxs-lookup"><span data-stu-id="0025f-111">In the **Asset hour control** dialog, .</span></span>

3. <span data-ttu-id="0025f-112">في مربع الحوار **مراقبة ساعات الأصول** / **مراقبة ساعات مواقع العمل** / **مراقبة ساعات أوامر العمل**، حدد فترة ليتم حسابها في الحقلين **من تاريخ** و **إلى تاريخ**.</span><span class="sxs-lookup"><span data-stu-id="0025f-112">In the **Asset hour control** / **Functional location hour control** / **Work order hour control** dialog, select a period to be calculated in the **From date** and **To date** fields.</span></span>

4. <span data-ttu-id="0025f-113">إذا لزم الأمر، حدد **مجموعة أبعاد مالية** لتضمينها في الحساب.</span><span class="sxs-lookup"><span data-stu-id="0025f-113">If required, select a **Financial dimension set** to be included in the calculation.</span></span>

5. <span data-ttu-id="0025f-114">حدد "نعم" على زر التبديل **تخطي الصفر** إذا لم ترغب في إظهار النتائج التي تحتوي على صفر.</span><span class="sxs-lookup"><span data-stu-id="0025f-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results containing zero hours.</span></span>

6. <span data-ttu-id="0025f-115">يمكنك استخدام حقل **المستوى** للإشارة إلى مستوى التفصيل الذي ترغب فيه في بنود مراقبة الساعات فيما يتعلق بمواقع العمل.</span><span class="sxs-lookup"><span data-stu-id="0025f-115">You can use the **Level** field to indicate how detailed you want the hour control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="0025f-116">على سبيل المثال، إذا قمت بإدراج الرقم "1" في الحقل، وكان لديك تدرجًا هرميًا لموقع عمل متعدد المستويات، فستظهر جميع بنود مراقبة الساعات لموقع عمل في المستوى العلوي، وبالتالي فإن الساعات على البند قد تُضاف من مواقع عمل موجودة في مستوى أدنى.</span><span class="sxs-lookup"><span data-stu-id="0025f-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all hour control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="0025f-117">إذا قمت بإدراج الرقم "0" في حقل **المستوى**، فسترى نتيجة مفصلة تعرض جميع بنود مراقبة الساعات على جميع مستويات مواقع العمل التي ترتبط بها.</span><span class="sxs-lookup"><span data-stu-id="0025f-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all hour control lines on all the functional location levels to which they are related.</span></span>

7. <span data-ttu-id="0025f-118">حدد "نعم" على زر التبديل **تضمين الأصول الفرعية** لإظهار التكاليف المرتبطة بالأصول الفرعية كبنود منفصلة.</span><span class="sxs-lookup"><span data-stu-id="0025f-118">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="0025f-119">إذا كنت ترغب في تقييد البحث، فيمكنك تحديد أصول / مواقع عمل / أوامر عمل معينة على علامة التبويب السريعة **السجلات المطلوب تضمينها‬**.</span><span class="sxs-lookup"><span data-stu-id="0025f-119">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="0025f-120">انقر فوق **موافق** لبدء الحساب.</span><span class="sxs-lookup"><span data-stu-id="0025f-120">Click **OK** to start the calculation.</span></span>

10. <span data-ttu-id="0025f-121">في صفحة **مراقبة ساعات الأصول** ، انقر فوق الأزرار **تجميع حسب** لإظهار مستوى التفاصيل المطلوب للحساب.</span><span class="sxs-lookup"><span data-stu-id="0025f-121">On the **Asset hour control** page, click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="0025f-122">يتم تمييز أزرار **تجميع حسب** المحددة.</span><span class="sxs-lookup"><span data-stu-id="0025f-122">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="0025f-123">انقر فوق زر لتنشيطه أو إلغاء تنشيطه.</span><span class="sxs-lookup"><span data-stu-id="0025f-123">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="0025f-124">مثال</span><span class="sxs-lookup"><span data-stu-id="0025f-124">Example</span></span>

<span data-ttu-id="0025f-125">تعرض لقطة الشاشة أدناه مثالاً لحساب **مراقبة ساعات الأصول**.</span><span class="sxs-lookup"><span data-stu-id="0025f-125">The screenshot below shows an example of an **Asset hour control** calculation.</span></span>

- <span data-ttu-id="0025f-126">يعرض حقل **الموازنة‏‎ الأصلية** تكاليف الساعات من تنبؤ أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="0025f-126">The **Original budget** field shows budget hours from the work order forecast.</span></span> 
- <span data-ttu-id="0025f-127">يعرض حقل **التكلفة الفعلية** الساعات التي تم ترحيلها على أوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="0025f-127">The **Actual hours** field shows posted hours on work orders.</span></span> 
- <span data-ttu-id="0025f-128">يعرض حقل **الساعات الإلزامية** إجمالي عدد الساعات التي تلتزم بها شركتك فيما يتعلق بأوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="0025f-128">The **Committed hours** field shows total amount of hours that your company is committed to in relation to work orders.</span></span>

![مثال على حساب مراقبة ساعات الأصول](media/04-controlling-and-reporting.png)

<span data-ttu-id="0025f-130">ثمة طريقة أخرى لحساب الساعات وهي إجراء تحديدات متعددة للأصول في **كل الأصول** أو **الأصول‏‎ النشطة**.</span><span class="sxs-lookup"><span data-stu-id="0025f-130">Another way of making an hour calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="0025f-131">ثم انقر فوق زر **مراقبة الساعات** على علامة التبويب السريعة **عام**.</span><span class="sxs-lookup"><span data-stu-id="0025f-131">Then you click the **Hour control** button on the **General** FastTab.</span></span> <span data-ttu-id="0025f-132">يتم إدراج الأصول المحددة بشكل تلقائي في حقل **الأصل** على علامة التبويب السريعة **السجلات المطلوب تضمينها‬**.</span><span class="sxs-lookup"><span data-stu-id="0025f-132">The selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="0025f-133">انقر فوق **موافق** في مربع الحوار **مراقبة ساعات الأصول**، ويظهر حساب الأصول المحددة.</span><span class="sxs-lookup"><span data-stu-id="0025f-133">Click **OK** in the **Asset hour control** dialog, and the calculation for the selected assets is shown.</span></span> <span data-ttu-id="0025f-134">يمكن تنفيذ الإجراء نفسه لمواقع العمل في **جميع مواقع العمل** أو **مواقع العمل النشطة** ولأوامر العمل في **جميع أوامر العمل** أو **أوامر العمل النشطة**.</span><span class="sxs-lookup"><span data-stu-id="0025f-134">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>


