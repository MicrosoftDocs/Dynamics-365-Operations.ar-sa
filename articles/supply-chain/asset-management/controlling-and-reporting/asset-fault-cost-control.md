---
title: التحكم في تكاليف خطأ الأصل
description: يشرح هذا الموضوع مراقبة تكاليف أخطاء الأصول في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bade6ffa5d5a9af6d23d0d681c32e72eb62d4ecc
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205519"
---
# <a name="asset-fault-cost-control"></a><span data-ttu-id="4dc04-103">التحكم في تكاليف خطأ الأصل</span><span class="sxs-lookup"><span data-stu-id="4dc04-103">Asset fault cost control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="4dc04-104">في إدارة الأصول، يمكنك حساب التكاليف في تسجيلات أخطاء الأصل للحصول عل نظرة عامة على التكاليف الفعلية مقارنة بتكاليف الموازنة.</span><span class="sxs-lookup"><span data-stu-id="4dc04-104">In Asset Management, you can calculate costs on asset fault registrations to get an overview of actual costs compared to budget costs.</span></span> <span data-ttu-id="4dc04-105">تستند التكاليف الفعلية إلى الحركات المرحّلة.</span><span class="sxs-lookup"><span data-stu-id="4dc04-105">Actual costs are based on posted transactions.</span></span> <span data-ttu-id="4dc04-106">التاريخ هو تاريخ الخطأ الذي تم فيه تسجيل العَرَض.</span><span class="sxs-lookup"><span data-stu-id="4dc04-106">The date is the fault date on which the symptom was recorded.</span></span>

1. <span data-ttu-id="4dc04-107">انقر فوق **إدارة الأصول** > **استعلامات‬** > **خطأ الأصل** > **مراقبة تكاليف أخطاء الأصول‏‎**.</span><span class="sxs-lookup"><span data-stu-id="4dc04-107">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault cost control**.</span></span>

2. <span data-ttu-id="4dc04-108">في مربع الحوار **مراقبة تكاليف أخطاء الأصول**، حدد مجموعة أبعاد مالية لتضمينها في الحساب، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="4dc04-108">In the **Asset fault cost control** dialog, select a financial dimension set to be included in the calculation, if required.</span></span>

4. <span data-ttu-id="4dc04-109">حدد "نعم" على زر التبديل **تخطي الصفر** إذا لم ترغب في إظهار النتائج ذات تكلفة صفرية.</span><span class="sxs-lookup"><span data-stu-id="4dc04-109">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="4dc04-110">يمكنك استخدام حقل **المستوى** للإشارة إلى مستوى التفصيل الذي ترغب فيه في بنود مراقبة التكاليف فيما يتعلق بمواقع العمل.</span><span class="sxs-lookup"><span data-stu-id="4dc04-110">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="4dc04-111">على سبيل المثال، إذا قمت بإدراج الرقم "1" في الحقل، وكان لديك بنية موقع عمل متعدد المستويات، فستظهر جميع بنود مراقبة تكاليف أخطاء الأصول لموقع عمل في المستوى العلوي، وبالتالي فإن الساعات على البند قد تُضاف من مواقع عمل موجودة في مستوى أدنى.</span><span class="sxs-lookup"><span data-stu-id="4dc04-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="4dc04-112">إذا قمت بإدراج الرقم "0" في حقل **المستوى**، فسترى نتيجة مفصلة تعرض جميع بنود مراقبة تكاليف أخطاء الأصول على جميع مستويات مواقع العمل التي ترتبط بها.</span><span class="sxs-lookup"><span data-stu-id="4dc04-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault cost control lines on all the functional location levels to which they are related.</span></span>

6. <span data-ttu-id="4dc04-113">إذا كنت ترغب في تقييد البحث، فيمكنك تحديد أصول معينة وتواريخ وأسباب أخطاء معينة على علامة التبويب السريعة **السجلات المطلوب تضمينها‬**.</span><span class="sxs-lookup"><span data-stu-id="4dc04-113">If you want to limit the search, you can select specific assets, fault dates, and fault causes on the **Records to include** FastTab.</span></span>

7. <span data-ttu-id="4dc04-114">انقر فوق **موافق** لبدء الحساب.</span><span class="sxs-lookup"><span data-stu-id="4dc04-114">Click **OK** to start the calculation.</span></span>

8. <span data-ttu-id="4dc04-115">انقر على الأزرار **تجميع حسب** لإظهار مستوى التفاصيل المطلوب للحساب.</span><span class="sxs-lookup"><span data-stu-id="4dc04-115">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="4dc04-116">يتم تمييز أزرار **تجميع حسب** المحددة.</span><span class="sxs-lookup"><span data-stu-id="4dc04-116">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="4dc04-117">انقر فوق زر لتنشيطه أو إلغاء تنشيطه.</span><span class="sxs-lookup"><span data-stu-id="4dc04-117">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="4dc04-118">مثال</span><span class="sxs-lookup"><span data-stu-id="4dc04-118">Example</span></span>

<span data-ttu-id="4dc04-119">يوضح هذا المثال حساب التحكم بتكلفة خطأ الأصل.</span><span class="sxs-lookup"><span data-stu-id="4dc04-119">This example shows an asset fault cost control calculation.</span></span>

- <span data-ttu-id="4dc04-120">يعرض حقل **الموازنة‏‎ الأصلية** تكاليف الموازنة من تنبؤ أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="4dc04-120">The **Original budget** field shows budget costs from the work order forecast.</span></span> 
- <span data-ttu-id="4dc04-121">يعرض حقل **التكلفة الفعلية** التكاليف التي تم ترحيلها على أوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="4dc04-121">The **Actual cost** field shows posted costs on work orders.</span></span> 
- <span data-ttu-id="4dc04-122">يعرض حقل **التكلفة الإلزامية** التكاليف الإجمالية التي تلتزم بها شركتك فيما يتعلق بأوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="4dc04-122">The **Committed cost** field shows total costs that your company is committed to in relation to work orders.</span></span>

    ![الشكل 1](media/05-controlling-and-reporting.png)

<span data-ttu-id="4dc04-124">للحصول على معلومات حول كيفية إعداد الأخطاء، راجع موضوع [إدارة الأخطاء](../setup-for-work-orders/fault-management.md) .</span><span class="sxs-lookup"><span data-stu-id="4dc04-124">For information about how to set up faults, see the [Fault management](../setup-for-work-orders/fault-management.md) topic.</span></span>
