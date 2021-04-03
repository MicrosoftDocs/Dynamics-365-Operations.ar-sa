---
title: تحديث التكاليف المعيارية في بيئة تصنيع
description: توفر هذه المقالة إرشادات حول كيفية تحديث التكاليف المعيارية في بيئة غير مصنعة.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79663
ms.assetid: 3a7c3d13-8dbc-442d-a281-ac0ebe99ec83
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 726eccdc8a9350a292ba719784b5db99afdfad4f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5262419"
---
# <a name="update-standard-costs-in-a-manufacturing-environment"></a><span data-ttu-id="ca126-103">تحديث التكاليف المعيارية في بيئة تصنيع</span><span class="sxs-lookup"><span data-stu-id="ca126-103">Update standard costs in a manufacturing environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ca126-104">توفر هذه المقالة إرشادات حول كيفية تحديث التكاليف المعيارية في بيئة غير مصنعة.</span><span class="sxs-lookup"><span data-stu-id="ca126-104">This article provides guidance about how to update standard costs in a manufacturing environment.</span></span> 

<span data-ttu-id="ca126-105">بإمكان التحديثات أن تعكس أصنافًا جديدة أو فئات تكلفة أو معادلات لحساب التكلفة غير المباشرة.</span><span class="sxs-lookup"><span data-stu-id="ca126-105">Updates can reflect new items, cost categories, or indirect cost calculation formulas.</span></span> <span data-ttu-id="ca126-106">ويمكنها أن تعكس أيضًا تصحيحات وتغييرات في التكاليف.</span><span class="sxs-lookup"><span data-stu-id="ca126-106">They can also reflect corrections and cost changes.</span></span> <span data-ttu-id="ca126-107">يؤثر نوع التحديث على الخطوات التي يجب عليك إكمالها لتحديث التكاليف المعيارية، كما هو موضح في الحالات التالية:</span><span class="sxs-lookup"><span data-stu-id="ca126-107">The type of update affects the steps that you must complete to update standard costs, as illustrated in the following cases:</span></span>

-   <span data-ttu-id="ca126-108">أدخل تغييرات التكلفة المعيارية المتوقعة للأصناف المشتراة، ثم قم بتغيير حالة سجلات تكلفة الصنف إلى **نشط** في التاريخ المناسب</span><span class="sxs-lookup"><span data-stu-id="ca126-108">Enter expected standard cost changes for purchased items, and then change the status of the item cost records to **Active** on the appropriate date.</span></span> <span data-ttu-id="ca126-109">ولكن لا تقم بإعادة حساب تكاليف الأصناف المصنعة التي تستخدم الأصناف المشتراة.</span><span class="sxs-lookup"><span data-stu-id="ca126-109">However, don't recalculate the costs of manufactured items that use the purchased items.</span></span>
-   <span data-ttu-id="ca126-110">أدخل التكاليف المعيارية لصنف مشترى جديد، ولكن لا تقم بإعادة حساب تكاليف الأصناف المصنعة التي لديها إصدار قائمة مكونات الصنف الذي يحتوي على الصنف المشترى الجديد كمكون.</span><span class="sxs-lookup"><span data-stu-id="ca126-110">Enter standard costs for a new purchased item, but don't recalculate the costs of manufactured items that have a bill of materials (BOM) version that contains the new purchased item as a component.</span></span>
-   <span data-ttu-id="ca126-111">قم بتصحيح أو تغيير تكلفة صنف مشترى، أو تغيير مجموعة التكلفة التي تم تعيينها لصنف مشترى، ثم احسب تكلفة كل الأصناف المصنعة التي لديها إصدار قائمة مكونات الصنف الذي يحتوي على الصنف المشترى كمكون.</span><span class="sxs-lookup"><span data-stu-id="ca126-111">Correct or change the cost of a purchased item, or change the cost group that is assigned to a purchased item, and calculate the cost for all manufactured items that have a BOM version that contains the purchased item as a component.</span></span>
-   <span data-ttu-id="ca126-112">قم بتغيير التكلفة لفئة تكلفة، واحسب التكلفة كل الأصناف المصنعة التي لديها إصدار مسار يحتوي على عمليات التوجيه التي تستعمل فئة التكلفة.</span><span class="sxs-lookup"><span data-stu-id="ca126-112">Change the cost for a cost category, and calculate the cost for all manufactured items that have a route version that contains routing operations that use the cost category.</span></span>
-   <span data-ttu-id="ca126-113">قم بتغيير فئات التكلفة التي تم تعيينها لعمليات التوجيه أو مجموعة التكلفة المعينة لفئات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="ca126-113">Change the cost categories that are assigned to routing operations or the cost group that is assigned to cost categories.</span></span> <span data-ttu-id="ca126-114">بعد ذلك، احسب تكلفة كل الأصناف المصنعة التي لديها إصدار مسار يحتوي على عمليات التوجيه التي تستعمل فئة التكلفة.</span><span class="sxs-lookup"><span data-stu-id="ca126-114">Then calculate the cost for all manufactured items that have a route version that contains routing operations that use the cost category.</span></span>
-   <span data-ttu-id="ca126-115">قم بتغيير معادلة التكلفة غير المباشرة، ثم احسب التكلفة لكل الأصناف المصنعة التي تتأثر بالتغيير.</span><span class="sxs-lookup"><span data-stu-id="ca126-115">Change an indirect cost calculation formula, and calculate the cost for all manufactured items that are affected by the change.</span></span>
-   <span data-ttu-id="ca126-116">قم بتغيير موقع التصنيع للصنف المصّنع أو إضافته، ثم احسب تكلفة تصنيع الصنف للموقع.</span><span class="sxs-lookup"><span data-stu-id="ca126-116">Change or add a manufacturing site for a manufactured item, and calculate the item's manufactured cost for the site.</span></span>
-   <span data-ttu-id="ca126-117">احسب، أو أعد حساب، تكلفة صنف مصّنع، ثم أعد حساب تكلفة كل الأصناف المصنعة التي لديها إصدار قائمة مكونات الصنف الذي يحتوي على الصنف المصنع كمكون.</span><span class="sxs-lookup"><span data-stu-id="ca126-117">Calculate, or recalculate, the cost for a manufactured item, and recalculate the cost for all manufactured items that have a BOM version that contains the manufactured item as a component.</span></span>
-   <span data-ttu-id="ca126-118">احسب تكاليف صنف مصّنع جديد بناءً على معلومات المسار وقائمة مكونات الصنف المعرفة والمعتمدة والنشطة.</span><span class="sxs-lookup"><span data-stu-id="ca126-118">Calculate costs for a new manufactured item, based on its defined, approved, and active BOM and route information.</span></span>

<span data-ttu-id="ca126-119">تتطلب كل حالة مراعاة خاصة حول كيفية تحديث التكاليف القياسية.</span><span class="sxs-lookup"><span data-stu-id="ca126-119">Each case requires careful consideration about how to update standard costs.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]