---
title: إعادة تصنيف الأصول الثابتة
description: لإعادة تصنيف أصل ثابت، يتعين عليك تحويله إلى مجموعة أصول ثابتة جديدة، أو تعيين رقم أصل ثابت جديد له في نفس المجموعة.
author: saraschi2
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8935213c4629de408a48df5e54a2122324e1b3e7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823922"
---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="f135d-103">إعادة تصنيف الأصول الثابتة</span><span class="sxs-lookup"><span data-stu-id="f135d-103">Reclassify fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f135d-104">لإعادة تصنيف أصل ثابت، يتعين عليك تحويله إلى مجموعة أصول ثابتة جديدة، أو تعيين رقم أصل ثابت جديد له في نفس المجموعة.</span><span class="sxs-lookup"><span data-stu-id="f135d-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="f135d-105">عند إعادة تصنيف أصل ثابت:</span><span class="sxs-lookup"><span data-stu-id="f135d-105">When a fixed asset is reclassified:</span></span>

* <span data-ttu-id="f135d-106">يتم إنشاء كل دفاتر الأصول الثابتة الموجودة للأصل الثابت الجديد.</span><span class="sxs-lookup"><span data-stu-id="f135d-106">All books for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="f135d-107">يتم نسخ أية معلومات كانت معدة للأصل الثابت الأولي إلى الأصل الثابت الجديد.</span><span class="sxs-lookup"><span data-stu-id="f135d-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="f135d-108">تكون حالة الدفاتر للأصل الثابت الأولي "مغلق".</span><span class="sxs-lookup"><span data-stu-id="f135d-108">The status of the books for the original fixed asset is Closed.</span></span> 

* <span data-ttu-id="f135d-109">تحتوي الدفاتر الجديدة للأصل الثابت الجديد على تاريخ إعادة التصنيف في الحقل **تاريخ الاستحواذ**.</span><span class="sxs-lookup"><span data-stu-id="f135d-109">The new books of the new fixed asset contain the date of the reclassification in the **Acquisition date** field.</span></span> <span data-ttu-id="f135d-110">يتم نسخ التاريخ الموجود في حقل **تاريخ تشغيل الإهلاك** من معلومات الأصل الأولي.</span><span class="sxs-lookup"><span data-stu-id="f135d-110">The date in the **Depreciation run date** field is copied from the original asset information.</span></span> <span data-ttu-id="f135d-111">إذا كان الإهلاك قد بدأ بالفعل، فسيعرض الحقل **التاريخ الذي تم فيه آخر تشغيل للإهلاك** تاريخ إعادة التصنيف.</span><span class="sxs-lookup"><span data-stu-id="f135d-111">If the depreciation has already started, the **Date when depreciation was last run** field displays the date of the reclassification.</span></span> 

* <span data-ttu-id="f135d-112">يتم إلغاء حركات الأصل الثابت الموجود للأصل الثابت الأولي، ويعاد إنشاءها للأصل الثابت الجديد.</span><span class="sxs-lookup"><span data-stu-id="f135d-112">The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

<span data-ttu-id="f135d-113">اتبع هذه الخطوات لإعادة تصنيف أحد الأصول الثابتة:</span><span class="sxs-lookup"><span data-stu-id="f135d-113">Follow these steps to reclassify a fixed asset:</span></span>

1. <span data-ttu-id="f135d-114">انتقل إلى **الأصول الثابتة > المهام الدورية > إعادة تصنيف.**</span><span class="sxs-lookup"><span data-stu-id="f135d-114">Go to **Fixed assets > Periodic tasks > Reclassification.**</span></span>
2. <span data-ttu-id="f135d-115">في حقل **مجموعة الأصول الثابتة** حدد المجموعة لإعادة تصنيفها.</span><span class="sxs-lookup"><span data-stu-id="f135d-115">In the **Fixed asset group** field, select the group to reclassify.</span></span>
3. <span data-ttu-id="f135d-116">في حقل **رقم الأصل الثابت**، حدد الأصل الثابت‏‎ لإعادة تصنيفه.</span><span class="sxs-lookup"><span data-stu-id="f135d-116">In the **Fixed asset number** field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="f135d-117">في حقل **مجموعة الأصول الثابتة الجديدة**، حدد مجموعة لتحويل الأصل الثابت إليها.</span><span class="sxs-lookup"><span data-stu-id="f135d-117">In the **New fixed asset group** field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="f135d-118">إذا كانت مجموعة الأصول الثابتة الجديدة مرفقة بتسلسل رقمي، فسيتم تحديث حقل  **رقم الأصل الثابت الجديد** بواسطة الرقم من التسلسل الرقمي لمجموعة الأصول الثابتة الجديدة.</span><span class="sxs-lookup"><span data-stu-id="f135d-118">If the new fixed asset group is attached to a number sequence, the **New fixed asset number** field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="f135d-119">وإلا، فسيتم تحديث حقل **رقم الأصل الثابت الجديد** برقم من التسلسل الرقمي الذي تم إعداده في صفحة **محددات الأصول الثابتة**.</span><span class="sxs-lookup"><span data-stu-id="f135d-119">Otherwise, the **New fixed asset number** field is updated with the number from the number sequence that is set up on the **Fixed asset parameters** page.</span></span> <span data-ttu-id="f135d-120">إذا لم يتم إعداد تسلسل رقمي في صفحة  **محددات الأصول الثابتة**، فأدخل رقمًا في الحقل **رقم الأصل الثابت الجديد**.</span><span class="sxs-lookup"><span data-stu-id="f135d-120">If a number sequence is not set up on the **Fixed asset parameters** page, enter a number in the **New fixed asset number** field.</span></span>  
5. <span data-ttu-id="f135d-121">في حقل **تاريخ إعادة التصنيف**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="f135d-121">In the **Reclassification date** field, enter a date.</span></span>
6. <span data-ttu-id="f135d-122">في حقل **مسلسل الإيصال**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f135d-122">In the **Voucher series** field, enter or select a value.</span></span>
7. <span data-ttu-id="f135d-123">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f135d-123">Click **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]