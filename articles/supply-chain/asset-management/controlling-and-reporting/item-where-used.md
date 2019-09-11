---
title: عنصر موجود في المكان المحدد لاستخدامه لاحقاً
description: يوضح هذا الموضوع كيفية الحصول على نظرة عامة حول مكان استخدام عنصر ما في إدارة الأصول.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 84ab803aedf5b803b6c5f39ff1907726335cb45d
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918316"
---
# <a name="item-where-used"></a><span data-ttu-id="910e9-103">عنصر موجود في المكان المحدد لاستخدامه لاحقاً</span><span class="sxs-lookup"><span data-stu-id="910e9-103">Item where used</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="910e9-104">يمكنك عمل حساب لصنف محدد للحصول على نظرة عامة حول المكان الذي تم فيه استخدام الصنف في إدارة الأصول.</span><span class="sxs-lookup"><span data-stu-id="910e9-104">You can make a calculation for a specific item to get an overview of where in Asset Management the item has been used.</span></span> <span data-ttu-id="910e9-105">تظهر النتائج السياق الذي تم استخدام الصنف به أثناء فترة حياته.</span><span class="sxs-lookup"><span data-stu-id="910e9-105">The results show the context in which the item has been used during its lifetime.</span></span> <span data-ttu-id="910e9-106">يمكن فتح صفحة **مكان استخدام الصنف** من قائمة إدارة الأصول الرئيسية، كما يمكن الوصول إليها من الصفحات التالية:</span><span class="sxs-lookup"><span data-stu-id="910e9-106">The **Item where used** page can be opened from the main Asset management menu, and it can also be accessed from the following pages:</span></span>

[<span data-ttu-id="910e9-107">BOM الأصل</span><span class="sxs-lookup"><span data-stu-id="910e9-107">Asset BOM</span></span>](../objects/object-BOM.md)

[<span data-ttu-id="910e9-108">قطع الغيار في الإعدادات الافتراضية لنوع الأصل</span><span class="sxs-lookup"><span data-stu-id="910e9-108">Spare parts on asset type defaults</span></span>](../setup-for-objects/object-types.md)

[<span data-ttu-id="910e9-109">التنبؤ بالأصناف على التنبؤ بالإعدادات الافتراضية لنوع مهمة الصيانة</span><span class="sxs-lookup"><span data-stu-id="910e9-109">Item forecast on Maintenance job type defaults forecast</span></span>](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

[<span data-ttu-id="910e9-110">التنبؤ بمتطلبات الصيانة لأمر العمل</span><span class="sxs-lookup"><span data-stu-id="910e9-110">Work order maintenance forecast</span></span>](../work-orders/maintenance-forecasts.md)

[<span data-ttu-id="910e9-111">طلب الشراء لأمر العمل</span><span class="sxs-lookup"><span data-stu-id="910e9-111">Work order purchase requisition</span></span>](../work-orders/procurement.md)

[<span data-ttu-id="910e9-112">شراء أمر العمل</span><span class="sxs-lookup"><span data-stu-id="910e9-112">Work order purchase</span></span>](../work-orders/procurement.md)

## <a name="make-an-item-where-used-calculation"></a><span data-ttu-id="910e9-113">إجراء حساب مكان-استخدام-الصنف</span><span class="sxs-lookup"><span data-stu-id="910e9-113">Make an item-where-used calculation</span></span>

1. <span data-ttu-id="910e9-114">انقر فوق **إدارة الأصول** > **استعلامات‬** > **مكان استخدام الصنف**، أو حدد زر **مكان استخدام الصنف** في إحدى الصفحات المذكورة أعلاه.</span><span class="sxs-lookup"><span data-stu-id="910e9-114">Click **Asset management** > **Inquiries** > **Item where used**, or select the **Item where used** button on one of the pages mentioned above.</span></span>

2. <span data-ttu-id="910e9-115">في مربع الحوار **مكان استخدام الصنف**، حدد الصنف الذي تريد إجراء الحساب له في الحقل **رقم الصنف**.</span><span class="sxs-lookup"><span data-stu-id="910e9-115">In the **Item where used** dialog, select the item for which you want to make the calculation in the **Item number** field.</span></span>

3. <span data-ttu-id="910e9-116">يمكنك استخدام حقل **المستوى** للإشارة إلى مستوى التفصيل الذي ترغب فيه في بنود الصنف فيما يتعلق بمواقع العمل.</span><span class="sxs-lookup"><span data-stu-id="910e9-116">You can use the **Level** field to indicate how detailed you want the item lines to be regarding functional locations.</span></span> <span data-ttu-id="910e9-117">على سبيل المثال، إذا قمت بإدخال الرقم "1" في الحقل، وكانت لديك بنية موقع عمل متعددة المستويات، سيتم عرض كافة بنود الصنف لموقع العمل في المستوى الأعلى.</span><span class="sxs-lookup"><span data-stu-id="910e9-117">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all item lines for a functional location will be shown on the top level.</span></span> <span data-ttu-id="910e9-118">وبالتالي، يمكن إضافة علاقة/كميه في البند من مواقع العمل الموجودة في مستوى أدنى.</span><span class="sxs-lookup"><span data-stu-id="910e9-118">Therefore, relation/quantity on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="910e9-119">إذا قمت بإدخال الرقم "0" في حقل **المستوى**، فسترى نتيجة مفصلة تعرض جميع بنود الصنف على جميع مستويات مواقع العمل التي ترتبط بها.</span><span class="sxs-lookup"><span data-stu-id="910e9-119">If you insert the number "0" in the **Level** field, you will see a detailed result showing all item lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="910e9-120">في القسم **تضمين**، حدد "نعم" على أزرار التبديل التي تريد تضمينها في الحساب.</span><span class="sxs-lookup"><span data-stu-id="910e9-120">In the **Include** section, select "Yes" on the toggle buttons that you want to include in the calculation.</span></span>

5. <span data-ttu-id="910e9-121">انقر فوق **موافق** لبدء الحساب.</span><span class="sxs-lookup"><span data-stu-id="910e9-121">Click **OK** to start the calculation.</span></span>

6. <span data-ttu-id="910e9-122">في علامة التبويب **مكان استخدام الصنف** > مجموعات جزء الإجراءات **تجميع حسب‬...**، حدد الأزرار ذات الصلة لإظهار مستوى التفاصيل المطلوب للحساب.</span><span class="sxs-lookup"><span data-stu-id="910e9-122">On the **Item where used** tab > **Group by...** action pane groups, select the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="910e9-123">يتم تمييز أزرار جزء الإجراءات المحددة.</span><span class="sxs-lookup"><span data-stu-id="910e9-123">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="910e9-124">انقر فوق زر لتنشيطه أو إلغاء تنشيطه.</span><span class="sxs-lookup"><span data-stu-id="910e9-124">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="910e9-125">إذا كنت ترغب في عرض الأبعاد المرتبطة بالصنف، فانقر فوق **عرض الأبعاد**، العرض، ثم حدد الأبعاد التي سيتم عرضها.</span><span class="sxs-lookup"><span data-stu-id="910e9-125">If you want to show dimensions related to the item, click **Display dimensions**, and select the dimensions to be shown.</span></span>

<span data-ttu-id="910e9-126">في الشكل المبين أدناه، ستري مثالاً لحساب مكان-استخدام-الصنف للصنف رقم "1000".</span><span class="sxs-lookup"><span data-stu-id="910e9-126">In the figure below, you see an example of an item-where-used calculation for item number "1000".</span></span>

![الشكل 1](media/12-controlling-and-reporting.png)

