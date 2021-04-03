---
title: إنشاء تقارير الاستهلاك‬
description: يشرح هذا الموضوع كيفية إنشاء تقارير الاستهلاك في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0cda21addfdc524537177740ebba6414ef8b4b96
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260000"
---
# <a name="create-consumption-reports"></a><span data-ttu-id="d496f-103">إنشاء تقارير الاستهلاك‬</span><span class="sxs-lookup"><span data-stu-id="d496f-103">Create consumption reports</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="d496f-104">عند إنشاء تسجيلات الاستهلاك وترحيلها على أوامر العمل في إدارة الأصول، يتوفر تقريران لعرض تفاصيل الاستهلاك.</span><span class="sxs-lookup"><span data-stu-id="d496f-104">When you've created and posted consumption registrations on work orders in Asset Management, two reports are available to display consumption details.</span></span>


## <a name="asset-consumption-report"></a><span data-ttu-id="d496f-105">تقرير استهلاك الأصول</span><span class="sxs-lookup"><span data-stu-id="d496f-105">Asset consumption report</span></span>

<span data-ttu-id="d496f-106">عند ترحيل الاستهلاك على أوامر العمل، يمكنك طباعة تقرير استهلاك الأصول.</span><span class="sxs-lookup"><span data-stu-id="d496f-106">When you have posted consumption on work orders, you can print an asset consumption report.</span></span> <span data-ttu-id="d496f-107">يعرض التقرير الساعات وتكاليف الساعات وتكاليف الأصناف والمصروفات المرحّلة على الأصول.</span><span class="sxs-lookup"><span data-stu-id="d496f-107">The report displays hours, hour costs, item costs, and expenses posted on assets.</span></span>

1. <span data-ttu-id="d496f-108">انقر فوق **إدارة الأصول** > **التقارير** > **الأصول** > **استهلاك الأصول**.</span><span class="sxs-lookup"><span data-stu-id="d496f-108">Click **Asset management** > **Reports** > **Assets** > **Asset consumption**.</span></span>

2. <span data-ttu-id="d496f-109">في مربع الحوار **استهلاك الأصول** ، حدد المعلمات ومستوى التفاصيل الذي تريد رؤيته من خلال تحديد **نعم** على أزرار التبديل ذات الصلة، وإدراج مستوى موقع عمل في القسم **إظهار** .</span><span class="sxs-lookup"><span data-stu-id="d496f-109">In the **Asset consumption** dialog, select the parameters and detail level you want to see by selecting **Yes** on the relevant toggle buttons, and inserting a functional location level in the **Show** section.</span></span>
    - <span data-ttu-id="d496f-110">يمكنك استخدام حقل **المستويات** للإشارة إلى مستوى التفصيل الذي ترغب فيه في بنود الصنف فيما يتعلق بمواقع العمل.</span><span class="sxs-lookup"><span data-stu-id="d496f-110">You can use the **Levels** field to indicate how detailed you want the asset lines to be regarding functional locations.</span></span> 
    
        <span data-ttu-id="d496f-111">على سبيل المثال، إذا قمت بإدراج الرقم "1" في الحقل، وكان لديك بنية موقع عمل متعدد المستويات، فستظهر جميع الأصول لموقع عمل في المستوى العلوي، وبالتالي فإن الساعات على البند قد تُضاف من مواقع عمل موجودة في مستوى أدنى.‬</span><span class="sxs-lookup"><span data-stu-id="d496f-111">For example, if you enter the number "1" in the field, and you have a multi-level functional location structure, all assets for a functional location will be shown on the top level, and therefore a line may be added up from functional locations located at a lower level.</span></span> 
        
        <span data-ttu-id="d496f-112">إذا قمت بإدخال الرقم "0" في حقل **المستويات** ، فسترى نتيجة مفصلة تعرض جميع الأصول على جميع مستويات مواقع العمل التي ترتبط بها.</span><span class="sxs-lookup"><span data-stu-id="d496f-112">If you enter the number "0" in the **Levels** field, you will see a detailed result showing all assets on all the functional location levels to which they are related.</span></span> 
        
    - <span data-ttu-id="d496f-113">حدد **نعم** على زر التبديل **المجموع على جميع الأصول الفرعية** لعرض مجاميع كل أصل فرعي في التقرير.</span><span class="sxs-lookup"><span data-stu-id="d496f-113">Select **Yes** on the **Sum on all sub assets** toggle button to see sums for each sub asset in the report.</span></span>

3. <span data-ttu-id="d496f-114">حدد فترة تاريخ في قسم **التواريخ**.</span><span class="sxs-lookup"><span data-stu-id="d496f-114">Select a date interval in the **Dates** section.</span></span>

4. <span data-ttu-id="d496f-115">على علامة التبويب السريعة **الوجهة**، حدد إذا كنت ترغب في عرض التقرير على الشاشة أو طباعته أو حفظه كملف أو بريد إلكتروني.</span><span class="sxs-lookup"><span data-stu-id="d496f-115">On the **Destination** FastTab, select if you want to display the report on screen, print it, or save it as a file or email.</span></span>

5. <span data-ttu-id="d496f-116">وإذا لزم الأمر، يمكنك تحديد أصول معينة ليتم عرضها في التقرير.</span><span class="sxs-lookup"><span data-stu-id="d496f-116">If required, you can select specific assets to be displayed in the report.</span></span> <span data-ttu-id="d496f-117">على علامة التبويب السريعة **السجلات المطلوب تضمينها‬**، انقر فوق **تصفية**، وأضف الأصول التي ترغب في تضمينها في التقرير.</span><span class="sxs-lookup"><span data-stu-id="d496f-117">On the **Records to include** FastTab, click **Filter**, and add the assets you want to include in the report.</span></span>

6. <span data-ttu-id="d496f-118">انقر فوق **موافق** لإنشاء التقرير.</span><span class="sxs-lookup"><span data-stu-id="d496f-118">Click **OK** to generate the report.</span></span>


## <a name="work-order-consumption-report"></a><span data-ttu-id="d496f-119">تقرير استهلاك أمر العمل</span><span class="sxs-lookup"><span data-stu-id="d496f-119">Work order consumption report</span></span>

<span data-ttu-id="d496f-120">عند ترحيل الاستهلاك على أوامر العمل، يمكنك طباعة تقرير استهلاك أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="d496f-120">When you have posted consumption on work orders, you can print a work order consumption report.</span></span> <span data-ttu-id="d496f-121">يعرض التقرير الساعات وتكاليف الساعات وتكاليف الأصناف والمصروفات المرحّلة على أوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="d496f-121">The report displays hours, hour costs, item costs, and expenses posted on work orders.</span></span>

1. <span data-ttu-id="d496f-122">انقر فوق **إدارة الأصول** > **التقارير** > **أوامر العمل** > **استهلاك أمر العمل**.</span><span class="sxs-lookup"><span data-stu-id="d496f-122">Click **Asset management** > **Reports** > **Work orders** > **Work order consumption**.</span></span>

2. <span data-ttu-id="d496f-123">في مربع الحوار **استهلاك أمر العمل** ، حدد المعلمات التي تريد تضمينها في التقرير عن طريق تحديد **نعم** على أزرار التبديل ذات الصلة في القسم **إظهار** .</span><span class="sxs-lookup"><span data-stu-id="d496f-123">In the **Work order consumption** dialog, select the parameters you want to include in the report by selecting **Yes** on the relevant toggle buttons in the **Show** section.</span></span>

3. <span data-ttu-id="d496f-124">حدد فترة تاريخ في قسم **التواريخ**.</span><span class="sxs-lookup"><span data-stu-id="d496f-124">Select a date interval in the **Dates** section.</span></span>

4. <span data-ttu-id="d496f-125">على علامة التبويب السريعة **الوجهة**، حدد إذا كنت ترغب في عرض التقرير على الشاشة أو طباعته أو حفظه كملف أو بريد إلكتروني.</span><span class="sxs-lookup"><span data-stu-id="d496f-125">On the **Destination** FastTab, select if you want to display the report on screen, print it, or save it as a file or email.</span></span>

5. <span data-ttu-id="d496f-126">وإذا لزم الأمر، يمكنك تحديد أوامر عمل معينة ليتم عرضها في التقرير.</span><span class="sxs-lookup"><span data-stu-id="d496f-126">If required, you can select specific work orders to be displayed in the report.</span></span> <span data-ttu-id="d496f-127">على علامة التبويب السريعة **السجلات المطلوب تضمينها‬**، انقر فوق **تصفية**، وأضف أوامر العمل التي ترغب في تضمينها في التقرير.</span><span class="sxs-lookup"><span data-stu-id="d496f-127">On the **Records to include** FastTab, click **Filter**, and add the work orders you want to include in the report.</span></span>

6. <span data-ttu-id="d496f-128">انقر فوق **موافق** لإنشاء التقرير.</span><span class="sxs-lookup"><span data-stu-id="d496f-128">Click **OK** to generate the report.</span></span>


>[!NOTE]
><span data-ttu-id="d496f-129">يمكنك أيضًا إنشاء [تقرير أمر عمل](../work-orders/work-order-report.md)، يحتوي على مزيد من التفاصيل المتعلقة بأمر العمل.</span><span class="sxs-lookup"><span data-stu-id="d496f-129">You can also generate a [work order report](../work-orders/work-order-report.md), which contains more work order details.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]