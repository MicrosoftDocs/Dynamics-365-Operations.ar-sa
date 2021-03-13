---
title: حساب تنبؤ العنصر
description: يشرح هذا الموضوع كيفية حساب التنبؤ بالأصناف في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetItemForecast
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 155dc720804196ccc44fad5eaf71e3563a9c68cf
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/16/2021
ms.locfileid: "5022548"
---
# <a name="calculate-item-forecast"></a><span data-ttu-id="b84f2-103">حساب تنبؤ العنصر</span><span class="sxs-lookup"><span data-stu-id="b84f2-103">Calculate item forecast</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="b84f2-104">وتمامًا كما يمكنك حساب القدرة الإنتاجية، التي ورد وصفها في القسم السابق، يمكنك أيضًا حساب التنبؤات بالأصناف في:</span><span class="sxs-lookup"><span data-stu-id="b84f2-104">Just as you can make capacity load calculations, which are described in the previous section, you can also make item forecast calculations on:</span></span>

- <span data-ttu-id="b84f2-105">بنود جدول الصيانة</span><span class="sxs-lookup"><span data-stu-id="b84f2-105">maintenance schedule lines</span></span>  
- <span data-ttu-id="b84f2-106">أوامر العمل التي لم تتم جدولتها بعد</span><span class="sxs-lookup"><span data-stu-id="b84f2-106">work orders that have not yet been scheduled</span></span>  
- <span data-ttu-id="b84f2-107">أوامر العمل المجدولة</span><span class="sxs-lookup"><span data-stu-id="b84f2-107">scheduled work orders</span></span>

<span data-ttu-id="b84f2-108">يعتبر هذا الأمر مفيدًا إذا أردت الحصول على نظرة عامة على استهلاك الصنف المتوقع (قطع الغيار بالإضافة إلى الأصناف الأخرى المطلوبة لإكمال أوامر العمل) لفترة محددة.</span><span class="sxs-lookup"><span data-stu-id="b84f2-108">This is useful if you want to get an overview of expected item consumption (spare parts as well as other items required for completing work orders) for a specific period.</span></span> <span data-ttu-id="b84f2-109">يمكن حساب التنبؤ بالأصناف على جميع الأصول أو أصول محددة.</span><span class="sxs-lookup"><span data-stu-id="b84f2-109">Calculation of item forecast can be done on all assets or selected assets.</span></span> <span data-ttu-id="b84f2-110">يمكنك أيضًا إجراء عملية حسابية على نشاط وقت تعطل الصيانة (**جميع أنشطة وقت تعطل الصيانة** أو **أنشطة وقت تعطل الصيانة‬‏‫ النشطة**) أو على مجموعة أوامر عمل (**جميع مجموعات أوامر العمل** أو **مجموعات أوامر العمل النشطة**).</span><span class="sxs-lookup"><span data-stu-id="b84f2-110">You can also make a calculation on a maintenance downtime activity (**All maintenance downtime activities** or **Active maintenance downtime activities**), or on a work order pool (**All work order pools** or **Active work order pools**).</span></span>

1. <span data-ttu-id="b84f2-111">انقر فوق **إدارة الأصول** > **استعلامات** > **التنبؤ بالأصناف‬**، أو **إدارة الأصول** > **عام** > **مجموعات أوامر العمل‬** > **جميع مجموعات أوامر العمل** / **مجموعات أوامر العمل النشطة** > حدد مجموعة أوامر العمل في القائمة > الزر **التنبؤ بالأصناف**، أو **إدارة الأصول** > **عام‏‎** > **أنشطة وقت تعطل الصيانة‬‏‫** > **جميع أنشطة وقت تعطل الصيانة‬‏‫** / **أنشطة وقت تعطل الصيانة‬‏‫ النشطة** > حدد نشاط وقت تعطل الصيانة في القائمة‬‏‫ > الزر **التنبؤ بالأصناف**.</span><span class="sxs-lookup"><span data-stu-id="b84f2-111">Click **Asset management** > **Inquiries** > **Item forecast**, or **Asset management** > **Common** > **Work order pools** > **All work order pools** / **Active work order pools** > select work order pool in the list > **Item forecast** button, or **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** / **Active maintenance downtime activities** > select maintenance downtime activity in the list > **Item forecast** button.</span></span>

2. <span data-ttu-id="b84f2-112">في مربع الحوار **حساب التنبؤ بالأصناف**، حدد فترة زمنية للحساب في الحقلين **تاريخ/وقت البدء** و **تاريخ/وقت الانتهاء**.</span><span class="sxs-lookup"><span data-stu-id="b84f2-112">In the **Calculate item forecast** dialog, select a period for the calculation in the **Start date/time** and **End date/time** fields.</span></span>

3. <span data-ttu-id="b84f2-113">حدد "نعم" على زر التبديل **تضمين جدول الصيانة** إذا أردت تضمين بنود جدول الصيانة في حساب التنبؤ.</span><span class="sxs-lookup"><span data-stu-id="b84f2-113">Select "Yes" on the **Include maintenance schedule** toggle button if you want to include maintenance schedule lines in the forecast calculation.</span></span>

4. <span data-ttu-id="b84f2-114">حدد "نعم" على زر التبديل **تضمين أمر العمل** إذا أردت تضمين وظائف أمر العمل في حساب التنبؤ.</span><span class="sxs-lookup"><span data-stu-id="b84f2-114">Select "Yes" on the **Include work order** toggle button if you want to include work order jobs in the forecast calculation.</span></span>

5. <span data-ttu-id="b84f2-115">يمكنك استخدام حقل **المستوى** للإشارة إلى مستوى التفصيل الذي ترغب فيه في بنود التنبؤ بالأصناف فيما يتعلق بمواقع العمل.</span><span class="sxs-lookup"><span data-stu-id="b84f2-115">You can use the **Level** field to indicate how detailed you want the item forecast lines to be regarding functional locations.</span></span> 

      <span data-ttu-id="b84f2-116">على سبيل المثال، إذا قمت بإدراج الرقم "1" في الحقل، وكان لديك بنية موقع عمل متعدد المستويات، فستظهر جميع بنود جدول الصيانة وأوامر العمل لموقع عمل في المستوى العلوي، وبالتالي فإن الساعات على البند قد تُضاف من مواقع عمل موجودة في مستوى أدنى.</span><span class="sxs-lookup"><span data-stu-id="b84f2-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines and work orders for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
  
      <span data-ttu-id="b84f2-117">إذا قمت بإدراج الرقم "0" في حقل **المستوى**، فسترى نتيجة مفصلة تعرض جميع بنود جدول الصيانة وجميع أوامر العمل على مستوى مواقع العمل الذي ترتبط به.</span><span class="sxs-lookup"><span data-stu-id="b84f2-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines and all work orders on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="b84f2-118">انقر فوق **موافق** لبدء الحساب.</span><span class="sxs-lookup"><span data-stu-id="b84f2-118">Click **OK** to start the calculation.</span></span>

7. <span data-ttu-id="b84f2-119">في مجموعات **تجميع حسب...** ، انقر فوق الأزرار ذات الصلة لإظهار مستوى التفاصيل المطلوب للحساب.</span><span class="sxs-lookup"><span data-stu-id="b84f2-119">In the **Group by...** groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="b84f2-120">في لقطه الشاشة أدناه، يتم تمييز الأزرار **تجميع حسب** المحددة باللون الأزرق.</span><span class="sxs-lookup"><span data-stu-id="b84f2-120">In the screenshot below, the selected **Group by** buttons are highlighted in blue color.</span></span> <span data-ttu-id="b84f2-121">انقر فوق زر لتنشيطه أو إلغاء تنشيطه.</span><span class="sxs-lookup"><span data-stu-id="b84f2-121">Click on a button to activate or deactivate it.</span></span>

8. <span data-ttu-id="b84f2-122">انقر فوق الزر‏‎ **عرض الأبعاد‬** للاطلاع على أبعاد المنتج أو التخزين أو التعقب المرتبطة بالأصناف.</span><span class="sxs-lookup"><span data-stu-id="b84f2-122">Click the **Display dimensions** button if you want to see the product, storage, or tracking dimensions related to the items.</span></span> <span data-ttu-id="b84f2-123">حدد خانات الاختيار ذات الصلة، وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b84f2-123">Select the relevant check boxes, and click **OK**.</span></span>

![الشكل 1](media/02-capacity-planning.png)
