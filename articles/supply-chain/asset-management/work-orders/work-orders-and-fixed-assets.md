---
title: أوامر العمل والأصول الثابتة
description: يشرح هذا الموضوع أوامر العمل والأصول الثابتة في إدارة الأصول.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 95fe394d22f9fe81511c230a2cf7b8ddf00d896f
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250819"
---
# <a name="work-orders-and-fixed-assets"></a><span data-ttu-id="c1759-103">أوامر العمل والأصول الثابتة</span><span class="sxs-lookup"><span data-stu-id="c1759-103">Work orders and fixed assets</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="c1759-104">في إدارة الأصول، يمكن ربط الأصول بالأصول الثابتة، ويمكن إنشاء أوامر عمل لهذه الأصول.</span><span class="sxs-lookup"><span data-stu-id="c1759-104">In Asset Management, assets can be related to fixed assets, and you can create work orders for those assets.</span></span> <span data-ttu-id="c1759-105">إذا استخدمت هذه الوظيفة، يمكنك الحصول على نظرة عامة كاملة على الأصول الثابتة ومشاريع الاستثمار ذات الصلة والتكاليف المسجلة على مشاريع الاستثمار في الوحدة النمطية **إدارة المشاريع ومحاسبتها** والوحدة النمطية **الأصول الثابتة**.</span><span class="sxs-lookup"><span data-stu-id="c1759-105">If you use this functionality, you can get a complete overview of fixed assets, related investment projects, and the costs registered on the investment projects in the **Project management and accounting** module and the **Fixed assets** module.</span></span>

>[!NOTE]
><span data-ttu-id="c1759-106">يتم ملء حقل **رقم الأصل الثابت** فقط في مشروع وظيفة أمر العمل في حالة تحديد النوع "استثمار" كنوع المشروع في مشروع وظيفة أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="c1759-106">The **Fixed asset number** field is only filled out on the work order job project if type "Investment" is selected as the project type on the work order job project.</span></span>

![الشكل 1](media/24-work-orders.png)

<span data-ttu-id="c1759-108">يصف الإجراء التالي العلاقة بين الأصول وأوامر العمل ومشاريع وظائف أمر العمل والأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="c1759-108">The following procedure describes the relation between assets, work orders, work order job projects, and fixed assets.</span></span>

1. <span data-ttu-id="c1759-109">تقوم بإنشاء أصل تربطه بأصل ثابت، كما هو موضح في الشكل أدناه.</span><span class="sxs-lookup"><span data-stu-id="c1759-109">You create an asset that you relate to a fixed asset, as shown in the figure below.</span></span>

![الشكل 2](media/25-work-orders.png)

2. <span data-ttu-id="c1759-111">عند إعداد أنواع أوامر العمل (**إدارة الأصول** > **الإعداد** > **أوامر العمل** > **أنواع أوامر العمل**)، تنشئ نوع أمر عمل للتعامل مع الاستثمارات.</span><span class="sxs-lookup"><span data-stu-id="c1759-111">When you set up work order types (**Asset management** > **Setup** > **Work orders** > **Work order types**), you create a work order type for handling investments.</span></span> <span data-ttu-id="c1759-112">راجع أيضًا [أنواع أوامر العمل](../setup-for-work-orders/work-order-types.md).</span><span class="sxs-lookup"><span data-stu-id="c1759-112">See also [Work order types](../setup-for-work-orders/work-order-types.md).</span></span>

![الشكل 3](media/26-work-orders.png)

3. <span data-ttu-id="c1759-114">عندما تقوم بإعداد مجموعات مشاريع أوامر العمل (**إدارة الأصول** > **الإعداد** > **أوامر العمل** >  **إعداد المشروع** > الارتباط **مجموعة المشاريع**)، تنشئ علاقة بين نوع أمر العمل المستخدم للاستثمارات ومجموعة المشاريع التي تم إنشاؤها للاستثمارات في الوحدة النمطية **إدارة المشاريع ومحاسبتها** (**إدارة المشاريع ومحاسبتها** > **الإعداد** > **الترحيل** > **مجموعات المشاريع**).</span><span class="sxs-lookup"><span data-stu-id="c1759-114">When you set up work order project groups (**Asset management** > **Setup** > **Work orders** > **Project setup** > **Project group** link), you create a relation between the work order type used for investments and the project group created for investments in the **Project management and accounting** module (**Project management and accounting** > **Setup** > **Posting** > **Project groups**).</span></span>

![الشكل 4](media/27-work-orders.png)

4. <span data-ttu-id="c1759-116">عندما تنشئ أمر عمل يتعلق بكائن الأصل الثابت، فأنت تحدد نوع أمر العمل المستخدم للتعامل مع الاستثمارات، على سبيل المثال، "استثمار".</span><span class="sxs-lookup"><span data-stu-id="c1759-116">When you create a work order that relates to a fixed asset object, you select the work order type used for handling investments, for example, "Investment".</span></span>

5. <span data-ttu-id="c1759-117">عند إنشاء أمر العمل، يتم عرض نوع أمر العمل المرتبط في **جميع أوامر العمل‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="c1759-117">When the work order is created, the related work order type is shown in **All work orders**.</span></span>

![الشكل 5](media/28-work-orders.png)

6. <span data-ttu-id="c1759-119">عند إنشاء أمر العمل، يتم إنشاء المشروع المرتبط بأمر العمل في **إدارة المشاريع ومحاسبتها** > **جميع المشاريع**.</span><span class="sxs-lookup"><span data-stu-id="c1759-119">When the work order is created, the project related to the work order is created in **Project management and accounting** > **All projects**.</span></span> <span data-ttu-id="c1759-120">يمكنك الاطلاع على المعلومات ذات الصلة بالمشروع من خلال النقر فوق الارتباط **معرف المشروع**  على أمر العمل (في **إدارة الأصول**، افتح أمر العمل في طريقة عرض التفاصيل > علامة التبويب السريعة **تفاصيل البنود** > علامة التبويب السريعة **عام** > الحقل **معرف المشروع**).</span><span class="sxs-lookup"><span data-stu-id="c1759-120">You can see project-related information by clicking the **Project ID** link on the work order (in **Asset management**, open the work order in Details view > **Line details** FastTab > **General** tab > **Project ID** field).</span></span>

![الشكل 6](media/29-work-orders.png)

7. <span data-ttu-id="c1759-122">في **الأصول الثابتة**، يمكنك الاطلاع على نظرة عامة على المشاريع المقترنة بأصل ثابت (**الأصول الثابتة** > **الأصول الثابتة** > **الأصول الثابتة** > انقر فوق الأصل الثابت في حقل **رقم الأصل الثابت** > استعرض المحتويات في الجزء **معلومات ذات الصلة** > قسم **المشروعات المقترنة‬**).</span><span class="sxs-lookup"><span data-stu-id="c1759-122">In **Fixed assets**, you are able to see an overview of the projects associated with a fixed asset (**Fixed assets** > **Fixed assets** > **Fixed assets** > click on the fixed asset in the **Fixed asset number** field > view the contents in the **Related information** pane > **Associated projects** section).</span></span>

