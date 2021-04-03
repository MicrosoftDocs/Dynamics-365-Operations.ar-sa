---
title: حساب القدرة الإنتاجية
description: يشرح هذا الموضوع كيفية حساب القدرة الإنتاجية في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetCapacityLoad, EntAssetWorkOrderCapacityLoadCalculate, EntAssetWorkOrderCapacityLoad
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7a9b235ecedf3399c79ee081a9fe7e2423045fa5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260048"
---
# <a name="calculate-capacity-load"></a><span data-ttu-id="f481c-103">حساب القدرة الإنتاجية</span><span class="sxs-lookup"><span data-stu-id="f481c-103">Calculate capacity load</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="f481c-104">في إدارة الأصول، يمكنك حساب القدرة الإنتاجية على:</span><span class="sxs-lookup"><span data-stu-id="f481c-104">In Asset Management, you can calculate capacity load on:</span></span>

- <span data-ttu-id="f481c-105">بنود جدول الصيانة</span><span class="sxs-lookup"><span data-stu-id="f481c-105">maintenance schedule lines</span></span>  
- <span data-ttu-id="f481c-106">أوامر العمل التي لم تتم جدولتها بعد</span><span class="sxs-lookup"><span data-stu-id="f481c-106">work orders that have not yet been scheduled</span></span>  
- <span data-ttu-id="f481c-107">أوامر العمل المجدولة</span><span class="sxs-lookup"><span data-stu-id="f481c-107">scheduled work orders</span></span>

<span data-ttu-id="f481c-108">يعتبر هذا الأمر مفيدًا إذا أردت الحصول على نظرة عامة على القدرة الإنتاجية المتوقعة لفترة محددة.</span><span class="sxs-lookup"><span data-stu-id="f481c-108">This is useful if you want to get an overview of expected capacity load for a specific period.</span></span> <span data-ttu-id="f481c-109">يمكن حساب القدرة الإنتاجية على جميع الأصول أو أصول محددة.</span><span class="sxs-lookup"><span data-stu-id="f481c-109">Calculation of capacity load can be done on all assets or selected assets.</span></span> <span data-ttu-id="f481c-110">يمكنك أيضًا إجراء الحساب على أنشطه وقت تعطل الصيانة أو مجموعات أوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="f481c-110">You can also make a calculation on maintenance downtime activities or work order pools.</span></span>

1. <span data-ttu-id="f481c-111">انقر فوق **إدارة الأصول** > **استعلامات** > **القدرة الإنتاجية‬**، أو **إدارة الأصول** > **عام** > **مجموعات أوامر العمل‬** > **جميع مجموعات أوامر العمل** / **مجموعات أوامر العمل النشطة** > حدد مجموعة أوامر العمل في القائمة > الزر **القدرة الإنتاجية**، أو **إدارة الأصول** > **عام‏‎** > **أنشطة وقت تعطل الصيانة‬‏‫** > **جميع أنشطة وقت تعطل الصيانة‬‏‫** / **أنشطة وقت تعطل الصيانة‬‏‫ النشطة** > حدد نشاط وقت تعطل الصيانة في القائمة‬‏‫ > الزر **القدرة الإنتاجية**.</span><span class="sxs-lookup"><span data-stu-id="f481c-111">Click **Asset management** > **Inquiries** > **Capacity load**, or **Asset management** > **Common** > **Work order pools** > **All work order pools** / **Active work order pools** > select work order pool in the list > **Capacity load** button, or **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** / **Active maintenance downtime activities** > select maintenance activity in the list > **Capacity load** button.</span></span>

2. <span data-ttu-id="f481c-112">في مربع الحوار **حساب القدرة الإنتاجية**، حدد فترة زمنية للحساب في الحقلين **تاريخ/وقت البدء** و **تاريخ/وقت الانتهاء**.</span><span class="sxs-lookup"><span data-stu-id="f481c-112">In the **Calculate capacity load** dialog, select a period for the calculation in the **Start date/time** and **End date/time** fields.</span></span>

3. <span data-ttu-id="f481c-113">حدد "نعم" على زر التبديل **تضمين جدول الصيانة** إذا أردت تضمين بنود جدول الصيانة في الحساب.</span><span class="sxs-lookup"><span data-stu-id="f481c-113">Select "Yes" on the **Include maintenance schedule** toggle button if you want to include maintenance schedule lines in the calculation.</span></span>

4. <span data-ttu-id="f481c-114">حدد "نعم" على زر التبديل **تضمين أمر العمل** إذا أردت تضمين وظائف أمر العمل في الحساب.</span><span class="sxs-lookup"><span data-stu-id="f481c-114">Select "Yes" on the **Include work order** toggle button if you want to include work order jobs in the calculation.</span></span>

5. <span data-ttu-id="f481c-115">يمكنك استخدام حقل **المستوى** للإشارة إلى مستوى التفصيل الذي ترغب فيه في بنود حساب فيما يتعلق بمواقع العمل.</span><span class="sxs-lookup"><span data-stu-id="f481c-115">You can use the **Level** field to indicate how detailed you want the capacity load lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="f481c-116">على سبيل المثال، إذا قمت بإدراج الرقم "1" في الحقل، وكان لديك بنية موقع عمل متعدد المستويات، فستظهر جميع بنود جدول الصيانة وأوامر العمل لموقع عمل في المستوى العلوي، وبالتالي فإن الساعات على البند قد تُضاف من مواقع عمل موجودة في مستوى أدنى.</span><span class="sxs-lookup"><span data-stu-id="f481c-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines and work orders for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="f481c-117">إذا قمت بإدراج الرقم "0" في حقل **المستوى**، فسترى نتيجة مفصلة تعرض جميع بنود جدول الصيانة وجميع أوامر العمل على مستويات مواقع العمل التي ترتبط بها.</span><span class="sxs-lookup"><span data-stu-id="f481c-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines and all work orders on all the functional location levels to which they are related.</span></span>

6. <span data-ttu-id="f481c-118">انقر فوق **موافق** لبدء الحساب.</span><span class="sxs-lookup"><span data-stu-id="f481c-118">Click **OK** to start the calculation.</span></span>

7. <span data-ttu-id="f481c-119">في مجموعات **تجميع حسب...** ، انقر فوق الأزرار ذات الصلة لإظهار مستوى التفاصيل المطلوب للحساب.</span><span class="sxs-lookup"><span data-stu-id="f481c-119">In the **Group by...** groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="f481c-120">في لقطه الشاشة أدناه، يتم تمييز الأزرار **تجميع حسب** المحددة باللون الأزرق.</span><span class="sxs-lookup"><span data-stu-id="f481c-120">In the screenshot below, the selected **Group by** buttons are highlighted in blue color.</span></span> <span data-ttu-id="f481c-121">انقر فوق زر لتنشيطه أو إلغاء تنشيطه.</span><span class="sxs-lookup"><span data-stu-id="f481c-121">Click on a button to activate or deactivate it.</span></span>

    ![الشكل 1](media/01-capacity-planning.png)

>[!NOTE]
><span data-ttu-id="f481c-123">إذا أردت التركيز فقط على تخطيط القدرة الإنتاجية فيما يتعلق بأوامر العمل المجدولة، راجع [حساب القدرة الإنتاجية على أوامر العمل المجدولة](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).</span><span class="sxs-lookup"><span data-stu-id="f481c-123">If you want to focus only on capacity planning regarding scheduled work orders, see [Calculate capacity load on scheduled work orders](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]