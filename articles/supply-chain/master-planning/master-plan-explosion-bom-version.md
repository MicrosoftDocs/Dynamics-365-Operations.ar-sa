---
title: تحديد إجمالي المكونات المطلوبة‬ لإصدار قائمة مكونات الصنف‬
description: توضح هذه المقالة سيناريو التخطيط الرئيسي الذي يتضمن تحديد إجمالي المكونات المطلوبة‬ لإصدار قائمة مكونات الصنف‬.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 617d9c3f05f2db30ec075a07b54c4827e668c20e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220838"
---
# <a name="explosion-of-a-bom-version"></a><span data-ttu-id="ed7ff-103">تحديد إجمالي المكونات المطلوبة‬ لإصدار قائمة مكونات الصنف‬</span><span class="sxs-lookup"><span data-stu-id="ed7ff-103">Explosion of a BOM version</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ed7ff-104">توضح هذه المقالة سيناريو التخطيط الرئيسي الذي يتضمن تحديد إجمالي المكونات المطلوبة‬ لإصدار قائمة مكونات الصنف‬.</span><span class="sxs-lookup"><span data-stu-id="ed7ff-104">This article explains a master planning scenario that involves explosion of a bill of materials (BOM) version.</span></span>

<span data-ttu-id="ed7ff-105">تؤدي عملية تحديد إجمالي المكونات المطلوبة لطلب خاص إصدار قائمة مكونات الصنف إلى إنشاء طلب لكل صنف بند في قائمة مكونات الصنف في موقع محدد وربما في مستودع محدد.</span><span class="sxs-lookup"><span data-stu-id="ed7ff-105">A demand explosion of a bill of materials (BOM) version creates a demand for each BOM line item at a specific site and, possibly, at a specific warehouse.</span></span> <span data-ttu-id="ed7ff-106">وفي قائمة مكونات الصنف الخاصة بأحد المواقع، يمكن تحديد مستودع خاص لكل بند في قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="ed7ff-106">In a site-specific BOM, a specific warehouse can be defined for each BOM line.</span></span> <span data-ttu-id="ed7ff-107">بالإضافة إلى ذلك، تحدد إعدادات بُعد الصنف بالنسبة لكل بند في قائمة مكونات الصنف ما إذا كان المستودع مطلوبًا أم لا.</span><span class="sxs-lookup"><span data-stu-id="ed7ff-107">Additionally, for each BOM line, the item's dimension settings determine whether the warehouse is required.</span></span> <span data-ttu-id="ed7ff-108">وبدوره يصبح هذا الطلب الناتج لكل صنف بند في قائمة مكونات الصنف نقطة البدء لتحديد إجمالي المكونات المطلوبة للطلب الإضافي.</span><span class="sxs-lookup"><span data-stu-id="ed7ff-108">The resulting demand for each BOM line item then becomes the starting point for additional demand explosion.</span></span> <span data-ttu-id="ed7ff-109">يتضمن سيناريو التخطيط الرئيسي هذا الشروط التالية:</span><span class="sxs-lookup"><span data-stu-id="ed7ff-109">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="ed7ff-110">بُعد الموقع إلزامي، ويجب إدخاله في حركة الطلب.</span><span class="sxs-lookup"><span data-stu-id="ed7ff-110">The site dimension is mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="ed7ff-111">بُعد الموقع متناسق.</span><span class="sxs-lookup"><span data-stu-id="ed7ff-111">The site dimension is consistent.</span></span> <span data-ttu-id="ed7ff-112">لذلك فالموقع للطلب من المستوى الأدنى هو نفس الموقع في حركة الطلب المبدئي.</span><span class="sxs-lookup"><span data-stu-id="ed7ff-112">Therefore, the site for lower-level demand is the same as the site on the initial demand transaction.</span></span>

<span data-ttu-id="ed7ff-113">يوضح الرسم التخطيطي التالي الكيفية التي تتم بها عملية تحديد إجمالي المكونات المطلوبة لطلب التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="ed7ff-113">The following illustration shows how the process for master planning demand explosion.</span></span> ![طلب عملية تحديد إجمالي المكونات المطلوبة باستخدام إصدار شجرة المواد](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="additional-resources"></a><span data-ttu-id="ed7ff-115">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="ed7ff-115">Additional resources</span></span>
--------

[<span data-ttu-id="ed7ff-116">تحديد إصدار BOM</span><span class="sxs-lookup"><span data-stu-id="ed7ff-116">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)

[<span data-ttu-id="ed7ff-117">نظرة عامة على التخطيط الرئيسي ووظائف المواقع المتعددة</span><span class="sxs-lookup"><span data-stu-id="ed7ff-117">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]