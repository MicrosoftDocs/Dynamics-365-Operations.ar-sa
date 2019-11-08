---
title: أوامر العمل والأصول الثابتة
description: يشرح هذا الموضوع أوامر العمل والأصول الثابتة في إدارة الأصول.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
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
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c87a2b94692e279a9c2f35dc38ac87bfd9bf7d27
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626214"
---
# <a name="work-orders-and-fixed-assets"></a><span data-ttu-id="045af-103">أوامر العمل والأصول الثابتة</span><span class="sxs-lookup"><span data-stu-id="045af-103">Work orders and fixed assets</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="045af-104">في إدارة الأصول، يمكن ربط الأصول بالأصول الثابتة، ويمكن إنشاء أوامر عمل لهذه الأصول.</span><span class="sxs-lookup"><span data-stu-id="045af-104">In Asset Management, assets can be related to fixed assets, and you can create work orders for those assets.</span></span> <span data-ttu-id="045af-105">إذا استخدمت هذه الوظيفة، يمكنك الحصول على نظرة عامة كاملة على الأصول الثابتة ومشاريع الاستثمار ذات الصلة والتكاليف المسجلة على مشاريع الاستثمار في الوحدة النمطية **إدارة المشاريع ومحاسبتها** والوحدة النمطية **الأصول الثابتة** في Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="045af-105">If you use this functionality, you can get a complete overview of fixed assets, related investment projects, and the costs that are registered on the investment projects in the **Project management and accounting** and **Fixed assets** modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

>[!NOTE]
><span data-ttu-id="045af-106">يتم تعيين حقل **رقم الأصل الثابت** فقط في مشروع وظيفة أمر العمل في حالة تحديد **الاستثمار** كنوع المشروع في مشروع وظيفة أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="045af-106">The **Fixed asset number** field on the work order job project is set only if **Investment** is selected as the project type on the work order job project.</span></span>

<span data-ttu-id="045af-107">يوضح الرسم التوضيحي أدناه العلاقة بين مشروع استثمار في الوحدة النمطية **‏‫إدارة المشاريع ومحاسبتها‬** ومشروع وظيفة أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="045af-107">The illustration below shows the relation between an investment project in the **Project management and accounting** module and a work order job project.</span></span>

![الشكل 1](media/24-work-orders.png)

<span data-ttu-id="045af-109">يصف الإجراء التالي العلاقة بين الأصول وأوامر العمل ومشاريع وظائف أمر العمل والأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="045af-109">The following procedure describes the relation between assets, work orders, work order job projects, and fixed assets.</span></span>

1. <span data-ttu-id="045af-110">يمكنك إنشاء أصل مرتبط بأصل ثابت.</span><span class="sxs-lookup"><span data-stu-id="045af-110">You create an asset that you relate to a fixed asset.</span></span>

![الشكل 2](media/25-work-orders.png)

2. <span data-ttu-id="045af-112">عند إعداد أنواع أوامر العمل على صفحة **أنواع أوامر العمل** (**إدارة الأصول** > **الإعداد** > **أوامر العمل** > **أنواع أوامر العمل**)، تنشئ نوع أمر عمل للتعامل مع الاستثمارات.</span><span class="sxs-lookup"><span data-stu-id="045af-112">When you set up work order types on the **Work order types** page (**Asset management** > **Setup** > **Work orders** > **Work order types**), you create a work order type for handling investments.</span></span> <span data-ttu-id="045af-113">راجع أيضًا [أنواع أوامر العمل](../setup-for-work-orders/work-order-types.md).</span><span class="sxs-lookup"><span data-stu-id="045af-113">See also [Work order types](../setup-for-work-orders/work-order-types.md).</span></span>

![الشكل 3](media/26-work-orders.png)

3. <span data-ttu-id="045af-115">عندما تقوم بإعداد مجموعات مشاريع أوامر العمل على علامة التبويب على علامة التبويب **مجموعة المشروع** بصفحة **‏‫إعداد مشروع أمر العمل‬** (**إدارة الأصول** > **الإعداد** > **أوامر العمل** > **إعداد المشروع**)، تنشئ علاقة بين نوع أمر العمل المستخدم للاستثمارات ومجموعة المشاريع التي تم إنشاؤها للاستثمارات في صفحة **مجموعات المشاريع** في الوحدة النمطية **إدارة المشاريع ومحاسبتها** (**إدارة المشاريع ومحاسبتها** > **الإعداد** > **الترحيل** > **مجموعات المشاريع**).</span><span class="sxs-lookup"><span data-stu-id="045af-115">When you set up work order project groups on the **Project group** tab of the **Work order project setup** page (**Asset management** > **Setup** > **Work orders** > **Project setup**), you create a relation between the work order type that is used for investments and the project group that was created for investments on the **Project groups** page in the **Project management and accounting** module (**Project management and accounting** > **Setup** > **Posting** > **Project groups**).</span></span>

![الشكل 4](media/27-work-orders.png)

4. <span data-ttu-id="045af-117">عندما تنشئ أمر عمل يتعلق بأصل ثابت، فأنت تحدد نوع أمر العمل المستخدم للتعامل مع الاستثمارات، على سبيل المثال، **استثمار**.</span><span class="sxs-lookup"><span data-stu-id="045af-117">When you create a work order that is related to a fixed asset, you select the work order type that is used to handle investments, such as **Investment**.</span></span>

5. <span data-ttu-id="045af-118">عند إنشاء أمر العمل، يتم عرض نوع أمر العمل المرتبط في **جميع أوامر العمل‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="045af-118">When the work order is created, the related work order type is shown on the **All work orders** page.</span></span>

![الشكل 5](media/28-work-orders.png)

6. <span data-ttu-id="045af-120">عند إنشاء أمر العمل، يتم إنشاء المشروع المرتبط بأمر العمل على صفحة**جميع المشروعات** في الوحدة النمطية **‏‫إدارة المشاريع ومحاسبتها‬** (**‏‫إدارة المشاريع ومحاسبتها‬** > **المشاريع** > **جميع المشاريع**).</span><span class="sxs-lookup"><span data-stu-id="045af-120">When the work order is created, the project that is related to the work order is created on the **All projects** page in the **Project management and accounting** module (**Project management and accounting** > **Projects** > **All projects**).</span></span> <span data-ttu-id="045af-121">لعرض المعلومات المتعلقة بالمشروع، حدد الارتباط في الحقل **معرف المشروع** ضمن علامة التبويب **عام** على علامة التبويب السريعة **‏‫تفاصيل السطر‬** في طريقة عرض التفاصيل في صفحة **جميع أوامر العمل** في الوحدة النمطية **إدارة الأوصول** (**إدارة الأوصول** > **عام** > **أوامر العمل** > **جميع أوامر العمل**).</span><span class="sxs-lookup"><span data-stu-id="045af-121">To view project-related information, select the link in the **Project ID** field on the **General** tab on the **Line details** FastTab in the details view of the **All work orders** page in the **Asset management** module (**Asset management** > **Commom** > **Work orders** > **All work orders**).</span></span>

![الشكل 6](media/29-work-orders.png)

7. <span data-ttu-id="045af-123">للاطلاع على نظرة عامة على المشاريع المقترنة بالأصل الثابت، حدد **الأصول الثابتة** > **الأصول الثابتة** > **الأصول الثابتة**، ثم في الحقل **رقم الأصل الثابت**، حدد الارتباط الخاص بالأصل الثابت لفتح طريقة عرض التفاصيل.</span><span class="sxs-lookup"><span data-stu-id="045af-123">To see an overview of the projects associated with a fixed asset, select **Fixed assets** > **Fixed assets** > **Fixed assets**, and then, in the **Fixed asset number** field, select the link for the fixed asset to open the details view.</span></span> <span data-ttu-id="045af-124">قم بتوسيع الجزء **‏‫المعلومات ذات الصلة** على الجانب الأيمن من الصفحة، ثم حدد علامة التبويب السرعية **‏‫المشروعات المقترنة‬**.</span><span class="sxs-lookup"><span data-stu-id="045af-124">Expand the **Related information** pane on the right side of the page, and select the **Associated projects** FastTab.</span></span>

