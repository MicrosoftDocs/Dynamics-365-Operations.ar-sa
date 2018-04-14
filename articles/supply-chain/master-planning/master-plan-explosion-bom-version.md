---
title: "تحديد إجمالي المكونات المطلوبة‬ لإصدار قائمة مكونات الصنف‬"
description: "توضح هذه المقالة سيناريو التخطيط الرئيسي الذي يتضمن تحديد إجمالي المكونات المطلوبة‬ لإصدار قائمة مكونات الصنف‬."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: bce6ffd0ee284f2a5e5b5fef0bdfa92e192b2f42
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---

# <a name="explosion-of-a-bom-version"></a><span data-ttu-id="145c3-103">تحديد إجمالي المكونات المطلوبة‬ لإصدار قائمة مكونات الصنف‬</span><span class="sxs-lookup"><span data-stu-id="145c3-103">Explosion of a BOM version</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="145c3-104">توضح هذه المقالة سيناريو التخطيط الرئيسي الذي يتضمن تحديد إجمالي المكونات المطلوبة‬ لإصدار قائمة مكونات الصنف‬.</span><span class="sxs-lookup"><span data-stu-id="145c3-104">This article explains a master planning scenario that involves explosion of a bill of materials (BOM) version.</span></span>

<span data-ttu-id="145c3-105">تؤدي عملية تحديد إجمالي المكونات المطلوبة لطلب خاص إصدار قائمة مكونات الصنف إلى إنشاء طلب لكل صنف بند في قائمة مكونات الصنف في موقع محدد وربما في مستودع محدد.</span><span class="sxs-lookup"><span data-stu-id="145c3-105">A demand explosion of a bill of materials (BOM) version creates a demand for each BOM line item at a specific site and, possibly, at a specific warehouse.</span></span> <span data-ttu-id="145c3-106">وفي قائمة مكونات الصنف الخاصة بأحد المواقع، يمكن تحديد مستودع خاص لكل بند في قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="145c3-106">In a site-specific BOM, a specific warehouse can be defined for each BOM line.</span></span> <span data-ttu-id="145c3-107">بالإضافة إلى ذلك، تحدد إعدادات بُعد الصنف بالنسبة لكل بند في قائمة مكونات الصنف ما إذا كان المستودع مطلوبًا أم لا.</span><span class="sxs-lookup"><span data-stu-id="145c3-107">Additionally, for each BOM line, the item's dimension settings determine whether the warehouse is required.</span></span> <span data-ttu-id="145c3-108">وبدوره يصبح هذا الطلب الناتج لكل صنف بند في قائمة مكونات الصنف نقطة البدء لتحديد إجمالي المكونات المطلوبة للطلب الإضافي.</span><span class="sxs-lookup"><span data-stu-id="145c3-108">The resulting demand for each BOM line item then becomes the starting point for additional demand explosion.</span></span> <span data-ttu-id="145c3-109">يتضمن سيناريو التخطيط الرئيسي هذا الشروط التالية:</span><span class="sxs-lookup"><span data-stu-id="145c3-109">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="145c3-110">بُعد الموقع إلزامي، ويجب إدخاله في حركة الطلب.</span><span class="sxs-lookup"><span data-stu-id="145c3-110">The site dimension is mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="145c3-111">بُعد الموقع متناسق.</span><span class="sxs-lookup"><span data-stu-id="145c3-111">The site dimension is consistent.</span></span> <span data-ttu-id="145c3-112">لذلك فالموقع للطلب من المستوى الأدنى هو نفس الموقع في حركة الطلب المبدئي.</span><span class="sxs-lookup"><span data-stu-id="145c3-112">Therefore, the site for lower-level demand is the same as the site on the initial demand transaction.</span></span>

<span data-ttu-id="145c3-113">يوضح الرسم التخطيطي التالي الكيفية التي تتم بها عملية تحديد إجمالي المكونات المطلوبة لطلب التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="145c3-113">The following illustration shows how the process for master planning demand explosion.</span></span> ![طلب عملية تحديد إجمالي المكونات المطلوبة باستخدام إصدار شجرة المواد](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="see-also"></a><span data-ttu-id="145c3-115">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="145c3-115">See also</span></span>
--------

[<span data-ttu-id="145c3-116">التخطيط الرئيسي - كيفية تحديد إصدار قائمة مكونات الصنف</span><span class="sxs-lookup"><span data-stu-id="145c3-116">Master planning - how the BOM version is determined</span></span>](master-plan-bom-version-determined.md)

[<span data-ttu-id="145c3-117">التخطيط الرئيسي ووظائف المواقع المتعددة</span><span class="sxs-lookup"><span data-stu-id="145c3-117">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)




