---
title: عنصر موجود في المكان المحدد لاستخدامه لاحقاً
description: يوضح هذا الموضوع كيفية الحصول على نظرة عامة حول مكان استخدام عنصر ما في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetItemWhereUsed, EntAssetItemWhereUsedCalculate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bc78568e314c7cf83848ed2c39f9613d6ed638ba
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421265"
---
# <a name="item-where-used"></a><span data-ttu-id="3386f-103">عنصر موجود في المكان المحدد لاستخدامه لاحقاً</span><span class="sxs-lookup"><span data-stu-id="3386f-103">Item where used</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="3386f-104">يمكنك عمل حساب لصنف محدد للحصول على نظرة عامة حول المكان الذي تم فيه استخدام الصنف في إدارة الأصول.</span><span class="sxs-lookup"><span data-stu-id="3386f-104">You can make a calculation for a specific item to get an overview of where in Asset Management the item has been used.</span></span> <span data-ttu-id="3386f-105">تظهر النتائج السياق الذي تم استخدام الصنف به أثناء فترة حياته.</span><span class="sxs-lookup"><span data-stu-id="3386f-105">The results show the context in which the item has been used during its lifetime.</span></span> <span data-ttu-id="3386f-106">يمكن فتح الصفحة **صنف مُستخدم** من قائمة إدارة الأصول الرئيسية، كما يمكن الوصول إليها من الصفحات التالية:</span><span class="sxs-lookup"><span data-stu-id="3386f-106">The **Item where used** page can be opened from the main Asset Management menu, and it can also be accessed from the following pages:</span></span>

- [<span data-ttu-id="3386f-107">BOM الأصل</span><span class="sxs-lookup"><span data-stu-id="3386f-107">Asset BOMs</span></span>](../objects/object-BOM.md)

- [<span data-ttu-id="3386f-108">قطع الغيار في الإعدادات الافتراضية لنوع الأصل</span><span class="sxs-lookup"><span data-stu-id="3386f-108">Spare parts on asset type defaults</span></span>](../setup-for-objects/object-types.md#spare-parts-on-the-asset-type-setup)

- [<span data-ttu-id="3386f-109">فئات أنواع مهام الصيانة وأنواع مهام الصيانة، ومتغيرات أنواع مهام الصيانة، ومهن مهام الصيانة، وقوائم فحص الصيانة</span><span class="sxs-lookup"><span data-stu-id="3386f-109">Maintenance job type categories and maintenance job types, maintenance job type variants, maintenance job trades, and maintenance checklists</span></span>](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

- [<span data-ttu-id="3386f-110">التنبؤ بالصيانة</span><span class="sxs-lookup"><span data-stu-id="3386f-110">Maintenance forecast</span></span>](../work-orders/maintenance-forecasts.md)

- [<span data-ttu-id="3386f-111">التدبير</span><span class="sxs-lookup"><span data-stu-id="3386f-111">Procurement</span></span>](../work-orders/procurement.md)

- [<span data-ttu-id="3386f-112">شراء أمر العمل</span><span class="sxs-lookup"><span data-stu-id="3386f-112">Work order purchase</span></span>](../work-orders/procurement.md)

## <a name="make-an-item-where-used-calculation"></a><span data-ttu-id="3386f-113">إجراء حساب مكان-استخدام-الصنف</span><span class="sxs-lookup"><span data-stu-id="3386f-113">Make an item-where-used calculation</span></span>

1. <span data-ttu-id="3386f-114">انقر فوق **إدارة الأصول** > **استعلامات‬** > **مكان استخدام الصنف**، أو حدد زر **مكان استخدام الصنف** في إحدى الصفحات المذكورة أعلاه.</span><span class="sxs-lookup"><span data-stu-id="3386f-114">Click **Asset management** > **Inquiries** > **Item where used**, or select the **Item where used** button on one of the pages mentioned above.</span></span>

2. <span data-ttu-id="3386f-115">في مربع الحوار **مكان استخدام الصنف**، حدد الصنف الذي تريد إجراء الحساب له في الحقل **رقم الصنف**.</span><span class="sxs-lookup"><span data-stu-id="3386f-115">In the **Item where used** dialog, select the item for which you want to make the calculation in the **Item number** field.</span></span>

3. <span data-ttu-id="3386f-116">يمكنك استخدام حقل **المستوى** للإشارة إلى مستوى التفصيل الذي ترغب فيه في بنود الصنف فيما يتعلق بمواقع العمل.</span><span class="sxs-lookup"><span data-stu-id="3386f-116">You can use the **Level** field to indicate how detailed you want the item lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="3386f-117">على سبيل المثال، إذا قمت بإدخال الرقم "1" في الحقل، وكانت لديك بنية موقع عمل متعددة المستويات، سيتم عرض كافة بنود الصنف لموقع العمل في المستوى الأعلى.</span><span class="sxs-lookup"><span data-stu-id="3386f-117">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all item lines for a functional location will be shown on the top level.</span></span> <span data-ttu-id="3386f-118">وبالتالي، يمكن إضافة علاقة/كميه في البند من مواقع العمل الموجودة في مستوى أدنى.</span><span class="sxs-lookup"><span data-stu-id="3386f-118">Therefore, relation/quantity on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="3386f-119">إذا قمت بإدخال الرقم "0" في حقل **المستوى**، فسترى نتيجة مفصلة تعرض جميع بنود الصنف على جميع مستويات مواقع العمل التي ترتبط بها.</span><span class="sxs-lookup"><span data-stu-id="3386f-119">If you insert the number "0" in the **Level** field, you will see a detailed result showing all item lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="3386f-120">في القسم **تضمين**، حدد "نعم" على أزرار التبديل التي تريد تضمينها في الحساب.</span><span class="sxs-lookup"><span data-stu-id="3386f-120">In the **Include** section, select "Yes" on the toggle buttons that you want to include in the calculation.</span></span>

5. <span data-ttu-id="3386f-121">انقر فوق **موافق** لبدء الحساب.</span><span class="sxs-lookup"><span data-stu-id="3386f-121">Click **OK** to start the calculation.</span></span>

6. <span data-ttu-id="3386f-122">في علامة التبويب **صنف مُستخدم** ، حدد الأزرار **تجميع حسب‬** ، لإظهار مستوى التفاصيل المطلوب للحساب.</span><span class="sxs-lookup"><span data-stu-id="3386f-122">On the **Item where used** tab, select the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="3386f-123">يتم تمييز أزرار **تجميع حسب** المحددة.</span><span class="sxs-lookup"><span data-stu-id="3386f-123">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="3386f-124">انقر فوق زر لتنشيطه أو إلغاء تنشيطه.</span><span class="sxs-lookup"><span data-stu-id="3386f-124">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="3386f-125">إذا كنت ترغب في عرض الأبعاد المرتبطة بالصنف، فانقر فوق **عرض الأبعاد**، العرض، ثم حدد الأبعاد التي سيتم عرضها.</span><span class="sxs-lookup"><span data-stu-id="3386f-125">If you want to show dimensions related to the item, click **Display dimensions**, and select the dimensions to be shown.</span></span>

## <a name="example"></a><span data-ttu-id="3386f-126">مثال</span><span class="sxs-lookup"><span data-stu-id="3386f-126">Example</span></span>

<span data-ttu-id="3386f-127">في لقطة الشاشة أدناه، سوف تري مثالاً لحساب الصنف المُستخدم للصنف رقم "1000".</span><span class="sxs-lookup"><span data-stu-id="3386f-127">In the screenshot below, you see an example of an item-where-used calculation for item number "1000".</span></span>

![مثال حساب الصنف المُستخدم](media/12-controlling-and-reporting.png)

